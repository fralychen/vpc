# AllocateEipAddress {#reference_i4w_xmt_ndb .reference}

Create an Elastic IP address \(EIP\).

An available EIP is randomly allocated in the specified region after this API is called. EIP supports ICMP, TCP, and UDP protocols, but does not support IGMP and SCTP protocols.

## Request parameters {#section_cch_pjg_mdb .section}

|Name|Type|Required|Description|
|:---|:---|:-------|:----------|
|Action|String|Yes| The action to perform. Valid value:

 AllocateEipAddress

 |
|RegionId|String|Yes| The region of the EIP.

 You can obtain the region ID by calling the DescribeRegions API.

 |
|Bandwidth|String|No| The peak bandwidth in Mbps of the EIP. The default value is 5.

 |
|InternetChargeType|String| No| The billing method of the EIP. Valid values:

-   PayByTraffic: EIP is charged by traffic.


 |
|InstanceChargeType|String|No| The payment method of the EIP. Valid values:

 -   PostPaid \(Default\): Pay-As-You-Go


 |
|ClientToken|String| No| A client token used to guarantee the idempotence of requests. 

 This parameter value is generated by the client and must be unique. It cannot exceed 64 ASCII characters.

 |

## Response parameters {#section_ugs_f1g_cz .section}

|Name|Type|Description|
|:---|:---|:----------|
|RequestId|String|The ID of the request.|
|EipAddress|String|The allocated IP address.|
|AllocationId|String|The ID of the EIP.|

## Examples {#section_ix5_h1g_cz .section}

**Request example**

``` {#AllocateEipAddress}
https://vpc.aliyuncs.com/?Action=AllocateEipAddress
&amp;amp;RegionId=cn-beijing
&amp;CommonParameters
```

**Response example**

-   XML format

    ```
    &amp;lt;? xml version="1.0" encoding="UTF-8" ? >
    &amp;lt;AllocateEipAddressResponse&gt;
        &amp;lt;AllocationId&gt;eip-25877c70x&amp;lt;/AllocationId&gt;
        &amp;lt;EipAddress&gt;123.56.0.206&amp;lt;/EipAddress&gt;
        &amp;lt;RequestId&gt;B6B9F518-60F8-4D81-9242-1207B356754D&amp;lt;/RequestId&gt;
    &amp;lt;/AllocateEipAddressResponse&gt;
    ```

-   JSON format

    ```
    {
      "AllocationId": "eip-25877c70x",
      "EipAddress": "123.56.0.206",
      "RequestId": "B6B9F518-60F8-4D81-9242-1207B356754D"
    }
    ```


