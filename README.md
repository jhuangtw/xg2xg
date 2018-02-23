A handy lookup table of similar technology and services to help xooglers survive the *real* world :)  
pull-requests welcomed. this doc is only intended for well-known technology and services.

See also: [The Hadoop Ecosystem Table](https://hadoopecosystemtable.github.io/)

__Please do not list any confidential projects!__

## Technology

### Core Technology

| Google Internal   | Google Open Source   |  Open Source  |
| -------------     |  -------------       |-------------  |
| MapReduce         |     | [Apache Hadoop](https://github.com/apache/hadoop), [Spark](https://github.com/apache/spark)  |
| Protocol Buffer   | [Protobuf](https://github.com/google/protobuf)    | [Cap'n Proto](https://capnproto.org/), [Thrift](https://github.com/apache/thrift), [Avro](https://github.com/apache/avro)      |
| Network protocol | [gRPC](https://github.com/grpc/grpc) | Bolt, [Thrift](https://github.com/apache/thrift) |
| Chubby            |      | [Apache Zookeeper](https://github.com/apache/zookeeper), [etcd](https://github.com/coreos/etcd)      |
| ? | | [Apache Kafka](https://github.com/apache/kafka), [Apache Pulsar](https://github.com/apache/incubator-pulsar) |


### Infrastructure

| Google Internal   | Google Open Source   |  Open Source  |
| -------------     |  -------------       |-------------  |
| Borg              | [Kubernetes](https://kubernetes.io/) | [Apache Mesos](https://github.com/apache/mesos) |
| GSLB (load balancer)| | ELB, [Istio](https://istio.io/), [F5](https://f5.com/products/big-ip), [envoy](https://github.com/lyft/envoy) |


### Storage

| Google Internal  | Google Open Source | Open Source    |
| -------------|------------ |-------------|
| GFS/Colossus| | HDFS, [Ceph](https://ceph.com), [GlusterFS](https://www.gluster.org) |
| BigTable     |   | [PrestoDB](https://prestodb.io/), Cassandra, HBase, Accumulo, DynamoDB |
| [Spanner](http://research.google.com/archive/spanner.html)   | [cloud spanner](https://cloud.google.com/spanner/) | [CockroachDB](https://github.com/cockroachdb/cockroach), [TiDB](https://github.com/pingcap/tidb) | 
| columnIO | | Apache Parquet |
| sstable | levelDB | |


### Services

| Google Internal  | Google Open Source | Open Source | SaaS |
| -------------|------------ |-------------|-------------|
| Dremel       |   [bigquery](https://cloud.google.com/bigquery/)     | Apache Drill, [Presto](https://prestodb.io), Spark(sort-of), | AWS Athena, [Redshift Spectrum](https://aws.amazon.com/redshift/spectrum/) |
| Dremel UI    |             | https://redash.io/ | |
| Search (Mustang, Alexandria) |             | Elasticsearch, Solr, Lucene | [algolia](https://www.algolia.com/) |
| pubsub | [pubsub](https://cloud.google.com/pubsub/docs/overview) | RabbitMQ, [PubNub](https://www.pubnub.com/) | AWS SQS/SNS |

### DevOps
| Google Internal  | Google Open Source | Real World    |
| -------------|------------ |-------------|
| Blaze        |  [Bazel](http://bazel.io)          | [Buck](https://buckbuild.com/), [Pants](https://www.pantsbuild.org/) |
| Oncall       |             | [PagerDuty](https://pagerduty.com), [OpsGenie](https://www.opsgenie.com/), [VictorOps](https://victorops.com/) |
| varz/borgmon | | [Prometheus](https://prometheus.io), [librato](https://www.librato.com), [newrelic](http://newrelic.com), skylight, scout, also [this](https://vimeo.com/173610242) and [this](https://prometheus.io/docs/introduction/comparison/) |
| Exception/Error Tracking (??) | | Sentry.io, Raygun.io, Rollbar, Honeybadger, Airbrake, OverOps |
| styleguides | [google styleguides](https://github.com/google/styleguide) | [PEP-8](https://www.python.org/dev/peps/pep-0008/) |
| blaze test / build / CI | | buildkite, circleCI, travis, jenkins, gitlabCI |
| continuous delivery / releasing | | [lambdaCD](http://www.lambda.cd), screwdriver.cd, [CodeShip](https://codeship.com), [shipit-engine](https://github.com/Shopify/shipit-engine), [GoCD](https://www.gocd.org), [AWS CodeDeploy](https://aws.amazon.com/codedeploy/), [Capistrano](https://www.capistranorb.com), [Fabric](https://www.fabfile.org), [ConcourseCI](https://concourse.ci/)|
| borg / borgcfg || [AWS Cloudformation](https://aws.amazon.com/cloudformation/), Puppet, Chef, Salt, Ansible, [Terraform](https://www.terraform.io) |
| borgcfg || [Jsonnet](http://jsonnet.org/) |
| logging || logstash, fluentd, papertrail, [cernan](https://github.com/postmates/cernan) |
| CodeSearch   |             | [Sourcegraph](https://sourcegraph.com) |

## Operational
| Google Internal  |   Real World  |
| -------------    | ------------- |
| free food        |   :(          |
| [software engineering at google](https://arxiv.org/ftp/arxiv/papers/1702/1702.01715.pdf) | |
| valentine        | [1Password](https://support.1password.com/create-share-vaults/)  [Lastpass](http://lastpass.com)|
| OWNERS files in repo     | [github CODEOWNERS](https://github.com/blog/2392-introducing-code-owners) |
| snippets | [Khan/snippets](https://github.com/Khan/snippets) |
