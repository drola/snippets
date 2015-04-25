Bootstrap related snippets
==========================

Equal height columns
--------------------

    /* Make equal height with table styles */

    @media (min-width: 768px) {
      .table-row {
        display: table;
        table-layout: fixed;
      }

      .table-row [class^="col-"] {
        display: table-cell;
        float: none;
      }
    }


    <div class="row table-row">
      <div class="col-md-4">This column is super duper long and there for it'll appear taller than the rest on devices larger than 768px. More blah blah blah blah blah blah blah blah blah blah blah blah  blah blah herp derp.</div>
      <div class="col-md-4">.col-md-4</div>
      <div class="col-md-4">.col-md-4</div>
    </div>


>  [https://jsbin.com/qoxofa/1/](https://jsbin.com/qoxofa/1/)

