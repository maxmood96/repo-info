## `clojure:temurin-25-tools-deps-1.12.5.1654-alpine`

```console
$ docker pull clojure@sha256:b801a113aa73f202d034ec701e6825cc2a9ea279f2a9448589cb394c932a5e40
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-25-tools-deps-1.12.5.1654-alpine` - linux; amd64

```console
$ docker pull clojure@sha256:35e2b401013330345921f62f81ac9e2ebaeb69c0ada7d4a4155ec962c2725664
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **133.1 MB (133059935 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9cdc48e2b813720727e710bbf17aab2ddd0c40ec1a784bac17549deac1f2a264`
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
# Thu, 04 Jun 2026 17:47:01 GMT
ENV CLOJURE_VERSION=1.12.5.1654
# Thu, 04 Jun 2026 17:47:01 GMT
WORKDIR /tmp
# Thu, 04 Jun 2026 17:47:04 GMT
RUN apk add --no-cache curl bash make git rlwrap && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "28f81b0833c0a072f4370ae0eb1e4c5a4f9f4a34035cd7607ea9f253a8b06da1 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apk del curl # buildkit
# Thu, 04 Jun 2026 17:47:04 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 04 Jun 2026 17:47:04 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 04 Jun 2026 17:47:04 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 04 Jun 2026 17:47:04 GMT
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
	-	`sha256:b9890b30cbf816c606c80821dd5b857951acb91b0aa41f2a47ffbf63ed14d9a4`  
		Last Modified: Thu, 04 Jun 2026 17:47:14 GMT  
		Size: 23.3 MB (23261706 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1846a9a343184bb88d931f07c20a8ffd49db7c27135fa9153e7d31f1075f2d93`  
		Last Modified: Thu, 04 Jun 2026 17:47:13 GMT  
		Size: 620.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8756799de7df8d7152331cf39c8ed0373a28572b3eb109d268d6e5eb9b519891`  
		Last Modified: Thu, 04 Jun 2026 17:47:13 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-tools-deps-1.12.5.1654-alpine` - unknown; unknown

```console
$ docker pull clojure@sha256:7cce7fd942a4f81c7e15724c2dd5ef7edc7dd145b7ab2610091cfa2a11298f14
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.2 MB (1219741 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa8d430f2beb967ab0018ab57a76e36dbde6ff0a1b24352ec616a86883d1047d`

```dockerfile
```

-	Layers:
	-	`sha256:2b60d2f8bf0fdf0b4c433b07d566a7f9908b2747909bcac87ad0b31b6813d986`  
		Last Modified: Thu, 04 Jun 2026 17:47:13 GMT  
		Size: 1.2 MB (1204316 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:611f86d1203cee26ede3cb382a1c940acf3d06df5034a7425a4aa81ea55c9d0d`  
		Last Modified: Thu, 04 Jun 2026 17:47:13 GMT  
		Size: 15.4 KB (15425 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-25-tools-deps-1.12.5.1654-alpine` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:1cb1bc4e118f8500a7ad347c6c63941166b7305e6d1c8c21a9c56722e8ce4b77
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **132.6 MB (132563135 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:75e4addc3fa554593fd77740a0aa047b51a217dcb3bfc4946480168eab5004c7`
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
# Thu, 04 Jun 2026 17:46:41 GMT
ENV CLOJURE_VERSION=1.12.5.1654
# Thu, 04 Jun 2026 17:46:41 GMT
WORKDIR /tmp
# Thu, 04 Jun 2026 17:46:44 GMT
RUN apk add --no-cache curl bash make git rlwrap && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "28f81b0833c0a072f4370ae0eb1e4c5a4f9f4a34035cd7607ea9f253a8b06da1 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apk del curl # buildkit
# Thu, 04 Jun 2026 17:46:44 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 04 Jun 2026 17:46:44 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 04 Jun 2026 17:46:44 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 04 Jun 2026 17:46:44 GMT
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
	-	`sha256:717fe558ce5ee9052ec76ec5dec91883302fdff788256276cceeee959e0bb9a3`  
		Last Modified: Thu, 04 Jun 2026 17:46:53 GMT  
		Size: 23.4 MB (23423718 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:276a11d99e8a0c062f5f637a28f18cf72e23c624c88c7faafe41a5d77ec27bf7`  
		Last Modified: Thu, 04 Jun 2026 17:46:52 GMT  
		Size: 620.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4af2b02c11d25af4840ef23343824e4482b17d95842b1a9e87e7a685b0492bd`  
		Last Modified: Thu, 04 Jun 2026 17:46:53 GMT  
		Size: 404.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-tools-deps-1.12.5.1654-alpine` - unknown; unknown

```console
$ docker pull clojure@sha256:ee20ed74612d5dcc91f69626206f524232e11f4078801c5b57d3760a8852edaf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.4 MB (1369182 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a0d983cd7cd661f0344d33377d800508092bd13371d14ccf752591ecaae5905`

```dockerfile
```

-	Layers:
	-	`sha256:71bbca52b834a5565333f7fdc75d746e418accb48681b76ce860e9f3d8d444fe`  
		Last Modified: Thu, 04 Jun 2026 17:46:52 GMT  
		Size: 1.4 MB (1353665 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2f5642181567079429032c4c73b5693c5548339de05abb7568bd861fe1399ccd`  
		Last Modified: Thu, 04 Jun 2026 17:46:52 GMT  
		Size: 15.5 KB (15517 bytes)  
		MIME: application/vnd.in-toto+json
