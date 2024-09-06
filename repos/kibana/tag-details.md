<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `kibana`

-	[`kibana:7.17.23`](#kibana71723)
-	[`kibana:8.15.1`](#kibana8151)

## `kibana:7.17.23`

```console
$ docker pull kibana@sha256:2ade8523d73f0bfe9cecd14fe8bdd32bf4f2f5bb38654953c9dfb38d402eb7e8
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `kibana:7.17.23` - linux; amd64

```console
$ docker pull kibana@sha256:1844c4d541ebeb441edfc816388d5f77b9d2632aa0b078c558b470bdbd4e4a6a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **348.0 MB (347998338 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:904f213d9f88f5b5723d1e512a754eca7bcf47ee58ddc4436a3cc773c728e341`
-	Entrypoint: `["\/bin\/tini","--"]`
-	Default Command: `["\/usr\/local\/bin\/kibana-docker"]`

```dockerfile
# Tue, 30 Jul 2024 15:39:57 GMT
ARG RELEASE
# Tue, 30 Jul 2024 15:39:57 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 30 Jul 2024 15:39:57 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 30 Jul 2024 15:39:57 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 30 Jul 2024 15:39:57 GMT
ADD file:e7cff353f027ecf0a2cb1cdd51714de3b083a11a0d965f104489f9a7e6925056 in / 
# Tue, 30 Jul 2024 15:39:57 GMT
CMD ["/bin/bash"]
# Tue, 30 Jul 2024 15:39:57 GMT
EXPOSE map[5601/tcp:{}]
# Tue, 30 Jul 2024 15:39:57 GMT
RUN for iter in {1..10}; do       export DEBIAN_FRONTEND=noninteractive &&       apt-get update  &&       apt-get upgrade -y  &&       apt-get install -y --no-install-recommends        fontconfig fonts-liberation libnss3 libfontconfig1 ca-certificates curl &&       apt-get clean &&       rm -rf /var/lib/apt/lists/* && exit_code=0 && break || exit_code=$? && echo "apt-get error: retry $iter in 10s" &&       sleep 10;     done;     (exit $exit_code) # buildkit
# Tue, 30 Jul 2024 15:39:57 GMT
RUN set -e ;     TINI_BIN="" ;     case "$(arch)" in         aarch64)             TINI_BIN='tini-arm64' ;             ;;         x86_64)             TINI_BIN='tini-amd64' ;             ;;         *) echo >&2 "Unsupported architecture $(arch)" ; exit 1 ;;     esac ;   TINI_VERSION='v0.19.0' ;   curl --retry 8 -S -L -O "https://github.com/krallin/tini/releases/download/${TINI_VERSION}/${TINI_BIN}" ;   curl --retry 8 -S -L -O "https://github.com/krallin/tini/releases/download/${TINI_VERSION}/${TINI_BIN}.sha256sum" ;   sha256sum -c "${TINI_BIN}.sha256sum" ;   rm "${TINI_BIN}.sha256sum" ;   mv "${TINI_BIN}" /bin/tini ;   chmod +x /bin/tini # buildkit
# Tue, 30 Jul 2024 15:39:57 GMT
RUN mkdir /usr/share/fonts/local # buildkit
# Tue, 30 Jul 2024 15:39:57 GMT
RUN curl --retry 8 -S -L -o /usr/share/fonts/local/NotoSansCJK-Regular.ttc https://github.com/googlefonts/noto-cjk/raw/NotoSansV2.001/NotoSansCJK-Regular.ttc # buildkit
# Tue, 30 Jul 2024 15:39:57 GMT
RUN echo "5dcd1c336cc9344cb77c03a0cd8982ca8a7dc97d620fd6c9c434e02dcb1ceeb3  /usr/share/fonts/local/NotoSansCJK-Regular.ttc" | sha256sum -c - # buildkit
# Tue, 30 Jul 2024 15:39:57 GMT
RUN fc-cache -v # buildkit
# Tue, 30 Jul 2024 15:39:57 GMT
COPY --chown=1000:0 /usr/share/kibana /usr/share/kibana # buildkit
# Tue, 30 Jul 2024 15:39:57 GMT
WORKDIR /usr/share/kibana
# Tue, 30 Jul 2024 15:39:57 GMT
RUN ln -s /usr/share/kibana /opt/kibana # buildkit
# Tue, 30 Jul 2024 15:39:57 GMT
ENV ELASTIC_CONTAINER=true
# Tue, 30 Jul 2024 15:39:57 GMT
ENV PATH=/usr/share/kibana/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 30 Jul 2024 15:39:57 GMT
COPY --chown=1000:0 config/kibana.yml /usr/share/kibana/config/kibana.yml # buildkit
# Tue, 30 Jul 2024 15:39:57 GMT
COPY bin/kibana-docker /usr/local/bin/ # buildkit
# Tue, 30 Jul 2024 15:39:57 GMT
RUN chmod g+ws /usr/share/kibana &&     find /usr/share/kibana -gid 0 -and -not -perm /g+w -exec chmod g+w {} \; # buildkit
# Tue, 30 Jul 2024 15:39:57 GMT
RUN find / -xdev -perm -4000 -exec chmod u-s {} + # buildkit
# Tue, 30 Jul 2024 15:39:57 GMT
RUN groupadd --gid 1000 kibana &&     useradd --uid 1000 --gid 1000 -G 0       --home-dir /usr/share/kibana --no-create-home       kibana # buildkit
# Tue, 30 Jul 2024 15:39:57 GMT
LABEL org.label-schema.build-date=2024-07-25T11:08:38.582Z org.label-schema.license=Elastic License org.label-schema.name=Kibana org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/kibana org.label-schema.usage=https://www.elastic.co/guide/en/kibana/reference/index.html org.label-schema.vcs-ref=89cafc519e1d6e0e08d8cf5c13eee6886fe6e412 org.label-schema.vcs-url=https://github.com/elastic/kibana org.label-schema.vendor=Elastic org.label-schema.version=7.17.23 org.opencontainers.image.created=2024-07-25T11:08:38.582Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/kibana/reference/index.html org.opencontainers.image.licenses=Elastic License org.opencontainers.image.revision=89cafc519e1d6e0e08d8cf5c13eee6886fe6e412 org.opencontainers.image.source=https://github.com/elastic/kibana org.opencontainers.image.title=Kibana org.opencontainers.image.url=https://www.elastic.co/products/kibana org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=7.17.23
# Tue, 30 Jul 2024 15:39:57 GMT
ENTRYPOINT ["/bin/tini" "--"]
# Tue, 30 Jul 2024 15:39:57 GMT
CMD ["/usr/local/bin/kibana-docker"]
# Tue, 30 Jul 2024 15:39:57 GMT
USER kibana
```

-	Layers:
	-	`sha256:602d8ad51b8130f3fcd71cb936dea612ebc799666136abf2e5914585b3178a4a`  
		Last Modified: Tue, 13 Aug 2024 10:23:50 GMT  
		Size: 27.5 MB (27511769 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a9bb484a9e0944ae82555e79ef862dcc52a8653ea6ac3c7c7cf4233331e1859`  
		Last Modified: Sat, 17 Aug 2024 02:02:27 GMT  
		Size: 10.7 MB (10704958 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b67a8f2e5a5a3e609498ab322d9a6d6b7532e6c6afa4d96e517fc378e5deeb9c`  
		Last Modified: Sat, 17 Aug 2024 02:02:27 GMT  
		Size: 9.5 KB (9526 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd6c722700526d9fd7cdc045cbd833363f02d53862ba73837eb308c89861e9c2`  
		Last Modified: Sat, 17 Aug 2024 02:02:27 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:146394d40477f5af5b863a4498c10575b48728bcf919b48fa1c6fd1332e1d622`  
		Last Modified: Sat, 17 Aug 2024 02:02:28 GMT  
		Size: 16.5 MB (16460484 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43fcde2e627c7e0ef636d18f4fbc84f6b98e052bdb794b8666d117db78b93929`  
		Last Modified: Sat, 17 Aug 2024 02:02:28 GMT  
		Size: 5.3 KB (5292 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44b27376f4881fefc78065e9ced95b992383f2518711a521f78064f7d92ce6d3`  
		Last Modified: Sat, 17 Aug 2024 02:02:32 GMT  
		Size: 293.1 MB (293109424 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4b3dc78f9589df6f232a4332ec57837c742f5bc75527d3ecd44cf42d252cf34`  
		Last Modified: Sat, 17 Aug 2024 02:02:28 GMT  
		Size: 131.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75285eb9bfa9123b0a311484425afb8a005646783815258c6524deab30f8d4ee`  
		Last Modified: Sat, 17 Aug 2024 02:02:28 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:868de2361dad3b3a9ea92cbff994441b0dca04fca54bc01ed3d54e45e089a86f`  
		Last Modified: Sat, 17 Aug 2024 02:02:29 GMT  
		Size: 4.5 KB (4504 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de5f5d997b7a780ac0e9c3e599c8dbf4df262d94cfa5c73cd3f750948251b3ad`  
		Last Modified: Sat, 17 Aug 2024 02:02:29 GMT  
		Size: 399.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bff6c80bb2f66888a076991d96dfb8a9b5abb64758ff8e227fe88a5bbb4a9909`  
		Last Modified: Sat, 17 Aug 2024 02:02:29 GMT  
		Size: 189.4 KB (189433 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:607f485af5ae250ad1bd22ca8b560da4389270660e90c911ca675d2a47c51ef6`  
		Last Modified: Sat, 17 Aug 2024 02:02:29 GMT  
		Size: 1.8 KB (1799 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kibana:7.17.23` - unknown; unknown

```console
$ docker pull kibana@sha256:48e0bc16c34f467b2e70df7a0b303e864a27a40d7e66ce69e17eac6571f90a61
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.4 MB (3419170 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c231041d5be7b7698bc4a490f2837633181930d68427baa64a6f0e6e6ba68378`

```dockerfile
```

-	Layers:
	-	`sha256:c33a8e90337a488ead7a07c14615533c3b7c9e95d736c6b393b31381e5768e18`  
		Last Modified: Sat, 17 Aug 2024 02:02:27 GMT  
		Size: 3.4 MB (3374915 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:01c5ea74598324987c0d5ff413c74155428e10f5ce3a74a925ce8f7efb8ffdb4`  
		Last Modified: Sat, 17 Aug 2024 02:02:27 GMT  
		Size: 44.3 KB (44255 bytes)  
		MIME: application/vnd.in-toto+json

### `kibana:7.17.23` - linux; arm64 variant v8

```console
$ docker pull kibana@sha256:2decbf0c4cd8864207b0a70b15c5c662b8a2c99bac9804af36d5d5711d41dd43
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **359.0 MB (359017263 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b1cad2ac43b29d091b026137ba8dc12ff5979c8384b4e9b446f2c1785037ecf1`
-	Entrypoint: `["\/bin\/tini","--"]`
-	Default Command: `["\/usr\/local\/bin\/kibana-docker"]`

```dockerfile
# Tue, 30 Jul 2024 15:39:57 GMT
ARG RELEASE
# Tue, 30 Jul 2024 15:39:57 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 30 Jul 2024 15:39:57 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 30 Jul 2024 15:39:57 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 30 Jul 2024 15:39:57 GMT
ADD file:6d8cc056ee741f09a6c7d965d8e2027d80ed2eccbfb0312593ce52d9256db437 in / 
# Tue, 30 Jul 2024 15:39:57 GMT
CMD ["/bin/bash"]
# Tue, 30 Jul 2024 15:39:57 GMT
EXPOSE map[5601/tcp:{}]
# Tue, 30 Jul 2024 15:39:57 GMT
RUN for iter in {1..10}; do       export DEBIAN_FRONTEND=noninteractive &&       apt-get update  &&       apt-get upgrade -y  &&       apt-get install -y --no-install-recommends        fontconfig fonts-liberation libnss3 libfontconfig1 ca-certificates curl &&       apt-get clean &&       rm -rf /var/lib/apt/lists/* && exit_code=0 && break || exit_code=$? && echo "apt-get error: retry $iter in 10s" &&       sleep 10;     done;     (exit $exit_code) # buildkit
# Tue, 30 Jul 2024 15:39:57 GMT
RUN set -e ;     TINI_BIN="" ;     case "$(arch)" in         aarch64)             TINI_BIN='tini-arm64' ;             ;;         x86_64)             TINI_BIN='tini-amd64' ;             ;;         *) echo >&2 "Unsupported architecture $(arch)" ; exit 1 ;;     esac ;   TINI_VERSION='v0.19.0' ;   curl --retry 8 -S -L -O "https://github.com/krallin/tini/releases/download/${TINI_VERSION}/${TINI_BIN}" ;   curl --retry 8 -S -L -O "https://github.com/krallin/tini/releases/download/${TINI_VERSION}/${TINI_BIN}.sha256sum" ;   sha256sum -c "${TINI_BIN}.sha256sum" ;   rm "${TINI_BIN}.sha256sum" ;   mv "${TINI_BIN}" /bin/tini ;   chmod +x /bin/tini # buildkit
# Tue, 30 Jul 2024 15:39:57 GMT
RUN mkdir /usr/share/fonts/local # buildkit
# Tue, 30 Jul 2024 15:39:57 GMT
RUN curl --retry 8 -S -L -o /usr/share/fonts/local/NotoSansCJK-Regular.ttc https://github.com/googlefonts/noto-cjk/raw/NotoSansV2.001/NotoSansCJK-Regular.ttc # buildkit
# Tue, 30 Jul 2024 15:39:57 GMT
RUN echo "5dcd1c336cc9344cb77c03a0cd8982ca8a7dc97d620fd6c9c434e02dcb1ceeb3  /usr/share/fonts/local/NotoSansCJK-Regular.ttc" | sha256sum -c - # buildkit
# Tue, 30 Jul 2024 15:39:57 GMT
RUN fc-cache -v # buildkit
# Tue, 30 Jul 2024 15:39:57 GMT
COPY --chown=1000:0 /usr/share/kibana /usr/share/kibana # buildkit
# Tue, 30 Jul 2024 15:39:57 GMT
WORKDIR /usr/share/kibana
# Tue, 30 Jul 2024 15:39:57 GMT
RUN ln -s /usr/share/kibana /opt/kibana # buildkit
# Tue, 30 Jul 2024 15:39:57 GMT
ENV ELASTIC_CONTAINER=true
# Tue, 30 Jul 2024 15:39:57 GMT
ENV PATH=/usr/share/kibana/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 30 Jul 2024 15:39:57 GMT
COPY --chown=1000:0 config/kibana.yml /usr/share/kibana/config/kibana.yml # buildkit
# Tue, 30 Jul 2024 15:39:57 GMT
COPY bin/kibana-docker /usr/local/bin/ # buildkit
# Tue, 30 Jul 2024 15:39:57 GMT
RUN chmod g+ws /usr/share/kibana &&     find /usr/share/kibana -gid 0 -and -not -perm /g+w -exec chmod g+w {} \; # buildkit
# Tue, 30 Jul 2024 15:39:57 GMT
RUN find / -xdev -perm -4000 -exec chmod u-s {} + # buildkit
# Tue, 30 Jul 2024 15:39:57 GMT
RUN groupadd --gid 1000 kibana &&     useradd --uid 1000 --gid 1000 -G 0       --home-dir /usr/share/kibana --no-create-home       kibana # buildkit
# Tue, 30 Jul 2024 15:39:57 GMT
LABEL org.label-schema.build-date=2024-07-25T11:08:38.582Z org.label-schema.license=Elastic License org.label-schema.name=Kibana org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/kibana org.label-schema.usage=https://www.elastic.co/guide/en/kibana/reference/index.html org.label-schema.vcs-ref=89cafc519e1d6e0e08d8cf5c13eee6886fe6e412 org.label-schema.vcs-url=https://github.com/elastic/kibana org.label-schema.vendor=Elastic org.label-schema.version=7.17.23 org.opencontainers.image.created=2024-07-25T11:08:38.582Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/kibana/reference/index.html org.opencontainers.image.licenses=Elastic License org.opencontainers.image.revision=89cafc519e1d6e0e08d8cf5c13eee6886fe6e412 org.opencontainers.image.source=https://github.com/elastic/kibana org.opencontainers.image.title=Kibana org.opencontainers.image.url=https://www.elastic.co/products/kibana org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=7.17.23
# Tue, 30 Jul 2024 15:39:57 GMT
ENTRYPOINT ["/bin/tini" "--"]
# Tue, 30 Jul 2024 15:39:57 GMT
CMD ["/usr/local/bin/kibana-docker"]
# Tue, 30 Jul 2024 15:39:57 GMT
USER kibana
```

-	Layers:
	-	`sha256:f02209be4ee528c246399de81af4552e52adb005a8a499815607b6b0d42746bf`  
		Last Modified: Mon, 03 Jun 2024 17:19:48 GMT  
		Size: 26.0 MB (25974217 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c7ec6d7c740205dde1821161aaf1bb91deb61868514c9cbe785fc15ed226c3a`  
		Last Modified: Sat, 17 Aug 2024 03:02:14 GMT  
		Size: 10.6 MB (10551949 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96f112612f9dc7a95e7163707c7c52b23613d80a5853cf9630b7197bc96c7487`  
		Last Modified: Sat, 17 Aug 2024 03:02:13 GMT  
		Size: 9.1 KB (9097 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:374e1524be0d193d0871047996dede1abbcc3474f4aadafba47decadb8e97ca3`  
		Last Modified: Sat, 17 Aug 2024 03:02:13 GMT  
		Size: 157.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1c501a5714a7f9d6fd7430207ab9908f6e7d359a949bce0acd64859f510a352`  
		Last Modified: Sat, 17 Aug 2024 03:02:14 GMT  
		Size: 16.5 MB (16460493 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13a31e3ca25fd482ae4c758682ac489c135462e29766e89dbcc02ae53c4edc70`  
		Last Modified: Sat, 17 Aug 2024 03:02:14 GMT  
		Size: 5.3 KB (5291 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:199d8ba363dafe7a13c2838c86bb90d2761826d5e35b4c7aba649e580e2420d8`  
		Last Modified: Sat, 17 Aug 2024 03:02:22 GMT  
		Size: 305.8 MB (305825328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d717fb2d1eb3ef6c52a839bf56cc8c209b9882ae1babfb01027df1316c15e598`  
		Last Modified: Sat, 17 Aug 2024 03:02:15 GMT  
		Size: 131.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5299e47c54427070ec3268ccd671602ece537151d2107438f72e288715b27e4`  
		Last Modified: Sat, 17 Aug 2024 03:02:15 GMT  
		Size: 399.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1e86499aa833f447386853b54788d9f281d422646244c74bc9018f8a0b1a73a`  
		Last Modified: Sat, 17 Aug 2024 03:02:16 GMT  
		Size: 4.5 KB (4508 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f5efa9518ad12954a482cd0433b280af39cf1ef1e9917e834be59b43bea03c1`  
		Last Modified: Sat, 17 Aug 2024 03:02:16 GMT  
		Size: 402.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3dfe5ce02788518a52379500fd2b4611a8be63749b8b63e56b11e025f6cee0ef`  
		Last Modified: Sat, 17 Aug 2024 03:02:16 GMT  
		Size: 183.4 KB (183422 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22abc766f81335595076517a773488b011cd8ab564d6dbc32f54e0383dd6f773`  
		Last Modified: Sat, 17 Aug 2024 03:02:17 GMT  
		Size: 1.8 KB (1805 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kibana:7.17.23` - unknown; unknown

```console
$ docker pull kibana@sha256:bffcfbe15701737171ba860b979b5a602bed145d6747395cb2a1744d0b948a22
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.4 MB (3419685 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:801adbf1187ee59215c6dc27c2dfd2f904acdb0b2ef4278f6fed266d8bfdc626`

```dockerfile
```

-	Layers:
	-	`sha256:e15988ebd88a00546bb7ef0e770ce129468c5222fe65c5ce184140eb91328321`  
		Last Modified: Sat, 17 Aug 2024 03:02:14 GMT  
		Size: 3.4 MB (3375165 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7e50ec5f62303c9a63171c7b4df15cd5b43d9bf13a8bc47b967826cf28529f8a`  
		Last Modified: Sat, 17 Aug 2024 03:02:13 GMT  
		Size: 44.5 KB (44520 bytes)  
		MIME: application/vnd.in-toto+json

## `kibana:8.15.1`

```console
$ docker pull kibana@sha256:826304508019ce346f35a6817b1e730c18efe2b5882bf12daec477060c98010e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `kibana:8.15.1` - linux; amd64

```console
$ docker pull kibana@sha256:426b9e373557bf62e6885aa98782505025d41f20100b069a310c75939d2926b4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **393.7 MB (393742062 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e0dde5a104ccd67354bd7538f97937b9942963e46d52dec64a90d8cf924284a`
-	Entrypoint: `["\/bin\/tini","--"]`
-	Default Command: `["\/usr\/local\/bin\/kibana-docker"]`

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
EXPOSE map[5601/tcp:{}]
# Thu, 05 Sep 2024 16:37:13 GMT
RUN for iter in {1..10}; do       export DEBIAN_FRONTEND=noninteractive &&       apt-get update  &&       apt-get upgrade -y  &&       apt-get install -y --no-install-recommends        fontconfig libnss3 curl ca-certificates &&       apt-get clean &&       rm -rf /var/lib/apt/lists/* && exit_code=0 && break || exit_code=$? && echo "apt-get error: retry $iter in 10s" &&       sleep 10;     done;     (exit $exit_code) # buildkit
# Thu, 05 Sep 2024 16:37:13 GMT
COPY --chown=1000:0 /usr/share/kibana /usr/share/kibana # buildkit
# Thu, 05 Sep 2024 16:37:13 GMT
COPY --chown=0:0 /bin/tini /bin/tini # buildkit
# Thu, 05 Sep 2024 16:37:13 GMT
COPY --chown=0:0 /usr/share/fonts/local/NotoSansCJK-Regular.ttc /usr/share/fonts/local/NotoSansCJK-Regular.ttc # buildkit
# Thu, 05 Sep 2024 16:37:13 GMT
RUN fc-cache -v # buildkit
# Thu, 05 Sep 2024 16:37:13 GMT
WORKDIR /usr/share/kibana
# Thu, 05 Sep 2024 16:37:13 GMT
RUN ln -s /usr/share/kibana /opt/kibana # buildkit
# Thu, 05 Sep 2024 16:37:13 GMT
ENV ELASTIC_CONTAINER=true
# Thu, 05 Sep 2024 16:37:13 GMT
ENV PATH=/usr/share/kibana/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 05 Sep 2024 16:37:13 GMT
COPY --chown=1000:0 config/kibana.yml /usr/share/kibana/config/kibana.yml # buildkit
# Thu, 05 Sep 2024 16:37:13 GMT
COPY bin/kibana-docker /usr/local/bin/ # buildkit
# Thu, 05 Sep 2024 16:37:13 GMT
RUN chmod g+ws /usr/share/kibana &&     find /usr/share/kibana -gid 0 -and -not -perm /g+w -exec chmod g+w {} \; # buildkit
# Thu, 05 Sep 2024 16:37:13 GMT
RUN find / -xdev -perm -4000 -exec chmod u-s {} + # buildkit
# Thu, 05 Sep 2024 16:37:13 GMT
RUN groupadd --gid 1000 kibana &&     useradd --uid 1000 --gid 1000 -G 0       --home-dir /usr/share/kibana --no-create-home       kibana # buildkit
# Thu, 05 Sep 2024 16:37:13 GMT
LABEL org.label-schema.build-date=2024-09-02T12:15:21.436Z org.label-schema.license=Elastic License org.label-schema.name=Kibana org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/kibana org.label-schema.usage=https://www.elastic.co/guide/en/kibana/reference/index.html org.label-schema.vcs-ref=f66ec5b0ddd990d103489c47ca1bcb97dc50bc6b org.label-schema.vcs-url=https://github.com/elastic/kibana org.label-schema.vendor=Elastic org.label-schema.version=8.15.1 org.opencontainers.image.created=2024-09-02T12:15:21.436Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/kibana/reference/index.html org.opencontainers.image.licenses=Elastic License org.opencontainers.image.revision=f66ec5b0ddd990d103489c47ca1bcb97dc50bc6b org.opencontainers.image.source=https://github.com/elastic/kibana org.opencontainers.image.title=Kibana org.opencontainers.image.url=https://www.elastic.co/products/kibana org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=8.15.1
# Thu, 05 Sep 2024 16:37:13 GMT
ENTRYPOINT ["/bin/tini" "--"]
# Thu, 05 Sep 2024 16:37:13 GMT
CMD ["/usr/local/bin/kibana-docker"]
# Thu, 05 Sep 2024 16:37:13 GMT
USER 1000
```

-	Layers:
	-	`sha256:602d8ad51b8130f3fcd71cb936dea612ebc799666136abf2e5914585b3178a4a`  
		Last Modified: Tue, 13 Aug 2024 10:23:50 GMT  
		Size: 27.5 MB (27511769 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63fdb71e81f1aab48fe4befba210ca076bee27c9ca7a9c74036983fe07eb77f5`  
		Last Modified: Thu, 05 Sep 2024 22:05:33 GMT  
		Size: 10.9 MB (10945277 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f38bcb526e838da90ffc8bdce23188725f29cabdc81b94a4dd49711ccfa18bf`  
		Last Modified: Thu, 05 Sep 2024 22:05:43 GMT  
		Size: 338.6 MB (338612904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbb7acd1efc4f4ea7280b7bb2d31b715da2a447e03f9bb6b5a89fcd61030dfb1`  
		Last Modified: Thu, 05 Sep 2024 22:05:33 GMT  
		Size: 9.5 KB (9530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:846f1629c72a6eb06ecccd8fdb1ec09e93b90a05b26bafbc4f29ca6727276c21`  
		Last Modified: Thu, 05 Sep 2024 22:05:34 GMT  
		Size: 16.5 MB (16460489 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ce6b9672912b161e80b737151de4a4cc5edb1f61e51103e03737f8c00f393c5`  
		Last Modified: Thu, 05 Sep 2024 22:05:34 GMT  
		Size: 5.3 KB (5282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34aab2c6e0fba6241730b041de8a36e1c1c535a5051e2dce9b016de3374a02b2`  
		Last Modified: Thu, 05 Sep 2024 22:05:34 GMT  
		Size: 131.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f81ccb102c8fa5e7d5bcf38f08c1b25667c82b13952aa2cf520c387febbe2cb`  
		Last Modified: Thu, 05 Sep 2024 22:05:35 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:208be2ce3fe324c3b60ca9a08c42d48dbbb347b8176815fd750de341949530a8`  
		Last Modified: Thu, 05 Sep 2024 22:05:35 GMT  
		Size: 4.6 KB (4627 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8519ba4305d25228c6d62a46bf92f529f35e43c323b284aded34f190b0dff4e8`  
		Last Modified: Thu, 05 Sep 2024 22:05:35 GMT  
		Size: 399.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b53aaa438adccd4389f3be76872845d7319ab2dbc8935c53eba1c994cb1ab66`  
		Last Modified: Thu, 05 Sep 2024 22:05:35 GMT  
		Size: 189.4 KB (189430 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c108aac256f036478ad3e192075be59e27990d0fdc8ca93803bcfc10b6090681`  
		Last Modified: Thu, 05 Sep 2024 22:05:36 GMT  
		Size: 1.8 KB (1797 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kibana:8.15.1` - unknown; unknown

```console
$ docker pull kibana@sha256:8cf439d59109dbab0a84c1b2eb1429a3a689fa731e26953a5f6a711bb8182cc0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4103967 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0cb8dd79606ee06e81ead98b0723dd86a4bdb203c5c3d1b9908a2997fd7ff254`

```dockerfile
```

-	Layers:
	-	`sha256:2220ecce9ce8bd7409c827767dd36c3c279905ac8d4f4af20449dfb5f160d03f`  
		Last Modified: Thu, 05 Sep 2024 22:05:33 GMT  
		Size: 4.1 MB (4063579 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ef92ee7d97b53f99ff9d9a72abeadbe370c71dfab34187f6457adfa4b8f83b42`  
		Last Modified: Thu, 05 Sep 2024 22:05:33 GMT  
		Size: 40.4 KB (40388 bytes)  
		MIME: application/vnd.in-toto+json

### `kibana:8.15.1` - linux; arm64 variant v8

```console
$ docker pull kibana@sha256:0723e618fbb73c4e4fb85dd8db1b94031aaf96d39954e6e66d7a7ce82b32f74f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **404.6 MB (404648844 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec167ad0e8d996730439ac291a9114b03863932e5908f69735fb0bf73faf7def`
-	Entrypoint: `["\/bin\/tini","--"]`
-	Default Command: `["\/usr\/local\/bin\/kibana-docker"]`

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
EXPOSE map[5601/tcp:{}]
# Thu, 05 Sep 2024 16:37:13 GMT
RUN for iter in {1..10}; do       export DEBIAN_FRONTEND=noninteractive &&       apt-get update  &&       apt-get upgrade -y  &&       apt-get install -y --no-install-recommends        fontconfig libnss3 curl ca-certificates &&       apt-get clean &&       rm -rf /var/lib/apt/lists/* && exit_code=0 && break || exit_code=$? && echo "apt-get error: retry $iter in 10s" &&       sleep 10;     done;     (exit $exit_code) # buildkit
# Thu, 05 Sep 2024 16:37:13 GMT
COPY --chown=1000:0 /usr/share/kibana /usr/share/kibana # buildkit
# Thu, 05 Sep 2024 16:37:13 GMT
COPY --chown=0:0 /bin/tini /bin/tini # buildkit
# Thu, 05 Sep 2024 16:37:13 GMT
COPY --chown=0:0 /usr/share/fonts/local/NotoSansCJK-Regular.ttc /usr/share/fonts/local/NotoSansCJK-Regular.ttc # buildkit
# Thu, 05 Sep 2024 16:37:13 GMT
RUN fc-cache -v # buildkit
# Thu, 05 Sep 2024 16:37:13 GMT
WORKDIR /usr/share/kibana
# Thu, 05 Sep 2024 16:37:13 GMT
RUN ln -s /usr/share/kibana /opt/kibana # buildkit
# Thu, 05 Sep 2024 16:37:13 GMT
ENV ELASTIC_CONTAINER=true
# Thu, 05 Sep 2024 16:37:13 GMT
ENV PATH=/usr/share/kibana/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 05 Sep 2024 16:37:13 GMT
COPY --chown=1000:0 config/kibana.yml /usr/share/kibana/config/kibana.yml # buildkit
# Thu, 05 Sep 2024 16:37:13 GMT
COPY bin/kibana-docker /usr/local/bin/ # buildkit
# Thu, 05 Sep 2024 16:37:13 GMT
RUN chmod g+ws /usr/share/kibana &&     find /usr/share/kibana -gid 0 -and -not -perm /g+w -exec chmod g+w {} \; # buildkit
# Thu, 05 Sep 2024 16:37:13 GMT
RUN find / -xdev -perm -4000 -exec chmod u-s {} + # buildkit
# Thu, 05 Sep 2024 16:37:13 GMT
RUN groupadd --gid 1000 kibana &&     useradd --uid 1000 --gid 1000 -G 0       --home-dir /usr/share/kibana --no-create-home       kibana # buildkit
# Thu, 05 Sep 2024 16:37:13 GMT
LABEL org.label-schema.build-date=2024-09-02T12:15:21.436Z org.label-schema.license=Elastic License org.label-schema.name=Kibana org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/kibana org.label-schema.usage=https://www.elastic.co/guide/en/kibana/reference/index.html org.label-schema.vcs-ref=f66ec5b0ddd990d103489c47ca1bcb97dc50bc6b org.label-schema.vcs-url=https://github.com/elastic/kibana org.label-schema.vendor=Elastic org.label-schema.version=8.15.1 org.opencontainers.image.created=2024-09-02T12:15:21.436Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/kibana/reference/index.html org.opencontainers.image.licenses=Elastic License org.opencontainers.image.revision=f66ec5b0ddd990d103489c47ca1bcb97dc50bc6b org.opencontainers.image.source=https://github.com/elastic/kibana org.opencontainers.image.title=Kibana org.opencontainers.image.url=https://www.elastic.co/products/kibana org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=8.15.1
# Thu, 05 Sep 2024 16:37:13 GMT
ENTRYPOINT ["/bin/tini" "--"]
# Thu, 05 Sep 2024 16:37:13 GMT
CMD ["/usr/local/bin/kibana-docker"]
# Thu, 05 Sep 2024 16:37:13 GMT
USER 1000
```

-	Layers:
	-	`sha256:f02209be4ee528c246399de81af4552e52adb005a8a499815607b6b0d42746bf`  
		Last Modified: Mon, 03 Jun 2024 17:19:48 GMT  
		Size: 26.0 MB (25974217 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdedf750a744afb7e0b04b26877aee1247d6f9ea65ba56552f24a1e9924a4a8f`  
		Last Modified: Sat, 17 Aug 2024 02:58:25 GMT  
		Size: 10.8 MB (10797079 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d67bbe7b6b7cf2f5aa1b7074695ee58bdfbb78703ae71443d4a2399b2772950`  
		Last Modified: Thu, 05 Sep 2024 22:19:44 GMT  
		Size: 351.2 MB (351211846 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ad594e431daa16b323ee60eaa4a41bb2712e36d6abb364a2241d98d9f3d6ccb`  
		Last Modified: Thu, 05 Sep 2024 22:19:36 GMT  
		Size: 9.1 KB (9098 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b40a6c171b38d01f72d4ea8f5248aca5bfc24c14358e647a9919026bd3e04021`  
		Last Modified: Thu, 05 Sep 2024 22:19:37 GMT  
		Size: 16.5 MB (16460489 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca544c9570d1048f3e9bbd6be835c61deb7bc868a4e6906859644370737c530b`  
		Last Modified: Thu, 05 Sep 2024 22:19:36 GMT  
		Size: 5.3 KB (5298 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ecd8aae931d61ddfff3a278853ab881df32709bdf8dc383cbe3959e5eb1d1da4`  
		Last Modified: Thu, 05 Sep 2024 22:19:37 GMT  
		Size: 131.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb61633fd72db7111f7b16095a54e20aaf28c97ec71bc98706055df82c800771`  
		Last Modified: Thu, 05 Sep 2024 22:19:37 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:603599a53019ffbb9514220fdf858648d0c35bf7a55db356819c3f0d590d5c92`  
		Last Modified: Thu, 05 Sep 2024 22:19:38 GMT  
		Size: 4.6 KB (4629 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bcf6ba2a0bb454ff9eef46c7bd1c4f9b6ae0acd28cdb12ed6983c6de8177248a`  
		Last Modified: Thu, 05 Sep 2024 22:19:38 GMT  
		Size: 400.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d08571e2eb63d047e75cd36fd4f48645ff2899d5c6da2df30093e30e748a9d76`  
		Last Modified: Thu, 05 Sep 2024 22:19:38 GMT  
		Size: 183.4 KB (183421 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:966f24bc4a7595e6c6fe9e52b3f6d21d7efd3126096fe17475da1a23c631c6cb`  
		Last Modified: Thu, 05 Sep 2024 22:19:39 GMT  
		Size: 1.8 KB (1806 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kibana:8.15.1` - unknown; unknown

```console
$ docker pull kibana@sha256:fccf0bf0652985000c9ada30b61f1ec3e0de4327c272e9e38943aeaea0a9f891
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4104481 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c261549449f8b65a1e1338bb85124133f418caa2728ccc4d3870a73107f67483`

```dockerfile
```

-	Layers:
	-	`sha256:cd2717e09601bc29b2b62d5caf5bb9cc2cbc39df3d3060788924df14f0c7a859`  
		Last Modified: Thu, 05 Sep 2024 22:19:36 GMT  
		Size: 4.1 MB (4063829 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6cecb08a450809924cae3019c818a66407f573cf16955ac96992a8093f2f03a6`  
		Last Modified: Thu, 05 Sep 2024 22:19:36 GMT  
		Size: 40.7 KB (40652 bytes)  
		MIME: application/vnd.in-toto+json
