<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `elasticsearch`

-	[`elasticsearch:7.17.24`](#elasticsearch71724)
-	[`elasticsearch:8.15.2`](#elasticsearch8152)

## `elasticsearch:7.17.24`

```console
$ docker pull elasticsearch@sha256:cf469407d37fdc8686ea18582a60b0f59b7559592545f4741c59e0a886499623
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `elasticsearch:7.17.24` - linux; amd64

```console
$ docker pull elasticsearch@sha256:1de6cd8dfa12bc2a51dc1bc120e919e691f864d551b0138d919a6b572e76309e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **362.6 MB (362619811 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:31e3e0ff8748b22be4d004788f6f2ef10410bb0cb4e4837ce50757e06d5dd471`
-	Entrypoint: `["\/bin\/tini","--","\/usr\/local\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["eswrapper"]`

```dockerfile
# Tue, 10 Sep 2024 08:21:14 GMT
ARG RELEASE
# Tue, 10 Sep 2024 08:21:14 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 10 Sep 2024 08:21:14 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 10 Sep 2024 08:21:14 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 10 Sep 2024 08:21:14 GMT
ADD file:6a209aa51ba684c0a39769619c42058ca99311b87563c7b079319a8bb91bec1f in / 
# Tue, 10 Sep 2024 08:21:14 GMT
CMD ["/bin/bash"]
# Tue, 10 Sep 2024 08:21:14 GMT
RUN yes no | dpkg-reconfigure dash &&     for iter in 1 2 3 4 5 6 7 8 9 10; do       export DEBIAN_FRONTEND=noninteractive &&       apt-get update &&       apt-get upgrade -y &&       apt-get install -y --no-install-recommends         ca-certificates curl netcat p11-kit unzip zip &&       apt-get clean &&       rm -rf /var/lib/apt/lists/* &&       exit_code=0 && break ||         exit_code=$? && echo "apt-get error: retry $iter in 10s" && sleep 10;     done;     exit $exit_code # buildkit
# Tue, 10 Sep 2024 08:21:14 GMT
RUN groupadd -g 1000 elasticsearch &&     adduser --uid 1000 --gid 1000 --home /usr/share/elasticsearch elasticsearch &&     adduser elasticsearch root &&     chown -R 0:0 /usr/share/elasticsearch # buildkit
# Tue, 10 Sep 2024 08:21:14 GMT
ENV ELASTIC_CONTAINER=true
# Tue, 10 Sep 2024 08:21:14 GMT
WORKDIR /usr/share/elasticsearch
# Tue, 10 Sep 2024 08:21:14 GMT
COPY --chown=0:0 /usr/share/elasticsearch /usr/share/elasticsearch # buildkit
# Tue, 10 Sep 2024 08:21:14 GMT
COPY --chown=0:0 /bin/tini /bin/tini # buildkit
# Tue, 10 Sep 2024 08:21:14 GMT
ENV PATH=/usr/share/elasticsearch/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 10 Sep 2024 08:21:14 GMT
COPY bin/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh # buildkit
# Tue, 10 Sep 2024 08:21:14 GMT
RUN chmod g=u /etc/passwd &&     chmod 0555 /usr/local/bin/docker-entrypoint.sh &&     find / -xdev -perm -4000 -exec chmod ug-s {} + &&     chmod 0775 /usr/share/elasticsearch &&     chown elasticsearch bin config config/jvm.options.d data logs plugins # buildkit
# Tue, 10 Sep 2024 08:21:14 GMT
COPY bin/docker-openjdk /etc/ca-certificates/update.d/docker-openjdk # buildkit
# Tue, 10 Sep 2024 08:21:14 GMT
RUN /etc/ca-certificates/update.d/docker-openjdk # buildkit
# Tue, 10 Sep 2024 08:21:14 GMT
EXPOSE map[9200/tcp:{} 9300/tcp:{}]
# Tue, 10 Sep 2024 08:21:14 GMT
LABEL org.label-schema.build-date=2024-09-05T07:34:51.812485320Z org.label-schema.license=Elastic-License-2.0 org.label-schema.name=Elasticsearch org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/elasticsearch org.label-schema.usage=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.label-schema.vcs-ref=fcf25fff740db6ab3ed5d145c58d70e4c3528ea7 org.label-schema.vcs-url=https://github.com/elastic/elasticsearch org.label-schema.vendor=Elastic org.label-schema.version=7.17.24 org.opencontainers.image.created=2024-09-05T07:34:51.812485320Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.opencontainers.image.licenses=Elastic-License-2.0 org.opencontainers.image.revision=fcf25fff740db6ab3ed5d145c58d70e4c3528ea7 org.opencontainers.image.source=https://github.com/elastic/elasticsearch org.opencontainers.image.title=Elasticsearch org.opencontainers.image.url=https://www.elastic.co/products/elasticsearch org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=7.17.24
# Tue, 10 Sep 2024 08:21:14 GMT
ENTRYPOINT ["/bin/tini" "--" "/usr/local/bin/docker-entrypoint.sh"]
# Tue, 10 Sep 2024 08:21:14 GMT
CMD ["eswrapper"]
```

-	Layers:
	-	`sha256:3823320faa42774534fd7eee0bd245af8cec6a720ad722144d40efa229291d8f`  
		Last Modified: Wed, 18 Sep 2024 05:32:37 GMT  
		Size: 27.5 MB (27511052 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3dc0dfdd028742b7971c45a465666a2b16c202c62a62e553018ffa8de53f9663`  
		Last Modified: Wed, 02 Oct 2024 01:58:43 GMT  
		Size: 7.5 MB (7523472 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b0b9f86f07146abd7c0bbb6fb9d6e761065530e7f7ce17ac6054e9454d7455a`  
		Last Modified: Wed, 02 Oct 2024 01:58:43 GMT  
		Size: 4.3 KB (4313 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f8801e55d0f90928f77f64017df718a01fb9f7880d9ae7cc22eed7651894dbc`  
		Last Modified: Wed, 02 Oct 2024 01:58:49 GMT  
		Size: 327.3 MB (327261327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:670ffc5268e5cfaabbb79c9d6368a5cfef926701a06c3eed5c2c91e8d7945927`  
		Last Modified: Wed, 02 Oct 2024 01:58:43 GMT  
		Size: 9.5 KB (9529 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9390fc5d8e7faddb10f80826c9712ea26ce03b89e0c4017e54408a1fd500ea47`  
		Last Modified: Wed, 02 Oct 2024 01:58:43 GMT  
		Size: 2.0 KB (1979 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec2afd6697c0dfa8643fbbc44bd165a6edc4617d34c76dc8e706df03ceaad068`  
		Last Modified: Wed, 02 Oct 2024 01:58:44 GMT  
		Size: 192.2 KB (192174 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3fdefecb2881f5bade4c0a6bfd103b6b52418afc69daa81cd164151f020eab64`  
		Last Modified: Wed, 02 Oct 2024 01:58:44 GMT  
		Size: 404.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6501ba51a84142f8491387228391a6611e5e954f0a809997d288c6858748591`  
		Last Modified: Wed, 02 Oct 2024 01:58:44 GMT  
		Size: 115.5 KB (115529 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elasticsearch:7.17.24` - unknown; unknown

```console
$ docker pull elasticsearch@sha256:dc43ed111f4a03a333b00784e45796659d898be2415d519e42148bf59358a5c1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2545910 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a7c837aad59389928615aae0c98b6c6bcdf28d9c716425b7580493361604298`

```dockerfile
```

-	Layers:
	-	`sha256:3859e3c0cc54659823b80a3448d7cd647099420adf264446676d8661758ac30e`  
		Last Modified: Wed, 02 Oct 2024 01:58:43 GMT  
		Size: 2.5 MB (2508271 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7b07c396de5bda8d26910b15e43f5975fa5eb0d889cc09c40999d3765e228a36`  
		Last Modified: Wed, 02 Oct 2024 01:58:43 GMT  
		Size: 37.6 KB (37639 bytes)  
		MIME: application/vnd.in-toto+json

### `elasticsearch:7.17.24` - linux; arm64 variant v8

```console
$ docker pull elasticsearch@sha256:230433a39ae12fafdfaa86e6854024818bb3c43283bbb8dc6139629ba82aecd9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **358.6 MB (358558975 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:36d53bc38408d393f5d9702d35df5ca8b1296601b7635c3acb33662159c69e67`
-	Entrypoint: `["\/bin\/tini","--","\/usr\/local\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["eswrapper"]`

```dockerfile
# Tue, 10 Sep 2024 08:21:14 GMT
ARG RELEASE
# Tue, 10 Sep 2024 08:21:14 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 10 Sep 2024 08:21:14 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 10 Sep 2024 08:21:14 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 10 Sep 2024 08:21:14 GMT
ADD file:8537b4db344382b39d669af27cd94ec0f870ceafe58c67ee54e3f9b38fb8d671 in / 
# Tue, 10 Sep 2024 08:21:14 GMT
CMD ["/bin/bash"]
# Tue, 10 Sep 2024 08:21:14 GMT
RUN yes no | dpkg-reconfigure dash &&     for iter in 1 2 3 4 5 6 7 8 9 10; do       export DEBIAN_FRONTEND=noninteractive &&       apt-get update &&       apt-get upgrade -y &&       apt-get install -y --no-install-recommends         ca-certificates curl netcat p11-kit unzip zip &&       apt-get clean &&       rm -rf /var/lib/apt/lists/* &&       exit_code=0 && break ||         exit_code=$? && echo "apt-get error: retry $iter in 10s" && sleep 10;     done;     exit $exit_code # buildkit
# Tue, 10 Sep 2024 08:21:14 GMT
RUN groupadd -g 1000 elasticsearch &&     adduser --uid 1000 --gid 1000 --home /usr/share/elasticsearch elasticsearch &&     adduser elasticsearch root &&     chown -R 0:0 /usr/share/elasticsearch # buildkit
# Tue, 10 Sep 2024 08:21:14 GMT
ENV ELASTIC_CONTAINER=true
# Tue, 10 Sep 2024 08:21:14 GMT
WORKDIR /usr/share/elasticsearch
# Tue, 10 Sep 2024 08:21:14 GMT
COPY --chown=0:0 /usr/share/elasticsearch /usr/share/elasticsearch # buildkit
# Tue, 10 Sep 2024 08:21:14 GMT
COPY --chown=0:0 /bin/tini /bin/tini # buildkit
# Tue, 10 Sep 2024 08:21:14 GMT
ENV PATH=/usr/share/elasticsearch/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 10 Sep 2024 08:21:14 GMT
COPY bin/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh # buildkit
# Tue, 10 Sep 2024 08:21:14 GMT
RUN chmod g=u /etc/passwd &&     chmod 0555 /usr/local/bin/docker-entrypoint.sh &&     find / -xdev -perm -4000 -exec chmod ug-s {} + &&     chmod 0775 /usr/share/elasticsearch &&     chown elasticsearch bin config config/jvm.options.d data logs plugins # buildkit
# Tue, 10 Sep 2024 08:21:14 GMT
COPY bin/docker-openjdk /etc/ca-certificates/update.d/docker-openjdk # buildkit
# Tue, 10 Sep 2024 08:21:14 GMT
RUN /etc/ca-certificates/update.d/docker-openjdk # buildkit
# Tue, 10 Sep 2024 08:21:14 GMT
EXPOSE map[9200/tcp:{} 9300/tcp:{}]
# Tue, 10 Sep 2024 08:21:14 GMT
LABEL org.label-schema.build-date=2024-09-05T07:34:51.812485320Z org.label-schema.license=Elastic-License-2.0 org.label-schema.name=Elasticsearch org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/elasticsearch org.label-schema.usage=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.label-schema.vcs-ref=fcf25fff740db6ab3ed5d145c58d70e4c3528ea7 org.label-schema.vcs-url=https://github.com/elastic/elasticsearch org.label-schema.vendor=Elastic org.label-schema.version=7.17.24 org.opencontainers.image.created=2024-09-05T07:34:51.812485320Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.opencontainers.image.licenses=Elastic-License-2.0 org.opencontainers.image.revision=fcf25fff740db6ab3ed5d145c58d70e4c3528ea7 org.opencontainers.image.source=https://github.com/elastic/elasticsearch org.opencontainers.image.title=Elasticsearch org.opencontainers.image.url=https://www.elastic.co/products/elasticsearch org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=7.17.24
# Tue, 10 Sep 2024 08:21:14 GMT
ENTRYPOINT ["/bin/tini" "--" "/usr/local/bin/docker-entrypoint.sh"]
# Tue, 10 Sep 2024 08:21:14 GMT
CMD ["eswrapper"]
```

-	Layers:
	-	`sha256:1b9f3c55f9d4aa5c52eb67a4cb7d0f4726ab85a413b50e3e3fe788befce3d297`  
		Last Modified: Fri, 11 Oct 2024 04:41:30 GMT  
		Size: 26.0 MB (25973828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a85c218d3b24c46787c192804f137c43a06fe522c75a5bd8d582c80857c36103`  
		Last Modified: Wed, 16 Oct 2024 02:48:36 GMT  
		Size: 7.3 MB (7347306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3088df8074d66943a171b0017f5118ea1384d714af989d1812a08dc889231ad`  
		Last Modified: Wed, 16 Oct 2024 02:48:35 GMT  
		Size: 4.3 KB (4319 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d5c290f76f38f5b961b283bf5f9f2a358f1a67b973be9e54936ca1f94fbc0cc`  
		Last Modified: Wed, 16 Oct 2024 02:48:43 GMT  
		Size: 324.9 MB (324920302 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e34f5311fcde263e713a72c578e8c709fa6a3a16c3090ef26b1f6af08981687`  
		Last Modified: Wed, 16 Oct 2024 02:48:36 GMT  
		Size: 9.1 KB (9092 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e5e53abf79329408585172e17f140bf57b3c5c8315f974c335afa37c4d52954`  
		Last Modified: Wed, 16 Oct 2024 02:48:36 GMT  
		Size: 2.0 KB (1978 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32294a517a218ad26d6fd6de67d38d5bb7d55e6fc947466f12442229b350d511`  
		Last Modified: Wed, 16 Oct 2024 02:48:37 GMT  
		Size: 186.2 KB (186177 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de43c482c62f0610ef283c667dc0d08d699d57ee351df237ee7f17c56381b1e3`  
		Last Modified: Wed, 16 Oct 2024 02:48:37 GMT  
		Size: 405.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c012cd9627fd550f332b33974307a32f67ab5bccd0d61999e7626c1a035edd9`  
		Last Modified: Wed, 16 Oct 2024 02:48:37 GMT  
		Size: 115.5 KB (115536 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elasticsearch:7.17.24` - unknown; unknown

```console
$ docker pull elasticsearch@sha256:e7bf5928f7b590ad15c4e8fa130da16c0aa8c059ebe0edfe2be20c9dfc53051e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2545109 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c35f387d94ccd900c98cd6b369a56ea8ddeb69cb92940bc9c0d63dcbb3cca1ae`

```dockerfile
```

-	Layers:
	-	`sha256:9d2ad51150b971952fb968154cd596110349e1a40bdd6ad49db2583e3470f354`  
		Last Modified: Wed, 16 Oct 2024 02:48:36 GMT  
		Size: 2.5 MB (2507240 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b668b0e29f1ee60ca77a26071bdb0cb007e53c73ce10ed5b4cb5146aaf97d3b9`  
		Last Modified: Wed, 16 Oct 2024 02:48:36 GMT  
		Size: 37.9 KB (37869 bytes)  
		MIME: application/vnd.in-toto+json

## `elasticsearch:8.15.2`

```console
$ docker pull elasticsearch@sha256:98dcef762a36fec75ec7edfffc1faa5190ff4adaadd6df8acd68e6ca9e0bf14d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `elasticsearch:8.15.2` - linux; amd64

```console
$ docker pull elasticsearch@sha256:d14d3320591b339c1f00389312cb06dae191d8378ccf8365c3801930eaedbb06
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **649.6 MB (649594596 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:574a00cbaa781d34ad4c9523421d818af1a48cd03898d29b364cc58a2151c97b`
-	Entrypoint: `["\/bin\/tini","--","\/usr\/local\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["eswrapper"]`

```dockerfile
# Wed, 18 Sep 2024 04:18:32 GMT
ARG RELEASE
# Wed, 18 Sep 2024 04:18:32 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 18 Sep 2024 04:18:32 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 18 Sep 2024 04:18:32 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 18 Sep 2024 04:18:34 GMT
ADD file:6a209aa51ba684c0a39769619c42058ca99311b87563c7b079319a8bb91bec1f in / 
# Wed, 18 Sep 2024 04:18:34 GMT
CMD ["/bin/bash"]
# Thu, 26 Sep 2024 08:08:51 GMT
RUN yes no | dpkg-reconfigure dash &&     for iter in 1 2 3 4 5 6 7 8 9 10; do       export DEBIAN_FRONTEND=noninteractive &&       apt-get update &&       apt-get upgrade -y &&       apt-get install -y --no-install-recommends         ca-certificates curl netcat p11-kit unzip zip  &&       apt-get clean &&       rm -rf /var/lib/apt/lists/* &&       exit_code=0 && break ||         exit_code=$? && echo "apt-get error: retry $iter in 10s" && sleep 10;     done;     exit $exit_code # buildkit
# Thu, 26 Sep 2024 08:08:51 GMT
RUN groupadd -g 1000 elasticsearch &&     adduser --uid 1000 --gid 1000 --home /usr/share/elasticsearch elasticsearch &&     adduser elasticsearch root &&     chown -R 0:0 /usr/share/elasticsearch # buildkit
# Thu, 26 Sep 2024 08:08:51 GMT
ENV ELASTIC_CONTAINER=true
# Thu, 26 Sep 2024 08:08:51 GMT
WORKDIR /usr/share/elasticsearch
# Thu, 26 Sep 2024 08:08:51 GMT
COPY --chown=0:0 /usr/share/elasticsearch /usr/share/elasticsearch # buildkit
# Thu, 26 Sep 2024 08:08:51 GMT
COPY --chown=0:0 /bin/tini /bin/tini # buildkit
# Thu, 26 Sep 2024 08:08:51 GMT
ENV PATH=/usr/share/elasticsearch/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 26 Sep 2024 08:08:51 GMT
COPY bin/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh # buildkit
# Thu, 26 Sep 2024 08:08:51 GMT
RUN chmod g=u /etc/passwd &&     chmod 0555 /usr/local/bin/docker-entrypoint.sh &&     find / -xdev -perm -4000 -exec chmod ug-s {} + &&     chmod 0775 /usr/share/elasticsearch &&     chown elasticsearch bin config config/jvm.options.d data logs plugins # buildkit
# Thu, 26 Sep 2024 08:08:51 GMT
COPY bin/docker-openjdk /etc/ca-certificates/update.d/docker-openjdk # buildkit
# Thu, 26 Sep 2024 08:08:51 GMT
RUN /etc/ca-certificates/update.d/docker-openjdk # buildkit
# Thu, 26 Sep 2024 08:08:51 GMT
EXPOSE map[9200/tcp:{} 9300/tcp:{}]
# Thu, 26 Sep 2024 08:08:51 GMT
LABEL org.label-schema.build-date=2024-09-19T10:06:03.564235954Z org.label-schema.license=Elastic-License-2.0 org.label-schema.name=Elasticsearch org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/elasticsearch org.label-schema.usage=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.label-schema.vcs-ref=98adf7bf6bb69b66ab95b761c9e5aadb0bb059a3 org.label-schema.vcs-url=https://github.com/elastic/elasticsearch org.label-schema.vendor=Elastic org.label-schema.version=8.15.2 org.opencontainers.image.created=2024-09-19T10:06:03.564235954Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.opencontainers.image.licenses=Elastic-License-2.0 org.opencontainers.image.revision=98adf7bf6bb69b66ab95b761c9e5aadb0bb059a3 org.opencontainers.image.source=https://github.com/elastic/elasticsearch org.opencontainers.image.title=Elasticsearch org.opencontainers.image.url=https://www.elastic.co/products/elasticsearch org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=8.15.2
# Thu, 26 Sep 2024 08:08:51 GMT
ENTRYPOINT ["/bin/tini" "--" "/usr/local/bin/docker-entrypoint.sh"]
# Thu, 26 Sep 2024 08:08:51 GMT
CMD ["eswrapper"]
# Thu, 26 Sep 2024 08:08:51 GMT
USER 1000:0
```

-	Layers:
	-	`sha256:3823320faa42774534fd7eee0bd245af8cec6a720ad722144d40efa229291d8f`  
		Last Modified: Wed, 18 Sep 2024 05:32:37 GMT  
		Size: 27.5 MB (27511052 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:169d23dcd898889d824f10066bf00680a0a35c280451cf604e558795cc638dd8`  
		Last Modified: Wed, 02 Oct 2024 01:59:26 GMT  
		Size: 7.5 MB (7523398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6b28722adaee8eda1685146ce13f6f64a0776da2df1b97eaacbceb07ed4b7c7`  
		Last Modified: Wed, 02 Oct 2024 01:59:26 GMT  
		Size: 4.3 KB (4313 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54cfee5965d815ca3738278faa828dd412f3858463ecb90daf0664039c33f14c`  
		Last Modified: Wed, 02 Oct 2024 01:59:39 GMT  
		Size: 614.2 MB (614236704 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b980bd608df22fa05077530aa110d67a824b18627e8c7d0d8a51a6ade497905`  
		Last Modified: Wed, 02 Oct 2024 01:59:26 GMT  
		Size: 9.5 KB (9530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:675322cac17aef3751e77a1a560c4855e2c19dd4f33a1caf3b84f8b36b880c1e`  
		Last Modified: Wed, 02 Oct 2024 01:59:27 GMT  
		Size: 1.7 KB (1721 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77aca5f76f2f933c3897b7a637a8b96216be5073b53ad5a73b61bab2ee93243c`  
		Last Modified: Wed, 02 Oct 2024 01:59:27 GMT  
		Size: 191.9 KB (191903 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1499dc90276bcef6a0d6f051673145d64b63b3825743d531a730bf07309f897c`  
		Last Modified: Wed, 02 Oct 2024 01:59:27 GMT  
		Size: 406.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4643be2871207d0c1f4369f9468e80175e2973e775d34818c51721f1b8dbfbb2`  
		Last Modified: Wed, 02 Oct 2024 01:59:27 GMT  
		Size: 115.5 KB (115537 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elasticsearch:8.15.2` - unknown; unknown

```console
$ docker pull elasticsearch@sha256:6a40ed1e7b04bed51c7b7d057faae7a1629d3a4ed04899d2706c7448366ba17c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2894173 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:11b36d59b794548262ed429d894fe1bb69de3b6f3b08b84ad9caf7a8166461e0`

```dockerfile
```

-	Layers:
	-	`sha256:c7b2ef9a83c18bf350be93b576fdfafb588e282fc86b29d808876329cee55b5d`  
		Last Modified: Wed, 02 Oct 2024 01:59:26 GMT  
		Size: 2.9 MB (2856520 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:84b8f8d7fb28e9b10e420e7bd3d06dbb9f33df2bfa0ad3470be58650a7c35418`  
		Last Modified: Wed, 02 Oct 2024 01:59:26 GMT  
		Size: 37.7 KB (37653 bytes)  
		MIME: application/vnd.in-toto+json

### `elasticsearch:8.15.2` - linux; arm64 variant v8

```console
$ docker pull elasticsearch@sha256:db1197163cedd96833a8183e301661f77aa0e17b44600db4c9cff019d7a537d0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **493.1 MB (493110514 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c1bc06e17d65d6599ce9959401019a7b90f4fecc00374ce952f7198d734e6ca7`
-	Entrypoint: `["\/bin\/tini","--","\/usr\/local\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["eswrapper"]`

```dockerfile
# Thu, 26 Sep 2024 08:08:51 GMT
ARG RELEASE
# Thu, 26 Sep 2024 08:08:51 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 26 Sep 2024 08:08:51 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 26 Sep 2024 08:08:51 GMT
LABEL org.opencontainers.image.version=20.04
# Thu, 26 Sep 2024 08:08:51 GMT
ADD file:8537b4db344382b39d669af27cd94ec0f870ceafe58c67ee54e3f9b38fb8d671 in / 
# Thu, 26 Sep 2024 08:08:51 GMT
CMD ["/bin/bash"]
# Thu, 26 Sep 2024 08:08:51 GMT
RUN yes no | dpkg-reconfigure dash &&     for iter in 1 2 3 4 5 6 7 8 9 10; do       export DEBIAN_FRONTEND=noninteractive &&       apt-get update &&       apt-get upgrade -y &&       apt-get install -y --no-install-recommends         ca-certificates curl netcat p11-kit unzip zip  &&       apt-get clean &&       rm -rf /var/lib/apt/lists/* &&       exit_code=0 && break ||         exit_code=$? && echo "apt-get error: retry $iter in 10s" && sleep 10;     done;     exit $exit_code # buildkit
# Thu, 26 Sep 2024 08:08:51 GMT
RUN groupadd -g 1000 elasticsearch &&     adduser --uid 1000 --gid 1000 --home /usr/share/elasticsearch elasticsearch &&     adduser elasticsearch root &&     chown -R 0:0 /usr/share/elasticsearch # buildkit
# Thu, 26 Sep 2024 08:08:51 GMT
ENV ELASTIC_CONTAINER=true
# Thu, 26 Sep 2024 08:08:51 GMT
WORKDIR /usr/share/elasticsearch
# Thu, 26 Sep 2024 08:08:51 GMT
COPY --chown=0:0 /usr/share/elasticsearch /usr/share/elasticsearch # buildkit
# Thu, 26 Sep 2024 08:08:51 GMT
COPY --chown=0:0 /bin/tini /bin/tini # buildkit
# Thu, 26 Sep 2024 08:08:51 GMT
ENV PATH=/usr/share/elasticsearch/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 26 Sep 2024 08:08:51 GMT
COPY bin/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh # buildkit
# Thu, 26 Sep 2024 08:08:51 GMT
RUN chmod g=u /etc/passwd &&     chmod 0555 /usr/local/bin/docker-entrypoint.sh &&     find / -xdev -perm -4000 -exec chmod ug-s {} + &&     chmod 0775 /usr/share/elasticsearch &&     chown elasticsearch bin config config/jvm.options.d data logs plugins # buildkit
# Thu, 26 Sep 2024 08:08:51 GMT
COPY bin/docker-openjdk /etc/ca-certificates/update.d/docker-openjdk # buildkit
# Thu, 26 Sep 2024 08:08:51 GMT
RUN /etc/ca-certificates/update.d/docker-openjdk # buildkit
# Thu, 26 Sep 2024 08:08:51 GMT
EXPOSE map[9200/tcp:{} 9300/tcp:{}]
# Thu, 26 Sep 2024 08:08:51 GMT
LABEL org.label-schema.build-date=2024-09-19T10:06:03.564235954Z org.label-schema.license=Elastic-License-2.0 org.label-schema.name=Elasticsearch org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/elasticsearch org.label-schema.usage=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.label-schema.vcs-ref=98adf7bf6bb69b66ab95b761c9e5aadb0bb059a3 org.label-schema.vcs-url=https://github.com/elastic/elasticsearch org.label-schema.vendor=Elastic org.label-schema.version=8.15.2 org.opencontainers.image.created=2024-09-19T10:06:03.564235954Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.opencontainers.image.licenses=Elastic-License-2.0 org.opencontainers.image.revision=98adf7bf6bb69b66ab95b761c9e5aadb0bb059a3 org.opencontainers.image.source=https://github.com/elastic/elasticsearch org.opencontainers.image.title=Elasticsearch org.opencontainers.image.url=https://www.elastic.co/products/elasticsearch org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=8.15.2
# Thu, 26 Sep 2024 08:08:51 GMT
ENTRYPOINT ["/bin/tini" "--" "/usr/local/bin/docker-entrypoint.sh"]
# Thu, 26 Sep 2024 08:08:51 GMT
CMD ["eswrapper"]
# Thu, 26 Sep 2024 08:08:51 GMT
USER 1000:0
```

-	Layers:
	-	`sha256:1b9f3c55f9d4aa5c52eb67a4cb7d0f4726ab85a413b50e3e3fe788befce3d297`  
		Last Modified: Fri, 11 Oct 2024 04:41:30 GMT  
		Size: 26.0 MB (25973828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e6126ba20a2f4f0d9b244bc4eb31f8371a886131254f264a47d9f4c849e44ca`  
		Last Modified: Wed, 16 Oct 2024 02:46:51 GMT  
		Size: 7.3 MB (7347326 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac0262944513a3fde69a989ef8a782aad588b8f85f4e1a1eced030b54168819d`  
		Last Modified: Wed, 16 Oct 2024 02:46:50 GMT  
		Size: 4.3 KB (4318 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:441b03c8b27d7f92ab4fefc119081f61db2541771a5e9806c2e97e21711dc1e7`  
		Last Modified: Wed, 16 Oct 2024 02:47:00 GMT  
		Size: 459.5 MB (459472338 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e68f5022884d59bf1c2add63e90b31ddb872d6514fb51fda84f242eecfc20bd3`  
		Last Modified: Wed, 16 Oct 2024 02:46:51 GMT  
		Size: 9.1 KB (9092 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a90d4084dd034807383176461b34c3d7031b6cf15a7d5c9457154aee0b14fc5`  
		Last Modified: Wed, 16 Oct 2024 02:46:52 GMT  
		Size: 1.7 KB (1721 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64f4741df87786f8a5ba913721008a7c55ce72038c83815c4b1ea2768a0be7a9`  
		Last Modified: Wed, 16 Oct 2024 02:46:52 GMT  
		Size: 185.9 KB (185915 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:351526e6e18eaf9de0da9b6bec2faab52e6c14d8f794b0171541ec732bc47d1a`  
		Last Modified: Wed, 16 Oct 2024 02:46:52 GMT  
		Size: 407.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53d85d131aa825918445125bb8c0337b596bf57cf742ead27fa84f65a78f1d64`  
		Last Modified: Wed, 16 Oct 2024 02:46:53 GMT  
		Size: 115.5 KB (115537 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elasticsearch:8.15.2` - unknown; unknown

```console
$ docker pull elasticsearch@sha256:5ded123c2338e6ce056bfc049e57e3e0c21b5d77654d6a702b1d1c84810669e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2893374 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d46ecf9960c97ca9cf8b94714ee5ae4f07fb6f59b779202c5e345c8a737c596`

```dockerfile
```

-	Layers:
	-	`sha256:9446dd085d2d41c2367eafa8315af7eaee02244265225f67c55e15d24d0a2eaa`  
		Last Modified: Wed, 16 Oct 2024 02:46:50 GMT  
		Size: 2.9 MB (2855489 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a7d4edf3db3ea2258d5f70bff311a4008e95471e72d483fbb46a59d63a0dda02`  
		Last Modified: Wed, 16 Oct 2024 02:46:50 GMT  
		Size: 37.9 KB (37885 bytes)  
		MIME: application/vnd.in-toto+json
