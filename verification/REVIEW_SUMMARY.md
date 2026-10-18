# 検証まとめ

- `erc.rpt`: 0エラー、0警告
- `drc.rpt`: 0違反、未配線0、フットプリントエラー0
- 電源ネット: USB_5V/DC_RAW → JP1 → REG_IN → 3.3 V buck → JP2 → SYS_3V3
- 書き込み電源: A105 PROG_3V3 → JP2 → SYS_3V3
- LED電力: DC_RAW → LED+、LED- → Q1 → GND
- USB信号: D+/D-未接続
- 制約: JP1/JP2の両側ブリッジ禁止、同時給電禁止、センタープラス限定

計算機上のERC/DRCは合格していますが、降圧回路の実負荷安定性、MOSFET温度、無線性能は初回試作で確認が必要です。
