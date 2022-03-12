<script>
  // @ts-nocheck
  import "./datatable.scss"
    import {
      DataTable,
      DataTableHead,
      DataTableRow,
      DataTableCell,
      DataTableBody,
      Button,
      Row, Col, Select,Checkbox
   } from 'svelte-materialify';
  let columns = ["Nisn", "Nama", "Jurusan", "Kelas", "Alamat", "Jenis Kelamin", "Tempat lahir", "Agama", "No tlp", "Email"]
	let data = [
    ["170030299", "john@example.com", "(353) 01 222 3333","john@example.com", "(353) 01 222 3333","john@example.com", "(353) 01 222 3333","(353) 01 222 3333","john@example.com", "(353) 01 222 3333"],
    ["170030299", "john@example.com", "(353) 01 222 3333","john@example.com", "(353) 01 222 3333","john@example.com", "(353) 01 222 3333","(353) 01 222 3333","john@example.com", "(353) 01 222 3333"],
    ["170030299", "john@example.com", "(353) 01 222 3333","john@example.com", "(353) 01 222 3333","john@example.com", "(353) 01 222 3333","(353) 01 222 3333","john@example.com", "(353) 01 222 3333"],
    ["170030299", "john@example.com", "(353) 01 222 3333","john@example.com", "(353) 01 222 3333","john@example.com", "(353) 01 222 3333","(353) 01 222 3333","john@example.com", "(353) 01 222 3333"],
    ["170030299", "john@example.com", "(353) 01 222 3333","john@example.com", "(353) 01 222 3333","john@example.com", "(353) 01 222 3333","(353) 01 222 3333","john@example.com", "(353) 01 222 3333"],
    
  ]

  //Checkall Checkbox


  </script>

  <div class="main-tabel">
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
            {#each data as row}
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
  </div>