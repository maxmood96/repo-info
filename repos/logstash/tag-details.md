<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `logstash`

-	[`logstash:7.17.24`](#logstash71724)
-	[`logstash:8.15.2`](#logstash8152)

## `logstash:7.17.24`

```console
$ docker pull logstash@sha256:e332d5b602084e079c0c9aefab6c72446dc5e31589752d0cdba67722d95c77b8
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `logstash:7.17.24` - linux; amd64

```console
$ docker pull logstash@sha256:9be0780873b568b855daf10668f046616ca873400b0fa1a69bbb3b71352a8cef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **450.6 MB (450557474 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7fa3d604897f920596bf30120de679f2c276ad729f3af93e709d6f48aedd048e`
-	Entrypoint: `["\/usr\/local\/bin\/docker-entrypoint"]`

```dockerfile
# Tue, 10 Sep 2024 08:21:14 GMT
ARG RELEASE
# Tue, 10 Sep 2024 08:21:14 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 10 Sep 2024 08:21:14 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 10 Sep 2024 08:21:14 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 10 Sep 2024 08:21:14 GMT
ADD file:6a209aa51ba684c0a39769619c42058ca99311b87563c7b079319a8bb91bec1f in / 
# Tue, 10 Sep 2024 08:21:14 GMT
CMD ["/bin/bash"]
# Tue, 10 Sep 2024 08:21:14 GMT
RUN for iter in {1..10}; do     export DEBIAN_FRONTEND=noninteractive &&     apt-get update -y &&     apt-get upgrade -y &&     apt-get install -y procps findutils tar gzip curl &&     apt-get install -y locales &&     apt-get clean all &&     locale-gen 'en_US.UTF-8' &&     apt-get clean metadata &&     exit_code=0 && break || exit_code=$? &&     echo "packaging error: retry $iter in 10s" &&     apt-get clean all &&     apt-get clean metadata &&     sleep 10; done;     (exit $exit_code) # buildkit
# Tue, 10 Sep 2024 08:21:14 GMT
RUN groupadd --gid 1000 logstash &&     adduser --uid 1000 --gid 1000     --home /usr/share/logstash --no-create-home     logstash # buildkit
# Tue, 10 Sep 2024 08:21:14 GMT
RUN curl -Lo - https://artifacts.elastic.co/downloads/logstash/logstash-7.17.24-linux-$(arch).tar.gz |     tar zxf - -C /usr/share &&     mv /usr/share/logstash-7.17.24 /usr/share/logstash &&     chown --recursive logstash:logstash /usr/share/logstash/ &&     chown -R logstash:root /usr/share/logstash &&     chmod -R g=u /usr/share/logstash &&     mkdir /licenses/ &&     mv /usr/share/logstash/NOTICE.TXT /licenses/NOTICE.TXT &&     mv /usr/share/logstash/LICENSE.txt /licenses/LICENSE.txt &&     find /usr/share/logstash -type d -exec chmod g+s {} \; &&     ln -s /usr/share/logstash /opt/logstash # buildkit
# Tue, 10 Sep 2024 08:21:14 GMT
WORKDIR /usr/share/logstash
# Tue, 10 Sep 2024 08:21:14 GMT
ENV ELASTIC_CONTAINER=true
# Tue, 10 Sep 2024 08:21:14 GMT
ENV PATH=/usr/share/logstash/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 10 Sep 2024 08:21:14 GMT
COPY config/pipelines.yml config/pipelines.yml # buildkit
# Tue, 10 Sep 2024 08:21:14 GMT
COPY config/logstash-full.yml config/logstash.yml # buildkit
# Tue, 10 Sep 2024 08:21:14 GMT
COPY config/log4j2.properties config/ # buildkit
# Tue, 10 Sep 2024 08:21:14 GMT
COPY pipeline/default.conf pipeline/logstash.conf # buildkit
# Tue, 10 Sep 2024 08:21:14 GMT
RUN chown --recursive logstash:root config/ pipeline/ # buildkit
# Tue, 10 Sep 2024 08:21:14 GMT
ENV LANG=en_US.UTF-8 LC_ALL=en_US.UTF-8
# Tue, 10 Sep 2024 08:21:14 GMT
COPY env2yaml/env2yaml /usr/local/bin/ # buildkit
# Tue, 10 Sep 2024 08:21:14 GMT
COPY bin/docker-entrypoint /usr/local/bin/ # buildkit
# Tue, 10 Sep 2024 08:21:14 GMT
RUN chmod 0755 /usr/local/bin/docker-entrypoint # buildkit
# Tue, 10 Sep 2024 08:21:14 GMT
USER 1000
# Tue, 10 Sep 2024 08:21:14 GMT
EXPOSE map[5044/tcp:{} 9600/tcp:{}]
# Tue, 10 Sep 2024 08:21:14 GMT
LABEL org.label-schema.schema-version=1.0 org.label-schema.vendor=Elastic org.opencontainers.image.vendor=Elastic org.label-schema.name=logstash org.opencontainers.image.title=logstash org.label-schema.version=7.17.24 org.opencontainers.image.version=7.17.24 org.label-schema.url=https://www.elastic.co/products/logstash org.label-schema.vcs-url=https://github.com/elastic/logstash org.label-schema.license=Elastic License org.opencontainers.image.licenses=Elastic License org.opencontainers.image.description=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' org.label-schema.build-date=2024-09-03T23:04:52+00:00 org.opencontainers.image.created=2024-09-03T23:04:52+00:00
# Tue, 10 Sep 2024 08:21:14 GMT
ENTRYPOINT ["/usr/local/bin/docker-entrypoint"]
```

-	Layers:
	-	`sha256:3823320faa42774534fd7eee0bd245af8cec6a720ad722144d40efa229291d8f`  
		Last Modified: Wed, 18 Sep 2024 05:32:37 GMT  
		Size: 27.5 MB (27511052 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d233dc36841b180c0ace657d8bfb191b2a05dd74d2f8c9cf6005ad50929f4519`  
		Last Modified: Wed, 02 Oct 2024 01:59:12 GMT  
		Size: 50.0 MB (49982665 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0d9007c6cd4505ea77d6b295dbe2d44e8e7d32db0d1641247cbd64056f10e07`  
		Last Modified: Wed, 02 Oct 2024 01:59:11 GMT  
		Size: 1.8 KB (1804 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:024160d5f58456b2cebaa798f294de957d7efbf4e5a10f52ee5484f2b9b02579`  
		Last Modified: Wed, 02 Oct 2024 01:59:19 GMT  
		Size: 371.0 MB (370998012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74100623470d8d802638894273e879932f8ff28283ddb75842a6bc38ddd05b60`  
		Last Modified: Wed, 02 Oct 2024 01:59:11 GMT  
		Size: 380.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:967460c01a55f5e970038d23cded7a0bb4f52cf5a0d8735b260c49f6f9874069`  
		Last Modified: Wed, 02 Oct 2024 01:59:12 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dea5974690c1455d103800405939c156fabc09d7df61e81723e3d151187e9dae`  
		Last Modified: Wed, 02 Oct 2024 01:59:13 GMT  
		Size: 474.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da796ffa193917987a04a5720bf11d97dfe74caafce131f1f2a643f2b7d3ea3b`  
		Last Modified: Wed, 02 Oct 2024 01:59:13 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e41fd3307aa380ea9ffadfb87c2542b8f2fa18667911ebbb95473f0828c2b31`  
		Last Modified: Wed, 02 Oct 2024 01:59:14 GMT  
		Size: 828.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c27935f1afb948d0354805df549832ce5388ddfbd877e09f39a430805cba6a1b`  
		Last Modified: Wed, 02 Oct 2024 01:59:14 GMT  
		Size: 2.1 MB (2061143 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61088760a62951cd71ca5875754c657a387b78e4bd3087e047b509bc7abb644e`  
		Last Modified: Wed, 02 Oct 2024 01:59:14 GMT  
		Size: 494.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `logstash:7.17.24` - unknown; unknown

```console
$ docker pull logstash@sha256:e6375851b9e392a47d83905fcb2072475f92c56c64d2c16d37bdf642c7a58755
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3278078 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f66265dc5eaf23c1cc093af88a89d83f2b30311c7803cbf21509a3c3d1d1db3b`

```dockerfile
```

-	Layers:
	-	`sha256:3b95e862d0079f65a597373e8afa6f48ea081878863cd928be4e77e68360c1de`  
		Last Modified: Wed, 02 Oct 2024 01:59:11 GMT  
		Size: 3.2 MB (3246143 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:23cd78d26468a6ab66ca6dead7cdade7f88e4a16245112653b43e02390e6f1e1`  
		Last Modified: Wed, 02 Oct 2024 01:59:11 GMT  
		Size: 31.9 KB (31935 bytes)  
		MIME: application/vnd.in-toto+json

### `logstash:7.17.24` - linux; arm64 variant v8

```console
$ docker pull logstash@sha256:958a899fd6d59761223f1fb1efb2ebc4ed4a73384466e23704a3670797ade4b9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **434.0 MB (434036860 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5815c5437fa0445caa8620ba2b8217f1410a3f5806962640977e543c5d7d051b`
-	Entrypoint: `["\/usr\/local\/bin\/docker-entrypoint"]`

```dockerfile
# Tue, 13 Aug 2024 09:27:56 GMT
ARG RELEASE
# Tue, 13 Aug 2024 09:27:56 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Aug 2024 09:27:56 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Aug 2024 09:27:56 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 13 Aug 2024 09:27:58 GMT
ADD file:6d8cc056ee741f09a6c7d965d8e2027d80ed2eccbfb0312593ce52d9256db437 in / 
# Tue, 13 Aug 2024 09:27:58 GMT
CMD ["/bin/bash"]
# Tue, 10 Sep 2024 08:21:14 GMT
RUN for iter in {1..10}; do     export DEBIAN_FRONTEND=noninteractive &&     apt-get update -y &&     apt-get upgrade -y &&     apt-get install -y procps findutils tar gzip curl &&     apt-get install -y locales &&     apt-get clean all &&     locale-gen 'en_US.UTF-8' &&     apt-get clean metadata &&     exit_code=0 && break || exit_code=$? &&     echo "packaging error: retry $iter in 10s" &&     apt-get clean all &&     apt-get clean metadata &&     sleep 10; done;     (exit $exit_code) # buildkit
# Tue, 10 Sep 2024 08:21:14 GMT
RUN groupadd --gid 1000 logstash &&     adduser --uid 1000 --gid 1000     --home /usr/share/logstash --no-create-home     logstash # buildkit
# Tue, 10 Sep 2024 08:21:14 GMT
RUN curl -Lo - https://artifacts.elastic.co/downloads/logstash/logstash-7.17.24-linux-$(arch).tar.gz |     tar zxf - -C /usr/share &&     mv /usr/share/logstash-7.17.24 /usr/share/logstash &&     chown --recursive logstash:logstash /usr/share/logstash/ &&     chown -R logstash:root /usr/share/logstash &&     chmod -R g=u /usr/share/logstash &&     mkdir /licenses/ &&     mv /usr/share/logstash/NOTICE.TXT /licenses/NOTICE.TXT &&     mv /usr/share/logstash/LICENSE.txt /licenses/LICENSE.txt &&     find /usr/share/logstash -type d -exec chmod g+s {} \; &&     ln -s /usr/share/logstash /opt/logstash # buildkit
# Tue, 10 Sep 2024 08:21:14 GMT
WORKDIR /usr/share/logstash
# Tue, 10 Sep 2024 08:21:14 GMT
ENV ELASTIC_CONTAINER=true
# Tue, 10 Sep 2024 08:21:14 GMT
ENV PATH=/usr/share/logstash/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 10 Sep 2024 08:21:14 GMT
COPY config/pipelines.yml config/pipelines.yml # buildkit
# Tue, 10 Sep 2024 08:21:14 GMT
COPY config/logstash-full.yml config/logstash.yml # buildkit
# Tue, 10 Sep 2024 08:21:14 GMT
COPY config/log4j2.properties config/ # buildkit
# Tue, 10 Sep 2024 08:21:14 GMT
COPY pipeline/default.conf pipeline/logstash.conf # buildkit
# Tue, 10 Sep 2024 08:21:14 GMT
RUN chown --recursive logstash:root config/ pipeline/ # buildkit
# Tue, 10 Sep 2024 08:21:14 GMT
ENV LANG=en_US.UTF-8 LC_ALL=en_US.UTF-8
# Tue, 10 Sep 2024 08:21:14 GMT
COPY env2yaml/env2yaml /usr/local/bin/ # buildkit
# Tue, 10 Sep 2024 08:21:14 GMT
COPY bin/docker-entrypoint /usr/local/bin/ # buildkit
# Tue, 10 Sep 2024 08:21:14 GMT
RUN chmod 0755 /usr/local/bin/docker-entrypoint # buildkit
# Tue, 10 Sep 2024 08:21:14 GMT
USER 1000
# Tue, 10 Sep 2024 08:21:14 GMT
EXPOSE map[5044/tcp:{} 9600/tcp:{}]
# Tue, 10 Sep 2024 08:21:14 GMT
LABEL org.label-schema.schema-version=1.0 org.label-schema.vendor=Elastic org.opencontainers.image.vendor=Elastic org.label-schema.name=logstash org.opencontainers.image.title=logstash org.label-schema.version=7.17.24 org.opencontainers.image.version=7.17.24 org.label-schema.url=https://www.elastic.co/products/logstash org.label-schema.vcs-url=https://github.com/elastic/logstash org.label-schema.license=Elastic License org.opencontainers.image.licenses=Elastic License org.opencontainers.image.description=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' org.label-schema.build-date=2024-09-03T23:04:52+00:00 org.opencontainers.image.created=2024-09-03T23:04:52+00:00
# Tue, 10 Sep 2024 08:21:14 GMT
ENTRYPOINT ["/usr/local/bin/docker-entrypoint"]
```

-	Layers:
	-	`sha256:6a1df50fc4815789598fa24d3ecacb70451e506447ab9e45665024b9f3f0233b`  
		Last Modified: Tue, 13 Aug 2024 10:23:55 GMT  
		Size: 26.0 MB (25974217 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4d75e0455933a035161db35f999c3e38bf8c0b81b4687dcfa767354d1e02686`  
		Last Modified: Tue, 10 Sep 2024 22:05:28 GMT  
		Size: 38.2 MB (38181170 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:409621c5fec8bc93ed897492984b1c57bbb4cb33015f344547b8d29f6549521f`  
		Last Modified: Tue, 10 Sep 2024 22:05:27 GMT  
		Size: 1.8 KB (1814 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd767bc60bb075e2cc749142d7b1d608eeed5e0fa6323d44ff0d4d420d9ce0e0`  
		Last Modified: Tue, 10 Sep 2024 22:05:35 GMT  
		Size: 367.8 MB (367815720 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:271b84cae8fc846f1fc4e9f5fdd18d8975821f44eae7fbd1c52f7dcc212e2beb`  
		Last Modified: Tue, 10 Sep 2024 22:05:27 GMT  
		Size: 378.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0af25cfc27094aa8b071d3c0658799de71789ccf2a3ae0fdbe8b67fea7b40c1`  
		Last Modified: Tue, 10 Sep 2024 22:05:28 GMT  
		Size: 278.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed4c236b104b5835c5b4ff568413054d2dadbf1c6871836caabb64374c875a4c`  
		Last Modified: Tue, 10 Sep 2024 22:05:28 GMT  
		Size: 474.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c01406b49c1cbd4db183311bc184f5d648dc91407218bcf39c163ee6fa261084`  
		Last Modified: Tue, 10 Sep 2024 22:05:29 GMT  
		Size: 278.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8da609f70a91af0da3e33495522dadcb4eeb981148541519c5cfdaa7ae1848b8`  
		Last Modified: Tue, 10 Sep 2024 22:05:29 GMT  
		Size: 829.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0fca40dd4dcfc48e0e8f579fba1b7b451de44dc48d4d8412072e6a2b0ef5b03f`  
		Last Modified: Tue, 10 Sep 2024 22:05:30 GMT  
		Size: 2.1 MB (2061144 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e2c7e4345bcfebdcf2a9d29e04f8d878a92f38564af865410a4ba3406396e19`  
		Last Modified: Tue, 10 Sep 2024 22:05:30 GMT  
		Size: 494.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `logstash:7.17.24` - unknown; unknown

```console
$ docker pull logstash@sha256:d2d6171d30ba98eeb64befaf0d70314e79060c604b488e16ed1faf902515ec63
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3101168 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac9ae68588fa8363d2c49aee13cd1e8150b5bbe438b6fca0c84f92838803fef8`

```dockerfile
```

-	Layers:
	-	`sha256:be4e20bcc06547192e2fa021addb0bd9ced0582bd78580a0926e59791ea26109`  
		Last Modified: Tue, 10 Sep 2024 22:05:27 GMT  
		Size: 3.1 MB (3068971 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dc30ebb1df5db46fdab69dc1a9e7d87e74e24c448dc73fed52379641d38eb8c6`  
		Last Modified: Tue, 10 Sep 2024 22:05:27 GMT  
		Size: 32.2 KB (32197 bytes)  
		MIME: application/vnd.in-toto+json

## `logstash:8.15.2`

```console
$ docker pull logstash@sha256:eb58e8586053d2b02d4623dc657efcd356405eed62d221fd4e9b807b72dc9440
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `logstash:8.15.2` - linux; amd64

```console
$ docker pull logstash@sha256:6a392c7cd1822a5f34535d55cff202c3e873653f5aabdf0bcbce2ce37757e05e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **505.2 MB (505177128 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ceff0d824270f536ef7fbb496ef8386e7c614b9fb81eb60c9b71065be786e60f`
-	Entrypoint: `["\/usr\/local\/bin\/docker-entrypoint"]`

```dockerfile
# Wed, 18 Sep 2024 04:18:32 GMT
ARG RELEASE
# Wed, 18 Sep 2024 04:18:32 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 18 Sep 2024 04:18:32 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 18 Sep 2024 04:18:32 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 18 Sep 2024 04:18:34 GMT
ADD file:6a209aa51ba684c0a39769619c42058ca99311b87563c7b079319a8bb91bec1f in / 
# Wed, 18 Sep 2024 04:18:34 GMT
CMD ["/bin/bash"]
# Thu, 26 Sep 2024 08:08:51 GMT
RUN for iter in {1..10}; do       export DEBIAN_FRONTEND=noninteractive &&     apt-get update -y &&   apt-get upgrade -y &&   apt-get install -y procps findutils tar gzip &&         apt-get install -y locales &&         apt-get install -y curl &&     apt-get clean all &&       locale-gen 'en_US.UTF-8' &&     apt-get clean metadata &&   exit_code=0 && break || exit_code=$? && echo "packaging error: retry $iter in 10s" && apt-get clean all &&   apt-get clean metadata && sleep 10; done; (exit $exit_code) # buildkit
# Thu, 26 Sep 2024 08:08:51 GMT
RUN groupadd --gid 1000 logstash &&   adduser --uid 1000 --gid 1000 --home /usr/share/logstash --no-create-home logstash # buildkit
# Thu, 26 Sep 2024 08:08:51 GMT
RUN curl -Lo - https://artifacts.elastic.co/downloads/logstash/logstash-8.15.2-linux-$(arch).tar.gz |   tar zxf - -C /usr/share &&   mv /usr/share/logstash-8.15.2 /usr/share/logstash &&   chown --recursive logstash:logstash /usr/share/logstash/ &&   chown -R logstash:root /usr/share/logstash &&   chmod -R g=u /usr/share/logstash &&   mkdir /licenses/ &&   mv /usr/share/logstash/NOTICE.TXT /licenses/NOTICE.TXT &&   mv /usr/share/logstash/LICENSE.txt /licenses/LICENSE.txt &&   find /usr/share/logstash -type d -exec chmod g+s {} \; &&   ln -s /usr/share/logstash /opt/logstash # buildkit
# Thu, 26 Sep 2024 08:08:51 GMT
WORKDIR /usr/share/logstash
# Thu, 26 Sep 2024 08:08:51 GMT
ENV ELASTIC_CONTAINER=true
# Thu, 26 Sep 2024 08:08:51 GMT
ENV PATH=/usr/share/logstash/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 26 Sep 2024 08:08:51 GMT
COPY config/logstash-full.yml config/logstash.yml # buildkit
# Thu, 26 Sep 2024 08:08:51 GMT
COPY config/pipelines.yml config/log4j2.properties config/log4j2.file.properties config/ # buildkit
# Thu, 26 Sep 2024 08:08:51 GMT
COPY pipeline/default.conf pipeline/logstash.conf # buildkit
# Thu, 26 Sep 2024 08:08:51 GMT
RUN chown --recursive logstash:root config/ pipeline/ # buildkit
# Thu, 26 Sep 2024 08:08:51 GMT
ENV LANG=en_US.UTF-8 LC_ALL=en_US.UTF-8
# Thu, 26 Sep 2024 08:08:51 GMT
COPY env2yaml/env2yaml-amd64 env2yaml/env2yaml-arm64 env2yaml/ # buildkit
# Thu, 26 Sep 2024 08:08:51 GMT
RUN env2yamlarch="$(dpkg --print-architecture)";   case "${env2yamlarch}" in     'x86_64'|'amd64')       env2yamlarch=amd64;       ;;     'aarch64'|'arm64')       env2yamlarch=arm64;       ;;     *) echo >&2 "error: unsupported architecture '$env2yamlarch'"; exit 1 ;;   esac;   mkdir -p /usr/local/bin;   cp env2yaml/env2yaml-${env2yamlarch} /usr/local/bin/env2yaml;   rm -rf env2yaml # buildkit
# Thu, 26 Sep 2024 08:08:51 GMT
COPY bin/docker-entrypoint /usr/local/bin/ # buildkit
# Thu, 26 Sep 2024 08:08:51 GMT
RUN chmod 0755 /usr/local/bin/docker-entrypoint # buildkit
# Thu, 26 Sep 2024 08:08:51 GMT
USER 1000
# Thu, 26 Sep 2024 08:08:51 GMT
EXPOSE map[5044/tcp:{} 9600/tcp:{}]
# Thu, 26 Sep 2024 08:08:51 GMT
LABEL org.label-schema.schema-version=1.0 org.label-schema.vendor=Elastic org.opencontainers.image.vendor=Elastic org.label-schema.name=logstash org.opencontainers.image.title=logstash org.label-schema.version=8.15.2 org.opencontainers.image.version=8.15.2 org.label-schema.url=https://www.elastic.co/products/logstash org.label-schema.vcs-url=https://github.com/elastic/logstash org.label-schema.license=Elastic License org.opencontainers.image.licenses=Elastic License org.opencontainers.image.description=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' org.label-schema.build-date=2024-09-17T15:11:45+00:00 org.opencontainers.image.created=2024-09-17T15:11:45+00:00
# Thu, 26 Sep 2024 08:08:51 GMT
ENTRYPOINT ["/usr/local/bin/docker-entrypoint"]
```

-	Layers:
	-	`sha256:3823320faa42774534fd7eee0bd245af8cec6a720ad722144d40efa229291d8f`  
		Last Modified: Wed, 18 Sep 2024 05:32:37 GMT  
		Size: 27.5 MB (27511052 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc08e005bd2fcf576c459cd40b413a2cf4511d462cb76ca676bca086e8416a6c`  
		Last Modified: Wed, 02 Oct 2024 01:58:53 GMT  
		Size: 50.0 MB (49991049 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9453e1d65f21a8558b9d3d5a06d7b0a866fe9e4444f8f19693819f1b2669b43`  
		Last Modified: Wed, 02 Oct 2024 01:58:53 GMT  
		Size: 1.8 KB (1804 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9ae9a179b4dfb16b7626771bd3e329ea4bdf10059d3b79d15231dcaf27d178b`  
		Last Modified: Wed, 02 Oct 2024 01:58:58 GMT  
		Size: 421.6 MB (421611170 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc31cfd3e01d123eda5ccea0b39a81925f0e099ad6b7b303e32ca017bf7b34a4`  
		Last Modified: Wed, 02 Oct 2024 01:58:53 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ec584fa1a7f3159a5e37e8f667d588b6334895ee7dc5f19a61205dd99f7f8c4`  
		Last Modified: Wed, 02 Oct 2024 01:58:53 GMT  
		Size: 1.6 KB (1578 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48a03797e11abc97d5b21c6398c83432ec27c5f2e6dbdd1821eac7f1ce795d8e`  
		Last Modified: Wed, 02 Oct 2024 01:58:54 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10953fac3d45f60de4f1ec4ce7de75b4f4380410da29a2fa68bda42c164f24b7`  
		Last Modified: Wed, 02 Oct 2024 01:58:54 GMT  
		Size: 1.8 KB (1765 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5cddaf797ddfa04da4cb53d15319a3c5129b70c6eaf4459f5ea1ffcdd73d754c`  
		Last Modified: Wed, 02 Oct 2024 01:58:54 GMT  
		Size: 4.0 MB (3995859 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a96f1f0329cf2cc77adef4ec6f75e5ccd75486c4642bff6f5da8f11e562ddc22`  
		Last Modified: Wed, 02 Oct 2024 01:58:55 GMT  
		Size: 2.1 MB (2061521 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03cc6b190baad9ebf864b1cc5cd130cb0aefb6282b0e087960d92420f4172e62`  
		Last Modified: Wed, 02 Oct 2024 01:58:55 GMT  
		Size: 710.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `logstash:8.15.2` - unknown; unknown

```console
$ docker pull logstash@sha256:47dc0690be7c5bdb8f32e919a9f49d52c574e878364b2d4232ca489fc4394bab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.4 MB (3431857 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:644d7994390727bf454499dfbc6b4264829a4230f1cc4f50533eecf89146a4f9`

```dockerfile
```

-	Layers:
	-	`sha256:268261867f18edad189ba18c429eb98f0891e6ea0d0306abae4a4d6d4020ec98`  
		Last Modified: Wed, 02 Oct 2024 01:58:53 GMT  
		Size: 3.4 MB (3397535 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5d6206d3b763f0e1a3cef9574da611efc65e2369627058d7e9b98c65556cfd39`  
		Last Modified: Wed, 02 Oct 2024 01:58:53 GMT  
		Size: 34.3 KB (34322 bytes)  
		MIME: application/vnd.in-toto+json

### `logstash:8.15.2` - linux; arm64 variant v8

```console
$ docker pull logstash@sha256:e3a481101eeccabaa8cdf74bf012ae048a279a326857e5fcae955f4de068f6f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **490.4 MB (490430530 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:edd6ed9ec1d15386a66cb80c6703b2785eba6cdf1200515512f6416723bb31a3`
-	Entrypoint: `["\/usr\/local\/bin\/docker-entrypoint"]`

```dockerfile
# Tue, 13 Aug 2024 09:27:56 GMT
ARG RELEASE
# Tue, 13 Aug 2024 09:27:56 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Aug 2024 09:27:56 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Aug 2024 09:27:56 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 13 Aug 2024 09:27:58 GMT
ADD file:6d8cc056ee741f09a6c7d965d8e2027d80ed2eccbfb0312593ce52d9256db437 in / 
# Tue, 13 Aug 2024 09:27:58 GMT
CMD ["/bin/bash"]
# Thu, 26 Sep 2024 08:08:51 GMT
RUN for iter in {1..10}; do       export DEBIAN_FRONTEND=noninteractive &&     apt-get update -y &&   apt-get upgrade -y &&   apt-get install -y procps findutils tar gzip &&         apt-get install -y locales &&         apt-get install -y curl &&     apt-get clean all &&       locale-gen 'en_US.UTF-8' &&     apt-get clean metadata &&   exit_code=0 && break || exit_code=$? && echo "packaging error: retry $iter in 10s" && apt-get clean all &&   apt-get clean metadata && sleep 10; done; (exit $exit_code) # buildkit
# Thu, 26 Sep 2024 08:08:51 GMT
RUN groupadd --gid 1000 logstash &&   adduser --uid 1000 --gid 1000 --home /usr/share/logstash --no-create-home logstash # buildkit
# Thu, 26 Sep 2024 08:08:51 GMT
RUN curl -Lo - https://artifacts.elastic.co/downloads/logstash/logstash-8.15.2-linux-$(arch).tar.gz |   tar zxf - -C /usr/share &&   mv /usr/share/logstash-8.15.2 /usr/share/logstash &&   chown --recursive logstash:logstash /usr/share/logstash/ &&   chown -R logstash:root /usr/share/logstash &&   chmod -R g=u /usr/share/logstash &&   mkdir /licenses/ &&   mv /usr/share/logstash/NOTICE.TXT /licenses/NOTICE.TXT &&   mv /usr/share/logstash/LICENSE.txt /licenses/LICENSE.txt &&   find /usr/share/logstash -type d -exec chmod g+s {} \; &&   ln -s /usr/share/logstash /opt/logstash # buildkit
# Thu, 26 Sep 2024 08:08:51 GMT
WORKDIR /usr/share/logstash
# Thu, 26 Sep 2024 08:08:51 GMT
ENV ELASTIC_CONTAINER=true
# Thu, 26 Sep 2024 08:08:51 GMT
ENV PATH=/usr/share/logstash/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 26 Sep 2024 08:08:51 GMT
COPY config/logstash-full.yml config/logstash.yml # buildkit
# Thu, 26 Sep 2024 08:08:51 GMT
COPY config/pipelines.yml config/log4j2.properties config/log4j2.file.properties config/ # buildkit
# Thu, 26 Sep 2024 08:08:51 GMT
COPY pipeline/default.conf pipeline/logstash.conf # buildkit
# Thu, 26 Sep 2024 08:08:51 GMT
RUN chown --recursive logstash:root config/ pipeline/ # buildkit
# Thu, 26 Sep 2024 08:08:51 GMT
ENV LANG=en_US.UTF-8 LC_ALL=en_US.UTF-8
# Thu, 26 Sep 2024 08:08:51 GMT
COPY env2yaml/env2yaml-amd64 env2yaml/env2yaml-arm64 env2yaml/ # buildkit
# Thu, 26 Sep 2024 08:08:51 GMT
RUN env2yamlarch="$(dpkg --print-architecture)";   case "${env2yamlarch}" in     'x86_64'|'amd64')       env2yamlarch=amd64;       ;;     'aarch64'|'arm64')       env2yamlarch=arm64;       ;;     *) echo >&2 "error: unsupported architecture '$env2yamlarch'"; exit 1 ;;   esac;   mkdir -p /usr/local/bin;   cp env2yaml/env2yaml-${env2yamlarch} /usr/local/bin/env2yaml;   rm -rf env2yaml # buildkit
# Thu, 26 Sep 2024 08:08:51 GMT
COPY bin/docker-entrypoint /usr/local/bin/ # buildkit
# Thu, 26 Sep 2024 08:08:51 GMT
RUN chmod 0755 /usr/local/bin/docker-entrypoint # buildkit
# Thu, 26 Sep 2024 08:08:51 GMT
USER 1000
# Thu, 26 Sep 2024 08:08:51 GMT
EXPOSE map[5044/tcp:{} 9600/tcp:{}]
# Thu, 26 Sep 2024 08:08:51 GMT
LABEL org.label-schema.schema-version=1.0 org.label-schema.vendor=Elastic org.opencontainers.image.vendor=Elastic org.label-schema.name=logstash org.opencontainers.image.title=logstash org.label-schema.version=8.15.2 org.opencontainers.image.version=8.15.2 org.label-schema.url=https://www.elastic.co/products/logstash org.label-schema.vcs-url=https://github.com/elastic/logstash org.label-schema.license=Elastic License org.opencontainers.image.licenses=Elastic License org.opencontainers.image.description=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' org.label-schema.build-date=2024-09-17T15:11:45+00:00 org.opencontainers.image.created=2024-09-17T15:11:45+00:00
# Thu, 26 Sep 2024 08:08:51 GMT
ENTRYPOINT ["/usr/local/bin/docker-entrypoint"]
```

-	Layers:
	-	`sha256:6a1df50fc4815789598fa24d3ecacb70451e506447ab9e45665024b9f3f0233b`  
		Last Modified: Tue, 13 Aug 2024 10:23:55 GMT  
		Size: 26.0 MB (25974217 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:525f0c809e52c4ad25ef616a794dacbaffc99ec873be4a4b04baaf67dfc06bf5`  
		Last Modified: Fri, 27 Sep 2024 04:37:29 GMT  
		Size: 38.7 MB (38738405 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35dbdc00fb7962d7932e5ccb71fa96442af5ade5bf7d057c782e20a24859ee4f`  
		Last Modified: Fri, 27 Sep 2024 04:37:27 GMT  
		Size: 1.8 KB (1809 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37a506ca864e096905155f02e3e0430bce2e068ca446b30568c432438c8cf9ee`  
		Last Modified: Fri, 27 Sep 2024 04:37:38 GMT  
		Size: 419.8 MB (419782836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c78df8cd4298f3f636600a27e9b167656783d072065aa53ea2b3061d634301a6`  
		Last Modified: Fri, 27 Sep 2024 04:37:27 GMT  
		Size: 278.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b062872a4e4db1d69e7722317c499014fcaf467f515cff22235aaa4b5b538a7`  
		Last Modified: Fri, 27 Sep 2024 04:37:28 GMT  
		Size: 1.6 KB (1578 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89a4873356872e077071617c540884310ba1e0f955f1aad25c87d8e8aa5b105c`  
		Last Modified: Fri, 27 Sep 2024 04:37:28 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b2c6a15f2db59377c38de9d5f82073700df93822922358274830ee9c0565f10`  
		Last Modified: Fri, 27 Sep 2024 04:37:29 GMT  
		Size: 1.8 KB (1766 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a53a273b9a11315cdc17431b229609fa56a0c1291143e594ba4b49786cba6d23`  
		Last Modified: Fri, 27 Sep 2024 04:37:30 GMT  
		Size: 4.0 MB (3995873 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:827286224cca6e86d2e9969a38ca177cb6cbfa0dbd360dea7e502fac6c91b23e`  
		Last Modified: Fri, 27 Sep 2024 04:37:30 GMT  
		Size: 1.9 MB (1932713 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d7a8e4505935a4b7bfee050de877e4144dae459ebf2a400228642516c825310`  
		Last Modified: Fri, 27 Sep 2024 04:37:30 GMT  
		Size: 712.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `logstash:8.15.2` - unknown; unknown

```console
$ docker pull logstash@sha256:0a05f4c01c284659e3f9156a55ebdcba72e5f33abad5487bac6cefc302cce890
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.4 MB (3431726 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8056d2f2b8f2277e162ff24a91537fa2d2dcd53df921630c9d4cb6cd6d15650d`

```dockerfile
```

-	Layers:
	-	`sha256:06b160024c2adf0fe5798c8c38abcbb2324da896f3774febb908667775c2e142`  
		Last Modified: Fri, 27 Sep 2024 04:37:28 GMT  
		Size: 3.4 MB (3397145 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f1d04485ead12dbc436d93b5e2da985e02cf9ad0bf7891f07778f65b38938043`  
		Last Modified: Fri, 27 Sep 2024 04:37:27 GMT  
		Size: 34.6 KB (34581 bytes)  
		MIME: application/vnd.in-toto+json
