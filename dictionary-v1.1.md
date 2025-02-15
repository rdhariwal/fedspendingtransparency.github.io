---
published: true
permalink: /dictionary-v1.1/
layout: hero
filename: dictionary-v1.1.md
title: DATA Act Information Model Schema Data Dictionary v1.1
---
<div class="article-wrap">
<p><i>December 22, 2017:</i> Treasury released the DATA Act Information Model Schema (DAIMS) v1.2. DAIMS v1.2 is a minor update of the schema and will be implemented with the submission of fiscal year 2018 quarter 3 data. Find out more information at <a href="{{ site.baseurl }}/DAIMS-v1.2/" title="DAIMS v1.2">DAIMS v1.2</a> or its <a href="{{ site.baseurl }}/dictionary-v1.2/" title="Data dictionary v1.2">Data Dictionary v1.2</a>.</p>

<h1> DATA Act Information Model Schema Data Dictionary v1.1 </h1>
<p><i>Released June 30, 2017 (Updated December 22, 2017)</i></p>
<h2 style="margin-top:50px">Background</h2>
<p>The DATA Act Information Model Schema (DAIMS; DATA Act Schema) provides an overall view of the hundreds of distinct data elements used to tell the story of how federal dollars are spent. The purpose of the data dictionary is to provide assistance in understanding the data elements within the DATA Act Schema.</p>

<p>The DATA Act directs the Office of Management and Budget (OMB) and the U.S. Treasury Department (Treasury) to establish government-wide data standards for federal funds and entities receiving such funds. The DAIMS will help to ensure that information is consistent and comparable and ultimately make data more accessible, reusable, and provide the necessary linkages between financial events. By making federal spending data accessible, searchable, reusable, and more reliable, the public can understand government spending. The DATA Act Schema will also reduce the need for massive system changes across federal agencies to collect information and allow agencies to focus on managing data.</p>

<h2>DAIMS v1.1 Release</h2>
<p><i>June 30, 2017</i> - DAIMS v1.1 is a minor update to transition financial assistance reporting to the DATA Act Broker, to better align with another federal government source system, and to provide clarifications for improved usability. These changes have a minimal impact to the data submissions that agencies make to the DATA Act Broker. DAIMS v1.1 will be implemented in production in fall 2017.</p>

<h2>DAIMS Data Dictionary (v1.1)</h2>
<h4> Column Headings</h4>
<p><strong>Grouping</strong>&mdash; Agencies report data in certain groupings.    
  <ul style="margin-bottom:0;">
    <li>File A – Appropriations Account Detail</li>
    <li>File B – Object Class and Program Activity Detail</li>
    <li>File C – Award and Financial Detail</li>
    <li>File D1 – Award and Awardee Attributes (Procurement)</li>
    <li>File D2 – Award and Awardee Attributes (Financial Assistance)</li>
    <li>File E – Additional Awardee Attributes</li>
    <li>File F – Sub-award Attributes</li>
</ul>
</p>
<p>
  <strong>Data Element Label</strong> &mdash; The name of an element in the DATA Act Schema.
</p>
<p>
  <strong>Definition</strong> &mdash; The business definition for the element.
</p>
<p>
  <strong>Use</strong> &mdash; Is this element required?
  <ul style="margin-bottom:0;">
    <li>Required – Element must be present.</li>
    <li>Optional – Element may be included but is not required.</li>
    <li>Conditional per Validation Rule – Element may be needed based on a validation rule.</li>
    <li>Conditional per Award Type – Element may be needed based on the type of award.</li>
    <li>Derived – Element content is obtained from the content of another element. For example, ZIP code is used to derive city and state.</li>
    <li>Extracted – Element is pulled from another source.</li>
  </ul>
</p>
<p>
  <strong>Data Category</strong> &mdash; Some elements are part of a category of elements.
</p>
</div>
<p></p>
<table id="dictTable" class="tablesorter table-bordered table-striped mb-40" style="word-wrap:break-word; table-layout:fixed;">
  <thead>
    <tr>
      <th>Grouping</th>
      <th>Data Element Label</th>
      <th style="width:40%;">Definition</th>
      <th>Use</th>
      <th>Data Category</th>
    </tr>
  </thead>    
  {% for element in site.data.elementsv1_1%}
  <tr>
    <td>{{ element.Grouping }}</td>
    <td>{{ element.DataElementLabel }}</td>
    <!--<td><a href="#C{{ forloop.index | plus:1 }}">{{ element.DAIMSSemanticLabel }}</a></td>-->
    <td>{{ element.Definition }}</td>
    <td>{{ element.Use }}</td>
    <td>{{element.DataCatagory}}</td>
  </tr>{% endfor %}
</table>
