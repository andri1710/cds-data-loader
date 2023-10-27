
# [cds-data-loader] DB struct - VCS_DB

<span id="M_BOM_HEADER"> </span>
## M_BOM_HEADER
| Column                | Data Type | Length | Nulls | Description |
| --------------------- | --------- | ------ | ----- | ----------- |
| Factory               | nvarchar  | 4      | :key: |             |
| Matl_Code             | nvarchar  | 40     | :key: |             |
| BOM_Usage             | nvarchar  | 1      | :key: |             |
| Alt_BOM               | nvarchar  | 2      | :key: |             |
| Change_No             | nvarchar  | 12     | :key: |             |
| Valid_From            | date      |        |       |             |
| Base_Uom              | decimal   | 13,3   |       |             |
| Matl_Unit             | nvarchar  | 3      |       |             |
| Insert_By             | nvarchar  | 10     |       |             |
| Insert_At             | datetime  |        |       |             |
| Update_By             | nvarchar  | 10     | true  |             |
| Update_At             | datetime  |        | true  |             |

### 備註：
*This release has no modifications to this part.*



<span id="M_BOM_DETAIL"> </span>
## M_BOM_DETAIL
| Column                | Data Type | Length | Nulls | Description |
| --------------------- | --------- | ------ | ----- | ----------- |
| Factory               | nvarchar  | 4      | :key: |             |
| Matl_Code             | nvarchar  | 40     | :key: |             |
| BOM_Usage             | nvarchar  | 1      | :key: |             |
| Alt_BOM               | nvarchar  | 2      | :key: |             |
| Change_No             | nvarchar  | 12     | :key: |             |
| Item                  | nvarchar  | 4      | :key: |             |
| Item_Matl_Code        | nvarchar  | 40     |       |             |
| Item_Cat              | nvarchar  | 1      |       |             |
| Quantity              | decimal   | 13,5   |       |             |
| Item_Matl_Unit        | nvarchar  | 3      | true  |             |
| Item_Matl_Prov_Ind    | nvarchar  | 1      | true  |             |
| Insert_By             | nvarchar  | 10     |       |             |
| Insert_At             | datetime  |        |       |             |
| Update_By             | nvarchar  | 10     | true  |             |
| Update_At             | datetime  |        | true  |             |

### 備註：
*This release has no modifications to this part.*



<span id="M_MATERIAL"> </span>
## M_MATERIAL
| Column                | Data Type | Length | Nulls | Description |
| --------------------- | --------- | ------ | ----- | ----------- |
| Factory               | nvarchar  | 4      | :key: |             |
| Matl_Code             | nvarchar  | 40     | :key: |             |
| Matl_Generic          | nvarchar  | 40     | true  |             |
| Matl_Name             | nvarchar  | 200    |       |             |
| Matl_Kind             | nvarchar  | 4      |       |             |
| Matl_Group            | nvarchar  | 9      |       |             |
| Matl_Size             | nvarchar  | 32     | true  |             |
| Matl_Unit             | nvarchar  | 3      |       |             |
| Unit_Desc             | nvarchar  | 30     | true  |             |
| Model                 | nvarchar  | 10     | true  |             |
| Model_Name            | varchar   | 40     | true  |             |
| Article               | nvarchar  | 10     | true  |             |
| Gender                | nvarchar  | 1      | true  |             |
| Part_No               | nvarchar  | 10     | true  |             |
| Part_Name             | nvarchar  | 100    | true  |             |
| Matl_Category         | nvarchar  | 2      | true  |             |
| Insert_By             | nvarchar  | 10     |       |             |
| Insert_At             | datetime  |        |       |             |
| Update_By             | nvarchar  | 10     | true  |             |
| Update_At             | datetime  |        | true  |             |
| Material_Spec         | nvarchar  | 1000   | true  |             |
| Issue_Unit            | nvarchar  | 3      | true  |             |
| Issue_Unit_Conversion | decimal   | 13,5   | true  |             |
| Order_Unit            | nvarchar  | 3      | true  |             |
| Order_Unit_Conversion | decimal   | 13,5   | true  |             |

### 備註：
*This release has no modifications to this part.*



<span id="M_SUPPLIER"> </span>
## M_SUPPLIER
| Column                | Data Type | Length | Nulls | Description |
| --------------------- | --------- | ------ | ----- | ----------- |
| Supplier_Code         | nvarchar  | 10     | :key: |             |
| Supplier_Name         | nvarchar  | 160    |       |             |
| Supplier_Abbreviation | nvarchar  | 20     |       |             |
| Uniform_No            | nvarchar  | 20     |       |             |
| Country               | nvarchar  | 3      |       |             |
| Contact_Person        | nvarchar  | 30     |       |             |
| Contract_Type         | nvarchar  | 1      | true  |             |
| Insert_By             | nvarchar  | 10     |       |             |
| Insert_At             | datetime  |        |       |             |
| Update_By             | nvarchar  | 10     | true  |             |
| Update_At             | datetime  |        | true  |             |

### 備註：
*This release has no modifications to this part.*



<span id="M_SUPPLIER_DETAIL"> </span>
## M_SUPPLIER_DETAIL
| Column                | Data Type | Length | Nulls | Description |
| --------------------- | --------- | ------ | ----- | ----------- |
| Supplier_Code         | nvarchar  | 10     | :key: |             |
| Factory               | nvarchar  | 4      | :key: |             |
| Terms_of_Paymen       | nvarchar  | 4      | :key: |             |
| Terms_of_Paymen_Desc  | nvarchar  | 30     |       |             |
| Planning_Group        | nvarchar  | 10     |       |             |
| Planning_Group_Desc   | nvarchar  | 30     |       |             |
| Payment_Methods       | nvarchar  | 10     |       |             |
| Payment_Methods_Desc  | nvarchar  | 30     |       |             |
| Insert_By             | nvarchar  | 10     |       |             |
| Insert_At             | datetime  |        |       |             |
| Update_By             | nvarchar  | 10     | true  |             |
| Update_At             | datetime  |        | true  |             |

### 備註：
*This release has no modifications to this part.*



<span id="T_PURCHASE"> </span>
## T_PURCHASE
| Column                | Data Type | Length | Nulls | Description |
| --------------------- | --------- | ------ | ----- | ----------- |
| Factory               | nvarchar  | 4      | :key: |             |
| Purchase_No           | nvarchar  | 10     | :key: |             |
| Purchase_Date         | date      |        |       |             |
| Supplier_Code         | nvarchar  | 10     |       |             |
| Sales_Order           | nvarchar  | 10     |       |             |
| Purchase_Type         | nvarchar  | 4      |       |             |
| Purchase_Type_Desc    | nvarchar  | 50     |       |             |
| Insert_By             | nvarchar  | 10     |       |             |
| Insert_At             | datetime  |        |       |             |
| Update_By             | nvarchar  | 10     | true  |             |
| Update_At             | datetime  |        | true  |             |
| Mo_Outsource          | nvarchar  | 1      | true  |             |

### 備註：
*This release has no modifications to this part.*



<span id="T_PURCHASE_DETAIL"> </span>
## T_PURCHASE_DETAIL
| Column                | Data Type | Length | Nulls | Description |
| --------------------- | --------- | ------ | ----- | ----------- |
| Factory               | nvarchar  | 4      | :key: |             |
| Purchase_No           | nvarchar  | 10     | :key: |             |
| Item                  | nvarchar  | 5      | :key: |             |
| Matl_Code             | nvarchar  | 40     |       |             |
| Matl_Unit             | nvarchar  | 3      |       |             |
| Unit_Desc             | nvarchar  | 30     |       |             |
| Quantity              | decimal   | 17,4   |       |             |
| Unit_Price            | decimal   | 30,10  |       |             |
| Amount                | decimal   | 30,10  |       |             |
| Currency              | nvarchar  | 20     |       |             |
| Sales_Order           | nvarchar  | 10     |       |             |
| Delivery_Date         | date      |        |       |             |
| Insert_By             | nvarchar  | 10     |       |             |
| Insert_At             | datetime  |        |       |             |
| Update_By             | nvarchar  | 10     | true  |             |
| Update_At             | datetime  |        | true  |             |
| Delete_Status         | nvarchar  | 10     | true  |             |

### 備註：
*This release has no modifications to this part.*



<span id="T_PURCHASE_SUBCONT"> </span>
## T_PURCHASE_SUBCONT
| Column                | Data Type | Length | Nulls | Description |
| --------------------- | --------- | ------ | ----- | ----------- |
| Factory               | nvarchar  | 4      | :key: |             |
| Purchase_No           | nvarchar  | 10     | :key: |             |
| Item                  | nvarchar  | 5      | :key: |             |
| Matl_Code             | nvarchar  | 40     |       |             |
| Matl_Item             | nvarchar  | 4      | :key: |             |
| Quantity              | decimal   | 13,3   |       |             |
| Matl_Unit             | nvarchar  | 3      |       |             |
| Unit_Desc             | nvarchar  | 30     |       |             |
| Supply_Sign           | nvarchar  | 1      |       |             |
| Insert_By             | nvarchar  | 10     |       |             |
| Insert_At             | datetime  |        |       |             |
| Update_By             | nvarchar  | 10     | true  |             |
| Update_At             | datetime  |        | true  |             |

### 備註：
*This release has no modifications to this part.*



<span id="T_PURCHASE_DELIVERY_SCHEDULE"> </span>
## T_PURCHASE_DELIVERY_SCHEDULE
| Column                | Data Type | Length | Nulls | Description |
| --------------------- | --------- | ------ | ----- | ----------- |
| Factory               | nvarchar  | 4      | :key: |             |
| Purchase_No           | nvarchar  | 10     | :key: |             |
| Purchase_Item         | nvarchar  | 5      | :key: |             |
| Sales_Order           | nvarchar  | 10     | :key: |             |
| Sales_Order_Item      | nvarchar  | 6      | :key: |             |
| Purchase_Batch        | decimal   | 17,4   | :key: |             |
| Purchase_Lot_Qty      | decimal   | 17,4   |       |             |
| Firm_Available_Date   | date      |        | true  |             |
| Insert_By             | nvarchar  | 10     |       |             |
| Insert_At             | datetime  |        |       |             |
| Update_By             | nvarchar  | 10     | true  |             |
| Update_At             | datetime  |        | true  |             |

### 備註：
*This release has no modifications to this part.*



<span id="T_INBOUND_DN"> </span>
## T_INBOUND_DN
| Column                | Data Type | Length | Nulls | Description |
| --------------------- | --------- | ------ | ----- | ----------- |
| Factory               | nvarchar  | 4      | :key: |             |
| InboundDN_No          | nvarchar  | 30     | :key: |             |
| Item                  | nvarchar  | 10     | :key: |             |
| Supplier_Code         | nvarchar  | 20     | true  |             |
| Container_No          | nvarchar  | 50     | true  |             |
| Delivery_Date         | date      |        | true  |             |
| Act_Receipt_Date      | date      |        | true  |             |
| Matl_Code             | nvarchar  | 40     | true  |             |
| QtyUnit_ID            | nvarchar  | 10     | true  |             |
| Unit_Desc             | nvarchar  | 50     | true  |             |
| Delivery_Qty          | decimal   | 30,10  | true  |             |
| Purchase_No           | nvarchar  | 50     | true  |             |
| Purchase_Item         | nvarchar  | 10     | true  |             |
| Insert_By             | nvarchar  | 10     |       |             |
| Insert_At             | datetime  |        |       |             |
| Update_By             | nvarchar  | 10     | true  |             |
| Update_At             | datetime  |        | true  |             |

### 備註：
*This release has no modifications to this part.*



<span id="T_PO_BOM"> </span>
## T_PO_BOM
| Column                | Data Type | Length | Nulls | Description |
| --------------------- | --------- | ------ | ----- | ----------- |
| Factory              | nvarchar   | 4      | :key: |             |
| PO_No                | nvarchar   | 35     | :key: |             |
| Matl_Code            | nvarchar   | 40     | :key: |             |
| Matl_Desc            | nvarchar   | 40     |       |             |
| Consumption_Qty      | decimal    | 13,5   |       |             |
| QtyUnit_ID           | nvarchar   | 3      |       |             |
| QtyUnit_Desc         | nvarchar   | 10     |       |             |
| Sales_Order          | nvarchar   | 10     |       |             |
| Insert_By            | nvarchar   | 10     |       |             |
| Insert_At            | datetime   |        |       |             |
| Update_By            | nvarchar   | 10     | true  |             |
| Update_At            | datetime   |        | true  |             |

### 備註：
*This release has no modifications to this part.*



<span id="T_PO_BOM_DETAIL"> </span>
## T_PO_BOM_DETAIL
| Column                | Data Type | Length | Nulls | Description |
| --------------------- | --------- | ------ | ----- | ----------- |
| Factory               | nvarchar  | 4      | :key: |             |
| PO_No                 | nvarchar  | 35     | :key: |             |
| Matl_Code             | nvarchar  | 40     | :key: |             |
| Item                  | nvarchar  | 4      | :key: |             |
| Matl_Desc             | nvarchar  | 40     | true  |             |
| Item_Material_No      | nvarchar  | 40     | true  |             |
| Item_Material_Name    | nvarchar  | 40     | true  |             |
| AVG_Consumption_Qty   | decimal   | 13,5   | true  |             |
| Consumption_Qty       | decimal   | 13,5   | true  |             |
| Unit_ID               | nvarchar  | 3      | true  |             |
| Unit_Desc             | nvarchar  | 10     | true  |             |
| Insert_By             | nvarchar  | 10     |       |             |
| Insert_At             | datetime  |        |       |             |
| Update_By             | nvarchar  | 10     | true  |             |
| Update_At             | datetime  |        | true  |             |

### 備註：
*This release has no modifications to this part.*



<span id="T_SHIPMENT"> </span>
## T_SHIPMENT
| Column                | Data Type | Length | Nulls | Description |
| --------------------- | --------- | ------ | ----- | ----------- |
| Factory               | nvarchar  | 4      | :key: |             |
| Shipment_No           | nvarchar  | 10     | :key: |             |
| Customer_ID           | nvarchar  | 10     |       |             |
| PODD                  | date      |        |       |             |
| FGOut_ActualDate      | date      |        | true  |             |
| Delivery_Mode         | nvarchar  | 2      |       |             |
| Delivery_Mode_Desc    | nvarchar  | 20     |       |             |
| Desti_ID              | nvarchar  | 10     |       |             |
| Ship_Way_Desc         | nvarchar  | 20     |       |             |
| Forwarder_Name        | nvarchar  | 80     | true  |             |
| Service_ID            | nvarchar  | 15     |       |             |
| Insert_By             | nvarchar  | 10     |       |             |
| Insert_At             | datetime  |        |       |             |
| Update_By             | nvarchar  | 10     | true  |             |
| Update_At             | datetime  |        | true  |             |

### 備註：
*This release has no modifications to this part.*



<span id="T_SHIPMENT_DETAIL"> </span>
## T_SHIPMENT_DETAIL
| Column                | Data Type | Length | Nulls | Description |
| --------------------- | --------- | ------ | ----- | ----------- |
| Factory               | nvarchar  | 4      | :key: |             |
| Shipment_No           | nvarchar  | 10     | :key: |             |
| Item                  | nvarchar  | 6      | :key: |             |
| Sales_Order           | nvarchar  | 10     |       |             |
| Matl_Code_WithSize    | nvarchar  | 40     |       |             |
| Order_Size            | nvarchar  | 4      | true  |             |
| Shipment_Qty          | decimal   | 15,3   |       |             |
| QtyUnit_ID            | nvarchar  | 10     |       |             |
| Insert_By             | nvarchar  | 10     |       |             |
| Insert_At             | datetime  |        |       |             |
| Update_By             | nvarchar  | 10     | true  |             |
| Update_At             | datetime  |        | true  |             |

### 備註：
*This release has no modifications to this part.*



<span id="T_SALES_ORDER"> </span>
## T_SALES_ORDER
| Column                | Data Type | Length | Nulls | Description |
| --------------------- | --------- | ------ | ----- | ----------- |
| Factory               | nvarchar  | 4      | :key: |             |
| Sales_Order           | nvarchar  | 10     | :key: |             |
| PO_No                 | nvarchar  | 35     | :key: |             |
| PODD                  | date      |        | true  |             |
| POSDD                 | date      |        | true  |             |
| Receive_Date          | date      |        | true  |             |
| Matl_Code             | nvarchar  | 40     | true  |             |
| Order_Type            | nvarchar  | 4      | true  |             |
| Order_Type_Desc       | nvarchar  | 20     | true  |             |
| Customer_Code         | nvarchar  | 10     | true  |             |
| Customer_Name         | nvarchar  | 80     | true  |             |
| Desti_Code            | nvarchar  | 10     | true  |             |
| Desti_Name            | nvarchar  | 80     | true  |             |
| Desti_Country_Name    | nvarchar  | 15     | true  |             |
| Desti_Address         | nvarchar  | 200    | true  |             |
| Insert_By             | nvarchar  | 10     |       |             |
| Insert_At             | datetime  |        |       |             |
| Update_By             | nvarchar  | 10     | true  |             |
| Update_At             | datetime  |        | true  |             |

### 備註：
*This release has no modifications to this part.*



<span id="T_SALES_ORDER_DETAIL"> </span>
## T_SALES_ORDER_DETAIL
| Column                | Data Type | Length | Nulls | Description |
| --------------------- | --------- | ------ | ----- | ----------- |
| Factory               | nvarchar  | 4      | :key: |             |
| Sales_Order           | nvarchar  | 10     | :key: |             |
| Item                  | nvarchar  | 6      | :key: |             |
| Matl_Code_WithSize    | nvarchar  | 40     |       |             |
| Order_Size            | nvarchar  | 4      |       |             |
| Order_Quantity        | decimal   | 15,3   |       |             |
| Order_Quantity_Unit   | nvarchar  | 3      |       |             |
| Unit_Price            | decimal   | 15,5   |       |             |
| Currency              | nvarchar  | 10     |       |             |
| Insert_By             | nvarchar  | 10     |       |             |
| Insert_At             | datetime  |        |       |             |
| Update_By             | nvarchar  | 10     | true  |             |
| Update_At             | datetime  |        | true  |             |

### 備註：
*This release has no modifications to this part.*



<span id="T_CARTON_ARRANGE_HEADER"> </span>
## T_CARTON_ARRANGE_HEADER
| Column                | Data Type | Length | Nulls | Description |
| --------------------- | --------- | ------ | ----- | ----------- |
| Factory               | nvarchar  | 4      | :key: |             |
| Sales_Order           | nvarchar  | 35     | :key: |             |
| CartonArrange_Seq     | nvarchar  | 10     | :key: |             |
| Po_Size               | nvarchar  | 20     | true  |             |
| Cust_Size             | nvarchar  | 10     | true  |             |
| Matl_Code             | nvarchar  | 40     | true  |             |
| In_Carton_Qty         | decimal   | 30,10  | true  |             |
| Carton_Cnt            | int       |        | true  |             |
| CartonNo_First        | int       |        | true  |             |
| CartonNo_Last         | int       |        | true  |             |
| Weight_Net            | decimal   | 30,10  | true  |             |
| Weight_Gross          | decimal   | 30,10  | true  |             |
| CBM                   | decimal   | 30,10  | true  |             |
| Packing_Type          | nvarchar  | 10     | true  |             |
| Packing_Contents      | nvarchar  | 200    | true  |             |
| Insert_By             | nvarchar  | 10     |       |             |
| Insert_At             | datetime  |        |       |             |
| Update_By             | nvarchar  | 10     | true  |             |
| Update_At             | datetime  |        | true  |             |

### 備註：
*This release has no modifications to this part.*



<span id="T_CARTON_ARRANGE_DETAIL"> </span>
## T_CARTON_ARRANGE_DETAIL
| Column                | Data Type | Length | Nulls | Description |
| --------------------- | --------- | ------ | ----- | ----------- |
| Factory               | nvarchar  | 4      | :key: |             |
| Sales_Order           | nvarchar  | 35     | :key: |             |
| Matl_Code             | nvarchar  | 40     |       |             |
| Carton_No             | int       |        | :key: |             |
| Po_Size               | nvarchar  | 20     | :key: |             |
| Cust_Size             | nvarchar  | 10     | :key: |             |
| In_Carton_Qty         | decimal   | 30,10  |       |             |
| Insert_By             | nvarchar  | 10     |       |             |
| Insert_At             | datetime  |        |       |             |
| Update_By             | nvarchar  | 10     | true  |             |
| Update_At             | datetime  |        | true  |             |

### 備註：
*This release has no modifications to this part.*



<span id="T_FG_WRITE_OFF_RESULT"> </span>
## T_FG_WRITE_OFF_RESULT
| Column                | Data Type | Length | Nulls | Description |
| --------------------- | --------- | ------ | ----- | ----------- |
| Factory               | nvarchar  | 4      | :key: |             |
| Sales_Order           | nvarchar  | 10     | :key: |             |
| Sales_Order_New       | nvarchar  | 10     | :key: |             |
| PO_No                 | nvarchar  | 35     | true  |             |
| PO_No_New             | nvarchar  | 35     | true  |             |
| Offset_Qty            | decimal   | 15,5   | true  |             |
| Deletion_Flag         | nvarchar  | 5      | true  |             |
| Insert_By             | nvarchar  | 10     |       |             |
| Insert_At             | datetime  |        |       |             |
| Update_By             | nvarchar  | 10     | true  |             |
| Update_At             | datetime  |        | true  |             |

### 備註：
*This release has no modifications to this part.*



<span id="EXAMPLE_TABLE_NAME"> </span>
## EXAMPLE_TABLE_NAME
| Column                | Data Type | Length | Nulls | Description |
| --------------------- | --------- | ------ | ----- | ----------- |

### 備註：
*This release has no modifications to this part.*

###### tags: `cds-data-loader`
