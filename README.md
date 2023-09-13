<html>
    <head>
        <meta charset="UTF-8">
        <title>Calculate</title>
    </head>
    <body>
        <div style="width: 350px">
            <form>
                ป้อนตัวเลขน้อยกว่า 100 <input type="text" name="number1"><br><br>
                <button type="submit" name="submit" value="submit">OK</button><br><br><hr>
            </form>
        </div>
        <?php
        if (isset($_GET['submit'])){
            $number1 = $_GET['number'];
            $count = 1;
            if($number1<100){
                do{
                    echo 'เพิ่มค่าทีละ 5 รอบที่ ',$count,' มีค่า = ',$number1,'<br>'
                    $number1+=5;
                    $count++;
                }while ($number1<=100);
            }else{
                echo 'ตัวเลขที่ป้อนเข้ามามากกว่า 100';
            }
        }
        ?>
    </body>
</html>
