<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `elasticsearch`

-	[`elasticsearch:7.17.24`](#elasticsearch71724)
-	[`elasticsearch:8.15.1`](#elasticsearch8151)

## `elasticsearch:7.17.24`

```console
$ docker pull elasticsearch@sha256:4596f5bbcfad34f0dd525ad578b18ef86289e677d149d749c07cd65df719d2a7
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
$ docker pull elasticsearch@sha256:6645e361ec3885495887371c7fa2590bfbd5d6de59b9de476692649f8f62cb60
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **358.5 MB (358539031 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b7568e2d526a99f5db6582bc2aaddbfc9ccd4b719ca75dfed3d89473e361c71`
-	Entrypoint: `["\/bin\/tini","--","\/usr\/local\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["eswrapper"]`

```dockerfile
# Tue, 13 Aug 2024 09:27:56 GMT
ARG RELEASE
# Tue, 13 Aug 2024 09:27:56 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Aug 2024 09:27:56 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Aug 2024 09:27:56 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 13 Aug 2024 09:27:58 GMT
ADD file:6d8cc056ee741f09a6c7d965d8e2027d80ed2eccbfb0312593ce52d9256db437 in / 
# Tue, 13 Aug 2024 09:27:58 GMT
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
	-	`sha256:6a1df50fc4815789598fa24d3ecacb70451e506447ab9e45665024b9f3f0233b`  
		Last Modified: Tue, 13 Aug 2024 10:23:55 GMT  
		Size: 26.0 MB (25974217 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c65bff5fa2fe382fb00d7c1d29586c3afb6c2fbd819c4a13affc34bb8798cb0`  
		Last Modified: Tue, 10 Sep 2024 21:59:57 GMT  
		Size: 7.3 MB (7333113 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fd7126b6d48a07d0a3dcfc121fa6161a49bf3861fa6e0ffa62e45a677ad7308`  
		Last Modified: Tue, 10 Sep 2024 21:59:57 GMT  
		Size: 4.3 KB (4320 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7a44a318da1d813692c4f91c1a6a4ee7caca78199ab282968477095f74785df`  
		Last Modified: Tue, 10 Sep 2024 22:00:08 GMT  
		Size: 324.9 MB (324920442 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:478e18727fbee2b89c50d4ca6da585cd59a913d4779fd9df6aa3c7a198f6385e`  
		Last Modified: Tue, 10 Sep 2024 21:59:58 GMT  
		Size: 9.1 KB (9096 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db542f74c5185323be7fb2d0477498912d4147bf18f76fa357b96e2ad68f09d0`  
		Last Modified: Tue, 10 Sep 2024 21:59:58 GMT  
		Size: 2.0 KB (1981 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be6b945bde2f1623f5039edd79509689798269a48c8f9aea162c36b5fa3b757e`  
		Last Modified: Tue, 10 Sep 2024 21:59:59 GMT  
		Size: 186.2 KB (186178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1907b0e598fc77638b40b916885ce3ad6a4068a171ada97d1c5c94266ec8d77f`  
		Last Modified: Tue, 10 Sep 2024 21:59:59 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:757bd77312299a99bdca1cce494c1329a2ead6481cebf831691bfdee0abd4e69`  
		Last Modified: Tue, 10 Sep 2024 22:00:00 GMT  
		Size: 109.2 KB (109249 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elasticsearch:7.17.24` - unknown; unknown

```console
$ docker pull elasticsearch@sha256:5987639b49290a4b3b52f1c51b46c7001793f28b2d825ceea67879eddbe78faa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2405378 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:66010b1d1b5ec0e4584e5fbc7ae3127b9e298a762f62787b82947bd71f05e3f9`

```dockerfile
```

-	Layers:
	-	`sha256:1149b593e16b43e7afab9388b474e33f4b776385fdf8a841b4c3e08a6ebc80a9`  
		Last Modified: Tue, 10 Sep 2024 21:59:57 GMT  
		Size: 2.4 MB (2367479 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:64d216d8589ce4f30aaf551804e3f07831cba63d9acdd95923ede70e2dc01c68`  
		Last Modified: Tue, 10 Sep 2024 21:59:57 GMT  
		Size: 37.9 KB (37899 bytes)  
		MIME: application/vnd.in-toto+json

## `elasticsearch:8.15.1`

```console
$ docker pull elasticsearch@sha256:67068465d6fdfaffa9ae6854ca2f6d43cc1308b93e88d2410fb15590f9f659b9
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `elasticsearch:8.15.1` - linux; amd64

```console
$ docker pull elasticsearch@sha256:f84d8baaa9b942369ae10a004d461be8f4c0312b8e180c3c1c24843ff1811354
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **647.1 MB (647130258 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:93fbfc36e85a61b24b400f40614b56703d37a967e26eb7aed1a9a196cf3a2d57`
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
# Thu, 05 Sep 2024 16:37:13 GMT
RUN yes no | dpkg-reconfigure dash &&     for iter in 1 2 3 4 5 6 7 8 9 10; do       export DEBIAN_FRONTEND=noninteractive &&       apt-get update &&       apt-get upgrade -y &&       apt-get install -y --no-install-recommends         ca-certificates curl netcat p11-kit unzip zip  &&       apt-get clean &&       rm -rf /var/lib/apt/lists/* &&       exit_code=0 && break ||         exit_code=$? && echo "apt-get error: retry $iter in 10s" && sleep 10;     done;     exit $exit_code # buildkit
# Thu, 05 Sep 2024 16:37:13 GMT
RUN groupadd -g 1000 elasticsearch &&     adduser --uid 1000 --gid 1000 --home /usr/share/elasticsearch elasticsearch &&     adduser elasticsearch root &&     chown -R 0:0 /usr/share/elasticsearch # buildkit
# Thu, 05 Sep 2024 16:37:13 GMT
ENV ELASTIC_CONTAINER=true
# Thu, 05 Sep 2024 16:37:13 GMT
WORKDIR /usr/share/elasticsearch
# Thu, 05 Sep 2024 16:37:13 GMT
COPY --chown=0:0 /usr/share/elasticsearch /usr/share/elasticsearch # buildkit
# Thu, 05 Sep 2024 16:37:13 GMT
COPY --chown=0:0 /bin/tini /bin/tini # buildkit
# Thu, 05 Sep 2024 16:37:13 GMT
ENV PATH=/usr/share/elasticsearch/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 05 Sep 2024 16:37:13 GMT
COPY bin/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh # buildkit
# Thu, 05 Sep 2024 16:37:13 GMT
RUN chmod g=u /etc/passwd &&     chmod 0555 /usr/local/bin/docker-entrypoint.sh &&     find / -xdev -perm -4000 -exec chmod ug-s {} + &&     chmod 0775 /usr/share/elasticsearch &&     chown elasticsearch bin config config/jvm.options.d data logs plugins # buildkit
# Thu, 05 Sep 2024 16:37:13 GMT
COPY bin/docker-openjdk /etc/ca-certificates/update.d/docker-openjdk # buildkit
# Thu, 05 Sep 2024 16:37:13 GMT
RUN /etc/ca-certificates/update.d/docker-openjdk # buildkit
# Thu, 05 Sep 2024 16:37:13 GMT
EXPOSE map[9200/tcp:{} 9300/tcp:{}]
# Thu, 05 Sep 2024 16:37:13 GMT
LABEL org.label-schema.build-date=2024-09-02T22:04:47.310170297Z org.label-schema.license=Elastic-License-2.0 org.label-schema.name=Elasticsearch org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/elasticsearch org.label-schema.usage=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.label-schema.vcs-ref=253e8544a65ad44581194068936f2a5d57c2c051 org.label-schema.vcs-url=https://github.com/elastic/elasticsearch org.label-schema.vendor=Elastic org.label-schema.version=8.15.1 org.opencontainers.image.created=2024-09-02T22:04:47.310170297Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.opencontainers.image.licenses=Elastic-License-2.0 org.opencontainers.image.revision=253e8544a65ad44581194068936f2a5d57c2c051 org.opencontainers.image.source=https://github.com/elastic/elasticsearch org.opencontainers.image.title=Elasticsearch org.opencontainers.image.url=https://www.elastic.co/products/elasticsearch org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=8.15.1
# Thu, 05 Sep 2024 16:37:13 GMT
ENTRYPOINT ["/bin/tini" "--" "/usr/local/bin/docker-entrypoint.sh"]
# Thu, 05 Sep 2024 16:37:13 GMT
CMD ["eswrapper"]
# Thu, 05 Sep 2024 16:37:13 GMT
USER 1000:0
```

-	Layers:
	-	`sha256:602d8ad51b8130f3fcd71cb936dea612ebc799666136abf2e5914585b3178a4a`  
		Last Modified: Tue, 13 Aug 2024 10:23:50 GMT  
		Size: 27.5 MB (27511769 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b95b60f66d56942c54cd13a9820f7dae1868a82bad472d84774d913bb742d73`  
		Last Modified: Thu, 05 Sep 2024 22:04:28 GMT  
		Size: 7.5 MB (7513902 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb3e6cafd3434d657ea43c621a583e76e69c46283ae860c94c13c9fd69128861`  
		Last Modified: Thu, 05 Sep 2024 22:04:27 GMT  
		Size: 4.3 KB (4313 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99828d28b577aaf1398455335d41c3429a43895a105313aa2b3cdc1acafccafb`  
		Last Modified: Thu, 05 Sep 2024 22:04:41 GMT  
		Size: 611.8 MB (611787428 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a77363ade226b31590902b25c00bd2cd6fb62de54c6956aea1ccbab5869b013`  
		Last Modified: Thu, 05 Sep 2024 22:04:27 GMT  
		Size: 9.5 KB (9529 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af69f436ae3345918d5cc89702c259358c76777979087784cd6b67781e4c6138`  
		Last Modified: Thu, 05 Sep 2024 22:04:28 GMT  
		Size: 1.7 KB (1723 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a59e81334a8e3ca4c5b89d70649558b20a8df799a2c8502ba12d6f75fa85379`  
		Last Modified: Thu, 05 Sep 2024 22:04:29 GMT  
		Size: 191.9 KB (191904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44d4c8544a10eaedb283ceb70c8109a1cdf8f872836e023c035dcec7f85bd16f`  
		Last Modified: Thu, 05 Sep 2024 22:04:29 GMT  
		Size: 406.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ae0a4f99837c56622610f90470967d09d8cd4fc41277cdd9e1da9d0843dd1e4`  
		Last Modified: Thu, 05 Sep 2024 22:04:29 GMT  
		Size: 109.3 KB (109252 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elasticsearch:8.15.1` - unknown; unknown

```console
$ docker pull elasticsearch@sha256:9bc86c5e305a123b5b0d7e2511d238cff9332da099b132fda94c40a8f48f1341
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2753146 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e6bc7fde9541eb89228e5123f360a08c5365a867fe56e1f982a064635f848b81`

```dockerfile
```

-	Layers:
	-	`sha256:72189e77bee3a90da2fbfa1d49df489de8f462a643c72087e113b8c5bcbcf950`  
		Last Modified: Thu, 05 Sep 2024 22:04:28 GMT  
		Size: 2.7 MB (2715496 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:75b5edce67e2fa451e40ec0797c07992e42ea192b100a2fe9440aa7757bd86c6`  
		Last Modified: Thu, 05 Sep 2024 22:04:27 GMT  
		Size: 37.6 KB (37650 bytes)  
		MIME: application/vnd.in-toto+json

### `elasticsearch:8.15.1` - linux; arm64 variant v8

```console
$ docker pull elasticsearch@sha256:26807d4b905098fe70fefe60f80ae2504d6b526d7ceeb00c72b757e8510fc839
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **491.2 MB (491227078 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a4408d0c0156dbb69eb873e666e9b9b12f2b7255f876102a550050947b5f9d7`
-	Entrypoint: `["\/bin\/tini","--","\/usr\/local\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["eswrapper"]`

```dockerfile
# Tue, 13 Aug 2024 09:27:56 GMT
ARG RELEASE
# Tue, 13 Aug 2024 09:27:56 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Aug 2024 09:27:56 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Aug 2024 09:27:56 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 13 Aug 2024 09:27:58 GMT
ADD file:6d8cc056ee741f09a6c7d965d8e2027d80ed2eccbfb0312593ce52d9256db437 in / 
# Tue, 13 Aug 2024 09:27:58 GMT
CMD ["/bin/bash"]
# Thu, 05 Sep 2024 16:37:13 GMT
RUN yes no | dpkg-reconfigure dash &&     for iter in 1 2 3 4 5 6 7 8 9 10; do       export DEBIAN_FRONTEND=noninteractive &&       apt-get update &&       apt-get upgrade -y &&       apt-get install -y --no-install-recommends         ca-certificates curl netcat p11-kit unzip zip  &&       apt-get clean &&       rm -rf /var/lib/apt/lists/* &&       exit_code=0 && break ||         exit_code=$? && echo "apt-get error: retry $iter in 10s" && sleep 10;     done;     exit $exit_code # buildkit
# Thu, 05 Sep 2024 16:37:13 GMT
RUN groupadd -g 1000 elasticsearch &&     adduser --uid 1000 --gid 1000 --home /usr/share/elasticsearch elasticsearch &&     adduser elasticsearch root &&     chown -R 0:0 /usr/share/elasticsearch # buildkit
# Thu, 05 Sep 2024 16:37:13 GMT
ENV ELASTIC_CONTAINER=true
# Thu, 05 Sep 2024 16:37:13 GMT
WORKDIR /usr/share/elasticsearch
# Thu, 05 Sep 2024 16:37:13 GMT
COPY --chown=0:0 /usr/share/elasticsearch /usr/share/elasticsearch # buildkit
# Thu, 05 Sep 2024 16:37:13 GMT
COPY --chown=0:0 /bin/tini /bin/tini # buildkit
# Thu, 05 Sep 2024 16:37:13 GMT
ENV PATH=/usr/share/elasticsearch/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 05 Sep 2024 16:37:13 GMT
COPY bin/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh # buildkit
# Thu, 05 Sep 2024 16:37:13 GMT
RUN chmod g=u /etc/passwd &&     chmod 0555 /usr/local/bin/docker-entrypoint.sh &&     find / -xdev -perm -4000 -exec chmod ug-s {} + &&     chmod 0775 /usr/share/elasticsearch &&     chown elasticsearch bin config config/jvm.options.d data logs plugins # buildkit
# Thu, 05 Sep 2024 16:37:13 GMT
COPY bin/docker-openjdk /etc/ca-certificates/update.d/docker-openjdk # buildkit
# Thu, 05 Sep 2024 16:37:13 GMT
RUN /etc/ca-certificates/update.d/docker-openjdk # buildkit
# Thu, 05 Sep 2024 16:37:13 GMT
EXPOSE map[9200/tcp:{} 9300/tcp:{}]
# Thu, 05 Sep 2024 16:37:13 GMT
LABEL org.label-schema.build-date=2024-09-02T22:04:47.310170297Z org.label-schema.license=Elastic-License-2.0 org.label-schema.name=Elasticsearch org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/elasticsearch org.label-schema.usage=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.label-schema.vcs-ref=253e8544a65ad44581194068936f2a5d57c2c051 org.label-schema.vcs-url=https://github.com/elastic/elasticsearch org.label-schema.vendor=Elastic org.label-schema.version=8.15.1 org.opencontainers.image.created=2024-09-02T22:04:47.310170297Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.opencontainers.image.licenses=Elastic-License-2.0 org.opencontainers.image.revision=253e8544a65ad44581194068936f2a5d57c2c051 org.opencontainers.image.source=https://github.com/elastic/elasticsearch org.opencontainers.image.title=Elasticsearch org.opencontainers.image.url=https://www.elastic.co/products/elasticsearch org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=8.15.1
# Thu, 05 Sep 2024 16:37:13 GMT
ENTRYPOINT ["/bin/tini" "--" "/usr/local/bin/docker-entrypoint.sh"]
# Thu, 05 Sep 2024 16:37:13 GMT
CMD ["eswrapper"]
# Thu, 05 Sep 2024 16:37:13 GMT
USER 1000:0
```

-	Layers:
	-	`sha256:f02209be4ee528c246399de81af4552e52adb005a8a499815607b6b0d42746bf`  
		Last Modified: Mon, 03 Jun 2024 17:19:48 GMT  
		Size: 26.0 MB (25974217 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:170d61ad04e3e11176a3e82cedd5cff709c010408c47b4030a7dfdd6edae7b4e`  
		Last Modified: Sat, 17 Aug 2024 02:16:44 GMT  
		Size: 7.3 MB (7333143 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6b8bcace31ea0038c023ce3b62483ec3c8d1504fb589a6004cf09df522473af`  
		Last Modified: Sat, 17 Aug 2024 02:16:43 GMT  
		Size: 4.3 KB (4321 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8579b28f71175a4a81dcbd28c2128ec176f3e861b04c2b1358865c10afdb5551`  
		Last Modified: Thu, 05 Sep 2024 22:08:05 GMT  
		Size: 457.6 MB (457608949 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53bbfb99c2ad899728cb7f97546be0fd5839a835246869e4d3f23a0326dcae80`  
		Last Modified: Thu, 05 Sep 2024 22:07:55 GMT  
		Size: 9.1 KB (9104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42efceb71ab4330839ab2a2b3559ba8bacce0360570d46c375f3a8abe98ab03f`  
		Last Modified: Thu, 05 Sep 2024 22:07:55 GMT  
		Size: 1.7 KB (1726 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cab0f68545a81e1e9d3e57859e646886f56ea3909c686ba3aab2832bdaf8f9ca`  
		Last Modified: Thu, 05 Sep 2024 22:07:55 GMT  
		Size: 185.9 KB (185925 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30fa3c69911b3cb9dc7740b2162b11ff94e99551059efb2f156f365cf41cd2ad`  
		Last Modified: Thu, 05 Sep 2024 22:07:56 GMT  
		Size: 408.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae5f18856d9a964a71fc5de310d686fecd16cabafef55031106cf0fb47e6e056`  
		Last Modified: Thu, 05 Sep 2024 22:07:56 GMT  
		Size: 109.3 KB (109253 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elasticsearch:8.15.1` - unknown; unknown

```console
$ docker pull elasticsearch@sha256:ae01b21c80d97030a84c4ebea6f582efd77a1af126bd47071d85a5d416a3eafb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2753643 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f05abc397ab0b26d5b615b0d60e673798547caa0c8dba2dcdbe2c38d81d97597`

```dockerfile
```

-	Layers:
	-	`sha256:2d0e5a06acfe334a37b6114c868c9179011f9aae6ec5887369a5981c2bdd69c4`  
		Last Modified: Thu, 05 Sep 2024 22:07:55 GMT  
		Size: 2.7 MB (2715728 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:07b972a8d926c277cce778145576ecd28de5997533a355b61dba470ee563d005`  
		Last Modified: Thu, 05 Sep 2024 22:07:55 GMT  
		Size: 37.9 KB (37915 bytes)  
		MIME: application/vnd.in-toto+json
