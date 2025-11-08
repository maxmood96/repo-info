## `gradle:9-jdk21-alpine`

```console
$ docker pull gradle@sha256:c92188dd54660d7249b708db95262ef2c91bf75a726b686e040442c1c372e25d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `gradle:9-jdk21-alpine` - linux; amd64

```console
$ docker pull gradle@sha256:1da55cf69dc34a54f5d23d158e473f586b910662c01f7facf6e39c5fff6bd890
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **363.1 MB (363145958 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca83cda55519225b4acfe617dbc2a457119a15aa972fc5720a0a327ab7ae1f5c`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["gradle"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-x86_64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Sat, 08 Nov 2025 17:59:09 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 08 Nov 2025 17:59:09 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 08 Nov 2025 17:59:09 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Sat, 08 Nov 2025 17:59:09 GMT
RUN set -eux;     apk add --no-cache         fontconfig ttf-dejavu         gnupg         ca-certificates p11-kit-trust         musl-locales musl-locales-lang         binutils         tzdata         coreutils         openssl     ;     rm -rf /var/cache/apk/* # buildkit
# Sat, 08 Nov 2025 17:59:09 GMT
ENV JAVA_VERSION=jdk-21.0.9+10
# Sat, 08 Nov 2025 17:59:14 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        aarch64)          ESUM='6d3c2b956d6b837bfdc992e58488fb16c96e5852820e9feaa42a8672bbca9c7b';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.9%2B10/OpenJDK21U-jdk_aarch64_alpine-linux_hotspot_21.0.9_10.tar.gz';          ;;        x86_64)          ESUM='52e30d3157432e87ee464b656f776f0a22946f1f3182eea779258284bc6f55da';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.9%2B10/OpenJDK21U-jdk_x64_alpine-linux_hotspot_21.0.9_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Sat, 08 Nov 2025 17:59:16 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Sat, 08 Nov 2025 17:59:16 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Sat, 08 Nov 2025 17:59:16 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Sat, 08 Nov 2025 17:59:16 GMT
CMD ["jshell"]
# Sat, 08 Nov 2025 18:21:17 GMT
CMD ["gradle"]
# Sat, 08 Nov 2025 18:21:17 GMT
ENV GRADLE_HOME=/opt/gradle
# Sat, 08 Nov 2025 18:21:17 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && addgroup --system --gid 1000 gradle     && adduser --system --ingroup gradle --uid 1000 --shell /bin/ash gradle     && mkdir /home/gradle/.gradle     && chown -R gradle:gradle /home/gradle     && chmod -R o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln -s /home/gradle/.gradle /root/.gradle # buildkit
# Sat, 08 Nov 2025 18:21:17 GMT
VOLUME [/home/gradle/.gradle]
# Sat, 08 Nov 2025 18:21:17 GMT
WORKDIR /home/gradle
# Sat, 08 Nov 2025 18:21:19 GMT
RUN set -o errexit -o nounset     && apk add --no-cache       make       curl       wget       tar             breezy       py3-tzlocal       git       git-lfs       mercurial       subversion         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Sat, 08 Nov 2025 18:21:19 GMT
ENV GRADLE_VERSION=9.2.0
# Sat, 08 Nov 2025 18:21:19 GMT
ARG GRADLE_DOWNLOAD_SHA256=df67a32e86e3276d011735facb1535f64d0d88df84fa87521e90becc2d735444
# Sat, 08 Nov 2025 18:21:21 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=df67a32e86e3276d011735facb1535f64d0d88df84fa87521e90becc2d735444
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum -c -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln -s "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Sat, 08 Nov 2025 18:21:21 GMT
USER gradle
# Sat, 08 Nov 2025 18:21:21 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=df67a32e86e3276d011735facb1535f64d0d88df84fa87521e90becc2d735444
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Sat, 08 Nov 2025 18:21:21 GMT
USER root
```

-	Layers:
	-	`sha256:2d35ebdb57d9971fea0cac1582aa78935adf8058b2cc32db163c98822e5dfa1b`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 3.8 MB (3802452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:604c946e03558d5b63598812078583a7cacf7c19412e2c71732c6c7e972a09e0`  
		Last Modified: Sat, 08 Nov 2025 17:59:43 GMT  
		Size: 21.1 MB (21112184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a34da1dc78644035d0dc76bd344bb33911551088d2c35e5eae20ee0883291ece`  
		Last Modified: Sat, 08 Nov 2025 18:21:14 GMT  
		Size: 158.1 MB (158102933 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6a3991c44d0e9016c97a7a16b122fc35778b7bf3abb694a7acabc5f8e6551c8`  
		Last Modified: Sat, 08 Nov 2025 17:59:41 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8cb030eff3c05fd59aaea4464781aa26b800aef5bdbe8b20be44289a6d4fde7`  
		Last Modified: Sat, 08 Nov 2025 17:59:41 GMT  
		Size: 2.3 KB (2279 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:650a7e55c5b49bb255fef3a87e31c7ed05c6c0e69fc15394b0798b39caf30aa2`  
		Last Modified: Sat, 08 Nov 2025 18:21:56 GMT  
		Size: 1.0 KB (1013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:932e05e66d905b2fdcc16968ba861fdab2015829140c0e99ab4b7b6813b9d03c`  
		Last Modified: Sat, 08 Nov 2025 18:22:00 GMT  
		Size: 44.5 MB (44548739 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74eca34ca57af554e4c346845cd8c12418e2e6910ba9867828d3b265c74e3735`  
		Last Modified: Sat, 08 Nov 2025 21:41:37 GMT  
		Size: 135.5 MB (135521298 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c2b269c220f529b172bbf476281e15443c739871440f6ed543cec12a6b94442`  
		Last Modified: Sat, 08 Nov 2025 18:21:56 GMT  
		Size: 54.9 KB (54899 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:9-jdk21-alpine` - unknown; unknown

```console
$ docker pull gradle@sha256:58d7ef4ba0f6610024179bb333acad22c0a21250683f68efe6c1b7fe1e1818a9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4728665 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21a611012a047d3efae3b1fcf3f7da0c54bc7235daf8587301a78cea5674117c`

```dockerfile
```

-	Layers:
	-	`sha256:a6749f844b91ca4da95d5700e4a91be057cc9669beb3b5f2970256398e8b894f`  
		Last Modified: Sat, 08 Nov 2025 21:33:15 GMT  
		Size: 4.7 MB (4706080 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:abca140de1c85a762c0dc18faadf554532d56eb472c76ee2f9fbbe666d35ed81`  
		Last Modified: Sat, 08 Nov 2025 21:33:16 GMT  
		Size: 22.6 KB (22585 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:9-jdk21-alpine` - linux; arm64 variant v8

```console
$ docker pull gradle@sha256:04889d32e310a0019a374103ad97850bcd999cd83c10fe9d4a2e4b337b6e1b8d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **361.0 MB (361033863 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ba62f6938ccfff316a4011cef9a325d005a7992b9857e353192005e2488b05f`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["gradle"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-aarch64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Sat, 08 Nov 2025 17:58:30 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 08 Nov 2025 17:58:30 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 08 Nov 2025 17:58:30 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Sat, 08 Nov 2025 17:58:30 GMT
RUN set -eux;     apk add --no-cache         fontconfig ttf-dejavu         gnupg         ca-certificates p11-kit-trust         musl-locales musl-locales-lang         binutils         tzdata         coreutils         openssl     ;     rm -rf /var/cache/apk/* # buildkit
# Sat, 08 Nov 2025 17:58:30 GMT
ENV JAVA_VERSION=jdk-21.0.9+10
# Sat, 08 Nov 2025 17:58:37 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        aarch64)          ESUM='6d3c2b956d6b837bfdc992e58488fb16c96e5852820e9feaa42a8672bbca9c7b';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.9%2B10/OpenJDK21U-jdk_aarch64_alpine-linux_hotspot_21.0.9_10.tar.gz';          ;;        x86_64)          ESUM='52e30d3157432e87ee464b656f776f0a22946f1f3182eea779258284bc6f55da';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.9%2B10/OpenJDK21U-jdk_x64_alpine-linux_hotspot_21.0.9_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Sat, 08 Nov 2025 17:58:38 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Sat, 08 Nov 2025 17:58:38 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Sat, 08 Nov 2025 17:58:38 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Sat, 08 Nov 2025 17:58:38 GMT
CMD ["jshell"]
# Sat, 08 Nov 2025 18:22:17 GMT
CMD ["gradle"]
# Sat, 08 Nov 2025 18:22:17 GMT
ENV GRADLE_HOME=/opt/gradle
# Sat, 08 Nov 2025 18:22:17 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && addgroup --system --gid 1000 gradle     && adduser --system --ingroup gradle --uid 1000 --shell /bin/ash gradle     && mkdir /home/gradle/.gradle     && chown -R gradle:gradle /home/gradle     && chmod -R o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln -s /home/gradle/.gradle /root/.gradle # buildkit
# Sat, 08 Nov 2025 18:22:17 GMT
VOLUME [/home/gradle/.gradle]
# Sat, 08 Nov 2025 18:22:17 GMT
WORKDIR /home/gradle
# Sat, 08 Nov 2025 18:22:19 GMT
RUN set -o errexit -o nounset     && apk add --no-cache       make       curl       wget       tar             breezy       py3-tzlocal       git       git-lfs       mercurial       subversion         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Sat, 08 Nov 2025 18:22:19 GMT
ENV GRADLE_VERSION=9.2.0
# Sat, 08 Nov 2025 18:22:19 GMT
ARG GRADLE_DOWNLOAD_SHA256=df67a32e86e3276d011735facb1535f64d0d88df84fa87521e90becc2d735444
# Sat, 08 Nov 2025 18:22:21 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=df67a32e86e3276d011735facb1535f64d0d88df84fa87521e90becc2d735444
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum -c -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln -s "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Sat, 08 Nov 2025 18:22:21 GMT
USER gradle
# Sat, 08 Nov 2025 18:22:22 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=df67a32e86e3276d011735facb1535f64d0d88df84fa87521e90becc2d735444
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Sat, 08 Nov 2025 18:22:22 GMT
USER root
```

-	Layers:
	-	`sha256:6b59a28fa20117e6048ad0616b8d8c901877ef15ff4c7f18db04e4f01f43bc39`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 4.1 MB (4138069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:534675d10f4caa61d314d425f92d547712626251f89901c5d58eac317205e1c5`  
		Last Modified: Sat, 08 Nov 2025 17:59:06 GMT  
		Size: 21.2 MB (21164202 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ac0dd9c7e27c9284c00f27ca9959b156926e12010ba8683e583ff6811916f12`  
		Last Modified: Sat, 08 Nov 2025 18:22:14 GMT  
		Size: 156.1 MB (156097412 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9c7361609fe55d3eb9a77ca907ab0d5f394b754ecf497fbd624cd8fe359a6db`  
		Last Modified: Sat, 08 Nov 2025 17:59:05 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:867c03b825a35a5db0249203ef051f7e12f2bc4c110f281f6de68072d3c55bab`  
		Last Modified: Sat, 08 Nov 2025 17:58:49 GMT  
		Size: 2.3 KB (2279 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69fa47183061c57951442eb0ee42cb5a898c3a3b5a9f52da44e99a37c6d85c48`  
		Last Modified: Sat, 08 Nov 2025 18:22:48 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:957c3da829addc9419461a0167e4e4ea6d04843730713d7e8bb88e83a1b251ab`  
		Last Modified: Sat, 08 Nov 2025 18:23:00 GMT  
		Size: 44.1 MB (44050056 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2ffef528be230d5f78c673e6f07f928f552d241342356f70bca3f55239d69ae`  
		Last Modified: Sat, 08 Nov 2025 21:41:56 GMT  
		Size: 135.5 MB (135521137 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3113b31f21a0cb009daac4056653c0a1d7cd0f3cc468edcc0392014e9b68131`  
		Last Modified: Sat, 08 Nov 2025 18:22:48 GMT  
		Size: 59.5 KB (59536 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:9-jdk21-alpine` - unknown; unknown

```console
$ docker pull gradle@sha256:d75cfafcb53584d40b0c6c73439ce40b83b5753a20a3c399aeb47af2ece92a19
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4878942 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bce429f73385ff9bc43200527d35e52e04fa8e4f501efdac8ac06b593bcc213c`

```dockerfile
```

-	Layers:
	-	`sha256:672eed435b0454c1df987e80fa2503ff431f7013f22db6b0b190c641017c3841`  
		Last Modified: Sat, 08 Nov 2025 21:33:20 GMT  
		Size: 4.9 MB (4856208 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:aaa0d21bdc5e4ecf544032a9301567832c8a0261ec5605215ba62c340ccbcccf`  
		Last Modified: Sat, 08 Nov 2025 21:33:21 GMT  
		Size: 22.7 KB (22734 bytes)  
		MIME: application/vnd.in-toto+json
