## `gradle:ubi`

```console
$ docker pull gradle@sha256:b104c726ced09b43a114585c3d3de4d7f0cdc11c7b4ba32fedbd9621e1ea2ee6
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

### `gradle:ubi` - linux; amd64

```console
$ docker pull gradle@sha256:d45cfa7f47fb7ff082ddd17caf6c1b4d16ab258126e8931f57f44b611e027370
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **341.0 MB (340957965 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:658c0c01a71c44441141dceec619684cd5068dc48e7096be183648dfa34986f1`
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
ENV JAVA_VERSION=jdk-25.0.2+10
# Mon, 13 Apr 2026 23:58:30 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='a9d73e711d967dc44896d4f430f73a68fd33590dabc29a7f2fb9f593425b854c';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.2%2B10/OpenJDK25U-jdk_aarch64_linux_hotspot_25.0.2_10.tar.gz';          ;;        ppc64le)          ESUM='b262b735b215173003766da36588d5f717dceada0286db41b439f93fb2ada468';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.2%2B10/OpenJDK25U-jdk_ppc64le_linux_hotspot_25.0.2_10.tar.gz';          ;;        s390x)          ESUM='15e5cbcadcf3d43623c31b825063cdc2817b9f1ba840b51dc6ef70e5d33c84e3';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.2%2B10/OpenJDK25U-jdk_s390x_linux_hotspot_25.0.2_10.tar.gz';          ;;        x86_64)          ESUM='987387933b64b9833846dee373b640440d3e1fd48a04804ec01a6dbf718e8ab8';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.2%2B10/OpenJDK25U-jdk_x64_linux_hotspot_25.0.2_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Mon, 13 Apr 2026 23:58:31 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Mon, 13 Apr 2026 23:58:31 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Mon, 13 Apr 2026 23:58:31 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Mon, 13 Apr 2026 23:58:31 GMT
CMD ["jshell"]
# Tue, 14 Apr 2026 00:10:33 GMT
CMD ["gradle"]
# Tue, 14 Apr 2026 00:10:33 GMT
ENV GRADLE_HOME=/opt/gradle
# Tue, 14 Apr 2026 00:10:33 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 101 gradle     && useradd --system --gid gradle --uid 101 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Tue, 14 Apr 2026 00:10:33 GMT
VOLUME [/home/gradle/.gradle]
# Tue, 14 Apr 2026 00:10:33 GMT
WORKDIR /home/gradle
# Tue, 14 Apr 2026 00:10:37 GMT
RUN set -o errexit -o nounset     && microdnf install -y         make         curl         wget         tar                 findutils                 unzip         which                 git         git-lfs         subversion     && microdnf clean all         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which svn # buildkit
# Tue, 14 Apr 2026 00:10:37 GMT
ENV GRADLE_VERSION=9.4.1
# Tue, 14 Apr 2026 00:10:37 GMT
ARG GRADLE_DOWNLOAD_SHA256=2ab2958f2a1e51120c326cad6f385153bb11ee93b3c216c5fccebfdfbb7ec6cb
# Tue, 14 Apr 2026 00:10:40 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=2ab2958f2a1e51120c326cad6f385153bb11ee93b3c216c5fccebfdfbb7ec6cb
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Tue, 14 Apr 2026 00:10:40 GMT
USER gradle
# Tue, 14 Apr 2026 00:10:40 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=2ab2958f2a1e51120c326cad6f385153bb11ee93b3c216c5fccebfdfbb7ec6cb
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --stacktrace --debug --version # buildkit
# Tue, 14 Apr 2026 00:10:40 GMT
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
	-	`sha256:63295ffccacdf6b0259bf830a9ec3ceb1425c5c1091087e85b1d0e4d45a7f4aa`  
		Last Modified: Mon, 13 Apr 2026 23:58:51 GMT  
		Size: 92.3 MB (92257947 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a4afa0c60eca9b5f6129d98c634728d3475258562359065dce40304ba4e9025`  
		Last Modified: Mon, 13 Apr 2026 23:58:47 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14d7fc61f704d6e0aa859c7e9921b2169ed47203049abb6293055edcf88e37b3`  
		Last Modified: Mon, 13 Apr 2026 23:58:47 GMT  
		Size: 2.3 KB (2290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:814ae216c990aba090ab7fff94109841cffd5931187496e7095a4b77078eb62d`  
		Last Modified: Tue, 14 Apr 2026 00:10:59 GMT  
		Size: 1.6 KB (1586 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b411ae7d52f8d339e715a811662652bdcdb582b9212bbe3cdc7a16ebfc053138`  
		Last Modified: Tue, 14 Apr 2026 00:11:01 GMT  
		Size: 38.8 MB (38795647 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:794b037d4e9835f99cc82bcfbc9c59c3633fbe78488d6c28ca8844e6349317fc`  
		Last Modified: Tue, 14 Apr 2026 00:11:03 GMT  
		Size: 137.8 MB (137808335 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1d75ce2255765ff67e653193d52e5fd9f3ac6b769cb377399d0e8f3db078b54`  
		Last Modified: Tue, 14 Apr 2026 00:10:59 GMT  
		Size: 25.6 KB (25612 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:ubi` - unknown; unknown

```console
$ docker pull gradle@sha256:707736a8b8eb82aa41709a35397488def0a9fdf6fe0914d143fd0a40ddaa0fe9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 MB (7019943 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:686d6d5642ba5509e42cc4c68a0f5c5e4ca5728c0f813dc2c3e843c2cc49d26a`

```dockerfile
```

-	Layers:
	-	`sha256:e736f1969858390087c5437ff0670ebdb9f3a1e9992802c911c0414451a6dc88`  
		Last Modified: Tue, 14 Apr 2026 00:10:59 GMT  
		Size: 7.0 MB (6994930 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dd29c9d44275a211099632f71ae7ea7741f4014d3082c84d2778d3a65ac19c97`  
		Last Modified: Tue, 14 Apr 2026 00:10:58 GMT  
		Size: 25.0 KB (25013 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:ubi` - linux; arm64 variant v8

```console
$ docker pull gradle@sha256:0250e0fb12dd4434ffb23990ef6d909be71c25b930d76fb4ed3c5b6424b28c9b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **337.5 MB (337519331 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cbe894513b4b71872d4442688059958589f5c14d6cf31138a392ab0a9cba367b`
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
# Tue, 14 Apr 2026 00:00:31 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 14 Apr 2026 00:00:31 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 14 Apr 2026 00:00:31 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 14 Apr 2026 00:00:31 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en         gnupg2     ;     microdnf clean all # buildkit
# Tue, 14 Apr 2026 00:00:31 GMT
ENV JAVA_VERSION=jdk-25.0.2+10
# Tue, 14 Apr 2026 00:00:37 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='a9d73e711d967dc44896d4f430f73a68fd33590dabc29a7f2fb9f593425b854c';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.2%2B10/OpenJDK25U-jdk_aarch64_linux_hotspot_25.0.2_10.tar.gz';          ;;        ppc64le)          ESUM='b262b735b215173003766da36588d5f717dceada0286db41b439f93fb2ada468';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.2%2B10/OpenJDK25U-jdk_ppc64le_linux_hotspot_25.0.2_10.tar.gz';          ;;        s390x)          ESUM='15e5cbcadcf3d43623c31b825063cdc2817b9f1ba840b51dc6ef70e5d33c84e3';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.2%2B10/OpenJDK25U-jdk_s390x_linux_hotspot_25.0.2_10.tar.gz';          ;;        x86_64)          ESUM='987387933b64b9833846dee373b640440d3e1fd48a04804ec01a6dbf718e8ab8';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.2%2B10/OpenJDK25U-jdk_x64_linux_hotspot_25.0.2_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Tue, 14 Apr 2026 00:00:39 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 14 Apr 2026 00:00:39 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 14 Apr 2026 00:00:39 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 14 Apr 2026 00:00:39 GMT
CMD ["jshell"]
# Tue, 14 Apr 2026 00:08:56 GMT
CMD ["gradle"]
# Tue, 14 Apr 2026 00:08:56 GMT
ENV GRADLE_HOME=/opt/gradle
# Tue, 14 Apr 2026 00:08:56 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 101 gradle     && useradd --system --gid gradle --uid 101 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Tue, 14 Apr 2026 00:08:56 GMT
VOLUME [/home/gradle/.gradle]
# Tue, 14 Apr 2026 00:08:56 GMT
WORKDIR /home/gradle
# Tue, 14 Apr 2026 00:09:00 GMT
RUN set -o errexit -o nounset     && microdnf install -y         make         curl         wget         tar                 findutils                 unzip         which                 git         git-lfs         subversion     && microdnf clean all         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which svn # buildkit
# Tue, 14 Apr 2026 00:09:00 GMT
ENV GRADLE_VERSION=9.4.1
# Tue, 14 Apr 2026 00:09:00 GMT
ARG GRADLE_DOWNLOAD_SHA256=2ab2958f2a1e51120c326cad6f385153bb11ee93b3c216c5fccebfdfbb7ec6cb
# Tue, 14 Apr 2026 00:09:03 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=2ab2958f2a1e51120c326cad6f385153bb11ee93b3c216c5fccebfdfbb7ec6cb
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Tue, 14 Apr 2026 00:09:03 GMT
USER gradle
# Tue, 14 Apr 2026 00:09:04 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=2ab2958f2a1e51120c326cad6f385153bb11ee93b3c216c5fccebfdfbb7ec6cb
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --stacktrace --debug --version # buildkit
# Tue, 14 Apr 2026 00:09:04 GMT
USER root
```

-	Layers:
	-	`sha256:412494b6387e552210df602617d718496fdcb1172b467aad0caa041e910fd015`  
		Last Modified: Mon, 13 Apr 2026 11:58:02 GMT  
		Size: 32.7 MB (32680047 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a2113f953881ad5161eba5b5de83f271c4957c5a35b63ef950753c4a6f9600e`  
		Last Modified: Tue, 14 Apr 2026 00:00:58 GMT  
		Size: 37.4 MB (37399494 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0fc158ef75feb3e16ee20b8cb7fa8920111c67dd4652ef10ac56b7fba52d4ebc`  
		Last Modified: Tue, 14 Apr 2026 00:00:59 GMT  
		Size: 91.3 MB (91297869 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38454b10c86526411e9ad32d50a9de22cddf7ea17b8f7904b316a65710443b53`  
		Last Modified: Tue, 14 Apr 2026 00:00:56 GMT  
		Size: 130.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2229b432162219de647395914829970b911613da4cdb9e6eb758f17df9a9a0c2`  
		Last Modified: Tue, 14 Apr 2026 00:00:57 GMT  
		Size: 2.3 KB (2290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1bebc8d980adc7bc1c8c618e8a3790edd14fa210da92f052ea3004e2adfbde1`  
		Last Modified: Tue, 14 Apr 2026 00:09:22 GMT  
		Size: 1.6 KB (1582 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b11de56b81d8504426501c57f2c2c447b075c20ad7f96323c4f18482eed1494`  
		Last Modified: Tue, 14 Apr 2026 00:09:23 GMT  
		Size: 38.3 MB (38300210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c301683b7d6771c742a535532b4e95c2e7c6f94df6a977f4923342dfde748a0`  
		Last Modified: Tue, 14 Apr 2026 00:09:26 GMT  
		Size: 137.8 MB (137808338 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7385e8b1e4d71db021e5d1bf7147277d52480afce0dd96d37d876c442380eec1`  
		Last Modified: Tue, 14 Apr 2026 00:09:22 GMT  
		Size: 29.3 KB (29339 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:ubi` - unknown; unknown

```console
$ docker pull gradle@sha256:6223931fb66d2296221ebf0b3c676e7650b39ddc47492475ba57aa7b1a28ef1f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 MB (7018441 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:508b1df3017a1efa4cafa39742930af05067e4d0fc16f5cfd97089df75c0bde1`

```dockerfile
```

-	Layers:
	-	`sha256:2954d948b3ecd621cee635a554575764ce371d7d67907372af6e3b10335d8605`  
		Last Modified: Tue, 14 Apr 2026 00:09:22 GMT  
		Size: 7.0 MB (6993207 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b418b920fc66031a0c325e313d4370262f7865a347312d12e93b08649270a099`  
		Last Modified: Tue, 14 Apr 2026 00:09:22 GMT  
		Size: 25.2 KB (25234 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:ubi` - linux; ppc64le

```console
$ docker pull gradle@sha256:8a8c4dcf425cdb3fe69691e91f59f492ea964f65286275ca5188760c65c7c034
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **347.9 MB (347904035 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7f0164071391d51d413cd6ccb58deae7bbd94053aea97498831d16d40a80d132`
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
ENV JAVA_VERSION=jdk-25.0.2+10
# Mon, 13 Apr 2026 23:59:50 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='a9d73e711d967dc44896d4f430f73a68fd33590dabc29a7f2fb9f593425b854c';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.2%2B10/OpenJDK25U-jdk_aarch64_linux_hotspot_25.0.2_10.tar.gz';          ;;        ppc64le)          ESUM='b262b735b215173003766da36588d5f717dceada0286db41b439f93fb2ada468';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.2%2B10/OpenJDK25U-jdk_ppc64le_linux_hotspot_25.0.2_10.tar.gz';          ;;        s390x)          ESUM='15e5cbcadcf3d43623c31b825063cdc2817b9f1ba840b51dc6ef70e5d33c84e3';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.2%2B10/OpenJDK25U-jdk_s390x_linux_hotspot_25.0.2_10.tar.gz';          ;;        x86_64)          ESUM='987387933b64b9833846dee373b640440d3e1fd48a04804ec01a6dbf718e8ab8';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.2%2B10/OpenJDK25U-jdk_x64_linux_hotspot_25.0.2_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Mon, 13 Apr 2026 23:59:53 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Mon, 13 Apr 2026 23:59:54 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Mon, 13 Apr 2026 23:59:54 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Mon, 13 Apr 2026 23:59:54 GMT
CMD ["jshell"]
# Tue, 14 Apr 2026 00:14:20 GMT
CMD ["gradle"]
# Tue, 14 Apr 2026 00:14:20 GMT
ENV GRADLE_HOME=/opt/gradle
# Tue, 14 Apr 2026 00:14:20 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 101 gradle     && useradd --system --gid gradle --uid 101 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Tue, 14 Apr 2026 00:14:20 GMT
VOLUME [/home/gradle/.gradle]
# Tue, 14 Apr 2026 00:14:20 GMT
WORKDIR /home/gradle
# Tue, 14 Apr 2026 00:14:40 GMT
RUN set -o errexit -o nounset     && microdnf install -y         make         curl         wget         tar                 findutils                 unzip         which                 git         git-lfs         subversion     && microdnf clean all         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which svn # buildkit
# Tue, 14 Apr 2026 00:14:40 GMT
ENV GRADLE_VERSION=9.4.1
# Tue, 14 Apr 2026 00:14:40 GMT
ARG GRADLE_DOWNLOAD_SHA256=2ab2958f2a1e51120c326cad6f385153bb11ee93b3c216c5fccebfdfbb7ec6cb
# Tue, 14 Apr 2026 00:14:45 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=2ab2958f2a1e51120c326cad6f385153bb11ee93b3c216c5fccebfdfbb7ec6cb
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Tue, 14 Apr 2026 00:14:45 GMT
USER gradle
# Tue, 14 Apr 2026 00:14:47 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=2ab2958f2a1e51120c326cad6f385153bb11ee93b3c216c5fccebfdfbb7ec6cb
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --stacktrace --debug --version # buildkit
# Tue, 14 Apr 2026 00:14:47 GMT
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
	-	`sha256:e4365014e54c825472c2fd84c7ab1d287128f19dbbc5465c335d17a9544e1773`  
		Last Modified: Tue, 14 Apr 2026 00:00:42 GMT  
		Size: 91.6 MB (91634926 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03624f7acd524209dbca510fe3f41c4589779b8a36662f172e9e369abaf9c321`  
		Last Modified: Tue, 14 Apr 2026 00:00:40 GMT  
		Size: 130.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2fd5cf0e223f3fff36ca988d6c7941d3500a8c3df5825a8d89137d2ffad63d72`  
		Last Modified: Tue, 14 Apr 2026 00:00:39 GMT  
		Size: 2.3 KB (2292 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6da9807fa408ccff4acd27674785e2e0b4838959159a3711e2a3fb4276818e9e`  
		Last Modified: Tue, 14 Apr 2026 00:15:35 GMT  
		Size: 1.6 KB (1584 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:228e03cc8e8e11510bd338f2703009fec94cd9568f9c8c5f433a4acec933a909`  
		Last Modified: Tue, 14 Apr 2026 00:15:36 GMT  
		Size: 40.5 MB (40539288 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:944a314fdaa3b46613d90c6b7c3ed4bed91964ee935fa426762ee03afa5f3e36`  
		Last Modified: Tue, 14 Apr 2026 00:15:39 GMT  
		Size: 137.8 MB (137808334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cfc6c7cba8407ed9bde0cea2bdc9cedba4dc78bc3f011b6799ce1e8378c9652`  
		Last Modified: Tue, 14 Apr 2026 00:15:35 GMT  
		Size: 376.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:ubi` - unknown; unknown

```console
$ docker pull gradle@sha256:e9167a9388ee66e9a1e888ecbf90ac902243a08d85fc5610a8202f7d682b65e9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 MB (6994769 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b9234aac710e2454b35b78db70fe456eeceadb0e66a1225c53d44a6bfd686640`

```dockerfile
```

-	Layers:
	-	`sha256:a8b4c4993a54616122c114682463748570b1f0b6343a8218d89c8f616dfdd8ce`  
		Last Modified: Tue, 14 Apr 2026 00:15:35 GMT  
		Size: 7.0 MB (6969672 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:528d7f9ab381025b3cda7f000798806d3dcfcfa6211b0334b8d2639c2a6b5e62`  
		Last Modified: Tue, 14 Apr 2026 00:15:35 GMT  
		Size: 25.1 KB (25097 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:ubi` - linux; s390x

```console
$ docker pull gradle@sha256:d18a7674624efef5657ffc6e786edfa5202d9a6c38d9e808d8480ff0cf60f3b5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **339.2 MB (339192734 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:09798a9936c42e5e22cd9108b973bce86d89e9c7f390b2fb1d125685ae809603`
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
ENV JAVA_VERSION=jdk-25.0.2+10
# Fri, 27 Mar 2026 19:00:38 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='a9d73e711d967dc44896d4f430f73a68fd33590dabc29a7f2fb9f593425b854c';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.2%2B10/OpenJDK25U-jdk_aarch64_linux_hotspot_25.0.2_10.tar.gz';          ;;        ppc64le)          ESUM='b262b735b215173003766da36588d5f717dceada0286db41b439f93fb2ada468';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.2%2B10/OpenJDK25U-jdk_ppc64le_linux_hotspot_25.0.2_10.tar.gz';          ;;        s390x)          ESUM='15e5cbcadcf3d43623c31b825063cdc2817b9f1ba840b51dc6ef70e5d33c84e3';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.2%2B10/OpenJDK25U-jdk_s390x_linux_hotspot_25.0.2_10.tar.gz';          ;;        x86_64)          ESUM='987387933b64b9833846dee373b640440d3e1fd48a04804ec01a6dbf718e8ab8';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.2%2B10/OpenJDK25U-jdk_x64_linux_hotspot_25.0.2_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Fri, 27 Mar 2026 19:00:39 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Fri, 27 Mar 2026 19:00:40 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Fri, 27 Mar 2026 19:00:40 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Fri, 27 Mar 2026 19:00:40 GMT
CMD ["jshell"]
# Fri, 27 Mar 2026 19:10:27 GMT
CMD ["gradle"]
# Fri, 27 Mar 2026 19:10:27 GMT
ENV GRADLE_HOME=/opt/gradle
# Fri, 27 Mar 2026 19:10:27 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 101 gradle     && useradd --system --gid gradle --uid 101 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Fri, 27 Mar 2026 19:10:27 GMT
VOLUME [/home/gradle/.gradle]
# Fri, 27 Mar 2026 19:10:27 GMT
WORKDIR /home/gradle
# Fri, 27 Mar 2026 19:10:35 GMT
RUN set -o errexit -o nounset     && microdnf install -y         make         curl         wget         tar                 findutils                 unzip         which                 git         git-lfs         subversion     && microdnf clean all         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which svn # buildkit
# Fri, 27 Mar 2026 19:10:35 GMT
ENV GRADLE_VERSION=9.4.1
# Fri, 27 Mar 2026 19:10:35 GMT
ARG GRADLE_DOWNLOAD_SHA256=2ab2958f2a1e51120c326cad6f385153bb11ee93b3c216c5fccebfdfbb7ec6cb
# Fri, 27 Mar 2026 19:10:39 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=2ab2958f2a1e51120c326cad6f385153bb11ee93b3c216c5fccebfdfbb7ec6cb
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Fri, 27 Mar 2026 19:10:39 GMT
USER gradle
# Fri, 27 Mar 2026 19:10:39 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=2ab2958f2a1e51120c326cad6f385153bb11ee93b3c216c5fccebfdfbb7ec6cb
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --stacktrace --debug --version # buildkit
# Fri, 27 Mar 2026 19:10:39 GMT
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
	-	`sha256:54e3abb08bb8865ca5fb7b04a317d59ff9098c5297f7a660331addc55e836787`  
		Last Modified: Fri, 27 Mar 2026 19:01:06 GMT  
		Size: 88.2 MB (88235359 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1f1acf957d22ab4d8ec9c88816b59df2302d11781f835d31c2751e567805746`  
		Last Modified: Fri, 27 Mar 2026 19:01:04 GMT  
		Size: 130.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f1f4514ec260a95cb0c4a6faaa672165eae571aca12042ca51db88f3d571da7`  
		Last Modified: Fri, 27 Mar 2026 19:01:04 GMT  
		Size: 2.3 KB (2290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eae197277291f7a566c0ba70a0a8ad1ea035432a1194d78633d9c3e25b2f11de`  
		Last Modified: Fri, 27 Mar 2026 19:11:08 GMT  
		Size: 1.6 KB (1585 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb200a4eb0526e3d3619d1e966316f37725d333ed4b96a87db5f67854cde9931`  
		Last Modified: Fri, 27 Mar 2026 19:11:09 GMT  
		Size: 40.9 MB (40875229 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a00f18ceab1631f77b0ff33785e249894ec63fd4782185db55a019e27b98c6f`  
		Last Modified: Fri, 27 Mar 2026 19:11:11 GMT  
		Size: 137.8 MB (137808334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f03a754c98b592945d3cbb1f2e815f295c20ecb9d14e6db93765d4a2bb472521`  
		Last Modified: Fri, 27 Mar 2026 19:11:08 GMT  
		Size: 376.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:ubi` - unknown; unknown

```console
$ docker pull gradle@sha256:9000c8127538de3ff3bb7d6cda5ec5317988890ef3f2548b05e69b4e767844b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 MB (6985134 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d82e5dd0c9c912e49275f366e2438c2a051c126a61b3f45191dceb072952a97`

```dockerfile
```

-	Layers:
	-	`sha256:2f0cc47a7b1b97f358e0670e0b09da78990eb1b1ee23e7c83102dbeb37dedc68`  
		Last Modified: Fri, 27 Mar 2026 19:11:08 GMT  
		Size: 7.0 MB (6960123 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:94eae19483b181deeaa73f9fc4f716925076d4395272a01d32c5528a7c7389f8`  
		Last Modified: Fri, 27 Mar 2026 19:11:08 GMT  
		Size: 25.0 KB (25011 bytes)  
		MIME: application/vnd.in-toto+json
