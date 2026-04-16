## `clojure:temurin-8-lein-2.12.0-jammy`

```console
$ docker pull clojure@sha256:cbd770c41c7f927f17cd9bd55fd6cc6e279af47926171a8e0157de1d0e4976aa
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `clojure:temurin-8-lein-2.12.0-jammy` - linux; amd64

```console
$ docker pull clojure@sha256:99644b6c49788c80665454612e01ca01ad863388dd9622fc7a159fc444637955
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **120.1 MB (120060850 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d3bb357699aa018785328d30bd21c9c5343022151734e5a172cc3480967fe84`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["lein","repl"]`

```dockerfile
# Fri, 10 Apr 2026 09:47:41 GMT
ARG RELEASE
# Fri, 10 Apr 2026 09:47:41 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 09:47:41 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 10 Apr 2026 09:47:43 GMT
ADD file:da2cd86408d9354e8bd817c8a4b8635a1d788cd20d0d70061ce02a173e8cf902 in / 
# Fri, 10 Apr 2026 09:47:44 GMT
CMD ["/bin/bash"]
# Wed, 15 Apr 2026 20:32:21 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 15 Apr 2026 20:32:21 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 15 Apr 2026 20:32:21 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 15 Apr 2026 20:32:21 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 20:32:21 GMT
ENV JAVA_VERSION=jdk8u482-b08
# Wed, 15 Apr 2026 20:32:24 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='e74becad56b4cc01f1556a671e578d3788789f5257f9499f6fbed84e63a55ecf';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u482-b08/OpenJDK8U-jdk_x64_linux_hotspot_8u482b08.tar.gz';          ;;        arm64)          ESUM='ada72fbf191fb287b4c1e54be372b64c40c27c2ffbfa01f880c92af11f4e7c94';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u482-b08/OpenJDK8U-jdk_aarch64_linux_hotspot_8u482b08.tar.gz';          ;;        armhf)          ESUM='1d0d16394e2fe637f9eb8e73e63ea6fe9ceee98337c0527aa058cee777ad638a';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u482-b08/OpenJDK8U-jdk_arm_linux_hotspot_8u482b08.tar.gz';          apt-get update;          DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1;          rm -rf /var/lib/apt/lists/*;          ;;        ppc64el)          ESUM='e77ba337c3ebb37fbef4961299f13fc4db87996ffd5470bdfb460cfc2ddb6053';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u482-b08/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u482b08.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig; # buildkit
# Wed, 15 Apr 2026 20:32:25 GMT
RUN set -eux;     echo "Verifying install ...";     echo "javac -version"; javac -version;     echo "java -version"; java -version;     echo "Complete." # buildkit
# Wed, 15 Apr 2026 20:32:25 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 15 Apr 2026 20:32:25 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 15 Apr 2026 22:00:46 GMT
ENV LEIN_VERSION=2.12.0
# Wed, 15 Apr 2026 22:00:46 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Wed, 15 Apr 2026 22:00:46 GMT
WORKDIR /tmp
# Wed, 15 Apr 2026 22:00:59 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Wed, 15 Apr 2026 22:00:59 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 15 Apr 2026 22:00:59 GMT
ENV LEIN_ROOT=1
# Wed, 15 Apr 2026 22:01:01 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Wed, 15 Apr 2026 22:01:01 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:f63eb04151bcac21ad049f8d781b97b219aba392c5457907f8f3e88e43eb48ec`  
		Last Modified: Fri, 10 Apr 2026 11:00:47 GMT  
		Size: 29.7 MB (29736498 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b699ac82f8f4bc202667b93bb403fa63a9d1637ce1f8fa60f2e6adceb8bf6be8`  
		Last Modified: Wed, 15 Apr 2026 20:32:38 GMT  
		Size: 16.2 MB (16150818 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3dfae8fec46c3d37535117b69a93963943ff3e3de751e2aa89287f69ec47171a`  
		Last Modified: Wed, 15 Apr 2026 20:32:39 GMT  
		Size: 55.2 MB (55172941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1d393a668fd7abdb353104b0fce5968b214d5ac3ff3cbb65251bdfe6116b21b`  
		Last Modified: Wed, 15 Apr 2026 20:32:33 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db2b0e71db5598e689453f02b98ac96955ee8ed91cbe61b6272a4122020be927`  
		Last Modified: Wed, 15 Apr 2026 20:32:37 GMT  
		Size: 2.3 KB (2308 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2db35806702ad7f5448d0db301254090fc41d57cc6da81293542fcc7fd1123f`  
		Last Modified: Wed, 15 Apr 2026 22:01:11 GMT  
		Size: 14.5 MB (14480419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa5b093f976bb7bbe03f4769136f9e3b17e04bc25cc7f577cdf73755d8374a25`  
		Last Modified: Wed, 15 Apr 2026 22:01:11 GMT  
		Size: 4.5 MB (4517707 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-lein-2.12.0-jammy` - unknown; unknown

```console
$ docker pull clojure@sha256:89e540848189f88465e5f61c36b402128652638d361ed6a878c310470a1aeeb9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4028581 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aea8a50076e1fcd189f3416df1cb9c89b725a659771061b2ebf9200baf057fb5`

```dockerfile
```

-	Layers:
	-	`sha256:c3170c2d4b540eb3e776a97823bba4411549ccd2f4a22c070e4d479d5de92feb`  
		Last Modified: Wed, 15 Apr 2026 22:01:10 GMT  
		Size: 4.0 MB (4012686 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:710d871908abbeae605dfb9843fa806bfb13047e288a9151656ef25277fd36ec`  
		Last Modified: Wed, 15 Apr 2026 22:01:10 GMT  
		Size: 15.9 KB (15895 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-lein-2.12.0-jammy` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:51db8a0f271f9549ca97960a0d9b5c9fc50b0fafe6a2a97aa489f5eafb4c4791
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **116.9 MB (116942978 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:45b61f1ea5f211cab0895fd490177c43c19b99d011779ae8fe34aa508874bfe1`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["lein","repl"]`

```dockerfile
# Fri, 10 Apr 2026 09:49:11 GMT
ARG RELEASE
# Fri, 10 Apr 2026 09:49:11 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 09:49:11 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 10 Apr 2026 09:49:13 GMT
ADD file:94ca084e2c34d90b4443d18fa6a7d983767fa1575d4bd2c06f6e31adfea270da in / 
# Fri, 10 Apr 2026 09:49:13 GMT
CMD ["/bin/bash"]
# Wed, 15 Apr 2026 20:32:43 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 15 Apr 2026 20:32:43 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 15 Apr 2026 20:32:43 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 15 Apr 2026 20:32:43 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 20:32:43 GMT
ENV JAVA_VERSION=jdk8u482-b08
# Wed, 15 Apr 2026 20:32:47 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='e74becad56b4cc01f1556a671e578d3788789f5257f9499f6fbed84e63a55ecf';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u482-b08/OpenJDK8U-jdk_x64_linux_hotspot_8u482b08.tar.gz';          ;;        arm64)          ESUM='ada72fbf191fb287b4c1e54be372b64c40c27c2ffbfa01f880c92af11f4e7c94';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u482-b08/OpenJDK8U-jdk_aarch64_linux_hotspot_8u482b08.tar.gz';          ;;        armhf)          ESUM='1d0d16394e2fe637f9eb8e73e63ea6fe9ceee98337c0527aa058cee777ad638a';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u482-b08/OpenJDK8U-jdk_arm_linux_hotspot_8u482b08.tar.gz';          apt-get update;          DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1;          rm -rf /var/lib/apt/lists/*;          ;;        ppc64el)          ESUM='e77ba337c3ebb37fbef4961299f13fc4db87996ffd5470bdfb460cfc2ddb6053';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u482-b08/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u482b08.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig; # buildkit
# Wed, 15 Apr 2026 20:32:47 GMT
RUN set -eux;     echo "Verifying install ...";     echo "javac -version"; javac -version;     echo "java -version"; java -version;     echo "Complete." # buildkit
# Wed, 15 Apr 2026 20:32:47 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 15 Apr 2026 20:32:47 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 15 Apr 2026 22:12:12 GMT
ENV LEIN_VERSION=2.12.0
# Wed, 15 Apr 2026 22:12:12 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Wed, 15 Apr 2026 22:12:12 GMT
WORKDIR /tmp
# Wed, 15 Apr 2026 22:12:25 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Wed, 15 Apr 2026 22:12:25 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 15 Apr 2026 22:12:25 GMT
ENV LEIN_ROOT=1
# Wed, 15 Apr 2026 22:12:27 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Wed, 15 Apr 2026 22:12:27 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:6edbc812af48552062d74659cf0a08b413dbfdbacdd5aac73329d889d9b3b44a`  
		Last Modified: Fri, 10 Apr 2026 11:00:55 GMT  
		Size: 27.6 MB (27606543 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90a116ac60a9bda7df2aa8d5f8c599e43b76fc505884b313fa5a950252ed9b69`  
		Last Modified: Wed, 15 Apr 2026 20:33:00 GMT  
		Size: 16.1 MB (16075202 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53614aca3bb32d1a5095ef396c08b4a7292999ad4a296c5ef9f8a53222ae5e3b`  
		Last Modified: Wed, 15 Apr 2026 20:33:01 GMT  
		Size: 54.3 MB (54261216 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e88e93f626800c3e743b24f70c0f766f3debe0ba6f4fe4007f364e298391e35b`  
		Last Modified: Wed, 15 Apr 2026 20:32:59 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f626c4297327dd6abfea8f0acb8ea0be823687a7a4e4f87e1cceb14b277b937e`  
		Last Modified: Wed, 15 Apr 2026 20:32:59 GMT  
		Size: 2.3 KB (2308 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b6d1eaa8aa530b80e3421da056b5cfb94d867a02b504e4a9215070e20dda3c6`  
		Last Modified: Wed, 15 Apr 2026 22:12:38 GMT  
		Size: 14.5 MB (14479874 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bcc45960523b57dec2d8cd4e7579d73adc7e7e3d0467a9152c2d29fcca63bfca`  
		Last Modified: Wed, 15 Apr 2026 22:12:37 GMT  
		Size: 4.5 MB (4517677 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-lein-2.12.0-jammy` - unknown; unknown

```console
$ docker pull clojure@sha256:4d5f87eda961c8d15114b83300401ea111b0ae9eae6d01387c45ad4f5439c935
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4029026 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4df0a1ea815c4804f60df5819a65d2a9bac0b58f9595ca10197f512948f4f8f2`

```dockerfile
```

-	Layers:
	-	`sha256:bf3b1bde90c89d8bf36e797c87eb97bf5fe168e02a16fee4199f71c7fcb5b01c`  
		Last Modified: Wed, 15 Apr 2026 22:12:37 GMT  
		Size: 4.0 MB (4013036 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3f6b012708a6b65eb4e0b19fae12ea25856bb36604ecebc501e603578ac3e49a`  
		Last Modified: Wed, 15 Apr 2026 22:12:38 GMT  
		Size: 16.0 KB (15990 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-lein-2.12.0-jammy` - linux; ppc64le

```console
$ docker pull clojure@sha256:3bc4c31a9874c73453dda5a419baa49cab27bc758d09628c8b7f3016db4ed619
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.0 MB (123967049 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:92a505e74648f3730eb6cb45b15b6a55cd994130e9765a0ca45b38a0150f30f1`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["lein","repl"]`

```dockerfile
# Sun, 22 Mar 2026 18:11:34 GMT
ARG RELEASE
# Sun, 22 Mar 2026 18:11:34 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 22 Mar 2026 18:11:34 GMT
LABEL org.opencontainers.image.version=22.04
# Sun, 22 Mar 2026 18:11:37 GMT
ADD file:268be611d24f69c3d8e480314cd587652e4c89a6032236737057c8b64f2379da in / 
# Sun, 22 Mar 2026 18:11:38 GMT
CMD ["/bin/bash"]
# Wed, 01 Apr 2026 20:20:51 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 01 Apr 2026 20:20:51 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 01 Apr 2026 20:20:51 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 01 Apr 2026 20:20:51 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 01 Apr 2026 20:20:51 GMT
ENV JAVA_VERSION=jdk8u482-b08
# Wed, 01 Apr 2026 20:21:00 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='e74becad56b4cc01f1556a671e578d3788789f5257f9499f6fbed84e63a55ecf';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u482-b08/OpenJDK8U-jdk_x64_linux_hotspot_8u482b08.tar.gz';          ;;        arm64)          ESUM='ada72fbf191fb287b4c1e54be372b64c40c27c2ffbfa01f880c92af11f4e7c94';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u482-b08/OpenJDK8U-jdk_aarch64_linux_hotspot_8u482b08.tar.gz';          ;;        armhf)          ESUM='1d0d16394e2fe637f9eb8e73e63ea6fe9ceee98337c0527aa058cee777ad638a';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u482-b08/OpenJDK8U-jdk_arm_linux_hotspot_8u482b08.tar.gz';          apt-get update;          DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1;          rm -rf /var/lib/apt/lists/*;          ;;        ppc64el)          ESUM='e77ba337c3ebb37fbef4961299f13fc4db87996ffd5470bdfb460cfc2ddb6053';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u482-b08/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u482b08.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig; # buildkit
# Wed, 01 Apr 2026 20:21:03 GMT
RUN set -eux;     echo "Verifying install ...";     echo "javac -version"; javac -version;     echo "java -version"; java -version;     echo "Complete." # buildkit
# Wed, 01 Apr 2026 20:21:04 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 01 Apr 2026 20:21:04 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 01 Apr 2026 21:39:46 GMT
ENV LEIN_VERSION=2.12.0
# Wed, 01 Apr 2026 21:39:46 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Wed, 01 Apr 2026 21:39:46 GMT
WORKDIR /tmp
# Wed, 01 Apr 2026 21:40:02 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Wed, 01 Apr 2026 21:40:02 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 01 Apr 2026 21:40:02 GMT
ENV LEIN_ROOT=1
# Wed, 01 Apr 2026 21:40:06 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Wed, 01 Apr 2026 21:40:06 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:6fb1b04a0a70d070de8a04181c7b855a46b1ea4f771660ae7f0783acd4569be2`  
		Last Modified: Sun, 22 Mar 2026 18:43:46 GMT  
		Size: 34.6 MB (34649660 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e568bb13a59c072b3af8c406e7b451459d28a2bdf653f96393ea9610f7d09959`  
		Last Modified: Wed, 01 Apr 2026 20:21:27 GMT  
		Size: 17.6 MB (17622524 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a466cb91d60c12ef2f2ef31a16b61be170026654e23713e63af5dc792239c6f`  
		Last Modified: Wed, 01 Apr 2026 20:21:31 GMT  
		Size: 52.7 MB (52652143 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:269cef637945ee94a49dcd4126081f85b8c87b30a479e74ae4f41cac1e7d6d2f`  
		Last Modified: Wed, 01 Apr 2026 20:21:29 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9579f76cd02fb4009f1f98ff5d2fb5a780091ba9a44d68603a54b118fc52524a`  
		Last Modified: Wed, 01 Apr 2026 20:21:29 GMT  
		Size: 2.3 KB (2304 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2353c67af23e1c89a34c69eca2572d99a453715ee5eb461aa5e6dcf61e32f888`  
		Last Modified: Wed, 01 Apr 2026 21:40:29 GMT  
		Size: 14.5 MB (14522520 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c236d5102e8022e87c19896a35b8593847ebcdef0f6dbf36f91f9782d10b91e6`  
		Last Modified: Wed, 01 Apr 2026 21:40:29 GMT  
		Size: 4.5 MB (4517740 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-lein-2.12.0-jammy` - unknown; unknown

```console
$ docker pull clojure@sha256:65ebb295d23c41dd00491d271370b9f954d8c7a71ae67ddbbffa828570048453
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4031314 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b9f040d900142e6dc6ce1ca73d959dece0243431eedd9a54d5ab4a2f8ca3cae6`

```dockerfile
```

-	Layers:
	-	`sha256:6855b73550b54a7a1d186882eaaf61368ed2ce0a1e25d34d9cd888919dfdc3db`  
		Last Modified: Wed, 01 Apr 2026 21:40:29 GMT  
		Size: 4.0 MB (4015385 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c8ed3ad8c723dca06882f8749d22cf7c96e8a6724e376595533566b880ba9bf3`  
		Last Modified: Wed, 01 Apr 2026 21:40:28 GMT  
		Size: 15.9 KB (15929 bytes)  
		MIME: application/vnd.in-toto+json
