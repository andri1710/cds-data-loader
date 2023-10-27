

# [cds-data-loader] DB struct - PLM IMDB

<span id="SAP_BOM_Header"> </span>
## SAP_BOM_Header
| Column      | Data Type | Length | Nulls | Description |
| ----------- | --------- | ------ | ----- | ----------- |
| SID         | nvarchar  | 20     | :key: |             |
| Material_No | nvarchar  | 40     | :key: |             |
| Factory_ID  | nvarchar  | 4      | :key: |             |
| BOM_Usage   | nvarchar  | 1      | :key: |             |
| Alt_BOM     | nvarchar  | 2      | :key: |             |
| Change_No   | nvarchar  | 12     | :key: |             |
| Valid_From  | nvarchar  | 8      |       |             |
| Base_Uom    | decimal   | 13,3   |       |             |
| Unit        | nvarchar  | 3      |       |             |
| Biz_Flag    | nchar     | 1      | true  |             |
| Biz_Tflag   | nchar     | 1      | true  |             |
| Biz_P_Time  | datetime  |        | true  |             |
| Biz_Y_Time  | datetime  |        | true  |             |
| Biz_Time    | datetime  |        | true  |             |

### 備註：
*This release has no modifications to this part.*


<span id="SAP_BOM_Detail"> </span>
## SAP_BOM_Detail
| Column      | Data Type | Length | Nulls | Description |
| ----------- | --------- | ------ | ----- | ----------- |
| SID         | nvarchar  | 20     | :key: |             |
| Material_No | nvarchar  | 40     | :key: |             |
| Factory_ID  | nvarchar  | 4      | :key: |             |
| BOM_Usage   | nvarchar  | 1      | :key: |             |
| Alt_BOM     | nvarchar  | 2      | :key: |             |
| Change_No   | nvarchar  | 12     | :key: |             |
| Item        | nvarchar  | 4      | :key: |             |
| Component   | nvarchar  | 40     |       |             |
| Item_Cat    | nvarchar  | 1      |       |             |
| Quantity    | decimal   | 13,5   |       |             |
| Unit        | nvarchar  | 3      | true  |             |
| Mat_Prov_Ind| nvarchar  | 1      | true  |             |
| Biz_Flag    | nchar     | 1      | true  |             |
| Biz_Tflag   | nchar     | 1      | true  |             |
| Biz_P_Time  | datetime  |        | true  |             |
| Biz_Y_Time  | datetime  |        | true  |             |
| Biz_Time    | datetime  |        | true  |             |

### 備註：
*This release has no modifications to this part.*

###### tags: `cds-data-loader`
