A handy lookup table of similar technology and services to help ex-googlers survive the *real* world :)
pull-requests are very welcomed. __Please do not list any confidential projects!__

For a working example of (some) of these technologies integrated together, see:
https://github.com/google/startup-os

See also: [System Design Primer](https://github.com/donnemartin/system-design-primer), [The Hadoop Ecosystem Table](https://hadoopecosystemtable.github.io/), [Map AWS services to GCP products](https://cloud.google.com/free/docs/map-aws-google-cloud-platform), [Database of Databases](https://dbdb.io/), [Google Open Source Glossary](https://opensource.google/docs/glossary/)

## Technology

### Core Technology

| Google Internal | Google External                          | Open Source / Real-World                 |
| --------------- | ---------------------------------------- | ---------------------------------------- |
| MapReduce       |                                          | [Apache Hadoop](https://github.com/apache/hadoop), [Spark](https://github.com/apache/spark) |
| [Flume](https://research.google/pubs/flumejava-easy-efficient-data-parallel-pipelines/)   | [DataFlow](https://cloud.google.com/dataflow)  | [Apache Beam](https://beam.apache.org/) |
| Protocol Buffer | [Protobuf](https://github.com/google/protobuf), [FlatBuffers](https://google.github.io/flatbuffers/) | [Cap'n Proto](https://capnproto.org/), [Thrift](https://github.com/apache/thrift), [Avro](https://github.com/apache/avro), [Amazon Ion](https://amzn.github.io/ion-docs/), [CBOR](https://cbor.io/), [kryo](https://github.com/EsotericSoftware/kryo) |
| Stubby          | [gRPC](https://github.com/grpc/grpc)     | [Thrift](https://github.com/apache/thrift), [Bolt](https://boltprotocol.org/) |
| Chubby          |                                          | [Apache Zookeeper](https://github.com/apache/zookeeper), [etcd](https://github.com/coreos/etcd), [HashiCorp Consul](https://github.com/hashicorp/consul) |
| Goops / PubSub  | [Cloud Pub/Sub](https://cloud.google.com/pubsub)     | [Apache Kafka](https://github.com/apache/kafka), [Apache Pulsar](https://github.com/apache/incubator-pulsar), [Facebook LogDevice](https://github.com/facebookincubator/LogDevice) |
| `//base`        |                                          | [abseil](https://github.com/abseil) |

### Infrastructure

| Google Internal      | Google External                          | Open Source / Real-World                 |
| -------------------- | ---------------------------------------- | ---------------------------------------- |
| Borg                 | [Kubernetes](https://kubernetes.io/)     | [Apache Mesos](https://github.com/apache/mesos), [Apache Aurora](https://aurora.apache.org/), [HashiCorp Nomad](https://github.com/hashicorp/nomad) |
| GSLB | [Cloud Load Balancing](https://cloud.google.com/load-balancing) - Internal | AWS ELB,  [Istio](https://istio.io/), [linkerd](https://linkerd.io/)
| OnePlatform          | [API Gateway](https://cloud.google.com/api-gateway) | [Swagger](https://swagger.io/) |
| GFE, Maglev, uberproxy | [Cloud Load Balancing](https://cloud.google.com/load-balancing) - HTTPS / External | [envoy](https://www.envoyproxy.io/), AWS ALB, [HAProxy](https://www.haproxy.org/), [nginx](https://www.nginx.com/), [F5](https://f5.com/products/big-ip) |
| uberproxy (sso proxy) | [Identity-Aware Proxy](https://cloud.google.com/iap) | [buzzfeed-sso](https://github.com/buzzfeed/sso), [Pomerium](https://pomerium.io/), [Envoy Gateway](https://gateway.envoyproxy.io/docs/tasks/security/oidc/) |
| Zanzibar             | [Zanzibar Research Paper](https://research.google/pubs/pub48190/) | [SpiceDB](https://github.com/authzed/spicedb)/[authzed](https://authzed.com/), [Ory Keto](https://www.ory.sh/keto/docs/), [topaz](https://github.com/aserto-dev/topaz), [Opal](https://opal.dev/), [(iam)Keycloak](https://www.keycloak.org/), [Warrant](https://github.com/warrant-dev/warrant), [OpenFGA](https://openfga.dev/) |
| data center hardware | [open compute](https://www.opencompute.org/) |                                          |
| Jupiter, Starblaze   |                                          |                                             |
| B4, Stargate, TE     |                                          |                                             |
| USPS, Andromeda      |                                          |                                             |
| ESDN                 |                                          | [Faucet](https://github.com/faucetsdn/faucet)
| [broccoli man](https://www.youtube.com/watch?v=3t6L-FlfeaI)  | ||


### Storage

| Google Internal                          | Google External                          | Open Source / Real-World                 |
| ---------------------------------------- | ---------------------------------------- | ---------------------------------------- |
| GFS/Colossus                             |                                          | [HDFS](https://hadoop.apache.org/docs/r1.2.1/hdfs_design.html), [Ceph](https://ceph.com), [GlusterFS](https://www.gluster.org), [MooseFS](https://moosefs.com/products/#moosefs) |
| Bigtable                                 | [Cloud Bigtable](https://cloud.google.com/bigtable) | [PrestoDB](https://prestodb.io/), [Cassandra](https://github.com/apache/cassandra), [HBase](https://github.com/apache/hbase), [Accumulo](https://github.com/apache/accumulo), [DynamoDB](https://aws.amazon.com/dynamodb), [ScyllaDB](https://www.scylladb.com/) |
| [Spanner](https://research.google.com/archive/spanner.html) | [Cloud Spanner](https://cloud.google.com/spanner/) | [Vitess](https://vitess.io), [CockroachDB](https://github.com/cockroachdb/cockroach), [TiDB](https://github.com/pingcap/tidb) |
| ColumnIO / [Capacitor](https://cloud.google.com/blog/products/bigquery/inside-capacitor-bigquerys-next-generation-columnar-storage-format) | [BigQuery storage](https://cloud.google.com/bigquery/docs/storage_overview) | [Apache Parquet](https://parquet.apache.org), [ORC](https://orc.apache.org/docs/), [Apache Iceberg](https://iceberg.apache.org/) |
| sstable                                  | [levelDB](https://github.com/google/leveldb) | [RocksDB](https://rocksdb.org), [pebble](https://github.com/cockroachdb/pebble)      |
| zippy                                    | [Snappy](https://github.com/google/snappy) | [lz4](https://github.com/lz4/lz4)        |
| RecordIO                                 | [Riegeli](https://github.com/google/riegeli), [TFRecords](https://github.com/tensorflow/docs/blob/r1.10/site/en/api_guides/python/python_io.md#tfrecords-format-details), & in [OR-Tools](https://github.com/google/or-tools/blob/stable/ortools/base/recordio.h), [szl](https://github.com/google/szl/blob/master/src/utilities/recordio.cc) | [stuffed-record-stream](https://github.com/backtrace-labs/stuffed-record-stream) |


### Services
| Google Internal                          | Google External                          | Open Source                              | SaaS                                     |
| ---------------------------------------- | ---------------------------------------- | ---------------------------------------- | ---------------------------------------- |
| Dremel                                   | [BigQuery](https://cloud.google.com/bigquery/) | [Apache Drill](https://github.com/apache/drill), [Presto](https://prestodb.io), Spark(sort-of), | [AWS Athena](https://aws.amazon.com/athena/), [Redshift Spectrum](https://aws.amazon.com/redshift/spectrum/), [Snowflake](https://www.snowflake.com) |
| Dremel UI                                |                                          | [Redash](https://github.com/getredash/redash), [Metabase](https://github.com/metabase/metabase), [Apache Superset](https://github.com/apache/incubator-superset) |                                          |
| Search (Mustang, Alexandria)             |                                          | [Elasticsearch](https://github.com/elastic/elasticsearch), [OpenSearch](https://opensearch.org/), Solr, Lucene              | [algolia](https://www.algolia.com/)      |
| pubsub                                   | [pubsub](https://cloud.google.com/pubsub/docs/overview) | [NATS.io](https://nats.io), [RabbitMQ](https://github.com/rabbitmq), [PubNub](https://www.pubnub.com/) | AWS SQS/SNS, [AWS AppSync](https://aws.amazon.com/appsync) |
| [MillWheel](https://ai.google/research/pubs/pub41378) | [Cloud Dataflow](https://cloud.google.com/dataflow/) | [Apache Flink](https://flink.apache.org/), beam |                |
| Colab | [Colaboratory](https://colab.research.google.com/) | [Jupyter](https://jupyter.org) | [Observable](https://observablehq.com/) |
| PLX | [Google Data Studio](https://datastudio.google.com/) | | [Mode](https://mode.com) |
| Monarch | [paper](https://research.google/pubs/pub50652/) | | |
| Napa | [paper](https://research.google/pubs/pub50617/) | | |
| MakerSuite| [MakerSuite](https://makersuite.google.com) | | |


### DevOps
| Google Internal                 | Google External                          | Real-World                               |
| ------------------------------- | ---------------------------------------- | ---------------------------------------- |
| Assimilator                     |                                          | [Dominator](https://github.com/Cloud-Foundations/Dominator) |
| Blaze                           | [Bazel](https://bazel.build)             | [Buck](https://buckbuild.com/), [Pants](https://www.pantsbuild.org/), [please.build](https://please.build/), [Blade](https://github.com/chen3feng/blade-build), [recc](https://gitlab.com/bloomberg/recc), [EngFlow](https://www.engflow.com/), [BuildBuddy](https://www.buildbuddy.io/), [flare.build](https://flare.build) |
| Oncall                          |                                          | [PagerDuty](https://pagerduty.com), [OpsGenie](https://www.opsgenie.com/), [VictorOps](https://victorops.com/) |
| varz/borgmon/monarch            | [Cloud Monitoring](https://cloud.google.com/monitoring) | [Datadog](https://www.datadoghq.com/), [Prometheus](https://prometheus.io), [M3](https://m3db.io/), [librato](https://www.librato.com), [newrelic](https://newrelic.com), skylight, scout, [Scotty](https://github.com/Cloud-Foundations/scotty)/[tricorder](https://github.com/Cloud-Foundations/tricorder), [netdata](https://github.com/netdata/netdata), [bosun](https://bosun.org/), also [this](https://vimeo.com/173610242) and [this](https://prometheus.io/docs/introduction/comparison/) |
| Viceroy                         | Cloud Monitoring                         | [Grafana](https://grafana.com/) |
| Exception/Error Tracking (thirdeye)   |                                          | Sentry.io, Raygun.io, [Rollbar](https://rollbar.com), Honeybadger, Airbrake, OverOps, [ELK stack](https://www.elastic.co/what-is/elk-stack) |
| styleguides                     | [google styleguides](https://github.com/google/styleguide) | [PEP-8](https://www.python.org/dev/peps/pep-0008/), [HoundCI auto-style-reviewer](https://houndci.com/) |
| Sponge                          |                                          | [EngFlow](https://www.engflow.com/) |
| Blaze/Forge/TAP/BuildCop        | [Cloud Build](https://cloud.google.com/cloud-build/) | [buildkite](https://buildkite.com/), [CircleCI](https://circleci.com), [Drone](https://drone.io/), [EngFlow](https://www.engflow.com/), [github](https://github.blog/2019-08-08-github-actions-now-supports-ci-cd/), [gitlabCI](https://about.gitlab.com/product/continuous-integration/), [jenkins](https://jenkins.io/), [travis](https://travis-ci.org/) |
| Forge/ObjFS                     |                                          | [EngFlow](https://www.engflow.com/), [flare.build](https://flare.build) |
| Sandman(test env)/Guitar        |                                          |                   |
| Sisyphus / Rapid                |                                          | [Spinnaker](https://www.spinnaker.io/), [lambdaCD](https://www.lambda.cd), screwdriver.cd, [CodeShip](https://codeship.com), [shipit-engine](https://github.com/Shopify/shipit-engine), [GoCD](https://www.gocd.org), [AWS CodeDeploy](https://aws.amazon.com/codedeploy/), [Capistrano](https://www.capistranorb.com), [Fabric](https://www.fabfile.org), [ConcourseCI](https://concourse.ci/), [samson](https://github.com/zendesk/samson) |
| MPM                             |                                          | [Docker](https://www.docker.com/), [OCI](https://opencontainers.org/) |
| borgcfg / gcl, [Prodspec + Annealing](https://www.usenix.org/publications/loginonline/prodspec-and-annealing-intent-based-actuation-google-production)            | [Jsonnet](https://jsonnet.org/), [Cue](https://cuelang.org/) | [AWS Cloudformation](https://aws.amazon.com/cloudformation/), Puppet, Chef, Salt, Ansible, [Terraform](https://www.terraform.io), [kubecfg](https://github.com/kubecfg/kubecfg), [pulumi](https://github.com/pulumi/pulumi), [Nix](https://nix.dev/), [Pkl](https://pkl-lang.org/) |
| logging, analog                 | [StackDriver](https://cloud.google.com/stackdriver/) | [logstash](https://github.com/elastic/logstash), [fluentd](https://github.com/fluent/fluentd), [PaperTrail](https://www.papertrail.com/), [cernan](https://github.com/postmates/cernan), [loki](https://grafana.com/oss/loki/) |
| CodeSearch, Grimoire            | [Zoekt](https://github.com/google/zoekt) [kythe](https://github.com/kythe/kythe) [Code Search](https://developers.google.com/code-search/user/getting-started) (for Google open source code only, with separate UI for Android and Chromium. Go CLI [source](https://github.com/google/codesearch).) | [Sourcegraph](https://sourcegraph.com), [OpenGrok](https://github.com/OpenGrok/OpenGrok/), [livegrep](https://github.com/livegrep/livegrep) |
| Critique, Gerrit, Mondrian etc. | [Gerrit](https://www.gerritcodereview.com/) | [Reviewable](https://reviewable.io) , [Phabricator](https://www.phacility.com/phabricator/)     |
| cider                           |                                          | [Eclipse Che](https://www.eclipse.org/che/), [Cloud9](https://c9.io/), [gitpod.io](https://gitpod.io), [Coder](https://coder.com/), [Code-Server (VSCode in a Tab)](https://github.com/cdr/code-server), [DevZero](https://www.devzero.io/) |
| buganizer                       | [Google Issue Tracker](https://issuetracker.google.com/) | [JIRA](https://www.atlassian.com/software/jira), [bugzilla](https://www.bugzilla.org/), github issues, [Linear](https://linear.app/) |
| Bugjuggler                      |                                          | [SnoozeThis](https://www.snoozethis.com/) |
| ToTT                            | [Google Test Blog](https://testing.googleblog.com/) | [Increment](https://increment.com/) |
| Copybara / MOE                  | [Copybara](https://github.com/google/copybara), [MOE](https://github.com/google/MOE)  |                                          |
| workflow/dependency management | | [Luigi](https://github.com/spotify/luigi), [Airflow](https://github.com/apache/airflow), [digdag](https://github.com/treasure-data/digdag), [Pachyderm](https://github.com/pachyderm/pachyderm), [Dask](https://github.com/dask/dask) |
| ErrorProne                      | [ErrorProne](https://errorprone.info/)   | [SpotBugs](https://spotbugs.github.io/), [FindBugs](https://findbugs.sourceforge.net/) |
| [Dapper](https://ai.google/research/pubs/pub36356) | [stackdriver trace](https://cloud.google.com/trace/) | [zipkin](https://github.com/openzipkin/zipkin), [OpenTelemetry](https://opentelemetry.io/), [jaeger](https://www.jaegertracing.io/), [LightStep](https://lightstep.com), [Honeycomb](https://www.honeycomb.io/trace/) |
| C++ Tips of the Week            | [Abseil C++ Tips of the Week](https://abseil.io/tips/) |  |
| [DiRT](https://cloud.google.com/blog/products/management-tools/shrinking-the-time-to-mitigate-production-incidents) | | [ChaosMonkey](https://github.com/Netflix/chaosmonkey), [aws fis](https://aws.amazon.com/fis/) |
| [Rosie](https://cacm.acm.org/magazines/2016/7/204032-why-google-stores-billions-of-lines-of-code-in-a-single-repository/fulltext) | | [microplane](https://github.com/Clever/microplane), [silver-platter](https://github.com/jelmer/silver-platter) |
| API Improvements Proposals | [AIP](https://google.aip.dev/) | |
| g4 {fix, submit} | | [Trunk.io](https://trunk.io), [Graphite](https://graphite.dev/) |
| probers | | [cloudprober](https://github.com/cloudprober/cloudprober) |
| GWP | [paper](https://static.googleusercontent.com/media/research.google.com/en//pubs/archive/36575.pdf) | [Parca](https://www.parca.dev), [Polar Signals](https://www.polarsignals.com) |

### Security
| Google Internal                  | Google External | Open Source                              |
| -------------------------------- | --------------- | ---------------------------------------- |
| prodaccess/LOAS                  |                 | [Keymaster](https://github.com/Cloud-Foundations/keymaster) |
| prod secrets/identity management |                 | [chamber](https://github.com/segmentio/chamber), [knox](https://github.com/pinterest/knox), [SPIFFE](https://spiffe.io/) |

## IT / Operations / Misc
| Google Internal                          | Real-World                               |
| ---------------------------------------- | ---------------------------------------- |
| software engineering at google [1](https://arxiv.org/ftp/arxiv/papers/1702/1702.01715.pdf), [2](https://abseil.io/resources/swe-book) | [Software Engineering at Google: Lessons Learned from Programming Over Time](https://www.amazon.com/Software-Engineering-Google-Lessons-Programming/dp/1492082791) |
| [SRE @ google](https://sre.google/sre-book/table-of-contents/) | |
| valentine                                | [Vault](https://www.vaultproject.io/), [1Password](https://support.1password.com/create-share-vaults/), [Lastpass](https://lastpass.com), [pass](https://www.passwordstore.org/), [keeper](https://www.keepersecurity.com/) |
| OWNERS files in repo                     | [github CODEOWNERS](https://github.com/blog/2392-introducing-code-owners) |
| snippets                                 | [Khan/snippets](https://github.com/Khan/snippets) |
| SnipIt                                   | [recordit](https://recordit.co/), [CloudApp](https://www.getcloudapp.com/), [dropbox screenshots](https://help.dropbox.com/installs-integrations/photos/screenshots), [Snippyly](https://snippyly.com/) |
| gpaste                                   | [pastee](https://paste.ee/), [pastebin](https://pastebin.com/) |
| stuff (SaaS IT management)               | [productiv](https://productiv.com/), [intello](https://www.intello.io/), [zylo](https://zylo.com/) |
| stuff (Device Management)                | [jamf](https://www.jamf.com/) |
| device security monitoring               | [Red Canary](https://redcanary.com/) |
| beyondcorp | [beyondcorp](https://www.beyondcorp.com/) |
| [go/ links](https://medium.com/@golinks/the-full-history-of-go-links-and-the-golink-system-cbc6d2c8bb3)                                | [golinks](https://www.golinks.io/), [go](https://github.com/kellegous/go), [Goat](https://goatcodes.com/), [trotto](https://github.com/trotto/go-links), [go-shorten](https://github.com/thomasdesr/go-shorten) |
| google3 philosophy                       | [innersource](https://resources.github.com/whitepapers/introduction-to-innersource/), [monorepo](https://cacm.acm.org/magazines/2016/7/204032-why-google-stores-billions-of-lines-of-code-in-a-single-repository/fulltext), [YouTube talk](https://www.youtube.com/watch?v=W71BTkUbdqE) |
| doing code review                        | [code review](https://google.github.io/eng-practices/review/reviewer/) |
| safely sharing 1-time secrets            | [sendsecure.ly](https://sendsecure.ly), [croc](https://github.com/schollz/croc), [onetimesecret](https://github.com/onetimesecret/onetimesecret), [privatebin](https://privatebin.info/) |
| messaging                                | [mattermost](https://github.com/mattermost/mattermost-server), [Slack](https://slack.com), gchat |
| tech talks | [TechTalks @ Google](https://www.youtube.com/user/GoogleTechTalks/videos) |
| g3doc | [writethedocs](https://www.writethedocs.org/), [docs-as-code](https://idratherbewriting.com/learnapidoc/pubapis_docs_as_code.html) |
| GUTS | [spoke](https://www.atspoke.com/), [freshservice](https://freshservice.com/) |
| MOMA | [glean](https://www.glean.com/) |

## PeopleOps / Culture
| Google Internal                          | Real-World                               |
| ---------------------------------------- | ---------------------------------------- |
| [OKR](https://en.wikipedia.org/wiki/OKR) | [CultureAmp OKR](https://www.cultureamp.com/okr-solution-b), [Lattice Goals](https://lattice.com/goals), [Ally](https://www.ally.io/), [workboard](https://www.workboard.com/) |
| HRIS/ERP                                 | [Namely](https://namely.com), [BambooHR](https://www.bamboohr.com/), [Workday](https://workday.com), [Paylocity](https://www.paylocity.com/) |
| [peer bonus](https://www.forbes.com/sites/jurgenappelo/2015/07/08/the-peer-to-peer-bonus-system/#33c47ef84329)   | [bonus.ly](https://bonus.ly/) |
| kudos  | [heytaco](https://www.heytaco.chat/), [slack ++ bot](https://github.com/tdmalone/working-plusplus/) |
| perks | [fond](https://fond.co) |
| talks | [Talks @ Google](https://www.youtube.com/c/talksatgoogle/videos) |
| dory | [slido](https://www.sli.do/), [dory(app)](https://dory.app/) |
| edge, people ops training                | [LifeLabs](https://www.lifelabslearning.com/)  |
| googlegeist                              | [Culture Amp](https://www.cultureamp.com/), [humu](https://www.humu.com/), [tinypulse](https://www.tinypulse.com/), [peakon](https://peakon.com/) |
| Meng                                     | [Search Inside Yourself](https://www.amazon.com/Search-Inside-Yourself-Unexpected-Achieving/dp/0062116932) |
| Lazlo                                    | [Work Rules](https://www.amazon.com/Work-Rules-Insights-Inside-Transform/dp/1455554790/) |
| Claire Stapleton                         | [Tech Support - existential advice for the modern tech worker](https://techsupport.substack.com/) |
| books about google | [How Google Works](https://www.amazon.com/How-Google-Works-Eric-Schmidt/dp/1455582328), [In The Plex](https://www.amazon.com/Plex-Google-Thinks-Works-Shapes/dp/1416596585), [Software Engineering at Google](https://www.amazon.com/Software-Engineering-Google-Lessons-Programming/dp/1492082791) |


also check out [xoogler.co](https://xoogler.co/), which organizes events, slack channels etc

*disclaimer: I'm not affiliated with any of the technologies/products mentioned above.*

*disclaimer: I left Google a number of years ago so some of the naming might be dated.*
