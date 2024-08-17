<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `elasticsearch`

-	[`elasticsearch:7.17.23`](#elasticsearch71723)
-	[`elasticsearch:8.15.0`](#elasticsearch8150)

## `elasticsearch:7.17.23`

```console
$ docker pull elasticsearch@sha256:a8a3291df2b687954a5e052c0b057270b11501ce5a64083a02599effe2b87c76
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `elasticsearch:7.17.23` - linux; amd64

```console
$ docker pull elasticsearch@sha256:beb8afe9be01c01bd5224cabe7a226825f75d56597cc583d58aad55cac36bfa8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **362.6 MB (362607517 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:15143b706164187198fd5b8c868997ab56e8a3ff4a6777778e9f1e0a5b472220`
-	Entrypoint: `["\/bin\/tini","--","\/usr\/local\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["eswrapper"]`

```dockerfile
# Tue, 30 Jul 2024 15:39:57 GMT
ARG RELEASE
# Tue, 30 Jul 2024 15:39:57 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 30 Jul 2024 15:39:57 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 30 Jul 2024 15:39:57 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 30 Jul 2024 15:39:57 GMT
ADD file:e7cff353f027ecf0a2cb1cdd51714de3b083a11a0d965f104489f9a7e6925056 in / 
# Tue, 30 Jul 2024 15:39:57 GMT
CMD ["/bin/bash"]
# Tue, 30 Jul 2024 15:39:57 GMT
RUN yes no | dpkg-reconfigure dash &&     for iter in 1 2 3 4 5 6 7 8 9 10; do       export DEBIAN_FRONTEND=noninteractive &&       apt-get update &&       apt-get upgrade -y &&       apt-get install -y --no-install-recommends         ca-certificates curl netcat p11-kit unzip zip &&       apt-get clean &&       rm -rf /var/lib/apt/lists/* &&       exit_code=0 && break ||         exit_code=$? && echo "apt-get error: retry $iter in 10s" && sleep 10;     done;     exit $exit_code # buildkit
# Tue, 30 Jul 2024 15:39:57 GMT
RUN groupadd -g 1000 elasticsearch &&     adduser --uid 1000 --gid 1000 --home /usr/share/elasticsearch elasticsearch &&     adduser elasticsearch root &&     chown -R 0:0 /usr/share/elasticsearch # buildkit
# Tue, 30 Jul 2024 15:39:57 GMT
ENV ELASTIC_CONTAINER=true
# Tue, 30 Jul 2024 15:39:57 GMT
WORKDIR /usr/share/elasticsearch
# Tue, 30 Jul 2024 15:39:57 GMT
COPY --chown=0:0 /usr/share/elasticsearch /usr/share/elasticsearch # buildkit
# Tue, 30 Jul 2024 15:39:57 GMT
COPY --chown=0:0 /bin/tini /bin/tini # buildkit
# Tue, 30 Jul 2024 15:39:57 GMT
ENV PATH=/usr/share/elasticsearch/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 30 Jul 2024 15:39:57 GMT
COPY bin/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh # buildkit
# Tue, 30 Jul 2024 15:39:57 GMT
RUN chmod g=u /etc/passwd &&     chmod 0555 /usr/local/bin/docker-entrypoint.sh &&     find / -xdev -perm -4000 -exec chmod ug-s {} + &&     chmod 0775 /usr/share/elasticsearch &&     chown elasticsearch bin config config/jvm.options.d data logs plugins # buildkit
# Tue, 30 Jul 2024 15:39:57 GMT
COPY bin/docker-openjdk /etc/ca-certificates/update.d/docker-openjdk # buildkit
# Tue, 30 Jul 2024 15:39:57 GMT
RUN /etc/ca-certificates/update.d/docker-openjdk # buildkit
# Tue, 30 Jul 2024 15:39:57 GMT
EXPOSE map[9200/tcp:{} 9300/tcp:{}]
# Tue, 30 Jul 2024 15:39:57 GMT
LABEL org.label-schema.build-date=2024-07-25T14:37:42.448799567Z org.label-schema.license=Elastic-License-2.0 org.label-schema.name=Elasticsearch org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/elasticsearch org.label-schema.usage=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.label-schema.vcs-ref=61d76462eecaf09ada684d1b5d319b5ff6865a83 org.label-schema.vcs-url=https://github.com/elastic/elasticsearch org.label-schema.vendor=Elastic org.label-schema.version=7.17.23 org.opencontainers.image.created=2024-07-25T14:37:42.448799567Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.opencontainers.image.licenses=Elastic-License-2.0 org.opencontainers.image.revision=61d76462eecaf09ada684d1b5d319b5ff6865a83 org.opencontainers.image.source=https://github.com/elastic/elasticsearch org.opencontainers.image.title=Elasticsearch org.opencontainers.image.url=https://www.elastic.co/products/elasticsearch org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=7.17.23
# Tue, 30 Jul 2024 15:39:57 GMT
ENTRYPOINT ["/bin/tini" "--" "/usr/local/bin/docker-entrypoint.sh"]
# Tue, 30 Jul 2024 15:39:57 GMT
CMD ["eswrapper"]
```

-	Layers:
	-	`sha256:602d8ad51b8130f3fcd71cb936dea612ebc799666136abf2e5914585b3178a4a`  
		Last Modified: Tue, 13 Aug 2024 10:23:50 GMT  
		Size: 27.5 MB (27511769 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b59231a43a77e78306015f62b6a6e6efb2cada0cb63fee5df70c504b19b82d07`  
		Last Modified: Sat, 17 Aug 2024 02:04:49 GMT  
		Size: 7.5 MB (7513981 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56333cf361ea326e65dd53ff9edb8080abcfcb330c07afc3f0aa98cf489864f2`  
		Last Modified: Sat, 17 Aug 2024 02:04:48 GMT  
		Size: 4.3 KB (4317 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2defd4684164a69d44c6d7260a1498796fb4e749a6318041df4fe3c98bf7e1b4`  
		Last Modified: Sat, 17 Aug 2024 02:04:53 GMT  
		Size: 327.3 MB (327264090 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39f942ce4afcd26f350b1962b0ac92e539a8047f169e16280ec19b199bbbffcd`  
		Last Modified: Sat, 17 Aug 2024 02:04:49 GMT  
		Size: 9.5 KB (9527 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5eea9b52cdf9d2e20275ce492e81c8442348797da72b233ab0848b1c9c176777`  
		Last Modified: Sat, 17 Aug 2024 02:04:49 GMT  
		Size: 2.0 KB (1976 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5417bfeb28508786da3895ccbeb643cf744b00db1b2a4d084be25a322aa7ca83`  
		Last Modified: Sat, 17 Aug 2024 02:04:49 GMT  
		Size: 192.2 KB (192170 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2f4a28e48c75c385fd87b7d1e4ea2b5c0b7512a0ef3903a16e4968468749a17`  
		Last Modified: Sat, 17 Aug 2024 02:04:50 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af110d8e6a3aa0143ce7f333bbedc74d98a9e0f1bb200eaef63d636fbb22269a`  
		Last Modified: Sat, 17 Aug 2024 02:04:50 GMT  
		Size: 109.3 KB (109252 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elasticsearch:7.17.23` - unknown; unknown

```console
$ docker pull elasticsearch@sha256:fd717c047a35363327a449674ce994b8fd6b572767744eb2ba967e32ea3b4820
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2404881 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:95dc7e2728bf551fd2637a998fb68f864d9733bde6d5f2b53d154b6c28570dbd`

```dockerfile
```

-	Layers:
	-	`sha256:a59d68ca77cebc0861e320af0dbabb46c7eb8cdc6ff3240aad804ef2a077db49`  
		Last Modified: Sat, 17 Aug 2024 02:04:48 GMT  
		Size: 2.4 MB (2367247 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c28f6464ea7ea3e877aa7c11851b13f87efbaf3d44ffb05907e55cee986216c3`  
		Last Modified: Sat, 17 Aug 2024 02:04:48 GMT  
		Size: 37.6 KB (37634 bytes)  
		MIME: application/vnd.in-toto+json

### `elasticsearch:7.17.23` - linux; arm64 variant v8

```console
$ docker pull elasticsearch@sha256:e48241da6a2af2d1640ab6a3b0581db5eec16546d8436451bc28211c4b5111d9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **358.5 MB (358540520 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5113bca13f4ff4f61c0a6da3bd93109b8d1f82147f9fa64f5c4ee0baa2baeb73`
-	Entrypoint: `["\/bin\/tini","--","\/usr\/local\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["eswrapper"]`

```dockerfile
# Tue, 30 Jul 2024 15:39:57 GMT
ARG RELEASE
# Tue, 30 Jul 2024 15:39:57 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 30 Jul 2024 15:39:57 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 30 Jul 2024 15:39:57 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 30 Jul 2024 15:39:57 GMT
ADD file:6d8cc056ee741f09a6c7d965d8e2027d80ed2eccbfb0312593ce52d9256db437 in / 
# Tue, 30 Jul 2024 15:39:57 GMT
CMD ["/bin/bash"]
# Tue, 30 Jul 2024 15:39:57 GMT
RUN yes no | dpkg-reconfigure dash &&     for iter in 1 2 3 4 5 6 7 8 9 10; do       export DEBIAN_FRONTEND=noninteractive &&       apt-get update &&       apt-get upgrade -y &&       apt-get install -y --no-install-recommends         ca-certificates curl netcat p11-kit unzip zip &&       apt-get clean &&       rm -rf /var/lib/apt/lists/* &&       exit_code=0 && break ||         exit_code=$? && echo "apt-get error: retry $iter in 10s" && sleep 10;     done;     exit $exit_code # buildkit
# Tue, 30 Jul 2024 15:39:57 GMT
RUN groupadd -g 1000 elasticsearch &&     adduser --uid 1000 --gid 1000 --home /usr/share/elasticsearch elasticsearch &&     adduser elasticsearch root &&     chown -R 0:0 /usr/share/elasticsearch # buildkit
# Tue, 30 Jul 2024 15:39:57 GMT
ENV ELASTIC_CONTAINER=true
# Tue, 30 Jul 2024 15:39:57 GMT
WORKDIR /usr/share/elasticsearch
# Tue, 30 Jul 2024 15:39:57 GMT
COPY --chown=0:0 /usr/share/elasticsearch /usr/share/elasticsearch # buildkit
# Tue, 30 Jul 2024 15:39:57 GMT
COPY --chown=0:0 /bin/tini /bin/tini # buildkit
# Tue, 30 Jul 2024 15:39:57 GMT
ENV PATH=/usr/share/elasticsearch/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 30 Jul 2024 15:39:57 GMT
COPY bin/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh # buildkit
# Tue, 30 Jul 2024 15:39:57 GMT
RUN chmod g=u /etc/passwd &&     chmod 0555 /usr/local/bin/docker-entrypoint.sh &&     find / -xdev -perm -4000 -exec chmod ug-s {} + &&     chmod 0775 /usr/share/elasticsearch &&     chown elasticsearch bin config config/jvm.options.d data logs plugins # buildkit
# Tue, 30 Jul 2024 15:39:57 GMT
COPY bin/docker-openjdk /etc/ca-certificates/update.d/docker-openjdk # buildkit
# Tue, 30 Jul 2024 15:39:57 GMT
RUN /etc/ca-certificates/update.d/docker-openjdk # buildkit
# Tue, 30 Jul 2024 15:39:57 GMT
EXPOSE map[9200/tcp:{} 9300/tcp:{}]
# Tue, 30 Jul 2024 15:39:57 GMT
LABEL org.label-schema.build-date=2024-07-25T14:37:42.448799567Z org.label-schema.license=Elastic-License-2.0 org.label-schema.name=Elasticsearch org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/elasticsearch org.label-schema.usage=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.label-schema.vcs-ref=61d76462eecaf09ada684d1b5d319b5ff6865a83 org.label-schema.vcs-url=https://github.com/elastic/elasticsearch org.label-schema.vendor=Elastic org.label-schema.version=7.17.23 org.opencontainers.image.created=2024-07-25T14:37:42.448799567Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.opencontainers.image.licenses=Elastic-License-2.0 org.opencontainers.image.revision=61d76462eecaf09ada684d1b5d319b5ff6865a83 org.opencontainers.image.source=https://github.com/elastic/elasticsearch org.opencontainers.image.title=Elasticsearch org.opencontainers.image.url=https://www.elastic.co/products/elasticsearch org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=7.17.23
# Tue, 30 Jul 2024 15:39:57 GMT
ENTRYPOINT ["/bin/tini" "--" "/usr/local/bin/docker-entrypoint.sh"]
# Tue, 30 Jul 2024 15:39:57 GMT
CMD ["eswrapper"]
```

-	Layers:
	-	`sha256:f02209be4ee528c246399de81af4552e52adb005a8a499815607b6b0d42746bf`  
		Last Modified: Mon, 03 Jun 2024 17:19:48 GMT  
		Size: 26.0 MB (25974217 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70727ca020b4a6002dd94720a78b314c1b8a2fdad77b50238d0bbb9f42f0ca8d`  
		Last Modified: Sat, 17 Aug 2024 02:18:16 GMT  
		Size: 7.3 MB (7333199 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3233432f82091206f8689656fa85be59c5e50961e2b45ec4b21b66207023571c`  
		Last Modified: Sat, 17 Aug 2024 02:18:16 GMT  
		Size: 4.3 KB (4316 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5d06c4734dd97ae9a32e72c3f33307ed875924bf08f2363b53089369d1ec076`  
		Last Modified: Sat, 17 Aug 2024 02:18:23 GMT  
		Size: 324.9 MB (324921840 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce01829020110beea02d7a83f77ad0de1b0863d0f43447a0676edd3d8056ee14`  
		Last Modified: Sat, 17 Aug 2024 02:18:16 GMT  
		Size: 9.1 KB (9097 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0931d89d9a773db0d2d36eb3869a3aeb9bacd246b50532663dce30a369b7b7a9`  
		Last Modified: Sat, 17 Aug 2024 02:18:17 GMT  
		Size: 2.0 KB (1979 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5daea7be30938d10040fe41639b9dd007321436000831c6aeba6013ce2004042`  
		Last Modified: Sat, 17 Aug 2024 02:18:17 GMT  
		Size: 186.2 KB (186183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23ccbf6583dd11e3d14de72b7b0f8aa71fc9be41aa4c9e53586273670cd5ab50`  
		Last Modified: Sat, 17 Aug 2024 02:18:17 GMT  
		Size: 402.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b1dcee05702e15fe29f73fd45efc3e8548aeaaaf7d4be2c426ce9556c11b5de`  
		Last Modified: Sat, 17 Aug 2024 02:18:18 GMT  
		Size: 109.3 KB (109255 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elasticsearch:7.17.23` - unknown; unknown

```console
$ docker pull elasticsearch@sha256:37c6680e210e7d259fd5683eeb080e014a8c9a1d37a9084a21fd9090bcb61f24
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2405378 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ed58c474658efa4dfd0a9bf0ce46ec59e2829d32c01d27912f94d716899609b`

```dockerfile
```

-	Layers:
	-	`sha256:42b3502eb590872764b059d84faa6a8250711ea3a587f10d25eee19e1846c86f`  
		Last Modified: Sat, 17 Aug 2024 02:18:16 GMT  
		Size: 2.4 MB (2367479 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cb9afc585d86a35a49f07f738e40ff6ba2aee139e24b79cc60c9e64308d66254`  
		Last Modified: Sat, 17 Aug 2024 02:18:16 GMT  
		Size: 37.9 KB (37899 bytes)  
		MIME: application/vnd.in-toto+json

## `elasticsearch:8.15.0`

```console
$ docker pull elasticsearch@sha256:310b9fc03b0657b0708c22b13cf3920f424c482a23f16a439d93c89636cb564c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `elasticsearch:8.15.0` - linux; amd64

```console
$ docker pull elasticsearch@sha256:c8f7d9e06b89dd28ff16f952bdfe08d9bb38cb2d0a1db1ac93076567433ad5c9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **647.1 MB (647099871 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a249dfc37cb54605ea82b608b8c9d7ab611bae1acffa982496c03b639de39415`
-	Entrypoint: `["\/bin\/tini","--","\/usr\/local\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["eswrapper"]`

```dockerfile
# Thu, 08 Aug 2024 13:05:51 GMT
ARG RELEASE
# Thu, 08 Aug 2024 13:05:51 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 08 Aug 2024 13:05:51 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 08 Aug 2024 13:05:51 GMT
LABEL org.opencontainers.image.version=20.04
# Thu, 08 Aug 2024 13:05:51 GMT
ADD file:e7cff353f027ecf0a2cb1cdd51714de3b083a11a0d965f104489f9a7e6925056 in / 
# Thu, 08 Aug 2024 13:05:51 GMT
CMD ["/bin/bash"]
# Thu, 08 Aug 2024 13:05:51 GMT
RUN yes no | dpkg-reconfigure dash &&     for iter in 1 2 3 4 5 6 7 8 9 10; do       export DEBIAN_FRONTEND=noninteractive &&       apt-get update &&       apt-get upgrade -y &&       apt-get install -y --no-install-recommends         ca-certificates curl netcat p11-kit unzip zip  &&       apt-get clean &&       rm -rf /var/lib/apt/lists/* &&       exit_code=0 && break ||         exit_code=$? && echo "apt-get error: retry $iter in 10s" && sleep 10;     done;     exit $exit_code # buildkit
# Thu, 08 Aug 2024 13:05:51 GMT
RUN groupadd -g 1000 elasticsearch &&     adduser --uid 1000 --gid 1000 --home /usr/share/elasticsearch elasticsearch &&     adduser elasticsearch root &&     chown -R 0:0 /usr/share/elasticsearch # buildkit
# Thu, 08 Aug 2024 13:05:51 GMT
ENV ELASTIC_CONTAINER=true
# Thu, 08 Aug 2024 13:05:51 GMT
WORKDIR /usr/share/elasticsearch
# Thu, 08 Aug 2024 13:05:51 GMT
COPY --chown=0:0 /usr/share/elasticsearch /usr/share/elasticsearch # buildkit
# Thu, 08 Aug 2024 13:05:51 GMT
COPY --chown=0:0 /bin/tini /bin/tini # buildkit
# Thu, 08 Aug 2024 13:05:51 GMT
ENV PATH=/usr/share/elasticsearch/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 08 Aug 2024 13:05:51 GMT
COPY bin/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh # buildkit
# Thu, 08 Aug 2024 13:05:51 GMT
RUN chmod g=u /etc/passwd &&     chmod 0555 /usr/local/bin/docker-entrypoint.sh &&     find / -xdev -perm -4000 -exec chmod ug-s {} + &&     chmod 0775 /usr/share/elasticsearch &&     chown elasticsearch bin config config/jvm.options.d data logs plugins # buildkit
# Thu, 08 Aug 2024 13:05:51 GMT
COPY bin/docker-openjdk /etc/ca-certificates/update.d/docker-openjdk # buildkit
# Thu, 08 Aug 2024 13:05:51 GMT
RUN /etc/ca-certificates/update.d/docker-openjdk # buildkit
# Thu, 08 Aug 2024 13:05:51 GMT
EXPOSE map[9200/tcp:{} 9300/tcp:{}]
# Thu, 08 Aug 2024 13:05:51 GMT
LABEL org.label-schema.build-date=2024-08-05T10:05:34.233336849Z org.label-schema.license=Elastic-License-2.0 org.label-schema.name=Elasticsearch org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/elasticsearch org.label-schema.usage=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.label-schema.vcs-ref=1a77947f34deddb41af25e6f0ddb8e830159c179 org.label-schema.vcs-url=https://github.com/elastic/elasticsearch org.label-schema.vendor=Elastic org.label-schema.version=8.15.0 org.opencontainers.image.created=2024-08-05T10:05:34.233336849Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.opencontainers.image.licenses=Elastic-License-2.0 org.opencontainers.image.revision=1a77947f34deddb41af25e6f0ddb8e830159c179 org.opencontainers.image.source=https://github.com/elastic/elasticsearch org.opencontainers.image.title=Elasticsearch org.opencontainers.image.url=https://www.elastic.co/products/elasticsearch org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=8.15.0
# Thu, 08 Aug 2024 13:05:51 GMT
ENTRYPOINT ["/bin/tini" "--" "/usr/local/bin/docker-entrypoint.sh"]
# Thu, 08 Aug 2024 13:05:51 GMT
CMD ["eswrapper"]
# Thu, 08 Aug 2024 13:05:51 GMT
USER 1000:0
```

-	Layers:
	-	`sha256:602d8ad51b8130f3fcd71cb936dea612ebc799666136abf2e5914585b3178a4a`  
		Last Modified: Tue, 13 Aug 2024 10:23:50 GMT  
		Size: 27.5 MB (27511769 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3303c12071cfd7675ee2f388e898c5946eaab5c050ab0b865a3686805ec57d83`  
		Last Modified: Sat, 17 Aug 2024 02:05:28 GMT  
		Size: 7.5 MB (7513906 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b6b73fc6b881bd1d8a87ad4e7118de7259a7a7aec03bc394efca29256638e94`  
		Last Modified: Sat, 17 Aug 2024 02:05:28 GMT  
		Size: 4.3 KB (4314 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:108a5a78cb68c5efa3cdc00df2b6747808faebf3407884ac321b29156c1b3915`  
		Last Modified: Sat, 17 Aug 2024 02:05:37 GMT  
		Size: 611.8 MB (611757051 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67723392e661b70d3ea1b9ee674960e6f5860d2c43ed98e3d041c7e9c0db1ec3`  
		Last Modified: Sat, 17 Aug 2024 02:05:28 GMT  
		Size: 9.5 KB (9527 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3dcabf294d31c933c378beb37d6d671d2087531cc8daaeb897e8474607358c93`  
		Last Modified: Sat, 17 Aug 2024 02:05:29 GMT  
		Size: 1.7 KB (1717 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d723b390f4823a260e756717c84f00f9905efe2b134994b6eb0d83e4ddd3bbd5`  
		Last Modified: Sat, 17 Aug 2024 02:05:29 GMT  
		Size: 191.9 KB (191900 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1435458a38ed256c4f2bafab8fa70d9377a650ba51444a3fe1c3d04bf4f8912`  
		Last Modified: Sat, 17 Aug 2024 02:05:29 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b9f55fe5055edbc747ec83aede1bb985fe76a9b365b081264d0a893256d56e5`  
		Last Modified: Sat, 17 Aug 2024 02:05:30 GMT  
		Size: 109.3 KB (109252 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elasticsearch:8.15.0` - unknown; unknown

```console
$ docker pull elasticsearch@sha256:53da9e07292958c45a3d24c2a0cf32dbf91008e05198b8d76f06732788580205
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2753145 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b064dee7b151569981a116e5929cd17a298f79601725491fde0c56f21e7c1e9`

```dockerfile
```

-	Layers:
	-	`sha256:7737d00b4ae3b80619277772631af91972b094aff7ae6f00776fb0034328c258`  
		Last Modified: Sat, 17 Aug 2024 02:05:28 GMT  
		Size: 2.7 MB (2715496 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:20605cdc08005fc9218ab7d2be8b2cf92210a1df4747af08688738031a35144b`  
		Last Modified: Sat, 17 Aug 2024 02:05:28 GMT  
		Size: 37.6 KB (37649 bytes)  
		MIME: application/vnd.in-toto+json

### `elasticsearch:8.15.0` - linux; arm64 variant v8

```console
$ docker pull elasticsearch@sha256:728fb6a55f3cb213fd96faeec24d054cd801db7ab59b0139c2b81a87c4100d7f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **491.2 MB (491202113 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e338ed85660bd5fe0a6f511f040b2b5a5f2c047e638889426c07291dab876d2`
-	Entrypoint: `["\/bin\/tini","--","\/usr\/local\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["eswrapper"]`

```dockerfile
# Thu, 08 Aug 2024 13:05:51 GMT
ARG RELEASE
# Thu, 08 Aug 2024 13:05:51 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 08 Aug 2024 13:05:51 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 08 Aug 2024 13:05:51 GMT
LABEL org.opencontainers.image.version=20.04
# Thu, 08 Aug 2024 13:05:51 GMT
ADD file:6d8cc056ee741f09a6c7d965d8e2027d80ed2eccbfb0312593ce52d9256db437 in / 
# Thu, 08 Aug 2024 13:05:51 GMT
CMD ["/bin/bash"]
# Thu, 08 Aug 2024 13:05:51 GMT
RUN yes no | dpkg-reconfigure dash &&     for iter in 1 2 3 4 5 6 7 8 9 10; do       export DEBIAN_FRONTEND=noninteractive &&       apt-get update &&       apt-get upgrade -y &&       apt-get install -y --no-install-recommends         ca-certificates curl netcat p11-kit unzip zip  &&       apt-get clean &&       rm -rf /var/lib/apt/lists/* &&       exit_code=0 && break ||         exit_code=$? && echo "apt-get error: retry $iter in 10s" && sleep 10;     done;     exit $exit_code # buildkit
# Thu, 08 Aug 2024 13:05:51 GMT
RUN groupadd -g 1000 elasticsearch &&     adduser --uid 1000 --gid 1000 --home /usr/share/elasticsearch elasticsearch &&     adduser elasticsearch root &&     chown -R 0:0 /usr/share/elasticsearch # buildkit
# Thu, 08 Aug 2024 13:05:51 GMT
ENV ELASTIC_CONTAINER=true
# Thu, 08 Aug 2024 13:05:51 GMT
WORKDIR /usr/share/elasticsearch
# Thu, 08 Aug 2024 13:05:51 GMT
COPY --chown=0:0 /usr/share/elasticsearch /usr/share/elasticsearch # buildkit
# Thu, 08 Aug 2024 13:05:51 GMT
COPY --chown=0:0 /bin/tini /bin/tini # buildkit
# Thu, 08 Aug 2024 13:05:51 GMT
ENV PATH=/usr/share/elasticsearch/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 08 Aug 2024 13:05:51 GMT
COPY bin/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh # buildkit
# Thu, 08 Aug 2024 13:05:51 GMT
RUN chmod g=u /etc/passwd &&     chmod 0555 /usr/local/bin/docker-entrypoint.sh &&     find / -xdev -perm -4000 -exec chmod ug-s {} + &&     chmod 0775 /usr/share/elasticsearch &&     chown elasticsearch bin config config/jvm.options.d data logs plugins # buildkit
# Thu, 08 Aug 2024 13:05:51 GMT
COPY bin/docker-openjdk /etc/ca-certificates/update.d/docker-openjdk # buildkit
# Thu, 08 Aug 2024 13:05:51 GMT
RUN /etc/ca-certificates/update.d/docker-openjdk # buildkit
# Thu, 08 Aug 2024 13:05:51 GMT
EXPOSE map[9200/tcp:{} 9300/tcp:{}]
# Thu, 08 Aug 2024 13:05:51 GMT
LABEL org.label-schema.build-date=2024-08-05T10:05:34.233336849Z org.label-schema.license=Elastic-License-2.0 org.label-schema.name=Elasticsearch org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/elasticsearch org.label-schema.usage=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.label-schema.vcs-ref=1a77947f34deddb41af25e6f0ddb8e830159c179 org.label-schema.vcs-url=https://github.com/elastic/elasticsearch org.label-schema.vendor=Elastic org.label-schema.version=8.15.0 org.opencontainers.image.created=2024-08-05T10:05:34.233336849Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.opencontainers.image.licenses=Elastic-License-2.0 org.opencontainers.image.revision=1a77947f34deddb41af25e6f0ddb8e830159c179 org.opencontainers.image.source=https://github.com/elastic/elasticsearch org.opencontainers.image.title=Elasticsearch org.opencontainers.image.url=https://www.elastic.co/products/elasticsearch org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=8.15.0
# Thu, 08 Aug 2024 13:05:51 GMT
ENTRYPOINT ["/bin/tini" "--" "/usr/local/bin/docker-entrypoint.sh"]
# Thu, 08 Aug 2024 13:05:51 GMT
CMD ["eswrapper"]
# Thu, 08 Aug 2024 13:05:51 GMT
USER 1000:0
```

-	Layers:
	-	`sha256:f02209be4ee528c246399de81af4552e52adb005a8a499815607b6b0d42746bf`  
		Last Modified: Mon, 03 Jun 2024 17:19:48 GMT  
		Size: 26.0 MB (25974217 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:170d61ad04e3e11176a3e82cedd5cff709c010408c47b4030a7dfdd6edae7b4e`  
		Last Modified: Sat, 17 Aug 2024 02:16:44 GMT  
		Size: 7.3 MB (7333143 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6b8bcace31ea0038c023ce3b62483ec3c8d1504fb589a6004cf09df522473af`  
		Last Modified: Sat, 17 Aug 2024 02:16:43 GMT  
		Size: 4.3 KB (4321 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7281e33dc3aea2526ce1d44fa07195fd965e1ff77e18abbba68d7ababeb03887`  
		Last Modified: Sat, 17 Aug 2024 02:16:53 GMT  
		Size: 457.6 MB (457584010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbb9ccc499b79aaaa53318de1ddb4ad055a8930d363443776dc711819eaa66e5`  
		Last Modified: Sat, 17 Aug 2024 02:16:43 GMT  
		Size: 9.1 KB (9097 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9a33b509c70f16bddb4e4598100b017afda668dd4540898ebbd1d450ddcb26b`  
		Last Modified: Sat, 17 Aug 2024 02:16:44 GMT  
		Size: 1.7 KB (1722 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d8332f3077c3c2a9095c937924f0e99d108c89d096d6dc9608926b0f756d127`  
		Last Modified: Sat, 17 Aug 2024 02:16:45 GMT  
		Size: 185.9 KB (185915 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe09928391430bfc65488c61262b76dd80718ebea1eecd58d0e977a5adf9d1b9`  
		Last Modified: Sat, 17 Aug 2024 02:16:45 GMT  
		Size: 406.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a124614c60a29a07eba3ead8780461e682f38d500d3e5aac0afbf1bb6b70aed3`  
		Last Modified: Sat, 17 Aug 2024 02:16:46 GMT  
		Size: 109.2 KB (109250 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elasticsearch:8.15.0` - unknown; unknown

```console
$ docker pull elasticsearch@sha256:16fffa1c8712bbf2c24a616bb60805826cad513fe7f21936456124ce598abb5f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2753643 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cbd744e8fd64635fd509761bc4169462238275cb67e680bf8f41cd8de825828d`

```dockerfile
```

-	Layers:
	-	`sha256:757ade56a7ebb006d3e11224e825780b88f27c31dbf5736980270e9640b79c9c`  
		Last Modified: Sat, 17 Aug 2024 02:16:44 GMT  
		Size: 2.7 MB (2715728 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6dc252cd12d653cd067b3b7112f403fe7175a3dd3f47a3a5eed75a6b0f00fccd`  
		Last Modified: Sat, 17 Aug 2024 02:16:43 GMT  
		Size: 37.9 KB (37915 bytes)  
		MIME: application/vnd.in-toto+json
