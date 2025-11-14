## `gradle:7-jdk8-ubi-minimal`

```console
$ docker pull gradle@sha256:248c14bce4f22e36927a6fbadd2b82561bcbd11bf7543f88422775cc3087ac0e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `gradle:7-jdk8-ubi-minimal` - linux; amd64

```console
$ docker pull gradle@sha256:f46c6f2c3ba08f12da7c2e462aa0c22ac0310d2e1dacdfd521bc2bd22d8a6fbe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **291.0 MB (290981221 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e4c27f2a92e3f02e39f7e292838936b2eb8108a5b87d00631bbc0724d2f41e4`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["gradle"]`

```dockerfile
# Wed, 12 Nov 2025 14:07:22 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 12 Nov 2025 14:07:22 GMT
LABEL vendor="Red Hat, Inc."
# Wed, 12 Nov 2025 14:07:22 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Wed, 12 Nov 2025 14:07:22 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.7"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Wed, 12 Nov 2025 14:07:22 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 12 Nov 2025 14:07:23 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Wed, 12 Nov 2025 14:07:23 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 12 Nov 2025 14:07:23 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 12 Nov 2025 14:07:23 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Wed, 12 Nov 2025 14:07:23 GMT
LABEL io.openshift.expose-services=""
# Wed, 12 Nov 2025 14:07:23 GMT
LABEL io.openshift.tags="minimal rhel9"
# Wed, 12 Nov 2025 14:07:23 GMT
ENV container oci
# Wed, 12 Nov 2025 14:07:24 GMT
COPY dir:fd8f02dabe7ae9790ce0638d1f9e9f60d460b3580843d39cb4dee8e471c106cc in /      
# Wed, 12 Nov 2025 14:07:24 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Wed, 12 Nov 2025 14:07:24 GMT
CMD ["/bin/bash"]
# Wed, 12 Nov 2025 14:07:24 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /usr/share/buildinfo/content-sets.json      
# Wed, 12 Nov 2025 14:07:24 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /root/buildinfo/content_manifests/content-sets.json      
# Wed, 12 Nov 2025 14:07:24 GMT
COPY file:b446d7ec96d8598bdd079305b40e4e5a0c1e0d484658876cab87a4393ac52954 in /usr/share/buildinfo/labels.json      
# Wed, 12 Nov 2025 14:07:24 GMT
COPY file:b446d7ec96d8598bdd079305b40e4e5a0c1e0d484658876cab87a4393ac52954 in /root/buildinfo/labels.json      
# Wed, 12 Nov 2025 14:07:24 GMT
LABEL "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="09400c6ea1039bbeb186633c5815980c077ced2a" "org.opencontainers.image.revision"="09400c6ea1039bbeb186633c5815980c077ced2a" "build-date"="2025-11-12T14:07:06Z" "release"="1762956380"org.opencontainers.image.revision=09400c6ea1039bbeb186633c5815980c077ced2a
# Fri, 14 Nov 2025 01:12:18 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 14 Nov 2025 01:12:18 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 14 Nov 2025 01:12:18 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 14 Nov 2025 01:12:18 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en     ;     microdnf clean all # buildkit
# Fri, 14 Nov 2025 01:12:18 GMT
ENV JAVA_VERSION=jdk8u472-b08
# Fri, 14 Nov 2025 01:12:22 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='e2aff19d85d2441e409d6cbdf12ef7c2acabb0de73bca4207947135dcaa935a2';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u472-b08/OpenJDK8U-jdk_aarch64_linux_hotspot_8u472b08.tar.gz';          ;;        ppc64le)          ESUM='eaf57a4564265583b0641c878bea8943d27ef110c096868f686dae179fb45d8f';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u472-b08/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u472b08.tar.gz';          ;;        x86_64)          ESUM='5becaa4ac660e844c5a39e2ebc39ff5ac824c37ff1b625af8c8b111dc13c3592';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u472-b08/OpenJDK8U-jdk_x64_linux_hotspot_8u472b08.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip; # buildkit
# Fri, 14 Nov 2025 01:12:22 GMT
RUN set -eux;     echo "Verifying install ...";     echo "javac -version"; javac -version;     echo "java -version"; java -version;     echo "Complete." # buildkit
# Fri, 14 Nov 2025 01:12:22 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Fri, 14 Nov 2025 01:12:22 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Fri, 14 Nov 2025 02:18:13 GMT
CMD ["gradle"]
# Fri, 14 Nov 2025 02:18:13 GMT
ENV GRADLE_HOME=/opt/gradle
# Fri, 14 Nov 2025 02:18:13 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 101 gradle     && useradd --system --gid gradle --uid 101 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Fri, 14 Nov 2025 02:18:13 GMT
VOLUME [/home/gradle/.gradle]
# Fri, 14 Nov 2025 02:18:13 GMT
WORKDIR /home/gradle
# Fri, 14 Nov 2025 02:18:17 GMT
RUN set -o errexit -o nounset     && microdnf install -y         make                 findutils                 unzip         which                 git         git-lfs         subversion     && microdnf clean all         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which svn # buildkit
# Fri, 14 Nov 2025 02:18:17 GMT
ENV GRADLE_VERSION=7.6.6
# Fri, 14 Nov 2025 02:18:17 GMT
ARG GRADLE_DOWNLOAD_SHA256=673d9776f303bc7048fc3329d232d6ebf1051b07893bd9d11616fad9a8673be0
# Fri, 14 Nov 2025 02:18:20 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=673d9776f303bc7048fc3329d232d6ebf1051b07893bd9d11616fad9a8673be0
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Fri, 14 Nov 2025 02:18:20 GMT
USER gradle
# Fri, 14 Nov 2025 02:18:20 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=673d9776f303bc7048fc3329d232d6ebf1051b07893bd9d11616fad9a8673be0
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Fri, 14 Nov 2025 02:18:20 GMT
USER root
```

-	Layers:
	-	`sha256:179ba4be1de0701de7b39988f2989858194723f60b56b12f8d9438358e471a73`  
		Last Modified: Wed, 12 Nov 2025 15:07:23 GMT  
		Size: 40.0 MB (40048414 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac048aa544114f65cbc2475ace061d7bf87a99852cf2ff1ff4a6d6c63d56740d`  
		Last Modified: Fri, 14 Nov 2025 01:12:49 GMT  
		Size: 30.6 MB (30635534 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04f0853ffda785c614fd4197eec9ac25577d27beadb89514c2fee3531b5450fa`  
		Last Modified: Fri, 14 Nov 2025 01:12:53 GMT  
		Size: 54.7 MB (54733842 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ccc61ea85954dcb5e700d5f0a450aa0a27ec257609bd99de265434304de9c86`  
		Last Modified: Fri, 14 Nov 2025 01:12:44 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:452d084b44787c92794601bba6fa5b8e377105f7a161320fe3fc86ac56616944`  
		Last Modified: Fri, 14 Nov 2025 01:12:44 GMT  
		Size: 2.3 KB (2314 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16ddc7d0fe590ce6f509b07a985183783142b5bdd07300584b023074e65b4f4a`  
		Last Modified: Fri, 14 Nov 2025 02:18:48 GMT  
		Size: 1.7 KB (1706 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11a5a8038af201369cdf7d19db27682623c259feb11450ee92fbf276b0ded54f`  
		Last Modified: Fri, 14 Nov 2025 02:18:51 GMT  
		Size: 37.0 MB (37034892 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1826f5cdb6a42b391c4e13e668accd2de71bb2f78cb38cd4d9d6ff400387a534`  
		Last Modified: Fri, 14 Nov 2025 02:18:42 GMT  
		Size: 128.5 MB (128469469 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67eee8e25ac644751ad9181898ed6fdaf327c947854432df314881001408ee90`  
		Last Modified: Fri, 14 Nov 2025 02:18:48 GMT  
		Size: 54.9 KB (54891 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:7-jdk8-ubi-minimal` - unknown; unknown

```console
$ docker pull gradle@sha256:0ed5f306150363c990a0f7033f0dac6b002eb273b1784c05dc1096cbd5365683
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5458473 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a4e63ce25fe5d4616eceaae735fb4fa9d2c6cab73e883014e3a31ab578d4b84`

```dockerfile
```

-	Layers:
	-	`sha256:13bc02c3600a8860310ed9fb0261904460626101b993fb392340872445fbf47b`  
		Last Modified: Fri, 14 Nov 2025 03:22:58 GMT  
		Size: 5.4 MB (5434913 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f9719da52b42558a0d28036058e4d9488f3af146e7dd6da869ec469dcc83b7a7`  
		Last Modified: Fri, 14 Nov 2025 03:22:59 GMT  
		Size: 23.6 KB (23560 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:7-jdk8-ubi-minimal` - linux; arm64 variant v8

```console
$ docker pull gradle@sha256:669f8843678bebc37eb689b3d75d78239ae26851413e5a551c54cfd25236f4cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **287.9 MB (287880658 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c0e7c55b0103aa53cd97859b79cb15419dba9a121fc3b06886cfc581cfbb08a2`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["gradle"]`

```dockerfile
# Wed, 12 Nov 2025 14:10:10 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 12 Nov 2025 14:10:10 GMT
LABEL vendor="Red Hat, Inc."
# Wed, 12 Nov 2025 14:10:10 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Wed, 12 Nov 2025 14:10:10 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.7"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Wed, 12 Nov 2025 14:10:10 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 12 Nov 2025 14:10:10 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Wed, 12 Nov 2025 14:10:10 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 12 Nov 2025 14:10:11 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 12 Nov 2025 14:10:11 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Wed, 12 Nov 2025 14:10:11 GMT
LABEL io.openshift.expose-services=""
# Wed, 12 Nov 2025 14:10:11 GMT
LABEL io.openshift.tags="minimal rhel9"
# Wed, 12 Nov 2025 14:10:11 GMT
ENV container oci
# Wed, 12 Nov 2025 14:10:11 GMT
COPY dir:306690a4b33e0c2c47cf50b466ed471eb7ab206a490a8f74fd060934dfe49241 in /      
# Wed, 12 Nov 2025 14:10:12 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Wed, 12 Nov 2025 14:10:12 GMT
CMD ["/bin/bash"]
# Wed, 12 Nov 2025 14:10:12 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /usr/share/buildinfo/content-sets.json      
# Wed, 12 Nov 2025 14:10:12 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /root/buildinfo/content_manifests/content-sets.json      
# Wed, 12 Nov 2025 14:10:12 GMT
COPY file:0fb7b120ef84051a76f1b80ab468bcf42e6749f2d4faca4621e99b2ad0f6bb9a in /usr/share/buildinfo/labels.json      
# Wed, 12 Nov 2025 14:10:12 GMT
COPY file:0fb7b120ef84051a76f1b80ab468bcf42e6749f2d4faca4621e99b2ad0f6bb9a in /root/buildinfo/labels.json      
# Wed, 12 Nov 2025 14:10:12 GMT
LABEL "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="09400c6ea1039bbeb186633c5815980c077ced2a" "org.opencontainers.image.revision"="09400c6ea1039bbeb186633c5815980c077ced2a" "build-date"="2025-11-12T14:09:54Z" "release"="1762956380"org.opencontainers.image.revision=09400c6ea1039bbeb186633c5815980c077ced2a
# Fri, 14 Nov 2025 01:28:14 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 14 Nov 2025 01:28:14 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 14 Nov 2025 01:28:14 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 14 Nov 2025 01:28:14 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en     ;     microdnf clean all # buildkit
# Fri, 14 Nov 2025 01:28:14 GMT
ENV JAVA_VERSION=jdk8u472-b08
# Fri, 14 Nov 2025 01:28:46 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='e2aff19d85d2441e409d6cbdf12ef7c2acabb0de73bca4207947135dcaa935a2';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u472-b08/OpenJDK8U-jdk_aarch64_linux_hotspot_8u472b08.tar.gz';          ;;        ppc64le)          ESUM='eaf57a4564265583b0641c878bea8943d27ef110c096868f686dae179fb45d8f';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u472-b08/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u472b08.tar.gz';          ;;        x86_64)          ESUM='5becaa4ac660e844c5a39e2ebc39ff5ac824c37ff1b625af8c8b111dc13c3592';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u472-b08/OpenJDK8U-jdk_x64_linux_hotspot_8u472b08.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip; # buildkit
# Fri, 14 Nov 2025 01:28:46 GMT
RUN set -eux;     echo "Verifying install ...";     echo "javac -version"; javac -version;     echo "java -version"; java -version;     echo "Complete." # buildkit
# Fri, 14 Nov 2025 01:28:46 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Fri, 14 Nov 2025 01:28:46 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Fri, 14 Nov 2025 02:22:09 GMT
CMD ["gradle"]
# Fri, 14 Nov 2025 02:22:09 GMT
ENV GRADLE_HOME=/opt/gradle
# Fri, 14 Nov 2025 02:22:09 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 101 gradle     && useradd --system --gid gradle --uid 101 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Fri, 14 Nov 2025 02:22:09 GMT
VOLUME [/home/gradle/.gradle]
# Fri, 14 Nov 2025 02:22:09 GMT
WORKDIR /home/gradle
# Fri, 14 Nov 2025 02:22:13 GMT
RUN set -o errexit -o nounset     && microdnf install -y         make                 findutils                 unzip         which                 git         git-lfs         subversion     && microdnf clean all         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which svn # buildkit
# Fri, 14 Nov 2025 02:22:13 GMT
ENV GRADLE_VERSION=7.6.6
# Fri, 14 Nov 2025 02:22:13 GMT
ARG GRADLE_DOWNLOAD_SHA256=673d9776f303bc7048fc3329d232d6ebf1051b07893bd9d11616fad9a8673be0
# Fri, 14 Nov 2025 02:22:16 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=673d9776f303bc7048fc3329d232d6ebf1051b07893bd9d11616fad9a8673be0
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Fri, 14 Nov 2025 02:22:16 GMT
USER gradle
# Fri, 14 Nov 2025 02:22:16 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=673d9776f303bc7048fc3329d232d6ebf1051b07893bd9d11616fad9a8673be0
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Fri, 14 Nov 2025 02:22:16 GMT
USER root
```

-	Layers:
	-	`sha256:e01bb2a7f0e8ff512f86254e984d1cf0bdc9b357f1e0f0f61d352832dc12a646`  
		Last Modified: Wed, 12 Nov 2025 15:16:35 GMT  
		Size: 38.2 MB (38221043 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a38ff535b7d17e017378b2198c1d1e6ff9a6aa2a395b8c4f6f05efc633d957f4`  
		Last Modified: Fri, 14 Nov 2025 01:28:39 GMT  
		Size: 30.9 MB (30885412 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53d58881ca3b1c3129b3b4c49a7f73d5bca5eb8d1bc39f206193268f3eeb2993`  
		Last Modified: Fri, 14 Nov 2025 01:29:11 GMT  
		Size: 53.8 MB (53815600 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e938aa146127f2ae85c1fb6df02b164a975e2aa5c9d971ad0d31945952c8c6f7`  
		Last Modified: Fri, 14 Nov 2025 01:29:04 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0741d8928df2e6d3de2625f41a67b4214f6e686fe082a9c28a972cd8d723981`  
		Last Modified: Fri, 14 Nov 2025 01:29:04 GMT  
		Size: 2.3 KB (2314 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d845019ce7f002bd6c0f3891d3644baf6fcf80a1d67405f62dc2ab2f557a949`  
		Last Modified: Fri, 14 Nov 2025 02:22:40 GMT  
		Size: 1.7 KB (1709 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57929525098a81059956f071c5c4a4977c723326020fc9d2e229f1a0e1083727`  
		Last Modified: Fri, 14 Nov 2025 02:22:45 GMT  
		Size: 36.4 MB (36425454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e028f1fbe8d6904317da428d57ee0a07c615d782657c1e0a4172083fc9b544f4`  
		Last Modified: Fri, 14 Nov 2025 02:22:36 GMT  
		Size: 128.5 MB (128469449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e94bd4df73fedf263af5832b70815385c00e565fea409ba2bc5fe151b55d9e64`  
		Last Modified: Fri, 14 Nov 2025 02:22:40 GMT  
		Size: 59.5 KB (59518 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:7-jdk8-ubi-minimal` - unknown; unknown

```console
$ docker pull gradle@sha256:7cd6ae3cfc5f1f98b6b344d428bae469ca5f092da4d2271efb34f6c9e3d59760
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5458750 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b0d9d2dec3c07a22fbf6a71749483b45e54e61a2a6bd71e945eda75bbd0eba59`

```dockerfile
```

-	Layers:
	-	`sha256:a6fffa9427e400d8460380890e566b7f9524ac3156f3e867500b421bf1046a74`  
		Last Modified: Fri, 14 Nov 2025 03:23:04 GMT  
		Size: 5.4 MB (5435017 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4256d16b1a9816284bdda7648629b57e4fd473519988a133a039708cc92c76ea`  
		Last Modified: Fri, 14 Nov 2025 03:23:05 GMT  
		Size: 23.7 KB (23733 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:7-jdk8-ubi-minimal` - linux; ppc64le

```console
$ docker pull gradle@sha256:a1db8840a0cf840d1e2b3c1759aae54bf429217fc260495eaed5bd8fe3cfb342
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **293.5 MB (293546124 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:88689b36e954362e409a224d2d24d183c98eb4f9a71b6d23bf080e056d4846e9`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["gradle"]`

```dockerfile
# Mon, 03 Nov 2025 14:29:54 GMT
LABEL maintainer="Red Hat, Inc."
# Mon, 03 Nov 2025 14:29:54 GMT
LABEL vendor="Red Hat, Inc."
# Mon, 03 Nov 2025 14:29:54 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Mon, 03 Nov 2025 14:29:54 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.7"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Mon, 03 Nov 2025 14:29:54 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Mon, 03 Nov 2025 14:29:54 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Mon, 03 Nov 2025 14:29:54 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 03 Nov 2025 14:29:54 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 03 Nov 2025 14:29:54 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Mon, 03 Nov 2025 14:29:54 GMT
LABEL io.openshift.expose-services=""
# Mon, 03 Nov 2025 14:29:54 GMT
LABEL io.openshift.tags="minimal rhel9"
# Mon, 03 Nov 2025 14:29:54 GMT
LABEL compose-id="RHEL-9.7.0-updates-20251029.7"
# Mon, 03 Nov 2025 14:29:54 GMT
ENV container oci
# Mon, 03 Nov 2025 14:29:55 GMT
COPY dir:2aa80c9d25b835f7579e139a16e61166355d7a0c67f0d21fa8b083adaa3d9f42 in /      
# Mon, 03 Nov 2025 14:29:55 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Mon, 03 Nov 2025 14:29:55 GMT
CMD ["/bin/bash"]
# Mon, 03 Nov 2025 14:29:55 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /usr/share/buildinfo/content-sets.json      
# Mon, 03 Nov 2025 14:29:55 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /root/buildinfo/content_manifests/content-sets.json      
# Mon, 03 Nov 2025 14:29:55 GMT
COPY file:49b4417acc3f1574e50c559322db7a558c77ea96ef2fd7003d92b0d6c0bc4675 in /usr/share/buildinfo/labels.json      
# Mon, 03 Nov 2025 14:29:55 GMT
COPY file:49b4417acc3f1574e50c559322db7a558c77ea96ef2fd7003d92b0d6c0bc4675 in /root/buildinfo/labels.json      
# Mon, 03 Nov 2025 14:29:55 GMT
LABEL "architecture"="ppc64le" "vcs-type"="git" "vcs-ref"="02d02ad5d9d5ef0add399eb1c8d5f2a4b9261204" "org.opencontainers.image.revision"="02d02ad5d9d5ef0add399eb1c8d5f2a4b9261204" "build-date"="2025-11-03T14:29:44Z" "release"="1762180032"org.opencontainers.image.revision=02d02ad5d9d5ef0add399eb1c8d5f2a4b9261204
# Wed, 12 Nov 2025 00:27:00 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 12 Nov 2025 00:27:00 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 12 Nov 2025 00:27:00 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 12 Nov 2025 00:27:00 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en     ;     microdnf clean all # buildkit
# Wed, 12 Nov 2025 00:27:00 GMT
ENV JAVA_VERSION=jdk8u472-b08
# Wed, 12 Nov 2025 00:27:07 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='e2aff19d85d2441e409d6cbdf12ef7c2acabb0de73bca4207947135dcaa935a2';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u472-b08/OpenJDK8U-jdk_aarch64_linux_hotspot_8u472b08.tar.gz';          ;;        ppc64le)          ESUM='eaf57a4564265583b0641c878bea8943d27ef110c096868f686dae179fb45d8f';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u472-b08/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u472b08.tar.gz';          ;;        x86_64)          ESUM='5becaa4ac660e844c5a39e2ebc39ff5ac824c37ff1b625af8c8b111dc13c3592';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u472-b08/OpenJDK8U-jdk_x64_linux_hotspot_8u472b08.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip; # buildkit
# Wed, 12 Nov 2025 00:27:08 GMT
RUN set -eux;     echo "Verifying install ...";     echo "javac -version"; javac -version;     echo "java -version"; java -version;     echo "Complete." # buildkit
# Wed, 12 Nov 2025 00:27:08 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 12 Nov 2025 00:27:08 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 12 Nov 2025 01:15:28 GMT
CMD ["gradle"]
# Wed, 12 Nov 2025 01:15:28 GMT
ENV GRADLE_HOME=/opt/gradle
# Wed, 12 Nov 2025 01:15:28 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 101 gradle     && useradd --system --gid gradle --uid 101 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Wed, 12 Nov 2025 01:15:28 GMT
VOLUME [/home/gradle/.gradle]
# Wed, 12 Nov 2025 01:15:28 GMT
WORKDIR /home/gradle
# Wed, 12 Nov 2025 01:15:42 GMT
RUN set -o errexit -o nounset     && microdnf install -y         make                 findutils                 unzip         which                 git         git-lfs         subversion     && microdnf clean all         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which svn # buildkit
# Wed, 12 Nov 2025 01:15:42 GMT
ENV GRADLE_VERSION=7.6.6
# Wed, 12 Nov 2025 01:15:42 GMT
ARG GRADLE_DOWNLOAD_SHA256=673d9776f303bc7048fc3329d232d6ebf1051b07893bd9d11616fad9a8673be0
# Wed, 12 Nov 2025 01:19:04 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=673d9776f303bc7048fc3329d232d6ebf1051b07893bd9d11616fad9a8673be0
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Wed, 12 Nov 2025 01:19:04 GMT
USER gradle
# Wed, 12 Nov 2025 01:19:05 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=673d9776f303bc7048fc3329d232d6ebf1051b07893bd9d11616fad9a8673be0
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Wed, 12 Nov 2025 01:19:05 GMT
USER root
```

-	Layers:
	-	`sha256:04de4da8229cfd129cfea893dac88ba696a562db55dbc18bd0f1170c64597ec0`  
		Last Modified: Tue, 11 Nov 2025 18:11:00 GMT  
		Size: 44.4 MB (44446682 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10811e923266c33db9d8e2226dde2a6e4344e022c251901b43e9588926da8eac`  
		Last Modified: Wed, 12 Nov 2025 00:27:44 GMT  
		Size: 30.1 MB (30115412 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8233a21197b36f97190c06abf0d62e61ea6cf085dbe167051a9616272b1904f1`  
		Last Modified: Wed, 12 Nov 2025 00:27:45 GMT  
		Size: 52.2 MB (52175825 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:793ca484fa8972019054b4152a2351aa57ce234b9930adbe41194d4a55b6dc9c`  
		Last Modified: Wed, 12 Nov 2025 00:27:42 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4cb2ccbf9e85955f096bbb67fd4540fccca5ae41749dff526ced98f8dc1aa228`  
		Last Modified: Wed, 12 Nov 2025 00:27:42 GMT  
		Size: 2.3 KB (2314 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77b5768fe26ca7815e662ebec75c0811a53c3ec0dbca029a60965bb9ac0e60a3`  
		Last Modified: Wed, 12 Nov 2025 01:16:36 GMT  
		Size: 1.7 KB (1704 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0260c64207312e323d40c1c16f32a130516fed500445ee2c4b45220e0a762039`  
		Last Modified: Wed, 12 Nov 2025 01:16:38 GMT  
		Size: 38.3 MB (38299598 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:833a410d3ac10d451b9c40d4417fa2a348de9f9d039b5168a08a50be32d8fcee`  
		Last Modified: Wed, 12 Nov 2025 20:56:48 GMT  
		Size: 128.5 MB (128469415 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d973d5caeee12b341668d113f0dd6bae6a1569539562c5eedca883903faeb143`  
		Last Modified: Wed, 12 Nov 2025 01:19:50 GMT  
		Size: 35.0 KB (35013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:7-jdk8-ubi-minimal` - unknown; unknown

```console
$ docker pull gradle@sha256:0e525d9d5b79857e069572def751237b82d977a3877a2b5b77645857adeeb086
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5456471 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:00f0d1657e774e86621dc298c5119caca5d7639c1698da9e7204f4e2e568dbb8`

```dockerfile
```

-	Layers:
	-	`sha256:f7e9626c1b27459234c37bb0c77cb7f2f473c73ef7e6bb90ebba69986c32e6e0`  
		Last Modified: Wed, 12 Nov 2025 03:19:50 GMT  
		Size: 5.4 MB (5432813 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d0be4e47e0bd546a9abe55cf0f4b9b7970964e1207235ba04a330f44cfbcca61`  
		Last Modified: Wed, 12 Nov 2025 03:19:50 GMT  
		Size: 23.7 KB (23658 bytes)  
		MIME: application/vnd.in-toto+json
