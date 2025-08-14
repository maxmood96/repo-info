## `clojure:temurin-24-alpine`

```console
$ docker pull clojure@sha256:8c0fca047d62b11ad7d2636f2c1a6b6c7e8c9636c7bef5ffda636748b50fa1cf
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-24-alpine` - linux; amd64

```console
$ docker pull clojure@sha256:2b0fb34787b3dce715a50f5934d1cc02dd87b700121ee33a5539c43322253c36
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **140.0 MB (139985949 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c7cae6fa17d50ed3ec685bc569e650428db3f63900ece47bc35906ba0887ebfb`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Sat, 07 Jun 2025 17:38:11 GMT
ADD alpine-minirootfs-3.22.1-x86_64.tar.gz / # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
CMD ["/bin/sh"]
# Sat, 07 Jun 2025 17:38:11 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 07 Jun 2025 17:38:11 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 07 Jun 2025 17:38:11 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Sat, 07 Jun 2025 17:38:11 GMT
RUN set -eux;     apk add --no-cache         fontconfig ttf-dejavu         gnupg         ca-certificates p11-kit-trust         musl-locales musl-locales-lang         binutils         tzdata         coreutils         openssl     ;     rm -rf /var/cache/apk/* # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
ENV JAVA_VERSION=jdk-24.0.2+12
# Sat, 07 Jun 2025 17:38:11 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        aarch64)          ESUM='5563867bf1abfc466c59bf3d08e9957a30666fe96fb8f9c5bae939ab11d262d5';          BINARY_URL='https://github.com/adoptium/temurin24-binaries/releases/download/jdk-24.0.2%2B12/OpenJDK24U-jdk_aarch64_alpine-linux_hotspot_24.0.2_12.tar.gz';          ;;        x86_64)          ESUM='947ba234c65cdbd4d852e8f2812334ed093530d86b32cca5d9b45d6672186f77';          BINARY_URL='https://github.com/adoptium/temurin24-binaries/releases/download/jdk-24.0.2%2B12/OpenJDK24U-jdk_x64_alpine-linux_hotspot_24.0.2_12.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Sat, 07 Jun 2025 17:38:11 GMT
CMD ["jshell"]
# Sat, 07 Jun 2025 17:38:11 GMT
ENV CLOJURE_VERSION=1.12.1.1550
# Sat, 07 Jun 2025 17:38:11 GMT
WORKDIR /tmp
# Sat, 07 Jun 2025 17:38:11 GMT
RUN apk add --no-cache curl bash make git rlwrap && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "aea202cd0573d79fd8b7db1b608762645a8f93006a86bc817ec130bed1d9707d *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apk del curl # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
ENTRYPOINT ["entrypoint"]
# Sat, 07 Jun 2025 17:38:11 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:9824c27679d3b27c5e1cb00a73adb6f4f8d556994111c12db3c5d61a0c843df8`  
		Last Modified: Tue, 15 Jul 2025 19:00:01 GMT  
		Size: 3.8 MB (3799689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd5ef2386be4a27ea92a01ef0263a3104d9355ac7f4fb22aa55e2a91eeee344e`  
		Last Modified: Mon, 04 Aug 2025 20:12:09 GMT  
		Size: 21.1 MB (21104348 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1eae701b9ed8b56a4df38c4ec9b72d1f048c6055ba56cff62e61db3768256810`  
		Last Modified: Mon, 04 Aug 2025 20:12:16 GMT  
		Size: 90.1 MB (90132918 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:939aba76ded566210b691bda00b92ffc2029071fc4984207e3c7d6dce00328d6`  
		Last Modified: Mon, 04 Aug 2025 19:25:55 GMT  
		Size: 130.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:907d1c29ddd75894bbcf074eab7ed68afbe4634ea810f2cf54368a7eec0eb6bc`  
		Last Modified: Mon, 04 Aug 2025 19:25:57 GMT  
		Size: 2.3 KB (2281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b127f26eaf7ea6fbe6b804caf1dd975a3ede236868a6f45837fe2d470a93ffcc`  
		Last Modified: Wed, 06 Aug 2025 10:30:10 GMT  
		Size: 24.9 MB (24945536 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0005799d19c658aaa5ebb4a3319b0f1d110079ebb4a9bcc4cc145d7ff545426`  
		Last Modified: Wed, 06 Aug 2025 10:30:07 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c7a5c6d8f87cfee0591785101fcdd47b6e05e2083e65ce7855ae4cfe5d1138f`  
		Last Modified: Wed, 06 Aug 2025 10:30:09 GMT  
		Size: 401.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-24-alpine` - unknown; unknown

```console
$ docker pull clojure@sha256:f4bc29724d0dfcfbb487744cdc1acd8dd4cf163d7c022440109490f188c1da84
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1261330 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d8d4023d4f0a055aab231122c60e59ed7dd6a52e91fae58ee5ec0ab32e5e4a6f`

```dockerfile
```

-	Layers:
	-	`sha256:32159d30d2d979d655dc7bf4c3077e101425a77ea099ee5e4b20878d2e39d344`  
		Last Modified: Mon, 04 Aug 2025 21:42:19 GMT  
		Size: 1.2 MB (1245862 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0c9588635cbcdf8bbfad7b0dfad602c54efcfcad2622af309cc8ba5fabcd8b99`  
		Last Modified: Mon, 04 Aug 2025 21:42:19 GMT  
		Size: 15.5 KB (15468 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-24-alpine` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:ce17767be33258a9358b6b910fb6299e10e37c120a0d63211df11a2f23c000eb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **139.5 MB (139465799 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b32891987ac4a9830d0420dca0aa578b54a19cbe5c3b546e4b5a699166bbe20c`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Sat, 07 Jun 2025 17:38:11 GMT
ADD alpine-minirootfs-3.22.1-aarch64.tar.gz / # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
CMD ["/bin/sh"]
# Sat, 07 Jun 2025 17:38:11 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 07 Jun 2025 17:38:11 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 07 Jun 2025 17:38:11 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Sat, 07 Jun 2025 17:38:11 GMT
RUN set -eux;     apk add --no-cache         fontconfig ttf-dejavu         gnupg         ca-certificates p11-kit-trust         musl-locales musl-locales-lang         binutils         tzdata         coreutils         openssl     ;     rm -rf /var/cache/apk/* # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
ENV JAVA_VERSION=jdk-24.0.2+12
# Sat, 07 Jun 2025 17:38:11 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        aarch64)          ESUM='5563867bf1abfc466c59bf3d08e9957a30666fe96fb8f9c5bae939ab11d262d5';          BINARY_URL='https://github.com/adoptium/temurin24-binaries/releases/download/jdk-24.0.2%2B12/OpenJDK24U-jdk_aarch64_alpine-linux_hotspot_24.0.2_12.tar.gz';          ;;        x86_64)          ESUM='947ba234c65cdbd4d852e8f2812334ed093530d86b32cca5d9b45d6672186f77';          BINARY_URL='https://github.com/adoptium/temurin24-binaries/releases/download/jdk-24.0.2%2B12/OpenJDK24U-jdk_x64_alpine-linux_hotspot_24.0.2_12.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Sat, 07 Jun 2025 17:38:11 GMT
CMD ["jshell"]
# Sat, 07 Jun 2025 17:38:11 GMT
ENV CLOJURE_VERSION=1.12.1.1550
# Sat, 07 Jun 2025 17:38:11 GMT
WORKDIR /tmp
# Sat, 07 Jun 2025 17:38:11 GMT
RUN apk add --no-cache curl bash make git rlwrap && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "aea202cd0573d79fd8b7db1b608762645a8f93006a86bc817ec130bed1d9707d *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apk del curl # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
ENTRYPOINT ["entrypoint"]
# Sat, 07 Jun 2025 17:38:11 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:6e174226ea690ced550e5641249a412cdbefd2d09871f3e64ab52137a54ba606`  
		Last Modified: Tue, 15 Jul 2025 18:59:50 GMT  
		Size: 4.1 MB (4130750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20a495748323e0cdac275f94a75856b53137d10e7dd79d59568fe601407fb00e`  
		Last Modified: Mon, 04 Aug 2025 19:31:51 GMT  
		Size: 21.1 MB (21148725 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f503b83c17e606e525a15bdf8c088d8b510866bd192730491923c7e09021b161`  
		Last Modified: Mon, 04 Aug 2025 19:39:38 GMT  
		Size: 89.1 MB (89116820 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4e121434e3e7ced93721c74730970c4545f0d07a1ab8a3cb707d8d97621657a`  
		Last Modified: Mon, 04 Aug 2025 19:39:33 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94585305800850d7db8da0cf8b919141fa5eb89e43d0bf4133469159f0960634`  
		Last Modified: Mon, 04 Aug 2025 19:39:33 GMT  
		Size: 2.3 KB (2280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d2da4153ce2daf5a0fa936459051dd9f27c317a80bed651ffbd596072bbb169`  
		Last Modified: Tue, 05 Aug 2025 00:01:44 GMT  
		Size: 25.1 MB (25066043 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60880e6a8e5029718e4b0806548acc48e35470506a4b936cdf3e2d5d8ba76cca`  
		Last Modified: Tue, 05 Aug 2025 00:01:42 GMT  
		Size: 619.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5b70eac9862e5100fbea28c3ef44a93d7fe14e2400a5e2198d6281268f65502`  
		Last Modified: Tue, 05 Aug 2025 00:01:42 GMT  
		Size: 402.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-24-alpine` - unknown; unknown

```console
$ docker pull clojure@sha256:20f1a9c24eadd6349d4461093af9c5756af7867e727fac20f7337b9b7878782d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.4 MB (1411422 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d0914bcbb6af0bf3299dffe1d40339c7fd23c9c73d266314decacc2035140ec8`

```dockerfile
```

-	Layers:
	-	`sha256:fcb7ce736483d3c655be8a82338e8417f10df9325ba835dfc432d02d417eef1a`  
		Last Modified: Tue, 05 Aug 2025 00:45:47 GMT  
		Size: 1.4 MB (1395861 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7823500725d22fdc700ddae5105bad5156f95328c2c6891ead1af5fdb9bd6163`  
		Last Modified: Tue, 05 Aug 2025 00:45:47 GMT  
		Size: 15.6 KB (15561 bytes)  
		MIME: application/vnd.in-toto+json
