<template>
    <div>
      <div
        @click="toggleIcon"
        class="btn-round w-[4rem] h-[4rem] rounded-full border border-black"
        :class="{
          animated: isDirty,
          plusButton: isPlus && isDirty,
          closeButton: !isPlus,
        }"
      >
        <span
          class="close relative inline-block w-[2rem] h-[2rem] top-[1rem] left-[1rem] overflow-hidden"
        ></span>
      </div>
    </div>
  </template>
  <script setup>
  const isPlus = ref(true);
  const isDirty = ref(false);
  const toggleIcon = () => {
    if (!isDirty.value) {
      isDirty.value = true;
    }
    isPlus.value = !isPlus.value;
  };
  </script>
  <style scoped>
  .close::before,
  .close::after {
    content: "";
    position: absolute;
    height: 2px;
    width: 100%;
    top: 50%;
    left: 0;
    margin-top: -1px;
    background: black;
  }
  
  .btn-round {
    transition: all .2s;
  }
  
  .close {
    transition: all .2s ease-in-out;
  }
  .btn-round:hover {
    background: black;
  }
  .btn-round:hover .close::after {
    content: "";
    position: absolute;
    height: 2px;
    width: 100%;
    top: 50%;
    left: 0;
    margin-top: -1px;
    background: white;
  }
  
  .btn-round:hover .close::before {
    content: "";
    position: absolute;
    height: 2px;
    width: 100%;
    top: 50%;
    left: 0;
    margin-top: -1px;
    background: white;
  }
  .close::before {
    transform: rotate(0deg);
  }
  .close::after {
    transform: rotate(90deg);
  }
  .animated {
    -webkit-animation-duration: 1s;
    animation-duration: 1s;
    -webkit-animation-fill-mode: both;
    animation-fill-mode: both;
  }
  @-webkit-keyframes plusButton {
    from {
      -webkit-transform-origin: center;
      transform-origin: center;
      -webkit-transform: rotate3d(0, 0, 1, -135deg);
      transform: rotate3d(0, 0, 1, -135deg);
    }
  
    to {
      -webkit-transform-origin: center;
      transform-origin: center;
      -webkit-transform: none;
      transform: none;
    }
  }
  
  @keyframes plusButton {
    from {
      -webkit-transform-origin: center;
      transform-origin: center;
      -webkit-transform: rotate3d(0, 0, 1, 135deg);
      transform: rotate3d(0, 0, 1, 135deg);
    }
  
    to {
      -webkit-transform-origin: center;
      transform-origin: center;
      -webkit-transform: none;
      transform: none;
    }
  }
  
  .plusButton {
    -webkit-animation-name: plusButton;
    animation-name: plusButton;
  }
  
  @-webkit-keyframes closeButton {
    from {
      -webkit-transform-origin: center;
      transform-origin: center;
      -webkit-transform: none;
      transform: none;
    }
  
    to {
      -webkit-transform-origin: center;
      transform-origin: center;
      -webkit-transform: rotate3d(0, 0, 1, 135deg);
      transform: rotate3d(0, 0, 1, 135deg);
    }
  }
  
  @keyframes closeButton {
    from {
      -webkit-transform-origin: center;
      transform-origin: center;
      -webkit-transform: none;
      transform: none;
    }
  
    to {
      -webkit-transform-origin: center;
      transform-origin: center;
      -webkit-transform: rotate3d(0, 0, 1, 135deg);
      transform: rotate3d(0, 0, 1, 135deg);
    }
  }
  
  .closeButton {
    -webkit-animation-name: closeButton;
    animation-name: closeButton;
  }
  </style>
  