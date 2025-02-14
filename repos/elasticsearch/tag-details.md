<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `elasticsearch`

-	[`elasticsearch:7.17.27`](#elasticsearch71727)
-	[`elasticsearch:8.16.4`](#elasticsearch8164)
-	[`elasticsearch:8.17.2`](#elasticsearch8172)

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
		Last Modified: Fri, 13 Dec 2024 13:08:34 GMT  
		Size: 27.5 MB (27511060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93c168d6ce7e950b0e1cd182e381f48cb7c48f82cb8c1221fa667c88185ce40d`  
		Last Modified: Wed, 15 Jan 2025 01:30:56 GMT  
		Size: 7.5 MB (7524303 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e39dca01aa6a2c5db92b1fa84c84f72ef8ff7fb1dfa28912b085c28ab6a940f`  
		Last Modified: Wed, 15 Jan 2025 01:30:47 GMT  
		Size: 4.3 KB (4312 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc4f5d43e73ad18f9fe6ee3160cb5ac146a0f45b3a5931d994b2ca16f5191bba`  
		Last Modified: Wed, 15 Jan 2025 01:38:59 GMT  
		Size: 327.3 MB (327262495 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97b320e643df90a7dde00d450074c06d660e96ea4624be83dfec160a9279ba67`  
		Last Modified: Wed, 15 Jan 2025 01:38:51 GMT  
		Size: 9.5 KB (9530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11397b40a19fa0054e331a433a7d83d3f392cdf76f5c6e9c55b32c096d790e1c`  
		Last Modified: Wed, 15 Jan 2025 01:38:52 GMT  
		Size: 2.0 KB (1978 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50d429019534b3f9acfe344a6eb0e5408e24bc420b2c7cf285a4b758d51bc77d`  
		Last Modified: Wed, 15 Jan 2025 01:38:53 GMT  
		Size: 192.2 KB (192171 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:280d610f1b7c174b77c13ec7b3d1b7ecc7eae454bfe99982aa18ba68153ce61b`  
		Last Modified: Wed, 15 Jan 2025 01:30:48 GMT  
		Size: 404.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:979b19d45037402335aa40ad65c6e2ecb38e2b210a6bb18c8e6e2a2917e9a2e6`  
		Last Modified: Wed, 15 Jan 2025 01:38:52 GMT  
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
		Last Modified: Wed, 15 Jan 2025 04:00:26 GMT  
		Size: 2.6 MB (2551136 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:21ab10d6870d45a852505fd648d1f7b2a7dcbd9ae7bedda4eec06e75c54f404f`  
		Last Modified: Wed, 15 Jan 2025 01:25:24 GMT  
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
		Last Modified: Fri, 13 Dec 2024 13:25:16 GMT  
		Size: 26.0 MB (25973828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b94b5f7dc63efc97d7aac00f1ff47d685babc6659a830f765d346e5cb09f0019`  
		Last Modified: Tue, 04 Feb 2025 13:40:05 GMT  
		Size: 7.3 MB (7347536 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:045f16f1c1e5b105517c26dd222e1171429bb9894892178df9fe0e63f2783c99`  
		Last Modified: Tue, 04 Feb 2025 08:08:15 GMT  
		Size: 4.3 KB (4319 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a74e1a7409159a1d77dfc2a6a4f71e23748526b42cdb08b99a36783cf988367c`  
		Last Modified: Tue, 04 Feb 2025 13:40:06 GMT  
		Size: 324.9 MB (324925722 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d99d020f552cf790194601796ae1682c5ae838967c42b6fa94d003cd9b902edd`  
		Last Modified: Tue, 04 Feb 2025 15:39:04 GMT  
		Size: 9.1 KB (9096 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8f958882899f954957d771a7e1b7aaf38d3e7bcc711df6e434b41d91a97572a`  
		Last Modified: Tue, 04 Feb 2025 10:21:55 GMT  
		Size: 2.0 KB (1979 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f6d103b20cd3b2147d99a9a9b4cba9e7a73861d36a6616f66b709d8a3b13bda`  
		Last Modified: Tue, 04 Feb 2025 12:31:47 GMT  
		Size: 186.2 KB (186176 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5cce3ada22df59801b30d351ece61b6a95aa7f6d899ed1d4823564f92007cde`  
		Last Modified: Mon, 03 Feb 2025 20:21:58 GMT  
		Size: 404.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39509e1eff1ea51e88403477c0d1cd98b030be538a966cc613bc8ebeb1b512e2`  
		Last Modified: Tue, 04 Feb 2025 11:06:14 GMT  
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
		Last Modified: Fri, 14 Feb 2025 09:09:51 GMT  
		Size: 2.6 MB (2550108 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2ba9c3734d9b4a8163946a0df7ed5e0d7da46bd7889e72dc281aae334703770a`  
		Last Modified: Fri, 14 Feb 2025 09:09:50 GMT  
		Size: 38.1 KB (38090 bytes)  
		MIME: application/vnd.in-toto+json

## `elasticsearch:8.16.4`

```console
$ docker pull elasticsearch@sha256:05726f49bc357f73c5c8a141c2ff6516858ef1b680a4f76defdcf186d574d667
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `elasticsearch:8.16.4` - linux; amd64

```console
$ docker pull elasticsearch@sha256:cd5a0622e342f1453681e77accc75aaeb71d8c791c45ab7b1ff34d0c5b75bbd1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **683.0 MB (683010921 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:78cba68cc0872f2a9e177982c31d120f743f05bda25559140588f9b89a88e82b`
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
# Tue, 11 Feb 2025 12:46:24 GMT
RUN yes no | dpkg-reconfigure dash &&     for iter in 1 2 3 4 5 6 7 8 9 10; do       export DEBIAN_FRONTEND=noninteractive &&       apt-get update &&       apt-get upgrade -y &&       apt-get install -y --no-install-recommends         ca-certificates curl netcat p11-kit unzip zip  &&       apt-get clean &&       rm -rf /var/lib/apt/lists/* &&       exit_code=0 && break ||         exit_code=$? && echo "apt-get error: retry $iter in 10s" && sleep 10;     done;     exit $exit_code # buildkit
# Tue, 11 Feb 2025 12:46:24 GMT
RUN groupadd -g 1000 elasticsearch &&     adduser --uid 1000 --gid 1000 --home /usr/share/elasticsearch elasticsearch &&     adduser elasticsearch root &&     chown -R 0:0 /usr/share/elasticsearch # buildkit
# Tue, 11 Feb 2025 12:46:24 GMT
ENV ELASTIC_CONTAINER=true
# Tue, 11 Feb 2025 12:46:24 GMT
WORKDIR /usr/share/elasticsearch
# Tue, 11 Feb 2025 12:46:24 GMT
COPY --chown=0:0 /usr/share/elasticsearch /usr/share/elasticsearch # buildkit
# Tue, 11 Feb 2025 12:46:24 GMT
COPY --chown=0:0 /bin/tini /bin/tini # buildkit
# Tue, 11 Feb 2025 12:46:24 GMT
ENV PATH=/usr/share/elasticsearch/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 11 Feb 2025 12:46:24 GMT
ENV SHELL=/bin/bash
# Tue, 11 Feb 2025 12:46:24 GMT
COPY bin/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh # buildkit
# Tue, 11 Feb 2025 12:46:24 GMT
RUN chmod g=u /etc/passwd &&     chmod 0555 /usr/local/bin/docker-entrypoint.sh &&     find / -xdev -perm -4000 -exec chmod ug-s {} + &&     chmod 0775 /usr/share/elasticsearch &&     chown elasticsearch bin config config/jvm.options.d data logs plugins # buildkit
# Tue, 11 Feb 2025 12:46:24 GMT
COPY bin/docker-openjdk /etc/ca-certificates/update.d/docker-openjdk # buildkit
# Tue, 11 Feb 2025 12:46:24 GMT
RUN /etc/ca-certificates/update.d/docker-openjdk # buildkit
# Tue, 11 Feb 2025 12:46:24 GMT
EXPOSE map[9200/tcp:{} 9300/tcp:{}]
# Tue, 11 Feb 2025 12:46:24 GMT
LABEL org.label-schema.build-date=2025-02-07T10:10:17.875226338Z org.label-schema.license=Elastic-License-2.0 org.label-schema.name=Elasticsearch org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/elasticsearch org.label-schema.usage=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.label-schema.vcs-ref=3a298fc72352e1b1be92b6619c29d875d64df820 org.label-schema.vcs-url=https://github.com/elastic/elasticsearch org.label-schema.vendor=Elastic org.label-schema.version=8.16.4 org.opencontainers.image.created=2025-02-07T10:10:17.875226338Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.opencontainers.image.licenses=Elastic-License-2.0 org.opencontainers.image.revision=3a298fc72352e1b1be92b6619c29d875d64df820 org.opencontainers.image.source=https://github.com/elastic/elasticsearch org.opencontainers.image.title=Elasticsearch org.opencontainers.image.url=https://www.elastic.co/products/elasticsearch org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=8.16.4
# Tue, 11 Feb 2025 12:46:24 GMT
ENTRYPOINT ["/bin/tini" "--" "/usr/local/bin/docker-entrypoint.sh"]
# Tue, 11 Feb 2025 12:46:24 GMT
CMD ["eswrapper"]
# Tue, 11 Feb 2025 12:46:24 GMT
USER 1000:0
```

-	Layers:
	-	`sha256:d9802f032d6798e2086607424bfe88cb8ec1d6f116e11cd99592dcaf261e9cd2`  
		Last Modified: Fri, 13 Dec 2024 13:08:34 GMT  
		Size: 27.5 MB (27511060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0923e83ea446d3b55881e77557bf0adf4526466a0f8c28e765d96c371a34d977`  
		Last Modified: Wed, 12 Feb 2025 01:40:24 GMT  
		Size: 14.1 MB (14106091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9508592333fbf3623db4f49021845893584e14cfd4d681241fcaa7c86fa213ec`  
		Last Modified: Wed, 12 Feb 2025 00:21:59 GMT  
		Size: 4.3 KB (4318 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5697045fce11fd096e9c7921d68d756b56885a60d5dc6dad1a18419fbbd8f8a6`  
		Last Modified: Wed, 12 Feb 2025 05:34:52 GMT  
		Size: 641.1 MB (641070333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7df35adf5731e58ea0597af653f610469e08251ec197a83d20d9c187a405ea9`  
		Last Modified: Wed, 12 Feb 2025 01:40:24 GMT  
		Size: 9.5 KB (9526 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:863b89ffdc0abe7e1e4883eff81222de68fc4689b6c95b98b03ee30b2dade0c4`  
		Last Modified: Wed, 12 Feb 2025 00:22:03 GMT  
		Size: 1.7 KB (1720 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:511de88caf16cfbe9433bd1602f9e03116ffa62e38be5edba2ec38b3b80dcdbe`  
		Last Modified: Wed, 12 Feb 2025 01:40:26 GMT  
		Size: 191.9 KB (191904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f4d8ea7d344c904ebe364394613be5edc2e1a81a9fc0bdbd45d57b9344ba9a9`  
		Last Modified: Tue, 11 Feb 2025 20:07:47 GMT  
		Size: 405.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f59a251e4851d02e9496c8967a9508cd24a33f1a8de3e2ac7219a385da43b42`  
		Last Modified: Tue, 11 Feb 2025 23:07:31 GMT  
		Size: 115.5 KB (115532 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elasticsearch:8.16.4` - unknown; unknown

```console
$ docker pull elasticsearch@sha256:ce258aa2211169f81f556b9d5a1af8859769b33575c4efdb2ffea2e07f98ac2d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (3042167 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a05ff7d755f7f7e373d6ffff47f6e403923ee37d9578e8e384ecdc1b958aec07`

```dockerfile
```

-	Layers:
	-	`sha256:36136f57df2df965ef3fa06962386bf130ae8a68001610832b49cdad97289245`  
		Last Modified: Wed, 12 Feb 2025 09:02:01 GMT  
		Size: 3.0 MB (3003952 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f7d6b406699951c7e5fe5b69fdfd9561ccf4be7f24c3acb0637e3dce8c5378ae`  
		Last Modified: Wed, 12 Feb 2025 09:02:01 GMT  
		Size: 38.2 KB (38215 bytes)  
		MIME: application/vnd.in-toto+json

### `elasticsearch:8.16.4` - linux; arm64 variant v8

```console
$ docker pull elasticsearch@sha256:79efb8ac0b476634299a0f460bda060f857d88bc55453b47e19777a832dad7d5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **525.3 MB (525285454 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:36fcabf9a43a156c7134fcb9bab252e13fb3e690551687ab4bac9d1b0e8523f8`
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
# Tue, 11 Feb 2025 12:46:24 GMT
RUN yes no | dpkg-reconfigure dash &&     for iter in 1 2 3 4 5 6 7 8 9 10; do       export DEBIAN_FRONTEND=noninteractive &&       apt-get update &&       apt-get upgrade -y &&       apt-get install -y --no-install-recommends         ca-certificates curl netcat p11-kit unzip zip  &&       apt-get clean &&       rm -rf /var/lib/apt/lists/* &&       exit_code=0 && break ||         exit_code=$? && echo "apt-get error: retry $iter in 10s" && sleep 10;     done;     exit $exit_code # buildkit
# Tue, 11 Feb 2025 12:46:24 GMT
RUN groupadd -g 1000 elasticsearch &&     adduser --uid 1000 --gid 1000 --home /usr/share/elasticsearch elasticsearch &&     adduser elasticsearch root &&     chown -R 0:0 /usr/share/elasticsearch # buildkit
# Tue, 11 Feb 2025 12:46:24 GMT
ENV ELASTIC_CONTAINER=true
# Tue, 11 Feb 2025 12:46:24 GMT
WORKDIR /usr/share/elasticsearch
# Tue, 11 Feb 2025 12:46:24 GMT
COPY --chown=0:0 /usr/share/elasticsearch /usr/share/elasticsearch # buildkit
# Tue, 11 Feb 2025 12:46:24 GMT
COPY --chown=0:0 /bin/tini /bin/tini # buildkit
# Tue, 11 Feb 2025 12:46:24 GMT
ENV PATH=/usr/share/elasticsearch/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 11 Feb 2025 12:46:24 GMT
ENV SHELL=/bin/bash
# Tue, 11 Feb 2025 12:46:24 GMT
COPY bin/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh # buildkit
# Tue, 11 Feb 2025 12:46:24 GMT
RUN chmod g=u /etc/passwd &&     chmod 0555 /usr/local/bin/docker-entrypoint.sh &&     find / -xdev -perm -4000 -exec chmod ug-s {} + &&     chmod 0775 /usr/share/elasticsearch &&     chown elasticsearch bin config config/jvm.options.d data logs plugins # buildkit
# Tue, 11 Feb 2025 12:46:24 GMT
COPY bin/docker-openjdk /etc/ca-certificates/update.d/docker-openjdk # buildkit
# Tue, 11 Feb 2025 12:46:24 GMT
RUN /etc/ca-certificates/update.d/docker-openjdk # buildkit
# Tue, 11 Feb 2025 12:46:24 GMT
EXPOSE map[9200/tcp:{} 9300/tcp:{}]
# Tue, 11 Feb 2025 12:46:24 GMT
LABEL org.label-schema.build-date=2025-02-07T10:10:17.875226338Z org.label-schema.license=Elastic-License-2.0 org.label-schema.name=Elasticsearch org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/elasticsearch org.label-schema.usage=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.label-schema.vcs-ref=3a298fc72352e1b1be92b6619c29d875d64df820 org.label-schema.vcs-url=https://github.com/elastic/elasticsearch org.label-schema.vendor=Elastic org.label-schema.version=8.16.4 org.opencontainers.image.created=2025-02-07T10:10:17.875226338Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.opencontainers.image.licenses=Elastic-License-2.0 org.opencontainers.image.revision=3a298fc72352e1b1be92b6619c29d875d64df820 org.opencontainers.image.source=https://github.com/elastic/elasticsearch org.opencontainers.image.title=Elasticsearch org.opencontainers.image.url=https://www.elastic.co/products/elasticsearch org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=8.16.4
# Tue, 11 Feb 2025 12:46:24 GMT
ENTRYPOINT ["/bin/tini" "--" "/usr/local/bin/docker-entrypoint.sh"]
# Tue, 11 Feb 2025 12:46:24 GMT
CMD ["eswrapper"]
# Tue, 11 Feb 2025 12:46:24 GMT
USER 1000:0
```

-	Layers:
	-	`sha256:1b9f3c55f9d4aa5c52eb67a4cb7d0f4726ab85a413b50e3e3fe788befce3d297`  
		Last Modified: Fri, 13 Dec 2024 13:25:16 GMT  
		Size: 26.0 MB (25973828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fe39b5cd905cbae96294eb9d1f2b188f35ad91674daefd5614a1f70c659960d`  
		Last Modified: Tue, 11 Feb 2025 21:20:05 GMT  
		Size: 12.9 MB (12869614 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0caab493f7e6310ac9a1bde88fb0c5648c5c14871ebf32183b33bb8e41acf4cb`  
		Last Modified: Tue, 11 Feb 2025 22:31:50 GMT  
		Size: 4.3 KB (4322 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b706921bda514150853ff55c12dbef27438cbaa5459ba1380a509d41a6ef491b`  
		Last Modified: Wed, 12 Feb 2025 01:50:20 GMT  
		Size: 486.1 MB (486124980 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4709ffddc4fe619c7ac0c7735b29c9dbf920355e427f9c8a6aeed21c190f3b5`  
		Last Modified: Wed, 12 Feb 2025 01:50:10 GMT  
		Size: 9.1 KB (9097 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a6bcf88ceac5f479b6122439a6810aceda6286bf8fd4eca801ede456c65d832`  
		Last Modified: Wed, 12 Feb 2025 03:11:34 GMT  
		Size: 1.7 KB (1721 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75de464ef08bbcf977e2cf1dcdd27ea9f9ee185d0a4e32a9dccb93e5d728cc05`  
		Last Modified: Wed, 12 Feb 2025 07:58:32 GMT  
		Size: 185.9 KB (185918 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a44fd99f39a0ef70dd5472fcfa47a485cafdfd0c9df6818543cba2fcb8d5ee4b`  
		Last Modified: Wed, 12 Feb 2025 01:50:10 GMT  
		Size: 406.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a13f09142c819486918f9fa03ac4f76a397ff9509570755927e1affc09d426a`  
		Last Modified: Wed, 12 Feb 2025 09:16:58 GMT  
		Size: 115.5 KB (115536 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elasticsearch:8.16.4` - unknown; unknown

```console
$ docker pull elasticsearch@sha256:52e4fd4190e483961701825c575828ea2b400fbf5be833c188a2d6abe66175a5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (3041342 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8fdb17ead546e636f4f92eab3a1d46be7678f33f04c48d29df136c8fc0064495`

```dockerfile
```

-	Layers:
	-	`sha256:5cfcbdbb944ca6bebe362c3bf451da0d8f013a2785018c97e0801dc96dccaa16`  
		Last Modified: Wed, 12 Feb 2025 09:02:01 GMT  
		Size: 3.0 MB (3002924 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e6a064e8d7eeb98fcbfbf07f1c8308a015d7048829e15efb9da6069269bcce7d`  
		Last Modified: Wed, 12 Feb 2025 09:02:01 GMT  
		Size: 38.4 KB (38418 bytes)  
		MIME: application/vnd.in-toto+json

## `elasticsearch:8.17.2`

```console
$ docker pull elasticsearch@sha256:f388389127fe71274ff82493748e26677b88ff599785875f088627e0ca0e4c28
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `elasticsearch:8.17.2` - linux; amd64

```console
$ docker pull elasticsearch@sha256:b3f066c9e432d0382088c16505e88f3277f0fb93f76834df18cfac492d0c6224
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **683.9 MB (683944477 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9d10d6cac1d58762e122b085aaf53d51dec2ed579ccb51d543f83de3782e4de4`
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
# Tue, 11 Feb 2025 12:44:29 GMT
RUN yes no | dpkg-reconfigure dash &&     for iter in 1 2 3 4 5 6 7 8 9 10; do       export DEBIAN_FRONTEND=noninteractive &&       apt-get update &&       apt-get upgrade -y &&       apt-get install -y --no-install-recommends         ca-certificates curl netcat p11-kit unzip zip  &&       apt-get clean &&       rm -rf /var/lib/apt/lists/* &&       exit_code=0 && break ||         exit_code=$? && echo "apt-get error: retry $iter in 10s" && sleep 10;     done;     exit $exit_code # buildkit
# Tue, 11 Feb 2025 12:44:29 GMT
RUN groupadd -g 1000 elasticsearch &&     adduser --uid 1000 --gid 1000 --home /usr/share/elasticsearch elasticsearch &&     adduser elasticsearch root &&     chown -R 0:0 /usr/share/elasticsearch # buildkit
# Tue, 11 Feb 2025 12:44:29 GMT
ENV ELASTIC_CONTAINER=true
# Tue, 11 Feb 2025 12:44:29 GMT
WORKDIR /usr/share/elasticsearch
# Tue, 11 Feb 2025 12:44:29 GMT
COPY --chown=0:0 /usr/share/elasticsearch /usr/share/elasticsearch # buildkit
# Tue, 11 Feb 2025 12:44:29 GMT
COPY --chown=0:0 /bin/tini /bin/tini # buildkit
# Tue, 11 Feb 2025 12:44:29 GMT
ENV PATH=/usr/share/elasticsearch/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 11 Feb 2025 12:44:29 GMT
ENV SHELL=/bin/bash
# Tue, 11 Feb 2025 12:44:29 GMT
COPY bin/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh # buildkit
# Tue, 11 Feb 2025 12:44:29 GMT
RUN chmod g=u /etc/passwd &&     chmod 0555 /usr/local/bin/docker-entrypoint.sh &&     find / -xdev -perm -4000 -exec chmod ug-s {} + &&     chmod 0775 /usr/share/elasticsearch &&     chown elasticsearch bin config config/jvm.options.d data logs plugins # buildkit
# Tue, 11 Feb 2025 12:44:29 GMT
COPY bin/docker-openjdk /etc/ca-certificates/update.d/docker-openjdk # buildkit
# Tue, 11 Feb 2025 12:44:29 GMT
RUN /etc/ca-certificates/update.d/docker-openjdk # buildkit
# Tue, 11 Feb 2025 12:44:29 GMT
EXPOSE map[9200/tcp:{} 9300/tcp:{}]
# Tue, 11 Feb 2025 12:44:29 GMT
LABEL org.label-schema.build-date=2025-02-05T22:10:57.067596412Z org.label-schema.license=Elastic-License-2.0 org.label-schema.name=Elasticsearch org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/elasticsearch org.label-schema.usage=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.label-schema.vcs-ref=747663ddda3421467150de0e4301e8d4bc636b0c org.label-schema.vcs-url=https://github.com/elastic/elasticsearch org.label-schema.vendor=Elastic org.label-schema.version=8.17.2 org.opencontainers.image.created=2025-02-05T22:10:57.067596412Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.opencontainers.image.licenses=Elastic-License-2.0 org.opencontainers.image.revision=747663ddda3421467150de0e4301e8d4bc636b0c org.opencontainers.image.source=https://github.com/elastic/elasticsearch org.opencontainers.image.title=Elasticsearch org.opencontainers.image.url=https://www.elastic.co/products/elasticsearch org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=8.17.2
# Tue, 11 Feb 2025 12:44:29 GMT
ENTRYPOINT ["/bin/tini" "--" "/usr/local/bin/docker-entrypoint.sh"]
# Tue, 11 Feb 2025 12:44:29 GMT
CMD ["eswrapper"]
# Tue, 11 Feb 2025 12:44:29 GMT
USER 1000:0
```

-	Layers:
	-	`sha256:d9802f032d6798e2086607424bfe88cb8ec1d6f116e11cd99592dcaf261e9cd2`  
		Last Modified: Fri, 13 Dec 2024 13:08:34 GMT  
		Size: 27.5 MB (27511060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cdf28dceaab4510970118c08d05c11095c02f118c46ec12c0cc792bdb697db7c`  
		Last Modified: Tue, 11 Feb 2025 21:08:16 GMT  
		Size: 14.1 MB (14106276 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5208ce524bb6fbf9f16d0fcd7dd3466c5ab5c8f4642004de284eab34df00db2`  
		Last Modified: Tue, 11 Feb 2025 21:08:11 GMT  
		Size: 4.3 KB (4317 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61d461147a60f05f3c624df3e500a8b330c2702ac6b2fab9fdabaa5725ce2a8d`  
		Last Modified: Tue, 11 Feb 2025 23:09:54 GMT  
		Size: 642.0 MB (642003697 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96bafd1a493acb86f0df3cead3a4f49aef1da22a2c64847ea4a0ac953d9a6ba6`  
		Last Modified: Tue, 11 Feb 2025 21:08:13 GMT  
		Size: 9.5 KB (9528 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:437be7cb1de43f56d69c64dac1ca5869ceba02177f98e52ffca83ca364f86384`  
		Last Modified: Tue, 11 Feb 2025 23:07:56 GMT  
		Size: 1.7 KB (1722 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b343a6636d44dd57773b62971899059f184e673c6209edb5e2f1fa4a5696587`  
		Last Modified: Tue, 11 Feb 2025 21:08:17 GMT  
		Size: 191.9 KB (191906 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c2225bb53581112125c91532112ce2d5b9bd251381fea50e9ad7d87a8dd8785`  
		Last Modified: Tue, 11 Feb 2025 21:08:17 GMT  
		Size: 408.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:990df000a65956dee92efa462d1dadbb961fb88a513d53e6e2a4e246cbda57df`  
		Last Modified: Tue, 11 Feb 2025 21:08:18 GMT  
		Size: 115.5 KB (115531 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elasticsearch:8.17.2` - unknown; unknown

```console
$ docker pull elasticsearch@sha256:554adf640e6b86ab93721facd364aa41710785a77c47a478afb2a7ea5de6274c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (3048365 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4cedfd0ec605bd608585458d96c28947024b965aa4fbc50def41622531a8b418`

```dockerfile
```

-	Layers:
	-	`sha256:4fb224543f6aec6676d16b633fb50ad82ae4e83f8ba1d0637adffb31bd570ce2`  
		Last Modified: Wed, 12 Feb 2025 11:11:41 GMT  
		Size: 3.0 MB (3010152 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b0ea0243d92ac0faa6ca0fdbc8ec079d7587f7f6b65837707987c329e763dfe6`  
		Last Modified: Wed, 12 Feb 2025 09:02:00 GMT  
		Size: 38.2 KB (38213 bytes)  
		MIME: application/vnd.in-toto+json

### `elasticsearch:8.17.2` - linux; arm64 variant v8

```console
$ docker pull elasticsearch@sha256:3a06960b67e8b05c1e0d17874bd1ca59bf36a3ae2a2dade721c2dba3bd897589
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **526.2 MB (526230091 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:18e6114dbf1e1f1677b8085a1cfd94128df8a4f15ed944cc008a8b6d50db91d6`
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
# Tue, 11 Feb 2025 12:44:29 GMT
RUN yes no | dpkg-reconfigure dash &&     for iter in 1 2 3 4 5 6 7 8 9 10; do       export DEBIAN_FRONTEND=noninteractive &&       apt-get update &&       apt-get upgrade -y &&       apt-get install -y --no-install-recommends         ca-certificates curl netcat p11-kit unzip zip  &&       apt-get clean &&       rm -rf /var/lib/apt/lists/* &&       exit_code=0 && break ||         exit_code=$? && echo "apt-get error: retry $iter in 10s" && sleep 10;     done;     exit $exit_code # buildkit
# Tue, 11 Feb 2025 12:44:29 GMT
RUN groupadd -g 1000 elasticsearch &&     adduser --uid 1000 --gid 1000 --home /usr/share/elasticsearch elasticsearch &&     adduser elasticsearch root &&     chown -R 0:0 /usr/share/elasticsearch # buildkit
# Tue, 11 Feb 2025 12:44:29 GMT
ENV ELASTIC_CONTAINER=true
# Tue, 11 Feb 2025 12:44:29 GMT
WORKDIR /usr/share/elasticsearch
# Tue, 11 Feb 2025 12:44:29 GMT
COPY --chown=0:0 /usr/share/elasticsearch /usr/share/elasticsearch # buildkit
# Tue, 11 Feb 2025 12:44:29 GMT
COPY --chown=0:0 /bin/tini /bin/tini # buildkit
# Tue, 11 Feb 2025 12:44:29 GMT
ENV PATH=/usr/share/elasticsearch/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 11 Feb 2025 12:44:29 GMT
ENV SHELL=/bin/bash
# Tue, 11 Feb 2025 12:44:29 GMT
COPY bin/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh # buildkit
# Tue, 11 Feb 2025 12:44:29 GMT
RUN chmod g=u /etc/passwd &&     chmod 0555 /usr/local/bin/docker-entrypoint.sh &&     find / -xdev -perm -4000 -exec chmod ug-s {} + &&     chmod 0775 /usr/share/elasticsearch &&     chown elasticsearch bin config config/jvm.options.d data logs plugins # buildkit
# Tue, 11 Feb 2025 12:44:29 GMT
COPY bin/docker-openjdk /etc/ca-certificates/update.d/docker-openjdk # buildkit
# Tue, 11 Feb 2025 12:44:29 GMT
RUN /etc/ca-certificates/update.d/docker-openjdk # buildkit
# Tue, 11 Feb 2025 12:44:29 GMT
EXPOSE map[9200/tcp:{} 9300/tcp:{}]
# Tue, 11 Feb 2025 12:44:29 GMT
LABEL org.label-schema.build-date=2025-02-05T22:10:57.067596412Z org.label-schema.license=Elastic-License-2.0 org.label-schema.name=Elasticsearch org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/elasticsearch org.label-schema.usage=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.label-schema.vcs-ref=747663ddda3421467150de0e4301e8d4bc636b0c org.label-schema.vcs-url=https://github.com/elastic/elasticsearch org.label-schema.vendor=Elastic org.label-schema.version=8.17.2 org.opencontainers.image.created=2025-02-05T22:10:57.067596412Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.opencontainers.image.licenses=Elastic-License-2.0 org.opencontainers.image.revision=747663ddda3421467150de0e4301e8d4bc636b0c org.opencontainers.image.source=https://github.com/elastic/elasticsearch org.opencontainers.image.title=Elasticsearch org.opencontainers.image.url=https://www.elastic.co/products/elasticsearch org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=8.17.2
# Tue, 11 Feb 2025 12:44:29 GMT
ENTRYPOINT ["/bin/tini" "--" "/usr/local/bin/docker-entrypoint.sh"]
# Tue, 11 Feb 2025 12:44:29 GMT
CMD ["eswrapper"]
# Tue, 11 Feb 2025 12:44:29 GMT
USER 1000:0
```

-	Layers:
	-	`sha256:1b9f3c55f9d4aa5c52eb67a4cb7d0f4726ab85a413b50e3e3fe788befce3d297`  
		Last Modified: Fri, 13 Dec 2024 13:25:16 GMT  
		Size: 26.0 MB (25973828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fe39b5cd905cbae96294eb9d1f2b188f35ad91674daefd5614a1f70c659960d`  
		Last Modified: Tue, 11 Feb 2025 21:20:05 GMT  
		Size: 12.9 MB (12869614 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0caab493f7e6310ac9a1bde88fb0c5648c5c14871ebf32183b33bb8e41acf4cb`  
		Last Modified: Tue, 11 Feb 2025 22:31:50 GMT  
		Size: 4.3 KB (4322 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47431c813b85cecf83530ae0e29b8bf2469460645601d1356ed1c86256633380`  
		Last Modified: Tue, 11 Feb 2025 21:20:21 GMT  
		Size: 487.1 MB (487069625 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:307bfd2984e3b0c2e5165673a4f60c3e842b88b76a4c50b54054c393b5b33d30`  
		Last Modified: Tue, 11 Feb 2025 21:20:23 GMT  
		Size: 9.1 KB (9097 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80bf11b249bc78c5b05395cadd837ab13cd93e1164986ce872123783ef6228d9`  
		Last Modified: Tue, 11 Feb 2025 21:20:24 GMT  
		Size: 1.7 KB (1719 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4ffe7871882bd21fcc9cf7074e75d45daa98b5d29ec651d639477ac5a560f13`  
		Last Modified: Tue, 11 Feb 2025 22:29:41 GMT  
		Size: 185.9 KB (185915 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:334bfa81daffa1eeab07412fd31a4796c27d2fdbdbc4acb98b370e9eaf6f2493`  
		Last Modified: Tue, 11 Feb 2025 21:20:26 GMT  
		Size: 405.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b8f5c821700996c5e3c66e000f8129b004f8caa0e80a542523c433a9de0de83`  
		Last Modified: Tue, 11 Feb 2025 21:20:27 GMT  
		Size: 115.5 KB (115534 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elasticsearch:8.17.2` - unknown; unknown

```console
$ docker pull elasticsearch@sha256:303f8188481ff4f100904c4e314a060f63c716f5e0a654ea7075cba4c9ee98b7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (3047542 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30aac96c5570afca778669e7a344eaeed2d12078bdd3c3e036f276b965f7dee2`

```dockerfile
```

-	Layers:
	-	`sha256:d441b45106d26f321f467c3ef112f629ba11e74147c6f440d2f5009722fd5281`  
		Last Modified: Wed, 12 Feb 2025 03:32:57 GMT  
		Size: 3.0 MB (3009124 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:35ea27ed7149aeba15bfb787929cdf6b1e42ac2a378820337053de38338abe82`  
		Last Modified: Wed, 12 Feb 2025 09:02:00 GMT  
		Size: 38.4 KB (38418 bytes)  
		MIME: application/vnd.in-toto+json
