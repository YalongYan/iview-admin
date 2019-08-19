<style lang="less">
  @import './list.less';
</style>

<template>
  <div>
    <div class="filter-container">
      <!-- <div class="filter-left">一键搜索</div> -->
      <div class="filter-right">
        <Input class="search-item" search placeholder="请输入候选人姓名，手机号，邮箱" />
      </div>
      <div style="clear:both"></div>
    </div>
    <Table border ref="selection" :columns="columns4" :data="data1">
       <template slot-scope="{ row }" slot="name">
        <PersonInfo :info="row"/>
      </template>
    </Table>
  </div>
</template>

<script>
import PersonInfo from './../../components/personInfo/personInfo.vue'
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
          slot: 'name',
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
          name: '刘德华',
          age: 18,
          address: 'New York No. 1 Lake Park',
          date: '2016-10-03',
          photo: 'photo.jpg',
          telephone: '18501223333',
          school: '北京大学 | 硕士',
          position: '律师事务所 | 实习生'
        },
        {
          name: '詹姆斯',
          age: 24,
          address: 'London No. 1 Lake Park',
          date: '2016-10-01',
          photo: 'photo.jpg',
          telephone: '18501223333',
          school: '北京大学 | 硕士',
          position: '律师事务所 | 实习生'
        },
        {
          name: 'Joe Black',
          age: 30,
          address: 'Sydney No. 1 Lake Park',
          date: '2016-10-02',
          photo: 'photo.jpg',
          telephone: '18501223333',
          school: '北京大学 | 硕士',
          position: '律师事务所 | 实习生'
        }
      ]
    }
  },
  components: {
    PersonInfo
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

<style lang='less'>
.filter-container{
  margin-bottom: 10px;

  .filter-left{
    float: left;
  }
  .filter-right{
    float: right;
    .search-item{
    }
  }
}
</style>
