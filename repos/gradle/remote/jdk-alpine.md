## `gradle:jdk-alpine`

```console
$ docker pull gradle@sha256:6ea131cf55a5369644edd44c0227e5d12d2575809dfe159fb4529ae1acd68de6
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `gradle:jdk-alpine` - linux; amd64

```console
$ docker pull gradle@sha256:2cf6c0aa4b6f64841dba8a8dcea34ea450c28056f47abd1fd8eaa51926b95390
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **296.0 MB (295955922 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af3a5191112f023c7abfef2041934a97d862fbc907b3d0f1694e81887210b71c`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["gradle"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:40 GMT
ADD alpine-minirootfs-3.23.4-x86_64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:40 GMT
CMD ["/bin/sh"]
# Wed, 15 Apr 2026 20:34:12 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 15 Apr 2026 20:34:12 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 15 Apr 2026 20:34:12 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 15 Apr 2026 20:34:12 GMT
RUN set -eux;     apk add --no-cache         fontconfig ttf-dejavu         ca-certificates p11-kit-trust         musl-locales musl-locales-lang         binutils         tzdata         coreutils         openssl     ;     rm -rf /var/cache/apk/* # buildkit
# Wed, 15 Apr 2026 20:34:12 GMT
ENV JAVA_VERSION=jdk-25.0.2+10
# Wed, 15 Apr 2026 20:34:21 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        aarch64)          ESUM='e8d928fb018eabb31a148ebadaa5a5ec69273e6562afede21c426960a6a67143';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.2%2B10/OpenJDK25U-jdk_aarch64_alpine-linux_hotspot_25.0.2_10.tar.gz';          ;;        x86_64)          ESUM='961f13ba0ee1e18c41c50ab642361e4283dee5e7947a48ed6a72c8a661d0cca0';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.2%2B10/OpenJDK25U-jdk_x64_alpine-linux_hotspot_25.0.2_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     apk add --no-cache --virtual .fetch-deps gnupg;     wget -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     apk del --no-network .fetch-deps; # buildkit
# Wed, 15 Apr 2026 20:34:23 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 15 Apr 2026 20:34:23 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 15 Apr 2026 20:34:23 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 15 Apr 2026 20:34:23 GMT
CMD ["jshell"]
# Tue, 28 Apr 2026 23:26:10 GMT
CMD ["gradle"]
# Tue, 28 Apr 2026 23:26:10 GMT
ENV GRADLE_HOME=/opt/gradle
# Tue, 28 Apr 2026 23:26:10 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && addgroup --system --gid 1000 gradle     && adduser --system --ingroup gradle --uid 1000 --shell /bin/ash gradle     && mkdir /home/gradle/.gradle     && chown -R gradle:gradle /home/gradle     && chmod -R o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln -s /home/gradle/.gradle /root/.gradle # buildkit
# Tue, 28 Apr 2026 23:26:10 GMT
VOLUME [/home/gradle/.gradle]
# Tue, 28 Apr 2026 23:26:10 GMT
WORKDIR /home/gradle
# Tue, 28 Apr 2026 23:26:13 GMT
RUN set -o errexit -o nounset     && apk add --no-cache       make       curl       wget       tar             breezy       py3-tzlocal       git       git-lfs       mercurial       subversion         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Tue, 28 Apr 2026 23:26:13 GMT
ENV GRADLE_VERSION=9.5.0
# Tue, 28 Apr 2026 23:26:13 GMT
ARG GRADLE_DOWNLOAD_SHA256=553c78f50dafcd54d65b9a444649057857469edf836431389695608536d6b746
# Tue, 28 Apr 2026 23:26:16 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=553c78f50dafcd54d65b9a444649057857469edf836431389695608536d6b746
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum -c -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln -s "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Tue, 28 Apr 2026 23:26:16 GMT
USER gradle
# Tue, 28 Apr 2026 23:26:17 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=553c78f50dafcd54d65b9a444649057857469edf836431389695608536d6b746
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --stacktrace --debug --version # buildkit
# Tue, 28 Apr 2026 23:26:17 GMT
USER root
```

-	Layers:
	-	`sha256:6a0ac1617861a677b045b7ff88545213ec31c0ff08763195a70a4a5adda577bb`  
		Last Modified: Wed, 15 Apr 2026 20:01:46 GMT  
		Size: 3.9 MB (3864189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32d78fbd718571b55d30809c1f3843638bd7b326cdd00fa9b1ad70fa32d1275e`  
		Last Modified: Wed, 15 Apr 2026 20:34:38 GMT  
		Size: 14.3 MB (14307228 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a0758b0503e9474a80d86a6848a74591d1f0224e311fa3e17a5bfa334cd0fd3`  
		Last Modified: Wed, 15 Apr 2026 20:34:45 GMT  
		Size: 91.5 MB (91491756 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43844d5cbff66283e09e3dc341de140a185899429dda46c135c2ddbcf13680a7`  
		Last Modified: Wed, 15 Apr 2026 20:34:38 GMT  
		Size: 130.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a8f14395c3629db1f2892a1628820feeeff222bb4aad5de5321d266613dab26`  
		Last Modified: Wed, 15 Apr 2026 20:34:38 GMT  
		Size: 2.3 KB (2280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55488a0cf0e3fae9daaed6cf02e37ed64475298b2aeda440064e08851f16a10c`  
		Last Modified: Tue, 28 Apr 2026 23:26:33 GMT  
		Size: 1.0 KB (1009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f2d0d782a7a40766f074f1bbead7b25efe0402ffc5e0dd94c70dda346fcab6e`  
		Last Modified: Tue, 28 Apr 2026 23:26:35 GMT  
		Size: 46.0 MB (46027181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:119e965ffc79cef4d8e12fc957237344d9f0e68aa205bd9ddd59bd93be36aa75`  
		Last Modified: Tue, 28 Apr 2026 23:26:38 GMT  
		Size: 140.2 MB (140236502 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da300b1596e29956e7dce430c2add26efb2a9fab33b9a0c9889268025374c91c`  
		Last Modified: Tue, 28 Apr 2026 23:26:33 GMT  
		Size: 25.6 KB (25615 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:jdk-alpine` - unknown; unknown

```console
$ docker pull gradle@sha256:46ff221c1c8670cd3665010300a58991dc4b646d08c5f2db88b9399c40709b71
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4652981 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a72fbd65c0d06244ece5f59fe311e45fc88cccd68cbf00b2fb3bda7f5e98fc24`

```dockerfile
```

-	Layers:
	-	`sha256:1d3d5369551fc640da7f2a4d34df13a4471b953a8c8e25f0da3ff9ce576e3b05`  
		Last Modified: Tue, 28 Apr 2026 23:26:33 GMT  
		Size: 4.6 MB (4627889 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9b0d38f1d5a4150f22d455daea0e4d55536f36677c620c8d3d8747e7c576613e`  
		Last Modified: Tue, 28 Apr 2026 23:26:33 GMT  
		Size: 25.1 KB (25092 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:jdk-alpine` - linux; arm64 variant v8

```console
$ docker pull gradle@sha256:02088aaaad170d9e67c2a43b3bb358bbfc17324bbdf82ec28931667447687e09
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **294.8 MB (294801844 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:45df639b188a565930789c8b6b4597a79cc9205f695786a563015fbf0712bff5`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["gradle"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:25 GMT
ADD alpine-minirootfs-3.23.4-aarch64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:25 GMT
CMD ["/bin/sh"]
# Wed, 15 Apr 2026 20:34:16 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 15 Apr 2026 20:34:16 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 15 Apr 2026 20:34:16 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 15 Apr 2026 20:34:16 GMT
RUN set -eux;     apk add --no-cache         fontconfig ttf-dejavu         ca-certificates p11-kit-trust         musl-locales musl-locales-lang         binutils         tzdata         coreutils         openssl     ;     rm -rf /var/cache/apk/* # buildkit
# Wed, 15 Apr 2026 20:34:16 GMT
ENV JAVA_VERSION=jdk-25.0.2+10
# Wed, 15 Apr 2026 20:34:24 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        aarch64)          ESUM='e8d928fb018eabb31a148ebadaa5a5ec69273e6562afede21c426960a6a67143';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.2%2B10/OpenJDK25U-jdk_aarch64_alpine-linux_hotspot_25.0.2_10.tar.gz';          ;;        x86_64)          ESUM='961f13ba0ee1e18c41c50ab642361e4283dee5e7947a48ed6a72c8a661d0cca0';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.2%2B10/OpenJDK25U-jdk_x64_alpine-linux_hotspot_25.0.2_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     apk add --no-cache --virtual .fetch-deps gnupg;     wget -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     apk del --no-network .fetch-deps; # buildkit
# Wed, 15 Apr 2026 20:34:25 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 15 Apr 2026 20:34:25 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 15 Apr 2026 20:34:25 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 15 Apr 2026 20:34:25 GMT
CMD ["jshell"]
# Tue, 28 Apr 2026 23:27:18 GMT
CMD ["gradle"]
# Tue, 28 Apr 2026 23:27:18 GMT
ENV GRADLE_HOME=/opt/gradle
# Tue, 28 Apr 2026 23:27:18 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && addgroup --system --gid 1000 gradle     && adduser --system --ingroup gradle --uid 1000 --shell /bin/ash gradle     && mkdir /home/gradle/.gradle     && chown -R gradle:gradle /home/gradle     && chmod -R o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln -s /home/gradle/.gradle /root/.gradle # buildkit
# Tue, 28 Apr 2026 23:27:18 GMT
VOLUME [/home/gradle/.gradle]
# Tue, 28 Apr 2026 23:27:18 GMT
WORKDIR /home/gradle
# Tue, 28 Apr 2026 23:27:24 GMT
RUN set -o errexit -o nounset     && apk add --no-cache       make       curl       wget       tar             breezy       py3-tzlocal       git       git-lfs       mercurial       subversion         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Tue, 28 Apr 2026 23:27:24 GMT
ENV GRADLE_VERSION=9.5.0
# Tue, 28 Apr 2026 23:27:24 GMT
ARG GRADLE_DOWNLOAD_SHA256=553c78f50dafcd54d65b9a444649057857469edf836431389695608536d6b746
# Tue, 28 Apr 2026 23:27:27 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=553c78f50dafcd54d65b9a444649057857469edf836431389695608536d6b746
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum -c -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln -s "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Tue, 28 Apr 2026 23:27:27 GMT
USER gradle
# Tue, 28 Apr 2026 23:27:28 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=553c78f50dafcd54d65b9a444649057857469edf836431389695608536d6b746
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --stacktrace --debug --version # buildkit
# Tue, 28 Apr 2026 23:27:28 GMT
USER root
```

-	Layers:
	-	`sha256:d17f077ada118cc762df373ff803592abf2dfa3ddafaa7381e364dd27a88fca7`  
		Last Modified: Wed, 15 Apr 2026 20:01:32 GMT  
		Size: 4.2 MB (4199870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed6d717b713a3906ce50c18cc5b8a9f6f962fa3091e74aa852bd01f53906eaba`  
		Last Modified: Wed, 15 Apr 2026 20:34:41 GMT  
		Size: 14.4 MB (14365581 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6022f48e982d301b32dc40f520c5a9a4325231a26157778864500a4679482274`  
		Last Modified: Wed, 15 Apr 2026 20:34:43 GMT  
		Size: 90.4 MB (90431717 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf0812bd713e2fba124f6aa2122ffaa2087b3a28dab5ccbb55cf55dabc2da220`  
		Last Modified: Wed, 15 Apr 2026 20:34:40 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da7f4f6f4f6e536abda7c68bf052334e6e8f4d8b073cc66ab6b42aa6f93d2aaa`  
		Last Modified: Wed, 15 Apr 2026 20:34:40 GMT  
		Size: 2.3 KB (2280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93c6a19c849fda8d06b4c460af40f7dcdbe5f8614b8750957354d3faf8ec7c2e`  
		Last Modified: Tue, 28 Apr 2026 23:27:44 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee6ae2fd0ff3ac9ec48322b9e37e61fa72501366bfbe4102e65289f1476dcab1`  
		Last Modified: Tue, 28 Apr 2026 23:27:46 GMT  
		Size: 45.5 MB (45535387 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64b4f2f5533e25b4e2c95a26915e5ebde6fbd75913237ed34728ed483d2cd177`  
		Last Modified: Tue, 28 Apr 2026 23:27:48 GMT  
		Size: 140.2 MB (140236481 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9bf5cb679d3e79c64b9a10b23c9579b60e6fbdda2b7729c34e74ee067923a137`  
		Last Modified: Tue, 28 Apr 2026 23:27:44 GMT  
		Size: 29.4 KB (29357 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:jdk-alpine` - unknown; unknown

```console
$ docker pull gradle@sha256:00e6b8411f9c93dfedcd077433a4e3ae1e2dd6aee7e0922d48b2ce8bfafc7650
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.8 MB (4802794 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:49dcbdb3a374d37845f10ce36416a501d4a9ff7c84ddeb1ba52c9e4af5a697a6`

```dockerfile
```

-	Layers:
	-	`sha256:6de22b7330ba247e95a2b1d01733e968972d90e70d0fbdb67ca85c85b75200fb`  
		Last Modified: Tue, 28 Apr 2026 23:27:44 GMT  
		Size: 4.8 MB (4777457 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:195a62ce6abde6d1eb05b2c53a5929e6c9bdeea4c64dfa6ee96d3dc3399492f6`  
		Last Modified: Tue, 28 Apr 2026 23:27:44 GMT  
		Size: 25.3 KB (25337 bytes)  
		MIME: application/vnd.in-toto+json
