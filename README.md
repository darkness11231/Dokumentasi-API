# Dokumentasi API Cek Kuota

**Method :**
`POST`

**Endpoint :**
`http://xchannell.web.id/api/tools/cek-sidompul`

**Provider Support :**

> XL, AXIS, Indosat, TRI

## Request

```bash
curl -X POST "http://xchannell.web.id/api/tools/cek-sidompul" \
-H "Content-Type: application/json" \
-d '{
  "key": "(key mu)",
  "nomor_hp": "(nomor yang di cek axis, xl, isat, tri)"
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

## Keterangan

> biaya = biaya pemotongan saldo  
> saldo = sisa saldo setelah request  
> nomor_hp = nomor target provider XL / AXIS / ISAT / TRI
