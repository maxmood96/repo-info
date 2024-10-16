<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `kibana`

-	[`kibana:7.17.24`](#kibana71724)
-	[`kibana:8.15.2`](#kibana8152)

## `kibana:7.17.24`

```console
$ docker pull kibana@sha256:103dcbd974025506358259d580a521af1e793b765857d72097b984f526dd477f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `kibana:7.17.24` - linux; amd64

```console
$ docker pull kibana@sha256:6e7b40c4fbe7ed88676c842734d0d51fd3008469948b843a06b0bf8d59f7ecef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **349.0 MB (349025782 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:50c5ac2046778c891a56110d4880cd1fcf5b53acb1aac135a5da654bc6f5cf2c`
-	Entrypoint: `["\/bin\/tini","--"]`
-	Default Command: `["\/usr\/local\/bin\/kibana-docker"]`

```dockerfile
# Tue, 10 Sep 2024 08:21:14 GMT
ARG RELEASE
# Tue, 10 Sep 2024 08:21:14 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 10 Sep 2024 08:21:14 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 10 Sep 2024 08:21:14 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 10 Sep 2024 08:21:14 GMT
ADD file:6a209aa51ba684c0a39769619c42058ca99311b87563c7b079319a8bb91bec1f in / 
# Tue, 10 Sep 2024 08:21:14 GMT
CMD ["/bin/bash"]
# Tue, 10 Sep 2024 08:21:14 GMT
EXPOSE map[5601/tcp:{}]
# Tue, 10 Sep 2024 08:21:14 GMT
RUN for iter in {1..10}; do       export DEBIAN_FRONTEND=noninteractive &&       apt-get update  &&       apt-get upgrade -y  &&       apt-get install -y --no-install-recommends        fontconfig fonts-liberation libnss3 libfontconfig1 ca-certificates curl &&       apt-get clean &&       rm -rf /var/lib/apt/lists/* && exit_code=0 && break || exit_code=$? && echo "apt-get error: retry $iter in 10s" &&       sleep 10;     done;     (exit $exit_code) # buildkit
# Tue, 10 Sep 2024 08:21:14 GMT
RUN set -e ;     TINI_BIN="" ;     case "$(arch)" in         aarch64)             TINI_BIN='tini-arm64' ;             ;;         x86_64)             TINI_BIN='tini-amd64' ;             ;;         *) echo >&2 "Unsupported architecture $(arch)" ; exit 1 ;;     esac ;   TINI_VERSION='v0.19.0' ;   curl --retry 8 -S -L -O "https://github.com/krallin/tini/releases/download/${TINI_VERSION}/${TINI_BIN}" ;   curl --retry 8 -S -L -O "https://github.com/krallin/tini/releases/download/${TINI_VERSION}/${TINI_BIN}.sha256sum" ;   sha256sum -c "${TINI_BIN}.sha256sum" ;   rm "${TINI_BIN}.sha256sum" ;   mv "${TINI_BIN}" /bin/tini ;   chmod +x /bin/tini # buildkit
# Tue, 10 Sep 2024 08:21:14 GMT
RUN mkdir /usr/share/fonts/local # buildkit
# Tue, 10 Sep 2024 08:21:14 GMT
RUN curl --retry 8 -S -L -o /usr/share/fonts/local/NotoSansCJK-Regular.ttc https://github.com/googlefonts/noto-cjk/raw/NotoSansV2.001/NotoSansCJK-Regular.ttc # buildkit
# Tue, 10 Sep 2024 08:21:14 GMT
RUN echo "5dcd1c336cc9344cb77c03a0cd8982ca8a7dc97d620fd6c9c434e02dcb1ceeb3  /usr/share/fonts/local/NotoSansCJK-Regular.ttc" | sha256sum -c - # buildkit
# Tue, 10 Sep 2024 08:21:14 GMT
RUN fc-cache -v # buildkit
# Tue, 10 Sep 2024 08:21:14 GMT
COPY --chown=1000:0 /usr/share/kibana /usr/share/kibana # buildkit
# Tue, 10 Sep 2024 08:21:14 GMT
WORKDIR /usr/share/kibana
# Tue, 10 Sep 2024 08:21:14 GMT
RUN ln -s /usr/share/kibana /opt/kibana # buildkit
# Tue, 10 Sep 2024 08:21:14 GMT
ENV ELASTIC_CONTAINER=true
# Tue, 10 Sep 2024 08:21:14 GMT
ENV PATH=/usr/share/kibana/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 10 Sep 2024 08:21:14 GMT
COPY --chown=1000:0 config/kibana.yml /usr/share/kibana/config/kibana.yml # buildkit
# Tue, 10 Sep 2024 08:21:14 GMT
COPY bin/kibana-docker /usr/local/bin/ # buildkit
# Tue, 10 Sep 2024 08:21:14 GMT
RUN chmod g+ws /usr/share/kibana &&     find /usr/share/kibana -gid 0 -and -not -perm /g+w -exec chmod g+w {} \; # buildkit
# Tue, 10 Sep 2024 08:21:14 GMT
RUN find / -xdev -perm -4000 -exec chmod u-s {} + # buildkit
# Tue, 10 Sep 2024 08:21:14 GMT
RUN groupadd --gid 1000 kibana &&     useradd --uid 1000 --gid 1000 -G 0       --home-dir /usr/share/kibana --no-create-home       kibana # buildkit
# Tue, 10 Sep 2024 08:21:14 GMT
LABEL org.label-schema.build-date=2024-09-04T11:10:43.736Z org.label-schema.license=Elastic License org.label-schema.name=Kibana org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/kibana org.label-schema.usage=https://www.elastic.co/guide/en/kibana/reference/index.html org.label-schema.vcs-ref=4fb3ec3c959e4c569aca4674243a2ecba9d973a7 org.label-schema.vcs-url=https://github.com/elastic/kibana org.label-schema.vendor=Elastic org.label-schema.version=7.17.24 org.opencontainers.image.created=2024-09-04T11:10:43.736Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/kibana/reference/index.html org.opencontainers.image.licenses=Elastic License org.opencontainers.image.revision=4fb3ec3c959e4c569aca4674243a2ecba9d973a7 org.opencontainers.image.source=https://github.com/elastic/kibana org.opencontainers.image.title=Kibana org.opencontainers.image.url=https://www.elastic.co/products/kibana org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=7.17.24
# Tue, 10 Sep 2024 08:21:14 GMT
ENTRYPOINT ["/bin/tini" "--"]
# Tue, 10 Sep 2024 08:21:14 GMT
CMD ["/usr/local/bin/kibana-docker"]
# Tue, 10 Sep 2024 08:21:14 GMT
USER kibana
```

-	Layers:
	-	`sha256:3823320faa42774534fd7eee0bd245af8cec6a720ad722144d40efa229291d8f`  
		Last Modified: Wed, 18 Sep 2024 05:32:37 GMT  
		Size: 27.5 MB (27511052 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5af65279dcf6de07e05d644ce3a5b3a15dc803910e5d33a99e3c5537b448d947`  
		Last Modified: Wed, 02 Oct 2024 02:00:00 GMT  
		Size: 10.7 MB (10723703 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6813b1a5ecdd45dcb6f3476b2a5694dfbc47e3ba9260b19675a2f151a96e479f`  
		Last Modified: Wed, 02 Oct 2024 02:00:00 GMT  
		Size: 9.5 KB (9526 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d525d085e02ce3edb1f0c28b694f1bb6ce15dbbc7d88e98104d78d7e128ad0a`  
		Last Modified: Wed, 02 Oct 2024 02:00:00 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52228a836be6cc3193cffdb1d86dff90e69f8759512b654c5cec08a7a228485c`  
		Last Modified: Wed, 02 Oct 2024 02:00:00 GMT  
		Size: 16.5 MB (16460483 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:068c37089041e33778f8d7726a93e67931fa82f2fc6de700c5f84de3d1649962`  
		Last Modified: Wed, 02 Oct 2024 02:00:01 GMT  
		Size: 5.3 KB (5291 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bb4507c55841cc8b7a90fcdc4a63f8f4b186033640962344a65cfaf439c0ff8`  
		Last Modified: Wed, 02 Oct 2024 02:00:06 GMT  
		Size: 294.1 MB (294118846 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50cf6b4332e18d8c01947e08ae4adcdc549d7105506d7d543fb9aca01ec7fa6e`  
		Last Modified: Wed, 02 Oct 2024 02:00:01 GMT  
		Size: 130.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ace8b7cda83d330c91194493bd8ab4ffbc1faccdfa95064d1a0221c398e9569`  
		Last Modified: Wed, 02 Oct 2024 02:00:01 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34432edde43ec9b2bf91f504449b68fe2471644649a27a5e6fdf938921de776f`  
		Last Modified: Wed, 02 Oct 2024 02:00:02 GMT  
		Size: 4.5 KB (4506 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d61632968f56f5f1c2019a99c9e8e50e0dc3837d35d1a7192812e63cd92799d`  
		Last Modified: Wed, 02 Oct 2024 02:00:02 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84c8be5c1e1a9d32971706e0b4e49391ead47ce6842acb8f45295323e3851301`  
		Last Modified: Wed, 02 Oct 2024 02:00:02 GMT  
		Size: 189.4 KB (189432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02a482b1629c365eb41aebaf19fa9eccbb66f74bba20b3539a6c2f0521a81c47`  
		Last Modified: Wed, 02 Oct 2024 02:00:02 GMT  
		Size: 1.8 KB (1797 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kibana:7.17.24` - unknown; unknown

```console
$ docker pull kibana@sha256:cd1f6a860efa3045f9714a5117c9c70bbe2d4d1e4c0c23ad9d79c6bc6c866c81
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.4 MB (3425628 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d989e872299ab0e62457d8ec31d345a190608cc2af2c424383020e14381bcc1`

```dockerfile
```

-	Layers:
	-	`sha256:2dc03a303cf0f820bb8754c62147c0c5e12e593373a93f046bcc3242e5b6f8e3`  
		Last Modified: Wed, 02 Oct 2024 02:00:00 GMT  
		Size: 3.4 MB (3381368 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d12bb79e95c88e7d568fdafd79f178568097936a41c113537c2b117b7dc03d60`  
		Last Modified: Wed, 02 Oct 2024 02:00:00 GMT  
		Size: 44.3 KB (44260 bytes)  
		MIME: application/vnd.in-toto+json

### `kibana:7.17.24` - linux; arm64 variant v8

```console
$ docker pull kibana@sha256:da9348bc579afd91261ed7b852b27747e380fe08acd7682edee7c1e9fb0a751e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **359.9 MB (359915384 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:845a1ea9f655d1584165c085e52fe60d77bff80f5511bf00441635040ccc375b`
-	Entrypoint: `["\/bin\/tini","--"]`
-	Default Command: `["\/usr\/local\/bin\/kibana-docker"]`

```dockerfile
# Tue, 10 Sep 2024 08:21:14 GMT
ARG RELEASE
# Tue, 10 Sep 2024 08:21:14 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 10 Sep 2024 08:21:14 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 10 Sep 2024 08:21:14 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 10 Sep 2024 08:21:14 GMT
ADD file:8537b4db344382b39d669af27cd94ec0f870ceafe58c67ee54e3f9b38fb8d671 in / 
# Tue, 10 Sep 2024 08:21:14 GMT
CMD ["/bin/bash"]
# Tue, 10 Sep 2024 08:21:14 GMT
EXPOSE map[5601/tcp:{}]
# Tue, 10 Sep 2024 08:21:14 GMT
RUN for iter in {1..10}; do       export DEBIAN_FRONTEND=noninteractive &&       apt-get update  &&       apt-get upgrade -y  &&       apt-get install -y --no-install-recommends        fontconfig fonts-liberation libnss3 libfontconfig1 ca-certificates curl &&       apt-get clean &&       rm -rf /var/lib/apt/lists/* && exit_code=0 && break || exit_code=$? && echo "apt-get error: retry $iter in 10s" &&       sleep 10;     done;     (exit $exit_code) # buildkit
# Tue, 10 Sep 2024 08:21:14 GMT
RUN set -e ;     TINI_BIN="" ;     case "$(arch)" in         aarch64)             TINI_BIN='tini-arm64' ;             ;;         x86_64)             TINI_BIN='tini-amd64' ;             ;;         *) echo >&2 "Unsupported architecture $(arch)" ; exit 1 ;;     esac ;   TINI_VERSION='v0.19.0' ;   curl --retry 8 -S -L -O "https://github.com/krallin/tini/releases/download/${TINI_VERSION}/${TINI_BIN}" ;   curl --retry 8 -S -L -O "https://github.com/krallin/tini/releases/download/${TINI_VERSION}/${TINI_BIN}.sha256sum" ;   sha256sum -c "${TINI_BIN}.sha256sum" ;   rm "${TINI_BIN}.sha256sum" ;   mv "${TINI_BIN}" /bin/tini ;   chmod +x /bin/tini # buildkit
# Tue, 10 Sep 2024 08:21:14 GMT
RUN mkdir /usr/share/fonts/local # buildkit
# Tue, 10 Sep 2024 08:21:14 GMT
RUN curl --retry 8 -S -L -o /usr/share/fonts/local/NotoSansCJK-Regular.ttc https://github.com/googlefonts/noto-cjk/raw/NotoSansV2.001/NotoSansCJK-Regular.ttc # buildkit
# Tue, 10 Sep 2024 08:21:14 GMT
RUN echo "5dcd1c336cc9344cb77c03a0cd8982ca8a7dc97d620fd6c9c434e02dcb1ceeb3  /usr/share/fonts/local/NotoSansCJK-Regular.ttc" | sha256sum -c - # buildkit
# Tue, 10 Sep 2024 08:21:14 GMT
RUN fc-cache -v # buildkit
# Tue, 10 Sep 2024 08:21:14 GMT
COPY --chown=1000:0 /usr/share/kibana /usr/share/kibana # buildkit
# Tue, 10 Sep 2024 08:21:14 GMT
WORKDIR /usr/share/kibana
# Tue, 10 Sep 2024 08:21:14 GMT
RUN ln -s /usr/share/kibana /opt/kibana # buildkit
# Tue, 10 Sep 2024 08:21:14 GMT
ENV ELASTIC_CONTAINER=true
# Tue, 10 Sep 2024 08:21:14 GMT
ENV PATH=/usr/share/kibana/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 10 Sep 2024 08:21:14 GMT
COPY --chown=1000:0 config/kibana.yml /usr/share/kibana/config/kibana.yml # buildkit
# Tue, 10 Sep 2024 08:21:14 GMT
COPY bin/kibana-docker /usr/local/bin/ # buildkit
# Tue, 10 Sep 2024 08:21:14 GMT
RUN chmod g+ws /usr/share/kibana &&     find /usr/share/kibana -gid 0 -and -not -perm /g+w -exec chmod g+w {} \; # buildkit
# Tue, 10 Sep 2024 08:21:14 GMT
RUN find / -xdev -perm -4000 -exec chmod u-s {} + # buildkit
# Tue, 10 Sep 2024 08:21:14 GMT
RUN groupadd --gid 1000 kibana &&     useradd --uid 1000 --gid 1000 -G 0       --home-dir /usr/share/kibana --no-create-home       kibana # buildkit
# Tue, 10 Sep 2024 08:21:14 GMT
LABEL org.label-schema.build-date=2024-09-04T11:10:43.736Z org.label-schema.license=Elastic License org.label-schema.name=Kibana org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/kibana org.label-schema.usage=https://www.elastic.co/guide/en/kibana/reference/index.html org.label-schema.vcs-ref=4fb3ec3c959e4c569aca4674243a2ecba9d973a7 org.label-schema.vcs-url=https://github.com/elastic/kibana org.label-schema.vendor=Elastic org.label-schema.version=7.17.24 org.opencontainers.image.created=2024-09-04T11:10:43.736Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/kibana/reference/index.html org.opencontainers.image.licenses=Elastic License org.opencontainers.image.revision=4fb3ec3c959e4c569aca4674243a2ecba9d973a7 org.opencontainers.image.source=https://github.com/elastic/kibana org.opencontainers.image.title=Kibana org.opencontainers.image.url=https://www.elastic.co/products/kibana org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=7.17.24
# Tue, 10 Sep 2024 08:21:14 GMT
ENTRYPOINT ["/bin/tini" "--"]
# Tue, 10 Sep 2024 08:21:14 GMT
CMD ["/usr/local/bin/kibana-docker"]
# Tue, 10 Sep 2024 08:21:14 GMT
USER kibana
```

-	Layers:
	-	`sha256:1b9f3c55f9d4aa5c52eb67a4cb7d0f4726ab85a413b50e3e3fe788befce3d297`  
		Last Modified: Fri, 11 Oct 2024 04:41:30 GMT  
		Size: 26.0 MB (25973828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9292fd052a4e5afdfe32d05bbde9aa9737b03f4f092222375f58aa893250f48`  
		Last Modified: Wed, 16 Oct 2024 03:24:59 GMT  
		Size: 10.6 MB (10575032 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aafe65c4e7d35e036f20c05c604524a12b7c180dcf8354448b764990a740a798`  
		Last Modified: Wed, 16 Oct 2024 03:24:58 GMT  
		Size: 9.1 KB (9095 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed698c438cb75e359246a05f0a09d8ab3744169938947a81eab7ff9c35ad192c`  
		Last Modified: Wed, 16 Oct 2024 03:24:58 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53bf4c1f716146058b2b87961c282bbca1bc4015028244ed2a66f638d20b70c6`  
		Last Modified: Wed, 16 Oct 2024 03:24:59 GMT  
		Size: 16.5 MB (16460483 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b1172c9a679de7f18a23a7d365c9a4ba12121e229f42af8fce85cd18a15227b`  
		Last Modified: Wed, 16 Oct 2024 03:24:59 GMT  
		Size: 5.3 KB (5291 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1acdea2f83a2972088d1c9554f767ba67c1b69cf8bc24dae3cbd0d906b70e6a6`  
		Last Modified: Wed, 16 Oct 2024 03:25:08 GMT  
		Size: 306.7 MB (306700783 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7d12cc5179408e41dcd2475ba2c45d370f03aa50de457e60ec73b2043d1a959`  
		Last Modified: Wed, 16 Oct 2024 03:25:00 GMT  
		Size: 132.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f278d701ed69f6232b5f2a8e83298f473e01f2ad738cd69bdeeac43d3ca99c80`  
		Last Modified: Wed, 16 Oct 2024 03:25:00 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd1469224f7966b05b1113893821317437725aae69fbe7a75e756a674fded488`  
		Last Modified: Wed, 16 Oct 2024 03:25:00 GMT  
		Size: 4.5 KB (4500 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9dabcd47631d11c54c0e40718d2d1abac26b328a9b63bb31992296782dd5b667`  
		Last Modified: Wed, 16 Oct 2024 03:25:01 GMT  
		Size: 400.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9065d414e85b530c093e7b87fd94b7d633affef7f2b3684d624a0befa1a3ae35`  
		Last Modified: Wed, 16 Oct 2024 03:25:01 GMT  
		Size: 183.4 KB (183416 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:516173a9a4882201a18b02234febd8ed3723dfacd411a46cf97c6e8a914ded9b`  
		Last Modified: Wed, 16 Oct 2024 03:25:01 GMT  
		Size: 1.8 KB (1804 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kibana:7.17.24` - unknown; unknown

```console
$ docker pull kibana@sha256:7b93ffc8322f37dec398d052cfbf7931e27849be83de3f43e348b98606885832
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.4 MB (3426183 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aee799f1951a1f11f9906ddd5c457f7338542dcd7176e0e4c865037bc4bf4929`

```dockerfile
```

-	Layers:
	-	`sha256:c0f62c8d91612386688f454684100a2ed191ae11e9f244ee6c8bf5a5a556d3b4`  
		Last Modified: Wed, 16 Oct 2024 03:24:59 GMT  
		Size: 3.4 MB (3381618 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0171979d3ed19b29daadd787f8d04585c0c497f47f7d4e64ad79d631a60dd807`  
		Last Modified: Wed, 16 Oct 2024 03:24:58 GMT  
		Size: 44.6 KB (44565 bytes)  
		MIME: application/vnd.in-toto+json

## `kibana:8.15.2`

```console
$ docker pull kibana@sha256:b54aedd5a4852fdd5f2cfcb2902e0940bdd143546d836dd1ff96280e23b59dd5
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `kibana:8.15.2` - linux; amd64

```console
$ docker pull kibana@sha256:b66e22261eb4ec2a40c9c0debd67feb8584479a874f0f3358558455b3d7ebed1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **393.7 MB (393746012 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4288c14dea65766ae412687628f8e7d0957f7598feff94b05791c7a94078ab7d`
-	Entrypoint: `["\/bin\/tini","--"]`
-	Default Command: `["\/usr\/local\/bin\/kibana-docker"]`

```dockerfile
# Wed, 18 Sep 2024 04:18:32 GMT
ARG RELEASE
# Wed, 18 Sep 2024 04:18:32 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 18 Sep 2024 04:18:32 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 18 Sep 2024 04:18:32 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 18 Sep 2024 04:18:34 GMT
ADD file:6a209aa51ba684c0a39769619c42058ca99311b87563c7b079319a8bb91bec1f in / 
# Wed, 18 Sep 2024 04:18:34 GMT
CMD ["/bin/bash"]
# Thu, 26 Sep 2024 08:08:51 GMT
EXPOSE map[5601/tcp:{}]
# Thu, 26 Sep 2024 08:08:51 GMT
RUN for iter in {1..10}; do       export DEBIAN_FRONTEND=noninteractive &&       apt-get update  &&       apt-get upgrade -y  &&       apt-get install -y --no-install-recommends        fontconfig libnss3 curl ca-certificates &&       apt-get clean &&       rm -rf /var/lib/apt/lists/* && exit_code=0 && break || exit_code=$? && echo "apt-get error: retry $iter in 10s" &&       sleep 10;     done;     (exit $exit_code) # buildkit
# Thu, 26 Sep 2024 08:08:51 GMT
COPY --chown=1000:0 /usr/share/kibana /usr/share/kibana # buildkit
# Thu, 26 Sep 2024 08:08:51 GMT
COPY --chown=0:0 /bin/tini /bin/tini # buildkit
# Thu, 26 Sep 2024 08:08:51 GMT
COPY --chown=0:0 /usr/share/fonts/local/NotoSansCJK-Regular.ttc /usr/share/fonts/local/NotoSansCJK-Regular.ttc # buildkit
# Thu, 26 Sep 2024 08:08:51 GMT
RUN fc-cache -v # buildkit
# Thu, 26 Sep 2024 08:08:51 GMT
WORKDIR /usr/share/kibana
# Thu, 26 Sep 2024 08:08:51 GMT
RUN ln -s /usr/share/kibana /opt/kibana # buildkit
# Thu, 26 Sep 2024 08:08:51 GMT
ENV ELASTIC_CONTAINER=true
# Thu, 26 Sep 2024 08:08:51 GMT
ENV PATH=/usr/share/kibana/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 26 Sep 2024 08:08:51 GMT
COPY --chown=1000:0 config/kibana.yml /usr/share/kibana/config/kibana.yml # buildkit
# Thu, 26 Sep 2024 08:08:51 GMT
COPY bin/kibana-docker /usr/local/bin/ # buildkit
# Thu, 26 Sep 2024 08:08:51 GMT
RUN chmod g+ws /usr/share/kibana &&     find /usr/share/kibana -gid 0 -and -not -perm /g+w -exec chmod g+w {} \; # buildkit
# Thu, 26 Sep 2024 08:08:51 GMT
RUN find / -xdev -perm -4000 -exec chmod u-s {} + # buildkit
# Thu, 26 Sep 2024 08:08:51 GMT
RUN groupadd --gid 1000 kibana &&     useradd --uid 1000 --gid 1000 -G 0       --home-dir /usr/share/kibana --no-create-home       kibana # buildkit
# Thu, 26 Sep 2024 08:08:51 GMT
LABEL org.label-schema.build-date=2024-09-19T11:10:25.889Z org.label-schema.license=Elastic License org.label-schema.name=Kibana org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/kibana org.label-schema.usage=https://www.elastic.co/guide/en/kibana/reference/index.html org.label-schema.vcs-ref=5a522bfe14bc6d06c20bc337477fd53f7c538973 org.label-schema.vcs-url=https://github.com/elastic/kibana org.label-schema.vendor=Elastic org.label-schema.version=8.15.2 org.opencontainers.image.created=2024-09-19T11:10:25.889Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/kibana/reference/index.html org.opencontainers.image.licenses=Elastic License org.opencontainers.image.revision=5a522bfe14bc6d06c20bc337477fd53f7c538973 org.opencontainers.image.source=https://github.com/elastic/kibana org.opencontainers.image.title=Kibana org.opencontainers.image.url=https://www.elastic.co/products/kibana org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=8.15.2
# Thu, 26 Sep 2024 08:08:51 GMT
ENTRYPOINT ["/bin/tini" "--"]
# Thu, 26 Sep 2024 08:08:51 GMT
CMD ["/usr/local/bin/kibana-docker"]
# Thu, 26 Sep 2024 08:08:51 GMT
USER 1000
```

-	Layers:
	-	`sha256:3823320faa42774534fd7eee0bd245af8cec6a720ad722144d40efa229291d8f`  
		Last Modified: Wed, 18 Sep 2024 05:32:37 GMT  
		Size: 27.5 MB (27511052 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ba0f3fdb6147be8ff55d116000d0223b3b085eb7ac134163749a1b4e200152d`  
		Last Modified: Wed, 02 Oct 2024 02:00:32 GMT  
		Size: 11.0 MB (10966499 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c81563f96d933b3824223fbe9e70dad7ea3df04a8f5759a26d0c5037ab70e60`  
		Last Modified: Wed, 02 Oct 2024 02:00:39 GMT  
		Size: 338.6 MB (338596341 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:188687a606a01b64bf02810778d9545313f5fce9b7087328b08f6dfd19a3f7ca`  
		Last Modified: Wed, 02 Oct 2024 02:00:31 GMT  
		Size: 9.5 KB (9529 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d6e0e13b2e1941867b01739cc04c64953aa47ff045bbacc3ee821940546e1c8`  
		Last Modified: Wed, 02 Oct 2024 02:00:32 GMT  
		Size: 16.5 MB (16460495 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:780e0b042829e3e7c8ced6d46ba5d1393a6c261f2c17a9a7b6b58c0cdfdf4888`  
		Last Modified: Wed, 02 Oct 2024 02:00:32 GMT  
		Size: 5.3 KB (5278 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a491fd4c7ee5c3aed461f02515ea56c0b9b5020dfbba8dd1743f5f403fcef12`  
		Last Modified: Wed, 02 Oct 2024 02:00:33 GMT  
		Size: 132.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8acb28f476e186b3c37cc18aa6dbbf8e91f3ee4820f45cc0daa981fa810d1af0`  
		Last Modified: Wed, 02 Oct 2024 02:00:33 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3e9676d1c93647a957de7fcedad2d7efc5f5379bc31536af6e87bcc732c5562`  
		Last Modified: Wed, 02 Oct 2024 02:00:34 GMT  
		Size: 4.6 KB (4626 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:951efba087852f2f3df236b213bc05125289da9a6b9f922adf6afa39b3e8b66e`  
		Last Modified: Wed, 02 Oct 2024 02:00:34 GMT  
		Size: 401.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a368899129b02f96af6461db0da3d43bfd419a98311d1b59894c625dd4fb0657`  
		Last Modified: Wed, 02 Oct 2024 02:00:34 GMT  
		Size: 189.4 KB (189434 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20beb8c34ade62b0713269b2afe177ae2e740f2110dc5e2be20a8c1e708d22c0`  
		Last Modified: Wed, 02 Oct 2024 02:00:35 GMT  
		Size: 1.8 KB (1797 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kibana:8.15.2` - unknown; unknown

```console
$ docker pull kibana@sha256:6cd6657a2ca4007dc900fe839f23567fb6ca8db1877487763122732c9a53a060
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4111146 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e749c4a209c666766c8b16d72dadb76407c9af1957fd12210e48def7dcdecf1`

```dockerfile
```

-	Layers:
	-	`sha256:b0ec45c8db7503bbab7e622a83060ed08b2d4b2a7396570ac5c31e5f081b4c32`  
		Last Modified: Wed, 02 Oct 2024 02:00:32 GMT  
		Size: 4.1 MB (4070754 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9a00fffc378afb96c0c228bff3680593e519d4851416ab16c2003e2b2be0f467`  
		Last Modified: Wed, 02 Oct 2024 02:00:31 GMT  
		Size: 40.4 KB (40392 bytes)  
		MIME: application/vnd.in-toto+json

### `kibana:8.15.2` - linux; arm64 variant v8

```console
$ docker pull kibana@sha256:000c0ae07d7ba3aa0b418cadb181ca666d51134bde1c90ca558f25106090808b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **404.7 MB (404656474 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7789b6d4ced50e1f2d0bab34673c43aea38f4935504e48004a2804ee731c24d2`
-	Entrypoint: `["\/bin\/tini","--"]`
-	Default Command: `["\/usr\/local\/bin\/kibana-docker"]`

```dockerfile
# Thu, 26 Sep 2024 08:08:51 GMT
ARG RELEASE
# Thu, 26 Sep 2024 08:08:51 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 26 Sep 2024 08:08:51 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 26 Sep 2024 08:08:51 GMT
LABEL org.opencontainers.image.version=20.04
# Thu, 26 Sep 2024 08:08:51 GMT
ADD file:8537b4db344382b39d669af27cd94ec0f870ceafe58c67ee54e3f9b38fb8d671 in / 
# Thu, 26 Sep 2024 08:08:51 GMT
CMD ["/bin/bash"]
# Thu, 26 Sep 2024 08:08:51 GMT
EXPOSE map[5601/tcp:{}]
# Thu, 26 Sep 2024 08:08:51 GMT
RUN for iter in {1..10}; do       export DEBIAN_FRONTEND=noninteractive &&       apt-get update  &&       apt-get upgrade -y  &&       apt-get install -y --no-install-recommends        fontconfig libnss3 curl ca-certificates &&       apt-get clean &&       rm -rf /var/lib/apt/lists/* && exit_code=0 && break || exit_code=$? && echo "apt-get error: retry $iter in 10s" &&       sleep 10;     done;     (exit $exit_code) # buildkit
# Thu, 26 Sep 2024 08:08:51 GMT
COPY --chown=1000:0 /usr/share/kibana /usr/share/kibana # buildkit
# Thu, 26 Sep 2024 08:08:51 GMT
COPY --chown=0:0 /bin/tini /bin/tini # buildkit
# Thu, 26 Sep 2024 08:08:51 GMT
COPY --chown=0:0 /usr/share/fonts/local/NotoSansCJK-Regular.ttc /usr/share/fonts/local/NotoSansCJK-Regular.ttc # buildkit
# Thu, 26 Sep 2024 08:08:51 GMT
RUN fc-cache -v # buildkit
# Thu, 26 Sep 2024 08:08:51 GMT
WORKDIR /usr/share/kibana
# Thu, 26 Sep 2024 08:08:51 GMT
RUN ln -s /usr/share/kibana /opt/kibana # buildkit
# Thu, 26 Sep 2024 08:08:51 GMT
ENV ELASTIC_CONTAINER=true
# Thu, 26 Sep 2024 08:08:51 GMT
ENV PATH=/usr/share/kibana/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 26 Sep 2024 08:08:51 GMT
COPY --chown=1000:0 config/kibana.yml /usr/share/kibana/config/kibana.yml # buildkit
# Thu, 26 Sep 2024 08:08:51 GMT
COPY bin/kibana-docker /usr/local/bin/ # buildkit
# Thu, 26 Sep 2024 08:08:51 GMT
RUN chmod g+ws /usr/share/kibana &&     find /usr/share/kibana -gid 0 -and -not -perm /g+w -exec chmod g+w {} \; # buildkit
# Thu, 26 Sep 2024 08:08:51 GMT
RUN find / -xdev -perm -4000 -exec chmod u-s {} + # buildkit
# Thu, 26 Sep 2024 08:08:51 GMT
RUN groupadd --gid 1000 kibana &&     useradd --uid 1000 --gid 1000 -G 0       --home-dir /usr/share/kibana --no-create-home       kibana # buildkit
# Thu, 26 Sep 2024 08:08:51 GMT
LABEL org.label-schema.build-date=2024-09-19T11:10:25.889Z org.label-schema.license=Elastic License org.label-schema.name=Kibana org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/kibana org.label-schema.usage=https://www.elastic.co/guide/en/kibana/reference/index.html org.label-schema.vcs-ref=5a522bfe14bc6d06c20bc337477fd53f7c538973 org.label-schema.vcs-url=https://github.com/elastic/kibana org.label-schema.vendor=Elastic org.label-schema.version=8.15.2 org.opencontainers.image.created=2024-09-19T11:10:25.889Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/kibana/reference/index.html org.opencontainers.image.licenses=Elastic License org.opencontainers.image.revision=5a522bfe14bc6d06c20bc337477fd53f7c538973 org.opencontainers.image.source=https://github.com/elastic/kibana org.opencontainers.image.title=Kibana org.opencontainers.image.url=https://www.elastic.co/products/kibana org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=8.15.2
# Thu, 26 Sep 2024 08:08:51 GMT
ENTRYPOINT ["/bin/tini" "--"]
# Thu, 26 Sep 2024 08:08:51 GMT
CMD ["/usr/local/bin/kibana-docker"]
# Thu, 26 Sep 2024 08:08:51 GMT
USER 1000
```

-	Layers:
	-	`sha256:1b9f3c55f9d4aa5c52eb67a4cb7d0f4726ab85a413b50e3e3fe788befce3d297`  
		Last Modified: Fri, 11 Oct 2024 04:41:30 GMT  
		Size: 26.0 MB (25973828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed6ba831b83cf620584ce3ad5fef753a25663549f8d119af4a0a620914f0f1de`  
		Last Modified: Wed, 16 Oct 2024 03:20:59 GMT  
		Size: 10.8 MB (10818125 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d1ef2f72a6b0df7a49ff43c17a7acf583e3c0afc10225dc48f11b901310be5c`  
		Last Modified: Wed, 16 Oct 2024 03:21:06 GMT  
		Size: 351.2 MB (351198857 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a772ebe0d034552073d8570dd976930bcfd13f459722a9016b64db454d563a88`  
		Last Modified: Wed, 16 Oct 2024 03:20:58 GMT  
		Size: 9.1 KB (9096 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12d1cc0ce12d298e18b6675fca6a7c3a19f8339db94b811a3ad18c081d6a3cb2`  
		Last Modified: Wed, 16 Oct 2024 03:20:59 GMT  
		Size: 16.5 MB (16460486 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:194ee217a7e14f4ba63d4c2e38153e206bd071a2c218c1707523effeaf5ef4e4`  
		Last Modified: Wed, 16 Oct 2024 03:20:59 GMT  
		Size: 5.3 KB (5276 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:487cc1666dc92a76189334afd98c10b91837f3a5439fbab01e1d0caa5fc5acdf`  
		Last Modified: Wed, 16 Oct 2024 03:21:00 GMT  
		Size: 131.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a564565898982f2f2a5e95208056e31ed879e96229169ad552fa47bcc4472d8`  
		Last Modified: Wed, 16 Oct 2024 03:21:00 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4bc1a865b6b95098da80934976cf029af15893e2f0b20ca30e70786ac726a34b`  
		Last Modified: Wed, 16 Oct 2024 03:21:00 GMT  
		Size: 4.6 KB (4623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7168c8c8ff3fde2ea26fcace03e9d5780bd359b98378cee841daa8d0a156993`  
		Last Modified: Wed, 16 Oct 2024 03:21:01 GMT  
		Size: 400.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06d3dba23e4c9e0720dde328f54eb6e2c8de76bc9cff688095217054c04580ed`  
		Last Modified: Wed, 16 Oct 2024 03:21:02 GMT  
		Size: 183.4 KB (183418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68097122ab461cfe82be8f945b924ca1ab540fdbe650f830ee6339fa1bacd1b9`  
		Last Modified: Wed, 16 Oct 2024 03:21:01 GMT  
		Size: 1.8 KB (1804 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kibana:8.15.2` - unknown; unknown

```console
$ docker pull kibana@sha256:6dfc306a8537687a0ef8f71fd9c713628519877dbb404e26dfdb2462a1ace823
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4111672 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb4d6dc8e5816843bb2b7cede4e554054ad16990cac0553f37a7011368a10659`

```dockerfile
```

-	Layers:
	-	`sha256:8b75ef73089df04d755ed4d03d66288e6fc4aeb53c6427265eb787161ff64c4a`  
		Last Modified: Wed, 16 Oct 2024 03:20:59 GMT  
		Size: 4.1 MB (4071004 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c892dc76f20da428e82b41607c9881ec0bb9b05ac0e895f7b105ba77a8b67d55`  
		Last Modified: Wed, 16 Oct 2024 03:20:58 GMT  
		Size: 40.7 KB (40668 bytes)  
		MIME: application/vnd.in-toto+json
