## `gradle:8-jdk17-alpine`

```console
$ docker pull gradle@sha256:85c75bdba8f9c9e41ce48e342e70ee932219b5af5c2aeac0ca0564855513da22
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `gradle:8-jdk17-alpine` - linux; amd64

```console
$ docker pull gradle@sha256:e6bedf4d95741785905fdc5edd01d4a70ea559deb5d7602a18115e5568f1403f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **331.8 MB (331804510 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7722e6d6ed7780a0cb3d4c2c4b8b58a57aa9b58b58c405af2de29a11396979e7`
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
RUN set -eux;     apk add --no-cache         fontconfig ttf-dejavu         ca-certificates p11-kit-trust         musl-locales musl-locales-lang         binutils         tzdata         coreutils         openssl     ;     rm -rf /var/cache/apk/* # buildkit
# Thu, 15 Aug 2024 06:00:50 GMT
ENV JAVA_VERSION=jdk-17.0.12+7
# Thu, 15 Aug 2024 06:00:50 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        x86_64)          ESUM='6d274a292a717a6f8d00a3ed0695497405c5c634c27fec1692dd13784f6ff6fa';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jdk_x64_alpine-linux_hotspot_17.0.12_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
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
	-	`sha256:479e64820c602a6421582ff22341d66b5c6938bee2115d203f3d03147a89505e`  
		Last Modified: Thu, 25 Jul 2024 17:29:26 GMT  
		Size: 14.0 MB (14039136 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e384a19a9b0cde9f53fc5c79a581f80b1606cb9b0c477b8019b1716ffe026fe`  
		Last Modified: Thu, 25 Jul 2024 17:29:36 GMT  
		Size: 144.4 MB (144394552 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ed71e81fa34c6c2e7902182aaf9da971d499b0e58d2dfcc2c789535bc6768e0`  
		Last Modified: Thu, 25 Jul 2024 17:29:24 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7beb93379603195c1cd0e0fa2dfd4b31ab5a9580ed4dd4cc301f4ca12c31c1ff`  
		Last Modified: Fri, 23 Aug 2024 19:26:45 GMT  
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
	-	`sha256:1c4c3ae4ccce28d81f42260c1beb8403f9f2d4f582d889e2ad2ce66a6827489f`  
		Last Modified: Fri, 23 Aug 2024 20:05:21 GMT  
		Size: 33.0 MB (33015879 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e11db3f56548d9e4eebf2b8baecc73dd77aac0ce309d10870d13f9a61a282f2`  
		Last Modified: Fri, 23 Aug 2024 20:05:23 GMT  
		Size: 136.7 MB (136728440 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38f29adc50d6f36d8f647da8513936fa67bfd488023be3124b9174fd36f9a95b`  
		Last Modified: Fri, 23 Aug 2024 20:05:21 GMT  
		Size: 291.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:8-jdk17-alpine` - unknown; unknown

```console
$ docker pull gradle@sha256:afce5fb2a6b50f80c61b9d095d6943d4a59181134eb42413465000dc29ad12be
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3091880 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:60511e0d41006498e0f360cf6901feb940efddf044ef60b2c794f7a8a21ba4e2`

```dockerfile
```

-	Layers:
	-	`sha256:aa8b9eb9ed67e892dfffef0cd38da4bae296e244a45fcf2818af0ae310abcd4e`  
		Last Modified: Fri, 23 Aug 2024 20:05:21 GMT  
		Size: 3.1 MB (3070357 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:94bd32489a2229d349bba9040d090a5cfc2c6273100681165ecd19521b336344`  
		Last Modified: Fri, 23 Aug 2024 20:05:21 GMT  
		Size: 21.5 KB (21523 bytes)  
		MIME: application/vnd.in-toto+json
