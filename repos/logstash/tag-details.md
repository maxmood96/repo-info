<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `logstash`

-	[`logstash:7.17.25`](#logstash71725)
-	[`logstash:8.15.3`](#logstash8153)

## `logstash:7.17.25`

**does not exist** (yet?)

## `logstash:8.15.3`

```console
$ docker pull logstash@sha256:e9c584e7c54a5f59d56b1a3a3f02753af7918a14978d12e9bcbf73bcd8417202
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `logstash:8.15.3` - linux; amd64

```console
$ docker pull logstash@sha256:1f10c7bcb61cfe267b29e21ebb56a5ca905f9179ee76027d7574ce6572761579
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **506.4 MB (506355449 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1fe62e5af9aeff6aa83741bb7227ec5965a170c834109a6b37e6aaa2bec6b7cd`
-	Entrypoint: `["\/usr\/local\/bin\/docker-entrypoint"]`

```dockerfile
# Fri, 11 Oct 2024 03:38:25 GMT
ARG RELEASE
# Fri, 11 Oct 2024 03:38:25 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 11 Oct 2024 03:38:25 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 11 Oct 2024 03:38:25 GMT
LABEL org.opencontainers.image.version=20.04
# Fri, 11 Oct 2024 03:38:27 GMT
ADD file:7486147a645d8835a5181c79f00a3606c6b714c83bcbfcd8862221eb14690f9e in / 
# Fri, 11 Oct 2024 03:38:27 GMT
CMD ["/bin/bash"]
# Thu, 17 Oct 2024 12:21:47 GMT
RUN for iter in {1..10}; do       export DEBIAN_FRONTEND=noninteractive &&     apt-get update -y &&   apt-get upgrade -y &&   apt-get install -y procps findutils tar gzip &&         apt-get install -y locales &&         apt-get install -y curl &&     apt-get clean all &&       locale-gen 'en_US.UTF-8' &&     apt-get clean metadata &&   exit_code=0 && break || exit_code=$? && echo "packaging error: retry $iter in 10s" && apt-get clean all &&   apt-get clean metadata && sleep 10; done; (exit $exit_code) # buildkit
# Thu, 17 Oct 2024 12:21:47 GMT
RUN groupadd --gid 1000 logstash &&   adduser --uid 1000 --gid 1000 --home /usr/share/logstash --no-create-home logstash # buildkit
# Thu, 17 Oct 2024 12:21:47 GMT
RUN curl -Lo - https://artifacts.elastic.co/downloads/logstash/logstash-8.15.3-linux-$(arch).tar.gz |   tar zxf - -C /usr/share &&   mv /usr/share/logstash-8.15.3 /usr/share/logstash &&   chown --recursive logstash:logstash /usr/share/logstash/ &&   chown -R logstash:root /usr/share/logstash &&   chmod -R g=u /usr/share/logstash &&   mkdir /licenses/ &&   mv /usr/share/logstash/NOTICE.TXT /licenses/NOTICE.TXT &&   mv /usr/share/logstash/LICENSE.txt /licenses/LICENSE.txt &&   find /usr/share/logstash -type d -exec chmod g+s {} \; &&   ln -s /usr/share/logstash /opt/logstash # buildkit
# Thu, 17 Oct 2024 12:21:47 GMT
WORKDIR /usr/share/logstash
# Thu, 17 Oct 2024 12:21:47 GMT
ENV ELASTIC_CONTAINER=true
# Thu, 17 Oct 2024 12:21:47 GMT
ENV PATH=/usr/share/logstash/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 17 Oct 2024 12:21:47 GMT
COPY config/logstash-full.yml config/logstash.yml # buildkit
# Thu, 17 Oct 2024 12:21:47 GMT
COPY config/pipelines.yml config/log4j2.properties config/log4j2.file.properties config/ # buildkit
# Thu, 17 Oct 2024 12:21:47 GMT
COPY pipeline/default.conf pipeline/logstash.conf # buildkit
# Thu, 17 Oct 2024 12:21:47 GMT
RUN chown --recursive logstash:root config/ pipeline/ # buildkit
# Thu, 17 Oct 2024 12:21:47 GMT
ENV LANG=en_US.UTF-8 LC_ALL=en_US.UTF-8
# Thu, 17 Oct 2024 12:21:47 GMT
COPY env2yaml/env2yaml-amd64 env2yaml/env2yaml-arm64 env2yaml/ # buildkit
# Thu, 17 Oct 2024 12:21:47 GMT
RUN env2yamlarch="$(dpkg --print-architecture)";   case "${env2yamlarch}" in     'x86_64'|'amd64')       env2yamlarch=amd64;       ;;     'aarch64'|'arm64')       env2yamlarch=arm64;       ;;     *) echo >&2 "error: unsupported architecture '$env2yamlarch'"; exit 1 ;;   esac;   mkdir -p /usr/local/bin;   cp env2yaml/env2yaml-${env2yamlarch} /usr/local/bin/env2yaml;   rm -rf env2yaml # buildkit
# Thu, 17 Oct 2024 12:21:47 GMT
COPY bin/docker-entrypoint /usr/local/bin/ # buildkit
# Thu, 17 Oct 2024 12:21:47 GMT
RUN chmod 0755 /usr/local/bin/docker-entrypoint # buildkit
# Thu, 17 Oct 2024 12:21:47 GMT
USER 1000
# Thu, 17 Oct 2024 12:21:47 GMT
EXPOSE map[5044/tcp:{} 9600/tcp:{}]
# Thu, 17 Oct 2024 12:21:47 GMT
LABEL org.label-schema.schema-version=1.0 org.label-schema.vendor=Elastic org.opencontainers.image.vendor=Elastic org.label-schema.name=logstash org.opencontainers.image.title=logstash org.label-schema.version=8.15.3 org.opencontainers.image.version=8.15.3 org.label-schema.url=https://www.elastic.co/products/logstash org.label-schema.vcs-url=https://github.com/elastic/logstash org.label-schema.license=Elastic License org.opencontainers.image.licenses=Elastic License org.opencontainers.image.description=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' org.label-schema.build-date=2024-10-08T16:06:14+00:00 org.opencontainers.image.created=2024-10-08T16:06:14+00:00
# Thu, 17 Oct 2024 12:21:47 GMT
ENTRYPOINT ["/usr/local/bin/docker-entrypoint"]
```

-	Layers:
	-	`sha256:d9802f032d6798e2086607424bfe88cb8ec1d6f116e11cd99592dcaf261e9cd2`  
		Last Modified: Fri, 11 Oct 2024 04:41:25 GMT  
		Size: 27.5 MB (27511060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ea98d10c2cddc08a4a118d3b6d0c6105acd13da5f697aba23ac9490713b7901`  
		Last Modified: Thu, 17 Oct 2024 20:59:21 GMT  
		Size: 50.2 MB (50203370 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c692d5a1244728c73b78455d73be73fdabab85266d2b839f1ae7f6128492fe8`  
		Last Modified: Thu, 17 Oct 2024 20:59:20 GMT  
		Size: 1.8 KB (1803 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aca356e735bae81f2212307c80c87253e91f7b7cc3d159795909e2fe59537f08`  
		Last Modified: Thu, 17 Oct 2024 20:59:26 GMT  
		Size: 422.6 MB (422575765 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3454ff7c6dbad80fc9ae756e2798edd06445d21e13b5e3d1d80ffdc60c28c06`  
		Last Modified: Thu, 17 Oct 2024 20:59:20 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d416e980a959bc33ffaa1f7b60b34169be87cec4f54a2e38696702d6ef687a0`  
		Last Modified: Thu, 17 Oct 2024 20:59:21 GMT  
		Size: 1.6 KB (1578 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57e167900bdd3006653b4dd141acf697006700d41effcb8f14e6dfc26813d933`  
		Last Modified: Thu, 17 Oct 2024 20:59:21 GMT  
		Size: 278.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:421832b8f4ac099ad24a158f06b8b91a8b962ac943f95e45dcc103e2a9546cac`  
		Last Modified: Thu, 17 Oct 2024 20:59:22 GMT  
		Size: 1.8 KB (1765 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac661e059e18181bf57be7789fdf96dbff69c5cbd60fcae0a7654a9932b7f8a7`  
		Last Modified: Thu, 17 Oct 2024 20:59:22 GMT  
		Size: 4.0 MB (3997025 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:257a94b584e0e83208cfba6e5b1a75ddbcb1e2379020a63808ab309394a0d6fb`  
		Last Modified: Thu, 17 Oct 2024 20:59:23 GMT  
		Size: 2.1 MB (2061753 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a9b00de5df8cb48b25b59821ab8bfb10cc64b261ea0222b9d37100e6120ef81`  
		Last Modified: Thu, 17 Oct 2024 20:59:23 GMT  
		Size: 712.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `logstash:8.15.3` - unknown; unknown

```console
$ docker pull logstash@sha256:868332a845b12cb3aadf0174f9b44107b3a380d856b09dcf9766ed6e65171905
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.4 MB (3435280 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4914b4640544acbcaeaafe150854cb9e83253ffd52fd10b6dbeac06df22ac552`

```dockerfile
```

-	Layers:
	-	`sha256:f15d81b8311925b1175dd46fa53600d49a18586515fdf6d6efbed5c7ec5614f2`  
		Last Modified: Thu, 17 Oct 2024 20:59:20 GMT  
		Size: 3.4 MB (3400925 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4fa1cbc1168161e9d4b8c563aac964f86e7b23d943f58a6850469f6d369dd09e`  
		Last Modified: Thu, 17 Oct 2024 20:59:20 GMT  
		Size: 34.4 KB (34355 bytes)  
		MIME: application/vnd.in-toto+json

### `logstash:8.15.3` - linux; arm64 variant v8

```console
$ docker pull logstash@sha256:8296992de05a249067ab0e0cf9a7f9af3f084c3b415d950fa0da7fa7a5acb915
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **491.0 MB (491031712 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dc94175444da27f95df57340ae93c90db6fb50f8052fadcabcf21458830354cb`
-	Entrypoint: `["\/usr\/local\/bin\/docker-entrypoint"]`

```dockerfile
# Fri, 11 Oct 2024 03:39:45 GMT
ARG RELEASE
# Fri, 11 Oct 2024 03:39:45 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 11 Oct 2024 03:39:45 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 11 Oct 2024 03:39:45 GMT
LABEL org.opencontainers.image.version=20.04
# Fri, 11 Oct 2024 03:39:47 GMT
ADD file:8537b4db344382b39d669af27cd94ec0f870ceafe58c67ee54e3f9b38fb8d671 in / 
# Fri, 11 Oct 2024 03:39:47 GMT
CMD ["/bin/bash"]
# Thu, 17 Oct 2024 12:21:47 GMT
RUN for iter in {1..10}; do       export DEBIAN_FRONTEND=noninteractive &&     apt-get update -y &&   apt-get upgrade -y &&   apt-get install -y procps findutils tar gzip &&         apt-get install -y locales &&         apt-get install -y curl &&     apt-get clean all &&       locale-gen 'en_US.UTF-8' &&     apt-get clean metadata &&   exit_code=0 && break || exit_code=$? && echo "packaging error: retry $iter in 10s" && apt-get clean all &&   apt-get clean metadata && sleep 10; done; (exit $exit_code) # buildkit
# Thu, 17 Oct 2024 12:21:47 GMT
RUN groupadd --gid 1000 logstash &&   adduser --uid 1000 --gid 1000 --home /usr/share/logstash --no-create-home logstash # buildkit
# Thu, 17 Oct 2024 12:21:47 GMT
RUN curl -Lo - https://artifacts.elastic.co/downloads/logstash/logstash-8.15.3-linux-$(arch).tar.gz |   tar zxf - -C /usr/share &&   mv /usr/share/logstash-8.15.3 /usr/share/logstash &&   chown --recursive logstash:logstash /usr/share/logstash/ &&   chown -R logstash:root /usr/share/logstash &&   chmod -R g=u /usr/share/logstash &&   mkdir /licenses/ &&   mv /usr/share/logstash/NOTICE.TXT /licenses/NOTICE.TXT &&   mv /usr/share/logstash/LICENSE.txt /licenses/LICENSE.txt &&   find /usr/share/logstash -type d -exec chmod g+s {} \; &&   ln -s /usr/share/logstash /opt/logstash # buildkit
# Thu, 17 Oct 2024 12:21:47 GMT
WORKDIR /usr/share/logstash
# Thu, 17 Oct 2024 12:21:47 GMT
ENV ELASTIC_CONTAINER=true
# Thu, 17 Oct 2024 12:21:47 GMT
ENV PATH=/usr/share/logstash/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 17 Oct 2024 12:21:47 GMT
COPY config/logstash-full.yml config/logstash.yml # buildkit
# Thu, 17 Oct 2024 12:21:47 GMT
COPY config/pipelines.yml config/log4j2.properties config/log4j2.file.properties config/ # buildkit
# Thu, 17 Oct 2024 12:21:47 GMT
COPY pipeline/default.conf pipeline/logstash.conf # buildkit
# Thu, 17 Oct 2024 12:21:47 GMT
RUN chown --recursive logstash:root config/ pipeline/ # buildkit
# Thu, 17 Oct 2024 12:21:47 GMT
ENV LANG=en_US.UTF-8 LC_ALL=en_US.UTF-8
# Thu, 17 Oct 2024 12:21:47 GMT
COPY env2yaml/env2yaml-amd64 env2yaml/env2yaml-arm64 env2yaml/ # buildkit
# Thu, 17 Oct 2024 12:21:47 GMT
RUN env2yamlarch="$(dpkg --print-architecture)";   case "${env2yamlarch}" in     'x86_64'|'amd64')       env2yamlarch=amd64;       ;;     'aarch64'|'arm64')       env2yamlarch=arm64;       ;;     *) echo >&2 "error: unsupported architecture '$env2yamlarch'"; exit 1 ;;   esac;   mkdir -p /usr/local/bin;   cp env2yaml/env2yaml-${env2yamlarch} /usr/local/bin/env2yaml;   rm -rf env2yaml # buildkit
# Thu, 17 Oct 2024 12:21:47 GMT
COPY bin/docker-entrypoint /usr/local/bin/ # buildkit
# Thu, 17 Oct 2024 12:21:47 GMT
RUN chmod 0755 /usr/local/bin/docker-entrypoint # buildkit
# Thu, 17 Oct 2024 12:21:47 GMT
USER 1000
# Thu, 17 Oct 2024 12:21:47 GMT
EXPOSE map[5044/tcp:{} 9600/tcp:{}]
# Thu, 17 Oct 2024 12:21:47 GMT
LABEL org.label-schema.schema-version=1.0 org.label-schema.vendor=Elastic org.opencontainers.image.vendor=Elastic org.label-schema.name=logstash org.opencontainers.image.title=logstash org.label-schema.version=8.15.3 org.opencontainers.image.version=8.15.3 org.label-schema.url=https://www.elastic.co/products/logstash org.label-schema.vcs-url=https://github.com/elastic/logstash org.label-schema.license=Elastic License org.opencontainers.image.licenses=Elastic License org.opencontainers.image.description=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' org.label-schema.build-date=2024-10-08T16:06:14+00:00 org.opencontainers.image.created=2024-10-08T16:06:14+00:00
# Thu, 17 Oct 2024 12:21:47 GMT
ENTRYPOINT ["/usr/local/bin/docker-entrypoint"]
```

-	Layers:
	-	`sha256:1b9f3c55f9d4aa5c52eb67a4cb7d0f4726ab85a413b50e3e3fe788befce3d297`  
		Last Modified: Fri, 11 Oct 2024 04:41:30 GMT  
		Size: 26.0 MB (25973828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50a885b0211a43d804aed6dd355647df7a51390a8987bfa94d2bc2dc61ff599c`  
		Last Modified: Wed, 16 Oct 2024 03:36:19 GMT  
		Size: 38.4 MB (38371505 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cfbf5c9ada372334204f621439e5fb28ef525da9372c35c689e4d9bcdd2e3197`  
		Last Modified: Wed, 16 Oct 2024 03:36:18 GMT  
		Size: 1.8 KB (1809 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d8ec2b910729266f502e6a476f5207d7da5869f2f115f50060b2644266da783`  
		Last Modified: Thu, 17 Oct 2024 22:22:35 GMT  
		Size: 420.7 MB (420749476 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5c6c31fbfb5fd3725320dc3b3c9692718f6e473f3cbe4500da6762ecca2e53f`  
		Last Modified: Thu, 17 Oct 2024 22:22:26 GMT  
		Size: 274.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d253c92098177faf6220d827801fed4f7850f2fd92b973f4662221e8a268968f`  
		Last Modified: Thu, 17 Oct 2024 22:22:26 GMT  
		Size: 1.6 KB (1578 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e47cfbb41d5a05f67f28230be204fd448ea51ab1cb6c7c1baa282d7fccda8fc`  
		Last Modified: Thu, 17 Oct 2024 22:22:26 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9677ea5582d44bd4c3dec770bd34ccd3ed888d7540916ed9c4e7d91034544ecf`  
		Last Modified: Thu, 17 Oct 2024 22:22:27 GMT  
		Size: 1.8 KB (1764 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e16aa31c894b1d6e99cbc8e1b9fe662d5f258f1234a3a3107a7a11740660b9fb`  
		Last Modified: Thu, 17 Oct 2024 22:22:27 GMT  
		Size: 4.0 MB (3997022 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5c9d22509209078c415186fe73a30f690aacc76505201f540df8071a1751196`  
		Last Modified: Thu, 17 Oct 2024 22:22:27 GMT  
		Size: 1.9 MB (1933407 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:632d996ad56bdf53ebcc29e734a8c5a6770ff090fdcc605f344e9f9ed4f3a7f7`  
		Last Modified: Thu, 17 Oct 2024 22:22:28 GMT  
		Size: 708.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `logstash:8.15.3` - unknown; unknown

```console
$ docker pull logstash@sha256:93de7eeb86e5b87336a5c145b163bb6a7b18e01b5b0a5a26d7ba4108dd7869f2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.4 MB (3435027 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2316e0ee359a7baa8cd3cc308328de8830486d312af41f14fe83c542a2ca03ea`

```dockerfile
```

-	Layers:
	-	`sha256:a22c6a54f481a1ccface5e1c828e8552b5fd85b1ad43e12ba7eebfbb3df14227`  
		Last Modified: Thu, 17 Oct 2024 22:22:26 GMT  
		Size: 3.4 MB (3400535 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:789ea3278c5d802e96c91c7dfa6450b98d8e1bfe4f4e079d5c0c39a147b86848`  
		Last Modified: Thu, 17 Oct 2024 22:22:26 GMT  
		Size: 34.5 KB (34492 bytes)  
		MIME: application/vnd.in-toto+json
