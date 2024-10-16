<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `elasticsearch`

-	[`elasticsearch:7.17.24`](#elasticsearch71724)
-	[`elasticsearch:8.15.2`](#elasticsearch8152)

## `elasticsearch:7.17.24`

```console
$ docker pull elasticsearch@sha256:b0d12b455e24b00539a119b0e6c88bcb7477bd6328a2c5c16ddfe7f39669357b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `elasticsearch:7.17.24` - linux; amd64

```console
$ docker pull elasticsearch@sha256:5810492498aae0c8192cfc2d80078b1ded1d35874e5fe4fb7e553588994d6af8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **362.6 MB (362620209 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fcd33427892e1f62e6d477e9dd8e54e1944ab3a498d9a8c31d19fd54ae3d7443`
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
ADD file:7486147a645d8835a5181c79f00a3606c6b714c83bcbfcd8862221eb14690f9e in / 
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
	-	`sha256:d9802f032d6798e2086607424bfe88cb8ec1d6f116e11cd99592dcaf261e9cd2`  
		Last Modified: Fri, 11 Oct 2024 04:41:25 GMT  
		Size: 27.5 MB (27511060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1ce9540ce7a62a5ac484e78f569d77bdf5b695b553cb3c22488480808f9a498`  
		Last Modified: Wed, 16 Oct 2024 16:16:22 GMT  
		Size: 7.5 MB (7523667 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:950db56af835e60c4a54cceb1abba8f57c8ece82c7fea1d755f98a6366ed4e49`  
		Last Modified: Wed, 16 Oct 2024 16:16:22 GMT  
		Size: 4.3 KB (4316 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92e4be3b6f0d9dcd6a9485464a977e98eaa2f8368e0133d2ca2f0fc2d2864f5e`  
		Last Modified: Wed, 16 Oct 2024 16:16:30 GMT  
		Size: 327.3 MB (327261515 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e7601da53979934ae41c31f49fdccd846fee83911e85d13758cb650ebdca650`  
		Last Modified: Wed, 16 Oct 2024 16:16:22 GMT  
		Size: 9.5 KB (9528 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e1e511a9416a7ee6f5e39e09bb9e9e351b46bdcc53f23ba3df9d19b42b575ab`  
		Last Modified: Wed, 16 Oct 2024 16:16:22 GMT  
		Size: 2.0 KB (1978 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78274466442a536d020064eee09ab3919ac26a34a72e39a42ff29f7e00ef35a8`  
		Last Modified: Wed, 16 Oct 2024 16:16:23 GMT  
		Size: 192.2 KB (192172 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f0778df447733ed210989db65987468c3c3ab06640ccf7b471160042d510c06`  
		Last Modified: Wed, 16 Oct 2024 16:16:24 GMT  
		Size: 404.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c5c09db317c96aec733aa5b09fb1de0d455265442bd4446ae4ec0fdcf70b69c`  
		Last Modified: Wed, 16 Oct 2024 16:16:24 GMT  
		Size: 115.5 KB (115537 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elasticsearch:7.17.24` - unknown; unknown

```console
$ docker pull elasticsearch@sha256:56086df5d5a884cadd1b38ac4fae519f55cc154bdb35e3c8b4e3d8876c010d75
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2545943 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:23ee65033bf727cdf27259a0c3f977f89c24a9c525ac026456ee85a718a016d5`

```dockerfile
```

-	Layers:
	-	`sha256:d0d4db6f6559243b919ed78428432a6e10502bebe43270b46424aeab428a08b1`  
		Last Modified: Wed, 16 Oct 2024 16:16:22 GMT  
		Size: 2.5 MB (2508271 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fd28aed3af91f693a10bded98daad9c8a61114615a55a2017208f8837688b54e`  
		Last Modified: Wed, 16 Oct 2024 16:16:22 GMT  
		Size: 37.7 KB (37672 bytes)  
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
$ docker pull elasticsearch@sha256:f4f986a9d0e078d35e9818bc5ac0b5d39157dfa840f12a95db7444f434000afe
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `elasticsearch:8.15.2` - linux; amd64

```console
$ docker pull elasticsearch@sha256:f8cac60da98f55ac2cf48882b7ddf57fe835a91078dcbb02211954009fe3f379
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **649.6 MB (649595181 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a853e8d425567ea8fbdc8b34ee509f987ae8951611bd9e20a10889ef5d1fdb5b`
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
ADD file:7486147a645d8835a5181c79f00a3606c6b714c83bcbfcd8862221eb14690f9e in / 
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
	-	`sha256:d9802f032d6798e2086607424bfe88cb8ec1d6f116e11cd99592dcaf261e9cd2`  
		Last Modified: Fri, 11 Oct 2024 04:41:25 GMT  
		Size: 27.5 MB (27511060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a121982e2b8da698e36c0660356b8f4c976b492cfb4e458a88866cb99ef75269`  
		Last Modified: Wed, 16 Oct 2024 16:15:44 GMT  
		Size: 7.5 MB (7523665 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6268225d6f152501c0d98fd8669faf4e881517e71b17ac099df55395113bb75`  
		Last Modified: Wed, 16 Oct 2024 16:15:43 GMT  
		Size: 4.3 KB (4311 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37aef8fbd672a0f8a0abb1ff114522eb1deb9e0ed95068ad5063eaf72abd4fc9`  
		Last Modified: Wed, 16 Oct 2024 16:15:59 GMT  
		Size: 614.2 MB (614237013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:141ddfe59bc47678cf760ed15ed1bf37bdaea08842ad62e0e4936071794f5fa9`  
		Last Modified: Wed, 16 Oct 2024 16:15:44 GMT  
		Size: 9.5 KB (9529 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dcc7fc6eaa2974fa94225f90363ff8e4b4030c4b71f7abebc80dc422e45bed94`  
		Last Modified: Wed, 16 Oct 2024 16:15:45 GMT  
		Size: 1.7 KB (1723 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:189e3c9793b726b834381adb607ba560bd84989b970c1c6fbf07b90ed0d4dd6e`  
		Last Modified: Wed, 16 Oct 2024 16:15:45 GMT  
		Size: 191.9 KB (191907 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1137a83a4a7f168a731f450c7350e5ec9c9a3874d78c89a072114b2d397faee6`  
		Last Modified: Wed, 16 Oct 2024 16:15:45 GMT  
		Size: 405.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a733100addc244b8de213f203cab80db237291f578555afcba853a1db541c8e`  
		Last Modified: Wed, 16 Oct 2024 16:15:46 GMT  
		Size: 115.5 KB (115536 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elasticsearch:8.15.2` - unknown; unknown

```console
$ docker pull elasticsearch@sha256:f00232285b9df7f83ea9f3ee5bef6d19bf8077497630c4d1d968db36f458fc5e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2894208 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c6df98549a57b42ce8e5e89d413888b09679269c01a11657f9f637eff223e005`

```dockerfile
```

-	Layers:
	-	`sha256:fd4909f509bb3361b3d6cf6111109e634349a0f056aaa0ea0fd014a7971164b0`  
		Last Modified: Wed, 16 Oct 2024 16:15:44 GMT  
		Size: 2.9 MB (2856520 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:468b9e08feb24cd17d4c4e4d7bcc4489af43cc6b8e023c36689f9bffd8bca88d`  
		Last Modified: Wed, 16 Oct 2024 16:15:44 GMT  
		Size: 37.7 KB (37688 bytes)  
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
