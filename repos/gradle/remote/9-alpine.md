## `gradle:9-alpine`

```console
$ docker pull gradle@sha256:10e70222a1e4cc41f3395b0fe217cf0dbe9de18f799b1c4ee15ce8d8881419f4
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `gradle:9-alpine` - linux; amd64

```console
$ docker pull gradle@sha256:6bfcc3c8a38331095ca91a5ebc6b22cf235263e106160ad8003dd24d446ef3d4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **293.5 MB (293466537 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b09830c14e653c57d9078a512eb4febcf3ec4a4eeac4c9651e0dd1b15846061e`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["gradle"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:04 GMT
ADD alpine-minirootfs-3.23.3-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:04 GMT
CMD ["/bin/sh"]
# Thu, 05 Feb 2026 22:20:43 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 05 Feb 2026 22:20:43 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 05 Feb 2026 22:20:43 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 05 Feb 2026 22:20:43 GMT
RUN set -eux;     apk add --no-cache         fontconfig ttf-dejavu         ca-certificates p11-kit-trust         musl-locales musl-locales-lang         binutils         tzdata         coreutils         openssl     ;     rm -rf /var/cache/apk/* # buildkit
# Thu, 05 Feb 2026 22:20:43 GMT
ENV JAVA_VERSION=jdk-25.0.2+10
# Thu, 05 Feb 2026 22:20:50 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        aarch64)          ESUM='e8d928fb018eabb31a148ebadaa5a5ec69273e6562afede21c426960a6a67143';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.2%2B10/OpenJDK25U-jdk_aarch64_alpine-linux_hotspot_25.0.2_10.tar.gz';          ;;        x86_64)          ESUM='961f13ba0ee1e18c41c50ab642361e4283dee5e7947a48ed6a72c8a661d0cca0';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.2%2B10/OpenJDK25U-jdk_x64_alpine-linux_hotspot_25.0.2_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     apk add --no-cache --virtual .fetch-deps gnupg;     wget -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     apk del --no-network .fetch-deps; # buildkit
# Thu, 05 Feb 2026 22:20:51 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 05 Feb 2026 22:20:51 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 05 Feb 2026 22:20:51 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 05 Feb 2026 22:20:51 GMT
CMD ["jshell"]
# Wed, 04 Mar 2026 17:53:58 GMT
CMD ["gradle"]
# Wed, 04 Mar 2026 17:53:58 GMT
ENV GRADLE_HOME=/opt/gradle
# Wed, 04 Mar 2026 17:53:58 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && addgroup --system --gid 1000 gradle     && adduser --system --ingroup gradle --uid 1000 --shell /bin/ash gradle     && mkdir /home/gradle/.gradle     && chown -R gradle:gradle /home/gradle     && chmod -R o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln -s /home/gradle/.gradle /root/.gradle # buildkit
# Wed, 04 Mar 2026 17:53:58 GMT
VOLUME [/home/gradle/.gradle]
# Wed, 04 Mar 2026 17:53:58 GMT
WORKDIR /home/gradle
# Wed, 04 Mar 2026 17:54:00 GMT
RUN set -o errexit -o nounset     && apk add --no-cache       make       curl       wget       tar             breezy       py3-tzlocal       git       git-lfs       mercurial       subversion         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Wed, 04 Mar 2026 17:54:00 GMT
ENV GRADLE_VERSION=9.4.0
# Wed, 04 Mar 2026 17:54:00 GMT
ARG GRADLE_DOWNLOAD_SHA256=60ea723356d81263e8002fec0fcf9e2b0eee0c0850c7a3d7ab0a63f2ccc601f3
# Wed, 04 Mar 2026 17:54:02 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=60ea723356d81263e8002fec0fcf9e2b0eee0c0850c7a3d7ab0a63f2ccc601f3
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum -c -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln -s "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Wed, 04 Mar 2026 17:54:02 GMT
USER gradle
# Wed, 04 Mar 2026 17:54:03 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=60ea723356d81263e8002fec0fcf9e2b0eee0c0850c7a3d7ab0a63f2ccc601f3
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --stacktrace --debug --version # buildkit
# Wed, 04 Mar 2026 17:54:03 GMT
USER root
```

-	Layers:
	-	`sha256:589002ba0eaed121a1dbf42f6648f29e5be55d5c8a6ee0f8eaa0285cc21ac153`  
		Last Modified: Wed, 28 Jan 2026 01:18:09 GMT  
		Size: 3.9 MB (3861821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a150fdcc19ea38586861ab60f38c860b790aae07d0df506d6237d0b88dd7bd6f`  
		Last Modified: Thu, 05 Feb 2026 22:21:06 GMT  
		Size: 14.3 MB (14303782 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6acd3bd6814d41ef248fdd907c1157cbd4d90e1cc3ec091e962a6416099873bc`  
		Last Modified: Thu, 05 Feb 2026 22:21:08 GMT  
		Size: 91.5 MB (91491467 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36b2ab561e1f5769d12480d85e27bf1a14a7757ff69b3acea0acc6b4bb0171cc`  
		Last Modified: Thu, 05 Feb 2026 22:21:05 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53405ff8853b1f58bfdc8d736024ea0d1b6df7fa5dedfb0e52a34829c361f358`  
		Last Modified: Thu, 05 Feb 2026 22:21:05 GMT  
		Size: 2.3 KB (2280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8cef8879cb72ee97801f405997fdd964e22fecb603dac0e66f5f92dfb9c8c7a`  
		Last Modified: Wed, 04 Mar 2026 17:54:18 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3ffa0027e386cb685e917b66a98e8f878dee0f81f303a73bd249aa0c2c5593a`  
		Last Modified: Wed, 04 Mar 2026 17:54:20 GMT  
		Size: 46.0 MB (46006878 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a1c91dae9d72e33f2c823098640955d0b6be30ad74bbc271a6b7e49d34decd5`  
		Last Modified: Wed, 04 Mar 2026 17:54:22 GMT  
		Size: 137.8 MB (137773511 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5945e57bebddfc81d1fc6aa166d21f1bece187e7f44f0b7846c06db559d0d22`  
		Last Modified: Wed, 04 Mar 2026 17:54:18 GMT  
		Size: 25.6 KB (25627 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:9-alpine` - unknown; unknown

```console
$ docker pull gradle@sha256:6de36c6a5c03cba5a01abef83d61aa4a66c4f43285f891d01082d1d8cf705a13
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4626027 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef5aa7a4156d60985ac86596599d278a1631fb6243553de108a2670f49bbee9f`

```dockerfile
```

-	Layers:
	-	`sha256:fa728bdd521710604f5b3fd353e27c27294148b207ef8dc8e573f2116dc4c7fc`  
		Last Modified: Wed, 04 Mar 2026 17:54:18 GMT  
		Size: 4.6 MB (4600935 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ba10ba9d5eaa4576c3818db1498de857c2c44e049920f26773764ba83e7ed81b`  
		Last Modified: Wed, 04 Mar 2026 17:54:18 GMT  
		Size: 25.1 KB (25092 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:9-alpine` - linux; arm64 variant v8

```console
$ docker pull gradle@sha256:2c58c1b2569318d2d108228c98c94ac4d2403e88ca292f7a947abab7e95c06c2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **292.3 MB (292329793 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f94edd934db9e63926d5121666d0b78b2f488a6cb459e5203cf2de62b4792e87`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["gradle"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:09 GMT
ADD alpine-minirootfs-3.23.3-aarch64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:09 GMT
CMD ["/bin/sh"]
# Thu, 05 Feb 2026 22:19:42 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 05 Feb 2026 22:19:42 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 05 Feb 2026 22:19:42 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 05 Feb 2026 22:19:42 GMT
RUN set -eux;     apk add --no-cache         fontconfig ttf-dejavu         ca-certificates p11-kit-trust         musl-locales musl-locales-lang         binutils         tzdata         coreutils         openssl     ;     rm -rf /var/cache/apk/* # buildkit
# Thu, 05 Feb 2026 22:19:42 GMT
ENV JAVA_VERSION=jdk-25.0.2+10
# Thu, 05 Feb 2026 22:19:48 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        aarch64)          ESUM='e8d928fb018eabb31a148ebadaa5a5ec69273e6562afede21c426960a6a67143';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.2%2B10/OpenJDK25U-jdk_aarch64_alpine-linux_hotspot_25.0.2_10.tar.gz';          ;;        x86_64)          ESUM='961f13ba0ee1e18c41c50ab642361e4283dee5e7947a48ed6a72c8a661d0cca0';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.2%2B10/OpenJDK25U-jdk_x64_alpine-linux_hotspot_25.0.2_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     apk add --no-cache --virtual .fetch-deps gnupg;     wget -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     apk del --no-network .fetch-deps; # buildkit
# Thu, 05 Feb 2026 22:19:50 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 05 Feb 2026 22:19:50 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 05 Feb 2026 22:19:50 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 05 Feb 2026 22:19:50 GMT
CMD ["jshell"]
# Wed, 04 Mar 2026 17:53:17 GMT
CMD ["gradle"]
# Wed, 04 Mar 2026 17:53:17 GMT
ENV GRADLE_HOME=/opt/gradle
# Wed, 04 Mar 2026 17:53:17 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && addgroup --system --gid 1000 gradle     && adduser --system --ingroup gradle --uid 1000 --shell /bin/ash gradle     && mkdir /home/gradle/.gradle     && chown -R gradle:gradle /home/gradle     && chmod -R o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln -s /home/gradle/.gradle /root/.gradle # buildkit
# Wed, 04 Mar 2026 17:53:17 GMT
VOLUME [/home/gradle/.gradle]
# Wed, 04 Mar 2026 17:53:17 GMT
WORKDIR /home/gradle
# Wed, 04 Mar 2026 17:53:21 GMT
RUN set -o errexit -o nounset     && apk add --no-cache       make       curl       wget       tar             breezy       py3-tzlocal       git       git-lfs       mercurial       subversion         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Wed, 04 Mar 2026 17:53:21 GMT
ENV GRADLE_VERSION=9.4.0
# Wed, 04 Mar 2026 17:53:21 GMT
ARG GRADLE_DOWNLOAD_SHA256=60ea723356d81263e8002fec0fcf9e2b0eee0c0850c7a3d7ab0a63f2ccc601f3
# Wed, 04 Mar 2026 17:53:24 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=60ea723356d81263e8002fec0fcf9e2b0eee0c0850c7a3d7ab0a63f2ccc601f3
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum -c -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln -s "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Wed, 04 Mar 2026 17:53:24 GMT
USER gradle
# Wed, 04 Mar 2026 17:53:24 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=60ea723356d81263e8002fec0fcf9e2b0eee0c0850c7a3d7ab0a63f2ccc601f3
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --stacktrace --debug --version # buildkit
# Wed, 04 Mar 2026 17:53:24 GMT
USER root
```

-	Layers:
	-	`sha256:d8ad8cd72600f46cc068e16c39046ebc76526e41051f43a8c249884b200936c0`  
		Last Modified: Wed, 28 Jan 2026 01:18:15 GMT  
		Size: 4.2 MB (4197091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1dc273c5968a27128010b44442da19c1d19512b5d65a3a7fc4734eec44550e27`  
		Last Modified: Thu, 05 Feb 2026 22:20:05 GMT  
		Size: 14.4 MB (14373158 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e47108ee2f22449f768312319f1c90c0d5a1580374197687fd1944d8e2265225`  
		Last Modified: Thu, 05 Feb 2026 22:20:07 GMT  
		Size: 90.4 MB (90431353 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33fed661f46011e75ee9460b18305d0584e08525180dd346895a225fab422298`  
		Last Modified: Thu, 05 Feb 2026 22:20:04 GMT  
		Size: 130.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e47f9177a4521d408115970652519968867bb5c776093bf3b8b10b66aaa3caa1`  
		Last Modified: Thu, 05 Feb 2026 22:20:04 GMT  
		Size: 2.3 KB (2281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b85e3c6d24a5eea3dfeadbe76b3023b5f5012d05bb959022981d4e382c0c6b6`  
		Last Modified: Wed, 04 Mar 2026 17:53:39 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b2da54432813c0d94b118ed4e4040cea7727946ac3bf6479b8ba0bf6ef579e6`  
		Last Modified: Wed, 04 Mar 2026 17:53:41 GMT  
		Size: 45.5 MB (45521898 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c228c7cd8f7918a99f01b837091783b4c4689be8ab811d98b8465664e4dd661a`  
		Last Modified: Wed, 04 Mar 2026 17:53:43 GMT  
		Size: 137.8 MB (137773495 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:030f1e75a86ced28994dae1a527409f26c29ca86cc41973a54feb538fff7e94d`  
		Last Modified: Wed, 04 Mar 2026 17:53:39 GMT  
		Size: 29.3 KB (29344 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:9-alpine` - unknown; unknown

```console
$ docker pull gradle@sha256:fe4008dc98a8d3a106482ce51f6a9230487819820ce69e5107506d183c90bc7d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.8 MB (4775840 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e8e42290e49a71c525b25dd694721a757b8c10dcdd082718adca853712eb2e2b`

```dockerfile
```

-	Layers:
	-	`sha256:a6a6b964e35123483a9fb6ba99e19ea0f56bbca4dab8fc0c490bedc227d4cfc7`  
		Last Modified: Wed, 04 Mar 2026 17:53:39 GMT  
		Size: 4.8 MB (4750503 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fedc07506be1292e461ad42c84821ee11862b729d823379c33d807954ecd7494`  
		Last Modified: Wed, 04 Mar 2026 17:53:39 GMT  
		Size: 25.3 KB (25337 bytes)  
		MIME: application/vnd.in-toto+json
