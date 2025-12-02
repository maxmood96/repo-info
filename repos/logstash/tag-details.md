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
$ docker pull logstash@sha256:5ad8d7a4f75b28434d970146930e8301060ba8efd1d2f312f3c241483e1ed31e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `logstash:9.1.7` - linux; amd64

```console
$ docker pull logstash@sha256:8e815c2dca8d2dc15361fae8d26cec79fb800c00bed2dc5dbd32034a6c9df948
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **477.6 MB (477605170 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:31c6f59e36e1586ec3a5d1accc831c80dc2cb17b60060531650166396e135737`
-	Entrypoint: `["\/usr\/local\/bin\/docker-entrypoint"]`

```dockerfile
# Mon, 01 Dec 2025 08:46:04 GMT
LABEL maintainer="Red Hat, Inc."
# Mon, 01 Dec 2025 08:46:04 GMT
LABEL vendor="Red Hat, Inc."
# Mon, 01 Dec 2025 08:46:04 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Mon, 01 Dec 2025 08:46:04 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.7"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Mon, 01 Dec 2025 08:46:04 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Mon, 01 Dec 2025 08:46:04 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Mon, 01 Dec 2025 08:46:04 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 01 Dec 2025 08:46:04 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 01 Dec 2025 08:46:04 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Mon, 01 Dec 2025 08:46:04 GMT
LABEL io.openshift.expose-services=""
# Mon, 01 Dec 2025 08:46:04 GMT
LABEL io.openshift.tags="minimal rhel9"
# Mon, 01 Dec 2025 08:46:04 GMT
ENV container oci
# Mon, 01 Dec 2025 08:46:05 GMT
COPY dir:9e1be6ea7c9ab655dce87115dc5a86f74430f6cce27de363947899ca9c40a12b in /      
# Mon, 01 Dec 2025 08:46:05 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Mon, 01 Dec 2025 08:46:05 GMT
CMD ["/bin/bash"]
# Mon, 01 Dec 2025 08:46:05 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /usr/share/buildinfo/content-sets.json      
# Mon, 01 Dec 2025 08:46:05 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /root/buildinfo/content_manifests/content-sets.json      
# Mon, 01 Dec 2025 08:46:05 GMT
COPY file:b2d99215ad0f777fc208a0abcf88392b89d81310198466ef08702f0413990c72 in /usr/share/buildinfo/labels.json      
# Mon, 01 Dec 2025 08:46:06 GMT
COPY file:b2d99215ad0f777fc208a0abcf88392b89d81310198466ef08702f0413990c72 in /root/buildinfo/labels.json      
# Mon, 01 Dec 2025 08:46:06 GMT
LABEL "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="aa778ff26f397863d5f50a6cf5f17a2343e5a626" "org.opencontainers.image.revision"="aa778ff26f397863d5f50a6cf5f17a2343e5a626" "build-date"="2025-12-01T08:45:48Z" "org.opencontainers.image.created"="2025-12-01T08:45:48Z" "release"="1764578379"org.opencontainers.image.revision=aa778ff26f397863d5f50a6cf5f17a2343e5a626,org.opencontainers.image.created=2025-12-01T08:45:48Z
# Tue, 02 Dec 2025 00:42:16 GMT
ENV ELASTIC_CONTAINER=true
# Tue, 02 Dec 2025 00:42:16 GMT
ENV PATH=/usr/share/logstash/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Dec 2025 00:42:16 GMT
ENV LANG=C.UTF-8 LC_ALL=C.UTF-8
# Tue, 02 Dec 2025 00:42:16 GMT
WORKDIR /usr/share
# Tue, 02 Dec 2025 00:42:24 GMT
RUN microdnf install -y procps findutils tar gzip &&   microdnf install -y openssl &&   microdnf install -y which shadow-utils &&   microdnf clean all # buildkit
# Tue, 02 Dec 2025 00:43:21 GMT
RUN groupadd --gid 1000 logstash &&   adduser --uid 1000 --gid 1000   --home "/usr/share/logstash"   --no-create-home   logstash &&   arch="$(rpm --query --queryformat='%{ARCH}' rpm)" &&   curl -f -Lo logstash.tar.gz https://artifacts.elastic.co/downloads/logstash/logstash-9.1.7-linux-${arch}.tar.gz &&   tar -zxf logstash.tar.gz -C /usr/share &&   rm logstash.tar.gz &&   mv /usr/share/logstash-9.1.7 /usr/share/logstash &&   chown -R logstash:root /usr/share/logstash &&   chmod -R g=u /usr/share/logstash &&   mkdir /licenses &&   mv /usr/share/logstash/NOTICE.TXT /licenses/NOTICE.TXT &&   mv /usr/share/logstash/LICENSE.txt /licenses/LICENSE.txt &&   find /usr/share/logstash -type d -exec chmod g+s {} \; &&   ln -s /usr/share/logstash /opt/logstash # buildkit
# Tue, 02 Dec 2025 00:43:21 GMT
COPY /tmp/go/src/env2yaml/env2yaml /usr/local/bin/env2yaml # buildkit
# Tue, 02 Dec 2025 00:43:21 GMT
COPY --chown=logstash:root config/pipelines.yml config/log4j2.properties config/log4j2.file.properties /usr/share/logstash/config/ # buildkit
# Tue, 02 Dec 2025 00:43:21 GMT
COPY --chown=logstash:root config/logstash-full.yml /usr/share/logstash/config/logstash.yml # buildkit
# Tue, 02 Dec 2025 00:43:21 GMT
COPY --chown=logstash:root pipeline/default.conf /usr/share/logstash/pipeline/logstash.conf # buildkit
# Tue, 02 Dec 2025 00:43:21 GMT
COPY --chmod=0755 bin/docker-entrypoint /usr/local/bin/ # buildkit
# Tue, 02 Dec 2025 00:43:21 GMT
WORKDIR /usr/share/logstash
# Tue, 02 Dec 2025 00:43:21 GMT
USER 1000
# Tue, 02 Dec 2025 00:43:21 GMT
EXPOSE map[5044/tcp:{} 9600/tcp:{}]
# Tue, 02 Dec 2025 00:43:21 GMT
LABEL org.label-schema.build-date=2025-11-04T18:24:06+00:00 org.label-schema.license=Elastic License org.label-schema.name=logstash org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/logstash org.label-schema.vcs-url=https://github.com/elastic/logstash org.label-schema.vendor=Elastic org.label-schema.version=9.1.7 org.opencontainers.image.created=2025-11-04T18:24:06+00:00 org.opencontainers.image.description=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' org.opencontainers.image.licenses=Elastic License org.opencontainers.image.title=logstash org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=9.1.7 description=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' license=Elastic License maintainer=info@elastic.co name=logstash summary=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' vendor=Elastic
# Tue, 02 Dec 2025 00:43:21 GMT
ENTRYPOINT ["/usr/local/bin/docker-entrypoint"]
```

-	Layers:
	-	`sha256:e33884b9ee6fd9f34b4688c1f3f27e3a36be1a8633a805f0780dcfa23073efcb`  
		Last Modified: Mon, 01 Dec 2025 09:26:00 GMT  
		Size: 40.0 MB (40040081 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:240efa1e7d59dd6e68f23d61b761bcabcac8f2addb61ba6b57ba4f611fd2e264`  
		Last Modified: Tue, 02 Dec 2025 00:44:08 GMT  
		Size: 5.2 MB (5154072 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9c649ad1b46806bdd52051bb89bb7f02c3a1f984616ce0170e9604ebe836293`  
		Last Modified: Tue, 02 Dec 2025 00:44:02 GMT  
		Size: 430.3 MB (430329274 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f359f90aa40025a21b6e8202deec14cf50ba677fe77a9b45e4b991431ac9ceb`  
		Last Modified: Tue, 02 Dec 2025 00:44:08 GMT  
		Size: 2.1 MB (2078841 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2fc494ad842290bb45f404e1b5a1c6308f3991eda1f0949b07d7384fbe5301e6`  
		Last Modified: Tue, 02 Dec 2025 00:44:08 GMT  
		Size: 1.6 KB (1575 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21a422e8536b02ea72a5270d6270a6e7c171b1c04bcf986248528f1252a0c5b7`  
		Last Modified: Tue, 02 Dec 2025 00:44:08 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f62c1c3f514fd259cb752627dfe171b1e0ad8fb9951ef21deb2d7d700e74c73d`  
		Last Modified: Tue, 02 Dec 2025 00:44:08 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b73c6d622c408dfa9667c906cd4ed4b7df34c5e157ccec29bcec6aad1bb1cbc7`  
		Last Modified: Tue, 02 Dec 2025 00:44:08 GMT  
		Size: 711.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `logstash:9.1.7` - unknown; unknown

```console
$ docker pull logstash@sha256:559ee78fa57ba4ca47ef9d0c6f16ab8c4d30f82b1b9b8c822970542d0b9c9c75
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2120112 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:314ee4a62698be8aa8388e93349b94ff7b4c13fa392221fe250ede562c76ae0f`

```dockerfile
```

-	Layers:
	-	`sha256:e822a9a323cc3ddfaf0c99b39a69c7644253de7726daac71334cdab2de0a37cc`  
		Last Modified: Tue, 02 Dec 2025 01:54:21 GMT  
		Size: 2.1 MB (2090558 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1f5cce4ec6615229439fbdfc6ab540cd2e1feb583785d696f1cb07d3678a006e`  
		Last Modified: Tue, 02 Dec 2025 01:54:22 GMT  
		Size: 29.6 KB (29554 bytes)  
		MIME: application/vnd.in-toto+json

### `logstash:9.1.7` - linux; arm64 variant v8

```console
$ docker pull logstash@sha256:932db91e2d0683d954528c9d95e7e8a9b66af5891035208efd36551c38983474
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **473.9 MB (473907946 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a92710ffc12883e08a4eaf66a8be73886fd83378ed5d98f0273525f1a1bcbb57`
-	Entrypoint: `["\/usr\/local\/bin\/docker-entrypoint"]`

```dockerfile
# Mon, 01 Dec 2025 08:45:36 GMT
LABEL maintainer="Red Hat, Inc."
# Mon, 01 Dec 2025 08:45:36 GMT
LABEL vendor="Red Hat, Inc."
# Mon, 01 Dec 2025 08:45:36 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Mon, 01 Dec 2025 08:45:36 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.7"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Mon, 01 Dec 2025 08:45:36 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Mon, 01 Dec 2025 08:45:36 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Mon, 01 Dec 2025 08:45:36 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 01 Dec 2025 08:45:36 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 01 Dec 2025 08:45:36 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Mon, 01 Dec 2025 08:45:36 GMT
LABEL io.openshift.expose-services=""
# Mon, 01 Dec 2025 08:45:36 GMT
LABEL io.openshift.tags="minimal rhel9"
# Mon, 01 Dec 2025 08:45:36 GMT
ENV container oci
# Mon, 01 Dec 2025 08:45:37 GMT
COPY dir:0300512c6394db4e597803fcc03b9993a2a4c4d9c6e4eb31c5a64534316ae291 in /      
# Mon, 01 Dec 2025 08:45:37 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Mon, 01 Dec 2025 08:45:37 GMT
CMD ["/bin/bash"]
# Mon, 01 Dec 2025 08:45:37 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /usr/share/buildinfo/content-sets.json      
# Mon, 01 Dec 2025 08:45:37 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /root/buildinfo/content_manifests/content-sets.json      
# Mon, 01 Dec 2025 08:45:37 GMT
COPY file:9ba4e215cc648b0ee2f7a9114145896fc716da8ab330689b6c8358fccff02c52 in /usr/share/buildinfo/labels.json      
# Mon, 01 Dec 2025 08:45:37 GMT
COPY file:9ba4e215cc648b0ee2f7a9114145896fc716da8ab330689b6c8358fccff02c52 in /root/buildinfo/labels.json      
# Mon, 01 Dec 2025 08:45:38 GMT
LABEL "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="aa778ff26f397863d5f50a6cf5f17a2343e5a626" "org.opencontainers.image.revision"="aa778ff26f397863d5f50a6cf5f17a2343e5a626" "build-date"="2025-12-01T08:45:20Z" "org.opencontainers.image.created"="2025-12-01T08:45:20Z" "release"="1764578379"org.opencontainers.image.revision=aa778ff26f397863d5f50a6cf5f17a2343e5a626,org.opencontainers.image.created=2025-12-01T08:45:20Z
# Tue, 02 Dec 2025 00:47:47 GMT
ENV ELASTIC_CONTAINER=true
# Tue, 02 Dec 2025 00:47:47 GMT
ENV PATH=/usr/share/logstash/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Dec 2025 00:47:47 GMT
ENV LANG=C.UTF-8 LC_ALL=C.UTF-8
# Tue, 02 Dec 2025 00:47:47 GMT
WORKDIR /usr/share
# Tue, 02 Dec 2025 00:47:57 GMT
RUN microdnf install -y procps findutils tar gzip &&   microdnf install -y openssl &&   microdnf install -y which shadow-utils &&   microdnf clean all # buildkit
# Tue, 02 Dec 2025 00:48:48 GMT
RUN groupadd --gid 1000 logstash &&   adduser --uid 1000 --gid 1000   --home "/usr/share/logstash"   --no-create-home   logstash &&   arch="$(rpm --query --queryformat='%{ARCH}' rpm)" &&   curl -f -Lo logstash.tar.gz https://artifacts.elastic.co/downloads/logstash/logstash-9.1.7-linux-${arch}.tar.gz &&   tar -zxf logstash.tar.gz -C /usr/share &&   rm logstash.tar.gz &&   mv /usr/share/logstash-9.1.7 /usr/share/logstash &&   chown -R logstash:root /usr/share/logstash &&   chmod -R g=u /usr/share/logstash &&   mkdir /licenses &&   mv /usr/share/logstash/NOTICE.TXT /licenses/NOTICE.TXT &&   mv /usr/share/logstash/LICENSE.txt /licenses/LICENSE.txt &&   find /usr/share/logstash -type d -exec chmod g+s {} \; &&   ln -s /usr/share/logstash /opt/logstash # buildkit
# Tue, 02 Dec 2025 00:48:48 GMT
COPY /tmp/go/src/env2yaml/env2yaml /usr/local/bin/env2yaml # buildkit
# Tue, 02 Dec 2025 00:48:48 GMT
COPY --chown=logstash:root config/pipelines.yml config/log4j2.properties config/log4j2.file.properties /usr/share/logstash/config/ # buildkit
# Tue, 02 Dec 2025 00:48:48 GMT
COPY --chown=logstash:root config/logstash-full.yml /usr/share/logstash/config/logstash.yml # buildkit
# Tue, 02 Dec 2025 00:48:48 GMT
COPY --chown=logstash:root pipeline/default.conf /usr/share/logstash/pipeline/logstash.conf # buildkit
# Tue, 02 Dec 2025 00:48:48 GMT
COPY --chmod=0755 bin/docker-entrypoint /usr/local/bin/ # buildkit
# Tue, 02 Dec 2025 00:48:49 GMT
WORKDIR /usr/share/logstash
# Tue, 02 Dec 2025 00:48:49 GMT
USER 1000
# Tue, 02 Dec 2025 00:48:49 GMT
EXPOSE map[5044/tcp:{} 9600/tcp:{}]
# Tue, 02 Dec 2025 00:48:49 GMT
LABEL org.label-schema.build-date=2025-11-04T18:24:06+00:00 org.label-schema.license=Elastic License org.label-schema.name=logstash org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/logstash org.label-schema.vcs-url=https://github.com/elastic/logstash org.label-schema.vendor=Elastic org.label-schema.version=9.1.7 org.opencontainers.image.created=2025-11-04T18:24:06+00:00 org.opencontainers.image.description=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' org.opencontainers.image.licenses=Elastic License org.opencontainers.image.title=logstash org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=9.1.7 description=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' license=Elastic License maintainer=info@elastic.co name=logstash summary=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' vendor=Elastic
# Tue, 02 Dec 2025 00:48:49 GMT
ENTRYPOINT ["/usr/local/bin/docker-entrypoint"]
```

-	Layers:
	-	`sha256:2318060655d9ba0a61831256291e1482c38f67e2e0879a90ccd9008c0ed03b36`  
		Last Modified: Mon, 01 Dec 2025 12:11:26 GMT  
		Size: 38.2 MB (38221706 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0145cc7bbce88dad33c18dc58d5f56b5084ca46ac019c4001263f8e44db9ee26`  
		Last Modified: Tue, 02 Dec 2025 00:49:45 GMT  
		Size: 5.2 MB (5154538 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c02301a022b39fd26a8bc52bfb2ff4f180873da90e6dfeb4e5ab2d250c1cdb8d`  
		Last Modified: Tue, 02 Dec 2025 00:49:38 GMT  
		Size: 428.6 MB (428601938 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12479a2f026893b3a2eef7b3c24142a4aaa47df5f2713f11346746f51723b49f`  
		Last Modified: Tue, 02 Dec 2025 00:49:45 GMT  
		Size: 1.9 MB (1926859 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67eddd1244dde59329a33cff6c8708b3d3356f9e6c7e884ded60e2376430db0d`  
		Last Modified: Tue, 02 Dec 2025 00:49:44 GMT  
		Size: 1.6 KB (1577 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72b3b6fac005c7ef83211d92be9f7384d88dfc817d57d771e9f9d4d189249bd6`  
		Last Modified: Tue, 02 Dec 2025 00:49:44 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6e7ef9aae0537cef05dba1e921335035cda62e69184fad41efe64228cf7cd43`  
		Last Modified: Tue, 02 Dec 2025 00:49:44 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9a590a9ceab9b5f8a08f94b50e1cbe25e82a5e9290b353a98b57a2930e5b954`  
		Last Modified: Tue, 02 Dec 2025 00:49:44 GMT  
		Size: 712.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `logstash:9.1.7` - unknown; unknown

```console
$ docker pull logstash@sha256:e104238e19c7d4e2fc492e4501ed2075d0ce03890b06deb169b9cff2e38f4852
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2120799 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:39afa5772edc1b45672d4df4c7a20303f3d863ab90ab82b21d8176ad866ee512`

```dockerfile
```

-	Layers:
	-	`sha256:6b87a9b4d47feb4d03edd95212a86e5e869cb99f7e0ee9a445e9698b3c1ca3d8`  
		Last Modified: Tue, 02 Dec 2025 01:54:26 GMT  
		Size: 2.1 MB (2091128 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d2f718cbf7e1111bfadea1671d596b7e6d4da4a7a95e82d0b41e3687efe660cc`  
		Last Modified: Tue, 02 Dec 2025 01:54:27 GMT  
		Size: 29.7 KB (29671 bytes)  
		MIME: application/vnd.in-toto+json

## `logstash:9.2.1`

```console
$ docker pull logstash@sha256:17daf87e4502cb831425d0b19c843e91f6fdeed54d019189b91d7d06a58b5e98
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `logstash:9.2.1` - linux; amd64

```console
$ docker pull logstash@sha256:005759b50643c1d3d445bdc2ca2b3adf655e3c7083a47e7c891192aa26a695b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **487.9 MB (487908123 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:50cd6258cbbde0b701ef49ea716134f7f4623144e3ee8aca9b595cb9203565d9`
-	Entrypoint: `["\/usr\/local\/bin\/docker-entrypoint"]`

```dockerfile
# Mon, 01 Dec 2025 08:46:04 GMT
LABEL maintainer="Red Hat, Inc."
# Mon, 01 Dec 2025 08:46:04 GMT
LABEL vendor="Red Hat, Inc."
# Mon, 01 Dec 2025 08:46:04 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Mon, 01 Dec 2025 08:46:04 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.7"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Mon, 01 Dec 2025 08:46:04 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Mon, 01 Dec 2025 08:46:04 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Mon, 01 Dec 2025 08:46:04 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 01 Dec 2025 08:46:04 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 01 Dec 2025 08:46:04 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Mon, 01 Dec 2025 08:46:04 GMT
LABEL io.openshift.expose-services=""
# Mon, 01 Dec 2025 08:46:04 GMT
LABEL io.openshift.tags="minimal rhel9"
# Mon, 01 Dec 2025 08:46:04 GMT
ENV container oci
# Mon, 01 Dec 2025 08:46:05 GMT
COPY dir:9e1be6ea7c9ab655dce87115dc5a86f74430f6cce27de363947899ca9c40a12b in /      
# Mon, 01 Dec 2025 08:46:05 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Mon, 01 Dec 2025 08:46:05 GMT
CMD ["/bin/bash"]
# Mon, 01 Dec 2025 08:46:05 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /usr/share/buildinfo/content-sets.json      
# Mon, 01 Dec 2025 08:46:05 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /root/buildinfo/content_manifests/content-sets.json      
# Mon, 01 Dec 2025 08:46:05 GMT
COPY file:b2d99215ad0f777fc208a0abcf88392b89d81310198466ef08702f0413990c72 in /usr/share/buildinfo/labels.json      
# Mon, 01 Dec 2025 08:46:06 GMT
COPY file:b2d99215ad0f777fc208a0abcf88392b89d81310198466ef08702f0413990c72 in /root/buildinfo/labels.json      
# Mon, 01 Dec 2025 08:46:06 GMT
LABEL "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="aa778ff26f397863d5f50a6cf5f17a2343e5a626" "org.opencontainers.image.revision"="aa778ff26f397863d5f50a6cf5f17a2343e5a626" "build-date"="2025-12-01T08:45:48Z" "org.opencontainers.image.created"="2025-12-01T08:45:48Z" "release"="1764578379"org.opencontainers.image.revision=aa778ff26f397863d5f50a6cf5f17a2343e5a626,org.opencontainers.image.created=2025-12-01T08:45:48Z
# Tue, 02 Dec 2025 00:42:30 GMT
ENV ELASTIC_CONTAINER=true
# Tue, 02 Dec 2025 00:42:30 GMT
ENV PATH=/usr/share/logstash/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Dec 2025 00:42:30 GMT
ENV LANG=C.UTF-8 LC_ALL=C.UTF-8
# Tue, 02 Dec 2025 00:42:30 GMT
WORKDIR /usr/share
# Tue, 02 Dec 2025 00:42:37 GMT
RUN microdnf install -y procps findutils tar gzip &&   microdnf install -y openssl &&   microdnf install -y which shadow-utils &&   microdnf clean all # buildkit
# Tue, 02 Dec 2025 00:43:22 GMT
RUN groupadd --gid 1000 logstash &&   adduser --uid 1000 --gid 1000   --home "/usr/share/logstash"   --no-create-home   logstash &&   arch="$(rpm --query --queryformat='%{ARCH}' rpm)" &&   curl --fail --location --output logstash.tar.gz https://artifacts.elastic.co/downloads/logstash/logstash-9.2.1-linux-${arch}.tar.gz &&   tar -zxf logstash.tar.gz -C /usr/share &&   rm logstash.tar.gz &&   mv /usr/share/logstash-9.2.1 /usr/share/logstash &&   chown -R logstash:root /usr/share/logstash &&   chmod -R g=u /usr/share/logstash &&   mkdir /licenses &&   mv /usr/share/logstash/NOTICE.TXT /licenses/NOTICE.TXT &&   mv /usr/share/logstash/LICENSE.txt /licenses/LICENSE.txt &&   find /usr/share/logstash -type d -exec chmod g+s {} \; &&   ln -s /usr/share/logstash /opt/logstash # buildkit
# Tue, 02 Dec 2025 00:43:22 GMT
COPY /tmp/go/src/env2yaml/env2yaml /usr/local/bin/env2yaml # buildkit
# Tue, 02 Dec 2025 00:43:22 GMT
COPY --chown=logstash:root config/pipelines.yml config/log4j2.properties config/log4j2.file.properties /usr/share/logstash/config/ # buildkit
# Tue, 02 Dec 2025 00:43:22 GMT
COPY --chown=logstash:root config/logstash-full.yml /usr/share/logstash/config/logstash.yml # buildkit
# Tue, 02 Dec 2025 00:43:22 GMT
COPY --chown=logstash:root pipeline/default.conf /usr/share/logstash/pipeline/logstash.conf # buildkit
# Tue, 02 Dec 2025 00:43:22 GMT
COPY --chmod=0755 bin/docker-entrypoint /usr/local/bin/ # buildkit
# Tue, 02 Dec 2025 00:43:22 GMT
WORKDIR /usr/share/logstash
# Tue, 02 Dec 2025 00:43:22 GMT
USER 1000
# Tue, 02 Dec 2025 00:43:22 GMT
EXPOSE map[5044/tcp:{} 9600/tcp:{}]
# Tue, 02 Dec 2025 00:43:22 GMT
LABEL org.label-schema.build-date=2025-11-04T18:22:56+00:00 org.label-schema.license=Elastic License org.label-schema.name=logstash org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/logstash org.label-schema.vcs-url=https://github.com/elastic/logstash org.label-schema.vendor=Elastic org.label-schema.version=9.2.1 org.opencontainers.image.created=2025-11-04T18:22:56+00:00 org.opencontainers.image.description=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' org.opencontainers.image.licenses=Elastic License org.opencontainers.image.title=logstash org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=9.2.1 description=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' license=Elastic License maintainer=info@elastic.co name=logstash summary=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' vendor=Elastic
# Tue, 02 Dec 2025 00:43:22 GMT
ENTRYPOINT ["/usr/local/bin/docker-entrypoint"]
```

-	Layers:
	-	`sha256:e33884b9ee6fd9f34b4688c1f3f27e3a36be1a8633a805f0780dcfa23073efcb`  
		Last Modified: Mon, 01 Dec 2025 09:26:00 GMT  
		Size: 40.0 MB (40040081 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fff6670941d9cd66f54852d233dd3122fef18026344019743d71f3d419b729a9`  
		Last Modified: Tue, 02 Dec 2025 00:44:47 GMT  
		Size: 5.2 MB (5154104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36a88724d35ec5d22ab7aa519858b3a249b014105c5ccf803626dc1e6f48820e`  
		Last Modified: Tue, 02 Dec 2025 02:02:06 GMT  
		Size: 440.6 MB (440632203 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96ea11cf2ef5988a12c363fab34b00c322c7141e887711df8812fe1e60aaeebf`  
		Last Modified: Tue, 02 Dec 2025 00:44:47 GMT  
		Size: 2.1 MB (2078832 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a6f79293b54ba2d9e3703c40d869d534733cf3557b149c2edecbae7f8f41ebc`  
		Last Modified: Tue, 02 Dec 2025 00:44:47 GMT  
		Size: 1.6 KB (1577 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1290d16fd7a6c3a756e8d7fa2ad1959679af937e719beb86b4b027140b3cc494`  
		Last Modified: Tue, 02 Dec 2025 00:44:47 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db296f95b68f2d86fcab090223ae694e13c1b8f547a52eed757c3163148e3476`  
		Last Modified: Tue, 02 Dec 2025 00:44:47 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a6ae6e5fef6e8d860f7340b4323b7fc178f29bfb6762fef3aa204cf00514f31`  
		Last Modified: Tue, 02 Dec 2025 00:44:47 GMT  
		Size: 711.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `logstash:9.2.1` - unknown; unknown

```console
$ docker pull logstash@sha256:b7c682e090f3a55fffd1ced7390fcf1efd40ea490634621a7cc962eec4068b8a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2129979 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dbebb1c8eb3709d16dd92f8459cc2e1086e20a924e67a08d831ba875a5202be8`

```dockerfile
```

-	Layers:
	-	`sha256:fc3182bcce3ad60f12efbb575e06f26cdf60ed8a5b1b2cec19670a40f69477fa`  
		Last Modified: Tue, 02 Dec 2025 01:54:30 GMT  
		Size: 2.1 MB (2100378 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d6535b3eeb393a5f957471457d555c64f54f2b9a9fe75c69dfaea5a653e42f2d`  
		Last Modified: Tue, 02 Dec 2025 01:54:31 GMT  
		Size: 29.6 KB (29601 bytes)  
		MIME: application/vnd.in-toto+json

### `logstash:9.2.1` - linux; arm64 variant v8

```console
$ docker pull logstash@sha256:a142112b17591dee8d771cc31f455d8f127b4aebd7dd17cbd1e56f05b608155b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **484.2 MB (484211086 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:222795d6cd988860cf7316140f6762365ba323f4b584359e56770818bb967a7b`
-	Entrypoint: `["\/usr\/local\/bin\/docker-entrypoint"]`

```dockerfile
# Mon, 01 Dec 2025 08:45:36 GMT
LABEL maintainer="Red Hat, Inc."
# Mon, 01 Dec 2025 08:45:36 GMT
LABEL vendor="Red Hat, Inc."
# Mon, 01 Dec 2025 08:45:36 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Mon, 01 Dec 2025 08:45:36 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.7"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Mon, 01 Dec 2025 08:45:36 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Mon, 01 Dec 2025 08:45:36 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Mon, 01 Dec 2025 08:45:36 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 01 Dec 2025 08:45:36 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 01 Dec 2025 08:45:36 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Mon, 01 Dec 2025 08:45:36 GMT
LABEL io.openshift.expose-services=""
# Mon, 01 Dec 2025 08:45:36 GMT
LABEL io.openshift.tags="minimal rhel9"
# Mon, 01 Dec 2025 08:45:36 GMT
ENV container oci
# Mon, 01 Dec 2025 08:45:37 GMT
COPY dir:0300512c6394db4e597803fcc03b9993a2a4c4d9c6e4eb31c5a64534316ae291 in /      
# Mon, 01 Dec 2025 08:45:37 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Mon, 01 Dec 2025 08:45:37 GMT
CMD ["/bin/bash"]
# Mon, 01 Dec 2025 08:45:37 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /usr/share/buildinfo/content-sets.json      
# Mon, 01 Dec 2025 08:45:37 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /root/buildinfo/content_manifests/content-sets.json      
# Mon, 01 Dec 2025 08:45:37 GMT
COPY file:9ba4e215cc648b0ee2f7a9114145896fc716da8ab330689b6c8358fccff02c52 in /usr/share/buildinfo/labels.json      
# Mon, 01 Dec 2025 08:45:37 GMT
COPY file:9ba4e215cc648b0ee2f7a9114145896fc716da8ab330689b6c8358fccff02c52 in /root/buildinfo/labels.json      
# Mon, 01 Dec 2025 08:45:38 GMT
LABEL "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="aa778ff26f397863d5f50a6cf5f17a2343e5a626" "org.opencontainers.image.revision"="aa778ff26f397863d5f50a6cf5f17a2343e5a626" "build-date"="2025-12-01T08:45:20Z" "org.opencontainers.image.created"="2025-12-01T08:45:20Z" "release"="1764578379"org.opencontainers.image.revision=aa778ff26f397863d5f50a6cf5f17a2343e5a626,org.opencontainers.image.created=2025-12-01T08:45:20Z
# Tue, 02 Dec 2025 00:47:55 GMT
ENV ELASTIC_CONTAINER=true
# Tue, 02 Dec 2025 00:47:55 GMT
ENV PATH=/usr/share/logstash/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Dec 2025 00:47:55 GMT
ENV LANG=C.UTF-8 LC_ALL=C.UTF-8
# Tue, 02 Dec 2025 00:47:55 GMT
WORKDIR /usr/share
# Tue, 02 Dec 2025 00:48:05 GMT
RUN microdnf install -y procps findutils tar gzip &&   microdnf install -y openssl &&   microdnf install -y which shadow-utils &&   microdnf clean all # buildkit
# Tue, 02 Dec 2025 00:48:50 GMT
RUN groupadd --gid 1000 logstash &&   adduser --uid 1000 --gid 1000   --home "/usr/share/logstash"   --no-create-home   logstash &&   arch="$(rpm --query --queryformat='%{ARCH}' rpm)" &&   curl --fail --location --output logstash.tar.gz https://artifacts.elastic.co/downloads/logstash/logstash-9.2.1-linux-${arch}.tar.gz &&   tar -zxf logstash.tar.gz -C /usr/share &&   rm logstash.tar.gz &&   mv /usr/share/logstash-9.2.1 /usr/share/logstash &&   chown -R logstash:root /usr/share/logstash &&   chmod -R g=u /usr/share/logstash &&   mkdir /licenses &&   mv /usr/share/logstash/NOTICE.TXT /licenses/NOTICE.TXT &&   mv /usr/share/logstash/LICENSE.txt /licenses/LICENSE.txt &&   find /usr/share/logstash -type d -exec chmod g+s {} \; &&   ln -s /usr/share/logstash /opt/logstash # buildkit
# Tue, 02 Dec 2025 00:48:50 GMT
COPY /tmp/go/src/env2yaml/env2yaml /usr/local/bin/env2yaml # buildkit
# Tue, 02 Dec 2025 00:48:51 GMT
COPY --chown=logstash:root config/pipelines.yml config/log4j2.properties config/log4j2.file.properties /usr/share/logstash/config/ # buildkit
# Tue, 02 Dec 2025 00:48:51 GMT
COPY --chown=logstash:root config/logstash-full.yml /usr/share/logstash/config/logstash.yml # buildkit
# Tue, 02 Dec 2025 00:48:51 GMT
COPY --chown=logstash:root pipeline/default.conf /usr/share/logstash/pipeline/logstash.conf # buildkit
# Tue, 02 Dec 2025 00:48:51 GMT
COPY --chmod=0755 bin/docker-entrypoint /usr/local/bin/ # buildkit
# Tue, 02 Dec 2025 00:48:51 GMT
WORKDIR /usr/share/logstash
# Tue, 02 Dec 2025 00:48:51 GMT
USER 1000
# Tue, 02 Dec 2025 00:48:51 GMT
EXPOSE map[5044/tcp:{} 9600/tcp:{}]
# Tue, 02 Dec 2025 00:48:51 GMT
LABEL org.label-schema.build-date=2025-11-04T18:22:56+00:00 org.label-schema.license=Elastic License org.label-schema.name=logstash org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/logstash org.label-schema.vcs-url=https://github.com/elastic/logstash org.label-schema.vendor=Elastic org.label-schema.version=9.2.1 org.opencontainers.image.created=2025-11-04T18:22:56+00:00 org.opencontainers.image.description=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' org.opencontainers.image.licenses=Elastic License org.opencontainers.image.title=logstash org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=9.2.1 description=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' license=Elastic License maintainer=info@elastic.co name=logstash summary=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' vendor=Elastic
# Tue, 02 Dec 2025 00:48:51 GMT
ENTRYPOINT ["/usr/local/bin/docker-entrypoint"]
```

-	Layers:
	-	`sha256:2318060655d9ba0a61831256291e1482c38f67e2e0879a90ccd9008c0ed03b36`  
		Last Modified: Mon, 01 Dec 2025 12:11:26 GMT  
		Size: 38.2 MB (38221706 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a88994b72fdb795940784cb31116b0057b8ad86e822f7e7e7847c8bcaa2dfb50`  
		Last Modified: Tue, 02 Dec 2025 00:49:49 GMT  
		Size: 5.2 MB (5154600 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:847ebfb1a6c6ba4e7d96701e58583f128d43690eeaa6eb122852da4698150a86`  
		Last Modified: Tue, 02 Dec 2025 00:49:43 GMT  
		Size: 438.9 MB (438905035 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f15a046cbc53d1525fca595537c9315e051700b2854568c88975c3c3c9c5086`  
		Last Modified: Tue, 02 Dec 2025 00:49:48 GMT  
		Size: 1.9 MB (1926841 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb304647041d343c249325eaea55c8fc490746fe41d19bcf9bf38d62b777693c`  
		Last Modified: Tue, 02 Dec 2025 00:49:48 GMT  
		Size: 1.6 KB (1576 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c79028bdabc82780becbcd4ad36d1aa9b0d9710ee174cd2a95355795c820694b`  
		Last Modified: Tue, 02 Dec 2025 00:49:48 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c40d7b182e0a6f2b402494e46a3a3a0a70610a765fc9d03590eddd515bef138`  
		Last Modified: Tue, 02 Dec 2025 00:49:48 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a3fedecb19c95d9ce20d5235c1d973579120b3ca3521efe378f02cab5e287c0`  
		Last Modified: Tue, 02 Dec 2025 00:49:48 GMT  
		Size: 711.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `logstash:9.2.1` - unknown; unknown

```console
$ docker pull logstash@sha256:9de0b78305d6fbcaa2afe6c52ffb5717f5a6058701fa8c441bf711d1608fc93a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2130667 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:48669742bd8994df07a3324cfc11caeba25a18fa7f1f4c9f01d04bcbce01ad58`

```dockerfile
```

-	Layers:
	-	`sha256:6eaead326de82fff673b43ee8a99bbc8aef307d1dd469d408ee550b7622082d8`  
		Last Modified: Tue, 02 Dec 2025 01:54:35 GMT  
		Size: 2.1 MB (2100948 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6eebffc73ad306243b3bc36fbf028eced30016b087952de7f08233991be8b5f6`  
		Last Modified: Tue, 02 Dec 2025 01:54:36 GMT  
		Size: 29.7 KB (29719 bytes)  
		MIME: application/vnd.in-toto+json
