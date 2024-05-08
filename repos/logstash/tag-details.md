<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `logstash`

-	[`logstash:7.17.21`](#logstash71721)
-	[`logstash:8.13.3`](#logstash8133)

## `logstash:7.17.21`

```console
$ docker pull logstash@sha256:32fa9ae11e6940e83b0dc4ad0b0d5076c7e20157bb97020c2913052604e5c23d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `logstash:7.17.21` - linux; amd64

```console
$ docker pull logstash@sha256:d10f2b50d4bfdd06dafbbf7cafa04f063a8d4bf6d50012a4872b93e368a84d35
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **444.6 MB (444616089 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a1703a39e1bc9dae6fe380bc2a21d2b1d7c10c7847edae862ca6045ed0aa81b`
-	Entrypoint: `["\/usr\/local\/bin\/docker-entrypoint"]`

```dockerfile
# Sat, 27 Apr 2024 14:03:39 GMT
ARG RELEASE
# Sat, 27 Apr 2024 14:03:39 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 27 Apr 2024 14:03:39 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sat, 27 Apr 2024 14:03:39 GMT
LABEL org.opencontainers.image.version=20.04
# Sat, 27 Apr 2024 14:03:41 GMT
ADD file:e5742fae181dc02a419e48d202fdd6a561b79ccbe7d3415e15e3d2c12e444a2a in / 
# Sat, 27 Apr 2024 14:03:41 GMT
CMD ["/bin/bash"]
# Thu, 02 May 2024 09:08:49 GMT
RUN for iter in {1..10}; do export DEBIAN_FRONTEND=noninteractive && apt-get update -y && apt-get upgrade -y && apt-get install -y procps findutils tar gzip curl && apt-get install -y locales && apt-get clean all && locale-gen 'en_US.UTF-8' &&     apt-get clean metadata && exit_code=0 && break || exit_code=$? &&     echo "packaging error: retry $iter in 10s" &&     apt-get clean all && apt-get clean metadata && sleep 10; done;     (exit $exit_code) # buildkit
# Thu, 02 May 2024 09:08:49 GMT
RUN groupadd --gid 1000 logstash &&     adduser --uid 1000 --gid 1000        --home /usr/share/logstash --no-create-home       logstash # buildkit
# Thu, 02 May 2024 09:08:49 GMT
RUN curl -Lo - https://artifacts.elastic.co/downloads/logstash/logstash-7.17.21-linux-$(arch).tar.gz |     tar zxf - -C /usr/share &&     mv /usr/share/logstash-7.17.21 /usr/share/logstash && chown --recursive logstash:logstash /usr/share/logstash/ &&     chown -R logstash:root /usr/share/logstash &&     chmod -R g=u /usr/share/logstash &&     mkdir /licenses/ &&     mv /usr/share/logstash/NOTICE.TXT /licenses/NOTICE.TXT &&     mv /usr/share/logstash/LICENSE.txt /licenses/LICENSE.txt &&     find /usr/share/logstash -type d -exec chmod g+s {} \; &&     ln -s /usr/share/logstash /opt/logstash # buildkit
# Thu, 02 May 2024 09:08:49 GMT
WORKDIR /usr/share/logstash
# Thu, 02 May 2024 09:08:49 GMT
ENV ELASTIC_CONTAINER=true
# Thu, 02 May 2024 09:08:49 GMT
ENV PATH=/usr/share/logstash/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 02 May 2024 09:08:49 GMT
ADD config/pipelines.yml config/pipelines.yml # buildkit
# Thu, 02 May 2024 09:08:49 GMT
ADD config/logstash-full.yml config/logstash.yml # buildkit
# Thu, 02 May 2024 09:08:49 GMT
ADD config/log4j2.properties config/ # buildkit
# Thu, 02 May 2024 09:08:49 GMT
ADD pipeline/default.conf pipeline/logstash.conf # buildkit
# Thu, 02 May 2024 09:08:49 GMT
RUN chown --recursive logstash:root config/ pipeline/ # buildkit
# Thu, 02 May 2024 09:08:49 GMT
ENV LANG=en_US.UTF-8 LC_ALL=en_US.UTF-8
# Thu, 02 May 2024 09:08:49 GMT
ADD env2yaml/env2yaml /usr/local/bin/ # buildkit
# Thu, 02 May 2024 09:08:49 GMT
ADD bin/docker-entrypoint /usr/local/bin/ # buildkit
# Thu, 02 May 2024 09:08:49 GMT
RUN chmod 0755 /usr/local/bin/docker-entrypoint # buildkit
# Thu, 02 May 2024 09:08:49 GMT
USER 1000
# Thu, 02 May 2024 09:08:49 GMT
EXPOSE map[5044/tcp:{} 9600/tcp:{}]
# Thu, 02 May 2024 09:08:49 GMT
LABEL org.label-schema.schema-version=1.0 org.label-schema.vendor=Elastic org.opencontainers.image.vendor=Elastic org.label-schema.name=logstash org.opencontainers.image.title=logstash org.label-schema.version=7.17.21 org.opencontainers.image.version=7.17.21 org.label-schema.url=https://www.elastic.co/products/logstash org.label-schema.vcs-url=https://github.com/elastic/logstash org.label-schema.license=Elastic License org.opencontainers.image.licenses=Elastic License org.opencontainers.image.description=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' org.label-schema.build-date=2024-04-25T21:20:46+00:00 org.opencontainers.image.created=2024-04-25T21:20:46+00:00
# Thu, 02 May 2024 09:08:49 GMT
ENTRYPOINT ["/usr/local/bin/docker-entrypoint"]
```

-	Layers:
	-	`sha256:d4c3c94e5e10ed15503bda7e145a3652ee935c0b2e9de9b5c98df7ec0a0cd925`  
		Last Modified: Sat, 27 Apr 2024 14:54:51 GMT  
		Size: 27.5 MB (27511657 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21bd16be53b1a57d0e6acb5859ad07ce9405cad7a95be5c108ff877edcfff122`  
		Last Modified: Thu, 02 May 2024 17:53:18 GMT  
		Size: 47.9 MB (47863853 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f867fe86586a16832ed53b0fd7d1074189bd925dfb07a56d2046602cf9500c2`  
		Last Modified: Thu, 02 May 2024 17:53:18 GMT  
		Size: 1.8 KB (1800 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ee7a5266121f1323b1e9c05ba8acfe17825b454c7c314502254b60057e02308`  
		Last Modified: Thu, 02 May 2024 17:53:25 GMT  
		Size: 367.3 MB (367333259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f8634f20cf3cf908a2eb301e2c8a53f211ece43b5b5b9d434ab8dd96d15abf7`  
		Last Modified: Thu, 02 May 2024 17:53:18 GMT  
		Size: 377.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a642815b31a57374eb49f785a024f1654887613c8402fc2ea41500bf6d826df7`  
		Last Modified: Thu, 02 May 2024 17:53:19 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:607ce8d8a777166ffd713c620788fc190e3a3f236202baa390d2d257dd0a7bea`  
		Last Modified: Thu, 02 May 2024 17:53:19 GMT  
		Size: 471.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d865ebb4b4a0a061896177a21aaa0ab13c3ac6312b9bea75417e9a396c2a8559`  
		Last Modified: Thu, 02 May 2024 17:53:20 GMT  
		Size: 278.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4cbe4e3b68eaf1c34e3ce5f59c6dac38a3bacd71b7b6347d0012b661d353b6e9`  
		Last Modified: Thu, 02 May 2024 17:53:20 GMT  
		Size: 825.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42afb9e94cc94708d60282fd0473cb902cdf45ced69778a2a019bee377adc5d4`  
		Last Modified: Thu, 02 May 2024 17:53:20 GMT  
		Size: 1.9 MB (1902738 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9360956bc73b24920e5c150313dadeccd623d31f1877604f84b644f91d199658`  
		Last Modified: Thu, 02 May 2024 17:53:21 GMT  
		Size: 491.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `logstash:7.17.21` - unknown; unknown

```console
$ docker pull logstash@sha256:252ebc23f05ccbcaa34eb664796dbe8f3694105b2f3436ac11132d711650e17d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (3010640 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:18b11c5a5f8fa62964e747ce8c35acf5b77a5411bb7d42aceb23106a93a7e112`

```dockerfile
```

-	Layers:
	-	`sha256:00a28dda92f1e18aea5b27a03d2a5fe9d52cc07464a035ecdac94903473713ac`  
		Last Modified: Thu, 02 May 2024 17:53:18 GMT  
		Size: 3.0 MB (2978468 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1c1ca843b0fba6b01c1ffa24532e0a2df8ee8155338737e7893359139d71bcdb`  
		Last Modified: Thu, 02 May 2024 17:53:18 GMT  
		Size: 32.2 KB (32172 bytes)  
		MIME: application/vnd.in-toto+json

### `logstash:7.17.21` - linux; arm64 variant v8

```console
$ docker pull logstash@sha256:c4eacbb75b8c0120edf026f860c8ef6f8723d894cfe8979661b7ee46192b4bfd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **429.3 MB (429323818 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c67109d704ba19b4fb4eedca24024bfa8484d9038ce8820b86065b7ed33c8a1e`
-	Entrypoint: `["\/usr\/local\/bin\/docker-entrypoint"]`

```dockerfile
# Sat, 27 Apr 2024 14:42:15 GMT
ARG RELEASE
# Sat, 27 Apr 2024 14:42:15 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 27 Apr 2024 14:42:15 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sat, 27 Apr 2024 14:42:15 GMT
LABEL org.opencontainers.image.version=20.04
# Sat, 27 Apr 2024 14:42:24 GMT
ADD file:d1a4a31f5a3aea1e130c7e173da2ed506ba19e91be74ab9700d398774d0ace22 in / 
# Sat, 27 Apr 2024 14:42:24 GMT
CMD ["/bin/bash"]
# Thu, 02 May 2024 09:08:49 GMT
RUN for iter in {1..10}; do export DEBIAN_FRONTEND=noninteractive && apt-get update -y && apt-get upgrade -y && apt-get install -y procps findutils tar gzip curl && apt-get install -y locales && apt-get clean all && locale-gen 'en_US.UTF-8' &&     apt-get clean metadata && exit_code=0 && break || exit_code=$? &&     echo "packaging error: retry $iter in 10s" &&     apt-get clean all && apt-get clean metadata && sleep 10; done;     (exit $exit_code) # buildkit
# Thu, 02 May 2024 09:08:49 GMT
RUN groupadd --gid 1000 logstash &&     adduser --uid 1000 --gid 1000        --home /usr/share/logstash --no-create-home       logstash # buildkit
# Thu, 02 May 2024 09:08:49 GMT
RUN curl -Lo - https://artifacts.elastic.co/downloads/logstash/logstash-7.17.21-linux-$(arch).tar.gz |     tar zxf - -C /usr/share &&     mv /usr/share/logstash-7.17.21 /usr/share/logstash && chown --recursive logstash:logstash /usr/share/logstash/ &&     chown -R logstash:root /usr/share/logstash &&     chmod -R g=u /usr/share/logstash &&     mkdir /licenses/ &&     mv /usr/share/logstash/NOTICE.TXT /licenses/NOTICE.TXT &&     mv /usr/share/logstash/LICENSE.txt /licenses/LICENSE.txt &&     find /usr/share/logstash -type d -exec chmod g+s {} \; &&     ln -s /usr/share/logstash /opt/logstash # buildkit
# Thu, 02 May 2024 09:08:49 GMT
WORKDIR /usr/share/logstash
# Thu, 02 May 2024 09:08:49 GMT
ENV ELASTIC_CONTAINER=true
# Thu, 02 May 2024 09:08:49 GMT
ENV PATH=/usr/share/logstash/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 02 May 2024 09:08:49 GMT
ADD config/pipelines.yml config/pipelines.yml # buildkit
# Thu, 02 May 2024 09:08:49 GMT
ADD config/logstash-full.yml config/logstash.yml # buildkit
# Thu, 02 May 2024 09:08:49 GMT
ADD config/log4j2.properties config/ # buildkit
# Thu, 02 May 2024 09:08:49 GMT
ADD pipeline/default.conf pipeline/logstash.conf # buildkit
# Thu, 02 May 2024 09:08:49 GMT
RUN chown --recursive logstash:root config/ pipeline/ # buildkit
# Thu, 02 May 2024 09:08:49 GMT
ENV LANG=en_US.UTF-8 LC_ALL=en_US.UTF-8
# Thu, 02 May 2024 09:08:49 GMT
ADD env2yaml/env2yaml /usr/local/bin/ # buildkit
# Thu, 02 May 2024 09:08:49 GMT
ADD bin/docker-entrypoint /usr/local/bin/ # buildkit
# Thu, 02 May 2024 09:08:49 GMT
RUN chmod 0755 /usr/local/bin/docker-entrypoint # buildkit
# Thu, 02 May 2024 09:08:49 GMT
USER 1000
# Thu, 02 May 2024 09:08:49 GMT
EXPOSE map[5044/tcp:{} 9600/tcp:{}]
# Thu, 02 May 2024 09:08:49 GMT
LABEL org.label-schema.schema-version=1.0 org.label-schema.vendor=Elastic org.opencontainers.image.vendor=Elastic org.label-schema.name=logstash org.opencontainers.image.title=logstash org.label-schema.version=7.17.21 org.opencontainers.image.version=7.17.21 org.label-schema.url=https://www.elastic.co/products/logstash org.label-schema.vcs-url=https://github.com/elastic/logstash org.label-schema.license=Elastic License org.opencontainers.image.licenses=Elastic License org.opencontainers.image.description=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' org.label-schema.build-date=2024-04-25T21:20:46+00:00 org.opencontainers.image.created=2024-04-25T21:20:46+00:00
# Thu, 02 May 2024 09:08:49 GMT
ENTRYPOINT ["/usr/local/bin/docker-entrypoint"]
```

-	Layers:
	-	`sha256:d7044108e6d4d8b24ea68c7ee675f78cb56d959d0878b78c97e8ca7c6b5fa2cc`  
		Last Modified: Sat, 27 Apr 2024 14:55:02 GMT  
		Size: 26.0 MB (25975500 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:421bb92fcde17234c65ded00edea0a5733401dbc11f167efe6cfc7199320932d`  
		Last Modified: Thu, 02 May 2024 11:53:33 GMT  
		Size: 37.4 MB (37393222 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2bd9bd267d032bf3ee2a77d78f3005e8ea29651716b45de12034591f0c189473`  
		Last Modified: Thu, 02 May 2024 11:53:32 GMT  
		Size: 1.8 KB (1808 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a9a4d4a25fca1775b4d604ec707fc6407f1444741c9d7f4fbb544a3a6c177c0`  
		Last Modified: Thu, 02 May 2024 18:17:41 GMT  
		Size: 364.0 MB (364047750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14c03f6f420f1cdc193282e52088dab3198425efdcbbb1b55e7eaef934edcf82`  
		Last Modified: Thu, 02 May 2024 18:17:34 GMT  
		Size: 380.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8aef8ebf5d97a618116b78cb54269e70c3bcbcfc5eccc8a959b60cec4ec375a`  
		Last Modified: Thu, 02 May 2024 18:17:34 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70c140f8d3231974bfe85cffe71469cf2fb005a866aa951bd193bab71ab7b287`  
		Last Modified: Thu, 02 May 2024 18:17:34 GMT  
		Size: 474.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2707967f8be88e72b6e7fbb42c57e6148aac6ebace5f68be5965f390dc4a6b5`  
		Last Modified: Thu, 02 May 2024 18:17:35 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:842547debd7494a508b24beb3e960da836022b0cab7685ce3e7218ef7f946400`  
		Last Modified: Thu, 02 May 2024 18:17:35 GMT  
		Size: 828.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54365b377fdd20acbc04ac5b308b301176eeda7174ecc65f1f646864f37a2b8c`  
		Last Modified: Thu, 02 May 2024 18:17:36 GMT  
		Size: 1.9 MB (1902742 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5442fa5deb3208971fd720cac18bd0f60701dd84f3c1440b8474911576fac58b`  
		Last Modified: Thu, 02 May 2024 18:17:36 GMT  
		Size: 493.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `logstash:7.17.21` - unknown; unknown

```console
$ docker pull logstash@sha256:eac24405411e4ce76865b276c7d3229b1b25c6cc5095bcd7cf10f5d2239e65c5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (3010704 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:910ac514591de5d2895a8a28fb7c88502d882232161cc6fc94547760e1e73984`

```dockerfile
```

-	Layers:
	-	`sha256:49c7172e5e798ea5538aaa8ddc9ced9c37d53eb4488720862adbe5fb0d100f1c`  
		Last Modified: Thu, 02 May 2024 18:17:34 GMT  
		Size: 3.0 MB (2978688 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a94c99c8ceeeb65591dc9cd35f188c0165dbc6c17f107284987e0a77b7ea9b24`  
		Last Modified: Thu, 02 May 2024 18:17:33 GMT  
		Size: 32.0 KB (32016 bytes)  
		MIME: application/vnd.in-toto+json

## `logstash:8.13.3`

```console
$ docker pull logstash@sha256:daea83018367c6a6099ae1fb557315821229da308e0a6fef48cca9ba8097630a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `logstash:8.13.3` - linux; amd64

```console
$ docker pull logstash@sha256:42a99f350fd7c3b39824f1a08c304e8d949d20d8e705213afc820e9422351c9f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **486.4 MB (486378595 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ccc23df93bc30e98c4370e7ba5ad37c46a1ac17f8d1cbe634d197774b64cff2c`
-	Entrypoint: `["\/usr\/local\/bin\/docker-entrypoint"]`

```dockerfile
# Sat, 27 Apr 2024 14:03:39 GMT
ARG RELEASE
# Sat, 27 Apr 2024 14:03:39 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 27 Apr 2024 14:03:39 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sat, 27 Apr 2024 14:03:39 GMT
LABEL org.opencontainers.image.version=20.04
# Sat, 27 Apr 2024 14:03:41 GMT
ADD file:e5742fae181dc02a419e48d202fdd6a561b79ccbe7d3415e15e3d2c12e444a2a in / 
# Sat, 27 Apr 2024 14:03:41 GMT
CMD ["/bin/bash"]
# Thu, 02 May 2024 17:24:52 GMT
RUN for iter in {1..10}; do   export DEBIAN_FRONTEND=noninteractive && apt-get update -y && apt-get upgrade -y && apt-get install -y procps findutils tar gzip &&   apt-get install -y locales &&   apt-get install -y curl && apt-get clean all &&   locale-gen 'en_US.UTF-8' &&   apt-get clean metadata && exit_code=0 && break || exit_code=$? && echo "packaging error: retry $iter in 10s" && apt-get clean all &&   apt-get clean metadata && sleep 10; done; (exit $exit_code) # buildkit
# Thu, 02 May 2024 17:24:52 GMT
RUN groupadd --gid 1000 logstash &&   adduser --uid 1000 --gid 1000 --home /usr/share/logstash --no-create-home logstash # buildkit
# Thu, 02 May 2024 17:24:52 GMT
RUN curl -Lo - https://artifacts.elastic.co/downloads/logstash/logstash-8.13.3-linux-$(arch).tar.gz |   tar zxf - -C /usr/share &&   mv /usr/share/logstash-8.13.3 /usr/share/logstash &&   chown --recursive logstash:logstash /usr/share/logstash/ &&   chown -R logstash:root /usr/share/logstash &&   chmod -R g=u /usr/share/logstash &&   mkdir /licenses/ &&   mv /usr/share/logstash/NOTICE.TXT /licenses/NOTICE.TXT &&   mv /usr/share/logstash/LICENSE.txt /licenses/LICENSE.txt &&   find /usr/share/logstash -type d -exec chmod g+s {} \; &&   ln -s /usr/share/logstash /opt/logstash # buildkit
# Thu, 02 May 2024 17:24:52 GMT
WORKDIR /usr/share/logstash
# Thu, 02 May 2024 17:24:52 GMT
ENV ELASTIC_CONTAINER=true
# Thu, 02 May 2024 17:24:52 GMT
ENV PATH=/usr/share/logstash/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 02 May 2024 17:24:52 GMT
COPY config/pipelines.yml config/pipelines.yml # buildkit
# Thu, 02 May 2024 17:24:52 GMT
COPY config/logstash-full.yml config/logstash.yml # buildkit
# Thu, 02 May 2024 17:24:52 GMT
COPY config/log4j2.properties config/ # buildkit
# Thu, 02 May 2024 17:24:52 GMT
COPY config/log4j2.file.properties config/ # buildkit
# Thu, 02 May 2024 17:24:52 GMT
COPY pipeline/default.conf pipeline/logstash.conf # buildkit
# Thu, 02 May 2024 17:24:52 GMT
COPY env2yaml/env2yaml-amd64 env2yaml/ # buildkit
# Thu, 02 May 2024 17:24:52 GMT
COPY env2yaml/env2yaml-arm64 env2yaml/ # buildkit
# Thu, 02 May 2024 17:24:52 GMT
RUN chown --recursive logstash:root config/ pipeline/ # buildkit
# Thu, 02 May 2024 17:24:52 GMT
ENV LANG=en_US.UTF-8 LC_ALL=en_US.UTF-8
# Thu, 02 May 2024 17:24:52 GMT
RUN env2yamlarch="$(dpkg --print-architecture)";   case "${env2yamlarch}" in     'x86_64'|'amd64')       env2yamlarch=amd64;       ;;     'aarch64'|'arm64')       env2yamlarch=arm64;       ;;     *) echo >&2 "error: unsupported architecture '$env2yamlarch'"; exit 1 ;;   esac;   cp env2yaml/env2yaml-${env2yamlarch} /usr/local/bin/env2yaml;   rm -rf env2yaml # buildkit
# Thu, 02 May 2024 17:24:52 GMT
COPY bin/docker-entrypoint /usr/local/bin/ # buildkit
# Thu, 02 May 2024 17:24:52 GMT
RUN chmod 0755 /usr/local/bin/docker-entrypoint # buildkit
# Thu, 02 May 2024 17:24:52 GMT
USER 1000
# Thu, 02 May 2024 17:24:52 GMT
EXPOSE map[5044/tcp:{} 9600/tcp:{}]
# Thu, 02 May 2024 17:24:52 GMT
LABEL org.label-schema.schema-version=1.0 org.label-schema.vendor=Elastic org.opencontainers.image.vendor=Elastic org.label-schema.name=logstash org.opencontainers.image.title=logstash org.label-schema.version=8.13.3 org.opencontainers.image.version=8.13.3 org.label-schema.url=https://www.elastic.co/products/logstash org.label-schema.vcs-url=https://github.com/elastic/logstash org.label-schema.license=Elastic License org.opencontainers.image.licenses=Elastic License org.opencontainers.image.description=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' org.label-schema.build-date=2024-04-25T21:23:18+00:00 org.opencontainers.image.created=2024-04-25T21:23:18+00:00
# Thu, 02 May 2024 17:24:52 GMT
ENTRYPOINT ["/usr/local/bin/docker-entrypoint"]
```

-	Layers:
	-	`sha256:d4c3c94e5e10ed15503bda7e145a3652ee935c0b2e9de9b5c98df7ec0a0cd925`  
		Last Modified: Sat, 27 Apr 2024 14:54:51 GMT  
		Size: 27.5 MB (27511657 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ba24d07db03ada07ee1cbdf987b281a23404df04d0a5201ab0b1abbeb01347e`  
		Last Modified: Tue, 07 May 2024 21:52:28 GMT  
		Size: 48.0 MB (48022535 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3dff04a0b484c3f12606d69d4d5d03a3fbfa3c69c522b4d085c726f593cc5ff2`  
		Last Modified: Tue, 07 May 2024 21:52:26 GMT  
		Size: 1.8 KB (1802 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4afc7999d79faeb9ff63f8d57d2b53d10484bbe9a735c09d0e0fd7a372e65d21`  
		Last Modified: Tue, 07 May 2024 21:52:34 GMT  
		Size: 405.2 MB (405246239 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:561bcb263ed423df1da957d7fcf6c268b32d53c7715864746625872eb8852760`  
		Last Modified: Tue, 07 May 2024 21:52:26 GMT  
		Size: 380.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ecddd49c7860163ecda1d03bcc04112419fe15ef7c2635036cb7faed7ea005d7`  
		Last Modified: Tue, 07 May 2024 21:52:27 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b16bd1a9400119a827dca07e416a741c9a3ed110211a5dbf8d65b1a4c457f8b`  
		Last Modified: Tue, 07 May 2024 21:52:28 GMT  
		Size: 474.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fae38ca383b1dc349fbfa45cc4411eec969197c36c77c7a20ab110232f63e904`  
		Last Modified: Tue, 07 May 2024 21:52:28 GMT  
		Size: 1.4 KB (1360 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30b8530eac5963eaf2d9fb5843c81760faa8d5944beed68769378fff7e5e45db`  
		Last Modified: Tue, 07 May 2024 21:52:29 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c2dc10a29def7c9cc33967758d5499c90f8af3acbd252d56d85f4fa06e494e7`  
		Last Modified: Tue, 07 May 2024 21:52:29 GMT  
		Size: 1.9 MB (1902192 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e36a7b21241ad8d97b73e5b03d15dcac10a9769d8e99873d5bcf97325aab0f34`  
		Last Modified: Tue, 07 May 2024 21:52:29 GMT  
		Size: 1.8 MB (1786634 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:583225fe6f24fbecc95994056101c32e7816df647bec384d5a71794864d4f443`  
		Last Modified: Tue, 07 May 2024 21:52:30 GMT  
		Size: 1.8 KB (1762 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3318239428c4e1a06384b94c116639c119133d3f6d8640bc91c622ba33a06ab2`  
		Last Modified: Tue, 07 May 2024 21:52:31 GMT  
		Size: 1.9 MB (1902232 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:765e3fb48a100094c99bd2dc7488a07738404601fd2a750b6854c8e5627c3e17`  
		Last Modified: Tue, 07 May 2024 21:52:31 GMT  
		Size: 711.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `logstash:8.13.3` - unknown; unknown

```console
$ docker pull logstash@sha256:70c02c0f2f6b07aa922bc27ec626367ff73d7b1cf2a9441d6d2e4bed6800a834
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3167400 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3fb128dbb6160da3507c53491cd349be04b66f405a2065d62e07f6bc55993cee`

```dockerfile
```

-	Layers:
	-	`sha256:63356a4f7f1892975cae4fa0615ea7fa6f3dbb574e5c0172e019b332ab067461`  
		Last Modified: Tue, 07 May 2024 21:52:26 GMT  
		Size: 3.1 MB (3125252 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c9acba7b4e0acfbdc04f5f94d923e128608dd3f89815cfb453423da60882c037`  
		Last Modified: Tue, 07 May 2024 21:52:26 GMT  
		Size: 42.1 KB (42148 bytes)  
		MIME: application/vnd.in-toto+json
