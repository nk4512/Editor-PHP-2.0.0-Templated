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

```
Render below 
        return $this->render('my_grooming_space/datatables_template.html.twig',[
            'table_create_type' => 'POST',
            'table_create_target' => 'api/create_table',
            'table_edit_type' => 'POST',
            'table_edit_target' => 'edittarget',
            'table_remove_type' => 'POST',
            'table_delete_target' => 'deletetarget',
            'table_data_source' => '/api/testData/data',
            'table_name' => 'Port to Fiber Mapping',
            'table_id' => 'hc_mapping',
            'table_data' => $table_data,
            'row_id_value' => 'id',
            'enable_create' => false,
            'enable_edit' => true,
            'enable_remove' => false,
        ]);
```