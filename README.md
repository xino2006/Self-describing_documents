# Self-describing_documents

Markdownなどのプレーンテキストから生成される文書内部にソースコードを埋め込む。

source --(compress)--> X --(base64)--> Z

source + Z --(Pandoc)--> PDF/docx(Self-describing_documents)

これにより、ソースとその結果（PDF、docx）が分かれるものを再利用、修正する際に便利である。

※　今回はPandocで極小文字で埋め込むことができなかったため、手動で埋め込みPDFに変換している。

sample.mdをgzipで圧縮、base64で変換したものが、sample.base。

sample.mdをpandocでdocxに変換してsample.baseを埋め込み、PDFにに変換したものが、sample.pdf。
