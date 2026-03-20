## `gradle:alpine`

```console
$ docker pull gradle@sha256:1740a41324f61a6936e18c7b2d53181645d039aa4551986b7543797cd7b770fe
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `gradle:alpine` - linux; amd64

```console
$ docker pull gradle@sha256:ee6e8c114fbc68b0b7865f58beefdfcc9ca81403272a3b77bda952266c66ea3f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **293.5 MB (293515104 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1dfda00a3c89b95535ac793d9e584a9314bd23280ff4a98df961a7612f076768`
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
# Fri, 20 Mar 2026 17:09:40 GMT
CMD ["gradle"]
# Fri, 20 Mar 2026 17:09:40 GMT
ENV GRADLE_HOME=/opt/gradle
# Fri, 20 Mar 2026 17:09:40 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && addgroup --system --gid 1000 gradle     && adduser --system --ingroup gradle --uid 1000 --shell /bin/ash gradle     && mkdir /home/gradle/.gradle     && chown -R gradle:gradle /home/gradle     && chmod -R o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln -s /home/gradle/.gradle /root/.gradle # buildkit
# Fri, 20 Mar 2026 17:09:40 GMT
VOLUME [/home/gradle/.gradle]
# Fri, 20 Mar 2026 17:09:40 GMT
WORKDIR /home/gradle
# Fri, 20 Mar 2026 17:09:43 GMT
RUN set -o errexit -o nounset     && apk add --no-cache       make       curl       wget       tar             breezy       py3-tzlocal       git       git-lfs       mercurial       subversion         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Fri, 20 Mar 2026 17:09:43 GMT
ENV GRADLE_VERSION=9.4.1
# Fri, 20 Mar 2026 17:09:43 GMT
ARG GRADLE_DOWNLOAD_SHA256=2ab2958f2a1e51120c326cad6f385153bb11ee93b3c216c5fccebfdfbb7ec6cb
# Fri, 20 Mar 2026 17:09:45 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=2ab2958f2a1e51120c326cad6f385153bb11ee93b3c216c5fccebfdfbb7ec6cb
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum -c -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln -s "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Fri, 20 Mar 2026 17:09:45 GMT
USER gradle
# Fri, 20 Mar 2026 17:09:46 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=2ab2958f2a1e51120c326cad6f385153bb11ee93b3c216c5fccebfdfbb7ec6cb
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --stacktrace --debug --version # buildkit
# Fri, 20 Mar 2026 17:09:46 GMT
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
	-	`sha256:9a2b58ecc902a6c286f3aa84410ff58dc7030311c6592dec4463c91857c262c1`  
		Last Modified: Fri, 20 Mar 2026 17:10:02 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:156030d6c13fb2c4753a24335c0d792a57bec0443dc4a133f4fe77737ad66fb2`  
		Last Modified: Fri, 20 Mar 2026 17:10:05 GMT  
		Size: 46.0 MB (46020421 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ee8260db53c4411557d61c280be3256dfa78e47c0ba34580af7c165aefaf3af`  
		Last Modified: Fri, 20 Mar 2026 17:10:09 GMT  
		Size: 137.8 MB (137808545 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b78a94e58b8fc7215e32f98ab8b10c087742c07670ec59f423e0084fa8261467`  
		Last Modified: Fri, 20 Mar 2026 17:10:02 GMT  
		Size: 25.6 KB (25617 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:alpine` - unknown; unknown

```console
$ docker pull gradle@sha256:ea7b0663f35628d52bb587353ee6fe8097a9864b9f8857eab2b5114d5c9406d4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4626026 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a26be561c840e9a216dccd8105fcdfbd566391a1b55957e0b5e8b39ac7b8b19e`

```dockerfile
```

-	Layers:
	-	`sha256:d041db4bd2259f53ad13119d9864417b5a1e3db7f10516c943b4073f0a1a40ac`  
		Last Modified: Fri, 20 Mar 2026 17:10:02 GMT  
		Size: 4.6 MB (4600935 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:50150333937ca2f571c5570c6969b0e12c86564a6b8f2879f7586b30d96b7205`  
		Last Modified: Fri, 20 Mar 2026 17:10:02 GMT  
		Size: 25.1 KB (25091 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:alpine` - linux; arm64 variant v8

```console
$ docker pull gradle@sha256:eabca5c14dbf5ee4a88491443cb85acdac0b2349ea1cdee5b3cb13bb251325ac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **292.4 MB (292380767 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea705b4bffecab5be438b87dc3ee8404ead9b6ea9a4997c5c8a9f23db143d066`
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
# Fri, 20 Mar 2026 17:09:25 GMT
CMD ["gradle"]
# Fri, 20 Mar 2026 17:09:25 GMT
ENV GRADLE_HOME=/opt/gradle
# Fri, 20 Mar 2026 17:09:25 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && addgroup --system --gid 1000 gradle     && adduser --system --ingroup gradle --uid 1000 --shell /bin/ash gradle     && mkdir /home/gradle/.gradle     && chown -R gradle:gradle /home/gradle     && chmod -R o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln -s /home/gradle/.gradle /root/.gradle # buildkit
# Fri, 20 Mar 2026 17:09:25 GMT
VOLUME [/home/gradle/.gradle]
# Fri, 20 Mar 2026 17:09:25 GMT
WORKDIR /home/gradle
# Fri, 20 Mar 2026 17:09:28 GMT
RUN set -o errexit -o nounset     && apk add --no-cache       make       curl       wget       tar             breezy       py3-tzlocal       git       git-lfs       mercurial       subversion         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Fri, 20 Mar 2026 17:09:28 GMT
ENV GRADLE_VERSION=9.4.1
# Fri, 20 Mar 2026 17:09:28 GMT
ARG GRADLE_DOWNLOAD_SHA256=2ab2958f2a1e51120c326cad6f385153bb11ee93b3c216c5fccebfdfbb7ec6cb
# Fri, 20 Mar 2026 17:09:31 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=2ab2958f2a1e51120c326cad6f385153bb11ee93b3c216c5fccebfdfbb7ec6cb
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum -c -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln -s "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Fri, 20 Mar 2026 17:09:31 GMT
USER gradle
# Fri, 20 Mar 2026 17:09:32 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=2ab2958f2a1e51120c326cad6f385153bb11ee93b3c216c5fccebfdfbb7ec6cb
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --stacktrace --debug --version # buildkit
# Fri, 20 Mar 2026 17:09:32 GMT
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
	-	`sha256:ece094a6a65881f4b7fbf7bf83d9b00782221e5f9a04f73e35c4f9fb73b33b82`  
		Last Modified: Fri, 20 Mar 2026 17:09:47 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e599c92be63548b09078b89dc27925bac137c7685cf26ac1344d4d178921131e`  
		Last Modified: Fri, 20 Mar 2026 17:09:50 GMT  
		Size: 45.5 MB (45537602 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93e51f711c65dfd86e8e8f01094e9a70621525105cc971ef29d4489435a115cc`  
		Last Modified: Fri, 20 Mar 2026 17:09:52 GMT  
		Size: 137.8 MB (137808761 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8ff998bc939aa397e8f2f28650bfa8c8a3d0aa9ab78b7ed50d42d8a1f51a746`  
		Last Modified: Fri, 20 Mar 2026 17:09:47 GMT  
		Size: 29.3 KB (29349 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:alpine` - unknown; unknown

```console
$ docker pull gradle@sha256:6d49c768a9682400cf691bba7b2e86acf7cba4e5d499d4165a3a1d912618eb63
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.8 MB (4775840 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a221ca5693f02b9c2fea2cb47776e9c28a98e518cde3c0b5abef393090e76df`

```dockerfile
```

-	Layers:
	-	`sha256:6d3e10b62724dfb3ccbdb6d9c9d6ec71485b961960668125419b896aeb63fe15`  
		Last Modified: Fri, 20 Mar 2026 17:09:47 GMT  
		Size: 4.8 MB (4750503 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a1d32e3082d9ba04924edab6c2f53c272dc545e6f1209d398f892b9227ea55cd`  
		Last Modified: Fri, 20 Mar 2026 17:09:47 GMT  
		Size: 25.3 KB (25337 bytes)  
		MIME: application/vnd.in-toto+json
