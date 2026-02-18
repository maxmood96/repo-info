<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `kibana`

-	[`kibana:8.19.11`](#kibana81911)
-	[`kibana:9.2.5`](#kibana925)
-	[`kibana:9.3.0`](#kibana930)

## `kibana:8.19.11`

```console
$ docker pull kibana@sha256:aa84be26792636760ce181a73e3b92c8670656d0fbe92b5dd3ba84626af862ab
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `kibana:8.19.11` - linux; amd64

```console
$ docker pull kibana@sha256:7aa9cfaf2e7fa909f663277f7549969f71c74965539c3be0fc7db744cf4f8266
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **442.0 MB (441986383 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d7bfae6c5a7cfd21a21ac813004a35072b39292c1d407c10535d748b4e5c19ed`
-	Entrypoint: `["\/bin\/tini","--"]`
-	Default Command: `["\/usr\/local\/bin\/kibana-docker"]`

```dockerfile
# Tue, 10 Feb 2026 16:49:54 GMT
ARG RELEASE
# Tue, 10 Feb 2026 16:49:54 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 10 Feb 2026 16:49:54 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 10 Feb 2026 16:49:54 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 10 Feb 2026 16:49:56 GMT
ADD file:1ae27d2ef4369361104b699712f3897141e394785df5d193d67b44626f57eb87 in / 
# Tue, 10 Feb 2026 16:49:57 GMT
CMD ["/bin/bash"]
# Tue, 17 Feb 2026 20:26:49 GMT
EXPOSE map[5601/tcp:{}]
# Tue, 17 Feb 2026 20:26:49 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&       apt-get update &&       apt-get install -y --no-install-recommends fontconfig fonts-liberation libnss3 curl ca-certificates &&       apt-get clean &&       rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Feb 2026 20:35:18 GMT
COPY --chown=1000:0 /usr/share/kibana /usr/share/kibana # buildkit
# Tue, 17 Feb 2026 20:35:18 GMT
COPY --chown=0:0 /bin/tini /bin/tini # buildkit
# Tue, 17 Feb 2026 20:35:19 GMT
COPY --chown=0:0 /usr/share/fonts/local/NotoSansCJK-Regular.ttc /usr/share/fonts/local/NotoSansCJK-Regular.ttc # buildkit
# Tue, 17 Feb 2026 20:35:19 GMT
RUN fc-cache -v # buildkit
# Tue, 17 Feb 2026 20:35:19 GMT
WORKDIR /usr/share/kibana
# Tue, 17 Feb 2026 20:35:19 GMT
RUN ln -s /usr/share/kibana /opt/kibana # buildkit
# Tue, 17 Feb 2026 20:35:19 GMT
ENV ELASTIC_CONTAINER=true
# Tue, 17 Feb 2026 20:35:19 GMT
ENV PATH=/usr/share/kibana/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Feb 2026 20:35:19 GMT
COPY --chown=1000:0 config/kibana.yml /usr/share/kibana/config/kibana.yml # buildkit
# Tue, 17 Feb 2026 20:35:19 GMT
COPY bin/kibana-docker /usr/local/bin/ # buildkit
# Tue, 17 Feb 2026 20:35:19 GMT
RUN chmod g+ws /usr/share/kibana &&     find /usr/share/kibana -gid 0 -and -not -perm /g+w -exec chmod g+w {} \; # buildkit
# Tue, 17 Feb 2026 20:35:20 GMT
RUN find / -xdev -perm -4000 -exec chmod u-s {} + # buildkit
# Tue, 17 Feb 2026 20:35:20 GMT
RUN userdel -r ubuntu && groupadd --gid 1000 kibana &&     useradd --uid 1000 --gid 1000 -G 0       --home-dir /usr/share/kibana --no-create-home       kibana # buildkit
# Tue, 17 Feb 2026 20:35:20 GMT
LABEL org.label-schema.build-date=2026-01-28T21:14:33.954Z org.label-schema.license=Elastic License org.label-schema.name=Kibana org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/kibana org.label-schema.usage=https://www.elastic.co/guide/en/kibana/reference/index.html org.label-schema.vcs-ref=c14722b56e3d34d5203bd311e91f9ec49227b044 org.label-schema.vcs-url=https://github.com/elastic/kibana org.label-schema.vendor=Elastic org.label-schema.version=8.19.11 org.opencontainers.image.created=2026-01-28T21:14:33.954Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/kibana/reference/index.html org.opencontainers.image.licenses=Elastic License org.opencontainers.image.revision=c14722b56e3d34d5203bd311e91f9ec49227b044 org.opencontainers.image.source=https://github.com/elastic/kibana org.opencontainers.image.title=Kibana org.opencontainers.image.url=https://www.elastic.co/products/kibana org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=8.19.11
# Tue, 17 Feb 2026 20:35:20 GMT
ENTRYPOINT ["/bin/tini" "--"]
# Tue, 17 Feb 2026 20:35:20 GMT
CMD ["/usr/local/bin/kibana-docker"]
# Tue, 17 Feb 2026 20:35:20 GMT
USER 1000
```

-	Layers:
	-	`sha256:01d7766a2e4a62b74e0bebf2cd12c47e675e9221174f6570854203e84ffe68b0`  
		Last Modified: Tue, 10 Feb 2026 17:41:34 GMT  
		Size: 29.7 MB (29727611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ce3cd79ef418edf384e3dd1e1d7707a9bc11a1180d3f830b9e552e4e8cfacc3`  
		Last Modified: Tue, 17 Feb 2026 20:36:14 GMT  
		Size: 9.4 MB (9432668 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b15685c8fa8cc436e9ada3a46fce2ff90200d2e2fd683bd299c8531d93c7c87`  
		Last Modified: Tue, 17 Feb 2026 20:36:21 GMT  
		Size: 386.2 MB (386182408 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:afd3708a8f68d73039064d6214253ee1d02684290172aaf270c8009d7cc15359`  
		Last Modified: Tue, 17 Feb 2026 20:36:13 GMT  
		Size: 9.5 KB (9528 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f0ec6ea63f1f27ef6738e95ea4bb0957199ae66e2ba870099b894e02f4b4a8c`  
		Last Modified: Tue, 17 Feb 2026 20:36:14 GMT  
		Size: 16.5 MB (16460477 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d617de9aa48a7746aabf417eb20f1e111c77545422ace430a1a4dea2c88be4d0`  
		Last Modified: Tue, 17 Feb 2026 20:36:14 GMT  
		Size: 5.2 KB (5235 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e365afe2ef9d148f414216ed4fc70344b51f57b5ceab12c3d844eafb1b2e015`  
		Last Modified: Tue, 17 Feb 2026 20:36:15 GMT  
		Size: 130.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6dd3ba1e70eac0c14e1fe86cb44af8980d60179f9f8c35674761d62c7cbb5ce5`  
		Last Modified: Tue, 17 Feb 2026 20:36:15 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5a0044e6e64794ffd87bd51693fd14d7c3dd3252e9166636da4a46e1826de61`  
		Last Modified: Tue, 17 Feb 2026 20:36:15 GMT  
		Size: 4.8 KB (4817 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10a7cbe38967835c8da13970ce3268ea46ae04d226a59591512ab184f9060bd6`  
		Last Modified: Tue, 17 Feb 2026 20:36:16 GMT  
		Size: 400.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6665bc640f35e73ced6f8a8fb330ed6fa9953d4d5ef9571430290c81d73a339f`  
		Last Modified: Tue, 17 Feb 2026 20:36:16 GMT  
		Size: 161.5 KB (161457 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97f451cf6301adfed19ae3575db51cac2b5804b02c1e02e6738f8b3d5ddce2d7`  
		Last Modified: Tue, 17 Feb 2026 20:36:17 GMT  
		Size: 1.2 KB (1223 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kibana:8.19.11` - unknown; unknown

```console
$ docker pull kibana@sha256:6cb9048a685c4f03850e5d26d7c8cd896616e2ea70e7dd91ce87e64e33cc131a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.0 MB (4962903 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b14c823b8a4d9d714a901b0b4405223ad82e0674706ea719366a589f65cf82b6`

```dockerfile
```

-	Layers:
	-	`sha256:88a632e7a729355ac48d429e4907812ccf2d4e48fbc7da261e69b652beee5308`  
		Last Modified: Tue, 17 Feb 2026 20:36:14 GMT  
		Size: 4.9 MB (4921988 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9e7c19239ed060b9de9e95d990924b2d6349abbbd2697ff1a14b7f4159a48559`  
		Last Modified: Tue, 17 Feb 2026 20:36:13 GMT  
		Size: 40.9 KB (40915 bytes)  
		MIME: application/vnd.in-toto+json

### `kibana:8.19.11` - linux; arm64 variant v8

```console
$ docker pull kibana@sha256:05de80041610395335272fdc631fe456655d225a7215b0081203aabcbe78dab8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **454.9 MB (454865747 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:747f3e64f9fae050321ab0ff62e56f0c9f754f8657dadbb0d73068a20df34687`
-	Entrypoint: `["\/bin\/tini","--"]`
-	Default Command: `["\/usr\/local\/bin\/kibana-docker"]`

```dockerfile
# Tue, 10 Feb 2026 16:52:26 GMT
ARG RELEASE
# Tue, 10 Feb 2026 16:52:26 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 10 Feb 2026 16:52:27 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 10 Feb 2026 16:52:27 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 10 Feb 2026 16:52:29 GMT
ADD file:25d708bf0b30ddee20c0b2764034e065aca922cafd48eb9c662e35ba02ccf1de in / 
# Tue, 10 Feb 2026 16:52:29 GMT
CMD ["/bin/bash"]
# Tue, 17 Feb 2026 20:26:07 GMT
EXPOSE map[5601/tcp:{}]
# Tue, 17 Feb 2026 20:26:07 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&       apt-get update &&       apt-get install -y --no-install-recommends fontconfig fonts-liberation libnss3 curl ca-certificates &&       apt-get clean &&       rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Feb 2026 20:33:23 GMT
COPY --chown=1000:0 /usr/share/kibana /usr/share/kibana # buildkit
# Tue, 17 Feb 2026 20:33:24 GMT
COPY --chown=0:0 /bin/tini /bin/tini # buildkit
# Tue, 17 Feb 2026 20:33:24 GMT
COPY --chown=0:0 /usr/share/fonts/local/NotoSansCJK-Regular.ttc /usr/share/fonts/local/NotoSansCJK-Regular.ttc # buildkit
# Tue, 17 Feb 2026 20:33:24 GMT
RUN fc-cache -v # buildkit
# Tue, 17 Feb 2026 20:33:24 GMT
WORKDIR /usr/share/kibana
# Tue, 17 Feb 2026 20:33:24 GMT
RUN ln -s /usr/share/kibana /opt/kibana # buildkit
# Tue, 17 Feb 2026 20:33:24 GMT
ENV ELASTIC_CONTAINER=true
# Tue, 17 Feb 2026 20:33:24 GMT
ENV PATH=/usr/share/kibana/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Feb 2026 20:33:24 GMT
COPY --chown=1000:0 config/kibana.yml /usr/share/kibana/config/kibana.yml # buildkit
# Tue, 17 Feb 2026 20:33:24 GMT
COPY bin/kibana-docker /usr/local/bin/ # buildkit
# Tue, 17 Feb 2026 20:33:25 GMT
RUN chmod g+ws /usr/share/kibana &&     find /usr/share/kibana -gid 0 -and -not -perm /g+w -exec chmod g+w {} \; # buildkit
# Tue, 17 Feb 2026 20:33:26 GMT
RUN find / -xdev -perm -4000 -exec chmod u-s {} + # buildkit
# Tue, 17 Feb 2026 20:33:26 GMT
RUN userdel -r ubuntu && groupadd --gid 1000 kibana &&     useradd --uid 1000 --gid 1000 -G 0       --home-dir /usr/share/kibana --no-create-home       kibana # buildkit
# Tue, 17 Feb 2026 20:33:26 GMT
LABEL org.label-schema.build-date=2026-01-28T21:14:33.954Z org.label-schema.license=Elastic License org.label-schema.name=Kibana org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/kibana org.label-schema.usage=https://www.elastic.co/guide/en/kibana/reference/index.html org.label-schema.vcs-ref=c14722b56e3d34d5203bd311e91f9ec49227b044 org.label-schema.vcs-url=https://github.com/elastic/kibana org.label-schema.vendor=Elastic org.label-schema.version=8.19.11 org.opencontainers.image.created=2026-01-28T21:14:33.954Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/kibana/reference/index.html org.opencontainers.image.licenses=Elastic License org.opencontainers.image.revision=c14722b56e3d34d5203bd311e91f9ec49227b044 org.opencontainers.image.source=https://github.com/elastic/kibana org.opencontainers.image.title=Kibana org.opencontainers.image.url=https://www.elastic.co/products/kibana org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=8.19.11
# Tue, 17 Feb 2026 20:33:26 GMT
ENTRYPOINT ["/bin/tini" "--"]
# Tue, 17 Feb 2026 20:33:26 GMT
CMD ["/usr/local/bin/kibana-docker"]
# Tue, 17 Feb 2026 20:33:26 GMT
USER 1000
```

-	Layers:
	-	`sha256:66a4bbbfab887561d75f1fdb3c6221c974346f82c9229f5ef99f96b7e6c25704`  
		Last Modified: Tue, 10 Feb 2026 17:41:42 GMT  
		Size: 28.9 MB (28865120 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad30ecd34f63b6d54be11eaa5617cd40d8cd2167089e0cf8ac59004081f6eb26`  
		Last Modified: Tue, 17 Feb 2026 20:34:32 GMT  
		Size: 9.4 MB (9448430 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51503324a3c45c30697b2cf6e5b7c45b674d8df192e7607e8296d52f2a55d9f1`  
		Last Modified: Tue, 17 Feb 2026 20:34:39 GMT  
		Size: 399.9 MB (399912368 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e45bf281ea02cd252ed2ff3368842516b3ad9569ffce784711147fa3c89fb25c`  
		Last Modified: Tue, 17 Feb 2026 20:34:32 GMT  
		Size: 9.1 KB (9100 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e67841edee82b94dfe625ad6fb5d1ab118a6b9e0661fad84451c22af7efde733`  
		Last Modified: Tue, 17 Feb 2026 20:34:33 GMT  
		Size: 16.5 MB (16460480 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64720d1eeafe28d900ea05e585aa016ac4e37da92dcefce69dc239524bb5accd`  
		Last Modified: Tue, 17 Feb 2026 20:34:33 GMT  
		Size: 5.2 KB (5241 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dfd09f0f12cc33383a7212ed4366553fcba98f3e1fb4e792e28cd0086a1dbcc3`  
		Last Modified: Tue, 17 Feb 2026 20:34:34 GMT  
		Size: 131.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05bcbdfec4787be83413039b7cab92122d74c3732e394ff146a22020eb5985b6`  
		Last Modified: Tue, 17 Feb 2026 20:34:34 GMT  
		Size: 399.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:621dacc7aa08155967b78f1e5a5435aaf76cc9439696b1ab3d3595554a069261`  
		Last Modified: Tue, 17 Feb 2026 20:34:34 GMT  
		Size: 4.8 KB (4824 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:327c4fd65a600ea45aad094cdc26a7c8805ce916b435f416e223f99873b67293`  
		Last Modified: Tue, 17 Feb 2026 20:34:35 GMT  
		Size: 402.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6aa84e13bb3804ca86d99d75c2a5049cc546385330a8a43e28fb45074cae0342`  
		Last Modified: Tue, 17 Feb 2026 20:34:35 GMT  
		Size: 158.0 KB (157996 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c3a68426220b3ca38f63c2b8b664f52075dbcfd52bd70d89f80166ee1f4c1aa`  
		Last Modified: Tue, 17 Feb 2026 20:34:35 GMT  
		Size: 1.2 KB (1224 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kibana:8.19.11` - unknown; unknown

```console
$ docker pull kibana@sha256:bc2bfcb7c73674559029194c9fe42ddd4a995df0e75753c2ece01b83539e3044
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.0 MB (4964215 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f3efc557985ccf78a7732dc5ced5d999dab2b7bc575d9129ff694380842cdd6`

```dockerfile
```

-	Layers:
	-	`sha256:ef2862f6b485fd612d17c9acc772fef9632f4df6109c333c31a81b49694d018c`  
		Last Modified: Tue, 17 Feb 2026 20:34:32 GMT  
		Size: 4.9 MB (4923052 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6829bd6d09a634e9d0dba78ded7fa56dcbdbd4b620ba764908870d7b19a1254d`  
		Last Modified: Tue, 17 Feb 2026 20:34:31 GMT  
		Size: 41.2 KB (41163 bytes)  
		MIME: application/vnd.in-toto+json

## `kibana:9.2.5`

```console
$ docker pull kibana@sha256:8a55b87a903dd146cd5d16f63f041a5134359698ead9b90c2528f2264100575e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `kibana:9.2.5` - linux; amd64

```console
$ docker pull kibana@sha256:c12a02f56ddf760090af28f18046fd41aa73625be6f147b683a42bde73db110c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **449.2 MB (449163074 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:45aa446cb57c917f2a790db01d71c1b87370e55c55a87ea724a9e0ac5bd6a2c0`
-	Entrypoint: `["\/bin\/tini","--"]`
-	Default Command: `["\/usr\/local\/bin\/kibana-docker"]`

```dockerfile
# Tue, 17 Feb 2026 16:42:45 GMT
LABEL maintainer="Red Hat, Inc."
# Tue, 17 Feb 2026 16:42:45 GMT
LABEL vendor="Red Hat, Inc."
# Tue, 17 Feb 2026 16:42:45 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Tue, 17 Feb 2026 16:42:45 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.7"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Tue, 17 Feb 2026 16:42:45 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Tue, 17 Feb 2026 16:42:45 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Tue, 17 Feb 2026 16:42:45 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Tue, 17 Feb 2026 16:42:45 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Tue, 17 Feb 2026 16:42:45 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Tue, 17 Feb 2026 16:42:45 GMT
LABEL io.openshift.expose-services=""
# Tue, 17 Feb 2026 16:42:45 GMT
LABEL io.openshift.tags="minimal rhel9"
# Tue, 17 Feb 2026 16:42:45 GMT
ENV container oci
# Tue, 17 Feb 2026 16:42:46 GMT
COPY dir:a84da6f36b88f4eb0d6c411f65b34c1a9d85150d3035dd516db4ece0c2569465 in /      
# Tue, 17 Feb 2026 16:42:46 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Tue, 17 Feb 2026 16:42:46 GMT
CMD ["/bin/bash"]
# Tue, 17 Feb 2026 16:42:46 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /usr/share/buildinfo/content-sets.json      
# Tue, 17 Feb 2026 16:42:46 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /root/buildinfo/content_manifests/content-sets.json      
# Tue, 17 Feb 2026 16:42:46 GMT
COPY file:6326b4becf4dcc53eab9a0e80efe304ada5421165d0586862d969cb5fa826bd8 in /usr/share/buildinfo/labels.json      
# Tue, 17 Feb 2026 16:42:46 GMT
COPY file:6326b4becf4dcc53eab9a0e80efe304ada5421165d0586862d969cb5fa826bd8 in /root/buildinfo/labels.json      
# Tue, 17 Feb 2026 16:42:46 GMT
LABEL "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="0ced2bbee24d5463d4530756a57f8db895246c48" "org.opencontainers.image.revision"="0ced2bbee24d5463d4530756a57f8db895246c48" "build-date"="2026-02-17T16:42:34Z" "org.opencontainers.image.created"="2026-02-17T16:42:34Z" "release"="1771346502"org.opencontainers.image.revision=0ced2bbee24d5463d4530756a57f8db895246c48,org.opencontainers.image.created=2026-02-17T16:42:34Z
# Wed, 18 Feb 2026 19:20:21 GMT
EXPOSE map[5601/tcp:{}]
# Wed, 18 Feb 2026 19:20:21 GMT
RUN microdnf install --setopt=tsflags=nodocs -y       fontconfig liberation-fonts-common freetype shadow-utils nss findutils &&       microdnf clean all # buildkit
# Wed, 18 Feb 2026 19:29:22 GMT
COPY --chown=1000:0 /usr/share/kibana /usr/share/kibana # buildkit
# Wed, 18 Feb 2026 19:29:23 GMT
COPY --chown=0:0 /bin/tini /bin/tini # buildkit
# Wed, 18 Feb 2026 19:29:23 GMT
COPY --chown=0:0 /usr/share/fonts/local/NotoSansCJK-Regular.ttc /usr/share/fonts/local/NotoSansCJK-Regular.ttc # buildkit
# Wed, 18 Feb 2026 19:29:23 GMT
RUN fc-cache -v # buildkit
# Wed, 18 Feb 2026 19:29:23 GMT
WORKDIR /usr/share/kibana
# Wed, 18 Feb 2026 19:29:23 GMT
RUN ln -s /usr/share/kibana /opt/kibana # buildkit
# Wed, 18 Feb 2026 19:29:23 GMT
ENV ELASTIC_CONTAINER=true
# Wed, 18 Feb 2026 19:29:23 GMT
ENV PATH=/usr/share/kibana/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 18 Feb 2026 19:29:23 GMT
COPY --chown=1000:0 config/kibana.yml /usr/share/kibana/config/kibana.yml # buildkit
# Wed, 18 Feb 2026 19:29:23 GMT
COPY bin/kibana-docker /usr/local/bin/ # buildkit
# Wed, 18 Feb 2026 19:29:24 GMT
RUN chmod g+ws /usr/share/kibana &&     find /usr/share/kibana -gid 0 -and -not -perm /g+w -exec chmod g+w {} \; # buildkit
# Wed, 18 Feb 2026 19:29:24 GMT
RUN find / -xdev -perm -4000 -exec chmod u-s {} + # buildkit
# Wed, 18 Feb 2026 19:29:25 GMT
RUN groupadd --gid 1000 kibana &&     useradd --uid 1000 --gid 1000 -G 0       --home-dir /usr/share/kibana --no-create-home       kibana # buildkit
# Wed, 18 Feb 2026 19:29:25 GMT
LABEL org.label-schema.build-date=2026-01-28T23:38:44.165Z org.label-schema.license=Elastic License org.label-schema.name=Kibana org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/kibana org.label-schema.usage=https://www.elastic.co/guide/en/kibana/reference/index.html org.label-schema.vcs-ref=f99524135b3b29ff4011629c9e8511086b1a597a org.label-schema.vcs-url=https://github.com/elastic/kibana org.label-schema.vendor=Elastic org.label-schema.version=9.2.5 org.opencontainers.image.created=2026-01-28T23:38:44.165Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/kibana/reference/index.html org.opencontainers.image.licenses=Elastic License org.opencontainers.image.revision=f99524135b3b29ff4011629c9e8511086b1a597a org.opencontainers.image.source=https://github.com/elastic/kibana org.opencontainers.image.title=Kibana org.opencontainers.image.url=https://www.elastic.co/products/kibana org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=9.2.5
# Wed, 18 Feb 2026 19:29:25 GMT
LABEL name=Kibana maintainer=infra@elastic.co vendor=Elastic version=9.2.5 release=1 summary=Kibana description=Your window into the Elastic Stack.
# Wed, 18 Feb 2026 19:29:25 GMT
RUN mkdir /licenses && ln LICENSE.txt /licenses/LICENSE # buildkit
# Wed, 18 Feb 2026 19:29:25 GMT
ENTRYPOINT ["/bin/tini" "--"]
# Wed, 18 Feb 2026 19:29:25 GMT
CMD ["/usr/local/bin/kibana-docker"]
# Wed, 18 Feb 2026 19:29:25 GMT
USER 1000
```

-	Layers:
	-	`sha256:4638e3415987f378f2d6dd70f9c6a2869dd5ebd09e3510ba45e46bbb6ec1a3dd`  
		Last Modified: Tue, 17 Feb 2026 18:08:54 GMT  
		Size: 40.0 MB (40033596 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f533661f25e4947d13cf73166de63cff7d0659ca6e622dfeb150dc6cc4025cb`  
		Last Modified: Wed, 18 Feb 2026 19:30:19 GMT  
		Size: 19.5 MB (19526347 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98dc1de20a5394da8a376c2c0e7d71ea2106c09a8e69fbfe4cc4977d54f79b4a`  
		Last Modified: Wed, 18 Feb 2026 19:30:26 GMT  
		Size: 373.0 MB (373044749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ea8133c6bf37568497f29572924063242457200c7f7a3611510410d1b6d66a0`  
		Last Modified: Wed, 18 Feb 2026 19:30:18 GMT  
		Size: 9.5 KB (9529 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:378ac1ba0defd0e0b6b0b2b591a020002ee9cc1e97c4a7ef41af78988d1abc71`  
		Last Modified: Wed, 18 Feb 2026 19:30:20 GMT  
		Size: 16.5 MB (16460486 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7682bec2a5959b6e7021f27a7debcf0dc5b83dc188ed4b0282065c337dc9f56`  
		Last Modified: Wed, 18 Feb 2026 19:30:20 GMT  
		Size: 5.2 KB (5221 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ddd537c8022ebc0200c9a13f66d5668aeeb0635322dd0af7673f18ff2af8d9f1`  
		Last Modified: Wed, 18 Feb 2026 19:30:21 GMT  
		Size: 132.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e26a370b16b07eb21f85ecdb8f29fe7adcca21200531dbc4ea465ff8d1db131`  
		Last Modified: Wed, 18 Feb 2026 19:30:21 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:299db2a5cde1ffc21ab6626ba049919c0aced38d830bb5c339bd7213e1454f1e`  
		Last Modified: Wed, 18 Feb 2026 19:30:21 GMT  
		Size: 4.9 KB (4895 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f88409006eefcca5d7004290d7fbef95c6990a519779c17390fd9d8f4539b91b`  
		Last Modified: Wed, 18 Feb 2026 19:30:22 GMT  
		Size: 399.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e444edc8e844419ae9c586c1a65cf3f05d0b994902b81b6594d74bc2f90fa03`  
		Last Modified: Wed, 18 Feb 2026 19:30:22 GMT  
		Size: 74.5 KB (74539 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:356dce00f45567ddc0097cbe93faed559d417a8ef9896aabece798426860250f`  
		Last Modified: Wed, 18 Feb 2026 19:30:22 GMT  
		Size: 1.0 KB (1046 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c808de5bc5a5442881dbd3c5e921f44d50f012923f52d6e2dbc560d67e46bd6`  
		Last Modified: Wed, 18 Feb 2026 19:30:24 GMT  
		Size: 1.7 KB (1708 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kibana:9.2.5` - unknown; unknown

```console
$ docker pull kibana@sha256:73b45da5fd00071724bf566e67f724072e086165db71ed16a6b69d510c5275bd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5790845 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5aabbb920d4181f2ba4725401b16130cc63977d1be6d27d9f9352763e6c7c770`

```dockerfile
```

-	Layers:
	-	`sha256:5efbd2ff561460c47d4806caba576ee88f57476c9a933b5ca97c04f705fa4022`  
		Last Modified: Wed, 18 Feb 2026 19:30:19 GMT  
		Size: 5.7 MB (5747619 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3dff788c4a07c4ab1b90ac65e05dd2534f643bc492613e6e373c202be26e0c75`  
		Last Modified: Wed, 18 Feb 2026 19:30:18 GMT  
		Size: 43.2 KB (43226 bytes)  
		MIME: application/vnd.in-toto+json

### `kibana:9.2.5` - linux; arm64 variant v8

```console
$ docker pull kibana@sha256:7ca33ceeaa3210faca15351694960ddf26404a8ef604958a4e40af51bb103a0e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **461.0 MB (461007607 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:825169b68ac4c875b25a38344bac5da98a455eba9b7f84ec21cc32e212f90ed3`
-	Entrypoint: `["\/bin\/tini","--"]`
-	Default Command: `["\/usr\/local\/bin\/kibana-docker"]`

```dockerfile
# Tue, 17 Feb 2026 16:45:44 GMT
LABEL maintainer="Red Hat, Inc."
# Tue, 17 Feb 2026 16:45:44 GMT
LABEL vendor="Red Hat, Inc."
# Tue, 17 Feb 2026 16:45:44 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Tue, 17 Feb 2026 16:45:44 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.7"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Tue, 17 Feb 2026 16:45:44 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Tue, 17 Feb 2026 16:45:44 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Tue, 17 Feb 2026 16:45:44 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Tue, 17 Feb 2026 16:45:44 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Tue, 17 Feb 2026 16:45:44 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Tue, 17 Feb 2026 16:45:44 GMT
LABEL io.openshift.expose-services=""
# Tue, 17 Feb 2026 16:45:44 GMT
LABEL io.openshift.tags="minimal rhel9"
# Tue, 17 Feb 2026 16:45:44 GMT
ENV container oci
# Tue, 17 Feb 2026 16:45:45 GMT
COPY dir:ac0ab1292a52ccb276077ed994531e1a3deef7d271c3502d95032264a0448d19 in /      
# Tue, 17 Feb 2026 16:45:45 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Tue, 17 Feb 2026 16:45:45 GMT
CMD ["/bin/bash"]
# Tue, 17 Feb 2026 16:45:45 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /usr/share/buildinfo/content-sets.json      
# Tue, 17 Feb 2026 16:45:45 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /root/buildinfo/content_manifests/content-sets.json      
# Tue, 17 Feb 2026 16:45:45 GMT
COPY file:b6e9611fd18f4ab100ec73ea6037b1118108a414096af83dfb78d47ad0a2b249 in /usr/share/buildinfo/labels.json      
# Tue, 17 Feb 2026 16:45:45 GMT
COPY file:b6e9611fd18f4ab100ec73ea6037b1118108a414096af83dfb78d47ad0a2b249 in /root/buildinfo/labels.json      
# Tue, 17 Feb 2026 16:45:46 GMT
LABEL "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="0ced2bbee24d5463d4530756a57f8db895246c48" "org.opencontainers.image.revision"="0ced2bbee24d5463d4530756a57f8db895246c48" "build-date"="2026-02-17T16:45:31Z" "org.opencontainers.image.created"="2026-02-17T16:45:31Z" "release"="1771346502"org.opencontainers.image.revision=0ced2bbee24d5463d4530756a57f8db895246c48,org.opencontainers.image.created=2026-02-17T16:45:31Z
# Wed, 18 Feb 2026 19:19:22 GMT
EXPOSE map[5601/tcp:{}]
# Wed, 18 Feb 2026 19:19:22 GMT
RUN microdnf install --setopt=tsflags=nodocs -y       fontconfig liberation-fonts-common freetype shadow-utils nss findutils &&       microdnf clean all # buildkit
# Wed, 18 Feb 2026 19:26:38 GMT
COPY --chown=1000:0 /usr/share/kibana /usr/share/kibana # buildkit
# Wed, 18 Feb 2026 19:26:39 GMT
COPY --chown=0:0 /bin/tini /bin/tini # buildkit
# Wed, 18 Feb 2026 19:26:39 GMT
COPY --chown=0:0 /usr/share/fonts/local/NotoSansCJK-Regular.ttc /usr/share/fonts/local/NotoSansCJK-Regular.ttc # buildkit
# Wed, 18 Feb 2026 19:26:39 GMT
RUN fc-cache -v # buildkit
# Wed, 18 Feb 2026 19:26:39 GMT
WORKDIR /usr/share/kibana
# Wed, 18 Feb 2026 19:26:39 GMT
RUN ln -s /usr/share/kibana /opt/kibana # buildkit
# Wed, 18 Feb 2026 19:26:39 GMT
ENV ELASTIC_CONTAINER=true
# Wed, 18 Feb 2026 19:26:39 GMT
ENV PATH=/usr/share/kibana/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 18 Feb 2026 19:26:39 GMT
COPY --chown=1000:0 config/kibana.yml /usr/share/kibana/config/kibana.yml # buildkit
# Wed, 18 Feb 2026 19:26:39 GMT
COPY bin/kibana-docker /usr/local/bin/ # buildkit
# Wed, 18 Feb 2026 19:26:40 GMT
RUN chmod g+ws /usr/share/kibana &&     find /usr/share/kibana -gid 0 -and -not -perm /g+w -exec chmod g+w {} \; # buildkit
# Wed, 18 Feb 2026 19:26:41 GMT
RUN find / -xdev -perm -4000 -exec chmod u-s {} + # buildkit
# Wed, 18 Feb 2026 19:26:41 GMT
RUN groupadd --gid 1000 kibana &&     useradd --uid 1000 --gid 1000 -G 0       --home-dir /usr/share/kibana --no-create-home       kibana # buildkit
# Wed, 18 Feb 2026 19:26:41 GMT
LABEL org.label-schema.build-date=2026-01-28T23:38:44.165Z org.label-schema.license=Elastic License org.label-schema.name=Kibana org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/kibana org.label-schema.usage=https://www.elastic.co/guide/en/kibana/reference/index.html org.label-schema.vcs-ref=f99524135b3b29ff4011629c9e8511086b1a597a org.label-schema.vcs-url=https://github.com/elastic/kibana org.label-schema.vendor=Elastic org.label-schema.version=9.2.5 org.opencontainers.image.created=2026-01-28T23:38:44.165Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/kibana/reference/index.html org.opencontainers.image.licenses=Elastic License org.opencontainers.image.revision=f99524135b3b29ff4011629c9e8511086b1a597a org.opencontainers.image.source=https://github.com/elastic/kibana org.opencontainers.image.title=Kibana org.opencontainers.image.url=https://www.elastic.co/products/kibana org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=9.2.5
# Wed, 18 Feb 2026 19:26:41 GMT
LABEL name=Kibana maintainer=infra@elastic.co vendor=Elastic version=9.2.5 release=1 summary=Kibana description=Your window into the Elastic Stack.
# Wed, 18 Feb 2026 19:26:41 GMT
RUN mkdir /licenses && ln LICENSE.txt /licenses/LICENSE # buildkit
# Wed, 18 Feb 2026 19:26:41 GMT
ENTRYPOINT ["/bin/tini" "--"]
# Wed, 18 Feb 2026 19:26:41 GMT
CMD ["/usr/local/bin/kibana-docker"]
# Wed, 18 Feb 2026 19:26:41 GMT
USER 1000
```

-	Layers:
	-	`sha256:063fbd5fac6af91f4042bbe66bae69795aa46675d5b0c800ed195ad79ed8fb02`  
		Last Modified: Tue, 17 Feb 2026 18:09:11 GMT  
		Size: 38.2 MB (38202534 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a0fbbb0d1dc4f02f5ed7bfdde45f12e67f69463cb89b41e763483e2b3aa8d7c`  
		Last Modified: Wed, 18 Feb 2026 19:27:46 GMT  
		Size: 19.5 MB (19476922 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c97e72a04fc4e00d8fd4b1982677dd02d0331d1d700e3044d6dafafc519a2f7`  
		Last Modified: Wed, 18 Feb 2026 19:27:53 GMT  
		Size: 386.8 MB (386771287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fd76cc66f7507d316349380b059e0eb434d0eba473be1da81b181af98dc652b`  
		Last Modified: Wed, 18 Feb 2026 19:27:45 GMT  
		Size: 9.1 KB (9100 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f3876a68f7eb211c612c7bcd8338cab5e1bb05463ae8d0a5e5095c04e84b862`  
		Last Modified: Wed, 18 Feb 2026 19:27:46 GMT  
		Size: 16.5 MB (16460492 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff43d64e1fc346fa5aeac1ad00bfe46bb23a29218fc16b0693e61d746165c5c2`  
		Last Modified: Wed, 18 Feb 2026 19:27:46 GMT  
		Size: 5.2 KB (5221 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37f3937d533d8a06921439e72ae1bf36438e65bf1da4473a917f87cbf7263fc6`  
		Last Modified: Wed, 18 Feb 2026 19:27:47 GMT  
		Size: 130.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f85e2b7de9f0a9752dd7c42aafe1e38951d2676c21cbc699a3e39a7e60a8d20`  
		Last Modified: Wed, 18 Feb 2026 19:27:47 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d687b8320a569524a50ba550041a88ab09daea33e7b9238a18adcbd4b2450c0`  
		Last Modified: Wed, 18 Feb 2026 19:27:48 GMT  
		Size: 4.9 KB (4893 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:054e83bb29e012c8dc676e417e06a362c5bf3b730fb1f5ab2424d204f6708a66`  
		Last Modified: Wed, 18 Feb 2026 19:27:49 GMT  
		Size: 400.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46e2aec4062a40f36b95ed9b90172d52fdbb510bb35a1021670bdba3d18db7c5`  
		Last Modified: Wed, 18 Feb 2026 19:27:49 GMT  
		Size: 73.4 KB (73448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef096d76964e8c1c127492168ef5addc33c77540dba3be1828cee43995c0fa2b`  
		Last Modified: Wed, 18 Feb 2026 19:27:49 GMT  
		Size: 1.0 KB (1044 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:851db3724e5d0fff0dcf47bbcfc1f2bd58566053a08b6167b6ca98f927a4617b`  
		Last Modified: Wed, 18 Feb 2026 19:27:50 GMT  
		Size: 1.7 KB (1708 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kibana:9.2.5` - unknown; unknown

```console
$ docker pull kibana@sha256:d9f8b2e1b3f4f992f09860f27bad30f48b84c476a991dadddbd520ae1dc83e32
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5789774 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:34b57b7ce345afe26d6f84c50252d360fbce1dd8b270f6b4532026c3204f18e3`

```dockerfile
```

-	Layers:
	-	`sha256:3f27c64769179c0d40988600f8a6d001058b2222b546d1d02db429bdf6ba83d4`  
		Last Modified: Wed, 18 Feb 2026 19:27:45 GMT  
		Size: 5.7 MB (5746291 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:17949546aadbb02d46c6582370ed0b511afd9b4209b7043094384bc5805d5e7f`  
		Last Modified: Wed, 18 Feb 2026 19:27:45 GMT  
		Size: 43.5 KB (43483 bytes)  
		MIME: application/vnd.in-toto+json

## `kibana:9.3.0`

```console
$ docker pull kibana@sha256:8f167d8b8c82d80ca8fc261637f548bb58190e9a445639285f20b07bd0a0e90e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `kibana:9.3.0` - linux; amd64

```console
$ docker pull kibana@sha256:e7559e2ed3093ed74a7d0fd5d7223207bf0eceb47be61aaecf62104b94b23895
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **453.9 MB (453860856 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e038d7194d1565e535e2f4d76f12362efcede4fea5218e0715897c933b15814f`
-	Entrypoint: `["\/bin\/tini","--"]`
-	Default Command: `["\/usr\/local\/bin\/kibana-docker"]`

```dockerfile
# Tue, 17 Feb 2026 16:42:45 GMT
LABEL maintainer="Red Hat, Inc."
# Tue, 17 Feb 2026 16:42:45 GMT
LABEL vendor="Red Hat, Inc."
# Tue, 17 Feb 2026 16:42:45 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Tue, 17 Feb 2026 16:42:45 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.7"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Tue, 17 Feb 2026 16:42:45 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Tue, 17 Feb 2026 16:42:45 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Tue, 17 Feb 2026 16:42:45 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Tue, 17 Feb 2026 16:42:45 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Tue, 17 Feb 2026 16:42:45 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Tue, 17 Feb 2026 16:42:45 GMT
LABEL io.openshift.expose-services=""
# Tue, 17 Feb 2026 16:42:45 GMT
LABEL io.openshift.tags="minimal rhel9"
# Tue, 17 Feb 2026 16:42:45 GMT
ENV container oci
# Tue, 17 Feb 2026 16:42:46 GMT
COPY dir:a84da6f36b88f4eb0d6c411f65b34c1a9d85150d3035dd516db4ece0c2569465 in /      
# Tue, 17 Feb 2026 16:42:46 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Tue, 17 Feb 2026 16:42:46 GMT
CMD ["/bin/bash"]
# Tue, 17 Feb 2026 16:42:46 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /usr/share/buildinfo/content-sets.json      
# Tue, 17 Feb 2026 16:42:46 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /root/buildinfo/content_manifests/content-sets.json      
# Tue, 17 Feb 2026 16:42:46 GMT
COPY file:6326b4becf4dcc53eab9a0e80efe304ada5421165d0586862d969cb5fa826bd8 in /usr/share/buildinfo/labels.json      
# Tue, 17 Feb 2026 16:42:46 GMT
COPY file:6326b4becf4dcc53eab9a0e80efe304ada5421165d0586862d969cb5fa826bd8 in /root/buildinfo/labels.json      
# Tue, 17 Feb 2026 16:42:46 GMT
LABEL "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="0ced2bbee24d5463d4530756a57f8db895246c48" "org.opencontainers.image.revision"="0ced2bbee24d5463d4530756a57f8db895246c48" "build-date"="2026-02-17T16:42:34Z" "org.opencontainers.image.created"="2026-02-17T16:42:34Z" "release"="1771346502"org.opencontainers.image.revision=0ced2bbee24d5463d4530756a57f8db895246c48,org.opencontainers.image.created=2026-02-17T16:42:34Z
# Wed, 18 Feb 2026 19:20:26 GMT
EXPOSE map[5601/tcp:{}]
# Wed, 18 Feb 2026 19:20:26 GMT
RUN microdnf install --setopt=tsflags=nodocs -y       fontconfig liberation-fonts-common freetype shadow-utils nss findutils &&       microdnf clean all # buildkit
# Wed, 18 Feb 2026 19:29:34 GMT
COPY --chown=1000:0 /usr/share/kibana /usr/share/kibana # buildkit
# Wed, 18 Feb 2026 19:29:35 GMT
COPY --chown=0:0 /bin/tini /bin/tini # buildkit
# Wed, 18 Feb 2026 19:29:35 GMT
COPY --chown=0:0 /usr/share/fonts/local/NotoSansCJK-Regular.ttc /usr/share/fonts/local/NotoSansCJK-Regular.ttc # buildkit
# Wed, 18 Feb 2026 19:29:35 GMT
RUN fc-cache -v # buildkit
# Wed, 18 Feb 2026 19:29:35 GMT
WORKDIR /usr/share/kibana
# Wed, 18 Feb 2026 19:29:35 GMT
RUN ln -s /usr/share/kibana /opt/kibana # buildkit
# Wed, 18 Feb 2026 19:29:35 GMT
ENV ELASTIC_CONTAINER=true
# Wed, 18 Feb 2026 19:29:35 GMT
ENV PATH=/usr/share/kibana/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 18 Feb 2026 19:29:35 GMT
COPY --chown=1000:0 config/kibana.yml /usr/share/kibana/config/kibana.yml # buildkit
# Wed, 18 Feb 2026 19:29:35 GMT
COPY bin/kibana-docker /usr/local/bin/ # buildkit
# Wed, 18 Feb 2026 19:29:36 GMT
RUN chmod g+ws /usr/share/kibana &&     find /usr/share/kibana -gid 0 -and -not -perm /g+w -exec chmod g+w {} \; # buildkit
# Wed, 18 Feb 2026 19:29:37 GMT
RUN find / -xdev -perm -4000 -exec chmod u-s {} + # buildkit
# Wed, 18 Feb 2026 19:29:37 GMT
RUN groupadd --gid 1000 kibana &&     useradd --uid 1000 --gid 1000 -G 0       --home-dir /usr/share/kibana --no-create-home       kibana # buildkit
# Wed, 18 Feb 2026 19:29:37 GMT
LABEL org.label-schema.build-date=2026-01-29T09:38:21.004Z org.label-schema.license=Elastic License org.label-schema.name=Kibana org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/kibana org.label-schema.usage=https://www.elastic.co/guide/en/kibana/reference/index.html org.label-schema.vcs-ref=30ab63cc0017fe2da7a84fb9b285dd762468802d org.label-schema.vcs-url=https://github.com/elastic/kibana org.label-schema.vendor=Elastic org.label-schema.version=9.3.0 org.opencontainers.image.created=2026-01-29T09:38:21.004Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/kibana/reference/index.html org.opencontainers.image.licenses=Elastic License org.opencontainers.image.revision=30ab63cc0017fe2da7a84fb9b285dd762468802d org.opencontainers.image.source=https://github.com/elastic/kibana org.opencontainers.image.title=Kibana org.opencontainers.image.url=https://www.elastic.co/products/kibana org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=9.3.0
# Wed, 18 Feb 2026 19:29:37 GMT
LABEL name=Kibana maintainer=infra@elastic.co vendor=Elastic version=9.3.0 release=1 summary=Kibana description=Your window into the Elastic Stack.
# Wed, 18 Feb 2026 19:29:37 GMT
RUN mkdir /licenses && ln LICENSE.txt /licenses/LICENSE # buildkit
# Wed, 18 Feb 2026 19:29:37 GMT
ENTRYPOINT ["/bin/tini" "--"]
# Wed, 18 Feb 2026 19:29:37 GMT
CMD ["/usr/local/bin/kibana-docker"]
# Wed, 18 Feb 2026 19:29:37 GMT
USER 1000
```

-	Layers:
	-	`sha256:4638e3415987f378f2d6dd70f9c6a2869dd5ebd09e3510ba45e46bbb6ec1a3dd`  
		Last Modified: Tue, 17 Feb 2026 18:08:54 GMT  
		Size: 40.0 MB (40033596 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1935278fd849ef6cb57a1e4c71c7f2bc2f1c8761e61487e6d371024520aa9b86`  
		Last Modified: Wed, 18 Feb 2026 19:30:33 GMT  
		Size: 19.5 MB (19526401 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6da7b3c8f4f6b4b4fd39799625c8b102a1b39b3dde97b11c6033698d02ae22f6`  
		Last Modified: Wed, 18 Feb 2026 19:30:41 GMT  
		Size: 377.7 MB (377742454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85f2eb7a8e1b0bab47955d7cd73dddfe6fa14b65b356861ad9b2c8130f71ee5d`  
		Last Modified: Wed, 18 Feb 2026 19:30:32 GMT  
		Size: 9.5 KB (9529 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c8a5110548ef09bc3baf638fbe7a6f73aea946804155c97be94685967191c52`  
		Last Modified: Wed, 18 Feb 2026 19:30:33 GMT  
		Size: 16.5 MB (16460484 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9098a5d9f272fb88b38e571dab95205907542eea4b7fe62627f1636bdc9e342e`  
		Last Modified: Wed, 18 Feb 2026 19:30:34 GMT  
		Size: 5.2 KB (5222 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be5532a1ff6ff1f7c5fd2a7e163903536bd09aad55759ce22923196c84d68639`  
		Last Modified: Wed, 18 Feb 2026 19:30:35 GMT  
		Size: 132.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ccd62203351442cb8ee850b59167e0773fc78eb80fcfc5bc57c5ce5001c6bf6`  
		Last Modified: Wed, 18 Feb 2026 19:30:35 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7a2b3b6cdd52c0e2811c86c02e83bf3ec3d5324f72fbefae73c780f2ae5e73c`  
		Last Modified: Wed, 18 Feb 2026 19:30:35 GMT  
		Size: 4.9 KB (4918 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0b371023308ba3f518657838c16e03adf3ae9f046581e403903179d5a465a25`  
		Last Modified: Wed, 18 Feb 2026 19:30:36 GMT  
		Size: 399.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e436c9ac0492cf5c48d6eb5efd6678ad6e073c23cd07f9071766648871f63a5`  
		Last Modified: Wed, 18 Feb 2026 19:30:36 GMT  
		Size: 74.5 KB (74540 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7c5c70828a9b43e9d4b40610bfa942b062a7a3ed3a4bdfd83590810938d0928`  
		Last Modified: Wed, 18 Feb 2026 19:30:36 GMT  
		Size: 1.0 KB (1045 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:217a43db041741e946e4cea369cdb86d5b5b1ac6bacfce5010cb1b5f49715dc6`  
		Last Modified: Wed, 18 Feb 2026 19:30:38 GMT  
		Size: 1.7 KB (1708 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kibana:9.3.0` - unknown; unknown

```console
$ docker pull kibana@sha256:705cd7d40d63d145720116f58c420d4a4462b74e29ed02fabffbfca13139c1ed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5856963 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c310b2d65448022e360a6e7c0b6fe8b468b1497577b27d84b824384b14cefb71`

```dockerfile
```

-	Layers:
	-	`sha256:c787ce2b9848db20b0f0b402441728e44857efafd5975ae4448060df3b30a60e`  
		Last Modified: Wed, 18 Feb 2026 19:30:33 GMT  
		Size: 5.8 MB (5813738 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ac236e3f495ce863273700bf3611350f11f488e2ace18c98d400f7659153ff79`  
		Last Modified: Wed, 18 Feb 2026 19:30:32 GMT  
		Size: 43.2 KB (43225 bytes)  
		MIME: application/vnd.in-toto+json

### `kibana:9.3.0` - linux; arm64 variant v8

```console
$ docker pull kibana@sha256:19027a61adf5e6813307a863cc12a278fdb8fa841bb28b4b7388aa190374d64c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **465.7 MB (465705710 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a81f644c3f2c0e46cbc60d1b17da838ce8866cd86c60b9fbd59fe8c0912a0ec9`
-	Entrypoint: `["\/bin\/tini","--"]`
-	Default Command: `["\/usr\/local\/bin\/kibana-docker"]`

```dockerfile
# Tue, 17 Feb 2026 16:45:44 GMT
LABEL maintainer="Red Hat, Inc."
# Tue, 17 Feb 2026 16:45:44 GMT
LABEL vendor="Red Hat, Inc."
# Tue, 17 Feb 2026 16:45:44 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Tue, 17 Feb 2026 16:45:44 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.7"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Tue, 17 Feb 2026 16:45:44 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Tue, 17 Feb 2026 16:45:44 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Tue, 17 Feb 2026 16:45:44 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Tue, 17 Feb 2026 16:45:44 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Tue, 17 Feb 2026 16:45:44 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Tue, 17 Feb 2026 16:45:44 GMT
LABEL io.openshift.expose-services=""
# Tue, 17 Feb 2026 16:45:44 GMT
LABEL io.openshift.tags="minimal rhel9"
# Tue, 17 Feb 2026 16:45:44 GMT
ENV container oci
# Tue, 17 Feb 2026 16:45:45 GMT
COPY dir:ac0ab1292a52ccb276077ed994531e1a3deef7d271c3502d95032264a0448d19 in /      
# Tue, 17 Feb 2026 16:45:45 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Tue, 17 Feb 2026 16:45:45 GMT
CMD ["/bin/bash"]
# Tue, 17 Feb 2026 16:45:45 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /usr/share/buildinfo/content-sets.json      
# Tue, 17 Feb 2026 16:45:45 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /root/buildinfo/content_manifests/content-sets.json      
# Tue, 17 Feb 2026 16:45:45 GMT
COPY file:b6e9611fd18f4ab100ec73ea6037b1118108a414096af83dfb78d47ad0a2b249 in /usr/share/buildinfo/labels.json      
# Tue, 17 Feb 2026 16:45:45 GMT
COPY file:b6e9611fd18f4ab100ec73ea6037b1118108a414096af83dfb78d47ad0a2b249 in /root/buildinfo/labels.json      
# Tue, 17 Feb 2026 16:45:46 GMT
LABEL "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="0ced2bbee24d5463d4530756a57f8db895246c48" "org.opencontainers.image.revision"="0ced2bbee24d5463d4530756a57f8db895246c48" "build-date"="2026-02-17T16:45:31Z" "org.opencontainers.image.created"="2026-02-17T16:45:31Z" "release"="1771346502"org.opencontainers.image.revision=0ced2bbee24d5463d4530756a57f8db895246c48,org.opencontainers.image.created=2026-02-17T16:45:31Z
# Wed, 18 Feb 2026 19:19:23 GMT
EXPOSE map[5601/tcp:{}]
# Wed, 18 Feb 2026 19:19:23 GMT
RUN microdnf install --setopt=tsflags=nodocs -y       fontconfig liberation-fonts-common freetype shadow-utils nss findutils &&       microdnf clean all # buildkit
# Wed, 18 Feb 2026 19:27:19 GMT
COPY --chown=1000:0 /usr/share/kibana /usr/share/kibana # buildkit
# Wed, 18 Feb 2026 19:27:19 GMT
COPY --chown=0:0 /bin/tini /bin/tini # buildkit
# Wed, 18 Feb 2026 19:27:19 GMT
COPY --chown=0:0 /usr/share/fonts/local/NotoSansCJK-Regular.ttc /usr/share/fonts/local/NotoSansCJK-Regular.ttc # buildkit
# Wed, 18 Feb 2026 19:27:20 GMT
RUN fc-cache -v # buildkit
# Wed, 18 Feb 2026 19:27:20 GMT
WORKDIR /usr/share/kibana
# Wed, 18 Feb 2026 19:27:20 GMT
RUN ln -s /usr/share/kibana /opt/kibana # buildkit
# Wed, 18 Feb 2026 19:27:20 GMT
ENV ELASTIC_CONTAINER=true
# Wed, 18 Feb 2026 19:27:20 GMT
ENV PATH=/usr/share/kibana/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 18 Feb 2026 19:27:20 GMT
COPY --chown=1000:0 config/kibana.yml /usr/share/kibana/config/kibana.yml # buildkit
# Wed, 18 Feb 2026 19:27:20 GMT
COPY bin/kibana-docker /usr/local/bin/ # buildkit
# Wed, 18 Feb 2026 19:27:21 GMT
RUN chmod g+ws /usr/share/kibana &&     find /usr/share/kibana -gid 0 -and -not -perm /g+w -exec chmod g+w {} \; # buildkit
# Wed, 18 Feb 2026 19:27:22 GMT
RUN find / -xdev -perm -4000 -exec chmod u-s {} + # buildkit
# Wed, 18 Feb 2026 19:27:22 GMT
RUN groupadd --gid 1000 kibana &&     useradd --uid 1000 --gid 1000 -G 0       --home-dir /usr/share/kibana --no-create-home       kibana # buildkit
# Wed, 18 Feb 2026 19:27:22 GMT
LABEL org.label-schema.build-date=2026-01-29T09:38:21.004Z org.label-schema.license=Elastic License org.label-schema.name=Kibana org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/kibana org.label-schema.usage=https://www.elastic.co/guide/en/kibana/reference/index.html org.label-schema.vcs-ref=30ab63cc0017fe2da7a84fb9b285dd762468802d org.label-schema.vcs-url=https://github.com/elastic/kibana org.label-schema.vendor=Elastic org.label-schema.version=9.3.0 org.opencontainers.image.created=2026-01-29T09:38:21.004Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/kibana/reference/index.html org.opencontainers.image.licenses=Elastic License org.opencontainers.image.revision=30ab63cc0017fe2da7a84fb9b285dd762468802d org.opencontainers.image.source=https://github.com/elastic/kibana org.opencontainers.image.title=Kibana org.opencontainers.image.url=https://www.elastic.co/products/kibana org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=9.3.0
# Wed, 18 Feb 2026 19:27:22 GMT
LABEL name=Kibana maintainer=infra@elastic.co vendor=Elastic version=9.3.0 release=1 summary=Kibana description=Your window into the Elastic Stack.
# Wed, 18 Feb 2026 19:27:22 GMT
RUN mkdir /licenses && ln LICENSE.txt /licenses/LICENSE # buildkit
# Wed, 18 Feb 2026 19:27:22 GMT
ENTRYPOINT ["/bin/tini" "--"]
# Wed, 18 Feb 2026 19:27:22 GMT
CMD ["/usr/local/bin/kibana-docker"]
# Wed, 18 Feb 2026 19:27:22 GMT
USER 1000
```

-	Layers:
	-	`sha256:063fbd5fac6af91f4042bbe66bae69795aa46675d5b0c800ed195ad79ed8fb02`  
		Last Modified: Tue, 17 Feb 2026 18:09:11 GMT  
		Size: 38.2 MB (38202534 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c51c2f83aead59c32e0bd4871cd8c6b176c5c406d6ad36ee677d6f1e10c99566`  
		Last Modified: Wed, 18 Feb 2026 19:28:28 GMT  
		Size: 19.5 MB (19476978 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef529eceda580ee38da10887b0ff632591515923d77fb7c6e8e003afdc4e4f73`  
		Last Modified: Wed, 18 Feb 2026 19:28:34 GMT  
		Size: 391.5 MB (391469313 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1fa17d451e33194bb3063f35c8433a9d8d95d047f57d8a396324d84e54b185e`  
		Last Modified: Wed, 18 Feb 2026 19:28:27 GMT  
		Size: 9.1 KB (9101 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c79dcc7f320360fbf820f45da287ca2d433eba6877831f8d018f8982973ca7c4`  
		Last Modified: Wed, 18 Feb 2026 19:28:28 GMT  
		Size: 16.5 MB (16460486 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1041abcdcc2829ecff5c60e6dc593faa84e1d82f6b9346015ade97fdfa0c66b`  
		Last Modified: Wed, 18 Feb 2026 19:28:28 GMT  
		Size: 5.2 KB (5222 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:815c868683ed31111850061740a84649ffccf0f30fd39f353c5a85e5dee967ec`  
		Last Modified: Wed, 18 Feb 2026 19:28:29 GMT  
		Size: 131.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3c1832eb3da13f9a320bbe4d9d4a95445e80a32df11509882b845931389ca60`  
		Last Modified: Wed, 18 Feb 2026 19:28:30 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea17fed25f97826f1425d0770514a8594cf995e5366fb1082ca61379d3097e36`  
		Last Modified: Wed, 18 Feb 2026 19:28:30 GMT  
		Size: 4.9 KB (4917 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9fc3ef18f0245d416bb49f94a749086d73144a319d583457464778f2dd58fd3`  
		Last Modified: Wed, 18 Feb 2026 19:28:31 GMT  
		Size: 399.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:219d911f9b7831a787dc09aa2185005d58deb0e2fa71ade46a32c1bfb780b9d7`  
		Last Modified: Wed, 18 Feb 2026 19:28:31 GMT  
		Size: 73.4 KB (73448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d46773fcbebd98733898303588b40e76e9c314489904244ab8a8fb360d0e2e85`  
		Last Modified: Wed, 18 Feb 2026 19:28:31 GMT  
		Size: 1.0 KB (1046 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f02521a1873a87c0fe798a9bcc323a2516ecace9fe2629a1122fa86d80556ef4`  
		Last Modified: Wed, 18 Feb 2026 19:28:32 GMT  
		Size: 1.7 KB (1707 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kibana:9.3.0` - unknown; unknown

```console
$ docker pull kibana@sha256:d237ee97b412ad3e79e78b884c95e924b4f3770a151776aff71b5a8f65a4d98d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5855893 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fd145d94466c5f3bb1bd6683b434e52821acc35aae1c011d0a83471c724327f4`

```dockerfile
```

-	Layers:
	-	`sha256:d0bf0ae6a2ee3a762160e85f9d9cd58b75b104f6f237cfdbb5744675f467e8ce`  
		Last Modified: Wed, 18 Feb 2026 19:28:27 GMT  
		Size: 5.8 MB (5812410 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9d3bd02b4a8c6b04009282f0ba33236b2a03864c27155ffd5f708cbe9b372228`  
		Last Modified: Wed, 18 Feb 2026 19:28:27 GMT  
		Size: 43.5 KB (43483 bytes)  
		MIME: application/vnd.in-toto+json
