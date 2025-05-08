## `clojure:temurin-24-tools-deps-1.12.0.1530-alpine`

```console
$ docker pull clojure@sha256:682544fa17d88efff432b57b3804ad4bc7cbfa6a9b27434b66bba5c5741043d4
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-24-tools-deps-1.12.0.1530-alpine` - linux; amd64

```console
$ docker pull clojure@sha256:44c8a7808cf41633869d0e1e1bd58155f7a5aae285e3ddaeda8d745ecc0828bb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **139.5 MB (139465852 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3327390653377e47bef9bfbec1fa7561e7118a3171dbdb521b672fb87ce74951`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-x86_64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Wed, 26 Mar 2025 16:17:22 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 26 Mar 2025 16:17:22 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 26 Mar 2025 16:17:22 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 26 Mar 2025 16:17:22 GMT
RUN set -eux;     apk add --no-cache         fontconfig ttf-dejavu         gnupg         ca-certificates p11-kit-trust         musl-locales musl-locales-lang         binutils         tzdata         coreutils         openssl     ;     rm -rf /var/cache/apk/* # buildkit
# Wed, 26 Mar 2025 16:17:22 GMT
ENV JAVA_VERSION=jdk-24.0.1+9
# Wed, 26 Mar 2025 16:17:22 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        aarch64)          ESUM='97b14f9c2f7e7ba4d4a958bba6835a23353b5fd858725031fc42af4f40a5a4ad';          BINARY_URL='https://github.com/adoptium/temurin24-binaries/releases/download/jdk-24.0.1%2B9/OpenJDK24U-jdk_aarch64_alpine-linux_hotspot_24.0.1_9.tar.gz';          ;;        x86_64)          ESUM='74627af4084a9eb65cc5bad3bb5723b89f1ffb5eaec9afbd696ec5bf684ed79a';          BINARY_URL='https://github.com/adoptium/temurin24-binaries/releases/download/jdk-24.0.1%2B9/OpenJDK24U-jdk_x64_alpine-linux_hotspot_24.0.1_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Wed, 26 Mar 2025 16:17:22 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 26 Mar 2025 16:17:22 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 26 Mar 2025 16:17:22 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 26 Mar 2025 16:17:22 GMT
CMD ["jshell"]
# Wed, 26 Mar 2025 16:17:22 GMT
ENV CLOJURE_VERSION=1.12.0.1530
# Wed, 26 Mar 2025 16:17:22 GMT
WORKDIR /tmp
# Wed, 26 Mar 2025 16:17:22 GMT
RUN apk add --no-cache curl bash make git && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "2a113e3a4f1005e05f4d6a6dee24ca317b0115cdd7e6ca6155a76f5ffa5ba35b *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apk del curl # buildkit
# Wed, 26 Mar 2025 16:17:22 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 26 Mar 2025 16:17:22 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 26 Mar 2025 16:17:22 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 26 Mar 2025 16:17:22 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:f18232174bc91741fdf3da96d85011092101a032a93a388b79e99e69c2d5c870`  
		Last Modified: Fri, 14 Feb 2025 14:36:50 GMT  
		Size: 3.6 MB (3642247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d89fa3206805da3f39f3d33e513000c7fe732767469d033fea6cf0c47b9c3a6b`  
		Last Modified: Thu, 08 May 2025 17:07:53 GMT  
		Size: 21.0 MB (20951357 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4e10588850906e608ba2d19a979d66a3c3231deab14453e4c96f0f145218c2f`  
		Last Modified: Thu, 08 May 2025 17:07:58 GMT  
		Size: 90.1 MB (90081657 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84f971aa3d7e1c0f663d0194507c129d747c8c22bd5a54388471f73fd984c2bb`  
		Last Modified: Thu, 08 May 2025 17:07:52 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:883498cd171d42da42c278599e117d11db9885fbea522558e72b6f1740e5567d`  
		Last Modified: Thu, 08 May 2025 17:07:52 GMT  
		Size: 2.3 KB (2279 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:307f5904fcf6f82b6e7ab3844f2b8e66b08d88c1da6eca65c712acf1a0c83dac`  
		Last Modified: Wed, 23 Apr 2025 17:16:26 GMT  
		Size: 24.8 MB (24787130 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e30e22179f5183b510ee1407f6f51284dbe4d0fd3aac20c369d24d427ad9997b`  
		Last Modified: Wed, 23 Apr 2025 17:16:25 GMT  
		Size: 620.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87198894316c0fcc05546c0889757313fd1c24b54db6016028f3a012ce4cc086`  
		Last Modified: Wed, 23 Apr 2025 17:16:25 GMT  
		Size: 402.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-24-tools-deps-1.12.0.1530-alpine` - unknown; unknown

```console
$ docker pull clojure@sha256:5d16ccc2747d05493fe8f98befaf5bc542051b2ac806104077de0bbdd12977e0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.2 MB (1216232 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:60e521c5720805d4bdebc68ead31b3b48dd29aa1e268297cc611b5cd888e14ed`

```dockerfile
```

-	Layers:
	-	`sha256:905115e0150adb203bf73ba120410a4e6f6f0c6ddff9df9e5f9b0ce612502be7`  
		Last Modified: Wed, 23 Apr 2025 17:16:26 GMT  
		Size: 1.2 MB (1200779 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fe5a2991c7d1638947dd9cc34742e671fe5c032b76a67f75b5b70b650690e53b`  
		Last Modified: Wed, 23 Apr 2025 17:16:25 GMT  
		Size: 15.5 KB (15453 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-24-tools-deps-1.12.0.1530-alpine` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:bf841698e30e99bc8a31d037c8ad856db0c87edc81e2b9307fc322cb9cb69002
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **139.0 MB (138982346 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d0afdcd4592733bad12cc5878144bba63f0b39809385e44cceae97871d491c57`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-aarch64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Wed, 23 Apr 2025 14:48:05 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 23 Apr 2025 14:48:05 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 23 Apr 2025 14:48:05 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 23 Apr 2025 14:48:05 GMT
RUN set -eux;     apk add --no-cache         fontconfig ttf-dejavu         gnupg         ca-certificates p11-kit-trust         musl-locales musl-locales-lang         binutils         tzdata         coreutils         openssl     ;     rm -rf /var/cache/apk/* # buildkit
# Wed, 23 Apr 2025 14:48:05 GMT
ENV JAVA_VERSION=jdk-24.0.1+9
# Wed, 23 Apr 2025 14:48:05 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        aarch64)          ESUM='97b14f9c2f7e7ba4d4a958bba6835a23353b5fd858725031fc42af4f40a5a4ad';          BINARY_URL='https://github.com/adoptium/temurin24-binaries/releases/download/jdk-24.0.1%2B9/OpenJDK24U-jdk_aarch64_alpine-linux_hotspot_24.0.1_9.tar.gz';          ;;        x86_64)          ESUM='74627af4084a9eb65cc5bad3bb5723b89f1ffb5eaec9afbd696ec5bf684ed79a';          BINARY_URL='https://github.com/adoptium/temurin24-binaries/releases/download/jdk-24.0.1%2B9/OpenJDK24U-jdk_x64_alpine-linux_hotspot_24.0.1_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Wed, 23 Apr 2025 14:48:05 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 23 Apr 2025 14:48:05 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 23 Apr 2025 14:48:05 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 23 Apr 2025 14:48:05 GMT
CMD ["jshell"]
# Mon, 28 Apr 2025 17:24:54 GMT
ENV CLOJURE_VERSION=1.12.0.1530
# Mon, 28 Apr 2025 17:24:54 GMT
WORKDIR /tmp
# Mon, 28 Apr 2025 17:24:54 GMT
RUN apk add --no-cache curl bash make git && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "2a113e3a4f1005e05f4d6a6dee24ca317b0115cdd7e6ca6155a76f5ffa5ba35b *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apk del curl # buildkit
# Mon, 28 Apr 2025 17:24:54 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Mon, 28 Apr 2025 17:24:54 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Mon, 28 Apr 2025 17:24:54 GMT
ENTRYPOINT ["entrypoint"]
# Mon, 28 Apr 2025 17:24:54 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:6e771e15690e2fabf2332d3a3b744495411d6e0b00b2aea64419b58b0066cf81`  
		Last Modified: Fri, 14 Feb 2025 14:37:30 GMT  
		Size: 4.0 MB (3993029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce4dc4c8e3ac1404ce7eb282c94493325536d142e577ef37ec27bcf3edd09f4b`  
		Last Modified: Thu, 08 May 2025 17:06:52 GMT  
		Size: 21.0 MB (21006028 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b587585b41566074b337300ac392de9b4d45b1d80418a53a9682dc5dc5cfa792`  
		Last Modified: Thu, 08 May 2025 17:06:58 GMT  
		Size: 89.1 MB (89067358 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0de1aae9586f9d6276f2cc85c43560b6c4303b29fadb32b3998b60ca44ac6f4e`  
		Last Modified: Thu, 08 May 2025 17:06:50 GMT  
		Size: 130.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6eef6807030255660c0fed6484392bae8ed8ca964c95eaf49f68b4b768b6af50`  
		Last Modified: Thu, 08 May 2025 17:06:51 GMT  
		Size: 2.3 KB (2280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed0e2482835a29870ea3d37a35a75093162f6cf3924c444738cf4e17db5f729b`  
		Last Modified: Mon, 28 Apr 2025 19:16:35 GMT  
		Size: 24.9 MB (24912465 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:258471713b453887f89d98712a67e967c56840e1b1bd348bc044b88207f24041`  
		Last Modified: Mon, 28 Apr 2025 19:16:34 GMT  
		Size: 621.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c674f67f9fea3aa1442e2fc00ae4724ed37950729b2c40575ea6aff4df0ce374`  
		Last Modified: Mon, 28 Apr 2025 19:16:34 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-24-tools-deps-1.12.0.1530-alpine` - unknown; unknown

```console
$ docker pull clojure@sha256:6aef6d63563f678cdfb58a2625517c36ab421df9fffc91c0cbcbcd038fa0df57
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.4 MB (1366323 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf699d2529b3f41e83feb0675321f2d6a648404f840a61c0e0e00882beec5a0d`

```dockerfile
```

-	Layers:
	-	`sha256:68645e23e79140ea84f43bf39396a8be5f5d0156fe42c833342cb2d36faa841d`  
		Last Modified: Mon, 28 Apr 2025 19:16:34 GMT  
		Size: 1.4 MB (1350778 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9b1c6d8dd64d5b62ccf18a1e1458f58f06015de603de2efb106c2c06f818ebfc`  
		Last Modified: Mon, 28 Apr 2025 19:16:34 GMT  
		Size: 15.5 KB (15545 bytes)  
		MIME: application/vnd.in-toto+json
