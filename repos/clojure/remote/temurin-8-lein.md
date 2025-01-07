## `clojure:temurin-8-lein`

```console
$ docker pull clojure@sha256:03aec6f0ce014833c9e30964281eb3e501fd4527557e5e954ad14346e8997a5a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-8-lein` - linux; amd64

```console
$ docker pull clojure@sha256:429a7027b882652f1fed4048e3bc3d4e8a8cc4f6b4e3fff867f6302a4d7ff28d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **189.6 MB (189613016 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d978cef75f0b5b49f82c1851530b155110a73a44ed8d6a18d23cc63dc9a4e03`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["lein","repl"]`

```dockerfile
# Wed, 11 Sep 2024 16:25:16 GMT
ARG RELEASE
# Wed, 11 Sep 2024 16:25:16 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 11 Sep 2024 16:25:16 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 11 Sep 2024 16:25:16 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 11 Sep 2024 16:25:17 GMT
ADD file:ebe009f86035c175ba244badd298a2582914415cf62783d510eab3a311a5d4e1 in / 
# Wed, 11 Sep 2024 16:25:18 GMT
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
ENV JAVA_VERSION=jdk8u432-b06
# Thu, 03 Oct 2024 17:49:34 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='abaaa90deadf51bd28921453baf2992b3dff6171bb7142f5bdd14ef269f7b245';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u432-b06/OpenJDK8U-jdk_x64_linux_hotspot_8u432b06.tar.gz';          ;;        arm64)          ESUM='383caabc20428e9500f2e07965317ed4387a0e336104483e29a9e06eeffbf26b';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u432-b06/OpenJDK8U-jdk_aarch64_linux_hotspot_8u432b06.tar.gz';          ;;        armhf)          ESUM='ff1ce3f6f1cf11987ab63f278b29cf1aae799652606c547f8a590e7acbd16b61';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u432-b06/OpenJDK8U-jdk_arm_linux_hotspot_8u432b06.tar.gz';          apt-get update;          DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1;          rm -rf /var/lib/apt/lists/*;          ;;        ppc64el)          ESUM='64fb17e83b79f9ad41dc18351a408bfe90324fd6360903ca5c0a740006c81be3';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u432-b06/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u432b06.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -r "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig; # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
RUN set -eux;     echo "Verifying install ...";     echo "javac -version"; javac -version;     echo "java -version"; java -version;     echo "Complete." # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 03 Oct 2024 17:49:34 GMT
ENV LEIN_VERSION=2.11.2
# Thu, 03 Oct 2024 17:49:34 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Thu, 03 Oct 2024 17:49:34 GMT
WORKDIR /tmp
# Thu, 03 Oct 2024 17:49:34 GMT
RUN set -eux; apt-get update && apt-get install -y make git gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "28a1a62668c5f427b413a8677e376affaa995f023b1fcd06e2d4c98ac1df5f3e *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Thu, 03 Oct 2024 17:49:34 GMT
ENV LEIN_ROOT=1
# Thu, 03 Oct 2024 17:49:34 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.0"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:6414378b647780fee8fd903ddb9541d134a1947ce092d08bdeb23a54cb3684ac`  
		Last Modified: Wed, 11 Sep 2024 17:24:41 GMT  
		Size: 29.5 MB (29535688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9249f08550d7d5c927ce79a2bcd2cf3104f70778fc0a870136ecd854c0cc143d`  
		Last Modified: Thu, 24 Oct 2024 00:56:50 GMT  
		Size: 16.1 MB (16142449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd348007a2bab865de854d23ccd36fde26ac79da81526b410eb604949ae5c00e`  
		Last Modified: Thu, 24 Oct 2024 00:56:52 GMT  
		Size: 103.6 MB (103632880 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4a932399772bc99224b18d5aa6d6521b059314093375b3c9cc857c7a9c2336f`  
		Last Modified: Thu, 24 Oct 2024 00:56:50 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7acc9dc90b5617adf999470853c386b3ec3915b306b0baffff98d87e7e1d757d`  
		Last Modified: Thu, 24 Oct 2024 00:56:50 GMT  
		Size: 2.3 KB (2308 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3209bdfed9eca2ff192ae6e5b02de6d7dbffc318e5ff2a0b5e0d6ddcd61d1fd7`  
		Last Modified: Thu, 24 Oct 2024 01:59:46 GMT  
		Size: 35.8 MB (35785349 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ac47abdfa6870f72b9ef1de189b26c090e7c41cdba513b737b8b4e61084404c`  
		Last Modified: Thu, 24 Oct 2024 01:59:45 GMT  
		Size: 4.5 MB (4514183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-lein` - unknown; unknown

```console
$ docker pull clojure@sha256:12b786800e7f1b9a1cb11f3e8ef576a68a2c53f4a35a2248560c8674cffcdb20
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5515670 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b7f2cf9d9d49ea4f43cd50f48b784908ce302b05c0dc4b0c066fea0a07b66e25`

```dockerfile
```

-	Layers:
	-	`sha256:0bf63ad7223e7d247b13f479411c6b8c6ef14299c6f811b51e5e2f8c84242705`  
		Last Modified: Thu, 24 Oct 2024 01:59:45 GMT  
		Size: 5.5 MB (5499070 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4c4097e42fdafa0d7dc9541554debc98c0d2d1e974303c1a7f7d40a66ce6f379`  
		Last Modified: Thu, 24 Oct 2024 01:59:45 GMT  
		Size: 16.6 KB (16600 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-lein` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:de5b21303fc3bd47653bde58cdb1501dd9ec3632161df825f21263b9497ee635
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **186.4 MB (186411276 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:996e932b56bd2a20c93ab1367a1c0865d5d70c8fbd9a20b99938b40f50885829`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["lein","repl"]`

```dockerfile
# Wed, 11 Sep 2024 16:26:04 GMT
ARG RELEASE
# Wed, 11 Sep 2024 16:26:04 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 11 Sep 2024 16:26:04 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 11 Sep 2024 16:26:04 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 11 Sep 2024 16:26:06 GMT
ADD file:53ce73ebbd6d87a234a33414686f12909aaaf28b7238593f746a327c7d004ce7 in / 
# Wed, 11 Sep 2024 16:26:06 GMT
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
ENV JAVA_VERSION=jdk8u432-b06
# Thu, 03 Oct 2024 17:49:34 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='abaaa90deadf51bd28921453baf2992b3dff6171bb7142f5bdd14ef269f7b245';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u432-b06/OpenJDK8U-jdk_x64_linux_hotspot_8u432b06.tar.gz';          ;;        arm64)          ESUM='383caabc20428e9500f2e07965317ed4387a0e336104483e29a9e06eeffbf26b';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u432-b06/OpenJDK8U-jdk_aarch64_linux_hotspot_8u432b06.tar.gz';          ;;        armhf)          ESUM='ff1ce3f6f1cf11987ab63f278b29cf1aae799652606c547f8a590e7acbd16b61';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u432-b06/OpenJDK8U-jdk_arm_linux_hotspot_8u432b06.tar.gz';          apt-get update;          DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1;          rm -rf /var/lib/apt/lists/*;          ;;        ppc64el)          ESUM='64fb17e83b79f9ad41dc18351a408bfe90324fd6360903ca5c0a740006c81be3';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u432-b06/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u432b06.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -r "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig; # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
RUN set -eux;     echo "Verifying install ...";     echo "javac -version"; javac -version;     echo "java -version"; java -version;     echo "Complete." # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 03 Oct 2024 17:49:34 GMT
ENV LEIN_VERSION=2.11.2
# Thu, 03 Oct 2024 17:49:34 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Thu, 03 Oct 2024 17:49:34 GMT
WORKDIR /tmp
# Thu, 03 Oct 2024 17:49:34 GMT
RUN set -eux; apt-get update && apt-get install -y make git gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "28a1a62668c5f427b413a8677e376affaa995f023b1fcd06e2d4c98ac1df5f3e *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Thu, 03 Oct 2024 17:49:34 GMT
ENV LEIN_ROOT=1
# Thu, 03 Oct 2024 17:49:34 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.0"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:a186900671ab62e1dea364788f4e84c156e1825939914cfb5a6770be2b58b4da`  
		Last Modified: Wed, 11 Sep 2024 17:24:47 GMT  
		Size: 27.4 MB (27358329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4821edbf1831262baf113efdfde0f697240ca3efc1fbebee80c4279708d73f92`  
		Last Modified: Thu, 24 Oct 2024 00:58:15 GMT  
		Size: 16.1 MB (16062123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22e49e1bab60b0d076a12a465b5191397c7b1fde236f952b9ef5667d75b7fdb7`  
		Size: 102.7 MB (102746969 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78302cd59caf00d4442781d364292f654299cf8a4a5cf4418eda06fb99e697ca`  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8acb3667402d0a25e1734ff2d5aa437eac3d167ff9ced796aa2df0930e92fd27`  
		Last Modified: Thu, 24 Oct 2024 00:58:14 GMT  
		Size: 2.3 KB (2308 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba569d01b2bbbf19712baed7868ba3dfee6b52de00a8be778fd6755496e616be`  
		Last Modified: Thu, 24 Oct 2024 08:55:39 GMT  
		Size: 35.7 MB (35727236 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8dbade5c7af6facd9b381e3679d69b183e1041e397eade5abdd2196517b5770`  
		Last Modified: Thu, 24 Oct 2024 08:55:38 GMT  
		Size: 4.5 MB (4514150 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-lein` - unknown; unknown

```console
$ docker pull clojure@sha256:c76285152d8f000724e70a3c52723cfdcf44af6cb00042d4e8bd7a5dc72ae841
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5522216 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c1c7fc4aea844276cea55f15bf5916a0b2decef1d80f90b41b8c59fb5f7b8088`

```dockerfile
```

-	Layers:
	-	`sha256:4cba8bc84385fd9e302017aa60c6ce47147f7a8a758b7800a23998bf7be0540d`  
		Size: 5.5 MB (5505497 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f4c372bde2cab88ba7f16ce799485f98160c233fbea6ec7d6f83f376fcc27785`  
		Last Modified: Thu, 24 Oct 2024 08:55:38 GMT  
		Size: 16.7 KB (16719 bytes)  
		MIME: application/vnd.in-toto+json
