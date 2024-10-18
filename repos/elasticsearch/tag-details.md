<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `elasticsearch`

-	[`elasticsearch:7.17.24`](#elasticsearch71724)
-	[`elasticsearch:8.15.3`](#elasticsearch8153)

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

## `elasticsearch:8.15.3`

```console
$ docker pull elasticsearch@sha256:54468761d3c815759843c1bdde088604c13ac0e45c626750c0a9bd0a43c0da3e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `elasticsearch:8.15.3` - linux; amd64

```console
$ docker pull elasticsearch@sha256:2690b9545898cb1cba114eda687b60a500c071898f20265eb8ae8fdd23908ba6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **650.2 MB (650203462 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e72d9686af70e3636215b50f493116f483b8692c6cb93d21a24e018d6796ea15`
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
# Thu, 17 Oct 2024 12:21:47 GMT
RUN yes no | dpkg-reconfigure dash &&     for iter in 1 2 3 4 5 6 7 8 9 10; do       export DEBIAN_FRONTEND=noninteractive &&       apt-get update &&       apt-get upgrade -y &&       apt-get install -y --no-install-recommends         ca-certificates curl netcat p11-kit unzip zip  &&       apt-get clean &&       rm -rf /var/lib/apt/lists/* &&       exit_code=0 && break ||         exit_code=$? && echo "apt-get error: retry $iter in 10s" && sleep 10;     done;     exit $exit_code # buildkit
# Thu, 17 Oct 2024 12:21:47 GMT
RUN groupadd -g 1000 elasticsearch &&     adduser --uid 1000 --gid 1000 --home /usr/share/elasticsearch elasticsearch &&     adduser elasticsearch root &&     chown -R 0:0 /usr/share/elasticsearch # buildkit
# Thu, 17 Oct 2024 12:21:47 GMT
ENV ELASTIC_CONTAINER=true
# Thu, 17 Oct 2024 12:21:47 GMT
WORKDIR /usr/share/elasticsearch
# Thu, 17 Oct 2024 12:21:47 GMT
COPY --chown=0:0 /usr/share/elasticsearch /usr/share/elasticsearch # buildkit
# Thu, 17 Oct 2024 12:21:47 GMT
COPY --chown=0:0 /bin/tini /bin/tini # buildkit
# Thu, 17 Oct 2024 12:21:47 GMT
ENV PATH=/usr/share/elasticsearch/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 17 Oct 2024 12:21:47 GMT
COPY bin/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh # buildkit
# Thu, 17 Oct 2024 12:21:47 GMT
RUN chmod g=u /etc/passwd &&     chmod 0555 /usr/local/bin/docker-entrypoint.sh &&     find / -xdev -perm -4000 -exec chmod ug-s {} + &&     chmod 0775 /usr/share/elasticsearch &&     chown elasticsearch bin config config/jvm.options.d data logs plugins # buildkit
# Thu, 17 Oct 2024 12:21:47 GMT
COPY bin/docker-openjdk /etc/ca-certificates/update.d/docker-openjdk # buildkit
# Thu, 17 Oct 2024 12:21:47 GMT
RUN /etc/ca-certificates/update.d/docker-openjdk # buildkit
# Thu, 17 Oct 2024 12:21:47 GMT
EXPOSE map[9200/tcp:{} 9300/tcp:{}]
# Thu, 17 Oct 2024 12:21:47 GMT
LABEL org.label-schema.build-date=2024-10-09T22:08:00.328917561Z org.label-schema.license=Elastic-License-2.0 org.label-schema.name=Elasticsearch org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/elasticsearch org.label-schema.usage=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.label-schema.vcs-ref=f97532e680b555c3a05e73a74c28afb666923018 org.label-schema.vcs-url=https://github.com/elastic/elasticsearch org.label-schema.vendor=Elastic org.label-schema.version=8.15.3 org.opencontainers.image.created=2024-10-09T22:08:00.328917561Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.opencontainers.image.licenses=Elastic-License-2.0 org.opencontainers.image.revision=f97532e680b555c3a05e73a74c28afb666923018 org.opencontainers.image.source=https://github.com/elastic/elasticsearch org.opencontainers.image.title=Elasticsearch org.opencontainers.image.url=https://www.elastic.co/products/elasticsearch org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=8.15.3
# Thu, 17 Oct 2024 12:21:47 GMT
ENTRYPOINT ["/bin/tini" "--" "/usr/local/bin/docker-entrypoint.sh"]
# Thu, 17 Oct 2024 12:21:47 GMT
CMD ["eswrapper"]
# Thu, 17 Oct 2024 12:21:47 GMT
USER 1000:0
```

-	Layers:
	-	`sha256:d9802f032d6798e2086607424bfe88cb8ec1d6f116e11cd99592dcaf261e9cd2`  
		Last Modified: Fri, 11 Oct 2024 04:41:25 GMT  
		Size: 27.5 MB (27511060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc4b793b4c8c52aa9f3c852bf62680d695c08768f5135c7ceee8e61ea9b6b0e2`  
		Last Modified: Thu, 17 Oct 2024 20:59:10 GMT  
		Size: 7.5 MB (7523758 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c906761a986525513cfd8dbdc3d9a19944fa0e13960068dc26c5cdb456721f9a`  
		Last Modified: Thu, 17 Oct 2024 20:59:10 GMT  
		Size: 4.3 KB (4311 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c183ad3bd8a3e053d7acbccc66d21d4ce7f650bf269037fb1e661a4d4352f86b`  
		Last Modified: Thu, 17 Oct 2024 20:59:18 GMT  
		Size: 614.8 MB (614845210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef9d54640409fcca31b61bfe6c98f0401b17e81d4675b29ad073ea450a9ce29c`  
		Last Modified: Thu, 17 Oct 2024 20:59:10 GMT  
		Size: 9.5 KB (9528 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16c61b4194a094fcb55a5c51ba6176068f7e2a1a3c6dfed871d8468200eb3dd6`  
		Last Modified: Thu, 17 Oct 2024 20:59:11 GMT  
		Size: 1.7 KB (1722 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4d4ae1d77a296deab71413dfcf6150b0f4cff2dfd7a998a4c3ff847783cbd39`  
		Last Modified: Thu, 17 Oct 2024 20:59:11 GMT  
		Size: 191.9 KB (191904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70d788479c6bf1512c9578187d54ded1affee689b2dfa6a71b29e07059445bd3`  
		Last Modified: Thu, 17 Oct 2024 20:59:11 GMT  
		Size: 404.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e374f4ff29ffce15f4c8c6af65db8b0c8fff1dd97c74d4d5c85729a96bd447af`  
		Last Modified: Thu, 17 Oct 2024 20:59:12 GMT  
		Size: 115.5 KB (115533 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elasticsearch:8.15.3` - unknown; unknown

```console
$ docker pull elasticsearch@sha256:94893219150f6abf8ee7fece463e79557647dd6c504c117f330289088d14bddc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2894218 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d1b198d41f81cf18fb9c9fb26f9d8f99f54ba5a297d0664c5c408da67bd45e5e`

```dockerfile
```

-	Layers:
	-	`sha256:2cf2ca410c9704094a5ff2f19cf445b31dcfa049702ad299505f34f98a831ba6`  
		Last Modified: Thu, 17 Oct 2024 20:59:10 GMT  
		Size: 2.9 MB (2856530 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9cbb504a18d038974de7185911b4f9b089a17b3b833c632824ce981e1f347812`  
		Last Modified: Thu, 17 Oct 2024 20:59:10 GMT  
		Size: 37.7 KB (37688 bytes)  
		MIME: application/vnd.in-toto+json

### `elasticsearch:8.15.3` - linux; arm64 variant v8

```console
$ docker pull elasticsearch@sha256:ef32189bb3fdcfaf3dc1f9d50444883380e26cbb3c8fc88820faf9f67d3a2228
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **493.7 MB (493713691 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cfcebb5958a96d48404026e016384940f776b434fd8f33f9e5dd24723cf799fb`
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
# Thu, 17 Oct 2024 12:21:47 GMT
RUN yes no | dpkg-reconfigure dash &&     for iter in 1 2 3 4 5 6 7 8 9 10; do       export DEBIAN_FRONTEND=noninteractive &&       apt-get update &&       apt-get upgrade -y &&       apt-get install -y --no-install-recommends         ca-certificates curl netcat p11-kit unzip zip  &&       apt-get clean &&       rm -rf /var/lib/apt/lists/* &&       exit_code=0 && break ||         exit_code=$? && echo "apt-get error: retry $iter in 10s" && sleep 10;     done;     exit $exit_code # buildkit
# Thu, 17 Oct 2024 12:21:47 GMT
RUN groupadd -g 1000 elasticsearch &&     adduser --uid 1000 --gid 1000 --home /usr/share/elasticsearch elasticsearch &&     adduser elasticsearch root &&     chown -R 0:0 /usr/share/elasticsearch # buildkit
# Thu, 17 Oct 2024 12:21:47 GMT
ENV ELASTIC_CONTAINER=true
# Thu, 17 Oct 2024 12:21:47 GMT
WORKDIR /usr/share/elasticsearch
# Thu, 17 Oct 2024 12:21:47 GMT
COPY --chown=0:0 /usr/share/elasticsearch /usr/share/elasticsearch # buildkit
# Thu, 17 Oct 2024 12:21:47 GMT
COPY --chown=0:0 /bin/tini /bin/tini # buildkit
# Thu, 17 Oct 2024 12:21:47 GMT
ENV PATH=/usr/share/elasticsearch/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 17 Oct 2024 12:21:47 GMT
COPY bin/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh # buildkit
# Thu, 17 Oct 2024 12:21:47 GMT
RUN chmod g=u /etc/passwd &&     chmod 0555 /usr/local/bin/docker-entrypoint.sh &&     find / -xdev -perm -4000 -exec chmod ug-s {} + &&     chmod 0775 /usr/share/elasticsearch &&     chown elasticsearch bin config config/jvm.options.d data logs plugins # buildkit
# Thu, 17 Oct 2024 12:21:47 GMT
COPY bin/docker-openjdk /etc/ca-certificates/update.d/docker-openjdk # buildkit
# Thu, 17 Oct 2024 12:21:47 GMT
RUN /etc/ca-certificates/update.d/docker-openjdk # buildkit
# Thu, 17 Oct 2024 12:21:47 GMT
EXPOSE map[9200/tcp:{} 9300/tcp:{}]
# Thu, 17 Oct 2024 12:21:47 GMT
LABEL org.label-schema.build-date=2024-10-09T22:08:00.328917561Z org.label-schema.license=Elastic-License-2.0 org.label-schema.name=Elasticsearch org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/elasticsearch org.label-schema.usage=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.label-schema.vcs-ref=f97532e680b555c3a05e73a74c28afb666923018 org.label-schema.vcs-url=https://github.com/elastic/elasticsearch org.label-schema.vendor=Elastic org.label-schema.version=8.15.3 org.opencontainers.image.created=2024-10-09T22:08:00.328917561Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.opencontainers.image.licenses=Elastic-License-2.0 org.opencontainers.image.revision=f97532e680b555c3a05e73a74c28afb666923018 org.opencontainers.image.source=https://github.com/elastic/elasticsearch org.opencontainers.image.title=Elasticsearch org.opencontainers.image.url=https://www.elastic.co/products/elasticsearch org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=8.15.3
# Thu, 17 Oct 2024 12:21:47 GMT
ENTRYPOINT ["/bin/tini" "--" "/usr/local/bin/docker-entrypoint.sh"]
# Thu, 17 Oct 2024 12:21:47 GMT
CMD ["eswrapper"]
# Thu, 17 Oct 2024 12:21:47 GMT
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
	-	`sha256:7168973486737c052342f699752a25c90e0093c8bd18174c43e9ca416f097206`  
		Last Modified: Thu, 17 Oct 2024 22:14:32 GMT  
		Size: 460.1 MB (460075484 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1fcba5a230599c3a61b4055ccd5d34a283ca58dc0805dea38fc7e28ae0c4a76`  
		Last Modified: Thu, 17 Oct 2024 22:14:21 GMT  
		Size: 9.1 KB (9106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13d9e5ced205af77fc609cda9b41bf2893970386913cdd003abc41598bf9c780`  
		Last Modified: Thu, 17 Oct 2024 22:14:21 GMT  
		Size: 1.7 KB (1723 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21bef60dc004c45d8449424e139ccf07dffb2cb295f3082648dc621da68b8b41`  
		Last Modified: Thu, 17 Oct 2024 22:14:22 GMT  
		Size: 185.9 KB (185922 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68ba8d2cfc8d6c8b91b7146da181ff0aba0c77f4b1dd49178eb7bcf89ca12d81`  
		Last Modified: Thu, 17 Oct 2024 22:14:22 GMT  
		Size: 411.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:969dcaffb4e4cc846c28e70365ba9a61f5f82f9d220503213293d84755573faa`  
		Last Modified: Thu, 17 Oct 2024 22:14:23 GMT  
		Size: 115.5 KB (115541 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elasticsearch:8.15.3` - unknown; unknown

```console
$ docker pull elasticsearch@sha256:e86771d80a201d69738ecafcb8b6b6a4c25d5870fcd4e86a384e0bb8355f06be
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2893384 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b047b918948c954afb4fdfe2d31ed8663dad4e405eeaa0dcbe9878bb17964257`

```dockerfile
```

-	Layers:
	-	`sha256:d29d0e90666df36fa8292b72ed559aeb0fc95fc48d21f9af69ad6daac7397fd1`  
		Last Modified: Thu, 17 Oct 2024 22:14:22 GMT  
		Size: 2.9 MB (2855499 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a16bf7ca56f2d6f7397a59fde7133c453807fc1cb07c4f1feb26d4202bc41f99`  
		Last Modified: Thu, 17 Oct 2024 22:14:21 GMT  
		Size: 37.9 KB (37885 bytes)  
		MIME: application/vnd.in-toto+json
