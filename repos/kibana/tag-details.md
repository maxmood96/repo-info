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
$ docker pull kibana@sha256:06ecb60134631629e04ae3b1f0362e81d802d5e66ccf3d18ce204530f55a9c5c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `kibana:9.1.7` - linux; amd64

```console
$ docker pull kibana@sha256:8ee903a2317ee42a912cd84a6e55e6d1066ac8b33699a87e3231132ade43c122
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **441.9 MB (441879893 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c9a7595b0ac2bea3638be7210eec573a44077efae04bf21f6ad8ba89b5532560`
-	Entrypoint: `["\/bin\/tini","--"]`
-	Default Command: `["\/usr\/local\/bin\/kibana-docker"]`

```dockerfile
# Wed, 15 Oct 2025 08:06:32 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 15 Oct 2025 08:06:32 GMT
LABEL vendor="Red Hat, Inc."
# Wed, 15 Oct 2025 08:06:32 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Wed, 15 Oct 2025 08:06:32 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.6"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Wed, 15 Oct 2025 08:06:32 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 15 Oct 2025 08:06:32 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Wed, 15 Oct 2025 08:06:33 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 15 Oct 2025 08:06:33 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 15 Oct 2025 08:06:33 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Wed, 15 Oct 2025 08:06:33 GMT
LABEL io.openshift.expose-services=""
# Wed, 15 Oct 2025 08:06:33 GMT
LABEL io.openshift.tags="minimal rhel9"
# Wed, 15 Oct 2025 08:06:33 GMT
ENV container oci
# Wed, 15 Oct 2025 08:06:34 GMT
COPY dir:f15650dcc2939ee0c30865212b61e6718fd6c24de4e7967bf7b651b8f0b24352 in /      
# Wed, 15 Oct 2025 08:06:34 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Wed, 15 Oct 2025 08:06:34 GMT
CMD ["/bin/bash"]
# Wed, 15 Oct 2025 08:06:34 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /usr/share/buildinfo/content-sets.json      
# Wed, 15 Oct 2025 08:06:34 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /root/buildinfo/content_manifests/content-sets.json      
# Wed, 15 Oct 2025 08:06:34 GMT
COPY file:16bf5aac480286f91e3031d4f1acb4e76fb8c3be38d180e4713a0efdc39d6bad in /root/buildinfo/labels.json      
# Wed, 15 Oct 2025 08:06:35 GMT
LABEL "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="d1b15a34ce69ea214e1d32f1f501304f6b8b8c59" "org.opencontainers.image.revision"="d1b15a34ce69ea214e1d32f1f501304f6b8b8c59" "build-date"="2025-10-15T08:06:12Z" "release"="1760515502"org.opencontainers.image.revision=d1b15a34ce69ea214e1d32f1f501304f6b8b8c59
# Tue, 11 Nov 2025 18:08:26 GMT
EXPOSE map[5601/tcp:{}]
# Tue, 11 Nov 2025 18:08:26 GMT
RUN microdnf install --setopt=tsflags=nodocs -y       fontconfig liberation-fonts-common freetype shadow-utils nss findutils &&       microdnf clean all # buildkit
# Tue, 11 Nov 2025 18:17:11 GMT
COPY --chown=1000:0 /usr/share/kibana /usr/share/kibana # buildkit
# Tue, 11 Nov 2025 18:17:12 GMT
COPY --chown=0:0 /bin/tini /bin/tini # buildkit
# Tue, 11 Nov 2025 18:17:12 GMT
COPY --chown=0:0 /usr/share/fonts/local/NotoSansCJK-Regular.ttc /usr/share/fonts/local/NotoSansCJK-Regular.ttc # buildkit
# Tue, 11 Nov 2025 18:17:12 GMT
RUN fc-cache -v # buildkit
# Tue, 11 Nov 2025 18:17:12 GMT
WORKDIR /usr/share/kibana
# Tue, 11 Nov 2025 18:17:12 GMT
RUN ln -s /usr/share/kibana /opt/kibana # buildkit
# Tue, 11 Nov 2025 18:17:12 GMT
ENV ELASTIC_CONTAINER=true
# Tue, 11 Nov 2025 18:17:12 GMT
ENV PATH=/usr/share/kibana/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 11 Nov 2025 18:17:12 GMT
COPY --chown=1000:0 config/kibana.yml /usr/share/kibana/config/kibana.yml # buildkit
# Tue, 11 Nov 2025 18:17:12 GMT
COPY bin/kibana-docker /usr/local/bin/ # buildkit
# Tue, 11 Nov 2025 18:17:13 GMT
RUN chmod g+ws /usr/share/kibana &&     find /usr/share/kibana -gid 0 -and -not -perm /g+w -exec chmod g+w {} \; # buildkit
# Tue, 11 Nov 2025 18:17:13 GMT
RUN find / -xdev -perm -4000 -exec chmod u-s {} + # buildkit
# Tue, 11 Nov 2025 18:17:14 GMT
RUN groupadd --gid 1000 kibana &&     useradd --uid 1000 --gid 1000 -G 0       --home-dir /usr/share/kibana --no-create-home       kibana # buildkit
# Tue, 11 Nov 2025 18:17:14 GMT
LABEL org.label-schema.build-date=2025-11-06T13:28:44.453Z org.label-schema.license=Elastic License org.label-schema.name=Kibana org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/kibana org.label-schema.usage=https://www.elastic.co/guide/en/kibana/reference/index.html org.label-schema.vcs-ref=6c427d979e2b3a65eea87f31ba4b65dc579ee2f0 org.label-schema.vcs-url=https://github.com/elastic/kibana org.label-schema.vendor=Elastic org.label-schema.version=9.1.7 org.opencontainers.image.created=2025-11-06T13:28:44.453Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/kibana/reference/index.html org.opencontainers.image.licenses=Elastic License org.opencontainers.image.revision=6c427d979e2b3a65eea87f31ba4b65dc579ee2f0 org.opencontainers.image.source=https://github.com/elastic/kibana org.opencontainers.image.title=Kibana org.opencontainers.image.url=https://www.elastic.co/products/kibana org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=9.1.7
# Tue, 11 Nov 2025 18:17:14 GMT
LABEL name=Kibana maintainer=infra@elastic.co vendor=Elastic version=9.1.7 release=1 summary=Kibana description=Your window into the Elastic Stack.
# Tue, 11 Nov 2025 18:17:14 GMT
RUN mkdir /licenses && ln LICENSE.txt /licenses/LICENSE # buildkit
# Tue, 11 Nov 2025 18:17:14 GMT
ENTRYPOINT ["/bin/tini" "--"]
# Tue, 11 Nov 2025 18:17:14 GMT
CMD ["/usr/local/bin/kibana-docker"]
# Tue, 11 Nov 2025 18:17:14 GMT
USER 1000
```

-	Layers:
	-	`sha256:2920d84eafa0cf94806ab58f0a2124f7b2d35bcbb06fc89a9106dcc28efe397a`  
		Last Modified: Wed, 15 Oct 2025 09:03:15 GMT  
		Size: 39.7 MB (39653524 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7991a4a31087a8b0c840617c46b269fd5b2780847628487d16930ee821469c5`  
		Last Modified: Tue, 11 Nov 2025 18:18:39 GMT  
		Size: 23.8 MB (23841594 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f11acc07db33b8053c8698d10027244646fc231f3d28ec13c14d8f2aeab3fca`  
		Last Modified: Tue, 11 Nov 2025 21:17:23 GMT  
		Size: 361.8 MB (361826512 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3cd25e8b4de3933b6f4e0a3f254d6cf69f37e7d3e1773335230d905924f7a10`  
		Last Modified: Tue, 11 Nov 2025 18:18:37 GMT  
		Size: 9.5 KB (9534 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cdf17c0c4a9720de258e9e5086d66a254e574a99f30f6f02baf083b9aee0b041`  
		Last Modified: Tue, 11 Nov 2025 18:18:38 GMT  
		Size: 16.5 MB (16460491 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f4447014db5a3790956170b33015d0c8ea4564c786ad8e970bea2191ae10251`  
		Last Modified: Tue, 11 Nov 2025 18:18:37 GMT  
		Size: 5.2 KB (5229 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff69325b73cc8f9d8aaa1176661cc9b802fc07dd7f9b7bea8084728a000910b1`  
		Last Modified: Tue, 11 Nov 2025 18:18:38 GMT  
		Size: 130.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b0b3b60bf8ee861b9ef11a4250e9e0798db14fd424561bb49f2594a2fd9b37b`  
		Last Modified: Tue, 11 Nov 2025 18:18:38 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d8fb7693c229f942f4b1979442ce622b8c1383799ae246052749fded02bbe8d`  
		Last Modified: Tue, 11 Nov 2025 18:18:39 GMT  
		Size: 4.7 KB (4745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24e7c389b32ef17b6ab8a987574d029d6b5a5f05318807ddeac4a22697e724a4`  
		Last Modified: Tue, 11 Nov 2025 18:18:38 GMT  
		Size: 399.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea400ee927dd098c9fcc171768b8591a59e474192b1f681a76236929f3d8db70`  
		Last Modified: Tue, 11 Nov 2025 18:18:39 GMT  
		Size: 74.5 KB (74544 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad3752aad89b936f2f6b42a08a86cbb780c4878377d3f416e7ddcbc3be027238`  
		Last Modified: Tue, 11 Nov 2025 18:18:39 GMT  
		Size: 1.1 KB (1058 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12eea04abf38b417fa70f66eab176676292d633cbda5a96b28939c3aec56fba7`  
		Last Modified: Tue, 11 Nov 2025 18:18:35 GMT  
		Size: 1.7 KB (1705 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kibana:9.1.7` - unknown; unknown

```console
$ docker pull kibana@sha256:898cb6ce11dc19e81767caeb49ea2750cc639036c339e966f644df9fece20045
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5698193 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:84088f4b92ec77593adf6cf3bb1a88962bd41480561da58a59df4965ca3f1fac`

```dockerfile
```

-	Layers:
	-	`sha256:6b387182dad1e6c1fee342f52e69ea2551e6c1a231afbaa06316bdcfb6af0cab`  
		Last Modified: Tue, 11 Nov 2025 21:11:32 GMT  
		Size: 5.7 MB (5654967 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:259d3dca0f1e0b3798a6709490d622b8a41aa105ae7c824a53396bc2fdb74899`  
		Last Modified: Tue, 11 Nov 2025 21:11:33 GMT  
		Size: 43.2 KB (43226 bytes)  
		MIME: application/vnd.in-toto+json

### `kibana:9.1.7` - linux; arm64 variant v8

```console
$ docker pull kibana@sha256:39ec3fa2f29fd735983edcf9aa82ace09beca44e9e906c24804af6d668e849b8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **452.9 MB (452851717 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c60ef09f6236780cb0b4ec6b46882d4d66a49bcf0a59a13129d70a21b40cee3`
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
# Tue, 11 Nov 2025 18:08:29 GMT
EXPOSE map[5601/tcp:{}]
# Tue, 11 Nov 2025 18:08:29 GMT
RUN microdnf install --setopt=tsflags=nodocs -y       fontconfig liberation-fonts-common freetype shadow-utils nss findutils &&       microdnf clean all # buildkit
# Tue, 11 Nov 2025 18:15:41 GMT
COPY --chown=1000:0 /usr/share/kibana /usr/share/kibana # buildkit
# Tue, 11 Nov 2025 18:15:41 GMT
COPY --chown=0:0 /bin/tini /bin/tini # buildkit
# Tue, 11 Nov 2025 18:15:41 GMT
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
# Tue, 11 Nov 2025 18:15:43 GMT
RUN find / -xdev -perm -4000 -exec chmod u-s {} + # buildkit
# Tue, 11 Nov 2025 18:15:44 GMT
RUN groupadd --gid 1000 kibana &&     useradd --uid 1000 --gid 1000 -G 0       --home-dir /usr/share/kibana --no-create-home       kibana # buildkit
# Tue, 11 Nov 2025 18:15:44 GMT
LABEL org.label-schema.build-date=2025-11-06T13:28:44.453Z org.label-schema.license=Elastic License org.label-schema.name=Kibana org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/kibana org.label-schema.usage=https://www.elastic.co/guide/en/kibana/reference/index.html org.label-schema.vcs-ref=6c427d979e2b3a65eea87f31ba4b65dc579ee2f0 org.label-schema.vcs-url=https://github.com/elastic/kibana org.label-schema.vendor=Elastic org.label-schema.version=9.1.7 org.opencontainers.image.created=2025-11-06T13:28:44.453Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/kibana/reference/index.html org.opencontainers.image.licenses=Elastic License org.opencontainers.image.revision=6c427d979e2b3a65eea87f31ba4b65dc579ee2f0 org.opencontainers.image.source=https://github.com/elastic/kibana org.opencontainers.image.title=Kibana org.opencontainers.image.url=https://www.elastic.co/products/kibana org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=9.1.7
# Tue, 11 Nov 2025 18:15:44 GMT
LABEL name=Kibana maintainer=infra@elastic.co vendor=Elastic version=9.1.7 release=1 summary=Kibana description=Your window into the Elastic Stack.
# Tue, 11 Nov 2025 18:15:44 GMT
RUN mkdir /licenses && ln LICENSE.txt /licenses/LICENSE # buildkit
# Tue, 11 Nov 2025 18:15:44 GMT
ENTRYPOINT ["/bin/tini" "--"]
# Tue, 11 Nov 2025 18:15:44 GMT
CMD ["/usr/local/bin/kibana-docker"]
# Tue, 11 Nov 2025 18:15:44 GMT
USER 1000
```

-	Layers:
	-	`sha256:2602e1c5e8830fe80a6207359ce01e6c9b7d6848be663c4df1e03c724149b8a6`  
		Last Modified: Wed, 15 Oct 2025 09:30:32 GMT  
		Size: 37.9 MB (37896281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8954c2d252d7373a066210daa02d86811527fa4292b6180f57d776e3f00a6ebf`  
		Last Modified: Tue, 11 Nov 2025 18:17:03 GMT  
		Size: 23.6 MB (23554310 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df488ea7471badb94c1d9fdf0ee155d04c7f2c74ac2e6a50679ac20e627c4a92`  
		Last Modified: Tue, 11 Nov 2025 21:16:42 GMT  
		Size: 374.8 MB (374844392 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa4e2119d9b65bcca2ab806fb99d271b4cba1cb13376bf6623db81aefd344f1d`  
		Last Modified: Tue, 11 Nov 2025 18:17:01 GMT  
		Size: 9.1 KB (9103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b182fa617782d06d8b53c7aac6aa9533cd5c02420b43282fd7344a7084082ac5`  
		Last Modified: Tue, 11 Nov 2025 18:17:02 GMT  
		Size: 16.5 MB (16460491 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f344a0bc0203dbdf14c765e52d3d10b5a566e13db684edd048ec615624189a56`  
		Last Modified: Tue, 11 Nov 2025 18:17:01 GMT  
		Size: 5.2 KB (5223 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a03948b3074d0fa79febb026dd2448bad0dac045f116259350f5e74c402a30a`  
		Last Modified: Tue, 11 Nov 2025 18:17:00 GMT  
		Size: 131.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba402d1194a3d367927bfd6e26d292d12a7460eee280ad22dfda923cad27ddc2`  
		Last Modified: Tue, 11 Nov 2025 18:17:02 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a50dcec774da4053e9f5fe047bec7ad4edeb2141a264ca3167b991d46ea569c4`  
		Last Modified: Tue, 11 Nov 2025 18:17:02 GMT  
		Size: 4.7 KB (4746 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1be57eb532bb0bd69a8599c2f9e77d0b043cf7ed7eebb9b8c954388d9a456764`  
		Last Modified: Tue, 11 Nov 2025 18:17:02 GMT  
		Size: 400.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1892ba0c9262d98e76d3e706e112f3c0474bedf2cb9c4cb1d3d032fa5d376ae`  
		Last Modified: Tue, 11 Nov 2025 18:17:04 GMT  
		Size: 73.5 KB (73453 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d43375a3f5bf1c2170bb9b237c51d4d4a7a43fa803cb9eb219e74ad2b7f43d83`  
		Last Modified: Tue, 11 Nov 2025 18:17:04 GMT  
		Size: 1.1 KB (1052 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aea6a27bf2934e5555899955d710a80c3586e89e042b67c4316e7268358415c4`  
		Last Modified: Tue, 11 Nov 2025 18:16:59 GMT  
		Size: 1.7 KB (1705 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kibana:9.1.7` - unknown; unknown

```console
$ docker pull kibana@sha256:c1d807ba61a65c7387a0e03d8f40eb282e6d368f2018c3215afdc649003737da
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5697128 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc976b33186151e8fe9857e5963c28359f60fdc361c300a5bbd4abe159b206c4`

```dockerfile
```

-	Layers:
	-	`sha256:276f24a536397688dc987d046d70a8db12c81e424869b81ec3a9257f0346804b`  
		Last Modified: Tue, 11 Nov 2025 21:11:39 GMT  
		Size: 5.7 MB (5653645 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:247622451ee2ed7b55f9881ed37e1544c50ab23abd566363fe8fc7988f5cc4ab`  
		Last Modified: Tue, 11 Nov 2025 21:11:41 GMT  
		Size: 43.5 KB (43483 bytes)  
		MIME: application/vnd.in-toto+json

## `kibana:9.2.1`

```console
$ docker pull kibana@sha256:6188d9d6f70a4d363daaf9857fb1ecb8f48a650ab94a6901f7470e6979d09ce9
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `kibana:9.2.1` - linux; amd64

```console
$ docker pull kibana@sha256:4d9eead7b79dc7e0400d732f077a9d2facea41fa201283876a177a3b167e8a47
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **440.3 MB (440250310 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eaa47ccb8a300ecf178117342060a0c6ba28798e9bdfa0ff1272d15e49d8d306`
-	Entrypoint: `["\/bin\/tini","--"]`
-	Default Command: `["\/usr\/local\/bin\/kibana-docker"]`

```dockerfile
# Wed, 15 Oct 2025 08:06:32 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 15 Oct 2025 08:06:32 GMT
LABEL vendor="Red Hat, Inc."
# Wed, 15 Oct 2025 08:06:32 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Wed, 15 Oct 2025 08:06:32 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.6"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Wed, 15 Oct 2025 08:06:32 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 15 Oct 2025 08:06:32 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Wed, 15 Oct 2025 08:06:33 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 15 Oct 2025 08:06:33 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 15 Oct 2025 08:06:33 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Wed, 15 Oct 2025 08:06:33 GMT
LABEL io.openshift.expose-services=""
# Wed, 15 Oct 2025 08:06:33 GMT
LABEL io.openshift.tags="minimal rhel9"
# Wed, 15 Oct 2025 08:06:33 GMT
ENV container oci
# Wed, 15 Oct 2025 08:06:34 GMT
COPY dir:f15650dcc2939ee0c30865212b61e6718fd6c24de4e7967bf7b651b8f0b24352 in /      
# Wed, 15 Oct 2025 08:06:34 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Wed, 15 Oct 2025 08:06:34 GMT
CMD ["/bin/bash"]
# Wed, 15 Oct 2025 08:06:34 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /usr/share/buildinfo/content-sets.json      
# Wed, 15 Oct 2025 08:06:34 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /root/buildinfo/content_manifests/content-sets.json      
# Wed, 15 Oct 2025 08:06:34 GMT
COPY file:16bf5aac480286f91e3031d4f1acb4e76fb8c3be38d180e4713a0efdc39d6bad in /root/buildinfo/labels.json      
# Wed, 15 Oct 2025 08:06:35 GMT
LABEL "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="d1b15a34ce69ea214e1d32f1f501304f6b8b8c59" "org.opencontainers.image.revision"="d1b15a34ce69ea214e1d32f1f501304f6b8b8c59" "build-date"="2025-10-15T08:06:12Z" "release"="1760515502"org.opencontainers.image.revision=d1b15a34ce69ea214e1d32f1f501304f6b8b8c59
# Tue, 11 Nov 2025 18:08:31 GMT
EXPOSE map[5601/tcp:{}]
# Tue, 11 Nov 2025 18:08:31 GMT
RUN microdnf install --setopt=tsflags=nodocs -y       fontconfig liberation-fonts-common freetype shadow-utils nss findutils &&       microdnf clean all # buildkit
# Tue, 11 Nov 2025 18:16:48 GMT
COPY --chown=1000:0 /usr/share/kibana /usr/share/kibana # buildkit
# Tue, 11 Nov 2025 18:16:49 GMT
COPY --chown=0:0 /bin/tini /bin/tini # buildkit
# Tue, 11 Nov 2025 18:16:49 GMT
COPY --chown=0:0 /usr/share/fonts/local/NotoSansCJK-Regular.ttc /usr/share/fonts/local/NotoSansCJK-Regular.ttc # buildkit
# Tue, 11 Nov 2025 18:16:49 GMT
RUN fc-cache -v # buildkit
# Tue, 11 Nov 2025 18:16:49 GMT
WORKDIR /usr/share/kibana
# Tue, 11 Nov 2025 18:16:49 GMT
RUN ln -s /usr/share/kibana /opt/kibana # buildkit
# Tue, 11 Nov 2025 18:16:49 GMT
ENV ELASTIC_CONTAINER=true
# Tue, 11 Nov 2025 18:16:49 GMT
ENV PATH=/usr/share/kibana/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 11 Nov 2025 18:16:49 GMT
COPY --chown=1000:0 config/kibana.yml /usr/share/kibana/config/kibana.yml # buildkit
# Tue, 11 Nov 2025 18:16:49 GMT
COPY bin/kibana-docker /usr/local/bin/ # buildkit
# Tue, 11 Nov 2025 18:16:50 GMT
RUN chmod g+ws /usr/share/kibana &&     find /usr/share/kibana -gid 0 -and -not -perm /g+w -exec chmod g+w {} \; # buildkit
# Tue, 11 Nov 2025 18:16:51 GMT
RUN find / -xdev -perm -4000 -exec chmod u-s {} + # buildkit
# Tue, 11 Nov 2025 18:16:51 GMT
RUN groupadd --gid 1000 kibana &&     useradd --uid 1000 --gid 1000 -G 0       --home-dir /usr/share/kibana --no-create-home       kibana # buildkit
# Tue, 11 Nov 2025 18:16:51 GMT
LABEL org.label-schema.build-date=2025-11-06T12:31:22.639Z org.label-schema.license=Elastic License org.label-schema.name=Kibana org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/kibana org.label-schema.usage=https://www.elastic.co/guide/en/kibana/reference/index.html org.label-schema.vcs-ref=2b1aec68b05596d5cbe93d7444cd128f814ef600 org.label-schema.vcs-url=https://github.com/elastic/kibana org.label-schema.vendor=Elastic org.label-schema.version=9.2.1 org.opencontainers.image.created=2025-11-06T12:31:22.639Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/kibana/reference/index.html org.opencontainers.image.licenses=Elastic License org.opencontainers.image.revision=2b1aec68b05596d5cbe93d7444cd128f814ef600 org.opencontainers.image.source=https://github.com/elastic/kibana org.opencontainers.image.title=Kibana org.opencontainers.image.url=https://www.elastic.co/products/kibana org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=9.2.1
# Tue, 11 Nov 2025 18:16:51 GMT
LABEL name=Kibana maintainer=infra@elastic.co vendor=Elastic version=9.2.1 release=1 summary=Kibana description=Your window into the Elastic Stack.
# Tue, 11 Nov 2025 18:16:51 GMT
RUN mkdir /licenses && ln LICENSE.txt /licenses/LICENSE # buildkit
# Tue, 11 Nov 2025 18:16:51 GMT
ENTRYPOINT ["/bin/tini" "--"]
# Tue, 11 Nov 2025 18:16:51 GMT
CMD ["/usr/local/bin/kibana-docker"]
# Tue, 11 Nov 2025 18:16:51 GMT
USER 1000
```

-	Layers:
	-	`sha256:2920d84eafa0cf94806ab58f0a2124f7b2d35bcbb06fc89a9106dcc28efe397a`  
		Last Modified: Wed, 15 Oct 2025 09:03:15 GMT  
		Size: 39.7 MB (39653524 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c040abcd4b9710bb9da1f0d9254f941ac42529b5e2eeda5f44d9d470cfa1db73`  
		Last Modified: Tue, 11 Nov 2025 18:18:12 GMT  
		Size: 23.8 MB (23841540 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:597b3b90f6e8554a6bafd970e3a0df2bc3525ed8a52932d3e10b19bcfba5cdf9`  
		Last Modified: Tue, 11 Nov 2025 21:18:15 GMT  
		Size: 360.2 MB (360196843 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:234c34dc42f051a8214a2c3d5718a86adabe50eb6bc702ec4e572da438e0923e`  
		Last Modified: Tue, 11 Nov 2025 18:18:07 GMT  
		Size: 9.5 KB (9533 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49adad52b4436dbdb5ab119577a2e1679313b64f7d95131ab267355059585798`  
		Last Modified: Tue, 11 Nov 2025 18:18:10 GMT  
		Size: 16.5 MB (16460490 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc142c68654b8fdf7b0def88c2e49eeb1e0b9dcdfe9ba184f115dec9f7d016b4`  
		Last Modified: Tue, 11 Nov 2025 18:18:07 GMT  
		Size: 5.2 KB (5223 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:154f4909d0edfc59b3495901166905861d8ecbc2b36629b4035264b0f612d607`  
		Last Modified: Tue, 11 Nov 2025 18:18:07 GMT  
		Size: 132.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62cdde379b66d8740e148c674c4e359f5c1985bb7867c33030224d4f49177def`  
		Last Modified: Tue, 11 Nov 2025 18:18:07 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f63dd805b105a62dd893b944b11ed0d63e2b5cda3323e572dbfaa5e295e9a3e`  
		Last Modified: Tue, 11 Nov 2025 18:18:07 GMT  
		Size: 4.9 KB (4897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae977e8c2cf1f0593ceaa4153c0a5c09eb26f553041f7c2bef2e7d9cb1ba4bd4`  
		Last Modified: Tue, 11 Nov 2025 18:18:07 GMT  
		Size: 399.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a0eeeacea9dffabbb22d4906d726e5e651ea89b4a2bca01307d9aa6ff718dbb`  
		Last Modified: Tue, 11 Nov 2025 18:18:08 GMT  
		Size: 74.5 KB (74541 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc7f3e62b3449a6c1cb0b109546e64f78214001b410070b7b08cabb9f8aa2e94`  
		Last Modified: Tue, 11 Nov 2025 18:18:07 GMT  
		Size: 1.1 KB (1050 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8423f241576c87e50074a0b52ee8329d2ffc8f185e40232672b8fda53604633`  
		Last Modified: Tue, 11 Nov 2025 18:18:09 GMT  
		Size: 1.7 KB (1708 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kibana:9.2.1` - unknown; unknown

```console
$ docker pull kibana@sha256:b77da95aa77e0a283a06c5ad99bd03aee1462a3f09ea0244ff0f45bdcb6df40a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5755916 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf9a67b90817979d1b7b1d4b2b8e4942c9a25a8927c13fdb32631c7f149aef26`

```dockerfile
```

-	Layers:
	-	`sha256:beff2e15f04ec2e2594b0660c8d9142f73432de757ee0a614da83c0f04944f99`  
		Last Modified: Tue, 11 Nov 2025 21:11:43 GMT  
		Size: 5.7 MB (5712690 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:18aa25cc57f9d64aec1098798d4242983f4d6fb7aba63e40a5f15d84626a504e`  
		Last Modified: Tue, 11 Nov 2025 21:11:44 GMT  
		Size: 43.2 KB (43226 bytes)  
		MIME: application/vnd.in-toto+json

### `kibana:9.2.1` - linux; arm64 variant v8

```console
$ docker pull kibana@sha256:23830edcfde77d806a55c7488b2970c693600fff9c82fd67d699708c6ffc1eec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **451.2 MB (451237317 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d81b573605ddb84921594c43dbed37726233798ba3e1a454e0bf919d488bcca`
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
# Tue, 11 Nov 2025 18:08:29 GMT
EXPOSE map[5601/tcp:{}]
# Tue, 11 Nov 2025 18:08:29 GMT
RUN microdnf install --setopt=tsflags=nodocs -y       fontconfig liberation-fonts-common freetype shadow-utils nss findutils &&       microdnf clean all # buildkit
# Tue, 11 Nov 2025 18:15:50 GMT
COPY --chown=1000:0 /usr/share/kibana /usr/share/kibana # buildkit
# Tue, 11 Nov 2025 18:15:51 GMT
COPY --chown=0:0 /bin/tini /bin/tini # buildkit
# Tue, 11 Nov 2025 18:15:51 GMT
COPY --chown=0:0 /usr/share/fonts/local/NotoSansCJK-Regular.ttc /usr/share/fonts/local/NotoSansCJK-Regular.ttc # buildkit
# Tue, 11 Nov 2025 18:15:51 GMT
RUN fc-cache -v # buildkit
# Tue, 11 Nov 2025 18:15:51 GMT
WORKDIR /usr/share/kibana
# Tue, 11 Nov 2025 18:15:51 GMT
RUN ln -s /usr/share/kibana /opt/kibana # buildkit
# Tue, 11 Nov 2025 18:15:51 GMT
ENV ELASTIC_CONTAINER=true
# Tue, 11 Nov 2025 18:15:51 GMT
ENV PATH=/usr/share/kibana/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 11 Nov 2025 18:15:51 GMT
COPY --chown=1000:0 config/kibana.yml /usr/share/kibana/config/kibana.yml # buildkit
# Tue, 11 Nov 2025 18:15:51 GMT
COPY bin/kibana-docker /usr/local/bin/ # buildkit
# Tue, 11 Nov 2025 18:15:52 GMT
RUN chmod g+ws /usr/share/kibana &&     find /usr/share/kibana -gid 0 -and -not -perm /g+w -exec chmod g+w {} \; # buildkit
# Tue, 11 Nov 2025 18:15:53 GMT
RUN find / -xdev -perm -4000 -exec chmod u-s {} + # buildkit
# Tue, 11 Nov 2025 18:15:53 GMT
RUN groupadd --gid 1000 kibana &&     useradd --uid 1000 --gid 1000 -G 0       --home-dir /usr/share/kibana --no-create-home       kibana # buildkit
# Tue, 11 Nov 2025 18:15:53 GMT
LABEL org.label-schema.build-date=2025-11-06T12:31:22.639Z org.label-schema.license=Elastic License org.label-schema.name=Kibana org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/kibana org.label-schema.usage=https://www.elastic.co/guide/en/kibana/reference/index.html org.label-schema.vcs-ref=2b1aec68b05596d5cbe93d7444cd128f814ef600 org.label-schema.vcs-url=https://github.com/elastic/kibana org.label-schema.vendor=Elastic org.label-schema.version=9.2.1 org.opencontainers.image.created=2025-11-06T12:31:22.639Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/kibana/reference/index.html org.opencontainers.image.licenses=Elastic License org.opencontainers.image.revision=2b1aec68b05596d5cbe93d7444cd128f814ef600 org.opencontainers.image.source=https://github.com/elastic/kibana org.opencontainers.image.title=Kibana org.opencontainers.image.url=https://www.elastic.co/products/kibana org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=9.2.1
# Tue, 11 Nov 2025 18:15:53 GMT
LABEL name=Kibana maintainer=infra@elastic.co vendor=Elastic version=9.2.1 release=1 summary=Kibana description=Your window into the Elastic Stack.
# Tue, 11 Nov 2025 18:15:53 GMT
RUN mkdir /licenses && ln LICENSE.txt /licenses/LICENSE # buildkit
# Tue, 11 Nov 2025 18:15:53 GMT
ENTRYPOINT ["/bin/tini" "--"]
# Tue, 11 Nov 2025 18:15:53 GMT
CMD ["/usr/local/bin/kibana-docker"]
# Tue, 11 Nov 2025 18:15:53 GMT
USER 1000
```

-	Layers:
	-	`sha256:2602e1c5e8830fe80a6207359ce01e6c9b7d6848be663c4df1e03c724149b8a6`  
		Last Modified: Wed, 15 Oct 2025 09:30:32 GMT  
		Size: 37.9 MB (37896281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9a6a4c03f2d5e06c41bb63f8d75ae1d956ed9c7f983dda8d4a90c382ccd4329`  
		Last Modified: Tue, 11 Nov 2025 18:17:16 GMT  
		Size: 23.6 MB (23554353 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e970b29f1352881e52f0845011bc2085efa447fdb28025c3366c9a7e617896c`  
		Last Modified: Tue, 11 Nov 2025 21:17:56 GMT  
		Size: 373.2 MB (373229803 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d9dac920fe9d43c58e98a83bda93a2670f361555729e83f93e3e12b47da7557`  
		Last Modified: Tue, 11 Nov 2025 18:17:13 GMT  
		Size: 9.1 KB (9103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cad143593a2be36126637dd6e731f1115fca7847ddf3fe8e0f4a8c59650824ef`  
		Last Modified: Tue, 11 Nov 2025 18:17:17 GMT  
		Size: 16.5 MB (16460490 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0db6bf070e2704ac7eae6a8d527b5df3ba78eecfab4bfb4b2ea75036b2e04fa`  
		Last Modified: Tue, 11 Nov 2025 18:17:13 GMT  
		Size: 5.2 KB (5226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fef228419bce775dd3bee2509673c82350613d507634bc4f646f7d4da095825`  
		Last Modified: Tue, 11 Nov 2025 18:17:13 GMT  
		Size: 131.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f42d9e255382b58b2efece97bf613c31609c5041c46605edc1e00c33a1af1dd9`  
		Last Modified: Tue, 11 Nov 2025 18:17:13 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:044251c2f2f1b830a12112578ea32aa3d9921760c1d0ce7187b375591e430721`  
		Last Modified: Tue, 11 Nov 2025 18:17:13 GMT  
		Size: 4.9 KB (4899 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf5b2f522ce321a0beeccc4e3660e868bac396ba975d4154284090916bc2b9c2`  
		Last Modified: Tue, 11 Nov 2025 18:17:13 GMT  
		Size: 401.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fd1b86889ccc88d6336f65bc5d8a3f7974a495e9770b15366c8209a34892542`  
		Last Modified: Tue, 11 Nov 2025 18:17:13 GMT  
		Size: 73.4 KB (73449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61711d4c7f2744b07c2295239cbb07484b17fce0ae1859ee279e80d998f0e9f5`  
		Last Modified: Tue, 11 Nov 2025 18:17:13 GMT  
		Size: 1.0 KB (1046 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2dd40b263f9f321aa3d932bea48cd0cc89fa211ded30d7dd42b7a34ac41ca85`  
		Last Modified: Tue, 11 Nov 2025 18:17:14 GMT  
		Size: 1.7 KB (1705 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kibana:9.2.1` - unknown; unknown

```console
$ docker pull kibana@sha256:e633a3a430aa9842e6ac1296084832d7a395bb8af333e8bb407ee082578cdcab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5754850 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:37f0e8589737b5c328d38eb58f54097fee67fd1d69100c4003809e41fae0878e`

```dockerfile
```

-	Layers:
	-	`sha256:880797144a4f2f8ff15f91d2b158a54dbe704f698dd498719e6771905300bfda`  
		Last Modified: Tue, 11 Nov 2025 21:11:50 GMT  
		Size: 5.7 MB (5711368 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:71cd3822f9fba7d85ccf1c47dc227dcb6858fa553b8cd0fdcc35add24f771b6b`  
		Last Modified: Tue, 11 Nov 2025 21:11:50 GMT  
		Size: 43.5 KB (43482 bytes)  
		MIME: application/vnd.in-toto+json
