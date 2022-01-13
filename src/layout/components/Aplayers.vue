<template>
  <span class="aplayer-container">
    <aplayer
      :autoplay="autoPlay"
      :float="float"
      :repeat.sync="repeat"
      :shuffle.sync="shuffle"
      :list-max-height="listMaxHeight"
      :list-folded.sync="listFolded"
      :mini="mini"
      :muted.sync="muted"
      :volume.sync="volume"
      :music.sync="music"
      :list="list"
    />
  </span>
</template>

<script>
import Aplayer from 'vue-aplayer'
Aplayer.disableVersionBadge = true

export default {
  name: 'Aplayers',
  components: {
    Aplayer
  },
  data() {
    return {
      autoPlay: false,
      float: true,
      repeat: 'repeat-all',
      shuffle: false, // 播放器初始化完成后动态改变随机状态无效(官方bug)
      listMaxHeight: '160px',
      listFolded: true,
      mini: false,
      muted: false,
      volume: 0.8,
      music: {
        title: '雨中仙',
        artist: '音阙诗听/昆玉',
        src: 'http://music.163.com/song/media/outer/url?id=1318489622.mp3',
        pic: 'https://y.gtimg.cn/music/photo_new/T002R300x300M000001tlqVz0GwrXW_1.jpg?max_age=2592000'
      },
      list: [
        {
          title: '芒种',
          artist: '音阙诗听/赵方婧',
          src: 'http://music.163.com/song/media/outer/url?id=1369798757.mp3',
          pic: 'http://p1.music.126.net/KFWbxh1ZLyy9WR77Ca08tA==/109951164866828786.jpg?param=90y90'
        },
        {
          title: '雨中仙',
          artist: '音阙诗听/昆玉',
          src: 'http://music.163.com/song/media/outer/url?id=1318489622.mp3',
          pic: 'https://y.gtimg.cn/music/photo_new/T002R300x300M000001tlqVz0GwrXW_1.jpg?max_age=2592000'
        },
        {
          title: '画中仙（翻自 金莎）',
          artist: '_清风',
          src: 'http://music.163.com/song/media/outer/url?id=1467770948.mp3',
          pic: 'http://p1.music.126.net/wgZWg1IFAigdodveDV97lA==/119846767428565.jpg?param=130y130'
        },
        {
          title: '染墨相思',
          artist: '音阙诗听/赵方婧',
          src: 'http://music.163.com/song/media/outer/url?id=489953640.mp3',
          pic: 'http://p1.music.126.net/Obp4DB3rTVn0N-ySTogJhw==/109951162972381214.jpg?param=130y130'
        }
      ]
    }
  }
}
</script>

<style lang="scss" scoped>
.aplayer-container {
  position: fixed;
  z-index: 99999;
  bottom: 10px;
  right: 10px;
}
.aplayer-container .aplayer {
  width: 350px;
  z-index: 99999;
}
</style>
