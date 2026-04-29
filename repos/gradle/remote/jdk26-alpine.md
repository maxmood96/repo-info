## `gradle:jdk26-alpine`

```console
$ docker pull gradle@sha256:d4fee577ab57e14c9098c20be9b535e4bea33fb9335c7df98e092c30ebc878a5
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `gradle:jdk26-alpine` - linux; amd64

```console
$ docker pull gradle@sha256:28dc8c817e92620f97513a7b09e50c14a7925f889de3bfc845eff2b90f250fa1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **298.2 MB (298180315 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd51096a4454ee852cd18d4b2d5d22cac20c450bf6970ad0a271953730f9d274`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["gradle"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:40 GMT
ADD alpine-minirootfs-3.23.4-x86_64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:40 GMT
CMD ["/bin/sh"]
# Wed, 15 Apr 2026 20:34:31 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 15 Apr 2026 20:34:31 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 15 Apr 2026 20:34:31 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 15 Apr 2026 20:34:31 GMT
RUN set -eux;     apk add --no-cache         fontconfig ttf-dejavu         ca-certificates p11-kit-trust         musl-locales musl-locales-lang         binutils         tzdata         coreutils         openssl     ;     rm -rf /var/cache/apk/* # buildkit
# Wed, 15 Apr 2026 20:34:31 GMT
ENV JAVA_VERSION=jdk-26+35
# Wed, 15 Apr 2026 20:35:19 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        aarch64)          ESUM='049027647a2d1cf3b1e3c1e7dad746aa6436928932bbed9130b87a25f585908a';          BINARY_URL='https://github.com/adoptium/temurin26-binaries/releases/download/jdk-26%2B35/OpenJDK26U-jdk_aarch64_alpine-linux_hotspot_26_35.tar.gz';          ;;        x86_64)          ESUM='c105e581fdccb4e7120d889235d1ad8d5b2bed0af4972bc881e0a8ba687c94a4';          BINARY_URL='https://github.com/adoptium/temurin26-binaries/releases/download/jdk-26%2B35/OpenJDK26U-jdk_x64_alpine-linux_hotspot_26_35.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     apk add --no-cache --virtual .fetch-deps gnupg;     wget -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     apk del --no-network .fetch-deps; # buildkit
# Wed, 15 Apr 2026 20:35:21 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 15 Apr 2026 20:35:21 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 15 Apr 2026 20:35:21 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 15 Apr 2026 20:35:21 GMT
CMD ["jshell"]
# Tue, 28 Apr 2026 23:31:16 GMT
CMD ["gradle"]
# Tue, 28 Apr 2026 23:31:16 GMT
ENV GRADLE_HOME=/opt/gradle
# Tue, 28 Apr 2026 23:31:16 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && addgroup --system --gid 1000 gradle     && adduser --system --ingroup gradle --uid 1000 --shell /bin/ash gradle     && mkdir /home/gradle/.gradle     && chown -R gradle:gradle /home/gradle     && chmod -R o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln -s /home/gradle/.gradle /root/.gradle # buildkit
# Tue, 28 Apr 2026 23:31:16 GMT
VOLUME [/home/gradle/.gradle]
# Tue, 28 Apr 2026 23:31:17 GMT
WORKDIR /home/gradle
# Tue, 28 Apr 2026 23:31:19 GMT
RUN set -o errexit -o nounset     && apk add --no-cache       make       curl       wget       tar             breezy       py3-tzlocal       git       git-lfs       mercurial       subversion         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Tue, 28 Apr 2026 23:31:19 GMT
ENV GRADLE_VERSION=9.5.0
# Tue, 28 Apr 2026 23:31:19 GMT
ARG GRADLE_DOWNLOAD_SHA256=553c78f50dafcd54d65b9a444649057857469edf836431389695608536d6b746
# Tue, 28 Apr 2026 23:31:21 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=553c78f50dafcd54d65b9a444649057857469edf836431389695608536d6b746
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum -c -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln -s "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Tue, 28 Apr 2026 23:31:21 GMT
USER gradle
# Tue, 28 Apr 2026 23:31:22 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=553c78f50dafcd54d65b9a444649057857469edf836431389695608536d6b746
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --stacktrace --debug --version # buildkit
# Tue, 28 Apr 2026 23:31:22 GMT
USER root
```

-	Layers:
	-	`sha256:6a0ac1617861a677b045b7ff88545213ec31c0ff08763195a70a4a5adda577bb`  
		Last Modified: Wed, 15 Apr 2026 20:01:46 GMT  
		Size: 3.9 MB (3864189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c8bff7045b4dedcda28d3e173f14d1ba10aa99e2d37aca0e2fc2121c2c26408`  
		Last Modified: Wed, 15 Apr 2026 20:35:38 GMT  
		Size: 14.3 MB (14307228 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:391edefba2e6ae3493026f4fb7364e2b3cfdb3d6f20c95c057a840c7e2a70de4`  
		Last Modified: Wed, 15 Apr 2026 20:35:37 GMT  
		Size: 93.7 MB (93716220 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:195635ff26dc4127f92b360891f7063894021e91e54110ef34da2c8959f43c67`  
		Last Modified: Wed, 15 Apr 2026 20:35:34 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d3caeef0ce8088f690976509ec2e96ce94d7badc8e863f438892920077dceff`  
		Last Modified: Wed, 15 Apr 2026 20:35:34 GMT  
		Size: 2.3 KB (2280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a724b71ffca4c78284616e82a8633896f24adbb3fea755ebc245235bdafe449`  
		Last Modified: Tue, 28 Apr 2026 23:31:38 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73856531affd9060a3c4f199264d49ee1963adc8764571af84b17621488be528`  
		Last Modified: Tue, 28 Apr 2026 23:31:40 GMT  
		Size: 46.0 MB (46027484 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:752b46162b6e7751b8d6c72c4bee6cb9fd1f226c0f219d45ce61c04ffe436e28`  
		Last Modified: Tue, 28 Apr 2026 23:31:42 GMT  
		Size: 140.2 MB (140236121 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f4168a486c364af231303003cbe67153e0e33a06e0eec1b6a4d339e87a8fcb5`  
		Last Modified: Tue, 28 Apr 2026 23:31:38 GMT  
		Size: 25.6 KB (25622 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:jdk26-alpine` - unknown; unknown

```console
$ docker pull gradle@sha256:236952a8ab128060c756154320900d74445e135a1725dad48b2329577d4249bd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4646143 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9d870d2055dc45d31572ce9d2ab5adc5cf3421203b788db63ae85215719dcaef`

```dockerfile
```

-	Layers:
	-	`sha256:b952c1e7d2d27accdef6e2d8bccf685204a8c15cbfce65425092c56e8b3c61e0`  
		Last Modified: Tue, 28 Apr 2026 23:31:38 GMT  
		Size: 4.6 MB (4623531 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0cf47b59c376da614ac45e85587c03b5bc5ca1fef6c73dede9b194f3a708f371`  
		Last Modified: Tue, 28 Apr 2026 23:31:38 GMT  
		Size: 22.6 KB (22612 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:jdk26-alpine` - linux; arm64 variant v8

```console
$ docker pull gradle@sha256:419eaf1ea94898c63e52f686391a06e070ba95416cd901e480a679d3f9971d51
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **297.0 MB (296978934 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:97fb092b2319c8ad4e1c1cb3194eb28076609f08a85f05adb19955c61af45810`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["gradle"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:25 GMT
ADD alpine-minirootfs-3.23.4-aarch64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:25 GMT
CMD ["/bin/sh"]
# Wed, 15 Apr 2026 20:34:49 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 15 Apr 2026 20:34:49 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 15 Apr 2026 20:34:49 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 15 Apr 2026 20:34:49 GMT
RUN set -eux;     apk add --no-cache         fontconfig ttf-dejavu         ca-certificates p11-kit-trust         musl-locales musl-locales-lang         binutils         tzdata         coreutils         openssl     ;     rm -rf /var/cache/apk/* # buildkit
# Wed, 15 Apr 2026 20:34:49 GMT
ENV JAVA_VERSION=jdk-26+35
# Wed, 15 Apr 2026 20:34:59 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        aarch64)          ESUM='049027647a2d1cf3b1e3c1e7dad746aa6436928932bbed9130b87a25f585908a';          BINARY_URL='https://github.com/adoptium/temurin26-binaries/releases/download/jdk-26%2B35/OpenJDK26U-jdk_aarch64_alpine-linux_hotspot_26_35.tar.gz';          ;;        x86_64)          ESUM='c105e581fdccb4e7120d889235d1ad8d5b2bed0af4972bc881e0a8ba687c94a4';          BINARY_URL='https://github.com/adoptium/temurin26-binaries/releases/download/jdk-26%2B35/OpenJDK26U-jdk_x64_alpine-linux_hotspot_26_35.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     apk add --no-cache --virtual .fetch-deps gnupg;     wget -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     apk del --no-network .fetch-deps; # buildkit
# Wed, 15 Apr 2026 20:35:00 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 15 Apr 2026 20:35:00 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 15 Apr 2026 20:35:00 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 15 Apr 2026 20:35:00 GMT
CMD ["jshell"]
# Tue, 28 Apr 2026 23:32:34 GMT
CMD ["gradle"]
# Tue, 28 Apr 2026 23:32:34 GMT
ENV GRADLE_HOME=/opt/gradle
# Tue, 28 Apr 2026 23:32:34 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && addgroup --system --gid 1000 gradle     && adduser --system --ingroup gradle --uid 1000 --shell /bin/ash gradle     && mkdir /home/gradle/.gradle     && chown -R gradle:gradle /home/gradle     && chmod -R o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln -s /home/gradle/.gradle /root/.gradle # buildkit
# Tue, 28 Apr 2026 23:32:34 GMT
VOLUME [/home/gradle/.gradle]
# Tue, 28 Apr 2026 23:32:34 GMT
WORKDIR /home/gradle
# Tue, 28 Apr 2026 23:32:36 GMT
RUN set -o errexit -o nounset     && apk add --no-cache       make       curl       wget       tar             breezy       py3-tzlocal       git       git-lfs       mercurial       subversion         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Tue, 28 Apr 2026 23:32:36 GMT
ENV GRADLE_VERSION=9.5.0
# Tue, 28 Apr 2026 23:32:36 GMT
ARG GRADLE_DOWNLOAD_SHA256=553c78f50dafcd54d65b9a444649057857469edf836431389695608536d6b746
# Tue, 28 Apr 2026 23:32:39 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=553c78f50dafcd54d65b9a444649057857469edf836431389695608536d6b746
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum -c -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln -s "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Tue, 28 Apr 2026 23:32:39 GMT
USER gradle
# Tue, 28 Apr 2026 23:32:40 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=553c78f50dafcd54d65b9a444649057857469edf836431389695608536d6b746
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --stacktrace --debug --version # buildkit
# Tue, 28 Apr 2026 23:32:40 GMT
USER root
```

-	Layers:
	-	`sha256:d17f077ada118cc762df373ff803592abf2dfa3ddafaa7381e364dd27a88fca7`  
		Last Modified: Wed, 15 Apr 2026 20:01:32 GMT  
		Size: 4.2 MB (4199870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10b8c9f714bd537100e4118563ae7a953d248cf9031f3f9563aec762a9abce04`  
		Last Modified: Wed, 15 Apr 2026 20:35:16 GMT  
		Size: 14.4 MB (14365600 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d118d41a2fa844b8c088c1ff89c9b0c2813f936d1f5be8258ff9b6f16390758`  
		Last Modified: Wed, 15 Apr 2026 20:35:18 GMT  
		Size: 92.6 MB (92608698 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd56b354af4d3369e57e9e8e23b3c98b944e529ac302b27349c701e656b15fc9`  
		Last Modified: Wed, 15 Apr 2026 20:35:15 GMT  
		Size: 130.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dacc27638916d2e266082323745d2dd8fa8a569aef22680acc5e3998a045c25a`  
		Last Modified: Wed, 15 Apr 2026 20:35:06 GMT  
		Size: 2.3 KB (2281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:226dd6b34734a215c19dc36ef72324a113d4fde51bcc092e332d7eefb675e0d2`  
		Last Modified: Tue, 28 Apr 2026 23:32:55 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbb8b86f62f2ee050cbed75548cad958a0976ac0abfe4a9b4026889a9cb2927e`  
		Last Modified: Tue, 28 Apr 2026 23:32:57 GMT  
		Size: 45.5 MB (45535504 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6f54fd8328a97b4215b39aac57411a5f505d568daa266a15acd66b1d237dd2e`  
		Last Modified: Tue, 28 Apr 2026 23:32:59 GMT  
		Size: 140.2 MB (140236454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b62e550de98419e37e1229f751ae6e9b3c803e21286329e6160fa117ce53aa0`  
		Last Modified: Tue, 28 Apr 2026 23:32:55 GMT  
		Size: 29.4 KB (29355 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:jdk26-alpine` - unknown; unknown

```console
$ docker pull gradle@sha256:506d2a42fc6e0d2784339780288c06dfff37a3341bf7f38592e9d9639f19dd22
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.8 MB (4795764 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b37b1c515a0de7a5e13caba755c040e5317aa769d10fbda7f6a4a6d4a74b636f`

```dockerfile
```

-	Layers:
	-	`sha256:94cd07b198cefe6c20321c24e9a7ddd1589265984bbe4af82c23404967158417`  
		Last Modified: Tue, 28 Apr 2026 23:32:55 GMT  
		Size: 4.8 MB (4773003 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:919edb875457db70b59772acd27b568c4b7df474ba3f5bbf68f538da90138ba0`  
		Last Modified: Tue, 28 Apr 2026 23:32:55 GMT  
		Size: 22.8 KB (22761 bytes)  
		MIME: application/vnd.in-toto+json
