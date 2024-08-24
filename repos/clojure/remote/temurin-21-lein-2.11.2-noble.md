## `clojure:temurin-21-lein-2.11.2-noble`

```console
$ docker pull clojure@sha256:0e4260f15d59b7dc310bbbff30295fc886af59cac3cc5440995f4d80325ec8c7
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-21-lein-2.11.2-noble` - linux; amd64

```console
$ docker pull clojure@sha256:5e9dbf66de46279ed0baff4db1c4e2888d4f4bf189fa15289a71f7ca49a1420f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **251.9 MB (251880602 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:747338e00e004adea27b4e037d2c4980b820d0265852a42eccfe7dae80fd26f0`
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
ENV JAVA_VERSION=jdk-21.0.4+7
# Wed, 07 Aug 2024 18:04:12 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='51fb4d03a4429c39d397d3a03a779077159317616550e4e71624c9843083e7b9';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.4%2B7/OpenJDK21U-jdk_x64_linux_hotspot_21.0.4_7.tar.gz';          ;;        arm64)          ESUM='d768eecddd7a515711659e02caef8516b7b7177fa34880a56398fd9822593a79';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.4%2B7/OpenJDK21U-jdk_aarch64_linux_hotspot_21.0.4_7.tar.gz';          ;;        ppc64el)          ESUM='c208cd0fb90560644a90f928667d2f53bfe408c957a5e36206585ad874427761';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.4%2B7/OpenJDK21U-jdk_ppc64le_linux_hotspot_21.0.4_7.tar.gz';          ;;        riscv64)          ESUM='b04fd7f52d18268a935f1a7144dae802b25db600ec97156ddd46b3100cbd13da';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.4%2B7/OpenJDK21U-jdk_riscv64_linux_hotspot_21.0.4_7.tar.gz';          ;;        s390x)          ESUM='c900c8d64fab1e53274974fa4a4c736a5a3754485a5c56f4947281480773658a';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.4%2B7/OpenJDK21U-jdk_s390x_linux_hotspot_21.0.4_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
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
	-	`sha256:facf7d693a40c7b09d711beecddef9142e6074a9d517b5b2f44a16299654b031`  
		Last Modified: Fri, 23 Aug 2024 19:28:43 GMT  
		Size: 158.6 MB (158587392 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb3fe075c198ddd7a31193d47754cdb43d384b3bcd7585284f478d8bd5fa5107`  
		Last Modified: Fri, 23 Aug 2024 19:28:30 GMT  
		Size: 175.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad28f0ce2ee5faf000467e3072dbaa09ec07d716c591a6871791efa036d05e9d`  
		Last Modified: Fri, 23 Aug 2024 19:28:30 GMT  
		Size: 2.1 KB (2108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:021aafdaa6dbd5d3ae77de45c1678294d78dfab76b89429b522f87ad0b8d80cb`  
		Last Modified: Fri, 23 Aug 2024 20:04:31 GMT  
		Size: 38.6 MB (38559981 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f7abfdfb65944380f19099c716a7a97a90ff4ff6a150083404edabb8d95f2d3`  
		Last Modified: Fri, 23 Aug 2024 20:04:30 GMT  
		Size: 4.4 MB (4398014 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a981f182b6a6bac7a7ba744808da5c3b6d66731aa871d2986cbd4dafaeee55ff`  
		Last Modified: Fri, 23 Aug 2024 20:04:30 GMT  
		Size: 399.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-lein-2.11.2-noble` - unknown; unknown

```console
$ docker pull clojure@sha256:7e98982470ede7ef7428acb5a7a379a52a325b67ee9c272ed283c2df4fdd45b5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.8 MB (4827641 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0dec383cbf25dded10079c86768c43b82183ac8e0b36b6a044f62b65c9d56a42`

```dockerfile
```

-	Layers:
	-	`sha256:f29efca97a18fac873b0f630a99933921ccac25648aaa18488cdd6044f01dec9`  
		Last Modified: Fri, 23 Aug 2024 20:04:30 GMT  
		Size: 4.8 MB (4809272 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c30a50e781482afdf98b4f59b584a14970bf47787e6852b47e5a1b3fc66cbedb`  
		Last Modified: Fri, 23 Aug 2024 20:04:30 GMT  
		Size: 18.4 KB (18369 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-lein-2.11.2-noble` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:4f032915bf4e3d197255ae9a293e499b4ec01ccf606571f8629b5cc198366cb1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **250.7 MB (250654188 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e144b61e23c819e6c2a4ccdbb27c2f496347f8ea3dcfc25c788479393b1900c1`
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
ENV JAVA_VERSION=jdk-21.0.4+7
# Wed, 07 Aug 2024 18:04:12 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='51fb4d03a4429c39d397d3a03a779077159317616550e4e71624c9843083e7b9';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.4%2B7/OpenJDK21U-jdk_x64_linux_hotspot_21.0.4_7.tar.gz';          ;;        arm64)          ESUM='d768eecddd7a515711659e02caef8516b7b7177fa34880a56398fd9822593a79';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.4%2B7/OpenJDK21U-jdk_aarch64_linux_hotspot_21.0.4_7.tar.gz';          ;;        ppc64el)          ESUM='c208cd0fb90560644a90f928667d2f53bfe408c957a5e36206585ad874427761';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.4%2B7/OpenJDK21U-jdk_ppc64le_linux_hotspot_21.0.4_7.tar.gz';          ;;        riscv64)          ESUM='b04fd7f52d18268a935f1a7144dae802b25db600ec97156ddd46b3100cbd13da';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.4%2B7/OpenJDK21U-jdk_riscv64_linux_hotspot_21.0.4_7.tar.gz';          ;;        s390x)          ESUM='c900c8d64fab1e53274974fa4a4c736a5a3754485a5c56f4947281480773658a';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.4%2B7/OpenJDK21U-jdk_s390x_linux_hotspot_21.0.4_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
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
	-	`sha256:e14f04caf9bed59074ef3aef2f88e85708db40de00edc54ae8ff795d1c4495d7`  
		Last Modified: Fri, 23 Aug 2024 19:46:09 GMT  
		Size: 156.8 MB (156756964 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b24eef44af83099ffdc11fb18199e5203c9ba74be9d1caf8a92782368b78d07`  
		Last Modified: Fri, 23 Aug 2024 19:45:59 GMT  
		Size: 175.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba26bf8b117fb371b47bc0e1c92c8bbf4937ba2e3fe7ce5b58222c2dc1a72586`  
		Last Modified: Fri, 23 Aug 2024 19:45:59 GMT  
		Size: 2.1 KB (2109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f3d7d675613241ff675bf02f1cf60b1a21f330bf15adda996dbee75139f74de`  
		Last Modified: Fri, 23 Aug 2024 20:54:31 GMT  
		Size: 38.6 MB (38623963 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0cabea6bef43a9da2c01368845ee82b9d0c7955d32851a6ab1db40afb4d49ed`  
		Last Modified: Fri, 23 Aug 2024 20:54:31 GMT  
		Size: 4.4 MB (4398002 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6aa9d61e52e73fa4c6259cba089ea51c2e693f3515deb9cace17d86552a0f0a`  
		Last Modified: Fri, 23 Aug 2024 20:54:30 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-lein-2.11.2-noble` - unknown; unknown

```console
$ docker pull clojure@sha256:b55d1df5363986778926ad4e8e7eb4a4e80f8bf81bc1142b33c932a04431077a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.0 MB (4966271 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eddfadac756854bdd3418b0a91c10d645cde401ddfe986775d36e6ea97b4f0c1`

```dockerfile
```

-	Layers:
	-	`sha256:b732d68f9dde72c4028b6d220825f2a485be8d238b271d1165a17f49b6548723`  
		Last Modified: Fri, 23 Aug 2024 20:54:30 GMT  
		Size: 4.9 MB (4947609 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a800fe39c9b94d0186a1541718c3ff5315e7d42a887ef78065e24e073fab2fe2`  
		Last Modified: Fri, 23 Aug 2024 20:54:29 GMT  
		Size: 18.7 KB (18662 bytes)  
		MIME: application/vnd.in-toto+json
