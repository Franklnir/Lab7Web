# Lab7Web

<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<title>PHP Dasar</title>
</head>
<body>
<h1>Belajar PHP Dasar</h1>
<?php
echo "Hello World";
?>
</body>
</html>
<?php
$nim = "31231051";
$nama = 'Irsyad';
echo "NIM : " . $nim . "<br>";
echo "Nama : $nama";
?>

![image](https://github.com/user-attachments/assets/a7399fa9-6354-4f57-a39e-2abff99b28af)

### langkah 2
<?php
echo 'Selamat Datang ' . $_GET['nama'];
?>
http://localhost/lab7_php_dasar/latihan2.php?nama=Irsyad
![image](https://github.com/user-attachments/assets/c6b01ce2-5052-40a2-b887-70eace0a301a)

### langkah 3

<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<title>PHP Dasar</title>
</head>
<body>
<h2>Form Input</h2>
<form method="post">
<label>Nama: </label>
<input type="text" name="nama">
<input type="submit" value="Kirim">
</form>
<?php
echo 'Selamat Datang ' . $_POST['nama'];
?>
</body>
</html>

![image](https://github.com/user-attachments/assets/2e8fb358-c54d-43eb-b300-39471fdf3d64)

### langkah 4
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>PHP Dasar</title>
</head>
<body>
    <h2>Form Input</h2>
    <form method="post">
        <label>Nama: </label>
        <input type="text" name="nama">
        <input type="submit" value="Kirim">
    </form>
    <?php
    if (isset($_POST['nama'])) {
        echo 'Selamat Datang ' . htmlspecialchars($_POST['nama']) . '<br>';
    }
    ?>
</body>
</html>

<?php
$gaji = 1000000;
$pajak = 0.1;
$thp = $gaji - ($gaji * $pajak);

echo "<h2>Perhitungan Gaji</h2>";
echo "Gaji sebelum pajak = Rp. $gaji <br>";
echo "Gaji yang dibawa pulang = Rp. $thp <br>";
?>

<?php
$nama_hari = date("l");
echo "<h2>Hari Ini (if-elseif)</h2>";
if ($nama_hari == "Sunday") {
    echo "Minggu";
} elseif ($nama_hari == "Monday") {
    echo "Senin";
} else {
    echo "Selasa";
}
?>

<?php
echo "<h2>Hari Ini (switch)</h2>";
switch ($nama_hari) {
    case "Sunday":
        echo "Minggu";
        break;
    case "Monday":
        echo "Senin";
        break;
    case "Tuesday":
        echo "Selasa";
        break;
    default:
        echo "sabtu";
        break;
}
?>

<?php
echo "<h2>Perulangan dengan For</h2>";
echo "Perulangan 1 sampai 10: <br>";
for ($i = 1; $i <= 10; $i++) {
    echo "Perulangan ke: $i <br>";
}
echo "Perulangan Menurun dari 10 ke 1: <br>";
for ($i = 10; $i >= 1; $i--) {
    echo "Perulangan ke: $i <br>";
}
?>

<?php
echo "<h2>Perulangan dengan While</h2>";
$i = 1;
echo "Perulangan 1 sampai 10: <br>";
while ($i <= 10) {
    echo "Perulangan ke: $i <br>";
    $i++;
}
?>

<?php
echo "<h2>Perulangan dengan Do-While</h2>";
$i = 1;
echo "Perulangan 1 sampai 10: <br>";
do {
    echo "Perulangan ke: $i <br>";
    $i++;
} while ($i <= 10);
?>
![image](https://github.com/user-attachments/assets/b97a8617-6193-4133-a858-1bdfba0ab755)
![image](https://github.com/user-attachments/assets/fecd5b43-9e69-4c10-9363-3cd53837626e)

### Pertanyaan dan Tugas
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Form Input PHP</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            background: linear-gradient(120deg, #74b9ff, #81ecec);
            color: #2d3436;
            margin: 0;
            padding: 0;
            display: flex;
            flex-direction: column;
            align-items: center;
            justify-content: center;
            min-height: 100vh;
        }
        h2 {
            color: #d63031;
        }
        form {
            background-color: #ffffff;
            padding: 20px;
            border-radius: 10px;
            box-shadow: 0 4px 8px rgba(0, 0, 0, 0.2);
            max-width: 400px;
            width: 100%;
        }
        label {
            display: block;
            margin-bottom: 8px;
            font-weight: bold;
        }
        input, select {
            width: 100%;
            padding: 10px;
            margin-bottom: 15px;
            border: 1px solid #dfe6e9;
            border-radius: 5px;
        }
        input[type="submit"] {
            background-color: #0984e3;
            color: #fff;
            border: none;
            cursor: pointer;
            transition: background-color 0.3s ease;
        }
        input[type="submit"]:hover {
            background-color: #74b9ff;
        }
        .result {
            margin-top: 20px;
            background-color: #fff;
            padding: 20px;
            border-radius: 10px;
            box-shadow: 0 4px 8px rgba(0, 0, 0, 0.2);
            max-width: 400px;
            width: 100%;
        }
    </style>
</head>
<body>
    <h2>Form Input PHP</h2>
    <form method="post">
        <label for="nama">Nama: </label>
        <input type="text" name="nama" id="nama" required>
        <label for="tanggal_lahir">Tanggal Lahir (YYYY-MM-DD): </label>
        <input type="date" name="tanggal_lahir" id="tanggal_lahir" required>
        <label for="pekerjaan">Pekerjaan: </label>
        <select name="pekerjaan" id="pekerjaan" required>
            <option value="Programmer">Programmer</option>
            <option value="Designer">Designer</option>
            <option value="Manager">Manager</option>
            <option value="Freelancer">Freelancer</option>
        </select>
        <input type="submit" value="Kirim">
    </form>
    <?php
    if ($_SERVER['REQUEST_METHOD'] == 'POST') {
        $nama = htmlspecialchars($_POST['nama']);
        $tanggal_lahir = $_POST['tanggal_lahir'];
        $pekerjaan = $_POST['pekerjaan'];
        $today = new DateTime();
        $birthDate = new DateTime($tanggal_lahir);
        $age = $today->diff($birthDate)->y;
        $gaji_usd = 0;
        switch ($pekerjaan) {
            case 'Programmer':
                $gaji_usd = 8000;
                break;
            case 'Designer':
                $gaji_usd = 7000;
                break;
            case 'Manager':
                $gaji_usd = 1000;
                break;
            case 'Freelancer':
                $gaji_usd = 5000;
                break;
        }
        echo "<div class='result'>";
        echo "<h2>Hasil Input</h2>";
        echo "Nama: $nama <br>";
        echo "Tanggal Lahir: $tanggal_lahir <br>";
        echo "Umur: $age tahun <br>";
        echo "Pekerjaan: $pekerjaan <br>";
        echo "Gaji: $ " . number_format($gaji_usd, 2, '.', ',') . " (USD)<br>";
        echo "</div>";
    }
    ?>
</body>
</html>

![image](https://github.com/user-attachments/assets/36efa6a4-6dc3-4ff2-9712-99c35400ede2)




