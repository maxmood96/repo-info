## `gradle:ubi`

```console
$ docker pull gradle@sha256:06ad034fc2f2dc25b8814efbe6ce68dc7e6189a6ed8d8f14dc46b9f7c11c1c75
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
$ docker pull gradle@sha256:8b4a6812246b023d21a63c222a076ef3735e2de40c48bdb18c3bd5961d30101a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **358.6 MB (358555944 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a84c7af9d35bab350bd1d92791360d1b8002d229bf9d775a2296740525da4427`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["gradle"]`

```dockerfile
# Thu, 18 Dec 2025 04:59:16 GMT
LABEL maintainer="Red Hat, Inc."
# Thu, 18 Dec 2025 04:59:16 GMT
LABEL vendor="Red Hat, Inc."
# Thu, 18 Dec 2025 04:59:16 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Thu, 18 Dec 2025 04:59:16 GMT
LABEL com.redhat.component="ubi10-minimal-container"       name="ubi10/ubi-minimal"       version="10.1"       cpe="cpe:/o:redhat:enterprise_linux:10.1"       distribution-scope="public"
# Thu, 18 Dec 2025 04:59:16 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Thu, 18 Dec 2025 04:59:16 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 10."
# Thu, 18 Dec 2025 04:59:16 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 18 Dec 2025 04:59:16 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 18 Dec 2025 04:59:16 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 10 Minimal"
# Thu, 18 Dec 2025 04:59:16 GMT
LABEL io.openshift.expose-services=""
# Thu, 18 Dec 2025 04:59:16 GMT
LABEL io.openshift.tags="minimal rhel10"
# Thu, 18 Dec 2025 04:59:16 GMT
ENV container oci
# Thu, 18 Dec 2025 04:59:17 GMT
COPY dir:fdc8c39dddd7104eb139c404c8e963d7763f4f2dba800adb3cb1affa751115f3 in /      
# Thu, 18 Dec 2025 04:59:17 GMT
COPY file:5de33b5fc08b00635bccf9134a18978dba13e2250aa51838f9969515a3957847 in /etc/yum.repos.d/.      
# Thu, 18 Dec 2025 04:59:17 GMT
CMD ["/bin/bash"]
# Thu, 18 Dec 2025 04:59:17 GMT
COPY file:595171150af68abc798ea385f7988d74b566aa8e84babff137f00b08b2164683 in /usr/share/buildinfo/content-sets.json      
# Thu, 18 Dec 2025 04:59:17 GMT
COPY file:595171150af68abc798ea385f7988d74b566aa8e84babff137f00b08b2164683 in /root/buildinfo/content_manifests/content-sets.json      
# Thu, 18 Dec 2025 04:59:17 GMT
COPY file:7bed867b68b82c11d96a326acbe92a53eeb4b701a4a63e4b069dab774da39ed9 in /usr/share/buildinfo/labels.json      
# Thu, 18 Dec 2025 04:59:17 GMT
COPY file:7bed867b68b82c11d96a326acbe92a53eeb4b701a4a63e4b069dab774da39ed9 in /root/buildinfo/labels.json      
# Thu, 18 Dec 2025 04:59:17 GMT
LABEL "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="3dbd4aac2bce2ca6b13274bf0662e947c80b18b9" "org.opencontainers.image.revision"="3dbd4aac2bce2ca6b13274bf0662e947c80b18b9" "build-date"="2025-12-18T04:58:54Z" "org.opencontainers.image.created"="2025-12-18T04:58:54Z" "release"="1766033715"org.opencontainers.image.revision=3dbd4aac2bce2ca6b13274bf0662e947c80b18b9,org.opencontainers.image.created=2025-12-18T04:58:54Z
# Thu, 18 Dec 2025 22:23:23 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 18 Dec 2025 22:23:23 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 18 Dec 2025 22:23:23 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 18 Dec 2025 22:23:23 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en         gnupg2     ;     microdnf clean all # buildkit
# Thu, 18 Dec 2025 22:23:23 GMT
ENV JAVA_VERSION=jdk-25.0.1+8
# Thu, 18 Dec 2025 22:24:01 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='5c83b7d2121ed482fd06831a1eba1633dbab818aba6addddf48e075b97e6e9b8';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.1%2B8/OpenJDK25U-jdk_aarch64_linux_hotspot_25.0.1_8.tar.gz';          ;;        ppc64le)          ESUM='54fdfbfa2c463863bd0c2c9c19901320d25ca533f31daa0bd866c4104af7ce5b';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.1%2B8/OpenJDK25U-jdk_ppc64le_linux_hotspot_25.0.1_8.tar.gz';          ;;        s390x)          ESUM='1b627ec601998e5450fd1af91ae26a43b4d646403a8938d7efe4dfb2848fd896';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.1%2B8/OpenJDK25U-jdk_s390x_linux_hotspot_25.0.1_8.tar.gz';          ;;        x86_64)          ESUM='8daf77d1aacffe38c9889689bc224a13557de77559d9a5bb91991e6a298baa0d';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.1%2B8/OpenJDK25U-jdk_x64_linux_hotspot_25.0.1_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Thu, 18 Dec 2025 22:24:02 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 18 Dec 2025 22:24:02 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 18 Dec 2025 22:24:02 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 18 Dec 2025 22:24:02 GMT
CMD ["jshell"]
# Fri, 16 Jan 2026 21:45:03 GMT
CMD ["gradle"]
# Fri, 16 Jan 2026 21:45:03 GMT
ENV GRADLE_HOME=/opt/gradle
# Fri, 16 Jan 2026 21:45:03 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 101 gradle     && useradd --system --gid gradle --uid 101 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Fri, 16 Jan 2026 21:45:03 GMT
VOLUME [/home/gradle/.gradle]
# Fri, 16 Jan 2026 21:45:03 GMT
WORKDIR /home/gradle
# Fri, 16 Jan 2026 21:45:08 GMT
RUN set -o errexit -o nounset     && microdnf install -y         make         curl         wget         tar                 findutils                 unzip         which                 git         git-lfs         subversion     && microdnf clean all         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which svn # buildkit
# Fri, 16 Jan 2026 21:45:08 GMT
ENV GRADLE_VERSION=9.3.0
# Fri, 16 Jan 2026 21:45:08 GMT
ARG GRADLE_DOWNLOAD_SHA256=0d585f69da091fc5b2beced877feab55a3064d43b8a1d46aeb07996b0915e0e0
# Fri, 16 Jan 2026 21:45:10 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=0d585f69da091fc5b2beced877feab55a3064d43b8a1d46aeb07996b0915e0e0
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Fri, 16 Jan 2026 21:45:10 GMT
USER gradle
# Fri, 16 Jan 2026 21:45:10 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=0d585f69da091fc5b2beced877feab55a3064d43b8a1d46aeb07996b0915e0e0
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --stacktrace --debug --version # buildkit
# Fri, 16 Jan 2026 21:45:10 GMT
USER root
```

-	Layers:
	-	`sha256:bbf656ece02bf42bcb72be26aaced8f9084f91250ae2336e1f2b7b9e8b979727`  
		Last Modified: Thu, 18 Dec 2025 11:19:18 GMT  
		Size: 34.5 MB (34531778 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8947fa77d92236d7708c9dd5127ac319d0dfb66ecb4d8c6da34db59d00d2f794`  
		Last Modified: Thu, 18 Dec 2025 22:23:56 GMT  
		Size: 55.3 MB (55325417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29338c551bc45d0bbf250592970f7b04a06889a5263de0b2a62b1de9786c0775`  
		Last Modified: Thu, 18 Dec 2025 22:24:37 GMT  
		Size: 92.0 MB (92046730 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b64918ffbe1fcb54b48c258b0d75f9770542176ba71715557ce5efac2eec3783`  
		Last Modified: Thu, 18 Dec 2025 22:24:20 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a09c96aca76843dfcf6ddcadb47924b43be94dbf7859b0ddf753420265a1270f`  
		Last Modified: Thu, 18 Dec 2025 22:24:20 GMT  
		Size: 2.3 KB (2291 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:706c837cb11d1551a81a6713b369d84807339b815c2f7e663b397574cbba943a`  
		Last Modified: Fri, 16 Jan 2026 21:45:29 GMT  
		Size: 1.6 KB (1627 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a387ea86217f6b92d358216aef5ba2cb387cdaf8ad2b85def154dfb34738789f`  
		Last Modified: Fri, 16 Jan 2026 21:45:42 GMT  
		Size: 39.6 MB (39633479 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1a0689303fbcfd620b9e8c7307d8a3616783b78119572ec03abb9f670630f62`  
		Last Modified: Fri, 16 Jan 2026 21:46:00 GMT  
		Size: 137.0 MB (136988873 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7125bf02a526fed9a40a7f45129af2982ad30efa4125eface71728c7655f194`  
		Last Modified: Fri, 16 Jan 2026 21:45:38 GMT  
		Size: 25.6 KB (25590 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:ubi` - unknown; unknown

```console
$ docker pull gradle@sha256:8df066a8bea59bbfaa8b61648f17d50cadfec7e87b441563c6cea24bbb73c140
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.9 MB (8891385 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e2b48e2507468f3e727c388c41e29838b329198d72ab29863906d8f31ee9e59`

```dockerfile
```

-	Layers:
	-	`sha256:95df7fca6b649be7e8cf6f8d41da24b2c6687abdd6aeeed42ca9d4f5ce1d8fde`  
		Last Modified: Sat, 17 Jan 2026 00:27:00 GMT  
		Size: 8.9 MB (8866376 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:025fdf9570416b9975e28c2562cb0b85d97b7f84cc7cc9e9845445b6240d8181`  
		Last Modified: Fri, 16 Jan 2026 21:45:29 GMT  
		Size: 25.0 KB (25009 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:ubi` - linux; arm64 variant v8

```console
$ docker pull gradle@sha256:3471752d6d4a69e0060a03f01e7b288191118de32d10d1627bd63c90355e6f94
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **355.0 MB (354950952 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f2bb5e74426c179e65e22717bf91aa394264baee70d6eb958349a4a7db948fbc`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["gradle"]`

```dockerfile
# Thu, 18 Dec 2025 05:04:19 GMT
LABEL maintainer="Red Hat, Inc."
# Thu, 18 Dec 2025 05:04:19 GMT
LABEL vendor="Red Hat, Inc."
# Thu, 18 Dec 2025 05:04:19 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Thu, 18 Dec 2025 05:04:19 GMT
LABEL com.redhat.component="ubi10-minimal-container"       name="ubi10/ubi-minimal"       version="10.1"       cpe="cpe:/o:redhat:enterprise_linux:10.1"       distribution-scope="public"
# Thu, 18 Dec 2025 05:04:19 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Thu, 18 Dec 2025 05:04:19 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 10."
# Thu, 18 Dec 2025 05:04:19 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 18 Dec 2025 05:04:19 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 18 Dec 2025 05:04:19 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 10 Minimal"
# Thu, 18 Dec 2025 05:04:19 GMT
LABEL io.openshift.expose-services=""
# Thu, 18 Dec 2025 05:04:19 GMT
LABEL io.openshift.tags="minimal rhel10"
# Thu, 18 Dec 2025 05:04:19 GMT
ENV container oci
# Thu, 18 Dec 2025 05:04:20 GMT
COPY dir:04b750083472751a7f5154bb88e2ce4d0526c13f7486508dfd32af911f2d6c12 in /      
# Thu, 18 Dec 2025 05:04:20 GMT
COPY file:5de33b5fc08b00635bccf9134a18978dba13e2250aa51838f9969515a3957847 in /etc/yum.repos.d/.      
# Thu, 18 Dec 2025 05:04:20 GMT
CMD ["/bin/bash"]
# Thu, 18 Dec 2025 05:04:20 GMT
COPY file:595171150af68abc798ea385f7988d74b566aa8e84babff137f00b08b2164683 in /usr/share/buildinfo/content-sets.json      
# Thu, 18 Dec 2025 05:04:20 GMT
COPY file:595171150af68abc798ea385f7988d74b566aa8e84babff137f00b08b2164683 in /root/buildinfo/content_manifests/content-sets.json      
# Thu, 18 Dec 2025 05:04:20 GMT
COPY file:3a827beb44c0bded02518913eace1a58024dbf0ce6482c0f23a932e3e59b2536 in /usr/share/buildinfo/labels.json      
# Thu, 18 Dec 2025 05:04:20 GMT
COPY file:3a827beb44c0bded02518913eace1a58024dbf0ce6482c0f23a932e3e59b2536 in /root/buildinfo/labels.json      
# Thu, 18 Dec 2025 05:04:20 GMT
LABEL "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="3dbd4aac2bce2ca6b13274bf0662e947c80b18b9" "org.opencontainers.image.revision"="3dbd4aac2bce2ca6b13274bf0662e947c80b18b9" "build-date"="2025-12-18T05:03:56Z" "org.opencontainers.image.created"="2025-12-18T05:03:56Z" "release"="1766033715"org.opencontainers.image.revision=3dbd4aac2bce2ca6b13274bf0662e947c80b18b9,org.opencontainers.image.created=2025-12-18T05:03:56Z
# Thu, 18 Dec 2025 22:30:46 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 18 Dec 2025 22:30:46 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 18 Dec 2025 22:30:46 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 18 Dec 2025 22:30:46 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en         gnupg2     ;     microdnf clean all # buildkit
# Thu, 18 Dec 2025 22:30:46 GMT
ENV JAVA_VERSION=jdk-25.0.1+8
# Thu, 18 Dec 2025 22:30:52 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='5c83b7d2121ed482fd06831a1eba1633dbab818aba6addddf48e075b97e6e9b8';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.1%2B8/OpenJDK25U-jdk_aarch64_linux_hotspot_25.0.1_8.tar.gz';          ;;        ppc64le)          ESUM='54fdfbfa2c463863bd0c2c9c19901320d25ca533f31daa0bd866c4104af7ce5b';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.1%2B8/OpenJDK25U-jdk_ppc64le_linux_hotspot_25.0.1_8.tar.gz';          ;;        s390x)          ESUM='1b627ec601998e5450fd1af91ae26a43b4d646403a8938d7efe4dfb2848fd896';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.1%2B8/OpenJDK25U-jdk_s390x_linux_hotspot_25.0.1_8.tar.gz';          ;;        x86_64)          ESUM='8daf77d1aacffe38c9889689bc224a13557de77559d9a5bb91991e6a298baa0d';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.1%2B8/OpenJDK25U-jdk_x64_linux_hotspot_25.0.1_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Thu, 18 Dec 2025 22:30:54 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 18 Dec 2025 22:30:54 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 18 Dec 2025 22:30:54 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 18 Dec 2025 22:30:54 GMT
CMD ["jshell"]
# Fri, 16 Jan 2026 21:46:00 GMT
CMD ["gradle"]
# Fri, 16 Jan 2026 21:46:00 GMT
ENV GRADLE_HOME=/opt/gradle
# Fri, 16 Jan 2026 21:46:00 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 101 gradle     && useradd --system --gid gradle --uid 101 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Fri, 16 Jan 2026 21:46:00 GMT
VOLUME [/home/gradle/.gradle]
# Fri, 16 Jan 2026 21:46:00 GMT
WORKDIR /home/gradle
# Fri, 16 Jan 2026 21:46:05 GMT
RUN set -o errexit -o nounset     && microdnf install -y         make         curl         wget         tar                 findutils                 unzip         which                 git         git-lfs         subversion     && microdnf clean all         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which svn # buildkit
# Fri, 16 Jan 2026 21:46:05 GMT
ENV GRADLE_VERSION=9.3.0
# Fri, 16 Jan 2026 21:46:05 GMT
ARG GRADLE_DOWNLOAD_SHA256=0d585f69da091fc5b2beced877feab55a3064d43b8a1d46aeb07996b0915e0e0
# Fri, 16 Jan 2026 21:46:07 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=0d585f69da091fc5b2beced877feab55a3064d43b8a1d46aeb07996b0915e0e0
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Fri, 16 Jan 2026 21:46:07 GMT
USER gradle
# Fri, 16 Jan 2026 21:46:08 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=0d585f69da091fc5b2beced877feab55a3064d43b8a1d46aeb07996b0915e0e0
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --stacktrace --debug --version # buildkit
# Fri, 16 Jan 2026 21:46:08 GMT
USER root
```

-	Layers:
	-	`sha256:f416e7c13e96a1bec342af3e79184aaf45de55dd66939245eb76ca02465c54c7`  
		Last Modified: Thu, 18 Dec 2025 12:14:44 GMT  
		Size: 32.6 MB (32633678 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10d948260fbeb5898b951608e82c62c396441948bd58cf3487ddc75bc89feaff`  
		Last Modified: Thu, 18 Dec 2025 22:31:26 GMT  
		Size: 55.1 MB (55118598 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:945294a41f01a860ee896a3ed13082b932d47912020e6b4d067b64862718e4d2`  
		Last Modified: Thu, 18 Dec 2025 22:31:16 GMT  
		Size: 91.1 MB (91056299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:211de23a9661dc491541f18097deece8c7c0168be7865ed682032a65a678291c`  
		Last Modified: Thu, 18 Dec 2025 22:31:21 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:454027df0d82c1aadeb9d60c48487b1013c0fbbe040fe8ea9e1e8de3ef5150a4`  
		Last Modified: Thu, 18 Dec 2025 22:31:13 GMT  
		Size: 2.3 KB (2290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ea534e708ea26c7c0335a17869bb18b12de0b622bfbd3c55fc41a6ff3c31852`  
		Last Modified: Fri, 16 Jan 2026 21:46:37 GMT  
		Size: 1.6 KB (1628 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6e3d9029f7a9da2ad863ba4b766a749dde1aba49638a96390e2a513643180fc`  
		Last Modified: Fri, 16 Jan 2026 21:46:42 GMT  
		Size: 39.1 MB (39120104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:505b4aad9ddd6b7314b4e27fbc3bc317c9a91a32811bdd042b230f944948c546`  
		Last Modified: Fri, 16 Jan 2026 21:46:50 GMT  
		Size: 137.0 MB (136988874 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:803f1c487bfe68a61b286420e646202dd2888e5206a67bf8bca9d89a5a015d16`  
		Last Modified: Fri, 16 Jan 2026 21:46:37 GMT  
		Size: 29.3 KB (29321 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:ubi` - unknown; unknown

```console
$ docker pull gradle@sha256:43ce9bad437e8012bd4dad6237ed48aede1aaadad84ebb976333dcc46c021d2e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.9 MB (8889947 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:65a365d8237791a732fe66224a77c61fbd4502a7c253a2524aa2817470edcd67`

```dockerfile
```

-	Layers:
	-	`sha256:e6c22fe02a0a7a5941573d434ea71c41fe4673d75fb4faacbba141757431b79c`  
		Last Modified: Sat, 17 Jan 2026 00:27:11 GMT  
		Size: 8.9 MB (8864717 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6910d68a230e76e8d7a0a440d24714c07020d38cb4b860ef603cf6247e816faa`  
		Last Modified: Sat, 17 Jan 2026 00:27:12 GMT  
		Size: 25.2 KB (25230 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:ubi` - linux; ppc64le

```console
$ docker pull gradle@sha256:e7fbdeaae37f83142d44f595a95b3e5e91152c7dd5c91e23cc3ce2877fd91323
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **366.0 MB (366030219 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f8c1cb62f28335ded19ef8d0df5e08f107a846c8a495b9c8cb1f519d3724385c`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["gradle"]`

```dockerfile
# Thu, 18 Dec 2025 07:03:44 GMT
LABEL maintainer="Red Hat, Inc."
# Thu, 18 Dec 2025 07:03:44 GMT
LABEL vendor="Red Hat, Inc."
# Thu, 18 Dec 2025 07:03:44 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Thu, 18 Dec 2025 07:03:44 GMT
LABEL com.redhat.component="ubi10-minimal-container"       name="ubi10/ubi-minimal"       version="10.1"       cpe="cpe:/o:redhat:enterprise_linux:10.1"       distribution-scope="public"
# Thu, 18 Dec 2025 07:03:44 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Thu, 18 Dec 2025 07:03:44 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 10."
# Thu, 18 Dec 2025 07:03:44 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 18 Dec 2025 07:03:44 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 18 Dec 2025 07:03:44 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 10 Minimal"
# Thu, 18 Dec 2025 07:03:44 GMT
LABEL io.openshift.expose-services=""
# Thu, 18 Dec 2025 07:03:44 GMT
LABEL io.openshift.tags="minimal rhel10"
# Thu, 18 Dec 2025 07:03:44 GMT
ENV container oci
# Thu, 18 Dec 2025 07:03:45 GMT
COPY dir:530980282317924eec1c6623b725ebfc8622f7b70907079d2b485327f826b92a in /      
# Thu, 18 Dec 2025 07:03:45 GMT
COPY file:5de33b5fc08b00635bccf9134a18978dba13e2250aa51838f9969515a3957847 in /etc/yum.repos.d/.      
# Thu, 18 Dec 2025 07:03:45 GMT
CMD ["/bin/bash"]
# Thu, 18 Dec 2025 07:03:45 GMT
COPY file:595171150af68abc798ea385f7988d74b566aa8e84babff137f00b08b2164683 in /usr/share/buildinfo/content-sets.json      
# Thu, 18 Dec 2025 07:03:45 GMT
COPY file:595171150af68abc798ea385f7988d74b566aa8e84babff137f00b08b2164683 in /root/buildinfo/content_manifests/content-sets.json      
# Thu, 18 Dec 2025 07:03:45 GMT
COPY file:c62fb4530a421926bb6d3aa12f09ef125c8c4fff4293e7e931975ad4241f6f26 in /usr/share/buildinfo/labels.json      
# Thu, 18 Dec 2025 07:03:45 GMT
COPY file:c62fb4530a421926bb6d3aa12f09ef125c8c4fff4293e7e931975ad4241f6f26 in /root/buildinfo/labels.json      
# Thu, 18 Dec 2025 07:03:46 GMT
LABEL "architecture"="ppc64le" "vcs-type"="git" "vcs-ref"="3dbd4aac2bce2ca6b13274bf0662e947c80b18b9" "org.opencontainers.image.revision"="3dbd4aac2bce2ca6b13274bf0662e947c80b18b9" "build-date"="2025-12-18T07:03:33Z" "org.opencontainers.image.created"="2025-12-18T07:03:33Z" "release"="1766033715"org.opencontainers.image.revision=3dbd4aac2bce2ca6b13274bf0662e947c80b18b9,org.opencontainers.image.created=2025-12-18T07:03:33Z
# Thu, 18 Dec 2025 22:39:15 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 18 Dec 2025 22:39:15 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 18 Dec 2025 22:39:15 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 18 Dec 2025 22:39:15 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en         gnupg2     ;     microdnf clean all # buildkit
# Thu, 18 Dec 2025 22:39:15 GMT
ENV JAVA_VERSION=jdk-25.0.1+8
# Thu, 18 Dec 2025 22:44:01 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='5c83b7d2121ed482fd06831a1eba1633dbab818aba6addddf48e075b97e6e9b8';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.1%2B8/OpenJDK25U-jdk_aarch64_linux_hotspot_25.0.1_8.tar.gz';          ;;        ppc64le)          ESUM='54fdfbfa2c463863bd0c2c9c19901320d25ca533f31daa0bd866c4104af7ce5b';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.1%2B8/OpenJDK25U-jdk_ppc64le_linux_hotspot_25.0.1_8.tar.gz';          ;;        s390x)          ESUM='1b627ec601998e5450fd1af91ae26a43b4d646403a8938d7efe4dfb2848fd896';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.1%2B8/OpenJDK25U-jdk_s390x_linux_hotspot_25.0.1_8.tar.gz';          ;;        x86_64)          ESUM='8daf77d1aacffe38c9889689bc224a13557de77559d9a5bb91991e6a298baa0d';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.1%2B8/OpenJDK25U-jdk_x64_linux_hotspot_25.0.1_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Thu, 18 Dec 2025 22:44:04 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 18 Dec 2025 22:44:04 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 18 Dec 2025 22:44:04 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 18 Dec 2025 22:44:04 GMT
CMD ["jshell"]
# Fri, 16 Jan 2026 21:43:55 GMT
CMD ["gradle"]
# Fri, 16 Jan 2026 21:43:55 GMT
ENV GRADLE_HOME=/opt/gradle
# Fri, 16 Jan 2026 21:43:55 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 101 gradle     && useradd --system --gid gradle --uid 101 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Fri, 16 Jan 2026 21:43:55 GMT
VOLUME [/home/gradle/.gradle]
# Fri, 16 Jan 2026 21:43:56 GMT
WORKDIR /home/gradle
# Fri, 16 Jan 2026 21:45:03 GMT
RUN set -o errexit -o nounset     && microdnf install -y         make         curl         wget         tar                 findutils                 unzip         which                 git         git-lfs         subversion     && microdnf clean all         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which svn # buildkit
# Fri, 16 Jan 2026 21:45:03 GMT
ENV GRADLE_VERSION=9.3.0
# Fri, 16 Jan 2026 21:45:03 GMT
ARG GRADLE_DOWNLOAD_SHA256=0d585f69da091fc5b2beced877feab55a3064d43b8a1d46aeb07996b0915e0e0
# Fri, 16 Jan 2026 21:45:13 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=0d585f69da091fc5b2beced877feab55a3064d43b8a1d46aeb07996b0915e0e0
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Fri, 16 Jan 2026 21:45:13 GMT
USER gradle
# Fri, 16 Jan 2026 21:45:15 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=0d585f69da091fc5b2beced877feab55a3064d43b8a1d46aeb07996b0915e0e0
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --stacktrace --debug --version # buildkit
# Fri, 16 Jan 2026 21:45:15 GMT
USER root
```

-	Layers:
	-	`sha256:97de3b33554c63d2e40af1481c1da99bde18eb30eff5e4d230d8ec855811f50c`  
		Last Modified: Thu, 18 Dec 2025 12:14:46 GMT  
		Size: 38.7 MB (38688551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4559e7867acf4f05baf702a54db8a3e2cc5bd1a16c2dcecfa940d5c1ad1b6dfd`  
		Last Modified: Thu, 18 Dec 2025 22:40:19 GMT  
		Size: 57.3 MB (57343233 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c901f5c99cf57502e858b5eee1e9cc8e9f0a5466c9e20cb195509a3bcbce3752`  
		Last Modified: Thu, 18 Dec 2025 22:44:55 GMT  
		Size: 91.6 MB (91613031 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9272d59d36a69c550333e5d86a01e154f25e85274b5be59cd9c002913d038349`  
		Last Modified: Thu, 18 Dec 2025 22:45:01 GMT  
		Size: 131.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e080a7e257e17ddddc224c82b4261a30a07f093a8666045730d0d2fd4250839`  
		Last Modified: Thu, 18 Dec 2025 22:45:01 GMT  
		Size: 2.3 KB (2291 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ea22b56f9d329012c5d87c894a6802c4c5d99bc5458c9e54235c473163c1ad1`  
		Last Modified: Fri, 16 Jan 2026 21:46:21 GMT  
		Size: 1.6 KB (1628 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76a838b2dbfafd323ae38fe4df0a8628b6e83a4a6543b9171287931518fa1344`  
		Last Modified: Fri, 16 Jan 2026 21:46:23 GMT  
		Size: 41.4 MB (41392065 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e925d83b0cbefeba5582b24e44957b246004c7fc58d2a80b34f96d84453e4cda`  
		Last Modified: Fri, 16 Jan 2026 21:46:15 GMT  
		Size: 137.0 MB (136988877 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:448b2c29b2540660bc808f942c71f15f4a095184663b9979baa632eb0a4ea7f8`  
		Last Modified: Fri, 16 Jan 2026 21:46:21 GMT  
		Size: 380.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:ubi` - unknown; unknown

```console
$ docker pull gradle@sha256:1c98629c84ad5d023c4f63ca0f1ce5f208f9580091495337f2e8ffc19c8dbcdc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.9 MB (8884517 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de608113f0db789da7aa6005b090316432d01d26f397b9b6f2cf25f6b81672db`

```dockerfile
```

-	Layers:
	-	`sha256:b1f5aea4c379874ebe74df957d45f0201cadeeec97fc4c0019784f1a82f4d8ae`  
		Last Modified: Sat, 17 Jan 2026 00:27:20 GMT  
		Size: 8.9 MB (8859424 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:083fed0a0b49f8507d8f2bb97abc5fa89bde8bed3d8ea563ca4db0a616719b45`  
		Last Modified: Fri, 16 Jan 2026 21:46:09 GMT  
		Size: 25.1 KB (25093 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:ubi` - linux; s390x

```console
$ docker pull gradle@sha256:431b5b294e47877f035f2eacbbd7f00b154d6fe31374159eb72350c918935472
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **357.2 MB (357224455 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:59ce339c243c895d784e3aea8a4788c523befddabad6f77082f7a730381be1ce`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["gradle"]`

```dockerfile
# Thu, 18 Dec 2025 07:10:02 GMT
LABEL maintainer="Red Hat, Inc."
# Thu, 18 Dec 2025 07:10:02 GMT
LABEL vendor="Red Hat, Inc."
# Thu, 18 Dec 2025 07:10:02 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Thu, 18 Dec 2025 07:10:02 GMT
LABEL com.redhat.component="ubi10-minimal-container"       name="ubi10/ubi-minimal"       version="10.1"       cpe="cpe:/o:redhat:enterprise_linux:10.1"       distribution-scope="public"
# Thu, 18 Dec 2025 07:10:02 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Thu, 18 Dec 2025 07:10:02 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 10."
# Thu, 18 Dec 2025 07:10:02 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 18 Dec 2025 07:10:02 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 18 Dec 2025 07:10:02 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 10 Minimal"
# Thu, 18 Dec 2025 07:10:02 GMT
LABEL io.openshift.expose-services=""
# Thu, 18 Dec 2025 07:10:03 GMT
LABEL io.openshift.tags="minimal rhel10"
# Thu, 18 Dec 2025 07:10:03 GMT
ENV container oci
# Thu, 18 Dec 2025 07:10:03 GMT
COPY dir:7d54469de7c29eaa832f7e98c75ae08842b7fae9314e66ea7e9e482c3966eeca in /      
# Thu, 18 Dec 2025 07:10:03 GMT
COPY file:5de33b5fc08b00635bccf9134a18978dba13e2250aa51838f9969515a3957847 in /etc/yum.repos.d/.      
# Thu, 18 Dec 2025 07:10:03 GMT
CMD ["/bin/bash"]
# Thu, 18 Dec 2025 07:10:03 GMT
COPY file:595171150af68abc798ea385f7988d74b566aa8e84babff137f00b08b2164683 in /usr/share/buildinfo/content-sets.json      
# Thu, 18 Dec 2025 07:10:03 GMT
COPY file:595171150af68abc798ea385f7988d74b566aa8e84babff137f00b08b2164683 in /root/buildinfo/content_manifests/content-sets.json      
# Thu, 18 Dec 2025 07:10:03 GMT
COPY file:bea094e4f4ee0e91f623d002425004416b4556dc8f71bf399fffb85c16bafec5 in /usr/share/buildinfo/labels.json      
# Thu, 18 Dec 2025 07:10:03 GMT
COPY file:bea094e4f4ee0e91f623d002425004416b4556dc8f71bf399fffb85c16bafec5 in /root/buildinfo/labels.json      
# Thu, 18 Dec 2025 07:10:03 GMT
LABEL "architecture"="s390x" "vcs-type"="git" "vcs-ref"="3dbd4aac2bce2ca6b13274bf0662e947c80b18b9" "org.opencontainers.image.revision"="3dbd4aac2bce2ca6b13274bf0662e947c80b18b9" "build-date"="2025-12-18T07:07:43Z" "org.opencontainers.image.created"="2025-12-18T07:07:43Z" "release"="1766033715"org.opencontainers.image.revision=3dbd4aac2bce2ca6b13274bf0662e947c80b18b9,org.opencontainers.image.created=2025-12-18T07:07:43Z
# Thu, 18 Dec 2025 22:41:25 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 18 Dec 2025 22:41:25 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 18 Dec 2025 22:41:25 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 18 Dec 2025 22:41:25 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en         gnupg2     ;     microdnf clean all # buildkit
# Thu, 18 Dec 2025 22:41:25 GMT
ENV JAVA_VERSION=jdk-25.0.1+8
# Thu, 18 Dec 2025 22:42:21 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='5c83b7d2121ed482fd06831a1eba1633dbab818aba6addddf48e075b97e6e9b8';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.1%2B8/OpenJDK25U-jdk_aarch64_linux_hotspot_25.0.1_8.tar.gz';          ;;        ppc64le)          ESUM='54fdfbfa2c463863bd0c2c9c19901320d25ca533f31daa0bd866c4104af7ce5b';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.1%2B8/OpenJDK25U-jdk_ppc64le_linux_hotspot_25.0.1_8.tar.gz';          ;;        s390x)          ESUM='1b627ec601998e5450fd1af91ae26a43b4d646403a8938d7efe4dfb2848fd896';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.1%2B8/OpenJDK25U-jdk_s390x_linux_hotspot_25.0.1_8.tar.gz';          ;;        x86_64)          ESUM='8daf77d1aacffe38c9889689bc224a13557de77559d9a5bb91991e6a298baa0d';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.1%2B8/OpenJDK25U-jdk_x64_linux_hotspot_25.0.1_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Thu, 18 Dec 2025 22:42:22 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 18 Dec 2025 22:42:22 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 18 Dec 2025 22:42:22 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 18 Dec 2025 22:42:22 GMT
CMD ["jshell"]
# Fri, 16 Jan 2026 21:43:48 GMT
CMD ["gradle"]
# Fri, 16 Jan 2026 21:43:48 GMT
ENV GRADLE_HOME=/opt/gradle
# Fri, 16 Jan 2026 21:43:48 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 101 gradle     && useradd --system --gid gradle --uid 101 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Fri, 16 Jan 2026 21:43:48 GMT
VOLUME [/home/gradle/.gradle]
# Fri, 16 Jan 2026 21:43:48 GMT
WORKDIR /home/gradle
# Fri, 16 Jan 2026 21:43:54 GMT
RUN set -o errexit -o nounset     && microdnf install -y         make         curl         wget         tar                 findutils                 unzip         which                 git         git-lfs         subversion     && microdnf clean all         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which svn # buildkit
# Fri, 16 Jan 2026 21:43:54 GMT
ENV GRADLE_VERSION=9.3.0
# Fri, 16 Jan 2026 21:43:54 GMT
ARG GRADLE_DOWNLOAD_SHA256=0d585f69da091fc5b2beced877feab55a3064d43b8a1d46aeb07996b0915e0e0
# Fri, 16 Jan 2026 21:43:58 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=0d585f69da091fc5b2beced877feab55a3064d43b8a1d46aeb07996b0915e0e0
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Fri, 16 Jan 2026 21:43:58 GMT
USER gradle
# Fri, 16 Jan 2026 21:43:58 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=0d585f69da091fc5b2beced877feab55a3064d43b8a1d46aeb07996b0915e0e0
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --stacktrace --debug --version # buildkit
# Fri, 16 Jan 2026 21:43:58 GMT
USER root
```

-	Layers:
	-	`sha256:27a76ad55c4b879c1269027dfeec6783f235d82059544eeb7c62ecb7ad66011a`  
		Last Modified: Thu, 18 Dec 2025 12:14:48 GMT  
		Size: 34.3 MB (34340329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e63f770e95bcd442fbd4b8fd68cccd7a912d2dd01d01bf876299e3b9c4b8eeda`  
		Last Modified: Thu, 18 Dec 2025 22:42:09 GMT  
		Size: 55.9 MB (55921082 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52a86798b558efb4d8d875a179c4db868f45fc2c6dea17a636ad8a351d068c96`  
		Last Modified: Thu, 18 Dec 2025 22:42:48 GMT  
		Size: 88.2 MB (88211716 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9bf264ae291787a793a02fb55a8048dd9b401b80671dd4835b6ee5a717a4e3a0`  
		Last Modified: Thu, 18 Dec 2025 22:42:53 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22da806615f6d48dce6f9ae2432b30bd022d20e05181676062f89dd57706f466`  
		Last Modified: Thu, 18 Dec 2025 22:42:53 GMT  
		Size: 2.3 KB (2290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43979a3040ac782da79d8fb53c1c0a1b3167d7aeed352b63e36eb21fe2290a2d`  
		Last Modified: Fri, 16 Jan 2026 21:44:38 GMT  
		Size: 1.6 KB (1624 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0faccaaec265a4450b0788c5fd7d2bf9ee1c7a489f4b815595443428cfb368d`  
		Last Modified: Fri, 16 Jan 2026 21:44:42 GMT  
		Size: 41.8 MB (41758002 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4cd4f149c9666fc79e0f4c0eb7abd3ad99f71124a189510195410dce5dbbbc5`  
		Last Modified: Fri, 16 Jan 2026 21:44:33 GMT  
		Size: 137.0 MB (136988878 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45b4eeb5a00ccb451d0b68f970141ad75fe7977c1ae6e98ddee79c66bedcfd73`  
		Last Modified: Fri, 16 Jan 2026 21:44:38 GMT  
		Size: 374.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:ubi` - unknown; unknown

```console
$ docker pull gradle@sha256:437a8b1706306f342e75867ba6f95a00b17347fa4d66309825b046ccdb19b1c1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.9 MB (8874513 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:183f5590bd58ef78489bb2a9f3ef7b13c0c3a56a9f4c4397e8eaff81576fd413`

```dockerfile
```

-	Layers:
	-	`sha256:3be40bf6ec1c8c3bd5b264449b7b2963e5d1aea6b8f60f7a798a687a2baeb48e`  
		Last Modified: Sat, 17 Jan 2026 00:27:29 GMT  
		Size: 8.8 MB (8849507 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:66c83f0bf3f4843160b29a9404614c6171c749ad437dc7b08a5321634e8327fd`  
		Last Modified: Sat, 17 Jan 2026 00:27:30 GMT  
		Size: 25.0 KB (25006 bytes)  
		MIME: application/vnd.in-toto+json
