# Dokumentasi API Cek Kuota

**Method :**
`POST`

**Endpoint XL/AXIS/THREE/INDOSAT :**
`http://api.projectxz.app/api/tools/cek-sidompul`

**Endpoint XL/AXIS/THREE/INDOSAT :**
`http://api.projectxz.app/api/tools/cek-tsel`

**Provider Support :**

> XL, AXIS, Indosat, TRI, Telkomsel

## Request

```bash
curl -X POST "http://api.projectxz.app/api/tools/cek-sidompul" \
-H "Content-Type: application/json" \
-d '{
  "key": "(key mu)",
  "nomor_hp": "(nomor yang di cek axis, xl, isat, tri)"
}'
```

## Request

```bash
curl -X POST "http://api.projectxz.app/api/tools/cek-tsel" \
-H "Content-Type: application/json" \
-d '{
  "key": "(key mu)",
  "nomor_hp": "(Telkomsel)"
}'
```


## Response Success (XL / AXIS)

```json
{
  "status": "SUCCESS",
  "biaya": 20,
  "saldo": 399998620,
  "data": {
    "status": "success",
    "code": 0,
    "data": {
      "success": true,
      "code": "000",
      "message": "",
      "data": {
        "subs_info": {
          "msisdn": "62877",
          "operator": "XL",
          "id_verified": "Sudah",
          "net_type": "4G",
          "tenure": "4 Tahun 1 Bulan",
          "exp_date": "16-06-2026",
          "grace_until": "16-07-2026",
          "volte": {
            "device": false,
            "area": false,
            "simcard": false
          }
        },
        "package_info": {
          "error_message": null,
          "packages": [
            {
              "name": "Bonus Paket Akrab",
              "expiry": "19-05-2026",
              "timestamp": 1779209999,
              "quotas": [
                {
                  "name": "Bonus myRewards",
                  "percent": 100,
                  "total": "6GB",
                  "remaining": "6GB"
                },
                {
                  "name": "Kuota Nasional",
                  "percent": 100,
                  "total": "8GB",
                  "remaining": "8GB"
                }
              ]
            }
          ]
        }
      }
    },
    "stderr": ""
  }
}
```


## Response Success (TRI / ISAT)

```json
{
  "status": "SUCCESS",
  "biaya": 20,
  "saldo": 399998600,
  "data": {
    "status": "0",
    "code": 0,
    "data": {
      "status": "0",
      "code": "26000",
      "message": "success",
      "transid": "SPSUP9142701779156594912679",
      "data": {
        "activationStatus": "Active",
        "bonstriDetails": {
          "loyaltyPoints": "0",
          "validityLoyaltyPoints": "226",
          "bonusPoints": "0",
          "pointstonexttierlevel": "2000",
          "totalPoints": "0"
        },
        "packdata": {
          "serviceclass": 637,
          "expireddate": "20270326",
          "status": "SUCCESS",
          "packageslist": [
            {
              "ServiceType": "Rating Discount",
              "ServiceName": "RFWABOOS20GB",
              "ServiceDescription": "Booster HiFi Air 20GB",
              "PackageCode": "RFWABOOS20GB",
              "PackageName": "RFWABOOS20GB",
              "StartDate": "14.05.2026",
              "EndDate": "27.02.2027",
              "EndTime": "13:14",
              "networkpackage": "PLAN_FWA_BOOSTER_20GB",
              "PackagePeriod": "0",
              "PeriodUnit": "",
              "BuyExtra": "N",
              "Unreg": "N",
              "UnregKeyword": "",
              "UnregShortcode": 0,
              "Quotas": [
                {
                  "name": "Kuota HiFi Air",
                  "description": "Kuota HiFi Air",
                  "initialQuota": 20480,
                  "usedQuota": 20480,
                  "remainingQuota": 20480,
                  "quotaUnit": "MB",
                  "benefitType": "DATA",
                  "expiryDate": 20270227,
                  "quotaSource": "NA",
                  "show": "ON",
                  "unlimitedFlag": "N",
                  "networkPackage": "PLAN_FWA_BOOSTER_20GB",
                  "showremaining": true,
                  "subtitle": "Booster HiFi Air 20GB",
                  "roaming": false,
                  "add_to_total": true,
                  "visibleForZone": false,
                  "displayInSubscriptionTab": false,
                  "isGoogleProduct": false,
                  "activeQuota": false,
                  "isSubscription": false
                }
              ],
              "buyextracatagory": "EXTRA QUOTA",
              "additional_info": "ups kamu kehabisan kuota",
              "total_data": 20971520,
              "total_voice": 0,
              "total_sms": 0,
              "total_rupia": 0,
              "expMsg": "Berakhir pada 27 Feb 2027",
              "reg_keyword": "RFWABOOS20GB",
              "familyOffer": "DONGLE",
              "showtop": true,
              "bonusSubType": "DONGLE",
              "displayInSubscriptionTab": false
            },
            {
              "ServiceType": "Rating Discount",
              "ServiceName": "HPBUN12ORI_Rev",
              "ServiceDescription": "SP HiFi Air 15GB selama 12 bln",
              "PackageCode": "HPBUN12ORI_Rev",
              "PackageName": "HPBUN12ORI_Rev",
              "StartDate": "04.03.2026",
              "EndDate": "27.02.2027",
              "EndTime": "13:14",
              "networkpackage": "PLAN_FWA_15GB_30D_SP",
              "PackagePeriod": "0",
              "PeriodUnit": "",
              "BuyExtra": "N",
              "Unreg": "N",
              "UnregKeyword": "",
              "UnregShortcode": 0,
              "Quotas": [
                {
                  "name": "Kuota FWA 15GB/30 hari",
                  "description": "Kuota FWA 15GB/30 hari",
                  "initialQuota": 15360,
                  "usedQuota": 15360,
                  "remainingQuota": 3789,
                  "quotaUnit": "MB",
                  "benefitType": "DATA",
                  "expiryDate": 20270227,
                  "quotaSource": "NA",
                  "show": "ON",
                  "unlimitedFlag": "N",
                  "networkPackage": "PLAN_FWA_15GB_30D_SP",
                  "showremaining": true,
                  "subtitle": "SP HiFi Air 15GB selama 12 bln",
                  "roaming": false,
                  "add_to_total": true,
                  "visibleForZone": false,
                  "displayInSubscriptionTab": false,
                  "isGoogleProduct": false,
                  "activeQuota": false,
                  "isSubscription": false
                }
              ],
              "buyextracatagory": "EXTRA QUOTA",
              "additional_info": "ups kamu kehabisan kuota",
              "total_data": 15728640,
              "total_voice": 0,
              "total_sms": 0,
              "total_rupia": 0,
              "expMsg": "Berakhir pada 27 Feb 2027",
              "reg_keyword": "HPBUN12ORI_Rev",
              "familyOffer": "DONGLE",
              "bonusSubType": "DONGLE",
              "displayInSubscriptionTab": false
            }
          ],
          "substype": "PREPAID",
          "tid": "SPSUP9142701779156594912679",
          "msisdn": "6289518477972"
        },
        "prepaidinfo": {
          "cardactiveuntil": "26 Mar 2027",
          "balance": "0",
          "graceperioduntil": "25 Apr 2027",
          "usersince": "04 March 2026",
          "expires": "Berlaku hingga 26 Mar 27",
          "activeuntil": "26 March 2027"
        },
        "status": "SUCCESS",
        "summary": {
          "data": {
            "usedquota": 36700160,
            "remainingquota": 24851456,
            "initialquota": 36700160,
            "quotaunit": "KB",
            "title": "DATA",
            "isunlimited": false
          },
          "roamingData": {
            "usedquota": 0,
            "remainingquota": 0,
            "initialquota": 0,
            "quotaunit": "KB",
            "isunlimited": false
          }
        },
        "customerinfo": {
          "sim4G": false,
          "corporateuser": false,
          "upgradeeligible": true,
          "lmsenrolled": false,
          "newuser": false
        },
        "smartAlerts": [
          {
            "color": "#dc3545",
            "title": "Oh tidak,<br>Kamu masih memiliki pembayaran yang belum selesai",
            "min": 0,
            "max": 0,
            "rule": "PAYMENT_REMINDER",
            "pageurl": "transactionhistory",
            "buttontext": "Riwayat Transaksi",
            "position": 0,
            "apiurl": "/personalization/attention",
            "promoimage": "",
            "datatype": "api",
            "datasource": "attention",
            "description": "",
            "fallback": 1,
            "ruleid": "5_2_0_ABOVE",
            "ctitle": "null",
            "promourl": "https://bimaplus.tri.co.id/en/deeplink?action=page&pagename=buy",
            "tabtitle": "Bayar Sekarang"
          },
          {
            "color": "#A69FF1-#00D7C2",
            "title": "Ada penawaran menarik buatmu, nih!",
            "min": 0,
            "max": 500,
            "rule": "CVM_OFFERS",
            "pageurl": "buy",
            "buttontext": "Lihat paket lainnya",
            "position": 5,
            "apiurl": "/personalization/rebuy",
            "promoimage": "https://bimaasset.ioh.co.id/assets/bima/imageassets/Contextual%20ID%20bima%20minibox.png",
            "datatype": "api",
            "datasource": "packages",
            "description": "Kami sudah pilihkan produk yang cocok untuk memaksimalkan keseruanmu ",
            "fallback": 0,
            "ruleid": "5_2_0_ABOVE",
            "ctitle": "NA",
            "promourl": "https://bimaplus.tri.co.id/product?id=2119582",
            "tabtitle": "Hot Promo"
          },
          {
            "color": "#00B091-#1CBFE7",
            "title": "Selamat Datang di bima+, beberapa hal yang bisa kamu lakukan untuk memulai",
            "min": 0,
            "max": 3,
            "rule": "CAMPAIGN_EXT_USER",
            "pageurl": "lifestyle",
            "buttontext": "",
            "position": 30,
            "apiurl": "/campaign/available?limit=5",
            "promoimage": "",
            "datatype": "api",
            "datasource": "vouchers",
            "description": "Klaim voucher gratis sekarang sebelum kehabisan",
            "fallback": 0,
            "ruleid": "5.4.0_N_ABOVE",
            "ctitle": "Need your attention<br>Hurry up check now",
            "tabtitle": "Voucher Gratis"
          }
        ],
        "dukapilstatus": "Registered",
        "emergencyCredit": {},
        "isInvoicegenerated": false,
        "sptravelonuse": false,
        "sptravelon_restricted": "imkas,impoin,kios,ucan,buy_content,rewards_tab",
        "zone": "Defend",
        "bonstri_joined": "0",
        "newuser": "false",
        "info": {
          "roaming": {
            "postpaid_icon": "https://bimaasset.ioh.co.id/assets/bima/icons/ic_Internet_globalpackage_bima.png",
            "prepaid_icon": "https://bimaasset.ioh.co.id/assets/bima/icons/ic_Internet_globalpackage_bima.png",
            "postpaid_package_icon": "https://bimaasset.ioh.co.id/assets/bima/icons/ic_Internet_globalpackage_bima.png",
            "prepaid_package_icon": "https://bimaasset.ioh.co.id/assets/bima/icons/ic_Internet_globalpackage_bima.png"
          },
          "eccard": {
            "icon": "https://myim3api.kloc.co/api/v1/image?id=379d9ee0-dc5d-4188-a8eb-a7afa0f3c6c4",
            "banner": "https://myim3api.kloc.co/api/v1/image?id=727a598d-f2bc-4956-b342-7e9bbb5fd80d"
          },
          "modules": "impoin,imkas,kios,ucan",
          "zeroquota_restricted": "impoin,imkas,kios"
        }
      }
    },
    "stderr": ""
  }
}
```
## Keterangan

> biaya = biaya pemotongan saldo  
> saldo = sisa saldo setelah request  
> nomor_hp = nomor target provider XL / AXIS / ISAT / TRI
