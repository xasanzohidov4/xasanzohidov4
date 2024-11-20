<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>lotint cyrillic</title>
    <link href="https://stackpath.bootstrapcdn.com/bootstrap/4.5.2/css/bootstrap.min.css" rel="stylesheet">
</head>

<body class="hg-light">

    <div class="container mt-5">
    <h1 class="text-center mb-4">latin-> cyrillic</h1>
    <div class="row justify-content-content">
        <div class="col-md-6">
         <div class="form-group">
            <input type="text" id="latinText" class="form-group">
        </div>
        <button onclick="convertToCyrillic()" class="btn btn-primary btn-block">CONVERT</button>
        <p id="cyrillicText" class="mt-4 p-3 border rounded bg white text-center"></p>
      </div>
    </div>
 </div>
 <script>
    function convertToCyrillic() {
        const latinToCyrillicMap = {
            'a': 'а', 'b': 'б', 'v': 'в', 'g': "г", 'd': 'д','D':'Д',
            'e': 'е', 'yo': 'ё', 'j': 'ж', 'z': 'з', 'i': 'и',
            'y': 'й', 'k': 'к', 'l': 'л', 'm': 'м', 'n': 'н',
            'o': 'о', 'p': 'п', 'r': 'р', 's': 'с', 't': 'т',
            'u': 'у', 'f': 'ф', 'kh': 'х', 'ts': 'ц', 'ch': 'ч',
            'sh': 'ш', 'shch': 'щ', '': 'ъ', 'y': 'ы', '': 'ь',
            'e': '', 'yu': 'ю', 'ya': 'я', "o'":" Ў", "g'": "ғ",
        };
        
        let latinText = document.getElementById('latinText').value.toLowerCase();
        let cyrillicText = '';

        let i = 0;
        while (i < latinText.length) {
            let twoChar = latinText.substr(i, 2);
            let oneChar = latinText.substr(i, 1);

            if (latinToCyrillicMap[twoChar]) {
                cyrillicText += latinToCyrillicMap[twoChar];
                i += 2;
            } else if (latinToCyrillicMap[oneChar]) {
                cyrillicText += latinToCyrillicMap[oneChar];
                i++;
            } else {
                cyrillicText += oneChar;
                i++;
            }
        }

        document.getElementById('cyrillicText').innerText = cyrillicText;
    }
</script>

</body>

</html>- 👋 Hi, I’m @xasanzohidov4
- 👀 I’m interested in ...
- 🌱 I’m currently learning ...
- 💞️ I’m looking to collaborate on ...
- 📫 How to reach me ...
- 😄 Pronouns: ...
- ⚡ Fun fact: ...

<!---
xasanzohidov4/xasanzohidov4 is a ✨ special ✨ repository because its `README.md` (this file) appears on your GitHub profile.
You can click the Preview link to take a look at your changes.
--->
