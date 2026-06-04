## `clojure:temurin-26-tools-deps-1.12.5.1654-alpine`

```console
$ docker pull clojure@sha256:6b13a5b9eff8ccd11fe5d84e1df0643e54f5202cca261edeef69b87c85969479
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-26-tools-deps-1.12.5.1654-alpine` - linux; amd64

```console
$ docker pull clojure@sha256:311da25afc3a5f21fa023251d79b13a4f2d4eae625a9f9f1769020a290753f26
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **135.2 MB (135163559 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:00d02bd2bb654acb6c102b7c55ec6e833416f8883280f1f0acf713241adf2124`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:40 GMT
ADD alpine-minirootfs-3.23.4-x86_64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:40 GMT
CMD ["/bin/sh"]
# Fri, 15 May 2026 20:28:55 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 15 May 2026 20:28:55 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 15 May 2026 20:28:55 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 15 May 2026 20:28:55 GMT
RUN set -eux;     apk add --no-cache         fontconfig ttf-dejavu         ca-certificates p11-kit-trust         musl-locales musl-locales-lang         binutils         tzdata         coreutils         openssl     ;     rm -rf /var/cache/apk/* # buildkit
# Fri, 15 May 2026 20:28:55 GMT
ENV JAVA_VERSION=jdk-26.0.1+8
# Fri, 15 May 2026 20:29:03 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        aarch64)          ESUM='7e32b89349385f10d7805197c7696b46556717d041e681017b12590bae6692ca';          BINARY_URL='https://github.com/adoptium/temurin26-binaries/releases/download/jdk-26.0.1%2B8/OpenJDK26U-jdk_aarch64_alpine-linux_hotspot_26.0.1_8.tar.gz';          ;;        x86_64)          ESUM='0c97fe7e503fb6daf36a5e86e8d083b97cc2354cda4d11288e6c3b8ec0818afc';          BINARY_URL='https://github.com/adoptium/temurin26-binaries/releases/download/jdk-26.0.1%2B8/OpenJDK26U-jdk_x64_alpine-linux_hotspot_26.0.1_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     apk add --no-cache --virtual .fetch-deps gnupg;     wget -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     apk del --no-network .fetch-deps; # buildkit
# Fri, 15 May 2026 20:29:04 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Fri, 15 May 2026 20:29:04 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Fri, 15 May 2026 20:29:04 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Fri, 15 May 2026 20:29:04 GMT
CMD ["jshell"]
# Thu, 04 Jun 2026 17:47:35 GMT
ENV CLOJURE_VERSION=1.12.5.1654
# Thu, 04 Jun 2026 17:47:35 GMT
WORKDIR /tmp
# Thu, 04 Jun 2026 17:47:38 GMT
RUN apk add --no-cache curl bash make git rlwrap && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "28f81b0833c0a072f4370ae0eb1e4c5a4f9f4a34035cd7607ea9f253a8b06da1 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apk del curl # buildkit
# Thu, 04 Jun 2026 17:47:38 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 04 Jun 2026 17:47:38 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 04 Jun 2026 17:47:38 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 04 Jun 2026 17:47:38 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:6a0ac1617861a677b045b7ff88545213ec31c0ff08763195a70a4a5adda577bb`  
		Last Modified: Wed, 15 Apr 2026 20:01:46 GMT  
		Size: 3.9 MB (3864189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e081e96822532a01c7bb1e027265fed4b4c27a2e1d696c326f173f3cc1223765`  
		Last Modified: Fri, 15 May 2026 20:29:20 GMT  
		Size: 14.3 MB (14307105 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbaa5d5be003b1eed063c02fb86d96eed583ae248613b526315e1da79db26c33`  
		Last Modified: Fri, 15 May 2026 20:29:22 GMT  
		Size: 93.7 MB (93726947 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e549ff0e96b732aa8f90eae5e53676271da5ac10a0fd38c6b26da9ff83ce4aae`  
		Last Modified: Fri, 15 May 2026 20:29:19 GMT  
		Size: 130.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:521a9ec0292e87558350138ddd287318bfa3975e6531bc92f1c86438baf45fe9`  
		Last Modified: Fri, 15 May 2026 20:29:20 GMT  
		Size: 2.5 KB (2461 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09460b02ba273383a950e182724e4a0a44eb938811035ab57109d69f00734db0`  
		Last Modified: Thu, 04 Jun 2026 17:47:48 GMT  
		Size: 23.3 MB (23261675 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e881f35c539561b039576fc79d8764056268b6368214132f464d91462d9e733a`  
		Last Modified: Thu, 04 Jun 2026 17:47:47 GMT  
		Size: 619.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e88295ad6521d12a10e1dc78894d46709b5e65bab0048df504f240a33e88561`  
		Last Modified: Thu, 04 Jun 2026 17:47:47 GMT  
		Size: 401.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-26-tools-deps-1.12.5.1654-alpine` - unknown; unknown

```console
$ docker pull clojure@sha256:3a636c5dd4d65acf6e66947ff9df768c3449e72fc03811e6f0bbe51f25363480
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.2 MB (1217238 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:608dd03ea9a4a4dae6466c7cb0a3be9a03c612b34cf382c1d0a2469408e4ec57`

```dockerfile
```

-	Layers:
	-	`sha256:c3eda4aad9be199103c535347be67135f1bea7b81d40ea03106fe5d9d817e85e`  
		Last Modified: Thu, 04 Jun 2026 17:47:47 GMT  
		Size: 1.2 MB (1201813 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b1aefc330450c6677fad2d700557ee2d2eff2b6f7a38c52e18c3aad9b092ff56`  
		Last Modified: Thu, 04 Jun 2026 17:47:48 GMT  
		Size: 15.4 KB (15425 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-26-tools-deps-1.12.5.1654-alpine` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:ebbe7b2988792f5ca450a0490ea19c185d4d1b1609d760ae2f5dd0553d117b74
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.6 MB (134611915 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7f4cf63a0b6cd88b55d85d150113c2a555d13e0f30425738eadf5526e02225b5`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:25 GMT
ADD alpine-minirootfs-3.23.4-aarch64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:25 GMT
CMD ["/bin/sh"]
# Fri, 15 May 2026 20:28:32 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 15 May 2026 20:28:32 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 15 May 2026 20:28:32 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 15 May 2026 20:28:32 GMT
RUN set -eux;     apk add --no-cache         fontconfig ttf-dejavu         ca-certificates p11-kit-trust         musl-locales musl-locales-lang         binutils         tzdata         coreutils         openssl     ;     rm -rf /var/cache/apk/* # buildkit
# Fri, 15 May 2026 20:28:32 GMT
ENV JAVA_VERSION=jdk-26.0.1+8
# Fri, 15 May 2026 20:28:42 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        aarch64)          ESUM='7e32b89349385f10d7805197c7696b46556717d041e681017b12590bae6692ca';          BINARY_URL='https://github.com/adoptium/temurin26-binaries/releases/download/jdk-26.0.1%2B8/OpenJDK26U-jdk_aarch64_alpine-linux_hotspot_26.0.1_8.tar.gz';          ;;        x86_64)          ESUM='0c97fe7e503fb6daf36a5e86e8d083b97cc2354cda4d11288e6c3b8ec0818afc';          BINARY_URL='https://github.com/adoptium/temurin26-binaries/releases/download/jdk-26.0.1%2B8/OpenJDK26U-jdk_x64_alpine-linux_hotspot_26.0.1_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     apk add --no-cache --virtual .fetch-deps gnupg;     wget -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     apk del --no-network .fetch-deps; # buildkit
# Fri, 15 May 2026 20:28:43 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Fri, 15 May 2026 20:28:43 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Fri, 15 May 2026 20:28:43 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Fri, 15 May 2026 20:28:43 GMT
CMD ["jshell"]
# Thu, 04 Jun 2026 17:47:23 GMT
ENV CLOJURE_VERSION=1.12.5.1654
# Thu, 04 Jun 2026 17:47:23 GMT
WORKDIR /tmp
# Thu, 04 Jun 2026 17:47:27 GMT
RUN apk add --no-cache curl bash make git rlwrap && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "28f81b0833c0a072f4370ae0eb1e4c5a4f9f4a34035cd7607ea9f253a8b06da1 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apk del curl # buildkit
# Thu, 04 Jun 2026 17:47:27 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 04 Jun 2026 17:47:27 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 04 Jun 2026 17:47:27 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 04 Jun 2026 17:47:27 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:d17f077ada118cc762df373ff803592abf2dfa3ddafaa7381e364dd27a88fca7`  
		Last Modified: Wed, 15 Apr 2026 20:01:32 GMT  
		Size: 4.2 MB (4199870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:663c281b02178500cc2405957896cb4b2c901f353ce59d8c702000b44a4eb4cb`  
		Last Modified: Fri, 15 May 2026 20:28:59 GMT  
		Size: 14.4 MB (14365440 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8478f678d308c7c3dd2a812916604bc76952d2cbdd6cbfed048df7d43bd35b55`  
		Last Modified: Fri, 15 May 2026 20:29:01 GMT  
		Size: 92.6 MB (92619253 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d36508231094e13df0969686478e5f11986327f94f6c60eac3a91ccd402da86b`  
		Last Modified: Fri, 15 May 2026 20:28:58 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6dd0378873387f971dd8030f59afc279b6de616979cc085f74c1a3b2f5bde1dc`  
		Last Modified: Fri, 15 May 2026 20:28:59 GMT  
		Size: 2.5 KB (2462 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1350e2079b79562da2cca26d2238ddba3bcfca9d4dab93218aff13c835c707a5`  
		Last Modified: Thu, 04 Jun 2026 17:47:36 GMT  
		Size: 23.4 MB (23423712 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71625927b93ddab45e473fb6eb9d6029f24e780f9eaaf57c1f82e45715c19001`  
		Last Modified: Thu, 04 Jun 2026 17:47:36 GMT  
		Size: 616.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fb50ed3a74dfa45525b9e1ab6ea3dc47b50e3405fa12b395ca1938d09a22649`  
		Last Modified: Thu, 04 Jun 2026 17:47:36 GMT  
		Size: 402.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-26-tools-deps-1.12.5.1654-alpine` - unknown; unknown

```console
$ docker pull clojure@sha256:c2f3ea7bf04c82b03f8e8f1f296918932e54108752d4e114376d0e5bf09fd6d3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.4 MB (1366679 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef8d7c83c9683876782a63d28b9f2e4f8566e26406b9f0dc402cb3289c55ebb4`

```dockerfile
```

-	Layers:
	-	`sha256:567c08ab7da6cee092cb5740c15fb263f4d709816542f5a82bff2c22794f12cc`  
		Last Modified: Thu, 04 Jun 2026 17:47:36 GMT  
		Size: 1.4 MB (1351162 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d78224816a9d15add4765b612b0808fe1d2f6537c4db0bf7f673c31ae898abfb`  
		Last Modified: Thu, 04 Jun 2026 17:47:35 GMT  
		Size: 15.5 KB (15517 bytes)  
		MIME: application/vnd.in-toto+json
