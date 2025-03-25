<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `logstash`

-	[`logstash:7.17.28`](#logstash71728)
-	[`logstash:8.16.6`](#logstash8166)
-	[`logstash:8.17.4`](#logstash8174)

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

## `logstash:8.16.6`

```console
$ docker pull logstash@sha256:8997e7148ed1873b7a31eb8814eafd6e5d901100f72012fd597b7529f9224f0f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `logstash:8.16.6` - linux; amd64

```console
$ docker pull logstash@sha256:2be84206757e0798fa5b04b2e9bc4d5a66642e3a8a116160d475a79210258d72
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **531.1 MB (531063424 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c03d9cfa3cb60fffa553cbda14f8c0a489f248bc010979cba47291bd4af4329`
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
# Tue, 25 Mar 2025 08:54:09 GMT
RUN for iter in {1..10}; do       export DEBIAN_FRONTEND=noninteractive &&     apt-get update -y &&   apt-get upgrade -y &&   apt-get install -y procps findutils tar gzip &&         apt-get install -y locales &&         apt-get install -y curl &&     apt-get clean all &&       locale-gen 'en_US.UTF-8' &&     apt-get clean metadata &&   exit_code=0 && break || exit_code=$? && echo "packaging error: retry $iter in 10s" && apt-get clean all &&   apt-get clean metadata && sleep 10; done; (exit $exit_code) # buildkit
# Tue, 25 Mar 2025 08:54:09 GMT
RUN groupadd --gid 1000 logstash &&   adduser --uid 1000 --gid 1000 --home /usr/share/logstash --no-create-home logstash # buildkit
# Tue, 25 Mar 2025 08:54:09 GMT
RUN curl -Lo - https://artifacts.elastic.co/downloads/logstash/logstash-8.16.6-linux-$(arch).tar.gz |   tar zxf - -C /usr/share &&   mv /usr/share/logstash-8.16.6 /usr/share/logstash &&   chown --recursive logstash:logstash /usr/share/logstash/ &&   chown -R logstash:root /usr/share/logstash &&   chmod -R g=u /usr/share/logstash &&   mkdir /licenses/ &&   mv /usr/share/logstash/NOTICE.TXT /licenses/NOTICE.TXT &&   mv /usr/share/logstash/LICENSE.txt /licenses/LICENSE.txt &&   find /usr/share/logstash -type d -exec chmod g+s {} \; &&   ln -s /usr/share/logstash /opt/logstash # buildkit
# Tue, 25 Mar 2025 08:54:09 GMT
WORKDIR /usr/share/logstash
# Tue, 25 Mar 2025 08:54:09 GMT
ENV ELASTIC_CONTAINER=true
# Tue, 25 Mar 2025 08:54:09 GMT
ENV PATH=/usr/share/logstash/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 25 Mar 2025 08:54:09 GMT
COPY config/logstash-full.yml config/logstash.yml # buildkit
# Tue, 25 Mar 2025 08:54:09 GMT
COPY config/pipelines.yml config/log4j2.properties config/log4j2.file.properties config/ # buildkit
# Tue, 25 Mar 2025 08:54:09 GMT
COPY pipeline/default.conf pipeline/logstash.conf # buildkit
# Tue, 25 Mar 2025 08:54:09 GMT
RUN chown --recursive logstash:root config/ pipeline/ # buildkit
# Tue, 25 Mar 2025 08:54:09 GMT
ENV LANG=en_US.UTF-8 LC_ALL=en_US.UTF-8
# Tue, 25 Mar 2025 08:54:09 GMT
COPY env2yaml/env2yaml-amd64 env2yaml/env2yaml-arm64 env2yaml/ # buildkit
# Tue, 25 Mar 2025 08:54:09 GMT
RUN set -eux; env2yamlarch="$(dpkg --print-architecture)";   case "${env2yamlarch}" in     'x86_64'|'amd64')       env2yamlarch=amd64;       ;;     'aarch64'|'arm64')       env2yamlarch=arm64;       ;;     *) echo >&2 "error: unsupported architecture '$env2yamlarch'"; exit 1 ;;   esac;   mkdir -p /usr/local/bin;   cp env2yaml/env2yaml-${env2yamlarch} /usr/local/bin/env2yaml;   rm -rf env2yaml # buildkit
# Tue, 25 Mar 2025 08:54:09 GMT
COPY bin/docker-entrypoint /usr/local/bin/ # buildkit
# Tue, 25 Mar 2025 08:54:09 GMT
RUN chmod 0755 /usr/local/bin/docker-entrypoint # buildkit
# Tue, 25 Mar 2025 08:54:09 GMT
USER 1000
# Tue, 25 Mar 2025 08:54:09 GMT
EXPOSE map[5044/tcp:{} 9600/tcp:{}]
# Tue, 25 Mar 2025 08:54:09 GMT
LABEL org.label-schema.schema-version=1.0 org.label-schema.vendor=Elastic org.opencontainers.image.vendor=Elastic org.label-schema.name=logstash org.opencontainers.image.title=logstash org.label-schema.version=8.16.6 org.opencontainers.image.version=8.16.6 org.label-schema.url=https://www.elastic.co/products/logstash org.label-schema.vcs-url=https://github.com/elastic/logstash org.label-schema.license=Elastic License org.opencontainers.image.licenses=Elastic License org.opencontainers.image.description=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' org.label-schema.build-date=2025-03-19T17:10:56+00:00 org.opencontainers.image.created=2025-03-19T17:10:56+00:00
# Tue, 25 Mar 2025 08:54:09 GMT
ENTRYPOINT ["/usr/local/bin/docker-entrypoint"]
```

-	Layers:
	-	`sha256:d9802f032d6798e2086607424bfe88cb8ec1d6f116e11cd99592dcaf261e9cd2`  
		Last Modified: Fri, 11 Oct 2024 04:41:25 GMT  
		Size: 27.5 MB (27511060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f85d4f5a02158dbcef02e504fb2b9708371cabc7502e7818c7d979e83ec40c6`  
		Last Modified: Tue, 25 Mar 2025 19:43:51 GMT  
		Size: 59.1 MB (59086753 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:536880699960418f89fae8c63bc5bad79a58f9667d45046ca386db4ce1e81446`  
		Last Modified: Tue, 25 Mar 2025 19:43:50 GMT  
		Size: 1.8 KB (1805 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a786acd1a8c78c1a849eaad7c5a20bc7b2ec6d5f4f56efef71992271218c44d`  
		Last Modified: Tue, 25 Mar 2025 19:43:57 GMT  
		Size: 438.3 MB (438311060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1601b617e7bd9e29eb9f0b8d2a918d14727bb2142bfaf7751e4e32822d51cfe7`  
		Last Modified: Tue, 25 Mar 2025 19:43:50 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b415ca074693045c8f0ac97b49df1f6bd640a8c4f37dfffdf34848da1ba7c84f`  
		Last Modified: Tue, 25 Mar 2025 19:43:51 GMT  
		Size: 1.6 KB (1579 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:604fa5bdbb42510d1320c9d59a60296a6339ea88871621e7e3c6ed24a7476400`  
		Last Modified: Tue, 25 Mar 2025 19:43:51 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b32a3d70c994afd9bc115c5c8fee52bf53ee5b88e7c94bf45d1fcbc9be50372`  
		Last Modified: Tue, 25 Mar 2025 19:43:51 GMT  
		Size: 1.8 KB (1765 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c0d028c81b09bb35b9971dd7d784530323f06d206754a0e3e2b3db6a392f7e9`  
		Last Modified: Tue, 25 Mar 2025 19:43:52 GMT  
		Size: 4.1 MB (4054504 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec32d0201991eef857b3d05923369d168c25fc4925e6d7edffcfb29a82a25dca`  
		Last Modified: Tue, 25 Mar 2025 19:43:52 GMT  
		Size: 2.1 MB (2093569 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d40a5629fed2cc2f03cc12e40cbef71b0180e35c6fd6af7858dfa8c58eddc46`  
		Last Modified: Tue, 25 Mar 2025 19:43:52 GMT  
		Size: 713.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `logstash:8.16.6` - unknown; unknown

```console
$ docker pull logstash@sha256:e0f6cd63c7db612e56b90660b3311398dd5b15070e9aa37217a33405a806cfed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3554633 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:66f1c130a41c721433717f50b6d5c35e33e4a04a1e7e4b852c801378dd936a46`

```dockerfile
```

-	Layers:
	-	`sha256:9757f72fad8841eeea0504e5f04af5c61f16c3d6820c632baebf98ffa8c633ba`  
		Last Modified: Tue, 25 Mar 2025 19:43:50 GMT  
		Size: 3.5 MB (3520040 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fb3d82922bbe7add6dc68c04dd9c22443c9e3cf2e91e867dd4adf034cf2297a3`  
		Last Modified: Tue, 25 Mar 2025 19:43:50 GMT  
		Size: 34.6 KB (34593 bytes)  
		MIME: application/vnd.in-toto+json

### `logstash:8.16.6` - linux; arm64 variant v8

```console
$ docker pull logstash@sha256:28b9c9cb697a5721d340c64920233a8951435c95524c28227b4b1cac5061b61f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **513.9 MB (513916007 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:08ebc0a6ec951a55d112e49d10f11d9f684c066d96ddb3d913b5b7dac0ccf4fa`
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
# Tue, 25 Mar 2025 08:54:09 GMT
RUN for iter in {1..10}; do       export DEBIAN_FRONTEND=noninteractive &&     apt-get update -y &&   apt-get upgrade -y &&   apt-get install -y procps findutils tar gzip &&         apt-get install -y locales &&         apt-get install -y curl &&     apt-get clean all &&       locale-gen 'en_US.UTF-8' &&     apt-get clean metadata &&   exit_code=0 && break || exit_code=$? && echo "packaging error: retry $iter in 10s" && apt-get clean all &&   apt-get clean metadata && sleep 10; done; (exit $exit_code) # buildkit
# Tue, 25 Mar 2025 08:54:09 GMT
RUN groupadd --gid 1000 logstash &&   adduser --uid 1000 --gid 1000 --home /usr/share/logstash --no-create-home logstash # buildkit
# Tue, 25 Mar 2025 08:54:09 GMT
RUN curl -Lo - https://artifacts.elastic.co/downloads/logstash/logstash-8.16.6-linux-$(arch).tar.gz |   tar zxf - -C /usr/share &&   mv /usr/share/logstash-8.16.6 /usr/share/logstash &&   chown --recursive logstash:logstash /usr/share/logstash/ &&   chown -R logstash:root /usr/share/logstash &&   chmod -R g=u /usr/share/logstash &&   mkdir /licenses/ &&   mv /usr/share/logstash/NOTICE.TXT /licenses/NOTICE.TXT &&   mv /usr/share/logstash/LICENSE.txt /licenses/LICENSE.txt &&   find /usr/share/logstash -type d -exec chmod g+s {} \; &&   ln -s /usr/share/logstash /opt/logstash # buildkit
# Tue, 25 Mar 2025 08:54:09 GMT
WORKDIR /usr/share/logstash
# Tue, 25 Mar 2025 08:54:09 GMT
ENV ELASTIC_CONTAINER=true
# Tue, 25 Mar 2025 08:54:09 GMT
ENV PATH=/usr/share/logstash/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 25 Mar 2025 08:54:09 GMT
COPY config/logstash-full.yml config/logstash.yml # buildkit
# Tue, 25 Mar 2025 08:54:09 GMT
COPY config/pipelines.yml config/log4j2.properties config/log4j2.file.properties config/ # buildkit
# Tue, 25 Mar 2025 08:54:09 GMT
COPY pipeline/default.conf pipeline/logstash.conf # buildkit
# Tue, 25 Mar 2025 08:54:09 GMT
RUN chown --recursive logstash:root config/ pipeline/ # buildkit
# Tue, 25 Mar 2025 08:54:09 GMT
ENV LANG=en_US.UTF-8 LC_ALL=en_US.UTF-8
# Tue, 25 Mar 2025 08:54:09 GMT
COPY env2yaml/env2yaml-amd64 env2yaml/env2yaml-arm64 env2yaml/ # buildkit
# Tue, 25 Mar 2025 08:54:09 GMT
RUN set -eux; env2yamlarch="$(dpkg --print-architecture)";   case "${env2yamlarch}" in     'x86_64'|'amd64')       env2yamlarch=amd64;       ;;     'aarch64'|'arm64')       env2yamlarch=arm64;       ;;     *) echo >&2 "error: unsupported architecture '$env2yamlarch'"; exit 1 ;;   esac;   mkdir -p /usr/local/bin;   cp env2yaml/env2yaml-${env2yamlarch} /usr/local/bin/env2yaml;   rm -rf env2yaml # buildkit
# Tue, 25 Mar 2025 08:54:09 GMT
COPY bin/docker-entrypoint /usr/local/bin/ # buildkit
# Tue, 25 Mar 2025 08:54:09 GMT
RUN chmod 0755 /usr/local/bin/docker-entrypoint # buildkit
# Tue, 25 Mar 2025 08:54:09 GMT
USER 1000
# Tue, 25 Mar 2025 08:54:09 GMT
EXPOSE map[5044/tcp:{} 9600/tcp:{}]
# Tue, 25 Mar 2025 08:54:09 GMT
LABEL org.label-schema.schema-version=1.0 org.label-schema.vendor=Elastic org.opencontainers.image.vendor=Elastic org.label-schema.name=logstash org.opencontainers.image.title=logstash org.label-schema.version=8.16.6 org.opencontainers.image.version=8.16.6 org.label-schema.url=https://www.elastic.co/products/logstash org.label-schema.vcs-url=https://github.com/elastic/logstash org.label-schema.license=Elastic License org.opencontainers.image.licenses=Elastic License org.opencontainers.image.description=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' org.label-schema.build-date=2025-03-19T17:10:56+00:00 org.opencontainers.image.created=2025-03-19T17:10:56+00:00
# Tue, 25 Mar 2025 08:54:09 GMT
ENTRYPOINT ["/usr/local/bin/docker-entrypoint"]
```

-	Layers:
	-	`sha256:1b9f3c55f9d4aa5c52eb67a4cb7d0f4726ab85a413b50e3e3fe788befce3d297`  
		Last Modified: Fri, 11 Oct 2024 04:41:30 GMT  
		Size: 26.0 MB (25973828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b992eb71d1a3781cc39688c56ea6aee6aba021d05f3ebb3409c6befcaccca1d2`  
		Last Modified: Tue, 25 Mar 2025 19:54:04 GMT  
		Size: 45.3 MB (45326096 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a087d2afbe4d0f3f89a791aeaf11cdaf6ae77949ec7fe66f01c6cafbe39da741`  
		Last Modified: Tue, 25 Mar 2025 19:54:02 GMT  
		Size: 1.8 KB (1806 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:591065cbe07c9ee71e2b82cf32b81dcb7b8fca4cb2c09e170dfd149386408efc`  
		Last Modified: Tue, 25 Mar 2025 19:54:15 GMT  
		Size: 436.6 MB (436594078 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:971c9b3682921d9a7bcd35680994331e80901c5f0b996ddb38e83844d4618e77`  
		Last Modified: Tue, 25 Mar 2025 19:54:03 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a73389368d795f43904ff5ccc2d2c55717bfefe889ec1bf0bff8c42c661d9c9`  
		Last Modified: Tue, 25 Mar 2025 19:54:03 GMT  
		Size: 1.6 KB (1579 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1f3c56e92f87df3d97bfc5ff6e741f2112b20065017d4caaf2b9ba9f816a619`  
		Last Modified: Tue, 25 Mar 2025 19:54:04 GMT  
		Size: 278.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7cd21411802df91049703d2a8ac609be2a6d8aaa3cf2193aef233ad51351796b`  
		Last Modified: Tue, 25 Mar 2025 19:54:04 GMT  
		Size: 1.8 KB (1764 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:178e0c24c8dd84f4b4ccaea59d16930ef195451aa02f4b9320abaaf1840cb41c`  
		Last Modified: Tue, 25 Mar 2025 19:54:05 GMT  
		Size: 4.1 MB (4054502 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c02d3e33ab38d96da3c165e7ddd5024b7e51f472d1e0fecd28829b53401b2916`  
		Last Modified: Tue, 25 Mar 2025 19:54:06 GMT  
		Size: 2.0 MB (1961022 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2af904b7968987eb1f370d75fbb68fc3924dab9a2450d45e3794e0bd0421ea5`  
		Last Modified: Tue, 25 Mar 2025 19:54:06 GMT  
		Size: 711.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `logstash:8.16.6` - unknown; unknown

```console
$ docker pull logstash@sha256:e6a339f91664ee76d89375118ba7ef1357ca08c4289624b05d2e33a73de02f40
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3554388 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dc8ac7a278c3add75416d26757e1b125889c36059cf4a887584fa1d88c3c6c42`

```dockerfile
```

-	Layers:
	-	`sha256:5995e68816cb367228893d3279fa24caa062d96975b1ed56896231cb7475c7f0`  
		Last Modified: Tue, 25 Mar 2025 19:54:03 GMT  
		Size: 3.5 MB (3519652 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3b24bfa9229cadda9b1b4079f5a0c74215526614226b2996fabcd86c023dd246`  
		Last Modified: Tue, 25 Mar 2025 19:54:02 GMT  
		Size: 34.7 KB (34736 bytes)  
		MIME: application/vnd.in-toto+json

## `logstash:8.17.4`

```console
$ docker pull logstash@sha256:22b4c2aad529320d4faafb6927dc39f62d6bcf6cfa92085e0fe67cae8ec3a036
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `logstash:8.17.4` - linux; amd64

```console
$ docker pull logstash@sha256:18605049922116bd5f20e1103d463f97817d4a2bf5a24bc427a203764984eb9f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **531.4 MB (531439398 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa00adc393cdc7391042e91324bd9a8ade69c240eb27fbdeca31f1ef7907e838`
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
# Tue, 25 Mar 2025 09:28:57 GMT
RUN for iter in {1..10}; do       export DEBIAN_FRONTEND=noninteractive &&     apt-get update -y &&   apt-get upgrade -y &&   apt-get install -y procps findutils tar gzip &&         apt-get install -y locales &&         apt-get install -y curl &&     apt-get clean all &&       locale-gen 'en_US.UTF-8' &&     apt-get clean metadata &&   exit_code=0 && break || exit_code=$? && echo "packaging error: retry $iter in 10s" && apt-get clean all &&   apt-get clean metadata && sleep 10; done; (exit $exit_code) # buildkit
# Tue, 25 Mar 2025 09:28:57 GMT
RUN groupadd --gid 1000 logstash &&   adduser --uid 1000 --gid 1000 --home /usr/share/logstash --no-create-home logstash # buildkit
# Tue, 25 Mar 2025 09:28:57 GMT
RUN curl -Lo - https://artifacts.elastic.co/downloads/logstash/logstash-8.17.4-linux-$(arch).tar.gz |   tar zxf - -C /usr/share &&   mv /usr/share/logstash-8.17.4 /usr/share/logstash &&   chown --recursive logstash:logstash /usr/share/logstash/ &&   chown -R logstash:root /usr/share/logstash &&   chmod -R g=u /usr/share/logstash &&   mkdir /licenses/ &&   mv /usr/share/logstash/NOTICE.TXT /licenses/NOTICE.TXT &&   mv /usr/share/logstash/LICENSE.txt /licenses/LICENSE.txt &&   find /usr/share/logstash -type d -exec chmod g+s {} \; &&   ln -s /usr/share/logstash /opt/logstash # buildkit
# Tue, 25 Mar 2025 09:28:57 GMT
WORKDIR /usr/share/logstash
# Tue, 25 Mar 2025 09:28:57 GMT
ENV ELASTIC_CONTAINER=true
# Tue, 25 Mar 2025 09:28:57 GMT
ENV PATH=/usr/share/logstash/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 25 Mar 2025 09:28:57 GMT
COPY config/logstash-full.yml config/logstash.yml # buildkit
# Tue, 25 Mar 2025 09:28:57 GMT
COPY config/pipelines.yml config/log4j2.properties config/log4j2.file.properties config/ # buildkit
# Tue, 25 Mar 2025 09:28:57 GMT
COPY pipeline/default.conf pipeline/logstash.conf # buildkit
# Tue, 25 Mar 2025 09:28:57 GMT
RUN chown --recursive logstash:root config/ pipeline/ # buildkit
# Tue, 25 Mar 2025 09:28:57 GMT
ENV LANG=en_US.UTF-8 LC_ALL=en_US.UTF-8
# Tue, 25 Mar 2025 09:28:57 GMT
COPY env2yaml/env2yaml-amd64 env2yaml/env2yaml-arm64 env2yaml/ # buildkit
# Tue, 25 Mar 2025 09:28:57 GMT
RUN set -eux; env2yamlarch="$(dpkg --print-architecture)";   case "${env2yamlarch}" in     'x86_64'|'amd64')       env2yamlarch=amd64;       ;;     'aarch64'|'arm64')       env2yamlarch=arm64;       ;;     *) echo >&2 "error: unsupported architecture '$env2yamlarch'"; exit 1 ;;   esac;   mkdir -p /usr/local/bin;   cp env2yaml/env2yaml-${env2yamlarch} /usr/local/bin/env2yaml;   rm -rf env2yaml # buildkit
# Tue, 25 Mar 2025 09:28:57 GMT
COPY bin/docker-entrypoint /usr/local/bin/ # buildkit
# Tue, 25 Mar 2025 09:28:57 GMT
RUN chmod 0755 /usr/local/bin/docker-entrypoint # buildkit
# Tue, 25 Mar 2025 09:28:57 GMT
USER 1000
# Tue, 25 Mar 2025 09:28:57 GMT
EXPOSE map[5044/tcp:{} 9600/tcp:{}]
# Tue, 25 Mar 2025 09:28:57 GMT
LABEL org.label-schema.schema-version=1.0 org.label-schema.vendor=Elastic org.opencontainers.image.vendor=Elastic org.label-schema.name=logstash org.opencontainers.image.title=logstash org.label-schema.version=8.17.4 org.opencontainers.image.version=8.17.4 org.label-schema.url=https://www.elastic.co/products/logstash org.label-schema.vcs-url=https://github.com/elastic/logstash org.label-schema.license=Elastic License org.opencontainers.image.licenses=Elastic License org.opencontainers.image.description=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' org.label-schema.build-date=2025-03-19T17:05:46+00:00 org.opencontainers.image.created=2025-03-19T17:05:46+00:00
# Tue, 25 Mar 2025 09:28:57 GMT
ENTRYPOINT ["/usr/local/bin/docker-entrypoint"]
```

-	Layers:
	-	`sha256:d9802f032d6798e2086607424bfe88cb8ec1d6f116e11cd99592dcaf261e9cd2`  
		Last Modified: Fri, 11 Oct 2024 04:41:25 GMT  
		Size: 27.5 MB (27511060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b214221bf27a2fb5ab59fe1f3f46276f22146ad2bd20be314d3442b10fefad76`  
		Last Modified: Tue, 25 Mar 2025 19:45:18 GMT  
		Size: 59.1 MB (59086940 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc430179bb83087c6d1c59d20db5cf3139c3afc8589fcf9aa6e1bfc276831024`  
		Last Modified: Tue, 25 Mar 2025 19:45:17 GMT  
		Size: 1.8 KB (1800 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:513ae3c154104d1ad801438e6551c54162fed48422d1f646285b33ecada87c3e`  
		Last Modified: Tue, 25 Mar 2025 19:45:24 GMT  
		Size: 438.7 MB (438686844 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2fd839875b9d6436cb7d1257dace2e75c66bac450eb924c9e382997fd326fdce`  
		Last Modified: Tue, 25 Mar 2025 19:45:17 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7326714b84b746bdcfd3124a8a04887176bc4bedaa01efddce98e6eb832ae2a6`  
		Last Modified: Tue, 25 Mar 2025 19:45:18 GMT  
		Size: 1.6 KB (1581 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c30b003d6d7dc8b035db2a69d5b6d19de1ee46b425f2f3650a06de14a6289d52`  
		Last Modified: Tue, 25 Mar 2025 19:45:18 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1141452e54398d370170f76c7d24ad3040661e708633f8d74344ea370b80a5f3`  
		Last Modified: Tue, 25 Mar 2025 19:45:19 GMT  
		Size: 1.8 KB (1765 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5b58d86655ae62a272f05aad218cef45e0160a3f009ba3984af0efeba8e2064`  
		Last Modified: Tue, 25 Mar 2025 19:45:19 GMT  
		Size: 4.1 MB (4054507 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a3a653f7b5394481c9bbcea18ccd262460cc15ef6423787b358b8ba62be6dbd`  
		Last Modified: Tue, 25 Mar 2025 19:45:20 GMT  
		Size: 2.1 MB (2093570 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83a3d96f29e48591e4a9aa0c04f36392fcb9cdddadcb9f6428d8106839c9c4a2`  
		Last Modified: Tue, 25 Mar 2025 19:45:19 GMT  
		Size: 713.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `logstash:8.17.4` - unknown; unknown

```console
$ docker pull logstash@sha256:5b68883d4bad30c8b0e24d90ad4698804138ad76ec2974ecdfdc0da5f6a744af
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3545576 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e9a181df33fb5f5577e350e4c9e9c483fd6d64a2f514e429d3adc5bf58b9773e`

```dockerfile
```

-	Layers:
	-	`sha256:f896f8ebc691308179ed8a3c2ad47dc14b41be5344a6fb71ea8e86710ba3619f`  
		Last Modified: Tue, 25 Mar 2025 19:45:17 GMT  
		Size: 3.5 MB (3510983 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a5bb9fc76d704ff082fc12935c1c229c2e6c561c4d5cc9ca7a65cd8718e9e0a9`  
		Last Modified: Tue, 25 Mar 2025 19:45:17 GMT  
		Size: 34.6 KB (34593 bytes)  
		MIME: application/vnd.in-toto+json

### `logstash:8.17.4` - linux; arm64 variant v8

```console
$ docker pull logstash@sha256:c9778e8d23d7505ea092a9759f5ec7224e3138fff28bc270f43c65187fd5f7a7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **514.3 MB (514301761 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b1d90d5292fec33398dcaed78d5be8c795f01008da0b2248da0a5dbce85a117`
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
# Tue, 25 Mar 2025 09:28:57 GMT
RUN for iter in {1..10}; do       export DEBIAN_FRONTEND=noninteractive &&     apt-get update -y &&   apt-get upgrade -y &&   apt-get install -y procps findutils tar gzip &&         apt-get install -y locales &&         apt-get install -y curl &&     apt-get clean all &&       locale-gen 'en_US.UTF-8' &&     apt-get clean metadata &&   exit_code=0 && break || exit_code=$? && echo "packaging error: retry $iter in 10s" && apt-get clean all &&   apt-get clean metadata && sleep 10; done; (exit $exit_code) # buildkit
# Tue, 25 Mar 2025 09:28:57 GMT
RUN groupadd --gid 1000 logstash &&   adduser --uid 1000 --gid 1000 --home /usr/share/logstash --no-create-home logstash # buildkit
# Tue, 25 Mar 2025 09:28:57 GMT
RUN curl -Lo - https://artifacts.elastic.co/downloads/logstash/logstash-8.17.4-linux-$(arch).tar.gz |   tar zxf - -C /usr/share &&   mv /usr/share/logstash-8.17.4 /usr/share/logstash &&   chown --recursive logstash:logstash /usr/share/logstash/ &&   chown -R logstash:root /usr/share/logstash &&   chmod -R g=u /usr/share/logstash &&   mkdir /licenses/ &&   mv /usr/share/logstash/NOTICE.TXT /licenses/NOTICE.TXT &&   mv /usr/share/logstash/LICENSE.txt /licenses/LICENSE.txt &&   find /usr/share/logstash -type d -exec chmod g+s {} \; &&   ln -s /usr/share/logstash /opt/logstash # buildkit
# Tue, 25 Mar 2025 09:28:57 GMT
WORKDIR /usr/share/logstash
# Tue, 25 Mar 2025 09:28:57 GMT
ENV ELASTIC_CONTAINER=true
# Tue, 25 Mar 2025 09:28:57 GMT
ENV PATH=/usr/share/logstash/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 25 Mar 2025 09:28:57 GMT
COPY config/logstash-full.yml config/logstash.yml # buildkit
# Tue, 25 Mar 2025 09:28:57 GMT
COPY config/pipelines.yml config/log4j2.properties config/log4j2.file.properties config/ # buildkit
# Tue, 25 Mar 2025 09:28:57 GMT
COPY pipeline/default.conf pipeline/logstash.conf # buildkit
# Tue, 25 Mar 2025 09:28:57 GMT
RUN chown --recursive logstash:root config/ pipeline/ # buildkit
# Tue, 25 Mar 2025 09:28:57 GMT
ENV LANG=en_US.UTF-8 LC_ALL=en_US.UTF-8
# Tue, 25 Mar 2025 09:28:57 GMT
COPY env2yaml/env2yaml-amd64 env2yaml/env2yaml-arm64 env2yaml/ # buildkit
# Tue, 25 Mar 2025 09:28:57 GMT
RUN set -eux; env2yamlarch="$(dpkg --print-architecture)";   case "${env2yamlarch}" in     'x86_64'|'amd64')       env2yamlarch=amd64;       ;;     'aarch64'|'arm64')       env2yamlarch=arm64;       ;;     *) echo >&2 "error: unsupported architecture '$env2yamlarch'"; exit 1 ;;   esac;   mkdir -p /usr/local/bin;   cp env2yaml/env2yaml-${env2yamlarch} /usr/local/bin/env2yaml;   rm -rf env2yaml # buildkit
# Tue, 25 Mar 2025 09:28:57 GMT
COPY bin/docker-entrypoint /usr/local/bin/ # buildkit
# Tue, 25 Mar 2025 09:28:57 GMT
RUN chmod 0755 /usr/local/bin/docker-entrypoint # buildkit
# Tue, 25 Mar 2025 09:28:57 GMT
USER 1000
# Tue, 25 Mar 2025 09:28:57 GMT
EXPOSE map[5044/tcp:{} 9600/tcp:{}]
# Tue, 25 Mar 2025 09:28:57 GMT
LABEL org.label-schema.schema-version=1.0 org.label-schema.vendor=Elastic org.opencontainers.image.vendor=Elastic org.label-schema.name=logstash org.opencontainers.image.title=logstash org.label-schema.version=8.17.4 org.opencontainers.image.version=8.17.4 org.label-schema.url=https://www.elastic.co/products/logstash org.label-schema.vcs-url=https://github.com/elastic/logstash org.label-schema.license=Elastic License org.opencontainers.image.licenses=Elastic License org.opencontainers.image.description=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' org.label-schema.build-date=2025-03-19T17:05:46+00:00 org.opencontainers.image.created=2025-03-19T17:05:46+00:00
# Tue, 25 Mar 2025 09:28:57 GMT
ENTRYPOINT ["/usr/local/bin/docker-entrypoint"]
```

-	Layers:
	-	`sha256:1b9f3c55f9d4aa5c52eb67a4cb7d0f4726ab85a413b50e3e3fe788befce3d297`  
		Last Modified: Fri, 11 Oct 2024 04:41:30 GMT  
		Size: 26.0 MB (25973828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b992eb71d1a3781cc39688c56ea6aee6aba021d05f3ebb3409c6befcaccca1d2`  
		Last Modified: Tue, 25 Mar 2025 19:54:04 GMT  
		Size: 45.3 MB (45326096 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a087d2afbe4d0f3f89a791aeaf11cdaf6ae77949ec7fe66f01c6cafbe39da741`  
		Last Modified: Tue, 25 Mar 2025 19:54:02 GMT  
		Size: 1.8 KB (1806 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2963477387999b0a6718114d6d90c6fc7c2ece88bebc93683ef7e7da6a05328`  
		Last Modified: Tue, 25 Mar 2025 20:05:52 GMT  
		Size: 437.0 MB (436979845 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4caa99343280868689f053bf38e94660333b930ef263c9e1f03cb14794d4573`  
		Last Modified: Tue, 25 Mar 2025 20:05:42 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7439fc7befb6e184d447e2c3431e528a1c4dc17b5e7638f270031d86ce702f33`  
		Last Modified: Tue, 25 Mar 2025 20:05:42 GMT  
		Size: 1.6 KB (1578 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6aa6d9c09294db6892278ed7613a698c685f3b0546bed4451a2dab39bc1fa3e3`  
		Last Modified: Tue, 25 Mar 2025 20:05:42 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:292d22a0c516af252c68b2820c402dcf9858b08b50bb14610e84331bae15c33c`  
		Last Modified: Tue, 25 Mar 2025 20:05:43 GMT  
		Size: 1.8 KB (1763 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77bb81fe4f3164444952da6b04e82cd43de9d9db463d5b0c10352c41a649ff56`  
		Last Modified: Tue, 25 Mar 2025 20:05:44 GMT  
		Size: 4.1 MB (4054500 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a828670b0d5fb6c366688550025864af69f29b98e0e91c912224c406f3c99d22`  
		Last Modified: Tue, 25 Mar 2025 20:05:44 GMT  
		Size: 2.0 MB (1961020 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f3919be392294b3a8d2e5abbc1f23a63587e22740da81fdd181f3c16c256b07`  
		Last Modified: Tue, 25 Mar 2025 20:05:44 GMT  
		Size: 709.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `logstash:8.17.4` - unknown; unknown

```console
$ docker pull logstash@sha256:d31fb8d5c259b6b0fba04112274ea32b148799e24914d5d44e7be8459f37ef07
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3545331 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:350c2e5ca43a36930e8d0e6ad3ab35b52471aff054e74522bac7ee2544dda215`

```dockerfile
```

-	Layers:
	-	`sha256:dfdf643d9e6e09712e0d5e756e7bd4efd2e40826ee1fa839234facb93923a345`  
		Last Modified: Tue, 25 Mar 2025 20:05:43 GMT  
		Size: 3.5 MB (3510595 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:090317d302296d4577b1a9464d2c12761778b763903b8f30fff09ef122762f64`  
		Last Modified: Tue, 25 Mar 2025 20:05:42 GMT  
		Size: 34.7 KB (34736 bytes)  
		MIME: application/vnd.in-toto+json
