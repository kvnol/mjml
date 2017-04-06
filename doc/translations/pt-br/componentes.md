# Componentes

Os componentes são o núcleo do MJML. Um componente é uma abstração do mais complexo layout de e-mail responsivo. Ele expõe os atributos e permite que você interaja com o aspecto final do componente.

O MJML sai da caixa trazendo uma série de componentes padrão para ajudar o desenvolvimnto fácil do seu primeiro modelo de e-mail sem ter de reinventar a roda.

Por exemplo, o componente `mj-button` possui um HTML complexo por dentro:

``` html

<!-- MJML -->
<mj-button href="#">
    Olá!
</mj-button>

<!-- HTML -->
<table cellpadding="0" cellspacing="0" style="border:none;border-radius:3px;" align="center">
  <tbody>
    <tr>
      <td style="background-color:#414141;border-radius:3px;color:#ffffff;cursor:auto;" align="center" valign="middle" bgcolor="#414141">
        <a class="mj-content" href="#" style="display:inline-block;text-decoration:none;background-color:#414141;border:1px solid #414141;border-radius:3px;color:#ffffff;font-size:13px;font-weight:bold;padding:15px 30px;" target="_blank">
          Olá!
        </a>
      </td>
    </tr>
  </tbody>
</table>
```
