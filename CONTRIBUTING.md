## Contributing to the C++ Core Guidelines

>「C++の中には、より小さく、より単純で、より安全な言語が、外に出ようと必死に奮闘している。」
>-- <cite>ビャルネ・ストラウストラップ</cite>

C++コアガイドラインは、C++言語そのものと同様に、ビャルネ・ストロストラップが主導する共同作業の成果である。これらは複数の組織にわたり、多くの
人年を費やした議論と設計の結果として生まれた。その設計は汎用性と広範な採用を促すが、
組織のニーズに合わせて自由に複製・修正することが可能である。

C++コアガイドラインへの貢献を以下の方法で推奨します：
- **個人からのフィードバック** コードに情熱を注ぐ開発者の方へ。
[イシュー](https://github.com/isocpp/CppCoreGuidelines/issues)での議論にご参加ください。どのルールが共感を得られ、どのルールがそうでないかをお聞かせください。適用が
過度に困難なルールはありましたか？コンパイラベンダーのガイドラインサポートライブラリ（例：
[MicrosoftのGSL実装](https://github.com/microsoft/gsl)）は、これらのガイドライン採用においてニーズを満たしていますか？
- **組織での採用** ガイドラインは広く採用可能に設計されていますが、
組織固有のニーズに合わせて修正することも想定されています。組織では、このリポジトリをフォークし、
ご自身のニーズを反映した変更を加えたガイドラインの独自コピーを作成することを推奨します。ガイドラインのタイトルには、これが組織による
ガイドラインのフォークであることを明記し、元の[ガイドライン](https://github.com/isocpp/CppCoreGuidelines)へのリンクを提供することをお勧めします。また、
ローカルでの変更がオリジナルガイドラインへの反映に適している場合は、プルリクエストにつながる可能性のある
[Issue](https://github.com/isocpp/CppCoreGuidelines/issues)を開いてください。
- **ガイドラインの維持** C++ Core Guidelinesは、世界中の数多くの組織に分散する豊富な知識から作成されました
。ガイドライン作成への貢献に情熱をお持ちの方や組織は、編集者またはメンテナとなることをご検討ください。
真剣に参加する意思のあるC++エキスパートの方は、
[email coreguidelines@isocpp.org](mailto:coreguidelines@isocpp.org?subject=Maintain%20the%20C++%20Code%20Guidelines) までご連絡ください。
 
## 貢献者ライセンス契約
C++ Core Guidelinesへのコンテンツ提供（本リポジトリへのプルリクエストの提出）により、あなたは
[Standard C++ Foundation](https://isocpp.org/about)の[利用規約](https://isocpp.org/home/terms-of-use)、特に著作権および特許に関する
すべての条項に同意するものとします。
- 貴殿は、提供した素材がオリジナルであること、または提供権限を有することを保証します。
- 貴殿が所有する素材について、Standard C++ Foundationに対し、提供された素材を商業目的または非商業目的で表示、複製、上演、頒布、および派生作品を作成するための、全世界的、非独占的、取消不能、譲渡可能、かつロイヤリティフリーのライセンスを付与します。
- その他の提供資料については、Standard C++ Foundation
が当該資料を商業的または非商業的利用のために表示、複製、実行、配布、および派生作品を作成することを許容する十分なライセンス下にある必要があります。
- 寄稿した資料がその後いかなる形であれISO/IEC C++標準に反映された場合、当該資料はISO/IEC JTC 
1の全方針（[著作権](http://www.iso.org/iso/home/policies.htm)、
 
[特許](http://www.iso.org/iso/home/standards_development/governance_of_technical_work/patents.htm)、および
[手続き](http://www.itscj.ipsj.or.jp/sc29/29w7proc.htm)を含むすべてのISO/IEC JTC 1ポリシーの対象となることに同意します。これらのポリシーに関するご質問は、
[ISO中央事務局](http://www.iso.org/iso/home/about.htm)までお問い合わせください。


## プルリクエスト

ガイドラインの範囲内での変更（例：バグ修正、例文の修正、曖昧な表現の明確化など）については、プルリクエストを歓迎します。大幅な変更については、まず[イシュー](https://github.com/isocpp/CppCoreGuidelines/issues)
で議論し、プルリクエストにイシュー番号を明記してください。
ガイドライン関連の変更については、Issueおよび/または
プルリクエスト内で該当ルールの番号を明記してください。

変更はマスターブランチの直近コミットの子コミットで行ってください。
多数の小さな変更を行う場合は、マージ時の問題を最小限に抑えるため、個別のプルリクエストを作成してください。

### 文書スタイルガイドライン

このリポジトリの文書は特定形式のMarkdownで記述されており、
テキストの書式設定に若干の曖昧さが残っています。文書全体が
まだ統一されていない可能性があることは承知していますが、プルリクエストでは
以下のスタイルガイドラインを維持してください。

#### インデント

コードとネストされたテキストは、インデントに4スペースの倍数を使用し、
タブ文字は使用しないでください。例：

    void func(const int x)
    {
        std::cout << x << '\n';
    }

#### コードブロック

コード解析をトリガーするには、[フェンス付きコードブロック](https://help.github.com/articles/github-flavored-markdown/#fenced-code-blocks) やその他のスタイルではなく、4スペースのインデントを使用してください。例:

    This is some document text, with an example below:

        void func()
        {
            std::cout << "This is code.\n";
        }

#### ドキュメントスタイルの決定事項

複数のドキュメントスタイルについて議論し決定しました。以下のスタイルに関する点を再検討するプルリクエストは提出しないでください:

- CppCoreGuidelines.mdファイルは単一のGH形式Markdownファイルです。章ごとに分割しません。
- コアガイドラインでは構文ハイライトを使用しません。PR #33、#96、#328、#779を参照してください。構文ハイライトが必要な場合は
http://isocpp.github.io/CppCoreGuidelines/CppCoreGuidelines で「見やすい」バージョンを閲覧するか、各自で後処理を行ってください。
- ASCII文字セットに固執しています。Unicodeのエンダッシュ、Unicodeスペース、装飾引用符は使用しません。多くの人が様々なテキストエディタでこのファイルを編集します。ASCIIはシンプルで普遍的に理解されています。

### 辞書の更新

ガイドライン内のコードサンプルはスペルチェッカーを通します。新しいクラス名や変数名は必ず[scripts/hunspell/isocpp.dic](https://github.com/isocpp/CppCoreGuidelines/blob/master/scripts/hunspell/isocpp.dic)に追加してください。

### その他

改行問題を防ぐため、Git設定で `autocrlf = input` および `whitespace = cr-at-eol` を設定してください。
