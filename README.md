# Clave-de-Acceso-SRI
DLL para generar la clave de acceso al momento de la facturación electrónica.

Ejemplo:

Private Sub FacturaElectronica()
Dim fac As New FacturacionElectronicaAutoriza.FacturacionElectronica

sacadenuevo:
         fac.ClavesAcceso(CODIGO DEL DOCUMENTO A EMITIR "01", SECUENCIAL DEL DOCUMENTO, FECHA, NÚMERO DE ESTABLECIMEINTO O SUCURSAL, PUNTO DE EMISION O FACTURERO ELECTRONICO, RUC EMPRESA, AMBIENTE) '1 pruebas | 2 produccion

01 = FACTURA
03 = LIQUIDACION DE COMPRA
ETC

        If fac.generado.Length = 49 Then
            estoy = fac.generado
        Else
            GoTo sacadenuevo

        End If

End Sub
![image](https://user-images.githubusercontent.com/124838827/217856458-ac3821aa-bda3-4e80-b3ab-e43bb99668a3.png)
![image](https://user-images.githubusercontent.com/124838827/217856644-3bd5d54e-9952-4f75-990d-e0b92efb0b8f.png)
