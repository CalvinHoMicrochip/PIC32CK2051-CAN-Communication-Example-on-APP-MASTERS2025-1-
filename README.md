# PIC32CK2051-CAN-Communication-Example-on-APP-MASTERS2025-1
# 這是一個用來驗證 APP-MASTERS25-1 上 PIC32CK CAN 通信的入門程式

* PIC32CK2051 CAN Test Project 在 MPLAB Harmony 中 CAN1 Module 的設定如下
  * CAN1 規劃為簡單的 Classic CAN
    * Bit Rate : 125K (因為 C20 & C23 出廠時安裝的電容值有錯，所以如果要高於 125K 的 Bit Rate 必須將這兩個電容移除或是改成 47pF )
    * Use RXFIFO0
    * Use TXFIFO
    * 使用 Filter0 來過濾 0x100 ~ 0x3FF 間的 Standard ID(11-bits), 這是為了方便做 Demo. 在製作多個 Ｎode 時可以不用一直修改 MCC Harmony CAN1 的 Configuration
      
<img width="635" height="234" alt="image" src="https://github.com/user-attachments/assets/8a275629-ce5e-4afb-8f89-18204b66bb66" />

<img width="1291" height="710" alt="image" src="https://github.com/user-attachments/assets/036d16ef-0022-4e24-9c90-4fb6c4c8878a" />

* main.c 中，對 CAN 的主要定義如下 :
  * CAN_TXID
  * CAN_RXID
<img width="999" height="482" alt="image" src="https://github.com/user-attachments/assets/2ad06b2a-18a5-420b-b237-cae8ec9719f3" />

<img width="999" height="565" alt="image" src="https://github.com/user-attachments/assets/b16e39d4-e9c9-472c-bc5c-c95debb65170" />



