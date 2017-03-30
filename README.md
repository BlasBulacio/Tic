# Tic
Primer tp

Index:
<html>
	<body>	
		<form name="formulario" action="a.php" method="POST">
			Tu nombre <input type="text" name="nombre"><br>
			<input type="radio" name="genero" value="hombre"> hombre<br>
			<input type="radio" name="genero" value="mujer"> mujer<br>
			Elija un color
			<select name="color">
			<option value="rojo">rojo</option>
			<option value="azul">azul</option>
			<option value="violeta">violeta</option>
			</select> <br>
			Ultima pelicula que viste? <input type="text" name="pelicula"><br>
			<input type="submit" name="enviar" value="Enviar">
		</form>
	</body>
</html>

a.php:
<html>
	<body>	
		<?PHP
			if (isset($_POST["enviar"]))
			{
				if ($_POST["nombre"]!="")	
				{
					echo "Hola ".$_POST["nombre"];
				}
				else
				{
					echo "infradotado complete el nombre";
				}
				
				if($_POST["genero"]!=""){
							echo ". Sos ".$_POST["genero"];
				}else
				{
					echo ". No elegiste genero";
				}
				if($_POST["color"]!=""){
							echo ". Elegiste el color ".$_POST["color"];
				}else
				{
					echo ". No elegiste color";
				}
				
				if ($_POST["pelicula"]!="")	
				{
					echo ". Viste ".$_POST["pelicula"];
				}
				else
				{
					echo "C. omo que nunca viste una pelicula?";
				}
				
			}
			else
			{
				echo "imbecil vaya al  formulario";
				echo "<a href=\"index.php\">volver</a>";
			}
			?>
			
	</body>
</html>
