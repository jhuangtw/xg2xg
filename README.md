A handy lookup table of similar technology and services to help ex-googlers survive the *real* world :)  
pull-requests very welcomed. __Please do not list any confidential projects!__

For a working example of (some) of these technologies integrated together, see:
https://github.com/google/startup-os

See also: [System Design Primer](https://github.com/donnemartin/system-design-primer), [The Hadoop Ecosystem Table](https://hadoopecosystemtable.github.io/), [Map AWS services to GCP products](https://cloud.google.com/free/docs/map-aws-google-cloud-platform)

## Technology

### Core Technology

| Google Internal   | Google External   |  Open Source / Real-World  |
| -------------     |  -------------       |-------------  |
| MapReduce         |     | [Apache Hadoop](https://github.com/apache/hadoop), [Spark](https://github.com/apache/spark)  |
| Protocol Buffer   | [Protobuf](https://github.com/google/protobuf)    | [Cap'n Proto](https://capnproto.org/), [Thrift](https://github.com/apache/thrift), [Avro](https://github.com/apache/avro), [Amazon Ion](https://amzn.github.io/ion-docs/)    |
| Stubby | [gRPC](https://github.com/grpc/grpc) | Bolt, [Thrift](https://github.com/apache/thrift) |
| Chubby            |      | [Apache Zookeeper](https://github.com/apache/zookeeper), [etcd](https://github.com/coreos/etcd), [Consul](https://www.consul.io/)      |
| ? | | [Apache Kafka](https://github.com/apache/kafka), [Apache Pulsar](https://github.com/apache/incubator-pulsar) |


### Infrastructure

| Google Internal   | Google External   |  Open Source / Real-World  |
| -------------     |  -------------       |-------------  |
| Borg              | [Kubernetes](https://kubernetes.io/) | [Apache Mesos](https://github.com/apache/mesos) |
| GSLB (load balancer)| | ELB, [HAProxy](http://www.haproxy.org/), [Istio](https://istio.io/), [F5](https://f5.com/products/big-ip), [envoy](https://github.com/lyft/envoy) |
| data center hardware | [open compute](http://www.opencompute.org/) |  |


### Storage

| Google Internal  | Google External | Open Source / Real-World  |
| -------------|------------ |-------------|
| GFS/Colossus| | HDFS, [Ceph](https://ceph.com), [GlusterFS](https://www.gluster.org) |
| BigTable     | [Cloud BigTable](https://cloud.google.com/bigtable)  | [PrestoDB](https://prestodb.io/), [Cassandra](https://github.com/apache/cassandra), [HBase](https://github.com/apache/hbase), [Accumulo](https://github.com/apache/accumulo), [DynamoDB](https://aws.amazon.com/dynamodb) |
| [Spanner](http://research.google.com/archive/spanner.html)   | [Cloud Spanner](https://cloud.google.com/spanner/) | [CockroachDB](https://github.com/cockroachdb/cockroach), [TiDB](https://github.com/pingcap/tidb) |
| ColumnIO / [Capacitor](https://cloud.google.com/blog/big-data/2016/04/inside-capacitor-bigquerys-next-generation-columnar-storage-format) | | [Apache Parquet](http://parquet.apache.org) |
| sstable | [levelDB](https://github.com/google/leveldb) | |
| zippy | [Snappy](https://github.com/google/snappy) | [lz4](https://github.com/lz4/lz4) |


### Services

| Google Internal  | Google External | Open Source | SaaS |
| -------------|------------ |-------------|-------------|
| Dremel       |   [bigquery](https://cloud.google.com/bigquery/)     | Apache Drill, [Presto](https://prestodb.io), Spark(sort-of), | AWS Athena, [Redshift Spectrum](https://aws.amazon.com/redshift/spectrum/) |
| Dremel UI    |             | [Redash](https://github.com/getredash/redash) | |
| Search (Mustang, Alexandria) |             | Elasticsearch, Solr, Lucene | [algolia](https://www.algolia.com/) |
| pubsub | [pubsub](https://cloud.google.com/pubsub/docs/overview) | RabbitMQ, [PubNub](https://www.pubnub.com/) | AWS SQS/SNS |
| [Flume (Java)](https://ai.google/research/pubs/pub35650) |             | [Apache Crunch](https://crunch.apache.org/) |     |

### DevOps
| Google Internal  | Google External | Real-World    |
| -------------|------------ |-------------|
| Assimilator  |             | [Dominator](https://github.com/Symantec/Dominator) |
| Blaze        |  [Bazel](http://bazel.io)          | [Buck](https://buckbuild.com/), [Pants](https://www.pantsbuild.org/), [please.build](https://please.build/) |
| Oncall       |             | [PagerDuty](https://pagerduty.com), [OpsGenie](https://www.opsgenie.com/), [VictorOps](https://victorops.com/) |
| varz/borgmon | | [Datadog](https://www.datadoghq.com/), [Prometheus](https://prometheus.io), [librato](https://www.librato.com), [newrelic](http://newrelic.com), skylight, scout, [Scotty](https://github.com/Symantec/scotty)/[tricorder](https://github.com/Symantec/tricorder), also [this](https://vimeo.com/173610242) and [this](https://prometheus.io/docs/introduction/comparison/) |
| Exception/Error Tracking (??) | | Sentry.io, Raygun.io, Rollbar, Honeybadger, Airbrake, OverOps |
| styleguides | [google styleguides](https://github.com/google/styleguide) | [PEP-8](https://www.python.org/dev/peps/pep-0008/), [HoundCI auto-style-reviewer](https://houndci.com/) |
| blaze test / build / CI | | buildkite, circleCI, travis, jenkins, gitlabCI |
| continuous delivery / releasing | | [Spinnaker](https://www.spinnaker.io/), [lambdaCD](http://www.lambda.cd), screwdriver.cd, [CodeShip](https://codeship.com), [shipit-engine](https://github.com/Shopify/shipit-engine), [GoCD](https://www.gocd.org), [AWS CodeDeploy](https://aws.amazon.com/codedeploy/), [Capistrano](http://www.capistranorb.com), [Fabric](http://www.fabfile.org), [ConcourseCI](https://concourse.ci/) | [Convox](https://convox.com/) |
| borg / borgcfg / gcl || [AWS Cloudformation](https://aws.amazon.com/cloudformation/), Puppet, Chef, Salt, Ansible, [Terraform](https://www.terraform.io), [Jsonnet](http://jsonnet.org/) |
| logging |[StackDriver](https://cloud.google.com/stackdriver/)| logstash, fluentd, papertrail, [cernan](https://github.com/postmates/cernan) |
| CodeSearch   | [Zoekt](https://github.com/google/zoekt) | [Sourcegraph](https://sourcegraph.com) |
| cider |  | [Eclipse Che](https://www.eclipse.org/che/), Cloud9 |
| buganizer | | JIRA, bugzilla, github issues |
| ToTT | [Google Test Blog](https://testing.googleblog.com/) | |

### Security
| Google Internal  | Google External | Real-World    |
| -------------|------------ |-------------|
| prodaccess   |             | [Keymaster](https://github.com/Symantec/keymaster) |
| prod secrets/identity management | | [knox](https://github.com/pinterest/knox), [SPIFFE](https://spiffe.io/) |

## IT / Operations
| Google Internal  |   Real-World  |
| -------------    | ------------- |
| free food        |   :(          |
| [software engineering at google](https://arxiv.org/ftp/arxiv/papers/1702/1702.01715.pdf) | |
| valentine        | [1Password](https://support.1password.com/create-share-vaults/), [Lastpass](http://lastpass.com)|
| OWNERS files in repo     | [github CODEOWNERS](https://github.com/blog/2392-introducing-code-owners) |
| snippets | [Khan/snippets](https://github.com/Khan/snippets) |
| memegen | [memegen](http://www.memegen.com/) |
| edge, people ops training | [LifeLabs](http://lifelabsnewyork.com/) |
| googlegeist | [Culture Amp](https://www.cultureamp.com/), [humu](http://www.humu.com/) |
| stuff (SaaS IT management) | [intello](https://www.intello.io/), [zylo](https://zylo.com/) |
| stuff (Device Management) | [Fleetsmith](https://www.fleetsmith.com/), [jamf](https://www.jamf.com/), [rippling IT](https://www.rippling.com/it/) |
| go/ links | [golinks](https://www.golinks.io/), [go](https://github.com/kellegous/go) |

also check out [xoogler.co](http://xoogler.co/), which organizes events, slack channels etc

*disclaimer: I'm not affiliated with any of the technologies mentioned above.*
