<template>
  <Shape class="card-content">
    <HeadingSmall>{{title}}</HeadingSmall>
    <SubtitleSmall v-if="subtitle">{{subtitle}}</SubtitleSmall>
    <Paragraph>{{content}}</Paragraph>
    <ButtonPrimary :link="buttonLink">{{buttonLabel}}</ButtonPrimary>
  </Shape>
</template>

<script>
import ButtonPrimary from '../ButtonPrimary'
import HeadingSmall from '../HeadingSmall'
import SubtitleSmall from '../SubtitleSmall'
import Paragraph from '../Paragraph'
import Shape from '../Shape'

export default {
  name: 'CardContent',
  props: {
    title: {
      type: String,
      default: 'Heading SM'
    },
    subtitle: {
      type: String
    },
    content: {
      type: String,
      default: 'Lorem ipsum dolor sit amet, consectetur adipiscing elit. Quisque consequat ultrices pulvinar. Pellentesque ut dui nec ante aliquam placerat vehicula sed nisl. Vestibulum vitae sodales orci. Vivamus non elementum magna. In blandit et augue a dictum. Aenean laoreet nunc et nisl fermentum ultrices.'
    },
    buttonLabel: {
      type: String,
      default: 'Button label'
    },
    buttonLink: {
      type: String
    }
  },
  components: {
    ButtonPrimary,
    HeadingSmall,
    SubtitleSmall,
    Paragraph,
    Shape
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style lang="scss" scoped>
  @import "@bit/lmartim.calamity._variables";
  .card-content {
    flex-direction: column;
    align-items: flex-start;

    .heading-small {
      margin-bottom: $spacing-size-xxxs;
    }

    .subtitle-small {
      margin-bottom: $spacing-size-xxs;
    }

    .paragraph {
      margin-bottom: $spacing-size-sm;
    }
  }
</style>
