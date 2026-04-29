## `gradle:jdk-lts-and-current-alpine`

```console
$ docker pull gradle@sha256:666af55ac081a1f1ccb54d68aa3a9aef8c23d23cdc8b05a4830bd01c6a6d0173
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `gradle:jdk-lts-and-current-alpine` - linux; amd64

```console
$ docker pull gradle@sha256:ed7f04495fdd2e7718953fc9627e19ebb3b4f8aaace051a388bba0f5171d058a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **389.6 MB (389631950 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1bbb905feb0f4232f10be82c05d047a44d7b57549a8ea4c8009c2de8b24b924a`
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
# Tue, 28 Apr 2026 23:31:41 GMT
COPY /opt/java/openjdk /opt/java/openjdk26 # buildkit
# Tue, 28 Apr 2026 23:31:41 GMT
RUN set -o errexit -o nounset     && ln -s /opt/java/openjdk /opt/java/openjdk25 # buildkit
# Tue, 28 Apr 2026 23:31:41 GMT
ENV JAVA_LTS_HOME=/opt/java/openjdk25
# Tue, 28 Apr 2026 23:31:41 GMT
ENV JAVA_CURRENT_HOME=/opt/java/openjdk26
# Tue, 28 Apr 2026 23:31:41 GMT
CMD ["gradle"]
# Tue, 28 Apr 2026 23:31:41 GMT
ENV GRADLE_HOME=/opt/gradle
# Tue, 28 Apr 2026 23:31:41 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && addgroup --system --gid 1000 gradle     && adduser --system --ingroup gradle --uid 1000 --shell /bin/ash gradle     && mkdir /home/gradle/.gradle     && chown -R gradle:gradle /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln -s /home/gradle/.gradle /root/.gradle       && echo "Ensuring Gradle detects installed JDKs"    && echo "org.gradle.java.installations.auto-detect=false" > /home/gradle/.gradle/gradle.properties    && echo "org.gradle.java.installations.auto-download=false" >> /home/gradle/.gradle/gradle.properties    && echo "org.gradle.java.installations.fromEnv=JAVA_LTS_HOME,JAVA_CURRENT_HOME" >> /home/gradle/.gradle/gradle.properties # buildkit
# Tue, 28 Apr 2026 23:31:41 GMT
VOLUME [/home/gradle/.gradle]
# Tue, 28 Apr 2026 23:31:41 GMT
WORKDIR /home/gradle
# Tue, 28 Apr 2026 23:31:43 GMT
RUN set -o errexit -o nounset     && apk add --no-cache       make       curl       wget       tar             breezy       py3-tzlocal       git       git-lfs       mercurial       subversion         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Tue, 28 Apr 2026 23:31:43 GMT
ENV GRADLE_VERSION=9.5.0
# Tue, 28 Apr 2026 23:31:43 GMT
ARG GRADLE_DOWNLOAD_SHA256=553c78f50dafcd54d65b9a444649057857469edf836431389695608536d6b746
# Tue, 28 Apr 2026 23:31:46 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=553c78f50dafcd54d65b9a444649057857469edf836431389695608536d6b746
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum -c -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln -s "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Tue, 28 Apr 2026 23:31:46 GMT
USER gradle
# Tue, 28 Apr 2026 23:31:46 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=553c78f50dafcd54d65b9a444649057857469edf836431389695608536d6b746
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --stacktrace --debug --version # buildkit
# Tue, 28 Apr 2026 23:31:46 GMT
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
	-	`sha256:431c76798c641597a680444755ec8ba3e9f5ec7e68455f60bf247567bc61bded`  
		Last Modified: Tue, 28 Apr 2026 23:32:12 GMT  
		Size: 93.7 MB (93675738 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0fa97d0a3828515d2d0440bb30e6f6f730c88d0b9c6ffd9c4d13c99b6ac034f`  
		Last Modified: Tue, 28 Apr 2026 23:32:08 GMT  
		Size: 152.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4423a5ed9ad1342d55fda6bbab17db4ee87cd1e45bdef7e2931c847dc073ff50`  
		Last Modified: Tue, 28 Apr 2026 23:32:07 GMT  
		Size: 1.1 KB (1138 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97bbcaf22b2fd86f2b1304eb8eaddd5b074199ac1883826224606ebf7b472671`  
		Last Modified: Tue, 28 Apr 2026 23:32:10 GMT  
		Size: 46.0 MB (46027239 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bc39cd20db7a1f471e14bd4d9544ed110f6a1125ef9b0d4af477b443f5293fe`  
		Last Modified: Tue, 28 Apr 2026 23:32:14 GMT  
		Size: 140.2 MB (140236458 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa1912aa784ed62bff667d1a04d234f2a0dc648baf92972510cff162f227cf9e`  
		Last Modified: Tue, 28 Apr 2026 23:32:09 GMT  
		Size: 25.6 KB (25610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:jdk-lts-and-current-alpine` - unknown; unknown

```console
$ docker pull gradle@sha256:b6db9105051da7631fd37796a55f9e271d0cf155757e4d8cdd20cbf4e920d940
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.8 MB (4777830 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f21612b832d1121d46accfd6d981cbc224b4d19fc2ab71d736a208abc818702`

```dockerfile
```

-	Layers:
	-	`sha256:f0da91186df5abcde9cda909a54ed405b0bfa99f361ac31fc89d1759b93fe323`  
		Last Modified: Tue, 28 Apr 2026 23:32:08 GMT  
		Size: 4.7 MB (4745432 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f94b938b079f61240d8e0d2c533ae6b8c79bf3c33f2edb5b4755fbfb3805abe9`  
		Last Modified: Tue, 28 Apr 2026 23:32:08 GMT  
		Size: 32.4 KB (32398 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:jdk-lts-and-current-alpine` - linux; arm64 variant v8

```console
$ docker pull gradle@sha256:17df5df871f5e83d04b6e95f452a02a68314b9f08229ea9d4a1953000de32ce9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **387.4 MB (387361410 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b53682bcf245c9140e3d4197fe3a6103d394431d795b13c80046406991b17825`
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
# Tue, 28 Apr 2026 23:32:58 GMT
COPY /opt/java/openjdk /opt/java/openjdk26 # buildkit
# Tue, 28 Apr 2026 23:32:59 GMT
RUN set -o errexit -o nounset     && ln -s /opt/java/openjdk /opt/java/openjdk25 # buildkit
# Tue, 28 Apr 2026 23:32:59 GMT
ENV JAVA_LTS_HOME=/opt/java/openjdk25
# Tue, 28 Apr 2026 23:32:59 GMT
ENV JAVA_CURRENT_HOME=/opt/java/openjdk26
# Tue, 28 Apr 2026 23:32:59 GMT
CMD ["gradle"]
# Tue, 28 Apr 2026 23:32:59 GMT
ENV GRADLE_HOME=/opt/gradle
# Tue, 28 Apr 2026 23:32:59 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && addgroup --system --gid 1000 gradle     && adduser --system --ingroup gradle --uid 1000 --shell /bin/ash gradle     && mkdir /home/gradle/.gradle     && chown -R gradle:gradle /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln -s /home/gradle/.gradle /root/.gradle       && echo "Ensuring Gradle detects installed JDKs"    && echo "org.gradle.java.installations.auto-detect=false" > /home/gradle/.gradle/gradle.properties    && echo "org.gradle.java.installations.auto-download=false" >> /home/gradle/.gradle/gradle.properties    && echo "org.gradle.java.installations.fromEnv=JAVA_LTS_HOME,JAVA_CURRENT_HOME" >> /home/gradle/.gradle/gradle.properties # buildkit
# Tue, 28 Apr 2026 23:32:59 GMT
VOLUME [/home/gradle/.gradle]
# Tue, 28 Apr 2026 23:32:59 GMT
WORKDIR /home/gradle
# Tue, 28 Apr 2026 23:33:01 GMT
RUN set -o errexit -o nounset     && apk add --no-cache       make       curl       wget       tar             breezy       py3-tzlocal       git       git-lfs       mercurial       subversion         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Tue, 28 Apr 2026 23:33:01 GMT
ENV GRADLE_VERSION=9.5.0
# Tue, 28 Apr 2026 23:33:01 GMT
ARG GRADLE_DOWNLOAD_SHA256=553c78f50dafcd54d65b9a444649057857469edf836431389695608536d6b746
# Tue, 28 Apr 2026 23:33:04 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=553c78f50dafcd54d65b9a444649057857469edf836431389695608536d6b746
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum -c -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln -s "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Tue, 28 Apr 2026 23:33:04 GMT
USER gradle
# Tue, 28 Apr 2026 23:33:04 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=553c78f50dafcd54d65b9a444649057857469edf836431389695608536d6b746
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --stacktrace --debug --version # buildkit
# Tue, 28 Apr 2026 23:33:04 GMT
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
	-	`sha256:45cb202a6a1721645abe4201df63eb8e4d1f0359f507873fcc7f36d89e567dc9`  
		Last Modified: Tue, 28 Apr 2026 23:33:30 GMT  
		Size: 92.6 MB (92559068 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d3061a07af5023ad346b4b886c62d6a26e8e16683c7f0885c7d669fef894a6d`  
		Last Modified: Tue, 28 Apr 2026 23:33:25 GMT  
		Size: 152.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c5e88918dddfe1c271d0351967e241dd52aa31f19f404a0d6dbb743f662e796`  
		Last Modified: Tue, 28 Apr 2026 23:33:25 GMT  
		Size: 1.1 KB (1138 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72bcac4b2d69bd00929ed81a67f76e0d49cd49f8cccd532e70d8e937313ffbb5`  
		Last Modified: Tue, 28 Apr 2026 23:33:27 GMT  
		Size: 45.5 MB (45535644 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50252b194ddcddb007fcec199cdaf2ae4f40f6a5181603ef5a70a205a5cec2bf`  
		Last Modified: Tue, 28 Apr 2026 23:33:32 GMT  
		Size: 140.2 MB (140236458 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10e67d29f404e38dbc0546c40654623b34cd49809b6d18990fd5a7d02a089dcb`  
		Last Modified: Tue, 28 Apr 2026 23:33:26 GMT  
		Size: 29.3 KB (29342 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:jdk-lts-and-current-alpine` - unknown; unknown

```console
$ docker pull gradle@sha256:8b0afbb309578ad1d5a893e8f5a9d5e1399f1abfbaf96bbe0b7a81014345db7f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4926965 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:84c8a53eb1af8a1226080dc505aea4ae118084874b99606a1e9a998ad7eec8d1`

```dockerfile
```

-	Layers:
	-	`sha256:0497ace4d26f74a0c8663a1b977200798f4ae822c0a89c16c5b7bd3c20c38bd4`  
		Last Modified: Tue, 28 Apr 2026 23:33:25 GMT  
		Size: 4.9 MB (4894329 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2f61ae82405ff27187e1104af390316bdebdd100e109503e1d1bcae402bd4a04`  
		Last Modified: Tue, 28 Apr 2026 23:33:24 GMT  
		Size: 32.6 KB (32636 bytes)  
		MIME: application/vnd.in-toto+json
