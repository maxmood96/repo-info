## `gradle:jdk17-alpine`

```console
$ docker pull gradle@sha256:6eadb94314dc30e1adafd8d79eea3353f3c36508a36f5e4741c5fe760cf933e8
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `gradle:jdk17-alpine` - linux; amd64

```console
$ docker pull gradle@sha256:6fec4f82d4abddd9f0050342632f635ffbfe56ea0927368ff8cf1b47023a2cf5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **354.2 MB (354195627 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c44859286c410fe0864c6ca0ecc4488ec014fb7d3937bc938ca4a9b545ff41bc`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["gradle"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:40 GMT
ADD alpine-minirootfs-3.23.4-x86_64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:40 GMT
CMD ["/bin/sh"]
# Wed, 15 Apr 2026 20:33:20 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 15 Apr 2026 20:33:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 15 Apr 2026 20:33:20 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 15 Apr 2026 20:33:20 GMT
RUN set -eux;     apk add --no-cache         fontconfig ttf-dejavu         gnupg         ca-certificates p11-kit-trust         musl-locales musl-locales-lang         binutils         tzdata         coreutils         openssl     ;     rm -rf /var/cache/apk/* # buildkit
# Wed, 15 Apr 2026 20:33:20 GMT
ENV JAVA_VERSION=jdk-17.0.18+8
# Wed, 15 Apr 2026 20:33:28 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        x86_64)          ESUM='3246fb1834d21c22ed717db9f8ba3f07e0f562bbeeebdc44a7499d5eb6df47bc';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jdk_x64_alpine-linux_hotspot_17.0.18_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Wed, 15 Apr 2026 20:33:29 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 15 Apr 2026 20:33:29 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 15 Apr 2026 20:33:29 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 15 Apr 2026 20:33:29 GMT
CMD ["jshell"]
# Tue, 28 Apr 2026 23:29:49 GMT
CMD ["gradle"]
# Tue, 28 Apr 2026 23:29:49 GMT
ENV GRADLE_HOME=/opt/gradle
# Tue, 28 Apr 2026 23:29:49 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && addgroup --system --gid 1000 gradle     && adduser --system --ingroup gradle --uid 1000 --shell /bin/ash gradle     && mkdir /home/gradle/.gradle     && chown -R gradle:gradle /home/gradle     && chmod -R o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln -s /home/gradle/.gradle /root/.gradle # buildkit
# Tue, 28 Apr 2026 23:29:49 GMT
VOLUME [/home/gradle/.gradle]
# Tue, 28 Apr 2026 23:29:49 GMT
WORKDIR /home/gradle
# Tue, 28 Apr 2026 23:29:51 GMT
RUN set -o errexit -o nounset     && apk add --no-cache       make       curl       wget       tar             breezy       py3-tzlocal       git       git-lfs       mercurial       subversion         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Tue, 28 Apr 2026 23:29:51 GMT
ENV GRADLE_VERSION=9.5.0
# Tue, 28 Apr 2026 23:29:51 GMT
ARG GRADLE_DOWNLOAD_SHA256=553c78f50dafcd54d65b9a444649057857469edf836431389695608536d6b746
# Tue, 28 Apr 2026 23:29:53 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=553c78f50dafcd54d65b9a444649057857469edf836431389695608536d6b746
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum -c -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln -s "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Tue, 28 Apr 2026 23:29:53 GMT
USER gradle
# Tue, 28 Apr 2026 23:29:54 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=553c78f50dafcd54d65b9a444649057857469edf836431389695608536d6b746
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --stacktrace --debug --version # buildkit
# Tue, 28 Apr 2026 23:29:54 GMT
USER root
```

-	Layers:
	-	`sha256:6a0ac1617861a677b045b7ff88545213ec31c0ff08763195a70a4a5adda577bb`  
		Last Modified: Wed, 15 Apr 2026 20:01:46 GMT  
		Size: 3.9 MB (3864189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7e18feb881252411e8481c736f2ef1a8f450f8e9fa28a7834b4cd096ffcc796`  
		Last Modified: Wed, 15 Apr 2026 20:33:44 GMT  
		Size: 21.3 MB (21315838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e642fade5205f4033b5c781cc2d6a0fcf038d2f82370ae6789690d81c2cd9b8d`  
		Last Modified: Wed, 15 Apr 2026 20:33:46 GMT  
		Size: 144.8 MB (144762385 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bec5268d796984af3be20bf1cbadc4a60b0a45eff14ccfda5cb11252b8154707`  
		Last Modified: Wed, 15 Apr 2026 20:33:43 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09b25f7d051ea8167c6952fccc5be5ccf7e6b821446064bb49ec9e2c3e1c80b5`  
		Last Modified: Wed, 15 Apr 2026 20:33:43 GMT  
		Size: 2.3 KB (2280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b7b2ce88af51c05092425e189eff899565d9c41e2438e26f166be4170fe2e14`  
		Last Modified: Tue, 28 Apr 2026 23:30:11 GMT  
		Size: 1.0 KB (1008 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ba70ea2a6f6d6e3317ef533d173fd4e104c1f1f83932004c157330ff2e060d6`  
		Last Modified: Tue, 28 Apr 2026 23:30:13 GMT  
		Size: 44.0 MB (43987710 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8204503b54b60f69c77524b504946e195e4b97b1912776685632d0643bdc4cb8`  
		Last Modified: Tue, 28 Apr 2026 23:30:15 GMT  
		Size: 140.2 MB (140236442 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a594f986756550abb0196cc7d87acc36f6d168b5152c74daa06b5d1711251aa0`  
		Last Modified: Tue, 28 Apr 2026 23:30:11 GMT  
		Size: 25.6 KB (25615 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:jdk17-alpine` - unknown; unknown

```console
$ docker pull gradle@sha256:d7a0eef5e6336518efc09e41dc548c74ae012939de8bbf513929be3c01e3defd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4737346 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b06d5d28c31bfeb062b15e4492a5845332dd61730c575e3dec9daf35ab762e2b`

```dockerfile
```

-	Layers:
	-	`sha256:24cb1255b18857796055cf9a8b02ccf2e7fd3121434e517334f488b1c135297c`  
		Last Modified: Tue, 28 Apr 2026 23:30:11 GMT  
		Size: 4.7 MB (4714712 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c7ea738fc319eb99e7874ba1b304f9e133b5d96d32c96453ac485520e271724e`  
		Last Modified: Tue, 28 Apr 2026 23:30:11 GMT  
		Size: 22.6 KB (22634 bytes)  
		MIME: application/vnd.in-toto+json
