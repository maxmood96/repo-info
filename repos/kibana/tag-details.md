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

```console
$ docker pull kibana@sha256:fe11e44d5d9a7ae0894e207f8ff2172a09e1303699a4854036906e197b9118a2
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; arm64 variant v8
	-	unknown; unknown

### `kibana:8.19.6` - linux; arm64 variant v8

```console
$ docker pull kibana@sha256:5bc196c5544cb1b78874b861051d97acc1a1ae2955d52e46c30bead9e50fb1e8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **449.0 MB (448974853 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:403d469c548c63d58426142b73c1e23193ec87c5cc033038b9db45bf2e8512c6`
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
# Thu, 23 Oct 2025 13:48:53 GMT
EXPOSE map[5601/tcp:{}]
# Thu, 23 Oct 2025 13:48:53 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&       apt-get update &&       apt-get install -y --no-install-recommends fontconfig fonts-liberation libnss3 curl ca-certificates &&       apt-get clean &&       rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 23 Oct 2025 13:48:53 GMT
COPY --chown=1000:0 /usr/share/kibana /usr/share/kibana # buildkit
# Thu, 23 Oct 2025 13:48:53 GMT
COPY --chown=0:0 /bin/tini /bin/tini # buildkit
# Thu, 23 Oct 2025 13:48:53 GMT
COPY --chown=0:0 /usr/share/fonts/local/NotoSansCJK-Regular.ttc /usr/share/fonts/local/NotoSansCJK-Regular.ttc # buildkit
# Thu, 23 Oct 2025 13:48:53 GMT
RUN fc-cache -v # buildkit
# Thu, 23 Oct 2025 13:48:53 GMT
WORKDIR /usr/share/kibana
# Thu, 23 Oct 2025 13:48:53 GMT
RUN ln -s /usr/share/kibana /opt/kibana # buildkit
# Thu, 23 Oct 2025 13:48:53 GMT
ENV ELASTIC_CONTAINER=true
# Thu, 23 Oct 2025 13:48:53 GMT
ENV PATH=/usr/share/kibana/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 23 Oct 2025 13:48:53 GMT
COPY --chown=1000:0 config/kibana.yml /usr/share/kibana/config/kibana.yml # buildkit
# Thu, 23 Oct 2025 13:48:53 GMT
COPY bin/kibana-docker /usr/local/bin/ # buildkit
# Thu, 23 Oct 2025 13:48:53 GMT
RUN chmod g+ws /usr/share/kibana &&     find /usr/share/kibana -gid 0 -and -not -perm /g+w -exec chmod g+w {} \; # buildkit
# Thu, 23 Oct 2025 13:48:53 GMT
RUN find / -xdev -perm -4000 -exec chmod u-s {} + # buildkit
# Thu, 23 Oct 2025 13:48:53 GMT
RUN userdel -r ubuntu && groupadd --gid 1000 kibana &&     useradd --uid 1000 --gid 1000 -G 0       --home-dir /usr/share/kibana --no-create-home       kibana # buildkit
# Thu, 23 Oct 2025 13:48:53 GMT
LABEL org.label-schema.build-date=2025-10-21T20:18:24.484Z org.label-schema.license=Elastic License org.label-schema.name=Kibana org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/kibana org.label-schema.usage=https://www.elastic.co/guide/en/kibana/reference/index.html org.label-schema.vcs-ref=93caa41bf1dca66c8754156cd7819e2ceb980455 org.label-schema.vcs-url=https://github.com/elastic/kibana org.label-schema.vendor=Elastic org.label-schema.version=8.19.6 org.opencontainers.image.created=2025-10-21T20:18:24.484Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/kibana/reference/index.html org.opencontainers.image.licenses=Elastic License org.opencontainers.image.revision=93caa41bf1dca66c8754156cd7819e2ceb980455 org.opencontainers.image.source=https://github.com/elastic/kibana org.opencontainers.image.title=Kibana org.opencontainers.image.url=https://www.elastic.co/products/kibana org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=8.19.6
# Thu, 23 Oct 2025 13:48:53 GMT
ENTRYPOINT ["/bin/tini" "--"]
# Thu, 23 Oct 2025 13:48:53 GMT
CMD ["/usr/local/bin/kibana-docker"]
# Thu, 23 Oct 2025 13:48:53 GMT
USER 1000
```

-	Layers:
	-	`sha256:b8a35db46e38ce87d4e743e1265ff436ed36e01d23246b24a1cbbeaae18ec432`  
		Last Modified: Wed, 01 Oct 2025 15:34:19 GMT  
		Size: 28.9 MB (28861712 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:580a31c4bac2f52fdd2fc72879b540667f6f83d4671c6ff75a75e717b696e732`  
		Last Modified: Thu, 23 Oct 2025 21:10:59 GMT  
		Size: 9.4 MB (9446261 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86dd260b8bf9b479a3c7f9cc6f3ab6ae88c13bd309209ff7f12a7a0184ec30ae`  
		Last Modified: Thu, 23 Oct 2025 23:16:46 GMT  
		Size: 394.0 MB (394027066 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b51d11f6e9682b8cd1da0658e738b5cf0c52f320f5a2c239ef72846fcb4a1e6`  
		Last Modified: Thu, 23 Oct 2025 21:10:58 GMT  
		Size: 9.1 KB (9099 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a007ffc33d46338e7650c1330d56a5c8bf27cc87a9e398d0bf689278f71b79e`  
		Last Modified: Thu, 23 Oct 2025 21:11:01 GMT  
		Size: 16.5 MB (16460487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5139fe298674dfe851c879b05aafaec8f65e67a3848c35c60c39915ec5a464b`  
		Last Modified: Thu, 23 Oct 2025 21:10:59 GMT  
		Size: 5.2 KB (5240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50ac275b41d0f909524fba2e9c31bea47083a5854828149b8bf556c6148c4784`  
		Last Modified: Thu, 23 Oct 2025 21:10:59 GMT  
		Size: 131.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7977b0acd408695ab366174ae8d79842024ee9c7afb7fbb08e113a7e052cfe3d`  
		Last Modified: Thu, 23 Oct 2025 21:10:58 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7daf5631e0b618ecc6e8ca2757d602127db8fb7580158a86d403c9c9c1333b16`  
		Last Modified: Thu, 23 Oct 2025 21:10:58 GMT  
		Size: 4.8 KB (4813 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5435c23d3b958b346f4410a2d0b3e3fd1cc08a14d285fd4c38bc3ef536d09596`  
		Last Modified: Thu, 23 Oct 2025 21:10:59 GMT  
		Size: 399.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0f70308b29f8e655490662ee4d23915ebf312fc5ef6816612319cc72e95d8d4`  
		Last Modified: Thu, 23 Oct 2025 21:10:59 GMT  
		Size: 158.0 KB (157993 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:411ae2e1dce1bc2641f3ca024478a4582f429edf369fbe4b2bc8ff6a15ec11ac`  
		Last Modified: Thu, 23 Oct 2025 21:10:59 GMT  
		Size: 1.2 KB (1224 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kibana:8.19.6` - unknown; unknown

```console
$ docker pull kibana@sha256:9564d1948602f9a52b883061b3617c8233207eae38a16c2b6f7c37ab67f829cf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4920129 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f265617e0145ef4be73caca09004fc1835eb2a99a530b09a4ccd7491cc392876`

```dockerfile
```

-	Layers:
	-	`sha256:6ddb215415f2af9558071723f07348955f2ae24cf82991c630cb363543c1072c`  
		Last Modified: Thu, 23 Oct 2025 23:11:20 GMT  
		Size: 4.9 MB (4878930 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3aac9fd3c43042fbaeb8bda15afac33c00a230e2547966bb2387f4bdf66bc9d8`  
		Last Modified: Thu, 23 Oct 2025 23:11:21 GMT  
		Size: 41.2 KB (41199 bytes)  
		MIME: application/vnd.in-toto+json

## `kibana:9.1.6`

```console
$ docker pull kibana@sha256:b34d56b12abb6f6b869e5a1512057cfb29a3c59894d0b9aa07aaec775c940593
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; arm64 variant v8
	-	unknown; unknown

### `kibana:9.1.6` - linux; arm64 variant v8

```console
$ docker pull kibana@sha256:cf39a681ac1d6c24a8b9d46560eda7583e1c0843da15cc0e3ccc1dcf25f20f58
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **448.9 MB (448943428 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c7f4045b6d6cab2d7027cc8b9d8909ad81bba283ee5e372997917459055a1d1c`
-	Entrypoint: `["\/bin\/tini","--"]`
-	Default Command: `["\/usr\/local\/bin\/kibana-docker"]`

```dockerfile
# Wed, 15 Oct 2025 08:10:52 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 15 Oct 2025 08:10:52 GMT
LABEL vendor="Red Hat, Inc."
# Wed, 15 Oct 2025 08:10:52 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Wed, 15 Oct 2025 08:10:52 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.6"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Wed, 15 Oct 2025 08:10:52 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 15 Oct 2025 08:10:52 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Wed, 15 Oct 2025 08:10:52 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 15 Oct 2025 08:10:52 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 15 Oct 2025 08:10:52 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Wed, 15 Oct 2025 08:10:52 GMT
LABEL io.openshift.expose-services=""
# Wed, 15 Oct 2025 08:10:52 GMT
LABEL io.openshift.tags="minimal rhel9"
# Wed, 15 Oct 2025 08:10:52 GMT
ENV container oci
# Wed, 15 Oct 2025 08:10:53 GMT
COPY dir:a993e2e2ad3cf26c4ca4b583710869f381ee3e7df7d41715015a96348230e455 in /      
# Wed, 15 Oct 2025 08:10:53 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Wed, 15 Oct 2025 08:10:53 GMT
CMD ["/bin/bash"]
# Wed, 15 Oct 2025 08:10:54 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /usr/share/buildinfo/content-sets.json      
# Wed, 15 Oct 2025 08:10:54 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /root/buildinfo/content_manifests/content-sets.json      
# Wed, 15 Oct 2025 08:10:54 GMT
COPY file:85de04d2096a64069474160b53ad5f2cfb18b7e3f3ec2a8d26b3946f32e004c9 in /root/buildinfo/labels.json      
# Wed, 15 Oct 2025 08:10:54 GMT
LABEL "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="d1b15a34ce69ea214e1d32f1f501304f6b8b8c59" "org.opencontainers.image.revision"="d1b15a34ce69ea214e1d32f1f501304f6b8b8c59" "build-date"="2025-10-15T08:10:36Z" "release"="1760515502"org.opencontainers.image.revision=d1b15a34ce69ea214e1d32f1f501304f6b8b8c59
# Thu, 23 Oct 2025 13:49:09 GMT
EXPOSE map[5601/tcp:{}]
# Thu, 23 Oct 2025 13:49:09 GMT
RUN microdnf install --setopt=tsflags=nodocs -y       fontconfig liberation-fonts-common freetype shadow-utils nss findutils &&       microdnf clean all # buildkit
# Thu, 23 Oct 2025 13:49:09 GMT
COPY --chown=1000:0 /usr/share/kibana /usr/share/kibana # buildkit
# Thu, 23 Oct 2025 13:49:09 GMT
COPY --chown=0:0 /bin/tini /bin/tini # buildkit
# Thu, 23 Oct 2025 13:49:09 GMT
COPY --chown=0:0 /usr/share/fonts/local/NotoSansCJK-Regular.ttc /usr/share/fonts/local/NotoSansCJK-Regular.ttc # buildkit
# Thu, 23 Oct 2025 13:49:09 GMT
RUN fc-cache -v # buildkit
# Thu, 23 Oct 2025 13:49:09 GMT
WORKDIR /usr/share/kibana
# Thu, 23 Oct 2025 13:49:09 GMT
RUN ln -s /usr/share/kibana /opt/kibana # buildkit
# Thu, 23 Oct 2025 13:49:09 GMT
ENV ELASTIC_CONTAINER=true
# Thu, 23 Oct 2025 13:49:09 GMT
ENV PATH=/usr/share/kibana/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 23 Oct 2025 13:49:09 GMT
COPY --chown=1000:0 config/kibana.yml /usr/share/kibana/config/kibana.yml # buildkit
# Thu, 23 Oct 2025 13:49:09 GMT
COPY bin/kibana-docker /usr/local/bin/ # buildkit
# Thu, 23 Oct 2025 13:49:09 GMT
RUN chmod g+ws /usr/share/kibana &&     find /usr/share/kibana -gid 0 -and -not -perm /g+w -exec chmod g+w {} \; # buildkit
# Thu, 23 Oct 2025 13:49:09 GMT
RUN find / -xdev -perm -4000 -exec chmod u-s {} + # buildkit
# Thu, 23 Oct 2025 13:49:09 GMT
RUN groupadd --gid 1000 kibana &&     useradd --uid 1000 --gid 1000 -G 0       --home-dir /usr/share/kibana --no-create-home       kibana # buildkit
# Thu, 23 Oct 2025 13:49:09 GMT
LABEL org.label-schema.build-date=2025-10-21T20:33:09.265Z org.label-schema.license=Elastic License org.label-schema.name=Kibana org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/kibana org.label-schema.usage=https://www.elastic.co/guide/en/kibana/reference/index.html org.label-schema.vcs-ref=fe461e4c2dd2d70d5890576919a218694f51eea3 org.label-schema.vcs-url=https://github.com/elastic/kibana org.label-schema.vendor=Elastic org.label-schema.version=9.1.6 org.opencontainers.image.created=2025-10-21T20:33:09.265Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/kibana/reference/index.html org.opencontainers.image.licenses=Elastic License org.opencontainers.image.revision=fe461e4c2dd2d70d5890576919a218694f51eea3 org.opencontainers.image.source=https://github.com/elastic/kibana org.opencontainers.image.title=Kibana org.opencontainers.image.url=https://www.elastic.co/products/kibana org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=9.1.6
# Thu, 23 Oct 2025 13:49:09 GMT
LABEL name=Kibana maintainer=infra@elastic.co vendor=Elastic version=9.1.6 release=1 summary=Kibana description=Your window into the Elastic Stack.
# Thu, 23 Oct 2025 13:49:09 GMT
RUN mkdir /licenses && ln LICENSE.txt /licenses/LICENSE # buildkit
# Thu, 23 Oct 2025 13:49:09 GMT
ENTRYPOINT ["/bin/tini" "--"]
# Thu, 23 Oct 2025 13:49:09 GMT
CMD ["/usr/local/bin/kibana-docker"]
# Thu, 23 Oct 2025 13:49:09 GMT
USER 1000
```

-	Layers:
	-	`sha256:2602e1c5e8830fe80a6207359ce01e6c9b7d6848be663c4df1e03c724149b8a6`  
		Last Modified: Wed, 15 Oct 2025 09:30:32 GMT  
		Size: 37.9 MB (37896281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c920ded354d76c8779145cb5efd63654fe99e71d853ad83fa0d5eeb344c1355`  
		Last Modified: Thu, 23 Oct 2025 21:10:45 GMT  
		Size: 19.5 MB (19487811 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3719b654a54e4d5857b9cfe21cffbe5987e785b997153631de7bd09954c2e0d5`  
		Last Modified: Thu, 23 Oct 2025 21:24:43 GMT  
		Size: 375.0 MB (375002095 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96149a0549381ad43930efccc178fb73f751256344b73f063a3081533f0660a9`  
		Last Modified: Thu, 23 Oct 2025 21:10:43 GMT  
		Size: 9.1 KB (9103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8af4102ef603ebc12f8e87c2196dcf50a669cfe57bf2aab0832ce4faa915f3a`  
		Last Modified: Thu, 23 Oct 2025 21:10:45 GMT  
		Size: 16.5 MB (16460489 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a30cd2a6fbececd887d963d2c17bc3016b7550e726deae2a20ed16c14b01d955`  
		Last Modified: Thu, 23 Oct 2025 21:10:42 GMT  
		Size: 5.2 KB (5224 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e8431d83b83c63744a143b07407afdbcc546172a6dec7ff4eaaeb31c43a77e5`  
		Last Modified: Thu, 23 Oct 2025 21:10:42 GMT  
		Size: 131.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:077d2101e0db72db3dc3297fec8442a360897daddafd71c6be8f74466e7d8b49`  
		Last Modified: Thu, 23 Oct 2025 21:10:43 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3fa1f7f24a8fccabeab3862337a0d13ed7c79aee85c880d42c922dc1aef759bb`  
		Last Modified: Thu, 23 Oct 2025 21:10:42 GMT  
		Size: 4.7 KB (4727 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8358045074f4728a4e0931143cdc29a381a8e94798abaf5936dac3477e06c4a5`  
		Last Modified: Thu, 23 Oct 2025 21:10:42 GMT  
		Size: 399.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0983ac7a1e2e321b0724fa9076bf814c4579d932e3fe96806aa739e6e12b1749`  
		Last Modified: Thu, 23 Oct 2025 21:10:42 GMT  
		Size: 74.0 KB (73986 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e598fdaaee922fb7b7ed2896b3da8aee79bf3401813de97f50c6e81828199f0`  
		Last Modified: Thu, 23 Oct 2025 21:10:42 GMT  
		Size: 1.0 KB (1045 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:611790c8ea475b5bdf402e9227cd366ed086358ee9a9bc479abfc09f4e9d84e4`  
		Last Modified: Thu, 23 Oct 2025 21:10:42 GMT  
		Size: 1.7 KB (1708 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kibana:9.1.6` - unknown; unknown

```console
$ docker pull kibana@sha256:44d20d4e6ea69c5753df36e55adae26ba338cfd6f37415d1515fb5a132925175
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5713818 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f47d1471494d25d71feb32d6e302abf6f0dfd026103a6606708d1bd3c8cf76d`

```dockerfile
```

-	Layers:
	-	`sha256:4fa74bc58bee27d7d69c59d26501c48eef798310fbeb38927d1f4eb0619575d5`  
		Last Modified: Thu, 23 Oct 2025 23:11:26 GMT  
		Size: 5.7 MB (5670293 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:35191af9a762678b53d69decd19880760585e89e296fc1848a8b52d0f386dc6c`  
		Last Modified: Thu, 23 Oct 2025 23:11:27 GMT  
		Size: 43.5 KB (43525 bytes)  
		MIME: application/vnd.in-toto+json

## `kibana:9.2.0`

```console
$ docker pull kibana@sha256:a329330698525d6c0793db061e2a682f538ba395ddb419885687e7bd2dcc27b1
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; arm64 variant v8
	-	unknown; unknown

### `kibana:9.2.0` - linux; arm64 variant v8

```console
$ docker pull kibana@sha256:6315d31deed85f165a1fac55c523702cfee528f585ed5bfe1fedfa3083b09aa2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **447.6 MB (447558129 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac303a095e03bb2880ab9554f5a9b818c68d8f1b2f99d2103e3a71d7b198d325`
-	Entrypoint: `["\/bin\/tini","--"]`
-	Default Command: `["\/usr\/local\/bin\/kibana-docker"]`

```dockerfile
# Wed, 15 Oct 2025 08:10:52 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 15 Oct 2025 08:10:52 GMT
LABEL vendor="Red Hat, Inc."
# Wed, 15 Oct 2025 08:10:52 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Wed, 15 Oct 2025 08:10:52 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.6"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Wed, 15 Oct 2025 08:10:52 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 15 Oct 2025 08:10:52 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Wed, 15 Oct 2025 08:10:52 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 15 Oct 2025 08:10:52 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 15 Oct 2025 08:10:52 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Wed, 15 Oct 2025 08:10:52 GMT
LABEL io.openshift.expose-services=""
# Wed, 15 Oct 2025 08:10:52 GMT
LABEL io.openshift.tags="minimal rhel9"
# Wed, 15 Oct 2025 08:10:52 GMT
ENV container oci
# Wed, 15 Oct 2025 08:10:53 GMT
COPY dir:a993e2e2ad3cf26c4ca4b583710869f381ee3e7df7d41715015a96348230e455 in /      
# Wed, 15 Oct 2025 08:10:53 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Wed, 15 Oct 2025 08:10:53 GMT
CMD ["/bin/bash"]
# Wed, 15 Oct 2025 08:10:54 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /usr/share/buildinfo/content-sets.json      
# Wed, 15 Oct 2025 08:10:54 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /root/buildinfo/content_manifests/content-sets.json      
# Wed, 15 Oct 2025 08:10:54 GMT
COPY file:85de04d2096a64069474160b53ad5f2cfb18b7e3f3ec2a8d26b3946f32e004c9 in /root/buildinfo/labels.json      
# Wed, 15 Oct 2025 08:10:54 GMT
LABEL "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="d1b15a34ce69ea214e1d32f1f501304f6b8b8c59" "org.opencontainers.image.revision"="d1b15a34ce69ea214e1d32f1f501304f6b8b8c59" "build-date"="2025-10-15T08:10:36Z" "release"="1760515502"org.opencontainers.image.revision=d1b15a34ce69ea214e1d32f1f501304f6b8b8c59
# Thu, 23 Oct 2025 08:40:15 GMT
EXPOSE map[5601/tcp:{}]
# Thu, 23 Oct 2025 08:40:15 GMT
RUN microdnf install --setopt=tsflags=nodocs -y       fontconfig liberation-fonts-common freetype shadow-utils nss findutils &&       microdnf clean all # buildkit
# Thu, 23 Oct 2025 08:40:15 GMT
COPY --chown=1000:0 /usr/share/kibana /usr/share/kibana # buildkit
# Thu, 23 Oct 2025 08:40:15 GMT
COPY --chown=0:0 /bin/tini /bin/tini # buildkit
# Thu, 23 Oct 2025 08:40:15 GMT
COPY --chown=0:0 /usr/share/fonts/local/NotoSansCJK-Regular.ttc /usr/share/fonts/local/NotoSansCJK-Regular.ttc # buildkit
# Thu, 23 Oct 2025 08:40:15 GMT
RUN fc-cache -v # buildkit
# Thu, 23 Oct 2025 08:40:15 GMT
WORKDIR /usr/share/kibana
# Thu, 23 Oct 2025 08:40:15 GMT
RUN ln -s /usr/share/kibana /opt/kibana # buildkit
# Thu, 23 Oct 2025 08:40:15 GMT
ENV ELASTIC_CONTAINER=true
# Thu, 23 Oct 2025 08:40:15 GMT
ENV PATH=/usr/share/kibana/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 23 Oct 2025 08:40:15 GMT
COPY --chown=1000:0 config/kibana.yml /usr/share/kibana/config/kibana.yml # buildkit
# Thu, 23 Oct 2025 08:40:15 GMT
COPY bin/kibana-docker /usr/local/bin/ # buildkit
# Thu, 23 Oct 2025 08:40:15 GMT
RUN chmod g+ws /usr/share/kibana &&     find /usr/share/kibana -gid 0 -and -not -perm /g+w -exec chmod g+w {} \; # buildkit
# Thu, 23 Oct 2025 08:40:15 GMT
RUN find / -xdev -perm -4000 -exec chmod u-s {} + # buildkit
# Thu, 23 Oct 2025 08:40:15 GMT
RUN groupadd --gid 1000 kibana &&     useradd --uid 1000 --gid 1000 -G 0       --home-dir /usr/share/kibana --no-create-home       kibana # buildkit
# Thu, 23 Oct 2025 08:40:15 GMT
LABEL org.label-schema.build-date=2025-10-21T11:30:30.173Z org.label-schema.license=Elastic License org.label-schema.name=Kibana org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/kibana org.label-schema.usage=https://www.elastic.co/guide/en/kibana/reference/index.html org.label-schema.vcs-ref=68626ce831ffb8e4138bb24ba8762a15a569a41c org.label-schema.vcs-url=https://github.com/elastic/kibana org.label-schema.vendor=Elastic org.label-schema.version=9.2.0 org.opencontainers.image.created=2025-10-21T11:30:30.173Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/kibana/reference/index.html org.opencontainers.image.licenses=Elastic License org.opencontainers.image.revision=68626ce831ffb8e4138bb24ba8762a15a569a41c org.opencontainers.image.source=https://github.com/elastic/kibana org.opencontainers.image.title=Kibana org.opencontainers.image.url=https://www.elastic.co/products/kibana org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=9.2.0
# Thu, 23 Oct 2025 08:40:15 GMT
LABEL name=Kibana maintainer=infra@elastic.co vendor=Elastic version=9.2.0 release=1 summary=Kibana description=Your window into the Elastic Stack.
# Thu, 23 Oct 2025 08:40:15 GMT
RUN mkdir /licenses && ln LICENSE.txt /licenses/LICENSE # buildkit
# Thu, 23 Oct 2025 08:40:15 GMT
ENTRYPOINT ["/bin/tini" "--"]
# Thu, 23 Oct 2025 08:40:15 GMT
CMD ["/usr/local/bin/kibana-docker"]
# Thu, 23 Oct 2025 08:40:15 GMT
USER 1000
```

-	Layers:
	-	`sha256:2602e1c5e8830fe80a6207359ce01e6c9b7d6848be663c4df1e03c724149b8a6`  
		Last Modified: Wed, 15 Oct 2025 09:30:32 GMT  
		Size: 37.9 MB (37896281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:691f81ab656790348e344972ba70bbac07c5560fc82d2d509017e6285fe21536`  
		Last Modified: Thu, 23 Oct 2025 22:15:45 GMT  
		Size: 19.5 MB (19487804 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:857ba2aa63c827d0e0322b226b38d48de7ffe5773c805a107911a7d862b11468`  
		Last Modified: Thu, 23 Oct 2025 23:11:01 GMT  
		Size: 373.6 MB (373616700 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:573a096e5546819d9f12c273f393f26d6930e6b0fa04f8d2adc2b6123eb0d17e`  
		Last Modified: Thu, 23 Oct 2025 22:15:41 GMT  
		Size: 9.1 KB (9101 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2cf227133788452b412dfeab08126466b791f47391061a33880e77aed0632bc7`  
		Last Modified: Thu, 23 Oct 2025 22:15:43 GMT  
		Size: 16.5 MB (16460492 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93a92fc7a9985178efb43e95f8b19c57b4b4148a5c3e78a8c01e065f2c5e7b3e`  
		Last Modified: Thu, 23 Oct 2025 22:15:41 GMT  
		Size: 5.2 KB (5224 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90d914f4f130870b3a362bce27a5d0c799bd2e535b3d0171121a8d57d8940e1e`  
		Last Modified: Thu, 23 Oct 2025 22:15:41 GMT  
		Size: 131.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:718e070b062923f6b02c67473484d30054cfc0f444fea8171dae7e11131db89f`  
		Last Modified: Thu, 23 Oct 2025 22:15:41 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cfe6b49d875f1185c83e6b160b9e3e7e4cf8d9782c345ccefe4a34414a5b0b47`  
		Last Modified: Thu, 23 Oct 2025 22:15:41 GMT  
		Size: 4.8 KB (4830 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd3b603bceea7d5a1759fef3262435d332a2fdc300d02c6dbba8f9f1f180e2bd`  
		Last Modified: Thu, 23 Oct 2025 22:15:41 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05bf0b2dbab7d5b35d471305373b7399742083b6e8dd575c63a31202da8e7b06`  
		Last Modified: Thu, 23 Oct 2025 22:15:41 GMT  
		Size: 74.0 KB (73986 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7430c7167736c32864c45109c5434d49cab632ec6c75f817bc627a6d7cccf8bc`  
		Last Modified: Thu, 23 Oct 2025 22:15:41 GMT  
		Size: 1.0 KB (1046 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aef8d2d0ec4788023671b3b7d68feead9ee63a36bcde5d80e72e464d3542f9be`  
		Last Modified: Thu, 23 Oct 2025 22:15:41 GMT  
		Size: 1.7 KB (1708 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kibana:9.2.0` - unknown; unknown

```console
$ docker pull kibana@sha256:9dbb79a309c04300083288b62d98ec2586424ef0c82664a5ca16c09ec572a362
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5774913 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:baaefe6dbe9cd54f9a63d3bca54020b0222f290bd8971ff9c07350d0643cf58c`

```dockerfile
```

-	Layers:
	-	`sha256:73d360523785930e0104d9bef482b6b46656c35d651edd563a9c9c8802fa14e6`  
		Last Modified: Thu, 23 Oct 2025 23:11:31 GMT  
		Size: 5.7 MB (5731388 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:aa05fb751410ccae7f95d0b6939ecfeb9ed3f356f299eb256ca9d308324361c9`  
		Last Modified: Thu, 23 Oct 2025 23:11:32 GMT  
		Size: 43.5 KB (43525 bytes)  
		MIME: application/vnd.in-toto+json
