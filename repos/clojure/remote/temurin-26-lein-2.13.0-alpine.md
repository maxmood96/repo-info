## `clojure:temurin-26-lein-2.13.0-alpine`

```console
$ docker pull clojure@sha256:2b0086c54a7429ecd53679c013cda85c10955632028a1228bf1a3df0c94f2c2e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-26-lein-2.13.0-alpine` - linux; amd64

```console
$ docker pull clojure@sha256:50271a337bb44e854be79154e61033d30b941a7f1e13866d0ecaa56801b40fd0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **131.8 MB (131803691 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:98acc6715de163545d294d0b9f922870418439f5b381f57cfe0309e171e111e9`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 22 Jun 2026 19:20:09 GMT
ADD alpine-minirootfs-3.23.5-x86_64.tar.gz / # buildkit
# Mon, 22 Jun 2026 19:20:09 GMT
CMD ["/bin/sh"]
# Mon, 22 Jun 2026 19:57:49 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 22 Jun 2026 19:57:49 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 22 Jun 2026 19:57:49 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 22 Jun 2026 19:57:49 GMT
RUN set -eux;     apk add --no-cache         fontconfig ttf-dejavu         ca-certificates p11-kit-trust         musl-locales musl-locales-lang         binutils         tzdata         coreutils         openssl     ;     rm -rf /var/cache/apk/* # buildkit
# Mon, 22 Jun 2026 19:57:49 GMT
ENV JAVA_VERSION=jdk-26.0.1+8
# Mon, 22 Jun 2026 19:57:58 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        aarch64)          ESUM='7e32b89349385f10d7805197c7696b46556717d041e681017b12590bae6692ca';          BINARY_URL='https://github.com/adoptium/temurin26-binaries/releases/download/jdk-26.0.1%2B8/OpenJDK26U-jdk_aarch64_alpine-linux_hotspot_26.0.1_8.tar.gz';          ;;        x86_64)          ESUM='0c97fe7e503fb6daf36a5e86e8d083b97cc2354cda4d11288e6c3b8ec0818afc';          BINARY_URL='https://github.com/adoptium/temurin26-binaries/releases/download/jdk-26.0.1%2B8/OpenJDK26U-jdk_x64_alpine-linux_hotspot_26.0.1_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     apk add --no-cache --virtual .fetch-deps gnupg;     wget -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     apk del --no-network .fetch-deps; # buildkit
# Mon, 22 Jun 2026 19:58:00 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Mon, 22 Jun 2026 19:58:00 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Mon, 22 Jun 2026 19:58:00 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Mon, 22 Jun 2026 19:58:00 GMT
CMD ["jshell"]
# Mon, 22 Jun 2026 20:25:40 GMT
ENV LEIN_VERSION=2.13.0
# Mon, 22 Jun 2026 20:25:40 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Mon, 22 Jun 2026 20:25:40 GMT
WORKDIR /tmp
# Mon, 22 Jun 2026 20:26:11 GMT
RUN set -eux; apk add --no-cache ca-certificates bash maven git gnupg && export GNUPGHOME="$(mktemp -d)" && export LEIN_ROOT=1 && mkdir -p $LEIN_INSTALL /usr/share/java /root/.lein && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && git clone --depth 1 --branch $LEIN_VERSION https://codeberg.org/leiningen/leiningen.git && cd leiningen && git verify-tag $LEIN_VERSION && [ "$(git rev-parse HEAD)" = "d703e4802feb3e5c3fa9ae9f1874fb7a3a3e3030" ] && ( cd leiningen-core && mvn -B -q -DskipTests install && mvn -B -q dependency:build-classpath -Dmdep.outputFile=.lein-bootstrap ) && bin/lein uberjar && install -m 0644 target/leiningen-$LEIN_VERSION-standalone.jar /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && install -m 0755 bin/lein-pkg $LEIN_INSTALL/lein && gpgconf --kill all && cd /tmp && rm -rf /tmp/leiningen /root/.m2 "$GNUPGHOME" && apk del ca-certificates maven git gnupg # buildkit
# Mon, 22 Jun 2026 20:26:11 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Mon, 22 Jun 2026 20:26:11 GMT
ENV LEIN_ROOT=1
# Mon, 22 Jun 2026 20:26:12 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.5"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Mon, 22 Jun 2026 20:26:12 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Mon, 22 Jun 2026 20:26:12 GMT
ENTRYPOINT ["entrypoint"]
# Mon, 22 Jun 2026 20:26:12 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:e6f31ffc071e5560b82a8685fba8214954e5721e3e49269d00958316edbe89fe`  
		Last Modified: Mon, 22 Jun 2026 12:03:33 GMT  
		Size: 3.8 MB (3844421 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2f2fd18a0a9bc0fb03fb517a12431b1bf11c2dd8a300797a70c469eb0573499`  
		Last Modified: Mon, 22 Jun 2026 19:58:15 GMT  
		Size: 14.3 MB (14259370 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54b896cecc272ef7121da940e2be26998d8de663b31adc1e3e4bb1cbb887ae6c`  
		Last Modified: Mon, 22 Jun 2026 19:58:17 GMT  
		Size: 93.7 MB (93726872 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46ef27f6a9817fdee68c106972c44385780e41f17b2e0f931781e6e066d03423`  
		Last Modified: Mon, 22 Jun 2026 19:58:14 GMT  
		Size: 130.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f794e94355907e9d4c3b9ac7bf794fdcc22add314a4fcd8d3c9ee0e9afed5a2`  
		Last Modified: Mon, 22 Jun 2026 19:58:06 GMT  
		Size: 2.5 KB (2463 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2584f09f5ef34d8befabaedbbd315aee71efeb881da46942162aceff5ada7360`  
		Last Modified: Mon, 22 Jun 2026 20:26:21 GMT  
		Size: 15.5 MB (15454826 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c3e10969fc16662ab70f4759c7ca73b62b769fafef2fbf7ac06c31c56481cda`  
		Last Modified: Mon, 22 Jun 2026 20:26:20 GMT  
		Size: 4.5 MB (4515174 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e6874964268f195629841d8544f1b5c1487bf3048d8880fde68f4261bc3b0f7`  
		Last Modified: Mon, 22 Jun 2026 20:26:20 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-26-lein-2.13.0-alpine` - unknown; unknown

```console
$ docker pull clojure@sha256:7ee9e63e0ffd235989c13b7b26c66a9916aa557eec63552796d0249066dec5ca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.0 MB (1047501 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:417a6d53297ab088ebbf07252c713c9353342eef8848bb46373c5d33c9305f9d`

```dockerfile
```

-	Layers:
	-	`sha256:e6f53acbc1133e9df464586888e1dd65c812761475ac7f417772325c82aa2933`  
		Last Modified: Mon, 22 Jun 2026 20:26:20 GMT  
		Size: 1.0 MB (1030111 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e8192d068431e050905e70a468accd61de72d4ad9ceffc1283cdb70e775e2703`  
		Last Modified: Mon, 22 Jun 2026 20:26:20 GMT  
		Size: 17.4 KB (17390 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-26-lein-2.13.0-alpine` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:8f577f8cefed4984e32e58f42f74c4861fd97f009a090d3160fb954685ba6450
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **131.2 MB (131168118 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:602054a93e28b7a8376c1d1af970d2d1bcdf2c60a0504b588d402147c8d130c0`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 22 Jun 2026 19:19:57 GMT
ADD alpine-minirootfs-3.23.5-aarch64.tar.gz / # buildkit
# Mon, 22 Jun 2026 19:19:57 GMT
CMD ["/bin/sh"]
# Mon, 22 Jun 2026 19:58:28 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 22 Jun 2026 19:58:28 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 22 Jun 2026 19:58:28 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 22 Jun 2026 19:58:28 GMT
RUN set -eux;     apk add --no-cache         fontconfig ttf-dejavu         ca-certificates p11-kit-trust         musl-locales musl-locales-lang         binutils         tzdata         coreutils         openssl     ;     rm -rf /var/cache/apk/* # buildkit
# Mon, 22 Jun 2026 19:58:28 GMT
ENV JAVA_VERSION=jdk-26.0.1+8
# Mon, 22 Jun 2026 19:58:37 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        aarch64)          ESUM='7e32b89349385f10d7805197c7696b46556717d041e681017b12590bae6692ca';          BINARY_URL='https://github.com/adoptium/temurin26-binaries/releases/download/jdk-26.0.1%2B8/OpenJDK26U-jdk_aarch64_alpine-linux_hotspot_26.0.1_8.tar.gz';          ;;        x86_64)          ESUM='0c97fe7e503fb6daf36a5e86e8d083b97cc2354cda4d11288e6c3b8ec0818afc';          BINARY_URL='https://github.com/adoptium/temurin26-binaries/releases/download/jdk-26.0.1%2B8/OpenJDK26U-jdk_x64_alpine-linux_hotspot_26.0.1_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     apk add --no-cache --virtual .fetch-deps gnupg;     wget -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     apk del --no-network .fetch-deps; # buildkit
# Mon, 22 Jun 2026 19:58:39 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Mon, 22 Jun 2026 19:58:39 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Mon, 22 Jun 2026 19:58:39 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Mon, 22 Jun 2026 19:58:39 GMT
CMD ["jshell"]
# Mon, 22 Jun 2026 20:58:48 GMT
ENV LEIN_VERSION=2.13.0
# Mon, 22 Jun 2026 20:58:48 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Mon, 22 Jun 2026 20:58:48 GMT
WORKDIR /tmp
# Mon, 22 Jun 2026 20:59:23 GMT
RUN set -eux; apk add --no-cache ca-certificates bash maven git gnupg && export GNUPGHOME="$(mktemp -d)" && export LEIN_ROOT=1 && mkdir -p $LEIN_INSTALL /usr/share/java /root/.lein && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && git clone --depth 1 --branch $LEIN_VERSION https://codeberg.org/leiningen/leiningen.git && cd leiningen && git verify-tag $LEIN_VERSION && [ "$(git rev-parse HEAD)" = "d703e4802feb3e5c3fa9ae9f1874fb7a3a3e3030" ] && ( cd leiningen-core && mvn -B -q -DskipTests install && mvn -B -q dependency:build-classpath -Dmdep.outputFile=.lein-bootstrap ) && bin/lein uberjar && install -m 0644 target/leiningen-$LEIN_VERSION-standalone.jar /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && install -m 0755 bin/lein-pkg $LEIN_INSTALL/lein && gpgconf --kill all && cd /tmp && rm -rf /tmp/leiningen /root/.m2 "$GNUPGHOME" && apk del ca-certificates maven git gnupg # buildkit
# Mon, 22 Jun 2026 20:59:23 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Mon, 22 Jun 2026 20:59:23 GMT
ENV LEIN_ROOT=1
# Mon, 22 Jun 2026 20:59:25 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.5"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Mon, 22 Jun 2026 20:59:25 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Mon, 22 Jun 2026 20:59:25 GMT
ENTRYPOINT ["entrypoint"]
# Mon, 22 Jun 2026 20:59:25 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:14a4754c352fba4c6c0da8e4f01bb990463c19f7ff63e090073c385bd2bc5046`  
		Last Modified: Mon, 22 Jun 2026 12:03:31 GMT  
		Size: 4.2 MB (4181860 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:259201305cf66a45c6f9b11bf24d453317731d6a78705f78a399137c52f9e461`  
		Last Modified: Mon, 22 Jun 2026 19:58:54 GMT  
		Size: 14.3 MB (14320313 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cd1e1a965bbb185d2269d31ef27dc5dbe89fa439f174a8b7bf40b3fc7a4190d`  
		Last Modified: Mon, 22 Jun 2026 19:58:56 GMT  
		Size: 92.6 MB (92617795 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20ebddc94b4afa6b0f737e5864afd8689f7952438e252acbcc0805bd077e8b6a`  
		Last Modified: Mon, 22 Jun 2026 19:58:54 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:938f966bc6eeccc12781f72ab7be7722b25b9dd4da6076c94fd98a7d26e96618`  
		Last Modified: Mon, 22 Jun 2026 19:58:54 GMT  
		Size: 2.5 KB (2463 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bd9ebb049f8a844874cdfa339849f6c11e16fb6e04d3d6c29cb007c8e9ddc22`  
		Last Modified: Mon, 22 Jun 2026 20:59:34 GMT  
		Size: 15.5 MB (15529935 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:326cd9002068546c8f8a0d80411850b9d4e1cff1fc11d173487b1d4cf25e052d`  
		Last Modified: Mon, 22 Jun 2026 20:59:33 GMT  
		Size: 4.5 MB (4515192 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efb5b87be8930c69ce551152e066efc94848fda35af34384f7edd5fa906d0c24`  
		Last Modified: Mon, 22 Jun 2026 20:59:33 GMT  
		Size: 400.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-26-lein-2.13.0-alpine` - unknown; unknown

```console
$ docker pull clojure@sha256:038cb40cbc21508ca0f6f688c29415a0b86eb684736820e2531f96abcb7cf486
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.2 MB (1196933 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff64c6ad343eed517501c1e0f7be7d9e1d733a9fc8c0eedd4d37cb7306ec41b0`

```dockerfile
```

-	Layers:
	-	`sha256:5d9a752efa1911de6b0a4898227d4e1b2cf6422703fca1f87e142b6b9fa70d2c`  
		Last Modified: Mon, 22 Jun 2026 20:59:33 GMT  
		Size: 1.2 MB (1179448 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e4a58c56b1d9a38b5d3449fe5328b5170f5fa34c92b60c73b1f91566c3eda753`  
		Last Modified: Mon, 22 Jun 2026 20:59:33 GMT  
		Size: 17.5 KB (17485 bytes)  
		MIME: application/vnd.in-toto+json
