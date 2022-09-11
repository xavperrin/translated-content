---
title: <script>
slug: Web/HTML/Element/script
translation_of: Web/HTML/Element/script
---
<p>O <strong>elemento HTML <code>&lt;script&gt;</code></strong> é usado para incluir ou referenciar um script executável.</p>

<table class="properties">
 <tbody>
  <tr>
   <th scope="row"><a href="/en-US/docs/Web/HTML/Content_categories">Categorias de conteúdo</a></th>
   <td><a href="/en-US/docs/Web/HTML/Content_categories#Metadata_content">Conteúdo de metadados</a>, <a href="/en-US/docs/Web/HTML/Content_categories#Flow_content">Fluxo de conteúdo</a>, <a href="/en-US/docs/Web/HTML/Content_categories#Phrasing_content">Conteúdo fraseado</a>.</td>
  </tr>
  <tr>
   <th scope="row">Conteúdo Permitido</th>
   <td>Script dinâmico, como <code>text/javascript</code>.</td>
  </tr>
  <tr>
   <th scope="row">Omissão de tag</th>
   <td>{{no_tag_omission}}</td>
  </tr>
  <tr>
   <th scope="row">Pais permitidos</th>
   <td>Qualquer elemento que aceite <a href="/en-US/docs/Web/HTML/Content_categories#Metadata_content">conteúdo de metadados</a>, ou qualquer elemento que aceite <a href="/en-US/docs/Web/HTML/Content_categories#Phrasing_content">conteúdo fraseado</a>.</td>
  </tr>
  <tr>
   <th scope="row">Regras ARIA permitidas</th>
   <td>Nenhuma</td>
  </tr>
  <tr>
   <th scope="row">Interface DOM</th>
   <td>{{domxref("HTMLScriptElement")}}</td>
  </tr>
 </tbody>
</table>

<h2 id="Atributos">Atributos</h2>

<p>Esse elemento inclui os <a href="/pt-BR/docs/Web/HTML/Global_attributes">atributos globais</a>.</p>

<dl>
 <dt>{{htmlattrdef("async")}} {{HTMLVersionInline(5)}}</dt>
 <dd><p>Um atributo booleano indicando que o navegador deve, se possível, executar o script assíncronamente.</p>
 <div class="blockIndicator warning">
 <p>Esse atributo não deve ser utilizado se o atributo <code>src</code> estiver ausente (ex. scripts embutidos). Se incluído, nesse caso, ele não terá nenhum efeito.</p>
 </div>
 <p>Scripts inseridos dinamicamente (usando <code>document.createElement</code>) são executados assincronamente por padrão, então para torná-lo uma execução síncrona (ex. executar scripts na ordem que eles foram carregados) atribua <code>async=false</code>.</p>
 <p>Veja <a href="#browser_compatibility">Browser compatibility</a> para notas no suporte do navegador. Veja também  <a href="/en-US/docs/Games/Techniques/Async_scripts">Scripts assíncronos para asm.js</a>.</p></dd>
 <dt>{{htmlattrdef("crossorigin")}}</dt>
 <dd>Elementos <code>script</code> passam o mínimo de informação para  {{domxref('GlobalEventHandlers.onerror', 'window.onerror')}} em scripts que não passem na checagem do <a href="https://developer.mozilla.org/en-US/docs/HTTP_access_control">CORS</a>. Para permitir logs de erro para sites que usam domínios diferentes para arquivos estáticos, use esse atributo. Veja <a href="https://developer.mozilla.org/en-US/docs/Web/HTML/CORS_settings_attributes">CORS settings attributes</a> para uma explicação mais detalhada dos argumentos válidos.</dd>
 <dt>{{htmlattrdef("defer")}}</dt>
 <dd><p>Esse atributo Boleano é usado para indicar ao navegador que o script deve ser executado depois que o documento tenha sido parseado, mas antes de disparar o evento {{event("DOMContentLoaded")}}</p>
 <p>Scripts com o atributo <code>defer</code> vão impedir que o evento DOMContentLoaded seja disparado até que o script seja carregado e tenha terminado de ser <em>avaliado</em>.</p>
 <div class="blockIndicator warning">
 <p>Esse atributo não deve ser usado se o atibuto <code>src</code> estiver ausente (ex. scripts inline), nesse caso ele não vai ter efeito.</p>
 </div>
 <p>Para conseguir um efeito similar para scripts inseridos dinamicamente use <code>async=false</code>. Scripts com o atributo <code>defer</code> vão ser executados na ordem em que aparecem no <code>document</code>.</p>
 </dd>
 <dt>{{htmlattrdef("integrity")}}</dt>
 <dd>Contains inline metadata that a user agent can use to verify that a fetched resource has been delivered free of unexpected manipulation. See <a href="/en-US/docs/Web/Security/Subresource_Integrity">Subresource Integrity</a>.</dd>
 <dt>{{htmlattrdef("nomodule")}} {{experimental_inline}}</dt>
 <dd>This Boolean attribute is set to indicate that the script should not be executed in browsers that support<a href="https://hacks.mozilla.org/2015/08/es6-in-depth-modules/"> ES6 modules</a> — in effect, this can be used to serve fallback scripts to older browsers that do not support modular JavaScript code.</dd>
 <dt>{{htmlattrdef("src")}}</dt>
 <dd>This attribute specifies the <abbr>URI</abbr> of an external script; this can be used as an alternative to embedding a script directly within a document. If a <code>script</code> element has a <code>src</code> attribute specified, it should not have a script embedded inside its tags.</dd>
 <dt>{{htmlattrdef("text")}}</dt>
 <dd>Like the <code>textContent </code>attribute, this attribute sets the text content of the element.  Unlike the <code>textContent </code>attribute, however, this attribute is evaluated as executable code after the node is inserted into the DOM.</dd>
 <dt>{{htmlattrdef("type")}}</dt>
 <dd>
 <p>Indicates the type of script represented. The value of this attribute will be in one of the following categories:</p>

 <ul>
  <li><strong>Omitted or a JavaScript MIME type:</strong> For HTML5-complient browsers this indicates the script is JavaScript. HTML5 spec urges authors to omit the attribute rather than provided a redundant MIME type. In earlier browsers, this identified the scripting language of the embedded or imported (via the <code>src</code> attribute) code. JavaScript MIME types are <a href="https://developer.mozilla.org/en-US/docs/Web/HTTP/Basics_of_HTTP/MIME_types">listed in the specification</a>.</li>
  <li><strong><code>module</code>:</strong> {{HTMLVersionInline(5)}} For HTML5-complient browsers the code is treated as a JavaScript module. Processing of the script contents are not affected by the <code>charset</code> and <code>defer</code> attributes. For information on using <code>module</code>, see <a class="external external-icon" href="https://hacks.mozilla.org/2015/08/es6-in-depth-modules/">ES6 in Depth: Modules</a>. {{experimental_inline}}</li>
  <li><strong>Any other value or MIME type:</strong> Embedded content is treated as a data block which won't be processed by the browser. The <code>src</code> attribute will be ignored.</li>
 </ul>

 <p>Note that in Firefox you can use advanced features such as let statements and other features in later JS versions, by using <code>type=application/javascript;version=1.8</code> {{Non-standard_inline}}. Beware, however, that as this is a non-standard feature, this will most likely break support for other browsers, in particular Chromium-based browsers.</p>

 <p>For how to include <em>exotic programming languages</em>, read about <a href="https://developer.mozilla.org/en-US/Add-ons/Code_snippets/Rosetta">Rosetta</a>.</p>
 </dd>
</dl> 

<h3 id="Atributos_obsoletos">Atributos obsoletos</h3>

<dl>
<dt>{{htmlattrdef("charset")}} {{Deprecated_inline}}</dt>
 <dd>If present, its value must be an ASCII case-insensitive match for "<code>utf-8</code>". Both it’s unnecessary to specify the <code>charset</code> attribute, because documents must use UTF-8, and the <code>script</code> element inherits its character encoding from the document.</dd>
 <dt>{{htmlattrdef("language")}} {{Deprecated_inline}}</dt>
 <dd>Like the <code>type</code> attribute, this attribute identifies the scripting language in use. Unlike the <code>type</code> attribute, however, this attribute’s possible values were never standardized. The <code>type</code> attribute should be used instead.</dd>
</dl>

<h2 id="Notas">Notas</h2>

<p>Scripts without <code>async</code> or <code>defer</code> attributes, as well as inline scripts, are fetched and executed immediately, before the browser continues to parse the page.</p>

<p>The script should be served with the <code>text/javascript</code> MIME type, but browsers are lenient and only block them if the script is served with an image type (<code>image/*</code>), a video type (<code>video/*</code>), an audio (<code>audio/*</code>) type, or <code>text/csv</code>. If the script is blocked, an {{event("error")}} is sent to the element, if not a {{event("success")}} event is sent.</p>

<h2 id="Exemplos">Exemplos</h2>

<pre class="brush: html notranslate">&lt;!-- HTML4 and (x)HTML --&gt;
&lt;script type="text/javascript" src="javascript.js"&gt;&lt;/script&gt;

&lt;!-- HTML5 --&gt;
&lt;script src="javascript.js"&gt;&lt;/script&gt;
</pre>

<h2 id="Specifications">Specifications</h2>

<table class="standard-table">
 <thead>
  <tr>
   <th scope="col">Specification</th>
   <th scope="col">Status</th>
   <th scope="col">Comments</th>
  </tr>
 </thead>
 <tbody>
  <tr>
   <td>{{SpecName('HTML WHATWG', "scripting.html#the-script-element", "&lt;script&gt;")}}</td>
   <td>{{Spec2('HTML WHATWG')}}</td>
   <td>Adds the module type</td>
  </tr>
  <tr>
   <td>{{SpecName('HTML5 W3C', 'scripting-1.html#script', '&lt;script&gt;')}}</td>
   <td>{{Spec2('HTML5 W3C')}}</td>
   <td></td>
  </tr>
  <tr>
   <td>{{SpecName('HTML4.01', 'interact/scripts.html#h-18.2.1', '&lt;script&gt;')}}</td>
   <td>{{Spec2('HTML4.01')}}</td>
   <td></td>
  </tr>
  <tr>
   <td>{{SpecName('Subresource Integrity', '#htmlscriptelement', '&lt;script&gt;')}}</td>
   <td>{{Spec2('Subresource Integrity')}}</td>
   <td>Adds the integrity attribute.</td>
  </tr>
 </tbody>
</table>

<h2 id="Browser_compatibility">Compatibilidade com navegadores</h2>

{{Compat("html.elements.script")}}

<h2 id="See_also">See also</h2>

<ul>
 <li>{{domxref("document.currentScript")}}</li>
 <li><a href="https://pie.gd/test/script-link-events/">Ryan Grove's &lt;script&gt; and &lt;link&gt; node event compatibility chart</a></li>
</ul>

<div>{{HTMLRef}}</div>