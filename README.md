# Pemograman Web
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Program 1 (project1.php)</title>
</head>
<body>
<h1> Aplikasi Kalkulator Sederhana</h1>
    <form action="kalkulator.php" method="post">
        Masukkan Bilangan Pertama: <input type="number" name="bilangan1"><br>
        Masukkan Bilangan Kedua: <input type="number" name="bilangan2"><br>   

        Pilih Operasi:
        <input type="radio" name="operasi" value="tambah"> Penjumlahan (+)
        <input type="radio" name="operasi" value="kurang"> Pengurangan (-)
        <input type="radio" name="operasi" value="kali"> Perkalian (*)
        <input type="radio" name="operasi" value="bagi"> Pembagian (/)<br>
        <input type="submit" value="Hitung">
    </form>
</body>
</html>

<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Program 2 (kalkulator.php)</title>
</head>
<body>
<?php
    $bilangan1 = $_POST['bilangan1'];
    $bilangan2 = $_POST['bilangan2'];
    $operasi = $_POST['operasi'];

    switch ($operasi) {
        case 'tambah':
            $hasil = $bilangan1 + $bilangan2;
            break;
        case 'kurang':
            $hasil = $bilangan1 - $bilangan2;
            break;
        case 'kali':
            $hasil = $bilangan1 * $bilangan2;
            break;
        case 'bagi':
            if ($bilangan2 == 0) {
                $hasil = "Tidak dapat dibagi dengan nol";
            } else {
                $hasil = $bilangan1 / $bilangan2;
            }
            break;
    }

    echo "Hasil Perhitungan: " . $hasil;
    ?>
</body>
</html>
