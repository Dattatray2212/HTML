# HTML
DOCTYPE html>
<html lang="en">
<head>
	<meta charset="UTF-8">
	<title>Хм</title>
	<style>
		fieldset{
			width: 800px;
		}
		.button{
			margin-left: 20px;
		}
	</style>
</head>
<body>
	<fieldset>
	<legend>Яблочная дилемма</legend>
	<form action="">
		Введите яблоки Маши: <input type="text" id="Masha" class="input" name="Masha">
		Введите яблоки Пети: <input type="text" id="Petya" class="input" name="Petya">
		<input type="submit" onclick="applesProblem()" class="button" value="Рассчитать"></input>
	</form>
	</fieldset>
	<script>
		function applesProblem(){
			class chelovek{
				constructor(name){
				this.name = name;
				this.apples = 0;
			}
		}
	let Petya = new chelovek("Petya");
	let Masha = new chelovek("Masha");
	let Dima = new chelovek("Dima");
	Dima.apples = 8;
	Masha.apples = parseInt(document.getElementById('Masha').value);
	Petya.apples = parseInt(document.getElementById('Petya').value);
	document.getElementById('Masha').value = "";
	document.getElementById('Petya').value = "";
	if (Petya.apples >= Masha.apples ){
	alert("Ничего не произошло.У Пети много яблок");
	} else {
		Petya.apples += Math.round(Masha.apples/2);
		Masha.apples -= Math.round(Masha.apples/2);
		if (Masha.apples < 5){
		Masha.apples += 2;
		Dima.apples -= 2;
		}
		if (Petya.apples >= 7 && Petya.apples >= 17){
		Petya.apples -= 7;
		Petya.apples -= 10;
		Dima.apples += 10;
		alert(`Количество яблок\nУ Маши: ${Masha.apples}\nУ Пети: ${Petya.apples}\nУ Димы: ${Dima.apples}`);
		} else if (Petya.apples >= 7){
		Petya.apples -= 7;
		Masha.apples -= 2;
		Dima.apples += 2;
		alert(`Количество яблок\nУ Маши: ${Masha.apples}\nУ Пети: ${Petya.apples}\nУ Димы: ${Dima.apples}`);
		} else {
		Petya.apples = 0;
		Masha.apples -= 2;
		Dima.apples += 2;
		alert(`Количество яблок\nУ Маши: ${Masha.apples}\nУ Пети: ${Petya.apples}\nУ Димы: ${Dima.apples}`);
	}	
	}
}
	</script>
</body>
</html>

