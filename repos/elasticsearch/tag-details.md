<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `elasticsearch`

-	[`elasticsearch:7.17.28`](#elasticsearch71728)
-	[`elasticsearch:8.16.5`](#elasticsearch8165)
-	[`elasticsearch:8.17.3`](#elasticsearch8173)

## `elasticsearch:7.17.28`

```console
$ docker pull elasticsearch@sha256:439b99f383a642ae899e584b3b453e71f458bdceef8135f8438098aa5de4d637
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `elasticsearch:7.17.28` - linux; amd64

```console
$ docker pull elasticsearch@sha256:3df196d4ec8817a78287ff8898475ed12f1a888511f3dd123692cd407c169d23
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **370.1 MB (370107261 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8acf440efb39c8732b1d7e6a8abc0db511a75101a218f871bf65b36653ae8856`
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
# Tue, 25 Feb 2025 11:58:14 GMT
RUN yes no | dpkg-reconfigure dash &&     for iter in 1 2 3 4 5 6 7 8 9 10; do       export DEBIAN_FRONTEND=noninteractive &&       apt-get update &&       apt-get upgrade -y &&       apt-get install -y --no-install-recommends         ca-certificates curl netcat p11-kit unzip zip &&       apt-get clean &&       rm -rf /var/lib/apt/lists/* &&       exit_code=0 && break ||         exit_code=$? && echo "apt-get error: retry $iter in 10s" && sleep 10;     done;     exit $exit_code # buildkit
# Tue, 25 Feb 2025 11:58:14 GMT
RUN groupadd -g 1000 elasticsearch &&     adduser --uid 1000 --gid 1000 --home /usr/share/elasticsearch elasticsearch &&     adduser elasticsearch root &&     chown -R 0:0 /usr/share/elasticsearch # buildkit
# Tue, 25 Feb 2025 11:58:14 GMT
ENV ELASTIC_CONTAINER=true
# Tue, 25 Feb 2025 11:58:14 GMT
WORKDIR /usr/share/elasticsearch
# Tue, 25 Feb 2025 11:58:14 GMT
COPY --chown=0:0 /usr/share/elasticsearch /usr/share/elasticsearch # buildkit
# Tue, 25 Feb 2025 11:58:14 GMT
COPY --chown=0:0 /bin/tini /bin/tini # buildkit
# Tue, 25 Feb 2025 11:58:14 GMT
ENV PATH=/usr/share/elasticsearch/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 25 Feb 2025 11:58:14 GMT
COPY bin/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh # buildkit
# Tue, 25 Feb 2025 11:58:14 GMT
RUN chmod g=u /etc/passwd &&     chmod 0555 /usr/local/bin/docker-entrypoint.sh &&     find / -xdev -perm -4000 -exec chmod ug-s {} + &&     chmod 0775 /usr/share/elasticsearch &&     chown elasticsearch bin config config/jvm.options.d data logs plugins # buildkit
# Tue, 25 Feb 2025 11:58:14 GMT
COPY bin/docker-openjdk /etc/ca-certificates/update.d/docker-openjdk # buildkit
# Tue, 25 Feb 2025 11:58:14 GMT
RUN /etc/ca-certificates/update.d/docker-openjdk # buildkit
# Tue, 25 Feb 2025 11:58:14 GMT
EXPOSE map[9200/tcp:{} 9300/tcp:{}]
# Tue, 25 Feb 2025 11:58:14 GMT
LABEL org.label-schema.build-date=2025-02-20T09:05:31.349013687Z org.label-schema.license=Elastic-License-2.0 org.label-schema.name=Elasticsearch org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/elasticsearch org.label-schema.usage=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.label-schema.vcs-ref=139cb5a961d8de68b8e02c45cc47f5289a3623af org.label-schema.vcs-url=https://github.com/elastic/elasticsearch org.label-schema.vendor=Elastic org.label-schema.version=7.17.28 org.opencontainers.image.created=2025-02-20T09:05:31.349013687Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.opencontainers.image.licenses=Elastic-License-2.0 org.opencontainers.image.revision=139cb5a961d8de68b8e02c45cc47f5289a3623af org.opencontainers.image.source=https://github.com/elastic/elasticsearch org.opencontainers.image.title=Elasticsearch org.opencontainers.image.url=https://www.elastic.co/products/elasticsearch org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=7.17.28
# Tue, 25 Feb 2025 11:58:14 GMT
ENTRYPOINT ["/bin/tini" "--" "/usr/local/bin/docker-entrypoint.sh"]
# Tue, 25 Feb 2025 11:58:14 GMT
CMD ["eswrapper"]
```

-	Layers:
	-	`sha256:d9802f032d6798e2086607424bfe88cb8ec1d6f116e11cd99592dcaf261e9cd2`  
		Last Modified: Fri, 11 Oct 2024 04:41:25 GMT  
		Size: 27.5 MB (27511060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4382b85d94cc628c2793b3c9f1d433563eb8ad1e9f57aa05b639b384774953a`  
		Last Modified: Tue, 25 Feb 2025 18:30:24 GMT  
		Size: 15.0 MB (15023210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1cafd153bd33e8607bb733e4f04de328caf10d6bd59a23b4a56ca45a7a835d7`  
		Last Modified: Tue, 25 Feb 2025 18:30:23 GMT  
		Size: 4.3 KB (4319 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1981fdbdc5e2af4a5054289cde430453bcf8c9b6daefd3af2298e0caf37e527d`  
		Last Modified: Tue, 25 Feb 2025 18:30:31 GMT  
		Size: 327.2 MB (327249022 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbe49153941abf6031ab1f8468423e0fd8767436bb4e17bda705d4328ae88fcc`  
		Last Modified: Tue, 25 Feb 2025 18:30:23 GMT  
		Size: 9.5 KB (9530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:835a5aab63438387feeb75d03f58df344ab5c4e56762d6fac2f5086ca88f1952`  
		Last Modified: Tue, 25 Feb 2025 18:30:24 GMT  
		Size: 2.0 KB (1980 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b92674f98b850435a3e6cd10bc9f6b6f716233f0bf95e3e88a8b35b111d59a55`  
		Last Modified: Tue, 25 Feb 2025 18:30:24 GMT  
		Size: 192.2 KB (192171 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1576a962b71b054c58be6c907bfc0bae6fd1a60f6f8a5c9cb9d21d7833d225c`  
		Last Modified: Tue, 25 Feb 2025 18:30:25 GMT  
		Size: 406.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b493097f538ec80cf57a7102e0acc054987e6435c805708f8d72a63a41312194`  
		Last Modified: Tue, 25 Feb 2025 18:30:25 GMT  
		Size: 115.5 KB (115531 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elasticsearch:7.17.28` - unknown; unknown

```console
$ docker pull elasticsearch@sha256:5c1e37825de7e40b4419a762eb2e48222741d59881842a1fe75c5a69ec734374
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2589051 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:602eee219fa90cf316910316ea218e2dd29fba66fd7eeb222f8fb7fad25504e0`

```dockerfile
```

-	Layers:
	-	`sha256:712635d07872f1073b058b642a773e2236391ce0fc76a2889a47d032bd16f271`  
		Last Modified: Tue, 25 Feb 2025 18:30:23 GMT  
		Size: 2.6 MB (2551154 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:297668a6609a5894eff69ab33bc75fdef5938698056b0960e14dedc145010c81`  
		Last Modified: Tue, 25 Feb 2025 18:30:23 GMT  
		Size: 37.9 KB (37897 bytes)  
		MIME: application/vnd.in-toto+json

### `elasticsearch:7.17.28` - linux; arm64 variant v8

```console
$ docker pull elasticsearch@sha256:c1b3d83e3a491ef45b666a1971a7af3a601000aba697fc9bc95267bef9057759
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **365.0 MB (364955657 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e55327d50196b341710a8b4cdf91c0bb05a017b6dc61078c8afe0f09e5571c4`
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
# Tue, 25 Feb 2025 11:58:14 GMT
RUN yes no | dpkg-reconfigure dash &&     for iter in 1 2 3 4 5 6 7 8 9 10; do       export DEBIAN_FRONTEND=noninteractive &&       apt-get update &&       apt-get upgrade -y &&       apt-get install -y --no-install-recommends         ca-certificates curl netcat p11-kit unzip zip &&       apt-get clean &&       rm -rf /var/lib/apt/lists/* &&       exit_code=0 && break ||         exit_code=$? && echo "apt-get error: retry $iter in 10s" && sleep 10;     done;     exit $exit_code # buildkit
# Tue, 25 Feb 2025 11:58:14 GMT
RUN groupadd -g 1000 elasticsearch &&     adduser --uid 1000 --gid 1000 --home /usr/share/elasticsearch elasticsearch &&     adduser elasticsearch root &&     chown -R 0:0 /usr/share/elasticsearch # buildkit
# Tue, 25 Feb 2025 11:58:14 GMT
ENV ELASTIC_CONTAINER=true
# Tue, 25 Feb 2025 11:58:14 GMT
WORKDIR /usr/share/elasticsearch
# Tue, 25 Feb 2025 11:58:14 GMT
COPY --chown=0:0 /usr/share/elasticsearch /usr/share/elasticsearch # buildkit
# Tue, 25 Feb 2025 11:58:14 GMT
COPY --chown=0:0 /bin/tini /bin/tini # buildkit
# Tue, 25 Feb 2025 11:58:14 GMT
ENV PATH=/usr/share/elasticsearch/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 25 Feb 2025 11:58:14 GMT
COPY bin/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh # buildkit
# Tue, 25 Feb 2025 11:58:14 GMT
RUN chmod g=u /etc/passwd &&     chmod 0555 /usr/local/bin/docker-entrypoint.sh &&     find / -xdev -perm -4000 -exec chmod ug-s {} + &&     chmod 0775 /usr/share/elasticsearch &&     chown elasticsearch bin config config/jvm.options.d data logs plugins # buildkit
# Tue, 25 Feb 2025 11:58:14 GMT
COPY bin/docker-openjdk /etc/ca-certificates/update.d/docker-openjdk # buildkit
# Tue, 25 Feb 2025 11:58:14 GMT
RUN /etc/ca-certificates/update.d/docker-openjdk # buildkit
# Tue, 25 Feb 2025 11:58:14 GMT
EXPOSE map[9200/tcp:{} 9300/tcp:{}]
# Tue, 25 Feb 2025 11:58:14 GMT
LABEL org.label-schema.build-date=2025-02-20T09:05:31.349013687Z org.label-schema.license=Elastic-License-2.0 org.label-schema.name=Elasticsearch org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/elasticsearch org.label-schema.usage=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.label-schema.vcs-ref=139cb5a961d8de68b8e02c45cc47f5289a3623af org.label-schema.vcs-url=https://github.com/elastic/elasticsearch org.label-schema.vendor=Elastic org.label-schema.version=7.17.28 org.opencontainers.image.created=2025-02-20T09:05:31.349013687Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.opencontainers.image.licenses=Elastic-License-2.0 org.opencontainers.image.revision=139cb5a961d8de68b8e02c45cc47f5289a3623af org.opencontainers.image.source=https://github.com/elastic/elasticsearch org.opencontainers.image.title=Elasticsearch org.opencontainers.image.url=https://www.elastic.co/products/elasticsearch org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=7.17.28
# Tue, 25 Feb 2025 11:58:14 GMT
ENTRYPOINT ["/bin/tini" "--" "/usr/local/bin/docker-entrypoint.sh"]
# Tue, 25 Feb 2025 11:58:14 GMT
CMD ["eswrapper"]
```

-	Layers:
	-	`sha256:1b9f3c55f9d4aa5c52eb67a4cb7d0f4726ab85a413b50e3e3fe788befce3d297`  
		Last Modified: Fri, 11 Oct 2024 04:41:30 GMT  
		Size: 26.0 MB (25973828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73b133d5c02ffb14a9c6e6ac94c32dadf32f97af646b31c80a855514c4931f4d`  
		Last Modified: Tue, 25 Feb 2025 23:40:34 GMT  
		Size: 13.8 MB (13751417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19d330b7cf948d0f619255ac08f295788e85a820c6e52b67902c9756bcd6c7e8`  
		Last Modified: Tue, 25 Feb 2025 23:40:33 GMT  
		Size: 4.3 KB (4321 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76e89805206fdb8432916dc6560a00ae443669c44d7a09151cb6349c88b484f2`  
		Last Modified: Tue, 25 Feb 2025 23:40:44 GMT  
		Size: 324.9 MB (324912862 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8002871af38cc7be0a2eebf218d126f51c10b412966de90d60a9c5f94f8159be`  
		Last Modified: Tue, 25 Feb 2025 23:40:33 GMT  
		Size: 9.1 KB (9098 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a2669410c65046a62db0ba3df2e88597b2de8bc96dadfcd351033d56e8f336d`  
		Last Modified: Tue, 25 Feb 2025 23:40:34 GMT  
		Size: 2.0 KB (1977 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5bc7747397d0c311890ea63bbc873f60d871d6e4fdd24c861ecb2bd7a2b0d822`  
		Last Modified: Tue, 25 Feb 2025 23:40:34 GMT  
		Size: 186.2 KB (186180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b714e911a00a541bbddb81fab83d24740b31db75953537789eef197eee32ec39`  
		Last Modified: Tue, 25 Feb 2025 23:40:35 GMT  
		Size: 405.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d505b1c53c82d2f484aa0c5c0b57ac1f17d700a7b4334573d9a8397a23f18129`  
		Last Modified: Tue, 25 Feb 2025 23:40:35 GMT  
		Size: 115.5 KB (115537 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elasticsearch:7.17.28` - unknown; unknown

```console
$ docker pull elasticsearch@sha256:c313ff7c830e1e09ccf30164de34db52281bf4cc226d57ddb12c14c1640c10d8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2588225 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:371cfa09214ad38aeed4e2a0a3d9aeb9ee33d0f041c24c4407224aecf3d5a3a2`

```dockerfile
```

-	Layers:
	-	`sha256:991a884ae21011ae96e96f66c15a7e7f0067982813928727d483a3407bfe849b`  
		Last Modified: Tue, 25 Feb 2025 23:40:33 GMT  
		Size: 2.6 MB (2550126 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:596d93db3ab022ef7a4baa58e6ac5e03b4f0c02fd2fd5908b5e7dce3951c27fb`  
		Last Modified: Tue, 25 Feb 2025 23:40:33 GMT  
		Size: 38.1 KB (38099 bytes)  
		MIME: application/vnd.in-toto+json

## `elasticsearch:8.16.5`

```console
$ docker pull elasticsearch@sha256:dc5f014ee6880f0ad9b58f45eb0aebfa1f7f23193db1c6f9550fa56a4e837a3d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `elasticsearch:8.16.5` - linux; amd64

```console
$ docker pull elasticsearch@sha256:8e1a7f3ab587f73054c2380b92af2df98338aa1f7c6496c6f11ba9358dd47b3a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **684.1 MB (684081904 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:113c3757cd55d52a992d64ac737809e0c90749a71090e213df80bf6a3b7222f6`
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
# Tue, 04 Mar 2025 09:16:27 GMT
RUN yes no | dpkg-reconfigure dash &&     for iter in 1 2 3 4 5 6 7 8 9 10; do       export DEBIAN_FRONTEND=noninteractive &&       apt-get update &&       apt-get upgrade -y &&       apt-get install -y --no-install-recommends         ca-certificates curl netcat p11-kit unzip zip  &&       apt-get clean &&       rm -rf /var/lib/apt/lists/* &&       exit_code=0 && break ||         exit_code=$? && echo "apt-get error: retry $iter in 10s" && sleep 10;     done;     exit $exit_code # buildkit
# Tue, 04 Mar 2025 09:16:27 GMT
RUN groupadd -g 1000 elasticsearch &&     adduser --uid 1000 --gid 1000 --home /usr/share/elasticsearch elasticsearch &&     adduser elasticsearch root &&     chown -R 0:0 /usr/share/elasticsearch # buildkit
# Tue, 04 Mar 2025 09:16:27 GMT
ENV ELASTIC_CONTAINER=true
# Tue, 04 Mar 2025 09:16:27 GMT
WORKDIR /usr/share/elasticsearch
# Tue, 04 Mar 2025 09:16:27 GMT
COPY --chown=0:0 /usr/share/elasticsearch /usr/share/elasticsearch # buildkit
# Tue, 04 Mar 2025 09:16:27 GMT
COPY --chown=0:0 /bin/tini /bin/tini # buildkit
# Tue, 04 Mar 2025 09:16:27 GMT
ENV PATH=/usr/share/elasticsearch/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Mar 2025 09:16:27 GMT
ENV SHELL=/bin/bash
# Tue, 04 Mar 2025 09:16:27 GMT
COPY bin/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh # buildkit
# Tue, 04 Mar 2025 09:16:27 GMT
RUN chmod g=u /etc/passwd &&     chmod 0555 /usr/local/bin/docker-entrypoint.sh &&     find / -xdev -perm -4000 -exec chmod ug-s {} + &&     chmod 0775 /usr/share/elasticsearch &&     chown elasticsearch bin config config/jvm.options.d data logs plugins # buildkit
# Tue, 04 Mar 2025 09:16:27 GMT
COPY bin/docker-openjdk /etc/ca-certificates/update.d/docker-openjdk # buildkit
# Tue, 04 Mar 2025 09:16:27 GMT
RUN /etc/ca-certificates/update.d/docker-openjdk # buildkit
# Tue, 04 Mar 2025 09:16:27 GMT
EXPOSE map[9200/tcp:{} 9300/tcp:{}]
# Tue, 04 Mar 2025 09:16:27 GMT
LABEL org.label-schema.build-date=2025-02-27T22:08:27.576465563Z org.label-schema.license=Elastic-License-2.0 org.label-schema.name=Elasticsearch org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/elasticsearch org.label-schema.usage=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.label-schema.vcs-ref=23fb957e211507e96c6295abfb74d12abff3a2ea org.label-schema.vcs-url=https://github.com/elastic/elasticsearch org.label-schema.vendor=Elastic org.label-schema.version=8.16.5 org.opencontainers.image.created=2025-02-27T22:08:27.576465563Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.opencontainers.image.licenses=Elastic-License-2.0 org.opencontainers.image.revision=23fb957e211507e96c6295abfb74d12abff3a2ea org.opencontainers.image.source=https://github.com/elastic/elasticsearch org.opencontainers.image.title=Elasticsearch org.opencontainers.image.url=https://www.elastic.co/products/elasticsearch org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=8.16.5
# Tue, 04 Mar 2025 09:16:27 GMT
ENTRYPOINT ["/bin/tini" "--" "/usr/local/bin/docker-entrypoint.sh"]
# Tue, 04 Mar 2025 09:16:27 GMT
CMD ["eswrapper"]
# Tue, 04 Mar 2025 09:16:27 GMT
USER 1000:0
```

-	Layers:
	-	`sha256:d9802f032d6798e2086607424bfe88cb8ec1d6f116e11cd99592dcaf261e9cd2`  
		Last Modified: Fri, 11 Oct 2024 04:41:25 GMT  
		Size: 27.5 MB (27511060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7effd18f5fc7ca51d3f115b830ef5ec53e5a8e70c224b82b9d2c35a872e9e0f`  
		Last Modified: Tue, 04 Mar 2025 21:59:04 GMT  
		Size: 15.0 MB (15023347 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:267cab83b589675749ee87e725dfe4539ad6c91f08ff342c957e2e02ac36c934`  
		Last Modified: Tue, 04 Mar 2025 21:59:03 GMT  
		Size: 4.3 KB (4318 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4385e712411f95459cd7557218e2b00ff8c652fc3c26aa8df513b7eb77f3511`  
		Last Modified: Tue, 04 Mar 2025 21:59:13 GMT  
		Size: 641.2 MB (641224056 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80a3b9d377b7db77096f747a514d7a6982cd51da748c09d410ef1d47c64285ef`  
		Last Modified: Tue, 04 Mar 2025 21:59:04 GMT  
		Size: 9.5 KB (9528 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e665ce0c1d2a6c51cd4418af939ad6443d728e72c0ba599ead9da419e144ef3`  
		Last Modified: Tue, 04 Mar 2025 21:59:04 GMT  
		Size: 1.7 KB (1722 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee42242ce056d3f83058b3dcd522dddb6ec007f13ab77182be77498deae12608`  
		Last Modified: Tue, 04 Mar 2025 21:59:04 GMT  
		Size: 191.9 KB (191902 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fbf241f511c111ecaa3b5ffe825b3de868c06ee2d2cdb64bf0f4d34ed793260`  
		Last Modified: Tue, 04 Mar 2025 21:59:05 GMT  
		Size: 404.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2681affc9848eb7dcd85db6a412a226bfbb2043fbe52f6af70967072dba6e8e2`  
		Last Modified: Tue, 04 Mar 2025 21:59:05 GMT  
		Size: 115.5 KB (115535 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elasticsearch:8.16.5` - unknown; unknown

```console
$ docker pull elasticsearch@sha256:a977c4ff5b26ac18cde7e19ad8601e6ebc73794e4363145b847ffa6ebc3180e0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (3040299 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c686624407e102636e40f731348c6ae35b10aaa626747d6e573e5747f84f29f2`

```dockerfile
```

-	Layers:
	-	`sha256:f1b657fad4a197367225035cd88835ec02a8340297bf74184af2f19a1029ac5f`  
		Last Modified: Tue, 04 Mar 2025 21:59:04 GMT  
		Size: 3.0 MB (3002084 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6892875d86fc19388e58594398068725ccdae272e75318fb295708a58ddf1b99`  
		Last Modified: Tue, 04 Mar 2025 21:59:03 GMT  
		Size: 38.2 KB (38215 bytes)  
		MIME: application/vnd.in-toto+json

## `elasticsearch:8.17.3`

```console
$ docker pull elasticsearch@sha256:4ff0bde47c709a02489fd0fd3f07c834c92826c0d2bcbae6fbdd32dee2872b9b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `elasticsearch:8.17.3` - linux; amd64

```console
$ docker pull elasticsearch@sha256:934ea65eb8967b72086b2449b46f5bd4d63475a02e7ec6f246f6e054d3136137
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **685.0 MB (684996499 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe65524de8716eefcf19e9d91e0f7368a6726520e5ecdc66edd7d74ad20be70e`
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
# Tue, 04 Mar 2025 09:12:50 GMT
RUN yes no | dpkg-reconfigure dash &&     for iter in 1 2 3 4 5 6 7 8 9 10; do       export DEBIAN_FRONTEND=noninteractive &&       apt-get update &&       apt-get upgrade -y &&       apt-get install -y --no-install-recommends         ca-certificates curl netcat p11-kit unzip zip  &&       apt-get clean &&       rm -rf /var/lib/apt/lists/* &&       exit_code=0 && break ||         exit_code=$? && echo "apt-get error: retry $iter in 10s" && sleep 10;     done;     exit $exit_code # buildkit
# Tue, 04 Mar 2025 09:12:50 GMT
RUN groupadd -g 1000 elasticsearch &&     adduser --uid 1000 --gid 1000 --home /usr/share/elasticsearch elasticsearch &&     adduser elasticsearch root &&     chown -R 0:0 /usr/share/elasticsearch # buildkit
# Tue, 04 Mar 2025 09:12:50 GMT
ENV ELASTIC_CONTAINER=true
# Tue, 04 Mar 2025 09:12:50 GMT
WORKDIR /usr/share/elasticsearch
# Tue, 04 Mar 2025 09:12:50 GMT
COPY --chown=0:0 /usr/share/elasticsearch /usr/share/elasticsearch # buildkit
# Tue, 04 Mar 2025 09:12:50 GMT
COPY --chown=0:0 /bin/tini /bin/tini # buildkit
# Tue, 04 Mar 2025 09:12:50 GMT
ENV PATH=/usr/share/elasticsearch/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Mar 2025 09:12:50 GMT
ENV SHELL=/bin/bash
# Tue, 04 Mar 2025 09:12:50 GMT
COPY bin/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh # buildkit
# Tue, 04 Mar 2025 09:12:50 GMT
RUN chmod g=u /etc/passwd &&     chmod 0555 /usr/local/bin/docker-entrypoint.sh &&     find / -xdev -perm -4000 -exec chmod ug-s {} + &&     chmod 0775 /usr/share/elasticsearch &&     chown elasticsearch bin config config/jvm.options.d data logs plugins # buildkit
# Tue, 04 Mar 2025 09:12:50 GMT
COPY bin/docker-openjdk /etc/ca-certificates/update.d/docker-openjdk # buildkit
# Tue, 04 Mar 2025 09:12:50 GMT
RUN /etc/ca-certificates/update.d/docker-openjdk # buildkit
# Tue, 04 Mar 2025 09:12:50 GMT
EXPOSE map[9200/tcp:{} 9300/tcp:{}]
# Tue, 04 Mar 2025 09:12:50 GMT
LABEL org.label-schema.build-date=2025-02-28T10:07:26.089129809Z org.label-schema.license=Elastic-License-2.0 org.label-schema.name=Elasticsearch org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/elasticsearch org.label-schema.usage=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.label-schema.vcs-ref=a091390de485bd4b127884f7e565c0cad59b10d2 org.label-schema.vcs-url=https://github.com/elastic/elasticsearch org.label-schema.vendor=Elastic org.label-schema.version=8.17.3 org.opencontainers.image.created=2025-02-28T10:07:26.089129809Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.opencontainers.image.licenses=Elastic-License-2.0 org.opencontainers.image.revision=a091390de485bd4b127884f7e565c0cad59b10d2 org.opencontainers.image.source=https://github.com/elastic/elasticsearch org.opencontainers.image.title=Elasticsearch org.opencontainers.image.url=https://www.elastic.co/products/elasticsearch org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=8.17.3
# Tue, 04 Mar 2025 09:12:50 GMT
ENTRYPOINT ["/bin/tini" "--" "/usr/local/bin/docker-entrypoint.sh"]
# Tue, 04 Mar 2025 09:12:50 GMT
CMD ["eswrapper"]
# Tue, 04 Mar 2025 09:12:50 GMT
USER 1000:0
```

-	Layers:
	-	`sha256:d9802f032d6798e2086607424bfe88cb8ec1d6f116e11cd99592dcaf261e9cd2`  
		Last Modified: Fri, 11 Oct 2024 04:41:25 GMT  
		Size: 27.5 MB (27511060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f719964e8d43284f2340b13859bc90669efbd620a45af14f94c19b213552cfce`  
		Last Modified: Tue, 04 Mar 2025 21:58:57 GMT  
		Size: 15.0 MB (15023311 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f06e940b3b3959a6212c055a8e0e88de1ee3ddc61574752c627d1a518b0a6e63`  
		Last Modified: Tue, 04 Mar 2025 21:58:57 GMT  
		Size: 4.3 KB (4315 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d49c241623ab94230412ee25d710f6f2b48db5e31488c4b93cb2c0223a9c61b`  
		Last Modified: Tue, 04 Mar 2025 21:59:07 GMT  
		Size: 642.1 MB (642138693 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9d8638aebd426d095e25ebb215e826b03053d2af9f1d952119b4fe568b2dd33`  
		Last Modified: Tue, 04 Mar 2025 21:58:57 GMT  
		Size: 9.5 KB (9528 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e667da6aebf50c45a7614c1e0d21cc77821dcb5f7aa797c1b3c4b95d48ee1a9d`  
		Last Modified: Tue, 04 Mar 2025 21:58:58 GMT  
		Size: 1.7 KB (1723 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:611b553eec4300af63a06592c57d988a5623bd41739d49e13b33f9ac95391ddd`  
		Last Modified: Tue, 04 Mar 2025 21:58:58 GMT  
		Size: 191.9 KB (191900 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc126464efb14a2e371c553705c19e0ec8e93794b5c0abf5a3c56591671e306d`  
		Last Modified: Tue, 04 Mar 2025 21:58:59 GMT  
		Size: 405.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71e490af130ddb378e2ea7a5de3e8768799602b90f359be4e33e1ed8fe185990`  
		Last Modified: Tue, 04 Mar 2025 21:58:59 GMT  
		Size: 115.5 KB (115532 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elasticsearch:8.17.3` - unknown; unknown

```console
$ docker pull elasticsearch@sha256:1d37aa1a7628d6c04281a500e5d8e8f6586edf320de15c120f257a2dbff6646a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (3046499 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fae0df6a93eea7dd90e5dcedc5b29e2dd23d29f47a050db61ef2987047247f2d`

```dockerfile
```

-	Layers:
	-	`sha256:b087ea09d1f56b012c4ce0ccb4af95697a2c91ec8e1fd0a40e00004535e22839`  
		Last Modified: Tue, 04 Mar 2025 21:58:57 GMT  
		Size: 3.0 MB (3008284 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ddb58c0de0bd4d6796e734c1c639739b2941ac638f4b491578ce45e155c12480`  
		Last Modified: Tue, 04 Mar 2025 21:58:57 GMT  
		Size: 38.2 KB (38215 bytes)  
		MIME: application/vnd.in-toto+json
