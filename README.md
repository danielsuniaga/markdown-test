<!-- HEADING -->

# my title

## my title h2

### my title h3

#### my title h4

##### my title h5

###### my title h6

<!-- Italic -->

this is an *italic* text

<!-- Strong -->

this is an **strong** text

<!-- strikethrogh -->

this is an ~~texto~~ text 

<!-- UL -->

* APPLE
    * APPLE 2
* ORANGE
    *   ASDASDADA
* ETC

1. APPLE
2. ORANGE
3. ETC

<!-- ENLACE -->

[faztweb.com](https://www.faztweb.com)

[faztweb.com](https://www.faztweb.com "Custom title")

<!-- CITAS -->

> this a quote

<!-- HR -->
` console.log("test") `

```javascript
function ingresar_carro() {
    var placa = $("#placa").val();
    var dats = new obt_dats_pla(placa,'2');
    $.ajax({
        async: true,
        type: "POST",
        url: "../gestion/parqueadero/ges_par.php",
        data: {
            data: dats
        },
        success: function(data) 
        {
            console.log(data);
            
            var a = $.parseJSON(data);

            if (a['Codigo']=='1') 
            {
                $('#btn_ingresar').attr("disabled", true).css('display','none');
                $('#form2').css('display','none');
                swal(a['Tipo'],a['Mensaje'],a['acc']);
                cargar_formulario();
            }
            else
            {
                swal(a['Tipo'],a['Mensaje'],a['acc']);
                
                /*if (a['Codigo']=='2') 
                {
                    $('#btn_ingresar').attr("disabled", true).css('display','none');
                }
                */
            }

        }
    });

}


```

```python
print("Hola mundo")
```

```html
<h1>hola mundo</h1>
```

<!-- TABLA -->

| Column 1 | Column 2 | Column 3 |
|----------|----------|----------|
| Row 1    | Cell 2   | Cell 3   |
| Row 2    | Cell 5   | Cell 6   |
| Row 3    | Cell 8   | Cell 9   |


<!-- IMAGEN -->
![Descripción de la imagen](31112.jpg "Leyenda")

<!-- GITHUB MARKDOWN-->

* [X] Task 1
* [ ] Task 2
* [ ] Task 3
* [X] Task 4

@dsuniaga :smiley: :+1: