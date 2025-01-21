<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `elasticsearch`

-	[`elasticsearch:7.17.27`](#elasticsearch71727)
-	[`elasticsearch:8.16.3`](#elasticsearch8163)
-	[`elasticsearch:8.17.1`](#elasticsearch8171)

## `elasticsearch:7.17.27`

```console
$ docker pull elasticsearch@sha256:9a6443f55243f6acbfeb4a112d15eb3b9aac74bf25e0e39fa19b3ddd3a6879d0
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `elasticsearch:7.17.27` - linux; amd64

```console
$ docker pull elasticsearch@sha256:07e9262b856006959e384de7ca9587bc5c6da024ca7042216a9ea26efe4c69c1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **362.6 MB (362621819 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:59cf58dd31db94adca71c93829a25bdd1d031ee80d9816a53880849fa1b706b8`
-	Entrypoint: `["\/bin\/tini","--","\/usr\/local\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["eswrapper"]`

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
# Tue, 14 Jan 2025 19:20:58 GMT
RUN yes no | dpkg-reconfigure dash &&     for iter in 1 2 3 4 5 6 7 8 9 10; do       export DEBIAN_FRONTEND=noninteractive &&       apt-get update &&       apt-get upgrade -y &&       apt-get install -y --no-install-recommends         ca-certificates curl netcat p11-kit unzip zip &&       apt-get clean &&       rm -rf /var/lib/apt/lists/* &&       exit_code=0 && break ||         exit_code=$? && echo "apt-get error: retry $iter in 10s" && sleep 10;     done;     exit $exit_code # buildkit
# Tue, 14 Jan 2025 19:20:58 GMT
RUN groupadd -g 1000 elasticsearch &&     adduser --uid 1000 --gid 1000 --home /usr/share/elasticsearch elasticsearch &&     adduser elasticsearch root &&     chown -R 0:0 /usr/share/elasticsearch # buildkit
# Tue, 14 Jan 2025 19:20:58 GMT
ENV ELASTIC_CONTAINER=true
# Tue, 14 Jan 2025 19:20:58 GMT
WORKDIR /usr/share/elasticsearch
# Tue, 14 Jan 2025 19:20:58 GMT
COPY --chown=0:0 /usr/share/elasticsearch /usr/share/elasticsearch # buildkit
# Tue, 14 Jan 2025 19:20:58 GMT
COPY --chown=0:0 /bin/tini /bin/tini # buildkit
# Tue, 14 Jan 2025 19:20:58 GMT
ENV PATH=/usr/share/elasticsearch/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 14 Jan 2025 19:20:58 GMT
COPY bin/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh # buildkit
# Tue, 14 Jan 2025 19:20:58 GMT
RUN chmod g=u /etc/passwd &&     chmod 0555 /usr/local/bin/docker-entrypoint.sh &&     find / -xdev -perm -4000 -exec chmod ug-s {} + &&     chmod 0775 /usr/share/elasticsearch &&     chown elasticsearch bin config config/jvm.options.d data logs plugins # buildkit
# Tue, 14 Jan 2025 19:20:58 GMT
COPY bin/docker-openjdk /etc/ca-certificates/update.d/docker-openjdk # buildkit
# Tue, 14 Jan 2025 19:20:58 GMT
RUN /etc/ca-certificates/update.d/docker-openjdk # buildkit
# Tue, 14 Jan 2025 19:20:58 GMT
EXPOSE map[9200/tcp:{} 9300/tcp:{}]
# Tue, 14 Jan 2025 19:20:58 GMT
LABEL org.label-schema.build-date=2025-01-09T14:09:01.578835424Z org.label-schema.license=Elastic-License-2.0 org.label-schema.name=Elasticsearch org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/elasticsearch org.label-schema.usage=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.label-schema.vcs-ref=0f88dde84795b30ca0d2c0c4796643ec5938aeb5 org.label-schema.vcs-url=https://github.com/elastic/elasticsearch org.label-schema.vendor=Elastic org.label-schema.version=7.17.27 org.opencontainers.image.created=2025-01-09T14:09:01.578835424Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.opencontainers.image.licenses=Elastic-License-2.0 org.opencontainers.image.revision=0f88dde84795b30ca0d2c0c4796643ec5938aeb5 org.opencontainers.image.source=https://github.com/elastic/elasticsearch org.opencontainers.image.title=Elasticsearch org.opencontainers.image.url=https://www.elastic.co/products/elasticsearch org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=7.17.27
# Tue, 14 Jan 2025 19:20:58 GMT
ENTRYPOINT ["/bin/tini" "--" "/usr/local/bin/docker-entrypoint.sh"]
# Tue, 14 Jan 2025 19:20:58 GMT
CMD ["eswrapper"]
```

-	Layers:
	-	`sha256:d9802f032d6798e2086607424bfe88cb8ec1d6f116e11cd99592dcaf261e9cd2`  
		Last Modified: Fri, 11 Oct 2024 04:41:25 GMT  
		Size: 27.5 MB (27511060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93c168d6ce7e950b0e1cd182e381f48cb7c48f82cb8c1221fa667c88185ce40d`  
		Last Modified: Tue, 14 Jan 2025 20:28:28 GMT  
		Size: 7.5 MB (7524303 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e39dca01aa6a2c5db92b1fa84c84f72ef8ff7fb1dfa28912b085c28ab6a940f`  
		Last Modified: Tue, 14 Jan 2025 20:28:27 GMT  
		Size: 4.3 KB (4312 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc4f5d43e73ad18f9fe6ee3160cb5ac146a0f45b3a5931d994b2ca16f5191bba`  
		Last Modified: Tue, 14 Jan 2025 20:28:32 GMT  
		Size: 327.3 MB (327262495 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97b320e643df90a7dde00d450074c06d660e96ea4624be83dfec160a9279ba67`  
		Last Modified: Tue, 14 Jan 2025 20:28:27 GMT  
		Size: 9.5 KB (9530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11397b40a19fa0054e331a433a7d83d3f392cdf76f5c6e9c55b32c096d790e1c`  
		Last Modified: Tue, 14 Jan 2025 20:28:28 GMT  
		Size: 2.0 KB (1978 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50d429019534b3f9acfe344a6eb0e5408e24bc420b2c7cf285a4b758d51bc77d`  
		Last Modified: Tue, 14 Jan 2025 20:28:28 GMT  
		Size: 192.2 KB (192171 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:280d610f1b7c174b77c13ec7b3d1b7ecc7eae454bfe99982aa18ba68153ce61b`  
		Last Modified: Tue, 14 Jan 2025 20:28:28 GMT  
		Size: 404.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:979b19d45037402335aa40ad65c6e2ecb38e2b210a6bb18c8e6e2a2917e9a2e6`  
		Last Modified: Tue, 14 Jan 2025 20:28:29 GMT  
		Size: 115.5 KB (115534 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elasticsearch:7.17.27` - unknown; unknown

```console
$ docker pull elasticsearch@sha256:a3ea15f2b1dec96d939c9ba4f149c3f78933f0552997cd426565c2fb8c04fb8b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2589024 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a84265a9404ad42f522a0300510cb966655efcf33a4bd3596cfe842ba6839eec`

```dockerfile
```

-	Layers:
	-	`sha256:47958e0314cab389487a9cd6a8b3d4232e5d6c2ab1793b6c8af705b4c7945f5b`  
		Last Modified: Tue, 14 Jan 2025 20:28:27 GMT  
		Size: 2.6 MB (2551136 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:21ab10d6870d45a852505fd648d1f7b2a7dcbd9ae7bedda4eec06e75c54f404f`  
		Last Modified: Tue, 14 Jan 2025 20:28:27 GMT  
		Size: 37.9 KB (37888 bytes)  
		MIME: application/vnd.in-toto+json

### `elasticsearch:7.17.27` - linux; arm64 variant v8

```console
$ docker pull elasticsearch@sha256:f1ee7d61820aed6cc83a05f481ef822644fa8134bee9c74e8c89ea8cf85047e0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **358.6 MB (358564629 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:37ac55d4ec9db03a1be37a1b0c394d513f5c85a0c80576891dcffdd9803bec1c`
-	Entrypoint: `["\/bin\/tini","--","\/usr\/local\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["eswrapper"]`

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
# Tue, 14 Jan 2025 19:20:58 GMT
RUN yes no | dpkg-reconfigure dash &&     for iter in 1 2 3 4 5 6 7 8 9 10; do       export DEBIAN_FRONTEND=noninteractive &&       apt-get update &&       apt-get upgrade -y &&       apt-get install -y --no-install-recommends         ca-certificates curl netcat p11-kit unzip zip &&       apt-get clean &&       rm -rf /var/lib/apt/lists/* &&       exit_code=0 && break ||         exit_code=$? && echo "apt-get error: retry $iter in 10s" && sleep 10;     done;     exit $exit_code # buildkit
# Tue, 14 Jan 2025 19:20:58 GMT
RUN groupadd -g 1000 elasticsearch &&     adduser --uid 1000 --gid 1000 --home /usr/share/elasticsearch elasticsearch &&     adduser elasticsearch root &&     chown -R 0:0 /usr/share/elasticsearch # buildkit
# Tue, 14 Jan 2025 19:20:58 GMT
ENV ELASTIC_CONTAINER=true
# Tue, 14 Jan 2025 19:20:58 GMT
WORKDIR /usr/share/elasticsearch
# Tue, 14 Jan 2025 19:20:58 GMT
COPY --chown=0:0 /usr/share/elasticsearch /usr/share/elasticsearch # buildkit
# Tue, 14 Jan 2025 19:20:58 GMT
COPY --chown=0:0 /bin/tini /bin/tini # buildkit
# Tue, 14 Jan 2025 19:20:58 GMT
ENV PATH=/usr/share/elasticsearch/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 14 Jan 2025 19:20:58 GMT
COPY bin/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh # buildkit
# Tue, 14 Jan 2025 19:20:58 GMT
RUN chmod g=u /etc/passwd &&     chmod 0555 /usr/local/bin/docker-entrypoint.sh &&     find / -xdev -perm -4000 -exec chmod ug-s {} + &&     chmod 0775 /usr/share/elasticsearch &&     chown elasticsearch bin config config/jvm.options.d data logs plugins # buildkit
# Tue, 14 Jan 2025 19:20:58 GMT
COPY bin/docker-openjdk /etc/ca-certificates/update.d/docker-openjdk # buildkit
# Tue, 14 Jan 2025 19:20:58 GMT
RUN /etc/ca-certificates/update.d/docker-openjdk # buildkit
# Tue, 14 Jan 2025 19:20:58 GMT
EXPOSE map[9200/tcp:{} 9300/tcp:{}]
# Tue, 14 Jan 2025 19:20:58 GMT
LABEL org.label-schema.build-date=2025-01-09T14:09:01.578835424Z org.label-schema.license=Elastic-License-2.0 org.label-schema.name=Elasticsearch org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/elasticsearch org.label-schema.usage=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.label-schema.vcs-ref=0f88dde84795b30ca0d2c0c4796643ec5938aeb5 org.label-schema.vcs-url=https://github.com/elastic/elasticsearch org.label-schema.vendor=Elastic org.label-schema.version=7.17.27 org.opencontainers.image.created=2025-01-09T14:09:01.578835424Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.opencontainers.image.licenses=Elastic-License-2.0 org.opencontainers.image.revision=0f88dde84795b30ca0d2c0c4796643ec5938aeb5 org.opencontainers.image.source=https://github.com/elastic/elasticsearch org.opencontainers.image.title=Elasticsearch org.opencontainers.image.url=https://www.elastic.co/products/elasticsearch org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=7.17.27
# Tue, 14 Jan 2025 19:20:58 GMT
ENTRYPOINT ["/bin/tini" "--" "/usr/local/bin/docker-entrypoint.sh"]
# Tue, 14 Jan 2025 19:20:58 GMT
CMD ["eswrapper"]
```

-	Layers:
	-	`sha256:1b9f3c55f9d4aa5c52eb67a4cb7d0f4726ab85a413b50e3e3fe788befce3d297`  
		Last Modified: Fri, 11 Oct 2024 04:41:30 GMT  
		Size: 26.0 MB (25973828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b94b5f7dc63efc97d7aac00f1ff47d685babc6659a830f765d346e5cb09f0019`  
		Last Modified: Wed, 15 Jan 2025 01:29:04 GMT  
		Size: 7.3 MB (7347536 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:045f16f1c1e5b105517c26dd222e1171429bb9894892178df9fe0e63f2783c99`  
		Last Modified: Wed, 15 Jan 2025 01:29:03 GMT  
		Size: 4.3 KB (4319 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a74e1a7409159a1d77dfc2a6a4f71e23748526b42cdb08b99a36783cf988367c`  
		Last Modified: Wed, 15 Jan 2025 01:29:10 GMT  
		Size: 324.9 MB (324925722 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d99d020f552cf790194601796ae1682c5ae838967c42b6fa94d003cd9b902edd`  
		Last Modified: Wed, 15 Jan 2025 01:29:03 GMT  
		Size: 9.1 KB (9096 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8f958882899f954957d771a7e1b7aaf38d3e7bcc711df6e434b41d91a97572a`  
		Last Modified: Wed, 15 Jan 2025 01:29:04 GMT  
		Size: 2.0 KB (1979 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f6d103b20cd3b2147d99a9a9b4cba9e7a73861d36a6616f66b709d8a3b13bda`  
		Last Modified: Wed, 15 Jan 2025 01:29:04 GMT  
		Size: 186.2 KB (186176 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5cce3ada22df59801b30d351ece61b6a95aa7f6d899ed1d4823564f92007cde`  
		Last Modified: Wed, 15 Jan 2025 01:29:05 GMT  
		Size: 404.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39509e1eff1ea51e88403477c0d1cd98b030be538a966cc613bc8ebeb1b512e2`  
		Last Modified: Wed, 15 Jan 2025 01:29:05 GMT  
		Size: 115.5 KB (115537 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elasticsearch:7.17.27` - unknown; unknown

```console
$ docker pull elasticsearch@sha256:5de0e392a6f62a9065b28479a6c00a71392eccc9cf2fb472c4ba109c23d76cea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2588198 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:87f291441dd21a0aead99aeb46d433cac2f28be143eadba3a79dea24fc720f6d`

```dockerfile
```

-	Layers:
	-	`sha256:077d2fe4726e2ea0b8dac6a60b7cbb8fe866b499cbd19d02876b3efa2d41e633`  
		Last Modified: Wed, 15 Jan 2025 01:29:03 GMT  
		Size: 2.6 MB (2550108 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2ba9c3734d9b4a8163946a0df7ed5e0d7da46bd7889e72dc281aae334703770a`  
		Last Modified: Wed, 15 Jan 2025 01:29:03 GMT  
		Size: 38.1 KB (38090 bytes)  
		MIME: application/vnd.in-toto+json

## `elasticsearch:8.16.3`

```console
$ docker pull elasticsearch@sha256:7706d227807752e62b7cbb79b28d309d8bb02cf6781ebcaf91269b01db0c42c1
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `elasticsearch:8.16.3` - linux; amd64

```console
$ docker pull elasticsearch@sha256:16dc7e7a612b1be1da8d71fcf0502e9e40c437d99ed74a0ad5b2a5d236e68b99
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **676.4 MB (676418006 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:febb03e1cda6bac56c285d380c0d5fcddc678cc40d5980baac1d49945e9ce32e`
-	Entrypoint: `["\/bin\/tini","--","\/usr\/local\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["eswrapper"]`

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
# Tue, 21 Jan 2025 08:29:25 GMT
RUN yes no | dpkg-reconfigure dash &&     for iter in 1 2 3 4 5 6 7 8 9 10; do       export DEBIAN_FRONTEND=noninteractive &&       apt-get update &&       apt-get upgrade -y &&       apt-get install -y --no-install-recommends         ca-certificates curl netcat p11-kit unzip zip  &&       apt-get clean &&       rm -rf /var/lib/apt/lists/* &&       exit_code=0 && break ||         exit_code=$? && echo "apt-get error: retry $iter in 10s" && sleep 10;     done;     exit $exit_code # buildkit
# Tue, 21 Jan 2025 08:29:25 GMT
RUN groupadd -g 1000 elasticsearch &&     adduser --uid 1000 --gid 1000 --home /usr/share/elasticsearch elasticsearch &&     adduser elasticsearch root &&     chown -R 0:0 /usr/share/elasticsearch # buildkit
# Tue, 21 Jan 2025 08:29:25 GMT
ENV ELASTIC_CONTAINER=true
# Tue, 21 Jan 2025 08:29:25 GMT
WORKDIR /usr/share/elasticsearch
# Tue, 21 Jan 2025 08:29:25 GMT
COPY --chown=0:0 /usr/share/elasticsearch /usr/share/elasticsearch # buildkit
# Tue, 21 Jan 2025 08:29:25 GMT
COPY --chown=0:0 /bin/tini /bin/tini # buildkit
# Tue, 21 Jan 2025 08:29:25 GMT
ENV PATH=/usr/share/elasticsearch/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 21 Jan 2025 08:29:25 GMT
ENV SHELL=/bin/bash
# Tue, 21 Jan 2025 08:29:25 GMT
COPY bin/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh # buildkit
# Tue, 21 Jan 2025 08:29:25 GMT
RUN chmod g=u /etc/passwd &&     chmod 0555 /usr/local/bin/docker-entrypoint.sh &&     find / -xdev -perm -4000 -exec chmod ug-s {} + &&     chmod 0775 /usr/share/elasticsearch &&     chown elasticsearch bin config config/jvm.options.d data logs plugins # buildkit
# Tue, 21 Jan 2025 08:29:25 GMT
COPY bin/docker-openjdk /etc/ca-certificates/update.d/docker-openjdk # buildkit
# Tue, 21 Jan 2025 08:29:25 GMT
RUN /etc/ca-certificates/update.d/docker-openjdk # buildkit
# Tue, 21 Jan 2025 08:29:25 GMT
EXPOSE map[9200/tcp:{} 9300/tcp:{}]
# Tue, 21 Jan 2025 08:29:25 GMT
LABEL org.label-schema.build-date=2025-01-10T10:08:28.587559883Z org.label-schema.license=Elastic-License-2.0 org.label-schema.name=Elasticsearch org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/elasticsearch org.label-schema.usage=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.label-schema.vcs-ref=2eb78bceb86e182dc8f45ab76a704b1bfd352c9d org.label-schema.vcs-url=https://github.com/elastic/elasticsearch org.label-schema.vendor=Elastic org.label-schema.version=8.16.3 org.opencontainers.image.created=2025-01-10T10:08:28.587559883Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.opencontainers.image.licenses=Elastic-License-2.0 org.opencontainers.image.revision=2eb78bceb86e182dc8f45ab76a704b1bfd352c9d org.opencontainers.image.source=https://github.com/elastic/elasticsearch org.opencontainers.image.title=Elasticsearch org.opencontainers.image.url=https://www.elastic.co/products/elasticsearch org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=8.16.3
# Tue, 21 Jan 2025 08:29:25 GMT
ENTRYPOINT ["/bin/tini" "--" "/usr/local/bin/docker-entrypoint.sh"]
# Tue, 21 Jan 2025 08:29:25 GMT
CMD ["eswrapper"]
# Tue, 21 Jan 2025 08:29:25 GMT
USER 1000:0
```

-	Layers:
	-	`sha256:d9802f032d6798e2086607424bfe88cb8ec1d6f116e11cd99592dcaf261e9cd2`  
		Last Modified: Fri, 11 Oct 2024 04:41:25 GMT  
		Size: 27.5 MB (27511060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:379b15f1494534c6e906eeaf799b4801a089ad6a0cde481ff446c0fdc882a072`  
		Last Modified: Tue, 21 Jan 2025 19:30:08 GMT  
		Size: 7.5 MB (7524281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb5328be92ea88eb61704c631497adf0d7bcc754ddcc088d857d23714b2eb372`  
		Last Modified: Tue, 21 Jan 2025 19:30:08 GMT  
		Size: 4.3 KB (4319 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec0306fd155cbe17e0af2ef1b3a216dfbf4bd44d0474e8c51ab81202783105a6`  
		Last Modified: Tue, 21 Jan 2025 19:30:20 GMT  
		Size: 641.1 MB (641059223 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9366089715563d268204cf2457afdb90c006352f252e75cd2316590ee6889f2`  
		Last Modified: Tue, 21 Jan 2025 19:30:08 GMT  
		Size: 9.5 KB (9526 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fd290a6b33a305c7315f96c8002e46d0029eddb54c87d8793e73baf70896e93`  
		Last Modified: Tue, 21 Jan 2025 19:30:08 GMT  
		Size: 1.7 KB (1721 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d3ad9851f32b7cd7fbba1f2f2337031a9d7f7486d61f79a7ea826b1e2999392`  
		Last Modified: Tue, 21 Jan 2025 19:30:09 GMT  
		Size: 191.9 KB (191905 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11a21968345e38a9c9c863f744311cd828ca713be052984ba426f471137f2352`  
		Last Modified: Tue, 21 Jan 2025 19:30:09 GMT  
		Size: 406.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6cfa4f9b0825a755108ac2d9812f3bc878b21c88c3d0f860fb07be12b198a89e`  
		Last Modified: Tue, 21 Jan 2025 19:30:09 GMT  
		Size: 115.5 KB (115533 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elasticsearch:8.16.3` - unknown; unknown

```console
$ docker pull elasticsearch@sha256:7ae6c2c3ee723a918e247b48baf16d5fef63b0e9ef86217a718ae4feec0fa543
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (3042158 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b70c13d5cf0bbecf4c60350fe30df6f703e4d1fae2f858383d6cf15eb724f4be`

```dockerfile
```

-	Layers:
	-	`sha256:de8f525744112cd670b0ffe62b4535ce813897e1a7edb2fb75604bd00523b558`  
		Last Modified: Tue, 21 Jan 2025 19:30:08 GMT  
		Size: 3.0 MB (3003952 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:79fd155e4e9f07647833f7dea2afdbc3695ec2b8bbf83c4d7784d24c1acd349c`  
		Last Modified: Tue, 21 Jan 2025 19:30:08 GMT  
		Size: 38.2 KB (38206 bytes)  
		MIME: application/vnd.in-toto+json

### `elasticsearch:8.16.3` - linux; arm64 variant v8

```console
$ docker pull elasticsearch@sha256:7cdfa8c1e206f5ff026ba196cab32cf8459fafdea8c8754d581c710168030d60
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **519.8 MB (519762925 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:139346ce1464a231e3c16a5858f92365db7471782c7f860c5e6df3688046d560`
-	Entrypoint: `["\/bin\/tini","--","\/usr\/local\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["eswrapper"]`

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
# Tue, 21 Jan 2025 08:29:25 GMT
RUN yes no | dpkg-reconfigure dash &&     for iter in 1 2 3 4 5 6 7 8 9 10; do       export DEBIAN_FRONTEND=noninteractive &&       apt-get update &&       apt-get upgrade -y &&       apt-get install -y --no-install-recommends         ca-certificates curl netcat p11-kit unzip zip  &&       apt-get clean &&       rm -rf /var/lib/apt/lists/* &&       exit_code=0 && break ||         exit_code=$? && echo "apt-get error: retry $iter in 10s" && sleep 10;     done;     exit $exit_code # buildkit
# Tue, 21 Jan 2025 08:29:25 GMT
RUN groupadd -g 1000 elasticsearch &&     adduser --uid 1000 --gid 1000 --home /usr/share/elasticsearch elasticsearch &&     adduser elasticsearch root &&     chown -R 0:0 /usr/share/elasticsearch # buildkit
# Tue, 21 Jan 2025 08:29:25 GMT
ENV ELASTIC_CONTAINER=true
# Tue, 21 Jan 2025 08:29:25 GMT
WORKDIR /usr/share/elasticsearch
# Tue, 21 Jan 2025 08:29:25 GMT
COPY --chown=0:0 /usr/share/elasticsearch /usr/share/elasticsearch # buildkit
# Tue, 21 Jan 2025 08:29:25 GMT
COPY --chown=0:0 /bin/tini /bin/tini # buildkit
# Tue, 21 Jan 2025 08:29:25 GMT
ENV PATH=/usr/share/elasticsearch/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 21 Jan 2025 08:29:25 GMT
ENV SHELL=/bin/bash
# Tue, 21 Jan 2025 08:29:25 GMT
COPY bin/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh # buildkit
# Tue, 21 Jan 2025 08:29:25 GMT
RUN chmod g=u /etc/passwd &&     chmod 0555 /usr/local/bin/docker-entrypoint.sh &&     find / -xdev -perm -4000 -exec chmod ug-s {} + &&     chmod 0775 /usr/share/elasticsearch &&     chown elasticsearch bin config config/jvm.options.d data logs plugins # buildkit
# Tue, 21 Jan 2025 08:29:25 GMT
COPY bin/docker-openjdk /etc/ca-certificates/update.d/docker-openjdk # buildkit
# Tue, 21 Jan 2025 08:29:25 GMT
RUN /etc/ca-certificates/update.d/docker-openjdk # buildkit
# Tue, 21 Jan 2025 08:29:25 GMT
EXPOSE map[9200/tcp:{} 9300/tcp:{}]
# Tue, 21 Jan 2025 08:29:25 GMT
LABEL org.label-schema.build-date=2025-01-10T10:08:28.587559883Z org.label-schema.license=Elastic-License-2.0 org.label-schema.name=Elasticsearch org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/elasticsearch org.label-schema.usage=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.label-schema.vcs-ref=2eb78bceb86e182dc8f45ab76a704b1bfd352c9d org.label-schema.vcs-url=https://github.com/elastic/elasticsearch org.label-schema.vendor=Elastic org.label-schema.version=8.16.3 org.opencontainers.image.created=2025-01-10T10:08:28.587559883Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.opencontainers.image.licenses=Elastic-License-2.0 org.opencontainers.image.revision=2eb78bceb86e182dc8f45ab76a704b1bfd352c9d org.opencontainers.image.source=https://github.com/elastic/elasticsearch org.opencontainers.image.title=Elasticsearch org.opencontainers.image.url=https://www.elastic.co/products/elasticsearch org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=8.16.3
# Tue, 21 Jan 2025 08:29:25 GMT
ENTRYPOINT ["/bin/tini" "--" "/usr/local/bin/docker-entrypoint.sh"]
# Tue, 21 Jan 2025 08:29:25 GMT
CMD ["eswrapper"]
# Tue, 21 Jan 2025 08:29:25 GMT
USER 1000:0
```

-	Layers:
	-	`sha256:1b9f3c55f9d4aa5c52eb67a4cb7d0f4726ab85a413b50e3e3fe788befce3d297`  
		Last Modified: Fri, 11 Oct 2024 04:41:30 GMT  
		Size: 26.0 MB (25973828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0f115f46f9e1a30ca45a6d320df30ebeeddee8136e0ac793f8da3249e298ccb`  
		Last Modified: Tue, 21 Jan 2025 19:53:24 GMT  
		Size: 7.3 MB (7347539 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93bfa8983082b5dc21ae377855e80afb49efd59da8cf84c064f81ff5b73fced8`  
		Last Modified: Tue, 21 Jan 2025 19:53:23 GMT  
		Size: 4.3 KB (4320 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51e9cb5301bbffd08d95462bb3b896dd0d71062180b438f815b4662874b685ac`  
		Last Modified: Tue, 21 Jan 2025 19:53:34 GMT  
		Size: 486.1 MB (486124536 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68eeaec9e2913fe4a5bdf0289f338e92a4c6ebf397b52a1ed99581ca8a5116c3`  
		Last Modified: Tue, 21 Jan 2025 19:53:23 GMT  
		Size: 9.1 KB (9096 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:beaf1ea63c988db2e46589673cd83307dbe23f013e804a8f8d72cc527190d413`  
		Last Modified: Tue, 21 Jan 2025 19:53:24 GMT  
		Size: 1.7 KB (1721 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22a04456653b65013417394776a61594f7a5595160675402cabab994d1fac496`  
		Last Modified: Tue, 21 Jan 2025 19:53:25 GMT  
		Size: 185.9 KB (185916 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f32b3b5b1330959bdff6b100d6ab1c802f4c6e8f6e8afad682f040b57026c29`  
		Last Modified: Tue, 21 Jan 2025 19:53:25 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae37a7d4b8bde327138d7cdb98bd93b9cd290e593281dbeb09591e391282c0b3`  
		Last Modified: Tue, 21 Jan 2025 19:53:25 GMT  
		Size: 115.5 KB (115534 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elasticsearch:8.16.3` - unknown; unknown

```console
$ docker pull elasticsearch@sha256:46c0bd8d46bf80897fb0a2439afa8eb8930929ff9715ed0bc5e238f3d732ecf8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (3041333 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf10dadb8824ab1a85851ad896165530bc204c9acbd01911fce37d166c7ba226`

```dockerfile
```

-	Layers:
	-	`sha256:a72c74cd18d6aa58371d8105c42332d04e46ef541827653b8a3a78eeddf6a978`  
		Last Modified: Tue, 21 Jan 2025 19:53:24 GMT  
		Size: 3.0 MB (3002924 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:44016f8123837dbf2539b24028871e91eb61acf5aafa4ba9623c7a5df05125b3`  
		Last Modified: Tue, 21 Jan 2025 19:53:23 GMT  
		Size: 38.4 KB (38409 bytes)  
		MIME: application/vnd.in-toto+json

## `elasticsearch:8.17.1`

```console
$ docker pull elasticsearch@sha256:b3c98b2b5b1c461d31bf1dec5d0907db0de22e344cb3d697cdefd4790629f5da
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `elasticsearch:8.17.1` - linux; amd64

```console
$ docker pull elasticsearch@sha256:05a23910f34a342a96f032c83c08d29fa0d6fc276254f74014eedd479c7c8e57
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **677.4 MB (677361213 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:76cccb2418a444c776bab0d44d7336d7273bf5fb52c5085cbd0cd704dc398fe8`
-	Entrypoint: `["\/bin\/tini","--","\/usr\/local\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["eswrapper"]`

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
# Tue, 21 Jan 2025 08:22:13 GMT
RUN yes no | dpkg-reconfigure dash &&     for iter in 1 2 3 4 5 6 7 8 9 10; do       export DEBIAN_FRONTEND=noninteractive &&       apt-get update &&       apt-get upgrade -y &&       apt-get install -y --no-install-recommends         ca-certificates curl netcat p11-kit unzip zip  &&       apt-get clean &&       rm -rf /var/lib/apt/lists/* &&       exit_code=0 && break ||         exit_code=$? && echo "apt-get error: retry $iter in 10s" && sleep 10;     done;     exit $exit_code # buildkit
# Tue, 21 Jan 2025 08:22:13 GMT
RUN groupadd -g 1000 elasticsearch &&     adduser --uid 1000 --gid 1000 --home /usr/share/elasticsearch elasticsearch &&     adduser elasticsearch root &&     chown -R 0:0 /usr/share/elasticsearch # buildkit
# Tue, 21 Jan 2025 08:22:13 GMT
ENV ELASTIC_CONTAINER=true
# Tue, 21 Jan 2025 08:22:13 GMT
WORKDIR /usr/share/elasticsearch
# Tue, 21 Jan 2025 08:22:13 GMT
COPY --chown=0:0 /usr/share/elasticsearch /usr/share/elasticsearch # buildkit
# Tue, 21 Jan 2025 08:22:13 GMT
COPY --chown=0:0 /bin/tini /bin/tini # buildkit
# Tue, 21 Jan 2025 08:22:13 GMT
ENV PATH=/usr/share/elasticsearch/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 21 Jan 2025 08:22:13 GMT
ENV SHELL=/bin/bash
# Tue, 21 Jan 2025 08:22:13 GMT
COPY bin/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh # buildkit
# Tue, 21 Jan 2025 08:22:13 GMT
RUN chmod g=u /etc/passwd &&     chmod 0555 /usr/local/bin/docker-entrypoint.sh &&     find / -xdev -perm -4000 -exec chmod ug-s {} + &&     chmod 0775 /usr/share/elasticsearch &&     chown elasticsearch bin config config/jvm.options.d data logs plugins # buildkit
# Tue, 21 Jan 2025 08:22:13 GMT
COPY bin/docker-openjdk /etc/ca-certificates/update.d/docker-openjdk # buildkit
# Tue, 21 Jan 2025 08:22:13 GMT
RUN /etc/ca-certificates/update.d/docker-openjdk # buildkit
# Tue, 21 Jan 2025 08:22:13 GMT
EXPOSE map[9200/tcp:{} 9300/tcp:{}]
# Tue, 21 Jan 2025 08:22:13 GMT
LABEL org.label-schema.build-date=2025-01-10T10:08:26.972230187Z org.label-schema.license=Elastic-License-2.0 org.label-schema.name=Elasticsearch org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/elasticsearch org.label-schema.usage=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.label-schema.vcs-ref=d4b391d925c31d262eb767b8b2db8f398103f909 org.label-schema.vcs-url=https://github.com/elastic/elasticsearch org.label-schema.vendor=Elastic org.label-schema.version=8.17.1 org.opencontainers.image.created=2025-01-10T10:08:26.972230187Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.opencontainers.image.licenses=Elastic-License-2.0 org.opencontainers.image.revision=d4b391d925c31d262eb767b8b2db8f398103f909 org.opencontainers.image.source=https://github.com/elastic/elasticsearch org.opencontainers.image.title=Elasticsearch org.opencontainers.image.url=https://www.elastic.co/products/elasticsearch org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=8.17.1
# Tue, 21 Jan 2025 08:22:13 GMT
ENTRYPOINT ["/bin/tini" "--" "/usr/local/bin/docker-entrypoint.sh"]
# Tue, 21 Jan 2025 08:22:13 GMT
CMD ["eswrapper"]
# Tue, 21 Jan 2025 08:22:13 GMT
USER 1000:0
```

-	Layers:
	-	`sha256:d9802f032d6798e2086607424bfe88cb8ec1d6f116e11cd99592dcaf261e9cd2`  
		Last Modified: Fri, 11 Oct 2024 04:41:25 GMT  
		Size: 27.5 MB (27511060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0c2592722548d66501179de36e1b1a6c139f1fe7b35fe378c644f81b459f9af`  
		Last Modified: Tue, 21 Jan 2025 19:29:29 GMT  
		Size: 7.5 MB (7524338 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d5fd18f86e6a541a1fe438f49e09d5ef591e976899c21d045fbc07773b3ec41`  
		Last Modified: Tue, 21 Jan 2025 19:29:29 GMT  
		Size: 4.3 KB (4315 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b90c2e94d5b30adb7d2029a3fdf2997473fc8492abdef436f1ec5cf464aa575c`  
		Last Modified: Tue, 21 Jan 2025 19:29:38 GMT  
		Size: 642.0 MB (642002373 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6eae409562d05e09b0b9ec72187f8214ee6588dabf02633d97639aa4956363a7`  
		Last Modified: Tue, 21 Jan 2025 19:29:29 GMT  
		Size: 9.5 KB (9528 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43a1b023780107f8cef1b8cc0abf23a77dd9c79d247f5859bb603a6b05239bbf`  
		Last Modified: Tue, 21 Jan 2025 19:29:29 GMT  
		Size: 1.7 KB (1724 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b026a259c4a17f5df96160b21be44479aa16be0ded31b304607b0691352a6f7`  
		Last Modified: Tue, 21 Jan 2025 19:29:29 GMT  
		Size: 191.9 KB (191904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0fc09a494bcf49391603ad6f54a2da0a105571fda770907046e66590aa1838d9`  
		Last Modified: Tue, 21 Jan 2025 19:29:30 GMT  
		Size: 404.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a51bc41d043b765ab244bed565a45f1fa40453cd510fbd7ef06a628c55eb0b9`  
		Last Modified: Tue, 21 Jan 2025 19:29:30 GMT  
		Size: 115.5 KB (115535 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elasticsearch:8.17.1` - unknown; unknown

```console
$ docker pull elasticsearch@sha256:0d60a1689dd86d92c2f6dc3b49abecea5d8dab0a502d39532636a28aa073840f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (3048357 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e5788c8325b8a96a4065368a9e2fb1729ad45def8237ea5ac1113a5b478cc8ee`

```dockerfile
```

-	Layers:
	-	`sha256:9b11818749db3f80f924a97b84db74c3279d86e9b2a619aa89a4caea1a01fcc4`  
		Last Modified: Tue, 21 Jan 2025 19:29:29 GMT  
		Size: 3.0 MB (3010152 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:823dca4dbfc5a637de44b9ba641f6c1cbb83936e79664ec86f90bafd1c7cc73a`  
		Last Modified: Tue, 21 Jan 2025 19:29:29 GMT  
		Size: 38.2 KB (38205 bytes)  
		MIME: application/vnd.in-toto+json

### `elasticsearch:8.17.1` - linux; arm64 variant v8

```console
$ docker pull elasticsearch@sha256:ca3812655ac79d912f8e46d8e641d3744be4dcfa8d59fd362ff374ac8facb7e4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **520.7 MB (520705340 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a4521b22f5b706fc24e41cb00d8cd151c4cba96aad06d98996d6aa18eb3dcc30`
-	Entrypoint: `["\/bin\/tini","--","\/usr\/local\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["eswrapper"]`

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
# Tue, 21 Jan 2025 08:22:13 GMT
RUN yes no | dpkg-reconfigure dash &&     for iter in 1 2 3 4 5 6 7 8 9 10; do       export DEBIAN_FRONTEND=noninteractive &&       apt-get update &&       apt-get upgrade -y &&       apt-get install -y --no-install-recommends         ca-certificates curl netcat p11-kit unzip zip  &&       apt-get clean &&       rm -rf /var/lib/apt/lists/* &&       exit_code=0 && break ||         exit_code=$? && echo "apt-get error: retry $iter in 10s" && sleep 10;     done;     exit $exit_code # buildkit
# Tue, 21 Jan 2025 08:22:13 GMT
RUN groupadd -g 1000 elasticsearch &&     adduser --uid 1000 --gid 1000 --home /usr/share/elasticsearch elasticsearch &&     adduser elasticsearch root &&     chown -R 0:0 /usr/share/elasticsearch # buildkit
# Tue, 21 Jan 2025 08:22:13 GMT
ENV ELASTIC_CONTAINER=true
# Tue, 21 Jan 2025 08:22:13 GMT
WORKDIR /usr/share/elasticsearch
# Tue, 21 Jan 2025 08:22:13 GMT
COPY --chown=0:0 /usr/share/elasticsearch /usr/share/elasticsearch # buildkit
# Tue, 21 Jan 2025 08:22:13 GMT
COPY --chown=0:0 /bin/tini /bin/tini # buildkit
# Tue, 21 Jan 2025 08:22:13 GMT
ENV PATH=/usr/share/elasticsearch/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 21 Jan 2025 08:22:13 GMT
ENV SHELL=/bin/bash
# Tue, 21 Jan 2025 08:22:13 GMT
COPY bin/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh # buildkit
# Tue, 21 Jan 2025 08:22:13 GMT
RUN chmod g=u /etc/passwd &&     chmod 0555 /usr/local/bin/docker-entrypoint.sh &&     find / -xdev -perm -4000 -exec chmod ug-s {} + &&     chmod 0775 /usr/share/elasticsearch &&     chown elasticsearch bin config config/jvm.options.d data logs plugins # buildkit
# Tue, 21 Jan 2025 08:22:13 GMT
COPY bin/docker-openjdk /etc/ca-certificates/update.d/docker-openjdk # buildkit
# Tue, 21 Jan 2025 08:22:13 GMT
RUN /etc/ca-certificates/update.d/docker-openjdk # buildkit
# Tue, 21 Jan 2025 08:22:13 GMT
EXPOSE map[9200/tcp:{} 9300/tcp:{}]
# Tue, 21 Jan 2025 08:22:13 GMT
LABEL org.label-schema.build-date=2025-01-10T10:08:26.972230187Z org.label-schema.license=Elastic-License-2.0 org.label-schema.name=Elasticsearch org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/elasticsearch org.label-schema.usage=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.label-schema.vcs-ref=d4b391d925c31d262eb767b8b2db8f398103f909 org.label-schema.vcs-url=https://github.com/elastic/elasticsearch org.label-schema.vendor=Elastic org.label-schema.version=8.17.1 org.opencontainers.image.created=2025-01-10T10:08:26.972230187Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.opencontainers.image.licenses=Elastic-License-2.0 org.opencontainers.image.revision=d4b391d925c31d262eb767b8b2db8f398103f909 org.opencontainers.image.source=https://github.com/elastic/elasticsearch org.opencontainers.image.title=Elasticsearch org.opencontainers.image.url=https://www.elastic.co/products/elasticsearch org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=8.17.1
# Tue, 21 Jan 2025 08:22:13 GMT
ENTRYPOINT ["/bin/tini" "--" "/usr/local/bin/docker-entrypoint.sh"]
# Tue, 21 Jan 2025 08:22:13 GMT
CMD ["eswrapper"]
# Tue, 21 Jan 2025 08:22:13 GMT
USER 1000:0
```

-	Layers:
	-	`sha256:1b9f3c55f9d4aa5c52eb67a4cb7d0f4726ab85a413b50e3e3fe788befce3d297`  
		Last Modified: Fri, 11 Oct 2024 04:41:30 GMT  
		Size: 26.0 MB (25973828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0f115f46f9e1a30ca45a6d320df30ebeeddee8136e0ac793f8da3249e298ccb`  
		Last Modified: Tue, 21 Jan 2025 19:53:24 GMT  
		Size: 7.3 MB (7347539 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93bfa8983082b5dc21ae377855e80afb49efd59da8cf84c064f81ff5b73fced8`  
		Last Modified: Tue, 21 Jan 2025 19:53:23 GMT  
		Size: 4.3 KB (4320 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:777b9dd9b360ff3cfdc4d6f587c31c40958a123b4d992809c31c80d705d77626`  
		Last Modified: Tue, 21 Jan 2025 19:55:34 GMT  
		Size: 487.1 MB (487066948 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9841e674b78d24d186ece14b17387d87dc6fb971e366a753983afe0c28024d7`  
		Last Modified: Tue, 21 Jan 2025 19:55:19 GMT  
		Size: 9.1 KB (9098 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbadb89cd10745cdb20d74db1f13ae150f0a569167b06a1e8e80c77915892684`  
		Last Modified: Tue, 21 Jan 2025 19:55:19 GMT  
		Size: 1.7 KB (1721 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4cd388d093940e02bfda4fcdb8112664d495df0346a36534c699272416f503b0`  
		Last Modified: Tue, 21 Jan 2025 19:55:19 GMT  
		Size: 185.9 KB (185918 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67419900d778f6071e7173bfd97e8e3ac2bd481613562ee4f3ad8b578af4fb13`  
		Last Modified: Tue, 21 Jan 2025 19:55:20 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42766a737dd1004bd1abf2fec76db00d33bea48db21c5037854ad0c6fa7e08e7`  
		Last Modified: Tue, 21 Jan 2025 19:55:20 GMT  
		Size: 115.5 KB (115533 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elasticsearch:8.17.1` - unknown; unknown

```console
$ docker pull elasticsearch@sha256:5c0dbde3f161850d7cd68360cd8e935b9c5e327b5f828fdcf164159140799c19
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (3047533 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:530ccd9744b1806344c2d4dea4505413a83cd06a3d91ebff2aec33b49204355b`

```dockerfile
```

-	Layers:
	-	`sha256:f15084704600202c5932052a227d2c7370faeb781641618e549299d67ea9da8b`  
		Last Modified: Tue, 21 Jan 2025 19:55:19 GMT  
		Size: 3.0 MB (3009124 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:78baeffcfcdef3327129987fc9f1ded7fea302f7f181263ae2b5fed23325f81b`  
		Last Modified: Tue, 21 Jan 2025 19:55:19 GMT  
		Size: 38.4 KB (38409 bytes)  
		MIME: application/vnd.in-toto+json
