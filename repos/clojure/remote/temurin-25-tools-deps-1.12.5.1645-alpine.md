## `clojure:temurin-25-tools-deps-1.12.5.1645-alpine`

```console
$ docker pull clojure@sha256:cd8d6b9edb33776453e20a43a57f0114c4547d99a3cf295b2c8fb2e3113265e1
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-25-tools-deps-1.12.5.1645-alpine` - linux; amd64

```console
$ docker pull clojure@sha256:2c305130c0f0b1fbc2c638d67c9f12442fa00f79b7501ae40057b4ec4635f25c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **136.2 MB (136151978 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:84496568216372a3383483134f64df1004ef731d91fa405f5a73d669b5a3ac5d`
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
# Fri, 15 May 2026 20:15:36 GMT
ENV CLOJURE_VERSION=1.12.5.1645
# Fri, 15 May 2026 20:15:36 GMT
WORKDIR /tmp
# Fri, 15 May 2026 20:15:39 GMT
RUN apk add --no-cache curl bash make git rlwrap && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "3d6e8428fd4c7f76de9f87f77b2347f293109f4e88fb20c154b3fa34a7f687dd *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apk del curl # buildkit
# Fri, 15 May 2026 20:15:39 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 15 May 2026 20:15:39 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 15 May 2026 20:15:39 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 15 May 2026 20:15:39 GMT
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
	-	`sha256:60d3c363025318ee83d02e48ae7f6e6259d76424a8a51bb94fc4fbe8edf4c42a`  
		Last Modified: Fri, 15 May 2026 20:15:49 GMT  
		Size: 26.4 MB (26353751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4ca7ab2b23602c1f75fe263ac57bb8f5431bd36845f6d51db1a1d877a5197a0`  
		Last Modified: Fri, 15 May 2026 20:15:48 GMT  
		Size: 619.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:edcd52fd4ad844878b1164b3400303948cef8c9f1f84711ff4597c09fe9ac2dc`  
		Last Modified: Fri, 15 May 2026 20:15:48 GMT  
		Size: 402.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-tools-deps-1.12.5.1645-alpine` - unknown; unknown

```console
$ docker pull clojure@sha256:f73918874aeb7049da1c662bf29660ca0c321eb0f4e8b87162c03d824e21bd57
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.2 MB (1222574 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d8f177a23dc6803677a5a574689802747350bbe9946020d14b2cd5eb25dbdde2`

```dockerfile
```

-	Layers:
	-	`sha256:970476c03eeafe6da4cb6d6c2a5ae6d63afaae3fd44f3008e7cda424b7babcbe`  
		Last Modified: Fri, 15 May 2026 20:15:48 GMT  
		Size: 1.2 MB (1207149 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e4b788d76893bd40c5e12bf94e0b3704e09792ebe3003c6903adbcc79d0d6015`  
		Last Modified: Fri, 15 May 2026 20:15:48 GMT  
		Size: 15.4 KB (15425 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-25-tools-deps-1.12.5.1645-alpine` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:e01b90d08b9baafa6dd9cd172abaa262aa76731ec9a83564b6831079e2005d37
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **135.7 MB (135654801 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:90df3d777c30172735aa059260ecfb95259a51d5c4db4a876196c06800815756`
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
# Fri, 15 May 2026 20:15:37 GMT
ENV CLOJURE_VERSION=1.12.5.1645
# Fri, 15 May 2026 20:15:37 GMT
WORKDIR /tmp
# Fri, 15 May 2026 20:15:40 GMT
RUN apk add --no-cache curl bash make git rlwrap && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "3d6e8428fd4c7f76de9f87f77b2347f293109f4e88fb20c154b3fa34a7f687dd *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apk del curl # buildkit
# Fri, 15 May 2026 20:15:40 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 15 May 2026 20:15:40 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 15 May 2026 20:15:40 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 15 May 2026 20:15:40 GMT
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
	-	`sha256:5b725b92f3ab6a41d69171bbf838a8908f896eeda0702631aa8cab3f7aa71f37`  
		Last Modified: Fri, 15 May 2026 20:15:49 GMT  
		Size: 26.5 MB (26515389 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3e8b3199e19a4a3021c2a0cd87e8094d53d77f95cdb28a1e9839a83ed4119ca`  
		Last Modified: Fri, 15 May 2026 20:15:49 GMT  
		Size: 618.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0958b00f7b39538bbc296f5f48fc22cabecaf5acdc090614b68b2356381659a8`  
		Last Modified: Fri, 15 May 2026 20:15:49 GMT  
		Size: 401.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-tools-deps-1.12.5.1645-alpine` - unknown; unknown

```console
$ docker pull clojure@sha256:529dbcb59f00375a2788b2f8d47e086f41539ed8fa9b3063e94ca7684a3fc534
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.4 MB (1372014 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:06ad8fbaf4cea5441c840a866f4f5b9da43f88dc8040c0ffe6993a4121dcc25b`

```dockerfile
```

-	Layers:
	-	`sha256:8c94df7722daf643b77e2e2a7146a4514aac83dc161385893f98022104820b21`  
		Last Modified: Fri, 15 May 2026 20:15:49 GMT  
		Size: 1.4 MB (1356498 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:921ddb96792840e46c337f7700c84e9becc54f8d03f8fd78af3eccb9e69027d5`  
		Last Modified: Fri, 15 May 2026 20:15:48 GMT  
		Size: 15.5 KB (15516 bytes)  
		MIME: application/vnd.in-toto+json
