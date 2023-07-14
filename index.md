# TABLA DE FORMATO DE CAMPOS DE UN DOCUMENTO ELECTRÓNICO (DE)
Schema XML 18: DE_v150.xsd (Documento Electrónico)
## AA. Campos que identifican el formato electrónico XML (AA001-AA009)

| Grupo | ID | Campo | Descripción | Nodo Padre | Tipo Dato | Longitud | Ocurrencia | Observaciones |
| --- | --- | --- | --- | --- | --- | --- | --- | --- |
| AA | AA001 | rDE | Documento Electrónico elemento raíz | Raíz | G | | 1-1 | |
| AA | AA002 | dVerFor | Versión del formato | AA001 | N | 3 | 1-1 | Control de versiones <br>Este campo debe contener la versión 150

## A. Campos firmados del Documento Electrónico (A001-A099)

| Grupo | ID | Campo | Descripción | Nodo Padre | Tipo Dato | Longitud | Ocurrencia | Observaciones |
| --- | --- | --- | --- | --- | --- | --- | --- | --- |
| A | A001 | DE | Campos firmados del DE | AA001 |G | | 1-1 | |
| A | A002 | Id | Identificador del DE | A001 | A | 44 | | **Atributo del Tag \<DE>** <br>**NOTA:** Con carácter excepcional cuando un RUC contenga letras para efectos del cálculo del Dígito verificador y la generación del CDC se realizará la conversión de dicha letra por su valor en código ASCI|
| A | A003 |dDVId | Dígito verificador del identificador del DE | A001 | N | 1 | 1-1 | Según algoritmo módulo 11 |
| A | A004 | dFecFirma | Fecha de la firma | A001 | F | 19 | 1-1 | La fecha y hora de la firma digital debe ser anterior a la fecha y hora de transmisión al SIFEN <br>El certificado digital debe estar vigente al momento de la firma digital del DE <br>Fecha y hora en el formato AAAA-MM-DDThh:mm:ss <br>El plazo límite de transmisión del DE al SIFEN para la aprobación normal es de 72 h contadas a partir de la fecha y hora de la firma digital.
| A | A005 | dSisFact | Sistema de facturación | A001 | N | 1 | 1-1 | 1=Sistema de facturación del contribuyente <br>2=SIFEN solución gratuita |
