<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `logstash`

-	[`logstash:8.19.16`](#logstash81916)
-	[`logstash:9.3.5`](#logstash935)
-	[`logstash:9.4.2`](#logstash942)

## `logstash:8.19.16`

```console
$ docker pull logstash@sha256:f239b59f3525feda70d999d7f44600d4b0b6e833c141cbf143c9d0e6402c526d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `logstash:8.19.16` - linux; amd64

```console
$ docker pull logstash@sha256:56bdd2ce3bdc181cd74c4d1890c7441fa819b3f670bdea6d0ed43ba0f6d6421b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **543.2 MB (543167763 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:40fc5ce70ebd6a69003e8603e9a59166c9a26da44db07b0f34112c56a5f38e99`
-	Entrypoint: `["\/usr\/local\/bin\/docker-entrypoint"]`

```dockerfile
# Fri, 10 Apr 2026 06:49:15 GMT
ARG RELEASE
# Fri, 10 Apr 2026 06:49:15 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 06:49:15 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 10 Apr 2026 06:49:17 GMT
ADD file:8ce1caf246e7c778bca84c516d02fd4e83766bb2c530a0fffa8a351b560a2728 in / 
# Fri, 10 Apr 2026 06:49:18 GMT
CMD ["/bin/bash"]
# Thu, 28 May 2026 21:34:59 GMT
RUN for iter in {1..10}; do       export DEBIAN_FRONTEND=noninteractive &&     apt-get update -y &&   apt-get upgrade -y &&   apt-get install -y procps findutils tar gzip &&         apt-get install -y locales &&         apt-get install -y curl &&     apt-get clean all &&       locale-gen 'en_US.UTF-8' &&     apt-get clean metadata &&   exit_code=0 && break || exit_code=$? && echo "packaging error: retry $iter in 10s" && apt-get clean all &&   apt-get clean metadata && sleep 10; done; (exit $exit_code) # buildkit
# Thu, 28 May 2026 21:34:59 GMT
RUN userdel -r ubuntu && groupadd --gid 1000 logstash &&   useradd --uid 1000 --gid 1000 --home /usr/share/logstash --no-create-home logstash # buildkit
# Thu, 28 May 2026 21:35:43 GMT
RUN curl -Lo - https://artifacts.elastic.co/downloads/logstash/logstash-8.19.16-linux-$(arch).tar.gz |   tar zxf - -C /usr/share &&   mv /usr/share/logstash-8.19.16 /usr/share/logstash &&   chown --recursive logstash:logstash /usr/share/logstash/ &&   chown -R logstash:root /usr/share/logstash &&   chmod -R g=u /usr/share/logstash &&   mkdir /licenses/ &&   mv /usr/share/logstash/NOTICE.TXT /licenses/NOTICE.TXT &&   mv /usr/share/logstash/LICENSE.txt /licenses/LICENSE.txt &&   find /usr/share/logstash -type d -exec chmod g+s {} \; &&   ln -s /usr/share/logstash /opt/logstash # buildkit
# Thu, 28 May 2026 21:35:43 GMT
WORKDIR /usr/share/logstash
# Thu, 28 May 2026 21:35:43 GMT
ENV ELASTIC_CONTAINER=true
# Thu, 28 May 2026 21:35:43 GMT
ENV PATH=/usr/share/logstash/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 28 May 2026 21:35:43 GMT
COPY config/logstash-full.yml config/logstash.yml # buildkit
# Thu, 28 May 2026 21:35:43 GMT
COPY config/pipelines.yml config/log4j2.properties config/log4j2.file.properties config/ # buildkit
# Thu, 28 May 2026 21:35:43 GMT
COPY pipeline/default.conf pipeline/logstash.conf # buildkit
# Thu, 28 May 2026 21:35:44 GMT
RUN chown --recursive logstash:root config/ pipeline/ # buildkit
# Thu, 28 May 2026 21:35:44 GMT
ENV LANG=en_US.UTF-8 LC_ALL=en_US.UTF-8
# Thu, 28 May 2026 21:35:44 GMT
COPY --chown=logstash:root env2yaml/classes /usr/share/logstash/env2yaml/classes/ # buildkit
# Thu, 28 May 2026 21:35:44 GMT
COPY --chown=logstash:root env2yaml/lib /usr/share/logstash/env2yaml/lib/ # buildkit
# Thu, 28 May 2026 21:35:44 GMT
COPY --chmod=0755 env2yaml/env2yaml /usr/local/bin/env2yaml # buildkit
# Thu, 28 May 2026 21:35:44 GMT
COPY bin/docker-entrypoint /usr/local/bin/ # buildkit
# Thu, 28 May 2026 21:35:44 GMT
RUN chmod 0755 /usr/local/bin/docker-entrypoint # buildkit
# Thu, 28 May 2026 21:35:44 GMT
USER 1000
# Thu, 28 May 2026 21:35:44 GMT
EXPOSE map[5044/tcp:{} 9600/tcp:{}]
# Thu, 28 May 2026 21:35:44 GMT
LABEL org.label-schema.schema-version=1.0 org.label-schema.vendor=Elastic org.opencontainers.image.vendor=Elastic org.label-schema.name=logstash org.opencontainers.image.title=logstash org.label-schema.version=8.19.16 org.opencontainers.image.version=8.19.16 org.label-schema.url=https://www.elastic.co/products/logstash org.label-schema.vcs-url=https://github.com/elastic/logstash org.label-schema.license=Elastic License org.opencontainers.image.licenses=Elastic License org.opencontainers.image.description=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' org.label-schema.build-date=2026-05-23T16:24:56+00:00 org.opencontainers.image.created=2026-05-23T16:24:56+00:00
# Thu, 28 May 2026 21:35:44 GMT
ENTRYPOINT ["/usr/local/bin/docker-entrypoint"]
```

-	Layers:
	-	`sha256:b40150c1c2717d324cdb17278c8efdfa4dfcd2ffe083e976f0bcedf31115f081`  
		Last Modified: Fri, 10 Apr 2026 09:34:17 GMT  
		Size: 29.7 MB (29732978 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa4506713c2be693b6cbb0cbb8344e2310f67771829d1814f89b4e87d2c647c5`  
		Last Modified: Thu, 28 May 2026 21:36:20 GMT  
		Size: 55.4 MB (55426346 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f61a5e7f04e2834eddf21f18c2b2a2f3116ccc38d52927063c276b83c421080`  
		Last Modified: Thu, 28 May 2026 21:36:17 GMT  
		Size: 1.2 KB (1223 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c37122c41991342735a6e35c0a7ae0d92ca8131ef466552d84487397dd11387c`  
		Last Modified: Thu, 28 May 2026 21:36:27 GMT  
		Size: 457.7 MB (457740703 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c07c40ebbcc303b11267ac88c60bd68728403ab4f5ca22ceec76a107bf5cc27`  
		Last Modified: Thu, 28 May 2026 21:36:17 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9761040dc5a06ed62c50436e146f84e22d0d6707a30b78d701e312341d071e0`  
		Last Modified: Thu, 28 May 2026 21:36:18 GMT  
		Size: 1.6 KB (1577 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07b24349a237c1280b6932f5022e9dec507a1e570615b2dc248f7c6142390c20`  
		Last Modified: Thu, 28 May 2026 21:36:19 GMT  
		Size: 278.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5e0308759733c578ac5290f7e5efaa8fe77d33049a610c0870169a75b416d60`  
		Last Modified: Thu, 28 May 2026 21:36:20 GMT  
		Size: 1.8 KB (1765 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6734c111a3ef822beb9a60efa2d706464126dc153008611942c6b43d86ce6bb4`  
		Last Modified: Thu, 28 May 2026 21:36:20 GMT  
		Size: 6.3 KB (6296 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8df0949b8df3183c390ba0f522fe20eacccc4a0d8c1d3563c75fd3a80ff1fd4`  
		Last Modified: Thu, 28 May 2026 21:36:21 GMT  
		Size: 255.2 KB (255186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16d6bfcfae9b3b180e437c98989ef4c83f07a2bc9ad1bccb49f8c635f547d3cf`  
		Last Modified: Thu, 28 May 2026 21:36:21 GMT  
		Size: 356.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19de9779b131942076d599f56d30f09802c409fa6c975dff4f5b9c274dbea0cd`  
		Last Modified: Thu, 28 May 2026 21:36:22 GMT  
		Size: 714.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `logstash:8.19.16` - unknown; unknown

```console
$ docker pull logstash@sha256:36ee43145e48b54746ff8b916ae8e39fb4938cb519777811cb182b1488df4a16
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3729924 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a49b174f365e6d73c47592f31487f00fd80672b4e657dc7eb45cbe6ff1489d7`

```dockerfile
```

-	Layers:
	-	`sha256:beefd2a9aa6ad3ae1a04653d839caabf238cf584496b78cef0f0e2bf0707e324`  
		Last Modified: Thu, 28 May 2026 21:36:17 GMT  
		Size: 3.7 MB (3694079 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:84ab62296344a17657a60b54413c3e9ad5080fb393a3f598173e0a92553d2aac`  
		Last Modified: Thu, 28 May 2026 21:36:17 GMT  
		Size: 35.8 KB (35845 bytes)  
		MIME: application/vnd.in-toto+json

### `logstash:8.19.16` - linux; arm64 variant v8

```console
$ docker pull logstash@sha256:f5946d39b5f9e44299455266b46e039e6fc67718b8cee9bc928c0ef97ed4792d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **544.1 MB (544112216 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0dc888f733db7e07047a680565be1570aa8294fb05d227f937f67d38cb909a0d`
-	Entrypoint: `["\/usr\/local\/bin\/docker-entrypoint"]`

```dockerfile
# Fri, 10 Apr 2026 06:56:52 GMT
ARG RELEASE
# Fri, 10 Apr 2026 06:56:52 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 06:56:52 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 10 Apr 2026 06:56:54 GMT
ADD file:c98b7645109cdf61ab97492b90629581b1b7cb925b9d58a5787a4aaeb719f2be in / 
# Fri, 10 Apr 2026 06:56:54 GMT
CMD ["/bin/bash"]
# Thu, 28 May 2026 21:35:37 GMT
RUN for iter in {1..10}; do       export DEBIAN_FRONTEND=noninteractive &&     apt-get update -y &&   apt-get upgrade -y &&   apt-get install -y procps findutils tar gzip &&         apt-get install -y locales &&         apt-get install -y curl &&     apt-get clean all &&       locale-gen 'en_US.UTF-8' &&     apt-get clean metadata &&   exit_code=0 && break || exit_code=$? && echo "packaging error: retry $iter in 10s" && apt-get clean all &&   apt-get clean metadata && sleep 10; done; (exit $exit_code) # buildkit
# Thu, 28 May 2026 21:35:37 GMT
RUN userdel -r ubuntu && groupadd --gid 1000 logstash &&   useradd --uid 1000 --gid 1000 --home /usr/share/logstash --no-create-home logstash # buildkit
# Thu, 28 May 2026 21:35:59 GMT
RUN curl -Lo - https://artifacts.elastic.co/downloads/logstash/logstash-8.19.16-linux-$(arch).tar.gz |   tar zxf - -C /usr/share &&   mv /usr/share/logstash-8.19.16 /usr/share/logstash &&   chown --recursive logstash:logstash /usr/share/logstash/ &&   chown -R logstash:root /usr/share/logstash &&   chmod -R g=u /usr/share/logstash &&   mkdir /licenses/ &&   mv /usr/share/logstash/NOTICE.TXT /licenses/NOTICE.TXT &&   mv /usr/share/logstash/LICENSE.txt /licenses/LICENSE.txt &&   find /usr/share/logstash -type d -exec chmod g+s {} \; &&   ln -s /usr/share/logstash /opt/logstash # buildkit
# Thu, 28 May 2026 21:35:59 GMT
WORKDIR /usr/share/logstash
# Thu, 28 May 2026 21:35:59 GMT
ENV ELASTIC_CONTAINER=true
# Thu, 28 May 2026 21:35:59 GMT
ENV PATH=/usr/share/logstash/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 28 May 2026 21:35:59 GMT
COPY config/logstash-full.yml config/logstash.yml # buildkit
# Thu, 28 May 2026 21:35:59 GMT
COPY config/pipelines.yml config/log4j2.properties config/log4j2.file.properties config/ # buildkit
# Thu, 28 May 2026 21:35:59 GMT
COPY pipeline/default.conf pipeline/logstash.conf # buildkit
# Thu, 28 May 2026 21:35:59 GMT
RUN chown --recursive logstash:root config/ pipeline/ # buildkit
# Thu, 28 May 2026 21:35:59 GMT
ENV LANG=en_US.UTF-8 LC_ALL=en_US.UTF-8
# Thu, 28 May 2026 21:35:59 GMT
COPY --chown=logstash:root env2yaml/classes /usr/share/logstash/env2yaml/classes/ # buildkit
# Thu, 28 May 2026 21:35:59 GMT
COPY --chown=logstash:root env2yaml/lib /usr/share/logstash/env2yaml/lib/ # buildkit
# Thu, 28 May 2026 21:35:59 GMT
COPY --chmod=0755 env2yaml/env2yaml /usr/local/bin/env2yaml # buildkit
# Thu, 28 May 2026 21:35:59 GMT
COPY bin/docker-entrypoint /usr/local/bin/ # buildkit
# Thu, 28 May 2026 21:35:59 GMT
RUN chmod 0755 /usr/local/bin/docker-entrypoint # buildkit
# Thu, 28 May 2026 21:35:59 GMT
USER 1000
# Thu, 28 May 2026 21:35:59 GMT
EXPOSE map[5044/tcp:{} 9600/tcp:{}]
# Thu, 28 May 2026 21:35:59 GMT
LABEL org.label-schema.schema-version=1.0 org.label-schema.vendor=Elastic org.opencontainers.image.vendor=Elastic org.label-schema.name=logstash org.opencontainers.image.title=logstash org.label-schema.version=8.19.16 org.opencontainers.image.version=8.19.16 org.label-schema.url=https://www.elastic.co/products/logstash org.label-schema.vcs-url=https://github.com/elastic/logstash org.label-schema.license=Elastic License org.opencontainers.image.licenses=Elastic License org.opencontainers.image.description=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' org.label-schema.build-date=2026-05-23T16:24:56+00:00 org.opencontainers.image.created=2026-05-23T16:24:56+00:00
# Thu, 28 May 2026 21:35:59 GMT
ENTRYPOINT ["/usr/local/bin/docker-entrypoint"]
```

-	Layers:
	-	`sha256:818154cda96df8bbb276b4f4339124da55756620a1037af15570bc95312850fa`  
		Last Modified: Fri, 10 Apr 2026 09:34:24 GMT  
		Size: 28.9 MB (28875785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e6e12123ba7f730b6169d096bfac54bd1c24fec9b926c4c56eab5cf3a0586d0`  
		Last Modified: Thu, 28 May 2026 21:36:40 GMT  
		Size: 58.9 MB (58928615 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c70a4543994ca64b9e26eb296a9ef311da1b9b05bcb35de37bb8d28dd4c63dad`  
		Last Modified: Thu, 28 May 2026 21:36:38 GMT  
		Size: 1.2 KB (1223 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:902d6577c111bfb37dfd44214c8f4d91333cd29371d2240413c298cf1dba4d10`  
		Last Modified: Thu, 28 May 2026 21:36:49 GMT  
		Size: 456.0 MB (456040089 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8b57b70dc28762637e7241c6f6c6b7d4f8b66cc35971918d8ceee17c2258f2b`  
		Last Modified: Thu, 28 May 2026 21:36:38 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f44f8426ec00cb6f234982678f631ee7db90fefc81da7625ee986af48ad6abd7`  
		Last Modified: Thu, 28 May 2026 21:36:39 GMT  
		Size: 1.6 KB (1578 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78986378f6faef8c0afa6d8b4f695044d6b6ab10dd5f6b5cc2704fcb45e40c69`  
		Last Modified: Thu, 28 May 2026 21:36:39 GMT  
		Size: 278.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bed79478969c187ad52bd899c8b687f451e388fbeaa4c99aea15a261de828644`  
		Last Modified: Thu, 28 May 2026 21:36:40 GMT  
		Size: 1.8 KB (1763 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:793d529a23c2aef1bb5e4494e40eec2c1d25a845a026302da7865f5de970dc1b`  
		Last Modified: Thu, 28 May 2026 21:36:40 GMT  
		Size: 6.3 KB (6296 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0698064e62214315de09a7bcd5370f07f6b171aaf7487921a2974b70f427d597`  
		Last Modified: Thu, 28 May 2026 21:36:42 GMT  
		Size: 255.2 KB (255184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65eb14f9fefa2549250266a0d05c5d7230d2f4a70a262ea17643e47c0031afed`  
		Last Modified: Thu, 28 May 2026 21:36:42 GMT  
		Size: 353.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:baa2c8f5fc55df57154faed2f78f9bcb712a637f2eb918758b1527e5ae4350f6`  
		Last Modified: Thu, 28 May 2026 21:36:43 GMT  
		Size: 713.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `logstash:8.19.16` - unknown; unknown

```console
$ docker pull logstash@sha256:4653132addf80f1e6b3212464d480f359f96c110d15f88249c63e0706412125c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3730477 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c8efe5ebddf831a039df186bdfac4c709079259b87782fb90fdeb9ec2e99a19`

```dockerfile
```

-	Layers:
	-	`sha256:1556606237fd76f22b4e810bc44bffe09633640f5f769ed847c7dd191d472b47`  
		Last Modified: Thu, 28 May 2026 21:36:38 GMT  
		Size: 3.7 MB (3694504 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6e5654c090488e42c961b061b11834ee35251d045a7c03205d7aa1d769c7b6b8`  
		Last Modified: Thu, 28 May 2026 21:36:38 GMT  
		Size: 36.0 KB (35973 bytes)  
		MIME: application/vnd.in-toto+json

## `logstash:9.3.5`

```console
$ docker pull logstash@sha256:154410df634eb1da69bf8f3b0ca1c3d5b25f8a995e71f4c7d88f819ad3c8d3a3
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `logstash:9.3.5` - linux; amd64

```console
$ docker pull logstash@sha256:10af8cf84929fed8fa2abd2b3af574da6c2fccfd9ddb8c787567784be18c11ce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **518.0 MB (518025580 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:726024920c23bb928ca4730e2026d7d2a442cce8ab709b411750105565475a15`
-	Entrypoint: `["\/usr\/local\/bin\/docker-entrypoint"]`

```dockerfile
# Tue, 26 May 2026 15:32:20 GMT
LABEL maintainer="Red Hat, Inc."
# Tue, 26 May 2026 15:32:20 GMT
LABEL vendor="Red Hat, Inc."
# Tue, 26 May 2026 15:32:20 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Tue, 26 May 2026 15:32:20 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.8"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Tue, 26 May 2026 15:32:20 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Tue, 26 May 2026 15:32:20 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Tue, 26 May 2026 15:32:20 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Tue, 26 May 2026 15:32:20 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Tue, 26 May 2026 15:32:21 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Tue, 26 May 2026 15:32:21 GMT
LABEL io.openshift.expose-services=""
# Tue, 26 May 2026 15:32:21 GMT
LABEL io.openshift.tags="minimal rhel9"
# Tue, 26 May 2026 15:32:21 GMT
ENV container oci
# Tue, 26 May 2026 15:32:22 GMT
COPY dir:bcf46f8211a223ea361ec9cb0b5d7567aaf9ce54beddfddade034948e142ca6d in /      
# Tue, 26 May 2026 15:32:22 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Tue, 26 May 2026 15:32:22 GMT
CMD ["/bin/bash"]
# Tue, 26 May 2026 15:32:22 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /usr/share/buildinfo/content-sets.json      
# Tue, 26 May 2026 15:32:23 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /root/buildinfo/content_manifests/content-sets.json      
# Tue, 26 May 2026 15:32:23 GMT
COPY file:227070320251c0bebb0aee79adad2b4d241a94b8936d1e12e22f0f0015cd467b in /usr/share/buildinfo/labels.json      
# Tue, 26 May 2026 15:32:23 GMT
COPY file:227070320251c0bebb0aee79adad2b4d241a94b8936d1e12e22f0f0015cd467b in /root/buildinfo/labels.json      
# Tue, 26 May 2026 15:32:23 GMT
LABEL "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="106f2a33b03195c917e783d47463c6f8e17f7458" "org.opencontainers.image.revision"="106f2a33b03195c917e783d47463c6f8e17f7458" "build-date"="2026-05-26T15:32:02Z" "org.opencontainers.image.created"="2026-05-26T15:32:02Z" "release"="1779809423"org.opencontainers.image.revision=106f2a33b03195c917e783d47463c6f8e17f7458,org.opencontainers.image.created=2026-05-26T15:32:02Z
# Thu, 28 May 2026 21:34:55 GMT
ENV ELASTIC_CONTAINER=true
# Thu, 28 May 2026 21:34:55 GMT
ENV PATH=/usr/share/logstash/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 28 May 2026 21:34:55 GMT
ENV LANG=C.UTF-8 LC_ALL=C.UTF-8
# Thu, 28 May 2026 21:34:55 GMT
WORKDIR /usr/share
# Thu, 28 May 2026 21:34:56 GMT
RUN microdnf install -y procps findutils tar gzip &&   microdnf install -y openssl &&   microdnf install -y which shadow-utils &&   microdnf clean all # buildkit
# Thu, 28 May 2026 21:35:26 GMT
RUN groupadd --gid 1000 logstash &&   adduser --uid 1000 --gid 1000   --home "/usr/share/logstash"   --no-create-home   logstash &&   arch="$(rpm --query --queryformat='%{ARCH}' rpm)" &&   curl --fail --location --output logstash.tar.gz https://artifacts.elastic.co/downloads/logstash/logstash-9.3.5-linux-${arch}.tar.gz &&   tar -zxf logstash.tar.gz -C /usr/share &&   rm logstash.tar.gz &&   mv /usr/share/logstash-9.3.5 /usr/share/logstash &&   chown -R logstash:root /usr/share/logstash &&   chmod -R g=u /usr/share/logstash &&   mkdir /licenses &&   mv /usr/share/logstash/NOTICE.TXT /licenses/NOTICE.TXT &&   mv /usr/share/logstash/LICENSE.txt /licenses/LICENSE.txt &&   find /usr/share/logstash -type d -exec chmod g+s {} \; &&   ln -s /usr/share/logstash /opt/logstash # buildkit
# Thu, 28 May 2026 21:35:26 GMT
COPY --chown=logstash:root env2yaml/classes /usr/share/logstash/env2yaml/classes/ # buildkit
# Thu, 28 May 2026 21:35:26 GMT
COPY --chown=logstash:root env2yaml/lib /usr/share/logstash/env2yaml/lib/ # buildkit
# Thu, 28 May 2026 21:35:26 GMT
COPY --chmod=0755 env2yaml/env2yaml /usr/local/bin/env2yaml # buildkit
# Thu, 28 May 2026 21:35:26 GMT
COPY --chown=logstash:root config/pipelines.yml config/log4j2.properties config/log4j2.file.properties /usr/share/logstash/config/ # buildkit
# Thu, 28 May 2026 21:35:26 GMT
COPY --chown=logstash:root config/logstash-full.yml /usr/share/logstash/config/logstash.yml # buildkit
# Thu, 28 May 2026 21:35:26 GMT
COPY --chown=logstash:root pipeline/default.conf /usr/share/logstash/pipeline/logstash.conf # buildkit
# Thu, 28 May 2026 21:35:26 GMT
COPY --chmod=0755 bin/docker-entrypoint /usr/local/bin/ # buildkit
# Thu, 28 May 2026 21:35:26 GMT
WORKDIR /usr/share/logstash
# Thu, 28 May 2026 21:35:26 GMT
USER 1000
# Thu, 28 May 2026 21:35:26 GMT
EXPOSE map[5044/tcp:{} 9600/tcp:{}]
# Thu, 28 May 2026 21:35:26 GMT
LABEL org.label-schema.build-date=2026-05-23T16:23:32+00:00 org.label-schema.license=Elastic License org.label-schema.name=logstash org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/logstash org.label-schema.vcs-url=https://github.com/elastic/logstash org.label-schema.vendor=Elastic org.label-schema.version=9.3.5 org.opencontainers.image.created=2026-05-23T16:23:32+00:00 org.opencontainers.image.description=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' org.opencontainers.image.licenses=Elastic License org.opencontainers.image.title=logstash org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=9.3.5 description=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' license=Elastic License maintainer=info@elastic.co name=logstash summary=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' vendor=Elastic
# Thu, 28 May 2026 21:35:26 GMT
ENTRYPOINT ["/usr/local/bin/docker-entrypoint"]
```

-	Layers:
	-	`sha256:1a36cba5a1d845cee5e57e6f2dc9f828b4cc53403e207333e2220cd426126f13`  
		Last Modified: Tue, 26 May 2026 18:02:56 GMT  
		Size: 40.7 MB (40708696 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e505e7b9bbe35113c1e65fe99615b45ba2b70621f328e1904870a3c01c1af37`  
		Last Modified: Thu, 28 May 2026 21:36:03 GMT  
		Size: 4.8 MB (4773515 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80f23f96fcb84fa9818f3357ff39b0698135eae91cab0aa6e095445fa3586071`  
		Last Modified: Thu, 28 May 2026 21:36:12 GMT  
		Size: 472.3 MB (472278634 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e37eb42b563c1dfabf22a266bb7e43f3961f58a8b4a8d1baab2e3065c3dc6bf6`  
		Last Modified: Thu, 28 May 2026 21:36:03 GMT  
		Size: 6.3 KB (6293 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3af3f6e120a561a6d5d1a90424f1c9ec54eb59dbe97308e0fb3a01795b47f34`  
		Last Modified: Thu, 28 May 2026 21:36:03 GMT  
		Size: 255.2 KB (255182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e1ec7d595391457357834fccdd1143cc90fabcec63b760b710f91cddbede8f2`  
		Last Modified: Thu, 28 May 2026 21:36:04 GMT  
		Size: 353.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8f89c855dcc67446bade3d81761c9b8f116b5c6bee2bdb873f706e8b6f29edc`  
		Last Modified: Thu, 28 May 2026 21:36:04 GMT  
		Size: 1.6 KB (1576 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3a743ff5ff1c8d6eef4e45f5e5a3f347df2dcc9af4464e8d2b7f06acea6eacf`  
		Last Modified: Thu, 28 May 2026 21:36:05 GMT  
		Size: 278.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13529be416436fba7b3294af063c2c097b759e14346e25ad8387a8a788a26f8a`  
		Last Modified: Thu, 28 May 2026 21:36:05 GMT  
		Size: 278.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:176ec468b24e54236db3f544bf2b267f0c9496f9b85efa70bc4a01a7d7401c85`  
		Last Modified: Thu, 28 May 2026 21:36:05 GMT  
		Size: 711.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `logstash:9.3.5` - unknown; unknown

```console
$ docker pull logstash@sha256:3e9783e061ab5241202a622e7d1c5c186a305db6bbbf71ac68dd41025817a18c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2142095 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fbf1dd9f6dec157cc4e4863c440dbaa5a146a0e58a01a845cac4586ab872fef7`

```dockerfile
```

-	Layers:
	-	`sha256:8a25578a6379d987b3fb84e73bcb88c578262347edae81960ecc9a98f9e53323`  
		Last Modified: Thu, 28 May 2026 21:36:03 GMT  
		Size: 2.1 MB (2111895 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fe0e143a3c456231074a809c63027b616d0037dd4f5c94a168e9b58c92e8650f`  
		Last Modified: Thu, 28 May 2026 21:36:03 GMT  
		Size: 30.2 KB (30200 bytes)  
		MIME: application/vnd.in-toto+json

### `logstash:9.3.5` - linux; arm64 variant v8

```console
$ docker pull logstash@sha256:86750b5701926eb039033d22bef83ee278472f9fe92d608a9d00dbeb5bbf200d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **514.5 MB (514452964 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb9fbd3496f09b89cba26c58fee0572bdbc0c63d673175c2c6f75297463c6e23`
-	Entrypoint: `["\/usr\/local\/bin\/docker-entrypoint"]`

```dockerfile
# Tue, 26 May 2026 15:34:04 GMT
LABEL maintainer="Red Hat, Inc."
# Tue, 26 May 2026 15:34:04 GMT
LABEL vendor="Red Hat, Inc."
# Tue, 26 May 2026 15:34:04 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Tue, 26 May 2026 15:34:04 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.8"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Tue, 26 May 2026 15:34:05 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Tue, 26 May 2026 15:34:05 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Tue, 26 May 2026 15:34:05 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Tue, 26 May 2026 15:34:05 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Tue, 26 May 2026 15:34:05 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Tue, 26 May 2026 15:34:05 GMT
LABEL io.openshift.expose-services=""
# Tue, 26 May 2026 15:34:05 GMT
LABEL io.openshift.tags="minimal rhel9"
# Tue, 26 May 2026 15:34:05 GMT
ENV container oci
# Tue, 26 May 2026 15:34:06 GMT
COPY dir:9311212a31ee4f8d868b9de6ebae2a0a4e5d17aa2e21f16141915c8746951a19 in /      
# Tue, 26 May 2026 15:34:06 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Tue, 26 May 2026 15:34:06 GMT
CMD ["/bin/bash"]
# Tue, 26 May 2026 15:34:06 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /usr/share/buildinfo/content-sets.json      
# Tue, 26 May 2026 15:34:06 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /root/buildinfo/content_manifests/content-sets.json      
# Tue, 26 May 2026 15:34:06 GMT
COPY file:ef2297de91351ccfd309c3f31893d4ad2d2e0f74bd425a0ed7ac8183f24ad2ed in /usr/share/buildinfo/labels.json      
# Tue, 26 May 2026 15:34:06 GMT
COPY file:ef2297de91351ccfd309c3f31893d4ad2d2e0f74bd425a0ed7ac8183f24ad2ed in /root/buildinfo/labels.json      
# Tue, 26 May 2026 15:34:06 GMT
LABEL "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="106f2a33b03195c917e783d47463c6f8e17f7458" "org.opencontainers.image.revision"="106f2a33b03195c917e783d47463c6f8e17f7458" "build-date"="2026-05-26T15:33:51Z" "org.opencontainers.image.created"="2026-05-26T15:33:51Z" "release"="1779809423"org.opencontainers.image.revision=106f2a33b03195c917e783d47463c6f8e17f7458,org.opencontainers.image.created=2026-05-26T15:33:51Z
# Thu, 28 May 2026 21:35:26 GMT
ENV ELASTIC_CONTAINER=true
# Thu, 28 May 2026 21:35:26 GMT
ENV PATH=/usr/share/logstash/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 28 May 2026 21:35:26 GMT
ENV LANG=C.UTF-8 LC_ALL=C.UTF-8
# Thu, 28 May 2026 21:35:26 GMT
WORKDIR /usr/share
# Thu, 28 May 2026 21:35:28 GMT
RUN microdnf install -y procps findutils tar gzip &&   microdnf install -y openssl &&   microdnf install -y which shadow-utils &&   microdnf clean all # buildkit
# Thu, 28 May 2026 21:35:56 GMT
RUN groupadd --gid 1000 logstash &&   adduser --uid 1000 --gid 1000   --home "/usr/share/logstash"   --no-create-home   logstash &&   arch="$(rpm --query --queryformat='%{ARCH}' rpm)" &&   curl --fail --location --output logstash.tar.gz https://artifacts.elastic.co/downloads/logstash/logstash-9.3.5-linux-${arch}.tar.gz &&   tar -zxf logstash.tar.gz -C /usr/share &&   rm logstash.tar.gz &&   mv /usr/share/logstash-9.3.5 /usr/share/logstash &&   chown -R logstash:root /usr/share/logstash &&   chmod -R g=u /usr/share/logstash &&   mkdir /licenses &&   mv /usr/share/logstash/NOTICE.TXT /licenses/NOTICE.TXT &&   mv /usr/share/logstash/LICENSE.txt /licenses/LICENSE.txt &&   find /usr/share/logstash -type d -exec chmod g+s {} \; &&   ln -s /usr/share/logstash /opt/logstash # buildkit
# Thu, 28 May 2026 21:35:56 GMT
COPY --chown=logstash:root env2yaml/classes /usr/share/logstash/env2yaml/classes/ # buildkit
# Thu, 28 May 2026 21:35:56 GMT
COPY --chown=logstash:root env2yaml/lib /usr/share/logstash/env2yaml/lib/ # buildkit
# Thu, 28 May 2026 21:35:57 GMT
COPY --chmod=0755 env2yaml/env2yaml /usr/local/bin/env2yaml # buildkit
# Thu, 28 May 2026 21:35:57 GMT
COPY --chown=logstash:root config/pipelines.yml config/log4j2.properties config/log4j2.file.properties /usr/share/logstash/config/ # buildkit
# Thu, 28 May 2026 21:35:57 GMT
COPY --chown=logstash:root config/logstash-full.yml /usr/share/logstash/config/logstash.yml # buildkit
# Thu, 28 May 2026 21:35:57 GMT
COPY --chown=logstash:root pipeline/default.conf /usr/share/logstash/pipeline/logstash.conf # buildkit
# Thu, 28 May 2026 21:35:57 GMT
COPY --chmod=0755 bin/docker-entrypoint /usr/local/bin/ # buildkit
# Thu, 28 May 2026 21:35:57 GMT
WORKDIR /usr/share/logstash
# Thu, 28 May 2026 21:35:57 GMT
USER 1000
# Thu, 28 May 2026 21:35:57 GMT
EXPOSE map[5044/tcp:{} 9600/tcp:{}]
# Thu, 28 May 2026 21:35:57 GMT
LABEL org.label-schema.build-date=2026-05-23T16:23:32+00:00 org.label-schema.license=Elastic License org.label-schema.name=logstash org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/logstash org.label-schema.vcs-url=https://github.com/elastic/logstash org.label-schema.vendor=Elastic org.label-schema.version=9.3.5 org.opencontainers.image.created=2026-05-23T16:23:32+00:00 org.opencontainers.image.description=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' org.opencontainers.image.licenses=Elastic License org.opencontainers.image.title=logstash org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=9.3.5 description=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' license=Elastic License maintainer=info@elastic.co name=logstash summary=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' vendor=Elastic
# Thu, 28 May 2026 21:35:57 GMT
ENTRYPOINT ["/usr/local/bin/docker-entrypoint"]
```

-	Layers:
	-	`sha256:96e18ab71592420b36f7601002b695ecc23bf6b95f86193c23b2753544d31b8a`  
		Last Modified: Tue, 26 May 2026 18:00:10 GMT  
		Size: 38.8 MB (38840156 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5e3e8a8dde2e6040eeafb0948722ce10653d243794dcd89402bf45edeff511d`  
		Last Modified: Thu, 28 May 2026 21:36:35 GMT  
		Size: 4.8 MB (4770745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90543f307c80c9f09ff08f613d4f91415e454d9c204d2071f8e2310001e40029`  
		Last Modified: Thu, 28 May 2026 21:36:44 GMT  
		Size: 470.6 MB (470577327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76044b2e474a06a0a86bab41d910c22d0998d97ef913da98a7ca3b8b3ef10cc6`  
		Last Modified: Thu, 28 May 2026 21:36:34 GMT  
		Size: 6.3 KB (6294 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67ed8a56629dce3aa78dab5f5e3773590398364bc819c1dea9a9348e67559f56`  
		Last Modified: Thu, 28 May 2026 21:36:34 GMT  
		Size: 255.2 KB (255182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ab3ee8074767ca934012e37800c51888057b0c09b98929205b484af24186d60`  
		Last Modified: Thu, 28 May 2026 21:36:36 GMT  
		Size: 352.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2fc93a5822157e9a70bcb0f2283db597cd43d6aa20082b7be5faf2a7b685188`  
		Last Modified: Thu, 28 May 2026 21:36:36 GMT  
		Size: 1.6 KB (1578 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa5a5e16dcbdaf3d9554e5fb9a44f187c9f366f198e901af11a6242ef5a28546`  
		Last Modified: Thu, 28 May 2026 21:36:36 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07e00ee7c947c85bf5fc52cc911e1c9bfab7f2cf257757b0adeef3a2a6d00992`  
		Last Modified: Thu, 28 May 2026 21:36:37 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee702cfa950fcaccb3838d448f9acfc0e1c8e1cff981890b8dd4c7a7b0d86c07`  
		Last Modified: Thu, 28 May 2026 21:36:37 GMT  
		Size: 712.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `logstash:9.3.5` - unknown; unknown

```console
$ docker pull logstash@sha256:ed38de96e8e438e97ecc6bbfd8c8b72665888717a2cdc91631c414179eeaccc5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2142742 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:93e1dd18f6acb675a372b96816e0e502bad2ba00013af9bf55c60346f4ab5f62`

```dockerfile
```

-	Layers:
	-	`sha256:e577ef5a6163653a17d99a2fc48d41c294087cc1fca5220e1ea1d48849f1d111`  
		Last Modified: Thu, 28 May 2026 21:36:34 GMT  
		Size: 2.1 MB (2112465 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6fceefdf4c4fc806158da951debcb928f0232ba088b2c5584d82bafef10c3356`  
		Last Modified: Thu, 28 May 2026 21:36:34 GMT  
		Size: 30.3 KB (30277 bytes)  
		MIME: application/vnd.in-toto+json

## `logstash:9.4.2`

```console
$ docker pull logstash@sha256:5c0700e37f1afab75b63705677cf058925a12886d3fbd38fceb32b0839c2f176
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `logstash:9.4.2` - linux; amd64

```console
$ docker pull logstash@sha256:c4097b54299c93ef2642ab75efd0480035c19289533416fe5593b76403b555c9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **524.5 MB (524461689 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:724ca47aa4f459bde9e740ab73d1e5bbc010b4b7c6915b88d0046ca6049a409c`
-	Entrypoint: `["\/usr\/local\/bin\/docker-entrypoint"]`

```dockerfile
# Tue, 26 May 2026 15:32:20 GMT
LABEL maintainer="Red Hat, Inc."
# Tue, 26 May 2026 15:32:20 GMT
LABEL vendor="Red Hat, Inc."
# Tue, 26 May 2026 15:32:20 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Tue, 26 May 2026 15:32:20 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.8"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Tue, 26 May 2026 15:32:20 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Tue, 26 May 2026 15:32:20 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Tue, 26 May 2026 15:32:20 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Tue, 26 May 2026 15:32:20 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Tue, 26 May 2026 15:32:21 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Tue, 26 May 2026 15:32:21 GMT
LABEL io.openshift.expose-services=""
# Tue, 26 May 2026 15:32:21 GMT
LABEL io.openshift.tags="minimal rhel9"
# Tue, 26 May 2026 15:32:21 GMT
ENV container oci
# Tue, 26 May 2026 15:32:22 GMT
COPY dir:bcf46f8211a223ea361ec9cb0b5d7567aaf9ce54beddfddade034948e142ca6d in /      
# Tue, 26 May 2026 15:32:22 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Tue, 26 May 2026 15:32:22 GMT
CMD ["/bin/bash"]
# Tue, 26 May 2026 15:32:22 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /usr/share/buildinfo/content-sets.json      
# Tue, 26 May 2026 15:32:23 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /root/buildinfo/content_manifests/content-sets.json      
# Tue, 26 May 2026 15:32:23 GMT
COPY file:227070320251c0bebb0aee79adad2b4d241a94b8936d1e12e22f0f0015cd467b in /usr/share/buildinfo/labels.json      
# Tue, 26 May 2026 15:32:23 GMT
COPY file:227070320251c0bebb0aee79adad2b4d241a94b8936d1e12e22f0f0015cd467b in /root/buildinfo/labels.json      
# Tue, 26 May 2026 15:32:23 GMT
LABEL "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="106f2a33b03195c917e783d47463c6f8e17f7458" "org.opencontainers.image.revision"="106f2a33b03195c917e783d47463c6f8e17f7458" "build-date"="2026-05-26T15:32:02Z" "org.opencontainers.image.created"="2026-05-26T15:32:02Z" "release"="1779809423"org.opencontainers.image.revision=106f2a33b03195c917e783d47463c6f8e17f7458,org.opencontainers.image.created=2026-05-26T15:32:02Z
# Thu, 28 May 2026 21:34:55 GMT
ENV ELASTIC_CONTAINER=true
# Thu, 28 May 2026 21:34:55 GMT
ENV PATH=/usr/share/logstash/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 28 May 2026 21:34:55 GMT
ENV LANG=C.UTF-8 LC_ALL=C.UTF-8
# Thu, 28 May 2026 21:34:55 GMT
WORKDIR /usr/share
# Thu, 28 May 2026 21:34:56 GMT
RUN microdnf install -y procps findutils tar gzip &&   microdnf install -y openssl &&   microdnf install -y which shadow-utils &&   microdnf clean all # buildkit
# Thu, 28 May 2026 21:37:09 GMT
RUN groupadd --gid 1000 logstash &&   adduser --uid 1000 --gid 1000   --home "/usr/share/logstash"   --no-create-home   logstash &&   arch="$(rpm --query --queryformat='%{ARCH}' rpm)" &&   curl --fail --location --output logstash.tar.gz https://artifacts.elastic.co/downloads/logstash/logstash-9.4.2-linux-${arch}.tar.gz &&   tar -zxf logstash.tar.gz -C /usr/share &&   rm logstash.tar.gz &&   mv /usr/share/logstash-9.4.2 /usr/share/logstash &&   chown -R logstash:root /usr/share/logstash &&   chmod -R g=u /usr/share/logstash &&   mkdir /licenses &&   mv /usr/share/logstash/NOTICE.TXT /licenses/NOTICE.TXT &&   mv /usr/share/logstash/LICENSE.txt /licenses/LICENSE.txt &&   find /usr/share/logstash -type d -exec chmod g+s {} \; &&   ln -s /usr/share/logstash /opt/logstash # buildkit
# Thu, 28 May 2026 21:37:09 GMT
COPY --chown=logstash:root env2yaml/classes /usr/share/logstash/env2yaml/classes/ # buildkit
# Thu, 28 May 2026 21:37:09 GMT
COPY --chown=logstash:root env2yaml/lib /usr/share/logstash/env2yaml/lib/ # buildkit
# Thu, 28 May 2026 21:37:09 GMT
COPY --chmod=0755 env2yaml/env2yaml /usr/local/bin/env2yaml # buildkit
# Thu, 28 May 2026 21:37:09 GMT
COPY --chown=logstash:root config/pipelines.yml config/log4j2.properties config/log4j2.file.properties /usr/share/logstash/config/ # buildkit
# Thu, 28 May 2026 21:37:09 GMT
COPY --chown=logstash:root config/logstash-full.yml /usr/share/logstash/config/logstash.yml # buildkit
# Thu, 28 May 2026 21:37:09 GMT
COPY --chown=logstash:root pipeline/default.conf /usr/share/logstash/pipeline/logstash.conf # buildkit
# Thu, 28 May 2026 21:37:09 GMT
COPY --chmod=0755 bin/docker-entrypoint /usr/local/bin/ # buildkit
# Thu, 28 May 2026 21:37:09 GMT
WORKDIR /usr/share/logstash
# Thu, 28 May 2026 21:37:09 GMT
USER 1000
# Thu, 28 May 2026 21:37:09 GMT
EXPOSE map[5044/tcp:{} 9600/tcp:{}]
# Thu, 28 May 2026 21:37:09 GMT
LABEL org.label-schema.build-date=2026-05-23T16:25:00+00:00 org.label-schema.license=Elastic License org.label-schema.name=logstash org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/logstash org.label-schema.vcs-url=https://github.com/elastic/logstash org.label-schema.vendor=Elastic org.label-schema.version=9.4.2 org.opencontainers.image.created=2026-05-23T16:25:00+00:00 org.opencontainers.image.description=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' org.opencontainers.image.licenses=Elastic License org.opencontainers.image.title=logstash org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=9.4.2 description=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' license=Elastic License maintainer=info@elastic.co name=logstash summary=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' vendor=Elastic
# Thu, 28 May 2026 21:37:09 GMT
ENTRYPOINT ["/usr/local/bin/docker-entrypoint"]
```

-	Layers:
	-	`sha256:1a36cba5a1d845cee5e57e6f2dc9f828b4cc53403e207333e2220cd426126f13`  
		Last Modified: Tue, 26 May 2026 18:02:56 GMT  
		Size: 40.7 MB (40708696 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e505e7b9bbe35113c1e65fe99615b45ba2b70621f328e1904870a3c01c1af37`  
		Last Modified: Thu, 28 May 2026 21:36:03 GMT  
		Size: 4.8 MB (4773515 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a6803e430e557dd0af4be3e5b083695db28fdef85a03ff7e658f73a423f82ef`  
		Last Modified: Thu, 28 May 2026 21:37:57 GMT  
		Size: 478.7 MB (478714664 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a9907f41401ff73ebd4e4e0a1610fa69b9ae1d7bae6ba8e681bf1bb345834ad`  
		Last Modified: Thu, 28 May 2026 21:37:47 GMT  
		Size: 6.4 KB (6367 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:daade4d74fcc046473c7998091dbfd08d5d4ed7c8a9140f3aebb68b4221d9c5a`  
		Last Modified: Thu, 28 May 2026 21:37:47 GMT  
		Size: 255.2 KB (255186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3121a23305055a9a6748ff3ac1b5b2f045d0548a4ac970795b6049723c81d709`  
		Last Modified: Thu, 28 May 2026 21:37:47 GMT  
		Size: 354.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62fa948bd9a1ae765ee674226636aa3388ab64e5f44ebac49ac02bbefc1b5926`  
		Last Modified: Thu, 28 May 2026 21:37:48 GMT  
		Size: 1.6 KB (1575 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e54479e82abe92ce80ebbecb07ba3be464cb19ad3f5642eb0eaef30a4bb0030`  
		Last Modified: Thu, 28 May 2026 21:37:48 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61dded88c0dec14dd7e42ceea3815c53d71f596a6188b9c346ff086a8206cf45`  
		Last Modified: Thu, 28 May 2026 21:37:49 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5aa9f9ecc2fef77821d263631f2a88e19c9c5b16b933058c64127ba78306fccd`  
		Last Modified: Thu, 28 May 2026 21:37:50 GMT  
		Size: 713.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `logstash:9.4.2` - unknown; unknown

```console
$ docker pull logstash@sha256:6812a147afab4a0f1fa7d9f7f2e5c9fee46f93eaca4b90dd822e99dea6245524
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2148093 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:675332d892355b1536ace3a7d3fda0e72924af998bd72693cbab055964d42dc1`

```dockerfile
```

-	Layers:
	-	`sha256:7a4a69d0119ca2df1579cbd06458b355def2c3c36dc07475ba05c9fba6e4f20c`  
		Last Modified: Thu, 28 May 2026 21:37:47 GMT  
		Size: 2.1 MB (2117893 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7436659cc660132d89ba3a51fcf77feb9f144ffae1ee2f7d7454729fdabaaeb9`  
		Last Modified: Thu, 28 May 2026 21:37:47 GMT  
		Size: 30.2 KB (30200 bytes)  
		MIME: application/vnd.in-toto+json

### `logstash:9.4.2` - linux; arm64 variant v8

```console
$ docker pull logstash@sha256:002ffdf276aa7c5a28a718cd76b934c1e30fbac538deb74ddd9ebe3835eecbda
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **520.9 MB (520886128 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad131ec0c3878d7112c26ff64d78378261c43fcf994d7d065c588cffc0fd95f7`
-	Entrypoint: `["\/usr\/local\/bin\/docker-entrypoint"]`

```dockerfile
# Tue, 26 May 2026 15:34:04 GMT
LABEL maintainer="Red Hat, Inc."
# Tue, 26 May 2026 15:34:04 GMT
LABEL vendor="Red Hat, Inc."
# Tue, 26 May 2026 15:34:04 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Tue, 26 May 2026 15:34:04 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.8"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Tue, 26 May 2026 15:34:05 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Tue, 26 May 2026 15:34:05 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Tue, 26 May 2026 15:34:05 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Tue, 26 May 2026 15:34:05 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Tue, 26 May 2026 15:34:05 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Tue, 26 May 2026 15:34:05 GMT
LABEL io.openshift.expose-services=""
# Tue, 26 May 2026 15:34:05 GMT
LABEL io.openshift.tags="minimal rhel9"
# Tue, 26 May 2026 15:34:05 GMT
ENV container oci
# Tue, 26 May 2026 15:34:06 GMT
COPY dir:9311212a31ee4f8d868b9de6ebae2a0a4e5d17aa2e21f16141915c8746951a19 in /      
# Tue, 26 May 2026 15:34:06 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Tue, 26 May 2026 15:34:06 GMT
CMD ["/bin/bash"]
# Tue, 26 May 2026 15:34:06 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /usr/share/buildinfo/content-sets.json      
# Tue, 26 May 2026 15:34:06 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /root/buildinfo/content_manifests/content-sets.json      
# Tue, 26 May 2026 15:34:06 GMT
COPY file:ef2297de91351ccfd309c3f31893d4ad2d2e0f74bd425a0ed7ac8183f24ad2ed in /usr/share/buildinfo/labels.json      
# Tue, 26 May 2026 15:34:06 GMT
COPY file:ef2297de91351ccfd309c3f31893d4ad2d2e0f74bd425a0ed7ac8183f24ad2ed in /root/buildinfo/labels.json      
# Tue, 26 May 2026 15:34:06 GMT
LABEL "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="106f2a33b03195c917e783d47463c6f8e17f7458" "org.opencontainers.image.revision"="106f2a33b03195c917e783d47463c6f8e17f7458" "build-date"="2026-05-26T15:33:51Z" "org.opencontainers.image.created"="2026-05-26T15:33:51Z" "release"="1779809423"org.opencontainers.image.revision=106f2a33b03195c917e783d47463c6f8e17f7458,org.opencontainers.image.created=2026-05-26T15:33:51Z
# Thu, 28 May 2026 21:35:19 GMT
ENV ELASTIC_CONTAINER=true
# Thu, 28 May 2026 21:35:19 GMT
ENV PATH=/usr/share/logstash/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 28 May 2026 21:35:19 GMT
ENV LANG=C.UTF-8 LC_ALL=C.UTF-8
# Thu, 28 May 2026 21:35:19 GMT
WORKDIR /usr/share
# Thu, 28 May 2026 21:35:21 GMT
RUN microdnf install -y procps findutils tar gzip &&   microdnf install -y openssl &&   microdnf install -y which shadow-utils &&   microdnf clean all # buildkit
# Thu, 28 May 2026 21:35:51 GMT
RUN groupadd --gid 1000 logstash &&   adduser --uid 1000 --gid 1000   --home "/usr/share/logstash"   --no-create-home   logstash &&   arch="$(rpm --query --queryformat='%{ARCH}' rpm)" &&   curl --fail --location --output logstash.tar.gz https://artifacts.elastic.co/downloads/logstash/logstash-9.4.2-linux-${arch}.tar.gz &&   tar -zxf logstash.tar.gz -C /usr/share &&   rm logstash.tar.gz &&   mv /usr/share/logstash-9.4.2 /usr/share/logstash &&   chown -R logstash:root /usr/share/logstash &&   chmod -R g=u /usr/share/logstash &&   mkdir /licenses &&   mv /usr/share/logstash/NOTICE.TXT /licenses/NOTICE.TXT &&   mv /usr/share/logstash/LICENSE.txt /licenses/LICENSE.txt &&   find /usr/share/logstash -type d -exec chmod g+s {} \; &&   ln -s /usr/share/logstash /opt/logstash # buildkit
# Thu, 28 May 2026 21:35:51 GMT
COPY --chown=logstash:root env2yaml/classes /usr/share/logstash/env2yaml/classes/ # buildkit
# Thu, 28 May 2026 21:35:51 GMT
COPY --chown=logstash:root env2yaml/lib /usr/share/logstash/env2yaml/lib/ # buildkit
# Thu, 28 May 2026 21:35:51 GMT
COPY --chmod=0755 env2yaml/env2yaml /usr/local/bin/env2yaml # buildkit
# Thu, 28 May 2026 21:35:51 GMT
COPY --chown=logstash:root config/pipelines.yml config/log4j2.properties config/log4j2.file.properties /usr/share/logstash/config/ # buildkit
# Thu, 28 May 2026 21:35:51 GMT
COPY --chown=logstash:root config/logstash-full.yml /usr/share/logstash/config/logstash.yml # buildkit
# Thu, 28 May 2026 21:35:52 GMT
COPY --chown=logstash:root pipeline/default.conf /usr/share/logstash/pipeline/logstash.conf # buildkit
# Thu, 28 May 2026 21:35:52 GMT
COPY --chmod=0755 bin/docker-entrypoint /usr/local/bin/ # buildkit
# Thu, 28 May 2026 21:35:52 GMT
WORKDIR /usr/share/logstash
# Thu, 28 May 2026 21:35:52 GMT
USER 1000
# Thu, 28 May 2026 21:35:52 GMT
EXPOSE map[5044/tcp:{} 9600/tcp:{}]
# Thu, 28 May 2026 21:35:52 GMT
LABEL org.label-schema.build-date=2026-05-23T16:25:00+00:00 org.label-schema.license=Elastic License org.label-schema.name=logstash org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/logstash org.label-schema.vcs-url=https://github.com/elastic/logstash org.label-schema.vendor=Elastic org.label-schema.version=9.4.2 org.opencontainers.image.created=2026-05-23T16:25:00+00:00 org.opencontainers.image.description=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' org.opencontainers.image.licenses=Elastic License org.opencontainers.image.title=logstash org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=9.4.2 description=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' license=Elastic License maintainer=info@elastic.co name=logstash summary=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' vendor=Elastic
# Thu, 28 May 2026 21:35:52 GMT
ENTRYPOINT ["/usr/local/bin/docker-entrypoint"]
```

-	Layers:
	-	`sha256:96e18ab71592420b36f7601002b695ecc23bf6b95f86193c23b2753544d31b8a`  
		Last Modified: Tue, 26 May 2026 18:00:10 GMT  
		Size: 38.8 MB (38840156 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae0c76281163e21f9cdba8393ea2be6a1d9c50d45a59ce1eae9473b6465d40e9`  
		Last Modified: Thu, 28 May 2026 21:36:33 GMT  
		Size: 4.8 MB (4770771 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf578cccaf455e57e81d79605e82f6e05e26350910446c85f0f3961af21578d9`  
		Last Modified: Thu, 28 May 2026 21:36:41 GMT  
		Size: 477.0 MB (477010398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df9af6741cc0a35e4b1b704af11cb7aad92f38fd70d614371e31e70552762bd8`  
		Last Modified: Thu, 28 May 2026 21:36:33 GMT  
		Size: 6.4 KB (6363 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2dde52ae88b8ab3c574e1bdd1723a4bb5a71fa83e0cafb461055bc11eae48633`  
		Last Modified: Thu, 28 May 2026 21:36:33 GMT  
		Size: 255.2 KB (255182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1eac4938ebffe25556fe4733bbfe2b37460bd32766986d3d58c1117b4a930870`  
		Last Modified: Thu, 28 May 2026 21:36:34 GMT  
		Size: 355.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af218316bc014fea7305aee45bafae1e91567be36ae9f7f8a22a6636a9a35c79`  
		Last Modified: Thu, 28 May 2026 21:36:34 GMT  
		Size: 1.6 KB (1576 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d67d624fc6c32c0f600cbc03a7408ae7488a250853ad8ece71f327a7a1e82ef2`  
		Last Modified: Thu, 28 May 2026 21:36:34 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0c695dc16662b0b7689b49b0d8670d8590792c7b20eeaf09f72225e0412edba`  
		Last Modified: Thu, 28 May 2026 21:36:35 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f3e97ad16243c174168bbc24116e958e755757a1b14b28704d4ded6bf3bef90`  
		Last Modified: Thu, 28 May 2026 21:36:35 GMT  
		Size: 711.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `logstash:9.4.2` - unknown; unknown

```console
$ docker pull logstash@sha256:e5cff9df5664379b910f4e6a1d9e16ca5c26d1197e96fa4e740efba612fde32c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2148740 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b092516570413453f802fb7cdff5496676e2173da5d0a4aaeee2b449d905072c`

```dockerfile
```

-	Layers:
	-	`sha256:3a03fe4d276dc4ca69bf6d59a39560be30ea9e855cf6e1c9281f4850b6efee61`  
		Last Modified: Thu, 28 May 2026 21:36:33 GMT  
		Size: 2.1 MB (2118463 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ac6618eb208685b9d5019611ce07f17402fb2af93041d873cf55d75dec72c37c`  
		Last Modified: Thu, 28 May 2026 21:36:32 GMT  
		Size: 30.3 KB (30277 bytes)  
		MIME: application/vnd.in-toto+json
