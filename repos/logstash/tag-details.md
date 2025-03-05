<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `logstash`

-	[`logstash:7.17.28`](#logstash71728)
-	[`logstash:8.16.5`](#logstash8165)
-	[`logstash:8.17.3`](#logstash8173)

## `logstash:7.17.28`

```console
$ docker pull logstash@sha256:c52dc70e274074260f4d825c4d6ae3a152d0dc964946ec05b422f1089439a4f7
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
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

### `logstash:7.17.28` - linux; arm64 variant v8

```console
$ docker pull logstash@sha256:92c6155c544067117f34825566c8e59e3a6b4a38bfc83b35b7e20718a1804dda
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **446.0 MB (446040736 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c5ce884935e2ac1ca059e68efd991f100d8b93eb1b12806d2776c013b44ea6e`
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
	-	`sha256:1b9f3c55f9d4aa5c52eb67a4cb7d0f4726ab85a413b50e3e3fe788befce3d297`  
		Last Modified: Fri, 11 Oct 2024 04:41:30 GMT  
		Size: 26.0 MB (25973828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb01db6dc1b3740bc20e03824d4628f0f418bd66256ecc7924eeb9eb1ff10b6b`  
		Last Modified: Tue, 25 Feb 2025 23:55:19 GMT  
		Size: 45.2 MB (45219399 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0424e35676f6ec7c72c69aca0aed12a5e1a492f94b9c5798eb75a60f01abc9d7`  
		Last Modified: Tue, 25 Feb 2025 23:55:17 GMT  
		Size: 1.8 KB (1801 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3bf6a3049a27f377393db29513cede80f9e0a5f18ae0e32eab48287fe164aaa8`  
		Last Modified: Tue, 25 Feb 2025 23:55:28 GMT  
		Size: 372.7 MB (372748393 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6257b2b970efcfb5860074d122704a20930f06a4be2550a99cf3ca10fc8bc21`  
		Last Modified: Tue, 25 Feb 2025 23:55:17 GMT  
		Size: 377.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7b74fb47b9434a518ad7ec6e6c3390fbe8f2676a61e86a0e50e733ba692aef2`  
		Last Modified: Tue, 25 Feb 2025 23:55:18 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:224dc8442929514734ba84928b925193d34ba2843106c068024f04a7b08b4cea`  
		Last Modified: Tue, 25 Feb 2025 23:55:18 GMT  
		Size: 472.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e82839b3fe92f6a6a117c8dfbed99c393eca46d8f926f7168ea84b20fbe6095f`  
		Last Modified: Tue, 25 Feb 2025 23:55:19 GMT  
		Size: 278.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd0888ca5549a286ef05f9e9ef1026c8131e06754f35a9a93ebf9a3711016822`  
		Last Modified: Tue, 25 Feb 2025 23:55:19 GMT  
		Size: 828.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f1fc2885bff8cd7de1669590c51fdc64ee2f995ce6b9ab613b96417e079df60`  
		Last Modified: Tue, 25 Feb 2025 23:55:20 GMT  
		Size: 2.1 MB (2094532 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2febf965eca2cb279b669a5e13e79b685da7fc64b91506e0e1d291df508bdcbf`  
		Last Modified: Tue, 25 Feb 2025 23:55:20 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `logstash:7.17.28` - unknown; unknown

```console
$ docker pull logstash@sha256:0c5943d2bb0879bf1ecbe19093cfa40e7c5cfb57ba24d371197977df96be68ff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.4 MB (3372296 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a8ca0c43ea9b7dfc1c2da377cc4e6e11256ec760c998fd3c497567c3243dbfbc`

```dockerfile
```

-	Layers:
	-	`sha256:e5c2ee4e405e3ee145956e3d96d56461147fd87d979174efc9e995d007101b38`  
		Last Modified: Tue, 25 Feb 2025 23:55:17 GMT  
		Size: 3.3 MB (3339982 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a9a0516240d62014ae19a808626e7051f7d788842ae980f954ebf0fd09e8e831`  
		Last Modified: Tue, 25 Feb 2025 23:55:17 GMT  
		Size: 32.3 KB (32314 bytes)  
		MIME: application/vnd.in-toto+json

## `logstash:8.16.5`

```console
$ docker pull logstash@sha256:4369c79e5631216081786d6f51dc9c06d3ad3811532b5c21dbcafedb7883b3cd
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `logstash:8.16.5` - linux; amd64

```console
$ docker pull logstash@sha256:8425455e5e974c4f23043a65b9dd1f8fdd55a0741fd8a228e32a4ae7f60199da
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **530.8 MB (530841247 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b3070dfd46c03d6bcced6a8f176fbe32ac2e39196c0672775049ea08c7a29340`
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
# Tue, 04 Mar 2025 09:16:27 GMT
RUN for iter in {1..10}; do       export DEBIAN_FRONTEND=noninteractive &&     apt-get update -y &&   apt-get upgrade -y &&   apt-get install -y procps findutils tar gzip &&         apt-get install -y locales &&         apt-get install -y curl &&     apt-get clean all &&       locale-gen 'en_US.UTF-8' &&     apt-get clean metadata &&   exit_code=0 && break || exit_code=$? && echo "packaging error: retry $iter in 10s" && apt-get clean all &&   apt-get clean metadata && sleep 10; done; (exit $exit_code) # buildkit
# Tue, 04 Mar 2025 09:16:27 GMT
RUN groupadd --gid 1000 logstash &&   adduser --uid 1000 --gid 1000 --home /usr/share/logstash --no-create-home logstash # buildkit
# Tue, 04 Mar 2025 09:16:27 GMT
RUN curl -Lo - https://artifacts.elastic.co/downloads/logstash/logstash-8.16.5-linux-$(arch).tar.gz |   tar zxf - -C /usr/share &&   mv /usr/share/logstash-8.16.5 /usr/share/logstash &&   chown --recursive logstash:logstash /usr/share/logstash/ &&   chown -R logstash:root /usr/share/logstash &&   chmod -R g=u /usr/share/logstash &&   mkdir /licenses/ &&   mv /usr/share/logstash/NOTICE.TXT /licenses/NOTICE.TXT &&   mv /usr/share/logstash/LICENSE.txt /licenses/LICENSE.txt &&   find /usr/share/logstash -type d -exec chmod g+s {} \; &&   ln -s /usr/share/logstash /opt/logstash # buildkit
# Tue, 04 Mar 2025 09:16:27 GMT
WORKDIR /usr/share/logstash
# Tue, 04 Mar 2025 09:16:27 GMT
ENV ELASTIC_CONTAINER=true
# Tue, 04 Mar 2025 09:16:27 GMT
ENV PATH=/usr/share/logstash/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Mar 2025 09:16:27 GMT
COPY config/logstash-full.yml config/logstash.yml # buildkit
# Tue, 04 Mar 2025 09:16:27 GMT
COPY config/pipelines.yml config/log4j2.properties config/log4j2.file.properties config/ # buildkit
# Tue, 04 Mar 2025 09:16:27 GMT
COPY pipeline/default.conf pipeline/logstash.conf # buildkit
# Tue, 04 Mar 2025 09:16:27 GMT
RUN chown --recursive logstash:root config/ pipeline/ # buildkit
# Tue, 04 Mar 2025 09:16:27 GMT
ENV LANG=en_US.UTF-8 LC_ALL=en_US.UTF-8
# Tue, 04 Mar 2025 09:16:27 GMT
COPY env2yaml/env2yaml-amd64 env2yaml/env2yaml-arm64 env2yaml/ # buildkit
# Tue, 04 Mar 2025 09:16:27 GMT
RUN env2yamlarch="$(dpkg --print-architecture)";   case "${env2yamlarch}" in     'x86_64'|'amd64')       env2yamlarch=amd64;       ;;     'aarch64'|'arm64')       env2yamlarch=arm64;       ;;     *) echo >&2 "error: unsupported architecture '$env2yamlarch'"; exit 1 ;;   esac;   mkdir -p /usr/local/bin;   cp env2yaml/env2yaml-${env2yamlarch} /usr/local/bin/env2yaml;   rm -rf env2yaml # buildkit
# Tue, 04 Mar 2025 09:16:27 GMT
COPY bin/docker-entrypoint /usr/local/bin/ # buildkit
# Tue, 04 Mar 2025 09:16:27 GMT
RUN chmod 0755 /usr/local/bin/docker-entrypoint # buildkit
# Tue, 04 Mar 2025 09:16:27 GMT
USER 1000
# Tue, 04 Mar 2025 09:16:27 GMT
EXPOSE map[5044/tcp:{} 9600/tcp:{}]
# Tue, 04 Mar 2025 09:16:27 GMT
LABEL org.label-schema.schema-version=1.0 org.label-schema.vendor=Elastic org.opencontainers.image.vendor=Elastic org.label-schema.name=logstash org.opencontainers.image.title=logstash org.label-schema.version=8.16.5 org.opencontainers.image.version=8.16.5 org.label-schema.url=https://www.elastic.co/products/logstash org.label-schema.vcs-url=https://github.com/elastic/logstash org.label-schema.license=Elastic License org.opencontainers.image.licenses=Elastic License org.opencontainers.image.description=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' org.label-schema.build-date=2025-02-26T14:22:35+00:00 org.opencontainers.image.created=2025-02-26T14:22:35+00:00
# Tue, 04 Mar 2025 09:16:27 GMT
ENTRYPOINT ["/usr/local/bin/docker-entrypoint"]
```

-	Layers:
	-	`sha256:d9802f032d6798e2086607424bfe88cb8ec1d6f116e11cd99592dcaf261e9cd2`  
		Last Modified: Fri, 11 Oct 2024 04:41:25 GMT  
		Size: 27.5 MB (27511060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7d5f635bdedc79d1a3571b4fda1c996f49142ae5413aa9096edc850473ce97f`  
		Last Modified: Tue, 04 Mar 2025 21:58:48 GMT  
		Size: 58.9 MB (58876269 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b7c8a30620c02b4b23382507aefaad50d02f4e53e2f834d753786c6f72dcc5d`  
		Last Modified: Tue, 04 Mar 2025 21:58:47 GMT  
		Size: 1.8 KB (1805 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f639bda1cf2bcb66865c65f475ababb910d188cda7b884b1d09a1ae0f17040c`  
		Last Modified: Tue, 04 Mar 2025 21:58:56 GMT  
		Size: 438.3 MB (438301508 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95ccfbc11867bd6bed84c6151a87d5dfc747577594c33536397572c08674afd9`  
		Last Modified: Tue, 04 Mar 2025 21:58:48 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:937833b0baae38976fde3aa6ae57504e6aefe4124e3f5f31cdf66df49d82dbcc`  
		Last Modified: Tue, 04 Mar 2025 21:58:48 GMT  
		Size: 1.6 KB (1577 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f07e9d11e11104811242c562d85e269be5e716b5576f14934d7ea37b459d0b93`  
		Last Modified: Tue, 04 Mar 2025 21:58:48 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0bd1e1f0578e3ffcebcdd8534257d8a7c79214d6eaf431ca00bad66ba8821ae8`  
		Last Modified: Tue, 04 Mar 2025 21:58:49 GMT  
		Size: 1.8 KB (1765 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c461dd4da0083d0f9676a7fa67bdd5f6bf14d8c9b8dd7f4bd1bcadf3bca74e8f`  
		Last Modified: Tue, 04 Mar 2025 21:58:49 GMT  
		Size: 4.1 MB (4052733 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0790d0ec1ecb2feb097432fa9321985d6470463050df39dc7457538865e9c58f`  
		Last Modified: Tue, 04 Mar 2025 21:58:50 GMT  
		Size: 2.1 MB (2093198 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0d979f96ef79b399788261bde89ef755e1b9ea8eca92f210b4513c2d7781c48`  
		Last Modified: Tue, 04 Mar 2025 21:58:50 GMT  
		Size: 713.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `logstash:8.16.5` - unknown; unknown

```console
$ docker pull logstash@sha256:fa0f1f361bb4c309dd52284f2c1a31067dafd5c19785eca4e8eb121c721b98f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3554611 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d0de83ef1b17e3d73cb50300d138d835a173b4c31d2355a33266cca8161c51c`

```dockerfile
```

-	Layers:
	-	`sha256:66bd8c3cbaf343fa6fff33fdba8c39b9315ab5d3401a2ceb6ab04ba9dfdbf29c`  
		Last Modified: Tue, 04 Mar 2025 21:58:48 GMT  
		Size: 3.5 MB (3520040 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9d6d5c315ad3b9f1938defcf95829dce0da953c4495201635e7260d623402cb4`  
		Last Modified: Tue, 04 Mar 2025 21:58:47 GMT  
		Size: 34.6 KB (34571 bytes)  
		MIME: application/vnd.in-toto+json

### `logstash:8.16.5` - linux; arm64 variant v8

```console
$ docker pull logstash@sha256:3a92eba429bed6652dda409f0f3e0eb56f195cefe943fe79148ce50f8c38e157
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **513.8 MB (513834530 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b4ccedcf51119ca3353bdc478a24e737c3591c5c45d5c8b6a602903fbf7ed7be`
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
# Tue, 04 Mar 2025 09:16:27 GMT
RUN for iter in {1..10}; do       export DEBIAN_FRONTEND=noninteractive &&     apt-get update -y &&   apt-get upgrade -y &&   apt-get install -y procps findutils tar gzip &&         apt-get install -y locales &&         apt-get install -y curl &&     apt-get clean all &&       locale-gen 'en_US.UTF-8' &&     apt-get clean metadata &&   exit_code=0 && break || exit_code=$? && echo "packaging error: retry $iter in 10s" && apt-get clean all &&   apt-get clean metadata && sleep 10; done; (exit $exit_code) # buildkit
# Tue, 04 Mar 2025 09:16:27 GMT
RUN groupadd --gid 1000 logstash &&   adduser --uid 1000 --gid 1000 --home /usr/share/logstash --no-create-home logstash # buildkit
# Tue, 04 Mar 2025 09:16:27 GMT
RUN curl -Lo - https://artifacts.elastic.co/downloads/logstash/logstash-8.16.5-linux-$(arch).tar.gz |   tar zxf - -C /usr/share &&   mv /usr/share/logstash-8.16.5 /usr/share/logstash &&   chown --recursive logstash:logstash /usr/share/logstash/ &&   chown -R logstash:root /usr/share/logstash &&   chmod -R g=u /usr/share/logstash &&   mkdir /licenses/ &&   mv /usr/share/logstash/NOTICE.TXT /licenses/NOTICE.TXT &&   mv /usr/share/logstash/LICENSE.txt /licenses/LICENSE.txt &&   find /usr/share/logstash -type d -exec chmod g+s {} \; &&   ln -s /usr/share/logstash /opt/logstash # buildkit
# Tue, 04 Mar 2025 09:16:27 GMT
WORKDIR /usr/share/logstash
# Tue, 04 Mar 2025 09:16:27 GMT
ENV ELASTIC_CONTAINER=true
# Tue, 04 Mar 2025 09:16:27 GMT
ENV PATH=/usr/share/logstash/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Mar 2025 09:16:27 GMT
COPY config/logstash-full.yml config/logstash.yml # buildkit
# Tue, 04 Mar 2025 09:16:27 GMT
COPY config/pipelines.yml config/log4j2.properties config/log4j2.file.properties config/ # buildkit
# Tue, 04 Mar 2025 09:16:27 GMT
COPY pipeline/default.conf pipeline/logstash.conf # buildkit
# Tue, 04 Mar 2025 09:16:27 GMT
RUN chown --recursive logstash:root config/ pipeline/ # buildkit
# Tue, 04 Mar 2025 09:16:27 GMT
ENV LANG=en_US.UTF-8 LC_ALL=en_US.UTF-8
# Tue, 04 Mar 2025 09:16:27 GMT
COPY env2yaml/env2yaml-amd64 env2yaml/env2yaml-arm64 env2yaml/ # buildkit
# Tue, 04 Mar 2025 09:16:27 GMT
RUN env2yamlarch="$(dpkg --print-architecture)";   case "${env2yamlarch}" in     'x86_64'|'amd64')       env2yamlarch=amd64;       ;;     'aarch64'|'arm64')       env2yamlarch=arm64;       ;;     *) echo >&2 "error: unsupported architecture '$env2yamlarch'"; exit 1 ;;   esac;   mkdir -p /usr/local/bin;   cp env2yaml/env2yaml-${env2yamlarch} /usr/local/bin/env2yaml;   rm -rf env2yaml # buildkit
# Tue, 04 Mar 2025 09:16:27 GMT
COPY bin/docker-entrypoint /usr/local/bin/ # buildkit
# Tue, 04 Mar 2025 09:16:27 GMT
RUN chmod 0755 /usr/local/bin/docker-entrypoint # buildkit
# Tue, 04 Mar 2025 09:16:27 GMT
USER 1000
# Tue, 04 Mar 2025 09:16:27 GMT
EXPOSE map[5044/tcp:{} 9600/tcp:{}]
# Tue, 04 Mar 2025 09:16:27 GMT
LABEL org.label-schema.schema-version=1.0 org.label-schema.vendor=Elastic org.opencontainers.image.vendor=Elastic org.label-schema.name=logstash org.opencontainers.image.title=logstash org.label-schema.version=8.16.5 org.opencontainers.image.version=8.16.5 org.label-schema.url=https://www.elastic.co/products/logstash org.label-schema.vcs-url=https://github.com/elastic/logstash org.label-schema.license=Elastic License org.opencontainers.image.licenses=Elastic License org.opencontainers.image.description=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' org.label-schema.build-date=2025-02-26T14:22:35+00:00 org.opencontainers.image.created=2025-02-26T14:22:35+00:00
# Tue, 04 Mar 2025 09:16:27 GMT
ENTRYPOINT ["/usr/local/bin/docker-entrypoint"]
```

-	Layers:
	-	`sha256:1b9f3c55f9d4aa5c52eb67a4cb7d0f4726ab85a413b50e3e3fe788befce3d297`  
		Last Modified: Fri, 11 Oct 2024 04:41:30 GMT  
		Size: 26.0 MB (25973828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:253229dc1f790beac9c25758fb24b6739e542949f7388a30183e8a334d25dbb7`  
		Last Modified: Tue, 04 Mar 2025 22:38:55 GMT  
		Size: 45.3 MB (45251975 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7c70bd27f9d560a0192c56bda8dd6deff315768e6b4331b9cead8e13d5981a2`  
		Last Modified: Tue, 04 Mar 2025 22:38:54 GMT  
		Size: 1.8 KB (1814 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a730a4ff9ca7b66d128f7f052353642ed07316837ccab4682de8a5b72f3c21db`  
		Last Modified: Tue, 04 Mar 2025 22:48:14 GMT  
		Size: 436.6 MB (436588942 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bed6bb830504265b7f4cb0cab5d9dc587f10da22a60a036662098b10661c8ed0`  
		Last Modified: Tue, 04 Mar 2025 22:48:01 GMT  
		Size: 278.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21f5eb8a5a0db88753c38227c7449ec1d4392bd0c18105a6d852c95f3506e17f`  
		Last Modified: Tue, 04 Mar 2025 22:48:01 GMT  
		Size: 1.6 KB (1580 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26fd32122007a5552c05863008e9d967a6220a2d70cab63ed93ed28d68aa5cb5`  
		Last Modified: Tue, 04 Mar 2025 22:48:01 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec4c1ef6a9dc84571544db646885cb9aa4277979e8ef58448c49cecf8cf3693e`  
		Last Modified: Tue, 04 Mar 2025 22:48:02 GMT  
		Size: 1.8 KB (1761 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:312caa6e27298b3adb1d5c00e681ef2abf781b989ce65b82a23c24d2ab7bb6f3`  
		Last Modified: Tue, 04 Mar 2025 22:48:03 GMT  
		Size: 4.1 MB (4052733 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbc64eda94d0974bec83aaf50af8aa51ce11796c03dfe51e11b14e1e168b2e40`  
		Last Modified: Tue, 04 Mar 2025 22:48:03 GMT  
		Size: 2.0 MB (1960568 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99221a4bf8988690d1207eacfb80bb7375234a44ca45c4fae485e6100194b0e7`  
		Last Modified: Tue, 04 Mar 2025 22:48:03 GMT  
		Size: 710.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `logstash:8.16.5` - unknown; unknown

```console
$ docker pull logstash@sha256:8e1896ed426496692035e59d5f5d57467551d9b6c595fcf885e7a1b8a409c15f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3554366 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ed050831fe7de197c109f100ee9c9b70ecba39522706ca6afd596c7ca839bbc`

```dockerfile
```

-	Layers:
	-	`sha256:073abdeea081cdc4e357e52f38f6dfa547f9d20625373e12caf553d6d0ee31f9`  
		Last Modified: Tue, 04 Mar 2025 22:48:02 GMT  
		Size: 3.5 MB (3519652 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1fce5e35326cc182cd7229ecf16cd3e09b9d13ea0cd75ebf363ad81124f5e0a3`  
		Last Modified: Tue, 04 Mar 2025 22:48:01 GMT  
		Size: 34.7 KB (34714 bytes)  
		MIME: application/vnd.in-toto+json

## `logstash:8.17.3`

```console
$ docker pull logstash@sha256:01feca1dd93ae1c7b0d16d6a7ec08070d13a2e9af16cba88ea916600af8ea8b8
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `logstash:8.17.3` - linux; amd64

```console
$ docker pull logstash@sha256:b23ee5f42dbf9688f3cdde295d20b16385ed7ce83e5267407d58d60fc38ee712
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **531.1 MB (531110546 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0290c30ce404f6f4c408279baa680f42e952da19541d818bc108be5b3e1a96f7`
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
# Tue, 04 Mar 2025 09:12:50 GMT
RUN for iter in {1..10}; do       export DEBIAN_FRONTEND=noninteractive &&     apt-get update -y &&   apt-get upgrade -y &&   apt-get install -y procps findutils tar gzip &&         apt-get install -y locales &&         apt-get install -y curl &&     apt-get clean all &&       locale-gen 'en_US.UTF-8' &&     apt-get clean metadata &&   exit_code=0 && break || exit_code=$? && echo "packaging error: retry $iter in 10s" && apt-get clean all &&   apt-get clean metadata && sleep 10; done; (exit $exit_code) # buildkit
# Tue, 04 Mar 2025 09:12:50 GMT
RUN groupadd --gid 1000 logstash &&   adduser --uid 1000 --gid 1000 --home /usr/share/logstash --no-create-home logstash # buildkit
# Tue, 04 Mar 2025 09:12:50 GMT
RUN curl -Lo - https://artifacts.elastic.co/downloads/logstash/logstash-8.17.3-linux-$(arch).tar.gz |   tar zxf - -C /usr/share &&   mv /usr/share/logstash-8.17.3 /usr/share/logstash &&   chown --recursive logstash:logstash /usr/share/logstash/ &&   chown -R logstash:root /usr/share/logstash &&   chmod -R g=u /usr/share/logstash &&   mkdir /licenses/ &&   mv /usr/share/logstash/NOTICE.TXT /licenses/NOTICE.TXT &&   mv /usr/share/logstash/LICENSE.txt /licenses/LICENSE.txt &&   find /usr/share/logstash -type d -exec chmod g+s {} \; &&   ln -s /usr/share/logstash /opt/logstash # buildkit
# Tue, 04 Mar 2025 09:12:50 GMT
WORKDIR /usr/share/logstash
# Tue, 04 Mar 2025 09:12:50 GMT
ENV ELASTIC_CONTAINER=true
# Tue, 04 Mar 2025 09:12:50 GMT
ENV PATH=/usr/share/logstash/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Mar 2025 09:12:50 GMT
COPY config/logstash-full.yml config/logstash.yml # buildkit
# Tue, 04 Mar 2025 09:12:50 GMT
COPY config/pipelines.yml config/log4j2.properties config/log4j2.file.properties config/ # buildkit
# Tue, 04 Mar 2025 09:12:50 GMT
COPY pipeline/default.conf pipeline/logstash.conf # buildkit
# Tue, 04 Mar 2025 09:12:50 GMT
RUN chown --recursive logstash:root config/ pipeline/ # buildkit
# Tue, 04 Mar 2025 09:12:50 GMT
ENV LANG=en_US.UTF-8 LC_ALL=en_US.UTF-8
# Tue, 04 Mar 2025 09:12:50 GMT
COPY env2yaml/env2yaml-amd64 env2yaml/env2yaml-arm64 env2yaml/ # buildkit
# Tue, 04 Mar 2025 09:12:50 GMT
RUN env2yamlarch="$(dpkg --print-architecture)";   case "${env2yamlarch}" in     'x86_64'|'amd64')       env2yamlarch=amd64;       ;;     'aarch64'|'arm64')       env2yamlarch=arm64;       ;;     *) echo >&2 "error: unsupported architecture '$env2yamlarch'"; exit 1 ;;   esac;   mkdir -p /usr/local/bin;   cp env2yaml/env2yaml-${env2yamlarch} /usr/local/bin/env2yaml;   rm -rf env2yaml # buildkit
# Tue, 04 Mar 2025 09:12:50 GMT
COPY bin/docker-entrypoint /usr/local/bin/ # buildkit
# Tue, 04 Mar 2025 09:12:50 GMT
RUN chmod 0755 /usr/local/bin/docker-entrypoint # buildkit
# Tue, 04 Mar 2025 09:12:50 GMT
USER 1000
# Tue, 04 Mar 2025 09:12:50 GMT
EXPOSE map[5044/tcp:{} 9600/tcp:{}]
# Tue, 04 Mar 2025 09:12:50 GMT
LABEL org.label-schema.schema-version=1.0 org.label-schema.vendor=Elastic org.opencontainers.image.vendor=Elastic org.label-schema.name=logstash org.opencontainers.image.title=logstash org.label-schema.version=8.17.3 org.opencontainers.image.version=8.17.3 org.label-schema.url=https://www.elastic.co/products/logstash org.label-schema.vcs-url=https://github.com/elastic/logstash org.label-schema.license=Elastic License org.opencontainers.image.licenses=Elastic License org.opencontainers.image.description=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' org.label-schema.build-date=2025-02-26T14:14:31+00:00 org.opencontainers.image.created=2025-02-26T14:14:31+00:00
# Tue, 04 Mar 2025 09:12:50 GMT
ENTRYPOINT ["/usr/local/bin/docker-entrypoint"]
```

-	Layers:
	-	`sha256:d9802f032d6798e2086607424bfe88cb8ec1d6f116e11cd99592dcaf261e9cd2`  
		Last Modified: Fri, 11 Oct 2024 04:41:25 GMT  
		Size: 27.5 MB (27511060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e07493f87fd6071e8adca5e363c3f605d375361270d83d10422a135085e95192`  
		Last Modified: Tue, 04 Mar 2025 21:59:07 GMT  
		Size: 58.9 MB (58876260 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a751c16b657f7449bb953cb7afd4a84cd21d13203c57667a478a81c435226f1b`  
		Last Modified: Tue, 04 Mar 2025 21:59:05 GMT  
		Size: 1.8 KB (1807 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b88addf5d30b91603ff305462980c8eae370853a87518bdd5833fe31b5bfd283`  
		Last Modified: Tue, 04 Mar 2025 21:59:19 GMT  
		Size: 438.6 MB (438570828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ea79734d5c368da336f200824d6582fcc1e74039e6a34640c6439b9604e95bb`  
		Last Modified: Tue, 04 Mar 2025 21:59:05 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e114745097284bb2587744e6dd61c1ad381a8a80c5ad86380dba247b9ef5447`  
		Last Modified: Tue, 04 Mar 2025 21:59:06 GMT  
		Size: 1.6 KB (1576 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb7d48c0163eb8a801b917c85430f0321436deef541c8aa7c77b6d4851afbf8a`  
		Last Modified: Tue, 04 Mar 2025 21:59:06 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6ff03cee39ced5bd9f9da4b6b15718167c672dc517ed9c618c4251266221724`  
		Last Modified: Tue, 04 Mar 2025 21:59:07 GMT  
		Size: 1.8 KB (1765 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4da2c2f4a0543cda880133017cebb9b9baa3ca9e1f38956b8a13cae1e2c9ced9`  
		Last Modified: Tue, 04 Mar 2025 21:59:08 GMT  
		Size: 4.1 MB (4052726 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f90aa124e1e1eae5bee57a14671e8f493e449596b6331e7d726c64a13c341dd0`  
		Last Modified: Tue, 04 Mar 2025 21:59:08 GMT  
		Size: 2.1 MB (2093196 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c5c37b236f19ccde8e1bf768cf41dd22a4ac8301571f45fdfe83c3a98b398fb`  
		Last Modified: Tue, 04 Mar 2025 21:59:09 GMT  
		Size: 713.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `logstash:8.17.3` - unknown; unknown

```console
$ docker pull logstash@sha256:64a6786314a4eef6409e3575299215a4afb7f3ed3d31f04968a0bbce377a1c7e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3556132 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:31e6c5525b21c363dc9a45d0d081175aa2c5187202764d9f61b18ad6a797b66f`

```dockerfile
```

-	Layers:
	-	`sha256:2367cf3671a62ff10987b88f47b35b921157a3b13a16a43a0c91df63be181885`  
		Last Modified: Tue, 04 Mar 2025 21:59:05 GMT  
		Size: 3.5 MB (3521561 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:df648f868f0a2620aaab4f7547264b625950bfcb13f59730c0cb25493bd9e7b0`  
		Last Modified: Tue, 04 Mar 2025 21:59:05 GMT  
		Size: 34.6 KB (34571 bytes)  
		MIME: application/vnd.in-toto+json

### `logstash:8.17.3` - linux; arm64 variant v8

```console
$ docker pull logstash@sha256:611b7b14116a383cd3e2c26242e7deaa83a3534e8a816944ad64bdf9477228f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **514.1 MB (514104515 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c5d802dcb21108074c34081922e6ec9c319ce0d14587e8dcc90a6c71318a903`
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
# Tue, 04 Mar 2025 09:12:50 GMT
RUN for iter in {1..10}; do       export DEBIAN_FRONTEND=noninteractive &&     apt-get update -y &&   apt-get upgrade -y &&   apt-get install -y procps findutils tar gzip &&         apt-get install -y locales &&         apt-get install -y curl &&     apt-get clean all &&       locale-gen 'en_US.UTF-8' &&     apt-get clean metadata &&   exit_code=0 && break || exit_code=$? && echo "packaging error: retry $iter in 10s" && apt-get clean all &&   apt-get clean metadata && sleep 10; done; (exit $exit_code) # buildkit
# Tue, 04 Mar 2025 09:12:50 GMT
RUN groupadd --gid 1000 logstash &&   adduser --uid 1000 --gid 1000 --home /usr/share/logstash --no-create-home logstash # buildkit
# Tue, 04 Mar 2025 09:12:50 GMT
RUN curl -Lo - https://artifacts.elastic.co/downloads/logstash/logstash-8.17.3-linux-$(arch).tar.gz |   tar zxf - -C /usr/share &&   mv /usr/share/logstash-8.17.3 /usr/share/logstash &&   chown --recursive logstash:logstash /usr/share/logstash/ &&   chown -R logstash:root /usr/share/logstash &&   chmod -R g=u /usr/share/logstash &&   mkdir /licenses/ &&   mv /usr/share/logstash/NOTICE.TXT /licenses/NOTICE.TXT &&   mv /usr/share/logstash/LICENSE.txt /licenses/LICENSE.txt &&   find /usr/share/logstash -type d -exec chmod g+s {} \; &&   ln -s /usr/share/logstash /opt/logstash # buildkit
# Tue, 04 Mar 2025 09:12:50 GMT
WORKDIR /usr/share/logstash
# Tue, 04 Mar 2025 09:12:50 GMT
ENV ELASTIC_CONTAINER=true
# Tue, 04 Mar 2025 09:12:50 GMT
ENV PATH=/usr/share/logstash/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Mar 2025 09:12:50 GMT
COPY config/logstash-full.yml config/logstash.yml # buildkit
# Tue, 04 Mar 2025 09:12:50 GMT
COPY config/pipelines.yml config/log4j2.properties config/log4j2.file.properties config/ # buildkit
# Tue, 04 Mar 2025 09:12:50 GMT
COPY pipeline/default.conf pipeline/logstash.conf # buildkit
# Tue, 04 Mar 2025 09:12:50 GMT
RUN chown --recursive logstash:root config/ pipeline/ # buildkit
# Tue, 04 Mar 2025 09:12:50 GMT
ENV LANG=en_US.UTF-8 LC_ALL=en_US.UTF-8
# Tue, 04 Mar 2025 09:12:50 GMT
COPY env2yaml/env2yaml-amd64 env2yaml/env2yaml-arm64 env2yaml/ # buildkit
# Tue, 04 Mar 2025 09:12:50 GMT
RUN env2yamlarch="$(dpkg --print-architecture)";   case "${env2yamlarch}" in     'x86_64'|'amd64')       env2yamlarch=amd64;       ;;     'aarch64'|'arm64')       env2yamlarch=arm64;       ;;     *) echo >&2 "error: unsupported architecture '$env2yamlarch'"; exit 1 ;;   esac;   mkdir -p /usr/local/bin;   cp env2yaml/env2yaml-${env2yamlarch} /usr/local/bin/env2yaml;   rm -rf env2yaml # buildkit
# Tue, 04 Mar 2025 09:12:50 GMT
COPY bin/docker-entrypoint /usr/local/bin/ # buildkit
# Tue, 04 Mar 2025 09:12:50 GMT
RUN chmod 0755 /usr/local/bin/docker-entrypoint # buildkit
# Tue, 04 Mar 2025 09:12:50 GMT
USER 1000
# Tue, 04 Mar 2025 09:12:50 GMT
EXPOSE map[5044/tcp:{} 9600/tcp:{}]
# Tue, 04 Mar 2025 09:12:50 GMT
LABEL org.label-schema.schema-version=1.0 org.label-schema.vendor=Elastic org.opencontainers.image.vendor=Elastic org.label-schema.name=logstash org.opencontainers.image.title=logstash org.label-schema.version=8.17.3 org.opencontainers.image.version=8.17.3 org.label-schema.url=https://www.elastic.co/products/logstash org.label-schema.vcs-url=https://github.com/elastic/logstash org.label-schema.license=Elastic License org.opencontainers.image.licenses=Elastic License org.opencontainers.image.description=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' org.label-schema.build-date=2025-02-26T14:14:31+00:00 org.opencontainers.image.created=2025-02-26T14:14:31+00:00
# Tue, 04 Mar 2025 09:12:50 GMT
ENTRYPOINT ["/usr/local/bin/docker-entrypoint"]
```

-	Layers:
	-	`sha256:1b9f3c55f9d4aa5c52eb67a4cb7d0f4726ab85a413b50e3e3fe788befce3d297`  
		Last Modified: Fri, 11 Oct 2024 04:41:30 GMT  
		Size: 26.0 MB (25973828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:253229dc1f790beac9c25758fb24b6739e542949f7388a30183e8a334d25dbb7`  
		Last Modified: Tue, 04 Mar 2025 22:38:55 GMT  
		Size: 45.3 MB (45251975 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7c70bd27f9d560a0192c56bda8dd6deff315768e6b4331b9cead8e13d5981a2`  
		Last Modified: Tue, 04 Mar 2025 22:38:54 GMT  
		Size: 1.8 KB (1814 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36b59902436fbc7be939d48809b74efbb7f9666ffc34bd181e5c58a892519a3c`  
		Last Modified: Tue, 04 Mar 2025 22:39:03 GMT  
		Size: 436.9 MB (436858939 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:783b4dec8f32fa70662b7fdd881eb8874ae4889f6fd8215ed58fcfde26a07890`  
		Last Modified: Tue, 04 Mar 2025 22:38:54 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60290318b35c06db50eef24dc6355897873204e18d560aad59b3a0e4dffc268a`  
		Last Modified: Tue, 04 Mar 2025 22:38:55 GMT  
		Size: 1.6 KB (1576 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81f9d2d027073dfd3ee7d872dd77ebae172f73c78bfb83b12fd8b42da298a885`  
		Last Modified: Tue, 04 Mar 2025 22:38:55 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a95142d68c2622255fd95ec8d2930d7c626978d0a4071fb9d0f7648cc5e536d`  
		Last Modified: Tue, 04 Mar 2025 22:38:56 GMT  
		Size: 1.8 KB (1762 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18460973a003ef5aa191cae34763a0bbf00ad85d2c47c4b7bb1127c077342fa9`  
		Last Modified: Tue, 04 Mar 2025 22:38:56 GMT  
		Size: 4.1 MB (4052729 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa627c795ff65849bdbf448f813b4717cf6108983804e217c9adedcd50666e5a`  
		Last Modified: Tue, 04 Mar 2025 22:38:57 GMT  
		Size: 2.0 MB (1960566 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06afb4f30b9223493428a84d1f03c2a8626542e03ce6bc8d0a7b807197eef85f`  
		Last Modified: Tue, 04 Mar 2025 22:38:57 GMT  
		Size: 709.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `logstash:8.17.3` - unknown; unknown

```console
$ docker pull logstash@sha256:97739dfecced1f3695e31aa77b5ed8d6b8269fb9601e5c1b14e7e09b8a1be4c3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3555887 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6663a9c7c3b33e035b0e6bcdcf4a1376b1c8b4c6683a4558a2345dbf17d8c7fa`

```dockerfile
```

-	Layers:
	-	`sha256:f608b072047b01822b4b1c2e3af168b05794099e5594adaa4bf49182a9195c68`  
		Last Modified: Tue, 04 Mar 2025 22:38:54 GMT  
		Size: 3.5 MB (3521173 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4ad11cfb174bbc6c6d7a877c1a6e8a245a0a3ce8a4c01c2ae19f3c05a456d27d`  
		Last Modified: Tue, 04 Mar 2025 22:38:54 GMT  
		Size: 34.7 KB (34714 bytes)  
		MIME: application/vnd.in-toto+json
