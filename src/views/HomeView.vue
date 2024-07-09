<script setup>

import CircularProgress from "@/components/CircularProgress.vue";
import LineChart from "@/components/LineChart.vue";

</script>

<template>
  <main class="kulager-main">
    <span class="title">Добро пожаловать, Елена!</span>
    <div class="short-stat">
      <div class="block">
        <div class="info-left">
          <span class="name">Пройдено вопросов <img src="../assets/images/info.svg" alt=""></span>
          <span class="stat"><span style="color:#ffa500">114</span> / 237</span>
        </div>
        <div class="info-right">
          <circular-progress :percentage="67" :size="100" :lineWidth="4"/>
        </div>
      </div>
      <div class="block">
        <div class="info-left">
          <span class="name">Решено билетов по темам <img src="../assets/images/info.svg" alt=""></span>
          <span class="stat"><span style="color:#006C9C">12</span> / 45</span>
        </div>
        <div class="info-right">
          <circular-progress :percentage="38" :lineColor="`#006C9C`" :size="100" :lineWidth="4"/>
        </div>
      </div>
      <div class="block">
        <div class="info-left">
          <span class="name">Изучено тем <img src="../assets/images/info.svg" alt=""></span>
          <span class="stat"><span style="color:#36B37E">28</span> / 95</span>
        </div>
        <div class="info-right">
          <circular-progress :percentage="86" :lineColor="`#36B37E`" :size="100" :lineWidth="4"/>
        </div>
      </div>
    </div>
    <div class="test-stat">
      <span class="sub-title">Статистика тестирования <img src="../assets/images/info.svg" alt=""></span>
      <div class="head">
        <span class="type">Тип</span>
        <span class="date">Дата</span>
        <span class="status">Статус</span>
        <span class="res">Результат</span>
      </div>
      <div class="stat-table">
       <div class="table-row">
         <div class="type">
           <div class="type-icon">
             <img src="../assets/images/type-icon-1.svg" alt="">
           </div>
           <div class="type-info">
             <span class="val-info">Тестирование по теме</span>
             <span>Сигналы регулировщика</span>
           </div>
         </div>
         <div class="date">
           <span class="date">24.02.2024</span>
           <span class="time">14:20</span>
         </div>
         <div class="status">
           <span class="status-value success">Сдано</span>
         </div>
         <div class="res">
           <div class="res-block">
             <span class="badge success"></span>
             <span>Верно:</span>
             <span class="value">30</span>
           </div>
           <div class="res-block">
             <span class="badge warning"></span>
             <span>Неверно:</span>
             <span class="value">6</span>
           </div>
           <div class="res-block">
             <span class="badge neutral"></span>
             <span>Всего:</span>
             <span class="value">40</span>
           </div>
         </div>
       </div>
        <div class="table-row">
          <div class="type">
            <div class="type-icon">
              <img src="../assets/images/type-icon-2.svg" alt="">
            </div>
            <div class="type-info">
              <span>Экзамен</span>
            </div>
          </div>
          <div class="date">
            <span class="date">24.02.2024</span>
            <span class="time">14:20</span>
          </div>
          <div class="status">
            <span class="status-value danger">Не сдан</span>
          </div>
          <div class="res">
            <div class="res-block">
              <span class="badge success"></span>
              <span>Верно:</span>
              <span class="value">30</span>
            </div>
            <div class="res-block">
              <span class="badge warning"></span>
              <span>Неверно:</span>
              <span class="value">6</span>
            </div>
            <div class="res-block">
              <span class="badge neutral"></span>
              <span>Всего:</span>
              <span class="value">40</span>
            </div>
          </div>
        </div>
        <div class="table-row">
          <div class="type">
            <div class="type-icon">
              <img src="../assets/images/type-icon-1.svg" alt="">
            </div>
            <div class="type-info">
              <span class="val-info">Тестирование по теме</span>
              <span>Дорожные знаки</span>
            </div>
          </div>
          <div class="date">
            <span class="date">24.02.2024</span>
            <span class="time">14:20</span>
          </div>
          <div class="status">
            <span class="status-value success">Сдано</span>
          </div>
          <div class="res">
            <div class="res-block">
              <span class="badge success"></span>
              <span>Верно:</span>
              <span class="value">30</span>
            </div>
            <div class="res-block">
              <span class="badge warning"></span>
              <span>Неверно:</span>
              <span class="value">6</span>
            </div>
            <div class="res-block">
              <span class="badge neutral"></span>
              <span>Всего:</span>
              <span class="value">40</span>
            </div>
          </div>
        </div>
        <div class="table-row">
          <div class="type">
            <div class="type-icon">
              <img src="../assets/images/type-icon-1.svg" alt="">
            </div>
            <div class="type-info">
              <span class="val-info">Тестирование по теме</span>
              <span>Скорость движения</span>
            </div>
          </div>
          <div class="date">
            <span class="date">24.02.2024</span>
            <span class="time">14:20</span>
          </div>
          <div class="status">
            <span class="status-value success">Сдано</span>
          </div>
          <div class="res">
            <div class="res-block">
              <span class="badge success"></span>
              <span>Верно:</span>
              <span class="value">30</span>
            </div>
            <div class="res-block">
              <span class="badge warning"></span>
              <span>Неверно:</span>
              <span class="value">6</span>
            </div>
            <div class="res-block">
              <span class="badge neutral"></span>
              <span>Всего:</span>
              <span class="value">40</span>
            </div>
          </div>
        </div>
        <div class="table-row">
          <div class="type">
            <div class="type-icon">
              <img src="../assets/images/type-icon-1.svg" alt="">
            </div>
            <div class="type-info">
              <span class="val-info">Тестирование по теме</span>
              <span>Сигналы регулировщика</span>
            </div>
          </div>
          <div class="date">
            <span class="date">24.02.2024</span>
            <span class="time">14:20</span>
          </div>
          <div class="status">
            <span class="status-value success">Сдано</span>
          </div>
          <div class="res">
            <div class="res-block">
              <span class="badge success"></span>
              <span>Верно:</span>
              <span class="value">30</span>
            </div>
            <div class="res-block">
              <span class="badge warning"></span>
              <span>Неверно:</span>
              <span class="value">6</span>
            </div>
            <div class="res-block">
              <span class="badge neutral"></span>
              <span>Всего:</span>
              <span class="value">40</span>
            </div>
          </div>
        </div>
        <div class="table-row">
          <div class="type">
            <div class="type-icon">
              <img src="../assets/images/type-icon-2.svg" alt="">
            </div>
            <div class="type-info">
              <span>Экзамен</span>
            </div>
          </div>
          <div class="date">
            <span class="date">24.02.2024</span>
            <span class="time">14:20</span>
          </div>
          <div class="status">
            <span class="status-value danger">Не сдан</span>
          </div>
          <div class="res">
            <div class="res-block">
              <span class="badge success"></span>
              <span>Верно:</span>
              <span class="value">30</span>
            </div>
            <div class="res-block">
              <span class="badge warning"></span>
              <span>Неверно:</span>
              <span class="value">6</span>
            </div>
            <div class="res-block">
              <span class="badge neutral"></span>
              <span>Всего:</span>
              <span class="value">40</span>
            </div>
          </div>
        </div>
        <div class="table-row">
          <div class="type">
            <div class="type-icon">
              <img src="../assets/images/type-icon-1.svg" alt="">
            </div>
            <div class="type-info">
              <span class="val-info">Тестирование по теме</span>
              <span>Сигналы регулировщика</span>
            </div>
          </div>
          <div class="date">
            <span class="date">24.02.2024</span>
            <span class="time">14:20</span>
          </div>
          <div class="status">
            <span class="status-value success">Сдано</span>
          </div>
          <div class="res">
            <div class="res-block">
              <span class="badge success"></span>
              <span>Верно:</span>
              <span class="value">30</span>
            </div>
            <div class="res-block">
              <span class="badge warning"></span>
              <span>Неверно:</span>
              <span class="value">6</span>
            </div>
            <div class="res-block">
              <span class="badge neutral"></span>
              <span>Всего:</span>
              <span class="value">40</span>
            </div>
          </div>
        </div>
      </div>
      <div class="bottom-pagination">
        <div class="pagination">
          <span class="pagination-item prev"><img src="../assets/images/chevron-left.svg"></span>
          <span class="pagination-item">3</span>
          <span class="pagination-item">4</span>
          <span class="pagination-item active">5</span>
          <span class="pagination-item">6</span>
          <span class="pagination-item">7</span>
          <span class="pagination-item next"><img src="../assets/images/chevron-right.svg"></span>
          <span class="total">
            <span>5</span> из <span class="total-count">15</span>
          </span>
        </div>
      </div>
    </div>
    <div class="test-stat">
      <span class="sub-title">Статистика изучения тем  <img src="../assets/images/info.svg" alt=""></span>
      <div class="head">
        <span class="type">Тема</span>
        <span class="date">Дата прочтения</span>
        <span class="spend">Затрачено на чтение</span>
      </div>
      <div class="stat-table">
        <div class="table-row">
          <div class="type">
            <div class="type-icon no-bg">
              <img src="../assets/images/type-icon-3.svg" alt="">
            </div>
            <div class="type-info">
              <span class="val-info">Глава 1.</span>
              <span>Общие положения</span>
            </div>
          </div>
          <div class="date">
            <span class="date">24.02.2024</span>
          </div>
          <div class="spend">
            <span class="status-value success">15 мин</span>
          </div>
        </div>
        <div class="table-row">
          <div class="type">
            <div class="type-icon no-bg">
              <img src="../assets/images/type-icon-3.svg" alt="">
            </div>
            <div class="type-info">
              <span class="val-info">Глава 2.</span>
              <span>Общие обязанности водителей</span>
            </div>
          </div>
          <div class="date">
            <span class="date">24.02.2024</span>
          </div>
          <div class="spend">
            <span class="status-value success">15 мин</span>
          </div>
        </div>
        <div class="table-row">
          <div class="type">
            <div class="type-icon no-bg">
              <img src="../assets/images/type-icon-3.svg" alt="">
            </div>
            <div class="type-info">
              <span class="val-info">Глава 3.</span>
              <span>Обязанности пешеходов</span>
            </div>
          </div>
          <div class="date">
            <span class="date">24.02.2024</span>
          </div>
          <div class="spend">
            <span class="status-value success">15 мин</span>
          </div>
        </div>
        <div class="table-row">
          <div class="type">
            <div class="type-icon no-bg">
              <img src="../assets/images/type-icon-3.svg" alt="">
            </div>
            <div class="type-info">
              <span class="val-info">Глава 4.</span>
              <span>Сигналы светофора и регулировщика</span>
            </div>
          </div>
          <div class="date">
            <span class="date">24.02.2024</span>
          </div>
          <div class="spend">
            <span class="status-value success">15 мин</span>
          </div>
        </div>
        <div class="table-row">
          <div class="type">
            <div class="type-icon no-bg">
              <img src="../assets/images/type-icon-3.svg" alt="">
            </div>
            <div class="type-info">
              <span class="val-info">Глава 5.</span>
              <span>Общие положения</span>
            </div>
          </div>
          <div class="date">
            <span class="date">24.02.2024</span>
          </div>
          <div class="spend">
            <span class="status-value success">15 мин</span>
          </div>
        </div>
      </div>
      <div class="bottom-pagination">
        <div class="pagination">
          <span class="pagination-item prev"><img src="../assets/images/chevron-left.svg"></span>
          <span class="pagination-item">3</span>
          <span class="pagination-item">4</span>
          <span class="pagination-item active">5</span>
          <span class="pagination-item">6</span>
          <span class="pagination-item">7</span>
          <span class="pagination-item next"><img src="../assets/images/chevron-right.svg"></span>
          <span class="total">
            <span>5</span> из <span class="total-count">15</span>
          </span>
        </div>
      </div>
    </div>
    <div class="stat-chart">
      <div class="test-stat chart">
        <span class="sub-title">Статистика за последние 7 дней <img src="../assets/images/info.svg" alt=""></span>
          <LineChart />
      </div>
      <div class="test-stat narrow">
        <span class="sub-title">Сложные для вас темы <img src="../assets/images/info.svg" alt=""></span>
        <span class="description">Самый низкий процент верных ответов</span>
        <div class="stat-table">
          <div class="table-row">
            <div class="type">
              <div class="type-icon no-bg">
                <img src="../assets/images/type-icon-3.svg" alt="">
              </div>
              <div class="type-info">
                <span>Знаки дорожного движения</span>
                <span class="val-info">30 из 100%</span>
              </div>
            </div>
          </div>
          <div class="table-row">
            <div class="type">
              <div class="type-icon no-bg">
                <img src="../assets/images/type-icon-3.svg" alt="">
              </div>
              <div class="type-info">
                <span>Знаки дорожного движения</span>
                <span class="val-info">30 из 100%</span>
              </div>
            </div>
          </div>
          <div class="table-row">
            <div class="type">
              <div class="type-icon no-bg">
                <img src="../assets/images/type-icon-3.svg" alt="">
              </div>
              <div class="type-info">
                <span>Знаки дорожного движения</span>
                <span class="val-info">30 из 100%</span>
              </div>
            </div>
          </div>
          <div class="table-row">
            <div class="type">
              <div class="type-icon no-bg">
                <img src="../assets/images/type-icon-3.svg" alt="">
              </div>
              <div class="type-info">
                <span>Знаки дорожного движения</span>
                <span class="val-info">30 из 100%</span>
              </div>
            </div>
          </div>
          <div class="table-row">
            <div class="type">
              <div class="type-icon no-bg">
                <img src="../assets/images/type-icon-3.svg" alt="">
              </div>
              <div class="type-info">
                <span>Знаки дорожного движения</span>
                <span class="val-info">30 из 100%</span>
              </div>
            </div>
          </div>

        </div>
      </div>
    </div>
  </main>
</template>

<style scoped lang="scss">
  .kulager-main{
    .title{
      display:block;
      font-size: 24px;
      font-weight: 700;
      margin:20px 0 40px;
    }
    .short-stat{
      display:flex;
      justify-content: space-between;
      .block{
        padding:20px 20px 20px 23px;
        display:flex;
        justify-content: space-between;
        width:32%;
        border: 1px solid rgba(145, 158, 171, 0.2);
        border-radius: 16px;
        box-shadow: 0 12px 24px -4px rgba(145, 158, 171, 0.25);
        .info-left{
          display:flex;
          flex-direction: column;
          justify-content: space-between;
          .name{
            font-weight: 600;
            white-space: nowrap;
            img{
              margin-left:5px;
            }
          }
          .stat{
            font-size:24px;
            color:#BDC6CF;
            span{
              font-size:32px;
            }
          }
        }
        .info-right{
          min-width:100px;
        }
      }
    }
    .test-stat{
      margin-top:25px;
      min-height:300px;
      border: 1px solid rgba(145, 158, 171, 0.2);
      border-radius: 16px;
      box-shadow: 0 12px 24px -4px rgba(145, 158, 171, 0.25);
      .sub-title{
        font-size:18px;
        font-weight: 700;
        padding:25px;
        display:flex;
        align-items: center;
        img{
          margin-left:7px;
        }
      }
      .head{
        display:flex;
        color: #7E7E7E;
        background: #F4F6F8;
        padding:16px;
        font-family: "Golos Text", sans-serif;
        font-weight: 600;
        font-size:13px;
      }
      .stat-table{
        font-family: "Golos Text", sans-serif;
        padding:8px 16px 16px;
      }
      .table-row{
        display:flex;
        align-items: center;
        width:100%;
        min-height:60px;
      }
      .type{
        box-sizing: border-box;
        min-width:200px;
        flex-grow: 1;
        display:flex;
        align-items: center;
        .type-icon{
          width:27px;
          height:27px;
          display:flex;
          align-items: center;
          justify-content: center;
          border-radius: 50%;
          background: #FDF2E2;
          margin-right:15px;
          margin-left:0;
          &.no-bg{
            background: none;
          }
        }
        .type-info{
          display:flex;
          flex-direction: column;
          font-weight: 500;
          .val-info{
            color:#7E7E7E;
          }
        }
      }
      .spend{
        min-width:180px;
      }
      .date{
        min-width:180px;
        .date{
          font-weight: 500;
          margin-right:5px;
        }
        .time{
          color:#7E7E7E;
          padding:0;
        }
      }
      .status{
        min-width:100px;
        .status-value{
          font-weight: 700;
          font-size: 12px;
          line-height: 20px;

          border-radius: 6px;
          padding:5px 8px;
          &.success{
            color:#00AB55;
            background: rgba(0, 171, 85, 0.2);
          }
          &.danger{
            color:#B71D18;
            background: #FFE4DE;
          }
        }
      }
      .res{
        min-width:330px;
        display:flex;
        .res-block{
          display:flex;
          align-items: center;
          margin-right:20px;
          padding:0;
          .value{
            font-weight: 500;
            margin-left:5px;
          }
        }
        .badge{
          min-width:12px;
          min-height:12px;
          width:12px;
          height:12px;
          border-radius: 50%;
          display:block;
          margin-right:6px;
          &.success{
            background: #00AB55;
          }
          &.warning{
            background: #F2A93F;
          }
          &.neutral{
            background: #DFDFDF;
          }

        }
      }
      .bottom-pagination{
        border-top:1px solid rgba(145, 158, 171, 0.2);
        display:flex;
        width:100%;
        justify-content: flex-end;
        align-items: center;
        padding:15px 20px;
        .pagination{
          align-items: center;
        }
        .pagination-item{
          min-width:32px;
          height:32px;
          border-radius: 8px;
          border:1px solid rgba(145, 158, 171, 0.2);
          display:flex;
          align-items: center;
          justify-content: center;
          padding:5px;
          margin:0 3px;
          cursor: pointer;
          &.active{
            background: #F2A93FFF;
            color:#fff;
            border:1px solid #F2A93FFF;
            cursor: default;
            &:hover{
              background: #F2A93FFF;
              color:#fff;
              border:1px solid #F2A93FFF;
            }
          }
          &:hover{
            color: #F2A93FFF;
            border:1px solid #F2A93FFF;
            background: #fff;
          }
          &.prev, &.next{
            border:none;
            &:hover{
              img{
                opacity: 0.5;
              }
            }
          }
        }
        .total{
          margin:0 10px 0 15px;
        }
        .total-count{
          font-weight: 500;
        }
      }
    }
    .stat-chart{
      width:100%;
      display:flex;
      margin-bottom:150px;
      .test-stat{
        &.chart{
          flex-grow: 1;
          padding-right:20px;
          padding-bottom: 20px;
        }
      }
      .narrow{
        min-width:345px;
        margin-left:20px;
        padding:25px;
        .sub-title{
          padding:0;
        }
        .description{
          opacity: 0.5;
        }
        .stat-table{
          margin-top:30px;
          padding: 0;
          .table-row{
            margin-bottom: 15px;
          }
        }
      }
    }
  }
</style>
