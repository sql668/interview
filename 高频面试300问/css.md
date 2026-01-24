
1. 如何检测CSS动画的FPS

```javascript
class AdvancedFPSDetector {
    constructor() {
        this.frameTimes = [];
        this.lastFrameTime = performance.now();
        this.currentFps = 60;
        this.isRunning = false;
    }
    
    start() {
        this.isRunning = true;
        this.detectFps();
    }
    
    stop() {
        this.isRunning = false;
    }
    
    detectFps() {
        if (!this.isRunning) return;
        
        const now = performance.now();

        // 每帧的间隔时间
        const delta = now - this.lastFrameTime;
        this.lastFrameTime = now;
        
        // 计算瞬时FPS
        const instantFps = Math.min(999, Math.round(1000 / delta));
        
        // 维护最近60帧的时间记录
        this.frameTimes.push(delta);
        if (this.frameTimes.length > 60) {
            this.frameTimes.shift();
        }
        
        // 计算平均FPS
        if (this.frameTimes.length > 0) {
            const averageDelta = this.frameTimes.reduce((a, b) => a + b, 0) / this.frameTimes.length;
            this.currentFps = Math.round(1000 / averageDelta);
        }
        
        console.log(`Instant FPS: ${instantFps}, Average FPS: ${this.currentFps}`);
        
        requestAnimationFrame(() => this.detectFps());
    }
    
    getFps() {
        return this.currentFps;
    }
}

// 使用示例
const fpsDetector = new AdvancedFPSDetector();
fpsDetector.start();

// 5秒后停止检测
setTimeout(() => {
    fpsDetector.stop();
    console.log('Final FPS:', fpsDetector.getFps());
}, 5000);

```