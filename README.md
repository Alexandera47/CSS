<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>3D Cube Animation</title>
<style>
  .container {
    width: 200px;
    height: 200px;
    perspective: 1000px;
    margin: 100px auto;
  }

  .cube {
    width: 100%;
    height: 100%;
    position: relative;
    transform-style: preserve-3d;
    transform: rotateX(45deg) rotateY(45deg);
    animation: spin 10s linear infinite;
  }

  .face {
    position: absolute;
    width: 200px;
    height: 200px;
    background-color: rgba(255, 0, 0, 0.7);
    border: 1px solid #fff;
    line-height: 200px;
    text-align: center;
    font-size: 24px;
    font-weight: bold;
  }

  .front { transform: translateZ(100px); }
  .back { transform: translateZ(-100px) rotateY(180deg); }
  .right { transform: rotateY(90deg) translateZ(100px); }
  .left { transform: rotateY(-90deg) translateZ(100px); }
  .top { transform: rotateX(90deg) translateZ(100px); }
  .bottom { transform: rotateX(-90deg) translateZ(100px); }

  @keyframes spin {
    0% { transform: rotateX(0deg) rotateY(0deg); }
    100% { transform: rotateX(360deg) rotateY(360deg); }
  }
</style>
</head>
<body>

<div class="container">
  <div class="cube">
    <div class="face front">Front</div>
    <div class="face back">Back</div>
    <div class="face right">Right</div>
    <div class="face left">Left</div>
    <div class="face top">Top</div>
    <div class="face bottom">Bottom</div>
  </div>
</div>

</body>
</html>
