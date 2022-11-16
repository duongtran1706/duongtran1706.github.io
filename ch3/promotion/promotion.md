# Promotion

- [Promotion](#promotion)
  - [Promotion:](#promotion-1)
    - [Miêu tả](#miêu-tả)
    - [Struct data](#struct-data)
- [Promotion Api](#promotion-api)
    - [`/v2/promotions`](#v2promotions)
      - [`POST`](#post)
        - [`Summary`:](#summary)
        - [`Parameters`](#parameters)
        - [`Responses`](#responses)
    - [`/v2/promotions/{promotion_id}`](#v2promotionspromotion_id)
      - [`GET`](#get)
        - [`Summary`:](#summary-1)
        - [`Parameters`](#parameters-1)
        - [`Responses`](#responses-1)
      - [`DELETE`](#delete)
        - [`Summary`:](#summary-2)
        - [`Parameters`](#parameters-2)
        - [`Responses`](#responses-2)
      - [`PATCH`](#patch)
        - [`Summary`:](#summary-3)
        - [`Parameters`](#parameters-3)
        - [`Responses`](#responses-3)
    - [`/v2/promotions:approve/{promotion_id}`](#v2promotionsapprovepromotion_id)
      - [`POST`](#post-1)
        - [`Summary`:](#summary-4)
        - [`Parameters`](#parameters-4)
        - [`Responses`](#responses-4)
    - [`/v2/promotions:count`](#v2promotionscount)
      - [`GET`](#get-1)
        - [`Summary`:](#summary-5)
        - [`Parameters`](#parameters-5)
        - [`Responses`](#responses-5)
    - [`/v2/promotions:end/{promotion_id}`](#v2promotionsendpromotion_id)
      - [`POST`](#post-2)
        - [`Summary`:](#summary-6)
        - [`Parameters`](#parameters-6)
        - [`Responses`](#responses-6)
    - [`/v2/promotions:postpone/{promotion_id}`](#v2promotionspostponepromotion_id)
      - [`POST`](#post-3)
        - [`Summary`:](#summary-7)
        - [`Parameters`](#parameters-7)
        - [`Responses`](#responses-7)
    - [`/v2/promotions:reject/{promotion_id}`](#v2promotionsrejectpromotion_id)
      - [`POST`](#post-4)
        - [`Summary`:](#summary-8)
        - [`Parameters`](#parameters-8)
        - [`Responses`](#responses-8)
    - [`/v2/promotions:request_approve/{promotion_id}`](#v2promotionsrequest_approvepromotion_id)
      - [`POST`](#post-5)
        - [`Summary`:](#summary-9)
        - [`Parameters`](#parameters-9)
        - [`Responses`](#responses-9)
    - [`/v2/promotions:resume/{promotion_id}`](#v2promotionsresumepromotion_id)
      - [`POST`](#post-6)
        - [`Summary`:](#summary-10)
        - [`Parameters`](#parameters-10)
        - [`Responses`](#responses-10)
    - [`/v2/promotions:search`](#v2promotionssearch)
      - [`GET`](#get-2)
        - [`Summary`:](#summary-11)
        - [`Parameters`](#parameters-11)
        - [`Responses`](#responses-11)
    - [`/v2/promotions/{promotion_id}/contents`](#v2promotionspromotion_idcontents)
      - [`POST`](#post-7)
        - [`Summary`:](#summary-12)
        - [`Parameters`](#parameters-12)
        - [`Responses`](#responses-12)
      - [`PUT`](#put)
        - [`Summary`:](#summary-13)
        - [`Parameters`](#parameters-13)
        - [`Responses`](#responses-13)
    - [`/v2/promotions/{promotion_id}/targets`](#v2promotionspromotion_idtargets)
      - [`POST`](#post-8)
        - [`Parameters`](#parameters-14)
        - [`Responses`](#responses-14)
      - [`PUT`](#put-1)
        - [`Parameters`](#parameters-15)
        - [`Responses`](#responses-15)
    - [`/v2/promotions/{promotion_id}/condition-usages`](#v2promotionspromotion_idcondition-usages)
      - [`POST`](#post-9)
        - [`Parameters`](#parameters-16)
        - [`Responses`](#responses-16)
    - [`/promotions/{promotion_id}/code-settings`](#promotionspromotion_idcode-settings)
      - [`GET`](#get-3)
        - [`Summary`:](#summary-14)
        - [`Parameters`](#parameters-17)
        - [`Responses`](#responses-17)
    - [`/v2/codes:count`](#v2codescount)
      - [`GET`](#get-4)
        - [`Summary`:](#summary-15)
        - [`Parameters`](#parameters-18)
        - [`Responses`](#responses-18)
    - [`/v2/promotions/{promotion_id}/code-setting`](#v2promotionspromotion_idcode-setting)
      - [`POST`](#post-10)
        - [`Summary`:](#summary-16)
        - [`Parameters`](#parameters-19)
        - [`Responses`](#responses-19)
    - [`/v2/promotions/{promotion_id}/code-settings`](#v2promotionspromotion_idcode-settings)
      - [`PATCH`](#patch-1)
        - [`Summary`:](#summary-17)
        - [`Parameters`](#parameters-20)
        - [`Responses`](#responses-20)
    - [`/ecomv2/v2/promotions:apply-promotion`](#ecomv2v2promotionsapply-promotion)
      - [`POST`](#post-11)
        - [`Summary`:](#summary-18)
        - [`Parameters`](#parameters-21)
        - [`Responses`](#responses-21)
    - [`/ecomv2/v2/promotions:check-apply-promotion`](#ecomv2v2promotionscheck-apply-promotion)
      - [`POST`](#post-12)
        - [`Summary`:](#summary-19)
        - [`Parameters`](#parameters-22)
        - [`Responses`](#responses-22)
    - [`/ecomv2/v2/promotions:check-voucher-code-is-valid`](#ecomv2v2promotionscheck-voucher-code-is-valid)
      - [`POST`](#post-13)
        - [`Summary`:](#summary-20)
        - [`Parameters`](#parameters-23)
        - [`Responses`](#responses-23)
    - [`/ecomv2/v2/promotions:commit-apply-promotion`](#ecomv2v2promotionscommit-apply-promotion)
      - [`POST`](#post-14)
        - [`Summary`:](#summary-21)
        - [`Parameters`](#parameters-24)
        - [`Responses`](#responses-24)
    - [`/ecomv2/v2/promotions:list-promotions`](#ecomv2v2promotionslist-promotions)
      - [`POST`](#post-15)
        - [`Summary`:](#summary-22)
        - [`Parameters`](#parameters-25)
        - [`Responses`](#responses-25)
    - [`/ecomv2/v2/promotions:revert-apply-promotion`](#ecomv2v2promotionsrevert-apply-promotion)
      - [`POST`](#post-16)
        - [`Summary`:](#summary-23)
        - [`Parameters`](#parameters-26)
        - [`Responses`](#responses-26)
    - [`/saleman/v2/promotions:list-promotions`](#salemanv2promotionslist-promotions)
      - [`POST`](#post-17)
        - [`Summary`:](#summary-24)
        - [`Parameters`](#parameters-27)
        - [`Responses`](#responses-27)
    - [`/v1/combines/promotions:apply-promotion`](#v1combinespromotionsapply-promotion)
      - [`POST`](#post-18)
        - [`Summary`:](#summary-25)
        - [`Parameters`](#parameters-28)
        - [`Responses`](#responses-28)
    - [`/v1/combines/promotions:check-apply-promotion`](#v1combinespromotionscheck-apply-promotion)
      - [`POST`](#post-19)
        - [`Parameters`](#parameters-29)
        - [`Responses`](#responses-29)
    - [`/v1/combines/promotions:check-voucher-code-is-valid`](#v1combinespromotionscheck-voucher-code-is-valid)
      - [`POST`](#post-20)
        - [`Summary`:](#summary-26)
        - [`Parameters`](#parameters-30)
        - [`Responses`](#responses-30)
    - [`/v1/combines/promotions:commit-apply-promotio`n](#v1combinespromotionscommit-apply-promotion)
      - [`POST`](#post-21)
        - [`Parameters`](#parameters-31)
        - [`Responses`](#responses-31)
    - [`/v1/combines/promotions:list-promotions`](#v1combinespromotionslist-promotions)
      - [`POST`](#post-22)
        - [`Summary`:](#summary-27)
        - [`Parameters`](#parameters-32)
        - [`Responses`](#responses-32)
    - [`/v1/combines/promotions:list-promotions-types`](#v1combinespromotionslist-promotions-types)
      - [`POST`](#post-23)
        - [`Summary`:](#summary-28)
        - [`Parameters`](#parameters-33)
        - [`Responses`](#responses-33)
    - [`/v1/combines/promotions:revert-apply-promotion`](#v1combinespromotionsrevert-apply-promotion)
      - [`POST`](#post-24)
        - [`Parameters`](#parameters-34)
        - [`Responses`](#responses-34)
    - [`Models`](#models)
      - [`CodeSettingCodeType`](#codesettingcodetype)
      - [`CodeSettingTypeCode`](#codesettingtypecode)
      - [`ConditionUsageMaxTimesPerPerson`](#conditionusagemaxtimesperperson)
      - [`ConditionUsageMaxTimesPerPersonPerTime`](#conditionusagemaxtimesperpersonpertime)
      - [`ConditionUsageMaxTimesUsage`](#conditionusagemaxtimesusage)
      - [`ContentEvent`](#contentevent)
      - [`MaxTimesPerPersonPerTimeTimeType`](#maxtimesperpersonpertimetimetype)
      - [`googlerpcStatus`](#googlerpcstatus)
      - [`promotionv2MaxTimes`](#promotionv2maxtimes)
      - [`promotionv2Status`](#promotionv2status)
      - [`v2ApprovePromotionResponse`](#v2approvepromotionresponse)
      - [`v2CachePromotionsResponse`](#v2cachepromotionsresponse)
      - [`v2CachePromotionsResponsePagination`](#v2cachepromotionsresponsepagination)
      - [`v2CodeSetting`](#v2codesetting)
      - [`v2ConditionUsage`](#v2conditionusage)
      - [`v2CountPromotionsResponse`](#v2countpromotionsresponse)
      - [`v2CreatePromotionBody`](#v2createpromotionbody)
      - [`v2EndPromotionResponse`](#v2endpromotionresponse)
      - [`v2PostponePromotionResponse`](#v2postponepromotionresponse)
      - [`v2Promotion`](#v2promotion)
      - [`v2PromotionBelongTo`](#v2promotionbelongto)
      - [`v2PromotionBelongToType`](#v2promotionbelongtotype)
      - [`v2PromotionKind`](#v2promotionkind)
      - [`v2PromotionMethod`](#v2promotionmethod)
      - [`v2PromotionStatus`](#v2promotionstatus)
      - [`v2PromotionType`](#v2promotiontype)
      - [`v2RejectPromotionResponse`](#v2rejectpromotionresponse)
      - [`v2RequestApprovePromotionResponse`](#v2requestapprovepromotionresponse)
      - [`v2ResumePromotionResponse`](#v2resumepromotionresponse)
      - [`v2SearchPromotionsRequestEqual`](#v2searchpromotionsrequestequal)
      - [`v2SearchPromotionsRequestFromBetween`](#v2searchpromotionsrequestfrombetween)
      - [`v2SearchPromotionsRequestLike`](#v2searchpromotionsrequestlike)
      - [`v2SearchPromotionsRequestToBetween`](#v2searchpromotionsrequesttobetween)
      - [`v2SearchPromotionsResponse`](#v2searchpromotionsresponse)
      - [`v2SearchPromotionsResponsePagination`](#v2searchpromotionsresponsepagination)
      - [`ContentEvent`](#contentevent-1)
      - [`protobufAny`](#protobufany)
      - [`v2Content`](#v2content)
      - [`v2CreateContentsResponse`](#v2createcontentsresponse)
      - [`v2Target`](#v2target)
      - [`ConditionUsageMaxTimesPerPerson`](#conditionusagemaxtimesperperson-1)
      - [`ConditionUsageMaxTimesPerPersonPerTime`](#conditionusagemaxtimesperpersonpertime-1)
      - [`ConditionUsageMaxTimesUsage`](#conditionusagemaxtimesusage-1)
      - [`MaxTimesPerPersonPerTimeTimeType`](#maxtimesperpersonpertimetimetype-1)
      - [`v2ConditionUsage`](#v2conditionusage-1)
      - [`v2CreateConditionUsageResponse`](#v2createconditionusageresponse)
      - [`CodeSettingCodeType`](#codesettingcodetype-1)
      - [`CodeSettingTypeCode`](#codesettingtypecode-1)
      - [`promotionv2MaxTimes`](#promotionv2maxtimes-1)
      - [`v2CodeSetting`](#v2codesetting-1)
      - [`v2CountCodesRequestCodeStatus`](#v2countcodesrequestcodestatus)
      - [`v2CountCodesResponse`](#v2countcodesresponse)
      - [`ApplyInfoAttachProduct`](#applyinfoattachproduct)
      - [`HowToLoadHowToChoose`](#howtoloadhowtochoose)
      - [`HowToLoadTypeLoad`](#howtoloadtypeload)
      - [`googlerpcStatus`](#googlerpcstatus-1)
      - [`integratev2Product`](#integratev2product)
      - [`v2ApplyInfo`](#v2applyinfo)
      - [`v2ApplyPromotionRequest`](#v2applypromotionrequest)
      - [`v2ApplyPromotionRequestOrder`](#v2applypromotionrequestorder)
      - [`v2ApplyPromotionRequestOrderProduct`](#v2applypromotionrequestorderproduct)
      - [`v2ApplyPromotionResponse`](#v2applypromotionresponse)
      - [`v2ApplyPromotionResponseOrder`](#v2applypromotionresponseorder)
      - [`v2ApplyPromotionResponseOrderProduct`](#v2applypromotionresponseorderproduct)
      - [`v2ApplyTransactionStatus`](#v2applytransactionstatus)
      - [`v2CheckApplyPromotionRequest`](#v2checkapplypromotionrequest)
      - [`v2CheckApplyPromotionRequestOrder`](#v2checkapplypromotionrequestorder)
      - [`v2CheckApplyPromotionRequestOrderProduct`](#v2checkapplypromotionrequestorderproduct)
      - [`v2CheckApplyPromotionResponse`](#v2checkapplypromotionresponse)
      - [`v2CheckApplyPromotionResponseOrder`](#v2checkapplypromotionresponseorder)
      - [`v2CheckApplyPromotionResponseOrderProduct`](#v2checkapplypromotionresponseorderproduct)
      - [`v2CheckApplyPromotionResponseStatus`](#v2checkapplypromotionresponsestatus)
      - [`v2CheckVoucherCodeIsValidRequest`](#v2checkvouchercodeisvalidrequest)
      - [`v2CheckVoucherCodeIsValidRequestOrder`](#v2checkvouchercodeisvalidrequestorder)
      - [`v2CheckVoucherCodeIsValidRequestOrderProduct`](#v2checkvouchercodeisvalidrequestorderproduct)
      - [`v2CheckVoucherCodeIsValidResponse`](#v2checkvouchercodeisvalidresponse)
      - [`v2CheckVoucherCodeIsValidResponseOrder`](#v2checkvouchercodeisvalidresponseorder)
      - [`v2Code`](#v2code)
      - [`v2CommitApplyPromotionRequest`](#v2commitapplypromotionrequest)
      - [`v2CommitApplyPromotionResponse`](#v2commitapplypromotionresponse)
      - [`v2HowToLoad`](#v2howtoload)
      - [`v2ListPromotionsRequest`](#v2listpromotionsrequest)
      - [`v2ListPromotionsRequestOrder`](#v2listpromotionsrequestorder)
      - [`v2ListPromotionsRequestOrderProduct`](#v2listpromotionsrequestorderproduct)
      - [`v2ListPromotionsResponse`](#v2listpromotionsresponse)
      - [`v2ListPromotionsResponseOrder`](#v2listpromotionsresponseorder)
      - [`v2ListPromotionsResponseOrderProduct`](#v2listpromotionsresponseorderproduct)
      - [`v2Promotion`](#v2promotion-1)
      - [`v2PromotionAction`](#v2promotionaction)
      - [`v2PromotionMethod`](#v2promotionmethod-1)
      - [`v2PromotionType`](#v2promotiontype-1)
      - [`v2RevertApplyPromotionRequest`](#v2revertapplypromotionrequest)
      - [`v2RevertApplyPromotionResponse`](#v2revertapplypromotionresponse)
      - [`v2Transaction`](#v2transaction)
      - [`v2TransactionApply`](#v2transactionapply)
      - [`v2TransactionStatus`](#v2transactionstatus)
      - [`v2VoucherCode`](#v2vouchercode)
      - [`ApplyInfoAttachProduct`](#applyinfoattachproduct-1)
      - [`HowToLoadHowToChoose`](#howtoloadhowtochoose-1)
      - [`HowToLoadTypeLoad`](#howtoloadtypeload-1)
      - [`ListPromotionsByTypesResponsePromotionsByType`](#listpromotionsbytypesresponsepromotionsbytype)
      - [`PropertyTypeProperty`](#propertytypeproperty)
      - [`combinev1Product`](#combinev1product)
      - [`combinev1PromotionType`](#combinev1promotiontype)
      - [`googlerpcStatus`](#googlerpcstatus-2)
      - [`protobufAny`](#protobufany-1)
      - [`v1ApplyContent`](#v1applycontent)
      - [`v1ApplyInfo`](#v1applyinfo)
      - [`v1ApplyPromotionRequest`](#v1applypromotionrequest)
      - [`v1ApplyPromotionRequestOrder`](#v1applypromotionrequestorder)
      - [`v1ApplyPromotionRequestOrderProduct`](#v1applypromotionrequestorderproduct)
      - [`v1ApplyPromotionResponse`](#v1applypromotionresponse)
      - [`v1ApplyPromotionResponseOrder`](#v1applypromotionresponseorder)
      - [`v1ApplyPromotionResponseOrderProduct`](#v1applypromotionresponseorderproduct)
      - [`v1ApplyTransactionStatus`](#v1applytransactionstatus)
      - [`v1CheckApplyPromotionRequest`](#v1checkapplypromotionrequest)
      - [`v1CheckApplyPromotionRequestOrder`](#v1checkapplypromotionrequestorder)
      - [`v1CheckApplyPromotionRequestOrderProduct`](#v1checkapplypromotionrequestorderproduct)
      - [`v1CheckApplyPromotionResponse`](#v1checkapplypromotionresponse)
      - [`v1CheckApplyPromotionResponseOrder`](#v1checkapplypromotionresponseorder)
      - [`v1CheckApplyPromotionResponseOrderProduct`](#v1checkapplypromotionresponseorderproduct)
      - [`v1CheckApplyPromotionResponseStatus`](#v1checkapplypromotionresponsestatus)
      - [`v1CheckVoucherCodeIsValidRequest`](#v1checkvouchercodeisvalidrequest)
      - [`v1CheckVoucherCodeIsValidRequestOrder`](#v1checkvouchercodeisvalidrequestorder)
      - [`v1CheckVoucherCodeIsValidRequestOrderProduct`](#v1checkvouchercodeisvalidrequestorderproduct)
      - [`v1CheckVoucherCodeIsValidResponse`](#v1checkvouchercodeisvalidresponse)
      - [`v1CheckVoucherCodeIsValidResponseOrder`](#v1checkvouchercodeisvalidresponseorder)
      - [`v1Code`](#v1code)
      - [`v1CommitApplyPromotionRequest`](#v1commitapplypromotionrequest)
      - [`v1CommitApplyPromotionResponse`](#v1commitapplypromotionresponse)
      - [`v1HowToLoad`](#v1howtoload)
      - [`v1ListPromotionsByTypesRequest`](#v1listpromotionsbytypesrequest)
      - [`v1ListPromotionsByTypesResponse`](#v1listpromotionsbytypesresponse)
      - [`v1ListPromotionsRequest`](#v1listpromotionsrequest)
      - [`v1ListPromotionsRequestOrder`](#v1listpromotionsrequestorder)
      - [`v1ListPromotionsRequestOrderProduct`](#v1listpromotionsrequestorderproduct)
      - [`v1ListPromotionsResponse`](#v1listpromotionsresponse)
      - [`v1ListPromotionsResponseOrder`](#v1listpromotionsresponseorder)
      - [`v1ListPromotionsResponseOrderProduct`](#v1listpromotionsresponseorderproduct)
      - [`v1Promotion`](#v1promotion)
      - [`v1PromotionAction`](#v1promotionaction)
      - [`v1PromotionError`](#v1promotionerror)
      - [`v1PromotionMethod`](#v1promotionmethod)
      - [`v1PropertyType`](#v1propertytype)
      - [`v1PropertyTypePromotionType`](#v1propertytypepromotiontype)
      - [`v1RevertApplyPromotionRequest`](#v1revertapplypromotionrequest)
      - [`v1RevertApplyPromotionResponse`](#v1revertapplypromotionresponse)
      - [`v1Transaction`](#v1transaction)
      - [`v1TransactionApply`](#v1transactionapply)
      - [`v1TransactionStatus`](#v1transactionstatus)
      - [`v1VoucherCode`](#v1vouchercode)

## Promotion:
 ### Miêu tả 
  - Giải quyết business chính của cả project promotion
 ### Struct data

  | fields                 | type                    | descriptions                                |
  | :--------------------- | :---------------------- | :------------------------------------------ |
  | id                     | string                  | định danh chương trình                      |
  | detail_name            | string                  | Tên chi tiết của ctkm  không hiển thị app   |
  | start_time             | Timestamp               | thời gian ctkm chạy                         |
  | expire_time            | Timestamp               | thời gian ctkm kết thúc                     |
  | type                   | `PromotionType`         | config cho ctkm thuộc loại gì               |
  | name                   | string                  | Tên sẽ được hiển thị trên ứng dụng đặt hàng |
  | status                 | `PromotionStatus`       | Trạng thái của ct                           |
  | method                 | `PromotionMethod`       | Loại của ctkm                               |
  | creator                | string                  |                                             |
  | create_time            | Timestamp               |                                             |
  | update_time            | Timestamp               |                                             |
  | condition              | `ConditionEntity`       | dùng trong v1                               |
  | action                 | `ActionEntity`          | dùng trong v1                               |
  | target                 | `TargetEntity`          | dùng trong v1                               |
  | reason_reject          | string                  | Nêu lý do reject ctkm                       |
  | company_id             | string                  | dùng trong v1                               |
  | code_setting           | `CodeSettingEntity`     | xem phần ghi chú                            |
  | reason_postpone        | string                  |                                             |
  | content                | string                  | dùng trong v1                               |
  | usage_agents           | string[]                | dùng nội bộ                                 |
  | number_of_use          | number                  | dùng nội bộ                                 |
  | description            | string                  |                                             |
  | detail                 | string                  | dùng nội bộ                                 |
  | is_of_vendor           | boolean                 | dùng trong v1                               |
  | vendor_name            | string                  | dùng trong v1                               |
  | channels               | string[]                |                                             |
  | groups                 | string[]                | dùng trong v1                               |
  | contents               | `ContentEntity`[]       | nơi thiết lập gói khuyến mãi                |
  | priority               | number                  | độ ưu tiên                                  |
  | branch_name            | string                  | dùng trong v1                               |
  | condition_usage        | `ConditionUsageEntity`  | điều kiện sử dụng                           |
  | targets                | any                     | đối tượng sử dụng                           |
  | gifts                  | `GiftProduct`[]         | lưu quà                                     |
  | kind                   | kind: `PromotionKind`;  | thiết lập chương trình theo loại            |
  | attach_products_groups | `AttachProductGroups`[] | dùng nội bộ                                 |
  | rulesEngines           | `RulesEntity`           | tdùng nội bộ                                |
  | method_apply_content   | `ApplyContent`          |                                             |

 - Ghi chú: 
  - PromotionType: 
     + `APPLY_FOR_CART`: Áp dụng trên giỏ hàng
     + `APPLY_FOR_ORDER`: Áp dụng trên đơn hàng
     + `APPLY_FOR_PRODUCT`: Áp dụng trên sản phẩm
  - PromotionStatus:
     + `INIT`: Khởi tạo
     + `WAITING_FOR_APPROVAL`: Đang chờ duyệt
     + `REJECT`: Từ chối
     + `UP_COMMING`: Sắp diễn ra
     + `HAPPENING`: Đang diễn ra
     + `END`: Kết thúc
     + `POSTPONE`: Tạm ngưng
     + `INACTIVE`: Không hoạt động
  - PromotionMethod:
     + `TOTAL_DISCOUNT_PER_CART`: Giảm giá trên giỏ hàng
     + `ATTACH_PRODUCTS_TO_CART`: Tặng kèm sản phẩm theo giỏ hàng
     + `DISCOUNTS_FOR_SPECIFIED_PRODUCTS`: Giảm giá theo sản phẩm chỉ định
     + `ATTACH_PRODUCTS_TO_PRODUCT`: Tặng kèm/Mua kèm sản phẩm
     + `REDUCE_SHIPPING_FEE`: Giảm phí vận chuyển
     + `TOTAL_DISCOUNT_PER_ORDER`: Giảm giá trên đơn hàng
     + `ATTACH_PRODUCTS_TO_ORDER`: Tặng kèm sản phẩm theo đơn hàng
     + `CASHBACK_TOTAL_PER_CART`: Hoàn tiền trên giỏ hàng
     + `CASHBACK_TOTAL_PER_ORDER`: Hoàn tiền trên đơn hàng
     + `ATTACH_PRODUCTS_AS_PERCENTAGE_OF_THE_ORDER_VALUE`: Tặng x % giá trị  bằng sản phẩm tùy ý
     + `ATTACH_PRODUCTS_BY_MULTIPE`: Tặng kèm sản phẩm theo bội số
     + `ATTACH_IN_PRODUCTS`: Tặng kèm sản phẩm trong danh sách
     + `DISCOUNT_MULTIPE_PER_ORDER`: Giảm giá bội số trên đơn hàng
  - ContentEntity: Chứa thông tin điều kiện ctkm cần thiết lập
  - ApplyContent: Hình thức ctkm được áp dụng gói khuyến mãi như thế nào(Loại trừ, cộng dồn, bậc thang)
  - RulesEntity:
  - AttachProductGroups:
  - PromotionKind:
  - ContentEntity:
  - CodeSettingEntity:
  - TargetEntity:
  - ConditionEntity:
  - ActionEntity:
  - 
  -------------------------------------------
# Promotion Api
  
### `/v2/promotions`
#### `POST`
##### `Summary`:

Cho phép người dùng thêm mới 1 chương trình khuyến mãi
Cho phép người dùng nhân bản khuyến mãi
##### `Parameters`

| Name | Located in | Description | Required | Schema                                          |
| ---- | ---------- | ----------- | -------- | ----------------------------------------------- |
| body | body       |             | Yes      | [v2CreatePromotionBody](#v2CreatePromotionBody) |

##### `Responses`

| Code    | Description                   | Schema                              |
| ------- | ----------------------------- | ----------------------------------- |
| 200     | A successful response.        | [v2Promotion](#v2Promotion)         |
| default | An unexpected error response. | [googlerpcStatus](#googlerpcStatus) |

### `/v2/promotions/{promotion_id}`

#### `GET`
##### `Summary`:

Cho phép người dùng lấy thông tin chi tiết của CTKM
[admin,admin_lead]

##### `Parameters`

| Name         | Located in | Description | Required | Schema |
| ------------ | ---------- | ----------- | -------- | ------ |
| promotion_id | path       |             | Yes      | string |

##### `Responses`

| Code    | Description                   | Schema                              |
| ------- | ----------------------------- | ----------------------------------- |
| 200     | A successful response.        | [v2Promotion](#v2Promotion)         |
| default | An unexpected error response. | [googlerpcStatus](#googlerpcStatus) |

#### `DELETE`
##### `Summary`:

Cho phép người dùng xóa chương trình khuyến mãi
[admin]

##### `Parameters`

| Name         | Located in | Description | Required | Schema |
| ------------ | ---------- | ----------- | -------- | ------ |
| promotion_id | path       |             | Yes      | string |

##### `Responses`

| Code    | Description                   | Schema                              |
| ------- | ----------------------------- | ----------------------------------- |
| 200     | A successful response.        |                                     |
| default | An unexpected error response. | [googlerpcStatus](#googlerpcStatus) |

#### `PATCH`
##### `Summary`:

Cho phép người dùng cập nhật chương trình khuyến mãi
[admin]

##### `Parameters`

| Name                           | Located in | Description | Required | Schema                                          |
| ------------------------------ | ---------- | ----------- | -------- | ----------------------------------------------- |
| promotion_id                   | path       |             | Yes      | string                                          |
| body                           | body       |             | Yes      | [v2CreatePromotionBody](#v2CreatePromotionBody) |
| __update_field_mask__promotion | query      |             | No       | string                                          |

##### `Responses`

| Code    | Description                   | Schema                              |
| ------- | ----------------------------- | ----------------------------------- |
| 200     | A successful response.        | [v2Promotion](#v2Promotion)         |
| default | An unexpected error response. | [googlerpcStatus](#googlerpcStatus) |

### `/v2/promotions:approve/{promotion_id}`

#### `POST`
##### `Summary`:

Cho phép người dùng phê duyệt chương trình khuyến mãi 
[admin_lead]

##### `Parameters`

| Name         | Located in | Description | Required | Schema |
| ------------ | ---------- | ----------- | -------- | ------ |
| promotion_id | path       |             | Yes      | string |

##### `Responses`

| Code    | Description                   | Schema                                                    |
| ------- | ----------------------------- | --------------------------------------------------------- |
| 200     | A successful response.        | [v2ApprovePromotionResponse](#v2ApprovePromotionResponse) |
| default | An unexpected error response. | [googlerpcStatus](#googlerpcStatus)                       |

### `/v2/promotions:count`

#### `GET`
##### `Summary`:

Cho phép người dùng đếm số lượng chương trình khuyến mãi theo trạng thái
[admin]

##### `Parameters`

| Name                     | Located in | Description | Required | Schema   |
| ------------------------ | ---------- | ----------- | -------- | -------- |
| equal.status             | query      |             | No       | string   |
| equal.type               | query      |             | No       | string   |
| equal.kind               | query      |             | No       | string   |
| like.name_or_id          | query      |             | No       | string   |
| like.creator             | query      |             | No       | string   |
| like.supplier_or_vendor  | query      |             | No       | string   |
| from_between.start_time  | query      |             | No       | dateTime |
| from_between.expire_time | query      |             | No       | dateTime |
| to_between.start_time    | query      |             | No       | dateTime |
| to_between.expire_time   | query      |             | No       | dateTime |
| page_number              | query      |             | No       | integer  |
| page_size                | query      |             | No       | integer  |
| order_by                 | query      |             | No       | string   |

##### `Responses`

| Code    | Description                   | Schema                                                  |
| ------- | ----------------------------- | ------------------------------------------------------- |
| 200     | A successful response.        | [v2CountPromotionsResponse](#v2CountPromotionsResponse) |
| default | An unexpected error response. | [googlerpcStatus](#googlerpcStatus)                     |

### `/v2/promotions:end/{promotion_id}`

#### `POST`
##### `Summary`:

Cho phép người dùng bắt đầu lại chương trình khuyến mãi
[admin,admin_lead]

##### `Parameters`

| Name         | Located in | Description | Required | Schema |
| ------------ | ---------- | ----------- | -------- | ------ |
| promotion_id | path       |             | Yes      | string |

##### `Responses`

| Code    | Description                   | Schema                                            |
| ------- | ----------------------------- | ------------------------------------------------- |
| 200     | A successful response.        | [v2EndPromotionResponse](#v2EndPromotionResponse) |
| default | An unexpected error response. | [googlerpcStatus](#googlerpcStatus)               |

### `/v2/promotions:postpone/{promotion_id}`

#### `POST`
##### `Summary`:

Cho phép người dừng tạm ngưng chương trình khuyến mãi
[admin,admin_lead]

##### `Parameters`

| Name         | Located in | Description | Required | Schema |
| ------------ | ---------- | ----------- | -------- | ------ |
| promotion_id | path       |             | Yes      | string |
| body         | body       |             | Yes      | object |

##### `Responses`

| Code    | Description                   | Schema                                                      |
| ------- | ----------------------------- | ----------------------------------------------------------- |
| 200     | A successful response.        | [v2PostponePromotionResponse](#v2PostponePromotionResponse) |
| default | An unexpected error response. | [googlerpcStatus](#googlerpcStatus)                         |

### `/v2/promotions:reject/{promotion_id}`

#### `POST`
##### `Summary`:

Cho phép người dùng từ chối chương trình khuyến mãi 
[admin_lead]

##### `Parameters`

| Name         | Located in | Description | Required | Schema |
| ------------ | ---------- | ----------- | -------- | ------ |
| promotion_id | path       |             | Yes      | string |
| body         | body       |             | Yes      | object |

##### `Responses`

| Code    | Description                   | Schema                                                  |
| ------- | ----------------------------- | ------------------------------------------------------- |
| 200     | A successful response.        | [v2RejectPromotionResponse](#v2RejectPromotionResponse) |
| default | An unexpected error response. | [googlerpcStatus](#googlerpcStatus)                     |

### `/v2/promotions:request_approve/{promotion_id}`

#### `POST`
##### `Summary`:

Cho phép người dùng gửi yêu cầu approve promotion
[admin]

##### `Parameters`

| Name         | Located in | Description | Required | Schema |
| ------------ | ---------- | ----------- | -------- | ------ |
| promotion_id | path       |             | Yes      | string |
| body         | body       |             | Yes      | object |

##### `Responses`

| Code    | Description                   | Schema                                                                  |
| ------- | ----------------------------- | ----------------------------------------------------------------------- |
| 200     | A successful response.        | [v2RequestApprovePromotionResponse](#v2RequestApprovePromotionResponse) |
| default | An unexpected error response. | [googlerpcStatus](#googlerpcStatus)                                     |

### `/v2/promotions:resume/{promotion_id}`

#### `POST`
##### `Summary`:

Cho phép người dùng bắt đầu lại chương trình khuyến mãi
[admin,admin_lead]

##### `Parameters`

| Name         | Located in | Description | Required | Schema |
| ------------ | ---------- | ----------- | -------- | ------ |
| promotion_id | path       |             | Yes      | string |

##### `Responses`

| Code    | Description                   | Schema                                                  |
| ------- | ----------------------------- | ------------------------------------------------------- |
| 200     | A successful response.        | [v2ResumePromotionResponse](#v2ResumePromotionResponse) |
| default | An unexpected error response. | [googlerpcStatus](#googlerpcStatus)                     |

### `/v2/promotions:search`

#### `GET`
##### `Summary`:

Cho phép người dùng tìm kiếm chương trình khuyến mãi theo các điều kiện 
[admin, admin_lead]

##### `Parameters`

| Name                     | Located in | Description | Required | Schema   |
| ------------------------ | ---------- | ----------- | -------- | -------- |
| equal.status             | query      |             | No       | string   |
| equal.type               | query      |             | No       | string   |
| equal.kind               | query      |             | No       | string   |
| like.name_or_id          | query      |             | No       | string   |
| like.creator             | query      |             | No       | string   |
| like.supplier_or_vendor  | query      |             | No       | string   |
| from_between.start_time  | query      |             | No       | dateTime |
| from_between.expire_time | query      |             | No       | dateTime |
| to_between.start_time    | query      |             | No       | dateTime |
| to_between.expire_time   | query      |             | No       | dateTime |
| page_number              | query      |             | No       | integer  |
| page_size                | query      |             | No       | integer  |
| order_by                 | query      |             | No       | string   |

##### `Responses`

| Code    | Description                   | Schema                                                    |
| ------- | ----------------------------- | --------------------------------------------------------- |
| 200     | A successful response.        | [v2SearchPromotionsResponse](#v2SearchPromotionsResponse) |
| default | An unexpected error response. | [googlerpcStatus](#googlerpcStatus)                       |



### `/v2/promotions/{promotion_id}/contents`

#### `POST`
##### `Summary`:
Cho phép người dùng tạo các gói khuyến mãi
##### `Parameters`

| Name         | Located in | Description | Required | Schema                  |
| ------------ | ---------- | ----------- | -------- | ----------------------- |
| promotion_id | path       |             | Yes      | string                  |
| body         | body       |             | Yes      | [v2Content](#v2content) |

##### `Responses`

| Code    | Description                   | Schema                                                |
| ------- | ----------------------------- | ----------------------------------------------------- |
| 200     | A successful response.        | [v2CreateContentsResponse](#v2CreateContentsResponse) |
| default | An unexpected error response. | [googlerpcStatus](#googlerpcStatus)                   |

#### `PUT`
##### `Summary`:
Cho phép người dùng cập nhật các gói khuyến mãi, lưu ý mỗi lần cập nhật thì cập nhật lại toàn bộ gói khuyến mãi
##### `Parameters`

| Name         | Located in | Description | Required | Schema                  |
| ------------ | ---------- | ----------- | -------- | ----------------------- |
| promotion_id | path       |             | Yes      | string                  |
| body         | body       |             | Yes      | [v2Content](#v2content) |

##### `Responses`

| Code    | Description                   | Schema                                                |
| ------- | ----------------------------- | ----------------------------------------------------- |
| 200     | A successful response.        | [v2CreateContentsResponse](#v2CreateContentsResponse) |
| default | An unexpected error response. | [googlerpcStatus](#googlerpcStatus)                   |


### `/v2/promotions/{promotion_id}/targets`

#### `POST`
##### `Parameters`

| Name         | Located in | Description | Required | Schema |
| ------------ | ---------- | ----------- | -------- | ------ |
| promotion_id | path       |             | Yes      | string |
| body         | body       |             | Yes      | object |

##### `Responses`

| Code    | Description                   | Schema                              |
| ------- | ----------------------------- | ----------------------------------- |
| 200     | A successful response.        | [v2Target](#v2Target)               |
| default | An unexpected error response. | [googlerpcStatus](#googlerpcStatus) |

#### `PUT`
##### `Parameters`

| Name         | Located in | Description | Required | Schema |
| ------------ | ---------- | ----------- | -------- | ------ |
| promotion_id | path       |             | Yes      | string |
| body         | body       |             | Yes      | object |

##### `Responses`

| Code    | Description                   | Schema                              |
| ------- | ----------------------------- | ----------------------------------- |
| 200     | A successful response.        | [v2Target](#v2Target)               |
| default | An unexpected error response. | [googlerpcStatus](#googlerpcStatus) |

---------------------------------------

### `/v2/promotions/{promotion_id}/condition-usages`

#### `POST`
##### `Parameters`

| Name         | Located in | Description | Required | Schema                                |
| ------------ | ---------- | ----------- | -------- | ------------------------------------- |
| promotion_id | path       |             | Yes      | string                                |
| body         | body       |             | Yes      | [v2ConditionUsage](#v2ConditionUsage) |

##### `Responses`

| Code    | Description                   | Schema                                                            |
| ------- | ----------------------------- | ----------------------------------------------------------------- |
| 200     | A successful response.        | [v2CreateConditionUsageResponse](#v2CreateConditionUsageResponse) |
| default | An unexpected error response. | [googlerpcStatus](#googlerpcStatus)                               |


### `/promotions/{promotion_id}/code-settings`

#### `GET`
##### `Summary`:

Cho phép người dùng cấu nhận cấu hình mà khuyến

##### `Parameters`

| Name         | Located in | Description | Required | Schema |
| ------------ | ---------- | ----------- | -------- | ------ |
| promotion_id | path       |             | Yes      | string |

##### `Responses`

| Code    | Description                   | Schema                              |
| ------- | ----------------------------- | ----------------------------------- |
| 200     | A successful response.        | [v2CodeSetting](#v2CodeSetting)     |
| default | An unexpected error response. | [googlerpcStatus](#googlerpcStatus) |

### `/v2/codes:count`

#### `GET`
##### `Summary`:

Cho phép người dùng đếm số lượng các mã khuyến mãi theo trạng thái

##### `Parameters`

| Name   | Located in | Description | Required | Schema |
| ------ | ---------- | ----------- | -------- | ------ |
| status | query      |             | No       | string |

##### `Responses`

| Code    | Description                   | Schema                                        |
| ------- | ----------------------------- | --------------------------------------------- |
| 200     | A successful response.        | [v2CountCodesResponse](#v2CountCodesResponse) |
| default | An unexpected error response. | [googlerpcStatus](#googlerpcStatus)           |

### `/v2/promotions/{promotion_id}/code-setting`

#### `POST`
##### `Summary`:

Cho phép người dùng cấu hình mã khuyến mãi cho chương trình khuyến mãi

##### `Parameters`

| Name         | Located in | Description | Required | Schema                          |
| ------------ | ---------- | ----------- | -------- | ------------------------------- |
| promotion_id | path       |             | Yes      | string                          |
| body         | body       |             | Yes      | [v2CodeSetting](#v2CodeSetting) |

##### `Responses`

| Code    | Description                   | Schema                              |
| ------- | ----------------------------- | ----------------------------------- |
| 200     | A successful response.        | [v2CodeSetting](#v2CodeSetting)     |
| default | An unexpected error response. | [googlerpcStatus](#googlerpcStatus) |

### `/v2/promotions/{promotion_id}/code-settings`

#### `PATCH`
##### `Summary`:

Cho phép người dùng cập nhật cấu hình khuyến mãi cho chương trình khuyến mãi

##### `Parameters`

| Name                              | Located in | Description | Required | Schema                          |
| --------------------------------- | ---------- | ----------- | -------- | ------------------------------- |
| promotion_id                      | path       |             | Yes      | string                          |
| body                              | body       |             | Yes      | [v2CodeSetting](#v2CodeSetting) |
| __update_field_mask__code_setting | query      |             | No       | string                          |

##### `Responses`

| Code    | Description                   | Schema                              |
| ------- | ----------------------------- | ----------------------------------- |
| 200     | A successful response.        | [v2CodeSetting](#v2CodeSetting)     |
| default | An unexpected error response. | [googlerpcStatus](#googlerpcStatus) |



### `/ecomv2/v2/promotions:apply-promotion`

#### `POST`
##### `Summary`:

Api integrate với bên Ecomv2, check là apply chương trình khuyến mãi theo cả 3 giỏ, đơn, sản phẩm 
##### `Parameters`

| Name | Located in | Description | Required | Schema |
| ---- | ---------- | ----------- | -------- | ---- |
| body | body |  | Yes | [v2ApplyPromotionRequest](#v2ApplyPromotionRequest) |

##### `Responses`

| Code | Description | Schema |
| ---- | ----------- | ------ |
| 200 | A successful response. | [v2ApplyPromotionResponse](#v2ApplyPromotionResponse) |
| default | An unexpected error response. | [googlerpcStatus](#googlerpcStatus) |

### `/ecomv2/v2/promotions:check-apply-promotion`

#### `POST`
##### `Summary`:

Api integrate với bên Ecomv2, check trước khi apply chương trình khuyến mãi theo cả 3 giỏ, đơn, sản phẩm , `hiện chưa dùng đến`
##### `Parameters`

| Name | Located in | Description | Required | Schema |
| ---- | ---------- | ----------- | -------- | ---- |
| body | body |  | Yes | [v2CheckApplyPromotionRequest](#v2CheckApplyPromotionRequest) |

##### `Responses`

| Code | Description | Schema |
| ---- | ----------- | ------ |
| 200 | A successful response. | [v2CheckApplyPromotionResponse](#v2CheckApplyPromotionResponse) |
| default | An unexpected error response. | [googlerpcStatus](#googlerpcStatus) |

### `/ecomv2/v2/promotions:check-voucher-code-is-valid`

#### `POST`
##### `Summary`:

Kiểm tra mã code có hợp lệ hay không
Lấy thông tin của chương trình khuyến mãi từ voucher code, chỉ dùng trong v1

##### `Parameters`

| Name | Located in | Description | Required | Schema |
| ---- | ---------- | ----------- | -------- | ---- |
| body | body |  | Yes | [v2CheckVoucherCodeIsValidRequest](#v2CheckVoucherCodeIsValidRequest) |

##### `Responses`

| Code | Description | Schema |
| ---- | ----------- | ------ |
| 200 | A successful response. | [v2CheckVoucherCodeIsValidResponse](#v2CheckVoucherCodeIsValidResponse) |
| default | An unexpected error response. | [googlerpcStatus](#googlerpcStatus) |

### `/ecomv2/v2/promotions:commit-apply-promotion`

#### `POST`
##### `Summary`:
Api integrate với bên Ecomv2, khi bên integrate đã tạo hoàn thành apply ctkm mà không phát sinh bất kỳ lỗi gì, thì gọi để xác nhận với promotion là đã hoàn thành ctkm
##### `Parameters`

| Name | Located in | Description | Required | Schema |
| ---- | ---------- | ----------- | -------- | ---- |
| body | body |  | Yes | [v2CommitApplyPromotionRequest](#v2CommitApplyPromotionRequest) |

##### `Responses`

| Code | Description | Schema |
| ---- | ----------- | ------ |
| 200 | A successful response. | [v2CommitApplyPromotionResponse](#v2CommitApplyPromotionResponse) |
| default | An unexpected error response. | [googlerpcStatus](#googlerpcStatus) |

### `/ecomv2/v2/promotions:list-promotions`

#### `POST`
##### `Summary`:

Stage 1: Lấy danh sách các chương trình khuyến mãi, function chính cho bên tích hợp

##### `Parameters`

| Name | Located in | Description | Required | Schema |
| ---- | ---------- | ----------- | -------- | ---- |
| body | body |  | Yes | [v2ListPromotionsRequest](#v2ListPromotionsRequest) |

##### `Responses`

| Code | Description | Schema |
| ---- | ----------- | ------ |
| 200 | A successful response. | [v2ListPromotionsResponse](#v2ListPromotionsResponse) |
| default | An unexpected error response. | [googlerpcStatus](#googlerpcStatus) |

### `/ecomv2/v2/promotions:revert-apply-promotion`

#### `POST`
##### `Summary`:

khi hủy đơn hàng, phải hoàn lại tất cả khuyến mãi đã dùng cho đơn đó

##### `Parameters`

| Name | Located in | Description | Required | Schema |
| ---- | ---------- | ----------- | -------- | ---- |
| body | body |  | Yes | [v2RevertApplyPromotionRequest](#v2RevertApplyPromotionRequest) |

##### `Responses`

| Code | Description | Schema |
| ---- | ----------- | ------ |
| 200 | A successful response. | [v2RevertApplyPromotionResponse](#v2RevertApplyPromotionResponse) |
| default | An unexpected error response. | [googlerpcStatus](#googlerpcStatus) |

### `/saleman/v2/promotions:list-promotions`

#### `POST`
##### `Summary`:

Stage 1: Lấy danh sách các chương trình khuyến mãi

##### `Parameters`

| Name | Located in | Description | Required | Schema |
| ---- | ---------- | ----------- | -------- | ---- |
| body | body |  | Yes | [v2ListPromotionsRequest](#v2ListPromotionsRequest) |

##### `Responses`

| Code | Description | Schema |
| ---- | ----------- | ------ |
| 200 | A successful response. | [v2ListPromotionsResponse](#v2ListPromotionsResponse) |
| default | An unexpected error response. | [googlerpcStatus](#googlerpcStatus) |


### `/v1/combines/promotions:apply-promotion`

#### `POST`
##### `Summary`:
tương tự như function trên
##### `Parameters`

| Name | Located in | Description | Required | Schema |
| ---- | ---------- | ----------- | -------- | ---- |
| body | body |  | Yes | [v1ApplyPromotionRequest](#v1ApplyPromotionRequest) |

##### `Responses`

| Code | Description | Schema |
| ---- | ----------- | ------ |
| 200 | A successful response. | [v1ApplyPromotionResponse](#v1ApplyPromotionResponse) |
| default | An unexpected error response. | [googlerpcStatus](#googlerpcStatus) |

### `/v1/combines/promotions:check-apply-promotion`

#### `POST`
##### `Parameters`

| Name | Located in | Description | Required | Schema |
| ---- | ---------- | ----------- | -------- | ---- |
| body | body |  | Yes | [v1CheckApplyPromotionRequest](#v1CheckApplyPromotionRequest) |

##### `Responses`

| Code | Description | Schema |
| ---- | ----------- | ------ |
| 200 | A successful response. | [v1CheckApplyPromotionResponse](#v1CheckApplyPromotionResponse) |
| default | An unexpected error response. | [googlerpcStatus](#googlerpcStatus) |

### `/v1/combines/promotions:check-voucher-code-is-valid`

#### `POST`
##### `Summary`:

Kiểm tra mã code có hợp lệ hay không
Lấy thông tin của chương trình khuyến mãi từ voucher code

##### `Parameters`

| Name | Located in | Description | Required | Schema |
| ---- | ---------- | ----------- | -------- | ---- |
| body | body |  | Yes | [v1CheckVoucherCodeIsValidRequest](#v1CheckVoucherCodeIsValidRequest) |

##### `Responses`

| Code | Description | Schema |
| ---- | ----------- | ------ |
| 200 | A successful response. | [v1CheckVoucherCodeIsValidResponse](#v1CheckVoucherCodeIsValidResponse) |
| default | An unexpected error response. | [googlerpcStatus](#googlerpcStatus) |

### `/v1/combines/promotions:commit-apply-promotio`n

#### `POST`
##### `Parameters`

| Name | Located in | Description | Required | Schema |
| ---- | ---------- | ----------- | -------- | ---- |
| body | body |  | Yes | [v1CommitApplyPromotionRequest](#v1CommitApplyPromotionRequest) |

##### `Responses`

| Code | Description | Schema |
| ---- | ----------- | ------ |
| 200 | A successful response. | [v1CommitApplyPromotionResponse](#v1CommitApplyPromotionResponse) |
| default | An unexpected error response. | [googlerpcStatus](#googlerpcStatus) |

### `/v1/combines/promotions:list-promotions`

#### `POST`
##### `Summary`:

Stage 1: Lấy danh sách các chương trình khuyến mãi

##### `Parameters`

| Name | Located in | Description | Required | Schema |
| ---- | ---------- | ----------- | -------- | ---- |
| body | body |  | Yes | [v1ListPromotionsRequest](#v1ListPromotionsRequest) |

##### `Responses`

| Code | Description | Schema |
| ---- | ----------- | ------ |
| 200 | A successful response. | [v1ListPromotionsResponse](#v1ListPromotionsResponse) |
| default | An unexpected error response. | [googlerpcStatus](#googlerpcStatus) |

### `/v1/combines/promotions:list-promotions-types`

#### `POST`
##### `Summary`:

Lấy danh sách các chương trình khuyến mãi của 1 NPP hoặc 1 thương hiệu / 1 ngành hàng

##### `Parameters`

| Name | Located in | Description | Required | Schema |
| ---- | ---------- | ----------- | -------- | ---- |
| body | body |  | Yes | [v1ListPromotionsByTypesRequest](#v1ListPromotionsByTypesRequest) |

##### `Responses`

| Code | Description | Schema |
| ---- | ----------- | ------ |
| 200 | A successful response. | [v1ListPromotionsByTypesResponse](#v1ListPromotionsByTypesResponse) |
| default | An unexpected error response. | [googlerpcStatus](#googlerpcStatus) |

### `/v1/combines/promotions:revert-apply-promotion`

#### `POST`
##### `Parameters`

| Name | Located in | Description | Required | Schema |
| ---- | ---------- | ----------- | -------- | ---- |
| body | body |  | Yes | [v1RevertApplyPromotionRequest](#v1RevertApplyPromotionRequest) |

##### `Responses`

| Code | Description | Schema |
| ---- | ----------- | ------ |
| 200 | A successful response. | [v1RevertApplyPromotionResponse](#v1RevertApplyPromotionResponse) |
| default | An unexpected error response. | [googlerpcStatus](#googlerpcStatus) |


### `Models`

#### `CodeSettingCodeType`

| Name                | Type   | Description | Required |
| ------------------- | ------ | ----------- | -------- |
| CodeSettingCodeType | string |             |          |

#### `CodeSettingTypeCode`

| Name                | Type   | Description | Required |
| ------------------- | ------ | ----------- | -------- |
| CodeSettingTypeCode | string |             |          |

#### `ConditionUsageMaxTimesPerPerson`

| Name     | Type    | Description | Required |
| -------- | ------- | ----------- | -------- |
| is_limit | boolean |             | No       |
| count    | integer |             | No       |

#### `ConditionUsageMaxTimesPerPersonPerTime`

| Name      | Type                                                                  | Description | Required |
| --------- | --------------------------------------------------------------------- | ----------- | -------- |
| is_limit  | boolean                                                               |             | No       |
| count     | integer                                                               |             | No       |
| time_type | [MaxTimesPerPersonPerTimeTimeType](#MaxTimesPerPersonPerTimeTimeType) |             | No       |

#### `ConditionUsageMaxTimesUsage`

| Name     | Type    | Description | Required |
| -------- | ------- | ----------- | -------- |
| is_limit | boolean |             | No       |
| count    | integer |             | No       |

#### `ContentEvent`

| Name   | Type   | Description | Required |
| ------ | ------ | ----------- | -------- |
| type   | string |             | No       |
| params | string |             | No       |

#### `MaxTimesPerPersonPerTimeTimeType`

| Name                             | Type   | Description | Required |
| -------------------------------- | ------ | ----------- | -------- |
| MaxTimesPerPersonPerTimeTimeType | string |             |          |

#### `googlerpcStatus`

| Name    | Type                            | Description | Required |
| ------- | ------------------------------- | ----------- | -------- |
| code    | integer                         |             | No       |
| message | string                          |             | No       |
| details | [ [protobufAny](#protobufAny) ] |             | No       |

#### `promotionv2MaxTimes`

| Name     | Type    | Description | Required |
| -------- | ------- | ----------- | -------- |
| is_limit | boolean |             | No       |
| count    | integer |             | No       |

#### `promotionv2Status`

| Name   | Type                                    | Description | Required |
| ------ | --------------------------------------- | ----------- | -------- |
| status | [v2PromotionStatus](#v2PromotionStatus) |             | No       |
| number | integer                                 |             | No       |

#### `v2ApprovePromotionResponse`

| Name   | Type                                    | Description | Required |
| ------ | --------------------------------------- | ----------- | -------- |
| status | [v2PromotionStatus](#v2PromotionStatus) |             | No       |

#### `v2CachePromotionsResponse`

| Name       | Type                                                                        | Description | Required |
| ---------- | --------------------------------------------------------------------------- | ----------- | -------- |
| promotions | [ [v2Promotion](#v2Promotion) ]                                             |             | No       |
| pagination | [v2CachePromotionsResponsePagination](#v2CachePromotionsResponsePagination) |             | No       |

#### `v2CachePromotionsResponsePagination`

| Name        | Type    | Description | Required |
| ----------- | ------- | ----------- | -------- |
| page_number | integer |             | No       |
| page_size   | integer |             | No       |
| total_size  | integer |             | No       |

#### `v2CodeSetting`

| Name                 | Type                                        | Description | Required |
| -------------------- | ------------------------------------------- | ----------- | -------- |
| is_use_code          | boolean                                     |             | No       |
| code_type            | [CodeSettingCodeType](#CodeSettingCodeType) |             | No       |
| max_times_per_person | [promotionv2MaxTimes](#promotionv2MaxTimes) |             | No       |
| count                | integer                                     |             | No       |
| max_times_per_code   | [promotionv2MaxTimes](#promotionv2MaxTimes) |             | No       |
| type                 | [CodeSettingTypeCode](#CodeSettingTypeCode) |             | No       |
| prefix               | string                                      |             | No       |
| postfix              | string                                      |             | No       |
| code_length          | integer                                     |             | No       |

#### `v2ConditionUsage`

| Name                          | Type                                                                              | Description | Required |
| ----------------------------- | --------------------------------------------------------------------------------- | ----------- | -------- |
| max_times_usage               | [ConditionUsageMaxTimesUsage](#ConditionUsageMaxTimesUsage)                       |             | No       |
| max_times_per_person          | [ConditionUsageMaxTimesPerPerson](#ConditionUsageMaxTimesPerPerson)               |             | No       |
| max_times_per_person_per_time | [ConditionUsageMaxTimesPerPersonPerTime](#ConditionUsageMaxTimesPerPersonPerTime) |             | No       |

#### `v2CountPromotionsResponse`

| Name     | Type                                        | Description | Required |
| -------- | ------------------------------------------- | ----------- | -------- |
| statuses | [ [promotionv2Status](#promotionv2Status) ] |             | No       |

#### `v2CreatePromotionBody`

| Name        | Type                                        | Description | Required |
| ----------- | ------------------------------------------- | ----------- | -------- |
| name        | string                                      |             | Yes      |
| detail_name | string                                      |             | Yes      |
| start_time  | dateTime                                    |             | Yes      |
| expire_time | dateTime                                    |             | Yes      |
| type        | [v2PromotionType](#v2PromotionType)         |             | No       |
| method      | [v2PromotionMethod](#v2PromotionMethod)     |             | No       |
| content     | string                                      |             | Yes      |
| description | string                                      |             | No       |
| detail      | string                                      |             | No       |
| channels    | [ string ]                                  |             | No       |
| priority    | integer                                     |             | No       |
| belong_to   | [v2PromotionBelongTo](#v2PromotionBelongTo) |             | No       |
| kind        | [v2PromotionKind](#v2PromotionKind)         |             | No       |

#### `v2EndPromotionResponse`

| Name   | Type                                    | Description | Required |
| ------ | --------------------------------------- | ----------- | -------- |
| status | [v2PromotionStatus](#v2PromotionStatus) |             | No       |

#### `v2PostponePromotionResponse`

| Name   | Type                                    | Description | Required |
| ------ | --------------------------------------- | ----------- | -------- |
| status | [v2PromotionStatus](#v2PromotionStatus) |             | No       |

#### `v2Promotion`

| Name            | Type                                        | Description | Required |
| --------------- | ------------------------------------------- | ----------- | -------- |
| id              | string                                      |             | No       |
| name            | string                                      |             | No       |
| start_time      | dateTime                                    |             | No       |
| expire_time     | dateTime                                    |             | No       |
| type            | [v2PromotionType](#v2PromotionType)         |             | No       |
| status          | [v2PromotionStatus](#v2PromotionStatus)     |             | No       |
| creator         | string                                      |             | No       |
| create_time     | dateTime                                    |             | No       |
| update_time     | dateTime                                    |             | No       |
| content         | string                                      |             | No       |
| description     | string                                      |             | No       |
| detail          | string                                      |             | No       |
| company_id      | string                                      |             | No       |
| vendor_name     | string                                      |             | No       |
| contents        | [ [v2Content](#v2Content) ]                 |             | No       |
| priority        | integer                                     |             | No       |
| method          | [v2PromotionMethod](#v2PromotionMethod)     |             | No       |
| condition_usage | [v2ConditionUsage](#v2ConditionUsage)       |             | No       |
| targets         | string                                      |             | No       |
| code_setting    | [v2CodeSetting](#v2CodeSetting)             |             | No       |
| belong_to       | [v2PromotionBelongTo](#v2PromotionBelongTo) |             | No       |
| channels        | [ string ]                                  |             | No       |
| kind            | [v2PromotionKind](#v2PromotionKind)         |             | No       |
| detail_name     | string                                      |             | No       |
| number_of_use   | integer                                     |             | No       |

#### `v2PromotionBelongTo`

| Name | Type                                                | Description | Required |
| ---- | --------------------------------------------------- | ----------- | -------- |
| name | string                                              |             | No       |
| type | [v2PromotionBelongToType](#v2PromotionBelongToType) |             | No       |
| id   | string                                              |             | No       |

#### `v2PromotionBelongToType`

| Name                    | Type   | Description | Required |
| ----------------------- | ------ | ----------- | -------- |
| v2PromotionBelongToType | string |             |          |

#### `v2PromotionKind`

| Name            | Type   | Description | Required |
| --------------- | ------ | ----------- | -------- |
| v2PromotionKind | string |             |          |

#### `v2PromotionMethod`

| Name              | Type   | Description | Required |
| ----------------- | ------ | ----------- | -------- |
| v2PromotionMethod | string |             |          |

#### `v2PromotionStatus`

| Name              | Type   | Description | Required |
| ----------------- | ------ | ----------- | -------- |
| v2PromotionStatus | string |             |          |

#### `v2PromotionType`

| Name            | Type   | Description | Required |
| --------------- | ------ | ----------- | -------- |
| v2PromotionType | string |             |          |

#### `v2RejectPromotionResponse`

| Name   | Type                                    | Description | Required |
| ------ | --------------------------------------- | ----------- | -------- |
| status | [v2PromotionStatus](#v2PromotionStatus) |             | No       |

#### `v2RequestApprovePromotionResponse`

| Name   | Type                                    | Description | Required |
| ------ | --------------------------------------- | ----------- | -------- |
| status | [v2PromotionStatus](#v2PromotionStatus) |             | No       |

#### `v2ResumePromotionResponse`

| Name   | Type                                    | Description | Required |
| ------ | --------------------------------------- | ----------- | -------- |
| status | [v2PromotionStatus](#v2PromotionStatus) |             | No       |

#### `v2SearchPromotionsRequestEqual`

| Name   | Type   | Description | Required |
| ------ | ------ | ----------- | -------- |
| status | string |             | No       |
| type   | string |             | No       |
| kind   | string |             | No       |

#### `v2SearchPromotionsRequestFromBetween`

| Name        | Type     | Description | Required |
| ----------- | -------- | ----------- | -------- |
| start_time  | dateTime |             | No       |
| expire_time | dateTime |             | No       |

#### `v2SearchPromotionsRequestLike`

| Name               | Type   | Description | Required |
| ------------------ | ------ | ----------- | -------- |
| name_or_id         | string |             | No       |
| creator            | string |             | No       |
| supplier_or_vendor | string |             | No       |

#### `v2SearchPromotionsRequestToBetween`

| Name        | Type     | Description | Required |
| ----------- | -------- | ----------- | -------- |
| start_time  | dateTime |             | No       |
| expire_time | dateTime |             | No       |

#### `v2SearchPromotionsResponse`

| Name       | Type                                                                          | Description | Required |
| ---------- | ----------------------------------------------------------------------------- | ----------- | -------- |
| promotions | [ [v2Promotion](#v2Promotion) ]                                               |             | No       |
| pagination | [v2SearchPromotionsResponsePagination](#v2SearchPromotionsResponsePagination) |             | No       |
| statuses   | [ [promotionv2Status](#promotionv2Status) ]                                   |             | No       |

#### `v2SearchPromotionsResponsePagination`

| Name        | Type    | Description | Required |
| ----------- | ------- | ----------- | -------- |
| page_number | integer |             | No       |
| page_size   | integer |             | No       |
| total_size  | integer |             | No       |

#### `ContentEvent`

| Name   | Type   | Description | Required |
| ------ | ------ | ----------- | -------- |
| type   | string |             | No       |
| params | string |             | No       |

#### `protobufAny`

| Name     | Type   | Description | Required |
| -------- | ------ | ----------- | -------- |
| type_url | string |             | No       |
| value    | byte   |             | No       |

#### `v2Content`

| Name       | Type                          | Description | Required |
| ---------- | ----------------------------- | ----------- | -------- |
| id         | string                        |             | No       |
| conditions | string                        |             | No       |
| event      | [ContentEvent](#ContentEvent) |             | No       |

#### `v2CreateContentsResponse`

| Name     | Type                        | Description | Required |
| -------- | --------------------------- | ----------- | -------- |
| contents | [ [v2Content](#v2Content) ] |             | No       |

#### `v2Target`

| Name    | Type   | Description | Required |
| ------- | ------ | ----------- | -------- |
| targets | string |             | No       |

#### `ConditionUsageMaxTimesPerPerson`

| Name     | Type    | Description | Required |
| -------- | ------- | ----------- | -------- |
| is_limit | boolean |             | No       |
| count    | integer |             | No       |

#### `ConditionUsageMaxTimesPerPersonPerTime`

| Name      | Type                                                                  | Description | Required |
| --------- | --------------------------------------------------------------------- | ----------- | -------- |
| is_limit  | boolean                                                               |             | No       |
| count     | integer                                                               |             | No       |
| time_type | [MaxTimesPerPersonPerTimeTimeType](#MaxTimesPerPersonPerTimeTimeType) |             | No       |

#### `ConditionUsageMaxTimesUsage`

| Name     | Type    | Description | Required |
| -------- | ------- | ----------- | -------- |
| is_limit | boolean |             | No       |
| count    | integer |             | No       |

#### `MaxTimesPerPersonPerTimeTimeType`

| Name                             | Type   | Description | Required |
| -------------------------------- | ------ | ----------- | -------- |
| MaxTimesPerPersonPerTimeTimeType | string |             |          |

#### `v2ConditionUsage`

| Name                          | Type                                                                              | Description | Required |
| ----------------------------- | --------------------------------------------------------------------------------- | ----------- | -------- |
| max_times_usage               | [ConditionUsageMaxTimesUsage](#ConditionUsageMaxTimesUsage)                       |             | No       |
| max_times_per_person          | [ConditionUsageMaxTimesPerPerson](#ConditionUsageMaxTimesPerPerson)               |             | No       |
| max_times_per_person_per_time | [ConditionUsageMaxTimesPerPersonPerTime](#ConditionUsageMaxTimesPerPersonPerTime) |             | No       |
`
#### `v2CreateConditionUsageResponse`

| Name            | Type                                  | Description | Required |
| --------------- | ------------------------------------- | ----------- | -------- |
| condition_usage | [v2ConditionUsage](#v2ConditionUsage) |             | No       |

#### `CodeSettingCodeType`

| Name                | Type   | Description | Required |
| ------------------- | ------ | ----------- | -------- |
| CodeSettingCodeType | string |             |          |

#### `CodeSettingTypeCode`

| Name                | Type   | Description | Required |
| ------------------- | ------ | ----------- | -------- |
| CodeSettingTypeCode | string |             |          |

#### `promotionv2MaxTimes`

| Name     | Type    | Description | Required |
| -------- | ------- | ----------- | -------- |
| is_limit | boolean |             | No       |
| count    | integer |             | No       |

#### `v2CodeSetting`

| Name                 | Type                                        | Description | Required |
| -------------------- | ------------------------------------------- | ----------- | -------- |
| is_use_code          | boolean                                     |             | No       |
| code_type            | [CodeSettingCodeType](#CodeSettingCodeType) |             | No       |
| max_times_per_person | [promotionv2MaxTimes](#promotionv2MaxTimes) |             | No       |
| count                | integer                                     |             | No       |
| max_times_per_code   | [promotionv2MaxTimes](#promotionv2MaxTimes) |             | No       |
| type                 | [CodeSettingTypeCode](#CodeSettingTypeCode) |             | No       |
| prefix               | string                                      |             | No       |
| postfix              | string                                      |             | No       |
| code_length          | integer                                     |             | No       |

#### `v2CountCodesRequestCodeStatus`

| Name                          | Type   | Description | Required |
| ----------------------------- | ------ | ----------- | -------- |
| v2CountCodesRequestCodeStatus | string |             |          |

#### `v2CountCodesResponse`

| Name   | Type    | Description | Required |
| ------ | ------- | ----------- | -------- |
| number | integer |             | No       |

#### `ApplyInfoAttachProduct`

| Name | Type | Description | Required |
| ---- | ---- | ----------- | -------- |
| sku | string |  | No |
| quantity | integer |  | No |

#### `HowToLoadHowToChoose`

| Name | Type | Description | Required |
| ---- | ---- | ----------- | -------- |
| HowToLoadHowToChoose | string |  |  |

#### `HowToLoadTypeLoad`

| Name | Type | Description | Required |
| ---- | ---- | ----------- | -------- |
| HowToLoadTypeLoad | string |  |  |

#### `googlerpcStatus`

| Name | Type | Description | Required |
| ---- | ---- | ----------- | -------- |
| code | integer |  | No |
| message | string |  | No |
| details | [ [protobufAny](#protobufAny) ] |  | No |

#### `integratev2Product`

| Name | Type | Description | Required |
| ---- | ---- | ----------- | -------- |
| voucher_code | [v2Code](#v2Code) |  | No |
| sku | string |  | No |
| price | float |  | No |
| quantity | integer |  | No |

#### `v2ApplyInfo`

| Name | Type | Description | Required |
| ---- | ---- | ----------- | -------- |
| promotion_id | string |  | No |
| voucher_code | string |  | No |
| attach_products | [ [ApplyInfoAttachProduct](#ApplyInfoAttachProduct) ] |  | No |

#### `v2ApplyPromotionRequest`

| Name | Type | Description | Required |
| ---- | ---- | ----------- | -------- |
| appplies_info | [ [v2ApplyInfo](#v2ApplyInfo) ] |  | No |
| payment_method | string |  | No |
| orders | [ [v2ApplyPromotionRequestOrder](#v2ApplyPromotionRequestOrder) ] |  | Yes |
| order_time | dateTime |  | No |
| agent_phone | string |  | Yes |
| total_amount | float |  | No |
| partner_code | string |  | No |

#### `v2ApplyPromotionRequestOrder`

| Name | Type | Description | Required |
| ---- | ---- | ----------- | -------- |
| appplies_info | [ [v2ApplyInfo](#v2ApplyInfo) ] |  | No |
| company_id | string |  | No |
| products | [ [v2ApplyPromotionRequestOrderProduct](#v2ApplyPromotionRequestOrderProduct) ] |  | Yes |
| payment_method | string |  | No |
| total_amount | float |  | No |
| code | string |  | No |

#### `v2ApplyPromotionRequestOrderProduct`

| Name | Type | Description | Required |
| ---- | ---- | ----------- | -------- |
| appplies_info | [ [v2ApplyInfo](#v2ApplyInfo) ] |  | No |
| sku | string |  | No |
| price | float |  | No |
| quantity | integer |  | No |

#### `v2ApplyPromotionResponse`

| Name | Type | Description | Required |
| ---- | ---- | ----------- | -------- |
| appplies_info | [ [v2ApplyInfo](#v2ApplyInfo) ] |  | No |
| transactions_apply | [ [v2TransactionApply](#v2TransactionApply) ] |  | No |
| orders | [ [v2ApplyPromotionResponseOrder](#v2ApplyPromotionResponseOrder) ] |  | Yes |
| errors | [ string ] |  | No |
| transaction | [v2Transaction](#v2Transaction) |  | No |

#### `v2ApplyPromotionResponseOrder`

| Name | Type | Description | Required |
| ---- | ---- | ----------- | -------- |
| appplies_info | [ [v2ApplyInfo](#v2ApplyInfo) ] |  | No |
| transactions_apply | [ [v2TransactionApply](#v2TransactionApply) ] |  | No |
| company_id | string |  | No |
| products | [ [v2ApplyPromotionResponseOrderProduct](#v2ApplyPromotionResponseOrderProduct) ] |  | Yes |
| payment_method | string |  | No |
| total_amount | float |  | No |
| code | string |  | No |
| transaction_apply | [v2TransactionApply](#v2TransactionApply) |  | No |
| errors | [ string ] |  | No |

#### `v2ApplyPromotionResponseOrderProduct`

| Name | Type | Description | Required |
| ---- | ---- | ----------- | -------- |
| appplies_info | [ [v2ApplyInfo](#v2ApplyInfo) ] |  | No |
| transactions_apply | [ [v2TransactionApply](#v2TransactionApply) ] |  | No |
| sku | string |  | No |
| price | float |  | No |
| quantity | integer |  | No |
| errors | [ string ] |  | No |

#### `v2ApplyTransactionStatus`

| Name | Type | Description | Required |
| ---- | ---- | ----------- | -------- |
| v2ApplyTransactionStatus | string |  |  |

#### `v2CheckApplyPromotionRequest`

| Name | Type | Description | Required |
| ---- | ---- | ----------- | -------- |
| appplies_info | [ [v2ApplyInfo](#v2ApplyInfo) ] |  | No |
| payment_method | string |  | No |
| orders | [ [v2CheckApplyPromotionRequestOrder](#v2CheckApplyPromotionRequestOrder) ] |  | Yes |
| order_time | dateTime |  | No |
| agent_phone | string |  | Yes |
| total_amount | float |  | No |
| partner_code | string |  | No |

#### `v2CheckApplyPromotionRequestOrder`

| Name | Type | Description | Required |
| ---- | ---- | ----------- | -------- |
| appplies_info | [ [v2ApplyInfo](#v2ApplyInfo) ] |  | No |
| company_id | string |  | No |
| products | [ [v2CheckApplyPromotionRequestOrderProduct](#v2CheckApplyPromotionRequestOrderProduct) ] |  | Yes |
| payment_method | string |  | No |
| total_amount | float |  | No |
| code | string |  | No |

#### `v2CheckApplyPromotionRequestOrderProduct`

| Name | Type | Description | Required |
| ---- | ---- | ----------- | -------- |
| appplies_info | [ [v2ApplyInfo](#v2ApplyInfo) ] |  | No |
| sku | string |  | No |
| price | float |  | No |
| quantity | integer |  | No |

#### `v2CheckApplyPromotionResponse`

| Name | Type | Description | Required |
| ---- | ---- | ----------- | -------- |
| appplies_info | [ [v2ApplyInfo](#v2ApplyInfo) ] |  | No |
| orders | [ [v2CheckApplyPromotionResponseOrder](#v2CheckApplyPromotionResponseOrder) ] |  | Yes |
| errors | [ string ] |  | No |
| status | [v2CheckApplyPromotionResponseStatus](#v2CheckApplyPromotionResponseStatus) |  | No |

#### `v2CheckApplyPromotionResponseOrder`

| Name | Type | Description | Required |
| ---- | ---- | ----------- | -------- |
| appplies_info | [ [v2ApplyInfo](#v2ApplyInfo) ] |  | No |
| company_id | string |  | No |
| products | [ [v2CheckApplyPromotionResponseOrderProduct](#v2CheckApplyPromotionResponseOrderProduct) ] |  | Yes |
| payment_method | string |  | No |
| total_amount | float |  | No |
| code | string |  | No |
| errors | [ string ] |  | No |

#### `v2CheckApplyPromotionResponseOrderProduct`

| Name | Type | Description | Required |
| ---- | ---- | ----------- | -------- |
| appplies_info | [ [v2ApplyInfo](#v2ApplyInfo) ] |  | No |
| sku | string |  | No |
| price | float |  | No |
| quantity | integer |  | No |
| errors | [ string ] |  | No |

#### `v2CheckApplyPromotionResponseStatus`

| Name | Type | Description | Required |
| ---- | ---- | ----------- | -------- |
| v2CheckApplyPromotionResponseStatus | string |  |  |

#### `v2CheckVoucherCodeIsValidRequest`

| Name | Type | Description | Required |
| ---- | ---- | ----------- | -------- |
| voucher_code | string |  | No |
| payment_method | string |  | No |
| orders | [ [v2CheckVoucherCodeIsValidRequestOrder](#v2CheckVoucherCodeIsValidRequestOrder) ] |  | Yes |
| order_time | dateTime |  | No |
| agent_phone | string |  | Yes |
| total_amount | float |  | No |
| type | string |  | No |
| partner_code | string |  | No |

#### `v2CheckVoucherCodeIsValidRequestOrder`

| Name | Type | Description | Required |
| ---- | ---- | ----------- | -------- |
| voucher_code | string |  | No |
| company_id | string |  | No |
| products | [ [v2CheckVoucherCodeIsValidRequestOrderProduct](#v2CheckVoucherCodeIsValidRequestOrderProduct) ] |  | Yes |
| payment_method | string |  | No |
| total_amount | float |  | No |

#### `v2CheckVoucherCodeIsValidRequestOrderProduct`

| Name | Type | Description | Required |
| ---- | ---- | ----------- | -------- |
| voucher_code | string |  | No |
| sku | string |  | No |
| price | float |  | No |
| quantity | integer |  | No |

#### `v2CheckVoucherCodeIsValidResponse`

| Name | Type | Description | Required |
| ---- | ---- | ----------- | -------- |
| voucher_code | [v2Code](#v2Code) |  | No |
| orders | [ [v2CheckVoucherCodeIsValidResponseOrder](#v2CheckVoucherCodeIsValidResponseOrder) ] |  | No |
| errors | [ string ] |  | No |
| promotions_allow_apply | [ [v2Promotion](#v2Promotion) ] |  | No |

#### `v2CheckVoucherCodeIsValidResponseOrder`

| Name | Type | Description | Required |
| ---- | ---- | ----------- | -------- |
| voucher_code | [v2Code](#v2Code) |  | No |
| company_id | string |  | No |
| products | [ [integratev2Product](#integratev2Product) ] |  | No |
| errors | [ string ] |  | No |

#### `v2Code`

| Name | Type | Description | Required |
| ---- | ---- | ----------- | -------- |
| id | string |  | No |
| code | string |  | No |
| number_of_use | integer |  | No |
| usage_agents | [ string ] |  | No |
| promotion | [v2PromotionAction](#v2PromotionAction) |  | No |

#### `v2CommitApplyPromotionRequest`

| Name | Type | Description | Required |
| ---- | ---- | ----------- | -------- |
| transaction_id | string |  | Yes |

#### `v2CommitApplyPromotionResponse`

| Name | Type | Description | Required |
| ---- | ---- | ----------- | -------- |
| transaction | [v2Transaction](#v2Transaction) |  | No |
| transactions_apply | [ [v2TransactionApply](#v2TransactionApply) ] |  | No |

#### `v2HowToLoad`

| Name | Type | Description | Required |
| ---- | ---- | ----------- | -------- |
| is_load | boolean |  | No |
| type_load | [HowToLoadTypeLoad](#HowToLoadTypeLoad) |  | No |
| how_to_choose | [HowToLoadHowToChoose](#HowToLoadHowToChoose) |  | No |
| is_suggest_show | boolean |  | No |

#### `v2ListPromotionsRequest`

| Name | Type | Description | Required |
| ---- | ---- | ----------- | -------- |
| agent_phone | string |  | Yes |
| orders | [ [v2ListPromotionsRequestOrder](#v2ListPromotionsRequestOrder) ] |  | Yes |
| order_time | dateTime |  | No |
| channel | string |  | No |
| payment_method | string |  | No |
| partner_code | string |  | No |
| total_amount | float |  | No |
| how_to_load | [v2HowToLoad](#v2HowToLoad) |  | No |

#### `v2ListPromotionsRequestOrder`

| Name | Type | Description | Required |
| ---- | ---- | ----------- | -------- |
| company_id | string |  | No |
| products | [ [v2ListPromotionsRequestOrderProduct](#v2ListPromotionsRequestOrderProduct) ] |  | Yes |
| payment_method | string |  | No |
| total_amount | float |  | No |
| how_to_load | [v2HowToLoad](#v2HowToLoad) |  | No |

#### `v2ListPromotionsRequestOrderProduct`

| Name | Type | Description | Required |
| ---- | ---- | ----------- | -------- |
| sku | string |  | No |
| price | float |  | No |
| quantity | integer |  | No |
| how_to_load | [v2HowToLoad](#v2HowToLoad) |  | No |

#### `v2ListPromotionsResponse`

| Name | Type | Description | Required |
| ---- | ---- | ----------- | -------- |
| orders | [ [v2ListPromotionsResponseOrder](#v2ListPromotionsResponseOrder) ] |  | Yes |
| promotions | [ [v2PromotionAction](#v2PromotionAction) ] |  | No |
| promotions_allow_apply | [ [v2Promotion](#v2Promotion) ] |  | No |
| promotion_ids_allow_apply | [ [v2Promotion](#v2Promotion) ] |  | No |

#### `v2ListPromotionsResponseOrder`

| Name | Type | Description | Required |
| ---- | ---- | ----------- | -------- |
| company_id | string |  | No |
| products | [ [v2ListPromotionsResponseOrderProduct](#v2ListPromotionsResponseOrderProduct) ] |  | Yes |
| promotions | [ [v2PromotionAction](#v2PromotionAction) ] |  | No |

#### `v2ListPromotionsResponseOrderProduct`

| Name | Type | Description | Required |
| ---- | ---- | ----------- | -------- |
| sku | string |  | No |
| price | float |  | No |
| quantity | integer |  | No |
| company_id | string |  | No |
| promotions | [ [v2PromotionAction](#v2PromotionAction) ] |  | No |

#### `v2Promotion`

| Name | Type | Description | Required |
| ---- | ---- | ----------- | -------- |
| id | string |  | No |
| name | string |  | No |
| expire_time | dateTime |  | No |
| start_time | dateTime |  | No |
| type | [v2PromotionType](#v2PromotionType) |  | No |
| content | string |  | No |
| description | string |  | No |
| detail | string |  | No |
| method | [v2PromotionMethod](#v2PromotionMethod) |  | No |

#### `v2PromotionAction`

| Name | Type | Description | Required |
| ---- | ---- | ----------- | -------- |
| id | string |  | No |
| discount_action | string |  | No |
| voucher_codes | [ [v2VoucherCode](#v2VoucherCode) ] |  | No |

#### `v2PromotionMethod`

| Name | Type | Description | Required |
| ---- | ---- | ----------- | -------- |
| v2PromotionMethod | string |  |  |

#### `v2PromotionType`

| Name | Type | Description | Required |
| ---- | ---- | ----------- | -------- |
| v2PromotionType | string |  |  |

#### `v2RevertApplyPromotionRequest`

| Name | Type | Description | Required |
| ---- | ---- | ----------- | -------- |
| transaction_id | string |  | Yes |

#### `v2RevertApplyPromotionResponse`

| Name | Type | Description | Required |
| ---- | ---- | ----------- | -------- |
| transaction | [v2Transaction](#v2Transaction) |  | No |
| transactions_apply | [ [v2TransactionApply](#v2TransactionApply) ] |  | No |

#### `v2Transaction`

| Name | Type | Description | Required |
| ---- | ---- | ----------- | -------- |
| id | string |  | No |
| status | [v2TransactionStatus](#v2TransactionStatus) |  | No |

#### `v2TransactionApply`

| Name | Type | Description | Required |
| ---- | ---- | ----------- | -------- |
| id | string |  | No |
| usage_agent | string |  | No |
| code_id | string |  | No |
| voucher_code | string |  | No |
| promotion_id | string |  | No |
| promotion_name | string |  | No |
| is_revert | boolean |  | No |
| usage_times | integer |  | No |
| status | [v2ApplyTransactionStatus](#v2ApplyTransactionStatus) |  | No |
| create_time | dateTime |  | No |
| update_time | dateTime |  | No |
| transaction_id | string |  | No |

#### `v2TransactionStatus`

| Name | Type | Description | Required |
| ---- | ---- | ----------- | -------- |
| v2TransactionStatus | string |  |  |

#### `v2VoucherCode`

| Name | Type | Description | Required |
| ---- | ---- | ----------- | -------- |
| id | string |  | No |
| code | string |  | No |

#### `ApplyInfoAttachProduct`

| Name | Type | Description | Required |
| ---- | ---- | ----------- | -------- |
| sku | string |  | No |
| quantity | integer |  | No |

#### `HowToLoadHowToChoose`

| Name | Type | Description | Required |
| ---- | ---- | ----------- | -------- |
| HowToLoadHowToChoose | string |  |  |

#### `HowToLoadTypeLoad`

| Name | Type | Description | Required |
| ---- | ---- | ----------- | -------- |
| HowToLoadTypeLoad | string |  |  |

#### `ListPromotionsByTypesResponsePromotionsByType`

| Name | Type | Description | Required |
| ---- | ---- | ----------- | -------- |
| type | [v1PropertyType](#v1PropertyType) |  | No |
| promotion_ids | [ string ] |  | No |

#### `PropertyTypeProperty`

| Name | Type | Description | Required |
| ---- | ---- | ----------- | -------- |
| PropertyTypeProperty | string |  |  |

#### `combinev1Product`

| Name | Type | Description | Required |
| ---- | ---- | ----------- | -------- |
| voucher_code | [v1Code](#v1Code) |  | No |
| sku | string |  | No |
| price | float |  | No |
| quantity | integer |  | No |

#### `combinev1PromotionType`

| Name | Type | Description | Required |
| ---- | ---- | ----------- | -------- |
| combinev1PromotionType | string |  |  |

#### `googlerpcStatus`

| Name | Type | Description | Required |
| ---- | ---- | ----------- | -------- |
| code | integer |  | No |
| message | string |  | No |
| details | [ [protobufAny](#protobufAny) ] |  | No |

#### `protobufAny`

| Name | Type | Description | Required |
| ---- | ---- | ----------- | -------- |
| type_url | string |  | No |
| value | byte |  | No |

#### `v1ApplyContent`

| Name | Type | Description | Required |
| ---- | ---- | ----------- | -------- |
| v1ApplyContent | string |  |  |

#### `v1ApplyInfo`

| Name | Type | Description | Required |
| ---- | ---- | ----------- | -------- |
| promotion_id | string |  | No |
| voucher_code | string |  | No |
| attach_products | [ [ApplyInfoAttachProduct](#ApplyInfoAttachProduct) ] |  | No |

#### `v1ApplyPromotionRequest`

| Name | Type | Description | Required |
| ---- | ---- | ----------- | -------- |
| appplies_info | [ [v1ApplyInfo](#v1ApplyInfo) ] |  | No |
| payment_method | string |  | No |
| orders | [ [v1ApplyPromotionRequestOrder](#v1ApplyPromotionRequestOrder) ] |  | Yes |
| order_time | dateTime |  | No |
| agent_phone | string |  | Yes |
| total_amount | float |  | No |
| partner_code | string |  | No |

#### `v1ApplyPromotionRequestOrder`

| Name | Type | Description | Required |
| ---- | ---- | ----------- | -------- |
| appplies_info | [ [v1ApplyInfo](#v1ApplyInfo) ] |  | No |
| company_id | string |  | No |
| products | [ [v1ApplyPromotionRequestOrderProduct](#v1ApplyPromotionRequestOrderProduct) ] |  | Yes |
| payment_method | string |  | No |
| total_amount | float |  | No |
| code | string |  | No |

#### `v1ApplyPromotionRequestOrderProduct`

| Name | Type | Description | Required |
| ---- | ---- | ----------- | -------- |
| appplies_info | [ [v1ApplyInfo](#v1ApplyInfo) ] |  | No |
| sku | string |  | No |
| price | float |  | No |
| quantity | integer |  | No |

#### `v1ApplyPromotionResponse`

| Name | Type | Description | Required |
| ---- | ---- | ----------- | -------- |
| appplies_info | [ [v1ApplyInfo](#v1ApplyInfo) ] |  | No |
| transactions_apply | [ [v1TransactionApply](#v1TransactionApply) ] |  | No |
| orders | [ [v1ApplyPromotionResponseOrder](#v1ApplyPromotionResponseOrder) ] |  | Yes |
| errors | [ string ] |  | No |
| transaction | [v1Transaction](#v1Transaction) |  | No |

#### `v1ApplyPromotionResponseOrder`

| Name | Type | Description | Required |
| ---- | ---- | ----------- | -------- |
| appplies_info | [ [v1ApplyInfo](#v1ApplyInfo) ] |  | No |
| transactions_apply | [ [v1TransactionApply](#v1TransactionApply) ] |  | No |
| company_id | string |  | No |
| products | [ [v1ApplyPromotionResponseOrderProduct](#v1ApplyPromotionResponseOrderProduct) ] |  | Yes |
| payment_method | string |  | No |
| total_amount | float |  | No |
| code | string |  | No |
| transaction_apply | [v1TransactionApply](#v1TransactionApply) |  | No |
| errors | [ string ] |  | No |

#### `v1ApplyPromotionResponseOrderProduct`

| Name | Type | Description | Required |
| ---- | ---- | ----------- | -------- |
| appplies_info | [ [v1ApplyInfo](#v1ApplyInfo) ] |  | No |
| transactions_apply | [ [v1TransactionApply](#v1TransactionApply) ] |  | No |
| sku | string |  | No |
| price | float |  | No |
| quantity | integer |  | No |
| errors | [ string ] |  | No |

#### `v1ApplyTransactionStatus`

| Name | Type | Description | Required |
| ---- | ---- | ----------- | -------- |
| v1ApplyTransactionStatus | string |  |  |

#### `v1CheckApplyPromotionRequest`

| Name | Type | Description | Required |
| ---- | ---- | ----------- | -------- |
| appplies_info | [ [v1ApplyInfo](#v1ApplyInfo) ] |  | No |
| payment_method | string |  | No |
| orders | [ [v1CheckApplyPromotionRequestOrder](#v1CheckApplyPromotionRequestOrder) ] |  | Yes |
| order_time | dateTime |  | No |
| agent_phone | string |  | Yes |
| total_amount | float |  | No |
| partner_code | string |  | No |

#### `v1CheckApplyPromotionRequestOrder`

| Name | Type | Description | Required |
| ---- | ---- | ----------- | -------- |
| appplies_info | [ [v1ApplyInfo](#v1ApplyInfo) ] |  | No |
| company_id | string |  | No |
| products | [ [v1CheckApplyPromotionRequestOrderProduct](#v1CheckApplyPromotionRequestOrderProduct) ] |  | Yes |
| payment_method | string |  | No |
| total_amount | float |  | No |
| code | string |  | No |

#### `v1CheckApplyPromotionRequestOrderProduct`

| Name | Type | Description | Required |
| ---- | ---- | ----------- | -------- |
| appplies_info | [ [v1ApplyInfo](#v1ApplyInfo) ] |  | No |
| sku | string |  | No |
| price | float |  | No |
| quantity | integer |  | No |

#### `v1CheckApplyPromotionResponse`

| Name | Type | Description | Required |
| ---- | ---- | ----------- | -------- |
| appplies_info | [ [v1ApplyInfo](#v1ApplyInfo) ] |  | No |
| orders | [ [v1CheckApplyPromotionResponseOrder](#v1CheckApplyPromotionResponseOrder) ] |  | Yes |
| errors | [ [v1PromotionError](#v1PromotionError) ] |  | No |
| status | [v1CheckApplyPromotionResponseStatus](#v1CheckApplyPromotionResponseStatus) |  | No |

#### `v1CheckApplyPromotionResponseOrder`

| Name | Type | Description | Required |
| ---- | ---- | ----------- | -------- |
| appplies_info | [ [v1ApplyInfo](#v1ApplyInfo) ] |  | No |
| company_id | string |  | No |
| products | [ [v1CheckApplyPromotionResponseOrderProduct](#v1CheckApplyPromotionResponseOrderProduct) ] |  | Yes |
| payment_method | string |  | No |
| total_amount | float |  | No |
| code | string |  | No |
| errors | [ [v1PromotionError](#v1PromotionError) ] |  | No |

#### `v1CheckApplyPromotionResponseOrderProduct`

| Name | Type | Description | Required |
| ---- | ---- | ----------- | -------- |
| appplies_info | [ [v1ApplyInfo](#v1ApplyInfo) ] |  | No |
| sku | string |  | No |
| price | float |  | No |
| quantity | integer |  | No |
| errors | [ [v1PromotionError](#v1PromotionError) ] |  | No |

#### `v1CheckApplyPromotionResponseStatus`

| Name | Type | Description | Required |
| ---- | ---- | ----------- | -------- |
| v1CheckApplyPromotionResponseStatus | string |  |  |

#### `v1CheckVoucherCodeIsValidRequest`

| Name | Type | Description | Required |
| ---- | ---- | ----------- | -------- |
| voucher_code | string |  | No |
| payment_method | string |  | No |
| orders | [ [v1CheckVoucherCodeIsValidRequestOrder](#v1CheckVoucherCodeIsValidRequestOrder) ] |  | Yes |
| order_time | dateTime |  | No |
| agent_phone | string |  | Yes |
| total_amount | float |  | No |
| type | string |  | No |
| partner_code | string |  | No |

#### `v1CheckVoucherCodeIsValidRequestOrder`

| Name | Type | Description | Required |
| ---- | ---- | ----------- | -------- |
| voucher_code | string |  | No |
| company_id | string |  | No |
| products | [ [v1CheckVoucherCodeIsValidRequestOrderProduct](#v1CheckVoucherCodeIsValidRequestOrderProduct) ] |  | Yes |
| payment_method | string |  | No |
| total_amount | float |  | No |

#### `v1CheckVoucherCodeIsValidRequestOrderProduct`

| Name | Type | Description | Required |
| ---- | ---- | ----------- | -------- |
| voucher_code | string |  | No |
| sku | string |  | No |
| price | float |  | No |
| quantity | integer |  | No |

#### `v1CheckVoucherCodeIsValidResponse`

| Name | Type | Description | Required |
| ---- | ---- | ----------- | -------- |
| voucher_code | [v1Code](#v1Code) |  | No |
| orders | [ [v1CheckVoucherCodeIsValidResponseOrder](#v1CheckVoucherCodeIsValidResponseOrder) ] |  | No |
| errors | [ string ] |  | No |
| promotions_allow_apply | [ [v1Promotion](#v1Promotion) ] |  | No |

#### `v1CheckVoucherCodeIsValidResponseOrder`

| Name | Type | Description | Required |
| ---- | ---- | ----------- | -------- |
| voucher_code | [v1Code](#v1Code) |  | No |
| company_id | string |  | No |
| products | [ [combinev1Product](#combinev1Product) ] |  | No |
| errors | [ string ] |  | No |

#### `v1Code`

| Name | Type | Description | Required |
| ---- | ---- | ----------- | -------- |
| id | string |  | No |
| code | string |  | No |
| number_of_use | integer |  | No |
| usage_agents | [ string ] |  | No |
| promotion | [v1PromotionAction](#v1PromotionAction) |  | No |

#### `v1CommitApplyPromotionRequest`

| Name | Type | Description | Required |
| ---- | ---- | ----------- | -------- |
| transaction_id | string |  | Yes |

#### `v1CommitApplyPromotionResponse`

| Name | Type | Description | Required |
| ---- | ---- | ----------- | -------- |
| transaction | [v1Transaction](#v1Transaction) |  | No |
| transactions_apply | [ [v1TransactionApply](#v1TransactionApply) ] |  | No |

#### `v1HowToLoad`

| Name | Type | Description | Required |
| ---- | ---- | ----------- | -------- |
| is_load | boolean |  | No |
| type_load | [HowToLoadTypeLoad](#HowToLoadTypeLoad) |  | No |
| how_to_choose | [HowToLoadHowToChoose](#HowToLoadHowToChoose) |  | No |
| is_suggest_show | boolean |  | No |

#### `v1ListPromotionsByTypesRequest`

| Name | Type | Description | Required |
| ---- | ---- | ----------- | -------- |
| agent_phone | string |  | Yes |
| types | [ [v1PropertyType](#v1PropertyType) ] |  | No |

#### `v1ListPromotionsByTypesResponse`

| Name | Type | Description | Required |
| ---- | ---- | ----------- | -------- |
| promotions_by_types | [ [ListPromotionsByTypesResponsePromotionsByType](#ListPromotionsByTypesResponsePromotionsByType) ] |  | No |
| promotions | [ [v1Promotion](#v1Promotion) ] |  | No |

#### `v1ListPromotionsRequest`

| Name | Type | Description | Required |
| ---- | ---- | ----------- | -------- |
| agent_phone | string |  | Yes |
| orders | [ [v1ListPromotionsRequestOrder](#v1ListPromotionsRequestOrder) ] |  | Yes |
| order_time | dateTime |  | No |
| channel | string |  | No |
| payment_method | string |  | No |
| partner_code | string |  | No |
| total_amount | float |  | No |
| how_to_load | [v1HowToLoad](#v1HowToLoad) |  | No |

#### `v1ListPromotionsRequestOrder`

| Name | Type | Description | Required |
| ---- | ---- | ----------- | -------- |
| company_id | string |  | No |
| products | [ [v1ListPromotionsRequestOrderProduct](#v1ListPromotionsRequestOrderProduct) ] |  | Yes |
| payment_method | string |  | No |
| total_amount | float |  | No |
| how_to_load | [v1HowToLoad](#v1HowToLoad) |  | No |

#### `v1ListPromotionsRequestOrderProduct`

| Name | Type | Description | Required |
| ---- | ---- | ----------- | -------- |
| sku | string |  | No |
| price | float |  | No |
| quantity | integer |  | No |
| how_to_load | [v1HowToLoad](#v1HowToLoad) |  | No |

#### `v1ListPromotionsResponse`

| Name | Type | Description | Required |
| ---- | ---- | ----------- | -------- |
| orders | [ [v1ListPromotionsResponseOrder](#v1ListPromotionsResponseOrder) ] |  | Yes |
| promotions | [ [v1PromotionAction](#v1PromotionAction) ] |  | No |
| promotions_allow_apply | [ [v1Promotion](#v1Promotion) ] |  | No |
| promotion_ids_allow_apply | [ [v1Promotion](#v1Promotion) ] |  | No |

#### `v1ListPromotionsResponseOrder`

| Name | Type | Description | Required |
| ---- | ---- | ----------- | -------- |
| company_id | string |  | No |
| products | [ [v1ListPromotionsResponseOrderProduct](#v1ListPromotionsResponseOrderProduct) ] |  | Yes |
| promotions | [ [v1PromotionAction](#v1PromotionAction) ] |  | No |

#### `v1ListPromotionsResponseOrderProduct`

| Name | Type | Description | Required |
| ---- | ---- | ----------- | -------- |
| sku | string |  | No |
| price | float |  | No |
| quantity | integer |  | No |
| company_id | string |  | No |
| promotions | [ [v1PromotionAction](#v1PromotionAction) ] |  | No |

#### `v1Promotion`

| Name | Type | Description | Required |
| ---- | ---- | ----------- | -------- |
| id | string |  | No |
| name | string |  | No |
| expire_time | dateTime |  | No |
| start_time | dateTime |  | No |
| type | [combinev1PromotionType](#combinev1PromotionType) |  | No |
| content | string |  | No |
| description | string |  | No |
| detail | string |  | No |
| method | [v1PromotionMethod](#v1PromotionMethod) |  | No |
| method_apply_content | [v1ApplyContent](#v1ApplyContent) |  | No |
| create_time | dateTime |  | No |

#### `v1PromotionAction`

| Name | Type | Description | Required |
| ---- | ---- | ----------- | -------- |
| id | string |  | No |
| discount_action | string |  | No |
| voucher_codes | [ [v1VoucherCode](#v1VoucherCode) ] |  | No |
| suggests | [ string ] |  | No |

#### `v1PromotionError`

| Name | Type | Description | Required |
| ---- | ---- | ----------- | -------- |
| promotion_id | string |  | No |
| errors | [ string ] |  | No |

#### `v1PromotionMethod`

| Name | Type | Description | Required |
| ---- | ---- | ----------- | -------- |
| v1PromotionMethod | string |  |  |

#### `v1PropertyType`

| Name | Type | Description | Required |
| ---- | ---- | ----------- | -------- |
| property | [PropertyTypeProperty](#PropertyTypeProperty) |  | No |
| id | string |  | No |
| promotion_types | [ [v1PropertyTypePromotionType](#v1PropertyTypePromotionType) ] |  | No |

#### `v1PropertyTypePromotionType`

| Name | Type | Description | Required |
| ---- | ---- | ----------- | -------- |
| v1PropertyTypePromotionType | string |  |  |

#### `v1RevertApplyPromotionRequest`

| Name | Type | Description | Required |
| ---- | ---- | ----------- | -------- |
| transaction_id | string |  | Yes |

#### `v1RevertApplyPromotionResponse`

| Name | Type | Description | Required |
| ---- | ---- | ----------- | -------- |
| transaction | [v1Transaction](#v1Transaction) |  | No |
| transactions_apply | [ [v1TransactionApply](#v1TransactionApply) ] |  | No |

#### `v1Transaction`

| Name | Type | Description | Required |
| ---- | ---- | ----------- | -------- |
| id | string |  | No |
| status | [v1TransactionStatus](#v1TransactionStatus) |  | No |

#### `v1TransactionApply`

| Name | Type | Description | Required |
| ---- | ---- | ----------- | -------- |
| id | string |  | No |
| usage_agent | string |  | No |
| code_id | string |  | No |
| voucher_code | string |  | No |
| promotion_id | string |  | No |
| promotion_name | string |  | No |
| is_revert | boolean |  | No |
| usage_times | integer |  | No |
| status | [v1ApplyTransactionStatus](#v1ApplyTransactionStatus) |  | No |
| create_time | dateTime |  | No |
| update_time | dateTime |  | No |
| transaction_id | string |  | No |
| promotion | [v1Promotion](#v1Promotion) |  | No |

#### `v1TransactionStatus`

| Name | Type | Description | Required |
| ---- | ---- | ----------- | -------- |
| v1TransactionStatus | string |  |  |

#### `v1VoucherCode`

| Name | Type | Description | Required |
| ---- | ---- | ----------- | -------- |
| id | string |  | No |
| code | string |  | No |