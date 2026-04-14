## `gradle:jdk17-ubi`

```console
$ docker pull gradle@sha256:4457f1dd2f12775af6441d077a6a2a5210531fb0369f9975cb7f46602f8102d5
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 8
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `gradle:jdk17-ubi` - linux; amd64

```console
$ docker pull gradle@sha256:9c2128716b494c68943c8e05f53370da6d0ea3ee9f32d92fc00d1cf5240218dc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **394.3 MB (394336997 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2720987c42436b8c012807b5100dd155e927b09276bc2bf8b7b0ef04b6ace66b`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["gradle"]`

```dockerfile
# Mon, 13 Apr 2026 09:14:03 GMT
LABEL maintainer="Red Hat, Inc."
# Mon, 13 Apr 2026 09:14:03 GMT
LABEL vendor="Red Hat, Inc."
# Mon, 13 Apr 2026 09:14:03 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Mon, 13 Apr 2026 09:14:03 GMT
LABEL com.redhat.component="ubi10-minimal-container"       name="ubi10/ubi-minimal"       version="10.1"       cpe="cpe:/o:redhat:enterprise_linux:10.1"       distribution-scope="public"
# Mon, 13 Apr 2026 09:14:03 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Mon, 13 Apr 2026 09:14:03 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 10."
# Mon, 13 Apr 2026 09:14:03 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 13 Apr 2026 09:14:03 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 13 Apr 2026 09:14:03 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 10 Minimal"
# Mon, 13 Apr 2026 09:14:03 GMT
LABEL io.openshift.expose-services=""
# Mon, 13 Apr 2026 09:14:03 GMT
LABEL io.openshift.tags="minimal rhel10"
# Mon, 13 Apr 2026 09:14:03 GMT
ENV container oci
# Mon, 13 Apr 2026 09:14:04 GMT
COPY dir:76b09a495622d7b6331e3b1ce0727af742be820fe3eaf865e896be5c160bcdbe in /      
# Mon, 13 Apr 2026 09:14:04 GMT
COPY file:5de33b5fc08b00635bccf9134a18978dba13e2250aa51838f9969515a3957847 in /etc/yum.repos.d/.      
# Mon, 13 Apr 2026 09:14:04 GMT
CMD ["/bin/bash"]
# Mon, 13 Apr 2026 09:14:04 GMT
COPY file:595171150af68abc798ea385f7988d74b566aa8e84babff137f00b08b2164683 in /usr/share/buildinfo/content-sets.json      
# Mon, 13 Apr 2026 09:14:04 GMT
COPY file:595171150af68abc798ea385f7988d74b566aa8e84babff137f00b08b2164683 in /root/buildinfo/content_manifests/content-sets.json      
# Mon, 13 Apr 2026 09:14:04 GMT
COPY file:95047be8e40b1e3c668ac62dda8bcb33d863723da6a80c1b3ce4f34f04292a93 in /usr/share/buildinfo/labels.json      
# Mon, 13 Apr 2026 09:14:04 GMT
COPY file:95047be8e40b1e3c668ac62dda8bcb33d863723da6a80c1b3ce4f34f04292a93 in /root/buildinfo/labels.json      
# Mon, 13 Apr 2026 09:14:05 GMT
LABEL "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="d468a83fbf6024b899244a1d1179beff08d84a7a" "org.opencontainers.image.revision"="d468a83fbf6024b899244a1d1179beff08d84a7a" "build-date"="2026-04-13T09:13:50Z" "org.opencontainers.image.created"="2026-04-13T09:13:50Z" "release"="1776071394"org.opencontainers.image.revision=d468a83fbf6024b899244a1d1179beff08d84a7a,org.opencontainers.image.created=2026-04-13T09:13:50Z
# Mon, 13 Apr 2026 23:54:51 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 13 Apr 2026 23:54:51 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 13 Apr 2026 23:54:51 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 13 Apr 2026 23:54:51 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en         gnupg2     ;     microdnf clean all # buildkit
# Mon, 13 Apr 2026 23:54:51 GMT
ENV JAVA_VERSION=jdk-17.0.18+8
# Mon, 13 Apr 2026 23:56:38 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='592a6702b3a07a0e0b82cb38aaab149bfce1b0c24d6b57ddb410bd9009333095';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jdk_aarch64_linux_hotspot_17.0.18_8.tar.gz';          ;;        ppc64le)          ESUM='5ab89fbde560e1a09386f389dd7881715b896f49c6e9aa974f72d551337dba5e';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jdk_ppc64le_linux_hotspot_17.0.18_8.tar.gz';          ;;        s390x)          ESUM='3693469655bcfa2fa5e70907245a2b3bc4236db7d9fa1b9feb0ab7abd235da09';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jdk_s390x_linux_hotspot_17.0.18_8.tar.gz';          ;;        x86_64)          ESUM='0c94cbb54325c40dcf026143eb621562017db5525727f2d9131a11250f72c450';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jdk_x64_linux_hotspot_17.0.18_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Mon, 13 Apr 2026 23:56:39 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Mon, 13 Apr 2026 23:56:39 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Mon, 13 Apr 2026 23:56:39 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Mon, 13 Apr 2026 23:56:39 GMT
CMD ["jshell"]
# Tue, 14 Apr 2026 00:12:16 GMT
CMD ["gradle"]
# Tue, 14 Apr 2026 00:12:16 GMT
ENV GRADLE_HOME=/opt/gradle
# Tue, 14 Apr 2026 00:12:16 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 101 gradle     && useradd --system --gid gradle --uid 101 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Tue, 14 Apr 2026 00:12:16 GMT
VOLUME [/home/gradle/.gradle]
# Tue, 14 Apr 2026 00:12:16 GMT
WORKDIR /home/gradle
# Tue, 14 Apr 2026 00:12:19 GMT
RUN set -o errexit -o nounset     && microdnf install -y         make         curl-minimal         wget         tar                 findutils                 unzip         which                 git         git-lfs         subversion     && microdnf clean all         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which svn # buildkit
# Tue, 14 Apr 2026 00:12:19 GMT
ENV GRADLE_VERSION=9.4.1
# Tue, 14 Apr 2026 00:12:19 GMT
ARG GRADLE_DOWNLOAD_SHA256=2ab2958f2a1e51120c326cad6f385153bb11ee93b3c216c5fccebfdfbb7ec6cb
# Tue, 14 Apr 2026 00:12:22 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=2ab2958f2a1e51120c326cad6f385153bb11ee93b3c216c5fccebfdfbb7ec6cb
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Tue, 14 Apr 2026 00:12:22 GMT
USER gradle
# Tue, 14 Apr 2026 00:12:22 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=2ab2958f2a1e51120c326cad6f385153bb11ee93b3c216c5fccebfdfbb7ec6cb
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --stacktrace --debug --version # buildkit
# Tue, 14 Apr 2026 00:12:22 GMT
USER root
```

-	Layers:
	-	`sha256:f0c6a9d8564d2a3d188b4b49db41fad56fb7e4756edf376c0ff881d93ab0da5e`  
		Last Modified: Mon, 13 Apr 2026 10:09:42 GMT  
		Size: 34.6 MB (34605867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2830c6d09b1072bd202a9bf9f23302896aa2a636fd90662b535f30dc1bab5377`  
		Last Modified: Mon, 13 Apr 2026 23:55:10 GMT  
		Size: 37.5 MB (37460521 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:222d05ab025e2ff555043699b6213f432d0f74ea9e4f6f19e912922df4c1ffe8`  
		Last Modified: Mon, 13 Apr 2026 23:56:59 GMT  
		Size: 145.6 MB (145637135 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ecb86b95eeeaac7c6bb03846ccbba389061bc95154d2c7c04803c4f6fd873a7c`  
		Last Modified: Mon, 13 Apr 2026 23:56:56 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b174d80b420eb3458d77ef4e479edeb777ad804e638543507f66efab6080a7d0`  
		Last Modified: Mon, 13 Apr 2026 23:56:56 GMT  
		Size: 2.3 KB (2291 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50047062ba94e294f764f8f41914c7999ada1d695fcf04ec23c803588d84fe03`  
		Last Modified: Tue, 14 Apr 2026 00:12:41 GMT  
		Size: 1.6 KB (1582 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8abf076f0ae6e79bb595bd26636133e48888daa5059e442bf1857ffb99c99944`  
		Last Modified: Tue, 14 Apr 2026 00:12:43 GMT  
		Size: 38.8 MB (38795501 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9e1136ecd4462e976d3d8c245727cf6a7a6b168207a033ef4d383f596242ba4`  
		Last Modified: Tue, 14 Apr 2026 00:12:45 GMT  
		Size: 137.8 MB (137808335 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:080c5090abb9d7063ff3495805738af61521a008dfed8fb5d7dd241ab0fcf836`  
		Last Modified: Tue, 14 Apr 2026 00:12:41 GMT  
		Size: 25.6 KB (25607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:jdk17-ubi` - unknown; unknown

```console
$ docker pull gradle@sha256:0ca3ef5ac4906fda7fdc509066e9d6f997eafd025293d57d1aaf14958a922731
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.1 MB (7051394 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e337f9678fc33749b4c0b2b670d99767c4ee528a32f7811f643dacb25e76145`

```dockerfile
```

-	Layers:
	-	`sha256:5017852ccedfe6aa1f954b18a11cea45f75d153b6356e56ac22ce924a5c2fc60`  
		Last Modified: Tue, 14 Apr 2026 00:12:41 GMT  
		Size: 7.0 MB (7026944 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2d7a42e7426a5d735fe1051e74dd5d7a223fb5d5f1cc28dfa93a48f8e51337e1`  
		Last Modified: Tue, 14 Apr 2026 00:12:41 GMT  
		Size: 24.4 KB (24450 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:jdk17-ubi` - linux; arm64 variant v8

```console
$ docker pull gradle@sha256:d912fea7470e4d89c32b460a8868157449bcc2e1cf07654896f7deb27a28df0b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **390.7 MB (390668211 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7f58c8ca5ada4127b5c5e8e28ad38fd4232faf9d4116c5720380ac0d0ebdd467`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["gradle"]`

```dockerfile
# Mon, 13 Apr 2026 09:16:57 GMT
LABEL maintainer="Red Hat, Inc."
# Mon, 13 Apr 2026 09:16:57 GMT
LABEL vendor="Red Hat, Inc."
# Mon, 13 Apr 2026 09:16:57 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Mon, 13 Apr 2026 09:16:57 GMT
LABEL com.redhat.component="ubi10-minimal-container"       name="ubi10/ubi-minimal"       version="10.1"       cpe="cpe:/o:redhat:enterprise_linux:10.1"       distribution-scope="public"
# Mon, 13 Apr 2026 09:16:57 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Mon, 13 Apr 2026 09:16:57 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 10."
# Mon, 13 Apr 2026 09:16:57 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 13 Apr 2026 09:16:57 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 13 Apr 2026 09:16:58 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 10 Minimal"
# Mon, 13 Apr 2026 09:16:58 GMT
LABEL io.openshift.expose-services=""
# Mon, 13 Apr 2026 09:16:58 GMT
LABEL io.openshift.tags="minimal rhel10"
# Mon, 13 Apr 2026 09:16:58 GMT
ENV container oci
# Mon, 13 Apr 2026 09:16:58 GMT
COPY dir:e4f84a8805207b4cd31715d3ea15f1b5641e6568c620ec6afade1b03163f2ec3 in /      
# Mon, 13 Apr 2026 09:16:59 GMT
COPY file:5de33b5fc08b00635bccf9134a18978dba13e2250aa51838f9969515a3957847 in /etc/yum.repos.d/.      
# Mon, 13 Apr 2026 09:16:59 GMT
CMD ["/bin/bash"]
# Mon, 13 Apr 2026 09:16:59 GMT
COPY file:595171150af68abc798ea385f7988d74b566aa8e84babff137f00b08b2164683 in /usr/share/buildinfo/content-sets.json      
# Mon, 13 Apr 2026 09:16:59 GMT
COPY file:595171150af68abc798ea385f7988d74b566aa8e84babff137f00b08b2164683 in /root/buildinfo/content_manifests/content-sets.json      
# Mon, 13 Apr 2026 09:16:59 GMT
COPY file:d8a3d61eb5d229916123ad1cb0753c18ec7103c4e50b2eea20333708695dac3e in /usr/share/buildinfo/labels.json      
# Mon, 13 Apr 2026 09:16:59 GMT
COPY file:d8a3d61eb5d229916123ad1cb0753c18ec7103c4e50b2eea20333708695dac3e in /root/buildinfo/labels.json      
# Mon, 13 Apr 2026 09:16:59 GMT
LABEL "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="d468a83fbf6024b899244a1d1179beff08d84a7a" "org.opencontainers.image.revision"="d468a83fbf6024b899244a1d1179beff08d84a7a" "build-date"="2026-04-13T09:16:42Z" "org.opencontainers.image.created"="2026-04-13T09:16:42Z" "release"="1776071394"org.opencontainers.image.revision=d468a83fbf6024b899244a1d1179beff08d84a7a,org.opencontainers.image.created=2026-04-13T09:16:42Z
# Tue, 14 Apr 2026 00:00:22 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 14 Apr 2026 00:00:22 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 14 Apr 2026 00:00:22 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 14 Apr 2026 00:00:22 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en         gnupg2     ;     microdnf clean all # buildkit
# Tue, 14 Apr 2026 00:00:22 GMT
ENV JAVA_VERSION=jdk-17.0.18+8
# Tue, 14 Apr 2026 00:00:28 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='592a6702b3a07a0e0b82cb38aaab149bfce1b0c24d6b57ddb410bd9009333095';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jdk_aarch64_linux_hotspot_17.0.18_8.tar.gz';          ;;        ppc64le)          ESUM='5ab89fbde560e1a09386f389dd7881715b896f49c6e9aa974f72d551337dba5e';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jdk_ppc64le_linux_hotspot_17.0.18_8.tar.gz';          ;;        s390x)          ESUM='3693469655bcfa2fa5e70907245a2b3bc4236db7d9fa1b9feb0ab7abd235da09';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jdk_s390x_linux_hotspot_17.0.18_8.tar.gz';          ;;        x86_64)          ESUM='0c94cbb54325c40dcf026143eb621562017db5525727f2d9131a11250f72c450';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jdk_x64_linux_hotspot_17.0.18_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Tue, 14 Apr 2026 00:00:29 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 14 Apr 2026 00:00:29 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 14 Apr 2026 00:00:29 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 14 Apr 2026 00:00:29 GMT
CMD ["jshell"]
# Tue, 14 Apr 2026 00:09:07 GMT
CMD ["gradle"]
# Tue, 14 Apr 2026 00:09:07 GMT
ENV GRADLE_HOME=/opt/gradle
# Tue, 14 Apr 2026 00:09:07 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 101 gradle     && useradd --system --gid gradle --uid 101 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Tue, 14 Apr 2026 00:09:07 GMT
VOLUME [/home/gradle/.gradle]
# Tue, 14 Apr 2026 00:09:07 GMT
WORKDIR /home/gradle
# Tue, 14 Apr 2026 00:09:12 GMT
RUN set -o errexit -o nounset     && microdnf install -y         make         curl-minimal         wget         tar                 findutils                 unzip         which                 git         git-lfs         subversion     && microdnf clean all         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which svn # buildkit
# Tue, 14 Apr 2026 00:09:12 GMT
ENV GRADLE_VERSION=9.4.1
# Tue, 14 Apr 2026 00:09:12 GMT
ARG GRADLE_DOWNLOAD_SHA256=2ab2958f2a1e51120c326cad6f385153bb11ee93b3c216c5fccebfdfbb7ec6cb
# Tue, 14 Apr 2026 00:09:15 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=2ab2958f2a1e51120c326cad6f385153bb11ee93b3c216c5fccebfdfbb7ec6cb
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Tue, 14 Apr 2026 00:09:15 GMT
USER gradle
# Tue, 14 Apr 2026 00:09:15 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=2ab2958f2a1e51120c326cad6f385153bb11ee93b3c216c5fccebfdfbb7ec6cb
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --stacktrace --debug --version # buildkit
# Tue, 14 Apr 2026 00:09:15 GMT
USER root
```

-	Layers:
	-	`sha256:412494b6387e552210df602617d718496fdcb1172b467aad0caa041e910fd015`  
		Last Modified: Mon, 13 Apr 2026 11:58:02 GMT  
		Size: 32.7 MB (32680047 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fbf5c315dc6b84347848e70019346cbf5158ebdfd6754288a4df4ce24e235bd`  
		Last Modified: Tue, 14 Apr 2026 00:00:48 GMT  
		Size: 37.4 MB (37399600 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0679af7db9379781d058cb409f008f6f27b19c4db9c34482767f176cb17e827`  
		Last Modified: Tue, 14 Apr 2026 00:00:51 GMT  
		Size: 144.4 MB (144446550 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b8df7009e5d68197753e222380e888d41e6823ad719d52a9c5adb5936127e3e`  
		Last Modified: Tue, 14 Apr 2026 00:00:47 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1cf1746f34c741ef59da1dc58541bcd659095d48bde59ac5a441592b978df672`  
		Last Modified: Tue, 14 Apr 2026 00:00:48 GMT  
		Size: 2.3 KB (2291 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6df1d11d320a606a3cadc57340718dd9562dd4deadeb45e8986663dd1af617f`  
		Last Modified: Tue, 14 Apr 2026 00:09:34 GMT  
		Size: 1.6 KB (1583 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6871e7cfd37fd94498c445988b4d7e2fb31f824fbe82f192feaddec98e82475`  
		Last Modified: Tue, 14 Apr 2026 00:09:35 GMT  
		Size: 38.3 MB (38300315 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d54f06992ae692d3286264b72371ec9e057f66fdfd5b65a23a37de3005d290b`  
		Last Modified: Tue, 14 Apr 2026 00:09:37 GMT  
		Size: 137.8 MB (137808331 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4beb99eb8ac31d9455544064d9af151ba2d5a07446518050304bd9d4951068be`  
		Last Modified: Tue, 14 Apr 2026 00:09:34 GMT  
		Size: 29.3 KB (29336 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:jdk17-ubi` - unknown; unknown

```console
$ docker pull gradle@sha256:a275217d10e8cf529fa5ecff214f0a27c841f0c9346ae0a9048207617f8d8fcb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 MB (7049848 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1481d1760986d711c0976a0c325930acf64f586bcf381fe2666369d1c8cf86f9`

```dockerfile
```

-	Layers:
	-	`sha256:8d82c32150cf4fcf40341bd3dc1d62997835625a60f364804fc294d5dac8eb3e`  
		Last Modified: Tue, 14 Apr 2026 00:09:34 GMT  
		Size: 7.0 MB (7025200 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3dee9e5120576d4fd9a8fadb12ac2a3e11df5cef460de3025b6b57f457582536`  
		Last Modified: Tue, 14 Apr 2026 00:09:34 GMT  
		Size: 24.6 KB (24648 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:jdk17-ubi` - linux; ppc64le

```console
$ docker pull gradle@sha256:94a0b37fb665eee327a055fff4dd436b313e52b1179d7240e651ab1c2112aefd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **401.7 MB (401729496 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c3356a3c6c3ad487208caa09c4ca169c00b7f0fce87ad291972123acd6585ad`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["gradle"]`

```dockerfile
# Mon, 13 Apr 2026 09:15:35 GMT
LABEL maintainer="Red Hat, Inc."
# Mon, 13 Apr 2026 09:15:35 GMT
LABEL vendor="Red Hat, Inc."
# Mon, 13 Apr 2026 09:15:35 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Mon, 13 Apr 2026 09:15:35 GMT
LABEL com.redhat.component="ubi10-minimal-container"       name="ubi10/ubi-minimal"       version="10.1"       cpe="cpe:/o:redhat:enterprise_linux:10.1"       distribution-scope="public"
# Mon, 13 Apr 2026 09:15:35 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Mon, 13 Apr 2026 09:15:35 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 10."
# Mon, 13 Apr 2026 09:15:35 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 13 Apr 2026 09:15:35 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 13 Apr 2026 09:15:35 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 10 Minimal"
# Mon, 13 Apr 2026 09:15:35 GMT
LABEL io.openshift.expose-services=""
# Mon, 13 Apr 2026 09:15:35 GMT
LABEL io.openshift.tags="minimal rhel10"
# Mon, 13 Apr 2026 09:15:35 GMT
ENV container oci
# Mon, 13 Apr 2026 09:15:36 GMT
COPY dir:d5bea9ef78808f560c142c54c074655a9c233520184b1046a8e6bef1925013a7 in /      
# Mon, 13 Apr 2026 09:15:36 GMT
COPY file:5de33b5fc08b00635bccf9134a18978dba13e2250aa51838f9969515a3957847 in /etc/yum.repos.d/.      
# Mon, 13 Apr 2026 09:15:36 GMT
CMD ["/bin/bash"]
# Mon, 13 Apr 2026 09:15:36 GMT
COPY file:595171150af68abc798ea385f7988d74b566aa8e84babff137f00b08b2164683 in /usr/share/buildinfo/content-sets.json      
# Mon, 13 Apr 2026 09:15:36 GMT
COPY file:595171150af68abc798ea385f7988d74b566aa8e84babff137f00b08b2164683 in /root/buildinfo/content_manifests/content-sets.json      
# Mon, 13 Apr 2026 09:15:36 GMT
COPY file:ef9ee329c018a2f17a5a5c4723c1803a667108705d8c3d16152fdcce104fca5d in /usr/share/buildinfo/labels.json      
# Mon, 13 Apr 2026 09:15:36 GMT
COPY file:ef9ee329c018a2f17a5a5c4723c1803a667108705d8c3d16152fdcce104fca5d in /root/buildinfo/labels.json      
# Mon, 13 Apr 2026 09:15:37 GMT
LABEL "architecture"="ppc64le" "vcs-type"="git" "vcs-ref"="d468a83fbf6024b899244a1d1179beff08d84a7a" "org.opencontainers.image.revision"="d468a83fbf6024b899244a1d1179beff08d84a7a" "build-date"="2026-04-13T09:15:24Z" "org.opencontainers.image.created"="2026-04-13T09:15:24Z" "release"="1776071394"org.opencontainers.image.revision=d468a83fbf6024b899244a1d1179beff08d84a7a,org.opencontainers.image.created=2026-04-13T09:15:24Z
# Mon, 13 Apr 2026 23:56:07 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 13 Apr 2026 23:56:07 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 13 Apr 2026 23:56:07 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 13 Apr 2026 23:56:07 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en         gnupg2     ;     microdnf clean all # buildkit
# Mon, 13 Apr 2026 23:56:07 GMT
ENV JAVA_VERSION=jdk-17.0.18+8
# Mon, 13 Apr 2026 23:57:56 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='592a6702b3a07a0e0b82cb38aaab149bfce1b0c24d6b57ddb410bd9009333095';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jdk_aarch64_linux_hotspot_17.0.18_8.tar.gz';          ;;        ppc64le)          ESUM='5ab89fbde560e1a09386f389dd7881715b896f49c6e9aa974f72d551337dba5e';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jdk_ppc64le_linux_hotspot_17.0.18_8.tar.gz';          ;;        s390x)          ESUM='3693469655bcfa2fa5e70907245a2b3bc4236db7d9fa1b9feb0ab7abd235da09';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jdk_s390x_linux_hotspot_17.0.18_8.tar.gz';          ;;        x86_64)          ESUM='0c94cbb54325c40dcf026143eb621562017db5525727f2d9131a11250f72c450';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jdk_x64_linux_hotspot_17.0.18_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Mon, 13 Apr 2026 23:58:00 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Mon, 13 Apr 2026 23:58:00 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Mon, 13 Apr 2026 23:58:00 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Mon, 13 Apr 2026 23:58:00 GMT
CMD ["jshell"]
# Tue, 14 Apr 2026 00:16:07 GMT
CMD ["gradle"]
# Tue, 14 Apr 2026 00:16:07 GMT
ENV GRADLE_HOME=/opt/gradle
# Tue, 14 Apr 2026 00:16:07 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 101 gradle     && useradd --system --gid gradle --uid 101 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Tue, 14 Apr 2026 00:16:07 GMT
VOLUME [/home/gradle/.gradle]
# Tue, 14 Apr 2026 00:16:08 GMT
WORKDIR /home/gradle
# Tue, 14 Apr 2026 00:16:37 GMT
RUN set -o errexit -o nounset     && microdnf install -y         make         curl-minimal         wget         tar                 findutils                 unzip         which                 git         git-lfs         subversion     && microdnf clean all         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which svn # buildkit
# Tue, 14 Apr 2026 00:16:37 GMT
ENV GRADLE_VERSION=9.4.1
# Tue, 14 Apr 2026 00:16:37 GMT
ARG GRADLE_DOWNLOAD_SHA256=2ab2958f2a1e51120c326cad6f385153bb11ee93b3c216c5fccebfdfbb7ec6cb
# Tue, 14 Apr 2026 00:16:41 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=2ab2958f2a1e51120c326cad6f385153bb11ee93b3c216c5fccebfdfbb7ec6cb
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Tue, 14 Apr 2026 00:16:41 GMT
USER gradle
# Tue, 14 Apr 2026 00:16:43 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=2ab2958f2a1e51120c326cad6f385153bb11ee93b3c216c5fccebfdfbb7ec6cb
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --stacktrace --debug --version # buildkit
# Tue, 14 Apr 2026 00:16:43 GMT
USER root
```

-	Layers:
	-	`sha256:6ab9c9492755280705c94f3f242c73ae33058d432445b818684063f12da4648d`  
		Last Modified: Mon, 13 Apr 2026 12:12:34 GMT  
		Size: 38.7 MB (38703789 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6635d84f1d74aebc8b054009ce82709f7f82d78dc2ec7a147aca9cfbbd6cd6ba`  
		Last Modified: Mon, 13 Apr 2026 23:56:49 GMT  
		Size: 39.2 MB (39213284 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72038a8b6745b95e07716812cdbfb8690d73359aea1377a6910cb7a35742a338`  
		Last Modified: Mon, 13 Apr 2026 23:58:37 GMT  
		Size: 145.5 MB (145460003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1017ab383e4f7bb81a5daae6d51811a2194ac735c6cc4f9bb999256455d8e4c2`  
		Last Modified: Mon, 13 Apr 2026 23:58:34 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0435081863cc9ebba573421eb7af7062734d0d500d2c379c8a540b7a5a8894ec`  
		Last Modified: Mon, 13 Apr 2026 23:58:34 GMT  
		Size: 2.3 KB (2288 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3c9a717ee6f51d2aa62800baf58b779cd72bb2cfb306bd531036a230edfb14d`  
		Last Modified: Tue, 14 Apr 2026 00:17:29 GMT  
		Size: 1.6 KB (1587 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26bb327807deebc07bd591e0ab2d7681a61f36cabfe8f341248d52127558306f`  
		Last Modified: Tue, 14 Apr 2026 00:17:31 GMT  
		Size: 40.5 MB (40539677 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:387fccefbdbd26f5b50e092a557c0cb8cb8bf4a097fd7560eacd75a4d9d08ba9`  
		Last Modified: Tue, 14 Apr 2026 00:17:34 GMT  
		Size: 137.8 MB (137808330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b18da5063b8d4949bfc1554991cd8b077857ed5741bf92049e00a8df23b39df6`  
		Last Modified: Tue, 14 Apr 2026 00:17:29 GMT  
		Size: 377.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:jdk17-ubi` - unknown; unknown

```console
$ docker pull gradle@sha256:131a5a8ebfb2b31cd190e565c07c7260664515f89c9ef38419cd938a5ce3c3d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 MB (7042885 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4720834b61a12f669d4e9e9c1859975d98d52889225a9572cefe8c8566915755`

```dockerfile
```

-	Layers:
	-	`sha256:640f0000ba153b012e2c963da693f61955d001bdea987d8d59ad9fd66388aca9`  
		Last Modified: Tue, 14 Apr 2026 00:17:29 GMT  
		Size: 7.0 MB (7018362 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:40d412c1a5778e2b84f5a016e39858ae78995f166d0efa298aa4b6ed39675130`  
		Last Modified: Tue, 14 Apr 2026 00:17:29 GMT  
		Size: 24.5 KB (24523 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:jdk17-ubi` - linux; s390x

```console
$ docker pull gradle@sha256:2195a1b68319e72413304996f5c448fbdf06860486e14dc9a7e079bc72196d38
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **386.6 MB (386586333 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d210a0d3cf9d2bb3ce69791a411ddc79747cbe5a4181f95fd3f30a4e8c0b7c7a`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["gradle"]`

```dockerfile
# Thu, 26 Mar 2026 17:28:54 GMT
LABEL maintainer="Red Hat, Inc."
# Thu, 26 Mar 2026 17:28:54 GMT
LABEL vendor="Red Hat, Inc."
# Thu, 26 Mar 2026 17:28:54 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Thu, 26 Mar 2026 17:28:54 GMT
LABEL com.redhat.component="ubi10-minimal-container"       name="ubi10/ubi-minimal"       version="10.1"       cpe="cpe:/o:redhat:enterprise_linux:10.1"       distribution-scope="public"
# Thu, 26 Mar 2026 17:28:54 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Thu, 26 Mar 2026 17:28:54 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 10."
# Thu, 26 Mar 2026 17:28:54 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 26 Mar 2026 17:28:54 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 26 Mar 2026 17:28:54 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 10 Minimal"
# Thu, 26 Mar 2026 17:28:54 GMT
LABEL io.openshift.expose-services=""
# Thu, 26 Mar 2026 17:28:54 GMT
LABEL io.openshift.tags="minimal rhel10"
# Thu, 26 Mar 2026 17:28:55 GMT
ENV container oci
# Thu, 26 Mar 2026 17:28:55 GMT
COPY dir:94a3048ecdc388a9fe69dc605a5ee32b82678da3107c34d9f886aca0d5d2e171 in /      
# Thu, 26 Mar 2026 17:28:55 GMT
COPY file:5de33b5fc08b00635bccf9134a18978dba13e2250aa51838f9969515a3957847 in /etc/yum.repos.d/.      
# Thu, 26 Mar 2026 17:28:55 GMT
CMD ["/bin/bash"]
# Thu, 26 Mar 2026 17:28:55 GMT
COPY file:595171150af68abc798ea385f7988d74b566aa8e84babff137f00b08b2164683 in /usr/share/buildinfo/content-sets.json      
# Thu, 26 Mar 2026 17:28:55 GMT
COPY file:595171150af68abc798ea385f7988d74b566aa8e84babff137f00b08b2164683 in /root/buildinfo/content_manifests/content-sets.json      
# Thu, 26 Mar 2026 17:28:55 GMT
COPY file:4fd670c85c1bcf73f03c7e85a75e911c58dd6829a2070a9da8f858286ab68657 in /usr/share/buildinfo/labels.json      
# Thu, 26 Mar 2026 17:28:55 GMT
COPY file:4fd670c85c1bcf73f03c7e85a75e911c58dd6829a2070a9da8f858286ab68657 in /root/buildinfo/labels.json      
# Thu, 26 Mar 2026 17:28:56 GMT
LABEL "architecture"="s390x" "vcs-type"="git" "vcs-ref"="4d17df4ea3ff25815cca2550bc445280420af0a9" "org.opencontainers.image.revision"="4d17df4ea3ff25815cca2550bc445280420af0a9" "build-date"="2026-03-26T17:28:13Z" "org.opencontainers.image.created"="2026-03-26T17:28:13Z" "release"="1774545417"org.opencontainers.image.revision=4d17df4ea3ff25815cca2550bc445280420af0a9,org.opencontainers.image.created=2026-03-26T17:28:13Z
# Fri, 27 Mar 2026 18:59:32 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 27 Mar 2026 18:59:32 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 27 Mar 2026 18:59:32 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 27 Mar 2026 18:59:32 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en         gnupg2     ;     microdnf clean all # buildkit
# Fri, 27 Mar 2026 18:59:32 GMT
ENV JAVA_VERSION=jdk-17.0.18+8
# Fri, 27 Mar 2026 18:59:37 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='592a6702b3a07a0e0b82cb38aaab149bfce1b0c24d6b57ddb410bd9009333095';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jdk_aarch64_linux_hotspot_17.0.18_8.tar.gz';          ;;        ppc64le)          ESUM='5ab89fbde560e1a09386f389dd7881715b896f49c6e9aa974f72d551337dba5e';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jdk_ppc64le_linux_hotspot_17.0.18_8.tar.gz';          ;;        s390x)          ESUM='3693469655bcfa2fa5e70907245a2b3bc4236db7d9fa1b9feb0ab7abd235da09';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jdk_s390x_linux_hotspot_17.0.18_8.tar.gz';          ;;        x86_64)          ESUM='0c94cbb54325c40dcf026143eb621562017db5525727f2d9131a11250f72c450';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jdk_x64_linux_hotspot_17.0.18_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Fri, 27 Mar 2026 18:59:38 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Fri, 27 Mar 2026 18:59:38 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Fri, 27 Mar 2026 18:59:38 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Fri, 27 Mar 2026 18:59:38 GMT
CMD ["jshell"]
# Fri, 27 Mar 2026 19:10:23 GMT
CMD ["gradle"]
# Fri, 27 Mar 2026 19:10:23 GMT
ENV GRADLE_HOME=/opt/gradle
# Fri, 27 Mar 2026 19:10:23 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 101 gradle     && useradd --system --gid gradle --uid 101 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Fri, 27 Mar 2026 19:10:23 GMT
VOLUME [/home/gradle/.gradle]
# Fri, 27 Mar 2026 19:10:23 GMT
WORKDIR /home/gradle
# Fri, 27 Mar 2026 19:10:29 GMT
RUN set -o errexit -o nounset     && microdnf install -y         make         curl-minimal         wget         tar                 findutils                 unzip         which                 git         git-lfs         subversion     && microdnf clean all         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which svn # buildkit
# Fri, 27 Mar 2026 19:10:29 GMT
ENV GRADLE_VERSION=9.4.1
# Fri, 27 Mar 2026 19:10:29 GMT
ARG GRADLE_DOWNLOAD_SHA256=2ab2958f2a1e51120c326cad6f385153bb11ee93b3c216c5fccebfdfbb7ec6cb
# Fri, 27 Mar 2026 19:10:33 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=2ab2958f2a1e51120c326cad6f385153bb11ee93b3c216c5fccebfdfbb7ec6cb
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Fri, 27 Mar 2026 19:10:33 GMT
USER gradle
# Fri, 27 Mar 2026 19:10:34 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=2ab2958f2a1e51120c326cad6f385153bb11ee93b3c216c5fccebfdfbb7ec6cb
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --stacktrace --debug --version # buildkit
# Fri, 27 Mar 2026 19:10:34 GMT
USER root
```

-	Layers:
	-	`sha256:9c01cab36040f3f8f1c78284c2d60452730d51f09eb8623c854a44417db02f17`  
		Last Modified: Thu, 26 Mar 2026 18:15:05 GMT  
		Size: 34.4 MB (34434323 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e92e629fa493b439430775fefb78b6ea7e4f3d723384615f003b8a5913c0ef72`  
		Last Modified: Fri, 27 Mar 2026 19:00:08 GMT  
		Size: 37.8 MB (37835076 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4cf990bea875a90cfb3eb653ef7ea88651ed9063bd030627325ecef3f359339e`  
		Last Modified: Fri, 27 Mar 2026 19:00:09 GMT  
		Size: 135.6 MB (135629137 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ecea4c23fabccc245ef16395a826101857be3d507ab1e9638a3a20729e27beb`  
		Last Modified: Fri, 27 Mar 2026 19:00:07 GMT  
		Size: 130.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de2bb7bdc5a6918b38852e1f8f2e253d0862c8ebb657b8bed981c8abd956bae7`  
		Last Modified: Fri, 27 Mar 2026 19:00:09 GMT  
		Size: 2.3 KB (2289 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9eb9ee2e0fffe7e08959ace133a6b6b9ca5c7fa83795caf5380a21ad7ed67fef`  
		Last Modified: Fri, 27 Mar 2026 19:11:02 GMT  
		Size: 1.6 KB (1583 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5629f994adbd088fc735303e3c032ab55c8dee60b733c0511e780f110ae2b690`  
		Last Modified: Fri, 27 Mar 2026 19:11:03 GMT  
		Size: 40.9 MB (40875049 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02cf3622484955167080d1248f880804cac348ffdb5d962434fa589ce29083f3`  
		Last Modified: Fri, 27 Mar 2026 19:11:05 GMT  
		Size: 137.8 MB (137808337 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8d952c5b6cbdb9939105dd4356168c8cf2a28e846d654e7de1dab4a576c2b5d`  
		Last Modified: Fri, 27 Mar 2026 19:11:02 GMT  
		Size: 377.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:jdk17-ubi` - unknown; unknown

```console
$ docker pull gradle@sha256:9661a5dc1a2966c1c7c09a0bb4bdfbd085d3f9a45c3ceda1e1ea1616d1ff02be
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 MB (7032024 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7de16aed4bd1f117b138223329c175827f7e11535460496e3da013808dfd8e1a`

```dockerfile
```

-	Layers:
	-	`sha256:d327fa3f6273da34ea23ce988c92e6b1f2a92b6d968ae462b6688cdb98382918`  
		Last Modified: Fri, 27 Mar 2026 19:11:02 GMT  
		Size: 7.0 MB (7007575 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:49417c8da10b435b1eab9184a159095b2632c36e60395c950a9431a5b77fdcae`  
		Last Modified: Fri, 27 Mar 2026 19:11:02 GMT  
		Size: 24.4 KB (24449 bytes)  
		MIME: application/vnd.in-toto+json
