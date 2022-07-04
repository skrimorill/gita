<template>
<div class="c-comment">
  <p>
    <span class="username">{{ username }}</span>
    {{ text }}
  </p>
</div>
</template>

export default {
    name: 'Comment',
    props: {
        username: {
          type: String,
          required: true
        },
          text: {
          type: String,
          required: true
        }
    }
}