<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `kibana`

-	[`kibana:7.17.7`](#kibana7177)
-	[`kibana:8.5.2`](#kibana852)

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

## `kibana:8.5.2`

```console
$ docker pull kibana@sha256:7a5a0a6de4662eecc33c42a15dd8efc2515aa845e3e8124c63086b1a8bd15116
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `kibana:8.5.2` - linux; amd64

```console
$ docker pull kibana@sha256:8d98aba128c42e5eaa503b4c5b81ae6ec74dcae5d886d9cd871e7a464a284d4b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **283.0 MB (282986851 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8bec3366fd9ab0c2a43a374fa895a27f002c47377fb32aad532975cc490cd80b`
-	Entrypoint: `["\/bin\/tini","--"]`
-	Default Command: `["\/usr\/local\/bin\/kibana-docker"]`

```dockerfile
# Tue, 25 Oct 2022 01:53:34 GMT
ADD file:7633003155a1059419aa1a6756fafb6e4f419d65bff7feb7c945de1e29dccb1e in / 
# Tue, 25 Oct 2022 01:53:35 GMT
CMD ["bash"]
# Wed, 16 Nov 2022 21:05:40 GMT
EXPOSE map[5601/tcp:{}]
# Wed, 16 Nov 2022 21:05:40 GMT
RUN for iter in {1..10}; do       export DEBIAN_FRONTEND=noninteractive &&       apt-get update  &&       apt-get upgrade -y  &&       apt-get install -y --no-install-recommends        fontconfig fonts-liberation libnss3 libfontconfig1 ca-certificates curl &&       apt-get clean &&       rm -rf /var/lib/apt/lists/* && exit_code=0 && break || exit_code=$? && echo "apt-get error: retry $iter in 10s" &&       sleep 10;     done;     (exit $exit_code) # buildkit
# Wed, 16 Nov 2022 21:05:41 GMT
RUN set -e ;     TINI_BIN="" ;     case "$(arch)" in         aarch64)             TINI_BIN='tini-arm64' ;             ;;         x86_64)             TINI_BIN='tini-amd64' ;             ;;         *) echo >&2 "Unsupported architecture $(arch)" ; exit 1 ;;     esac ;   TINI_VERSION='v0.19.0' ;   curl --retry 8 -S -L -O "https://github.com/krallin/tini/releases/download/${TINI_VERSION}/${TINI_BIN}" ;   curl --retry 8 -S -L -O "https://github.com/krallin/tini/releases/download/${TINI_VERSION}/${TINI_BIN}.sha256sum" ;   sha256sum -c "${TINI_BIN}.sha256sum" ;   rm "${TINI_BIN}.sha256sum" ;   mv "${TINI_BIN}" /bin/tini ;   chmod +x /bin/tini # buildkit
# Wed, 16 Nov 2022 21:05:42 GMT
RUN mkdir /usr/share/fonts/local # buildkit
# Wed, 16 Nov 2022 21:05:42 GMT
RUN curl --retry 8 -S -L -o /usr/share/fonts/local/NotoSansCJK-Regular.ttc https://github.com/googlefonts/noto-cjk/raw/NotoSansV2.001/NotoSansCJK-Regular.ttc # buildkit
# Wed, 16 Nov 2022 21:05:43 GMT
RUN echo "5dcd1c336cc9344cb77c03a0cd8982ca8a7dc97d620fd6c9c434e02dcb1ceeb3  /usr/share/fonts/local/NotoSansCJK-Regular.ttc" | sha256sum -c - # buildkit
# Wed, 16 Nov 2022 21:05:43 GMT
RUN fc-cache -v # buildkit
# Wed, 16 Nov 2022 21:06:44 GMT
COPY /usr/share/kibana /usr/share/kibana # buildkit
# Wed, 16 Nov 2022 21:06:44 GMT
WORKDIR /usr/share/kibana
# Wed, 16 Nov 2022 21:06:44 GMT
RUN ln -s /usr/share/kibana /opt/kibana # buildkit
# Wed, 16 Nov 2022 21:06:44 GMT
ENV ELASTIC_CONTAINER=true
# Wed, 16 Nov 2022 21:06:44 GMT
ENV PATH=/usr/share/kibana/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 16 Nov 2022 21:06:44 GMT
COPY config/kibana.yml /usr/share/kibana/config/kibana.yml # buildkit
# Wed, 16 Nov 2022 21:06:44 GMT
COPY bin/kibana-docker /usr/local/bin/ # buildkit
# Wed, 16 Nov 2022 21:06:45 GMT
RUN chmod g+ws /usr/share/kibana &&     find /usr/share/kibana -gid 0 -and -not -perm /g+w -exec chmod g+w {} \; # buildkit
# Wed, 16 Nov 2022 21:06:45 GMT
RUN find / -xdev -perm -4000 -exec chmod u-s {} + # buildkit
# Wed, 16 Nov 2022 21:06:46 GMT
RUN groupadd --gid 1000 kibana &&     useradd --uid 1000 --gid 1000 -G 0       --home-dir /usr/share/kibana --no-create-home       kibana # buildkit
# Wed, 16 Nov 2022 21:06:46 GMT
LABEL org.label-schema.build-date=2022-11-16T20:43:16.419Z org.label-schema.license=Elastic License org.label-schema.name=Kibana org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/kibana org.label-schema.usage=https://www.elastic.co/guide/en/kibana/reference/index.html org.label-schema.vcs-ref=d08bc2fc2c62274c16732ca0621964747cc961b8 org.label-schema.vcs-url=https://github.com/elastic/kibana org.label-schema.vendor=Elastic org.label-schema.version=8.5.2 org.opencontainers.image.created=2022-11-16T20:43:16.419Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/kibana/reference/index.html org.opencontainers.image.licenses=Elastic License org.opencontainers.image.revision=d08bc2fc2c62274c16732ca0621964747cc961b8 org.opencontainers.image.source=https://github.com/elastic/kibana org.opencontainers.image.title=Kibana org.opencontainers.image.url=https://www.elastic.co/products/kibana org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=8.5.2
# Wed, 16 Nov 2022 21:06:46 GMT
ENTRYPOINT ["/bin/tini" "--"]
# Wed, 16 Nov 2022 21:06:46 GMT
CMD ["/usr/local/bin/kibana-docker"]
# Wed, 16 Nov 2022 21:06:46 GMT
USER kibana
```

-	Layers:
	-	`sha256:eaead16dc43bb8811d4ff450935d607f9ba4baffda4fc110cc402fa43f601d83`  
		Last Modified: Fri, 21 Oct 2022 03:03:39 GMT  
		Size: 28.6 MB (28577834 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:158eb79de4ce112163962764b13d68d30593d54809df34f2dc8870bf0697ff77`  
		Last Modified: Thu, 24 Nov 2022 09:39:06 GMT  
		Size: 10.5 MB (10514275 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21713b2945409adf0d6077d5d29e84e463458c7faa5f222f02542379d46b6e71`  
		Last Modified: Thu, 24 Nov 2022 09:39:04 GMT  
		Size: 9.5 KB (9525 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a754d38e796a64f2fe59d6659b76a305ad041c7d18e76d34ecf4f082683c0c3a`  
		Last Modified: Thu, 24 Nov 2022 09:39:02 GMT  
		Size: 158.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45dcaf2f63e96cb1474d780c7e67c907a1cbf82c3ba8e5f887b450140c1cf435`  
		Last Modified: Thu, 24 Nov 2022 09:39:03 GMT  
		Size: 16.5 MB (16460498 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2400270f20e1690fc38fa600390efe92cb99257dcd42520c111ad2e0fa8acc1`  
		Last Modified: Thu, 24 Nov 2022 09:39:01 GMT  
		Size: 5.3 KB (5287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2328e87e33afeab31bf8aa3d3aac96b87c1de0dde78567d75c27205452fc949e`  
		Last Modified: Thu, 24 Nov 2022 09:39:35 GMT  
		Size: 227.2 MB (227222651 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86c8b13c0b89c941a3d6a9891614ebcec6ea704fa1290f607bd5c62c0a510f37`  
		Last Modified: Thu, 24 Nov 2022 09:39:01 GMT  
		Size: 133.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf4693470dce6c0e09cb6a82a18ba37dfe46694c08f9bacbf6e3d13d3911d388`  
		Last Modified: Thu, 24 Nov 2022 09:38:59 GMT  
		Size: 397.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74556fb7cb6fd3ecadb07d35147c91e329461ca4d1370a67838f018ecf3702da`  
		Last Modified: Thu, 24 Nov 2022 09:38:59 GMT  
		Size: 4.4 KB (4420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7540ead99c3b91e487eeca0909dda365687ef9b50e3f39c21e3ca9c08d7ff480`  
		Last Modified: Thu, 24 Nov 2022 09:38:59 GMT  
		Size: 399.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce82ccfdf2827db92fdb826f4f1815bd8064ec12ca8d94ad97ce2fb562d8a2aa`  
		Last Modified: Thu, 24 Nov 2022 09:38:59 GMT  
		Size: 189.4 KB (189388 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67495baab3b9fc4a86f74ec22020e245bf4c011bebb259bfa22e42f30f876af2`  
		Last Modified: Thu, 24 Nov 2022 09:38:59 GMT  
		Size: 1.8 KB (1822 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kibana:8.5.2` - linux; arm64 variant v8

```console
$ docker pull kibana@sha256:c21cfe6acfedca009d40b7d8bb6fcf5ffcff458cd11c27a94374436867769b00
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **297.9 MB (297877511 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d2cef2959aac93f2a74c763db2e762c222fa0f95276d1f3664fb738011a70288`
-	Entrypoint: `["\/bin\/tini","--"]`
-	Default Command: `["\/usr\/local\/bin\/kibana-docker"]`

```dockerfile
# Tue, 25 Oct 2022 05:54:59 GMT
ADD file:6784d0c4432f4f32d6ee4d96eedf33ea82d88ef6901c763665fa77c842621999 in / 
# Tue, 25 Oct 2022 05:54:59 GMT
CMD ["bash"]
# Wed, 16 Nov 2022 21:08:40 GMT
EXPOSE map[5601/tcp:{}]
# Wed, 16 Nov 2022 21:08:40 GMT
RUN for iter in {1..10}; do       export DEBIAN_FRONTEND=noninteractive &&       apt-get update  &&       apt-get upgrade -y  &&       apt-get install -y --no-install-recommends        fontconfig fonts-liberation libnss3 libfontconfig1 ca-certificates curl &&       apt-get clean &&       rm -rf /var/lib/apt/lists/* && exit_code=0 && break || exit_code=$? && echo "apt-get error: retry $iter in 10s" &&       sleep 10;     done;     (exit $exit_code) # buildkit
# Wed, 16 Nov 2022 21:08:42 GMT
RUN set -e ;     TINI_BIN="" ;     case "$(arch)" in         aarch64)             TINI_BIN='tini-arm64' ;             ;;         x86_64)             TINI_BIN='tini-amd64' ;             ;;         *) echo >&2 "Unsupported architecture $(arch)" ; exit 1 ;;     esac ;   TINI_VERSION='v0.19.0' ;   curl --retry 8 -S -L -O "https://github.com/krallin/tini/releases/download/${TINI_VERSION}/${TINI_BIN}" ;   curl --retry 8 -S -L -O "https://github.com/krallin/tini/releases/download/${TINI_VERSION}/${TINI_BIN}.sha256sum" ;   sha256sum -c "${TINI_BIN}.sha256sum" ;   rm "${TINI_BIN}.sha256sum" ;   mv "${TINI_BIN}" /bin/tini ;   chmod +x /bin/tini # buildkit
# Wed, 16 Nov 2022 21:08:42 GMT
RUN mkdir /usr/share/fonts/local # buildkit
# Wed, 16 Nov 2022 21:08:45 GMT
RUN curl --retry 8 -S -L -o /usr/share/fonts/local/NotoSansCJK-Regular.ttc https://github.com/googlefonts/noto-cjk/raw/NotoSansV2.001/NotoSansCJK-Regular.ttc # buildkit
# Wed, 16 Nov 2022 21:08:45 GMT
RUN echo "5dcd1c336cc9344cb77c03a0cd8982ca8a7dc97d620fd6c9c434e02dcb1ceeb3  /usr/share/fonts/local/NotoSansCJK-Regular.ttc" | sha256sum -c - # buildkit
# Wed, 16 Nov 2022 21:08:46 GMT
RUN fc-cache -v # buildkit
# Wed, 16 Nov 2022 21:09:43 GMT
COPY /usr/share/kibana /usr/share/kibana # buildkit
# Wed, 16 Nov 2022 21:09:43 GMT
WORKDIR /usr/share/kibana
# Wed, 16 Nov 2022 21:09:43 GMT
RUN ln -s /usr/share/kibana /opt/kibana # buildkit
# Wed, 16 Nov 2022 21:09:43 GMT
ENV ELASTIC_CONTAINER=true
# Wed, 16 Nov 2022 21:09:43 GMT
ENV PATH=/usr/share/kibana/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 16 Nov 2022 21:09:43 GMT
COPY config/kibana.yml /usr/share/kibana/config/kibana.yml # buildkit
# Wed, 16 Nov 2022 21:09:43 GMT
COPY bin/kibana-docker /usr/local/bin/ # buildkit
# Wed, 16 Nov 2022 21:09:44 GMT
RUN chmod g+ws /usr/share/kibana &&     find /usr/share/kibana -gid 0 -and -not -perm /g+w -exec chmod g+w {} \; # buildkit
# Wed, 16 Nov 2022 21:09:45 GMT
RUN find / -xdev -perm -4000 -exec chmod u-s {} + # buildkit
# Wed, 16 Nov 2022 21:09:45 GMT
RUN groupadd --gid 1000 kibana &&     useradd --uid 1000 --gid 1000 -G 0       --home-dir /usr/share/kibana --no-create-home       kibana # buildkit
# Wed, 16 Nov 2022 21:09:45 GMT
LABEL org.label-schema.build-date=2022-11-16T20:43:16.419Z org.label-schema.license=Elastic License org.label-schema.name=Kibana org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/kibana org.label-schema.usage=https://www.elastic.co/guide/en/kibana/reference/index.html org.label-schema.vcs-ref=d08bc2fc2c62274c16732ca0621964747cc961b8 org.label-schema.vcs-url=https://github.com/elastic/kibana org.label-schema.vendor=Elastic org.label-schema.version=8.5.2 org.opencontainers.image.created=2022-11-16T20:43:16.419Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/kibana/reference/index.html org.opencontainers.image.licenses=Elastic License org.opencontainers.image.revision=d08bc2fc2c62274c16732ca0621964747cc961b8 org.opencontainers.image.source=https://github.com/elastic/kibana org.opencontainers.image.title=Kibana org.opencontainers.image.url=https://www.elastic.co/products/kibana org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=8.5.2
# Wed, 16 Nov 2022 21:09:45 GMT
ENTRYPOINT ["/bin/tini" "--"]
# Wed, 16 Nov 2022 21:09:45 GMT
CMD ["/usr/local/bin/kibana-docker"]
# Wed, 16 Nov 2022 21:09:45 GMT
USER kibana
```

-	Layers:
	-	`sha256:4e7e0215f4adc2c48ad9cb3b3781e21d474b477587f85682c2e2975ae91dce9d`  
		Last Modified: Tue, 25 Oct 2022 05:55:59 GMT  
		Size: 27.2 MB (27195998 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb3fecb53e953030bf9a24c619bcfbe8f414790e46eb4d64c78eeca71732bb1c`  
		Last Modified: Tue, 29 Nov 2022 01:51:27 GMT  
		Size: 10.4 MB (10382915 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90dbd99d24102f5e6265ac2ba61ef3cbcfe78e72875397b32039c7dcb20e5e45`  
		Last Modified: Tue, 29 Nov 2022 01:51:25 GMT  
		Size: 9.1 KB (9100 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba94ca2e731e4f0d99c98af65575f914fb649470a99e2086e3e9452c873f035f`  
		Last Modified: Tue, 29 Nov 2022 01:51:25 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18a36579ed5b6a61ed23b4120d5b62cc338e9f6008c02d5cf1e4212fac14f191`  
		Last Modified: Tue, 29 Nov 2022 01:51:24 GMT  
		Size: 16.5 MB (16460486 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45a69af64c65b82ea574d11387c37bbf95a6748ee482cc34356f8eba02d69c33`  
		Last Modified: Tue, 29 Nov 2022 01:51:23 GMT  
		Size: 5.3 KB (5293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48933d44360786180f1e7ae630edf58900f21701b17509009979d185885c3938`  
		Last Modified: Tue, 29 Nov 2022 01:51:47 GMT  
		Size: 243.6 MB (243632929 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94a88be571d6ef200c136325902ccad6511fc9af28a9d707d53bcd58b111101d`  
		Last Modified: Tue, 29 Nov 2022 01:51:22 GMT  
		Size: 133.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79fc295c9391b4c3429075773ee9d2ab6e8d5fb718167250c802aa8cdc7a556e`  
		Last Modified: Tue, 29 Nov 2022 01:51:20 GMT  
		Size: 396.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:948eb727f6076224ac4205c10b92702c599cba9fc2900086bb479a11369c8d01`  
		Last Modified: Tue, 29 Nov 2022 01:51:20 GMT  
		Size: 4.4 KB (4418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd9be858692c973d6bcc171928f893cb04983251c56a6d121415d853e0201593`  
		Last Modified: Tue, 29 Nov 2022 01:51:20 GMT  
		Size: 399.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28526544ceaecd2d0906cfeabeab199d59e205eee98ca78b9f37967966ba006b`  
		Last Modified: Tue, 29 Nov 2022 01:51:20 GMT  
		Size: 183.4 KB (183395 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f8606779aaec3f36302c9788d51e9ebd128181dd21dd4691b712b8a1eaf7716`  
		Last Modified: Tue, 29 Nov 2022 01:51:25 GMT  
		Size: 1.8 KB (1825 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
