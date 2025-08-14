## `clojure:temurin-8-tools-deps-alpine`

```console
$ docker pull clojure@sha256:9c5f05f64690c812bdc9fc7b72a6d9b725fc0ffeeb2ae8e4266b43fec8937b82
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `clojure:temurin-8-tools-deps-alpine` - linux; amd64

```console
$ docker pull clojure@sha256:6ccacb5e91b4a68e31bf6b77844866d4a3e102a86dc15c928e39a61d2338b49f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **98.0 MB (98047130 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f560911f61f031bbe23a7a99aece1ccde46ee6ceb21f098e717a0db67c67c676`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["clj"]`

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
RUN set -eux;     apk add --no-cache         fontconfig ttf-dejavu         gnupg         ca-certificates p11-kit-trust         musl-locales musl-locales-lang         tzdata         coreutils         openssl     ;     rm -rf /var/cache/apk/* # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
ENV JAVA_VERSION=jdk8u462-b08
# Sat, 07 Jun 2025 17:38:11 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        x86_64)          ESUM='21e28ad4faf34a2d353252ea363d57afe8d72f9d55f66a54e4e99fd1acb7786b';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u462-b08/OpenJDK8U-jdk_x64_alpine-linux_hotspot_8u462b08.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip; # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
RUN set -eux;     echo "Verifying install ...";     echo "javac -version"; javac -version;     echo "java -version"; java -version;     echo "Complete." # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Sat, 07 Jun 2025 17:38:11 GMT
ENV CLOJURE_VERSION=1.12.1.1550
# Sat, 07 Jun 2025 17:38:11 GMT
WORKDIR /tmp
# Sat, 07 Jun 2025 17:38:11 GMT
RUN apk add --no-cache curl bash make git rlwrap && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "aea202cd0573d79fd8b7db1b608762645a8f93006a86bc817ec130bed1d9707d *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apk del curl # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:9824c27679d3b27c5e1cb00a73adb6f4f8d556994111c12db3c5d61a0c843df8`  
		Last Modified: Tue, 15 Jul 2025 19:00:01 GMT  
		Size: 3.8 MB (3799689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f203d7f2ad91296c29189d9e5c0619b490cb71fe963cad10b53ec84f88ca971d`  
		Last Modified: Mon, 04 Aug 2025 19:10:43 GMT  
		Size: 16.3 MB (16280141 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b884ab8379b7e3f3639c2a35bac4787823a7d7bbcb15fec9531a4e72f8043f69`  
		Last Modified: Mon, 04 Aug 2025 19:10:52 GMT  
		Size: 52.6 MB (52635396 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d301459c24bef03fac78826eaca6eef9060db4208be33da132df14690b45d88`  
		Last Modified: Mon, 04 Aug 2025 19:10:40 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:baa4fd338b932d98deda035704b29a8991d4ce5a7b04a7e3eaac2fe5e23925f1`  
		Last Modified: Mon, 04 Aug 2025 19:10:41 GMT  
		Size: 2.3 KB (2304 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c38f92e75c1a644aa8f1911397bcfedf638c7fce6b0c955ac0c1496544c1a78`  
		Last Modified: Thu, 07 Aug 2025 01:37:05 GMT  
		Size: 25.3 MB (25328822 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e0d98f00c7cfd98dcf16d4a1fded40aa43d889c726f46926dc1190248aa1f3c`  
		Last Modified: Mon, 04 Aug 2025 20:55:22 GMT  
		Size: 620.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-alpine` - unknown; unknown

```console
$ docker pull clojure@sha256:2cdc7f0deb9c753b175fceb9f1fdec7f2c4a8ab05e158fdc470c733ad5931678
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1311279 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b72ff5602d3a42aaa867c5d2818f5180529ca468059ef067927bd4ee504c39d`

```dockerfile
```

-	Layers:
	-	`sha256:9072e7bc60290f01473711f2ca1becc78328a81c16c8afc37bec348eb2f6ad69`  
		Last Modified: Mon, 04 Aug 2025 21:44:32 GMT  
		Size: 1.3 MB (1297856 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:db02ea88232616a0979d2ca02c6c2c610e7eb3af25adb20bf4c8a6904f840648`  
		Last Modified: Mon, 04 Aug 2025 21:44:33 GMT  
		Size: 13.4 KB (13423 bytes)  
		MIME: application/vnd.in-toto+json
