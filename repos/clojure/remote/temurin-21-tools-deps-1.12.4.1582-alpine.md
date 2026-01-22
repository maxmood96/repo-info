## `clojure:temurin-21-tools-deps-1.12.4.1582-alpine`

```console
$ docker pull clojure@sha256:ed44687e4c0b9bb885db5edbaec1a784e7e013f9ef4d7ed0f7639d91585de5c7
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-21-tools-deps-1.12.4.1582-alpine` - linux; amd64

```console
$ docker pull clojure@sha256:65098d59d43a059c1fe5af0ff470c21f280187e5505f3419d93cd89f13b229d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **208.1 MB (208142274 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e343632cbac8c5770899d38da3350eb6df5f97e37546024af89b27c4c7018d8e`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-x86_64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Sat, 08 Nov 2025 17:59:09 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 08 Nov 2025 17:59:09 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 08 Nov 2025 17:59:09 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Sat, 08 Nov 2025 17:59:09 GMT
RUN set -eux;     apk add --no-cache         fontconfig ttf-dejavu         gnupg         ca-certificates p11-kit-trust         musl-locales musl-locales-lang         binutils         tzdata         coreutils         openssl     ;     rm -rf /var/cache/apk/* # buildkit
# Sat, 08 Nov 2025 17:59:09 GMT
ENV JAVA_VERSION=jdk-21.0.9+10
# Sat, 08 Nov 2025 17:59:14 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        aarch64)          ESUM='6d3c2b956d6b837bfdc992e58488fb16c96e5852820e9feaa42a8672bbca9c7b';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.9%2B10/OpenJDK21U-jdk_aarch64_alpine-linux_hotspot_21.0.9_10.tar.gz';          ;;        x86_64)          ESUM='52e30d3157432e87ee464b656f776f0a22946f1f3182eea779258284bc6f55da';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.9%2B10/OpenJDK21U-jdk_x64_alpine-linux_hotspot_21.0.9_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Sat, 08 Nov 2025 17:59:16 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Sat, 08 Nov 2025 17:59:16 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Sat, 08 Nov 2025 17:59:16 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Sat, 08 Nov 2025 17:59:16 GMT
CMD ["jshell"]
# Thu, 11 Dec 2025 22:39:26 GMT
ENV CLOJURE_VERSION=1.12.4.1582
# Thu, 11 Dec 2025 22:39:26 GMT
WORKDIR /tmp
# Thu, 11 Dec 2025 22:39:29 GMT
RUN apk add --no-cache curl bash make git rlwrap && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "0dc6f211d2a737ce6872feb0aa4d1cbbbe72d02665c684f9ad206b88d2e7f4fb *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apk del curl # buildkit
# Thu, 11 Dec 2025 22:39:30 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 11 Dec 2025 22:39:30 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 11 Dec 2025 22:39:30 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 11 Dec 2025 22:39:30 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:2d35ebdb57d9971fea0cac1582aa78935adf8058b2cc32db163c98822e5dfa1b`  
		Last Modified: Wed, 08 Oct 2025 12:04:21 GMT  
		Size: 3.8 MB (3802452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:604c946e03558d5b63598812078583a7cacf7c19412e2c71732c6c7e972a09e0`  
		Last Modified: Sat, 08 Nov 2025 17:59:31 GMT  
		Size: 21.1 MB (21112184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a34da1dc78644035d0dc76bd344bb33911551088d2c35e5eae20ee0883291ece`  
		Last Modified: Wed, 07 Jan 2026 18:56:58 GMT  
		Size: 158.1 MB (158102933 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6a3991c44d0e9016c97a7a16b122fc35778b7bf3abb694a7acabc5f8e6551c8`  
		Last Modified: Sat, 08 Nov 2025 17:59:30 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8cb030eff3c05fd59aaea4464781aa26b800aef5bdbe8b20be44289a6d4fde7`  
		Last Modified: Sat, 08 Nov 2025 17:59:30 GMT  
		Size: 2.3 KB (2279 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e169b1abdb33da5d93ffffc885cb8105b37e0234fd84ff8ea5bc8aef072354f`  
		Last Modified: Thu, 11 Dec 2025 22:39:40 GMT  
		Size: 25.1 MB (25121242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec8a8883ef92d2697caca495073f8279484debf6d0fef26168fce5a5cb296b84`  
		Last Modified: Thu, 11 Dec 2025 22:39:46 GMT  
		Size: 619.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31636dab5e40e8b679a51352e89779109791014c23c2b62f745e2e2625e1b508`  
		Last Modified: Thu, 11 Dec 2025 22:39:46 GMT  
		Size: 404.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-1.12.4.1582-alpine` - unknown; unknown

```console
$ docker pull clojure@sha256:7b70e03823013bcca9401305f127b7c917c5c5a33084d7698dd204a309264e70
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1316391 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b316ed0c070650b0b7a14b55a9cccb4e684a548561aba89c5791233c78c79f2`

```dockerfile
```

-	Layers:
	-	`sha256:57cdfcc2ace667cee97348155a75fe38c2cb11197107730d107aa337fdbe102d`  
		Last Modified: Thu, 11 Dec 2025 22:39:40 GMT  
		Size: 1.3 MB (1300960 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b3806d616bef390aeddf4af5b278b51a3faa3bea56288ef3b5d102232bdc04e1`  
		Last Modified: Fri, 12 Dec 2025 01:40:36 GMT  
		Size: 15.4 KB (15431 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-tools-deps-1.12.4.1582-alpine` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:14328e35ee850c59b207d1e610e93630ceb6186fd57894a7020ed2c1f44cb9c9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **206.6 MB (206641399 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c033f61e4fbac6e6293c036cc413c3bfe604bb27d4ae9aa615e078d7ca59d09c`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-aarch64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Sat, 08 Nov 2025 17:58:30 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 08 Nov 2025 17:58:30 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 08 Nov 2025 17:58:30 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Sat, 08 Nov 2025 17:58:30 GMT
RUN set -eux;     apk add --no-cache         fontconfig ttf-dejavu         gnupg         ca-certificates p11-kit-trust         musl-locales musl-locales-lang         binutils         tzdata         coreutils         openssl     ;     rm -rf /var/cache/apk/* # buildkit
# Sat, 08 Nov 2025 17:58:30 GMT
ENV JAVA_VERSION=jdk-21.0.9+10
# Sat, 08 Nov 2025 17:58:37 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        aarch64)          ESUM='6d3c2b956d6b837bfdc992e58488fb16c96e5852820e9feaa42a8672bbca9c7b';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.9%2B10/OpenJDK21U-jdk_aarch64_alpine-linux_hotspot_21.0.9_10.tar.gz';          ;;        x86_64)          ESUM='52e30d3157432e87ee464b656f776f0a22946f1f3182eea779258284bc6f55da';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.9%2B10/OpenJDK21U-jdk_x64_alpine-linux_hotspot_21.0.9_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Sat, 08 Nov 2025 17:58:38 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Sat, 08 Nov 2025 17:58:38 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Sat, 08 Nov 2025 17:58:38 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Sat, 08 Nov 2025 17:58:38 GMT
CMD ["jshell"]
# Thu, 11 Dec 2025 22:39:49 GMT
ENV CLOJURE_VERSION=1.12.4.1582
# Thu, 11 Dec 2025 22:39:49 GMT
WORKDIR /tmp
# Thu, 11 Dec 2025 22:39:53 GMT
RUN apk add --no-cache curl bash make git rlwrap && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "0dc6f211d2a737ce6872feb0aa4d1cbbbe72d02665c684f9ad206b88d2e7f4fb *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apk del curl # buildkit
# Thu, 11 Dec 2025 22:39:53 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 11 Dec 2025 22:39:53 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 11 Dec 2025 22:39:53 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 11 Dec 2025 22:39:53 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:6b59a28fa20117e6048ad0616b8d8c901877ef15ff4c7f18db04e4f01f43bc39`  
		Last Modified: Sun, 07 Dec 2025 13:54:03 GMT  
		Size: 4.1 MB (4138069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:534675d10f4caa61d314d425f92d547712626251f89901c5d58eac317205e1c5`  
		Last Modified: Sat, 08 Nov 2025 17:58:56 GMT  
		Size: 21.2 MB (21164202 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ac0dd9c7e27c9284c00f27ca9959b156926e12010ba8683e583ff6811916f12`  
		Last Modified: Wed, 07 Jan 2026 18:58:24 GMT  
		Size: 156.1 MB (156097412 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9c7361609fe55d3eb9a77ca907ab0d5f394b754ecf497fbd624cd8fe359a6db`  
		Last Modified: Wed, 07 Jan 2026 18:58:16 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:867c03b825a35a5db0249203ef051f7e12f2bc4c110f281f6de68072d3c55bab`  
		Last Modified: Wed, 07 Jan 2026 18:57:14 GMT  
		Size: 2.3 KB (2279 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9038baca7cc414796a92a3a46548d048c886e1f877809fa8d391d892410e984b`  
		Last Modified: Thu, 11 Dec 2025 22:40:10 GMT  
		Size: 25.2 MB (25238258 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fa206fb0e76a8fe2944403564b3e5b63cf6c1025fd8af289b3a1dc955361662`  
		Last Modified: Thu, 11 Dec 2025 22:40:08 GMT  
		Size: 616.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ec0bae64a4f611d8a8c9ef7c675a7dca73b70b1e5741788ddc4c2e669dbe84f`  
		Last Modified: Thu, 11 Dec 2025 22:40:02 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-1.12.4.1582-alpine` - unknown; unknown

```console
$ docker pull clojure@sha256:1f67869c663d5135c45af6d1507f13ba63236a68763805b4508edf7f9ef41b59
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.5 MB (1466485 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed6a1634c2fb159a0e399371a49e095cba3caf4a12adb1515c0e51870165a1d1`

```dockerfile
```

-	Layers:
	-	`sha256:b61d50ef83ac067e54a218166871fbf5fe5d797b55b38c297520f1445591e4d3`  
		Last Modified: Fri, 12 Dec 2025 01:40:40 GMT  
		Size: 1.5 MB (1450962 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:06be5dd973909f44eb1412a0a774e14b37955506e7137abe397ebe5be0fea484`  
		Last Modified: Fri, 12 Dec 2025 01:40:41 GMT  
		Size: 15.5 KB (15523 bytes)  
		MIME: application/vnd.in-toto+json
