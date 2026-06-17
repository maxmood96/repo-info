## `clojure:temurin-26-lein-alpine`

```console
$ docker pull clojure@sha256:e02fc1d35260d6286914bc9ec2a128bb6420edad3c1e5b7c9a0e1de5c96ad86a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-26-lein-alpine` - linux; amd64

```console
$ docker pull clojure@sha256:74c7b2c23f43a209faaec1fb8b56e622ec85e514e441434a41bd5cb6f34274de
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **131.9 MB (131892310 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:52181cfee6b0444d279593c08759847bc25c974f9859b9d7fa987c6c523ef45d`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:40 GMT
ADD alpine-minirootfs-3.23.4-x86_64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:40 GMT
CMD ["/bin/sh"]
# Fri, 15 May 2026 20:28:55 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 15 May 2026 20:28:55 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 15 May 2026 20:28:55 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 15 May 2026 20:28:55 GMT
RUN set -eux;     apk add --no-cache         fontconfig ttf-dejavu         ca-certificates p11-kit-trust         musl-locales musl-locales-lang         binutils         tzdata         coreutils         openssl     ;     rm -rf /var/cache/apk/* # buildkit
# Fri, 15 May 2026 20:28:55 GMT
ENV JAVA_VERSION=jdk-26.0.1+8
# Fri, 15 May 2026 20:29:03 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        aarch64)          ESUM='7e32b89349385f10d7805197c7696b46556717d041e681017b12590bae6692ca';          BINARY_URL='https://github.com/adoptium/temurin26-binaries/releases/download/jdk-26.0.1%2B8/OpenJDK26U-jdk_aarch64_alpine-linux_hotspot_26.0.1_8.tar.gz';          ;;        x86_64)          ESUM='0c97fe7e503fb6daf36a5e86e8d083b97cc2354cda4d11288e6c3b8ec0818afc';          BINARY_URL='https://github.com/adoptium/temurin26-binaries/releases/download/jdk-26.0.1%2B8/OpenJDK26U-jdk_x64_alpine-linux_hotspot_26.0.1_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     apk add --no-cache --virtual .fetch-deps gnupg;     wget -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     apk del --no-network .fetch-deps; # buildkit
# Fri, 15 May 2026 20:29:04 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Fri, 15 May 2026 20:29:04 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Fri, 15 May 2026 20:29:04 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Fri, 15 May 2026 20:29:04 GMT
CMD ["jshell"]
# Tue, 16 Jun 2026 23:37:51 GMT
ENV LEIN_VERSION=2.13.0
# Tue, 16 Jun 2026 23:37:51 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 16 Jun 2026 23:37:51 GMT
WORKDIR /tmp
# Tue, 16 Jun 2026 23:38:22 GMT
RUN set -eux; apk add --no-cache ca-certificates bash maven git gnupg && export GNUPGHOME="$(mktemp -d)" && export LEIN_ROOT=1 && mkdir -p $LEIN_INSTALL /usr/share/java /root/.lein && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && git clone --depth 1 --branch $LEIN_VERSION https://codeberg.org/leiningen/leiningen.git && cd leiningen && git verify-tag $LEIN_VERSION && [ "$(git rev-parse HEAD)" = "d703e4802feb3e5c3fa9ae9f1874fb7a3a3e3030" ] && ( cd leiningen-core && mvn -B -q -DskipTests install && mvn -B -q dependency:build-classpath -Dmdep.outputFile=.lein-bootstrap ) && bin/lein uberjar && install -m 0644 target/leiningen-$LEIN_VERSION-standalone.jar /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && install -m 0755 bin/lein-pkg $LEIN_INSTALL/lein && gpgconf --kill all && cd /tmp && rm -rf /tmp/leiningen /root/.m2 "$GNUPGHOME" && apk del ca-certificates maven git gnupg # buildkit
# Tue, 16 Jun 2026 23:38:22 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 16 Jun 2026 23:38:22 GMT
ENV LEIN_ROOT=1
# Tue, 16 Jun 2026 23:38:24 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.5"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 16 Jun 2026 23:38:24 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 16 Jun 2026 23:38:24 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 16 Jun 2026 23:38:24 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:6a0ac1617861a677b045b7ff88545213ec31c0ff08763195a70a4a5adda577bb`  
		Last Modified: Wed, 15 Apr 2026 20:01:46 GMT  
		Size: 3.9 MB (3864189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e081e96822532a01c7bb1e027265fed4b4c27a2e1d696c326f173f3cc1223765`  
		Last Modified: Fri, 15 May 2026 20:29:20 GMT  
		Size: 14.3 MB (14307105 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbaa5d5be003b1eed063c02fb86d96eed583ae248613b526315e1da79db26c33`  
		Last Modified: Fri, 15 May 2026 20:29:22 GMT  
		Size: 93.7 MB (93726947 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e549ff0e96b732aa8f90eae5e53676271da5ac10a0fd38c6b26da9ff83ce4aae`  
		Last Modified: Fri, 15 May 2026 20:29:19 GMT  
		Size: 130.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:521a9ec0292e87558350138ddd287318bfa3975e6531bc92f1c86438baf45fe9`  
		Last Modified: Fri, 15 May 2026 20:29:20 GMT  
		Size: 2.5 KB (2461 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd3dc5be857fe1c8290d685fafd093b4daf847aa10a3130ae9d6b9253c18d583`  
		Last Modified: Tue, 16 Jun 2026 23:38:32 GMT  
		Size: 15.5 MB (15475827 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2efe03408a0104c99cdd5c5e739cbb6b8a39267e356b27c8e34b74cfa909ca7d`  
		Last Modified: Tue, 16 Jun 2026 23:38:32 GMT  
		Size: 4.5 MB (4515213 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d7620a58862b473d5c95164f84697c23e78e776a276ce9cc71c57f8bcc60088`  
		Last Modified: Tue, 16 Jun 2026 23:38:32 GMT  
		Size: 406.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-26-lein-alpine` - unknown; unknown

```console
$ docker pull clojure@sha256:37c9e7616b15985cbb9a4bfed936f6367b95113e5a8cbf9efdd8dacc3cec3299
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.0 MB (1047500 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d128d2c14d0745c367d06b788605c484c2a2a1702b5655c0c69f04ebdb8e4c0`

```dockerfile
```

-	Layers:
	-	`sha256:e23c9a4143f7dee5e2d8c591a6d33a7b1e4e2d30edb7669d00dd01243819c3ff`  
		Last Modified: Tue, 16 Jun 2026 23:38:32 GMT  
		Size: 1.0 MB (1030111 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8b82c87f11d2b3a480424a30a8c78fcc2159b6cea0a54c18a2259a2df8b4e176`  
		Last Modified: Tue, 16 Jun 2026 23:38:32 GMT  
		Size: 17.4 KB (17389 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-26-lein-alpine` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:ee4b5080d1e336d9542db109f443b51b1b7d2844da2a9a9c19bed3e2741706d6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **131.3 MB (131256395 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4af0253e8d4d7d56ad76aeac29a15218732dbe0f707190fa7dccf29dc82fe07a`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:25 GMT
ADD alpine-minirootfs-3.23.4-aarch64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:25 GMT
CMD ["/bin/sh"]
# Fri, 15 May 2026 20:28:32 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 15 May 2026 20:28:32 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 15 May 2026 20:28:32 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 15 May 2026 20:28:32 GMT
RUN set -eux;     apk add --no-cache         fontconfig ttf-dejavu         ca-certificates p11-kit-trust         musl-locales musl-locales-lang         binutils         tzdata         coreutils         openssl     ;     rm -rf /var/cache/apk/* # buildkit
# Fri, 15 May 2026 20:28:32 GMT
ENV JAVA_VERSION=jdk-26.0.1+8
# Fri, 15 May 2026 20:28:42 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        aarch64)          ESUM='7e32b89349385f10d7805197c7696b46556717d041e681017b12590bae6692ca';          BINARY_URL='https://github.com/adoptium/temurin26-binaries/releases/download/jdk-26.0.1%2B8/OpenJDK26U-jdk_aarch64_alpine-linux_hotspot_26.0.1_8.tar.gz';          ;;        x86_64)          ESUM='0c97fe7e503fb6daf36a5e86e8d083b97cc2354cda4d11288e6c3b8ec0818afc';          BINARY_URL='https://github.com/adoptium/temurin26-binaries/releases/download/jdk-26.0.1%2B8/OpenJDK26U-jdk_x64_alpine-linux_hotspot_26.0.1_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     apk add --no-cache --virtual .fetch-deps gnupg;     wget -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     apk del --no-network .fetch-deps; # buildkit
# Fri, 15 May 2026 20:28:43 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Fri, 15 May 2026 20:28:43 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Fri, 15 May 2026 20:28:43 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Fri, 15 May 2026 20:28:43 GMT
CMD ["jshell"]
# Tue, 16 Jun 2026 23:37:38 GMT
ENV LEIN_VERSION=2.13.0
# Tue, 16 Jun 2026 23:37:38 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 16 Jun 2026 23:37:38 GMT
WORKDIR /tmp
# Tue, 16 Jun 2026 23:38:15 GMT
RUN set -eux; apk add --no-cache ca-certificates bash maven git gnupg && export GNUPGHOME="$(mktemp -d)" && export LEIN_ROOT=1 && mkdir -p $LEIN_INSTALL /usr/share/java /root/.lein && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && git clone --depth 1 --branch $LEIN_VERSION https://codeberg.org/leiningen/leiningen.git && cd leiningen && git verify-tag $LEIN_VERSION && [ "$(git rev-parse HEAD)" = "d703e4802feb3e5c3fa9ae9f1874fb7a3a3e3030" ] && ( cd leiningen-core && mvn -B -q -DskipTests install && mvn -B -q dependency:build-classpath -Dmdep.outputFile=.lein-bootstrap ) && bin/lein uberjar && install -m 0644 target/leiningen-$LEIN_VERSION-standalone.jar /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && install -m 0755 bin/lein-pkg $LEIN_INSTALL/lein && gpgconf --kill all && cd /tmp && rm -rf /tmp/leiningen /root/.m2 "$GNUPGHOME" && apk del ca-certificates maven git gnupg # buildkit
# Tue, 16 Jun 2026 23:38:15 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 16 Jun 2026 23:38:15 GMT
ENV LEIN_ROOT=1
# Tue, 16 Jun 2026 23:38:17 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.5"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 16 Jun 2026 23:38:17 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 16 Jun 2026 23:38:17 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 16 Jun 2026 23:38:17 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:d17f077ada118cc762df373ff803592abf2dfa3ddafaa7381e364dd27a88fca7`  
		Last Modified: Wed, 15 Apr 2026 20:01:32 GMT  
		Size: 4.2 MB (4199870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:663c281b02178500cc2405957896cb4b2c901f353ce59d8c702000b44a4eb4cb`  
		Last Modified: Fri, 15 May 2026 20:28:59 GMT  
		Size: 14.4 MB (14365440 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8478f678d308c7c3dd2a812916604bc76952d2cbdd6cbfed048df7d43bd35b55`  
		Last Modified: Fri, 15 May 2026 20:29:01 GMT  
		Size: 92.6 MB (92619253 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d36508231094e13df0969686478e5f11986327f94f6c60eac3a91ccd402da86b`  
		Last Modified: Fri, 15 May 2026 20:28:58 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6dd0378873387f971dd8030f59afc279b6de616979cc085f74c1a3b2f5bde1dc`  
		Last Modified: Fri, 15 May 2026 20:28:59 GMT  
		Size: 2.5 KB (2462 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cee4102324f206dd11e708db59c22ea1665b405f0cc14bdbcd27040235b89821`  
		Last Modified: Tue, 16 Jun 2026 23:38:26 GMT  
		Size: 15.6 MB (15553619 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c64b3307163ffd1a84c618c604c6c84102a9747821a244c15795a9791453668b`  
		Last Modified: Tue, 16 Jun 2026 23:38:26 GMT  
		Size: 4.5 MB (4515185 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8653ae685ee3548ebc1fe613b3e055b7485aaed5607d20566d82b586e42d86c7`  
		Last Modified: Tue, 16 Jun 2026 23:38:26 GMT  
		Size: 406.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-26-lein-alpine` - unknown; unknown

```console
$ docker pull clojure@sha256:dff7518d8d5d4eff1b0932ac09424b7f0e40c15030856210164f69606af0b177
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.2 MB (1196933 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e5ddd2b10e6f92cad73246d1f27eb9362e1c93ee6e0c878a1b30ef8030f45092`

```dockerfile
```

-	Layers:
	-	`sha256:2d76b111d854b45ec0b8f47ec467494aded94fc741c0a1e1e539393e40f34e61`  
		Last Modified: Tue, 16 Jun 2026 23:38:25 GMT  
		Size: 1.2 MB (1179448 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:76f67a002ecd0af4bc57be82e79f075bdf07eea10a1f791224e980443fd9de3d`  
		Last Modified: Tue, 16 Jun 2026 23:38:25 GMT  
		Size: 17.5 KB (17485 bytes)  
		MIME: application/vnd.in-toto+json
