<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `kibana`

-	[`kibana:7.17.26`](#kibana71726)
-	[`kibana:8.15.5`](#kibana8155)
-	[`kibana:8.16.1`](#kibana8161)

## `kibana:7.17.26`

```console
$ docker pull kibana@sha256:bc1cd2972c35efde55c189a354bb85586b60fa2c20042902961a9053f7adf86b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `kibana:7.17.26` - linux; amd64

```console
$ docker pull kibana@sha256:8bd133f1822584d4ebd4cbaceda8855f89f4bd78426d9164b7372a1bf6c5be2a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **350.2 MB (350190795 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:86125e2096145214289b981b29771bafe313de9ff71028f97b3e48e966177b65`
-	Entrypoint: `["\/bin\/tini","--"]`
-	Default Command: `["\/usr\/local\/bin\/kibana-docker"]`

```dockerfile
# Fri, 11 Oct 2024 03:38:25 GMT
ARG RELEASE
# Fri, 11 Oct 2024 03:38:25 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 11 Oct 2024 03:38:25 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 11 Oct 2024 03:38:25 GMT
LABEL org.opencontainers.image.version=20.04
# Fri, 11 Oct 2024 03:38:27 GMT
ADD file:7486147a645d8835a5181c79f00a3606c6b714c83bcbfcd8862221eb14690f9e in / 
# Fri, 11 Oct 2024 03:38:27 GMT
CMD ["/bin/bash"]
# Tue, 03 Dec 2024 13:02:17 GMT
EXPOSE map[5601/tcp:{}]
# Tue, 03 Dec 2024 13:02:17 GMT
RUN for iter in {1..10}; do       export DEBIAN_FRONTEND=noninteractive &&       apt-get update  &&       apt-get upgrade -y  &&       apt-get install -y --no-install-recommends        fontconfig fonts-liberation libnss3 libfontconfig1 ca-certificates curl &&       apt-get clean &&       rm -rf /var/lib/apt/lists/* && exit_code=0 && break || exit_code=$? && echo "apt-get error: retry $iter in 10s" &&       sleep 10;     done;     (exit $exit_code) # buildkit
# Tue, 03 Dec 2024 13:02:17 GMT
RUN set -e ;     TINI_BIN="" ;     case "$(arch)" in         aarch64)             TINI_BIN='tini-arm64' ;             ;;         x86_64)             TINI_BIN='tini-amd64' ;             ;;         *) echo >&2 "Unsupported architecture $(arch)" ; exit 1 ;;     esac ;   TINI_VERSION='v0.19.0' ;   curl --retry 8 -S -L -O "https://github.com/krallin/tini/releases/download/${TINI_VERSION}/${TINI_BIN}" ;   curl --retry 8 -S -L -O "https://github.com/krallin/tini/releases/download/${TINI_VERSION}/${TINI_BIN}.sha256sum" ;   sha256sum -c "${TINI_BIN}.sha256sum" ;   rm "${TINI_BIN}.sha256sum" ;   mv "${TINI_BIN}" /bin/tini ;   chmod +x /bin/tini # buildkit
# Tue, 03 Dec 2024 13:02:17 GMT
RUN mkdir /usr/share/fonts/local # buildkit
# Tue, 03 Dec 2024 13:02:17 GMT
RUN curl --retry 8 -S -L -o /usr/share/fonts/local/NotoSansCJK-Regular.ttc https://github.com/googlefonts/noto-cjk/raw/NotoSansV2.001/NotoSansCJK-Regular.ttc # buildkit
# Tue, 03 Dec 2024 13:02:17 GMT
RUN echo "5dcd1c336cc9344cb77c03a0cd8982ca8a7dc97d620fd6c9c434e02dcb1ceeb3  /usr/share/fonts/local/NotoSansCJK-Regular.ttc" | sha256sum -c - # buildkit
# Tue, 03 Dec 2024 13:02:17 GMT
RUN fc-cache -v # buildkit
# Tue, 03 Dec 2024 13:02:17 GMT
COPY --chown=1000:0 /usr/share/kibana /usr/share/kibana # buildkit
# Tue, 03 Dec 2024 13:02:17 GMT
WORKDIR /usr/share/kibana
# Tue, 03 Dec 2024 13:02:17 GMT
RUN ln -s /usr/share/kibana /opt/kibana # buildkit
# Tue, 03 Dec 2024 13:02:17 GMT
ENV ELASTIC_CONTAINER=true
# Tue, 03 Dec 2024 13:02:17 GMT
ENV PATH=/usr/share/kibana/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Dec 2024 13:02:17 GMT
COPY --chown=1000:0 config/kibana.yml /usr/share/kibana/config/kibana.yml # buildkit
# Tue, 03 Dec 2024 13:02:17 GMT
COPY bin/kibana-docker /usr/local/bin/ # buildkit
# Tue, 03 Dec 2024 13:02:17 GMT
RUN chmod g+ws /usr/share/kibana &&     find /usr/share/kibana -gid 0 -and -not -perm /g+w -exec chmod g+w {} \; # buildkit
# Tue, 03 Dec 2024 13:02:17 GMT
RUN find / -xdev -perm -4000 -exec chmod u-s {} + # buildkit
# Tue, 03 Dec 2024 13:02:17 GMT
RUN groupadd --gid 1000 kibana &&     useradd --uid 1000 --gid 1000 -G 0       --home-dir /usr/share/kibana --no-create-home       kibana # buildkit
# Tue, 03 Dec 2024 13:02:17 GMT
LABEL org.label-schema.build-date=2024-11-26T12:11:54.291Z org.label-schema.license=Elastic License org.label-schema.name=Kibana org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/kibana org.label-schema.usage=https://www.elastic.co/guide/en/kibana/reference/index.html org.label-schema.vcs-ref=2ed05e4a85cb41a24646b02ee9c1b6ab2b0e9cde org.label-schema.vcs-url=https://github.com/elastic/kibana org.label-schema.vendor=Elastic org.label-schema.version=7.17.26 org.opencontainers.image.created=2024-11-26T12:11:54.291Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/kibana/reference/index.html org.opencontainers.image.licenses=Elastic License org.opencontainers.image.revision=2ed05e4a85cb41a24646b02ee9c1b6ab2b0e9cde org.opencontainers.image.source=https://github.com/elastic/kibana org.opencontainers.image.title=Kibana org.opencontainers.image.url=https://www.elastic.co/products/kibana org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=7.17.26
# Tue, 03 Dec 2024 13:02:17 GMT
ENTRYPOINT ["/bin/tini" "--"]
# Tue, 03 Dec 2024 13:02:17 GMT
CMD ["/usr/local/bin/kibana-docker"]
# Tue, 03 Dec 2024 13:02:17 GMT
USER kibana
```

-	Layers:
	-	`sha256:d9802f032d6798e2086607424bfe88cb8ec1d6f116e11cd99592dcaf261e9cd2`  
		Last Modified: Fri, 11 Oct 2024 04:41:25 GMT  
		Size: 27.5 MB (27511060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:590ed550527a8d93ce633556d61b3e8d88cba7a24ddd478e9dd2a0eff903f356`  
		Last Modified: Tue, 03 Dec 2024 19:31:30 GMT  
		Size: 10.7 MB (10723869 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e3faf5e235fa4ed4a10867776317a8fc758f9c43e77261eeb268a5a2a2dfe3d`  
		Last Modified: Tue, 03 Dec 2024 19:31:30 GMT  
		Size: 9.5 KB (9529 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d4540743acfa28d456e5a1c03288a086f5cf9516128650bb9f0c91f485d2c49`  
		Last Modified: Tue, 03 Dec 2024 19:31:29 GMT  
		Size: 160.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d52c57c949c1fe77eedb3044cb913825a4033656c5c645c995570d664ec10c2`  
		Last Modified: Tue, 03 Dec 2024 19:31:30 GMT  
		Size: 16.5 MB (16460489 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1a9c9dc1a614345e36404a07049a2a31cbd02df4087b1c615821ead296eebf8`  
		Last Modified: Tue, 03 Dec 2024 19:31:31 GMT  
		Size: 5.3 KB (5297 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad6fee08805b694cee2f7aa48045c870791e6bef6810ad0af859fc2d834df11e`  
		Last Modified: Tue, 03 Dec 2024 19:31:37 GMT  
		Size: 295.3 MB (295283661 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:349b98ddec90697e1647392f923a2db66340fc8982f2e35f654c02484b85c982`  
		Last Modified: Tue, 03 Dec 2024 19:31:31 GMT  
		Size: 132.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10db4bdc349a2fd8528ffcb9db8f5e731595dbae068e86e4e6070e5bf7a64d76`  
		Last Modified: Tue, 03 Dec 2024 19:31:32 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aaaf4716c51a2e356d33073829801012b426ecee71a7c5babc27be690e3ed97f`  
		Last Modified: Tue, 03 Dec 2024 19:31:32 GMT  
		Size: 4.5 KB (4505 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3fb3330f94467c337a6c80df2da2a7d1e287194455bfc6ee4ef0c622674f7e67`  
		Last Modified: Tue, 03 Dec 2024 19:31:32 GMT  
		Size: 401.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:453bc89ed015468a939e7d5c9225c54fd94eca0f6cb76853a5c82893a2617886`  
		Last Modified: Tue, 03 Dec 2024 19:31:33 GMT  
		Size: 189.4 KB (189431 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4fd951edd397b9e9e9a589c5b6bcf5150168c9e8ab417b7679ceb1884b81a69`  
		Last Modified: Tue, 03 Dec 2024 19:31:33 GMT  
		Size: 1.8 KB (1800 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kibana:7.17.26` - unknown; unknown

```console
$ docker pull kibana@sha256:d976750be8431f5ef218ede2cb31d95e5d27215a64fb5dd7994b3c1cee3bcffb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3475895 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:31bba74442fd7a91de0ef9e612838c02719954157fc379ccb19d8b8ff29e23f6`

```dockerfile
```

-	Layers:
	-	`sha256:d6d1481f84b053597ae05baf4171fde6d92471b449773d478cfbc7b5d37efc61`  
		Last Modified: Tue, 03 Dec 2024 19:31:30 GMT  
		Size: 3.4 MB (3431386 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:496016d74cc223ded5101c845edce3ce7da3e6fd51233207ba21263a5441402b`  
		Last Modified: Tue, 03 Dec 2024 19:31:30 GMT  
		Size: 44.5 KB (44509 bytes)  
		MIME: application/vnd.in-toto+json

## `kibana:8.15.5`

```console
$ docker pull kibana@sha256:50747708188e70e064a7fcc8e8f85b163dce6cdc2c5adfa4f0bf1e65427be8b5
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `kibana:8.15.5` - linux; amd64

```console
$ docker pull kibana@sha256:89956cf11a3bf2965cf413a881541c5833ae1e43ea81e4ed1f8f3d675b65f9c1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **396.0 MB (396022146 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e76560fb814122f627cc084a2f2ad758932e691cc90268c00b247445b5c84761`
-	Entrypoint: `["\/bin\/tini","--"]`
-	Default Command: `["\/usr\/local\/bin\/kibana-docker"]`

```dockerfile
# Fri, 11 Oct 2024 03:38:25 GMT
ARG RELEASE
# Fri, 11 Oct 2024 03:38:25 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 11 Oct 2024 03:38:25 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 11 Oct 2024 03:38:25 GMT
LABEL org.opencontainers.image.version=20.04
# Fri, 11 Oct 2024 03:38:27 GMT
ADD file:7486147a645d8835a5181c79f00a3606c6b714c83bcbfcd8862221eb14690f9e in / 
# Fri, 11 Oct 2024 03:38:27 GMT
CMD ["/bin/bash"]
# Tue, 26 Nov 2024 10:47:54 GMT
EXPOSE map[5601/tcp:{}]
# Tue, 26 Nov 2024 10:47:54 GMT
RUN for iter in {1..10}; do       export DEBIAN_FRONTEND=noninteractive &&       apt-get update  &&       apt-get upgrade -y  &&       apt-get install -y --no-install-recommends        fontconfig libnss3 curl ca-certificates &&       apt-get clean &&       rm -rf /var/lib/apt/lists/* && exit_code=0 && break || exit_code=$? && echo "apt-get error: retry $iter in 10s" &&       sleep 10;     done;     (exit $exit_code) # buildkit
# Tue, 26 Nov 2024 10:47:54 GMT
COPY --chown=1000:0 /usr/share/kibana /usr/share/kibana # buildkit
# Tue, 26 Nov 2024 10:47:54 GMT
COPY --chown=0:0 /bin/tini /bin/tini # buildkit
# Tue, 26 Nov 2024 10:47:54 GMT
COPY --chown=0:0 /usr/share/fonts/local/NotoSansCJK-Regular.ttc /usr/share/fonts/local/NotoSansCJK-Regular.ttc # buildkit
# Tue, 26 Nov 2024 10:47:54 GMT
RUN fc-cache -v # buildkit
# Tue, 26 Nov 2024 10:47:54 GMT
WORKDIR /usr/share/kibana
# Tue, 26 Nov 2024 10:47:54 GMT
RUN ln -s /usr/share/kibana /opt/kibana # buildkit
# Tue, 26 Nov 2024 10:47:54 GMT
ENV ELASTIC_CONTAINER=true
# Tue, 26 Nov 2024 10:47:54 GMT
ENV PATH=/usr/share/kibana/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 26 Nov 2024 10:47:54 GMT
COPY --chown=1000:0 config/kibana.yml /usr/share/kibana/config/kibana.yml # buildkit
# Tue, 26 Nov 2024 10:47:54 GMT
COPY bin/kibana-docker /usr/local/bin/ # buildkit
# Tue, 26 Nov 2024 10:47:54 GMT
RUN chmod g+ws /usr/share/kibana &&     find /usr/share/kibana -gid 0 -and -not -perm /g+w -exec chmod g+w {} \; # buildkit
# Tue, 26 Nov 2024 10:47:54 GMT
RUN find / -xdev -perm -4000 -exec chmod u-s {} + # buildkit
# Tue, 26 Nov 2024 10:47:54 GMT
RUN groupadd --gid 1000 kibana &&     useradd --uid 1000 --gid 1000 -G 0       --home-dir /usr/share/kibana --no-create-home       kibana # buildkit
# Tue, 26 Nov 2024 10:47:54 GMT
LABEL org.label-schema.build-date=2024-11-21T19:13:27.003Z org.label-schema.license=Elastic License org.label-schema.name=Kibana org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/kibana org.label-schema.usage=https://www.elastic.co/guide/en/kibana/reference/index.html org.label-schema.vcs-ref=5454456a21f37f1af07df030c56a2953ad33f999 org.label-schema.vcs-url=https://github.com/elastic/kibana org.label-schema.vendor=Elastic org.label-schema.version=8.15.5 org.opencontainers.image.created=2024-11-21T19:13:27.003Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/kibana/reference/index.html org.opencontainers.image.licenses=Elastic License org.opencontainers.image.revision=5454456a21f37f1af07df030c56a2953ad33f999 org.opencontainers.image.source=https://github.com/elastic/kibana org.opencontainers.image.title=Kibana org.opencontainers.image.url=https://www.elastic.co/products/kibana org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=8.15.5
# Tue, 26 Nov 2024 10:47:54 GMT
ENTRYPOINT ["/bin/tini" "--"]
# Tue, 26 Nov 2024 10:47:54 GMT
CMD ["/usr/local/bin/kibana-docker"]
# Tue, 26 Nov 2024 10:47:54 GMT
USER 1000
```

-	Layers:
	-	`sha256:d9802f032d6798e2086607424bfe88cb8ec1d6f116e11cd99592dcaf261e9cd2`  
		Last Modified: Fri, 11 Oct 2024 04:41:25 GMT  
		Size: 27.5 MB (27511060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22b40923dd27f47daa05b48422745a7fc0a8b404f4da7534b9d9d30fb35f1b30`  
		Last Modified: Tue, 26 Nov 2024 18:26:17 GMT  
		Size: 11.0 MB (10966641 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0b7d669130d8f172ca12324f1684b2f27aacdad4b827a35f13f548ddfa060fa`  
		Last Modified: Tue, 26 Nov 2024 18:26:34 GMT  
		Size: 340.9 MB (340872349 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b620c991f0a9853f8ee1e11df70f067aa792469bba9fc591a218a24bd8612ec9`  
		Last Modified: Tue, 26 Nov 2024 18:26:16 GMT  
		Size: 9.5 KB (9530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca31569adfebaf6d65e771c870a86ee43672f799cd2c77dd37364a7c80e60c8d`  
		Last Modified: Tue, 26 Nov 2024 18:26:17 GMT  
		Size: 16.5 MB (16460477 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e393a4e164540d44589005833741489389956de341efbb423a89b38f9e6cd86`  
		Last Modified: Tue, 26 Nov 2024 18:26:17 GMT  
		Size: 5.3 KB (5275 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b69aa101730b82d83092548a1d710a915f69108a0199d9cd06415110fdcf96e`  
		Last Modified: Tue, 26 Nov 2024 18:26:18 GMT  
		Size: 131.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:322854bcbf955e17815b385bfc2e22d982ce74e9e65b2ca933c3e6d164c5fc57`  
		Last Modified: Tue, 26 Nov 2024 18:26:18 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7477d6d5941638622cf3b751355e198df75635ba807d81171d8cd56ad09780d4`  
		Last Modified: Tue, 26 Nov 2024 18:26:18 GMT  
		Size: 4.6 KB (4625 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8eb9b7dbd02a39fda55c2309df06265dae23106821e5576db4ff5600302f9749`  
		Last Modified: Tue, 26 Nov 2024 18:26:19 GMT  
		Size: 399.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf44f67bd129f8d95737f2e701f6fd8e0168797116226c5dd5f2d81236895038`  
		Last Modified: Tue, 26 Nov 2024 18:26:19 GMT  
		Size: 189.4 KB (189435 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8469bd51b7dd5294dbd8cc3c8fce4aef1ece652b3e664b5ae4d5d3b1e6d602c3`  
		Last Modified: Tue, 26 Nov 2024 18:26:19 GMT  
		Size: 1.8 KB (1797 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kibana:8.15.5` - unknown; unknown

```console
$ docker pull kibana@sha256:dbbf478111c6a62c87444e83e7758476ab42e0183c642e8db725c1ca1c077e22
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4235095 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:14a51595cfca3f355af7769a5ea27b8618cc1b01a2f740741b292dbfeffd2cbc`

```dockerfile
```

-	Layers:
	-	`sha256:0c5b3d8c2dd2f3a9c3f59b1ebd596f1a1d361ab15a86b84c65ea79f06b99cb44`  
		Last Modified: Tue, 26 Nov 2024 18:26:17 GMT  
		Size: 4.2 MB (4194453 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:14615724e06aed1856ef71d7fb2282d2a3fb2b31444c7987fc7b3b2a1666424d`  
		Last Modified: Tue, 26 Nov 2024 18:26:16 GMT  
		Size: 40.6 KB (40642 bytes)  
		MIME: application/vnd.in-toto+json

### `kibana:8.15.5` - linux; arm64 variant v8

```console
$ docker pull kibana@sha256:ce9527b50694af3ae57504bdc9dc840617a87a9a8ca778ea79fa738ed0eb7ca2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **406.5 MB (406480816 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e03f8e8bfeb2afe13115a4e13d94b06af23021d978641df4cec3efbc903c496`
-	Entrypoint: `["\/bin\/tini","--"]`
-	Default Command: `["\/usr\/local\/bin\/kibana-docker"]`

```dockerfile
# Fri, 11 Oct 2024 03:39:45 GMT
ARG RELEASE
# Fri, 11 Oct 2024 03:39:45 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 11 Oct 2024 03:39:45 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 11 Oct 2024 03:39:45 GMT
LABEL org.opencontainers.image.version=20.04
# Fri, 11 Oct 2024 03:39:47 GMT
ADD file:8537b4db344382b39d669af27cd94ec0f870ceafe58c67ee54e3f9b38fb8d671 in / 
# Fri, 11 Oct 2024 03:39:47 GMT
CMD ["/bin/bash"]
# Tue, 26 Nov 2024 10:47:54 GMT
EXPOSE map[5601/tcp:{}]
# Tue, 26 Nov 2024 10:47:54 GMT
RUN for iter in {1..10}; do       export DEBIAN_FRONTEND=noninteractive &&       apt-get update  &&       apt-get upgrade -y  &&       apt-get install -y --no-install-recommends        fontconfig libnss3 curl ca-certificates &&       apt-get clean &&       rm -rf /var/lib/apt/lists/* && exit_code=0 && break || exit_code=$? && echo "apt-get error: retry $iter in 10s" &&       sleep 10;     done;     (exit $exit_code) # buildkit
# Tue, 26 Nov 2024 10:47:54 GMT
COPY --chown=1000:0 /usr/share/kibana /usr/share/kibana # buildkit
# Tue, 26 Nov 2024 10:47:54 GMT
COPY --chown=0:0 /bin/tini /bin/tini # buildkit
# Tue, 26 Nov 2024 10:47:54 GMT
COPY --chown=0:0 /usr/share/fonts/local/NotoSansCJK-Regular.ttc /usr/share/fonts/local/NotoSansCJK-Regular.ttc # buildkit
# Tue, 26 Nov 2024 10:47:54 GMT
RUN fc-cache -v # buildkit
# Tue, 26 Nov 2024 10:47:54 GMT
WORKDIR /usr/share/kibana
# Tue, 26 Nov 2024 10:47:54 GMT
RUN ln -s /usr/share/kibana /opt/kibana # buildkit
# Tue, 26 Nov 2024 10:47:54 GMT
ENV ELASTIC_CONTAINER=true
# Tue, 26 Nov 2024 10:47:54 GMT
ENV PATH=/usr/share/kibana/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 26 Nov 2024 10:47:54 GMT
COPY --chown=1000:0 config/kibana.yml /usr/share/kibana/config/kibana.yml # buildkit
# Tue, 26 Nov 2024 10:47:54 GMT
COPY bin/kibana-docker /usr/local/bin/ # buildkit
# Tue, 26 Nov 2024 10:47:54 GMT
RUN chmod g+ws /usr/share/kibana &&     find /usr/share/kibana -gid 0 -and -not -perm /g+w -exec chmod g+w {} \; # buildkit
# Tue, 26 Nov 2024 10:47:54 GMT
RUN find / -xdev -perm -4000 -exec chmod u-s {} + # buildkit
# Tue, 26 Nov 2024 10:47:54 GMT
RUN groupadd --gid 1000 kibana &&     useradd --uid 1000 --gid 1000 -G 0       --home-dir /usr/share/kibana --no-create-home       kibana # buildkit
# Tue, 26 Nov 2024 10:47:54 GMT
LABEL org.label-schema.build-date=2024-11-21T19:13:27.003Z org.label-schema.license=Elastic License org.label-schema.name=Kibana org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/kibana org.label-schema.usage=https://www.elastic.co/guide/en/kibana/reference/index.html org.label-schema.vcs-ref=5454456a21f37f1af07df030c56a2953ad33f999 org.label-schema.vcs-url=https://github.com/elastic/kibana org.label-schema.vendor=Elastic org.label-schema.version=8.15.5 org.opencontainers.image.created=2024-11-21T19:13:27.003Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/kibana/reference/index.html org.opencontainers.image.licenses=Elastic License org.opencontainers.image.revision=5454456a21f37f1af07df030c56a2953ad33f999 org.opencontainers.image.source=https://github.com/elastic/kibana org.opencontainers.image.title=Kibana org.opencontainers.image.url=https://www.elastic.co/products/kibana org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=8.15.5
# Tue, 26 Nov 2024 10:47:54 GMT
ENTRYPOINT ["/bin/tini" "--"]
# Tue, 26 Nov 2024 10:47:54 GMT
CMD ["/usr/local/bin/kibana-docker"]
# Tue, 26 Nov 2024 10:47:54 GMT
USER 1000
```

-	Layers:
	-	`sha256:1b9f3c55f9d4aa5c52eb67a4cb7d0f4726ab85a413b50e3e3fe788befce3d297`  
		Last Modified: Fri, 11 Oct 2024 04:41:30 GMT  
		Size: 26.0 MB (25973828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5615ce72569ba1d15512469e51a8912567f652afdf4f67ce8df86e055a26c182`  
		Last Modified: Mon, 18 Nov 2024 23:48:55 GMT  
		Size: 10.8 MB (10818065 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1932457f06085c0f3c48de6837f74c683c4529ba16cdb7859808cfda30cf28d5`  
		Last Modified: Tue, 26 Nov 2024 18:33:44 GMT  
		Size: 353.0 MB (353023235 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a48b9fa80e13d4720cc7cd04dddb925f497de09abc0199b75179bcb7a0ccf1d`  
		Last Modified: Tue, 26 Nov 2024 18:33:36 GMT  
		Size: 9.1 KB (9096 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86b15d479f36b89001d2544506309967f558d80c5829f7be5231f5dbccfe4ac4`  
		Last Modified: Tue, 26 Nov 2024 18:33:37 GMT  
		Size: 16.5 MB (16460490 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f97fa73bd40402a551bc5c5106185c4c8dad79a0d63867cfa51ef203c85a7b1`  
		Last Modified: Tue, 26 Nov 2024 18:33:37 GMT  
		Size: 5.3 KB (5296 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6c9aef279d514553e4aae0900687616bab654e3eb4e4269b14cad516ef0ae0b`  
		Last Modified: Tue, 26 Nov 2024 18:33:38 GMT  
		Size: 131.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44df78a1745c5b575d8fe7fbf0d2c12a2378adf61bdafb613caac97b4445c564`  
		Last Modified: Tue, 26 Nov 2024 18:33:38 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66b0ddf82bc47ae4eec5dfe6cf52aef70c0fe390a0161aaabb5dfb41b9cebc59`  
		Last Modified: Tue, 26 Nov 2024 18:33:38 GMT  
		Size: 4.6 KB (4623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c54a7af09096e5a78fe223cbf9ff16b3722098913890fc63a760cdabde8f4ec1`  
		Last Modified: Tue, 26 Nov 2024 18:33:39 GMT  
		Size: 401.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f76018731203698886f80c8c8c5cd0f5ad7493a6a5fd59cb618d5d823b3ca4b`  
		Last Modified: Tue, 26 Nov 2024 18:33:39 GMT  
		Size: 183.4 KB (183417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef7259657d36520a14681e91b8a8275dc120cb3e0389790af0b4916046ca542a`  
		Last Modified: Tue, 26 Nov 2024 18:33:39 GMT  
		Size: 1.8 KB (1805 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kibana:8.15.5` - unknown; unknown

```console
$ docker pull kibana@sha256:7bd23cfe8f70689fbb682c1362e611c6b7f41f6f80e1edd4e150815fec6f51c4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4235593 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df97528fc0ae3cadb50204ddca154443adfeb52583e861acbd0fc333d3881041`

```dockerfile
```

-	Layers:
	-	`sha256:9760d09eab7772c7cac0d24160d7012488eacd14e88bf3c967561eb99f23158a`  
		Last Modified: Tue, 26 Nov 2024 18:33:37 GMT  
		Size: 4.2 MB (4194703 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:25ebcfe3e081aa7d088201fbad440603a1e6020ffcf12eff3cc5832a4c47a209`  
		Last Modified: Tue, 26 Nov 2024 18:33:37 GMT  
		Size: 40.9 KB (40890 bytes)  
		MIME: application/vnd.in-toto+json

## `kibana:8.16.1`

```console
$ docker pull kibana@sha256:e18c1f6d92e819b1c577a1af9a02bfcae6e8b63596368eec3b40e9ad98fa3caa
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `kibana:8.16.1` - linux; amd64

```console
$ docker pull kibana@sha256:f8c9ef95178e2d69f235b7608002aad6e65a9bd5619a97c6fcf70cd711b54e93
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **399.5 MB (399539259 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3bd512e662b948d5cb401f5157a796b1637867982f9ee6ec7e3fe570bcbc7fd8`
-	Entrypoint: `["\/bin\/tini","--"]`
-	Default Command: `["\/usr\/local\/bin\/kibana-docker"]`

```dockerfile
# Fri, 11 Oct 2024 03:38:25 GMT
ARG RELEASE
# Fri, 11 Oct 2024 03:38:25 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 11 Oct 2024 03:38:25 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 11 Oct 2024 03:38:25 GMT
LABEL org.opencontainers.image.version=20.04
# Fri, 11 Oct 2024 03:38:27 GMT
ADD file:7486147a645d8835a5181c79f00a3606c6b714c83bcbfcd8862221eb14690f9e in / 
# Fri, 11 Oct 2024 03:38:27 GMT
CMD ["/bin/bash"]
# Thu, 21 Nov 2024 14:43:56 GMT
EXPOSE map[5601/tcp:{}]
# Thu, 21 Nov 2024 14:43:56 GMT
RUN for iter in {1..10}; do       export DEBIAN_FRONTEND=noninteractive &&       apt-get update  &&       apt-get upgrade -y  &&       apt-get install -y --no-install-recommends        fontconfig libnss3 curl ca-certificates &&       apt-get clean &&       rm -rf /var/lib/apt/lists/* && exit_code=0 && break || exit_code=$? && echo "apt-get error: retry $iter in 10s" &&       sleep 10;     done;     (exit $exit_code) # buildkit
# Thu, 21 Nov 2024 14:43:56 GMT
COPY --chown=1000:0 /usr/share/kibana /usr/share/kibana # buildkit
# Thu, 21 Nov 2024 14:43:56 GMT
COPY --chown=0:0 /bin/tini /bin/tini # buildkit
# Thu, 21 Nov 2024 14:43:56 GMT
COPY --chown=0:0 /usr/share/fonts/local/NotoSansCJK-Regular.ttc /usr/share/fonts/local/NotoSansCJK-Regular.ttc # buildkit
# Thu, 21 Nov 2024 14:43:56 GMT
RUN fc-cache -v # buildkit
# Thu, 21 Nov 2024 14:43:56 GMT
WORKDIR /usr/share/kibana
# Thu, 21 Nov 2024 14:43:56 GMT
RUN ln -s /usr/share/kibana /opt/kibana # buildkit
# Thu, 21 Nov 2024 14:43:56 GMT
ENV ELASTIC_CONTAINER=true
# Thu, 21 Nov 2024 14:43:56 GMT
ENV PATH=/usr/share/kibana/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 21 Nov 2024 14:43:56 GMT
COPY --chown=1000:0 config/kibana.yml /usr/share/kibana/config/kibana.yml # buildkit
# Thu, 21 Nov 2024 14:43:56 GMT
COPY bin/kibana-docker /usr/local/bin/ # buildkit
# Thu, 21 Nov 2024 14:43:56 GMT
RUN chmod g+ws /usr/share/kibana &&     find /usr/share/kibana -gid 0 -and -not -perm /g+w -exec chmod g+w {} \; # buildkit
# Thu, 21 Nov 2024 14:43:56 GMT
RUN find / -xdev -perm -4000 -exec chmod u-s {} + # buildkit
# Thu, 21 Nov 2024 14:43:56 GMT
RUN groupadd --gid 1000 kibana &&     useradd --uid 1000 --gid 1000 -G 0       --home-dir /usr/share/kibana --no-create-home       kibana # buildkit
# Thu, 21 Nov 2024 14:43:56 GMT
LABEL org.label-schema.build-date=2024-11-18T21:51:43.597Z org.label-schema.license=Elastic License org.label-schema.name=Kibana org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/kibana org.label-schema.usage=https://www.elastic.co/guide/en/kibana/reference/index.html org.label-schema.vcs-ref=c8b46e87c4d61de4fe046ce5ea0a0b68aad5acf9 org.label-schema.vcs-url=https://github.com/elastic/kibana org.label-schema.vendor=Elastic org.label-schema.version=8.16.1 org.opencontainers.image.created=2024-11-18T21:51:43.597Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/kibana/reference/index.html org.opencontainers.image.licenses=Elastic License org.opencontainers.image.revision=c8b46e87c4d61de4fe046ce5ea0a0b68aad5acf9 org.opencontainers.image.source=https://github.com/elastic/kibana org.opencontainers.image.title=Kibana org.opencontainers.image.url=https://www.elastic.co/products/kibana org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=8.16.1
# Thu, 21 Nov 2024 14:43:56 GMT
ENTRYPOINT ["/bin/tini" "--"]
# Thu, 21 Nov 2024 14:43:56 GMT
CMD ["/usr/local/bin/kibana-docker"]
# Thu, 21 Nov 2024 14:43:56 GMT
USER 1000
```

-	Layers:
	-	`sha256:d9802f032d6798e2086607424bfe88cb8ec1d6f116e11cd99592dcaf261e9cd2`  
		Last Modified: Fri, 11 Oct 2024 04:41:25 GMT  
		Size: 27.5 MB (27511060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c09c13c28a9457ae8351feba0af26380ec81d28b0bd85a34ff46ceb4c10b97b`  
		Last Modified: Fri, 22 Nov 2024 22:27:20 GMT  
		Size: 11.0 MB (10966600 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2725ea15fd504d7a1bf6e70379bc8601ccfbf419f42b27157fe7970cf783f153`  
		Last Modified: Fri, 22 Nov 2024 22:27:24 GMT  
		Size: 344.4 MB (344389396 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7555efbf0e0e57d6b2ff7f4c5ec164d7fcdfe15222fc645085df8df3a304b883`  
		Last Modified: Fri, 22 Nov 2024 22:27:20 GMT  
		Size: 9.5 KB (9531 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fe02a55404585e7ba59c162fa3f9a5d22908ba8f8b5a1d7edd3626afe001f00`  
		Last Modified: Fri, 22 Nov 2024 22:27:21 GMT  
		Size: 16.5 MB (16460495 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07f98293cbc6ee0a63d7a9aaa66dde40d8caa26cc9301dc9c845e7be74f83349`  
		Last Modified: Fri, 22 Nov 2024 22:27:20 GMT  
		Size: 5.3 KB (5278 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5912356d257df2378fbf4e0e1601eb09c1ab582a5e76ff57b777f590d4a7717b`  
		Last Modified: Fri, 22 Nov 2024 22:27:21 GMT  
		Size: 131.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab8e5194538bf0faa60f77fd2416b0c75033479286330004357b4abaafe3a573`  
		Last Modified: Fri, 22 Nov 2024 22:27:21 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5699e7e34f4ccf05533b5238e7d1fdbe1893518f9ad00273dc0fb7ffa11fa720`  
		Last Modified: Fri, 22 Nov 2024 22:27:22 GMT  
		Size: 4.7 KB (4708 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e199b4ca13004e31fe8f8fa3379b1e9f271337cbd39ef478c95107a931aa37ed`  
		Last Modified: Fri, 22 Nov 2024 22:27:22 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ada342a4c70a9fe6662eff41981563444cbcedec1d35f2b844b62f4e8d788df`  
		Last Modified: Fri, 22 Nov 2024 22:27:22 GMT  
		Size: 189.4 KB (189435 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c7750700c9c9421908a7e3f9f52fada3f55362c5da62ff98a2a74e02317583b`  
		Last Modified: Fri, 22 Nov 2024 22:27:22 GMT  
		Size: 1.8 KB (1799 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kibana:8.16.1` - unknown; unknown

```console
$ docker pull kibana@sha256:b4aa4248184403e507fd219e79f6859fe0077a35e563436f8c8404aeaff15bb9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4364422 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:44e804663ffe72a322e0f84fb4ac958bb9a7c272d46569121ff310180c525701`

```dockerfile
```

-	Layers:
	-	`sha256:41934a059eb1faeb4aeaf432637557ad04d70f8f64d0656beb02ae94ddc2c1fe`  
		Last Modified: Fri, 22 Nov 2024 22:27:20 GMT  
		Size: 4.3 MB (4323778 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a800f48aaa0002734c84931f1d1fee08b9db544317974f6b8b9ee5adb76f4e87`  
		Last Modified: Fri, 22 Nov 2024 22:27:20 GMT  
		Size: 40.6 KB (40644 bytes)  
		MIME: application/vnd.in-toto+json

### `kibana:8.16.1` - linux; arm64 variant v8

```console
$ docker pull kibana@sha256:9e7acb4155627f28c22393035c665a25584cf572e99c49d77151146de305620d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **410.0 MB (409996531 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d452e3e905302d366dfab749cefbc8d33425ab0d23c704da3068eb846b331cb`
-	Entrypoint: `["\/bin\/tini","--"]`
-	Default Command: `["\/usr\/local\/bin\/kibana-docker"]`

```dockerfile
# Fri, 11 Oct 2024 03:39:45 GMT
ARG RELEASE
# Fri, 11 Oct 2024 03:39:45 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 11 Oct 2024 03:39:45 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 11 Oct 2024 03:39:45 GMT
LABEL org.opencontainers.image.version=20.04
# Fri, 11 Oct 2024 03:39:47 GMT
ADD file:8537b4db344382b39d669af27cd94ec0f870ceafe58c67ee54e3f9b38fb8d671 in / 
# Fri, 11 Oct 2024 03:39:47 GMT
CMD ["/bin/bash"]
# Thu, 21 Nov 2024 14:43:56 GMT
EXPOSE map[5601/tcp:{}]
# Thu, 21 Nov 2024 14:43:56 GMT
RUN for iter in {1..10}; do       export DEBIAN_FRONTEND=noninteractive &&       apt-get update  &&       apt-get upgrade -y  &&       apt-get install -y --no-install-recommends        fontconfig libnss3 curl ca-certificates &&       apt-get clean &&       rm -rf /var/lib/apt/lists/* && exit_code=0 && break || exit_code=$? && echo "apt-get error: retry $iter in 10s" &&       sleep 10;     done;     (exit $exit_code) # buildkit
# Thu, 21 Nov 2024 14:43:56 GMT
COPY --chown=1000:0 /usr/share/kibana /usr/share/kibana # buildkit
# Thu, 21 Nov 2024 14:43:56 GMT
COPY --chown=0:0 /bin/tini /bin/tini # buildkit
# Thu, 21 Nov 2024 14:43:56 GMT
COPY --chown=0:0 /usr/share/fonts/local/NotoSansCJK-Regular.ttc /usr/share/fonts/local/NotoSansCJK-Regular.ttc # buildkit
# Thu, 21 Nov 2024 14:43:56 GMT
RUN fc-cache -v # buildkit
# Thu, 21 Nov 2024 14:43:56 GMT
WORKDIR /usr/share/kibana
# Thu, 21 Nov 2024 14:43:56 GMT
RUN ln -s /usr/share/kibana /opt/kibana # buildkit
# Thu, 21 Nov 2024 14:43:56 GMT
ENV ELASTIC_CONTAINER=true
# Thu, 21 Nov 2024 14:43:56 GMT
ENV PATH=/usr/share/kibana/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 21 Nov 2024 14:43:56 GMT
COPY --chown=1000:0 config/kibana.yml /usr/share/kibana/config/kibana.yml # buildkit
# Thu, 21 Nov 2024 14:43:56 GMT
COPY bin/kibana-docker /usr/local/bin/ # buildkit
# Thu, 21 Nov 2024 14:43:56 GMT
RUN chmod g+ws /usr/share/kibana &&     find /usr/share/kibana -gid 0 -and -not -perm /g+w -exec chmod g+w {} \; # buildkit
# Thu, 21 Nov 2024 14:43:56 GMT
RUN find / -xdev -perm -4000 -exec chmod u-s {} + # buildkit
# Thu, 21 Nov 2024 14:43:56 GMT
RUN groupadd --gid 1000 kibana &&     useradd --uid 1000 --gid 1000 -G 0       --home-dir /usr/share/kibana --no-create-home       kibana # buildkit
# Thu, 21 Nov 2024 14:43:56 GMT
LABEL org.label-schema.build-date=2024-11-18T21:51:43.597Z org.label-schema.license=Elastic License org.label-schema.name=Kibana org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/kibana org.label-schema.usage=https://www.elastic.co/guide/en/kibana/reference/index.html org.label-schema.vcs-ref=c8b46e87c4d61de4fe046ce5ea0a0b68aad5acf9 org.label-schema.vcs-url=https://github.com/elastic/kibana org.label-schema.vendor=Elastic org.label-schema.version=8.16.1 org.opencontainers.image.created=2024-11-18T21:51:43.597Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/kibana/reference/index.html org.opencontainers.image.licenses=Elastic License org.opencontainers.image.revision=c8b46e87c4d61de4fe046ce5ea0a0b68aad5acf9 org.opencontainers.image.source=https://github.com/elastic/kibana org.opencontainers.image.title=Kibana org.opencontainers.image.url=https://www.elastic.co/products/kibana org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=8.16.1
# Thu, 21 Nov 2024 14:43:56 GMT
ENTRYPOINT ["/bin/tini" "--"]
# Thu, 21 Nov 2024 14:43:56 GMT
CMD ["/usr/local/bin/kibana-docker"]
# Thu, 21 Nov 2024 14:43:56 GMT
USER 1000
```

-	Layers:
	-	`sha256:1b9f3c55f9d4aa5c52eb67a4cb7d0f4726ab85a413b50e3e3fe788befce3d297`  
		Last Modified: Fri, 11 Oct 2024 04:41:30 GMT  
		Size: 26.0 MB (25973828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5615ce72569ba1d15512469e51a8912567f652afdf4f67ce8df86e055a26c182`  
		Last Modified: Mon, 18 Nov 2024 23:48:55 GMT  
		Size: 10.8 MB (10818065 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39b409364d0faea72e610f0cd83134cc8f421ea09c56f11155195e3ab835a4ee`  
		Last Modified: Fri, 22 Nov 2024 22:39:05 GMT  
		Size: 356.5 MB (356538873 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97fe55bca762601e2d11ddf23be97d01b719c223c3f0bc4302aed063a6e743cb`  
		Last Modified: Fri, 22 Nov 2024 22:38:58 GMT  
		Size: 9.1 KB (9097 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:447ba0f4f0a7a3d3b1c6030f799a243f2364446c81e551aad0e35525200c8d92`  
		Last Modified: Fri, 22 Nov 2024 22:38:59 GMT  
		Size: 16.5 MB (16460485 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8e483b95a7aa3b08845bc7d00b547558a4d4a3744dd8ca37aaf5e4c65a2886c`  
		Last Modified: Fri, 22 Nov 2024 22:38:58 GMT  
		Size: 5.3 KB (5303 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20e6384c0b839e59f38f5cd8400b77bec6765b5efdbd52fbb427a22d0ae02f02`  
		Last Modified: Fri, 22 Nov 2024 22:38:59 GMT  
		Size: 130.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58061144adaca5875d0db1f3f2d4ea6906e17b928a7b3ce79ece9f8a4fe84cca`  
		Last Modified: Fri, 22 Nov 2024 22:38:59 GMT  
		Size: 394.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9d9270968484519e50d572e5d5f17fa406777a96191002a969429309dce43a7`  
		Last Modified: Fri, 22 Nov 2024 22:39:00 GMT  
		Size: 4.7 KB (4704 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14870c37dd46589a85a047128425fa7c700c506d689e9c63fb4d1c34404d7859`  
		Last Modified: Fri, 22 Nov 2024 22:39:00 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1dfde3d9a2ab78c0e68bce005be30e0b3acac5b28a902c29b39a7afedadba7c5`  
		Last Modified: Fri, 22 Nov 2024 22:39:00 GMT  
		Size: 183.4 KB (183417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebe0788bd1a53fe8a126ee2ec298e99c57cea0d0b797a010e629446dd3e8dea8`  
		Last Modified: Fri, 22 Nov 2024 22:39:01 GMT  
		Size: 1.8 KB (1805 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kibana:8.16.1` - unknown; unknown

```console
$ docker pull kibana@sha256:e580f4749fb6d1388ee43e14bd93b79fb878d175e1f37e93f72487383775ddf8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4364920 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e141e58e99da2968ac2899210c50abf25e1213e97e83b7b4bf66ade5901dc3a2`

```dockerfile
```

-	Layers:
	-	`sha256:dcb10ceb483b232f5f4c16ae741b97f7192ab25ba3485956c346060ca9dcce13`  
		Last Modified: Fri, 22 Nov 2024 22:38:58 GMT  
		Size: 4.3 MB (4324028 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:43a639ba57f141e261ec6210b2eb2351fae2b68b6db4cc333634c7424a24fd4c`  
		Last Modified: Fri, 22 Nov 2024 22:38:58 GMT  
		Size: 40.9 KB (40892 bytes)  
		MIME: application/vnd.in-toto+json
