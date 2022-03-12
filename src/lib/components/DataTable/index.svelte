<main class="main-tabel">
  <div class="content-tabel">  
      <DataTable>
        <DataTableHead>
          <DataTableRow>
            {#each columns as column}
            <DataTableCell>{column}</DataTableCell>
            {/each}
          </DataTableRow>
        </DataTableHead>
        <DataTableBody>
          {#each datas as row}
          <DataTableRow>
              {#each row as cell}
                <DataTableCell>
                  {cell}
                </DataTableCell>
                {/each}
          </DataTableRow>
          {/each}
        </DataTableBody>
      </DataTable>
  </div>
</main>

<script>
  import "./datatable.scss"
  import {
    DataTable,
    DataTableHead,
    DataTableRow,
    DataTableCell,
    DataTableBody,
  } from 'svelte-materialify';
  export let columns;
  export let datas;
</script>