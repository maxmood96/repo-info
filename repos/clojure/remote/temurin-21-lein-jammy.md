## `clojure:temurin-21-lein-jammy`

```console
$ docker pull clojure@sha256:c185e6ec8d8cfa3a12329f5926ea3a42daf1d41900105a7e25850975184b1ad3
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-21-lein-jammy` - linux; amd64

```console
$ docker pull clojure@sha256:e83ede1baa0d1fdc074f19ef79ecccab857678afbc5034a469fa52ee4236977b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **246.6 MB (246627812 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c303d52290fe27d517ce14a400d5172f17f75fd7b7e90d7bf6c06ad4410efca`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Wed, 07 Aug 2024 18:04:12 GMT
ARG RELEASE
# Wed, 07 Aug 2024 18:04:12 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 07 Aug 2024 18:04:12 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 07 Aug 2024 18:04:12 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 07 Aug 2024 18:04:12 GMT
ADD file:2f8a54a5efd080fb81efea702b4e3e07d946eec7563fb2281bd28950c10ec462 in / 
# Wed, 07 Aug 2024 18:04:12 GMT
CMD ["/bin/bash"]
# Wed, 24 Jul 2024 22:19:06 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 24 Jul 2024 22:19:06 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Jul 2024 22:19:06 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 24 Jul 2024 22:19:06 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 24 Jul 2024 22:19:06 GMT
ENV JAVA_VERSION=jdk-21.0.4+7
# Wed, 24 Jul 2024 22:19:06 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='51fb4d03a4429c39d397d3a03a779077159317616550e4e71624c9843083e7b9';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.4%2B7/OpenJDK21U-jdk_x64_linux_hotspot_21.0.4_7.tar.gz';          ;;        arm64)          ESUM='d768eecddd7a515711659e02caef8516b7b7177fa34880a56398fd9822593a79';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.4%2B7/OpenJDK21U-jdk_aarch64_linux_hotspot_21.0.4_7.tar.gz';          ;;        ppc64el)          ESUM='c208cd0fb90560644a90f928667d2f53bfe408c957a5e36206585ad874427761';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.4%2B7/OpenJDK21U-jdk_ppc64le_linux_hotspot_21.0.4_7.tar.gz';          ;;        s390x)          ESUM='c900c8d64fab1e53274974fa4a4c736a5a3754485a5c56f4947281480773658a';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.4%2B7/OpenJDK21U-jdk_s390x_linux_hotspot_21.0.4_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Wed, 24 Jul 2024 22:19:06 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 24 Jul 2024 22:19:06 GMT
COPY entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 24 Jul 2024 22:19:06 GMT
ENTRYPOINT ["/bin/bash" "/__cacert_entrypoint.sh"]
# Wed, 24 Jul 2024 22:19:06 GMT
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
	-	`sha256:762bedf4b1b784c3de6c5022c5307d63123d3b7cdd59211317e37e9d477deaa0`  
		Last Modified: Fri, 09 Aug 2024 01:22:05 GMT  
		Size: 30.4 MB (30440714 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67d2822c71e1c49e3b52ca63c8ad15833449ee66e6c398a302eb046c556826e0`  
		Last Modified: Sat, 17 Aug 2024 01:12:37 GMT  
		Size: 17.4 MB (17415429 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:482fbf153ddc486288887c925609aba1a06123ef449197541916204000b32be3`  
		Last Modified: Sat, 17 Aug 2024 01:14:02 GMT  
		Size: 158.6 MB (158587052 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:880c2e95b386c797a96f9abf3551e5738cf995742285d5f45314d75676ed6d7a`  
		Last Modified: Sat, 17 Aug 2024 01:13:50 GMT  
		Size: 175.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d374cf93eba985e32df69f0d66d0f96d62292e4de04a8adf60ea4ab943bf0a9f`  
		Last Modified: Sat, 17 Aug 2024 01:13:50 GMT  
		Size: 1.9 KB (1867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c54246a2f096fdade477e1919dadd46ad28030267cd38742953e6cdad6c51ca`  
		Last Modified: Sat, 17 Aug 2024 01:59:47 GMT  
		Size: 35.8 MB (35784094 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f19e9ac8049b4429cdc7b952c2e6819d067737e62bf0b98f9ea3c454aab32e43`  
		Last Modified: Sat, 17 Aug 2024 01:59:47 GMT  
		Size: 4.4 MB (4398050 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:445b206ec84832c1c28d8b7ac57b8c81d6c1a0338e62051f7637bfae63f5d0e1`  
		Last Modified: Sat, 17 Aug 2024 01:59:47 GMT  
		Size: 399.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-lein-jammy` - unknown; unknown

```console
$ docker pull clojure@sha256:a8c0050f8fe4361a1735956dbb3b57eb0fd6147b20b7362a9568c3563ea3adc3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5368113 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bfe7732100561b18a09cbb2a1699b20bd709e5e0027c3affc838a40ebd412c2c`

```dockerfile
```

-	Layers:
	-	`sha256:f09718b9e762c3f5cff8310bffcfc882a81b3a5f07c0bbf6cd2ac1e555e41af7`  
		Last Modified: Sat, 17 Aug 2024 01:59:47 GMT  
		Size: 5.3 MB (5349744 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9fe71e9f373d155e92d465aa97ca56f09f4245606abc0ab3bce57795228ad4a5`  
		Last Modified: Sat, 17 Aug 2024 01:59:47 GMT  
		Size: 18.4 KB (18369 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-lein-jammy` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:5e11d0adb7a9cce8691684cb3e8277da2c43c6c28148d4912eff670d5ea1aff0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **244.1 MB (244111638 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9d66e2ddb4fc75a4e99b0b5b1c4904713b0059abf42d87c5d7741a2417ffd602`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Thu, 27 Jun 2024 19:23:22 GMT
ARG RELEASE
# Thu, 27 Jun 2024 19:23:22 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 27 Jun 2024 19:23:22 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 27 Jun 2024 19:23:22 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 27 Jun 2024 19:23:26 GMT
ADD file:2bed1fbf8253926f27dc275983c274712d836e9b6acdb1059d29c072d8f63a03 in / 
# Thu, 27 Jun 2024 19:23:26 GMT
CMD ["/bin/bash"]
# Wed, 24 Jul 2024 22:19:06 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 24 Jul 2024 22:19:06 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Jul 2024 22:19:06 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 24 Jul 2024 22:19:06 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 24 Jul 2024 22:19:06 GMT
ENV JAVA_VERSION=jdk-21.0.4+7
# Wed, 24 Jul 2024 22:19:06 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='51fb4d03a4429c39d397d3a03a779077159317616550e4e71624c9843083e7b9';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.4%2B7/OpenJDK21U-jdk_x64_linux_hotspot_21.0.4_7.tar.gz';          ;;        arm64)          ESUM='d768eecddd7a515711659e02caef8516b7b7177fa34880a56398fd9822593a79';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.4%2B7/OpenJDK21U-jdk_aarch64_linux_hotspot_21.0.4_7.tar.gz';          ;;        ppc64el)          ESUM='c208cd0fb90560644a90f928667d2f53bfe408c957a5e36206585ad874427761';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.4%2B7/OpenJDK21U-jdk_ppc64le_linux_hotspot_21.0.4_7.tar.gz';          ;;        s390x)          ESUM='c900c8d64fab1e53274974fa4a4c736a5a3754485a5c56f4947281480773658a';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.4%2B7/OpenJDK21U-jdk_s390x_linux_hotspot_21.0.4_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Wed, 24 Jul 2024 22:19:06 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 24 Jul 2024 22:19:06 GMT
COPY entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 24 Jul 2024 22:19:06 GMT
ENTRYPOINT ["/bin/bash" "/__cacert_entrypoint.sh"]
# Wed, 24 Jul 2024 22:19:06 GMT
CMD ["jshell"]
# Thu, 25 Jul 2024 20:19:09 GMT
ENV LEIN_VERSION=2.11.2
# Thu, 25 Jul 2024 20:19:09 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Thu, 25 Jul 2024 20:19:09 GMT
WORKDIR /tmp
# Thu, 25 Jul 2024 20:19:09 GMT
RUN set -eux; apt-get update && apt-get install -y make git gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "28a1a62668c5f427b413a8677e376affaa995f023b1fcd06e2d4c98ac1df5f3e *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Thu, 25 Jul 2024 20:19:09 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Thu, 25 Jul 2024 20:19:09 GMT
ENV LEIN_ROOT=1
# Thu, 25 Jul 2024 20:19:09 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.11.3"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Thu, 25 Jul 2024 20:19:09 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 25 Jul 2024 20:19:09 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 25 Jul 2024 20:19:09 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:24cfbc0d689f4d514c091713d28dff40b2e697cb854a24b2fae97f94b10bc383`  
		Last Modified: Fri, 28 Jun 2024 02:10:56 GMT  
		Size: 28.4 MB (28401129 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6672595a5d127b59ecf75423f0ef5367642a9d021fe56a7d618121f1c21d2fd7`  
		Last Modified: Tue, 02 Jul 2024 04:35:30 GMT  
		Size: 18.8 MB (18827827 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c225f5a6552449ce207f5bfbd85f6ed1a26a3b52f2a3e7270b29af2ee771cad`  
		Last Modified: Tue, 23 Jul 2024 04:15:08 GMT  
		Size: 156.8 MB (156756723 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81ec6fdf43db04c2e6133f92c02f91fe54d3123e5a1cabb3d0368f92a4d26831`  
		Last Modified: Tue, 23 Jul 2024 04:14:58 GMT  
		Size: 176.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af142f8f7ec876d457a54ad62e2b413df48ec349e9dfbbfddbc3c71251042def`  
		Last Modified: Thu, 25 Jul 2024 17:46:59 GMT  
		Size: 1.9 KB (1867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0be01ba13703721e8f0e806538fedb9d6afe02d5620dfc6fb46b813bc3707a7d`  
		Last Modified: Thu, 25 Jul 2024 21:21:19 GMT  
		Size: 35.7 MB (35725467 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5cdc9a82003ae291aa9ec2b340b90ee941e78dbfa39b33520f8d1939b41c0c1`  
		Last Modified: Thu, 25 Jul 2024 21:21:18 GMT  
		Size: 4.4 MB (4398019 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb31161860b3fb389b9cb51e7ef4e4cd3c55b4965dfe293ce061b77fdb2afea5`  
		Last Modified: Thu, 25 Jul 2024 21:21:17 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-lein-jammy` - unknown; unknown

```console
$ docker pull clojure@sha256:2defef3670d684e843f621825f0842fa6d00607c0b1d970e096c8330c61cc983
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5470644 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9afb1b9fff395e5b0584f786035051ed554e01c7e7aa960b46d81e2dbfd30661`

```dockerfile
```

-	Layers:
	-	`sha256:d02813f62c5a10c84712789ef697a492f45f520f245bf7ff50b2cca262dac354`  
		Last Modified: Thu, 25 Jul 2024 21:21:18 GMT  
		Size: 5.5 MB (5451982 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2e37f434cd52417d8ec82600eecde12fbddcd61a7fe2f9015ee58caf56eab32a`  
		Last Modified: Thu, 25 Jul 2024 21:21:17 GMT  
		Size: 18.7 KB (18662 bytes)  
		MIME: application/vnd.in-toto+json
