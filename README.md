# AWS IAM Tracker

This project collects IAM actions, AWS APIs and managed policies from various public sources.

You can explore the data collected using [the static site](https://glassechidna.github.io/trackiam/).

Collected data is published to the [policies](/policies) and [services](/services) folders in this repo.

Thank you to [alanakirby/aktion](https://github.com/alanakirby/aktion) for originally 
having this idea and being gracious about me shamelessly ripping it off.
	
# Stats

* Unique services: 228
* Unique actions: 8307
* Managed policies: 683

Most common managed policy name prefixes:

| Policy ARN | Count |
| ------ | ----- |
| `arn:aws:iam::aws:policy/AWS*` | 194 |
| `arn:aws:iam::aws:policy/Amazon*` | 184 |
| `arn:aws:iam::aws:policy/aws-service-role/*` | 124 |
| `arn:aws:iam::aws:policy/service-role/*` | 106 |
| `arn:aws:iam::aws:policy/job-function/*` | 7 |
| Other | 68 |

The following table summarises the AWS APIs. 

* The first column is the name of the API as far as IAM policies are concerned. 
* The second column is IAM actions that exactly match the names of invokable 
  APIs exposed by AWS.
* The third column is invokable APIs that don't have a corresponding IAM action.
* The fourth column is IAM actions that don't have a corresponding invokable API.

| Service | Action/API pairs | APIs without actions | Actions without APIs |
| ------ | ----- | ----- | ----- |
| [`ec2`](services/ec2.yml) | 399 | 4 | 0 |
| [`iam`](services/iam.yml) | 140 | 0 | 1 |
| [`sagemaker`](services/sagemaker.yml) | 139 | 0 | 2 |
| [`glue`](services/glue.yml) | 124 | 7 | 1 |
| [`rds`](services/rds.yml) | 123 | 7 | 1 |
| [`ssm`](services/ssm.yml) | 121 | 1 | 7 |
| [`chime`](services/chime.yml) | 115 | 1 | 50 |
| [`mobiletargeting`](services/mobiletargeting.yml) | 107 | 5 | 0 |
| [`ses`](services/ses.yml) | 103 | 9 | 0 |
| [`lightsail`](services/lightsail.yml) | 101 | 12 | 0 |
| [`cognito-idp`](services/cognito-idp.yml) | 100 | 0 | 0 |
| [`greengrass`](services/greengrass.yml) | 90 | 0 | 0 |
| [`redshift`](services/redshift.yml) | 88 | 4 | 18 |
| [`servicecatalog`](services/servicecatalog.yml) | 83 | 0 | 0 |
| [`waf-regional`](services/waf-regional.yml) | 81 | 0 | 0 |
| [`a4b`](services/a4b.yml) | 77 | 16 | 3 |
| [`config`](services/config.yml) | 77 | 2 | 2 |
| [`codecommit`](services/codecommit.yml) | 77 | 0 | 11 |
| [`waf`](services/waf.yml) | 77 | 0 | 0 |
| [`devicefarm`](services/devicefarm.yml) | 77 | 0 | 0 |
| [`gamelift`](services/gamelift.yml) | 76 | 13 | 0 |
| [`opsworks`](services/opsworks.yml) | 73 | 1 | 0 |
| [`storagegateway`](services/storagegateway.yml) | 71 | 7 | 0 |
| [`clouddirectory`](services/clouddirectory.yml) | 62 | 4 | 0 |
| [`ds`](services/ds.yml) | 57 | 0 | 6 |
| [`autoscaling`](services/autoscaling.yml) | 57 | 0 | 0 |
| [`route53`](services/route53.yml) | 56 | 1 | 0 |
| [`directconnect`](services/directconnect.yml) | 56 | 0 | 0 |
| [`cloudformation`](services/cloudformation.yml) | 54 | 1 | 3 |
| [`guardduty`](services/guardduty.yml) | 54 | 1 | 0 |
| [`elasticloadbalancing`](services/elasticloadbalancing.yml) | 54 | 0 | 1 |
| [`iotsitewise`](services/iotsitewise.yml) | 54 | 0 | 0 |
| [`s3`](services/s3.yml) | 53 | 51 | 39 |
| [`organizations`](services/organizations.yml) | 51 | 0 | 0 |
| [`comprehend`](services/comprehend.yml) | 51 | 0 | 0 |
| [`macie2`](services/macie2.yml) | 50 | 1 | 3 |
| [`lambda`](services/lambda.yml) | 48 | 1 | 3 |
| [`quicksight`](services/quicksight.yml) | 47 | 19 | 9 |
| [`appstream`](services/appstream.yml) | 47 | 0 | 3 |
| [`codedeploy`](services/codedeploy.yml) | 47 | 0 | 1 |
| [`rekognition`](services/rekognition.yml) | 47 | 0 | 0 |
| [`backup`](services/backup.yml) | 46 | 2 | 1 |
| [`dms`](services/dms.yml) | 45 | 2 | 0 |
| [`kms`](services/kms.yml) | 45 | 1 | 2 |
| [`cloudfront`](services/cloudfront.yml) | 45 | 0 | 1 |
| [`ecs`](services/ecs.yml) | 44 | 5 | 2 |
| [`elasticbeanstalk`](services/elasticbeanstalk.yml) | 44 | 3 | 2 |
| [`lex`](services/lex.yml) | 44 | 0 | 0 |
| [`workmail`](services/workmail.yml) | 43 | 0 | 53 |
| [`elasticache`](services/elasticache.yml) | 42 | 15 | 0 |
| [`dynamodb`](services/dynamodb.yml) | 42 | 3 | 6 |
| [`securityhub`](services/securityhub.yml) | 42 | 0 | 0 |
| [`workdocs`](services/workdocs.yml) | 41 | 0 | 10 |
| [`medialive`](services/medialive.yml) | 40 | 6 | 0 |
| [`imagebuilder`](services/imagebuilder.yml) | 40 | 2 | 0 |
| [`wafv2`](services/wafv2.yml) | 40 | 0 | 0 |
| [`robomaker`](services/robomaker.yml) | 40 | 0 | 0 |
| [`personalize`](services/personalize.yml) | 39 | 7 | 0 |
| [`logs`](services/logs.yml) | 39 | 3 | 5 |
| [`mechanicalturk`](services/mechanicalturk.yml) | 39 | 0 | 0 |
| [`codepipeline`](services/codepipeline.yml) | 37 | 0 | 0 |
| [`appsync`](services/appsync.yml) | 36 | 5 | 1 |
| [`amplify`](services/amplify.yml) | 36 | 1 | 0 |
| [`iotthingsgraph`](services/iotthingsgraph.yml) | 35 | 0 | 0 |
| [`swf`](services/swf.yml) | 34 | 3 | 12 |
| [`codebuild`](services/codebuild.yml) | 34 | 0 | 7 |
| [`iotanalytics`](services/iotanalytics.yml) | 33 | 1 | 0 |
| [`worklink`](services/worklink.yml) | 33 | 0 | 0 |
| [`sns`](services/sns.yml) | 33 | 0 | 0 |
| [`glacier`](services/glacier.yml) | 33 | 0 | 0 |
| [`appconfig`](services/appconfig.yml) | 33 | 0 | 0 |
| [`workspaces`](services/workspaces.yml) | 32 | 9 | 0 |
| [`inspector`](services/inspector.yml) | 32 | 5 | 0 |
| [`frauddetector`](services/frauddetector.yml) | 32 | 0 | 0 |
| [`codeartifact`](services/codeartifact.yml) | 31 | 0 | 4 |
| [`events`](services/events.yml) | 31 | 0 | 0 |
| [`cloudhsm`](services/cloudhsm.yml) | 31 | 0 | 0 |
| [`schemas`](services/schemas.yml) | 30 | 0 | 0 |
| [`elasticmapreduce`](services/elasticmapreduce.yml) | 29 | 4 | 8 |
| [`cloudwatch`](services/cloudwatch.yml) | 29 | 1 | 0 |
| [`connect`](services/connect.yml) | 29 | 0 | 6 |
| [`ecr`](services/ecr.yml) | 29 | 0 | 0 |
| [`es`](services/es.yml) | 28 | 9 | 9 |
| [`cloudsearch`](services/cloudsearch.yml) | 28 | 1 | 4 |
| [`sms`](services/sms.yml) | 28 | 0 | 2 |
| [`athena`](services/athena.yml) | 28 | 0 | 1 |
| [`appmesh`](services/appmesh.yml) | 28 | 0 | 1 |
| [`networkmanager`](services/networkmanager.yml) | 28 | 0 | 0 |
| [`machinelearning`](services/machinelearning.yml) | 28 | 0 | 0 |
| [`datasync`](services/datasync.yml) | 27 | 2 | 0 |
| [`kinesisvideo`](services/kinesisvideo.yml) | 27 | 0 | 3 |
| [`forecast`](services/forecast.yml) | 27 | 0 | 0 |
| [`kinesis`](services/kinesis.yml) | 26 | 2 | 0 |
| [`kinesisanalytics`](services/kinesisanalytics.yml) | 26 | 0 | 1 |
| [`mediastore`](services/mediastore.yml) | 26 | 0 | 0 |
| [`iot1click`](services/iot1click.yml) | 26 | 0 | 0 |
| [`mediaconvert`](services/mediaconvert.yml) | 25 | 0 | 0 |
| [`groundstation`](services/groundstation.yml) | 25 | 0 | 0 |
| [`globalaccelerator`](services/globalaccelerator.yml) | 25 | 0 | 0 |
| [`discovery`](services/discovery.yml) | 25 | 0 | 0 |
| [`transcribe`](services/transcribe.yml) | 24 | 0 | 3 |
| [`kendra`](services/kendra.yml) | 24 | 0 | 0 |
| [`route53domains`](services/route53domains.yml) | 23 | 5 | 0 |
| [`elasticfilesystem`](services/elasticfilesystem.yml) | 23 | 0 | 5 |
| [`servicediscovery`](services/servicediscovery.yml) | 23 | 0 | 0 |
| [`ram`](services/ram.yml) | 22 | 2 | 0 |
| [`dataexchange`](services/dataexchange.yml) | 22 | 0 | 1 |
| [`states`](services/states.yml) | 22 | 0 | 0 |
| [`route53resolver`](services/route53resolver.yml) | 22 | 0 | 0 |
| [`mq`](services/mq.yml) | 22 | 0 | 0 |
| [`kafka`](services/kafka.yml) | 21 | 2 | 0 |
| [`dax`](services/dax.yml) | 21 | 0 | 9 |
| [`eks`](services/eks.yml) | 21 | 0 | 0 |
| [`cognito-identity`](services/cognito-identity.yml) | 21 | 0 | 0 |
| [`qldb`](services/qldb.yml) | 20 | 0 | 3 |
| [`iotevents`](services/iotevents.yml) | 20 | 0 | 1 |
| [`xray`](services/xray.yml) | 20 | 0 | 0 |
| [`sqs`](services/sqs.yml) | 20 | 0 | 0 |
| [`managedblockchain`](services/managedblockchain.yml) | 20 | 0 | 0 |
| [`acm-pca`](services/acm-pca.yml) | 20 | 0 | 0 |
| [`mgh`](services/mgh.yml) | 19 | 1 | 0 |
| [`datapipeline`](services/datapipeline.yml) | 19 | 0 | 2 |
| [`ce`](services/ce.yml) | 19 | 0 | 0 |
| [`shield`](services/shield.yml) | 18 | 5 | 0 |
| [`codestar`](services/codestar.yml) | 18 | 0 | 3 |
| [`transfer`](services/transfer.yml) | 18 | 0 | 0 |
| [`secretsmanager`](services/secretsmanager.yml) | 18 | 0 | 0 |
| [`cloudtrail`](services/cloudtrail.yml) | 18 | 0 | 0 |
| [`access-analyzer`](services/access-analyzer.yml) | 18 | 0 | 0 |
| [`applicationinsights`](services/applicationinsights.yml) | 17 | 10 | 0 |
| [`snowball`](services/snowball.yml) | 17 | 2 | 0 |
| [`cognito-sync`](services/cognito-sync.yml) | 17 | 0 | 2 |
| [`fms`](services/fms.yml) | 17 | 0 | 0 |
| [`elastictranscoder`](services/elastictranscoder.yml) | 17 | 0 | 0 |
| [`servicequotas`](services/servicequotas.yml) | 16 | 0 | 0 |
| [`batch`](services/batch.yml) | 16 | 0 | 0 |
| [`opsworks-cm`](services/opsworks-cm.yml) | 15 | 4 | 0 |
| [`license-manager`](services/license-manager.yml) | 15 | 1 | 0 |
| [`mediaconnect`](services/mediaconnect.yml) | 14 | 8 | 0 |
| [`mediapackage`](services/mediapackage.yml) | 14 | 4 | 0 |
| [`support`](services/support.yml) | 14 | 0 | 8 |
| [`serverlessrepo`](services/serverlessrepo.yml) | 14 | 0 | 1 |
| [`fsx`](services/fsx.yml) | 14 | 0 | 0 |
| [`cloud9`](services/cloud9.yml) | 13 | 0 | 2 |
| [`lakeformation`](services/lakeformation.yml) | 13 | 0 | 1 |
| [`health`](services/health.yml) | 13 | 0 | 0 |
| [`codestar-notifications`](services/codestar-notifications.yml) | 13 | 0 | 0 |
| [`acm`](services/acm.yml) | 13 | 0 | 0 |
| [`mediapackage-vod`](services/mediapackage-vod.yml) | 12 | 4 | 0 |
| [`codeguru-profiler`](services/codeguru-profiler.yml) | 12 | 0 | 8 |
| [`detective`](services/detective.yml) | 12 | 0 | 5 |
| [`signer`](services/signer.yml) | 12 | 0 | 0 |
| [`resource-groups`](services/resource-groups.yml) | 12 | 0 | 0 |
| [`firehose`](services/firehose.yml) | 12 | 0 | 0 |
| [`synthetics`](services/synthetics.yml) | 11 | 2 | 0 |
| [`aws-marketplace`](services/aws-marketplace.yml) | 11 | 0 | 39 |
| [`codeguru-reviewer`](services/codeguru-reviewer.yml) | 10 | 0 | 3 |
| [`sdb`](services/sdb.yml) | 10 | 0 | 0 |
| [`application-autoscaling`](services/application-autoscaling.yml) | 10 | 0 | 0 |
| [`iot`](services/iot.yml) | 9 | 0 | 201 |
| [`translate`](services/translate.yml) | 9 | 0 | 0 |
| [`polly`](services/polly.yml) | 9 | 0 | 0 |
| [`compute-optimizer`](services/compute-optimizer.yml) | 9 | 0 | 0 |
| [`mobilehub`](services/mobilehub.yml) | 8 | 1 | 15 |
| [`sts`](services/sts.yml) | 8 | 0 | 2 |
| [`tag`](services/tag.yml) | 8 | 0 | 0 |
| [`sms-voice`](services/sms-voice.yml) | 8 | 0 | 0 |
| [`savingsplans`](services/savingsplans.yml) | 8 | 0 | 0 |
| [`dlm`](services/dlm.yml) | 8 | 0 | 0 |
| [`codestar-connections`](services/codestar-connections.yml) | 7 | 0 | 7 |
| [`mediatailor`](services/mediatailor.yml) | 7 | 0 | 0 |
| [`macie`](services/macie.yml) | 7 | 0 | 0 |
| [`textract`](services/textract.yml) | 6 | 0 | 0 |
| [`rds-data`](services/rds-data.yml) | 6 | 0 | 0 |
| [`importexport`](services/importexport.yml) | 6 | 0 | 0 |
| [`autoscaling-plans`](services/autoscaling-plans.yml) | 6 | 0 | 0 |
| [`outposts`](services/outposts.yml) | 5 | 2 | 0 |
| [`cur`](services/cur.yml) | 4 | 0 | 0 |
| [`pricing`](services/pricing.yml) | 3 | 0 | 0 |
| [`ebs`](services/ebs.yml) | 3 | 0 | 0 |
| [`comprehendmedical`](services/comprehendmedical.yml) | 2 | 19 | 0 |
| [`honeycode`](services/honeycode.yml) | 2 | 0 | 3 |
| [`pi`](services/pi.yml) | 2 | 0 | 0 |
| [`mobileanalytics`](services/mobileanalytics.yml) | 1 | 0 | 2 |
| [`workmailmessageflow`](services/workmailmessageflow.yml) | 1 | 0 | 0 |
| [`ec2-instance-connect`](services/ec2-instance-connect.yml) | 1 | 0 | 0 |
| [`execute-api`](services/execute-api.yml) | 0 | 215 | 3 |
| [`apigateway`](services/apigateway.yml) | 0 | 151 | 7 |
| [`budgets`](services/budgets.yml) | 0 | 14 | 2 |
| [`IoTSecuredTunneling`](services/IoTSecuredTunneling.yml) | 0 | 7 | 0 |
| [`elastic-inference`](services/elastic-inference.yml) | 0 | 6 | 1 |
| [`awsssoportal`](services/awsssoportal.yml) | 0 | 4 | 0 |
| [`awsssooidc`](services/awsssooidc.yml) | 0 | 3 | 0 |
| [`marketplacecommerceanalytics`](services/marketplacecommerceanalytics.yml) | 0 | 2 | 0 |
| [`sso`](services/sso.yml) | 0 | 0 | 54 |
| [`sso-directory`](services/sso-directory.yml) | 0 | 0 | 37 |
| [`deepracer`](services/deepracer.yml) | 0 | 0 | 26 |
| [`appmesh-preview`](services/appmesh-preview.yml) | 0 | 0 | 26 |
| [`deeplens`](services/deeplens.yml) | 0 | 0 | 24 |
| [`deepcomposer`](services/deepcomposer.yml) | 0 | 0 | 15 |
| [`appflow`](services/appflow.yml) | 0 | 0 | 15 |
| [`trustedadvisor`](services/trustedadvisor.yml) | 0 | 0 | 12 |
| [`chatbot`](services/chatbot.yml) | 0 | 0 | 12 |
| [`freertos`](services/freertos.yml) | 0 | 0 | 11 |
| [`dbqms`](services/dbqms.yml) | 0 | 0 | 9 |
| [`launchwizard`](services/launchwizard.yml) | 0 | 0 | 8 |
| [`cassandra`](services/cassandra.yml) | 0 | 0 | 7 |
| [`aws-portal`](services/aws-portal.yml) | 0 | 0 | 7 |
| [`ec2messages`](services/ec2messages.yml) | 0 | 0 | 6 |
| [`wellarchitected`](services/wellarchitected.yml) | 0 | 0 | 5 |
| [`iot-device-tester`](services/iot-device-tester.yml) | 0 | 0 | 5 |
| [`aws-marketplace-management`](services/aws-marketplace-management.yml) | 0 | 0 | 5 |
| [`ssmmessages`](services/ssmmessages.yml) | 0 | 0 | 4 |
| [`groundtruthlabeling`](services/groundtruthlabeling.yml) | 0 | 0 | 4 |
| [`artifact`](services/artifact.yml) | 0 | 0 | 4 |
| [`resource-explorer`](services/resource-explorer.yml) | 0 | 0 | 3 |
| [`awsconnector`](services/awsconnector.yml) | 0 | 0 | 3 |
| [`account`](services/account.yml) | 0 | 0 | 3 |
| [`sumerian`](services/sumerian.yml) | 0 | 0 | 2 |
| [`purchase-orders`](services/purchase-orders.yml) | 0 | 0 | 2 |
| [`wam`](services/wam.yml) | 0 | 0 | 1 |
| [`rds-db`](services/rds-db.yml) | 0 | 0 | 1 |
| [`neptune-db`](services/neptune-db.yml) | 0 | 0 | 1 |
| [`iq-permission`](services/iq-permission.yml) | 0 | 0 | 1 |
| [`iq`](services/iq.yml) | 0 | 0 | 1 |
| [`codeguru`](services/codeguru.yml) | 0 | 0 | 1 |
| [`backup-storage`](services/backup-storage.yml) | 0 | 0 | 1 |
| [`arsenal`](services/arsenal.yml) | 0 | 0 | 1 |

Most common action prefixes:

| Prefix | Count |
| ------ | ----- |
| `List` | 1148 |
| `Get` | 1096 |
| `Describe` | 1042 |
| `Delete` | 971 |
| `Create` | 885 |
| `Update` | 673 |
| `Put` | 236 |
| `Start` | 149 |
| `Tag` | 116 |
| `Untag` | 115 |

