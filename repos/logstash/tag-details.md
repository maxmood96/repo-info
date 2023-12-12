<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `logstash`

-	[`logstash:7.17.15`](#logstash71715)
-	[`logstash:8.11.1`](#logstash8111)

## `logstash:7.17.15`

```console
$ docker pull logstash@sha256:15f41f0762756248e98fc74f600108f76fa699d9e98406113f20099e33137c48
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `logstash:7.17.15` - linux; amd64

```console
$ docker pull logstash@sha256:981a501d715d5a6aa90f1bf61fb57c367fb5cbc9b143a8a098da406a5bb214c9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **449.3 MB (449258515 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8252bbbc4eaa61788faefb42205b27c3f64b7ca9c4599a45e4dfabad3f229c2b`
-	Entrypoint: `["\/usr\/local\/bin\/docker-entrypoint"]`

```dockerfile
# Mon, 13 Nov 2023 18:15:06 GMT
ARG RELEASE
# Mon, 13 Nov 2023 18:15:06 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 13 Nov 2023 18:15:06 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 13 Nov 2023 18:15:06 GMT
LABEL org.opencontainers.image.version=20.04
# Mon, 13 Nov 2023 18:15:06 GMT
ADD file:9169bb1d6ef21313aed17e924538fee03d858460ae6b05e01968457dfc043bd7 in / 
# Mon, 13 Nov 2023 18:15:06 GMT
CMD ["/bin/bash"]
# Mon, 13 Nov 2023 18:15:06 GMT
RUN for iter in {1..10}; do export DEBIAN_FRONTEND=noninteractive && apt-get update -y && apt-get upgrade -y && apt-get install -y procps findutils tar gzip curl && apt-get install -y locales && apt-get clean all && locale-gen 'en_US.UTF-8' &&     apt-get clean metadata && exit_code=0 && break || exit_code=$? &&     echo "packaging error: retry $iter in 10s" &&     apt-get clean all && apt-get clean metadata && sleep 10; done;     (exit $exit_code) # buildkit
# Mon, 13 Nov 2023 18:15:06 GMT
RUN groupadd --gid 1000 logstash &&     adduser --uid 1000 --gid 1000        --home /usr/share/logstash --no-create-home       logstash # buildkit
# Mon, 13 Nov 2023 18:15:06 GMT
RUN curl -Lo - https://artifacts.elastic.co/downloads/logstash/logstash-7.17.15-linux-$(arch).tar.gz |     tar zxf - -C /usr/share &&     mv /usr/share/logstash-7.17.15 /usr/share/logstash && chown --recursive logstash:logstash /usr/share/logstash/ &&     chown -R logstash:root /usr/share/logstash &&     chmod -R g=u /usr/share/logstash &&     mkdir /licenses/ &&     mv /usr/share/logstash/NOTICE.TXT /licenses/NOTICE.TXT &&     mv /usr/share/logstash/LICENSE.txt /licenses/LICENSE.txt &&     find /usr/share/logstash -type d -exec chmod g+s {} \; &&     ln -s /usr/share/logstash /opt/logstash # buildkit
# Mon, 13 Nov 2023 18:15:06 GMT
WORKDIR /usr/share/logstash
# Mon, 13 Nov 2023 18:15:06 GMT
ENV ELASTIC_CONTAINER=true
# Mon, 13 Nov 2023 18:15:06 GMT
ENV PATH=/usr/share/logstash/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 13 Nov 2023 18:15:06 GMT
ADD config/pipelines.yml config/pipelines.yml # buildkit
# Mon, 13 Nov 2023 18:15:06 GMT
ADD config/logstash-full.yml config/logstash.yml # buildkit
# Mon, 13 Nov 2023 18:15:06 GMT
ADD config/log4j2.properties config/ # buildkit
# Mon, 13 Nov 2023 18:15:06 GMT
ADD pipeline/default.conf pipeline/logstash.conf # buildkit
# Mon, 13 Nov 2023 18:15:06 GMT
RUN chown --recursive logstash:root config/ pipeline/ # buildkit
# Mon, 13 Nov 2023 18:15:06 GMT
ENV LANG=en_US.UTF-8 LC_ALL=en_US.UTF-8
# Mon, 13 Nov 2023 18:15:06 GMT
ADD env2yaml/env2yaml /usr/local/bin/ # buildkit
# Mon, 13 Nov 2023 18:15:06 GMT
ADD bin/docker-entrypoint /usr/local/bin/ # buildkit
# Mon, 13 Nov 2023 18:15:06 GMT
RUN chmod 0755 /usr/local/bin/docker-entrypoint # buildkit
# Mon, 13 Nov 2023 18:15:06 GMT
USER 1000
# Mon, 13 Nov 2023 18:15:06 GMT
EXPOSE map[5044/tcp:{} 9600/tcp:{}]
# Mon, 13 Nov 2023 18:15:06 GMT
LABEL org.label-schema.schema-version=1.0 org.label-schema.vendor=Elastic org.opencontainers.image.vendor=Elastic org.label-schema.name=logstash org.opencontainers.image.title=logstash org.label-schema.version=7.17.15 org.opencontainers.image.version=7.17.15 org.label-schema.url=https://www.elastic.co/products/logstash org.label-schema.vcs-url=https://github.com/elastic/logstash org.label-schema.license=Elastic License org.opencontainers.image.licenses=Elastic License org.opencontainers.image.description=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' org.label-schema.build-date=2023-10-10T17:45:59+00:00 org.opencontainers.image.created=2023-10-10T17:45:59+00:00
# Mon, 13 Nov 2023 18:15:06 GMT
ENTRYPOINT ["/usr/local/bin/docker-entrypoint"]
```

-	Layers:
	-	`sha256:25ad149ed3cff49ddb57ceb4418377f63c897198de1f9de7a24506397822de3e`  
		Last Modified: Tue, 28 Nov 2023 05:37:19 GMT  
		Size: 27.5 MB (27512563 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ea1dd30ed5345f9a075fe3dd998885fe70d01cda4af47e2defbaa1c58dd92a8`  
		Last Modified: Tue, 12 Dec 2023 17:17:05 GMT  
		Size: 53.0 MB (53034538 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fd6a06bf9b2171d61cf2d5f51e7f8af3a39e83cfcc4194363fa78a3be185b28`  
		Last Modified: Tue, 12 Dec 2023 17:17:04 GMT  
		Size: 1.8 KB (1804 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36a44393f770a282819dd8debb11a2cc6d9bdb39289234bff2db10759a3ecf0e`  
		Last Modified: Tue, 12 Dec 2023 17:17:11 GMT  
		Size: 366.9 MB (366860961 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78991df294eb4bbf423c19dff8a34d92b6d5d4ee12ff1e6527aa5ad8571a0fcd`  
		Last Modified: Tue, 12 Dec 2023 17:17:05 GMT  
		Size: 381.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14ce72cd40c302db58f7b8aa185708d98392dfdfdcee35fc02a14e0937b4aebd`  
		Last Modified: Tue, 12 Dec 2023 17:17:05 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0dd19ca0e5909c91562a86b508f364315348899e4ea5c0316e35e3d75f022b5`  
		Last Modified: Tue, 12 Dec 2023 17:17:07 GMT  
		Size: 474.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed11fc4bf7ab94e6e626220335941265ca2b451a9700421ee29e5bb2025134cd`  
		Last Modified: Tue, 12 Dec 2023 17:17:07 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3230caa2d09664b149af201f96bfc1427f1653cce025261f57c9e3b7ed64e5a9`  
		Last Modified: Tue, 12 Dec 2023 17:17:07 GMT  
		Size: 826.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff809c5b6211826dea1c53467a3f87f30c04cf45e01143dc6b0ba468111d21fd`  
		Last Modified: Tue, 12 Dec 2023 17:17:08 GMT  
		Size: 1.8 MB (1845857 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d21acfe91bf2420a2944a717df0fc6d333e4156cd87a47dafc16efef65ea0aa`  
		Last Modified: Tue, 12 Dec 2023 17:17:08 GMT  
		Size: 491.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `logstash:7.17.15` - unknown; unknown

```console
$ docker pull logstash@sha256:d2ac33c9e63baaabd791afec042bd458b8061acf95b514fc07161c159074d137
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2705531 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:58d4b01b22da9a5c39fa75962f9f13385776288f3620be02d77ffe54eb03135a`

```dockerfile
```

-	Layers:
	-	`sha256:d5f24206c5b887931084b839ca21184d00a10f10f22fb3060a5ac25bee527bb1`  
		Last Modified: Tue, 12 Dec 2023 17:17:05 GMT  
		Size: 2.7 MB (2673362 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:93a64ac5dee0789f89fd31b5774aa21ad75052b36ad6969dae7c687c294255ad`  
		Last Modified: Tue, 12 Dec 2023 17:17:05 GMT  
		Size: 32.2 KB (32169 bytes)  
		MIME: application/vnd.in-toto+json

### `logstash:7.17.15` - linux; arm64 variant v8

```console
$ docker pull logstash@sha256:eeb46e0608a24df87ef113352d49b02a4615694de7fff19e95e02770acf0e2fb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **433.9 MB (433917214 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a2453987bbe2bc8b899628aa2d917848d80cab1d90782088f82bbae1812550b`
-	Entrypoint: `["\/usr\/local\/bin\/docker-entrypoint"]`

```dockerfile
# Mon, 13 Nov 2023 18:15:06 GMT
ARG RELEASE
# Mon, 13 Nov 2023 18:15:06 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 13 Nov 2023 18:15:06 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 13 Nov 2023 18:15:06 GMT
LABEL org.opencontainers.image.version=20.04
# Mon, 13 Nov 2023 18:15:06 GMT
ADD file:f80c582e6edb1f05fc0cefc201be3c47d4b4c6ceb20889c434c9fdef0291cbbf in / 
# Mon, 13 Nov 2023 18:15:06 GMT
CMD ["/bin/bash"]
# Mon, 13 Nov 2023 18:15:06 GMT
RUN for iter in {1..10}; do export DEBIAN_FRONTEND=noninteractive && apt-get update -y && apt-get upgrade -y && apt-get install -y procps findutils tar gzip curl && apt-get install -y locales && apt-get clean all && locale-gen 'en_US.UTF-8' &&     apt-get clean metadata && exit_code=0 && break || exit_code=$? &&     echo "packaging error: retry $iter in 10s" &&     apt-get clean all && apt-get clean metadata && sleep 10; done;     (exit $exit_code) # buildkit
# Mon, 13 Nov 2023 18:15:06 GMT
RUN groupadd --gid 1000 logstash &&     adduser --uid 1000 --gid 1000        --home /usr/share/logstash --no-create-home       logstash # buildkit
# Mon, 13 Nov 2023 18:15:06 GMT
RUN curl -Lo - https://artifacts.elastic.co/downloads/logstash/logstash-7.17.15-linux-$(arch).tar.gz |     tar zxf - -C /usr/share &&     mv /usr/share/logstash-7.17.15 /usr/share/logstash && chown --recursive logstash:logstash /usr/share/logstash/ &&     chown -R logstash:root /usr/share/logstash &&     chmod -R g=u /usr/share/logstash &&     mkdir /licenses/ &&     mv /usr/share/logstash/NOTICE.TXT /licenses/NOTICE.TXT &&     mv /usr/share/logstash/LICENSE.txt /licenses/LICENSE.txt &&     find /usr/share/logstash -type d -exec chmod g+s {} \; &&     ln -s /usr/share/logstash /opt/logstash # buildkit
# Mon, 13 Nov 2023 18:15:06 GMT
WORKDIR /usr/share/logstash
# Mon, 13 Nov 2023 18:15:06 GMT
ENV ELASTIC_CONTAINER=true
# Mon, 13 Nov 2023 18:15:06 GMT
ENV PATH=/usr/share/logstash/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 13 Nov 2023 18:15:06 GMT
ADD config/pipelines.yml config/pipelines.yml # buildkit
# Mon, 13 Nov 2023 18:15:06 GMT
ADD config/logstash-full.yml config/logstash.yml # buildkit
# Mon, 13 Nov 2023 18:15:06 GMT
ADD config/log4j2.properties config/ # buildkit
# Mon, 13 Nov 2023 18:15:06 GMT
ADD pipeline/default.conf pipeline/logstash.conf # buildkit
# Mon, 13 Nov 2023 18:15:06 GMT
RUN chown --recursive logstash:root config/ pipeline/ # buildkit
# Mon, 13 Nov 2023 18:15:06 GMT
ENV LANG=en_US.UTF-8 LC_ALL=en_US.UTF-8
# Mon, 13 Nov 2023 18:15:06 GMT
ADD env2yaml/env2yaml /usr/local/bin/ # buildkit
# Mon, 13 Nov 2023 18:15:06 GMT
ADD bin/docker-entrypoint /usr/local/bin/ # buildkit
# Mon, 13 Nov 2023 18:15:06 GMT
RUN chmod 0755 /usr/local/bin/docker-entrypoint # buildkit
# Mon, 13 Nov 2023 18:15:06 GMT
USER 1000
# Mon, 13 Nov 2023 18:15:06 GMT
EXPOSE map[5044/tcp:{} 9600/tcp:{}]
# Mon, 13 Nov 2023 18:15:06 GMT
LABEL org.label-schema.schema-version=1.0 org.label-schema.vendor=Elastic org.opencontainers.image.vendor=Elastic org.label-schema.name=logstash org.opencontainers.image.title=logstash org.label-schema.version=7.17.15 org.opencontainers.image.version=7.17.15 org.label-schema.url=https://www.elastic.co/products/logstash org.label-schema.vcs-url=https://github.com/elastic/logstash org.label-schema.license=Elastic License org.opencontainers.image.licenses=Elastic License org.opencontainers.image.description=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' org.label-schema.build-date=2023-10-10T17:45:59+00:00 org.opencontainers.image.created=2023-10-10T17:45:59+00:00
# Mon, 13 Nov 2023 18:15:06 GMT
ENTRYPOINT ["/usr/local/bin/docker-entrypoint"]
```

-	Layers:
	-	`sha256:dae58cbd668a05adbb25fa9970bfa041b807c2c537b86caa4ab74f77cfac02df`  
		Last Modified: Tue, 28 Nov 2023 05:37:25 GMT  
		Size: 26.0 MB (25975507 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:483023149b3e363410a4efa610382d9c1895c71ab225b1e3aeb1f58abbe3d12d`  
		Last Modified: Tue, 12 Dec 2023 17:43:18 GMT  
		Size: 42.5 MB (42496582 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97cb2de4e64897810ce7b16621b7ce7c9e83e9fcc5599d663460bc239058b036`  
		Last Modified: Tue, 12 Dec 2023 17:43:15 GMT  
		Size: 1.8 KB (1808 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:293f78e8902618b8ce6bd62966e1903860bf455d32a4389c821bbc08e509da00`  
		Last Modified: Tue, 12 Dec 2023 17:46:13 GMT  
		Size: 363.6 MB (363594680 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2628fc69cbf2a0e05d1e696c66696066c72f744427f15f9e5434df49ad60b38`  
		Last Modified: Tue, 12 Dec 2023 17:46:05 GMT  
		Size: 377.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb399562f35097db39a03a0a90bbc6ac0e96100bfc11c87181104c91923c7b4c`  
		Last Modified: Tue, 12 Dec 2023 17:46:05 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5f003285c261cc64895f32e98ad328691e47609777a033f7976d0cc88558512`  
		Last Modified: Tue, 12 Dec 2023 17:46:05 GMT  
		Size: 471.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:379bf41dcc66a9dce0a6681fca8fe6c1fdb8ab8e06425893b757cc85544e6c31`  
		Last Modified: Tue, 12 Dec 2023 17:46:06 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3cb7058fd586c2a4a11450b9065a62dea8ea7caaaa43d5e57f2cc92deeba7dd3`  
		Last Modified: Tue, 12 Dec 2023 17:46:07 GMT  
		Size: 827.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4bc92a58c8f4456cdd9c4960d9e4e4f97522d666b70ab87d6d5b9becdeb54b3`  
		Last Modified: Tue, 12 Dec 2023 17:46:07 GMT  
		Size: 1.8 MB (1845854 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3be4d252e408ee7007977c214a72375e096ae3a028d4deff2affe2920e2a9b97`  
		Last Modified: Tue, 12 Dec 2023 17:46:07 GMT  
		Size: 493.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `logstash:7.17.15` - unknown; unknown

```console
$ docker pull logstash@sha256:e37eac1d6f711a32cfa419ff4fdb84be30ad23c39b6703151836c2d1cd4982c6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2705702 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:94b18d21e48491f63847c4635dfde5f2ecf3864e53f21453000e5a5f75e3de2c`

```dockerfile
```

-	Layers:
	-	`sha256:ebebc9d27cc85f32ca3541037c6679e91d743642e8b178a84e239acd0fc906aa`  
		Last Modified: Tue, 12 Dec 2023 17:46:05 GMT  
		Size: 2.7 MB (2673690 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:107e8345a8e013fbf3267868995d911188bbfc8e9473672d8cce361af10bf7f5`  
		Last Modified: Tue, 12 Dec 2023 17:46:05 GMT  
		Size: 32.0 KB (32012 bytes)  
		MIME: application/vnd.in-toto+json

## `logstash:8.11.1`

```console
$ docker pull logstash@sha256:a4cac4a9042c1b198a0fefa767296d665528433b88bd2bcb6a4a5ab9e18da3ac
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `logstash:8.11.1` - linux; amd64

```console
$ docker pull logstash@sha256:74ed36547f4a8269253336673578c2f2a3239725417a211446e3ca4ad25e69f0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **432.9 MB (432937415 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b202614ea2945ab3aabab30755ce88db73271a7166c5d1038f9cf2b36fbdf4a`
-	Entrypoint: `["\/usr\/local\/bin\/docker-entrypoint"]`

```dockerfile
# Mon, 13 Nov 2023 14:50:42 GMT
ARG RELEASE
# Mon, 13 Nov 2023 14:50:42 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 13 Nov 2023 14:50:42 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 13 Nov 2023 14:50:42 GMT
LABEL org.opencontainers.image.version=20.04
# Mon, 13 Nov 2023 14:50:42 GMT
ADD file:9169bb1d6ef21313aed17e924538fee03d858460ae6b05e01968457dfc043bd7 in / 
# Mon, 13 Nov 2023 14:50:42 GMT
CMD ["/bin/bash"]
# Mon, 13 Nov 2023 14:50:42 GMT
RUN for iter in {1..10}; do export DEBIAN_FRONTEND=noninteractive && apt-get update -y && apt-get upgrade -y && apt-get install -y procps findutils tar gzip curl && apt-get install -y locales && apt-get clean all && locale-gen 'en_US.UTF-8' &&     apt-get clean metadata && exit_code=0 && break || exit_code=$? &&     echo "packaging error: retry $iter in 10s" &&     apt-get clean all && apt-get clean metadata && sleep 10; done;     (exit $exit_code) # buildkit
# Mon, 13 Nov 2023 14:50:42 GMT
RUN groupadd --gid 1000 logstash &&     adduser --uid 1000 --gid 1000        --home /usr/share/logstash --no-create-home       logstash # buildkit
# Mon, 13 Nov 2023 14:50:42 GMT
RUN curl -Lo - https://artifacts.elastic.co/downloads/logstash/logstash-8.11.1-linux-$(arch).tar.gz |     tar zxf - -C /usr/share &&     mv /usr/share/logstash-8.11.1 /usr/share/logstash && chown --recursive logstash:logstash /usr/share/logstash/ &&     chown -R logstash:root /usr/share/logstash &&     chmod -R g=u /usr/share/logstash &&     mkdir /licenses/ &&     mv /usr/share/logstash/NOTICE.TXT /licenses/NOTICE.TXT &&     mv /usr/share/logstash/LICENSE.txt /licenses/LICENSE.txt && find /usr/share/logstash -type d -exec chmod g+s {} \; && ln -s /usr/share/logstash /opt/logstash # buildkit
# Mon, 13 Nov 2023 14:50:42 GMT
WORKDIR /usr/share/logstash
# Mon, 13 Nov 2023 14:50:42 GMT
ENV ELASTIC_CONTAINER=true
# Mon, 13 Nov 2023 14:50:42 GMT
ENV PATH=/usr/share/logstash/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 13 Nov 2023 14:50:42 GMT
COPY config/pipelines.yml config/pipelines.yml # buildkit
# Mon, 13 Nov 2023 14:50:42 GMT
COPY config/logstash-full.yml config/logstash.yml # buildkit
# Mon, 13 Nov 2023 14:50:42 GMT
COPY config/log4j2.properties config/ # buildkit
# Mon, 13 Nov 2023 14:50:42 GMT
COPY config/log4j2.file.properties config/ # buildkit
# Mon, 13 Nov 2023 14:50:42 GMT
COPY pipeline/default.conf pipeline/logstash.conf # buildkit
# Mon, 13 Nov 2023 14:50:42 GMT
RUN chown --recursive logstash:root config/ pipeline/ # buildkit
# Mon, 13 Nov 2023 14:50:42 GMT
ENV LANG=en_US.UTF-8 LC_ALL=en_US.UTF-8
# Mon, 13 Nov 2023 14:50:42 GMT
COPY env2yaml/env2yaml /usr/local/bin/ # buildkit
# Mon, 13 Nov 2023 14:50:42 GMT
COPY bin/docker-entrypoint /usr/local/bin/ # buildkit
# Mon, 13 Nov 2023 14:50:42 GMT
RUN chmod 0755 /usr/local/bin/docker-entrypoint # buildkit
# Mon, 13 Nov 2023 14:50:42 GMT
USER 1000
# Mon, 13 Nov 2023 14:50:42 GMT
EXPOSE map[5044/tcp:{} 9600/tcp:{}]
# Mon, 13 Nov 2023 14:50:42 GMT
LABEL org.label-schema.schema-version=1.0 org.label-schema.vendor=Elastic org.opencontainers.image.vendor=Elastic org.label-schema.name=logstash org.opencontainers.image.title=logstash org.label-schema.version=8.11.1 org.opencontainers.image.version=8.11.1 org.label-schema.url=https://www.elastic.co/products/logstash org.label-schema.vcs-url=https://github.com/elastic/logstash org.label-schema.license=Elastic License org.opencontainers.image.licenses=Elastic License org.opencontainers.image.description=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' org.label-schema.build-date=2023-11-11T08:49:05+00:00 org.opencontainers.image.created=2023-11-11T08:49:05+00:00
# Mon, 13 Nov 2023 14:50:42 GMT
ENTRYPOINT ["/usr/local/bin/docker-entrypoint"]
```

-	Layers:
	-	`sha256:25ad149ed3cff49ddb57ceb4418377f63c897198de1f9de7a24506397822de3e`  
		Last Modified: Tue, 28 Nov 2023 05:37:19 GMT  
		Size: 27.5 MB (27512563 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2cdf5d52b72b83b3c423ea19a1dd01cba895b5ff817c05b00e8161e375db9d1e`  
		Last Modified: Tue, 12 Dec 2023 17:17:15 GMT  
		Size: 53.0 MB (53034658 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a409fb5da6fc15261740446e84cdd80422cd60f56531aaac58cbe7b466a412c5`  
		Last Modified: Tue, 12 Dec 2023 17:17:13 GMT  
		Size: 1.8 KB (1805 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ba87091c952403ff64e4f9ca9f8ae7c29bd9393d326b2ca7de045c9f3fa8338`  
		Last Modified: Tue, 12 Dec 2023 17:17:21 GMT  
		Size: 350.5 MB (350538118 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3aea8ff3d17bca668679b4b07c6e0db5ec1b7aab169d4e7e15c313a8938b3a33`  
		Last Modified: Tue, 12 Dec 2023 17:17:13 GMT  
		Size: 381.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f228565cecb1ba942753e88f98d4c0969ee7beae2c08826267a998343a76d53b`  
		Last Modified: Tue, 12 Dec 2023 17:17:14 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74cf874ab5e165da3273bb9a5310984834dd6265f1cad35fd384b8692659bcba`  
		Last Modified: Tue, 12 Dec 2023 17:17:14 GMT  
		Size: 475.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b539e549defa87cf88c2a012af7269768307c0df22c6131b66c3c3ae8d29e3ec`  
		Last Modified: Tue, 12 Dec 2023 17:17:15 GMT  
		Size: 1.4 KB (1363 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61f14b76145d9509ccd4d7295db1f6b49340d403912013d7b697432f2149f6df`  
		Last Modified: Tue, 12 Dec 2023 17:17:15 GMT  
		Size: 278.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5377cec80da8a1d69e06281f1ccf86abedc12e0971af98a03b24a34060e336ab`  
		Last Modified: Tue, 12 Dec 2023 17:17:16 GMT  
		Size: 1.8 KB (1764 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:918101a726e598a45946e4d42a5190670761ad799a3f5e592d16a2ee51839f30`  
		Last Modified: Tue, 12 Dec 2023 17:17:17 GMT  
		Size: 1.8 MB (1844955 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84707193a417fb6778ecdb0b2fa4b03f80ad2a2ec0d0c6a508aeb14fbc41695d`  
		Last Modified: Tue, 12 Dec 2023 17:17:16 GMT  
		Size: 712.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `logstash:8.11.1` - unknown; unknown

```console
$ docker pull logstash@sha256:e99d9673886aee315eda7b3bf21f29cb055a3ff2c52408c5e18f533f2d220c02
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2835715 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e7348356fb76de8a397bdd7ab472c41dcbabd9345d7219543d5217a815037e8b`

```dockerfile
```

-	Layers:
	-	`sha256:12c5cd7e23bc030169b3090b55e870b582f5fa3c160779325044c25480985711`  
		Last Modified: Tue, 12 Dec 2023 17:17:13 GMT  
		Size: 2.8 MB (2801016 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a3d63703d378e2c5a9773be32942b8c5d73c53e5c4fa93430d32b32efe0d483a`  
		Last Modified: Tue, 12 Dec 2023 17:17:13 GMT  
		Size: 34.7 KB (34699 bytes)  
		MIME: application/vnd.in-toto+json

### `logstash:8.11.1` - linux; arm64 variant v8

```console
$ docker pull logstash@sha256:763ee346e166c6c589b38c844f6b0b16815b02780c09889aa8a4cac7b2489130
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **419.7 MB (419674551 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b698a3bb9519af2d1dcc391ad13f3b1a835b35d93a7ee1f3b6586d13f170ecb4`
-	Entrypoint: `["\/usr\/local\/bin\/docker-entrypoint"]`

```dockerfile
# Mon, 13 Nov 2023 14:50:42 GMT
ARG RELEASE
# Mon, 13 Nov 2023 14:50:42 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 13 Nov 2023 14:50:42 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 13 Nov 2023 14:50:42 GMT
LABEL org.opencontainers.image.version=20.04
# Mon, 13 Nov 2023 14:50:42 GMT
ADD file:f80c582e6edb1f05fc0cefc201be3c47d4b4c6ceb20889c434c9fdef0291cbbf in / 
# Mon, 13 Nov 2023 14:50:42 GMT
CMD ["/bin/bash"]
# Mon, 13 Nov 2023 14:50:42 GMT
RUN for iter in {1..10}; do export DEBIAN_FRONTEND=noninteractive && apt-get update -y && apt-get upgrade -y && apt-get install -y procps findutils tar gzip curl && apt-get install -y locales && apt-get clean all && locale-gen 'en_US.UTF-8' &&     apt-get clean metadata && exit_code=0 && break || exit_code=$? &&     echo "packaging error: retry $iter in 10s" &&     apt-get clean all && apt-get clean metadata && sleep 10; done;     (exit $exit_code) # buildkit
# Mon, 13 Nov 2023 14:50:42 GMT
RUN groupadd --gid 1000 logstash &&     adduser --uid 1000 --gid 1000        --home /usr/share/logstash --no-create-home       logstash # buildkit
# Mon, 13 Nov 2023 14:50:42 GMT
RUN curl -Lo - https://artifacts.elastic.co/downloads/logstash/logstash-8.11.1-linux-$(arch).tar.gz |     tar zxf - -C /usr/share &&     mv /usr/share/logstash-8.11.1 /usr/share/logstash && chown --recursive logstash:logstash /usr/share/logstash/ &&     chown -R logstash:root /usr/share/logstash &&     chmod -R g=u /usr/share/logstash &&     mkdir /licenses/ &&     mv /usr/share/logstash/NOTICE.TXT /licenses/NOTICE.TXT &&     mv /usr/share/logstash/LICENSE.txt /licenses/LICENSE.txt && find /usr/share/logstash -type d -exec chmod g+s {} \; && ln -s /usr/share/logstash /opt/logstash # buildkit
# Mon, 13 Nov 2023 14:50:42 GMT
WORKDIR /usr/share/logstash
# Mon, 13 Nov 2023 14:50:42 GMT
ENV ELASTIC_CONTAINER=true
# Mon, 13 Nov 2023 14:50:42 GMT
ENV PATH=/usr/share/logstash/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 13 Nov 2023 14:50:42 GMT
COPY config/pipelines.yml config/pipelines.yml # buildkit
# Mon, 13 Nov 2023 14:50:42 GMT
COPY config/logstash-full.yml config/logstash.yml # buildkit
# Mon, 13 Nov 2023 14:50:42 GMT
COPY config/log4j2.properties config/ # buildkit
# Mon, 13 Nov 2023 14:50:42 GMT
COPY config/log4j2.file.properties config/ # buildkit
# Mon, 13 Nov 2023 14:50:42 GMT
COPY pipeline/default.conf pipeline/logstash.conf # buildkit
# Mon, 13 Nov 2023 14:50:42 GMT
RUN chown --recursive logstash:root config/ pipeline/ # buildkit
# Mon, 13 Nov 2023 14:50:42 GMT
ENV LANG=en_US.UTF-8 LC_ALL=en_US.UTF-8
# Mon, 13 Nov 2023 14:50:42 GMT
COPY env2yaml/env2yaml /usr/local/bin/ # buildkit
# Mon, 13 Nov 2023 14:50:42 GMT
COPY bin/docker-entrypoint /usr/local/bin/ # buildkit
# Mon, 13 Nov 2023 14:50:42 GMT
RUN chmod 0755 /usr/local/bin/docker-entrypoint # buildkit
# Mon, 13 Nov 2023 14:50:42 GMT
USER 1000
# Mon, 13 Nov 2023 14:50:42 GMT
EXPOSE map[5044/tcp:{} 9600/tcp:{}]
# Mon, 13 Nov 2023 14:50:42 GMT
LABEL org.label-schema.schema-version=1.0 org.label-schema.vendor=Elastic org.opencontainers.image.vendor=Elastic org.label-schema.name=logstash org.opencontainers.image.title=logstash org.label-schema.version=8.11.1 org.opencontainers.image.version=8.11.1 org.label-schema.url=https://www.elastic.co/products/logstash org.label-schema.vcs-url=https://github.com/elastic/logstash org.label-schema.license=Elastic License org.opencontainers.image.licenses=Elastic License org.opencontainers.image.description=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' org.label-schema.build-date=2023-11-11T08:49:05+00:00 org.opencontainers.image.created=2023-11-11T08:49:05+00:00
# Mon, 13 Nov 2023 14:50:42 GMT
ENTRYPOINT ["/usr/local/bin/docker-entrypoint"]
```

-	Layers:
	-	`sha256:dae58cbd668a05adbb25fa9970bfa041b807c2c537b86caa4ab74f77cfac02df`  
		Last Modified: Tue, 28 Nov 2023 05:37:25 GMT  
		Size: 26.0 MB (25975507 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:483023149b3e363410a4efa610382d9c1895c71ab225b1e3aeb1f58abbe3d12d`  
		Last Modified: Tue, 12 Dec 2023 17:43:18 GMT  
		Size: 42.5 MB (42496582 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97cb2de4e64897810ce7b16621b7ce7c9e83e9fcc5599d663460bc239058b036`  
		Last Modified: Tue, 12 Dec 2023 17:43:15 GMT  
		Size: 1.8 KB (1808 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:417519c0bcb31805bec0a4b7e7fb61cf71d64f92d01b38ef8aa0c652c7a60886`  
		Last Modified: Tue, 12 Dec 2023 17:43:27 GMT  
		Size: 349.4 MB (349350395 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b5166f1d478453abe3f67259b84550b1b01e8531ac27d78e884ecc1683d3b7b`  
		Last Modified: Tue, 12 Dec 2023 17:43:15 GMT  
		Size: 377.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:337c899da713f726a82c4bd500cdd2d7beb303f96841204c29727a9c82dd3934`  
		Last Modified: Tue, 12 Dec 2023 17:43:16 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c0019e32ea99636fdf0550d89e46d801507dd6e6683e769719e0ca0a96ff4ba`  
		Last Modified: Tue, 12 Dec 2023 17:43:17 GMT  
		Size: 470.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e812737bed35a18ecc928f98cb4deeb4b72d91eb9d3c0741f8e25caf62564f4a`  
		Last Modified: Tue, 12 Dec 2023 17:43:18 GMT  
		Size: 1.4 KB (1359 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8506b838dac5423edc8cbfc0e8ef0cfce22cdaf92dfa1012d66e8dd964a410b`  
		Last Modified: Tue, 12 Dec 2023 17:43:18 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2e5fd89175b95926b58abdc8577354f84271ab0bde65eea84d4744cee57c550`  
		Last Modified: Tue, 12 Dec 2023 17:43:19 GMT  
		Size: 1.8 KB (1766 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a650ad677ae81e25aa29f6ffcd3b58b32851007403e1352731e8d1b7887a241d`  
		Last Modified: Tue, 12 Dec 2023 17:43:19 GMT  
		Size: 1.8 MB (1844957 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c08fffe5e77d3a63b5bda84f30d5367260ae5a1cf9bfd71af83db682375c0f31`  
		Last Modified: Tue, 12 Dec 2023 17:43:20 GMT  
		Size: 713.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `logstash:8.11.1` - unknown; unknown

```console
$ docker pull logstash@sha256:3995457a827e7b438dd3b2399c854422b93cf1dbab5aa3a2316a1f1edcb9a8da
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2835889 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a1cf6a463bba9da33767050214515cba84a7ae45703ae54bd4a9a93f357a9e9a`

```dockerfile
```

-	Layers:
	-	`sha256:b9d6d5a4a242f9e9ce94706953a9a2f60a5c412af59b2108c55a91a6e1dcb8ab`  
		Last Modified: Tue, 12 Dec 2023 17:43:16 GMT  
		Size: 2.8 MB (2801349 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8fc8d188cad391dac275d337ae191cc21ddd9d6a56233057b98a3a2f27236de1`  
		Last Modified: Tue, 12 Dec 2023 17:43:15 GMT  
		Size: 34.5 KB (34540 bytes)  
		MIME: application/vnd.in-toto+json
