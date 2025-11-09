## `gradle:9-jdk-25-and-25-alpine`

```console
$ docker pull gradle@sha256:c123d0d2b4b937e8dc367b547362e15ffd6384b09cb1d90a7bf8ecf37eb9befe
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `gradle:9-jdk-25-and-25-alpine` - linux; amd64

```console
$ docker pull gradle@sha256:0eb9148d8c4c49c75b9095f36c0e5ac6848a1daffc13f10183d9db8c328cc7b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **291.5 MB (291468439 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ced8d77fb7f877f632c30387f2577222628ee4aaf63934695ac25f68a7bb7634`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["gradle"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-x86_64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Sat, 08 Nov 2025 18:00:04 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 08 Nov 2025 18:00:04 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 08 Nov 2025 18:00:04 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Sat, 08 Nov 2025 18:00:04 GMT
RUN set -eux;     apk add --no-cache         fontconfig ttf-dejavu         ca-certificates p11-kit-trust         musl-locales musl-locales-lang         binutils         tzdata         coreutils         openssl     ;     rm -rf /var/cache/apk/* # buildkit
# Sat, 08 Nov 2025 18:00:04 GMT
ENV JAVA_VERSION=jdk-25.0.1+8
# Sat, 08 Nov 2025 18:00:10 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        aarch64)          ESUM='e95584c7fb7d4020003b325d5c3af9c29dde514571da362aac04586a88f2d728';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.1%2B8/OpenJDK25U-jdk_aarch64_alpine-linux_hotspot_25.0.1_8.tar.gz';          ;;        x86_64)          ESUM='375a1f22ef1a488737330ea10bbc7418a1a49c5d0df36d4f59d18fd82fc63593';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.1%2B8/OpenJDK25U-jdk_x64_alpine-linux_hotspot_25.0.1_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     apk add --no-cache --virtual .fetch-deps gnupg;     wget -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     apk del --no-network .fetch-deps; # buildkit
# Sat, 08 Nov 2025 18:00:11 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Sat, 08 Nov 2025 18:00:11 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Sat, 08 Nov 2025 18:00:11 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Sat, 08 Nov 2025 18:00:11 GMT
CMD ["jshell"]
# Sat, 08 Nov 2025 18:22:19 GMT
RUN set -o errexit -o nounset     && ln -s /opt/java/openjdk /opt/java/openjdk25 # buildkit
# Sat, 08 Nov 2025 18:22:20 GMT
ENV JAVA_CURRENT_HOME=/opt/java/openjdk25
# Sat, 08 Nov 2025 18:22:20 GMT
ENV JAVA_LTS_HOME=/opt/java/openjdk25
# Sat, 08 Nov 2025 18:22:20 GMT
CMD ["gradle"]
# Sat, 08 Nov 2025 18:22:20 GMT
ENV GRADLE_HOME=/opt/gradle
# Sat, 08 Nov 2025 18:22:20 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && addgroup --system --gid 1000 gradle     && adduser --system --ingroup gradle --uid 1000 --shell /bin/ash gradle     && mkdir /home/gradle/.gradle     && chown -R gradle:gradle /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln -s /home/gradle/.gradle /root/.gradle       && echo "Ensuring Gradle detects installed JDKs"    && echo "org.gradle.java.installations.auto-detect=false" > /home/gradle/.gradle/gradle.properties    && echo "org.gradle.java.installations.auto-download=false" >> /home/gradle/.gradle/gradle.properties    && echo "org.gradle.java.installations.fromEnv=JAVA_LTS_HOME,JAVA_CURRENT_HOME" >> /home/gradle/.gradle/gradle.properties # buildkit
# Sat, 08 Nov 2025 18:22:20 GMT
VOLUME [/home/gradle/.gradle]
# Sat, 08 Nov 2025 18:22:20 GMT
WORKDIR /home/gradle
# Sat, 08 Nov 2025 18:22:21 GMT
RUN set -o errexit -o nounset     && apk add --no-cache       make       curl       wget       tar             breezy       py3-tzlocal       git       git-lfs       mercurial       subversion         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Sat, 08 Nov 2025 18:22:21 GMT
ENV GRADLE_VERSION=9.2.0
# Sat, 08 Nov 2025 18:22:21 GMT
ARG GRADLE_DOWNLOAD_SHA256=df67a32e86e3276d011735facb1535f64d0d88df84fa87521e90becc2d735444
# Sat, 08 Nov 2025 18:22:23 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=df67a32e86e3276d011735facb1535f64d0d88df84fa87521e90becc2d735444
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum -c -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln -s "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Sat, 08 Nov 2025 18:22:23 GMT
USER gradle
# Sat, 08 Nov 2025 18:22:24 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=df67a32e86e3276d011735facb1535f64d0d88df84fa87521e90becc2d735444
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Sat, 08 Nov 2025 18:22:24 GMT
USER root
```

-	Layers:
	-	`sha256:2d35ebdb57d9971fea0cac1582aa78935adf8058b2cc32db163c98822e5dfa1b`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 3.8 MB (3802452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc0ab655b026e5703579820f0d4485d514c6ec9d4b5b462890ac71da2da0ae46`  
		Last Modified: Sat, 08 Nov 2025 18:00:40 GMT  
		Size: 14.2 MB (14245329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:669f1a65d0fae852f6718306326728109ed1ddecfbfd653037dda93a9669e4a7`  
		Last Modified: Sat, 08 Nov 2025 18:00:50 GMT  
		Size: 91.3 MB (91279717 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f288373361582707b01fea1abf34f4ff1053f3baee5acb21cf34af46e4f8c85`  
		Last Modified: Sat, 08 Nov 2025 18:00:37 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ce3137254c0a4b1b24ea31eeee2f470985f40fee31365b16a41a6d5745dac38`  
		Last Modified: Sat, 08 Nov 2025 18:00:38 GMT  
		Size: 2.3 KB (2281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:331bf712d56b33749165b9cc7e7afd881264a8a301f295a31372383292cb7f2f`  
		Last Modified: Sat, 08 Nov 2025 18:22:50 GMT  
		Size: 149.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:115dbe0aa006339224722838135a0bfc0159220d6bde801b9bc153924c01492f`  
		Last Modified: Sat, 08 Nov 2025 18:22:50 GMT  
		Size: 1.1 KB (1140 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf23ccd7ad81fa3f435fc8bac284a21d71983dd15e6212449c70a9e5ac360358`  
		Last Modified: Sat, 08 Nov 2025 18:22:53 GMT  
		Size: 46.6 MB (46561226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a25b8fde0652298f04c1b65016638a9c85bbf5994e6aa5b95571544cb39ccfb7`  
		Last Modified: Sun, 09 Nov 2025 06:31:16 GMT  
		Size: 135.5 MB (135521087 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:293bbe0675fe7be0ef7a4265cae0257b6a038dc9e877cfd27cda2785c1d1d565`  
		Last Modified: Sat, 08 Nov 2025 18:22:51 GMT  
		Size: 54.9 KB (54899 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:9-jdk-25-and-25-alpine` - unknown; unknown

```console
$ docker pull gradle@sha256:6caaf21794b30f2d808f00df036d084eef4236568289cbdd9a1309386e75e9ba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4626662 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c865980403b7c58cf84e1d9dbc514fa2b1d8ebcd39df6d6294c4c207fe7895d`

```dockerfile
```

-	Layers:
	-	`sha256:2c2bae966ecd878bad7d3721a9536e574998b3bc8c891694b0e5145baacd5af6`  
		Last Modified: Sat, 08 Nov 2025 21:31:54 GMT  
		Size: 4.6 MB (4598401 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:685416741d7ed1a49ee3ffa1b856566411fbd14f3baf5c664cb9a42c1d54b5fa`  
		Last Modified: Sat, 08 Nov 2025 21:31:55 GMT  
		Size: 28.3 KB (28261 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:9-jdk-25-and-25-alpine` - linux; arm64 variant v8

```console
$ docker pull gradle@sha256:d7ce65bceca64e8b452d6e25447cc0d63841300d5a22f7a91bae77cca522d1aa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **290.3 MB (290335902 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fcdb2f5afe6ab918dc9ae5294528d521b43aff7a9822ef279b0642089a10b0be`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["gradle"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-aarch64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Sat, 08 Nov 2025 17:59:31 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 08 Nov 2025 17:59:31 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 08 Nov 2025 17:59:31 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Sat, 08 Nov 2025 17:59:31 GMT
RUN set -eux;     apk add --no-cache         fontconfig ttf-dejavu         ca-certificates p11-kit-trust         musl-locales musl-locales-lang         binutils         tzdata         coreutils         openssl     ;     rm -rf /var/cache/apk/* # buildkit
# Sat, 08 Nov 2025 17:59:31 GMT
ENV JAVA_VERSION=jdk-25.0.1+8
# Sat, 08 Nov 2025 17:59:40 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        aarch64)          ESUM='e95584c7fb7d4020003b325d5c3af9c29dde514571da362aac04586a88f2d728';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.1%2B8/OpenJDK25U-jdk_aarch64_alpine-linux_hotspot_25.0.1_8.tar.gz';          ;;        x86_64)          ESUM='375a1f22ef1a488737330ea10bbc7418a1a49c5d0df36d4f59d18fd82fc63593';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.1%2B8/OpenJDK25U-jdk_x64_alpine-linux_hotspot_25.0.1_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     apk add --no-cache --virtual .fetch-deps gnupg;     wget -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     apk del --no-network .fetch-deps; # buildkit
# Sat, 08 Nov 2025 17:59:42 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Sat, 08 Nov 2025 17:59:42 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Sat, 08 Nov 2025 17:59:42 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Sat, 08 Nov 2025 17:59:42 GMT
CMD ["jshell"]
# Sat, 08 Nov 2025 18:23:04 GMT
RUN set -o errexit -o nounset     && ln -s /opt/java/openjdk /opt/java/openjdk25 # buildkit
# Sat, 08 Nov 2025 18:23:05 GMT
ENV JAVA_CURRENT_HOME=/opt/java/openjdk25
# Sat, 08 Nov 2025 18:23:05 GMT
ENV JAVA_LTS_HOME=/opt/java/openjdk25
# Sat, 08 Nov 2025 18:23:05 GMT
CMD ["gradle"]
# Sat, 08 Nov 2025 18:23:05 GMT
ENV GRADLE_HOME=/opt/gradle
# Sat, 08 Nov 2025 18:23:05 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && addgroup --system --gid 1000 gradle     && adduser --system --ingroup gradle --uid 1000 --shell /bin/ash gradle     && mkdir /home/gradle/.gradle     && chown -R gradle:gradle /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln -s /home/gradle/.gradle /root/.gradle       && echo "Ensuring Gradle detects installed JDKs"    && echo "org.gradle.java.installations.auto-detect=false" > /home/gradle/.gradle/gradle.properties    && echo "org.gradle.java.installations.auto-download=false" >> /home/gradle/.gradle/gradle.properties    && echo "org.gradle.java.installations.fromEnv=JAVA_LTS_HOME,JAVA_CURRENT_HOME" >> /home/gradle/.gradle/gradle.properties # buildkit
# Sat, 08 Nov 2025 18:23:05 GMT
VOLUME [/home/gradle/.gradle]
# Sat, 08 Nov 2025 18:23:05 GMT
WORKDIR /home/gradle
# Sat, 08 Nov 2025 18:23:07 GMT
RUN set -o errexit -o nounset     && apk add --no-cache       make       curl       wget       tar             breezy       py3-tzlocal       git       git-lfs       mercurial       subversion         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Sat, 08 Nov 2025 18:23:07 GMT
ENV GRADLE_VERSION=9.2.0
# Sat, 08 Nov 2025 18:23:07 GMT
ARG GRADLE_DOWNLOAD_SHA256=df67a32e86e3276d011735facb1535f64d0d88df84fa87521e90becc2d735444
# Sat, 08 Nov 2025 18:23:09 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=df67a32e86e3276d011735facb1535f64d0d88df84fa87521e90becc2d735444
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum -c -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln -s "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Sat, 08 Nov 2025 18:23:09 GMT
USER gradle
# Sat, 08 Nov 2025 18:23:10 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=df67a32e86e3276d011735facb1535f64d0d88df84fa87521e90becc2d735444
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Sat, 08 Nov 2025 18:23:10 GMT
USER root
```

-	Layers:
	-	`sha256:6b59a28fa20117e6048ad0616b8d8c901877ef15ff4c7f18db04e4f01f43bc39`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 4.1 MB (4138069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:942b164f8b4d68be083596089650c1556ab1373815abc8abda59bc45d20ffd1c`  
		Last Modified: Sat, 08 Nov 2025 18:00:15 GMT  
		Size: 14.4 MB (14352513 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:edde8e40d136c44f0d23e0b4d7594cae8888c80bed021fac4cf5ebebb75434c1`  
		Last Modified: Sat, 08 Nov 2025 18:21:45 GMT  
		Size: 90.2 MB (90190637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13765a23e62e85c56a5a54b976e0378167533c0495d297bb429a218799ab164f`  
		Last Modified: Sat, 08 Nov 2025 18:00:05 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29c959ab9ac7fdf8f6393c84753f989ef0811ac7c86a2d184030c23e2d067c93`  
		Last Modified: Sat, 08 Nov 2025 18:00:04 GMT  
		Size: 2.3 KB (2277 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4bef0983876a37e4aa61cc2c2e06a6f62f7ec44b1ed0c1144c1187b3dccf562b`  
		Last Modified: Sat, 08 Nov 2025 18:23:34 GMT  
		Size: 148.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:357fe0e9c657d7dd5105976031fd60a6d63f793f00e95ce40e7393c4d0e11aa0`  
		Last Modified: Sat, 08 Nov 2025 18:23:34 GMT  
		Size: 1.1 KB (1138 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41c002ad19a5187023c5b5fc82f68829a881f44052ffdce3354a601e58409cbe`  
		Last Modified: Sat, 08 Nov 2025 18:23:36 GMT  
		Size: 46.1 MB (46070206 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e2b70456a171bc414698e6181cea7c669b3909fb55e086ffb99f3ac4f75bf29`  
		Last Modified: Sun, 09 Nov 2025 06:32:22 GMT  
		Size: 135.5 MB (135521221 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5949603d7ec2b6a0175ecfdd45ac4407cbf2b06393622e57f191d21cf1e10c35`  
		Last Modified: Sat, 08 Nov 2025 18:23:34 GMT  
		Size: 59.5 KB (59533 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:9-jdk-25-and-25-alpine` - unknown; unknown

```console
$ docker pull gradle@sha256:75ec30e25566c5313d8927c4d4091ff80af235360664f11013e17fed72ecc3cc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.8 MB (4777047 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b71f243c1fc9377d65d496059cf7bd44447fce3e2fbb947eea3f7a37f8a07f63`

```dockerfile
```

-	Layers:
	-	`sha256:f4b5e66a803dff51ebcf9288584095f456813a748702ed03786ca3a9562c15ae`  
		Last Modified: Sat, 08 Nov 2025 21:31:59 GMT  
		Size: 4.7 MB (4748574 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cb33833efa9e513a274d646b5239269b310f6b010ced3d67c4097472d3688d2c`  
		Last Modified: Sat, 08 Nov 2025 21:31:59 GMT  
		Size: 28.5 KB (28473 bytes)  
		MIME: application/vnd.in-toto+json
