# OS自作入門

[社内向けプレゼン資料](https://docs.google.com/presentation/d/e/2PACX-1vSR5xee-Wltcep1plauS3pP0s6HBOU65qB0Xg1A54i7DP2Bm8h8AlygPSC0QE2XnmmXgfLmsr6Vuobg/pub?start=false&loop=false&delayms=3000&slide=id.p)

# ゼロからのOS自作入門

- まずはざっくり試し読みしつつ、前作との差分をメモ
- 64bit, C++で作っている
- UEFIブート。ブートローダーもCで作れる
- PS/2でなくUSBマウス。USBデバイスドライバを作るのがこの本のウリらしい
- プロセスのコンテキストスイッチって、レジスタの保存は自力で全部やるらしい（インラインアセンブラで記述している）
  - 32bitだとTSSに登録していたら自動でやってくれていたが、効率的なコードを自分で書けるようにするためっぽい
- ウィンドウ描画はメインスレッドで、って書いているが、スレッドの概念があるのかな？プロセスのこと？
- ちゃんとELF形式でビルドしてローダーも作っているらしい。
