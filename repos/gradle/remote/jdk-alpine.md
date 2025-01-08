## `gradle:jdk-alpine`

```console
$ docker pull gradle@sha256:70c7191c382fc7f956cacd326ded88bf69a01f707aa2556adb931c090377e601
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `gradle:jdk-alpine` - linux; amd64

```console
$ docker pull gradle@sha256:dcbb5e9e770c868444998bde4c0e728d763956cc3ff6efae02a744f6cd412cd0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **349.6 MB (349587321 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b4b4bcbaf5d891c6248588bca20b4a8cc5ae1770a9756d13fddc05d66f46934c`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["gradle"]`

```dockerfile
# Wed, 23 Oct 2024 15:41:32 GMT
ADD alpine-minirootfs-3.20.4-x86_64.tar.gz / # buildkit
# Wed, 23 Oct 2024 15:41:32 GMT
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
ENV JAVA_VERSION=jdk-21.0.5+11
# Wed, 23 Oct 2024 15:41:32 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        aarch64)          ESUM='f22e32b869dd0e5e3f248646f62bffaa307b360299488ac8764e622923d7e747';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.5%2B11/OpenJDK21U-jdk_aarch64_alpine-linux_hotspot_21.0.5_11.tar.gz';          ;;        x86_64)          ESUM='8da7da49101d45f646272616f20e8b10d57472bbf5961d64ffb07d7ba93c6909';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.5%2B11/OpenJDK21U-jdk_x64_alpine-linux_hotspot_21.0.5_11.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -r "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Wed, 23 Oct 2024 15:41:32 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 23 Oct 2024 15:41:32 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 23 Oct 2024 15:41:32 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 23 Oct 2024 15:41:32 GMT
CMD ["jshell"]
# Fri, 20 Dec 2024 17:54:11 GMT
CMD ["gradle"]
# Fri, 20 Dec 2024 17:54:11 GMT
ENV GRADLE_HOME=/opt/gradle
# Fri, 20 Dec 2024 17:54:11 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && addgroup --system --gid 1000 gradle     && adduser --system --ingroup gradle --uid 1000 --shell /bin/ash gradle     && mkdir /home/gradle/.gradle     && chown -R gradle:gradle /home/gradle     && chmod -R o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln -s /home/gradle/.gradle /root/.gradle # buildkit
# Fri, 20 Dec 2024 17:54:11 GMT
VOLUME [/home/gradle/.gradle]
# Fri, 20 Dec 2024 17:54:11 GMT
WORKDIR /home/gradle
# Fri, 20 Dec 2024 17:54:11 GMT
RUN set -o errexit -o nounset     && echo "Installing VCSes"     && apk add --no-cache       git       git-lfs       mercurial       subversion         && echo "Testing VCSes"     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Fri, 20 Dec 2024 17:54:11 GMT
ENV GRADLE_VERSION=8.12
# Fri, 20 Dec 2024 17:54:11 GMT
ARG GRADLE_DOWNLOAD_SHA256=7a00d51fb93147819aab76024feece20b6b84e420694101f276be952e08bef03
# Fri, 20 Dec 2024 17:54:11 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=7a00d51fb93147819aab76024feece20b6b84e420694101f276be952e08bef03
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum -c -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln -s "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Fri, 20 Dec 2024 17:54:11 GMT
USER gradle
# Fri, 20 Dec 2024 17:54:11 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=7a00d51fb93147819aab76024feece20b6b84e420694101f276be952e08bef03
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Fri, 20 Dec 2024 17:54:11 GMT
USER root
```

-	Layers:
	-	`sha256:63b69af3dc5582ce6b63be03623e334ccd4e5cb4bde42702bbfc7a986a1bf432`  
		Last Modified: Tue, 07 Jan 2025 02:28:35 GMT  
		Size: 3.6 MB (3613999 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74124278afe2b18a31c86c5481b70f13610d72f9251456efb60077c008ba80d9`  
		Last Modified: Tue, 07 Jan 2025 03:31:25 GMT  
		Size: 20.6 MB (20646874 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed8fcf39531b5efa8fb9a8f692b5b7b7feca498796d140b94c6255523f4c7f6d`  
		Last Modified: Tue, 07 Jan 2025 03:31:27 GMT  
		Size: 157.8 MB (157779528 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e62fe376e35d90e3e99f049badca94e8fe7301d699d6a2539330a8994d9f8799`  
		Last Modified: Tue, 07 Jan 2025 03:31:25 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af5d46d44a8796aecf2575f05400a60dd8d65d4f9f801590d09cd3b4f278318d`  
		Last Modified: Tue, 07 Jan 2025 03:31:25 GMT  
		Size: 2.3 KB (2278 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d508022931c7d4dc4888e13805f215a5e2ee81038a2b921cb6c1f662ba61851`  
		Last Modified: Tue, 07 Jan 2025 04:20:10 GMT  
		Size: 1.0 KB (1021 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d14577e257e2e4e4dbd0249d2e687f4c311471d3a70869d87cd31164759ce28`  
		Last Modified: Tue, 07 Jan 2025 04:20:11 GMT  
		Size: 30.9 MB (30924431 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ddd64162fece26f279001ef072fdff53681a47dc89fc769c1c86ef219a27c0d0`  
		Last Modified: Tue, 07 Jan 2025 04:20:12 GMT  
		Size: 136.6 MB (136564130 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1bc415465ddda2c434fd6032eed2373091990298c1d5e8fbeb5f6964c66575ca`  
		Last Modified: Tue, 07 Jan 2025 04:20:10 GMT  
		Size: 54.9 KB (54899 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:jdk-alpine` - unknown; unknown

```console
$ docker pull gradle@sha256:b8b0bbd3d9b59adb9f88831adc5c1e9f91f5f8286fb4758daa128eafe91dd9d0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3328543 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c2e4c98c2463d35607d164004c7e4250864590aeccd93e0c8395eeedd77177b5`

```dockerfile
```

-	Layers:
	-	`sha256:3b378d3ea8b6e8b46fe10ba94fd2ed861b8be4adac86a391ef35f595eade6480`  
		Last Modified: Tue, 07 Jan 2025 04:20:10 GMT  
		Size: 3.3 MB (3305795 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dfb03382221b9e3ec3dc24889c9659fd9fc552222d745ddc0654a525d2fe4598`  
		Last Modified: Tue, 07 Jan 2025 04:20:10 GMT  
		Size: 22.7 KB (22748 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:jdk-alpine` - linux; arm64 variant v8

```console
$ docker pull gradle@sha256:a64eed5ec33e5ad3890bbd69edb1faaabf3594ae3be324e7b895f20dea7c1f22
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **348.4 MB (348393951 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c2d5e88e60fd385f5d574d36217f8e793098b2b225b8c99297898ab5aea069c`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["gradle"]`

```dockerfile
# Wed, 23 Oct 2024 15:41:32 GMT
ADD alpine-minirootfs-3.20.4-aarch64.tar.gz / # buildkit
# Wed, 23 Oct 2024 15:41:32 GMT
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
ENV JAVA_VERSION=jdk-21.0.5+11
# Wed, 23 Oct 2024 15:41:32 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        aarch64)          ESUM='f22e32b869dd0e5e3f248646f62bffaa307b360299488ac8764e622923d7e747';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.5%2B11/OpenJDK21U-jdk_aarch64_alpine-linux_hotspot_21.0.5_11.tar.gz';          ;;        x86_64)          ESUM='8da7da49101d45f646272616f20e8b10d57472bbf5961d64ffb07d7ba93c6909';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.5%2B11/OpenJDK21U-jdk_x64_alpine-linux_hotspot_21.0.5_11.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -r "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Wed, 23 Oct 2024 15:41:32 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 23 Oct 2024 15:41:32 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 23 Oct 2024 15:41:32 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 23 Oct 2024 15:41:32 GMT
CMD ["jshell"]
# Fri, 20 Dec 2024 17:54:11 GMT
CMD ["gradle"]
# Fri, 20 Dec 2024 17:54:11 GMT
ENV GRADLE_HOME=/opt/gradle
# Fri, 20 Dec 2024 17:54:11 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && addgroup --system --gid 1000 gradle     && adduser --system --ingroup gradle --uid 1000 --shell /bin/ash gradle     && mkdir /home/gradle/.gradle     && chown -R gradle:gradle /home/gradle     && chmod -R o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln -s /home/gradle/.gradle /root/.gradle # buildkit
# Fri, 20 Dec 2024 17:54:11 GMT
VOLUME [/home/gradle/.gradle]
# Fri, 20 Dec 2024 17:54:11 GMT
WORKDIR /home/gradle
# Fri, 20 Dec 2024 17:54:11 GMT
RUN set -o errexit -o nounset     && echo "Installing VCSes"     && apk add --no-cache       git       git-lfs       mercurial       subversion         && echo "Testing VCSes"     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Fri, 20 Dec 2024 17:54:11 GMT
ENV GRADLE_VERSION=8.12
# Fri, 20 Dec 2024 17:54:11 GMT
ARG GRADLE_DOWNLOAD_SHA256=7a00d51fb93147819aab76024feece20b6b84e420694101f276be952e08bef03
# Fri, 20 Dec 2024 17:54:11 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=7a00d51fb93147819aab76024feece20b6b84e420694101f276be952e08bef03
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum -c -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln -s "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Fri, 20 Dec 2024 17:54:11 GMT
USER gradle
# Fri, 20 Dec 2024 17:54:11 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=7a00d51fb93147819aab76024feece20b6b84e420694101f276be952e08bef03
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Fri, 20 Dec 2024 17:54:11 GMT
USER root
```

-	Layers:
	-	`sha256:ef22e11fe7735044a1b56fc644666588aa863fb6abe827f676cb9d11ba34d993`  
		Last Modified: Tue, 07 Jan 2025 03:03:03 GMT  
		Size: 4.1 MB (4086686 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0debfbcf140de1b1e0c5b7204c63e292d79de69a68e3267957c67e04f0ba24af`  
		Last Modified: Tue, 07 Jan 2025 07:27:36 GMT  
		Size: 21.0 MB (21033362 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc7e26f108db4058af6f9154e47e87b732fbd6fb04792a0871d1074952992b75`  
		Last Modified: Tue, 07 Jan 2025 07:27:36 GMT  
		Size: 155.7 MB (155740151 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b3ed595529c90be877f0b53e3b866c077cd55bd6b85c36388f452338ba4c676`  
		Last Modified: Tue, 07 Jan 2025 07:27:32 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a3a0beda2910401756d0ac146e871cdae993a2a999f118127df9ca88c508fc0`  
		Last Modified: Tue, 07 Jan 2025 07:27:32 GMT  
		Size: 2.3 KB (2281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4516d6cb3248a4479e8b8be6807543e961615927205960aadd214ec92a18f645`  
		Last Modified: Tue, 07 Jan 2025 16:28:54 GMT  
		Size: 1.0 KB (1021 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf1b9689b4143a69e1b7af48a7d32f62257dde451b9e2432c687e7cc24969a0c`  
		Last Modified: Tue, 07 Jan 2025 16:28:55 GMT  
		Size: 30.9 MB (30906501 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ea0de4946813795522e6caf74c15fc7f0eefb7517f58aab0407bbf256cd637a`  
		Last Modified: Tue, 07 Jan 2025 16:28:58 GMT  
		Size: 136.6 MB (136564249 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eeae98fd3f886cb4c03875c37aaf9d3b2db094c9a1c741d74ebea5f4e9bb5a9b`  
		Last Modified: Tue, 07 Jan 2025 16:28:54 GMT  
		Size: 59.5 KB (59540 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:jdk-alpine` - unknown; unknown

```console
$ docker pull gradle@sha256:d02dc08dd9ea5e3db662a339f421b74021a253a1f64030234585d946970c0ca0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.4 MB (3433463 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6d09b5cd5549569ca8b23bfc8b57e1d938a7d409355e7d2d4b07199cb6cd7250`

```dockerfile
```

-	Layers:
	-	`sha256:ea1d2401e8299616bd29fecb1f4ce23f6b226bad57ff9c0265739420c9aedbd8`  
		Last Modified: Tue, 07 Jan 2025 16:28:54 GMT  
		Size: 3.4 MB (3410494 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ecf737c04e9c6473e046767a13979a1d9ce560f2e30c66649a6ecbf9daa2d3dd`  
		Size: 23.0 KB (22969 bytes)  
		MIME: application/vnd.in-toto+json
