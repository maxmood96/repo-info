## `gradle:8-jdk11-alpine`

```console
$ docker pull gradle@sha256:4294763d373353b18eda14911ea4666bd692672759dfa4b9d6475f11db0d6a6f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `gradle:8-jdk11-alpine` - linux; amd64

```console
$ docker pull gradle@sha256:8322ad4daff726c3ad9d2481b4d8e2ae4273d83a32e3563d05c5a8ac1c0d8ef8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **324.9 MB (324884025 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f71c44957e98002686b4bb621b6bfdb128922855e6e57f01bedbc496f54ab8c2`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["gradle"]`

```dockerfile
# Mon, 22 Jul 2024 22:26:43 GMT
ADD file:99093095d62d0421541d882f9ceeddb2981fe701ec0aa9d2c08480712d5fed21 in / 
# Mon, 22 Jul 2024 22:26:43 GMT
CMD ["/bin/sh"]
# Thu, 15 Aug 2024 06:00:50 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 15 Aug 2024 06:00:50 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 15 Aug 2024 06:00:50 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 15 Aug 2024 06:00:50 GMT
RUN set -eux;     apk add --no-cache         fontconfig ttf-dejavu         ca-certificates p11-kit-trust         musl-locales musl-locales-lang         tzdata         coreutils         openssl     ;     rm -rf /var/cache/apk/* # buildkit
# Thu, 15 Aug 2024 06:00:50 GMT
ENV JAVA_VERSION=jdk-11.0.24+8
# Thu, 15 Aug 2024 06:00:50 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        x86_64)          ESUM='ae988c72eeb2d78bb729a3387601ce0ea84305734ebdbe95d276f39952a8e019';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jdk_x64_alpine-linux_hotspot_11.0.24_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Thu, 15 Aug 2024 06:00:50 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 15 Aug 2024 06:00:50 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 15 Aug 2024 06:00:50 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 15 Aug 2024 06:00:50 GMT
CMD ["jshell"]
# Thu, 15 Aug 2024 06:00:50 GMT
CMD ["gradle"]
# Thu, 15 Aug 2024 06:00:50 GMT
ENV GRADLE_HOME=/opt/gradle
# Thu, 15 Aug 2024 06:00:50 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && addgroup --system --gid 1000 gradle     && adduser --system --ingroup gradle --uid 1000 --shell /bin/ash gradle     && mkdir /home/gradle/.gradle     && chown -R gradle:gradle /home/gradle     && chmod -R o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln -s /home/gradle/.gradle /root/.gradle # buildkit
# Thu, 15 Aug 2024 06:00:50 GMT
VOLUME [/home/gradle/.gradle]
# Thu, 15 Aug 2024 06:00:50 GMT
WORKDIR /home/gradle
# Thu, 15 Aug 2024 06:00:50 GMT
RUN set -o errexit -o nounset     && echo "Installing VCSes"     && apk add --no-cache       git       git-lfs       mercurial       subversion         && echo "Testing VCSes"     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Thu, 15 Aug 2024 06:00:50 GMT
ENV GRADLE_VERSION=8.10
# Thu, 15 Aug 2024 06:00:50 GMT
ARG GRADLE_DOWNLOAD_SHA256=5b9c5eb3f9fc2c94abaea57d90bd78747ca117ddbbf96c859d3741181a12bf2a
# Thu, 15 Aug 2024 06:00:50 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=5b9c5eb3f9fc2c94abaea57d90bd78747ca117ddbbf96c859d3741181a12bf2a
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum -c -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln -s "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Thu, 15 Aug 2024 06:00:50 GMT
USER gradle
# Thu, 15 Aug 2024 06:00:50 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=5b9c5eb3f9fc2c94abaea57d90bd78747ca117ddbbf96c859d3741181a12bf2a
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Thu, 15 Aug 2024 06:00:50 GMT
USER root
```

-	Layers:
	-	`sha256:c6a83fedfae6ed8a4f5f7cbb6a7b6f1c1ec3d86fea8cb9e5ba2e5e6673fde9f6`  
		Last Modified: Mon, 22 Jul 2024 22:27:14 GMT  
		Size: 3.6 MB (3622892 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6dff7dc6fc2858af0a16833a15a63741d58d895a9d1a9a2de411e9921a0de0dd`  
		Last Modified: Thu, 25 Jul 2024 17:25:18 GMT  
		Size: 9.4 MB (9394889 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef2a3080f55a0df9191af7a0a5db0289f1fb254d52b39af6fa1d3089b3292284`  
		Last Modified: Thu, 25 Jul 2024 17:28:06 GMT  
		Size: 140.7 MB (140723653 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:157f0a6d035e90e7a6e9bceb73fa7e2a378d545b4cc559693c03a0d4b3526f34`  
		Last Modified: Thu, 25 Jul 2024 17:27:55 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c320391631e63b2725b0a72a09db50ab50c01d0ec0d40fe8ec6cbbe16c93286c`  
		Last Modified: Fri, 23 Aug 2024 19:25:34 GMT  
		Size: 2.1 KB (2106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86b18a4c3b607b77f438fe947c2efb3070113c8d8360cfae70c99368bc71d2a2`  
		Last Modified: Fri, 23 Aug 2024 20:05:20 GMT  
		Size: 1.0 KB (1023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3cfd1130c7d4dc91e4dcc6ed873aa51a4bc5c010acc410cddc3b12ad9dcdb9d`  
		Last Modified: Fri, 23 Aug 2024 20:05:21 GMT  
		Size: 34.4 MB (34410296 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c36fac16c5a461da5fba69181c0721bc78e9f24b5a0f18588d1a006c6417e92`  
		Last Modified: Fri, 23 Aug 2024 20:05:22 GMT  
		Size: 136.7 MB (136728687 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a1f409da954314a81d81185710fc505638ebb05d5ff68d721709cb38da3d3af`  
		Last Modified: Fri, 23 Aug 2024 20:05:20 GMT  
		Size: 289.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:8-jdk11-alpine` - unknown; unknown

```console
$ docker pull gradle@sha256:cf0bce1de3a7bf2512dfa1545de65f86a4db77d8f0c4c2850f81251bb9a87a5f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (3001721 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b1def94aa5c000df94bebf91580f69f395edbc396737c29668d03c024aa7413d`

```dockerfile
```

-	Layers:
	-	`sha256:d16fc31e92b660987cab054b9dcb7bb720e6860597521f89c73ad5ad507a8e92`  
		Last Modified: Fri, 23 Aug 2024 20:05:20 GMT  
		Size: 3.0 MB (2980840 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2eea623dd3cfd8a55572def73fe60e3887203708ab83df383fad724dc32843d5`  
		Last Modified: Fri, 23 Aug 2024 20:05:20 GMT  
		Size: 20.9 KB (20881 bytes)  
		MIME: application/vnd.in-toto+json
