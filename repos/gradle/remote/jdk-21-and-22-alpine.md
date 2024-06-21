## `gradle:jdk-21-and-22-alpine`

```console
$ docker pull gradle@sha256:c78b2365f085c3019f99fc8954287941e5f679ad440b7380a0927f35aab59220
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `gradle:jdk-21-and-22-alpine` - linux; amd64

```console
$ docker pull gradle@sha256:4192e80cc0f8af0a0ad8ca657504ae3edc3998906280f8e0373ff9aadd8051d0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **505.1 MB (505148693 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f0878c8b70db11fe4c9fa74001bd6d22cf835382df7c591af44c4968fde7bca7`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["gradle"]`

```dockerfile
# Sat, 27 Jan 2024 00:30:48 GMT
ADD file:37a76ec18f9887751cd8473744917d08b7431fc4085097bb6a09d81b41775473 in / 
# Sat, 27 Jan 2024 00:30:48 GMT
CMD ["/bin/sh"]
# Tue, 23 Apr 2024 20:51:38 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 23 Apr 2024 20:51:38 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 23 Apr 2024 20:51:38 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 23 Apr 2024 20:51:38 GMT
RUN set -eux;     apk add --no-cache         fontconfig ttf-dejavu         ca-certificates p11-kit-trust         musl-locales musl-locales-lang         binutils         tzdata     ;     rm -rf /var/cache/apk/* # buildkit
# Tue, 23 Apr 2024 20:51:38 GMT
ENV JAVA_VERSION=jdk-21.0.3+9
# Tue, 23 Apr 2024 20:51:38 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        aarch64|arm64)          ESUM='0f68a9122054149861f6ce9d1b1c176bbe30dd76b36b74c916ba897c12e9d970';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.3%2B9/OpenJDK21U-jdk_aarch64_alpine-linux_hotspot_21.0.3_9.tar.gz';          ;;        amd64|x86_64)          ESUM='8e861638bf6b08c6d5837de6dc929930550928ec5fcc81b9fa7e8296afd0f9c0';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.3%2B9/OpenJDK21U-jdk_x64_alpine-linux_hotspot_21.0.3_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Tue, 23 Apr 2024 20:51:38 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 23 Apr 2024 20:51:38 GMT
COPY entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 23 Apr 2024 20:51:38 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 23 Apr 2024 20:51:38 GMT
CMD ["jshell"]
# Tue, 04 Jun 2024 20:56:32 GMT
COPY /opt/java/openjdk /opt/java/openjdk22 # buildkit
# Tue, 04 Jun 2024 20:56:32 GMT
RUN set -o errexit -o nounset     && ln -s /opt/java/openjdk /opt/java/openjdk21 # buildkit
# Tue, 04 Jun 2024 20:56:32 GMT
ENV JAVA_CURRENT_HOME=/opt/java/openjdk22
# Tue, 04 Jun 2024 20:56:32 GMT
ENV JAVA_LTS_HOME=/opt/java/openjdk21
# Tue, 04 Jun 2024 20:56:32 GMT
CMD ["gradle"]
# Tue, 04 Jun 2024 20:56:32 GMT
ENV GRADLE_HOME=/opt/gradle
# Tue, 04 Jun 2024 20:56:32 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && addgroup --system --gid 1000 gradle     && adduser --system --ingroup gradle --uid 1000 --shell /bin/ash gradle     && mkdir /home/gradle/.gradle     && chown -R gradle:gradle /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln -s /home/gradle/.gradle /root/.gradle       && echo "Ensuring Gradle detects installed JDKs"    && echo "org.gradle.java.installations.auto-detect=false" > /home/gradle/.gradle/gradle.properties    && echo "org.gradle.java.installations.auto-download=false" >> /home/gradle/.gradle/gradle.properties    && echo "org.gradle.java.installations.fromEnv=JAVA_LTS_HOME,JAVA_CURRENT_HOME" >> /home/gradle/.gradle/gradle.properties # buildkit
# Tue, 04 Jun 2024 20:56:32 GMT
VOLUME [/home/gradle/.gradle]
# Tue, 04 Jun 2024 20:56:32 GMT
WORKDIR /home/gradle
# Tue, 04 Jun 2024 20:56:32 GMT
RUN set -o errexit -o nounset     && echo "Installing VCSes"     && apk add --no-cache       git       git-lfs       mercurial       subversion         && echo "Testing VCSes"     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Tue, 04 Jun 2024 20:56:32 GMT
ENV GRADLE_VERSION=8.8
# Tue, 04 Jun 2024 20:56:32 GMT
ARG GRADLE_DOWNLOAD_SHA256=a4b4158601f8636cdeeab09bd76afb640030bb5b144aafe261a5e8af027dc612
# Tue, 04 Jun 2024 20:56:32 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=a4b4158601f8636cdeeab09bd76afb640030bb5b144aafe261a5e8af027dc612
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum -c -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln -s "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Tue, 04 Jun 2024 20:56:32 GMT
USER gradle
# Tue, 04 Jun 2024 20:56:32 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=a4b4158601f8636cdeeab09bd76afb640030bb5b144aafe261a5e8af027dc612
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Tue, 04 Jun 2024 20:56:32 GMT
USER root
```

-	Layers:
	-	`sha256:4abcf20661432fb2d719aaf90656f55c287f8ca915dc1c92ec14ff61e67fbaf8`  
		Last Modified: Sat, 27 Jan 2024 00:31:24 GMT  
		Size: 3.4 MB (3408729 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3fd38fd7cf5b8d60c92e1aa46a24527229fb51b451491d35a7028a8a1d0aba4`  
		Last Modified: Thu, 28 Mar 2024 02:08:23 GMT  
		Size: 13.1 MB (13142803 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:332bf309ecf2b86f336452cb3137f9b266c99d9a10612bd124e2f13e0dad9bb3`  
		Last Modified: Wed, 24 Apr 2024 19:16:14 GMT  
		Size: 158.7 MB (158716489 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e377b89d6767f434b66aef2b55d4397fa1ca4ef205a16f2fc626005be867634`  
		Last Modified: Wed, 24 Apr 2024 19:16:01 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45705fa60e5881f3a69ceb008964dcca0e72d626655d99b6d92e4c0834c7131b`  
		Last Modified: Wed, 24 Apr 2024 19:16:01 GMT  
		Size: 717.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9043056f966fe5ef73f8052c46acb7fd9d0f2f9e6439ed3a1d7ef313e67bb15`  
		Last Modified: Wed, 05 Jun 2024 17:05:59 GMT  
		Size: 156.9 MB (156935616 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3fb55d4630379a2d5372642d2d19db931efeb801c2697564c3dcf0c608ebcfdb`  
		Last Modified: Wed, 05 Jun 2024 17:05:57 GMT  
		Size: 153.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cf3d681c79410bd48c2fd86d562acb1feca911767dd082ab04792c1c7e43e0d`  
		Last Modified: Wed, 05 Jun 2024 17:05:57 GMT  
		Size: 1.4 KB (1432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dce900751485db75756f829d76747223978f4beddc0331f90399f3be63a636e0`  
		Last Modified: Wed, 05 Jun 2024 17:05:58 GMT  
		Size: 34.9 MB (34878913 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dec7e974a3061e0b89796d7b3019268c7eb0195e535e01853728bae417023ab6`  
		Last Modified: Wed, 05 Jun 2024 17:06:00 GMT  
		Size: 138.1 MB (138063334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dca9dda3ccf2d5fb2e7daa393cc37774c6e2124cb33304ae676ce8374ccc6175`  
		Last Modified: Wed, 05 Jun 2024 17:05:58 GMT  
		Size: 285.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:jdk-21-and-22-alpine` - unknown; unknown

```console
$ docker pull gradle@sha256:1ea165568df917325d7d99f895a51c96f144509991c9d795368779f244becdf2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.4 MB (3430587 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d918d143685ed503c13c94ae8036ad66eb2243bb85238b878ab60e6ae7ce5491`

```dockerfile
```

-	Layers:
	-	`sha256:9fa28e7bb8b7de55d3fd03c489dd01f69387fa984183efb31115bc81c2603245`  
		Last Modified: Wed, 05 Jun 2024 17:05:57 GMT  
		Size: 3.4 MB (3400068 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:db111971b236dacb5f8435ce9542cc1adefc3e9bef67d0df8184cf25674392e5`  
		Last Modified: Wed, 05 Jun 2024 17:05:57 GMT  
		Size: 30.5 KB (30519 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:jdk-21-and-22-alpine` - linux; arm64 variant v8

```console
$ docker pull gradle@sha256:30bf33f360ec8778e44325c6a7dc96193330285671069c874913b0a3833b4aca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **501.1 MB (501089845 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c087950fe8bba18f34c798fb4e3128e10d075f9ac22721663e3ce82f0993139`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["gradle"]`

```dockerfile
# Sun, 16 Jun 2024 03:23:28 GMT
ADD file:f5632bd5469a9b26f7ff1739bb0b5dd166613259104f7bf76d587a8a428debcc in / 
# Sun, 16 Jun 2024 03:23:28 GMT
CMD ["/bin/sh"]
# Tue, 23 Apr 2024 20:51:38 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 23 Apr 2024 20:51:38 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 23 Apr 2024 20:51:38 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 23 Apr 2024 20:51:38 GMT
RUN set -eux;     apk add --no-cache         fontconfig ttf-dejavu         ca-certificates p11-kit-trust         musl-locales musl-locales-lang         binutils         tzdata     ;     rm -rf /var/cache/apk/* # buildkit
# Tue, 23 Apr 2024 20:51:38 GMT
ENV JAVA_VERSION=jdk-21.0.3+9
# Tue, 23 Apr 2024 20:51:38 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        aarch64|arm64)          ESUM='0f68a9122054149861f6ce9d1b1c176bbe30dd76b36b74c916ba897c12e9d970';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.3%2B9/OpenJDK21U-jdk_aarch64_alpine-linux_hotspot_21.0.3_9.tar.gz';          ;;        amd64|x86_64)          ESUM='8e861638bf6b08c6d5837de6dc929930550928ec5fcc81b9fa7e8296afd0f9c0';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.3%2B9/OpenJDK21U-jdk_x64_alpine-linux_hotspot_21.0.3_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Tue, 23 Apr 2024 20:51:38 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 23 Apr 2024 20:51:38 GMT
COPY entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 23 Apr 2024 20:51:38 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 23 Apr 2024 20:51:38 GMT
CMD ["jshell"]
# Sun, 16 Jun 2024 03:23:28 GMT
COPY /opt/java/openjdk /opt/java/openjdk22 # buildkit
# Sun, 16 Jun 2024 03:23:28 GMT
RUN set -o errexit -o nounset     && ln -s /opt/java/openjdk /opt/java/openjdk21 # buildkit
# Sun, 16 Jun 2024 03:23:28 GMT
ENV JAVA_CURRENT_HOME=/opt/java/openjdk22
# Sun, 16 Jun 2024 03:23:28 GMT
ENV JAVA_LTS_HOME=/opt/java/openjdk21
# Sun, 16 Jun 2024 03:23:28 GMT
CMD ["gradle"]
# Sun, 16 Jun 2024 03:23:28 GMT
ENV GRADLE_HOME=/opt/gradle
# Sun, 16 Jun 2024 03:23:28 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && addgroup --system --gid 1000 gradle     && adduser --system --ingroup gradle --uid 1000 --shell /bin/ash gradle     && mkdir /home/gradle/.gradle     && chown -R gradle:gradle /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln -s /home/gradle/.gradle /root/.gradle       && echo "Ensuring Gradle detects installed JDKs"    && echo "org.gradle.java.installations.auto-detect=false" > /home/gradle/.gradle/gradle.properties    && echo "org.gradle.java.installations.auto-download=false" >> /home/gradle/.gradle/gradle.properties    && echo "org.gradle.java.installations.fromEnv=JAVA_LTS_HOME,JAVA_CURRENT_HOME" >> /home/gradle/.gradle/gradle.properties # buildkit
# Sun, 16 Jun 2024 03:23:28 GMT
VOLUME [/home/gradle/.gradle]
# Sun, 16 Jun 2024 03:23:28 GMT
WORKDIR /home/gradle
# Sun, 16 Jun 2024 03:23:28 GMT
RUN set -o errexit -o nounset     && echo "Installing VCSes"     && apk add --no-cache       git       git-lfs       mercurial       subversion         && echo "Testing VCSes"     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Sun, 16 Jun 2024 03:23:28 GMT
ENV GRADLE_VERSION=8.8
# Sun, 16 Jun 2024 03:23:28 GMT
ARG GRADLE_DOWNLOAD_SHA256=a4b4158601f8636cdeeab09bd76afb640030bb5b144aafe261a5e8af027dc612
# Sun, 16 Jun 2024 03:23:28 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=a4b4158601f8636cdeeab09bd76afb640030bb5b144aafe261a5e8af027dc612
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum -c -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln -s "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Sun, 16 Jun 2024 03:23:28 GMT
USER gradle
# Sun, 16 Jun 2024 03:23:28 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=a4b4158601f8636cdeeab09bd76afb640030bb5b144aafe261a5e8af027dc612
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Sun, 16 Jun 2024 03:23:28 GMT
USER root
```

-	Layers:
	-	`sha256:d4f2d2bd5ed999e04bfbfb910f14154b488ad32abf053954bff805f47fc3ad1e`  
		Last Modified: Thu, 20 Jun 2024 17:41:12 GMT  
		Size: 3.4 MB (3357202 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6db88ea1e6a26d6517be6a6098be6964b10513b0bfdfea893bc9752c9c04b6e1`  
		Last Modified: Thu, 20 Jun 2024 19:04:39 GMT  
		Size: 13.4 MB (13425513 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66b0682e580b8b1aea7e2a977909ae9bbc90e100935552a7b6421a8e6dc7d1b6`  
		Last Modified: Thu, 20 Jun 2024 19:04:48 GMT  
		Size: 156.6 MB (156642191 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5483442b5e5e84e7ae2ea9fae5136bd6c4f733ea6148becc7c0957531e3cd47d`  
		Last Modified: Thu, 20 Jun 2024 19:04:37 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:133900c1550c17ba4fc70c056a0119b660f80ef8f03f73d3a2cf42e890cb8136`  
		Last Modified: Thu, 20 Jun 2024 19:04:37 GMT  
		Size: 717.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:add2c4cbb465bc78cc623ec02c3888ff2e460c6ebe9168117650fc0cfb1b81c0`  
		Last Modified: Fri, 21 Jun 2024 07:28:55 GMT  
		Size: 154.7 MB (154683766 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b41fe9389f25f7976681b7ddd585d0a1c2e3e5413ee29b13390fffd4cf5ad36e`  
		Last Modified: Fri, 21 Jun 2024 07:28:50 GMT  
		Size: 152.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6b7c79c3673dd51c0e12c81eed8a6d3021dfca63d927b8256b30cb59dfacd21`  
		Last Modified: Fri, 21 Jun 2024 07:28:50 GMT  
		Size: 1.4 KB (1430 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5e141217c60cf91d6a528f87c6dffc20c1c46425a22dce8cffb37f6d7f17984`  
		Last Modified: Fri, 21 Jun 2024 07:28:52 GMT  
		Size: 34.9 MB (34915039 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85e1939fe5a531c75f405777145a420a6380060fb242a9396f87cbc2d39b81a3`  
		Last Modified: Fri, 21 Jun 2024 07:28:55 GMT  
		Size: 138.1 MB (138063357 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a32e6d46b5661aff8a6ffc9e98accf4c9d2309a98c5f4481d762ec14742fb8c`  
		Last Modified: Fri, 21 Jun 2024 07:28:51 GMT  
		Size: 287.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:jdk-21-and-22-alpine` - unknown; unknown

```console
$ docker pull gradle@sha256:32bbd7c68d310b4e83d4be58ca911c7bf599cc93bb3af616f68e890d19421d05
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3535769 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d8d27af8bfc2cb572734f6f6cd273fbe7ef69ac33823a46f9a56af394173684`

```dockerfile
```

-	Layers:
	-	`sha256:f8e36549ad716f126c8ce5472e5e0c646a92c342af7a8bcc3ab97ea6fdff7b86`  
		Last Modified: Fri, 21 Jun 2024 07:28:51 GMT  
		Size: 3.5 MB (3504580 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5d4d32b7aa8e705b20b9d33c1999da4bea367b0eefdea756236cb921b4907a8d`  
		Last Modified: Fri, 21 Jun 2024 07:28:51 GMT  
		Size: 31.2 KB (31189 bytes)  
		MIME: application/vnd.in-toto+json
