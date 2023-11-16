<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `kibana`

-	[`kibana:7.17.15`](#kibana71715)
-	[`kibana:8.11.1`](#kibana8111)

## `kibana:7.17.15`

```console
$ docker pull kibana@sha256:ace97abf87328ed44c2c8e4ab529119cd4f73c6c8f5efa61b280977621f0481e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `kibana:7.17.15` - linux; amd64

```console
$ docker pull kibana@sha256:849a11430b89cb7728bb042c87c92e979d6a01db785165b92968096525f68f7f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **398.0 MB (397959432 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e26fb4f5acbbdce32ca7fe332b0a00a671cda6534b1e4a05be571a4573681947`
-	Entrypoint: `["\/bin\/tini","--"]`
-	Default Command: `["\/usr\/local\/bin\/kibana-docker"]`

```dockerfile
# Tue, 03 Oct 2023 10:45:50 GMT
ARG RELEASE
# Tue, 03 Oct 2023 10:45:50 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 03 Oct 2023 10:45:50 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 03 Oct 2023 10:45:50 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 03 Oct 2023 10:45:51 GMT
ADD file:4809da414c2d478b4d991cbdaa2df457f2b3d07d0ff6cf673f09a66f90833e81 in / 
# Tue, 03 Oct 2023 10:45:52 GMT
CMD ["/bin/bash"]
# Fri, 10 Nov 2023 21:17:26 GMT
EXPOSE map[5601/tcp:{}]
# Fri, 10 Nov 2023 21:17:26 GMT
RUN for iter in {1..10}; do       export DEBIAN_FRONTEND=noninteractive &&       apt-get update  &&       apt-get upgrade -y  &&       apt-get install -y --no-install-recommends        fontconfig fonts-liberation libnss3 libfontconfig1 ca-certificates curl &&       apt-get clean &&       rm -rf /var/lib/apt/lists/* && exit_code=0 && break || exit_code=$? && echo "apt-get error: retry $iter in 10s" &&       sleep 10;     done;     (exit $exit_code) # buildkit
# Fri, 10 Nov 2023 21:17:27 GMT
RUN set -e ;     TINI_BIN="" ;     case "$(arch)" in         aarch64)             TINI_BIN='tini-arm64' ;             ;;         x86_64)             TINI_BIN='tini-amd64' ;             ;;         *) echo >&2 "Unsupported architecture $(arch)" ; exit 1 ;;     esac ;   TINI_VERSION='v0.19.0' ;   curl --retry 8 -S -L -O "https://github.com/krallin/tini/releases/download/${TINI_VERSION}/${TINI_BIN}" ;   curl --retry 8 -S -L -O "https://github.com/krallin/tini/releases/download/${TINI_VERSION}/${TINI_BIN}.sha256sum" ;   sha256sum -c "${TINI_BIN}.sha256sum" ;   rm "${TINI_BIN}.sha256sum" ;   mv "${TINI_BIN}" /bin/tini ;   chmod +x /bin/tini # buildkit
# Fri, 10 Nov 2023 21:17:28 GMT
RUN mkdir /usr/share/fonts/local # buildkit
# Fri, 10 Nov 2023 21:17:28 GMT
RUN curl --retry 8 -S -L -o /usr/share/fonts/local/NotoSansCJK-Regular.ttc https://github.com/googlefonts/noto-cjk/raw/NotoSansV2.001/NotoSansCJK-Regular.ttc # buildkit
# Fri, 10 Nov 2023 21:17:29 GMT
RUN echo "5dcd1c336cc9344cb77c03a0cd8982ca8a7dc97d620fd6c9c434e02dcb1ceeb3  /usr/share/fonts/local/NotoSansCJK-Regular.ttc" | sha256sum -c - # buildkit
# Fri, 10 Nov 2023 21:17:29 GMT
RUN fc-cache -v # buildkit
# Fri, 10 Nov 2023 21:18:41 GMT
COPY /usr/share/kibana /usr/share/kibana # buildkit
# Fri, 10 Nov 2023 21:18:41 GMT
WORKDIR /usr/share/kibana
# Fri, 10 Nov 2023 21:18:41 GMT
RUN ln -s /usr/share/kibana /opt/kibana # buildkit
# Fri, 10 Nov 2023 21:18:41 GMT
ENV ELASTIC_CONTAINER=true
# Fri, 10 Nov 2023 21:18:41 GMT
ENV PATH=/usr/share/kibana/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 10 Nov 2023 21:18:41 GMT
COPY config/kibana.yml /usr/share/kibana/config/kibana.yml # buildkit
# Fri, 10 Nov 2023 21:18:41 GMT
COPY bin/kibana-docker /usr/local/bin/ # buildkit
# Fri, 10 Nov 2023 21:18:42 GMT
RUN chmod g+ws /usr/share/kibana &&     find /usr/share/kibana -gid 0 -and -not -perm /g+w -exec chmod g+w {} \; # buildkit
# Fri, 10 Nov 2023 21:18:42 GMT
RUN find / -xdev -perm -4000 -exec chmod u-s {} + # buildkit
# Fri, 10 Nov 2023 21:18:43 GMT
RUN groupadd --gid 1000 kibana &&     useradd --uid 1000 --gid 1000 -G 0       --home-dir /usr/share/kibana --no-create-home       kibana # buildkit
# Fri, 10 Nov 2023 21:18:43 GMT
LABEL org.label-schema.build-date=2023-11-10T20:46:53.174Z org.label-schema.license=Elastic License org.label-schema.name=Kibana org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/kibana org.label-schema.usage=https://www.elastic.co/guide/en/kibana/reference/index.html org.label-schema.vcs-ref=60e0d4fa38a2c99350f1533c141f641edbb8e608 org.label-schema.vcs-url=https://github.com/elastic/kibana org.label-schema.vendor=Elastic org.label-schema.version=7.17.15 org.opencontainers.image.created=2023-11-10T20:46:53.174Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/kibana/reference/index.html org.opencontainers.image.licenses=Elastic License org.opencontainers.image.revision=60e0d4fa38a2c99350f1533c141f641edbb8e608 org.opencontainers.image.source=https://github.com/elastic/kibana org.opencontainers.image.title=Kibana org.opencontainers.image.url=https://www.elastic.co/products/kibana org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=7.17.15
# Fri, 10 Nov 2023 21:18:43 GMT
ENTRYPOINT ["/bin/tini" "--"]
# Fri, 10 Nov 2023 21:18:43 GMT
CMD ["/usr/local/bin/kibana-docker"]
# Fri, 10 Nov 2023 21:18:43 GMT
USER kibana
```

-	Layers:
	-	`sha256:70db4e7a2af7f73b7cef95301fc20fbedcfe68e5fb874e2cfba0b5ae41a066ca`  
		Last Modified: Wed, 25 Oct 2023 11:40:40 GMT  
		Size: 31.8 MB (31790746 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb3f34d1ff2b7ea81fba4afacae98c95d7735ba703af0f6af4a32bbc21abc740`  
		Last Modified: Mon, 13 Nov 2023 17:58:59 GMT  
		Size: 11.7 MB (11717552 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:913312171dc75316a6a7d1a5a02a933095c3a130670390b941a8591fea358d06`  
		Last Modified: Mon, 13 Nov 2023 17:58:38 GMT  
		Size: 10.2 KB (10155 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e091b483bef35c3a9e5ac2cff2aad44667fb4bc6036a407b019f75218bf29160`  
		Last Modified: Mon, 13 Nov 2023 17:58:46 GMT  
		Size: 163.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:963297fa798e8e78eec031e4b1f3bf8c238d6d920e88fb63559ac5d71074499b`  
		Last Modified: Mon, 13 Nov 2023 17:58:39 GMT  
		Size: 17.8 MB (17831459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89732bc7504122601f40269fc9ddfb70982e633ea9caf641ae45736f2846b004`  
		Last Modified: Sat, 26 Jan 2019 16:40:00 GMT  
		Size: 39.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81c0c2098454a2913c7df17e3f85dfd78fc61cc6ed544ce2ab95f071e7153eaf`  
		Last Modified: Mon, 13 Nov 2023 17:58:36 GMT  
		Size: 5.9 KB (5924 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0efb7cfc499a82f65c39db5abc09d78cc45e2518b48f1ecbda4e159a1f26eb7`  
		Last Modified: Mon, 13 Nov 2023 17:58:57 GMT  
		Size: 336.4 MB (336387079 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89732bc7504122601f40269fc9ddfb70982e633ea9caf641ae45736f2846b004`  
		Last Modified: Sat, 26 Jan 2019 16:40:00 GMT  
		Size: 39.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15e310fe125f6f51e999f0160046e462be40c250bfb1489f70352f0511718945`  
		Last Modified: Mon, 13 Nov 2023 17:58:16 GMT  
		Size: 141.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e543894663c15ee647e66a4ede8c5dce9fe144782ede9dfa238450c090933939`  
		Last Modified: Mon, 13 Nov 2023 17:58:48 GMT  
		Size: 417.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1cc004e2e087846e9c96c38a7b53ffa74be65304754466fc3ea204e69526fb36`  
		Last Modified: Mon, 13 Nov 2023 17:58:17 GMT  
		Size: 5.0 KB (5009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56c0beafef60aaa8f5ae7a220d2f512ae4356cfbc3d54378cb096339e06fc4b0`  
		Last Modified: Mon, 13 Nov 2023 17:58:31 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc3b3a7bf9a0971dca19b9f475394e73d51d6f040b58f6bcb8420c9c02bf8197`  
		Last Modified: Mon, 13 Nov 2023 17:59:01 GMT  
		Size: 208.2 KB (208245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc09a842ddf2c74c80b9d00cb883b61280e2cd870cce655eb8142f9db668aa9f`  
		Last Modified: Mon, 13 Nov 2023 17:58:45 GMT  
		Size: 2.0 KB (2045 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kibana:7.17.15` - unknown; unknown

```console
$ docker pull kibana@sha256:fb152fdba3767ceebc894f7da011b0c04ee573f44225d177131d3253edc31ee6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (3046836 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e522dc817cfe195d1e5b82efa5dbb48044d7f8455f3fc2e4a47e2e6805a8d73f`

```dockerfile
```

-	Layers:
	-	`sha256:0d152a54af23f94cfa88844b9eb11ee817e00f52c3e288f952672a8cf6087159`  
		Last Modified: Thu, 16 Nov 2023 01:20:35 GMT  
		Size: 3.0 MB (3038270 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:41d1fcf28d176a8859c30bacae5432c2020d979b966a94d82649fe4468248662`  
		Last Modified: Thu, 16 Nov 2023 01:20:35 GMT  
		Size: 8.6 KB (8566 bytes)  
		MIME: application/vnd.in-toto+json

## `kibana:8.11.1`

```console
$ docker pull kibana@sha256:89ae04f8c4e62eb40c1bc5850dbf5107127f76dfa01ddabe918fb3d0af23a214
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `kibana:8.11.1` - linux; amd64

```console
$ docker pull kibana@sha256:f510ef281e3ce774aed7659f3eee88e48ecf4d8cfa36daabe663a3954e3af9f4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **419.7 MB (419709077 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fda5cc289ef7b12d67ab067140c56e815da53c1db4e3235c361be676341c4995`
-	Entrypoint: `["\/bin\/tini","--"]`
-	Default Command: `["\/usr\/local\/bin\/kibana-docker"]`

```dockerfile
# Tue, 03 Oct 2023 10:45:50 GMT
ARG RELEASE
# Tue, 03 Oct 2023 10:45:50 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 03 Oct 2023 10:45:50 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 03 Oct 2023 10:45:50 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 03 Oct 2023 10:45:51 GMT
ADD file:4809da414c2d478b4d991cbdaa2df457f2b3d07d0ff6cf673f09a66f90833e81 in / 
# Tue, 03 Oct 2023 10:45:52 GMT
CMD ["/bin/bash"]
# Fri, 10 Nov 2023 21:42:46 GMT
EXPOSE map[5601/tcp:{}]
# Fri, 10 Nov 2023 21:42:46 GMT
RUN for iter in {1..10}; do       export DEBIAN_FRONTEND=noninteractive &&       apt-get update  &&       apt-get upgrade -y  &&       apt-get install -y --no-install-recommends        fontconfig fonts-liberation libnss3 libfontconfig1 ca-certificates curl &&       apt-get clean &&       rm -rf /var/lib/apt/lists/* && exit_code=0 && break || exit_code=$? && echo "apt-get error: retry $iter in 10s" &&       sleep 10;     done;     (exit $exit_code) # buildkit
# Fri, 10 Nov 2023 21:42:48 GMT
RUN set -e ;     TINI_BIN="" ;     case "$(arch)" in         aarch64)             TINI_BIN='tini-arm64' ;             ;;         x86_64)             TINI_BIN='tini-amd64' ;             ;;         *) echo >&2 "Unsupported architecture $(arch)" ; exit 1 ;;     esac ;   TINI_VERSION='v0.19.0' ;   curl --retry 8 -S -L -O "https://github.com/krallin/tini/releases/download/${TINI_VERSION}/${TINI_BIN}" ;   curl --retry 8 -S -L -O "https://github.com/krallin/tini/releases/download/${TINI_VERSION}/${TINI_BIN}.sha256sum" ;   sha256sum -c "${TINI_BIN}.sha256sum" ;   rm "${TINI_BIN}.sha256sum" ;   mv "${TINI_BIN}" /bin/tini ;   chmod +x /bin/tini # buildkit
# Fri, 10 Nov 2023 21:42:49 GMT
RUN mkdir /usr/share/fonts/local # buildkit
# Fri, 10 Nov 2023 21:42:50 GMT
RUN curl --retry 8 -S -L -o /usr/share/fonts/local/NotoSansCJK-Regular.ttc https://github.com/googlefonts/noto-cjk/raw/NotoSansV2.001/NotoSansCJK-Regular.ttc # buildkit
# Fri, 10 Nov 2023 21:42:50 GMT
RUN echo "5dcd1c336cc9344cb77c03a0cd8982ca8a7dc97d620fd6c9c434e02dcb1ceeb3  /usr/share/fonts/local/NotoSansCJK-Regular.ttc" | sha256sum -c - # buildkit
# Fri, 10 Nov 2023 21:42:50 GMT
RUN fc-cache -v # buildkit
# Fri, 10 Nov 2023 21:44:48 GMT
COPY /usr/share/kibana /usr/share/kibana # buildkit
# Fri, 10 Nov 2023 21:44:48 GMT
WORKDIR /usr/share/kibana
# Fri, 10 Nov 2023 21:44:48 GMT
RUN ln -s /usr/share/kibana /opt/kibana # buildkit
# Fri, 10 Nov 2023 21:44:48 GMT
ENV ELASTIC_CONTAINER=true
# Fri, 10 Nov 2023 21:44:48 GMT
ENV PATH=/usr/share/kibana/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 10 Nov 2023 21:44:48 GMT
COPY config/kibana.yml /usr/share/kibana/config/kibana.yml # buildkit
# Fri, 10 Nov 2023 21:44:48 GMT
COPY bin/kibana-docker /usr/local/bin/ # buildkit
# Fri, 10 Nov 2023 21:44:49 GMT
RUN chmod g+ws /usr/share/kibana &&     find /usr/share/kibana -gid 0 -and -not -perm /g+w -exec chmod g+w {} \; # buildkit
# Fri, 10 Nov 2023 21:44:50 GMT
RUN find / -xdev -perm -4000 -exec chmod u-s {} + # buildkit
# Fri, 10 Nov 2023 21:44:51 GMT
RUN groupadd --gid 1000 kibana &&     useradd --uid 1000 --gid 1000 -G 0       --home-dir /usr/share/kibana --no-create-home       kibana # buildkit
# Fri, 10 Nov 2023 21:44:51 GMT
LABEL org.label-schema.build-date=2023-11-10T21:05:44.206Z org.label-schema.license=Elastic License org.label-schema.name=Kibana org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/kibana org.label-schema.usage=https://www.elastic.co/guide/en/kibana/reference/index.html org.label-schema.vcs-ref=09feaf416f986b239b8e8ad95ecdda0f9d56ebec org.label-schema.vcs-url=https://github.com/elastic/kibana org.label-schema.vendor=Elastic org.label-schema.version=8.11.1 org.opencontainers.image.created=2023-11-10T21:05:44.206Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/kibana/reference/index.html org.opencontainers.image.licenses=Elastic License org.opencontainers.image.revision=09feaf416f986b239b8e8ad95ecdda0f9d56ebec org.opencontainers.image.source=https://github.com/elastic/kibana org.opencontainers.image.title=Kibana org.opencontainers.image.url=https://www.elastic.co/products/kibana org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=8.11.1
# Fri, 10 Nov 2023 21:44:51 GMT
ENTRYPOINT ["/bin/tini" "--"]
# Fri, 10 Nov 2023 21:44:51 GMT
CMD ["/usr/local/bin/kibana-docker"]
# Fri, 10 Nov 2023 21:44:51 GMT
USER kibana
```

-	Layers:
	-	`sha256:70db4e7a2af7f73b7cef95301fc20fbedcfe68e5fb874e2cfba0b5ae41a066ca`  
		Last Modified: Wed, 25 Oct 2023 11:40:40 GMT  
		Size: 31.8 MB (31790746 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f972df8c969bbc116a2bb69930432c1963232b843683e63aaff9ea04ced9d54`  
		Last Modified: Mon, 13 Nov 2023 14:12:53 GMT  
		Size: 11.7 MB (11717986 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9401695156e098dab46e087e429e01eaa5d1aa428a8d6050bcdc052019984bce`  
		Last Modified: Mon, 13 Nov 2023 14:12:52 GMT  
		Size: 10.2 KB (10156 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30f248e9383edfbff10d7c827e1dc1cb7da877503f94444d094e50a6b2dd39fb`  
		Last Modified: Mon, 13 Nov 2023 14:12:53 GMT  
		Size: 164.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1f80395ecb82bdf59f7e65e5c7b1a0efe095944ee916dfd59ff6c9b6c36c96b`  
		Last Modified: Mon, 13 Nov 2023 14:12:53 GMT  
		Size: 17.8 MB (17831459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89732bc7504122601f40269fc9ddfb70982e633ea9caf641ae45736f2846b004`  
		Last Modified: Sat, 26 Jan 2019 16:40:00 GMT  
		Size: 39.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e865dab2dcf3ae75cbaf19817749df43eca15847d8edff4cd6e3f37d020718a5`  
		Last Modified: Mon, 13 Nov 2023 14:12:54 GMT  
		Size: 6.0 KB (5953 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:582891637c6a403a7862d7eff36f47a42405d47b5bd5d4fbe64bc98a0ce94c28`  
		Last Modified: Mon, 13 Nov 2023 14:13:08 GMT  
		Size: 358.1 MB (358136145 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89732bc7504122601f40269fc9ddfb70982e633ea9caf641ae45736f2846b004`  
		Last Modified: Sat, 26 Jan 2019 16:40:00 GMT  
		Size: 39.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:508a0c06fd907ed3525f21b73947d06df372308521d9591355699ce6067341f0`  
		Last Modified: Mon, 13 Nov 2023 14:12:55 GMT  
		Size: 140.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1a11029889b246d5b608cc41cb4e51cda2008624f11b8e52b6f7bab80627abd`  
		Last Modified: Mon, 13 Nov 2023 14:12:55 GMT  
		Size: 418.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b5a0bef074930ce8aa8eed7a100c3dff21ca52c90be0d08d4967fb7679f1fa6`  
		Last Modified: Mon, 13 Nov 2023 14:12:56 GMT  
		Size: 5.1 KB (5131 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb855b63b4f1c9af94c5c7b47c3a5cbf185d6e4c45b123c7991523f03214e1f9`  
		Last Modified: Mon, 13 Nov 2023 14:12:56 GMT  
		Size: 418.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0aea2c9f546ed6f25ae4a87ad2c509177dab568784d807f9a88dbcdf20cb06ee`  
		Last Modified: Mon, 13 Nov 2023 14:12:56 GMT  
		Size: 208.2 KB (208246 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec2ef9eb599490a0191bfcc13211c08811cc304a1a584d9ff4e74a6aafe68fbd`  
		Last Modified: Mon, 13 Nov 2023 14:12:57 GMT  
		Size: 2.0 KB (2037 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kibana:8.11.1` - unknown; unknown

```console
$ docker pull kibana@sha256:aa982f96d1d4b3b62dda7b29dc967034a4adc74f4fb0e3370f5c106aa4d0403c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3466018 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:42f67f645b4afaafcb971c425b0aae861730fbc8c0e6ef1f055f570ef7b9e2f1`

```dockerfile
```

-	Layers:
	-	`sha256:38b75aa05e47bad5a04a235b0ac0cd3b0563d4573bb46417d468ce7abb549535`  
		Last Modified: Thu, 16 Nov 2023 01:20:49 GMT  
		Size: 3.5 MB (3457458 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fc424aac81f61f9d5c8c5b361387356c22900ca1e2b341a45c584e0232c0a5e4`  
		Last Modified: Thu, 16 Nov 2023 01:20:49 GMT  
		Size: 8.6 KB (8560 bytes)  
		MIME: application/vnd.in-toto+json
