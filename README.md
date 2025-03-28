# Self-describing_documents

Markdownなどのプレーンテキストから生成される文書内部にソースコードを埋め込む。

source --(compress)--> X --(base64)--> Z
source + Z --(Pandoc)--> Word(Self-describing_documents)

