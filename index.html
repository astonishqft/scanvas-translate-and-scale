<!DOCTYPE html>
<html lang="en">

<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <meta http-equiv="X-UA-Compatible" content="ie=edge">
  <title>Canvas鼠标滚轮缩放和拖放</title>
  <style>
    canvas {
      border: solid 1px #000;
      margin: 0px auto;
      display: block;
    }
    .options {
      display: flex;
      justify-content: center;
      height: 44px;
      align-items: center;
    }
    button {
      margin-left: 15px;
    }
  </style>
</head>

<body>
  <div class="options">
    <button onclick="zoomIn()">放大 +</button>
    <button onclick="zoomOut()">缩小 -</button>
    <button onclick="reset()">还原</button>
  </div>
  <canvas id="canvas"></canvas>
  <script>
    class Scene {
      offset = { x: 0, y: 0 }; // 拖动偏移
      curOffset = { x: 0, y: 0 }; // 记录上一次的偏移量
      mousePosition = { x: 0, y: 0 }; // 记录鼠标滚轮点击时的坐标位置
      maxScale = 8;
      minScale = 0.4;
      scaleStep = 0.2;
      scale = 1;
      preScale = 1;

      x = 0; // 记录鼠标点击Canvas时的横坐标
      y = 0; // 记录鼠标点击Canvas时的纵坐标

      constructor(id, options = {
        width: 600,
        height: 400
      }) {
        this.canvas = document.querySelector('#' + id)
        this.width = options.width;
        this.height = options.height;
        this.canvas.width = options.width;
        this.canvas.height = options.height;
        this.ctx = this.canvas.getContext('2d');

        this.onMousedown = this.onMousedown.bind(this);
        this.onMousemove = this.onMousemove.bind(this);
        this.onMouseup = this.onMouseup.bind(this);
        this.onMousewheel = this.onMousewheel.bind(this);
        this.canvas.addEventListener('mousewheel', this.onMousewheel);
        this.canvas.addEventListener('mousedown', this.onMousedown);
      }

      onMousewheel(e) {
        e.preventDefault();

        this.mousePosition.x = e.offsetX; // 记录当前鼠标点击的横坐标
        this.mousePosition.y = e.offsetY; // 记录当前鼠标点击的纵坐标
        if (e.wheelDelta > 0) {
          // 放大
          this.scale = parseFloat((this.scaleStep + this.scale).toFixed(2)); // 解决小数点运算丢失精度的问题
          if (this.scale > this.maxScale) {
            this.scale = this.maxScale;
            return;
          }
        } else {
          // 缩小
          this.scale = parseFloat((this.scale - this.scaleStep).toFixed(2)); // 解决小数点运算丢失精度的问题
          if (this.scale < this.minScale) {
            this.scale = this.minScale;
            return;
          }
        }

        this.zoom();
      }

      zoom() {
        this.offset.x = this.mousePosition.x - (this.mousePosition.x - this.offset.x) * this.scale / this.preScale;
        this.offset.y = this.mousePosition.y - (this.mousePosition.y - this.offset.y) * this.scale / this.preScale;

        this.paint(this.ctx);
        this.preScale = this.scale;
        this.curOffset.x = this.offset.x;
        this.curOffset.y = this.offset.y;
      }

      onMousedown(e) {
        if (e.button === 0) {
          // 鼠标左键
          this.x = e.x;
          this.y = e.y
          window.addEventListener('mousemove', this.onMousemove);
          window.addEventListener('mouseup', this.onMouseup)
        }
      }

      onMousemove(e) {
       this.offset.x = this.curOffset.x + (e.x - this.x);
       this.offset.y = this.curOffset.y + (e.y - this.y);

       this.paint();
      }

      onMouseup() {
        this.curOffset.x = this.offset.x;
        this.curOffset.y = this.offset.y;
        window.removeEventListener('mousemove', this.onMousemove);
        window.removeEventListener('mouseup', this.onMouseup);
      }

      zoomIn() {
        this.scale += this.scaleStep;
        if (this.scale > this.maxScale) {
          this.scale = this.maxScale;
          return;
        }
        this.mousePosition.x = this.width / 2;
        this.mousePosition.y = this.height / 2;
        this.zoom();
      }

      zoomOut() {
        this.scale -= this.scaleStep;
        if (this.scale < this.minScale) {
          this.scale = this.minScale;
          return;
        }
        this.mousePosition.x = this.width / 2;
        this.mousePosition.y = this.height / 2;
        this.zoom();
      }

      // 重置
      reset = function () {
        this.clear();
        this.scale = 1; // 当前缩放
        this.preScale = 1; // 上一次缩放
        this.offset = { x: 0, y: 0 }; // 拖动偏移
        this.curOffset = { x: 0, y: 0 }; // 当前偏移
        this.mousePosition = { x: 0, y: 0 };
        this.draw();
      };

      draw() {
        this.ctx.fillStyle = 'red';
        this.ctx.fillRect(50, 50, 50, 50);

        this.ctx.fillStyle = 'green';
        this.ctx.fillRect(150, 150, 50, 50);
      }

      clear() {
        this.canvas.width = this.width;
      }

      paint() {
        this.clear();
        this.ctx.translate(this.offset.x, this.offset.y);
        this.ctx.scale(this.scale, this.scale);
        this.draw();
      }
    }

    let scene = new Scene('canvas');

    scene.draw();

    // 放大
    function zoomIn() {
      scene.zoomIn();
    }

    // 缩小
    function zoomOut() {
      scene.zoomOut();
    }

    // 还原
    function reset() {
      scene.reset();
    }
  </script>
</body>

</html>
