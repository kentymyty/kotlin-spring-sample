# kotlin-spring-sample

## KotlinのSpring Boot実装

1. [Spring Initializer](https://start.spring.io/)でベースプロジェクトを作成できる
2. @SpringBootApplicationがエントリーポイント
   1. コマンドで実行する
   ```
    ./gradlew bootRun
   ```
3. @Controller
   1. 「resources/templates/」下のHTMLファイルをreturn
   2. Thymeleafのテンプレートエンジンで埋め込みが
4. @RestController
   1. Responseのクラスを定義をしておき、戻り値の型とすることでJSON応答
5. @RequestMapping
   1. classのパスとして指定できる
   2. class単位でパスを分けたいときに使用
6. @GetMapping, @PostMapping, etc...
   1. "/path1/path2"として指定することでエンドポイントを作成できる
   2. @PathVariableでパスパラメータを取得
   3. @RequestParamでGET,POSTなどのパラメータを取得
   4. @RequestBodyでPOSTのJSONリクエストパラメータを取得
   4. 正規表現での指定も可能
      1. メソッドパスパラメータによってメソッドを分けたいときなど
7. DI
   1. コンストラクタインジェクションが基本（Swiftと同じ）
   2. フィールドインジェクション（@Autowired）でプロパティに宣言することでもOK
      循環依存に注意
   3. interfaceの実装クラスに@Componentをつけることでインジェクションされる
   4. 複数実装クラス(@Component)がある場合は@Qualifierで実装するComponentを指定する、
