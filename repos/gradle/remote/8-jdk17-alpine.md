## `gradle:8-jdk17-alpine`

```console
$ docker pull gradle@sha256:8c2725fddb8f01f8aeadc23708c124614b6b64a3be6434be36de926af1f39f3e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `gradle:8-jdk17-alpine` - linux; amd64

```console
$ docker pull gradle@sha256:8e3720caea00b173ba285875d8a8e6aa396db4db4a09b1860c177b5f12caa062
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **350.9 MB (350949435 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f1e8b3c5c73b956f644c4a54332cfa3951b9e3fc96b81149e76271455c789aaa`
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
# Wed, 15 Apr 2026 21:31:20 GMT
CMD ["gradle"]
# Wed, 15 Apr 2026 21:31:20 GMT
ENV GRADLE_HOME=/opt/gradle
# Wed, 15 Apr 2026 21:31:20 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && addgroup --system --gid 1000 gradle     && adduser --system --ingroup gradle --uid 1000 --shell /bin/ash gradle     && mkdir /home/gradle/.gradle     && chown -R gradle:gradle /home/gradle     && chmod -R o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln -s /home/gradle/.gradle /root/.gradle # buildkit
# Wed, 15 Apr 2026 21:31:20 GMT
VOLUME [/home/gradle/.gradle]
# Wed, 15 Apr 2026 21:31:20 GMT
WORKDIR /home/gradle
# Wed, 15 Apr 2026 21:31:22 GMT
RUN set -o errexit -o nounset     && apk add --no-cache       curl       make             breezy       py3-tzlocal       git       git-lfs       mercurial       subversion         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Wed, 15 Apr 2026 21:31:22 GMT
ENV GRADLE_VERSION=8.14.4
# Wed, 15 Apr 2026 21:31:22 GMT
ARG GRADLE_DOWNLOAD_SHA256=f1771298a70f6db5a29daf62378c4e18a17fc33c9ba6b14362e0cdf40610380d
# Wed, 15 Apr 2026 21:31:25 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=f1771298a70f6db5a29daf62378c4e18a17fc33c9ba6b14362e0cdf40610380d
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum -c -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln -s "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Wed, 15 Apr 2026 21:31:25 GMT
USER gradle
# Wed, 15 Apr 2026 21:31:25 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=f1771298a70f6db5a29daf62378c4e18a17fc33c9ba6b14362e0cdf40610380d
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Wed, 15 Apr 2026 21:31:25 GMT
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
	-	`sha256:e5dc7f2745b25cd20b6a54b3ad61a9fb1d46e28c1ec0d03f25ef825a2bdb5e8b`  
		Last Modified: Wed, 15 Apr 2026 21:31:41 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71a4b5995e37de0f0a24e28f629ab3bb1690726008c2583def4e9a89d4efa955`  
		Last Modified: Wed, 15 Apr 2026 21:31:44 GMT  
		Size: 43.6 MB (43560543 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ac113ac2de40e99f8125134d67deef25b9b50c8b4a359d871224706a3a03dda`  
		Last Modified: Wed, 15 Apr 2026 21:31:46 GMT  
		Size: 137.4 MB (137388129 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1483048f7434b4880d77216ae2d2970e9e4b2023bef157c3816d86dc5ede78fe`  
		Last Modified: Wed, 15 Apr 2026 21:31:42 GMT  
		Size: 54.9 KB (54901 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:8-jdk17-alpine` - unknown; unknown

```console
$ docker pull gradle@sha256:87d2f86a0c33c1dbaafee6f9ccd380fe810b146c5d2801a836107f50b4f1d784
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4717462 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cab31465c0dad57b907c358b01173b07a879f6b82be0c4cbdc5421ca639bc46c`

```dockerfile
```

-	Layers:
	-	`sha256:8e585bb72a873eb499573d6dd69c6d20033c0174c3b80ff7dd01f94cf3cbbe5c`  
		Last Modified: Wed, 15 Apr 2026 21:31:42 GMT  
		Size: 4.7 MB (4695314 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4fd77140a11318278cb12142006fe469bf5716f6492ab6445a37fc49eda2da8e`  
		Last Modified: Wed, 15 Apr 2026 21:31:41 GMT  
		Size: 22.1 KB (22148 bytes)  
		MIME: application/vnd.in-toto+json
