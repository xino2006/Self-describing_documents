# Self-describing_documents

これは1つの概念です。/　This is one concept.

Markdownなどのプレーンテキストから生成される文書内部にソースコードを埋め込む。/ The document has its source code.


source --(compress)--> X --(base64)--> Z

source + Z --(Pandoc)--> PDF/docx(Self-describing_documents)

これにより、ソースとその結果（PDF、docx）が分かれるものを再利用、修正する際に便利である。/ The document is useful in the future.

※　今回はPandocで極小文字で埋め込むことができなかったため、手動で埋め込みPDFに変換している。

sample.mdをgzipで圧縮、base64で変換したものが、sample.base。/　sample.md is compressed with gzip and converted to base64 to create sample.base.

sample.mdをpandocでdocxに変換してsample.baseを埋め込み、PDFにに変換したものが、sample.pdf。/　Sample.md is converted to docx using pandoc, sample.base is embedded, and then converted to PDF to create sample.pdf.
