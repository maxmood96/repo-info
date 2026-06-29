## `gradle:jdk21-alpine`

```console
$ docker pull gradle@sha256:615d75ef01f9c1aacab46fd022828a6d35738308fe89b64be3ec7e113af03c00
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `gradle:jdk21-alpine` - linux; amd64

```console
$ docker pull gradle@sha256:3c8e87703ae2a98ce5a451c418d265f0665e9efc14fb302467852a8a69f1c112
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **368.1 MB (368092530 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:116926370d925394df87b583dcfe4f6513713d63c142f7666a027a1379ef9a38`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["gradle"]`

```dockerfile
# Mon, 22 Jun 2026 19:20:09 GMT
ADD alpine-minirootfs-3.23.5-x86_64.tar.gz / # buildkit
# Mon, 22 Jun 2026 19:20:09 GMT
CMD ["/bin/sh"]
# Mon, 22 Jun 2026 19:57:09 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 22 Jun 2026 19:57:09 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 22 Jun 2026 19:57:09 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 22 Jun 2026 19:57:09 GMT
RUN set -eux;     apk add --no-cache         fontconfig ttf-dejavu         gnupg         ca-certificates p11-kit-trust         musl-locales musl-locales-lang         binutils         tzdata         coreutils         openssl     ;     rm -rf /var/cache/apk/* # buildkit
# Mon, 22 Jun 2026 19:57:09 GMT
ENV JAVA_VERSION=jdk-21.0.11+10
# Mon, 22 Jun 2026 19:57:17 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        aarch64)          ESUM='c8d63598d1dc0a656033515ed258bd6db37506a05407d9f65cd23b95c21027b5';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.11%2B10/OpenJDK21U-jdk_aarch64_alpine-linux_hotspot_21.0.11_10.tar.gz';          ;;        x86_64)          ESUM='38bfdcef1e4b45de2ec222047ac79c76bea75d4d7406a310e26cfa236763f05f';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.11%2B10/OpenJDK21U-jdk_x64_alpine-linux_hotspot_21.0.11_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Mon, 22 Jun 2026 19:57:18 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Mon, 22 Jun 2026 19:57:18 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Mon, 22 Jun 2026 19:57:18 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Mon, 22 Jun 2026 19:57:18 GMT
CMD ["jshell"]
# Mon, 29 Jun 2026 17:11:35 GMT
CMD ["gradle"]
# Mon, 29 Jun 2026 17:11:35 GMT
ENV GRADLE_HOME=/opt/gradle
# Mon, 29 Jun 2026 17:11:35 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && addgroup --system --gid 1000 gradle     && adduser --system --ingroup gradle --uid 1000 --shell /bin/ash gradle     && mkdir /home/gradle/.gradle     && chown -R gradle:gradle /home/gradle     && chmod -R o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln -s /home/gradle/.gradle /root/.gradle # buildkit
# Mon, 29 Jun 2026 17:11:35 GMT
VOLUME [/home/gradle/.gradle]
# Mon, 29 Jun 2026 17:11:35 GMT
WORKDIR /home/gradle
# Mon, 29 Jun 2026 17:11:37 GMT
RUN set -o errexit -o nounset     && apk add --no-cache       make       curl       wget       tar             breezy       py3-tzlocal       git       git-lfs       mercurial       subversion         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Mon, 29 Jun 2026 17:11:37 GMT
ENV GRADLE_VERSION=9.6.1
# Mon, 29 Jun 2026 17:11:37 GMT
ARG GRADLE_DOWNLOAD_SHA256=9c0f7faeeb306cb14e4279a3e084ca6b596894089a0638e68a07c945a32c9e14
# Mon, 29 Jun 2026 17:11:39 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=9c0f7faeeb306cb14e4279a3e084ca6b596894089a0638e68a07c945a32c9e14
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum -c -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln -s "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Mon, 29 Jun 2026 17:11:39 GMT
USER gradle
# Mon, 29 Jun 2026 17:11:39 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=9c0f7faeeb306cb14e4279a3e084ca6b596894089a0638e68a07c945a32c9e14
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --stacktrace --debug --version # buildkit
# Mon, 29 Jun 2026 17:11:39 GMT
USER root
```

-	Layers:
	-	`sha256:e6f31ffc071e5560b82a8685fba8214954e5721e3e49269d00958316edbe89fe`  
		Last Modified: Mon, 22 Jun 2026 12:03:33 GMT  
		Size: 3.8 MB (3844421 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d42b27ff362c29d4c86173d5eb45dc9fc28c27d52c5791cb63a9113e6f0e3646`  
		Last Modified: Mon, 22 Jun 2026 19:57:35 GMT  
		Size: 21.3 MB (21290130 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c90809b4c96d37014d44d53b2f534fcdc3a9b2baa628af103045b46795a7189`  
		Last Modified: Mon, 22 Jun 2026 19:57:38 GMT  
		Size: 158.4 MB (158396795 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d7ee5d98789e02e3500e8e207c5963d76ea5e48dbe5f519229aeb3847e2bc62`  
		Last Modified: Mon, 22 Jun 2026 19:57:33 GMT  
		Size: 130.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d68dfaba6ad42ab866380109a6c2636053416cb8f6e06672fa092a97451fd747`  
		Last Modified: Mon, 22 Jun 2026 19:57:34 GMT  
		Size: 2.3 KB (2281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06e095bd31e123681eb42420250436ce601111c6a7ba270a2cbeab46e0d339bb`  
		Last Modified: Mon, 29 Jun 2026 17:11:54 GMT  
		Size: 1.0 KB (1013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76851685c6c6e7d0892c3126215c648df9480a4e03c62fc862b40c8594ca74cb`  
		Last Modified: Mon, 29 Jun 2026 17:11:56 GMT  
		Size: 43.9 MB (43935965 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eccb7a1fcc25938bb176bc5d79db5a18551be5a3534d233f359a50f99eda30d2`  
		Last Modified: Mon, 29 Jun 2026 17:11:58 GMT  
		Size: 140.6 MB (140596147 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6f3bf52837d2ad130bb31a74727d698aeed17ffe82c5f719cffad399c82cf5f`  
		Last Modified: Mon, 29 Jun 2026 17:11:54 GMT  
		Size: 25.6 KB (25616 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:jdk21-alpine` - unknown; unknown

```console
$ docker pull gradle@sha256:4de6513d802b6ebf5719a155e36d952f23e15d79684bcb7f191a25825b118cb2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4733173 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:75bb809eb6981b3a6d7a604dcaf295e336c665fe616ec559a8cecc63cf87476d`

```dockerfile
```

-	Layers:
	-	`sha256:154ee4d93d99695ac178fcdd6d5fe7a1b2d7a417737b22ac68a29d3e0eaf3762`  
		Last Modified: Mon, 29 Jun 2026 17:11:55 GMT  
		Size: 4.7 MB (4710535 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:91150c097e7913a9f51cc5653a0bdf9dda8f932c73de6170e3c025a6bd939690`  
		Last Modified: Mon, 29 Jun 2026 17:11:54 GMT  
		Size: 22.6 KB (22638 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:jdk21-alpine` - linux; arm64 variant v8

```console
$ docker pull gradle@sha256:cdc92ed2c613afd6371b721bff09b7599319b2af563885e6a89d237e685f0be3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **365.9 MB (365940752 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:715c65f1702793eefe781e7af7ce695b172995725bf2d5d1a8cab5772cbf2b91`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["gradle"]`

```dockerfile
# Mon, 22 Jun 2026 19:19:57 GMT
ADD alpine-minirootfs-3.23.5-aarch64.tar.gz / # buildkit
# Mon, 22 Jun 2026 19:19:57 GMT
CMD ["/bin/sh"]
# Mon, 22 Jun 2026 19:57:56 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 22 Jun 2026 19:57:56 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 22 Jun 2026 19:57:56 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 22 Jun 2026 19:57:56 GMT
RUN set -eux;     apk add --no-cache         fontconfig ttf-dejavu         gnupg         ca-certificates p11-kit-trust         musl-locales musl-locales-lang         binutils         tzdata         coreutils         openssl     ;     rm -rf /var/cache/apk/* # buildkit
# Mon, 22 Jun 2026 19:57:56 GMT
ENV JAVA_VERSION=jdk-21.0.11+10
# Mon, 22 Jun 2026 19:58:06 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        aarch64)          ESUM='c8d63598d1dc0a656033515ed258bd6db37506a05407d9f65cd23b95c21027b5';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.11%2B10/OpenJDK21U-jdk_aarch64_alpine-linux_hotspot_21.0.11_10.tar.gz';          ;;        x86_64)          ESUM='38bfdcef1e4b45de2ec222047ac79c76bea75d4d7406a310e26cfa236763f05f';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.11%2B10/OpenJDK21U-jdk_x64_alpine-linux_hotspot_21.0.11_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Mon, 22 Jun 2026 19:58:07 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Mon, 22 Jun 2026 19:58:07 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Mon, 22 Jun 2026 19:58:07 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Mon, 22 Jun 2026 19:58:07 GMT
CMD ["jshell"]
# Mon, 29 Jun 2026 17:11:43 GMT
CMD ["gradle"]
# Mon, 29 Jun 2026 17:11:43 GMT
ENV GRADLE_HOME=/opt/gradle
# Mon, 29 Jun 2026 17:11:43 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && addgroup --system --gid 1000 gradle     && adduser --system --ingroup gradle --uid 1000 --shell /bin/ash gradle     && mkdir /home/gradle/.gradle     && chown -R gradle:gradle /home/gradle     && chmod -R o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln -s /home/gradle/.gradle /root/.gradle # buildkit
# Mon, 29 Jun 2026 17:11:43 GMT
VOLUME [/home/gradle/.gradle]
# Mon, 29 Jun 2026 17:11:43 GMT
WORKDIR /home/gradle
# Mon, 29 Jun 2026 17:11:45 GMT
RUN set -o errexit -o nounset     && apk add --no-cache       make       curl       wget       tar             breezy       py3-tzlocal       git       git-lfs       mercurial       subversion         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Mon, 29 Jun 2026 17:11:45 GMT
ENV GRADLE_VERSION=9.6.1
# Mon, 29 Jun 2026 17:11:45 GMT
ARG GRADLE_DOWNLOAD_SHA256=9c0f7faeeb306cb14e4279a3e084ca6b596894089a0638e68a07c945a32c9e14
# Mon, 29 Jun 2026 17:11:48 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=9c0f7faeeb306cb14e4279a3e084ca6b596894089a0638e68a07c945a32c9e14
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum -c -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln -s "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Mon, 29 Jun 2026 17:11:48 GMT
USER gradle
# Mon, 29 Jun 2026 17:11:49 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=9c0f7faeeb306cb14e4279a3e084ca6b596894089a0638e68a07c945a32c9e14
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --stacktrace --debug --version # buildkit
# Mon, 29 Jun 2026 17:11:49 GMT
USER root
```

-	Layers:
	-	`sha256:14a4754c352fba4c6c0da8e4f01bb990463c19f7ff63e090073c385bd2bc5046`  
		Last Modified: Mon, 22 Jun 2026 12:03:31 GMT  
		Size: 4.2 MB (4181860 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4528e8515ecbe5a4cead182002e4915088694f327a2a6d59eb4d8879cc01934`  
		Last Modified: Mon, 22 Jun 2026 19:58:24 GMT  
		Size: 21.3 MB (21281739 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d9ad1632bf4f15fb4547045f89810b89d4e2c12f4cc1e1cb1b38c68666c29d7`  
		Last Modified: Mon, 22 Jun 2026 19:58:27 GMT  
		Size: 156.4 MB (156402333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c9d07f7518fbbb05f6c65a2c0b79b89a2e5fde15459a3d4e2f4f4ceaf1a7f70`  
		Last Modified: Mon, 22 Jun 2026 19:58:23 GMT  
		Size: 130.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eab2a9682f8c999c8b4b42cc35b437b44dfbdf44d7726ea13daab581dd97384b`  
		Last Modified: Mon, 22 Jun 2026 19:58:23 GMT  
		Size: 2.3 KB (2281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63780bbf858ef5ee05c650e9ad517d0e1e77c33aea13597db9914ddbc3e53c90`  
		Last Modified: Mon, 29 Jun 2026 17:12:05 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ba9b68ef15b14d867cd383311deeba8e8e67f4221c6b0d0943153b46356b126`  
		Last Modified: Mon, 29 Jun 2026 17:12:08 GMT  
		Size: 43.4 MB (43445738 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8690cd38e0b5f36d2f0225c219e93d6c34fadcb00f282631f6de8e9300e39807`  
		Last Modified: Mon, 29 Jun 2026 17:12:10 GMT  
		Size: 140.6 MB (140596279 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8778373d122d2f104f7ddd79a9c44b899214ddd11f34b4db2afe91a02aaae54b`  
		Last Modified: Mon, 29 Jun 2026 17:12:06 GMT  
		Size: 29.3 KB (29348 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:jdk21-alpine` - unknown; unknown

```console
$ docker pull gradle@sha256:e0548aa1193531a5fbfe429deba474379c74fa57d1624696d3f8762fb6ef1502
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4882793 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:74e7e37fb90ecbe6e3d5b05af9f684769618dcc6ef34052de6a1ae76523cd388`

```dockerfile
```

-	Layers:
	-	`sha256:cfa413b27c0255ccfcdf546afba44958523a21d40ff1cd67f4f71bdaf95f4ad3`  
		Last Modified: Mon, 29 Jun 2026 17:12:06 GMT  
		Size: 4.9 MB (4860010 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:381e356d23b1ddef54c08c191813c10ee34eda8518e5040b10967b0818734d8b`  
		Last Modified: Mon, 29 Jun 2026 17:12:06 GMT  
		Size: 22.8 KB (22783 bytes)  
		MIME: application/vnd.in-toto+json
