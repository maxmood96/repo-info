## `gradle:9-jdk-alpine`

```console
$ docker pull gradle@sha256:4d50266538c871adbcd8ece20d61d10e42b6c8c7dec1f10498d9508d45759c35
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `gradle:9-jdk-alpine` - linux; amd64

```console
$ docker pull gradle@sha256:e427a17acc80a270b14e9b306a6a68e7e369812a543013145aa89d6b9cdd915b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **296.3 MB (296319009 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a2d263f9521b023f71b5eeb5396bd17427c93eca1d4738349dc297cb7b144bc2`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["gradle"]`

```dockerfile
# Mon, 22 Jun 2026 19:20:09 GMT
ADD alpine-minirootfs-3.23.5-x86_64.tar.gz / # buildkit
# Mon, 22 Jun 2026 19:20:09 GMT
CMD ["/bin/sh"]
# Mon, 22 Jun 2026 19:57:28 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 22 Jun 2026 19:57:28 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 22 Jun 2026 19:57:28 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 22 Jun 2026 19:57:28 GMT
RUN set -eux;     apk add --no-cache         fontconfig ttf-dejavu         ca-certificates p11-kit-trust         musl-locales musl-locales-lang         binutils         tzdata         coreutils         openssl     ;     rm -rf /var/cache/apk/* # buildkit
# Mon, 22 Jun 2026 19:57:28 GMT
ENV JAVA_VERSION=jdk-25.0.3+9
# Mon, 22 Jun 2026 19:57:35 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        aarch64)          ESUM='6ed368e93049d3b188c045fce0b20953bbea92fe0614dbbf4d3fd8daad7be3b2';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.3%2B9/OpenJDK25U-jdk_aarch64_alpine-linux_hotspot_25.0.3_9.tar.gz';          ;;        x86_64)          ESUM='51c2415b370aac7c3796b0c4663c8fcf91bc22d76f03df95b25fa5667cb5fdd8';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.3%2B9/OpenJDK25U-jdk_x64_alpine-linux_hotspot_25.0.3_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     apk add --no-cache --virtual .fetch-deps gnupg;     wget -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     apk del --no-network .fetch-deps; # buildkit
# Mon, 22 Jun 2026 19:57:36 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Mon, 22 Jun 2026 19:57:36 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Mon, 22 Jun 2026 19:57:36 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Mon, 22 Jun 2026 19:57:36 GMT
CMD ["jshell"]
# Mon, 29 Jun 2026 17:10:54 GMT
CMD ["gradle"]
# Mon, 29 Jun 2026 17:10:54 GMT
ENV GRADLE_HOME=/opt/gradle
# Mon, 29 Jun 2026 17:10:54 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && addgroup --system --gid 1000 gradle     && adduser --system --ingroup gradle --uid 1000 --shell /bin/ash gradle     && mkdir /home/gradle/.gradle     && chown -R gradle:gradle /home/gradle     && chmod -R o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln -s /home/gradle/.gradle /root/.gradle # buildkit
# Mon, 29 Jun 2026 17:10:54 GMT
VOLUME [/home/gradle/.gradle]
# Mon, 29 Jun 2026 17:10:54 GMT
WORKDIR /home/gradle
# Mon, 29 Jun 2026 17:11:02 GMT
RUN set -o errexit -o nounset     && apk add --no-cache       make       curl       wget       tar             breezy       py3-tzlocal       git       git-lfs       mercurial       subversion         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Mon, 29 Jun 2026 17:11:02 GMT
ENV GRADLE_VERSION=9.6.1
# Mon, 29 Jun 2026 17:11:02 GMT
ARG GRADLE_DOWNLOAD_SHA256=9c0f7faeeb306cb14e4279a3e084ca6b596894089a0638e68a07c945a32c9e14
# Mon, 29 Jun 2026 17:11:04 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=9c0f7faeeb306cb14e4279a3e084ca6b596894089a0638e68a07c945a32c9e14
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum -c -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln -s "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Mon, 29 Jun 2026 17:11:04 GMT
USER gradle
# Mon, 29 Jun 2026 17:11:05 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=9c0f7faeeb306cb14e4279a3e084ca6b596894089a0638e68a07c945a32c9e14
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --stacktrace --debug --version # buildkit
# Mon, 29 Jun 2026 17:11:05 GMT
USER root
```

-	Layers:
	-	`sha256:e6f31ffc071e5560b82a8685fba8214954e5721e3e49269d00958316edbe89fe`  
		Last Modified: Mon, 22 Jun 2026 12:03:33 GMT  
		Size: 3.8 MB (3844421 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95dd7d1a57040850aa18d8f120a347787a853ddadfc0e04c01ba359687f83037`  
		Last Modified: Mon, 22 Jun 2026 19:57:55 GMT  
		Size: 14.3 MB (14259376 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:586ae85e2c68546c53c9b39b13ad3a217cff435d3f4ed14c0808da512b593ea2`  
		Last Modified: Mon, 22 Jun 2026 19:58:08 GMT  
		Size: 91.6 MB (91624437 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1580feaf93ee040ffb3f5ef134e5cc50ea4a1357ecdd98270885a7563d2b8e21`  
		Last Modified: Mon, 22 Jun 2026 19:57:50 GMT  
		Size: 131.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84edc40c41dfe07d6b44bf4c0fa58803f7070a8fb7ec3f9603d8cb0e50ac8058`  
		Last Modified: Mon, 22 Jun 2026 19:57:50 GMT  
		Size: 2.3 KB (2281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af5fbc2a263a1f5acbbb1b4da9cae7756eb99be53b12acc917be9ffdf9940a4a`  
		Last Modified: Mon, 29 Jun 2026 17:11:19 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aaec641306e2ce243da3ea98b2069f0ce49c751f806daa4d7f05f6301be3e54f`  
		Last Modified: Mon, 29 Jun 2026 17:11:22 GMT  
		Size: 46.0 MB (45965453 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4ed663515e560f29f7e779e4a5055d9f6e83e2657fe4e30b69b83f83a8614bf`  
		Last Modified: Mon, 29 Jun 2026 17:11:24 GMT  
		Size: 140.6 MB (140596248 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28e8db2e33a63e48baf41ad81b53963b5a528653118f1be9d2fecea34ccba89d`  
		Last Modified: Mon, 29 Jun 2026 17:11:20 GMT  
		Size: 25.6 KB (25618 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:9-jdk-alpine` - unknown; unknown

```console
$ docker pull gradle@sha256:e68e70da967cd795a0becb3d14f81fca2b38e0595932dae34adeb2a08b1659a7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4646944 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3cc3d97d3d1b9e677b4f600b7dcb64925ef3cb328abcc70bd59fa411738bac5`

```dockerfile
```

-	Layers:
	-	`sha256:8f77926e457254de34ceb7dcb267a1e27baa2ea42beaa6131b2c36f70f8f1722`  
		Last Modified: Mon, 29 Jun 2026 17:11:20 GMT  
		Size: 4.6 MB (4621856 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:09fecded04845d9b0542dcca4702574b4e251988eed4cbaa7b7fbedfff18da63`  
		Last Modified: Mon, 29 Jun 2026 17:11:19 GMT  
		Size: 25.1 KB (25088 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:9-jdk-alpine` - linux; arm64 variant v8

```console
$ docker pull gradle@sha256:1f6fea37bfb546a2ebf11840245524352d8d803e1509a832a73749a07e0383d3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **295.2 MB (295186081 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:11b367c7e98d6da8caae69db0a7b4d694e00cf316087af5669ef06bac27ed6ee`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["gradle"]`

```dockerfile
# Mon, 22 Jun 2026 19:19:57 GMT
ADD alpine-minirootfs-3.23.5-aarch64.tar.gz / # buildkit
# Mon, 22 Jun 2026 19:19:57 GMT
CMD ["/bin/sh"]
# Mon, 22 Jun 2026 20:12:39 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 22 Jun 2026 20:12:39 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 22 Jun 2026 20:12:39 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 22 Jun 2026 20:12:39 GMT
RUN set -eux;     apk add --no-cache         fontconfig ttf-dejavu         ca-certificates p11-kit-trust         musl-locales musl-locales-lang         binutils         tzdata         coreutils         openssl     ;     rm -rf /var/cache/apk/* # buildkit
# Mon, 22 Jun 2026 20:12:39 GMT
ENV JAVA_VERSION=jdk-25.0.3+9
# Mon, 22 Jun 2026 20:12:45 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        aarch64)          ESUM='6ed368e93049d3b188c045fce0b20953bbea92fe0614dbbf4d3fd8daad7be3b2';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.3%2B9/OpenJDK25U-jdk_aarch64_alpine-linux_hotspot_25.0.3_9.tar.gz';          ;;        x86_64)          ESUM='51c2415b370aac7c3796b0c4663c8fcf91bc22d76f03df95b25fa5667cb5fdd8';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.3%2B9/OpenJDK25U-jdk_x64_alpine-linux_hotspot_25.0.3_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     apk add --no-cache --virtual .fetch-deps gnupg;     wget -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     apk del --no-network .fetch-deps; # buildkit
# Mon, 22 Jun 2026 20:12:46 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Mon, 22 Jun 2026 20:12:46 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Mon, 22 Jun 2026 20:12:46 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Mon, 22 Jun 2026 20:12:46 GMT
CMD ["jshell"]
# Mon, 29 Jun 2026 17:11:04 GMT
CMD ["gradle"]
# Mon, 29 Jun 2026 17:11:04 GMT
ENV GRADLE_HOME=/opt/gradle
# Mon, 29 Jun 2026 17:11:04 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && addgroup --system --gid 1000 gradle     && adduser --system --ingroup gradle --uid 1000 --shell /bin/ash gradle     && mkdir /home/gradle/.gradle     && chown -R gradle:gradle /home/gradle     && chmod -R o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln -s /home/gradle/.gradle /root/.gradle # buildkit
# Mon, 29 Jun 2026 17:11:04 GMT
VOLUME [/home/gradle/.gradle]
# Mon, 29 Jun 2026 17:11:04 GMT
WORKDIR /home/gradle
# Mon, 29 Jun 2026 17:11:21 GMT
RUN set -o errexit -o nounset     && apk add --no-cache       make       curl       wget       tar             breezy       py3-tzlocal       git       git-lfs       mercurial       subversion         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Mon, 29 Jun 2026 17:11:21 GMT
ENV GRADLE_VERSION=9.6.1
# Mon, 29 Jun 2026 17:11:21 GMT
ARG GRADLE_DOWNLOAD_SHA256=9c0f7faeeb306cb14e4279a3e084ca6b596894089a0638e68a07c945a32c9e14
# Mon, 29 Jun 2026 17:11:24 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=9c0f7faeeb306cb14e4279a3e084ca6b596894089a0638e68a07c945a32c9e14
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum -c -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln -s "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Mon, 29 Jun 2026 17:11:24 GMT
USER gradle
# Mon, 29 Jun 2026 17:11:25 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=9c0f7faeeb306cb14e4279a3e084ca6b596894089a0638e68a07c945a32c9e14
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --stacktrace --debug --version # buildkit
# Mon, 29 Jun 2026 17:11:25 GMT
USER root
```

-	Layers:
	-	`sha256:14a4754c352fba4c6c0da8e4f01bb990463c19f7ff63e090073c385bd2bc5046`  
		Last Modified: Mon, 22 Jun 2026 12:03:31 GMT  
		Size: 4.2 MB (4181860 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff532a92b2635da709828a163e9a5ed2f5149ecbe38b06fce240f8fb7104afca`  
		Last Modified: Mon, 22 Jun 2026 20:13:02 GMT  
		Size: 14.3 MB (14320296 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de05b5f3adafc3ef06ed696a78315ea4e1caf24c78e679cc659d636c92fbdd77`  
		Last Modified: Mon, 22 Jun 2026 20:13:06 GMT  
		Size: 90.6 MB (90571688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a582b2da42ce858dfb28843505bc7c46dab8db82854a593f73fe11f4abc3d085`  
		Last Modified: Mon, 22 Jun 2026 20:13:01 GMT  
		Size: 130.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2881aa8c3290ef38ec53319eae6c5498e1f555bf0142e50a1dd91eb8728d60dd`  
		Last Modified: Mon, 22 Jun 2026 20:13:01 GMT  
		Size: 2.3 KB (2281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:925932e25a83ce02be51698d7d7a9b7758e3e5acbaa648c62caa841c00c67bb7`  
		Last Modified: Mon, 29 Jun 2026 17:11:41 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57f104cd39739765a9d91a6fb8126f86fb535a3a826e6cc1761aebbaff20f3af`  
		Last Modified: Mon, 29 Jun 2026 17:11:43 GMT  
		Size: 45.5 MB (45483196 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a053119ff5ca726027838146f0d7efc675a1696782afcd30946cee912b169ecb`  
		Last Modified: Mon, 29 Jun 2026 17:11:47 GMT  
		Size: 140.6 MB (140596236 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfd34b2f0707a150cc8e3cfc1b5ade76587d00f4f21a2d84bc8b1037f8dd78f3`  
		Last Modified: Mon, 29 Jun 2026 17:11:41 GMT  
		Size: 29.4 KB (29350 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:9-jdk-alpine` - unknown; unknown

```console
$ docker pull gradle@sha256:8be59e254fce9731c2d5cbbb7542c01223444afa629a3bfa4ef63a005a88e8a1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.8 MB (4796757 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c775c88acdac789e90a86d7937dd6f6ec5b5d6a3b457652f8f9e9953aaacb489`

```dockerfile
```

-	Layers:
	-	`sha256:98ec3d62e4b9a2d1ec4200d0536d8095c9194014ef56604e0a32afcf646f3b55`  
		Last Modified: Mon, 29 Jun 2026 17:11:41 GMT  
		Size: 4.8 MB (4771424 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:471ba595ebb9954074a0df4160d89eb95869b6be344b5dde557ab9a193bf4fe3`  
		Last Modified: Mon, 29 Jun 2026 17:11:41 GMT  
		Size: 25.3 KB (25333 bytes)  
		MIME: application/vnd.in-toto+json
