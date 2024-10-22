<!DOCTYPE html>
<html>
<head>
	<meta charset="utf-8">
	<meta name="viewport" content="width=device-width, initial-scale=1">
	<title></title>
</head>
<body>

<?php

$carros = [
    ["nombre" => "Toyota Corolla", "precio" => 20000],
    ["nombre" => "Honda Civic", "precio" => 22000],
    ["nombre" => "Ford Focus", "precio" => 21000],
    ["nombre" => "Chevrolet Cruze", "precio" => 19500],
    ["nombre" => "Volkswagen Golf", "precio" => 23000]
];


echo "Array inicial:\n";
foreach ($carros as $carro) {
    echo "Nombre: " . $carro["nombre"] . ", Precio: $" . $carro["precio"] . "\n";
}
echo "--------------------------\n";


array_push($carros, ["nombre" => "Mazda 3", "precio" => 22500]);
array_push($carros, ["nombre" => "Hyundai Elantra", "precio" => 20500]);


usort($carros, function($a, $b) {
    return strcmp($a["nombre"], $b["nombre"]);
});


echo "Array ordenado:\n";
foreach ($carros as $carro) {
    echo "Nombre: " . $carro["nombre"] . ", Precio: $" . $carro["precio"] . "\n";
}
?>
</body>
</html>