# Practical work

実務で行ってきた実績と経験をまとめています。

# 実務と経験

## DICOM画像を対象とした医用画像自動解析システムの開発
* 利用技術
  * 言語：Java SpringBoot, C#(.NET)
  * IDE: Visual Studio Code
  * OS：Linux
  * Infra：Kubernetes, Containerd, PostgreSQL, Keycloak, Apache Kafka
  * CI: Jenkins, Ansible
* 期間：5年
* 主な業務内容：
  * 画像分類機能
    * Dicomメタ情報を活用して、撮影方法や撮影部位に基づく自動分類機能を検討・実装
    * ✅成果：手動での分類処理がゼロになることにより、画像の受信から解析までの全自動化が実現。
  * Kubernetesを用いた解析優先度の制御機能
    * Kubernetes APIを利用した解析アプリケーションの起動の優先度設定機能を検討・実装
    * ✅成果：解析アプリケーションの優先順位をリソースベースに調整し、処理の滞留を回避。
  * OAuth2連携による外部モバイルViewerサーバへの通知機能
    * OAuthを活用し、解析完了時に外部Viewerに連携
    * ✅成果：解析完了通知をすることで、読影ワークフローの迅速化に貢献。
  * Ansibleスクリプトによるサーバ構築の自動化
    * JenkinsとAnsibleを連携させて、テストにおける環境構築を自動化
    * ✅成果：1台当たり、2時間から30分に短縮

## 心疾患解析アプリケーションのアルゴリズム要素開発
* 利用技術
  * 言語：C++
  * IDE：Visual Studio
* 期間：1年
* 主な業務内容：
  * 冠動脈の解析アルゴリズム
    * CT画像を使って心筋梗塞の原因となる冠動脈疾患の解析アルゴリズムを検討・実装
    * ✅成果：共同研究先の技師の方による評価にて約80%の解析精度で検出

## 医用画像処理ワークステーションのデータ管理周りの開発
* 利用技術
  * 言語：Java SpringBoot
  * IDE：Visual Studio Code
  * OS：Linux on WSL
  * Infra：PostgreSQL, RabbitMQ
* 期間：半年
* 主な業務内容：
  * 画像の受信・登録機能
    * Java SpringBootにおいてdcm4cheを利用した画像の受信・登録処理
    * ✅成果：前身となるワークステーションより受信・登録の速度性能の15%程度改善を達成

## 上記の医用画像自動解析システムのAWS SaaS化に向けたPoC検証
* 利用技術
  * Infra：AWS Systems Manager, Cognito, Application Load Balancer, Aurora, Automation Runbook
* 期間：1年
* 主な業務内容：
  * オンプレミス環境へのリモートインストールの検証
    * Systems Managerでオンプレミス環境に接続をして、自動インストールスクリプトを作成。
    * ✅成果：オンプレミス環境におけるサーバ構築作業がの時間を8割程度削減
  * 認証機能の検証。
    * Cognitoを用いて、AWS上にデプロイされるサービスにアクセスする際の認証機能を検証。
    * ✅成果：従来用いていたKeycloakとのOAuth仕様との比較を完了。