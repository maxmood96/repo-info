<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `logstash`

-	[`logstash:8.19.13`](#logstash81913)
-	[`logstash:9.2.7`](#logstash927)
-	[`logstash:9.3.2`](#logstash932)

## `logstash:8.19.13`

```console
$ docker pull logstash@sha256:59ddbb68b1c65be41ac4c098e7b4435333d5acedca090027a8e66efcc5035d22
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `logstash:8.19.13` - linux; amd64

```console
$ docker pull logstash@sha256:9946aca2404e04c1a2dbc243926a0b188f3d7df978ce112d875264ea4be38248
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **538.8 MB (538796972 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f336664bdd068d56fad870bbe3f649a9d8fb6b19768dc0e2773cf85294cc245f`
-	Entrypoint: `["\/usr\/local\/bin\/docker-entrypoint"]`

```dockerfile
# Fri, 03 Apr 2026 15:16:40 GMT
ARG RELEASE
# Fri, 03 Apr 2026 15:16:40 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 03 Apr 2026 15:16:40 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 03 Apr 2026 15:16:42 GMT
ADD file:0f6466425c4f1800aae9224ddc3437b90c829cea58fb8edd5dde2f1eb0ee28da in / 
# Fri, 03 Apr 2026 15:16:43 GMT
CMD ["/bin/bash"]
# Tue, 07 Apr 2026 01:59:05 GMT
RUN for iter in {1..10}; do       export DEBIAN_FRONTEND=noninteractive &&     apt-get update -y &&   apt-get upgrade -y &&   apt-get install -y procps findutils tar gzip &&         apt-get install -y locales &&         apt-get install -y curl &&     apt-get clean all &&       locale-gen 'en_US.UTF-8' &&     apt-get clean metadata &&   exit_code=0 && break || exit_code=$? && echo "packaging error: retry $iter in 10s" && apt-get clean all &&   apt-get clean metadata && sleep 10; done; (exit $exit_code) # buildkit
# Tue, 07 Apr 2026 01:59:05 GMT
RUN userdel -r ubuntu && groupadd --gid 1000 logstash &&   useradd --uid 1000 --gid 1000 --home /usr/share/logstash --no-create-home logstash # buildkit
# Tue, 07 Apr 2026 01:59:45 GMT
RUN curl -Lo - https://artifacts.elastic.co/downloads/logstash/logstash-8.19.13-linux-$(arch).tar.gz |   tar zxf - -C /usr/share &&   mv /usr/share/logstash-8.19.13 /usr/share/logstash &&   chown --recursive logstash:logstash /usr/share/logstash/ &&   chown -R logstash:root /usr/share/logstash &&   chmod -R g=u /usr/share/logstash &&   mkdir /licenses/ &&   mv /usr/share/logstash/NOTICE.TXT /licenses/NOTICE.TXT &&   mv /usr/share/logstash/LICENSE.txt /licenses/LICENSE.txt &&   find /usr/share/logstash -type d -exec chmod g+s {} \; &&   ln -s /usr/share/logstash /opt/logstash # buildkit
# Tue, 07 Apr 2026 01:59:45 GMT
WORKDIR /usr/share/logstash
# Tue, 07 Apr 2026 01:59:45 GMT
ENV ELASTIC_CONTAINER=true
# Tue, 07 Apr 2026 01:59:45 GMT
ENV PATH=/usr/share/logstash/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Apr 2026 01:59:45 GMT
COPY config/logstash-full.yml config/logstash.yml # buildkit
# Tue, 07 Apr 2026 01:59:46 GMT
COPY config/pipelines.yml config/log4j2.properties config/log4j2.file.properties config/ # buildkit
# Tue, 07 Apr 2026 01:59:46 GMT
COPY pipeline/default.conf pipeline/logstash.conf # buildkit
# Tue, 07 Apr 2026 01:59:46 GMT
RUN chown --recursive logstash:root config/ pipeline/ # buildkit
# Tue, 07 Apr 2026 01:59:46 GMT
ENV LANG=en_US.UTF-8 LC_ALL=en_US.UTF-8
# Tue, 07 Apr 2026 01:59:46 GMT
COPY --chown=logstash:root env2yaml/classes /usr/share/logstash/env2yaml/classes/ # buildkit
# Tue, 07 Apr 2026 01:59:46 GMT
COPY --chown=logstash:root env2yaml/lib /usr/share/logstash/env2yaml/lib/ # buildkit
# Tue, 07 Apr 2026 01:59:46 GMT
COPY --chmod=0755 env2yaml/env2yaml /usr/local/bin/env2yaml # buildkit
# Tue, 07 Apr 2026 01:59:46 GMT
COPY bin/docker-entrypoint /usr/local/bin/ # buildkit
# Tue, 07 Apr 2026 01:59:46 GMT
RUN chmod 0755 /usr/local/bin/docker-entrypoint # buildkit
# Tue, 07 Apr 2026 01:59:46 GMT
USER 1000
# Tue, 07 Apr 2026 01:59:46 GMT
EXPOSE map[5044/tcp:{} 9600/tcp:{}]
# Tue, 07 Apr 2026 01:59:46 GMT
LABEL org.label-schema.schema-version=1.0 org.label-schema.vendor=Elastic org.opencontainers.image.vendor=Elastic org.label-schema.name=logstash org.opencontainers.image.title=logstash org.label-schema.version=8.19.13 org.opencontainers.image.version=8.19.13 org.label-schema.url=https://www.elastic.co/products/logstash org.label-schema.vcs-url=https://github.com/elastic/logstash org.label-schema.license=Elastic License org.opencontainers.image.licenses=Elastic License org.opencontainers.image.description=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' org.label-schema.build-date=2026-03-10T13:51:26+00:00 org.opencontainers.image.created=2026-03-10T13:51:26+00:00
# Tue, 07 Apr 2026 01:59:46 GMT
ENTRYPOINT ["/usr/local/bin/docker-entrypoint"]
```

-	Layers:
	-	`sha256:689b91d88a0f4086057ec826027b128902ecf2b516be510371c115bc55da19a6`  
		Last Modified: Fri, 03 Apr 2026 15:56:29 GMT  
		Size: 29.7 MB (29733459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f495e58103bca660f57d43476aa4cdcbc7e2a49d0385b9e0983e1bc9b2c232d`  
		Last Modified: Tue, 07 Apr 2026 02:00:28 GMT  
		Size: 52.2 MB (52205457 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1b36660e851a7b7d8f24d1e985469ff10116fc71e735d81b5a7a830c388172d`  
		Last Modified: Tue, 07 Apr 2026 02:00:24 GMT  
		Size: 1.2 KB (1224 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7c0d6a057f57c324a388db6f6c03070b9592e211d5d1d85e2b9ed9777f8f10f`  
		Last Modified: Tue, 07 Apr 2026 02:00:34 GMT  
		Size: 456.6 MB (456590339 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b06b0ce7b94d40c96732fafc57a088bb08083eb576d5be297bc403362e7add3`  
		Last Modified: Tue, 07 Apr 2026 02:00:25 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cdc2a99867dfb3f9438f76438e7452ad817b076b8a036f1766a73a7f58199c86`  
		Last Modified: Tue, 07 Apr 2026 02:00:26 GMT  
		Size: 1.6 KB (1577 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ceee9e3343fa606cc8d2f2d32238d182a0efbc1dfbfa29b7efbc457355587ddf`  
		Last Modified: Tue, 07 Apr 2026 02:00:27 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1519c957086b9c4f94ad42d0fc2b6cdb5f600d6eac932c1b1f4c10d5203b674f`  
		Last Modified: Tue, 07 Apr 2026 02:00:28 GMT  
		Size: 1.8 KB (1762 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4bed35b76cc4ef1f7b2d3a324911c61b0519b705f1f174a3db10d58d5b1de8e9`  
		Last Modified: Tue, 07 Apr 2026 02:00:29 GMT  
		Size: 6.3 KB (6292 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:239238f13441e45177b369f76e43b2057464df5a67fd366ac3ca93a1e5a90a5c`  
		Last Modified: Tue, 07 Apr 2026 02:00:30 GMT  
		Size: 255.2 KB (255181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2cd63a5930cbcfa3830f4c3587cc37e62b824559103a2f7169407d375cf4d46b`  
		Last Modified: Tue, 07 Apr 2026 02:00:30 GMT  
		Size: 352.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a52900025efd98716b452b30ca548feeec1b1397c04697c4e51cb36c78d80256`  
		Last Modified: Tue, 07 Apr 2026 02:00:32 GMT  
		Size: 711.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `logstash:8.19.13` - unknown; unknown

```console
$ docker pull logstash@sha256:6c4d1473514794ce2d256fcad0157922e600e789fd8e2914afbee7a3873dd903
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3731485 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e453684ac95ae2eb9c8588cc555e69250f1e1fee32d5bafd8212508b65c72fce`

```dockerfile
```

-	Layers:
	-	`sha256:fd15db4536613e9c40286537f814899234d850af0bc525587414a27f860f9e25`  
		Last Modified: Tue, 07 Apr 2026 02:00:26 GMT  
		Size: 3.7 MB (3695640 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fbbbb8f6f84772d73ae6b905f0f0a6e0627b633204903741d0ae13a92b27f63d`  
		Last Modified: Tue, 07 Apr 2026 02:00:24 GMT  
		Size: 35.8 KB (35845 bytes)  
		MIME: application/vnd.in-toto+json

### `logstash:8.19.13` - linux; arm64 variant v8

```console
$ docker pull logstash@sha256:56913368959b915f080feb070d67f6f5f71c47e0000f7d9863c4832efdf2fdae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **539.2 MB (539232778 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d1a54ab85ca450111864016e57e464f6218f0e652d9f7b9e15c651acfa26ad6`
-	Entrypoint: `["\/usr\/local\/bin\/docker-entrypoint"]`

```dockerfile
# Fri, 03 Apr 2026 15:15:14 GMT
ARG RELEASE
# Fri, 03 Apr 2026 15:15:14 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 03 Apr 2026 15:15:14 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 03 Apr 2026 15:15:17 GMT
ADD file:9bab986009eae65b5534b3547eb3a7d0a1564404426de350dfd183cf3a4ffa9f in / 
# Fri, 03 Apr 2026 15:15:17 GMT
CMD ["/bin/bash"]
# Tue, 07 Apr 2026 02:02:27 GMT
RUN for iter in {1..10}; do       export DEBIAN_FRONTEND=noninteractive &&     apt-get update -y &&   apt-get upgrade -y &&   apt-get install -y procps findutils tar gzip &&         apt-get install -y locales &&         apt-get install -y curl &&     apt-get clean all &&       locale-gen 'en_US.UTF-8' &&     apt-get clean metadata &&   exit_code=0 && break || exit_code=$? && echo "packaging error: retry $iter in 10s" && apt-get clean all &&   apt-get clean metadata && sleep 10; done; (exit $exit_code) # buildkit
# Tue, 07 Apr 2026 02:02:27 GMT
RUN userdel -r ubuntu && groupadd --gid 1000 logstash &&   useradd --uid 1000 --gid 1000 --home /usr/share/logstash --no-create-home logstash # buildkit
# Tue, 07 Apr 2026 02:03:08 GMT
RUN curl -Lo - https://artifacts.elastic.co/downloads/logstash/logstash-8.19.13-linux-$(arch).tar.gz |   tar zxf - -C /usr/share &&   mv /usr/share/logstash-8.19.13 /usr/share/logstash &&   chown --recursive logstash:logstash /usr/share/logstash/ &&   chown -R logstash:root /usr/share/logstash &&   chmod -R g=u /usr/share/logstash &&   mkdir /licenses/ &&   mv /usr/share/logstash/NOTICE.TXT /licenses/NOTICE.TXT &&   mv /usr/share/logstash/LICENSE.txt /licenses/LICENSE.txt &&   find /usr/share/logstash -type d -exec chmod g+s {} \; &&   ln -s /usr/share/logstash /opt/logstash # buildkit
# Tue, 07 Apr 2026 02:03:09 GMT
WORKDIR /usr/share/logstash
# Tue, 07 Apr 2026 02:03:09 GMT
ENV ELASTIC_CONTAINER=true
# Tue, 07 Apr 2026 02:03:09 GMT
ENV PATH=/usr/share/logstash/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Apr 2026 02:03:09 GMT
COPY config/logstash-full.yml config/logstash.yml # buildkit
# Tue, 07 Apr 2026 02:03:09 GMT
COPY config/pipelines.yml config/log4j2.properties config/log4j2.file.properties config/ # buildkit
# Tue, 07 Apr 2026 02:03:09 GMT
COPY pipeline/default.conf pipeline/logstash.conf # buildkit
# Tue, 07 Apr 2026 02:03:09 GMT
RUN chown --recursive logstash:root config/ pipeline/ # buildkit
# Tue, 07 Apr 2026 02:03:09 GMT
ENV LANG=en_US.UTF-8 LC_ALL=en_US.UTF-8
# Tue, 07 Apr 2026 02:03:09 GMT
COPY --chown=logstash:root env2yaml/classes /usr/share/logstash/env2yaml/classes/ # buildkit
# Tue, 07 Apr 2026 02:03:09 GMT
COPY --chown=logstash:root env2yaml/lib /usr/share/logstash/env2yaml/lib/ # buildkit
# Tue, 07 Apr 2026 02:03:09 GMT
COPY --chmod=0755 env2yaml/env2yaml /usr/local/bin/env2yaml # buildkit
# Tue, 07 Apr 2026 02:03:09 GMT
COPY bin/docker-entrypoint /usr/local/bin/ # buildkit
# Tue, 07 Apr 2026 02:03:09 GMT
RUN chmod 0755 /usr/local/bin/docker-entrypoint # buildkit
# Tue, 07 Apr 2026 02:03:09 GMT
USER 1000
# Tue, 07 Apr 2026 02:03:09 GMT
EXPOSE map[5044/tcp:{} 9600/tcp:{}]
# Tue, 07 Apr 2026 02:03:09 GMT
LABEL org.label-schema.schema-version=1.0 org.label-schema.vendor=Elastic org.opencontainers.image.vendor=Elastic org.label-schema.name=logstash org.opencontainers.image.title=logstash org.label-schema.version=8.19.13 org.opencontainers.image.version=8.19.13 org.label-schema.url=https://www.elastic.co/products/logstash org.label-schema.vcs-url=https://github.com/elastic/logstash org.label-schema.license=Elastic License org.opencontainers.image.licenses=Elastic License org.opencontainers.image.description=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' org.label-schema.build-date=2026-03-10T13:51:26+00:00 org.opencontainers.image.created=2026-03-10T13:51:26+00:00
# Tue, 07 Apr 2026 02:03:09 GMT
ENTRYPOINT ["/usr/local/bin/docker-entrypoint"]
```

-	Layers:
	-	`sha256:76fd055477b6edf8004a5a962edad02a820d4c8b2f02682410edfbe376b418c5`  
		Last Modified: Fri, 03 Apr 2026 15:56:36 GMT  
		Size: 28.9 MB (28874075 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:576fb3d305ecbbca4ba38e97c6439992834dd03c13f4702778a77134e6514711`  
		Last Modified: Tue, 07 Apr 2026 02:03:51 GMT  
		Size: 55.2 MB (55225070 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebb1e6bf5ab8788d7d63769a705864ba9d493bc5fa92f9e26f357851027155e5`  
		Last Modified: Tue, 07 Apr 2026 02:03:48 GMT  
		Size: 1.2 KB (1223 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7daddb47a2670fc80effabd3c6a493283d7198597d72908fc26635d2812f9f45`  
		Last Modified: Tue, 07 Apr 2026 02:03:58 GMT  
		Size: 454.9 MB (454865892 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec70eed2a74d44ee293344e316733f147f6e343e3331ac667d6bc7a08a86faf9`  
		Last Modified: Tue, 07 Apr 2026 02:03:48 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47634a1a226214ca08a51435416f0988dd90102bf797fe91eb81cfd478cc9325`  
		Last Modified: Tue, 07 Apr 2026 02:03:49 GMT  
		Size: 1.6 KB (1583 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:745c48adc2c766f209010384807dedaf5056265b7a5b2b2bd57b025fa117e0d8`  
		Last Modified: Tue, 07 Apr 2026 02:03:49 GMT  
		Size: 278.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ead8e4613877454853a2080a4b4104e1f09d0298a8b089e30147eb4a657be877`  
		Last Modified: Tue, 07 Apr 2026 02:03:51 GMT  
		Size: 1.8 KB (1766 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05fa5978ba4dcd3a2299f8859cd52857b425421160efd8683de5e190cbb08862`  
		Last Modified: Tue, 07 Apr 2026 02:03:51 GMT  
		Size: 6.3 KB (6296 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bae42b33308dc7925fb4817220676d39337deee380c3bbcde88025ce916f4206`  
		Last Modified: Tue, 07 Apr 2026 02:03:52 GMT  
		Size: 255.2 KB (255185 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a8d2381b0a9f3dc7b82510a6efdb932bdd5819c79ba5e9e53de89a182e697a2`  
		Last Modified: Tue, 07 Apr 2026 02:03:52 GMT  
		Size: 354.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee034e2734ee6a9f64e284538371e31849e476cc46c9fc0046bcb0a75cf9c4d9`  
		Last Modified: Tue, 07 Apr 2026 02:03:53 GMT  
		Size: 713.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `logstash:8.19.13` - unknown; unknown

```console
$ docker pull logstash@sha256:d1cdbf7ed9c6942b132d1407d106b09a2249e86f2130b8a8894357959ced8268
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3732038 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:67e198207478a06298bdb317e621cb071a6746bb989470ff387107eebdae3152`

```dockerfile
```

-	Layers:
	-	`sha256:7cdd3a4c449d81c12318073f348330f5c3ccbfe292e1f4af7b9041c07d95830a`  
		Last Modified: Tue, 07 Apr 2026 02:03:48 GMT  
		Size: 3.7 MB (3696065 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1a9fe6dbaff4aabc63b695f8b2d0f21e29b78f973284513cb7fd9f77cd5ef1dc`  
		Last Modified: Tue, 07 Apr 2026 02:03:48 GMT  
		Size: 36.0 KB (35973 bytes)  
		MIME: application/vnd.in-toto+json

## `logstash:9.2.7`

```console
$ docker pull logstash@sha256:60c37510ec4251e72dc1a3f7005580be5631fc09a51b3c9a3b92fbcac89ab45c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `logstash:9.2.7` - linux; amd64

```console
$ docker pull logstash@sha256:89d564e252f131200c962a1f677fbd966a9148b822700775e75fc242d96d9aa3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **502.4 MB (502409211 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5073f77a29861a3956e284a24bd6bdbc811307e7a3093f3a3233d2f6b085c1b7`
-	Entrypoint: `["\/usr\/local\/bin\/docker-entrypoint"]`

```dockerfile
# Thu, 19 Mar 2026 17:02:51 GMT
LABEL maintainer="Red Hat, Inc."
# Thu, 19 Mar 2026 17:02:51 GMT
LABEL vendor="Red Hat, Inc."
# Thu, 19 Mar 2026 17:02:52 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Thu, 19 Mar 2026 17:02:52 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.7"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Thu, 19 Mar 2026 17:02:52 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Thu, 19 Mar 2026 17:02:52 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Thu, 19 Mar 2026 17:02:52 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 19 Mar 2026 17:02:52 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 19 Mar 2026 17:02:52 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Thu, 19 Mar 2026 17:02:52 GMT
LABEL io.openshift.expose-services=""
# Thu, 19 Mar 2026 17:02:52 GMT
LABEL io.openshift.tags="minimal rhel9"
# Thu, 19 Mar 2026 17:02:52 GMT
ENV container oci
# Thu, 19 Mar 2026 17:02:52 GMT
COPY dir:2cb6e43856cb0ad61489a8c64de98c252b875727203d4889684da9c688115b96 in /      
# Thu, 19 Mar 2026 17:02:52 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Thu, 19 Mar 2026 17:02:52 GMT
CMD ["/bin/bash"]
# Thu, 19 Mar 2026 17:02:52 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /usr/share/buildinfo/content-sets.json      
# Thu, 19 Mar 2026 17:02:53 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /root/buildinfo/content_manifests/content-sets.json      
# Thu, 19 Mar 2026 17:02:53 GMT
COPY file:289d553fe837e625c2f8fb767ab91c5be2d390395d3693929ca213958efa8fc8 in /usr/share/buildinfo/labels.json      
# Thu, 19 Mar 2026 17:02:53 GMT
COPY file:289d553fe837e625c2f8fb767ab91c5be2d390395d3693929ca213958efa8fc8 in /root/buildinfo/labels.json      
# Thu, 19 Mar 2026 17:02:53 GMT
LABEL "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="d0c250a501ab44b94ebea3e751fcaa45749a08a2" "org.opencontainers.image.revision"="d0c250a501ab44b94ebea3e751fcaa45749a08a2" "build-date"="2026-03-19T17:02:39Z" "org.opencontainers.image.created"="2026-03-19T17:02:39Z" "release"="1773939694"org.opencontainers.image.revision=d0c250a501ab44b94ebea3e751fcaa45749a08a2,org.opencontainers.image.created=2026-03-19T17:02:39Z
# Fri, 20 Mar 2026 00:18:05 GMT
ENV ELASTIC_CONTAINER=true
# Fri, 20 Mar 2026 00:18:05 GMT
ENV PATH=/usr/share/logstash/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 20 Mar 2026 00:18:05 GMT
ENV LANG=C.UTF-8 LC_ALL=C.UTF-8
# Fri, 20 Mar 2026 00:18:05 GMT
WORKDIR /usr/share
# Fri, 20 Mar 2026 00:18:07 GMT
RUN microdnf install -y procps findutils tar gzip &&   microdnf install -y openssl &&   microdnf install -y which shadow-utils &&   microdnf clean all # buildkit
# Fri, 20 Mar 2026 00:18:58 GMT
RUN groupadd --gid 1000 logstash &&   adduser --uid 1000 --gid 1000   --home "/usr/share/logstash"   --no-create-home   logstash &&   arch="$(rpm --query --queryformat='%{ARCH}' rpm)" &&   curl --fail --location --output logstash.tar.gz https://artifacts.elastic.co/downloads/logstash/logstash-9.2.7-linux-${arch}.tar.gz &&   tar -zxf logstash.tar.gz -C /usr/share &&   rm logstash.tar.gz &&   mv /usr/share/logstash-9.2.7 /usr/share/logstash &&   chown -R logstash:root /usr/share/logstash &&   chmod -R g=u /usr/share/logstash &&   mkdir /licenses &&   mv /usr/share/logstash/NOTICE.TXT /licenses/NOTICE.TXT &&   mv /usr/share/logstash/LICENSE.txt /licenses/LICENSE.txt &&   find /usr/share/logstash -type d -exec chmod g+s {} \; &&   ln -s /usr/share/logstash /opt/logstash # buildkit
# Fri, 20 Mar 2026 00:18:58 GMT
COPY --chown=logstash:root env2yaml/classes /usr/share/logstash/env2yaml/classes/ # buildkit
# Fri, 20 Mar 2026 00:18:58 GMT
COPY --chown=logstash:root env2yaml/lib /usr/share/logstash/env2yaml/lib/ # buildkit
# Fri, 20 Mar 2026 00:18:58 GMT
COPY --chmod=0755 env2yaml/env2yaml /usr/local/bin/env2yaml # buildkit
# Fri, 20 Mar 2026 00:18:58 GMT
COPY --chown=logstash:root config/pipelines.yml config/log4j2.properties config/log4j2.file.properties /usr/share/logstash/config/ # buildkit
# Fri, 20 Mar 2026 00:18:58 GMT
COPY --chown=logstash:root config/logstash-full.yml /usr/share/logstash/config/logstash.yml # buildkit
# Fri, 20 Mar 2026 00:18:58 GMT
COPY --chown=logstash:root pipeline/default.conf /usr/share/logstash/pipeline/logstash.conf # buildkit
# Fri, 20 Mar 2026 00:18:59 GMT
COPY --chmod=0755 bin/docker-entrypoint /usr/local/bin/ # buildkit
# Fri, 20 Mar 2026 00:18:59 GMT
WORKDIR /usr/share/logstash
# Fri, 20 Mar 2026 00:18:59 GMT
USER 1000
# Fri, 20 Mar 2026 00:18:59 GMT
EXPOSE map[5044/tcp:{} 9600/tcp:{}]
# Fri, 20 Mar 2026 00:18:59 GMT
LABEL org.label-schema.build-date=2026-03-10T15:01:58+00:00 org.label-schema.license=Elastic License org.label-schema.name=logstash org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/logstash org.label-schema.vcs-url=https://github.com/elastic/logstash org.label-schema.vendor=Elastic org.label-schema.version=9.2.7 org.opencontainers.image.created=2026-03-10T15:01:58+00:00 org.opencontainers.image.description=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' org.opencontainers.image.licenses=Elastic License org.opencontainers.image.title=logstash org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=9.2.7 description=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' license=Elastic License maintainer=info@elastic.co name=logstash summary=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' vendor=Elastic
# Fri, 20 Mar 2026 00:18:59 GMT
ENTRYPOINT ["/usr/local/bin/docker-entrypoint"]
```

-	Layers:
	-	`sha256:75bed6ef625ff772ca48f63f12693f16f2b44649aa07030a7c4bc6b85225d5dd`  
		Last Modified: Thu, 19 Mar 2026 17:57:56 GMT  
		Size: 40.0 MB (40031119 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25e7b58d85b237b45bf5050ef0b503afd6ee6ce2df515da61e9fdbf740093155`  
		Last Modified: Fri, 20 Mar 2026 00:19:34 GMT  
		Size: 5.2 MB (5154854 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7847128f703b2806de98b724b841f7e2647922c3642e941decc39bae38d56428`  
		Last Modified: Fri, 20 Mar 2026 00:19:45 GMT  
		Size: 457.0 MB (456958510 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:054df0dded86ba9ac8e28abdc3146ec17dd6ed160da3cdb260caf2c82eabd410`  
		Last Modified: Fri, 20 Mar 2026 00:19:34 GMT  
		Size: 6.3 KB (6293 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba9d7ba96df75eb0f99bea059616bda24e6f043524de1e672ab9a7934398dff8`  
		Last Modified: Fri, 20 Mar 2026 00:19:34 GMT  
		Size: 255.2 KB (255182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3d260ff3d826e1ecb6d1cc66dbea0fe65fa3273eb87663cd208ad457f7829fa`  
		Last Modified: Fri, 20 Mar 2026 00:19:35 GMT  
		Size: 354.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:441b1428d69bc744d30f1f657e44065547f640ad713b3722fa9bde2271cc4ba7`  
		Last Modified: Fri, 20 Mar 2026 00:19:35 GMT  
		Size: 1.6 KB (1574 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f19e5715547713bf4e3610df03d14c810fb7289178b013a15854852adb2abe7d`  
		Last Modified: Fri, 20 Mar 2026 00:19:35 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6070ab62aacea5c722cc391f40d5f8d161a191f9819a73538b00d80008627969`  
		Last Modified: Fri, 20 Mar 2026 00:19:36 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9894778709bef0909ac8c4d369e75c165b1aa3cd488502089ab1d0f01f9b3349`  
		Last Modified: Fri, 20 Mar 2026 00:19:36 GMT  
		Size: 711.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `logstash:9.2.7` - unknown; unknown

```console
$ docker pull logstash@sha256:933303f7d1fce03be532709db3ed0049bcbd5efe8f9959da396c204ec4a020b8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2169954 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:43c8898597c185b7290ecb46c893aa33033ebd55bfee2863c7da04fc912f82c9`

```dockerfile
```

-	Layers:
	-	`sha256:703b8b77b6bbda13bd8589639b117aee4b53a0dc6f96c90e921a83f646b3e981`  
		Last Modified: Fri, 20 Mar 2026 00:19:34 GMT  
		Size: 2.1 MB (2139754 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:506188ad7b5865c31f4e1b0b2450e612b3537ec3383efdc2c2b868e9d6a38e7f`  
		Last Modified: Fri, 20 Mar 2026 00:19:34 GMT  
		Size: 30.2 KB (30200 bytes)  
		MIME: application/vnd.in-toto+json

### `logstash:9.2.7` - linux; arm64 variant v8

```console
$ docker pull logstash@sha256:669b618330f0df2ae884f521ef1538508bfdb80abf368f63977f6acbdcfff464
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **498.9 MB (498861347 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c1201e0b131ee750acab14e05dc439e9bf5ea2298e02cd4dba8b9ee42150a6ba`
-	Entrypoint: `["\/usr\/local\/bin\/docker-entrypoint"]`

```dockerfile
# Thu, 19 Mar 2026 17:04:53 GMT
LABEL maintainer="Red Hat, Inc."
# Thu, 19 Mar 2026 17:04:53 GMT
LABEL vendor="Red Hat, Inc."
# Thu, 19 Mar 2026 17:04:53 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Thu, 19 Mar 2026 17:04:53 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.7"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Thu, 19 Mar 2026 17:04:53 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Thu, 19 Mar 2026 17:04:53 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Thu, 19 Mar 2026 17:04:53 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 19 Mar 2026 17:04:53 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 19 Mar 2026 17:04:53 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Thu, 19 Mar 2026 17:04:53 GMT
LABEL io.openshift.expose-services=""
# Thu, 19 Mar 2026 17:04:53 GMT
LABEL io.openshift.tags="minimal rhel9"
# Thu, 19 Mar 2026 17:04:53 GMT
ENV container oci
# Thu, 19 Mar 2026 17:04:54 GMT
COPY dir:ebed5b428b4d7b7bd491e92b7639c4e00e22e8a9993f0cbde996cf63a3263224 in /      
# Thu, 19 Mar 2026 17:04:54 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Thu, 19 Mar 2026 17:04:54 GMT
CMD ["/bin/bash"]
# Thu, 19 Mar 2026 17:04:55 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /usr/share/buildinfo/content-sets.json      
# Thu, 19 Mar 2026 17:04:55 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /root/buildinfo/content_manifests/content-sets.json      
# Thu, 19 Mar 2026 17:04:55 GMT
COPY file:819fd782db190e306ad6dedf6720029cee5c6639348ef8be1d7fa1456c09e46b in /usr/share/buildinfo/labels.json      
# Thu, 19 Mar 2026 17:04:55 GMT
COPY file:819fd782db190e306ad6dedf6720029cee5c6639348ef8be1d7fa1456c09e46b in /root/buildinfo/labels.json      
# Thu, 19 Mar 2026 17:04:55 GMT
LABEL "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="d0c250a501ab44b94ebea3e751fcaa45749a08a2" "org.opencontainers.image.revision"="d0c250a501ab44b94ebea3e751fcaa45749a08a2" "build-date"="2026-03-19T17:04:41Z" "org.opencontainers.image.created"="2026-03-19T17:04:41Z" "release"="1773939694"org.opencontainers.image.revision=d0c250a501ab44b94ebea3e751fcaa45749a08a2,org.opencontainers.image.created=2026-03-19T17:04:41Z
# Fri, 20 Mar 2026 00:16:02 GMT
ENV ELASTIC_CONTAINER=true
# Fri, 20 Mar 2026 00:16:02 GMT
ENV PATH=/usr/share/logstash/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 20 Mar 2026 00:16:02 GMT
ENV LANG=C.UTF-8 LC_ALL=C.UTF-8
# Fri, 20 Mar 2026 00:16:02 GMT
WORKDIR /usr/share
# Fri, 20 Mar 2026 00:16:04 GMT
RUN microdnf install -y procps findutils tar gzip &&   microdnf install -y openssl &&   microdnf install -y which shadow-utils &&   microdnf clean all # buildkit
# Fri, 20 Mar 2026 00:17:03 GMT
RUN groupadd --gid 1000 logstash &&   adduser --uid 1000 --gid 1000   --home "/usr/share/logstash"   --no-create-home   logstash &&   arch="$(rpm --query --queryformat='%{ARCH}' rpm)" &&   curl --fail --location --output logstash.tar.gz https://artifacts.elastic.co/downloads/logstash/logstash-9.2.7-linux-${arch}.tar.gz &&   tar -zxf logstash.tar.gz -C /usr/share &&   rm logstash.tar.gz &&   mv /usr/share/logstash-9.2.7 /usr/share/logstash &&   chown -R logstash:root /usr/share/logstash &&   chmod -R g=u /usr/share/logstash &&   mkdir /licenses &&   mv /usr/share/logstash/NOTICE.TXT /licenses/NOTICE.TXT &&   mv /usr/share/logstash/LICENSE.txt /licenses/LICENSE.txt &&   find /usr/share/logstash -type d -exec chmod g+s {} \; &&   ln -s /usr/share/logstash /opt/logstash # buildkit
# Fri, 20 Mar 2026 00:17:03 GMT
COPY --chown=logstash:root env2yaml/classes /usr/share/logstash/env2yaml/classes/ # buildkit
# Fri, 20 Mar 2026 00:17:03 GMT
COPY --chown=logstash:root env2yaml/lib /usr/share/logstash/env2yaml/lib/ # buildkit
# Fri, 20 Mar 2026 00:17:03 GMT
COPY --chmod=0755 env2yaml/env2yaml /usr/local/bin/env2yaml # buildkit
# Fri, 20 Mar 2026 00:17:03 GMT
COPY --chown=logstash:root config/pipelines.yml config/log4j2.properties config/log4j2.file.properties /usr/share/logstash/config/ # buildkit
# Fri, 20 Mar 2026 00:17:03 GMT
COPY --chown=logstash:root config/logstash-full.yml /usr/share/logstash/config/logstash.yml # buildkit
# Fri, 20 Mar 2026 00:17:03 GMT
COPY --chown=logstash:root pipeline/default.conf /usr/share/logstash/pipeline/logstash.conf # buildkit
# Fri, 20 Mar 2026 00:17:03 GMT
COPY --chmod=0755 bin/docker-entrypoint /usr/local/bin/ # buildkit
# Fri, 20 Mar 2026 00:17:03 GMT
WORKDIR /usr/share/logstash
# Fri, 20 Mar 2026 00:17:03 GMT
USER 1000
# Fri, 20 Mar 2026 00:17:03 GMT
EXPOSE map[5044/tcp:{} 9600/tcp:{}]
# Fri, 20 Mar 2026 00:17:03 GMT
LABEL org.label-schema.build-date=2026-03-10T15:01:58+00:00 org.label-schema.license=Elastic License org.label-schema.name=logstash org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/logstash org.label-schema.vcs-url=https://github.com/elastic/logstash org.label-schema.vendor=Elastic org.label-schema.version=9.2.7 org.opencontainers.image.created=2026-03-10T15:01:58+00:00 org.opencontainers.image.description=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' org.opencontainers.image.licenses=Elastic License org.opencontainers.image.title=logstash org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=9.2.7 description=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' license=Elastic License maintainer=info@elastic.co name=logstash summary=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' vendor=Elastic
# Fri, 20 Mar 2026 00:17:03 GMT
ENTRYPOINT ["/usr/local/bin/docker-entrypoint"]
```

-	Layers:
	-	`sha256:58b15a07209fe35d94749ac0349d53a753811f2289c2cd68bbdf7aefa4462360`  
		Last Modified: Thu, 19 Mar 2026 18:10:21 GMT  
		Size: 38.2 MB (38204902 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2437fdd1f7c6cfc16f57c95ace35edb7fd9b94194a726f5bdd5f6f1d0e4d30f`  
		Last Modified: Fri, 20 Mar 2026 00:17:40 GMT  
		Size: 5.2 MB (5155548 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:671dccb3af213cf364cf75aa74a0e085a24bb595d129a26aabfb2fdb18df3c5d`  
		Last Modified: Fri, 20 Mar 2026 00:17:49 GMT  
		Size: 455.2 MB (455236164 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3647ffc3b772978ed22673dfe936e0e68a27b08d419adb66a15c847265796f5`  
		Last Modified: Fri, 20 Mar 2026 00:17:40 GMT  
		Size: 6.3 KB (6295 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe5264484c1c29ae56ed3d8d4b701c646485cb1361cfb0396eafa2628de62ad2`  
		Last Modified: Fri, 20 Mar 2026 00:17:40 GMT  
		Size: 255.2 KB (255187 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5cde27b062d7698bc35ea45d2fd5d497d7dfda5911a87c12f9dd7fb496e2594c`  
		Last Modified: Fri, 20 Mar 2026 00:17:41 GMT  
		Size: 352.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e25177ff4a0aeb1976a01661e03312dd7698cb55ccc009b04de383c36e40e969`  
		Last Modified: Fri, 20 Mar 2026 00:17:41 GMT  
		Size: 1.6 KB (1575 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b06ada9e180efe4e2e7e5142b43f786fda821ec2f4ec3a047755076feac8f5f`  
		Last Modified: Fri, 20 Mar 2026 00:17:42 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9bae6e2f126623be86f617019551bf617afe0e0c5e197e1fc5b211dd7dabe316`  
		Last Modified: Fri, 20 Mar 2026 00:17:43 GMT  
		Size: 274.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c83a2a05060333e0f880b1378fd46f7343d5a27f339c34ceaa5379f69bc9f6e0`  
		Last Modified: Fri, 20 Mar 2026 00:17:43 GMT  
		Size: 711.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `logstash:9.2.7` - unknown; unknown

```console
$ docker pull logstash@sha256:c9a28aa3aca0683d1b0f8e6244a896f0968498a27ee1bd9438c8606cea2361af
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2170600 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:38ad69d8e785b5b207578c30ceb883466c119adb5b5114f585c8a66dd577bae6`

```dockerfile
```

-	Layers:
	-	`sha256:3a24ac637bdb9389965cbdb896316479e4cc0705684abbed70e135c5eb5cb35d`  
		Last Modified: Fri, 20 Mar 2026 00:17:40 GMT  
		Size: 2.1 MB (2140324 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9c2cc2839e112dec4a0a63cb96b51a4d37cb983d288f6ec694cfd54dfc9fa093`  
		Last Modified: Fri, 20 Mar 2026 00:17:40 GMT  
		Size: 30.3 KB (30276 bytes)  
		MIME: application/vnd.in-toto+json

## `logstash:9.3.2`

```console
$ docker pull logstash@sha256:b1e953e7da9185efc6f190bacc254cf290eb9ca5f9dfbc82e77ad31bec6cd6ab
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `logstash:9.3.2` - linux; amd64

```console
$ docker pull logstash@sha256:e9a4f0f97876b6d81f03904212edf7f96f20d6cf29f8056fbca978450cd41648
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **516.7 MB (516707307 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04a8891fcf262dbff13b019f13aee8514cb0cfaabcc0abff48523312d99e7cc8`
-	Entrypoint: `["\/usr\/local\/bin\/docker-entrypoint"]`

```dockerfile
# Thu, 19 Mar 2026 17:02:51 GMT
LABEL maintainer="Red Hat, Inc."
# Thu, 19 Mar 2026 17:02:51 GMT
LABEL vendor="Red Hat, Inc."
# Thu, 19 Mar 2026 17:02:52 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Thu, 19 Mar 2026 17:02:52 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.7"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Thu, 19 Mar 2026 17:02:52 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Thu, 19 Mar 2026 17:02:52 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Thu, 19 Mar 2026 17:02:52 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 19 Mar 2026 17:02:52 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 19 Mar 2026 17:02:52 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Thu, 19 Mar 2026 17:02:52 GMT
LABEL io.openshift.expose-services=""
# Thu, 19 Mar 2026 17:02:52 GMT
LABEL io.openshift.tags="minimal rhel9"
# Thu, 19 Mar 2026 17:02:52 GMT
ENV container oci
# Thu, 19 Mar 2026 17:02:52 GMT
COPY dir:2cb6e43856cb0ad61489a8c64de98c252b875727203d4889684da9c688115b96 in /      
# Thu, 19 Mar 2026 17:02:52 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Thu, 19 Mar 2026 17:02:52 GMT
CMD ["/bin/bash"]
# Thu, 19 Mar 2026 17:02:52 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /usr/share/buildinfo/content-sets.json      
# Thu, 19 Mar 2026 17:02:53 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /root/buildinfo/content_manifests/content-sets.json      
# Thu, 19 Mar 2026 17:02:53 GMT
COPY file:289d553fe837e625c2f8fb767ab91c5be2d390395d3693929ca213958efa8fc8 in /usr/share/buildinfo/labels.json      
# Thu, 19 Mar 2026 17:02:53 GMT
COPY file:289d553fe837e625c2f8fb767ab91c5be2d390395d3693929ca213958efa8fc8 in /root/buildinfo/labels.json      
# Thu, 19 Mar 2026 17:02:53 GMT
LABEL "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="d0c250a501ab44b94ebea3e751fcaa45749a08a2" "org.opencontainers.image.revision"="d0c250a501ab44b94ebea3e751fcaa45749a08a2" "build-date"="2026-03-19T17:02:39Z" "org.opencontainers.image.created"="2026-03-19T17:02:39Z" "release"="1773939694"org.opencontainers.image.revision=d0c250a501ab44b94ebea3e751fcaa45749a08a2,org.opencontainers.image.created=2026-03-19T17:02:39Z
# Fri, 20 Mar 2026 00:18:02 GMT
ENV ELASTIC_CONTAINER=true
# Fri, 20 Mar 2026 00:18:02 GMT
ENV PATH=/usr/share/logstash/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 20 Mar 2026 00:18:02 GMT
ENV LANG=C.UTF-8 LC_ALL=C.UTF-8
# Fri, 20 Mar 2026 00:18:02 GMT
WORKDIR /usr/share
# Fri, 20 Mar 2026 00:18:04 GMT
RUN microdnf install -y procps findutils tar gzip &&   microdnf install -y openssl &&   microdnf install -y which shadow-utils &&   microdnf clean all # buildkit
# Fri, 20 Mar 2026 00:18:56 GMT
RUN groupadd --gid 1000 logstash &&   adduser --uid 1000 --gid 1000   --home "/usr/share/logstash"   --no-create-home   logstash &&   arch="$(rpm --query --queryformat='%{ARCH}' rpm)" &&   curl --fail --location --output logstash.tar.gz https://artifacts.elastic.co/downloads/logstash/logstash-9.3.2-linux-${arch}.tar.gz &&   tar -zxf logstash.tar.gz -C /usr/share &&   rm logstash.tar.gz &&   mv /usr/share/logstash-9.3.2 /usr/share/logstash &&   chown -R logstash:root /usr/share/logstash &&   chmod -R g=u /usr/share/logstash &&   mkdir /licenses &&   mv /usr/share/logstash/NOTICE.TXT /licenses/NOTICE.TXT &&   mv /usr/share/logstash/LICENSE.txt /licenses/LICENSE.txt &&   find /usr/share/logstash -type d -exec chmod g+s {} \; &&   ln -s /usr/share/logstash /opt/logstash # buildkit
# Fri, 20 Mar 2026 00:18:56 GMT
COPY --chown=logstash:root env2yaml/classes /usr/share/logstash/env2yaml/classes/ # buildkit
# Fri, 20 Mar 2026 00:18:56 GMT
COPY --chown=logstash:root env2yaml/lib /usr/share/logstash/env2yaml/lib/ # buildkit
# Fri, 20 Mar 2026 00:18:56 GMT
COPY --chmod=0755 env2yaml/env2yaml /usr/local/bin/env2yaml # buildkit
# Fri, 20 Mar 2026 00:18:56 GMT
COPY --chown=logstash:root config/pipelines.yml config/log4j2.properties config/log4j2.file.properties /usr/share/logstash/config/ # buildkit
# Fri, 20 Mar 2026 00:18:56 GMT
COPY --chown=logstash:root config/logstash-full.yml /usr/share/logstash/config/logstash.yml # buildkit
# Fri, 20 Mar 2026 00:18:56 GMT
COPY --chown=logstash:root pipeline/default.conf /usr/share/logstash/pipeline/logstash.conf # buildkit
# Fri, 20 Mar 2026 00:18:56 GMT
COPY --chmod=0755 bin/docker-entrypoint /usr/local/bin/ # buildkit
# Fri, 20 Mar 2026 00:18:56 GMT
WORKDIR /usr/share/logstash
# Fri, 20 Mar 2026 00:18:56 GMT
USER 1000
# Fri, 20 Mar 2026 00:18:56 GMT
EXPOSE map[5044/tcp:{} 9600/tcp:{}]
# Fri, 20 Mar 2026 00:18:56 GMT
LABEL org.label-schema.build-date=2026-03-10T17:13:01+00:00 org.label-schema.license=Elastic License org.label-schema.name=logstash org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/logstash org.label-schema.vcs-url=https://github.com/elastic/logstash org.label-schema.vendor=Elastic org.label-schema.version=9.3.2 org.opencontainers.image.created=2026-03-10T17:13:01+00:00 org.opencontainers.image.description=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' org.opencontainers.image.licenses=Elastic License org.opencontainers.image.title=logstash org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=9.3.2 description=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' license=Elastic License maintainer=info@elastic.co name=logstash summary=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' vendor=Elastic
# Fri, 20 Mar 2026 00:18:56 GMT
ENTRYPOINT ["/usr/local/bin/docker-entrypoint"]
```

-	Layers:
	-	`sha256:75bed6ef625ff772ca48f63f12693f16f2b44649aa07030a7c4bc6b85225d5dd`  
		Last Modified: Thu, 19 Mar 2026 17:57:56 GMT  
		Size: 40.0 MB (40031119 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ee56507cc2559f5db8f61bd30006f6d19a96edda91be6b1838bc78cc4c2c3cf`  
		Last Modified: Fri, 20 Mar 2026 00:19:30 GMT  
		Size: 5.2 MB (5154880 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e635dd7b466f6629e69aeae8fcb5791cbaf7f61e4282be192177e4a3403b7ea3`  
		Last Modified: Fri, 20 Mar 2026 00:19:41 GMT  
		Size: 471.3 MB (471256583 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04e73e5480a258cbc92278fc066efed40cc5e4aa5f9652a8a6728486637ec6cc`  
		Last Modified: Fri, 20 Mar 2026 00:19:30 GMT  
		Size: 6.3 KB (6295 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6008836bdb87362167ebd91df56a8b560c45386a44cccb6282480ed7251e565`  
		Last Modified: Fri, 20 Mar 2026 00:19:30 GMT  
		Size: 255.2 KB (255181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:900dd28a2035ca5ddfd8647e8beb445b1072eef4603b0cd771172d3fded41038`  
		Last Modified: Fri, 20 Mar 2026 00:19:31 GMT  
		Size: 351.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd53e97a112fc3e6c6a4ffe796fc68cfed637a90350f025a768ca3b6768942e9`  
		Last Modified: Fri, 20 Mar 2026 00:19:31 GMT  
		Size: 1.6 KB (1574 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:118ab693bfc241bc13808cae4ad210f7d84c16865a6ddc85a23c903945785e48`  
		Last Modified: Fri, 20 Mar 2026 00:19:33 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0cf68e20f9a00ddf7c4b9f2fb7ed716a25f28d5e7d6e2cdfcde06b352d9978d9`  
		Last Modified: Fri, 20 Mar 2026 00:19:33 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:938733d6a7c65feae2a8149cce310180085159902e2d89a52ca6e4a4adaa515d`  
		Last Modified: Fri, 20 Mar 2026 00:19:33 GMT  
		Size: 710.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `logstash:9.3.2` - unknown; unknown

```console
$ docker pull logstash@sha256:fa56d7d5123abe3398d4360379e34be8e5b49c76dc06ee20810383b5cb261f52
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2149441 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b804676aee140e1532f5b4c29722e0d85a7cd3ca1ffdcca410e698f24964a9d`

```dockerfile
```

-	Layers:
	-	`sha256:ff1ae278acfd44d30d8a88b9895a7984e3a132e4fa96ee44c7da3cd9937d10f2`  
		Last Modified: Fri, 20 Mar 2026 00:19:30 GMT  
		Size: 2.1 MB (2119241 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7b4431ddb632f7401b627c072da63aa598cb6bc3fd1682bcd1ed166799c35f2b`  
		Last Modified: Fri, 20 Mar 2026 00:19:30 GMT  
		Size: 30.2 KB (30200 bytes)  
		MIME: application/vnd.in-toto+json

### `logstash:9.3.2` - linux; arm64 variant v8

```console
$ docker pull logstash@sha256:ae57b868421bfbed45900d9efc6dcc8884b0d39bdc571bb9f9feebe7bb14e62c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **513.2 MB (513168767 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ea62d639412766afba4c14afab993153e73444e80dd96da8824c17be918dcd2`
-	Entrypoint: `["\/usr\/local\/bin\/docker-entrypoint"]`

```dockerfile
# Thu, 19 Mar 2026 17:04:53 GMT
LABEL maintainer="Red Hat, Inc."
# Thu, 19 Mar 2026 17:04:53 GMT
LABEL vendor="Red Hat, Inc."
# Thu, 19 Mar 2026 17:04:53 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Thu, 19 Mar 2026 17:04:53 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.7"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Thu, 19 Mar 2026 17:04:53 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Thu, 19 Mar 2026 17:04:53 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Thu, 19 Mar 2026 17:04:53 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 19 Mar 2026 17:04:53 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 19 Mar 2026 17:04:53 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Thu, 19 Mar 2026 17:04:53 GMT
LABEL io.openshift.expose-services=""
# Thu, 19 Mar 2026 17:04:53 GMT
LABEL io.openshift.tags="minimal rhel9"
# Thu, 19 Mar 2026 17:04:53 GMT
ENV container oci
# Thu, 19 Mar 2026 17:04:54 GMT
COPY dir:ebed5b428b4d7b7bd491e92b7639c4e00e22e8a9993f0cbde996cf63a3263224 in /      
# Thu, 19 Mar 2026 17:04:54 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Thu, 19 Mar 2026 17:04:54 GMT
CMD ["/bin/bash"]
# Thu, 19 Mar 2026 17:04:55 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /usr/share/buildinfo/content-sets.json      
# Thu, 19 Mar 2026 17:04:55 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /root/buildinfo/content_manifests/content-sets.json      
# Thu, 19 Mar 2026 17:04:55 GMT
COPY file:819fd782db190e306ad6dedf6720029cee5c6639348ef8be1d7fa1456c09e46b in /usr/share/buildinfo/labels.json      
# Thu, 19 Mar 2026 17:04:55 GMT
COPY file:819fd782db190e306ad6dedf6720029cee5c6639348ef8be1d7fa1456c09e46b in /root/buildinfo/labels.json      
# Thu, 19 Mar 2026 17:04:55 GMT
LABEL "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="d0c250a501ab44b94ebea3e751fcaa45749a08a2" "org.opencontainers.image.revision"="d0c250a501ab44b94ebea3e751fcaa45749a08a2" "build-date"="2026-03-19T17:04:41Z" "org.opencontainers.image.created"="2026-03-19T17:04:41Z" "release"="1773939694"org.opencontainers.image.revision=d0c250a501ab44b94ebea3e751fcaa45749a08a2,org.opencontainers.image.created=2026-03-19T17:04:41Z
# Fri, 20 Mar 2026 00:16:05 GMT
ENV ELASTIC_CONTAINER=true
# Fri, 20 Mar 2026 00:16:05 GMT
ENV PATH=/usr/share/logstash/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 20 Mar 2026 00:16:05 GMT
ENV LANG=C.UTF-8 LC_ALL=C.UTF-8
# Fri, 20 Mar 2026 00:16:05 GMT
WORKDIR /usr/share
# Fri, 20 Mar 2026 00:16:07 GMT
RUN microdnf install -y procps findutils tar gzip &&   microdnf install -y openssl &&   microdnf install -y which shadow-utils &&   microdnf clean all # buildkit
# Fri, 20 Mar 2026 00:17:03 GMT
RUN groupadd --gid 1000 logstash &&   adduser --uid 1000 --gid 1000   --home "/usr/share/logstash"   --no-create-home   logstash &&   arch="$(rpm --query --queryformat='%{ARCH}' rpm)" &&   curl --fail --location --output logstash.tar.gz https://artifacts.elastic.co/downloads/logstash/logstash-9.3.2-linux-${arch}.tar.gz &&   tar -zxf logstash.tar.gz -C /usr/share &&   rm logstash.tar.gz &&   mv /usr/share/logstash-9.3.2 /usr/share/logstash &&   chown -R logstash:root /usr/share/logstash &&   chmod -R g=u /usr/share/logstash &&   mkdir /licenses &&   mv /usr/share/logstash/NOTICE.TXT /licenses/NOTICE.TXT &&   mv /usr/share/logstash/LICENSE.txt /licenses/LICENSE.txt &&   find /usr/share/logstash -type d -exec chmod g+s {} \; &&   ln -s /usr/share/logstash /opt/logstash # buildkit
# Fri, 20 Mar 2026 00:17:03 GMT
COPY --chown=logstash:root env2yaml/classes /usr/share/logstash/env2yaml/classes/ # buildkit
# Fri, 20 Mar 2026 00:17:03 GMT
COPY --chown=logstash:root env2yaml/lib /usr/share/logstash/env2yaml/lib/ # buildkit
# Fri, 20 Mar 2026 00:17:03 GMT
COPY --chmod=0755 env2yaml/env2yaml /usr/local/bin/env2yaml # buildkit
# Fri, 20 Mar 2026 00:17:03 GMT
COPY --chown=logstash:root config/pipelines.yml config/log4j2.properties config/log4j2.file.properties /usr/share/logstash/config/ # buildkit
# Fri, 20 Mar 2026 00:17:03 GMT
COPY --chown=logstash:root config/logstash-full.yml /usr/share/logstash/config/logstash.yml # buildkit
# Fri, 20 Mar 2026 00:17:03 GMT
COPY --chown=logstash:root pipeline/default.conf /usr/share/logstash/pipeline/logstash.conf # buildkit
# Fri, 20 Mar 2026 00:17:03 GMT
COPY --chmod=0755 bin/docker-entrypoint /usr/local/bin/ # buildkit
# Fri, 20 Mar 2026 00:17:03 GMT
WORKDIR /usr/share/logstash
# Fri, 20 Mar 2026 00:17:03 GMT
USER 1000
# Fri, 20 Mar 2026 00:17:03 GMT
EXPOSE map[5044/tcp:{} 9600/tcp:{}]
# Fri, 20 Mar 2026 00:17:03 GMT
LABEL org.label-schema.build-date=2026-03-10T17:13:01+00:00 org.label-schema.license=Elastic License org.label-schema.name=logstash org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/logstash org.label-schema.vcs-url=https://github.com/elastic/logstash org.label-schema.vendor=Elastic org.label-schema.version=9.3.2 org.opencontainers.image.created=2026-03-10T17:13:01+00:00 org.opencontainers.image.description=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' org.opencontainers.image.licenses=Elastic License org.opencontainers.image.title=logstash org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=9.3.2 description=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' license=Elastic License maintainer=info@elastic.co name=logstash summary=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' vendor=Elastic
# Fri, 20 Mar 2026 00:17:03 GMT
ENTRYPOINT ["/usr/local/bin/docker-entrypoint"]
```

-	Layers:
	-	`sha256:58b15a07209fe35d94749ac0349d53a753811f2289c2cd68bbdf7aefa4462360`  
		Last Modified: Thu, 19 Mar 2026 18:10:21 GMT  
		Size: 38.2 MB (38204902 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:edc72d85834f8cad087247079c798657c2db0a4ebc1ee18f5e6a42a4a94085ce`  
		Last Modified: Fri, 20 Mar 2026 00:17:41 GMT  
		Size: 5.2 MB (5155556 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3bdbc91fa3bca48638fa344aa733d9dae90c337aba825db8578a0988a65b63e2`  
		Last Modified: Fri, 20 Mar 2026 00:17:51 GMT  
		Size: 469.5 MB (469543577 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:377cce27256deb0fc2b894d00130bedb1a4e90db70da650145896b098d60b1dd`  
		Last Modified: Fri, 20 Mar 2026 00:17:41 GMT  
		Size: 6.3 KB (6295 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19cbfc0fab9a6207df1c5aac228071a5189662bf136f9444c7bf48013daaecea`  
		Last Modified: Fri, 20 Mar 2026 00:17:41 GMT  
		Size: 255.2 KB (255186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1f01639dd5c695dcc1bde49fc020818497e7eb859fd24dd4f3ef13687a595be`  
		Last Modified: Fri, 20 Mar 2026 00:17:42 GMT  
		Size: 353.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:775e40fe19bfe72587d315b60fd615ee8ff618baffccf1a641343ec8c51b513e`  
		Last Modified: Fri, 20 Mar 2026 00:17:42 GMT  
		Size: 1.6 KB (1575 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39feea8f30a969067308b1182e341bd82a7a1445b66974e47b7e153210c97012`  
		Last Modified: Fri, 20 Mar 2026 00:17:42 GMT  
		Size: 274.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad9e48e5e6788e5966cb1f8ad92f753873837412990eae200da38d0f018461ca`  
		Last Modified: Fri, 20 Mar 2026 00:17:43 GMT  
		Size: 274.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2ba62fa5fc09006ef5d0e0868d14d0314623aaef11480731daa09205711fe27`  
		Last Modified: Fri, 20 Mar 2026 00:17:43 GMT  
		Size: 711.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `logstash:9.3.2` - unknown; unknown

```console
$ docker pull logstash@sha256:072e825ec6b2543c240e72b758769e567c79a275228b7e42e1be5fbca343e94e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2150087 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:047127a241b48bc942197e58af31f2061ba0e2b790e1870dedcf3e2a845fb732`

```dockerfile
```

-	Layers:
	-	`sha256:491dabe1eb37942f69273dc81267e7206b9994c7be28bde6cece7a73ea9e9e85`  
		Last Modified: Fri, 20 Mar 2026 00:17:41 GMT  
		Size: 2.1 MB (2119811 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ddf863b93bf752a073c4333c48c8144bc7651680cd2c330e0a0197564b3f0e7d`  
		Last Modified: Fri, 20 Mar 2026 00:17:41 GMT  
		Size: 30.3 KB (30276 bytes)  
		MIME: application/vnd.in-toto+json
