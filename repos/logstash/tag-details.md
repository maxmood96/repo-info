<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `logstash`

-	[`logstash:8.18.8`](#logstash8188)
-	[`logstash:8.19.9`](#logstash8199)
-	[`logstash:9.1.9`](#logstash919)
-	[`logstash:9.2.3`](#logstash923)

## `logstash:8.18.8`

```console
$ docker pull logstash@sha256:f2608dcb12d14d3aa4a3aad470bbcac1f5cc391baa64a0c560f41a70c7e514b9
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `logstash:8.18.8` - linux; amd64

```console
$ docker pull logstash@sha256:0c561a809266e5787e59e27cf7c10ad53a51d695aa01464b3fe1fe3447f28303
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **525.8 MB (525824723 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a2d032d949a350fca05beb8a66e8387d7e95d55153b47169c374c5c5c97d650`
-	Entrypoint: `["\/usr\/local\/bin\/docker-entrypoint"]`

```dockerfile
# Thu, 16 Oct 2025 19:23:01 GMT
ARG RELEASE
# Thu, 16 Oct 2025 19:23:01 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 16 Oct 2025 19:23:01 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 16 Oct 2025 19:23:01 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 16 Oct 2025 19:23:03 GMT
ADD file:ddf1aa62235de6657123492b19d27d937c25668011b5ebf923a3f019200f8540 in / 
# Thu, 16 Oct 2025 19:23:03 GMT
CMD ["/bin/bash"]
# Thu, 13 Nov 2025 23:28:56 GMT
RUN for iter in {1..10}; do       export DEBIAN_FRONTEND=noninteractive &&     apt-get update -y &&   apt-get upgrade -y &&   apt-get install -y procps findutils tar gzip &&         apt-get install -y locales &&         apt-get install -y curl &&     apt-get clean all &&       locale-gen 'en_US.UTF-8' &&     apt-get clean metadata &&   exit_code=0 && break || exit_code=$? && echo "packaging error: retry $iter in 10s" && apt-get clean all &&   apt-get clean metadata && sleep 10; done; (exit $exit_code) # buildkit
# Thu, 13 Nov 2025 23:28:56 GMT
RUN userdel -r ubuntu && groupadd --gid 1000 logstash &&   useradd --uid 1000 --gid 1000 --home /usr/share/logstash --no-create-home logstash # buildkit
# Thu, 13 Nov 2025 23:29:37 GMT
RUN curl -Lo - https://artifacts.elastic.co/downloads/logstash/logstash-8.18.8-linux-$(arch).tar.gz |   tar zxf - -C /usr/share &&   mv /usr/share/logstash-8.18.8 /usr/share/logstash &&   chown --recursive logstash:logstash /usr/share/logstash/ &&   chown -R logstash:root /usr/share/logstash &&   chmod -R g=u /usr/share/logstash &&   mkdir /licenses/ &&   mv /usr/share/logstash/NOTICE.TXT /licenses/NOTICE.TXT &&   mv /usr/share/logstash/LICENSE.txt /licenses/LICENSE.txt &&   find /usr/share/logstash -type d -exec chmod g+s {} \; &&   ln -s /usr/share/logstash /opt/logstash # buildkit
# Thu, 13 Nov 2025 23:29:37 GMT
WORKDIR /usr/share/logstash
# Thu, 13 Nov 2025 23:29:37 GMT
ENV ELASTIC_CONTAINER=true
# Thu, 13 Nov 2025 23:29:37 GMT
ENV PATH=/usr/share/logstash/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 13 Nov 2025 23:29:37 GMT
COPY config/logstash-full.yml config/logstash.yml # buildkit
# Thu, 13 Nov 2025 23:29:37 GMT
COPY config/pipelines.yml config/log4j2.properties config/log4j2.file.properties config/ # buildkit
# Thu, 13 Nov 2025 23:29:37 GMT
COPY pipeline/default.conf pipeline/logstash.conf # buildkit
# Thu, 13 Nov 2025 23:29:37 GMT
RUN chown --recursive logstash:root config/ pipeline/ # buildkit
# Thu, 13 Nov 2025 23:29:37 GMT
ENV LANG=en_US.UTF-8 LC_ALL=en_US.UTF-8
# Thu, 13 Nov 2025 23:29:37 GMT
COPY env2yaml/env2yaml-amd64 env2yaml/env2yaml-arm64 env2yaml/ # buildkit
# Thu, 13 Nov 2025 23:29:38 GMT
RUN set -eux; env2yamlarch="$(dpkg --print-architecture)";   case "${env2yamlarch}" in     'x86_64'|'amd64')       env2yamlarch=amd64;       ;;     'aarch64'|'arm64')       env2yamlarch=arm64;       ;;     *) echo >&2 "error: unsupported architecture '$env2yamlarch'"; exit 1 ;;   esac;   mkdir -p /usr/local/bin;   cp env2yaml/env2yaml-${env2yamlarch} /usr/local/bin/env2yaml;   rm -rf env2yaml # buildkit
# Thu, 13 Nov 2025 23:29:38 GMT
COPY bin/docker-entrypoint /usr/local/bin/ # buildkit
# Thu, 13 Nov 2025 23:29:38 GMT
RUN chmod 0755 /usr/local/bin/docker-entrypoint # buildkit
# Thu, 13 Nov 2025 23:29:38 GMT
USER 1000
# Thu, 13 Nov 2025 23:29:38 GMT
EXPOSE map[5044/tcp:{} 9600/tcp:{}]
# Thu, 13 Nov 2025 23:29:38 GMT
LABEL org.label-schema.schema-version=1.0 org.label-schema.vendor=Elastic org.opencontainers.image.vendor=Elastic org.label-schema.name=logstash org.opencontainers.image.title=logstash org.label-schema.version=8.18.8 org.opencontainers.image.version=8.18.8 org.label-schema.url=https://www.elastic.co/products/logstash org.label-schema.vcs-url=https://github.com/elastic/logstash org.label-schema.license=Elastic License org.opencontainers.image.licenses=Elastic License org.opencontainers.image.description=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' org.label-schema.build-date=2025-09-30T19:02:11+00:00 org.opencontainers.image.created=2025-09-30T19:02:11+00:00
# Thu, 13 Nov 2025 23:29:38 GMT
ENTRYPOINT ["/usr/local/bin/docker-entrypoint"]
```

-	Layers:
	-	`sha256:20043066d3d5c78b45520c5707319835ac7d1f3d7f0dded0138ea0897d6a3188`  
		Last Modified: Mon, 15 Dec 2025 21:56:21 GMT  
		Size: 29.7 MB (29724688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7cdd79b80ccaa55c41f750c02665aedad9405ced41da54b49d0be9208fd2d5d6`  
		Last Modified: Thu, 13 Nov 2025 23:30:45 GMT  
		Size: 49.0 MB (49030452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:429834f6c7f98c2abc9f1c4742c85442daf5653762f7a26de93eb462bac346df`  
		Last Modified: Thu, 13 Nov 2025 23:30:36 GMT  
		Size: 1.2 KB (1224 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc1e8a17be130a7f1d7217bdb655fd8126de4f651453d3d6e89436d6d1d342b0`  
		Last Modified: Fri, 14 Nov 2025 02:26:54 GMT  
		Size: 441.0 MB (440981473 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3d1fa58ef233269bc32839e4f818d021168cb0c6e80e0200148f4c3cff15b0f`  
		Last Modified: Thu, 13 Nov 2025 23:30:36 GMT  
		Size: 278.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e30fbcc4fda19e49a762266e0e6faded74b019c5aabdb92f222341949c77a44c`  
		Last Modified: Thu, 13 Nov 2025 23:30:36 GMT  
		Size: 1.6 KB (1578 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b20a0b4ac67d42cb574f5eb946d234c5257b40c6b153f029dc385f75f6a8ce2a`  
		Last Modified: Thu, 13 Nov 2025 23:30:37 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:970c249e208f213784ac2ece9cea2b943c597c3cf702e90c5f37cb445217ed81`  
		Last Modified: Thu, 13 Nov 2025 23:30:37 GMT  
		Size: 1.8 KB (1769 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cdb233dac8d41e821577474435b7f1a1769b4bee17a2e45734d903c3eb6bcf0c`  
		Last Modified: Thu, 13 Nov 2025 23:30:41 GMT  
		Size: 4.0 MB (4004180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a382d3f5355e9be2f82d6625b36b3a8e72685cfcf41b1b116ca460e6b39b4efe`  
		Last Modified: Thu, 13 Nov 2025 23:30:37 GMT  
		Size: 2.1 MB (2078022 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:664a3632afa8063325511c3e4f4995f36e06390039e1a84893ebdd91e574e018`  
		Last Modified: Thu, 13 Nov 2025 23:30:36 GMT  
		Size: 713.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `logstash:8.18.8` - unknown; unknown

```console
$ docker pull logstash@sha256:2b0556efd6d5028087e0dcb7eaf140ae64c164864695dd5a4180bb4eb6872d07
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3692271 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ace81df77812ed20bb2a9d7277e0e88c0e1c9da9ee07e7bf541d544ece1077f`

```dockerfile
```

-	Layers:
	-	`sha256:e9a099deaf531ca02082a6f0b37812c340b9e4419acc44f046dcd834a9c26c2c`  
		Last Modified: Fri, 14 Nov 2025 01:53:26 GMT  
		Size: 3.7 MB (3657663 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d6d73e810d46eba1a1728c1b8064af55f67a3a2dc44d3da8cf9c8664068be48f`  
		Last Modified: Fri, 14 Nov 2025 01:53:26 GMT  
		Size: 34.6 KB (34608 bytes)  
		MIME: application/vnd.in-toto+json

### `logstash:8.18.8` - linux; arm64 variant v8

```console
$ docker pull logstash@sha256:eda3d8c0f02db1a48df7826ed5a096b0c5331594e5a6f67397e8c5a9614cc57e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **525.0 MB (524967182 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:32b14e7870f762fbe697e10861bb87bb433bb4d7176d2ea76762c64a6d2ad8fc`
-	Entrypoint: `["\/usr\/local\/bin\/docker-entrypoint"]`

```dockerfile
# Thu, 16 Oct 2025 19:26:52 GMT
ARG RELEASE
# Thu, 16 Oct 2025 19:26:52 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 16 Oct 2025 19:26:52 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 16 Oct 2025 19:26:52 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 16 Oct 2025 19:26:58 GMT
ADD file:44fdb45bd3a8d9bd9c66b716aa0bb6ee11b6fbcceb59ee0eb54165785a35dfcb in / 
# Thu, 16 Oct 2025 19:26:58 GMT
CMD ["/bin/bash"]
# Thu, 13 Nov 2025 23:28:31 GMT
RUN for iter in {1..10}; do       export DEBIAN_FRONTEND=noninteractive &&     apt-get update -y &&   apt-get upgrade -y &&   apt-get install -y procps findutils tar gzip &&         apt-get install -y locales &&         apt-get install -y curl &&     apt-get clean all &&       locale-gen 'en_US.UTF-8' &&     apt-get clean metadata &&   exit_code=0 && break || exit_code=$? && echo "packaging error: retry $iter in 10s" && apt-get clean all &&   apt-get clean metadata && sleep 10; done; (exit $exit_code) # buildkit
# Thu, 13 Nov 2025 23:28:31 GMT
RUN userdel -r ubuntu && groupadd --gid 1000 logstash &&   useradd --uid 1000 --gid 1000 --home /usr/share/logstash --no-create-home logstash # buildkit
# Thu, 13 Nov 2025 23:29:13 GMT
RUN curl -Lo - https://artifacts.elastic.co/downloads/logstash/logstash-8.18.8-linux-$(arch).tar.gz |   tar zxf - -C /usr/share &&   mv /usr/share/logstash-8.18.8 /usr/share/logstash &&   chown --recursive logstash:logstash /usr/share/logstash/ &&   chown -R logstash:root /usr/share/logstash &&   chmod -R g=u /usr/share/logstash &&   mkdir /licenses/ &&   mv /usr/share/logstash/NOTICE.TXT /licenses/NOTICE.TXT &&   mv /usr/share/logstash/LICENSE.txt /licenses/LICENSE.txt &&   find /usr/share/logstash -type d -exec chmod g+s {} \; &&   ln -s /usr/share/logstash /opt/logstash # buildkit
# Thu, 13 Nov 2025 23:29:14 GMT
WORKDIR /usr/share/logstash
# Thu, 13 Nov 2025 23:29:14 GMT
ENV ELASTIC_CONTAINER=true
# Thu, 13 Nov 2025 23:29:14 GMT
ENV PATH=/usr/share/logstash/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 13 Nov 2025 23:29:14 GMT
COPY config/logstash-full.yml config/logstash.yml # buildkit
# Thu, 13 Nov 2025 23:29:14 GMT
COPY config/pipelines.yml config/log4j2.properties config/log4j2.file.properties config/ # buildkit
# Thu, 13 Nov 2025 23:29:14 GMT
COPY pipeline/default.conf pipeline/logstash.conf # buildkit
# Thu, 13 Nov 2025 23:29:14 GMT
RUN chown --recursive logstash:root config/ pipeline/ # buildkit
# Thu, 13 Nov 2025 23:29:14 GMT
ENV LANG=en_US.UTF-8 LC_ALL=en_US.UTF-8
# Thu, 13 Nov 2025 23:29:14 GMT
COPY env2yaml/env2yaml-amd64 env2yaml/env2yaml-arm64 env2yaml/ # buildkit
# Thu, 13 Nov 2025 23:29:14 GMT
RUN set -eux; env2yamlarch="$(dpkg --print-architecture)";   case "${env2yamlarch}" in     'x86_64'|'amd64')       env2yamlarch=amd64;       ;;     'aarch64'|'arm64')       env2yamlarch=arm64;       ;;     *) echo >&2 "error: unsupported architecture '$env2yamlarch'"; exit 1 ;;   esac;   mkdir -p /usr/local/bin;   cp env2yaml/env2yaml-${env2yamlarch} /usr/local/bin/env2yaml;   rm -rf env2yaml # buildkit
# Thu, 13 Nov 2025 23:29:14 GMT
COPY bin/docker-entrypoint /usr/local/bin/ # buildkit
# Thu, 13 Nov 2025 23:29:14 GMT
RUN chmod 0755 /usr/local/bin/docker-entrypoint # buildkit
# Thu, 13 Nov 2025 23:29:14 GMT
USER 1000
# Thu, 13 Nov 2025 23:29:14 GMT
EXPOSE map[5044/tcp:{} 9600/tcp:{}]
# Thu, 13 Nov 2025 23:29:14 GMT
LABEL org.label-schema.schema-version=1.0 org.label-schema.vendor=Elastic org.opencontainers.image.vendor=Elastic org.label-schema.name=logstash org.opencontainers.image.title=logstash org.label-schema.version=8.18.8 org.opencontainers.image.version=8.18.8 org.label-schema.url=https://www.elastic.co/products/logstash org.label-schema.vcs-url=https://github.com/elastic/logstash org.label-schema.license=Elastic License org.opencontainers.image.licenses=Elastic License org.opencontainers.image.description=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' org.label-schema.build-date=2025-09-30T19:02:11+00:00 org.opencontainers.image.created=2025-09-30T19:02:11+00:00
# Thu, 13 Nov 2025 23:29:14 GMT
ENTRYPOINT ["/usr/local/bin/docker-entrypoint"]
```

-	Layers:
	-	`sha256:97dd3f0ce510a30a2868ff104e9ff286ffc0ef01284aebe383ea81e85e26a415`  
		Last Modified: Mon, 15 Dec 2025 21:56:39 GMT  
		Size: 28.9 MB (28861957 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7e2941a2ca4b19bbd5b2b6121b4d7ea76e18d66621a65bc2b69892a6695274a`  
		Last Modified: Thu, 13 Nov 2025 23:30:10 GMT  
		Size: 50.9 MB (50920587 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92811a7a0282e3c3ac478c27030a0833d205ecfa3722d637ff310259ff4c61cd`  
		Last Modified: Thu, 13 Nov 2025 23:30:07 GMT  
		Size: 1.2 KB (1222 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46880e8efe89d131f1fcef7fbbc1bac25b066a52c522510ea5a4d54905c43408`  
		Last Modified: Fri, 14 Nov 2025 02:27:30 GMT  
		Size: 439.2 MB (439248985 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30e816dbf151b745cf877898cf1f38eb5d1e9fdba9cb829677c7db3f51e2356a`  
		Last Modified: Thu, 13 Nov 2025 23:30:07 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6cd8b3a2856c46ef6c5fc08409f79704e1e152daf357e774a4112e9a0e6e3310`  
		Last Modified: Thu, 13 Nov 2025 23:30:07 GMT  
		Size: 1.6 KB (1579 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a38a53e225d75eff12773ef054757fc3c918925e9c6a254255a6abae89b9454d`  
		Last Modified: Thu, 13 Nov 2025 23:30:07 GMT  
		Size: 278.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0611631f79d04d18e50936612a7f2ed8941206427eb741095e883b9554d5abd9`  
		Last Modified: Thu, 13 Nov 2025 23:30:07 GMT  
		Size: 1.8 KB (1765 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef1c7deb1dda72ff0ea0be3b4ec4a75470d63cdc3b774dbbed0ce150ef7c8aa6`  
		Last Modified: Thu, 13 Nov 2025 23:30:07 GMT  
		Size: 4.0 MB (4004181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5769e7b7e10a84cb8c18514c4fb229e6085c41326be9344426201b72d03d95cb`  
		Last Modified: Thu, 13 Nov 2025 23:30:07 GMT  
		Size: 1.9 MB (1925573 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be7261f1bc119d985222300eb703ac17b3f85ef3be1d2b7c59548d52b1931610`  
		Last Modified: Thu, 13 Nov 2025 23:30:07 GMT  
		Size: 714.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `logstash:8.18.8` - unknown; unknown

```console
$ docker pull logstash@sha256:282ec9c8c443d33ce1d7b8ae801910caf07e84f50e12b7640d560cce877f10f5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3692840 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cbc02dbb43679cc9148cb7874de46881ffa09231366dd245364e0924316feaec`

```dockerfile
```

-	Layers:
	-	`sha256:eb2724933da0910479dfd0de4d69f32aaede2048f786924e0754d75f1a82048a`  
		Last Modified: Fri, 14 Nov 2025 01:53:31 GMT  
		Size: 3.7 MB (3658088 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1ff2be8520e57438521bdce72e162db54d896d0333fd5b8b4a3e65312794eb7f`  
		Last Modified: Fri, 14 Nov 2025 01:53:32 GMT  
		Size: 34.8 KB (34752 bytes)  
		MIME: application/vnd.in-toto+json

## `logstash:8.19.9`

```console
$ docker pull logstash@sha256:52ba04e22b34affd0d5fe6a2716139668e2d6f3c4099fb6aed15a2ee872eb4d9
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `logstash:8.19.9` - linux; amd64

```console
$ docker pull logstash@sha256:f2cd79e3a70b08bf97c56f951924cfd027893fe0b15049eec2ffa8d0ba3018f9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **523.3 MB (523296455 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b4761105ce4128a57d72b387f7fba06588c3aaaeac5322f1035e057b0f4354b3`
-	Entrypoint: `["\/usr\/local\/bin\/docker-entrypoint"]`

```dockerfile
# Thu, 16 Oct 2025 19:23:01 GMT
ARG RELEASE
# Thu, 16 Oct 2025 19:23:01 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 16 Oct 2025 19:23:01 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 16 Oct 2025 19:23:01 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 16 Oct 2025 19:23:03 GMT
ADD file:ddf1aa62235de6657123492b19d27d937c25668011b5ebf923a3f019200f8540 in / 
# Thu, 16 Oct 2025 19:23:03 GMT
CMD ["/bin/bash"]
# Thu, 18 Dec 2025 19:12:29 GMT
RUN for iter in {1..10}; do       export DEBIAN_FRONTEND=noninteractive &&     apt-get update -y &&   apt-get upgrade -y &&   apt-get install -y procps findutils tar gzip &&         apt-get install -y locales &&         apt-get install -y curl &&     apt-get clean all &&       locale-gen 'en_US.UTF-8' &&     apt-get clean metadata &&   exit_code=0 && break || exit_code=$? && echo "packaging error: retry $iter in 10s" && apt-get clean all &&   apt-get clean metadata && sleep 10; done; (exit $exit_code) # buildkit
# Thu, 18 Dec 2025 19:12:29 GMT
RUN userdel -r ubuntu && groupadd --gid 1000 logstash &&   useradd --uid 1000 --gid 1000 --home /usr/share/logstash --no-create-home logstash # buildkit
# Thu, 18 Dec 2025 19:12:51 GMT
RUN curl -Lo - https://artifacts.elastic.co/downloads/logstash/logstash-8.19.9-linux-$(arch).tar.gz |   tar zxf - -C /usr/share &&   mv /usr/share/logstash-8.19.9 /usr/share/logstash &&   chown --recursive logstash:logstash /usr/share/logstash/ &&   chown -R logstash:root /usr/share/logstash &&   chmod -R g=u /usr/share/logstash &&   mkdir /licenses/ &&   mv /usr/share/logstash/NOTICE.TXT /licenses/NOTICE.TXT &&   mv /usr/share/logstash/LICENSE.txt /licenses/LICENSE.txt &&   find /usr/share/logstash -type d -exec chmod g+s {} \; &&   ln -s /usr/share/logstash /opt/logstash # buildkit
# Thu, 18 Dec 2025 19:12:51 GMT
WORKDIR /usr/share/logstash
# Thu, 18 Dec 2025 19:12:51 GMT
ENV ELASTIC_CONTAINER=true
# Thu, 18 Dec 2025 19:12:51 GMT
ENV PATH=/usr/share/logstash/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 18 Dec 2025 19:12:51 GMT
COPY config/logstash-full.yml config/logstash.yml # buildkit
# Thu, 18 Dec 2025 19:12:51 GMT
COPY config/pipelines.yml config/log4j2.properties config/log4j2.file.properties config/ # buildkit
# Thu, 18 Dec 2025 19:12:51 GMT
COPY pipeline/default.conf pipeline/logstash.conf # buildkit
# Thu, 18 Dec 2025 19:12:51 GMT
RUN chown --recursive logstash:root config/ pipeline/ # buildkit
# Thu, 18 Dec 2025 19:12:51 GMT
ENV LANG=en_US.UTF-8 LC_ALL=en_US.UTF-8
# Thu, 18 Dec 2025 19:12:51 GMT
COPY --chown=logstash:root env2yaml/classes /usr/share/logstash/env2yaml/classes/ # buildkit
# Thu, 18 Dec 2025 19:12:52 GMT
COPY --chown=logstash:root env2yaml/lib /usr/share/logstash/env2yaml/lib/ # buildkit
# Thu, 18 Dec 2025 19:12:52 GMT
COPY --chmod=0755 env2yaml/env2yaml /usr/local/bin/env2yaml # buildkit
# Thu, 18 Dec 2025 19:12:52 GMT
COPY bin/docker-entrypoint /usr/local/bin/ # buildkit
# Thu, 18 Dec 2025 19:12:52 GMT
RUN chmod 0755 /usr/local/bin/docker-entrypoint # buildkit
# Thu, 18 Dec 2025 19:12:52 GMT
USER 1000
# Thu, 18 Dec 2025 19:12:52 GMT
EXPOSE map[5044/tcp:{} 9600/tcp:{}]
# Thu, 18 Dec 2025 19:12:52 GMT
LABEL org.label-schema.schema-version=1.0 org.label-schema.vendor=Elastic org.opencontainers.image.vendor=Elastic org.label-schema.name=logstash org.opencontainers.image.title=logstash org.label-schema.version=8.19.9 org.opencontainers.image.version=8.19.9 org.label-schema.url=https://www.elastic.co/products/logstash org.label-schema.vcs-url=https://github.com/elastic/logstash org.label-schema.license=Elastic License org.opencontainers.image.licenses=Elastic License org.opencontainers.image.description=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' org.label-schema.build-date=2025-12-10T14:22:40+00:00 org.opencontainers.image.created=2025-12-10T14:22:40+00:00
# Thu, 18 Dec 2025 19:12:52 GMT
ENTRYPOINT ["/usr/local/bin/docker-entrypoint"]
```

-	Layers:
	-	`sha256:20043066d3d5c78b45520c5707319835ac7d1f3d7f0dded0138ea0897d6a3188`  
		Last Modified: Mon, 15 Dec 2025 21:56:21 GMT  
		Size: 29.7 MB (29724688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:426e916f8d73b22744a0874a6c86352f6aa61de8889932e5e4604f86b78e87e2`  
		Last Modified: Thu, 18 Dec 2025 19:13:47 GMT  
		Size: 51.9 MB (51901993 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58e61a22492ec0ddfb5ad5f4473ab090fcbd65faaf995bab22dcd9e9c40ad245`  
		Last Modified: Thu, 18 Dec 2025 19:13:42 GMT  
		Size: 1.2 KB (1224 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96b57033250ab840200f7bf1f72a20b6170392722e89d39048db5034c3ac1d8c`  
		Last Modified: Thu, 18 Dec 2025 19:15:37 GMT  
		Size: 441.4 MB (441402039 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:596f828f2d4b5753206d35710a936bfb847aa2ef6d8877fec3a1f3ad87a14105`  
		Last Modified: Thu, 18 Dec 2025 19:13:42 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba839c01258ae558eb77b2332f168a475d002caffd98ac2353def7398af8b2c3`  
		Last Modified: Thu, 18 Dec 2025 19:13:42 GMT  
		Size: 1.6 KB (1578 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df73bad551b221c609be986e7b7330549df022690ca450c8ff9134b306fc5177`  
		Last Modified: Thu, 18 Dec 2025 19:13:42 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7359ad50f19f285d63b20dcd298bb43c5719fe6b9c017cc9934fa325afab142d`  
		Last Modified: Thu, 18 Dec 2025 19:13:42 GMT  
		Size: 1.8 KB (1766 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cab9af9919522f4b7b9231b0a70c49d9edef4cf28173f8bf681b82d30a5a1cd1`  
		Last Modified: Thu, 18 Dec 2025 19:13:42 GMT  
		Size: 6.3 KB (6295 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f12a8e52401b939a799f4b94f3087ff21824547cc0b29a71e084297906d63d7`  
		Last Modified: Thu, 18 Dec 2025 19:13:42 GMT  
		Size: 255.2 KB (255190 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:246034fa7936772abe0e6032828d64503b6a64b582ecee10ccf2bd3562d001e3`  
		Last Modified: Thu, 18 Dec 2025 19:13:42 GMT  
		Size: 353.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e72614c63db0fec10d412dccc9ec46b7fae5b693e0658e11f30a9a5156e6cf50`  
		Last Modified: Thu, 18 Dec 2025 19:13:42 GMT  
		Size: 713.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `logstash:8.19.9` - unknown; unknown

```console
$ docker pull logstash@sha256:b379847b9b98d787531904e2c286c12f04b08f8afc87636dcc9bd147eff8d356
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3687572 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cfd97e2b32c68065333f5373dc8bd67601b72ab041bd0d084e445a8e52894844`

```dockerfile
```

-	Layers:
	-	`sha256:f8bc821a0acb06b9e3ed57f9ef3ebb1fd6a1bb86a4b500c2cd45430f59b43c40`  
		Last Modified: Thu, 18 Dec 2025 19:53:28 GMT  
		Size: 3.7 MB (3651735 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bebeef9ed36934137c01461dc5829f98273e255c2a45a1f5b5044c0cd7a8feee`  
		Last Modified: Thu, 18 Dec 2025 19:53:29 GMT  
		Size: 35.8 KB (35837 bytes)  
		MIME: application/vnd.in-toto+json

### `logstash:8.19.9` - linux; arm64 variant v8

```console
$ docker pull logstash@sha256:895af57ec7a058234fd2d80802b3913de5963a3ec1bd0988f4b7faec46bcf097
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **523.0 MB (523012572 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b048c620ad2aa410e398146647a0a1d5fb3e6700e0bd920b7ad2dd2dceace93d`
-	Entrypoint: `["\/usr\/local\/bin\/docker-entrypoint"]`

```dockerfile
# Thu, 16 Oct 2025 19:26:52 GMT
ARG RELEASE
# Thu, 16 Oct 2025 19:26:52 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 16 Oct 2025 19:26:52 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 16 Oct 2025 19:26:52 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 16 Oct 2025 19:26:58 GMT
ADD file:44fdb45bd3a8d9bd9c66b716aa0bb6ee11b6fbcceb59ee0eb54165785a35dfcb in / 
# Thu, 16 Oct 2025 19:26:58 GMT
CMD ["/bin/bash"]
# Thu, 18 Dec 2025 19:11:40 GMT
RUN for iter in {1..10}; do       export DEBIAN_FRONTEND=noninteractive &&     apt-get update -y &&   apt-get upgrade -y &&   apt-get install -y procps findutils tar gzip &&         apt-get install -y locales &&         apt-get install -y curl &&     apt-get clean all &&       locale-gen 'en_US.UTF-8' &&     apt-get clean metadata &&   exit_code=0 && break || exit_code=$? && echo "packaging error: retry $iter in 10s" && apt-get clean all &&   apt-get clean metadata && sleep 10; done; (exit $exit_code) # buildkit
# Thu, 18 Dec 2025 19:11:40 GMT
RUN userdel -r ubuntu && groupadd --gid 1000 logstash &&   useradd --uid 1000 --gid 1000 --home /usr/share/logstash --no-create-home logstash # buildkit
# Thu, 18 Dec 2025 19:12:01 GMT
RUN curl -Lo - https://artifacts.elastic.co/downloads/logstash/logstash-8.19.9-linux-$(arch).tar.gz |   tar zxf - -C /usr/share &&   mv /usr/share/logstash-8.19.9 /usr/share/logstash &&   chown --recursive logstash:logstash /usr/share/logstash/ &&   chown -R logstash:root /usr/share/logstash &&   chmod -R g=u /usr/share/logstash &&   mkdir /licenses/ &&   mv /usr/share/logstash/NOTICE.TXT /licenses/NOTICE.TXT &&   mv /usr/share/logstash/LICENSE.txt /licenses/LICENSE.txt &&   find /usr/share/logstash -type d -exec chmod g+s {} \; &&   ln -s /usr/share/logstash /opt/logstash # buildkit
# Thu, 18 Dec 2025 19:12:01 GMT
WORKDIR /usr/share/logstash
# Thu, 18 Dec 2025 19:12:01 GMT
ENV ELASTIC_CONTAINER=true
# Thu, 18 Dec 2025 19:12:01 GMT
ENV PATH=/usr/share/logstash/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 18 Dec 2025 19:12:01 GMT
COPY config/logstash-full.yml config/logstash.yml # buildkit
# Thu, 18 Dec 2025 19:12:01 GMT
COPY config/pipelines.yml config/log4j2.properties config/log4j2.file.properties config/ # buildkit
# Thu, 18 Dec 2025 19:12:01 GMT
COPY pipeline/default.conf pipeline/logstash.conf # buildkit
# Thu, 18 Dec 2025 19:12:01 GMT
RUN chown --recursive logstash:root config/ pipeline/ # buildkit
# Thu, 18 Dec 2025 19:12:01 GMT
ENV LANG=en_US.UTF-8 LC_ALL=en_US.UTF-8
# Thu, 18 Dec 2025 19:12:01 GMT
COPY --chown=logstash:root env2yaml/classes /usr/share/logstash/env2yaml/classes/ # buildkit
# Thu, 18 Dec 2025 19:12:02 GMT
COPY --chown=logstash:root env2yaml/lib /usr/share/logstash/env2yaml/lib/ # buildkit
# Thu, 18 Dec 2025 19:12:02 GMT
COPY --chmod=0755 env2yaml/env2yaml /usr/local/bin/env2yaml # buildkit
# Thu, 18 Dec 2025 19:12:02 GMT
COPY bin/docker-entrypoint /usr/local/bin/ # buildkit
# Thu, 18 Dec 2025 19:12:02 GMT
RUN chmod 0755 /usr/local/bin/docker-entrypoint # buildkit
# Thu, 18 Dec 2025 19:12:02 GMT
USER 1000
# Thu, 18 Dec 2025 19:12:02 GMT
EXPOSE map[5044/tcp:{} 9600/tcp:{}]
# Thu, 18 Dec 2025 19:12:02 GMT
LABEL org.label-schema.schema-version=1.0 org.label-schema.vendor=Elastic org.opencontainers.image.vendor=Elastic org.label-schema.name=logstash org.opencontainers.image.title=logstash org.label-schema.version=8.19.9 org.opencontainers.image.version=8.19.9 org.label-schema.url=https://www.elastic.co/products/logstash org.label-schema.vcs-url=https://github.com/elastic/logstash org.label-schema.license=Elastic License org.opencontainers.image.licenses=Elastic License org.opencontainers.image.description=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' org.label-schema.build-date=2025-12-10T14:22:40+00:00 org.opencontainers.image.created=2025-12-10T14:22:40+00:00
# Thu, 18 Dec 2025 19:12:02 GMT
ENTRYPOINT ["/usr/local/bin/docker-entrypoint"]
```

-	Layers:
	-	`sha256:97dd3f0ce510a30a2868ff104e9ff286ffc0ef01284aebe383ea81e85e26a415`  
		Last Modified: Mon, 15 Dec 2025 21:56:39 GMT  
		Size: 28.9 MB (28861957 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:417aa4be65aac684047b6472d6f58fc45b8ef0f351f0116e84a6e98da2fff155`  
		Last Modified: Thu, 18 Dec 2025 19:13:01 GMT  
		Size: 54.2 MB (54189699 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4949fc94887c80d618a1140fc470acfff9bd91dc1aa2e700189266d9d7e30ef7`  
		Last Modified: Thu, 18 Dec 2025 19:12:56 GMT  
		Size: 1.2 KB (1224 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37607bf55db5d43b36f475be2b9fdeb3ec2a43dbc7e33e44e37de28274139bcc`  
		Last Modified: Thu, 18 Dec 2025 19:14:59 GMT  
		Size: 439.7 MB (439693160 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0b8dcc690a9026e797b018b7f4300ae53780d2cb870697aaf0e3c9116d6b068`  
		Last Modified: Thu, 18 Dec 2025 19:12:56 GMT  
		Size: 278.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf8202d10b09da31883e96ad5d4f467bca2eb79b42b5021d118c3ae8d74d5075`  
		Last Modified: Thu, 18 Dec 2025 19:12:56 GMT  
		Size: 1.6 KB (1581 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dadb978f069e8bd20a1edce4691b83cd49894f23f29d59dc0122aa9897adff41`  
		Last Modified: Thu, 18 Dec 2025 19:12:56 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db0f3b6328e86ed27ecf341fc30729098cd68a1a15bdf7bb91197ebceb62abf0`  
		Last Modified: Thu, 18 Dec 2025 19:12:56 GMT  
		Size: 1.8 KB (1764 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c61eb0f401ea3f59ab4f778e3c0684ff7ad294d05c2c62a401aabf77069a345c`  
		Last Modified: Thu, 18 Dec 2025 19:12:56 GMT  
		Size: 6.3 KB (6303 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90d6277faeef23c4bbbdeac4b99ec831587aae52efcb3a3ddd5a7187df5c8a83`  
		Last Modified: Thu, 18 Dec 2025 19:12:56 GMT  
		Size: 255.2 KB (255196 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aefb131b872b6348668348593f3088aeb140aa01f8c7d518583366f6f53ae3d0`  
		Last Modified: Thu, 18 Dec 2025 19:12:56 GMT  
		Size: 354.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1704eec8bf71e06db02a2910f167c1289d6e1275270eabb0ac61a55ec6d8a3f4`  
		Last Modified: Thu, 18 Dec 2025 19:12:56 GMT  
		Size: 713.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `logstash:8.19.9` - unknown; unknown

```console
$ docker pull logstash@sha256:6769e1d7ac24fbd4f3ebff2d546b51f3b6f3ac2aa327edabcf0bfd1d270c4359
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3688125 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a8513c1562f0d7b1e081996f2567ed9b99c4cb5d8e3e37e4d91f764d8c5a61f2`

```dockerfile
```

-	Layers:
	-	`sha256:3c06653fddcbd0909f44a4ba672a724a7e6c3a275ad673ea4e59f228bbb3bcc0`  
		Last Modified: Thu, 18 Dec 2025 19:53:34 GMT  
		Size: 3.7 MB (3652160 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b7b6c2199dde22e80f3ba725ed867af6c433a726067161034d061aa870b6d735`  
		Last Modified: Thu, 18 Dec 2025 19:53:35 GMT  
		Size: 36.0 KB (35965 bytes)  
		MIME: application/vnd.in-toto+json

## `logstash:9.1.9`

```console
$ docker pull logstash@sha256:64e681c72ef1268f9887fbaa0e426f54b5765c1dd14741a536c881401dd335df
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `logstash:9.1.9` - linux; amd64

```console
$ docker pull logstash@sha256:14ad85871b259ec265cbd0423116247afa00f5e288cad089310448116a0f7b22
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **475.8 MB (475800498 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5814d8c55276395d3987d701521f3ca30c9fc32e8f6b42205f2044dd5a036f43`
-	Entrypoint: `["\/usr\/local\/bin\/docker-entrypoint"]`

```dockerfile
# Wed, 03 Dec 2025 20:36:20 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 03 Dec 2025 20:36:20 GMT
LABEL vendor="Red Hat, Inc."
# Wed, 03 Dec 2025 20:36:20 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Wed, 03 Dec 2025 20:36:20 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.7"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Wed, 03 Dec 2025 20:36:20 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 03 Dec 2025 20:36:20 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Wed, 03 Dec 2025 20:36:20 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 03 Dec 2025 20:36:20 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 03 Dec 2025 20:36:20 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Wed, 03 Dec 2025 20:36:20 GMT
LABEL io.openshift.expose-services=""
# Wed, 03 Dec 2025 20:36:20 GMT
LABEL io.openshift.tags="minimal rhel9"
# Wed, 03 Dec 2025 20:36:20 GMT
ENV container oci
# Wed, 03 Dec 2025 20:36:21 GMT
COPY dir:be2a521f68bf56126048c385ab01382fd10aa537a578d817938c3b4ce9ee2ae8 in /      
# Wed, 03 Dec 2025 20:36:21 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Wed, 03 Dec 2025 20:36:21 GMT
CMD ["/bin/bash"]
# Wed, 03 Dec 2025 20:36:21 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /usr/share/buildinfo/content-sets.json      
# Wed, 03 Dec 2025 20:36:21 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /root/buildinfo/content_manifests/content-sets.json      
# Wed, 03 Dec 2025 20:36:21 GMT
COPY file:94153b6833d6f050d8e2572e9c332f16148f47aceac72aaf42af4d08feb01e61 in /usr/share/buildinfo/labels.json      
# Wed, 03 Dec 2025 20:36:21 GMT
COPY file:94153b6833d6f050d8e2572e9c332f16148f47aceac72aaf42af4d08feb01e61 in /root/buildinfo/labels.json      
# Wed, 03 Dec 2025 20:36:21 GMT
LABEL "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="1595c1bf15cd4327d529f330e61327764327397e" "org.opencontainers.image.revision"="1595c1bf15cd4327d529f330e61327764327397e" "build-date"="2025-12-03T20:36:05Z" "org.opencontainers.image.created"="2025-12-03T20:36:05Z" "release"="1764794109"org.opencontainers.image.revision=1595c1bf15cd4327d529f330e61327764327397e,org.opencontainers.image.created=2025-12-03T20:36:05Z
# Thu, 18 Dec 2025 19:13:44 GMT
ENV ELASTIC_CONTAINER=true
# Thu, 18 Dec 2025 19:13:44 GMT
ENV PATH=/usr/share/logstash/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 18 Dec 2025 19:13:44 GMT
ENV LANG=C.UTF-8 LC_ALL=C.UTF-8
# Thu, 18 Dec 2025 19:13:44 GMT
WORKDIR /usr/share
# Thu, 18 Dec 2025 19:13:46 GMT
RUN microdnf install -y procps findutils tar gzip &&   microdnf install -y openssl &&   microdnf install -y which shadow-utils &&   microdnf clean all # buildkit
# Thu, 18 Dec 2025 19:14:12 GMT
RUN groupadd --gid 1000 logstash &&   adduser --uid 1000 --gid 1000   --home "/usr/share/logstash"   --no-create-home   logstash &&   arch="$(rpm --query --queryformat='%{ARCH}' rpm)" &&   curl -f -Lo logstash.tar.gz https://artifacts.elastic.co/downloads/logstash/logstash-9.1.9-linux-${arch}.tar.gz &&   tar -zxf logstash.tar.gz -C /usr/share &&   rm logstash.tar.gz &&   mv /usr/share/logstash-9.1.9 /usr/share/logstash &&   chown -R logstash:root /usr/share/logstash &&   chmod -R g=u /usr/share/logstash &&   mkdir /licenses &&   mv /usr/share/logstash/NOTICE.TXT /licenses/NOTICE.TXT &&   mv /usr/share/logstash/LICENSE.txt /licenses/LICENSE.txt &&   find /usr/share/logstash -type d -exec chmod g+s {} \; &&   ln -s /usr/share/logstash /opt/logstash # buildkit
# Thu, 18 Dec 2025 19:14:12 GMT
COPY --chown=logstash:root env2yaml/classes /usr/share/logstash/env2yaml/classes/ # buildkit
# Thu, 18 Dec 2025 19:14:12 GMT
COPY --chown=logstash:root env2yaml/lib /usr/share/logstash/env2yaml/lib/ # buildkit
# Thu, 18 Dec 2025 19:14:12 GMT
COPY --chmod=0755 env2yaml/env2yaml /usr/local/bin/env2yaml # buildkit
# Thu, 18 Dec 2025 19:14:12 GMT
COPY --chown=logstash:root config/pipelines.yml config/log4j2.properties config/log4j2.file.properties /usr/share/logstash/config/ # buildkit
# Thu, 18 Dec 2025 19:14:12 GMT
COPY --chown=logstash:root config/logstash-full.yml /usr/share/logstash/config/logstash.yml # buildkit
# Thu, 18 Dec 2025 19:14:12 GMT
COPY --chown=logstash:root pipeline/default.conf /usr/share/logstash/pipeline/logstash.conf # buildkit
# Thu, 18 Dec 2025 19:14:13 GMT
COPY --chmod=0755 bin/docker-entrypoint /usr/local/bin/ # buildkit
# Thu, 18 Dec 2025 19:14:13 GMT
WORKDIR /usr/share/logstash
# Thu, 18 Dec 2025 19:14:13 GMT
USER 1000
# Thu, 18 Dec 2025 19:14:13 GMT
EXPOSE map[5044/tcp:{} 9600/tcp:{}]
# Thu, 18 Dec 2025 19:14:13 GMT
LABEL org.label-schema.build-date=2025-12-10T14:14:26+00:00 org.label-schema.license=Elastic License org.label-schema.name=logstash org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/logstash org.label-schema.vcs-url=https://github.com/elastic/logstash org.label-schema.vendor=Elastic org.label-schema.version=9.1.9 org.opencontainers.image.created=2025-12-10T14:14:26+00:00 org.opencontainers.image.description=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' org.opencontainers.image.licenses=Elastic License org.opencontainers.image.title=logstash org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=9.1.9 description=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' license=Elastic License maintainer=info@elastic.co name=logstash summary=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' vendor=Elastic
# Thu, 18 Dec 2025 19:14:13 GMT
ENTRYPOINT ["/usr/local/bin/docker-entrypoint"]
```

-	Layers:
	-	`sha256:46a9484471e55e0e501c08ff903616330af0505ba749ef70e8c87e103e07844a`  
		Last Modified: Wed, 03 Dec 2025 21:15:52 GMT  
		Size: 40.0 MB (40040759 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f678e1f5eaf4a0e64dc7442c04ed592d809d1450732f80120ffe4778fba2bdd`  
		Last Modified: Thu, 18 Dec 2025 19:15:03 GMT  
		Size: 5.2 MB (5153916 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07b78f7701687c6d9ec688bb3ea00319a718633158c06594b7ac49353085d5e0`  
		Last Modified: Thu, 18 Dec 2025 19:17:26 GMT  
		Size: 430.3 MB (430341085 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f20f6ab5307c21fc7d99b2bc0c335e65cc59ab25580c254411796eeddf65b3d1`  
		Last Modified: Thu, 18 Dec 2025 19:15:01 GMT  
		Size: 6.3 KB (6295 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd1f2438002219b603686e677c89c854198b7e2db341d3f8335c9e792f99cb7e`  
		Last Modified: Thu, 18 Dec 2025 19:15:01 GMT  
		Size: 255.2 KB (255184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d45b0918da2adbdde40ac3c473d1abf0800cd357bca6c8fab3580d3208985bd`  
		Last Modified: Thu, 18 Dec 2025 19:15:01 GMT  
		Size: 355.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:270109e9e0683e24c17bc0088f395c7d62a3f37aff2de7ba80774ea8945278c3`  
		Last Modified: Thu, 18 Dec 2025 19:15:01 GMT  
		Size: 1.6 KB (1576 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:555c6da61eb79f3deba03e799c0bec1d74fcacb5a6a3b34d326e679212d46800`  
		Last Modified: Thu, 18 Dec 2025 19:15:01 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:662eca799ede95e6b40e47c498b22495c795ea1bf26d7733c5dd7909e94d8670`  
		Last Modified: Thu, 18 Dec 2025 19:15:01 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2fcc42b7ba06ea42fefca42d7d41a312d55287034403b3f00b324a8c8e2930a8`  
		Last Modified: Thu, 18 Dec 2025 19:15:01 GMT  
		Size: 713.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `logstash:9.1.9` - unknown; unknown

```console
$ docker pull logstash@sha256:1f15ef54d0f7831b0d0a60a2aed34c78e5ecdbfba17bda142beb0fff79f6543e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2118674 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:025394487521df6d5f6507cecac8bad63c85c5a951e09639101f526fe0fb01b3`

```dockerfile
```

-	Layers:
	-	`sha256:72adc52977f55b0fceb4ad6ea033c065cec0a0fd155173b1d11e5995e7751ecb`  
		Last Modified: Thu, 18 Dec 2025 22:53:39 GMT  
		Size: 2.1 MB (2088522 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4a0c0780f6124e8f576d58d5f3f9311c0be718dfa0190e4e86b60889741f0346`  
		Last Modified: Thu, 18 Dec 2025 22:53:39 GMT  
		Size: 30.2 KB (30152 bytes)  
		MIME: application/vnd.in-toto+json

### `logstash:9.1.9` - linux; arm64 variant v8

```console
$ docker pull logstash@sha256:4eedb480793175b7cb7e27b30dd03e754abe4c3665087755308be475e1d7fc8d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **472.3 MB (472256957 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:481839005e15e4e02a0784d431f0c50e83dadfec69979d365cf693eb03f67a67`
-	Entrypoint: `["\/usr\/local\/bin\/docker-entrypoint"]`

```dockerfile
# Wed, 03 Dec 2025 20:39:01 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 03 Dec 2025 20:39:01 GMT
LABEL vendor="Red Hat, Inc."
# Wed, 03 Dec 2025 20:39:01 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Wed, 03 Dec 2025 20:39:01 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.7"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Wed, 03 Dec 2025 20:39:01 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 03 Dec 2025 20:39:01 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Wed, 03 Dec 2025 20:39:01 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 03 Dec 2025 20:39:01 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 03 Dec 2025 20:39:01 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Wed, 03 Dec 2025 20:39:01 GMT
LABEL io.openshift.expose-services=""
# Wed, 03 Dec 2025 20:39:01 GMT
LABEL io.openshift.tags="minimal rhel9"
# Wed, 03 Dec 2025 20:39:01 GMT
ENV container oci
# Wed, 03 Dec 2025 20:39:02 GMT
COPY dir:f4ea265792475a3d4d1f704e5646b6b392f1a575aee1ff63417d34e28530c8cb in /      
# Wed, 03 Dec 2025 20:39:02 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Wed, 03 Dec 2025 20:39:02 GMT
CMD ["/bin/bash"]
# Wed, 03 Dec 2025 20:39:02 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /usr/share/buildinfo/content-sets.json      
# Wed, 03 Dec 2025 20:39:02 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /root/buildinfo/content_manifests/content-sets.json      
# Wed, 03 Dec 2025 20:39:02 GMT
COPY file:cac453727cef4359ee0e696635ab5d4ce6ce1ac7334c1d943b8e8f2fb464f41f in /usr/share/buildinfo/labels.json      
# Wed, 03 Dec 2025 20:39:02 GMT
COPY file:cac453727cef4359ee0e696635ab5d4ce6ce1ac7334c1d943b8e8f2fb464f41f in /root/buildinfo/labels.json      
# Wed, 03 Dec 2025 20:39:03 GMT
LABEL "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="1595c1bf15cd4327d529f330e61327764327397e" "org.opencontainers.image.revision"="1595c1bf15cd4327d529f330e61327764327397e" "build-date"="2025-12-03T20:38:45Z" "org.opencontainers.image.created"="2025-12-03T20:38:45Z" "release"="1764794109"org.opencontainers.image.revision=1595c1bf15cd4327d529f330e61327764327397e,org.opencontainers.image.created=2025-12-03T20:38:45Z
# Thu, 18 Dec 2025 19:11:28 GMT
ENV ELASTIC_CONTAINER=true
# Thu, 18 Dec 2025 19:11:28 GMT
ENV PATH=/usr/share/logstash/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 18 Dec 2025 19:11:28 GMT
ENV LANG=C.UTF-8 LC_ALL=C.UTF-8
# Thu, 18 Dec 2025 19:11:28 GMT
WORKDIR /usr/share
# Thu, 18 Dec 2025 19:11:31 GMT
RUN microdnf install -y procps findutils tar gzip &&   microdnf install -y openssl &&   microdnf install -y which shadow-utils &&   microdnf clean all # buildkit
# Thu, 18 Dec 2025 19:13:18 GMT
RUN groupadd --gid 1000 logstash &&   adduser --uid 1000 --gid 1000   --home "/usr/share/logstash"   --no-create-home   logstash &&   arch="$(rpm --query --queryformat='%{ARCH}' rpm)" &&   curl -f -Lo logstash.tar.gz https://artifacts.elastic.co/downloads/logstash/logstash-9.1.9-linux-${arch}.tar.gz &&   tar -zxf logstash.tar.gz -C /usr/share &&   rm logstash.tar.gz &&   mv /usr/share/logstash-9.1.9 /usr/share/logstash &&   chown -R logstash:root /usr/share/logstash &&   chmod -R g=u /usr/share/logstash &&   mkdir /licenses &&   mv /usr/share/logstash/NOTICE.TXT /licenses/NOTICE.TXT &&   mv /usr/share/logstash/LICENSE.txt /licenses/LICENSE.txt &&   find /usr/share/logstash -type d -exec chmod g+s {} \; &&   ln -s /usr/share/logstash /opt/logstash # buildkit
# Thu, 18 Dec 2025 19:13:18 GMT
COPY --chown=logstash:root env2yaml/classes /usr/share/logstash/env2yaml/classes/ # buildkit
# Thu, 18 Dec 2025 19:13:18 GMT
COPY --chown=logstash:root env2yaml/lib /usr/share/logstash/env2yaml/lib/ # buildkit
# Thu, 18 Dec 2025 19:13:18 GMT
COPY --chmod=0755 env2yaml/env2yaml /usr/local/bin/env2yaml # buildkit
# Thu, 18 Dec 2025 19:13:19 GMT
COPY --chown=logstash:root config/pipelines.yml config/log4j2.properties config/log4j2.file.properties /usr/share/logstash/config/ # buildkit
# Thu, 18 Dec 2025 19:13:19 GMT
COPY --chown=logstash:root config/logstash-full.yml /usr/share/logstash/config/logstash.yml # buildkit
# Thu, 18 Dec 2025 19:13:19 GMT
COPY --chown=logstash:root pipeline/default.conf /usr/share/logstash/pipeline/logstash.conf # buildkit
# Thu, 18 Dec 2025 19:13:19 GMT
COPY --chmod=0755 bin/docker-entrypoint /usr/local/bin/ # buildkit
# Thu, 18 Dec 2025 19:13:19 GMT
WORKDIR /usr/share/logstash
# Thu, 18 Dec 2025 19:13:19 GMT
USER 1000
# Thu, 18 Dec 2025 19:13:19 GMT
EXPOSE map[5044/tcp:{} 9600/tcp:{}]
# Thu, 18 Dec 2025 19:13:19 GMT
LABEL org.label-schema.build-date=2025-12-10T14:14:26+00:00 org.label-schema.license=Elastic License org.label-schema.name=logstash org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/logstash org.label-schema.vcs-url=https://github.com/elastic/logstash org.label-schema.vendor=Elastic org.label-schema.version=9.1.9 org.opencontainers.image.created=2025-12-10T14:14:26+00:00 org.opencontainers.image.description=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' org.opencontainers.image.licenses=Elastic License org.opencontainers.image.title=logstash org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=9.1.9 description=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' license=Elastic License maintainer=info@elastic.co name=logstash summary=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' vendor=Elastic
# Thu, 18 Dec 2025 19:13:19 GMT
ENTRYPOINT ["/usr/local/bin/docker-entrypoint"]
```

-	Layers:
	-	`sha256:15f4b55884339bddb52ca0550d5b1208576ecf31649e067b468dc4e7b90745bd`  
		Last Modified: Wed, 03 Dec 2025 22:01:09 GMT  
		Size: 38.2 MB (38222823 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7344c4d4940b5296f08ad80321ddcb7c9c8490b4571145650974131952000fb9`  
		Last Modified: Thu, 18 Dec 2025 19:12:51 GMT  
		Size: 5.2 MB (5153580 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1081b79176576965124221d290a3529fce6fc203ccdd8107b18b7a9d188fe64c`  
		Last Modified: Thu, 18 Dec 2025 19:16:45 GMT  
		Size: 428.6 MB (428615807 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0cad10838c656ab1675afbce30c07b52af72483aff2289501ba7eb28eb25443`  
		Last Modified: Thu, 18 Dec 2025 19:14:11 GMT  
		Size: 6.3 KB (6297 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04e3d42ba9196a09477343bf519aad5eec74471f9608c29cd26383036ca2d639`  
		Last Modified: Thu, 18 Dec 2025 19:14:12 GMT  
		Size: 255.2 KB (255185 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e14a2e2163d2a6d8356fec5f3f1ec4bb5963fbb926074be8414b2efac25fc129`  
		Last Modified: Thu, 18 Dec 2025 19:14:12 GMT  
		Size: 355.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eaf20d6dbea5cb35ce41e3bb3d598c8cc4d8e7aa9baf0ab869cfcc43d919773f`  
		Last Modified: Thu, 18 Dec 2025 19:14:12 GMT  
		Size: 1.6 KB (1578 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a89113aa396407f81c008a1e4737be7bd78141cdb1f8c8bd8aba1c49acbbbf1e`  
		Last Modified: Thu, 18 Dec 2025 19:14:12 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df5d65cda0ba861e4104cdc4b8f99ebdac2847f34cfe128f0886e8852e3ed7c6`  
		Last Modified: Thu, 18 Dec 2025 19:14:12 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e171d2c2fba3b2fae9cfcc257d7be4bde67b829ad7bb00245a639ab61ed7b340`  
		Last Modified: Thu, 18 Dec 2025 19:14:11 GMT  
		Size: 712.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `logstash:9.1.9` - unknown; unknown

```console
$ docker pull logstash@sha256:09ecc4454c2106e61b76abac651f02ca6b3dc21b90afd14e3af04543b442b6a8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2119321 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c246b68fdd153218ac558ceb739f42ca06109afc4cac95685f736770fe3f4c51`

```dockerfile
```

-	Layers:
	-	`sha256:ce0e25d89f43b2adfec6c125d128dff66c66fbea8410f05512cf0a0c96ba9c8c`  
		Last Modified: Thu, 18 Dec 2025 19:53:30 GMT  
		Size: 2.1 MB (2089092 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:eae745a34f93af12c5c1fe810db9c939d2c83d3a5b1112657b05af759bc6afa5`  
		Last Modified: Thu, 18 Dec 2025 19:53:31 GMT  
		Size: 30.2 KB (30229 bytes)  
		MIME: application/vnd.in-toto+json

## `logstash:9.2.3`

```console
$ docker pull logstash@sha256:b05058936f8aeb1edae3c48486f412aa5d53d0116d47e4be6e2eec992cb122ff
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `logstash:9.2.3` - linux; amd64

```console
$ docker pull logstash@sha256:d2e8549aa9bb61d4e3916d3e3bfb03610ca7d3c2cb1097b5d7133b10564719ac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **486.1 MB (486107731 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:08fa31ea596f91d2fa1167e876d0eb1e99dc25137601ecc3f8b0c94e0e43976b`
-	Entrypoint: `["\/usr\/local\/bin\/docker-entrypoint"]`

```dockerfile
# Wed, 03 Dec 2025 20:36:20 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 03 Dec 2025 20:36:20 GMT
LABEL vendor="Red Hat, Inc."
# Wed, 03 Dec 2025 20:36:20 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Wed, 03 Dec 2025 20:36:20 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.7"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Wed, 03 Dec 2025 20:36:20 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 03 Dec 2025 20:36:20 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Wed, 03 Dec 2025 20:36:20 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 03 Dec 2025 20:36:20 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 03 Dec 2025 20:36:20 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Wed, 03 Dec 2025 20:36:20 GMT
LABEL io.openshift.expose-services=""
# Wed, 03 Dec 2025 20:36:20 GMT
LABEL io.openshift.tags="minimal rhel9"
# Wed, 03 Dec 2025 20:36:20 GMT
ENV container oci
# Wed, 03 Dec 2025 20:36:21 GMT
COPY dir:be2a521f68bf56126048c385ab01382fd10aa537a578d817938c3b4ce9ee2ae8 in /      
# Wed, 03 Dec 2025 20:36:21 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Wed, 03 Dec 2025 20:36:21 GMT
CMD ["/bin/bash"]
# Wed, 03 Dec 2025 20:36:21 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /usr/share/buildinfo/content-sets.json      
# Wed, 03 Dec 2025 20:36:21 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /root/buildinfo/content_manifests/content-sets.json      
# Wed, 03 Dec 2025 20:36:21 GMT
COPY file:94153b6833d6f050d8e2572e9c332f16148f47aceac72aaf42af4d08feb01e61 in /usr/share/buildinfo/labels.json      
# Wed, 03 Dec 2025 20:36:21 GMT
COPY file:94153b6833d6f050d8e2572e9c332f16148f47aceac72aaf42af4d08feb01e61 in /root/buildinfo/labels.json      
# Wed, 03 Dec 2025 20:36:21 GMT
LABEL "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="1595c1bf15cd4327d529f330e61327764327397e" "org.opencontainers.image.revision"="1595c1bf15cd4327d529f330e61327764327397e" "build-date"="2025-12-03T20:36:05Z" "org.opencontainers.image.created"="2025-12-03T20:36:05Z" "release"="1764794109"org.opencontainers.image.revision=1595c1bf15cd4327d529f330e61327764327397e,org.opencontainers.image.created=2025-12-03T20:36:05Z
# Thu, 18 Dec 2025 19:12:02 GMT
ENV ELASTIC_CONTAINER=true
# Thu, 18 Dec 2025 19:12:02 GMT
ENV PATH=/usr/share/logstash/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 18 Dec 2025 19:12:02 GMT
ENV LANG=C.UTF-8 LC_ALL=C.UTF-8
# Thu, 18 Dec 2025 19:12:02 GMT
WORKDIR /usr/share
# Thu, 18 Dec 2025 19:12:04 GMT
RUN microdnf install -y procps findutils tar gzip &&   microdnf install -y openssl &&   microdnf install -y which shadow-utils &&   microdnf clean all # buildkit
# Thu, 18 Dec 2025 19:12:54 GMT
RUN groupadd --gid 1000 logstash &&   adduser --uid 1000 --gid 1000   --home "/usr/share/logstash"   --no-create-home   logstash &&   arch="$(rpm --query --queryformat='%{ARCH}' rpm)" &&   curl --fail --location --output logstash.tar.gz https://artifacts.elastic.co/downloads/logstash/logstash-9.2.3-linux-${arch}.tar.gz &&   tar -zxf logstash.tar.gz -C /usr/share &&   rm logstash.tar.gz &&   mv /usr/share/logstash-9.2.3 /usr/share/logstash &&   chown -R logstash:root /usr/share/logstash &&   chmod -R g=u /usr/share/logstash &&   mkdir /licenses &&   mv /usr/share/logstash/NOTICE.TXT /licenses/NOTICE.TXT &&   mv /usr/share/logstash/LICENSE.txt /licenses/LICENSE.txt &&   find /usr/share/logstash -type d -exec chmod g+s {} \; &&   ln -s /usr/share/logstash /opt/logstash # buildkit
# Thu, 18 Dec 2025 19:12:54 GMT
COPY --chown=logstash:root env2yaml/classes /usr/share/logstash/env2yaml/classes/ # buildkit
# Thu, 18 Dec 2025 19:12:54 GMT
COPY --chown=logstash:root env2yaml/lib /usr/share/logstash/env2yaml/lib/ # buildkit
# Thu, 18 Dec 2025 19:12:54 GMT
COPY --chmod=0755 env2yaml/env2yaml /usr/local/bin/env2yaml # buildkit
# Thu, 18 Dec 2025 19:12:54 GMT
COPY --chown=logstash:root config/pipelines.yml config/log4j2.properties config/log4j2.file.properties /usr/share/logstash/config/ # buildkit
# Thu, 18 Dec 2025 19:12:54 GMT
COPY --chown=logstash:root config/logstash-full.yml /usr/share/logstash/config/logstash.yml # buildkit
# Thu, 18 Dec 2025 19:12:54 GMT
COPY --chown=logstash:root pipeline/default.conf /usr/share/logstash/pipeline/logstash.conf # buildkit
# Thu, 18 Dec 2025 19:12:54 GMT
COPY --chmod=0755 bin/docker-entrypoint /usr/local/bin/ # buildkit
# Thu, 18 Dec 2025 19:12:54 GMT
WORKDIR /usr/share/logstash
# Thu, 18 Dec 2025 19:12:54 GMT
USER 1000
# Thu, 18 Dec 2025 19:12:54 GMT
EXPOSE map[5044/tcp:{} 9600/tcp:{}]
# Thu, 18 Dec 2025 19:12:54 GMT
LABEL org.label-schema.build-date=2025-12-10T14:15:16+00:00 org.label-schema.license=Elastic License org.label-schema.name=logstash org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/logstash org.label-schema.vcs-url=https://github.com/elastic/logstash org.label-schema.vendor=Elastic org.label-schema.version=9.2.3 org.opencontainers.image.created=2025-12-10T14:15:16+00:00 org.opencontainers.image.description=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' org.opencontainers.image.licenses=Elastic License org.opencontainers.image.title=logstash org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=9.2.3 description=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' license=Elastic License maintainer=info@elastic.co name=logstash summary=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' vendor=Elastic
# Thu, 18 Dec 2025 19:12:54 GMT
ENTRYPOINT ["/usr/local/bin/docker-entrypoint"]
```

-	Layers:
	-	`sha256:46a9484471e55e0e501c08ff903616330af0505ba749ef70e8c87e103e07844a`  
		Last Modified: Wed, 03 Dec 2025 21:15:52 GMT  
		Size: 40.0 MB (40040759 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d30da03df0b8583e0a5af36437a06f3e60e0c6365bab59a2129156c4813e4f9`  
		Last Modified: Thu, 18 Dec 2025 19:13:45 GMT  
		Size: 5.2 MB (5153949 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6844bcaf619ac8558b293d72599af5fd1721990001af3a83d70288227191f1ff`  
		Last Modified: Thu, 18 Dec 2025 19:15:36 GMT  
		Size: 440.6 MB (440648287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a041852c801de9ab19bf868b05193f490ba6a10c79595a7042031206f06f0c3`  
		Last Modified: Thu, 18 Dec 2025 19:13:42 GMT  
		Size: 6.3 KB (6297 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f76dc560e75025809b472e13b2cac34db9abfb841788088d3c2ca90a4ccc3d19`  
		Last Modified: Thu, 18 Dec 2025 19:13:42 GMT  
		Size: 255.2 KB (255184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54bd5ea23543130bd5d79e0d68416ef0c3798a499820cf8f96af7a1a92daff42`  
		Last Modified: Thu, 18 Dec 2025 19:13:41 GMT  
		Size: 352.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83ea5a6b0f2f267c381d2f229fcda6b0bd5e5b408922738f10e27600e31df4ae`  
		Last Modified: Thu, 18 Dec 2025 19:13:41 GMT  
		Size: 1.6 KB (1575 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ba7191fc6bc1c6362e54a61cbd68ee6f4495c60a8510f665949e4540277e6e3`  
		Last Modified: Thu, 18 Dec 2025 19:13:43 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a7f5fb3da5bd91419b86be5ec9dd979eca82eb0af080a9f8df62ba11bc7a4fd`  
		Last Modified: Thu, 18 Dec 2025 19:13:42 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9efed2aabf1089fbc2978a12a953844dd2faa9be117972c99e9711bf580f4859`  
		Last Modified: Thu, 18 Dec 2025 19:13:42 GMT  
		Size: 712.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `logstash:9.2.3` - unknown; unknown

```console
$ docker pull logstash@sha256:3dc90804b2929a6db22307cf3589e0af76ff5328de8246a1d27c664cf48ef725
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2128542 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7eae952b01da00167e07898d772863ae224676f7c7965c639d070324f6c8b603`

```dockerfile
```

-	Layers:
	-	`sha256:ae3017c815ac761aff3ddaad1715bc687ae367ca8de67c5bf180aa20fb02d104`  
		Last Modified: Thu, 18 Dec 2025 19:53:39 GMT  
		Size: 2.1 MB (2098342 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e3b8ecaa4ddee6afd0f0d3bbe09f4b422d9256726f1406fd5b685bf85d7161c8`  
		Last Modified: Thu, 18 Dec 2025 19:53:40 GMT  
		Size: 30.2 KB (30200 bytes)  
		MIME: application/vnd.in-toto+json

### `logstash:9.2.3` - linux; arm64 variant v8

```console
$ docker pull logstash@sha256:d8bb46b4063704b266220bb4c0caa110a8e854092b86df043755318a10e7e834
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **482.6 MB (482558146 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0808bcc5f54f846375246eee21ebfc5e746afc3719eed77a3cca8392d72082ad`
-	Entrypoint: `["\/usr\/local\/bin\/docker-entrypoint"]`

```dockerfile
# Wed, 03 Dec 2025 20:39:01 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 03 Dec 2025 20:39:01 GMT
LABEL vendor="Red Hat, Inc."
# Wed, 03 Dec 2025 20:39:01 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Wed, 03 Dec 2025 20:39:01 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.7"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Wed, 03 Dec 2025 20:39:01 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 03 Dec 2025 20:39:01 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Wed, 03 Dec 2025 20:39:01 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 03 Dec 2025 20:39:01 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 03 Dec 2025 20:39:01 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Wed, 03 Dec 2025 20:39:01 GMT
LABEL io.openshift.expose-services=""
# Wed, 03 Dec 2025 20:39:01 GMT
LABEL io.openshift.tags="minimal rhel9"
# Wed, 03 Dec 2025 20:39:01 GMT
ENV container oci
# Wed, 03 Dec 2025 20:39:02 GMT
COPY dir:f4ea265792475a3d4d1f704e5646b6b392f1a575aee1ff63417d34e28530c8cb in /      
# Wed, 03 Dec 2025 20:39:02 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Wed, 03 Dec 2025 20:39:02 GMT
CMD ["/bin/bash"]
# Wed, 03 Dec 2025 20:39:02 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /usr/share/buildinfo/content-sets.json      
# Wed, 03 Dec 2025 20:39:02 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /root/buildinfo/content_manifests/content-sets.json      
# Wed, 03 Dec 2025 20:39:02 GMT
COPY file:cac453727cef4359ee0e696635ab5d4ce6ce1ac7334c1d943b8e8f2fb464f41f in /usr/share/buildinfo/labels.json      
# Wed, 03 Dec 2025 20:39:02 GMT
COPY file:cac453727cef4359ee0e696635ab5d4ce6ce1ac7334c1d943b8e8f2fb464f41f in /root/buildinfo/labels.json      
# Wed, 03 Dec 2025 20:39:03 GMT
LABEL "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="1595c1bf15cd4327d529f330e61327764327397e" "org.opencontainers.image.revision"="1595c1bf15cd4327d529f330e61327764327397e" "build-date"="2025-12-03T20:38:45Z" "org.opencontainers.image.created"="2025-12-03T20:38:45Z" "release"="1764794109"org.opencontainers.image.revision=1595c1bf15cd4327d529f330e61327764327397e,org.opencontainers.image.created=2025-12-03T20:38:45Z
# Thu, 18 Dec 2025 19:11:28 GMT
ENV ELASTIC_CONTAINER=true
# Thu, 18 Dec 2025 19:11:28 GMT
ENV PATH=/usr/share/logstash/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 18 Dec 2025 19:11:28 GMT
ENV LANG=C.UTF-8 LC_ALL=C.UTF-8
# Thu, 18 Dec 2025 19:11:28 GMT
WORKDIR /usr/share
# Thu, 18 Dec 2025 19:11:31 GMT
RUN microdnf install -y procps findutils tar gzip &&   microdnf install -y openssl &&   microdnf install -y which shadow-utils &&   microdnf clean all # buildkit
# Thu, 18 Dec 2025 19:11:58 GMT
RUN groupadd --gid 1000 logstash &&   adduser --uid 1000 --gid 1000   --home "/usr/share/logstash"   --no-create-home   logstash &&   arch="$(rpm --query --queryformat='%{ARCH}' rpm)" &&   curl --fail --location --output logstash.tar.gz https://artifacts.elastic.co/downloads/logstash/logstash-9.2.3-linux-${arch}.tar.gz &&   tar -zxf logstash.tar.gz -C /usr/share &&   rm logstash.tar.gz &&   mv /usr/share/logstash-9.2.3 /usr/share/logstash &&   chown -R logstash:root /usr/share/logstash &&   chmod -R g=u /usr/share/logstash &&   mkdir /licenses &&   mv /usr/share/logstash/NOTICE.TXT /licenses/NOTICE.TXT &&   mv /usr/share/logstash/LICENSE.txt /licenses/LICENSE.txt &&   find /usr/share/logstash -type d -exec chmod g+s {} \; &&   ln -s /usr/share/logstash /opt/logstash # buildkit
# Thu, 18 Dec 2025 19:11:58 GMT
COPY --chown=logstash:root env2yaml/classes /usr/share/logstash/env2yaml/classes/ # buildkit
# Thu, 18 Dec 2025 19:11:58 GMT
COPY --chown=logstash:root env2yaml/lib /usr/share/logstash/env2yaml/lib/ # buildkit
# Thu, 18 Dec 2025 19:11:58 GMT
COPY --chmod=0755 env2yaml/env2yaml /usr/local/bin/env2yaml # buildkit
# Thu, 18 Dec 2025 19:11:58 GMT
COPY --chown=logstash:root config/pipelines.yml config/log4j2.properties config/log4j2.file.properties /usr/share/logstash/config/ # buildkit
# Thu, 18 Dec 2025 19:11:59 GMT
COPY --chown=logstash:root config/logstash-full.yml /usr/share/logstash/config/logstash.yml # buildkit
# Thu, 18 Dec 2025 19:11:59 GMT
COPY --chown=logstash:root pipeline/default.conf /usr/share/logstash/pipeline/logstash.conf # buildkit
# Thu, 18 Dec 2025 19:11:59 GMT
COPY --chmod=0755 bin/docker-entrypoint /usr/local/bin/ # buildkit
# Thu, 18 Dec 2025 19:11:59 GMT
WORKDIR /usr/share/logstash
# Thu, 18 Dec 2025 19:11:59 GMT
USER 1000
# Thu, 18 Dec 2025 19:11:59 GMT
EXPOSE map[5044/tcp:{} 9600/tcp:{}]
# Thu, 18 Dec 2025 19:11:59 GMT
LABEL org.label-schema.build-date=2025-12-10T14:15:16+00:00 org.label-schema.license=Elastic License org.label-schema.name=logstash org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/logstash org.label-schema.vcs-url=https://github.com/elastic/logstash org.label-schema.vendor=Elastic org.label-schema.version=9.2.3 org.opencontainers.image.created=2025-12-10T14:15:16+00:00 org.opencontainers.image.description=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' org.opencontainers.image.licenses=Elastic License org.opencontainers.image.title=logstash org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=9.2.3 description=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' license=Elastic License maintainer=info@elastic.co name=logstash summary=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' vendor=Elastic
# Thu, 18 Dec 2025 19:11:59 GMT
ENTRYPOINT ["/usr/local/bin/docker-entrypoint"]
```

-	Layers:
	-	`sha256:15f4b55884339bddb52ca0550d5b1208576ecf31649e067b468dc4e7b90745bd`  
		Last Modified: Wed, 03 Dec 2025 22:01:09 GMT  
		Size: 38.2 MB (38222823 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7344c4d4940b5296f08ad80321ddcb7c9c8490b4571145650974131952000fb9`  
		Last Modified: Thu, 18 Dec 2025 19:12:51 GMT  
		Size: 5.2 MB (5153580 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d4346b96f73d5d78434a9e671052a20e4d0e3aafd3c3ab8e56699aac5cc23c4`  
		Last Modified: Thu, 18 Dec 2025 19:13:43 GMT  
		Size: 438.9 MB (438917011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f71d6d64a6d211ae0eaf94bdc0c786fe51a464c2a08e363796208772431bc12`  
		Last Modified: Thu, 18 Dec 2025 19:12:50 GMT  
		Size: 6.3 KB (6293 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37ce6f1916725d1eda75fdb795db557853f4b8d071655ef92e21ca3498addbf4`  
		Last Modified: Thu, 18 Dec 2025 19:12:52 GMT  
		Size: 255.2 KB (255180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a8f0efb559ede0e225c82c00d8f6ab8ae96df2b3d404c5ddd34de1cca7fcfee`  
		Last Modified: Thu, 18 Dec 2025 19:12:50 GMT  
		Size: 354.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d8d3e2857969af1c3c168264282256225931c30d36b7a5d2d1cce1dfa1e9cad`  
		Last Modified: Thu, 18 Dec 2025 19:12:51 GMT  
		Size: 1.6 KB (1575 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ac2c91ff373313c4c73ab25ccb9dc68553bfe2035494b3a2b69968c0f69aa2d`  
		Last Modified: Thu, 18 Dec 2025 19:12:50 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd411316c501d7d87488276663577d30a112d868da6374253eb9ce7f9e3a5fc2`  
		Last Modified: Thu, 18 Dec 2025 19:12:51 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8725309dca8d67532b46f66f6dc1714229a851e98f6a48d4db1428e51fa64a9e`  
		Last Modified: Thu, 18 Dec 2025 19:12:51 GMT  
		Size: 712.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `logstash:9.2.3` - unknown; unknown

```console
$ docker pull logstash@sha256:049340a74f3c91ba7e3fb69a7862fe1e25092418dc8a4c0ebbd929eb30e1c60b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2129189 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fcb4f49fc314ed0db5fb8e71a57555f06c45447ced494c5519c39360527d09b6`

```dockerfile
```

-	Layers:
	-	`sha256:91c97c21d6d00fab49b6adb0b1d2c58b3c75f9e85fd42b5393441ee3d255165f`  
		Last Modified: Thu, 18 Dec 2025 19:53:44 GMT  
		Size: 2.1 MB (2098912 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b37c4cdefbdb86e8fb3b811d0f955fb8e4203dc88cfa08d2420cf2370ab5278f`  
		Last Modified: Thu, 18 Dec 2025 19:53:44 GMT  
		Size: 30.3 KB (30277 bytes)  
		MIME: application/vnd.in-toto+json
