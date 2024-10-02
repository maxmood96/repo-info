<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `elasticsearch`

-	[`elasticsearch:7.17.24`](#elasticsearch71724)
-	[`elasticsearch:8.15.2`](#elasticsearch8152)

## `elasticsearch:7.17.24`

```console
$ docker pull elasticsearch@sha256:5e69055d9720e6e233c7183723e42bdc43f29327157de3b5405e63a0c677b4b3
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `elasticsearch:7.17.24` - linux; amd64

```console
$ docker pull elasticsearch@sha256:2a1716693c3d05580035686d114bf56b43f679361a2ce061b0ea999cdd2297b2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **362.6 MB (362604801 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:51456027c7320bb8f356513cdbc0a863ad8db794a624b91d40071c5dce59499e`
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
	-	`sha256:602d8ad51b8130f3fcd71cb936dea612ebc799666136abf2e5914585b3178a4a`  
		Last Modified: Tue, 13 Aug 2024 10:23:50 GMT  
		Size: 27.5 MB (27511769 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9dabe8716c11f424e0e365dd071184cf6a3615fe534a9947513640251dd9064`  
		Last Modified: Tue, 10 Sep 2024 21:58:06 GMT  
		Size: 7.5 MB (7513902 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7244d17a6b1f468b9e5c67f2c2b1d4244a2c81421a263c08020f4b87df646fe`  
		Last Modified: Tue, 10 Sep 2024 21:58:06 GMT  
		Size: 4.3 KB (4314 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8a19a50b790b7ed3b533ea195fb59ed3fdc2162d019b01a73c30bb8fb0e5fec`  
		Last Modified: Tue, 10 Sep 2024 21:58:11 GMT  
		Size: 327.3 MB (327261447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c70688f5dcf9e66016c8299b59bdf09bede81af5ab198ab75d2927c3be36be30`  
		Last Modified: Tue, 10 Sep 2024 21:58:06 GMT  
		Size: 9.5 KB (9530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:211fb306b6333a0cb9b1298537e2dc52a164bc61e1cd4067f9771c7d96ed7ca1`  
		Last Modified: Tue, 10 Sep 2024 21:58:06 GMT  
		Size: 2.0 KB (1977 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c4207a4d164f3724af7afcc6173322d0262bd8a386001c1f09cc916e2f25f1f`  
		Last Modified: Tue, 10 Sep 2024 21:58:07 GMT  
		Size: 192.2 KB (192172 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a13bbea473ab3565505f1dd185e07e2993f5096fd9495493a35c9e338f5c18d`  
		Last Modified: Tue, 10 Sep 2024 21:58:07 GMT  
		Size: 406.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed42f21c49fff3cbbfb2067165ebd63a49c89e177c7d13278de2034d2cae9025`  
		Last Modified: Tue, 10 Sep 2024 21:58:07 GMT  
		Size: 109.3 KB (109252 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elasticsearch:7.17.24` - unknown; unknown

```console
$ docker pull elasticsearch@sha256:14c7110c67a6af2aafbb9d1f08a6b4d7b1f33a20aa1ce20e2802266f9aa73e3f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2404881 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8605372f8c83194cfc8100e73f54c805e22b3af36b74ad9cfe86adcd96b88cfc`

```dockerfile
```

-	Layers:
	-	`sha256:757d1febf9677acb3d95cd2aff81a9261323ad567e2ba71586bff7e5e4e9d7a0`  
		Last Modified: Tue, 10 Sep 2024 21:58:06 GMT  
		Size: 2.4 MB (2367247 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7ebed7d3cbe6ddd2df5f768bec2b0e09cccaa5e241b157e8de9b1975d3d6ccf7`  
		Last Modified: Tue, 10 Sep 2024 21:58:06 GMT  
		Size: 37.6 KB (37634 bytes)  
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
$ docker pull elasticsearch@sha256:0df801ff5313073df19a2bf00e440d84c7ac15835511e8efcc2ed83239076190
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `elasticsearch:8.15.2` - linux; amd64

```console
$ docker pull elasticsearch@sha256:538fd060e372edbdad6dd2c17092d20cbdcfafccbe96a0248eccdc279649c59b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **650.0 MB (650007698 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4144bf34cabc977ba39487ef20a5229893e6fde40f57a7881101ab0388750472`
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
	-	`sha256:602d8ad51b8130f3fcd71cb936dea612ebc799666136abf2e5914585b3178a4a`  
		Last Modified: Tue, 13 Aug 2024 10:23:50 GMT  
		Size: 27.5 MB (27511769 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5aa49cd3400e268dafce962ecd21fb4651272871e170c76fbccf707a64d8adea`  
		Last Modified: Thu, 26 Sep 2024 22:58:08 GMT  
		Size: 7.9 MB (7935475 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68f8e1a1de8ebe5f8710ed7e25af83a9ff5768633411be49bcd09ef6af688886`  
		Last Modified: Thu, 26 Sep 2024 22:58:08 GMT  
		Size: 4.3 KB (4316 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc74c001e63c567dadd8d007d1b68de29a506508ee7af4ce02141b0fc422a965`  
		Last Modified: Thu, 26 Sep 2024 22:58:17 GMT  
		Size: 614.2 MB (614237007 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:782ec43f9bd53476c6f80ad34eda78da2bf0fe2024ac6296751c16415e71ce7d`  
		Last Modified: Thu, 26 Sep 2024 22:58:08 GMT  
		Size: 9.5 KB (9528 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eee34f68e3ff1432cacd677bb7f2231e34068bc3eee238d08c5a2ed664bf862c`  
		Last Modified: Thu, 26 Sep 2024 22:58:09 GMT  
		Size: 1.7 KB (1721 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:418344dad4838f38235527c4a3f7184eb2a3a4ded8f59a42f687f7cb8c74e6e4`  
		Last Modified: Thu, 26 Sep 2024 22:58:09 GMT  
		Size: 191.9 KB (191908 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e29aa6f39a41a9727475e7aff474d98ba97a9d91f0c8af2e4319d0d96ada7055`  
		Last Modified: Thu, 26 Sep 2024 22:58:09 GMT  
		Size: 406.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37326dc704bc3af9f8dde6e32f15a2c76441478ae3707bb4b588867a7b6bb017`  
		Last Modified: Thu, 26 Sep 2024 22:58:10 GMT  
		Size: 115.5 KB (115536 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elasticsearch:8.15.2` - unknown; unknown

```console
$ docker pull elasticsearch@sha256:c2307dacca12d4e6aaae406d8bb3a88d063524e63cdfe37e8284d51f39105e2e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2894170 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a1f8185e3b2c1ee20376efd2d00dcd4f6ae01918267ce6d64ff1059ecf18a515`

```dockerfile
```

-	Layers:
	-	`sha256:6c138b1219a4c686cfc7cad31920125e47bf55d64c30afb64347e8eab3e6d41f`  
		Last Modified: Thu, 26 Sep 2024 22:58:08 GMT  
		Size: 2.9 MB (2856520 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f1842a457cc73f39e817ef5beff20d999a095c232273dae35bcc92ca16d90507`  
		Last Modified: Thu, 26 Sep 2024 22:58:08 GMT  
		Size: 37.6 KB (37650 bytes)  
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
