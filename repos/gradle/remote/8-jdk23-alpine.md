## `gradle:8-jdk23-alpine`

```console
$ docker pull gradle@sha256:df5e30ed8f0fea8b2c5bbfe97cc1d7b92da6b64a044384f0b1c16dbb9b20bcab
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `gradle:8-jdk23-alpine` - linux; amd64

```console
$ docker pull gradle@sha256:0e78a268f86cd6b9d288fae008443a01307cde0eae59631029cf4453cbad1d09
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **359.9 MB (359917047 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:36c1b9204a197727b9ad361863005ebbaeef3267733cf7fa3544b0b573a257d4`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["gradle"]`

```dockerfile
# Fri, 06 Sep 2024 12:05:36 GMT
ADD alpine-minirootfs-3.20.3-x86_64.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:05:36 GMT
CMD ["/bin/sh"]
# Wed, 23 Oct 2024 15:41:32 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 23 Oct 2024 15:41:32 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 23 Oct 2024 15:41:32 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 23 Oct 2024 15:41:32 GMT
RUN set -eux;     apk add --no-cache         fontconfig ttf-dejavu         gnupg         ca-certificates p11-kit-trust         musl-locales musl-locales-lang         binutils         tzdata         coreutils         openssl     ;     rm -rf /var/cache/apk/* # buildkit
# Wed, 23 Oct 2024 15:41:32 GMT
ENV JAVA_VERSION=jdk-23.0.1+11
# Wed, 23 Oct 2024 15:41:32 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        aarch64)          ESUM='ebdd6602d27bd7535bf06f21e8a0c3d563be7b790a90bef00cb6ac4123c66f86';          BINARY_URL='https://github.com/adoptium/temurin23-binaries/releases/download/jdk-23.0.1%2B11/OpenJDK23U-jdk_aarch64_alpine-linux_hotspot_23.0.1_11.tar.gz';          ;;        x86_64)          ESUM='4c37a9e885c4e099b049c3ba9baa073de1525e28cd5ffca016c5c5bd7ed385a6';          BINARY_URL='https://github.com/adoptium/temurin23-binaries/releases/download/jdk-23.0.1%2B11/OpenJDK23U-jdk_x64_alpine-linux_hotspot_23.0.1_11.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -r "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Wed, 23 Oct 2024 15:41:32 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 23 Oct 2024 15:41:32 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 23 Oct 2024 15:41:32 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 23 Oct 2024 15:41:32 GMT
CMD ["jshell"]
# Wed, 13 Nov 2024 00:13:30 GMT
CMD ["gradle"]
# Wed, 13 Nov 2024 00:13:30 GMT
ENV GRADLE_HOME=/opt/gradle
# Wed, 13 Nov 2024 00:13:30 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && addgroup --system --gid 1000 gradle     && adduser --system --ingroup gradle --uid 1000 --shell /bin/ash gradle     && mkdir /home/gradle/.gradle     && chown -R gradle:gradle /home/gradle     && chmod -R o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln -s /home/gradle/.gradle /root/.gradle # buildkit
# Wed, 13 Nov 2024 00:13:30 GMT
VOLUME [/home/gradle/.gradle]
# Wed, 13 Nov 2024 00:13:30 GMT
WORKDIR /home/gradle
# Wed, 13 Nov 2024 00:13:30 GMT
RUN set -o errexit -o nounset     && echo "Installing VCSes"     && apk add --no-cache       git       git-lfs       mercurial       subversion         && echo "Testing VCSes"     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Wed, 13 Nov 2024 00:13:30 GMT
ENV GRADLE_VERSION=8.11
# Wed, 13 Nov 2024 00:13:30 GMT
ARG GRADLE_DOWNLOAD_SHA256=57dafb5c2622c6cc08b993c85b7c06956a2f53536432a30ead46166dbca0f1e9
# Wed, 13 Nov 2024 00:13:30 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=57dafb5c2622c6cc08b993c85b7c06956a2f53536432a30ead46166dbca0f1e9
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum -c -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln -s "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Wed, 13 Nov 2024 00:13:30 GMT
USER gradle
# Wed, 13 Nov 2024 00:13:30 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=57dafb5c2622c6cc08b993c85b7c06956a2f53536432a30ead46166dbca0f1e9
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Wed, 13 Nov 2024 00:13:30 GMT
USER root
```

-	Layers:
	-	`sha256:da9db072f522755cbeb85be2b3f84059b70571b229512f1571d9217b77e1087f`  
		Last Modified: Fri, 06 Sep 2024 14:39:08 GMT  
		Size: 3.6 MB (3623904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80ac0afaffe8235a13dd8d90914a2d6cd114cf39e349a24c38c2bcdea79ab015`  
		Last Modified: Tue, 12 Nov 2024 02:39:09 GMT  
		Size: 23.0 MB (22953184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0deb3338abfe175e7b298fa61a7147c870fb4aed00f53f4d30d674547e1b45f`  
		Last Modified: Tue, 12 Nov 2024 02:39:12 GMT  
		Size: 165.5 MB (165513301 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3915703c046dd63269dbc212a69ec33a47d1030d48b31a874adf6bf73d47c449`  
		Last Modified: Tue, 12 Nov 2024 02:39:07 GMT  
		Size: 130.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c78fe47fe453af682fad0d120e9e4f2a5c05f85ebe5e3bdec8014fc7020c9c7d`  
		Last Modified: Tue, 12 Nov 2024 02:38:50 GMT  
		Size: 2.3 KB (2281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b476bf411dd8fede2c94afc61d75a674573c5ba390675bc53c78d61a751a8362`  
		Last Modified: Wed, 13 Nov 2024 02:07:22 GMT  
		Size: 1.0 KB (1020 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0d4ccd4b5592183d64cc889030d1537791a13230b8757faa2ce56196f085525`  
		Last Modified: Wed, 13 Nov 2024 02:07:23 GMT  
		Size: 30.9 MB (30898895 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a7feb4153cea5b7c8ba4ded39f1d2b40e328eb505bafcb33ed7364ae854b98d`  
		Last Modified: Wed, 13 Nov 2024 02:07:25 GMT  
		Size: 136.9 MB (136924012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53267b4a4d376b3188dcea14c96825d929a83b2765363ebe7aafe98b2c49c205`  
		Last Modified: Wed, 13 Nov 2024 02:07:22 GMT  
		Size: 288.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:8-jdk23-alpine` - unknown; unknown

```console
$ docker pull gradle@sha256:862ef73499a180133985b1f35d75842c7f0c850409992a3d96bfcee549cbbe40
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3341693 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c72429021bdb22c3862f7e1676925b90143ffb0006cacc974f2ca7597e2367f`

```dockerfile
```

-	Layers:
	-	`sha256:54c5073951154dd7defd4c1900eff5145fa5ccbf91a0dcf092cd8efe65b63e10`  
		Last Modified: Wed, 13 Nov 2024 02:07:22 GMT  
		Size: 3.3 MB (3320783 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4ef45bd785a4b459ef2a98f1e640bdc5af8ba5d18ba196d90c96bc5e235616f5`  
		Last Modified: Wed, 13 Nov 2024 02:07:22 GMT  
		Size: 20.9 KB (20910 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:8-jdk23-alpine` - linux; arm64 variant v8

```console
$ docker pull gradle@sha256:b2d57323148473b4c74b0a10abbc873571e1f2fda9115e8feba87505019aeadb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **359.1 MB (359138449 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f0a03f05ded983e32cdf68b612e0cc00fbe69e728e897cd0942ee508b2e90a9`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["gradle"]`

```dockerfile
# Fri, 06 Sep 2024 12:05:36 GMT
ADD alpine-minirootfs-3.20.3-aarch64.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:05:36 GMT
CMD ["/bin/sh"]
# Wed, 23 Oct 2024 15:41:32 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 23 Oct 2024 15:41:32 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 23 Oct 2024 15:41:32 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 23 Oct 2024 15:41:32 GMT
RUN set -eux;     apk add --no-cache         fontconfig ttf-dejavu         gnupg         ca-certificates p11-kit-trust         musl-locales musl-locales-lang         binutils         tzdata         coreutils         openssl     ;     rm -rf /var/cache/apk/* # buildkit
# Wed, 23 Oct 2024 15:41:32 GMT
ENV JAVA_VERSION=jdk-23.0.1+11
# Wed, 23 Oct 2024 15:41:32 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        aarch64)          ESUM='ebdd6602d27bd7535bf06f21e8a0c3d563be7b790a90bef00cb6ac4123c66f86';          BINARY_URL='https://github.com/adoptium/temurin23-binaries/releases/download/jdk-23.0.1%2B11/OpenJDK23U-jdk_aarch64_alpine-linux_hotspot_23.0.1_11.tar.gz';          ;;        x86_64)          ESUM='4c37a9e885c4e099b049c3ba9baa073de1525e28cd5ffca016c5c5bd7ed385a6';          BINARY_URL='https://github.com/adoptium/temurin23-binaries/releases/download/jdk-23.0.1%2B11/OpenJDK23U-jdk_x64_alpine-linux_hotspot_23.0.1_11.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -r "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Wed, 23 Oct 2024 15:41:32 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 23 Oct 2024 15:41:32 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 23 Oct 2024 15:41:32 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 23 Oct 2024 15:41:32 GMT
CMD ["jshell"]
# Wed, 13 Nov 2024 00:13:30 GMT
CMD ["gradle"]
# Wed, 13 Nov 2024 00:13:30 GMT
ENV GRADLE_HOME=/opt/gradle
# Wed, 13 Nov 2024 00:13:30 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && addgroup --system --gid 1000 gradle     && adduser --system --ingroup gradle --uid 1000 --shell /bin/ash gradle     && mkdir /home/gradle/.gradle     && chown -R gradle:gradle /home/gradle     && chmod -R o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln -s /home/gradle/.gradle /root/.gradle # buildkit
# Wed, 13 Nov 2024 00:13:30 GMT
VOLUME [/home/gradle/.gradle]
# Wed, 13 Nov 2024 00:13:30 GMT
WORKDIR /home/gradle
# Wed, 13 Nov 2024 00:13:30 GMT
RUN set -o errexit -o nounset     && echo "Installing VCSes"     && apk add --no-cache       git       git-lfs       mercurial       subversion         && echo "Testing VCSes"     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Wed, 13 Nov 2024 00:13:30 GMT
ENV GRADLE_VERSION=8.11
# Wed, 13 Nov 2024 00:13:30 GMT
ARG GRADLE_DOWNLOAD_SHA256=57dafb5c2622c6cc08b993c85b7c06956a2f53536432a30ead46166dbca0f1e9
# Wed, 13 Nov 2024 00:13:30 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=57dafb5c2622c6cc08b993c85b7c06956a2f53536432a30ead46166dbca0f1e9
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum -c -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln -s "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Wed, 13 Nov 2024 00:13:30 GMT
USER gradle
# Wed, 13 Nov 2024 00:13:30 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=57dafb5c2622c6cc08b993c85b7c06956a2f53536432a30ead46166dbca0f1e9
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Wed, 13 Nov 2024 00:13:30 GMT
USER root
```

-	Layers:
	-	`sha256:9986a736f7d3d24bb01b0a560fa0f19c4b57e56c646e1f998941529d28710e6b`  
		Last Modified: Mon, 09 Sep 2024 07:03:59 GMT  
		Size: 4.1 MB (4087726 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4e35b18e3113b7f2ff24b09398759411d2064bbc52968a3357a6760d0c2b1f9`  
		Last Modified: Tue, 12 Nov 2024 11:26:38 GMT  
		Size: 23.7 MB (23731447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2db31191851a20ed74edf1c325a20c8656b97d58146f289463d6412a41fb76c0`  
		Last Modified: Tue, 12 Nov 2024 11:28:08 GMT  
		Size: 163.3 MB (163315918 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f885213b736ea29aae6521dcc23013e1b68d4c899016f70d1d611f4e61ee86e`  
		Last Modified: Tue, 12 Nov 2024 11:28:04 GMT  
		Size: 131.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bdd7bbd77347b5c434ff3cadc2b92fe2bb3f2c75a52f55a079d3aadd380558c`  
		Last Modified: Tue, 12 Nov 2024 11:28:04 GMT  
		Size: 2.3 KB (2281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4eb01b18eae2daaee1762678c3b6105ed138d819ee8fac308471a445c7f86a19`  
		Last Modified: Wed, 13 Nov 2024 08:34:08 GMT  
		Size: 1.0 KB (1023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46bb79793cf80492d9d2362ff15960fa658f0ba4e672954b0ed991f8c7abfbea`  
		Last Modified: Wed, 13 Nov 2024 08:34:10 GMT  
		Size: 31.1 MB (31075591 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2be34d0f4c4006ef373fe5f4c7e6a9f183616d62d24c425579fb1baa8a53752a`  
		Last Modified: Wed, 13 Nov 2024 08:34:13 GMT  
		Size: 136.9 MB (136924009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f54d943aa1618444153a4903b867c123fdc7f36495c7eb28510da88522e49050`  
		Last Modified: Wed, 13 Nov 2024 08:34:08 GMT  
		Size: 291.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:8-jdk23-alpine` - unknown; unknown

```console
$ docker pull gradle@sha256:d707ed35c370c49a7ba46c1ed05570910534366f66fb6cf296ed12d032789beb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.4 MB (3446008 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2bc46d16c8512f9c882f0a8d0274a06d5098a504498346f9852d8cf4b26d9b7d`

```dockerfile
```

-	Layers:
	-	`sha256:7b4c90a9b4e0f6463257999800d1bd7709d8888139752b3d6d657d6088731eeb`  
		Last Modified: Wed, 13 Nov 2024 08:34:09 GMT  
		Size: 3.4 MB (3424949 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f9a5f1ea93cdc76dd976a4afb09d33acd0606588f6c14598250bba1d3ca853f2`  
		Last Modified: Wed, 13 Nov 2024 08:34:08 GMT  
		Size: 21.1 KB (21059 bytes)  
		MIME: application/vnd.in-toto+json
