
# [cds-data-loader] DB struct - SAP IMDB

<span id="All_Material"> </span>
## All_Material
| Column           | Data Type | Length | Nulls | Description |
| ---------------- | --------- | ------ | ----- | ----------- |
| SID              | nvarchar  | 30     | :key: |             |
| Factory_ID       | nvarchar  | 20     | :key: |             |
| Factory3         | nvarchar  | 200    | true  |             |
| MaterialNO       | nvarchar  | 200    | :key: |             |
| Generic_Material | nvarchar  | 200    | true  |             |
| Material_Name    | nvarchar  | 200    | true  |             |
| Material_Spec    | nvarchar  | 2000   | true  |             |
| Unit             | nvarchar  | 200    | true  |             |
| Unit_Desc        | nvarchar  | 200    | true  |             |
| Material_Type    | nvarchar  | 200    | true  |             |
| Category         | nvarchar  | 200    | true  |             |
| Special_Category | nvarchar  | 200    | true  |             |
| Plan_Period      | nvarchar  | 200    | true  |             |
| Purchase_Group   | nvarchar  | 200    | true  |             |
| Process_Type     | nvarchar  | 200    | true  |             |
| Model_NO         | nvarchar  | 200    | true  |             |
| Article          | nvarchar  | 200    | true  |             |
| Model_Name       | nvarchar  | 200    | true  |             |
| Article_Name     | nvarchar  | 200    | true  |             |
| Estimation_Method| nvarchar  | 200    | true  |             |
| Main_Class       | nvarchar  | 200    | true  |             |
| Middle_Class     | nvarchar  | 200    | true  |             |
| Gender           | nvarchar  | 200    | true  |             |
| Material_Size    | nvarchar  | 200    | true  |             |
| Length           | numeric   | 13,5   | true  |             |
| Width            | numeric   | 13,5   | true  |             |
| High             | numeric   | 13,5   | true  |             |
| Carton_Unit      | nvarchar  | 200    | true  |             |
| Part_NO          | nvarchar  | 200    | true  |             |
| Part_Name        | nvarchar  | 200    | true  |             |
| Code             | nvarchar  | 200    | true  |             |
| Material_Category| nchar     | 2      | true  |             |
| CreateTime       | nvarchar  | 200    | true  |             |
| CreateUser       | nvarchar  | 200    | true  |             |
| Trans_Msg        | nvarchar  | 200    | true  |             |
| Update_By        | varchar   | 50     | true  |             |
| Update_Time      | datetime  |        | true  |             |
| Biz_Flag         | char      | 1      | true  |             |
| Biz_Tflag        | char      | 1      | true  |             |
| Biz_P_Time       | datetime  |        | true  |             |
| Biz_Y_Time       | datetime  |        | true  |             |
| Biz_Time         | datetime  |        | true  |             |
| Brand_Category   | nvarchar  | 255    | true  |             |
| Order_Unit       | nvarchar  | 3      | true  |             |
| Order_Unit_Conversion| numeric | 13,5 | true  |             |
| Issue_Unit       | nvarchar  | 3      | true  |             |
| Issue_Unit_Conversion| numeric | 13,5 | true  |             |
| Min_Withdrawn_Qty| numeric   | 13,5   | true  |             |

### 備註：
*This release has no modifications to this part.*


<span id="All_Supplier"> </span>
## All_Supplier
| Column                | Data Type | Length | Nulls | Description |
| --------------------- | --------- | ------ | ----- | ----------- |
| SID                   | nvarchar  | 30     | :key: |             |
| Factory_ID            | nvarchar  | 20     |       |             |
| Supplier_Code         | nvarchar  | 100    | :key: |             |
| Supplier_Name         | nvarchar  | 100    | true  |             |
| Supplier              | nvarchar  | 100    |       |             |
| Uniform_No            | nvarchar  | 100    | true  |             |
| Country_Code          | nvarchar  | 100    | true  |             |
| Contact               | nvarchar  | 100    | true  |             |
| CreateUser            | nvarchar  | 200    | true  |             |
| CreateTime            | nvarchar  | 200    | true  |             |
| Trans_Msg             | nvarchar  | 200    | true  |             |
| Update_By             | varchar   | 50     | true  |             |
| Update_Time           | datetime  |        | true  |             |
| Biz_Flag              | char      | 1      | true  |             |
| Biz_Tflag             | char      | 1      | true  |             |
| Biz_P_Time            | datetime  |        | true  |             |
| Biz_Y_Time            | datetime  |        | true  |             |
| Biz_Time              | datetime  |        | true  |             |
| Source                | nvarchar  | 4      | true  |             |

### 備註：
*This release has no modifications to this part.*


<span id="All_Supplier_Detail"> </span>
## All_Supplier_Detail
| Column                | Data Type | Length | Nulls | Description |
| --------------------- | --------- | ------ | ----- | ----------- |
| SID                   | nvarchar  | 30     | :key: |             |
| Supplier_Code         | nvarchar  | 100    | :key: |             |
| Company_ID            | nvarchar  | 200    | :key: |             |
| Terms_of_Payment      | nvarchar  | 10     | true  |             |
| Terms_of_Payment_Desc | nvarchar  | 50     | true  |             |
| Planning_Group        | nvarchar  | 10     | true  |             |
| Planning_Group_Desc   | nvarchar  | 50     | true  |             |
| Payment_Methods       | nvarchar  | 10     | true  |             |
| Payment_Methods_Desc  | nvarchar  | 50     | true  |             |
| Update_By             | varchar   | 50     | true  |             |
| Update_Time           | datetime  |        | true  |             |
| Biz_Flag              | char      | 1      | true  |             |
| Biz_Tflag             | char      | 1      | true  |             |
| Biz_P_Time            | datetime  |        | true  |             |
| Biz_Y_Time            | datetime  |        | true  |             |
| Biz_Time              | datetime  |        | true  |             |

### 備註：
*This release has no modifications to this part.*


<span id="All_Purchase_Order_Header"> </span>
## All_Purchase_Order_Header
| Column                | Data Type | Length | Nulls | Description |
| --------------------- | --------- | ------ | ----- | ----------- |
| SID                   | nvarchar  | 60     | :key: |             |
| Factory_ID            | nvarchar  | 60     | :key: |             |
| Factory3              | nvarchar  | 60     | :key: |             |
| Purchase_Order_Header | nvarchar  | 60     | :key: |             |
| Po_Create_Time        | nvarchar  | 8      |       |             |
| Supplier_ID           | nvarchar  | 60     |       |             |
| Customer_Order_ID     | nvarchar  | 60     |       |             |
| Po_Type               | nvarchar  | 60     |       |             |
| Po_Type_Name          | nvarchar  | 60     | true  |             |
| Op_Outsource          | nvarchar  | 60     | true  |             |
| Mo_Outsource          | nvarchar  | 360    | true  |             |
| Biz_Flag              | char      | 1      | true  |             |
| Biz_Tflag             | char      | 1      | true  |             |
| Biz_P_Time            | datetime  |        | true  |             |
| Biz_Y_Time            | datetime  |        | true  |             |
| Biz_Time              | datetime  |        | true  |             |

### 備註：
*This release has no modifications to this part.*



<span id="All_Purchase_Order_Item"> </span>
## All_Purchase_Order_Item
| Column                | Data Type | Length | Nulls | Description |
| --------------------- | --------- | ------ | ----- | ----------- |
| SID                   | nvarchar  | 60     | :key: |             |
| Factory_ID            | nvarchar  | 60     | :key: |             |
| Factory3              | nvarchar  | 60     | :key: |             |
| Purchase_Order_Header | nvarchar  | 60     | :key: |             |
| Purchase_Order_Line   | nvarchar  | 60     | :key: |             |
| Sales_Order_Header    | nvarchar  | 60     |       |             |
| Sales_Order_Line      | nvarchar  | 60     | true  |             |
| Mfg_Order_ID          | nvarchar  | 60     | true  |             |
| Route_ID              | nvarchar  | 60     | true  |             |
| Material_No           | nvarchar  | 60     | :key: |             |
| Unit_ID               | nvarchar  | 60     |       |             |
| Qtyunit_Desc          | nvarchar  | 60     | true  |             |
| Purchase_Qty          | numeric   | 17,4   |       |             |
| Stocked_Qty           | numeric   | 17,4   |       |             |
| Net_Unitprice         | decimal   | 30,10  | true  |             |
| Net_Amount            | decimal   | 30,10  | true  |             |
| Firm_Available_Date   | nvarchar  | 8      |       |             |
| Delete_Status         | nvarchar  | 60     | true  |             |
| Delivery_Status       | nvarchar  | 60     | true  |             |
| Biz_Flag              | char      | 1      | true  |             |
| Biz_Tflag             | char      | 1      | true  |             |
| Biz_P_Time            | datetime  |        | true  |             |
| Biz_Y_Time            | datetime  |        | true  |             |
| Biz_Time              | datetime  |        | true  |             |
| Currency              | nvarchar  | 20     |       |             |

### 備註：
*This release has no modifications to this part.*



<span id="All_Component"> </span>
## All_Component
| Column                    | Data Type | Length | Nulls | Description |
| ------------------------- | --------- | ------ | ----- | ----------- |
| SID                       | nvarchar  | 60     | :key: |             |
| Factory_ID                | nvarchar  | 60     | :key: |             |
| Factory3                  | nvarchar  | 60     | :key: |             |
| Purchase_Order_Header     | nvarchar  | 60     | :key: |             |
| Purchase_Order_Line       | nvarchar  | 60     | :key: |             |
| Sequence_Txt              | nvarchar  | 60     | :key: |             |
| Input_Part_ID             | nvarchar  | 60     |       |             |
| Input_Part_ID_Demand_Qty  | numeric   | 17,4   |       |             |
| Input_Part_ID_Release_Qty | numeric   | 17,4   |       |             |
| Unit_ID                   | nvarchar  | 60     |       |             |
| Qtyunit_Desc              | nvarchar  | 60     | true  |             |
| Supplier_Provision        | nvarchar  | 1      |       |             |
| Biz_Flag                  | char      | 1      | true  |             |
| Biz_Tflag                 | char      | 1      | true  |             |
| Biz_P_Time                | datetime  |        | true  |             |
| Biz_Y_Time                | datetime  |        | true  |             |
| Biz_Time                  | datetime  |        | true  |             |

### 備註：
*This release has no modifications to this part.*



<span id="All_Delivery_Schedule"> </span>
## All_Delivery_Schedule
| Column                | Data Type | Length | Nulls | Description |
| --------------------- | --------- | ------ | ----- | ----------- |
| SID                   | nvarchar  | 60     | :key: |             |
| Factory_ID            | nvarchar  | 60     | :key: |             |
| Factory3              | nvarchar  | 60     | :key: |             |
| Purchase_Order_Header | nvarchar  | 60     | :key: |             |
| Purchase_Order_Line   | nvarchar  | 60     | :key: |             |
| Sales_Order_Header    | nvarchar  | 60     | :key: |             |
| Sales_Order_Line      | nvarchar  | 60     | :key: |             |
| Purchase_Order_Batch  | numeric   | 17,4   | :key: |             |
| Purchase_Lot_Qty      | numeric   | 17,4   |       |             |
| Firm_Available_Date   | nvarchar  | 8      | true  |             |
| Biz_Flag              | char      | 1      | true  |             |
| Biz_Tflag             | char      | 1      | true  |             |
| Biz_P_Time            | datetime  |        | true  |             |
| Biz_Y_Time            | datetime  |        | true  |             |
| Biz_Time              | datetime  |        | true  |             |

### 備註：
*This release has no modifications to this part.*



<span id="CDS_Inbound_DN"> </span>
## CDS_Inbound_DN
| Column                | Data Type | Length | Nulls | Description |
| --------------------- | --------- | ------ | ----- | ----------- |
| SID                   | nvarchar  | 30     | :key: |             |
| Factory_ID            | varchar   | 10     | :key: |             |
| InboundDN_No          | varchar   | 30     | :key: |             |
| Item_Seq              | varchar   | 10     | :key: |             |
| Supplier_ID           | nvarchar  | 20     | true  |             |
| Container_No          | nvarchar  | 50     | true  |             |
| Delivery_Date         | nvarchar  | 8      | true  |             |
| Act_Receipt_Date      | nvarchar  | 8      | true  |             |
| Material_No           | varchar   | 40     | true  |             |
| Qty_Unit_ID           | nvarchar  | 10     | true  |             |
| Qty_Unit_Desc         | nvarchar  | 50     | true  |             |
| Delivery_Qty          | decimal   | 30,10  | true  |             |
| Purchase_No           | nvarchar  | 50     | true  |             |
| Purchase_Item_Seq     | varchar   | 10     | true  |             |
| Update_By             | varchar   | 50     | true  |             |
| Update_Time           | datetime  |        | true  |             |
| Biz_Flag              | char      | 1      | true  |             |
| Biz_Tflag             | char      | 1      | true  |             |
| Biz_P_Time            | datetime  |        | true  |             |
| Biz_Y_Time            | datetime  |        | true  |             |
| Biz_Time              | datetime  |        | true  |             |
| ITM_VYGID             | nvarchar  | 35     | true  |             |

### 備註：
*This release has no modifications to this part.*



<span id="CDS_Receipt_Invoice_Header"> </span>
## CDS_Receipt_Invoice_Header
| Column                | Data Type | Length | Nulls | Description |
| --------------------- | --------- | ------ | ----- | ----------- |
| SID                   | nvarchar  | 30     | :key: |             |
| Inv_Doc_No            | nvarchar  | 50     | :key: |             |
| Inv_Doc_Year          | char      | 4      | :key: |             |
| Factory_ID            | varchar   | 10     | :key: |             |
| Inv_Date              | nvarchar  | 8      | true  |             |
| Posting_Date          | nvarchar  | 8      | true  |             |
| Inv_Amount            | decimal   | 30,10  | true  |             |
| Tax_Amount            | decimal   | 30,10  | true  |             |
| Tax_Code              | nvarchar  | 10     | true  |             |
| Tax_Code_Desc         | nvarchar  | 50     | true  |             |
| Invoice_No            | nvarchar  | 50     | true  |             |
| Currency              | nvarchar  | 20     | true  |             |
| Supplier_ID           | nvarchar  | 20     | true  |             |
| Payment_Baseline_Date | nvarchar  | 8      | true  |             |
| Payment_Due_Date      | nvarchar  | 8      | true  |             |
| Payment_Terms         | nvarchar  | 50     | true  |             |
| Curr_Exchange_Rate    | decimal   | 30,10  | true  |             |
| Update_By             | varchar   | 50     | true  |             |
| Update_Time           | datetime  |        | true  |             |
| Biz_Flag              | char      | 1      | true  |             |
| Biz_Tflag             | char      | 1      | true  |             |
| Biz_P_Time            | datetime  |        | true  |             |
| Biz_Y_Time            | datetime  |        | true  |             |
| Biz_Time              | datetime  |        | true  |             |

### 備註：
*This release has no modifications to this part.*



<span id="CDS_Receipt_Invoice_Detail"> </span>
## CDS_Receipt_Invoice_Detail
| Column                | Data Type | Length | Nulls | Description |
| --------------------- | --------- | ------ | ----- | ----------- |
| SID                   | nvarchar  | 30     | :key: |             |
| Inv_Doc_No            | nvarchar  | 50     | :key: |             |
| Inv_Doc_Year          | char      | 4      | :key: |             |
| Item_Seq              | varchar   | 10     | :key: |             |
| Purchase_No           | nvarchar  | 50     | true  |             |
| Purchase_Item_Seq     | varchar   | 10     | true  |             |
| Material_No           | varchar   | 40     | true  |             |
| Factory_ID            | varchar   | 10     | true  |             |
| Amount                | decimal   | 30,10  | true  |             |
| Add_Deduct_Type       | char      | 1      | true  |             |
| Quantity              | decimal   | 30,10  | true  |             |
| Qty_Unit_ID           | nvarchar  | 10     | true  |             |
| Qty_Unit_Desc         | nvarchar  | 50     | true  |             |
| Receipt_Doc_Year      | char      | 4      | true  |             |
| Receipt_Doc_No        | nvarchar  | 50     | true  |             |
| Receipt_Item_Seq      | varchar   | 10     | true  |             |
| Update_By             | varchar   | 50     | true  |             |
| Update_Time           | datetime  |        | true  |             |
| Biz_Flag              | char      | 1      | true  |             |
| Biz_Tflag             | char      | 1      | true  |             |
| Biz_P_Time            | datetime  |        | true  |             |
| Biz_Y_Time            | datetime  |        | true  |             |
| Biz_Time              | datetime  |        | true  |             |

### 備註：
*This release has no modifications to this part.*



<span id="CDS_Receipt_Invoice_Account"> </span>
## CDS_Receipt_Invoice_Account
| Column                | Data Type | Length | Nulls | Description |
| --------------------- | --------- | ------ | ----- | ----------- |
| SID                   | nvarchar  | 30     | :key: |             |
| Inv_Doc_No            | nvarchar  | 50     | :key: |             |
| Inv_Doc_Year          | char      | 4      | :key: |             |
| Item_Seq              | varchar   | 10     | :key: |             |
| Accounting_Acct       | nvarchar  | 20     | true  |             |
| Debit_Credit_Type     | char      | 1      | true  |             |
| Amount                | decimal   | 30,10  | true  |             |
| Tax_Code              | nvarchar  | 10     | true  |             |
| Tax_Code_Desc         | nvarchar  | 50     | true  |             |
| Factory_ID            | varchar   | 10     | true  |             |
| Update_By             | varchar   | 50     | true  |             |
| Update_Time           | datetime  |        | true  |             |
| Biz_Flag              | char      | 1      | true  |             |
| Biz_Tflag             | char      | 1      | true  |             |
| Biz_P_Time            | datetime  |        | true  |             |
| Biz_Y_Time            | datetime  |        | true  |             |
| Biz_Time              | datetime  |        | true  |             |

### 備註：
*This release has no modifications to this part.*



<span id="CDS_Stock_At_Factory"> </span>
## CDS_Stock_At_Factory
| Column                | Data Type | Length | Nulls | Description |
| --------------------- | --------- | ------ | ----- | ----------- |
| SID                   | nvarchar  | 30     | :key: |             |
| Factory_ID            | varchar   | 10     | :key: |             |
| Material_No_G         | varchar   | 40     | true  |             |
| Material_No_V         | varchar   | 40     | :key: |             |
| Storage_Location      | nvarchar  | 10     | :key: |             |
| Unrestricted_Qty      | decimal   | 30,10  | true  |             |
| On_The_Way_Qty        | decimal   | 30,10  | true  |             |
| Quality_Checking_Qty  | decimal   | 30,10  | true  |             |
| Qty_Unit_ID           | nvarchar  | 10     | true  |             |
| Qty_Unit_Desc         | nvarchar  | 50     | true  |             |
| Update_By             | varchar   | 50     | true  |             |
| Update_Time           | datetime  |        | true  |             |
| Biz_Flag              | char      | 1      | true  |             |
| Biz_Tflag             | char      | 1      | true  |             |
| Biz_P_Time            | datetime  |        | true  |             |
| Biz_Y_Time            | datetime  |        | true  |             |
| Biz_Time              | datetime  |        | true  |             |

### 備註：
*This release has no modifications to this part.*



<span id="CDS_Stock_At_Supplier"> </span>
## CDS_Stock_At_Supplier
| Column                | Data Type | Length | Nulls | Description |
| --------------------- | --------- | ------ | ----- | ----------- |
| SID                   | nvarchar  | 30     | :key: |             |
| Factory_ID            | varchar   | 10     | :key: |             |
| Material_No           | varchar   | 40     | :key: |             |
| Supplier_ID           | nvarchar  | 20     | :key: |             |
| Quantity              | decimal   | 30,10  | true  |             |
| Qty_Unit_ID           | nvarchar  | 10     | true  |             |
| Qty_Unit_Desc         | nvarchar  | 50     | true  |             |
| Update_By             | varchar   | 50     | true  |             |
| Update_Time           | datetime  |        | true  |             |
| Biz_Flag              | char      | 1      | true  |             |
| Biz_Tflag             | char      | 1      | true  |             |
| Biz_P_Time            | datetime  |        | true  |             |
| Biz_Y_Time            | datetime  |        | true  |             |
| Biz_Time              | datetime  |        | true  |             |

### 備註：
*This release has no modifications to this part.*



<span id="CDS_SO_Stock"> </span>
## CDS_SO_Stock
| Column                | Data Type | Length | Nulls | Description |
| --------------------- | --------- | ------ | ----- | ----------- |
| SID                   | nvarchar  | 30     | :key: |             |
| Factory_ID            | varchar   | 10     | :key: |             |
| Material_No           | varchar   | 40     | :key: |             |
| Storage_Location      | nvarchar  | 10     | :key: |             |
| SO_No                 | varchar   | 35     | :key: |             |
| SO_Item_Seq           | varchar   | 10     | :key: |             |
| Quantity              | decimal   | 30,10  | true  |             |
| Qty_Unit_ID           | nvarchar  | 10     | true  |             |
| Qty_Unit_Desc         | nvarchar  | 50     | true  |             |
| Update_By             | varchar   | 50     | true  |             |
| Update_Time           | datetime  |        | true  |             |
| Biz_Flag              | char      | 1      | true  |             |
| Biz_Tflag             | char      | 1      | true  |             |
| Biz_P_Time            | datetime  |        | true  |             |
| Biz_Y_Time            | datetime  |        | true  |             |
| Biz_Time              | datetime  |        | true  |             |

### 備註：
*This release has no modifications to this part.*



<span id="CDS_Material_Movement"> </span>
## CDS_Material_Movement
| Column                | Data Type | Length | Nulls | Description |
| --------------------- | --------- | ------ | ----- | ----------- |
| SID                   | nvarchar  | 30     | :key: |             |
| Doc_Year              | char      | 4      | :key: |             |
| Doc_No                | varchar   | 10     | :key: |             |
| Item_Seq              | varchar   | 10     | :key: |             |
| Posting_Date          | nvarchar  | 8      | true  |             |
| Movement_Type_ID      | nvarchar  | 10     | true  |             |
| Movement_Type_Name    | nvarchar  | 50     | true  |             |
| Material_No           | varchar   | 40     | true  |             |
| Factory_ID            | varchar   | 10     | true  |             |
| Storage_Location      | nvarchar  | 10     | true  |             |
| Movement_Qty          | decimal   | 30,10  | true  |             |
| Qty_Unit_ID           | nvarchar  | 10     | true  |             |
| Qty_Unit_Desc         | nvarchar  | 50     | true  |             |
| SO_No                 | varchar   | 35     | true  |             |
| SO_Item_Seq           | varchar   | 10     | true  |             |
| Add_Deduct_Type       | char      | 1      | true  |             |
| Purchase_No           | nvarchar  | 50     | true  |             |
| Purchase_Item_Seq     | varchar   | 10     | true  |             |
| Supplier_ID           | nvarchar  | 20     | true  |             |
| WO_No                 | varchar   | 20     | true  |             |
| WO_Item_Seq           | varchar   | 10     | true  |             |
| Update_By             | varchar   | 50     | true  |             |
| Update_Time           | datetime  |        | true  |             |
| Biz_Flag              | char      | 1      | true  |             |
| Biz_Tflag             | char      | 1      | true  |             |
| Biz_P_Time            | datetime  |        | true  |             |
| Biz_Y_Time            | datetime  |        | true  |             |
| Biz_Time              | datetime  |        | true  |             |

### 備註：
*This release has no modifications to this part.*



<span id="CDS_PO_BOM"> </span>
## CDS_PO_BOM
| Column                | Data Type | Length | Nulls | Description |
| --------------------- | --------- | ------ | ----- | ----------- |
| SID                   | nvarchar  | 30     | :key: |             |
| Factory_ID            | varchar   | 10     | :key: |             |
| PO_No                 | varchar   | 35     | :key: |             |
| Material_No           | varchar   | 40     | :key: |             |
| Material_Name         | nvarchar  | 100    | true  |             |
| Consumption_Qty       | decimal   | 30,10  | true  |             |
| QtyUnit_ID            | nvarchar  | 10     | true  |             |
| QtyUnit_Desc          | nvarchar  | 50     | true  |             |
| Update_By             | varchar   | 50     | true  |             |
| Update_Time           | datetime  |        | true  |             |
| Biz_Flag              | char      | 1      | true  |             |
| Biz_Tflag             | char      | 1      | true  |             |
| Biz_P_Time            | datetime  |        | true  |             |
| Biz_Y_Time            | datetime  |        | true  |             |
| Biz_Time              | datetime  |        | true  |             |
| SO_NO                 | varchar   | 40     | true  |             |

### 備註：
*This release has no modifications to this part.*



<span id="CDS_PO_BOM_Detail"> </span>
## CDS_PO_BOM_Detail
| Column                | Data Type | Length | Nulls | Description |
| --------------------- | --------- | ------ | ----- | ----------- |
| SID                   | nvarchar  | 30     | :key: |             |
| Factory_ID            | varchar   | 10     | :key: |             |
| PO_No                 | varchar   | 35     | :key: |             |
| Material_No           | varchar   | 40     | :key: |             |
| Item_Seq              | varchar   | 10     | :key: |             |
| Material_Name         | nvarchar  | 100    | true  |             |
| Item_Material_No      | varchar   | 40     | true  |             |
| Item_Material_Name    | nvarchar  | 100    | true  |             |
| AVG_Consumption_Qty   | decimal   | 30,10  | true  |             |
| Consumption_Qty       | decimal   | 30,10  | true  |             |
| QtyUnit_ID            | nvarchar  | 10     | true  |             |
| QtyUnit_Desc          | nvarchar  | 50     | true  |             |
| Update_By             | varchar   | 50     | true  |             |
| Update_Time           | datetime  |        | true  |             |
| Biz_Flag              | char      | 1      | true  |             |
| Biz_Tflag             | char      | 1      | true  |             |
| Biz_P_Time            | datetime  |        | true  |             |
| Biz_Y_Time            | datetime  |        | true  |             |
| Biz_Time              | datetime  |        | true  |             |

### 備註：
*This release has no modifications to this part.*



<span id="CDS_WOGroup"> </span>
## CDS_WOGroup
| Column                | Data Type | Length | Nulls | Description |
| --------------------- | --------- | ------ | ----- | ----------- |
| SID                   | nvarchar  | 30     | :key: |             |
| Factory_ID            | varchar   | 10     | :key: |             |
| WO_Group_No           | varchar   | 50     | :key: |             |
| Material_No           | varchar   | 40     | true  |             |
| Material_Name         | nvarchar  | 100    | true  |             |
| WO_Group_Qty          | decimal   | 30,10  | true  |             |
| QtyUnit_ID            | nvarchar  | 10     | true  |             |
| QtyUnit_Desc          | nvarchar  | 50     | true  |             |
| PO_No                 | varchar   | 35     | true  |             |
| PO_Batch              | varchar   | 14     | true  |             |
| Update_By             | varchar   | 50     | true  |             |
| Update_Time           | datetime  |        | true  |             |
| Biz_Flag              | char      | 1      | true  |             |
| Biz_Tflag             | char      | 1      | true  |             |
| Biz_P_Time            | datetime  |        | true  |             |
| Biz_Y_Time            | datetime  |        | true  |             |
| Biz_Time              | datetime  |        | true  |             |

### 備註：
*This release has no modifications to this part.*



<span id="CDS_WOHeader"> </span>
## CDS_WOHeader
| Column                | Data Type | Length | Nulls | Description |
| --------------------- | --------- | ------ | ----- | ----------- |
| SID                   | nvarchar  | 30     | :key: |             |
| Factory_ID            | varchar   | 10     | :key: |             |
| WO_Group_No           | varchar   | 50     | :key: |             |
| WO_No                 | varchar   | 20     | :key: |             |
| PO_No                 | varchar   | 35     | true  |             |
| PO_Batch              | varchar   | 14     | true  |             |
| WO_Type_ID            | nvarchar  | 10     | true  |             |
| WO_Type_Name          | nvarchar  | 50     | true  |             |
| Material_No           | varchar   | 40     | true  |             |
| Material_Name         | nvarchar  | 100    | true  |             |
| WO_Qty                | decimal   | 30,10  | true  |             |
| QtyUnit_ID            | nvarchar  | 10     | true  |             |
| QtyUnit_Desc          | nvarchar  | 50     | true  |             |
| Start_Date            | nvarchar  | 8      | true  |             |
| End_Date              | nvarchar  | 8      | true  |             |
| WO_Status             | nvarchar  | 50     | true  |             |
| Storage_Location      | nvarchar  | 10     | true  |             |
| Update_By             | varchar   | 50     | true  |             |
| Update_Time           | datetime  |        | true  |             |
| Biz_Flag              | char      | 1      | true  |             |
| Biz_Tflag             | char      | 1      | true  |             |
| Biz_P_Time            | datetime  |        | true  |             |
| Biz_Y_Time            | datetime  |        | true  |             |
| Biz_Time              | datetime  |        | true  |             |

### 備註：
*This release has no modifications to this part.*



<span id="CDS_WODetail"> </span>
## CDS_WODetail
| Column                | Data Type | Length | Nulls | Description |
| --------------------- | --------- | ------ | ----- | ----------- |
| SID                   | nvarchar  | 30     | :key: |             |
| Factory_ID            | varchar   | 10     | :key: |             |
| WO_Group_No           | varchar   | 50     | :key: |             |
| WO_No                 | varchar   | 20     | :key: |             |
| Item_Seq              | varchar   | 10     | :key: |             |
| Item_Material_No      | varchar   | 40     | true  |             |
| Item_Material_Name    | nvarchar  | 100    | true  |             |
| Item_Req_Qty          | decimal   | 30,10  | true  |             |
| QtyUnit_ID            | nvarchar  | 10     | true  |             |
| QtyUnit_Desc          | nvarchar  | 50     | true  |             |
| Update_By             | varchar   | 50     | true  |             |
| Update_Time           | datetime  |        | true  |             |
| Biz_Flag              | char      | 1      | true  |             |
| Biz_Tflag             | char      | 1      | true  |             |
| Biz_P_Time            | datetime  |        | true  |             |
| Biz_Y_Time            | datetime  |        | true  |             |
| Biz_Time              | datetime  |        | true  |             |

### 備註：
*This release has no modifications to this part.*



<span id="CDS_WO_Matl_Issuing"> </span>
## CDS_WO_Matl_Issuing
| Column                      | Data Type | Length | Nulls | Description |
| --------------------------- | --------- | ------ | ----- | ----------- |
| SID                         | nvarchar  | 30     | :key: |             |
| WO_No                       | varchar   | 20     | :key: |             |
| Material_No                 | varchar   | 40     | :key: |             |
| Material_Name               | nvarchar  | 100    | true  |             |
| Factory_ID                  | varchar   | 10     | true  |             |
| PO_No                       | varchar   | 35     | true  |             |
| PO_Batch                    | varchar   | 14     | true  |             |
| WO_Group_No                 | varchar   | 50     | true  |             |
| Matl_Issuing_Qty            | decimal   | 30,10  | true  |             |
| QtyUnit_ID                  | nvarchar  | 10     | true  |             |
| QtyUnit_Desc                | nvarchar  | 50     | true  |             |
| IssuingTo_Hierarchy         | nvarchar  | 10     | true  |             |
| Part_No                     | nvarchar  | 30     | true  |             |
| Part_Name                   | nvarchar  | 255    | true  |             |
| IssuingFrom_Storage_Location| varchar   | 4      | true  |             |
| WO_Type_ID                  | nvarchar  | 10     | true  |             |
| WO_Type_Name                | nvarchar  | 50     | true  |             |
| RepackageFrom_SO_No         | varchar   | 35     | true  |             |
| RepackageFrom_SO_Batch      | varchar   | 20     | true  |             |
| Update_By                   | varchar   | 50     | true  |             |
| Update_Time                 | datetime  |        | true  |             |
| Biz_Flag                    | char      | 1      | true  |             |
| Biz_Tflag                   | char      | 1      | true  |             |
| Biz_P_Time                  | datetime  |        | true  |             |
| Biz_Y_Time                  | datetime  |        | true  |             |
| Biz_Time                    | datetime  |        | true  |             |

### 備註：
*This release has no modifications to this part.*



<span id="CDS_FGReceipt"> </span>
## CDS_FGReceipt
| Column                | Data Type | Length | Nulls | Description |
| --------------------- | --------- | ------ | ----- | ----------- |
| SID                   | nvarchar  | 30     | :key: |             |
| Factory_ID            | varchar   | 10     | :key: |             |
| WO_No                 | varchar   | 20     | :key: |             |
| Material_No           | varchar   | 40     | :key: |             |
| Material_Name         | nvarchar  | 100    | true  |             |
| PO_No                 | varchar   | 35     | true  |             |
| PO_Batch              | varchar   | 14     | true  |             |
| Receipt_Qty           | decimal   | 30,10  | true  |             |
| QtyUnit_ID            | nvarchar  | 10     | true  |             |
| QtyUnit_Desc          | nvarchar  | 50     | true  |             |
| Storage_Location      | nvarchar  | 10     | true  |             |
| PO_Size               | nvarchar  | 20     | true  |             |
| RepackageFrom_SO_No   | varchar   | 35     | true  |             |
| RepackageFrom_SO_Batch| varchar   | 20     | true  |             |
| Update_By             | varchar   | 50     | true  |             |
| Update_Time           | datetime  |        | true  |             |
| Biz_Flag              | char      | 1      | true  |             |
| Biz_Tflag             | char      | 1      | true  |             |
| Biz_P_Time            | datetime  |        | true  |             |
| Biz_Y_Time            | datetime  |        | true  |             |
| Biz_Time              | datetime  |        | true  |             |

### 備註：
*This release has no modifications to this part.*



<span id="CDS_Sales_Order_Header"> </span>
## CDS_Sales_Order_Header
| Column                | Data Type | Length | Nulls | Description |
| --------------------- | --------- | ------ | ----- | ----------- |
| SID                   | nvarchar  | 30     | :key: |             |
| Factory_ID            | varchar   | 10     | :key: |             |
| SO_No                 | varchar   | 35     | :key: |             |
| PO_No                 | varchar   | 35     | true  |             |
| PODD                  | nvarchar  | 8      | true  |             |
| POSDD                 | nvarchar  | 8      | true  |             |
| PO_Receipt_Date       | nvarchar  | 8      | true  |             |
| Material_No           | varchar   | 40     | true  |             |
| SO_Type_ID            | nvarchar  | 10     | true  |             |
| SO_Type_Desc          | nvarchar  | 50     | true  |             |
| Customer_ID           | nvarchar  | 10     | true  |             |
| Customer_Name         | nvarchar  | 100    | true  |             |
| Desti_ID              | nvarchar  | 10     | true  |             |
| Desti_Name            | nvarchar  | 100    | true  |             |
| Desti_Country_Name    | nvarchar  | 35     | true  |             |
| Desti_Address         | nvarchar  | 200    | true  |             |
| Update_By             | varchar   | 50     | true  |             |
| Update_Time           | datetime  |        | true  |             |
| Biz_Flag              | char      | 1      | true  |             |
| Biz_Tflag             | char      | 1      | true  |             |
| Biz_P_Time            | datetime  |        | true  |             |
| Biz_Y_Time            | datetime  |        | true  |             |
| Biz_Time              | datetime  |        | true  |             |

### 備註：
*This release has no modifications to this part.*



<span id="CDS_Sales_Order_Detail"> </span>
## CDS_Sales_Order_Detail
| Column                | Data Type | Length | Nulls | Description |
| --------------------- | --------- | ------ | ----- | ----------- |
| SID                   | nvarchar  | 30     | :key: |             |
| Factory_ID            | varchar   | 10     | :key: |             |
| SO_No                 | varchar   | 35     | :key: |             |
| Item_Seq              | varchar   | 10     | :key: |             |
| Material_No           | varchar   | 40     | true  |             |
| PO_Size               | nvarchar  | 20     | true  |             |
| PO_Qty                | decimal   | 30,10  | true  |             |
| Qty_Unit_ID           | nvarchar  | 10     | true  |             |
| Update_By             | varchar   | 50     | true  |             |
| Update_Time           | datetime  |        | true  |             |
| Biz_Flag              | char      | 1      | true  |             |
| Biz_Tflag             | char      | 1      | true  |             |
| Biz_P_Time            | datetime  |        | true  |             |
| Biz_Y_Time            | datetime  |        | true  |             |
| Biz_Time              | datetime  |        | true  |             |
| Unit_Price            | decimal   |        | true  |             |
| Currency              | varchar   | 10     | true  |             |

### 備註：
*This release has no modifications to this part.*



<span id="CDS_Carton_Arrange_Header"> </span>
## CDS_Carton_Arrange_Header
| Column                | Data Type | Length | Nulls | Description |
| --------------------- | --------- | ------ | ----- | ----------- |
| SID                   | nvarchar  | 30     | :key: |             |
| Factory_ID            | varchar   | 10     | :key: |             |
| SO_No                 | varchar   | 35     | :key: |             |
| Carton_Arrange_Seq    | varchar   | 10     | :key: |             |
| PO_Size               | nvarchar  | 20     | true  |             |
| Cust_Size             | varchar   | 10     | true  |             |
| Material_No           | varchar   | 40     | true  |             |
| In_Carton_Qty         | decimal   | 30,10  | true  |             |
| Carton_Cnt            | int       |        | true  |             |
| Carton_No_First       | int       |        | true  |             |
| Carton_No_Last        | int       |        | true  |             |
| Weight_Net            | decimal   | 30,10  | true  |             |
| Weight_Gross          | decimal   | 30,10  | true  |             |
| CBM                   | decimal   | 30,10  | true  |             |
| Packing_Type          | varchar   | 10     | true  |             |
| Packing_Contents      | nvarchar  | 200    | true  |             |
| Update_By             | varchar   | 50     | true  |             |
| Update_Time           | datetime  |        | true  |             |
| Biz_Flag              | char      | 1      | true  |             |
| Biz_Tflag             | char      | 1      | true  |             |
| Biz_P_Time            | datetime  |        | true  |             |
| Biz_Y_Time            | datetime  |        | true  |             |
| Biz_Time              | datetime  |        | true  |             |

### 備註：
*This release has no modifications to this part.*



<span id="CDS_Carton_Arrange_Detail"> </span>
## CDS_Carton_Arrange_Detail
| Column                | Data Type | Length | Nulls | Description |
| --------------------- | --------- | ------ | ----- | ----------- |
| SID                   | nvarchar  | 30     | :key: |             |
| Factory_ID            | varchar   | 10     | :key: |             |
| SO_No                 | varchar   | 35     | :key: |             |
| Material_No           | varchar   | 40     |       |             |
| Carton_No             | int       |        | :key: |             |
| PO_Size               | nvarchar  | 20     | :key: |             |
| Cust_Size             | varchar   | 10     | :key: |             |
| In_Carton_Qty         | decimal   | 30,10  |       |             |
| Update_By             | varchar   | 50     | true  |             |
| Update_Time           | datetime  |        | true  |             |
| Biz_Flag              | char      | 1      | true  |             |
| Biz_Tflag             | char      | 1      | true  |             |
| Biz_P_Time            | datetime  |        | true  |             |
| Biz_Y_Time            | datetime  |        | true  |             |
| Biz_Time              | datetime  |        | true  |             |

### 備註：
*This release has no modifications to this part.*



<span id="CDS_FG_Write_Off_Result"> </span>
## CDS_FG_Write_Off_Result
| Column                | Data Type | Length | Nulls | Description |
| --------------------- | --------- | ------ | ----- | ----------- |
| SID                   | varchar  | 30     | :key: |             |
| Factory_ID            | varchar  | 10     | :key: |             |
| So_No                 | varchar  | 35     | :key: |             |
| So_New                | varchar  | 35     | :key: |             |
| Po_No                 | varchar  | 35     | true  |             |
| Po_New                | varchar  | 35     | true  |             |
| Offset_Qty            | decimal  | 15,5   | true  |             |
| Deletion_Flag         | varchar  | 5      | true  |             |
| Update_By             | varchar  | 50     | true  |             |
| Update_Time           | datetime |        | true  |             |
| Biz_Flag              | char     | 1      | true  |             |
| Biz_Tflag             | char     | 1      | true  |             |
| Biz_P_Time            | datetime |        | true  |             |
| Biz_Y_Time            | datetime |        | true  |             |
| Biz_Time              | datetime |        | true  |             |

### 備註：
*This release has no modifications to this part.*



<span id="CDS_Shipment_Header"> </span>
## CDS_Shipment_Header
| Column                | Data Type | Length | Nulls | Description |
| --------------------- | --------- | ------ | ----- | ----------- |
| SID                   | nvarchar  | 30     | :key: |             |
| Factory_ID            | varchar   | 10     | :key: |             |
| Shipment_No           | varchar   | 20     | :key: |             |
| Customer_ID           | nvarchar  | 10     | true  |             |
| PODD                  | nvarchar  | 8      | true  |             |
| FGOut_ActualDate      | nvarchar  | 8      | true  |             |
| Delivery_Mode         | nvarchar  | 10     | true  |             |
| Delivery_Mode_Desc    | nvarchar  | 50     | true  |             |
| Desti_ID              | nvarchar  | 10     | true  |             |
| Shipment_Mode_Desc    | nvarchar  | 50     | true  |             |
| Forwarder_Name        | nvarchar  | 100    | true  |             |
| Service_ID            | nvarchar  | 35     | true  |             |
| Update_By             | varchar   | 50     | true  |             |
| Update_Time           | datetime  |        | true  |             |
| Biz_Flag              | char      | 1      | true  |             |
| Biz_Tflag             | char      | 1      | true  |             |
| Biz_P_Time            | datetime  |        | true  |             |
| Biz_Y_Time            | datetime  |        | true  |             |
| Biz_Time              | datetime  |        | true  |             |

### 備註：
*This release has no modifications to this part.*



<span id="CDS_Shipment_Detail"> </span>
## CDS_Shipment_Detail
| Column                | Data Type | Length | Nulls | Description |
| --------------------- | --------- | ------ | ----- | ----------- |
| SID                   | nvarchar  | 30     | :key: |             |
| Factory_ID            | varchar   | 10     | :key: |             |
| Shipment_No           | varchar   | 20     | :key: |             |
| Item_Seq              | varchar   | 10     | :key: |             |
| SO_No                 | varchar   | 35     | true  |             |
| Material_No           | varchar   | 40     | true  |             |
| PO_Size               | nvarchar  | 20     | true  |             |
| Shipment_Qty          | decimal   | 30,10  | true  |             |
| Qty_Unit_ID           | nvarchar  | 10     | true  |             |
| Update_By             | varchar   | 50     | true  |             |
| Update_Time           | datetime  |        | true  |             |
| Biz_Flag              | char      | 1      | true  |             |
| Biz_Tflag             | char      | 1      | true  |             |
| Biz_P_Time            | datetime  |        | true  |             |
| Biz_Y_Time            | datetime  |        | true  |             |
| Biz_Time              | datetime  |        | true  |             |

### 備註：
*This release has no modifications to this part.*





<span id="EXAMPLE_TABLE_NAME"> </span>
## EXAMPLE_TABLE_NAME
| Column                | Data Type | Length | Nulls | Description |
| --------------------- | --------- | ------ | ----- | ----------- |

### 備註：
*This release has no modifications to this part.*


###### tags: `cds-data-loader`
