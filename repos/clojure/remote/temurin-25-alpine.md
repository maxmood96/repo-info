## `clojure:temurin-25-alpine`

```console
$ docker pull clojure@sha256:cfa7ab18dfb4cf75cd48a0c2ffdd7a82162e7367b4230dbc2d11938e2d5490f6
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-25-alpine` - linux; amd64

```console
$ docker pull clojure@sha256:dfe0c5044f25d923f93525a4f7a7884e8136a7813912c0d45e5499e72295e932
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **136.2 MB (136233399 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a8926eb664c6f670c51250f4aaa72ea073406fc728c96b5d699d46d70267d25`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:40 GMT
ADD alpine-minirootfs-3.23.4-x86_64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:40 GMT
CMD ["/bin/sh"]
# Thu, 30 Apr 2026 23:26:24 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 30 Apr 2026 23:26:24 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 30 Apr 2026 23:26:24 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 30 Apr 2026 23:26:24 GMT
RUN set -eux;     apk add --no-cache         fontconfig ttf-dejavu         ca-certificates p11-kit-trust         musl-locales musl-locales-lang         binutils         tzdata         coreutils         openssl     ;     rm -rf /var/cache/apk/* # buildkit
# Thu, 30 Apr 2026 23:26:24 GMT
ENV JAVA_VERSION=jdk-25.0.3+9
# Thu, 30 Apr 2026 23:26:31 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        aarch64)          ESUM='6ed368e93049d3b188c045fce0b20953bbea92fe0614dbbf4d3fd8daad7be3b2';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.3%2B9/OpenJDK25U-jdk_aarch64_alpine-linux_hotspot_25.0.3_9.tar.gz';          ;;        x86_64)          ESUM='51c2415b370aac7c3796b0c4663c8fcf91bc22d76f03df95b25fa5667cb5fdd8';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.3%2B9/OpenJDK25U-jdk_x64_alpine-linux_hotspot_25.0.3_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     apk add --no-cache --virtual .fetch-deps gnupg;     wget -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     apk del --no-network .fetch-deps; # buildkit
# Thu, 30 Apr 2026 23:26:33 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 30 Apr 2026 23:26:33 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 30 Apr 2026 23:26:33 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 30 Apr 2026 23:26:33 GMT
CMD ["jshell"]
# Thu, 14 May 2026 23:36:02 GMT
ENV CLOJURE_VERSION=1.12.5.1638
# Thu, 14 May 2026 23:36:02 GMT
WORKDIR /tmp
# Thu, 14 May 2026 23:36:05 GMT
RUN apk add --no-cache curl bash make git rlwrap && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "bccfca8c437514786f0827a11195b89b833357b2a668091f4321b451b2e36df5 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apk del curl # buildkit
# Thu, 14 May 2026 23:36:05 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 14 May 2026 23:36:05 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 14 May 2026 23:36:05 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 14 May 2026 23:36:05 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:6a0ac1617861a677b045b7ff88545213ec31c0ff08763195a70a4a5adda577bb`  
		Last Modified: Wed, 15 Apr 2026 20:01:46 GMT  
		Size: 3.9 MB (3864189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbcd71e97d819f54817ede73936d3ba8e0e56a42c8dec6fffa3dcf0a5f0b4cd7`  
		Last Modified: Thu, 30 Apr 2026 23:26:47 GMT  
		Size: 14.3 MB (14307043 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:069decb9687a1d107c70cc1f3b39e28717aee5b68017f656ac233f17fabf3d80`  
		Last Modified: Thu, 30 Apr 2026 23:26:49 GMT  
		Size: 91.6 MB (91623532 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18b72908a207a549bc818ba092166eeb02f65c17134d611b1f98600452d5217e`  
		Last Modified: Thu, 30 Apr 2026 23:26:47 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2a11818993d9767c2a1269e3b83ea425a7dbc1d260bf8e8e208ef3eb39c4234`  
		Last Modified: Thu, 30 Apr 2026 23:26:47 GMT  
		Size: 2.3 KB (2281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cda3308e4d282231ca1662a43c4ee73083286f3e9293beb05bea368fd0e329a6`  
		Last Modified: Thu, 14 May 2026 23:36:14 GMT  
		Size: 26.4 MB (26435173 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dfecd310c5fc15cfb42056ce34c37615d11a0022fe504f95cc76714788ba5da2`  
		Last Modified: Thu, 14 May 2026 23:36:14 GMT  
		Size: 619.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63dc66fed45da52d95a07e3336bf4f1273db779f41236b4d62b1b859dcdcec34`  
		Last Modified: Thu, 14 May 2026 23:36:14 GMT  
		Size: 401.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-alpine` - unknown; unknown

```console
$ docker pull clojure@sha256:f5a77193f5a349a4e1cbe2c2fb9be93ce1560bf0978c1eb75c36ef0425252efa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.2 MB (1224168 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:98d97cb042b0e38a76133d3486ca7aa8c2ef52f4f322d0048cb99db857882b7f`

```dockerfile
```

-	Layers:
	-	`sha256:71d03d057a28622e4f45d9ab4fbbf96301fa35b23b8fb61404fddd44d209956c`  
		Last Modified: Thu, 14 May 2026 23:36:14 GMT  
		Size: 1.2 MB (1208743 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:48f464a24f1d66f8deb1b0dc124aea41d519944579153397fc9392c11e79440a`  
		Last Modified: Thu, 14 May 2026 23:36:13 GMT  
		Size: 15.4 KB (15425 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-25-alpine` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:e4ecb96833e8707b870672b6a808431f2749118b39ef6f0f2bace5e7e4a0f565
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **135.7 MB (135736319 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dbf6bd2f3cbaea854a63dc996b4018876e7d36a881091283c199eaf8b601ec95`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:25 GMT
ADD alpine-minirootfs-3.23.4-aarch64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:25 GMT
CMD ["/bin/sh"]
# Thu, 30 Apr 2026 23:27:10 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 30 Apr 2026 23:27:10 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 30 Apr 2026 23:27:10 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 30 Apr 2026 23:27:10 GMT
RUN set -eux;     apk add --no-cache         fontconfig ttf-dejavu         ca-certificates p11-kit-trust         musl-locales musl-locales-lang         binutils         tzdata         coreutils         openssl     ;     rm -rf /var/cache/apk/* # buildkit
# Thu, 30 Apr 2026 23:27:10 GMT
ENV JAVA_VERSION=jdk-25.0.3+9
# Thu, 30 Apr 2026 23:27:18 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        aarch64)          ESUM='6ed368e93049d3b188c045fce0b20953bbea92fe0614dbbf4d3fd8daad7be3b2';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.3%2B9/OpenJDK25U-jdk_aarch64_alpine-linux_hotspot_25.0.3_9.tar.gz';          ;;        x86_64)          ESUM='51c2415b370aac7c3796b0c4663c8fcf91bc22d76f03df95b25fa5667cb5fdd8';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.3%2B9/OpenJDK25U-jdk_x64_alpine-linux_hotspot_25.0.3_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     apk add --no-cache --virtual .fetch-deps gnupg;     wget -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     apk del --no-network .fetch-deps; # buildkit
# Thu, 30 Apr 2026 23:27:20 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 30 Apr 2026 23:27:20 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 30 Apr 2026 23:27:20 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 30 Apr 2026 23:27:20 GMT
CMD ["jshell"]
# Thu, 14 May 2026 23:36:02 GMT
ENV CLOJURE_VERSION=1.12.5.1638
# Thu, 14 May 2026 23:36:02 GMT
WORKDIR /tmp
# Thu, 14 May 2026 23:36:06 GMT
RUN apk add --no-cache curl bash make git rlwrap && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "bccfca8c437514786f0827a11195b89b833357b2a668091f4321b451b2e36df5 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apk del curl # buildkit
# Thu, 14 May 2026 23:36:06 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 14 May 2026 23:36:06 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 14 May 2026 23:36:06 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 14 May 2026 23:36:06 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:d17f077ada118cc762df373ff803592abf2dfa3ddafaa7381e364dd27a88fca7`  
		Last Modified: Wed, 15 Apr 2026 20:01:32 GMT  
		Size: 4.2 MB (4199870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0efb54362f71a4de98d9ab1446a3a15f82375b426469238870ae07f85f0cf6c0`  
		Last Modified: Thu, 30 Apr 2026 23:27:36 GMT  
		Size: 14.4 MB (14365384 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6641ca90ca6a66c761ef0829dcdd74acc577f377e8239e611764f58e2a21ba3`  
		Last Modified: Thu, 30 Apr 2026 23:27:38 GMT  
		Size: 90.6 MB (90570695 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:538f2e9dbb24a3c1b3ea622a48cd011aa7bd60814a36dd76839ffd9293cb51f2`  
		Last Modified: Thu, 30 Apr 2026 23:27:35 GMT  
		Size: 131.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4d40a550ae76fe4e3f445bfdd07b594be44e2c12492b1425c709e312127b5a1`  
		Last Modified: Thu, 30 Apr 2026 23:27:35 GMT  
		Size: 2.3 KB (2281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59494fd37a33187c4e5c49c203bdbeaf9bd3f247697257e73cc1ef43497c901f`  
		Last Modified: Thu, 14 May 2026 23:36:15 GMT  
		Size: 26.6 MB (26596904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d375ac84897e8dc506997bc6ed39b8d21b8751e8bffba676da550fa74d28c600`  
		Last Modified: Thu, 14 May 2026 23:36:15 GMT  
		Size: 619.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3055a7784545a2b6d89c4c6fafe8060b7b081bf52ff9e1ec82185d084bb7437e`  
		Last Modified: Thu, 14 May 2026 23:36:14 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-alpine` - unknown; unknown

```console
$ docker pull clojure@sha256:a3f898946b9f2988a8aff841d2f0b0877462f05ec390afaf43f72c2c3bc7702b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.4 MB (1373608 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:14a011b14b87c8f4d909664bd07fe60313f49419ee08ed03a8b97894a7f91283`

```dockerfile
```

-	Layers:
	-	`sha256:581fd082519b11c63f9cebf7885eafb2c256117fb61de7847c8a2d6ef98cfdc5`  
		Last Modified: Thu, 14 May 2026 23:36:15 GMT  
		Size: 1.4 MB (1358092 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b97506b653e01da1e121dd42814057997e8e3419ba1c9b30611218bdceb45fa2`  
		Last Modified: Thu, 14 May 2026 23:36:14 GMT  
		Size: 15.5 KB (15516 bytes)  
		MIME: application/vnd.in-toto+json
