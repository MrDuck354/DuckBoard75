# DuckBoard 75

## Project Goals:
To create a basic 75% keyboard
By creating this keyboard, I will be learning how to 3D model/print on OnShape, how to create a PCB on KiCad and how to solder.

## Steps
Made a PCB on KiCad with a arduino nano and switches
<img width="1621" height="890" alt="Screenshot 2026-07-30 192301" src="https://github.com/user-attachments/assets/0c2e8957-9f6b-452c-b6f7-c63aaabeb616" />

Made a plate on OnShape using the PCB as a reference
<img width="1138" height="458" alt="Screenshot 2026-08-10 212719" src="https://github.com/user-attachments/assets/d7d71d5a-7a56-462d-b94d-6c9b631481f5" />
<img width="1406" height="604" alt="Screenshot 2026-08-10 212730" src="https://github.com/user-attachments/assets/d6777845-53f0-4c0e-b471-7c0d1d67d394" />

Made a bottom case
<img width="1464" height="799" alt="Screenshot 2026-08-01 111654" src="https://github.com/user-attachments/assets/d205e84c-2959-47d1-85b4-aad2c72d8d11" />
<img width="623" height="459" alt="Screenshot 2026-08-10 212657" src="https://github.com/user-attachments/assets/57312178-023c-4205-915d-2defdc1220f8" />

Created the firmware
[Completed](duckboard_firmware)

Soldered the electronics together
(Not yet completed)

## OnShape link
[OnShape Link](OnShapeLink)

## Bill of Materials
[BOM.csv](DuckBoard%2075%20BOM%20-%20DuckBoard%2075%20BOM%20-%20Sheet1.csv)
| Item | Price (USD) | QTY | Purpose | Total + Shipping |
| --- | --- | --- | --- | --- |
| [PCB]([https://github.com](https://cart.jlcpcb.com/quote?spm=jlcpcb.Public.2006)) | $27.40 | 5 (minimum) | Electronics for keyboard |  |
| [M2 Screws]([https://github.com](https://www.aliexpress.com/item/1005004527586307.html?spm=a2g0o.detail.0.0.11c3fgvnfgvnbD&mp=1&pdp_npi=6%40dis%21USD%21USD+1.13%21USD+1.11%21%21USD+1.11%21%21%21%402103212317823526741237199ea06e%2112000029486656873%21ct%21US%217547000002%21%211%210%21&gatewayAdapt=usa2glo4itemAdapt)) | $2.33 | 1 | To hold everything together |  |
| [Keycaps]([https://github.com](https://www.aliexpress.com/item/1005004527586307.html?spm=a2g0o.detail.0.0.11c3fgvnfgvnbD&mp=1&pdp_npi=6%40dis%21USD%21USD+1.13%21USD+1.11%21%21USD+1.11%21%21%21%402103212317823526741237199ea06e%2112000029486656873%21ct%21US%217547000002%21%211%210%21&gatewayAdapt=usa2glo4itemAdapt)) | $6.93 | 1 | Keycaps |  |
| [Stabilizers]([https://github.com](https://www.aliexpress.com/item/1005006528731543.html?spm=a2g0o.productlist.0.0.112352680K8Aiv&mp=1&pdp_npi=6%40dis%21USD%21USD+8.16%21USD+7.46%21%21USD+7.46%21%21%21%402103212317823524874202004ea06e%2112000037543723490%21ct%21US%217547000002%21%211%210%21&gatewayAdapt=usa2glo4itemAdapt)) | $8.84 | 1 | Stabilizers |  |
| [Diodes]([https://github.com](https://www.aliexpress.com/item/1005002339916163.html?spm=a2g0o.productlist.main.4.6cb16ae2c2K9iQ&aem_p4p_detail=202607311717321159445797392080000109962&algo_pvid=60e80187-334d-4970-9369-da9bf1ee4b9f&algo_exp_id=60e80187-334d-4970-9369-da9bf1ee4b9f-3&pdp_ext_f=%7B%22order%22%3A%221282%22%2C%22eval%22%3A%221%22%2C%22fromPage%22%3A%22search%22%7D&pdp_npi=6%40dis%21USD%210.89%210.87%21%21%210.89%210.87%21%402101de2517855434524457575e0cf2%2112000020175180916%21sea%21NZ%217985869037%21ABX%211%210%21n_tag%3A-29910%3Bd%3Af3154200%3Bm03_new_user%3A-29895&curPageLogUid=11r81NCdmT7s&utparam-url=scene%3Asearch%7Cquery_from%3A%7Cx_object_id%3A1005002339916163%7C_p_origin_prod%3A&search_p4p_id=202607311717321159445797392080000109962_1)) | $0.87 | 1 | to control flow of electricity |  |
| [Switches]([https://github.com](https://www.aliexpress.com/item/1005004285423123.html?spm=a2g0o.productlist.main.11.2f361b6e73HJZu&algo_pvid=a090be33-1bfd-4105-8713-c38f03b5d6f4&algo_exp_id=a090be33-1bfd-4105-8713-c38f03b5d6f4-10&pdp_ext_f=%7B%22order%22%3A%2213737%22%2C%22spu_best_type%22%3A%22price%22%2C%22eval%22%3A%221%22%2C%22fromPage%22%3A%22search%22%7D&pdp_npi=6%40dis%21USD%212.87%210.99%21%21%212.87%210.99%21%402101e7a317855436822738413e0d41%2112000028628937373%21sea%21NZ%217985869037%21ABX%211%210%21n_tag%3A-29910%3Bd%3Af3154200%3Bm03_new_user%3A-29895%3BpisId%3A5000000210976560&curPageLogUid=kVSF8tEkUPWA&utparam-url=scene%3Asearch%7Cquery_from%3A%7Cx_object_id%3A1005004285423123%7C_p_origin_prod%3A)) | $3.53 | 90pcs | switches |  |
| [Micro Controller]([https://github.com](https://www.aliexpress.com/p/trade/confirm.html?shoppingCartIdString=81025824138227,81025930773702,81025824138112&shopcartIds=81025824138227,81025930773702,81025824138112&channelInfo=%7B%22sourceType%22%3A%22nn_mix%22%7D&aff_fcid=undefined)) | $2.64 | 1 | to control everything |  |
| [Solder Wire]([https://github.com](https://www.aliexpress.com/p/trade/confirm.html?shoppingCartIdString=81025824138227,81025930773702,81025824138112&shopcartIds=81025824138227,81025930773702,81025824138112&channelInfo=%7B%22sourceType%22%3A%22nn_mix%22%7D&aff_fcid=undefined)) | $1.32 | 1 | to connect electronics |  |
| 3D printing costs| $20 | 1 | to create the case| |
| AliExpress Shipping | $6.50 |  | To get the items |  |
| JLCPCB Shipping | $20.69 |  | To get the PCB |  |
|  |  |  |  | $94 |
