
# Applications
- [Applications](#applications)
  - [Applications](#applications-1)
    - [Miêu tả](#miêu-tả)
    - [Entities Chính](#entities-chính)
    - [/v1/agents/{agent\_id}](#v1agentsagent_id)
      - [PATCH](#patch)
        - [Parameters](#parameters)
        - [Responses](#responses)
    - [/v1/agents:browse-list-id](#v1agentsbrowse-list-id)
      - [POST](#post)
        - [Summary:](#summary)
        - [Parameters](#parameters-1)
        - [Responses](#responses-1)
    - [/v1/agents:search](#v1agentssearch)
      - [GET](#get)
        - [Summary:](#summary-1)
        - [Parameters](#parameters-2)
        - [Responses](#responses-2)
    - [Models](#models)
      - [DistrictProvince](#districtprovince)
      - [openapisapplicationv1Pagination](#openapisapplicationv1pagination)
      - [protobufAny](#protobufany)
      - [rpcStatus](#rpcstatus)
      - [v1Agent](#v1agent)
      - [v1BusinessType](#v1businesstype)
      - [v1ConfigAgentStatusAppliedResponse](#v1configagentstatusappliedresponse)
      - [v1District](#v1district)
      - [v1LocationType](#v1locationtype)
      - [v1PromotionStatus](#v1promotionstatus)
      - [v1SearchAgentsRequestEqual](#v1searchagentsrequestequal)
      - [v1SearchAgentsRequestLike](#v1searchagentsrequestlike)
      - [v1SearchAgentsRequestQuery](#v1searchagentsrequestquery)
      - [v1SearchAgentsResponse](#v1searchagentsresponse)
      - [v1Supplier](#v1supplier)
      - [v1Vendor](#v1vendor)
    - [/v1/users](#v1users)
      - [POST](#post-1)
        - [Parameters](#parameters-3)
        - [Responses](#responses-3)
    - [/v1/users:login](#v1userslogin)
      - [POST](#post-2)
        - [Parameters](#parameters-4)
        - [Responses](#responses-4)
    - [/v1/users:logout](#v1userslogout)
      - [POST](#post-3)
        - [Responses](#responses-5)
    - [/v1/users:refresh-token](#v1usersrefresh-token)
      - [POST](#post-4)
        - [Parameters](#parameters-5)
        - [Responses](#responses-6)
    - [Models](#models-1)
      - [protobufAny](#protobufany-1)
      - [rpcStatus](#rpcstatus-1)
      - [v1CreateUserRequest](#v1createuserrequest)
      - [v1LoginRequest](#v1loginrequest)
      - [v1LoginResponse](#v1loginresponse)
      - [v1RefreshTokenRequest](#v1refreshtokenrequest)
      - [v1RefreshTokenResponse](#v1refreshtokenresponse)
      - [v1Role](#v1role)
      - [v1User](#v1user)

## Applications
 ### Miêu tả 
  - Xử lý việc auththen của cms promotion và thông tin user đã được đăng ký
 ### Entities Chính
  - `user`
  - `agent`

### /v1/agents/{agent_id}

#### PATCH
##### Parameters

| Name | Located in | Description | Required | Schema |
| ---- | ---------- | ----------- | -------- | ---- |
| agent_id | path |  | Yes | string |
| body | body |  | Yes | object |

##### Responses

| Code | Description | Schema |
| ---- | ----------- | ------ |
| 200 | A successful response. | [v1ConfigAgentStatusAppliedResponse](#v1ConfigAgentStatusAppliedResponse) |
| default | An unexpected error response. | [rpcStatus](#rpcStatus) |

### /v1/agents:browse-list-id

#### POST
##### Summary:

Cho phép người dùng tìm kiếm và lọc danh sách điểm bán hàng theo điều kiện [Được đồng bộ từ bên thứ 3]

##### Parameters

| Name | Located in | Description | Required | Schema |
| ---- | ---------- | ----------- | -------- | ---- |
| body | body |  | Yes | [v1SearchAgentsRequestQuery](#v1SearchAgentsRequestQuery) |
| equal.status | query |  | No | string |
| equal.phones | query | TODO: Write build schema for enum AgentStatus status = 1;. | No | [ string ] |
| like.phone | query |  | No | string |
| like.vendor | query |  | No | string |
| like.name | query |  | No | string |
| page_number | query |  | No | integer |
| page_size | query |  | No | integer |
| order_by | query |  | No | string |

##### Responses

| Code | Description | Schema |
| ---- | ----------- | ------ |
| 200 | A successful response. | [v1SearchAgentsResponse](#v1SearchAgentsResponse) |
| default | An unexpected error response. | [rpcStatus](#rpcStatus) |

### /v1/agents:search

#### GET
##### Summary:

Cho phép người dùng tìm kiếm và lọc danh sách điểm bán hàng theo điều kiện [Được đồng bộ từ bên thứ 3]

##### Parameters

| Name | Located in | Description | Required | Schema |
| ---- | ---------- | ----------- | -------- | ---- |
| equal.status | query |  | No | string |
| equal.phones | query | TODO: Write build schema for enum AgentStatus status = 1;. | No | [ string ] |
| like.phone | query |  | No | string |
| like.vendor | query |  | No | string |
| like.name | query |  | No | string |
| page_number | query |  | No | integer |
| page_size | query |  | No | integer |
| order_by | query |  | No | string |
| query.list_id | query |  | Yes | [ string ] |

##### Responses

| Code | Description | Schema |
| ---- | ----------- | ------ |
| 200 | A successful response. | [v1SearchAgentsResponse](#v1SearchAgentsResponse) |
| default | An unexpected error response. | [rpcStatus](#rpcStatus) |

### Models


#### DistrictProvince

| Name | Type | Description | Required |
| ---- | ---- | ----------- | -------- |
| id | string |  | No |
| name | string |  | No |

#### openapisapplicationv1Pagination

| Name | Type | Description | Required |
| ---- | ---- | ----------- | -------- |
| page_number | integer |  | No |
| page_size | integer |  | No |
| total_size | integer |  | No |

#### protobufAny

| Name | Type | Description | Required |
| ---- | ---- | ----------- | -------- |
| type_url | string |  | No |
| value | byte |  | No |

#### rpcStatus

| Name | Type | Description | Required |
| ---- | ---- | ----------- | -------- |
| code | integer |  | No |
| message | string |  | No |
| details | [ [protobufAny](#protobufAny) ] |  | No |

#### v1Agent

| Name | Type | Description | Required |
| ---- | ---- | ----------- | -------- |
| id | string |  | No |
| name | string |  | No |
| phone | string |  | No |
| status | string |  | No |
| business_type_id | string |  | No |
| location_type_id | string |  | No |
| vendor_ids | [ string ] |  | No |
| district_id | string |  | No |
| create_time | dateTime |  | No |
| update_time | dateTime |  | No |
| business_type | [v1BusinessType](#v1BusinessType) |  | No |
| location_type | [v1LocationType](#v1LocationType) |  | No |
| vendors | [ [v1Vendor](#v1Vendor) ] |  | No |
| asset_status | string |  | No |
| total_ordered | integer |  | No |
| supplier_ids | [ string ] |  | No |
| agent_id | string |  | No |
| promotion_status_applied | [v1PromotionStatus](#v1PromotionStatus) |  | No |
| valid_promotions | [ string ] |  | No |
| invalid_promotions | [ string ] |  | No |

#### v1BusinessType

| Name | Type | Description | Required |
| ---- | ---- | ----------- | -------- |
| id | string |  | No |
| name | string |  | No |
| code | string |  | No |
| create_time | dateTime |  | No |
| update_time | dateTime |  | No |
| business_type_id | integer |  | No |
| sync_histories | [ dateTime ] |  | No |

#### v1ConfigAgentStatusAppliedResponse

| Name | Type | Description | Required |
| ---- | ---- | ----------- | -------- |
| agent_id | string |  | No |
| status | [v1PromotionStatus](#v1PromotionStatus) |  | No |

#### v1District

| Name | Type | Description | Required |
| ---- | ---- | ----------- | -------- |
| id | string |  | No |
| district_id | integer |  | No |
| province_id | string |  | No |
| name | string |  | No |
| code | string |  | No |
| create_time | dateTime |  | No |
| update_time | dateTime |  | No |
| province | [DistrictProvince](#DistrictProvince) |  | No |
| sync_histories | [ dateTime ] |  | No |

#### v1LocationType

| Name | Type | Description | Required |
| ---- | ---- | ----------- | -------- |
| id | string |  | No |
| name | string |  | No |
| code | string |  | No |
| create_time | dateTime |  | No |
| update_time | dateTime |  | No |
| location_type_id | integer |  | No |
| sync_histories | [ dateTime ] |  | No |

#### v1PromotionStatus

| Name | Type | Description | Required |
| ---- | ---- | ----------- | -------- |
| v1PromotionStatus | string |  |  |

#### v1SearchAgentsRequestEqual

| Name | Type | Description | Required |
| ---- | ---- | ----------- | -------- |
| status | string |  | No |
| phones | [ string ] |  | No |

#### v1SearchAgentsRequestLike

| Name | Type | Description | Required |
| ---- | ---- | ----------- | -------- |
| phone | string |  | No |
| vendor | string |  | No |
| name | string |  | No |

#### v1SearchAgentsRequestQuery

| Name | Type | Description | Required |
| ---- | ---- | ----------- | -------- |
| list_id | [ string ] |  | Yes |

#### v1SearchAgentsResponse

| Name | Type | Description | Required |
| ---- | ---- | ----------- | -------- |
| agents | [ [v1Agent](#v1Agent) ] |  | No |
| pagination | [openapisapplicationv1Pagination](#openapisapplicationv1Pagination) |  | No |

#### v1Supplier

| Name | Type | Description | Required |
| ---- | ---- | ----------- | -------- |
| id | string |  | No |
| supplier_id | integer |  | No |
| name | string |  | No |
| status | string |  | No |
| create_time | dateTime |  | No |
| update_time | dateTime |  | No |
| phone | string |  | No |
| code | string |  | No |
| sync_histories | [ dateTime ] |  | No |

#### v1Vendor

| Name | Type | Description | Required |
| ---- | ---- | ----------- | -------- |
| id | string |  | No |
| company_id | string |  | No |
| create_by | string |  | No |
| name | string |  | No |
| image | string |  | No |
| active | boolean |  | No |
| code | string |  | No |
| phone | string |  | No |
| create_time | dateTime |  | No |
| update_time | dateTime |  | No |
| supplier_ids | [ string ] |  | No |
| district_id | string |  | No |
| address | string |  | No |
| sync_histories | [ dateTime ] |  | No |
| district | [v1District](#v1District) |  | No |
| suppliers | [ [v1Supplier](#v1Supplier) ] |  | No |

-------------------------------
### /v1/users

#### POST
##### Parameters

| Name | Located in | Description | Required | Schema |
| ---- | ---------- | ----------- | -------- | ---- |
| body | body |  | Yes | [v1CreateUserRequest](#v1CreateUserRequest) |

##### Responses

| Code | Description | Schema |
| ---- | ----------- | ------ |
| 200 | A successful response. | [v1User](#v1User) |
| default | An unexpected error response. | [rpcStatus](#rpcStatus) |

### /v1/users:login

#### POST
##### Parameters

| Name | Located in | Description | Required | Schema |
| ---- | ---------- | ----------- | -------- | ---- |
| body | body |  | Yes | [v1LoginRequest](#v1LoginRequest) |

##### Responses

| Code | Description | Schema |
| ---- | ----------- | ------ |
| 200 | A successful response. | [v1LoginResponse](#v1LoginResponse) |
| default | An unexpected error response. | [rpcStatus](#rpcStatus) |

### /v1/users:logout

#### POST
##### Responses

| Code | Description | Schema |
| ---- | ----------- | ------ |
| 200 | A successful response. |  |
| default | An unexpected error response. | [rpcStatus](#rpcStatus) |

### /v1/users:refresh-token

#### POST
##### Parameters

| Name | Located in | Description | Required | Schema |
| ---- | ---------- | ----------- | -------- | ---- |
| body | body |  | Yes | [v1RefreshTokenRequest](#v1RefreshTokenRequest) |

##### Responses

| Code | Description | Schema |
| ---- | ----------- | ------ |
| 200 | A successful response. | [v1RefreshTokenResponse](#v1RefreshTokenResponse) |
| default | An unexpected error response. | [rpcStatus](#rpcStatus) |

### Models


#### protobufAny

| Name | Type | Description | Required |
| ---- | ---- | ----------- | -------- |
| type_url | string |  | No |
| value | byte |  | No |

#### rpcStatus

| Name | Type | Description | Required |
| ---- | ---- | ----------- | -------- |
| code | integer |  | No |
| message | string |  | No |
| details | [ [protobufAny](#protobufAny) ] |  | No |

#### v1CreateUserRequest

| Name | Type | Description | Required |
| ---- | ---- | ----------- | -------- |
| company_id | string |  | No |
| name | string |  | No |
| phone | string |  | Yes |
| email | string |  | Yes |
| password | string |  | Yes |
| app_id | string |  | Yes |
| roles | [ [v1Role](#v1Role) ] |  | Yes |
| adress | string |  | No |

#### v1LoginRequest

| Name | Type | Description | Required |
| ---- | ---- | ----------- | -------- |
| username | string |  | No |
| password | string |  | No |

#### v1LoginResponse

| Name | Type | Description | Required |
| ---- | ---- | ----------- | -------- |
| access_token | string | REQUIRED.  The access token issued by the authorization server. | No |
| token_type | string | REQUIRED.  The type of the token issued as described in Section 7.1.  Value is case insensitive. | No |
| expires_in | integer | RECOMMENDED.  The lifetime in seconds of the access token.  For example, the value "3600" denotes that the access token will expire in one hour from the time the response was generated. If omitted, the authorization server SHOULD provide the expiration time via other means or document the default value. | No |
| refresh_token | string | grant_type REQUIRED.  Value MUST be set to "refresh_token".  refresh_token REQUIRED.  The refresh token issued to the client.  scope OPTIONAL.  The scope of the access request as described by Section 3.3.  The requested scope MUST NOT include any scope not originally granted by the resource owner, and if omitted is treated as equal to the scope originally granted by the resource owner.  Because refresh tokens are typically long-lasting credentials used to request additional access tokens, the refresh token is bound to the client to which it was issued.  If the client type is confidential or the client was issued client credentials (or assigned other authentication requirements), the client MUST authenticate with the authorization server as described in Section 3.2.1.  For example, the client makes the following HTTP request using transport-layer security (with extra line breaks for display purposes only):  POST /token HTTP/1.1 Host: server.example.com Authorization: Basic czZCaGRSa3F0MzpnWDFmQmF0M2JW Content-Type: application/x-www-form-urlencoded  grant_type=refresh_token&refresh_token=tGzv3JOkF0XG5Qx2TlKWIA | No |

#### v1RefreshTokenRequest

| Name | Type | Description | Required |
| ---- | ---- | ----------- | -------- |
| refresh_token | string |  | No |

#### v1RefreshTokenResponse

| Name | Type | Description | Required |
| ---- | ---- | ----------- | -------- |
| access_token | string | REQUIRED.  The access token issued by the authorization server. | No |
| token_type | string | REQUIRED.  The type of the token issued as described in Section 7.1.  Value is case insensitive. | No |
| expires_in | integer | RECOMMENDED.  The lifetime in seconds of the access token.  For example, the value "3600" denotes that the access token will expire in one hour from the time the response was generated. If omitted, the authorization server SHOULD provide the expiration time via other means or document the default value. | No |
| refresh_token | string | grant_type REQUIRED.  Value MUST be set to "refresh_token".  refresh_token REQUIRED.  The refresh token issued to the client.  scope OPTIONAL.  The scope of the access request as described by Section 3.3.  The requested scope MUST NOT include any scope not originally granted by the resource owner, and if omitted is treated as equal to the scope originally granted by the resource owner.  Because refresh tokens are typically long-lasting credentials used to request additional access tokens, the refresh token is bound to the client to which it was issued.  If the client type is confidential or the client was issued client credentials (or assigned other authentication requirements), the client MUST authenticate with the authorization server as described in Section 3.2.1.  For example, the client makes the following HTTP request using transport-layer security (with extra line breaks for display purposes only):  POST /token HTTP/1.1 Host: server.example.com Authorization: Basic czZCaGRSa3F0MzpnWDFmQmF0M2JW Content-Type: application/x-www-form-urlencoded  grant_type=refresh_token&refresh_token=tGzv3JOkF0XG5Qx2TlKWIA | No |

#### v1Role

| Name | Type | Description | Required |
| ---- | ---- | ----------- | -------- |
| v1Role | string |  |  |

#### v1User

| Name | Type | Description | Required |
| ---- | ---- | ----------- | -------- |
| id | string |  | No |
| company_id | string |  | No |
| name | string |  | No |
| email | string |  | No |
| phone | string |  | No |
| password | string |  | No |
| roles | [ string ] |  | No |
| app_id | string |  | No |
| adress | string |  | No |
| create_time | dateTime |  | No |
| update_time | dateTime |  | No |