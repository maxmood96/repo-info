<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `kibana`

-	[`kibana:7.17.23`](#kibana71723)
-	[`kibana:8.15.0`](#kibana8150)

## `kibana:7.17.23`

```console
$ docker pull kibana@sha256:35caffeb480e6cd55afaad72f78820f802e21c2d73996c1b46c2998c0513f977
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `kibana:7.17.23` - linux; amd64

```console
$ docker pull kibana@sha256:4a556e133eb84198ada7d022bf584e51baaebfde37504b41ce71cf426f3a8b9f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **348.0 MB (347998549 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ac3fcd6e3cf2f6c872942fc7bd4ba40133ca8ccb9b026b91c1655e4c27f3714`
-	Entrypoint: `["\/bin\/tini","--"]`
-	Default Command: `["\/usr\/local\/bin\/kibana-docker"]`

```dockerfile
# Mon, 03 Jun 2024 17:10:41 GMT
ARG RELEASE
# Mon, 03 Jun 2024 17:10:41 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 03 Jun 2024 17:10:41 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 03 Jun 2024 17:10:41 GMT
LABEL org.opencontainers.image.version=20.04
# Mon, 03 Jun 2024 17:10:43 GMT
ADD file:e7cff353f027ecf0a2cb1cdd51714de3b083a11a0d965f104489f9a7e6925056 in / 
# Mon, 03 Jun 2024 17:10:43 GMT
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
	-	`sha256:9ea8908f47652b59b8055316d9c0e16b365e2b5cee15d3efcb79e2957e3e7cad`  
		Last Modified: Mon, 03 Jun 2024 17:19:42 GMT  
		Size: 27.5 MB (27511769 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14d58b7e02241f0df45b825ff566cea76ee72b8c775cae627ee25361c56d4277`  
		Last Modified: Tue, 30 Jul 2024 23:57:48 GMT  
		Size: 10.7 MB (10705202 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eda1d045d8f037a4cede106b3388e4b71f17e79ef8df52fcba8c54347c2f185b`  
		Last Modified: Tue, 30 Jul 2024 23:57:47 GMT  
		Size: 9.5 KB (9527 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1b64aa82aaeb099fa20713dfc68109f297e6c11f36a3c2376bf51b4420c303e`  
		Last Modified: Tue, 30 Jul 2024 23:57:47 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:011470b4653a8a15d00138553b18033af8cfae90234c32d72e0c75ae8d9d7d1c`  
		Last Modified: Tue, 30 Jul 2024 23:57:48 GMT  
		Size: 16.5 MB (16460482 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f43ee48d02cbcee441b6c03ceeb6a46ef4d254ec3f1eb18f989b54e62439ff1a`  
		Last Modified: Tue, 30 Jul 2024 23:57:48 GMT  
		Size: 5.3 KB (5291 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4fa930acf74ba1436d35d769f85d4a0f5236b5bee6fac214c3ed3293223c3885`  
		Last Modified: Tue, 30 Jul 2024 23:57:53 GMT  
		Size: 293.1 MB (293109389 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72419d7838a48b15b0b37feef8e4f9561453602386d4366a888d94ecec16fbfc`  
		Last Modified: Tue, 30 Jul 2024 23:57:49 GMT  
		Size: 131.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa35ee0148608aecd81fea5e3fe55b7dadda160f681f08db28f5bbe63c0f30d8`  
		Last Modified: Tue, 30 Jul 2024 23:57:49 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1e2291e7031ce8eeada88ce52cf6ef6a95c1e6f2c78fe3a9d34281c096a1b51`  
		Last Modified: Tue, 30 Jul 2024 23:57:49 GMT  
		Size: 4.5 KB (4504 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c5ea02a62cdbed7d9d9119ff82194e2e88c46a4b8b2abdd413595d825684e3f`  
		Last Modified: Tue, 30 Jul 2024 23:57:50 GMT  
		Size: 400.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7a82cf58aed41de89d341d4826a2e50a2ad4775dac5723460a01082af10094f`  
		Last Modified: Tue, 30 Jul 2024 23:57:50 GMT  
		Size: 189.4 KB (189433 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bf852f8d2be258938275c8ebf8b462536332a0fcf92b9255e3f861b91dcffd1`  
		Last Modified: Tue, 30 Jul 2024 23:57:50 GMT  
		Size: 1.8 KB (1801 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kibana:7.17.23` - unknown; unknown

```console
$ docker pull kibana@sha256:89ee645a423757a9cdd3642628f9486d024f848fbdbeb690f98a9e45334c85bb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.4 MB (3419170 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a40f3393a250cf0eaa3bae4e1070bffac2a2090f8aff2fc8e93c7be4a32d29ac`

```dockerfile
```

-	Layers:
	-	`sha256:ff2aa860944a74d732cd830751c55973763ed24ce422e3428f3a44d9f06dc055`  
		Last Modified: Tue, 30 Jul 2024 23:57:47 GMT  
		Size: 3.4 MB (3374915 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:76dbad1e538d8201885abb5aaff1ec3895761dcd2e0ee8aae20484ea53fc7c65`  
		Last Modified: Tue, 30 Jul 2024 23:57:47 GMT  
		Size: 44.3 KB (44255 bytes)  
		MIME: application/vnd.in-toto+json

### `kibana:7.17.23` - linux; arm64 variant v8

```console
$ docker pull kibana@sha256:1353d52871cac840200d9698a3eb1238f74c663d65f687de03d975edc6946cba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **359.0 MB (359016136 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:29f574757a8d970439eba5f628ced8961e04f15ce547904e9bf02ab0344784da`
-	Entrypoint: `["\/bin\/tini","--"]`
-	Default Command: `["\/usr\/local\/bin\/kibana-docker"]`

```dockerfile
# Mon, 03 Jun 2024 16:52:57 GMT
ARG RELEASE
# Mon, 03 Jun 2024 16:52:57 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 03 Jun 2024 16:52:57 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 03 Jun 2024 16:52:57 GMT
LABEL org.opencontainers.image.version=20.04
# Mon, 03 Jun 2024 16:52:59 GMT
ADD file:6d8cc056ee741f09a6c7d965d8e2027d80ed2eccbfb0312593ce52d9256db437 in / 
# Mon, 03 Jun 2024 16:52:59 GMT
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
	-	`sha256:4bba57925f299085ba607447fc5910c019b3f453e0b2f007969b9ffc316dac0e`  
		Last Modified: Wed, 31 Jul 2024 00:01:34 GMT  
		Size: 10.6 MB (10550849 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d35f577835ff9843df8879c0eabf1b1d3a74286a83f5cbe16834e4ef9abe412b`  
		Last Modified: Wed, 31 Jul 2024 00:01:33 GMT  
		Size: 9.1 KB (9095 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:052d22e5fd9fce8ddd9cd9b9ce938c631ae8c43b967731f5fb950e5ec91a2653`  
		Last Modified: Wed, 31 Jul 2024 00:01:33 GMT  
		Size: 161.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:608d6054fd32fbb88a7dd962d42c58a606368541bde3ed9a4649ea2da98271c8`  
		Last Modified: Wed, 31 Jul 2024 00:01:34 GMT  
		Size: 16.5 MB (16460488 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:caf2fe5ead40bf2466c3c9fc4f8557e3cc4055311ef5f1a962b3b41c41bc407a`  
		Last Modified: Wed, 31 Jul 2024 00:01:34 GMT  
		Size: 5.3 KB (5289 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59513cb252a4a14889c0825d2f60c7a8bbbd6e61107ee9e8fd24cd514426de55`  
		Last Modified: Wed, 31 Jul 2024 00:01:41 GMT  
		Size: 305.8 MB (305825313 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04872247a276cbbeed28bb4210eb7b04b56394444e99fb628dc3cf3e07fe516c`  
		Last Modified: Wed, 31 Jul 2024 00:01:35 GMT  
		Size: 132.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:836b97af19fcef9d07b972b643c65a4589b3ecdf9cab88dc555a7d1b7684f29d`  
		Last Modified: Wed, 31 Jul 2024 00:01:35 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48fd60819533a68f4676ab4a6e6cfab69514651cce5fe2e909259265aa4f4bf9`  
		Last Modified: Wed, 31 Jul 2024 00:01:36 GMT  
		Size: 4.5 KB (4507 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12364ea9b96f6ab6ecb07008960b5ea8b4df40657b9182749d7880fef7e83962`  
		Last Modified: Wed, 31 Jul 2024 00:01:36 GMT  
		Size: 399.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf4e9865008c53eb15133972fe1f756aedcf49c80b03ecd77e711204ba6a29ee`  
		Last Modified: Wed, 31 Jul 2024 00:01:37 GMT  
		Size: 183.4 KB (183421 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf9cb5b9a9d0bb6aa7349368667fe98a7a9d06c9f12a599fdc73d23d390a6fb6`  
		Last Modified: Wed, 31 Jul 2024 00:01:37 GMT  
		Size: 1.8 KB (1804 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kibana:7.17.23` - unknown; unknown

```console
$ docker pull kibana@sha256:716d39e3482f6681774ea7c4169fb5d82e56220966d017c97bf5b32d927da4bd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.4 MB (3419685 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0cc9c6cc72328da35b343f95346542674ec3f20db12dfe45fb766b7bba825a07`

```dockerfile
```

-	Layers:
	-	`sha256:1536f40d5b88a733acf031c0783f384898da3325094e4eafb416b7fc07356716`  
		Last Modified: Wed, 31 Jul 2024 00:01:34 GMT  
		Size: 3.4 MB (3375165 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4e6a5bfa6e3bf0740999b6836dcd8a597689b6bfb70684f5bfb9d97cb0e8c5c6`  
		Last Modified: Wed, 31 Jul 2024 00:01:33 GMT  
		Size: 44.5 KB (44520 bytes)  
		MIME: application/vnd.in-toto+json

## `kibana:8.15.0`

**does not exist** (yet?)
