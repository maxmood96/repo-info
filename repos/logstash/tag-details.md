<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `logstash`

-	[`logstash:7.17.23`](#logstash71723)
-	[`logstash:8.15.0`](#logstash8150)

## `logstash:7.17.23`

```console
$ docker pull logstash@sha256:f439f4be3b2f375908c5aef6ffa0cc19f29343fb0a9b393230ecb593af0b37cc
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `logstash:7.17.23` - linux; amd64

```console
$ docker pull logstash@sha256:e21f50b92a7bc68fb4a133378a21314f55003c65b47b99330471aee96b61ee01
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **449.2 MB (449249897 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:167d07a2a70cc4223758a5ebb3c96c15dd8959e0c9f062dd871dfaeae395e15c`
-	Entrypoint: `["\/usr\/local\/bin\/docker-entrypoint"]`

```dockerfile
# Mon, 03 Jun 2024 17:10:41 GMT
ARG RELEASE
# Mon, 03 Jun 2024 17:10:41 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 03 Jun 2024 17:10:41 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 03 Jun 2024 17:10:41 GMT
LABEL org.opencontainers.image.version=20.04
# Mon, 03 Jun 2024 17:10:43 GMT
ADD file:e7cff353f027ecf0a2cb1cdd51714de3b083a11a0d965f104489f9a7e6925056 in / 
# Mon, 03 Jun 2024 17:10:43 GMT
CMD ["/bin/bash"]
# Tue, 30 Jul 2024 15:39:57 GMT
RUN for iter in {1..10}; do     export DEBIAN_FRONTEND=noninteractive &&     apt-get update -y &&     apt-get upgrade -y &&     apt-get install -y procps findutils tar gzip curl &&     apt-get install -y locales &&     apt-get clean all &&     locale-gen 'en_US.UTF-8' &&     apt-get clean metadata &&     exit_code=0 && break || exit_code=$? &&     echo "packaging error: retry $iter in 10s" &&     apt-get clean all &&     apt-get clean metadata &&     sleep 10; done;     (exit $exit_code) # buildkit
# Tue, 30 Jul 2024 15:39:57 GMT
RUN groupadd --gid 1000 logstash &&     adduser --uid 1000 --gid 1000     --home /usr/share/logstash --no-create-home     logstash # buildkit
# Tue, 30 Jul 2024 15:39:57 GMT
RUN curl -Lo - https://artifacts.elastic.co/downloads/logstash/logstash-7.17.23-linux-$(arch).tar.gz |     tar zxf - -C /usr/share &&     mv /usr/share/logstash-7.17.23 /usr/share/logstash &&     chown --recursive logstash:logstash /usr/share/logstash/ &&     chown -R logstash:root /usr/share/logstash &&     chmod -R g=u /usr/share/logstash &&     mkdir /licenses/ &&     mv /usr/share/logstash/NOTICE.TXT /licenses/NOTICE.TXT &&     mv /usr/share/logstash/LICENSE.txt /licenses/LICENSE.txt &&     find /usr/share/logstash -type d -exec chmod g+s {} \; &&     ln -s /usr/share/logstash /opt/logstash # buildkit
# Tue, 30 Jul 2024 15:39:57 GMT
WORKDIR /usr/share/logstash
# Tue, 30 Jul 2024 15:39:57 GMT
ENV ELASTIC_CONTAINER=true
# Tue, 30 Jul 2024 15:39:57 GMT
ENV PATH=/usr/share/logstash/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 30 Jul 2024 15:39:57 GMT
COPY config/pipelines.yml config/pipelines.yml # buildkit
# Tue, 30 Jul 2024 15:39:57 GMT
COPY config/logstash-full.yml config/logstash.yml # buildkit
# Tue, 30 Jul 2024 15:39:57 GMT
COPY config/log4j2.properties config/ # buildkit
# Tue, 30 Jul 2024 15:39:57 GMT
COPY pipeline/default.conf pipeline/logstash.conf # buildkit
# Tue, 30 Jul 2024 15:39:57 GMT
RUN chown --recursive logstash:root config/ pipeline/ # buildkit
# Tue, 30 Jul 2024 15:39:57 GMT
ENV LANG=en_US.UTF-8 LC_ALL=en_US.UTF-8
# Tue, 30 Jul 2024 15:39:57 GMT
COPY env2yaml/env2yaml /usr/local/bin/ # buildkit
# Tue, 30 Jul 2024 15:39:57 GMT
COPY bin/docker-entrypoint /usr/local/bin/ # buildkit
# Tue, 30 Jul 2024 15:39:57 GMT
RUN chmod 0755 /usr/local/bin/docker-entrypoint # buildkit
# Tue, 30 Jul 2024 15:39:57 GMT
USER 1000
# Tue, 30 Jul 2024 15:39:57 GMT
EXPOSE map[5044/tcp:{} 9600/tcp:{}]
# Tue, 30 Jul 2024 15:39:57 GMT
LABEL org.label-schema.schema-version=1.0 org.label-schema.vendor=Elastic org.opencontainers.image.vendor=Elastic org.label-schema.name=logstash org.opencontainers.image.title=logstash org.label-schema.version=7.17.23 org.opencontainers.image.version=7.17.23 org.label-schema.url=https://www.elastic.co/products/logstash org.label-schema.vcs-url=https://github.com/elastic/logstash org.label-schema.license=Elastic License org.opencontainers.image.licenses=Elastic License org.opencontainers.image.description=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' org.label-schema.build-date=2024-07-23T07:27:01+00:00 org.opencontainers.image.created=2024-07-23T07:27:01+00:00
# Tue, 30 Jul 2024 15:39:57 GMT
ENTRYPOINT ["/usr/local/bin/docker-entrypoint"]
```

-	Layers:
	-	`sha256:9ea8908f47652b59b8055316d9c0e16b365e2b5cee15d3efcb79e2957e3e7cad`  
		Last Modified: Mon, 03 Jun 2024 17:19:42 GMT  
		Size: 27.5 MB (27511769 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9cc3a5c7e3ae657f87760909357ff7ae9ffc5004b5f36aee8cfb2ae02d79dda`  
		Last Modified: Tue, 30 Jul 2024 23:56:18 GMT  
		Size: 49.1 MB (49102713 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d502749c4144882b325d8a4268ed77bb4171876fb32e393abe78fef7ea80554`  
		Last Modified: Tue, 30 Jul 2024 23:56:17 GMT  
		Size: 1.8 KB (1807 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9450f78f86387ebf5808678a6e950d6bbe145538e328f2a75c2a79e067d1a4c8`  
		Last Modified: Tue, 30 Jul 2024 23:56:22 GMT  
		Size: 370.7 MB (370728140 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32b65e227e453760107f3b760c25b7001270a11eaaafc06549b82dc79910ca7e`  
		Last Modified: Tue, 30 Jul 2024 23:56:17 GMT  
		Size: 377.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb92ed51f16e82fc49431cba280e870d3d41c5d55e043740ca40faa3bf2f3239`  
		Last Modified: Tue, 30 Jul 2024 23:56:18 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dce18aa72f75dcdae5fd9c524366970a6cfb0bf139dbe31524c5419f388570ea`  
		Last Modified: Tue, 30 Jul 2024 23:56:18 GMT  
		Size: 471.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd6a8260e351d3944b98dbd8af525a9f60b26f8a6ac5d3f4d2eb7f8d8a7a9e4e`  
		Last Modified: Tue, 30 Jul 2024 23:56:19 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47e0784aa21575d7217aec2509869a38c92b3ceef8f35ee154ae7d96f34d5dd4`  
		Last Modified: Tue, 30 Jul 2024 23:56:19 GMT  
		Size: 828.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54dce8afdbed24e46b144553b59d7e00865835789dfdc1ac05e1bec072d8f207`  
		Last Modified: Tue, 30 Jul 2024 23:56:19 GMT  
		Size: 1.9 MB (1902684 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:542d4b9dec35707b84164286b04cdd872f30d90002044ad720f0fc97e1e5845c`  
		Last Modified: Tue, 30 Jul 2024 23:56:19 GMT  
		Size: 492.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `logstash:7.17.23` - unknown; unknown

```console
$ docker pull logstash@sha256:352cecd9349c83014a932191b2deabd00d7dafc60034611e1d6ada518a2aa7ef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3100668 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc9b7f531a0081510f975a182da60547a90ed4807f5f9886fec5fc6ebd2e1da0`

```dockerfile
```

-	Layers:
	-	`sha256:3de537640efdb1e893d967c7527e5d3c667f173d158b68172e78395533dd8329`  
		Last Modified: Tue, 30 Jul 2024 23:56:17 GMT  
		Size: 3.1 MB (3068736 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2dd94304e4339199083b4f6e4a24ff3fca6b2afbd3c74a1f07014d3a20066b03`  
		Last Modified: Tue, 30 Jul 2024 23:56:17 GMT  
		Size: 31.9 KB (31932 bytes)  
		MIME: application/vnd.in-toto+json

### `logstash:7.17.23` - linux; arm64 variant v8

```console
$ docker pull logstash@sha256:156a36242194242d3f8c4550662afd6ec7a8f7657ee16d3c5ca2ceb34097174c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **433.3 MB (433297459 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e5213e31f292ae5dde8a1ac2452f369d152c622a178a52d21641a97c90b3be84`
-	Entrypoint: `["\/usr\/local\/bin\/docker-entrypoint"]`

```dockerfile
# Mon, 03 Jun 2024 16:52:57 GMT
ARG RELEASE
# Mon, 03 Jun 2024 16:52:57 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 03 Jun 2024 16:52:57 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 03 Jun 2024 16:52:57 GMT
LABEL org.opencontainers.image.version=20.04
# Mon, 03 Jun 2024 16:52:59 GMT
ADD file:6d8cc056ee741f09a6c7d965d8e2027d80ed2eccbfb0312593ce52d9256db437 in / 
# Mon, 03 Jun 2024 16:52:59 GMT
CMD ["/bin/bash"]
# Tue, 30 Jul 2024 15:39:57 GMT
RUN for iter in {1..10}; do     export DEBIAN_FRONTEND=noninteractive &&     apt-get update -y &&     apt-get upgrade -y &&     apt-get install -y procps findutils tar gzip curl &&     apt-get install -y locales &&     apt-get clean all &&     locale-gen 'en_US.UTF-8' &&     apt-get clean metadata &&     exit_code=0 && break || exit_code=$? &&     echo "packaging error: retry $iter in 10s" &&     apt-get clean all &&     apt-get clean metadata &&     sleep 10; done;     (exit $exit_code) # buildkit
# Tue, 30 Jul 2024 15:39:57 GMT
RUN groupadd --gid 1000 logstash &&     adduser --uid 1000 --gid 1000     --home /usr/share/logstash --no-create-home     logstash # buildkit
# Tue, 30 Jul 2024 15:39:57 GMT
RUN curl -Lo - https://artifacts.elastic.co/downloads/logstash/logstash-7.17.23-linux-$(arch).tar.gz |     tar zxf - -C /usr/share &&     mv /usr/share/logstash-7.17.23 /usr/share/logstash &&     chown --recursive logstash:logstash /usr/share/logstash/ &&     chown -R logstash:root /usr/share/logstash &&     chmod -R g=u /usr/share/logstash &&     mkdir /licenses/ &&     mv /usr/share/logstash/NOTICE.TXT /licenses/NOTICE.TXT &&     mv /usr/share/logstash/LICENSE.txt /licenses/LICENSE.txt &&     find /usr/share/logstash -type d -exec chmod g+s {} \; &&     ln -s /usr/share/logstash /opt/logstash # buildkit
# Tue, 30 Jul 2024 15:39:57 GMT
WORKDIR /usr/share/logstash
# Tue, 30 Jul 2024 15:39:57 GMT
ENV ELASTIC_CONTAINER=true
# Tue, 30 Jul 2024 15:39:57 GMT
ENV PATH=/usr/share/logstash/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 30 Jul 2024 15:39:57 GMT
COPY config/pipelines.yml config/pipelines.yml # buildkit
# Tue, 30 Jul 2024 15:39:57 GMT
COPY config/logstash-full.yml config/logstash.yml # buildkit
# Tue, 30 Jul 2024 15:39:57 GMT
COPY config/log4j2.properties config/ # buildkit
# Tue, 30 Jul 2024 15:39:57 GMT
COPY pipeline/default.conf pipeline/logstash.conf # buildkit
# Tue, 30 Jul 2024 15:39:57 GMT
RUN chown --recursive logstash:root config/ pipeline/ # buildkit
# Tue, 30 Jul 2024 15:39:57 GMT
ENV LANG=en_US.UTF-8 LC_ALL=en_US.UTF-8
# Tue, 30 Jul 2024 15:39:57 GMT
COPY env2yaml/env2yaml /usr/local/bin/ # buildkit
# Tue, 30 Jul 2024 15:39:57 GMT
COPY bin/docker-entrypoint /usr/local/bin/ # buildkit
# Tue, 30 Jul 2024 15:39:57 GMT
RUN chmod 0755 /usr/local/bin/docker-entrypoint # buildkit
# Tue, 30 Jul 2024 15:39:57 GMT
USER 1000
# Tue, 30 Jul 2024 15:39:57 GMT
EXPOSE map[5044/tcp:{} 9600/tcp:{}]
# Tue, 30 Jul 2024 15:39:57 GMT
LABEL org.label-schema.schema-version=1.0 org.label-schema.vendor=Elastic org.opencontainers.image.vendor=Elastic org.label-schema.name=logstash org.opencontainers.image.title=logstash org.label-schema.version=7.17.23 org.opencontainers.image.version=7.17.23 org.label-schema.url=https://www.elastic.co/products/logstash org.label-schema.vcs-url=https://github.com/elastic/logstash org.label-schema.license=Elastic License org.opencontainers.image.licenses=Elastic License org.opencontainers.image.description=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' org.label-schema.build-date=2024-07-23T07:27:01+00:00 org.opencontainers.image.created=2024-07-23T07:27:01+00:00
# Tue, 30 Jul 2024 15:39:57 GMT
ENTRYPOINT ["/usr/local/bin/docker-entrypoint"]
```

-	Layers:
	-	`sha256:f02209be4ee528c246399de81af4552e52adb005a8a499815607b6b0d42746bf`  
		Last Modified: Mon, 03 Jun 2024 17:19:48 GMT  
		Size: 26.0 MB (25974217 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ef091fc202eedefa169830decc3f8f914ec3cf27daaeac0afdbf156cec11759`  
		Last Modified: Wed, 31 Jul 2024 00:03:49 GMT  
		Size: 38.0 MB (37953274 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0987672485fbb34c03c26153bb9be52e9831d04cf13625e9f2776af3d68fae29`  
		Last Modified: Wed, 31 Jul 2024 00:03:48 GMT  
		Size: 1.8 KB (1812 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee6356fc18750a1cf4236d4da012ad00e47e9d4f2c47e5dc997bff894bf074c1`  
		Last Modified: Wed, 31 Jul 2024 00:03:55 GMT  
		Size: 367.5 MB (367462681 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6cf46cfcf621e29ac293ff239b4eb8c8e4cb03480b2d74d3c3f71fc92ae98be3`  
		Last Modified: Wed, 31 Jul 2024 00:03:48 GMT  
		Size: 378.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b60ab2b5b4a7e12aef13e03ed56d11205410c0c5811701f6bb66b5efdf17f3c`  
		Last Modified: Wed, 31 Jul 2024 00:03:49 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e5b9559202ab25fc3df3e79336a8cc59ed06b7645b5eeaf796846adf60ceace`  
		Last Modified: Wed, 31 Jul 2024 00:03:49 GMT  
		Size: 472.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff4f9d243d8266ca1a022a8b86e9dbed0bd3f0e94791a7ef11938316b3278dd3`  
		Last Modified: Wed, 31 Jul 2024 00:03:50 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b47396cd8899ac2e04f05718c5bf1319693a215cb715b5dc4520637b483be3d3`  
		Last Modified: Wed, 31 Jul 2024 00:03:50 GMT  
		Size: 827.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64f275967e8d18f99e2a30096925454c686938152550b24c54599de66dde2b08`  
		Last Modified: Wed, 31 Jul 2024 00:03:51 GMT  
		Size: 1.9 MB (1902685 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d117c82226b44bd9de5b4dcc9aad444d619759b6efb12d79fe0c57981b791c1e`  
		Last Modified: Wed, 31 Jul 2024 00:03:51 GMT  
		Size: 493.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `logstash:7.17.23` - unknown; unknown

```console
$ docker pull logstash@sha256:a5e6fccf170a6f6fd82e204ac9733b668dca33b0077bfa926d29dee17cc0e6db
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3101168 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5fa0e129c625084c07feda94fb23ec9cacaf99898c071f5784fd6c875f10903a`

```dockerfile
```

-	Layers:
	-	`sha256:a861f701bc12c25d308a68ea22677a0b530483423ae9a0437f6984d18308d06b`  
		Last Modified: Wed, 31 Jul 2024 00:03:48 GMT  
		Size: 3.1 MB (3068971 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:361bf9e7e70122bc875e94ea63df003976154b7e8eaf059b2d52315ba1d8c26a`  
		Last Modified: Wed, 31 Jul 2024 00:03:48 GMT  
		Size: 32.2 KB (32197 bytes)  
		MIME: application/vnd.in-toto+json

## `logstash:8.15.0`

```console
$ docker pull logstash@sha256:1704102d8c31416bd6d1527add326c9fa154d948b11c27033b1e128ae36e01f4
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `logstash:8.15.0` - linux; amd64

```console
$ docker pull logstash@sha256:f6f9e060524403f285944c2a93acdfe2b04e10528d51ac116dc72643ffa8b2cc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **504.3 MB (504272536 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f538e208fde939e34b2b43d9ae26da00accd4db39f6129c99ee77c6afc5fecee`
-	Entrypoint: `["\/usr\/local\/bin\/docker-entrypoint"]`

```dockerfile
# Mon, 03 Jun 2024 17:10:41 GMT
ARG RELEASE
# Mon, 03 Jun 2024 17:10:41 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 03 Jun 2024 17:10:41 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 03 Jun 2024 17:10:41 GMT
LABEL org.opencontainers.image.version=20.04
# Mon, 03 Jun 2024 17:10:43 GMT
ADD file:e7cff353f027ecf0a2cb1cdd51714de3b083a11a0d965f104489f9a7e6925056 in / 
# Mon, 03 Jun 2024 17:10:43 GMT
CMD ["/bin/bash"]
# Thu, 08 Aug 2024 13:05:51 GMT
RUN for iter in {1..10}; do       export DEBIAN_FRONTEND=noninteractive &&     apt-get update -y &&   apt-get upgrade -y &&   apt-get install -y procps findutils tar gzip &&         apt-get install -y locales &&         apt-get install -y curl &&     apt-get clean all &&       locale-gen 'en_US.UTF-8' &&     apt-get clean metadata &&   exit_code=0 && break || exit_code=$? && echo "packaging error: retry $iter in 10s" && apt-get clean all &&   apt-get clean metadata && sleep 10; done; (exit $exit_code) # buildkit
# Thu, 08 Aug 2024 13:05:51 GMT
RUN groupadd --gid 1000 logstash &&   adduser --uid 1000 --gid 1000 --home /usr/share/logstash --no-create-home logstash # buildkit
# Thu, 08 Aug 2024 13:05:51 GMT
RUN curl -Lo - https://artifacts.elastic.co/downloads/logstash/logstash-8.15.0-linux-$(arch).tar.gz |   tar zxf - -C /usr/share &&   mv /usr/share/logstash-8.15.0 /usr/share/logstash &&   chown --recursive logstash:logstash /usr/share/logstash/ &&   chown -R logstash:root /usr/share/logstash &&   chmod -R g=u /usr/share/logstash &&   mkdir /licenses/ &&   mv /usr/share/logstash/NOTICE.TXT /licenses/NOTICE.TXT &&   mv /usr/share/logstash/LICENSE.txt /licenses/LICENSE.txt &&   find /usr/share/logstash -type d -exec chmod g+s {} \; &&   ln -s /usr/share/logstash /opt/logstash # buildkit
# Thu, 08 Aug 2024 13:05:51 GMT
WORKDIR /usr/share/logstash
# Thu, 08 Aug 2024 13:05:51 GMT
ENV ELASTIC_CONTAINER=true
# Thu, 08 Aug 2024 13:05:51 GMT
ENV PATH=/usr/share/logstash/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 08 Aug 2024 13:05:51 GMT
COPY config/logstash-full.yml config/logstash.yml # buildkit
# Thu, 08 Aug 2024 13:05:51 GMT
COPY config/pipelines.yml config/log4j2.properties config/log4j2.file.properties config/ # buildkit
# Thu, 08 Aug 2024 13:05:51 GMT
COPY pipeline/default.conf pipeline/logstash.conf # buildkit
# Thu, 08 Aug 2024 13:05:51 GMT
RUN chown --recursive logstash:root config/ pipeline/ # buildkit
# Thu, 08 Aug 2024 13:05:51 GMT
ENV LANG=en_US.UTF-8 LC_ALL=en_US.UTF-8
# Thu, 08 Aug 2024 13:05:51 GMT
COPY env2yaml/env2yaml-amd64 env2yaml/env2yaml-arm64 env2yaml/ # buildkit
# Thu, 08 Aug 2024 13:05:51 GMT
RUN env2yamlarch="$(dpkg --print-architecture)";   case "${env2yamlarch}" in     'x86_64'|'amd64')       env2yamlarch=amd64;       ;;     'aarch64'|'arm64')       env2yamlarch=arm64;       ;;     *) echo >&2 "error: unsupported architecture '$env2yamlarch'"; exit 1 ;;   esac;   mkdir -p /usr/local/bin;   cp env2yaml/env2yaml-${env2yamlarch} /usr/local/bin/env2yaml;   rm -rf env2yaml # buildkit
# Thu, 08 Aug 2024 13:05:51 GMT
COPY bin/docker-entrypoint /usr/local/bin/ # buildkit
# Thu, 08 Aug 2024 13:05:51 GMT
RUN chmod 0755 /usr/local/bin/docker-entrypoint # buildkit
# Thu, 08 Aug 2024 13:05:51 GMT
USER 1000
# Thu, 08 Aug 2024 13:05:51 GMT
EXPOSE map[5044/tcp:{} 9600/tcp:{}]
# Thu, 08 Aug 2024 13:05:51 GMT
LABEL org.label-schema.schema-version=1.0 org.label-schema.vendor=Elastic org.opencontainers.image.vendor=Elastic org.label-schema.name=logstash org.opencontainers.image.title=logstash org.label-schema.version=8.15.0 org.opencontainers.image.version=8.15.0 org.label-schema.url=https://www.elastic.co/products/logstash org.label-schema.vcs-url=https://github.com/elastic/logstash org.label-schema.license=Elastic License org.opencontainers.image.licenses=Elastic License org.opencontainers.image.description=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' org.label-schema.build-date=2024-07-24T10:13:18+00:00 org.opencontainers.image.created=2024-07-24T10:13:18+00:00
# Thu, 08 Aug 2024 13:05:51 GMT
ENTRYPOINT ["/usr/local/bin/docker-entrypoint"]
```

-	Layers:
	-	`sha256:9ea8908f47652b59b8055316d9c0e16b365e2b5cee15d3efcb79e2957e3e7cad`  
		Last Modified: Mon, 03 Jun 2024 17:19:42 GMT  
		Size: 27.5 MB (27511769 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:820b787001289a592495ac01a6d9282879cf87c7ca4861832a638b0839661561`  
		Last Modified: Thu, 08 Aug 2024 22:57:18 GMT  
		Size: 49.2 MB (49235075 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95dadfcb3dff50c3fe440cc0d1f01f2bdb481781d3f91d43464a5335be63e859`  
		Last Modified: Thu, 08 Aug 2024 22:57:18 GMT  
		Size: 1.8 KB (1803 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a950f285602fcf494a49e593b6a0d288254f66a35d9c5dddaf7fc23cbef200ae`  
		Last Modified: Thu, 08 Aug 2024 22:57:24 GMT  
		Size: 421.9 MB (421926523 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:346f11da1b5fd7d481a0dd1bf02f8925dcf4276cc0883f9de264a4bcfb2e70e2`  
		Last Modified: Thu, 08 Aug 2024 22:57:18 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b5d9fa45d525cecc1de8e6fc3d724f044d48aad94dec7f8787a822d66feded9`  
		Last Modified: Thu, 08 Aug 2024 22:57:18 GMT  
		Size: 1.6 KB (1580 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7596075fcf83d34ab37b53e5f36388a1880e9f098642359ce7407f20e14e9bad`  
		Last Modified: Thu, 08 Aug 2024 22:57:18 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25942f4344f857835e69622d7ff1f06a09f8731d8797ac9bbcda1f055a3bb0cd`  
		Last Modified: Thu, 08 Aug 2024 22:57:19 GMT  
		Size: 1.8 KB (1771 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab7af6158e2ec1c24a98e90252b7dec108f0e17c156ee8afaa306db5707a8a91`  
		Last Modified: Thu, 08 Aug 2024 22:57:19 GMT  
		Size: 3.7 MB (3690579 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4b06aff4cd69ffce4628b8c3f9d119255b9c6fd564f359eee265c0da09ff115`  
		Last Modified: Thu, 08 Aug 2024 22:57:20 GMT  
		Size: 1.9 MB (1902102 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eaa3233c2f18f706dfc6318f1a6ea28fa86b77a8143ef7a87bce485a90fa8cfd`  
		Last Modified: Thu, 08 Aug 2024 22:57:20 GMT  
		Size: 714.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `logstash:8.15.0` - unknown; unknown

```console
$ docker pull logstash@sha256:9b6216bf936dd668c9de8b5b6ea9eeed234d359b6b7325e410f4b48a4915609e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3273110 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca3d35693145534990d5e987dbbc479136bb9d91388084d774c5d15eadb1df08`

```dockerfile
```

-	Layers:
	-	`sha256:3f592cea4cc9521178847ceb2dcfb2bd488031720db77c6ffc227cf053c15417`  
		Last Modified: Thu, 08 Aug 2024 22:57:18 GMT  
		Size: 3.2 MB (3238794 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:aba98b881faa51ffc384d20f5033716621f643e934c9fc827cb1e1a44aa6ff23`  
		Last Modified: Thu, 08 Aug 2024 22:57:18 GMT  
		Size: 34.3 KB (34316 bytes)  
		MIME: application/vnd.in-toto+json

### `logstash:8.15.0` - linux; arm64 variant v8

```console
$ docker pull logstash@sha256:f8111591be74f081a03dc6ec05eb5c84de71a4143ccbc363122bc02dcb9c4a12
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **489.6 MB (489566975 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:58f1821f98b82d2fe4ef3b30ba26633c27ad80ade0944c0670c28780260c9e34`
-	Entrypoint: `["\/usr\/local\/bin\/docker-entrypoint"]`

```dockerfile
# Mon, 03 Jun 2024 16:52:57 GMT
ARG RELEASE
# Mon, 03 Jun 2024 16:52:57 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 03 Jun 2024 16:52:57 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 03 Jun 2024 16:52:57 GMT
LABEL org.opencontainers.image.version=20.04
# Mon, 03 Jun 2024 16:52:59 GMT
ADD file:6d8cc056ee741f09a6c7d965d8e2027d80ed2eccbfb0312593ce52d9256db437 in / 
# Mon, 03 Jun 2024 16:52:59 GMT
CMD ["/bin/bash"]
# Thu, 08 Aug 2024 13:05:51 GMT
RUN for iter in {1..10}; do       export DEBIAN_FRONTEND=noninteractive &&     apt-get update -y &&   apt-get upgrade -y &&   apt-get install -y procps findutils tar gzip &&         apt-get install -y locales &&         apt-get install -y curl &&     apt-get clean all &&       locale-gen 'en_US.UTF-8' &&     apt-get clean metadata &&   exit_code=0 && break || exit_code=$? && echo "packaging error: retry $iter in 10s" && apt-get clean all &&   apt-get clean metadata && sleep 10; done; (exit $exit_code) # buildkit
# Thu, 08 Aug 2024 13:05:51 GMT
RUN groupadd --gid 1000 logstash &&   adduser --uid 1000 --gid 1000 --home /usr/share/logstash --no-create-home logstash # buildkit
# Thu, 08 Aug 2024 13:05:51 GMT
RUN curl -Lo - https://artifacts.elastic.co/downloads/logstash/logstash-8.15.0-linux-$(arch).tar.gz |   tar zxf - -C /usr/share &&   mv /usr/share/logstash-8.15.0 /usr/share/logstash &&   chown --recursive logstash:logstash /usr/share/logstash/ &&   chown -R logstash:root /usr/share/logstash &&   chmod -R g=u /usr/share/logstash &&   mkdir /licenses/ &&   mv /usr/share/logstash/NOTICE.TXT /licenses/NOTICE.TXT &&   mv /usr/share/logstash/LICENSE.txt /licenses/LICENSE.txt &&   find /usr/share/logstash -type d -exec chmod g+s {} \; &&   ln -s /usr/share/logstash /opt/logstash # buildkit
# Thu, 08 Aug 2024 13:05:51 GMT
WORKDIR /usr/share/logstash
# Thu, 08 Aug 2024 13:05:51 GMT
ENV ELASTIC_CONTAINER=true
# Thu, 08 Aug 2024 13:05:51 GMT
ENV PATH=/usr/share/logstash/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 08 Aug 2024 13:05:51 GMT
COPY config/logstash-full.yml config/logstash.yml # buildkit
# Thu, 08 Aug 2024 13:05:51 GMT
COPY config/pipelines.yml config/log4j2.properties config/log4j2.file.properties config/ # buildkit
# Thu, 08 Aug 2024 13:05:51 GMT
COPY pipeline/default.conf pipeline/logstash.conf # buildkit
# Thu, 08 Aug 2024 13:05:51 GMT
RUN chown --recursive logstash:root config/ pipeline/ # buildkit
# Thu, 08 Aug 2024 13:05:51 GMT
ENV LANG=en_US.UTF-8 LC_ALL=en_US.UTF-8
# Thu, 08 Aug 2024 13:05:51 GMT
COPY env2yaml/env2yaml-amd64 env2yaml/env2yaml-arm64 env2yaml/ # buildkit
# Thu, 08 Aug 2024 13:05:51 GMT
RUN env2yamlarch="$(dpkg --print-architecture)";   case "${env2yamlarch}" in     'x86_64'|'amd64')       env2yamlarch=amd64;       ;;     'aarch64'|'arm64')       env2yamlarch=arm64;       ;;     *) echo >&2 "error: unsupported architecture '$env2yamlarch'"; exit 1 ;;   esac;   mkdir -p /usr/local/bin;   cp env2yaml/env2yaml-${env2yamlarch} /usr/local/bin/env2yaml;   rm -rf env2yaml # buildkit
# Thu, 08 Aug 2024 13:05:51 GMT
COPY bin/docker-entrypoint /usr/local/bin/ # buildkit
# Thu, 08 Aug 2024 13:05:51 GMT
RUN chmod 0755 /usr/local/bin/docker-entrypoint # buildkit
# Thu, 08 Aug 2024 13:05:51 GMT
USER 1000
# Thu, 08 Aug 2024 13:05:51 GMT
EXPOSE map[5044/tcp:{} 9600/tcp:{}]
# Thu, 08 Aug 2024 13:05:51 GMT
LABEL org.label-schema.schema-version=1.0 org.label-schema.vendor=Elastic org.opencontainers.image.vendor=Elastic org.label-schema.name=logstash org.opencontainers.image.title=logstash org.label-schema.version=8.15.0 org.opencontainers.image.version=8.15.0 org.label-schema.url=https://www.elastic.co/products/logstash org.label-schema.vcs-url=https://github.com/elastic/logstash org.label-schema.license=Elastic License org.opencontainers.image.licenses=Elastic License org.opencontainers.image.description=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' org.label-schema.build-date=2024-07-24T10:13:18+00:00 org.opencontainers.image.created=2024-07-24T10:13:18+00:00
# Thu, 08 Aug 2024 13:05:51 GMT
ENTRYPOINT ["/usr/local/bin/docker-entrypoint"]
```

-	Layers:
	-	`sha256:f02209be4ee528c246399de81af4552e52adb005a8a499815607b6b0d42746bf`  
		Last Modified: Mon, 03 Jun 2024 17:19:48 GMT  
		Size: 26.0 MB (25974217 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1f53b1ddb3e129f5c7b542be871b2e0508aa900d3280fee5696b66ad09e759e`  
		Last Modified: Thu, 08 Aug 2024 23:09:08 GMT  
		Size: 38.0 MB (38009337 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:178f3ab1949c3be422490b62f545bb474f9abe2ebbd78f273ea5a431f68a3fac`  
		Last Modified: Thu, 08 Aug 2024 23:09:06 GMT  
		Size: 1.8 KB (1809 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:888df0ecd1d0f4d7848a58efb8e30da07bef9f9d75090c158e2a93d83716d4c7`  
		Last Modified: Thu, 08 Aug 2024 23:09:15 GMT  
		Size: 420.1 MB (420098840 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:789a0d0cc9f9693fc48722eb16ac82ae88c05f9783c9db7db40d5ecbb07e9f06`  
		Last Modified: Thu, 08 Aug 2024 23:09:07 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:afacfd02c65660a2366ef8e16de34da5e68e11ab7bed67d38d0d49319b8dae44`  
		Last Modified: Thu, 08 Aug 2024 23:09:07 GMT  
		Size: 1.6 KB (1576 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc3ca06183fc09e0da2638196756149d742f2ca911cae741eb940cc6d3f3900f`  
		Last Modified: Thu, 08 Aug 2024 23:09:08 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bff18a76d581cd80ae743e870847ec41837f109af8f4edeeec00459d84aa7e54`  
		Last Modified: Thu, 08 Aug 2024 23:09:08 GMT  
		Size: 1.8 KB (1763 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:197c88cc9c7aa0b8d1730f197cbe6e089f679e4ca9449d5461939b62496de9d4`  
		Last Modified: Thu, 08 Aug 2024 23:09:09 GMT  
		Size: 3.7 MB (3690575 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbb62228dc5008d349a327289b68be5c7ec71ad1b3111b03157be030849912f7`  
		Last Modified: Thu, 08 Aug 2024 23:09:09 GMT  
		Size: 1.8 MB (1787528 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0790177f07146cdb0e8d62182a9e8d32dffb9cf41c6a8a4cc64f4bfa70c0f370`  
		Last Modified: Thu, 08 Aug 2024 23:09:09 GMT  
		Size: 713.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `logstash:8.15.0` - unknown; unknown

```console
$ docker pull logstash@sha256:ded2ce5a1ed11c23161d14699d4363814ad95717e2ad21410a7010d407748942
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3273611 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf0747d43c8f69dc936f1a880aa939cd438a640bedd9ff3c172cffdc20d23b8c`

```dockerfile
```

-	Layers:
	-	`sha256:829b310662ea485550212ec16fd291647767d83edeaf8fbfa1afb5a7b3645c7f`  
		Last Modified: Thu, 08 Aug 2024 23:09:07 GMT  
		Size: 3.2 MB (3239029 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c411ba830d7c927331211739c8a4375ff38bbc02c39ecec2e0de613f9461c1e9`  
		Last Modified: Thu, 08 Aug 2024 23:09:06 GMT  
		Size: 34.6 KB (34582 bytes)  
		MIME: application/vnd.in-toto+json
