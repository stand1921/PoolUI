<template>
  <div id="app" class="grid-content bg-purple">
    <el-container>
      <el-header>
        <el-row>
          <el-menu
              class=""
              mode="horizontal"
              textColor="#FFFFFF"
              backgroundColor="#409EFF"
              activeTextColor="#FFFFFF"
              align="right">
            <el-menu-item index="1" align="right"><a class="access" href="/" target="_blank">首页</a></el-menu-item>
            <el-menu-item index="2" align="right"><a class="access" href="/" target="_blank">统计</a></el-menu-item>
            <el-menu-item index="3" align="right"><a class="access" href="/" target="_blank">工具</a></el-menu-item>
            <el-menu-item index="4" align="right"><a class="access" href="/" target="_blank">客服</a></el-menu-item>
            <el-menu-item index="5" align="right"><a class="access" href="/" target="_blank">帮助</a></el-menu-item>
          </el-menu>
        </el-row>
      </el-header>
      <el-main>
        <el-row>
          <el-col :span="4"><div class="grid-content"></div></el-col>
          <el-col :span="16">
            <el-breadcrumb separator="/">
              <el-breadcrumb-item :to="{ path: '/' }">首页</el-breadcrumb-item>
              <el-breadcrumb-item>统计</el-breadcrumb-item>
            </el-breadcrumb>
          </el-col>
          <el-col :span="4"><div class="grid-content"></div></el-col>
        </el-row>
        <el-row :gutter="20">
          <el-col :span="4"><div class="grid-content"></div></el-col>
          <el-col :span="8">
            <div class="grid-content bg-purple">
              <el-card class="box-card">
                <div class="text item head-table">
                  <dl><dt><b style="color:#000">比特币/BTC</b></dt></dl>
                  <dl>
                    <dt>算力</dt>
                    <dd>
                      <span>3.440</span>
                      <span class="text-muted">EH/s</span>
                    </dd>
                  </dl>
                  <dl>
                    <dt>矿机</dt>
                    <dd>
                      <span>123123</span>
                    </dd>
                  </dl>
                  <dl>
                    <dt>挖矿所得</dt>
                    <dd>
                      <span>17231</span>
                      <span class="text-muted">BTC</span>
                    </dd>
                  </dl>
                </div>
              </el-card>
            </div>
          </el-col>
          <el-col :span="8">
            <div class="grid-content bg-purple">
              <el-card class="box-card">
                <div class="text item head-table">
                  <dl><dt><b style="color:#000">比特币现金/BCH</b></dt></dl>
                  <dl>
                    <dt>算力</dt>
                    <dd>
                      <span>3.440</span>
                      <span class="text-muted">EH/s</span>
                    </dd>
                  </dl>
                  <dl>
                    <dt>矿机</dt>
                    <dd>
                      <span>78688</span>
                    </dd>
                  </dl>
                  <dl>
                    <dt>挖矿所得</dt>
                    <dd>
                      <span>64747</span>
                      <span class="text-muted">BCH</span>
                    </dd>
                  </dl>
                </div>
              </el-card>
            </div>
          </el-col>
          <el-col :span="4"><div class="grid-content"></div></el-col>
        </el-row>

        <el-row>
          <el-col :span="4"><div class="grid-content"></div></el-col>
          <el-col :span="16">
            <el-card class="box-card">
              <div slot="header" class="clearfix">
                <span>全网算力</span>
              </div>
              <div class="grid-content bg-purple-light">
                <div id="graph1" style="width:1140px;height:450px;"></div>
              </div>
            </el-card>
          </el-col>
          <el-col :span="4"><div class="grid-content"></div></el-col>
        </el-row>

        <el-row>
          <el-col :span="4"><div class="grid-content"></div></el-col>
          <el-col :span="16">
            <el-card class="box-card">
              <div slot="header" class="clearfix">
                <span>最高单机算力</span>
              </div>
              <div class="grid-content bg-purple-light">
                <div id="graph2" style="width:1140px;height:450px;"></div>
              </div>
            </el-card>
          </el-col>
          <el-col :span="4"><div class="grid-content"></div></el-col>
        </el-row>

        <el-row>
          <el-col :span="4"><div class="grid-content"></div></el-col>
          <el-col :span="16">
            <el-card class="box-card">
              <div slot="header" class="clearfix">
                <span>广播区块</span>
              </div>
              <div class="grid-content bg-purple-light">
                <div id="graph3" style="width:600px;height:450px;"></div>
              </div>
            </el-card>
          </el-col>
          <el-col :span="4"><div class="grid-content"></div></el-col>
        </el-row>
      </el-main>
      <el-footer>联系我们</el-footer>
    </el-container>
  </div>
</template>

<style>
  .access {
    text-decoration:none;
  }
  .el-row {
    margin-bottom: 20px;
    &:last-child {
      margin-bottom: 0;
    }
  }
  .el-col {
    border-radius: 4px;
  }

  .bg-purple {
    background: #eef1f6;
  }

  .grid-content {
    border-radius: 4px;
    min-height: 36px;
  }
  .row-bg {
    padding: 10px 0;
    background-color: #f9fafc;
  }




  .text {
    font-size: 14px;
  }

  .item {
    margin-bottom: 18px;
  }

  .clearfix:before,
  .clearfix:after {
    display: table;
    content: "";
  }
  .clearfix:after {
    clear: both
  }

  .head-table>dl {
    margin-bottom: 0;
    overflow: hidden;
    width: 100%;
  }

  .head-table>dl>dd {
    line-height: 30px;
    float: right;
    margin-left: 8px;
  }

  .head-table>dl>dt {
    line-height: 30px;
    float: left;
    color: #888;
    font-weight: 300;
  }

  /*.box-card {*/
    /*width: 480px;*/
  /*}*/

   /*.el-header, .el-footer {*/
    /*background-color: #B3C0D1;*/
    /*color: #333;*/
    /*text-align: center;*/
    /*line-height: 60px;*/
  /*}*/

  /*.el-aside {*/
    /*background-color: #D3DCE6;*/
    /*color: #333;*/
    /*text-align: center;*/
    /*line-height: 200px;*/
  /*}*/

  /*.el-main {*/
    /*background-color: #E9EEF3;*/
    /*color: #333;*/
    /*text-align: center;*/
    /*line-height: 160px;*/
  /*}*/

  /*body > .el-container {*/
    /*margin-bottom: 40px;*/
  /*}*/

  /*.el-container:nth-child(5) .el-aside,*/
  /*.el-container:nth-child(6) .el-aside {*/
    /*line-height: 260px;*/
  /*}*/

  /*.el-container:nth-child(7) .el-aside {*/
    /*line-height: 320px;*/
  /*}*/
</style>

<script>
  import echarts from 'echarts'
//  import menu_img from '../img/menu.png'
//  import demo1_img from '../img/demo1.png'
//  import demo2_img from '../img/demo2.png'
//  import demo3_img from '../img/demo3.png'
//  import demo4_img from '../img/demo4.png'
//  import XLSX from 'xlsx'

  export default {
    data() {
      return {
        paintVisible: false,
//        menu_img: menu_img,
//        demo_img: [demo1_img, demo2_img, demo3_img, demo4_img],
        fileList: [],
        dataSet: [],
        columns: [],
        dimColumn: null,
        valueColumn: null,

                  table1: [{
            date: '2016-05-02',
            name: '王小虎',
            address: '上海市普陀区金沙江路 1518 弄'
          }, {
            date: '2016-05-04',
            name: '王小虎',
            address: '上海市普陀区金沙江路 1517 弄'
          }, {
            date: '2016-05-01',
            name: '王小虎',
            address: '上海市普陀区金沙江路 1519 弄'
          }, {
            date: '2016-05-03',
            name: '王小虎',
            address: '上海市普陀区金沙江路 1516 弄'
          }],

                  table2: [{
            date: '2016-05-02',
            name: '王小虎',
            address: '上海市普陀区金沙江路 1518 弄'
          }, {
            date: '2016-05-04',
            name: '王小虎',
            address: '上海市普陀区金沙江路 1517 弄'
          }, {
            date: '2016-05-01',
            name: '王小虎',
            address: '上海市普陀区金沙江路 1519 弄'
          }, {
            date: '2016-05-03',
            name: '王小虎',
            address: '上海市普陀区金沙江路 1516 弄'
          }]
      }
    },
    mounted: () => {
      let myChart1 = echarts.init(document.getElementById('graph1'))
      var base1 = +new Date(1968, 9, 3);
      var oneDay1 = 24 * 3600 * 1000;
      var date1 = [];
      var data1 = [Math.random() * 300];

      for (var i = 1; i < 200; i++) {
          var now1 = new Date(base1 += oneDay1);
          date1.push([now1.getFullYear(), now1.getMonth() + 1, now1.getDate()].join('/'));
          data1.push(Math.round((Math.random() - 0.5) * 20 + data1[i - 1]));
      }

      var option1 = {
          tooltip: {
              trigger: 'axis',
              position: function (pt) {
                  return [pt[0], '10%'];
              }
          },
          title: {
              left: 'center',
              text: '全网算力',
          },
          toolbox: {
              feature: {
                  dataZoom: {
                      yAxisIndex: 'none'
                  },
                  restore: {},
                  saveAsImage: {}
              }
          },
          xAxis: {
              type: 'category',
              boundaryGap: false,
              data: date1
          },
          yAxis: {
              type: 'value',
              boundaryGap: [0, '100%']
          },
          dataZoom: [{
              type: 'inside',
              start: 0,
              end: 10
          }, {
              start: 0,
              end: 10,
              handleIcon: 'M10.7,11.9v-1.3H9.3v1.3c-4.9,0.3-8.8,4.4-8.8,9.4c0,5,3.9,9.1,8.8,9.4v1.3h1.3v-1.3c4.9-0.3,8.8-4.4,8.8-9.4C19.5,16.3,15.6,12.2,10.7,11.9z M13.3,24.4H6.7V23h6.6V24.4z M13.3,19.6H6.7v-1.4h6.6V19.6z',
              handleSize: '80%',
              handleStyle: {
                  color: '#fff',
                  shadowBlur: 3,
                  shadowColor: 'rgba(0, 0, 0, 0.6)',
                  shadowOffsetX: 2,
                  shadowOffsetY: 2
              }
          }],
          series: [
              {
                  name:'模拟数据',
                  type:'line',
                  smooth:true,
                  symbol: 'none',
                  sampling: 'average',
                  itemStyle: {
                      normal: {
                          color: 'rgb(255, 70, 131)'
                      }
                  },
                  areaStyle: {
                      normal: {
                          color: new echarts.graphic.LinearGradient(0, 0, 0, 1, [{
                              offset: 0,
                              color: 'rgb(255, 158, 68)'
                          }, {
                              offset: 1,
                              color: 'rgb(255, 70, 131)'
                          }])
                      }
                  },
                  data: data1
              }
          ]
      };

      myChart1.setOption(option1)

      let myChart2 = echarts.init(document.getElementById('graph2'))
      var base2 = +new Date(1968, 9, 3);
      var oneDay2 = 24 * 3600 * 1000;
      var date2 = [];
      var data2 = [Math.random() * 300];

      for (var i = 1; i < 200; i++) {
          var now2 = new Date(base2 += oneDay2);
          date2.push([now2.getFullYear(), now2.getMonth() + 1, now2.getDate()].join('/'));
          data2.push(Math.round((Math.random() - 0.5) * 20 + data2[i - 1]));
      }

      var option2 = {
          tooltip: {
              trigger: 'axis',
              position: function (pt) {
                  return [pt[0], '10%'];
              }
          },
          title: {
              left: 'center',
              text: '单机最高算力',
          },
          toolbox: {
              feature: {
                  dataZoom: {
                      yAxisIndex: 'none'
                  },
                  restore: {},
                  saveAsImage: {}
              }
          },
          xAxis: {
              type: 'category',
              boundaryGap: false,
              data: date2
          },
          yAxis: {
              type: 'value',
              boundaryGap: [0, '100%']
          },
          dataZoom: [{
              type: 'inside',
              start: 0,
              end: 10
          }, {
              start: 0,
              end: 10,
              handleIcon: 'M10.7,11.9v-1.3H9.3v1.3c-4.9,0.3-8.8,4.4-8.8,9.4c0,5,3.9,9.1,8.8,9.4v1.3h1.3v-1.3c4.9-0.3,8.8-4.4,8.8-9.4C19.5,16.3,15.6,12.2,10.7,11.9z M13.3,24.4H6.7V23h6.6V24.4z M13.3,19.6H6.7v-1.4h6.6V19.6z',
              handleSize: '80%',
              handleStyle: {
                  color: '#fff',
                  shadowBlur: 3,
                  shadowColor: 'rgba(0, 0, 0, 0.6)',
                  shadowOffsetX: 2,
                  shadowOffsetY: 2
              }
          }],
          series: [
              {
                  name:'模拟数据',
                  type:'line',
                  smooth:true,
                  symbol: 'none',
                  sampling: 'average',
                  itemStyle: {
                      normal: {
                          color: 'rgb(255, 70, 131)'
                      }
                  },
                  areaStyle: {
                      normal: {
                          color: new echarts.graphic.LinearGradient(0, 0, 0, 1, [{
                              offset: 0,
                              color: 'rgb(255, 158, 68)'
                          }, {
                              offset: 1,
                              color: 'rgb(255, 70, 131)'
                          }])
                      }
                  },
                  data: data2
              }
          ]
      };

      myChart2.setOption(option2)


    },
    methods: {
    }
  }
</script>
