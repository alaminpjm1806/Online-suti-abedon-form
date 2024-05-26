<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>অনলাইন ছুটির আবেদন ফরম</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            background-color: #f2f2f2;
            display: flex;
            justify-content: center;
            align-items: center;
            height: 100vh;
            margin: 0;
        }
        .form-container {
            background-color: #fff;
            padding: 20px;
            border-radius: 8px;
            box-shadow: 0 0 10px rgba(0, 0, 0, 0.1);
            width: 100%;
            max-width: 500px;
        }
        .form-container h2 {
            text-align: center;
            margin-bottom: 20px;
        }
        .form-container label {
            display: block;
            margin-bottom: 8px;
            font-weight: bold;
        }
        .form-container input, .form-container textarea, .form-container select {
            width: 100%;
            padding: 10px;
            margin-bottom: 20px;
            border: 1px solid #ccc;
            border-radius: 4px;
        }
        .form-container button {
            width: 100%;
            padding: 10px;
            background-color: #4CAF50;
            color: white;
            border: none;
            border-radius: 4px;
            cursor: pointer;
            font-size: 16px;
        }
        .form-container button:hover {
            background-color: #45a049;
        }
        .form-container .hidden {
            display: none;
        }
    </style>
    <script>
        function togglePrescription() {
            var illnessSelect = document.getElementById("illness");
            var prescriptionUpload = document.getElementById("prescription-upload");
            if (illnessSelect.value === "yes") {
                prescriptionUpload.classList.remove("hidden");
            } else {
                prescriptionUpload.classList.add("hidden");
            }
        }
    </script>
</head>
<body>

<div class="form-container">
    <h2>অনলাইন ছুটির আবেদন ফরম</h2>
    <form action="#" method="post" enctype="multipart/form-data">
        <label for="name">নাম:</label>
        <input type="text" id="name" name="name" required>

        <label for="class">ক্লাস:</label>
        <input type="text" id="class" name="class" required>

        <label for="roll">রোল:</label>
        <input type="text" id="roll" name="roll" required>

        <label for="mobile">মোবাইল নম্বর:</label>
        <input type="tel" id="mobile" name="mobile" pattern="[0-9]{11}" required>

        <label for="reason">ছুটির কারণ:</label>
        <textarea id="reason" name="reason" rows="4" required></textarea>

        <label for="start_date">ছুটির শুরুর তারিখ:</label>
        <input type="date" id="start_date" name="start_date" required>

        <label for="end_date">ছুটির শেষ তারিখ:</label>
        <input type="date" id="end_date" name="end_date" required>

        <label for="illness">অসুস্থ:</label>
        <select id="illness" name="illness" onchange="togglePrescription()" required>
            <option value="no">না</option>
            <option value="yes">হ্যাঁ</option>
        </select>

        <div id="prescription-upload" class="hidden">
            <label for="prescription">ডাক্টারের প্রেসক্রিপশন আপলোড করুন:</label>
            <input type="file" id="prescription" name="prescription" accept="image/*">
        </div>

        <button type="submit">জমা দিন</button>
    </form>
</div>

</body>
</html>
