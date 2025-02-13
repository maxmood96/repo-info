## `gradle:8-jdk17-alpine`

```console
$ docker pull gradle@sha256:cde9e892ca1f4a98f200b27c6a6dd05a38ca62fc494b9c52977b9404c7485c9d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `gradle:8-jdk17-alpine` - linux; amd64

```console
$ docker pull gradle@sha256:4bc2c348fd67e3de3eca29159752847297ec7b020c592d9c2a77ac8f1c294b23
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **337.5 MB (337482760 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:381ad2e1caa6fa2d854b88443ed3b07187016e404701560a8b9edf0ce1d3c7b0`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["gradle"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-x86_64.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
CMD ["/bin/sh"]
# Mon, 27 Jan 2025 19:22:41 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 27 Jan 2025 19:22:41 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 27 Jan 2025 19:22:41 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 27 Jan 2025 19:22:41 GMT
RUN set -eux;     apk add --no-cache         fontconfig ttf-dejavu         gnupg         ca-certificates p11-kit-trust         musl-locales musl-locales-lang         binutils         tzdata         coreutils         openssl     ;     rm -rf /var/cache/apk/* # buildkit
# Mon, 27 Jan 2025 19:22:41 GMT
ENV JAVA_VERSION=jdk-17.0.14+7
# Mon, 27 Jan 2025 19:22:41 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        x86_64)          ESUM='259c85e16f7bbfdfb3e0a2ec1c5d6e2063300d413422286583265a9d8a882358';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jdk_x64_alpine-linux_hotspot_17.0.14_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Mon, 27 Jan 2025 19:22:41 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Mon, 27 Jan 2025 19:22:41 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Mon, 27 Jan 2025 19:22:41 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Mon, 27 Jan 2025 19:22:41 GMT
CMD ["jshell"]
# Mon, 27 Jan 2025 19:22:41 GMT
CMD ["gradle"]
# Mon, 27 Jan 2025 19:22:41 GMT
ENV GRADLE_HOME=/opt/gradle
# Mon, 27 Jan 2025 19:22:41 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && addgroup --system --gid 1000 gradle     && adduser --system --ingroup gradle --uid 1000 --shell /bin/ash gradle     && mkdir /home/gradle/.gradle     && chown -R gradle:gradle /home/gradle     && chmod -R o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln -s /home/gradle/.gradle /root/.gradle # buildkit
# Mon, 27 Jan 2025 19:22:41 GMT
VOLUME [/home/gradle/.gradle]
# Mon, 27 Jan 2025 19:22:41 GMT
WORKDIR /home/gradle
# Mon, 27 Jan 2025 19:22:41 GMT
RUN set -o errexit -o nounset     && echo "Installing VCSes"     && apk add --no-cache       git       git-lfs       mercurial       subversion         && echo "Testing VCSes"     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Mon, 27 Jan 2025 19:22:41 GMT
ENV GRADLE_VERSION=8.12.1
# Mon, 27 Jan 2025 19:22:41 GMT
ARG GRADLE_DOWNLOAD_SHA256=8d97a97984f6cbd2b85fe4c60a743440a347544bf18818048e611f5288d46c94
# Mon, 27 Jan 2025 19:22:41 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=8d97a97984f6cbd2b85fe4c60a743440a347544bf18818048e611f5288d46c94
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum -c -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln -s "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Mon, 27 Jan 2025 19:22:41 GMT
USER gradle
# Mon, 27 Jan 2025 19:22:41 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=8d97a97984f6cbd2b85fe4c60a743440a347544bf18818048e611f5288d46c94
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Mon, 27 Jan 2025 19:22:41 GMT
USER root
```

-	Layers:
	-	`sha256:1f3e46996e2966e4faa5846e56e76e3748b7315e2ded61476c24403d592134f0`  
		Last Modified: Tue, 14 Jan 2025 20:33:02 GMT  
		Size: 3.6 MB (3641715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e964c090714275a4065e7acea241466fc487f2081bfb24e52722b02aa023934d`  
		Last Modified: Mon, 03 Feb 2025 20:16:58 GMT  
		Size: 20.9 MB (20908693 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ecda534f804788bc889d59c4e16afbcff57b89cab14639f41351998e0f6c354`  
		Last Modified: Mon, 03 Feb 2025 20:42:11 GMT  
		Size: 143.7 MB (143716399 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58c1b586d223d730dc8abb27b6539523713b21fc6623d20b76cbcb67e56f94ce`  
		Last Modified: Mon, 03 Feb 2025 20:32:08 GMT  
		Size: 130.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c43895d73efd1a8a528e3d0fea9b8b264f32ef501fe42aedf37f113017882492`  
		Last Modified: Mon, 03 Feb 2025 20:14:43 GMT  
		Size: 2.3 KB (2280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7496c630cccd82a355110077e8d1ab085c022f248e52b2b187911e3ab86fb2ae`  
		Last Modified: Mon, 03 Feb 2025 20:41:06 GMT  
		Size: 1.0 KB (1022 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5a73c414907fafa76974cd5857f94f6a39f394cb66d0165706739626a0f669f`  
		Last Modified: Mon, 03 Feb 2025 20:40:22 GMT  
		Size: 32.6 MB (32595498 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f692b77992e1c79501ce3f4fde63a4c288bd354d10f5cb4542a0edeb07acabf`  
		Last Modified: Tue, 04 Feb 2025 03:57:29 GMT  
		Size: 136.6 MB (136562088 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30f5e44804da4dc978440ed170280f7819d6cd15e7f59efba76e662f327642f7`  
		Last Modified: Mon, 03 Feb 2025 20:22:44 GMT  
		Size: 54.9 KB (54903 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:8-jdk17-alpine` - unknown; unknown

```console
$ docker pull gradle@sha256:dd30959b8a28fbc9b55577202dced624692d9a5c38b1f0dcbaad910d21b2a4e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.4 MB (3368350 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3cde23cae6567617058c7304878a33efa2f431d0d5207aa23590108e70f8d0e0`

```dockerfile
```

-	Layers:
	-	`sha256:9eade9cc1006d8c448ac807288d867fcc95c5cf7fc37a98c3816ab886fb9d982`  
		Last Modified: Sun, 09 Feb 2025 20:08:35 GMT  
		Size: 3.3 MB (3346798 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0ac0b77b95678981314ec9fd1fe915ce24d37c9bd05b0b30ddd134b866a14b33`  
		Last Modified: Fri, 31 Jan 2025 02:11:19 GMT  
		Size: 21.6 KB (21552 bytes)  
		MIME: application/vnd.in-toto+json
