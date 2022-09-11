---
title: <ruby>
slug: Web/HTML/Element/ruby
tags:
  - Elemento
  - HTML
  - Referencia
  - Semântica HTML
  - Web
translation_of: Web/HTML/Element/ruby
---
<h2 id="Summary" name="Summary">Resumo</h2>

<p>O <strong>elemento</strong> <strong>HTML <code>&lt;ruby&gt;</code> </strong> representa uma anotação ruby. Anotações ruby são para mostrar a pronúncia de caracteres do Leste Asiático</p>

<ul>
 <li><dfn><a href="/en-US/docs/Web/HTML/Content_categories" title="HTML/Content_categories">Categorias de conteúdo</a></dfn> <a href="/en-US/docs/Web/HTML/Content_categories#Flow_content" title="HTML/Content_categories#Phrasing_content">Conteúdo de fluxo</a>, <a href="/en-US/docs/Web/HTML/Content_categories#Phrasing_content" title="HTML/Content_categories#Phrasing_content">conteúdo fraseado</a>, conteúdo palpável.</li>
 <li><dfn>Conteúdo permitido</dfn> <a href="/en-US/docs/Web/HTML/Content_categories#Phrasing_content" title="HTML/Content_categories#Phrasing_content">Conteúdo fraseado</a>.</li>
 <li><dfn>Omissão de tag</dfn> {{no_tag_omission}}</li>
 <li><dfn>Elementos pais permitidos</dfn>Ver prosa</li>
 <li><dfn>Interface DOM</dfn> {{domxref("HTMLElement")}}</li>
</ul>

<h2 id="Attributes" name="Attributes">Atributos</h2>

<p>Esse elemento somente inclui os <a href="/pt-BR/docs/Web/HTML/Global_attributes" title="HTML/Atributos Globais">atributos globais</a>.</p>

<h2 id="Examples" name="Examples">Exemplos</h2>

<h3 id="Exemplo_1_Caracter">Exemplo 1: Caracter</h3>

<pre class="brush:html">&lt;ruby&gt;
  漢 &lt;rp&gt;(&lt;/rp&gt;&lt;rt&gt;Kan&lt;/rt&gt;&lt;rp&gt;)&lt;/rp&gt;
  字 &lt;rp&gt;(&lt;/rp&gt;&lt;rt&gt;ji&lt;/rt&gt;&lt;rp&gt;)&lt;/rp&gt;
&lt;/ruby&gt;</pre>

<h3 id="Exemplo_2_Palavra">Exemplo 2: Palavra</h3>

<pre class="brush:html">&lt;ruby&gt;
  明日 &lt;rp&gt;(&lt;/rp&gt;&lt;rt&gt;Ashita&lt;/rt&gt;&lt;rp&gt;)&lt;/rp&gt;
&lt;/ruby&gt;</pre>

<h2 id="Specifications" name="Specifications">Especificações</h2>

<table class="standard-table">
 <thead>
  <tr>
   <th scope="col">Especificação</th>
   <th scope="col">Status</th>
   <th scope="col">Comentário</th>
  </tr>
 </thead>
 <tbody>
  <tr>
   <td>{{SpecName('HTML WHATWG', 'text-level-semantics.html#the-ruby-element', '&lt;ruby&gt;')}}</td>
   <td>{{Spec2('HTML WHATWG')}}</td>
   <td> </td>
  </tr>
  <tr>
   <td>{{SpecName('HTML5 W3C', 'text-level-semantics.html#the-ruby-element', '&lt;ruby&gt;')}}</td>
   <td>{{Spec2('HTML5 W3C')}}</td>
   <td> </td>
  </tr>
 </tbody>
</table>

<h2 id="Browser_compatibility">Compatibilidade com navegadores</h2>

{{Compat("html.elements.ruby")}}

<h2 id="See_also" name="See_also">Veja também</h2>

<ul>
 <li>{{HTMLElement("rt")}}</li>
 <li>{{HTMLElement("rp")}}</li>
</ul>

<p>{{ HTMLRef }}</p>