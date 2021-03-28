# Editor-PHP-2.0.0-Templated

Table creation using a template and generator

V1.0
-Initial build




#Data structure to build the table columns
```
$table_data = array(
            '0' => array(
                'key' => 'key',
                'width' => 'width of the column',
                'name' => 'Column Name',
                'class' => 'Any text class compatible with datatables'
            )
        );
```

enable_create/edit/remove
-Set 'true' to enable the respective buttons

```
Render below 
        return $this->render('my_grooming_space/datatables_template.html.twig',[
            'table_create_type' => 'POST/PUT/GET/DELETE',
            'table_create_target' => 'api/create_target',
            'table_edit_type' => 'POST/PUT/GET/DELETE',
            'table_edit_target' => 'api/edit_target',
            'table_remove_type' => 'POST/PUT/GET/DELETE',
            'table_delete_target' => 'api/delete_target',
            'table_data_source' => '/api/testData/data',
            'table_name' => 'Table Name',
            'table_id' => 'table_id',
            'table_data' => $table_data,
            'row_id_value' => 'Row the table should use as an ID. Example row_id',
            'enable_create' => true/false,
            'enable_edit' => true/false,
            'enable_remove' => false/false,
        ]);
```