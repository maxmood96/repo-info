## `gradle:jdk-25-and-25-alpine`

```console
$ docker pull gradle@sha256:6020308def76e3827f0d2ff4bd8f0f5a063812987931af9ec977da0f9816fe6a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `gradle:jdk-25-and-25-alpine` - linux; amd64

```console
$ docker pull gradle@sha256:cf43cb8b59300f8c8f3b908a1d990b289e89dfb814231a916efcd5f2e260f4dc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **293.5 MB (293466425 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b105dd8ebaf3065e58f5b240ef905d7edb6cdfef2a4ffa7ac2ad83b410cff947`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["gradle"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:04 GMT
ADD alpine-minirootfs-3.23.3-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:04 GMT
CMD ["/bin/sh"]
# Thu, 05 Feb 2026 22:20:43 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 05 Feb 2026 22:20:43 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 05 Feb 2026 22:20:43 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 05 Feb 2026 22:20:43 GMT
RUN set -eux;     apk add --no-cache         fontconfig ttf-dejavu         ca-certificates p11-kit-trust         musl-locales musl-locales-lang         binutils         tzdata         coreutils         openssl     ;     rm -rf /var/cache/apk/* # buildkit
# Thu, 05 Feb 2026 22:20:43 GMT
ENV JAVA_VERSION=jdk-25.0.2+10
# Thu, 05 Feb 2026 22:20:50 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        aarch64)          ESUM='e8d928fb018eabb31a148ebadaa5a5ec69273e6562afede21c426960a6a67143';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.2%2B10/OpenJDK25U-jdk_aarch64_alpine-linux_hotspot_25.0.2_10.tar.gz';          ;;        x86_64)          ESUM='961f13ba0ee1e18c41c50ab642361e4283dee5e7947a48ed6a72c8a661d0cca0';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.2%2B10/OpenJDK25U-jdk_x64_alpine-linux_hotspot_25.0.2_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     apk add --no-cache --virtual .fetch-deps gnupg;     wget -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     apk del --no-network .fetch-deps; # buildkit
# Thu, 05 Feb 2026 22:20:51 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 05 Feb 2026 22:20:51 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 05 Feb 2026 22:20:51 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 05 Feb 2026 22:20:51 GMT
CMD ["jshell"]
# Wed, 04 Mar 2026 17:55:41 GMT
RUN set -o errexit -o nounset     && ln -s /opt/java/openjdk /opt/java/openjdk25 # buildkit
# Wed, 04 Mar 2026 17:55:41 GMT
ENV JAVA_CURRENT_HOME=/opt/java/openjdk25
# Wed, 04 Mar 2026 17:55:41 GMT
ENV JAVA_LTS_HOME=/opt/java/openjdk25
# Wed, 04 Mar 2026 17:55:41 GMT
CMD ["gradle"]
# Wed, 04 Mar 2026 17:55:41 GMT
ENV GRADLE_HOME=/opt/gradle
# Wed, 04 Mar 2026 17:55:41 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && addgroup --system --gid 1000 gradle     && adduser --system --ingroup gradle --uid 1000 --shell /bin/ash gradle     && mkdir /home/gradle/.gradle     && chown -R gradle:gradle /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln -s /home/gradle/.gradle /root/.gradle       && echo "Ensuring Gradle detects installed JDKs"    && echo "org.gradle.java.installations.auto-detect=false" > /home/gradle/.gradle/gradle.properties    && echo "org.gradle.java.installations.auto-download=false" >> /home/gradle/.gradle/gradle.properties    && echo "org.gradle.java.installations.fromEnv=JAVA_LTS_HOME,JAVA_CURRENT_HOME" >> /home/gradle/.gradle/gradle.properties # buildkit
# Wed, 04 Mar 2026 17:55:41 GMT
VOLUME [/home/gradle/.gradle]
# Wed, 04 Mar 2026 17:55:41 GMT
WORKDIR /home/gradle
# Wed, 04 Mar 2026 17:55:44 GMT
RUN set -o errexit -o nounset     && apk add --no-cache       make       curl       wget       tar             breezy       py3-tzlocal       git       git-lfs       mercurial       subversion         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Wed, 04 Mar 2026 17:55:44 GMT
ENV GRADLE_VERSION=9.4.0
# Wed, 04 Mar 2026 17:55:44 GMT
ARG GRADLE_DOWNLOAD_SHA256=60ea723356d81263e8002fec0fcf9e2b0eee0c0850c7a3d7ab0a63f2ccc601f3
# Wed, 04 Mar 2026 17:55:46 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=60ea723356d81263e8002fec0fcf9e2b0eee0c0850c7a3d7ab0a63f2ccc601f3
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum -c -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln -s "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Wed, 04 Mar 2026 17:55:46 GMT
USER gradle
# Wed, 04 Mar 2026 17:55:47 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=60ea723356d81263e8002fec0fcf9e2b0eee0c0850c7a3d7ab0a63f2ccc601f3
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --stacktrace --debug --version # buildkit
# Wed, 04 Mar 2026 17:55:47 GMT
USER root
```

-	Layers:
	-	`sha256:589002ba0eaed121a1dbf42f6648f29e5be55d5c8a6ee0f8eaa0285cc21ac153`  
		Last Modified: Wed, 28 Jan 2026 01:18:09 GMT  
		Size: 3.9 MB (3861821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a150fdcc19ea38586861ab60f38c860b790aae07d0df506d6237d0b88dd7bd6f`  
		Last Modified: Thu, 05 Feb 2026 22:21:06 GMT  
		Size: 14.3 MB (14303782 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6acd3bd6814d41ef248fdd907c1157cbd4d90e1cc3ec091e962a6416099873bc`  
		Last Modified: Thu, 05 Feb 2026 22:21:08 GMT  
		Size: 91.5 MB (91491467 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36b2ab561e1f5769d12480d85e27bf1a14a7757ff69b3acea0acc6b4bb0171cc`  
		Last Modified: Thu, 05 Feb 2026 22:21:05 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53405ff8853b1f58bfdc8d736024ea0d1b6df7fa5dedfb0e52a34829c361f358`  
		Last Modified: Thu, 05 Feb 2026 22:21:05 GMT  
		Size: 2.3 KB (2280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bd38f6934ae6972c74212ab3b4d62abfec234113ae8b5f4b1e73a6c436f5ba4`  
		Last Modified: Wed, 04 Mar 2026 17:56:01 GMT  
		Size: 152.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8a80f72e20cb2411d5a404f36690a65b79f80bd57fc6632287bd81348f0bd1c`  
		Last Modified: Wed, 04 Mar 2026 17:56:01 GMT  
		Size: 1.1 KB (1139 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7e23b5a37dcfe98c17396997f2971eb1a3be5071f30dabe14ff1a9fb470b3e8`  
		Last Modified: Wed, 04 Mar 2026 17:56:04 GMT  
		Size: 46.0 MB (46006688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef3f6badd572ae05f8a86e8040fcb206bd406a05c68cc1dfeffe5167b1d1878a`  
		Last Modified: Wed, 04 Mar 2026 17:56:06 GMT  
		Size: 137.8 MB (137773322 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b1420ad291096f38adbe7dbb1264d20e2f889d6af398ab13e2adaf28c2a31c3`  
		Last Modified: Wed, 04 Mar 2026 17:56:02 GMT  
		Size: 25.6 KB (25613 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:jdk-25-and-25-alpine` - unknown; unknown

```console
$ docker pull gradle@sha256:aeb62c3012d867c5515385d4cb5129ac7b0c876f02abd75995ac2416f8453c84
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4628225 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5157a491732f76822487f4f4debca8bd43b96e9b7868b12def4624ddbc269869`

```dockerfile
```

-	Layers:
	-	`sha256:006e18eb8c363e03c86a9fbce0bfca09da7e4f1ab58f03e3884f80080bb37b77`  
		Last Modified: Wed, 04 Mar 2026 17:56:02 GMT  
		Size: 4.6 MB (4599911 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:398ed38934778dd9a4205de5a768e5fbc41645aebaad6fcc5e6919546847cf0c`  
		Last Modified: Wed, 04 Mar 2026 17:56:01 GMT  
		Size: 28.3 KB (28314 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:jdk-25-and-25-alpine` - linux; arm64 variant v8

```console
$ docker pull gradle@sha256:abd88166d53c549191f206a6c36c0d459c6eb4c56ef6ccc3db72a1ecf694a386
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **292.3 MB (292328578 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3d041edb721cd5b0407cf6bdacfe759de9d23caa8aed5030554c781fa8a3267`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["gradle"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:09 GMT
ADD alpine-minirootfs-3.23.3-aarch64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:09 GMT
CMD ["/bin/sh"]
# Thu, 05 Feb 2026 22:19:42 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 05 Feb 2026 22:19:42 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 05 Feb 2026 22:19:42 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 05 Feb 2026 22:19:42 GMT
RUN set -eux;     apk add --no-cache         fontconfig ttf-dejavu         ca-certificates p11-kit-trust         musl-locales musl-locales-lang         binutils         tzdata         coreutils         openssl     ;     rm -rf /var/cache/apk/* # buildkit
# Thu, 05 Feb 2026 22:19:42 GMT
ENV JAVA_VERSION=jdk-25.0.2+10
# Thu, 05 Feb 2026 22:19:48 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        aarch64)          ESUM='e8d928fb018eabb31a148ebadaa5a5ec69273e6562afede21c426960a6a67143';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.2%2B10/OpenJDK25U-jdk_aarch64_alpine-linux_hotspot_25.0.2_10.tar.gz';          ;;        x86_64)          ESUM='961f13ba0ee1e18c41c50ab642361e4283dee5e7947a48ed6a72c8a661d0cca0';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.2%2B10/OpenJDK25U-jdk_x64_alpine-linux_hotspot_25.0.2_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     apk add --no-cache --virtual .fetch-deps gnupg;     wget -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     apk del --no-network .fetch-deps; # buildkit
# Thu, 05 Feb 2026 22:19:50 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 05 Feb 2026 22:19:50 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 05 Feb 2026 22:19:50 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 05 Feb 2026 22:19:50 GMT
CMD ["jshell"]
# Wed, 04 Mar 2026 17:55:10 GMT
RUN set -o errexit -o nounset     && ln -s /opt/java/openjdk /opt/java/openjdk25 # buildkit
# Wed, 04 Mar 2026 17:55:10 GMT
ENV JAVA_CURRENT_HOME=/opt/java/openjdk25
# Wed, 04 Mar 2026 17:55:10 GMT
ENV JAVA_LTS_HOME=/opt/java/openjdk25
# Wed, 04 Mar 2026 17:55:10 GMT
CMD ["gradle"]
# Wed, 04 Mar 2026 17:55:10 GMT
ENV GRADLE_HOME=/opt/gradle
# Wed, 04 Mar 2026 17:55:10 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && addgroup --system --gid 1000 gradle     && adduser --system --ingroup gradle --uid 1000 --shell /bin/ash gradle     && mkdir /home/gradle/.gradle     && chown -R gradle:gradle /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln -s /home/gradle/.gradle /root/.gradle       && echo "Ensuring Gradle detects installed JDKs"    && echo "org.gradle.java.installations.auto-detect=false" > /home/gradle/.gradle/gradle.properties    && echo "org.gradle.java.installations.auto-download=false" >> /home/gradle/.gradle/gradle.properties    && echo "org.gradle.java.installations.fromEnv=JAVA_LTS_HOME,JAVA_CURRENT_HOME" >> /home/gradle/.gradle/gradle.properties # buildkit
# Wed, 04 Mar 2026 17:55:10 GMT
VOLUME [/home/gradle/.gradle]
# Wed, 04 Mar 2026 17:55:10 GMT
WORKDIR /home/gradle
# Wed, 04 Mar 2026 17:55:12 GMT
RUN set -o errexit -o nounset     && apk add --no-cache       make       curl       wget       tar             breezy       py3-tzlocal       git       git-lfs       mercurial       subversion         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Wed, 04 Mar 2026 17:55:12 GMT
ENV GRADLE_VERSION=9.4.0
# Wed, 04 Mar 2026 17:55:12 GMT
ARG GRADLE_DOWNLOAD_SHA256=60ea723356d81263e8002fec0fcf9e2b0eee0c0850c7a3d7ab0a63f2ccc601f3
# Wed, 04 Mar 2026 17:55:15 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=60ea723356d81263e8002fec0fcf9e2b0eee0c0850c7a3d7ab0a63f2ccc601f3
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum -c -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln -s "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Wed, 04 Mar 2026 17:55:15 GMT
USER gradle
# Wed, 04 Mar 2026 17:55:16 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=60ea723356d81263e8002fec0fcf9e2b0eee0c0850c7a3d7ab0a63f2ccc601f3
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --stacktrace --debug --version # buildkit
# Wed, 04 Mar 2026 17:55:16 GMT
USER root
```

-	Layers:
	-	`sha256:d8ad8cd72600f46cc068e16c39046ebc76526e41051f43a8c249884b200936c0`  
		Last Modified: Wed, 28 Jan 2026 01:18:15 GMT  
		Size: 4.2 MB (4197091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1dc273c5968a27128010b44442da19c1d19512b5d65a3a7fc4734eec44550e27`  
		Last Modified: Thu, 05 Feb 2026 22:20:05 GMT  
		Size: 14.4 MB (14373158 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e47108ee2f22449f768312319f1c90c0d5a1580374197687fd1944d8e2265225`  
		Last Modified: Thu, 05 Feb 2026 22:20:07 GMT  
		Size: 90.4 MB (90431353 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33fed661f46011e75ee9460b18305d0584e08525180dd346895a225fab422298`  
		Last Modified: Thu, 05 Feb 2026 22:20:04 GMT  
		Size: 130.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e47f9177a4521d408115970652519968867bb5c776093bf3b8b10b66aaa3caa1`  
		Last Modified: Thu, 05 Feb 2026 22:20:04 GMT  
		Size: 2.3 KB (2281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7acdf60bdf8f426cbc75800e75e00c90224d8aad4663bd68b2c0a8b4936c7c5a`  
		Last Modified: Wed, 04 Mar 2026 17:55:31 GMT  
		Size: 152.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:454e62c61a420077e2027791766bf0a5f9f287a7217888e51f7cc0dd7983f9ae`  
		Last Modified: Wed, 04 Mar 2026 17:55:31 GMT  
		Size: 1.1 KB (1137 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87979ea3ea4aae95c2f461add3f1d8ad6f540335fc1ee59bd5dea6d7ae518d2c`  
		Last Modified: Wed, 04 Mar 2026 17:55:33 GMT  
		Size: 45.5 MB (45520354 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96be204e7b25293608dc64cf02a6c34f7538c3a33530704508aa92f01124497c`  
		Last Modified: Wed, 04 Mar 2026 17:55:35 GMT  
		Size: 137.8 MB (137773549 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:adb76ee0d908e11711073492f1d1cc079ae3574de72690f74703efacf63b7ed1`  
		Last Modified: Wed, 04 Mar 2026 17:55:32 GMT  
		Size: 29.3 KB (29341 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:jdk-25-and-25-alpine` - unknown; unknown

```console
$ docker pull gradle@sha256:4c04080f8af5408cc7246e9e2b549e5a504ed6381baefb8a54f5e5b751c6ee83
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.8 MB (4777958 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:84adf561d1f66a162ecbdd4a70e001de87e50b9e731beb8bea463c6ccf78f10b`

```dockerfile
```

-	Layers:
	-	`sha256:d529c5ebfe44a84ab769e3db6b6f583247e9a28cfd705e7f9f8952c7bfea5eae`  
		Last Modified: Wed, 04 Mar 2026 17:55:31 GMT  
		Size: 4.7 MB (4749431 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1fc69b22b926f40993b899beacbc328fe7f1c0ad1900deaae9a2bbbd48c71b47`  
		Last Modified: Wed, 04 Mar 2026 17:55:31 GMT  
		Size: 28.5 KB (28527 bytes)  
		MIME: application/vnd.in-toto+json
