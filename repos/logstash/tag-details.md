<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `logstash`

-	[`logstash:8.19.12`](#logstash81912)
-	[`logstash:9.2.6`](#logstash926)
-	[`logstash:9.3.1`](#logstash931)

## `logstash:8.19.12`

```console
$ docker pull logstash@sha256:8705d6acdc44e2acd5cb58c14d0b2a547ec7692faa4b71dde8e70fdf5c276783
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `logstash:8.19.12` - linux; amd64

```console
$ docker pull logstash@sha256:dcde08c021533c70f83d4440c9174e218b6ec674eb57f31f7740555d45656bcd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **534.5 MB (534503071 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:875fba3fd9f22f6f69e58b45b453f3b116b57af712c62b6b1010ea9167f57e9f`
-	Entrypoint: `["\/usr\/local\/bin\/docker-entrypoint"]`

```dockerfile
# Tue, 10 Feb 2026 16:49:54 GMT
ARG RELEASE
# Tue, 10 Feb 2026 16:49:54 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 10 Feb 2026 16:49:54 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 10 Feb 2026 16:49:54 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 10 Feb 2026 16:49:56 GMT
ADD file:1ae27d2ef4369361104b699712f3897141e394785df5d193d67b44626f57eb87 in / 
# Tue, 10 Feb 2026 16:49:57 GMT
CMD ["/bin/bash"]
# Thu, 26 Feb 2026 19:04:16 GMT
RUN for iter in {1..10}; do       export DEBIAN_FRONTEND=noninteractive &&     apt-get update -y &&   apt-get upgrade -y &&   apt-get install -y procps findutils tar gzip &&         apt-get install -y locales &&         apt-get install -y curl &&     apt-get clean all &&       locale-gen 'en_US.UTF-8' &&     apt-get clean metadata &&   exit_code=0 && break || exit_code=$? && echo "packaging error: retry $iter in 10s" && apt-get clean all &&   apt-get clean metadata && sleep 10; done; (exit $exit_code) # buildkit
# Thu, 26 Feb 2026 19:04:16 GMT
RUN userdel -r ubuntu && groupadd --gid 1000 logstash &&   useradd --uid 1000 --gid 1000 --home /usr/share/logstash --no-create-home logstash # buildkit
# Thu, 26 Feb 2026 19:14:24 GMT
RUN curl -Lo - https://artifacts.elastic.co/downloads/logstash/logstash-8.19.12-linux-$(arch).tar.gz |   tar zxf - -C /usr/share &&   mv /usr/share/logstash-8.19.12 /usr/share/logstash &&   chown --recursive logstash:logstash /usr/share/logstash/ &&   chown -R logstash:root /usr/share/logstash &&   chmod -R g=u /usr/share/logstash &&   mkdir /licenses/ &&   mv /usr/share/logstash/NOTICE.TXT /licenses/NOTICE.TXT &&   mv /usr/share/logstash/LICENSE.txt /licenses/LICENSE.txt &&   find /usr/share/logstash -type d -exec chmod g+s {} \; &&   ln -s /usr/share/logstash /opt/logstash # buildkit
# Thu, 26 Feb 2026 19:14:24 GMT
WORKDIR /usr/share/logstash
# Thu, 26 Feb 2026 19:14:24 GMT
ENV ELASTIC_CONTAINER=true
# Thu, 26 Feb 2026 19:14:24 GMT
ENV PATH=/usr/share/logstash/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 26 Feb 2026 19:14:24 GMT
COPY config/logstash-full.yml config/logstash.yml # buildkit
# Thu, 26 Feb 2026 19:14:24 GMT
COPY config/pipelines.yml config/log4j2.properties config/log4j2.file.properties config/ # buildkit
# Thu, 26 Feb 2026 19:14:24 GMT
COPY pipeline/default.conf pipeline/logstash.conf # buildkit
# Thu, 26 Feb 2026 19:14:24 GMT
RUN chown --recursive logstash:root config/ pipeline/ # buildkit
# Thu, 26 Feb 2026 19:14:24 GMT
ENV LANG=en_US.UTF-8 LC_ALL=en_US.UTF-8
# Thu, 26 Feb 2026 19:14:24 GMT
COPY --chown=logstash:root env2yaml/classes /usr/share/logstash/env2yaml/classes/ # buildkit
# Thu, 26 Feb 2026 19:14:24 GMT
COPY --chown=logstash:root env2yaml/lib /usr/share/logstash/env2yaml/lib/ # buildkit
# Thu, 26 Feb 2026 19:14:24 GMT
COPY --chmod=0755 env2yaml/env2yaml /usr/local/bin/env2yaml # buildkit
# Thu, 26 Feb 2026 19:14:24 GMT
COPY bin/docker-entrypoint /usr/local/bin/ # buildkit
# Thu, 26 Feb 2026 19:14:24 GMT
RUN chmod 0755 /usr/local/bin/docker-entrypoint # buildkit
# Thu, 26 Feb 2026 19:14:24 GMT
USER 1000
# Thu, 26 Feb 2026 19:14:24 GMT
EXPOSE map[5044/tcp:{} 9600/tcp:{}]
# Thu, 26 Feb 2026 19:14:24 GMT
LABEL org.label-schema.schema-version=1.0 org.label-schema.vendor=Elastic org.opencontainers.image.vendor=Elastic org.label-schema.name=logstash org.opencontainers.image.title=logstash org.label-schema.version=8.19.12 org.opencontainers.image.version=8.19.12 org.label-schema.url=https://www.elastic.co/products/logstash org.label-schema.vcs-url=https://github.com/elastic/logstash org.label-schema.license=Elastic License org.opencontainers.image.licenses=Elastic License org.opencontainers.image.description=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' org.label-schema.build-date=2026-02-18T12:09:10+00:00 org.opencontainers.image.created=2026-02-18T12:09:10+00:00
# Thu, 26 Feb 2026 19:14:24 GMT
ENTRYPOINT ["/usr/local/bin/docker-entrypoint"]
```

-	Layers:
	-	`sha256:01d7766a2e4a62b74e0bebf2cd12c47e675e9221174f6570854203e84ffe68b0`  
		Last Modified: Tue, 10 Feb 2026 17:41:34 GMT  
		Size: 29.7 MB (29727611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff33bca73127d6aefee757e13944f4a8733820fd4272f7e9a65112548f7d3653`  
		Last Modified: Thu, 26 Feb 2026 19:15:03 GMT  
		Size: 53.2 MB (53152586 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04dc2d4692036cca0c24c348a84442e90bee30b5490b69a8b6c746c2e3c4ebb8`  
		Last Modified: Thu, 26 Feb 2026 19:15:00 GMT  
		Size: 1.2 KB (1223 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b46e7b783ad4d3375249ba6bf6218e346a03fb5350a68a056ff75f6a609e9812`  
		Last Modified: Thu, 26 Feb 2026 19:15:11 GMT  
		Size: 451.4 MB (451355145 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82e241109f837eef03c46ea5d45e6a1e6e12e2e9cd0d01551476a0a08cb2e6cc`  
		Last Modified: Thu, 26 Feb 2026 19:15:01 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d80a97704fb72a2d9582cd8be5710c5a0c4a2ff4ca9bf591780c1780fb6b953`  
		Last Modified: Thu, 26 Feb 2026 19:15:02 GMT  
		Size: 1.6 KB (1577 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f16300b068ed0ce2560678adf6b9bb0cf7916f02188e4ba7680d18d863650b4`  
		Last Modified: Thu, 26 Feb 2026 19:15:02 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a3dbe59c3f60fa3b9ae8bad866a8b093b67d3eaaa9b14994a010f303e524610`  
		Last Modified: Thu, 26 Feb 2026 19:15:03 GMT  
		Size: 1.8 KB (1765 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:587e6efd0f049388df98bef878730c2ec809b7e345e40b6663462af0d70876fe`  
		Last Modified: Thu, 26 Feb 2026 19:15:03 GMT  
		Size: 6.3 KB (6295 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b425f6879e23d03e1caa22916b6e8a42bfb4819b17a4ddf63547451f820bc79f`  
		Last Modified: Thu, 26 Feb 2026 19:15:04 GMT  
		Size: 255.2 KB (255183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c5e58dd6e9a6fe902408b97fa1b78370b3a9b2d1e0880e3f59591779867c235`  
		Last Modified: Thu, 26 Feb 2026 19:15:04 GMT  
		Size: 355.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce31ef92721f83e428e05b8b18786925ccdc2fef494fc04dc04ff95f8bef8117`  
		Last Modified: Thu, 26 Feb 2026 19:15:04 GMT  
		Size: 713.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `logstash:8.19.12` - unknown; unknown

```console
$ docker pull logstash@sha256:4869129679cab3eab1f51e2cea9ddce9a0798a5bf9bd871f15dd87bbbefe12e0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3720981 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be3267c1448478bb347045fcc57c9d2b36c66b5d57e990014800c2457c749947`

```dockerfile
```

-	Layers:
	-	`sha256:ad06b8dcd8e3111c11d63e69fc90d1bdbb6c679612f13b12d35f80940c0fd839`  
		Last Modified: Thu, 26 Feb 2026 19:15:01 GMT  
		Size: 3.7 MB (3685136 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:211d10ff07458118212294a424719fcb0c3f84200a1b0767b362306879492e9f`  
		Last Modified: Thu, 26 Feb 2026 19:15:00 GMT  
		Size: 35.8 KB (35845 bytes)  
		MIME: application/vnd.in-toto+json

### `logstash:8.19.12` - linux; arm64 variant v8

```console
$ docker pull logstash@sha256:718f6d3a565a919290083afc9ce4a203f2b671093ecd903121b92d084db587f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **534.6 MB (534644862 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:758d0d34733aeae50f7caa8326670db4bac79c4fd383c9efc75ee7da61f422d1`
-	Entrypoint: `["\/usr\/local\/bin\/docker-entrypoint"]`

```dockerfile
# Mon, 23 Feb 2026 17:19:30 GMT
ARG RELEASE
# Mon, 23 Feb 2026 17:19:30 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 23 Feb 2026 17:19:30 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 23 Feb 2026 17:19:30 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 23 Feb 2026 17:19:32 GMT
ADD file:2763d61bc43bd178306ae0d4151c2477166ebf199b8d7294d9ea410f9891993f in / 
# Mon, 23 Feb 2026 17:19:33 GMT
CMD ["/bin/bash"]
# Tue, 17 Mar 2026 01:41:28 GMT
RUN for iter in {1..10}; do       export DEBIAN_FRONTEND=noninteractive &&     apt-get update -y &&   apt-get upgrade -y &&   apt-get install -y procps findutils tar gzip &&         apt-get install -y locales &&         apt-get install -y curl &&     apt-get clean all &&       locale-gen 'en_US.UTF-8' &&     apt-get clean metadata &&   exit_code=0 && break || exit_code=$? && echo "packaging error: retry $iter in 10s" && apt-get clean all &&   apt-get clean metadata && sleep 10; done; (exit $exit_code) # buildkit
# Tue, 17 Mar 2026 01:41:28 GMT
RUN userdel -r ubuntu && groupadd --gid 1000 logstash &&   useradd --uid 1000 --gid 1000 --home /usr/share/logstash --no-create-home logstash # buildkit
# Tue, 17 Mar 2026 01:42:12 GMT
RUN curl -Lo - https://artifacts.elastic.co/downloads/logstash/logstash-8.19.12-linux-$(arch).tar.gz |   tar zxf - -C /usr/share &&   mv /usr/share/logstash-8.19.12 /usr/share/logstash &&   chown --recursive logstash:logstash /usr/share/logstash/ &&   chown -R logstash:root /usr/share/logstash &&   chmod -R g=u /usr/share/logstash &&   mkdir /licenses/ &&   mv /usr/share/logstash/NOTICE.TXT /licenses/NOTICE.TXT &&   mv /usr/share/logstash/LICENSE.txt /licenses/LICENSE.txt &&   find /usr/share/logstash -type d -exec chmod g+s {} \; &&   ln -s /usr/share/logstash /opt/logstash # buildkit
# Tue, 17 Mar 2026 01:42:12 GMT
WORKDIR /usr/share/logstash
# Tue, 17 Mar 2026 01:42:12 GMT
ENV ELASTIC_CONTAINER=true
# Tue, 17 Mar 2026 01:42:12 GMT
ENV PATH=/usr/share/logstash/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Mar 2026 01:42:12 GMT
COPY config/logstash-full.yml config/logstash.yml # buildkit
# Tue, 17 Mar 2026 01:42:12 GMT
COPY config/pipelines.yml config/log4j2.properties config/log4j2.file.properties config/ # buildkit
# Tue, 17 Mar 2026 01:42:12 GMT
COPY pipeline/default.conf pipeline/logstash.conf # buildkit
# Tue, 17 Mar 2026 01:42:13 GMT
RUN chown --recursive logstash:root config/ pipeline/ # buildkit
# Tue, 17 Mar 2026 01:42:13 GMT
ENV LANG=en_US.UTF-8 LC_ALL=en_US.UTF-8
# Tue, 17 Mar 2026 01:42:13 GMT
COPY --chown=logstash:root env2yaml/classes /usr/share/logstash/env2yaml/classes/ # buildkit
# Tue, 17 Mar 2026 01:42:13 GMT
COPY --chown=logstash:root env2yaml/lib /usr/share/logstash/env2yaml/lib/ # buildkit
# Tue, 17 Mar 2026 01:42:13 GMT
COPY --chmod=0755 env2yaml/env2yaml /usr/local/bin/env2yaml # buildkit
# Tue, 17 Mar 2026 01:42:13 GMT
COPY bin/docker-entrypoint /usr/local/bin/ # buildkit
# Tue, 17 Mar 2026 01:42:13 GMT
RUN chmod 0755 /usr/local/bin/docker-entrypoint # buildkit
# Tue, 17 Mar 2026 01:42:13 GMT
USER 1000
# Tue, 17 Mar 2026 01:42:13 GMT
EXPOSE map[5044/tcp:{} 9600/tcp:{}]
# Tue, 17 Mar 2026 01:42:13 GMT
LABEL org.label-schema.schema-version=1.0 org.label-schema.vendor=Elastic org.opencontainers.image.vendor=Elastic org.label-schema.name=logstash org.opencontainers.image.title=logstash org.label-schema.version=8.19.12 org.opencontainers.image.version=8.19.12 org.label-schema.url=https://www.elastic.co/products/logstash org.label-schema.vcs-url=https://github.com/elastic/logstash org.label-schema.license=Elastic License org.opencontainers.image.licenses=Elastic License org.opencontainers.image.description=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' org.label-schema.build-date=2026-02-18T12:09:10+00:00 org.opencontainers.image.created=2026-02-18T12:09:10+00:00
# Tue, 17 Mar 2026 01:42:13 GMT
ENTRYPOINT ["/usr/local/bin/docker-entrypoint"]
```

-	Layers:
	-	`sha256:86790fc5660dcd86928b849ae0826aba701bf9e005e92c8f9e06c917e82c87f7`  
		Last Modified: Mon, 23 Feb 2026 17:51:24 GMT  
		Size: 28.9 MB (28869709 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bcef9fefb0d6cca8aca5a11dbde776dc5e4864cd483b57cef88be97fdbaa465`  
		Last Modified: Tue, 17 Mar 2026 01:42:54 GMT  
		Size: 55.9 MB (55869270 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff533c5316f169a2886f100f7554e14da07367fb7f95462126f8a73fef63c556`  
		Last Modified: Tue, 17 Mar 2026 01:42:52 GMT  
		Size: 1.2 KB (1223 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2b542e2f5d3aef9108f82344478c21d113e168f1126974193ae973129599543`  
		Last Modified: Tue, 17 Mar 2026 01:43:02 GMT  
		Size: 449.6 MB (449638141 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ae4e8636c21f5da8daf05e9f9bcc004224a9b3733bfea841f4407ae1927d2d3`  
		Last Modified: Tue, 17 Mar 2026 01:42:53 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdf26692cc92e10af8560434b4b6f305cbef99139836bd8a94b3815bb1846bd7`  
		Last Modified: Tue, 17 Mar 2026 01:42:53 GMT  
		Size: 1.6 KB (1580 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d3ad7e274e6caf3f58f785a50a021901d677d500a429e92af75d9c1330b8eec`  
		Last Modified: Tue, 17 Mar 2026 01:42:54 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5f4b6ee1973cb4468eab0975db70b1b5008a19612f8af58d0166f288c3a1fe0`  
		Last Modified: Tue, 17 Mar 2026 01:42:55 GMT  
		Size: 1.8 KB (1767 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3fff66e8b18dcdfc15696b4d01b12583f6dd7953a770daca7fa2aa78195b925`  
		Last Modified: Tue, 17 Mar 2026 01:42:55 GMT  
		Size: 6.3 KB (6298 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:440aeef01434b2e4bad3a8029e7eb096a48c5973e69b32920f2faff4da430110`  
		Last Modified: Tue, 17 Mar 2026 01:42:56 GMT  
		Size: 255.2 KB (255185 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d358081bfa41133602cac3ff540f2cfadaafc05340c3557aa71dd22f4e9a89a`  
		Last Modified: Tue, 17 Mar 2026 01:42:56 GMT  
		Size: 356.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8708b010e66bb985b34c832d3c244e78b553a224ae9591f258437a9f6e67044`  
		Last Modified: Tue, 17 Mar 2026 01:42:56 GMT  
		Size: 713.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `logstash:8.19.12` - unknown; unknown

```console
$ docker pull logstash@sha256:03f2dfe831197c80bd1ef8ab743a0f80f7f5f7679321ea1e2e1aaa9fc2aaf2c3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3721533 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe2ba1d8042ce546920dc9e9be7a66f917e7bdcde47f278e1b78a4e93d3c9146`

```dockerfile
```

-	Layers:
	-	`sha256:955ab5f2120882e1dbb961f4d3bc768f0a04dc0b0d57569d6566ad3f44d9524e`  
		Last Modified: Tue, 17 Mar 2026 01:42:52 GMT  
		Size: 3.7 MB (3685561 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2a9e372e6690be979d1e861bf45348ce2bb222d27b7892bcfe57ea2871d08744`  
		Last Modified: Tue, 17 Mar 2026 01:42:52 GMT  
		Size: 36.0 KB (35972 bytes)  
		MIME: application/vnd.in-toto+json

## `logstash:9.2.6`

```console
$ docker pull logstash@sha256:bc12d9dc4a04e377ae4d44d3a414b1e762730488ce5f7e45e0bfe60ff6dcc666
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `logstash:9.2.6` - linux; amd64

```console
$ docker pull logstash@sha256:0fc5076895f728de5d588efaf3537313156b03f8a8ec08cd7407143fcfbe56d6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **496.1 MB (496080314 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:76df4000ec65586c9b186db277d386a9b27693bcc95a97e5ec5c96801d1bd3d4`
-	Entrypoint: `["\/usr\/local\/bin\/docker-entrypoint"]`

```dockerfile
# Wed, 11 Mar 2026 04:51:30 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 11 Mar 2026 04:51:30 GMT
LABEL vendor="Red Hat, Inc."
# Wed, 11 Mar 2026 04:51:30 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Wed, 11 Mar 2026 04:51:30 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.7"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Wed, 11 Mar 2026 04:51:30 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 11 Mar 2026 04:51:30 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Wed, 11 Mar 2026 04:51:30 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 11 Mar 2026 04:51:30 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 11 Mar 2026 04:51:30 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Wed, 11 Mar 2026 04:51:30 GMT
LABEL io.openshift.expose-services=""
# Wed, 11 Mar 2026 04:51:30 GMT
LABEL io.openshift.tags="minimal rhel9"
# Wed, 11 Mar 2026 04:51:30 GMT
ENV container oci
# Wed, 11 Mar 2026 04:51:31 GMT
COPY dir:c1ba4c335e7831ddebf5732b67e3739a636a3d3dbf6b4d4089ed8f31a1bfbfd1 in /      
# Wed, 11 Mar 2026 04:51:31 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Wed, 11 Mar 2026 04:51:31 GMT
CMD ["/bin/bash"]
# Wed, 11 Mar 2026 04:51:31 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /usr/share/buildinfo/content-sets.json      
# Wed, 11 Mar 2026 04:51:31 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /root/buildinfo/content_manifests/content-sets.json      
# Wed, 11 Mar 2026 04:51:31 GMT
COPY file:53f3c4e4ec21f021024505adc7a7710e18079e2a86f12f898f971cadc64b7478 in /usr/share/buildinfo/labels.json      
# Wed, 11 Mar 2026 04:51:31 GMT
COPY file:53f3c4e4ec21f021024505adc7a7710e18079e2a86f12f898f971cadc64b7478 in /root/buildinfo/labels.json      
# Wed, 11 Mar 2026 04:51:32 GMT
LABEL "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="ddf3e9d218968613397a7b4df7547f25ad755449" "org.opencontainers.image.revision"="ddf3e9d218968613397a7b4df7547f25ad755449" "build-date"="2026-03-11T04:51:18Z" "org.opencontainers.image.created"="2026-03-11T04:51:18Z" "release"="1773204619"org.opencontainers.image.revision=ddf3e9d218968613397a7b4df7547f25ad755449,org.opencontainers.image.created=2026-03-11T04:51:18Z
# Wed, 11 Mar 2026 18:35:12 GMT
ENV ELASTIC_CONTAINER=true
# Wed, 11 Mar 2026 18:35:12 GMT
ENV PATH=/usr/share/logstash/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 11 Mar 2026 18:35:12 GMT
ENV LANG=C.UTF-8 LC_ALL=C.UTF-8
# Wed, 11 Mar 2026 18:35:12 GMT
WORKDIR /usr/share
# Wed, 11 Mar 2026 18:35:14 GMT
RUN microdnf install -y procps findutils tar gzip &&   microdnf install -y openssl &&   microdnf install -y which shadow-utils &&   microdnf clean all # buildkit
# Wed, 11 Mar 2026 18:36:03 GMT
RUN groupadd --gid 1000 logstash &&   adduser --uid 1000 --gid 1000   --home "/usr/share/logstash"   --no-create-home   logstash &&   arch="$(rpm --query --queryformat='%{ARCH}' rpm)" &&   curl --fail --location --output logstash.tar.gz https://artifacts.elastic.co/downloads/logstash/logstash-9.2.6-linux-${arch}.tar.gz &&   tar -zxf logstash.tar.gz -C /usr/share &&   rm logstash.tar.gz &&   mv /usr/share/logstash-9.2.6 /usr/share/logstash &&   chown -R logstash:root /usr/share/logstash &&   chmod -R g=u /usr/share/logstash &&   mkdir /licenses &&   mv /usr/share/logstash/NOTICE.TXT /licenses/NOTICE.TXT &&   mv /usr/share/logstash/LICENSE.txt /licenses/LICENSE.txt &&   find /usr/share/logstash -type d -exec chmod g+s {} \; &&   ln -s /usr/share/logstash /opt/logstash # buildkit
# Wed, 11 Mar 2026 18:36:03 GMT
COPY --chown=logstash:root env2yaml/classes /usr/share/logstash/env2yaml/classes/ # buildkit
# Wed, 11 Mar 2026 18:36:03 GMT
COPY --chown=logstash:root env2yaml/lib /usr/share/logstash/env2yaml/lib/ # buildkit
# Wed, 11 Mar 2026 18:36:03 GMT
COPY --chmod=0755 env2yaml/env2yaml /usr/local/bin/env2yaml # buildkit
# Wed, 11 Mar 2026 18:36:03 GMT
COPY --chown=logstash:root config/pipelines.yml config/log4j2.properties config/log4j2.file.properties /usr/share/logstash/config/ # buildkit
# Wed, 11 Mar 2026 18:36:03 GMT
COPY --chown=logstash:root config/logstash-full.yml /usr/share/logstash/config/logstash.yml # buildkit
# Wed, 11 Mar 2026 18:36:03 GMT
COPY --chown=logstash:root pipeline/default.conf /usr/share/logstash/pipeline/logstash.conf # buildkit
# Wed, 11 Mar 2026 18:36:03 GMT
COPY --chmod=0755 bin/docker-entrypoint /usr/local/bin/ # buildkit
# Wed, 11 Mar 2026 18:36:03 GMT
WORKDIR /usr/share/logstash
# Wed, 11 Mar 2026 18:36:03 GMT
USER 1000
# Wed, 11 Mar 2026 18:36:03 GMT
EXPOSE map[5044/tcp:{} 9600/tcp:{}]
# Wed, 11 Mar 2026 18:36:03 GMT
LABEL org.label-schema.build-date=2026-02-18T12:05:35+00:00 org.label-schema.license=Elastic License org.label-schema.name=logstash org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/logstash org.label-schema.vcs-url=https://github.com/elastic/logstash org.label-schema.vendor=Elastic org.label-schema.version=9.2.6 org.opencontainers.image.created=2026-02-18T12:05:35+00:00 org.opencontainers.image.description=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' org.opencontainers.image.licenses=Elastic License org.opencontainers.image.title=logstash org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=9.2.6 description=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' license=Elastic License maintainer=info@elastic.co name=logstash summary=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' vendor=Elastic
# Wed, 11 Mar 2026 18:36:03 GMT
ENTRYPOINT ["/usr/local/bin/docker-entrypoint"]
```

-	Layers:
	-	`sha256:1174ed37633caad5219e59c67f05fe4e54bd728c7a8cfd4ea1df16de15de2f76`  
		Last Modified: Wed, 11 Mar 2026 06:07:51 GMT  
		Size: 40.0 MB (39990896 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a83cbfe4b6953d9f75b1ff87629686ad7e0e6db5a86e51b4a2fcb34becbd289`  
		Last Modified: Wed, 11 Mar 2026 18:36:36 GMT  
		Size: 5.2 MB (5155619 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:657e125b2fa42df81fc56ea817facda474b7149525059606727b8835bbaa61da`  
		Last Modified: Wed, 11 Mar 2026 18:36:45 GMT  
		Size: 450.7 MB (450669074 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5b1df3f8246ae6e93932125cdb09ad38762f50320ccf616b8d15acbc67e343d`  
		Last Modified: Wed, 11 Mar 2026 18:36:36 GMT  
		Size: 6.3 KB (6293 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d43fe492ea1b7b97b86955c572dcb0f701acfba9ce28e4b4371149e75870c45`  
		Last Modified: Wed, 11 Mar 2026 18:36:36 GMT  
		Size: 255.2 KB (255180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ad55d7064bb6d28cf24941575feafb44be93f5c2bcb120d5f569082d7f39eb2`  
		Last Modified: Wed, 11 Mar 2026 18:36:37 GMT  
		Size: 353.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3d5ee1b88acfa9fa05ade26ef404ea735954f1bfae351bf58eaee0f1446abc3`  
		Last Modified: Wed, 11 Mar 2026 18:36:37 GMT  
		Size: 1.6 KB (1576 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63cb188622ee98c479bd0b5b855c8b540760232363aab12376cc2017dd9e6612`  
		Last Modified: Wed, 11 Mar 2026 18:36:37 GMT  
		Size: 274.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf1b7ac09cce55bae1ce948438dce81f28f6e5b405f6444dd029bf8e0c76fcf0`  
		Last Modified: Wed, 11 Mar 2026 18:36:38 GMT  
		Size: 274.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e6efe85c253bad5b5803b81aeca0e3e0057f6210e5ee83e1a2fa852f11e9432`  
		Last Modified: Wed, 11 Mar 2026 18:36:38 GMT  
		Size: 711.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `logstash:9.2.6` - unknown; unknown

```console
$ docker pull logstash@sha256:bb75581684edf4fca8cc65fa9f0b1170ea416f57c378c4bec147a386f22f1bfa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2163313 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f69865b3a4e901ae08356d29b2fa6eb117187e6f81977ca9c0fc506a4fc39b0`

```dockerfile
```

-	Layers:
	-	`sha256:423e1b431687ff2cf80cbae032628625e7e16f1b582bec8ce307822692d0ae6b`  
		Last Modified: Wed, 11 Mar 2026 18:36:36 GMT  
		Size: 2.1 MB (2133113 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9221440b109b4162ff37cb84fce00d4e7419e257d93af1f1ae4545e3bbde2ab8`  
		Last Modified: Wed, 11 Mar 2026 18:36:36 GMT  
		Size: 30.2 KB (30200 bytes)  
		MIME: application/vnd.in-toto+json

### `logstash:9.2.6` - linux; arm64 variant v8

```console
$ docker pull logstash@sha256:e1581fa3717c4dd764bd4a804df5bfc09b0cf0cec7af99343d789b802882f65a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **492.6 MB (492571146 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ebda8e2da8159e9e95b00f95899c0d3cd1bc8fc54855ed5d681ea838711c7ae`
-	Entrypoint: `["\/usr\/local\/bin\/docker-entrypoint"]`

```dockerfile
# Wed, 11 Mar 2026 04:53:19 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 11 Mar 2026 04:53:19 GMT
LABEL vendor="Red Hat, Inc."
# Wed, 11 Mar 2026 04:53:19 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Wed, 11 Mar 2026 04:53:19 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.7"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Wed, 11 Mar 2026 04:53:19 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 11 Mar 2026 04:53:19 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Wed, 11 Mar 2026 04:53:19 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 11 Mar 2026 04:53:19 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 11 Mar 2026 04:53:19 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Wed, 11 Mar 2026 04:53:19 GMT
LABEL io.openshift.expose-services=""
# Wed, 11 Mar 2026 04:53:19 GMT
LABEL io.openshift.tags="minimal rhel9"
# Wed, 11 Mar 2026 04:53:19 GMT
ENV container oci
# Wed, 11 Mar 2026 04:53:20 GMT
COPY dir:7796b64b73526e8dad6fca20071cfe57334a57323fbbb1f9256c4ffffa8b27db in /      
# Wed, 11 Mar 2026 04:53:20 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Wed, 11 Mar 2026 04:53:20 GMT
CMD ["/bin/bash"]
# Wed, 11 Mar 2026 04:53:20 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /usr/share/buildinfo/content-sets.json      
# Wed, 11 Mar 2026 04:53:21 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /root/buildinfo/content_manifests/content-sets.json      
# Wed, 11 Mar 2026 04:53:21 GMT
COPY file:186c4202737062dc84f1db98b633710a412a23c003ba73ff6ae51d727aea1cd8 in /usr/share/buildinfo/labels.json      
# Wed, 11 Mar 2026 04:53:21 GMT
COPY file:186c4202737062dc84f1db98b633710a412a23c003ba73ff6ae51d727aea1cd8 in /root/buildinfo/labels.json      
# Wed, 11 Mar 2026 04:53:21 GMT
LABEL "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="ddf3e9d218968613397a7b4df7547f25ad755449" "org.opencontainers.image.revision"="ddf3e9d218968613397a7b4df7547f25ad755449" "build-date"="2026-03-11T04:53:07Z" "org.opencontainers.image.created"="2026-03-11T04:53:07Z" "release"="1773204619"org.opencontainers.image.revision=ddf3e9d218968613397a7b4df7547f25ad755449,org.opencontainers.image.created=2026-03-11T04:53:07Z
# Wed, 11 Mar 2026 18:35:36 GMT
ENV ELASTIC_CONTAINER=true
# Wed, 11 Mar 2026 18:35:36 GMT
ENV PATH=/usr/share/logstash/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 11 Mar 2026 18:35:36 GMT
ENV LANG=C.UTF-8 LC_ALL=C.UTF-8
# Wed, 11 Mar 2026 18:35:36 GMT
WORKDIR /usr/share
# Wed, 11 Mar 2026 18:35:38 GMT
RUN microdnf install -y procps findutils tar gzip &&   microdnf install -y openssl &&   microdnf install -y which shadow-utils &&   microdnf clean all # buildkit
# Wed, 11 Mar 2026 18:36:29 GMT
RUN groupadd --gid 1000 logstash &&   adduser --uid 1000 --gid 1000   --home "/usr/share/logstash"   --no-create-home   logstash &&   arch="$(rpm --query --queryformat='%{ARCH}' rpm)" &&   curl --fail --location --output logstash.tar.gz https://artifacts.elastic.co/downloads/logstash/logstash-9.2.6-linux-${arch}.tar.gz &&   tar -zxf logstash.tar.gz -C /usr/share &&   rm logstash.tar.gz &&   mv /usr/share/logstash-9.2.6 /usr/share/logstash &&   chown -R logstash:root /usr/share/logstash &&   chmod -R g=u /usr/share/logstash &&   mkdir /licenses &&   mv /usr/share/logstash/NOTICE.TXT /licenses/NOTICE.TXT &&   mv /usr/share/logstash/LICENSE.txt /licenses/LICENSE.txt &&   find /usr/share/logstash -type d -exec chmod g+s {} \; &&   ln -s /usr/share/logstash /opt/logstash # buildkit
# Wed, 11 Mar 2026 18:36:29 GMT
COPY --chown=logstash:root env2yaml/classes /usr/share/logstash/env2yaml/classes/ # buildkit
# Wed, 11 Mar 2026 18:36:29 GMT
COPY --chown=logstash:root env2yaml/lib /usr/share/logstash/env2yaml/lib/ # buildkit
# Wed, 11 Mar 2026 18:36:29 GMT
COPY --chmod=0755 env2yaml/env2yaml /usr/local/bin/env2yaml # buildkit
# Wed, 11 Mar 2026 18:36:30 GMT
COPY --chown=logstash:root config/pipelines.yml config/log4j2.properties config/log4j2.file.properties /usr/share/logstash/config/ # buildkit
# Wed, 11 Mar 2026 18:36:30 GMT
COPY --chown=logstash:root config/logstash-full.yml /usr/share/logstash/config/logstash.yml # buildkit
# Wed, 11 Mar 2026 18:36:30 GMT
COPY --chown=logstash:root pipeline/default.conf /usr/share/logstash/pipeline/logstash.conf # buildkit
# Wed, 11 Mar 2026 18:36:30 GMT
COPY --chmod=0755 bin/docker-entrypoint /usr/local/bin/ # buildkit
# Wed, 11 Mar 2026 18:36:30 GMT
WORKDIR /usr/share/logstash
# Wed, 11 Mar 2026 18:36:30 GMT
USER 1000
# Wed, 11 Mar 2026 18:36:30 GMT
EXPOSE map[5044/tcp:{} 9600/tcp:{}]
# Wed, 11 Mar 2026 18:36:30 GMT
LABEL org.label-schema.build-date=2026-02-18T12:05:35+00:00 org.label-schema.license=Elastic License org.label-schema.name=logstash org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/logstash org.label-schema.vcs-url=https://github.com/elastic/logstash org.label-schema.vendor=Elastic org.label-schema.version=9.2.6 org.opencontainers.image.created=2026-02-18T12:05:35+00:00 org.opencontainers.image.description=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' org.opencontainers.image.licenses=Elastic License org.opencontainers.image.title=logstash org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=9.2.6 description=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' license=Elastic License maintainer=info@elastic.co name=logstash summary=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' vendor=Elastic
# Wed, 11 Mar 2026 18:36:30 GMT
ENTRYPOINT ["/usr/local/bin/docker-entrypoint"]
```

-	Layers:
	-	`sha256:a929c158045efa38dcdfac5809dfda6e7c13c225e0aae109412941b4ed8f3880`  
		Last Modified: Wed, 11 Mar 2026 06:07:49 GMT  
		Size: 38.2 MB (38205467 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2e2f87e99ad19503094ba0ffc06ae26c46ee04bcd8588bdd363546fb9565394`  
		Last Modified: Wed, 11 Mar 2026 18:37:08 GMT  
		Size: 5.2 MB (5154669 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aee275e8416e85403452f4613361f839710e311c29fc2e005f75a7f4df8ea476`  
		Last Modified: Wed, 11 Mar 2026 18:37:16 GMT  
		Size: 448.9 MB (448946271 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb8c3d8335827d850c71d754d83463c298d673f8122667ed7ca6ec275cf77a6c`  
		Last Modified: Wed, 11 Mar 2026 18:37:07 GMT  
		Size: 6.3 KB (6294 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:517d8009a2c5b2d2ec80dd20871a79c5c728291b2e45733ecb738f908e496135`  
		Last Modified: Wed, 11 Mar 2026 18:37:07 GMT  
		Size: 255.2 KB (255181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59c2f2136f2ebc564b81289d6b040ad19c893f6a9705841f379128f243b55814`  
		Last Modified: Wed, 11 Mar 2026 18:37:09 GMT  
		Size: 353.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:778e3c739177c127fd1b6e68611b58d22a3c91b1626d4f77c58b86ed0e5a2fb7`  
		Last Modified: Wed, 11 Mar 2026 18:37:09 GMT  
		Size: 1.6 KB (1580 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75276d4321375e01b7099a7b90c1fc542b46f1eb1832250fff2132692706e3b9`  
		Last Modified: Wed, 11 Mar 2026 18:37:09 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:036d3ab1af938d6c4a5dbcf98300296257ab8701e229b750931d01eaa56ffa26`  
		Last Modified: Wed, 11 Mar 2026 18:37:10 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db52c22b3a36714df0f11554a52e00d74510c667a6ed8ad31f3d2c1169021689`  
		Last Modified: Wed, 11 Mar 2026 18:37:10 GMT  
		Size: 711.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `logstash:9.2.6` - unknown; unknown

```console
$ docker pull logstash@sha256:0593951a17ca9b09a103706a44249870ec18afa9fc77f99575e52c7cc237db05
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2163960 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a6ee4e794be8534e3b7bb76e5ceb55aca6a0acc524915a591474715ccb3fb46`

```dockerfile
```

-	Layers:
	-	`sha256:b3c6353ba7f5f4566acfe777df41970fcb73834e39e914be62835a1f3de04f32`  
		Last Modified: Wed, 11 Mar 2026 18:37:08 GMT  
		Size: 2.1 MB (2133683 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:59113e3bb04e40efab71fb61b6cc10f3581b0a9cdf6661dc39536ff3b5bccde3`  
		Last Modified: Wed, 11 Mar 2026 18:37:07 GMT  
		Size: 30.3 KB (30277 bytes)  
		MIME: application/vnd.in-toto+json

## `logstash:9.3.1`

```console
$ docker pull logstash@sha256:f9c32e6e9fdd1ba6dc1cac5a77628cc8c3598692ef2bc91df70f92e3974a21f7
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `logstash:9.3.1` - linux; amd64

```console
$ docker pull logstash@sha256:f79afbfe71dd5472ba2c190eee1603a46d3ae90e802311bd5f1692d655a3520d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **511.5 MB (511499631 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:711d867bfe45ad899cbcba558ed9054c70339ca9ab6d9c5c502a15edb077b715`
-	Entrypoint: `["\/usr\/local\/bin\/docker-entrypoint"]`

```dockerfile
# Wed, 11 Mar 2026 04:51:30 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 11 Mar 2026 04:51:30 GMT
LABEL vendor="Red Hat, Inc."
# Wed, 11 Mar 2026 04:51:30 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Wed, 11 Mar 2026 04:51:30 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.7"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Wed, 11 Mar 2026 04:51:30 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 11 Mar 2026 04:51:30 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Wed, 11 Mar 2026 04:51:30 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 11 Mar 2026 04:51:30 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 11 Mar 2026 04:51:30 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Wed, 11 Mar 2026 04:51:30 GMT
LABEL io.openshift.expose-services=""
# Wed, 11 Mar 2026 04:51:30 GMT
LABEL io.openshift.tags="minimal rhel9"
# Wed, 11 Mar 2026 04:51:30 GMT
ENV container oci
# Wed, 11 Mar 2026 04:51:31 GMT
COPY dir:c1ba4c335e7831ddebf5732b67e3739a636a3d3dbf6b4d4089ed8f31a1bfbfd1 in /      
# Wed, 11 Mar 2026 04:51:31 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Wed, 11 Mar 2026 04:51:31 GMT
CMD ["/bin/bash"]
# Wed, 11 Mar 2026 04:51:31 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /usr/share/buildinfo/content-sets.json      
# Wed, 11 Mar 2026 04:51:31 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /root/buildinfo/content_manifests/content-sets.json      
# Wed, 11 Mar 2026 04:51:31 GMT
COPY file:53f3c4e4ec21f021024505adc7a7710e18079e2a86f12f898f971cadc64b7478 in /usr/share/buildinfo/labels.json      
# Wed, 11 Mar 2026 04:51:31 GMT
COPY file:53f3c4e4ec21f021024505adc7a7710e18079e2a86f12f898f971cadc64b7478 in /root/buildinfo/labels.json      
# Wed, 11 Mar 2026 04:51:32 GMT
LABEL "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="ddf3e9d218968613397a7b4df7547f25ad755449" "org.opencontainers.image.revision"="ddf3e9d218968613397a7b4df7547f25ad755449" "build-date"="2026-03-11T04:51:18Z" "org.opencontainers.image.created"="2026-03-11T04:51:18Z" "release"="1773204619"org.opencontainers.image.revision=ddf3e9d218968613397a7b4df7547f25ad755449,org.opencontainers.image.created=2026-03-11T04:51:18Z
# Wed, 11 Mar 2026 18:35:16 GMT
ENV ELASTIC_CONTAINER=true
# Wed, 11 Mar 2026 18:35:16 GMT
ENV PATH=/usr/share/logstash/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 11 Mar 2026 18:35:16 GMT
ENV LANG=C.UTF-8 LC_ALL=C.UTF-8
# Wed, 11 Mar 2026 18:35:16 GMT
WORKDIR /usr/share
# Wed, 11 Mar 2026 18:35:18 GMT
RUN microdnf install -y procps findutils tar gzip &&   microdnf install -y openssl &&   microdnf install -y which shadow-utils &&   microdnf clean all # buildkit
# Wed, 11 Mar 2026 18:36:00 GMT
RUN groupadd --gid 1000 logstash &&   adduser --uid 1000 --gid 1000   --home "/usr/share/logstash"   --no-create-home   logstash &&   arch="$(rpm --query --queryformat='%{ARCH}' rpm)" &&   curl --fail --location --output logstash.tar.gz https://artifacts.elastic.co/downloads/logstash/logstash-9.3.1-linux-${arch}.tar.gz &&   tar -zxf logstash.tar.gz -C /usr/share &&   rm logstash.tar.gz &&   mv /usr/share/logstash-9.3.1 /usr/share/logstash &&   chown -R logstash:root /usr/share/logstash &&   chmod -R g=u /usr/share/logstash &&   mkdir /licenses &&   mv /usr/share/logstash/NOTICE.TXT /licenses/NOTICE.TXT &&   mv /usr/share/logstash/LICENSE.txt /licenses/LICENSE.txt &&   find /usr/share/logstash -type d -exec chmod g+s {} \; &&   ln -s /usr/share/logstash /opt/logstash # buildkit
# Wed, 11 Mar 2026 18:36:00 GMT
COPY --chown=logstash:root env2yaml/classes /usr/share/logstash/env2yaml/classes/ # buildkit
# Wed, 11 Mar 2026 18:36:00 GMT
COPY --chown=logstash:root env2yaml/lib /usr/share/logstash/env2yaml/lib/ # buildkit
# Wed, 11 Mar 2026 18:36:00 GMT
COPY --chmod=0755 env2yaml/env2yaml /usr/local/bin/env2yaml # buildkit
# Wed, 11 Mar 2026 18:36:00 GMT
COPY --chown=logstash:root config/pipelines.yml config/log4j2.properties config/log4j2.file.properties /usr/share/logstash/config/ # buildkit
# Wed, 11 Mar 2026 18:36:00 GMT
COPY --chown=logstash:root config/logstash-full.yml /usr/share/logstash/config/logstash.yml # buildkit
# Wed, 11 Mar 2026 18:36:00 GMT
COPY --chown=logstash:root pipeline/default.conf /usr/share/logstash/pipeline/logstash.conf # buildkit
# Wed, 11 Mar 2026 18:36:01 GMT
COPY --chmod=0755 bin/docker-entrypoint /usr/local/bin/ # buildkit
# Wed, 11 Mar 2026 18:36:01 GMT
WORKDIR /usr/share/logstash
# Wed, 11 Mar 2026 18:36:01 GMT
USER 1000
# Wed, 11 Mar 2026 18:36:01 GMT
EXPOSE map[5044/tcp:{} 9600/tcp:{}]
# Wed, 11 Mar 2026 18:36:01 GMT
LABEL org.label-schema.build-date=2026-02-18T12:06:22+00:00 org.label-schema.license=Elastic License org.label-schema.name=logstash org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/logstash org.label-schema.vcs-url=https://github.com/elastic/logstash org.label-schema.vendor=Elastic org.label-schema.version=9.3.1 org.opencontainers.image.created=2026-02-18T12:06:22+00:00 org.opencontainers.image.description=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' org.opencontainers.image.licenses=Elastic License org.opencontainers.image.title=logstash org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=9.3.1 description=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' license=Elastic License maintainer=info@elastic.co name=logstash summary=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' vendor=Elastic
# Wed, 11 Mar 2026 18:36:01 GMT
ENTRYPOINT ["/usr/local/bin/docker-entrypoint"]
```

-	Layers:
	-	`sha256:1174ed37633caad5219e59c67f05fe4e54bd728c7a8cfd4ea1df16de15de2f76`  
		Last Modified: Wed, 11 Mar 2026 06:07:51 GMT  
		Size: 40.0 MB (39990896 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:165eceb1e8404a8074738d46191b42bfd17513189e8a7a2d56b821d120574e6a`  
		Last Modified: Wed, 11 Mar 2026 18:36:35 GMT  
		Size: 5.2 MB (5155623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0efdbed88a04ffbed3ee7267ff10332c442611cb6b3e3f1efa450b5b1a149dd`  
		Last Modified: Wed, 11 Mar 2026 18:36:43 GMT  
		Size: 466.1 MB (466088376 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ebd399f2a8bafd824bd8dabd07300e3f949f476bfc548fa4c1ef1e9ef95446d`  
		Last Modified: Wed, 11 Mar 2026 18:36:35 GMT  
		Size: 6.3 KB (6298 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:939bb754a26781b6a7d648a922fb641c4d0feb6823f5ffd311fdfc7a5e368aee`  
		Last Modified: Wed, 11 Mar 2026 18:36:35 GMT  
		Size: 255.2 KB (255185 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6501aa13d3f797e45a607ba805bf01de7b9c00bea87d348b02c4e5c08c872b12`  
		Last Modified: Wed, 11 Mar 2026 18:36:36 GMT  
		Size: 352.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:045d765f5f49527c8e4a0335bd2f8b75b3cdb3da0fcd96854c61c219704c6225`  
		Last Modified: Wed, 11 Mar 2026 18:36:36 GMT  
		Size: 1.6 KB (1575 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99e8ffbe8221312024556837e3e1f529707a33e7dd208a9d94402935709a94f8`  
		Last Modified: Wed, 11 Mar 2026 18:36:36 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:135d58ee53f20a6257892d334cb4a280d7bac0c49b0c4baf10d8c81d702642b2`  
		Last Modified: Wed, 11 Mar 2026 18:36:37 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41b67ad85415155717b020f8a16a1a747d8560be47c7eff34762c195f8494f75`  
		Last Modified: Wed, 11 Mar 2026 18:36:37 GMT  
		Size: 711.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `logstash:9.3.1` - unknown; unknown

```console
$ docker pull logstash@sha256:ea00b6b783c5d5e5b45e1f93a695caf3543ac2eb52425eadf08e1c6f5ab6d094
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2142272 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f9a75898e22d97b80fe10117aef3267792c36c961d2d4058f9fe2ef69066c1c1`

```dockerfile
```

-	Layers:
	-	`sha256:59bcd0a2c6235a29acfdba606490db4a9e6cb0c77eed60ce190eeaf6b88b78d4`  
		Last Modified: Wed, 11 Mar 2026 18:36:35 GMT  
		Size: 2.1 MB (2112072 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:84779cba163e779ef7419b7b51d755d43067d9c2f686be4789a1f0a70cb685bd`  
		Last Modified: Wed, 11 Mar 2026 18:36:35 GMT  
		Size: 30.2 KB (30200 bytes)  
		MIME: application/vnd.in-toto+json

### `logstash:9.3.1` - linux; arm64 variant v8

```console
$ docker pull logstash@sha256:7b63954a588d184a5aa256cc8a5ad695ba007d76e24612e6e5ad474c510e2649
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **508.0 MB (507987372 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d3a89554cfdcefa6628cacdb047babc99897c8102c1654fc5a188cacede77f31`
-	Entrypoint: `["\/usr\/local\/bin\/docker-entrypoint"]`

```dockerfile
# Wed, 11 Mar 2026 04:53:19 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 11 Mar 2026 04:53:19 GMT
LABEL vendor="Red Hat, Inc."
# Wed, 11 Mar 2026 04:53:19 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Wed, 11 Mar 2026 04:53:19 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.7"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Wed, 11 Mar 2026 04:53:19 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 11 Mar 2026 04:53:19 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Wed, 11 Mar 2026 04:53:19 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 11 Mar 2026 04:53:19 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 11 Mar 2026 04:53:19 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Wed, 11 Mar 2026 04:53:19 GMT
LABEL io.openshift.expose-services=""
# Wed, 11 Mar 2026 04:53:19 GMT
LABEL io.openshift.tags="minimal rhel9"
# Wed, 11 Mar 2026 04:53:19 GMT
ENV container oci
# Wed, 11 Mar 2026 04:53:20 GMT
COPY dir:7796b64b73526e8dad6fca20071cfe57334a57323fbbb1f9256c4ffffa8b27db in /      
# Wed, 11 Mar 2026 04:53:20 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Wed, 11 Mar 2026 04:53:20 GMT
CMD ["/bin/bash"]
# Wed, 11 Mar 2026 04:53:20 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /usr/share/buildinfo/content-sets.json      
# Wed, 11 Mar 2026 04:53:21 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /root/buildinfo/content_manifests/content-sets.json      
# Wed, 11 Mar 2026 04:53:21 GMT
COPY file:186c4202737062dc84f1db98b633710a412a23c003ba73ff6ae51d727aea1cd8 in /usr/share/buildinfo/labels.json      
# Wed, 11 Mar 2026 04:53:21 GMT
COPY file:186c4202737062dc84f1db98b633710a412a23c003ba73ff6ae51d727aea1cd8 in /root/buildinfo/labels.json      
# Wed, 11 Mar 2026 04:53:21 GMT
LABEL "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="ddf3e9d218968613397a7b4df7547f25ad755449" "org.opencontainers.image.revision"="ddf3e9d218968613397a7b4df7547f25ad755449" "build-date"="2026-03-11T04:53:07Z" "org.opencontainers.image.created"="2026-03-11T04:53:07Z" "release"="1773204619"org.opencontainers.image.revision=ddf3e9d218968613397a7b4df7547f25ad755449,org.opencontainers.image.created=2026-03-11T04:53:07Z
# Wed, 11 Mar 2026 18:36:17 GMT
ENV ELASTIC_CONTAINER=true
# Wed, 11 Mar 2026 18:36:17 GMT
ENV PATH=/usr/share/logstash/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 11 Mar 2026 18:36:17 GMT
ENV LANG=C.UTF-8 LC_ALL=C.UTF-8
# Wed, 11 Mar 2026 18:36:17 GMT
WORKDIR /usr/share
# Wed, 11 Mar 2026 18:36:19 GMT
RUN microdnf install -y procps findutils tar gzip &&   microdnf install -y openssl &&   microdnf install -y which shadow-utils &&   microdnf clean all # buildkit
# Wed, 11 Mar 2026 18:37:10 GMT
RUN groupadd --gid 1000 logstash &&   adduser --uid 1000 --gid 1000   --home "/usr/share/logstash"   --no-create-home   logstash &&   arch="$(rpm --query --queryformat='%{ARCH}' rpm)" &&   curl --fail --location --output logstash.tar.gz https://artifacts.elastic.co/downloads/logstash/logstash-9.3.1-linux-${arch}.tar.gz &&   tar -zxf logstash.tar.gz -C /usr/share &&   rm logstash.tar.gz &&   mv /usr/share/logstash-9.3.1 /usr/share/logstash &&   chown -R logstash:root /usr/share/logstash &&   chmod -R g=u /usr/share/logstash &&   mkdir /licenses &&   mv /usr/share/logstash/NOTICE.TXT /licenses/NOTICE.TXT &&   mv /usr/share/logstash/LICENSE.txt /licenses/LICENSE.txt &&   find /usr/share/logstash -type d -exec chmod g+s {} \; &&   ln -s /usr/share/logstash /opt/logstash # buildkit
# Wed, 11 Mar 2026 18:37:10 GMT
COPY --chown=logstash:root env2yaml/classes /usr/share/logstash/env2yaml/classes/ # buildkit
# Wed, 11 Mar 2026 18:37:10 GMT
COPY --chown=logstash:root env2yaml/lib /usr/share/logstash/env2yaml/lib/ # buildkit
# Wed, 11 Mar 2026 18:37:10 GMT
COPY --chmod=0755 env2yaml/env2yaml /usr/local/bin/env2yaml # buildkit
# Wed, 11 Mar 2026 18:37:10 GMT
COPY --chown=logstash:root config/pipelines.yml config/log4j2.properties config/log4j2.file.properties /usr/share/logstash/config/ # buildkit
# Wed, 11 Mar 2026 18:37:10 GMT
COPY --chown=logstash:root config/logstash-full.yml /usr/share/logstash/config/logstash.yml # buildkit
# Wed, 11 Mar 2026 18:37:10 GMT
COPY --chown=logstash:root pipeline/default.conf /usr/share/logstash/pipeline/logstash.conf # buildkit
# Wed, 11 Mar 2026 18:37:10 GMT
COPY --chmod=0755 bin/docker-entrypoint /usr/local/bin/ # buildkit
# Wed, 11 Mar 2026 18:37:10 GMT
WORKDIR /usr/share/logstash
# Wed, 11 Mar 2026 18:37:10 GMT
USER 1000
# Wed, 11 Mar 2026 18:37:10 GMT
EXPOSE map[5044/tcp:{} 9600/tcp:{}]
# Wed, 11 Mar 2026 18:37:10 GMT
LABEL org.label-schema.build-date=2026-02-18T12:06:22+00:00 org.label-schema.license=Elastic License org.label-schema.name=logstash org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/logstash org.label-schema.vcs-url=https://github.com/elastic/logstash org.label-schema.vendor=Elastic org.label-schema.version=9.3.1 org.opencontainers.image.created=2026-02-18T12:06:22+00:00 org.opencontainers.image.description=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' org.opencontainers.image.licenses=Elastic License org.opencontainers.image.title=logstash org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=9.3.1 description=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' license=Elastic License maintainer=info@elastic.co name=logstash summary=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' vendor=Elastic
# Wed, 11 Mar 2026 18:37:10 GMT
ENTRYPOINT ["/usr/local/bin/docker-entrypoint"]
```

-	Layers:
	-	`sha256:a929c158045efa38dcdfac5809dfda6e7c13c225e0aae109412941b4ed8f3880`  
		Last Modified: Wed, 11 Mar 2026 06:07:49 GMT  
		Size: 38.2 MB (38205467 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0c0680baa1724eecf49ccbd61ae0cea4442069b5f1d2d7743a61925d7e34dd2`  
		Last Modified: Wed, 11 Mar 2026 18:37:47 GMT  
		Size: 5.2 MB (5154662 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3fe926fb31f9b574b20780e4406376bca426e5673bb42ce724a7157d4a631428`  
		Last Modified: Wed, 11 Mar 2026 18:37:57 GMT  
		Size: 464.4 MB (464362509 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6d46559bc3f830fcb49e5f332cb0318749fb3bf20fdd27f1d626d5ab31921fa`  
		Last Modified: Wed, 11 Mar 2026 18:37:47 GMT  
		Size: 6.3 KB (6294 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b28930fa0aa4b380d30b1c4116225d4c819042167c7fd7834843a2528c6d571`  
		Last Modified: Wed, 11 Mar 2026 18:37:47 GMT  
		Size: 255.2 KB (255183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c847ff2e41576d118ac71f704ab4b509eac9781f36912e0c924c647ddebe0cd4`  
		Last Modified: Wed, 11 Mar 2026 18:37:48 GMT  
		Size: 354.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbe025ed7fdc32c8ba7b763fbc120688e06e3334dc01713d8e06428bf53419dd`  
		Last Modified: Wed, 11 Mar 2026 18:37:48 GMT  
		Size: 1.6 KB (1575 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e0e2c5499fdb4cc38bd18c88566912cceb1f6c5c63449f48ad4f489bc9ffed5`  
		Last Modified: Wed, 11 Mar 2026 18:37:49 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30717a8449a9373a64f5eb3a1d0d718930e3d6b87c01aa95811bda7cec16b845`  
		Last Modified: Wed, 11 Mar 2026 18:37:50 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ae49c9db3e44cf366c6a0d6250f07eef9f83ffe2a1ff3e32927777067bcf555`  
		Last Modified: Wed, 11 Mar 2026 18:37:50 GMT  
		Size: 710.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `logstash:9.3.1` - unknown; unknown

```console
$ docker pull logstash@sha256:d27fd05d9f61c91bd82fa1ca23c1597d8ce6b6a29597823be23eaed3dc7f943e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2142919 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ac5fbda13e8f94c58aa61d2e137885bc787ff554ee3875249dd18b8a6b8a5f1`

```dockerfile
```

-	Layers:
	-	`sha256:11200b1f16eefb5c3940ddacccd605332dfd40564b00e0fc6875fac2454cf3bd`  
		Last Modified: Wed, 11 Mar 2026 18:37:47 GMT  
		Size: 2.1 MB (2112642 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b784e4f94027e5b85d97646b8a349658e09e20b8215d9728536bb6a7e11496ed`  
		Last Modified: Wed, 11 Mar 2026 18:37:47 GMT  
		Size: 30.3 KB (30277 bytes)  
		MIME: application/vnd.in-toto+json
