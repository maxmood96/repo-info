<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `kibana`

-	[`kibana:7.17.29`](#kibana71729)
-	[`kibana:8.17.10`](#kibana81710)
-	[`kibana:8.18.8`](#kibana8188)
-	[`kibana:8.19.5`](#kibana8195)
-	[`kibana:9.0.8`](#kibana908)
-	[`kibana:9.1.5`](#kibana915)

## `kibana:7.17.29`

```console
$ docker pull kibana@sha256:71efe2f13a43b57627efcc10cf53431d005b17321c0628a0822ce0539839dcf1
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `kibana:7.17.29` - linux; amd64

```console
$ docker pull kibana@sha256:d985cc4486198fddd8d3260a7c55dcd722ad2d5fa5c07675a5d7a006d8f1e0d6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **354.6 MB (354583725 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:38df612d715f4275d5a724053f86af0c516e87cc185529f93dba8f576b1d72df`
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
ADD file:249778a1782b02a1c2bcf9f292f5778d81442a53c3de1958d712f10baf7e0b60 in / 
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
	-	`sha256:4b3ffd8ccb5201a0fc03585952effb4ed2d1ea5e704d2e7330212fb8b16c86a3`  
		Last Modified: Wed, 01 Oct 2025 15:21:59 GMT  
		Size: 29.7 MB (29723147 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebcad3b0e26e11e07c8350412e361f41a960325681ba6cfebd2d8b48784a7bd5`  
		Last Modified: Thu, 09 Oct 2025 21:22:07 GMT  
		Size: 10.1 MB (10104466 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c77820f401e28a6d7ab3f3419c2c2187a25ac6078a0066bc136e487101d6db15`  
		Last Modified: Thu, 09 Oct 2025 21:22:05 GMT  
		Size: 9.5 KB (9523 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77bafede94784c29535da788bd097fd592becb67e45c45550d0b46b7a526ce1c`  
		Last Modified: Thu, 09 Oct 2025 21:22:05 GMT  
		Size: 157.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eec10f902cfd25ddbd95d17d6decfb39946d6fdfb1c57e39763415e9a52dd268`  
		Last Modified: Thu, 09 Oct 2025 21:22:07 GMT  
		Size: 16.5 MB (16460488 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b908041b87ece737cbe9d1c87c7155bba7547546270fb8b3a2cd03ebd7d3a69`  
		Last Modified: Thu, 09 Oct 2025 21:22:05 GMT  
		Size: 5.3 KB (5251 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b0a7b4d4c0eb4dfe767c77526df09d350ef8af8c8ab74d1488feec9fedaf415`  
		Last Modified: Thu, 09 Oct 2025 23:17:35 GMT  
		Size: 298.1 MB (298112525 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2edf6d45654699f9a2453fb6135e47c54e15c736a83cf6e35c6219c8391adaa7`  
		Last Modified: Thu, 09 Oct 2025 21:22:05 GMT  
		Size: 130.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d3494ca2ca5c9fa97fd5ae0e186febfcf1211b61858ab93cda4ffc70c196960`  
		Last Modified: Thu, 09 Oct 2025 21:22:06 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca75e2cbd1ad6633a6406ed949ecba91c270b57d516bef005dfaed5d69453200`  
		Last Modified: Thu, 09 Oct 2025 21:22:06 GMT  
		Size: 4.5 KB (4501 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57a2cfad0a8b6cb4e1997085eee0e0443f8af455f7fac07030ae07b9caf34d12`  
		Last Modified: Thu, 09 Oct 2025 21:22:06 GMT  
		Size: 399.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9a39942146e4d4285e188426d0afe2c7642d108cf4ef55830c8f96ad2b1c727`  
		Last Modified: Thu, 09 Oct 2025 21:22:06 GMT  
		Size: 161.5 KB (161455 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f91c7efcebdb89982e19c676c225a0096505caa6508f016341ba80890791a11a`  
		Last Modified: Thu, 09 Oct 2025 21:22:06 GMT  
		Size: 1.2 KB (1224 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kibana:7.17.29` - unknown; unknown

```console
$ docker pull kibana@sha256:d14d10fb0caba6a4a60c8be75703fc9ed8a89ef337d4b7e45ef34a75ae2aaf6b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3551402 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8cff892d201bb7d3539753f2561919e751c61e8f1b0a160326d602950bfd65b0`

```dockerfile
```

-	Layers:
	-	`sha256:071c15e09dfaa26d2d372d865cc3c90085a4f16246e29b101bf2c061c641cde6`  
		Last Modified: Thu, 09 Oct 2025 23:16:21 GMT  
		Size: 3.5 MB (3506834 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4fb274ecabe44571549a21a136f02375e9baf0e1929f05697a79e98636e0ead5`  
		Last Modified: Thu, 09 Oct 2025 23:15:55 GMT  
		Size: 44.6 KB (44568 bytes)  
		MIME: application/vnd.in-toto+json

### `kibana:7.17.29` - linux; arm64 variant v8

```console
$ docker pull kibana@sha256:1f900309e9d1544770d0cd90b35ca2fd20e94599011bef3cae548f205195e08b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **366.8 MB (366772492 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:63a652d145451db32d29d2423269083d712e9c835b9916c28d5dc5082aec91a3`
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
ADD file:d77dea5c49828eb0de89439d2b631bc8ea27cb9ef774412b56a060ba1673487b in / 
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
	-	`sha256:b8a35db46e38ce87d4e743e1265ff436ed36e01d23246b24a1cbbeaae18ec432`  
		Last Modified: Wed, 01 Oct 2025 15:34:19 GMT  
		Size: 28.9 MB (28861712 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55d7884e42ee962f737877b4a92c5541b5642bea96fadeadb69463a88ee48b96`  
		Last Modified: Thu, 09 Oct 2025 21:26:18 GMT  
		Size: 10.1 MB (10122962 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2e00982d23dc380504049dc6d56c9f7c7d3c13bb175b8d5a80162f564d42fee`  
		Last Modified: Thu, 09 Oct 2025 21:26:00 GMT  
		Size: 9.1 KB (9093 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d93108b493c9562c5fc86d0cfc9f548605ff584cf73966a183795d805a427156`  
		Last Modified: Thu, 09 Oct 2025 21:26:00 GMT  
		Size: 157.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7718d55ae26a253083d5888b7bce5653067d6d051d2f5bc6e3e9360117b9e94e`  
		Last Modified: Thu, 09 Oct 2025 21:26:05 GMT  
		Size: 16.5 MB (16460489 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7647a25ab238faf148c680d33c2b718e136972a0a71f7119f5fc8823bc871f9f`  
		Last Modified: Thu, 09 Oct 2025 21:26:00 GMT  
		Size: 5.2 KB (5247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db7f4b6d02c57109f1e03496c028bca10d3eabe935197d98ba27704914f27640`  
		Last Modified: Thu, 09 Oct 2025 23:18:15 GMT  
		Size: 311.1 MB (311148111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c0f2c553743f6da85b3b9639a364f064767a5b15dcd1b898c10f3ed1c22b055`  
		Last Modified: Thu, 09 Oct 2025 21:26:00 GMT  
		Size: 131.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d915457e6a09b93444c64522a7358fabed890268fb3b6e56b5e11d1cfa409b5f`  
		Last Modified: Thu, 09 Oct 2025 21:26:00 GMT  
		Size: 399.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3bdd9ed79068f1db3d11f07cd0b134e7edc0c232b9d5896bd6b5876f5ab3985a`  
		Last Modified: Thu, 09 Oct 2025 21:26:00 GMT  
		Size: 4.5 KB (4505 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8669a0790ebd7ea0b40361cbb91d4a964c2d01e5984cdd72c05e5c6b3a0da41b`  
		Last Modified: Thu, 09 Oct 2025 21:26:00 GMT  
		Size: 401.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf01772e35d176dc06d8cd6ed11cb75b28a22a10f076de1f9f0723f3a9516cec`  
		Last Modified: Thu, 09 Oct 2025 21:26:00 GMT  
		Size: 158.0 KB (157993 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad7367a3147cdc2e7b00683759cda8979487c5c8d1f83ca9eb667e58c9b9ff20`  
		Last Modified: Thu, 09 Oct 2025 21:26:00 GMT  
		Size: 1.2 KB (1228 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kibana:7.17.29` - unknown; unknown

```console
$ docker pull kibana@sha256:725a6019f17c3f9de74db2219b0b7348b76193329ef220d8fa97d36da7b86823
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3552744 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e19e542e093d97b29eceb172122edfe831f702ec73fd5997f6f484df98b380d`

```dockerfile
```

-	Layers:
	-	`sha256:cd26cd8c8ea9d1afbc55863ef3ac25faa82c1356e94d52cc3f2711607048219d`  
		Last Modified: Thu, 09 Oct 2025 23:15:14 GMT  
		Size: 3.5 MB (3507898 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1823ffd39456686797796a065ea269a56b2506159b0f4c0f7af1749ea61a9359`  
		Last Modified: Thu, 09 Oct 2025 23:15:16 GMT  
		Size: 44.8 KB (44846 bytes)  
		MIME: application/vnd.in-toto+json

## `kibana:8.17.10`

```console
$ docker pull kibana@sha256:9ad0bb5642d555ed98a7c4dac96b932c0d2cf9d69261503018d96c10723f5a6e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `kibana:8.17.10` - linux; amd64

```console
$ docker pull kibana@sha256:ef37d412808571523560626649e927507f2e7105be3e303b74141cef5d70d98b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **404.0 MB (403973888 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e83308f53b32a469632c987ac60640405bd5c56ab7ad6eaf8e78b785b8edc67c`
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
ADD file:249778a1782b02a1c2bcf9f292f5778d81442a53c3de1958d712f10baf7e0b60 in / 
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
	-	`sha256:4b3ffd8ccb5201a0fc03585952effb4ed2d1ea5e704d2e7330212fb8b16c86a3`  
		Last Modified: Wed, 01 Oct 2025 15:21:59 GMT  
		Size: 29.7 MB (29723147 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48e3d0beeea52f14aa486c4502710446dc03ffa1cb6797f5e30f788fedcacbff`  
		Last Modified: Thu, 09 Oct 2025 21:28:04 GMT  
		Size: 10.1 MB (10104464 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19e3bf7d439a6036a811dc3161e94578e9b743d3d68199a95a213c293a0f4e63`  
		Last Modified: Thu, 09 Oct 2025 23:17:50 GMT  
		Size: 347.5 MB (347502658 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c85c490b127e4205bcde246080f1925927e7fee78e765cb3dec6917bad468e0`  
		Last Modified: Thu, 09 Oct 2025 21:28:03 GMT  
		Size: 9.5 KB (9527 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53b27d9e547901af133991e8c86e93cf552c8009137c740b7dbc427fcbb0fc84`  
		Last Modified: Thu, 09 Oct 2025 21:28:04 GMT  
		Size: 16.5 MB (16460491 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c58006eaebce325bedf178143f121cfa44ef574a38df833775f2e31c80518081`  
		Last Modified: Thu, 09 Oct 2025 21:28:03 GMT  
		Size: 5.2 KB (5242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:661c48f0860b30ae6f97409e8e3140a8587993632da5493639def1471d8c93e6`  
		Last Modified: Thu, 09 Oct 2025 21:28:04 GMT  
		Size: 130.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab600dd37f332b71e96d450e3864f2775f4a645b0839f8f7d78e94c255e9998d`  
		Last Modified: Thu, 09 Oct 2025 21:28:04 GMT  
		Size: 394.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fdf434797938030943e2b629bce66919c35c9a7930a3f87dfb7b8c71020eb086`  
		Last Modified: Thu, 09 Oct 2025 21:28:04 GMT  
		Size: 4.7 KB (4727 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:522e0eda738df40576be9039472db5610041c3c7f8626455be47828c99407db8`  
		Last Modified: Thu, 09 Oct 2025 21:28:04 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00df52cd9ff1441e29c5a5952c4c7bdbfc1142891c23e3077973f074f790c400`  
		Last Modified: Thu, 09 Oct 2025 21:28:04 GMT  
		Size: 161.5 KB (161454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08d6743ca215fefb3ff1c40614791a19b4bcc54574f65c6fa6b1277c84239aee`  
		Last Modified: Thu, 09 Oct 2025 21:28:05 GMT  
		Size: 1.2 KB (1224 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kibana:8.17.10` - unknown; unknown

```console
$ docker pull kibana@sha256:275e46db2b9f14c4bc5d6774ab2a63c8a79e29b92103d25b7378f25d098a3456
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4560886 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5864c7df854ddcc47e127b1e7b3f24e55259a9e90d9f9b91159f510ff1407dbd`

```dockerfile
```

-	Layers:
	-	`sha256:5b1e98b61ab68450de5532bbe080a4df0f407f02319ed499d77c392df5f96190`  
		Last Modified: Thu, 09 Oct 2025 23:15:27 GMT  
		Size: 4.5 MB (4520140 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f9806b88c93d2867519f67a6700719e1e7cbaaa62562e95766f052429f2a8210`  
		Last Modified: Thu, 09 Oct 2025 23:15:35 GMT  
		Size: 40.7 KB (40746 bytes)  
		MIME: application/vnd.in-toto+json

### `kibana:8.17.10` - linux; arm64 variant v8

```console
$ docker pull kibana@sha256:68dd757ba69d1a8f6689ef54d2a2e7f4ab4014c27d0a4b373fd0ccdb586d9fc3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **416.2 MB (416175826 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:989578928e417a93b20bfe3b7cbabd5f0d792df0cfd7459856fc6a780b54de13`
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
ADD file:d77dea5c49828eb0de89439d2b631bc8ea27cb9ef774412b56a060ba1673487b in / 
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
	-	`sha256:b8a35db46e38ce87d4e743e1265ff436ed36e01d23246b24a1cbbeaae18ec432`  
		Last Modified: Wed, 01 Oct 2025 15:34:19 GMT  
		Size: 28.9 MB (28861712 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f2450a5dc44dee9d2ba16f837cc6ef2fa9e5a8132b1f06de92f6d955a0034bb`  
		Last Modified: Thu, 09 Oct 2025 21:28:01 GMT  
		Size: 10.1 MB (10122781 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f47b821bf38b2c27b7b3edf5ba068491147abb8c2b684121d8e8798b94d46bd2`  
		Last Modified: Thu, 09 Oct 2025 23:17:31 GMT  
		Size: 360.6 MB (360551596 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b730fd1169053e6cc9cd20b80b5352dfa7b7209af8d9c48bb1ac263185ed9b28`  
		Last Modified: Thu, 09 Oct 2025 21:28:01 GMT  
		Size: 9.1 KB (9100 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abce5f958fd0ef0ff1b12666fb8a37cbccc6272f6e669aebbbbccf234ead40ff`  
		Last Modified: Thu, 09 Oct 2025 21:28:03 GMT  
		Size: 16.5 MB (16460485 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c55510df65a821f97a77823048e9f85fa71d59019b6602bdfa05dcc3c68a1f2a`  
		Last Modified: Thu, 09 Oct 2025 21:28:01 GMT  
		Size: 5.2 KB (5240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8b4ff159564d43909b2cd655cc35c2273d22ddd1a47e4dd65c1050c6c642060`  
		Last Modified: Thu, 09 Oct 2025 21:28:00 GMT  
		Size: 130.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fddf787f8eac8b1fe0f2741d8d1f3062909a96258df13246caf8b1c7b750df5`  
		Last Modified: Thu, 09 Oct 2025 21:28:00 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f043f481fb16f0115913c220bd99001f073da4f15361fd20d833b04d06c8d5a0`  
		Last Modified: Thu, 09 Oct 2025 21:28:01 GMT  
		Size: 4.7 KB (4732 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86da0010b34aff4d19a9c2310ac481c133ab776279118c81d130eb2708741339`  
		Last Modified: Thu, 09 Oct 2025 21:28:00 GMT  
		Size: 400.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:add2af34314cf30e70222946113952de12cbdd7823221c17fe6d89f4e7ed9062`  
		Last Modified: Thu, 09 Oct 2025 21:28:01 GMT  
		Size: 158.0 KB (157998 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94819b8247ad0972b37ef8125a901b5ec35ef482b6e6ab212666cd18fb751551`  
		Last Modified: Thu, 09 Oct 2025 21:28:01 GMT  
		Size: 1.2 KB (1223 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kibana:8.17.10` - unknown; unknown

```console
$ docker pull kibana@sha256:6cba3dccb59bf7a7ac8b97b466a9b9b905f025a5f81d545e7619d4d8edd25b44
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4562196 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1469557d1bfbe5aba110c922e8807cfb959bcb5ac558da5e97b6611c0eb0cb49`

```dockerfile
```

-	Layers:
	-	`sha256:e2580b81e6f7101fce226685301872aa808e7017d10cb7c830a1cf8382755814`  
		Last Modified: Thu, 09 Oct 2025 23:15:40 GMT  
		Size: 4.5 MB (4521204 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7a2a0b32402b0cd41f39aca30b489af70f034d613c31d481a3ae0594c39bda03`  
		Last Modified: Thu, 09 Oct 2025 23:15:41 GMT  
		Size: 41.0 KB (40992 bytes)  
		MIME: application/vnd.in-toto+json

## `kibana:8.18.8`

```console
$ docker pull kibana@sha256:8f0222a60940f7fbf1a160c07821fa69b19a2b4403a7c44327c1f2668a5e0a7d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `kibana:8.18.8` - linux; amd64

```console
$ docker pull kibana@sha256:7dadeeda71e6315fc8917a269bff45cd5191e697cedd6009992de12aaefebf07
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **424.8 MB (424750384 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d28ea8b894825053ab863ae6f0b587f1c6370890281b575395356cd5577d6847`
-	Entrypoint: `["\/bin\/tini","--"]`
-	Default Command: `["\/usr\/local\/bin\/kibana-docker"]`

```dockerfile
# Wed, 01 Oct 2025 13:01:35 GMT
ARG RELEASE
# Wed, 01 Oct 2025 13:01:35 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Oct 2025 13:01:35 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Oct 2025 13:01:35 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 01 Oct 2025 13:01:37 GMT
ADD file:249778a1782b02a1c2bcf9f292f5778d81442a53c3de1958d712f10baf7e0b60 in / 
# Wed, 01 Oct 2025 13:01:37 GMT
CMD ["/bin/bash"]
# Mon, 06 Oct 2025 13:08:19 GMT
EXPOSE map[5601/tcp:{}]
# Mon, 06 Oct 2025 13:08:19 GMT
RUN for iter in {1..10}; do       export DEBIAN_FRONTEND=noninteractive &&       apt-get update  &&       apt-get upgrade -y  &&       apt-get install -y --no-install-recommends       fontconfig fonts-liberation libnss3 curl ca-certificates &&       apt-get clean &&       rm -rf /var/lib/apt/lists/* && exit_code=0 && break || exit_code=$? && echo "apt-get error: retry $iter in 10s" &&       sleep 10;     done;     (exit $exit_code) # buildkit
# Mon, 06 Oct 2025 13:08:19 GMT
COPY --chown=1000:0 /usr/share/kibana /usr/share/kibana # buildkit
# Mon, 06 Oct 2025 13:08:19 GMT
COPY --chown=0:0 /bin/tini /bin/tini # buildkit
# Mon, 06 Oct 2025 13:08:19 GMT
COPY --chown=0:0 /usr/share/fonts/local/NotoSansCJK-Regular.ttc /usr/share/fonts/local/NotoSansCJK-Regular.ttc # buildkit
# Mon, 06 Oct 2025 13:08:19 GMT
RUN fc-cache -v # buildkit
# Mon, 06 Oct 2025 13:08:19 GMT
WORKDIR /usr/share/kibana
# Mon, 06 Oct 2025 13:08:19 GMT
RUN ln -s /usr/share/kibana /opt/kibana # buildkit
# Mon, 06 Oct 2025 13:08:19 GMT
ENV ELASTIC_CONTAINER=true
# Mon, 06 Oct 2025 13:08:19 GMT
ENV PATH=/usr/share/kibana/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 06 Oct 2025 13:08:19 GMT
COPY --chown=1000:0 config/kibana.yml /usr/share/kibana/config/kibana.yml # buildkit
# Mon, 06 Oct 2025 13:08:19 GMT
COPY bin/kibana-docker /usr/local/bin/ # buildkit
# Mon, 06 Oct 2025 13:08:19 GMT
RUN chmod g+ws /usr/share/kibana &&     find /usr/share/kibana -gid 0 -and -not -perm /g+w -exec chmod g+w {} \; # buildkit
# Mon, 06 Oct 2025 13:08:19 GMT
RUN find / -xdev -perm -4000 -exec chmod u-s {} + # buildkit
# Mon, 06 Oct 2025 13:08:19 GMT
RUN userdel -r ubuntu && groupadd --gid 1000 kibana &&     useradd --uid 1000 --gid 1000 -G 0       --home-dir /usr/share/kibana --no-create-home       kibana # buildkit
# Mon, 06 Oct 2025 13:08:19 GMT
LABEL org.label-schema.build-date=2025-10-02T20:20:10.933Z org.label-schema.license=Elastic License org.label-schema.name=Kibana org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/kibana org.label-schema.usage=https://www.elastic.co/guide/en/kibana/reference/index.html org.label-schema.vcs-ref=08ece643671f3ee61a7297b3e67aa99e79a1aef7 org.label-schema.vcs-url=https://github.com/elastic/kibana org.label-schema.vendor=Elastic org.label-schema.version=8.18.8 org.opencontainers.image.created=2025-10-02T20:20:10.933Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/kibana/reference/index.html org.opencontainers.image.licenses=Elastic License org.opencontainers.image.revision=08ece643671f3ee61a7297b3e67aa99e79a1aef7 org.opencontainers.image.source=https://github.com/elastic/kibana org.opencontainers.image.title=Kibana org.opencontainers.image.url=https://www.elastic.co/products/kibana org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=8.18.8
# Mon, 06 Oct 2025 13:08:19 GMT
ENTRYPOINT ["/bin/tini" "--"]
# Mon, 06 Oct 2025 13:08:19 GMT
CMD ["/usr/local/bin/kibana-docker"]
# Mon, 06 Oct 2025 13:08:19 GMT
USER 1000
```

-	Layers:
	-	`sha256:4b3ffd8ccb5201a0fc03585952effb4ed2d1ea5e704d2e7330212fb8b16c86a3`  
		Last Modified: Wed, 01 Oct 2025 15:21:59 GMT  
		Size: 29.7 MB (29723147 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff2da63d6b38c4f9daeae0ec96636a34e52faa334269354e45182b2768a9fe1b`  
		Last Modified: Thu, 09 Oct 2025 21:28:13 GMT  
		Size: 10.1 MB (10104413 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96fbfa82f84aa158fd15f518ecb0cbe5f2aa484350cb716f2ae9562e7fccb4b9`  
		Last Modified: Thu, 09 Oct 2025 23:28:37 GMT  
		Size: 368.3 MB (368279166 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e616da0ae26e8892edde6ce233214ef5d3dce7d4da4915b7c43bdeb3122febbe`  
		Last Modified: Thu, 09 Oct 2025 21:28:01 GMT  
		Size: 9.5 KB (9528 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd3a641f5fa869c0d25cdced0eab01ba8e46192ae0ca391c9930830501ed1924`  
		Last Modified: Thu, 09 Oct 2025 21:28:04 GMT  
		Size: 16.5 MB (16460492 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb2632ae6f1c871e3b16144d240c7989c2978a42c351eecdaa00680442494dde`  
		Last Modified: Thu, 09 Oct 2025 21:28:01 GMT  
		Size: 5.2 KB (5241 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65bb327fe63080d9e9f6a794dd647a3b7eb787067ac4d38e63c96fe2100d80b8`  
		Last Modified: Thu, 09 Oct 2025 21:28:02 GMT  
		Size: 131.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c16dd50ff29e70e739112c98f6d70ad157fdaf1d8ef3345fe9760baa4f3dc95`  
		Last Modified: Thu, 09 Oct 2025 21:28:02 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:749f4dd09735269b37d2cb07940a090267720242f204478a3ec8713070e32f72`  
		Last Modified: Thu, 09 Oct 2025 21:28:02 GMT  
		Size: 4.8 KB (4761 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4502c3de91cc258c17c540e1b480ddfbe38397e2360a5dd41a6539f699c65455`  
		Last Modified: Thu, 09 Oct 2025 21:28:02 GMT  
		Size: 399.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2182a1961211b741be6df96e68d35d3e545840eb6b5cb85a78f524edcc3e961`  
		Last Modified: Thu, 09 Oct 2025 21:28:02 GMT  
		Size: 161.5 KB (161455 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7ffb46e4b1602deb0fb6a9f281938a1c33d0596392aba47c2fda95d117f4dec`  
		Last Modified: Thu, 09 Oct 2025 21:28:01 GMT  
		Size: 1.2 KB (1223 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kibana:8.18.8` - unknown; unknown

```console
$ docker pull kibana@sha256:13016960671d996cb0bc164b20d915eb154134633b38d6e439d26302b1118a73
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4897629 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a490f73f8b32bbc2ccca1717c1dfd200ddc89a9ededacd1f42745d65d0b64e23`

```dockerfile
```

-	Layers:
	-	`sha256:fde1c0c348e7117faac6b178a9a5534a5a84ec7dca4cc65596f10e4e811c7bc1`  
		Last Modified: Thu, 09 Oct 2025 23:15:16 GMT  
		Size: 4.9 MB (4856890 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:41f13542d0a505dc714ebc3ba53821960d791931c380431cbdee0bd8d568348a`  
		Last Modified: Thu, 09 Oct 2025 23:15:17 GMT  
		Size: 40.7 KB (40739 bytes)  
		MIME: application/vnd.in-toto+json

### `kibana:8.18.8` - linux; arm64 variant v8

```console
$ docker pull kibana@sha256:3c5f9bd34260ef54884dd430074e8ad8aeeae36f9a69692051e21366aee9d3f9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **437.0 MB (437031568 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:025b14e16945eadb036ab8ce5265744f5614d2d381d8ac58c1849b8de09782f9`
-	Entrypoint: `["\/bin\/tini","--"]`
-	Default Command: `["\/usr\/local\/bin\/kibana-docker"]`

```dockerfile
# Wed, 01 Oct 2025 13:01:38 GMT
ARG RELEASE
# Wed, 01 Oct 2025 13:01:38 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Oct 2025 13:01:38 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Oct 2025 13:01:38 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 01 Oct 2025 13:01:40 GMT
ADD file:d77dea5c49828eb0de89439d2b631bc8ea27cb9ef774412b56a060ba1673487b in / 
# Wed, 01 Oct 2025 13:01:40 GMT
CMD ["/bin/bash"]
# Mon, 06 Oct 2025 13:08:19 GMT
EXPOSE map[5601/tcp:{}]
# Mon, 06 Oct 2025 13:08:19 GMT
RUN for iter in {1..10}; do       export DEBIAN_FRONTEND=noninteractive &&       apt-get update  &&       apt-get upgrade -y  &&       apt-get install -y --no-install-recommends       fontconfig fonts-liberation libnss3 curl ca-certificates &&       apt-get clean &&       rm -rf /var/lib/apt/lists/* && exit_code=0 && break || exit_code=$? && echo "apt-get error: retry $iter in 10s" &&       sleep 10;     done;     (exit $exit_code) # buildkit
# Mon, 06 Oct 2025 13:08:19 GMT
COPY --chown=1000:0 /usr/share/kibana /usr/share/kibana # buildkit
# Mon, 06 Oct 2025 13:08:19 GMT
COPY --chown=0:0 /bin/tini /bin/tini # buildkit
# Mon, 06 Oct 2025 13:08:19 GMT
COPY --chown=0:0 /usr/share/fonts/local/NotoSansCJK-Regular.ttc /usr/share/fonts/local/NotoSansCJK-Regular.ttc # buildkit
# Mon, 06 Oct 2025 13:08:19 GMT
RUN fc-cache -v # buildkit
# Mon, 06 Oct 2025 13:08:19 GMT
WORKDIR /usr/share/kibana
# Mon, 06 Oct 2025 13:08:19 GMT
RUN ln -s /usr/share/kibana /opt/kibana # buildkit
# Mon, 06 Oct 2025 13:08:19 GMT
ENV ELASTIC_CONTAINER=true
# Mon, 06 Oct 2025 13:08:19 GMT
ENV PATH=/usr/share/kibana/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 06 Oct 2025 13:08:19 GMT
COPY --chown=1000:0 config/kibana.yml /usr/share/kibana/config/kibana.yml # buildkit
# Mon, 06 Oct 2025 13:08:19 GMT
COPY bin/kibana-docker /usr/local/bin/ # buildkit
# Mon, 06 Oct 2025 13:08:19 GMT
RUN chmod g+ws /usr/share/kibana &&     find /usr/share/kibana -gid 0 -and -not -perm /g+w -exec chmod g+w {} \; # buildkit
# Mon, 06 Oct 2025 13:08:19 GMT
RUN find / -xdev -perm -4000 -exec chmod u-s {} + # buildkit
# Mon, 06 Oct 2025 13:08:19 GMT
RUN userdel -r ubuntu && groupadd --gid 1000 kibana &&     useradd --uid 1000 --gid 1000 -G 0       --home-dir /usr/share/kibana --no-create-home       kibana # buildkit
# Mon, 06 Oct 2025 13:08:19 GMT
LABEL org.label-schema.build-date=2025-10-02T20:20:10.933Z org.label-schema.license=Elastic License org.label-schema.name=Kibana org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/kibana org.label-schema.usage=https://www.elastic.co/guide/en/kibana/reference/index.html org.label-schema.vcs-ref=08ece643671f3ee61a7297b3e67aa99e79a1aef7 org.label-schema.vcs-url=https://github.com/elastic/kibana org.label-schema.vendor=Elastic org.label-schema.version=8.18.8 org.opencontainers.image.created=2025-10-02T20:20:10.933Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/kibana/reference/index.html org.opencontainers.image.licenses=Elastic License org.opencontainers.image.revision=08ece643671f3ee61a7297b3e67aa99e79a1aef7 org.opencontainers.image.source=https://github.com/elastic/kibana org.opencontainers.image.title=Kibana org.opencontainers.image.url=https://www.elastic.co/products/kibana org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=8.18.8
# Mon, 06 Oct 2025 13:08:19 GMT
ENTRYPOINT ["/bin/tini" "--"]
# Mon, 06 Oct 2025 13:08:19 GMT
CMD ["/usr/local/bin/kibana-docker"]
# Mon, 06 Oct 2025 13:08:19 GMT
USER 1000
```

-	Layers:
	-	`sha256:b8a35db46e38ce87d4e743e1265ff436ed36e01d23246b24a1cbbeaae18ec432`  
		Last Modified: Wed, 01 Oct 2025 15:34:19 GMT  
		Size: 28.9 MB (28861712 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:666789432768e6b0d3808c7c015f41d81e58ccd20cf20bc9b608ec02c665b38c`  
		Last Modified: Thu, 09 Oct 2025 21:22:12 GMT  
		Size: 10.1 MB (10122777 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6bb2f3c588658898658ccbfabd00ea8b4174b00e6489ed4705c826d6698e4e1`  
		Last Modified: Thu, 09 Oct 2025 22:22:40 GMT  
		Size: 381.4 MB (381407294 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72b71eab8654e85ebd09ad70dae982a705007db8f61155da28e01a0eab29b5bf`  
		Last Modified: Thu, 09 Oct 2025 21:22:11 GMT  
		Size: 9.1 KB (9100 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aeb484b650a5ee4fb0e61b46a38db310a35a21ab8e37ad661d92fb4da186e276`  
		Last Modified: Thu, 09 Oct 2025 21:22:12 GMT  
		Size: 16.5 MB (16460494 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4525ab8f886e5413d23df750f834b5bcbe1e2967d85e4d037b88bf51d3e88d56`  
		Last Modified: Thu, 09 Oct 2025 21:22:11 GMT  
		Size: 5.2 KB (5242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc375f42aa4e6ef81dc6ad67e59e13b4d3198292fba15f39ad031f70caf54404`  
		Last Modified: Thu, 09 Oct 2025 21:22:11 GMT  
		Size: 131.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a9ba176edf8cc060b88ef54a1ece6e6803fef756901bf265da240ef5f11018c`  
		Last Modified: Thu, 09 Oct 2025 21:22:11 GMT  
		Size: 399.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b894c1a257305bea028caeb17abb4f27a59259a4fd04b499dd8a26bebd45ed49`  
		Last Modified: Thu, 09 Oct 2025 21:22:11 GMT  
		Size: 4.8 KB (4766 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58608d90386a5726b130872dcb56434529b11de14c2345d17f96262c51fb97db`  
		Last Modified: Thu, 09 Oct 2025 21:22:11 GMT  
		Size: 399.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:343d38b55a28e01d693f24fee24cd9d71f58c894b5d0ac0512b29a0b606f8c0c`  
		Last Modified: Thu, 09 Oct 2025 21:22:11 GMT  
		Size: 158.0 KB (157998 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9ba89b06cf9de34bfe29a39b3d386b77c76a411b1497b68b115baf5a2613ca2`  
		Last Modified: Thu, 09 Oct 2025 21:22:11 GMT  
		Size: 1.2 KB (1224 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kibana:8.18.8` - unknown; unknown

```console
$ docker pull kibana@sha256:62eff88ab543119dbd4f89db5b62daa82a2d0efea1281f5b355c89a7735fe35d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4898941 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea89152f4426604b8035b27550691da7e4d64259099af4f7a54f9821ee8dba0b`

```dockerfile
```

-	Layers:
	-	`sha256:475f5cf1b1f389015c59e9d271341e963bb272af941867ae070b2ff002c36bf3`  
		Last Modified: Thu, 09 Oct 2025 23:30:15 GMT  
		Size: 4.9 MB (4857954 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:510f84761fd4a54825f8eb192c7506fc1d2cd24b330ac8ca611bce99cf070087`  
		Last Modified: Thu, 09 Oct 2025 23:16:09 GMT  
		Size: 41.0 KB (40987 bytes)  
		MIME: application/vnd.in-toto+json

## `kibana:8.19.5`

```console
$ docker pull kibana@sha256:98d365cbd0a33d31443e28adb548b1cbd0d4e7fd39bb20b59903d0e0f76f5553
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `kibana:8.19.5` - linux; amd64

```console
$ docker pull kibana@sha256:7d7f02fc2b228fb3092e22b46b4edbebf9a1afb838ca67291d0031cfe6d181cb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **436.9 MB (436865586 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b7463c319669529877f455387966eb98c2def77a16b2faa3bbfd00ca607af11`
-	Entrypoint: `["\/bin\/tini","--"]`
-	Default Command: `["\/usr\/local\/bin\/kibana-docker"]`

```dockerfile
# Wed, 01 Oct 2025 13:01:35 GMT
ARG RELEASE
# Wed, 01 Oct 2025 13:01:35 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Oct 2025 13:01:35 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Oct 2025 13:01:35 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 01 Oct 2025 13:01:37 GMT
ADD file:249778a1782b02a1c2bcf9f292f5778d81442a53c3de1958d712f10baf7e0b60 in / 
# Wed, 01 Oct 2025 13:01:37 GMT
CMD ["/bin/bash"]
# Mon, 06 Oct 2025 13:08:09 GMT
EXPOSE map[5601/tcp:{}]
# Mon, 06 Oct 2025 13:08:09 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&       apt-get update &&       apt-get install -y --no-install-recommends fontconfig fonts-liberation libnss3 curl ca-certificates &&       apt-get clean &&       rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 06 Oct 2025 13:08:09 GMT
COPY --chown=1000:0 /usr/share/kibana /usr/share/kibana # buildkit
# Mon, 06 Oct 2025 13:08:09 GMT
COPY --chown=0:0 /bin/tini /bin/tini # buildkit
# Mon, 06 Oct 2025 13:08:09 GMT
COPY --chown=0:0 /usr/share/fonts/local/NotoSansCJK-Regular.ttc /usr/share/fonts/local/NotoSansCJK-Regular.ttc # buildkit
# Mon, 06 Oct 2025 13:08:09 GMT
RUN fc-cache -v # buildkit
# Mon, 06 Oct 2025 13:08:09 GMT
WORKDIR /usr/share/kibana
# Mon, 06 Oct 2025 13:08:09 GMT
RUN ln -s /usr/share/kibana /opt/kibana # buildkit
# Mon, 06 Oct 2025 13:08:09 GMT
ENV ELASTIC_CONTAINER=true
# Mon, 06 Oct 2025 13:08:09 GMT
ENV PATH=/usr/share/kibana/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 06 Oct 2025 13:08:09 GMT
COPY --chown=1000:0 config/kibana.yml /usr/share/kibana/config/kibana.yml # buildkit
# Mon, 06 Oct 2025 13:08:09 GMT
COPY bin/kibana-docker /usr/local/bin/ # buildkit
# Mon, 06 Oct 2025 13:08:09 GMT
RUN chmod g+ws /usr/share/kibana &&     find /usr/share/kibana -gid 0 -and -not -perm /g+w -exec chmod g+w {} \; # buildkit
# Mon, 06 Oct 2025 13:08:09 GMT
RUN find / -xdev -perm -4000 -exec chmod u-s {} + # buildkit
# Mon, 06 Oct 2025 13:08:09 GMT
RUN userdel -r ubuntu && groupadd --gid 1000 kibana &&     useradd --uid 1000 --gid 1000 -G 0       --home-dir /usr/share/kibana --no-create-home       kibana # buildkit
# Mon, 06 Oct 2025 13:08:09 GMT
LABEL org.label-schema.build-date=2025-10-03T16:17:52.399Z org.label-schema.license=Elastic License org.label-schema.name=Kibana org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/kibana org.label-schema.usage=https://www.elastic.co/guide/en/kibana/reference/index.html org.label-schema.vcs-ref=2ceb68bd03a3cc20c26495ec986ed4f244589d69 org.label-schema.vcs-url=https://github.com/elastic/kibana org.label-schema.vendor=Elastic org.label-schema.version=8.19.5 org.opencontainers.image.created=2025-10-03T16:17:52.399Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/kibana/reference/index.html org.opencontainers.image.licenses=Elastic License org.opencontainers.image.revision=2ceb68bd03a3cc20c26495ec986ed4f244589d69 org.opencontainers.image.source=https://github.com/elastic/kibana org.opencontainers.image.title=Kibana org.opencontainers.image.url=https://www.elastic.co/products/kibana org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=8.19.5
# Mon, 06 Oct 2025 13:08:09 GMT
ENTRYPOINT ["/bin/tini" "--"]
# Mon, 06 Oct 2025 13:08:09 GMT
CMD ["/usr/local/bin/kibana-docker"]
# Mon, 06 Oct 2025 13:08:09 GMT
USER 1000
```

-	Layers:
	-	`sha256:4b3ffd8ccb5201a0fc03585952effb4ed2d1ea5e704d2e7330212fb8b16c86a3`  
		Last Modified: Wed, 01 Oct 2025 15:21:59 GMT  
		Size: 29.7 MB (29723147 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19a47aaa7525d79b53da90a7177553bb4d4c118c12357a3c935bd20eff99156e`  
		Last Modified: Thu, 09 Oct 2025 21:28:26 GMT  
		Size: 9.4 MB (9432004 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92d94b75db1a135c9c0691fcf003741e96bda67125133230dededd9743095eda`  
		Last Modified: Thu, 09 Oct 2025 22:22:20 GMT  
		Size: 381.1 MB (381066748 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:078d2fda80471be392d34216f3cb6768ae68f248368f1fbb890435a1004fc070`  
		Last Modified: Thu, 09 Oct 2025 21:28:01 GMT  
		Size: 9.5 KB (9526 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d5ea6953a637327e9e28685cea14b8fb982411166234c503011dc52a1c1f3e8`  
		Last Modified: Thu, 09 Oct 2025 21:28:03 GMT  
		Size: 16.5 MB (16460483 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54ee27d6fb7b5e5585d07eb92ea618882d73abf3877ec12641b568a6474f4ab3`  
		Last Modified: Thu, 09 Oct 2025 21:28:02 GMT  
		Size: 5.2 KB (5240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3290bba65f8498b40e0689c3db2f0f98cf6d37e4fadb0f54b9b4fee2151a39b5`  
		Last Modified: Thu, 09 Oct 2025 21:28:02 GMT  
		Size: 131.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:daab443809bc85f32f1fa18068304aac127e07e7299b14478061491f079ee7b6`  
		Last Modified: Thu, 09 Oct 2025 21:28:02 GMT  
		Size: 394.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bcc94e31a4f9f344b52bc5eedd0e049c9b6221c145578d1e47a4b4713ebcf9be`  
		Last Modified: Thu, 09 Oct 2025 21:28:03 GMT  
		Size: 4.8 KB (4808 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0432501b5c2fb1fe8e7f411893173c3accbabdac2b79771d564c37031494170`  
		Last Modified: Thu, 09 Oct 2025 21:28:03 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bc8044d4aa8bb748724063a27755ab00946790cc984d4ac89ee2cb1905adc65`  
		Last Modified: Thu, 09 Oct 2025 21:28:03 GMT  
		Size: 161.5 KB (161454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38926580b49b97d657e06cf7286f4ff8481027dd34e22cdde199ed4375137eee`  
		Last Modified: Thu, 09 Oct 2025 21:28:03 GMT  
		Size: 1.2 KB (1223 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kibana:8.19.5` - unknown; unknown

```console
$ docker pull kibana@sha256:c979bb577cef1ef163f8dda1f26b0d170df948534c1a63ccb947d87e4eeb6c93
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4911414 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd543fe2a902ddfb502bcdc6ea963cb6cc60bdc4a018e19fda3fb00076acf1f7`

```dockerfile
```

-	Layers:
	-	`sha256:09d251f2082a0c1d7b7f700e122481ba18fd3ae56fd4522d5014a7270582821d`  
		Last Modified: Thu, 09 Oct 2025 23:15:26 GMT  
		Size: 4.9 MB (4870464 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:db44b2be4263e2a9a52095084f75638f4d9e2ce5a470887fbdfefaeb80b9406d`  
		Last Modified: Thu, 09 Oct 2025 23:15:27 GMT  
		Size: 41.0 KB (40950 bytes)  
		MIME: application/vnd.in-toto+json

### `kibana:8.19.5` - linux; arm64 variant v8

```console
$ docker pull kibana@sha256:58877692beb007843d6e03bc441d450fde794310c7fdc15d987abe43b489819e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **448.9 MB (448878100 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e1119d916a55b6672a2bcc3a186e4fd16d48b0f5a46bb357ea4cbdcfe18e9bc9`
-	Entrypoint: `["\/bin\/tini","--"]`
-	Default Command: `["\/usr\/local\/bin\/kibana-docker"]`

```dockerfile
# Wed, 01 Oct 2025 13:01:38 GMT
ARG RELEASE
# Wed, 01 Oct 2025 13:01:38 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Oct 2025 13:01:38 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Oct 2025 13:01:38 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 01 Oct 2025 13:01:40 GMT
ADD file:d77dea5c49828eb0de89439d2b631bc8ea27cb9ef774412b56a060ba1673487b in / 
# Wed, 01 Oct 2025 13:01:40 GMT
CMD ["/bin/bash"]
# Mon, 06 Oct 2025 13:08:09 GMT
EXPOSE map[5601/tcp:{}]
# Mon, 06 Oct 2025 13:08:09 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&       apt-get update &&       apt-get install -y --no-install-recommends fontconfig fonts-liberation libnss3 curl ca-certificates &&       apt-get clean &&       rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 06 Oct 2025 13:08:09 GMT
COPY --chown=1000:0 /usr/share/kibana /usr/share/kibana # buildkit
# Mon, 06 Oct 2025 13:08:09 GMT
COPY --chown=0:0 /bin/tini /bin/tini # buildkit
# Mon, 06 Oct 2025 13:08:09 GMT
COPY --chown=0:0 /usr/share/fonts/local/NotoSansCJK-Regular.ttc /usr/share/fonts/local/NotoSansCJK-Regular.ttc # buildkit
# Mon, 06 Oct 2025 13:08:09 GMT
RUN fc-cache -v # buildkit
# Mon, 06 Oct 2025 13:08:09 GMT
WORKDIR /usr/share/kibana
# Mon, 06 Oct 2025 13:08:09 GMT
RUN ln -s /usr/share/kibana /opt/kibana # buildkit
# Mon, 06 Oct 2025 13:08:09 GMT
ENV ELASTIC_CONTAINER=true
# Mon, 06 Oct 2025 13:08:09 GMT
ENV PATH=/usr/share/kibana/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 06 Oct 2025 13:08:09 GMT
COPY --chown=1000:0 config/kibana.yml /usr/share/kibana/config/kibana.yml # buildkit
# Mon, 06 Oct 2025 13:08:09 GMT
COPY bin/kibana-docker /usr/local/bin/ # buildkit
# Mon, 06 Oct 2025 13:08:09 GMT
RUN chmod g+ws /usr/share/kibana &&     find /usr/share/kibana -gid 0 -and -not -perm /g+w -exec chmod g+w {} \; # buildkit
# Mon, 06 Oct 2025 13:08:09 GMT
RUN find / -xdev -perm -4000 -exec chmod u-s {} + # buildkit
# Mon, 06 Oct 2025 13:08:09 GMT
RUN userdel -r ubuntu && groupadd --gid 1000 kibana &&     useradd --uid 1000 --gid 1000 -G 0       --home-dir /usr/share/kibana --no-create-home       kibana # buildkit
# Mon, 06 Oct 2025 13:08:09 GMT
LABEL org.label-schema.build-date=2025-10-03T16:17:52.399Z org.label-schema.license=Elastic License org.label-schema.name=Kibana org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/kibana org.label-schema.usage=https://www.elastic.co/guide/en/kibana/reference/index.html org.label-schema.vcs-ref=2ceb68bd03a3cc20c26495ec986ed4f244589d69 org.label-schema.vcs-url=https://github.com/elastic/kibana org.label-schema.vendor=Elastic org.label-schema.version=8.19.5 org.opencontainers.image.created=2025-10-03T16:17:52.399Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/kibana/reference/index.html org.opencontainers.image.licenses=Elastic License org.opencontainers.image.revision=2ceb68bd03a3cc20c26495ec986ed4f244589d69 org.opencontainers.image.source=https://github.com/elastic/kibana org.opencontainers.image.title=Kibana org.opencontainers.image.url=https://www.elastic.co/products/kibana org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=8.19.5
# Mon, 06 Oct 2025 13:08:09 GMT
ENTRYPOINT ["/bin/tini" "--"]
# Mon, 06 Oct 2025 13:08:09 GMT
CMD ["/usr/local/bin/kibana-docker"]
# Mon, 06 Oct 2025 13:08:09 GMT
USER 1000
```

-	Layers:
	-	`sha256:b8a35db46e38ce87d4e743e1265ff436ed36e01d23246b24a1cbbeaae18ec432`  
		Last Modified: Wed, 01 Oct 2025 15:34:19 GMT  
		Size: 28.9 MB (28861712 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f192a4b06dc264fde56cee4fed4970c626e27206af77fc62d94f37ecc8bc6913`  
		Last Modified: Thu, 09 Oct 2025 21:22:32 GMT  
		Size: 9.4 MB (9446328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de419828dc6d747f141c5e20150ea919626d70c53f1bcb172ec4d4d2c4f095ac`  
		Last Modified: Thu, 09 Oct 2025 23:33:29 GMT  
		Size: 393.9 MB (393930241 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c009dc99fa03fef25a37cb200f10bce526b38ba4a0a75e47cef74af2b7964a80`  
		Last Modified: Thu, 09 Oct 2025 21:22:31 GMT  
		Size: 9.1 KB (9098 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49e7cef4fadfd13406621fa6a1fed314c05a22bfd0c688afb72cfc5e6ff3060c`  
		Last Modified: Thu, 09 Oct 2025 21:22:33 GMT  
		Size: 16.5 MB (16460495 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0fd9968dae2cc059eb481fcdea5d2f5ff8ea0f46bcd7b9c826ce45da91a5ed2`  
		Last Modified: Thu, 09 Oct 2025 21:22:31 GMT  
		Size: 5.2 KB (5244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5456437db06dae899730773a85609f2a35cdcdea4e30187ffce8f8f28740bfe`  
		Last Modified: Thu, 09 Oct 2025 21:22:31 GMT  
		Size: 131.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37995f2a69c06ca109932842548a3409f561ed42489d0dffd67f8bc77adfc84c`  
		Last Modified: Thu, 09 Oct 2025 21:22:31 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4fdb044d3c0b7c3a4b3d549b3f66f3d3a153cb477babb24edcab396f825ac34d`  
		Last Modified: Thu, 09 Oct 2025 21:22:31 GMT  
		Size: 4.8 KB (4809 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06a45d803489c326f84c16ff3251b5920cd11dfc6d9d72212ed81aeb2e6ed072`  
		Last Modified: Thu, 09 Oct 2025 21:22:31 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23b0f20c98cd38eda32751fee8952bc8812951aa9f1d64137865a20cfd2a3475`  
		Last Modified: Thu, 09 Oct 2025 21:22:31 GMT  
		Size: 158.0 KB (157993 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4b2dc949658c9f2828d76ed478903dc8420998653c58f202aa388ddfe5349c0`  
		Last Modified: Thu, 09 Oct 2025 21:22:31 GMT  
		Size: 1.2 KB (1223 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kibana:8.19.5` - unknown; unknown

```console
$ docker pull kibana@sha256:939e5b783598c63cf824ca7a0ae5957ca354aa05fc20dbc9d35ad8cf96f6ccbd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4912727 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d5d63e5caffb8ada66263b95f77e1d8e01a399d146a2f933dc2f04ddeec1a88b`

```dockerfile
```

-	Layers:
	-	`sha256:b717c699956dd069bc79259b552c649d178374e50961b4a786bf09f938575994`  
		Last Modified: Thu, 09 Oct 2025 23:15:31 GMT  
		Size: 4.9 MB (4871528 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:420b905701494deaa27a501d6648d9d051853d3b27b8511eba81bc0b6ed174bf`  
		Last Modified: Thu, 09 Oct 2025 23:15:32 GMT  
		Size: 41.2 KB (41199 bytes)  
		MIME: application/vnd.in-toto+json

## `kibana:9.0.8`

```console
$ docker pull kibana@sha256:5bb592a2e5ca000241ce23e794a70c63ccef9455706c8b61f65361fd514167fb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `kibana:9.0.8` - linux; amd64

```console
$ docker pull kibana@sha256:ae6991552bf33bacb39ae0cd62fdb2655cd6b17d9f69c27181fda21e805adf85
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **438.7 MB (438681313 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c133adab6b563edc9a3af440c1994d8396797ceb5ade01fec7acace7e721e6f9`
-	Entrypoint: `["\/bin\/tini","--"]`
-	Default Command: `["\/usr\/local\/bin\/kibana-docker"]`

```dockerfile
# Mon, 06 Oct 2025 11:09:04 GMT
LABEL maintainer="Red Hat, Inc."
# Mon, 06 Oct 2025 11:09:04 GMT
LABEL vendor="Red Hat, Inc."
# Mon, 06 Oct 2025 11:09:04 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Mon, 06 Oct 2025 11:09:04 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.6"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Mon, 06 Oct 2025 11:09:04 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Mon, 06 Oct 2025 11:09:04 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Mon, 06 Oct 2025 11:09:04 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 06 Oct 2025 11:09:04 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 06 Oct 2025 11:09:04 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Mon, 06 Oct 2025 11:09:04 GMT
LABEL io.openshift.expose-services=""
# Mon, 06 Oct 2025 11:09:04 GMT
LABEL io.openshift.tags="minimal rhel9"
# Mon, 06 Oct 2025 11:09:04 GMT
ENV container oci
# Mon, 06 Oct 2025 11:09:04 GMT
COPY dir:f15650dcc2939ee0c30865212b61e6718fd6c24de4e7967bf7b651b8f0b24352 in /      
# Mon, 06 Oct 2025 11:09:04 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Mon, 06 Oct 2025 11:09:04 GMT
CMD ["/bin/bash"]
# Mon, 06 Oct 2025 11:09:04 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /usr/share/buildinfo/content-sets.json      
# Mon, 06 Oct 2025 11:09:04 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /root/buildinfo/content_manifests/content-sets.json      
# Mon, 06 Oct 2025 11:09:04 GMT
COPY file:16bf5aac480286f91e3031d4f1acb4e76fb8c3be38d180e4713a0efdc39d6bad in /root/buildinfo/labels.json      
# Mon, 06 Oct 2025 11:09:04 GMT
LABEL "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="d1b15a34ce69ea214e1d32f1f501304f6b8b8c59" "org.opencontainers.image.revision"="d1b15a34ce69ea214e1d32f1f501304f6b8b8c59" "build-date"="2025-10-15T08:06:12Z" "release"="1760515502"org.opencontainers.image.revision=d1b15a34ce69ea214e1d32f1f501304f6b8b8c59
# Mon, 06 Oct 2025 11:09:04 GMT
EXPOSE map[5601/tcp:{}]
# Mon, 06 Oct 2025 11:09:04 GMT
RUN microdnf install --setopt=tsflags=nodocs -y       fontconfig liberation-fonts-common freetype shadow-utils nss findutils &&       microdnf clean all # buildkit
# Mon, 06 Oct 2025 11:09:04 GMT
COPY --chown=1000:0 /usr/share/kibana /usr/share/kibana # buildkit
# Mon, 06 Oct 2025 11:09:04 GMT
COPY --chown=0:0 /bin/tini /bin/tini # buildkit
# Mon, 06 Oct 2025 11:09:04 GMT
COPY --chown=0:0 /usr/share/fonts/local/NotoSansCJK-Regular.ttc /usr/share/fonts/local/NotoSansCJK-Regular.ttc # buildkit
# Mon, 06 Oct 2025 11:09:04 GMT
RUN fc-cache -v # buildkit
# Mon, 06 Oct 2025 11:09:04 GMT
WORKDIR /usr/share/kibana
# Mon, 06 Oct 2025 11:09:04 GMT
RUN ln -s /usr/share/kibana /opt/kibana # buildkit
# Mon, 06 Oct 2025 11:09:04 GMT
ENV ELASTIC_CONTAINER=true
# Mon, 06 Oct 2025 11:09:04 GMT
ENV PATH=/usr/share/kibana/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 06 Oct 2025 11:09:04 GMT
COPY --chown=1000:0 config/kibana.yml /usr/share/kibana/config/kibana.yml # buildkit
# Mon, 06 Oct 2025 11:09:04 GMT
COPY bin/kibana-docker /usr/local/bin/ # buildkit
# Mon, 06 Oct 2025 11:09:04 GMT
RUN chmod g+ws /usr/share/kibana &&     find /usr/share/kibana -gid 0 -and -not -perm /g+w -exec chmod g+w {} \; # buildkit
# Mon, 06 Oct 2025 11:09:04 GMT
RUN find / -xdev -perm -4000 -exec chmod u-s {} + # buildkit
# Mon, 06 Oct 2025 11:09:04 GMT
RUN groupadd --gid 1000 kibana &&     useradd --uid 1000 --gid 1000 -G 0       --home-dir /usr/share/kibana --no-create-home       kibana # buildkit
# Mon, 06 Oct 2025 11:09:04 GMT
LABEL org.label-schema.build-date=2025-10-02T20:34:56.884Z org.label-schema.license=Elastic License org.label-schema.name=Kibana org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/kibana org.label-schema.usage=https://www.elastic.co/guide/en/kibana/reference/index.html org.label-schema.vcs-ref=16276053a4c29c654785bb35bce6b512c15435b1 org.label-schema.vcs-url=https://github.com/elastic/kibana org.label-schema.vendor=Elastic org.label-schema.version=9.0.8 org.opencontainers.image.created=2025-10-02T20:34:56.884Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/kibana/reference/index.html org.opencontainers.image.licenses=Elastic License org.opencontainers.image.revision=16276053a4c29c654785bb35bce6b512c15435b1 org.opencontainers.image.source=https://github.com/elastic/kibana org.opencontainers.image.title=Kibana org.opencontainers.image.url=https://www.elastic.co/products/kibana org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=9.0.8
# Mon, 06 Oct 2025 11:09:04 GMT
LABEL name=Kibana maintainer=infra@elastic.co vendor=Elastic version=9.0.8 release=1 summary=Kibana description=Your window into the Elastic Stack.
# Mon, 06 Oct 2025 11:09:04 GMT
RUN mkdir /licenses && ln LICENSE.txt /licenses/LICENSE # buildkit
# Mon, 06 Oct 2025 11:09:04 GMT
ENTRYPOINT ["/bin/tini" "--"]
# Mon, 06 Oct 2025 11:09:04 GMT
CMD ["/usr/local/bin/kibana-docker"]
# Mon, 06 Oct 2025 11:09:04 GMT
USER 1000
```

-	Layers:
	-	`sha256:2920d84eafa0cf94806ab58f0a2124f7b2d35bcbb06fc89a9106dcc28efe397a`  
		Last Modified: Wed, 15 Oct 2025 09:03:15 GMT  
		Size: 39.7 MB (39653524 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b939ac8132c2cf44440ce0b08bf9c1274560898dbebec18e6ad6a44298759c19`  
		Last Modified: Thu, 16 Oct 2025 19:36:16 GMT  
		Size: 19.5 MB (19530289 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6eafc1882bcf7ee11d5f0480f573941699ab6b383c3dc01239dcdab73599b63b`  
		Last Modified: Thu, 16 Oct 2025 20:12:57 GMT  
		Size: 362.9 MB (362938760 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36a6479214344fb5d581cb2239a25c842dc244acc1c60641ef3b5add92a9871a`  
		Last Modified: Thu, 16 Oct 2025 19:36:14 GMT  
		Size: 9.5 KB (9533 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:edabf97bc1c3006c9e1a9c0d9dc275dc682d7138687d2deb97531fcc07b0842e`  
		Last Modified: Thu, 16 Oct 2025 19:36:16 GMT  
		Size: 16.5 MB (16460484 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b027235fbd489b008b963700c49aa1bcfb0330beadcd33d7426426b5ca66e91e`  
		Last Modified: Thu, 16 Oct 2025 19:36:15 GMT  
		Size: 5.2 KB (5229 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76dd43074c841c1f3567b71fc6f131ccbd8d3ee423dfa9116a68c00482c9882e`  
		Last Modified: Thu, 16 Oct 2025 19:36:14 GMT  
		Size: 132.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66c7339dd9855c11e48d1d9d0fb820192c8f930baa5d4d58fc84347c57c471ae`  
		Last Modified: Thu, 16 Oct 2025 19:36:15 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d52e31b29a56e9dedf0c7358bb92bc6a3b9b38c3ca101996d4952f3c528370df`  
		Last Modified: Thu, 16 Oct 2025 19:36:15 GMT  
		Size: 4.7 KB (4688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fdf18e4d76c008845321d7759b76ef50888edd661555a5887dcae0dbddc93660`  
		Last Modified: Thu, 16 Oct 2025 19:36:13 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ef2d7015a0203b352fca1a59ac5f3f655ee0630fa57f2eead5e39186514d388`  
		Last Modified: Thu, 16 Oct 2025 19:36:13 GMT  
		Size: 75.1 KB (75100 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08e183862ce91430728406b7beed6acefadfc53c7de97258e70237b4664cca3a`  
		Last Modified: Thu, 16 Oct 2025 19:36:13 GMT  
		Size: 1.0 KB (1044 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a0d9dae8ec0bfb9a06c952274e8ef967602226dce0663a09ee2bbae24e290b7`  
		Last Modified: Thu, 16 Oct 2025 19:36:13 GMT  
		Size: 1.7 KB (1706 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kibana:9.0.8` - unknown; unknown

```console
$ docker pull kibana@sha256:af4113a1cbc24339beecb8e3afb13a31f6dd6d9a3d87aa3472eb78b210221393
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5609860 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ad166f9f52da6d71c74bc1a6b1500a7e0d04fccfc8515fbc24d1b9609405e0e`

```dockerfile
```

-	Layers:
	-	`sha256:a84e2daf83325b4673b3e24969379466922d213a164af1e5e622fbdce954436e`  
		Last Modified: Thu, 16 Oct 2025 23:11:20 GMT  
		Size: 5.6 MB (5566591 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1a64c612f04ca6955b7f237d2c737223faf01f9d6407978b80f114ba08539196`  
		Last Modified: Thu, 16 Oct 2025 23:11:21 GMT  
		Size: 43.3 KB (43269 bytes)  
		MIME: application/vnd.in-toto+json

### `kibana:9.0.8` - linux; arm64 variant v8

```console
$ docker pull kibana@sha256:b5c1a587003eb6b85431d34cd9669dcc85cc381c124afa072ba001c3f1008fa6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **450.0 MB (450025118 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e5368502ca9bda98bca7b0746379914d707587cc3412e633574f78887076b09`
-	Entrypoint: `["\/bin\/tini","--"]`
-	Default Command: `["\/usr\/local\/bin\/kibana-docker"]`

```dockerfile
# Mon, 06 Oct 2025 11:09:04 GMT
LABEL maintainer="Red Hat, Inc."
# Mon, 06 Oct 2025 11:09:04 GMT
LABEL vendor="Red Hat, Inc."
# Mon, 06 Oct 2025 11:09:04 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Mon, 06 Oct 2025 11:09:04 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.6"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Mon, 06 Oct 2025 11:09:04 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Mon, 06 Oct 2025 11:09:04 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Mon, 06 Oct 2025 11:09:04 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 06 Oct 2025 11:09:04 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 06 Oct 2025 11:09:04 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Mon, 06 Oct 2025 11:09:04 GMT
LABEL io.openshift.expose-services=""
# Mon, 06 Oct 2025 11:09:04 GMT
LABEL io.openshift.tags="minimal rhel9"
# Mon, 06 Oct 2025 11:09:04 GMT
ENV container oci
# Mon, 06 Oct 2025 11:09:04 GMT
COPY dir:a993e2e2ad3cf26c4ca4b583710869f381ee3e7df7d41715015a96348230e455 in /      
# Mon, 06 Oct 2025 11:09:04 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Mon, 06 Oct 2025 11:09:04 GMT
CMD ["/bin/bash"]
# Mon, 06 Oct 2025 11:09:04 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /usr/share/buildinfo/content-sets.json      
# Mon, 06 Oct 2025 11:09:04 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /root/buildinfo/content_manifests/content-sets.json      
# Mon, 06 Oct 2025 11:09:04 GMT
COPY file:85de04d2096a64069474160b53ad5f2cfb18b7e3f3ec2a8d26b3946f32e004c9 in /root/buildinfo/labels.json      
# Mon, 06 Oct 2025 11:09:04 GMT
LABEL "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="d1b15a34ce69ea214e1d32f1f501304f6b8b8c59" "org.opencontainers.image.revision"="d1b15a34ce69ea214e1d32f1f501304f6b8b8c59" "build-date"="2025-10-15T08:10:36Z" "release"="1760515502"org.opencontainers.image.revision=d1b15a34ce69ea214e1d32f1f501304f6b8b8c59
# Mon, 06 Oct 2025 11:09:04 GMT
EXPOSE map[5601/tcp:{}]
# Mon, 06 Oct 2025 11:09:04 GMT
RUN microdnf install --setopt=tsflags=nodocs -y       fontconfig liberation-fonts-common freetype shadow-utils nss findutils &&       microdnf clean all # buildkit
# Mon, 06 Oct 2025 11:09:04 GMT
COPY --chown=1000:0 /usr/share/kibana /usr/share/kibana # buildkit
# Mon, 06 Oct 2025 11:09:04 GMT
COPY --chown=0:0 /bin/tini /bin/tini # buildkit
# Mon, 06 Oct 2025 11:09:04 GMT
COPY --chown=0:0 /usr/share/fonts/local/NotoSansCJK-Regular.ttc /usr/share/fonts/local/NotoSansCJK-Regular.ttc # buildkit
# Mon, 06 Oct 2025 11:09:04 GMT
RUN fc-cache -v # buildkit
# Mon, 06 Oct 2025 11:09:04 GMT
WORKDIR /usr/share/kibana
# Mon, 06 Oct 2025 11:09:04 GMT
RUN ln -s /usr/share/kibana /opt/kibana # buildkit
# Mon, 06 Oct 2025 11:09:04 GMT
ENV ELASTIC_CONTAINER=true
# Mon, 06 Oct 2025 11:09:04 GMT
ENV PATH=/usr/share/kibana/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 06 Oct 2025 11:09:04 GMT
COPY --chown=1000:0 config/kibana.yml /usr/share/kibana/config/kibana.yml # buildkit
# Mon, 06 Oct 2025 11:09:04 GMT
COPY bin/kibana-docker /usr/local/bin/ # buildkit
# Mon, 06 Oct 2025 11:09:04 GMT
RUN chmod g+ws /usr/share/kibana &&     find /usr/share/kibana -gid 0 -and -not -perm /g+w -exec chmod g+w {} \; # buildkit
# Mon, 06 Oct 2025 11:09:04 GMT
RUN find / -xdev -perm -4000 -exec chmod u-s {} + # buildkit
# Mon, 06 Oct 2025 11:09:04 GMT
RUN groupadd --gid 1000 kibana &&     useradd --uid 1000 --gid 1000 -G 0       --home-dir /usr/share/kibana --no-create-home       kibana # buildkit
# Mon, 06 Oct 2025 11:09:04 GMT
LABEL org.label-schema.build-date=2025-10-02T20:34:56.884Z org.label-schema.license=Elastic License org.label-schema.name=Kibana org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/kibana org.label-schema.usage=https://www.elastic.co/guide/en/kibana/reference/index.html org.label-schema.vcs-ref=16276053a4c29c654785bb35bce6b512c15435b1 org.label-schema.vcs-url=https://github.com/elastic/kibana org.label-schema.vendor=Elastic org.label-schema.version=9.0.8 org.opencontainers.image.created=2025-10-02T20:34:56.884Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/kibana/reference/index.html org.opencontainers.image.licenses=Elastic License org.opencontainers.image.revision=16276053a4c29c654785bb35bce6b512c15435b1 org.opencontainers.image.source=https://github.com/elastic/kibana org.opencontainers.image.title=Kibana org.opencontainers.image.url=https://www.elastic.co/products/kibana org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=9.0.8
# Mon, 06 Oct 2025 11:09:04 GMT
LABEL name=Kibana maintainer=infra@elastic.co vendor=Elastic version=9.0.8 release=1 summary=Kibana description=Your window into the Elastic Stack.
# Mon, 06 Oct 2025 11:09:04 GMT
RUN mkdir /licenses && ln LICENSE.txt /licenses/LICENSE # buildkit
# Mon, 06 Oct 2025 11:09:04 GMT
ENTRYPOINT ["/bin/tini" "--"]
# Mon, 06 Oct 2025 11:09:04 GMT
CMD ["/usr/local/bin/kibana-docker"]
# Mon, 06 Oct 2025 11:09:04 GMT
USER 1000
```

-	Layers:
	-	`sha256:2602e1c5e8830fe80a6207359ce01e6c9b7d6848be663c4df1e03c724149b8a6`  
		Last Modified: Wed, 15 Oct 2025 09:30:32 GMT  
		Size: 37.9 MB (37896281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41c17c8390c372ced83dac1cdde6caf4b64e159636bed75cf104bccbc30432f8`  
		Last Modified: Thu, 16 Oct 2025 19:35:20 GMT  
		Size: 19.5 MB (19487748 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:663d6980ed1d0689a96e0dd1e2dbf7e4ba4ddf249e2f9a1a581f527dd41c1a0f`  
		Last Modified: Thu, 16 Oct 2025 20:15:51 GMT  
		Size: 376.1 MB (376083889 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:177ca95264f50c52c9a1df1884c5f8982a0574d83b68bd0cf8af3af97a60d476`  
		Last Modified: Thu, 16 Oct 2025 19:35:18 GMT  
		Size: 9.1 KB (9100 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5af2a397751155bdbdeb0db6504c1735ff1d7922dfa7649e6ed3a49e84ac3e4f`  
		Last Modified: Thu, 16 Oct 2025 19:35:21 GMT  
		Size: 16.5 MB (16460493 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40da15d629d249eefd58371d3151458e2faa2d5f6a6d1f6702424583640a3006`  
		Last Modified: Thu, 16 Oct 2025 19:35:18 GMT  
		Size: 5.2 KB (5224 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bed43b5d8e98d033a695c6e1af9e56f8966e1d9d9b25a4a6393595ace831b7c0`  
		Last Modified: Thu, 16 Oct 2025 19:35:18 GMT  
		Size: 131.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fcde4f9cb33af36b031433a5547e5fadfbc5e14da19feddfa9b2920facac691b`  
		Last Modified: Thu, 16 Oct 2025 19:35:18 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8fd744800c3dc3030eeff554ce43c594e14c082bdd3416f14ac1a8462beb264`  
		Last Modified: Thu, 16 Oct 2025 19:35:19 GMT  
		Size: 4.7 KB (4688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c52e242b4945198d11fc2cb490d63bf2b74dd3a803bca1ab1e826f6389c8b068`  
		Last Modified: Thu, 16 Oct 2025 19:35:19 GMT  
		Size: 399.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d2928c9892124fd7dce8fc22858f0cddc27e8ef53f85a8ea22e94bd5b6afd53`  
		Last Modified: Thu, 16 Oct 2025 19:35:19 GMT  
		Size: 74.0 KB (73986 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3de3eff4235a00756c68d537f1f1690002f0371b20fa78e36df085ee28411da`  
		Last Modified: Thu, 16 Oct 2025 19:35:19 GMT  
		Size: 1.0 KB (1044 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:819318f3367b6da19c364d165ea0a00612cfd91e1550e9b6e577fde6035c4042`  
		Last Modified: Thu, 16 Oct 2025 19:35:19 GMT  
		Size: 1.7 KB (1707 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kibana:9.0.8` - unknown; unknown

```console
$ docker pull kibana@sha256:e19b02c52352027c2253e8a7cebf0956e6c82b8d5b89a9d052fd4fd3bf07e70f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5608795 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6635477c3405f7c664835bd4db0a178e9108a75cf4ae0783c8de570315ed2e05`

```dockerfile
```

-	Layers:
	-	`sha256:98818dd41321132ea21b3c16fd4e7e09b5d6eb7cec69293c950ea87276d88f35`  
		Last Modified: Thu, 16 Oct 2025 20:11:26 GMT  
		Size: 5.6 MB (5565269 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6edcfea70b2f03e75a4b0fe67452f8eeeb71f6beaef7f4aa4975c0ab28bd58fc`  
		Last Modified: Thu, 16 Oct 2025 20:11:27 GMT  
		Size: 43.5 KB (43526 bytes)  
		MIME: application/vnd.in-toto+json

## `kibana:9.1.5`

```console
$ docker pull kibana@sha256:d71bf33f4c1a617bb6d4c25e08fe2b5f512de37b025efe323672a711b1777554
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `kibana:9.1.5` - linux; amd64

```console
$ docker pull kibana@sha256:2102555efe91940e8396589762bfcf94ec47cd663f6104ba56d4f2a87e92bda7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **438.0 MB (438004677 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f0e3f082a5b5232323ed63fc26b1a6550004fcc96e530fb455ba437bdcba63a`
-	Entrypoint: `["\/bin\/tini","--"]`
-	Default Command: `["\/usr\/local\/bin\/kibana-docker"]`

```dockerfile
# Mon, 06 Oct 2025 11:10:10 GMT
LABEL maintainer="Red Hat, Inc."
# Mon, 06 Oct 2025 11:10:10 GMT
LABEL vendor="Red Hat, Inc."
# Mon, 06 Oct 2025 11:10:10 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Mon, 06 Oct 2025 11:10:10 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.6"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Mon, 06 Oct 2025 11:10:10 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Mon, 06 Oct 2025 11:10:10 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Mon, 06 Oct 2025 11:10:10 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 06 Oct 2025 11:10:10 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 06 Oct 2025 11:10:10 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Mon, 06 Oct 2025 11:10:10 GMT
LABEL io.openshift.expose-services=""
# Mon, 06 Oct 2025 11:10:10 GMT
LABEL io.openshift.tags="minimal rhel9"
# Mon, 06 Oct 2025 11:10:10 GMT
ENV container oci
# Mon, 06 Oct 2025 11:10:10 GMT
COPY dir:f15650dcc2939ee0c30865212b61e6718fd6c24de4e7967bf7b651b8f0b24352 in /      
# Mon, 06 Oct 2025 11:10:10 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Mon, 06 Oct 2025 11:10:10 GMT
CMD ["/bin/bash"]
# Mon, 06 Oct 2025 11:10:10 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /usr/share/buildinfo/content-sets.json      
# Mon, 06 Oct 2025 11:10:10 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /root/buildinfo/content_manifests/content-sets.json      
# Mon, 06 Oct 2025 11:10:10 GMT
COPY file:16bf5aac480286f91e3031d4f1acb4e76fb8c3be38d180e4713a0efdc39d6bad in /root/buildinfo/labels.json      
# Mon, 06 Oct 2025 11:10:10 GMT
LABEL "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="d1b15a34ce69ea214e1d32f1f501304f6b8b8c59" "org.opencontainers.image.revision"="d1b15a34ce69ea214e1d32f1f501304f6b8b8c59" "build-date"="2025-10-15T08:06:12Z" "release"="1760515502"org.opencontainers.image.revision=d1b15a34ce69ea214e1d32f1f501304f6b8b8c59
# Mon, 06 Oct 2025 11:10:10 GMT
EXPOSE map[5601/tcp:{}]
# Mon, 06 Oct 2025 11:10:10 GMT
RUN microdnf install --setopt=tsflags=nodocs -y       fontconfig liberation-fonts-common freetype shadow-utils nss findutils &&       microdnf clean all # buildkit
# Mon, 06 Oct 2025 11:10:10 GMT
COPY --chown=1000:0 /usr/share/kibana /usr/share/kibana # buildkit
# Mon, 06 Oct 2025 11:10:10 GMT
COPY --chown=0:0 /bin/tini /bin/tini # buildkit
# Mon, 06 Oct 2025 11:10:10 GMT
COPY --chown=0:0 /usr/share/fonts/local/NotoSansCJK-Regular.ttc /usr/share/fonts/local/NotoSansCJK-Regular.ttc # buildkit
# Mon, 06 Oct 2025 11:10:10 GMT
RUN fc-cache -v # buildkit
# Mon, 06 Oct 2025 11:10:10 GMT
WORKDIR /usr/share/kibana
# Mon, 06 Oct 2025 11:10:10 GMT
RUN ln -s /usr/share/kibana /opt/kibana # buildkit
# Mon, 06 Oct 2025 11:10:10 GMT
ENV ELASTIC_CONTAINER=true
# Mon, 06 Oct 2025 11:10:10 GMT
ENV PATH=/usr/share/kibana/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 06 Oct 2025 11:10:10 GMT
COPY --chown=1000:0 config/kibana.yml /usr/share/kibana/config/kibana.yml # buildkit
# Mon, 06 Oct 2025 11:10:10 GMT
COPY bin/kibana-docker /usr/local/bin/ # buildkit
# Mon, 06 Oct 2025 11:10:10 GMT
RUN chmod g+ws /usr/share/kibana &&     find /usr/share/kibana -gid 0 -and -not -perm /g+w -exec chmod g+w {} \; # buildkit
# Mon, 06 Oct 2025 11:10:10 GMT
RUN find / -xdev -perm -4000 -exec chmod u-s {} + # buildkit
# Mon, 06 Oct 2025 11:10:10 GMT
RUN groupadd --gid 1000 kibana &&     useradd --uid 1000 --gid 1000 -G 0       --home-dir /usr/share/kibana --no-create-home       kibana # buildkit
# Mon, 06 Oct 2025 11:10:10 GMT
LABEL org.label-schema.build-date=2025-10-02T12:43:32.321Z org.label-schema.license=Elastic License org.label-schema.name=Kibana org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/kibana org.label-schema.usage=https://www.elastic.co/guide/en/kibana/reference/index.html org.label-schema.vcs-ref=4a62c99c68a5156b84e1bf986d47e0a317591820 org.label-schema.vcs-url=https://github.com/elastic/kibana org.label-schema.vendor=Elastic org.label-schema.version=9.1.5 org.opencontainers.image.created=2025-10-02T12:43:32.321Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/kibana/reference/index.html org.opencontainers.image.licenses=Elastic License org.opencontainers.image.revision=4a62c99c68a5156b84e1bf986d47e0a317591820 org.opencontainers.image.source=https://github.com/elastic/kibana org.opencontainers.image.title=Kibana org.opencontainers.image.url=https://www.elastic.co/products/kibana org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=9.1.5
# Mon, 06 Oct 2025 11:10:10 GMT
LABEL name=Kibana maintainer=infra@elastic.co vendor=Elastic version=9.1.5 release=1 summary=Kibana description=Your window into the Elastic Stack.
# Mon, 06 Oct 2025 11:10:10 GMT
RUN mkdir /licenses && ln LICENSE.txt /licenses/LICENSE # buildkit
# Mon, 06 Oct 2025 11:10:10 GMT
ENTRYPOINT ["/bin/tini" "--"]
# Mon, 06 Oct 2025 11:10:10 GMT
CMD ["/usr/local/bin/kibana-docker"]
# Mon, 06 Oct 2025 11:10:10 GMT
USER 1000
```

-	Layers:
	-	`sha256:2920d84eafa0cf94806ab58f0a2124f7b2d35bcbb06fc89a9106dcc28efe397a`  
		Last Modified: Wed, 15 Oct 2025 09:03:15 GMT  
		Size: 39.7 MB (39653524 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d35aa11bc464475cdec16f7a8db08f652ab3b07e7bfffdabf47d93dc6103869`  
		Last Modified: Thu, 16 Oct 2025 19:36:46 GMT  
		Size: 19.5 MB (19530204 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c543efbc430105d231060dc60f14b325623c026e914d793b00c8d8c73270d7b3`  
		Last Modified: Thu, 16 Oct 2025 23:12:23 GMT  
		Size: 362.3 MB (362262173 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4da912a74c88a2e876e659d580a63d8e7a06fbee72affcf4770a920dbb6401b`  
		Last Modified: Thu, 16 Oct 2025 19:36:43 GMT  
		Size: 9.5 KB (9534 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88b59ad80c4b7a9bc9a566b504ab12d53a508d68636a84850fa2f5a22d8592d8`  
		Last Modified: Thu, 16 Oct 2025 19:36:47 GMT  
		Size: 16.5 MB (16460486 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3458df3e7918558744518c9ea72a70df03490778179d3e3c1e7b35467fe00f70`  
		Last Modified: Thu, 16 Oct 2025 19:36:43 GMT  
		Size: 5.2 KB (5223 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b252e1e129b3437682d90bffa7aea1b172800c6e1a83cd64eb125494302cfb84`  
		Last Modified: Thu, 16 Oct 2025 19:36:43 GMT  
		Size: 130.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa61eeb7e28b14ceaf790cf4067080c8761d23a59894c6ec4307ff8f6cea2c80`  
		Last Modified: Thu, 16 Oct 2025 19:36:43 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c18d73f06246031f3be951c33c024cb7ba99de6a61d0eab493eab2aad18e6962`  
		Last Modified: Thu, 16 Oct 2025 19:36:43 GMT  
		Size: 4.7 KB (4727 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:716cb01c5e6f92d84fa8515a5d1a79aee3ee53879c4995b6ccb395a947de7e9b`  
		Last Modified: Thu, 16 Oct 2025 19:36:43 GMT  
		Size: 400.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c9554d87bd049389b32fbb3a5bab8420b8c10cefe5ccdcc546139da7643aeb9`  
		Last Modified: Thu, 16 Oct 2025 19:36:43 GMT  
		Size: 75.1 KB (75096 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af29a0ac19cdeb7142a33fe0a0f348e64a914881ec94e0b027a3386ecab5408c`  
		Last Modified: Thu, 16 Oct 2025 19:36:43 GMT  
		Size: 1.0 KB (1045 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd0432623bf2217738d733440954f59536bab821b300fe2a260b6751987b0215`  
		Last Modified: Thu, 16 Oct 2025 19:36:43 GMT  
		Size: 1.7 KB (1706 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kibana:9.1.5` - unknown; unknown

```console
$ docker pull kibana@sha256:8f04a939615802d4a1edda6a5c692611dce9a2e076210f91a04ad747a1e26160
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5734543 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b5c3b71f9eb34113395f28d6ce530da00c36ba0d493f5931330a04c73faf151`

```dockerfile
```

-	Layers:
	-	`sha256:33c0e14a91adb9c2af9bb3931d845a39bd518c3c63ac3cb05db5cf591381d8d4`  
		Last Modified: Thu, 16 Oct 2025 23:11:27 GMT  
		Size: 5.7 MB (5691274 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4814199ce2abfbe4dd8d43c4191decab82e7670dc836ce21d7a2de786c87e52f`  
		Last Modified: Thu, 16 Oct 2025 23:11:27 GMT  
		Size: 43.3 KB (43269 bytes)  
		MIME: application/vnd.in-toto+json

### `kibana:9.1.5` - linux; arm64 variant v8

```console
$ docker pull kibana@sha256:1d2abf2db8c094172822dfea216ca4b4cc7105754ad007180552048fbdcb86ad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **449.1 MB (449068620 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e20d992f95561019b74fd1829ca7f619892913e0df4e294b9d7854c7e7e24ff4`
-	Entrypoint: `["\/bin\/tini","--"]`
-	Default Command: `["\/usr\/local\/bin\/kibana-docker"]`

```dockerfile
# Mon, 06 Oct 2025 11:10:10 GMT
LABEL maintainer="Red Hat, Inc."
# Mon, 06 Oct 2025 11:10:10 GMT
LABEL vendor="Red Hat, Inc."
# Mon, 06 Oct 2025 11:10:10 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Mon, 06 Oct 2025 11:10:10 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.6"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Mon, 06 Oct 2025 11:10:10 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Mon, 06 Oct 2025 11:10:10 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Mon, 06 Oct 2025 11:10:10 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 06 Oct 2025 11:10:10 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 06 Oct 2025 11:10:10 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Mon, 06 Oct 2025 11:10:10 GMT
LABEL io.openshift.expose-services=""
# Mon, 06 Oct 2025 11:10:10 GMT
LABEL io.openshift.tags="minimal rhel9"
# Mon, 06 Oct 2025 11:10:10 GMT
ENV container oci
# Mon, 06 Oct 2025 11:10:10 GMT
COPY dir:a993e2e2ad3cf26c4ca4b583710869f381ee3e7df7d41715015a96348230e455 in /      
# Mon, 06 Oct 2025 11:10:10 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Mon, 06 Oct 2025 11:10:10 GMT
CMD ["/bin/bash"]
# Mon, 06 Oct 2025 11:10:10 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /usr/share/buildinfo/content-sets.json      
# Mon, 06 Oct 2025 11:10:10 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /root/buildinfo/content_manifests/content-sets.json      
# Mon, 06 Oct 2025 11:10:10 GMT
COPY file:85de04d2096a64069474160b53ad5f2cfb18b7e3f3ec2a8d26b3946f32e004c9 in /root/buildinfo/labels.json      
# Mon, 06 Oct 2025 11:10:10 GMT
LABEL "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="d1b15a34ce69ea214e1d32f1f501304f6b8b8c59" "org.opencontainers.image.revision"="d1b15a34ce69ea214e1d32f1f501304f6b8b8c59" "build-date"="2025-10-15T08:10:36Z" "release"="1760515502"org.opencontainers.image.revision=d1b15a34ce69ea214e1d32f1f501304f6b8b8c59
# Mon, 06 Oct 2025 11:10:10 GMT
EXPOSE map[5601/tcp:{}]
# Mon, 06 Oct 2025 11:10:10 GMT
RUN microdnf install --setopt=tsflags=nodocs -y       fontconfig liberation-fonts-common freetype shadow-utils nss findutils &&       microdnf clean all # buildkit
# Mon, 06 Oct 2025 11:10:10 GMT
COPY --chown=1000:0 /usr/share/kibana /usr/share/kibana # buildkit
# Mon, 06 Oct 2025 11:10:10 GMT
COPY --chown=0:0 /bin/tini /bin/tini # buildkit
# Mon, 06 Oct 2025 11:10:10 GMT
COPY --chown=0:0 /usr/share/fonts/local/NotoSansCJK-Regular.ttc /usr/share/fonts/local/NotoSansCJK-Regular.ttc # buildkit
# Mon, 06 Oct 2025 11:10:10 GMT
RUN fc-cache -v # buildkit
# Mon, 06 Oct 2025 11:10:10 GMT
WORKDIR /usr/share/kibana
# Mon, 06 Oct 2025 11:10:10 GMT
RUN ln -s /usr/share/kibana /opt/kibana # buildkit
# Mon, 06 Oct 2025 11:10:10 GMT
ENV ELASTIC_CONTAINER=true
# Mon, 06 Oct 2025 11:10:10 GMT
ENV PATH=/usr/share/kibana/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 06 Oct 2025 11:10:10 GMT
COPY --chown=1000:0 config/kibana.yml /usr/share/kibana/config/kibana.yml # buildkit
# Mon, 06 Oct 2025 11:10:10 GMT
COPY bin/kibana-docker /usr/local/bin/ # buildkit
# Mon, 06 Oct 2025 11:10:10 GMT
RUN chmod g+ws /usr/share/kibana &&     find /usr/share/kibana -gid 0 -and -not -perm /g+w -exec chmod g+w {} \; # buildkit
# Mon, 06 Oct 2025 11:10:10 GMT
RUN find / -xdev -perm -4000 -exec chmod u-s {} + # buildkit
# Mon, 06 Oct 2025 11:10:10 GMT
RUN groupadd --gid 1000 kibana &&     useradd --uid 1000 --gid 1000 -G 0       --home-dir /usr/share/kibana --no-create-home       kibana # buildkit
# Mon, 06 Oct 2025 11:10:10 GMT
LABEL org.label-schema.build-date=2025-10-02T12:43:32.321Z org.label-schema.license=Elastic License org.label-schema.name=Kibana org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/kibana org.label-schema.usage=https://www.elastic.co/guide/en/kibana/reference/index.html org.label-schema.vcs-ref=4a62c99c68a5156b84e1bf986d47e0a317591820 org.label-schema.vcs-url=https://github.com/elastic/kibana org.label-schema.vendor=Elastic org.label-schema.version=9.1.5 org.opencontainers.image.created=2025-10-02T12:43:32.321Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/kibana/reference/index.html org.opencontainers.image.licenses=Elastic License org.opencontainers.image.revision=4a62c99c68a5156b84e1bf986d47e0a317591820 org.opencontainers.image.source=https://github.com/elastic/kibana org.opencontainers.image.title=Kibana org.opencontainers.image.url=https://www.elastic.co/products/kibana org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=9.1.5
# Mon, 06 Oct 2025 11:10:10 GMT
LABEL name=Kibana maintainer=infra@elastic.co vendor=Elastic version=9.1.5 release=1 summary=Kibana description=Your window into the Elastic Stack.
# Mon, 06 Oct 2025 11:10:10 GMT
RUN mkdir /licenses && ln LICENSE.txt /licenses/LICENSE # buildkit
# Mon, 06 Oct 2025 11:10:10 GMT
ENTRYPOINT ["/bin/tini" "--"]
# Mon, 06 Oct 2025 11:10:10 GMT
CMD ["/usr/local/bin/kibana-docker"]
# Mon, 06 Oct 2025 11:10:10 GMT
USER 1000
```

-	Layers:
	-	`sha256:2602e1c5e8830fe80a6207359ce01e6c9b7d6848be663c4df1e03c724149b8a6`  
		Last Modified: Wed, 15 Oct 2025 09:30:32 GMT  
		Size: 37.9 MB (37896281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d67f4d8a91c3d43f0b76cc9cdb88cf44852cb447113fbf1ef4b67100fbfb5cb6`  
		Last Modified: Thu, 16 Oct 2025 19:35:19 GMT  
		Size: 19.5 MB (19487742 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75655eea04c4c4b3075b98c8dfb3dfab39f574973f09747ee8a8b5281ae73c0a`  
		Last Modified: Thu, 16 Oct 2025 20:16:07 GMT  
		Size: 375.1 MB (375127348 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:685a33234305511fec481fad4e685ca9d29c89203b06d005b8988c4e8db5119c`  
		Last Modified: Thu, 16 Oct 2025 19:35:17 GMT  
		Size: 9.1 KB (9103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3119054ddd5e58baa15678d962d57166158c20eb84c612ce678a0cee28eb4e61`  
		Last Modified: Thu, 16 Oct 2025 19:35:18 GMT  
		Size: 16.5 MB (16460488 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79f21ebfaecd555f7dff33b456f751b83933dea6a881566e31b47c51ef7b6893`  
		Last Modified: Thu, 16 Oct 2025 19:35:17 GMT  
		Size: 5.2 KB (5228 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ecb1502ea37cb78daad30cb7c074e6829819a7d7a479ac0c1a1b33222d71c17`  
		Last Modified: Thu, 16 Oct 2025 19:35:17 GMT  
		Size: 131.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e335d5f7f0caa62922f5276e267ab6cfe45a7109d253509b4f49980089d6de41`  
		Last Modified: Thu, 16 Oct 2025 19:35:17 GMT  
		Size: 399.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46733ed74ca07cc0b5505ad28ac860b92f4835e1d6ccf838d331f218207e674a`  
		Last Modified: Thu, 16 Oct 2025 19:35:17 GMT  
		Size: 4.7 KB (4729 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff088927a4928e3fff5cd43a755939c4acf8318d71e01f6041adceaef52e881e`  
		Last Modified: Thu, 16 Oct 2025 19:35:17 GMT  
		Size: 401.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43f3040e46ab1e6ef9367efa6fe96ef964a6b6865151d3b8b8fa5498f787f10b`  
		Last Modified: Thu, 16 Oct 2025 19:35:17 GMT  
		Size: 74.0 KB (73986 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b207c619a48850a70b8ebd4a003845c37ceca710e3db9674b75cdf5d85ca8bee`  
		Last Modified: Thu, 16 Oct 2025 19:35:17 GMT  
		Size: 1.0 KB (1044 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06e4c2e92096e13d4255ca1fb233764978796a29df928971dc868c9e77587b8b`  
		Last Modified: Thu, 16 Oct 2025 19:35:15 GMT  
		Size: 1.7 KB (1708 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kibana:9.1.5` - unknown; unknown

```console
$ docker pull kibana@sha256:767f9a7d5c30229eb7aa67bee9d8343ac13957e915301fdc7fad734f6a11bb70
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5733478 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:776745e445aa0305f9007d2ac740d160796a0cfb3551867d871c0c80b998dda9`

```dockerfile
```

-	Layers:
	-	`sha256:6a7a5880ead041659c5640aeb76042df2a40055a514f5bca933d4b79155f10c9`  
		Last Modified: Thu, 16 Oct 2025 20:11:32 GMT  
		Size: 5.7 MB (5689952 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8ca6eef8b004f78d7919418837cbd9626d0c87041833ffa7be912bd71b24dfeb`  
		Last Modified: Thu, 16 Oct 2025 20:11:33 GMT  
		Size: 43.5 KB (43526 bytes)  
		MIME: application/vnd.in-toto+json
