## `clojure:temurin-26-tools-deps-alpine`

```console
$ docker pull clojure@sha256:7c7c6c15ab45a76717b3b380b8ac91495c6b42b63bb94ec865a423c525e353e6
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-26-tools-deps-alpine` - linux; amd64

```console
$ docker pull clojure@sha256:9bb5ebe04a2dc2680ca97315bf91f6521a2afa3ce79ad0c07d698b2149e05ed8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **135.1 MB (135094924 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c417f55823053233950db220970fc86450ce26f8916e665c02d7dd42e77db9a5`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 22 Jun 2026 19:20:09 GMT
ADD alpine-minirootfs-3.23.5-x86_64.tar.gz / # buildkit
# Mon, 22 Jun 2026 19:20:09 GMT
CMD ["/bin/sh"]
# Mon, 22 Jun 2026 19:57:49 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 22 Jun 2026 19:57:49 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 22 Jun 2026 19:57:49 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 22 Jun 2026 19:57:49 GMT
RUN set -eux;     apk add --no-cache         fontconfig ttf-dejavu         ca-certificates p11-kit-trust         musl-locales musl-locales-lang         binutils         tzdata         coreutils         openssl     ;     rm -rf /var/cache/apk/* # buildkit
# Mon, 22 Jun 2026 19:57:49 GMT
ENV JAVA_VERSION=jdk-26.0.1+8
# Mon, 22 Jun 2026 19:57:58 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        aarch64)          ESUM='7e32b89349385f10d7805197c7696b46556717d041e681017b12590bae6692ca';          BINARY_URL='https://github.com/adoptium/temurin26-binaries/releases/download/jdk-26.0.1%2B8/OpenJDK26U-jdk_aarch64_alpine-linux_hotspot_26.0.1_8.tar.gz';          ;;        x86_64)          ESUM='0c97fe7e503fb6daf36a5e86e8d083b97cc2354cda4d11288e6c3b8ec0818afc';          BINARY_URL='https://github.com/adoptium/temurin26-binaries/releases/download/jdk-26.0.1%2B8/OpenJDK26U-jdk_x64_alpine-linux_hotspot_26.0.1_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     apk add --no-cache --virtual .fetch-deps gnupg;     wget -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     apk del --no-network .fetch-deps; # buildkit
# Mon, 22 Jun 2026 19:58:00 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Mon, 22 Jun 2026 19:58:00 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Mon, 22 Jun 2026 19:58:00 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Mon, 22 Jun 2026 19:58:00 GMT
CMD ["jshell"]
# Mon, 22 Jun 2026 20:25:41 GMT
ENV CLOJURE_VERSION=1.12.5.1654
# Mon, 22 Jun 2026 20:25:41 GMT
WORKDIR /tmp
# Mon, 22 Jun 2026 20:25:44 GMT
RUN apk add --no-cache curl bash make git rlwrap && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "28f81b0833c0a072f4370ae0eb1e4c5a4f9f4a34035cd7607ea9f253a8b06da1 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apk del curl # buildkit
# Mon, 22 Jun 2026 20:25:44 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Mon, 22 Jun 2026 20:25:44 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Mon, 22 Jun 2026 20:25:44 GMT
ENTRYPOINT ["entrypoint"]
# Mon, 22 Jun 2026 20:25:44 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:e6f31ffc071e5560b82a8685fba8214954e5721e3e49269d00958316edbe89fe`  
		Last Modified: Mon, 22 Jun 2026 12:03:33 GMT  
		Size: 3.8 MB (3844421 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2f2fd18a0a9bc0fb03fb517a12431b1bf11c2dd8a300797a70c469eb0573499`  
		Last Modified: Mon, 22 Jun 2026 19:58:15 GMT  
		Size: 14.3 MB (14259370 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54b896cecc272ef7121da940e2be26998d8de663b31adc1e3e4bb1cbb887ae6c`  
		Last Modified: Mon, 22 Jun 2026 19:58:17 GMT  
		Size: 93.7 MB (93726872 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46ef27f6a9817fdee68c106972c44385780e41f17b2e0f931781e6e066d03423`  
		Last Modified: Mon, 22 Jun 2026 19:58:14 GMT  
		Size: 130.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f794e94355907e9d4c3b9ac7bf794fdcc22add314a4fcd8d3c9ee0e9afed5a2`  
		Last Modified: Mon, 22 Jun 2026 19:58:06 GMT  
		Size: 2.5 KB (2463 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8e91c576e5cbf507858e9f7062e1ee707e2a4c78dfd5e2fdb2f7342cfecc6d8`  
		Last Modified: Mon, 22 Jun 2026 20:25:54 GMT  
		Size: 23.3 MB (23260616 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cad88530694936e18e61362bfe0b2463f69144271dfb87d97d619c864658dc4b`  
		Last Modified: Mon, 22 Jun 2026 20:25:53 GMT  
		Size: 618.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac389702df8816032fa28513d0fbc078422e523e67d2443e69d69f6c66244b00`  
		Last Modified: Mon, 22 Jun 2026 20:25:53 GMT  
		Size: 402.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-26-tools-deps-alpine` - unknown; unknown

```console
$ docker pull clojure@sha256:a6b6dd3b0d05fb8c3382145a14b28deb5efb665c026ae92ddb17121d50bc4dd9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.2 MB (1200346 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac94624e4522f31ea14b50f7e2f489b9778d0b5b8cd5ce371c612104e3b5e8f7`

```dockerfile
```

-	Layers:
	-	`sha256:4cd7f37ef6f31a5fdc449a036a437f1ba75e897e2bee2d738358cd28c34027d9`  
		Last Modified: Mon, 22 Jun 2026 20:25:53 GMT  
		Size: 1.2 MB (1184921 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1bab1b2f5cbb50c00f7a6dd95ca55823202e70826ee4853b0d97c4df6359f297`  
		Last Modified: Mon, 22 Jun 2026 20:25:53 GMT  
		Size: 15.4 KB (15425 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-26-tools-deps-alpine` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:373ca2412c53e86e22cda238224a8327063a47e73a77a5679452f58c925346eb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.5 MB (134546257 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b4f5f10532c8e7da0ac7c8d243ad0fdf9b5e1cb4df80280bd31e2a3de6a1af48`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 22 Jun 2026 19:19:57 GMT
ADD alpine-minirootfs-3.23.5-aarch64.tar.gz / # buildkit
# Mon, 22 Jun 2026 19:19:57 GMT
CMD ["/bin/sh"]
# Mon, 22 Jun 2026 19:58:28 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 22 Jun 2026 19:58:28 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 22 Jun 2026 19:58:28 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 22 Jun 2026 19:58:28 GMT
RUN set -eux;     apk add --no-cache         fontconfig ttf-dejavu         ca-certificates p11-kit-trust         musl-locales musl-locales-lang         binutils         tzdata         coreutils         openssl     ;     rm -rf /var/cache/apk/* # buildkit
# Mon, 22 Jun 2026 19:58:28 GMT
ENV JAVA_VERSION=jdk-26.0.1+8
# Mon, 22 Jun 2026 19:58:37 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        aarch64)          ESUM='7e32b89349385f10d7805197c7696b46556717d041e681017b12590bae6692ca';          BINARY_URL='https://github.com/adoptium/temurin26-binaries/releases/download/jdk-26.0.1%2B8/OpenJDK26U-jdk_aarch64_alpine-linux_hotspot_26.0.1_8.tar.gz';          ;;        x86_64)          ESUM='0c97fe7e503fb6daf36a5e86e8d083b97cc2354cda4d11288e6c3b8ec0818afc';          BINARY_URL='https://github.com/adoptium/temurin26-binaries/releases/download/jdk-26.0.1%2B8/OpenJDK26U-jdk_x64_alpine-linux_hotspot_26.0.1_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     apk add --no-cache --virtual .fetch-deps gnupg;     wget -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     apk del --no-network .fetch-deps; # buildkit
# Mon, 22 Jun 2026 19:58:39 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Mon, 22 Jun 2026 19:58:39 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Mon, 22 Jun 2026 19:58:39 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Mon, 22 Jun 2026 19:58:39 GMT
CMD ["jshell"]
# Mon, 22 Jun 2026 20:58:49 GMT
ENV CLOJURE_VERSION=1.12.5.1654
# Mon, 22 Jun 2026 20:58:49 GMT
WORKDIR /tmp
# Mon, 22 Jun 2026 20:58:53 GMT
RUN apk add --no-cache curl bash make git rlwrap && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "28f81b0833c0a072f4370ae0eb1e4c5a4f9f4a34035cd7607ea9f253a8b06da1 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apk del curl # buildkit
# Mon, 22 Jun 2026 20:58:53 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Mon, 22 Jun 2026 20:58:53 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Mon, 22 Jun 2026 20:58:53 GMT
ENTRYPOINT ["entrypoint"]
# Mon, 22 Jun 2026 20:58:53 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:14a4754c352fba4c6c0da8e4f01bb990463c19f7ff63e090073c385bd2bc5046`  
		Last Modified: Mon, 22 Jun 2026 12:03:31 GMT  
		Size: 4.2 MB (4181860 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:259201305cf66a45c6f9b11bf24d453317731d6a78705f78a399137c52f9e461`  
		Last Modified: Mon, 22 Jun 2026 19:58:54 GMT  
		Size: 14.3 MB (14320313 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cd1e1a965bbb185d2269d31ef27dc5dbe89fa439f174a8b7bf40b3fc7a4190d`  
		Last Modified: Mon, 22 Jun 2026 19:58:56 GMT  
		Size: 92.6 MB (92617795 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20ebddc94b4afa6b0f737e5864afd8689f7952438e252acbcc0805bd077e8b6a`  
		Last Modified: Mon, 22 Jun 2026 19:58:54 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:938f966bc6eeccc12781f72ab7be7722b25b9dd4da6076c94fd98a7d26e96618`  
		Last Modified: Mon, 22 Jun 2026 19:58:54 GMT  
		Size: 2.5 KB (2463 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85a42f0667473d7ab5fc129b5cf72749f957578e9bf1ef7e4cb771a0f20382ee`  
		Last Modified: Mon, 22 Jun 2026 20:59:02 GMT  
		Size: 23.4 MB (23422654 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08a139397877e7407e53ef9bf9fee49909328f8100488a1f6beb62cc8f9f7ee5`  
		Last Modified: Mon, 22 Jun 2026 20:59:01 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1436bb06beb718d679c07253b41f3c43ee831290d1ccbc7a661fb801a43fabf3`  
		Last Modified: Mon, 22 Jun 2026 20:59:01 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-26-tools-deps-alpine` - unknown; unknown

```console
$ docker pull clojure@sha256:56d7d8bfc477faf5bbee8e70069ec90e829c5658f5ac93cc4ed6b18fd7969ebf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1349786 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:43d534e7a4e461d157185e858b1f7f2a92bd2b8dad9274a1dd9177957e745c2d`

```dockerfile
```

-	Layers:
	-	`sha256:4e4e8e877389b254bbaed5c44639e23ccfd1d56b93041c88f418698277dab1c8`  
		Last Modified: Mon, 22 Jun 2026 20:59:01 GMT  
		Size: 1.3 MB (1334270 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fda0e74191bf2316759873c86c6f72efb3442831aa425caaacacc17c8311a89e`  
		Last Modified: Mon, 22 Jun 2026 20:59:01 GMT  
		Size: 15.5 KB (15516 bytes)  
		MIME: application/vnd.in-toto+json
