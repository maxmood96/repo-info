<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `logstash`

-	[`logstash:7.17.20`](#logstash71720)
-	[`logstash:8.13.0`](#logstash8130)

## `logstash:7.17.20`

```console
$ docker pull logstash@sha256:850c47b37309af8d386566e9bcdb6c540bb02e161bd2906b66d8394d547dea73
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `logstash:7.17.20` - linux; amd64

```console
$ docker pull logstash@sha256:4c0a4cd15e6ce442b257a3e18fb48382c0ea0d3114148750607bf1275f3aa38f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **445.3 MB (445279949 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8af3561174d9ae9deed93e23db7081a25a1bbbcd90a197f261468e1a80592436`
-	Entrypoint: `["\/usr\/local\/bin\/docker-entrypoint"]`

```dockerfile
# Tue, 09 Apr 2024 08:24:48 GMT
ARG RELEASE
# Tue, 09 Apr 2024 08:24:48 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 09 Apr 2024 08:24:48 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 09 Apr 2024 08:24:48 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 09 Apr 2024 08:24:48 GMT
ADD file:ea2128e23dce0162557abadd80656bd5ae047d573095d1d4323eb4154490dfdc in / 
# Tue, 09 Apr 2024 08:24:48 GMT
CMD ["/bin/bash"]
# Tue, 09 Apr 2024 08:24:48 GMT
RUN for iter in {1..10}; do export DEBIAN_FRONTEND=noninteractive && apt-get update -y && apt-get upgrade -y && apt-get install -y procps findutils tar gzip curl && apt-get install -y locales && apt-get clean all && locale-gen 'en_US.UTF-8' &&     apt-get clean metadata && exit_code=0 && break || exit_code=$? &&     echo "packaging error: retry $iter in 10s" &&     apt-get clean all && apt-get clean metadata && sleep 10; done;     (exit $exit_code) # buildkit
# Tue, 09 Apr 2024 08:24:48 GMT
RUN groupadd --gid 1000 logstash &&     adduser --uid 1000 --gid 1000        --home /usr/share/logstash --no-create-home       logstash # buildkit
# Tue, 09 Apr 2024 08:24:48 GMT
RUN curl -Lo - https://artifacts.elastic.co/downloads/logstash/logstash-7.17.20-linux-$(arch).tar.gz |     tar zxf - -C /usr/share &&     mv /usr/share/logstash-7.17.20 /usr/share/logstash && chown --recursive logstash:logstash /usr/share/logstash/ &&     chown -R logstash:root /usr/share/logstash &&     chmod -R g=u /usr/share/logstash &&     mkdir /licenses/ &&     mv /usr/share/logstash/NOTICE.TXT /licenses/NOTICE.TXT &&     mv /usr/share/logstash/LICENSE.txt /licenses/LICENSE.txt &&     find /usr/share/logstash -type d -exec chmod g+s {} \; &&     ln -s /usr/share/logstash /opt/logstash # buildkit
# Tue, 09 Apr 2024 08:24:48 GMT
WORKDIR /usr/share/logstash
# Tue, 09 Apr 2024 08:24:48 GMT
ENV ELASTIC_CONTAINER=true
# Tue, 09 Apr 2024 08:24:48 GMT
ENV PATH=/usr/share/logstash/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 09 Apr 2024 08:24:48 GMT
ADD config/pipelines.yml config/pipelines.yml # buildkit
# Tue, 09 Apr 2024 08:24:48 GMT
ADD config/logstash-full.yml config/logstash.yml # buildkit
# Tue, 09 Apr 2024 08:24:48 GMT
ADD config/log4j2.properties config/ # buildkit
# Tue, 09 Apr 2024 08:24:48 GMT
ADD pipeline/default.conf pipeline/logstash.conf # buildkit
# Tue, 09 Apr 2024 08:24:48 GMT
RUN chown --recursive logstash:root config/ pipeline/ # buildkit
# Tue, 09 Apr 2024 08:24:48 GMT
ENV LANG=en_US.UTF-8 LC_ALL=en_US.UTF-8
# Tue, 09 Apr 2024 08:24:48 GMT
ADD env2yaml/env2yaml /usr/local/bin/ # buildkit
# Tue, 09 Apr 2024 08:24:48 GMT
ADD bin/docker-entrypoint /usr/local/bin/ # buildkit
# Tue, 09 Apr 2024 08:24:48 GMT
RUN chmod 0755 /usr/local/bin/docker-entrypoint # buildkit
# Tue, 09 Apr 2024 08:24:48 GMT
USER 1000
# Tue, 09 Apr 2024 08:24:48 GMT
EXPOSE map[5044/tcp:{} 9600/tcp:{}]
# Tue, 09 Apr 2024 08:24:48 GMT
LABEL org.label-schema.schema-version=1.0 org.label-schema.vendor=Elastic org.opencontainers.image.vendor=Elastic org.label-schema.name=logstash org.opencontainers.image.title=logstash org.label-schema.version=7.17.20 org.opencontainers.image.version=7.17.20 org.label-schema.url=https://www.elastic.co/products/logstash org.label-schema.vcs-url=https://github.com/elastic/logstash org.label-schema.license=Elastic License org.opencontainers.image.licenses=Elastic License org.opencontainers.image.description=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' org.label-schema.build-date=2024-03-26T08:47:56+00:00 org.opencontainers.image.created=2024-03-26T08:47:56+00:00
# Tue, 09 Apr 2024 08:24:48 GMT
ENTRYPOINT ["/usr/local/bin/docker-entrypoint"]
```

-	Layers:
	-	`sha256:43cfb69dbb464ebad014cd4687bf02ee4f5011d540916c658af36faafbfd3481`  
		Last Modified: Wed, 10 Apr 2024 19:19:18 GMT  
		Size: 27.5 MB (27511841 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f96040c313722f6f169fd3243c074050d894142a48477031ff65a1aaf081b11`  
		Last Modified: Tue, 16 Apr 2024 04:26:44 GMT  
		Size: 48.5 MB (48528299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3bb27e9974a06117da48c1f89de1e2b56d669c375403f2a2d39e35acc15d2e28`  
		Last Modified: Tue, 16 Apr 2024 04:26:42 GMT  
		Size: 1.8 KB (1802 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d47d30948702822c25f6a051e4aed68c2bd4940d3126a1bea06bf896ba3cb3ee`  
		Last Modified: Tue, 16 Apr 2024 04:26:50 GMT  
		Size: 367.3 MB (367332234 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ec85b764bba348525ce4aed77b2ce14ba65d1b8168090cc636fdace08e822cf`  
		Last Modified: Tue, 16 Apr 2024 04:26:42 GMT  
		Size: 378.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c71581e3c167396dae067d2741d7a94f15e5a2057d001e9fda5894f57d44d55b`  
		Last Modified: Tue, 16 Apr 2024 04:26:43 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:edbaee74d0ec6dbef5704bb0a9c91e567616dfbb864c33b4f0774e978fad83fd`  
		Last Modified: Tue, 16 Apr 2024 04:26:43 GMT  
		Size: 471.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c1fff51e649130013caa5b43fc4ab3b02db3988ed4d3cc3b395dad3ab5a2d41`  
		Last Modified: Tue, 16 Apr 2024 04:26:44 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c604edc652af5acde33fbb8be126c1d134a78ed8bb656d8ee2054f15da8b5071`  
		Last Modified: Tue, 16 Apr 2024 04:26:45 GMT  
		Size: 827.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e12b2f450e5059bdaafd6e73b07a714e8d9c79ea468d47bca519af976d24c94`  
		Last Modified: Tue, 16 Apr 2024 04:26:46 GMT  
		Size: 1.9 MB (1902986 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5b601a445cb11f1131bf5dd53d938298e6ba51a695b6f3381835b9d36bd4df8`  
		Last Modified: Tue, 16 Apr 2024 04:26:46 GMT  
		Size: 493.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `logstash:7.17.20` - unknown; unknown

```console
$ docker pull logstash@sha256:8fe7f4494733bf3654a16f4eade753108ce4ad0b8e33b8d4593f838e07715d92
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (3009615 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f3bfcc02433aa836c10147e087575a697b91a086fe9a2b279871e18a6067ea6`

```dockerfile
```

-	Layers:
	-	`sha256:e691211dbc0bab25686f40dc56f8fe2f6113a044f025a77ace44f7842964d072`  
		Last Modified: Tue, 16 Apr 2024 04:26:42 GMT  
		Size: 3.0 MB (2977446 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6a03df1345d3b7cd38ba16fb22bc75f0e37e69e2e0020cedf767c0689402db4d`  
		Last Modified: Tue, 16 Apr 2024 04:26:41 GMT  
		Size: 32.2 KB (32169 bytes)  
		MIME: application/vnd.in-toto+json

### `logstash:7.17.20` - linux; arm64 variant v8

```console
$ docker pull logstash@sha256:2eead3bb15f116743eb083016072c82e12277623f78453da2f59ce52975aa6eb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **430.1 MB (430079189 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b6eeca5cf15bda662e50b9040c4d398a33ca6dcaf550193d57bada8f0366c3d`
-	Entrypoint: `["\/usr\/local\/bin\/docker-entrypoint"]`

```dockerfile
# Tue, 09 Apr 2024 08:24:48 GMT
ARG RELEASE
# Tue, 09 Apr 2024 08:24:48 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 09 Apr 2024 08:24:48 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 09 Apr 2024 08:24:48 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 09 Apr 2024 08:24:48 GMT
ADD file:acbed61dbc48e6a7411bf9844ddddb8ea75cd88378599d63b0b603e98acf0762 in / 
# Tue, 09 Apr 2024 08:24:48 GMT
CMD ["/bin/bash"]
# Tue, 09 Apr 2024 08:24:48 GMT
RUN for iter in {1..10}; do export DEBIAN_FRONTEND=noninteractive && apt-get update -y && apt-get upgrade -y && apt-get install -y procps findutils tar gzip curl && apt-get install -y locales && apt-get clean all && locale-gen 'en_US.UTF-8' &&     apt-get clean metadata && exit_code=0 && break || exit_code=$? &&     echo "packaging error: retry $iter in 10s" &&     apt-get clean all && apt-get clean metadata && sleep 10; done;     (exit $exit_code) # buildkit
# Tue, 09 Apr 2024 08:24:48 GMT
RUN groupadd --gid 1000 logstash &&     adduser --uid 1000 --gid 1000        --home /usr/share/logstash --no-create-home       logstash # buildkit
# Tue, 09 Apr 2024 08:24:48 GMT
RUN curl -Lo - https://artifacts.elastic.co/downloads/logstash/logstash-7.17.20-linux-$(arch).tar.gz |     tar zxf - -C /usr/share &&     mv /usr/share/logstash-7.17.20 /usr/share/logstash && chown --recursive logstash:logstash /usr/share/logstash/ &&     chown -R logstash:root /usr/share/logstash &&     chmod -R g=u /usr/share/logstash &&     mkdir /licenses/ &&     mv /usr/share/logstash/NOTICE.TXT /licenses/NOTICE.TXT &&     mv /usr/share/logstash/LICENSE.txt /licenses/LICENSE.txt &&     find /usr/share/logstash -type d -exec chmod g+s {} \; &&     ln -s /usr/share/logstash /opt/logstash # buildkit
# Tue, 09 Apr 2024 08:24:48 GMT
WORKDIR /usr/share/logstash
# Tue, 09 Apr 2024 08:24:48 GMT
ENV ELASTIC_CONTAINER=true
# Tue, 09 Apr 2024 08:24:48 GMT
ENV PATH=/usr/share/logstash/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 09 Apr 2024 08:24:48 GMT
ADD config/pipelines.yml config/pipelines.yml # buildkit
# Tue, 09 Apr 2024 08:24:48 GMT
ADD config/logstash-full.yml config/logstash.yml # buildkit
# Tue, 09 Apr 2024 08:24:48 GMT
ADD config/log4j2.properties config/ # buildkit
# Tue, 09 Apr 2024 08:24:48 GMT
ADD pipeline/default.conf pipeline/logstash.conf # buildkit
# Tue, 09 Apr 2024 08:24:48 GMT
RUN chown --recursive logstash:root config/ pipeline/ # buildkit
# Tue, 09 Apr 2024 08:24:48 GMT
ENV LANG=en_US.UTF-8 LC_ALL=en_US.UTF-8
# Tue, 09 Apr 2024 08:24:48 GMT
ADD env2yaml/env2yaml /usr/local/bin/ # buildkit
# Tue, 09 Apr 2024 08:24:48 GMT
ADD bin/docker-entrypoint /usr/local/bin/ # buildkit
# Tue, 09 Apr 2024 08:24:48 GMT
RUN chmod 0755 /usr/local/bin/docker-entrypoint # buildkit
# Tue, 09 Apr 2024 08:24:48 GMT
USER 1000
# Tue, 09 Apr 2024 08:24:48 GMT
EXPOSE map[5044/tcp:{} 9600/tcp:{}]
# Tue, 09 Apr 2024 08:24:48 GMT
LABEL org.label-schema.schema-version=1.0 org.label-schema.vendor=Elastic org.opencontainers.image.vendor=Elastic org.label-schema.name=logstash org.opencontainers.image.title=logstash org.label-schema.version=7.17.20 org.opencontainers.image.version=7.17.20 org.label-schema.url=https://www.elastic.co/products/logstash org.label-schema.vcs-url=https://github.com/elastic/logstash org.label-schema.license=Elastic License org.opencontainers.image.licenses=Elastic License org.opencontainers.image.description=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' org.label-schema.build-date=2024-03-26T08:47:56+00:00 org.opencontainers.image.created=2024-03-26T08:47:56+00:00
# Tue, 09 Apr 2024 08:24:48 GMT
ENTRYPOINT ["/usr/local/bin/docker-entrypoint"]
```

-	Layers:
	-	`sha256:fb67143098b346a05ff35775af9ba34ccf9a89e4079f4ceb9a51b05ae257e78c`  
		Last Modified: Wed, 10 Apr 2024 19:19:24 GMT  
		Size: 26.0 MB (25974891 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9349f81a1065cc476e591d33c090e901a4ecf9f71a69e3c18630786e41f10334`  
		Last Modified: Tue, 16 Apr 2024 11:47:37 GMT  
		Size: 38.1 MB (38149427 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a50595d08f53078a1dab66ea7d0ebbe85087ed4068d6350a82c4b1c150648e43`  
		Last Modified: Tue, 16 Apr 2024 11:47:35 GMT  
		Size: 1.8 KB (1807 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d2f48ca166032eff3ff05c066bf83cfa607e449b76b2fd2d473a675c8e0cec5`  
		Last Modified: Tue, 16 Apr 2024 11:47:43 GMT  
		Size: 364.0 MB (364047298 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:062ca11be0328887a3fada8d5c6214518cf59a0aaec6a328108a5f69c0197c33`  
		Last Modified: Tue, 16 Apr 2024 11:47:36 GMT  
		Size: 377.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c16f59112eb25e5d9a8c0794fe878a9a493e978932aeeba9e18c7e691caf272`  
		Last Modified: Tue, 16 Apr 2024 11:47:36 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db8800c2461bb6ad4c623fddf86d64d50c6f408a61b084d5ea0eecbcda0d6af1`  
		Last Modified: Tue, 16 Apr 2024 11:47:36 GMT  
		Size: 471.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a173f5db54a4e6b83c47c065a7b3c5e4a88ab30ea17d3fa92fd151084bafa195`  
		Last Modified: Tue, 16 Apr 2024 11:47:38 GMT  
		Size: 278.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2288f7d15aca277020fa0addd0890971e6ed99477c73fc63fd680eaf3de255f`  
		Last Modified: Tue, 16 Apr 2024 11:47:38 GMT  
		Size: 826.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35069ecbd7099af3f114bc9af2b64bbcacbe1f3445985a8d9ea7ba73de58fc7a`  
		Last Modified: Tue, 16 Apr 2024 11:47:39 GMT  
		Size: 1.9 MB (1902982 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8ca6f955f0bd4b2e6d9377934cdcfe0d589d1aaa1784102f9dc82131cea9d1d`  
		Last Modified: Tue, 16 Apr 2024 11:47:39 GMT  
		Size: 492.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `logstash:7.17.20` - unknown; unknown

```console
$ docker pull logstash@sha256:65a9014e803de8e51926be497091784e0cc24ab534ec9a877e1df5a6f48aaf57
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (3009678 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e955e121854a4b39b0889b1d72367a6bf9c4eefbc220670cb11409d2c4f0ec4`

```dockerfile
```

-	Layers:
	-	`sha256:a5168efe3c621b1091d07c1400a5cba7eb675f4b6b5d63b4ed063eb4627989df`  
		Last Modified: Tue, 16 Apr 2024 11:47:36 GMT  
		Size: 3.0 MB (2977666 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5a7526278b917aa5614fe4adab577f86329c595fc7275dfc9df5737b77c0037d`  
		Last Modified: Tue, 16 Apr 2024 11:47:35 GMT  
		Size: 32.0 KB (32012 bytes)  
		MIME: application/vnd.in-toto+json

## `logstash:8.13.0`

```console
$ docker pull logstash@sha256:9e1025206d85a0a6dac4f693fba95f402de56efe5f9c849af3e8c45210160463
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `logstash:8.13.0` - linux; amd64

```console
$ docker pull logstash@sha256:605bf935c2dd042cc8fe9d29b797c60627586376b34f6f0eb402c2eed6d15815
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **491.5 MB (491488113 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c2e85175a458e3390c2f757a198d9605fedef3ed9cd584ec072f858cd4d38e50`
-	Entrypoint: `["\/usr\/local\/bin\/docker-entrypoint"]`

```dockerfile
# Tue, 26 Mar 2024 13:49:26 GMT
ARG RELEASE
# Tue, 26 Mar 2024 13:49:26 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 26 Mar 2024 13:49:26 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 26 Mar 2024 13:49:26 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 26 Mar 2024 13:49:26 GMT
ADD file:ea2128e23dce0162557abadd80656bd5ae047d573095d1d4323eb4154490dfdc in / 
# Tue, 26 Mar 2024 13:49:26 GMT
CMD ["/bin/bash"]
# Tue, 26 Mar 2024 13:49:26 GMT
RUN for iter in {1..10}; do export DEBIAN_FRONTEND=noninteractive && apt-get update -y && apt-get upgrade -y && apt-get install -y procps findutils tar gzip curl && apt-get install -y locales && apt-get clean all && locale-gen 'en_US.UTF-8' && apt-get clean metadata && exit_code=0 && break || exit_code=$? && echo "packaging error: retry $iter in 10s" && apt-get clean all && apt-get clean metadata && sleep 10; done; (exit $exit_code) # buildkit
# Tue, 26 Mar 2024 13:49:26 GMT
RUN groupadd --gid 1000 logstash &&     adduser --uid 1000 --gid 1000     --home /usr/share/logstash --no-create-home     logstash # buildkit
# Tue, 26 Mar 2024 13:49:26 GMT
RUN curl -Lo - https://artifacts.elastic.co/downloads/logstash/logstash-8.13.0-linux-$(arch).tar.gz |     tar zxf - -C /usr/share &&     mv /usr/share/logstash-8.13.0 /usr/share/logstash &&     chown --recursive logstash:logstash /usr/share/logstash/ &&     chown -R logstash:root /usr/share/logstash &&     chmod -R g=u /usr/share/logstash &&     mkdir /licenses/ &&     mv /usr/share/logstash/NOTICE.TXT /licenses/NOTICE.TXT &&     mv /usr/share/logstash/LICENSE.txt /licenses/LICENSE.txt &&     find /usr/share/logstash -type d -exec chmod g+s {} \; &&     ln -s /usr/share/logstash /opt/logstash # buildkit
# Tue, 26 Mar 2024 13:49:26 GMT
WORKDIR /usr/share/logstash
# Tue, 26 Mar 2024 13:49:26 GMT
ENV ELASTIC_CONTAINER=true
# Tue, 26 Mar 2024 13:49:26 GMT
ENV PATH=/usr/share/logstash/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 26 Mar 2024 13:49:26 GMT
COPY config/pipelines.yml config/pipelines.yml # buildkit
# Tue, 26 Mar 2024 13:49:26 GMT
COPY config/logstash-full.yml config/logstash.yml # buildkit
# Tue, 26 Mar 2024 13:49:26 GMT
COPY config/log4j2.properties config/ # buildkit
# Tue, 26 Mar 2024 13:49:26 GMT
COPY config/log4j2.file.properties config/ # buildkit
# Tue, 26 Mar 2024 13:49:26 GMT
COPY pipeline/default.conf pipeline/logstash.conf # buildkit
# Tue, 26 Mar 2024 13:49:26 GMT
RUN chown --recursive logstash:root config/ pipeline/ # buildkit
# Tue, 26 Mar 2024 13:49:26 GMT
ENV LANG=en_US.UTF-8 LC_ALL=en_US.UTF-8
# Tue, 26 Mar 2024 13:49:26 GMT
COPY env2yaml/env2yaml /usr/local/bin/ # buildkit
# Tue, 26 Mar 2024 13:49:26 GMT
COPY bin/docker-entrypoint /usr/local/bin/ # buildkit
# Tue, 26 Mar 2024 13:49:26 GMT
RUN chmod 0755 /usr/local/bin/docker-entrypoint # buildkit
# Tue, 26 Mar 2024 13:49:26 GMT
USER 1000
# Tue, 26 Mar 2024 13:49:26 GMT
EXPOSE map[5044/tcp:{} 9600/tcp:{}]
# Tue, 26 Mar 2024 13:49:26 GMT
LABEL org.label-schema.schema-version=1.0 org.label-schema.vendor=Elastic org.opencontainers.image.vendor=Elastic org.label-schema.name=logstash org.opencontainers.image.title=logstash org.label-schema.version=8.13.0 org.opencontainers.image.version=8.13.0 org.label-schema.url=https://www.elastic.co/products/logstash org.label-schema.vcs-url=https://github.com/elastic/logstash org.label-schema.license=Elastic License org.opencontainers.image.licenses=Elastic License org.opencontainers.image.description=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' org.label-schema.build-date=2024-03-21T09:15:34+00:00 org.opencontainers.image.created=2024-03-21T09:15:34+00:00
# Tue, 26 Mar 2024 13:49:26 GMT
ENTRYPOINT ["/usr/local/bin/docker-entrypoint"]
```

-	Layers:
	-	`sha256:43cfb69dbb464ebad014cd4687bf02ee4f5011d540916c658af36faafbfd3481`  
		Last Modified: Wed, 10 Apr 2024 19:19:18 GMT  
		Size: 27.5 MB (27511841 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7134d77560c2bc0ac67a775bda8c2724ec98f36830675d927998cbb1731b66fd`  
		Last Modified: Tue, 16 Apr 2024 04:26:24 GMT  
		Size: 48.5 MB (48527848 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e8b066f2c57861858e7748ee3365eaa61bdee2cee5b59e92ecd8c6af801e580`  
		Last Modified: Tue, 16 Apr 2024 04:26:24 GMT  
		Size: 1.8 KB (1804 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d81f5381930bf7c525569fbdf1a61d3d712a4702abce69d1fb768cfb6053b17b`  
		Last Modified: Tue, 16 Apr 2024 04:26:30 GMT  
		Size: 413.5 MB (413537880 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66ff272c3f13cd820348a9bac02c972dd329b1f019b3a94e9cc5e56c7217cb12`  
		Last Modified: Tue, 16 Apr 2024 04:26:24 GMT  
		Size: 377.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b8e0d1b1efde6a1fbbdd116047e9ed69a505cef06a955124ede3b21ecef004e`  
		Last Modified: Tue, 16 Apr 2024 04:26:24 GMT  
		Size: 274.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e1ffff0ce2b70f1422336ce68628cefbc9a0019156b67c68170ed26ffb8e1c7`  
		Last Modified: Tue, 16 Apr 2024 04:26:24 GMT  
		Size: 471.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1520568ef1560bb5f0da85d33a93161fe91a9e7dd69ea4330604958d9621a2f5`  
		Last Modified: Tue, 16 Apr 2024 04:26:25 GMT  
		Size: 1.4 KB (1358 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4fea9bab0958c6757d2295c4d0ebdb8b3bc8eedf0e0bd66116092c90ec79de80`  
		Last Modified: Tue, 16 Apr 2024 04:26:25 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e302332168c6241ac4a5ca0d1e60da2124991a4e1abd363850f973156f4e040f`  
		Last Modified: Tue, 16 Apr 2024 04:26:26 GMT  
		Size: 1.8 KB (1763 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a133ea147a79ef51b2e5e2793e2be0628e03658d5cc6b6e487a59e5d204a179`  
		Last Modified: Tue, 16 Apr 2024 04:26:26 GMT  
		Size: 1.9 MB (1903444 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1be68df979b6a9fe64d1eb16738d97e9c0edcda26635b14aa9afe38cd66f39e0`  
		Last Modified: Tue, 16 Apr 2024 04:26:26 GMT  
		Size: 712.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `logstash:8.13.0` - unknown; unknown

```console
$ docker pull logstash@sha256:07640c199ebf031c051116d31437497bf71f0e48ce92b14c8836b922f888dfdb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3212533 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:73818e4e161e40a183efcdef2344f4eab52678bcbeeff517c1a56fa503f24856`

```dockerfile
```

-	Layers:
	-	`sha256:e17d172d87bb5cf7343a5e36b1af92120a1826cd187aec83113a96a771af8184`  
		Last Modified: Tue, 16 Apr 2024 04:26:24 GMT  
		Size: 3.2 MB (3177843 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4906a7767994275775a86294ad30eafbcd697820953d8577f83720503239b456`  
		Last Modified: Tue, 16 Apr 2024 04:26:24 GMT  
		Size: 34.7 KB (34690 bytes)  
		MIME: application/vnd.in-toto+json

### `logstash:8.13.0` - linux; arm64 variant v8

```console
$ docker pull logstash@sha256:ea0e389e8517fb75a692c745954c9489057a3862150c42626f325163935d1a56
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **478.4 MB (478380854 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d6913b92bc029e907b5219c3b733ddd05626280619caaac5012bc8b632fbe68`
-	Entrypoint: `["\/usr\/local\/bin\/docker-entrypoint"]`

```dockerfile
# Tue, 26 Mar 2024 13:49:26 GMT
ARG RELEASE
# Tue, 26 Mar 2024 13:49:26 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 26 Mar 2024 13:49:26 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 26 Mar 2024 13:49:26 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 26 Mar 2024 13:49:26 GMT
ADD file:acbed61dbc48e6a7411bf9844ddddb8ea75cd88378599d63b0b603e98acf0762 in / 
# Tue, 26 Mar 2024 13:49:26 GMT
CMD ["/bin/bash"]
# Tue, 26 Mar 2024 13:49:26 GMT
RUN for iter in {1..10}; do export DEBIAN_FRONTEND=noninteractive && apt-get update -y && apt-get upgrade -y && apt-get install -y procps findutils tar gzip curl && apt-get install -y locales && apt-get clean all && locale-gen 'en_US.UTF-8' && apt-get clean metadata && exit_code=0 && break || exit_code=$? && echo "packaging error: retry $iter in 10s" && apt-get clean all && apt-get clean metadata && sleep 10; done; (exit $exit_code) # buildkit
# Tue, 26 Mar 2024 13:49:26 GMT
RUN groupadd --gid 1000 logstash &&     adduser --uid 1000 --gid 1000     --home /usr/share/logstash --no-create-home     logstash # buildkit
# Tue, 26 Mar 2024 13:49:26 GMT
RUN curl -Lo - https://artifacts.elastic.co/downloads/logstash/logstash-8.13.0-linux-$(arch).tar.gz |     tar zxf - -C /usr/share &&     mv /usr/share/logstash-8.13.0 /usr/share/logstash &&     chown --recursive logstash:logstash /usr/share/logstash/ &&     chown -R logstash:root /usr/share/logstash &&     chmod -R g=u /usr/share/logstash &&     mkdir /licenses/ &&     mv /usr/share/logstash/NOTICE.TXT /licenses/NOTICE.TXT &&     mv /usr/share/logstash/LICENSE.txt /licenses/LICENSE.txt &&     find /usr/share/logstash -type d -exec chmod g+s {} \; &&     ln -s /usr/share/logstash /opt/logstash # buildkit
# Tue, 26 Mar 2024 13:49:26 GMT
WORKDIR /usr/share/logstash
# Tue, 26 Mar 2024 13:49:26 GMT
ENV ELASTIC_CONTAINER=true
# Tue, 26 Mar 2024 13:49:26 GMT
ENV PATH=/usr/share/logstash/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 26 Mar 2024 13:49:26 GMT
COPY config/pipelines.yml config/pipelines.yml # buildkit
# Tue, 26 Mar 2024 13:49:26 GMT
COPY config/logstash-full.yml config/logstash.yml # buildkit
# Tue, 26 Mar 2024 13:49:26 GMT
COPY config/log4j2.properties config/ # buildkit
# Tue, 26 Mar 2024 13:49:26 GMT
COPY config/log4j2.file.properties config/ # buildkit
# Tue, 26 Mar 2024 13:49:26 GMT
COPY pipeline/default.conf pipeline/logstash.conf # buildkit
# Tue, 26 Mar 2024 13:49:26 GMT
RUN chown --recursive logstash:root config/ pipeline/ # buildkit
# Tue, 26 Mar 2024 13:49:26 GMT
ENV LANG=en_US.UTF-8 LC_ALL=en_US.UTF-8
# Tue, 26 Mar 2024 13:49:26 GMT
COPY env2yaml/env2yaml /usr/local/bin/ # buildkit
# Tue, 26 Mar 2024 13:49:26 GMT
COPY bin/docker-entrypoint /usr/local/bin/ # buildkit
# Tue, 26 Mar 2024 13:49:26 GMT
RUN chmod 0755 /usr/local/bin/docker-entrypoint # buildkit
# Tue, 26 Mar 2024 13:49:26 GMT
USER 1000
# Tue, 26 Mar 2024 13:49:26 GMT
EXPOSE map[5044/tcp:{} 9600/tcp:{}]
# Tue, 26 Mar 2024 13:49:26 GMT
LABEL org.label-schema.schema-version=1.0 org.label-schema.vendor=Elastic org.opencontainers.image.vendor=Elastic org.label-schema.name=logstash org.opencontainers.image.title=logstash org.label-schema.version=8.13.0 org.opencontainers.image.version=8.13.0 org.label-schema.url=https://www.elastic.co/products/logstash org.label-schema.vcs-url=https://github.com/elastic/logstash org.label-schema.license=Elastic License org.opencontainers.image.licenses=Elastic License org.opencontainers.image.description=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' org.label-schema.build-date=2024-03-21T09:15:34+00:00 org.opencontainers.image.created=2024-03-21T09:15:34+00:00
# Tue, 26 Mar 2024 13:49:26 GMT
ENTRYPOINT ["/usr/local/bin/docker-entrypoint"]
```

-	Layers:
	-	`sha256:fb67143098b346a05ff35775af9ba34ccf9a89e4079f4ceb9a51b05ae257e78c`  
		Last Modified: Wed, 10 Apr 2024 19:19:24 GMT  
		Size: 26.0 MB (25974891 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a79ffc9f6c071ab88911e0139060b7da98f30a5671f61a94bf0a1f7247056aa2`  
		Last Modified: Tue, 16 Apr 2024 11:21:11 GMT  
		Size: 38.1 MB (38149468 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:508f0a65fcca070e39c87687ecaf1b0e9a4a5bfd384fff554b2e7606c07185c3`  
		Last Modified: Tue, 16 Apr 2024 11:21:09 GMT  
		Size: 1.8 KB (1808 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3185e60d52c9ddc4d2e7e0eb38ce61a6fd8fb78a1b9a33b002ed542b53df90c2`  
		Last Modified: Tue, 16 Apr 2024 11:21:22 GMT  
		Size: 412.3 MB (412345928 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f00a72fcfbab02905a0f8f5cf271afc0b41b98320a85989ce269c6653221e9c5`  
		Last Modified: Tue, 16 Apr 2024 11:21:10 GMT  
		Size: 381.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18761923db11a60bb69803477b8b43a55cd3392f53d0159448a4d68e883588da`  
		Last Modified: Tue, 16 Apr 2024 11:21:10 GMT  
		Size: 278.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05415ddc4e98bcef704a69a668922fe933bc66fe3203ecf089bb2bab252d2a14`  
		Last Modified: Tue, 16 Apr 2024 11:21:12 GMT  
		Size: 474.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8023bea9d37e71f799b7410f7bfb330f21c6584846caef80df59088edad6ce3e`  
		Last Modified: Tue, 16 Apr 2024 11:21:11 GMT  
		Size: 1.4 KB (1364 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:611147156213178522bc3b1d543d3e2117450dca21861b5151e229897c5cf9e8`  
		Last Modified: Tue, 16 Apr 2024 11:21:12 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58ca75ecb24154452f83677c6b7a01783f6508abbdb6439e3b8cc8dab78691a3`  
		Last Modified: Tue, 16 Apr 2024 11:21:13 GMT  
		Size: 1.8 KB (1766 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:450abc718a1d5073beb379b75bf6f8fa4138b0118632dffe05f4cabe07bc5e7e`  
		Last Modified: Tue, 16 Apr 2024 11:21:13 GMT  
		Size: 1.9 MB (1903444 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b62d62481f6d68dc410b55e1fe3aea7606f9f69d85b4ad38a962462dd10ef6d1`  
		Last Modified: Tue, 16 Apr 2024 11:21:14 GMT  
		Size: 711.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `logstash:8.13.0` - unknown; unknown

```console
$ docker pull logstash@sha256:06aea6d6d2f02f82aa76a67ee6e0b19bda923dc92562e6935af30b5bf0bfa2e3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3212588 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:550bce9400a9d52bcaaae9eaeaf81aed5021eddb45023b12977477dc607e1042`

```dockerfile
```

-	Layers:
	-	`sha256:459b1c474dd49b8d3a7d57980437a54630b1796047b7b545c64c27f982e8cef6`  
		Last Modified: Tue, 16 Apr 2024 11:21:10 GMT  
		Size: 3.2 MB (3178056 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:af906e1b6bf5a4daf8f9573cd1e6599b9caf6a6536e5d83f3af54e2ccb76ee6f`  
		Last Modified: Tue, 16 Apr 2024 11:21:10 GMT  
		Size: 34.5 KB (34532 bytes)  
		MIME: application/vnd.in-toto+json
