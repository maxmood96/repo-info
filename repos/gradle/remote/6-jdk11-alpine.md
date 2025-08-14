## `gradle:6-jdk11-alpine`

```console
$ docker pull gradle@sha256:bd075eaa586a704e8b9f4ffb4eb3c952292a1c5559f11215168fd8219f6c1a01
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `gradle:6-jdk11-alpine` - linux; amd64

```console
$ docker pull gradle@sha256:e43df687a4a85d71ac0f6685047fa30f945b2b18c5fe5c9d87f3169781e57641
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **314.6 MB (314590431 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b3a5ac6f0bd4fb816781dbeb4c6b49b5a1d538375d69ecace8401516e1b2b445`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["gradle"]`

```dockerfile
# Mon, 02 Jun 2025 18:02:05 GMT
ADD alpine-minirootfs-3.22.1-x86_64.tar.gz / # buildkit
# Mon, 02 Jun 2025 18:02:05 GMT
CMD ["/bin/sh"]
# Mon, 02 Jun 2025 18:02:05 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 02 Jun 2025 18:02:05 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 02 Jun 2025 18:02:05 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 02 Jun 2025 18:02:05 GMT
RUN set -eux;     apk add --no-cache         fontconfig ttf-dejavu         gnupg         ca-certificates p11-kit-trust         musl-locales musl-locales-lang         tzdata         coreutils         openssl     ;     rm -rf /var/cache/apk/* # buildkit
# Mon, 02 Jun 2025 18:02:05 GMT
ENV JAVA_VERSION=jdk-11.0.28+6
# Mon, 02 Jun 2025 18:02:05 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        x86_64)          ESUM='7e9e5241d1378d75ae70e9b216d0d51d3aa2e61e187e92e09d117cb613e16ee4';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.28%2B6/OpenJDK11U-jdk_x64_alpine-linux_hotspot_11.0.28_6.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Mon, 02 Jun 2025 18:02:05 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Mon, 02 Jun 2025 18:02:05 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Mon, 02 Jun 2025 18:02:05 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Mon, 02 Jun 2025 18:02:05 GMT
CMD ["jshell"]
# Mon, 02 Jun 2025 18:02:05 GMT
CMD ["gradle"]
# Mon, 02 Jun 2025 18:02:05 GMT
ENV GRADLE_HOME=/opt/gradle
# Mon, 02 Jun 2025 18:02:05 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && addgroup --system --gid 1000 gradle     && adduser --system --ingroup gradle --uid 1000 --shell /bin/ash gradle     && mkdir /home/gradle/.gradle     && chown -R gradle:gradle /home/gradle     && chmod -R o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln -s /home/gradle/.gradle /root/.gradle # buildkit
# Mon, 02 Jun 2025 18:02:05 GMT
VOLUME [/home/gradle/.gradle]
# Mon, 02 Jun 2025 18:02:05 GMT
WORKDIR /home/gradle
# Mon, 02 Jun 2025 18:02:05 GMT
RUN set -o errexit -o nounset     && apk add --no-cache       curl       make             breezy       py3-tzlocal       git       git-lfs       mercurial       subversion         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Mon, 02 Jun 2025 18:02:05 GMT
ENV GRADLE_VERSION=6.9.4
# Mon, 02 Jun 2025 18:02:05 GMT
ARG GRADLE_DOWNLOAD_SHA256=3e240228538de9f18772a574e99a0ba959e83d6ef351014381acd9631781389a
# Mon, 02 Jun 2025 18:02:05 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=3e240228538de9f18772a574e99a0ba959e83d6ef351014381acd9631781389a
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum -c -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln -s "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Mon, 02 Jun 2025 18:02:05 GMT
USER gradle
# Mon, 02 Jun 2025 18:02:05 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=3e240228538de9f18772a574e99a0ba959e83d6ef351014381acd9631781389a
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Mon, 02 Jun 2025 18:02:05 GMT
USER root
```

-	Layers:
	-	`sha256:9824c27679d3b27c5e1cb00a73adb6f4f8d556994111c12db3c5d61a0c843df8`  
		Last Modified: Tue, 15 Jul 2025 19:00:01 GMT  
		Size: 3.8 MB (3799689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32368a88ab88c011f9799e221ffa3a76a0557d8f869cb207cb6f61e0a1955762`  
		Last Modified: Mon, 04 Aug 2025 19:11:15 GMT  
		Size: 16.3 MB (16280183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d648ad0c3205513ffbb1e09ea89959604157e09c4cc8d981f5fa1b1e777c4f0`  
		Last Modified: Mon, 04 Aug 2025 20:12:02 GMT  
		Size: 140.8 MB (140841600 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:593271197e067f9172951dae5461f06c964edf69c2598534299fed88688fb565`  
		Last Modified: Mon, 04 Aug 2025 19:11:16 GMT  
		Size: 131.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b79e640d46de60752e85b9c04c3a723384b01154acc6635a1cda3176da6ada69`  
		Last Modified: Mon, 04 Aug 2025 19:11:16 GMT  
		Size: 2.3 KB (2280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16d303203de2491584d5d857dd971183799963aeed944d9d531eb25bb7a40ca5`  
		Last Modified: Mon, 04 Aug 2025 20:12:53 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d488f25d5619662fc21d4adc7569ac2b364a6566b649e3ad0956016072010bc`  
		Last Modified: Mon, 04 Aug 2025 20:13:00 GMT  
		Size: 45.5 MB (45537582 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a661c064bb3f8b35e124dada2ea0c578e51ed3b17bcf38d8412b85e6b5c3d907`  
		Last Modified: Mon, 04 Aug 2025 20:13:07 GMT  
		Size: 107.7 MB (107696647 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0998510a431a48f8e96eb776461b956d64b7ffd60232753ed6f2a46311955e5f`  
		Last Modified: Mon, 04 Aug 2025 20:12:54 GMT  
		Size: 431.3 KB (431275 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:6-jdk11-alpine` - unknown; unknown

```console
$ docker pull gradle@sha256:a948d0e73a5ffae62e3a39cc41c007b088838551f86bd5e8fe086cde8226741a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4526296 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bffe42fd1c698ca34fac102ce69f1c3d11be2c39aa824215068b3e71b6f2398a`

```dockerfile
```

-	Layers:
	-	`sha256:0e8beb619b1d90fd8ec1523a2623598d3e6c141e12107eaf1242808b81b883dd`  
		Last Modified: Mon, 04 Aug 2025 23:17:37 GMT  
		Size: 4.5 MB (4502234 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:52d08c0f9e2ff3c9601d179a6a7d20f8bace63a6b2c32775302ef21a3c4c3938`  
		Last Modified: Mon, 04 Aug 2025 23:17:38 GMT  
		Size: 24.1 KB (24062 bytes)  
		MIME: application/vnd.in-toto+json
