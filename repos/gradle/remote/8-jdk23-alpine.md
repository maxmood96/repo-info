## `gradle:8-jdk23-alpine`

```console
$ docker pull gradle@sha256:a015fc884b281c3e2e93156539d5aee60e4d8eb496e7e4f6f5ac7e2483e5aa74
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `gradle:8-jdk23-alpine` - linux; amd64

```console
$ docker pull gradle@sha256:e2efb4ae18cf890e0b8d15beef859d8968cd489c5ac0caf11a9fbe4e357b68c1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **359.7 MB (359722931 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:92c8378a5fa71c4b6aba98b58f625a921a2427f7d63ecc2444b28645003221d2`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["gradle"]`

```dockerfile
# Fri, 06 Sep 2024 12:05:36 GMT
ADD alpine-minirootfs-3.20.3-x86_64.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:05:36 GMT
CMD ["/bin/sh"]
# Wed, 23 Oct 2024 15:41:32 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 23 Oct 2024 15:41:32 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 23 Oct 2024 15:41:32 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 23 Oct 2024 15:41:32 GMT
RUN set -eux;     apk add --no-cache         fontconfig ttf-dejavu         gnupg         ca-certificates p11-kit-trust         musl-locales musl-locales-lang         binutils         tzdata         coreutils         openssl     ;     rm -rf /var/cache/apk/* # buildkit
# Wed, 23 Oct 2024 15:41:32 GMT
ENV JAVA_VERSION=jdk-23.0.1+11
# Wed, 23 Oct 2024 15:41:32 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        aarch64)          ESUM='ebdd6602d27bd7535bf06f21e8a0c3d563be7b790a90bef00cb6ac4123c66f86';          BINARY_URL='https://github.com/adoptium/temurin23-binaries/releases/download/jdk-23.0.1%2B11/OpenJDK23U-jdk_aarch64_alpine-linux_hotspot_23.0.1_11.tar.gz';          ;;        x86_64)          ESUM='4c37a9e885c4e099b049c3ba9baa073de1525e28cd5ffca016c5c5bd7ed385a6';          BINARY_URL='https://github.com/adoptium/temurin23-binaries/releases/download/jdk-23.0.1%2B11/OpenJDK23U-jdk_x64_alpine-linux_hotspot_23.0.1_11.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -r "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Wed, 23 Oct 2024 15:41:32 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 23 Oct 2024 15:41:32 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 23 Oct 2024 15:41:32 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 23 Oct 2024 15:41:32 GMT
CMD ["jshell"]
# Wed, 06 Nov 2024 04:13:47 GMT
CMD ["gradle"]
# Wed, 06 Nov 2024 04:13:47 GMT
ENV GRADLE_HOME=/opt/gradle
# Wed, 06 Nov 2024 04:13:47 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && addgroup --system --gid 1000 gradle     && adduser --system --ingroup gradle --uid 1000 --shell /bin/ash gradle     && mkdir /home/gradle/.gradle     && chown -R gradle:gradle /home/gradle     && chmod -R o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln -s /home/gradle/.gradle /root/.gradle # buildkit
# Wed, 06 Nov 2024 04:13:47 GMT
VOLUME [/home/gradle/.gradle]
# Wed, 06 Nov 2024 04:13:47 GMT
WORKDIR /home/gradle
# Wed, 06 Nov 2024 04:13:47 GMT
RUN set -o errexit -o nounset     && echo "Installing VCSes"     && apk add --no-cache       git       git-lfs       mercurial       subversion         && echo "Testing VCSes"     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Wed, 06 Nov 2024 04:13:47 GMT
ENV GRADLE_VERSION=8.10.2
# Wed, 06 Nov 2024 04:13:47 GMT
ARG GRADLE_DOWNLOAD_SHA256=31c55713e40233a8303827ceb42ca48a47267a0ad4bab9177123121e71524c26
# Wed, 06 Nov 2024 04:13:47 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=31c55713e40233a8303827ceb42ca48a47267a0ad4bab9177123121e71524c26
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum -c -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln -s "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Wed, 06 Nov 2024 04:13:47 GMT
USER gradle
# Wed, 06 Nov 2024 04:13:47 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=31c55713e40233a8303827ceb42ca48a47267a0ad4bab9177123121e71524c26
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Wed, 06 Nov 2024 04:13:47 GMT
USER root
```

-	Layers:
	-	`sha256:da9db072f522755cbeb85be2b3f84059b70571b229512f1571d9217b77e1087f`  
		Last Modified: Fri, 06 Sep 2024 14:39:08 GMT  
		Size: 3.6 MB (3623904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80ac0afaffe8235a13dd8d90914a2d6cd114cf39e349a24c38c2bcdea79ab015`  
		Last Modified: Tue, 12 Nov 2024 02:39:09 GMT  
		Size: 23.0 MB (22953184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0deb3338abfe175e7b298fa61a7147c870fb4aed00f53f4d30d674547e1b45f`  
		Last Modified: Tue, 12 Nov 2024 02:39:12 GMT  
		Size: 165.5 MB (165513301 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3915703c046dd63269dbc212a69ec33a47d1030d48b31a874adf6bf73d47c449`  
		Last Modified: Tue, 12 Nov 2024 02:39:07 GMT  
		Size: 130.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c78fe47fe453af682fad0d120e9e4f2a5c05f85ebe5e3bdec8014fc7020c9c7d`  
		Last Modified: Tue, 12 Nov 2024 02:38:50 GMT  
		Size: 2.3 KB (2281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75a205ef363763a5f6a48e6b93a2d0c769a6e3cac794b18cd2b42c56931a6111`  
		Last Modified: Tue, 12 Nov 2024 03:14:47 GMT  
		Size: 1.0 KB (1022 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e70665d4b34a2d6847db47b2e73ecd5400ce91cdd9e48fc05ca79f858c8b3da3`  
		Last Modified: Tue, 12 Nov 2024 03:14:49 GMT  
		Size: 30.9 MB (30899089 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8388ca2ac53caae28372def46670f06ece7232940014b0747cc1ac6c1aee97c`  
		Last Modified: Tue, 12 Nov 2024 03:14:52 GMT  
		Size: 136.7 MB (136729692 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:400c2092ddb826cf6651db492b83c34c9160fe19a3cdc3b53ba6da61d887c267`  
		Last Modified: Tue, 12 Nov 2024 03:14:48 GMT  
		Size: 296.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:8-jdk23-alpine` - unknown; unknown

```console
$ docker pull gradle@sha256:880b1217aab00e27c5f6f17b24e77285a0856b20f8a45eea6410b5b21d05a88b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3332091 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3bd91f41903b0ead24e72ab3b3249c537e6b106e51c398fa0a0e9b3a4c2b0809`

```dockerfile
```

-	Layers:
	-	`sha256:030293ad6dbc03d1276e838b7c77b6d1ba284e5b591ad3e10289acfe4aa0eedb`  
		Last Modified: Tue, 12 Nov 2024 03:14:48 GMT  
		Size: 3.3 MB (3311177 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cf9d68d9a43e7613c52128f12176e3b185cd50390b25efa7323c2a5a3453e969`  
		Last Modified: Tue, 12 Nov 2024 03:14:48 GMT  
		Size: 20.9 KB (20914 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:8-jdk23-alpine` - linux; arm64 variant v8

```console
$ docker pull gradle@sha256:e54bc217490332e657e373eb7dddc6a1ec7798ea0b2c9438dd642b43ae8990ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **358.8 MB (358752119 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b238e861b3670377b7771731554f22ffb6086ac185113996717a127d0ec9a7fe`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["gradle"]`

```dockerfile
# Fri, 06 Sep 2024 22:44:10 GMT
ADD file:ee5bb8409915b11413f44cce4c22fed658aba4fb078a448e08dd4ac9a23581f2 in / 
# Fri, 06 Sep 2024 22:44:11 GMT
CMD ["/bin/sh"]
# Wed, 16 Oct 2024 03:51:19 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 16 Oct 2024 03:51:19 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 16 Oct 2024 03:51:19 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 16 Oct 2024 03:51:19 GMT
RUN set -eux;     apk add --no-cache         fontconfig ttf-dejavu         gnupg         ca-certificates p11-kit-trust         musl-locales musl-locales-lang         binutils         tzdata         coreutils         openssl     ;     rm -rf /var/cache/apk/* # buildkit
# Wed, 16 Oct 2024 03:51:19 GMT
ENV JAVA_VERSION=jdk-23.0.1+11
# Wed, 16 Oct 2024 03:51:19 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        aarch64)          ESUM='ebdd6602d27bd7535bf06f21e8a0c3d563be7b790a90bef00cb6ac4123c66f86';          BINARY_URL='https://github.com/adoptium/temurin23-binaries/releases/download/jdk-23.0.1%2B11/OpenJDK23U-jdk_aarch64_alpine-linux_hotspot_23.0.1_11.tar.gz';          ;;        x86_64)          ESUM='4c37a9e885c4e099b049c3ba9baa073de1525e28cd5ffca016c5c5bd7ed385a6';          BINARY_URL='https://github.com/adoptium/temurin23-binaries/releases/download/jdk-23.0.1%2B11/OpenJDK23U-jdk_x64_alpine-linux_hotspot_23.0.1_11.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -r "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Wed, 16 Oct 2024 03:51:19 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 16 Oct 2024 03:51:19 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 16 Oct 2024 03:51:19 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 16 Oct 2024 03:51:19 GMT
CMD ["jshell"]
# Wed, 16 Oct 2024 03:51:19 GMT
CMD ["gradle"]
# Wed, 16 Oct 2024 03:51:19 GMT
ENV GRADLE_HOME=/opt/gradle
# Wed, 16 Oct 2024 03:51:19 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && addgroup --system --gid 1000 gradle     && adduser --system --ingroup gradle --uid 1000 --shell /bin/ash gradle     && mkdir /home/gradle/.gradle     && chown -R gradle:gradle /home/gradle     && chmod -R o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln -s /home/gradle/.gradle /root/.gradle # buildkit
# Wed, 16 Oct 2024 03:51:19 GMT
VOLUME [/home/gradle/.gradle]
# Wed, 16 Oct 2024 03:51:19 GMT
WORKDIR /home/gradle
# Wed, 16 Oct 2024 03:51:19 GMT
RUN set -o errexit -o nounset     && echo "Installing VCSes"     && apk add --no-cache       git       git-lfs       mercurial       subversion         && echo "Testing VCSes"     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Wed, 16 Oct 2024 03:51:19 GMT
ENV GRADLE_VERSION=8.10.2
# Wed, 16 Oct 2024 03:51:19 GMT
ARG GRADLE_DOWNLOAD_SHA256=31c55713e40233a8303827ceb42ca48a47267a0ad4bab9177123121e71524c26
# Wed, 16 Oct 2024 03:51:19 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=31c55713e40233a8303827ceb42ca48a47267a0ad4bab9177123121e71524c26
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum -c -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln -s "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Wed, 16 Oct 2024 03:51:19 GMT
USER gradle
# Wed, 16 Oct 2024 03:51:19 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=31c55713e40233a8303827ceb42ca48a47267a0ad4bab9177123121e71524c26
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Wed, 16 Oct 2024 03:51:19 GMT
USER root
```

-	Layers:
	-	`sha256:cf04c63912e16506c4413937c7f4579018e4bb25c272d989789cfba77b12f951`  
		Last Modified: Fri, 06 Sep 2024 22:44:39 GMT  
		Size: 4.1 MB (4087646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba5ab350b8ff57c75640d387c970dd2282464d9836a98c0f02d04ffe85d3db64`  
		Last Modified: Thu, 24 Oct 2024 01:14:18 GMT  
		Size: 23.7 MB (23731419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95498a283ecd538532b8a7cea1be8462e6dbe863fdedd3e095a6a5f1b4a15a9e`  
		Last Modified: Thu, 24 Oct 2024 01:19:42 GMT  
		Size: 163.3 MB (163315840 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ed6bb967beba8210b0f1fc248fedf04f00058a1af4816baa27ab290efeaa649`  
		Last Modified: Thu, 24 Oct 2024 01:19:38 GMT  
		Size: 130.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4c1e2e0f6d842ca700db91de478c29907f7a0b9b0eccafdb8602f2a01f8e016`  
		Last Modified: Thu, 24 Oct 2024 01:19:38 GMT  
		Size: 2.3 KB (2281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1cd3c49e973d1c3d8a85938a21a971f9c79bba03988f545fcc13732cc4fb87f9`  
		Last Modified: Thu, 24 Oct 2024 02:40:20 GMT  
		Size: 1.0 KB (1021 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5ed8f6d31fa013f2933d3a65a8eb892ef8ae2aef00dcbf70dd088a4ac64514a`  
		Last Modified: Thu, 24 Oct 2024 02:40:21 GMT  
		Size: 30.9 MB (30883106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f704a9abcc2fe0e4290f70a5d2f098306e914516037d92eab2466f6ddb7ad783`  
		Last Modified: Thu, 24 Oct 2024 02:40:24 GMT  
		Size: 136.7 MB (136730351 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76478dc205168f638d41f845a50ce073a7930af6bb2df904dbe9de8d7dcdee63`  
		Last Modified: Thu, 24 Oct 2024 02:40:20 GMT  
		Size: 293.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:8-jdk23-alpine` - unknown; unknown

```console
$ docker pull gradle@sha256:1c19e9f14ebcb9b7059d38960573e332209f87b856a8e2ce5060173217ae5509
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.4 MB (3436441 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f8feae46304c75a901c83349abfabd8ed6e0b07130eabb17fa6c9aa9e0ea8e4`

```dockerfile
```

-	Layers:
	-	`sha256:cb226ca9e79d3108060811f368efa04b37387fe9f475d4b64c21994543560b43`  
		Last Modified: Thu, 24 Oct 2024 02:40:20 GMT  
		Size: 3.4 MB (3415342 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:badf6beb44a37d818a014a74d2b9568da49e0001ac2e8e1d55b6c6bb7e8f427a`  
		Last Modified: Thu, 24 Oct 2024 02:40:20 GMT  
		Size: 21.1 KB (21099 bytes)  
		MIME: application/vnd.in-toto+json
