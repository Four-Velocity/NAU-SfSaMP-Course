<template>
  <svg
    xmlns="http://www.w3.org/2000/svg"
    :width="width"
    :height="height"
    :viewBox="'0 0 ' + width + ' ' + height"
    fill="none"
  >
    <rect :width="width" :height="height" fill="url(#paint0_radial_5_2)" />
    <defs>
      <radialGradient
        id="paint0_radial_5_2"
        :cx="centerX"
        :cy="centerY"
        r="1"
        gradientUnits="userSpaceOnUse"
        :gradientTransform="`translate(${height / 2} ${
          width / 2
        }) rotate(90) scale(${height / 2})`"
      >
        <stop :stop-color="innerColor" />
        <stop offset="1" :stop-color="outerColor" />
      </radialGradient>
    </defs>
  </svg>
</template>
  <script>
export default {
  name: "Rectangle",
  props: {
    height: { type: Number, default: 500 },
    width: { type: Number, default: 500 },
    innerColor: { type: String, default: "#FF0099" },
    outerColor: { type: String, default: "#EE882a" },
    centerX: { type: Number, required: true },
    centerY: { type: Number, required: true },
  },
};
</script>