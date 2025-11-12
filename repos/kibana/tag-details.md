<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `kibana`

-	[`kibana:7.17.29`](#kibana71729)
-	[`kibana:8.18.8`](#kibana8188)
-	[`kibana:8.19.7`](#kibana8197)
-	[`kibana:9.1.7`](#kibana917)
-	[`kibana:9.2.1`](#kibana921)

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

## `kibana:8.19.7`

```console
$ docker pull kibana@sha256:82abe5b2b610ccff1abe0374cda1e827d7fb87123722365e76105c8a0702f3a8
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `kibana:8.19.7` - linux; amd64

```console
$ docker pull kibana@sha256:3246fd6ed10b5e62e42798cf58e063aefcfae469ea94950f08d3a0d66e0022bb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **436.7 MB (436689155 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0220db8129a9d9b8355d0cc05834482b805967f86aac9c502e7cd52c6753e549`
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
# Tue, 11 Nov 2025 18:08:34 GMT
EXPOSE map[5601/tcp:{}]
# Tue, 11 Nov 2025 18:08:34 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&       apt-get update &&       apt-get install -y --no-install-recommends fontconfig fonts-liberation libnss3 curl ca-certificates &&       apt-get clean &&       rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 11 Nov 2025 18:17:09 GMT
COPY --chown=1000:0 /usr/share/kibana /usr/share/kibana # buildkit
# Tue, 11 Nov 2025 18:17:09 GMT
COPY --chown=0:0 /bin/tini /bin/tini # buildkit
# Tue, 11 Nov 2025 18:17:09 GMT
COPY --chown=0:0 /usr/share/fonts/local/NotoSansCJK-Regular.ttc /usr/share/fonts/local/NotoSansCJK-Regular.ttc # buildkit
# Tue, 11 Nov 2025 18:17:09 GMT
RUN fc-cache -v # buildkit
# Tue, 11 Nov 2025 18:17:09 GMT
WORKDIR /usr/share/kibana
# Tue, 11 Nov 2025 18:17:09 GMT
RUN ln -s /usr/share/kibana /opt/kibana # buildkit
# Tue, 11 Nov 2025 18:17:09 GMT
ENV ELASTIC_CONTAINER=true
# Tue, 11 Nov 2025 18:17:09 GMT
ENV PATH=/usr/share/kibana/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 11 Nov 2025 18:17:09 GMT
COPY --chown=1000:0 config/kibana.yml /usr/share/kibana/config/kibana.yml # buildkit
# Tue, 11 Nov 2025 18:17:09 GMT
COPY bin/kibana-docker /usr/local/bin/ # buildkit
# Tue, 11 Nov 2025 18:17:10 GMT
RUN chmod g+ws /usr/share/kibana &&     find /usr/share/kibana -gid 0 -and -not -perm /g+w -exec chmod g+w {} \; # buildkit
# Tue, 11 Nov 2025 18:17:11 GMT
RUN find / -xdev -perm -4000 -exec chmod u-s {} + # buildkit
# Tue, 11 Nov 2025 18:17:11 GMT
RUN userdel -r ubuntu && groupadd --gid 1000 kibana &&     useradd --uid 1000 --gid 1000 -G 0       --home-dir /usr/share/kibana --no-create-home       kibana # buildkit
# Tue, 11 Nov 2025 18:17:11 GMT
LABEL org.label-schema.build-date=2025-11-07T13:25:36.883Z org.label-schema.license=Elastic License org.label-schema.name=Kibana org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/kibana org.label-schema.usage=https://www.elastic.co/guide/en/kibana/reference/index.html org.label-schema.vcs-ref=28cf679904329ed50de370ff1e1e71f1b57996a1 org.label-schema.vcs-url=https://github.com/elastic/kibana org.label-schema.vendor=Elastic org.label-schema.version=8.19.7 org.opencontainers.image.created=2025-11-07T13:25:36.883Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/kibana/reference/index.html org.opencontainers.image.licenses=Elastic License org.opencontainers.image.revision=28cf679904329ed50de370ff1e1e71f1b57996a1 org.opencontainers.image.source=https://github.com/elastic/kibana org.opencontainers.image.title=Kibana org.opencontainers.image.url=https://www.elastic.co/products/kibana org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=8.19.7
# Tue, 11 Nov 2025 18:17:11 GMT
ENTRYPOINT ["/bin/tini" "--"]
# Tue, 11 Nov 2025 18:17:11 GMT
CMD ["/usr/local/bin/kibana-docker"]
# Tue, 11 Nov 2025 18:17:11 GMT
USER 1000
```

-	Layers:
	-	`sha256:4b3ffd8ccb5201a0fc03585952effb4ed2d1ea5e704d2e7330212fb8b16c86a3`  
		Last Modified: Wed, 01 Oct 2025 15:21:59 GMT  
		Size: 29.7 MB (29723147 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c880e16938134ffd5120094848bf531ba255e2b83935d72de98f9e78ff043c8`  
		Last Modified: Tue, 11 Nov 2025 18:18:25 GMT  
		Size: 9.4 MB (9432161 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9144df5f9df21eda7bfa954630a10c7cc7b31f4ef238749bf6580076a56db51`  
		Last Modified: Tue, 11 Nov 2025 21:16:02 GMT  
		Size: 380.9 MB (380890140 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24d23e644925a23ad27c66ce23147b781854e6d2013cc8c0cc44d22315d7fe79`  
		Last Modified: Tue, 11 Nov 2025 18:18:21 GMT  
		Size: 9.5 KB (9527 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbdf4dbf4351da731e0460037e7794c7d75a685f89276941d54f9f0570be03f8`  
		Last Modified: Tue, 11 Nov 2025 18:18:23 GMT  
		Size: 16.5 MB (16460483 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8edc743ec862d0603b4978822dc1862e60f4a8390f158e95aaedd9bc61c59744`  
		Last Modified: Tue, 11 Nov 2025 18:18:22 GMT  
		Size: 5.2 KB (5242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8da2e4f3163c48d5dd57e04b50ce74f9c5aeef73540a22a61386efceb89fd733`  
		Last Modified: Tue, 11 Nov 2025 18:18:21 GMT  
		Size: 132.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a911068a7b5523c059511739dad960a8f903225cf35750f47e990cd69f0867c`  
		Last Modified: Tue, 11 Nov 2025 18:18:21 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab896229d63dd3fe421891c284bce4d592adfc33f6b5fcf2eace61d87e78c6ab`  
		Last Modified: Tue, 11 Nov 2025 18:18:21 GMT  
		Size: 4.8 KB (4819 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6067fe3323e4c7be885410ff7e67c57d6e7c656fdd0c61aba076f7d6646dd5a5`  
		Last Modified: Tue, 11 Nov 2025 18:18:21 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26c3f639c38719ee756e94e0dadab3d9e5873c39e45c658eac2e16c4043186da`  
		Last Modified: Tue, 11 Nov 2025 18:18:22 GMT  
		Size: 161.5 KB (161455 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b00de42e17ca6effdbc80527fd8c96d4ff2d5a68a27bceedb5222321ede4ffd`  
		Last Modified: Tue, 11 Nov 2025 18:18:21 GMT  
		Size: 1.2 KB (1224 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kibana:8.19.7` - unknown; unknown

```console
$ docker pull kibana@sha256:55f1532d70a54fd40a1a495d5eedbaa924d1a95499100d217d471dd78bff0d29
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4915242 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:05b8673a29aac09eecc3cbb72f3cb96a5c10634c89f0163804c74abfb9fce220`

```dockerfile
```

-	Layers:
	-	`sha256:29472c3159c3f02cc5c8f51e462b9dc3756195a37886005a65821f623f0a7c98`  
		Last Modified: Tue, 11 Nov 2025 21:11:22 GMT  
		Size: 4.9 MB (4874334 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f37442f097e4b3894d28a414a5895d6d6308896843875060477c5adfc4c8afc1`  
		Last Modified: Tue, 11 Nov 2025 21:11:23 GMT  
		Size: 40.9 KB (40908 bytes)  
		MIME: application/vnd.in-toto+json

### `kibana:8.19.7` - linux; arm64 variant v8

```console
$ docker pull kibana@sha256:81dd642d838f55b9eb22c5a818566add99ff4179b69f429cea397606bc5ab67a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **448.9 MB (448862553 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fd18f3371d5b9b2ec734ad4ce8597a28257dcf0e537d7ee73e3695efab7f7720`
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
# Tue, 11 Nov 2025 18:08:29 GMT
EXPOSE map[5601/tcp:{}]
# Tue, 11 Nov 2025 18:08:29 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&       apt-get update &&       apt-get install -y --no-install-recommends fontconfig fonts-liberation libnss3 curl ca-certificates &&       apt-get clean &&       rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 11 Nov 2025 18:15:41 GMT
COPY --chown=1000:0 /usr/share/kibana /usr/share/kibana # buildkit
# Tue, 11 Nov 2025 18:15:41 GMT
COPY --chown=0:0 /bin/tini /bin/tini # buildkit
# Tue, 11 Nov 2025 18:15:42 GMT
COPY --chown=0:0 /usr/share/fonts/local/NotoSansCJK-Regular.ttc /usr/share/fonts/local/NotoSansCJK-Regular.ttc # buildkit
# Tue, 11 Nov 2025 18:15:42 GMT
RUN fc-cache -v # buildkit
# Tue, 11 Nov 2025 18:15:42 GMT
WORKDIR /usr/share/kibana
# Tue, 11 Nov 2025 18:15:42 GMT
RUN ln -s /usr/share/kibana /opt/kibana # buildkit
# Tue, 11 Nov 2025 18:15:42 GMT
ENV ELASTIC_CONTAINER=true
# Tue, 11 Nov 2025 18:15:42 GMT
ENV PATH=/usr/share/kibana/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 11 Nov 2025 18:15:42 GMT
COPY --chown=1000:0 config/kibana.yml /usr/share/kibana/config/kibana.yml # buildkit
# Tue, 11 Nov 2025 18:15:42 GMT
COPY bin/kibana-docker /usr/local/bin/ # buildkit
# Tue, 11 Nov 2025 18:15:43 GMT
RUN chmod g+ws /usr/share/kibana &&     find /usr/share/kibana -gid 0 -and -not -perm /g+w -exec chmod g+w {} \; # buildkit
# Tue, 11 Nov 2025 18:15:44 GMT
RUN find / -xdev -perm -4000 -exec chmod u-s {} + # buildkit
# Tue, 11 Nov 2025 18:15:44 GMT
RUN userdel -r ubuntu && groupadd --gid 1000 kibana &&     useradd --uid 1000 --gid 1000 -G 0       --home-dir /usr/share/kibana --no-create-home       kibana # buildkit
# Tue, 11 Nov 2025 18:15:44 GMT
LABEL org.label-schema.build-date=2025-11-07T13:25:36.883Z org.label-schema.license=Elastic License org.label-schema.name=Kibana org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/kibana org.label-schema.usage=https://www.elastic.co/guide/en/kibana/reference/index.html org.label-schema.vcs-ref=28cf679904329ed50de370ff1e1e71f1b57996a1 org.label-schema.vcs-url=https://github.com/elastic/kibana org.label-schema.vendor=Elastic org.label-schema.version=8.19.7 org.opencontainers.image.created=2025-11-07T13:25:36.883Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/kibana/reference/index.html org.opencontainers.image.licenses=Elastic License org.opencontainers.image.revision=28cf679904329ed50de370ff1e1e71f1b57996a1 org.opencontainers.image.source=https://github.com/elastic/kibana org.opencontainers.image.title=Kibana org.opencontainers.image.url=https://www.elastic.co/products/kibana org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=8.19.7
# Tue, 11 Nov 2025 18:15:44 GMT
ENTRYPOINT ["/bin/tini" "--"]
# Tue, 11 Nov 2025 18:15:44 GMT
CMD ["/usr/local/bin/kibana-docker"]
# Tue, 11 Nov 2025 18:15:44 GMT
USER 1000
```

-	Layers:
	-	`sha256:b8a35db46e38ce87d4e743e1265ff436ed36e01d23246b24a1cbbeaae18ec432`  
		Last Modified: Wed, 01 Oct 2025 15:34:19 GMT  
		Size: 28.9 MB (28861712 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8acae7d853fa0c0e19758674e69e145f22a8540db5dbef11f9db45c7420a086`  
		Last Modified: Tue, 11 Nov 2025 18:17:00 GMT  
		Size: 9.4 MB (9446414 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb0e28e29bca31b09d03fa46f244cb5e7bcf35fe44175d353e7b7aa5c9cada45`  
		Last Modified: Tue, 11 Nov 2025 21:15:43 GMT  
		Size: 393.9 MB (393914597 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:863ac36706aee86b6ca48137f0e83c91727279a627896eb8632becd68f009303`  
		Last Modified: Tue, 11 Nov 2025 18:16:59 GMT  
		Size: 9.1 KB (9098 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e07981d01e7f034dfee0b5420ae9457a4250218653acb3dc999eb729b95d9fef`  
		Last Modified: Tue, 11 Nov 2025 18:17:01 GMT  
		Size: 16.5 MB (16460495 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1035a0661fa1acf59f030a5dbb6510e777fec88a4b2cf977b7adcdd40e9a42f`  
		Last Modified: Tue, 11 Nov 2025 18:16:59 GMT  
		Size: 5.2 KB (5237 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a03948b3074d0fa79febb026dd2448bad0dac045f116259350f5e74c402a30a`  
		Last Modified: Tue, 11 Nov 2025 18:17:00 GMT  
		Size: 131.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2249b73710a22cf297b3202099b225cb9d98c0daedff2155caaa85b33c337027`  
		Last Modified: Tue, 11 Nov 2025 18:16:59 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:097872d7b2c480e165863ffd8bfc6ea375bccf1d63cebcdcc595369d7568faf2`  
		Last Modified: Tue, 11 Nov 2025 18:16:59 GMT  
		Size: 4.8 KB (4821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e1909c80ee1f31a038f333468dcaf1203137ecd39b6acb52ec11c9b2d7ef51c`  
		Last Modified: Tue, 11 Nov 2025 18:16:59 GMT  
		Size: 399.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df22c0edb5e9ba658448e52a56543c05db8c5d699e71dd35ae65b55a89575187`  
		Last Modified: Tue, 11 Nov 2025 18:16:59 GMT  
		Size: 158.0 KB (157997 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6eeec022f5e3430b61724d82ec7d48ea9afaeee60bf28ffed78d9f47ae0692a9`  
		Last Modified: Tue, 11 Nov 2025 18:16:59 GMT  
		Size: 1.2 KB (1224 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kibana:8.19.7` - unknown; unknown

```console
$ docker pull kibana@sha256:8b90a5e525f09f60c1c83e92e55b3cae55fba884e57a1f6d5da9323e4f0df23e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4916553 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b36d6a270b29b405e214f47f019ec1e3ea12d9257bba4e8beee89ce23a447b66`

```dockerfile
```

-	Layers:
	-	`sha256:4791744e3585c440d51225489dbbd022c339ee0a7185774e8a75dfa52a8c6579`  
		Last Modified: Tue, 11 Nov 2025 21:11:28 GMT  
		Size: 4.9 MB (4875398 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8d4f4b232111938398d2166d1ae510e6d15356e3ef7dddeef9d6e97a692c1dd8`  
		Last Modified: Tue, 11 Nov 2025 21:11:29 GMT  
		Size: 41.2 KB (41155 bytes)  
		MIME: application/vnd.in-toto+json

## `kibana:9.1.7`

```console
$ docker pull kibana@sha256:d82650a1a7ab6245ba8fb1d18edc339ee4b96d9dc551a15f74da211c4c25069b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `kibana:9.1.7` - linux; amd64

```console
$ docker pull kibana@sha256:d866ec9d018e87c4ada323b237cc05670f9e338f5c05d7978d8c8e13917d596c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **437.9 MB (437912387 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e8b0dbf058139596c1fd7c91221344e6ebd8f923c588458a9b0b5fb4aa2d9f47`
-	Entrypoint: `["\/bin\/tini","--"]`
-	Default Command: `["\/usr\/local\/bin\/kibana-docker"]`

```dockerfile
# Mon, 03 Nov 2025 14:28:07 GMT
LABEL maintainer="Red Hat, Inc."
# Mon, 03 Nov 2025 14:28:07 GMT
LABEL vendor="Red Hat, Inc."
# Mon, 03 Nov 2025 14:28:07 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Mon, 03 Nov 2025 14:28:07 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.7"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Mon, 03 Nov 2025 14:28:07 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Mon, 03 Nov 2025 14:28:07 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Mon, 03 Nov 2025 14:28:07 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 03 Nov 2025 14:28:07 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 03 Nov 2025 14:28:07 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Mon, 03 Nov 2025 14:28:07 GMT
LABEL io.openshift.expose-services=""
# Mon, 03 Nov 2025 14:28:07 GMT
LABEL io.openshift.tags="minimal rhel9"
# Mon, 03 Nov 2025 14:28:07 GMT
LABEL compose-id="RHEL-9.7.0-updates-20251029.7"
# Mon, 03 Nov 2025 14:28:07 GMT
ENV container oci
# Mon, 03 Nov 2025 14:28:08 GMT
COPY dir:39710e73aef560d625154347dc7e6b417064723d33d900483645d9d706c0f7a2 in /      
# Mon, 03 Nov 2025 14:28:08 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Mon, 03 Nov 2025 14:28:08 GMT
CMD ["/bin/bash"]
# Mon, 03 Nov 2025 14:28:08 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /usr/share/buildinfo/content-sets.json      
# Mon, 03 Nov 2025 14:28:08 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /root/buildinfo/content_manifests/content-sets.json      
# Mon, 03 Nov 2025 14:28:08 GMT
COPY file:90c5e1a95185d091ee07721ff43a8413d78a6f7cb920f7ce46a03a173e5f926a in /usr/share/buildinfo/labels.json      
# Mon, 03 Nov 2025 14:28:08 GMT
COPY file:90c5e1a95185d091ee07721ff43a8413d78a6f7cb920f7ce46a03a173e5f926a in /root/buildinfo/labels.json      
# Mon, 03 Nov 2025 14:28:09 GMT
LABEL "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="02d02ad5d9d5ef0add399eb1c8d5f2a4b9261204" "org.opencontainers.image.revision"="02d02ad5d9d5ef0add399eb1c8d5f2a4b9261204" "build-date"="2025-11-03T14:27:54Z" "release"="1762180032"org.opencontainers.image.revision=02d02ad5d9d5ef0add399eb1c8d5f2a4b9261204
# Wed, 12 Nov 2025 00:29:00 GMT
EXPOSE map[5601/tcp:{}]
# Wed, 12 Nov 2025 00:29:00 GMT
RUN microdnf install --setopt=tsflags=nodocs -y       fontconfig liberation-fonts-common freetype shadow-utils nss findutils &&       microdnf clean all # buildkit
# Wed, 12 Nov 2025 00:37:38 GMT
COPY --chown=1000:0 /usr/share/kibana /usr/share/kibana # buildkit
# Wed, 12 Nov 2025 00:37:38 GMT
COPY --chown=0:0 /bin/tini /bin/tini # buildkit
# Wed, 12 Nov 2025 00:37:38 GMT
COPY --chown=0:0 /usr/share/fonts/local/NotoSansCJK-Regular.ttc /usr/share/fonts/local/NotoSansCJK-Regular.ttc # buildkit
# Wed, 12 Nov 2025 00:37:38 GMT
RUN fc-cache -v # buildkit
# Wed, 12 Nov 2025 00:37:39 GMT
WORKDIR /usr/share/kibana
# Wed, 12 Nov 2025 00:37:39 GMT
RUN ln -s /usr/share/kibana /opt/kibana # buildkit
# Wed, 12 Nov 2025 00:37:39 GMT
ENV ELASTIC_CONTAINER=true
# Wed, 12 Nov 2025 00:37:39 GMT
ENV PATH=/usr/share/kibana/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 12 Nov 2025 00:37:39 GMT
COPY --chown=1000:0 config/kibana.yml /usr/share/kibana/config/kibana.yml # buildkit
# Wed, 12 Nov 2025 00:37:39 GMT
COPY bin/kibana-docker /usr/local/bin/ # buildkit
# Wed, 12 Nov 2025 00:37:39 GMT
RUN chmod g+ws /usr/share/kibana &&     find /usr/share/kibana -gid 0 -and -not -perm /g+w -exec chmod g+w {} \; # buildkit
# Wed, 12 Nov 2025 00:37:40 GMT
RUN find / -xdev -perm -4000 -exec chmod u-s {} + # buildkit
# Wed, 12 Nov 2025 00:37:40 GMT
RUN groupadd --gid 1000 kibana &&     useradd --uid 1000 --gid 1000 -G 0       --home-dir /usr/share/kibana --no-create-home       kibana # buildkit
# Wed, 12 Nov 2025 00:37:40 GMT
LABEL org.label-schema.build-date=2025-11-06T13:28:44.453Z org.label-schema.license=Elastic License org.label-schema.name=Kibana org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/kibana org.label-schema.usage=https://www.elastic.co/guide/en/kibana/reference/index.html org.label-schema.vcs-ref=6c427d979e2b3a65eea87f31ba4b65dc579ee2f0 org.label-schema.vcs-url=https://github.com/elastic/kibana org.label-schema.vendor=Elastic org.label-schema.version=9.1.7 org.opencontainers.image.created=2025-11-06T13:28:44.453Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/kibana/reference/index.html org.opencontainers.image.licenses=Elastic License org.opencontainers.image.revision=6c427d979e2b3a65eea87f31ba4b65dc579ee2f0 org.opencontainers.image.source=https://github.com/elastic/kibana org.opencontainers.image.title=Kibana org.opencontainers.image.url=https://www.elastic.co/products/kibana org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=9.1.7
# Wed, 12 Nov 2025 00:37:40 GMT
LABEL name=Kibana maintainer=infra@elastic.co vendor=Elastic version=9.1.7 release=1 summary=Kibana description=Your window into the Elastic Stack.
# Wed, 12 Nov 2025 00:37:41 GMT
RUN mkdir /licenses && ln LICENSE.txt /licenses/LICENSE # buildkit
# Wed, 12 Nov 2025 00:37:41 GMT
ENTRYPOINT ["/bin/tini" "--"]
# Wed, 12 Nov 2025 00:37:41 GMT
CMD ["/usr/local/bin/kibana-docker"]
# Wed, 12 Nov 2025 00:37:41 GMT
USER 1000
```

-	Layers:
	-	`sha256:ef1934e719674e24c0e9879fad65a4a167d4510bb71da2c3ed5e85f5d800bd89`  
		Last Modified: Tue, 11 Nov 2025 17:18:44 GMT  
		Size: 40.0 MB (40000743 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db4c6dce3228bce5ca3d59bd29191ad77d390dadbaeeaaecbaf0e96f91072dd1`  
		Last Modified: Wed, 12 Nov 2025 00:38:55 GMT  
		Size: 19.5 MB (19526921 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec4a5e98c3ac2c37ac3dca8cf81b68d5c92347404b77e71b4f5f9a1ab925e030`  
		Last Modified: Wed, 12 Nov 2025 03:13:47 GMT  
		Size: 361.8 MB (361826472 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62179ba43e56223e97bac2c17355096d27d09fc84eb5031b00cd9b46bd823a26`  
		Last Modified: Wed, 12 Nov 2025 00:38:53 GMT  
		Size: 9.5 KB (9532 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92aed0d8197eb98400b34212185d022b26e747f5de96d38e5bbb10eab74dd0cc`  
		Last Modified: Wed, 12 Nov 2025 00:38:57 GMT  
		Size: 16.5 MB (16460493 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5206b07a821c00db7e44ca1448da1110ef72ed3b98f440c7d10970d9f2ee25b1`  
		Last Modified: Wed, 12 Nov 2025 00:38:54 GMT  
		Size: 5.2 KB (5226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b500fe0e92a52e2727437df1bc0756611e76e267e2b617b560e4474330ce917`  
		Last Modified: Wed, 12 Nov 2025 00:38:55 GMT  
		Size: 132.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:983b506d60118a981e6425a02ab3518854c0c0deb2a8e4da984b4e77967fbbc9`  
		Last Modified: Wed, 12 Nov 2025 00:38:55 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e8a4a75ddd21653777b9d88ceabc36374c38c91eeb0638424d67eb9ff9a5730`  
		Last Modified: Wed, 12 Nov 2025 00:38:55 GMT  
		Size: 4.7 KB (4741 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ddf23f85d47b430fc09bbf8a74f90fb32d0b57dcd5b275239719cfa0d090fd9`  
		Last Modified: Wed, 12 Nov 2025 00:38:56 GMT  
		Size: 401.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5af9b4dec4781ddb7c6e54fe4c0671b3db7d15e97c7ad1d9208464b84e14d3c`  
		Last Modified: Wed, 12 Nov 2025 00:38:56 GMT  
		Size: 74.5 KB (74541 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86e3c9cf9db460baea73061d6c396cada04dcebe265a18aa3275a46bb861d749`  
		Last Modified: Wed, 12 Nov 2025 00:38:57 GMT  
		Size: 1.0 KB (1048 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6117011f25cd30822777ecdbf2016498595691bb5ad1295504c41982c0c19ebd`  
		Last Modified: Wed, 12 Nov 2025 00:38:52 GMT  
		Size: 1.7 KB (1707 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kibana:9.1.7` - unknown; unknown

```console
$ docker pull kibana@sha256:9a371dc44cd52f0e875979a363ef4b6176f0ab575cd74a62ae4218d83e16cb32
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5698743 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:91f8a7001ffd5eb2767831eaa0c5f9c0d42da7741f70112c173b454b5e0d2e5b`

```dockerfile
```

-	Layers:
	-	`sha256:d2219b8c0cfcfb0e3d0deccb8ee531a3ba3ab52eb6c1388c0a809e0f7d991770`  
		Last Modified: Wed, 12 Nov 2025 03:11:23 GMT  
		Size: 5.7 MB (5655517 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:231f700aed105b026e459901420ec1ef2c0c9261ed210e37435a19bf004eb001`  
		Last Modified: Wed, 12 Nov 2025 03:11:24 GMT  
		Size: 43.2 KB (43226 bytes)  
		MIME: application/vnd.in-toto+json

### `kibana:9.1.7` - linux; arm64 variant v8

```console
$ docker pull kibana@sha256:ebbfa07853bd48fb6ebd544ae0446d2fa05032546a5c9c421c4bb3d671de5662
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **449.1 MB (449098521 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca7d7c823c20c55fed50f33209efbe75c3d4961cd232df49384ba9a5f3b700e4`
-	Entrypoint: `["\/bin\/tini","--"]`
-	Default Command: `["\/usr\/local\/bin\/kibana-docker"]`

```dockerfile
# Mon, 03 Nov 2025 14:39:20 GMT
LABEL maintainer="Red Hat, Inc."
# Mon, 03 Nov 2025 14:39:20 GMT
LABEL vendor="Red Hat, Inc."
# Mon, 03 Nov 2025 14:39:20 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Mon, 03 Nov 2025 14:39:20 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.7"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Mon, 03 Nov 2025 14:39:20 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Mon, 03 Nov 2025 14:39:20 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Mon, 03 Nov 2025 14:39:20 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 03 Nov 2025 14:39:20 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 03 Nov 2025 14:39:20 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Mon, 03 Nov 2025 14:39:20 GMT
LABEL io.openshift.expose-services=""
# Mon, 03 Nov 2025 14:39:20 GMT
LABEL io.openshift.tags="minimal rhel9"
# Mon, 03 Nov 2025 14:39:20 GMT
LABEL compose-id="RHEL-9.7.0-updates-20251029.7"
# Mon, 03 Nov 2025 14:39:20 GMT
ENV container oci
# Mon, 03 Nov 2025 14:39:21 GMT
COPY dir:e6638cbef7baa2be94a007ecfd2531710d358328001d7cc1a125e3837ced3f20 in /      
# Mon, 03 Nov 2025 14:39:21 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Mon, 03 Nov 2025 14:39:21 GMT
CMD ["/bin/bash"]
# Mon, 03 Nov 2025 14:39:21 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /usr/share/buildinfo/content-sets.json      
# Mon, 03 Nov 2025 14:39:21 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /root/buildinfo/content_manifests/content-sets.json      
# Mon, 03 Nov 2025 14:39:21 GMT
COPY file:e6c4ae052c98b0a8455fbdd83ea8c94d3ab007cf48a3ddf7f4cddb8006394bb4 in /usr/share/buildinfo/labels.json      
# Mon, 03 Nov 2025 14:39:21 GMT
COPY file:e6c4ae052c98b0a8455fbdd83ea8c94d3ab007cf48a3ddf7f4cddb8006394bb4 in /root/buildinfo/labels.json      
# Mon, 03 Nov 2025 14:39:21 GMT
LABEL "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="02d02ad5d9d5ef0add399eb1c8d5f2a4b9261204" "org.opencontainers.image.revision"="02d02ad5d9d5ef0add399eb1c8d5f2a4b9261204" "build-date"="2025-11-03T14:39:04Z" "release"="1762180032"org.opencontainers.image.revision=02d02ad5d9d5ef0add399eb1c8d5f2a4b9261204
# Wed, 12 Nov 2025 00:26:46 GMT
EXPOSE map[5601/tcp:{}]
# Wed, 12 Nov 2025 00:26:46 GMT
RUN microdnf install --setopt=tsflags=nodocs -y       fontconfig liberation-fonts-common freetype shadow-utils nss findutils &&       microdnf clean all # buildkit
# Wed, 12 Nov 2025 00:33:33 GMT
COPY --chown=1000:0 /usr/share/kibana /usr/share/kibana # buildkit
# Wed, 12 Nov 2025 00:33:34 GMT
COPY --chown=0:0 /bin/tini /bin/tini # buildkit
# Wed, 12 Nov 2025 00:33:34 GMT
COPY --chown=0:0 /usr/share/fonts/local/NotoSansCJK-Regular.ttc /usr/share/fonts/local/NotoSansCJK-Regular.ttc # buildkit
# Wed, 12 Nov 2025 00:33:34 GMT
RUN fc-cache -v # buildkit
# Wed, 12 Nov 2025 00:33:34 GMT
WORKDIR /usr/share/kibana
# Wed, 12 Nov 2025 00:33:34 GMT
RUN ln -s /usr/share/kibana /opt/kibana # buildkit
# Wed, 12 Nov 2025 00:33:34 GMT
ENV ELASTIC_CONTAINER=true
# Wed, 12 Nov 2025 00:33:34 GMT
ENV PATH=/usr/share/kibana/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 12 Nov 2025 00:33:34 GMT
COPY --chown=1000:0 config/kibana.yml /usr/share/kibana/config/kibana.yml # buildkit
# Wed, 12 Nov 2025 00:33:34 GMT
COPY bin/kibana-docker /usr/local/bin/ # buildkit
# Wed, 12 Nov 2025 00:33:35 GMT
RUN chmod g+ws /usr/share/kibana &&     find /usr/share/kibana -gid 0 -and -not -perm /g+w -exec chmod g+w {} \; # buildkit
# Wed, 12 Nov 2025 00:33:36 GMT
RUN find / -xdev -perm -4000 -exec chmod u-s {} + # buildkit
# Wed, 12 Nov 2025 00:33:36 GMT
RUN groupadd --gid 1000 kibana &&     useradd --uid 1000 --gid 1000 -G 0       --home-dir /usr/share/kibana --no-create-home       kibana # buildkit
# Wed, 12 Nov 2025 00:33:36 GMT
LABEL org.label-schema.build-date=2025-11-06T13:28:44.453Z org.label-schema.license=Elastic License org.label-schema.name=Kibana org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/kibana org.label-schema.usage=https://www.elastic.co/guide/en/kibana/reference/index.html org.label-schema.vcs-ref=6c427d979e2b3a65eea87f31ba4b65dc579ee2f0 org.label-schema.vcs-url=https://github.com/elastic/kibana org.label-schema.vendor=Elastic org.label-schema.version=9.1.7 org.opencontainers.image.created=2025-11-06T13:28:44.453Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/kibana/reference/index.html org.opencontainers.image.licenses=Elastic License org.opencontainers.image.revision=6c427d979e2b3a65eea87f31ba4b65dc579ee2f0 org.opencontainers.image.source=https://github.com/elastic/kibana org.opencontainers.image.title=Kibana org.opencontainers.image.url=https://www.elastic.co/products/kibana org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=9.1.7
# Wed, 12 Nov 2025 00:33:36 GMT
LABEL name=Kibana maintainer=infra@elastic.co vendor=Elastic version=9.1.7 release=1 summary=Kibana description=Your window into the Elastic Stack.
# Wed, 12 Nov 2025 00:33:36 GMT
RUN mkdir /licenses && ln LICENSE.txt /licenses/LICENSE # buildkit
# Wed, 12 Nov 2025 00:33:36 GMT
ENTRYPOINT ["/bin/tini" "--"]
# Wed, 12 Nov 2025 00:33:36 GMT
CMD ["/usr/local/bin/kibana-docker"]
# Wed, 12 Nov 2025 00:33:36 GMT
USER 1000
```

-	Layers:
	-	`sha256:fccdcd3fc47f898d65f9d4531d01539ce33a7ec8038500d557bfe58eb4b6ae87`  
		Last Modified: Tue, 11 Nov 2025 18:10:59 GMT  
		Size: 38.2 MB (38211473 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1836dc0ac94038ce49765a4bb767e8466923855bff6c64560c7565c81b68d302`  
		Last Modified: Wed, 12 Nov 2025 00:34:58 GMT  
		Size: 19.5 MB (19485951 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b4d48a345c660c47982fddddc6715824c4707c89974bb87437f37590a072b94`  
		Last Modified: Wed, 12 Nov 2025 03:15:57 GMT  
		Size: 374.8 MB (374844391 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89ae6eefb3bfb209ccd72fdfa522de65a082a9489eb393316d2e765b045e333e`  
		Last Modified: Wed, 12 Nov 2025 00:34:56 GMT  
		Size: 9.1 KB (9100 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5c0f8a2392b6ba770d978ed150c7b3087e065727c206e29ad974365d725c5c9`  
		Last Modified: Wed, 12 Nov 2025 00:34:58 GMT  
		Size: 16.5 MB (16460484 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:662ea5f47db869ed3bc9abde65821120f9707c84abfb8370d906a60bef145bf9`  
		Last Modified: Wed, 12 Nov 2025 00:34:56 GMT  
		Size: 5.2 KB (5225 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63b00797498b64cb94acc5e77fa4f9685ffa11800bfb1a96d17b4d83db5a85fe`  
		Last Modified: Wed, 12 Nov 2025 00:34:57 GMT  
		Size: 131.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3a8c5a8bda321e7459a75628a3918944c47f9d961c254c3af48c07ed2d7dfc7`  
		Last Modified: Wed, 12 Nov 2025 00:34:56 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88c6e9e00eb738ad03dddff75f8e16593e9e8e7179166db0a607b3ef544960e5`  
		Last Modified: Wed, 12 Nov 2025 00:34:57 GMT  
		Size: 4.7 KB (4740 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f12af722e687435e381da56b9fe9ab813d2836c2b3d51606054442da14d9a88`  
		Last Modified: Wed, 12 Nov 2025 00:34:56 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23da0621e9bab27ed870c919daca297ce3ba87caad193facfc34f68a3f3b004d`  
		Last Modified: Wed, 12 Nov 2025 00:34:57 GMT  
		Size: 73.4 KB (73449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f390352db751d10ac7fe1fb6f12105634e5874d813ac812447fb23ec98fd1bad`  
		Last Modified: Wed, 12 Nov 2025 00:34:57 GMT  
		Size: 1.0 KB (1044 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2c6afe35b82ebd7d951eefa1d8c955733c8bb854f9077f3ec31634bda163c7f`  
		Last Modified: Wed, 12 Nov 2025 00:34:57 GMT  
		Size: 1.7 KB (1707 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kibana:9.1.7` - unknown; unknown

```console
$ docker pull kibana@sha256:ae5be6e4fe9f2c4caf25a94eef55ab579625f44716c502d7237b04a13c69f2c2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5697676 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a69af6112819ab818a609df1eb3f0883b593b67d6ffeb8c06a4d696eff6e5dac`

```dockerfile
```

-	Layers:
	-	`sha256:0d75e7158a44f256eede00cf3e3baea72598dcd5da66c21db3b9a52b68cbe8b1`  
		Last Modified: Wed, 12 Nov 2025 03:11:29 GMT  
		Size: 5.7 MB (5654193 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ff8fdc6a0ed10115ce8a63d5d33927c24c17c96dfeeab191dbb11224b5d86540`  
		Last Modified: Wed, 12 Nov 2025 03:11:30 GMT  
		Size: 43.5 KB (43483 bytes)  
		MIME: application/vnd.in-toto+json

## `kibana:9.2.1`

```console
$ docker pull kibana@sha256:46e75a3a22dd5b1ffceb073fda692f8d222c45d96407e74d04f47de36fe8bc03
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `kibana:9.2.1` - linux; amd64

```console
$ docker pull kibana@sha256:d1a6dc6a462dd476d81efbe860cc52c7bbdc1848bc4c1a8e8245d2d0b86de722
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **436.3 MB (436282901 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1dea35de6a1083ab6aa702a8cd572a1e84b2c9208b560cae43147e0a7b13b4b2`
-	Entrypoint: `["\/bin\/tini","--"]`
-	Default Command: `["\/usr\/local\/bin\/kibana-docker"]`

```dockerfile
# Mon, 03 Nov 2025 14:28:07 GMT
LABEL maintainer="Red Hat, Inc."
# Mon, 03 Nov 2025 14:28:07 GMT
LABEL vendor="Red Hat, Inc."
# Mon, 03 Nov 2025 14:28:07 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Mon, 03 Nov 2025 14:28:07 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.7"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Mon, 03 Nov 2025 14:28:07 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Mon, 03 Nov 2025 14:28:07 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Mon, 03 Nov 2025 14:28:07 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 03 Nov 2025 14:28:07 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 03 Nov 2025 14:28:07 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Mon, 03 Nov 2025 14:28:07 GMT
LABEL io.openshift.expose-services=""
# Mon, 03 Nov 2025 14:28:07 GMT
LABEL io.openshift.tags="minimal rhel9"
# Mon, 03 Nov 2025 14:28:07 GMT
LABEL compose-id="RHEL-9.7.0-updates-20251029.7"
# Mon, 03 Nov 2025 14:28:07 GMT
ENV container oci
# Mon, 03 Nov 2025 14:28:08 GMT
COPY dir:39710e73aef560d625154347dc7e6b417064723d33d900483645d9d706c0f7a2 in /      
# Mon, 03 Nov 2025 14:28:08 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Mon, 03 Nov 2025 14:28:08 GMT
CMD ["/bin/bash"]
# Mon, 03 Nov 2025 14:28:08 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /usr/share/buildinfo/content-sets.json      
# Mon, 03 Nov 2025 14:28:08 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /root/buildinfo/content_manifests/content-sets.json      
# Mon, 03 Nov 2025 14:28:08 GMT
COPY file:90c5e1a95185d091ee07721ff43a8413d78a6f7cb920f7ce46a03a173e5f926a in /usr/share/buildinfo/labels.json      
# Mon, 03 Nov 2025 14:28:08 GMT
COPY file:90c5e1a95185d091ee07721ff43a8413d78a6f7cb920f7ce46a03a173e5f926a in /root/buildinfo/labels.json      
# Mon, 03 Nov 2025 14:28:09 GMT
LABEL "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="02d02ad5d9d5ef0add399eb1c8d5f2a4b9261204" "org.opencontainers.image.revision"="02d02ad5d9d5ef0add399eb1c8d5f2a4b9261204" "build-date"="2025-11-03T14:27:54Z" "release"="1762180032"org.opencontainers.image.revision=02d02ad5d9d5ef0add399eb1c8d5f2a4b9261204
# Wed, 12 Nov 2025 00:28:59 GMT
EXPOSE map[5601/tcp:{}]
# Wed, 12 Nov 2025 00:28:59 GMT
RUN microdnf install --setopt=tsflags=nodocs -y       fontconfig liberation-fonts-common freetype shadow-utils nss findutils &&       microdnf clean all # buildkit
# Wed, 12 Nov 2025 00:37:14 GMT
COPY --chown=1000:0 /usr/share/kibana /usr/share/kibana # buildkit
# Wed, 12 Nov 2025 00:37:15 GMT
COPY --chown=0:0 /bin/tini /bin/tini # buildkit
# Wed, 12 Nov 2025 00:37:15 GMT
COPY --chown=0:0 /usr/share/fonts/local/NotoSansCJK-Regular.ttc /usr/share/fonts/local/NotoSansCJK-Regular.ttc # buildkit
# Wed, 12 Nov 2025 00:37:15 GMT
RUN fc-cache -v # buildkit
# Wed, 12 Nov 2025 00:37:15 GMT
WORKDIR /usr/share/kibana
# Wed, 12 Nov 2025 00:37:15 GMT
RUN ln -s /usr/share/kibana /opt/kibana # buildkit
# Wed, 12 Nov 2025 00:37:15 GMT
ENV ELASTIC_CONTAINER=true
# Wed, 12 Nov 2025 00:37:15 GMT
ENV PATH=/usr/share/kibana/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 12 Nov 2025 00:37:15 GMT
COPY --chown=1000:0 config/kibana.yml /usr/share/kibana/config/kibana.yml # buildkit
# Wed, 12 Nov 2025 00:37:15 GMT
COPY bin/kibana-docker /usr/local/bin/ # buildkit
# Wed, 12 Nov 2025 00:37:16 GMT
RUN chmod g+ws /usr/share/kibana &&     find /usr/share/kibana -gid 0 -and -not -perm /g+w -exec chmod g+w {} \; # buildkit
# Wed, 12 Nov 2025 00:37:16 GMT
RUN find / -xdev -perm -4000 -exec chmod u-s {} + # buildkit
# Wed, 12 Nov 2025 00:37:16 GMT
RUN groupadd --gid 1000 kibana &&     useradd --uid 1000 --gid 1000 -G 0       --home-dir /usr/share/kibana --no-create-home       kibana # buildkit
# Wed, 12 Nov 2025 00:37:16 GMT
LABEL org.label-schema.build-date=2025-11-06T12:31:22.639Z org.label-schema.license=Elastic License org.label-schema.name=Kibana org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/kibana org.label-schema.usage=https://www.elastic.co/guide/en/kibana/reference/index.html org.label-schema.vcs-ref=2b1aec68b05596d5cbe93d7444cd128f814ef600 org.label-schema.vcs-url=https://github.com/elastic/kibana org.label-schema.vendor=Elastic org.label-schema.version=9.2.1 org.opencontainers.image.created=2025-11-06T12:31:22.639Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/kibana/reference/index.html org.opencontainers.image.licenses=Elastic License org.opencontainers.image.revision=2b1aec68b05596d5cbe93d7444cd128f814ef600 org.opencontainers.image.source=https://github.com/elastic/kibana org.opencontainers.image.title=Kibana org.opencontainers.image.url=https://www.elastic.co/products/kibana org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=9.2.1
# Wed, 12 Nov 2025 00:37:16 GMT
LABEL name=Kibana maintainer=infra@elastic.co vendor=Elastic version=9.2.1 release=1 summary=Kibana description=Your window into the Elastic Stack.
# Wed, 12 Nov 2025 00:37:17 GMT
RUN mkdir /licenses && ln LICENSE.txt /licenses/LICENSE # buildkit
# Wed, 12 Nov 2025 00:37:17 GMT
ENTRYPOINT ["/bin/tini" "--"]
# Wed, 12 Nov 2025 00:37:17 GMT
CMD ["/usr/local/bin/kibana-docker"]
# Wed, 12 Nov 2025 00:37:17 GMT
USER 1000
```

-	Layers:
	-	`sha256:ef1934e719674e24c0e9879fad65a4a167d4510bb71da2c3ed5e85f5d800bd89`  
		Last Modified: Tue, 11 Nov 2025 17:18:44 GMT  
		Size: 40.0 MB (40000743 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5ad9fd9ce672ef9b2fa7d4bba1bf5339593c472c7198b86236186d4cc0ad3b6`  
		Last Modified: Wed, 12 Nov 2025 00:38:26 GMT  
		Size: 19.5 MB (19526963 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab0f9a20e8234fd2550a90e0240b91d32ecc099519fb3a0ba400ddc1620d9022`  
		Last Modified: Wed, 12 Nov 2025 03:13:46 GMT  
		Size: 360.2 MB (360196797 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f5b685867ed715467dcbd3933874f17ac3438751e8394833d4b4660579d3097`  
		Last Modified: Wed, 12 Nov 2025 00:38:24 GMT  
		Size: 9.5 KB (9532 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0a1aeadcabbfc6967ba6da4f0dce1b761d4124355946b56f02e57537d5ae624`  
		Last Modified: Wed, 12 Nov 2025 00:38:25 GMT  
		Size: 16.5 MB (16460488 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efc4cb76b4f3d5a5e1d7c91a4586427fd7608fd7239b899368629c96bad9a67e`  
		Last Modified: Wed, 12 Nov 2025 00:38:25 GMT  
		Size: 5.2 KB (5227 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4e1e2ab8407318ecc9cea87e1825785d6eebc0bd915645f99050ec2f3495888`  
		Last Modified: Wed, 12 Nov 2025 00:38:25 GMT  
		Size: 131.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89063f79f48bea4184d5496f36985b391556616ba58e68175398da816d09c3a7`  
		Last Modified: Wed, 12 Nov 2025 00:38:25 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3fbb0d5e91a4e1175031305ac93baad66d5d013d6ae4320f53349a1f10a302f`  
		Last Modified: Wed, 12 Nov 2025 00:38:26 GMT  
		Size: 4.9 KB (4895 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de1f0c550706cc0ae683868b82f6b2ac0266f8479f885f41f003dc0a9c9ec1f4`  
		Last Modified: Wed, 12 Nov 2025 00:38:26 GMT  
		Size: 400.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d60f0e5901e9ea6cab278a30f0d68b7751d0d370eacb7f95b98745dd11c17b57`  
		Last Modified: Wed, 12 Nov 2025 00:38:26 GMT  
		Size: 74.5 KB (74543 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:feba1dcb9172dc89dade6c4b9f5e4a13d93d27c846b8dd0961396a97d2dc8375`  
		Last Modified: Wed, 12 Nov 2025 00:38:26 GMT  
		Size: 1.0 KB (1045 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32ff531933d79360255648154eefe0b1064d8f1d667cdadfaf8906d455f60895`  
		Last Modified: Wed, 12 Nov 2025 00:38:22 GMT  
		Size: 1.7 KB (1708 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kibana:9.2.1` - unknown; unknown

```console
$ docker pull kibana@sha256:f671bab067da3ec55fb1a5d1fa1e5585066feca9fe84f9652a331bf55a451dc9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5756466 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b7f298e1eae86d91535565efc2f31c6a8e74a6384476aabb2b434f056a4127f7`

```dockerfile
```

-	Layers:
	-	`sha256:3c5ba737c3b5f8051f16c4b4059487ec4264ca12dc08889f6335854ad4f7772b`  
		Last Modified: Wed, 12 Nov 2025 03:11:32 GMT  
		Size: 5.7 MB (5713240 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:29593bd7d30f6ff10fc6247c405ac2eadf9c8aed3f6a0dee8c39923d621a4077`  
		Last Modified: Wed, 12 Nov 2025 03:11:33 GMT  
		Size: 43.2 KB (43226 bytes)  
		MIME: application/vnd.in-toto+json

### `kibana:9.2.1` - linux; arm64 variant v8

```console
$ docker pull kibana@sha256:37d77e43f598f1e5e1e46ea7e18c75febb812a2788181baca64d54d72d3bac72
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **447.5 MB (447484112 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a9c25a8d9486c2b382c4ac8998093ab42f2b67fb0b0340a5ddd350117badd83`
-	Entrypoint: `["\/bin\/tini","--"]`
-	Default Command: `["\/usr\/local\/bin\/kibana-docker"]`

```dockerfile
# Mon, 03 Nov 2025 14:39:20 GMT
LABEL maintainer="Red Hat, Inc."
# Mon, 03 Nov 2025 14:39:20 GMT
LABEL vendor="Red Hat, Inc."
# Mon, 03 Nov 2025 14:39:20 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Mon, 03 Nov 2025 14:39:20 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.7"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Mon, 03 Nov 2025 14:39:20 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Mon, 03 Nov 2025 14:39:20 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Mon, 03 Nov 2025 14:39:20 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 03 Nov 2025 14:39:20 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 03 Nov 2025 14:39:20 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Mon, 03 Nov 2025 14:39:20 GMT
LABEL io.openshift.expose-services=""
# Mon, 03 Nov 2025 14:39:20 GMT
LABEL io.openshift.tags="minimal rhel9"
# Mon, 03 Nov 2025 14:39:20 GMT
LABEL compose-id="RHEL-9.7.0-updates-20251029.7"
# Mon, 03 Nov 2025 14:39:20 GMT
ENV container oci
# Mon, 03 Nov 2025 14:39:21 GMT
COPY dir:e6638cbef7baa2be94a007ecfd2531710d358328001d7cc1a125e3837ced3f20 in /      
# Mon, 03 Nov 2025 14:39:21 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Mon, 03 Nov 2025 14:39:21 GMT
CMD ["/bin/bash"]
# Mon, 03 Nov 2025 14:39:21 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /usr/share/buildinfo/content-sets.json      
# Mon, 03 Nov 2025 14:39:21 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /root/buildinfo/content_manifests/content-sets.json      
# Mon, 03 Nov 2025 14:39:21 GMT
COPY file:e6c4ae052c98b0a8455fbdd83ea8c94d3ab007cf48a3ddf7f4cddb8006394bb4 in /usr/share/buildinfo/labels.json      
# Mon, 03 Nov 2025 14:39:21 GMT
COPY file:e6c4ae052c98b0a8455fbdd83ea8c94d3ab007cf48a3ddf7f4cddb8006394bb4 in /root/buildinfo/labels.json      
# Mon, 03 Nov 2025 14:39:21 GMT
LABEL "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="02d02ad5d9d5ef0add399eb1c8d5f2a4b9261204" "org.opencontainers.image.revision"="02d02ad5d9d5ef0add399eb1c8d5f2a4b9261204" "build-date"="2025-11-03T14:39:04Z" "release"="1762180032"org.opencontainers.image.revision=02d02ad5d9d5ef0add399eb1c8d5f2a4b9261204
# Wed, 12 Nov 2025 00:27:47 GMT
EXPOSE map[5601/tcp:{}]
# Wed, 12 Nov 2025 00:27:47 GMT
RUN microdnf install --setopt=tsflags=nodocs -y       fontconfig liberation-fonts-common freetype shadow-utils nss findutils &&       microdnf clean all # buildkit
# Wed, 12 Nov 2025 00:35:06 GMT
COPY --chown=1000:0 /usr/share/kibana /usr/share/kibana # buildkit
# Wed, 12 Nov 2025 00:35:07 GMT
COPY --chown=0:0 /bin/tini /bin/tini # buildkit
# Wed, 12 Nov 2025 00:35:07 GMT
COPY --chown=0:0 /usr/share/fonts/local/NotoSansCJK-Regular.ttc /usr/share/fonts/local/NotoSansCJK-Regular.ttc # buildkit
# Wed, 12 Nov 2025 00:35:07 GMT
RUN fc-cache -v # buildkit
# Wed, 12 Nov 2025 00:35:07 GMT
WORKDIR /usr/share/kibana
# Wed, 12 Nov 2025 00:35:07 GMT
RUN ln -s /usr/share/kibana /opt/kibana # buildkit
# Wed, 12 Nov 2025 00:35:07 GMT
ENV ELASTIC_CONTAINER=true
# Wed, 12 Nov 2025 00:35:07 GMT
ENV PATH=/usr/share/kibana/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 12 Nov 2025 00:35:07 GMT
COPY --chown=1000:0 config/kibana.yml /usr/share/kibana/config/kibana.yml # buildkit
# Wed, 12 Nov 2025 00:35:07 GMT
COPY bin/kibana-docker /usr/local/bin/ # buildkit
# Wed, 12 Nov 2025 00:35:08 GMT
RUN chmod g+ws /usr/share/kibana &&     find /usr/share/kibana -gid 0 -and -not -perm /g+w -exec chmod g+w {} \; # buildkit
# Wed, 12 Nov 2025 00:35:09 GMT
RUN find / -xdev -perm -4000 -exec chmod u-s {} + # buildkit
# Wed, 12 Nov 2025 00:35:09 GMT
RUN groupadd --gid 1000 kibana &&     useradd --uid 1000 --gid 1000 -G 0       --home-dir /usr/share/kibana --no-create-home       kibana # buildkit
# Wed, 12 Nov 2025 00:35:09 GMT
LABEL org.label-schema.build-date=2025-11-06T12:31:22.639Z org.label-schema.license=Elastic License org.label-schema.name=Kibana org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/kibana org.label-schema.usage=https://www.elastic.co/guide/en/kibana/reference/index.html org.label-schema.vcs-ref=2b1aec68b05596d5cbe93d7444cd128f814ef600 org.label-schema.vcs-url=https://github.com/elastic/kibana org.label-schema.vendor=Elastic org.label-schema.version=9.2.1 org.opencontainers.image.created=2025-11-06T12:31:22.639Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/kibana/reference/index.html org.opencontainers.image.licenses=Elastic License org.opencontainers.image.revision=2b1aec68b05596d5cbe93d7444cd128f814ef600 org.opencontainers.image.source=https://github.com/elastic/kibana org.opencontainers.image.title=Kibana org.opencontainers.image.url=https://www.elastic.co/products/kibana org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=9.2.1
# Wed, 12 Nov 2025 00:35:09 GMT
LABEL name=Kibana maintainer=infra@elastic.co vendor=Elastic version=9.2.1 release=1 summary=Kibana description=Your window into the Elastic Stack.
# Wed, 12 Nov 2025 00:35:09 GMT
RUN mkdir /licenses && ln LICENSE.txt /licenses/LICENSE # buildkit
# Wed, 12 Nov 2025 00:35:09 GMT
ENTRYPOINT ["/bin/tini" "--"]
# Wed, 12 Nov 2025 00:35:09 GMT
CMD ["/usr/local/bin/kibana-docker"]
# Wed, 12 Nov 2025 00:35:09 GMT
USER 1000
```

-	Layers:
	-	`sha256:fccdcd3fc47f898d65f9d4531d01539ce33a7ec8038500d557bfe58eb4b6ae87`  
		Last Modified: Tue, 11 Nov 2025 18:10:59 GMT  
		Size: 38.2 MB (38211473 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf529e29085c0d41b6dac0b774fc80c69c53ce3246cc2c06496c5d94222a29f5`  
		Last Modified: Wed, 12 Nov 2025 00:36:29 GMT  
		Size: 19.5 MB (19485971 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:afeb073da0920b42ea87d2375bc8641f6b8eeb14f0ec646660d88b96e88099c5`  
		Last Modified: Wed, 12 Nov 2025 03:16:56 GMT  
		Size: 373.2 MB (373229801 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:afbdfd51aaed820266869ec57d61f4d50c24d142fd92b065e7ad1507d5fc05d8`  
		Last Modified: Wed, 12 Nov 2025 00:36:28 GMT  
		Size: 9.1 KB (9102 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2b9dbb059cf0e80682f7e4c81029daf5c5201a82beaecf019919fa14f22a730`  
		Last Modified: Wed, 12 Nov 2025 00:36:32 GMT  
		Size: 16.5 MB (16460488 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12acf10dbe0c46ecce0bf7ad1f195aad86fb386f736d763e2dff6687c1b399f0`  
		Last Modified: Wed, 12 Nov 2025 00:36:29 GMT  
		Size: 5.2 KB (5225 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ee9adf581c71ed505cafdaecc818a44ca6b7946f40d1354368eee85be4581f5`  
		Last Modified: Wed, 12 Nov 2025 00:36:30 GMT  
		Size: 131.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5f7607db996f7c057cc00c4572c2ab0e51a93f4fd60c9dcf2f1517906759079`  
		Last Modified: Wed, 12 Nov 2025 00:36:30 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8410ec8332fde43df905ddf971762f092e59bbe1a807ea3e750ec27d89c5dd9f`  
		Last Modified: Wed, 12 Nov 2025 00:36:30 GMT  
		Size: 4.9 KB (4893 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0511952508427deca5b1e1cd712229b3d143beb5637107db1b96bccabfc101d5`  
		Last Modified: Wed, 12 Nov 2025 00:36:34 GMT  
		Size: 399.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80ce02ca95ca3e8437bfcb975703d16ea39b9b6ae825ae0b0dce9aa389ac97ad`  
		Last Modified: Wed, 12 Nov 2025 00:36:31 GMT  
		Size: 73.4 KB (73449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d32d659d46eec44dd79b97aa17711371e72b2330e859ef6c1114c23104525b2d`  
		Last Modified: Wed, 12 Nov 2025 00:36:31 GMT  
		Size: 1.0 KB (1045 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61f6989e839f9c96e995957508d38dfc2a3c26ff31a9095d23d6469c598ef936`  
		Last Modified: Wed, 12 Nov 2025 00:36:26 GMT  
		Size: 1.7 KB (1707 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kibana:9.2.1` - unknown; unknown

```console
$ docker pull kibana@sha256:6084e85585a2916d697748050bb93c7bf6068acea951926c55b214aa894e6722
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5755399 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d3888488895548ef0facbcac6c58034cee597e679484f2c8a26ba1f6f86e5dc6`

```dockerfile
```

-	Layers:
	-	`sha256:b4a493b87f231be92d229b3d06076f323ea9ead60504467bba5a89385a81f455`  
		Last Modified: Wed, 12 Nov 2025 03:11:38 GMT  
		Size: 5.7 MB (5711916 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:36b241ad4929df5124d962ac127de9f558245e0e0908257a71acd704b6beef99`  
		Last Modified: Wed, 12 Nov 2025 03:11:39 GMT  
		Size: 43.5 KB (43483 bytes)  
		MIME: application/vnd.in-toto+json
