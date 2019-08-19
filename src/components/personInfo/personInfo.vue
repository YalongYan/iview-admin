<template>
  <div class="container">
    <div class="left-ctn">
        <img class="photoImg" src="./../../assets/images/photo.jpg"/>
    </div>
    <div class="right-ctn">
        <span class="name"> {{ info.name }} </span>
        <div class="icon-group">
            <span class="icon-item"><i class="ivu-icon ivu-icon-ios-eye-outline" style="font-size: 24px;margin-bottom: -3px;"></i></span>
            <span class="icon-item"><i class="ivu-icon ivu-icon-ios-call-outline" style="font-size: 20px;"></i></span>
            <span class="icon-item"><i class="ivu-icon ivu-icon-ios-document-outline" style="font-size: 19px;"></i></span>
        </div>
        <div style="clear:both"></div>
        <div class="info-sub-list"> <i class="ivu-icon ivu-icon-ios-briefcase-outline" style="font-size: 14px; margin-top: -2px;"></i>  {{ info.position }} </div>
        <div class="info-sub-list"> <i class="ivu-icon ivu-icon-ios-school-outline" style="font-size: 16px; margin-top: -2px;"></i>  {{ info.school }} </div>
    </div>
    <div style="clear: both"></div>
  </div>
</template>

<script>
export default {
  data () {
    return {
    }
  },
  props: {
    info: {
      type: Object,
      default: () => {}
    }
  },
  computed: {
  },
  components: {
    // LoginForm
  },
  methods: {
  }
}
</script>

<style lang='less' scoped>
.container{
    margin: 5px 0;
    .left-ctn{
        float: left;
        .photoImg{
            width: 30px;
            height: 30px;
            border-radius: 50%;
            margin-top: 10px;
            margin-right: 10px;
        }
    }
    .right-ctn{
        float: left;
        text-align: left;
        .name{
            color: #2D8cF0;
            display: inline-block;
            width: 120px;
            line-height: 30px;
            overflow: hidden;
            text-overflow: ellipsis;
            white-space: nowrap;
            float: left;
        }
        .icon-group{
            float: left;
            margin-top: 5px;
        }
        .info-sub-list{
            line-height: 26px;
        }
        .icon-item{
            cursor: pointer;
            i:hover{
                color: #2D8cF0;
            }
            margin-left: 8px;
        }
    }
}
</style>
