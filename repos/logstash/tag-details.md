<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `logstash`

-	[`logstash:7.17.20`](#logstash71720)
-	[`logstash:8.13.0`](#logstash8130)

## `logstash:7.17.20`

```console
$ docker pull logstash@sha256:305700ff38ea43acc2e99de77780fcd4489c48294fbc64a4d920f49621315446
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
$ docker pull logstash@sha256:38bb22a2f980124d5c8f8a2dea1ceb09d65a4547902652488f6596e4a924a8b3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **429.1 MB (429142106 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f662a8259f96b9db7b67a79e179a4fdde138489d2a95d2e3f215755f619ffe09`
-	Entrypoint: `["\/usr\/local\/bin\/docker-entrypoint"]`

```dockerfile
# Fri, 16 Feb 2024 19:15:01 GMT
ARG RELEASE
# Fri, 16 Feb 2024 19:15:01 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 16 Feb 2024 19:15:01 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 16 Feb 2024 19:15:01 GMT
LABEL org.opencontainers.image.version=20.04
# Fri, 16 Feb 2024 19:15:06 GMT
ADD file:a8303c80b47ec165c276111aa6f98ee877e4da60ddafa00b7547032a3de7935d in / 
# Fri, 16 Feb 2024 19:15:06 GMT
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
	-	`sha256:6aae4cfdd5a10a8b0554e75c4c14ae38022a0c8f08dc5d769a735c705670cab7`  
		Last Modified: Fri, 16 Feb 2024 21:40:59 GMT  
		Size: 26.0 MB (25974391 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5425fb225216dc969f3f10fa6812a6be467ea7c73fcdc1aa4c81534d48916720`  
		Last Modified: Tue, 26 Mar 2024 19:08:37 GMT  
		Size: 37.2 MB (37212876 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2b78517e16767316435e2ba9c047bbbc6d0af81f3c639bd7ee8f46fc542318d`  
		Last Modified: Tue, 26 Mar 2024 19:08:36 GMT  
		Size: 1.8 KB (1810 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7119906fff0f65e166780ca04762d4c39a22e3aa1ebfa9b231347796925be78e`  
		Last Modified: Tue, 09 Apr 2024 18:57:54 GMT  
		Size: 364.0 MB (364047239 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d482483b8911d1de11dc61fc4d175e1ae1fc4ad9052a28fdd17ff604687e342c`  
		Last Modified: Tue, 09 Apr 2024 18:57:47 GMT  
		Size: 380.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1dc5da3ae51c5c0891df8ef48dad34379a2564bb1270ee866ec7b1e8c7302d66`  
		Last Modified: Tue, 09 Apr 2024 18:57:47 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e5164f677dbf2154aff7645f677a1c3bd3de71666bb75682618bdacec7f96b3`  
		Last Modified: Tue, 09 Apr 2024 18:57:47 GMT  
		Size: 474.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35636dea2513e4a41842b6f15d0668f281ae7aa033fad2f30795a12b91b51a62`  
		Last Modified: Tue, 09 Apr 2024 18:57:48 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5341eb1595212f49b142000198df4601097c31c59f6c14ab36a2006a75934a6`  
		Last Modified: Tue, 09 Apr 2024 18:57:48 GMT  
		Size: 827.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99e7e74361b595961e5e36e511110a1c71f8b8199bd985285f65014f06345093`  
		Last Modified: Tue, 09 Apr 2024 18:57:49 GMT  
		Size: 1.9 MB (1902995 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5048442229302a6ffed6368d9d80e4c0b7fa85a79268b2f0ddc0e9202b6143d`  
		Last Modified: Tue, 09 Apr 2024 18:57:49 GMT  
		Size: 494.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `logstash:7.17.20` - unknown; unknown

```console
$ docker pull logstash@sha256:a8d1a2679f4db6f9287017b96c0de97ca2d52d23b4440e116653e65dd476d197
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (3009678 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a242a19b35ac874d2216131b34f75a3d6bcd2dd81b8603d741c6b7e04957d354`

```dockerfile
```

-	Layers:
	-	`sha256:4a4de0ca0938d145bd74924f2d8bebea4e672fa571c58df596cdcc1e5941a40e`  
		Last Modified: Tue, 09 Apr 2024 18:57:47 GMT  
		Size: 3.0 MB (2977666 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c8bea02595d6d4f358d901fe5a92209c5c399facf980ba01169fa622dfdc36df`  
		Last Modified: Tue, 09 Apr 2024 18:57:47 GMT  
		Size: 32.0 KB (32012 bytes)  
		MIME: application/vnd.in-toto+json

## `logstash:8.13.0`

```console
$ docker pull logstash@sha256:d404341034eb48b62e81f3c730e4244299a244956179d16db973ac4add60048c
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
$ docker pull logstash@sha256:ade4c45b58c35477ef61874237331f3bc3205e47044db8bd6552702e4a33df9a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **477.4 MB (477443668 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a28b37048aaa72ef6be711e16b5f29b7aca2837044a71bf313893980cb04b42e`
-	Entrypoint: `["\/usr\/local\/bin\/docker-entrypoint"]`

```dockerfile
# Fri, 16 Feb 2024 19:15:01 GMT
ARG RELEASE
# Fri, 16 Feb 2024 19:15:01 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 16 Feb 2024 19:15:01 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 16 Feb 2024 19:15:01 GMT
LABEL org.opencontainers.image.version=20.04
# Fri, 16 Feb 2024 19:15:06 GMT
ADD file:a8303c80b47ec165c276111aa6f98ee877e4da60ddafa00b7547032a3de7935d in / 
# Fri, 16 Feb 2024 19:15:06 GMT
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
	-	`sha256:6aae4cfdd5a10a8b0554e75c4c14ae38022a0c8f08dc5d769a735c705670cab7`  
		Last Modified: Fri, 16 Feb 2024 21:40:59 GMT  
		Size: 26.0 MB (25974391 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f5e80fd83213efbe9caa80d6a019635678ee5cc95745f6acfa6f90c52f46df5`  
		Last Modified: Tue, 26 Mar 2024 19:07:17 GMT  
		Size: 37.2 MB (37212801 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96c22d41b53528ed35fbeb2bfe0dd2d51fedef7886026b6c9af30f1386365cde`  
		Last Modified: Tue, 26 Mar 2024 19:07:15 GMT  
		Size: 1.8 KB (1812 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ad7a1df18c719dd5312ecb83d38bdb2400349fbaf551bfb43aacbe1d123254c`  
		Last Modified: Tue, 26 Mar 2024 19:07:23 GMT  
		Size: 412.3 MB (412345902 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ddc524d760a392f0ee217dc0a3bf114ea645902012b5e43c736a5b1be7e2456e`  
		Last Modified: Tue, 26 Mar 2024 19:07:15 GMT  
		Size: 382.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08401652822e12af3c388e4e1c94ef641cb4b20444a859479223d5356fe2c809`  
		Last Modified: Tue, 26 Mar 2024 19:07:16 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:695271c2dfebb37d215cc8f3f3386432bf3c5576de25061e56325dd8c6c558f2`  
		Last Modified: Tue, 26 Mar 2024 19:07:17 GMT  
		Size: 475.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fe93bd8ccad9167870793206184cc2b9db4741147e37371b4b355869ed665d3`  
		Last Modified: Tue, 26 Mar 2024 19:07:18 GMT  
		Size: 1.4 KB (1363 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfd6dfb1d001a06ea354e4f6f92aa4743699da41e3cdc3615b095e38185620e6`  
		Last Modified: Tue, 26 Mar 2024 19:07:18 GMT  
		Size: 278.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5881ee79406147fb77c814643140b4ef3619668b3d36a123c1531f5be89c939`  
		Last Modified: Tue, 26 Mar 2024 19:07:19 GMT  
		Size: 1.8 KB (1765 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66d7ad580d97b6bb27e16e11d62fbece68772e3a9edf7c2168a7a0d2eb47cd8b`  
		Last Modified: Tue, 26 Mar 2024 19:07:19 GMT  
		Size: 1.9 MB (1903443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34979c15a1233c67bd0ec46dadaeb9569227dc9d89d950fee2a65c338a094c1d`  
		Last Modified: Tue, 26 Mar 2024 19:07:19 GMT  
		Size: 713.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `logstash:8.13.0` - unknown; unknown

```console
$ docker pull logstash@sha256:0f2bab4cb10e5f91f35a44a6be840eb663d099d578295d8e43956c8989e8f7da
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3211951 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ba68b61c5a236dab9c41021948429c3f3b4c8da03c703286afe903251cb3590`

```dockerfile
```

-	Layers:
	-	`sha256:562ca2a5070b8e2035df29e6c634bbd953ec6a8081b1808052ab752cff4abf2f`  
		Last Modified: Tue, 26 Mar 2024 19:07:15 GMT  
		Size: 3.2 MB (3177418 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:17aed4827ecf2de08bb7abf88eee3dea2fb807541ee82fe2502604e610ef7ef2`  
		Last Modified: Tue, 26 Mar 2024 19:07:15 GMT  
		Size: 34.5 KB (34533 bytes)  
		MIME: application/vnd.in-toto+json
