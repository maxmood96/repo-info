<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `logstash`

-	[`logstash:8.18.8`](#logstash8188)
-	[`logstash:8.19.7`](#logstash8197)
-	[`logstash:9.1.7`](#logstash917)
-	[`logstash:9.2.1`](#logstash921)

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
		Last Modified: Thu, 16 Oct 2025 21:15:22 GMT  
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
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
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
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
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
		Last Modified: Thu, 16 Oct 2025 21:17:48 GMT  
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
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
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
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
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

## `logstash:8.19.7`

```console
$ docker pull logstash@sha256:49df884c1068983a34af7bc31a1f81ab4279bcffbab698e201e8a46a7210590b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `logstash:8.19.7` - linux; amd64

```console
$ docker pull logstash@sha256:2a4b36a326068588554f600a96d0a98ab9c26b88ec0273024dd103af9bc69ffa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **526.2 MB (526243157 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e594605f93ea9784545a63eeb0cdd575f7af3fa5ab56f9a388ae431b1387a043`
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
# Thu, 13 Nov 2025 23:28:58 GMT
RUN for iter in {1..10}; do       export DEBIAN_FRONTEND=noninteractive &&     apt-get update -y &&   apt-get upgrade -y &&   apt-get install -y procps findutils tar gzip &&         apt-get install -y locales &&         apt-get install -y curl &&     apt-get clean all &&       locale-gen 'en_US.UTF-8' &&     apt-get clean metadata &&   exit_code=0 && break || exit_code=$? && echo "packaging error: retry $iter in 10s" && apt-get clean all &&   apt-get clean metadata && sleep 10; done; (exit $exit_code) # buildkit
# Thu, 13 Nov 2025 23:28:59 GMT
RUN userdel -r ubuntu && groupadd --gid 1000 logstash &&   useradd --uid 1000 --gid 1000 --home /usr/share/logstash --no-create-home logstash # buildkit
# Thu, 13 Nov 2025 23:29:38 GMT
RUN curl -Lo - https://artifacts.elastic.co/downloads/logstash/logstash-8.19.7-linux-$(arch).tar.gz |   tar zxf - -C /usr/share &&   mv /usr/share/logstash-8.19.7 /usr/share/logstash &&   chown --recursive logstash:logstash /usr/share/logstash/ &&   chown -R logstash:root /usr/share/logstash &&   chmod -R g=u /usr/share/logstash &&   mkdir /licenses/ &&   mv /usr/share/logstash/NOTICE.TXT /licenses/NOTICE.TXT &&   mv /usr/share/logstash/LICENSE.txt /licenses/LICENSE.txt &&   find /usr/share/logstash -type d -exec chmod g+s {} \; &&   ln -s /usr/share/logstash /opt/logstash # buildkit
# Thu, 13 Nov 2025 23:29:38 GMT
WORKDIR /usr/share/logstash
# Thu, 13 Nov 2025 23:29:38 GMT
ENV ELASTIC_CONTAINER=true
# Thu, 13 Nov 2025 23:29:38 GMT
ENV PATH=/usr/share/logstash/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 13 Nov 2025 23:29:38 GMT
COPY config/logstash-full.yml config/logstash.yml # buildkit
# Thu, 13 Nov 2025 23:29:38 GMT
COPY config/pipelines.yml config/log4j2.properties config/log4j2.file.properties config/ # buildkit
# Thu, 13 Nov 2025 23:29:38 GMT
COPY pipeline/default.conf pipeline/logstash.conf # buildkit
# Thu, 13 Nov 2025 23:29:38 GMT
RUN chown --recursive logstash:root config/ pipeline/ # buildkit
# Thu, 13 Nov 2025 23:29:38 GMT
ENV LANG=en_US.UTF-8 LC_ALL=en_US.UTF-8
# Thu, 13 Nov 2025 23:29:39 GMT
COPY env2yaml/env2yaml-amd64 env2yaml/env2yaml-arm64 env2yaml/ # buildkit
# Thu, 13 Nov 2025 23:29:39 GMT
RUN set -eux; env2yamlarch="$(dpkg --print-architecture)";   case "${env2yamlarch}" in     'x86_64'|'amd64')       env2yamlarch=amd64;       ;;     'aarch64'|'arm64')       env2yamlarch=arm64;       ;;     *) echo >&2 "error: unsupported architecture '$env2yamlarch'"; exit 1 ;;   esac;   mkdir -p /usr/local/bin;   cp env2yaml/env2yaml-${env2yamlarch} /usr/local/bin/env2yaml;   rm -rf env2yaml # buildkit
# Thu, 13 Nov 2025 23:29:39 GMT
COPY bin/docker-entrypoint /usr/local/bin/ # buildkit
# Thu, 13 Nov 2025 23:29:39 GMT
RUN chmod 0755 /usr/local/bin/docker-entrypoint # buildkit
# Thu, 13 Nov 2025 23:29:39 GMT
USER 1000
# Thu, 13 Nov 2025 23:29:39 GMT
EXPOSE map[5044/tcp:{} 9600/tcp:{}]
# Thu, 13 Nov 2025 23:29:39 GMT
LABEL org.label-schema.schema-version=1.0 org.label-schema.vendor=Elastic org.opencontainers.image.vendor=Elastic org.label-schema.name=logstash org.opencontainers.image.title=logstash org.label-schema.version=8.19.7 org.opencontainers.image.version=8.19.7 org.label-schema.url=https://www.elastic.co/products/logstash org.label-schema.vcs-url=https://github.com/elastic/logstash org.label-schema.license=Elastic License org.opencontainers.image.licenses=Elastic License org.opencontainers.image.description=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' org.label-schema.build-date=2025-11-04T18:31:44+00:00 org.opencontainers.image.created=2025-11-04T18:31:44+00:00
# Thu, 13 Nov 2025 23:29:39 GMT
ENTRYPOINT ["/usr/local/bin/docker-entrypoint"]
```

-	Layers:
	-	`sha256:20043066d3d5c78b45520c5707319835ac7d1f3d7f0dded0138ea0897d6a3188`  
		Last Modified: Thu, 16 Oct 2025 21:15:22 GMT  
		Size: 29.7 MB (29724688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff90193b95fb19e4f476b7f04f879023aa7c2919ba3dbd305c392fe481909c72`  
		Last Modified: Thu, 13 Nov 2025 23:30:33 GMT  
		Size: 49.0 MB (49030468 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32cf3e8735f7211d5096f908fa83e51cd1283a8715e80083851ee811d3c6ab2e`  
		Last Modified: Thu, 13 Nov 2025 23:30:30 GMT  
		Size: 1.2 KB (1235 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f94c12b7ce0c034d668bd970d5f5164af02046f0c709ef756177cb8dd8d94a6c`  
		Last Modified: Fri, 14 Nov 2025 02:25:29 GMT  
		Size: 441.4 MB (441397950 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6adf37063a9f4db09ab05e0a7cf30465972ac6d8ef629ccc468ed40052904071`  
		Last Modified: Thu, 13 Nov 2025 23:30:29 GMT  
		Size: 278.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bf601524a146f2507b8e6dcd31b1220232b3948401f0a8b9598e6d1bce5fe22`  
		Last Modified: Thu, 13 Nov 2025 23:30:29 GMT  
		Size: 1.6 KB (1582 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f820cd3ad32d9b3d8de95154da1b33fb379dedc14494161e28cfa1038c5aa65`  
		Last Modified: Thu, 13 Nov 2025 23:30:29 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a09044aedf3a8739fe029075c3b8230d4ec51d6a9400eecfd4b7d8ed4678ba4`  
		Last Modified: Thu, 13 Nov 2025 23:30:29 GMT  
		Size: 1.8 KB (1766 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f53632abd983b209fe839ae0cbc458dcc2b6b55c7b7fd2c6c1ee39e2d248dcb`  
		Last Modified: Thu, 13 Nov 2025 23:30:29 GMT  
		Size: 4.0 MB (4005469 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b380f3267c3a88eebbca8078dcd80bb0a086ac8bf7bce7516c0523b479c03f36`  
		Last Modified: Thu, 13 Nov 2025 23:30:30 GMT  
		Size: 2.1 MB (2078666 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2bd43b587ce39783a1027a5ddefc25df9d6f4df10730e7b43644e2e5ed7aba6`  
		Last Modified: Thu, 13 Nov 2025 23:30:29 GMT  
		Size: 712.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `logstash:8.19.7` - unknown; unknown

```console
$ docker pull logstash@sha256:168a2252d7fcc9f127368442cabef6cf601d17ddac28c7d7960ba8f9956904b5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3687833 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b1d1bd1576defe445eb6e8d35307fb9558b8b8a55e819c1d7960b9bdfb76131d`

```dockerfile
```

-	Layers:
	-	`sha256:4fb9fe7e9fd44457c7a082d6d8bd10b79a988bc4aaaca5843e08f7c079161c48`  
		Last Modified: Fri, 14 Nov 2025 01:53:35 GMT  
		Size: 3.7 MB (3653221 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b531694c6f7ad13f3f30cdb1638f9564f42d493b791b3e606b6447d01235b4f6`  
		Last Modified: Fri, 14 Nov 2025 01:53:35 GMT  
		Size: 34.6 KB (34612 bytes)  
		MIME: application/vnd.in-toto+json

### `logstash:8.19.7` - linux; arm64 variant v8

```console
$ docker pull logstash@sha256:687d30ee863290f416a9344f434a7f425d80a6262c107ccb9a4b6c43f05b451c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **525.4 MB (525403370 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ecf30ad8c23d7acbc32d92043eb98675b6bceaa3675696aad583e5eb1e593a1f`
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
# Thu, 13 Nov 2025 23:28:30 GMT
RUN for iter in {1..10}; do       export DEBIAN_FRONTEND=noninteractive &&     apt-get update -y &&   apt-get upgrade -y &&   apt-get install -y procps findutils tar gzip &&         apt-get install -y locales &&         apt-get install -y curl &&     apt-get clean all &&       locale-gen 'en_US.UTF-8' &&     apt-get clean metadata &&   exit_code=0 && break || exit_code=$? && echo "packaging error: retry $iter in 10s" && apt-get clean all &&   apt-get clean metadata && sleep 10; done; (exit $exit_code) # buildkit
# Thu, 13 Nov 2025 23:28:30 GMT
RUN userdel -r ubuntu && groupadd --gid 1000 logstash &&   useradd --uid 1000 --gid 1000 --home /usr/share/logstash --no-create-home logstash # buildkit
# Thu, 13 Nov 2025 23:29:13 GMT
RUN curl -Lo - https://artifacts.elastic.co/downloads/logstash/logstash-8.19.7-linux-$(arch).tar.gz |   tar zxf - -C /usr/share &&   mv /usr/share/logstash-8.19.7 /usr/share/logstash &&   chown --recursive logstash:logstash /usr/share/logstash/ &&   chown -R logstash:root /usr/share/logstash &&   chmod -R g=u /usr/share/logstash &&   mkdir /licenses/ &&   mv /usr/share/logstash/NOTICE.TXT /licenses/NOTICE.TXT &&   mv /usr/share/logstash/LICENSE.txt /licenses/LICENSE.txt &&   find /usr/share/logstash -type d -exec chmod g+s {} \; &&   ln -s /usr/share/logstash /opt/logstash # buildkit
# Thu, 13 Nov 2025 23:29:13 GMT
WORKDIR /usr/share/logstash
# Thu, 13 Nov 2025 23:29:13 GMT
ENV ELASTIC_CONTAINER=true
# Thu, 13 Nov 2025 23:29:13 GMT
ENV PATH=/usr/share/logstash/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 13 Nov 2025 23:29:13 GMT
COPY config/logstash-full.yml config/logstash.yml # buildkit
# Thu, 13 Nov 2025 23:29:13 GMT
COPY config/pipelines.yml config/log4j2.properties config/log4j2.file.properties config/ # buildkit
# Thu, 13 Nov 2025 23:29:13 GMT
COPY pipeline/default.conf pipeline/logstash.conf # buildkit
# Thu, 13 Nov 2025 23:29:13 GMT
RUN chown --recursive logstash:root config/ pipeline/ # buildkit
# Thu, 13 Nov 2025 23:29:13 GMT
ENV LANG=en_US.UTF-8 LC_ALL=en_US.UTF-8
# Thu, 13 Nov 2025 23:29:13 GMT
COPY env2yaml/env2yaml-amd64 env2yaml/env2yaml-arm64 env2yaml/ # buildkit
# Thu, 13 Nov 2025 23:29:13 GMT
RUN set -eux; env2yamlarch="$(dpkg --print-architecture)";   case "${env2yamlarch}" in     'x86_64'|'amd64')       env2yamlarch=amd64;       ;;     'aarch64'|'arm64')       env2yamlarch=arm64;       ;;     *) echo >&2 "error: unsupported architecture '$env2yamlarch'"; exit 1 ;;   esac;   mkdir -p /usr/local/bin;   cp env2yaml/env2yaml-${env2yamlarch} /usr/local/bin/env2yaml;   rm -rf env2yaml # buildkit
# Thu, 13 Nov 2025 23:29:13 GMT
COPY bin/docker-entrypoint /usr/local/bin/ # buildkit
# Thu, 13 Nov 2025 23:29:13 GMT
RUN chmod 0755 /usr/local/bin/docker-entrypoint # buildkit
# Thu, 13 Nov 2025 23:29:13 GMT
USER 1000
# Thu, 13 Nov 2025 23:29:13 GMT
EXPOSE map[5044/tcp:{} 9600/tcp:{}]
# Thu, 13 Nov 2025 23:29:13 GMT
LABEL org.label-schema.schema-version=1.0 org.label-schema.vendor=Elastic org.opencontainers.image.vendor=Elastic org.label-schema.name=logstash org.opencontainers.image.title=logstash org.label-schema.version=8.19.7 org.opencontainers.image.version=8.19.7 org.label-schema.url=https://www.elastic.co/products/logstash org.label-schema.vcs-url=https://github.com/elastic/logstash org.label-schema.license=Elastic License org.opencontainers.image.licenses=Elastic License org.opencontainers.image.description=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' org.label-schema.build-date=2025-11-04T18:31:44+00:00 org.opencontainers.image.created=2025-11-04T18:31:44+00:00
# Thu, 13 Nov 2025 23:29:13 GMT
ENTRYPOINT ["/usr/local/bin/docker-entrypoint"]
```

-	Layers:
	-	`sha256:97dd3f0ce510a30a2868ff104e9ff286ffc0ef01284aebe383ea81e85e26a415`  
		Last Modified: Thu, 16 Oct 2025 21:17:48 GMT  
		Size: 28.9 MB (28861957 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed524d9de1f203d2c1af7057d298666cbd488f2248ae06c4997f2665808977cc`  
		Last Modified: Thu, 13 Nov 2025 23:30:12 GMT  
		Size: 50.9 MB (50920543 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b599cedf77b61925226d81a77267d2176a938ffadb159c7c298bbff0ab33cb30`  
		Last Modified: Thu, 13 Nov 2025 23:30:07 GMT  
		Size: 1.2 KB (1223 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2bf5a448feb9d96d06df1bcb8773b364693b852aa24dbdfeb376b02a6e399b7`  
		Last Modified: Fri, 14 Nov 2025 02:26:04 GMT  
		Size: 439.7 MB (439682989 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:111c29a4877e9b1d21de678530eb31664b44c2ebfe17cb480d962118ce008265`  
		Last Modified: Thu, 13 Nov 2025 23:30:07 GMT  
		Size: 278.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:796c9e12c13eec50fbd5ba636a5378f96c057ed6f4ff6b4e4e972e140d975336`  
		Last Modified: Thu, 13 Nov 2025 23:30:07 GMT  
		Size: 1.6 KB (1582 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f21e87a7961528613dbf0c07c91f0da0ffc963cff13c2b49d8ca47eccdca267`  
		Last Modified: Thu, 13 Nov 2025 23:30:07 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df883f3589cfa4fce086242bb1b8ba33014436661a49a599ebc593a9fe66c9e8`  
		Last Modified: Thu, 13 Nov 2025 23:30:07 GMT  
		Size: 1.8 KB (1768 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c16b66a44c5ac0a3c21e84e9d3c3641f3c6f49ef08b43d4f1d03ea63b64c28b`  
		Last Modified: Thu, 13 Nov 2025 23:30:08 GMT  
		Size: 4.0 MB (4005469 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1712271c13bd779319b6dcf8eb07e84bd3452dd7950d3f3fa0917a0a7efdc1f`  
		Last Modified: Thu, 13 Nov 2025 23:30:08 GMT  
		Size: 1.9 MB (1926505 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88216873916a581231d01ffd74c4b05124cb4fc7e8b3d8603481a4e38a984e48`  
		Last Modified: Thu, 13 Nov 2025 23:30:08 GMT  
		Size: 713.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `logstash:8.19.7` - unknown; unknown

```console
$ docker pull logstash@sha256:b5cd6760869587fcceda70901f12dcb45e1ec7e08979a57b7e25ee82acee470d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3688402 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f2463afd5d871f2363ee7206f2fa0b1242c912783bd2a5349bcb378c82f79b82`

```dockerfile
```

-	Layers:
	-	`sha256:e28a155d2bf8744e624f1814393eaf01f4a7770d594eddf53b1833ef42848d0c`  
		Last Modified: Fri, 14 Nov 2025 01:53:40 GMT  
		Size: 3.7 MB (3653646 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7006e0acbb5095a9edbf1ad412390e64481791be5029909383227f80b8a62257`  
		Last Modified: Fri, 14 Nov 2025 01:53:41 GMT  
		Size: 34.8 KB (34756 bytes)  
		MIME: application/vnd.in-toto+json

## `logstash:9.1.7`

```console
$ docker pull logstash@sha256:1282352c8c8aed501b03d67a1729ea14e782b90e35b568962eb837d28b5b51e5
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `logstash:9.1.7` - linux; amd64

```console
$ docker pull logstash@sha256:e004b73b7048319ea8f0bec7491a85089dac61b61bbd0333a9f69290fa3a5750
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **477.6 MB (477558809 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0eb79fb999a63a5aef6da3905369f3d19270be57161d5c48ba7e411d30a9fca3`
-	Entrypoint: `["\/usr\/local\/bin\/docker-entrypoint"]`

```dockerfile
# Mon, 03 Nov 2025 14:28:07 GMT
LABEL maintainer="Red Hat, Inc."
# Mon, 03 Nov 2025 14:28:07 GMT
LABEL vendor="Red Hat, Inc."
# Mon, 03 Nov 2025 14:28:07 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Mon, 03 Nov 2025 14:28:07 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.7"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Mon, 03 Nov 2025 14:28:07 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Mon, 03 Nov 2025 14:28:07 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Mon, 03 Nov 2025 14:28:07 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 03 Nov 2025 14:28:07 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 03 Nov 2025 14:28:07 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Mon, 03 Nov 2025 14:28:07 GMT
LABEL io.openshift.expose-services=""
# Mon, 03 Nov 2025 14:28:07 GMT
LABEL io.openshift.tags="minimal rhel9"
# Mon, 03 Nov 2025 14:28:07 GMT
LABEL compose-id="RHEL-9.7.0-updates-20251029.7"
# Mon, 03 Nov 2025 14:28:07 GMT
ENV container oci
# Mon, 03 Nov 2025 14:28:08 GMT
COPY dir:39710e73aef560d625154347dc7e6b417064723d33d900483645d9d706c0f7a2 in /      
# Mon, 03 Nov 2025 14:28:08 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Mon, 03 Nov 2025 14:28:08 GMT
CMD ["/bin/bash"]
# Mon, 03 Nov 2025 14:28:08 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /usr/share/buildinfo/content-sets.json      
# Mon, 03 Nov 2025 14:28:08 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /root/buildinfo/content_manifests/content-sets.json      
# Mon, 03 Nov 2025 14:28:08 GMT
COPY file:90c5e1a95185d091ee07721ff43a8413d78a6f7cb920f7ce46a03a173e5f926a in /usr/share/buildinfo/labels.json      
# Mon, 03 Nov 2025 14:28:08 GMT
COPY file:90c5e1a95185d091ee07721ff43a8413d78a6f7cb920f7ce46a03a173e5f926a in /root/buildinfo/labels.json      
# Mon, 03 Nov 2025 14:28:09 GMT
LABEL "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="02d02ad5d9d5ef0add399eb1c8d5f2a4b9261204" "org.opencontainers.image.revision"="02d02ad5d9d5ef0add399eb1c8d5f2a4b9261204" "build-date"="2025-11-03T14:27:54Z" "release"="1762180032"org.opencontainers.image.revision=02d02ad5d9d5ef0add399eb1c8d5f2a4b9261204
# Wed, 12 Nov 2025 00:27:03 GMT
ENV ELASTIC_CONTAINER=true
# Wed, 12 Nov 2025 00:27:03 GMT
ENV PATH=/usr/share/logstash/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 12 Nov 2025 00:27:03 GMT
ENV LANG=C.UTF-8 LC_ALL=C.UTF-8
# Wed, 12 Nov 2025 00:27:03 GMT
WORKDIR /usr/share
# Wed, 12 Nov 2025 00:27:12 GMT
RUN microdnf install -y procps findutils tar gzip &&   microdnf install -y openssl &&   microdnf install -y which shadow-utils &&   microdnf clean all # buildkit
# Wed, 12 Nov 2025 00:28:03 GMT
RUN groupadd --gid 1000 logstash &&   adduser --uid 1000 --gid 1000   --home "/usr/share/logstash"   --no-create-home   logstash &&   arch="$(rpm --query --queryformat='%{ARCH}' rpm)" &&   curl -f -Lo logstash.tar.gz https://artifacts.elastic.co/downloads/logstash/logstash-9.1.7-linux-${arch}.tar.gz &&   tar -zxf logstash.tar.gz -C /usr/share &&   rm logstash.tar.gz &&   mv /usr/share/logstash-9.1.7 /usr/share/logstash &&   chown -R logstash:root /usr/share/logstash &&   chmod -R g=u /usr/share/logstash &&   mkdir /licenses &&   mv /usr/share/logstash/NOTICE.TXT /licenses/NOTICE.TXT &&   mv /usr/share/logstash/LICENSE.txt /licenses/LICENSE.txt &&   find /usr/share/logstash -type d -exec chmod g+s {} \; &&   ln -s /usr/share/logstash /opt/logstash # buildkit
# Wed, 12 Nov 2025 00:28:03 GMT
COPY /tmp/go/src/env2yaml/env2yaml /usr/local/bin/env2yaml # buildkit
# Wed, 12 Nov 2025 00:28:03 GMT
COPY --chown=logstash:root config/pipelines.yml config/log4j2.properties config/log4j2.file.properties /usr/share/logstash/config/ # buildkit
# Wed, 12 Nov 2025 00:28:03 GMT
COPY --chown=logstash:root config/logstash-full.yml /usr/share/logstash/config/logstash.yml # buildkit
# Wed, 12 Nov 2025 00:28:03 GMT
COPY --chown=logstash:root pipeline/default.conf /usr/share/logstash/pipeline/logstash.conf # buildkit
# Wed, 12 Nov 2025 00:28:03 GMT
COPY --chmod=0755 bin/docker-entrypoint /usr/local/bin/ # buildkit
# Wed, 12 Nov 2025 00:28:03 GMT
WORKDIR /usr/share/logstash
# Wed, 12 Nov 2025 00:28:03 GMT
USER 1000
# Wed, 12 Nov 2025 00:28:03 GMT
EXPOSE map[5044/tcp:{} 9600/tcp:{}]
# Wed, 12 Nov 2025 00:28:03 GMT
LABEL org.label-schema.build-date=2025-11-04T18:24:06+00:00 org.label-schema.license=Elastic License org.label-schema.name=logstash org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/logstash org.label-schema.vcs-url=https://github.com/elastic/logstash org.label-schema.vendor=Elastic org.label-schema.version=9.1.7 org.opencontainers.image.created=2025-11-04T18:24:06+00:00 org.opencontainers.image.description=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' org.opencontainers.image.licenses=Elastic License org.opencontainers.image.title=logstash org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=9.1.7 description=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' license=Elastic License maintainer=info@elastic.co name=logstash summary=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' vendor=Elastic
# Wed, 12 Nov 2025 00:28:03 GMT
ENTRYPOINT ["/usr/local/bin/docker-entrypoint"]
```

-	Layers:
	-	`sha256:ef1934e719674e24c0e9879fad65a4a167d4510bb71da2c3ed5e85f5d800bd89`  
		Last Modified: Tue, 11 Nov 2025 17:18:44 GMT  
		Size: 40.0 MB (40000743 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba08ffa2fc6588f8cfb8ee84071bf573d0941e8759083a6f14b5c578d504c816`  
		Last Modified: Wed, 12 Nov 2025 00:28:51 GMT  
		Size: 5.1 MB (5147817 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8e5a90d5cfdbcec07a48ea0d47b6b726340489b3bb63b9eda8e0f4959fb914e`  
		Last Modified: Wed, 12 Nov 2025 03:57:24 GMT  
		Size: 430.3 MB (430328501 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4145e9627d74996067e05f5daba468e5c8950a39525fe4b07bbb8458395de9c`  
		Last Modified: Wed, 12 Nov 2025 00:28:50 GMT  
		Size: 2.1 MB (2078842 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc110383dac8a31a21e671d5d2be5ce6e1229a7ed8df5a8c65877f62713c582e`  
		Last Modified: Wed, 12 Nov 2025 00:28:50 GMT  
		Size: 1.6 KB (1576 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13e77c4a61dff62eea99ce2f9782574a36707435e44da66b724cdbdd16a8828d`  
		Last Modified: Wed, 12 Nov 2025 00:28:50 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b815ff428d47931db349a477168f19978f6b1c4aa84da204d4fcb3fa9e8ae83d`  
		Last Modified: Wed, 12 Nov 2025 00:28:50 GMT  
		Size: 278.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9173feb053dc15a039ee3ef321fff16e283b081d70fc48cb64acf1e8d7f8c9c`  
		Last Modified: Wed, 12 Nov 2025 00:28:50 GMT  
		Size: 711.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `logstash:9.1.7` - unknown; unknown

```console
$ docker pull logstash@sha256:cb8d8ed667b5d722b79ddc5d1a9d66f21adc3cdd051d7f5339d9f7d3c6f86b2f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2120096 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2129b42c35ef3fbf2b16af012560eb6ef21e84deaa770a51d85b4cc61f6f953a`

```dockerfile
```

-	Layers:
	-	`sha256:1729df2508444f7574e03c9459a5e135b33ad9d6158c1788088cb7b4134ad8cc`  
		Last Modified: Wed, 12 Nov 2025 01:53:20 GMT  
		Size: 2.1 MB (2090542 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:97e60429724087a4668585cf45306d362727566adffb018a156c60e0bd5b3061`  
		Last Modified: Wed, 12 Nov 2025 01:53:21 GMT  
		Size: 29.6 KB (29554 bytes)  
		MIME: application/vnd.in-toto+json

### `logstash:9.1.7` - linux; arm64 variant v8

```console
$ docker pull logstash@sha256:7446343e7c606bd0247c1e1a08b51d052b94cf6f3105beddad29dd496754c2d3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **473.9 MB (473889089 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e23d61d14f8a3d159694e31614bf41271a893f285c4e05c58c71fb88300d007`
-	Entrypoint: `["\/usr\/local\/bin\/docker-entrypoint"]`

```dockerfile
# Mon, 03 Nov 2025 14:39:20 GMT
LABEL maintainer="Red Hat, Inc."
# Mon, 03 Nov 2025 14:39:20 GMT
LABEL vendor="Red Hat, Inc."
# Mon, 03 Nov 2025 14:39:20 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Mon, 03 Nov 2025 14:39:20 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.7"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Mon, 03 Nov 2025 14:39:20 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Mon, 03 Nov 2025 14:39:20 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Mon, 03 Nov 2025 14:39:20 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 03 Nov 2025 14:39:20 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 03 Nov 2025 14:39:20 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Mon, 03 Nov 2025 14:39:20 GMT
LABEL io.openshift.expose-services=""
# Mon, 03 Nov 2025 14:39:20 GMT
LABEL io.openshift.tags="minimal rhel9"
# Mon, 03 Nov 2025 14:39:20 GMT
LABEL compose-id="RHEL-9.7.0-updates-20251029.7"
# Mon, 03 Nov 2025 14:39:20 GMT
ENV container oci
# Mon, 03 Nov 2025 14:39:21 GMT
COPY dir:e6638cbef7baa2be94a007ecfd2531710d358328001d7cc1a125e3837ced3f20 in /      
# Mon, 03 Nov 2025 14:39:21 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Mon, 03 Nov 2025 14:39:21 GMT
CMD ["/bin/bash"]
# Mon, 03 Nov 2025 14:39:21 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /usr/share/buildinfo/content-sets.json      
# Mon, 03 Nov 2025 14:39:21 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /root/buildinfo/content_manifests/content-sets.json      
# Mon, 03 Nov 2025 14:39:21 GMT
COPY file:e6c4ae052c98b0a8455fbdd83ea8c94d3ab007cf48a3ddf7f4cddb8006394bb4 in /usr/share/buildinfo/labels.json      
# Mon, 03 Nov 2025 14:39:21 GMT
COPY file:e6c4ae052c98b0a8455fbdd83ea8c94d3ab007cf48a3ddf7f4cddb8006394bb4 in /root/buildinfo/labels.json      
# Mon, 03 Nov 2025 14:39:21 GMT
LABEL "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="02d02ad5d9d5ef0add399eb1c8d5f2a4b9261204" "org.opencontainers.image.revision"="02d02ad5d9d5ef0add399eb1c8d5f2a4b9261204" "build-date"="2025-11-03T14:39:04Z" "release"="1762180032"org.opencontainers.image.revision=02d02ad5d9d5ef0add399eb1c8d5f2a4b9261204
# Wed, 12 Nov 2025 00:27:47 GMT
ENV ELASTIC_CONTAINER=true
# Wed, 12 Nov 2025 00:27:47 GMT
ENV PATH=/usr/share/logstash/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 12 Nov 2025 00:27:47 GMT
ENV LANG=C.UTF-8 LC_ALL=C.UTF-8
# Wed, 12 Nov 2025 00:27:47 GMT
WORKDIR /usr/share
# Wed, 12 Nov 2025 00:27:57 GMT
RUN microdnf install -y procps findutils tar gzip &&   microdnf install -y openssl &&   microdnf install -y which shadow-utils &&   microdnf clean all # buildkit
# Wed, 12 Nov 2025 00:28:47 GMT
RUN groupadd --gid 1000 logstash &&   adduser --uid 1000 --gid 1000   --home "/usr/share/logstash"   --no-create-home   logstash &&   arch="$(rpm --query --queryformat='%{ARCH}' rpm)" &&   curl -f -Lo logstash.tar.gz https://artifacts.elastic.co/downloads/logstash/logstash-9.1.7-linux-${arch}.tar.gz &&   tar -zxf logstash.tar.gz -C /usr/share &&   rm logstash.tar.gz &&   mv /usr/share/logstash-9.1.7 /usr/share/logstash &&   chown -R logstash:root /usr/share/logstash &&   chmod -R g=u /usr/share/logstash &&   mkdir /licenses &&   mv /usr/share/logstash/NOTICE.TXT /licenses/NOTICE.TXT &&   mv /usr/share/logstash/LICENSE.txt /licenses/LICENSE.txt &&   find /usr/share/logstash -type d -exec chmod g+s {} \; &&   ln -s /usr/share/logstash /opt/logstash # buildkit
# Wed, 12 Nov 2025 00:28:47 GMT
COPY /tmp/go/src/env2yaml/env2yaml /usr/local/bin/env2yaml # buildkit
# Wed, 12 Nov 2025 00:28:47 GMT
COPY --chown=logstash:root config/pipelines.yml config/log4j2.properties config/log4j2.file.properties /usr/share/logstash/config/ # buildkit
# Wed, 12 Nov 2025 00:28:47 GMT
COPY --chown=logstash:root config/logstash-full.yml /usr/share/logstash/config/logstash.yml # buildkit
# Wed, 12 Nov 2025 00:28:47 GMT
COPY --chown=logstash:root pipeline/default.conf /usr/share/logstash/pipeline/logstash.conf # buildkit
# Wed, 12 Nov 2025 00:28:48 GMT
COPY --chmod=0755 bin/docker-entrypoint /usr/local/bin/ # buildkit
# Wed, 12 Nov 2025 00:28:48 GMT
WORKDIR /usr/share/logstash
# Wed, 12 Nov 2025 00:28:48 GMT
USER 1000
# Wed, 12 Nov 2025 00:28:48 GMT
EXPOSE map[5044/tcp:{} 9600/tcp:{}]
# Wed, 12 Nov 2025 00:28:48 GMT
LABEL org.label-schema.build-date=2025-11-04T18:24:06+00:00 org.label-schema.license=Elastic License org.label-schema.name=logstash org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/logstash org.label-schema.vcs-url=https://github.com/elastic/logstash org.label-schema.vendor=Elastic org.label-schema.version=9.1.7 org.opencontainers.image.created=2025-11-04T18:24:06+00:00 org.opencontainers.image.description=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' org.opencontainers.image.licenses=Elastic License org.opencontainers.image.title=logstash org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=9.1.7 description=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' license=Elastic License maintainer=info@elastic.co name=logstash summary=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' vendor=Elastic
# Wed, 12 Nov 2025 00:28:48 GMT
ENTRYPOINT ["/usr/local/bin/docker-entrypoint"]
```

-	Layers:
	-	`sha256:fccdcd3fc47f898d65f9d4531d01539ce33a7ec8038500d557bfe58eb4b6ae87`  
		Last Modified: Tue, 11 Nov 2025 18:10:59 GMT  
		Size: 38.2 MB (38211473 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cf5e300dc91d5bfeeb5cf4d5a19dc6ac25019695b33b871574ab571904330fa`  
		Last Modified: Wed, 12 Nov 2025 00:29:39 GMT  
		Size: 5.1 MB (5146008 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:feba5795ac88e10c36af818451049ef447d5b4d4ea79f63a5e4e37720bf925c7`  
		Last Modified: Wed, 12 Nov 2025 09:37:22 GMT  
		Size: 428.6 MB (428601843 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ada5ed8d4b716c793e1d9fc654bf155dd85f35850647d2710837ef164949c524`  
		Last Modified: Wed, 12 Nov 2025 00:29:39 GMT  
		Size: 1.9 MB (1926865 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c59946ad42512d5539203225831945f1206025834c2955d7305938faaad98643`  
		Last Modified: Wed, 12 Nov 2025 00:29:39 GMT  
		Size: 1.6 KB (1575 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb96a9a874ba2d15cefcee8637b656583a5a7b9b98596cf0721fc07bd5711ce0`  
		Last Modified: Wed, 12 Nov 2025 00:29:39 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ceb98927cdcaf7ab06495f1139a227208f9bab9da29db5507b9bd02379928b7`  
		Last Modified: Wed, 12 Nov 2025 00:29:39 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2709ff6f5a7713057b87c5bdc79ba322f8046b0beae226b91520b334500b19e`  
		Last Modified: Wed, 12 Nov 2025 00:29:39 GMT  
		Size: 711.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `logstash:9.1.7` - unknown; unknown

```console
$ docker pull logstash@sha256:40198e71762bcf1f23266d1c3f8f327e6f8be0a3a5c7f4503aa0cc4b4fec45c2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2120783 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2412e91c4e1d0b4098b801e9f35d067509c470ce2981a68093f739b3d7c78ce7`

```dockerfile
```

-	Layers:
	-	`sha256:9c2ea2193f5da041dd02659d351def8150bcdaafabdf896beae5db8c8611369d`  
		Last Modified: Wed, 12 Nov 2025 01:53:24 GMT  
		Size: 2.1 MB (2091112 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0be87fbc662ea7353bf088d104208397abfaccd1658efcbcd8d8368565124f2e`  
		Last Modified: Wed, 12 Nov 2025 01:53:25 GMT  
		Size: 29.7 KB (29671 bytes)  
		MIME: application/vnd.in-toto+json

## `logstash:9.2.1`

```console
$ docker pull logstash@sha256:782d55660ff0539ca757d56deec0789ac17728bf509c2e72ddf0958e861c2c47
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `logstash:9.2.1` - linux; amd64

```console
$ docker pull logstash@sha256:838e4196851770c712953dc599b761d4544316aebdc2f9b79c2d4b2c5b2aaf23
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **487.9 MB (487862141 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1689deab253065b9ee98089de1d7bc7f7c007b3a8f4c55ed4ecb4f2293018534`
-	Entrypoint: `["\/usr\/local\/bin\/docker-entrypoint"]`

```dockerfile
# Mon, 03 Nov 2025 14:28:07 GMT
LABEL maintainer="Red Hat, Inc."
# Mon, 03 Nov 2025 14:28:07 GMT
LABEL vendor="Red Hat, Inc."
# Mon, 03 Nov 2025 14:28:07 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Mon, 03 Nov 2025 14:28:07 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.7"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Mon, 03 Nov 2025 14:28:07 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Mon, 03 Nov 2025 14:28:07 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Mon, 03 Nov 2025 14:28:07 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 03 Nov 2025 14:28:07 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 03 Nov 2025 14:28:07 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Mon, 03 Nov 2025 14:28:07 GMT
LABEL io.openshift.expose-services=""
# Mon, 03 Nov 2025 14:28:07 GMT
LABEL io.openshift.tags="minimal rhel9"
# Mon, 03 Nov 2025 14:28:07 GMT
LABEL compose-id="RHEL-9.7.0-updates-20251029.7"
# Mon, 03 Nov 2025 14:28:07 GMT
ENV container oci
# Mon, 03 Nov 2025 14:28:08 GMT
COPY dir:39710e73aef560d625154347dc7e6b417064723d33d900483645d9d706c0f7a2 in /      
# Mon, 03 Nov 2025 14:28:08 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Mon, 03 Nov 2025 14:28:08 GMT
CMD ["/bin/bash"]
# Mon, 03 Nov 2025 14:28:08 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /usr/share/buildinfo/content-sets.json      
# Mon, 03 Nov 2025 14:28:08 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /root/buildinfo/content_manifests/content-sets.json      
# Mon, 03 Nov 2025 14:28:08 GMT
COPY file:90c5e1a95185d091ee07721ff43a8413d78a6f7cb920f7ce46a03a173e5f926a in /usr/share/buildinfo/labels.json      
# Mon, 03 Nov 2025 14:28:08 GMT
COPY file:90c5e1a95185d091ee07721ff43a8413d78a6f7cb920f7ce46a03a173e5f926a in /root/buildinfo/labels.json      
# Mon, 03 Nov 2025 14:28:09 GMT
LABEL "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="02d02ad5d9d5ef0add399eb1c8d5f2a4b9261204" "org.opencontainers.image.revision"="02d02ad5d9d5ef0add399eb1c8d5f2a4b9261204" "build-date"="2025-11-03T14:27:54Z" "release"="1762180032"org.opencontainers.image.revision=02d02ad5d9d5ef0add399eb1c8d5f2a4b9261204
# Wed, 12 Nov 2025 00:27:03 GMT
ENV ELASTIC_CONTAINER=true
# Wed, 12 Nov 2025 00:27:03 GMT
ENV PATH=/usr/share/logstash/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 12 Nov 2025 00:27:03 GMT
ENV LANG=C.UTF-8 LC_ALL=C.UTF-8
# Wed, 12 Nov 2025 00:27:03 GMT
WORKDIR /usr/share
# Wed, 12 Nov 2025 00:27:12 GMT
RUN microdnf install -y procps findutils tar gzip &&   microdnf install -y openssl &&   microdnf install -y which shadow-utils &&   microdnf clean all # buildkit
# Wed, 12 Nov 2025 00:29:37 GMT
RUN groupadd --gid 1000 logstash &&   adduser --uid 1000 --gid 1000   --home "/usr/share/logstash"   --no-create-home   logstash &&   arch="$(rpm --query --queryformat='%{ARCH}' rpm)" &&   curl --fail --location --output logstash.tar.gz https://artifacts.elastic.co/downloads/logstash/logstash-9.2.1-linux-${arch}.tar.gz &&   tar -zxf logstash.tar.gz -C /usr/share &&   rm logstash.tar.gz &&   mv /usr/share/logstash-9.2.1 /usr/share/logstash &&   chown -R logstash:root /usr/share/logstash &&   chmod -R g=u /usr/share/logstash &&   mkdir /licenses &&   mv /usr/share/logstash/NOTICE.TXT /licenses/NOTICE.TXT &&   mv /usr/share/logstash/LICENSE.txt /licenses/LICENSE.txt &&   find /usr/share/logstash -type d -exec chmod g+s {} \; &&   ln -s /usr/share/logstash /opt/logstash # buildkit
# Wed, 12 Nov 2025 00:29:37 GMT
COPY /tmp/go/src/env2yaml/env2yaml /usr/local/bin/env2yaml # buildkit
# Wed, 12 Nov 2025 00:29:37 GMT
COPY --chown=logstash:root config/pipelines.yml config/log4j2.properties config/log4j2.file.properties /usr/share/logstash/config/ # buildkit
# Wed, 12 Nov 2025 00:29:37 GMT
COPY --chown=logstash:root config/logstash-full.yml /usr/share/logstash/config/logstash.yml # buildkit
# Wed, 12 Nov 2025 00:29:37 GMT
COPY --chown=logstash:root pipeline/default.conf /usr/share/logstash/pipeline/logstash.conf # buildkit
# Wed, 12 Nov 2025 00:29:37 GMT
COPY --chmod=0755 bin/docker-entrypoint /usr/local/bin/ # buildkit
# Wed, 12 Nov 2025 00:29:37 GMT
WORKDIR /usr/share/logstash
# Wed, 12 Nov 2025 00:29:37 GMT
USER 1000
# Wed, 12 Nov 2025 00:29:37 GMT
EXPOSE map[5044/tcp:{} 9600/tcp:{}]
# Wed, 12 Nov 2025 00:29:37 GMT
LABEL org.label-schema.build-date=2025-11-04T18:22:56+00:00 org.label-schema.license=Elastic License org.label-schema.name=logstash org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/logstash org.label-schema.vcs-url=https://github.com/elastic/logstash org.label-schema.vendor=Elastic org.label-schema.version=9.2.1 org.opencontainers.image.created=2025-11-04T18:22:56+00:00 org.opencontainers.image.description=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' org.opencontainers.image.licenses=Elastic License org.opencontainers.image.title=logstash org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=9.2.1 description=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' license=Elastic License maintainer=info@elastic.co name=logstash summary=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' vendor=Elastic
# Wed, 12 Nov 2025 00:29:37 GMT
ENTRYPOINT ["/usr/local/bin/docker-entrypoint"]
```

-	Layers:
	-	`sha256:ef1934e719674e24c0e9879fad65a4a167d4510bb71da2c3ed5e85f5d800bd89`  
		Last Modified: Tue, 11 Nov 2025 17:18:44 GMT  
		Size: 40.0 MB (40000743 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba08ffa2fc6588f8cfb8ee84071bf573d0941e8759083a6f14b5c578d504c816`  
		Last Modified: Wed, 12 Nov 2025 00:28:51 GMT  
		Size: 5.1 MB (5147817 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d3e86bcf970f8e0f65cb30024c9d03958476f82cf22fecf96c5f86fa2f263be`  
		Last Modified: Wed, 12 Nov 2025 02:33:21 GMT  
		Size: 440.6 MB (440631845 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a349297bf9f6039497587783ef7c3d75bf4c39c752195f7609a4f176ae54cbe8`  
		Last Modified: Wed, 12 Nov 2025 00:30:24 GMT  
		Size: 2.1 MB (2078833 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45af0aad64cef5655ceb8fc1b625421e29f350eb14e188bf272476b0ab13a4d3`  
		Last Modified: Wed, 12 Nov 2025 00:30:24 GMT  
		Size: 1.6 KB (1575 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea4589ea598d3872511f70908a19cfd957ba70088159e21902bd73d06a26b59a`  
		Last Modified: Wed, 12 Nov 2025 00:30:24 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f0401be97e0334c2cdb9dd611cf6145a8a07acce6318b2f9ac50441c76ec650`  
		Last Modified: Wed, 12 Nov 2025 00:30:24 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f3b21ac1b8555f7ffe251b4ab39282d4c575549751e421c59a4f3857ef6a14f`  
		Last Modified: Wed, 12 Nov 2025 00:30:24 GMT  
		Size: 712.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `logstash:9.2.1` - unknown; unknown

```console
$ docker pull logstash@sha256:3e87ce19c4e77504e1d0682ee041942de055e724ae54aea4249c74b63ee73aea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2129963 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd389027b9941ff33e47f26ce06facac1659210d2db8313394a29168bb847a44`

```dockerfile
```

-	Layers:
	-	`sha256:b44d9863d7846416c296b28afbeeef327e1d804970178989f9ef601197ceea0b`  
		Last Modified: Wed, 12 Nov 2025 01:53:29 GMT  
		Size: 2.1 MB (2100362 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:92ba1e5cacb4de7171880aa1477beb651817f7ff57c344154596e108a93ca5ec`  
		Last Modified: Wed, 12 Nov 2025 01:53:30 GMT  
		Size: 29.6 KB (29601 bytes)  
		MIME: application/vnd.in-toto+json

### `logstash:9.2.1` - linux; arm64 variant v8

```console
$ docker pull logstash@sha256:f5b4ea7128b9c7400b5f85147696cd9f1bc3cb22662501b6fb1f6e617be57773
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **484.2 MB (484192729 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ac2e2fd9e93bb310c6f4f2fec4232f771879454aa63989e2897bcef3b2dc59e`
-	Entrypoint: `["\/usr\/local\/bin\/docker-entrypoint"]`

```dockerfile
# Mon, 03 Nov 2025 14:39:20 GMT
LABEL maintainer="Red Hat, Inc."
# Mon, 03 Nov 2025 14:39:20 GMT
LABEL vendor="Red Hat, Inc."
# Mon, 03 Nov 2025 14:39:20 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Mon, 03 Nov 2025 14:39:20 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.7"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Mon, 03 Nov 2025 14:39:20 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Mon, 03 Nov 2025 14:39:20 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Mon, 03 Nov 2025 14:39:20 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 03 Nov 2025 14:39:20 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 03 Nov 2025 14:39:20 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Mon, 03 Nov 2025 14:39:20 GMT
LABEL io.openshift.expose-services=""
# Mon, 03 Nov 2025 14:39:20 GMT
LABEL io.openshift.tags="minimal rhel9"
# Mon, 03 Nov 2025 14:39:20 GMT
LABEL compose-id="RHEL-9.7.0-updates-20251029.7"
# Mon, 03 Nov 2025 14:39:20 GMT
ENV container oci
# Mon, 03 Nov 2025 14:39:21 GMT
COPY dir:e6638cbef7baa2be94a007ecfd2531710d358328001d7cc1a125e3837ced3f20 in /      
# Mon, 03 Nov 2025 14:39:21 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Mon, 03 Nov 2025 14:39:21 GMT
CMD ["/bin/bash"]
# Mon, 03 Nov 2025 14:39:21 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /usr/share/buildinfo/content-sets.json      
# Mon, 03 Nov 2025 14:39:21 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /root/buildinfo/content_manifests/content-sets.json      
# Mon, 03 Nov 2025 14:39:21 GMT
COPY file:e6c4ae052c98b0a8455fbdd83ea8c94d3ab007cf48a3ddf7f4cddb8006394bb4 in /usr/share/buildinfo/labels.json      
# Mon, 03 Nov 2025 14:39:21 GMT
COPY file:e6c4ae052c98b0a8455fbdd83ea8c94d3ab007cf48a3ddf7f4cddb8006394bb4 in /root/buildinfo/labels.json      
# Mon, 03 Nov 2025 14:39:21 GMT
LABEL "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="02d02ad5d9d5ef0add399eb1c8d5f2a4b9261204" "org.opencontainers.image.revision"="02d02ad5d9d5ef0add399eb1c8d5f2a4b9261204" "build-date"="2025-11-03T14:39:04Z" "release"="1762180032"org.opencontainers.image.revision=02d02ad5d9d5ef0add399eb1c8d5f2a4b9261204
# Wed, 12 Nov 2025 00:26:07 GMT
ENV ELASTIC_CONTAINER=true
# Wed, 12 Nov 2025 00:26:07 GMT
ENV PATH=/usr/share/logstash/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 12 Nov 2025 00:26:07 GMT
ENV LANG=C.UTF-8 LC_ALL=C.UTF-8
# Wed, 12 Nov 2025 00:26:07 GMT
WORKDIR /usr/share
# Wed, 12 Nov 2025 00:26:16 GMT
RUN microdnf install -y procps findutils tar gzip &&   microdnf install -y openssl &&   microdnf install -y which shadow-utils &&   microdnf clean all # buildkit
# Wed, 12 Nov 2025 00:27:07 GMT
RUN groupadd --gid 1000 logstash &&   adduser --uid 1000 --gid 1000   --home "/usr/share/logstash"   --no-create-home   logstash &&   arch="$(rpm --query --queryformat='%{ARCH}' rpm)" &&   curl --fail --location --output logstash.tar.gz https://artifacts.elastic.co/downloads/logstash/logstash-9.2.1-linux-${arch}.tar.gz &&   tar -zxf logstash.tar.gz -C /usr/share &&   rm logstash.tar.gz &&   mv /usr/share/logstash-9.2.1 /usr/share/logstash &&   chown -R logstash:root /usr/share/logstash &&   chmod -R g=u /usr/share/logstash &&   mkdir /licenses &&   mv /usr/share/logstash/NOTICE.TXT /licenses/NOTICE.TXT &&   mv /usr/share/logstash/LICENSE.txt /licenses/LICENSE.txt &&   find /usr/share/logstash -type d -exec chmod g+s {} \; &&   ln -s /usr/share/logstash /opt/logstash # buildkit
# Wed, 12 Nov 2025 00:27:07 GMT
COPY /tmp/go/src/env2yaml/env2yaml /usr/local/bin/env2yaml # buildkit
# Wed, 12 Nov 2025 00:27:07 GMT
COPY --chown=logstash:root config/pipelines.yml config/log4j2.properties config/log4j2.file.properties /usr/share/logstash/config/ # buildkit
# Wed, 12 Nov 2025 00:27:07 GMT
COPY --chown=logstash:root config/logstash-full.yml /usr/share/logstash/config/logstash.yml # buildkit
# Wed, 12 Nov 2025 00:27:07 GMT
COPY --chown=logstash:root pipeline/default.conf /usr/share/logstash/pipeline/logstash.conf # buildkit
# Wed, 12 Nov 2025 00:27:07 GMT
COPY --chmod=0755 bin/docker-entrypoint /usr/local/bin/ # buildkit
# Wed, 12 Nov 2025 00:27:07 GMT
WORKDIR /usr/share/logstash
# Wed, 12 Nov 2025 00:27:07 GMT
USER 1000
# Wed, 12 Nov 2025 00:27:07 GMT
EXPOSE map[5044/tcp:{} 9600/tcp:{}]
# Wed, 12 Nov 2025 00:27:07 GMT
LABEL org.label-schema.build-date=2025-11-04T18:22:56+00:00 org.label-schema.license=Elastic License org.label-schema.name=logstash org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/logstash org.label-schema.vcs-url=https://github.com/elastic/logstash org.label-schema.vendor=Elastic org.label-schema.version=9.2.1 org.opencontainers.image.created=2025-11-04T18:22:56+00:00 org.opencontainers.image.description=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' org.opencontainers.image.licenses=Elastic License org.opencontainers.image.title=logstash org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=9.2.1 description=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' license=Elastic License maintainer=info@elastic.co name=logstash summary=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' vendor=Elastic
# Wed, 12 Nov 2025 00:27:07 GMT
ENTRYPOINT ["/usr/local/bin/docker-entrypoint"]
```

-	Layers:
	-	`sha256:fccdcd3fc47f898d65f9d4531d01539ce33a7ec8038500d557bfe58eb4b6ae87`  
		Last Modified: Tue, 11 Nov 2025 18:10:59 GMT  
		Size: 38.2 MB (38211473 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f71e8a4753d23ce5c4edb4cf20502bce845d035ecbd804614e6f7268bf721692`  
		Last Modified: Wed, 12 Nov 2025 00:28:01 GMT  
		Size: 5.1 MB (5146000 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01cdfe89646a6e9f15e3c553c17c9003fc14f66b4f4a0085578521532f8dc09f`  
		Last Modified: Wed, 12 Nov 2025 03:45:53 GMT  
		Size: 438.9 MB (438905507 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d2a66c53a9834d2f7229e0f47b440d89b7ba5ec48fe8f86f865fcfc53abbf2f`  
		Last Modified: Wed, 12 Nov 2025 00:28:01 GMT  
		Size: 1.9 MB (1926841 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9664d17e33434912de0ef9c93f2d55cecd0d16e2709675e350eaaa0820f18f8b`  
		Last Modified: Wed, 12 Nov 2025 00:28:01 GMT  
		Size: 1.6 KB (1577 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2a64375614f691df0a2b3a78bb0ce9943dc1d8295572386544b93961e3d1b7b`  
		Last Modified: Wed, 12 Nov 2025 00:28:01 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2735a09509afdffa27e70b2121a3093d85adf24acc577e166e5d21050ee48805`  
		Last Modified: Wed, 12 Nov 2025 00:28:01 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6daedee833f79500e54efa9ffe98c90ab667f263c0f2d9406415bb41945c45a`  
		Last Modified: Wed, 12 Nov 2025 00:28:01 GMT  
		Size: 711.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `logstash:9.2.1` - unknown; unknown

```console
$ docker pull logstash@sha256:66afc028b57fa6b036098e91cd404a92ebba724ebff4613e3c394f4b129f9a48
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2130649 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a791a8c7edf9b0d91e847a98a82cb6d6836175f21545442062ea42be0f293c27`

```dockerfile
```

-	Layers:
	-	`sha256:4ae066810895bc322403d8f6c18b67188bc1753246a08c8ec916d34b66c7e408`  
		Last Modified: Wed, 12 Nov 2025 09:37:19 GMT  
		Size: 2.1 MB (2100932 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f62b29df92a64c940a23f95d2b4997d33d636bba55cae436318e1d84bdf034a9`  
		Last Modified: Wed, 12 Nov 2025 09:37:18 GMT  
		Size: 29.7 KB (29717 bytes)  
		MIME: application/vnd.in-toto+json
