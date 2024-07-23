## `gradle:6-alpine`

```console
$ docker pull gradle@sha256:beb44181845550c853aceda90eb68a9d08d97da3c21d546f71a6debec9c179f1
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `gradle:6-alpine` - linux; amd64

```console
$ docker pull gradle@sha256:903db690c1f8367649ea4411633178bb58724972e135b2e00e0babd5e78a6881
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **302.2 MB (302169375 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a2cc454bb775b1fd476ca7cbb09fe0a97d26ff388af271f7afd3bbeca2204c8`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["gradle"]`

```dockerfile
# Thu, 18 Jan 2024 04:04:59 GMT
ADD file:99093095d62d0421541d882f9ceeddb2981fe701ec0aa9d2c08480712d5fed21 in / 
# Thu, 18 Jan 2024 04:04:59 GMT
CMD ["/bin/sh"]
# Thu, 18 Jan 2024 04:04:59 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 18 Jan 2024 04:04:59 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 18 Jan 2024 04:04:59 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 18 Jan 2024 04:04:59 GMT
RUN set -eux;     apk add --no-cache         fontconfig ttf-dejavu         ca-certificates p11-kit-trust         musl-locales musl-locales-lang         binutils         tzdata     ;     rm -rf /var/cache/apk/* # buildkit
# Thu, 18 Jan 2024 04:04:59 GMT
ENV JAVA_VERSION=jdk-17.0.12+7
# Thu, 18 Jan 2024 04:04:59 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        x86_64)          ESUM='6d274a292a717a6f8d00a3ed0695497405c5c634c27fec1692dd13784f6ff6fa';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jdk_x64_alpine-linux_hotspot_17.0.12_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Thu, 18 Jan 2024 04:04:59 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 18 Jan 2024 04:04:59 GMT
COPY entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 18 Jan 2024 04:04:59 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 18 Jan 2024 04:04:59 GMT
CMD ["jshell"]
# Thu, 18 Jan 2024 04:04:59 GMT
CMD ["gradle"]
# Thu, 18 Jan 2024 04:04:59 GMT
ENV GRADLE_HOME=/opt/gradle
# Thu, 18 Jan 2024 04:04:59 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && addgroup --system --gid 1000 gradle     && adduser --system --ingroup gradle --uid 1000 --shell /bin/ash gradle     && mkdir /home/gradle/.gradle     && chown -R gradle:gradle /home/gradle     && chmod -R o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln -s /home/gradle/.gradle /root/.gradle # buildkit
# Thu, 18 Jan 2024 04:04:59 GMT
VOLUME [/home/gradle/.gradle]
# Thu, 18 Jan 2024 04:04:59 GMT
WORKDIR /home/gradle
# Thu, 18 Jan 2024 04:04:59 GMT
RUN set -o errexit -o nounset     && echo "Installing VCSes"     && apk add --no-cache       git       git-lfs       mercurial       subversion         && echo "Testing VCSes"     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Thu, 18 Jan 2024 04:04:59 GMT
ENV GRADLE_VERSION=6.9.4
# Thu, 18 Jan 2024 04:04:59 GMT
ARG GRADLE_DOWNLOAD_SHA256=3e240228538de9f18772a574e99a0ba959e83d6ef351014381acd9631781389a
# Thu, 18 Jan 2024 04:04:59 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=3e240228538de9f18772a574e99a0ba959e83d6ef351014381acd9631781389a
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum -c -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln -s "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Thu, 18 Jan 2024 04:04:59 GMT
USER gradle
# Thu, 18 Jan 2024 04:04:59 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=3e240228538de9f18772a574e99a0ba959e83d6ef351014381acd9631781389a
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Thu, 18 Jan 2024 04:04:59 GMT
USER root
```

-	Layers:
	-	`sha256:c6a83fedfae6ed8a4f5f7cbb6a7b6f1c1ec3d86fea8cb9e5ba2e5e6673fde9f6`  
		Last Modified: Mon, 22 Jul 2024 22:27:14 GMT  
		Size: 3.6 MB (3622892 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e118bbc909a65083d314d2da5fe1f703619cf9810828b0d739ed6962de633f2`  
		Last Modified: Tue, 23 Jul 2024 01:06:33 GMT  
		Size: 13.0 MB (13019343 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f1ac76beb96a2904db02448518399d50e48e50a297defebe2826e9ee08b2160`  
		Last Modified: Tue, 23 Jul 2024 01:06:42 GMT  
		Size: 144.4 MB (144394579 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:345ef59aa5e3addd013e241224f605436ae9f06f01ba0f31f5fc941fd4431d62`  
		Last Modified: Tue, 23 Jul 2024 01:06:31 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c934f25dfcf9de9f16e47a2fde109ba262dca0c1794676bc143cfc85e06b0035`  
		Last Modified: Tue, 23 Jul 2024 01:06:31 GMT  
		Size: 1.4 KB (1437 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:455fedd9352963dac9125a93706f69c910599af3956565f1fff4dfa676d5d470`  
		Last Modified: Tue, 23 Jul 2024 02:02:15 GMT  
		Size: 1.0 KB (1020 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e16b43a247accebd42ab4ad6c2d826ebb71af3d03bc2019f7807524859f634aa`  
		Last Modified: Tue, 23 Jul 2024 02:02:16 GMT  
		Size: 33.0 MB (33001938 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:567fb2bd0fb7ca4096d8b165bc662977b903b3e4f1758910d88c09afa1073344`  
		Last Modified: Tue, 23 Jul 2024 02:02:16 GMT  
		Size: 107.7 MB (107696704 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fce3d87f643af0e02223744ce3b404a8518b332c78545db025d1dcef3c03102e`  
		Last Modified: Tue, 23 Jul 2024 02:02:15 GMT  
		Size: 431.3 KB (431272 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:6-alpine` - unknown; unknown

```console
$ docker pull gradle@sha256:8ddcb7cd49de042d508401b6e215fa2000060bcae67706e14a4800c5d6577144
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2991112 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d8e0c0f68fa6ad3486b3c24ab56cb9279cbc9b55d3b9e52629e39341b99128d6`

```dockerfile
```

-	Layers:
	-	`sha256:fe3845cf66a523dc0f8f7b4f6781900ffbfc99f005e9c5e30d27e81a05a19737`  
		Last Modified: Tue, 23 Jul 2024 02:02:15 GMT  
		Size: 3.0 MB (2968675 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:60318063f38008fe526ebb160006e2efc2e8aa82946cda38df3310bb0aba8ef9`  
		Last Modified: Tue, 23 Jul 2024 02:02:15 GMT  
		Size: 22.4 KB (22437 bytes)  
		MIME: application/vnd.in-toto+json
