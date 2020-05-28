<!DOCTYPE html>
<html lang="ja">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Oyako de Cafe smile</title>
    <link rel="stylesheet" href="style.css">
    <script type="text/javascript" src="/js/script.js"></script>
    <script src="https://code.jquery.com/jquery-1.12.4.min.js" type="text/javascript"></script>
    <script type="text/javascript">
    function slideSwitch() {
        var $active = $('#slideshow img.active');

        if ( $active.length == 0 ) $active = $('#slideshow img:last');

        var $next =  $active.next().length ? $active.next()
            : $('#slideshow img:first');

        $active.addClass('last-active');

        $next.css({opacity: 0.0})
            .addClass('active')
            .animate({opacity: 1.0}, 2000, function() {
                $active.removeClass('active last-active');
            });
    }

    $(function() {
        setInterval( "slideSwitch()", 2500 );
    });
    </script>
</head>
<body>
    <header>
        <div class="container">
            <!-- <h1>OYAKO DE CAFE</h1>
            <h2>SMILE</h2> -->
            <p id="slideshow">
                <img src="./images/smile.jpg" alt="smile1" class="active">
                <img src="./images/smile2.jpg" alt="smile2">
                <img src="./images/smile3.jpg" alt="smile3">
            </p>
        </div>
        <div class="text">
            <h1>Thank you forever</h1>
            <h2>Photo Edit ©: <span>Sana</span></h2>
            <a class="end-movie" href="https://youtu.be/WAiO5IGa4as">最後に　スタッフの皆様へ.......</a>
            
        </div>

    </header>
</body>
</html>
