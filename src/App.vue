<script setup>
import {ref} from 'vue'
import { RouterLink, RouterView } from 'vue-router'
const isSearch = ref(false)
</script>

<template>
  <div class="lk-main">
    <div class="main-container">
      <div class="sidebar">
        <div class="sidebar-wrapper">
          <img class="logo" src="./assets/images/logo.png" alt="kulager-logo">

          <div class="user-info">
            <div class="avatar">
              <img src="./assets/images/avatar.svg" alt="user-avatar">
            </div>
            <div class="user-info_text">
              <span class="name mb-0"><span class="accent-text">Елена Никитина</span></span>
              <span class="role">Ученик</span>
            </div>
          </div>

          <div class="user-info">
            <div class="user-info_text">
              <span class="info">Информация по оплате</span>
              <span class="left"><span class="accent-text">Осталось:</span> <span class="number">60 дней</span></span>
              <div class="progress-bar">
                <span></span>
              </div>
            </div>
          </div>

          <div class="sidebar-nav">
            <RouterLink to="/" tag="li" class="nav-item active">
              <svg width="24" height="24" viewBox="0 0 24 24" fill="none" xmlns="http://www.w3.org/2000/svg">
                <path opacity="0.5" d="M2 12.204C2 9.915 2 8.771 2.52 7.823C3.038 6.874 3.987 6.286 5.884 5.108L7.884 3.867C9.889 2.622 10.892 2 12 2C13.108 2 14.11 2.622 16.116 3.867L18.116 5.108C20.013 6.286 20.962 6.874 21.481 7.823C22 8.771 22 9.915 22 12.203V13.725C22 17.625 22 19.576 20.828 20.788C19.657 22 17.771 22 14 22H10C6.229 22 4.343 22 3.172 20.788C2 19.576 2 17.626 2 13.725V12.204Z" fill="#5E5E5E"/>
                <path d="M9.447 15.398C9.28721 15.2795 9.08686 15.2292 8.89004 15.2584C8.69323 15.2876 8.51605 15.3937 8.3975 15.5535C8.27895 15.7133 8.22873 15.9136 8.25789 16.1105C8.28705 16.3073 8.39321 16.4845 8.553 16.603C9.5484 17.3468 10.7574 17.7491 12 17.75C13.2426 17.7491 14.4516 17.3468 15.447 16.603C15.6069 16.4845 15.7132 16.3072 15.7425 16.1103C15.7717 15.9134 15.7216 15.7129 15.603 15.553C15.4844 15.3931 15.3072 15.2868 15.1103 15.2575C14.9134 15.2283 14.7129 15.2785 14.553 15.397C13.8164 15.9494 12.9208 16.2486 12 16.25C11.0794 16.2489 10.1838 15.95 9.447 15.398Z" fill="#5E5E5E"/>
              </svg>
              <span>Главная</span>
            </RouterLink>
            <RouterLink to="/about" class="nav-item">
              <svg width="24" height="24" viewBox="0 0 24 24" fill="none" xmlns="http://www.w3.org/2000/svg">
                <path opacity="0.5" d="M4.727 2.733C5.033 2.425 5.461 2.225 6.271 2.115C7.105 2.002 8.209 2 9.793 2H14.207C15.791 2 16.895 2.002 17.729 2.115C18.539 2.225 18.967 2.425 19.273 2.733C19.578 3.041 19.777 3.473 19.886 4.29C19.998 5.13 20 6.245 20 7.842V18H7.426C6.342 18 5.964 18.006 5.673 18.068C5.16 18.178 4.713 18.415 4.388 18.735C4.278 18.843 4.224 18.896 4.097 19.24C4.03639 19.386 4.00349 19.542 4 19.7V7.842C4 6.245 4.002 5.131 4.114 4.29C4.223 3.474 4.422 3.041 4.727 2.733Z" fill="#5E5E5E"/>
                <path d="M20 18H7.42601C6.34201 18 5.96401 18.006 5.67301 18.068C5.16001 18.178 4.71301 18.415 4.38801 18.735C4.27801 18.843 4.22401 18.896 4.09701 19.24C3.97001 19.583 3.99001 19.729 4.03101 20.02L4.05301 20.17C4.16301 20.823 4.36301 21.168 4.66901 21.414C4.97601 21.66 5.40601 21.821 6.21901 21.908C7.05601 21.998 8.16501 22 9.75501 22H14.185C15.775 22 16.885 21.999 17.721 21.908C18.534 21.821 18.964 21.66 19.271 21.414C19.471 21.254 19.625 21.052 19.738 20.75H8.00001C7.8011 20.75 7.61033 20.671 7.46968 20.5303C7.32903 20.3897 7.25001 20.1989 7.25001 20C7.25001 19.8011 7.32903 19.6103 7.46968 19.4697C7.61033 19.329 7.8011 19.25 8.00001 19.25H19.975C19.993 18.887 19.998 18.474 20 18ZM7.25001 7C7.25001 6.80109 7.32903 6.61032 7.46968 6.46967C7.61033 6.32902 7.8011 6.25 8.00001 6.25H16C16.1989 6.25 16.3897 6.32902 16.5303 6.46967C16.671 6.61032 16.75 6.80109 16.75 7C16.75 7.19891 16.671 7.38968 16.5303 7.53033C16.3897 7.67098 16.1989 7.75 16 7.75H8.00001C7.8011 7.75 7.61033 7.67098 7.46968 7.53033C7.32903 7.38968 7.25001 7.19891 7.25001 7ZM8.00001 9.75C7.8011 9.75 7.61033 9.82902 7.46968 9.96967C7.32903 10.1103 7.25001 10.3011 7.25001 10.5C7.25001 10.6989 7.32903 10.8897 7.46968 11.0303C7.61033 11.171 7.8011 11.25 8.00001 11.25H13C13.1989 11.25 13.3897 11.171 13.5303 11.0303C13.671 10.8897 13.75 10.6989 13.75 10.5C13.75 10.3011 13.671 10.1103 13.5303 9.96967C13.3897 9.82902 13.1989 9.75 13 9.75H8.00001Z" fill="#5E5E5E"/>
              </svg>
              <span>Обучение</span>
            </RouterLink>
            <RouterLink to="/" class="nav-item">
              <svg width="24" height="24" viewBox="0 0 24 24" fill="none" xmlns="http://www.w3.org/2000/svg">
                <path opacity="0.5" d="M2 12C2 7.28636 2 4.92909 3.46364 3.46364C4.93 2 7.28727 2 12 2C16.7136 2 19.0709 2 20.5364 3.46364C22 4.93 22 7.28727 22 12C22 16.7136 22 19.0709 20.5364 20.5364C19.07 22 16.7127 22 12 22C7.28636 22 4.92909 22 3.46364 20.5364C2 19.07 2 16.7127 2 12Z" fill="#5E5E5E"/>
                <path d="M13.7509 14.0928C13.9736 13.9191 14.1754 13.7173 14.58 13.3128L19.6164 8.27641C19.7382 8.15459 19.6827 7.94459 19.52 7.88823C18.7323 7.61297 18.0174 7.16257 17.4291 6.57096C16.8371 5.98271 16.3864 5.26778 16.1109 4.48005C16.0554 4.31641 15.8454 4.26187 15.7236 4.38369L10.6873 9.42005C10.2827 9.82369 10.0809 10.0264 9.90726 10.2491C9.70216 10.5117 9.52627 10.7958 9.38272 11.0964C9.26181 11.351 9.1709 11.6228 8.9909 12.1646L8.75726 12.8646L8.38544 13.9791L8.03817 15.0228C7.9948 15.1535 7.98861 15.2937 8.02031 15.4277C8.052 15.5617 8.12033 15.6842 8.21765 15.7817C8.31498 15.8791 8.43747 15.9475 8.57145 15.9793C8.70543 16.0112 8.84561 16.0051 8.97635 15.9619L10.0218 15.6137L11.1345 15.2428L11.8345 15.0091C12.3773 14.8282 12.6482 14.7382 12.9027 14.6164C13.2037 14.4733 13.4881 14.2977 13.7509 14.0928ZM21.1936 6.70005C21.71 6.18384 22.0001 5.48367 22.0002 4.75355C22.0002 4.02344 21.7103 3.3232 21.1941 2.80687C20.6779 2.29054 19.9777 2.00042 19.2476 2.00034C18.5175 2.00025 17.8172 2.29021 17.3009 2.80641L17.1382 2.96823C17.0613 3.04432 17.0042 3.13794 16.9715 3.24104C16.9389 3.34413 16.9318 3.45361 16.9509 3.56005C16.9754 3.69641 17.0209 3.89641 17.1036 4.1355C17.3266 4.77356 17.6915 5.35266 18.1709 5.82914C18.6471 6.30842 19.2259 6.67335 19.8636 6.89641C20.1027 6.97823 20.3027 7.02459 20.4391 7.04914C20.6573 7.08823 20.8754 7.01732 21.0318 6.86096L21.1936 6.70005Z" fill="#5E5E5E"/>
              </svg>
              <span>Тестирование</span>
            </RouterLink>
            <RouterLink to="/" class="nav-item">
              <svg width="24" height="24" viewBox="0 0 24 24" fill="none" xmlns="http://www.w3.org/2000/svg">
                <path opacity="0.5" d="M18.75 9V9.704C18.75 10.549 18.99 11.375 19.442 12.078L20.55 13.801C21.561 15.375 20.789 17.514 19.03 18.011C14.4338 19.313 9.56625 19.313 4.97 18.011C3.211 17.514 2.439 15.375 3.45 13.801L4.558 12.078C5.01157 11.3694 5.25211 10.5454 5.251 9.704V9C5.251 5.134 8.273 2 12 2C15.727 2 18.75 5.134 18.75 9Z" fill="#5E5E5E"/>
                <path d="M7.24301 18.545C7.56976 19.5491 8.20589 20.4241 9.06031 21.0446C9.91472 21.665 10.9436 21.9992 11.9995 21.9992C13.0555 21.9992 14.0843 21.665 14.9387 21.0446C15.7931 20.4241 16.4293 19.5491 16.756 18.545C13.611 19.135 10.389 19.135 7.24301 18.545Z" fill="#5E5E5E"/>
              </svg>
              <span to="/">Уведомления</span>
            </RouterLink>
            <RouterLink to="/" class="nav-item">
              <svg width="24" height="24" viewBox="0 0 24 24" fill="none" xmlns="http://www.w3.org/2000/svg">
                <path opacity="0.5" fill-rule="evenodd" clip-rule="evenodd" d="M14.279 2.152C13.909 2 13.439 2 12.5 2C11.561 2 11.092 2 10.721 2.152C10.2285 2.35421 9.83639 2.74377 9.63101 3.235C9.53701 3.458 9.50101 3.719 9.48601 4.098C9.47934 4.3726 9.40274 4.64097 9.26346 4.87772C9.12417 5.11447 8.9268 5.31178 8.69001 5.451C8.44875 5.5851 8.17755 5.65615 7.90154 5.65754C7.62552 5.65894 7.35361 5.59065 7.11101 5.459C6.77301 5.281 6.52801 5.183 6.28601 5.151C5.75656 5.08148 5.22108 5.2238 4.79601 5.547C4.47801 5.789 4.24301 6.193 3.77401 7C3.30401 7.807 3.07001 8.21 3.01701 8.605C2.94701 9.131 3.09101 9.663 3.41701 10.084C3.56501 10.276 3.77401 10.437 4.09701 10.639C4.57401 10.936 4.88001 11.442 4.88001 12C4.88001 12.558 4.57401 13.064 4.09801 13.36C3.77401 13.563 3.56501 13.724 3.41601 13.916C3.25509 14.1239 3.13698 14.3617 3.06849 14.6156C3.00001 14.8694 2.98251 15.1343 3.01701 15.395C3.07001 15.789 3.30401 16.193 3.77401 17C4.24401 17.807 4.47801 18.21 4.79601 18.453C5.22001 18.776 5.75601 18.918 6.28601 18.849C6.52801 18.817 6.77301 18.719 7.11101 18.541C7.35374 18.4092 7.62583 18.3408 7.90204 18.3422C8.17825 18.3436 8.44963 18.4147 8.69101 18.549C9.17701 18.829 9.46501 19.344 9.48601 19.902C9.50101 20.282 9.53701 20.542 9.63101 20.765C9.83501 21.255 10.227 21.645 10.721 21.848C11.091 22 11.561 22 12.5 22C13.439 22 13.909 22 14.279 21.848C14.7716 21.6458 15.1636 21.2562 15.369 20.765C15.463 20.542 15.499 20.282 15.514 19.902C15.534 19.344 15.823 18.828 16.31 18.549C16.5513 18.4149 16.8225 18.3439 17.0985 18.3425C17.3745 18.3411 17.6464 18.4093 17.889 18.541C18.227 18.719 18.472 18.817 18.714 18.849C19.244 18.919 19.78 18.776 20.204 18.453C20.522 18.211 20.757 17.807 21.226 17C21.696 16.193 21.93 15.79 21.983 15.395C22.0174 15.1343 21.9997 14.8693 21.9311 14.6155C21.8624 14.3616 21.7441 14.1239 21.583 13.916C21.435 13.724 21.226 13.563 20.903 13.361C20.426 13.064 20.12 12.558 20.12 12C20.12 11.442 20.426 10.936 20.902 10.64C21.226 10.437 21.435 10.276 21.584 10.084C21.7449 9.87606 21.863 9.63829 21.9315 9.38443C22 9.13057 22.0175 8.86566 21.983 8.605C21.93 8.211 21.696 7.807 21.226 7C20.756 6.193 20.522 5.79 20.204 5.547C19.7789 5.2238 19.2435 5.08148 18.714 5.151C18.472 5.183 18.227 5.281 17.889 5.459C17.6463 5.59083 17.3742 5.65922 17.098 5.65782C16.8218 5.65642 16.5504 5.58528 16.309 5.451C16.0724 5.31166 15.8752 5.11429 15.7361 4.87755C15.597 4.64081 15.5206 4.37251 15.514 4.098C15.499 3.718 15.463 3.458 15.369 3.235C15.2674 2.99174 15.1188 2.77088 14.9318 2.58506C14.7447 2.39923 14.5229 2.25208 14.279 2.152Z" fill="#5E5E5E"/>
                <path d="M15.523 12C15.523 13.657 14.169 15 12.5 15C10.83 15 9.47699 13.657 9.47699 12C9.47699 10.343 10.83 9 12.5 9C14.17 9 15.523 10.343 15.523 12Z" fill="#5E5E5E"/>
              </svg>
              <span to="/">Настройки</span>
            </RouterLink>
          </div>

          <div class="contacts-block">
            <img src="./assets/images/share.svg" alt="share">
            <span class="mt-2 mb-1">Связь с нами:</span>
            <a href="tel:+79997697553">+7 999 769-75-53</a>
            <button type="button" class="btn">Написать в WhatsApp <img src="./assets/images/whatsapp.svg" alt="whatsapp"></button>
          </div>
        </div>
      </div>
      <div class="main-wrapper">
        <header>
          <div class="wrapper">
            <div class="search" :class="{'active': isSearch}">
              <span class="search-icon" @click="isSearch = !isSearch">
                <svg width="16" height="15" viewBox="0 0 16 15" fill="none" xmlns="http://www.w3.org/2000/svg">
                  <path fill-rule="evenodd" clip-rule="evenodd" d="M12.425 10.75L15.2583 13.575C15.4161 13.7315 15.5048 13.9445 15.5048 14.1667C15.5048 14.3889 15.4161 14.6019 15.2583 14.7583C15.1019 14.9161 14.8889 15.0048 14.6667 15.0048C14.4445 15.0048 14.2315 14.9161 14.075 14.7583L11.25 11.925C10.0854 12.8392 8.64721 13.3352 7.16667 13.3333C3.48477 13.3333 0.5 10.3486 0.5 6.66667C0.5 2.98477 3.48477 0 7.16667 0C10.8486 0 13.8333 2.98477 13.8333 6.66667C13.8352 8.14721 13.3392 9.58538 12.425 10.75ZM7.16667 1.66667C4.40524 1.66667 2.16667 3.90524 2.16667 6.66667C2.16667 9.42809 4.40524 11.6667 7.16667 11.6667C9.92809 11.6667 12.1667 9.42809 12.1667 6.66667C12.1667 3.90524 9.92809 1.66667 7.16667 1.66667Z" fill="#7E7E7E"/>
                </svg>
              </span>
              <input type="text">
            </div>
            <div class="right-bar">
              <div class="notifications">
                <img src="./assets/images/notifications.svg" alt="">
                <span class="badge">8</span>
              </div>
              <div class="lang-toggle">
                <span class="ru active">Рус</span>
                <span class="kz">қаз</span>
              </div>
            </div>
          </div>
        </header>
        <RouterView />
      </div>
    </div>
    <footer>
      <div class="wrapper">
      </div>
    </footer>
  </div>
</template>

<style lang="scss" scoped>
@import "assets/main.scss";
  .lk-main{
    display:flex;
    flex-direction: column;
    width:100%;
    height:100%;
    align-items: center;
  }
  .main-container{
    display:flex;
    max-width:1440px;
    width:100%;
    height:100%;
  }
  .sidebar{
    width:280px;
    min-width:280px;
    border-right:1px dashed #E5E8EB;
    display:flex;
    flex-direction: column;
    align-items: center;

    position: relative;
    left:0;
    top:0;
    z-index: 1;
    background: #FFF;
    &:before{
      content: '';
      width:9999px;
      height:100%;
      position: absolute;
      right:280px;
      top:0;
      background: #FFF;
    }
    .sidebar-wrapper{
      width: 100%;
      position: sticky;
      z-index: 999;
      padding: 25px 20px;
      top:0;
      background: #FFF;
    }
    .logo{
      width:145px;
      margin-bottom:25px;
    }
    .user-info{
      display:flex;
      background: #F6F6F6;
      padding:20px 20px 20px;
      border-radius: 12px;
      width:100%;
      margin-bottom:10px;
      align-items: center;
      .avatar{
        margin-right:15px;
      }
      .user-info_text{
        width:100%;
        display:flex;
        flex-direction: column;
        .role, .info{
          color:$secondary-color;
          font-weight: 300;
          letter-spacing: 0.5px;
        }
        .left{
          .number{
            color:$accent-color;
          }
        }
      }
      .progress-bar{
        background: #EDEDED;
        height:4px;
        border-radius:4px;
        width:100%;
        margin-top:10px;
        span{
          background: $accent-color;
          width:40%;
          height:4px;
          border-radius:4px;
        }
      }
    }
    .sidebar-nav{
      width:100%;
      margin-top:20px;
      .nav-item{
        text-decoration: none;
        display:flex;
        align-items: center;
        width:100%;
        padding:12px 15px;
        font-family: "Golos Text", sans-serif;
        font-weight: 500;
        border-radius: 8px;
        margin-bottom:5px;
        transition: 0.3s;
        span{
          text-decoration: none;
          color: #969696;
          transition: 0.3s;
        }
        svg{
          margin-right:15px;
        }
        &:active{
          background: $accent-color-opacity;
          opacity: 0.5;
          span{
            color:$accent-color !important;
          }
        }
        &.active{
          background: $accent-color-opacity;
          span{
            color:#000;
          }
          svg{
            path{
              fill:$accent-color
            }
          }
        }
      }
    }
    .contacts-block{
      position: fixed;
      bottom:20px;
      width:230px;
      display:flex;
      flex-direction: column;
      padding:15px;
      border: 1px solid rgba(145, 158, 171, 0.2);
      border-radius: 12px;
      box-shadow: 0 12px 24px -4px rgba(145, 158, 171, 0.25);

      img{
        width:20px;
      }
      span{
        color:#637381;
      }
      a{
        font-family: "Golos Text", sans-serif;
        text-decoration: none;
        color:#000;
        font-size:15.5px;
        font-weight: 500;
        margin:0 0 15px;
      }
      .btn{
        max-width:100%;
        color:#36B37E;
        border:1px solid #36B37E;
        height:38px;
        border-radius: 8px;
        font-weight: 500;
        img{
          margin-left:10px;
        }
      }
    }
  }
  .main-wrapper{
    width:100%;
    padding:0 40px;
    header{
      width:100%;
      height:80px;
      align-items: center;
      display:flex;
      .wrapper{
        width:100%;
        display:flex;
        align-items: center;
        justify-content: space-between;
      }
      .search{
        background: rgba(145, 158, 171, 0.1);
        height:36px;
        width:36px;
        border-radius: 18px;
        display:flex;
        transition: 0.3s ease-in-out;
        align-items: center;
        overflow: hidden;
        &:focus, &:active, &.active{
          flex-grow:1;
        }
        input{
          background: none;
          border:none;
          outline:none;
        }
        .search-icon{
          min-width:36px;
          svg{
            transform: translate(10px, -1px);
          }
        }
      }
      .right-bar{
        margin-left:20px;
        display:flex;
        align-items: center;
        .notifications{
          margin-right:20px;
          position: relative;
          .badge{
            background: red;
            font-size:12px;
            font-weight: 700;
            height:20px;
            min-width:20px;
            display:flex;
            justify-content: center;
            align-items: center;
            color:#FFF;
            border-radius: 10px;
            position: absolute;
            right:-10px;
            top:-10px;
          }
        }
        .lang-toggle{
          display:flex;
          flex-direction: column;
          .ru, .kz{
            text-transform: capitalize;
            padding:3px 12px;
            border-radius: 20px;
            color:#5E5E5E;
            cursor:pointer;
            &.active{
              background:#F6F6F6;
              color:#000;
            }
          }
        }
      }
    }
  }
footer{
  background: #F4F6F8;
  height:50px;
  width:100%;
  margin-top:-50px;
}
</style>
