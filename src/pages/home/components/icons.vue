<template>
	<div class="icons">
		<router-link tag="div" class="icon" v-for="item of list" :key="item.id" :to="'/detail/components/' + item.id">
			<div class="icon-img">
				<img class='icon-img-content' :src='item.imgUrl'/>
			</div>
			<p class="icon-content">{{item.content}}</p>
		</router-link>
	</div>
</template>

<script>
export default {
  name: 'HomeIcons',
  props: {
    list: Array
  }
}
</script>

<style lang="stylus" scoped>
  @import '~styles/varibles.styl'
  @import '~styles/mixins.styl'
  .icons
    overflow: hidden
    height: 0
    padding-bottom: 25%
    margin-top: .6rem
    .icon
      position: relative
      float: left
      width: 25%
      height: 0
      padding-bottom: 25%
      overflow: hidden
      .icon-img
        position: absolute
        top: 0
        left: 0
        right: 0
        bottom: .44rem
        box-sizing: border
        padding: .1rem
        .icon-img-content
          display: block
          height: 100%
          width: 76.53%
          margin: 0 auto
      .icon-content
        position: absolute
        left: 0
        right: 0
        bottom: 0
        height: .44rem
        line-height: .44rem
        text-align: center
        color: $darkTextColor
        ellipsis()
</style>
