## `gradle:9-jdk17-ubi`

```console
$ docker pull gradle@sha256:ded136995e41dfd5c01a161edbf8d8d823659f94021dfe8577ae4f9008355342
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

### `gradle:9-jdk17-ubi` - linux; amd64

```console
$ docker pull gradle@sha256:5c09d4529d851c778b00d6a054a609e1f0c3dee55a9806d1deb5e97af9e4a7c1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **388.2 MB (388152476 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a8f164388d291abaf0d379856515d895ca6ac4b6629b658c4a7bba1a691c5cf`
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
# Fri, 14 Nov 2025 01:13:02 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 14 Nov 2025 01:13:02 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 14 Nov 2025 01:13:02 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 14 Nov 2025 01:13:02 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en     ;     microdnf clean all # buildkit
# Fri, 14 Nov 2025 01:13:02 GMT
ENV JAVA_VERSION=jdk-17.0.17+10
# Fri, 14 Nov 2025 01:13:08 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='dc29ca6d35beb4419b4b00419b8a3dfbf5ae551e1ae2b046b516d9a579d04533';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jdk_aarch64_linux_hotspot_17.0.17_10.tar.gz';          ;;        ppc64le)          ESUM='2a29d1be61940c1bd639018c07f4622e1f145a7ef34e7294fee877e39226d9da';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jdk_ppc64le_linux_hotspot_17.0.17_10.tar.gz';          ;;        s390x)          ESUM='76327b1d00c67f6be91717754fd85fc85ce496d48876f69accb9c53ed31dc546';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jdk_s390x_linux_hotspot_17.0.17_10.tar.gz';          ;;        x86_64)          ESUM='992f96e7995075ac7636bb1a8de52b0c61d71ed3137fafc979ab96b4ab78dd75';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jdk_x64_linux_hotspot_17.0.17_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Fri, 14 Nov 2025 01:13:09 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Fri, 14 Nov 2025 01:13:09 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Fri, 14 Nov 2025 01:13:09 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Fri, 14 Nov 2025 01:13:09 GMT
CMD ["jshell"]
# Fri, 14 Nov 2025 02:17:46 GMT
CMD ["gradle"]
# Fri, 14 Nov 2025 02:17:46 GMT
ENV GRADLE_HOME=/opt/gradle
# Fri, 14 Nov 2025 02:17:46 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 101 gradle     && useradd --system --gid gradle --uid 101 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Fri, 14 Nov 2025 02:17:46 GMT
VOLUME [/home/gradle/.gradle]
# Fri, 14 Nov 2025 02:17:46 GMT
WORKDIR /home/gradle
# Fri, 14 Nov 2025 02:17:50 GMT
RUN set -o errexit -o nounset     && microdnf install -y         make         curl-minimal         wget         tar                 findutils                 unzip         which                 git         git-lfs         subversion     && microdnf clean all         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which svn # buildkit
# Fri, 14 Nov 2025 02:17:50 GMT
ENV GRADLE_VERSION=9.2.0
# Fri, 14 Nov 2025 02:17:50 GMT
ARG GRADLE_DOWNLOAD_SHA256=df67a32e86e3276d011735facb1535f64d0d88df84fa87521e90becc2d735444
# Fri, 14 Nov 2025 02:17:54 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=df67a32e86e3276d011735facb1535f64d0d88df84fa87521e90becc2d735444
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Fri, 14 Nov 2025 02:17:54 GMT
USER gradle
# Fri, 14 Nov 2025 02:17:54 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=df67a32e86e3276d011735facb1535f64d0d88df84fa87521e90becc2d735444
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Fri, 14 Nov 2025 02:17:54 GMT
USER root
```

-	Layers:
	-	`sha256:179ba4be1de0701de7b39988f2989858194723f60b56b12f8d9438358e471a73`  
		Last Modified: Wed, 12 Nov 2025 15:07:23 GMT  
		Size: 40.0 MB (40048414 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1781a3d2d07619b8314f9651860ed99e9b3ee72a18ec3543c404e6e5e846ce57`  
		Last Modified: Fri, 14 Nov 2025 01:13:37 GMT  
		Size: 30.6 MB (30635139 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7717310feded50125039db72fcbd6723a755f127f5d8d1ddc257cf6b682a7d6d`  
		Last Modified: Fri, 14 Nov 2025 02:17:43 GMT  
		Size: 144.9 MB (144852867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:750da7db57623001c79b201dfcf2ec37c724fbdbbed132e1cc4d606c9013298d`  
		Last Modified: Fri, 14 Nov 2025 01:13:35 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a9ea1cf2bf03a1cb755ab07629b94af52018a4a2ee9fd19a234e667e867828b`  
		Last Modified: Fri, 14 Nov 2025 01:13:35 GMT  
		Size: 2.3 KB (2291 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b72d89414debcaedbe2bac18835ad7d6fce54817911d7f4ed12cc19730cb5fa2`  
		Last Modified: Fri, 14 Nov 2025 02:18:19 GMT  
		Size: 1.7 KB (1707 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:321c1421bb98e6d9ef0bd5bedafd78d7a7f5f02881bec434748b09cb70a5b340`  
		Last Modified: Fri, 14 Nov 2025 02:18:25 GMT  
		Size: 37.0 MB (37035272 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7179d7e18e17862f08f33186d220be32578b03ef28ce164028fc3ca6d718ebba`  
		Last Modified: Fri, 14 Nov 2025 02:18:15 GMT  
		Size: 135.5 MB (135521733 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c32d571b036f5e160b60a1ad4f8038d747b7eda86c036490c3c65043123b7bd`  
		Last Modified: Fri, 14 Nov 2025 02:18:19 GMT  
		Size: 54.9 KB (54893 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:9-jdk17-ubi` - unknown; unknown

```console
$ docker pull gradle@sha256:506b90c8c1dca06bc8d26275624c3b9254fce9fd2bf63d1377e49dd417d5dad1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5422011 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e1d048348a97d2a43da401fb5b07b5c1d355087d9ebaaa498ff8d0b858e7a2e1`

```dockerfile
```

-	Layers:
	-	`sha256:cd06f2d93ceb58ee26d26a0890649a7eabe40f31374120c033cac577e4cad811`  
		Last Modified: Fri, 14 Nov 2025 03:35:07 GMT  
		Size: 5.4 MB (5397564 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:acddfab4d8398c48e098fbfd2fac158a7a4d81bad7a411bd0332eee42bb1156c`  
		Last Modified: Fri, 14 Nov 2025 03:35:08 GMT  
		Size: 24.4 KB (24447 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:9-jdk17-ubi` - linux; arm64 variant v8

```console
$ docker pull gradle@sha256:b534efa7846f8b6dab668f0ecd0854ecd94ed1ea14c31d4892006ed08815f187
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **384.8 MB (384802479 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:62f2750fcc88013010e4e7582842df92dbb3a68c12c56c0d8d21904443b8dead`
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
# Fri, 14 Nov 2025 01:28:20 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 14 Nov 2025 01:28:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 14 Nov 2025 01:28:20 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 14 Nov 2025 01:28:20 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en     ;     microdnf clean all # buildkit
# Fri, 14 Nov 2025 01:28:20 GMT
ENV JAVA_VERSION=jdk-17.0.17+10
# Fri, 14 Nov 2025 01:28:27 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='dc29ca6d35beb4419b4b00419b8a3dfbf5ae551e1ae2b046b516d9a579d04533';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jdk_aarch64_linux_hotspot_17.0.17_10.tar.gz';          ;;        ppc64le)          ESUM='2a29d1be61940c1bd639018c07f4622e1f145a7ef34e7294fee877e39226d9da';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jdk_ppc64le_linux_hotspot_17.0.17_10.tar.gz';          ;;        s390x)          ESUM='76327b1d00c67f6be91717754fd85fc85ce496d48876f69accb9c53ed31dc546';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jdk_s390x_linux_hotspot_17.0.17_10.tar.gz';          ;;        x86_64)          ESUM='992f96e7995075ac7636bb1a8de52b0c61d71ed3137fafc979ab96b4ab78dd75';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jdk_x64_linux_hotspot_17.0.17_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Fri, 14 Nov 2025 01:28:28 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Fri, 14 Nov 2025 01:28:28 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Fri, 14 Nov 2025 01:28:28 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Fri, 14 Nov 2025 01:28:28 GMT
CMD ["jshell"]
# Fri, 14 Nov 2025 02:20:48 GMT
CMD ["gradle"]
# Fri, 14 Nov 2025 02:20:48 GMT
ENV GRADLE_HOME=/opt/gradle
# Fri, 14 Nov 2025 02:20:48 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 101 gradle     && useradd --system --gid gradle --uid 101 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Fri, 14 Nov 2025 02:20:48 GMT
VOLUME [/home/gradle/.gradle]
# Fri, 14 Nov 2025 02:20:48 GMT
WORKDIR /home/gradle
# Fri, 14 Nov 2025 02:20:53 GMT
RUN set -o errexit -o nounset     && microdnf install -y         make         curl-minimal         wget         tar                 findutils                 unzip         which                 git         git-lfs         subversion     && microdnf clean all         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which svn # buildkit
# Fri, 14 Nov 2025 02:20:53 GMT
ENV GRADLE_VERSION=9.2.0
# Fri, 14 Nov 2025 02:20:53 GMT
ARG GRADLE_DOWNLOAD_SHA256=df67a32e86e3276d011735facb1535f64d0d88df84fa87521e90becc2d735444
# Fri, 14 Nov 2025 02:20:56 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=df67a32e86e3276d011735facb1535f64d0d88df84fa87521e90becc2d735444
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Fri, 14 Nov 2025 02:20:56 GMT
USER gradle
# Fri, 14 Nov 2025 02:20:56 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=df67a32e86e3276d011735facb1535f64d0d88df84fa87521e90becc2d735444
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Fri, 14 Nov 2025 02:20:56 GMT
USER root
```

-	Layers:
	-	`sha256:e01bb2a7f0e8ff512f86254e984d1cf0bdc9b357f1e0f0f61d352832dc12a646`  
		Last Modified: Wed, 12 Nov 2025 15:16:35 GMT  
		Size: 38.2 MB (38221043 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48960c34ddbfa8b8e131fd6a7e92f7db1b2656e9ee8ed3d0004706df37396894`  
		Last Modified: Fri, 14 Nov 2025 01:28:56 GMT  
		Size: 30.9 MB (30885195 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:226a6037ff9d519cde06292af96bbfa2bdc4dae4038408945c2842908064a79a`  
		Last Modified: Fri, 14 Nov 2025 02:20:44 GMT  
		Size: 143.7 MB (143685377 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:805d073de166f29316d663577b482249132852c0e274f7e4c1e4a8e0d7742acb`  
		Last Modified: Fri, 14 Nov 2025 01:28:53 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe25262e729ff9aea24a6de21b15ae264bf21df995085e2911d3f583b9f219a6`  
		Last Modified: Fri, 14 Nov 2025 01:28:51 GMT  
		Size: 2.3 KB (2290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22363e4ebf7dbf21579c0bfb07737af8d20e3aedffe4f9c831b6751ef99cd83c`  
		Last Modified: Fri, 14 Nov 2025 02:21:22 GMT  
		Size: 1.7 KB (1705 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:903ed13b02ad590bd53518f8511941b85b30d0d92d532ba39d18382c85c461e0`  
		Last Modified: Fri, 14 Nov 2025 02:21:26 GMT  
		Size: 36.4 MB (36425514 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af1ff16757f83390890b18e894d496b89c316f683e969d40550e45385b7e1554`  
		Last Modified: Fri, 14 Nov 2025 04:33:17 GMT  
		Size: 135.5 MB (135521667 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:265ab233d726ef80fd72094ed47250e00a1bbc7f64044b0c9e234374da6c1e6b`  
		Last Modified: Fri, 14 Nov 2025 02:21:22 GMT  
		Size: 59.5 KB (59527 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:9-jdk17-ubi` - unknown; unknown

```console
$ docker pull gradle@sha256:580a6ecbbc5b10a5025b8bce384d2ede9e1fe79f06a231bb9077107bfe1957cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5421638 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b4d944e2cd28dd408890af032ccfdd7fbe043188f7889bd3959e161f3bb884fd`

```dockerfile
```

-	Layers:
	-	`sha256:1caf14dab15ea028adf0a93b15b006e1210a063cdb56548a4c2309a757aa1811`  
		Last Modified: Fri, 14 Nov 2025 03:35:18 GMT  
		Size: 5.4 MB (5396994 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:61ff5cd1dc36943ff340e102b8859635cbedb9b4a4af4efb400328074e27a54e`  
		Last Modified: Fri, 14 Nov 2025 03:35:19 GMT  
		Size: 24.6 KB (24644 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:9-jdk17-ubi` - linux; ppc64le

```console
$ docker pull gradle@sha256:901a030bf91f4f5615d7072e92a539b612051089aa321a91d64ff544a610ce76
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **391.1 MB (391095173 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:189eb88f934f0ab3ea6e14a8404921ead233369dca0dd985e17277944f98a0d3`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["gradle"]`

```dockerfile
# Fri, 01 Aug 2025 11:04:34 GMT
LABEL maintainer="Red Hat, Inc."
# Fri, 01 Aug 2025 11:04:34 GMT
LABEL vendor="Red Hat, Inc."
# Fri, 01 Aug 2025 11:04:34 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Fri, 01 Aug 2025 11:04:34 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.6"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Fri, 01 Aug 2025 11:04:34 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Fri, 01 Aug 2025 11:04:34 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Fri, 01 Aug 2025 11:04:34 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Fri, 01 Aug 2025 11:04:34 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Fri, 01 Aug 2025 11:04:34 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Fri, 01 Aug 2025 11:04:34 GMT
LABEL io.openshift.expose-services=""
# Fri, 01 Aug 2025 11:04:34 GMT
LABEL io.openshift.tags="minimal rhel9"
# Fri, 01 Aug 2025 11:04:34 GMT
ENV container oci
# Fri, 01 Aug 2025 11:04:34 GMT
COPY dir:449eb2f239bac2d8d364a723cb091b20b453ccb6c9e9ef4542e774b1e6a3f931 in /      
# Fri, 01 Aug 2025 11:04:34 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Fri, 01 Aug 2025 11:04:34 GMT
CMD ["/bin/bash"]
# Fri, 01 Aug 2025 11:04:34 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /usr/share/buildinfo/content-sets.json      
# Fri, 01 Aug 2025 11:04:34 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /root/buildinfo/content_manifests/content-sets.json      
# Fri, 01 Aug 2025 11:04:34 GMT
COPY file:a1ec773a4fe5bc79df5be7b721d463b5573cea3333f3a512f669f32fa8283a6b in /root/buildinfo/labels.json      
# Fri, 01 Aug 2025 11:04:34 GMT
LABEL "architecture"="ppc64le" "vcs-type"="git" "vcs-ref"="d1b15a34ce69ea214e1d32f1f501304f6b8b8c59" "org.opencontainers.image.revision"="d1b15a34ce69ea214e1d32f1f501304f6b8b8c59" "build-date"="2025-10-15T08:07:44Z" "release"="1760515502"org.opencontainers.image.revision=d1b15a34ce69ea214e1d32f1f501304f6b8b8c59
# Fri, 01 Aug 2025 11:04:34 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 01 Aug 2025 11:04:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 01 Aug 2025 11:04:34 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 01 Aug 2025 11:04:34 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en     ;     microdnf clean all # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
ENV JAVA_VERSION=jdk-17.0.16+8
# Fri, 01 Aug 2025 11:04:34 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='423416447885d9e45f96dd9e0b2c1367da5e1b0353e187cfdf9388c9820ac147';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.16%2B8/OpenJDK17U-jdk_aarch64_linux_hotspot_17.0.16_8.tar.gz';          ;;        ppc64le)          ESUM='eb020f74e00870379522be0b44fc6322c2214e77971c258400c8b5af704d5c0a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.16%2B8/OpenJDK17U-jdk_ppc64le_linux_hotspot_17.0.16_8.tar.gz';          ;;        s390x)          ESUM='03dd99d34d2d1b88395765df3acbec2cb81de286f64b1d9e6df3682bee365168';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.16%2B8/OpenJDK17U-jdk_s390x_linux_hotspot_17.0.16_8.tar.gz';          ;;        x86_64)          ESUM='166774efcf0f722f2ee18eba0039de2d685b350ee14d7b69e6f83437dafd2af1';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.16%2B8/OpenJDK17U-jdk_x64_linux_hotspot_17.0.16_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Fri, 01 Aug 2025 11:04:34 GMT
CMD ["jshell"]
# Tue, 30 Sep 2025 09:31:25 GMT
CMD ["gradle"]
# Tue, 30 Sep 2025 09:31:25 GMT
ENV GRADLE_HOME=/opt/gradle
# Tue, 30 Sep 2025 09:31:25 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 101 gradle     && useradd --system --gid gradle --uid 101 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Tue, 30 Sep 2025 09:31:25 GMT
VOLUME [/home/gradle/.gradle]
# Tue, 30 Sep 2025 09:31:25 GMT
WORKDIR /home/gradle
# Tue, 30 Sep 2025 09:31:25 GMT
RUN set -o errexit -o nounset     && microdnf install -y         make         curl-minimal         wget         tar                 findutils                 unzip         which                 git         git-lfs         subversion     && microdnf clean all         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which svn # buildkit
# Tue, 30 Sep 2025 09:31:25 GMT
ENV GRADLE_VERSION=9.1.0
# Tue, 30 Sep 2025 09:31:25 GMT
ARG GRADLE_DOWNLOAD_SHA256=a17ddd85a26b6a7f5ddb71ff8b05fc5104c0202c6e64782429790c933686c806
# Tue, 30 Sep 2025 09:31:25 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=a17ddd85a26b6a7f5ddb71ff8b05fc5104c0202c6e64782429790c933686c806
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Tue, 30 Sep 2025 09:31:25 GMT
USER gradle
# Tue, 30 Sep 2025 09:31:25 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=a17ddd85a26b6a7f5ddb71ff8b05fc5104c0202c6e64782429790c933686c806
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Tue, 30 Sep 2025 09:31:25 GMT
USER root
```

-	Layers:
	-	`sha256:7d2fc558322651c1228b069dff5be5599bf4a7e595e3227e6de491f7067f1a45`  
		Last Modified: Wed, 15 Oct 2025 08:44:15 GMT  
		Size: 44.1 MB (44050495 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6e876758687ee7b24ef8e66e150458a00c077b6471ef21c521bdde430e3e50c`  
		Last Modified: Thu, 16 Oct 2025 19:26:31 GMT  
		Size: 30.0 MB (29971557 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8c12b4e688b4184bc756ea7005169c8f6401e702c6bdf65ffdb4746e88012c4`  
		Last Modified: Fri, 17 Oct 2025 12:44:12 GMT  
		Size: 144.4 MB (144393845 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de9cadec2da00c278ab276060019fd0b207a9d852f1ed6fdb1ffa8952f371bc2`  
		Last Modified: Thu, 16 Oct 2025 19:31:14 GMT  
		Size: 130.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d24124d0bfcc02969bf248740611e30edfbe44ea4323805702d74f4f76fad3df`  
		Last Modified: Thu, 16 Oct 2025 19:31:14 GMT  
		Size: 2.3 KB (2290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c3fcfe4b922a31eeb33510e9d629e1b3a930e4bbcf782b518e19f08f0e5b976`  
		Last Modified: Thu, 16 Oct 2025 20:13:13 GMT  
		Size: 1.7 KB (1713 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3047aa43460cb5fd3b23d077defc34315ba680cbae87223e1ad6064381958d0`  
		Last Modified: Thu, 16 Oct 2025 20:13:17 GMT  
		Size: 38.1 MB (38125422 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:304dc821b9b92f804948021121195c1ff2aecebf42139fa8e01ad2f58c6d1691`  
		Last Modified: Fri, 17 Oct 2025 15:10:27 GMT  
		Size: 134.5 MB (134514684 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f862d5953a0247d96629efaba09109ffc69e0c3364908545badc9f93aee3797b`  
		Last Modified: Thu, 16 Oct 2025 20:13:13 GMT  
		Size: 35.0 KB (35005 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:9-jdk17-ubi` - unknown; unknown

```console
$ docker pull gradle@sha256:c191c0ffcb8be98164771d42fb753d8c1fd8e1b97a90d94064ec549fc22cf0f5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5398147 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c0925a23802300bf65dc0d36c89099e88b6626a735cba8e4ee961ee67b518855`

```dockerfile
```

-	Layers:
	-	`sha256:1f3ca949b9099d4c57d21607b9ed75b56031aeb8176ba030631ad04ec3de161e`  
		Last Modified: Thu, 16 Oct 2025 23:24:31 GMT  
		Size: 5.4 MB (5373551 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:61d3f8d7dc7f7bbb57d40c9676d5013786ff2bc12caad3a2da6880f6b1d40247`  
		Last Modified: Thu, 16 Oct 2025 23:24:33 GMT  
		Size: 24.6 KB (24596 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:9-jdk17-ubi` - linux; s390x

```console
$ docker pull gradle@sha256:8e635e1a7a459eafc5c696decfa484ca12392945b89e7b56ed66d6f584f88257
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **371.0 MB (371027051 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f5a6f8baeec9f51006773ab168134c8dc6a67ae169404ab78c08707ed3cafd9`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["gradle"]`

```dockerfile
# Fri, 01 Aug 2025 11:04:34 GMT
LABEL maintainer="Red Hat, Inc."
# Fri, 01 Aug 2025 11:04:34 GMT
LABEL vendor="Red Hat, Inc."
# Fri, 01 Aug 2025 11:04:34 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Fri, 01 Aug 2025 11:04:34 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.6"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Fri, 01 Aug 2025 11:04:34 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Fri, 01 Aug 2025 11:04:34 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Fri, 01 Aug 2025 11:04:34 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Fri, 01 Aug 2025 11:04:34 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Fri, 01 Aug 2025 11:04:34 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Fri, 01 Aug 2025 11:04:34 GMT
LABEL io.openshift.expose-services=""
# Fri, 01 Aug 2025 11:04:34 GMT
LABEL io.openshift.tags="minimal rhel9"
# Fri, 01 Aug 2025 11:04:34 GMT
ENV container oci
# Fri, 01 Aug 2025 11:04:34 GMT
COPY dir:c7531cf9ca81563f111865af7c21a35f1b40cdbceb45f292beb90b52a7f09fd7 in /      
# Fri, 01 Aug 2025 11:04:34 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Fri, 01 Aug 2025 11:04:34 GMT
CMD ["/bin/bash"]
# Fri, 01 Aug 2025 11:04:34 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /usr/share/buildinfo/content-sets.json      
# Fri, 01 Aug 2025 11:04:34 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /root/buildinfo/content_manifests/content-sets.json      
# Fri, 01 Aug 2025 11:04:34 GMT
COPY file:c18f78822817f13e8af547877aa1bb6f7295fa27828e91bdb8605916bb9a08c8 in /root/buildinfo/labels.json      
# Fri, 01 Aug 2025 11:04:34 GMT
LABEL "architecture"="s390x" "vcs-type"="git" "vcs-ref"="d1b15a34ce69ea214e1d32f1f501304f6b8b8c59" "org.opencontainers.image.revision"="d1b15a34ce69ea214e1d32f1f501304f6b8b8c59" "build-date"="2025-10-15T08:12:03Z" "release"="1760515502"org.opencontainers.image.revision=d1b15a34ce69ea214e1d32f1f501304f6b8b8c59
# Fri, 01 Aug 2025 11:04:34 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 01 Aug 2025 11:04:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 01 Aug 2025 11:04:34 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 01 Aug 2025 11:04:34 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en     ;     microdnf clean all # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
ENV JAVA_VERSION=jdk-17.0.16+8
# Fri, 01 Aug 2025 11:04:34 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='423416447885d9e45f96dd9e0b2c1367da5e1b0353e187cfdf9388c9820ac147';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.16%2B8/OpenJDK17U-jdk_aarch64_linux_hotspot_17.0.16_8.tar.gz';          ;;        ppc64le)          ESUM='eb020f74e00870379522be0b44fc6322c2214e77971c258400c8b5af704d5c0a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.16%2B8/OpenJDK17U-jdk_ppc64le_linux_hotspot_17.0.16_8.tar.gz';          ;;        s390x)          ESUM='03dd99d34d2d1b88395765df3acbec2cb81de286f64b1d9e6df3682bee365168';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.16%2B8/OpenJDK17U-jdk_s390x_linux_hotspot_17.0.16_8.tar.gz';          ;;        x86_64)          ESUM='166774efcf0f722f2ee18eba0039de2d685b350ee14d7b69e6f83437dafd2af1';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.16%2B8/OpenJDK17U-jdk_x64_linux_hotspot_17.0.16_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Fri, 01 Aug 2025 11:04:34 GMT
CMD ["jshell"]
# Tue, 30 Sep 2025 09:31:25 GMT
CMD ["gradle"]
# Tue, 30 Sep 2025 09:31:25 GMT
ENV GRADLE_HOME=/opt/gradle
# Tue, 30 Sep 2025 09:31:25 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 101 gradle     && useradd --system --gid gradle --uid 101 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Tue, 30 Sep 2025 09:31:25 GMT
VOLUME [/home/gradle/.gradle]
# Tue, 30 Sep 2025 09:31:25 GMT
WORKDIR /home/gradle
# Tue, 30 Sep 2025 09:31:25 GMT
RUN set -o errexit -o nounset     && microdnf install -y         make         curl-minimal         wget         tar                 findutils                 unzip         which                 git         git-lfs         subversion     && microdnf clean all         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which svn # buildkit
# Tue, 30 Sep 2025 09:31:25 GMT
ENV GRADLE_VERSION=9.1.0
# Tue, 30 Sep 2025 09:31:25 GMT
ARG GRADLE_DOWNLOAD_SHA256=a17ddd85a26b6a7f5ddb71ff8b05fc5104c0202c6e64782429790c933686c806
# Tue, 30 Sep 2025 09:31:25 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=a17ddd85a26b6a7f5ddb71ff8b05fc5104c0202c6e64782429790c933686c806
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Tue, 30 Sep 2025 09:31:25 GMT
USER gradle
# Tue, 30 Sep 2025 09:31:25 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=a17ddd85a26b6a7f5ddb71ff8b05fc5104c0202c6e64782429790c933686c806
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Tue, 30 Sep 2025 09:31:25 GMT
USER root
```

-	Layers:
	-	`sha256:a42ec211faae823c9be27da6cd639f320fbf91a4d4f8d9a8428b8b1f4f661ad4`  
		Last Modified: Wed, 15 Oct 2025 12:11:19 GMT  
		Size: 37.8 MB (37759797 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7122be53af945934a44fcce8efaac2e8dd2ea492439aeef1841a59957e794d4`  
		Last Modified: Thu, 16 Oct 2025 19:59:19 GMT  
		Size: 27.6 MB (27571223 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:609efcc00c750898b2a3b0b29c8b8af07f63a1fbaf8ef46c1d0b174c48f8ce9e`  
		Last Modified: Fri, 17 Oct 2025 12:44:12 GMT  
		Size: 134.7 MB (134724681 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3dd8fdd69d92f0eb93867410a4139860cf70db66da4c0bf566331f53041944ea`  
		Last Modified: Thu, 16 Oct 2025 20:01:12 GMT  
		Size: 130.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d97903fa99d932a6f660a5ef94649afb7b475edb1759f97c3c6b1b4f7d354103`  
		Last Modified: Thu, 16 Oct 2025 20:01:12 GMT  
		Size: 2.3 KB (2291 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b63ad6386c42f7b736f580791029bc573c0a23735694a3bde98177b74e8eb45c`  
		Last Modified: Thu, 16 Oct 2025 20:25:42 GMT  
		Size: 1.7 KB (1709 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72375b2f47e7dd0b13e2eb72013578b7b5da38821df4beb2ff476b36a5b6afec`  
		Last Modified: Thu, 16 Oct 2025 20:25:48 GMT  
		Size: 36.4 MB (36417504 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8304d393349bf211878e8a0a8d370642204c8909485829f526066e0fe24fc729`  
		Last Modified: Fri, 17 Oct 2025 15:10:30 GMT  
		Size: 134.5 MB (134514678 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b3c5fdf72502c50d66ff1b52f091156dc393e916a8e620c35d89d7acd4b6c6f`  
		Last Modified: Thu, 16 Oct 2025 20:25:42 GMT  
		Size: 35.0 KB (35006 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:9-jdk17-ubi` - unknown; unknown

```console
$ docker pull gradle@sha256:a1fedfd8eae94d52bfa86cb8c5c7e1aecbfc3cb05e8e36852d2ba02eeb1030bd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5387343 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa8b2ecf931373ac659991e3ed0d832adc7c2cfdc24a142df091286185dd0cc5`

```dockerfile
```

-	Layers:
	-	`sha256:5354e2d28de9796307fa91d3ea9c39eded802fc086759b6693fe7bd57d85de5b`  
		Last Modified: Thu, 16 Oct 2025 23:24:38 GMT  
		Size: 5.4 MB (5362821 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ef0255960aadaff86147186d8d3c8a66ee1c729b40005c96b247a0dc45175f3f`  
		Last Modified: Thu, 16 Oct 2025 23:24:39 GMT  
		Size: 24.5 KB (24522 bytes)  
		MIME: application/vnd.in-toto+json
