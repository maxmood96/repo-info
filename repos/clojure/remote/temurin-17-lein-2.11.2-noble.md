## `clojure:temurin-17-lein-2.11.2-noble`

```console
$ docker pull clojure@sha256:763d2fb9d8971421781f00ec06e391362f5f642be5fe61a3353f6752ffd4a939
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-17-lein-2.11.2-noble` - linux; amd64

```console
$ docker pull clojure@sha256:a2dcfaa5fb13ea70ac61668112446cb2d478418e8a08e1058f9359a4c7a4999a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **238.5 MB (238470400 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe7dfbf537f40480561a302a0222d4a8519448cc13bb68a4441810b449ecabd4`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Thu, 01 Aug 2024 14:23:53 GMT
ARG RELEASE
# Thu, 01 Aug 2024 14:23:53 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 01 Aug 2024 14:23:53 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 01 Aug 2024 14:23:53 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 01 Aug 2024 14:23:55 GMT
ADD file:c2e78eb585ec4e503f14c4ea98f4962c998f5eb075749507953f85387742694b in / 
# Thu, 01 Aug 2024 14:23:55 GMT
CMD ["/bin/bash"]
# Wed, 07 Aug 2024 18:04:12 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 07 Aug 2024 18:04:12 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 07 Aug 2024 18:04:12 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 07 Aug 2024 18:04:12 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 07 Aug 2024 18:04:12 GMT
ENV JAVA_VERSION=jdk-17.0.12+7
# Wed, 07 Aug 2024 18:04:12 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='9d4dd339bf7e6a9dcba8347661603b74c61ab2a5083ae67bf76da6285da8a778';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jdk_x64_linux_hotspot_17.0.12_7.tar.gz';          ;;        arm64)          ESUM='8257de06bf37f0c8f19f8d542e2ab5a4e17db3ca5f29d041bd0b02ab265db021';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jdk_aarch64_linux_hotspot_17.0.12_7.tar.gz';          ;;        armhf)          ESUM='ce7873ebf40ed0eb1089941ead4d3af79a205b1264f3162860d26ae957572b74';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jdk_arm_linux_hotspot_17.0.12_7.tar.gz';          ;;        ppc64el)          ESUM='c97988e5a99b8ae0c47ba330b0883398c7433312db0051d8c5ff97911bae1605';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jdk_ppc64le_linux_hotspot_17.0.12_7.tar.gz';          ;;        riscv64)          ESUM='d024c100eba4709970716ddcac757ba5e3122a8ff9c6f539ff8bac5b47f51f3a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jdk_riscv64_linux_hotspot_17.0.12_7.tar.gz';          ;;        s390x)          ESUM='e244947f4c9176bd559598874b6ecaafcabba19c7067271cebb78708c2e9d14f';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jdk_s390x_linux_hotspot_17.0.12_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Wed, 07 Aug 2024 18:04:12 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 07 Aug 2024 18:04:12 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 07 Aug 2024 18:04:12 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 07 Aug 2024 18:04:12 GMT
CMD ["jshell"]
# Wed, 07 Aug 2024 18:04:12 GMT
ENV LEIN_VERSION=2.11.2
# Wed, 07 Aug 2024 18:04:12 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Wed, 07 Aug 2024 18:04:12 GMT
WORKDIR /tmp
# Wed, 07 Aug 2024 18:04:12 GMT
RUN set -eux; apt-get update && apt-get install -y make git gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "28a1a62668c5f427b413a8677e376affaa995f023b1fcd06e2d4c98ac1df5f3e *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Wed, 07 Aug 2024 18:04:12 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 07 Aug 2024 18:04:12 GMT
ENV LEIN_ROOT=1
# Wed, 07 Aug 2024 18:04:12 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.11.3"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Wed, 07 Aug 2024 18:04:12 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 07 Aug 2024 18:04:12 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 07 Aug 2024 18:04:12 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:eb993dcd6942ffcb7633f2cb271bd4b0a275fc9bdc8f5100c5b4d24694cacf50`  
		Last Modified: Fri, 02 Aug 2024 03:03:23 GMT  
		Size: 30.6 MB (30567306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef6d67df44ebaf68af30549648235de86e15355c7fc9afc496d8d73df71a7a3d`  
		Last Modified: Sat, 17 Aug 2024 01:12:58 GMT  
		Size: 19.8 MB (19765195 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:433fc9917055e1710168ae0a7dc40db5a8d87d2f79f9977e84de187b5502a391`  
		Last Modified: Fri, 23 Aug 2024 19:27:20 GMT  
		Size: 145.2 MB (145177489 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b197c2065e2b7fd4160e6e2efef0f6f7c48eb2bc798ba5397e259b4d7fae49f`  
		Last Modified: Fri, 23 Aug 2024 19:27:09 GMT  
		Size: 174.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b90d6083d60b2804b311f81ac07a4f3bea7d0c10b16b8153d50063b8aab22c98`  
		Last Modified: Fri, 23 Aug 2024 19:27:09 GMT  
		Size: 2.1 KB (2109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62d2cc290c7efd1e37813055820ead02f3651cbe94810c5122a8f9a5094f7426`  
		Last Modified: Fri, 23 Aug 2024 20:02:07 GMT  
		Size: 38.6 MB (38559647 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:593a802470fbcda9a3d3147e4bcf581f4c4d11121fd94a904a7a6f18ea4837cc`  
		Last Modified: Fri, 23 Aug 2024 20:02:07 GMT  
		Size: 4.4 MB (4398050 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7794797f51d0ae10f28f40c9d5d696e5c1ccb45fda7d47df5400e017904bbd51`  
		Last Modified: Fri, 23 Aug 2024 20:02:07 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-lein-2.11.2-noble` - unknown; unknown

```console
$ docker pull clojure@sha256:562f8d499c33a15f69e35292e1aa3afab31619c721ffafb904c317bf1f08bf58
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.8 MB (4827633 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4845ad4d799f41b883e45c6f4c5bc4041d8fd7c420ea2d2c1e0c16147353c1b0`

```dockerfile
```

-	Layers:
	-	`sha256:4598b2d00f1344f615ba0ecd8e3767280ee60a8d399702840e6bd4fdeb05f541`  
		Last Modified: Fri, 23 Aug 2024 20:02:07 GMT  
		Size: 4.8 MB (4809262 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d15aae9da9768e8f5bd93a2ea50f32ed9ffa0201e3e3d8b7b4f8534a541576f4`  
		Last Modified: Fri, 23 Aug 2024 20:02:07 GMT  
		Size: 18.4 KB (18371 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-lein-2.11.2-noble` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:0a9f5935305335951ef417e0a93d81fb0e2062aa2d3da424d1c3721aea598c88
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **237.9 MB (237864616 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:14a7e6be15d1292c97c57dd332a1296e9989b6e95d22accc0b96f867b701512c`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Thu, 01 Aug 2024 15:33:35 GMT
ARG RELEASE
# Thu, 01 Aug 2024 15:33:35 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 01 Aug 2024 15:33:35 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 01 Aug 2024 15:33:36 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 01 Aug 2024 15:33:38 GMT
ADD file:154285ca3d49a142bc6d59c9d48f14546f32b2d6de94387c30c1ba3759249b0f in / 
# Thu, 01 Aug 2024 15:33:38 GMT
CMD ["/bin/bash"]
# Wed, 07 Aug 2024 18:04:12 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 07 Aug 2024 18:04:12 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 07 Aug 2024 18:04:12 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 07 Aug 2024 18:04:12 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 07 Aug 2024 18:04:12 GMT
ENV JAVA_VERSION=jdk-17.0.12+7
# Wed, 07 Aug 2024 18:04:12 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='9d4dd339bf7e6a9dcba8347661603b74c61ab2a5083ae67bf76da6285da8a778';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jdk_x64_linux_hotspot_17.0.12_7.tar.gz';          ;;        arm64)          ESUM='8257de06bf37f0c8f19f8d542e2ab5a4e17db3ca5f29d041bd0b02ab265db021';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jdk_aarch64_linux_hotspot_17.0.12_7.tar.gz';          ;;        armhf)          ESUM='ce7873ebf40ed0eb1089941ead4d3af79a205b1264f3162860d26ae957572b74';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jdk_arm_linux_hotspot_17.0.12_7.tar.gz';          ;;        ppc64el)          ESUM='c97988e5a99b8ae0c47ba330b0883398c7433312db0051d8c5ff97911bae1605';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jdk_ppc64le_linux_hotspot_17.0.12_7.tar.gz';          ;;        riscv64)          ESUM='d024c100eba4709970716ddcac757ba5e3122a8ff9c6f539ff8bac5b47f51f3a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jdk_riscv64_linux_hotspot_17.0.12_7.tar.gz';          ;;        s390x)          ESUM='e244947f4c9176bd559598874b6ecaafcabba19c7067271cebb78708c2e9d14f';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jdk_s390x_linux_hotspot_17.0.12_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Wed, 07 Aug 2024 18:04:12 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 07 Aug 2024 18:04:12 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 07 Aug 2024 18:04:12 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 07 Aug 2024 18:04:12 GMT
CMD ["jshell"]
# Wed, 07 Aug 2024 18:04:12 GMT
ENV LEIN_VERSION=2.11.2
# Wed, 07 Aug 2024 18:04:12 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Wed, 07 Aug 2024 18:04:12 GMT
WORKDIR /tmp
# Wed, 07 Aug 2024 18:04:12 GMT
RUN set -eux; apt-get update && apt-get install -y make git gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "28a1a62668c5f427b413a8677e376affaa995f023b1fcd06e2d4c98ac1df5f3e *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Wed, 07 Aug 2024 18:04:12 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 07 Aug 2024 18:04:12 GMT
ENV LEIN_ROOT=1
# Wed, 07 Aug 2024 18:04:12 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.11.3"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Wed, 07 Aug 2024 18:04:12 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 07 Aug 2024 18:04:12 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 07 Aug 2024 18:04:12 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:1567e7ea90b67fc95ccdeeec39bdc3045098dee7e0c604975b957a9f8c0e9616`  
		Last Modified: Fri, 02 Aug 2024 07:40:09 GMT  
		Size: 29.9 MB (29910029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d730088f68183e8bde2999ed48782fec63b9dea3c9a5d270fdede5082140ac57`  
		Last Modified: Sat, 17 Aug 2024 01:35:47 GMT  
		Size: 21.0 MB (20962516 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63202666823207d23b114135036a4ba52640d00e0fe7d2cdc42c43005b27fb2c`  
		Last Modified: Fri, 23 Aug 2024 19:44:53 GMT  
		Size: 144.0 MB (143967366 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b75423c8553c1b04c70bfa26b7b46042513fbe5958d27b8b0492e7077aa97a94`  
		Last Modified: Fri, 23 Aug 2024 19:44:44 GMT  
		Size: 174.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d81e98ce99ed1262b36a32369d06f321168fc8039d61327ab23e19487dc0f122`  
		Last Modified: Fri, 23 Aug 2024 19:44:44 GMT  
		Size: 2.1 KB (2108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da0fbea1ccc79c6a224257e2936a7aea436aa40a58d885f133b15d25ef32f124`  
		Last Modified: Fri, 23 Aug 2024 20:51:37 GMT  
		Size: 38.6 MB (38623992 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76837f8c22b756bfad2bfc018718aa5daa119b88f1819e421d7f95e7598d2e68`  
		Last Modified: Fri, 23 Aug 2024 20:51:32 GMT  
		Size: 4.4 MB (4398000 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:849d33bd742c6ccb32dec2bdd36d71cd5c56141fbabf163fd8aff511265dcf69`  
		Last Modified: Fri, 23 Aug 2024 20:51:32 GMT  
		Size: 399.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-lein-2.11.2-noble` - unknown; unknown

```console
$ docker pull clojure@sha256:3676b7beae4d8c5c9375d32428018e17c2797558f24a7338c1918bbc945a68f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.0 MB (4966263 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:09667d72475cb4c812a5e6e66ce94805f348e9fd672942ff0505537b9eac753c`

```dockerfile
```

-	Layers:
	-	`sha256:4d437a06b15510e585843f3489edb9c67fa7ca33c856e1d0051be7c887256805`  
		Last Modified: Fri, 23 Aug 2024 20:51:31 GMT  
		Size: 4.9 MB (4947599 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d602af0fad3c865f21a9e9555b3308c27af09bb9b12205bf37ce3d8083784068`  
		Last Modified: Fri, 23 Aug 2024 20:51:31 GMT  
		Size: 18.7 KB (18664 bytes)  
		MIME: application/vnd.in-toto+json
