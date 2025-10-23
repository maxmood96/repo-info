<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `kibana`

-	[`kibana:7.17.29`](#kibana71729)
-	[`kibana:8.18.8`](#kibana8188)
-	[`kibana:8.19.6`](#kibana8196)
-	[`kibana:9.1.6`](#kibana916)
-	[`kibana:9.2.0`](#kibana920)

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

## `kibana:8.19.6`

**does not exist** (yet?)

## `kibana:9.1.6`

**does not exist** (yet?)

## `kibana:9.2.0`

**does not exist** (yet?)
