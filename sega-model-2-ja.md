# Sega Model 2 日本語訳

Sega Retro「Sega Model 2」の日本語訳です。本文・技術仕様・ゲーム一覧・注記・参考文献を収録しています。

- 原著者：Sega Retro contributors（Sega Retroの寄稿者）
- 原文：[Sega Model 2](https://segaretro.org/Sega_Model_2)
- 翻訳対象：[版ID 1149915](https://segaretro.org/index.php?title=Sega_Model_2&oldid=1149915)
- 著者・改訂履歴：[ページ履歴](https://segaretro.org/index.php?title=Sega_Model_2&action=history)
- 原文および本翻訳のライセンス：[Creative Commons Attribution 4.0 International（CC BY 4.0）](https://creativecommons.org/licenses/by/4.0/)
- 翻訳・編集日：2026年10月14日

本ページは原文の翻訳・翻案であり、Sega Retroやセガによる公式日本語版ではありません。原文の数値、単位、年代、注記番号を保持し、見出しとレイアウトを再構成し、引用発言は意味を保って日本語の間接話法にしています。原文にある写真、ロゴ、雑誌・資料のスキャンは転載していません。画像類については原ページをご覧ください。本文のライセンス表示は、リンク先の第三者資料や画像にまで適用されるものではありません。

**数値に関する注意：** これは原文の翻訳であり、仕様の独立した検証や訂正ではありません。たとえば原文の「24 Hz HSync」や「80 MAC operations/sec」、集計値と内訳の差異なども原文どおり残しています。資料間の違いについては、各注記と参考文献をご確認ください。

## 基本情報

| 項目 | 内容 |
| --- | --- |
| 名称 | Sega Model 2（モデル2） |
| メーカー | Sega Enterprises, Ltd. |
| 派生モデル | Model 2A-CRX、Model 2B-CRX、Model 2C-CRX |
| 拡張基板 | DSB1／DSB2（Model 2C-CRX） |

## 概要

Sega Model 2（モデル2）は、セガがSega Model 1基板の後継として1993年に初めて登場させたアーケード用システム基板である。Model 1のハードウェアを発展させたもので、特にテクスチャを貼り付けたポリゴンを導入した点が大きく、当時としてはよりリアルな3Dグラフィックスを可能にした。

Model 2基板はアーケード業界における重要な節目となり、Daytona USA、Virtua Cop、Sega Rally Championship、Dead or Alive、Virtua Striker、Cyber Troopers Virtual-On、The House of the Deadなど、1990年代を代表する複数のアーケードシリーズの誕生を支えた。1996年にはSega Model 3が後継となった。

## ハードウェア

Model 2はModel 1の直接の後継として設計された。先代と同じく、アーケード事業者向けのプリント基板セットとして、またはセガが製作した専用筐体に組み込まれる形で提供された。General Electricがリアルタイムのテクスチャマッピング用ASICをセガに持ちかけたことをきっかけに誕生し、1992年8月の業務提携につながった。[[3]](#ref-3) 基板の製作には約1年を要した。[[3]](#ref-3)

Model 1からModel 2への最も目立つ進歩はテクスチャマッピングである。先代が対応していた単色のフラットシェーディングという制限を超え、ポリゴンにビットマップ画像を貼り付けられるようになった。Model 2では、テクスチャフィルタリングとテクスチャのアンチエイリアシング[[4]](#ref-4)、さらにトライリニアフィルタリングも導入された。[[2]](#ref-2) テクスチャ付きポリゴンを毎秒500,000個処理でき[[5]](#ref-5)、トライリニアフィルタリング[[2]](#ref-2)を含むすべてのハードウェア効果[[6]](#ref-6)を使用した場合は毎秒300,000ポリゴンを処理できた。[[3]](#ref-3) 当時最も強力なゲームシステムであり、登場から5年後の1998年のPC用グラフィックスカードに相当する性能だった。[[2]](#ref-2)

このシステムには、初代Model 2、Model 2A-CRX、Model 2B-CRX、Model 2C-CRXの計4種類がある。Model 2と2A-CRXは、ジオメトリ処理用コードを内部に備えたカスタムDSPを使用する。一方、2B-CRXと2C-CRXは詳細な資料が公開されているDSPを使用し、起動時にジオメトリ処理用コードをDSPへ転送する。

鈴木裕によれば、Fighting Vipers向けに開発されたSega Model 2B-CRX基板は、処理速度がやや速く、より多くのポリゴンを表示する際の応答性も高いという。[[7]](#ref-7)


## 技術仕様

### Model 2

- 基板構成：CPU基板、ビデオ基板、通信基板、ROM基板、サウンド基板、フィードバックドライバー基板[[8]](#ref-8)
- リビジョン：CPU基板 837-10071（50 MHz）、ビデオ基板 837-10072（50 MHz）、通信基板 837-10537、ROM基板 834-10798、サウンド基板 837-8679（20 MHz）、ドライブ基板 838-10646[[9]](#ref-9)
- メインCPU：Intel i960-KB @ 25 MHz[[10]](#ref-10)[[11]](#ref-11)
  - 固定小数点演算：32‑bit RISC命令 @ 25 MIPS[[12]](#ref-12)
  - 浮動小数点演算ユニット：32/64/80‑bit演算 @ 13.6 MFLOPS[[11]](#ref-11)
  - バス幅：32‑bit
- 追加CPU：2x Zilog Z80（8/16‑bit命令 @ 1.74 MIPS）
  - 通信基板：8 MHz[[9]](#ref-9)[[13]](#ref-13)（1.16 MIPS）
  - フィードバックドライバー：4 MHz[[8]](#ref-8)（0.58 MIPS）

#### サウンド

- サウンドCPU：Motorola 68000 @ 10 MHz（16/32‑bit命令 @ 1.75 MIPS）
- サウンドチップ：2x Sega 315‑5560 MultiPCM
- PCMチャンネル数：56
- PCMサンプルROM：最大16 MB（PCMチップあたり8 MB）
- PCM音質：ビット深度16‑bit、サンプリングレート44.1 kHz（CD音質）[[14]](#ref-14)
- サウンドタイマー：Yamaha YM3438 @ 8 MHz（Model 2のみ）

#### グラフィックス

Sega Model 2のグラフィックス仕様：[[15]](#ref-15)[[8]](#ref-8)[[16]](#ref-16)

- GPU：
  - 6x Fujitsu TGP MB86234
  - Segaビデオ基板 837-10072
- GPUジオメトリエンジンDSPコプロセッサ：6x Fujitsu TGP MB86234 @ 16 MHz[[17]](#ref-17)[[18]](#ref-18)[[9]](#ref-9)
  - リビジョン：315‑5673、315‑5677、2x 315‑5678、2x 315‑5679（後に1994年、2x 315‑5679Bに更新）
  - コプロセッサの機能：浮動小数点演算機能、軸回転演算機能、3D行列演算機能、ALU、DMAコントローラー、T&L（座標変換、クリッピング、ライティング）[[19]](#ref-19)
  - 命令セット：32‑bit命令、480 MIPS（各80 MIPS）[[n 1]](#note-1)
  - 固定小数点演算：192 MIPS（各32 MIPS）[[n 2]](#note-2)
  - 浮動小数点演算ユニット：96 MFLOPS（各16 MFLOPS）[[n 3]](#note-3)
  - バス幅：192‑bit（各32‑bit）
  - 注記：CPU基板上に搭載。DSPには、コプロセッサ機能とT&L機能を実現するため、セガ独自のマイクロコードによる変更が施されている。[[19]](#ref-19)
- GPUグラフィックスカード：Segaビデオ基板 837-10072 @ 50 MHz[[9]](#ref-9)[[21]](#ref-21)
  - セガ製Zソート／クリッピング用チップセット：315‑5644（32 MHz）、315‑5645（32 MHz）、315‑5712（40 MHz）、2x 315‑5725（50 MHz）
  - Lockheed Martin製ラスタライズ／テクスチャマッピング用プロセッサ：315‑5646（50 MHz）、315‑5647（50 MHz）
  - Sega System 24タイルマップエンジン：315‑5292タイルマップジェネレーター（32 MHz）[[22]](#ref-22)[[23]](#ref-23)
- ディスプレイ：最大50-inchのディスプレイ[[24]](#ref-24)
- 表示解像度：496×384 pixels、水平同期（HSync）24 Hz、プログレッシブ走査（ノンインターレース）、ダブルバッファリング[[15]](#ref-15)
- オーバースキャン解像度：656×496
- ピクセルクロック：19.523 MHz
- リフレッシュレート：60 Hz、57.52416 Hz、30 Hz[[15]](#ref-15)
- フレームレート：60 FPS、[[25]](#ref-25) 57.52416 FPS、30 FPS
- 色深度：65,536（16bpp）、16,777,216（24bpp）、[[5]](#ref-5) 256（8bpp）
- グラフィックスハードウェアの機能：フラットシェーディング、テクスチャマッピング、パースペクティブ補正、テクスチャフィルタリング、テクスチャのアンチエイリアシング、マイクロテクスチャ、拡散反射、鏡面反射、スペキュラーライティング、アルファブレンディング、透明処理、ラスタライズ、ミップマッピング、LOD、[[15]](#ref-15) Zバッファリング、ポイントサンプリング、バイリニアフィルタリング、トライリニアフィルタリング[[2]](#ref-2)
- テクスチャマップ解像度：最大1024×2048 pixels
- マイクロテクスチャのサイズ：最大128×128 pixels
- 演算性能：110 MFLOPS（浮動小数点）、210 MIPS（固定小数点）[[n 4]](#note-4)
  - 加算：61 million adds/sec（浮動小数点）、110 million adds/sec（固定小数点）[[n 5]](#note-5)
  - 乗算：61 million multiplies/sec（浮動小数点）、110 million multiplies/sec（固定小数点）[[n 6]](#note-6)
  - 除算：30 million divides/sec[[n 7]](#note-7)
- ジオメトリ変換：6 million vertices/sec、[[n 8]](#note-8) 2 million polygons/sec[[n 9]](#note-9)
- フラットライティング：1.2 million polygons/sec（浮動小数点）、[[n 10]](#note-10) 2 million polygons/sec（固定小数点）[[n 11]](#note-11)
- スペキュラーライティング：900,000 polygons/sec[[n 12]](#note-12)
- グーローライティング：880,000 polygons/sec（浮動小数点）、[[n 13]](#note-13) 1.5 million polygons/sec（固定小数点）[[n 14]](#note-14)
- レンダリングのフィルレート：110 MPixels/s（16bpp）、230 MPixels/s（8bpp）、260 MPixels/s（4bpp）
  - ポリゴン：100 MPixels/s（16bpp）、200 MPixels/s（8bpp）[[n 15]](#note-15)
  - タイルマップ：15 MPixels/s（16bpp）、30 MPixels/s（8bpp）、61 MPixels/s（4bpp）[[n 16]](#note-16)
- ポリゴン描画性能：100 MPixels/s、900,000 vectors/sec
- テクスチャマッピング性能：100 MTexels/s、ライティング
  - 900,000 polygons/sec：スペキュラー、100-texelのポリゴン
  - 500,000 polygons/sec：[[5]](#ref-5) スペキュラー、200-texelのポリゴン
  - 300,000 polygons/sec：すべてのハードウェアエフェクト、[[6]](#ref-6) トライリニアフィルタリング、[[2]](#ref-2) スペキュラー、300-texelのポリゴン
  - 300,000 polygons/sec：グーローシェーディング（ソフトウェア）、32-texelのポリゴン[[n 17]](#note-17)
- ハードウェアサポート：モーションキャプチャー

#### メモリ

- メモリ：最大62 MB（メイン10,881 KB、ビデオ35,460 KB、オーディオ16,960 KB、その他18 KB）
- システムRAM：9776 KB（9.546875 MB）[[15]](#ref-15)
  - メインRAM：1152 KB（1.125 MB）
  - VRAM：5984 KB（フレームバッファVRAM 1 MB、コプロセッサバッファSRAM/SDRAM 64 KB、テクスチャSRAM/SDRAM 4 MB、輝度128 KB、ジオメトリ32 KB、タイル576 KB、色64 KB）
  - オーディオRAM：576 KB
  - その他のRAM：2064 KB（バックアップSRAM/NVRAM 16 KB、追加RAM 2 MB）
- プロセッサ内部キャッシュ：36.75 KB
  - CPUキャッシュ：768 bytes[[10]](#ref-10)
  - TGP内部RAMキャッシュ：36 KB（TGPあたり6 KB）[[18]](#ref-18)
- ゲームROM：最大54.25 MB
  - メインROM：9.5 MB（EPROM、MROM）
  - ビデオROM：28.75 MB（MROM）
  - オーディオROM：16 MB（MROM）

#### 帯域幅

- システムRAM帯域幅：982 MB/s
  - メインRAM帯域幅：78.7 MB/s
    - i960：66.7 MB/s[[30]](#ref-30)
    - Z80：12 MB/s[[n 18]](#note-18)
  - VRAM帯域幅：883.34066 MB/s[[9]](#ref-9)[[21]](#ref-21)
    - TGP：384 MB/s[[n 19]](#note-19)
    - ビデオ基板：499.34066 MB/s
      - 315‑5292 & 315‑5644：30.769232 MB/s[[n 20]](#note-20)
      - 315‑5645：28.571428 MB/s[[n 21]](#note-21)
      - 315‑5646 & 315‑5647：400 MB/s[[n 22]](#note-22)
      - 315‑5712：40 MB/s[[n 23]](#note-23)
  - オーディオRAM帯域幅：20 MB/s[[n 24]](#note-24)
- プロセッサ内部キャッシュ帯域幅：484 MB/s
  - CPUキャッシュ：100 MB/s[[n 25]](#note-25)
  - TGP内部RAMキャッシュ：384 MB/s[[n 26]](#note-26)
- ゲームROM帯域幅：933–1000 MB/s[[n 27]](#note-27)[[9]](#ref-9)[[8]](#ref-8)
  - EPROM：133–200 MB/s[[n 28]](#note-28)
  - MROM：800 MB/s[[n 29]](#note-29)

### Model 2A-CRX

1994年に登場したModel 2A-CRXでは、サウンド機能の強化とROM容量の増加が行われた。

- サウンドCPU：Motorola 68000 @ 12 MHz（16/32‑bit命令 @ 2.1 MIPS）
- サウンドチップ：Yamaha SCSP
- PCMチャンネル数：32
- PCMサンプルROM：最大16 MB
- PCM音質：ビット深度16‑bit、サンプリングレート44.1 kHz（CD音質）
- SCSPの機能：128-step DSP、32チャンネルのPCM/FM/MIDI/LFO
- メモリ：最大142 MB（メイン35,969 KB、ビデオ90,244 KB、オーディオ16,960 KB、その他2064 KB）
- システムRAM：9776 KB（9.546875 MB）
  - メインRAM：1152 KB（1.125 MB）
  - VRAM：5984 KB（5.84375 MB）
  - オーディオRAM：576 KB
  - その他のRAM：2064 KB（2.015625 MB）
- プロセッサ内部キャッシュ：36.75 KB
  - CPUキャッシュ：768 bytes
  - TGP内部RAMキャッシュ：36 KB
- ゲームROM：最大132.25 MB（メイン34 MB、ビデオ82.25 MB、[[37]](#ref-37) オーディオ16 MB）

### Model 2B-CRX

1995年に登場したModel 2B-CRXでは、ジオメトリエンジンDSPコプロセッサの強化とVRAMの増設が行われた。[[15]](#ref-15)

- GPUジオメトリエンジンDSPコプロセッサ：2x ADSP-21062 SHARC @ 40 MHz[[38]](#ref-38)
  - コプロセッサの機能：浮動小数点演算機能、軸回転演算機能、3D行列演算機能、SOC、ALU、T&L
  - 固定小数点命令：32‑bit命令、80 MIPS（各40 MIPS）
  - 浮動小数点演算ユニット：32/40‑bit演算、240 MFLOPS（各120 MFLOPS）、80 MAC operations/sec（各40 MACs/sec）
  - データバス幅：96‑bit（各48‑bit）
  - DMAコントローラー：20 DMAチャンネル（各10チャンネル）、SHARCあたり80 MHzのメモリアクセス（デュアルメモリアクセス）、転送速度480 MB/s（各240 MB/s）
- ライティング演算：240 MFLOPS
  - フラットライティング：1.8 million polygons/sec（浮動小数点）[[n 30]](#note-30)
  - スペキュラーライティング：1.5 million polygons/sec[[n 31]](#note-31)
  - グーローライティング：1.3 million polygons/sec（浮動小数点）[[n 32]](#note-32)
- レンダリングのフィルレート：130 MPixels/s（16bpp）、270 MPixels/s（8bpp）、300 MPixels/s（4bpp）
  - ポリゴン：120 MPixels/s（16bpp）、[[n 33]](#note-33) 240 MPixels/s（8bpp）
  - タイルマップ：15 MPixels/s（16bpp）、30 MPixels/s（8bpp）、61 MPixels/s（4bpp）
- テクスチャマッピング性能：120 MTexels/s、ライティング
  - 900,000 polygons/sec：スペキュラー、130-texelのポリゴン
  - 600,000 polygons/sec：スペキュラー、200-texelのポリゴン
  - 300,000 polygons/sec：グーローシェーディング（ソフトウェア）、32-texelのポリゴン[[n 34]](#note-34)
- メモリ：最大150.21 MB（メイン35.125 MB、ビデオ99,332 KB、オーディオ16,960 KB、その他18 KB）
- システムRAM：18,388 KB（17.957031 MB）[[8]](#ref-8)
  - メインRAM：1152 KB（1.125 MB）
  - VRAM：14,596 KB（フレームバッファVRAM 1.5 MB、コプロセッサバッファSRAM/SDRAM 8228 KB、テクスチャSRAM/SDRAM 4 MB、輝度64 KB、ジオメトリ32 KB、タイル576 KB、色64 KB）
  - オーディオRAM：576 KB
  - その他のRAM：2064 KB（2.015625 MB）
- プロセッサ内部キャッシュ：512.75 KB
  - CPUキャッシュ：768 bytes
  - DSP内部RAMキャッシュ：512 KB SRAM（DSPあたり256 KB）[[38]](#ref-38)
- ゲームROM：最大132.25 MB（メイン34 MB、ビデオ82.25 MB、オーディオ16 MB）
- システムRAM帯域幅：1.1 GB/s
  - メインRAM帯域幅：112 MB/s
  - VRAM帯域幅：979.34066 MB/s
    - SHARC：480 MB/s（2x 240 MB/s）[[39]](#ref-39)
    - ビデオ基板：499.34066 MB/s
  - オーディオRAM帯域幅：20 MB/s

### Model 2C-CRX

1996年に登場したModel 2C-CRXでは、GPUチップセットが強化され、MPEGサウンド基板がオプションで用意された。

- GPUジオメトリコプロセッサ：2x Fujitsu TGPx4 MB86235 @ 40 MHz[[15]](#ref-15)[[40]](#ref-40)
  - コプロセッサの機能：ジオメトリエンジンDSP、浮動小数点演算機能、軸回転演算機能、3D行列演算機能、ALU、DMA、T&L
  - バス幅：192‑bit（各96‑bit；64‑bit SDRAM、32‑bit SRAM）
- GPU描画プロセッサ：2x Fujitsu MB86271 AGP（Advanced Graphics Processor）@ 60 MHz[[41]](#ref-41)
  - 機能：ハードウェアレンダリング、DMA
  - 固定小数点演算：32/64‑bit命令、240 MIPS（各120 MIPS）
- GPU Zソーター：2x Fujitsu MB86272[[41]](#ref-41)
  - 機能：Zソート、クリッピング
- グラフィックスハードウェアの機能：グーローシェーディング、隠面処理、Zバッファリング、ポイントサンプリング、バイリニアフィルタリング、トライリニアフィルタリング[[42]](#ref-42)
- レンダリングのフィルレート：200 MPixels/s（16bpp）、400 MPixels/s（8bpp）、430 MPixels/s（4bpp）
  - ポリゴン：188 MPixels/s（16bpp）、[[n 35]](#note-35) 376 MPixels/s（8bpp）
  - タイルマップ：15 MPixels/s（16bpp）、30 MPixels/s（8bpp）、61 MPixels/s（4bpp）
- テクスチャマッピング性能：188 MTexels/s、ライティング、スペキュラー、[[15]](#ref-15) アルファブレンディング[[40]](#ref-40)
  - 900,000 polygons/sec：150-texelのポリゴン[[n 36]](#note-36)
  - 600,000 polygons/sec：Zソート、[[n 37]](#note-37) 400-texelのポリゴン
  - 520,000 polygons/sec：グーローシェーディング、[[n 38]](#note-38) 150-texelのポリゴン[[n 39]](#note-39)
  - 360,000 polygons/sec：グーローシェーディング、Zソート、[[n 40]](#note-40) 300-texelのポリゴン
- オプションのMPEGサウンド基板：DSB1
  - サウンドCPU：Zilog Z80（8/16‑bit命令）
  - サウンドチップ：NEC µD65654GF102
- オプションのMPEGサウンド基板：DSB2
  - サウンドCPU：Motorola 68000（16/32‑bit命令）
  - サウンドチップ：NEC µD65654GF102


## ゲーム一覧

作品名と年は原文の表記を保持しています。同一作品が複数の基板欄に掲載される場合も原文どおりです。


### Model 2

- Daytona USA (1993)
- Daytona USA Deluxe '93 (1993)
- Desert Tank (1994)
- Virtua Cop (1994)

### Model 2A-CRX

- Virtua Fighter 2 (1994)
- Manx TT Superbike (1995)
- Sega Rally Championship (1995)
- Sky Target (1995)
- Virtua Cop 2 (1995)
- Dead or Alive (1996)
- Dynamite Cop (1996)
- Virtua Fighter 2.1 (1996)
- Motor Raid (1997)
- Zero Gunner (1997)
- Hanguk Pro Yagu 98 (1998)
- Pilot Kids (1999)
- Air Walkers （未発売）

### Model 2B-CRX

- Fighting Vipers (1995)
- Gunblade NY (1995)
- Indy 500 (1995)
- Rail Chase 2 (1995)
- Virtua Striker (1995)
- Dead or Alive (1996)
- Dynamite Baseball (1996)
- Dynamite Cop (1996)
- Last Bronx (1996)
- Pilot Kids (1999)
- Sonic the Fighters (1996)
- Super GT 24H (1996)
- Cyber Troopers Virtual-On (1996)
- Dynamite Baseball 97 (1997)
- Zero Gunner (1997)

### Model 2C-CRX

- Dynamite Cop (1996)
- Over Rev (1997)
- Power Sled (1996)
- Sega Ski Super G (1996)
- Sega Touring Car Championship (1996)
- Sega Water Ski (1996)
- Wave Runner (1996)
- The House of the Dead (1997)
- Top Skater (1997)
- Behind Enemy Lines (1998)

### その他

- Ultimate Domain （未発売） — Atlusが開発。Mean Machines Sega第51号で紹介された。


## 歴史

Model 2の開発は、著名なゲームデザイナーである鈴木裕とセガAM2のチームが主導し[[46]](#ref-46)、セガ、富士通、GE Aerospaceの共同プロジェクトとして進められた。GE Aerospaceは1993年にMartin Mariettaに買収され、現在はLockheed Martinの一部となっている。セガはポリゴンのジオメトリエンジンを社内開発した。[[16]](#ref-16) 富士通のDSPコプロセッサにセガ独自のマイクロコードを組み込み、ハードウェアT&L機能を実現したものである。[[19]](#ref-19) 家庭向けシステムにハードウェアT&Lが登場するのは、その何年も後のことだった。これにGE Aerospaceの高価なテクスチャマッピング技術[[16]](#ref-16)を組み合わせ、鈴木のチームはより低価格なチップセットへとまとめ上げた。

鈴木の説明によれば、Model 2のテクスチャマッピング用チップは、旧General Electric Aerial & Spaceの技術を受け継いだLockheed Martinの軍用機器に由来する。総額3,200万米ドルのフライトシミュレーション装置の一部で、チップだけを買う場合でも200万米ドルと提示されたという。それをビデオゲーム用に作り変え、1台あたり5,000円（50米ドル）で利用できる技術にする必要があった。困難だったものの5,000円で実現できたが、この技術をゲーム用に購入したいと話した際、セガでは誰も信じてくれなかったとも述べている。[[46]](#ref-46) 結果として成功し、業界に量産可能なテクスチャマッピング技術をもたらしたという。またVirtua Fighter 2ではモーションキャプチャ技術も活用し、ゲーム業界に導入した。[[47]](#ref-47)

新しいCPUを扱ううえでの問題もあった。[[46]](#ref-46) 使用したIntel i960-KBは、原文によれば1993年に登場したばかりだった。[[11]](#ref-11) 鈴木は、新しいCPUにはまだデバッガがなく、最新ハードウェア自体にも多くのバグがあると説明している。デバッガが存在してもそのデバッガにもバグがあり、デバッガそのものをデバッグしなければならなかった。さらに、新しいハードウェアにはライブラリもシステムもないため、それらもすべて作る必要があり、過酷な循環だったという。[[46]](#ref-46)

1998年末のインタビューで、元GE Aerospace（後のLockheed Martin）社員であるRead3DのJon Lenyoは、セガによるModel 2の開発は、早くも1990年11月までさかのぼれると述べた。この時、彼とGE Aerospaceの社員たちがセガを訪問し、自社技術のトライリニア・テクスチャフィルタリングとシェーディング機能を実演した。セガはすでに社内でSega Model 1の開発を進めていたため、最終的にGE Aerospaceの技術はModel 2に組み込まれた。[[2]](#ref-2)

このアーケード基板はDaytona USAとともに登場した。同作は1993年に完成して著作権表示が付され、1993年のアミューズメントマシンショーで初披露された。[[48]](#ref-48)

約15,000米ドル（2014年の価値で25,000米ドル相当）という高価格にもかかわらず、Model 2プラットフォームは大きな成功を収めた。Daytona USA、Virtua Fighter 2、Cyber Troopers Virtual-On、The House of the Dead、Dead or Aliveなど、歴代でも特に高い売上を記録したアーケードゲームが登場した。セガは初年度に33,000台以上のModel 2を販売し[[49]](#ref-49)、その後は年間65,000台を販売した。[[2]](#ref-2) 1996年までの累計販売台数は130,000台を超え、ハードウェア筐体の販売による売上は20億米ドルに達した。[[n 41]](#note-41) インフレ調整後では30億米ドル以上に相当し、歴代でも特に多く売れたアーケードシステムの一つとなった。

Model 2は1996年にSega Model 3へと引き継がれた。Model 3の後継にはSega NAOMI、Sega Hikaru、Sega NAOMI 2が続いた。

## 制作クレジット

- Hiroshi Yagi [[52]](#ref-52)
- 3Dプレビュー用ソフトウェア：Kenneth Ibrahim [[53]](#ref-53)
- 情報源：開発者による言及

## 雑誌記事

詳細は原サイトの[Sega Model 2／Magazine articles](https://segaretro.org/Sega_Model_2/Magazine_articles)を参照。

## 写真ギャラリー

写真自体は転載していません。[原文の写真ギャラリー](https://segaretro.org/index.php?title=Sega_Model_2&oldid=1149915#Photo_gallery)には、次の写真が掲載されています。

- CPU
- ビデオ基板
- 一般的なROM基板（Virtua Cop）
- Model 2A CPU
- Model 2Aビデオ基板
- Model 2A ROM基板（Dead or Alive）
- Model 2B CPU／ビデオ基板
- Model 2Bフィルター基板
- Model 2B通信基板
- Model 2B ROM基板
- Model 2C基板
- 日本のセガによるModel 2B CRXの公式写真



## 注釈

<a id="note-1"></a>

[n 1] サイクルあたり5命令[[20]](#ref-20)。

<a id="note-2"></a>

[n 2] サイクルあたり1回の[MAC（積和）演算](https://en.wikipedia.org/wiki/Multiply%E2%80%93accumulate_operation)（乗算と加算）[[20]](#ref-20)。

<a id="note-3"></a>

[n 3] サイクルあたり1演算（MAC演算あたり2サイクル）[[20]](#ref-20)。

<a id="note-4"></a>

[n 4] TGP：96 MFLOPS、192 MIPS[[18]](#ref-18)。<br>i960：13.6 MFLOPS、25 MIPS[[11]](#ref-11)。

<a id="note-5"></a>

[n 5] TGP：加算48百万回/秒（浮動小数点）、加算96百万回/秒（固定小数点）[[26]](#ref-26)。<br>i960：加算13.6百万回/秒（浮動小数点）、加算25百万回/秒（固定小数点）。

<a id="note-6"></a>

[n 6] TGP：乗算48百万回/秒（浮動小数点）、乗算96百万回/秒（固定小数点）[[26]](#ref-26)。<br>i960：乗算13.6百万回/秒（浮動小数点）、乗算25百万回/秒（固定小数点）。

<a id="note-7"></a>

[n 7] Zソートおよびクリッピング用チップセット、32 MHz。

<a id="note-8"></a>

[n 8] TGP：5,333,333頂点/秒、頂点あたり18サイクル（9回のMAC演算）[[15]](#ref-15)。<br>i960：755,555頂点/秒、頂点あたり18回の浮動小数点演算（9回のMAC演算）。

<a id="note-9"></a>

[n 9] 三角形ポリゴンあたり3頂点。

<a id="note-10"></a>

[n 10] TGP：1,043,478ポリゴン/秒、ポリゴンあたり92サイクル（46回のMAC演算）[[15]](#ref-15)。<br>i960：147,826ポリゴン/秒、ポリゴンあたり92回の浮動小数点演算（46回のMAC演算）。

<a id="note-11"></a>

[n 11] ポリゴンあたり46サイクル（46回のMAC演算）[[15]](#ref-15)。

<a id="note-12"></a>

[n 12] ポリゴンあたり102サイクル（51回のMAC演算）[[15]](#ref-15)。

<a id="note-13"></a>

[n 13] TGP：774,193ポリゴン/秒、ポリゴンあたり124サイクル（62回のMAC演算）[[15]](#ref-15)[[27]](#ref-27)。<br>i960：109,677ポリゴン/秒、ポリゴンあたり124回の浮動小数点演算（62回のMAC演算）。

<a id="note-14"></a>

[n 14] ポリゴンあたり62サイクル（62回のMAC演算）[[15]](#ref-15)[[27]](#ref-27)。

<a id="note-15"></a>

[n 15] ポリゴン描画帯域幅400 MB/s（2×32ビット、50 MHz）。

<a id="note-16"></a>

[n 16] タイルマップ生成器の帯域幅30.769232 MB/s（2×16ビット、7.692308 MHz）。

<a id="note-17"></a>

[n 17] ポリゴンあたり163サイクル（ジオメトリ処理124サイクル、ラスタ演算39回）。走査線4本のポリゴンあたり175サイクル（ポリゴンごとに走査線あたり3演算）[[28]](#ref-28)[[29]](#ref-29)。32ピクセルのポリゴンあたり271サイクル（ピクセルあたり3サイクル）。

<a id="note-18"></a>

[n 18] 2×8ビット、8/4 MHz。

<a id="note-19"></a>

[n 19] 6×32ビット、16 MHz[[31]](#ref-31)。

<a id="note-20"></a>

[n 20] 2×16ビット、7.692308 MHz[[32]](#ref-32)。

<a id="note-21"></a>

[n 21] 16ビット、14.285714 MHz[[33]](#ref-33)。

<a id="note-22"></a>

[n 22] 2×32ビット、50 MHz。

<a id="note-23"></a>

[n 23] 8ビット、40 MHz[[34]](#ref-34)。

<a id="note-24"></a>

[n 24] 16ビット、10 MHz。

<a id="note-25"></a>

[n 25] 32ビット、25 MHz。

<a id="note-26"></a>

[n 26] 6×32ビット、16 MHz。

<a id="note-27"></a>

[n 27] 5×32ビット。

<a id="note-28"></a>

[n 28] 32ビット、33–50 MHz、20–30 ns[[35]](#ref-35)[[36]](#ref-36)。

<a id="note-29"></a>

[n 29] 4×32ビット、50 MHz。

<a id="note-30"></a>

[n 30] ポリゴンあたり46回のMAC演算[[15]](#ref-15)：1,739,130ポリゴン/秒（SHARC）、147,826ポリゴン/秒（i960）。

<a id="note-31"></a>

[n 31] ポリゴンあたり51回のMAC演算[[15]](#ref-15)。

<a id="note-32"></a>

[n 32] ポリゴンあたり62回のMAC演算[[15]](#ref-15)[[27]](#ref-27)：1,290,322ポリゴン/秒（SHARC）、109,677ポリゴン/秒（i960）。

<a id="note-33"></a>

[n 33] フレームあたり2メガピクセル。

<a id="note-34"></a>

[n 34] ポリゴンあたり101サイクル（ジオメトリ処理62サイクル、ラスタ演算39回）。走査線4本のポリゴンあたり113サイクル（ポリゴンごとに走査線あたり3演算）[[28]](#ref-28)[[29]](#ref-29)。32ピクセルのポリゴンあたり209サイクル（ピクセルあたり3サイクル）。

<a id="note-35"></a>

[n 35] GPUあたり94メガピクセル/秒[[43]](#ref-43)。

<a id="note-36"></a>

[n 36] ポリゴンあたり88サイクル[[44]](#ref-44)、ポリゴンあたり266命令（固定小数点）、GPUあたり450,000ポリゴン/秒（150ピクセルのポリゴン）[[45]](#ref-45)。

<a id="note-37"></a>

[n 37] ポリゴンあたり272回の浮動小数点演算。

<a id="note-38"></a>

[n 38] ポリゴンあたり151サイクル[[44]](#ref-44)。

<a id="note-39"></a>

[n 39] GPUあたり250,000ポリゴン/秒（150ピクセルのポリゴン）[[45]](#ref-45)。

<a id="note-40"></a>

[n 40] ポリゴンあたり438回の浮動小数点演算。

<a id="note-41"></a>

[n 41] 130,000台[[50]](#ref-50)、1台あたり$15,000[[2]](#ref-2)[[51]](#ref-51)。

## 参考文献

<a id="ref-1"></a>

[1] [Mean Machines Sega](https://segaretro.org/Mean_Machines_Sega), ["August 1994" (UK; 1994-06-30), 93ページ](https://segaretro.org/index.php?title=File:MeanMachinesSega22UK.pdf&page=93)

<a id="ref-2"></a>

[2] [Second Hand Smoke: One up, two down (October 22, 1999)](http://www.thg.ru/smoke/19991022/print.html)

<a id="ref-3"></a>

[3] [Edge](https://segaretro.org/Edge), ["June 1994" (UK; 1994-04-28), 49ページ](https://segaretro.org/index.php?title=File:Edge_UK_009.pdf&page=49)

<a id="ref-4"></a>

[4] [IGN PRESENTS THE HISTORY OF SEGA (8ページ)](http://ign.com/articles/2009/04/21/ign-presents-the-history-of-sega?page=8)

<a id="ref-5"></a>

[5] [Saturn maybe not so stellar (Game Zero Magazine)](http://www.gamezero.com/team-0/whats_new/past/news9504.html)

<a id="ref-6"></a>

[6] [File:DaytonaUSA Model2 Flyer.pdf, 2ページ](https://segaretro.org/index.php?title=File:DaytonaUSA_Model2_Flyer.pdf&page=2)

<a id="ref-7"></a>

[7] [File:SSM_UK_02.pdf, 21ページ](https://segaretro.org/index.php?title=File:SSM_UK_02.pdf&page=21)

<a id="ref-8"></a>

[8] [Sega Model 2 (MAME)](https://github.com/mamedev/mame/blob/master/src/mame/drivers/model2.cpp)

<a id="ref-9"></a>

[9] [Sega PCB](http://www.tvspels-nostalgi.com/pcb_sega.htm)

<a id="ref-10"></a>

[10] [File:I960 datasheet.pdf](https://segaretro.org/File:I960_datasheet.pdf)

<a id="ref-11"></a>

[11] [File:80960KB datasheet.pdf](https://segaretro.org/File:80960KB_datasheet.pdf)

<a id="ref-12"></a>

[12] [File:I960 datasheet.pdf, 2ページ](https://segaretro.org/index.php?title=File:I960_datasheet.pdf&page=2)

<a id="ref-13"></a>

[13] [http://pdf.datasheetarchive.com/indexerfiles/Scans-068/DSA2IH00225160.pdf](http://pdf.datasheetarchive.com/indexerfiles/Scans-068/DSA2IH00225160.pdf)

<a id="ref-14"></a>

[14] [File:ST-077-R2-052594.pdf](https://segaretro.org/File:ST-077-R2-052594.pdf)

<a id="ref-15"></a>

[15] [Sega Model 2 Geometry Engine and 3D Rasterizer (MAME)](https://github.com/mamedev/mame/blob/master/src/mame/video/model2.cpp)

<a id="ref-16"></a>

[16] [Next Generation](https://segaretro.org/Next_Generation), ["November 1995" (US; 1995-10-24), 16ページ](https://segaretro.org/index.php?title=File:NextGeneration_US_11.pdf&page=16)

<a id="ref-17"></a>

[17] [Sega Model 2 ROM Dump](http://members.iinet.net.au/~lantra9jp1_nbn/gurudumps/m2status/index.html)

<a id="ref-18"></a>

[18] [File:MB86232 datasheet.pdf](https://segaretro.org/File:MB86232_datasheet.pdf)

<a id="ref-19"></a>

[19] [TGP (MAME)](http://wiki.mamedev.org/index.php/TGP:Index)

<a id="ref-20"></a>

[20] [File:MB86232 datasheet.pdf, 32ページ](https://segaretro.org/index.php?title=File:MB86232_datasheet.pdf&page=32)

<a id="ref-21"></a>

[21] [Sega Model 2 Video Board](http://hico-srv004.pixhotel.fr/sites/default/files/gamoovernet/20110520120039-lapin252-IMG-0112.JPG)

<a id="ref-22"></a>

[22] [Sega 16‑Bit Common Hardware](https://github.com/bji/libmame/blob/master/old/src/mame/video/segaic16.c), [MAME](https://segaretro.org/MAME)

<a id="ref-23"></a>

[23] [Sega System 24 Hardware Notes (2013-06-16)](https://segaretro.org/Sega_System_24_Hardware_Notes_(2013-06-16))

<a id="ref-24"></a>

[24] [Electronic Gaming Monthly](https://segaretro.org/Electronic_Gaming_Monthly), ["June 1994" (US; 1994-xx-xx), 68ページ](https://segaretro.org/index.php?title=File:EGM_US_059.pdf&page=68)

<a id="ref-25"></a>

[25] [File:VirtuaFighter2 Model2 Flyer.pdf, 2ページ](https://segaretro.org/index.php?title=File:VirtuaFighter2_Model2_Flyer.pdf&page=2)

<a id="ref-26"></a>

[26] [File:MB86232 datasheet.pdf, 33ページ](https://segaretro.org/index.php?title=File:MB86232_datasheet.pdf&page=33)

<a id="ref-27"></a>

[27] [Design of Digital Systems and Devices (95-97ページ)](https://books.google.co.uk/books?id=iAvHt5RCHbMC&pg=PA95)

<a id="ref-28"></a>

[28] [Transformation Of Rendering Algorithms For Hardware Implementation (53ページ)](http://sirkan.iit.bme.hu/~szirmay/abbas.pdf#page=53)

<a id="ref-29"></a>

[29] [File:32XUSHardwareManual.pdf, 76ページ](https://segaretro.org/index.php?title=File:32XUSHardwareManual.pdf&page=76)

<a id="ref-30"></a>

[30] [File:80960KB datasheet.pdf, 7ページ](https://segaretro.org/index.php?title=File:80960KB_datasheet.pdf&page=7)

<a id="ref-31"></a>

[31] [File:TC5588P datasheet.pdf](https://segaretro.org/File:TC5588P_datasheet.pdf)

<a id="ref-32"></a>

[32] [File:TC518128CPL datasheet.pdf](https://segaretro.org/File:TC518128CPL_datasheet.pdf)

<a id="ref-33"></a>

[33] [File:MB84256A datasheet.pdf](https://segaretro.org/File:MB84256A_datasheet.pdf)

<a id="ref-34"></a>

[34] [http://pdf.datasheetarchive.com/datasheetsmain/Datasheets-39/DSA-764435.pdf](http://pdf.datasheetarchive.com/datasheetsmain/Datasheets-39/DSA-764435.pdf)

<a id="ref-35"></a>

[35] [File:AM27C1024 datasheet.pdf](https://segaretro.org/File:AM27C1024_datasheet.pdf)

<a id="ref-36"></a>

[36] [File:MX27C1024 datasheet.pdf](https://segaretro.org/File:MX27C1024_datasheet.pdf)

<a id="ref-37"></a>

[37] [Dynamite Cop (MAME)](http://mamedb.blu-ferret.co.uk/game/dynamcop)

<a id="ref-38"></a>

[38] [File:ADSP-2106 datasheet.pdf](https://segaretro.org/File:ADSP-2106_datasheet.pdf)

<a id="ref-39"></a>

[39] [File:ADSP-2106 datasheet.pdf, 4ページ](https://segaretro.org/index.php?title=File:ADSP-2106_datasheet.pdf&page=4)

<a id="ref-40"></a>

[40] [File:3DGraphicsProcessorChipSet.pdf](https://segaretro.org/File:3DGraphicsProcessorChipSet.pdf)

<a id="ref-41"></a>

[41] [File:3DGraphicsProcessorChipSet.pdf, 4ページ](https://segaretro.org/index.php?title=File:3DGraphicsProcessorChipSet.pdf&page=4)

<a id="ref-42"></a>

[42] [File:3D-CG System with Video Texturing.pdf](https://segaretro.org/File:3D-CG_System_with_Video_Texturing.pdf)

<a id="ref-43"></a>

[43] [File:3DGraphicsProcessorChipSet.pdf, 12ページ](https://segaretro.org/index.php?title=File:3DGraphicsProcessorChipSet.pdf&page=12)

<a id="ref-44"></a>

[44] [File:3DGraphicsProcessorChipSet.pdf, 8ページ](https://segaretro.org/index.php?title=File:3DGraphicsProcessorChipSet.pdf&page=8)

<a id="ref-45"></a>

[45] [File:3DGraphicsProcessorChipSet.pdf, 11ページ](https://segaretro.org/index.php?title=File:3DGraphicsProcessorChipSet.pdf&page=11)

<a id="ref-46"></a>

[46] [http://www.1up.com/features/disappearance-suzuki-part-1](http://archive.is/35o4a) (archive.today)

<a id="ref-47"></a>

[47] [Yu Suzuki recalls using military tech to make Virtua Fighter 2](http://www.gamasutra.com/view/news/228512/Yu_Suzuki_recalls_using_military_tech_to_make_Virtua_Fighter_2.php)

<a id="ref-48"></a>

[48] [Electronic Gaming Monthly](https://segaretro.org/Electronic_Gaming_Monthly), ["October 1993" (US; 1993-xx-xx), 222ページ](https://segaretro.org/index.php?title=File:EGM_US_051.pdf&page=222)

<a id="ref-49"></a>

[49] [Press release: 1995-03-20: Lockheed Martin 3D Graphics Accelerator offers real-time PC visual system performance](https://segaretro.org/Press_release:_1995-03-20:_Lockheed_Martin_3D_Graphics_Accelerator_offers_real-time_PC_visual_system_performance)

<a id="ref-50"></a>

[50] [http://www.real3d.com/sega.html](http://web.archive.org/web/19971210083243/http://www.real3d.com/sega.html) (Wayback Machine: 1997-12-10 08:32)

<a id="ref-51"></a>

[51] [http://assemblergames.com/forums/showthread.php?47028-Early-concept-of-Daytona-USA-at-Summer-CES-1993-Not-on-Model-2-but-Compu-Scene](https://web.archive.org/web/20141104190719/http://assemblergames.com/forums/showthread.php?47028-Early-concept-of-Daytona-USA-at-Summer-CES-1993-Not-on-Model-2-but-Compu-Scene) (Wayback Machine: 2014-11-04 19:07)

<a id="ref-52"></a>

[52] [https://www.4gamer.net/games/999/G999905/20210126043/](https://web.archive.org/web/20210205150032/https://www.4gamer.net/games/999/G999905/20210126043/) (Wayback Machine: 2021-02-05 15:00)

<a id="ref-53"></a>

[53] [https://www.youtube.com/watch?v=1CEdmZ5P0jA](https://www.youtube.com/watch?v=1CEdmZ5P0jA)
