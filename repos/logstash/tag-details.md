<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `logstash`

-	[`logstash:7.17.28`](#logstash71728)
-	[`logstash:8.16.4`](#logstash8164)
-	[`logstash:8.17.2`](#logstash8172)

## `logstash:7.17.28`

```console
$ docker pull logstash@sha256:081585e5240939628fd78a804d9de13f1db65494318e12a06040c91098a95fc1
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `logstash:7.17.28` - linux; amd64

```console
$ docker pull logstash@sha256:de6b285d788251f25292379fab827a41277458b09576b413addb118f795016f4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **464.3 MB (464341941 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:53627a5ce7615cba4ac9e9d3502b8935200466c7653129ce8fb77a0f9225d0a6`
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
# Tue, 25 Feb 2025 11:58:14 GMT
RUN for iter in {1..10}; do     export DEBIAN_FRONTEND=noninteractive &&     apt-get update -y &&     apt-get upgrade -y &&     apt-get install -y procps findutils tar gzip curl &&     apt-get install -y locales &&     apt-get clean all &&     locale-gen 'en_US.UTF-8' &&     apt-get clean metadata &&     exit_code=0 && break || exit_code=$? &&     echo "packaging error: retry $iter in 10s" &&     apt-get clean all &&     apt-get clean metadata &&     sleep 10; done;     (exit $exit_code) # buildkit
# Tue, 25 Feb 2025 11:58:14 GMT
RUN groupadd --gid 1000 logstash &&     adduser --uid 1000 --gid 1000     --home /usr/share/logstash --no-create-home     logstash # buildkit
# Tue, 25 Feb 2025 11:58:14 GMT
RUN curl -Lo - https://artifacts.elastic.co/downloads/logstash/logstash-7.17.28-linux-$(arch).tar.gz |     tar zxf - -C /usr/share &&     mv /usr/share/logstash-7.17.28 /usr/share/logstash &&     chown --recursive logstash:logstash /usr/share/logstash/ &&     chown -R logstash:root /usr/share/logstash &&     chmod -R g=u /usr/share/logstash &&     mkdir /licenses/ &&     mv /usr/share/logstash/NOTICE.TXT /licenses/NOTICE.TXT &&     mv /usr/share/logstash/LICENSE.txt /licenses/LICENSE.txt &&     find /usr/share/logstash -type d -exec chmod g+s {} \; &&     ln -s /usr/share/logstash /opt/logstash # buildkit
# Tue, 25 Feb 2025 11:58:14 GMT
WORKDIR /usr/share/logstash
# Tue, 25 Feb 2025 11:58:14 GMT
ENV ELASTIC_CONTAINER=true
# Tue, 25 Feb 2025 11:58:14 GMT
ENV PATH=/usr/share/logstash/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 25 Feb 2025 11:58:14 GMT
COPY config/pipelines.yml config/pipelines.yml # buildkit
# Tue, 25 Feb 2025 11:58:14 GMT
COPY config/logstash-full.yml config/logstash.yml # buildkit
# Tue, 25 Feb 2025 11:58:14 GMT
COPY config/log4j2.properties config/ # buildkit
# Tue, 25 Feb 2025 11:58:14 GMT
COPY pipeline/default.conf pipeline/logstash.conf # buildkit
# Tue, 25 Feb 2025 11:58:14 GMT
RUN chown --recursive logstash:root config/ pipeline/ # buildkit
# Tue, 25 Feb 2025 11:58:14 GMT
ENV LANG=en_US.UTF-8 LC_ALL=en_US.UTF-8
# Tue, 25 Feb 2025 11:58:14 GMT
COPY env2yaml/env2yaml /usr/local/bin/ # buildkit
# Tue, 25 Feb 2025 11:58:14 GMT
COPY bin/docker-entrypoint /usr/local/bin/ # buildkit
# Tue, 25 Feb 2025 11:58:14 GMT
RUN chmod 0755 /usr/local/bin/docker-entrypoint # buildkit
# Tue, 25 Feb 2025 11:58:14 GMT
USER 1000
# Tue, 25 Feb 2025 11:58:14 GMT
EXPOSE map[5044/tcp:{} 9600/tcp:{}]
# Tue, 25 Feb 2025 11:58:14 GMT
LABEL org.label-schema.schema-version=1.0 org.label-schema.vendor=Elastic org.opencontainers.image.vendor=Elastic org.label-schema.name=logstash org.opencontainers.image.title=logstash org.label-schema.version=7.17.28 org.opencontainers.image.version=7.17.28 org.label-schema.url=https://www.elastic.co/products/logstash org.label-schema.vcs-url=https://github.com/elastic/logstash org.label-schema.license=Elastic License org.opencontainers.image.licenses=Elastic License org.opencontainers.image.description=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' org.label-schema.build-date=2025-02-18T11:10:52+00:00 org.opencontainers.image.created=2025-02-18T11:10:52+00:00
# Tue, 25 Feb 2025 11:58:14 GMT
ENTRYPOINT ["/usr/local/bin/docker-entrypoint"]
```

-	Layers:
	-	`sha256:d9802f032d6798e2086607424bfe88cb8ec1d6f116e11cd99592dcaf261e9cd2`  
		Last Modified: Fri, 11 Oct 2024 04:41:25 GMT  
		Size: 27.5 MB (27511060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7fa420d335f3713906f433d6bf4dfd9c0a99ffd7e76a1aa9967d121be4490525`  
		Last Modified: Tue, 25 Feb 2025 18:30:25 GMT  
		Size: 58.8 MB (58778290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb8220629431ab959867b9485651d632cbbf8f2bfcdca3c11ec25bbd3eb898c1`  
		Last Modified: Tue, 25 Feb 2025 18:30:23 GMT  
		Size: 1.8 KB (1807 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e5a6259a94a5f00a05d92857343361e6925f135cc677bb8a817905dc31b26b4`  
		Last Modified: Tue, 25 Feb 2025 18:30:31 GMT  
		Size: 376.0 MB (375953444 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a422f86892721325b7a63d6b7f6ddb89f5a45b96fca1e1c0c3001d47921f6a2`  
		Last Modified: Tue, 25 Feb 2025 18:30:23 GMT  
		Size: 381.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d30e0419630d19668cae284de7a14a50c5445516ac19d779fd31d2bfa7825cb4`  
		Last Modified: Tue, 25 Feb 2025 18:30:24 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9020270f69b021a95f828bf5b59569fe206e870581d81145052f366e849e1740`  
		Last Modified: Tue, 25 Feb 2025 18:30:24 GMT  
		Size: 475.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccccf2d311031460940d1a476160bdcbd0899080409210c301efdab4d030327b`  
		Last Modified: Tue, 25 Feb 2025 18:30:25 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53fcc992e562aafafa3a1b0ff5d8f548c3273a982332222c4ffb0201110a27c6`  
		Last Modified: Tue, 25 Feb 2025 18:30:25 GMT  
		Size: 828.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37a0115e049b03c682a09c9d34f7565f1b3a27e64b4b128c96fb3acce953d4b7`  
		Last Modified: Tue, 25 Feb 2025 18:30:27 GMT  
		Size: 2.1 MB (2094544 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5c02e13fcdcb13e171d8ef7e2a6f2526ce5a5b7de450483cdbb2662a76b6ffa`  
		Last Modified: Tue, 25 Feb 2025 18:30:26 GMT  
		Size: 492.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `logstash:7.17.28` - unknown; unknown

```console
$ docker pull logstash@sha256:4df7c51a5587e318157e974ab209cee513f292de905a206e0ad54d7e61e759d6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.4 MB (3371932 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b05173e19748c4423dc15ee3a7b697cf45661932d0d54a43534053f69a8ecc2d`

```dockerfile
```

-	Layers:
	-	`sha256:83c621ff44a3ca1084b78aa5fef2657963dd6d8009e8aa6b9496210f9110b024`  
		Last Modified: Tue, 25 Feb 2025 18:30:24 GMT  
		Size: 3.3 MB (3339746 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4595b18937007ca4e2f81a8e35f6bc732c39a72ad415639d6899f7fc5fa433dc`  
		Last Modified: Tue, 25 Feb 2025 18:30:23 GMT  
		Size: 32.2 KB (32186 bytes)  
		MIME: application/vnd.in-toto+json

## `logstash:8.16.4`

```console
$ docker pull logstash@sha256:f44375526aeccbf692008a558a84c8cb2a9f996d4ea79e61b1c114d779977b80
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `logstash:8.16.4` - linux; amd64

```console
$ docker pull logstash@sha256:4111ae0703e3336bc6a67e63feae63313fd56aeac547b341157c92fcd309df14
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **529.6 MB (529583575 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:913ce58aa39e4b188acf5c753b0010347f64635ee50db5c69d4529c9cd84a372`
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
# Tue, 11 Feb 2025 12:46:24 GMT
RUN for iter in {1..10}; do       export DEBIAN_FRONTEND=noninteractive &&     apt-get update -y &&   apt-get upgrade -y &&   apt-get install -y procps findutils tar gzip &&         apt-get install -y locales &&         apt-get install -y curl &&     apt-get clean all &&       locale-gen 'en_US.UTF-8' &&     apt-get clean metadata &&   exit_code=0 && break || exit_code=$? && echo "packaging error: retry $iter in 10s" && apt-get clean all &&   apt-get clean metadata && sleep 10; done; (exit $exit_code) # buildkit
# Tue, 11 Feb 2025 12:46:24 GMT
RUN groupadd --gid 1000 logstash &&   adduser --uid 1000 --gid 1000 --home /usr/share/logstash --no-create-home logstash # buildkit
# Tue, 11 Feb 2025 12:46:24 GMT
RUN curl -Lo - https://artifacts.elastic.co/downloads/logstash/logstash-8.16.4-linux-$(arch).tar.gz |   tar zxf - -C /usr/share &&   mv /usr/share/logstash-8.16.4 /usr/share/logstash &&   chown --recursive logstash:logstash /usr/share/logstash/ &&   chown -R logstash:root /usr/share/logstash &&   chmod -R g=u /usr/share/logstash &&   mkdir /licenses/ &&   mv /usr/share/logstash/NOTICE.TXT /licenses/NOTICE.TXT &&   mv /usr/share/logstash/LICENSE.txt /licenses/LICENSE.txt &&   find /usr/share/logstash -type d -exec chmod g+s {} \; &&   ln -s /usr/share/logstash /opt/logstash # buildkit
# Tue, 11 Feb 2025 12:46:24 GMT
WORKDIR /usr/share/logstash
# Tue, 11 Feb 2025 12:46:24 GMT
ENV ELASTIC_CONTAINER=true
# Tue, 11 Feb 2025 12:46:24 GMT
ENV PATH=/usr/share/logstash/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 11 Feb 2025 12:46:24 GMT
COPY config/logstash-full.yml config/logstash.yml # buildkit
# Tue, 11 Feb 2025 12:46:24 GMT
COPY config/pipelines.yml config/log4j2.properties config/log4j2.file.properties config/ # buildkit
# Tue, 11 Feb 2025 12:46:24 GMT
COPY pipeline/default.conf pipeline/logstash.conf # buildkit
# Tue, 11 Feb 2025 12:46:24 GMT
RUN chown --recursive logstash:root config/ pipeline/ # buildkit
# Tue, 11 Feb 2025 12:46:24 GMT
ENV LANG=en_US.UTF-8 LC_ALL=en_US.UTF-8
# Tue, 11 Feb 2025 12:46:24 GMT
COPY env2yaml/env2yaml-amd64 env2yaml/env2yaml-arm64 env2yaml/ # buildkit
# Tue, 11 Feb 2025 12:46:24 GMT
RUN env2yamlarch="$(dpkg --print-architecture)";   case "${env2yamlarch}" in     'x86_64'|'amd64')       env2yamlarch=amd64;       ;;     'aarch64'|'arm64')       env2yamlarch=arm64;       ;;     *) echo >&2 "error: unsupported architecture '$env2yamlarch'"; exit 1 ;;   esac;   mkdir -p /usr/local/bin;   cp env2yaml/env2yaml-${env2yamlarch} /usr/local/bin/env2yaml;   rm -rf env2yaml # buildkit
# Tue, 11 Feb 2025 12:46:24 GMT
COPY bin/docker-entrypoint /usr/local/bin/ # buildkit
# Tue, 11 Feb 2025 12:46:24 GMT
RUN chmod 0755 /usr/local/bin/docker-entrypoint # buildkit
# Tue, 11 Feb 2025 12:46:24 GMT
USER 1000
# Tue, 11 Feb 2025 12:46:24 GMT
EXPOSE map[5044/tcp:{} 9600/tcp:{}]
# Tue, 11 Feb 2025 12:46:24 GMT
LABEL org.label-schema.schema-version=1.0 org.label-schema.vendor=Elastic org.opencontainers.image.vendor=Elastic org.label-schema.name=logstash org.opencontainers.image.title=logstash org.label-schema.version=8.16.4 org.opencontainers.image.version=8.16.4 org.label-schema.url=https://www.elastic.co/products/logstash org.label-schema.vcs-url=https://github.com/elastic/logstash org.label-schema.license=Elastic License org.opencontainers.image.licenses=Elastic License org.opencontainers.image.description=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' org.label-schema.build-date=2025-02-05T18:47:51+00:00 org.opencontainers.image.created=2025-02-05T18:47:51+00:00
# Tue, 11 Feb 2025 12:46:24 GMT
ENTRYPOINT ["/usr/local/bin/docker-entrypoint"]
```

-	Layers:
	-	`sha256:d9802f032d6798e2086607424bfe88cb8ec1d6f116e11cd99592dcaf261e9cd2`  
		Last Modified: Fri, 11 Oct 2024 04:41:25 GMT  
		Size: 27.5 MB (27511060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:673e49f0148fedbac5c18ce0120683b7f360670e7c58872768911d3209806aaf`  
		Last Modified: Tue, 11 Feb 2025 19:30:16 GMT  
		Size: 57.7 MB (57729045 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c4ab29b63179eabb60324ee92398e947705fb1940d883f2fe2536077d04bb4d`  
		Last Modified: Tue, 11 Feb 2025 19:30:15 GMT  
		Size: 1.8 KB (1805 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:190911b25f5cb3f2c330912c5e15500a336bbf68219019c6358faedaf144ff40`  
		Last Modified: Tue, 11 Feb 2025 19:30:28 GMT  
		Size: 438.3 MB (438269071 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e578f6fa8c9559aabacbf758175295ae893df7c2e313ba95d7573ee59e81380`  
		Last Modified: Tue, 11 Feb 2025 19:30:15 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b21d7db151587e06fb40b1fa173aa2464dc40c25d420aef4f0bf6e0cb7f63ad`  
		Last Modified: Tue, 11 Feb 2025 19:30:16 GMT  
		Size: 1.6 KB (1580 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5486f7e2c5f76ba68d3b9978af05c596a23ecf0a667c72f5a1bd6e2e4a72036`  
		Last Modified: Tue, 11 Feb 2025 19:30:16 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d6631f989db1c046a4d2b33ed9963dbe463b9f553f15245e477f59964ba998d`  
		Last Modified: Tue, 11 Feb 2025 19:30:17 GMT  
		Size: 1.8 KB (1765 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1dd1ccd757063671a96257d0d236a62aee870dee7b3aa1ecc987b83b24d85a17`  
		Last Modified: Tue, 11 Feb 2025 19:30:17 GMT  
		Size: 4.0 MB (4002549 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49a0fc59212173e7baba9cf72f0178f9c8d19b8b8b9a34cda33c55d061da2737`  
		Last Modified: Tue, 11 Feb 2025 19:30:17 GMT  
		Size: 2.1 MB (2065365 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a40cd1128f19d036c68826c77d5385cabfc4d80ab8e6aa3f7a282034443a2522`  
		Last Modified: Tue, 11 Feb 2025 19:30:18 GMT  
		Size: 711.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `logstash:8.16.4` - unknown; unknown

```console
$ docker pull logstash@sha256:f6bab828c80c1e232bb3e1a8d2d72c84ce8776d7c1122f79749ec8906073a154
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3554590 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5222cb2a4576c6d19b0060fda1ffdf1641f3dd4d8361b5f8f2c211a105fcfb7c`

```dockerfile
```

-	Layers:
	-	`sha256:f3d4c6d6e4418fe82382857558341222f96fed9aa76f9f1555c15ac621c4a95e`  
		Last Modified: Tue, 11 Feb 2025 19:30:15 GMT  
		Size: 3.5 MB (3520019 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9e414fee78a7c0e80e913b2a811de29bbd621d6596437b3354a2eca609002b31`  
		Last Modified: Tue, 11 Feb 2025 19:30:15 GMT  
		Size: 34.6 KB (34571 bytes)  
		MIME: application/vnd.in-toto+json

### `logstash:8.16.4` - linux; arm64 variant v8

```console
$ docker pull logstash@sha256:a051a3ddd0d7d0c40a5646d4a7688cb9cfc450379e3c8ea47a633c5cc585c2b8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **512.8 MB (512768325 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:958b74aff4e8cda145c47024112aaaeb560654c6000e8e796c0de004f5b12b7b`
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
# Tue, 11 Feb 2025 12:46:24 GMT
RUN for iter in {1..10}; do       export DEBIAN_FRONTEND=noninteractive &&     apt-get update -y &&   apt-get upgrade -y &&   apt-get install -y procps findutils tar gzip &&         apt-get install -y locales &&         apt-get install -y curl &&     apt-get clean all &&       locale-gen 'en_US.UTF-8' &&     apt-get clean metadata &&   exit_code=0 && break || exit_code=$? && echo "packaging error: retry $iter in 10s" && apt-get clean all &&   apt-get clean metadata && sleep 10; done; (exit $exit_code) # buildkit
# Tue, 11 Feb 2025 12:46:24 GMT
RUN groupadd --gid 1000 logstash &&   adduser --uid 1000 --gid 1000 --home /usr/share/logstash --no-create-home logstash # buildkit
# Tue, 11 Feb 2025 12:46:24 GMT
RUN curl -Lo - https://artifacts.elastic.co/downloads/logstash/logstash-8.16.4-linux-$(arch).tar.gz |   tar zxf - -C /usr/share &&   mv /usr/share/logstash-8.16.4 /usr/share/logstash &&   chown --recursive logstash:logstash /usr/share/logstash/ &&   chown -R logstash:root /usr/share/logstash &&   chmod -R g=u /usr/share/logstash &&   mkdir /licenses/ &&   mv /usr/share/logstash/NOTICE.TXT /licenses/NOTICE.TXT &&   mv /usr/share/logstash/LICENSE.txt /licenses/LICENSE.txt &&   find /usr/share/logstash -type d -exec chmod g+s {} \; &&   ln -s /usr/share/logstash /opt/logstash # buildkit
# Tue, 11 Feb 2025 12:46:24 GMT
WORKDIR /usr/share/logstash
# Tue, 11 Feb 2025 12:46:24 GMT
ENV ELASTIC_CONTAINER=true
# Tue, 11 Feb 2025 12:46:24 GMT
ENV PATH=/usr/share/logstash/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 11 Feb 2025 12:46:24 GMT
COPY config/logstash-full.yml config/logstash.yml # buildkit
# Tue, 11 Feb 2025 12:46:24 GMT
COPY config/pipelines.yml config/log4j2.properties config/log4j2.file.properties config/ # buildkit
# Tue, 11 Feb 2025 12:46:24 GMT
COPY pipeline/default.conf pipeline/logstash.conf # buildkit
# Tue, 11 Feb 2025 12:46:24 GMT
RUN chown --recursive logstash:root config/ pipeline/ # buildkit
# Tue, 11 Feb 2025 12:46:24 GMT
ENV LANG=en_US.UTF-8 LC_ALL=en_US.UTF-8
# Tue, 11 Feb 2025 12:46:24 GMT
COPY env2yaml/env2yaml-amd64 env2yaml/env2yaml-arm64 env2yaml/ # buildkit
# Tue, 11 Feb 2025 12:46:24 GMT
RUN env2yamlarch="$(dpkg --print-architecture)";   case "${env2yamlarch}" in     'x86_64'|'amd64')       env2yamlarch=amd64;       ;;     'aarch64'|'arm64')       env2yamlarch=arm64;       ;;     *) echo >&2 "error: unsupported architecture '$env2yamlarch'"; exit 1 ;;   esac;   mkdir -p /usr/local/bin;   cp env2yaml/env2yaml-${env2yamlarch} /usr/local/bin/env2yaml;   rm -rf env2yaml # buildkit
# Tue, 11 Feb 2025 12:46:24 GMT
COPY bin/docker-entrypoint /usr/local/bin/ # buildkit
# Tue, 11 Feb 2025 12:46:24 GMT
RUN chmod 0755 /usr/local/bin/docker-entrypoint # buildkit
# Tue, 11 Feb 2025 12:46:24 GMT
USER 1000
# Tue, 11 Feb 2025 12:46:24 GMT
EXPOSE map[5044/tcp:{} 9600/tcp:{}]
# Tue, 11 Feb 2025 12:46:24 GMT
LABEL org.label-schema.schema-version=1.0 org.label-schema.vendor=Elastic org.opencontainers.image.vendor=Elastic org.label-schema.name=logstash org.opencontainers.image.title=logstash org.label-schema.version=8.16.4 org.opencontainers.image.version=8.16.4 org.label-schema.url=https://www.elastic.co/products/logstash org.label-schema.vcs-url=https://github.com/elastic/logstash org.label-schema.license=Elastic License org.opencontainers.image.licenses=Elastic License org.opencontainers.image.description=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' org.label-schema.build-date=2025-02-05T18:47:51+00:00 org.opencontainers.image.created=2025-02-05T18:47:51+00:00
# Tue, 11 Feb 2025 12:46:24 GMT
ENTRYPOINT ["/usr/local/bin/docker-entrypoint"]
```

-	Layers:
	-	`sha256:1b9f3c55f9d4aa5c52eb67a4cb7d0f4726ab85a413b50e3e3fe788befce3d297`  
		Last Modified: Fri, 11 Oct 2024 04:41:30 GMT  
		Size: 26.0 MB (25973828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7651092bb7bf62c6844dc81b0a938d4067dd5bafe70c6ed10922a5aaf08eff87`  
		Last Modified: Tue, 11 Feb 2025 19:49:17 GMT  
		Size: 44.3 MB (44294656 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ef0a54360ec84df15a8be824f6cbdcc417fb33f38f49de22a02735cd175287f`  
		Last Modified: Tue, 11 Feb 2025 19:49:15 GMT  
		Size: 1.8 KB (1807 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5b3390ef1dc4ddbbba9d2b65b48025c99a97574f1012dec99d1cf6833ef7375`  
		Last Modified: Tue, 11 Feb 2025 19:49:25 GMT  
		Size: 436.6 MB (436553516 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c0d5f286ec85a7b3dbea46893f55c065a974c10e7774b8bdf805a097716d044`  
		Last Modified: Tue, 11 Feb 2025 19:49:16 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8daf130f0ee702f5019935ddda2e21e99c0ddd97449b7e71a22d989c6dd63d0e`  
		Last Modified: Tue, 11 Feb 2025 19:49:16 GMT  
		Size: 1.6 KB (1578 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44178f8c742359d8d2809da03d5ffd7b04e3149f6522a9ffccedd0d8b0e381dc`  
		Last Modified: Tue, 11 Feb 2025 19:49:17 GMT  
		Size: 278.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29994eab0865dd258a8578902658107dbd7ee8c0b39ac709800b4802a6ac4895`  
		Last Modified: Tue, 11 Feb 2025 19:49:17 GMT  
		Size: 1.8 KB (1766 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:322d70a6a4c98f3d2beecaf46f4975b0fbbfa4d2d8d4fe89f8f56676db365f19`  
		Last Modified: Tue, 11 Feb 2025 19:49:18 GMT  
		Size: 4.0 MB (4002539 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5127126e646c17131afae840dd5a6e8bc2c0f102b43b3992c58007e061f4385c`  
		Last Modified: Tue, 11 Feb 2025 19:49:19 GMT  
		Size: 1.9 MB (1937306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f77c089fd3bc24ded136c5bebe2c89d2ac114fb5a2531e24eaabb98fe03902c3`  
		Last Modified: Tue, 11 Feb 2025 19:49:18 GMT  
		Size: 710.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `logstash:8.16.4` - unknown; unknown

```console
$ docker pull logstash@sha256:8c4f30764f638747358bed3da32e5bf514659e975ec676d2cb58277273ef3672
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3554345 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:22e71eb743ef4b2a3d534de8dd7b2d515c1ac4d6acfb7ee94601fd4a2bf265b2`

```dockerfile
```

-	Layers:
	-	`sha256:6d6bbbf6f77add08a4c5a7dfaac70e5a91547f4ea1282f70d029f3403dc817c5`  
		Last Modified: Tue, 11 Feb 2025 19:49:16 GMT  
		Size: 3.5 MB (3519631 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c833678a9c854d3e8bebb88d546e07aa732ddcefdcf7da98771251a3c76345fc`  
		Last Modified: Tue, 11 Feb 2025 19:49:15 GMT  
		Size: 34.7 KB (34714 bytes)  
		MIME: application/vnd.in-toto+json

## `logstash:8.17.2`

```console
$ docker pull logstash@sha256:c59e15f0cbcf8422c6ebec0fa1d5c567c7784acf814d81c71d3d410a6c4c6116
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `logstash:8.17.2` - linux; amd64

```console
$ docker pull logstash@sha256:c126b006cb1e3633e430d4da4d245bdda4dafbafd8ddfbea4b23fe61196ecc3e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **529.9 MB (529857237 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:760c7f40c4f5da2e5ec59c96ce54ed36dd2146e6022c36807448231b79b1437d`
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
# Tue, 11 Feb 2025 12:44:29 GMT
RUN for iter in {1..10}; do       export DEBIAN_FRONTEND=noninteractive &&     apt-get update -y &&   apt-get upgrade -y &&   apt-get install -y procps findutils tar gzip &&         apt-get install -y locales &&         apt-get install -y curl &&     apt-get clean all &&       locale-gen 'en_US.UTF-8' &&     apt-get clean metadata &&   exit_code=0 && break || exit_code=$? && echo "packaging error: retry $iter in 10s" && apt-get clean all &&   apt-get clean metadata && sleep 10; done; (exit $exit_code) # buildkit
# Tue, 11 Feb 2025 12:44:29 GMT
RUN groupadd --gid 1000 logstash &&   adduser --uid 1000 --gid 1000 --home /usr/share/logstash --no-create-home logstash # buildkit
# Tue, 11 Feb 2025 12:44:29 GMT
RUN curl -Lo - https://artifacts.elastic.co/downloads/logstash/logstash-8.17.2-linux-$(arch).tar.gz |   tar zxf - -C /usr/share &&   mv /usr/share/logstash-8.17.2 /usr/share/logstash &&   chown --recursive logstash:logstash /usr/share/logstash/ &&   chown -R logstash:root /usr/share/logstash &&   chmod -R g=u /usr/share/logstash &&   mkdir /licenses/ &&   mv /usr/share/logstash/NOTICE.TXT /licenses/NOTICE.TXT &&   mv /usr/share/logstash/LICENSE.txt /licenses/LICENSE.txt &&   find /usr/share/logstash -type d -exec chmod g+s {} \; &&   ln -s /usr/share/logstash /opt/logstash # buildkit
# Tue, 11 Feb 2025 12:44:29 GMT
WORKDIR /usr/share/logstash
# Tue, 11 Feb 2025 12:44:29 GMT
ENV ELASTIC_CONTAINER=true
# Tue, 11 Feb 2025 12:44:29 GMT
ENV PATH=/usr/share/logstash/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 11 Feb 2025 12:44:29 GMT
COPY config/logstash-full.yml config/logstash.yml # buildkit
# Tue, 11 Feb 2025 12:44:29 GMT
COPY config/pipelines.yml config/log4j2.properties config/log4j2.file.properties config/ # buildkit
# Tue, 11 Feb 2025 12:44:29 GMT
COPY pipeline/default.conf pipeline/logstash.conf # buildkit
# Tue, 11 Feb 2025 12:44:29 GMT
RUN chown --recursive logstash:root config/ pipeline/ # buildkit
# Tue, 11 Feb 2025 12:44:29 GMT
ENV LANG=en_US.UTF-8 LC_ALL=en_US.UTF-8
# Tue, 11 Feb 2025 12:44:29 GMT
COPY env2yaml/env2yaml-amd64 env2yaml/env2yaml-arm64 env2yaml/ # buildkit
# Tue, 11 Feb 2025 12:44:29 GMT
RUN env2yamlarch="$(dpkg --print-architecture)";   case "${env2yamlarch}" in     'x86_64'|'amd64')       env2yamlarch=amd64;       ;;     'aarch64'|'arm64')       env2yamlarch=arm64;       ;;     *) echo >&2 "error: unsupported architecture '$env2yamlarch'"; exit 1 ;;   esac;   mkdir -p /usr/local/bin;   cp env2yaml/env2yaml-${env2yamlarch} /usr/local/bin/env2yaml;   rm -rf env2yaml # buildkit
# Tue, 11 Feb 2025 12:44:29 GMT
COPY bin/docker-entrypoint /usr/local/bin/ # buildkit
# Tue, 11 Feb 2025 12:44:29 GMT
RUN chmod 0755 /usr/local/bin/docker-entrypoint # buildkit
# Tue, 11 Feb 2025 12:44:29 GMT
USER 1000
# Tue, 11 Feb 2025 12:44:29 GMT
EXPOSE map[5044/tcp:{} 9600/tcp:{}]
# Tue, 11 Feb 2025 12:44:29 GMT
LABEL org.label-schema.schema-version=1.0 org.label-schema.vendor=Elastic org.opencontainers.image.vendor=Elastic org.label-schema.name=logstash org.opencontainers.image.title=logstash org.label-schema.version=8.17.2 org.opencontainers.image.version=8.17.2 org.label-schema.url=https://www.elastic.co/products/logstash org.label-schema.vcs-url=https://github.com/elastic/logstash org.label-schema.license=Elastic License org.opencontainers.image.licenses=Elastic License org.opencontainers.image.description=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' org.label-schema.build-date=2025-02-05T18:46:19+00:00 org.opencontainers.image.created=2025-02-05T18:46:19+00:00
# Tue, 11 Feb 2025 12:44:29 GMT
ENTRYPOINT ["/usr/local/bin/docker-entrypoint"]
```

-	Layers:
	-	`sha256:d9802f032d6798e2086607424bfe88cb8ec1d6f116e11cd99592dcaf261e9cd2`  
		Last Modified: Fri, 11 Oct 2024 04:41:25 GMT  
		Size: 27.5 MB (27511060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7511019e58f7cab84eaa566b6922e35c5e52cb0e9bd083c82d6388b9f6c29d46`  
		Last Modified: Tue, 11 Feb 2025 19:30:14 GMT  
		Size: 57.7 MB (57729030 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f1cc28a8b72f3dd235a6a41009526b2cf500be1a8b7d5bdc7560340350ae669`  
		Last Modified: Tue, 11 Feb 2025 19:30:11 GMT  
		Size: 1.8 KB (1807 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f4a50bc9490087e4f74909a67b192e8c60c674270e1046b503f6fc4167a7bf7`  
		Last Modified: Tue, 11 Feb 2025 19:30:26 GMT  
		Size: 438.5 MB (438542755 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0dd8c599b81b02a9c6c3b85c16e70361f2de497f788b02202139bb635f113315`  
		Last Modified: Tue, 11 Feb 2025 19:30:11 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2d466263f283b32177f32bdac8dae52a11b1a265472b674134f973863bceac0`  
		Last Modified: Tue, 11 Feb 2025 19:30:12 GMT  
		Size: 1.6 KB (1579 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3706caeb0c635fe5962bfd406d5c7ae6764fd03f78f2cc3b1b89e77fa0af6da4`  
		Last Modified: Tue, 11 Feb 2025 19:30:12 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95c13380124205f4fd4185a223095afbd7990c8ca4f8b1f96ac9d978b86d01bb`  
		Last Modified: Tue, 11 Feb 2025 19:30:13 GMT  
		Size: 1.8 KB (1767 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e34c1b6f4fd2c5750a03a68308ae24c3d2f539260906452247beec6910ad1f68`  
		Last Modified: Tue, 11 Feb 2025 19:30:14 GMT  
		Size: 4.0 MB (4002545 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2d9337fa80046a8f68b46a9c2b8e8b943a721b932fbd215b7b3615e10d1924a`  
		Last Modified: Tue, 11 Feb 2025 19:30:15 GMT  
		Size: 2.1 MB (2065361 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5396503d29a8111426487a4a32322a6a34179365193d3f9276dc614513a0c520`  
		Last Modified: Tue, 11 Feb 2025 19:30:15 GMT  
		Size: 713.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `logstash:8.17.2` - unknown; unknown

```console
$ docker pull logstash@sha256:0edd3eabca68c4b8a3663c630160ac177666cf00bacf04917ce17b4be00a5695
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3556111 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2cf5ff6476494d241b558230051411c0f002f13e89d0e646b380717857e36276`

```dockerfile
```

-	Layers:
	-	`sha256:2a2598ef13ea9ea9d531028fa3ea41033cf236e61fc4b6a8b52de499536f576f`  
		Last Modified: Tue, 11 Feb 2025 19:30:12 GMT  
		Size: 3.5 MB (3521540 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2e41750deffef9bb46a50912e8647dc450622418dbe78a1b1688f9049c4afc20`  
		Last Modified: Tue, 11 Feb 2025 19:30:11 GMT  
		Size: 34.6 KB (34571 bytes)  
		MIME: application/vnd.in-toto+json

### `logstash:8.17.2` - linux; arm64 variant v8

```console
$ docker pull logstash@sha256:1795a0fc8de1ca866ea39cccaa0c1309a5bfb72bca1e39ae1aa9d7cb543f965f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **513.1 MB (513050961 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e4313bc2be39f46e5b87a49b18b98206f9b730edddec66f5fe2662103f9ef40c`
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
# Tue, 11 Feb 2025 12:44:29 GMT
RUN for iter in {1..10}; do       export DEBIAN_FRONTEND=noninteractive &&     apt-get update -y &&   apt-get upgrade -y &&   apt-get install -y procps findutils tar gzip &&         apt-get install -y locales &&         apt-get install -y curl &&     apt-get clean all &&       locale-gen 'en_US.UTF-8' &&     apt-get clean metadata &&   exit_code=0 && break || exit_code=$? && echo "packaging error: retry $iter in 10s" && apt-get clean all &&   apt-get clean metadata && sleep 10; done; (exit $exit_code) # buildkit
# Tue, 11 Feb 2025 12:44:29 GMT
RUN groupadd --gid 1000 logstash &&   adduser --uid 1000 --gid 1000 --home /usr/share/logstash --no-create-home logstash # buildkit
# Tue, 11 Feb 2025 12:44:29 GMT
RUN curl -Lo - https://artifacts.elastic.co/downloads/logstash/logstash-8.17.2-linux-$(arch).tar.gz |   tar zxf - -C /usr/share &&   mv /usr/share/logstash-8.17.2 /usr/share/logstash &&   chown --recursive logstash:logstash /usr/share/logstash/ &&   chown -R logstash:root /usr/share/logstash &&   chmod -R g=u /usr/share/logstash &&   mkdir /licenses/ &&   mv /usr/share/logstash/NOTICE.TXT /licenses/NOTICE.TXT &&   mv /usr/share/logstash/LICENSE.txt /licenses/LICENSE.txt &&   find /usr/share/logstash -type d -exec chmod g+s {} \; &&   ln -s /usr/share/logstash /opt/logstash # buildkit
# Tue, 11 Feb 2025 12:44:29 GMT
WORKDIR /usr/share/logstash
# Tue, 11 Feb 2025 12:44:29 GMT
ENV ELASTIC_CONTAINER=true
# Tue, 11 Feb 2025 12:44:29 GMT
ENV PATH=/usr/share/logstash/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 11 Feb 2025 12:44:29 GMT
COPY config/logstash-full.yml config/logstash.yml # buildkit
# Tue, 11 Feb 2025 12:44:29 GMT
COPY config/pipelines.yml config/log4j2.properties config/log4j2.file.properties config/ # buildkit
# Tue, 11 Feb 2025 12:44:29 GMT
COPY pipeline/default.conf pipeline/logstash.conf # buildkit
# Tue, 11 Feb 2025 12:44:29 GMT
RUN chown --recursive logstash:root config/ pipeline/ # buildkit
# Tue, 11 Feb 2025 12:44:29 GMT
ENV LANG=en_US.UTF-8 LC_ALL=en_US.UTF-8
# Tue, 11 Feb 2025 12:44:29 GMT
COPY env2yaml/env2yaml-amd64 env2yaml/env2yaml-arm64 env2yaml/ # buildkit
# Tue, 11 Feb 2025 12:44:29 GMT
RUN env2yamlarch="$(dpkg --print-architecture)";   case "${env2yamlarch}" in     'x86_64'|'amd64')       env2yamlarch=amd64;       ;;     'aarch64'|'arm64')       env2yamlarch=arm64;       ;;     *) echo >&2 "error: unsupported architecture '$env2yamlarch'"; exit 1 ;;   esac;   mkdir -p /usr/local/bin;   cp env2yaml/env2yaml-${env2yamlarch} /usr/local/bin/env2yaml;   rm -rf env2yaml # buildkit
# Tue, 11 Feb 2025 12:44:29 GMT
COPY bin/docker-entrypoint /usr/local/bin/ # buildkit
# Tue, 11 Feb 2025 12:44:29 GMT
RUN chmod 0755 /usr/local/bin/docker-entrypoint # buildkit
# Tue, 11 Feb 2025 12:44:29 GMT
USER 1000
# Tue, 11 Feb 2025 12:44:29 GMT
EXPOSE map[5044/tcp:{} 9600/tcp:{}]
# Tue, 11 Feb 2025 12:44:29 GMT
LABEL org.label-schema.schema-version=1.0 org.label-schema.vendor=Elastic org.opencontainers.image.vendor=Elastic org.label-schema.name=logstash org.opencontainers.image.title=logstash org.label-schema.version=8.17.2 org.opencontainers.image.version=8.17.2 org.label-schema.url=https://www.elastic.co/products/logstash org.label-schema.vcs-url=https://github.com/elastic/logstash org.label-schema.license=Elastic License org.opencontainers.image.licenses=Elastic License org.opencontainers.image.description=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' org.label-schema.build-date=2025-02-05T18:46:19+00:00 org.opencontainers.image.created=2025-02-05T18:46:19+00:00
# Tue, 11 Feb 2025 12:44:29 GMT
ENTRYPOINT ["/usr/local/bin/docker-entrypoint"]
```

-	Layers:
	-	`sha256:1b9f3c55f9d4aa5c52eb67a4cb7d0f4726ab85a413b50e3e3fe788befce3d297`  
		Last Modified: Fri, 11 Oct 2024 04:41:30 GMT  
		Size: 26.0 MB (25973828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7651092bb7bf62c6844dc81b0a938d4067dd5bafe70c6ed10922a5aaf08eff87`  
		Last Modified: Tue, 11 Feb 2025 19:49:17 GMT  
		Size: 44.3 MB (44294656 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ef0a54360ec84df15a8be824f6cbdcc417fb33f38f49de22a02735cd175287f`  
		Last Modified: Tue, 11 Feb 2025 19:49:15 GMT  
		Size: 1.8 KB (1807 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9153ec654bedbd7c7ee07a985b9f50f35adb9f1b4b9c136d70a596d68e89eb8f`  
		Last Modified: Tue, 11 Feb 2025 19:50:56 GMT  
		Size: 436.8 MB (436836162 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89d697a5ca2b32444f6a6a9d05161cb67ea3729a05ffc8d38c706ee73cd20ab0`  
		Last Modified: Tue, 11 Feb 2025 19:50:46 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8f29dbfe48e925e9edb57f27e658ba2ddd9bbbd38ad8582c892f5037e9f1b49`  
		Last Modified: Tue, 11 Feb 2025 19:50:46 GMT  
		Size: 1.6 KB (1579 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1d56f377f60dab95d1d15491ac5af4f26c99ace81f878239a1f5638dbe4e3aa`  
		Last Modified: Tue, 11 Feb 2025 19:50:46 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f64c84c306b15670f2473a3ba6599ccb408707a7f5bc232005cb841548aab4b`  
		Last Modified: Tue, 11 Feb 2025 19:50:47 GMT  
		Size: 1.8 KB (1764 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e25da39a01781ec16b78525fe74357c37aabcdda80ec4630c5f04550aef291c8`  
		Last Modified: Tue, 11 Feb 2025 19:50:48 GMT  
		Size: 4.0 MB (4002537 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4ccb4fa82211672240629c8e9473524e858f4d7a804286f183a1d959b583b96`  
		Last Modified: Tue, 11 Feb 2025 19:50:48 GMT  
		Size: 1.9 MB (1937301 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41c2a47824cf2982f3f293012501607e08f4c334373b16b04a0cf124569d9fd9`  
		Last Modified: Tue, 11 Feb 2025 19:50:48 GMT  
		Size: 710.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `logstash:8.17.2` - unknown; unknown

```console
$ docker pull logstash@sha256:38fbd3ae00eccfb68bc73a2d5b0d03efc308c659989e31fcc9d0238bfa9d2bcc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3555865 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f0aece22668badff04d176180876034a166125fcb2449d371cffcb930f30512`

```dockerfile
```

-	Layers:
	-	`sha256:0812960bdc467e819d082e1a69de2a0d96259bca5063a5ec23a5df1aa01c3f48`  
		Last Modified: Tue, 11 Feb 2025 19:50:47 GMT  
		Size: 3.5 MB (3521152 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1a087180fefe8af2d975276e751a146f2118ec810e032f6ee6d3c9bff3415ac5`  
		Last Modified: Tue, 11 Feb 2025 19:50:46 GMT  
		Size: 34.7 KB (34713 bytes)  
		MIME: application/vnd.in-toto+json
