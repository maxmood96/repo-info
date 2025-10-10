<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `elasticsearch`

-	[`elasticsearch:8.17.10`](#elasticsearch81710)
-	[`elasticsearch:8.18.8`](#elasticsearch8188)
-	[`elasticsearch:8.19.5`](#elasticsearch8195)
-	[`elasticsearch:9.0.8`](#elasticsearch908)
-	[`elasticsearch:9.1.5`](#elasticsearch915)

## `elasticsearch:8.17.10`

```console
$ docker pull elasticsearch@sha256:b3de9d0a05f0839c9f3d6881429bf0b6c3bef0a2ca0c3df80fa819d1f4d10be4
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `elasticsearch:8.17.10` - linux; amd64

```console
$ docker pull elasticsearch@sha256:be6ec2f2335a3b82e0cfde2805213ab500dad69ab519ea30a9bd1412fffe7d96
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **677.6 MB (677633917 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:33f67c1a16429e5e7d993c0b24b2b1ad11b1a3bcd82ba9cba9b7495c512499a9`
-	Entrypoint: `["\/bin\/tini","--","\/usr\/local\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["eswrapper"]`

```dockerfile
# Tue, 12 Aug 2025 08:18:47 GMT
ARG RELEASE
# Tue, 12 Aug 2025 08:18:47 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 12 Aug 2025 08:18:47 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 12 Aug 2025 08:18:47 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 12 Aug 2025 08:18:47 GMT
ADD file:249778a1782b02a1c2bcf9f292f5778d81442a53c3de1958d712f10baf7e0b60 in / 
# Tue, 12 Aug 2025 08:18:47 GMT
CMD ["/bin/bash"]
# Tue, 12 Aug 2025 08:18:47 GMT
RUN yes no | dpkg-reconfigure dash &&     for iter in 1 2 3 4 5 6 7 8 9 10; do       export DEBIAN_FRONTEND=noninteractive &&       apt-get update &&       apt-get upgrade -y &&       apt-get install -y --no-install-recommends         ca-certificates curl netcat-openbsd p11-kit unzip zip  &&       apt-get clean &&       rm -rf /var/lib/apt/lists/* &&       exit_code=0 && break ||         exit_code=$? && echo "apt-get error: retry $iter in 10s" && sleep 10;     done;     exit $exit_code # buildkit
# Tue, 12 Aug 2025 08:18:47 GMT
RUN userdel -r ubuntu &&     groupadd -g 1000 elasticsearch &&     useradd --uid 1000 --gid 1000 --home-dir /usr/share/elasticsearch --create-home elasticsearch &&     usermod -aG root elasticsearch &&     chown -R 0:0 /usr/share/elasticsearch # buildkit
# Tue, 12 Aug 2025 08:18:47 GMT
ENV ELASTIC_CONTAINER=true
# Tue, 12 Aug 2025 08:18:47 GMT
WORKDIR /usr/share/elasticsearch
# Tue, 12 Aug 2025 08:18:47 GMT
COPY --chown=0:0 /usr/share/elasticsearch /usr/share/elasticsearch # buildkit
# Tue, 12 Aug 2025 08:18:47 GMT
COPY --chown=0:0 /bin/tini /bin/tini # buildkit
# Tue, 12 Aug 2025 08:18:47 GMT
ENV PATH=/usr/share/elasticsearch/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 Aug 2025 08:18:47 GMT
ENV SHELL=/bin/bash
# Tue, 12 Aug 2025 08:18:47 GMT
COPY bin/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh # buildkit
# Tue, 12 Aug 2025 08:18:47 GMT
RUN chmod g=u /etc/passwd &&     chmod 0555 /usr/local/bin/docker-entrypoint.sh &&     find / -xdev -perm -4000 -exec chmod ug-s {} + &&     chmod 0775 /usr/share/elasticsearch &&     chown elasticsearch bin config config/jvm.options.d data logs plugins # buildkit
# Tue, 12 Aug 2025 08:18:47 GMT
COPY bin/docker-openjdk /etc/ca-certificates/update.d/docker-openjdk # buildkit
# Tue, 12 Aug 2025 08:18:47 GMT
RUN /etc/ca-certificates/update.d/docker-openjdk # buildkit
# Tue, 12 Aug 2025 08:18:47 GMT
EXPOSE map[9200/tcp:{} 9300/tcp:{}]
# Tue, 12 Aug 2025 08:18:47 GMT
LABEL org.label-schema.build-date=2025-08-08T08:36:52.872377389Z org.label-schema.license=Elastic-License-2.0 org.label-schema.name=Elasticsearch org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/elasticsearch org.label-schema.usage=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.label-schema.vcs-ref=e5c4b2af120c131ea2885730f6693cb7d40a0a63 org.label-schema.vcs-url=https://github.com/elastic/elasticsearch org.label-schema.vendor=Elastic org.label-schema.version=8.17.10 org.opencontainers.image.created=2025-08-08T08:36:52.872377389Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.opencontainers.image.licenses=Elastic-License-2.0 org.opencontainers.image.revision=e5c4b2af120c131ea2885730f6693cb7d40a0a63 org.opencontainers.image.source=https://github.com/elastic/elasticsearch org.opencontainers.image.title=Elasticsearch org.opencontainers.image.url=https://www.elastic.co/products/elasticsearch org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=8.17.10
# Tue, 12 Aug 2025 08:18:47 GMT
ENTRYPOINT ["/bin/tini" "--" "/usr/local/bin/docker-entrypoint.sh"]
# Tue, 12 Aug 2025 08:18:47 GMT
CMD ["eswrapper"]
# Tue, 12 Aug 2025 08:18:47 GMT
USER 1000:0
```

-	Layers:
	-	`sha256:4b3ffd8ccb5201a0fc03585952effb4ed2d1ea5e704d2e7330212fb8b16c86a3`  
		Last Modified: Wed, 01 Oct 2025 15:21:59 GMT  
		Size: 29.7 MB (29723147 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8eedc5e1c3ce91a500785679f7f90d5247435f52c17fd423909e6ae5d67c6d76`  
		Last Modified: Thu, 09 Oct 2025 21:16:35 GMT  
		Size: 5.2 MB (5169363 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eac0410b67591b31d001bbd93d7a4409b4d1a4cac24e43ed479fe12486f8aee7`  
		Last Modified: Thu, 09 Oct 2025 21:16:34 GMT  
		Size: 3.5 KB (3525 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ec95c7b9d17c1b8a062624f91add3ea023974e1a003a7d87b03c41914856fa4`  
		Last Modified: Thu, 09 Oct 2025 22:21:05 GMT  
		Size: 642.4 MB (642446726 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a326011794f4a75a2019af424aee267e3d1ec8fcc963f6fb917ba6f3103a19d`  
		Last Modified: Thu, 09 Oct 2025 21:16:34 GMT  
		Size: 9.5 KB (9530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa69920a1697d903af8d41e34a80a0506861ed4847da2f4569de11ab65a2fa24`  
		Last Modified: Thu, 09 Oct 2025 21:16:35 GMT  
		Size: 1.7 KB (1714 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99ff1fe08893384d2aefc5847c5ca9ca2f1ac43ec7955756fbc8584d8109b85b`  
		Last Modified: Thu, 09 Oct 2025 21:16:35 GMT  
		Size: 163.9 KB (163937 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e68374f881a7f1652cbec1952ce6857922bb7ee75c3bce4650bf4c7934333e8c`  
		Last Modified: Thu, 09 Oct 2025 21:16:34 GMT  
		Size: 404.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56a354a31a8b6ec04877bb50c204f73e1abd18e2c7221b59fbe1c7585eff52ae`  
		Last Modified: Thu, 09 Oct 2025 21:16:34 GMT  
		Size: 115.5 KB (115539 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elasticsearch:8.17.10` - unknown; unknown

```console
$ docker pull elasticsearch@sha256:3b30e2d55fabc28cbd8a943d737ff639832214c22825b806ebfd12db351c6c41
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3203181 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e52fbdb5fb9d1dc2e03a8adb14eaa7b6529776e574e5bdfa876b884abceac2a1`

```dockerfile
```

-	Layers:
	-	`sha256:6978f8d3c3cd5c2628639f5a3ef3be449fe7266dc819a7d50962f92da45849f6`  
		Last Modified: Fri, 10 Oct 2025 00:25:22 GMT  
		Size: 3.2 MB (3164785 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cea96f205ed5c7b692517853cec0743486c0a8fd8c8ed5cf40daf945df77a90f`  
		Last Modified: Fri, 10 Oct 2025 00:25:23 GMT  
		Size: 38.4 KB (38396 bytes)  
		MIME: application/vnd.in-toto+json

### `elasticsearch:8.17.10` - linux; arm64 variant v8

```console
$ docker pull elasticsearch@sha256:301047b72827de2cbfa8aaa61c8110589a66ecd5189b9822a4fdd9854bb3a64b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **521.8 MB (521840101 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a6808b6a8087edbfcaf4256aa8999a03aa96d3414c84c224c904ab1d2f21183`
-	Entrypoint: `["\/bin\/tini","--","\/usr\/local\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["eswrapper"]`

```dockerfile
# Tue, 12 Aug 2025 08:18:47 GMT
ARG RELEASE
# Tue, 12 Aug 2025 08:18:47 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 12 Aug 2025 08:18:47 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 12 Aug 2025 08:18:47 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 12 Aug 2025 08:18:47 GMT
ADD file:d77dea5c49828eb0de89439d2b631bc8ea27cb9ef774412b56a060ba1673487b in / 
# Tue, 12 Aug 2025 08:18:47 GMT
CMD ["/bin/bash"]
# Tue, 12 Aug 2025 08:18:47 GMT
RUN yes no | dpkg-reconfigure dash &&     for iter in 1 2 3 4 5 6 7 8 9 10; do       export DEBIAN_FRONTEND=noninteractive &&       apt-get update &&       apt-get upgrade -y &&       apt-get install -y --no-install-recommends         ca-certificates curl netcat-openbsd p11-kit unzip zip  &&       apt-get clean &&       rm -rf /var/lib/apt/lists/* &&       exit_code=0 && break ||         exit_code=$? && echo "apt-get error: retry $iter in 10s" && sleep 10;     done;     exit $exit_code # buildkit
# Tue, 12 Aug 2025 08:18:47 GMT
RUN userdel -r ubuntu &&     groupadd -g 1000 elasticsearch &&     useradd --uid 1000 --gid 1000 --home-dir /usr/share/elasticsearch --create-home elasticsearch &&     usermod -aG root elasticsearch &&     chown -R 0:0 /usr/share/elasticsearch # buildkit
# Tue, 12 Aug 2025 08:18:47 GMT
ENV ELASTIC_CONTAINER=true
# Tue, 12 Aug 2025 08:18:47 GMT
WORKDIR /usr/share/elasticsearch
# Tue, 12 Aug 2025 08:18:47 GMT
COPY --chown=0:0 /usr/share/elasticsearch /usr/share/elasticsearch # buildkit
# Tue, 12 Aug 2025 08:18:47 GMT
COPY --chown=0:0 /bin/tini /bin/tini # buildkit
# Tue, 12 Aug 2025 08:18:47 GMT
ENV PATH=/usr/share/elasticsearch/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 Aug 2025 08:18:47 GMT
ENV SHELL=/bin/bash
# Tue, 12 Aug 2025 08:18:47 GMT
COPY bin/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh # buildkit
# Tue, 12 Aug 2025 08:18:47 GMT
RUN chmod g=u /etc/passwd &&     chmod 0555 /usr/local/bin/docker-entrypoint.sh &&     find / -xdev -perm -4000 -exec chmod ug-s {} + &&     chmod 0775 /usr/share/elasticsearch &&     chown elasticsearch bin config config/jvm.options.d data logs plugins # buildkit
# Tue, 12 Aug 2025 08:18:47 GMT
COPY bin/docker-openjdk /etc/ca-certificates/update.d/docker-openjdk # buildkit
# Tue, 12 Aug 2025 08:18:47 GMT
RUN /etc/ca-certificates/update.d/docker-openjdk # buildkit
# Tue, 12 Aug 2025 08:18:47 GMT
EXPOSE map[9200/tcp:{} 9300/tcp:{}]
# Tue, 12 Aug 2025 08:18:47 GMT
LABEL org.label-schema.build-date=2025-08-08T08:36:52.872377389Z org.label-schema.license=Elastic-License-2.0 org.label-schema.name=Elasticsearch org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/elasticsearch org.label-schema.usage=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.label-schema.vcs-ref=e5c4b2af120c131ea2885730f6693cb7d40a0a63 org.label-schema.vcs-url=https://github.com/elastic/elasticsearch org.label-schema.vendor=Elastic org.label-schema.version=8.17.10 org.opencontainers.image.created=2025-08-08T08:36:52.872377389Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.opencontainers.image.licenses=Elastic-License-2.0 org.opencontainers.image.revision=e5c4b2af120c131ea2885730f6693cb7d40a0a63 org.opencontainers.image.source=https://github.com/elastic/elasticsearch org.opencontainers.image.title=Elasticsearch org.opencontainers.image.url=https://www.elastic.co/products/elasticsearch org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=8.17.10
# Tue, 12 Aug 2025 08:18:47 GMT
ENTRYPOINT ["/bin/tini" "--" "/usr/local/bin/docker-entrypoint.sh"]
# Tue, 12 Aug 2025 08:18:47 GMT
CMD ["eswrapper"]
# Tue, 12 Aug 2025 08:18:47 GMT
USER 1000:0
```

-	Layers:
	-	`sha256:b8a35db46e38ce87d4e743e1265ff436ed36e01d23246b24a1cbbeaae18ec432`  
		Last Modified: Wed, 01 Oct 2025 15:34:19 GMT  
		Size: 28.9 MB (28861712 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc4a249a7653b5587deb526cfe163703315e82a2477884b6ee4d649497881d92`  
		Last Modified: Thu, 09 Oct 2025 21:17:01 GMT  
		Size: 5.2 MB (5173535 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab7829c53b9093491ed333461e93ff042bd4ceec79d1270f05ad3f8e1b54ad22`  
		Last Modified: Thu, 09 Oct 2025 21:17:00 GMT  
		Size: 3.5 KB (3526 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de0bdd8547e9cdae2d4bc21012d2a5294bf0b338754041086672823404d1aafd`  
		Last Modified: Thu, 09 Oct 2025 22:21:26 GMT  
		Size: 487.5 MB (487514153 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95a26e596d9754063df41015d4f5f70edf1a0556a973ca07cbd0bf8ac56df822`  
		Last Modified: Thu, 09 Oct 2025 21:17:00 GMT  
		Size: 9.1 KB (9107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5964c90ba87dfa17e8179d9c3b10dd16bc7ce4111f3322eec3362beb3bd163dc`  
		Last Modified: Thu, 09 Oct 2025 21:17:00 GMT  
		Size: 1.7 KB (1719 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6fa40efa13908eb34e321cd26311b333c7b3e0398409f57e625f2f679edd4d9`  
		Last Modified: Thu, 09 Oct 2025 21:17:00 GMT  
		Size: 160.4 KB (160368 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b77f119afc8071954dbde3f8eb57af302ac8ba8bdfd41901c1649480473d2695`  
		Last Modified: Thu, 09 Oct 2025 21:16:59 GMT  
		Size: 406.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0ca87781420b3c7ff6852dd9992ef2c45a6ec7de48653c32c1ba1514de9430b`  
		Last Modified: Thu, 09 Oct 2025 21:16:59 GMT  
		Size: 115.5 KB (115543 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elasticsearch:8.17.10` - unknown; unknown

```console
$ docker pull elasticsearch@sha256:3b8a7d49f5dd9d678954aacb43d89c7e186349a8b8a31fdc23fad77954f03348
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3203167 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6262c755559bcce617ee1af54c89c4fc678c76916bc25357dfd18427540460ca`

```dockerfile
```

-	Layers:
	-	`sha256:36941e97114d8e2cb751f70644438afb1fbb024bb1282cb0bb76401a92d7b908`  
		Last Modified: Fri, 10 Oct 2025 00:25:34 GMT  
		Size: 3.2 MB (3164569 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d1d04cf5d33c60bfc36a2dbbc2e5b59b339e78af8e80672093907763a2411770`  
		Last Modified: Fri, 10 Oct 2025 00:25:38 GMT  
		Size: 38.6 KB (38598 bytes)  
		MIME: application/vnd.in-toto+json

## `elasticsearch:8.18.8`

```console
$ docker pull elasticsearch@sha256:98dbdba49c516867885cb84558b76f99f3c7463230b63cd9e1ac20d6f4b2daa7
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `elasticsearch:8.18.8` - linux; amd64

```console
$ docker pull elasticsearch@sha256:9dee3e296691806e6149f0b589a5367e2b12a3df1bb18395c278f0e5daf2d5c3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **700.1 MB (700095793 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a5b31487c6b3bcda2e3e9deac4d72541a87a7635ee3e57ef7d591394d93f06e2`
-	Entrypoint: `["\/bin\/tini","--","\/usr\/local\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["eswrapper"]`

```dockerfile
# Wed, 01 Oct 2025 13:01:35 GMT
ARG RELEASE
# Wed, 01 Oct 2025 13:01:35 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Oct 2025 13:01:35 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Oct 2025 13:01:35 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 01 Oct 2025 13:01:37 GMT
ADD file:249778a1782b02a1c2bcf9f292f5778d81442a53c3de1958d712f10baf7e0b60 in / 
# Wed, 01 Oct 2025 13:01:37 GMT
CMD ["/bin/bash"]
# Mon, 06 Oct 2025 13:08:19 GMT
RUN yes no | dpkg-reconfigure dash &&     for iter in 1 2 3 4 5 6 7 8 9 10; do       export DEBIAN_FRONTEND=noninteractive &&       apt-get update &&       apt-get upgrade -y &&       apt-get install -y --no-install-recommends         ca-certificates curl netcat-openbsd p11-kit unzip zip  &&       apt-get clean &&       rm -rf /var/lib/apt/lists/* &&       exit_code=0 && break ||         exit_code=$? && echo "apt-get error: retry $iter in 10s" && sleep 10;     done;     exit $exit_code # buildkit
# Mon, 06 Oct 2025 13:08:19 GMT
RUN userdel -r ubuntu &&     groupadd -g 1000 elasticsearch &&     useradd --uid 1000 --gid 1000 --home-dir /usr/share/elasticsearch --create-home elasticsearch &&     usermod -aG root elasticsearch &&     chown -R 0:0 /usr/share/elasticsearch # buildkit
# Mon, 06 Oct 2025 13:08:19 GMT
ENV ELASTIC_CONTAINER=true
# Mon, 06 Oct 2025 13:08:19 GMT
WORKDIR /usr/share/elasticsearch
# Mon, 06 Oct 2025 13:08:19 GMT
COPY --chown=0:0 /usr/share/elasticsearch /usr/share/elasticsearch # buildkit
# Mon, 06 Oct 2025 13:08:19 GMT
COPY --chown=0:0 /bin/tini /bin/tini # buildkit
# Mon, 06 Oct 2025 13:08:19 GMT
ENV PATH=/usr/share/elasticsearch/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 06 Oct 2025 13:08:19 GMT
ENV SHELL=/bin/bash
# Mon, 06 Oct 2025 13:08:19 GMT
COPY bin/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh # buildkit
# Mon, 06 Oct 2025 13:08:19 GMT
RUN chmod g=u /etc/passwd &&     chmod 0555 /usr/local/bin/docker-entrypoint.sh &&     find / -xdev -perm -4000 -exec chmod ug-s {} + &&     chmod 0775 /usr/share/elasticsearch &&     chown elasticsearch bin config config/jvm.options.d data logs plugins # buildkit
# Mon, 06 Oct 2025 13:08:19 GMT
COPY bin/docker-openjdk /etc/ca-certificates/update.d/docker-openjdk # buildkit
# Mon, 06 Oct 2025 13:08:19 GMT
RUN /etc/ca-certificates/update.d/docker-openjdk # buildkit
# Mon, 06 Oct 2025 13:08:19 GMT
EXPOSE map[9200/tcp:{} 9300/tcp:{}]
# Mon, 06 Oct 2025 13:08:19 GMT
LABEL org.label-schema.build-date=2025-10-02T22:10:40.225397673Z org.label-schema.license=Elastic-License-2.0 org.label-schema.name=Elasticsearch org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/elasticsearch org.label-schema.usage=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.label-schema.vcs-ref=c1310008a98b8bb63c9fc08e763de1d065b943ce org.label-schema.vcs-url=https://github.com/elastic/elasticsearch org.label-schema.vendor=Elastic org.label-schema.version=8.18.8 org.opencontainers.image.created=2025-10-02T22:10:40.225397673Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.opencontainers.image.licenses=Elastic-License-2.0 org.opencontainers.image.revision=c1310008a98b8bb63c9fc08e763de1d065b943ce org.opencontainers.image.source=https://github.com/elastic/elasticsearch org.opencontainers.image.title=Elasticsearch org.opencontainers.image.url=https://www.elastic.co/products/elasticsearch org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=8.18.8
# Mon, 06 Oct 2025 13:08:19 GMT
ENTRYPOINT ["/bin/tini" "--" "/usr/local/bin/docker-entrypoint.sh"]
# Mon, 06 Oct 2025 13:08:19 GMT
CMD ["eswrapper"]
# Mon, 06 Oct 2025 13:08:19 GMT
USER 1000:0
```

-	Layers:
	-	`sha256:4b3ffd8ccb5201a0fc03585952effb4ed2d1ea5e704d2e7330212fb8b16c86a3`  
		Last Modified: Wed, 01 Oct 2025 15:21:59 GMT  
		Size: 29.7 MB (29723147 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:767bd80aa3e96203f0fe79f488dd8396afad619772ad6b46f2f59b0aeb4350ef`  
		Last Modified: Thu, 09 Oct 2025 21:17:06 GMT  
		Size: 5.2 MB (5169275 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:413d463ed9d998440f2298dd041dc6706696a68b5f937c0667f2921f9b4906de`  
		Last Modified: Thu, 09 Oct 2025 21:17:06 GMT  
		Size: 3.5 KB (3529 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a745141e1b7bddf3289f47905d3e9a3f5b12a17fb66d65b19231248de43b0569`  
		Last Modified: Fri, 10 Oct 2025 00:58:53 GMT  
		Size: 664.9 MB (664908705 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2e1dcaa020bc80cf995518d3214281296dddb6929ca630b8206d8914a3673a8`  
		Last Modified: Thu, 09 Oct 2025 21:17:07 GMT  
		Size: 9.5 KB (9531 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6659622c6ac5a6460d61c66362194945f73c57beeb0d863bd57cb5587ea8c690`  
		Last Modified: Thu, 09 Oct 2025 21:17:07 GMT  
		Size: 1.7 KB (1713 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4cc353993c24183bc2b158391bb553e2378953cc21fa6fac53fd839d9c15648`  
		Last Modified: Thu, 09 Oct 2025 21:17:07 GMT  
		Size: 163.9 KB (163927 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6576d73f85dd503c1bbd02bcb5f4a6acd790d30e09225478a512d94be59b7636`  
		Last Modified: Thu, 09 Oct 2025 21:17:07 GMT  
		Size: 407.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b84906a5d7244c4d424537bacc7565af37af9134b64fa31b6f66b706bdef0474`  
		Last Modified: Thu, 09 Oct 2025 21:17:08 GMT  
		Size: 115.5 KB (115527 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elasticsearch:8.18.8` - unknown; unknown

```console
$ docker pull elasticsearch@sha256:583fb33b37f59aa1b7b7a523bd5de66ea81c83ed073164346a887c8c2871f707
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3231333 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d4d7cc6550158ddc5755d7835c522726b0e042129f197cb1ebfc1ba32fc596e`

```dockerfile
```

-	Layers:
	-	`sha256:a5b7e4e2c571c6e004ee3da3f479c33e7e3f78d3f612f3fc6483c3397c83a75f`  
		Last Modified: Fri, 10 Oct 2025 00:25:46 GMT  
		Size: 3.2 MB (3192944 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:88015e54603339551d580163f662e7a661b3e35c73e50083e1dc1dd5f7c658d9`  
		Last Modified: Fri, 10 Oct 2025 00:25:53 GMT  
		Size: 38.4 KB (38389 bytes)  
		MIME: application/vnd.in-toto+json

### `elasticsearch:8.18.8` - linux; arm64 variant v8

```console
$ docker pull elasticsearch@sha256:35bdb3b7836e25bd668c422e87f3b5c6e61a4e5bc5bfa3e35cea48b1336a9564
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **542.3 MB (542329268 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2663e44d51c2133b258684ab42178ee8d6f884ace46b523662b5189892c9a8e2`
-	Entrypoint: `["\/bin\/tini","--","\/usr\/local\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["eswrapper"]`

```dockerfile
# Wed, 01 Oct 2025 13:01:38 GMT
ARG RELEASE
# Wed, 01 Oct 2025 13:01:38 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Oct 2025 13:01:38 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Oct 2025 13:01:38 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 01 Oct 2025 13:01:40 GMT
ADD file:d77dea5c49828eb0de89439d2b631bc8ea27cb9ef774412b56a060ba1673487b in / 
# Wed, 01 Oct 2025 13:01:40 GMT
CMD ["/bin/bash"]
# Mon, 06 Oct 2025 13:08:19 GMT
RUN yes no | dpkg-reconfigure dash &&     for iter in 1 2 3 4 5 6 7 8 9 10; do       export DEBIAN_FRONTEND=noninteractive &&       apt-get update &&       apt-get upgrade -y &&       apt-get install -y --no-install-recommends         ca-certificates curl netcat-openbsd p11-kit unzip zip  &&       apt-get clean &&       rm -rf /var/lib/apt/lists/* &&       exit_code=0 && break ||         exit_code=$? && echo "apt-get error: retry $iter in 10s" && sleep 10;     done;     exit $exit_code # buildkit
# Mon, 06 Oct 2025 13:08:19 GMT
RUN userdel -r ubuntu &&     groupadd -g 1000 elasticsearch &&     useradd --uid 1000 --gid 1000 --home-dir /usr/share/elasticsearch --create-home elasticsearch &&     usermod -aG root elasticsearch &&     chown -R 0:0 /usr/share/elasticsearch # buildkit
# Mon, 06 Oct 2025 13:08:19 GMT
ENV ELASTIC_CONTAINER=true
# Mon, 06 Oct 2025 13:08:19 GMT
WORKDIR /usr/share/elasticsearch
# Mon, 06 Oct 2025 13:08:19 GMT
COPY --chown=0:0 /usr/share/elasticsearch /usr/share/elasticsearch # buildkit
# Mon, 06 Oct 2025 13:08:19 GMT
COPY --chown=0:0 /bin/tini /bin/tini # buildkit
# Mon, 06 Oct 2025 13:08:19 GMT
ENV PATH=/usr/share/elasticsearch/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 06 Oct 2025 13:08:19 GMT
ENV SHELL=/bin/bash
# Mon, 06 Oct 2025 13:08:19 GMT
COPY bin/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh # buildkit
# Mon, 06 Oct 2025 13:08:19 GMT
RUN chmod g=u /etc/passwd &&     chmod 0555 /usr/local/bin/docker-entrypoint.sh &&     find / -xdev -perm -4000 -exec chmod ug-s {} + &&     chmod 0775 /usr/share/elasticsearch &&     chown elasticsearch bin config config/jvm.options.d data logs plugins # buildkit
# Mon, 06 Oct 2025 13:08:19 GMT
COPY bin/docker-openjdk /etc/ca-certificates/update.d/docker-openjdk # buildkit
# Mon, 06 Oct 2025 13:08:19 GMT
RUN /etc/ca-certificates/update.d/docker-openjdk # buildkit
# Mon, 06 Oct 2025 13:08:19 GMT
EXPOSE map[9200/tcp:{} 9300/tcp:{}]
# Mon, 06 Oct 2025 13:08:19 GMT
LABEL org.label-schema.build-date=2025-10-02T22:10:40.225397673Z org.label-schema.license=Elastic-License-2.0 org.label-schema.name=Elasticsearch org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/elasticsearch org.label-schema.usage=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.label-schema.vcs-ref=c1310008a98b8bb63c9fc08e763de1d065b943ce org.label-schema.vcs-url=https://github.com/elastic/elasticsearch org.label-schema.vendor=Elastic org.label-schema.version=8.18.8 org.opencontainers.image.created=2025-10-02T22:10:40.225397673Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.opencontainers.image.licenses=Elastic-License-2.0 org.opencontainers.image.revision=c1310008a98b8bb63c9fc08e763de1d065b943ce org.opencontainers.image.source=https://github.com/elastic/elasticsearch org.opencontainers.image.title=Elasticsearch org.opencontainers.image.url=https://www.elastic.co/products/elasticsearch org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=8.18.8
# Mon, 06 Oct 2025 13:08:19 GMT
ENTRYPOINT ["/bin/tini" "--" "/usr/local/bin/docker-entrypoint.sh"]
# Mon, 06 Oct 2025 13:08:19 GMT
CMD ["eswrapper"]
# Mon, 06 Oct 2025 13:08:19 GMT
USER 1000:0
```

-	Layers:
	-	`sha256:b8a35db46e38ce87d4e743e1265ff436ed36e01d23246b24a1cbbeaae18ec432`  
		Last Modified: Wed, 01 Oct 2025 15:34:19 GMT  
		Size: 28.9 MB (28861712 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eef09c9af7481b35edf6c79b749e5f32d66919be2df62c77b9d90ddfda2b67de`  
		Last Modified: Thu, 09 Oct 2025 21:17:03 GMT  
		Size: 5.2 MB (5173604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6eec3fe3c02a318a387136627999b3a1327565c99e6d20438b89208b98725ff8`  
		Last Modified: Thu, 09 Oct 2025 21:17:03 GMT  
		Size: 3.5 KB (3526 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6881f7c0dc53a9f3b85477480345b9dce6127f66c59720a4d206c3e4b1959360`  
		Last Modified: Fri, 10 Oct 2025 01:16:47 GMT  
		Size: 508.0 MB (508003268 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c9098ffdd1b75a43ae8bbdcfbc3bd3003384d5322e0464f126290caf7d972f1`  
		Last Modified: Thu, 09 Oct 2025 21:17:03 GMT  
		Size: 9.1 KB (9104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89a2b1c461b627fd7a78b1c49d049d02155d709a82c15270ffb0e42eae8ceb2d`  
		Last Modified: Thu, 09 Oct 2025 21:17:04 GMT  
		Size: 1.7 KB (1716 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d58c48aab091ac2fdd7f5f4f63a99ba3781b599d1e7761454a4afa3b8a049973`  
		Last Modified: Thu, 09 Oct 2025 21:17:04 GMT  
		Size: 160.4 KB (160367 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6d43e898705ce7b24c4412c1c6dd23d1cff776abb7598064a573f43d117debf`  
		Last Modified: Thu, 09 Oct 2025 21:17:04 GMT  
		Size: 407.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7151da738860448b3c3e863cda2e9fec24c419402b4f7d7ddb3ba5c06649b9c9`  
		Last Modified: Thu, 09 Oct 2025 21:17:04 GMT  
		Size: 115.5 KB (115532 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elasticsearch:8.18.8` - unknown; unknown

```console
$ docker pull elasticsearch@sha256:2e1d46a717081e636329861de64e76e863aec337d28d634e2663d2a4434840b8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3231949 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:70295bea9f3cbfe16c5de9ea3bdcca065c06314fd6d4ef438534f798e74a9b53`

```dockerfile
```

-	Layers:
	-	`sha256:f3ccee60d218ed20c68b9d8411293a6af10e03a3ef4322442a5d3501118ceec7`  
		Last Modified: Fri, 10 Oct 2025 00:25:58 GMT  
		Size: 3.2 MB (3193357 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cce7ed71d275f6b2092e7ed56697075dd3a23708d8877fca11917a5a4b1c912f`  
		Last Modified: Fri, 10 Oct 2025 00:26:00 GMT  
		Size: 38.6 KB (38592 bytes)  
		MIME: application/vnd.in-toto+json

## `elasticsearch:8.19.5`

```console
$ docker pull elasticsearch@sha256:767258226c972b46c0c22817c16a9d7f40a90f67ec71fdc33f3c831c8eecdd6e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `elasticsearch:8.19.5` - linux; amd64

```console
$ docker pull elasticsearch@sha256:7a159fec8fc8a7b15ae74dcc01f418b39147a93ae097236774fec0b23e40364a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **707.0 MB (707023537 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:734c26a7355716887bc6085c66f47a2a1c4872962240934e977fb761732e8f62`
-	Entrypoint: `["\/bin\/tini","--","\/usr\/local\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["eswrapper"]`

```dockerfile
# Wed, 01 Oct 2025 13:01:35 GMT
ARG RELEASE
# Wed, 01 Oct 2025 13:01:35 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Oct 2025 13:01:35 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Oct 2025 13:01:35 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 01 Oct 2025 13:01:37 GMT
ADD file:249778a1782b02a1c2bcf9f292f5778d81442a53c3de1958d712f10baf7e0b60 in / 
# Wed, 01 Oct 2025 13:01:37 GMT
CMD ["/bin/bash"]
# Mon, 06 Oct 2025 13:08:09 GMT
RUN yes no | dpkg-reconfigure dash && for iter in 1 2 3 4 5 6 7 8 9 10; do       export DEBIAN_FRONTEND=noninteractive &&       apt-get update &&       apt-get upgrade -y &&       apt-get install -y --no-install-recommends         ca-certificates curl netcat-openbsd p11-kit unzip zip  &&       apt-get clean &&       rm -rf /var/lib/apt/lists/* &&       exit_code=0 && break ||         exit_code=$? && echo "apt-get error: retry $iter in 10s" && sleep 10;     done;     exit $exit_code # buildkit
# Mon, 06 Oct 2025 13:08:09 GMT
RUN userdel -r ubuntu &&     groupadd -g 1000 elasticsearch &&     useradd --uid 1000 --gid 1000 --home-dir /usr/share/elasticsearch --create-home elasticsearch &&     usermod -aG root elasticsearch &&     chown -R 0:0 /usr/share/elasticsearch # buildkit
# Mon, 06 Oct 2025 13:08:09 GMT
ENV ELASTIC_CONTAINER=true
# Mon, 06 Oct 2025 13:08:09 GMT
WORKDIR /usr/share/elasticsearch
# Mon, 06 Oct 2025 13:08:09 GMT
COPY --chown=0:0 /usr/share/elasticsearch /usr/share/elasticsearch # buildkit
# Mon, 06 Oct 2025 13:08:09 GMT
COPY --chown=0:0 /bin/tini /bin/tini # buildkit
# Mon, 06 Oct 2025 13:08:09 GMT
ENV PATH=/usr/share/elasticsearch/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 06 Oct 2025 13:08:09 GMT
ENV SHELL=/bin/bash
# Mon, 06 Oct 2025 13:08:09 GMT
COPY bin/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh # buildkit
# Mon, 06 Oct 2025 13:08:09 GMT
RUN chmod g=u /etc/passwd &&     chmod 0555 /usr/local/bin/docker-entrypoint.sh &&     find / -xdev -perm -4000 -exec chmod ug-s {} + &&     chmod 0775 /usr/share/elasticsearch &&     chown elasticsearch bin config config/jvm.options.d data logs plugins # buildkit
# Mon, 06 Oct 2025 13:08:09 GMT
COPY bin/docker-openjdk /etc/ca-certificates/update.d/docker-openjdk # buildkit
# Mon, 06 Oct 2025 13:08:09 GMT
RUN /etc/ca-certificates/update.d/docker-openjdk # buildkit
# Mon, 06 Oct 2025 13:08:09 GMT
EXPOSE map[9200/tcp:{} 9300/tcp:{}]
# Mon, 06 Oct 2025 13:08:09 GMT
LABEL org.label-schema.build-date=2025-10-03T16:35:50.165700789Z org.label-schema.license=Elastic-License-2.0 org.label-schema.name=Elasticsearch org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/elasticsearch org.label-schema.usage=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.label-schema.vcs-ref=d6dd0417f05cd69706f4f103c69bbb8b7688db9c org.label-schema.vcs-url=https://github.com/elastic/elasticsearch org.label-schema.vendor=Elastic org.label-schema.version=8.19.5 org.opencontainers.image.created=2025-10-03T16:35:50.165700789Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.opencontainers.image.licenses=Elastic-License-2.0 org.opencontainers.image.revision=d6dd0417f05cd69706f4f103c69bbb8b7688db9c org.opencontainers.image.source=https://github.com/elastic/elasticsearch org.opencontainers.image.title=Elasticsearch org.opencontainers.image.url=https://www.elastic.co/products/elasticsearch org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=8.19.5
# Mon, 06 Oct 2025 13:08:09 GMT
ENTRYPOINT ["/bin/tini" "--" "/usr/local/bin/docker-entrypoint.sh"]
# Mon, 06 Oct 2025 13:08:09 GMT
CMD ["eswrapper"]
# Mon, 06 Oct 2025 13:08:09 GMT
USER 1000:0
```

-	Layers:
	-	`sha256:4b3ffd8ccb5201a0fc03585952effb4ed2d1ea5e704d2e7330212fb8b16c86a3`  
		Last Modified: Wed, 01 Oct 2025 15:21:59 GMT  
		Size: 29.7 MB (29723147 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3803a88497ce2e629a1c015338f5f597ec467258e80735485f1eeebda7a1d7c4`  
		Last Modified: Thu, 09 Oct 2025 21:17:07 GMT  
		Size: 5.2 MB (5169367 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8663db04811d3deb592099ef3d2b56fbce3ad165087c139ed336c256a88eff11`  
		Last Modified: Thu, 09 Oct 2025 21:17:05 GMT  
		Size: 3.5 KB (3529 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:673c6a0a1e25a4dfef0482cb6a3c1a80b4e4f33e5c1164a010ea291a40274054`  
		Last Modified: Fri, 10 Oct 2025 00:30:38 GMT  
		Size: 671.8 MB (671836349 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0452798322ea4ae6d8b1f82196774ec061db7e98e5ca393a0e99881878b2336`  
		Last Modified: Thu, 09 Oct 2025 21:17:06 GMT  
		Size: 9.5 KB (9532 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8caf7b774b384fc9e46b7b07dfd4d97be0557dd94cb91a1127f58cf48db4e9bd`  
		Last Modified: Thu, 09 Oct 2025 21:17:06 GMT  
		Size: 1.7 KB (1715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffc135fb520588e50189775d0866b4249ce346d89a20e58f7770f3fda9770525`  
		Last Modified: Thu, 09 Oct 2025 21:17:06 GMT  
		Size: 163.9 KB (163929 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb7ccadc2c6437725f88b03f3813fbfb3bfc04770a2c9529cdbfb575af8fb4a5`  
		Last Modified: Thu, 09 Oct 2025 21:17:06 GMT  
		Size: 406.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e85cdd953efd7a3b20ceea4ad617df41ff1e3787f738d41ebec08b3c92511c09`  
		Last Modified: Thu, 09 Oct 2025 21:17:06 GMT  
		Size: 115.5 KB (115531 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elasticsearch:8.19.5` - unknown; unknown

```console
$ docker pull elasticsearch@sha256:8ff8da34080e45565d1ec8ccfc99d277fe57f4f2dd0c1cdd24528041532404e6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3252032 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:39d0062d8aa020d5df60c2f803a83e7ee1c343d81513f9c6964349288a9ab5a5`

```dockerfile
```

-	Layers:
	-	`sha256:1539422c0fdb5892f2f1a6244a676ab5f392c828fe52ad1bdf37b89fda30dfe4`  
		Last Modified: Fri, 10 Oct 2025 00:25:41 GMT  
		Size: 3.2 MB (3215149 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7a72a419b5a148d81e96f835bd6b2b8c3bca2f916d076cbb3e168b1fd2cb937a`  
		Last Modified: Fri, 10 Oct 2025 00:25:44 GMT  
		Size: 36.9 KB (36883 bytes)  
		MIME: application/vnd.in-toto+json

### `elasticsearch:8.19.5` - linux; arm64 variant v8

```console
$ docker pull elasticsearch@sha256:3d2ea8c94d31c915af80fdcc0f54ed684d7c645365bfa37b5595c21dd314b2ca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **549.2 MB (549225686 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e9914136dd9f91f58de2b273f28a5c13cf9872815a43f87bc6abd4dd164da25`
-	Entrypoint: `["\/bin\/tini","--","\/usr\/local\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["eswrapper"]`

```dockerfile
# Wed, 01 Oct 2025 13:01:38 GMT
ARG RELEASE
# Wed, 01 Oct 2025 13:01:38 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Oct 2025 13:01:38 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Oct 2025 13:01:38 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 01 Oct 2025 13:01:40 GMT
ADD file:d77dea5c49828eb0de89439d2b631bc8ea27cb9ef774412b56a060ba1673487b in / 
# Wed, 01 Oct 2025 13:01:40 GMT
CMD ["/bin/bash"]
# Mon, 06 Oct 2025 13:08:09 GMT
RUN yes no | dpkg-reconfigure dash && for iter in 1 2 3 4 5 6 7 8 9 10; do       export DEBIAN_FRONTEND=noninteractive &&       apt-get update &&       apt-get upgrade -y &&       apt-get install -y --no-install-recommends         ca-certificates curl netcat-openbsd p11-kit unzip zip  &&       apt-get clean &&       rm -rf /var/lib/apt/lists/* &&       exit_code=0 && break ||         exit_code=$? && echo "apt-get error: retry $iter in 10s" && sleep 10;     done;     exit $exit_code # buildkit
# Mon, 06 Oct 2025 13:08:09 GMT
RUN userdel -r ubuntu &&     groupadd -g 1000 elasticsearch &&     useradd --uid 1000 --gid 1000 --home-dir /usr/share/elasticsearch --create-home elasticsearch &&     usermod -aG root elasticsearch &&     chown -R 0:0 /usr/share/elasticsearch # buildkit
# Mon, 06 Oct 2025 13:08:09 GMT
ENV ELASTIC_CONTAINER=true
# Mon, 06 Oct 2025 13:08:09 GMT
WORKDIR /usr/share/elasticsearch
# Mon, 06 Oct 2025 13:08:09 GMT
COPY --chown=0:0 /usr/share/elasticsearch /usr/share/elasticsearch # buildkit
# Mon, 06 Oct 2025 13:08:09 GMT
COPY --chown=0:0 /bin/tini /bin/tini # buildkit
# Mon, 06 Oct 2025 13:08:09 GMT
ENV PATH=/usr/share/elasticsearch/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 06 Oct 2025 13:08:09 GMT
ENV SHELL=/bin/bash
# Mon, 06 Oct 2025 13:08:09 GMT
COPY bin/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh # buildkit
# Mon, 06 Oct 2025 13:08:09 GMT
RUN chmod g=u /etc/passwd &&     chmod 0555 /usr/local/bin/docker-entrypoint.sh &&     find / -xdev -perm -4000 -exec chmod ug-s {} + &&     chmod 0775 /usr/share/elasticsearch &&     chown elasticsearch bin config config/jvm.options.d data logs plugins # buildkit
# Mon, 06 Oct 2025 13:08:09 GMT
COPY bin/docker-openjdk /etc/ca-certificates/update.d/docker-openjdk # buildkit
# Mon, 06 Oct 2025 13:08:09 GMT
RUN /etc/ca-certificates/update.d/docker-openjdk # buildkit
# Mon, 06 Oct 2025 13:08:09 GMT
EXPOSE map[9200/tcp:{} 9300/tcp:{}]
# Mon, 06 Oct 2025 13:08:09 GMT
LABEL org.label-schema.build-date=2025-10-03T16:35:50.165700789Z org.label-schema.license=Elastic-License-2.0 org.label-schema.name=Elasticsearch org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/elasticsearch org.label-schema.usage=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.label-schema.vcs-ref=d6dd0417f05cd69706f4f103c69bbb8b7688db9c org.label-schema.vcs-url=https://github.com/elastic/elasticsearch org.label-schema.vendor=Elastic org.label-schema.version=8.19.5 org.opencontainers.image.created=2025-10-03T16:35:50.165700789Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.opencontainers.image.licenses=Elastic-License-2.0 org.opencontainers.image.revision=d6dd0417f05cd69706f4f103c69bbb8b7688db9c org.opencontainers.image.source=https://github.com/elastic/elasticsearch org.opencontainers.image.title=Elasticsearch org.opencontainers.image.url=https://www.elastic.co/products/elasticsearch org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=8.19.5
# Mon, 06 Oct 2025 13:08:09 GMT
ENTRYPOINT ["/bin/tini" "--" "/usr/local/bin/docker-entrypoint.sh"]
# Mon, 06 Oct 2025 13:08:09 GMT
CMD ["eswrapper"]
# Mon, 06 Oct 2025 13:08:09 GMT
USER 1000:0
```

-	Layers:
	-	`sha256:b8a35db46e38ce87d4e743e1265ff436ed36e01d23246b24a1cbbeaae18ec432`  
		Last Modified: Wed, 01 Oct 2025 15:34:19 GMT  
		Size: 28.9 MB (28861712 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45843370130afd9fe4e249b277f4b10b40eba354043efdc5d31049f57fae96bb`  
		Last Modified: Thu, 09 Oct 2025 21:17:00 GMT  
		Size: 5.2 MB (5173621 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf193103b17779a8bfc4c2e6c3dd0a223b717a4477696de3639d01a2dbd56747`  
		Last Modified: Thu, 09 Oct 2025 21:16:59 GMT  
		Size: 3.5 KB (3527 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cae0c2c72ee876b9bfce0b6e9d08befa6121cfe4d9bfb74046ee71943b7b39d`  
		Last Modified: Fri, 10 Oct 2025 01:17:40 GMT  
		Size: 514.9 MB (514899682 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccbfa254799d31f0c900b546b734394206c9180986fd42e3b289c30b2810862e`  
		Last Modified: Thu, 09 Oct 2025 21:17:00 GMT  
		Size: 9.1 KB (9106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19832ad0ce37ec42514658bc4a88e1d8d899652c3bc22ac0542e9c024f6d120d`  
		Last Modified: Thu, 09 Oct 2025 21:17:00 GMT  
		Size: 1.7 KB (1716 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f8ba90958ecef650841d35bd9c15809d7583b55a480073b9ff86538b9b5f279`  
		Last Modified: Thu, 09 Oct 2025 21:17:00 GMT  
		Size: 160.4 KB (160356 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0683a9cc48eb5b35b86d522acfdbeb1837079688e910c244d0c35403a3d4833e`  
		Last Modified: Thu, 09 Oct 2025 21:16:59 GMT  
		Size: 406.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68b5ac8f6ba58c529b6d44d79ebae54050ed490c806120407bebc32f9693577a`  
		Last Modified: Thu, 09 Oct 2025 21:17:00 GMT  
		Size: 115.5 KB (115528 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elasticsearch:8.19.5` - unknown; unknown

```console
$ docker pull elasticsearch@sha256:bb9ec51b5e5f6ff4aeb21c28d412652e2910d942c8ffe7e83289fc8f79db549d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3252648 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:761b44faaec03c5d378e03a42a726bdf89f606e9fe7324c22ee0bc97b5bfcce2`

```dockerfile
```

-	Layers:
	-	`sha256:bd49d342a7a0dfc43ff2d31b99784c0ecdcd20fcf41700be67f0a89f34256eb8`  
		Last Modified: Fri, 10 Oct 2025 00:26:00 GMT  
		Size: 3.2 MB (3215562 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:18ad3d2df7c247c112ab91f366429adec6f9f3e44e4ae67be6a91bd985a3fe71`  
		Last Modified: Fri, 10 Oct 2025 00:26:06 GMT  
		Size: 37.1 KB (37086 bytes)  
		MIME: application/vnd.in-toto+json

## `elasticsearch:9.0.8`

```console
$ docker pull elasticsearch@sha256:10c1b6e8c7f1d67fd3f59ff58974d7f51a4e2ad5cbf5b6331944af1d84cb505e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `elasticsearch:9.0.8` - linux; amd64

```console
$ docker pull elasticsearch@sha256:e84f011a779b43eba0673bbdbb04142b74f1b52c95c9806ce7f977c3e876b129
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **711.5 MB (711487330 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b1629a74612aa2d8013691f36f2aff7b7abc5de5cc764ef989abbb1e56db0a4f`
-	Entrypoint: `["\/bin\/tini","--","\/usr\/local\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["eswrapper"]`

```dockerfile
# Thu, 18 Sep 2025 08:36:47 GMT
LABEL maintainer="Red Hat, Inc."
# Thu, 18 Sep 2025 08:36:47 GMT
LABEL vendor="Red Hat, Inc."
# Thu, 18 Sep 2025 08:36:47 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Thu, 18 Sep 2025 08:36:47 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.6"       distribution-scope="public"
# Thu, 18 Sep 2025 08:36:47 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Thu, 18 Sep 2025 08:36:47 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Thu, 18 Sep 2025 08:36:47 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 18 Sep 2025 08:36:47 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 18 Sep 2025 08:36:47 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Thu, 18 Sep 2025 08:36:47 GMT
LABEL io.openshift.expose-services=""
# Thu, 18 Sep 2025 08:36:47 GMT
LABEL io.openshift.tags="minimal rhel9"
# Thu, 18 Sep 2025 08:36:47 GMT
ENV container oci
# Thu, 18 Sep 2025 08:36:48 GMT
COPY dir:c341d431f712f164558c0a23b4ff14b886e2ce5a998d4c5baaaa381ffd7c3b00 in / 
# Thu, 18 Sep 2025 08:36:48 GMT
COPY file:b37d593713ee21ad52a4cd1424dc019a24f7966f85df0ac4b86d234302695328 in /etc/yum.repos.d/. 
# Thu, 18 Sep 2025 08:36:48 GMT
CMD ["/bin/bash"]
# Thu, 18 Sep 2025 08:36:49 GMT
COPY file:58cc94f5b3b2d60de2c77a6ed4b1797dcede502ccdb429a72e7a72d994235b3c in /usr/share/buildinfo/content-sets.json 
# Thu, 18 Sep 2025 08:36:49 GMT
COPY file:58cc94f5b3b2d60de2c77a6ed4b1797dcede502ccdb429a72e7a72d994235b3c in /root/buildinfo/content_manifests/content-sets.json 
# Thu, 18 Sep 2025 08:36:49 GMT
COPY file:097ec12a5c22da979b55e75443e50150904b478d4249b64b2431aae8901ea4d2 in /root/buildinfo/labels.json 
# Thu, 18 Sep 2025 08:36:49 GMT
LABEL "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="0c20ee48321f5d64135f6208d1332c0b032df6c3" "org.opencontainers.image.revision"="0c20ee48321f5d64135f6208d1332c0b032df6c3" "build-date"="2025-09-18T08:36:33Z" "release"="1758184547"
# Mon, 06 Oct 2025 11:09:04 GMT
RUN microdnf install --setopt=tsflags=nodocs -y     nc shadow-utils zip unzip findutils procps-ng &&     microdnf clean all # buildkit
# Mon, 06 Oct 2025 11:09:04 GMT
RUN groupadd -g 1000 elasticsearch &&     adduser -u 1000 -g 1000 -G 0 -d /usr/share/elasticsearch elasticsearch &&     chown -R 0:0 /usr/share/elasticsearch # buildkit
# Mon, 06 Oct 2025 11:09:04 GMT
ENV ELASTIC_CONTAINER=true
# Mon, 06 Oct 2025 11:09:04 GMT
COPY /bin/tini /bin/tini # buildkit
# Mon, 06 Oct 2025 11:09:04 GMT
WORKDIR /usr/share/elasticsearch
# Mon, 06 Oct 2025 11:09:04 GMT
COPY --chown=0:0 /usr/share/elasticsearch . # buildkit
# Mon, 06 Oct 2025 11:09:04 GMT
RUN ln -sf /etc/pki/ca-trust/extracted/java/cacerts jdk/lib/security/cacerts # buildkit
# Mon, 06 Oct 2025 11:09:04 GMT
ENV PATH=/usr/share/elasticsearch/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 06 Oct 2025 11:09:04 GMT
ENV SHELL=/bin/bash
# Mon, 06 Oct 2025 11:09:04 GMT
COPY --chmod=0555 bin/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh # buildkit
# Mon, 06 Oct 2025 11:09:04 GMT
RUN chmod g=u /etc/passwd &&     find / -xdev -perm -4000 -exec chmod ug-s {} + &&     chmod 0775 /usr/share/elasticsearch &&     chown elasticsearch bin config config/jvm.options.d data logs plugins # buildkit
# Mon, 06 Oct 2025 11:09:04 GMT
EXPOSE map[9200/tcp:{} 9300/tcp:{}]
# Mon, 06 Oct 2025 11:09:04 GMT
LABEL org.label-schema.build-date=2025-10-02T22:06:15.098088583Z org.label-schema.license=Elastic-License-2.0 org.label-schema.name=Elasticsearch org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/elasticsearch org.label-schema.usage=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.label-schema.vcs-ref=936f7cf370e0d7952bb71a98629284c3c0e0d00e org.label-schema.vcs-url=https://github.com/elastic/elasticsearch org.label-schema.vendor=Elastic org.label-schema.version=9.0.8 org.opencontainers.image.created=2025-10-02T22:06:15.098088583Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.opencontainers.image.licenses=Elastic-License-2.0 org.opencontainers.image.revision=936f7cf370e0d7952bb71a98629284c3c0e0d00e org.opencontainers.image.source=https://github.com/elastic/elasticsearch org.opencontainers.image.title=Elasticsearch org.opencontainers.image.url=https://www.elastic.co/products/elasticsearch org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=9.0.8
# Mon, 06 Oct 2025 11:09:04 GMT
LABEL name=Elasticsearch maintainer=infra@elastic.co vendor=Elastic version=9.0.8 release=1 summary=Elasticsearch description=You know, for search.
# Mon, 06 Oct 2025 11:09:04 GMT
RUN mkdir /licenses && ln LICENSE.txt /licenses/LICENSE # buildkit
# Mon, 06 Oct 2025 11:09:04 GMT
ENTRYPOINT ["/bin/tini" "--" "/usr/local/bin/docker-entrypoint.sh"]
# Mon, 06 Oct 2025 11:09:04 GMT
CMD ["eswrapper"]
# Mon, 06 Oct 2025 11:09:04 GMT
USER 1000:0
```

-	Layers:
	-	`sha256:9f4bff248214d12c7254dc3c25ef82bd14ff143e2a06d159f2a8cc1c9e6ef1fd`  
		Last Modified: Thu, 18 Sep 2025 15:30:42 GMT  
		Size: 39.6 MB (39648249 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0fc658d731fd5ecfa349d08a752957d755e5371316fc45fce407060e7fa304b`  
		Last Modified: Mon, 06 Oct 2025 20:38:08 GMT  
		Size: 4.3 MB (4282682 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58e98ba0d90869fd987fc1bd20dbba39bd537fa44b692521bf6e0e038bd9d775`  
		Last Modified: Mon, 06 Oct 2025 20:38:04 GMT  
		Size: 1.5 KB (1530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbdf885783cb360426460961f2b03c146d6408170cf1ad26cbcb0686806a111f`  
		Last Modified: Mon, 06 Oct 2025 20:38:03 GMT  
		Size: 9.5 KB (9533 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6ae56d1185f48fdd817d7abf6ccd77a0f8209e95ff72d16a42d0c33b0c3176e`  
		Last Modified: Mon, 06 Oct 2025 20:39:25 GMT  
		Size: 667.5 MB (667465874 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7dfdd52c490d1dbbf9206e55f3881b60eca71d1ff1142eb7f0392cc35673ad4`  
		Last Modified: Mon, 06 Oct 2025 20:38:04 GMT  
		Size: 270.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4fb5e8750d84389739533b1f68430b6cb120ed33471689c4095a1622e945f705`  
		Last Modified: Mon, 06 Oct 2025 20:38:04 GMT  
		Size: 1.7 KB (1719 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77918d87f5e152d8ee7f0b7f88f6052824fd1efb4edcc832caed9f5295bec869`  
		Last Modified: Mon, 06 Oct 2025 20:38:03 GMT  
		Size: 75.7 KB (75747 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77da23aa1bc99b0f1c9c47a9a0e7ec7d7fe69f438937b2a922af43cad395edd1`  
		Last Modified: Mon, 06 Oct 2025 20:38:04 GMT  
		Size: 1.7 KB (1694 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elasticsearch:9.0.8` - unknown; unknown

```console
$ docker pull elasticsearch@sha256:295b81d57aebf0cfc8533f4097d52caf27cdd8c610aa243ae370947d6492f6f1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2064714 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:94bfcd792f045a35bc2ddea20c57a4f89127d565eef641b07444510c27dba7b6`

```dockerfile
```

-	Layers:
	-	`sha256:70e50279ac8388599645acaa4ea0095c7d12f736a45458ce02f7f118c4e12171`  
		Last Modified: Mon, 06 Oct 2025 21:25:43 GMT  
		Size: 2.0 MB (2030875 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9fcc6bafd5ad96fa13000504697dcb735a26e89cee9dc8e05ffb1ef2d166cccb`  
		Last Modified: Mon, 06 Oct 2025 21:25:44 GMT  
		Size: 33.8 KB (33839 bytes)  
		MIME: application/vnd.in-toto+json

### `elasticsearch:9.0.8` - linux; arm64 variant v8

```console
$ docker pull elasticsearch@sha256:a97ebcf6c52a4de8ee9d7665a08f3e9de18ce00169b4a601f78b5e63de61ba24
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **549.8 MB (549844238 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2046b0f6e0bc2127f3bbcb37afda917898b314b78efd754eaee4b2470a955ceb`
-	Entrypoint: `["\/bin\/tini","--","\/usr\/local\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["eswrapper"]`

```dockerfile
# Thu, 18 Sep 2025 08:39:52 GMT
LABEL maintainer="Red Hat, Inc."
# Thu, 18 Sep 2025 08:39:52 GMT
LABEL vendor="Red Hat, Inc."
# Thu, 18 Sep 2025 08:39:52 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Thu, 18 Sep 2025 08:39:52 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.6"       distribution-scope="public"
# Thu, 18 Sep 2025 08:39:52 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Thu, 18 Sep 2025 08:39:52 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Thu, 18 Sep 2025 08:39:52 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 18 Sep 2025 08:39:52 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 18 Sep 2025 08:39:52 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Thu, 18 Sep 2025 08:39:52 GMT
LABEL io.openshift.expose-services=""
# Thu, 18 Sep 2025 08:39:52 GMT
LABEL io.openshift.tags="minimal rhel9"
# Thu, 18 Sep 2025 08:39:52 GMT
ENV container oci
# Thu, 18 Sep 2025 08:39:53 GMT
COPY dir:9f6ea5fd9a48598d911c3860918a4b145eb452cb81a81a77f69e1ed6481637df in / 
# Thu, 18 Sep 2025 08:39:53 GMT
COPY file:b37d593713ee21ad52a4cd1424dc019a24f7966f85df0ac4b86d234302695328 in /etc/yum.repos.d/. 
# Thu, 18 Sep 2025 08:39:53 GMT
CMD ["/bin/bash"]
# Thu, 18 Sep 2025 08:39:54 GMT
COPY file:0667e9d31385a24c3aef13f2dd9ab6a7b71b3dfcfef5127d3c1e2ea2c838e5cb in /usr/share/buildinfo/content-sets.json 
# Thu, 18 Sep 2025 08:39:54 GMT
COPY file:0667e9d31385a24c3aef13f2dd9ab6a7b71b3dfcfef5127d3c1e2ea2c838e5cb in /root/buildinfo/content_manifests/content-sets.json 
# Thu, 18 Sep 2025 08:39:54 GMT
COPY file:f5f06837bcbb5ebacc66d8764dd5ddb2c916d273cd4f80d9b8b34880aba3bbeb in /root/buildinfo/labels.json 
# Thu, 18 Sep 2025 08:39:54 GMT
LABEL "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="0c20ee48321f5d64135f6208d1332c0b032df6c3" "org.opencontainers.image.revision"="0c20ee48321f5d64135f6208d1332c0b032df6c3" "build-date"="2025-09-18T08:39:36Z" "release"="1758184547"
# Mon, 06 Oct 2025 11:09:04 GMT
RUN microdnf install --setopt=tsflags=nodocs -y     nc shadow-utils zip unzip findutils procps-ng &&     microdnf clean all # buildkit
# Mon, 06 Oct 2025 11:09:04 GMT
RUN groupadd -g 1000 elasticsearch &&     adduser -u 1000 -g 1000 -G 0 -d /usr/share/elasticsearch elasticsearch &&     chown -R 0:0 /usr/share/elasticsearch # buildkit
# Mon, 06 Oct 2025 11:09:04 GMT
ENV ELASTIC_CONTAINER=true
# Mon, 06 Oct 2025 11:09:04 GMT
COPY /bin/tini /bin/tini # buildkit
# Mon, 06 Oct 2025 11:09:04 GMT
WORKDIR /usr/share/elasticsearch
# Mon, 06 Oct 2025 11:09:04 GMT
COPY --chown=0:0 /usr/share/elasticsearch . # buildkit
# Mon, 06 Oct 2025 11:09:04 GMT
RUN ln -sf /etc/pki/ca-trust/extracted/java/cacerts jdk/lib/security/cacerts # buildkit
# Mon, 06 Oct 2025 11:09:04 GMT
ENV PATH=/usr/share/elasticsearch/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 06 Oct 2025 11:09:04 GMT
ENV SHELL=/bin/bash
# Mon, 06 Oct 2025 11:09:04 GMT
COPY --chmod=0555 bin/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh # buildkit
# Mon, 06 Oct 2025 11:09:04 GMT
RUN chmod g=u /etc/passwd &&     find / -xdev -perm -4000 -exec chmod ug-s {} + &&     chmod 0775 /usr/share/elasticsearch &&     chown elasticsearch bin config config/jvm.options.d data logs plugins # buildkit
# Mon, 06 Oct 2025 11:09:04 GMT
EXPOSE map[9200/tcp:{} 9300/tcp:{}]
# Mon, 06 Oct 2025 11:09:04 GMT
LABEL org.label-schema.build-date=2025-10-02T22:06:15.098088583Z org.label-schema.license=Elastic-License-2.0 org.label-schema.name=Elasticsearch org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/elasticsearch org.label-schema.usage=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.label-schema.vcs-ref=936f7cf370e0d7952bb71a98629284c3c0e0d00e org.label-schema.vcs-url=https://github.com/elastic/elasticsearch org.label-schema.vendor=Elastic org.label-schema.version=9.0.8 org.opencontainers.image.created=2025-10-02T22:06:15.098088583Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.opencontainers.image.licenses=Elastic-License-2.0 org.opencontainers.image.revision=936f7cf370e0d7952bb71a98629284c3c0e0d00e org.opencontainers.image.source=https://github.com/elastic/elasticsearch org.opencontainers.image.title=Elasticsearch org.opencontainers.image.url=https://www.elastic.co/products/elasticsearch org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=9.0.8
# Mon, 06 Oct 2025 11:09:04 GMT
LABEL name=Elasticsearch maintainer=infra@elastic.co vendor=Elastic version=9.0.8 release=1 summary=Elasticsearch description=You know, for search.
# Mon, 06 Oct 2025 11:09:04 GMT
RUN mkdir /licenses && ln LICENSE.txt /licenses/LICENSE # buildkit
# Mon, 06 Oct 2025 11:09:04 GMT
ENTRYPOINT ["/bin/tini" "--" "/usr/local/bin/docker-entrypoint.sh"]
# Mon, 06 Oct 2025 11:09:04 GMT
CMD ["eswrapper"]
# Mon, 06 Oct 2025 11:09:04 GMT
USER 1000:0
```

-	Layers:
	-	`sha256:a9f9218e937ae927e68fe68d00604365ddda1b238616443bc0a4b9e574067342`  
		Last Modified: Thu, 18 Sep 2025 15:44:52 GMT  
		Size: 37.9 MB (37900151 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e26d1d6c963b9bd5f5ec7369e0de0caf7b29cd13272492992164f34361fdc79`  
		Last Modified: Mon, 06 Oct 2025 20:37:04 GMT  
		Size: 4.3 MB (4290426 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32bb7ab32f844c3493d8595fa519d27e2759905c753c43d625f7dbc2b5e01dad`  
		Last Modified: Mon, 06 Oct 2025 20:37:04 GMT  
		Size: 1.5 KB (1530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1670271ac78b9194c208b0680b732b7cf4400d701f279fd29a48f734db91112c`  
		Last Modified: Mon, 06 Oct 2025 20:37:04 GMT  
		Size: 9.1 KB (9102 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31086c4e2e931ebd53aaec71d78aeec858fd600b710563e5a248b3dc9864be1f`  
		Last Modified: Mon, 06 Oct 2025 20:38:09 GMT  
		Size: 507.6 MB (507564674 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:351b6bb0c931e9a06d18b3faa24b10a463bcfa4a1d2d147f7996c6eca05bac48`  
		Last Modified: Mon, 06 Oct 2025 20:37:03 GMT  
		Size: 269.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0380e8037b6ee5492ab7984b984d7176c5d310a0c5f5d86e44eefc5096b758ad`  
		Last Modified: Mon, 06 Oct 2025 20:37:04 GMT  
		Size: 1.7 KB (1720 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b119279a9fbc40cd7f8ccce757892646c0b46d9e9474596e22013b43a173be3a`  
		Last Modified: Mon, 06 Oct 2025 20:37:03 GMT  
		Size: 74.6 KB (74640 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:000f69b721f915859e9127dd51e85d49bb983c13947c78996f6a30f6b4154c19`  
		Last Modified: Mon, 06 Oct 2025 20:37:03 GMT  
		Size: 1.7 KB (1694 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elasticsearch:9.0.8` - unknown; unknown

```console
$ docker pull elasticsearch@sha256:3e4d8ebfe7b26ad0dd79a855e46be6438a5fffb1bd4984d0aeb04529f25d9854
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2065460 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a5e34c55420388ac81d10bd0d093a0cdb3d586734867a8f464ce0ae2635dea01`

```dockerfile
```

-	Layers:
	-	`sha256:fd3586109919c368f6d4ae5b372f3679d16c5ac2316553d791a4b1d28b7d7c51`  
		Last Modified: Mon, 06 Oct 2025 21:25:48 GMT  
		Size: 2.0 MB (2031439 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3b557b1e6b2451fca6bef04836b29e49f4ea35da0cacf11865df1e3a4e23ffa6`  
		Last Modified: Mon, 06 Oct 2025 21:25:49 GMT  
		Size: 34.0 KB (34021 bytes)  
		MIME: application/vnd.in-toto+json

## `elasticsearch:9.1.5`

```console
$ docker pull elasticsearch@sha256:9dac882b67afe5161f8988a7ede0e9890145182af83e4e1d4d10631c2f66656f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `elasticsearch:9.1.5` - linux; amd64

```console
$ docker pull elasticsearch@sha256:48a0f013e919d797200acd3c5d7facb3d489c4614c2ab9d456f989cef76d2a6a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **726.5 MB (726504246 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c5900781248258881a2094b9c28c8b0606ebbcdb359f180210ca7ddf3a8e2205`
-	Entrypoint: `["\/bin\/tini","--","\/usr\/local\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["eswrapper"]`

```dockerfile
# Thu, 18 Sep 2025 08:36:47 GMT
LABEL maintainer="Red Hat, Inc."
# Thu, 18 Sep 2025 08:36:47 GMT
LABEL vendor="Red Hat, Inc."
# Thu, 18 Sep 2025 08:36:47 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Thu, 18 Sep 2025 08:36:47 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.6"       distribution-scope="public"
# Thu, 18 Sep 2025 08:36:47 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Thu, 18 Sep 2025 08:36:47 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Thu, 18 Sep 2025 08:36:47 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 18 Sep 2025 08:36:47 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 18 Sep 2025 08:36:47 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Thu, 18 Sep 2025 08:36:47 GMT
LABEL io.openshift.expose-services=""
# Thu, 18 Sep 2025 08:36:47 GMT
LABEL io.openshift.tags="minimal rhel9"
# Thu, 18 Sep 2025 08:36:47 GMT
ENV container oci
# Thu, 18 Sep 2025 08:36:48 GMT
COPY dir:c341d431f712f164558c0a23b4ff14b886e2ce5a998d4c5baaaa381ffd7c3b00 in / 
# Thu, 18 Sep 2025 08:36:48 GMT
COPY file:b37d593713ee21ad52a4cd1424dc019a24f7966f85df0ac4b86d234302695328 in /etc/yum.repos.d/. 
# Thu, 18 Sep 2025 08:36:48 GMT
CMD ["/bin/bash"]
# Thu, 18 Sep 2025 08:36:49 GMT
COPY file:58cc94f5b3b2d60de2c77a6ed4b1797dcede502ccdb429a72e7a72d994235b3c in /usr/share/buildinfo/content-sets.json 
# Thu, 18 Sep 2025 08:36:49 GMT
COPY file:58cc94f5b3b2d60de2c77a6ed4b1797dcede502ccdb429a72e7a72d994235b3c in /root/buildinfo/content_manifests/content-sets.json 
# Thu, 18 Sep 2025 08:36:49 GMT
COPY file:097ec12a5c22da979b55e75443e50150904b478d4249b64b2431aae8901ea4d2 in /root/buildinfo/labels.json 
# Thu, 18 Sep 2025 08:36:49 GMT
LABEL "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="0c20ee48321f5d64135f6208d1332c0b032df6c3" "org.opencontainers.image.revision"="0c20ee48321f5d64135f6208d1332c0b032df6c3" "build-date"="2025-09-18T08:36:33Z" "release"="1758184547"
# Mon, 06 Oct 2025 11:10:10 GMT
RUN microdnf install --setopt=tsflags=nodocs -y     nc shadow-utils zip unzip findutils procps-ng &&     microdnf clean all # buildkit
# Mon, 06 Oct 2025 11:10:10 GMT
RUN groupadd -g 1000 elasticsearch &&     adduser -u 1000 -g 1000 -G 0 -d /usr/share/elasticsearch elasticsearch &&     chown -R 0:0 /usr/share/elasticsearch # buildkit
# Mon, 06 Oct 2025 11:10:10 GMT
ENV ELASTIC_CONTAINER=true
# Mon, 06 Oct 2025 11:10:10 GMT
COPY /bin/tini /bin/tini # buildkit
# Mon, 06 Oct 2025 11:10:10 GMT
WORKDIR /usr/share/elasticsearch
# Mon, 06 Oct 2025 11:10:10 GMT
COPY --chown=0:0 /usr/share/elasticsearch . # buildkit
# Mon, 06 Oct 2025 11:10:10 GMT
RUN ln -sf /etc/pki/ca-trust/extracted/java/cacerts jdk/lib/security/cacerts # buildkit
# Mon, 06 Oct 2025 11:10:10 GMT
ENV PATH=/usr/share/elasticsearch/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 06 Oct 2025 11:10:10 GMT
ENV SHELL=/bin/bash
# Mon, 06 Oct 2025 11:10:10 GMT
COPY --chmod=0555 bin/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh # buildkit
# Mon, 06 Oct 2025 11:10:10 GMT
RUN chmod g=u /etc/passwd &&     find / -xdev -perm -4000 -exec chmod ug-s {} + &&     chmod 0775 /usr/share/elasticsearch &&     chown elasticsearch bin config config/jvm.options.d data logs plugins # buildkit
# Mon, 06 Oct 2025 11:10:10 GMT
EXPOSE map[9200/tcp:{} 9300/tcp:{}]
# Mon, 06 Oct 2025 11:10:10 GMT
LABEL org.label-schema.build-date=2025-10-02T22:07:12.966975992Z org.label-schema.license=Elastic-License-2.0 org.label-schema.name=Elasticsearch org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/elasticsearch org.label-schema.usage=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.label-schema.vcs-ref=90ee222e7e0136dd8ddbb34015538f3a00c129b7 org.label-schema.vcs-url=https://github.com/elastic/elasticsearch org.label-schema.vendor=Elastic org.label-schema.version=9.1.5 org.opencontainers.image.created=2025-10-02T22:07:12.966975992Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.opencontainers.image.licenses=Elastic-License-2.0 org.opencontainers.image.revision=90ee222e7e0136dd8ddbb34015538f3a00c129b7 org.opencontainers.image.source=https://github.com/elastic/elasticsearch org.opencontainers.image.title=Elasticsearch org.opencontainers.image.url=https://www.elastic.co/products/elasticsearch org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=9.1.5
# Mon, 06 Oct 2025 11:10:10 GMT
LABEL name=Elasticsearch maintainer=infra@elastic.co vendor=Elastic version=9.1.5 release=1 summary=Elasticsearch description=You know, for search.
# Mon, 06 Oct 2025 11:10:10 GMT
RUN mkdir /licenses && ln LICENSE.txt /licenses/LICENSE # buildkit
# Mon, 06 Oct 2025 11:10:10 GMT
ENTRYPOINT ["/bin/tini" "--" "/usr/local/bin/docker-entrypoint.sh"]
# Mon, 06 Oct 2025 11:10:10 GMT
CMD ["eswrapper"]
# Mon, 06 Oct 2025 11:10:10 GMT
USER 1000:0
```

-	Layers:
	-	`sha256:9f4bff248214d12c7254dc3c25ef82bd14ff143e2a06d159f2a8cc1c9e6ef1fd`  
		Last Modified: Thu, 18 Sep 2025 15:30:42 GMT  
		Size: 39.6 MB (39648249 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cfdea4eec579b41823ef978d3f5da47e9dae60b707384126cc1128dbd9764712`  
		Last Modified: Mon, 06 Oct 2025 20:38:12 GMT  
		Size: 4.3 MB (4282696 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0339edb92a604f6908fb6322b31e498f6172b261a97c08b1441730410462e247`  
		Last Modified: Mon, 06 Oct 2025 20:38:03 GMT  
		Size: 1.5 KB (1525 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d620359daf50e58cadd9cbd15f270ce60fb8a2381bb39f462e4c842ce39883d2`  
		Last Modified: Mon, 06 Oct 2025 20:38:03 GMT  
		Size: 9.5 KB (9533 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35ef9c90b6ad55b4b23a821436c7ba00f039e7ef485f07a606069e04cf0d848d`  
		Last Modified: Mon, 06 Oct 2025 21:01:48 GMT  
		Size: 682.5 MB (682482776 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2dc577f8ffce967e49c5b8119a0478b43b8522a46bc1bf5c3a044beca253f29`  
		Last Modified: Mon, 06 Oct 2025 20:38:03 GMT  
		Size: 272.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7778cc196d0768fadd4c1df8f6a18a89e4dbc10b08c4639d4538bdbff736621`  
		Last Modified: Mon, 06 Oct 2025 20:38:03 GMT  
		Size: 1.7 KB (1721 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:595f1c606af50b141c38bbed779a6a4b07dbb5d381f8dc3a998a73d1a2bb8879`  
		Last Modified: Mon, 06 Oct 2025 20:38:03 GMT  
		Size: 75.7 KB (75748 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48a6236f9f211860c4211fcdf347b1bf19b59f3ac63caf094d85a52e98e0e733`  
		Last Modified: Mon, 06 Oct 2025 20:38:03 GMT  
		Size: 1.7 KB (1694 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elasticsearch:9.1.5` - unknown; unknown

```console
$ docker pull elasticsearch@sha256:f2ddf67caf83745ac45816f17ef32ed403c9f111a27a350fbbafde2f7dcd0215
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2118209 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:980bb0289041640ddea3671e04049e3d11dc2679ee45b90bafc998663bb34806`

```dockerfile
```

-	Layers:
	-	`sha256:bbfe038b5ba7f3f48dc79f1a8855f2d4b9e5d9a1cd68fd62e02c94613a1603bc`  
		Last Modified: Mon, 06 Oct 2025 21:25:49 GMT  
		Size: 2.1 MB (2084370 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f7ed610b47be9e80dee8a67fc83588f1d459ef89e13c372e1089d2f0b57b307e`  
		Last Modified: Mon, 06 Oct 2025 21:25:50 GMT  
		Size: 33.8 KB (33839 bytes)  
		MIME: application/vnd.in-toto+json

### `elasticsearch:9.1.5` - linux; arm64 variant v8

```console
$ docker pull elasticsearch@sha256:994b0df97532976bcb792ab9471c0971bb7ee3f8e84cb9e203820c4f5b0cead8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **564.9 MB (564853172 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b1c9f1d7872553d47050dece25ccb6675a48aff433e33a2744f376cee65f4fea`
-	Entrypoint: `["\/bin\/tini","--","\/usr\/local\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["eswrapper"]`

```dockerfile
# Thu, 18 Sep 2025 08:39:52 GMT
LABEL maintainer="Red Hat, Inc."
# Thu, 18 Sep 2025 08:39:52 GMT
LABEL vendor="Red Hat, Inc."
# Thu, 18 Sep 2025 08:39:52 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Thu, 18 Sep 2025 08:39:52 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.6"       distribution-scope="public"
# Thu, 18 Sep 2025 08:39:52 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Thu, 18 Sep 2025 08:39:52 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Thu, 18 Sep 2025 08:39:52 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 18 Sep 2025 08:39:52 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 18 Sep 2025 08:39:52 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Thu, 18 Sep 2025 08:39:52 GMT
LABEL io.openshift.expose-services=""
# Thu, 18 Sep 2025 08:39:52 GMT
LABEL io.openshift.tags="minimal rhel9"
# Thu, 18 Sep 2025 08:39:52 GMT
ENV container oci
# Thu, 18 Sep 2025 08:39:53 GMT
COPY dir:9f6ea5fd9a48598d911c3860918a4b145eb452cb81a81a77f69e1ed6481637df in / 
# Thu, 18 Sep 2025 08:39:53 GMT
COPY file:b37d593713ee21ad52a4cd1424dc019a24f7966f85df0ac4b86d234302695328 in /etc/yum.repos.d/. 
# Thu, 18 Sep 2025 08:39:53 GMT
CMD ["/bin/bash"]
# Thu, 18 Sep 2025 08:39:54 GMT
COPY file:0667e9d31385a24c3aef13f2dd9ab6a7b71b3dfcfef5127d3c1e2ea2c838e5cb in /usr/share/buildinfo/content-sets.json 
# Thu, 18 Sep 2025 08:39:54 GMT
COPY file:0667e9d31385a24c3aef13f2dd9ab6a7b71b3dfcfef5127d3c1e2ea2c838e5cb in /root/buildinfo/content_manifests/content-sets.json 
# Thu, 18 Sep 2025 08:39:54 GMT
COPY file:f5f06837bcbb5ebacc66d8764dd5ddb2c916d273cd4f80d9b8b34880aba3bbeb in /root/buildinfo/labels.json 
# Thu, 18 Sep 2025 08:39:54 GMT
LABEL "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="0c20ee48321f5d64135f6208d1332c0b032df6c3" "org.opencontainers.image.revision"="0c20ee48321f5d64135f6208d1332c0b032df6c3" "build-date"="2025-09-18T08:39:36Z" "release"="1758184547"
# Mon, 06 Oct 2025 11:10:10 GMT
RUN microdnf install --setopt=tsflags=nodocs -y     nc shadow-utils zip unzip findutils procps-ng &&     microdnf clean all # buildkit
# Mon, 06 Oct 2025 11:10:10 GMT
RUN groupadd -g 1000 elasticsearch &&     adduser -u 1000 -g 1000 -G 0 -d /usr/share/elasticsearch elasticsearch &&     chown -R 0:0 /usr/share/elasticsearch # buildkit
# Mon, 06 Oct 2025 11:10:10 GMT
ENV ELASTIC_CONTAINER=true
# Mon, 06 Oct 2025 11:10:10 GMT
COPY /bin/tini /bin/tini # buildkit
# Mon, 06 Oct 2025 11:10:10 GMT
WORKDIR /usr/share/elasticsearch
# Mon, 06 Oct 2025 11:10:10 GMT
COPY --chown=0:0 /usr/share/elasticsearch . # buildkit
# Mon, 06 Oct 2025 11:10:10 GMT
RUN ln -sf /etc/pki/ca-trust/extracted/java/cacerts jdk/lib/security/cacerts # buildkit
# Mon, 06 Oct 2025 11:10:10 GMT
ENV PATH=/usr/share/elasticsearch/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 06 Oct 2025 11:10:10 GMT
ENV SHELL=/bin/bash
# Mon, 06 Oct 2025 11:10:10 GMT
COPY --chmod=0555 bin/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh # buildkit
# Mon, 06 Oct 2025 11:10:10 GMT
RUN chmod g=u /etc/passwd &&     find / -xdev -perm -4000 -exec chmod ug-s {} + &&     chmod 0775 /usr/share/elasticsearch &&     chown elasticsearch bin config config/jvm.options.d data logs plugins # buildkit
# Mon, 06 Oct 2025 11:10:10 GMT
EXPOSE map[9200/tcp:{} 9300/tcp:{}]
# Mon, 06 Oct 2025 11:10:10 GMT
LABEL org.label-schema.build-date=2025-10-02T22:07:12.966975992Z org.label-schema.license=Elastic-License-2.0 org.label-schema.name=Elasticsearch org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/elasticsearch org.label-schema.usage=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.label-schema.vcs-ref=90ee222e7e0136dd8ddbb34015538f3a00c129b7 org.label-schema.vcs-url=https://github.com/elastic/elasticsearch org.label-schema.vendor=Elastic org.label-schema.version=9.1.5 org.opencontainers.image.created=2025-10-02T22:07:12.966975992Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.opencontainers.image.licenses=Elastic-License-2.0 org.opencontainers.image.revision=90ee222e7e0136dd8ddbb34015538f3a00c129b7 org.opencontainers.image.source=https://github.com/elastic/elasticsearch org.opencontainers.image.title=Elasticsearch org.opencontainers.image.url=https://www.elastic.co/products/elasticsearch org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=9.1.5
# Mon, 06 Oct 2025 11:10:10 GMT
LABEL name=Elasticsearch maintainer=infra@elastic.co vendor=Elastic version=9.1.5 release=1 summary=Elasticsearch description=You know, for search.
# Mon, 06 Oct 2025 11:10:10 GMT
RUN mkdir /licenses && ln LICENSE.txt /licenses/LICENSE # buildkit
# Mon, 06 Oct 2025 11:10:10 GMT
ENTRYPOINT ["/bin/tini" "--" "/usr/local/bin/docker-entrypoint.sh"]
# Mon, 06 Oct 2025 11:10:10 GMT
CMD ["eswrapper"]
# Mon, 06 Oct 2025 11:10:10 GMT
USER 1000:0
```

-	Layers:
	-	`sha256:a9f9218e937ae927e68fe68d00604365ddda1b238616443bc0a4b9e574067342`  
		Last Modified: Thu, 18 Sep 2025 15:44:52 GMT  
		Size: 37.9 MB (37900151 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e19c1fd3d9b1295fdd3aa416ab6b1007024fdbdab2f681d7b4682d83b24c785a`  
		Last Modified: Mon, 06 Oct 2025 20:37:04 GMT  
		Size: 4.3 MB (4290407 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c50c99bb08a6f967e286e846adeea0081cf55f0bfa88953f59b002e55c37590`  
		Last Modified: Mon, 06 Oct 2025 20:37:03 GMT  
		Size: 1.5 KB (1532 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:365b2bbeca84ead5e03dabfd8f2c8464e6e45be63e0a5bf4e6efa95bf522d209`  
		Last Modified: Mon, 06 Oct 2025 20:37:03 GMT  
		Size: 9.1 KB (9103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cda9f340da037d629ace04734836c7b76ff8ad738c547811b30de9b07b04f7a8`  
		Last Modified: Mon, 06 Oct 2025 22:06:06 GMT  
		Size: 522.6 MB (522573629 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8965b34874474d405cb5d3be5d25c79ddd72395f9dec06562301ea799e70834b`  
		Last Modified: Mon, 06 Oct 2025 20:37:03 GMT  
		Size: 270.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63a0fc2739dd1190aa3d7762ca2f1b71b02da7bb0e44883cb9ba435b500e2122`  
		Last Modified: Mon, 06 Oct 2025 20:37:03 GMT  
		Size: 1.7 KB (1718 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1481df50a8806d47a5eddfba00fe03fa6efee6dc4c9666d7bc47fec4d6d068a7`  
		Last Modified: Mon, 06 Oct 2025 20:37:03 GMT  
		Size: 74.6 KB (74636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71e8f591acc134f6c243ba9ba1a440602530eedde77dcf6e2bdba81be90da17a`  
		Last Modified: Mon, 06 Oct 2025 20:37:04 GMT  
		Size: 1.7 KB (1694 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elasticsearch:9.1.5` - unknown; unknown

```console
$ docker pull elasticsearch@sha256:aef7ecd2705179a2a4d29f5bad9a0c0694b15f60444ca77d9c43905f944bad76
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2118955 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a1f0c43928aa3389c8de1389ba87a9d5b723c58b7866880324473adc4b62c917`

```dockerfile
```

-	Layers:
	-	`sha256:a257381b5fa69b96cc2ed3045c04c72fceb065a01158367fc324fd3d7ef2586d`  
		Last Modified: Mon, 06 Oct 2025 21:25:59 GMT  
		Size: 2.1 MB (2084934 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2e6c16a55591ae4b5099a665c159a4a05f100f28dbbffc8d628144543209ea0a`  
		Last Modified: Mon, 06 Oct 2025 21:26:00 GMT  
		Size: 34.0 KB (34021 bytes)  
		MIME: application/vnd.in-toto+json
