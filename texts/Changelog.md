# <a name="changelog"></a> Changelog

## Table of Contents
- [Version 1.10](#v1.10.0.0.20181113)
- [Version 1.9](#v1.9.0.20180515)
- [Version 1.8](#v1.8.0.20171114)
- [Version 1.7](#v1.7.0.20170822)
- [Version 1.6](#v1.6.0.20170404)
- [Version 1.5](#v1.5.0.20170207)
- [Version 1.4](#v1.4.0.20161015)

## <a name="v1.10.0.0.20181113"></a> Version 1.10 (released 2018-11-13)
- available on Sandbox: 2018-08-14
- introduced version 1.10
- added value `1.10` for _SpecVersion_
- added method [Transaction/MultipartCapture](index.html#Payment_v1_Transaction_MultipartCapture) for capturing multiple parts of a transaction also supporting enhanced clearing for marketplaces
- added method [Transaction/MultipartFinalize](index.html#Payment_v1_Transaction_MultipartFinalize) to finalize a transaction that is still open for capturing additional parts
- added container _MarketPlace_ to [Transaction/Capture](index.html#Payment_v1_Transaction_Capture) request to support enhanced clearing for marketplaces
- removed container _Partial_ from [Transaction/Capture](index.html#Payment_v1_Transaction_Capture) request - see method [Transaction/MultipartCapture](index.html#Payment_v1_Transaction_MultipartCapture) for details
- replaced _TransactionId_ and _OrderId_ with _CaptureId_ in [Transaction/Capture](index.html#Payment_v1_Transaction_Capture) response to uniquely identify captures
- replaced container _TransactionReference_ with _CaptureReference_ in [Transaction/Refund](index.html#Payment_v1_Transaction_Refund) and [Transaction/AssertCapture](index.html#Payment_v1_Transaction_AssertCapture) request to uniquely identify captures
- added value `TWINT` for field `Type` in [Alias/Insert](index.html#Payment_v1_Alias_Insert) requests (only available in the Sandbox environment until further notice)
- added subcontainer `Twint` to container `PaymentMeans`

## <a name="v1.9.0.20180515"></a> Version 1.9 (released 2018-05-15)
- available on Sandbox: 2018-04-26
- introduced version 1.9
- added value `1.9` for _SpecVersion_
- replaced container _ThreeDs_ from previous versions with _Liability_ in [PaymentPage/Assert](index.html#Payment_v1_PaymentPage_Assert) and [Transaction/Initialize](index.html#Payment_v1_Transaction_Initialize) responses

## <a name="v1.8.0.20171114"></a> Version 1.8 (released 2017-11-14)
- available on Sandbox: 2017-11-02
- introduced version 1.8
- added value `1.8` for _SpecVersion_
- added _SixTransactionReference_ to [PaymentPage/Assert](index.html#Payment_v1_PaymentPage_Assert), [Transaction/AuthorizeDirect](index.html#Payment_v1_Transaction_AuthorizeDirect), [Transaction/AuthorizeReferenced](index.html#Payment_v1_Transaction_AuthorizeReferenced), [Transaction/RefundDirect](index.html#Payment_v1_Transaction_RefundDirect) and [Transaction/Refund](index.html#Payment_v1_Transaction_Refund) responses for Omni Channel use cases
- added method [OmniChannel/AcquireTransaction](index.html#Payment_v1_OmniChannel_AcquireTransaction) for retrieving a previously authorized transaction from another channel
- added method [OmniChannel/InsertAlias](index.html#Payment_v1_OmniChannel_InsertAlias) for retrieving an alias for a card used in a previously authorized transaction from another channel
- added container _CardForm_ for [Alias/Insert](index.html#Payment_v1_Alias_Insert) and [Transaction/Initialize](index.html#Payment_v1_Transaction_Initialize) requests for adjusting the card form's mandatory fields

## <a name="v1.7.0.20170822"></a> Version 1.7 (released 2017-08-22)
- available on Sandbox: 2017-08-03
- introduced version 1.7
- added value `1.7` for _SpecVersion_
- added value `TWINT` for _Brand.PaymentMethod_
- added _ApprovalCode_ to [PaymentPage/Assert](index.html#Payment_v1_PaymentPage_Assert), [Transaction/AuthorizeDirect](index.html#Payment_v1_Transaction_AuthorizeDirect), [Transaction/AuthorizeReferenced](index.html#Payment_v1_Transaction_AuthorizeReferenced), [Transaction/RefundDirect](index.html#Payment_v1_Transaction_RefundDirect) and [Transaction/Refund](index.html#Payment_v1_Transaction_Refund) responses
- added _PaymentMethods_ to [Transaction/Initialize](index.html#Payment_v1_Transaction_Initialize) and [Alias/Insert](index.html#Payment_v1_Alias_Insert) requests
- increased number of concurrent Basic Authentication credentials to 10
- improved description for pending statuses

## <a name="v1.6.0.20170404"></a> Version 1.6 (released 2017-04-04)
- available on Sandbox: 2017-03-14
- introduced version 1.6
- added value `1.6` for _SpecVersion_
- added container _Check_ for [Alias/InsertDirect](index.html#Payment_v1_Alias_InsertDirect) request
- added container _CheckResult_ for [Alias/AssertInsert](index.html#Payment_v1_Alias_AssertInsert) and [Alias/InsertDirect](index.html#Payment_v1_Alias_InsertDirect) responses

## <a name="v1.5.0.20170207"></a> Version 1.5 (released 2017-02-07)
- introduced version 1.5
- added value `1.5` for _SpecVersion_
- added method [Transaction/AssertCapture](index.html#Payment_v1_Transaction_AssertCapture) for checking the status of a pending capture (currently needed for paydirekt)
- added method [Transaction/AssertRefund](index.html#Payment_v1_Transaction_AssertRefund) for checking the status of a pending refund (currently needed for paydirekt)
- added container _PendingNotification_ for [Transaction/Capture](index.html#Payment_v1_Transaction_Capture) requests for notification settings on pending captures (currently needed for paydirekt)
- added container _PendingNotification_ for [Transaction/Refund](index.html#Payment_v1_Transaction_Refund) requests for notification settings on pending captures (currently needed for paydirekt)
- added _Status_ in  [Transaction/Capture](index.html#Payment_v1_Transaction_Capture) responses to indicate the status of a capture
- changed _Date_ in  [Transaction/Capture](index.html#Payment_v1_Transaction_Capture) responses to optional, e.g. for pending captures
- changed [PaymentPage/Initialize](index.html#Payment_v1_PaymentPage_Initialize) request to allow _BillingAddressForm.Display_ and _DeliveryAddressForm.Display_ both set to `true` at the same time
- added _ContentSecurityEnabled_ to _Styling_ container to control Content Security Policy
- corrected type documentation for _CountrySubdivisionCode_ to "_AlphaNumeric_" in the address containers

## <a name="v1.4.0.20161015"></a> Version 1.4 (released 2016-10-15)
- new version 1.4
  - added value `1.4` for _SpecVersion_
  - added option _SuppressDcc_ for [Transaction/AuthorizeReferenced](index.html#Payment_v1_Transaction_AuthorizeReferenced)
  - added values `BANCONTACT` and `PAYDIREKT` for _Brand.PaymentMethod_ and _PaymentMethods_ in [PaymentPage/Initialize](index.html#Payment_v1_PaymentPage_Initialize)
  - added validation for element _Payment.MandateId_
  - added option _ConfigSet_ for [PaymentPage/Initialize](index.html#Payment_v1_PaymentPage_Initialize)
- added a note that partial captures are currently only supported for PayPal
- added a note that values for AliasID are case-insensitive
- corrected example for [Transaction/AuthorizeDirect](index.html#Payment_v1_Transaction_AuthorizeDirect)
- corrected example for [Transaction/AuthorizeReferenced](index.html#Payment_v1_Transaction_AuthorizeReferenced)
- corrected example for [Transaction/Authorize](index.html#Payment_v1_Transaction_Authorize)
- corrected example for [Transaction/Initialize](index.html#Payment_v1_Transaction_Initialize)
- improved description for _TransactionReference_
- corrected example for _BillpayCapture.DelayInDays_
- improved description for _ReturnUrls_
