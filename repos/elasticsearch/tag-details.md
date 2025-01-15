<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `elasticsearch`

-	[`elasticsearch:7.17.27`](#elasticsearch71727)
-	[`elasticsearch:8.16.2`](#elasticsearch8162)
-	[`elasticsearch:8.17.0`](#elasticsearch8170)

## `elasticsearch:7.17.27`

```console
$ docker pull elasticsearch@sha256:91dd552b4889bc61b54a3cdd9533cc11d9ea605d84062754466e84acb505b0ac
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
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

## `elasticsearch:8.16.2`

```console
$ docker pull elasticsearch@sha256:bc9e1b1b840cf580db434ef7e957a8ac089ddd984d709afb410a3dcddced346b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `elasticsearch:8.16.2` - linux; amd64

```console
$ docker pull elasticsearch@sha256:d12e69d934706507e2212c7fbe94ad923e370bddb54b27005a6e539120207644
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **676.4 MB (676417899 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ace4fb95679fd53d63f899735c6ae50fa21db92eb555ffc69983c5c5e0ffd7bd`
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
# Tue, 17 Dec 2024 15:31:13 GMT
RUN yes no | dpkg-reconfigure dash &&     for iter in 1 2 3 4 5 6 7 8 9 10; do       export DEBIAN_FRONTEND=noninteractive &&       apt-get update &&       apt-get upgrade -y &&       apt-get install -y --no-install-recommends         ca-certificates curl netcat p11-kit unzip zip  &&       apt-get clean &&       rm -rf /var/lib/apt/lists/* &&       exit_code=0 && break ||         exit_code=$? && echo "apt-get error: retry $iter in 10s" && sleep 10;     done;     exit $exit_code # buildkit
# Tue, 17 Dec 2024 15:31:13 GMT
RUN groupadd -g 1000 elasticsearch &&     adduser --uid 1000 --gid 1000 --home /usr/share/elasticsearch elasticsearch &&     adduser elasticsearch root &&     chown -R 0:0 /usr/share/elasticsearch # buildkit
# Tue, 17 Dec 2024 15:31:13 GMT
ENV ELASTIC_CONTAINER=true
# Tue, 17 Dec 2024 15:31:13 GMT
WORKDIR /usr/share/elasticsearch
# Tue, 17 Dec 2024 15:31:13 GMT
COPY --chown=0:0 /usr/share/elasticsearch /usr/share/elasticsearch # buildkit
# Tue, 17 Dec 2024 15:31:13 GMT
COPY --chown=0:0 /bin/tini /bin/tini # buildkit
# Tue, 17 Dec 2024 15:31:13 GMT
ENV PATH=/usr/share/elasticsearch/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Dec 2024 15:31:13 GMT
ENV SHELL=/bin/bash
# Tue, 17 Dec 2024 15:31:13 GMT
COPY bin/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh # buildkit
# Tue, 17 Dec 2024 15:31:13 GMT
RUN chmod g=u /etc/passwd &&     chmod 0555 /usr/local/bin/docker-entrypoint.sh &&     find / -xdev -perm -4000 -exec chmod ug-s {} + &&     chmod 0775 /usr/share/elasticsearch &&     chown elasticsearch bin config config/jvm.options.d data logs plugins # buildkit
# Tue, 17 Dec 2024 15:31:13 GMT
COPY bin/docker-openjdk /etc/ca-certificates/update.d/docker-openjdk # buildkit
# Tue, 17 Dec 2024 15:31:13 GMT
RUN /etc/ca-certificates/update.d/docker-openjdk # buildkit
# Tue, 17 Dec 2024 15:31:13 GMT
EXPOSE map[9200/tcp:{} 9300/tcp:{}]
# Tue, 17 Dec 2024 15:31:13 GMT
LABEL org.label-schema.build-date=2024-12-12T10:08:52.873963388Z org.label-schema.license=Elastic-License-2.0 org.label-schema.name=Elasticsearch org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/elasticsearch org.label-schema.usage=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.label-schema.vcs-ref=fc1fb13693e87881046baa93e2cf1f4caf2fd58b org.label-schema.vcs-url=https://github.com/elastic/elasticsearch org.label-schema.vendor=Elastic org.label-schema.version=8.16.2 org.opencontainers.image.created=2024-12-12T10:08:52.873963388Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.opencontainers.image.licenses=Elastic-License-2.0 org.opencontainers.image.revision=fc1fb13693e87881046baa93e2cf1f4caf2fd58b org.opencontainers.image.source=https://github.com/elastic/elasticsearch org.opencontainers.image.title=Elasticsearch org.opencontainers.image.url=https://www.elastic.co/products/elasticsearch org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=8.16.2
# Tue, 17 Dec 2024 15:31:13 GMT
ENTRYPOINT ["/bin/tini" "--" "/usr/local/bin/docker-entrypoint.sh"]
# Tue, 17 Dec 2024 15:31:13 GMT
CMD ["eswrapper"]
# Tue, 17 Dec 2024 15:31:13 GMT
USER 1000:0
```

-	Layers:
	-	`sha256:d9802f032d6798e2086607424bfe88cb8ec1d6f116e11cd99592dcaf261e9cd2`  
		Last Modified: Fri, 11 Oct 2024 04:41:25 GMT  
		Size: 27.5 MB (27511060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c1a2dea2c5c9eaa5af9e0a93ddd999b3d0ce8fb64047a6a3f6e8beede4af40a`  
		Last Modified: Tue, 17 Dec 2024 19:31:00 GMT  
		Size: 7.5 MB (7524210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc42ce4e35ebf8d8bb3dc8c51ad16e324ae44745a6bf4814e57a4d94546932b2`  
		Last Modified: Tue, 17 Dec 2024 19:31:00 GMT  
		Size: 4.3 KB (4317 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43837247ecd24f24824584d99b6d98536a7b969dc63ae454769daa8af6509570`  
		Last Modified: Tue, 17 Dec 2024 19:31:15 GMT  
		Size: 641.1 MB (641059188 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08be9ea1190a64770aa164bddef19cd3dc1d1c717fe1253352ce9b1c9303022a`  
		Last Modified: Tue, 17 Dec 2024 19:31:00 GMT  
		Size: 9.5 KB (9526 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9640d080f0fe9454a624c1627b2ca1187896a16de704fc530d0370247f283127`  
		Last Modified: Tue, 17 Dec 2024 19:31:01 GMT  
		Size: 1.7 KB (1720 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9d4ddeba318098fca243a476f4427470184b8d20b76d0d4fdc77e746aa1b3d3`  
		Last Modified: Tue, 17 Dec 2024 19:31:01 GMT  
		Size: 191.9 KB (191903 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a48ff322ba459255c0decda50df03a306a4423d93d1c4cb0e2f3d9d078b355f`  
		Last Modified: Tue, 17 Dec 2024 19:31:01 GMT  
		Size: 406.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c616d934496a0261974b229425262a530414b31822f3f7250ffcd268a24cf296`  
		Last Modified: Tue, 17 Dec 2024 19:31:02 GMT  
		Size: 115.5 KB (115537 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elasticsearch:8.16.2` - unknown; unknown

```console
$ docker pull elasticsearch@sha256:6881f71ea502ee7e72536fd91056c7944886dbc5b6b699f18f2852fbfc5236df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (3042158 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:417ef527a5d132585bf9642811dcb24d16111550f27ae22217fd3899899a14ef`

```dockerfile
```

-	Layers:
	-	`sha256:4b74b3e83e886154b964cdab3cc8fff7179597fdb6a6a6efd51ed7c9bd3009b2`  
		Last Modified: Tue, 17 Dec 2024 19:31:00 GMT  
		Size: 3.0 MB (3003952 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c99fbe14ccc701d9c166ffbce38027312cb4c9a70cd14cfcfe032be3aed38ec9`  
		Last Modified: Tue, 17 Dec 2024 19:31:00 GMT  
		Size: 38.2 KB (38206 bytes)  
		MIME: application/vnd.in-toto+json

### `elasticsearch:8.16.2` - linux; arm64 variant v8

```console
$ docker pull elasticsearch@sha256:6fea36db837c0db2fb4aa0ecf66e7edfa0d58044016d46bfedef0170543fa5e4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **519.8 MB (519760081 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f03be3320f12a5cb3810cf67257e80e6dc50f0186c2700d98648e71dfd69a752`
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
# Tue, 17 Dec 2024 15:31:13 GMT
RUN yes no | dpkg-reconfigure dash &&     for iter in 1 2 3 4 5 6 7 8 9 10; do       export DEBIAN_FRONTEND=noninteractive &&       apt-get update &&       apt-get upgrade -y &&       apt-get install -y --no-install-recommends         ca-certificates curl netcat p11-kit unzip zip  &&       apt-get clean &&       rm -rf /var/lib/apt/lists/* &&       exit_code=0 && break ||         exit_code=$? && echo "apt-get error: retry $iter in 10s" && sleep 10;     done;     exit $exit_code # buildkit
# Tue, 17 Dec 2024 15:31:13 GMT
RUN groupadd -g 1000 elasticsearch &&     adduser --uid 1000 --gid 1000 --home /usr/share/elasticsearch elasticsearch &&     adduser elasticsearch root &&     chown -R 0:0 /usr/share/elasticsearch # buildkit
# Tue, 17 Dec 2024 15:31:13 GMT
ENV ELASTIC_CONTAINER=true
# Tue, 17 Dec 2024 15:31:13 GMT
WORKDIR /usr/share/elasticsearch
# Tue, 17 Dec 2024 15:31:13 GMT
COPY --chown=0:0 /usr/share/elasticsearch /usr/share/elasticsearch # buildkit
# Tue, 17 Dec 2024 15:31:13 GMT
COPY --chown=0:0 /bin/tini /bin/tini # buildkit
# Tue, 17 Dec 2024 15:31:13 GMT
ENV PATH=/usr/share/elasticsearch/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Dec 2024 15:31:13 GMT
ENV SHELL=/bin/bash
# Tue, 17 Dec 2024 15:31:13 GMT
COPY bin/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh # buildkit
# Tue, 17 Dec 2024 15:31:13 GMT
RUN chmod g=u /etc/passwd &&     chmod 0555 /usr/local/bin/docker-entrypoint.sh &&     find / -xdev -perm -4000 -exec chmod ug-s {} + &&     chmod 0775 /usr/share/elasticsearch &&     chown elasticsearch bin config config/jvm.options.d data logs plugins # buildkit
# Tue, 17 Dec 2024 15:31:13 GMT
COPY bin/docker-openjdk /etc/ca-certificates/update.d/docker-openjdk # buildkit
# Tue, 17 Dec 2024 15:31:13 GMT
RUN /etc/ca-certificates/update.d/docker-openjdk # buildkit
# Tue, 17 Dec 2024 15:31:13 GMT
EXPOSE map[9200/tcp:{} 9300/tcp:{}]
# Tue, 17 Dec 2024 15:31:13 GMT
LABEL org.label-schema.build-date=2024-12-12T10:08:52.873963388Z org.label-schema.license=Elastic-License-2.0 org.label-schema.name=Elasticsearch org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/elasticsearch org.label-schema.usage=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.label-schema.vcs-ref=fc1fb13693e87881046baa93e2cf1f4caf2fd58b org.label-schema.vcs-url=https://github.com/elastic/elasticsearch org.label-schema.vendor=Elastic org.label-schema.version=8.16.2 org.opencontainers.image.created=2024-12-12T10:08:52.873963388Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.opencontainers.image.licenses=Elastic-License-2.0 org.opencontainers.image.revision=fc1fb13693e87881046baa93e2cf1f4caf2fd58b org.opencontainers.image.source=https://github.com/elastic/elasticsearch org.opencontainers.image.title=Elasticsearch org.opencontainers.image.url=https://www.elastic.co/products/elasticsearch org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=8.16.2
# Tue, 17 Dec 2024 15:31:13 GMT
ENTRYPOINT ["/bin/tini" "--" "/usr/local/bin/docker-entrypoint.sh"]
# Tue, 17 Dec 2024 15:31:13 GMT
CMD ["eswrapper"]
# Tue, 17 Dec 2024 15:31:13 GMT
USER 1000:0
```

-	Layers:
	-	`sha256:1b9f3c55f9d4aa5c52eb67a4cb7d0f4726ab85a413b50e3e3fe788befce3d297`  
		Last Modified: Fri, 11 Oct 2024 04:41:30 GMT  
		Size: 26.0 MB (25973828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cfcb4f2689e34c6963eced424e556d32cfb29edfdb45405bce094376452282f1`  
		Last Modified: Tue, 17 Dec 2024 19:31:39 GMT  
		Size: 7.3 MB (7347611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45c3cd9ccbf1c863ff2f0025223aa60d0097f5aa2fd702165f0e9878c9987d3a`  
		Last Modified: Tue, 17 Dec 2024 19:31:38 GMT  
		Size: 4.3 KB (4322 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9fbaf667992011a2199171da441d01c0d4b2ae4970f68801ea0ce30c90b3331`  
		Last Modified: Tue, 17 Dec 2024 19:31:51 GMT  
		Size: 486.1 MB (486121610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f75abdcf3b9414656db3478105e8112b315a5bccf73f272e648141c3e5e447a`  
		Last Modified: Tue, 17 Dec 2024 19:31:39 GMT  
		Size: 9.1 KB (9098 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68d78204905742c5c5088b826c0b8bb3cba5f1d2885214934e474649621451f3`  
		Last Modified: Tue, 17 Dec 2024 19:31:39 GMT  
		Size: 1.7 KB (1721 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e831c0c25436f50a65c901e9fad8e91a56765a3f899f20d93ebfd49641ecfd76`  
		Last Modified: Tue, 17 Dec 2024 19:31:40 GMT  
		Size: 185.9 KB (185919 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52fb8de6e31f3d57c5189b250de2c7ae61ce0f45cf3ee5d4fe24189b9dfe0373`  
		Last Modified: Tue, 17 Dec 2024 19:31:40 GMT  
		Size: 404.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:320e6140595100f6d063ee25be718e8a3272757822d87048f40bd30d624cbb89`  
		Last Modified: Tue, 17 Dec 2024 19:31:41 GMT  
		Size: 115.5 KB (115536 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elasticsearch:8.16.2` - unknown; unknown

```console
$ docker pull elasticsearch@sha256:ec293e013283a3dc439895cebc7f402f323d290282972ab9afdea35a54ec91af
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (3041333 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:da5a28849ddb7f10bb65b8aa19867e7e8868f89ef4ef04ad1f50669bc630e39b`

```dockerfile
```

-	Layers:
	-	`sha256:91a4c524b38342c703d25f42d7f4834dfe47f429a8031c957384cead5c447436`  
		Last Modified: Tue, 17 Dec 2024 19:31:39 GMT  
		Size: 3.0 MB (3002924 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:36ea11f6abb08884e1fb9d9fd040a4b7fcdddd717e91a66e723da0f3ae3b3107`  
		Last Modified: Tue, 17 Dec 2024 19:31:39 GMT  
		Size: 38.4 KB (38409 bytes)  
		MIME: application/vnd.in-toto+json

## `elasticsearch:8.17.0`

```console
$ docker pull elasticsearch@sha256:0681af5779b516b0652df86aa1db52e225f2d4e68bb3a3099534377b7f788739
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `elasticsearch:8.17.0` - linux; amd64

```console
$ docker pull elasticsearch@sha256:632745d3d218cd1091765aa24dc72ce9998daab9a2afb189d9a32923b29c18cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **677.4 MB (677362049 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:da83271bb4fe40d57e8f2ce08f4ba7934906f85eb27d81bdab6dbcfef57f4414`
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
# Mon, 16 Dec 2024 18:48:50 GMT
RUN yes no | dpkg-reconfigure dash &&     for iter in 1 2 3 4 5 6 7 8 9 10; do       export DEBIAN_FRONTEND=noninteractive &&       apt-get update &&       apt-get upgrade -y &&       apt-get install -y --no-install-recommends         ca-certificates curl netcat p11-kit unzip zip  &&       apt-get clean &&       rm -rf /var/lib/apt/lists/* &&       exit_code=0 && break ||         exit_code=$? && echo "apt-get error: retry $iter in 10s" && sleep 10;     done;     exit $exit_code # buildkit
# Mon, 16 Dec 2024 18:48:50 GMT
RUN groupadd -g 1000 elasticsearch &&     adduser --uid 1000 --gid 1000 --home /usr/share/elasticsearch elasticsearch &&     adduser elasticsearch root &&     chown -R 0:0 /usr/share/elasticsearch # buildkit
# Mon, 16 Dec 2024 18:48:50 GMT
ENV ELASTIC_CONTAINER=true
# Mon, 16 Dec 2024 18:48:50 GMT
WORKDIR /usr/share/elasticsearch
# Mon, 16 Dec 2024 18:48:50 GMT
COPY --chown=0:0 /usr/share/elasticsearch /usr/share/elasticsearch # buildkit
# Mon, 16 Dec 2024 18:48:50 GMT
COPY --chown=0:0 /bin/tini /bin/tini # buildkit
# Mon, 16 Dec 2024 18:48:50 GMT
ENV PATH=/usr/share/elasticsearch/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 16 Dec 2024 18:48:50 GMT
ENV SHELL=/bin/bash
# Mon, 16 Dec 2024 18:48:50 GMT
COPY bin/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh # buildkit
# Mon, 16 Dec 2024 18:48:50 GMT
RUN chmod g=u /etc/passwd &&     chmod 0555 /usr/local/bin/docker-entrypoint.sh &&     find / -xdev -perm -4000 -exec chmod ug-s {} + &&     chmod 0775 /usr/share/elasticsearch &&     chown elasticsearch bin config config/jvm.options.d data logs plugins # buildkit
# Mon, 16 Dec 2024 18:48:50 GMT
COPY bin/docker-openjdk /etc/ca-certificates/update.d/docker-openjdk # buildkit
# Mon, 16 Dec 2024 18:48:50 GMT
RUN /etc/ca-certificates/update.d/docker-openjdk # buildkit
# Mon, 16 Dec 2024 18:48:50 GMT
EXPOSE map[9200/tcp:{} 9300/tcp:{}]
# Mon, 16 Dec 2024 18:48:50 GMT
LABEL org.label-schema.build-date=2024-12-11T12:08:05.663969764Z org.label-schema.license=Elastic-License-2.0 org.label-schema.name=Elasticsearch org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/elasticsearch org.label-schema.usage=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.label-schema.vcs-ref=2b6a7fed44faa321997703718f07ee0420804b41 org.label-schema.vcs-url=https://github.com/elastic/elasticsearch org.label-schema.vendor=Elastic org.label-schema.version=8.17.0 org.opencontainers.image.created=2024-12-11T12:08:05.663969764Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.opencontainers.image.licenses=Elastic-License-2.0 org.opencontainers.image.revision=2b6a7fed44faa321997703718f07ee0420804b41 org.opencontainers.image.source=https://github.com/elastic/elasticsearch org.opencontainers.image.title=Elasticsearch org.opencontainers.image.url=https://www.elastic.co/products/elasticsearch org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=8.17.0
# Mon, 16 Dec 2024 18:48:50 GMT
ENTRYPOINT ["/bin/tini" "--" "/usr/local/bin/docker-entrypoint.sh"]
# Mon, 16 Dec 2024 18:48:50 GMT
CMD ["eswrapper"]
# Mon, 16 Dec 2024 18:48:50 GMT
USER 1000:0
```

-	Layers:
	-	`sha256:d9802f032d6798e2086607424bfe88cb8ec1d6f116e11cd99592dcaf261e9cd2`  
		Last Modified: Fri, 11 Oct 2024 04:41:25 GMT  
		Size: 27.5 MB (27511060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b328744a4c64b5b8e873b854b5f8d7678de1fdeb3542b004db5afaf4997124b`  
		Last Modified: Tue, 17 Dec 2024 19:31:18 GMT  
		Size: 7.5 MB (7524335 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2894a47525f71d3f7aee0e93c2d4bed6908bf40cef57a6416c013f987f659f63`  
		Last Modified: Tue, 17 Dec 2024 19:31:17 GMT  
		Size: 4.3 KB (4314 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43fda7a86acacb1f91fd785050203f344100dd542056f470d2247928e98197d4`  
		Last Modified: Tue, 17 Dec 2024 19:31:31 GMT  
		Size: 642.0 MB (642003213 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6535aa65357430a83274c82dff5894f4874fef1a83c485c4d89e4698ad40e04`  
		Last Modified: Tue, 17 Dec 2024 19:31:17 GMT  
		Size: 9.5 KB (9530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24d6219917549bd736ff55b5e8e61b8d3d84da400368dfbd644d8b0d469cb21b`  
		Last Modified: Tue, 17 Dec 2024 19:31:18 GMT  
		Size: 1.7 KB (1724 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51a94653ad0a2d2e1610e5b218583e518be8d5f7f8941f117cb99319f56a40f4`  
		Last Modified: Tue, 17 Dec 2024 19:31:18 GMT  
		Size: 191.9 KB (191905 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:279e0e1bedeb3d25e26893e4bfba1b53f8cc50779e0ec182b3f3997b1d7ba2d8`  
		Last Modified: Tue, 17 Dec 2024 19:31:19 GMT  
		Size: 404.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1868f92bc48f2bb11551075566a0a838a5a2c8328e77192729fdee352416cd8d`  
		Last Modified: Tue, 17 Dec 2024 19:31:19 GMT  
		Size: 115.5 KB (115532 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elasticsearch:8.17.0` - unknown; unknown

```console
$ docker pull elasticsearch@sha256:dc22e8aa656717d49b0a1bd4371e47457997d01a3549e5bea623d359a633946f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (3048358 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f98987046e8c273b4f2a870960a9e401dc941abd7cf4280b82442bff624c6000`

```dockerfile
```

-	Layers:
	-	`sha256:3319222c6ef0e3b25aeb7031a638cae25ec836a87da63c2c0bad1278159dbcb0`  
		Last Modified: Tue, 17 Dec 2024 19:31:17 GMT  
		Size: 3.0 MB (3010152 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:375f0e84cacaba83a340a3d11f7ac30c9e3006510acc1e9399d3199dc83ce4b1`  
		Last Modified: Tue, 17 Dec 2024 19:31:17 GMT  
		Size: 38.2 KB (38206 bytes)  
		MIME: application/vnd.in-toto+json

### `elasticsearch:8.17.0` - linux; arm64 variant v8

```console
$ docker pull elasticsearch@sha256:d4ebc12182dd78bd9125837827907a192a014df15047b1aca8964de4c14ab7fa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **520.7 MB (520700861 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee222e626a6c5cfd7f0c4b4bbde05b4057061048745c75780b4b5dad8c2c9184`
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
# Mon, 16 Dec 2024 18:48:50 GMT
RUN yes no | dpkg-reconfigure dash &&     for iter in 1 2 3 4 5 6 7 8 9 10; do       export DEBIAN_FRONTEND=noninteractive &&       apt-get update &&       apt-get upgrade -y &&       apt-get install -y --no-install-recommends         ca-certificates curl netcat p11-kit unzip zip  &&       apt-get clean &&       rm -rf /var/lib/apt/lists/* &&       exit_code=0 && break ||         exit_code=$? && echo "apt-get error: retry $iter in 10s" && sleep 10;     done;     exit $exit_code # buildkit
# Mon, 16 Dec 2024 18:48:50 GMT
RUN groupadd -g 1000 elasticsearch &&     adduser --uid 1000 --gid 1000 --home /usr/share/elasticsearch elasticsearch &&     adduser elasticsearch root &&     chown -R 0:0 /usr/share/elasticsearch # buildkit
# Mon, 16 Dec 2024 18:48:50 GMT
ENV ELASTIC_CONTAINER=true
# Mon, 16 Dec 2024 18:48:50 GMT
WORKDIR /usr/share/elasticsearch
# Mon, 16 Dec 2024 18:48:50 GMT
COPY --chown=0:0 /usr/share/elasticsearch /usr/share/elasticsearch # buildkit
# Mon, 16 Dec 2024 18:48:50 GMT
COPY --chown=0:0 /bin/tini /bin/tini # buildkit
# Mon, 16 Dec 2024 18:48:50 GMT
ENV PATH=/usr/share/elasticsearch/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 16 Dec 2024 18:48:50 GMT
ENV SHELL=/bin/bash
# Mon, 16 Dec 2024 18:48:50 GMT
COPY bin/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh # buildkit
# Mon, 16 Dec 2024 18:48:50 GMT
RUN chmod g=u /etc/passwd &&     chmod 0555 /usr/local/bin/docker-entrypoint.sh &&     find / -xdev -perm -4000 -exec chmod ug-s {} + &&     chmod 0775 /usr/share/elasticsearch &&     chown elasticsearch bin config config/jvm.options.d data logs plugins # buildkit
# Mon, 16 Dec 2024 18:48:50 GMT
COPY bin/docker-openjdk /etc/ca-certificates/update.d/docker-openjdk # buildkit
# Mon, 16 Dec 2024 18:48:50 GMT
RUN /etc/ca-certificates/update.d/docker-openjdk # buildkit
# Mon, 16 Dec 2024 18:48:50 GMT
EXPOSE map[9200/tcp:{} 9300/tcp:{}]
# Mon, 16 Dec 2024 18:48:50 GMT
LABEL org.label-schema.build-date=2024-12-11T12:08:05.663969764Z org.label-schema.license=Elastic-License-2.0 org.label-schema.name=Elasticsearch org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/elasticsearch org.label-schema.usage=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.label-schema.vcs-ref=2b6a7fed44faa321997703718f07ee0420804b41 org.label-schema.vcs-url=https://github.com/elastic/elasticsearch org.label-schema.vendor=Elastic org.label-schema.version=8.17.0 org.opencontainers.image.created=2024-12-11T12:08:05.663969764Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.opencontainers.image.licenses=Elastic-License-2.0 org.opencontainers.image.revision=2b6a7fed44faa321997703718f07ee0420804b41 org.opencontainers.image.source=https://github.com/elastic/elasticsearch org.opencontainers.image.title=Elasticsearch org.opencontainers.image.url=https://www.elastic.co/products/elasticsearch org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=8.17.0
# Mon, 16 Dec 2024 18:48:50 GMT
ENTRYPOINT ["/bin/tini" "--" "/usr/local/bin/docker-entrypoint.sh"]
# Mon, 16 Dec 2024 18:48:50 GMT
CMD ["eswrapper"]
# Mon, 16 Dec 2024 18:48:50 GMT
USER 1000:0
```

-	Layers:
	-	`sha256:1b9f3c55f9d4aa5c52eb67a4cb7d0f4726ab85a413b50e3e3fe788befce3d297`  
		Last Modified: Fri, 11 Oct 2024 04:41:30 GMT  
		Size: 26.0 MB (25973828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cfcb4f2689e34c6963eced424e556d32cfb29edfdb45405bce094376452282f1`  
		Last Modified: Tue, 17 Dec 2024 19:31:39 GMT  
		Size: 7.3 MB (7347611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45c3cd9ccbf1c863ff2f0025223aa60d0097f5aa2fd702165f0e9878c9987d3a`  
		Last Modified: Tue, 17 Dec 2024 19:31:38 GMT  
		Size: 4.3 KB (4322 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:752d7645cc90e2596f6188451ed461a07330a8b1e1197c29a1c0148ccae5b517`  
		Last Modified: Tue, 17 Dec 2024 19:33:50 GMT  
		Size: 487.1 MB (487062392 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa6a2d371e80bd0ea2c522a5edcc0c8daace182bb46616a6e6117f8ac9581622`  
		Last Modified: Tue, 17 Dec 2024 19:33:40 GMT  
		Size: 9.1 KB (9097 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c3f9c51e4d95f136ba5300ca31fb0b71574de783a8e26bcc5a284dea0031de4`  
		Last Modified: Tue, 17 Dec 2024 19:33:40 GMT  
		Size: 1.7 KB (1720 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:500155f5acc6cec7a2502cf131fc4e3598bafbd50900c5c9de4cbba43ab1a626`  
		Last Modified: Tue, 17 Dec 2024 19:33:40 GMT  
		Size: 185.9 KB (185917 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75cc1fc3ae4b7bd7b5efaf51ffae0e09af0e9406b2312d07d37d54fd98039230`  
		Last Modified: Tue, 17 Dec 2024 19:33:41 GMT  
		Size: 404.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:362d067ed0a6985ba7845f70f209c4fabb74727a9fe664886af950cad6ecb06a`  
		Last Modified: Tue, 17 Dec 2024 19:33:41 GMT  
		Size: 115.5 KB (115538 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elasticsearch:8.17.0` - unknown; unknown

```console
$ docker pull elasticsearch@sha256:960e9d0046247d7a6a9159a181713654df8268e2749e13daa2f733d3538a4966
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (3047533 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:95054969dfac6a61807e1dec7b023ddd428d4bc03f4371df7e4aed023750601a`

```dockerfile
```

-	Layers:
	-	`sha256:29df7f1d03300cb6de1db812d6d6fdde810830ede2ed7d2e2d01e09a96850360`  
		Last Modified: Tue, 17 Dec 2024 19:33:40 GMT  
		Size: 3.0 MB (3009124 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e287ed6f93b4b62b88a4c458131ed644ae8f165155a918137423fe005c1aa7f2`  
		Last Modified: Tue, 17 Dec 2024 19:33:40 GMT  
		Size: 38.4 KB (38409 bytes)  
		MIME: application/vnd.in-toto+json
