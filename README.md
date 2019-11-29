# Perímetros
Perímetros dos projetos vigentes da São Paulo Urbanismo. Pode-se utilizar as urls como um serviço de dados. Veja mais abaixo como puxar os dados:

## Perímetros disponibilizados neste repositório: 

| Nome                                 | Projeto                            | url do github pages |
| ------------------------------------ |:----------------------------------:| :-------------------|
| Perímetro de expansão PIU Arco Tietê | PIU<sup>[1](#piu)</sup> Arco Tietê | [PerimetroExpansao_ArcoTiete.geojson](https://spurb.github.io/perimetros/PerimetroExpansao_ArcoTiete.geojson) |

<a name="piu">1</a>. Projeto de Intervenção Urbana - [Decreto nº 56.901, de 29 de março 2016](http://gestaourbana.prefeitura.sp.gov.br/wp-content/uploads/2016/03/Decreto-56.901.pdf)



### Instruções para consumir os perímetros na sua aplicação:
#### Javascript XHR
```javascript
var xhrRequest = new XMLHttpRequest()

xhrRequest.addEventListener("load", function (evt) {
    console.log(evt.target.response)
})

xhrRequest.open('GET', 'https://spurb.github.io/perimetros/PerimetroExpansao_ArcoTiete.geojson', true, null, null)
xhrRequest.send()
```

#### Python 3
```sh
# instale a lib 'requests'
pip install requests
```
No seu programa em python
```python
import requests
resposta = requests.get('https://spurb.github.io/perimetros/PerimetroExpansao_ArcoTiete.geojson')
print(resposta.text)
```