<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `kibana`

-	[`kibana:7.17.24`](#kibana71724)
-	[`kibana:8.15.2`](#kibana8152)

## `kibana:7.17.24`

```console
$ docker pull kibana@sha256:63c031b977b9a84b8c3cd519d74300a9be308ac813ba2a0f4bce3283b6103f45
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
$ docker pull kibana@sha256:edcfcded3f02aa673a563b7ad5e91cece046fb205e16494fbfff7c563c501197
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **359.9 MB (359915237 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0998989922123422adb169e28a3c088efe7afc7a81f52cb06cd7095214226889`
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
ADD file:193e44687e108da6ce3970dd4e85b4ab975e008873500871bb89e452afe82d52 in / 
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
	-	`sha256:f7087ec3f63a82386ce40d74d075d761ece5bfaefdc30b9ef62f73ecfb2e41fe`  
		Last Modified: Wed, 18 Sep 2024 05:32:46 GMT  
		Size: 26.0 MB (25973592 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25424d07ccf7351a2d55edfaafd5e9c42655d44b1608f79e993e0b99b7988278`  
		Last Modified: Wed, 02 Oct 2024 03:01:36 GMT  
		Size: 10.6 MB (10574961 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b58b1fc0a3139a7fb884e2f25aa46f8d87790f77a5819d5a30f5cfed485ee714`  
		Last Modified: Wed, 02 Oct 2024 03:01:35 GMT  
		Size: 9.1 KB (9091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da9ae7ee76f9d147fb8b9829dfe7abf77656d266da4395d2e2d5d54fa1f832db`  
		Last Modified: Wed, 02 Oct 2024 03:01:35 GMT  
		Size: 157.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3974258476c0903831987b7d3377c3251bc41fc0260362e64d648c6c7a0bdfa6`  
		Last Modified: Wed, 02 Oct 2024 03:01:36 GMT  
		Size: 16.5 MB (16460479 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:110d9405350600e0a9e488d1e0f7a5f53d9c1bc3727b9eeaab5a7c4a0166a31b`  
		Last Modified: Wed, 02 Oct 2024 03:01:36 GMT  
		Size: 5.3 KB (5303 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e87b471d228d27b8dad71522c7d6fd3c38a44d380698dbe6decf7059f32e5ef`  
		Last Modified: Wed, 02 Oct 2024 03:01:43 GMT  
		Size: 306.7 MB (306700933 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34bf9e48213a8346bd14bb2b5a1ab1298f981cc0b92c44e1448691a7932d1346`  
		Last Modified: Wed, 02 Oct 2024 03:01:37 GMT  
		Size: 132.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a08b893b767f23771058c993f35887dc977a02e2d2c6eb2e12dc1e0d291b2ae3`  
		Last Modified: Wed, 02 Oct 2024 03:01:37 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b6ddd10743a2364004376a33bae05eb71efd89fc684c5fe640ae3b7f5965121`  
		Last Modified: Wed, 02 Oct 2024 03:01:37 GMT  
		Size: 4.5 KB (4506 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8f5529f2a56cd9bddec59df1143a54e117d5981185eb75e9dc6d4085407c195`  
		Last Modified: Wed, 02 Oct 2024 03:01:38 GMT  
		Size: 400.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4370241a0f1a95289dd086a854cbcbe235a5ac165fb47f1906cba4ccd2ff2278`  
		Last Modified: Wed, 02 Oct 2024 03:01:38 GMT  
		Size: 183.4 KB (183417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:776d0743f2db9e54155f96c595203a0130075b3996ca01a4621f4b5a5ffcd474`  
		Last Modified: Wed, 02 Oct 2024 03:01:38 GMT  
		Size: 1.8 KB (1805 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kibana:7.17.24` - unknown; unknown

```console
$ docker pull kibana@sha256:d98e4435a8d4144f1b7950cba0210130e5ad9241145a045faed762d9f93642c5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.4 MB (3426150 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a6e939d1f0db224f4398338e293a1491f0502377d555e8227baaa897c609e4e`

```dockerfile
```

-	Layers:
	-	`sha256:c9f8c6a4f34c88b8d2e177de212a549146efa0106b006fb64a7cbccda3976876`  
		Last Modified: Wed, 02 Oct 2024 03:01:35 GMT  
		Size: 3.4 MB (3381618 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:87765218058e817db911e55b1fd761e6527d0761e44dd19ba8b06fbe87f657c3`  
		Last Modified: Wed, 02 Oct 2024 03:01:35 GMT  
		Size: 44.5 KB (44532 bytes)  
		MIME: application/vnd.in-toto+json

## `kibana:8.15.2`

```console
$ docker pull kibana@sha256:eb531ec902bfc952c98c94ab135d723dec692f0716a991154f0af08ba4590b33
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
$ docker pull kibana@sha256:0bd827a6462d34a581688edd41d73b776cf417efe4385c18cee3b23fb16dcc53
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **404.7 MB (404656236 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fee6191bd9010772486fdf39b0a71caa79065d0b2d5196f3f0df02a6d4c57b2c`
-	Entrypoint: `["\/bin\/tini","--"]`
-	Default Command: `["\/usr\/local\/bin\/kibana-docker"]`

```dockerfile
# Wed, 18 Sep 2024 04:18:13 GMT
ARG RELEASE
# Wed, 18 Sep 2024 04:18:13 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 18 Sep 2024 04:18:13 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 18 Sep 2024 04:18:13 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 18 Sep 2024 04:18:15 GMT
ADD file:193e44687e108da6ce3970dd4e85b4ab975e008873500871bb89e452afe82d52 in / 
# Wed, 18 Sep 2024 04:18:15 GMT
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
	-	`sha256:f7087ec3f63a82386ce40d74d075d761ece5bfaefdc30b9ef62f73ecfb2e41fe`  
		Last Modified: Wed, 18 Sep 2024 05:32:46 GMT  
		Size: 26.0 MB (25973592 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:877fd225e07252c89c103332530b8b836f3169e2a2b9b61d6c055a0019a08089`  
		Last Modified: Wed, 02 Oct 2024 02:57:56 GMT  
		Size: 10.8 MB (10818062 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:477d33e0432d6e05dab48f05322df9a23eb4a139633d4edf4e326c1d77c863c6`  
		Last Modified: Wed, 02 Oct 2024 02:58:03 GMT  
		Size: 351.2 MB (351198919 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02d4132ec6cb354838e2aacabb575a6473ff008d0c62e5360cf74ab229cac330`  
		Last Modified: Wed, 02 Oct 2024 02:57:55 GMT  
		Size: 9.1 KB (9096 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0edd3fdd25dbe68ef3dcbb106cec5e4fde6debe2ce7f5dfdde15803940a4e3b1`  
		Last Modified: Wed, 02 Oct 2024 02:57:57 GMT  
		Size: 16.5 MB (16460477 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9bcf043542a3ee623fd8333c477ecd70b4dfa06349557da3e07ae932065b6345`  
		Last Modified: Wed, 02 Oct 2024 02:57:56 GMT  
		Size: 5.3 KB (5282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3089da05203bfcd9185eaefcfcf13a0fbdf253e7f3bd840aa0fc9104c9da4471`  
		Last Modified: Wed, 02 Oct 2024 02:57:57 GMT  
		Size: 132.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c175d6232ff9e1795ffac1ae5cadef0a20d4c3ced02542c8575e3c2402f152a`  
		Last Modified: Wed, 02 Oct 2024 02:57:57 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b47549e5ab1e13b0bbc5a5a07a85406b45203122d131912bcae9b771bebcab3`  
		Last Modified: Wed, 02 Oct 2024 02:57:58 GMT  
		Size: 4.6 KB (4624 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6c70309427326299c3af82e72d29b5fc3a401673e7d6de1f2b03beae6313a5f`  
		Last Modified: Wed, 02 Oct 2024 02:57:58 GMT  
		Size: 400.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27997dc824d53b1b8882340d49740967061722969a18124b4ad375e3abaaafbe`  
		Last Modified: Wed, 02 Oct 2024 02:57:58 GMT  
		Size: 183.4 KB (183419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57823ff55b84a51cb2aadd62ae94be243f87855797851c4f383a1046dfb6785e`  
		Last Modified: Wed, 02 Oct 2024 02:57:59 GMT  
		Size: 1.8 KB (1805 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kibana:8.15.2` - unknown; unknown

```console
$ docker pull kibana@sha256:f3d9d562ed2fe0fb40e201aab289bf18fcbe4937129ccd7c7395361a214a20c9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4111639 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d4caa42d0d5f44757ade4484796ac94cfd38f1a693908e629cac36e4756a241`

```dockerfile
```

-	Layers:
	-	`sha256:4bd7d83f51756be04b090c0022b17d3870ace9bd4067f0edafc01939546ab755`  
		Last Modified: Wed, 02 Oct 2024 02:57:55 GMT  
		Size: 4.1 MB (4071004 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:442b31a702d90d766573c8a330848b2d2655850d32ba2196a69674f1b25d6cf3`  
		Last Modified: Wed, 02 Oct 2024 02:57:55 GMT  
		Size: 40.6 KB (40635 bytes)  
		MIME: application/vnd.in-toto+json
