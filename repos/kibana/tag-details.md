<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `kibana`

-	[`kibana:7.17.7`](#kibana7177)
-	[`kibana:8.5.0`](#kibana850)

## `kibana:7.17.7`

```console
$ docker pull kibana@sha256:414b6a159b8ab8049bcf45236d7ec86bc0238ba9ec86fbd362e948c09cc34991
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `kibana:7.17.7` - linux; amd64

```console
$ docker pull kibana@sha256:688e915984126d61b8602c8ab12c0e63b7d6d5d734a6743cd144baf9c92fdc24
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **325.2 MB (325226252 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:47c5b6ca1535b5be025db5fc594ec5d1592e82653691bf7a4d7568c80f11dfa8`
-	Entrypoint: `["\/bin\/tini","--"]`
-	Default Command: `["\/usr\/local\/bin\/kibana-docker"]`

```dockerfile
# Tue, 04 Oct 2022 23:35:12 GMT
ADD file:8faed18d471598732aa3816c8f70e227f16f4de5db6c5c32812a09141048f56d in / 
# Tue, 04 Oct 2022 23:35:12 GMT
CMD ["bash"]
# Thu, 13 Oct 2022 11:33:52 GMT
EXPOSE map[5601/tcp:{}]
# Thu, 13 Oct 2022 11:33:52 GMT
RUN for iter in {1..10}; do       export DEBIAN_FRONTEND=noninteractive &&       apt-get update  &&       apt-get upgrade -y  &&       apt-get install -y --no-install-recommends        fontconfig fonts-liberation libnss3 libfontconfig1 ca-certificates curl &&       apt-get clean &&       rm -rf /var/lib/apt/lists/* && exit_code=0 && break || exit_code=$? && echo "apt-get error: retry $iter in 10s" &&       sleep 10;     done;     (exit $exit_code) # buildkit
# Thu, 13 Oct 2022 11:33:54 GMT
RUN set -e ;     TINI_BIN="" ;     case "$(arch)" in         aarch64)             TINI_BIN='tini-arm64' ;             ;;         x86_64)             TINI_BIN='tini-amd64' ;             ;;         *) echo >&2 "Unsupported architecture $(arch)" ; exit 1 ;;     esac ;   TINI_VERSION='v0.19.0' ;   curl --retry 8 -S -L -O "https://github.com/krallin/tini/releases/download/${TINI_VERSION}/${TINI_BIN}" ;   curl --retry 8 -S -L -O "https://github.com/krallin/tini/releases/download/${TINI_VERSION}/${TINI_BIN}.sha256sum" ;   sha256sum -c "${TINI_BIN}.sha256sum" ;   rm "${TINI_BIN}.sha256sum" ;   mv "${TINI_BIN}" /bin/tini ;   chmod +x /bin/tini # buildkit
# Thu, 13 Oct 2022 11:33:54 GMT
RUN mkdir /usr/share/fonts/local # buildkit
# Thu, 13 Oct 2022 11:33:55 GMT
RUN curl --retry 8 -S -L -o /usr/share/fonts/local/NotoSansCJK-Regular.ttc https://github.com/googlefonts/noto-cjk/raw/NotoSansV2.001/NotoSansCJK-Regular.ttc # buildkit
# Thu, 13 Oct 2022 11:33:55 GMT
RUN echo "5dcd1c336cc9344cb77c03a0cd8982ca8a7dc97d620fd6c9c434e02dcb1ceeb3  /usr/share/fonts/local/NotoSansCJK-Regular.ttc" | sha256sum -c - # buildkit
# Thu, 13 Oct 2022 11:33:56 GMT
RUN fc-cache -v # buildkit
# Thu, 13 Oct 2022 11:34:53 GMT
COPY /usr/share/kibana /usr/share/kibana # buildkit
# Thu, 13 Oct 2022 11:34:53 GMT
WORKDIR /usr/share/kibana
# Thu, 13 Oct 2022 11:34:53 GMT
RUN ln -s /usr/share/kibana /opt/kibana # buildkit
# Thu, 13 Oct 2022 11:34:53 GMT
ENV ELASTIC_CONTAINER=true
# Thu, 13 Oct 2022 11:34:53 GMT
ENV PATH=/usr/share/kibana/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 13 Oct 2022 11:34:53 GMT
COPY config/kibana.yml /usr/share/kibana/config/kibana.yml # buildkit
# Thu, 13 Oct 2022 11:34:53 GMT
COPY bin/kibana-docker /usr/local/bin/ # buildkit
# Thu, 13 Oct 2022 11:34:54 GMT
RUN chmod g+ws /usr/share/kibana &&     find /usr/share/kibana -gid 0 -and -not -perm /g+w -exec chmod g+w {} \; # buildkit
# Thu, 13 Oct 2022 11:34:55 GMT
RUN find / -xdev -perm -4000 -exec chmod u-s {} + # buildkit
# Thu, 13 Oct 2022 11:34:55 GMT
RUN groupadd --gid 1000 kibana &&     useradd --uid 1000 --gid 1000 -G 0       --home-dir /usr/share/kibana --no-create-home       kibana # buildkit
# Thu, 13 Oct 2022 11:34:55 GMT
LABEL org.label-schema.build-date=2022-10-13T11:08:08.384Z org.label-schema.license=Elastic License org.label-schema.name=Kibana org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/kibana org.label-schema.usage=https://www.elastic.co/guide/en/kibana/reference/index.html org.label-schema.vcs-ref=d60b53b0f972a3e59c06c2cb1bf5818f92d1cb63 org.label-schema.vcs-url=https://github.com/elastic/kibana org.label-schema.vendor=Elastic org.label-schema.version=7.17.7 org.opencontainers.image.created=2022-10-13T11:08:08.384Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/kibana/reference/index.html org.opencontainers.image.licenses=Elastic License org.opencontainers.image.revision=d60b53b0f972a3e59c06c2cb1bf5818f92d1cb63 org.opencontainers.image.source=https://github.com/elastic/kibana org.opencontainers.image.title=Kibana org.opencontainers.image.url=https://www.elastic.co/products/kibana org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=7.17.7
# Thu, 13 Oct 2022 11:34:55 GMT
ENTRYPOINT ["/bin/tini" "--"]
# Thu, 13 Oct 2022 11:34:55 GMT
CMD ["/usr/local/bin/kibana-docker"]
# Thu, 13 Oct 2022 11:34:55 GMT
USER kibana
```

-	Layers:
	-	`sha256:fb0b3276a519f5e7085f51c75989b287b234b3508e1524cf2cdcbc397c06ec3d`  
		Last Modified: Thu, 22 Sep 2022 20:37:52 GMT  
		Size: 28.6 MB (28574451 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ff10acfee0ec519331e95c95a78953d67fb530cfde3f6f3bf3fd2246da19ad0`  
		Last Modified: Thu, 27 Oct 2022 00:21:26 GMT  
		Size: 10.9 MB (10859172 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:389dd4b16fb3c8bbfedf30e8088075a5cca6f1de6852e8ccfa52242f33b58ad6`  
		Last Modified: Thu, 27 Oct 2022 00:21:24 GMT  
		Size: 9.5 KB (9525 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0a153be433adce4c78f7b2f6b3ad3048ef4304ceeb25271372f4d06e69c9e9b`  
		Last Modified: Thu, 27 Oct 2022 00:21:22 GMT  
		Size: 159.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f70ada2dbae717de01734e027164f46178c2304a58c702dd5488375e1b2c347`  
		Last Modified: Thu, 27 Oct 2022 00:21:23 GMT  
		Size: 16.5 MB (16460493 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f886755e1faef990bf587c830745fc38bde61889959e4ff9a57436b97921e858`  
		Last Modified: Thu, 27 Oct 2022 00:21:22 GMT  
		Size: 5.3 KB (5289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71c4c41a32c356534571e15346f0bfeaaa565a5482cfbc17ac4f031a639654f1`  
		Last Modified: Thu, 27 Oct 2022 00:21:55 GMT  
		Size: 269.1 MB (269120450 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f06e31ef44b16d3b808aa158ec91285ba48fc3ce46be97b7ca03d735a290dbc6`  
		Last Modified: Thu, 27 Oct 2022 00:21:21 GMT  
		Size: 134.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa5de441a7b60e60d77a2166ee22dcd97bd6a7af69ca118300ca283083ff8ff1`  
		Last Modified: Thu, 27 Oct 2022 00:21:19 GMT  
		Size: 397.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9501cd64e5ec0558ef787e9591111e154ae854a739d8de870da22b00fe1c56e6`  
		Last Modified: Thu, 27 Oct 2022 00:21:19 GMT  
		Size: 4.5 KB (4506 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8aa2ba840eb00f5fc27bb15cb17656aa0ef143f92d5d7af3f9319ad5f4c50609`  
		Last Modified: Thu, 27 Oct 2022 00:21:19 GMT  
		Size: 400.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09b573bb90bed58e0e68bb340d1430d88392e3e595c733fbe91be59909b46350`  
		Last Modified: Thu, 27 Oct 2022 00:21:19 GMT  
		Size: 189.4 KB (189391 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb60bde26a17c014793459708c56c923a6c3a673d6f0c39bea9f7a05ffaef91e`  
		Last Modified: Thu, 27 Oct 2022 00:21:19 GMT  
		Size: 1.8 KB (1821 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kibana:7.17.7` - linux; arm64 variant v8

```console
$ docker pull kibana@sha256:84781310f0f3dce3a4892160d64497e3d16aff2bd1fcc4c5832d0b19865a9289
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **338.4 MB (338353583 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c229fd67efd81d3f0b2b2e5ecfc60cb22f6a92d52197ebead46d713d2fbaac64`
-	Entrypoint: `["\/bin\/tini","--"]`
-	Default Command: `["\/usr\/local\/bin\/kibana-docker"]`

```dockerfile
# Wed, 05 Oct 2022 00:02:10 GMT
ADD file:30b589901d2a6b82d0b7271487bdaf37514649a798cc13a17f74394321bdd051 in / 
# Wed, 05 Oct 2022 00:02:11 GMT
CMD ["bash"]
# Thu, 13 Oct 2022 11:36:55 GMT
EXPOSE map[5601/tcp:{}]
# Thu, 13 Oct 2022 11:36:55 GMT
RUN for iter in {1..10}; do       export DEBIAN_FRONTEND=noninteractive &&       apt-get update  &&       apt-get upgrade -y  &&       apt-get install -y --no-install-recommends        fontconfig fonts-liberation libnss3 libfontconfig1 ca-certificates curl &&       apt-get clean &&       rm -rf /var/lib/apt/lists/* && exit_code=0 && break || exit_code=$? && echo "apt-get error: retry $iter in 10s" &&       sleep 10;     done;     (exit $exit_code) # buildkit
# Thu, 13 Oct 2022 11:36:57 GMT
RUN set -e ;     TINI_BIN="" ;     case "$(arch)" in         aarch64)             TINI_BIN='tini-arm64' ;             ;;         x86_64)             TINI_BIN='tini-amd64' ;             ;;         *) echo >&2 "Unsupported architecture $(arch)" ; exit 1 ;;     esac ;   TINI_VERSION='v0.19.0' ;   curl --retry 8 -S -L -O "https://github.com/krallin/tini/releases/download/${TINI_VERSION}/${TINI_BIN}" ;   curl --retry 8 -S -L -O "https://github.com/krallin/tini/releases/download/${TINI_VERSION}/${TINI_BIN}.sha256sum" ;   sha256sum -c "${TINI_BIN}.sha256sum" ;   rm "${TINI_BIN}.sha256sum" ;   mv "${TINI_BIN}" /bin/tini ;   chmod +x /bin/tini # buildkit
# Thu, 13 Oct 2022 11:36:58 GMT
RUN mkdir /usr/share/fonts/local # buildkit
# Thu, 13 Oct 2022 11:37:00 GMT
RUN curl --retry 8 -S -L -o /usr/share/fonts/local/NotoSansCJK-Regular.ttc https://github.com/googlefonts/noto-cjk/raw/NotoSansV2.001/NotoSansCJK-Regular.ttc # buildkit
# Thu, 13 Oct 2022 11:37:01 GMT
RUN echo "5dcd1c336cc9344cb77c03a0cd8982ca8a7dc97d620fd6c9c434e02dcb1ceeb3  /usr/share/fonts/local/NotoSansCJK-Regular.ttc" | sha256sum -c - # buildkit
# Thu, 13 Oct 2022 11:37:02 GMT
RUN fc-cache -v # buildkit
# Thu, 13 Oct 2022 11:37:57 GMT
COPY /usr/share/kibana /usr/share/kibana # buildkit
# Thu, 13 Oct 2022 11:37:57 GMT
WORKDIR /usr/share/kibana
# Thu, 13 Oct 2022 11:37:57 GMT
RUN ln -s /usr/share/kibana /opt/kibana # buildkit
# Thu, 13 Oct 2022 11:37:57 GMT
ENV ELASTIC_CONTAINER=true
# Thu, 13 Oct 2022 11:37:57 GMT
ENV PATH=/usr/share/kibana/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 13 Oct 2022 11:37:57 GMT
COPY config/kibana.yml /usr/share/kibana/config/kibana.yml # buildkit
# Thu, 13 Oct 2022 11:37:57 GMT
COPY bin/kibana-docker /usr/local/bin/ # buildkit
# Thu, 13 Oct 2022 11:37:58 GMT
RUN chmod g+ws /usr/share/kibana &&     find /usr/share/kibana -gid 0 -and -not -perm /g+w -exec chmod g+w {} \; # buildkit
# Thu, 13 Oct 2022 11:37:59 GMT
RUN find / -xdev -perm -4000 -exec chmod u-s {} + # buildkit
# Thu, 13 Oct 2022 11:38:00 GMT
RUN groupadd --gid 1000 kibana &&     useradd --uid 1000 --gid 1000 -G 0       --home-dir /usr/share/kibana --no-create-home       kibana # buildkit
# Thu, 13 Oct 2022 11:38:00 GMT
LABEL org.label-schema.build-date=2022-10-13T11:08:08.384Z org.label-schema.license=Elastic License org.label-schema.name=Kibana org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/kibana org.label-schema.usage=https://www.elastic.co/guide/en/kibana/reference/index.html org.label-schema.vcs-ref=d60b53b0f972a3e59c06c2cb1bf5818f92d1cb63 org.label-schema.vcs-url=https://github.com/elastic/kibana org.label-schema.vendor=Elastic org.label-schema.version=7.17.7 org.opencontainers.image.created=2022-10-13T11:08:08.384Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/kibana/reference/index.html org.opencontainers.image.licenses=Elastic License org.opencontainers.image.revision=d60b53b0f972a3e59c06c2cb1bf5818f92d1cb63 org.opencontainers.image.source=https://github.com/elastic/kibana org.opencontainers.image.title=Kibana org.opencontainers.image.url=https://www.elastic.co/products/kibana org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=7.17.7
# Thu, 13 Oct 2022 11:38:00 GMT
ENTRYPOINT ["/bin/tini" "--"]
# Thu, 13 Oct 2022 11:38:00 GMT
CMD ["/usr/local/bin/kibana-docker"]
# Thu, 13 Oct 2022 11:38:00 GMT
USER kibana
```

-	Layers:
	-	`sha256:514fa78e57ce0d9437bc984cc36ab780c24b69da2b922bfff16737072e3e7de2`  
		Last Modified: Wed, 05 Oct 2022 00:03:51 GMT  
		Size: 27.2 MB (27191622 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3529e72c508ff0c278baa082272c33398313d46c0d9ce9fe40a40b4c5a08da00`  
		Last Modified: Wed, 26 Oct 2022 20:29:50 GMT  
		Size: 10.7 MB (10722256 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0585400ab4eb919c7b7b17055696358f9e4af11b6cdd0251d119c9c061722023`  
		Last Modified: Wed, 26 Oct 2022 20:29:48 GMT  
		Size: 9.1 KB (9097 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b45335f3c1dd3a8f1dfba84038b846f342d7b1ba1a8871c8ca3c9d0ee50489f`  
		Last Modified: Wed, 26 Oct 2022 20:29:47 GMT  
		Size: 159.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3379c494583da78edbdc81aaa481b82306ef148a817430fffe6020c10f361dde`  
		Last Modified: Wed, 26 Oct 2022 20:29:49 GMT  
		Size: 16.5 MB (16460495 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8468d973542b3c8616b0e8cbbdcbf23e1ee004fe61e1eed3cc65e2769861a6cc`  
		Last Modified: Wed, 26 Oct 2022 20:29:46 GMT  
		Size: 5.3 KB (5287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34b77109bc67edcca176d061e28487d7fb4067172185df235fd7071892f70844`  
		Last Modified: Wed, 26 Oct 2022 20:30:11 GMT  
		Size: 283.8 MB (283773951 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:775d06ca9fb9ed231701a4f0f43778cae2dd0389bffb23de3d9596029ddfb4cc`  
		Last Modified: Wed, 26 Oct 2022 20:29:45 GMT  
		Size: 133.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1528dd9baaf0de5faa6896d397c81ea5e36406ff305f788dfbdbe5192cdae47b`  
		Last Modified: Wed, 26 Oct 2022 20:29:42 GMT  
		Size: 395.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1102316d9fbdf06487275aacff53ad9f16bc43813feaabcbeafc21da91bc4669`  
		Last Modified: Wed, 26 Oct 2022 20:29:42 GMT  
		Size: 4.5 KB (4506 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:790d774652bfa0418ce89a7f709b6dd2cbcca55262d1be69a323252c86ea5690`  
		Last Modified: Wed, 26 Oct 2022 20:29:42 GMT  
		Size: 397.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:906e4ce11fd4ef4bf903429529f67328c7a8130516be2ff143b3dabacd673ac2`  
		Last Modified: Wed, 26 Oct 2022 20:29:43 GMT  
		Size: 183.4 KB (183395 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5be51d178a5092cb1ad5b51052bf3ccf28f29ccd4c52c5506fbe3d7e335b4b60`  
		Last Modified: Wed, 26 Oct 2022 20:29:46 GMT  
		Size: 1.8 KB (1826 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kibana:8.5.0`

```console
$ docker pull kibana@sha256:a6ebeab5aeeada5772739991b4e242f3970f8c8a622330801136a4129e3564d3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `kibana:8.5.0` - linux; amd64

```console
$ docker pull kibana@sha256:104b20b634c1e2f282ddc939a29e422154b590e2f5bc339257374ce9ac13e711
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **285.5 MB (285508914 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4737b8e943ba21f022ea7b898de744793f01bc5d96ab0fc5874de415f20c9684`
-	Entrypoint: `["\/bin\/tini","--"]`
-	Default Command: `["\/usr\/local\/bin\/kibana-docker"]`

```dockerfile
# Tue, 04 Oct 2022 23:35:12 GMT
ADD file:8faed18d471598732aa3816c8f70e227f16f4de5db6c5c32812a09141048f56d in / 
# Tue, 04 Oct 2022 23:35:12 GMT
CMD ["bash"]
# Mon, 24 Oct 2022 11:31:17 GMT
EXPOSE map[5601/tcp:{}]
# Mon, 24 Oct 2022 11:31:17 GMT
RUN for iter in {1..10}; do       export DEBIAN_FRONTEND=noninteractive &&       apt-get update  &&       apt-get upgrade -y  &&       apt-get install -y --no-install-recommends        fontconfig fonts-liberation libnss3 libfontconfig1 ca-certificates curl &&       apt-get clean &&       rm -rf /var/lib/apt/lists/* && exit_code=0 && break || exit_code=$? && echo "apt-get error: retry $iter in 10s" &&       sleep 10;     done;     (exit $exit_code) # buildkit
# Mon, 24 Oct 2022 11:31:18 GMT
RUN set -e ;     TINI_BIN="" ;     case "$(arch)" in         aarch64)             TINI_BIN='tini-arm64' ;             ;;         x86_64)             TINI_BIN='tini-amd64' ;             ;;         *) echo >&2 "Unsupported architecture $(arch)" ; exit 1 ;;     esac ;   TINI_VERSION='v0.19.0' ;   curl --retry 8 -S -L -O "https://github.com/krallin/tini/releases/download/${TINI_VERSION}/${TINI_BIN}" ;   curl --retry 8 -S -L -O "https://github.com/krallin/tini/releases/download/${TINI_VERSION}/${TINI_BIN}.sha256sum" ;   sha256sum -c "${TINI_BIN}.sha256sum" ;   rm "${TINI_BIN}.sha256sum" ;   mv "${TINI_BIN}" /bin/tini ;   chmod +x /bin/tini # buildkit
# Mon, 24 Oct 2022 11:31:19 GMT
RUN mkdir /usr/share/fonts/local # buildkit
# Mon, 24 Oct 2022 11:31:19 GMT
RUN curl --retry 8 -S -L -o /usr/share/fonts/local/NotoSansCJK-Regular.ttc https://github.com/googlefonts/noto-cjk/raw/NotoSansV2.001/NotoSansCJK-Regular.ttc # buildkit
# Mon, 24 Oct 2022 11:31:20 GMT
RUN echo "5dcd1c336cc9344cb77c03a0cd8982ca8a7dc97d620fd6c9c434e02dcb1ceeb3  /usr/share/fonts/local/NotoSansCJK-Regular.ttc" | sha256sum -c - # buildkit
# Mon, 24 Oct 2022 11:31:20 GMT
RUN fc-cache -v # buildkit
# Mon, 24 Oct 2022 11:32:23 GMT
COPY /usr/share/kibana /usr/share/kibana # buildkit
# Mon, 24 Oct 2022 11:32:23 GMT
WORKDIR /usr/share/kibana
# Mon, 24 Oct 2022 11:32:24 GMT
RUN ln -s /usr/share/kibana /opt/kibana # buildkit
# Mon, 24 Oct 2022 11:32:24 GMT
ENV ELASTIC_CONTAINER=true
# Mon, 24 Oct 2022 11:32:24 GMT
ENV PATH=/usr/share/kibana/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 24 Oct 2022 11:32:24 GMT
COPY config/kibana.yml /usr/share/kibana/config/kibana.yml # buildkit
# Mon, 24 Oct 2022 11:32:24 GMT
COPY bin/kibana-docker /usr/local/bin/ # buildkit
# Mon, 24 Oct 2022 11:32:24 GMT
RUN chmod g+ws /usr/share/kibana &&     find /usr/share/kibana -gid 0 -and -not -perm /g+w -exec chmod g+w {} \; # buildkit
# Mon, 24 Oct 2022 11:32:25 GMT
RUN find / -xdev -perm -4000 -exec chmod u-s {} + # buildkit
# Mon, 24 Oct 2022 11:32:25 GMT
RUN groupadd --gid 1000 kibana &&     useradd --uid 1000 --gid 1000 -G 0       --home-dir /usr/share/kibana --no-create-home       kibana # buildkit
# Mon, 24 Oct 2022 11:32:25 GMT
LABEL org.label-schema.build-date=2022-10-24T11:08:22.637Z org.label-schema.license=Elastic License org.label-schema.name=Kibana org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/kibana org.label-schema.usage=https://www.elastic.co/guide/en/kibana/reference/index.html org.label-schema.vcs-ref=3db77af5d7066697635ad3e1eeeae81a92ae9711 org.label-schema.vcs-url=https://github.com/elastic/kibana org.label-schema.vendor=Elastic org.label-schema.version=8.5.0 org.opencontainers.image.created=2022-10-24T11:08:22.637Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/kibana/reference/index.html org.opencontainers.image.licenses=Elastic License org.opencontainers.image.revision=3db77af5d7066697635ad3e1eeeae81a92ae9711 org.opencontainers.image.source=https://github.com/elastic/kibana org.opencontainers.image.title=Kibana org.opencontainers.image.url=https://www.elastic.co/products/kibana org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=8.5.0
# Mon, 24 Oct 2022 11:32:25 GMT
ENTRYPOINT ["/bin/tini" "--"]
# Mon, 24 Oct 2022 11:32:25 GMT
CMD ["/usr/local/bin/kibana-docker"]
# Mon, 24 Oct 2022 11:32:25 GMT
USER kibana
```

-	Layers:
	-	`sha256:fb0b3276a519f5e7085f51c75989b287b234b3508e1524cf2cdcbc397c06ec3d`  
		Last Modified: Thu, 22 Sep 2022 20:37:52 GMT  
		Size: 28.6 MB (28574451 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2850271de0a40e81bbf63b96ab826abe809e2958d6a273f01409aa8aa897d797`  
		Last Modified: Wed, 02 Nov 2022 18:23:55 GMT  
		Size: 13.1 MB (13062434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84c86256fd54f303b678b80180b78b21eeed0da057b577e0acec3078390ac95c`  
		Last Modified: Wed, 02 Nov 2022 18:23:53 GMT  
		Size: 9.5 KB (9527 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32d573bfcd3848bd52eaf2554fafbb8a3643e83840e14707670213d9864fbea5`  
		Last Modified: Wed, 02 Nov 2022 18:23:51 GMT  
		Size: 161.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a928f9f2cecef35bbd246164a91803d105ff3e7552916f0f1583c0c5b6a1bb0`  
		Last Modified: Wed, 02 Nov 2022 18:23:52 GMT  
		Size: 16.5 MB (16460488 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c5fe6e9504b3dcfea8e9ddc9995550667f9afd7ba73e8de7093befc6d453699`  
		Last Modified: Wed, 02 Nov 2022 18:23:50 GMT  
		Size: 5.3 KB (5289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d4859fe6051e48bb2cc555aaa4ceceb0691f1dba99ead2aa864e0759865eab9`  
		Last Modified: Wed, 02 Nov 2022 18:24:19 GMT  
		Size: 227.2 MB (227199944 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e29c68241870523f5921f2417ebc5b60c6ef46939f81d31c59c32d6b119ae4ed`  
		Last Modified: Wed, 02 Nov 2022 18:23:50 GMT  
		Size: 133.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e118038248de6fc6ffa5102992cd44935bc667d80590ffa0b22ddd6f4cb5a5f`  
		Last Modified: Wed, 02 Nov 2022 18:23:48 GMT  
		Size: 396.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e28677a2c8001ce0f3ed2966f2f61b9a8db9afe52f3635f94748c346e9c01222`  
		Last Modified: Wed, 02 Nov 2022 18:23:48 GMT  
		Size: 4.4 KB (4418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:195f6c332d2662dc4583984e5036b1807926fc0058c40a2700274963a038b90d`  
		Last Modified: Wed, 02 Nov 2022 18:23:48 GMT  
		Size: 398.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e15e8431a44aed660a68ede809a852575c44d36876688950c1280e6fd9445293`  
		Last Modified: Wed, 02 Nov 2022 18:23:48 GMT  
		Size: 189.4 KB (189393 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d82e19c378bc87fc86f6098f6fbd81f527d0573eeadfd755f1d18c6130beb44a`  
		Last Modified: Wed, 02 Nov 2022 18:23:48 GMT  
		Size: 1.8 KB (1818 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kibana:8.5.0` - linux; arm64 variant v8

```console
$ docker pull kibana@sha256:a583c148aa8eb3da47be874e9ad6566b94fe1bda300a36b1eb0930cd84fa5de8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **300.3 MB (300258512 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe6250c95a1c5772b15db6e6b46d2bff68f91c125c032aa6284296cb957828f7`
-	Entrypoint: `["\/bin\/tini","--"]`
-	Default Command: `["\/usr\/local\/bin\/kibana-docker"]`

```dockerfile
# Wed, 05 Oct 2022 00:02:10 GMT
ADD file:30b589901d2a6b82d0b7271487bdaf37514649a798cc13a17f74394321bdd051 in / 
# Wed, 05 Oct 2022 00:02:11 GMT
CMD ["bash"]
# Mon, 24 Oct 2022 11:34:27 GMT
EXPOSE map[5601/tcp:{}]
# Mon, 24 Oct 2022 11:34:27 GMT
RUN for iter in {1..10}; do       export DEBIAN_FRONTEND=noninteractive &&       apt-get update  &&       apt-get upgrade -y  &&       apt-get install -y --no-install-recommends        fontconfig fonts-liberation libnss3 libfontconfig1 ca-certificates curl &&       apt-get clean &&       rm -rf /var/lib/apt/lists/* && exit_code=0 && break || exit_code=$? && echo "apt-get error: retry $iter in 10s" &&       sleep 10;     done;     (exit $exit_code) # buildkit
# Mon, 24 Oct 2022 11:34:29 GMT
RUN set -e ;     TINI_BIN="" ;     case "$(arch)" in         aarch64)             TINI_BIN='tini-arm64' ;             ;;         x86_64)             TINI_BIN='tini-amd64' ;             ;;         *) echo >&2 "Unsupported architecture $(arch)" ; exit 1 ;;     esac ;   TINI_VERSION='v0.19.0' ;   curl --retry 8 -S -L -O "https://github.com/krallin/tini/releases/download/${TINI_VERSION}/${TINI_BIN}" ;   curl --retry 8 -S -L -O "https://github.com/krallin/tini/releases/download/${TINI_VERSION}/${TINI_BIN}.sha256sum" ;   sha256sum -c "${TINI_BIN}.sha256sum" ;   rm "${TINI_BIN}.sha256sum" ;   mv "${TINI_BIN}" /bin/tini ;   chmod +x /bin/tini # buildkit
# Mon, 24 Oct 2022 11:34:29 GMT
RUN mkdir /usr/share/fonts/local # buildkit
# Mon, 24 Oct 2022 11:34:32 GMT
RUN curl --retry 8 -S -L -o /usr/share/fonts/local/NotoSansCJK-Regular.ttc https://github.com/googlefonts/noto-cjk/raw/NotoSansV2.001/NotoSansCJK-Regular.ttc # buildkit
# Mon, 24 Oct 2022 11:34:32 GMT
RUN echo "5dcd1c336cc9344cb77c03a0cd8982ca8a7dc97d620fd6c9c434e02dcb1ceeb3  /usr/share/fonts/local/NotoSansCJK-Regular.ttc" | sha256sum -c - # buildkit
# Mon, 24 Oct 2022 11:34:33 GMT
RUN fc-cache -v # buildkit
# Mon, 24 Oct 2022 11:35:35 GMT
COPY /usr/share/kibana /usr/share/kibana # buildkit
# Mon, 24 Oct 2022 11:35:35 GMT
WORKDIR /usr/share/kibana
# Mon, 24 Oct 2022 11:35:35 GMT
RUN ln -s /usr/share/kibana /opt/kibana # buildkit
# Mon, 24 Oct 2022 11:35:35 GMT
ENV ELASTIC_CONTAINER=true
# Mon, 24 Oct 2022 11:35:35 GMT
ENV PATH=/usr/share/kibana/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 24 Oct 2022 11:35:35 GMT
COPY config/kibana.yml /usr/share/kibana/config/kibana.yml # buildkit
# Mon, 24 Oct 2022 11:35:35 GMT
COPY bin/kibana-docker /usr/local/bin/ # buildkit
# Mon, 24 Oct 2022 11:35:36 GMT
RUN chmod g+ws /usr/share/kibana &&     find /usr/share/kibana -gid 0 -and -not -perm /g+w -exec chmod g+w {} \; # buildkit
# Mon, 24 Oct 2022 11:35:37 GMT
RUN find / -xdev -perm -4000 -exec chmod u-s {} + # buildkit
# Mon, 24 Oct 2022 11:35:38 GMT
RUN groupadd --gid 1000 kibana &&     useradd --uid 1000 --gid 1000 -G 0       --home-dir /usr/share/kibana --no-create-home       kibana # buildkit
# Mon, 24 Oct 2022 11:35:38 GMT
LABEL org.label-schema.build-date=2022-10-24T11:08:22.637Z org.label-schema.license=Elastic License org.label-schema.name=Kibana org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/kibana org.label-schema.usage=https://www.elastic.co/guide/en/kibana/reference/index.html org.label-schema.vcs-ref=3db77af5d7066697635ad3e1eeeae81a92ae9711 org.label-schema.vcs-url=https://github.com/elastic/kibana org.label-schema.vendor=Elastic org.label-schema.version=8.5.0 org.opencontainers.image.created=2022-10-24T11:08:22.637Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/kibana/reference/index.html org.opencontainers.image.licenses=Elastic License org.opencontainers.image.revision=3db77af5d7066697635ad3e1eeeae81a92ae9711 org.opencontainers.image.source=https://github.com/elastic/kibana org.opencontainers.image.title=Kibana org.opencontainers.image.url=https://www.elastic.co/products/kibana org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=8.5.0
# Mon, 24 Oct 2022 11:35:38 GMT
ENTRYPOINT ["/bin/tini" "--"]
# Mon, 24 Oct 2022 11:35:38 GMT
CMD ["/usr/local/bin/kibana-docker"]
# Mon, 24 Oct 2022 11:35:38 GMT
USER kibana
```

-	Layers:
	-	`sha256:514fa78e57ce0d9437bc984cc36ab780c24b69da2b922bfff16737072e3e7de2`  
		Last Modified: Wed, 05 Oct 2022 00:03:51 GMT  
		Size: 27.2 MB (27191622 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a0761ae43fae56061f5010f748c8ace957df5871c70a8dea2349fe55267f221`  
		Last Modified: Wed, 02 Nov 2022 18:40:57 GMT  
		Size: 12.9 MB (12876981 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:215a1d718b48b00dffddf804d5fd7d0fc96ff0ae6d16fe7b5917fba856173c32`  
		Last Modified: Wed, 02 Nov 2022 18:40:54 GMT  
		Size: 9.1 KB (9100 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43cb23d8d0cafd23550b66f14a1650619c036ec181b9e5f4fc1aebd9153ada8a`  
		Last Modified: Wed, 02 Nov 2022 18:40:54 GMT  
		Size: 161.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2bf37fb90f2e70674c04a7a8e1d16f4f039aacd6bcfe2c6d171ec2ead54e6bfa`  
		Last Modified: Wed, 02 Nov 2022 18:40:52 GMT  
		Size: 16.5 MB (16460495 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0af7518ba766eb1b56b50891b664020e91a3f950f07ce3a81b647825ec981790`  
		Last Modified: Wed, 02 Nov 2022 18:40:51 GMT  
		Size: 5.3 KB (5298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10e26bb572d5c3b9afc12f7c5c67136f652ee76e50dc51bf3f5864a9ffe1325b`  
		Last Modified: Wed, 02 Nov 2022 18:41:16 GMT  
		Size: 243.5 MB (243524231 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53cfb316e3576e22053a5e2e7f768161b1c87ef5b7c24c678a162d7c80c487f8`  
		Last Modified: Wed, 02 Nov 2022 18:40:51 GMT  
		Size: 132.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b27e75f0814744ad49525a8344092c2b5fd3bc987d0d0138400e8591169975fd`  
		Last Modified: Wed, 02 Nov 2022 18:40:48 GMT  
		Size: 397.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e88ea2c9f16d87ec9289f3780b0ea2ce3949fee41bfe075b91b62ff8b3ca8b3`  
		Last Modified: Wed, 02 Nov 2022 18:40:48 GMT  
		Size: 4.4 KB (4415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53b4681630a65df93833e01976b4ac1fc1e0fca518e435e6927adfecb7605332`  
		Last Modified: Wed, 02 Nov 2022 18:40:48 GMT  
		Size: 399.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:678ff514e03f6809bb055d2f12431b56d68ffc4eceaca81928c43d6f5362d871`  
		Last Modified: Wed, 02 Nov 2022 18:40:49 GMT  
		Size: 183.4 KB (183395 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e95049911f22cd595ace9ba9360063943f1ef7bd7d7e9c893662a48a4effdc18`  
		Last Modified: Wed, 02 Nov 2022 18:40:54 GMT  
		Size: 1.8 KB (1822 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
