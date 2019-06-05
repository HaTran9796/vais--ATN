<template>
    <div>
        <div class="content-login panel-content">
            <div class="container">
                <div class="row">
                    <div class="col-lg-7 col-md-8 col-sm-12 col-12 m-auto">
                        <div class="form-general">
                            <div class="top-content top-content-login d-flex align-items-center justify-content-between mb-4">
                                <h1 class="logo"><a href="" title="" class="image img-cover"><img src="image/upload/logo.png" alt=""></a></h1>
                                <div class="slogan">
                                    <div class="text">Phần mềm gán nhãn dữ liệu</div>
                                </div>
                            </div>
                            <div class="wrap-form-login wrap-form">
                                <form action="" method="" class="form form-login" @submit.prevent="handleSubmit">
                                    <div class="row">
                                        <div class="col-12">
                                            <div class="form-group row ">
                                                <label for="name-login" class="col-12 col-form-label name-label">Tên đăng nhập </label>
                                                <div class="col-12">
                                                    <input type="text" class="form-control" id="name-login" placeholder="hatran9796@gmail.com" v-model="email">
                                                </div>
                                            </div>
                                        </div>
                                        <div class="col-12">
                                            <div class="form-group row">
                                                <label for="password-login" class="col-12 col-form-label name-label">Mật khẩu</label>
                                                <div class="col-12">
                                                    <input type="password" class="form-control" id="password-login" placeholder="Password" v-model="password">
                                                </div>
                                            </div>
                                        </div>
                                        <div class="col-12">
                                            <div class="form-group row d-flex justify-content-center wrap-btn">
                                                <div class="text-center big-btn">
                                                    <button class="btn-form btn-login ">Đăng nhập</button>
                                                </div>
                                            </div>
                                        </div>
                                    </div>
                                </form>
                            </div>
                        </div>
                    </div>
                </div>
            </div>
	    </div>
    </div>
</template>
<script>
export default {
    props: {path: String},
    data() {
        return {
            email: '',
            password: '',
        }
    },
    methods: {
        handleSubmit: function(){
            console.log("Thực hiện submit");
        }
    },
} 
</script>
<style scoped>
.form-general {
    padding: 40px 60px;
    background: #ffffff;
    border-radius: 30px;
    box-shadow: 0px 0px 10px 1px rgba(147, 149, 148, 0.18);
    -webkit-box-shadow: 0px 0px 10px 1px rgba(147, 149, 148, 0.18);
    -moz-box-shadow: 0px 0px 10px 1px rgba(147, 149, 148, 0.18);
}

.top-content .slogan .text {
    font-size: 19px;
    line-height: 28px;
    text-align: center;
    text-transform: uppercase;
    color: #21add5;
    font-weight: 600;
}

.wrap-btn .btn-form {
    color: #ffffff;
    position: relative;
    display: inline-block;
    padding: 10px 20px;
    border-radius: 20px;
    text-align: center;
    border: none;
    text-transform: uppercase;
    font-size: 14px;
    transition: .4s;
    z-index: 3;
}

.wrap-btn .btn-form::before {
    content: '';
    display: block;
    position: absolute;
    width: 0%;
    height: 100%;
    left: 0;
    top: 0;
    color: #ffffff;
    transition: .4s;
    -webkit-transition: .4s;
    -moz-transition: .4s;
    -o-transition: .4s;
    border-radius: 20px;
}

.wrap-btn .btn-login {
    background: #0054a5;
    margin-right: 10px;
    outline: none;
}

.wrap-btn .btn-logout {
    background: #f38c2a;
}

.wrap-btn .btn-form:hover {
    color: #fff;
}

.wrap-btn .btn-form:hover::before {
    background: #222328;
    transition: .4s;
    width: 100%;
    z-index: -1;
}

/**********************/

.forgot {
    color: #21add5;
}

.forgot:hover {
    text-decoration: underline;
    color: #21add5;
}

.text-small {
    font-size: 13px;
}

.pl-20 {
    padding-left: 20px;
}


/*******************/

.wrap-border {
    border: 1px solid #222222;
}

.new-request {
    background: #0054a5;
    color: #ffffff;
    font-size: 15px;
    display: inline-block;
    padding: 5px 20px;
    transition: .3s;
}

.new-request:hover {
    color: #ffffff;
    background: #222222;
    transition: .3s;
}

.wrap-border {
    min-height: 250px;
}

.big-item-new-file {
    position: relative;
}

.wrap-menu {
    position: absolute;
    right: 0;
    top: 0;
}
</style>
