# Kalkulator
Belajar Jquery
<!DOCTYPE html>
<html>
<head>
<meta charset="UTF-8">
<title>Online</title>
<script src="jquery-3.6.0.js"></script>
<script>
   $(document).ready(function() {  
	 $("#tombol").click(function() {
        
        var a = parseInt($("#nilai1").val());
        var b = parseInt($("#nilai2").val());
        var operasi = $("#operasi").val();
        var total = $("#hasil").val();

        if(isNaN(a) || isNaN(b)) {
			alert('isi form dengan angka!')					    
	    } else {
	    	if(operasi=="+") {
				$("#hasil").val(a+b);
			}else if(operasi=="-") {
				$("#hasil").val(a-b);
			}else if(operasi=="*") {
				$("#hasil").val(a*b);
			}else if(operasi=="/") {
				$("#hasil").val(a/b);
			}	
		}

     })
   });
   </script>
</head>
<body>
	<p>-KALKULATOR-</p>
	<p>Masukan Nilai :</p>
	<p>
	Nilai 1	: <input type="text" id="nilai1">
	Nilai 2	: <input type="text" id="nilai2">
	</p> 
	Operasi : <select id="operasi"></br>
				<option value="+">Tambah</option>
				<option value="-">Pengurangan</option>
				<option value="*">Perkalian</option>
				<option value="/">Pembagian</option>				
			  </select>		 
	<p>	
		Hasil   : <input type="text" id="hasil"><br/>
	</p>

	<button id="tombol">Hitung</button>
</body>
</html>
