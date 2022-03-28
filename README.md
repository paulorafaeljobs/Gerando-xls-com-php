# Gerando xls com php
Gerar planilha excel com Php
```php
<?php
$arquivo = 'relatorio.xls';
$html = '';
$html .= '<table border="1">';
$html .= '<tr>';
$html .= '<td colspan="5">Relatório</tr>';
$html .= '</tr>';
		
$html .= '<tr>';
$html .= '<td><b>ID</b></td>';
$html .= '<td><b>Nome</b></td>';
$html .= '<td><b>E-mail</b></td>';
$html .= '<td><b>Assunto</b></td>';
$html .= '<td><b>Data</b></td>';
$html .= '</tr>';

$html .= '<tr>';
$html .= '<td>1</td>';
$html .= '<td>Paulo Rafael</td>';
$html .= '<td>paulo.rafael.jobs@gmail.com</td>';
$html .= '<td>Email</td>';
$html .= '<td>01/01/2000</td>';
$html .= '</tr>';
$html .= '</table>';

		
header ("Expires: Mon, 26 Jul 1997 05:00:00 GMT");
header ("Last-Modified: " . gmdate("D,d M YH:i:s") . " GMT");
header ("Cache-Control: no-cache, must-revalidate");
header ("Pragma: no-cache");
header ("Content-type: application/x-msexcel");
header ("Content-Disposition: attachment; filename=\"{$arquivo}\"" );
header ("Content-Description: PHP Generated Data" );
echo $html;
exit; 
```
