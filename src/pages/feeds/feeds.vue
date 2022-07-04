<template>
  <div class="headerline">
    <headerline>
        <template #headerline>
          <div class="icon">
            <icon name="home" />
          </div>
        </template>
        <template #content>
          <ul class="stories">
            <li class="stories-item" v-for="story in stories" :key="story.id">
            <story-user-item
            :avatar="story.avatar"
            :username="story.username"
            @onPress="handlePress(story.id)"
            />
            </li>
          </ul>
        </template>
    </headerline>
  </div>
</template>

<script>
import StoryUserItem from '@/components/storyUserItem/storyUserItem.vue'
import { headerline } from '../../components/headerline'
import { icon } from '../../icons'
import stories from './data.json'
export default {
  name: 'feeds',
  components: {
    headerline,
    icon,
    StoryUserItem
  },
  data () {
    return {
      stories
    }
  }
}
</script>

<style lang="scss" scoped>
  .icon {
    color: red;
    width: 50px;
  }
</style>

<style lang="scss" scoped src='./feeds.scss'></style>
