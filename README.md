A handy lookup table of similar technology and services to help ex-googlers survive the *real* world :)  
pull-requests very welcomed. __Please do not list any confidential projects!__

See also: [The Hadoop Ecosystem Table](https://hadoopecosystemtable.github.io/)

## Technology

### Core Technology

| Google Internal   | Google External   |  Open Source / Real-World  |
| -------------     |  -------------       |-------------  |
| MapReduce         |     | [Apache Hadoop](https://github.com/apache/hadoop), [Spark](https://github.com/apache/spark)  |
| Protocol Buffer   | [Protobuf](https://github.com/google/protobuf)    | [Cap'n Proto](https://capnproto.org/), [Thrift](https://github.com/apache/thrift), [Avro](https://github.com/apache/avro) [Amazon Ion](https://amzn.github.io/ion-docs/)    |
| RPC | [gRPC](https://github.com/grpc/grpc) | Bolt, [Thrift](https://github.com/apache/thrift) |
| Chubby            |      | [Apache Zookeeper](https://github.com/apache/zookeeper), [etcd](https://github.com/coreos/etcd)      |
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
| BigTable     |   | [PrestoDB](https://prestodb.io/), [Cassandra](https://github.com/apache/cassandra), [HBase](https://github.com/apache/hbase), [Accumulo](https://github.com/apache/accumulo), [DynamoDB](https://aws.amazon.com/dynamodb) |
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

### DevOps
| Google Internal  | Google External | Real-World    |
| -------------|------------ |-------------|
| Blaze        |  [Bazel](http://bazel.io)          | [Buck](https://buckbuild.com/), [Pants](https://www.pantsbuild.org/), [please.build](https://please.build/) |
| Oncall       |             | [PagerDuty](https://pagerduty.com), [OpsGenie](https://www.opsgenie.com/), [VictorOps](https://victorops.com/) |
| varz/borgmon | | [Prometheus](https://prometheus.io), [librato](https://www.librato.com), [newrelic](http://newrelic.com), skylight, scout, also [this](https://vimeo.com/173610242) and [this](https://prometheus.io/docs/introduction/comparison/) |
| Exception/Error Tracking (??) | | Sentry.io, Raygun.io, Rollbar, Honeybadger, Airbrake, OverOps |
| styleguides | [google styleguides](https://github.com/google/styleguide) | [PEP-8](https://www.python.org/dev/peps/pep-0008/) |
| blaze test / build / CI | | buildkite, circleCI, travis, jenkins, gitlabCI |
| continuous delivery / releasing | | [lambdaCD](http://www.lambda.cd), screwdriver.cd, [CodeShip](https://codeship.com), [shipit-engine](https://github.com/Shopify/shipit-engine), [GoCD](https://www.gocd.org), [AWS CodeDeploy](https://aws.amazon.com/codedeploy/), [Capistrano](https://www.capistranorb.com), [Fabric](https://www.fabfile.org), [ConcourseCI](https://concourse.ci/)|
| borg / borgcfg || [AWS Cloudformation](https://aws.amazon.com/cloudformation/), Puppet, Chef, Salt, Ansible, [Terraform](https://www.terraform.io), [Jsonnet](http://jsonnet.org/) |
| logging || logstash, fluentd, papertrail, [cernan](https://github.com/postmates/cernan) |
| CodeSearch   |             | [Sourcegraph](https://sourcegraph.com) |
| cider |  | [Eclipse Che](https://www.eclipse.org/che/), Cloud9 |

## Operational
| Google Internal  |   Real-World  |
| -------------    | ------------- |
| free food        |   :(          |
| [software engineering at google](https://arxiv.org/ftp/arxiv/papers/1702/1702.01715.pdf) | |
| valentine        | [1Password](https://support.1password.com/create-share-vaults/)  [Lastpass](http://lastpass.com)|
| OWNERS files in repo     | [github CODEOWNERS](https://github.com/blog/2392-introducing-code-owners) |
| snippets | [Khan/snippets](https://github.com/Khan/snippets) |
| memegen | [memegen](http://www.memegen.com/) |
| edge, people ops training | [LifeLabs](http://lifelabsnewyork.com/) |
| googlegeist | [Culture Amp](https://www.cultureamp.com/), [humu](http://www.humu.com/) |

also check out [xoogler.co](http://xoogler.co/), which organizes events, slack channels etc

*disclaimer: I'm not affiliated with any of the technologies mentioned above.*
