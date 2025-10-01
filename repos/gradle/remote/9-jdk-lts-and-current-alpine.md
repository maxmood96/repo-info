## `gradle:9-jdk-lts-and-current-alpine`

```console
$ docker pull gradle@sha256:ae3b0524396b28dba4a19229ca2cd918dc214a03e947c0cae60c9e9c74578637
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `gradle:9-jdk-lts-and-current-alpine` - linux; amd64

```console
$ docker pull gradle@sha256:7e26691884c7c6c1d58493f540a75889e1b8ebf1daf1ef3e1fc41bab8ceb46e8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **292.9 MB (292864481 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:908db9050f0e99ff1cc582bf43fb275cd1271b5b4573596b3af1ad869db0edc1`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["gradle"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-x86_64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Thu, 25 Sep 2025 19:59:06 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 25 Sep 2025 19:59:06 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 25 Sep 2025 19:59:06 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 25 Sep 2025 19:59:06 GMT
RUN set -eux;     apk add --no-cache         fontconfig ttf-dejavu         ca-certificates p11-kit-trust         musl-locales musl-locales-lang         binutils         tzdata         coreutils         openssl     ;     rm -rf /var/cache/apk/* # buildkit
# Thu, 25 Sep 2025 19:59:06 GMT
ENV JAVA_VERSION=jdk-25+36
# Thu, 25 Sep 2025 19:59:06 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        aarch64)          ESUM='1f18ba69ca7d674724307a66928a9b80049748b4276c629450935543db2cdfb1';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25%2B36/OpenJDK25U-jdk_aarch64_alpine-linux_hotspot_25_36.tar.gz';          ;;        x86_64)          ESUM='637e47474d411ed86134f413af7d5fef4180ddb0bf556347b7e74a88cf8904c8';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25%2B36/OpenJDK25U-jdk_x64_alpine-linux_hotspot_25_36.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     apk add --no-cache --virtual .fetch-deps gnupg;     wget -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     apk del --no-network .fetch-deps; # buildkit
# Thu, 25 Sep 2025 19:59:06 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 25 Sep 2025 19:59:06 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 25 Sep 2025 19:59:06 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 25 Sep 2025 19:59:06 GMT
CMD ["jshell"]
# Tue, 30 Sep 2025 09:31:25 GMT
RUN set -o errexit -o nounset     && ln -s /opt/java/openjdk /opt/java/openjdk25 # buildkit
# Tue, 30 Sep 2025 09:31:25 GMT
ENV JAVA_CURRENT_HOME=/opt/java/openjdk25
# Tue, 30 Sep 2025 09:31:25 GMT
ENV JAVA_LTS_HOME=/opt/java/openjdk25
# Tue, 30 Sep 2025 09:31:25 GMT
CMD ["gradle"]
# Tue, 30 Sep 2025 09:31:25 GMT
ENV GRADLE_HOME=/opt/gradle
# Tue, 30 Sep 2025 09:31:25 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && addgroup --system --gid 1000 gradle     && adduser --system --ingroup gradle --uid 1000 --shell /bin/ash gradle     && mkdir /home/gradle/.gradle     && chown -R gradle:gradle /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln -s /home/gradle/.gradle /root/.gradle       && echo "Ensuring Gradle detects installed JDKs"    && echo "org.gradle.java.installations.auto-detect=false" > /home/gradle/.gradle/gradle.properties    && echo "org.gradle.java.installations.auto-download=false" >> /home/gradle/.gradle/gradle.properties    && echo "org.gradle.java.installations.fromEnv=JAVA_LTS_HOME,JAVA_CURRENT_HOME" >> /home/gradle/.gradle/gradle.properties # buildkit
# Tue, 30 Sep 2025 09:31:25 GMT
VOLUME [/home/gradle/.gradle]
# Tue, 30 Sep 2025 09:31:25 GMT
WORKDIR /home/gradle
# Tue, 30 Sep 2025 09:31:25 GMT
RUN set -o errexit -o nounset     && apk add --no-cache       make       curl       wget       tar             breezy       py3-tzlocal       git       git-lfs       mercurial       subversion         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Tue, 30 Sep 2025 09:31:25 GMT
ENV GRADLE_VERSION=9.1.0
# Tue, 30 Sep 2025 09:31:25 GMT
ARG GRADLE_DOWNLOAD_SHA256=a17ddd85a26b6a7f5ddb71ff8b05fc5104c0202c6e64782429790c933686c806
# Tue, 30 Sep 2025 09:31:25 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=a17ddd85a26b6a7f5ddb71ff8b05fc5104c0202c6e64782429790c933686c806
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum -c -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln -s "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Tue, 30 Sep 2025 09:31:25 GMT
USER gradle
# Tue, 30 Sep 2025 09:31:25 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=a17ddd85a26b6a7f5ddb71ff8b05fc5104c0202c6e64782429790c933686c806
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Tue, 30 Sep 2025 09:31:25 GMT
USER root
```

-	Layers:
	-	`sha256:9824c27679d3b27c5e1cb00a73adb6f4f8d556994111c12db3c5d61a0c843df8`  
		Last Modified: Tue, 15 Jul 2025 19:00:01 GMT  
		Size: 3.8 MB (3799689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a3235af166d0e0dd50e19e20858b82f8426896169d8fb006e7af70cf5bab2ec`  
		Last Modified: Thu, 25 Sep 2025 21:10:16 GMT  
		Size: 16.7 MB (16712375 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1517093c1e4a89db0baebdd7ad1f00eec21e82ed85917c7e5ad6a38c4f713ca5`  
		Last Modified: Thu, 25 Sep 2025 21:10:21 GMT  
		Size: 91.3 MB (91266566 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3572efb6542a9d6c0e9c176353bc30d46e298950e0b84a312f2dc9c3f0773460`  
		Last Modified: Thu, 25 Sep 2025 21:10:16 GMT  
		Size: 130.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d62a6643ab7738e694834bd6c11821c0dd1dad73b8338ef28de3e60b90bfc142`  
		Last Modified: Thu, 25 Sep 2025 21:10:08 GMT  
		Size: 2.3 KB (2281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16c587a48bb5e2a3c25ff5a19c8f76872bd42a013855fda926dc6874b0f29f56`  
		Last Modified: Tue, 30 Sep 2025 16:58:27 GMT  
		Size: 151.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2d2df9bd341189ecc0099871f1cd2ced940682d5150b7a146413c312550dd4f`  
		Last Modified: Tue, 30 Sep 2025 16:58:27 GMT  
		Size: 1.1 KB (1139 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:425229add137ae36ea2eb647447743c00f835b3fceab7e0717993a8cd63a79a1`  
		Last Modified: Tue, 30 Sep 2025 16:58:31 GMT  
		Size: 46.5 MB (46513067 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70cbc53948218c6ab14bba204b66754a3d655f60264d0208b2a1063054469a44`  
		Last Modified: Wed, 01 Oct 2025 14:58:18 GMT  
		Size: 134.5 MB (134514153 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6858e47de13edde9f5e6f2450f5e89032e9969a3541377dac84c54045d527db1`  
		Last Modified: Tue, 30 Sep 2025 16:58:22 GMT  
		Size: 54.9 KB (54898 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:9-jdk-lts-and-current-alpine` - unknown; unknown

```console
$ docker pull gradle@sha256:3d3eb42a1bbcf54167961e088e6eb9388937e12f83973278e9638ec718f75cc6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4617261 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c95e68634df0f97ca5fdd7d5e393dc7a348939fe4b6348402c4188306a4ad41`

```dockerfile
```

-	Layers:
	-	`sha256:24061edda96de943014fcf1a7300d0424347c03686d0a34d994a590d64d3c304`  
		Last Modified: Wed, 01 Oct 2025 14:21:09 GMT  
		Size: 4.6 MB (4588973 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1856bd8017c6ef6d0046ceb53a2c6ca606b7296f0fc834127a8eaa9e79783a3b`  
		Last Modified: Wed, 01 Oct 2025 14:21:10 GMT  
		Size: 28.3 KB (28288 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:9-jdk-lts-and-current-alpine` - linux; arm64 variant v8

```console
$ docker pull gradle@sha256:a7cb8f428792071e0deb860476b67d2529307d4b68264baa521531f8960c12c2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **448.6 MB (448575293 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1396bde4fd3f9690c829b0b41893ffe7fc1ef3660afc38b3211c5a5d9cec5d40`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["gradle"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-aarch64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Fri, 01 Aug 2025 11:04:34 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 01 Aug 2025 11:04:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 01 Aug 2025 11:04:34 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 01 Aug 2025 11:04:34 GMT
RUN set -eux;     apk add --no-cache         fontconfig ttf-dejavu         gnupg         ca-certificates p11-kit-trust         musl-locales musl-locales-lang         binutils         tzdata         coreutils         openssl     ;     rm -rf /var/cache/apk/* # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
ENV JAVA_VERSION=jdk-21.0.8+9
# Fri, 01 Aug 2025 11:04:34 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        aarch64)          ESUM='4773cfdc59d66b75f4a68ac843b2b5854791840114cf8bb1b56fb6f7826ae498';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.8%2B9/OpenJDK21U-jdk_aarch64_alpine-linux_hotspot_21.0.8_9.tar.gz';          ;;        x86_64)          ESUM='73c4cbe10f4f385383d9cb54d34f2bee2c68b5265f9e3d954f3326948c40c0be';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.8%2B9/OpenJDK21U-jdk_x64_alpine-linux_hotspot_21.0.8_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Fri, 01 Aug 2025 11:04:34 GMT
CMD ["jshell"]
# Fri, 19 Sep 2025 14:40:42 GMT
COPY /opt/java/openjdk /opt/java/openjdk24 # buildkit
# Fri, 19 Sep 2025 14:40:42 GMT
RUN set -o errexit -o nounset     && ln -s /opt/java/openjdk /opt/java/openjdk21 # buildkit
# Fri, 19 Sep 2025 14:40:42 GMT
ENV JAVA_CURRENT_HOME=/opt/java/openjdk24
# Fri, 19 Sep 2025 14:40:42 GMT
ENV JAVA_LTS_HOME=/opt/java/openjdk21
# Fri, 19 Sep 2025 14:40:42 GMT
CMD ["gradle"]
# Fri, 19 Sep 2025 14:40:42 GMT
ENV GRADLE_HOME=/opt/gradle
# Fri, 19 Sep 2025 14:40:42 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && addgroup --system --gid 1000 gradle     && adduser --system --ingroup gradle --uid 1000 --shell /bin/ash gradle     && mkdir /home/gradle/.gradle     && chown -R gradle:gradle /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln -s /home/gradle/.gradle /root/.gradle       && echo "Ensuring Gradle detects installed JDKs"    && echo "org.gradle.java.installations.auto-detect=false" > /home/gradle/.gradle/gradle.properties    && echo "org.gradle.java.installations.auto-download=false" >> /home/gradle/.gradle/gradle.properties    && echo "org.gradle.java.installations.fromEnv=JAVA_LTS_HOME,JAVA_CURRENT_HOME" >> /home/gradle/.gradle/gradle.properties # buildkit
# Fri, 19 Sep 2025 14:40:42 GMT
VOLUME [/home/gradle/.gradle]
# Fri, 19 Sep 2025 14:40:42 GMT
WORKDIR /home/gradle
# Fri, 19 Sep 2025 14:40:42 GMT
RUN set -o errexit -o nounset     && apk add --no-cache       curl       make             breezy       py3-tzlocal       git       git-lfs       mercurial       subversion         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Fri, 19 Sep 2025 14:40:42 GMT
ENV GRADLE_VERSION=9.1.0
# Fri, 19 Sep 2025 14:40:42 GMT
ARG GRADLE_DOWNLOAD_SHA256=a17ddd85a26b6a7f5ddb71ff8b05fc5104c0202c6e64782429790c933686c806
# Fri, 19 Sep 2025 14:40:42 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=a17ddd85a26b6a7f5ddb71ff8b05fc5104c0202c6e64782429790c933686c806
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum -c -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln -s "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Fri, 19 Sep 2025 14:40:42 GMT
USER gradle
# Fri, 19 Sep 2025 14:40:42 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=a17ddd85a26b6a7f5ddb71ff8b05fc5104c0202c6e64782429790c933686c806
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Fri, 19 Sep 2025 14:40:42 GMT
USER root
```

-	Layers:
	-	`sha256:6e174226ea690ced550e5641249a412cdbefd2d09871f3e64ab52137a54ba606`  
		Last Modified: Tue, 15 Jul 2025 18:59:50 GMT  
		Size: 4.1 MB (4130750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20a495748323e0cdac275f94a75856b53137d10e7dd79d59568fe601407fb00e`  
		Last Modified: Mon, 04 Aug 2025 19:31:51 GMT  
		Size: 21.1 MB (21148725 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:686152e11509087fae61a232dd8c14a35ba03ee6d67dc590eff8efd157e12de9`  
		Last Modified: Mon, 04 Aug 2025 21:27:06 GMT  
		Size: 156.0 MB (156022610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25a5e3450f3fe69d4cac3d21cb8d6c1c51e6d6f96214aa277c280b7b8c543832`  
		Last Modified: Mon, 04 Aug 2025 19:31:49 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5af7201f64b2984b23a0f6114fdb4930c66ab8886bf4145e5fce7dda16c5f25`  
		Last Modified: Mon, 04 Aug 2025 19:31:49 GMT  
		Size: 2.3 KB (2280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c93b728d5936bd95b61deb5d5db299b6fb85c0129c27721c2ab5c6b078e1237`  
		Last Modified: Fri, 19 Sep 2025 22:46:27 GMT  
		Size: 89.1 MB (89117487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:930a5c38783b1157df7693b2a8035e9f06da7164e2aa64a7c0329e14770a3794`  
		Last Modified: Fri, 19 Sep 2025 18:25:24 GMT  
		Size: 153.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb88103db4a962f256d03b8513f1f8b7eb97e42fd79d0657a0f38a2231aa4799`  
		Last Modified: Fri, 19 Sep 2025 18:25:24 GMT  
		Size: 1.1 KB (1140 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:925fc75f736bfbff9fb75a29907847ba3bd8179dd944af714d9de5d0a1189dd5`  
		Last Modified: Fri, 19 Sep 2025 22:46:30 GMT  
		Size: 43.6 MB (43578534 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:967724859069961e6d5fb0598333cc9c5930ffe75af445b71048cb6a4ecd88d3`  
		Last Modified: Fri, 19 Sep 2025 22:46:38 GMT  
		Size: 134.5 MB (134513918 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c4ead13fd833dfa2781b96efc1cee24227728146fedb3892ad0ce245186483b`  
		Last Modified: Fri, 19 Sep 2025 18:25:26 GMT  
		Size: 59.5 KB (59536 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:9-jdk-lts-and-current-alpine` - unknown; unknown

```console
$ docker pull gradle@sha256:fd9f812e19dc518dab517650f37ea5d978b7f4d70152606a0e71958b711ec195
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.0 MB (4978104 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:711318ac2dd30691586041fb4209e4a0be617aa03ea156003fff9f15baca1bac`

```dockerfile
```

-	Layers:
	-	`sha256:8276195d6a52043db539918c8a324ffeed3e750bf8a542d9efc50c9b46a0fcf6`  
		Last Modified: Fri, 19 Sep 2025 20:22:40 GMT  
		Size: 4.9 MB (4945604 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5b43268a5e985c94c5ac5d17032b928a8cccbe9dd363c37748f608688d4cceb4`  
		Last Modified: Fri, 19 Sep 2025 20:22:41 GMT  
		Size: 32.5 KB (32500 bytes)  
		MIME: application/vnd.in-toto+json
