## `gradle:9-jdk17-alpine`

```console
$ docker pull gradle@sha256:793a9fde825fb5afa96c897ed288f025ba4dbbe9a5a8adcca3d28bfea3f3b4bc
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `gradle:9-jdk17-alpine` - linux; amd64

```console
$ docker pull gradle@sha256:0ca82b13fae44af1967e363b505c392af500b63386dab65f397f739c885ed1bf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **351.8 MB (351758915 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ea97e51e7aadc348b833a62b1e169c540d852b349fdca476eab0fc3154f745c`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["gradle"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:04 GMT
ADD alpine-minirootfs-3.23.3-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:04 GMT
CMD ["/bin/sh"]
# Thu, 05 Feb 2026 22:17:14 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 05 Feb 2026 22:17:14 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 05 Feb 2026 22:17:14 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 05 Feb 2026 22:17:14 GMT
RUN set -eux;     apk add --no-cache         fontconfig ttf-dejavu         gnupg         ca-certificates p11-kit-trust         musl-locales musl-locales-lang         binutils         tzdata         coreutils         openssl     ;     rm -rf /var/cache/apk/* # buildkit
# Thu, 05 Feb 2026 22:17:14 GMT
ENV JAVA_VERSION=jdk-17.0.18+8
# Thu, 05 Feb 2026 22:17:20 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        x86_64)          ESUM='3246fb1834d21c22ed717db9f8ba3f07e0f562bbeeebdc44a7499d5eb6df47bc';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jdk_x64_alpine-linux_hotspot_17.0.18_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Thu, 05 Feb 2026 22:17:21 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 05 Feb 2026 22:17:21 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 05 Feb 2026 22:17:21 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 05 Feb 2026 22:17:21 GMT
CMD ["jshell"]
# Fri, 20 Mar 2026 17:11:01 GMT
CMD ["gradle"]
# Fri, 20 Mar 2026 17:11:01 GMT
ENV GRADLE_HOME=/opt/gradle
# Fri, 20 Mar 2026 17:11:01 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && addgroup --system --gid 1000 gradle     && adduser --system --ingroup gradle --uid 1000 --shell /bin/ash gradle     && mkdir /home/gradle/.gradle     && chown -R gradle:gradle /home/gradle     && chmod -R o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln -s /home/gradle/.gradle /root/.gradle # buildkit
# Fri, 20 Mar 2026 17:11:01 GMT
VOLUME [/home/gradle/.gradle]
# Fri, 20 Mar 2026 17:11:01 GMT
WORKDIR /home/gradle
# Fri, 20 Mar 2026 17:11:03 GMT
RUN set -o errexit -o nounset     && apk add --no-cache       make       curl       wget       tar             breezy       py3-tzlocal       git       git-lfs       mercurial       subversion         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Fri, 20 Mar 2026 17:11:03 GMT
ENV GRADLE_VERSION=9.4.1
# Fri, 20 Mar 2026 17:11:03 GMT
ARG GRADLE_DOWNLOAD_SHA256=2ab2958f2a1e51120c326cad6f385153bb11ee93b3c216c5fccebfdfbb7ec6cb
# Fri, 20 Mar 2026 17:11:05 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=2ab2958f2a1e51120c326cad6f385153bb11ee93b3c216c5fccebfdfbb7ec6cb
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum -c -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln -s "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Fri, 20 Mar 2026 17:11:05 GMT
USER gradle
# Fri, 20 Mar 2026 17:11:06 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=2ab2958f2a1e51120c326cad6f385153bb11ee93b3c216c5fccebfdfbb7ec6cb
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --stacktrace --debug --version # buildkit
# Fri, 20 Mar 2026 17:11:06 GMT
USER root
```

-	Layers:
	-	`sha256:589002ba0eaed121a1dbf42f6648f29e5be55d5c8a6ee0f8eaa0285cc21ac153`  
		Last Modified: Wed, 28 Jan 2026 01:18:09 GMT  
		Size: 3.9 MB (3861821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a547da4fe1538a9de970334bfb206793ffde2bd214a847994365c731033eeff`  
		Last Modified: Thu, 05 Feb 2026 22:17:35 GMT  
		Size: 21.3 MB (21315075 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82c540078c28f902907cb8db0fe7898ee78430d17c840a361da6ef7827dba16f`  
		Last Modified: Thu, 05 Feb 2026 22:17:38 GMT  
		Size: 144.8 MB (144762403 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7cd2436f004e3c25b262ab1b7a9ff98f09c80c2bb3359c7e6fc8b4c4364bb969`  
		Last Modified: Thu, 05 Feb 2026 22:17:34 GMT  
		Size: 130.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:946c51efe0fd37b3c13616ceba0f5a7fcc6c82f60c8679d6cf5e8fddd8620fc9`  
		Last Modified: Thu, 05 Feb 2026 22:17:34 GMT  
		Size: 2.3 KB (2280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c9dce065e8cf356024d6a818d95a77f4894edd5197be224c57ea33d4e3d0bf0`  
		Last Modified: Fri, 20 Mar 2026 17:11:22 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df24f901f784d14d012ec8f32869a7fede593988761ada3e2acc282810f9ba68`  
		Last Modified: Fri, 20 Mar 2026 17:11:24 GMT  
		Size: 44.0 MB (43982154 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc042b2dd13e1a0185cec5c49dc7d581339c2ebfe4b80dcece42b44fb740ce52`  
		Last Modified: Fri, 20 Mar 2026 17:11:26 GMT  
		Size: 137.8 MB (137808397 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67dc28cabddf9cbe53ceac48be5de290129c233311c89b58ecb4295a8cf0086a`  
		Last Modified: Fri, 20 Mar 2026 17:11:22 GMT  
		Size: 25.6 KB (25613 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:9-jdk17-alpine` - unknown; unknown

```console
$ docker pull gradle@sha256:b26ae43012b228217aedb5bc5f64bf82090938aa3e3447afd0451605d1da1999
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4710391 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:881d2db6f956ff64265d8dfe790175346f49121c6557e33c13ebad14610c4ba0`

```dockerfile
```

-	Layers:
	-	`sha256:df28c098695027320d3ab5d52c013f2d7051439add7d9cb172a7373b33ffc91d`  
		Last Modified: Fri, 20 Mar 2026 17:11:22 GMT  
		Size: 4.7 MB (4687758 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0ffc3932bbf2036ee584c89ef0301d2e84b5d22096d5d6f30e694c79fc1ffb75`  
		Last Modified: Fri, 20 Mar 2026 17:11:21 GMT  
		Size: 22.6 KB (22633 bytes)  
		MIME: application/vnd.in-toto+json
