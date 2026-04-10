## `gradle:9-jdk26-alpine`

```console
$ docker pull gradle@sha256:48452293c79df4168cfe3fb52a79866f4ad747d15151a42f59d9fbe323b0becc
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `gradle:9-jdk26-alpine` - linux; amd64

```console
$ docker pull gradle@sha256:cfbdf217be04f8f11c099c28b4e409fe6c8b07b1058bbd89210906761329eb2c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **295.7 MB (295743859 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0fd1a11237af3a70d5badd94aaf042ad64ae6a7fb262185afd1151d32fb5f32a`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["gradle"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:04 GMT
ADD alpine-minirootfs-3.23.3-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:04 GMT
CMD ["/bin/sh"]
# Wed, 08 Apr 2026 17:27:02 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 08 Apr 2026 17:27:02 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 08 Apr 2026 17:27:02 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 08 Apr 2026 17:27:02 GMT
RUN set -eux;     apk add --no-cache         fontconfig ttf-dejavu         ca-certificates p11-kit-trust         musl-locales musl-locales-lang         binutils         tzdata         coreutils         openssl     ;     rm -rf /var/cache/apk/* # buildkit
# Wed, 08 Apr 2026 17:27:02 GMT
ENV JAVA_VERSION=jdk-26+35
# Wed, 08 Apr 2026 17:27:11 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        aarch64)          ESUM='049027647a2d1cf3b1e3c1e7dad746aa6436928932bbed9130b87a25f585908a';          BINARY_URL='https://github.com/adoptium/temurin26-binaries/releases/download/jdk-26%2B35/OpenJDK26U-jdk_aarch64_alpine-linux_hotspot_26_35.tar.gz';          ;;        x86_64)          ESUM='c105e581fdccb4e7120d889235d1ad8d5b2bed0af4972bc881e0a8ba687c94a4';          BINARY_URL='https://github.com/adoptium/temurin26-binaries/releases/download/jdk-26%2B35/OpenJDK26U-jdk_x64_alpine-linux_hotspot_26_35.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     apk add --no-cache --virtual .fetch-deps gnupg;     wget -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     apk del --no-network .fetch-deps; # buildkit
# Wed, 08 Apr 2026 17:27:13 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 08 Apr 2026 17:27:13 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 08 Apr 2026 17:27:13 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 08 Apr 2026 17:27:13 GMT
CMD ["jshell"]
# Fri, 10 Apr 2026 16:55:14 GMT
CMD ["gradle"]
# Fri, 10 Apr 2026 16:55:14 GMT
ENV GRADLE_HOME=/opt/gradle
# Fri, 10 Apr 2026 16:55:14 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && addgroup --system --gid 1000 gradle     && adduser --system --ingroup gradle --uid 1000 --shell /bin/ash gradle     && mkdir /home/gradle/.gradle     && chown -R gradle:gradle /home/gradle     && chmod -R o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln -s /home/gradle/.gradle /root/.gradle # buildkit
# Fri, 10 Apr 2026 16:55:14 GMT
VOLUME [/home/gradle/.gradle]
# Fri, 10 Apr 2026 16:55:14 GMT
WORKDIR /home/gradle
# Fri, 10 Apr 2026 16:55:16 GMT
RUN set -o errexit -o nounset     && apk add --no-cache       make       curl       wget       tar             breezy       py3-tzlocal       git       git-lfs       mercurial       subversion         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Fri, 10 Apr 2026 16:55:16 GMT
ENV GRADLE_VERSION=9.4.1
# Fri, 10 Apr 2026 16:55:16 GMT
ARG GRADLE_DOWNLOAD_SHA256=2ab2958f2a1e51120c326cad6f385153bb11ee93b3c216c5fccebfdfbb7ec6cb
# Fri, 10 Apr 2026 16:55:18 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=2ab2958f2a1e51120c326cad6f385153bb11ee93b3c216c5fccebfdfbb7ec6cb
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum -c -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln -s "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Fri, 10 Apr 2026 16:55:18 GMT
USER gradle
# Fri, 10 Apr 2026 16:55:18 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=2ab2958f2a1e51120c326cad6f385153bb11ee93b3c216c5fccebfdfbb7ec6cb
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --stacktrace --debug --version # buildkit
# Fri, 10 Apr 2026 16:55:18 GMT
USER root
```

-	Layers:
	-	`sha256:589002ba0eaed121a1dbf42f6648f29e5be55d5c8a6ee0f8eaa0285cc21ac153`  
		Last Modified: Wed, 28 Jan 2026 01:18:09 GMT  
		Size: 3.9 MB (3861821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93c6d9e7d89cbd69af00c05b6e1f8e836453cf6b5b157a598acc85d79cc992a9`  
		Last Modified: Wed, 08 Apr 2026 17:27:28 GMT  
		Size: 14.3 MB (14304112 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5577c5db19f793491142513b33aac7a7c056c12043adbe2187f56471d189e949`  
		Last Modified: Wed, 08 Apr 2026 17:27:30 GMT  
		Size: 93.7 MB (93716635 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c44de7d97aaccbae3d1907cc254b959ad565314344e0b2b270991d5e3d95da84`  
		Last Modified: Wed, 08 Apr 2026 17:27:27 GMT  
		Size: 131.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0897996f16ec4acd4523b469d5607884c086896ce74ad65d52bba0344025e8b`  
		Last Modified: Wed, 08 Apr 2026 17:27:27 GMT  
		Size: 2.3 KB (2281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89d2b57540f5600516fe6d8eb854ba47ecdc88fd166a5f16ddb0f5053a42fa2e`  
		Last Modified: Fri, 10 Apr 2026 16:55:34 GMT  
		Size: 1.0 KB (1009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d381b80460b758d4693d90a0db4040f7028490ea49ca14ee70fadd89b8be721`  
		Last Modified: Fri, 10 Apr 2026 16:55:36 GMT  
		Size: 46.0 MB (46023793 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b31466e87b4e444e84ed4325f853c25c4e290ac6e5016625b15d62142726159`  
		Last Modified: Fri, 10 Apr 2026 16:55:38 GMT  
		Size: 137.8 MB (137808430 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3f4de3adf4c6656dc656d3ff4d3c43d6c1377233043393c9d2b13a0b6892fd1`  
		Last Modified: Fri, 10 Apr 2026 16:55:34 GMT  
		Size: 25.6 KB (25615 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:9-jdk26-alpine` - unknown; unknown

```console
$ docker pull gradle@sha256:eb95b507184c1b6b1b9cb9a57ba7bfe222280d93ff9196f55ccaaa5737b9f691
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4619189 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:16c9e19852f5bc189c4b4999b795c701cb703eb6c0025c106d660e7d0631176b`

```dockerfile
```

-	Layers:
	-	`sha256:cf5331a69e3ce1cbfb26ce33dacc900db8936da1c67b8a230c23047a81ef39be`  
		Last Modified: Fri, 10 Apr 2026 16:55:34 GMT  
		Size: 4.6 MB (4596577 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:21ed8643cf81d853f2af8f01e109f4dfe79f88a69b511e59b26dd154656a0d1e`  
		Last Modified: Fri, 10 Apr 2026 16:55:34 GMT  
		Size: 22.6 KB (22612 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:9-jdk26-alpine` - linux; arm64 variant v8

```console
$ docker pull gradle@sha256:0e5c07ae75ba0b790fcd479bc36ebbed7257392e37565a504ee1144b166404f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **294.6 MB (294555579 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8975c34bfa5e5abac84b4909e1c318c94489d381dbfc29d102c3e8cc301efbc7`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["gradle"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:09 GMT
ADD alpine-minirootfs-3.23.3-aarch64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:09 GMT
CMD ["/bin/sh"]
# Wed, 08 Apr 2026 17:28:08 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 08 Apr 2026 17:28:08 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 08 Apr 2026 17:28:08 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 08 Apr 2026 17:28:08 GMT
RUN set -eux;     apk add --no-cache         fontconfig ttf-dejavu         ca-certificates p11-kit-trust         musl-locales musl-locales-lang         binutils         tzdata         coreutils         openssl     ;     rm -rf /var/cache/apk/* # buildkit
# Wed, 08 Apr 2026 17:28:08 GMT
ENV JAVA_VERSION=jdk-26+35
# Wed, 08 Apr 2026 17:28:18 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        aarch64)          ESUM='049027647a2d1cf3b1e3c1e7dad746aa6436928932bbed9130b87a25f585908a';          BINARY_URL='https://github.com/adoptium/temurin26-binaries/releases/download/jdk-26%2B35/OpenJDK26U-jdk_aarch64_alpine-linux_hotspot_26_35.tar.gz';          ;;        x86_64)          ESUM='c105e581fdccb4e7120d889235d1ad8d5b2bed0af4972bc881e0a8ba687c94a4';          BINARY_URL='https://github.com/adoptium/temurin26-binaries/releases/download/jdk-26%2B35/OpenJDK26U-jdk_x64_alpine-linux_hotspot_26_35.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     apk add --no-cache --virtual .fetch-deps gnupg;     wget -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     apk del --no-network .fetch-deps; # buildkit
# Wed, 08 Apr 2026 17:28:19 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 08 Apr 2026 17:28:19 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 08 Apr 2026 17:28:19 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 08 Apr 2026 17:28:19 GMT
CMD ["jshell"]
# Fri, 10 Apr 2026 16:56:13 GMT
CMD ["gradle"]
# Fri, 10 Apr 2026 16:56:13 GMT
ENV GRADLE_HOME=/opt/gradle
# Fri, 10 Apr 2026 16:56:13 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && addgroup --system --gid 1000 gradle     && adduser --system --ingroup gradle --uid 1000 --shell /bin/ash gradle     && mkdir /home/gradle/.gradle     && chown -R gradle:gradle /home/gradle     && chmod -R o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln -s /home/gradle/.gradle /root/.gradle # buildkit
# Fri, 10 Apr 2026 16:56:13 GMT
VOLUME [/home/gradle/.gradle]
# Fri, 10 Apr 2026 16:56:13 GMT
WORKDIR /home/gradle
# Fri, 10 Apr 2026 16:56:17 GMT
RUN set -o errexit -o nounset     && apk add --no-cache       make       curl       wget       tar             breezy       py3-tzlocal       git       git-lfs       mercurial       subversion         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Fri, 10 Apr 2026 16:56:17 GMT
ENV GRADLE_VERSION=9.4.1
# Fri, 10 Apr 2026 16:56:17 GMT
ARG GRADLE_DOWNLOAD_SHA256=2ab2958f2a1e51120c326cad6f385153bb11ee93b3c216c5fccebfdfbb7ec6cb
# Fri, 10 Apr 2026 16:56:20 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=2ab2958f2a1e51120c326cad6f385153bb11ee93b3c216c5fccebfdfbb7ec6cb
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum -c -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln -s "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Fri, 10 Apr 2026 16:56:20 GMT
USER gradle
# Fri, 10 Apr 2026 16:56:20 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=2ab2958f2a1e51120c326cad6f385153bb11ee93b3c216c5fccebfdfbb7ec6cb
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --stacktrace --debug --version # buildkit
# Fri, 10 Apr 2026 16:56:20 GMT
USER root
```

-	Layers:
	-	`sha256:d8ad8cd72600f46cc068e16c39046ebc76526e41051f43a8c249884b200936c0`  
		Last Modified: Wed, 28 Jan 2026 01:18:15 GMT  
		Size: 4.2 MB (4197091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9ccdff04ff7edee57bed94a8c62171239c7b006206fd98ad8e30823b60a28da`  
		Last Modified: Wed, 08 Apr 2026 17:28:34 GMT  
		Size: 14.4 MB (14373265 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e76800d5cb27e61f1409e0f4507e139c567e21e69c5dc0e321657337875c7d8c`  
		Last Modified: Wed, 08 Apr 2026 17:28:36 GMT  
		Size: 92.6 MB (92608862 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4fcfff75b67965338d8bc778e36ba0902a20b28ed537fc7b19f4041f6c239640`  
		Last Modified: Wed, 08 Apr 2026 17:28:33 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1827940bcff4b3fffc6024c952b6684419e7a2a77b918483dae0767edb2fc630`  
		Last Modified: Wed, 08 Apr 2026 17:28:34 GMT  
		Size: 2.3 KB (2280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea0d579cdb504af189c73da008d1bdab90bbf7f49b35e5e914d1db638aaf24d4`  
		Last Modified: Fri, 10 Apr 2026 16:56:36 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d328dd49a67a7a751971e1b326bb29fcdd2bea59d8afb06bc51d013245a94a9`  
		Last Modified: Fri, 10 Apr 2026 16:56:38 GMT  
		Size: 45.5 MB (45535150 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e6c5720478d8f18e3a6e16bd358891dac83f96ff76db30a7172cd6e22702688`  
		Last Modified: Fri, 10 Apr 2026 16:56:40 GMT  
		Size: 137.8 MB (137808416 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00968573ba9ecffd8d19299793e07d6151149d80559c41ed112a255095cc2bf3`  
		Last Modified: Fri, 10 Apr 2026 16:56:35 GMT  
		Size: 29.3 KB (29345 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:9-jdk26-alpine` - unknown; unknown

```console
$ docker pull gradle@sha256:31f0c5f266ac6b0d4371174a96e389ba1f8de9166c2cf24b24ce10a6dc7bc0a7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.8 MB (4768810 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d5ebe0bc36e7bcd3bd74029012a5ffba5884feb8a935f8cbf25aac9d390a46c`

```dockerfile
```

-	Layers:
	-	`sha256:ce8390d4d5c7c52ad6f88d6da60f27e5af7c8470727a8bbee1022c4b481ee5cd`  
		Last Modified: Fri, 10 Apr 2026 16:56:36 GMT  
		Size: 4.7 MB (4746049 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:be07c65d4bcd5a34f85a52b1150e613e59d0164f6efaec3a3f5c0a428e4d14df`  
		Last Modified: Fri, 10 Apr 2026 16:56:35 GMT  
		Size: 22.8 KB (22761 bytes)  
		MIME: application/vnd.in-toto+json
