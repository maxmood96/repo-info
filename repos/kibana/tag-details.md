<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `kibana`

-	[`kibana:7.17.28`](#kibana71728)
-	[`kibana:8.17.10`](#kibana81710)
-	[`kibana:8.18.5`](#kibana8185)
-	[`kibana:8.19.2`](#kibana8192)
-	[`kibana:9.0.5`](#kibana905)
-	[`kibana:9.1.2`](#kibana912)

## `kibana:7.17.28`

```console
$ docker pull kibana@sha256:d079a482ff41300e596ca340bd8c75ad9258f5b77c84f711f640fdb8f38291e4
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `kibana:7.17.28` - linux; amd64

```console
$ docker pull kibana@sha256:93a05ff9136e38f0f39e41ebf437562cd02343dc9b15757ab07f5191d76fd5d3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **353.9 MB (353911017 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec7680dc6a3011aef284630f6f9060a4aba6f0c6c86b8d42d6858a4f573c6d0b`
-	Entrypoint: `["\/bin\/tini","--"]`
-	Default Command: `["\/usr\/local\/bin\/kibana-docker"]`

```dockerfile
# Thu, 31 Jul 2025 10:41:27 GMT
ARG RELEASE
# Thu, 31 Jul 2025 10:41:27 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 31 Jul 2025 10:41:27 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 31 Jul 2025 10:41:27 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 31 Jul 2025 10:41:27 GMT
ADD file:e67907c77897d27192314f6c4fa0112b6f7dce3e127500516535cc50fe736c92 in / 
# Thu, 31 Jul 2025 10:41:27 GMT
CMD ["/bin/bash"]
# Thu, 31 Jul 2025 10:41:27 GMT
EXPOSE map[5601/tcp:{}]
# Thu, 31 Jul 2025 10:41:27 GMT
RUN for iter in {1..10}; do       export DEBIAN_FRONTEND=noninteractive &&       apt-get update  &&       apt-get upgrade -y  &&       apt-get install -y --no-install-recommends        fontconfig fonts-liberation libnss3 libfontconfig1 ca-certificates curl &&       apt-get clean &&       rm -rf /var/lib/apt/lists/* && exit_code=0 && break || exit_code=$? && echo "apt-get error: retry $iter in 10s" &&       sleep 10;     done;     (exit $exit_code) # buildkit
# Thu, 31 Jul 2025 10:41:27 GMT
RUN set -e ;     TINI_BIN="" ;     case "$(arch)" in         aarch64)             TINI_BIN='tini-arm64' ;             ;;         x86_64)             TINI_BIN='tini-amd64' ;             ;;         *) echo >&2 "Unsupported architecture $(arch)" ; exit 1 ;;     esac ;   TINI_VERSION='v0.19.0' ;   curl --retry 8 -S -L -O "https://github.com/krallin/tini/releases/download/${TINI_VERSION}/${TINI_BIN}" ;   curl --retry 8 -S -L -O "https://github.com/krallin/tini/releases/download/${TINI_VERSION}/${TINI_BIN}.sha256sum" ;   sha256sum -c "${TINI_BIN}.sha256sum" ;   rm "${TINI_BIN}.sha256sum" ;   mv "${TINI_BIN}" /bin/tini ;   chmod +x /bin/tini # buildkit
# Thu, 31 Jul 2025 10:41:27 GMT
RUN mkdir /usr/share/fonts/local # buildkit
# Thu, 31 Jul 2025 10:41:27 GMT
RUN curl --retry 8 -S -L -o /usr/share/fonts/local/NotoSansCJK-Regular.ttc https://github.com/googlefonts/noto-cjk/raw/NotoSansV2.001/NotoSansCJK-Regular.ttc # buildkit
# Thu, 31 Jul 2025 10:41:27 GMT
RUN echo "5dcd1c336cc9344cb77c03a0cd8982ca8a7dc97d620fd6c9c434e02dcb1ceeb3  /usr/share/fonts/local/NotoSansCJK-Regular.ttc" | sha256sum -c - # buildkit
# Thu, 31 Jul 2025 10:41:27 GMT
RUN fc-cache -v # buildkit
# Thu, 31 Jul 2025 10:41:27 GMT
COPY --chown=1000:0 /usr/share/kibana /usr/share/kibana # buildkit
# Thu, 31 Jul 2025 10:41:27 GMT
WORKDIR /usr/share/kibana
# Thu, 31 Jul 2025 10:41:27 GMT
RUN ln -s /usr/share/kibana /opt/kibana # buildkit
# Thu, 31 Jul 2025 10:41:27 GMT
ENV ELASTIC_CONTAINER=true
# Thu, 31 Jul 2025 10:41:27 GMT
ENV PATH=/usr/share/kibana/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 31 Jul 2025 10:41:27 GMT
COPY --chown=1000:0 config/kibana.yml /usr/share/kibana/config/kibana.yml # buildkit
# Thu, 31 Jul 2025 10:41:27 GMT
COPY bin/kibana-docker /usr/local/bin/ # buildkit
# Thu, 31 Jul 2025 10:41:27 GMT
RUN chmod g+ws /usr/share/kibana &&     find /usr/share/kibana -gid 0 -and -not -perm /g+w -exec chmod g+w {} \; # buildkit
# Thu, 31 Jul 2025 10:41:27 GMT
RUN find / -xdev -perm -4000 -exec chmod u-s {} + # buildkit
# Thu, 31 Jul 2025 10:41:27 GMT
RUN userdel -r ubuntu && groupadd --gid 1000 kibana &&     useradd --uid 1000 --gid 1000 -G 0       --home-dir /usr/share/kibana --no-create-home       kibana # buildkit
# Thu, 31 Jul 2025 10:41:27 GMT
LABEL org.label-schema.build-date=2025-06-18T11:10:23.947Z org.label-schema.license=Elastic License org.label-schema.name=Kibana org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/kibana org.label-schema.usage=https://www.elastic.co/guide/en/kibana/reference/index.html org.label-schema.vcs-ref=f6e2f2e44cc0a6a11435f1b6350f735e23bef4b4 org.label-schema.vcs-url=https://github.com/elastic/kibana org.label-schema.vendor=Elastic org.label-schema.version=7.17.29 org.opencontainers.image.created=2025-06-18T11:10:23.947Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/kibana/reference/index.html org.opencontainers.image.licenses=Elastic License org.opencontainers.image.revision=f6e2f2e44cc0a6a11435f1b6350f735e23bef4b4 org.opencontainers.image.source=https://github.com/elastic/kibana org.opencontainers.image.title=Kibana org.opencontainers.image.url=https://www.elastic.co/products/kibana org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=7.17.29
# Thu, 31 Jul 2025 10:41:27 GMT
ENTRYPOINT ["/bin/tini" "--"]
# Thu, 31 Jul 2025 10:41:27 GMT
CMD ["/usr/local/bin/kibana-docker"]
# Thu, 31 Jul 2025 10:41:27 GMT
USER kibana
```

-	Layers:
	-	`sha256:76249c7cd50397d2e8c06a75106723d057deaba0ffbc7f4af1bb02bcf71d81cf`  
		Last Modified: Tue, 19 Aug 2025 17:39:10 GMT  
		Size: 29.7 MB (29723064 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51230c45091a12df86d5e8628d68f815e6bc9dfa66f222440195c69d3ec14229`  
		Last Modified: Tue, 02 Sep 2025 00:30:15 GMT  
		Size: 9.4 MB (9431862 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8021ed2684e321da45dbb5db24ab16a732b15a8f9c235f8b557dc9b0f872c4c8`  
		Last Modified: Tue, 02 Sep 2025 00:30:15 GMT  
		Size: 9.5 KB (9526 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57c21f509b2e348e536bf6df286b06275ee35853dc2aab1cf14c719036dc9e53`  
		Last Modified: Tue, 02 Sep 2025 00:30:15 GMT  
		Size: 161.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60429a247d383196ec1f7f1de3f4c2705630c1b35b3b1622ede409a0d36a39a8`  
		Last Modified: Tue, 02 Sep 2025 00:30:18 GMT  
		Size: 16.5 MB (16460488 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1535ff005d0c5a7457dddbf6b18ff14532e1333dda4e19786116e2451be8ce59`  
		Last Modified: Tue, 02 Sep 2025 00:30:15 GMT  
		Size: 5.2 KB (5244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4519322c62f5be2911a15a81c10b6d25e26b2243dd415ec85beb28d118d3bf9`  
		Last Modified: Tue, 02 Sep 2025 02:13:57 GMT  
		Size: 298.1 MB (298112497 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66cc9616306d70d2015e8198297c2950e727113bdaf8af176b735f90c502e786`  
		Last Modified: Tue, 02 Sep 2025 00:30:16 GMT  
		Size: 130.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:776e559f0a8ac75b7c79e87ab99ab7c8f6d0e5f1894c4e5b97157986a4bf5631`  
		Last Modified: Tue, 02 Sep 2025 00:30:15 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe23521436e303cff387d635b5a2333d56c283adf60a3ca9eab6a87de3505444`  
		Last Modified: Tue, 02 Sep 2025 00:30:16 GMT  
		Size: 4.5 KB (4505 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:056871ad96eeeb58ac2436caf172840cfc7ead46420b73714edd886de148bdf9`  
		Last Modified: Tue, 02 Sep 2025 00:30:16 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b3c3196dae94abd2168a257d97fb98ef26847e281d88f2eff42cc4089b0c334`  
		Last Modified: Tue, 02 Sep 2025 00:30:16 GMT  
		Size: 161.5 KB (161458 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04993a920960e5c000564772ce039e747dbb9fe107b6dcf02918e71aac53046d`  
		Last Modified: Tue, 02 Sep 2025 00:30:16 GMT  
		Size: 1.2 KB (1224 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kibana:7.17.28` - unknown; unknown

```console
$ docker pull kibana@sha256:78abca99355a47ad2788f0c6fa6a96d0221c4f052970e0d0e180f179b381e957
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3551384 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1619969ea7f7dd8744581dc50f432aa21452f4d5a2c7e8edf67c136699b232d7`

```dockerfile
```

-	Layers:
	-	`sha256:5bb37931117743cae8b7308fc8c6585a5b96fbd40b75a1f324b58e312a7ddb49`  
		Last Modified: Tue, 02 Sep 2025 02:11:18 GMT  
		Size: 3.5 MB (3506830 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:04cba3f68b9fe90817b1bd9f33affa6040e501ccc26945d3540167c596444ebb`  
		Last Modified: Tue, 02 Sep 2025 02:11:19 GMT  
		Size: 44.6 KB (44554 bytes)  
		MIME: application/vnd.in-toto+json

### `kibana:7.17.28` - linux; arm64 variant v8

```console
$ docker pull kibana@sha256:881a636d46c2ec1ee3afd7402a388183f80c26ba97d96541b6cf181176b3002c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **366.2 MB (366174215 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4860e9fd2dcf13538914e5ca2a024d3e3dc857a7dae562a8a1b9d9381ee22d57`
-	Entrypoint: `["\/bin\/tini","--"]`
-	Default Command: `["\/usr\/local\/bin\/kibana-docker"]`

```dockerfile
# Wed, 30 Jul 2025 07:00:50 GMT
ARG RELEASE
# Wed, 30 Jul 2025 07:00:50 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 30 Jul 2025 07:00:50 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 30 Jul 2025 07:00:50 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 30 Jul 2025 07:00:53 GMT
ADD file:e189629238f69759e9c6cb1cac039ece646eeecb640e5eb670e5cf92543b46fb in / 
# Wed, 30 Jul 2025 07:00:53 GMT
CMD ["/bin/bash"]
# Thu, 31 Jul 2025 10:41:27 GMT
EXPOSE map[5601/tcp:{}]
# Thu, 31 Jul 2025 10:41:27 GMT
RUN for iter in {1..10}; do       export DEBIAN_FRONTEND=noninteractive &&       apt-get update  &&       apt-get upgrade -y  &&       apt-get install -y --no-install-recommends        fontconfig fonts-liberation libnss3 libfontconfig1 ca-certificates curl &&       apt-get clean &&       rm -rf /var/lib/apt/lists/* && exit_code=0 && break || exit_code=$? && echo "apt-get error: retry $iter in 10s" &&       sleep 10;     done;     (exit $exit_code) # buildkit
# Thu, 31 Jul 2025 10:41:27 GMT
RUN set -e ;     TINI_BIN="" ;     case "$(arch)" in         aarch64)             TINI_BIN='tini-arm64' ;             ;;         x86_64)             TINI_BIN='tini-amd64' ;             ;;         *) echo >&2 "Unsupported architecture $(arch)" ; exit 1 ;;     esac ;   TINI_VERSION='v0.19.0' ;   curl --retry 8 -S -L -O "https://github.com/krallin/tini/releases/download/${TINI_VERSION}/${TINI_BIN}" ;   curl --retry 8 -S -L -O "https://github.com/krallin/tini/releases/download/${TINI_VERSION}/${TINI_BIN}.sha256sum" ;   sha256sum -c "${TINI_BIN}.sha256sum" ;   rm "${TINI_BIN}.sha256sum" ;   mv "${TINI_BIN}" /bin/tini ;   chmod +x /bin/tini # buildkit
# Thu, 31 Jul 2025 10:41:27 GMT
RUN mkdir /usr/share/fonts/local # buildkit
# Thu, 31 Jul 2025 10:41:27 GMT
RUN curl --retry 8 -S -L -o /usr/share/fonts/local/NotoSansCJK-Regular.ttc https://github.com/googlefonts/noto-cjk/raw/NotoSansV2.001/NotoSansCJK-Regular.ttc # buildkit
# Thu, 31 Jul 2025 10:41:27 GMT
RUN echo "5dcd1c336cc9344cb77c03a0cd8982ca8a7dc97d620fd6c9c434e02dcb1ceeb3  /usr/share/fonts/local/NotoSansCJK-Regular.ttc" | sha256sum -c - # buildkit
# Thu, 31 Jul 2025 10:41:27 GMT
RUN fc-cache -v # buildkit
# Thu, 31 Jul 2025 10:41:27 GMT
COPY --chown=1000:0 /usr/share/kibana /usr/share/kibana # buildkit
# Thu, 31 Jul 2025 10:41:27 GMT
WORKDIR /usr/share/kibana
# Thu, 31 Jul 2025 10:41:27 GMT
RUN ln -s /usr/share/kibana /opt/kibana # buildkit
# Thu, 31 Jul 2025 10:41:27 GMT
ENV ELASTIC_CONTAINER=true
# Thu, 31 Jul 2025 10:41:27 GMT
ENV PATH=/usr/share/kibana/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 31 Jul 2025 10:41:27 GMT
COPY --chown=1000:0 config/kibana.yml /usr/share/kibana/config/kibana.yml # buildkit
# Thu, 31 Jul 2025 10:41:27 GMT
COPY bin/kibana-docker /usr/local/bin/ # buildkit
# Thu, 31 Jul 2025 10:41:27 GMT
RUN chmod g+ws /usr/share/kibana &&     find /usr/share/kibana -gid 0 -and -not -perm /g+w -exec chmod g+w {} \; # buildkit
# Thu, 31 Jul 2025 10:41:27 GMT
RUN find / -xdev -perm -4000 -exec chmod u-s {} + # buildkit
# Thu, 31 Jul 2025 10:41:27 GMT
RUN userdel -r ubuntu && groupadd --gid 1000 kibana &&     useradd --uid 1000 --gid 1000 -G 0       --home-dir /usr/share/kibana --no-create-home       kibana # buildkit
# Thu, 31 Jul 2025 10:41:27 GMT
LABEL org.label-schema.build-date=2025-06-18T11:10:23.947Z org.label-schema.license=Elastic License org.label-schema.name=Kibana org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/kibana org.label-schema.usage=https://www.elastic.co/guide/en/kibana/reference/index.html org.label-schema.vcs-ref=f6e2f2e44cc0a6a11435f1b6350f735e23bef4b4 org.label-schema.vcs-url=https://github.com/elastic/kibana org.label-schema.vendor=Elastic org.label-schema.version=7.17.29 org.opencontainers.image.created=2025-06-18T11:10:23.947Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/kibana/reference/index.html org.opencontainers.image.licenses=Elastic License org.opencontainers.image.revision=f6e2f2e44cc0a6a11435f1b6350f735e23bef4b4 org.opencontainers.image.source=https://github.com/elastic/kibana org.opencontainers.image.title=Kibana org.opencontainers.image.url=https://www.elastic.co/products/kibana org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=7.17.29
# Thu, 31 Jul 2025 10:41:27 GMT
ENTRYPOINT ["/bin/tini" "--"]
# Thu, 31 Jul 2025 10:41:27 GMT
CMD ["/usr/local/bin/kibana-docker"]
# Thu, 31 Jul 2025 10:41:27 GMT
USER kibana
```

-	Layers:
	-	`sha256:49a8ca9a328e179fe07d40f7f2fd5fb2860b5c45463c288b64f05be521173d2e`  
		Last Modified: Wed, 30 Jul 2025 10:35:20 GMT  
		Size: 28.9 MB (28860377 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0022fcadab11aac508c44fe2564d57dba4958e2459fe3601997f0b0e1fbe4f3`  
		Last Modified: Tue, 12 Aug 2025 19:32:47 GMT  
		Size: 9.5 MB (9526043 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73251f8340ddcf2b3ee116db30533c21e52164484a360324511d647f75c8462a`  
		Last Modified: Tue, 12 Aug 2025 19:32:43 GMT  
		Size: 9.1 KB (9098 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f1127a44491b4f226e5189c6a31536b1c79650020e7e30aaf8e1e7940ce5bce`  
		Last Modified: Tue, 12 Aug 2025 19:32:38 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5303fdaa61e274cddd3bca2ae09c8443327b5e364a50f33be0f0d7d177ad9383`  
		Last Modified: Tue, 12 Aug 2025 19:32:42 GMT  
		Size: 16.5 MB (16460486 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a401df8c2556e38352092346e4f7738d8d30a4b5a39fcf58b9de74b60e523549`  
		Last Modified: Tue, 12 Aug 2025 19:32:39 GMT  
		Size: 5.2 KB (5245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5aa9124afe2c12964cca9df55086cf36aa0106b3c4d8105987e1c2805696e59`  
		Last Modified: Tue, 12 Aug 2025 20:15:41 GMT  
		Size: 311.1 MB (311148084 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:293edb58c34bef9bcf7d31aee314e7dc1bc0d1c893f8b1e0896cccb82c1089bb`  
		Last Modified: Tue, 12 Aug 2025 19:32:39 GMT  
		Size: 132.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ad04a1ef7d1a97f3569b2e80f82de9e039cdf2efb90146ecb3605e5a040f1e0`  
		Last Modified: Tue, 12 Aug 2025 19:32:40 GMT  
		Size: 400.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:498cd5a3324096ff5866a223ab1bafbad237d7bcbef088c43cbf3b1ce2ee263c`  
		Last Modified: Tue, 12 Aug 2025 19:32:38 GMT  
		Size: 4.5 KB (4505 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79c051d9f38c8d59a8b381f1e4308ff8d1059b26c5769e5cbbe8f6be38b378cf`  
		Last Modified: Tue, 12 Aug 2025 19:32:39 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee1d3947101d0f169cba7fbe369d2a56ff46edfa53d0f9f94228e3ec825f3e75`  
		Last Modified: Tue, 12 Aug 2025 19:32:39 GMT  
		Size: 158.0 KB (157996 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22f069672ef6242bc544c55162d3e17675d724b3c420085b7efe865229c7c400`  
		Last Modified: Tue, 12 Aug 2025 19:32:40 GMT  
		Size: 1.2 KB (1223 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kibana:7.17.28` - unknown; unknown

```console
$ docker pull kibana@sha256:30ebceca5baf6355650c39e28aca0d8830c92e15add5920b87c4f63ba218ab27
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3552726 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec2347078ee9652d86809bee5427a1d2706268b6008df0005e854eb5e98550b9`

```dockerfile
```

-	Layers:
	-	`sha256:737a4a6267fa88409d9c08f1955981d0c6188067791a83e5a35cb9b02ebc1f73`  
		Last Modified: Tue, 12 Aug 2025 20:11:29 GMT  
		Size: 3.5 MB (3507894 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:133cdcbb0ac57251fa0735b1b06fe9d1ede8302c778949c66d1fff3a47e2035d`  
		Last Modified: Tue, 12 Aug 2025 20:11:30 GMT  
		Size: 44.8 KB (44832 bytes)  
		MIME: application/vnd.in-toto+json

## `kibana:8.17.10`

```console
$ docker pull kibana@sha256:1b8bf17d749494aeec0fb43d86229e63515e9cfc9c8d542cf309680ed49cbc5f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `kibana:8.17.10` - linux; amd64

```console
$ docker pull kibana@sha256:76e225a6fb855cfc84697d25479fe2f62d8d59022169eb18d1f162131906b2a1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **403.3 MB (403301151 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a66eea01510671f794da8ded4dcb1a5804876e9d56e6c78e2b142f4492118732`
-	Entrypoint: `["\/bin\/tini","--"]`
-	Default Command: `["\/usr\/local\/bin\/kibana-docker"]`

```dockerfile
# Tue, 12 Aug 2025 08:18:47 GMT
ARG RELEASE
# Tue, 12 Aug 2025 08:18:47 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 12 Aug 2025 08:18:47 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 12 Aug 2025 08:18:47 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 12 Aug 2025 08:18:47 GMT
ADD file:e67907c77897d27192314f6c4fa0112b6f7dce3e127500516535cc50fe736c92 in / 
# Tue, 12 Aug 2025 08:18:47 GMT
CMD ["/bin/bash"]
# Tue, 12 Aug 2025 08:18:47 GMT
EXPOSE map[5601/tcp:{}]
# Tue, 12 Aug 2025 08:18:47 GMT
RUN for iter in {1..10}; do       export DEBIAN_FRONTEND=noninteractive &&       apt-get update  &&       apt-get upgrade -y  &&       apt-get install -y --no-install-recommends       fontconfig fonts-liberation libnss3 curl ca-certificates &&       apt-get clean &&       rm -rf /var/lib/apt/lists/* && exit_code=0 && break || exit_code=$? && echo "apt-get error: retry $iter in 10s" &&       sleep 10;     done;     (exit $exit_code) # buildkit
# Tue, 12 Aug 2025 08:18:47 GMT
COPY --chown=1000:0 /usr/share/kibana /usr/share/kibana # buildkit
# Tue, 12 Aug 2025 08:18:47 GMT
COPY --chown=0:0 /bin/tini /bin/tini # buildkit
# Tue, 12 Aug 2025 08:18:47 GMT
COPY --chown=0:0 /usr/share/fonts/local/NotoSansCJK-Regular.ttc /usr/share/fonts/local/NotoSansCJK-Regular.ttc # buildkit
# Tue, 12 Aug 2025 08:18:47 GMT
RUN fc-cache -v # buildkit
# Tue, 12 Aug 2025 08:18:47 GMT
WORKDIR /usr/share/kibana
# Tue, 12 Aug 2025 08:18:47 GMT
RUN ln -s /usr/share/kibana /opt/kibana # buildkit
# Tue, 12 Aug 2025 08:18:47 GMT
ENV ELASTIC_CONTAINER=true
# Tue, 12 Aug 2025 08:18:47 GMT
ENV PATH=/usr/share/kibana/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 Aug 2025 08:18:47 GMT
COPY --chown=1000:0 config/kibana.yml /usr/share/kibana/config/kibana.yml # buildkit
# Tue, 12 Aug 2025 08:18:47 GMT
COPY bin/kibana-docker /usr/local/bin/ # buildkit
# Tue, 12 Aug 2025 08:18:47 GMT
RUN chmod g+ws /usr/share/kibana &&     find /usr/share/kibana -gid 0 -and -not -perm /g+w -exec chmod g+w {} \; # buildkit
# Tue, 12 Aug 2025 08:18:47 GMT
RUN find / -xdev -perm -4000 -exec chmod u-s {} + # buildkit
# Tue, 12 Aug 2025 08:18:47 GMT
RUN userdel -r ubuntu && groupadd --gid 1000 kibana &&     useradd --uid 1000 --gid 1000 -G 0       --home-dir /usr/share/kibana --no-create-home       kibana # buildkit
# Tue, 12 Aug 2025 08:18:47 GMT
LABEL org.label-schema.build-date=2025-08-07T20:18:34.689Z org.label-schema.license=Elastic License org.label-schema.name=Kibana org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/kibana org.label-schema.usage=https://www.elastic.co/guide/en/kibana/reference/index.html org.label-schema.vcs-ref=bbd44b7913a0eec99d54d68722f751de92ebe1ce org.label-schema.vcs-url=https://github.com/elastic/kibana org.label-schema.vendor=Elastic org.label-schema.version=8.17.10 org.opencontainers.image.created=2025-08-07T20:18:34.689Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/kibana/reference/index.html org.opencontainers.image.licenses=Elastic License org.opencontainers.image.revision=bbd44b7913a0eec99d54d68722f751de92ebe1ce org.opencontainers.image.source=https://github.com/elastic/kibana org.opencontainers.image.title=Kibana org.opencontainers.image.url=https://www.elastic.co/products/kibana org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=8.17.10
# Tue, 12 Aug 2025 08:18:47 GMT
ENTRYPOINT ["/bin/tini" "--"]
# Tue, 12 Aug 2025 08:18:47 GMT
CMD ["/usr/local/bin/kibana-docker"]
# Tue, 12 Aug 2025 08:18:47 GMT
USER 1000
```

-	Layers:
	-	`sha256:76249c7cd50397d2e8c06a75106723d057deaba0ffbc7f4af1bb02bcf71d81cf`  
		Last Modified: Tue, 19 Aug 2025 17:39:10 GMT  
		Size: 29.7 MB (29723064 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:024b295d945e78c2eec382a63b6c2f1b543315ee5630fa05d4e74debd2ae0854`  
		Last Modified: Tue, 02 Sep 2025 01:45:11 GMT  
		Size: 9.4 MB (9431813 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a790d368a9b54f45b81c8ad107997fe77c057775715d0127a11f929618f3027d`  
		Last Modified: Tue, 02 Sep 2025 02:16:06 GMT  
		Size: 347.5 MB (347502642 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93b8581cd2b7629f4472a5cc61dfc7fec08927e2190d1d2ee1ae7084b667a920`  
		Last Modified: Mon, 01 Sep 2025 23:40:56 GMT  
		Size: 9.5 KB (9528 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fde7799eb7587c3f2c2f3db86a3b528180f8f7bafd5f80ef32062b10eef6082d`  
		Last Modified: Mon, 01 Sep 2025 23:40:57 GMT  
		Size: 16.5 MB (16460491 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef96d16cfda78456f389f37caa55a16d91ec41ea711b4e5dcb56970e6c73b085`  
		Last Modified: Mon, 01 Sep 2025 23:40:57 GMT  
		Size: 5.2 KB (5241 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85dc941c7905aebd7542c5ddd05194c6e69bbe80d5d4d38a745e32c1e9495052`  
		Last Modified: Mon, 01 Sep 2025 23:40:56 GMT  
		Size: 130.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b5d3efa714cafd32377ff36e5d432fddac75e1743d3ec697e7b4875e51f10d4`  
		Last Modified: Mon, 01 Sep 2025 23:40:56 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3041bbfe4b92c73466bd75e4652816b3acf1432e81d925e0caeb6fbd9cc565d9`  
		Last Modified: Mon, 01 Sep 2025 23:40:56 GMT  
		Size: 4.7 KB (4730 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd1c025878e3d66f16b052601b68e2b5e87e08541b513ec74de6c7d40b7640a3`  
		Last Modified: Mon, 01 Sep 2025 23:40:57 GMT  
		Size: 400.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b16340f28589c78931c4441720efb0bb578c1760c7a33a00f8fe707720dc5d7b`  
		Last Modified: Mon, 01 Sep 2025 23:40:56 GMT  
		Size: 161.5 KB (161459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e97b4decfd2b9f96a89fb57e8dc0b5d955edf7cca5624f868fb71364b43af1a6`  
		Last Modified: Mon, 01 Sep 2025 23:40:56 GMT  
		Size: 1.2 KB (1224 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kibana:8.17.10` - unknown; unknown

```console
$ docker pull kibana@sha256:8ff3fa6dc9a1c04885c46fb316790d28846b8a2fad43e4aa19c3a1d7da01ff4a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4560869 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:963529b5e7827ce8223520bdcc7ffe471d109c855c59f68bf96b764b2730eeeb`

```dockerfile
```

-	Layers:
	-	`sha256:f46ee49ba8f3f456c84ec98ca549b2a38eff49eebfe51d5294c7273777661e84`  
		Last Modified: Tue, 02 Sep 2025 02:11:24 GMT  
		Size: 4.5 MB (4520136 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ac778db419d5f09f2268fc7ecf1a368ac45b10a88ff31b79c22b803cd776c85b`  
		Last Modified: Tue, 02 Sep 2025 02:11:25 GMT  
		Size: 40.7 KB (40733 bytes)  
		MIME: application/vnd.in-toto+json

### `kibana:8.17.10` - linux; arm64 variant v8

```console
$ docker pull kibana@sha256:7acfa3b707f2b64f9b9fd0e7cdd4a0421ef864e343dce1f7453668455e4c0827
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **415.6 MB (415577885 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c4bc8c38600bb09844c45b14e9b995421aa186ff8374101a1c1449c42af5be23`
-	Entrypoint: `["\/bin\/tini","--"]`
-	Default Command: `["\/usr\/local\/bin\/kibana-docker"]`

```dockerfile
# Wed, 30 Jul 2025 07:00:50 GMT
ARG RELEASE
# Wed, 30 Jul 2025 07:00:50 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 30 Jul 2025 07:00:50 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 30 Jul 2025 07:00:50 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 30 Jul 2025 07:00:53 GMT
ADD file:e189629238f69759e9c6cb1cac039ece646eeecb640e5eb670e5cf92543b46fb in / 
# Wed, 30 Jul 2025 07:00:53 GMT
CMD ["/bin/bash"]
# Tue, 12 Aug 2025 08:18:47 GMT
EXPOSE map[5601/tcp:{}]
# Tue, 12 Aug 2025 08:18:47 GMT
RUN for iter in {1..10}; do       export DEBIAN_FRONTEND=noninteractive &&       apt-get update  &&       apt-get upgrade -y  &&       apt-get install -y --no-install-recommends       fontconfig fonts-liberation libnss3 curl ca-certificates &&       apt-get clean &&       rm -rf /var/lib/apt/lists/* && exit_code=0 && break || exit_code=$? && echo "apt-get error: retry $iter in 10s" &&       sleep 10;     done;     (exit $exit_code) # buildkit
# Tue, 12 Aug 2025 08:18:47 GMT
COPY --chown=1000:0 /usr/share/kibana /usr/share/kibana # buildkit
# Tue, 12 Aug 2025 08:18:47 GMT
COPY --chown=0:0 /bin/tini /bin/tini # buildkit
# Tue, 12 Aug 2025 08:18:47 GMT
COPY --chown=0:0 /usr/share/fonts/local/NotoSansCJK-Regular.ttc /usr/share/fonts/local/NotoSansCJK-Regular.ttc # buildkit
# Tue, 12 Aug 2025 08:18:47 GMT
RUN fc-cache -v # buildkit
# Tue, 12 Aug 2025 08:18:47 GMT
WORKDIR /usr/share/kibana
# Tue, 12 Aug 2025 08:18:47 GMT
RUN ln -s /usr/share/kibana /opt/kibana # buildkit
# Tue, 12 Aug 2025 08:18:47 GMT
ENV ELASTIC_CONTAINER=true
# Tue, 12 Aug 2025 08:18:47 GMT
ENV PATH=/usr/share/kibana/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 Aug 2025 08:18:47 GMT
COPY --chown=1000:0 config/kibana.yml /usr/share/kibana/config/kibana.yml # buildkit
# Tue, 12 Aug 2025 08:18:47 GMT
COPY bin/kibana-docker /usr/local/bin/ # buildkit
# Tue, 12 Aug 2025 08:18:47 GMT
RUN chmod g+ws /usr/share/kibana &&     find /usr/share/kibana -gid 0 -and -not -perm /g+w -exec chmod g+w {} \; # buildkit
# Tue, 12 Aug 2025 08:18:47 GMT
RUN find / -xdev -perm -4000 -exec chmod u-s {} + # buildkit
# Tue, 12 Aug 2025 08:18:47 GMT
RUN userdel -r ubuntu && groupadd --gid 1000 kibana &&     useradd --uid 1000 --gid 1000 -G 0       --home-dir /usr/share/kibana --no-create-home       kibana # buildkit
# Tue, 12 Aug 2025 08:18:47 GMT
LABEL org.label-schema.build-date=2025-08-07T20:18:34.689Z org.label-schema.license=Elastic License org.label-schema.name=Kibana org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/kibana org.label-schema.usage=https://www.elastic.co/guide/en/kibana/reference/index.html org.label-schema.vcs-ref=bbd44b7913a0eec99d54d68722f751de92ebe1ce org.label-schema.vcs-url=https://github.com/elastic/kibana org.label-schema.vendor=Elastic org.label-schema.version=8.17.10 org.opencontainers.image.created=2025-08-07T20:18:34.689Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/kibana/reference/index.html org.opencontainers.image.licenses=Elastic License org.opencontainers.image.revision=bbd44b7913a0eec99d54d68722f751de92ebe1ce org.opencontainers.image.source=https://github.com/elastic/kibana org.opencontainers.image.title=Kibana org.opencontainers.image.url=https://www.elastic.co/products/kibana org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=8.17.10
# Tue, 12 Aug 2025 08:18:47 GMT
ENTRYPOINT ["/bin/tini" "--"]
# Tue, 12 Aug 2025 08:18:47 GMT
CMD ["/usr/local/bin/kibana-docker"]
# Tue, 12 Aug 2025 08:18:47 GMT
USER 1000
```

-	Layers:
	-	`sha256:49a8ca9a328e179fe07d40f7f2fd5fb2860b5c45463c288b64f05be521173d2e`  
		Last Modified: Wed, 30 Jul 2025 10:35:20 GMT  
		Size: 28.9 MB (28860377 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7390382d183389d73c2977b686c41af0e633e39481df6d453af5527481b586d`  
		Last Modified: Tue, 12 Aug 2025 19:39:37 GMT  
		Size: 9.5 MB (9526104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1dc776529f99083751cf1e4452cc4866d0f572414ee285ded33b5ccd51fa6d23`  
		Last Modified: Tue, 12 Aug 2025 20:16:39 GMT  
		Size: 360.6 MB (360551661 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75d0211a2426add1c35807523043ab786a07865793e6694ec6c4ae07815e9ce5`  
		Last Modified: Tue, 12 Aug 2025 19:39:35 GMT  
		Size: 9.1 KB (9099 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8aa91fbf8d346949dd3aefc24a63810183dad4c5266c8cc08a790eed613807a8`  
		Last Modified: Tue, 12 Aug 2025 19:39:38 GMT  
		Size: 16.5 MB (16460494 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94be9050a3bdcd0176433bde36b71825f176f53f134866839417fc44e38c05f3`  
		Last Modified: Tue, 12 Aug 2025 19:39:37 GMT  
		Size: 5.2 KB (5240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0c80e85b8d4678b0968fbf03123771f052e8b797a896a9c923c394a92b0d269`  
		Last Modified: Tue, 12 Aug 2025 19:39:36 GMT  
		Size: 131.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:102463ea3d08147234ef1574d4fdd7621ac9305ed4b155e5ad724fceeb5a744f`  
		Last Modified: Tue, 12 Aug 2025 19:39:36 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99d1dc04b68cf303d22568798e37f5d940934243d9b83bc167c083846d1406ea`  
		Last Modified: Tue, 12 Aug 2025 19:39:37 GMT  
		Size: 4.7 KB (4728 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6758d959f227508fe70511f58d0e3e960127b0078cc88d79b559bf926b10316`  
		Last Modified: Tue, 12 Aug 2025 19:39:38 GMT  
		Size: 402.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95590b862e14b9d89bca6a6168b6b357a8eb1f1a3fa713d56cc80fe65e546c17`  
		Last Modified: Tue, 12 Aug 2025 19:39:38 GMT  
		Size: 158.0 KB (157996 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:482b28ca260c092690bada595ae9dda52fe478a586c4b0ba887ee758274faa70`  
		Last Modified: Tue, 12 Aug 2025 19:39:37 GMT  
		Size: 1.2 KB (1223 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kibana:8.17.10` - unknown; unknown

```console
$ docker pull kibana@sha256:f5e80f783d2a355c5d1ff96e78e8bff08ffe0ba2bb86b6077c81dc9b86df9081
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4562181 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d19ecc548ad09cdafa0747c26084e5866862526a46a4dc16461d56a6c4d73b87`

```dockerfile
```

-	Layers:
	-	`sha256:12bcacc2a25da2b0de7a947d1c0fc474f320a8a3b929323f2ef45a78ed177c57`  
		Last Modified: Tue, 12 Aug 2025 20:11:37 GMT  
		Size: 4.5 MB (4521200 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e95f3e16cbace48a24d20556d4358599a81dd971108e6dfa1101d43a1aafc54a`  
		Last Modified: Tue, 12 Aug 2025 20:11:37 GMT  
		Size: 41.0 KB (40981 bytes)  
		MIME: application/vnd.in-toto+json

## `kibana:8.18.5`

```console
$ docker pull kibana@sha256:28bac7049cfce696455825380038ca4db1932ce54da0c6695ac8b97272dcf0da
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `kibana:8.18.5` - linux; amd64

```console
$ docker pull kibana@sha256:ea30a3f7caec07f02a32dea79279c0942b661e8cfb7bfd52ed0b8b9b1b2a28b5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **423.3 MB (423316189 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c0f784b3936c1eaf395229df7d59894e20ed27ac6b0797995662af4ecfb1edc7`
-	Entrypoint: `["\/bin\/tini","--"]`
-	Default Command: `["\/usr\/local\/bin\/kibana-docker"]`

```dockerfile
# Tue, 12 Aug 2025 08:42:34 GMT
ARG RELEASE
# Tue, 12 Aug 2025 08:42:34 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 12 Aug 2025 08:42:34 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 12 Aug 2025 08:42:34 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 12 Aug 2025 08:42:34 GMT
ADD file:e67907c77897d27192314f6c4fa0112b6f7dce3e127500516535cc50fe736c92 in / 
# Tue, 12 Aug 2025 08:42:34 GMT
CMD ["/bin/bash"]
# Tue, 12 Aug 2025 08:42:34 GMT
EXPOSE map[5601/tcp:{}]
# Tue, 12 Aug 2025 08:42:34 GMT
RUN for iter in {1..10}; do       export DEBIAN_FRONTEND=noninteractive &&       apt-get update  &&       apt-get upgrade -y  &&       apt-get install -y --no-install-recommends       fontconfig fonts-liberation libnss3 curl ca-certificates &&       apt-get clean &&       rm -rf /var/lib/apt/lists/* && exit_code=0 && break || exit_code=$? && echo "apt-get error: retry $iter in 10s" &&       sleep 10;     done;     (exit $exit_code) # buildkit
# Tue, 12 Aug 2025 08:42:34 GMT
COPY --chown=1000:0 /usr/share/kibana /usr/share/kibana # buildkit
# Tue, 12 Aug 2025 08:42:34 GMT
COPY --chown=0:0 /bin/tini /bin/tini # buildkit
# Tue, 12 Aug 2025 08:42:34 GMT
COPY --chown=0:0 /usr/share/fonts/local/NotoSansCJK-Regular.ttc /usr/share/fonts/local/NotoSansCJK-Regular.ttc # buildkit
# Tue, 12 Aug 2025 08:42:34 GMT
RUN fc-cache -v # buildkit
# Tue, 12 Aug 2025 08:42:34 GMT
WORKDIR /usr/share/kibana
# Tue, 12 Aug 2025 08:42:34 GMT
RUN ln -s /usr/share/kibana /opt/kibana # buildkit
# Tue, 12 Aug 2025 08:42:34 GMT
ENV ELASTIC_CONTAINER=true
# Tue, 12 Aug 2025 08:42:34 GMT
ENV PATH=/usr/share/kibana/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 Aug 2025 08:42:34 GMT
COPY --chown=1000:0 config/kibana.yml /usr/share/kibana/config/kibana.yml # buildkit
# Tue, 12 Aug 2025 08:42:34 GMT
COPY bin/kibana-docker /usr/local/bin/ # buildkit
# Tue, 12 Aug 2025 08:42:34 GMT
RUN chmod g+ws /usr/share/kibana &&     find /usr/share/kibana -gid 0 -and -not -perm /g+w -exec chmod g+w {} \; # buildkit
# Tue, 12 Aug 2025 08:42:34 GMT
RUN find / -xdev -perm -4000 -exec chmod u-s {} + # buildkit
# Tue, 12 Aug 2025 08:42:34 GMT
RUN userdel -r ubuntu && groupadd --gid 1000 kibana &&     useradd --uid 1000 --gid 1000 -G 0       --home-dir /usr/share/kibana --no-create-home       kibana # buildkit
# Tue, 12 Aug 2025 08:42:34 GMT
LABEL org.label-schema.build-date=2025-08-06T20:16:41.306Z org.label-schema.license=Elastic License org.label-schema.name=Kibana org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/kibana org.label-schema.usage=https://www.elastic.co/guide/en/kibana/reference/index.html org.label-schema.vcs-ref=1ac33f19e9d91983b71ac580abe325579e2d7495 org.label-schema.vcs-url=https://github.com/elastic/kibana org.label-schema.vendor=Elastic org.label-schema.version=8.18.5 org.opencontainers.image.created=2025-08-06T20:16:41.306Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/kibana/reference/index.html org.opencontainers.image.licenses=Elastic License org.opencontainers.image.revision=1ac33f19e9d91983b71ac580abe325579e2d7495 org.opencontainers.image.source=https://github.com/elastic/kibana org.opencontainers.image.title=Kibana org.opencontainers.image.url=https://www.elastic.co/products/kibana org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=8.18.5
# Tue, 12 Aug 2025 08:42:34 GMT
ENTRYPOINT ["/bin/tini" "--"]
# Tue, 12 Aug 2025 08:42:34 GMT
CMD ["/usr/local/bin/kibana-docker"]
# Tue, 12 Aug 2025 08:42:34 GMT
USER 1000
```

-	Layers:
	-	`sha256:76249c7cd50397d2e8c06a75106723d057deaba0ffbc7f4af1bb02bcf71d81cf`  
		Last Modified: Tue, 19 Aug 2025 17:39:10 GMT  
		Size: 29.7 MB (29723064 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65cd026036ebc02ac6a9fb8da345501b3cc6e2fe0a6502527a6246bcd492f868`  
		Last Modified: Mon, 01 Sep 2025 23:13:43 GMT  
		Size: 9.4 MB (9431891 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfdfb344ece88b9674bc68ff5c965e4d3b406878788bf710828d8d894c629fc7`  
		Last Modified: Tue, 02 Sep 2025 00:28:59 GMT  
		Size: 367.5 MB (367517578 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69913c76075c640a12ed1c23c60e1a0cd8e67178215c275888c88541b3cd9f34`  
		Last Modified: Mon, 01 Sep 2025 23:13:41 GMT  
		Size: 9.5 KB (9530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c6f4fef45464bd813925937a4ba40ae9c0fea5deb0a907ba859c97e8e12ebcb`  
		Last Modified: Mon, 01 Sep 2025 23:13:42 GMT  
		Size: 16.5 MB (16460484 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:066ccc8ebee31859379f03a36b9fcbdbe6ccde8b82eebe455ad006c06c2d40ad`  
		Last Modified: Mon, 01 Sep 2025 23:13:41 GMT  
		Size: 5.2 KB (5239 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cef7024990011175071370348c647d7e9a4df49004c4c4fdc13b24a8a279bd08`  
		Last Modified: Mon, 01 Sep 2025 23:13:41 GMT  
		Size: 131.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc6798ef3cd30483eb1cd0ff6726a506b498ea99ffc9164d835dc57752b62684`  
		Last Modified: Mon, 01 Sep 2025 23:13:41 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1927a8341449024f4d9b68850a89d072d24f6afe522b2d4c4f0d05e4480fcca1`  
		Last Modified: Mon, 01 Sep 2025 23:13:41 GMT  
		Size: 4.8 KB (4761 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92fbdfd6aa29cb6fce224fc42e51173baa20688e2a327e3b4e837347a06baa9b`  
		Last Modified: Mon, 01 Sep 2025 23:13:41 GMT  
		Size: 400.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2ed3bfa8ea5c09135f8fdafe7171286013690a013b85ab6b1c4689290dd3161`  
		Last Modified: Mon, 01 Sep 2025 23:13:41 GMT  
		Size: 161.5 KB (161459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ac243767a58834025647d3fb943bef7e51f1eed4ea02d5d6488913888c3bbac`  
		Last Modified: Mon, 01 Sep 2025 23:13:41 GMT  
		Size: 1.2 KB (1223 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kibana:8.18.5` - unknown; unknown

```console
$ docker pull kibana@sha256:eece99544ac19e0f1a61758a1ab0428b1b832117d0ba25dd7eea995117de4bf2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4917379 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e00df3421ad6058fed9f195dabb3ddb2f63a77e4a580a4731ee5170412d259b6`

```dockerfile
```

-	Layers:
	-	`sha256:4d19bd02211c8dfcb55b8f838401fb7402702560ac7a06da312e3094d7a3f3f7`  
		Last Modified: Tue, 02 Sep 2025 02:11:30 GMT  
		Size: 4.9 MB (4876652 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:82caee081562180c29895474e65bf8ef5ca032e68d55b64e3a0f02f88bef0c17`  
		Last Modified: Tue, 02 Sep 2025 02:11:31 GMT  
		Size: 40.7 KB (40727 bytes)  
		MIME: application/vnd.in-toto+json

### `kibana:8.18.5` - linux; arm64 variant v8

```console
$ docker pull kibana@sha256:d5c1cad8f5ac13f609254e66c89183f2f0b4ebc8209e5b1a085dfe94f90451b7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **435.6 MB (435577219 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e59c32c41d5aa8be163d3db3fec4ba65ca2cbcb98b0054dd2b5084021bc16bd`
-	Entrypoint: `["\/bin\/tini","--"]`
-	Default Command: `["\/usr\/local\/bin\/kibana-docker"]`

```dockerfile
# Wed, 30 Jul 2025 07:00:50 GMT
ARG RELEASE
# Wed, 30 Jul 2025 07:00:50 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 30 Jul 2025 07:00:50 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 30 Jul 2025 07:00:50 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 30 Jul 2025 07:00:53 GMT
ADD file:e189629238f69759e9c6cb1cac039ece646eeecb640e5eb670e5cf92543b46fb in / 
# Wed, 30 Jul 2025 07:00:53 GMT
CMD ["/bin/bash"]
# Tue, 12 Aug 2025 08:42:34 GMT
EXPOSE map[5601/tcp:{}]
# Tue, 12 Aug 2025 08:42:34 GMT
RUN for iter in {1..10}; do       export DEBIAN_FRONTEND=noninteractive &&       apt-get update  &&       apt-get upgrade -y  &&       apt-get install -y --no-install-recommends       fontconfig fonts-liberation libnss3 curl ca-certificates &&       apt-get clean &&       rm -rf /var/lib/apt/lists/* && exit_code=0 && break || exit_code=$? && echo "apt-get error: retry $iter in 10s" &&       sleep 10;     done;     (exit $exit_code) # buildkit
# Tue, 12 Aug 2025 08:42:34 GMT
COPY --chown=1000:0 /usr/share/kibana /usr/share/kibana # buildkit
# Tue, 12 Aug 2025 08:42:34 GMT
COPY --chown=0:0 /bin/tini /bin/tini # buildkit
# Tue, 12 Aug 2025 08:42:34 GMT
COPY --chown=0:0 /usr/share/fonts/local/NotoSansCJK-Regular.ttc /usr/share/fonts/local/NotoSansCJK-Regular.ttc # buildkit
# Tue, 12 Aug 2025 08:42:34 GMT
RUN fc-cache -v # buildkit
# Tue, 12 Aug 2025 08:42:34 GMT
WORKDIR /usr/share/kibana
# Tue, 12 Aug 2025 08:42:34 GMT
RUN ln -s /usr/share/kibana /opt/kibana # buildkit
# Tue, 12 Aug 2025 08:42:34 GMT
ENV ELASTIC_CONTAINER=true
# Tue, 12 Aug 2025 08:42:34 GMT
ENV PATH=/usr/share/kibana/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 Aug 2025 08:42:34 GMT
COPY --chown=1000:0 config/kibana.yml /usr/share/kibana/config/kibana.yml # buildkit
# Tue, 12 Aug 2025 08:42:34 GMT
COPY bin/kibana-docker /usr/local/bin/ # buildkit
# Tue, 12 Aug 2025 08:42:34 GMT
RUN chmod g+ws /usr/share/kibana &&     find /usr/share/kibana -gid 0 -and -not -perm /g+w -exec chmod g+w {} \; # buildkit
# Tue, 12 Aug 2025 08:42:34 GMT
RUN find / -xdev -perm -4000 -exec chmod u-s {} + # buildkit
# Tue, 12 Aug 2025 08:42:34 GMT
RUN userdel -r ubuntu && groupadd --gid 1000 kibana &&     useradd --uid 1000 --gid 1000 -G 0       --home-dir /usr/share/kibana --no-create-home       kibana # buildkit
# Tue, 12 Aug 2025 08:42:34 GMT
LABEL org.label-schema.build-date=2025-08-06T20:16:41.306Z org.label-schema.license=Elastic License org.label-schema.name=Kibana org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/kibana org.label-schema.usage=https://www.elastic.co/guide/en/kibana/reference/index.html org.label-schema.vcs-ref=1ac33f19e9d91983b71ac580abe325579e2d7495 org.label-schema.vcs-url=https://github.com/elastic/kibana org.label-schema.vendor=Elastic org.label-schema.version=8.18.5 org.opencontainers.image.created=2025-08-06T20:16:41.306Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/kibana/reference/index.html org.opencontainers.image.licenses=Elastic License org.opencontainers.image.revision=1ac33f19e9d91983b71ac580abe325579e2d7495 org.opencontainers.image.source=https://github.com/elastic/kibana org.opencontainers.image.title=Kibana org.opencontainers.image.url=https://www.elastic.co/products/kibana org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=8.18.5
# Tue, 12 Aug 2025 08:42:34 GMT
ENTRYPOINT ["/bin/tini" "--"]
# Tue, 12 Aug 2025 08:42:34 GMT
CMD ["/usr/local/bin/kibana-docker"]
# Tue, 12 Aug 2025 08:42:34 GMT
USER 1000
```

-	Layers:
	-	`sha256:49a8ca9a328e179fe07d40f7f2fd5fb2860b5c45463c288b64f05be521173d2e`  
		Last Modified: Wed, 30 Jul 2025 10:35:20 GMT  
		Size: 28.9 MB (28860377 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7390382d183389d73c2977b686c41af0e633e39481df6d453af5527481b586d`  
		Last Modified: Tue, 12 Aug 2025 19:39:37 GMT  
		Size: 9.5 MB (9526104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65a9f6c64a42cc1c96d909eb6b19238041654050a211a1ad74841debf205b21b`  
		Last Modified: Tue, 12 Aug 2025 20:17:03 GMT  
		Size: 380.6 MB (380550981 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abcd5373e34f6124e0955e0902f4a5b54b9ee04def8deb33aa0bcfa8e8f5b560`  
		Last Modified: Tue, 12 Aug 2025 19:47:10 GMT  
		Size: 9.1 KB (9096 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:073d1060274aabb8a7b32412d624565821cd408c2d9a66b30b621a25d37b315d`  
		Last Modified: Tue, 12 Aug 2025 19:47:15 GMT  
		Size: 16.5 MB (16460484 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:849a09cf15308406ee80ba2e129ac811c40db1554c7ef0d11cd61e3429b43645`  
		Last Modified: Tue, 12 Aug 2025 19:47:10 GMT  
		Size: 5.2 KB (5239 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:301af5c80a49456004215f01ebde7b965909ba10fdb36dcd897543d520fbf1d7`  
		Last Modified: Tue, 12 Aug 2025 19:47:11 GMT  
		Size: 131.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01a2702a433bac855d21b1cf01c4ec74387987fbffa81bf757b18fb485711ed0`  
		Last Modified: Tue, 12 Aug 2025 19:47:12 GMT  
		Size: 393.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30b973a700064fdf1c9610c18e1e3416052d8f9632f32ee3ffaafc0a8b2761c6`  
		Last Modified: Tue, 12 Aug 2025 19:47:12 GMT  
		Size: 4.8 KB (4759 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e6ef2d0d986e66e8419cb495ce6283a8931991706e520c34cb6e36c05ce44fa`  
		Last Modified: Tue, 12 Aug 2025 19:47:11 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03628bf22b0c94880b89acd6a68c5014a10d98bd3a232e4f3a14e015cf613ffa`  
		Last Modified: Tue, 12 Aug 2025 19:47:12 GMT  
		Size: 158.0 KB (157996 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f91e0ce080dc01fdbc30d59bcb1698f53c0457b1fa7809b05056934b02e6d233`  
		Last Modified: Tue, 12 Aug 2025 19:47:12 GMT  
		Size: 1.2 KB (1231 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kibana:8.18.5` - unknown; unknown

```console
$ docker pull kibana@sha256:9db96a53183648403742ca628987eecececb24112767f1fc819c5c8f92804b4e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4918691 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:86d46e12c1556b0bec948e415f79da2c122265383c858863e2408d06d7fd7ce9`

```dockerfile
```

-	Layers:
	-	`sha256:19a3ee6a8eb8ed1d176a51dde0b48d8a045fab2a648e26753bfa1c4af589590a`  
		Last Modified: Tue, 12 Aug 2025 20:11:52 GMT  
		Size: 4.9 MB (4877716 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1c7e86d59f2f08d23d142dc5e52ace62e9a3fb2636f5d6d1c416d9c95198eec9`  
		Last Modified: Tue, 12 Aug 2025 20:11:53 GMT  
		Size: 41.0 KB (40975 bytes)  
		MIME: application/vnd.in-toto+json

## `kibana:8.19.2`

```console
$ docker pull kibana@sha256:5edafd4681b6554cc48b255d25021781274b2ae76a9c90b48b9617f15f7ef017
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `kibana:8.19.2` - linux; amd64

```console
$ docker pull kibana@sha256:0852c03f3bc8ca7748180c02f014cb01b8baccf9c59b1ef6c919e60923a8133b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **436.1 MB (436104859 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e60c987bf3ef8d4aa37ea70e42d1ab795bda627482d714e93422bf567cbf43f`
-	Entrypoint: `["\/bin\/tini","--"]`
-	Default Command: `["\/usr\/local\/bin\/kibana-docker"]`

```dockerfile
# Tue, 12 Aug 2025 11:48:35 GMT
ARG RELEASE
# Tue, 12 Aug 2025 11:48:35 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 12 Aug 2025 11:48:35 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 12 Aug 2025 11:48:35 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 12 Aug 2025 11:48:35 GMT
ADD file:e67907c77897d27192314f6c4fa0112b6f7dce3e127500516535cc50fe736c92 in / 
# Tue, 12 Aug 2025 11:48:35 GMT
CMD ["/bin/bash"]
# Tue, 12 Aug 2025 11:48:35 GMT
EXPOSE map[5601/tcp:{}]
# Tue, 12 Aug 2025 11:48:35 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&       apt-get update &&       apt-get install -y --no-install-recommends fontconfig fonts-liberation libnss3 curl ca-certificates &&       apt-get clean &&       rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 12 Aug 2025 11:48:35 GMT
COPY --chown=1000:0 /usr/share/kibana /usr/share/kibana # buildkit
# Tue, 12 Aug 2025 11:48:35 GMT
COPY --chown=0:0 /bin/tini /bin/tini # buildkit
# Tue, 12 Aug 2025 11:48:35 GMT
COPY --chown=0:0 /usr/share/fonts/local/NotoSansCJK-Regular.ttc /usr/share/fonts/local/NotoSansCJK-Regular.ttc # buildkit
# Tue, 12 Aug 2025 11:48:35 GMT
RUN fc-cache -v # buildkit
# Tue, 12 Aug 2025 11:48:35 GMT
WORKDIR /usr/share/kibana
# Tue, 12 Aug 2025 11:48:35 GMT
RUN ln -s /usr/share/kibana /opt/kibana # buildkit
# Tue, 12 Aug 2025 11:48:35 GMT
ENV ELASTIC_CONTAINER=true
# Tue, 12 Aug 2025 11:48:35 GMT
ENV PATH=/usr/share/kibana/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 Aug 2025 11:48:35 GMT
COPY --chown=1000:0 config/kibana.yml /usr/share/kibana/config/kibana.yml # buildkit
# Tue, 12 Aug 2025 11:48:35 GMT
COPY bin/kibana-docker /usr/local/bin/ # buildkit
# Tue, 12 Aug 2025 11:48:35 GMT
RUN chmod g+ws /usr/share/kibana &&     find /usr/share/kibana -gid 0 -and -not -perm /g+w -exec chmod g+w {} \; # buildkit
# Tue, 12 Aug 2025 11:48:35 GMT
RUN find / -xdev -perm -4000 -exec chmod u-s {} + # buildkit
# Tue, 12 Aug 2025 11:48:35 GMT
RUN userdel -r ubuntu && groupadd --gid 1000 kibana &&     useradd --uid 1000 --gid 1000 -G 0       --home-dir /usr/share/kibana --no-create-home       kibana # buildkit
# Tue, 12 Aug 2025 11:48:35 GMT
LABEL org.label-schema.build-date=2025-08-11T11:07:38.658Z org.label-schema.license=Elastic License org.label-schema.name=Kibana org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/kibana org.label-schema.usage=https://www.elastic.co/guide/en/kibana/reference/index.html org.label-schema.vcs-ref=8634f44eaffa9f009f50401a2fbba85c95739a38 org.label-schema.vcs-url=https://github.com/elastic/kibana org.label-schema.vendor=Elastic org.label-schema.version=8.19.2 org.opencontainers.image.created=2025-08-11T11:07:38.658Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/kibana/reference/index.html org.opencontainers.image.licenses=Elastic License org.opencontainers.image.revision=8634f44eaffa9f009f50401a2fbba85c95739a38 org.opencontainers.image.source=https://github.com/elastic/kibana org.opencontainers.image.title=Kibana org.opencontainers.image.url=https://www.elastic.co/products/kibana org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=8.19.2
# Tue, 12 Aug 2025 11:48:35 GMT
ENTRYPOINT ["/bin/tini" "--"]
# Tue, 12 Aug 2025 11:48:35 GMT
CMD ["/usr/local/bin/kibana-docker"]
# Tue, 12 Aug 2025 11:48:35 GMT
USER 1000
```

-	Layers:
	-	`sha256:76249c7cd50397d2e8c06a75106723d057deaba0ffbc7f4af1bb02bcf71d81cf`  
		Last Modified: Tue, 19 Aug 2025 17:39:10 GMT  
		Size: 29.7 MB (29723064 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b8f01e28d0afecec3a8a8b86d11c177f8ee2a742bebe96ea24e4bb391fbbd49`  
		Last Modified: Mon, 01 Sep 2025 23:14:41 GMT  
		Size: 9.4 MB (9431835 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:beb99ac34b5cc6d5f160f1631df9b845a23b9d12b73d6227974ca3ad9f93788e`  
		Last Modified: Tue, 02 Sep 2025 02:16:54 GMT  
		Size: 380.3 MB (380306259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:408a89f57b02a4833d291faa3e9c741869b66e11e8571e8280bcf400089ec701`  
		Last Modified: Mon, 01 Sep 2025 23:15:34 GMT  
		Size: 9.5 KB (9529 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8942734dcc84fa260416003ae1587accc7c0d4de766704eabbddb73f2ba31c3f`  
		Last Modified: Mon, 01 Sep 2025 23:15:36 GMT  
		Size: 16.5 MB (16460485 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af3649fd817900abc6b313597d3e232005dc6cc7392e3ed45ff4f417fec76d60`  
		Last Modified: Mon, 01 Sep 2025 23:15:33 GMT  
		Size: 5.2 KB (5241 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3724a44fdceb618a3bd7350d2bacfc25676a2a3dd98d68ae56631afa4f6c8845`  
		Last Modified: Mon, 01 Sep 2025 23:15:33 GMT  
		Size: 131.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a65c0876745c2d2fe373944355b84d1b5cf9d0034b81d42429a61c162c38538`  
		Last Modified: Mon, 01 Sep 2025 23:15:33 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd2ec5a362b8c6355585a8f2ecf1d4a5f2def906631b03be27551ac9c7c7cd08`  
		Last Modified: Mon, 01 Sep 2025 23:15:42 GMT  
		Size: 4.8 KB (4804 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:576153d20c27f46a03a558dbd0270657a78a11d27ebc45b32155e726ba82075b`  
		Last Modified: Mon, 01 Sep 2025 23:15:33 GMT  
		Size: 400.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8632fb15fe5b8ea4e22c3c32f2319f5997dac5a1dad68142f52c2d069b65bc47`  
		Last Modified: Mon, 01 Sep 2025 23:15:34 GMT  
		Size: 161.5 KB (161458 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a4fd2cc54cc784f83b28b6ba6fc4e48931f84e7b829c3c48e5753ee2a97955a`  
		Last Modified: Mon, 01 Sep 2025 23:43:11 GMT  
		Size: 1.2 KB (1224 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kibana:8.19.2` - unknown; unknown

```console
$ docker pull kibana@sha256:341139543d3f6447c068bac18e3d82aeb13f7f5d6daa8ae167a2462af7507f3d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4932258 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:57f00a3536cec97cb5c083c5d24317f2b67cbe7de0d5e4a6678f6b8f550a4dbe`

```dockerfile
```

-	Layers:
	-	`sha256:bd8737549ea2afed6d04080dbbf1064ee81dcd43103052dbfcbb96e1941069d2`  
		Last Modified: Tue, 02 Sep 2025 02:11:36 GMT  
		Size: 4.9 MB (4891307 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c33c665efe3bdfa16ce047db5cf22a3254109e065b0f3f7187e411b9b11a8757`  
		Last Modified: Tue, 02 Sep 2025 02:11:37 GMT  
		Size: 41.0 KB (40951 bytes)  
		MIME: application/vnd.in-toto+json

### `kibana:8.19.2` - linux; arm64 variant v8

```console
$ docker pull kibana@sha256:eee6e493afc50ca4a28941c22e861fc8d2374383f39bb077a945f03f877d6a37
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **448.0 MB (448035263 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:38f510adfcf1a2ded4926b47c213bac7b7eaeab7372fcf81a3f35c86c269f296`
-	Entrypoint: `["\/bin\/tini","--"]`
-	Default Command: `["\/usr\/local\/bin\/kibana-docker"]`

```dockerfile
# Wed, 30 Jul 2025 07:00:50 GMT
ARG RELEASE
# Wed, 30 Jul 2025 07:00:50 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 30 Jul 2025 07:00:50 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 30 Jul 2025 07:00:50 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 30 Jul 2025 07:00:53 GMT
ADD file:e189629238f69759e9c6cb1cac039ece646eeecb640e5eb670e5cf92543b46fb in / 
# Wed, 30 Jul 2025 07:00:53 GMT
CMD ["/bin/bash"]
# Tue, 12 Aug 2025 11:48:35 GMT
EXPOSE map[5601/tcp:{}]
# Tue, 12 Aug 2025 11:48:35 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&       apt-get update &&       apt-get install -y --no-install-recommends fontconfig fonts-liberation libnss3 curl ca-certificates &&       apt-get clean &&       rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 12 Aug 2025 11:48:35 GMT
COPY --chown=1000:0 /usr/share/kibana /usr/share/kibana # buildkit
# Tue, 12 Aug 2025 11:48:35 GMT
COPY --chown=0:0 /bin/tini /bin/tini # buildkit
# Tue, 12 Aug 2025 11:48:35 GMT
COPY --chown=0:0 /usr/share/fonts/local/NotoSansCJK-Regular.ttc /usr/share/fonts/local/NotoSansCJK-Regular.ttc # buildkit
# Tue, 12 Aug 2025 11:48:35 GMT
RUN fc-cache -v # buildkit
# Tue, 12 Aug 2025 11:48:35 GMT
WORKDIR /usr/share/kibana
# Tue, 12 Aug 2025 11:48:35 GMT
RUN ln -s /usr/share/kibana /opt/kibana # buildkit
# Tue, 12 Aug 2025 11:48:35 GMT
ENV ELASTIC_CONTAINER=true
# Tue, 12 Aug 2025 11:48:35 GMT
ENV PATH=/usr/share/kibana/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 Aug 2025 11:48:35 GMT
COPY --chown=1000:0 config/kibana.yml /usr/share/kibana/config/kibana.yml # buildkit
# Tue, 12 Aug 2025 11:48:35 GMT
COPY bin/kibana-docker /usr/local/bin/ # buildkit
# Tue, 12 Aug 2025 11:48:35 GMT
RUN chmod g+ws /usr/share/kibana &&     find /usr/share/kibana -gid 0 -and -not -perm /g+w -exec chmod g+w {} \; # buildkit
# Tue, 12 Aug 2025 11:48:35 GMT
RUN find / -xdev -perm -4000 -exec chmod u-s {} + # buildkit
# Tue, 12 Aug 2025 11:48:35 GMT
RUN userdel -r ubuntu && groupadd --gid 1000 kibana &&     useradd --uid 1000 --gid 1000 -G 0       --home-dir /usr/share/kibana --no-create-home       kibana # buildkit
# Tue, 12 Aug 2025 11:48:35 GMT
LABEL org.label-schema.build-date=2025-08-11T11:07:38.658Z org.label-schema.license=Elastic License org.label-schema.name=Kibana org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/kibana org.label-schema.usage=https://www.elastic.co/guide/en/kibana/reference/index.html org.label-schema.vcs-ref=8634f44eaffa9f009f50401a2fbba85c95739a38 org.label-schema.vcs-url=https://github.com/elastic/kibana org.label-schema.vendor=Elastic org.label-schema.version=8.19.2 org.opencontainers.image.created=2025-08-11T11:07:38.658Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/kibana/reference/index.html org.opencontainers.image.licenses=Elastic License org.opencontainers.image.revision=8634f44eaffa9f009f50401a2fbba85c95739a38 org.opencontainers.image.source=https://github.com/elastic/kibana org.opencontainers.image.title=Kibana org.opencontainers.image.url=https://www.elastic.co/products/kibana org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=8.19.2
# Tue, 12 Aug 2025 11:48:35 GMT
ENTRYPOINT ["/bin/tini" "--"]
# Tue, 12 Aug 2025 11:48:35 GMT
CMD ["/usr/local/bin/kibana-docker"]
# Tue, 12 Aug 2025 11:48:35 GMT
USER 1000
```

-	Layers:
	-	`sha256:49a8ca9a328e179fe07d40f7f2fd5fb2860b5c45463c288b64f05be521173d2e`  
		Last Modified: Wed, 30 Jul 2025 10:35:20 GMT  
		Size: 28.9 MB (28860377 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:422aadf3d556125efcb65d8d104d95a37b722aff4a4d8a96cb3dd6fda4c0155a`  
		Last Modified: Tue, 12 Aug 2025 19:54:44 GMT  
		Size: 9.4 MB (9445862 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ad9a5d9a0e9e06309942022d1324b81b1ef1964c71aecaf1cb90bdd8d0b7b8f`  
		Last Modified: Tue, 12 Aug 2025 20:53:59 GMT  
		Size: 393.1 MB (393089223 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:670e9d0dd118efa243d60a6896ce630c01eee62a5174ff428fc87a54d6fe47e4`  
		Last Modified: Tue, 12 Aug 2025 19:54:41 GMT  
		Size: 9.1 KB (9098 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9cd33f87bf420cc3b32e513728f7c88ff79d2c0828dd31ca88cf19c0d48ddcb`  
		Last Modified: Tue, 12 Aug 2025 19:54:42 GMT  
		Size: 16.5 MB (16460484 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:331e7271430bc0a42b4fb796020036437aab22d506df200a70b324bbac9e994d`  
		Last Modified: Tue, 12 Aug 2025 19:54:42 GMT  
		Size: 5.2 KB (5239 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:187df41b8e20c23ce12a0d30a9755f1fdd57abbddd7c7c0244e0eeab13c9324e`  
		Last Modified: Tue, 12 Aug 2025 19:54:41 GMT  
		Size: 131.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69c672cae6028529928ab9409e4b771de681f739abc69782837a90eb66547749`  
		Last Modified: Tue, 12 Aug 2025 19:54:37 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8cbe5b76070cb6599cc57f60357447ec15677d328b5a70a81c8e7caa741ff3e`  
		Last Modified: Tue, 12 Aug 2025 19:54:37 GMT  
		Size: 4.8 KB (4802 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d23a7a2d582d899453f16f09865c6c92a0667cd04fb14fc782194cecf4d223f`  
		Last Modified: Tue, 12 Aug 2025 19:54:38 GMT  
		Size: 400.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3c33cfac144a39d3564d910a303471d6ed8c71470d2b0f1958b8267c01a37e5`  
		Last Modified: Tue, 12 Aug 2025 19:54:38 GMT  
		Size: 158.0 KB (157996 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f12ac502b491ab8bcfc8711ebd60e606d5198ed8d7044714c37f1e43c2ec46c`  
		Last Modified: Tue, 12 Aug 2025 19:54:38 GMT  
		Size: 1.2 KB (1223 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kibana:8.19.2` - unknown; unknown

```console
$ docker pull kibana@sha256:5c67a51b12abcc5744acd8f6ddb17e168362f99bfd39ac3c7ade45b8892410f6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4933570 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:45a3ab730d50b7a5a5b543d45ab41d7cf4a9e5d22cc385fe1a40cdf35be7b5cc`

```dockerfile
```

-	Layers:
	-	`sha256:8057fb77284f7700a7952cbd0f1ba79e63422dae0686fa02d33c711e16bd1a71`  
		Last Modified: Tue, 12 Aug 2025 20:11:57 GMT  
		Size: 4.9 MB (4892371 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1475c2301f5aa03b7ee35d00a08b7e1bfaddf879563bb8cbede5f4a5fc322122`  
		Last Modified: Tue, 12 Aug 2025 20:11:58 GMT  
		Size: 41.2 KB (41199 bytes)  
		MIME: application/vnd.in-toto+json

## `kibana:9.0.5`

```console
$ docker pull kibana@sha256:8080a59eff90e73e85f09e766dc4d7446ce2adf40148bcfce8d3dd3645a2260b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `kibana:9.0.5` - linux; amd64

```console
$ docker pull kibana@sha256:fadc76f6d509afd38d9207dc566425cecbec55f9e250390b09675adffbf40afe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **437.8 MB (437757489 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:249525bf5c4cd277f012537e73b5b3e22a057c934dc360b54a49d272861d2e4a`
-	Entrypoint: `["\/bin\/tini","--"]`
-	Default Command: `["\/usr\/local\/bin\/kibana-docker"]`

```dockerfile
# Tue, 12 Aug 2025 08:42:57 GMT
LABEL maintainer="Red Hat, Inc."
# Tue, 12 Aug 2025 08:42:57 GMT
LABEL vendor="Red Hat, Inc."
# Tue, 12 Aug 2025 08:42:57 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Tue, 12 Aug 2025 08:42:57 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.6"       distribution-scope="public"
# Tue, 12 Aug 2025 08:42:57 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Tue, 12 Aug 2025 08:42:57 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Tue, 12 Aug 2025 08:42:57 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Tue, 12 Aug 2025 08:42:57 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Tue, 12 Aug 2025 08:42:57 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Tue, 12 Aug 2025 08:42:57 GMT
LABEL io.openshift.expose-services=""
# Tue, 12 Aug 2025 08:42:57 GMT
LABEL io.openshift.tags="minimal rhel9"
# Tue, 12 Aug 2025 08:42:57 GMT
ENV container oci
# Tue, 12 Aug 2025 08:42:57 GMT
COPY dir:e1f22eafd6489859288910ef7585f9d694693aa84a31ba9d54dea9e7a451abe6 in / 
# Tue, 12 Aug 2025 08:42:57 GMT
COPY file:b37d593713ee21ad52a4cd1424dc019a24f7966f85df0ac4b86d234302695328 in /etc/yum.repos.d/. 
# Tue, 12 Aug 2025 08:42:57 GMT
CMD ["/bin/bash"]
# Tue, 12 Aug 2025 08:42:57 GMT
COPY file:58cc94f5b3b2d60de2c77a6ed4b1797dcede502ccdb429a72e7a72d994235b3c in /usr/share/buildinfo/content-sets.json 
# Tue, 12 Aug 2025 08:42:57 GMT
COPY file:58cc94f5b3b2d60de2c77a6ed4b1797dcede502ccdb429a72e7a72d994235b3c in /root/buildinfo/content_manifests/content-sets.json 
# Tue, 12 Aug 2025 08:42:57 GMT
LABEL "build-date"="2025-08-20T13:12:41" "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="f4b088292653bbf5ca8188a5e59ffd06a8671d4b" "release"="1755695350"
# Tue, 12 Aug 2025 08:42:57 GMT
EXPOSE map[5601/tcp:{}]
# Tue, 12 Aug 2025 08:42:57 GMT
RUN microdnf install --setopt=tsflags=nodocs -y       fontconfig liberation-fonts-common freetype shadow-utils nss findutils &&       microdnf clean all # buildkit
# Tue, 12 Aug 2025 08:42:57 GMT
COPY --chown=1000:0 /usr/share/kibana /usr/share/kibana # buildkit
# Tue, 12 Aug 2025 08:42:57 GMT
COPY --chown=0:0 /bin/tini /bin/tini # buildkit
# Tue, 12 Aug 2025 08:42:57 GMT
COPY --chown=0:0 /usr/share/fonts/local/NotoSansCJK-Regular.ttc /usr/share/fonts/local/NotoSansCJK-Regular.ttc # buildkit
# Tue, 12 Aug 2025 08:42:57 GMT
RUN fc-cache -v # buildkit
# Tue, 12 Aug 2025 08:42:57 GMT
WORKDIR /usr/share/kibana
# Tue, 12 Aug 2025 08:42:57 GMT
RUN ln -s /usr/share/kibana /opt/kibana # buildkit
# Tue, 12 Aug 2025 08:42:57 GMT
ENV ELASTIC_CONTAINER=true
# Tue, 12 Aug 2025 08:42:57 GMT
ENV PATH=/usr/share/kibana/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 Aug 2025 08:42:57 GMT
COPY --chown=1000:0 config/kibana.yml /usr/share/kibana/config/kibana.yml # buildkit
# Tue, 12 Aug 2025 08:42:57 GMT
COPY bin/kibana-docker /usr/local/bin/ # buildkit
# Tue, 12 Aug 2025 08:42:57 GMT
RUN chmod g+ws /usr/share/kibana &&     find /usr/share/kibana -gid 0 -and -not -perm /g+w -exec chmod g+w {} \; # buildkit
# Tue, 12 Aug 2025 08:42:57 GMT
RUN find / -xdev -perm -4000 -exec chmod u-s {} + # buildkit
# Tue, 12 Aug 2025 08:42:57 GMT
RUN groupadd --gid 1000 kibana &&     useradd --uid 1000 --gid 1000 -G 0       --home-dir /usr/share/kibana --no-create-home       kibana # buildkit
# Tue, 12 Aug 2025 08:42:57 GMT
LABEL org.label-schema.build-date=2025-08-06T20:32:53.139Z org.label-schema.license=Elastic License org.label-schema.name=Kibana org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/kibana org.label-schema.usage=https://www.elastic.co/guide/en/kibana/reference/index.html org.label-schema.vcs-ref=27e18adc5dc02c84d484e5f221837de2e733f3e4 org.label-schema.vcs-url=https://github.com/elastic/kibana org.label-schema.vendor=Elastic org.label-schema.version=9.0.5 org.opencontainers.image.created=2025-08-06T20:32:53.139Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/kibana/reference/index.html org.opencontainers.image.licenses=Elastic License org.opencontainers.image.revision=27e18adc5dc02c84d484e5f221837de2e733f3e4 org.opencontainers.image.source=https://github.com/elastic/kibana org.opencontainers.image.title=Kibana org.opencontainers.image.url=https://www.elastic.co/products/kibana org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=9.0.5
# Tue, 12 Aug 2025 08:42:57 GMT
LABEL name=Kibana maintainer=infra@elastic.co vendor=Elastic version=9.0.5 release=1 summary=Kibana description=Your window into the Elastic Stack.
# Tue, 12 Aug 2025 08:42:57 GMT
RUN mkdir /licenses && ln LICENSE.txt /licenses/LICENSE # buildkit
# Tue, 12 Aug 2025 08:42:57 GMT
ENTRYPOINT ["/bin/tini" "--"]
# Tue, 12 Aug 2025 08:42:57 GMT
CMD ["/usr/local/bin/kibana-docker"]
# Tue, 12 Aug 2025 08:42:57 GMT
USER 1000
```

-	Layers:
	-	`sha256:1e02d32990adc4dad7c8927f91cca33a1baba746105504093311eb3b0b691fa0`  
		Last Modified: Wed, 20 Aug 2025 15:04:59 GMT  
		Size: 39.6 MB (39647287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4e17d3f5c0b2229f3b09ef99dd1b3a631c4452b575f7c856db6bb4f4df0f76a`  
		Last Modified: Thu, 21 Aug 2025 19:12:10 GMT  
		Size: 19.4 MB (19380838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9760276c89b92f8422bc4914ee5c102c4b5912ff697298e1bba8dbde59c2966`  
		Last Modified: Thu, 21 Aug 2025 20:15:54 GMT  
		Size: 362.2 MB (362170623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26609de6a2f8a5c57ffe0fbe3b399c83e28a0567199865079f10d670d82eb069`  
		Last Modified: Thu, 21 Aug 2025 19:06:35 GMT  
		Size: 9.5 KB (9532 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f30c60fedeaf8a927e3c74aeb472d5166b012038ae54a0f1e937e52c5249d4cc`  
		Last Modified: Thu, 21 Aug 2025 19:06:47 GMT  
		Size: 16.5 MB (16460489 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95a889c238ee3a88831f1cf18f2047025cb532fc49e2f4c2b4edccfc08a31503`  
		Last Modified: Thu, 21 Aug 2025 19:06:52 GMT  
		Size: 5.2 KB (5225 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68c71c0c956bdb180bd28690c429643e04a6d98eaea524a25c98a4c08885c837`  
		Last Modified: Thu, 21 Aug 2025 19:06:56 GMT  
		Size: 131.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:041d5433f8e43d7ffef8f3b1e3dfa63261201f492447321348ba057507da971b`  
		Last Modified: Thu, 21 Aug 2025 19:07:03 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13b8702fff66136d11f9c6b3a4b2fcafdeebd99bd789030cb937a3154421663f`  
		Last Modified: Thu, 21 Aug 2025 19:07:07 GMT  
		Size: 4.7 KB (4688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c89fddae438f81ecfa789ae4a9c4014cd2043fd1bb5a3bc213aedfd74348241`  
		Last Modified: Thu, 21 Aug 2025 19:07:10 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ff09ab5dbab955527978f0e1532e0931112ae77ccdc001560b7f11dc7383b4a`  
		Last Modified: Thu, 21 Aug 2025 19:07:13 GMT  
		Size: 75.1 KB (75095 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f8ef8901a4e65b23bcaf085f915f638189564f542d8f48aa7ab4defe5473b9a`  
		Last Modified: Thu, 21 Aug 2025 19:07:18 GMT  
		Size: 1.0 KB (1046 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:638623b817c9dc8f608d7da4e60c13ba740c1c2ee84aae29671c7e698d9eb395`  
		Last Modified: Thu, 21 Aug 2025 19:07:25 GMT  
		Size: 1.7 KB (1709 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kibana:9.0.5` - unknown; unknown

```console
$ docker pull kibana@sha256:f589c6a50440d13cb8bc9b1136a1a389a1d8a21075cd7d4b4779343dc378bfe8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5628251 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb2b91ebca315414bcc578af3cebf4215dd17ddb296e2adefd675c33a3250475`

```dockerfile
```

-	Layers:
	-	`sha256:ca1851ecae6fcbe58c7938875a5465068989b844ebb141f940eb11a82f966194`  
		Last Modified: Thu, 21 Aug 2025 20:11:26 GMT  
		Size: 5.6 MB (5585066 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d6285a7c6d58e7efb4a2dea64e087293a4462d47570831a30302ece9de67a8f9`  
		Last Modified: Thu, 21 Aug 2025 20:11:26 GMT  
		Size: 43.2 KB (43185 bytes)  
		MIME: application/vnd.in-toto+json

### `kibana:9.0.5` - linux; arm64 variant v8

```console
$ docker pull kibana@sha256:6a15e2f5bd9ef49ae3badc4668c1561536ace46f3e0e7b51611f547adfccff0c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **449.0 MB (448955462 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:52c174a8feba8bf9a8abd41aed1f8dec11c41cce3a1816c23983bb76e366edc2`
-	Entrypoint: `["\/bin\/tini","--"]`
-	Default Command: `["\/usr\/local\/bin\/kibana-docker"]`

```dockerfile
# Tue, 12 Aug 2025 08:42:57 GMT
LABEL maintainer="Red Hat, Inc."
# Tue, 12 Aug 2025 08:42:57 GMT
LABEL vendor="Red Hat, Inc."
# Tue, 12 Aug 2025 08:42:57 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Tue, 12 Aug 2025 08:42:57 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.6"       distribution-scope="public"
# Tue, 12 Aug 2025 08:42:57 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Tue, 12 Aug 2025 08:42:57 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Tue, 12 Aug 2025 08:42:57 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Tue, 12 Aug 2025 08:42:57 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Tue, 12 Aug 2025 08:42:57 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Tue, 12 Aug 2025 08:42:57 GMT
LABEL io.openshift.expose-services=""
# Tue, 12 Aug 2025 08:42:57 GMT
LABEL io.openshift.tags="minimal rhel9"
# Tue, 12 Aug 2025 08:42:57 GMT
ENV container oci
# Tue, 12 Aug 2025 08:42:57 GMT
COPY dir:f91aecd64a5df0b73e2b5740ae90f4bb03c2e87890175a65862ca830f6caced5 in / 
# Tue, 12 Aug 2025 08:42:57 GMT
COPY file:b37d593713ee21ad52a4cd1424dc019a24f7966f85df0ac4b86d234302695328 in /etc/yum.repos.d/. 
# Tue, 12 Aug 2025 08:42:57 GMT
CMD ["/bin/bash"]
# Tue, 12 Aug 2025 08:42:57 GMT
COPY file:0667e9d31385a24c3aef13f2dd9ab6a7b71b3dfcfef5127d3c1e2ea2c838e5cb in /usr/share/buildinfo/content-sets.json 
# Tue, 12 Aug 2025 08:42:57 GMT
COPY file:0667e9d31385a24c3aef13f2dd9ab6a7b71b3dfcfef5127d3c1e2ea2c838e5cb in /root/buildinfo/content_manifests/content-sets.json 
# Tue, 12 Aug 2025 08:42:57 GMT
LABEL "build-date"="2025-08-20T13:14:46" "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="f4b088292653bbf5ca8188a5e59ffd06a8671d4b" "release"="1755695350"
# Tue, 12 Aug 2025 08:42:57 GMT
EXPOSE map[5601/tcp:{}]
# Tue, 12 Aug 2025 08:42:57 GMT
RUN microdnf install --setopt=tsflags=nodocs -y       fontconfig liberation-fonts-common freetype shadow-utils nss findutils &&       microdnf clean all # buildkit
# Tue, 12 Aug 2025 08:42:57 GMT
COPY --chown=1000:0 /usr/share/kibana /usr/share/kibana # buildkit
# Tue, 12 Aug 2025 08:42:57 GMT
COPY --chown=0:0 /bin/tini /bin/tini # buildkit
# Tue, 12 Aug 2025 08:42:57 GMT
COPY --chown=0:0 /usr/share/fonts/local/NotoSansCJK-Regular.ttc /usr/share/fonts/local/NotoSansCJK-Regular.ttc # buildkit
# Tue, 12 Aug 2025 08:42:57 GMT
RUN fc-cache -v # buildkit
# Tue, 12 Aug 2025 08:42:57 GMT
WORKDIR /usr/share/kibana
# Tue, 12 Aug 2025 08:42:57 GMT
RUN ln -s /usr/share/kibana /opt/kibana # buildkit
# Tue, 12 Aug 2025 08:42:57 GMT
ENV ELASTIC_CONTAINER=true
# Tue, 12 Aug 2025 08:42:57 GMT
ENV PATH=/usr/share/kibana/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 Aug 2025 08:42:57 GMT
COPY --chown=1000:0 config/kibana.yml /usr/share/kibana/config/kibana.yml # buildkit
# Tue, 12 Aug 2025 08:42:57 GMT
COPY bin/kibana-docker /usr/local/bin/ # buildkit
# Tue, 12 Aug 2025 08:42:57 GMT
RUN chmod g+ws /usr/share/kibana &&     find /usr/share/kibana -gid 0 -and -not -perm /g+w -exec chmod g+w {} \; # buildkit
# Tue, 12 Aug 2025 08:42:57 GMT
RUN find / -xdev -perm -4000 -exec chmod u-s {} + # buildkit
# Tue, 12 Aug 2025 08:42:57 GMT
RUN groupadd --gid 1000 kibana &&     useradd --uid 1000 --gid 1000 -G 0       --home-dir /usr/share/kibana --no-create-home       kibana # buildkit
# Tue, 12 Aug 2025 08:42:57 GMT
LABEL org.label-schema.build-date=2025-08-06T20:32:53.139Z org.label-schema.license=Elastic License org.label-schema.name=Kibana org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/kibana org.label-schema.usage=https://www.elastic.co/guide/en/kibana/reference/index.html org.label-schema.vcs-ref=27e18adc5dc02c84d484e5f221837de2e733f3e4 org.label-schema.vcs-url=https://github.com/elastic/kibana org.label-schema.vendor=Elastic org.label-schema.version=9.0.5 org.opencontainers.image.created=2025-08-06T20:32:53.139Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/kibana/reference/index.html org.opencontainers.image.licenses=Elastic License org.opencontainers.image.revision=27e18adc5dc02c84d484e5f221837de2e733f3e4 org.opencontainers.image.source=https://github.com/elastic/kibana org.opencontainers.image.title=Kibana org.opencontainers.image.url=https://www.elastic.co/products/kibana org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=9.0.5
# Tue, 12 Aug 2025 08:42:57 GMT
LABEL name=Kibana maintainer=infra@elastic.co vendor=Elastic version=9.0.5 release=1 summary=Kibana description=Your window into the Elastic Stack.
# Tue, 12 Aug 2025 08:42:57 GMT
RUN mkdir /licenses && ln LICENSE.txt /licenses/LICENSE # buildkit
# Tue, 12 Aug 2025 08:42:57 GMT
ENTRYPOINT ["/bin/tini" "--"]
# Tue, 12 Aug 2025 08:42:57 GMT
CMD ["/usr/local/bin/kibana-docker"]
# Tue, 12 Aug 2025 08:42:57 GMT
USER 1000
```

-	Layers:
	-	`sha256:73ac460760dbc07b4e932677ed1d86c86c51259cd8ea7c5f1d5b13c9dd3d9d59`  
		Last Modified: Wed, 20 Aug 2025 18:13:24 GMT  
		Size: 37.9 MB (37859581 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6e8b56e4723ec079a70aa0cfe1546349f02500063f34e283876aa2ab251abb7`  
		Last Modified: Thu, 21 Aug 2025 19:20:11 GMT  
		Size: 19.3 MB (19312287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41f75167bc54122bfe8f809b1be855a00f8be7d6e84c6da30b359d9412c99d29`  
		Last Modified: Thu, 21 Aug 2025 20:15:40 GMT  
		Size: 375.2 MB (375226396 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c812541b37abba24a9c2e7f36d90629d3a708a946394718bad52518e086835d8`  
		Last Modified: Thu, 21 Aug 2025 19:20:10 GMT  
		Size: 9.1 KB (9100 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc0ca81978676e38c38a25a90a5354b2731f84b9c9a5409917c15ef93a46bbec`  
		Last Modified: Thu, 21 Aug 2025 19:20:11 GMT  
		Size: 16.5 MB (16460484 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:143f760752b507d296ee12351c40dcbd449bb7ff4b34765c345b680099cf20a4`  
		Last Modified: Thu, 21 Aug 2025 19:20:10 GMT  
		Size: 5.2 KB (5228 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62e1972d4252ba16aadef078b74f0cf37c1c71c2a0753ee16a23122e2dc24b00`  
		Last Modified: Thu, 21 Aug 2025 19:20:10 GMT  
		Size: 131.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b357ee3585bc3258a717e5fb509ba0d2b80db12ea39d4110c782978fb0619cd`  
		Last Modified: Thu, 21 Aug 2025 19:20:10 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d0015a883b3a2490cadff00b8b257a75c75887f343d5bbef35a2159e3954bd7`  
		Last Modified: Thu, 21 Aug 2025 19:20:10 GMT  
		Size: 4.7 KB (4690 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c49f30281d82914ac50ffc385b968ea9383297b52a5e552e688df20d763229a2`  
		Last Modified: Thu, 21 Aug 2025 19:20:10 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd36b5927908c0d292cd60a205535e7b4b993f3cb6cd0b80ed3abac132523840`  
		Last Modified: Thu, 21 Aug 2025 19:20:10 GMT  
		Size: 74.0 KB (73985 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b45a9924f107ec4dc6acda6565fc8601bc547409602782e464cfd9f349ce6bf1`  
		Last Modified: Thu, 21 Aug 2025 19:20:10 GMT  
		Size: 1.0 KB (1046 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00ba6dc9e874f31987d00857c793354e6ef98bfc75c0eee848a8b13dae43c525`  
		Last Modified: Thu, 21 Aug 2025 19:20:11 GMT  
		Size: 1.7 KB (1709 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kibana:9.0.5` - unknown; unknown

```console
$ docker pull kibana@sha256:e0b99ece8a532016140f0a0806cd1467b41928d4a5986fbbd91b057d91c01b82
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5627186 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9d502857bc6cc2aa1d3a2e67b01e441d4ae3aa0f260538fe40165b1158e85319`

```dockerfile
```

-	Layers:
	-	`sha256:661d52d8dc0fea4f3ca16aab2ef950072c72ddad373b8d9cdbedeb74e3a0e766`  
		Last Modified: Thu, 21 Aug 2025 20:12:30 GMT  
		Size: 5.6 MB (5583744 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:54ddf189f68d40d4117eef0e50c75d1b6439e4c9e968aa91a192a67b4d6fc934`  
		Last Modified: Thu, 21 Aug 2025 20:12:25 GMT  
		Size: 43.4 KB (43442 bytes)  
		MIME: application/vnd.in-toto+json

## `kibana:9.1.2`

```console
$ docker pull kibana@sha256:c3aca1e84676c1aeadbc86eaa922bbe60085366a3dff3d7704f4cd70817d0800
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `kibana:9.1.2` - linux; amd64

```console
$ docker pull kibana@sha256:55280d35582bfc3f21ec395776f20c2f9c8a9ca35108792a82f2135f59aa37f9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **435.7 MB (435699518 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7f8207e151109cbc9e5ec951d1baea81f2cd6a9146b9702e9d27ad2610cef4c0`
-	Entrypoint: `["\/bin\/tini","--"]`
-	Default Command: `["\/usr\/local\/bin\/kibana-docker"]`

```dockerfile
# Tue, 12 Aug 2025 11:49:08 GMT
LABEL maintainer="Red Hat, Inc."
# Tue, 12 Aug 2025 11:49:08 GMT
LABEL vendor="Red Hat, Inc."
# Tue, 12 Aug 2025 11:49:08 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Tue, 12 Aug 2025 11:49:08 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.6"       distribution-scope="public"
# Tue, 12 Aug 2025 11:49:08 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Tue, 12 Aug 2025 11:49:08 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Tue, 12 Aug 2025 11:49:08 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Tue, 12 Aug 2025 11:49:08 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Tue, 12 Aug 2025 11:49:08 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Tue, 12 Aug 2025 11:49:08 GMT
LABEL io.openshift.expose-services=""
# Tue, 12 Aug 2025 11:49:08 GMT
LABEL io.openshift.tags="minimal rhel9"
# Tue, 12 Aug 2025 11:49:08 GMT
ENV container oci
# Tue, 12 Aug 2025 11:49:08 GMT
COPY dir:e1f22eafd6489859288910ef7585f9d694693aa84a31ba9d54dea9e7a451abe6 in / 
# Tue, 12 Aug 2025 11:49:08 GMT
COPY file:b37d593713ee21ad52a4cd1424dc019a24f7966f85df0ac4b86d234302695328 in /etc/yum.repos.d/. 
# Tue, 12 Aug 2025 11:49:08 GMT
CMD ["/bin/bash"]
# Tue, 12 Aug 2025 11:49:08 GMT
COPY file:58cc94f5b3b2d60de2c77a6ed4b1797dcede502ccdb429a72e7a72d994235b3c in /usr/share/buildinfo/content-sets.json 
# Tue, 12 Aug 2025 11:49:08 GMT
COPY file:58cc94f5b3b2d60de2c77a6ed4b1797dcede502ccdb429a72e7a72d994235b3c in /root/buildinfo/content_manifests/content-sets.json 
# Tue, 12 Aug 2025 11:49:08 GMT
LABEL "build-date"="2025-08-20T13:12:41" "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="f4b088292653bbf5ca8188a5e59ffd06a8671d4b" "release"="1755695350"
# Tue, 12 Aug 2025 11:49:08 GMT
EXPOSE map[5601/tcp:{}]
# Tue, 12 Aug 2025 11:49:08 GMT
RUN microdnf install --setopt=tsflags=nodocs -y       fontconfig liberation-fonts-common freetype shadow-utils nss findutils &&       microdnf clean all # buildkit
# Tue, 12 Aug 2025 11:49:08 GMT
COPY --chown=1000:0 /usr/share/kibana /usr/share/kibana # buildkit
# Tue, 12 Aug 2025 11:49:08 GMT
COPY --chown=0:0 /bin/tini /bin/tini # buildkit
# Tue, 12 Aug 2025 11:49:08 GMT
COPY --chown=0:0 /usr/share/fonts/local/NotoSansCJK-Regular.ttc /usr/share/fonts/local/NotoSansCJK-Regular.ttc # buildkit
# Tue, 12 Aug 2025 11:49:08 GMT
RUN fc-cache -v # buildkit
# Tue, 12 Aug 2025 11:49:08 GMT
WORKDIR /usr/share/kibana
# Tue, 12 Aug 2025 11:49:08 GMT
RUN ln -s /usr/share/kibana /opt/kibana # buildkit
# Tue, 12 Aug 2025 11:49:08 GMT
ENV ELASTIC_CONTAINER=true
# Tue, 12 Aug 2025 11:49:08 GMT
ENV PATH=/usr/share/kibana/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 Aug 2025 11:49:08 GMT
COPY --chown=1000:0 config/kibana.yml /usr/share/kibana/config/kibana.yml # buildkit
# Tue, 12 Aug 2025 11:49:08 GMT
COPY bin/kibana-docker /usr/local/bin/ # buildkit
# Tue, 12 Aug 2025 11:49:08 GMT
RUN chmod g+ws /usr/share/kibana &&     find /usr/share/kibana -gid 0 -and -not -perm /g+w -exec chmod g+w {} \; # buildkit
# Tue, 12 Aug 2025 11:49:08 GMT
RUN find / -xdev -perm -4000 -exec chmod u-s {} + # buildkit
# Tue, 12 Aug 2025 11:49:08 GMT
RUN groupadd --gid 1000 kibana &&     useradd --uid 1000 --gid 1000 -G 0       --home-dir /usr/share/kibana --no-create-home       kibana # buildkit
# Tue, 12 Aug 2025 11:49:08 GMT
LABEL org.label-schema.build-date=2025-08-11T16:35:56.587Z org.label-schema.license=Elastic License org.label-schema.name=Kibana org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/kibana org.label-schema.usage=https://www.elastic.co/guide/en/kibana/reference/index.html org.label-schema.vcs-ref=616b79995b497dd1c83937d5f71450516b36b6fa org.label-schema.vcs-url=https://github.com/elastic/kibana org.label-schema.vendor=Elastic org.label-schema.version=9.1.2 org.opencontainers.image.created=2025-08-11T16:35:56.587Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/kibana/reference/index.html org.opencontainers.image.licenses=Elastic License org.opencontainers.image.revision=616b79995b497dd1c83937d5f71450516b36b6fa org.opencontainers.image.source=https://github.com/elastic/kibana org.opencontainers.image.title=Kibana org.opencontainers.image.url=https://www.elastic.co/products/kibana org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=9.1.2
# Tue, 12 Aug 2025 11:49:08 GMT
LABEL name=Kibana maintainer=infra@elastic.co vendor=Elastic version=9.1.2 release=1 summary=Kibana description=Your window into the Elastic Stack.
# Tue, 12 Aug 2025 11:49:08 GMT
RUN mkdir /licenses && ln LICENSE.txt /licenses/LICENSE # buildkit
# Tue, 12 Aug 2025 11:49:08 GMT
ENTRYPOINT ["/bin/tini" "--"]
# Tue, 12 Aug 2025 11:49:08 GMT
CMD ["/usr/local/bin/kibana-docker"]
# Tue, 12 Aug 2025 11:49:08 GMT
USER 1000
```

-	Layers:
	-	`sha256:1e02d32990adc4dad7c8927f91cca33a1baba746105504093311eb3b0b691fa0`  
		Last Modified: Wed, 20 Aug 2025 15:04:59 GMT  
		Size: 39.6 MB (39647287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f1cfebe487f50a798bf1ac93ebf4ee16c43e6af60dfb3210b7a119c279874e0`  
		Last Modified: Thu, 21 Aug 2025 19:12:05 GMT  
		Size: 19.4 MB (19380854 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0f308681d8a817ba4b98d90121baf52fe7be5b3da3fdee7809649c47a35d13b`  
		Last Modified: Thu, 21 Aug 2025 20:16:30 GMT  
		Size: 360.1 MB (360112605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57b0e44f2b29b2704fc376116d990f752fd83250c2236aad4caff04c58f8221e`  
		Last Modified: Thu, 21 Aug 2025 19:12:03 GMT  
		Size: 9.5 KB (9531 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b4e103d41a0bcd7c3722b77b1c88ed73e5ca094cb022b75bf83dfb45309c014`  
		Last Modified: Thu, 21 Aug 2025 19:12:06 GMT  
		Size: 16.5 MB (16460485 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eddbde8bcd7c45a9fafa150263c8bb4d0189c687894fbc0105f6e6254db1e8b8`  
		Last Modified: Thu, 21 Aug 2025 19:12:04 GMT  
		Size: 5.2 KB (5222 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:617227c6813679eeb1859781887bed5746e38162acd69334e3fac01745a892df`  
		Last Modified: Thu, 21 Aug 2025 19:12:04 GMT  
		Size: 130.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d31f789eb27330e22c9b383fab8c5e1f992fad78c91a2225238dd2dcfe20644`  
		Last Modified: Thu, 21 Aug 2025 19:12:04 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33f13e742bc18adc30afd1768981e33cb7140abd89605fdaacc7217342f6022a`  
		Last Modified: Thu, 21 Aug 2025 19:12:03 GMT  
		Size: 4.7 KB (4723 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e607192c6b2634115924b181a5c46c85defaa40a5a61fcf42c9d78040d10a799`  
		Last Modified: Thu, 21 Aug 2025 19:12:04 GMT  
		Size: 399.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16d580e0f83fb9d274f0fa1e392d28489ab7cbace71e6eb71264f859ba32d739`  
		Last Modified: Thu, 21 Aug 2025 19:12:03 GMT  
		Size: 75.1 KB (75097 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c549eca81d9d5e7c3800e8cd26f3b583548114f4bf15a7a2e68168083cc13a94`  
		Last Modified: Thu, 21 Aug 2025 19:12:05 GMT  
		Size: 1.0 KB (1048 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b715357487e09320e40d5e9b0e98ff762af0aff174994cee455b443b1095dd7b`  
		Last Modified: Thu, 21 Aug 2025 19:12:05 GMT  
		Size: 1.7 KB (1708 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kibana:9.1.2` - unknown; unknown

```console
$ docker pull kibana@sha256:6c17532ee009919ccbb8b2a5d5f664062b895578087722a29c00cf26cfb693ce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5737511 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1241e24268735dca8da5e754c482cbbb533ed699de1ab9e3b2fcf01140d415f3`

```dockerfile
```

-	Layers:
	-	`sha256:b6b99d3fd1a82cff246ed1bb07b492ec57686717bc5e2e6ec752d2ebdd1f242f`  
		Last Modified: Thu, 21 Aug 2025 20:11:36 GMT  
		Size: 5.7 MB (5694326 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:29c09a4e552dc0a050e6f4a62a5585af2aa7192c9b262b66aa1692474328ab8f`  
		Last Modified: Thu, 21 Aug 2025 20:11:37 GMT  
		Size: 43.2 KB (43185 bytes)  
		MIME: application/vnd.in-toto+json

### `kibana:9.1.2` - linux; arm64 variant v8

```console
$ docker pull kibana@sha256:e7f84c8f49603346131ef089394845c9ecbd88ba6c15bb6506330a1e26771fc3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **446.6 MB (446601239 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:37cad73ae707126c10df2c623b46ba861554123f5b1fc829f8af0327c9ce6e59`
-	Entrypoint: `["\/bin\/tini","--"]`
-	Default Command: `["\/usr\/local\/bin\/kibana-docker"]`

```dockerfile
# Tue, 12 Aug 2025 11:49:08 GMT
LABEL maintainer="Red Hat, Inc."
# Tue, 12 Aug 2025 11:49:08 GMT
LABEL vendor="Red Hat, Inc."
# Tue, 12 Aug 2025 11:49:08 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Tue, 12 Aug 2025 11:49:08 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.6"       distribution-scope="public"
# Tue, 12 Aug 2025 11:49:08 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Tue, 12 Aug 2025 11:49:08 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Tue, 12 Aug 2025 11:49:08 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Tue, 12 Aug 2025 11:49:08 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Tue, 12 Aug 2025 11:49:08 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Tue, 12 Aug 2025 11:49:08 GMT
LABEL io.openshift.expose-services=""
# Tue, 12 Aug 2025 11:49:08 GMT
LABEL io.openshift.tags="minimal rhel9"
# Tue, 12 Aug 2025 11:49:08 GMT
ENV container oci
# Tue, 12 Aug 2025 11:49:08 GMT
COPY dir:f91aecd64a5df0b73e2b5740ae90f4bb03c2e87890175a65862ca830f6caced5 in / 
# Tue, 12 Aug 2025 11:49:08 GMT
COPY file:b37d593713ee21ad52a4cd1424dc019a24f7966f85df0ac4b86d234302695328 in /etc/yum.repos.d/. 
# Tue, 12 Aug 2025 11:49:08 GMT
CMD ["/bin/bash"]
# Tue, 12 Aug 2025 11:49:08 GMT
COPY file:0667e9d31385a24c3aef13f2dd9ab6a7b71b3dfcfef5127d3c1e2ea2c838e5cb in /usr/share/buildinfo/content-sets.json 
# Tue, 12 Aug 2025 11:49:08 GMT
COPY file:0667e9d31385a24c3aef13f2dd9ab6a7b71b3dfcfef5127d3c1e2ea2c838e5cb in /root/buildinfo/content_manifests/content-sets.json 
# Tue, 12 Aug 2025 11:49:08 GMT
LABEL "build-date"="2025-08-20T13:14:46" "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="f4b088292653bbf5ca8188a5e59ffd06a8671d4b" "release"="1755695350"
# Tue, 12 Aug 2025 11:49:08 GMT
EXPOSE map[5601/tcp:{}]
# Tue, 12 Aug 2025 11:49:08 GMT
RUN microdnf install --setopt=tsflags=nodocs -y       fontconfig liberation-fonts-common freetype shadow-utils nss findutils &&       microdnf clean all # buildkit
# Tue, 12 Aug 2025 11:49:08 GMT
COPY --chown=1000:0 /usr/share/kibana /usr/share/kibana # buildkit
# Tue, 12 Aug 2025 11:49:08 GMT
COPY --chown=0:0 /bin/tini /bin/tini # buildkit
# Tue, 12 Aug 2025 11:49:08 GMT
COPY --chown=0:0 /usr/share/fonts/local/NotoSansCJK-Regular.ttc /usr/share/fonts/local/NotoSansCJK-Regular.ttc # buildkit
# Tue, 12 Aug 2025 11:49:08 GMT
RUN fc-cache -v # buildkit
# Tue, 12 Aug 2025 11:49:08 GMT
WORKDIR /usr/share/kibana
# Tue, 12 Aug 2025 11:49:08 GMT
RUN ln -s /usr/share/kibana /opt/kibana # buildkit
# Tue, 12 Aug 2025 11:49:08 GMT
ENV ELASTIC_CONTAINER=true
# Tue, 12 Aug 2025 11:49:08 GMT
ENV PATH=/usr/share/kibana/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 Aug 2025 11:49:08 GMT
COPY --chown=1000:0 config/kibana.yml /usr/share/kibana/config/kibana.yml # buildkit
# Tue, 12 Aug 2025 11:49:08 GMT
COPY bin/kibana-docker /usr/local/bin/ # buildkit
# Tue, 12 Aug 2025 11:49:08 GMT
RUN chmod g+ws /usr/share/kibana &&     find /usr/share/kibana -gid 0 -and -not -perm /g+w -exec chmod g+w {} \; # buildkit
# Tue, 12 Aug 2025 11:49:08 GMT
RUN find / -xdev -perm -4000 -exec chmod u-s {} + # buildkit
# Tue, 12 Aug 2025 11:49:08 GMT
RUN groupadd --gid 1000 kibana &&     useradd --uid 1000 --gid 1000 -G 0       --home-dir /usr/share/kibana --no-create-home       kibana # buildkit
# Tue, 12 Aug 2025 11:49:08 GMT
LABEL org.label-schema.build-date=2025-08-11T16:35:56.587Z org.label-schema.license=Elastic License org.label-schema.name=Kibana org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/kibana org.label-schema.usage=https://www.elastic.co/guide/en/kibana/reference/index.html org.label-schema.vcs-ref=616b79995b497dd1c83937d5f71450516b36b6fa org.label-schema.vcs-url=https://github.com/elastic/kibana org.label-schema.vendor=Elastic org.label-schema.version=9.1.2 org.opencontainers.image.created=2025-08-11T16:35:56.587Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/kibana/reference/index.html org.opencontainers.image.licenses=Elastic License org.opencontainers.image.revision=616b79995b497dd1c83937d5f71450516b36b6fa org.opencontainers.image.source=https://github.com/elastic/kibana org.opencontainers.image.title=Kibana org.opencontainers.image.url=https://www.elastic.co/products/kibana org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=9.1.2
# Tue, 12 Aug 2025 11:49:08 GMT
LABEL name=Kibana maintainer=infra@elastic.co vendor=Elastic version=9.1.2 release=1 summary=Kibana description=Your window into the Elastic Stack.
# Tue, 12 Aug 2025 11:49:08 GMT
RUN mkdir /licenses && ln LICENSE.txt /licenses/LICENSE # buildkit
# Tue, 12 Aug 2025 11:49:08 GMT
ENTRYPOINT ["/bin/tini" "--"]
# Tue, 12 Aug 2025 11:49:08 GMT
CMD ["/usr/local/bin/kibana-docker"]
# Tue, 12 Aug 2025 11:49:08 GMT
USER 1000
```

-	Layers:
	-	`sha256:73ac460760dbc07b4e932677ed1d86c86c51259cd8ea7c5f1d5b13c9dd3d9d59`  
		Last Modified: Wed, 20 Aug 2025 18:13:24 GMT  
		Size: 37.9 MB (37859581 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6e8b56e4723ec079a70aa0cfe1546349f02500063f34e283876aa2ab251abb7`  
		Last Modified: Thu, 21 Aug 2025 19:20:11 GMT  
		Size: 19.3 MB (19312287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3bdbcc1bdc8e9d63296b9af1e8a8dc7a21d50919098003d05990981079b03a7`  
		Last Modified: Thu, 21 Aug 2025 20:17:27 GMT  
		Size: 372.9 MB (372872133 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fecacdc1e82bae1336a5f868496082490036b10c0c58b1a2263364ced6049739`  
		Last Modified: Thu, 21 Aug 2025 19:29:45 GMT  
		Size: 9.1 KB (9101 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c98d49777834e6231b46f62acf4667752989c5035a0b01da2248273771fd0ae7`  
		Last Modified: Thu, 21 Aug 2025 19:29:47 GMT  
		Size: 16.5 MB (16460489 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5e44e2a051903db75298c3f0a47b2a8460f6a4b6f74150cec01e81ec4f91ba2`  
		Last Modified: Thu, 21 Aug 2025 19:29:47 GMT  
		Size: 5.2 KB (5231 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c24ff7adc0e05f6f22a4f8ef555f2ff812d1f7163cf6c464a47ec51d63c7e0a`  
		Last Modified: Thu, 21 Aug 2025 19:29:42 GMT  
		Size: 131.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56fdd72d2c2ec0f0c49ec37aeb770f4322eae34e5fd9ae7cad866deb034ab419`  
		Last Modified: Thu, 21 Aug 2025 19:29:42 GMT  
		Size: 393.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39b506bff6d6a3eba1015e548dfdfc541813a0a4b100470542d00122fce1153d`  
		Last Modified: Thu, 21 Aug 2025 19:29:42 GMT  
		Size: 4.7 KB (4725 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4535616589f9fb339ba3b5017124a491c078205da02941e21e1b1872f3bd8156`  
		Last Modified: Thu, 21 Aug 2025 19:29:42 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38002f388a488af3a9d147e8a19bb51da830157dde56638182d5d576a00804e8`  
		Last Modified: Thu, 21 Aug 2025 19:29:42 GMT  
		Size: 74.0 KB (73986 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2f986e94f02496027432df29df1e8d0786eb8877f799d5dcfa5230f8d8d1c1a`  
		Last Modified: Thu, 21 Aug 2025 19:29:42 GMT  
		Size: 1.0 KB (1045 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfec2a68583d9cd1b055a37984efc0b633ed3900bddebe84040d2844dc6e7b97`  
		Last Modified: Thu, 21 Aug 2025 19:29:42 GMT  
		Size: 1.7 KB (1708 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kibana:9.1.2` - unknown; unknown

```console
$ docker pull kibana@sha256:bde8e65f17af630cfd0b236c11b34c2eeba9d2f4fc2c9e968cac6ec3ab199981
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5736446 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc2c73c44201842b1dbaf0ccf49670d080d68f1728d23e6153b78461b8c5b7c4`

```dockerfile
```

-	Layers:
	-	`sha256:6a1a64c04325e4d8f9ec3884dd17dbc536452f5b78450f22e55c05319d2e18c0`  
		Last Modified: Thu, 21 Aug 2025 20:11:43 GMT  
		Size: 5.7 MB (5693004 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:98aa29fcf3d64a61f57b398e870373ce0a66e45480c071feb4196af3518568b3`  
		Last Modified: Thu, 21 Aug 2025 20:11:44 GMT  
		Size: 43.4 KB (43442 bytes)  
		MIME: application/vnd.in-toto+json
