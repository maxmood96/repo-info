<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `logstash`

-	[`logstash:7.17.26`](#logstash71726)
-	[`logstash:8.15.5`](#logstash8155)
-	[`logstash:8.16.1`](#logstash8161)

## `logstash:7.17.26`

```console
$ docker pull logstash@sha256:b9f2f6013fc6b6c1cf95d3915264c7721681346629bf8b910d92b3d30cc56fe3
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `logstash:7.17.26` - linux; amd64

```console
$ docker pull logstash@sha256:3f0fd65748174a8cbcb12187c9e9f641084ac986715f10108464fdc6aec77f6a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **451.0 MB (450986081 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f8008a134f95a22df5d39d7d595cdb214fdf14d250c520ed3dc5dd826f97c23c`
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
# Tue, 03 Dec 2024 13:02:17 GMT
RUN for iter in {1..10}; do     export DEBIAN_FRONTEND=noninteractive &&     apt-get update -y &&     apt-get upgrade -y &&     apt-get install -y procps findutils tar gzip curl &&     apt-get install -y locales &&     apt-get clean all &&     locale-gen 'en_US.UTF-8' &&     apt-get clean metadata &&     exit_code=0 && break || exit_code=$? &&     echo "packaging error: retry $iter in 10s" &&     apt-get clean all &&     apt-get clean metadata &&     sleep 10; done;     (exit $exit_code) # buildkit
# Tue, 03 Dec 2024 13:02:17 GMT
RUN groupadd --gid 1000 logstash &&     adduser --uid 1000 --gid 1000     --home /usr/share/logstash --no-create-home     logstash # buildkit
# Tue, 03 Dec 2024 13:02:17 GMT
RUN curl -Lo - https://artifacts.elastic.co/downloads/logstash/logstash-7.17.26-linux-$(arch).tar.gz |     tar zxf - -C /usr/share &&     mv /usr/share/logstash-7.17.26 /usr/share/logstash &&     chown --recursive logstash:logstash /usr/share/logstash/ &&     chown -R logstash:root /usr/share/logstash &&     chmod -R g=u /usr/share/logstash &&     mkdir /licenses/ &&     mv /usr/share/logstash/NOTICE.TXT /licenses/NOTICE.TXT &&     mv /usr/share/logstash/LICENSE.txt /licenses/LICENSE.txt &&     find /usr/share/logstash -type d -exec chmod g+s {} \; &&     ln -s /usr/share/logstash /opt/logstash # buildkit
# Tue, 03 Dec 2024 13:02:17 GMT
WORKDIR /usr/share/logstash
# Tue, 03 Dec 2024 13:02:17 GMT
ENV ELASTIC_CONTAINER=true
# Tue, 03 Dec 2024 13:02:17 GMT
ENV PATH=/usr/share/logstash/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Dec 2024 13:02:17 GMT
COPY config/pipelines.yml config/pipelines.yml # buildkit
# Tue, 03 Dec 2024 13:02:17 GMT
COPY config/logstash-full.yml config/logstash.yml # buildkit
# Tue, 03 Dec 2024 13:02:17 GMT
COPY config/log4j2.properties config/ # buildkit
# Tue, 03 Dec 2024 13:02:17 GMT
COPY pipeline/default.conf pipeline/logstash.conf # buildkit
# Tue, 03 Dec 2024 13:02:17 GMT
RUN chown --recursive logstash:root config/ pipeline/ # buildkit
# Tue, 03 Dec 2024 13:02:17 GMT
ENV LANG=en_US.UTF-8 LC_ALL=en_US.UTF-8
# Tue, 03 Dec 2024 13:02:17 GMT
COPY env2yaml/env2yaml /usr/local/bin/ # buildkit
# Tue, 03 Dec 2024 13:02:17 GMT
COPY bin/docker-entrypoint /usr/local/bin/ # buildkit
# Tue, 03 Dec 2024 13:02:17 GMT
RUN chmod 0755 /usr/local/bin/docker-entrypoint # buildkit
# Tue, 03 Dec 2024 13:02:17 GMT
USER 1000
# Tue, 03 Dec 2024 13:02:17 GMT
EXPOSE map[5044/tcp:{} 9600/tcp:{}]
# Tue, 03 Dec 2024 13:02:17 GMT
LABEL org.label-schema.schema-version=1.0 org.label-schema.vendor=Elastic org.opencontainers.image.vendor=Elastic org.label-schema.name=logstash org.opencontainers.image.title=logstash org.label-schema.version=7.17.26 org.opencontainers.image.version=7.17.26 org.label-schema.url=https://www.elastic.co/products/logstash org.label-schema.vcs-url=https://github.com/elastic/logstash org.label-schema.license=Elastic License org.opencontainers.image.licenses=Elastic License org.opencontainers.image.description=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' org.label-schema.build-date=2024-10-22T09:18:02+00:00 org.opencontainers.image.created=2024-10-22T09:18:02+00:00
# Tue, 03 Dec 2024 13:02:17 GMT
ENTRYPOINT ["/usr/local/bin/docker-entrypoint"]
```

-	Layers:
	-	`sha256:d9802f032d6798e2086607424bfe88cb8ec1d6f116e11cd99592dcaf261e9cd2`  
		Last Modified: Fri, 11 Oct 2024 04:41:25 GMT  
		Size: 27.5 MB (27511060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2db6aeeb96fc01883119363b6cca3fdb39b89036d6a317b6ad5ec4c7f4c975e7`  
		Last Modified: Tue, 03 Dec 2024 19:30:30 GMT  
		Size: 50.4 MB (50409358 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67fb4172d9a8cf1cfbd5e468d9deb80f9931e7d3e7d33934cc46560b6b219375`  
		Last Modified: Tue, 03 Dec 2024 19:30:30 GMT  
		Size: 1.8 KB (1807 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff54592f3770c76c69d4a526c8a7d286a136ae29dc91da5c223b98f8b82f4d5b`  
		Last Modified: Tue, 03 Dec 2024 19:30:36 GMT  
		Size: 371.0 MB (370999252 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1d9318cb0250cd0fac086ce89a6d4a37c10e0d22b8a668dd1cedb3e5ab5c1a1`  
		Last Modified: Tue, 03 Dec 2024 19:30:30 GMT  
		Size: 381.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7eb889b5053bdb66d1765a64d9137d17d41735d18ec1ba53e5703eb0fa852d7`  
		Last Modified: Tue, 03 Dec 2024 19:30:30 GMT  
		Size: 278.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a465e4eb4962dfb93a40fab2da0b2449f27877a4918a2bf84501672e80c4a0b`  
		Last Modified: Tue, 03 Dec 2024 19:30:30 GMT  
		Size: 474.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98e78fd8fe26c9d1736d1e19c3e3f6e6876a5457dbdb49b6563af726e9ed4537`  
		Last Modified: Tue, 03 Dec 2024 19:30:31 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f66875b69814f164e0d7ea594119f1e78335f2b4e294d941e66fb6cda2d133a`  
		Last Modified: Tue, 03 Dec 2024 19:30:31 GMT  
		Size: 826.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84e86ef604def7ff65dc33e6178ef64e0647bc1ccaa2ceff2ff7d282a01e19c6`  
		Last Modified: Tue, 03 Dec 2024 19:30:32 GMT  
		Size: 2.1 MB (2061813 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdf5881c9caee2982a1f6e4fd384c3d9a9758d471315989bdc2c7e9d6fe82262`  
		Last Modified: Tue, 03 Dec 2024 19:30:32 GMT  
		Size: 492.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `logstash:7.17.26` - unknown; unknown

```console
$ docker pull logstash@sha256:df8de812c1c7ae5d741af46b84b6d2a917ad5ffa54ca774065e6a6e4bdba2176
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3342661 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6d81999f2643343581d519bd06cfbfb3eb96aae567d0e65a84bf3e132c88568f`

```dockerfile
```

-	Layers:
	-	`sha256:fb8e580a1164c26525d7db74bc1e10a47ef9fe186981393e2c7348a24ce3466a`  
		Last Modified: Tue, 03 Dec 2024 19:30:30 GMT  
		Size: 3.3 MB (3310475 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:013204889f606a0d0eb98352aa450cbebaddea8072e5d3f08851d60f81345bb3`  
		Last Modified: Tue, 03 Dec 2024 19:30:30 GMT  
		Size: 32.2 KB (32186 bytes)  
		MIME: application/vnd.in-toto+json

### `logstash:7.17.26` - linux; arm64 variant v8

```console
$ docker pull logstash@sha256:848067865c10f07985e4f9601eda558d108781b09823c8a35ff0bbd1fc20231f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **434.4 MB (434355995 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:79544cc20f5729568343e6c74ff36a635d1c58a716477641ac19362cea2bfa60`
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
# Tue, 03 Dec 2024 13:02:17 GMT
RUN for iter in {1..10}; do     export DEBIAN_FRONTEND=noninteractive &&     apt-get update -y &&     apt-get upgrade -y &&     apt-get install -y procps findutils tar gzip curl &&     apt-get install -y locales &&     apt-get clean all &&     locale-gen 'en_US.UTF-8' &&     apt-get clean metadata &&     exit_code=0 && break || exit_code=$? &&     echo "packaging error: retry $iter in 10s" &&     apt-get clean all &&     apt-get clean metadata &&     sleep 10; done;     (exit $exit_code) # buildkit
# Tue, 03 Dec 2024 13:02:17 GMT
RUN groupadd --gid 1000 logstash &&     adduser --uid 1000 --gid 1000     --home /usr/share/logstash --no-create-home     logstash # buildkit
# Tue, 03 Dec 2024 13:02:17 GMT
RUN curl -Lo - https://artifacts.elastic.co/downloads/logstash/logstash-7.17.26-linux-$(arch).tar.gz |     tar zxf - -C /usr/share &&     mv /usr/share/logstash-7.17.26 /usr/share/logstash &&     chown --recursive logstash:logstash /usr/share/logstash/ &&     chown -R logstash:root /usr/share/logstash &&     chmod -R g=u /usr/share/logstash &&     mkdir /licenses/ &&     mv /usr/share/logstash/NOTICE.TXT /licenses/NOTICE.TXT &&     mv /usr/share/logstash/LICENSE.txt /licenses/LICENSE.txt &&     find /usr/share/logstash -type d -exec chmod g+s {} \; &&     ln -s /usr/share/logstash /opt/logstash # buildkit
# Tue, 03 Dec 2024 13:02:17 GMT
WORKDIR /usr/share/logstash
# Tue, 03 Dec 2024 13:02:17 GMT
ENV ELASTIC_CONTAINER=true
# Tue, 03 Dec 2024 13:02:17 GMT
ENV PATH=/usr/share/logstash/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Dec 2024 13:02:17 GMT
COPY config/pipelines.yml config/pipelines.yml # buildkit
# Tue, 03 Dec 2024 13:02:17 GMT
COPY config/logstash-full.yml config/logstash.yml # buildkit
# Tue, 03 Dec 2024 13:02:17 GMT
COPY config/log4j2.properties config/ # buildkit
# Tue, 03 Dec 2024 13:02:17 GMT
COPY pipeline/default.conf pipeline/logstash.conf # buildkit
# Tue, 03 Dec 2024 13:02:17 GMT
RUN chown --recursive logstash:root config/ pipeline/ # buildkit
# Tue, 03 Dec 2024 13:02:17 GMT
ENV LANG=en_US.UTF-8 LC_ALL=en_US.UTF-8
# Tue, 03 Dec 2024 13:02:17 GMT
COPY env2yaml/env2yaml /usr/local/bin/ # buildkit
# Tue, 03 Dec 2024 13:02:17 GMT
COPY bin/docker-entrypoint /usr/local/bin/ # buildkit
# Tue, 03 Dec 2024 13:02:17 GMT
RUN chmod 0755 /usr/local/bin/docker-entrypoint # buildkit
# Tue, 03 Dec 2024 13:02:17 GMT
USER 1000
# Tue, 03 Dec 2024 13:02:17 GMT
EXPOSE map[5044/tcp:{} 9600/tcp:{}]
# Tue, 03 Dec 2024 13:02:17 GMT
LABEL org.label-schema.schema-version=1.0 org.label-schema.vendor=Elastic org.opencontainers.image.vendor=Elastic org.label-schema.name=logstash org.opencontainers.image.title=logstash org.label-schema.version=7.17.26 org.opencontainers.image.version=7.17.26 org.label-schema.url=https://www.elastic.co/products/logstash org.label-schema.vcs-url=https://github.com/elastic/logstash org.label-schema.license=Elastic License org.opencontainers.image.licenses=Elastic License org.opencontainers.image.description=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' org.label-schema.build-date=2024-10-22T09:18:02+00:00 org.opencontainers.image.created=2024-10-22T09:18:02+00:00
# Tue, 03 Dec 2024 13:02:17 GMT
ENTRYPOINT ["/usr/local/bin/docker-entrypoint"]
```

-	Layers:
	-	`sha256:1b9f3c55f9d4aa5c52eb67a4cb7d0f4726ab85a413b50e3e3fe788befce3d297`  
		Last Modified: Fri, 11 Oct 2024 04:41:30 GMT  
		Size: 26.0 MB (25973828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b15dab92dc341480f7f5fb5df70bbc8e2d54d871ae312465c70577e786879ad5`  
		Last Modified: Wed, 04 Dec 2024 01:50:17 GMT  
		Size: 38.5 MB (38499401 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4371ecc102d626f0d44b99b146222c9fdc100564b295f6fe90ebe35a71580ce1`  
		Last Modified: Wed, 04 Dec 2024 01:50:15 GMT  
		Size: 1.8 KB (1808 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ad79ff48d21795f46f4c2035131ed6f880cfab4b8a978abd395a8bfed720a9d`  
		Last Modified: Wed, 04 Dec 2024 01:50:23 GMT  
		Size: 367.8 MB (367816359 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc9c568c5686638d2257030838054153e3c3aa202ca72cffa57d5f4ed1475931`  
		Last Modified: Wed, 04 Dec 2024 01:50:16 GMT  
		Size: 378.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88bfd2e599a0ba382e318c2bd5ded1646d0b059595de7fc47acd5e61311f70f5`  
		Last Modified: Wed, 04 Dec 2024 01:50:16 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ed8b6ff5670a3ffe264b87b6578cb00b41ea8d5f80dcb097ce3ebddc60c042e`  
		Last Modified: Wed, 04 Dec 2024 01:50:17 GMT  
		Size: 472.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e463f9858dbcdd5d9e0c224464a6b14c166fcb91c3acebce247d0db7b4c7088`  
		Last Modified: Wed, 04 Dec 2024 01:50:17 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7271db100e21d65b11c350077a8886634fc47fb9a94c9e0d8cefaf734568468`  
		Last Modified: Wed, 04 Dec 2024 01:50:18 GMT  
		Size: 827.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:855a2e49bbfe7c0f0c37ceee421babd077877918548b40fbf68c8ba8c449175d`  
		Last Modified: Wed, 04 Dec 2024 01:50:18 GMT  
		Size: 2.1 MB (2061810 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4216a5300992c2d0718285f936b20d6e20e79d46bc31db3d34776f0d1b94901f`  
		Last Modified: Wed, 04 Dec 2024 01:50:18 GMT  
		Size: 492.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `logstash:7.17.26` - unknown; unknown

```console
$ docker pull logstash@sha256:905ede1fe4fc3405c018695ec51200f67966ffa41cad0f0d2470462a7deca5ea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3343024 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:baae475f168961496ca72a728a49a49a6943bcae0272a61fca18b72f64173b5c`

```dockerfile
```

-	Layers:
	-	`sha256:de4ae28cde3a3a92d46dab716a15ba907096762d1b4cc2b76a54c25d9a8367e0`  
		Last Modified: Wed, 04 Dec 2024 01:50:16 GMT  
		Size: 3.3 MB (3310710 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9b583fe96f3f853b8bdf1cfbbf2dafc67d2ca23ee74784aabf8f0c398d0c884d`  
		Last Modified: Wed, 04 Dec 2024 01:50:16 GMT  
		Size: 32.3 KB (32314 bytes)  
		MIME: application/vnd.in-toto+json

## `logstash:8.15.5`

```console
$ docker pull logstash@sha256:43949b5fee039921115f78d79c318503cc3b8af1a8efa798240a30c353568186
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `logstash:8.15.5` - linux; amd64

```console
$ docker pull logstash@sha256:f3de51b13bea6897ac7496fc46342d073d132c8eba88c8cae61662fae0b7a3a9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **515.4 MB (515357536 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4891356a761f2a9370c13271a5aa237fd683d9969491981712105c7f82bede67`
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
# Tue, 26 Nov 2024 10:47:54 GMT
RUN for iter in {1..10}; do       export DEBIAN_FRONTEND=noninteractive &&     apt-get update -y &&   apt-get upgrade -y &&   apt-get install -y procps findutils tar gzip &&         apt-get install -y locales &&         apt-get install -y curl &&     apt-get clean all &&       locale-gen 'en_US.UTF-8' &&     apt-get clean metadata &&   exit_code=0 && break || exit_code=$? && echo "packaging error: retry $iter in 10s" && apt-get clean all &&   apt-get clean metadata && sleep 10; done; (exit $exit_code) # buildkit
# Tue, 26 Nov 2024 10:47:54 GMT
RUN groupadd --gid 1000 logstash &&   adduser --uid 1000 --gid 1000 --home /usr/share/logstash --no-create-home logstash # buildkit
# Tue, 26 Nov 2024 10:47:54 GMT
RUN curl -Lo - https://artifacts.elastic.co/downloads/logstash/logstash-8.15.5-linux-$(arch).tar.gz |   tar zxf - -C /usr/share &&   mv /usr/share/logstash-8.15.5 /usr/share/logstash &&   chown --recursive logstash:logstash /usr/share/logstash/ &&   chown -R logstash:root /usr/share/logstash &&   chmod -R g=u /usr/share/logstash &&   mkdir /licenses/ &&   mv /usr/share/logstash/NOTICE.TXT /licenses/NOTICE.TXT &&   mv /usr/share/logstash/LICENSE.txt /licenses/LICENSE.txt &&   find /usr/share/logstash -type d -exec chmod g+s {} \; &&   ln -s /usr/share/logstash /opt/logstash # buildkit
# Tue, 26 Nov 2024 10:47:54 GMT
WORKDIR /usr/share/logstash
# Tue, 26 Nov 2024 10:47:54 GMT
ENV ELASTIC_CONTAINER=true
# Tue, 26 Nov 2024 10:47:54 GMT
ENV PATH=/usr/share/logstash/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 26 Nov 2024 10:47:54 GMT
COPY config/logstash-full.yml config/logstash.yml # buildkit
# Tue, 26 Nov 2024 10:47:54 GMT
COPY config/pipelines.yml config/log4j2.properties config/log4j2.file.properties config/ # buildkit
# Tue, 26 Nov 2024 10:47:54 GMT
COPY pipeline/default.conf pipeline/logstash.conf # buildkit
# Tue, 26 Nov 2024 10:47:54 GMT
RUN chown --recursive logstash:root config/ pipeline/ # buildkit
# Tue, 26 Nov 2024 10:47:54 GMT
ENV LANG=en_US.UTF-8 LC_ALL=en_US.UTF-8
# Tue, 26 Nov 2024 10:47:54 GMT
COPY env2yaml/env2yaml-amd64 env2yaml/env2yaml-arm64 env2yaml/ # buildkit
# Tue, 26 Nov 2024 10:47:54 GMT
RUN env2yamlarch="$(dpkg --print-architecture)";   case "${env2yamlarch}" in     'x86_64'|'amd64')       env2yamlarch=amd64;       ;;     'aarch64'|'arm64')       env2yamlarch=arm64;       ;;     *) echo >&2 "error: unsupported architecture '$env2yamlarch'"; exit 1 ;;   esac;   mkdir -p /usr/local/bin;   cp env2yaml/env2yaml-${env2yamlarch} /usr/local/bin/env2yaml;   rm -rf env2yaml # buildkit
# Tue, 26 Nov 2024 10:47:54 GMT
COPY bin/docker-entrypoint /usr/local/bin/ # buildkit
# Tue, 26 Nov 2024 10:47:54 GMT
RUN chmod 0755 /usr/local/bin/docker-entrypoint # buildkit
# Tue, 26 Nov 2024 10:47:54 GMT
USER 1000
# Tue, 26 Nov 2024 10:47:54 GMT
EXPOSE map[5044/tcp:{} 9600/tcp:{}]
# Tue, 26 Nov 2024 10:47:54 GMT
LABEL org.label-schema.schema-version=1.0 org.label-schema.vendor=Elastic org.opencontainers.image.vendor=Elastic org.label-schema.name=logstash org.opencontainers.image.title=logstash org.label-schema.version=8.15.5 org.opencontainers.image.version=8.15.5 org.label-schema.url=https://www.elastic.co/products/logstash org.label-schema.vcs-url=https://github.com/elastic/logstash org.label-schema.license=Elastic License org.opencontainers.image.licenses=Elastic License org.opencontainers.image.description=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' org.label-schema.build-date=2024-11-21T16:16:23+00:00 org.opencontainers.image.created=2024-11-21T16:16:23+00:00
# Tue, 26 Nov 2024 10:47:54 GMT
ENTRYPOINT ["/usr/local/bin/docker-entrypoint"]
```

-	Layers:
	-	`sha256:d9802f032d6798e2086607424bfe88cb8ec1d6f116e11cd99592dcaf261e9cd2`  
		Last Modified: Fri, 11 Oct 2024 04:41:25 GMT  
		Size: 27.5 MB (27511060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d467576d027ee917add60ed057027cbfafe9b6139f4e1f4112dad294c875ff3d`  
		Last Modified: Tue, 26 Nov 2024 18:24:55 GMT  
		Size: 50.4 MB (50409601 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6b6706af1a07618caa8d4af859709eaaf55e715275af7db3e8ae930e64ff1ba`  
		Last Modified: Tue, 26 Nov 2024 18:24:54 GMT  
		Size: 1.8 KB (1807 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f870dba6bf45b93d6c312446a20a53eb591da18477fec61880a38c38104e896`  
		Last Modified: Tue, 26 Nov 2024 18:25:07 GMT  
		Size: 431.4 MB (431363368 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2055655aa54efbbc940b03cc105344f2be0ec6ebb65557a56401b238265c5d8b`  
		Last Modified: Tue, 26 Nov 2024 18:24:54 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cee372098071524c765125781865849f1e06107f02880b3fbc82511c8e640ddd`  
		Last Modified: Tue, 26 Nov 2024 18:24:55 GMT  
		Size: 1.6 KB (1581 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d3ab42e604edb867443fc12e79875505daa2358932dc5115aa01969f204ab1a`  
		Last Modified: Tue, 26 Nov 2024 18:24:55 GMT  
		Size: 278.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89ac059fae36e7c58b9481f299a9340e80c3ede5de3eb69aafe21b341db222ac`  
		Last Modified: Tue, 26 Nov 2024 18:24:55 GMT  
		Size: 1.8 KB (1767 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7374e3741fa9f41ab713883e6a4e968bc11ed4c763d675d662c58e949ad17fd6`  
		Last Modified: Tue, 26 Nov 2024 18:24:56 GMT  
		Size: 4.0 MB (4001896 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fe5cb76831869a918f7ab07fefc5effc351dfd4a5aadb32c15bd3839b00ed30`  
		Last Modified: Tue, 26 Nov 2024 18:24:56 GMT  
		Size: 2.1 MB (2065124 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dceece115d91a46ab37701619e4e168a784d07dbf3abf2da6526e76ae62e0bc4`  
		Last Modified: Tue, 26 Nov 2024 18:24:56 GMT  
		Size: 713.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `logstash:8.15.5` - unknown; unknown

```console
$ docker pull logstash@sha256:00d89b30d6cd2e16f2a85e1e4b8ae09d44a0495920fb9ea005d991055744cac9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3563080 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cbcf1d3888254b991f9c480924b24b694d11a22d3f40e105040f1b44e1bead20`

```dockerfile
```

-	Layers:
	-	`sha256:d6e0b8e2edf5c000459180edc48df5cd4bb7e96866ead0b5d1a708fed113f43b`  
		Last Modified: Tue, 26 Nov 2024 18:24:54 GMT  
		Size: 3.5 MB (3528509 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:98661fd14c7f0d12a3a1d56ca390e9435fbdededb6e925dea4a2ebd0ce63cd08`  
		Last Modified: Tue, 26 Nov 2024 18:24:54 GMT  
		Size: 34.6 KB (34571 bytes)  
		MIME: application/vnd.in-toto+json

### `logstash:8.15.5` - linux; arm64 variant v8

```console
$ docker pull logstash@sha256:0081f5fc82a47b937b0155713f6dcdea4a35c1d24e42f3e1ed998e1da321db47
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **500.0 MB (500009957 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d3226f150472b2d4b63bc994c368445512c9aead831d08e8711664f54f2815fd`
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
# Tue, 26 Nov 2024 10:47:54 GMT
RUN for iter in {1..10}; do       export DEBIAN_FRONTEND=noninteractive &&     apt-get update -y &&   apt-get upgrade -y &&   apt-get install -y procps findutils tar gzip &&         apt-get install -y locales &&         apt-get install -y curl &&     apt-get clean all &&       locale-gen 'en_US.UTF-8' &&     apt-get clean metadata &&   exit_code=0 && break || exit_code=$? && echo "packaging error: retry $iter in 10s" && apt-get clean all &&   apt-get clean metadata && sleep 10; done; (exit $exit_code) # buildkit
# Tue, 26 Nov 2024 10:47:54 GMT
RUN groupadd --gid 1000 logstash &&   adduser --uid 1000 --gid 1000 --home /usr/share/logstash --no-create-home logstash # buildkit
# Tue, 26 Nov 2024 10:47:54 GMT
RUN curl -Lo - https://artifacts.elastic.co/downloads/logstash/logstash-8.15.5-linux-$(arch).tar.gz |   tar zxf - -C /usr/share &&   mv /usr/share/logstash-8.15.5 /usr/share/logstash &&   chown --recursive logstash:logstash /usr/share/logstash/ &&   chown -R logstash:root /usr/share/logstash &&   chmod -R g=u /usr/share/logstash &&   mkdir /licenses/ &&   mv /usr/share/logstash/NOTICE.TXT /licenses/NOTICE.TXT &&   mv /usr/share/logstash/LICENSE.txt /licenses/LICENSE.txt &&   find /usr/share/logstash -type d -exec chmod g+s {} \; &&   ln -s /usr/share/logstash /opt/logstash # buildkit
# Tue, 26 Nov 2024 10:47:54 GMT
WORKDIR /usr/share/logstash
# Tue, 26 Nov 2024 10:47:54 GMT
ENV ELASTIC_CONTAINER=true
# Tue, 26 Nov 2024 10:47:54 GMT
ENV PATH=/usr/share/logstash/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 26 Nov 2024 10:47:54 GMT
COPY config/logstash-full.yml config/logstash.yml # buildkit
# Tue, 26 Nov 2024 10:47:54 GMT
COPY config/pipelines.yml config/log4j2.properties config/log4j2.file.properties config/ # buildkit
# Tue, 26 Nov 2024 10:47:54 GMT
COPY pipeline/default.conf pipeline/logstash.conf # buildkit
# Tue, 26 Nov 2024 10:47:54 GMT
RUN chown --recursive logstash:root config/ pipeline/ # buildkit
# Tue, 26 Nov 2024 10:47:54 GMT
ENV LANG=en_US.UTF-8 LC_ALL=en_US.UTF-8
# Tue, 26 Nov 2024 10:47:54 GMT
COPY env2yaml/env2yaml-amd64 env2yaml/env2yaml-arm64 env2yaml/ # buildkit
# Tue, 26 Nov 2024 10:47:54 GMT
RUN env2yamlarch="$(dpkg --print-architecture)";   case "${env2yamlarch}" in     'x86_64'|'amd64')       env2yamlarch=amd64;       ;;     'aarch64'|'arm64')       env2yamlarch=arm64;       ;;     *) echo >&2 "error: unsupported architecture '$env2yamlarch'"; exit 1 ;;   esac;   mkdir -p /usr/local/bin;   cp env2yaml/env2yaml-${env2yamlarch} /usr/local/bin/env2yaml;   rm -rf env2yaml # buildkit
# Tue, 26 Nov 2024 10:47:54 GMT
COPY bin/docker-entrypoint /usr/local/bin/ # buildkit
# Tue, 26 Nov 2024 10:47:54 GMT
RUN chmod 0755 /usr/local/bin/docker-entrypoint # buildkit
# Tue, 26 Nov 2024 10:47:54 GMT
USER 1000
# Tue, 26 Nov 2024 10:47:54 GMT
EXPOSE map[5044/tcp:{} 9600/tcp:{}]
# Tue, 26 Nov 2024 10:47:54 GMT
LABEL org.label-schema.schema-version=1.0 org.label-schema.vendor=Elastic org.opencontainers.image.vendor=Elastic org.label-schema.name=logstash org.opencontainers.image.title=logstash org.label-schema.version=8.15.5 org.opencontainers.image.version=8.15.5 org.label-schema.url=https://www.elastic.co/products/logstash org.label-schema.vcs-url=https://github.com/elastic/logstash org.label-schema.license=Elastic License org.opencontainers.image.licenses=Elastic License org.opencontainers.image.description=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' org.label-schema.build-date=2024-11-21T16:16:23+00:00 org.opencontainers.image.created=2024-11-21T16:16:23+00:00
# Tue, 26 Nov 2024 10:47:54 GMT
ENTRYPOINT ["/usr/local/bin/docker-entrypoint"]
```

-	Layers:
	-	`sha256:1b9f3c55f9d4aa5c52eb67a4cb7d0f4726ab85a413b50e3e3fe788befce3d297`  
		Last Modified: Fri, 11 Oct 2024 04:41:30 GMT  
		Size: 26.0 MB (25973828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79676800b9a2ae226dc384582a2bae1d0ddec86dc46fc29d0d8a5b8459060953`  
		Last Modified: Mon, 18 Nov 2024 23:51:28 GMT  
		Size: 38.5 MB (38487075 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d025482904aeb44a113a53cf5d18a7d0af58be62c4efe85397a3e7abf888bff7`  
		Last Modified: Mon, 18 Nov 2024 23:51:21 GMT  
		Size: 1.8 KB (1807 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fcdad7cbb33ea66d7fa0ad7c7896b2407744d2032f9462dc3efe10dfdeabde69`  
		Last Modified: Tue, 26 Nov 2024 18:35:59 GMT  
		Size: 429.6 MB (429603717 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85ab8446a2b0b5c5aea02da8e4357842adee7c6980de0ba35298bfb659b4531c`  
		Last Modified: Tue, 26 Nov 2024 18:35:51 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52c50765c2d6c8d15a472d35a9e410cb907ddd33567cc4ae209c07021e3fdb5e`  
		Last Modified: Tue, 26 Nov 2024 18:35:51 GMT  
		Size: 1.6 KB (1576 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1af2406cfa7359e0aba26cec4a80ad41cd9d550e7e7f4bcae3d84866949beea9`  
		Last Modified: Tue, 26 Nov 2024 18:35:51 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72852dc912f589de751bf09cdbbe4df2efc80fcd72393edd2ca6c5edd2551bd2`  
		Last Modified: Tue, 26 Nov 2024 18:35:52 GMT  
		Size: 1.8 KB (1761 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:170ac01a72c1b7141476084cd0888fea3db75dc58bdead14aa6be18420d2eda2`  
		Last Modified: Tue, 26 Nov 2024 18:35:52 GMT  
		Size: 4.0 MB (4001887 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:526b149cab116c8bbdfffcdf5d4cb7cf3cdd691d8ff07fc9db3d25fff645f728`  
		Last Modified: Tue, 26 Nov 2024 18:35:52 GMT  
		Size: 1.9 MB (1936982 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f65f99bec163bdf85b20388e53e54c7206ecad9f5ffdaed47bed110fdae37ce`  
		Last Modified: Tue, 26 Nov 2024 18:35:53 GMT  
		Size: 709.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `logstash:8.15.5` - unknown; unknown

```console
$ docker pull logstash@sha256:334a1191d51b8f0c8cadb6f2838554df90da359febe778cfc0e3e171c49fe40b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3562833 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:037435ee020fb8e8317f3f05792828708da75554109628d4fcd7acbc84f877d7`

```dockerfile
```

-	Layers:
	-	`sha256:211ae244ac25c0ec994a4771b090c64c22b8659938a389b37eb018b519382f1a`  
		Last Modified: Tue, 26 Nov 2024 18:35:51 GMT  
		Size: 3.5 MB (3528119 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e3be302d019b01d07f980b3a45ffd6107f0a219af0445bdc1401af5abb469b8f`  
		Last Modified: Tue, 26 Nov 2024 18:35:51 GMT  
		Size: 34.7 KB (34714 bytes)  
		MIME: application/vnd.in-toto+json

## `logstash:8.16.1`

```console
$ docker pull logstash@sha256:dca706ef2cf7b0ea326f49bec73647c04270fc763d73eabf93408161955793a0
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `logstash:8.16.1` - linux; amd64

```console
$ docker pull logstash@sha256:a40a832bb6326f09f7e838abb1173923cc047917469cff0a9a26b95d1f6f38dc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **515.5 MB (515455318 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fd31c622a44e005068175bd014caf3f2cbedd5e298d64434366759413ed01b50`
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
# Thu, 21 Nov 2024 14:43:56 GMT
RUN for iter in {1..10}; do       export DEBIAN_FRONTEND=noninteractive &&     apt-get update -y &&   apt-get upgrade -y &&   apt-get install -y procps findutils tar gzip &&         apt-get install -y locales &&         apt-get install -y curl &&     apt-get clean all &&       locale-gen 'en_US.UTF-8' &&     apt-get clean metadata &&   exit_code=0 && break || exit_code=$? && echo "packaging error: retry $iter in 10s" && apt-get clean all &&   apt-get clean metadata && sleep 10; done; (exit $exit_code) # buildkit
# Thu, 21 Nov 2024 14:43:56 GMT
RUN groupadd --gid 1000 logstash &&   adduser --uid 1000 --gid 1000 --home /usr/share/logstash --no-create-home logstash # buildkit
# Thu, 21 Nov 2024 14:43:56 GMT
RUN curl -Lo - https://artifacts.elastic.co/downloads/logstash/logstash-8.16.1-linux-$(arch).tar.gz |   tar zxf - -C /usr/share &&   mv /usr/share/logstash-8.16.1 /usr/share/logstash &&   chown --recursive logstash:logstash /usr/share/logstash/ &&   chown -R logstash:root /usr/share/logstash &&   chmod -R g=u /usr/share/logstash &&   mkdir /licenses/ &&   mv /usr/share/logstash/NOTICE.TXT /licenses/NOTICE.TXT &&   mv /usr/share/logstash/LICENSE.txt /licenses/LICENSE.txt &&   find /usr/share/logstash -type d -exec chmod g+s {} \; &&   ln -s /usr/share/logstash /opt/logstash # buildkit
# Thu, 21 Nov 2024 14:43:56 GMT
WORKDIR /usr/share/logstash
# Thu, 21 Nov 2024 14:43:56 GMT
ENV ELASTIC_CONTAINER=true
# Thu, 21 Nov 2024 14:43:56 GMT
ENV PATH=/usr/share/logstash/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 21 Nov 2024 14:43:56 GMT
COPY config/logstash-full.yml config/logstash.yml # buildkit
# Thu, 21 Nov 2024 14:43:56 GMT
COPY config/pipelines.yml config/log4j2.properties config/log4j2.file.properties config/ # buildkit
# Thu, 21 Nov 2024 14:43:56 GMT
COPY pipeline/default.conf pipeline/logstash.conf # buildkit
# Thu, 21 Nov 2024 14:43:56 GMT
RUN chown --recursive logstash:root config/ pipeline/ # buildkit
# Thu, 21 Nov 2024 14:43:56 GMT
ENV LANG=en_US.UTF-8 LC_ALL=en_US.UTF-8
# Thu, 21 Nov 2024 14:43:56 GMT
COPY env2yaml/env2yaml-amd64 env2yaml/env2yaml-arm64 env2yaml/ # buildkit
# Thu, 21 Nov 2024 14:43:56 GMT
RUN env2yamlarch="$(dpkg --print-architecture)";   case "${env2yamlarch}" in     'x86_64'|'amd64')       env2yamlarch=amd64;       ;;     'aarch64'|'arm64')       env2yamlarch=arm64;       ;;     *) echo >&2 "error: unsupported architecture '$env2yamlarch'"; exit 1 ;;   esac;   mkdir -p /usr/local/bin;   cp env2yaml/env2yaml-${env2yamlarch} /usr/local/bin/env2yaml;   rm -rf env2yaml # buildkit
# Thu, 21 Nov 2024 14:43:56 GMT
COPY bin/docker-entrypoint /usr/local/bin/ # buildkit
# Thu, 21 Nov 2024 14:43:56 GMT
RUN chmod 0755 /usr/local/bin/docker-entrypoint # buildkit
# Thu, 21 Nov 2024 14:43:56 GMT
USER 1000
# Thu, 21 Nov 2024 14:43:56 GMT
EXPOSE map[5044/tcp:{} 9600/tcp:{}]
# Thu, 21 Nov 2024 14:43:56 GMT
LABEL org.label-schema.schema-version=1.0 org.label-schema.vendor=Elastic org.opencontainers.image.vendor=Elastic org.label-schema.name=logstash org.opencontainers.image.title=logstash org.label-schema.version=8.16.1 org.opencontainers.image.version=8.16.1 org.label-schema.url=https://www.elastic.co/products/logstash org.label-schema.vcs-url=https://github.com/elastic/logstash org.label-schema.license=Elastic License org.opencontainers.image.licenses=Elastic License org.opencontainers.image.description=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' org.label-schema.build-date=2024-11-19T01:53:47+00:00 org.opencontainers.image.created=2024-11-19T01:53:47+00:00
# Thu, 21 Nov 2024 14:43:56 GMT
ENTRYPOINT ["/usr/local/bin/docker-entrypoint"]
```

-	Layers:
	-	`sha256:d9802f032d6798e2086607424bfe88cb8ec1d6f116e11cd99592dcaf261e9cd2`  
		Last Modified: Fri, 11 Oct 2024 04:41:25 GMT  
		Size: 27.5 MB (27511060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd80872c9925b6f48397a6937dc5be5e9373358f98508c764e9d929dc25689e3`  
		Last Modified: Fri, 22 Nov 2024 22:26:11 GMT  
		Size: 50.4 MB (50408006 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:363de12eb4ff2aec1086ab4499aa06074f4ea13d96d0a07ded975719405a3489`  
		Last Modified: Fri, 22 Nov 2024 22:26:10 GMT  
		Size: 1.8 KB (1806 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4ebe8adab0a34021d4cd1cac5b802f8a6b8752df68935f97e47f848ec59df67`  
		Last Modified: Fri, 22 Nov 2024 22:26:17 GMT  
		Size: 431.5 MB (431462753 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:afde81803e1e75ddfa396bb408f2b6aae7ef763adab17fea78ff509375c7f38f`  
		Last Modified: Fri, 22 Nov 2024 22:26:10 GMT  
		Size: 278.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d66239faf6529a87f2645a6072cd214e7170c84c3122b320ef51564d3d79a908`  
		Last Modified: Fri, 22 Nov 2024 22:26:11 GMT  
		Size: 1.6 KB (1582 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:adede9264b3cba4e05f29c4a78b468a3cad6ad572534cd4a672e95d3f4ce12bf`  
		Last Modified: Fri, 22 Nov 2024 22:26:11 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1439ce21dc366f956be64cd5a61f428c94134638365ed2e25d60ad1e2bbc8e4`  
		Last Modified: Fri, 22 Nov 2024 22:26:12 GMT  
		Size: 1.8 KB (1764 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a534824f74d362b3b248ec465f8a17466c320bfb45ebd68bcccc4910b1632b92`  
		Last Modified: Fri, 22 Nov 2024 22:26:12 GMT  
		Size: 4.0 MB (4001890 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c35a282d07a3b67a7689c5a03f3bc07411ff413ac272773bc2a7c3f8a5794e5`  
		Last Modified: Fri, 22 Nov 2024 22:26:13 GMT  
		Size: 2.1 MB (2065126 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6379766a8d4536ba8c0897f1f7be2dd83963d814e028fe91fef745e8837fa4c7`  
		Last Modified: Fri, 22 Nov 2024 22:26:13 GMT  
		Size: 712.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `logstash:8.16.1` - unknown; unknown

```console
$ docker pull logstash@sha256:d5f2272e6517d03bce5cbbdff7cdbefdf136d85c3ccb8394faf0fe79d4cc8522
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3558822 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:11e7bca2dc6c7c277467d5480c4ff9cd27dcbcc2df8ff54bdb860d88e63d1f82`

```dockerfile
```

-	Layers:
	-	`sha256:46427d5071ef08e19c9ea7546a46943c38364dc4445101225dec07b3a54d1a4e`  
		Last Modified: Fri, 22 Nov 2024 22:26:10 GMT  
		Size: 3.5 MB (3524251 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3f7a4f6710a06aaadb029a21d7ef106cfc61a95ecc62e4439d69ba50c8401660`  
		Last Modified: Fri, 22 Nov 2024 22:26:10 GMT  
		Size: 34.6 KB (34571 bytes)  
		MIME: application/vnd.in-toto+json

### `logstash:8.16.1` - linux; arm64 variant v8

```console
$ docker pull logstash@sha256:df5af145fc4ca05deaf69963d6b51c54e5082b716cc83fefe41b1a3c812ef0d4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **500.1 MB (500102906 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a42c729c3ef93d4c1cc1d43a0a26dc70f56f965df020c218e646f5ca2e629b20`
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
# Thu, 21 Nov 2024 14:43:56 GMT
RUN for iter in {1..10}; do       export DEBIAN_FRONTEND=noninteractive &&     apt-get update -y &&   apt-get upgrade -y &&   apt-get install -y procps findutils tar gzip &&         apt-get install -y locales &&         apt-get install -y curl &&     apt-get clean all &&       locale-gen 'en_US.UTF-8' &&     apt-get clean metadata &&   exit_code=0 && break || exit_code=$? && echo "packaging error: retry $iter in 10s" && apt-get clean all &&   apt-get clean metadata && sleep 10; done; (exit $exit_code) # buildkit
# Thu, 21 Nov 2024 14:43:56 GMT
RUN groupadd --gid 1000 logstash &&   adduser --uid 1000 --gid 1000 --home /usr/share/logstash --no-create-home logstash # buildkit
# Thu, 21 Nov 2024 14:43:56 GMT
RUN curl -Lo - https://artifacts.elastic.co/downloads/logstash/logstash-8.16.1-linux-$(arch).tar.gz |   tar zxf - -C /usr/share &&   mv /usr/share/logstash-8.16.1 /usr/share/logstash &&   chown --recursive logstash:logstash /usr/share/logstash/ &&   chown -R logstash:root /usr/share/logstash &&   chmod -R g=u /usr/share/logstash &&   mkdir /licenses/ &&   mv /usr/share/logstash/NOTICE.TXT /licenses/NOTICE.TXT &&   mv /usr/share/logstash/LICENSE.txt /licenses/LICENSE.txt &&   find /usr/share/logstash -type d -exec chmod g+s {} \; &&   ln -s /usr/share/logstash /opt/logstash # buildkit
# Thu, 21 Nov 2024 14:43:56 GMT
WORKDIR /usr/share/logstash
# Thu, 21 Nov 2024 14:43:56 GMT
ENV ELASTIC_CONTAINER=true
# Thu, 21 Nov 2024 14:43:56 GMT
ENV PATH=/usr/share/logstash/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 21 Nov 2024 14:43:56 GMT
COPY config/logstash-full.yml config/logstash.yml # buildkit
# Thu, 21 Nov 2024 14:43:56 GMT
COPY config/pipelines.yml config/log4j2.properties config/log4j2.file.properties config/ # buildkit
# Thu, 21 Nov 2024 14:43:56 GMT
COPY pipeline/default.conf pipeline/logstash.conf # buildkit
# Thu, 21 Nov 2024 14:43:56 GMT
RUN chown --recursive logstash:root config/ pipeline/ # buildkit
# Thu, 21 Nov 2024 14:43:56 GMT
ENV LANG=en_US.UTF-8 LC_ALL=en_US.UTF-8
# Thu, 21 Nov 2024 14:43:56 GMT
COPY env2yaml/env2yaml-amd64 env2yaml/env2yaml-arm64 env2yaml/ # buildkit
# Thu, 21 Nov 2024 14:43:56 GMT
RUN env2yamlarch="$(dpkg --print-architecture)";   case "${env2yamlarch}" in     'x86_64'|'amd64')       env2yamlarch=amd64;       ;;     'aarch64'|'arm64')       env2yamlarch=arm64;       ;;     *) echo >&2 "error: unsupported architecture '$env2yamlarch'"; exit 1 ;;   esac;   mkdir -p /usr/local/bin;   cp env2yaml/env2yaml-${env2yamlarch} /usr/local/bin/env2yaml;   rm -rf env2yaml # buildkit
# Thu, 21 Nov 2024 14:43:56 GMT
COPY bin/docker-entrypoint /usr/local/bin/ # buildkit
# Thu, 21 Nov 2024 14:43:56 GMT
RUN chmod 0755 /usr/local/bin/docker-entrypoint # buildkit
# Thu, 21 Nov 2024 14:43:56 GMT
USER 1000
# Thu, 21 Nov 2024 14:43:56 GMT
EXPOSE map[5044/tcp:{} 9600/tcp:{}]
# Thu, 21 Nov 2024 14:43:56 GMT
LABEL org.label-schema.schema-version=1.0 org.label-schema.vendor=Elastic org.opencontainers.image.vendor=Elastic org.label-schema.name=logstash org.opencontainers.image.title=logstash org.label-schema.version=8.16.1 org.opencontainers.image.version=8.16.1 org.label-schema.url=https://www.elastic.co/products/logstash org.label-schema.vcs-url=https://github.com/elastic/logstash org.label-schema.license=Elastic License org.opencontainers.image.licenses=Elastic License org.opencontainers.image.description=Logstash is a free and open server-side data processing pipeline that ingests data from a multitude of sources, transforms it, and then sends it to your favorite 'stash.' org.label-schema.build-date=2024-11-19T01:53:47+00:00 org.opencontainers.image.created=2024-11-19T01:53:47+00:00
# Thu, 21 Nov 2024 14:43:56 GMT
ENTRYPOINT ["/usr/local/bin/docker-entrypoint"]
```

-	Layers:
	-	`sha256:1b9f3c55f9d4aa5c52eb67a4cb7d0f4726ab85a413b50e3e3fe788befce3d297`  
		Last Modified: Fri, 11 Oct 2024 04:41:30 GMT  
		Size: 26.0 MB (25973828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79676800b9a2ae226dc384582a2bae1d0ddec86dc46fc29d0d8a5b8459060953`  
		Last Modified: Mon, 18 Nov 2024 23:51:28 GMT  
		Size: 38.5 MB (38487075 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d025482904aeb44a113a53cf5d18a7d0af58be62c4efe85397a3e7abf888bff7`  
		Last Modified: Mon, 18 Nov 2024 23:51:21 GMT  
		Size: 1.8 KB (1807 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e47bed8a6240efdbe4462480b8e42d506fe2c4e71723181decba9c6582905498`  
		Last Modified: Fri, 22 Nov 2024 22:41:26 GMT  
		Size: 429.7 MB (429696658 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f07ba47bab9006d488a02f8272b30b6e4484c969109ee52d7974a0ec19f5b5a1`  
		Last Modified: Fri, 22 Nov 2024 22:41:13 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4cf88e69d76fd18dccdb70bd45b0d010c3270356b44a067c98a69227f1305a74`  
		Last Modified: Fri, 22 Nov 2024 22:41:11 GMT  
		Size: 1.6 KB (1576 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2978499e6052f9df9ebbda0ba05c3a72c0d492c396b69d2750980aca3331754`  
		Last Modified: Fri, 22 Nov 2024 22:41:11 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d793204f9ab56c7ef3b468874b288c107715b7fe90d87955c1e1d771210e1f23`  
		Last Modified: Fri, 22 Nov 2024 22:41:12 GMT  
		Size: 1.8 KB (1766 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9589ad38fb02eb2a5ab4a02c19cf3597494ac52ac9dedfdd896cdb3440162558`  
		Last Modified: Fri, 22 Nov 2024 22:41:12 GMT  
		Size: 4.0 MB (4001890 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03350f2a738dde0c0e914e2e922b6dfba6bba204059c637192a588758fdc1ea6`  
		Last Modified: Fri, 22 Nov 2024 22:41:13 GMT  
		Size: 1.9 MB (1936981 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b84fad0ef32e07350f225582268892c3e83e5f17596942bc65e968222817a0c`  
		Last Modified: Fri, 22 Nov 2024 22:41:13 GMT  
		Size: 710.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `logstash:8.16.1` - unknown; unknown

```console
$ docker pull logstash@sha256:4a53918afe3dc725e0fef6d04d1625a481091094953dab0aa8904672c9628141
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3558575 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1131906f3c3b1599ba30a4a4ee915d5bb4fdc29a2a2756af669b9b6342d88d61`

```dockerfile
```

-	Layers:
	-	`sha256:efaab9398f139731f147f5bd0000ef0ef5da739b6c8f183c14a8f15eef08941d`  
		Last Modified: Fri, 22 Nov 2024 22:41:11 GMT  
		Size: 3.5 MB (3523861 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:24c736e1ed149ee08564f6704126b7746ba67b7893727639c3e516246c1b5407`  
		Last Modified: Fri, 22 Nov 2024 22:41:10 GMT  
		Size: 34.7 KB (34714 bytes)  
		MIME: application/vnd.in-toto+json
