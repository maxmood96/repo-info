## `gradle:9-jdk26-alpine`

```console
$ docker pull gradle@sha256:d180ac66d39139f7cb1914bf79bdb2f0272a343ab345cf0bf4795a380dd61ca0
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `gradle:9-jdk26-alpine` - linux; amd64

```console
$ docker pull gradle@sha256:fe4aed053da7eba3e7d2a880b01d81216a37ee06ba9077d3a3e589407b9d86f2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **298.4 MB (298421327 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a26fc7a801dc9b001428cc27f6f62265bdf424443e45c5a8b42eb64b093480b5`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["gradle"]`

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
# Mon, 29 Jun 2026 17:13:50 GMT
CMD ["gradle"]
# Mon, 29 Jun 2026 17:13:50 GMT
ENV GRADLE_HOME=/opt/gradle
# Mon, 29 Jun 2026 17:13:50 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && addgroup --system --gid 1000 gradle     && adduser --system --ingroup gradle --uid 1000 --shell /bin/ash gradle     && mkdir /home/gradle/.gradle     && chown -R gradle:gradle /home/gradle     && chmod -R o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln -s /home/gradle/.gradle /root/.gradle # buildkit
# Mon, 29 Jun 2026 17:13:50 GMT
VOLUME [/home/gradle/.gradle]
# Mon, 29 Jun 2026 17:13:50 GMT
WORKDIR /home/gradle
# Mon, 29 Jun 2026 17:13:52 GMT
RUN set -o errexit -o nounset     && apk add --no-cache       make       curl       wget       tar             breezy       py3-tzlocal       git       git-lfs       mercurial       subversion         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Mon, 29 Jun 2026 17:13:52 GMT
ENV GRADLE_VERSION=9.6.1
# Mon, 29 Jun 2026 17:13:52 GMT
ARG GRADLE_DOWNLOAD_SHA256=9c0f7faeeb306cb14e4279a3e084ca6b596894089a0638e68a07c945a32c9e14
# Mon, 29 Jun 2026 17:13:54 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=9c0f7faeeb306cb14e4279a3e084ca6b596894089a0638e68a07c945a32c9e14
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum -c -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln -s "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Mon, 29 Jun 2026 17:13:54 GMT
USER gradle
# Mon, 29 Jun 2026 17:13:55 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=9c0f7faeeb306cb14e4279a3e084ca6b596894089a0638e68a07c945a32c9e14
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --stacktrace --debug --version # buildkit
# Mon, 29 Jun 2026 17:13:55 GMT
USER root
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
	-	`sha256:9618391b6aae155622f650c08aad6607cb7bb35df7b312cf23a415f68fdf9cfe`  
		Last Modified: Mon, 29 Jun 2026 17:14:11 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2b742049f532bb8a41d1db447fedb302a33dbc55e410e7d3d8a7929ec990ecc`  
		Last Modified: Mon, 29 Jun 2026 17:14:13 GMT  
		Size: 46.0 MB (45965243 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bce82cbcb19e2ca4a24803196565b14b029ef3bb9e96372b38b7a8557ea7925`  
		Last Modified: Mon, 29 Jun 2026 17:14:16 GMT  
		Size: 140.6 MB (140596162 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:936e2db053101275ec6cdee0a329cd3a97502745665e6637222a971b2076000a`  
		Last Modified: Mon, 29 Jun 2026 17:14:11 GMT  
		Size: 25.6 KB (25622 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:9-jdk26-alpine` - unknown; unknown

```console
$ docker pull gradle@sha256:97264b79d4f38b24df939db396613587cd7c4f315607ca6b453d6e194460d964
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4639513 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed91779e43247050e7515bf09c6c834f6ff7930c763a2b724e73a821d1853190`

```dockerfile
```

-	Layers:
	-	`sha256:d35a6800e8ba95e887ace4b0c91e16d8993d020256bbedc2b5eb18eb0dd1ab99`  
		Last Modified: Mon, 29 Jun 2026 17:14:11 GMT  
		Size: 4.6 MB (4616889 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f69f6bcfdd1aaeafd04eb797e0ab56bca665b22f8e678c67a4974ae3268ee1d5`  
		Last Modified: Mon, 29 Jun 2026 17:14:11 GMT  
		Size: 22.6 KB (22624 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:9-jdk26-alpine` - linux; arm64 variant v8

```console
$ docker pull gradle@sha256:d9d77439adbd3850d3aff7cee8876d5399e1222d317630849432ecca6e8d474c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **297.2 MB (297232393 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ed4b9f623f509209d4d338665ec9118ff22cc58444b2aa0fa33b3bd7d49876d`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["gradle"]`

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
# Mon, 29 Jun 2026 17:13:40 GMT
CMD ["gradle"]
# Mon, 29 Jun 2026 17:13:40 GMT
ENV GRADLE_HOME=/opt/gradle
# Mon, 29 Jun 2026 17:13:40 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && addgroup --system --gid 1000 gradle     && adduser --system --ingroup gradle --uid 1000 --shell /bin/ash gradle     && mkdir /home/gradle/.gradle     && chown -R gradle:gradle /home/gradle     && chmod -R o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln -s /home/gradle/.gradle /root/.gradle # buildkit
# Mon, 29 Jun 2026 17:13:40 GMT
VOLUME [/home/gradle/.gradle]
# Mon, 29 Jun 2026 17:13:40 GMT
WORKDIR /home/gradle
# Mon, 29 Jun 2026 17:13:43 GMT
RUN set -o errexit -o nounset     && apk add --no-cache       make       curl       wget       tar             breezy       py3-tzlocal       git       git-lfs       mercurial       subversion         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Mon, 29 Jun 2026 17:13:43 GMT
ENV GRADLE_VERSION=9.6.1
# Mon, 29 Jun 2026 17:13:43 GMT
ARG GRADLE_DOWNLOAD_SHA256=9c0f7faeeb306cb14e4279a3e084ca6b596894089a0638e68a07c945a32c9e14
# Mon, 29 Jun 2026 17:13:46 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=9c0f7faeeb306cb14e4279a3e084ca6b596894089a0638e68a07c945a32c9e14
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum -c -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln -s "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Mon, 29 Jun 2026 17:13:46 GMT
USER gradle
# Mon, 29 Jun 2026 17:13:46 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=9c0f7faeeb306cb14e4279a3e084ca6b596894089a0638e68a07c945a32c9e14
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --stacktrace --debug --version # buildkit
# Mon, 29 Jun 2026 17:13:46 GMT
USER root
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
	-	`sha256:a8d3e73f8900c55cfb3b2ef2cb96c5dd1625bb5843e7e391ac16016dcf7b4c63`  
		Last Modified: Mon, 29 Jun 2026 17:14:03 GMT  
		Size: 1.0 KB (1013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d67752042fd2e3aefb8b1f2eba7177705e69537ab898113136a8e946bd26ded8`  
		Last Modified: Mon, 29 Jun 2026 17:14:06 GMT  
		Size: 45.5 MB (45483290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76225afcc9757268bc324e2a40820fd71f924e8ca21130533c8380700c3ca99a`  
		Last Modified: Mon, 29 Jun 2026 17:14:08 GMT  
		Size: 140.6 MB (140596154 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc0e79ad90e6ad4086eb15e6b6610196b7d766ea40ca247ccafe407740cbfb57`  
		Last Modified: Mon, 29 Jun 2026 17:14:03 GMT  
		Size: 29.3 KB (29345 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:9-jdk26-alpine` - unknown; unknown

```console
$ docker pull gradle@sha256:23dbd5904b5e86ab88782771cef5f2017c7d882beb875b5e16ea442c57896ac8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.8 MB (4789134 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f0078e11fd9d4ec4f635a422e35cd983048e7a1a2320e2acbffc3ae175de799`

```dockerfile
```

-	Layers:
	-	`sha256:c253acc0b43470f0c51aa7e92c3babfc93996bae0ffefd187e505ebbaeb526b6`  
		Last Modified: Mon, 29 Jun 2026 17:14:03 GMT  
		Size: 4.8 MB (4766361 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:232ab19c465cdcca50b0e1ba002bb0a859e95b8d11eb311dde0e4b63b9e2e2ac`  
		Last Modified: Mon, 29 Jun 2026 17:14:03 GMT  
		Size: 22.8 KB (22773 bytes)  
		MIME: application/vnd.in-toto+json
