## `gradle:jdk21-alpine`

```console
$ docker pull gradle@sha256:c716297fb74b744712744acebe481dd538c0b87c01488639b4590e00caadc2a8
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `gradle:jdk21-alpine` - linux; amd64

```console
$ docker pull gradle@sha256:3a895bcb1cc3bd1e1235befa1a6b32ca8cc72a105a9086ed303f24c37a551df7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **348.2 MB (348212753 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:15f33434fb206cbb356f0fd5c4e619579f1090a4fc4e827f3c203003eca09adb`
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
# Sat, 01 Jun 2024 15:03:05 GMT
CMD ["gradle"]
# Sat, 01 Jun 2024 15:03:05 GMT
ENV GRADLE_HOME=/opt/gradle
# Sat, 01 Jun 2024 15:03:05 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && addgroup --system --gid 1000 gradle     && adduser --system --ingroup gradle --uid 1000 --shell /bin/ash gradle     && mkdir /home/gradle/.gradle     && chown -R gradle:gradle /home/gradle     && chmod -R o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln -s /home/gradle/.gradle /root/.gradle # buildkit
# Sat, 01 Jun 2024 15:03:05 GMT
VOLUME [/home/gradle/.gradle]
# Sat, 01 Jun 2024 15:03:05 GMT
WORKDIR /home/gradle
# Sat, 01 Jun 2024 15:03:05 GMT
RUN set -o errexit -o nounset     && echo "Installing VCSes"     && apk add --no-cache       git       git-lfs       mercurial       subversion         && echo "Testing VCSes"     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Sat, 01 Jun 2024 15:03:05 GMT
ENV GRADLE_VERSION=8.8
# Sat, 01 Jun 2024 15:03:05 GMT
ARG GRADLE_DOWNLOAD_SHA256=a4b4158601f8636cdeeab09bd76afb640030bb5b144aafe261a5e8af027dc612
# Sat, 01 Jun 2024 15:03:05 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=a4b4158601f8636cdeeab09bd76afb640030bb5b144aafe261a5e8af027dc612
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum -c -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln -s "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Sat, 01 Jun 2024 15:03:05 GMT
USER gradle
# Sat, 01 Jun 2024 15:03:05 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=a4b4158601f8636cdeeab09bd76afb640030bb5b144aafe261a5e8af027dc612
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Sat, 01 Jun 2024 15:03:05 GMT
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
	-	`sha256:a4ad9725b231b71b6e95a91fc33e71a90ee623d7ac9cea3222082aad860b6bdd`  
		Last Modified: Mon, 03 Jun 2024 19:00:39 GMT  
		Size: 1.3 KB (1306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c8543971a88146a837c332f3175263b8df4633dc5fc147410fde88c8dbecf9b`  
		Last Modified: Mon, 03 Jun 2024 19:00:40 GMT  
		Size: 34.9 MB (34878835 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ba7aa1dcc2435599bcfa9ae54320c775ccf3f32b65b9f20af3f05bc38610b75`  
		Last Modified: Mon, 03 Jun 2024 19:00:41 GMT  
		Size: 138.1 MB (138063363 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf9a07d66e8e9bda597e60ab0445e3563ef0aed2af3da8e46f0845ed8f7cac20`  
		Last Modified: Mon, 03 Jun 2024 19:00:39 GMT  
		Size: 289.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:jdk21-alpine` - unknown; unknown

```console
$ docker pull gradle@sha256:7b8c78797bf03ea2948d12b639cc6d5054e512462e2d4ce40a6c4820d4b8cf24
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.4 MB (3416576 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:81d32fdb966d45e99ea30a5b27d642d5201facb59a1b316750a2ac39e2d7bfa3`

```dockerfile
```

-	Layers:
	-	`sha256:86795bfddd4b7e59172f38be961e5ec804ea68983009656cda963aca3f268f01`  
		Last Modified: Mon, 03 Jun 2024 19:00:39 GMT  
		Size: 3.4 MB (3395758 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:70a0026261a482d812e9a2bcb225432f71ebd715f671eb54dd0af1c7d6311d2a`  
		Last Modified: Mon, 03 Jun 2024 19:00:39 GMT  
		Size: 20.8 KB (20818 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:jdk21-alpine` - linux; arm64 variant v8

```console
$ docker pull gradle@sha256:25d9815be0d504e62528d54c7101a8ec5f9fc6bdfd38cbbb049c40c0df12dd78
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **346.4 MB (346396857 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c5aa9df73cb544776f7493aef5f29be4a33f15b0115ebaae49945ded56b2d76d`
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
# Sat, 01 Jun 2024 15:03:05 GMT
CMD ["gradle"]
# Sat, 01 Jun 2024 15:03:05 GMT
ENV GRADLE_HOME=/opt/gradle
# Sat, 01 Jun 2024 15:03:05 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && addgroup --system --gid 1000 gradle     && adduser --system --ingroup gradle --uid 1000 --shell /bin/ash gradle     && mkdir /home/gradle/.gradle     && chown -R gradle:gradle /home/gradle     && chmod -R o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln -s /home/gradle/.gradle /root/.gradle # buildkit
# Sat, 01 Jun 2024 15:03:05 GMT
VOLUME [/home/gradle/.gradle]
# Sat, 01 Jun 2024 15:03:05 GMT
WORKDIR /home/gradle
# Sat, 01 Jun 2024 15:03:05 GMT
RUN set -o errexit -o nounset     && echo "Installing VCSes"     && apk add --no-cache       git       git-lfs       mercurial       subversion         && echo "Testing VCSes"     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Sat, 01 Jun 2024 15:03:05 GMT
ENV GRADLE_VERSION=8.8
# Sat, 01 Jun 2024 15:03:05 GMT
ARG GRADLE_DOWNLOAD_SHA256=a4b4158601f8636cdeeab09bd76afb640030bb5b144aafe261a5e8af027dc612
# Sat, 01 Jun 2024 15:03:05 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=a4b4158601f8636cdeeab09bd76afb640030bb5b144aafe261a5e8af027dc612
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum -c -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln -s "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Sat, 01 Jun 2024 15:03:05 GMT
USER gradle
# Sat, 01 Jun 2024 15:03:05 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=a4b4158601f8636cdeeab09bd76afb640030bb5b144aafe261a5e8af027dc612
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Sat, 01 Jun 2024 15:03:05 GMT
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
	-	`sha256:c2bfdf1326002f32fd429307a63de80c656926070e5ffe78441f89d01517e7ef`  
		Last Modified: Tue, 04 Jun 2024 04:20:10 GMT  
		Size: 1.3 KB (1309 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df7cbe776d753b5074738a11bd2fb63bcc6d6e995a3e1a4412c9850a5856f8d8`  
		Last Modified: Tue, 04 Jun 2024 04:20:11 GMT  
		Size: 34.9 MB (34914889 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa764ebaaeaec1f85552fe950dfaa8658fcd4cc901d839d7c8bbc1175125760e`  
		Last Modified: Tue, 04 Jun 2024 04:20:14 GMT  
		Size: 138.1 MB (138063372 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93eeaee4718dc490ce7a4f8e1e93278366ec922312d510a957a059546602451d`  
		Last Modified: Tue, 04 Jun 2024 04:20:10 GMT  
		Size: 291.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:jdk21-alpine` - unknown; unknown

```console
$ docker pull gradle@sha256:5a3069bbc94cafd65e8a612368c03f099214176ae626864def1ef270f99ccc6d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3522297 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:381d23a50bab442d3440fa095000a49c6de7c48bf79e3e1e8a2ba122f416fc28`

```dockerfile
```

-	Layers:
	-	`sha256:b305a0354bfc559766ceca925e4aabc3233e2aacd2469fbbc49802ba53d8a27c`  
		Last Modified: Tue, 04 Jun 2024 04:20:10 GMT  
		Size: 3.5 MB (3501161 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1ae95740fb4a5f7c1ddbd615df21820cd681f3077a3946605c3214e55e3ecc86`  
		Last Modified: Tue, 04 Jun 2024 04:20:10 GMT  
		Size: 21.1 KB (21136 bytes)  
		MIME: application/vnd.in-toto+json
