## `clojure:temurin-11-noble`

```console
$ docker pull clojure@sha256:934ced8b91757b72ee28e36f58d2d336607dc6c4f6ac91741ffccc56880de5fb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-11-noble` - linux; amd64

```console
$ docker pull clojure@sha256:6c795c7d80b69f690c15f58ddaf6387dad7f2a45059a522db866b346710002ee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **247.3 MB (247269516 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:220c16fb15db35fc8194e3f8cdc3c2280c32cfbfff6d0e6abfd310925ce8fce7`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["clj"]`

```dockerfile
# Thu, 03 Oct 2024 17:49:34 GMT
ARG RELEASE
# Thu, 03 Oct 2024 17:49:34 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 03 Oct 2024 17:49:34 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 03 Oct 2024 17:49:34 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 03 Oct 2024 17:49:34 GMT
ADD file:34dc4f3ab7a694ecde47ff7a610be18591834c45f1d7251813267798412604e5 in / 
# Thu, 03 Oct 2024 17:49:34 GMT
CMD ["/bin/bash"]
# Thu, 03 Oct 2024 17:49:34 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 03 Oct 2024 17:49:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 03 Oct 2024 17:49:34 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 03 Oct 2024 17:49:34 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
ENV JAVA_VERSION=jdk-11.0.25+9
# Thu, 03 Oct 2024 17:49:34 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='191baa2e052627614022171400a917d28f0987dc54da48aaf07b06f552bb9884';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.25%2B9/OpenJDK11U-jdk_x64_linux_hotspot_11.0.25_9.tar.gz';          ;;        arm64)          ESUM='f2087cc3abdd509b74facf8e43e81e36244d14c70dec080b8f3a662695417ca7';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.25%2B9/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.25_9.tar.gz';          ;;        armhf)          ESUM='6bdd7da08c9f8fedded8da0411b6566c16cb9a904d164b68a0b7f11c8376673a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.25%2B9/OpenJDK11U-jdk_arm_linux_hotspot_11.0.25_9.tar.gz';          ;;        ppc64el)          ESUM='0014ffdae26d2b8f840b4842e3f9d4edc3576b4a961770708273d8ecc86ba5b6';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.25%2B9/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.25_9.tar.gz';          ;;        s390x)          ESUM='5fb661da82943f42a14bed94beda6d4dd3188987bd13b77e8b6f907054a73e9d';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.25%2B9/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.25_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -r "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 03 Oct 2024 17:49:34 GMT
CMD ["jshell"]
# Thu, 03 Oct 2024 17:49:34 GMT
ENV CLOJURE_VERSION=1.12.0.1479
# Thu, 03 Oct 2024 17:49:34 GMT
WORKDIR /tmp
# Thu, 03 Oct 2024 17:49:34 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "94f29b9b66183bd58307c46fb561fd9e9148666bac13a4518a9931b6f989d830 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:ff65ddf9395be21bfe1f320b7705e539ee44c1053034f801b1a3cbbf2d0f4056`  
		Last Modified: Fri, 11 Oct 2024 05:07:18 GMT  
		Size: 29.8 MB (29750363 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0220ed2954f56241917dfc61000fa0b0045806d7983e770dc002c6146430b3a6`  
		Last Modified: Thu, 24 Oct 2024 00:56:54 GMT  
		Size: 17.0 MB (16965883 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc606e0b1efa1c045c9a6e3c4f8171631fe1d3daf5bd2a27b3b144a3890a18a6`  
		Last Modified: Thu, 24 Oct 2024 00:56:56 GMT  
		Size: 145.6 MB (145608899 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cba4551cea19faa644bd39289c57189e85b067dc9315cff188db1a14041b3837`  
		Last Modified: Thu, 24 Oct 2024 00:56:54 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:574bb298c8262a0ea017824087053f55c5d75b64f0abc83fea72b0d8a23efc3a`  
		Last Modified: Thu, 24 Oct 2024 00:56:54 GMT  
		Size: 2.3 KB (2282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0c417499ab8dbef3c6894dfb8bbcdb342879f85a0f1816ef43b3f414c539fda`  
		Last Modified: Thu, 24 Oct 2024 01:59:53 GMT  
		Size: 54.9 MB (54941282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a92e1c7578356dea9673b5a9cf9ba4be7c4c8118bd2080bfec18b1404224c490`  
		Last Modified: Thu, 24 Oct 2024 01:59:52 GMT  
		Size: 616.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-noble` - unknown; unknown

```console
$ docker pull clojure@sha256:988490340fbb05d2c5dc79ccfcb966019b6d7d3ba6c451482762011d76615208
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5555288 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b000e1a2374521226f26a738d006fb416dbff1dc61d0ebf7f9f54701f9b9cf83`

```dockerfile
```

-	Layers:
	-	`sha256:f1c83bb65b427dfce2a47b1e3f3cee1faab310361f960700321500789788509a`  
		Last Modified: Thu, 24 Oct 2024 01:59:52 GMT  
		Size: 5.5 MB (5541738 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:433ef5cbe8b6b5ce6985ad9a919f95fe9129e5ab8330b820d8f5bc06bfae3d28`  
		Last Modified: Thu, 24 Oct 2024 01:59:52 GMT  
		Size: 13.6 KB (13550 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-noble` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:e7a21c6d07ddc0ae98791cff83f36c09849f7adb1021d1f5067f747ab8d81b24
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **243.1 MB (243140537 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb8b3ddbd49a33a576b74bc15b6b5d846bb14c92792ad49fc5fce93d46416748`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["clj"]`

```dockerfile
# Thu, 03 Oct 2024 17:49:34 GMT
ARG RELEASE
# Thu, 03 Oct 2024 17:49:34 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 03 Oct 2024 17:49:34 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 03 Oct 2024 17:49:34 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 03 Oct 2024 17:49:34 GMT
ADD file:b14427a5ec8028ba993a0ff27f9e398456229f9113c9c39f3cc7a0f96c15943b in / 
# Thu, 03 Oct 2024 17:49:34 GMT
CMD ["/bin/bash"]
# Thu, 03 Oct 2024 17:49:34 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 03 Oct 2024 17:49:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 03 Oct 2024 17:49:34 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 03 Oct 2024 17:49:34 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
ENV JAVA_VERSION=jdk-11.0.25+9
# Thu, 03 Oct 2024 17:49:34 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='191baa2e052627614022171400a917d28f0987dc54da48aaf07b06f552bb9884';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.25%2B9/OpenJDK11U-jdk_x64_linux_hotspot_11.0.25_9.tar.gz';          ;;        arm64)          ESUM='f2087cc3abdd509b74facf8e43e81e36244d14c70dec080b8f3a662695417ca7';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.25%2B9/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.25_9.tar.gz';          ;;        armhf)          ESUM='6bdd7da08c9f8fedded8da0411b6566c16cb9a904d164b68a0b7f11c8376673a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.25%2B9/OpenJDK11U-jdk_arm_linux_hotspot_11.0.25_9.tar.gz';          ;;        ppc64el)          ESUM='0014ffdae26d2b8f840b4842e3f9d4edc3576b4a961770708273d8ecc86ba5b6';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.25%2B9/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.25_9.tar.gz';          ;;        s390x)          ESUM='5fb661da82943f42a14bed94beda6d4dd3188987bd13b77e8b6f907054a73e9d';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.25%2B9/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.25_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -r "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 03 Oct 2024 17:49:34 GMT
CMD ["jshell"]
# Thu, 03 Oct 2024 17:49:34 GMT
ENV CLOJURE_VERSION=1.12.0.1479
# Thu, 03 Oct 2024 17:49:34 GMT
WORKDIR /tmp
# Thu, 03 Oct 2024 17:49:34 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "94f29b9b66183bd58307c46fb561fd9e9148666bac13a4518a9931b6f989d830 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:1f630473117188fe348ebdcf0da5e93138275af14007f15baf79967a365e647a`  
		Last Modified: Fri, 11 Oct 2024 05:07:24 GMT  
		Size: 28.9 MB (28885845 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45e2f7d4d887134d9aff4c6177e18f66336c5f3549bb3d16b0c27622e2b8b22c`  
		Last Modified: Thu, 24 Oct 2024 00:59:40 GMT  
		Size: 17.0 MB (16980397 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87a6609c434b423402f39cd2501cdc6274d03756c8ab11fd0b7d11d7d2c04f0c`  
		Last Modified: Thu, 24 Oct 2024 01:04:35 GMT  
		Size: 142.4 MB (142386869 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf7a4300ac20368a416b622e93851e8717db27d862ccdbfa226391ef4fc8af10`  
		Last Modified: Thu, 24 Oct 2024 01:04:31 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ca6e8e502eb40b36eba1a4316eb4b67e0ad240805df8e1b230c11b039a7169e`  
		Last Modified: Thu, 24 Oct 2024 01:04:31 GMT  
		Size: 2.3 KB (2282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3014c0baba8d5086863a4e6eff7431750a98ab46e2d52efa536398ac0adaa281`  
		Last Modified: Thu, 24 Oct 2024 09:12:57 GMT  
		Size: 54.9 MB (54884338 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28509be8b9282ba9c0d13254ce449568a90b40e973cff5991c81eada0927e78a`  
		Last Modified: Thu, 24 Oct 2024 09:12:55 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-noble` - unknown; unknown

```console
$ docker pull clojure@sha256:19ec0db05d2fddc8018271ca7a9f5de47c71584bc2f03d61747b240fe975d6aa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5562569 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5bb4c0324fdf53f8d4c9a53f3f7d910808c2c59ca1f1e854241cf223e7726fca`

```dockerfile
```

-	Layers:
	-	`sha256:c3bb6fee0d918a07a86cb3aa3b3e7bc83d7bdd1dd393534d1c4728ccca793365`  
		Last Modified: Thu, 24 Oct 2024 09:12:56 GMT  
		Size: 5.5 MB (5548927 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:07fa0a41a7bfbda4902774d29fddecba5bcded8525622e528f64a5d5069796c2`  
		Last Modified: Thu, 24 Oct 2024 09:12:55 GMT  
		Size: 13.6 KB (13642 bytes)  
		MIME: application/vnd.in-toto+json
