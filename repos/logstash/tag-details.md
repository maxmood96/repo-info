<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `logstash`

-	[`logstash:7.17.27`](#logstash71727)
-	[`logstash:8.16.2`](#logstash8162)
-	[`logstash:8.17.0`](#logstash8170)

## `logstash:7.17.27`

```console
$ docker pull logstash@sha256:ef677b761a0ff04fca8d72b33b2ac6e9f78818d7ce204ac6ae26f33db5a56038
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `logstash:7.17.27` - linux; amd64

```console
$ docker pull logstash@sha256:437cb89a43d71203e3d4b0c983e3f3b342e99b2035a4389f47060be791200744
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **451.5 MB (451515920 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:783a6d1f20b254f588918594eab84f8174a0312b3216090fb776194179c816b7`
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
# Tue, 14 Jan 2025 19:20:58 GMT
RUN for iter in {1..10}; do     export DEBIAN_FRONTEND=noninteractive &&     apt-get update -y &&     apt-get upgrade -y &&     apt-get install -y procps findutils tar gzip curl &&     apt-get install -y locales &&     apt-get clean all &&     locale-gen 'en_US.UTF-8' &&     apt-get clean metadata &&     exit_code=0 && break || exit_code=$? &&     echo "packaging error: retry $iter in 10s" &&     apt-get clean all &&     apt-get clean metadata &&     sleep 10; done;     (exit $exit_code) # buildkit
# Tue, 14 Jan 2025 19:20:58 GMT
RUN groupadd --gid 1000 logstash &&     adduser --uid 1000 --gid 1000     --home /usr/share/logstash --no-create-home     logstash # buildkit
# Tue, 14 Jan 2025 19:20:58 GMT
RUN curl -Lo - https://artifacts.elastic.co/downloads/logstash/logstash-7.17.27-linux-$(arch).tar.gz |     tar zxf - -C /usr/share &&     mv /usr/share/logstash-7.17.27 /usr/share/logstash &&     chown --recursive logstash:logstash /usr/share/logstash/ &&     chown -R logstash:root /usr/share/logstash &&     chmod -R g=u /usr/share/logstash &&     mkdir /licenses/ &&     mv /usr/share/logstash/NOTICE.TXT /licenses/NOTICE.TXT &&     mv /usr/share/logstash/LICENSE.txt /licenses/LICENSE.txt &&     find /usr/share/logstash -type d -exec chmod g+s {} \; &&     ln -s /usr/share/logstash /opt/logstash # buildkit
# Tue, 14 Jan 2025 19:20:58 GMT
WORKDIR /usr/share/logstash
# Tue, 14 Jan 2025 19:20:58 GMT
ENV ELASTIC_CONTAINER=true
# Tue, 14 Jan 2025 19:20:58 GMT
ENV PATH=/usr/share/logstash/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 14 Jan 2025 19:20:58 GMT
COPY config/pipelines.yml config/pipelines.yml # buildkit
# Tue, 14 Jan 2025 19:20:58 GMT
COPY config/logstash-full.yml config/logstash.yml # buildkit
# Tue, 14 Jan 2025 19:20:58 GMT
COPY config/log4j2.properties config/ # buildkit
# Tue, 14 Jan 2025 19:20:58 GMT
COPY pipeline/default.conf pipeline/logstash.conf # buildkit
# Tue, 14 Jan 2025 19:20:58 GMT
RUN chown --recursive logstash:root config/ pipeline/ # buildkit
# Tue, 14 Jan 2025 19:20:58 GMT
ENV LANG=en_US.UTF-8 LC_ALL=en_US.UTF-8
# Tue, 14 Jan 2025 19:20:58 GMT
COPY env2yaml/env2yaml /usr/local/bin/ # buildkit
# Tue, 14 Jan 2025 19:20:58 GMT
COPY bin/docker-entrypoint /usr/local/bin/ # buildkit
# Tue, 14 Jan 2025 19:20:58 GMT
RUN chmod 0755 /usr/local/bin/docker-entrypoint # buildkit
# Tue, 14 Jan 2025 19:20:58 GMT
USER 1000
# Tue, 14 Jan 2025 19:20:58 GMT
EXPOSE map[5044/tcp:{} 9600/tcp:{}]
# Tue, 14 Jan 2025 19:20:58 GMT
LABEL org.label-schema.schema-version=1.0 org.label-schema.vendor=Elastic org.opencontainers.image.vendor=Elastic org.label-schema.name=logstash org.opencontainers.image.title=logstash org.label-schema.version=7.17.27 org.opencontainers.image.version=7.17.27 org.label-schema.url=https://www.elastic.co/products/logstash org.label-schema.vcs-url=https://github.com/elastic/logstash org.label-schema.license=Elastic License org.opencontainers.image.licenses=Elastic License org.opencontainers.image.description=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' org.label-schema.build-date=2025-01-07T18:11:24+00:00 org.opencontainers.image.created=2025-01-07T18:11:24+00:00
# Tue, 14 Jan 2025 19:20:58 GMT
ENTRYPOINT ["/usr/local/bin/docker-entrypoint"]
```

-	Layers:
	-	`sha256:d9802f032d6798e2086607424bfe88cb8ec1d6f116e11cd99592dcaf261e9cd2`  
		Last Modified: Fri, 13 Dec 2024 13:08:34 GMT  
		Size: 27.5 MB (27511060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd33058be4cd2506de6cb2935b1e7d68b36f7e5c015de5b7ac0a23b90e0243b5`  
		Last Modified: Tue, 14 Jan 2025 22:54:18 GMT  
		Size: 50.9 MB (50934588 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb1594f29e7c4e5e8ab33efbe8cccd45fa6aede07941212b5aaa4ea2ee0b97af`  
		Last Modified: Tue, 14 Jan 2025 20:28:31 GMT  
		Size: 1.8 KB (1803 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d14880be545b185b83525b5b94dcce04c08098168af0ff3240c51f87bddc78ce`  
		Last Modified: Tue, 14 Jan 2025 22:54:28 GMT  
		Size: 371.0 MB (370999278 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03a51655eebfe06bca503122097285751ae898dbc9dae344705772ff82bcac75`  
		Last Modified: Tue, 14 Jan 2025 23:15:16 GMT  
		Size: 379.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51b8038b148a04c56b03c30ad25e675e9c265f2a52fe741f20257bd4e4303c1c`  
		Last Modified: Tue, 14 Jan 2025 22:54:14 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d60e9b8156b8774126c46f06b0870ec5fbe34bd632d442188da373a1230fdd8`  
		Last Modified: Tue, 14 Jan 2025 23:14:42 GMT  
		Size: 474.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a18f28c337a79a98b1ce53470028968202888d840d28c582825e9047a55306a`  
		Last Modified: Tue, 14 Jan 2025 23:15:18 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1f154696cacfcce12dd854a60355f6733d4ceeb41085940e1bc80644ed72348`  
		Last Modified: Tue, 14 Jan 2025 23:15:18 GMT  
		Size: 830.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac4e13ffed2ce3cba3275c264fd8c67e9488354337b5c802383d138059f31e1f`  
		Last Modified: Tue, 14 Jan 2025 20:28:33 GMT  
		Size: 2.1 MB (2066395 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8c17004626d6ef861a2a85e5d3fbc31cf9cfa482857fcd11bcdb8b51a2161a8`  
		Last Modified: Tue, 14 Jan 2025 20:28:33 GMT  
		Size: 493.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `logstash:7.17.27` - unknown; unknown

```console
$ docker pull logstash@sha256:2d55c8e10a1042ed07546183a616fc4e71ea0293988984aecac26e9657effcb8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3335723 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:31a02fec3e07772e71e7f2fc05e9f8471f2ee973b4776895667fd315d0c2d330`

```dockerfile
```

-	Layers:
	-	`sha256:528ea07606b5a7bbc49ad7fe6b9671f3a515f7c5c5eb7ef47aa1cc34d91f9376`  
		Last Modified: Tue, 14 Jan 2025 20:28:31 GMT  
		Size: 3.3 MB (3303537 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fcca1374a9dee9d50a32c5da34ad23ace32ba0bcb304e7cc68a4e6a7752c2959`  
		Last Modified: Tue, 14 Jan 2025 20:28:31 GMT  
		Size: 32.2 KB (32186 bytes)  
		MIME: application/vnd.in-toto+json

## `logstash:8.16.2`

```console
$ docker pull logstash@sha256:c3c26b28428b1cb2ba12a04b24842b0b3bc9fdb64cee1c475c70d7e83cffd2d7
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `logstash:8.16.2` - linux; amd64

```console
$ docker pull logstash@sha256:668ddc3b8bcd116cdbd7abfbc51ce13907f575248b2d01877e96dc4b5c0074a5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **520.5 MB (520539132 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a2b13dcf37f19152daef772bafb3eaf7bf2bd29dc2a2da5e1075a0447b215a7f`
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
# Tue, 17 Dec 2024 15:31:13 GMT
RUN for iter in {1..10}; do       export DEBIAN_FRONTEND=noninteractive &&     apt-get update -y &&   apt-get upgrade -y &&   apt-get install -y procps findutils tar gzip &&         apt-get install -y locales &&         apt-get install -y curl &&     apt-get clean all &&       locale-gen 'en_US.UTF-8' &&     apt-get clean metadata &&   exit_code=0 && break || exit_code=$? && echo "packaging error: retry $iter in 10s" && apt-get clean all &&   apt-get clean metadata && sleep 10; done; (exit $exit_code) # buildkit
# Tue, 17 Dec 2024 15:31:13 GMT
RUN groupadd --gid 1000 logstash &&   adduser --uid 1000 --gid 1000 --home /usr/share/logstash --no-create-home logstash # buildkit
# Tue, 17 Dec 2024 15:31:13 GMT
RUN curl -Lo - https://artifacts.elastic.co/downloads/logstash/logstash-8.16.2-linux-$(arch).tar.gz |   tar zxf - -C /usr/share &&   mv /usr/share/logstash-8.16.2 /usr/share/logstash &&   chown --recursive logstash:logstash /usr/share/logstash/ &&   chown -R logstash:root /usr/share/logstash &&   chmod -R g=u /usr/share/logstash &&   mkdir /licenses/ &&   mv /usr/share/logstash/NOTICE.TXT /licenses/NOTICE.TXT &&   mv /usr/share/logstash/LICENSE.txt /licenses/LICENSE.txt &&   find /usr/share/logstash -type d -exec chmod g+s {} \; &&   ln -s /usr/share/logstash /opt/logstash # buildkit
# Tue, 17 Dec 2024 15:31:13 GMT
WORKDIR /usr/share/logstash
# Tue, 17 Dec 2024 15:31:13 GMT
ENV ELASTIC_CONTAINER=true
# Tue, 17 Dec 2024 15:31:13 GMT
ENV PATH=/usr/share/logstash/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Dec 2024 15:31:13 GMT
COPY config/logstash-full.yml config/logstash.yml # buildkit
# Tue, 17 Dec 2024 15:31:13 GMT
COPY config/pipelines.yml config/log4j2.properties config/log4j2.file.properties config/ # buildkit
# Tue, 17 Dec 2024 15:31:13 GMT
COPY pipeline/default.conf pipeline/logstash.conf # buildkit
# Tue, 17 Dec 2024 15:31:13 GMT
RUN chown --recursive logstash:root config/ pipeline/ # buildkit
# Tue, 17 Dec 2024 15:31:13 GMT
ENV LANG=en_US.UTF-8 LC_ALL=en_US.UTF-8
# Tue, 17 Dec 2024 15:31:13 GMT
COPY env2yaml/env2yaml-amd64 env2yaml/env2yaml-arm64 env2yaml/ # buildkit
# Tue, 17 Dec 2024 15:31:13 GMT
RUN env2yamlarch="$(dpkg --print-architecture)";   case "${env2yamlarch}" in     'x86_64'|'amd64')       env2yamlarch=amd64;       ;;     'aarch64'|'arm64')       env2yamlarch=arm64;       ;;     *) echo >&2 "error: unsupported architecture '$env2yamlarch'"; exit 1 ;;   esac;   mkdir -p /usr/local/bin;   cp env2yaml/env2yaml-${env2yamlarch} /usr/local/bin/env2yaml;   rm -rf env2yaml # buildkit
# Tue, 17 Dec 2024 15:31:13 GMT
COPY bin/docker-entrypoint /usr/local/bin/ # buildkit
# Tue, 17 Dec 2024 15:31:13 GMT
RUN chmod 0755 /usr/local/bin/docker-entrypoint # buildkit
# Tue, 17 Dec 2024 15:31:13 GMT
USER 1000
# Tue, 17 Dec 2024 15:31:13 GMT
EXPOSE map[5044/tcp:{} 9600/tcp:{}]
# Tue, 17 Dec 2024 15:31:13 GMT
LABEL org.label-schema.schema-version=1.0 org.label-schema.vendor=Elastic org.opencontainers.image.vendor=Elastic org.label-schema.name=logstash org.opencontainers.image.title=logstash org.label-schema.version=8.16.2 org.opencontainers.image.version=8.16.2 org.label-schema.url=https://www.elastic.co/products/logstash org.label-schema.vcs-url=https://github.com/elastic/logstash org.label-schema.license=Elastic License org.opencontainers.image.licenses=Elastic License org.opencontainers.image.description=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' org.label-schema.build-date=2024-12-11T16:38:24+00:00 org.opencontainers.image.created=2024-12-11T16:38:24+00:00
# Tue, 17 Dec 2024 15:31:13 GMT
ENTRYPOINT ["/usr/local/bin/docker-entrypoint"]
```

-	Layers:
	-	`sha256:d9802f032d6798e2086607424bfe88cb8ec1d6f116e11cd99592dcaf261e9cd2`  
		Last Modified: Fri, 13 Dec 2024 13:08:34 GMT  
		Size: 27.5 MB (27511060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3d32e2c2a56bf50cdaff07edc54d3c501be54116bb0a02559b288049c372647`  
		Last Modified: Tue, 17 Dec 2024 19:30:07 GMT  
		Size: 50.6 MB (50649025 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:829d6133eb15ae1cdbc3754dced7d69823369061a4db1c9d02be0eef5dfb88c8`  
		Last Modified: Tue, 17 Dec 2024 19:30:06 GMT  
		Size: 1.8 KB (1805 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4882e5d56e5a0ef233663cc42d2d8320a7954e77b7c440da96d427b7e1949e7b`  
		Last Modified: Tue, 17 Dec 2024 19:30:12 GMT  
		Size: 436.3 MB (436301698 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71937f1915ddbb397f2e576613db7f795810f0ed385d15c65d36c8de907b7e19`  
		Last Modified: Tue, 17 Dec 2024 19:30:06 GMT  
		Size: 278.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:def805de23b90a36f9f35725cdf8c7dc5b58e72771aec6289b725444424d82fd`  
		Last Modified: Wed, 18 Dec 2024 10:33:08 GMT  
		Size: 1.6 KB (1581 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f96cc820f953aab08efca434b32dcad8d8ea51eac563f66a50e0b7918cf3bb8`  
		Last Modified: Wed, 18 Dec 2024 08:22:51 GMT  
		Size: 278.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:163a509abab25901c90b4523288a79041800a826192f9f5934030c986bce725a`  
		Last Modified: Tue, 17 Dec 2024 19:30:08 GMT  
		Size: 1.8 KB (1766 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7b294de323226e205d10f3a5433bb6c90aa2261b7b68482cac2df09fd83ddad`  
		Last Modified: Wed, 18 Dec 2024 10:33:16 GMT  
		Size: 4.0 MB (4004301 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d36526edd89b7fe509288ca21bb6ad1d8cf5e215687572a0cb4ad311483bd80`  
		Last Modified: Wed, 18 Dec 2024 08:22:58 GMT  
		Size: 2.1 MB (2066564 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff65d649460ed48148dfcb51c0a1695e66258e679eb8962fc570c9c70923eb33`  
		Last Modified: Tue, 17 Dec 2024 19:30:08 GMT  
		Size: 712.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `logstash:8.16.2` - unknown; unknown

```console
$ docker pull logstash@sha256:d4e79a7eea867d077ec184d543f2fb658e2d731ff93c7492d253a40fa3dea0e4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3551900 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb68ba6835c369a2d6b76b0de0ff673b805226bba4ad24f1ea042a8b07240c47`

```dockerfile
```

-	Layers:
	-	`sha256:9b4acd5f49768c23ad531ed4918768b8fe3dfb18255be08fd6768912fecbb0d4`  
		Last Modified: Wed, 18 Dec 2024 21:15:05 GMT  
		Size: 3.5 MB (3517329 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:90e9009657735628c549fd6371d384b0f86dbf22719598947f5eaf41bba1d826`  
		Last Modified: Wed, 18 Dec 2024 21:15:04 GMT  
		Size: 34.6 KB (34571 bytes)  
		MIME: application/vnd.in-toto+json

### `logstash:8.16.2` - linux; arm64 variant v8

```console
$ docker pull logstash@sha256:9a714bff25297a756fc86c4969ff7931232a277dba44b57bc731076a5a97f300
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **505.0 MB (505025586 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eee71ed4be2272e1a2e13f956380a23aa2f46ce79d3a211e627f2c810af928f2`
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
# Tue, 17 Dec 2024 15:31:13 GMT
RUN for iter in {1..10}; do       export DEBIAN_FRONTEND=noninteractive &&     apt-get update -y &&   apt-get upgrade -y &&   apt-get install -y procps findutils tar gzip &&         apt-get install -y locales &&         apt-get install -y curl &&     apt-get clean all &&       locale-gen 'en_US.UTF-8' &&     apt-get clean metadata &&   exit_code=0 && break || exit_code=$? && echo "packaging error: retry $iter in 10s" && apt-get clean all &&   apt-get clean metadata && sleep 10; done; (exit $exit_code) # buildkit
# Tue, 17 Dec 2024 15:31:13 GMT
RUN groupadd --gid 1000 logstash &&   adduser --uid 1000 --gid 1000 --home /usr/share/logstash --no-create-home logstash # buildkit
# Tue, 17 Dec 2024 15:31:13 GMT
RUN curl -Lo - https://artifacts.elastic.co/downloads/logstash/logstash-8.16.2-linux-$(arch).tar.gz |   tar zxf - -C /usr/share &&   mv /usr/share/logstash-8.16.2 /usr/share/logstash &&   chown --recursive logstash:logstash /usr/share/logstash/ &&   chown -R logstash:root /usr/share/logstash &&   chmod -R g=u /usr/share/logstash &&   mkdir /licenses/ &&   mv /usr/share/logstash/NOTICE.TXT /licenses/NOTICE.TXT &&   mv /usr/share/logstash/LICENSE.txt /licenses/LICENSE.txt &&   find /usr/share/logstash -type d -exec chmod g+s {} \; &&   ln -s /usr/share/logstash /opt/logstash # buildkit
# Tue, 17 Dec 2024 15:31:13 GMT
WORKDIR /usr/share/logstash
# Tue, 17 Dec 2024 15:31:13 GMT
ENV ELASTIC_CONTAINER=true
# Tue, 17 Dec 2024 15:31:13 GMT
ENV PATH=/usr/share/logstash/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Dec 2024 15:31:13 GMT
COPY config/logstash-full.yml config/logstash.yml # buildkit
# Tue, 17 Dec 2024 15:31:13 GMT
COPY config/pipelines.yml config/log4j2.properties config/log4j2.file.properties config/ # buildkit
# Tue, 17 Dec 2024 15:31:13 GMT
COPY pipeline/default.conf pipeline/logstash.conf # buildkit
# Tue, 17 Dec 2024 15:31:13 GMT
RUN chown --recursive logstash:root config/ pipeline/ # buildkit
# Tue, 17 Dec 2024 15:31:13 GMT
ENV LANG=en_US.UTF-8 LC_ALL=en_US.UTF-8
# Tue, 17 Dec 2024 15:31:13 GMT
COPY env2yaml/env2yaml-amd64 env2yaml/env2yaml-arm64 env2yaml/ # buildkit
# Tue, 17 Dec 2024 15:31:13 GMT
RUN env2yamlarch="$(dpkg --print-architecture)";   case "${env2yamlarch}" in     'x86_64'|'amd64')       env2yamlarch=amd64;       ;;     'aarch64'|'arm64')       env2yamlarch=arm64;       ;;     *) echo >&2 "error: unsupported architecture '$env2yamlarch'"; exit 1 ;;   esac;   mkdir -p /usr/local/bin;   cp env2yaml/env2yaml-${env2yamlarch} /usr/local/bin/env2yaml;   rm -rf env2yaml # buildkit
# Tue, 17 Dec 2024 15:31:13 GMT
COPY bin/docker-entrypoint /usr/local/bin/ # buildkit
# Tue, 17 Dec 2024 15:31:13 GMT
RUN chmod 0755 /usr/local/bin/docker-entrypoint # buildkit
# Tue, 17 Dec 2024 15:31:13 GMT
USER 1000
# Tue, 17 Dec 2024 15:31:13 GMT
EXPOSE map[5044/tcp:{} 9600/tcp:{}]
# Tue, 17 Dec 2024 15:31:13 GMT
LABEL org.label-schema.schema-version=1.0 org.label-schema.vendor=Elastic org.opencontainers.image.vendor=Elastic org.label-schema.name=logstash org.opencontainers.image.title=logstash org.label-schema.version=8.16.2 org.opencontainers.image.version=8.16.2 org.label-schema.url=https://www.elastic.co/products/logstash org.label-schema.vcs-url=https://github.com/elastic/logstash org.label-schema.license=Elastic License org.opencontainers.image.licenses=Elastic License org.opencontainers.image.description=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' org.label-schema.build-date=2024-12-11T16:38:24+00:00 org.opencontainers.image.created=2024-12-11T16:38:24+00:00
# Tue, 17 Dec 2024 15:31:13 GMT
ENTRYPOINT ["/usr/local/bin/docker-entrypoint"]
```

-	Layers:
	-	`sha256:1b9f3c55f9d4aa5c52eb67a4cb7d0f4726ab85a413b50e3e3fe788befce3d297`  
		Last Modified: Fri, 13 Dec 2024 13:25:16 GMT  
		Size: 26.0 MB (25973828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7607b73ed44e6a98b7e6a19eea72f5e863956fea3129734cb9581e4701b38e5e`  
		Last Modified: Tue, 17 Dec 2024 19:49:01 GMT  
		Size: 38.6 MB (38580216 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5dfe66d81f9cc1524352bdab74f4ad34bbcc7751bc9b4596d331b2925b46ca4b`  
		Last Modified: Wed, 18 Dec 2024 19:01:19 GMT  
		Size: 1.8 KB (1806 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b30503e174ba5af59259f81da68b531cc4a4486a22be7ff1e881664bc56907e`  
		Last Modified: Wed, 18 Dec 2024 19:05:35 GMT  
		Size: 434.5 MB (434523092 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6896d9800d92641a5a4518275db6ff9c42b35704da2400ab36835525d1c6faa3`  
		Last Modified: Wed, 18 Dec 2024 10:07:43 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24b5fd36626bb491d50ee42ebac60cc159df99a47e200dd6c656867c384e44ad`  
		Last Modified: Wed, 18 Dec 2024 21:15:05 GMT  
		Size: 1.6 KB (1578 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69e0c13015002ed05256671eb55f55b395634f0e3f81b345a12b0b03cbda2581`  
		Last Modified: Tue, 17 Dec 2024 19:49:01 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cac03859b47c17312342d0575807f2a0356d6be3ca76d536b46d5f60d049043`  
		Last Modified: Tue, 17 Dec 2024 19:49:02 GMT  
		Size: 1.8 KB (1761 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37b6c386c58272d6d005013bfffbf718dc34696eca5cf55e01b4541934a6924a`  
		Last Modified: Tue, 17 Dec 2024 19:49:03 GMT  
		Size: 4.0 MB (4004303 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c667b273290f083dcc2914ae32f1057c40d1cc55dc25b0f3efde52e2c80ed050`  
		Last Modified: Tue, 17 Dec 2024 19:49:03 GMT  
		Size: 1.9 MB (1937677 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75dce67f936e244437a7be5c8d817507e9fbc2c0087866acba7883e8ec3cd122`  
		Last Modified: Tue, 17 Dec 2024 19:49:03 GMT  
		Size: 708.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `logstash:8.16.2` - unknown; unknown

```console
$ docker pull logstash@sha256:b379e6ae8eb286b9d92ec02bf9bb384f5444c133eea05b0236d77f3923ab9e1e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3551654 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9bb15eead49bd36080944d6d7beb2126e580e6914f5bd5e2f8cefc060e98d625`

```dockerfile
```

-	Layers:
	-	`sha256:6bfeb0b9bd5d281aee84dafe762d2299dcb9856d42cc3fe6bcf8bbc0686c0b47`  
		Last Modified: Tue, 17 Dec 2024 19:49:00 GMT  
		Size: 3.5 MB (3516941 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7cd999f8855181f3e300382c685df74fe9962b83486a5a74d1c76567ee8864da`  
		Last Modified: Wed, 18 Dec 2024 21:15:04 GMT  
		Size: 34.7 KB (34713 bytes)  
		MIME: application/vnd.in-toto+json

## `logstash:8.17.0`

```console
$ docker pull logstash@sha256:8793dd50c1aee8fbbc6993c06c6c0e1a9fc492b30c6a98fe3ed77d166f234ec2
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `logstash:8.17.0` - linux; amd64

```console
$ docker pull logstash@sha256:2d3a442937eee96f5d70dcd28d2415bbced98f2d02916eb5fc71244e0ccdc458
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **515.8 MB (515798491 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e0d59a47a5fcba2e39c33e01a78de498299f7e09a3815c8ccecba27d5cd1b16`
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
# Mon, 16 Dec 2024 18:48:50 GMT
RUN for iter in {1..10}; do       export DEBIAN_FRONTEND=noninteractive &&     apt-get update -y &&   apt-get upgrade -y &&   apt-get install -y procps findutils tar gzip &&         apt-get install -y locales &&         apt-get install -y curl &&     apt-get clean all &&       locale-gen 'en_US.UTF-8' &&     apt-get clean metadata &&   exit_code=0 && break || exit_code=$? && echo "packaging error: retry $iter in 10s" && apt-get clean all &&   apt-get clean metadata && sleep 10; done; (exit $exit_code) # buildkit
# Mon, 16 Dec 2024 18:48:50 GMT
RUN groupadd --gid 1000 logstash &&   adduser --uid 1000 --gid 1000 --home /usr/share/logstash --no-create-home logstash # buildkit
# Mon, 16 Dec 2024 18:48:50 GMT
RUN curl -Lo - https://artifacts.elastic.co/downloads/logstash/logstash-8.17.0-linux-$(arch).tar.gz |   tar zxf - -C /usr/share &&   mv /usr/share/logstash-8.17.0 /usr/share/logstash &&   chown --recursive logstash:logstash /usr/share/logstash/ &&   chown -R logstash:root /usr/share/logstash &&   chmod -R g=u /usr/share/logstash &&   mkdir /licenses/ &&   mv /usr/share/logstash/NOTICE.TXT /licenses/NOTICE.TXT &&   mv /usr/share/logstash/LICENSE.txt /licenses/LICENSE.txt &&   find /usr/share/logstash -type d -exec chmod g+s {} \; &&   ln -s /usr/share/logstash /opt/logstash # buildkit
# Mon, 16 Dec 2024 18:48:50 GMT
WORKDIR /usr/share/logstash
# Mon, 16 Dec 2024 18:48:50 GMT
ENV ELASTIC_CONTAINER=true
# Mon, 16 Dec 2024 18:48:50 GMT
ENV PATH=/usr/share/logstash/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 16 Dec 2024 18:48:50 GMT
COPY config/logstash-full.yml config/logstash.yml # buildkit
# Mon, 16 Dec 2024 18:48:50 GMT
COPY config/pipelines.yml config/log4j2.properties config/log4j2.file.properties config/ # buildkit
# Mon, 16 Dec 2024 18:48:50 GMT
COPY pipeline/default.conf pipeline/logstash.conf # buildkit
# Mon, 16 Dec 2024 18:48:50 GMT
RUN chown --recursive logstash:root config/ pipeline/ # buildkit
# Mon, 16 Dec 2024 18:48:50 GMT
ENV LANG=en_US.UTF-8 LC_ALL=en_US.UTF-8
# Mon, 16 Dec 2024 18:48:50 GMT
COPY env2yaml/env2yaml-amd64 env2yaml/env2yaml-arm64 env2yaml/ # buildkit
# Mon, 16 Dec 2024 18:48:50 GMT
RUN env2yamlarch="$(dpkg --print-architecture)";   case "${env2yamlarch}" in     'x86_64'|'amd64')       env2yamlarch=amd64;       ;;     'aarch64'|'arm64')       env2yamlarch=arm64;       ;;     *) echo >&2 "error: unsupported architecture '$env2yamlarch'"; exit 1 ;;   esac;   mkdir -p /usr/local/bin;   cp env2yaml/env2yaml-${env2yamlarch} /usr/local/bin/env2yaml;   rm -rf env2yaml # buildkit
# Mon, 16 Dec 2024 18:48:50 GMT
COPY bin/docker-entrypoint /usr/local/bin/ # buildkit
# Mon, 16 Dec 2024 18:48:50 GMT
RUN chmod 0755 /usr/local/bin/docker-entrypoint # buildkit
# Mon, 16 Dec 2024 18:48:50 GMT
USER 1000
# Mon, 16 Dec 2024 18:48:50 GMT
EXPOSE map[5044/tcp:{} 9600/tcp:{}]
# Mon, 16 Dec 2024 18:48:50 GMT
LABEL org.label-schema.schema-version=1.0 org.label-schema.vendor=Elastic org.opencontainers.image.vendor=Elastic org.label-schema.name=logstash org.opencontainers.image.title=logstash org.label-schema.version=8.17.0 org.opencontainers.image.version=8.17.0 org.label-schema.url=https://www.elastic.co/products/logstash org.label-schema.vcs-url=https://github.com/elastic/logstash org.label-schema.license=Elastic License org.opencontainers.image.licenses=Elastic License org.opencontainers.image.description=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' org.label-schema.build-date=2024-12-05T00:55:38+00:00 org.opencontainers.image.created=2024-12-05T00:55:38+00:00
# Mon, 16 Dec 2024 18:48:50 GMT
ENTRYPOINT ["/usr/local/bin/docker-entrypoint"]
```

-	Layers:
	-	`sha256:d9802f032d6798e2086607424bfe88cb8ec1d6f116e11cd99592dcaf261e9cd2`  
		Last Modified: Fri, 13 Dec 2024 13:08:34 GMT  
		Size: 27.5 MB (27511060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:731445757cc46ed4479fdc9a155b6abd88df2233d8eeda2a0e88de7b93f00908`  
		Last Modified: Tue, 17 Dec 2024 19:30:15 GMT  
		Size: 50.6 MB (50648959 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1d39d2f293de555c17ea30894e0126bccce999bbca2904a8bd77632053bde29`  
		Last Modified: Tue, 17 Dec 2024 19:30:14 GMT  
		Size: 1.8 KB (1806 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f5bae56b53db347df28b8b28b69fc783a569c5bd4eb221f8fb7f7f971d1b7a0`  
		Last Modified: Tue, 17 Dec 2024 19:30:21 GMT  
		Size: 431.6 MB (431564973 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a02e8aa84a22a4a9fd5427dfa5f0aebdd5d4ac3df4e59ecf1aa8b409a58fd607`  
		Last Modified: Tue, 17 Dec 2024 19:30:14 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aebe8849b94681f884770a3e9ed2c0b27ec9aa9902cef9c3a263d0d3c761b8fa`  
		Last Modified: Tue, 17 Dec 2024 19:30:15 GMT  
		Size: 1.6 KB (1577 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8677af43e2eab39e072c65133e43af79b51271d869f448924b244a4f14d055eb`  
		Last Modified: Tue, 17 Dec 2024 19:30:15 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5dfb3faf58e05e640842b17adcd769f1eb96619ac34d8dd0548cbbe9db64d4bf`  
		Last Modified: Tue, 17 Dec 2024 19:30:16 GMT  
		Size: 1.8 KB (1769 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e7a58462dc16f9dc9ecc19b9cec7c1a6d3a350b849d8f6a55e3158ab5d2eefd`  
		Last Modified: Tue, 17 Dec 2024 19:30:16 GMT  
		Size: 4.0 MB (4001893 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e11e09148a2908975d3d19544e42822b29a64686ae231972d27914313f71b80`  
		Last Modified: Wed, 18 Dec 2024 00:19:17 GMT  
		Size: 2.1 MB (2065126 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd863fd6f1555ca10d2d1fdd20dbb8af8456ef7c3a56c98d8afad246de879673`  
		Last Modified: Tue, 17 Dec 2024 19:30:17 GMT  
		Size: 712.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `logstash:8.17.0` - unknown; unknown

```console
$ docker pull logstash@sha256:74b6a1ff20a02f9094dda9e5867607639f44c5e0e0d40d5a270eb7da06cf7ea6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3553459 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:efb2346d12d0badd16c40318c1b5fc3c7c0601c038add4d96b4647f47551e422`

```dockerfile
```

-	Layers:
	-	`sha256:d468e3f6c99052ac310b04125b81f80cebd2dfaacd9d92c34bdb711144267ef5`  
		Last Modified: Mon, 06 Jan 2025 17:49:44 GMT  
		Size: 3.5 MB (3518888 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:47b8253992ed9d1f4be92e39f3636f842a16ab994e754f10c600694be5145581`  
		Last Modified: Wed, 18 Dec 2024 10:06:46 GMT  
		Size: 34.6 KB (34571 bytes)  
		MIME: application/vnd.in-toto+json

### `logstash:8.17.0` - linux; arm64 variant v8

```console
$ docker pull logstash@sha256:52fba1e3d3699f69ce13557da0a5a55e69d723c99c72f5c69c8099a4d400f63e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **500.3 MB (500297101 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c71b27429e0e49b67e4798ca5e69778676fc707aad027240d96d28a30f06257`
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
# Mon, 16 Dec 2024 18:48:50 GMT
RUN for iter in {1..10}; do       export DEBIAN_FRONTEND=noninteractive &&     apt-get update -y &&   apt-get upgrade -y &&   apt-get install -y procps findutils tar gzip &&         apt-get install -y locales &&         apt-get install -y curl &&     apt-get clean all &&       locale-gen 'en_US.UTF-8' &&     apt-get clean metadata &&   exit_code=0 && break || exit_code=$? && echo "packaging error: retry $iter in 10s" && apt-get clean all &&   apt-get clean metadata && sleep 10; done; (exit $exit_code) # buildkit
# Mon, 16 Dec 2024 18:48:50 GMT
RUN groupadd --gid 1000 logstash &&   adduser --uid 1000 --gid 1000 --home /usr/share/logstash --no-create-home logstash # buildkit
# Mon, 16 Dec 2024 18:48:50 GMT
RUN curl -Lo - https://artifacts.elastic.co/downloads/logstash/logstash-8.17.0-linux-$(arch).tar.gz |   tar zxf - -C /usr/share &&   mv /usr/share/logstash-8.17.0 /usr/share/logstash &&   chown --recursive logstash:logstash /usr/share/logstash/ &&   chown -R logstash:root /usr/share/logstash &&   chmod -R g=u /usr/share/logstash &&   mkdir /licenses/ &&   mv /usr/share/logstash/NOTICE.TXT /licenses/NOTICE.TXT &&   mv /usr/share/logstash/LICENSE.txt /licenses/LICENSE.txt &&   find /usr/share/logstash -type d -exec chmod g+s {} \; &&   ln -s /usr/share/logstash /opt/logstash # buildkit
# Mon, 16 Dec 2024 18:48:50 GMT
WORKDIR /usr/share/logstash
# Mon, 16 Dec 2024 18:48:50 GMT
ENV ELASTIC_CONTAINER=true
# Mon, 16 Dec 2024 18:48:50 GMT
ENV PATH=/usr/share/logstash/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 16 Dec 2024 18:48:50 GMT
COPY config/logstash-full.yml config/logstash.yml # buildkit
# Mon, 16 Dec 2024 18:48:50 GMT
COPY config/pipelines.yml config/log4j2.properties config/log4j2.file.properties config/ # buildkit
# Mon, 16 Dec 2024 18:48:50 GMT
COPY pipeline/default.conf pipeline/logstash.conf # buildkit
# Mon, 16 Dec 2024 18:48:50 GMT
RUN chown --recursive logstash:root config/ pipeline/ # buildkit
# Mon, 16 Dec 2024 18:48:50 GMT
ENV LANG=en_US.UTF-8 LC_ALL=en_US.UTF-8
# Mon, 16 Dec 2024 18:48:50 GMT
COPY env2yaml/env2yaml-amd64 env2yaml/env2yaml-arm64 env2yaml/ # buildkit
# Mon, 16 Dec 2024 18:48:50 GMT
RUN env2yamlarch="$(dpkg --print-architecture)";   case "${env2yamlarch}" in     'x86_64'|'amd64')       env2yamlarch=amd64;       ;;     'aarch64'|'arm64')       env2yamlarch=arm64;       ;;     *) echo >&2 "error: unsupported architecture '$env2yamlarch'"; exit 1 ;;   esac;   mkdir -p /usr/local/bin;   cp env2yaml/env2yaml-${env2yamlarch} /usr/local/bin/env2yaml;   rm -rf env2yaml # buildkit
# Mon, 16 Dec 2024 18:48:50 GMT
COPY bin/docker-entrypoint /usr/local/bin/ # buildkit
# Mon, 16 Dec 2024 18:48:50 GMT
RUN chmod 0755 /usr/local/bin/docker-entrypoint # buildkit
# Mon, 16 Dec 2024 18:48:50 GMT
USER 1000
# Mon, 16 Dec 2024 18:48:50 GMT
EXPOSE map[5044/tcp:{} 9600/tcp:{}]
# Mon, 16 Dec 2024 18:48:50 GMT
LABEL org.label-schema.schema-version=1.0 org.label-schema.vendor=Elastic org.opencontainers.image.vendor=Elastic org.label-schema.name=logstash org.opencontainers.image.title=logstash org.label-schema.version=8.17.0 org.opencontainers.image.version=8.17.0 org.label-schema.url=https://www.elastic.co/products/logstash org.label-schema.vcs-url=https://github.com/elastic/logstash org.label-schema.license=Elastic License org.opencontainers.image.licenses=Elastic License org.opencontainers.image.description=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' org.label-schema.build-date=2024-12-05T00:55:38+00:00 org.opencontainers.image.created=2024-12-05T00:55:38+00:00
# Mon, 16 Dec 2024 18:48:50 GMT
ENTRYPOINT ["/usr/local/bin/docker-entrypoint"]
```

-	Layers:
	-	`sha256:1b9f3c55f9d4aa5c52eb67a4cb7d0f4726ab85a413b50e3e3fe788befce3d297`  
		Last Modified: Fri, 13 Dec 2024 13:25:16 GMT  
		Size: 26.0 MB (25973828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7607b73ed44e6a98b7e6a19eea72f5e863956fea3129734cb9581e4701b38e5e`  
		Last Modified: Tue, 17 Dec 2024 19:49:01 GMT  
		Size: 38.6 MB (38580216 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5dfe66d81f9cc1524352bdab74f4ad34bbcc7751bc9b4596d331b2925b46ca4b`  
		Last Modified: Wed, 18 Dec 2024 19:01:19 GMT  
		Size: 1.8 KB (1806 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b60b5dcf2d91b3b266659d90fa8b487259bdb6a3e646aa1e4102063288dcbc1`  
		Last Modified: Wed, 18 Dec 2024 15:02:56 GMT  
		Size: 429.8 MB (429797716 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:691b00add91e3ca96ef1ec8c49634f5e40d70304e08a1088fafc15972d5d95a3`  
		Last Modified: Tue, 17 Dec 2024 19:50:32 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07e0ca7c06007a84570ec06b98a41ba0d081b99e2e44f2abef64131f31c4f829`  
		Last Modified: Tue, 17 Dec 2024 19:50:32 GMT  
		Size: 1.6 KB (1578 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3476b68f1c78458dad18bbc5ed6c84e7287a2a398b44bd3507d13d06934d5905`  
		Last Modified: Tue, 17 Dec 2024 19:50:32 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebdee453918b2b06d5ed6bc2e6927f1f5d30c25eff746354b045eec4e3894e3f`  
		Last Modified: Tue, 17 Dec 2024 19:50:33 GMT  
		Size: 1.8 KB (1762 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1215e6c8ba3f791aa41ef4232e8dacacb58878d388de800f41163478cba20161`  
		Last Modified: Tue, 17 Dec 2024 19:50:34 GMT  
		Size: 4.0 MB (4001889 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d38f281c263c2f0980fc7f0c815eaa4f390748af2bbf449911dce6b38a015502`  
		Last Modified: Wed, 18 Dec 2024 12:02:31 GMT  
		Size: 1.9 MB (1936983 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01ea7020abbae0d771e26a86dbea74e20c5dd9856d4544e05bfe4ce1f627ff97`  
		Last Modified: Tue, 17 Dec 2024 19:50:34 GMT  
		Size: 709.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `logstash:8.17.0` - unknown; unknown

```console
$ docker pull logstash@sha256:f91d60df43eaba7594648e82c11e8ffd64b32b7101bc2782b3446708a9bbddf5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3553214 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5112060bedfda376df04cb81a079a9cd3a5c50049ed19ac1814f85cedd9f9248`

```dockerfile
```

-	Layers:
	-	`sha256:7baa7cc11a555caed4d9f854472818000b6ce12c0b3ca64daf26a0074ed7de5d`  
		Last Modified: Mon, 30 Dec 2024 07:57:47 GMT  
		Size: 3.5 MB (3518500 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:24c3f926e116d09208269d6b708c19a143192e1fb480161b5e501edcf70c1b2f`  
		Last Modified: Mon, 30 Dec 2024 07:57:45 GMT  
		Size: 34.7 KB (34714 bytes)  
		MIME: application/vnd.in-toto+json
