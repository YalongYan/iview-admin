<style lang="less">
  @import './list.less';
</style>

<template>
  <div>
    <div class="filter-container">
      <div class="filter-left">
        <Dropdown trigger="click" style="margin-top: 5px;">
          <a href="javascript:void(0)" style="color: black; font-size: 16px;font-weight：bold">
              一键筛选
              <Icon type="ios-arrow-down" style="margin-top: -2px;"></Icon>
          </a>
          <DropdownMenu slot="list">
              <DropdownItem>驴打滚</DropdownItem>
              <DropdownItem>炸酱面</DropdownItem>
              <DropdownItem>豆汁儿</DropdownItem>
              <DropdownItem>冰糖葫芦</DropdownItem>
              <DropdownItem>北京烤鸭</DropdownItem>
          </DropdownMenu>
        </Dropdown>
      </div>
      <div class="filter-right">
        <Input class="search-item" search placeholder="请输入候选人姓名，手机号，邮箱" />
        <div class="filter-icon-group">
          <span class="filter-icon-group-item"><i class="ivu-icon ivu-icon-ios-download-outline" style="font-size: 20px;margin-top: -5px;"></i></span>
          <span class="filter-icon-group-item"><i class="ivu-icon ivu-icon-ios-refresh" style="margin-top: -2px;"></i></span>
          <span class="filter-icon-group-item"><i class="ivu-icon ivu-icon-ios-funnel-outline" style="font-size: 16px;margin-top: -2px;"></i></span>
          <span class="filter-icon-group-item"><i class="ivu-icon ivu-icon-ios-settings-outline" style="font-size: 17px; margin-top: -3px;"></i></span>
        </div>
        <div style="clear: both"></div>
      </div>
      <div style="clear:both"></div>
    </div>
    <Table border ref="selection" :columns="columns4" :data="data1"></Table>
  </div>
</template>

<script>
export default {
  data () {
    return {
      columns4: [
        {
          type: 'selection',
          width: 60,
          align: 'center'
        },
        {
          title: 'Name',
          key: 'name',
          sortable: true
        },
        {
          title: 'Age',
          key: 'age',
          sortable: true
        },
        {
          title: 'Address',
          key: 'address'
        }
      ],
      data1: [
        {
          name: 'John Brown',
          age: 18,
          address: 'New York No. 1 Lake Park',
          date: '2016-10-03'
        },
        {
          name: 'Jim Green',
          age: 24,
          address: 'London No. 1 Lake Park',
          date: '2016-10-01'
        },
        {
          name: 'Joe Black',
          age: 30,
          address: 'Sydney No. 1 Lake Park',
          date: '2016-10-02'
        },
        {
          name: 'Jon Snow',
          age: 26,
          address: 'Ottawa No. 2 Lake Park',
          date: '2016-10-04'
        }
      ]
    }
  },
  components: {
    // LoginForm
  },
  methods: {
    // ...mapActions([
    //   'handleLogin',
    //   'getUserInfo'
    // ]),
    // handleSubmit ({ userName, password }) {
    //   this.handleLogin({ userName, password }).then(res => {
    //     this.getUserInfo().then(res => {
    //       this.$router.push({
    //         name: this.$config.homeName
    //       })
    //     })
    //   })
    // }
  }
}
</script>

<style lang='less' scoped>
.filter-container{
  margin-bottom: 10px;

  .filter-left{
    float: left;
  }
  .filter-right{
    float: right;
    width: 420px;

    .search-item{
      float: left;
      width: 250px;
    }
    .filter-icon-group{
      float: left;

      .filter-icon-group-item{
        cursor: pointer;
        display: inline-block;
        border: 1px solid #DCDEE2;
        margin-left: 10px;
        border-radius: 4px;
        font-size: 22px;
        width: 30px;
        height: 30px;
        text-align: center;
        line-height: 30px;
      }
    }
  }
}
</style>
