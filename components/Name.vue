<template>
    <div class="main-wrapper">
      <p id="main-name">
        <span>M</span>
        <span>i</span>
        <span>h</span>
        <span>o</span>
        <span>k</span>
        <span>o</span>
        <span>&nbsp;</span>
        <span>O</span>
        <span>h</span>
        <span>a</span>
        <span>r</span>
        <span>a</span>
      </p>
    </div>
</template>

<style lang="scss" scoped>
.main-wrapper{
  height: 730px;
  background: linear-gradient(-135deg, #aa4b6b, #6b6b83, #3b8d99);
}

.main-wrapper p{
  text-align: center;
  font-size: 4em;
  line-height: 730px;
  font-family: 'Cutive Mono', monospace;
  font-weight: bold;
}

span {
	color: transparent;
  animation: blur 10s;
  animation-fill-mode: forwards;
}

span:nth-child(1) {
	animation-delay: 0.1s;
}
span:nth-child(2) {
	animation-delay: 0.2s;
}
span:nth-child(3) {
	animation-delay: 0.3s;
}
span:nth-child(4) {
	animation-delay: 0.4s;
}
span:nth-child(5) {
	animation-delay: 0.5s;
}
span:nth-child(6) {
	animation-delay: 0.6s;
}
span:nth-child(7) {
	animation-delay: 0.7s;
}
span:nth-child(8) {
	animation-delay: 0.8s;
}
span:nth-child(9) {
	animation-delay: 0.9s;
}
span:nth-child(10) {
	animation-delay: 1.0s;
}
span:nth-child(11) {
	animation-delay: 1.1s;
}
span:nth-child(12) {
	animation-delay: 1.2s;
}
span:nth-child(13) {
	animation-delay: 1.3s;
}

@keyframes blur {
    0%		{text-shadow:  0 0 10px #fff; opacity:0;}
	5%		{text-shadow:  0 0 5px #fff;}
	10%		{opacity: 1;}
	100%	{text-shadow:  0 0 0px #fff;}
}

@media screen and (max-width: 1200px) {
  #main-name{
    font-size: 3em;
  }
}

@media screen and (max-width: 480px){
    #main-name{
      font-size: 1.3em;
      line-height: 600px;
    }
}

</style>