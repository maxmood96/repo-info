<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `kibana`

-	[`kibana:7.17.9`](#kibana7179)
-	[`kibana:8.7.0`](#kibana870)

## `kibana:7.17.9`

```console
$ docker pull kibana@sha256:69f04843b05fb3cf26ec8c06cd36d560e0bca9ce41e6886c807d865b7ea618e9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `kibana:7.17.9` - linux; amd64

```console
$ docker pull kibana@sha256:aefb8ca90b82030e22037a957dee4bff9236eea235324375f19e8922eaa20502
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **329.2 MB (329196799 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c0059eed7da920704796ce2bb872e83155821f9a64fc634274d1e9f8cc23e22`
-	Entrypoint: `["\/bin\/tini","--"]`
-	Default Command: `["\/usr\/local\/bin\/kibana-docker"]`

```dockerfile
# Fri, 09 Dec 2022 01:20:21 GMT
ADD file:9d282119af0c42bc823c95b4192a3350cf2cad670622017356dd2e637762e425 in / 
# Fri, 09 Dec 2022 01:20:21 GMT
CMD ["bash"]
# Mon, 30 Jan 2023 12:43:38 GMT
EXPOSE map[5601/tcp:{}]
# Mon, 30 Jan 2023 12:43:38 GMT
RUN for iter in {1..10}; do       export DEBIAN_FRONTEND=noninteractive &&       apt-get update  &&       apt-get upgrade -y  &&       apt-get install -y --no-install-recommends        fontconfig fonts-liberation libnss3 libfontconfig1 ca-certificates curl &&       apt-get clean &&       rm -rf /var/lib/apt/lists/* && exit_code=0 && break || exit_code=$? && echo "apt-get error: retry $iter in 10s" &&       sleep 10;     done;     (exit $exit_code) # buildkit
# Mon, 30 Jan 2023 12:43:39 GMT
RUN set -e ;     TINI_BIN="" ;     case "$(arch)" in         aarch64)             TINI_BIN='tini-arm64' ;             ;;         x86_64)             TINI_BIN='tini-amd64' ;             ;;         *) echo >&2 "Unsupported architecture $(arch)" ; exit 1 ;;     esac ;   TINI_VERSION='v0.19.0' ;   curl --retry 8 -S -L -O "https://github.com/krallin/tini/releases/download/${TINI_VERSION}/${TINI_BIN}" ;   curl --retry 8 -S -L -O "https://github.com/krallin/tini/releases/download/${TINI_VERSION}/${TINI_BIN}.sha256sum" ;   sha256sum -c "${TINI_BIN}.sha256sum" ;   rm "${TINI_BIN}.sha256sum" ;   mv "${TINI_BIN}" /bin/tini ;   chmod +x /bin/tini # buildkit
# Mon, 30 Jan 2023 12:43:40 GMT
RUN mkdir /usr/share/fonts/local # buildkit
# Mon, 30 Jan 2023 12:43:40 GMT
RUN curl --retry 8 -S -L -o /usr/share/fonts/local/NotoSansCJK-Regular.ttc https://github.com/googlefonts/noto-cjk/raw/NotoSansV2.001/NotoSansCJK-Regular.ttc # buildkit
# Mon, 30 Jan 2023 12:43:41 GMT
RUN echo "5dcd1c336cc9344cb77c03a0cd8982ca8a7dc97d620fd6c9c434e02dcb1ceeb3  /usr/share/fonts/local/NotoSansCJK-Regular.ttc" | sha256sum -c - # buildkit
# Mon, 30 Jan 2023 12:43:41 GMT
RUN fc-cache -v # buildkit
# Mon, 30 Jan 2023 12:44:32 GMT
COPY /usr/share/kibana /usr/share/kibana # buildkit
# Mon, 30 Jan 2023 12:44:32 GMT
WORKDIR /usr/share/kibana
# Mon, 30 Jan 2023 12:44:33 GMT
RUN ln -s /usr/share/kibana /opt/kibana # buildkit
# Mon, 30 Jan 2023 12:44:33 GMT
ENV ELASTIC_CONTAINER=true
# Mon, 30 Jan 2023 12:44:33 GMT
ENV PATH=/usr/share/kibana/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 30 Jan 2023 12:44:33 GMT
COPY config/kibana.yml /usr/share/kibana/config/kibana.yml # buildkit
# Mon, 30 Jan 2023 12:44:33 GMT
COPY bin/kibana-docker /usr/local/bin/ # buildkit
# Mon, 30 Jan 2023 12:44:33 GMT
RUN chmod g+ws /usr/share/kibana &&     find /usr/share/kibana -gid 0 -and -not -perm /g+w -exec chmod g+w {} \; # buildkit
# Mon, 30 Jan 2023 12:44:34 GMT
RUN find / -xdev -perm -4000 -exec chmod u-s {} + # buildkit
# Mon, 30 Jan 2023 12:44:34 GMT
RUN groupadd --gid 1000 kibana &&     useradd --uid 1000 --gid 1000 -G 0       --home-dir /usr/share/kibana --no-create-home       kibana # buildkit
# Mon, 30 Jan 2023 12:44:34 GMT
LABEL org.label-schema.build-date=2023-01-30T12:17:55.756Z org.label-schema.license=Elastic License org.label-schema.name=Kibana org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/kibana org.label-schema.usage=https://www.elastic.co/guide/en/kibana/reference/index.html org.label-schema.vcs-ref=00b0b0440dbf6f8c542448473e020c99d352a0f5 org.label-schema.vcs-url=https://github.com/elastic/kibana org.label-schema.vendor=Elastic org.label-schema.version=7.17.9 org.opencontainers.image.created=2023-01-30T12:17:55.756Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/kibana/reference/index.html org.opencontainers.image.licenses=Elastic License org.opencontainers.image.revision=00b0b0440dbf6f8c542448473e020c99d352a0f5 org.opencontainers.image.source=https://github.com/elastic/kibana org.opencontainers.image.title=Kibana org.opencontainers.image.url=https://www.elastic.co/products/kibana org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=7.17.9
# Mon, 30 Jan 2023 12:44:34 GMT
ENTRYPOINT ["/bin/tini" "--"]
# Mon, 30 Jan 2023 12:44:34 GMT
CMD ["/usr/local/bin/kibana-docker"]
# Mon, 30 Jan 2023 12:44:34 GMT
USER kibana
```

-	Layers:
	-	`sha256:846c0b181fff0c667d9444f8378e8fcfa13116da8d308bf21673f7e4bea8d580`  
		Last Modified: Thu, 08 Dec 2022 13:18:11 GMT  
		Size: 28.6 MB (28576882 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:144df3972ed5731ddb73eedaa8175c38669f8733ffb422a4323513f0d44f71ba`  
		Last Modified: Tue, 07 Feb 2023 20:44:30 GMT  
		Size: 10.9 MB (10906819 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ee71c9917ce20f4dbee2249dea74ade95868679cfd52b5f03fa2840d5e30db3`  
		Last Modified: Tue, 07 Feb 2023 20:44:27 GMT  
		Size: 9.5 KB (9527 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8eb0c544b6b907f0514d9c683562908bca16da597f718e00213f669011b2cb2b`  
		Last Modified: Tue, 07 Feb 2023 20:44:26 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13fdf76384b609c053725de172048895872be3940fb183653f5a828b8c165dcc`  
		Last Modified: Tue, 07 Feb 2023 20:44:27 GMT  
		Size: 16.5 MB (16460475 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ed11a68cbb9ec5d6759be8fb4fc4c3c1cba9a5ae575222c87c8b16e7c706f61`  
		Last Modified: Tue, 07 Feb 2023 20:44:23 GMT  
		Size: 5.3 KB (5296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d90cf8802e3328f4006c3893cd1fe84ab5de0628bcc226d8aa8550f809903def`  
		Last Modified: Tue, 07 Feb 2023 20:45:14 GMT  
		Size: 273.0 MB (273040936 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:742662fee0f03cf5f5d8033ddea5645d2edf53a1e5bb4435c58d646a192af976`  
		Last Modified: Tue, 07 Feb 2023 20:44:23 GMT  
		Size: 133.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4cf74473cf818dbb8962a37a1dcb95e9c8a3f8fad10ae4b3b7b5fa5ebfa5cbb4`  
		Last Modified: Tue, 07 Feb 2023 20:44:23 GMT  
		Size: 395.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eae97ce5d6732c6a7bdc0163a67625da75a8aaf77ebf32edaf598f9e8a1494e3`  
		Last Modified: Tue, 07 Feb 2023 20:44:23 GMT  
		Size: 4.5 KB (4505 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6abdf7b4ef80863e971dc65d278754db5234e6a094aa9b0e3dcf5b336a9b07a4`  
		Last Modified: Tue, 07 Feb 2023 20:44:21 GMT  
		Size: 397.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81d01537b7d629fdbc3b6dc57a054b9aa96ee80ae82f5e033d8430266764403b`  
		Last Modified: Tue, 07 Feb 2023 20:44:21 GMT  
		Size: 189.4 KB (189391 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5f8c3eee3b1d20a9d5984f01a5f49bc0ddf13326997445a905fa0857f548a46`  
		Last Modified: Tue, 07 Feb 2023 20:44:21 GMT  
		Size: 1.8 KB (1819 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kibana:7.17.9` - linux; arm64 variant v8

```console
$ docker pull kibana@sha256:33a858d7b002ca0dc15e0f26ce18567c3ffbfe2c5829dd94b7bb42536df89ce5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **344.1 MB (344107968 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6d71855e558ed8d7ca1dfc89490143dcadd482df2ee70398863b18ef11fd85cf`
-	Entrypoint: `["\/bin\/tini","--"]`
-	Default Command: `["\/usr\/local\/bin\/kibana-docker"]`

```dockerfile
# Fri, 09 Dec 2022 01:46:50 GMT
ADD file:8cba976cb6ea226de769a768ee274e7679d34f923c93392f340680dc6696232e in / 
# Fri, 09 Dec 2022 01:46:50 GMT
CMD ["bash"]
# Mon, 30 Jan 2023 12:46:34 GMT
EXPOSE map[5601/tcp:{}]
# Mon, 30 Jan 2023 12:46:34 GMT
RUN for iter in {1..10}; do       export DEBIAN_FRONTEND=noninteractive &&       apt-get update  &&       apt-get upgrade -y  &&       apt-get install -y --no-install-recommends        fontconfig fonts-liberation libnss3 libfontconfig1 ca-certificates curl &&       apt-get clean &&       rm -rf /var/lib/apt/lists/* && exit_code=0 && break || exit_code=$? && echo "apt-get error: retry $iter in 10s" &&       sleep 10;     done;     (exit $exit_code) # buildkit
# Mon, 30 Jan 2023 12:46:36 GMT
RUN set -e ;     TINI_BIN="" ;     case "$(arch)" in         aarch64)             TINI_BIN='tini-arm64' ;             ;;         x86_64)             TINI_BIN='tini-amd64' ;             ;;         *) echo >&2 "Unsupported architecture $(arch)" ; exit 1 ;;     esac ;   TINI_VERSION='v0.19.0' ;   curl --retry 8 -S -L -O "https://github.com/krallin/tini/releases/download/${TINI_VERSION}/${TINI_BIN}" ;   curl --retry 8 -S -L -O "https://github.com/krallin/tini/releases/download/${TINI_VERSION}/${TINI_BIN}.sha256sum" ;   sha256sum -c "${TINI_BIN}.sha256sum" ;   rm "${TINI_BIN}.sha256sum" ;   mv "${TINI_BIN}" /bin/tini ;   chmod +x /bin/tini # buildkit
# Mon, 30 Jan 2023 12:46:36 GMT
RUN mkdir /usr/share/fonts/local # buildkit
# Mon, 30 Jan 2023 12:46:39 GMT
RUN curl --retry 8 -S -L -o /usr/share/fonts/local/NotoSansCJK-Regular.ttc https://github.com/googlefonts/noto-cjk/raw/NotoSansV2.001/NotoSansCJK-Regular.ttc # buildkit
# Mon, 30 Jan 2023 12:46:39 GMT
RUN echo "5dcd1c336cc9344cb77c03a0cd8982ca8a7dc97d620fd6c9c434e02dcb1ceeb3  /usr/share/fonts/local/NotoSansCJK-Regular.ttc" | sha256sum -c - # buildkit
# Mon, 30 Jan 2023 12:46:40 GMT
RUN fc-cache -v # buildkit
# Mon, 30 Jan 2023 12:47:30 GMT
COPY /usr/share/kibana /usr/share/kibana # buildkit
# Mon, 30 Jan 2023 12:47:30 GMT
WORKDIR /usr/share/kibana
# Mon, 30 Jan 2023 12:47:30 GMT
RUN ln -s /usr/share/kibana /opt/kibana # buildkit
# Mon, 30 Jan 2023 12:47:30 GMT
ENV ELASTIC_CONTAINER=true
# Mon, 30 Jan 2023 12:47:30 GMT
ENV PATH=/usr/share/kibana/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 30 Jan 2023 12:47:31 GMT
COPY config/kibana.yml /usr/share/kibana/config/kibana.yml # buildkit
# Mon, 30 Jan 2023 12:47:31 GMT
COPY bin/kibana-docker /usr/local/bin/ # buildkit
# Mon, 30 Jan 2023 12:47:31 GMT
RUN chmod g+ws /usr/share/kibana &&     find /usr/share/kibana -gid 0 -and -not -perm /g+w -exec chmod g+w {} \; # buildkit
# Mon, 30 Jan 2023 12:47:32 GMT
RUN find / -xdev -perm -4000 -exec chmod u-s {} + # buildkit
# Mon, 30 Jan 2023 12:47:33 GMT
RUN groupadd --gid 1000 kibana &&     useradd --uid 1000 --gid 1000 -G 0       --home-dir /usr/share/kibana --no-create-home       kibana # buildkit
# Mon, 30 Jan 2023 12:47:33 GMT
LABEL org.label-schema.build-date=2023-01-30T12:17:55.756Z org.label-schema.license=Elastic License org.label-schema.name=Kibana org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/kibana org.label-schema.usage=https://www.elastic.co/guide/en/kibana/reference/index.html org.label-schema.vcs-ref=00b0b0440dbf6f8c542448473e020c99d352a0f5 org.label-schema.vcs-url=https://github.com/elastic/kibana org.label-schema.vendor=Elastic org.label-schema.version=7.17.9 org.opencontainers.image.created=2023-01-30T12:17:55.756Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/kibana/reference/index.html org.opencontainers.image.licenses=Elastic License org.opencontainers.image.revision=00b0b0440dbf6f8c542448473e020c99d352a0f5 org.opencontainers.image.source=https://github.com/elastic/kibana org.opencontainers.image.title=Kibana org.opencontainers.image.url=https://www.elastic.co/products/kibana org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=7.17.9
# Mon, 30 Jan 2023 12:47:33 GMT
ENTRYPOINT ["/bin/tini" "--"]
# Mon, 30 Jan 2023 12:47:33 GMT
CMD ["/usr/local/bin/kibana-docker"]
# Mon, 30 Jan 2023 12:47:33 GMT
USER kibana
```

-	Layers:
	-	`sha256:f04b4bbe15805316c8fda79beedd3b77e6b1ffcd0acf81226c3089e63f6bffeb`  
		Last Modified: Thu, 08 Dec 2022 15:28:02 GMT  
		Size: 27.2 MB (27193168 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aacab5eee6d97ad288bcac89d5d41ce8543a839d2adec5064b5b9067644aef29`  
		Last Modified: Tue, 07 Feb 2023 22:57:17 GMT  
		Size: 10.8 MB (10768381 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ebdd3887fd1a28b41bbe597dbe690527176cb44a98c34976352a82c164536bd`  
		Last Modified: Tue, 07 Feb 2023 22:57:15 GMT  
		Size: 9.1 KB (9099 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c64a8b693a1a9f7e25477637e4a119cc9a75168f326e60c228b4da27e0f17332`  
		Last Modified: Tue, 07 Feb 2023 22:57:14 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d17e555a88d6e5d0b72515ee9c0b3bc44c4787e9d64a0307d457e7bab620e20`  
		Last Modified: Tue, 07 Feb 2023 22:57:15 GMT  
		Size: 16.5 MB (16460476 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e70368d00a87c7cd3a307fedd180221ac5425754e1b33290ad59dcc1c62c118`  
		Last Modified: Tue, 07 Feb 2023 22:57:14 GMT  
		Size: 5.3 KB (5290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:027bfdb93caa1ced65cc512ae065a682b899bf3a9072c327d63a2d18955bef2e`  
		Last Modified: Tue, 07 Feb 2023 22:57:41 GMT  
		Size: 289.5 MB (289480686 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb89142f2d0761e51559b02dc38afb0ba5a8873b3f8b163f4930555a05ed6545`  
		Last Modified: Tue, 07 Feb 2023 22:57:13 GMT  
		Size: 133.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f002453150a97e2204515ee75923ab0cecdff8cb3205978a163ae0c86ac2ff6`  
		Last Modified: Tue, 07 Feb 2023 22:57:11 GMT  
		Size: 394.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2528ab2b7d241945a7a83f39ec84b06482e381b3a71d6302c9100be299ae700`  
		Last Modified: Tue, 07 Feb 2023 22:57:12 GMT  
		Size: 4.5 KB (4506 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d130895ed20fd9b4d2818be86b11b882d8efd0a721625edc022ad38cb5087dd2`  
		Last Modified: Tue, 07 Feb 2023 22:57:11 GMT  
		Size: 397.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63fa2f4692370f3a8864a28f8476e0da22cd21b15b61ff73541cc8b5f09de4c7`  
		Last Modified: Tue, 07 Feb 2023 22:57:12 GMT  
		Size: 183.4 KB (183393 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f22b75c18e5f9b7e0edb152d3537697fa37f4d35e069b4b4e87844bbfd8c527`  
		Last Modified: Tue, 07 Feb 2023 22:57:11 GMT  
		Size: 1.8 KB (1821 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kibana:8.7.0`

```console
$ docker pull kibana@sha256:eb37f58646a901dc7727cf448cae36daaefaba79de33b5058dab79aa4c04aefb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 0
