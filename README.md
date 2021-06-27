<!doctype html>
<html>
    <head>
        <meta charset="utf-8">
        <title>PHP Basit Hesap Makinesi</title>
        <link rel="stylesheet" href="https://maxcdn.bootstrapcdn.com/bootstrap/3.3.5/css/bootstrap.min.css">
        <link rel="stylesheet" href="https://maxcdn.bootstrapcdn.com/bootstrap/3.3.5/css/bootstrap-theme.min.css">
    </head>
    <body>
		<br><br><br><br>
		<h2 align="center">PHP ile Basit Hesap Makinesi</h2>
      <div class="container">
            <form action="<?=$_SERVER['PHP_SELF']?>" method="post">
              <div class="form-group">
                <label for="sayi1">Sayı 1</label>
                <input type="text" class="form-control" name="sayi1">
              </div>
              <div class="form-group">
                <label for="sayi2">Sayı 2</label>
                <input type="text" class="form-control" name="sayi2">
              </div>
              <div class="form-group">
                <label for="secim">İşlem Seçin</label>
                <select name="secim" class="form-control">
                    <option value="+">TOPLA</option>
                    <option value="-">FARK</option>
                    <option value="*">ÇARPIM</option>
                    <option value="/">BÖLÜM</option>
                </select>
              </div>
              <button type="submit" name="kontrol" class="btn btn-default" >ÇALIŞTIR</button>
            </form>
        </div>
        <!-- PHP KODLARI -->
        <div class="container">
           <table class="table table-striped">
                <?php
                if(isset($_POST["kontrol"]))//kontrol adında bir form nesnesi var mı kontrolü yapılıyor
                {
                    $sayi1=$_POST["sayi1"];
                    $sayi2=$_POST["sayi2"];
                    $secim=$_POST["secim"];
                    $sonuc=0;
                    
                    if($secim == '+')
                    {
                        $sonuc=$sayi1+$sayi2;
                    }
                    elseif($secim == '-')
                    {
                        $sonuc=$sayi1-$sayi2;    
                    }
                    elseif($secim == '*')
                    {
                        $sonuc=$sayi1*$sayi2;    
                    }
                    elseif($secim == '/')
                    {
                         $sonuc=$sayi1/$sayi2;   
                    }
                    
                    echo "<h1 class='text-info'>$sonuc</h1>";
                }     
                ?>
            </table>
       </div>
    </body>
</html>
<!doctype html>
<html>
    <head>
        <meta charset="utf-8">
        <title>PHP Basit Hesap Makinesi</title>
        <link rel="stylesheet" href="https://maxcdn.bootstrapcdn.com/bootstrap/3.3.5/css/bootstrap.min.css">
        <link rel="stylesheet" href="https://maxcdn.bootstrapcdn.com/bootstrap/3.3.5/css/bootstrap-theme.min.css">
    </head>
    <body>
		<br><br><br><br>
		<h2 align="center">PHP ile Basit Hesap Makinesi</h2>
      <div class="container">
            <form action="<?=$_SERVER['PHP_SELF']?>" method="post">
              <div class="form-group">
                <label for="sayi1">Sayı 1</label>
                <input type="text" class="form-control" name="sayi1">
              </div>
              <div class="form-group">
                <label for="sayi2">Sayı 2</label>
                <input type="text" class="form-control" name="sayi2">
              </div>
              <div class="form-group">
                <label for="secim">İşlem Seçin</label>
                <select name="secim" class="form-control">
                    <option value="+">TOPLA</option>
                    <option value="-">FARK</option>
                    <option value="*">ÇARPIM</option>
                    <option value="/">BÖLÜM</option>
                </select>
              </div>
              <button type="submit" name="kontrol" class="btn btn-default" >ÇALIŞTIR</button>
            </form>
        </div>
        <!-- PHP KODLARI -->
        <div class="container">
           <table class="table table-striped">
                <?php
                if(isset($_POST["kontrol"]))//kontrol adında bir form nesnesi var mı kontrolü yapılıyor
                {
                    $sayi1=$_POST["sayi1"];
                    $sayi2=$_POST["sayi2"];
                    $secim=$_POST["secim"];
                    $sonuc=0;
                    
                    if($secim == '+')
                    {
                        $sonuc=$sayi1+$sayi2;
                    }
                    elseif($secim == '-')
                    {
                        $sonuc=$sayi1-$sayi2;    
                    }
                    elseif($secim == '*')
                    {
                        $sonuc=$sayi1*$sayi2;    
                    }
                    elseif($secim == '/')
                    {
                         $sonuc=$sayi1/$sayi2;   
                    }
                    
                    echo "<h1 class='text-info'>$sonuc</h1>";
                }     
                ?>
            </table>
       </div>
    </body>
</html>
