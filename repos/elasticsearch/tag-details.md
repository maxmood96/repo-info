<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `elasticsearch`

-	[`elasticsearch:7.17.23`](#elasticsearch71723)
-	[`elasticsearch:8.15.1`](#elasticsearch8151)

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

## `elasticsearch:8.15.1`

```console
$ docker pull elasticsearch@sha256:67068465d6fdfaffa9ae6854ca2f6d43cc1308b93e88d2410fb15590f9f659b9
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `elasticsearch:8.15.1` - linux; amd64

```console
$ docker pull elasticsearch@sha256:f84d8baaa9b942369ae10a004d461be8f4c0312b8e180c3c1c24843ff1811354
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **647.1 MB (647130258 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:93fbfc36e85a61b24b400f40614b56703d37a967e26eb7aed1a9a196cf3a2d57`
-	Entrypoint: `["\/bin\/tini","--","\/usr\/local\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["eswrapper"]`

```dockerfile
# Tue, 13 Aug 2024 09:26:46 GMT
ARG RELEASE
# Tue, 13 Aug 2024 09:26:46 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Aug 2024 09:26:46 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Aug 2024 09:26:46 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 13 Aug 2024 09:26:48 GMT
ADD file:e7cff353f027ecf0a2cb1cdd51714de3b083a11a0d965f104489f9a7e6925056 in / 
# Tue, 13 Aug 2024 09:26:48 GMT
CMD ["/bin/bash"]
# Thu, 05 Sep 2024 16:37:13 GMT
RUN yes no | dpkg-reconfigure dash &&     for iter in 1 2 3 4 5 6 7 8 9 10; do       export DEBIAN_FRONTEND=noninteractive &&       apt-get update &&       apt-get upgrade -y &&       apt-get install -y --no-install-recommends         ca-certificates curl netcat p11-kit unzip zip  &&       apt-get clean &&       rm -rf /var/lib/apt/lists/* &&       exit_code=0 && break ||         exit_code=$? && echo "apt-get error: retry $iter in 10s" && sleep 10;     done;     exit $exit_code # buildkit
# Thu, 05 Sep 2024 16:37:13 GMT
RUN groupadd -g 1000 elasticsearch &&     adduser --uid 1000 --gid 1000 --home /usr/share/elasticsearch elasticsearch &&     adduser elasticsearch root &&     chown -R 0:0 /usr/share/elasticsearch # buildkit
# Thu, 05 Sep 2024 16:37:13 GMT
ENV ELASTIC_CONTAINER=true
# Thu, 05 Sep 2024 16:37:13 GMT
WORKDIR /usr/share/elasticsearch
# Thu, 05 Sep 2024 16:37:13 GMT
COPY --chown=0:0 /usr/share/elasticsearch /usr/share/elasticsearch # buildkit
# Thu, 05 Sep 2024 16:37:13 GMT
COPY --chown=0:0 /bin/tini /bin/tini # buildkit
# Thu, 05 Sep 2024 16:37:13 GMT
ENV PATH=/usr/share/elasticsearch/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 05 Sep 2024 16:37:13 GMT
COPY bin/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh # buildkit
# Thu, 05 Sep 2024 16:37:13 GMT
RUN chmod g=u /etc/passwd &&     chmod 0555 /usr/local/bin/docker-entrypoint.sh &&     find / -xdev -perm -4000 -exec chmod ug-s {} + &&     chmod 0775 /usr/share/elasticsearch &&     chown elasticsearch bin config config/jvm.options.d data logs plugins # buildkit
# Thu, 05 Sep 2024 16:37:13 GMT
COPY bin/docker-openjdk /etc/ca-certificates/update.d/docker-openjdk # buildkit
# Thu, 05 Sep 2024 16:37:13 GMT
RUN /etc/ca-certificates/update.d/docker-openjdk # buildkit
# Thu, 05 Sep 2024 16:37:13 GMT
EXPOSE map[9200/tcp:{} 9300/tcp:{}]
# Thu, 05 Sep 2024 16:37:13 GMT
LABEL org.label-schema.build-date=2024-09-02T22:04:47.310170297Z org.label-schema.license=Elastic-License-2.0 org.label-schema.name=Elasticsearch org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/elasticsearch org.label-schema.usage=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.label-schema.vcs-ref=253e8544a65ad44581194068936f2a5d57c2c051 org.label-schema.vcs-url=https://github.com/elastic/elasticsearch org.label-schema.vendor=Elastic org.label-schema.version=8.15.1 org.opencontainers.image.created=2024-09-02T22:04:47.310170297Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.opencontainers.image.licenses=Elastic-License-2.0 org.opencontainers.image.revision=253e8544a65ad44581194068936f2a5d57c2c051 org.opencontainers.image.source=https://github.com/elastic/elasticsearch org.opencontainers.image.title=Elasticsearch org.opencontainers.image.url=https://www.elastic.co/products/elasticsearch org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=8.15.1
# Thu, 05 Sep 2024 16:37:13 GMT
ENTRYPOINT ["/bin/tini" "--" "/usr/local/bin/docker-entrypoint.sh"]
# Thu, 05 Sep 2024 16:37:13 GMT
CMD ["eswrapper"]
# Thu, 05 Sep 2024 16:37:13 GMT
USER 1000:0
```

-	Layers:
	-	`sha256:602d8ad51b8130f3fcd71cb936dea612ebc799666136abf2e5914585b3178a4a`  
		Last Modified: Tue, 13 Aug 2024 10:23:50 GMT  
		Size: 27.5 MB (27511769 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b95b60f66d56942c54cd13a9820f7dae1868a82bad472d84774d913bb742d73`  
		Last Modified: Thu, 05 Sep 2024 22:04:28 GMT  
		Size: 7.5 MB (7513902 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb3e6cafd3434d657ea43c621a583e76e69c46283ae860c94c13c9fd69128861`  
		Last Modified: Thu, 05 Sep 2024 22:04:27 GMT  
		Size: 4.3 KB (4313 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99828d28b577aaf1398455335d41c3429a43895a105313aa2b3cdc1acafccafb`  
		Last Modified: Thu, 05 Sep 2024 22:04:41 GMT  
		Size: 611.8 MB (611787428 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a77363ade226b31590902b25c00bd2cd6fb62de54c6956aea1ccbab5869b013`  
		Last Modified: Thu, 05 Sep 2024 22:04:27 GMT  
		Size: 9.5 KB (9529 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af69f436ae3345918d5cc89702c259358c76777979087784cd6b67781e4c6138`  
		Last Modified: Thu, 05 Sep 2024 22:04:28 GMT  
		Size: 1.7 KB (1723 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a59e81334a8e3ca4c5b89d70649558b20a8df799a2c8502ba12d6f75fa85379`  
		Last Modified: Thu, 05 Sep 2024 22:04:29 GMT  
		Size: 191.9 KB (191904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44d4c8544a10eaedb283ceb70c8109a1cdf8f872836e023c035dcec7f85bd16f`  
		Last Modified: Thu, 05 Sep 2024 22:04:29 GMT  
		Size: 406.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ae0a4f99837c56622610f90470967d09d8cd4fc41277cdd9e1da9d0843dd1e4`  
		Last Modified: Thu, 05 Sep 2024 22:04:29 GMT  
		Size: 109.3 KB (109252 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elasticsearch:8.15.1` - unknown; unknown

```console
$ docker pull elasticsearch@sha256:9bc86c5e305a123b5b0d7e2511d238cff9332da099b132fda94c40a8f48f1341
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2753146 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e6bc7fde9541eb89228e5123f360a08c5365a867fe56e1f982a064635f848b81`

```dockerfile
```

-	Layers:
	-	`sha256:72189e77bee3a90da2fbfa1d49df489de8f462a643c72087e113b8c5bcbcf950`  
		Last Modified: Thu, 05 Sep 2024 22:04:28 GMT  
		Size: 2.7 MB (2715496 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:75b5edce67e2fa451e40ec0797c07992e42ea192b100a2fe9440aa7757bd86c6`  
		Last Modified: Thu, 05 Sep 2024 22:04:27 GMT  
		Size: 37.6 KB (37650 bytes)  
		MIME: application/vnd.in-toto+json

### `elasticsearch:8.15.1` - linux; arm64 variant v8

```console
$ docker pull elasticsearch@sha256:26807d4b905098fe70fefe60f80ae2504d6b526d7ceeb00c72b757e8510fc839
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **491.2 MB (491227078 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a4408d0c0156dbb69eb873e666e9b9b12f2b7255f876102a550050947b5f9d7`
-	Entrypoint: `["\/bin\/tini","--","\/usr\/local\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["eswrapper"]`

```dockerfile
# Tue, 13 Aug 2024 09:27:56 GMT
ARG RELEASE
# Tue, 13 Aug 2024 09:27:56 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Aug 2024 09:27:56 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Aug 2024 09:27:56 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 13 Aug 2024 09:27:58 GMT
ADD file:6d8cc056ee741f09a6c7d965d8e2027d80ed2eccbfb0312593ce52d9256db437 in / 
# Tue, 13 Aug 2024 09:27:58 GMT
CMD ["/bin/bash"]
# Thu, 05 Sep 2024 16:37:13 GMT
RUN yes no | dpkg-reconfigure dash &&     for iter in 1 2 3 4 5 6 7 8 9 10; do       export DEBIAN_FRONTEND=noninteractive &&       apt-get update &&       apt-get upgrade -y &&       apt-get install -y --no-install-recommends         ca-certificates curl netcat p11-kit unzip zip  &&       apt-get clean &&       rm -rf /var/lib/apt/lists/* &&       exit_code=0 && break ||         exit_code=$? && echo "apt-get error: retry $iter in 10s" && sleep 10;     done;     exit $exit_code # buildkit
# Thu, 05 Sep 2024 16:37:13 GMT
RUN groupadd -g 1000 elasticsearch &&     adduser --uid 1000 --gid 1000 --home /usr/share/elasticsearch elasticsearch &&     adduser elasticsearch root &&     chown -R 0:0 /usr/share/elasticsearch # buildkit
# Thu, 05 Sep 2024 16:37:13 GMT
ENV ELASTIC_CONTAINER=true
# Thu, 05 Sep 2024 16:37:13 GMT
WORKDIR /usr/share/elasticsearch
# Thu, 05 Sep 2024 16:37:13 GMT
COPY --chown=0:0 /usr/share/elasticsearch /usr/share/elasticsearch # buildkit
# Thu, 05 Sep 2024 16:37:13 GMT
COPY --chown=0:0 /bin/tini /bin/tini # buildkit
# Thu, 05 Sep 2024 16:37:13 GMT
ENV PATH=/usr/share/elasticsearch/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 05 Sep 2024 16:37:13 GMT
COPY bin/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh # buildkit
# Thu, 05 Sep 2024 16:37:13 GMT
RUN chmod g=u /etc/passwd &&     chmod 0555 /usr/local/bin/docker-entrypoint.sh &&     find / -xdev -perm -4000 -exec chmod ug-s {} + &&     chmod 0775 /usr/share/elasticsearch &&     chown elasticsearch bin config config/jvm.options.d data logs plugins # buildkit
# Thu, 05 Sep 2024 16:37:13 GMT
COPY bin/docker-openjdk /etc/ca-certificates/update.d/docker-openjdk # buildkit
# Thu, 05 Sep 2024 16:37:13 GMT
RUN /etc/ca-certificates/update.d/docker-openjdk # buildkit
# Thu, 05 Sep 2024 16:37:13 GMT
EXPOSE map[9200/tcp:{} 9300/tcp:{}]
# Thu, 05 Sep 2024 16:37:13 GMT
LABEL org.label-schema.build-date=2024-09-02T22:04:47.310170297Z org.label-schema.license=Elastic-License-2.0 org.label-schema.name=Elasticsearch org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/elasticsearch org.label-schema.usage=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.label-schema.vcs-ref=253e8544a65ad44581194068936f2a5d57c2c051 org.label-schema.vcs-url=https://github.com/elastic/elasticsearch org.label-schema.vendor=Elastic org.label-schema.version=8.15.1 org.opencontainers.image.created=2024-09-02T22:04:47.310170297Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.opencontainers.image.licenses=Elastic-License-2.0 org.opencontainers.image.revision=253e8544a65ad44581194068936f2a5d57c2c051 org.opencontainers.image.source=https://github.com/elastic/elasticsearch org.opencontainers.image.title=Elasticsearch org.opencontainers.image.url=https://www.elastic.co/products/elasticsearch org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=8.15.1
# Thu, 05 Sep 2024 16:37:13 GMT
ENTRYPOINT ["/bin/tini" "--" "/usr/local/bin/docker-entrypoint.sh"]
# Thu, 05 Sep 2024 16:37:13 GMT
CMD ["eswrapper"]
# Thu, 05 Sep 2024 16:37:13 GMT
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
	-	`sha256:8579b28f71175a4a81dcbd28c2128ec176f3e861b04c2b1358865c10afdb5551`  
		Last Modified: Thu, 05 Sep 2024 22:08:05 GMT  
		Size: 457.6 MB (457608949 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53bbfb99c2ad899728cb7f97546be0fd5839a835246869e4d3f23a0326dcae80`  
		Last Modified: Thu, 05 Sep 2024 22:07:55 GMT  
		Size: 9.1 KB (9104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42efceb71ab4330839ab2a2b3559ba8bacce0360570d46c375f3a8abe98ab03f`  
		Last Modified: Thu, 05 Sep 2024 22:07:55 GMT  
		Size: 1.7 KB (1726 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cab0f68545a81e1e9d3e57859e646886f56ea3909c686ba3aab2832bdaf8f9ca`  
		Last Modified: Thu, 05 Sep 2024 22:07:55 GMT  
		Size: 185.9 KB (185925 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30fa3c69911b3cb9dc7740b2162b11ff94e99551059efb2f156f365cf41cd2ad`  
		Last Modified: Thu, 05 Sep 2024 22:07:56 GMT  
		Size: 408.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae5f18856d9a964a71fc5de310d686fecd16cabafef55031106cf0fb47e6e056`  
		Last Modified: Thu, 05 Sep 2024 22:07:56 GMT  
		Size: 109.3 KB (109253 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elasticsearch:8.15.1` - unknown; unknown

```console
$ docker pull elasticsearch@sha256:ae01b21c80d97030a84c4ebea6f582efd77a1af126bd47071d85a5d416a3eafb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2753643 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f05abc397ab0b26d5b615b0d60e673798547caa0c8dba2dcdbe2c38d81d97597`

```dockerfile
```

-	Layers:
	-	`sha256:2d0e5a06acfe334a37b6114c868c9179011f9aae6ec5887369a5981c2bdd69c4`  
		Last Modified: Thu, 05 Sep 2024 22:07:55 GMT  
		Size: 2.7 MB (2715728 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:07b972a8d926c277cce778145576ecd28de5997533a355b61dba470ee563d005`  
		Last Modified: Thu, 05 Sep 2024 22:07:55 GMT  
		Size: 37.9 KB (37915 bytes)  
		MIME: application/vnd.in-toto+json
