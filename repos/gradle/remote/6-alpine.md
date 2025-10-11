## `gradle:6-alpine`

```console
$ docker pull gradle@sha256:0d0596fe3de911a9e0704e592f3080ba19d33d1ba3372903b2d15102132c88d7
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `gradle:6-alpine` - linux; amd64

```console
$ docker pull gradle@sha256:d7dd7bef736cf20c8938dea5e6d6af2cc58acaa95fffb77cf674445e0aae1a78
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **314.6 MB (314596480 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8fb08437b1f1da5d3d0a59b9626217af7cfbdb60f921ac29d07c5d6becd89e1d`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["gradle"]`

```dockerfile
# Fri, 01 Aug 2025 11:04:34 GMT
ADD alpine-minirootfs-3.22.2-x86_64.tar.gz / # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
CMD ["/bin/sh"]
# Fri, 01 Aug 2025 11:04:34 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 01 Aug 2025 11:04:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 01 Aug 2025 11:04:34 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 01 Aug 2025 11:04:34 GMT
RUN set -eux;     apk add --no-cache         fontconfig ttf-dejavu         gnupg         ca-certificates p11-kit-trust         musl-locales musl-locales-lang         tzdata         coreutils         openssl     ;     rm -rf /var/cache/apk/* # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
ENV JAVA_VERSION=jdk-11.0.28+6
# Fri, 01 Aug 2025 11:04:34 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        x86_64)          ESUM='7e9e5241d1378d75ae70e9b216d0d51d3aa2e61e187e92e09d117cb613e16ee4';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.28%2B6/OpenJDK11U-jdk_x64_alpine-linux_hotspot_11.0.28_6.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Fri, 01 Aug 2025 11:04:34 GMT
CMD ["jshell"]
# Tue, 23 Sep 2025 15:36:53 GMT
CMD ["gradle"]
# Tue, 23 Sep 2025 15:36:53 GMT
ENV GRADLE_HOME=/opt/gradle
# Tue, 23 Sep 2025 15:36:53 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && addgroup --system --gid 1000 gradle     && adduser --system --ingroup gradle --uid 1000 --shell /bin/ash gradle     && mkdir /home/gradle/.gradle     && chown -R gradle:gradle /home/gradle     && chmod -R o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln -s /home/gradle/.gradle /root/.gradle # buildkit
# Tue, 23 Sep 2025 15:36:53 GMT
VOLUME [/home/gradle/.gradle]
# Tue, 23 Sep 2025 15:36:53 GMT
WORKDIR /home/gradle
# Tue, 23 Sep 2025 15:36:53 GMT
RUN set -o errexit -o nounset     && apk add --no-cache       curl       make             breezy       py3-tzlocal       git       git-lfs       mercurial       subversion         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Tue, 23 Sep 2025 15:36:53 GMT
ENV GRADLE_VERSION=6.9.4
# Tue, 23 Sep 2025 15:36:53 GMT
ARG GRADLE_DOWNLOAD_SHA256=3e240228538de9f18772a574e99a0ba959e83d6ef351014381acd9631781389a
# Tue, 23 Sep 2025 15:36:53 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=3e240228538de9f18772a574e99a0ba959e83d6ef351014381acd9631781389a
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum -c -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln -s "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Tue, 23 Sep 2025 15:36:53 GMT
USER gradle
# Tue, 23 Sep 2025 15:36:53 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=3e240228538de9f18772a574e99a0ba959e83d6ef351014381acd9631781389a
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Tue, 23 Sep 2025 15:36:53 GMT
USER root
```

-	Layers:
	-	`sha256:2d35ebdb57d9971fea0cac1582aa78935adf8058b2cc32db163c98822e5dfa1b`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 3.8 MB (3802452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fc9e5a155a7ff06c0190ea62107ab1a927e87f603ebbf7a293a0f96aa156ee7`  
		Last Modified: Wed, 08 Oct 2025 23:01:38 GMT  
		Size: 16.3 MB (16289659 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09f7cadbd3f978eaee4ce9a81527bb2dced7d116e33e7e96e77af514781073ee`  
		Last Modified: Wed, 08 Oct 2025 23:39:17 GMT  
		Size: 140.8 MB (140841635 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe80d87e1e391e254ecece5c43911c68edfddd2bd6a7582367fda36de120a1f7`  
		Last Modified: Wed, 08 Oct 2025 23:02:06 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80e292129e0fa0f3fd5d4c68c90a9ac89b092e4768cf7bdef779596a5f99c513`  
		Last Modified: Wed, 08 Oct 2025 23:02:06 GMT  
		Size: 2.3 KB (2280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0fe2abba5940734562248f47bdb348f938bcaa8b6a569380d852923ccdae5497`  
		Last Modified: Wed, 08 Oct 2025 23:40:03 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:baab94517bea7647a4fb5c34f6d405b66b73d7ba75b74c58d85302752d84ed75`  
		Last Modified: Wed, 08 Oct 2025 23:40:11 GMT  
		Size: 45.5 MB (45531328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f538f01262abdf300641cbfb3c089cb45cbe57572e7be2539f46e84dac61261`  
		Last Modified: Wed, 08 Oct 2025 23:40:31 GMT  
		Size: 107.7 MB (107696675 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39098c3981aff387a8e0c9f2b5813ec84a3610ccec2c00997c8764e1488657ed`  
		Last Modified: Wed, 08 Oct 2025 23:40:04 GMT  
		Size: 431.3 KB (431280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:6-alpine` - unknown; unknown

```console
$ docker pull gradle@sha256:dada92fd67ba80f7ed2cf726df327bb65b35067fa91b7710ea9e944580b6a9b9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4528892 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fd61ae8fcd084b868d8f1362a13a17969975e69489c59b67dd5a9405f6f329e8`

```dockerfile
```

-	Layers:
	-	`sha256:9983af41d8ae9860692cc1073706f8bb0c2e36b99fe63f87c5c31ad9d90e9d28`  
		Last Modified: Thu, 09 Oct 2025 02:17:19 GMT  
		Size: 4.5 MB (4504847 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:437e0ff7a70091006542ea6dddc70bbe20b5146cb8c49804e041c0629003cb48`  
		Last Modified: Thu, 09 Oct 2025 02:17:20 GMT  
		Size: 24.0 KB (24045 bytes)  
		MIME: application/vnd.in-toto+json
