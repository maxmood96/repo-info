## `gradle:jdk-25-and-25-alpine`

```console
$ docker pull gradle@sha256:1cd4b77fd5392d22965e217494e58a04195d46387af0674b88fc2d8cd428724e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `gradle:jdk-25-and-25-alpine` - linux; amd64

```console
$ docker pull gradle@sha256:89b9c66dd6347000cc6395f86e75bde7e8d92842804fda99f723e60d2cd99a70
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **292.9 MB (292895078 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b328e3f923200d86949654876d16f7659481687dbfc767f4a9c4076bfb7a715c`
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
# Fri, 16 Jan 2026 21:47:09 GMT
RUN set -o errexit -o nounset     && ln -s /opt/java/openjdk /opt/java/openjdk25 # buildkit
# Fri, 16 Jan 2026 21:47:09 GMT
ENV JAVA_CURRENT_HOME=/opt/java/openjdk25
# Fri, 16 Jan 2026 21:47:09 GMT
ENV JAVA_LTS_HOME=/opt/java/openjdk25
# Fri, 16 Jan 2026 21:47:09 GMT
CMD ["gradle"]
# Fri, 16 Jan 2026 21:47:09 GMT
ENV GRADLE_HOME=/opt/gradle
# Fri, 16 Jan 2026 21:47:09 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && addgroup --system --gid 1000 gradle     && adduser --system --ingroup gradle --uid 1000 --shell /bin/ash gradle     && mkdir /home/gradle/.gradle     && chown -R gradle:gradle /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln -s /home/gradle/.gradle /root/.gradle       && echo "Ensuring Gradle detects installed JDKs"    && echo "org.gradle.java.installations.auto-detect=false" > /home/gradle/.gradle/gradle.properties    && echo "org.gradle.java.installations.auto-download=false" >> /home/gradle/.gradle/gradle.properties    && echo "org.gradle.java.installations.fromEnv=JAVA_LTS_HOME,JAVA_CURRENT_HOME" >> /home/gradle/.gradle/gradle.properties # buildkit
# Fri, 16 Jan 2026 21:47:09 GMT
VOLUME [/home/gradle/.gradle]
# Fri, 16 Jan 2026 21:47:09 GMT
WORKDIR /home/gradle
# Fri, 16 Jan 2026 21:47:11 GMT
RUN set -o errexit -o nounset     && apk add --no-cache       make       curl       wget       tar             breezy       py3-tzlocal       git       git-lfs       mercurial       subversion         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Fri, 16 Jan 2026 21:47:11 GMT
ENV GRADLE_VERSION=9.3.0
# Fri, 16 Jan 2026 21:47:11 GMT
ARG GRADLE_DOWNLOAD_SHA256=0d585f69da091fc5b2beced877feab55a3064d43b8a1d46aeb07996b0915e0e0
# Fri, 16 Jan 2026 21:47:13 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=0d585f69da091fc5b2beced877feab55a3064d43b8a1d46aeb07996b0915e0e0
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum -c -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln -s "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Fri, 16 Jan 2026 21:47:13 GMT
USER gradle
# Fri, 16 Jan 2026 21:47:14 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=0d585f69da091fc5b2beced877feab55a3064d43b8a1d46aeb07996b0915e0e0
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --stacktrace --debug --version # buildkit
# Fri, 16 Jan 2026 21:47:14 GMT
USER root
```

-	Layers:
	-	`sha256:2d35ebdb57d9971fea0cac1582aa78935adf8058b2cc32db163c98822e5dfa1b`  
		Last Modified: Sun, 07 Dec 2025 13:53:31 GMT  
		Size: 3.8 MB (3802452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc0ab655b026e5703579820f0d4485d514c6ec9d4b5b462890ac71da2da0ae46`  
		Last Modified: Wed, 07 Jan 2026 18:58:11 GMT  
		Size: 14.2 MB (14245329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:669f1a65d0fae852f6718306326728109ed1ddecfbfd653037dda93a9669e4a7`  
		Last Modified: Wed, 07 Jan 2026 18:58:45 GMT  
		Size: 91.3 MB (91279717 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f288373361582707b01fea1abf34f4ff1053f3baee5acb21cf34af46e4f8c85`  
		Last Modified: Sat, 08 Nov 2025 18:00:25 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ce3137254c0a4b1b24ea31eeee2f470985f40fee31365b16a41a6d5745dac38`  
		Last Modified: Sat, 08 Nov 2025 18:00:25 GMT  
		Size: 2.3 KB (2281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7852c5337c1e7bcdafaba5c54b9d1d4dc87373e76db32a3b74250cdb9064a437`  
		Last Modified: Fri, 16 Jan 2026 21:47:30 GMT  
		Size: 152.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e1d4a42f99cf50322cd246367858237909a6313dd007a66440262cb6916c679`  
		Last Modified: Fri, 16 Jan 2026 21:47:30 GMT  
		Size: 1.1 KB (1141 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:004439623e217836b864c64cae2d405a66ab13d24bcaa8c933bacdcbbeb22639`  
		Last Modified: Fri, 16 Jan 2026 21:47:45 GMT  
		Size: 46.5 MB (46548843 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9494eb981f547e1d996579801606103ff4fdeff6633810f3c15b57a3ef570d6`  
		Last Modified: Sat, 17 Jan 2026 19:19:29 GMT  
		Size: 137.0 MB (136989410 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:657efcdda9e7ec5613b72d3fc6a6c8ee680a015ffd3843ee532e3b8d56be2abd`  
		Last Modified: Fri, 16 Jan 2026 21:47:31 GMT  
		Size: 25.6 KB (25594 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:jdk-25-and-25-alpine` - unknown; unknown

```console
$ docker pull gradle@sha256:0f8a908441d8e5a6a519e22d950e600dafda67047030532aa5b74cca9d2a5a89
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4615675 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:059e5fde143d6266b05f44118396399809ec875c322b69f7947142583da992da`

```dockerfile
```

-	Layers:
	-	`sha256:13e19cd4a04f9ffaf575a03b3afaab3d42f744cfd5348cf86a3e48f7ee7dd8a6`  
		Last Modified: Sat, 17 Jan 2026 00:22:14 GMT  
		Size: 4.6 MB (4587365 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:746fa830204048f3816b3523eff5388183c68a000bae3c58925a36593973d887`  
		Last Modified: Fri, 16 Jan 2026 21:47:30 GMT  
		Size: 28.3 KB (28310 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:jdk-25-and-25-alpine` - linux; arm64 variant v8

```console
$ docker pull gradle@sha256:2ddfd93c8b4fffb437baa7bade95cfc0bc3c24615d2967e4e2ddf1918caf50dc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **291.8 MB (291779836 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1cfb126b900a1dd07edd44b91d009c9157b18585469015d0838f6c31fcbfff30`
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
# Fri, 16 Jan 2026 21:46:52 GMT
RUN set -o errexit -o nounset     && ln -s /opt/java/openjdk /opt/java/openjdk25 # buildkit
# Fri, 16 Jan 2026 21:46:52 GMT
ENV JAVA_CURRENT_HOME=/opt/java/openjdk25
# Fri, 16 Jan 2026 21:46:52 GMT
ENV JAVA_LTS_HOME=/opt/java/openjdk25
# Fri, 16 Jan 2026 21:46:52 GMT
CMD ["gradle"]
# Fri, 16 Jan 2026 21:46:52 GMT
ENV GRADLE_HOME=/opt/gradle
# Fri, 16 Jan 2026 21:46:52 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && addgroup --system --gid 1000 gradle     && adduser --system --ingroup gradle --uid 1000 --shell /bin/ash gradle     && mkdir /home/gradle/.gradle     && chown -R gradle:gradle /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln -s /home/gradle/.gradle /root/.gradle       && echo "Ensuring Gradle detects installed JDKs"    && echo "org.gradle.java.installations.auto-detect=false" > /home/gradle/.gradle/gradle.properties    && echo "org.gradle.java.installations.auto-download=false" >> /home/gradle/.gradle/gradle.properties    && echo "org.gradle.java.installations.fromEnv=JAVA_LTS_HOME,JAVA_CURRENT_HOME" >> /home/gradle/.gradle/gradle.properties # buildkit
# Fri, 16 Jan 2026 21:46:52 GMT
VOLUME [/home/gradle/.gradle]
# Fri, 16 Jan 2026 21:46:52 GMT
WORKDIR /home/gradle
# Fri, 16 Jan 2026 21:46:55 GMT
RUN set -o errexit -o nounset     && apk add --no-cache       make       curl       wget       tar             breezy       py3-tzlocal       git       git-lfs       mercurial       subversion         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Fri, 16 Jan 2026 21:46:55 GMT
ENV GRADLE_VERSION=9.3.0
# Fri, 16 Jan 2026 21:46:55 GMT
ARG GRADLE_DOWNLOAD_SHA256=0d585f69da091fc5b2beced877feab55a3064d43b8a1d46aeb07996b0915e0e0
# Fri, 16 Jan 2026 21:46:57 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=0d585f69da091fc5b2beced877feab55a3064d43b8a1d46aeb07996b0915e0e0
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum -c -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln -s "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Fri, 16 Jan 2026 21:46:57 GMT
USER gradle
# Fri, 16 Jan 2026 21:46:58 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=0d585f69da091fc5b2beced877feab55a3064d43b8a1d46aeb07996b0915e0e0
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --stacktrace --debug --version # buildkit
# Fri, 16 Jan 2026 21:46:58 GMT
USER root
```

-	Layers:
	-	`sha256:6b59a28fa20117e6048ad0616b8d8c901877ef15ff4c7f18db04e4f01f43bc39`  
		Last Modified: Sun, 07 Dec 2025 13:54:03 GMT  
		Size: 4.1 MB (4138069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:942b164f8b4d68be083596089650c1556ab1373815abc8abda59bc45d20ffd1c`  
		Last Modified: Wed, 07 Jan 2026 21:18:13 GMT  
		Size: 14.4 MB (14352513 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:edde8e40d136c44f0d23e0b4d7594cae8888c80bed021fac4cf5ebebb75434c1`  
		Last Modified: Wed, 07 Jan 2026 21:18:16 GMT  
		Size: 90.2 MB (90190637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13765a23e62e85c56a5a54b976e0378167533c0495d297bb429a218799ab164f`  
		Last Modified: Sat, 08 Nov 2025 17:59:56 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29c959ab9ac7fdf8f6393c84753f989ef0811ac7c86a2d184030c23e2d067c93`  
		Last Modified: Sat, 08 Nov 2025 17:59:56 GMT  
		Size: 2.3 KB (2277 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f984e09cdca9f7ba458c0f5ba67858b7f71c84e34a1037001aa2999124a32800`  
		Last Modified: Fri, 16 Jan 2026 21:47:12 GMT  
		Size: 151.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76fb1f3abea56a3c24eaad70fd37381afb70c8935f3541cfe7b4381e409e5d16`  
		Last Modified: Fri, 16 Jan 2026 21:47:12 GMT  
		Size: 1.1 KB (1141 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:755c0920891756e5c38e5a5574e6414a50f61d634ff43a48b8c0672ea00550ad`  
		Last Modified: Fri, 16 Jan 2026 21:47:14 GMT  
		Size: 46.1 MB (46076062 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b85cc628ccfa6c1247ccb82e6f8dae2e357b5f2a92acb8baf749f0e48f9edbf8`  
		Last Modified: Fri, 16 Jan 2026 21:47:36 GMT  
		Size: 137.0 MB (136989501 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:817c2fc55b2eb88f4967ddaf09a467478806bd603c428ef72ecb9b9cbb5567fc`  
		Last Modified: Fri, 16 Jan 2026 21:47:13 GMT  
		Size: 29.3 KB (29325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:jdk-25-and-25-alpine` - unknown; unknown

```console
$ docker pull gradle@sha256:2e6811645bfb99993a0d0187590f7105c0d551253ce8dc3541d86542dd2f59b3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.8 MB (4766060 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:977dc686616357da2713225d997e33c84a79ef8780fda5d76944887b24cee612`

```dockerfile
```

-	Layers:
	-	`sha256:7845b2b95e276499872f7b94a6c73272bdd80dbb5216238abd67eaa5215640bb`  
		Last Modified: Fri, 16 Jan 2026 21:47:12 GMT  
		Size: 4.7 MB (4737538 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b34d2aa81e029690a7c937fdfd838632e109382a06099d9ed35f92d7c1c83380`  
		Last Modified: Fri, 16 Jan 2026 21:47:12 GMT  
		Size: 28.5 KB (28522 bytes)  
		MIME: application/vnd.in-toto+json
