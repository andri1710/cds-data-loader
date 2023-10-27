# [cds-data-loader] System spec - Auto running

## Trigger List
### 1. weeklyTrigger1

   * **Timing:** 21:30:00 Thursday everyweek (每周每星期四21:30)
   * **To do Job List :** 
     * [weeklyJob1](#weeklyJob1)
   
### 2. dailyTrigger

   * **Timing:** 21:15:00 everyday (每天21:15:00)
   * **To do Job List :** 
     * [dailyJob](#dailyJob)
   
### 3. hourlyTrigger

   * **Timing:** 15 past the hour (每小時第15分鐘)
   * **To do Job List :** 
     * [hourlyJob](#hourlyJob)

## Job List

<span id="weeklyJob1"></span>
### 1. weeklyJob1

   * **Job Detail:** WeeklyJob_WeeklyOneTime
     | Trans. Kind | SPEC_ID | Remark                |
     | ----------- | ------- | ------------------------- |
     | Checker     | CHK001  | 檢查30天內有下採購單的料號 是否有對應海關料號(海料), 若沒有對應，自動發MAIL給USER。      |
     
<span id="dailyJob"></span>
### 2. dailyJob

   * **Job Detail:** DailyJob_DailyOneTime
     | Trans. Kind | SPEC_ID | Remark                |
     | ----------- | ------- | ------------------------- |
     | By_Spec_ID  | [SAP_MM006](#SAP_MM006)   |      |
     | By_Spec_ID  | [SAP_MM011](#SAP_MM011)   |      |
     | DB_Worker   | Cleaning_IMDBBackup   |      |
     
<span id="hourlyJob"></span>
### 3. hourlyJob

   * **Job Detail:** HourlyJob_HourlyOneTime
     | Trans. Kind | SPEC_ID     | Remark                |
     | ----------- | ----------- | --------------------- |
     | By_Spec_ID  | [SAP_MM028](#SAP_MM028)   |      |
     | By_Spec_ID  | [SAP_PP053](#SAP_PP053)   |      |
     | By_Spec_ID  | [SAP_SD010](#SAP_SD010)   |      |
     | By_Spec_ID  | [SAP_SD011](#SAP_SD011)   |      |
     | By_Spec_ID  | [PLM_PPI001](#PLM_PPI001) |      |
     | By_Spec_ID  | [SAP_MM045](#SAP_MM045)   |      |
   
## SPEC_ID
#### 共同拋轉邏輯：
1. 在拋轉每個SID時重開新的連線，並在COMMIT後關閉連線。
2. 能否COMMIT的管控點：
   * 每個Table的資料比數 (Control_File.Count) 等於 實際拋轉的資料筆數。
   * 每個SID的table個數 (Control_File.Table_Count) 等於 實際拋轉的table個數。
   * 拋完所有該SID的資料 (廠別, table, 資料)時 一起Commit。
3. Commit順序：
   * 1. VCS_DB的異動
   * 2. IMDB的異動
     * Control_File.Control_Flag 上 Y。
     * Control_File.Update_By 上 ExeService
     * Control_File.Update_Time 上 啟動拋轉日期時間。
4. **檢查該table的資料是否存在 (使用該table的key值)**：
    * **若存在，直接Insert到對應的table、Insert_By上ExeService、Insert_At上啟動拋轉日期時間**。
    * **若不存在，Update所有不是Key值的欄位、Update_By上ExeService、Update_At上啟動拋轉日期時間**。
5. 日期欄位的轉換。因SAP及PLM傳出來的日期為字串(yyyyMMdd)，故在本拋轉程式會將其轉換成日期格式。
<span id="PLM_PPI001"></span>
### PLM_PPI001 

| From Table Name | To Table Name | Description |
| --------------- | ------------- | ----------- |
| [SAP_BOM_Header](/@hackmd-andri/CDS-DBStruc-PLM_IMDB#SAP_BOM_Header)  | [M_BOM_HEADER](/@hackmd-andri/CDS-DBStruc-VCS_DB#M_BOM_HEADER)  | 基本BOM表頭  :heavy_check_mark: |
| [SAP_BOM_Detail](/@hackmd-andri/CDS-DBStruc-PLM_IMDB#SAP_BOM_Detail)  | [M_BOM_DETAIL](/@hackmd-andri/CDS-DBStruc-VCS_DB#M_BOM_DETAIL)  | 基本BOM表身  :heavy_check_mark: |

#### 備註：
*This release has no modifications to this part.*

<span id="SAP_MM006"></span>
### SAP_MM006 

| From Table Name | To Table Name | Description         |
| --------------- | ------------- | ------------------- |
| [All_Material](/@hackmd-andri/CDS-DBStruc-SAP_IMDB#All_Material)    | [M_MATERIAL](/@hackmd-andri/CDS-DBStruc-VCS_DB#M_MATERIAL)    | 內部材料主檔          :heavy_check_mark: |

#### 備註：
* `≈202308` 若Generic_Material=" "時，填入MaterialNo。
   ```javascript=
   IF (IMDB.All_Material.Generic_Material == " ")
   {
      VCS_DB.M_Material.Generic_Matl_Code = IMDB.All_Material.MaterialNo;
   }
   ELSE
   {
       VCS_DB.M_Material.Generic_Matl_Code = IMDB.All_Material.Generic_Material;
   }
   
   ```



<span id="SAP_MM011"> </span>
### SAP_MM011 

| From Table Name     | To Table Name     | Description |
| ------------------- | ----------------- | ----------- |
| [All_Supplier](/@hackmd-andri/CDS-DBStruc-SAP_IMDB#All_Supplier)               | [M_SUPPLIER](/@hackmd-andri/CDS-DBStruc-VCS_DB#M_SUPPLIER)               | 廠商主檔     :heavy_check_mark: |
| [All_Supplier_Detail](/@hackmd-andri/CDS-DBStruc-SAP_IMDB#All_Supplier_Detail) | [M_SUPPLIER_DETAIL](/@hackmd-andri/CDS-DBStruc-VCS_DB#M_SUPPLIER_DETAIL) | 廠商明細     :heavy_check_mark: |

#### 備註：
*This release has no modifications to this part.*


<span id="SAP_MM028"> </span>
### SAP_MM028 

| From Table Name           | To Table Name                | Description  |
| ------------------------- | ---------------------------- | ------------ |
| [All_Purchase_Order_Header](/@hackmd-andri/CDS-DBStruc-SAP_IMDB#All_Purchase_Order_Header) | [T_PURCHASE](/@hackmd-andri/CDS-DBStruc-VCS_DB#T_PURCHASE)                                                                  | 採購主檔      :heavy_check_mark: |
| [All_Purchase_Order_Item](/@hackmd-andri/CDS-DBStruc-SAP_IMDB#All_Purchase_Order_Item)     | [T_PURCHASE_DETAIL](/@hackmd-andri/CDS-DBStruc-VCS_DB#T_PURCHASE_DETAIL)                                                    | 採購明細      :heavy_check_mark: |
| [All_Component](/@hackmd-andri/CDS-DBStruc-SAP_IMDB#All_Component)                         | [T_PURCHASE_SUBCONT](/@hackmd-andri/CDS-DBStruc-VCS_DB#T_PURCHASE_SUBCONT)                                                  | 採購原件明細   :heavy_check_mark: |
| [All_Delivery_Schedule](/@hackmd-andri/CDS-DBStruc-SAP_IMDB#All_Delivery_Schedule)         | [T_PURCHASE_DELIVERY_SCHEDULE](/@hackmd-andri/CDS-DBStruc-VCS_DB#T_PURCHASE_DELIVERY_SCHEDULE) | 採購單送貨明細 :heavy_check_mark: |

#### 備註：
*This release has no modifications to this part.*

<span id="SAP_MM045"> </span>
### SAP_MM045 

| From Table Name | To Table Name | Description             |
| --------------- | ------------- | ----------------------- |
| [CDS_Inbound_DN](/@hackmd-andri/CDS-DBStruc-SAP_IMDB#CDS_Inbound_DN)  | [T_INBOUND_DN](/@hackmd-andri/CDS-DBStruc-VCS_DB#T_INBOUND_DN)  | 入廠的運送明細(廠商出貨名細) :heavy_check_mark: |

#### 備註：
* `≈202309` 若InboundDN_No的第一碼為零，自動去掉。
   ```javascript=
    var InboundDN_No = IMDB.CDS_Inbound_DN.InboundDN_No;
    if (InboundDN_No.Substring(0,1) == "0")
    {
        InboundDN_No = InboundDN_No.Substring(1);
    }
    VCS_DB.T_INBOUND_DN.InboundDN_No = InboundDN_No;   
   ```

<span id="SAP_MM063"> </span>
### SAP_MM063 

| From Table Name             | To Table Name | Description      |
| --------------------------- | ------------- | ---------------- |
| [CDS_Receipt_Invoice_Header](/@hackmd-andri/CDS-DBStruc-SAP_IMDB#CDS_Receipt_Invoice_Header)   | ???           | 發票驗證文件表頭    |
| [CDS_Receipt_Invoice_Detail](/@hackmd-andri/CDS-DBStruc-SAP_IMDB#CDS_Receipt_Invoice_Detail)   | ???           | 發票驗證文件表身    |
| [CDS_Receipt_Invoice_Account](/@hackmd-andri/CDS-DBStruc-SAP_IMDB#CDS_Receipt_Invoice_Account) | ???           | 發票驗證文件總帳科目 |

#### 備註：
*This release has no modifications to this part.*

<span id="SAP_MM064"> </span>
### SAP_MM064 

| From Table Name       | To Table Name | Description          |
| --------------------- | ------------- | -------------------- |
| [CDS_Stock_At_Factory](/@hackmd-andri/CDS-DBStruc-SAP_IMDB#CDS_Stock_At_Factory)   | ???           | 廠內庫存               |
| [CDS_Stock_At_Supplier](/@hackmd-andri/CDS-DBStruc-SAP_IMDB#CDS_Stock_At_Supplier) | ???           | 供應商庫存(委外加工原料) |
| [CDS_SO_Stock](/@hackmd-andri/CDS-DBStruc-SAP_IMDB#CDS_SO_Stock)                   | ???           | 訂單庫存               |

#### 備註：
*This release has no modifications to this part.*

<span id="SAP_MM067"> </span>
### SAP_MM067 

| From Table Name       | To Table Name | Description             |
| --------------------- | ------------- | ----------------------- |
| [CDS_Material_Movement](/@hackmd-andri/CDS-DBStruc-SAP_IMDB#CDS_Material_Movement) | ???           | 物料文件                 |

#### 備註：
*This release has no modifications to this part.*

<span id="SAP_PP053"> </span>
### SAP_PP053 

| From Table Name   | To Table Name   | Description  |
| ----------------- | --------------- | ------------ |
| [CDS_PO_BOM](/@hackmd-andri/CDS-DBStruc-SAP_IMDB#CDS_PO_BOM)               | [T_PO_BOM](/@hackmd-andri/CDS-DBStruc-VCS_DB#T_PO_BOM)               | PO BOM主檔    :heavy_check_mark:|
| [CDS_PO_BOM_Detail](/@hackmd-andri/CDS-DBStruc-SAP_IMDB#CDS_PO_BOM_Detail) | [T_PO_BOM_DETAIL](/@hackmd-andri/CDS-DBStruc-VCS_DB#T_PO_BOM_DETAIL) | PO BOM 明細   :heavy_check_mark:|

#### 特殊拋轉邏輯：
* `≈2023/08/24`
T_PO_BOM_DETAIL 先檢查是否有資料，若已存在，先刪除後再新增所有明細。
   ```sql
   SELECT * FROM T_PO_BOM_DETAIL WHERE Factory_ID = <廠別> AND PO_No = <PO_No> AND Matl_Code = <材料號碼>
   
   CASE WHEN (IS EXISTS) THEN
      DELETE FROM T_PO_BOM_DETAIL WHERE Factory_ID = <廠別> AND PO_No = <PO_No> AND Matl_Code = <材料號碼>
      
   INSERT INTO T_PO_BOM_DETAIL VALUES (<廠別> & <PO_No> & <材料號碼>明細資料)
   ```
#### 備註：
*This release has no modifications to this part.*

<span id="SAP_PP054"> </span>
### SAP_PP054 

| From Table Name | To Table Name | Description     |
| --------------- | ------------- | --------------- |
| [CDS_WOGroup](/@hackmd-andri/CDS-DBStruc-SAP_IMDB#CDS_WOGroup)      | ???           | 工單群組Outbound |
| [CDS_WOHeader](/@hackmd-andri/CDS-DBStruc-SAP_IMDB#CDS_WOHeader)    | ???           | 工單表頭Outbound |
| [CDS_WODetail](/@hackmd-andri/CDS-DBStruc-SAP_IMDB#CDS_WODetail)    | ???           | 工單元件Outbound |

#### 備註：
*This release has no modifications to this part.*

<span id="SAP_PP055"> </span>
### SAP_PP055

| From Table Name     | To Table Name | Description |
| ------------------- | ------------- | ----------- |
| [CDS_WO_Matl_Issuing](/@hackmd-andri/CDS-DBStruc-SAP_IMDB#CDS_WO_Matl_Issuing) | ???           | 發料資訊傳出  |

#### 備註：
*This release has no modifications to this part.*

<span id="SAP_PP056"> </span>
### SAP_PP056

| From Table Name | To Table Name | Description   |
| --------------- | ------------- | ------------- |
| [CDS_FGReceipt](/@hackmd-andri/CDS-DBStruc-SAP_IMDB#CDS_FGReceipt)   | ???           | 成品入庫資訊傳出 |

#### 備註：
*This release has no modifications to this part.*

<span id="SAP_SD010"> </span>
### SAP_SD010

| From Table Name           | To Table Name           | Description |
| ------------------------- | ----------------------- | ----------- |
| [CDS_Sales_Order_Header](/@hackmd-andri/CDS-DBStruc-SAP_IMDB#CDS_Sales_Order_Header)       | [T_SALES_ORDER](/@hackmd-andri/CDS-DBStruc-VCS_DB#T_SALES_ORDER)                     | 訂單主檔      :heavy_check_mark:|
| [CDS_Sales_Order_Detail](/@hackmd-andri/CDS-DBStruc-SAP_IMDB#CDS_Sales_Order_Detail)       | [T_SALES_ORDER_DETAIL](/@hackmd-andri/CDS-DBStruc-VCS_DB#T_SALES_ORDER_DETAIL)       | 訂單明細      :heavy_check_mark:|
| [CDS_Carton_Arrange_Header](/@hackmd-andri/CDS-DBStruc-SAP_IMDB#CDS_Carton_Arrange_Header) | [T_CARTON_ARRANGE_HEADER](/@hackmd-andri/CDS-DBStruc-VCS_DB#T_CARTON_ARRANGE_HEADER) | 外箱編列主檔  :heavy_check_mark:|
| [CDS_Carton_Arrange_Detail](/@hackmd-andri/CDS-DBStruc-SAP_IMDB#CDS_Carton_Arrange_Detail) | [T_CARTON_ARRANGE_DETAIL](/@hackmd-andri/CDS-DBStruc-VCS_DB#T_CARTON_ARRANGE_DETAIL) | 外箱編列明細  :heavy_check_mark:|
| [CDS_FG_Write_Off_Result](/@hackmd-andri/CDS-DBStruc-SAP_IMDB#CDS_FG_Write_Off_Result)     | [T_FG_WRITE_OFF_RESULT](/@hackmd-andri/CDS-DBStruc-VCS_DB#T_FG_WRITE_OFF_RESULT)     | 重包裝明細    :heavy_check_mark:|

#### 備註：
*This release has no modifications to this part.*

<span id="SAP_SD011"> </span>
### SAP_SD011

| From Table Name     | To Table Name     | Description |
| ------------------- | ----------------- | ----------- |
| [CDS_Shipment_Header](/@hackmd-andri/CDS-DBStruc-SAP_IMDB#CDS_Shipment_Header) | [T_S<HIPMENT](/@hackmd-andri/CDS-DBStruc-VCS_DB#T_SHIPMENT)               | 出貨主檔      :heavy_check_mark:|
| [CDS_Shipment_Detail](/@hackmd-andri/CDS-DBStruc-SAP_IMDB#CDS_Shipment_Detail) | [T_SHIPMENT_DETAIL](/@hackmd-andri/CDS-DBStruc-VCS_DB#T_SHIPMENT_DETAIL) | 出貨明細      :heavy_check_mark:|

#### 特殊拋轉邏輯：
* `≈2023/10/18`
T_SHIPMENT_DETAIL 先檢查是否有資料，若已存在，先刪除後再新增所有明細。
   ```sql
   SELECT * FROM T_SHIPMENT_DETAIL WHERE Factory_ID = <廠別> AND Shipment_No = <Shipment_No>
   
   CASE WHEN (IS EXISTS) THEN
      DELETE FROM T_SHIPMENT_DETAIL WHERE Factory_ID = <廠別> AND Shipment_No = <Shipment_No>
      
   INSERT INTO T_SHIPMENT_DETAIL VALUES (<廠別>及<Shipment_No>明細資料)
   ```
   


#### 備註：
*This release has no modifications to this part.*


###### tags: `cds-data-loader`
