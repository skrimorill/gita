<template>
    <div class="c-feed">
      <toggler @onToggler="toggle"/>
      <div class="comments" v-if="show">
        <ul class="comments-list">
          <li class="comments-item" v-for="n in 5" :key="n">
            <comment text="Some Text" username="john Doe" />
          </li>
        </ul>
      </div>
    </div>
</template>

import { comment } from '../comment'
import { toggler } from '../toggler'

export default {
    name: 'feed-item',
    components: {
      component,
      toggler
    },
    data () {
      return {
        show: false
      }
    }
    methods: {
      toggle (isOpened) {
        this.shown = isOpened
      }
    }
}


