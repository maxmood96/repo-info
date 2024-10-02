<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `elasticsearch`

-	[`elasticsearch:7.17.24`](#elasticsearch71724)
-	[`elasticsearch:8.15.2`](#elasticsearch8152)

## `elasticsearch:7.17.24`

```console
$ docker pull elasticsearch@sha256:ff9fab41c50a56400461f4629a70f4e60ee8b3f0b42e57a97f91e1ad68d332b2
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
$ docker pull elasticsearch@sha256:0434962ef5b8a507c90dfee1d618438dde1f13c0d86807faa3b77ef72cebd08e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **358.6 MB (358558732 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:136dd5aaf52fa763906d0b63eeee7ab2b9f7d288a9c1cc056079ea8bd9fe9e15`
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
ADD file:193e44687e108da6ce3970dd4e85b4ab975e008873500871bb89e452afe82d52 in / 
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
	-	`sha256:f7087ec3f63a82386ce40d74d075d761ece5bfaefdc30b9ef62f73ecfb2e41fe`  
		Last Modified: Wed, 18 Sep 2024 05:32:46 GMT  
		Size: 26.0 MB (25973592 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d979694296e96cbd46d49b760e0cf911f6a229269dc0c7396b1aa92354726761`  
		Last Modified: Wed, 02 Oct 2024 02:29:43 GMT  
		Size: 7.3 MB (7347176 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a69b527753c6d26964bd01ea73e0a5b22b33729188aab2d94f5f300e89b3123`  
		Last Modified: Wed, 02 Oct 2024 02:29:42 GMT  
		Size: 4.3 KB (4318 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de28a04ef1528ff905501d7180a0293bb95c17da50d5f8a4d343dd7a9a6ab793`  
		Last Modified: Wed, 02 Oct 2024 02:29:49 GMT  
		Size: 324.9 MB (324920431 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7430f889dabb2228289113a5eb872049ed4e567760c46e97855e469aa22635b`  
		Last Modified: Wed, 02 Oct 2024 02:29:42 GMT  
		Size: 9.1 KB (9094 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc89c12a00f6b90708d5c8d4eb70799bf60a9e468dd9cdc42002bb27148b475f`  
		Last Modified: Wed, 02 Oct 2024 02:29:43 GMT  
		Size: 2.0 KB (1977 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a47952dfdd726953fb9fb7cb639a50a2ca94f5b40c6dfb86e2051a632e1eecf`  
		Last Modified: Wed, 02 Oct 2024 02:29:43 GMT  
		Size: 186.2 KB (186178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c58a725bcb3a04c858393e0270823607eab6f213c1ff036a31123d52287a78bb`  
		Last Modified: Wed, 02 Oct 2024 02:29:44 GMT  
		Size: 404.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db0dd20542ef7fd87bcf67db020612333111612021f183d204c273cc98423d48`  
		Last Modified: Wed, 02 Oct 2024 02:29:44 GMT  
		Size: 115.5 KB (115530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elasticsearch:7.17.24` - unknown; unknown

```console
$ docker pull elasticsearch@sha256:fdd0afb6004909fe3968c744e12353599141852c21550ad93a80ab5603adcf3c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2545076 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:23a0c4d024b792552138e10ffdd53ae0bb5296f8d86bd57928834c682f8ef9a8`

```dockerfile
```

-	Layers:
	-	`sha256:509f0d6abdb5da14f928e2bfafe2b826c2784f78d73ca428fc39022b03c741a0`  
		Last Modified: Wed, 02 Oct 2024 02:29:43 GMT  
		Size: 2.5 MB (2507240 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:620ffa4f35ff3e1e79431b4d0776ae5ad94452c846008d23d2dcbc47752f3a51`  
		Last Modified: Wed, 02 Oct 2024 02:29:42 GMT  
		Size: 37.8 KB (37836 bytes)  
		MIME: application/vnd.in-toto+json

## `elasticsearch:8.15.2`

```console
$ docker pull elasticsearch@sha256:2f2b0abc7d7b127d6eea3ee8de0c347e53b8d1b833500e5bceb89029841e0d7d
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
$ docker pull elasticsearch@sha256:b4ccdc7401ff82a69ee5b9458d3538a3e9b78d1e183bd44a510367d22da535c4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **493.1 MB (493110138 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:682b20bbec36803c311139ded4c3673f3e84f87e81d836f8a707a590f3467749`
-	Entrypoint: `["\/bin\/tini","--","\/usr\/local\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["eswrapper"]`

```dockerfile
# Wed, 18 Sep 2024 04:18:13 GMT
ARG RELEASE
# Wed, 18 Sep 2024 04:18:13 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 18 Sep 2024 04:18:13 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 18 Sep 2024 04:18:13 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 18 Sep 2024 04:18:15 GMT
ADD file:193e44687e108da6ce3970dd4e85b4ab975e008873500871bb89e452afe82d52 in / 
# Wed, 18 Sep 2024 04:18:15 GMT
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
	-	`sha256:f7087ec3f63a82386ce40d74d075d761ece5bfaefdc30b9ef62f73ecfb2e41fe`  
		Last Modified: Wed, 18 Sep 2024 05:32:46 GMT  
		Size: 26.0 MB (25973592 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d5c3a6cb71b6bc8c2e9e8049bce561e7d95789b3c9e48c0026288a04599105d`  
		Last Modified: Wed, 02 Oct 2024 02:28:14 GMT  
		Size: 7.3 MB (7347180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:777bf9099072b1bbd209fa9153004b78af6f14896477d75cc247647ab378257b`  
		Last Modified: Wed, 02 Oct 2024 02:28:13 GMT  
		Size: 4.3 KB (4319 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba3adf0faf359deff75a9edc286ac501380d8951bd2fe62549a7c377afabbff5`  
		Last Modified: Wed, 02 Oct 2024 02:28:24 GMT  
		Size: 459.5 MB (459472341 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:708f62386319b0d3ff9f903ceb03d3fcd889d4ed9b4307356b955aebe822476f`  
		Last Modified: Wed, 02 Oct 2024 02:28:14 GMT  
		Size: 9.1 KB (9093 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f746a724cd807a0d9db308b4b2e581075f7213a01384c9f2a80243212e1a2d04`  
		Last Modified: Wed, 02 Oct 2024 02:28:15 GMT  
		Size: 1.7 KB (1722 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0a2c690462db3acb9c8ea2bbb630cfab5b9b98f633cc9ec64b5b2c5444e7be0`  
		Last Modified: Wed, 02 Oct 2024 02:28:15 GMT  
		Size: 185.9 KB (185918 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:596149b2e241a0be2c3a02c666a885088c5a2797e39d82c63ef615aa52ecb1f5`  
		Last Modified: Wed, 02 Oct 2024 02:28:15 GMT  
		Size: 405.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2eb7abd8d1e04abc1a1571d74faf68a4dcab80fba5a2e0b9cdbc632d062a316`  
		Last Modified: Wed, 02 Oct 2024 02:28:16 GMT  
		Size: 115.5 KB (115536 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elasticsearch:8.15.2` - unknown; unknown

```console
$ docker pull elasticsearch@sha256:c808760bf1816945e50034390ee748550b3e0db8dee762aeef2c505e358f2785
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2893340 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:16da4a709df2c0a61476051b9c53224a787cd6da0bbbb31a25711d500378c199`

```dockerfile
```

-	Layers:
	-	`sha256:66cdb9f5feffd2848bf6e3498a283229613a980a804dbb4e7afb82a85ead3e22`  
		Last Modified: Wed, 02 Oct 2024 02:28:14 GMT  
		Size: 2.9 MB (2855489 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4067d326dcfc51de0a0ba0b154556805aab3bcc9d3dadce0f2ab3f775f753114`  
		Last Modified: Wed, 02 Oct 2024 02:28:13 GMT  
		Size: 37.9 KB (37851 bytes)  
		MIME: application/vnd.in-toto+json
