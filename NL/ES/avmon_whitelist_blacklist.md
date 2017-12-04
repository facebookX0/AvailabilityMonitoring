---

copyright:
  years: 2015, 2017
lastupdated: "2017-11-07"

---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}
{:codeblock: .codeblock}

# Bloqueo y filtrado con la lista blanca y la lista negra
{: #avmon_filters}

Utilice la lista blanca y la lista negra para determinar a qué recursos se enviarán solicitudes y qué recursos contribuyen a las métricas y al estado de las pruebas de aplicación. Las listas blancas y negras sólo están disponibles para páginas web y pruebas de comportamiento programado.
{: shortdesc}

Los campos **Lista blanca** y **Lista negra** definen los recursos a los que la prueba puede o no acceder y los recursos que contribuyen a las métricas y al estado de las pruebas. La lista blanca y la lista negra pueden controlar qué dependencias y recursos contribuyen a los tiempos de respuesta de sus aplicaciones web probadas, como por ejemplo métricas de terceros. Puede configurar la Lista blanca y la Lista negra al crear una página web o una prueba de comportamiento programado.

Puede utilizar la **Lista blanca** para definir los dominios y los URL permitidos; a continuación, utilice la **Lista negra** para bloquear elementos específicos de sus ubicaciones permitidas.

## Sintaxis

Utilice comas (,) para separar elementos en la Lista negra y la Lista blanca. Utilice el símbolo de comodín (\*) para filtrar elementos de cada URL o dominio.

## Lista blanca

Añada URL o dominios que desee incluir en los cálculos de solicitudes y de métricas en el campo Lista blanca. Puede listar hasta 10 elementos en la Lista blanca. Cada elemento no puede superar los 200 caracteres. Todos los dominios y URL que no coincidan con los elementos de la Lista blanca se bloquean.

Por ejemplo:
```
ibm.com, *developerworks*, *.s81c.com/*
```
{: codeblock}

## Lista negra

Añada URL o dominios que desee bloquear de los cálculos de solicitudes y de métricas en el campo Lista negra. Puede listar hasta 20 elementos en la Lista negra. Cada elemento no puede superar los 200 caracteres.

Por ejemplo:
```
*.profile.*.cloudfront.net/*.png
```
{: codeblock}

## Comportamiento de filtrado y de bloqueo

Las pruebas pueden tener tanto una Lista blanca como una Lista negra. Al determinar qué ubicaciones están permitidas o bloqueadas, la Lista negra siempre sobrescribe la Lista blanca. La tabla siguiente muestra el comportamiento de filtrado y de bloqueo para todos los casos de ejemplo de la Lista blanca y de la Lista negra.

<table id="avmon_whitelist_blacklist__table_gyg_vvp_fbb">
<caption>Tabla 1. Comportamiento de filtrado y de bloqueo para la Lista blanca y la Lista negra</caption>
<thead>
<tr>
<th>Lista negra</th>
<th>Lista blanca</th>
<th>Comportamiento</th>
<th>Motivo</th>
</tr>
</thead>
<tbody>
<tr>
<td>Vacío</td>
<td>Vacío</td>
<td>Permitir acceso</td>
<td>No hay reglas de filtrado especificadas.</td>
</tr>
<tr>
<td>Vacío</td>
<td>URL no coincide con la entrada de la lista</td>
<td>Bloquear acceso</td>
<td>URL no está en la lista blanca.</td>
</tr>
<tr>
<td>Vacío</td>
<td>URL coincide con la entrada de lista</td>
<td>Permitir acceso</td>
<td>URL está en la lista blanca. No hay entrada de lista negra para bloquear el acceso.</td>
</tr>
<tr>
<td>URL no coincide con la entrada de la lista</td>
<td>Vacío</td>
<td>Permitir acceso</td>
<td>URL no está en la lista negra. No hay entrada de lista blanca para bloquear el acceso.</td>
</tr>
<tr>
<td>URL coincide con la entrada de lista</td>
<td>Vacío</td>
<td>Bloquear acceso</td>
<td>URL está en la lista negra.</td>
</tr>
<tr>
<td>URL no coincide con la entrada de la lista</td>
<td>URL no coincide con la entrada de la lista</td>
<td>Bloquear acceso</td>
<td>URL no está en la lista blanca.</td>
</tr>
<tr>
<td>URL no coincide con la entrada de la lista</td>
<td>URL coincide con la entrada de lista</td>
<td>Permitir acceso</td>
<td>URL está en la lista blanca. URL no está en la lista negra.</td>
</tr>
<tr>
<td>URL coincide con la entrada de lista</td>
<td>URL no coincide con la entrada de la lista</td>
<td>Bloquear acceso</td>
<td>URL no está en la lista blanca. URL está en la lista negra.</td>
</tr>
<tr>
<td>URL coincide con la entrada de lista</td>
<td>URL coincide con la entrada de lista</td>
<td>Bloquear acceso</td>
<td>URL está en la lista negra. La entrada de lista negra sobrescribe la entrada de lista blanca.</td>
</tr>
</tbody>
</table>
