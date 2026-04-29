## `gradle:9-jdk21-alpine`

```console
$ docker pull gradle@sha256:a97d4df49b5ae46e42ad7470d551dd393911c79c190f03949a61779f1cb21b11
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `gradle:9-jdk21-alpine` - linux; amd64

```console
$ docker pull gradle@sha256:e751a2f7be904aa0b5811a2025afe5a34303effdceb13fcd2f59952a014e6384
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **367.6 MB (367552091 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2ca31a9db2a72d41512ed79396554b85f0029edeb67c5de65ae4385239dd8df7`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["gradle"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:40 GMT
ADD alpine-minirootfs-3.23.4-x86_64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:40 GMT
CMD ["/bin/sh"]
# Wed, 15 Apr 2026 20:33:52 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 15 Apr 2026 20:33:52 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 15 Apr 2026 20:33:52 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 15 Apr 2026 20:33:52 GMT
RUN set -eux;     apk add --no-cache         fontconfig ttf-dejavu         gnupg         ca-certificates p11-kit-trust         musl-locales musl-locales-lang         binutils         tzdata         coreutils         openssl     ;     rm -rf /var/cache/apk/* # buildkit
# Wed, 15 Apr 2026 20:33:52 GMT
ENV JAVA_VERSION=jdk-21.0.10+7
# Wed, 15 Apr 2026 20:34:01 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        aarch64)          ESUM='19eba6c3877612157ef1f46deb92745b4567cfcd64b79f15449c68cd2b7501e3';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.10%2B7/OpenJDK21U-jdk_aarch64_alpine-linux_hotspot_21.0.10_7.tar.gz';          ;;        x86_64)          ESUM='8eb39f442c3c603e414af43844b419a9b5d4f3fe221181f323aa4eec1bd20cf8';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.10%2B7/OpenJDK21U-jdk_x64_alpine-linux_hotspot_21.0.10_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Wed, 15 Apr 2026 20:34:02 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 15 Apr 2026 20:34:02 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 15 Apr 2026 20:34:02 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 15 Apr 2026 20:34:02 GMT
CMD ["jshell"]
# Tue, 28 Apr 2026 23:30:20 GMT
CMD ["gradle"]
# Tue, 28 Apr 2026 23:30:20 GMT
ENV GRADLE_HOME=/opt/gradle
# Tue, 28 Apr 2026 23:30:20 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && addgroup --system --gid 1000 gradle     && adduser --system --ingroup gradle --uid 1000 --shell /bin/ash gradle     && mkdir /home/gradle/.gradle     && chown -R gradle:gradle /home/gradle     && chmod -R o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln -s /home/gradle/.gradle /root/.gradle # buildkit
# Tue, 28 Apr 2026 23:30:20 GMT
VOLUME [/home/gradle/.gradle]
# Tue, 28 Apr 2026 23:30:20 GMT
WORKDIR /home/gradle
# Tue, 28 Apr 2026 23:30:22 GMT
RUN set -o errexit -o nounset     && apk add --no-cache       make       curl       wget       tar             breezy       py3-tzlocal       git       git-lfs       mercurial       subversion         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Tue, 28 Apr 2026 23:30:22 GMT
ENV GRADLE_VERSION=9.5.0
# Tue, 28 Apr 2026 23:30:22 GMT
ARG GRADLE_DOWNLOAD_SHA256=553c78f50dafcd54d65b9a444649057857469edf836431389695608536d6b746
# Tue, 28 Apr 2026 23:30:25 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=553c78f50dafcd54d65b9a444649057857469edf836431389695608536d6b746
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum -c -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln -s "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Tue, 28 Apr 2026 23:30:25 GMT
USER gradle
# Tue, 28 Apr 2026 23:30:25 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=553c78f50dafcd54d65b9a444649057857469edf836431389695608536d6b746
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --stacktrace --debug --version # buildkit
# Tue, 28 Apr 2026 23:30:25 GMT
USER root
```

-	Layers:
	-	`sha256:6a0ac1617861a677b045b7ff88545213ec31c0ff08763195a70a4a5adda577bb`  
		Last Modified: Wed, 15 Apr 2026 20:01:46 GMT  
		Size: 3.9 MB (3864189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5ef2c34364d42e41eb14af65c85cfcd9ba8407f18b51bde4f6428bff92388a2`  
		Last Modified: Wed, 15 Apr 2026 20:34:17 GMT  
		Size: 21.3 MB (21315853 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:136a888652a1277373c20061d1c0d79e332ba8eece5ba04c0c24fce61ce8940d`  
		Last Modified: Wed, 15 Apr 2026 20:34:20 GMT  
		Size: 158.1 MB (158118925 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b440bedad35bcaf95f5c16474e5bcdc67677eca1377bc3b6bd9a64aa13552d0`  
		Last Modified: Wed, 15 Apr 2026 20:34:16 GMT  
		Size: 130.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07c1bb0b54884876ce179c9ad3683a68d7689b97597df8b1b2dfeeaaf5e7b60e`  
		Last Modified: Wed, 15 Apr 2026 20:34:16 GMT  
		Size: 2.3 KB (2280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93f48c513cae8bbb8c215acbdb619988ca7c4c7d7fbede4c2e16e64285bdc299`  
		Last Modified: Tue, 28 Apr 2026 23:30:41 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37ccf20f8ae716156f2a82ee97c067899f1d5837c062d904faeda4bc0ba0ce21`  
		Last Modified: Tue, 28 Apr 2026 23:30:44 GMT  
		Size: 44.0 MB (43987735 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45d1ae5a78bcff63c3ed16d4d1a14f78b35508f1dd5a346be74d6ba9e14789b9`  
		Last Modified: Tue, 28 Apr 2026 23:30:46 GMT  
		Size: 140.2 MB (140236318 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e61e0c5b8f4b5e9ba6623cefc80ed554023d66b98beddc791320cba163e0a732`  
		Last Modified: Tue, 28 Apr 2026 23:30:41 GMT  
		Size: 25.6 KB (25618 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:9-jdk21-alpine` - unknown; unknown

```console
$ docker pull gradle@sha256:a5a0a00f22c71924a3c3971ddc930d96eed15f4a9e09d34b641f5a1b855d2de2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4739198 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:37cac0454bfa16d048a3865e44bdbdf83c752aa7112043549fc36e585a2505bd`

```dockerfile
```

-	Layers:
	-	`sha256:2e0a40e772cb59df752438014ceeb6efae1fcc5d6353faba7e139656de8809bb`  
		Last Modified: Tue, 28 Apr 2026 23:30:42 GMT  
		Size: 4.7 MB (4716564 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:45ab2e6b5c2a9998684a1b0911e0185fc235c9729ee59ca3cd1d63a1e817f34e`  
		Last Modified: Tue, 28 Apr 2026 23:30:41 GMT  
		Size: 22.6 KB (22634 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:9-jdk21-alpine` - linux; arm64 variant v8

```console
$ docker pull gradle@sha256:2ee2dbd03964b1df72df55ca4976f7635032038b2360d1b70c56d3043179caec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **365.4 MB (365398927 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f492857c007a0490c3ea4c8f702cc18597113f84a735306307ccc360ebb76e03`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["gradle"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:25 GMT
ADD alpine-minirootfs-3.23.4-aarch64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:25 GMT
CMD ["/bin/sh"]
# Wed, 15 Apr 2026 20:33:55 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 15 Apr 2026 20:33:55 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 15 Apr 2026 20:33:55 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 15 Apr 2026 20:33:55 GMT
RUN set -eux;     apk add --no-cache         fontconfig ttf-dejavu         gnupg         ca-certificates p11-kit-trust         musl-locales musl-locales-lang         binutils         tzdata         coreutils         openssl     ;     rm -rf /var/cache/apk/* # buildkit
# Wed, 15 Apr 2026 20:33:55 GMT
ENV JAVA_VERSION=jdk-21.0.10+7
# Wed, 15 Apr 2026 20:34:03 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        aarch64)          ESUM='19eba6c3877612157ef1f46deb92745b4567cfcd64b79f15449c68cd2b7501e3';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.10%2B7/OpenJDK21U-jdk_aarch64_alpine-linux_hotspot_21.0.10_7.tar.gz';          ;;        x86_64)          ESUM='8eb39f442c3c603e414af43844b419a9b5d4f3fe221181f323aa4eec1bd20cf8';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.10%2B7/OpenJDK21U-jdk_x64_alpine-linux_hotspot_21.0.10_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Wed, 15 Apr 2026 20:34:05 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 15 Apr 2026 20:34:05 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 15 Apr 2026 20:34:05 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 15 Apr 2026 20:34:05 GMT
CMD ["jshell"]
# Tue, 28 Apr 2026 23:30:34 GMT
CMD ["gradle"]
# Tue, 28 Apr 2026 23:30:34 GMT
ENV GRADLE_HOME=/opt/gradle
# Tue, 28 Apr 2026 23:30:34 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && addgroup --system --gid 1000 gradle     && adduser --system --ingroup gradle --uid 1000 --shell /bin/ash gradle     && mkdir /home/gradle/.gradle     && chown -R gradle:gradle /home/gradle     && chmod -R o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln -s /home/gradle/.gradle /root/.gradle # buildkit
# Tue, 28 Apr 2026 23:30:34 GMT
VOLUME [/home/gradle/.gradle]
# Tue, 28 Apr 2026 23:30:34 GMT
WORKDIR /home/gradle
# Tue, 28 Apr 2026 23:30:36 GMT
RUN set -o errexit -o nounset     && apk add --no-cache       make       curl       wget       tar             breezy       py3-tzlocal       git       git-lfs       mercurial       subversion         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Tue, 28 Apr 2026 23:30:36 GMT
ENV GRADLE_VERSION=9.5.0
# Tue, 28 Apr 2026 23:30:36 GMT
ARG GRADLE_DOWNLOAD_SHA256=553c78f50dafcd54d65b9a444649057857469edf836431389695608536d6b746
# Tue, 28 Apr 2026 23:30:39 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=553c78f50dafcd54d65b9a444649057857469edf836431389695608536d6b746
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum -c -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln -s "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Tue, 28 Apr 2026 23:30:39 GMT
USER gradle
# Tue, 28 Apr 2026 23:30:40 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=553c78f50dafcd54d65b9a444649057857469edf836431389695608536d6b746
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --stacktrace --debug --version # buildkit
# Tue, 28 Apr 2026 23:30:40 GMT
USER root
```

-	Layers:
	-	`sha256:d17f077ada118cc762df373ff803592abf2dfa3ddafaa7381e364dd27a88fca7`  
		Last Modified: Wed, 15 Apr 2026 20:01:32 GMT  
		Size: 4.2 MB (4199870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:daaacc5fcb81aaf4c24ca62b7c7d748d4925abc4199e39981b80b93898777d06`  
		Last Modified: Wed, 15 Apr 2026 20:34:22 GMT  
		Size: 21.3 MB (21303504 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ea8e162f72eb44c19a73f38e10d121143bdee45dc7426f76cb9f2b16ab73763`  
		Last Modified: Wed, 15 Apr 2026 20:34:25 GMT  
		Size: 156.1 MB (156129898 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37767c9371d4e03127e4bbe85929010c025d7d442785d1805b213575c0a75fd1`  
		Last Modified: Wed, 15 Apr 2026 20:34:21 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d12d0e0cbded327c9df870505ef20a84efb14dd8ccbe2a48a63e4120f61b65ba`  
		Last Modified: Wed, 15 Apr 2026 20:34:21 GMT  
		Size: 2.3 KB (2280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4ec14664e298cf1f64d5c6af33ce2e6367c0fe05a0b15234e94772c2af43801`  
		Last Modified: Tue, 28 Apr 2026 23:30:56 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ae99efdfa0418b019f6d2601c980156f879289cbd43470016bd320d5de67903`  
		Last Modified: Tue, 28 Apr 2026 23:30:58 GMT  
		Size: 43.5 MB (43496351 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dce42ff44d278fcce0cfc9b3fd70c45e291d4e320105677e7ad253b6ab22db1c`  
		Last Modified: Tue, 28 Apr 2026 23:31:00 GMT  
		Size: 140.2 MB (140236503 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1322991fcde24396ebb0c468d496e22c680e5ec93acbc36ffbec429b03f08929`  
		Last Modified: Tue, 28 Apr 2026 23:30:56 GMT  
		Size: 29.3 KB (29348 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:9-jdk21-alpine` - unknown; unknown

```console
$ docker pull gradle@sha256:125eb1d76b31ceac7b5dab9c39beb0efb20dff23198adaf92d111561b6493ea2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4888822 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7cdae32f71dc05349e9bb390763fe97d937bb96ad4a2cc071c2cb381dd2b3fa9`

```dockerfile
```

-	Layers:
	-	`sha256:77662170adadb4abe2697c4e825264c625cacc7d13e482b28e51e12641c15005`  
		Last Modified: Tue, 28 Apr 2026 23:30:56 GMT  
		Size: 4.9 MB (4866039 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bd4b6175b90505d9bde24c5284ad97b1d5c8c2d6ea0fedd39111e1be989a4e40`  
		Last Modified: Tue, 28 Apr 2026 23:30:56 GMT  
		Size: 22.8 KB (22783 bytes)  
		MIME: application/vnd.in-toto+json
