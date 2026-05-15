## `gradle:9-jdk-25-and-26-alpine`

```console
$ docker pull gradle@sha256:e2310db1529ba6bc8a7f5796c4b2156313bb95d2aa6ff572e4305af513b5c026
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `gradle:9-jdk-25-and-26-alpine` - linux; amd64

```console
$ docker pull gradle@sha256:57202174d4669fae56cbb76e726ecc7f2c93838e8064688eb6fb0e890207effe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **389.7 MB (389691049 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:464f34539005aca9c4f47f726b2467535bf2c7808f3d6542297f42dea2645f3f`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["gradle"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:40 GMT
ADD alpine-minirootfs-3.23.4-x86_64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:40 GMT
CMD ["/bin/sh"]
# Thu, 30 Apr 2026 23:26:24 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 30 Apr 2026 23:26:24 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 30 Apr 2026 23:26:24 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 30 Apr 2026 23:26:24 GMT
RUN set -eux;     apk add --no-cache         fontconfig ttf-dejavu         ca-certificates p11-kit-trust         musl-locales musl-locales-lang         binutils         tzdata         coreutils         openssl     ;     rm -rf /var/cache/apk/* # buildkit
# Thu, 30 Apr 2026 23:26:24 GMT
ENV JAVA_VERSION=jdk-25.0.3+9
# Thu, 30 Apr 2026 23:26:31 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        aarch64)          ESUM='6ed368e93049d3b188c045fce0b20953bbea92fe0614dbbf4d3fd8daad7be3b2';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.3%2B9/OpenJDK25U-jdk_aarch64_alpine-linux_hotspot_25.0.3_9.tar.gz';          ;;        x86_64)          ESUM='51c2415b370aac7c3796b0c4663c8fcf91bc22d76f03df95b25fa5667cb5fdd8';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.3%2B9/OpenJDK25U-jdk_x64_alpine-linux_hotspot_25.0.3_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     apk add --no-cache --virtual .fetch-deps gnupg;     wget -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     apk del --no-network .fetch-deps; # buildkit
# Thu, 30 Apr 2026 23:26:33 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 30 Apr 2026 23:26:33 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 30 Apr 2026 23:26:33 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 30 Apr 2026 23:26:33 GMT
CMD ["jshell"]
# Fri, 15 May 2026 20:35:42 GMT
COPY /opt/java/openjdk /opt/java/openjdk26 # buildkit
# Fri, 15 May 2026 20:35:42 GMT
RUN set -o errexit -o nounset     && ln -s /opt/java/openjdk /opt/java/openjdk25 # buildkit
# Fri, 15 May 2026 20:35:43 GMT
ENV JAVA_LTS_HOME=/opt/java/openjdk25
# Fri, 15 May 2026 20:35:43 GMT
ENV JAVA_CURRENT_HOME=/opt/java/openjdk26
# Fri, 15 May 2026 20:35:43 GMT
CMD ["gradle"]
# Fri, 15 May 2026 20:35:43 GMT
ENV GRADLE_HOME=/opt/gradle
# Fri, 15 May 2026 20:35:43 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && addgroup --system --gid 1000 gradle     && adduser --system --ingroup gradle --uid 1000 --shell /bin/ash gradle     && mkdir /home/gradle/.gradle     && chown -R gradle:gradle /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln -s /home/gradle/.gradle /root/.gradle       && echo "Ensuring Gradle detects installed JDKs"    && echo "org.gradle.java.installations.auto-detect=false" > /home/gradle/.gradle/gradle.properties    && echo "org.gradle.java.installations.auto-download=false" >> /home/gradle/.gradle/gradle.properties    && echo "org.gradle.java.installations.fromEnv=JAVA_LTS_HOME,JAVA_CURRENT_HOME" >> /home/gradle/.gradle/gradle.properties # buildkit
# Fri, 15 May 2026 20:35:43 GMT
VOLUME [/home/gradle/.gradle]
# Fri, 15 May 2026 20:35:43 GMT
WORKDIR /home/gradle
# Fri, 15 May 2026 20:35:45 GMT
RUN set -o errexit -o nounset     && apk add --no-cache       make       curl       wget       tar             breezy       py3-tzlocal       git       git-lfs       mercurial       subversion         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Fri, 15 May 2026 20:35:45 GMT
ENV GRADLE_VERSION=9.5.1
# Fri, 15 May 2026 20:35:45 GMT
ARG GRADLE_DOWNLOAD_SHA256=bafc141b619ad6350fd975fc903156dd5c151998cc8b058e8c1044ab5f7b031f
# Fri, 15 May 2026 20:35:47 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=bafc141b619ad6350fd975fc903156dd5c151998cc8b058e8c1044ab5f7b031f
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum -c -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln -s "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Fri, 15 May 2026 20:35:47 GMT
USER gradle
# Fri, 15 May 2026 20:35:47 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=bafc141b619ad6350fd975fc903156dd5c151998cc8b058e8c1044ab5f7b031f
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --stacktrace --debug --version # buildkit
# Fri, 15 May 2026 20:35:47 GMT
USER root
```

-	Layers:
	-	`sha256:6a0ac1617861a677b045b7ff88545213ec31c0ff08763195a70a4a5adda577bb`  
		Last Modified: Wed, 15 Apr 2026 20:01:46 GMT  
		Size: 3.9 MB (3864189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbcd71e97d819f54817ede73936d3ba8e0e56a42c8dec6fffa3dcf0a5f0b4cd7`  
		Last Modified: Thu, 30 Apr 2026 23:26:47 GMT  
		Size: 14.3 MB (14307043 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:069decb9687a1d107c70cc1f3b39e28717aee5b68017f656ac233f17fabf3d80`  
		Last Modified: Thu, 30 Apr 2026 23:26:49 GMT  
		Size: 91.6 MB (91623532 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18b72908a207a549bc818ba092166eeb02f65c17134d611b1f98600452d5217e`  
		Last Modified: Thu, 30 Apr 2026 23:26:47 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2a11818993d9767c2a1269e3b83ea425a7dbc1d260bf8e8e208ef3eb39c4234`  
		Last Modified: Thu, 30 Apr 2026 23:26:47 GMT  
		Size: 2.3 KB (2281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f1bfb7c6d31877976a77593def38cadeb8b9047f32b15c428c5b16c131c3e91`  
		Last Modified: Fri, 15 May 2026 20:36:13 GMT  
		Size: 93.7 MB (93676449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f735d486ea3bf82658f90328598ac5de3be62158dd9f898d651ef7228342460`  
		Last Modified: Fri, 15 May 2026 20:36:09 GMT  
		Size: 153.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:774190ab951043114cfac82fe6d5923948b0ab61b4919dc460954d418e17e922`  
		Last Modified: Fri, 15 May 2026 20:36:09 GMT  
		Size: 1.1 KB (1145 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be1b61d920c8d44f0020598fdb6bdc73079318883aaca8b7f632f00265890269`  
		Last Modified: Fri, 15 May 2026 20:36:11 GMT  
		Size: 46.0 MB (45952975 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6722aae501650c567f373a1805b9d7ce94da26739c07a9604fb01bf153833e1f`  
		Last Modified: Fri, 15 May 2026 20:36:14 GMT  
		Size: 140.2 MB (140237517 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c854508e029401920f80050dd37c0dbb11523429f59aaabdaf11af4221bdca08`  
		Last Modified: Fri, 15 May 2026 20:36:10 GMT  
		Size: 25.6 KB (25604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:9-jdk-25-and-26-alpine` - unknown; unknown

```console
$ docker pull gradle@sha256:56a0b7b4cff392d63bf366310f14903364c801e8fa77432de940cbc56f7210c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.8 MB (4776867 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:01fb18c66d551a8482f7723d7205ef7155809d96d1855e891bb232cd03d0c73d`

```dockerfile
```

-	Layers:
	-	`sha256:2b2b6e915e7317438fea98128584714a00bc65abe7fbd26694c75c919eaff45b`  
		Last Modified: Fri, 15 May 2026 20:36:09 GMT  
		Size: 4.7 MB (4744475 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d429614d641e7f69524dd50feb2f783d7081c6c9b9fed161b6c168ea13beb024`  
		Last Modified: Fri, 15 May 2026 20:36:08 GMT  
		Size: 32.4 KB (32392 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:9-jdk-25-and-26-alpine` - linux; arm64 variant v8

```console
$ docker pull gradle@sha256:a3024ee6252f29c2e8975f127c26e56ca8768dc63926ec4bacbc5d1fc8989f12
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **387.4 MB (387446151 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d12e23bb8fc884fac683ae85a441d9975991a534b81acecb37c2cdb41efbcc62`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["gradle"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:25 GMT
ADD alpine-minirootfs-3.23.4-aarch64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:25 GMT
CMD ["/bin/sh"]
# Thu, 30 Apr 2026 23:27:10 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 30 Apr 2026 23:27:10 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 30 Apr 2026 23:27:10 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 30 Apr 2026 23:27:10 GMT
RUN set -eux;     apk add --no-cache         fontconfig ttf-dejavu         ca-certificates p11-kit-trust         musl-locales musl-locales-lang         binutils         tzdata         coreutils         openssl     ;     rm -rf /var/cache/apk/* # buildkit
# Thu, 30 Apr 2026 23:27:10 GMT
ENV JAVA_VERSION=jdk-25.0.3+9
# Thu, 30 Apr 2026 23:27:18 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        aarch64)          ESUM='6ed368e93049d3b188c045fce0b20953bbea92fe0614dbbf4d3fd8daad7be3b2';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.3%2B9/OpenJDK25U-jdk_aarch64_alpine-linux_hotspot_25.0.3_9.tar.gz';          ;;        x86_64)          ESUM='51c2415b370aac7c3796b0c4663c8fcf91bc22d76f03df95b25fa5667cb5fdd8';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.3%2B9/OpenJDK25U-jdk_x64_alpine-linux_hotspot_25.0.3_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     apk add --no-cache --virtual .fetch-deps gnupg;     wget -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     apk del --no-network .fetch-deps; # buildkit
# Thu, 30 Apr 2026 23:27:20 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 30 Apr 2026 23:27:20 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 30 Apr 2026 23:27:20 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 30 Apr 2026 23:27:20 GMT
CMD ["jshell"]
# Fri, 15 May 2026 20:35:35 GMT
COPY /opt/java/openjdk /opt/java/openjdk26 # buildkit
# Fri, 15 May 2026 20:35:35 GMT
RUN set -o errexit -o nounset     && ln -s /opt/java/openjdk /opt/java/openjdk25 # buildkit
# Fri, 15 May 2026 20:35:35 GMT
ENV JAVA_LTS_HOME=/opt/java/openjdk25
# Fri, 15 May 2026 20:35:35 GMT
ENV JAVA_CURRENT_HOME=/opt/java/openjdk26
# Fri, 15 May 2026 20:35:35 GMT
CMD ["gradle"]
# Fri, 15 May 2026 20:35:35 GMT
ENV GRADLE_HOME=/opt/gradle
# Fri, 15 May 2026 20:35:35 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && addgroup --system --gid 1000 gradle     && adduser --system --ingroup gradle --uid 1000 --shell /bin/ash gradle     && mkdir /home/gradle/.gradle     && chown -R gradle:gradle /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln -s /home/gradle/.gradle /root/.gradle       && echo "Ensuring Gradle detects installed JDKs"    && echo "org.gradle.java.installations.auto-detect=false" > /home/gradle/.gradle/gradle.properties    && echo "org.gradle.java.installations.auto-download=false" >> /home/gradle/.gradle/gradle.properties    && echo "org.gradle.java.installations.fromEnv=JAVA_LTS_HOME,JAVA_CURRENT_HOME" >> /home/gradle/.gradle/gradle.properties # buildkit
# Fri, 15 May 2026 20:35:35 GMT
VOLUME [/home/gradle/.gradle]
# Fri, 15 May 2026 20:35:35 GMT
WORKDIR /home/gradle
# Fri, 15 May 2026 20:35:37 GMT
RUN set -o errexit -o nounset     && apk add --no-cache       make       curl       wget       tar             breezy       py3-tzlocal       git       git-lfs       mercurial       subversion         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Fri, 15 May 2026 20:35:37 GMT
ENV GRADLE_VERSION=9.5.1
# Fri, 15 May 2026 20:35:37 GMT
ARG GRADLE_DOWNLOAD_SHA256=bafc141b619ad6350fd975fc903156dd5c151998cc8b058e8c1044ab5f7b031f
# Fri, 15 May 2026 20:35:40 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=bafc141b619ad6350fd975fc903156dd5c151998cc8b058e8c1044ab5f7b031f
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum -c -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln -s "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Fri, 15 May 2026 20:35:40 GMT
USER gradle
# Fri, 15 May 2026 20:35:40 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=bafc141b619ad6350fd975fc903156dd5c151998cc8b058e8c1044ab5f7b031f
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --stacktrace --debug --version # buildkit
# Fri, 15 May 2026 20:35:40 GMT
USER root
```

-	Layers:
	-	`sha256:d17f077ada118cc762df373ff803592abf2dfa3ddafaa7381e364dd27a88fca7`  
		Last Modified: Wed, 15 Apr 2026 20:01:32 GMT  
		Size: 4.2 MB (4199870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0efb54362f71a4de98d9ab1446a3a15f82375b426469238870ae07f85f0cf6c0`  
		Last Modified: Thu, 30 Apr 2026 23:27:36 GMT  
		Size: 14.4 MB (14365384 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6641ca90ca6a66c761ef0829dcdd74acc577f377e8239e611764f58e2a21ba3`  
		Last Modified: Thu, 30 Apr 2026 23:27:38 GMT  
		Size: 90.6 MB (90570695 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:538f2e9dbb24a3c1b3ea622a48cd011aa7bd60814a36dd76839ffd9293cb51f2`  
		Last Modified: Thu, 30 Apr 2026 23:27:35 GMT  
		Size: 131.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4d40a550ae76fe4e3f445bfdd07b594be44e2c12492b1425c709e312127b5a1`  
		Last Modified: Thu, 30 Apr 2026 23:27:35 GMT  
		Size: 2.3 KB (2281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dae23a81b091130b9bc31ba6c38cdd97259e930c9f4e8dd8e4be5c3285a2c554`  
		Last Modified: Fri, 15 May 2026 20:36:05 GMT  
		Size: 92.6 MB (92567091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09ecc1f565fee8555fe9b94399249c9061c6c16697b36d7fe2ae7a57e82b57e8`  
		Last Modified: Fri, 15 May 2026 20:36:01 GMT  
		Size: 151.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:448a2c9fcecbd8d440484bb4dd6b2c2fdece37339d916c2a5b86cb0b43017bb1`  
		Last Modified: Fri, 15 May 2026 20:36:01 GMT  
		Size: 1.1 KB (1140 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0bb471c1c066cd2ab6bb3794a9ee5acc03b1013bdeabf0caaf3317edecbad15b`  
		Last Modified: Fri, 15 May 2026 20:36:03 GMT  
		Size: 45.5 MB (45472842 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:460ab562faaa28a9c0be7f6608ba1cd4b48b942fbb06117adea2fa55d920f0eb`  
		Last Modified: Fri, 15 May 2026 20:36:06 GMT  
		Size: 140.2 MB (140237197 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b9f0197afd0cc4705d279c1b4f2249c878893616b04b8b4ad9b1aa5f997a88a`  
		Last Modified: Fri, 15 May 2026 20:36:02 GMT  
		Size: 29.3 KB (29337 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:9-jdk-25-and-26-alpine` - unknown; unknown

```console
$ docker pull gradle@sha256:fbf2830890af3c6c2a04303066d55b16b9022af5c30b6f2da491e0455751eb0b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4926003 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f3ef8cbfecce2ab6757be3be1fcdceeed1892a1b831733e9487c98b1cd0c473`

```dockerfile
```

-	Layers:
	-	`sha256:a5f87e481bc593f21d6104e93fda28ae708c289638ea299ce7a58fe87baf5cd9`  
		Last Modified: Fri, 15 May 2026 20:36:06 GMT  
		Size: 4.9 MB (4893372 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:03c968693a2799cb2360a58ae1ead09c6fe91464f22cbea3b9c90bc849f8748d`  
		Last Modified: Fri, 15 May 2026 20:36:01 GMT  
		Size: 32.6 KB (32631 bytes)  
		MIME: application/vnd.in-toto+json
