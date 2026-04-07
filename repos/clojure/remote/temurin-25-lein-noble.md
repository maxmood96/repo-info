## `clojure:temurin-25-lein-noble`

```console
$ docker pull clojure@sha256:94a4c51940b0916f1b3d4711b368be5d79611b699cf666a04ce2fc7a28a63a7e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 10
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; riscv64
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `clojure:temurin-25-lein-noble` - linux; amd64

```console
$ docker pull clojure@sha256:4b539df37586625027c6f49fff0c01eef1e0220fee22d07733db3b8f88015e2b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **158.6 MB (158578663 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d84eb53fea4f300a2a55acf686fff79b584601178ca9355c7b0860f8ef788df`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Fri, 03 Apr 2026 15:16:40 GMT
ARG RELEASE
# Fri, 03 Apr 2026 15:16:40 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 03 Apr 2026 15:16:40 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 03 Apr 2026 15:16:42 GMT
ADD file:0f6466425c4f1800aae9224ddc3437b90c829cea58fb8edd5dde2f1eb0ee28da in / 
# Fri, 03 Apr 2026 15:16:43 GMT
CMD ["/bin/bash"]
# Tue, 07 Apr 2026 01:52:16 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 07 Apr 2026 01:52:16 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Apr 2026 01:52:16 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 07 Apr 2026 01:52:16 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 01:52:16 GMT
ENV JAVA_VERSION=jdk-25.0.2+10
# Tue, 07 Apr 2026 01:52:36 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='987387933b64b9833846dee373b640440d3e1fd48a04804ec01a6dbf718e8ab8';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.2%2B10/OpenJDK25U-jdk_x64_linux_hotspot_25.0.2_10.tar.gz';          ;;        arm64)          ESUM='a9d73e711d967dc44896d4f430f73a68fd33590dabc29a7f2fb9f593425b854c';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.2%2B10/OpenJDK25U-jdk_aarch64_linux_hotspot_25.0.2_10.tar.gz';          ;;        ppc64el)          ESUM='b262b735b215173003766da36588d5f717dceada0286db41b439f93fb2ada468';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.2%2B10/OpenJDK25U-jdk_ppc64le_linux_hotspot_25.0.2_10.tar.gz';          ;;        riscv64)          ESUM='168119e4fba350f4e6b3ca92450a2b90a8502b89a235a04415e9adf9f5d3164e';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.2%2B10/OpenJDK25U-jdk_riscv64_linux_hotspot_25.0.2_10.tar.gz';          ;;        s390x)          ESUM='15e5cbcadcf3d43623c31b825063cdc2817b9f1ba840b51dc6ef70e5d33c84e3';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.2%2B10/OpenJDK25U-jdk_s390x_linux_hotspot_25.0.2_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     savedAptMark="$(apt-mark showmanual)";     apt-get update;     apt-get install -y --no-install-recommends wget gnupg;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     apt-mark auto '.*' > /dev/null;     apt-mark manual $savedAptMark > /dev/null;     apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false;     rm -rf /var/lib/apt/lists/*;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Tue, 07 Apr 2026 01:52:37 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 07 Apr 2026 01:52:37 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 07 Apr 2026 01:52:37 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 07 Apr 2026 01:52:37 GMT
CMD ["jshell"]
# Tue, 07 Apr 2026 03:16:49 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 07 Apr 2026 03:16:49 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 07 Apr 2026 03:16:49 GMT
WORKDIR /tmp
# Tue, 07 Apr 2026 03:17:06 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 07 Apr 2026 03:17:06 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 07 Apr 2026 03:17:06 GMT
ENV LEIN_ROOT=1
# Tue, 07 Apr 2026 03:17:08 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 07 Apr 2026 03:17:08 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 07 Apr 2026 03:17:08 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 07 Apr 2026 03:17:08 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:689b91d88a0f4086057ec826027b128902ecf2b516be510371c115bc55da19a6`  
		Last Modified: Fri, 03 Apr 2026 15:56:29 GMT  
		Size: 29.7 MB (29733459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1d7a89f363d00fbdb4eeb3725625f77439f3317bf972e4c8d4e74325647ecb6`  
		Last Modified: Tue, 07 Apr 2026 01:52:54 GMT  
		Size: 17.5 MB (17462707 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d58dcb4ab26520b9c733623bef23b51e9fbf6845834f6d3fad23e922d5c316b4`  
		Last Modified: Tue, 07 Apr 2026 01:52:57 GMT  
		Size: 92.4 MB (92388861 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abc49b9bffc8e184c7b52408c24aa9b27a669c1699ff5339445f20666c11d334`  
		Last Modified: Tue, 07 Apr 2026 01:52:54 GMT  
		Size: 2.3 KB (2282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c152a4479454996fdeccafcaae42a148c4650ef31a77815fbbfc398063eb9e96`  
		Last Modified: Tue, 07 Apr 2026 03:17:19 GMT  
		Size: 14.5 MB (14473210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfc63f413352275a2b1d2b80c4cbca215a72efff8213c5534c206483f1b891e5`  
		Last Modified: Tue, 07 Apr 2026 03:17:19 GMT  
		Size: 4.5 MB (4517683 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9da5690ac07e05234c911584af992d0e4531c92245de2fd2d053e6a8156c8245`  
		Last Modified: Tue, 07 Apr 2026 03:17:19 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-lein-noble` - unknown; unknown

```console
$ docker pull clojure@sha256:344154e22447d4be64c493e4cced1beca60bc4dc575a72d39ebd2f8719971c92
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.4 MB (3387285 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e4cfce0a93002ef63c9d99db41a81aea948e09f328d8d5339d1f4c6bfd3a78d`

```dockerfile
```

-	Layers:
	-	`sha256:7a259ef129a1b17f3063681932b10a96fd6dd93c4e3488db604b31bb20658d76`  
		Last Modified: Tue, 07 Apr 2026 03:17:19 GMT  
		Size: 3.4 MB (3368919 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e3c67c8e0b68e17313f92f4537d763fb93c05b071bcaf41d2edd1b405265d03f`  
		Last Modified: Tue, 07 Apr 2026 03:17:18 GMT  
		Size: 18.4 KB (18366 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-25-lein-noble` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:2a8edc11dde0affdf22efb3ee465db00564995dc891fac0d1128d94eafe4b44c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **157.9 MB (157947955 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c56477ceb44896e69042f5afd7ed18c68a5f7669e50fe4cedf02802fb5d65487`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Fri, 03 Apr 2026 15:15:14 GMT
ARG RELEASE
# Fri, 03 Apr 2026 15:15:14 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 03 Apr 2026 15:15:14 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 03 Apr 2026 15:15:17 GMT
ADD file:9bab986009eae65b5534b3547eb3a7d0a1564404426de350dfd183cf3a4ffa9f in / 
# Fri, 03 Apr 2026 15:15:17 GMT
CMD ["/bin/bash"]
# Tue, 07 Apr 2026 01:55:30 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 07 Apr 2026 01:55:30 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Apr 2026 01:55:30 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 07 Apr 2026 01:55:30 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 01:55:30 GMT
ENV JAVA_VERSION=jdk-25.0.2+10
# Tue, 07 Apr 2026 01:55:53 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='987387933b64b9833846dee373b640440d3e1fd48a04804ec01a6dbf718e8ab8';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.2%2B10/OpenJDK25U-jdk_x64_linux_hotspot_25.0.2_10.tar.gz';          ;;        arm64)          ESUM='a9d73e711d967dc44896d4f430f73a68fd33590dabc29a7f2fb9f593425b854c';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.2%2B10/OpenJDK25U-jdk_aarch64_linux_hotspot_25.0.2_10.tar.gz';          ;;        ppc64el)          ESUM='b262b735b215173003766da36588d5f717dceada0286db41b439f93fb2ada468';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.2%2B10/OpenJDK25U-jdk_ppc64le_linux_hotspot_25.0.2_10.tar.gz';          ;;        riscv64)          ESUM='168119e4fba350f4e6b3ca92450a2b90a8502b89a235a04415e9adf9f5d3164e';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.2%2B10/OpenJDK25U-jdk_riscv64_linux_hotspot_25.0.2_10.tar.gz';          ;;        s390x)          ESUM='15e5cbcadcf3d43623c31b825063cdc2817b9f1ba840b51dc6ef70e5d33c84e3';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.2%2B10/OpenJDK25U-jdk_s390x_linux_hotspot_25.0.2_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     savedAptMark="$(apt-mark showmanual)";     apt-get update;     apt-get install -y --no-install-recommends wget gnupg;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     apt-mark auto '.*' > /dev/null;     apt-mark manual $savedAptMark > /dev/null;     apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false;     rm -rf /var/lib/apt/lists/*;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Tue, 07 Apr 2026 01:55:54 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 07 Apr 2026 01:55:54 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 07 Apr 2026 01:55:54 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 07 Apr 2026 01:55:54 GMT
CMD ["jshell"]
# Tue, 07 Apr 2026 03:27:39 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 07 Apr 2026 03:27:39 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 07 Apr 2026 03:27:39 GMT
WORKDIR /tmp
# Tue, 07 Apr 2026 03:27:58 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 07 Apr 2026 03:27:58 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 07 Apr 2026 03:27:58 GMT
ENV LEIN_ROOT=1
# Tue, 07 Apr 2026 03:27:59 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 07 Apr 2026 03:27:59 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 07 Apr 2026 03:27:59 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 07 Apr 2026 03:27:59 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:76fd055477b6edf8004a5a962edad02a820d4c8b2f02682410edfbe376b418c5`  
		Last Modified: Fri, 03 Apr 2026 15:56:36 GMT  
		Size: 28.9 MB (28874075 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3015356b23ea1b0133580e617372417cc6db3dabdf6e97b8ce4e0c591947552`  
		Last Modified: Tue, 07 Apr 2026 01:56:10 GMT  
		Size: 18.7 MB (18654733 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40e4754d54bd61e52c7042dc67b848766f81f8e0b5fcc71ae9885823b64baca6`  
		Last Modified: Tue, 07 Apr 2026 01:56:12 GMT  
		Size: 91.4 MB (91424717 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f199c35f5162fea3c8f07eef1e388cab02e2e3f619c9b2842b8bcd77a768e1e`  
		Last Modified: Tue, 07 Apr 2026 01:55:39 GMT  
		Size: 2.3 KB (2281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21a806222413827ddc1c5f5a0f65155f82de512188c16bff9c379fd704198172`  
		Last Modified: Tue, 07 Apr 2026 03:28:09 GMT  
		Size: 14.5 MB (14474001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83e39ceb46f3802de6eadd59c4913228906ed85ebcea3eb7d5492a1fca5743a8`  
		Last Modified: Tue, 07 Apr 2026 03:28:09 GMT  
		Size: 4.5 MB (4517688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3f8a9022d391bf5826522c39cf67d6eeb5385657cddff323211b96efa056ba0`  
		Last Modified: Tue, 07 Apr 2026 03:28:09 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-lein-noble` - unknown; unknown

```console
$ docker pull clojure@sha256:d17308279c7f534681603906847ecbd53aa5ba3b1465ad66220686ccbdf9a2fd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3518853 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e524fe6b0d86475b34f96b696794c04d567d376abcf8973bf83c2ded959b47e`

```dockerfile
```

-	Layers:
	-	`sha256:52c6cb6ecab9883197e5626028e5522d0e1b7aef6d6d9d4b886d1879805a1b26`  
		Last Modified: Tue, 07 Apr 2026 03:28:09 GMT  
		Size: 3.5 MB (3500394 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:65e823546f48ce535e9c4815c51ba6dd0f87796d6783a575d524c9477e600a30`  
		Last Modified: Tue, 07 Apr 2026 03:28:09 GMT  
		Size: 18.5 KB (18459 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-25-lein-noble` - linux; ppc64le

```console
$ docker pull clojure@sha256:12738bc423ace9b80449b9d10215eb3ffcf0907002571bb72282bf89e42bbd32
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **162.4 MB (162433613 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c96d211349717f20449545d3d236f5d9dcc2645f902e5aa3c0a386f322d9566`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 23 Feb 2026 17:18:33 GMT
ARG RELEASE
# Mon, 23 Feb 2026 17:18:33 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 23 Feb 2026 17:18:33 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 23 Feb 2026 17:18:33 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 23 Feb 2026 17:18:36 GMT
ADD file:2a89eb67bf550d9680999e3ff99dbaa17c251b6c343a241318e879a26da53fca in / 
# Mon, 23 Feb 2026 17:18:37 GMT
CMD ["/bin/bash"]
# Tue, 17 Mar 2026 08:38:03 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 17 Mar 2026 08:38:03 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Mar 2026 08:38:03 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 17 Mar 2026 08:38:03 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Mar 2026 08:38:03 GMT
ENV JAVA_VERSION=jdk-25.0.2+10
# Tue, 17 Mar 2026 08:38:49 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='987387933b64b9833846dee373b640440d3e1fd48a04804ec01a6dbf718e8ab8';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.2%2B10/OpenJDK25U-jdk_x64_linux_hotspot_25.0.2_10.tar.gz';          ;;        arm64)          ESUM='a9d73e711d967dc44896d4f430f73a68fd33590dabc29a7f2fb9f593425b854c';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.2%2B10/OpenJDK25U-jdk_aarch64_linux_hotspot_25.0.2_10.tar.gz';          ;;        ppc64el)          ESUM='b262b735b215173003766da36588d5f717dceada0286db41b439f93fb2ada468';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.2%2B10/OpenJDK25U-jdk_ppc64le_linux_hotspot_25.0.2_10.tar.gz';          ;;        riscv64)          ESUM='168119e4fba350f4e6b3ca92450a2b90a8502b89a235a04415e9adf9f5d3164e';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.2%2B10/OpenJDK25U-jdk_riscv64_linux_hotspot_25.0.2_10.tar.gz';          ;;        s390x)          ESUM='15e5cbcadcf3d43623c31b825063cdc2817b9f1ba840b51dc6ef70e5d33c84e3';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.2%2B10/OpenJDK25U-jdk_s390x_linux_hotspot_25.0.2_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     savedAptMark="$(apt-mark showmanual)";     apt-get update;     apt-get install -y --no-install-recommends wget gnupg;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     apt-mark auto '.*' > /dev/null;     apt-mark manual $savedAptMark > /dev/null;     apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false;     rm -rf /var/lib/apt/lists/*;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Tue, 17 Mar 2026 08:38:52 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 17 Mar 2026 08:38:53 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 17 Mar 2026 08:38:53 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 17 Mar 2026 08:38:53 GMT
CMD ["jshell"]
# Tue, 17 Mar 2026 18:45:00 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 17 Mar 2026 18:45:00 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 17 Mar 2026 18:45:00 GMT
WORKDIR /tmp
# Tue, 17 Mar 2026 18:45:43 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 17 Mar 2026 18:45:43 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 17 Mar 2026 18:45:43 GMT
ENV LEIN_ROOT=1
# Tue, 17 Mar 2026 18:45:47 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 17 Mar 2026 18:45:47 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 17 Mar 2026 18:45:47 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 17 Mar 2026 18:45:47 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:f826c9b754a00ada9d9335ffdf3ffd40f6925a3223caac76cc429823b8621f9e`  
		Last Modified: Mon, 23 Feb 2026 17:51:39 GMT  
		Size: 34.3 MB (34310051 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:719799e3fd3fced1bf5442d22aed7fb7582f8aef125453efff5308862d936136`  
		Last Modified: Tue, 17 Mar 2026 08:39:28 GMT  
		Size: 17.3 MB (17328483 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2fd462ea1b064dfa4c0f2866d0b9c265dbb70fc5dc940ba5349e7e89dca9544`  
		Last Modified: Tue, 17 Mar 2026 08:39:30 GMT  
		Size: 91.8 MB (91756951 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d7f07a919432b86262243e8578a37d80592647d53ec1896888579931c683559`  
		Last Modified: Tue, 17 Mar 2026 08:39:27 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5472ced119fe308b21cee10998bfe938b4781c690af43c9b542669c8f18f330`  
		Last Modified: Tue, 17 Mar 2026 18:46:05 GMT  
		Size: 14.5 MB (14517665 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73c2f79922635e857f7d40e5a510957f65bd09772a0ca6e55f139c5f72b2c8ce`  
		Last Modified: Tue, 17 Mar 2026 18:46:05 GMT  
		Size: 4.5 MB (4517717 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:507f9aedc6c163d6ca4d034821ad34d916945f808154723660524f336858c56a`  
		Last Modified: Tue, 17 Mar 2026 18:46:04 GMT  
		Size: 399.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-lein-noble` - unknown; unknown

```console
$ docker pull clojure@sha256:939c5d9c58d82959a4c42e5337b03c21ea002846c11e67aee01df19ee359719b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.4 MB (3418218 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:694a1d0512e77dfb1bc2545b3fcb73bfe4dafa4f8c703ed1629b19cd9cbeb649`

```dockerfile
```

-	Layers:
	-	`sha256:ef57e9d99b7cb428c1d1af0fef6fa5553e36f5d0b15ff1e02c73e1034a5df973`  
		Last Modified: Tue, 17 Mar 2026 18:46:05 GMT  
		Size: 3.4 MB (3399818 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:182c469d817e3050212480ec9a3dde72d7d0e52fcd970c548efa2e11a5bb8517`  
		Last Modified: Tue, 17 Mar 2026 18:46:04 GMT  
		Size: 18.4 KB (18400 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-25-lein-noble` - linux; riscv64

```console
$ docker pull clojure@sha256:1dbaabca468dd3de0c8542365d6d75cd1d04912fcd365d8f755a1c94b6cde517
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **154.7 MB (154709679 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fcbaba4bb362f2bd42fc8a091a7f9ffdfef2c3875b2a5e6ba6d4f812af27b400`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 23 Feb 2026 17:42:34 GMT
ARG RELEASE
# Mon, 23 Feb 2026 17:42:34 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 23 Feb 2026 17:42:35 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 23 Feb 2026 17:42:35 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 23 Feb 2026 17:43:25 GMT
ADD file:1243b7db425cac690d91f87ad37c1beec0d95da6b3942dc8084039fe1cc2baf4 in / 
# Mon, 23 Feb 2026 17:43:30 GMT
CMD ["/bin/bash"]
# Sat, 21 Mar 2026 04:40:25 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 21 Mar 2026 04:40:25 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 21 Mar 2026 04:40:25 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Sat, 21 Mar 2026 04:40:25 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 21 Mar 2026 04:40:25 GMT
ENV JAVA_VERSION=jdk-25.0.2+10
# Sat, 21 Mar 2026 04:42:53 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='987387933b64b9833846dee373b640440d3e1fd48a04804ec01a6dbf718e8ab8';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.2%2B10/OpenJDK25U-jdk_x64_linux_hotspot_25.0.2_10.tar.gz';          ;;        arm64)          ESUM='a9d73e711d967dc44896d4f430f73a68fd33590dabc29a7f2fb9f593425b854c';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.2%2B10/OpenJDK25U-jdk_aarch64_linux_hotspot_25.0.2_10.tar.gz';          ;;        ppc64el)          ESUM='b262b735b215173003766da36588d5f717dceada0286db41b439f93fb2ada468';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.2%2B10/OpenJDK25U-jdk_ppc64le_linux_hotspot_25.0.2_10.tar.gz';          ;;        riscv64)          ESUM='168119e4fba350f4e6b3ca92450a2b90a8502b89a235a04415e9adf9f5d3164e';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.2%2B10/OpenJDK25U-jdk_riscv64_linux_hotspot_25.0.2_10.tar.gz';          ;;        s390x)          ESUM='15e5cbcadcf3d43623c31b825063cdc2817b9f1ba840b51dc6ef70e5d33c84e3';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.2%2B10/OpenJDK25U-jdk_s390x_linux_hotspot_25.0.2_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     savedAptMark="$(apt-mark showmanual)";     apt-get update;     apt-get install -y --no-install-recommends wget gnupg;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     apt-mark auto '.*' > /dev/null;     apt-mark manual $savedAptMark > /dev/null;     apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false;     rm -rf /var/lib/apt/lists/*;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Sat, 21 Mar 2026 04:43:07 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Sat, 21 Mar 2026 04:43:08 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Sat, 21 Mar 2026 04:43:08 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Sat, 21 Mar 2026 04:43:08 GMT
CMD ["jshell"]
# Sun, 22 Mar 2026 19:23:44 GMT
ENV LEIN_VERSION=2.12.0
# Sun, 22 Mar 2026 19:23:44 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Sun, 22 Mar 2026 19:23:44 GMT
WORKDIR /tmp
# Sun, 22 Mar 2026 19:24:54 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Sun, 22 Mar 2026 19:24:54 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Sun, 22 Mar 2026 19:24:54 GMT
ENV LEIN_ROOT=1
# Sun, 22 Mar 2026 19:25:10 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Sun, 22 Mar 2026 19:25:10 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Sun, 22 Mar 2026 19:25:10 GMT
ENTRYPOINT ["entrypoint"]
# Sun, 22 Mar 2026 19:25:10 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:866473980fd7aa6ac5a8a995315a35248ab945008a1938bd15f65082df53b2d3`  
		Last Modified: Mon, 23 Feb 2026 17:51:46 GMT  
		Size: 31.0 MB (30960145 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6a39ea40737df0869a665cb1cd59261c3e337da5cacd4b5bf17fab5765e174b`  
		Last Modified: Sat, 21 Mar 2026 04:46:34 GMT  
		Size: 13.8 MB (13849902 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c61a4c41ee7ac84fc9d708e3b438f588cbe9de5cbf14f708499a9366509dbf6`  
		Last Modified: Sat, 21 Mar 2026 04:46:45 GMT  
		Size: 90.9 MB (90910647 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:595de38fa3ddd618163afb8e9f42eb19f6a4c7a8ce9d4f89f4b6109fbd005c85`  
		Last Modified: Sat, 21 Mar 2026 04:46:30 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f1c0a53cfa8928ee67aa8695518a1b7848abb7f6d41d75e58ae9af45a3a9be2`  
		Last Modified: Sun, 22 Mar 2026 19:27:09 GMT  
		Size: 14.5 MB (14468475 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e74d78ea6209ef839a930c649820f8442292450261dd6ce5fcbe5dfc1fd0e61b`  
		Last Modified: Sun, 22 Mar 2026 19:27:08 GMT  
		Size: 4.5 MB (4517761 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3e70e0506d73a4c0175ef3caf81fd2acdfa6438d1b240d37523c05d1cbed12d`  
		Last Modified: Sun, 22 Mar 2026 19:27:06 GMT  
		Size: 402.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-lein-noble` - unknown; unknown

```console
$ docker pull clojure@sha256:601f1071d1a6215ae22ae5047eae84c79051dfd1bbb4b2fc6f737050a88988ac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3476482 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0fecb186b8abf5d3bf0ef114d64e6c5d34c48440b552e3f7dcd6f183739d543b`

```dockerfile
```

-	Layers:
	-	`sha256:89c9c3ef0ae0ae96b5c7758e8b993c0aa6febeeb0fcaa0bd3791bca6031548c0`  
		Last Modified: Sun, 22 Mar 2026 19:27:07 GMT  
		Size: 3.5 MB (3458082 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:161c255bf6596c8dbafb51928be7e9896e9ed3b2306311ecfb69090ca342027b`  
		Last Modified: Sun, 22 Mar 2026 19:27:06 GMT  
		Size: 18.4 KB (18400 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-25-lein-noble` - linux; s390x

```console
$ docker pull clojure@sha256:4bf4fb5d6bb48b4de0119a19d09906b25be08083069a9752d0a60747487d8fc4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **153.6 MB (153605501 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bfb435dfefcc3e2e7e2a2cbc597c242f36242c1645b3ddb98eb4bd8f217a7002`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Fri, 03 Apr 2026 15:12:46 GMT
ARG RELEASE
# Fri, 03 Apr 2026 15:12:46 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 03 Apr 2026 15:12:46 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 03 Apr 2026 15:12:48 GMT
ADD file:31d45a66208318e1066130bac8975f44dea6e7e93cbfb2d29b0888e686bb10d5 in / 
# Fri, 03 Apr 2026 15:12:48 GMT
CMD ["/bin/bash"]
# Tue, 07 Apr 2026 03:10:25 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 07 Apr 2026 03:10:25 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Apr 2026 03:10:25 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 07 Apr 2026 03:10:25 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 03:10:25 GMT
ENV JAVA_VERSION=jdk-25.0.2+10
# Tue, 07 Apr 2026 03:10:37 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='987387933b64b9833846dee373b640440d3e1fd48a04804ec01a6dbf718e8ab8';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.2%2B10/OpenJDK25U-jdk_x64_linux_hotspot_25.0.2_10.tar.gz';          ;;        arm64)          ESUM='a9d73e711d967dc44896d4f430f73a68fd33590dabc29a7f2fb9f593425b854c';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.2%2B10/OpenJDK25U-jdk_aarch64_linux_hotspot_25.0.2_10.tar.gz';          ;;        ppc64el)          ESUM='b262b735b215173003766da36588d5f717dceada0286db41b439f93fb2ada468';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.2%2B10/OpenJDK25U-jdk_ppc64le_linux_hotspot_25.0.2_10.tar.gz';          ;;        riscv64)          ESUM='168119e4fba350f4e6b3ca92450a2b90a8502b89a235a04415e9adf9f5d3164e';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.2%2B10/OpenJDK25U-jdk_riscv64_linux_hotspot_25.0.2_10.tar.gz';          ;;        s390x)          ESUM='15e5cbcadcf3d43623c31b825063cdc2817b9f1ba840b51dc6ef70e5d33c84e3';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.2%2B10/OpenJDK25U-jdk_s390x_linux_hotspot_25.0.2_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     savedAptMark="$(apt-mark showmanual)";     apt-get update;     apt-get install -y --no-install-recommends wget gnupg;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     apt-mark auto '.*' > /dev/null;     apt-mark manual $savedAptMark > /dev/null;     apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false;     rm -rf /var/lib/apt/lists/*;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Tue, 07 Apr 2026 03:10:39 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 07 Apr 2026 03:10:39 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 07 Apr 2026 03:10:39 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 07 Apr 2026 03:10:39 GMT
CMD ["jshell"]
# Tue, 07 Apr 2026 05:46:57 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 07 Apr 2026 05:46:57 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 07 Apr 2026 05:46:57 GMT
WORKDIR /tmp
# Tue, 07 Apr 2026 05:47:08 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 07 Apr 2026 05:47:08 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 07 Apr 2026 05:47:08 GMT
ENV LEIN_ROOT=1
# Tue, 07 Apr 2026 05:47:10 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 07 Apr 2026 05:47:10 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 07 Apr 2026 05:47:10 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 07 Apr 2026 05:47:10 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:248eeda3355e38b5891b7f407370b5faea53785cd947438684bf34a757d0f83c`  
		Last Modified: Fri, 03 Apr 2026 15:57:06 GMT  
		Size: 29.9 MB (29911843 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4faede105445d3bd795bc7d8f0df624f6136d385a408c8b711fa2f889d29b74`  
		Last Modified: Tue, 07 Apr 2026 03:11:03 GMT  
		Size: 16.3 MB (16310110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8420605b37028e8129b0298a6b1ecc9d87364f35bd713709d378c9535aa90ee7`  
		Last Modified: Tue, 07 Apr 2026 03:11:06 GMT  
		Size: 88.4 MB (88369843 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43fbaf8d78a65877be7baa1bc40c97993c92212d890166ebb6fd149416207a53`  
		Last Modified: Tue, 07 Apr 2026 03:11:03 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dfe7de45d7938ec912b161175bc2075e02fa6d1b181887c104c44f5d9166854c`  
		Last Modified: Tue, 07 Apr 2026 05:47:23 GMT  
		Size: 14.5 MB (14493235 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00441dbb9c67edfff5eda33957e8cbd4d0e84e17f018c38da3d600d8a25b9ec4`  
		Last Modified: Tue, 07 Apr 2026 05:47:23 GMT  
		Size: 4.5 MB (4517725 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e87153fccc7a25c25b474edbb2e6475bbfdaed636e263d49a68bdc4e39a9050c`  
		Last Modified: Tue, 07 Apr 2026 05:47:23 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-lein-noble` - unknown; unknown

```console
$ docker pull clojure@sha256:3262c4209e0fa116e757d7621287d8a5c2b8cafa68a68ad231d40367294ec510
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3317676 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:425d5676206db31667d04087d232474a69c54a1812b0d30a25746ee1718b3826`

```dockerfile
```

-	Layers:
	-	`sha256:6fd6f0bc9eadaa9f34d8cd9971a969c65894359b482c06914e5a39ff0f71e043`  
		Last Modified: Tue, 07 Apr 2026 05:47:23 GMT  
		Size: 3.3 MB (3299311 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:82e18b173dad7ade1f74b9fb953bbd5412281ddb91c2eb15b7c96fb89bcaeb46`  
		Last Modified: Tue, 07 Apr 2026 05:47:23 GMT  
		Size: 18.4 KB (18365 bytes)  
		MIME: application/vnd.in-toto+json
