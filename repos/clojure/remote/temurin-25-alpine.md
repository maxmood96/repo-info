## `clojure:temurin-25-alpine`

```console
$ docker pull clojure@sha256:b245b6528c10338fcd8d4ce67f1f6abfff9cea9ace85454f4a600f3fcc113dc1
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-25-alpine` - linux; amd64

```console
$ docker pull clojure@sha256:aac3aef6ac6ec4aa757a570be898dbc746a10b0900e610b793230fd941ee1094
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **136.1 MB (136059531 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c4c60896a33e802337bbaa0424bb23b1643fc492e993318dafa91338830baea`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:04 GMT
ADD alpine-minirootfs-3.23.3-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:04 GMT
CMD ["/bin/sh"]
# Thu, 05 Feb 2026 22:20:43 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 05 Feb 2026 22:20:43 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 05 Feb 2026 22:20:43 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 05 Feb 2026 22:20:43 GMT
RUN set -eux;     apk add --no-cache         fontconfig ttf-dejavu         ca-certificates p11-kit-trust         musl-locales musl-locales-lang         binutils         tzdata         coreutils         openssl     ;     rm -rf /var/cache/apk/* # buildkit
# Thu, 05 Feb 2026 22:20:43 GMT
ENV JAVA_VERSION=jdk-25.0.2+10
# Thu, 05 Feb 2026 22:20:50 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        aarch64)          ESUM='e8d928fb018eabb31a148ebadaa5a5ec69273e6562afede21c426960a6a67143';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.2%2B10/OpenJDK25U-jdk_aarch64_alpine-linux_hotspot_25.0.2_10.tar.gz';          ;;        x86_64)          ESUM='961f13ba0ee1e18c41c50ab642361e4283dee5e7947a48ed6a72c8a661d0cca0';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.2%2B10/OpenJDK25U-jdk_x64_alpine-linux_hotspot_25.0.2_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     apk add --no-cache --virtual .fetch-deps gnupg;     wget -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     apk del --no-network .fetch-deps; # buildkit
# Thu, 05 Feb 2026 22:20:51 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 05 Feb 2026 22:20:51 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 05 Feb 2026 22:20:51 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 05 Feb 2026 22:20:51 GMT
CMD ["jshell"]
# Mon, 02 Mar 2026 19:47:51 GMT
ENV CLOJURE_VERSION=1.12.4.1607
# Mon, 02 Mar 2026 19:47:51 GMT
WORKDIR /tmp
# Mon, 02 Mar 2026 19:47:54 GMT
RUN apk add --no-cache curl bash make git rlwrap && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "bdd7f655825144cbe9055569bfc78b01c44dc2b7156802c817608db9229c8ab5 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apk del curl # buildkit
# Mon, 02 Mar 2026 19:47:54 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Mon, 02 Mar 2026 19:47:54 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Mon, 02 Mar 2026 19:47:54 GMT
ENTRYPOINT ["entrypoint"]
# Mon, 02 Mar 2026 19:47:54 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:589002ba0eaed121a1dbf42f6648f29e5be55d5c8a6ee0f8eaa0285cc21ac153`  
		Last Modified: Wed, 28 Jan 2026 01:18:09 GMT  
		Size: 3.9 MB (3861821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a150fdcc19ea38586861ab60f38c860b790aae07d0df506d6237d0b88dd7bd6f`  
		Last Modified: Thu, 05 Feb 2026 22:21:06 GMT  
		Size: 14.3 MB (14303782 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6acd3bd6814d41ef248fdd907c1157cbd4d90e1cc3ec091e962a6416099873bc`  
		Last Modified: Thu, 05 Feb 2026 22:21:08 GMT  
		Size: 91.5 MB (91491467 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36b2ab561e1f5769d12480d85e27bf1a14a7757ff69b3acea0acc6b4bb0171cc`  
		Last Modified: Thu, 05 Feb 2026 22:21:05 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53405ff8853b1f58bfdc8d736024ea0d1b6df7fa5dedfb0e52a34829c361f358`  
		Last Modified: Thu, 05 Feb 2026 22:21:05 GMT  
		Size: 2.3 KB (2280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b94ab526004d36c87d0bf13a5466c513e1b35b10d214795d2fd6af902f793684`  
		Last Modified: Mon, 02 Mar 2026 19:48:03 GMT  
		Size: 26.4 MB (26398995 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cdd1d0877b74889a084f20e4d65e8c794fcd508f32fff970c37420d3e5e1cb1f`  
		Last Modified: Mon, 02 Mar 2026 19:48:03 GMT  
		Size: 621.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f63522a8a013d2dbd39fab2703fbfd7d6deda9ad794ccaaa1cdebba20a9d703`  
		Last Modified: Mon, 02 Mar 2026 19:48:03 GMT  
		Size: 404.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-alpine` - unknown; unknown

```console
$ docker pull clojure@sha256:17a934ccf8323f216550eab8cedfff03f5158f10c0a95eb9c14a2d5fe328ea68
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.2 MB (1225503 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3fffe29a870b8abc12023992ad28b2f67c561481c2cb091a7beb0e75c96e55b7`

```dockerfile
```

-	Layers:
	-	`sha256:17bb1b89a01823fed787e186f3038d7e3959e3e132bc7e4aff374e68fb0b44c5`  
		Last Modified: Mon, 02 Mar 2026 19:48:03 GMT  
		Size: 1.2 MB (1210077 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:320fc7ba465773e3fd6b463f30bedf866599fcee842948d17029cfba6713d769`  
		Last Modified: Mon, 02 Mar 2026 19:48:02 GMT  
		Size: 15.4 KB (15426 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-25-alpine` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:d971c019045865dd87d37a7b239ee9823153854a4baac030c205c538259686d5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **135.6 MB (135566830 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:40669cdf0138fa53db41db0b72203ae5049c6f665d592e87e93851b8dc00474e`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:09 GMT
ADD alpine-minirootfs-3.23.3-aarch64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:09 GMT
CMD ["/bin/sh"]
# Thu, 05 Feb 2026 22:19:42 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 05 Feb 2026 22:19:42 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 05 Feb 2026 22:19:42 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 05 Feb 2026 22:19:42 GMT
RUN set -eux;     apk add --no-cache         fontconfig ttf-dejavu         ca-certificates p11-kit-trust         musl-locales musl-locales-lang         binutils         tzdata         coreutils         openssl     ;     rm -rf /var/cache/apk/* # buildkit
# Thu, 05 Feb 2026 22:19:42 GMT
ENV JAVA_VERSION=jdk-25.0.2+10
# Thu, 05 Feb 2026 22:19:48 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        aarch64)          ESUM='e8d928fb018eabb31a148ebadaa5a5ec69273e6562afede21c426960a6a67143';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.2%2B10/OpenJDK25U-jdk_aarch64_alpine-linux_hotspot_25.0.2_10.tar.gz';          ;;        x86_64)          ESUM='961f13ba0ee1e18c41c50ab642361e4283dee5e7947a48ed6a72c8a661d0cca0';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.2%2B10/OpenJDK25U-jdk_x64_alpine-linux_hotspot_25.0.2_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     apk add --no-cache --virtual .fetch-deps gnupg;     wget -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     apk del --no-network .fetch-deps; # buildkit
# Thu, 05 Feb 2026 22:19:50 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 05 Feb 2026 22:19:50 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 05 Feb 2026 22:19:50 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 05 Feb 2026 22:19:50 GMT
CMD ["jshell"]
# Mon, 02 Mar 2026 19:48:13 GMT
ENV CLOJURE_VERSION=1.12.4.1607
# Mon, 02 Mar 2026 19:48:13 GMT
WORKDIR /tmp
# Mon, 02 Mar 2026 19:48:16 GMT
RUN apk add --no-cache curl bash make git rlwrap && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "bdd7f655825144cbe9055569bfc78b01c44dc2b7156802c817608db9229c8ab5 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apk del curl # buildkit
# Mon, 02 Mar 2026 19:48:16 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Mon, 02 Mar 2026 19:48:16 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Mon, 02 Mar 2026 19:48:16 GMT
ENTRYPOINT ["entrypoint"]
# Mon, 02 Mar 2026 19:48:16 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:d8ad8cd72600f46cc068e16c39046ebc76526e41051f43a8c249884b200936c0`  
		Last Modified: Wed, 28 Jan 2026 01:18:15 GMT  
		Size: 4.2 MB (4197091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1dc273c5968a27128010b44442da19c1d19512b5d65a3a7fc4734eec44550e27`  
		Last Modified: Thu, 05 Feb 2026 22:20:05 GMT  
		Size: 14.4 MB (14373158 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e47108ee2f22449f768312319f1c90c0d5a1580374197687fd1944d8e2265225`  
		Last Modified: Thu, 05 Feb 2026 22:20:07 GMT  
		Size: 90.4 MB (90431353 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33fed661f46011e75ee9460b18305d0584e08525180dd346895a225fab422298`  
		Last Modified: Thu, 05 Feb 2026 22:20:04 GMT  
		Size: 130.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e47f9177a4521d408115970652519968867bb5c776093bf3b8b10b66aaa3caa1`  
		Last Modified: Thu, 05 Feb 2026 22:20:04 GMT  
		Size: 2.3 KB (2281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03f0dfee04655bb4b16882399c42013dfbf7d71a423f07d03705e4dea8c736e5`  
		Last Modified: Mon, 02 Mar 2026 19:48:26 GMT  
		Size: 26.6 MB (26561764 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32e2ba14b15c7cf6ff71d0240dbaf1ef071db21262b974a4da91a18d49fb739b`  
		Last Modified: Mon, 02 Mar 2026 19:48:25 GMT  
		Size: 618.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:234825552bd71afa2ed6838ade06a2200ad11c0b695f6547c9a265f3c6725997`  
		Last Modified: Mon, 02 Mar 2026 19:48:25 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-alpine` - unknown; unknown

```console
$ docker pull clojure@sha256:f422469f76223bc5fbdc3c56df6540378fca1137ce8cc945308a1001cac40460
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.4 MB (1374943 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e0d86bdce35d92e65dcde79001a952e752c2e18426d2b3ad98f5b73e13789c8b`

```dockerfile
```

-	Layers:
	-	`sha256:dd74303dfc706818766ef40fdfaf1aa143c608760e543bdf4d24d8cc0a99275e`  
		Last Modified: Mon, 02 Mar 2026 19:48:25 GMT  
		Size: 1.4 MB (1359426 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b115128771f022884caf22f0f0f8288cb0a11cced330be4a42e4a3bf877a1f68`  
		Last Modified: Mon, 02 Mar 2026 19:48:25 GMT  
		Size: 15.5 KB (15517 bytes)  
		MIME: application/vnd.in-toto+json
