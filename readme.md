THIS IS POST FORM
(write >copy>page to a new html page)

<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">

    <link rel="stylesheet" href="css/blog.css">

    <link rel="preconnect" href="https://fonts.googleapis.com">
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
    <link
        href="https://fonts.googleapis.com/css2?family=GFS+Didot&family=Karma&family=Lora:ital,wght@0,400;0,700;1,400&family=Playfair+Display:ital,wght@0,400;0,700;1,400;1,600&family=Poppins:ital,wght@0,400;0,500;0,700;1,300&family=Raleway:ital,wght@0,600;1,700&family=Roboto:wght@400;500;700&display=swap"
        rel="stylesheet">


    <title>Quyet Blog</title>
    <!--ShareThis-->
    <script type='text/javascript'
        src='https://platform-api.sharethis.com/js/sharethis.js#property=65178eb252401a0012c02659&product=inline-share-buttons'
        async='async'></script>
</head>

<body>
    <header>
        <div class="header-wrapper">
            <nav>
                <a class="logo" href="#"><img src="Images/LOGO_small.svg" alt=""></a>

                <div class="blog-name">
                    <h4>Quyet's writing</h4>
                </div>
                <div class="sub-btn"><a href="#">Subscribe</a></div>
            </nav>
        </div>
    </header>


    <!--end of header-->

<!--START WRITING FROM HERE-->
    <div class="wrapper">
        <div class="body-section">
(title)          <h2 class="post-heading">How writing for yourself can change your life.</h2>
(subtitle)         <p class="sub-heading">The power of writing when it comes to self-discovery, embracing and being our true
                selves.</p>
            <div class="inform-frame">
                <div class="inform-content">
                    <img class="avatar" src="Images/about-me-img.png" alt="">
                    <div class="inform-content-left">
                        <h4>Tran trong quyet</h4>
(date)                      <p class="date-post">Sep 12, 2023</p>
                    </div>
                </div>
            </div>
            <!--START WRITING FROM HERE-->
            <p class="main-para">
(main para)     <b>Write for ourselves unlock the power of honesty</b>
                <br><br>
                <br><br>
                <br><br>
                <b></b>
                <br><br>
                <br><br>
                <br><br>
                <b></b>
                <br><br>
            </p>


<!--End of writing-->


        </div>
        <div class="share-btn-container">
            <!-- ShareThis BEGIN -->
            <div class="sharethis-inline-share-buttons"></div>
            <!-- ShareThis END -->
        </div>

        <a class="all-post-btn" href="blog.html">Đọc bài viết khác</a>
        <div class="subscribe-section">
            <h2 class="head">Đăng ký nhận bài viết hàng tuần </h2>
            <div class="form-frame">
                <form name="submit-to-google-sheet">
                    <input type="email" name="Email" placeholder="Địa chỉ Email" required>
                    <button type="submit">Đăng ký</button>
                </form>
                <span id="msg"></span>
            </div>
        </div>
    </div>
    <footer>
        <div class="wrapper footer">
            <div class="footer-sec">
                <a href="#">Về Trang Chính</a>
                <a class="donate-btn" href="index.html">donate</a>
            </div>
            
        </div>
    </footer>
    <p class="cpr">TranQuyet © 2023, All right reserved</p>


    
    <!--email subscribe form-----------js-->
    <script>
        const scriptURL = 'https://script.google.com/macros/s/AKfycbw7FZ81GqLFUmBpmso71uAzkcWvhMYRUnKcN0CAFTxFIlBi0TqPFk9FvV42ECfItxKz/exec'
        const form = document.forms['submit-to-google-sheet']
        const msg = document.getElementById("msg")

        form.addEventListener('submit', e => {
            e.preventDefault()
            fetch(scriptURL, { method: 'POST', body: new FormData(form) })
                .then(response => {
                    msg.innerHTML = "Đã đăng ký!"
                    setTimeout(function () {
                        msg.innerHTML = ""
                    }, 4000)
                    form.reset()
                })
                .catch(error => console.error('Error!', error.message))
        })
    </script>
</body>



</html>