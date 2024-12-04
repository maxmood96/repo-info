<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `elasticsearch`

-	[`elasticsearch:7.17.26`](#elasticsearch71726)
-	[`elasticsearch:8.15.5`](#elasticsearch8155)
-	[`elasticsearch:8.16.1`](#elasticsearch8161)

## `elasticsearch:7.17.26`

```console
$ docker pull elasticsearch@sha256:340f15d5e07488e6bddc60e90690cab1288ffbccb4d20841fa282a7b6501fe51
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `elasticsearch:7.17.26` - linux; amd64

```console
$ docker pull elasticsearch@sha256:b897cf79fc18c3e01e45ed9005e5d110295498f46c1caac56ac81997dd2bebeb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **362.6 MB (362608270 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:50c1e2b365c23a93a7c788b10a5122b762eb21b6a7484b2d2e36a0b5cf675437`
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
# Tue, 03 Dec 2024 13:02:17 GMT
RUN yes no | dpkg-reconfigure dash &&     for iter in 1 2 3 4 5 6 7 8 9 10; do       export DEBIAN_FRONTEND=noninteractive &&       apt-get update &&       apt-get upgrade -y &&       apt-get install -y --no-install-recommends         ca-certificates curl netcat p11-kit unzip zip &&       apt-get clean &&       rm -rf /var/lib/apt/lists/* &&       exit_code=0 && break ||         exit_code=$? && echo "apt-get error: retry $iter in 10s" && sleep 10;     done;     exit $exit_code # buildkit
# Tue, 03 Dec 2024 13:02:17 GMT
RUN groupadd -g 1000 elasticsearch &&     adduser --uid 1000 --gid 1000 --home /usr/share/elasticsearch elasticsearch &&     adduser elasticsearch root &&     chown -R 0:0 /usr/share/elasticsearch # buildkit
# Tue, 03 Dec 2024 13:02:17 GMT
ENV ELASTIC_CONTAINER=true
# Tue, 03 Dec 2024 13:02:17 GMT
WORKDIR /usr/share/elasticsearch
# Tue, 03 Dec 2024 13:02:17 GMT
COPY --chown=0:0 /usr/share/elasticsearch /usr/share/elasticsearch # buildkit
# Tue, 03 Dec 2024 13:02:17 GMT
COPY --chown=0:0 /bin/tini /bin/tini # buildkit
# Tue, 03 Dec 2024 13:02:17 GMT
ENV PATH=/usr/share/elasticsearch/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Dec 2024 13:02:17 GMT
COPY bin/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh # buildkit
# Tue, 03 Dec 2024 13:02:17 GMT
RUN chmod g=u /etc/passwd &&     chmod 0555 /usr/local/bin/docker-entrypoint.sh &&     find / -xdev -perm -4000 -exec chmod ug-s {} + &&     chmod 0775 /usr/share/elasticsearch &&     chown elasticsearch bin config config/jvm.options.d data logs plugins # buildkit
# Tue, 03 Dec 2024 13:02:17 GMT
COPY bin/docker-openjdk /etc/ca-certificates/update.d/docker-openjdk # buildkit
# Tue, 03 Dec 2024 13:02:17 GMT
RUN /etc/ca-certificates/update.d/docker-openjdk # buildkit
# Tue, 03 Dec 2024 13:02:17 GMT
EXPOSE map[9200/tcp:{} 9300/tcp:{}]
# Tue, 03 Dec 2024 13:02:17 GMT
LABEL org.label-schema.build-date=2024-11-28T08:05:55.550508263Z org.label-schema.license=Elastic-License-2.0 org.label-schema.name=Elasticsearch org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/elasticsearch org.label-schema.usage=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.label-schema.vcs-ref=f40328375bfa289242f942fb3d992032ab662e14 org.label-schema.vcs-url=https://github.com/elastic/elasticsearch org.label-schema.vendor=Elastic org.label-schema.version=7.17.26 org.opencontainers.image.created=2024-11-28T08:05:55.550508263Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.opencontainers.image.licenses=Elastic-License-2.0 org.opencontainers.image.revision=f40328375bfa289242f942fb3d992032ab662e14 org.opencontainers.image.source=https://github.com/elastic/elasticsearch org.opencontainers.image.title=Elasticsearch org.opencontainers.image.url=https://www.elastic.co/products/elasticsearch org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=7.17.26
# Tue, 03 Dec 2024 13:02:17 GMT
ENTRYPOINT ["/bin/tini" "--" "/usr/local/bin/docker-entrypoint.sh"]
# Tue, 03 Dec 2024 13:02:17 GMT
CMD ["eswrapper"]
```

-	Layers:
	-	`sha256:d9802f032d6798e2086607424bfe88cb8ec1d6f116e11cd99592dcaf261e9cd2`  
		Last Modified: Fri, 11 Oct 2024 04:41:25 GMT  
		Size: 27.5 MB (27511060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e32e5cb1a01db955df4a39089ffdef3e1f095996654ca7016215539a573ede7a`  
		Last Modified: Tue, 03 Dec 2024 19:32:20 GMT  
		Size: 7.5 MB (7523652 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c1d74473d15b0440ae4742e2f6c7e088b6ea0e70adc3609c7895f613d84cbeb`  
		Last Modified: Tue, 03 Dec 2024 19:32:20 GMT  
		Size: 4.3 KB (4315 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c34956b884255dbcce9e9ddf057cf3a64ead331fc6cb957b26299cfbdc4ca0f`  
		Last Modified: Tue, 03 Dec 2024 19:32:25 GMT  
		Size: 327.2 MB (327249605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb4fe5a338af6d01efa1b1cec801a58a6a4320ef3037a11275c015c4415c2217`  
		Last Modified: Tue, 03 Dec 2024 19:32:20 GMT  
		Size: 9.5 KB (9529 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a911decf74b90be604770beb6cfae93e0912686ddb8a8b344ccfaf9feecf00d`  
		Last Modified: Tue, 03 Dec 2024 19:32:21 GMT  
		Size: 2.0 KB (1977 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb4b640b13ad3605edc9a07a79c9076d42081309d1cf0b2608b76ac8b2d212af`  
		Last Modified: Tue, 03 Dec 2024 19:32:21 GMT  
		Size: 192.2 KB (192164 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0cac06f9686651f8679459e80142d7ba2fbde11474722c826969ea53d11f171`  
		Last Modified: Tue, 03 Dec 2024 19:32:21 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:600c9b7647bf4db99023b270899d65ba9823a068e671b417977c50e23d5c5a3b`  
		Last Modified: Tue, 03 Dec 2024 19:32:21 GMT  
		Size: 115.5 KB (115533 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elasticsearch:7.17.26` - unknown; unknown

```console
$ docker pull elasticsearch@sha256:83e61a43b1305ee3a2ffcde66ee202d211c1570e041a6a3a9bb16b6f86203be9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2593109 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f85203a5ec21973f868b5fa2995023400198631bd490f7fcbb6ea229e5648107`

```dockerfile
```

-	Layers:
	-	`sha256:708f7fce7688f9c1778847c5e4669f5b0a51c2bfdde308bd202f39aaeaad5bcb`  
		Last Modified: Tue, 03 Dec 2024 19:32:20 GMT  
		Size: 2.6 MB (2555221 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3084bc3d9d485970fd093974f473591b678d51b7d327c79f047c435f1ef3f901`  
		Last Modified: Tue, 03 Dec 2024 19:32:20 GMT  
		Size: 37.9 KB (37888 bytes)  
		MIME: application/vnd.in-toto+json

### `elasticsearch:7.17.26` - linux; arm64 variant v8

```console
$ docker pull elasticsearch@sha256:6658726d47270e17c060222ebf54fdf2c4444b4759947d1945ab9f2a4974a559
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **358.6 MB (358551326 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a999bbbb3b452ae6c9a9f399ffb618cac0623f4cda7ffd4e82d15a0172e4cca6`
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
# Tue, 03 Dec 2024 13:02:17 GMT
RUN yes no | dpkg-reconfigure dash &&     for iter in 1 2 3 4 5 6 7 8 9 10; do       export DEBIAN_FRONTEND=noninteractive &&       apt-get update &&       apt-get upgrade -y &&       apt-get install -y --no-install-recommends         ca-certificates curl netcat p11-kit unzip zip &&       apt-get clean &&       rm -rf /var/lib/apt/lists/* &&       exit_code=0 && break ||         exit_code=$? && echo "apt-get error: retry $iter in 10s" && sleep 10;     done;     exit $exit_code # buildkit
# Tue, 03 Dec 2024 13:02:17 GMT
RUN groupadd -g 1000 elasticsearch &&     adduser --uid 1000 --gid 1000 --home /usr/share/elasticsearch elasticsearch &&     adduser elasticsearch root &&     chown -R 0:0 /usr/share/elasticsearch # buildkit
# Tue, 03 Dec 2024 13:02:17 GMT
ENV ELASTIC_CONTAINER=true
# Tue, 03 Dec 2024 13:02:17 GMT
WORKDIR /usr/share/elasticsearch
# Tue, 03 Dec 2024 13:02:17 GMT
COPY --chown=0:0 /usr/share/elasticsearch /usr/share/elasticsearch # buildkit
# Tue, 03 Dec 2024 13:02:17 GMT
COPY --chown=0:0 /bin/tini /bin/tini # buildkit
# Tue, 03 Dec 2024 13:02:17 GMT
ENV PATH=/usr/share/elasticsearch/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Dec 2024 13:02:17 GMT
COPY bin/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh # buildkit
# Tue, 03 Dec 2024 13:02:17 GMT
RUN chmod g=u /etc/passwd &&     chmod 0555 /usr/local/bin/docker-entrypoint.sh &&     find / -xdev -perm -4000 -exec chmod ug-s {} + &&     chmod 0775 /usr/share/elasticsearch &&     chown elasticsearch bin config config/jvm.options.d data logs plugins # buildkit
# Tue, 03 Dec 2024 13:02:17 GMT
COPY bin/docker-openjdk /etc/ca-certificates/update.d/docker-openjdk # buildkit
# Tue, 03 Dec 2024 13:02:17 GMT
RUN /etc/ca-certificates/update.d/docker-openjdk # buildkit
# Tue, 03 Dec 2024 13:02:17 GMT
EXPOSE map[9200/tcp:{} 9300/tcp:{}]
# Tue, 03 Dec 2024 13:02:17 GMT
LABEL org.label-schema.build-date=2024-11-28T08:05:55.550508263Z org.label-schema.license=Elastic-License-2.0 org.label-schema.name=Elasticsearch org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/elasticsearch org.label-schema.usage=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.label-schema.vcs-ref=f40328375bfa289242f942fb3d992032ab662e14 org.label-schema.vcs-url=https://github.com/elastic/elasticsearch org.label-schema.vendor=Elastic org.label-schema.version=7.17.26 org.opencontainers.image.created=2024-11-28T08:05:55.550508263Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.opencontainers.image.licenses=Elastic-License-2.0 org.opencontainers.image.revision=f40328375bfa289242f942fb3d992032ab662e14 org.opencontainers.image.source=https://github.com/elastic/elasticsearch org.opencontainers.image.title=Elasticsearch org.opencontainers.image.url=https://www.elastic.co/products/elasticsearch org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=7.17.26
# Tue, 03 Dec 2024 13:02:17 GMT
ENTRYPOINT ["/bin/tini" "--" "/usr/local/bin/docker-entrypoint.sh"]
# Tue, 03 Dec 2024 13:02:17 GMT
CMD ["eswrapper"]
```

-	Layers:
	-	`sha256:1b9f3c55f9d4aa5c52eb67a4cb7d0f4726ab85a413b50e3e3fe788befce3d297`  
		Last Modified: Fri, 11 Oct 2024 04:41:30 GMT  
		Size: 26.0 MB (25973828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8e2b1282221e026317aebd1e5da35128510fbfafd12f28459efca613e5ead6f`  
		Last Modified: Wed, 04 Dec 2024 01:39:57 GMT  
		Size: 7.3 MB (7347247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b537164255cea8423914f208008cd80cd8928c2521ba5b2a7a3eb954444ef30`  
		Last Modified: Wed, 04 Dec 2024 01:39:56 GMT  
		Size: 4.3 KB (4320 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b38a89b7f62642edd69689f2d24f361ace925d0653d9f17ec58717e374643078`  
		Last Modified: Wed, 04 Dec 2024 01:40:03 GMT  
		Size: 324.9 MB (324912710 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bfff5537ce081ee128452d946b8dca868ab0339d64bea382b1212078d3fddd7`  
		Last Modified: Wed, 04 Dec 2024 01:39:56 GMT  
		Size: 9.1 KB (9095 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0d52aff4804999f67e8a1065264f39282f7277db415e7baf4dea19615867759`  
		Last Modified: Wed, 04 Dec 2024 01:39:57 GMT  
		Size: 2.0 KB (1976 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:812cc15c3dd2f8d69104a729e3dd48e74ea0148381199a811709b37e1b7d47ac`  
		Last Modified: Wed, 04 Dec 2024 01:39:58 GMT  
		Size: 186.2 KB (186181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba90d2a2da3a0a79d7ce43d4703c797988d4a13051225bbeede3943f19771dc7`  
		Last Modified: Wed, 04 Dec 2024 01:39:58 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03bf5b4808cefb71809db9ac4b11505e33f6730f934addd481df49fd59f0a35c`  
		Last Modified: Wed, 04 Dec 2024 01:39:58 GMT  
		Size: 115.5 KB (115534 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elasticsearch:7.17.26` - unknown; unknown

```console
$ docker pull elasticsearch@sha256:2d6cf56e86b915f160a2cc130b53f52f96340f7b30b052d9c69e8d34a73bcf98
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2592280 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:26f3b402f028c8277edf3bbbcc051ea8ee98f51e2d87d38b0dfb62ed4432ff3a`

```dockerfile
```

-	Layers:
	-	`sha256:8f4b9767d87061fd505e0cfb7f8ce4db31aeb526acc37b69210db2889e612f66`  
		Last Modified: Wed, 04 Dec 2024 01:39:57 GMT  
		Size: 2.6 MB (2554190 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bf3935d68fec44311f0274ae38aeffbcc9307aabd41d3750b7ce609f215c9928`  
		Last Modified: Wed, 04 Dec 2024 01:39:56 GMT  
		Size: 38.1 KB (38090 bytes)  
		MIME: application/vnd.in-toto+json

## `elasticsearch:8.15.5`

```console
$ docker pull elasticsearch@sha256:82d39a05c027480938d5d405d7ddd933f221effcd1d8a33356f0dd0212640df9
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `elasticsearch:8.15.5` - linux; amd64

```console
$ docker pull elasticsearch@sha256:c7dd133ad77ec2a6ceb03a0daaa9c8556626a3e4f245daed0b62c7ecb4be3df6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **651.1 MB (651068006 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e983a5cfa41874a2c248b3a50dbdf98449b066c5e665987fd6b32b8126bf47d9`
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
# Tue, 26 Nov 2024 10:47:54 GMT
RUN yes no | dpkg-reconfigure dash &&     for iter in 1 2 3 4 5 6 7 8 9 10; do       export DEBIAN_FRONTEND=noninteractive &&       apt-get update &&       apt-get upgrade -y &&       apt-get install -y --no-install-recommends         ca-certificates curl netcat p11-kit unzip zip  &&       apt-get clean &&       rm -rf /var/lib/apt/lists/* &&       exit_code=0 && break ||         exit_code=$? && echo "apt-get error: retry $iter in 10s" && sleep 10;     done;     exit $exit_code # buildkit
# Tue, 26 Nov 2024 10:47:54 GMT
RUN groupadd -g 1000 elasticsearch &&     adduser --uid 1000 --gid 1000 --home /usr/share/elasticsearch elasticsearch &&     adduser elasticsearch root &&     chown -R 0:0 /usr/share/elasticsearch # buildkit
# Tue, 26 Nov 2024 10:47:54 GMT
ENV ELASTIC_CONTAINER=true
# Tue, 26 Nov 2024 10:47:54 GMT
WORKDIR /usr/share/elasticsearch
# Tue, 26 Nov 2024 10:47:54 GMT
COPY --chown=0:0 /usr/share/elasticsearch /usr/share/elasticsearch # buildkit
# Tue, 26 Nov 2024 10:47:54 GMT
COPY --chown=0:0 /bin/tini /bin/tini # buildkit
# Tue, 26 Nov 2024 10:47:54 GMT
ENV PATH=/usr/share/elasticsearch/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 26 Nov 2024 10:47:54 GMT
COPY bin/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh # buildkit
# Tue, 26 Nov 2024 10:47:54 GMT
RUN chmod g=u /etc/passwd &&     chmod 0555 /usr/local/bin/docker-entrypoint.sh &&     find / -xdev -perm -4000 -exec chmod ug-s {} + &&     chmod 0775 /usr/share/elasticsearch &&     chown elasticsearch bin config config/jvm.options.d data logs plugins # buildkit
# Tue, 26 Nov 2024 10:47:54 GMT
COPY bin/docker-openjdk /etc/ca-certificates/update.d/docker-openjdk # buildkit
# Tue, 26 Nov 2024 10:47:54 GMT
RUN /etc/ca-certificates/update.d/docker-openjdk # buildkit
# Tue, 26 Nov 2024 10:47:54 GMT
EXPOSE map[9200/tcp:{} 9300/tcp:{}]
# Tue, 26 Nov 2024 10:47:54 GMT
LABEL org.label-schema.build-date=2024-11-21T22:06:13.985834967Z org.label-schema.license=Elastic-License-2.0 org.label-schema.name=Elasticsearch org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/elasticsearch org.label-schema.usage=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.label-schema.vcs-ref=b10896bcfe167cce44a84ba2771d101fb596d40d org.label-schema.vcs-url=https://github.com/elastic/elasticsearch org.label-schema.vendor=Elastic org.label-schema.version=8.15.5 org.opencontainers.image.created=2024-11-21T22:06:13.985834967Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.opencontainers.image.licenses=Elastic-License-2.0 org.opencontainers.image.revision=b10896bcfe167cce44a84ba2771d101fb596d40d org.opencontainers.image.source=https://github.com/elastic/elasticsearch org.opencontainers.image.title=Elasticsearch org.opencontainers.image.url=https://www.elastic.co/products/elasticsearch org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=8.15.5
# Tue, 26 Nov 2024 10:47:54 GMT
ENTRYPOINT ["/bin/tini" "--" "/usr/local/bin/docker-entrypoint.sh"]
# Tue, 26 Nov 2024 10:47:54 GMT
CMD ["eswrapper"]
# Tue, 26 Nov 2024 10:47:54 GMT
USER 1000:0
```

-	Layers:
	-	`sha256:d9802f032d6798e2086607424bfe88cb8ec1d6f116e11cd99592dcaf261e9cd2`  
		Last Modified: Fri, 11 Oct 2024 04:41:25 GMT  
		Size: 27.5 MB (27511060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17e9ebd97e160eb4ce1e1ae6b499f9a23847d73bf8e939e9d49db8c3f152543f`  
		Last Modified: Tue, 26 Nov 2024 18:27:17 GMT  
		Size: 7.5 MB (7523702 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7de1bd8f314146b8d61ebc77b9d96d5847ae8ffe47f00bf1b365250369111787`  
		Last Modified: Tue, 26 Nov 2024 18:27:17 GMT  
		Size: 4.3 KB (4317 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81b6d6fb462c845d40fe4bf5da328c37cf7481f768157705a029199e7a1f20d8`  
		Last Modified: Tue, 26 Nov 2024 18:27:25 GMT  
		Size: 615.7 MB (615709821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff62ec68f75a4abbc9ac5a9b50f78dd02eeb337e73332348519a7221fef91ed3`  
		Last Modified: Tue, 26 Nov 2024 18:27:17 GMT  
		Size: 9.5 KB (9523 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35c0e24c5da73d95c4adabbad02355182ccd146391907a48e21fd5fcf80a0582`  
		Last Modified: Tue, 26 Nov 2024 18:27:18 GMT  
		Size: 1.7 KB (1719 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b7e76321b94ba543b31a032524a201b8daef69416391cacec8cd8a599031b94`  
		Last Modified: Tue, 26 Nov 2024 18:27:18 GMT  
		Size: 191.9 KB (191900 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a014a471a9ee7cb8aab4075e3676dbfe772c2468c93541a3e28b2e615b028a7e`  
		Last Modified: Tue, 26 Nov 2024 18:27:18 GMT  
		Size: 406.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e040db56d40fa9c7caa905995fef4f8d023ca3c903e5104cbd8a09c483845889`  
		Last Modified: Tue, 26 Nov 2024 18:27:19 GMT  
		Size: 115.5 KB (115526 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elasticsearch:8.15.5` - unknown; unknown

```console
$ docker pull elasticsearch@sha256:5e9f9f12d35a34aa50ee434f5d40510ff4861f23d0136650d94c44823b60a702
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2980507 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:61fd65a763bde738696a996fd48c4fd6d7e5bcada69490b64a66772df1fe50e5`

```dockerfile
```

-	Layers:
	-	`sha256:c5e9a25ee347f755ad92b22c3734859abe4e5e2ce827b0940f03a16aad9cbe95`  
		Last Modified: Tue, 26 Nov 2024 18:27:17 GMT  
		Size: 2.9 MB (2942603 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:478de23964428271c6cec2d24ae2f96f1f2ae3a7d8141f0d1029742d1e08a022`  
		Last Modified: Tue, 26 Nov 2024 18:27:17 GMT  
		Size: 37.9 KB (37904 bytes)  
		MIME: application/vnd.in-toto+json

### `elasticsearch:8.15.5` - linux; arm64 variant v8

```console
$ docker pull elasticsearch@sha256:90185845d8ccb9810ca11aeee110891bfceba201743e81c1037bc1c08fd213ea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **494.6 MB (494571156 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9d4ce1c00571537453baa36c31ed176d2ed6663b0d6b5e49d05e6cd311796892`
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
# Tue, 26 Nov 2024 10:47:54 GMT
RUN yes no | dpkg-reconfigure dash &&     for iter in 1 2 3 4 5 6 7 8 9 10; do       export DEBIAN_FRONTEND=noninteractive &&       apt-get update &&       apt-get upgrade -y &&       apt-get install -y --no-install-recommends         ca-certificates curl netcat p11-kit unzip zip  &&       apt-get clean &&       rm -rf /var/lib/apt/lists/* &&       exit_code=0 && break ||         exit_code=$? && echo "apt-get error: retry $iter in 10s" && sleep 10;     done;     exit $exit_code # buildkit
# Tue, 26 Nov 2024 10:47:54 GMT
RUN groupadd -g 1000 elasticsearch &&     adduser --uid 1000 --gid 1000 --home /usr/share/elasticsearch elasticsearch &&     adduser elasticsearch root &&     chown -R 0:0 /usr/share/elasticsearch # buildkit
# Tue, 26 Nov 2024 10:47:54 GMT
ENV ELASTIC_CONTAINER=true
# Tue, 26 Nov 2024 10:47:54 GMT
WORKDIR /usr/share/elasticsearch
# Tue, 26 Nov 2024 10:47:54 GMT
COPY --chown=0:0 /usr/share/elasticsearch /usr/share/elasticsearch # buildkit
# Tue, 26 Nov 2024 10:47:54 GMT
COPY --chown=0:0 /bin/tini /bin/tini # buildkit
# Tue, 26 Nov 2024 10:47:54 GMT
ENV PATH=/usr/share/elasticsearch/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 26 Nov 2024 10:47:54 GMT
COPY bin/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh # buildkit
# Tue, 26 Nov 2024 10:47:54 GMT
RUN chmod g=u /etc/passwd &&     chmod 0555 /usr/local/bin/docker-entrypoint.sh &&     find / -xdev -perm -4000 -exec chmod ug-s {} + &&     chmod 0775 /usr/share/elasticsearch &&     chown elasticsearch bin config config/jvm.options.d data logs plugins # buildkit
# Tue, 26 Nov 2024 10:47:54 GMT
COPY bin/docker-openjdk /etc/ca-certificates/update.d/docker-openjdk # buildkit
# Tue, 26 Nov 2024 10:47:54 GMT
RUN /etc/ca-certificates/update.d/docker-openjdk # buildkit
# Tue, 26 Nov 2024 10:47:54 GMT
EXPOSE map[9200/tcp:{} 9300/tcp:{}]
# Tue, 26 Nov 2024 10:47:54 GMT
LABEL org.label-schema.build-date=2024-11-21T22:06:13.985834967Z org.label-schema.license=Elastic-License-2.0 org.label-schema.name=Elasticsearch org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/elasticsearch org.label-schema.usage=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.label-schema.vcs-ref=b10896bcfe167cce44a84ba2771d101fb596d40d org.label-schema.vcs-url=https://github.com/elastic/elasticsearch org.label-schema.vendor=Elastic org.label-schema.version=8.15.5 org.opencontainers.image.created=2024-11-21T22:06:13.985834967Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.opencontainers.image.licenses=Elastic-License-2.0 org.opencontainers.image.revision=b10896bcfe167cce44a84ba2771d101fb596d40d org.opencontainers.image.source=https://github.com/elastic/elasticsearch org.opencontainers.image.title=Elasticsearch org.opencontainers.image.url=https://www.elastic.co/products/elasticsearch org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=8.15.5
# Tue, 26 Nov 2024 10:47:54 GMT
ENTRYPOINT ["/bin/tini" "--" "/usr/local/bin/docker-entrypoint.sh"]
# Tue, 26 Nov 2024 10:47:54 GMT
CMD ["eswrapper"]
# Tue, 26 Nov 2024 10:47:54 GMT
USER 1000:0
```

-	Layers:
	-	`sha256:1b9f3c55f9d4aa5c52eb67a4cb7d0f4726ab85a413b50e3e3fe788befce3d297`  
		Last Modified: Fri, 11 Oct 2024 04:41:30 GMT  
		Size: 26.0 MB (25973828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc895cb5cb5d3a3b7efd1d4f6dd7593c12321fdd7383704697e5b0213f17500f`  
		Last Modified: Mon, 18 Nov 2024 23:42:17 GMT  
		Size: 7.3 MB (7347302 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c0fd9ad867422b2a6f093d60c1244d5e391ff43a794fcead8d76939b9621c2b`  
		Last Modified: Mon, 18 Nov 2024 23:42:17 GMT  
		Size: 4.3 KB (4323 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e27e0a18ea97478d6e587e29fb7c78dbc38a803df994cf3e40e7cd5f5337513e`  
		Last Modified: Tue, 26 Nov 2024 18:27:30 GMT  
		Size: 460.9 MB (460932961 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3e8b0295b66bd4377e566365cd4cccae2f01fe242146b2689e46248a7019446`  
		Last Modified: Tue, 26 Nov 2024 18:27:19 GMT  
		Size: 9.1 KB (9105 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa7b9aebe61c0e9a2a65cad568d558c8aaddf1bdac36ccc18949d6a4e0501268`  
		Last Modified: Tue, 26 Nov 2024 18:27:19 GMT  
		Size: 1.7 KB (1726 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9aec644b5f803bbcc2363566a14fca3c8fdeafdcb92c1939e2df10c606d9e0b8`  
		Last Modified: Tue, 26 Nov 2024 18:27:19 GMT  
		Size: 185.9 KB (185932 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc677c48115ee2c98ea5bbaf7f298835d26762fb37751573ba1024b2d2310395`  
		Last Modified: Tue, 26 Nov 2024 18:27:20 GMT  
		Size: 408.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c67805f190df50f59464637a503648ea576025c97a671a6e291cf228e1cc550`  
		Last Modified: Tue, 26 Nov 2024 18:27:20 GMT  
		Size: 115.5 KB (115539 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elasticsearch:8.15.5` - unknown; unknown

```console
$ docker pull elasticsearch@sha256:510ee99bb6b79ad2933523626725c896e05206e929f7e02e86869dfff050b154
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2979679 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f85c84c91bb2b60b3266bd20927b18512e2ea3fc3d73664daae3a6b2de2466e6`

```dockerfile
```

-	Layers:
	-	`sha256:12ed4c4366f33da22956372ac9e4ebbfd7058d9d71bec62469d1a3e89ccc6c8d`  
		Last Modified: Tue, 26 Nov 2024 18:27:20 GMT  
		Size: 2.9 MB (2941572 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:886c2fcd5499eff2aaf0c4e2f8ecd8c1d92b72bb39398dfbac59cb830f1b99fa`  
		Last Modified: Tue, 26 Nov 2024 18:27:19 GMT  
		Size: 38.1 KB (38107 bytes)  
		MIME: application/vnd.in-toto+json

## `elasticsearch:8.16.1`

```console
$ docker pull elasticsearch@sha256:e5ee5f8dacbf18fa3ab59a098cc7d4d69f73e61637eb45f1c029e74b1cb200a1
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `elasticsearch:8.16.1` - linux; amd64

```console
$ docker pull elasticsearch@sha256:d6878475f25bfea020573cf0dd94aab8e80688b0c55cdc97c40264e72026d301
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **676.4 MB (676423233 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d3bd8c11e2e7ead52c0200d6d7f2007874ab776e7fa62b643b97574f7ba81caf`
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
# Thu, 21 Nov 2024 14:43:56 GMT
RUN yes no | dpkg-reconfigure dash &&     for iter in 1 2 3 4 5 6 7 8 9 10; do       export DEBIAN_FRONTEND=noninteractive &&       apt-get update &&       apt-get upgrade -y &&       apt-get install -y --no-install-recommends         ca-certificates curl netcat p11-kit unzip zip  &&       apt-get clean &&       rm -rf /var/lib/apt/lists/* &&       exit_code=0 && break ||         exit_code=$? && echo "apt-get error: retry $iter in 10s" && sleep 10;     done;     exit $exit_code # buildkit
# Thu, 21 Nov 2024 14:43:56 GMT
RUN groupadd -g 1000 elasticsearch &&     adduser --uid 1000 --gid 1000 --home /usr/share/elasticsearch elasticsearch &&     adduser elasticsearch root &&     chown -R 0:0 /usr/share/elasticsearch # buildkit
# Thu, 21 Nov 2024 14:43:56 GMT
ENV ELASTIC_CONTAINER=true
# Thu, 21 Nov 2024 14:43:56 GMT
WORKDIR /usr/share/elasticsearch
# Thu, 21 Nov 2024 14:43:56 GMT
COPY --chown=0:0 /usr/share/elasticsearch /usr/share/elasticsearch # buildkit
# Thu, 21 Nov 2024 14:43:56 GMT
COPY --chown=0:0 /bin/tini /bin/tini # buildkit
# Thu, 21 Nov 2024 14:43:56 GMT
ENV PATH=/usr/share/elasticsearch/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 21 Nov 2024 14:43:56 GMT
ENV SHELL=/bin/bash
# Thu, 21 Nov 2024 14:43:56 GMT
COPY bin/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh # buildkit
# Thu, 21 Nov 2024 14:43:56 GMT
RUN chmod g=u /etc/passwd &&     chmod 0555 /usr/local/bin/docker-entrypoint.sh &&     find / -xdev -perm -4000 -exec chmod ug-s {} + &&     chmod 0775 /usr/share/elasticsearch &&     chown elasticsearch bin config config/jvm.options.d data logs plugins # buildkit
# Thu, 21 Nov 2024 14:43:56 GMT
COPY bin/docker-openjdk /etc/ca-certificates/update.d/docker-openjdk # buildkit
# Thu, 21 Nov 2024 14:43:56 GMT
RUN /etc/ca-certificates/update.d/docker-openjdk # buildkit
# Thu, 21 Nov 2024 14:43:56 GMT
EXPOSE map[9200/tcp:{} 9300/tcp:{}]
# Thu, 21 Nov 2024 14:43:56 GMT
LABEL org.label-schema.build-date=2024-11-19T16:00:31.793213192Z org.label-schema.license=Elastic-License-2.0 org.label-schema.name=Elasticsearch org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/elasticsearch org.label-schema.usage=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.label-schema.vcs-ref=ffe992aa682c1968b5df375b5095b3a21f122bf3 org.label-schema.vcs-url=https://github.com/elastic/elasticsearch org.label-schema.vendor=Elastic org.label-schema.version=8.16.1 org.opencontainers.image.created=2024-11-19T16:00:31.793213192Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.opencontainers.image.licenses=Elastic-License-2.0 org.opencontainers.image.revision=ffe992aa682c1968b5df375b5095b3a21f122bf3 org.opencontainers.image.source=https://github.com/elastic/elasticsearch org.opencontainers.image.title=Elasticsearch org.opencontainers.image.url=https://www.elastic.co/products/elasticsearch org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=8.16.1
# Thu, 21 Nov 2024 14:43:56 GMT
ENTRYPOINT ["/bin/tini" "--" "/usr/local/bin/docker-entrypoint.sh"]
# Thu, 21 Nov 2024 14:43:56 GMT
CMD ["eswrapper"]
# Thu, 21 Nov 2024 14:43:56 GMT
USER 1000:0
```

-	Layers:
	-	`sha256:d9802f032d6798e2086607424bfe88cb8ec1d6f116e11cd99592dcaf261e9cd2`  
		Last Modified: Fri, 11 Oct 2024 04:41:25 GMT  
		Size: 27.5 MB (27511060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db5284e56853e59c3cd65ac4e5b6d29b741218254ce00ecabadc6a5eb8d8f6d3`  
		Last Modified: Fri, 22 Nov 2024 22:29:28 GMT  
		Size: 7.5 MB (7523664 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a83fbdc57cf00c7f01c43f754f830df5b73f1a77366102076ea8a9284198015`  
		Last Modified: Fri, 22 Nov 2024 22:29:27 GMT  
		Size: 4.3 KB (4315 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d795c858d6ef5fb843aadf47e0318946eeb41a0a397a1d794d3ae0a93d923760`  
		Last Modified: Fri, 22 Nov 2024 22:29:42 GMT  
		Size: 641.1 MB (641065067 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a7794733e5c4a80ba044fd99afc2d62f52a5dae1ebe0f7fe57e96484d3ca076`  
		Last Modified: Fri, 22 Nov 2024 22:29:27 GMT  
		Size: 9.5 KB (9526 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28d6e0f319b04d0a3318a454bf25afcd76944c4749741e4476fb69a2d3040a19`  
		Last Modified: Fri, 22 Nov 2024 22:29:28 GMT  
		Size: 1.7 KB (1722 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b7c37b51a32bf0b8e165d91d854b1f85b5399bcbaa75fd0cf9c98aaf4721b92`  
		Last Modified: Fri, 22 Nov 2024 22:29:28 GMT  
		Size: 191.9 KB (191906 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:645b8ddcf26d3c0d93e43847141c3636ec72a57b66d6252a00f85f7e86b51d09`  
		Last Modified: Fri, 22 Nov 2024 22:29:29 GMT  
		Size: 407.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2575b34d7a7f0ec4b501f9c799c476149509608887cfc755210de7dca534bf8`  
		Last Modified: Fri, 22 Nov 2024 22:29:29 GMT  
		Size: 115.5 KB (115534 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elasticsearch:8.16.1` - unknown; unknown

```console
$ docker pull elasticsearch@sha256:ea02471241e54ba89702f0406a62e87c831b5d5ab427a7ef0eae1f7fb0ba92b5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (3048298 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c820c2b026c460a9050d6393541cadcd24f6dfc1640f7b65a0592c9bb2c3701`

```dockerfile
```

-	Layers:
	-	`sha256:3d25a57a6bbe13e63b553893d2bf891eb8a291e8eecd0333f23d3633a93ec981`  
		Last Modified: Fri, 22 Nov 2024 22:29:28 GMT  
		Size: 3.0 MB (3010092 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6a3535b4f150516e9e3eac975145056a6eb7394412250343d60805bbab67f085`  
		Last Modified: Fri, 22 Nov 2024 22:29:27 GMT  
		Size: 38.2 KB (38206 bytes)  
		MIME: application/vnd.in-toto+json

### `elasticsearch:8.16.1` - linux; arm64 variant v8

```console
$ docker pull elasticsearch@sha256:c5ea110d0a644fbfaaf44ab1d16612e510b2f977afc333aa261d981a8af12784
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **519.8 MB (519769532 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b93690647f924d1bd03be51543f091f0ed5974e8fcc88d0a395790f18cf15949`
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
# Thu, 21 Nov 2024 14:43:56 GMT
RUN yes no | dpkg-reconfigure dash &&     for iter in 1 2 3 4 5 6 7 8 9 10; do       export DEBIAN_FRONTEND=noninteractive &&       apt-get update &&       apt-get upgrade -y &&       apt-get install -y --no-install-recommends         ca-certificates curl netcat p11-kit unzip zip  &&       apt-get clean &&       rm -rf /var/lib/apt/lists/* &&       exit_code=0 && break ||         exit_code=$? && echo "apt-get error: retry $iter in 10s" && sleep 10;     done;     exit $exit_code # buildkit
# Thu, 21 Nov 2024 14:43:56 GMT
RUN groupadd -g 1000 elasticsearch &&     adduser --uid 1000 --gid 1000 --home /usr/share/elasticsearch elasticsearch &&     adduser elasticsearch root &&     chown -R 0:0 /usr/share/elasticsearch # buildkit
# Thu, 21 Nov 2024 14:43:56 GMT
ENV ELASTIC_CONTAINER=true
# Thu, 21 Nov 2024 14:43:56 GMT
WORKDIR /usr/share/elasticsearch
# Thu, 21 Nov 2024 14:43:56 GMT
COPY --chown=0:0 /usr/share/elasticsearch /usr/share/elasticsearch # buildkit
# Thu, 21 Nov 2024 14:43:56 GMT
COPY --chown=0:0 /bin/tini /bin/tini # buildkit
# Thu, 21 Nov 2024 14:43:56 GMT
ENV PATH=/usr/share/elasticsearch/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 21 Nov 2024 14:43:56 GMT
ENV SHELL=/bin/bash
# Thu, 21 Nov 2024 14:43:56 GMT
COPY bin/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh # buildkit
# Thu, 21 Nov 2024 14:43:56 GMT
RUN chmod g=u /etc/passwd &&     chmod 0555 /usr/local/bin/docker-entrypoint.sh &&     find / -xdev -perm -4000 -exec chmod ug-s {} + &&     chmod 0775 /usr/share/elasticsearch &&     chown elasticsearch bin config config/jvm.options.d data logs plugins # buildkit
# Thu, 21 Nov 2024 14:43:56 GMT
COPY bin/docker-openjdk /etc/ca-certificates/update.d/docker-openjdk # buildkit
# Thu, 21 Nov 2024 14:43:56 GMT
RUN /etc/ca-certificates/update.d/docker-openjdk # buildkit
# Thu, 21 Nov 2024 14:43:56 GMT
EXPOSE map[9200/tcp:{} 9300/tcp:{}]
# Thu, 21 Nov 2024 14:43:56 GMT
LABEL org.label-schema.build-date=2024-11-19T16:00:31.793213192Z org.label-schema.license=Elastic-License-2.0 org.label-schema.name=Elasticsearch org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/elasticsearch org.label-schema.usage=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.label-schema.vcs-ref=ffe992aa682c1968b5df375b5095b3a21f122bf3 org.label-schema.vcs-url=https://github.com/elastic/elasticsearch org.label-schema.vendor=Elastic org.label-schema.version=8.16.1 org.opencontainers.image.created=2024-11-19T16:00:31.793213192Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.opencontainers.image.licenses=Elastic-License-2.0 org.opencontainers.image.revision=ffe992aa682c1968b5df375b5095b3a21f122bf3 org.opencontainers.image.source=https://github.com/elastic/elasticsearch org.opencontainers.image.title=Elasticsearch org.opencontainers.image.url=https://www.elastic.co/products/elasticsearch org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=8.16.1
# Thu, 21 Nov 2024 14:43:56 GMT
ENTRYPOINT ["/bin/tini" "--" "/usr/local/bin/docker-entrypoint.sh"]
# Thu, 21 Nov 2024 14:43:56 GMT
CMD ["eswrapper"]
# Thu, 21 Nov 2024 14:43:56 GMT
USER 1000:0
```

-	Layers:
	-	`sha256:1b9f3c55f9d4aa5c52eb67a4cb7d0f4726ab85a413b50e3e3fe788befce3d297`  
		Last Modified: Fri, 11 Oct 2024 04:41:30 GMT  
		Size: 26.0 MB (25973828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc895cb5cb5d3a3b7efd1d4f6dd7593c12321fdd7383704697e5b0213f17500f`  
		Last Modified: Mon, 18 Nov 2024 23:42:17 GMT  
		Size: 7.3 MB (7347302 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c0fd9ad867422b2a6f093d60c1244d5e391ff43a794fcead8d76939b9621c2b`  
		Last Modified: Mon, 18 Nov 2024 23:42:17 GMT  
		Size: 4.3 KB (4323 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe8e0ffee7c9e89363344a4ab50b7d78708cae11dabe1981c00b3e003900a968`  
		Last Modified: Fri, 22 Nov 2024 22:32:24 GMT  
		Size: 486.1 MB (486131338 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d733871a0031e03ac68a7da4aae2768e49f71feef31dfea8faf1a2a4a6070387`  
		Last Modified: Fri, 22 Nov 2024 22:32:12 GMT  
		Size: 9.1 KB (9105 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:408ae58363b94c788801a49d22f9bc7ff2a1da18ea26f7a0cad5ef16ebc43254`  
		Last Modified: Fri, 22 Nov 2024 22:32:12 GMT  
		Size: 1.7 KB (1726 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dab6cd2208d6b34cd383cf0abf386d0b11111364b366a9b27b7170c2c4f896b5`  
		Last Modified: Fri, 22 Nov 2024 22:32:12 GMT  
		Size: 185.9 KB (185931 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e41882eb00176e59a60b809b82d542bb6c249ecb1752b41f1f99c5863560bda9`  
		Last Modified: Fri, 22 Nov 2024 22:32:13 GMT  
		Size: 407.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3e2352a9791a655c09b873870a3c4221d3698bdb508c8b3022119193076dfde`  
		Last Modified: Fri, 22 Nov 2024 22:32:13 GMT  
		Size: 115.5 KB (115540 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elasticsearch:8.16.1` - unknown; unknown

```console
$ docker pull elasticsearch@sha256:efbabd1f8b3cc9d0f859f2f2ae80945acef88c380643d8089973445a5b3b6426
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (3047470 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c4b2448ac2c9e7530e5782134c8b5de6833987a232b07c9622d539364f824e5`

```dockerfile
```

-	Layers:
	-	`sha256:8b4dd864061e48de71db7b5e7ecca413a72761d1e4e5d591c603c1bee5124baa`  
		Last Modified: Fri, 22 Nov 2024 22:32:13 GMT  
		Size: 3.0 MB (3009061 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1f2cc87c4980f775b182acff18d977d534f38e4ed9dbd15b2f4b8c75db5131c8`  
		Last Modified: Fri, 22 Nov 2024 22:32:12 GMT  
		Size: 38.4 KB (38409 bytes)  
		MIME: application/vnd.in-toto+json
