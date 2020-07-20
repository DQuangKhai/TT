<template>
  <div class="popup">
    <div class="popup-title">
      <h4>Nhận hoàn tiền 10%</h4>
      <p>Khi mua sắm tại đây</p>
      <button class="btn btn-success">KÍCH HOẠT NGAY</button>
    </div>
  </div>
  
</template>

<script>
    export default {
        data() {
            return {};
        },
    };
</script>

<style lang="scss" scoped>
    .popup-title {
        width: 300px;
        padding: 10px;
    }
    
    h4 {
        font-size: 20px;
        text-align: center;
        color: red;
    }
    
    p {
        text-align: center;
        display: block;
    }
    
    .btn {
        width: 100%;
        text-align: center;
        border-radius: 5px;
    }
</style>