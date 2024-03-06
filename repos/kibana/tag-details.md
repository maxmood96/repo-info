<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `kibana`

-	[`kibana:7.17.18`](#kibana71718)
-	[`kibana:8.12.2`](#kibana8122)

## `kibana:7.17.18`

```console
$ docker pull kibana@sha256:1e5ed987f8177f5f93c2550f698d47c6fb4a5e2ba90c54ebe6029772efd0369c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `kibana:7.17.18` - linux; amd64

```console
$ docker pull kibana@sha256:37c195ea6bf71dd13b8a5f6f3f357013609a8db8662c5957ec8272a80ba622cb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **358.4 MB (358403696 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:117cbfb16aaa22dab5fac8b444f0767fa24cd77c29a58e75c330599debe34b89`
-	Entrypoint: `["\/bin\/tini","--"]`
-	Default Command: `["\/usr\/local\/bin\/kibana-docker"]`

```dockerfile
# Tue, 06 Feb 2024 11:29:54 GMT
ARG RELEASE
# Tue, 06 Feb 2024 11:29:54 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 06 Feb 2024 11:29:54 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 06 Feb 2024 11:29:54 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 06 Feb 2024 11:29:54 GMT
ADD file:a25798f31219000d6a82d2c9258743926b1a400530d12dbb1eadf2c2519f9888 in / 
# Tue, 06 Feb 2024 11:29:54 GMT
CMD ["/bin/bash"]
# Tue, 06 Feb 2024 11:29:54 GMT
EXPOSE map[5601/tcp:{}]
# Tue, 06 Feb 2024 11:29:54 GMT
RUN for iter in {1..10}; do       export DEBIAN_FRONTEND=noninteractive &&       apt-get update  &&       apt-get upgrade -y  &&       apt-get install -y --no-install-recommends        fontconfig fonts-liberation libnss3 libfontconfig1 ca-certificates curl &&       apt-get clean &&       rm -rf /var/lib/apt/lists/* && exit_code=0 && break || exit_code=$? && echo "apt-get error: retry $iter in 10s" &&       sleep 10;     done;     (exit $exit_code) # buildkit
# Tue, 06 Feb 2024 11:29:54 GMT
RUN set -e ;     TINI_BIN="" ;     case "$(arch)" in         aarch64)             TINI_BIN='tini-arm64' ;             ;;         x86_64)             TINI_BIN='tini-amd64' ;             ;;         *) echo >&2 "Unsupported architecture $(arch)" ; exit 1 ;;     esac ;   TINI_VERSION='v0.19.0' ;   curl --retry 8 -S -L -O "https://github.com/krallin/tini/releases/download/${TINI_VERSION}/${TINI_BIN}" ;   curl --retry 8 -S -L -O "https://github.com/krallin/tini/releases/download/${TINI_VERSION}/${TINI_BIN}.sha256sum" ;   sha256sum -c "${TINI_BIN}.sha256sum" ;   rm "${TINI_BIN}.sha256sum" ;   mv "${TINI_BIN}" /bin/tini ;   chmod +x /bin/tini # buildkit
# Tue, 06 Feb 2024 11:29:54 GMT
RUN mkdir /usr/share/fonts/local # buildkit
# Tue, 06 Feb 2024 11:29:54 GMT
RUN curl --retry 8 -S -L -o /usr/share/fonts/local/NotoSansCJK-Regular.ttc https://github.com/googlefonts/noto-cjk/raw/NotoSansV2.001/NotoSansCJK-Regular.ttc # buildkit
# Tue, 06 Feb 2024 11:29:54 GMT
RUN echo "5dcd1c336cc9344cb77c03a0cd8982ca8a7dc97d620fd6c9c434e02dcb1ceeb3  /usr/share/fonts/local/NotoSansCJK-Regular.ttc" | sha256sum -c - # buildkit
# Tue, 06 Feb 2024 11:29:54 GMT
RUN fc-cache -v # buildkit
# Tue, 06 Feb 2024 11:29:54 GMT
COPY /usr/share/kibana /usr/share/kibana # buildkit
# Tue, 06 Feb 2024 11:29:54 GMT
WORKDIR /usr/share/kibana
# Tue, 06 Feb 2024 11:29:54 GMT
RUN ln -s /usr/share/kibana /opt/kibana # buildkit
# Tue, 06 Feb 2024 11:29:54 GMT
ENV ELASTIC_CONTAINER=true
# Tue, 06 Feb 2024 11:29:54 GMT
ENV PATH=/usr/share/kibana/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 06 Feb 2024 11:29:54 GMT
COPY config/kibana.yml /usr/share/kibana/config/kibana.yml # buildkit
# Tue, 06 Feb 2024 11:29:54 GMT
COPY bin/kibana-docker /usr/local/bin/ # buildkit
# Tue, 06 Feb 2024 11:29:54 GMT
RUN chmod g+ws /usr/share/kibana &&     find /usr/share/kibana -gid 0 -and -not -perm /g+w -exec chmod g+w {} \; # buildkit
# Tue, 06 Feb 2024 11:29:54 GMT
RUN find / -xdev -perm -4000 -exec chmod u-s {} + # buildkit
# Tue, 06 Feb 2024 11:29:54 GMT
RUN groupadd --gid 1000 kibana &&     useradd --uid 1000 --gid 1000 -G 0       --home-dir /usr/share/kibana --no-create-home       kibana # buildkit
# Tue, 06 Feb 2024 11:29:54 GMT
LABEL org.label-schema.build-date=2024-02-01T12:06:00.919Z org.label-schema.license=Elastic License org.label-schema.name=Kibana org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/kibana org.label-schema.usage=https://www.elastic.co/guide/en/kibana/reference/index.html org.label-schema.vcs-ref=d9651872f4b223d9f91a873f1d6a9fb7d1fe4f64 org.label-schema.vcs-url=https://github.com/elastic/kibana org.label-schema.vendor=Elastic org.label-schema.version=7.17.18 org.opencontainers.image.created=2024-02-01T12:06:00.919Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/kibana/reference/index.html org.opencontainers.image.licenses=Elastic License org.opencontainers.image.revision=d9651872f4b223d9f91a873f1d6a9fb7d1fe4f64 org.opencontainers.image.source=https://github.com/elastic/kibana org.opencontainers.image.title=Kibana org.opencontainers.image.url=https://www.elastic.co/products/kibana org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=7.17.18
# Tue, 06 Feb 2024 11:29:54 GMT
ENTRYPOINT ["/bin/tini" "--"]
# Tue, 06 Feb 2024 11:29:54 GMT
CMD ["/usr/local/bin/kibana-docker"]
# Tue, 06 Feb 2024 11:29:54 GMT
USER kibana
```

-	Layers:
	-	`sha256:17d0386c2fff30a5b92652bbef2b84639dba9b9f17bdbb819c8d10badd827fdb`  
		Last Modified: Fri, 16 Feb 2024 21:40:52 GMT  
		Size: 27.5 MB (27514312 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:274275be56c8620838ffc8f35002c13bdfee9b48b932c90eb06e5fdf659cb340`  
		Last Modified: Wed, 06 Mar 2024 02:57:32 GMT  
		Size: 10.5 MB (10533200 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14492576505b4e19d13ab7a72609656b8ba747ef6a304e52f39a55985df2404b`  
		Last Modified: Wed, 06 Mar 2024 02:57:31 GMT  
		Size: 9.5 KB (9526 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c52bbd06d19570b0afedd97625f5f674450862a7a101f2ce85764a6588ea291f`  
		Last Modified: Wed, 06 Mar 2024 02:57:31 GMT  
		Size: 160.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff5e8f83515f25eb9f27eafed771ea9e9aa9f4603e43ec1621059a8b699d4000`  
		Last Modified: Wed, 06 Mar 2024 02:57:32 GMT  
		Size: 16.5 MB (16460490 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af53a86481ab48769096eb90a115d8051db116d5597732b050b05631fa559db3`  
		Last Modified: Wed, 06 Mar 2024 02:57:32 GMT  
		Size: 5.3 KB (5289 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00c0dfffbb884bf3f894d24661a0f4ebd57607a35530dda6440f844fa89e732d`  
		Last Modified: Wed, 06 Mar 2024 02:57:39 GMT  
		Size: 303.7 MB (303683987 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11da4c54b9c23585cff2562a8544c81565b9fa5ea61e21615f5a42686f2045ad`  
		Last Modified: Wed, 06 Mar 2024 02:57:33 GMT  
		Size: 130.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72e8dd7e28c6424bfee88ac80c5a6e49a65bc2de143b6c2a8ad53bb11729e925`  
		Last Modified: Wed, 06 Mar 2024 02:57:33 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb5c83abeca39dab1de1b9e0c4a01ade92f74792b0bc5cbfb6ba439689a5e4da`  
		Last Modified: Wed, 06 Mar 2024 02:57:33 GMT  
		Size: 4.5 KB (4506 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06ad99e14e5c9f1214071dfe43cada7082412f3abb52a00bda2cf1c4cddb68fd`  
		Last Modified: Wed, 06 Mar 2024 02:57:34 GMT  
		Size: 401.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eba2986f5116e2926b4873f41f60eeb67e6cdaf811c877fb58c9d5dbf34e30fc`  
		Last Modified: Wed, 06 Mar 2024 02:57:34 GMT  
		Size: 189.4 KB (189432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8a8e7c16fa4f9a0bb8ce333629abafe49d33640aa6ee440719608c22fe530d0`  
		Last Modified: Wed, 06 Mar 2024 02:57:34 GMT  
		Size: 1.8 KB (1801 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kibana:7.17.18` - unknown; unknown

```console
$ docker pull kibana@sha256:8f9292ad2f11d582048779a9647278b1edf7bac89243fd007b548d472a2831c8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2219584 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1271ff77574d43c92544e61ba1eeed1a6ee7c4e9a303e83f969a660a73c734d0`

```dockerfile
```

-	Layers:
	-	`sha256:63bc80312c4f530f38b19defd5c410f4d1810ec2d7ce7ceb682a60858add43b2`  
		Last Modified: Wed, 06 Mar 2024 02:57:31 GMT  
		Size: 2.2 MB (2175222 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ad2d181cb1a0fcba0922aa44cf3ec6ed46f42bd5786ccafa75d0b5117b978816`  
		Last Modified: Wed, 06 Mar 2024 02:57:31 GMT  
		Size: 44.4 KB (44362 bytes)  
		MIME: application/vnd.in-toto+json

### `kibana:7.17.18` - linux; arm64 variant v8

```console
$ docker pull kibana@sha256:6ced7aea205b32d44281e28c6b4f396974ecb9017fdb1b31f5b5cf497364fa01
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **368.9 MB (368863724 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9904cc2b183f780df6f777928d2098244f9e416b6260d354e452ce53498a1fdb`
-	Entrypoint: `["\/bin\/tini","--"]`
-	Default Command: `["\/usr\/local\/bin\/kibana-docker"]`

```dockerfile
# Tue, 06 Feb 2024 11:29:54 GMT
ARG RELEASE
# Tue, 06 Feb 2024 11:29:54 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 06 Feb 2024 11:29:54 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 06 Feb 2024 11:29:54 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 06 Feb 2024 11:29:54 GMT
ADD file:a8303c80b47ec165c276111aa6f98ee877e4da60ddafa00b7547032a3de7935d in / 
# Tue, 06 Feb 2024 11:29:54 GMT
CMD ["/bin/bash"]
# Tue, 06 Feb 2024 11:29:54 GMT
EXPOSE map[5601/tcp:{}]
# Tue, 06 Feb 2024 11:29:54 GMT
RUN for iter in {1..10}; do       export DEBIAN_FRONTEND=noninteractive &&       apt-get update  &&       apt-get upgrade -y  &&       apt-get install -y --no-install-recommends        fontconfig fonts-liberation libnss3 libfontconfig1 ca-certificates curl &&       apt-get clean &&       rm -rf /var/lib/apt/lists/* && exit_code=0 && break || exit_code=$? && echo "apt-get error: retry $iter in 10s" &&       sleep 10;     done;     (exit $exit_code) # buildkit
# Tue, 06 Feb 2024 11:29:54 GMT
RUN set -e ;     TINI_BIN="" ;     case "$(arch)" in         aarch64)             TINI_BIN='tini-arm64' ;             ;;         x86_64)             TINI_BIN='tini-amd64' ;             ;;         *) echo >&2 "Unsupported architecture $(arch)" ; exit 1 ;;     esac ;   TINI_VERSION='v0.19.0' ;   curl --retry 8 -S -L -O "https://github.com/krallin/tini/releases/download/${TINI_VERSION}/${TINI_BIN}" ;   curl --retry 8 -S -L -O "https://github.com/krallin/tini/releases/download/${TINI_VERSION}/${TINI_BIN}.sha256sum" ;   sha256sum -c "${TINI_BIN}.sha256sum" ;   rm "${TINI_BIN}.sha256sum" ;   mv "${TINI_BIN}" /bin/tini ;   chmod +x /bin/tini # buildkit
# Tue, 06 Feb 2024 11:29:54 GMT
RUN mkdir /usr/share/fonts/local # buildkit
# Tue, 06 Feb 2024 11:29:54 GMT
RUN curl --retry 8 -S -L -o /usr/share/fonts/local/NotoSansCJK-Regular.ttc https://github.com/googlefonts/noto-cjk/raw/NotoSansV2.001/NotoSansCJK-Regular.ttc # buildkit
# Tue, 06 Feb 2024 11:29:54 GMT
RUN echo "5dcd1c336cc9344cb77c03a0cd8982ca8a7dc97d620fd6c9c434e02dcb1ceeb3  /usr/share/fonts/local/NotoSansCJK-Regular.ttc" | sha256sum -c - # buildkit
# Tue, 06 Feb 2024 11:29:54 GMT
RUN fc-cache -v # buildkit
# Tue, 06 Feb 2024 11:29:54 GMT
COPY /usr/share/kibana /usr/share/kibana # buildkit
# Tue, 06 Feb 2024 11:29:54 GMT
WORKDIR /usr/share/kibana
# Tue, 06 Feb 2024 11:29:54 GMT
RUN ln -s /usr/share/kibana /opt/kibana # buildkit
# Tue, 06 Feb 2024 11:29:54 GMT
ENV ELASTIC_CONTAINER=true
# Tue, 06 Feb 2024 11:29:54 GMT
ENV PATH=/usr/share/kibana/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 06 Feb 2024 11:29:54 GMT
COPY config/kibana.yml /usr/share/kibana/config/kibana.yml # buildkit
# Tue, 06 Feb 2024 11:29:54 GMT
COPY bin/kibana-docker /usr/local/bin/ # buildkit
# Tue, 06 Feb 2024 11:29:54 GMT
RUN chmod g+ws /usr/share/kibana &&     find /usr/share/kibana -gid 0 -and -not -perm /g+w -exec chmod g+w {} \; # buildkit
# Tue, 06 Feb 2024 11:29:54 GMT
RUN find / -xdev -perm -4000 -exec chmod u-s {} + # buildkit
# Tue, 06 Feb 2024 11:29:54 GMT
RUN groupadd --gid 1000 kibana &&     useradd --uid 1000 --gid 1000 -G 0       --home-dir /usr/share/kibana --no-create-home       kibana # buildkit
# Tue, 06 Feb 2024 11:29:54 GMT
LABEL org.label-schema.build-date=2024-02-01T12:06:00.919Z org.label-schema.license=Elastic License org.label-schema.name=Kibana org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/kibana org.label-schema.usage=https://www.elastic.co/guide/en/kibana/reference/index.html org.label-schema.vcs-ref=d9651872f4b223d9f91a873f1d6a9fb7d1fe4f64 org.label-schema.vcs-url=https://github.com/elastic/kibana org.label-schema.vendor=Elastic org.label-schema.version=7.17.18 org.opencontainers.image.created=2024-02-01T12:06:00.919Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/kibana/reference/index.html org.opencontainers.image.licenses=Elastic License org.opencontainers.image.revision=d9651872f4b223d9f91a873f1d6a9fb7d1fe4f64 org.opencontainers.image.source=https://github.com/elastic/kibana org.opencontainers.image.title=Kibana org.opencontainers.image.url=https://www.elastic.co/products/kibana org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=7.17.18
# Tue, 06 Feb 2024 11:29:54 GMT
ENTRYPOINT ["/bin/tini" "--"]
# Tue, 06 Feb 2024 11:29:54 GMT
CMD ["/usr/local/bin/kibana-docker"]
# Tue, 06 Feb 2024 11:29:54 GMT
USER kibana
```

-	Layers:
	-	`sha256:6aae4cfdd5a10a8b0554e75c4c14ae38022a0c8f08dc5d769a735c705670cab7`  
		Last Modified: Fri, 16 Feb 2024 21:40:59 GMT  
		Size: 26.0 MB (25974391 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4c9948864bfb49a024b682d75c0e5b52c06c1a9e1e0ff0b6e522a03f8931bbd`  
		Last Modified: Wed, 06 Mar 2024 16:53:13 GMT  
		Size: 10.4 MB (10396688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18077aa4ba170eb38aa241c2039f3adaddb6fcf2b3528eaca8aa6f45d359e413`  
		Last Modified: Wed, 06 Mar 2024 16:53:12 GMT  
		Size: 9.1 KB (9099 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:577482fbe412643d000fb170d0399204515aba9d337a84de336375f26ab1397b`  
		Last Modified: Wed, 06 Mar 2024 16:53:12 GMT  
		Size: 157.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b81a29926d0bcaf2765541922bd0e49fa92c33d01a695fa72f10b51416bcf0d`  
		Last Modified: Wed, 06 Mar 2024 16:53:14 GMT  
		Size: 16.5 MB (16460489 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8b2f2b0683e5afe7cfc41dfe0bd6dedc02aa9320161d116f60565349aed2234`  
		Last Modified: Wed, 06 Mar 2024 16:53:13 GMT  
		Size: 5.3 KB (5298 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aec2f190f5b2822ed3310d30b2aac9f018ee82ddebf515ca1ba607c7ab5852b9`  
		Last Modified: Wed, 06 Mar 2024 16:57:58 GMT  
		Size: 315.8 MB (315826865 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d31183a09547bbc4015432f16fcf96b6450625b231de2bca29634098a752898d`  
		Last Modified: Wed, 06 Mar 2024 16:57:52 GMT  
		Size: 131.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86c28d53ad74c28a03d524c772eb4638118b05e6f2d88234faf814500869b879`  
		Last Modified: Wed, 06 Mar 2024 16:57:52 GMT  
		Size: 401.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17ee4debc851d415dc881d2ce4c83bf78ef700d971cc7d510ec293d5c9d28335`  
		Last Modified: Wed, 06 Mar 2024 16:57:52 GMT  
		Size: 4.5 KB (4508 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68c2cf6adc3a08eacc39528f7f759945970c306cdb8a7ef5583c97bdbb899df8`  
		Last Modified: Wed, 06 Mar 2024 16:57:53 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25b361d64c00b753d5fa17324f32303f6a2d647671d50f17961baad9c7fdb177`  
		Last Modified: Wed, 06 Mar 2024 16:53:16 GMT  
		Size: 183.4 KB (183424 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6bd4b7c52e60c31d52fe2fdd871680d58cf3530ee26e8f462b09bd17fd21179`  
		Last Modified: Wed, 06 Mar 2024 16:57:53 GMT  
		Size: 1.8 KB (1806 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kibana:7.17.18` - unknown; unknown

```console
$ docker pull kibana@sha256:384038e5307977712d66361b7a20d7d3ae4c7364734b3cfeeb2ec40211dd1b82
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2219663 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7681319dc0ac75c4143d9ed5bee983ec112dd83672a3923fc721a444ed8161da`

```dockerfile
```

-	Layers:
	-	`sha256:f40e6a036f64f3f9cd57bcc2bf547da6ea8b250cfc1141a469f445f7723ee935`  
		Last Modified: Wed, 06 Mar 2024 16:57:51 GMT  
		Size: 2.2 MB (2175457 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b901841b3e83151017b4e7c9e71cd8a370eb7e9b355b52188ce66804b489f419`  
		Last Modified: Wed, 06 Mar 2024 16:57:51 GMT  
		Size: 44.2 KB (44206 bytes)  
		MIME: application/vnd.in-toto+json

## `kibana:8.12.2`

```console
$ docker pull kibana@sha256:459e5653a76008b709f3cb3d32e17449ab202321d1fc0e20ac832cd1ec8e2d01
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `kibana:8.12.2` - linux; amd64

```console
$ docker pull kibana@sha256:194055ed8cff37a234e7c891bed680e2cc3f4c38308b80c8e389a7c40374f213
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **371.8 MB (371793100 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c285823994c439ed9cffd5cb8e161f11a0b3628c2915cac805b6a782012ecc6e`
-	Entrypoint: `["\/bin\/tini","--"]`
-	Default Command: `["\/usr\/local\/bin\/kibana-docker"]`

```dockerfile
# Fri, 16 Feb 2024 21:32:49 GMT
ARG RELEASE
# Fri, 16 Feb 2024 21:32:49 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 16 Feb 2024 21:32:49 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 16 Feb 2024 21:32:49 GMT
LABEL org.opencontainers.image.version=20.04
# Fri, 16 Feb 2024 21:32:52 GMT
ADD file:a25798f31219000d6a82d2c9258743926b1a400530d12dbb1eadf2c2519f9888 in / 
# Fri, 16 Feb 2024 21:32:52 GMT
CMD ["/bin/bash"]
# Thu, 22 Feb 2024 12:50:52 GMT
EXPOSE map[5601/tcp:{}]
# Thu, 22 Feb 2024 12:50:52 GMT
RUN for iter in {1..10}; do       export DEBIAN_FRONTEND=noninteractive &&       apt-get update  &&       apt-get upgrade -y  &&       apt-get install -y --no-install-recommends        fontconfig fonts-liberation libnss3 libfontconfig1 ca-certificates curl &&       apt-get clean &&       rm -rf /var/lib/apt/lists/* && exit_code=0 && break || exit_code=$? && echo "apt-get error: retry $iter in 10s" &&       sleep 10;     done;     (exit $exit_code) # buildkit
# Thu, 22 Feb 2024 12:50:52 GMT
RUN set -e ;     TINI_BIN="" ;     case "$(arch)" in         aarch64)             TINI_BIN='tini-arm64' ;             ;;         x86_64)             TINI_BIN='tini-amd64' ;             ;;         *) echo >&2 "Unsupported architecture $(arch)" ; exit 1 ;;     esac ;   TINI_VERSION='v0.19.0' ;   curl --retry 8 -S -L -O "https://github.com/krallin/tini/releases/download/${TINI_VERSION}/${TINI_BIN}" ;   curl --retry 8 -S -L -O "https://github.com/krallin/tini/releases/download/${TINI_VERSION}/${TINI_BIN}.sha256sum" ;   sha256sum -c "${TINI_BIN}.sha256sum" ;   rm "${TINI_BIN}.sha256sum" ;   mv "${TINI_BIN}" /bin/tini ;   chmod +x /bin/tini # buildkit
# Thu, 22 Feb 2024 12:50:52 GMT
RUN mkdir /usr/share/fonts/local # buildkit
# Thu, 22 Feb 2024 12:50:52 GMT
RUN curl --retry 8 -S -L -o /usr/share/fonts/local/NotoSansCJK-Regular.ttc https://github.com/googlefonts/noto-cjk/raw/NotoSansV2.001/NotoSansCJK-Regular.ttc # buildkit
# Thu, 22 Feb 2024 12:50:52 GMT
RUN echo "5dcd1c336cc9344cb77c03a0cd8982ca8a7dc97d620fd6c9c434e02dcb1ceeb3  /usr/share/fonts/local/NotoSansCJK-Regular.ttc" | sha256sum -c - # buildkit
# Thu, 22 Feb 2024 12:50:52 GMT
RUN fc-cache -v # buildkit
# Thu, 22 Feb 2024 12:50:52 GMT
COPY /usr/share/kibana /usr/share/kibana # buildkit
# Thu, 22 Feb 2024 12:50:52 GMT
WORKDIR /usr/share/kibana
# Thu, 22 Feb 2024 12:50:52 GMT
RUN ln -s /usr/share/kibana /opt/kibana # buildkit
# Thu, 22 Feb 2024 12:50:52 GMT
ENV ELASTIC_CONTAINER=true
# Thu, 22 Feb 2024 12:50:52 GMT
ENV PATH=/usr/share/kibana/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 22 Feb 2024 12:50:52 GMT
COPY config/kibana.yml /usr/share/kibana/config/kibana.yml # buildkit
# Thu, 22 Feb 2024 12:50:52 GMT
COPY bin/kibana-docker /usr/local/bin/ # buildkit
# Thu, 22 Feb 2024 12:50:52 GMT
RUN chmod g+ws /usr/share/kibana &&     find /usr/share/kibana -gid 0 -and -not -perm /g+w -exec chmod g+w {} \; # buildkit
# Thu, 22 Feb 2024 12:50:52 GMT
RUN find / -xdev -perm -4000 -exec chmod u-s {} + # buildkit
# Thu, 22 Feb 2024 12:50:52 GMT
RUN groupadd --gid 1000 kibana &&     useradd --uid 1000 --gid 1000 -G 0       --home-dir /usr/share/kibana --no-create-home       kibana # buildkit
# Thu, 22 Feb 2024 12:50:52 GMT
LABEL org.label-schema.build-date=2024-02-19T12:06:34.117Z org.label-schema.license=Elastic License org.label-schema.name=Kibana org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/kibana org.label-schema.usage=https://www.elastic.co/guide/en/kibana/reference/index.html org.label-schema.vcs-ref=f5bd489c5ff9c676c4f861c42da6ea99ae350832 org.label-schema.vcs-url=https://github.com/elastic/kibana org.label-schema.vendor=Elastic org.label-schema.version=8.12.2 org.opencontainers.image.created=2024-02-19T12:06:34.117Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/kibana/reference/index.html org.opencontainers.image.licenses=Elastic License org.opencontainers.image.revision=f5bd489c5ff9c676c4f861c42da6ea99ae350832 org.opencontainers.image.source=https://github.com/elastic/kibana org.opencontainers.image.title=Kibana org.opencontainers.image.url=https://www.elastic.co/products/kibana org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=8.12.2
# Thu, 22 Feb 2024 12:50:52 GMT
ENTRYPOINT ["/bin/tini" "--"]
# Thu, 22 Feb 2024 12:50:52 GMT
CMD ["/usr/local/bin/kibana-docker"]
# Thu, 22 Feb 2024 12:50:52 GMT
USER 1000
```

-	Layers:
	-	`sha256:17d0386c2fff30a5b92652bbef2b84639dba9b9f17bdbb819c8d10badd827fdb`  
		Last Modified: Fri, 16 Feb 2024 21:40:52 GMT  
		Size: 27.5 MB (27514312 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:663c7eae5a29ce15f2dc1d74b8172f5d8b51a329d5837016b7e33d67465ac8b2`  
		Last Modified: Wed, 06 Mar 2024 02:58:31 GMT  
		Size: 10.5 MB (10533211 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77bd5e461cf45f4052bb78993954e3ffa0615d06f3871cd013d1ae93fbcf91f6`  
		Last Modified: Wed, 06 Mar 2024 02:58:30 GMT  
		Size: 9.5 KB (9524 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32642d83a7f026522a571a23db6dee76507ef5b8b2ba6a561548d1ad5eaf74d3`  
		Last Modified: Wed, 06 Mar 2024 02:58:30 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a757158a78d5d6110a7d33e6edf54bc06d3e7704f3205e837fca005151f7a8e`  
		Last Modified: Wed, 06 Mar 2024 02:58:31 GMT  
		Size: 16.5 MB (16460475 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41f8381864cde88e6c24be7bd5c015f3348134375e00ee0d180dc896baa46570`  
		Last Modified: Wed, 06 Mar 2024 02:58:32 GMT  
		Size: 5.3 KB (5283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5055cdf698bdec9973c8da23394afcc22766e5d6c469ba11cddf313b68155456`  
		Last Modified: Wed, 06 Mar 2024 02:58:36 GMT  
		Size: 317.1 MB (317073359 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae08c5d62807acd6aaa9bd2aa8d2581fac76e2653393a6048fec4124b894c475`  
		Last Modified: Wed, 06 Mar 2024 02:58:32 GMT  
		Size: 131.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00cb1d5240ca6610a657735c9ccd231e68edda7a4f56b997d757481fc873d7c4`  
		Last Modified: Wed, 06 Mar 2024 02:58:33 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14d846c032bc276eccbba2e51417ef1d386d005f55dd27faf22f3244ae011912`  
		Last Modified: Wed, 06 Mar 2024 02:58:32 GMT  
		Size: 4.6 KB (4554 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b974acb2af001cb9eee3945d861adfdadb88075a8f1ecf95816508b7926a271e`  
		Last Modified: Wed, 06 Mar 2024 02:58:33 GMT  
		Size: 401.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98b0181b4b719198ecdf49ab84c4021004de1c1fc1d2aeed90514964e772219f`  
		Last Modified: Wed, 06 Mar 2024 02:58:33 GMT  
		Size: 189.4 KB (189432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9321933bedb4c1ab5b4c8612f2b66307e600665aa36423760a0ba69e71961254`  
		Last Modified: Wed, 06 Mar 2024 02:58:34 GMT  
		Size: 1.8 KB (1797 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kibana:8.12.2` - unknown; unknown

```console
$ docker pull kibana@sha256:b0783cc4ce78f3ba4119e54209fee4412d76bc07bc182bca7addd662a061bc73
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2169545 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:73c7aaec3c84685bd7d2eda6157e9e6110a66a8056266ad111e4098f575131ca`

```dockerfile
```

-	Layers:
	-	`sha256:a35d0e031a0e6a61b2e9a64972ef70e381986e3e12273fe3e01bf6041fda14e4`  
		Last Modified: Wed, 06 Mar 2024 02:58:31 GMT  
		Size: 2.1 MB (2125193 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f9d01565e43d84d7488eaffa169fbdb7bab2ca0b0d0656254c6a228ee37cd73d`  
		Last Modified: Wed, 06 Mar 2024 02:58:30 GMT  
		Size: 44.4 KB (44352 bytes)  
		MIME: application/vnd.in-toto+json

### `kibana:8.12.2` - linux; arm64 variant v8

```console
$ docker pull kibana@sha256:a24591e30ba88c9d9dd0360821161367130391386b304efd7ac0d13e1edebe24
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **382.2 MB (382247938 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4226a8d6443d802777e39b503c66671e1846eed97e16f9044ade4ec5cbdcb756`
-	Entrypoint: `["\/bin\/tini","--"]`
-	Default Command: `["\/usr\/local\/bin\/kibana-docker"]`

```dockerfile
# Fri, 16 Feb 2024 19:15:01 GMT
ARG RELEASE
# Fri, 16 Feb 2024 19:15:01 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 16 Feb 2024 19:15:01 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 16 Feb 2024 19:15:01 GMT
LABEL org.opencontainers.image.version=20.04
# Fri, 16 Feb 2024 19:15:06 GMT
ADD file:a8303c80b47ec165c276111aa6f98ee877e4da60ddafa00b7547032a3de7935d in / 
# Fri, 16 Feb 2024 19:15:06 GMT
CMD ["/bin/bash"]
# Thu, 22 Feb 2024 12:50:52 GMT
EXPOSE map[5601/tcp:{}]
# Thu, 22 Feb 2024 12:50:52 GMT
RUN for iter in {1..10}; do       export DEBIAN_FRONTEND=noninteractive &&       apt-get update  &&       apt-get upgrade -y  &&       apt-get install -y --no-install-recommends        fontconfig fonts-liberation libnss3 libfontconfig1 ca-certificates curl &&       apt-get clean &&       rm -rf /var/lib/apt/lists/* && exit_code=0 && break || exit_code=$? && echo "apt-get error: retry $iter in 10s" &&       sleep 10;     done;     (exit $exit_code) # buildkit
# Thu, 22 Feb 2024 12:50:52 GMT
RUN set -e ;     TINI_BIN="" ;     case "$(arch)" in         aarch64)             TINI_BIN='tini-arm64' ;             ;;         x86_64)             TINI_BIN='tini-amd64' ;             ;;         *) echo >&2 "Unsupported architecture $(arch)" ; exit 1 ;;     esac ;   TINI_VERSION='v0.19.0' ;   curl --retry 8 -S -L -O "https://github.com/krallin/tini/releases/download/${TINI_VERSION}/${TINI_BIN}" ;   curl --retry 8 -S -L -O "https://github.com/krallin/tini/releases/download/${TINI_VERSION}/${TINI_BIN}.sha256sum" ;   sha256sum -c "${TINI_BIN}.sha256sum" ;   rm "${TINI_BIN}.sha256sum" ;   mv "${TINI_BIN}" /bin/tini ;   chmod +x /bin/tini # buildkit
# Thu, 22 Feb 2024 12:50:52 GMT
RUN mkdir /usr/share/fonts/local # buildkit
# Thu, 22 Feb 2024 12:50:52 GMT
RUN curl --retry 8 -S -L -o /usr/share/fonts/local/NotoSansCJK-Regular.ttc https://github.com/googlefonts/noto-cjk/raw/NotoSansV2.001/NotoSansCJK-Regular.ttc # buildkit
# Thu, 22 Feb 2024 12:50:52 GMT
RUN echo "5dcd1c336cc9344cb77c03a0cd8982ca8a7dc97d620fd6c9c434e02dcb1ceeb3  /usr/share/fonts/local/NotoSansCJK-Regular.ttc" | sha256sum -c - # buildkit
# Thu, 22 Feb 2024 12:50:52 GMT
RUN fc-cache -v # buildkit
# Thu, 22 Feb 2024 12:50:52 GMT
COPY /usr/share/kibana /usr/share/kibana # buildkit
# Thu, 22 Feb 2024 12:50:52 GMT
WORKDIR /usr/share/kibana
# Thu, 22 Feb 2024 12:50:52 GMT
RUN ln -s /usr/share/kibana /opt/kibana # buildkit
# Thu, 22 Feb 2024 12:50:52 GMT
ENV ELASTIC_CONTAINER=true
# Thu, 22 Feb 2024 12:50:52 GMT
ENV PATH=/usr/share/kibana/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 22 Feb 2024 12:50:52 GMT
COPY config/kibana.yml /usr/share/kibana/config/kibana.yml # buildkit
# Thu, 22 Feb 2024 12:50:52 GMT
COPY bin/kibana-docker /usr/local/bin/ # buildkit
# Thu, 22 Feb 2024 12:50:52 GMT
RUN chmod g+ws /usr/share/kibana &&     find /usr/share/kibana -gid 0 -and -not -perm /g+w -exec chmod g+w {} \; # buildkit
# Thu, 22 Feb 2024 12:50:52 GMT
RUN find / -xdev -perm -4000 -exec chmod u-s {} + # buildkit
# Thu, 22 Feb 2024 12:50:52 GMT
RUN groupadd --gid 1000 kibana &&     useradd --uid 1000 --gid 1000 -G 0       --home-dir /usr/share/kibana --no-create-home       kibana # buildkit
# Thu, 22 Feb 2024 12:50:52 GMT
LABEL org.label-schema.build-date=2024-02-19T12:06:34.117Z org.label-schema.license=Elastic License org.label-schema.name=Kibana org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/kibana org.label-schema.usage=https://www.elastic.co/guide/en/kibana/reference/index.html org.label-schema.vcs-ref=f5bd489c5ff9c676c4f861c42da6ea99ae350832 org.label-schema.vcs-url=https://github.com/elastic/kibana org.label-schema.vendor=Elastic org.label-schema.version=8.12.2 org.opencontainers.image.created=2024-02-19T12:06:34.117Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/kibana/reference/index.html org.opencontainers.image.licenses=Elastic License org.opencontainers.image.revision=f5bd489c5ff9c676c4f861c42da6ea99ae350832 org.opencontainers.image.source=https://github.com/elastic/kibana org.opencontainers.image.title=Kibana org.opencontainers.image.url=https://www.elastic.co/products/kibana org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=8.12.2
# Thu, 22 Feb 2024 12:50:52 GMT
ENTRYPOINT ["/bin/tini" "--"]
# Thu, 22 Feb 2024 12:50:52 GMT
CMD ["/usr/local/bin/kibana-docker"]
# Thu, 22 Feb 2024 12:50:52 GMT
USER 1000
```

-	Layers:
	-	`sha256:6aae4cfdd5a10a8b0554e75c4c14ae38022a0c8f08dc5d769a735c705670cab7`  
		Last Modified: Fri, 16 Feb 2024 21:40:59 GMT  
		Size: 26.0 MB (25974391 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4c9948864bfb49a024b682d75c0e5b52c06c1a9e1e0ff0b6e522a03f8931bbd`  
		Last Modified: Wed, 06 Mar 2024 16:53:13 GMT  
		Size: 10.4 MB (10396688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18077aa4ba170eb38aa241c2039f3adaddb6fcf2b3528eaca8aa6f45d359e413`  
		Last Modified: Wed, 06 Mar 2024 16:53:12 GMT  
		Size: 9.1 KB (9099 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:577482fbe412643d000fb170d0399204515aba9d337a84de336375f26ab1397b`  
		Last Modified: Wed, 06 Mar 2024 16:53:12 GMT  
		Size: 157.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b81a29926d0bcaf2765541922bd0e49fa92c33d01a695fa72f10b51416bcf0d`  
		Last Modified: Wed, 06 Mar 2024 16:53:14 GMT  
		Size: 16.5 MB (16460489 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8b2f2b0683e5afe7cfc41dfe0bd6dedc02aa9320161d116f60565349aed2234`  
		Last Modified: Wed, 06 Mar 2024 16:53:13 GMT  
		Size: 5.3 KB (5298 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:141196c9b290ab6089302d68544e5a63cbf961a5fb832e22cb1064a6e1d8e085`  
		Last Modified: Wed, 06 Mar 2024 16:53:20 GMT  
		Size: 329.2 MB (329211041 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e5a72e2b0accd31f668c8dbfad596e261c1c8066962a021ff513980031a28d8`  
		Last Modified: Wed, 06 Mar 2024 16:53:14 GMT  
		Size: 131.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:507acfea25530e0d12c7033d9a75dfca81e6fc6e4ac57e99f6cd00f9d8f938cf`  
		Last Modified: Wed, 06 Mar 2024 16:53:15 GMT  
		Size: 399.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15dc2098abe63f1393f6c4fe0413eef8993f6ef70b0a1636de1a2a01b7c54113`  
		Last Modified: Wed, 06 Mar 2024 16:53:15 GMT  
		Size: 4.6 KB (4553 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57ae57d868135690bb0f28f10868569ecfc49250d247537bf7a4b9d43824eb15`  
		Last Modified: Wed, 06 Mar 2024 16:53:16 GMT  
		Size: 401.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25b361d64c00b753d5fa17324f32303f6a2d647671d50f17961baad9c7fdb177`  
		Last Modified: Wed, 06 Mar 2024 16:53:16 GMT  
		Size: 183.4 KB (183424 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03c22a449abd1f93621b607897f5b05a1b6d18def0a87439ccb1ee52b652ee47`  
		Last Modified: Wed, 06 Mar 2024 16:53:16 GMT  
		Size: 1.8 KB (1803 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kibana:8.12.2` - unknown; unknown

```console
$ docker pull kibana@sha256:8528c9710e7511cb3f1107f844d9fc179233f9cede4e073c9442b17fe2f47374
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2169623 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:13100919423175089527fb5e4b3978cad752377090d85851ea975746b9956013`

```dockerfile
```

-	Layers:
	-	`sha256:aec272003c808415dc5840d8b2e00f9589588cee74b869b868840ea86b1ffafc`  
		Last Modified: Wed, 06 Mar 2024 16:53:13 GMT  
		Size: 2.1 MB (2125428 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3b2c19913748b8c26565dd29b37769f922268147a33599ae422a97bd445829a2`  
		Last Modified: Wed, 06 Mar 2024 16:53:13 GMT  
		Size: 44.2 KB (44195 bytes)  
		MIME: application/vnd.in-toto+json
