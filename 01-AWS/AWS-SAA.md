





 # 1 分野
- コンピューティング 
- コスト管理 
- データベース 
- 災害対策 
- 高可用性 
- マネジメントとガバナンス 
- マイクロサービスとコンポーネントのデカップリング 

- 5.2 移行とデータの転送 

- ネットワーキング、接続、コンテンツ配信 
- セキュリティ 
- サーバーレスの設計原則 
- ストレージ

# 2 AWS のサービスと機能 
## 2.1 アナリティクス: 
- Amazon Athena 
- Amazon Elasticsearch Service (Amazon ES) 
- Amazon EMR 
- AWS Glue 
- Amazon Kinesis 
- Amazon QuickSight 
## 2.2 AWS の請求情報とコスト管理: 
- AWS Budgets 
- Cost Explorer 

## 2.3 アプリケーション統合: 

- Amazon Simple Notification Service (Amazon SNS) 
- Amazon Simple Queue Service (Amazon SQS) 

## 2.4 コンピューティング: 
- Amazon EC2 

- AWS Elastic Beanstalk 

- Amazon Elastic Container Service (Amazon ECS) 

- Amazon Elastic Kubernetes Service (Amazon EKS) 

- Elastic Load Balancing 

  ELBと=ALB(Application)+CLB(Classic)+NLB(Network)

- AWS Fargate 

- AWS Lambda
## 2.5 データベース: 
- Amazon Aurora 
- Amazon DynamoDB 
- Amazon ElastiCache 
- Amazon RDS 
- Amazon Redshift 
## 2.6 マネジメント、ガバナンス: 
- AWS Auto Scaling 

- AWS Backup 

- AWS CloudFormation 

  AWSリソースをコードで管理できるサービス

- AWS CloudTrail 

- Amazon CloudWatch 

- AWS Config 

- Amazon EventBridge (Amazon CloudWatch Events) 

- AWS Organizations 

- AWS Resource Access Manager 

- AWS Systems Manager 

- AWS Trusted Advisor 

## 2.7 移行、転送: 
- AWS Database Migration Service (AWS DMS) 
- AWS DataSync 
- AWS Migration Hub 
- AWS Server Migration Service (SMS) 
- AWS Snowball 
- AWS Transfer Family 

## 2.8 ネットワーク、コンテンツ配信: 
- Amazon API Gateway 

  AWS Lambda、EC2、もしくはAWS外でパブリックとして公開されているアプリケーションをAPIとして公開する

- Amazon CloudFront 

  AWSが提供するCDN（Content Delivery Network）サービス   `Lambda@Edge`

- AWS Direct Connect 

  お客様の施設から AWS リージョンへのネットワーク接続を確立

  ![](.\images\AWSDirectConnect.png)

- AWS Global Accelerator 

  ALB、NLB、EC2の前段に置いてアプリケーションの可用性とパフォーマンスを改善するサービス

  ![](.\images\global-accelerator-before.png)

  ![](.\images\global-accelerator-after.png)

- Amazon Route 53 

  フルマネージド型のDNSサービス

- AWS Transit Gateway 

- Amazon VPC (および関連機能) 



- 比較

  ![](.\images\vgw-dgw-tgw.png)

   Transit Gateway       Direct Connect Gateway(DXGW)      Virtual Gateway   



## 2.9 セキュリティ、アイデンティティ、コンプライアンス: 
- AWS Certificate Manager (ACM) 

  ACMはSSL/TLSサーバー証明書を無料で発行できるサービス

- AWS Directory Service 

- Amazon GuardDuty 

- AWS Identity and Access Management (IAM) 

- Amazon Inspector 

- AWS Key Management Service (AWS KMS) 

- Amazon Macie 

- AWS Secrets Manager 

- AWS Shield 

- AWS Single Sign-On 

- AWS WAF 

## 2.10 ストレージ:  2021/12/05



プロビジョンド IOPS SSD (io2 Block Express、io2、および io1)、汎用 SSD (gp3 および gp2)、スループット最適化 HDD (st1)、 Cold HDD (sc1)



- Amazon Elastic Block Store (Amazon EBS) 　　　　HD

  - https://aws.amazon.com/jp/ebs/features/#Amazon_EBS-Optimized_instances

  - https://aws.amazon.com/cn/ebs/faqs/

  - https://aws.amazon.com/jp/ebs/faqs/?nc1=h_ls

    | 名称                         | 特徴 |                                                      |
    | ---------------------------- | ---- | ---------------------------------------------------- |
    | IOPS SSD(io2 Block Express)  |      | R5b インスタンスのみで使用可能                       |
    | IOPS SSD(io2)                |      | R5b. を除くすべての EC2 インスタンスタイプで使用     |
    | IOPS SSD(io1)                |      |                                                      |
    | 汎用 SSD (gp2)               |      |                                                      |
    | 汎用 SSD (gp3)               |      |                                                      |
    | スループット最適化 HDD (st1) |      | アクセス頻度が高いスループット集約型ワークロード向け |
    | Cold HDD (sc1)               |      | アクセス頻度の低いワークロード向け                   |

    

- Amazon Elastic File System (Amazon EFS) 　　　linux向けの共通ファイルサーバ　　

- Amazon FSx 　　　　　Windows・linux向けの共通ファイルサーバ

- Amazon S3 

  - https://aws.amazon.com/cn/s3/storage-classes/

    |                                                          |                                                              |      |
    | -------------------------------------------------------- | ------------------------------------------------------------ | ---- |
    | Amazon S3 標準 (S3 標準)                                 | 頻繁にアクセスされるデータ向け                               |      |
    | Amazon S3 Intelligent-Tiering (S3 Intelligent-Tiering)   | 存続期間が長くあまり頻繁にアクセスされないデータ向け         |      |
    | Amazon S3 標準 – 低頻度アクセス (S3 標準 – IA)           | アクセスパターンが変化、または不明な存続期間が長いデータ向け |      |
    | Amazon S3 1 ゾーン – 低頻度アクセス (S3 1 ゾーン – IA)   | 存続期間が長くあまり頻繁にアクセスされない、且つ重要度の低いデータ向け |      |
    |                                                          |                                                              |      |
    | Amazon S3 Glacier (S3 Glacier)                           | 取得時間が数分から数時間許容される長期アーカイブデータ向け   |      |
    | Amazon S3 Glacier Deep Archive (S3 Glacier Deep Archive) | 取得時間が12時間許容される長期アーカイブデータ向け           |      |

    

- Amazon S3 Glacier 

- AWS Storage Gateway



Amazon EBS – Designed to support block storage volumes with Amazon EC2 instances

Amazon S3 – Designed to support millions of storage objects and accessed using REST APIs

Amazon EFS – Designed as a native Multi-AZ file system for NFS file shares

Amazon FSx for Lustre – Designed for distributed high performance computing workloads

Amazon FSx for Windows File Server – Designed to support SMB file shares in a Single-AZ or Multi-AZ configuration







# 3 単語集

- IOPS    Input/Output Per Second
- SAN     Storage Area Network





# 4 リソース

blog推荐

http://jayendrapatil.com/   （多人强烈推荐）

 

免费

www.briefmenow.org/amazon

https://awsjp.com/

https://www.lleicloud.com/index.php/aws-certified-solutions-architect-practice-tests/  （官方指导测试题2019版 1000+道）
