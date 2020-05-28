<template>
  <div>
    <!-- <h1>分享功能</h1> -->
    <vshare
      :vshareConfig="vshareConfig"
    >
    </vshare>
  </div>
</template>
<script>
export default {
  filters: {},
  data () {
    return {
      vshareConfig: {
          shareList: [
            // 此处放分享列表（ID）
            'more',
            'qzone',
            'tsina',
            'tqq',
            'renren',
            'weixin'
          ],
          common : {
            //此处放置通用设置
            bdText:"你是我的"
          },
          share : [{
            //此处放置分享按钮设置
            bdSize:24
            }
          ],
          slide : [
            //此处放置浮窗分享设置
            false
          ],
          image : [
            //此处放置图片分享设置
            false
          ],
          selectShare : [
            //此处放置划词分享设置
           false
          ]
        }
      
    }
  },
  created () {},
  methods: {}
}
</script>
<style>
</style>
