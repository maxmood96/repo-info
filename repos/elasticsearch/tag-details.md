<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `elasticsearch`

-	[`elasticsearch:7.17.28`](#elasticsearch71728)
-	[`elasticsearch:8.16.6`](#elasticsearch8166)
-	[`elasticsearch:8.17.4`](#elasticsearch8174)

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

## `elasticsearch:8.16.6`

```console
$ docker pull elasticsearch@sha256:fab89d1647c5aee3c060e42e2fff3c69c542c8981fdbea921a9f9d7dafe272e6
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `elasticsearch:8.16.6` - linux; amd64

```console
$ docker pull elasticsearch@sha256:80d50947170cec574185b15f5d32ff9a65386b91b91daf0f20095df8d79aa482
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **684.1 MB (684115511 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cea02a35bbc4fa4b2ea844d00f5429b552f23bdc98daf27151a871f1cf47f262`
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
# Tue, 25 Mar 2025 08:54:09 GMT
RUN yes no | dpkg-reconfigure dash &&     for iter in 1 2 3 4 5 6 7 8 9 10; do       export DEBIAN_FRONTEND=noninteractive &&       apt-get update &&       apt-get upgrade -y &&       apt-get install -y --no-install-recommends         ca-certificates curl netcat p11-kit unzip zip  &&       apt-get clean &&       rm -rf /var/lib/apt/lists/* &&       exit_code=0 && break ||         exit_code=$? && echo "apt-get error: retry $iter in 10s" && sleep 10;     done;     exit $exit_code # buildkit
# Tue, 25 Mar 2025 08:54:09 GMT
RUN groupadd -g 1000 elasticsearch &&     adduser --uid 1000 --gid 1000 --home /usr/share/elasticsearch elasticsearch &&     adduser elasticsearch root &&     chown -R 0:0 /usr/share/elasticsearch # buildkit
# Tue, 25 Mar 2025 08:54:09 GMT
ENV ELASTIC_CONTAINER=true
# Tue, 25 Mar 2025 08:54:09 GMT
WORKDIR /usr/share/elasticsearch
# Tue, 25 Mar 2025 08:54:09 GMT
COPY --chown=0:0 /usr/share/elasticsearch /usr/share/elasticsearch # buildkit
# Tue, 25 Mar 2025 08:54:09 GMT
COPY --chown=0:0 /bin/tini /bin/tini # buildkit
# Tue, 25 Mar 2025 08:54:09 GMT
ENV PATH=/usr/share/elasticsearch/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 25 Mar 2025 08:54:09 GMT
ENV SHELL=/bin/bash
# Tue, 25 Mar 2025 08:54:09 GMT
COPY bin/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh # buildkit
# Tue, 25 Mar 2025 08:54:09 GMT
RUN chmod g=u /etc/passwd &&     chmod 0555 /usr/local/bin/docker-entrypoint.sh &&     find / -xdev -perm -4000 -exec chmod ug-s {} + &&     chmod 0775 /usr/share/elasticsearch &&     chown elasticsearch bin config config/jvm.options.d data logs plugins # buildkit
# Tue, 25 Mar 2025 08:54:09 GMT
COPY bin/docker-openjdk /etc/ca-certificates/update.d/docker-openjdk # buildkit
# Tue, 25 Mar 2025 08:54:09 GMT
RUN /etc/ca-certificates/update.d/docker-openjdk # buildkit
# Tue, 25 Mar 2025 08:54:09 GMT
EXPOSE map[9200/tcp:{} 9300/tcp:{}]
# Tue, 25 Mar 2025 08:54:09 GMT
LABEL org.label-schema.build-date=2025-03-20T10:07:27.754027795Z org.label-schema.license=Elastic-License-2.0 org.label-schema.name=Elasticsearch org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/elasticsearch org.label-schema.usage=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.label-schema.vcs-ref=2eabb32aee47ed0c4ba71c169f098d0379402efe org.label-schema.vcs-url=https://github.com/elastic/elasticsearch org.label-schema.vendor=Elastic org.label-schema.version=8.16.6 org.opencontainers.image.created=2025-03-20T10:07:27.754027795Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.opencontainers.image.licenses=Elastic-License-2.0 org.opencontainers.image.revision=2eabb32aee47ed0c4ba71c169f098d0379402efe org.opencontainers.image.source=https://github.com/elastic/elasticsearch org.opencontainers.image.title=Elasticsearch org.opencontainers.image.url=https://www.elastic.co/products/elasticsearch org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=8.16.6
# Tue, 25 Mar 2025 08:54:09 GMT
ENTRYPOINT ["/bin/tini" "--" "/usr/local/bin/docker-entrypoint.sh"]
# Tue, 25 Mar 2025 08:54:09 GMT
CMD ["eswrapper"]
# Tue, 25 Mar 2025 08:54:09 GMT
USER 1000:0
```

-	Layers:
	-	`sha256:d9802f032d6798e2086607424bfe88cb8ec1d6f116e11cd99592dcaf261e9cd2`  
		Last Modified: Fri, 11 Oct 2024 04:41:25 GMT  
		Size: 27.5 MB (27511060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4cefb614df1d196510a8514e59f550b1908f8b0f23d816dfb1bc9be6a5bbfc64`  
		Last Modified: Tue, 25 Mar 2025 19:44:36 GMT  
		Size: 15.0 MB (15023398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d7a8238779180400c74046a2aa06c9332706ea10f4bb1bec782ee7bee35be83`  
		Last Modified: Tue, 25 Mar 2025 19:44:35 GMT  
		Size: 4.3 KB (4317 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:235c741554d7a669b591f8a2d4770c6945f38d821c36f9ebb114a11c4da334e3`  
		Last Modified: Tue, 25 Mar 2025 19:44:49 GMT  
		Size: 641.3 MB (641257615 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f1b3c286095528d94d60d9a8cdf7cf65fb0bbfe2b2d27ea53ae8d6581f50a5b`  
		Last Modified: Tue, 25 Mar 2025 19:44:35 GMT  
		Size: 9.5 KB (9527 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ab0cc76c041c3c429d7d750691c148a624e6df396e8de73e0725bb286423ab1`  
		Last Modified: Tue, 25 Mar 2025 19:44:36 GMT  
		Size: 1.7 KB (1723 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54f292d2926990eefd0fcccf74ab752b3238d75efe59272c6700bc19e1e38a68`  
		Last Modified: Tue, 25 Mar 2025 19:44:36 GMT  
		Size: 191.9 KB (191901 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4751e956700c3e26afd60aabf81a80cdb7ea8bebabd40be3d3d104d6550a94b0`  
		Last Modified: Tue, 25 Mar 2025 19:44:37 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:991bc540f612bd6630ffb2b3cce7b16d6dd75d2af02003a3d2b4270446ea809b`  
		Last Modified: Tue, 25 Mar 2025 19:44:37 GMT  
		Size: 115.5 KB (115535 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elasticsearch:8.16.6` - unknown; unknown

```console
$ docker pull elasticsearch@sha256:6342c3563d81f668bdcf22cd571a7af39eef0923bf0f2b91c20447d8d7fd53e6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (3040875 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:591d375cbfe440b8600cf85f8087f4218d1f3c32817c46adee55986b2e514cf2`

```dockerfile
```

-	Layers:
	-	`sha256:1d5b8dee3a4af711784e4d0a95415b3653147fef4b1648074fe602ce8860a185`  
		Last Modified: Tue, 25 Mar 2025 19:44:35 GMT  
		Size: 3.0 MB (3002661 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d38e14b2c6de3cbd277faced29a2d61acf649f444c8ed48d2d2ba46849aa2349`  
		Last Modified: Tue, 25 Mar 2025 19:44:35 GMT  
		Size: 38.2 KB (38214 bytes)  
		MIME: application/vnd.in-toto+json

### `elasticsearch:8.16.6` - linux; arm64 variant v8

```console
$ docker pull elasticsearch@sha256:46361de8b04efa356a763b1f30be384817e55e585674be8da247e44988844ef8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **526.4 MB (526366510 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e63269b9fd03952ca052032714d6750fc3bd1774250b911438d25e5621e830e8`
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
# Tue, 25 Mar 2025 08:54:09 GMT
RUN yes no | dpkg-reconfigure dash &&     for iter in 1 2 3 4 5 6 7 8 9 10; do       export DEBIAN_FRONTEND=noninteractive &&       apt-get update &&       apt-get upgrade -y &&       apt-get install -y --no-install-recommends         ca-certificates curl netcat p11-kit unzip zip  &&       apt-get clean &&       rm -rf /var/lib/apt/lists/* &&       exit_code=0 && break ||         exit_code=$? && echo "apt-get error: retry $iter in 10s" && sleep 10;     done;     exit $exit_code # buildkit
# Tue, 25 Mar 2025 08:54:09 GMT
RUN groupadd -g 1000 elasticsearch &&     adduser --uid 1000 --gid 1000 --home /usr/share/elasticsearch elasticsearch &&     adduser elasticsearch root &&     chown -R 0:0 /usr/share/elasticsearch # buildkit
# Tue, 25 Mar 2025 08:54:09 GMT
ENV ELASTIC_CONTAINER=true
# Tue, 25 Mar 2025 08:54:09 GMT
WORKDIR /usr/share/elasticsearch
# Tue, 25 Mar 2025 08:54:09 GMT
COPY --chown=0:0 /usr/share/elasticsearch /usr/share/elasticsearch # buildkit
# Tue, 25 Mar 2025 08:54:09 GMT
COPY --chown=0:0 /bin/tini /bin/tini # buildkit
# Tue, 25 Mar 2025 08:54:09 GMT
ENV PATH=/usr/share/elasticsearch/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 25 Mar 2025 08:54:09 GMT
ENV SHELL=/bin/bash
# Tue, 25 Mar 2025 08:54:09 GMT
COPY bin/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh # buildkit
# Tue, 25 Mar 2025 08:54:09 GMT
RUN chmod g=u /etc/passwd &&     chmod 0555 /usr/local/bin/docker-entrypoint.sh &&     find / -xdev -perm -4000 -exec chmod ug-s {} + &&     chmod 0775 /usr/share/elasticsearch &&     chown elasticsearch bin config config/jvm.options.d data logs plugins # buildkit
# Tue, 25 Mar 2025 08:54:09 GMT
COPY bin/docker-openjdk /etc/ca-certificates/update.d/docker-openjdk # buildkit
# Tue, 25 Mar 2025 08:54:09 GMT
RUN /etc/ca-certificates/update.d/docker-openjdk # buildkit
# Tue, 25 Mar 2025 08:54:09 GMT
EXPOSE map[9200/tcp:{} 9300/tcp:{}]
# Tue, 25 Mar 2025 08:54:09 GMT
LABEL org.label-schema.build-date=2025-03-20T10:07:27.754027795Z org.label-schema.license=Elastic-License-2.0 org.label-schema.name=Elasticsearch org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/elasticsearch org.label-schema.usage=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.label-schema.vcs-ref=2eabb32aee47ed0c4ba71c169f098d0379402efe org.label-schema.vcs-url=https://github.com/elastic/elasticsearch org.label-schema.vendor=Elastic org.label-schema.version=8.16.6 org.opencontainers.image.created=2025-03-20T10:07:27.754027795Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.opencontainers.image.licenses=Elastic-License-2.0 org.opencontainers.image.revision=2eabb32aee47ed0c4ba71c169f098d0379402efe org.opencontainers.image.source=https://github.com/elastic/elasticsearch org.opencontainers.image.title=Elasticsearch org.opencontainers.image.url=https://www.elastic.co/products/elasticsearch org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=8.16.6
# Tue, 25 Mar 2025 08:54:09 GMT
ENTRYPOINT ["/bin/tini" "--" "/usr/local/bin/docker-entrypoint.sh"]
# Tue, 25 Mar 2025 08:54:09 GMT
CMD ["eswrapper"]
# Tue, 25 Mar 2025 08:54:09 GMT
USER 1000:0
```

-	Layers:
	-	`sha256:1b9f3c55f9d4aa5c52eb67a4cb7d0f4726ab85a413b50e3e3fe788befce3d297`  
		Last Modified: Fri, 11 Oct 2024 04:41:30 GMT  
		Size: 26.0 MB (25973828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e5c2366281558c3fd6d4aa155d04ace1d089bf5eddaa8f02d51dedadf212541`  
		Last Modified: Tue, 25 Mar 2025 19:44:24 GMT  
		Size: 13.8 MB (13751835 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0287c434f4bcc57ce95e84644d46ac9e8f3f4fa25e320e2a6d77508895a40175`  
		Last Modified: Tue, 25 Mar 2025 19:44:23 GMT  
		Size: 4.3 KB (4318 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c7a14a9b09d7b4dce65d0d019b91129bd64364d04be6c066a41ccaa46e13635`  
		Last Modified: Tue, 25 Mar 2025 19:44:33 GMT  
		Size: 486.3 MB (486323822 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b206641e45ee45a3d961b5b2ab1318cf491b64cb51da5eb310639795206220f1`  
		Last Modified: Tue, 25 Mar 2025 19:44:23 GMT  
		Size: 9.1 KB (9097 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5dbd57782e82acd156df6b54c5169f01dcdce7dc49a0a29196d77948a0f25774`  
		Last Modified: Tue, 25 Mar 2025 19:44:24 GMT  
		Size: 1.7 KB (1722 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26fa3c6aaeeb254431e665d8be4d4bbb64c28d4ffa0ab60fbcf8176a8454a6c8`  
		Last Modified: Tue, 25 Mar 2025 19:44:24 GMT  
		Size: 185.9 KB (185914 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bed167ef1f03dbb75fc9f4395ff693c587701fc06b3eca7c5234c8fedf1c8ae7`  
		Last Modified: Tue, 25 Mar 2025 19:44:25 GMT  
		Size: 406.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56c77f54fd0f6743e093c589548a2c4e4602840cefde8bd19ed631533f33dcd5`  
		Last Modified: Tue, 25 Mar 2025 19:44:25 GMT  
		Size: 115.5 KB (115536 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elasticsearch:8.16.6` - unknown; unknown

```console
$ docker pull elasticsearch@sha256:67861c6469782c19521c8711a624037b33e3afd06b0c5c0010959b4f953efdc8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (3040051 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df280673d79bab4fdd71e05fb198067256d34bfa607c3a2f0d6febdd9b5083ed`

```dockerfile
```

-	Layers:
	-	`sha256:cb5d4d5382914cc7eb977992600ca75d0456e3466816627a0887d739edeb871a`  
		Last Modified: Tue, 25 Mar 2025 19:44:23 GMT  
		Size: 3.0 MB (3001633 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c6a461b86d6d946853a2e5bbdca88a7318ddb8ab6548a491fe588eabb9d31880`  
		Last Modified: Tue, 25 Mar 2025 19:44:23 GMT  
		Size: 38.4 KB (38418 bytes)  
		MIME: application/vnd.in-toto+json

## `elasticsearch:8.17.4`

```console
$ docker pull elasticsearch@sha256:52b6582d6467e52407cb6fa84df5d48b9a74924833bec23cc468aa2386ebc408
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `elasticsearch:8.17.4` - linux; amd64

```console
$ docker pull elasticsearch@sha256:91afdfb99a446bd35855e2b13ad2944c1f691bfed436f96de30d849fa59e91b8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **685.1 MB (685063613 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:26649e4f96a1d84b22fb28df39b49577f4a4271e8e34751d688ad200a0a01b91`
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
# Tue, 25 Mar 2025 09:28:57 GMT
RUN yes no | dpkg-reconfigure dash &&     for iter in 1 2 3 4 5 6 7 8 9 10; do       export DEBIAN_FRONTEND=noninteractive &&       apt-get update &&       apt-get upgrade -y &&       apt-get install -y --no-install-recommends         ca-certificates curl netcat p11-kit unzip zip  &&       apt-get clean &&       rm -rf /var/lib/apt/lists/* &&       exit_code=0 && break ||         exit_code=$? && echo "apt-get error: retry $iter in 10s" && sleep 10;     done;     exit $exit_code # buildkit
# Tue, 25 Mar 2025 09:28:57 GMT
RUN groupadd -g 1000 elasticsearch &&     adduser --uid 1000 --gid 1000 --home /usr/share/elasticsearch elasticsearch &&     adduser elasticsearch root &&     chown -R 0:0 /usr/share/elasticsearch # buildkit
# Tue, 25 Mar 2025 09:28:57 GMT
ENV ELASTIC_CONTAINER=true
# Tue, 25 Mar 2025 09:28:57 GMT
WORKDIR /usr/share/elasticsearch
# Tue, 25 Mar 2025 09:28:57 GMT
COPY --chown=0:0 /usr/share/elasticsearch /usr/share/elasticsearch # buildkit
# Tue, 25 Mar 2025 09:28:57 GMT
COPY --chown=0:0 /bin/tini /bin/tini # buildkit
# Tue, 25 Mar 2025 09:28:57 GMT
ENV PATH=/usr/share/elasticsearch/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 25 Mar 2025 09:28:57 GMT
ENV SHELL=/bin/bash
# Tue, 25 Mar 2025 09:28:57 GMT
COPY bin/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh # buildkit
# Tue, 25 Mar 2025 09:28:57 GMT
RUN chmod g=u /etc/passwd &&     chmod 0555 /usr/local/bin/docker-entrypoint.sh &&     find / -xdev -perm -4000 -exec chmod ug-s {} + &&     chmod 0775 /usr/share/elasticsearch &&     chown elasticsearch bin config config/jvm.options.d data logs plugins # buildkit
# Tue, 25 Mar 2025 09:28:57 GMT
COPY bin/docker-openjdk /etc/ca-certificates/update.d/docker-openjdk # buildkit
# Tue, 25 Mar 2025 09:28:57 GMT
RUN /etc/ca-certificates/update.d/docker-openjdk # buildkit
# Tue, 25 Mar 2025 09:28:57 GMT
EXPOSE map[9200/tcp:{} 9300/tcp:{}]
# Tue, 25 Mar 2025 09:28:57 GMT
LABEL org.label-schema.build-date=2025-03-20T15:39:59.811110136Z org.label-schema.license=Elastic-License-2.0 org.label-schema.name=Elasticsearch org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/elasticsearch org.label-schema.usage=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.label-schema.vcs-ref=c63c7f5f8ce7d2e4805b7b3d842e7e792d84dda1 org.label-schema.vcs-url=https://github.com/elastic/elasticsearch org.label-schema.vendor=Elastic org.label-schema.version=8.17.4 org.opencontainers.image.created=2025-03-20T15:39:59.811110136Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.opencontainers.image.licenses=Elastic-License-2.0 org.opencontainers.image.revision=c63c7f5f8ce7d2e4805b7b3d842e7e792d84dda1 org.opencontainers.image.source=https://github.com/elastic/elasticsearch org.opencontainers.image.title=Elasticsearch org.opencontainers.image.url=https://www.elastic.co/products/elasticsearch org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=8.17.4
# Tue, 25 Mar 2025 09:28:57 GMT
ENTRYPOINT ["/bin/tini" "--" "/usr/local/bin/docker-entrypoint.sh"]
# Tue, 25 Mar 2025 09:28:57 GMT
CMD ["eswrapper"]
# Tue, 25 Mar 2025 09:28:57 GMT
USER 1000:0
```

-	Layers:
	-	`sha256:d9802f032d6798e2086607424bfe88cb8ec1d6f116e11cd99592dcaf261e9cd2`  
		Last Modified: Fri, 11 Oct 2024 04:41:25 GMT  
		Size: 27.5 MB (27511060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e7f745fc0574d2cbd9bd9a7e6b8ce4a9f32ca47f9d55cc10f003076ce4d9984`  
		Last Modified: Tue, 25 Mar 2025 19:45:32 GMT  
		Size: 15.0 MB (15023395 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9fa208ca05acac492e2b095b73f476a929f0a3f7b0e7f1b4d0f60ba93c614fe`  
		Last Modified: Tue, 25 Mar 2025 19:45:31 GMT  
		Size: 4.3 KB (4314 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a24c6ad77c70ff3fd8a82b7e2f57c68826596a3a0fbd35985d5fd2e1f06a3253`  
		Last Modified: Tue, 25 Mar 2025 19:45:46 GMT  
		Size: 642.2 MB (642205717 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f2e34e687d6ecf1c7f9bfb63852c06e45fef038e0bb5abf4074b3851f04497f`  
		Last Modified: Tue, 25 Mar 2025 19:45:31 GMT  
		Size: 9.5 KB (9530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa95599c6a3bcf307983f4e6786bf695491ae98a7b88de63e08ea64684d2543d`  
		Last Modified: Tue, 25 Mar 2025 19:45:32 GMT  
		Size: 1.7 KB (1722 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb1415b173431d73046fff399adc6de7c63908e33de79df697a15b0715c66ef8`  
		Last Modified: Tue, 25 Mar 2025 19:45:32 GMT  
		Size: 191.9 KB (191904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89f07aca6090c51412b23be9f9fc27a6d56bd5fc59adc14645548e9aa34bc248`  
		Last Modified: Tue, 25 Mar 2025 19:45:33 GMT  
		Size: 404.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71f4910f4ddd1c40bc09e5fccc50894535a598a67622c6e273c6ab1d4a090632`  
		Last Modified: Tue, 25 Mar 2025 19:45:33 GMT  
		Size: 115.5 KB (115535 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elasticsearch:8.17.4` - unknown; unknown

```console
$ docker pull elasticsearch@sha256:8a1b3d67de50f4f65e47d0efe6f4f9714f7741af1b63dd325e90308d4bab3db4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (3047076 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:91da762f5dc7f2938d95b4e336959a93a5c6d0eedc3d99b6aee9ab36ea56f662`

```dockerfile
```

-	Layers:
	-	`sha256:66029fb4b696776d1a51300393ff697aeb769eb8022039d4bc74ac622fe81761`  
		Last Modified: Tue, 25 Mar 2025 19:45:31 GMT  
		Size: 3.0 MB (3008861 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d5ea30e24e6dac95e03b770b84ee3ab1539082592d93acb165dbfc50f9ee3b4f`  
		Last Modified: Tue, 25 Mar 2025 19:45:31 GMT  
		Size: 38.2 KB (38215 bytes)  
		MIME: application/vnd.in-toto+json

### `elasticsearch:8.17.4` - linux; arm64 variant v8

```console
$ docker pull elasticsearch@sha256:fec9dd9861e33c7966f7cbc83c0fcee1274b60c9e68930fc6560956ffe49d3b5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **527.3 MB (527307058 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b91f43df96db428e4404a2e6dec5584a7b527755dded3a1c072c178f33ab288e`
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
# Tue, 25 Mar 2025 09:28:57 GMT
RUN yes no | dpkg-reconfigure dash &&     for iter in 1 2 3 4 5 6 7 8 9 10; do       export DEBIAN_FRONTEND=noninteractive &&       apt-get update &&       apt-get upgrade -y &&       apt-get install -y --no-install-recommends         ca-certificates curl netcat p11-kit unzip zip  &&       apt-get clean &&       rm -rf /var/lib/apt/lists/* &&       exit_code=0 && break ||         exit_code=$? && echo "apt-get error: retry $iter in 10s" && sleep 10;     done;     exit $exit_code # buildkit
# Tue, 25 Mar 2025 09:28:57 GMT
RUN groupadd -g 1000 elasticsearch &&     adduser --uid 1000 --gid 1000 --home /usr/share/elasticsearch elasticsearch &&     adduser elasticsearch root &&     chown -R 0:0 /usr/share/elasticsearch # buildkit
# Tue, 25 Mar 2025 09:28:57 GMT
ENV ELASTIC_CONTAINER=true
# Tue, 25 Mar 2025 09:28:57 GMT
WORKDIR /usr/share/elasticsearch
# Tue, 25 Mar 2025 09:28:57 GMT
COPY --chown=0:0 /usr/share/elasticsearch /usr/share/elasticsearch # buildkit
# Tue, 25 Mar 2025 09:28:57 GMT
COPY --chown=0:0 /bin/tini /bin/tini # buildkit
# Tue, 25 Mar 2025 09:28:57 GMT
ENV PATH=/usr/share/elasticsearch/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 25 Mar 2025 09:28:57 GMT
ENV SHELL=/bin/bash
# Tue, 25 Mar 2025 09:28:57 GMT
COPY bin/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh # buildkit
# Tue, 25 Mar 2025 09:28:57 GMT
RUN chmod g=u /etc/passwd &&     chmod 0555 /usr/local/bin/docker-entrypoint.sh &&     find / -xdev -perm -4000 -exec chmod ug-s {} + &&     chmod 0775 /usr/share/elasticsearch &&     chown elasticsearch bin config config/jvm.options.d data logs plugins # buildkit
# Tue, 25 Mar 2025 09:28:57 GMT
COPY bin/docker-openjdk /etc/ca-certificates/update.d/docker-openjdk # buildkit
# Tue, 25 Mar 2025 09:28:57 GMT
RUN /etc/ca-certificates/update.d/docker-openjdk # buildkit
# Tue, 25 Mar 2025 09:28:57 GMT
EXPOSE map[9200/tcp:{} 9300/tcp:{}]
# Tue, 25 Mar 2025 09:28:57 GMT
LABEL org.label-schema.build-date=2025-03-20T15:39:59.811110136Z org.label-schema.license=Elastic-License-2.0 org.label-schema.name=Elasticsearch org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/elasticsearch org.label-schema.usage=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.label-schema.vcs-ref=c63c7f5f8ce7d2e4805b7b3d842e7e792d84dda1 org.label-schema.vcs-url=https://github.com/elastic/elasticsearch org.label-schema.vendor=Elastic org.label-schema.version=8.17.4 org.opencontainers.image.created=2025-03-20T15:39:59.811110136Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.opencontainers.image.licenses=Elastic-License-2.0 org.opencontainers.image.revision=c63c7f5f8ce7d2e4805b7b3d842e7e792d84dda1 org.opencontainers.image.source=https://github.com/elastic/elasticsearch org.opencontainers.image.title=Elasticsearch org.opencontainers.image.url=https://www.elastic.co/products/elasticsearch org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=8.17.4
# Tue, 25 Mar 2025 09:28:57 GMT
ENTRYPOINT ["/bin/tini" "--" "/usr/local/bin/docker-entrypoint.sh"]
# Tue, 25 Mar 2025 09:28:57 GMT
CMD ["eswrapper"]
# Tue, 25 Mar 2025 09:28:57 GMT
USER 1000:0
```

-	Layers:
	-	`sha256:1b9f3c55f9d4aa5c52eb67a4cb7d0f4726ab85a413b50e3e3fe788befce3d297`  
		Last Modified: Fri, 11 Oct 2024 04:41:30 GMT  
		Size: 26.0 MB (25973828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e5c2366281558c3fd6d4aa155d04ace1d089bf5eddaa8f02d51dedadf212541`  
		Last Modified: Tue, 25 Mar 2025 19:44:24 GMT  
		Size: 13.8 MB (13751835 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0287c434f4bcc57ce95e84644d46ac9e8f3f4fa25e320e2a6d77508895a40175`  
		Last Modified: Tue, 25 Mar 2025 19:44:23 GMT  
		Size: 4.3 KB (4318 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:648b38059e64908e99d982b25be15d64748be0656791fc0bce37fc8c101c420e`  
		Last Modified: Tue, 25 Mar 2025 19:56:51 GMT  
		Size: 487.3 MB (487264360 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2575204bebd49dca5799047ab6e3a9d7dc04c884b567329f8bf8b8ddd0e8ca01`  
		Last Modified: Tue, 25 Mar 2025 19:56:41 GMT  
		Size: 9.1 KB (9099 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0bf271c7c6f82131b0d9fc6ccbfa6342c201a0bace9bc571938a790a06acac8c`  
		Last Modified: Tue, 25 Mar 2025 19:56:41 GMT  
		Size: 1.7 KB (1723 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4848bb6cfb7c74932e6cffd7ddbb39c4e0191e50fd23620b6fb091ab2f23e3e3`  
		Last Modified: Tue, 25 Mar 2025 19:56:41 GMT  
		Size: 185.9 KB (185920 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6e1d4bbfb5f0aa78027619b3cd1cfcea023d50d2a9c9ea09040670e605b4b34`  
		Last Modified: Tue, 25 Mar 2025 19:56:42 GMT  
		Size: 406.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4489603061e1f096fff9b1375795fc37ee904b18a9dcc0b36b793fbf20be1b46`  
		Last Modified: Tue, 25 Mar 2025 19:56:42 GMT  
		Size: 115.5 KB (115537 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elasticsearch:8.17.4` - unknown; unknown

```console
$ docker pull elasticsearch@sha256:658568a13bc614c3a4dc150f49e96d100e35f46f9d560bc80aedbb8b8ad9d714
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (3046251 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef581eb893f4c4355cc45e6f1876b83b083fdfff170598c3074897f4046bca85`

```dockerfile
```

-	Layers:
	-	`sha256:3826b65fbac469198569266d13f91a13064b5e623fef96864b6905132a9c97ad`  
		Last Modified: Tue, 25 Mar 2025 19:56:42 GMT  
		Size: 3.0 MB (3007833 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e6a4ccaed599968cf007482fb7413c618fac6160cf9d97669654928eccfb682d`  
		Last Modified: Tue, 25 Mar 2025 19:56:41 GMT  
		Size: 38.4 KB (38418 bytes)  
		MIME: application/vnd.in-toto+json
