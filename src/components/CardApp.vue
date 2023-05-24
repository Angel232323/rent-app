<template>
  <div class="card">
    <div class="card-content">
      <span class="tag-card">Los Angeles CA</span>
      <div class="footer-card">
        <div class="action">
            <button><i class='bx bx-heart'></i></button>
        </div>
        <div class="footer-card-left">
          <div class="title"><h3>{{title}}</h3></div>
          <div class="user">
            <div class="content-user">
              <div class="img-content">
                <img
                  :src="imgUser"
                  alt=""
                />
              </div>
              <div class="username"><h6>{{username}}</h6></div>
            </div>
            <div class="starts">
              <span><i class="bx bxs-star"></i></span>
              <span><i class="bx bxs-star"></i></span>
              <span><i class="bx bxs-star"></i></span>
              <small>{{star}} Stars</small>
            </div>
          </div>
        </div>
        <div class="footer-card-right">
          <div class="price">
            <h2>${{price}}</h2>
          </div>
          <div class="rooms">
            <div class="rooms-items">
              <i class="bx bx-bed"></i>
              {{ cantRoom }}
            </div>
            <div class="rooms-items">
              <i class="bx bx-bed"></i>
              {{cantRoom}}
            </div>
            <div class="rooms-items">
              <i class="bx bx-bed"></i>
              {{cantRoom}}
            </div>
          </div>
        </div>
      </div>
      <img
        :src="imgCard"
        alt=""
        srcset=""
      />
    </div>
  </div>
</template>

<style lang="less">
// Color Handler
@bgicons: rgba(69, 208, 215);
@bgiconsnegative: rgba(225, 207, 241);


.card {
  .card-content {
    box-shadow: 0px 5px 10px -2px rgba(74, 54, 251, 0.2);
    margin-bottom: 15px;
    

    .footer-card {
      padding: 10px;
      position: absolute;
      bottom: 0%;
      width: 100%;
      display: flex;
      background-color: #fff;
      border-radius: 15px;
      align-items: center;
      .action{
        position: absolute;
        bottom: 87%;
        right: 10%;
        button{
            box-shadow: 0px 5px 10px -2px rgba(74, 54, 251, 0.2);
            color: red;
            border: none;
            outline: none;
            border-radius: 50px;
            background-color: white;
            padding: 8px;
            
        }

      }
      .footer-card-right {
        width: 40%;
        display: flex;
        flex-direction: column;
        align-items: center;
        margin: 10px;

        .rooms {
          display: flex;
          justify-content: space-between;
          width: 80%;

    
          .rooms-items {
            color: @bgiconsnegative;
            display: flex;
            justify-content: space-between;
          }
        }
      }
      .footer-card-left {
        display: flex;
        flex-direction: column;
        width: 60%;
        .title{
            margin: 10px;
            text-align: start;
        }
        .user {
          display: flex;
          flex-direction: column;
          .starts {
            margin: 10px;
            text-align: start;
            display: flex;
            small {
              margin-left: 20px;
            }
            align-items: center;
            color: @bgiconsnegative;
            i {
              color: @bgicons;
            }
          }
          .content-user {
            display: flex;
            align-items: center;
            margin-left: 10px;
            .username {
              margin-left: 10px;
            }
          }
        }
        .img-content {
          width: 30px;
          height: 30px;
          border-radius: 50px;
          overflow: hidden;
          img {
            width: 100%;
            height: 100%;
            object-fit: cover;
          }
        }
      }
    }
    border-radius: 30px;
    overflow: hidden;
    width: 100%;
    position: relative;
    .tag-card {
      position: absolute;
      background-color: rgb(244, 242, 243);
      padding: 8px;
      z-index: 3000;
      top: 0;
      margin: 20px;
      border-radius: 15px;
      font-size: 0.9rem;
    }
    img {
      object-fit: cover;
      width: 100%;
      height: 100%;
    }
  }
}
</style>

<script>
export default {
  name: "CardApp",
  props: {
    title:{
        type: String,
        default: "Not Found"
    },
    price:{
        type: Number,
        default: 0
    },
    username:{
        type: String,
        default:"Anonym"
    },
    imgUser:{
        type: String,
        default:"https://www.nicepng.com/png/detail/202-2022264_usuario-annimo-usuario-annimo-user-icon-png-transparent.png"
    },
    imgCard:{
        type: String,
        default:"https://images.unsplash.com/photo-1443827357341-5def682bb98b?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=872&q=80"
    },
    cantRoom:{
        type: Number,
        default:0
    },
    star:{
        type: Number,
        default:0
    }
  }
};
</script>
