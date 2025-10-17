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
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
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
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
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
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
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
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
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
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
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
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
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
$ docker pull elasticsearch@sha256:577a16c5977a87be70fc49fef8f6f6271176fe62633e4594ad16381db55160f6
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `elasticsearch:9.0.8` - linux; amd64

```console
$ docker pull elasticsearch@sha256:5d73f8c2a5069acae6f73008bf1becd7d13f589b6cd5524dc5b4c5bfd4f42a35
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **711.5 MB (711492373 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a5aa192dd263fef0796d2c895335e7786c5d4f2493ea1e9b5d9f8e895f076c60`
-	Entrypoint: `["\/bin\/tini","--","\/usr\/local\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["eswrapper"]`

```dockerfile
# Mon, 06 Oct 2025 11:09:04 GMT
LABEL maintainer="Red Hat, Inc."
# Mon, 06 Oct 2025 11:09:04 GMT
LABEL vendor="Red Hat, Inc."
# Mon, 06 Oct 2025 11:09:04 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Mon, 06 Oct 2025 11:09:04 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.6"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Mon, 06 Oct 2025 11:09:04 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Mon, 06 Oct 2025 11:09:04 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Mon, 06 Oct 2025 11:09:04 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 06 Oct 2025 11:09:04 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 06 Oct 2025 11:09:04 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Mon, 06 Oct 2025 11:09:04 GMT
LABEL io.openshift.expose-services=""
# Mon, 06 Oct 2025 11:09:04 GMT
LABEL io.openshift.tags="minimal rhel9"
# Mon, 06 Oct 2025 11:09:04 GMT
ENV container oci
# Mon, 06 Oct 2025 11:09:04 GMT
COPY dir:f15650dcc2939ee0c30865212b61e6718fd6c24de4e7967bf7b651b8f0b24352 in /      
# Mon, 06 Oct 2025 11:09:04 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Mon, 06 Oct 2025 11:09:04 GMT
CMD ["/bin/bash"]
# Mon, 06 Oct 2025 11:09:04 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /usr/share/buildinfo/content-sets.json      
# Mon, 06 Oct 2025 11:09:04 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /root/buildinfo/content_manifests/content-sets.json      
# Mon, 06 Oct 2025 11:09:04 GMT
COPY file:16bf5aac480286f91e3031d4f1acb4e76fb8c3be38d180e4713a0efdc39d6bad in /root/buildinfo/labels.json      
# Mon, 06 Oct 2025 11:09:04 GMT
LABEL "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="d1b15a34ce69ea214e1d32f1f501304f6b8b8c59" "org.opencontainers.image.revision"="d1b15a34ce69ea214e1d32f1f501304f6b8b8c59" "build-date"="2025-10-15T08:06:12Z" "release"="1760515502"org.opencontainers.image.revision=d1b15a34ce69ea214e1d32f1f501304f6b8b8c59
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
	-	`sha256:2920d84eafa0cf94806ab58f0a2124f7b2d35bcbb06fc89a9106dcc28efe397a`  
		Last Modified: Wed, 15 Oct 2025 09:03:15 GMT  
		Size: 39.7 MB (39653524 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c96545f3f2c5d672bf6b409adbf6cea27802012917a1aaf3720b3d5f5a8a5b8`  
		Last Modified: Thu, 16 Oct 2025 19:29:29 GMT  
		Size: 4.3 MB (4282629 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46cf2eafddaf644d036b3be6a34356fb942999db097198352b8ecd19bbac2a2f`  
		Last Modified: Thu, 16 Oct 2025 19:29:29 GMT  
		Size: 1.5 KB (1526 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c358a591346b9e3b972abe3589cc06da4ebdd49dd7d596a71c3aca0b3b4bcfd6`  
		Last Modified: Thu, 16 Oct 2025 19:29:29 GMT  
		Size: 9.5 KB (9531 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:950d7fbfb11842c33455f46e8897b334a9a5f2984d042ae8b8e34aca7fe97431`  
		Last Modified: Thu, 16 Oct 2025 20:11:54 GMT  
		Size: 667.5 MB (667465702 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90cbb240da26e8e2d2968559c5754fd2cf5a985f4e92770349cb3b9d26cb9ebe`  
		Last Modified: Thu, 16 Oct 2025 19:29:29 GMT  
		Size: 270.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df1cea933e15f19aab5bc45f16f0d5504ac07f9d38df25266d813807bb301dc7`  
		Last Modified: Thu, 16 Oct 2025 19:29:29 GMT  
		Size: 1.7 KB (1720 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:405707ba23ee7100b96ec7697b3ba131f77b64c8d5e2fd55cb00df4d2ddb82c5`  
		Last Modified: Thu, 16 Oct 2025 19:29:29 GMT  
		Size: 75.7 KB (75746 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f255910490a4b2a64c2e946a7e722cf548366675aa2f22e4fd9a40a373a7035`  
		Last Modified: Thu, 16 Oct 2025 19:29:29 GMT  
		Size: 1.7 KB (1693 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elasticsearch:9.0.8` - unknown; unknown

```console
$ docker pull elasticsearch@sha256:9c276aa8c31ba789e073a54e92c77460e94afa21a45074c594a95bb8ac6ff16f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2064774 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1bf90fc39b6aa5e4f9c5d70951d3acfa12a6e3157f9a01c55b72d2eb0b1f38f4`

```dockerfile
```

-	Layers:
	-	`sha256:717a561d842330d729e1311ded57af65c7a5e5f4dd1b8a5363369e0c95b744a5`  
		Last Modified: Thu, 16 Oct 2025 21:25:22 GMT  
		Size: 2.0 MB (2030875 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e8899fb11650f90534c6886527b09d75add6547a6e876cfb91eef1808c7de306`  
		Last Modified: Thu, 16 Oct 2025 21:25:23 GMT  
		Size: 33.9 KB (33899 bytes)  
		MIME: application/vnd.in-toto+json

### `elasticsearch:9.0.8` - linux; arm64 variant v8

```console
$ docker pull elasticsearch@sha256:18c024f641892a765f1b89e5e3a1e56acbaa28425b729052b7555ea18a2d2844
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **549.8 MB (549840336 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe110352587eb0e9f71fe983e0773ec430cd42eb5b49ee12a74c43f71c542bf8`
-	Entrypoint: `["\/bin\/tini","--","\/usr\/local\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["eswrapper"]`

```dockerfile
# Mon, 06 Oct 2025 11:09:04 GMT
LABEL maintainer="Red Hat, Inc."
# Mon, 06 Oct 2025 11:09:04 GMT
LABEL vendor="Red Hat, Inc."
# Mon, 06 Oct 2025 11:09:04 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Mon, 06 Oct 2025 11:09:04 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.6"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Mon, 06 Oct 2025 11:09:04 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Mon, 06 Oct 2025 11:09:04 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Mon, 06 Oct 2025 11:09:04 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 06 Oct 2025 11:09:04 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 06 Oct 2025 11:09:04 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Mon, 06 Oct 2025 11:09:04 GMT
LABEL io.openshift.expose-services=""
# Mon, 06 Oct 2025 11:09:04 GMT
LABEL io.openshift.tags="minimal rhel9"
# Mon, 06 Oct 2025 11:09:04 GMT
ENV container oci
# Mon, 06 Oct 2025 11:09:04 GMT
COPY dir:a993e2e2ad3cf26c4ca4b583710869f381ee3e7df7d41715015a96348230e455 in /      
# Mon, 06 Oct 2025 11:09:04 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Mon, 06 Oct 2025 11:09:04 GMT
CMD ["/bin/bash"]
# Mon, 06 Oct 2025 11:09:04 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /usr/share/buildinfo/content-sets.json      
# Mon, 06 Oct 2025 11:09:04 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /root/buildinfo/content_manifests/content-sets.json      
# Mon, 06 Oct 2025 11:09:04 GMT
COPY file:85de04d2096a64069474160b53ad5f2cfb18b7e3f3ec2a8d26b3946f32e004c9 in /root/buildinfo/labels.json      
# Mon, 06 Oct 2025 11:09:04 GMT
LABEL "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="d1b15a34ce69ea214e1d32f1f501304f6b8b8c59" "org.opencontainers.image.revision"="d1b15a34ce69ea214e1d32f1f501304f6b8b8c59" "build-date"="2025-10-15T08:10:36Z" "release"="1760515502"org.opencontainers.image.revision=d1b15a34ce69ea214e1d32f1f501304f6b8b8c59
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
	-	`sha256:2602e1c5e8830fe80a6207359ce01e6c9b7d6848be663c4df1e03c724149b8a6`  
		Last Modified: Wed, 15 Oct 2025 09:30:32 GMT  
		Size: 37.9 MB (37896281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41683c36bc7e0dfa005b1238eb849a248429d9ade238479a539336bbbb1503cb`  
		Last Modified: Thu, 16 Oct 2025 19:29:14 GMT  
		Size: 4.3 MB (4290411 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7cce230e90d3842b475519028e8a2a6f44eb36843468bebb35b0bed099b62ee`  
		Last Modified: Thu, 16 Oct 2025 19:29:13 GMT  
		Size: 1.5 KB (1527 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd814ff094fff3c423b9a4df988cc6bc730723c9bbaa3f034a2d5eeaffab9a30`  
		Last Modified: Thu, 16 Oct 2025 19:29:14 GMT  
		Size: 9.1 KB (9101 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1a47e62089c8563c60fb102e6d9c475c5c692d015dd206284a543ce2641da19`  
		Last Modified: Thu, 16 Oct 2025 22:16:47 GMT  
		Size: 507.6 MB (507564668 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:490db02ee859f047a1991c5e8e727bfaa3c938e7440ed05e5f88ace2ca840982`  
		Last Modified: Thu, 16 Oct 2025 19:29:13 GMT  
		Size: 270.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5bf61666422d8ebb4bcb6b39e7bd93da4af68df5a2d1def52c8cf94f731cbe3`  
		Last Modified: Thu, 16 Oct 2025 19:29:14 GMT  
		Size: 1.7 KB (1717 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18d44ebf41d89c8e9056248db3a8dcc989f0327eb526b7f744a16b941550cb64`  
		Last Modified: Thu, 16 Oct 2025 19:29:13 GMT  
		Size: 74.6 KB (74637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed50ce58634af2e17252c2043088846a765e012f6579435b4a2a08c689b05add`  
		Last Modified: Thu, 16 Oct 2025 19:29:14 GMT  
		Size: 1.7 KB (1692 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elasticsearch:9.0.8` - unknown; unknown

```console
$ docker pull elasticsearch@sha256:23dc1a315f555e820926c1da20932cb82d8f5c1eb6e6d1ee69e0d931c6d8454c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2065520 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e3632b0937a6f96dfc829a92304a8058060ec8bba9ae1f94127f28d0fafcc96`

```dockerfile
```

-	Layers:
	-	`sha256:e16842128b2b1c27b6f3fe8ed2b7b82cc9c04f910606fc544c1298927c9747ab`  
		Last Modified: Thu, 16 Oct 2025 21:25:27 GMT  
		Size: 2.0 MB (2031439 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2a296f1bd5090c594df0f63688848a7bc403a251aa39f0666849a91986e4161c`  
		Last Modified: Thu, 16 Oct 2025 21:25:28 GMT  
		Size: 34.1 KB (34081 bytes)  
		MIME: application/vnd.in-toto+json

## `elasticsearch:9.1.5`

```console
$ docker pull elasticsearch@sha256:767e028f0bc761d4120487bf36613eecf484dbffd4e62240127e56928a5ef49c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `elasticsearch:9.1.5` - linux; amd64

```console
$ docker pull elasticsearch@sha256:2985ff980b99ac7d626fbb63a022ddc1b74cc56159d8f3596ca44e55f37ae526
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **726.5 MB (726509693 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e40cbaae3db07436b0a315f711fb33e772e4fa32ecdb43c733a79665f92cdf9`
-	Entrypoint: `["\/bin\/tini","--","\/usr\/local\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["eswrapper"]`

```dockerfile
# Mon, 06 Oct 2025 11:10:10 GMT
LABEL maintainer="Red Hat, Inc."
# Mon, 06 Oct 2025 11:10:10 GMT
LABEL vendor="Red Hat, Inc."
# Mon, 06 Oct 2025 11:10:10 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Mon, 06 Oct 2025 11:10:10 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.6"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Mon, 06 Oct 2025 11:10:10 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Mon, 06 Oct 2025 11:10:10 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Mon, 06 Oct 2025 11:10:10 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 06 Oct 2025 11:10:10 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 06 Oct 2025 11:10:10 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Mon, 06 Oct 2025 11:10:10 GMT
LABEL io.openshift.expose-services=""
# Mon, 06 Oct 2025 11:10:10 GMT
LABEL io.openshift.tags="minimal rhel9"
# Mon, 06 Oct 2025 11:10:10 GMT
ENV container oci
# Mon, 06 Oct 2025 11:10:10 GMT
COPY dir:f15650dcc2939ee0c30865212b61e6718fd6c24de4e7967bf7b651b8f0b24352 in /      
# Mon, 06 Oct 2025 11:10:10 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Mon, 06 Oct 2025 11:10:10 GMT
CMD ["/bin/bash"]
# Mon, 06 Oct 2025 11:10:10 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /usr/share/buildinfo/content-sets.json      
# Mon, 06 Oct 2025 11:10:10 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /root/buildinfo/content_manifests/content-sets.json      
# Mon, 06 Oct 2025 11:10:10 GMT
COPY file:16bf5aac480286f91e3031d4f1acb4e76fb8c3be38d180e4713a0efdc39d6bad in /root/buildinfo/labels.json      
# Mon, 06 Oct 2025 11:10:10 GMT
LABEL "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="d1b15a34ce69ea214e1d32f1f501304f6b8b8c59" "org.opencontainers.image.revision"="d1b15a34ce69ea214e1d32f1f501304f6b8b8c59" "build-date"="2025-10-15T08:06:12Z" "release"="1760515502"org.opencontainers.image.revision=d1b15a34ce69ea214e1d32f1f501304f6b8b8c59
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
	-	`sha256:2920d84eafa0cf94806ab58f0a2124f7b2d35bcbb06fc89a9106dcc28efe397a`  
		Last Modified: Wed, 15 Oct 2025 09:03:15 GMT  
		Size: 39.7 MB (39653524 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f4057bf76ca16d3f9282e67c31fdae9ecd506d2d4e38567e8874ff5a3216d77`  
		Last Modified: Thu, 16 Oct 2025 19:30:34 GMT  
		Size: 4.3 MB (4282623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a5d5a12748447a641b900191720ad36effdf0130c7f6da8586f7d92a39100cb`  
		Last Modified: Thu, 16 Oct 2025 19:30:34 GMT  
		Size: 1.5 KB (1527 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:992867b2cd9f9938e599eb44510dba8d1c85ad932196995d4af41071abb8c17c`  
		Last Modified: Thu, 16 Oct 2025 19:30:34 GMT  
		Size: 9.5 KB (9534 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80c24520339612bf82f07e806ad220b690df660cc33db586bc8dff3de47a0ac3`  
		Last Modified: Thu, 16 Oct 2025 21:31:10 GMT  
		Size: 682.5 MB (682483021 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8429217327449faa185892a38b77a0ba7580594252bbbb0571f7fae0fbb17a8c`  
		Last Modified: Thu, 16 Oct 2025 19:30:34 GMT  
		Size: 271.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30f3fed6cb85323d6c9a82efffb03d9a82bdb5785c4701bad9e55ede0893b980`  
		Last Modified: Thu, 16 Oct 2025 19:30:34 GMT  
		Size: 1.7 KB (1718 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ae03585b696a325b7f08ec490a8c643a8c537a2d792052b28224842a23ec630`  
		Last Modified: Thu, 16 Oct 2025 19:30:34 GMT  
		Size: 75.8 KB (75750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a81aa1621458475659b8df0b382589a57de6091ea0f7c887f54bae1d45e419d`  
		Last Modified: Thu, 16 Oct 2025 19:30:34 GMT  
		Size: 1.7 KB (1693 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elasticsearch:9.1.5` - unknown; unknown

```console
$ docker pull elasticsearch@sha256:0e58040d367d035537973fa22458ee6a2489b8adf8bf47936ff25c7b26d80954
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2118269 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:32cf1356126614711a1bded6762b9923c4403966444f765d95992a548d5101bb`

```dockerfile
```

-	Layers:
	-	`sha256:60f3b6c6a9a1d5d2b745864bbcbbed9726699cb24ee67a30a1853f4ed8ac125d`  
		Last Modified: Thu, 16 Oct 2025 21:25:32 GMT  
		Size: 2.1 MB (2084370 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5483480e98af0e6e55d7a5f14a12b92130d818f6a767ca791e904746c9d0823f`  
		Last Modified: Thu, 16 Oct 2025 21:25:33 GMT  
		Size: 33.9 KB (33899 bytes)  
		MIME: application/vnd.in-toto+json

### `elasticsearch:9.1.5` - linux; arm64 variant v8

```console
$ docker pull elasticsearch@sha256:dbedb0085f143b800878b7a13072d2b54bb97066ef0b91ab9f0c570b8fa81952
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **564.8 MB (564849310 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:99373aab45782ba671c3cb3cc098adcc6f0c6304e0477100e6d3ff2fecde8c65`
-	Entrypoint: `["\/bin\/tini","--","\/usr\/local\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["eswrapper"]`

```dockerfile
# Mon, 06 Oct 2025 11:10:10 GMT
LABEL maintainer="Red Hat, Inc."
# Mon, 06 Oct 2025 11:10:10 GMT
LABEL vendor="Red Hat, Inc."
# Mon, 06 Oct 2025 11:10:10 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Mon, 06 Oct 2025 11:10:10 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.6"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Mon, 06 Oct 2025 11:10:10 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Mon, 06 Oct 2025 11:10:10 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Mon, 06 Oct 2025 11:10:10 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 06 Oct 2025 11:10:10 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 06 Oct 2025 11:10:10 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Mon, 06 Oct 2025 11:10:10 GMT
LABEL io.openshift.expose-services=""
# Mon, 06 Oct 2025 11:10:10 GMT
LABEL io.openshift.tags="minimal rhel9"
# Mon, 06 Oct 2025 11:10:10 GMT
ENV container oci
# Mon, 06 Oct 2025 11:10:10 GMT
COPY dir:a993e2e2ad3cf26c4ca4b583710869f381ee3e7df7d41715015a96348230e455 in /      
# Mon, 06 Oct 2025 11:10:10 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Mon, 06 Oct 2025 11:10:10 GMT
CMD ["/bin/bash"]
# Mon, 06 Oct 2025 11:10:10 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /usr/share/buildinfo/content-sets.json      
# Mon, 06 Oct 2025 11:10:10 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /root/buildinfo/content_manifests/content-sets.json      
# Mon, 06 Oct 2025 11:10:10 GMT
COPY file:85de04d2096a64069474160b53ad5f2cfb18b7e3f3ec2a8d26b3946f32e004c9 in /root/buildinfo/labels.json      
# Mon, 06 Oct 2025 11:10:10 GMT
LABEL "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="d1b15a34ce69ea214e1d32f1f501304f6b8b8c59" "org.opencontainers.image.revision"="d1b15a34ce69ea214e1d32f1f501304f6b8b8c59" "build-date"="2025-10-15T08:10:36Z" "release"="1760515502"org.opencontainers.image.revision=d1b15a34ce69ea214e1d32f1f501304f6b8b8c59
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
	-	`sha256:2602e1c5e8830fe80a6207359ce01e6c9b7d6848be663c4df1e03c724149b8a6`  
		Last Modified: Wed, 15 Oct 2025 09:30:32 GMT  
		Size: 37.9 MB (37896281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:950756f6edb375289296422ee1bdbc92389710e99b755875dc35676b5a6a5934`  
		Last Modified: Thu, 16 Oct 2025 19:28:46 GMT  
		Size: 4.3 MB (4290421 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75f355c6d51457633b0ee5b22ba7046cc54aeb3956fd7a82fec5c57636262baa`  
		Last Modified: Thu, 16 Oct 2025 19:28:45 GMT  
		Size: 1.5 KB (1528 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21497217980cc8a9f43da4d22d8c67fcd66455e5e2203f45483fd4dd6fc4acac`  
		Last Modified: Thu, 16 Oct 2025 19:28:45 GMT  
		Size: 9.1 KB (9103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:369e249a4ac899e5455b1be6de65bbe55e019b05d434b6a14a22bad3cc62c6bf`  
		Last Modified: Thu, 16 Oct 2025 20:11:34 GMT  
		Size: 522.6 MB (522573627 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fd37369f0698c4f89cdfe0410a1ed4b52043b5eadd589255dc1ad5418b32749`  
		Last Modified: Thu, 16 Oct 2025 19:28:46 GMT  
		Size: 269.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4da8995bcbbd9a00bb31fb11385e1a79f2485497dfc9d74a874b4252f28edcf5`  
		Last Modified: Thu, 16 Oct 2025 19:28:46 GMT  
		Size: 1.7 KB (1719 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:309a42f92c72e1b59bfe7046a83001ca47b73c60afdac37ce9846eb7f4fc8c6a`  
		Last Modified: Thu, 16 Oct 2025 19:28:46 GMT  
		Size: 74.6 KB (74637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1462dcd72143755bbf5d8ad3d5a9f91a5840c5d391d40f66c196e59869520abf`  
		Last Modified: Thu, 16 Oct 2025 19:28:45 GMT  
		Size: 1.7 KB (1693 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elasticsearch:9.1.5` - unknown; unknown

```console
$ docker pull elasticsearch@sha256:1ab1c51ab44b97549df474a02fd2ae755ab0c1f3a2d62dbc1162ad126350a971
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2119015 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e79a5b2c30e873b9f1d69c10131bd9702fc3426276d9f1e5e591f55d35162815`

```dockerfile
```

-	Layers:
	-	`sha256:b66ea0ebc8b382de6a0837c6bc4def93f3572ee94f26b9ee0f7adbf26c31f1d2`  
		Last Modified: Thu, 16 Oct 2025 21:25:37 GMT  
		Size: 2.1 MB (2084934 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1a872a50f8f6b9b0459e02f9e555c65b9a0bc870dae780a346edc61bdf36b1fd`  
		Last Modified: Thu, 16 Oct 2025 21:25:38 GMT  
		Size: 34.1 KB (34081 bytes)  
		MIME: application/vnd.in-toto+json
