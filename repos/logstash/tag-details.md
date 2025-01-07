<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `logstash`

-	[`logstash:7.17.26`](#logstash71726)
-	[`logstash:8.16.2`](#logstash8162)
-	[`logstash:8.17.0`](#logstash8170)

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
		Size: 371.0 MB (370999252 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1d9318cb0250cd0fac086ce89a6d4a37c10e0d22b8a668dd1cedb3e5ab5c1a1`  
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
		Last Modified: Tue, 17 Dec 2024 19:30:07 GMT  
		Size: 1.6 KB (1581 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f96cc820f953aab08efca434b32dcad8d8ea51eac563f66a50e0b7918cf3bb8`  
		Last Modified: Tue, 17 Dec 2024 19:30:07 GMT  
		Size: 278.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:163a509abab25901c90b4523288a79041800a826192f9f5934030c986bce725a`  
		Last Modified: Tue, 17 Dec 2024 19:30:08 GMT  
		Size: 1.8 KB (1766 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7b294de323226e205d10f3a5433bb6c90aa2261b7b68482cac2df09fd83ddad`  
		Last Modified: Tue, 17 Dec 2024 19:30:08 GMT  
		Size: 4.0 MB (4004301 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d36526edd89b7fe509288ca21bb6ad1d8cf5e215687572a0cb4ad311483bd80`  
		Last Modified: Tue, 17 Dec 2024 19:30:08 GMT  
		Size: 2.1 MB (2066564 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff65d649460ed48148dfcb51c0a1695e66258e679eb8962fc570c9c70923eb33`  
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
		Last Modified: Tue, 17 Dec 2024 19:30:06 GMT  
		Size: 3.5 MB (3517329 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:90e9009657735628c549fd6371d384b0f86dbf22719598947f5eaf41bba1d826`  
		Last Modified: Tue, 17 Dec 2024 19:30:06 GMT  
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
		Last Modified: Fri, 11 Oct 2024 04:41:30 GMT  
		Size: 26.0 MB (25973828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7607b73ed44e6a98b7e6a19eea72f5e863956fea3129734cb9581e4701b38e5e`  
		Last Modified: Tue, 17 Dec 2024 19:49:01 GMT  
		Size: 38.6 MB (38580216 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5dfe66d81f9cc1524352bdab74f4ad34bbcc7751bc9b4596d331b2925b46ca4b`  
		Last Modified: Tue, 17 Dec 2024 19:49:00 GMT  
		Size: 1.8 KB (1806 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b30503e174ba5af59259f81da68b531cc4a4486a22be7ff1e881664bc56907e`  
		Last Modified: Tue, 17 Dec 2024 19:49:09 GMT  
		Size: 434.5 MB (434523092 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6896d9800d92641a5a4518275db6ff9c42b35704da2400ab36835525d1c6faa3`  
		Last Modified: Tue, 17 Dec 2024 19:49:00 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24b5fd36626bb491d50ee42ebac60cc159df99a47e200dd6c656867c384e44ad`  
		Last Modified: Tue, 17 Dec 2024 19:49:01 GMT  
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
		Last Modified: Tue, 17 Dec 2024 19:49:00 GMT  
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
		Size: 27.5 MB (27511060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:731445757cc46ed4479fdc9a155b6abd88df2233d8eeda2a0e88de7b93f00908`  
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
		Last Modified: Tue, 17 Dec 2024 19:30:17 GMT  
		Size: 2.1 MB (2065126 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd863fd6f1555ca10d2d1fdd20dbb8af8456ef7c3a56c98d8afad246de879673`  
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
		Last Modified: Tue, 17 Dec 2024 19:30:15 GMT  
		Size: 3.5 MB (3518888 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:47b8253992ed9d1f4be92e39f3636f842a16ab994e754f10c600694be5145581`  
		Last Modified: Tue, 17 Dec 2024 19:30:14 GMT  
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
		Last Modified: Fri, 11 Oct 2024 04:41:30 GMT  
		Size: 26.0 MB (25973828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7607b73ed44e6a98b7e6a19eea72f5e863956fea3129734cb9581e4701b38e5e`  
		Last Modified: Tue, 17 Dec 2024 19:49:01 GMT  
		Size: 38.6 MB (38580216 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5dfe66d81f9cc1524352bdab74f4ad34bbcc7751bc9b4596d331b2925b46ca4b`  
		Last Modified: Tue, 17 Dec 2024 19:49:00 GMT  
		Size: 1.8 KB (1806 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b60b5dcf2d91b3b266659d90fa8b487259bdb6a3e646aa1e4102063288dcbc1`  
		Last Modified: Tue, 17 Dec 2024 19:50:41 GMT  
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
		Size: 1.6 KB (1578 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3476b68f1c78458dad18bbc5ed6c84e7287a2a398b44bd3507d13d06934d5905`  
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
		Last Modified: Tue, 17 Dec 2024 19:50:32 GMT  
		Size: 3.5 MB (3518500 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:24c3f926e116d09208269d6b708c19a143192e1fb480161b5e501edcf70c1b2f`  
		Last Modified: Tue, 17 Dec 2024 19:50:32 GMT  
		Size: 34.7 KB (34714 bytes)  
		MIME: application/vnd.in-toto+json
