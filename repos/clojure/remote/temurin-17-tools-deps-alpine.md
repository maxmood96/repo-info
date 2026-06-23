## `clojure:temurin-17-tools-deps-alpine`

```console
$ docker pull clojure@sha256:dfa9965557421f575803c973bc6ef20caa0a80ee37c106d0faba112c9f453495
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `clojure:temurin-17-tools-deps-alpine` - linux; amd64

```console
$ docker pull clojure@sha256:86d2894b2aa8b63166c7bc0b9f07c41452abb1dd316795c5cf2adff40992e06b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **192.4 MB (192410040 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3c4d6a340542d7f1ecbebcab4046437602fe314ce642d7365064cc282228869`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 22 Jun 2026 19:20:09 GMT
ADD alpine-minirootfs-3.23.5-x86_64.tar.gz / # buildkit
# Mon, 22 Jun 2026 19:20:09 GMT
CMD ["/bin/sh"]
# Mon, 22 Jun 2026 19:56:53 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 22 Jun 2026 19:56:53 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 22 Jun 2026 19:56:53 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 22 Jun 2026 19:56:53 GMT
RUN set -eux;     apk add --no-cache         fontconfig ttf-dejavu         gnupg         ca-certificates p11-kit-trust         musl-locales musl-locales-lang         binutils         tzdata         coreutils         openssl     ;     rm -rf /var/cache/apk/* # buildkit
# Mon, 22 Jun 2026 19:56:53 GMT
ENV JAVA_VERSION=jdk-17.0.19+10
# Mon, 22 Jun 2026 19:57:01 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        x86_64)          ESUM='960b4090b75a887bb21a915a294bee3a97cd11876967c95e5bd29d9ec4812e17';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.19%2B10/OpenJDK17U-jdk_x64_alpine-linux_hotspot_17.0.19_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Mon, 22 Jun 2026 19:57:02 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Mon, 22 Jun 2026 19:57:02 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Mon, 22 Jun 2026 19:57:02 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Mon, 22 Jun 2026 19:57:02 GMT
CMD ["jshell"]
# Mon, 22 Jun 2026 20:24:45 GMT
ENV CLOJURE_VERSION=1.12.5.1654
# Mon, 22 Jun 2026 20:24:45 GMT
WORKDIR /tmp
# Mon, 22 Jun 2026 20:24:48 GMT
RUN apk add --no-cache curl bash make git rlwrap && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "28f81b0833c0a072f4370ae0eb1e4c5a4f9f4a34035cd7607ea9f253a8b06da1 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apk del curl # buildkit
# Mon, 22 Jun 2026 20:24:48 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Mon, 22 Jun 2026 20:24:48 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Mon, 22 Jun 2026 20:24:48 GMT
ENTRYPOINT ["entrypoint"]
# Mon, 22 Jun 2026 20:24:48 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:e6f31ffc071e5560b82a8685fba8214954e5721e3e49269d00958316edbe89fe`  
		Last Modified: Mon, 22 Jun 2026 12:03:33 GMT  
		Size: 3.8 MB (3844421 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb24b7abeaf5ce9e23187de02071382730c0873637800e8a9adcb59301992717`  
		Last Modified: Mon, 22 Jun 2026 19:57:16 GMT  
		Size: 21.3 MB (21290166 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca9a403ef070b145efc0a24ea5ea18c62cf96257bfefd784d70237ec8671df1f`  
		Last Modified: Mon, 22 Jun 2026 19:57:19 GMT  
		Size: 145.1 MB (145051633 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8954f1747c4e5c426ae38631e95b0494950eb78209f25ea413a0d591f5bfd8b0`  
		Last Modified: Mon, 22 Jun 2026 19:57:15 GMT  
		Size: 130.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76f47b51787bf9ee6cbfe3b6ad72acc64ab2cd047c11d06a156720b184193e59`  
		Last Modified: Mon, 22 Jun 2026 19:57:15 GMT  
		Size: 2.3 KB (2280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:372e2a99e00fc6811b332e34332f2afb67a8993fe1b4781c0e0e67a65f454ded`  
		Last Modified: Mon, 22 Jun 2026 20:24:57 GMT  
		Size: 22.2 MB (22220362 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d67369f2eaffde0782a596f45583233434ad9f73f6c1a6050fe8420d1d22109`  
		Last Modified: Mon, 22 Jun 2026 20:24:57 GMT  
		Size: 616.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c7691a3b5d927390468a05650bc6b1034669d9a542b694b0d2e8284d9c67fe5`  
		Last Modified: Mon, 22 Jun 2026 20:24:57 GMT  
		Size: 400.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-alpine` - unknown; unknown

```console
$ docker pull clojure@sha256:a1168eaa767b70d4e3858782d7a7aa9c7f30ed56a972dc4670034cbb444cef87
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1302836 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:afc21d725a94dbe5adf5d466d97dcdfbb77be00e22b2a75782acbc5c30cb623c`

```dockerfile
```

-	Layers:
	-	`sha256:c36ddcb7fc6581efbccc414c5cdb3b9683382e17330072ad511b5e08b3067e72`  
		Last Modified: Mon, 22 Jun 2026 20:24:57 GMT  
		Size: 1.3 MB (1287404 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1c285d80a8b23d2fe3fd37141b322730bb95c99f3cff67a9bcfecccb1245f2e2`  
		Last Modified: Mon, 22 Jun 2026 20:24:57 GMT  
		Size: 15.4 KB (15432 bytes)  
		MIME: application/vnd.in-toto+json
