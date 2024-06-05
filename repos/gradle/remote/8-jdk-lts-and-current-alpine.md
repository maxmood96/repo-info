## `gradle:8-jdk-lts-and-current-alpine`

```console
$ docker pull gradle@sha256:2b39e1c27816e1b1a9dd06d225e8d4537985c114ba3445179b20e10b5cc003db
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `gradle:8-jdk-lts-and-current-alpine` - linux; amd64

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

### `gradle:8-jdk-lts-and-current-alpine` - unknown; unknown

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

### `gradle:8-jdk-lts-and-current-alpine` - linux; arm64 variant v8

```console
$ docker pull gradle@sha256:6bf2c0546b2b23263660f6ebda914ba594f6a0c619cb94477a9372a080e28cd5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **501.1 MB (501080770 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e73c1fa013347383bdd92a138b11ef437114532a7db92fae3ee9127414aea6dc`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["gradle"]`

```dockerfile
# Fri, 26 Jan 2024 23:44:47 GMT
ADD file:d0764a717d1e9d0aff3fa84779b11bfa0afe4430dcb6b46d965b209167639ba0 in / 
# Fri, 26 Jan 2024 23:44:47 GMT
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
	-	`sha256:bca4290a96390d7a6fc6f2f9929370d06f8dfcacba591c76e3d5c5044e7f420c`  
		Last Modified: Fri, 26 Jan 2024 23:45:19 GMT  
		Size: 3.3 MB (3347715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38eb0c9d7c04691eff93919fd977269a8104369a10cadd69b1a9b35aba5b9085`  
		Last Modified: Thu, 28 Mar 2024 00:54:36 GMT  
		Size: 13.4 MB (13426226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14913aa90dd272383828ac4d0e86076a10938413131e5ee6e93ee4e6648d0ce4`  
		Last Modified: Wed, 24 Apr 2024 18:00:31 GMT  
		Size: 156.6 MB (156642116 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1580f0bf3a1e75eafc1948692da9e627918593541852652450c41c2321f95cfe`  
		Last Modified: Wed, 24 Apr 2024 18:00:20 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a0e74802a9ebeb8466444d95d80e5dd58cc73053c763de1f6d93af5c2cef10c`  
		Last Modified: Wed, 24 Apr 2024 18:00:20 GMT  
		Size: 717.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53f366960c4bf1e81d19128d567321f1936c002c1dac3ea4975b9502c8c74eec`  
		Last Modified: Tue, 04 Jun 2024 06:43:25 GMT  
		Size: 154.7 MB (154683749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6077dfd0bd2562320c2c84a0775bd6f8e22e4567b859e5eacfe4944abc61669e`  
		Last Modified: Tue, 04 Jun 2024 06:43:22 GMT  
		Size: 153.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2d66ac1050d2890d9d2279b8fd59c681ddb49e74a999730c29331b1de8b0d3d`  
		Last Modified: Tue, 04 Jun 2024 06:43:22 GMT  
		Size: 1.4 KB (1432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e123f452cabe501367a33f4a4121e30f5b11b55f32a3779cc214d6ad55f632dd`  
		Last Modified: Tue, 04 Jun 2024 06:43:23 GMT  
		Size: 34.9 MB (34914789 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2750a5ed3992cfa5457623843ccbf819f6b328451eef4a49725d12859f155d28`  
		Last Modified: Tue, 04 Jun 2024 06:43:26 GMT  
		Size: 138.1 MB (138063364 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f5cfa82aea968206668ffc3530bc4c96a0dc8d4e22da6d759089bad363563b2`  
		Last Modified: Tue, 04 Jun 2024 06:43:23 GMT  
		Size: 287.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:8-jdk-lts-and-current-alpine` - unknown; unknown

```console
$ docker pull gradle@sha256:c6e606ed6b7b9b53dc481067faf453a3a96f33a772bb73107990f55bf73821ef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3535831 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f2a2c0c5632f0950360ca50fd1683cdc2b23ae55ffe10c75cdeefab2d2d0a6e7`

```dockerfile
```

-	Layers:
	-	`sha256:411c42b17f2c9a49af93be5b1e8bd729d65510aab33656101f406916a1a67f80`  
		Last Modified: Wed, 05 Jun 2024 18:37:38 GMT  
		Size: 3.5 MB (3505520 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1ad55d6d1539f8953e98807dd622e827e2a545d10d2d102382ae2603e8567799`  
		Last Modified: Wed, 05 Jun 2024 18:37:38 GMT  
		Size: 30.3 KB (30311 bytes)  
		MIME: application/vnd.in-toto+json
