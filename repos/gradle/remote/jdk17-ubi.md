## `gradle:jdk17-ubi`

```console
$ docker pull gradle@sha256:52ccbd3c19696864e2009b94aadb03d098d11b692eb95217444d2c5e9e456e69
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
$ docker pull gradle@sha256:74459530ba4082105a84d20fe984d9bdb9b8385e376321da1d96cb741d6f9ad7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **394.3 MB (394310689 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a65391a0973597a9306b08acb6fcc9448e8d5809eb5134469e5aa655344ceb80`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["gradle"]`

```dockerfile
# Mon, 23 Mar 2026 01:13:56 GMT
LABEL maintainer="Red Hat, Inc."
# Mon, 23 Mar 2026 01:13:56 GMT
LABEL vendor="Red Hat, Inc."
# Mon, 23 Mar 2026 01:13:56 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Mon, 23 Mar 2026 01:13:56 GMT
LABEL com.redhat.component="ubi10-minimal-container"       name="ubi10/ubi-minimal"       version="10.1"       cpe="cpe:/o:redhat:enterprise_linux:10.1"       distribution-scope="public"
# Mon, 23 Mar 2026 01:13:56 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Mon, 23 Mar 2026 01:13:56 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 10."
# Mon, 23 Mar 2026 01:13:56 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 23 Mar 2026 01:13:56 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 23 Mar 2026 01:13:56 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 10 Minimal"
# Mon, 23 Mar 2026 01:13:56 GMT
LABEL io.openshift.expose-services=""
# Mon, 23 Mar 2026 01:13:56 GMT
LABEL io.openshift.tags="minimal rhel10"
# Mon, 23 Mar 2026 01:13:56 GMT
ENV container oci
# Mon, 23 Mar 2026 01:13:56 GMT
COPY dir:e4512bf3738a47eefff7ab81e82e38ca2f5173e43ee99a65e6dd13d89e02bd8f in /      
# Mon, 23 Mar 2026 01:13:56 GMT
COPY file:5de33b5fc08b00635bccf9134a18978dba13e2250aa51838f9969515a3957847 in /etc/yum.repos.d/.      
# Mon, 23 Mar 2026 01:13:57 GMT
CMD ["/bin/bash"]
# Mon, 23 Mar 2026 01:13:57 GMT
COPY file:595171150af68abc798ea385f7988d74b566aa8e84babff137f00b08b2164683 in /usr/share/buildinfo/content-sets.json      
# Mon, 23 Mar 2026 01:13:57 GMT
COPY file:595171150af68abc798ea385f7988d74b566aa8e84babff137f00b08b2164683 in /root/buildinfo/content_manifests/content-sets.json      
# Mon, 23 Mar 2026 01:13:57 GMT
COPY file:0abc55831e7dab59520989ee7f9e642cfb86d0399f7103e87f7378145dd94508 in /usr/share/buildinfo/labels.json      
# Mon, 23 Mar 2026 01:13:57 GMT
COPY file:0abc55831e7dab59520989ee7f9e642cfb86d0399f7103e87f7378145dd94508 in /root/buildinfo/labels.json      
# Mon, 23 Mar 2026 01:13:57 GMT
LABEL "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="5dc0ef0fb78e16b3f245c8e5fe3428173f80d0b6" "org.opencontainers.image.revision"="5dc0ef0fb78e16b3f245c8e5fe3428173f80d0b6" "build-date"="2026-03-23T01:13:42Z" "org.opencontainers.image.created"="2026-03-23T01:13:42Z" "release"="1774228210"org.opencontainers.image.revision=5dc0ef0fb78e16b3f245c8e5fe3428173f80d0b6,org.opencontainers.image.created=2026-03-23T01:13:42Z
# Mon, 23 Mar 2026 18:16:41 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 23 Mar 2026 18:16:41 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 23 Mar 2026 18:16:41 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 23 Mar 2026 18:16:41 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en         gnupg2     ;     microdnf clean all # buildkit
# Mon, 23 Mar 2026 18:16:41 GMT
ENV JAVA_VERSION=jdk-17.0.18+8
# Mon, 23 Mar 2026 18:17:14 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='592a6702b3a07a0e0b82cb38aaab149bfce1b0c24d6b57ddb410bd9009333095';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jdk_aarch64_linux_hotspot_17.0.18_8.tar.gz';          ;;        ppc64le)          ESUM='5ab89fbde560e1a09386f389dd7881715b896f49c6e9aa974f72d551337dba5e';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jdk_ppc64le_linux_hotspot_17.0.18_8.tar.gz';          ;;        s390x)          ESUM='3693469655bcfa2fa5e70907245a2b3bc4236db7d9fa1b9feb0ab7abd235da09';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jdk_s390x_linux_hotspot_17.0.18_8.tar.gz';          ;;        x86_64)          ESUM='0c94cbb54325c40dcf026143eb621562017db5525727f2d9131a11250f72c450';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jdk_x64_linux_hotspot_17.0.18_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Mon, 23 Mar 2026 18:17:15 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Mon, 23 Mar 2026 18:17:15 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Mon, 23 Mar 2026 18:17:15 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Mon, 23 Mar 2026 18:17:15 GMT
CMD ["jshell"]
# Mon, 23 Mar 2026 19:11:30 GMT
CMD ["gradle"]
# Mon, 23 Mar 2026 19:11:30 GMT
ENV GRADLE_HOME=/opt/gradle
# Mon, 23 Mar 2026 19:11:30 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 101 gradle     && useradd --system --gid gradle --uid 101 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Mon, 23 Mar 2026 19:11:30 GMT
VOLUME [/home/gradle/.gradle]
# Mon, 23 Mar 2026 19:11:30 GMT
WORKDIR /home/gradle
# Mon, 23 Mar 2026 19:11:34 GMT
RUN set -o errexit -o nounset     && microdnf install -y         make         curl-minimal         wget         tar                 findutils                 unzip         which                 git         git-lfs         subversion     && microdnf clean all         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which svn # buildkit
# Mon, 23 Mar 2026 19:11:34 GMT
ENV GRADLE_VERSION=9.4.1
# Mon, 23 Mar 2026 19:11:34 GMT
ARG GRADLE_DOWNLOAD_SHA256=2ab2958f2a1e51120c326cad6f385153bb11ee93b3c216c5fccebfdfbb7ec6cb
# Mon, 23 Mar 2026 19:11:37 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=2ab2958f2a1e51120c326cad6f385153bb11ee93b3c216c5fccebfdfbb7ec6cb
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Mon, 23 Mar 2026 19:11:37 GMT
USER gradle
# Mon, 23 Mar 2026 19:11:37 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=2ab2958f2a1e51120c326cad6f385153bb11ee93b3c216c5fccebfdfbb7ec6cb
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --stacktrace --debug --version # buildkit
# Mon, 23 Mar 2026 19:11:37 GMT
USER root
```

-	Layers:
	-	`sha256:2979ea27473f21e894361ff5d915252c378d4a8073aca3908465bbbf348780b7`  
		Last Modified: Mon, 23 Mar 2026 03:10:44 GMT  
		Size: 34.6 MB (34630234 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74d0832986a7ff4a71bd0147fcbf36f8bdfdd6ad730c95d6239831094a33254d`  
		Last Modified: Mon, 23 Mar 2026 18:17:01 GMT  
		Size: 37.4 MB (37446708 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41064d70cffea082e17f4981cb6c5543dc60af28d8d44de22f989e41e0184473`  
		Last Modified: Mon, 23 Mar 2026 18:17:36 GMT  
		Size: 145.6 MB (145637153 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b634749061fd64f399704a3e6189a725225243fa70494ba4433bf94f35c2adad`  
		Last Modified: Mon, 23 Mar 2026 18:17:32 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8df904bfeb513bb17453ec02dd10eaa17dca104bac7da0f5cf4e798385cf4bf3`  
		Last Modified: Mon, 23 Mar 2026 18:17:32 GMT  
		Size: 2.3 KB (2290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58896691d1e09d66f3476256e5be180660af65e9015fbac74c4b326e3af09862`  
		Last Modified: Mon, 23 Mar 2026 19:11:53 GMT  
		Size: 1.6 KB (1584 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72264e05403f785c9883ae62b68d3c3598949d996cb691d9fe03bf2c4755cd51`  
		Last Modified: Mon, 23 Mar 2026 19:11:55 GMT  
		Size: 38.8 MB (38758610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4c3301ec1c982da57aa983639d5646cf520ca0a2f3272a6c68077885724f50b`  
		Last Modified: Mon, 23 Mar 2026 19:11:57 GMT  
		Size: 137.8 MB (137808337 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76136df7900635cd10500c0ee08269b506e335f2b2b4265b9822b6f09207ba43`  
		Last Modified: Mon, 23 Mar 2026 19:11:54 GMT  
		Size: 25.6 KB (25612 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:jdk17-ubi` - unknown; unknown

```console
$ docker pull gradle@sha256:1aee88b138d91b8261c00c01adc498afc7a1b767156c662dd917a908f9c60569
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.1 MB (7051367 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e792a4fd432d3a79e275247b8f0f3f08e9a6a9bbc37e5b5e7a4543b9240f22d`

```dockerfile
```

-	Layers:
	-	`sha256:1fdb95fb8aadbc288c6059009c0b4c9e9b182c5aa960bb99c445bb59e78e4898`  
		Last Modified: Mon, 23 Mar 2026 19:11:54 GMT  
		Size: 7.0 MB (7026916 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7331208f705dc8d24d97a74fd39fc196cfc20815f776eaa016030a1f6c7fcf32`  
		Last Modified: Mon, 23 Mar 2026 19:11:53 GMT  
		Size: 24.5 KB (24451 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:jdk17-ubi` - linux; arm64 variant v8

```console
$ docker pull gradle@sha256:b0a7652b3b70ff96435968f57bd16e33dff5220bd91dcf37c70503caceca2f93
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **390.6 MB (390623022 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bafe318eb3834c0157648e51475a2c3ff9c9fabc686a17ee32ce2dc8aa48c861`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["gradle"]`

```dockerfile
# Mon, 23 Mar 2026 01:17:03 GMT
LABEL maintainer="Red Hat, Inc."
# Mon, 23 Mar 2026 01:17:03 GMT
LABEL vendor="Red Hat, Inc."
# Mon, 23 Mar 2026 01:17:03 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Mon, 23 Mar 2026 01:17:03 GMT
LABEL com.redhat.component="ubi10-minimal-container"       name="ubi10/ubi-minimal"       version="10.1"       cpe="cpe:/o:redhat:enterprise_linux:10.1"       distribution-scope="public"
# Mon, 23 Mar 2026 01:17:03 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Mon, 23 Mar 2026 01:17:03 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 10."
# Mon, 23 Mar 2026 01:17:03 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 23 Mar 2026 01:17:03 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 23 Mar 2026 01:17:03 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 10 Minimal"
# Mon, 23 Mar 2026 01:17:03 GMT
LABEL io.openshift.expose-services=""
# Mon, 23 Mar 2026 01:17:03 GMT
LABEL io.openshift.tags="minimal rhel10"
# Mon, 23 Mar 2026 01:17:03 GMT
ENV container oci
# Mon, 23 Mar 2026 01:17:04 GMT
COPY dir:5423a2d232cda7a57202522795efee6ca78fcc0651e41ab821993b780fdf8627 in /      
# Mon, 23 Mar 2026 01:17:04 GMT
COPY file:5de33b5fc08b00635bccf9134a18978dba13e2250aa51838f9969515a3957847 in /etc/yum.repos.d/.      
# Mon, 23 Mar 2026 01:17:04 GMT
CMD ["/bin/bash"]
# Mon, 23 Mar 2026 01:17:04 GMT
COPY file:595171150af68abc798ea385f7988d74b566aa8e84babff137f00b08b2164683 in /usr/share/buildinfo/content-sets.json      
# Mon, 23 Mar 2026 01:17:05 GMT
COPY file:595171150af68abc798ea385f7988d74b566aa8e84babff137f00b08b2164683 in /root/buildinfo/content_manifests/content-sets.json      
# Mon, 23 Mar 2026 01:17:05 GMT
COPY file:c5d7f4f2dd90b98f707a017338d65e0949c625a6c68e260ee9a0d4613ffd89fd in /usr/share/buildinfo/labels.json      
# Mon, 23 Mar 2026 01:17:05 GMT
COPY file:c5d7f4f2dd90b98f707a017338d65e0949c625a6c68e260ee9a0d4613ffd89fd in /root/buildinfo/labels.json      
# Mon, 23 Mar 2026 01:17:05 GMT
LABEL "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="5dc0ef0fb78e16b3f245c8e5fe3428173f80d0b6" "org.opencontainers.image.revision"="5dc0ef0fb78e16b3f245c8e5fe3428173f80d0b6" "build-date"="2026-03-23T01:16:47Z" "org.opencontainers.image.created"="2026-03-23T01:16:47Z" "release"="1774228210"org.opencontainers.image.revision=5dc0ef0fb78e16b3f245c8e5fe3428173f80d0b6,org.opencontainers.image.created=2026-03-23T01:16:47Z
# Mon, 23 Mar 2026 18:16:48 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 23 Mar 2026 18:16:48 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 23 Mar 2026 18:16:48 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 23 Mar 2026 18:16:48 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en         gnupg2     ;     microdnf clean all # buildkit
# Mon, 23 Mar 2026 18:16:48 GMT
ENV JAVA_VERSION=jdk-17.0.18+8
# Mon, 23 Mar 2026 18:16:54 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='592a6702b3a07a0e0b82cb38aaab149bfce1b0c24d6b57ddb410bd9009333095';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jdk_aarch64_linux_hotspot_17.0.18_8.tar.gz';          ;;        ppc64le)          ESUM='5ab89fbde560e1a09386f389dd7881715b896f49c6e9aa974f72d551337dba5e';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jdk_ppc64le_linux_hotspot_17.0.18_8.tar.gz';          ;;        s390x)          ESUM='3693469655bcfa2fa5e70907245a2b3bc4236db7d9fa1b9feb0ab7abd235da09';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jdk_s390x_linux_hotspot_17.0.18_8.tar.gz';          ;;        x86_64)          ESUM='0c94cbb54325c40dcf026143eb621562017db5525727f2d9131a11250f72c450';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jdk_x64_linux_hotspot_17.0.18_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Mon, 23 Mar 2026 18:16:56 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Mon, 23 Mar 2026 18:16:56 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Mon, 23 Mar 2026 18:16:56 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Mon, 23 Mar 2026 18:16:56 GMT
CMD ["jshell"]
# Mon, 23 Mar 2026 19:11:11 GMT
CMD ["gradle"]
# Mon, 23 Mar 2026 19:11:11 GMT
ENV GRADLE_HOME=/opt/gradle
# Mon, 23 Mar 2026 19:11:11 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 101 gradle     && useradd --system --gid gradle --uid 101 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Mon, 23 Mar 2026 19:11:11 GMT
VOLUME [/home/gradle/.gradle]
# Mon, 23 Mar 2026 19:11:11 GMT
WORKDIR /home/gradle
# Mon, 23 Mar 2026 19:11:15 GMT
RUN set -o errexit -o nounset     && microdnf install -y         make         curl-minimal         wget         tar                 findutils                 unzip         which                 git         git-lfs         subversion     && microdnf clean all         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which svn # buildkit
# Mon, 23 Mar 2026 19:11:15 GMT
ENV GRADLE_VERSION=9.4.1
# Mon, 23 Mar 2026 19:11:15 GMT
ARG GRADLE_DOWNLOAD_SHA256=2ab2958f2a1e51120c326cad6f385153bb11ee93b3c216c5fccebfdfbb7ec6cb
# Mon, 23 Mar 2026 19:11:18 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=2ab2958f2a1e51120c326cad6f385153bb11ee93b3c216c5fccebfdfbb7ec6cb
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Mon, 23 Mar 2026 19:11:18 GMT
USER gradle
# Mon, 23 Mar 2026 19:11:18 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=2ab2958f2a1e51120c326cad6f385153bb11ee93b3c216c5fccebfdfbb7ec6cb
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --stacktrace --debug --version # buildkit
# Mon, 23 Mar 2026 19:11:18 GMT
USER root
```

-	Layers:
	-	`sha256:cbfdca2ca63ac63914141abb4cb933134b748fc3efb6e835daea267d6feb9296`  
		Last Modified: Mon, 23 Mar 2026 03:33:50 GMT  
		Size: 32.7 MB (32686471 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9176ca794d3857d1a4e75d7fbeacc8b8807872cefdeb0112a40d62c6ff3b3a8`  
		Last Modified: Mon, 23 Mar 2026 18:17:14 GMT  
		Size: 37.4 MB (37389043 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:816e9e6681189b2775bc7b2f42f7cecff125f91fd66d4fbc0a54797981367bb9`  
		Last Modified: Mon, 23 Mar 2026 18:17:17 GMT  
		Size: 144.4 MB (144446607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99b132c3bcccc6b034bd54587fdaafe753cc9e6909e5d3ef94f2bd6053cfcdda`  
		Last Modified: Mon, 23 Mar 2026 18:17:13 GMT  
		Size: 130.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:201ebe98b0a2f762079e7567ac91bf4681eec8ec607683a8c5838715f53b70a5`  
		Last Modified: Mon, 23 Mar 2026 18:17:13 GMT  
		Size: 2.3 KB (2291 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0bc9c334e73aa134cc129f582d60a79e8931b43f2b555e78f577911b62fb5ac`  
		Last Modified: Mon, 23 Mar 2026 19:11:37 GMT  
		Size: 1.6 KB (1583 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:afc02db9293bfc2c7f3b24f183399d3e5add4f144337748eadb1c3f3f29afad8`  
		Last Modified: Mon, 23 Mar 2026 19:11:38 GMT  
		Size: 38.3 MB (38259198 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:933d23cbb350427e2cbe90b8a7d618b396a9f8c038623044c60108aef7d87080`  
		Last Modified: Mon, 23 Mar 2026 19:11:40 GMT  
		Size: 137.8 MB (137808332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbecb5b687529cabadc13f5c7a7efdedc43021bcb04bfbad2b698d93775a989e`  
		Last Modified: Mon, 23 Mar 2026 19:11:37 GMT  
		Size: 29.3 KB (29335 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:jdk17-ubi` - unknown; unknown

```console
$ docker pull gradle@sha256:7d09a1126d00f03306f86acc1358972a578791ad5b453594d10dc20c263be3a4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 MB (7049820 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e4c7d115a2802e9ae43a7e52233cba24a2f530d33bcf4371a7101627834a8bf`

```dockerfile
```

-	Layers:
	-	`sha256:beeba3755aa3a9fccd5ddb0c14b5dfa1d482153077c770ee319c73e9df3cacd4`  
		Last Modified: Mon, 23 Mar 2026 19:11:37 GMT  
		Size: 7.0 MB (7025172 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f72fb10b2d3b1177347a1d16d0e523d110175e048b89e6948731af9794149833`  
		Last Modified: Mon, 23 Mar 2026 19:11:36 GMT  
		Size: 24.6 KB (24648 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:jdk17-ubi` - linux; ppc64le

```console
$ docker pull gradle@sha256:fc0d31850713265986123a151e0fa2bda9d6a1eb112a7c3b0dc0275fe34a1206
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **401.7 MB (401705353 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea14d705863cf6ba7d6e5228919f4bd5e0b79b106852a6478cf49faf86809909`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["gradle"]`

```dockerfile
# Mon, 23 Mar 2026 01:15:45 GMT
LABEL maintainer="Red Hat, Inc."
# Mon, 23 Mar 2026 01:15:45 GMT
LABEL vendor="Red Hat, Inc."
# Mon, 23 Mar 2026 01:15:45 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Mon, 23 Mar 2026 01:15:45 GMT
LABEL com.redhat.component="ubi10-minimal-container"       name="ubi10/ubi-minimal"       version="10.1"       cpe="cpe:/o:redhat:enterprise_linux:10.1"       distribution-scope="public"
# Mon, 23 Mar 2026 01:15:45 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Mon, 23 Mar 2026 01:15:45 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 10."
# Mon, 23 Mar 2026 01:15:45 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 23 Mar 2026 01:15:46 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 23 Mar 2026 01:15:46 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 10 Minimal"
# Mon, 23 Mar 2026 01:15:46 GMT
LABEL io.openshift.expose-services=""
# Mon, 23 Mar 2026 01:15:46 GMT
LABEL io.openshift.tags="minimal rhel10"
# Mon, 23 Mar 2026 01:15:46 GMT
ENV container oci
# Mon, 23 Mar 2026 01:15:46 GMT
COPY dir:6d632c778a00dcaccd2b27492019a49da2e9ded15d90cc220bd8ef2e111c01aa in /      
# Mon, 23 Mar 2026 01:15:46 GMT
COPY file:5de33b5fc08b00635bccf9134a18978dba13e2250aa51838f9969515a3957847 in /etc/yum.repos.d/.      
# Mon, 23 Mar 2026 01:15:46 GMT
CMD ["/bin/bash"]
# Mon, 23 Mar 2026 01:15:46 GMT
COPY file:595171150af68abc798ea385f7988d74b566aa8e84babff137f00b08b2164683 in /usr/share/buildinfo/content-sets.json      
# Mon, 23 Mar 2026 01:15:46 GMT
COPY file:595171150af68abc798ea385f7988d74b566aa8e84babff137f00b08b2164683 in /root/buildinfo/content_manifests/content-sets.json      
# Mon, 23 Mar 2026 01:15:47 GMT
COPY file:c49dc785bea5c076578ee2a5e8eb4e7290c033b08769d6c1e8e12f43990c44cc in /usr/share/buildinfo/labels.json      
# Mon, 23 Mar 2026 01:15:47 GMT
COPY file:c49dc785bea5c076578ee2a5e8eb4e7290c033b08769d6c1e8e12f43990c44cc in /root/buildinfo/labels.json      
# Mon, 23 Mar 2026 01:15:47 GMT
LABEL "architecture"="ppc64le" "vcs-type"="git" "vcs-ref"="5dc0ef0fb78e16b3f245c8e5fe3428173f80d0b6" "org.opencontainers.image.revision"="5dc0ef0fb78e16b3f245c8e5fe3428173f80d0b6" "build-date"="2026-03-23T01:15:34Z" "org.opencontainers.image.created"="2026-03-23T01:15:34Z" "release"="1774228210"org.opencontainers.image.revision=5dc0ef0fb78e16b3f245c8e5fe3428173f80d0b6,org.opencontainers.image.created=2026-03-23T01:15:34Z
# Mon, 23 Mar 2026 18:25:02 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 23 Mar 2026 18:25:02 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 23 Mar 2026 18:25:02 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 23 Mar 2026 18:25:02 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en         gnupg2     ;     microdnf clean all # buildkit
# Mon, 23 Mar 2026 18:25:02 GMT
ENV JAVA_VERSION=jdk-17.0.18+8
# Mon, 23 Mar 2026 18:27:01 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='592a6702b3a07a0e0b82cb38aaab149bfce1b0c24d6b57ddb410bd9009333095';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jdk_aarch64_linux_hotspot_17.0.18_8.tar.gz';          ;;        ppc64le)          ESUM='5ab89fbde560e1a09386f389dd7881715b896f49c6e9aa974f72d551337dba5e';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jdk_ppc64le_linux_hotspot_17.0.18_8.tar.gz';          ;;        s390x)          ESUM='3693469655bcfa2fa5e70907245a2b3bc4236db7d9fa1b9feb0ab7abd235da09';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jdk_s390x_linux_hotspot_17.0.18_8.tar.gz';          ;;        x86_64)          ESUM='0c94cbb54325c40dcf026143eb621562017db5525727f2d9131a11250f72c450';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jdk_x64_linux_hotspot_17.0.18_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Mon, 23 Mar 2026 18:27:04 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Mon, 23 Mar 2026 18:27:04 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Mon, 23 Mar 2026 18:27:04 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Mon, 23 Mar 2026 18:27:04 GMT
CMD ["jshell"]
# Mon, 23 Mar 2026 19:11:13 GMT
CMD ["gradle"]
# Mon, 23 Mar 2026 19:11:13 GMT
ENV GRADLE_HOME=/opt/gradle
# Mon, 23 Mar 2026 19:11:13 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 101 gradle     && useradd --system --gid gradle --uid 101 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Mon, 23 Mar 2026 19:11:13 GMT
VOLUME [/home/gradle/.gradle]
# Mon, 23 Mar 2026 19:11:13 GMT
WORKDIR /home/gradle
# Mon, 23 Mar 2026 19:11:28 GMT
RUN set -o errexit -o nounset     && microdnf install -y         make         curl-minimal         wget         tar                 findutils                 unzip         which                 git         git-lfs         subversion     && microdnf clean all         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which svn # buildkit
# Mon, 23 Mar 2026 19:11:28 GMT
ENV GRADLE_VERSION=9.4.1
# Mon, 23 Mar 2026 19:11:28 GMT
ARG GRADLE_DOWNLOAD_SHA256=2ab2958f2a1e51120c326cad6f385153bb11ee93b3c216c5fccebfdfbb7ec6cb
# Mon, 23 Mar 2026 19:11:34 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=2ab2958f2a1e51120c326cad6f385153bb11ee93b3c216c5fccebfdfbb7ec6cb
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Mon, 23 Mar 2026 19:11:34 GMT
USER gradle
# Mon, 23 Mar 2026 19:11:37 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=2ab2958f2a1e51120c326cad6f385153bb11ee93b3c216c5fccebfdfbb7ec6cb
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --stacktrace --debug --version # buildkit
# Mon, 23 Mar 2026 19:11:37 GMT
USER root
```

-	Layers:
	-	`sha256:6b71f50ac5496b49a24d4e0868fe8e453f93532ef823631b2317185af571b8e7`  
		Last Modified: Mon, 23 Mar 2026 06:15:15 GMT  
		Size: 38.7 MB (38727029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93c8eaa293db94961782c260ece22ece0b24bab37073f3fe6b143b29d7b188a9`  
		Last Modified: Mon, 23 Mar 2026 18:25:46 GMT  
		Size: 39.2 MB (39200511 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:840bb311f1cabddc8b9851f1b4482e8d346f40e04733d1ae0dca026dce0522c1`  
		Last Modified: Mon, 23 Mar 2026 18:27:43 GMT  
		Size: 145.5 MB (145459990 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ff94e59941aa5d659e98a59e8c191b0c199303b427503beb943484732592c30`  
		Last Modified: Mon, 23 Mar 2026 18:27:39 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5908348e98dce1c7021f4af8314cd1df0e65ade0e4e29cb26e94cd73c31c0e64`  
		Last Modified: Mon, 23 Mar 2026 18:27:39 GMT  
		Size: 2.3 KB (2290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2f85f4c4f51b977457436f30b5bd3ef48d1981dd5a902d6aae21d0966a7c49f`  
		Last Modified: Mon, 23 Mar 2026 19:12:22 GMT  
		Size: 1.6 KB (1590 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79381e5c98e058b59f1c24022d32d49a1cf7eae4aaf3d755a7367e2d7458538f`  
		Last Modified: Mon, 23 Mar 2026 19:12:24 GMT  
		Size: 40.5 MB (40505069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:531e62fa0ff4a1330c436cdb3619e4e1d952e4e058deb9413a83f2305ecac37f`  
		Last Modified: Mon, 23 Mar 2026 19:12:27 GMT  
		Size: 137.8 MB (137808335 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04c232888c038fa59e070ade73fbaa79de94f9bb44f253afff760095352565b9`  
		Last Modified: Mon, 23 Mar 2026 19:12:22 GMT  
		Size: 379.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:jdk17-ubi` - unknown; unknown

```console
$ docker pull gradle@sha256:393a2cdbe94c29146294a858865905844688e7d6509d0d93fb88fb9dc7de6402
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 MB (7042857 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad39f6a87b68ee95bb4a7979e6fcb37d252428faa6e452b7286f96abb829bc98`

```dockerfile
```

-	Layers:
	-	`sha256:0281343e3e4b47a2f38605aa6d869e673cf1637103b311d43646b21eecf146e6`  
		Last Modified: Mon, 23 Mar 2026 19:12:22 GMT  
		Size: 7.0 MB (7018334 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f1d22c7d16dd7d886cbfaab0b2f053aadf7db84d3825c806f5aebd7b427811b9`  
		Last Modified: Mon, 23 Mar 2026 19:12:22 GMT  
		Size: 24.5 KB (24523 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:jdk17-ubi` - linux; s390x

```console
$ docker pull gradle@sha256:8f652e94b6df7f966671ea32ec3b221e396fccadbc623c6fc4f10d9daa247a2e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **386.6 MB (386560170 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9825e335d2cc1b1e8fc26263b59c84b9d63bd79cca7dc3986e2fda31d5ccddc6`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["gradle"]`

```dockerfile
# Mon, 23 Mar 2026 01:50:52 GMT
LABEL maintainer="Red Hat, Inc."
# Mon, 23 Mar 2026 01:50:52 GMT
LABEL vendor="Red Hat, Inc."
# Mon, 23 Mar 2026 01:50:52 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Mon, 23 Mar 2026 01:50:52 GMT
LABEL com.redhat.component="ubi10-minimal-container"       name="ubi10/ubi-minimal"       version="10.1"       cpe="cpe:/o:redhat:enterprise_linux:10.1"       distribution-scope="public"
# Mon, 23 Mar 2026 01:50:52 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Mon, 23 Mar 2026 01:50:52 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 10."
# Mon, 23 Mar 2026 01:50:52 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 23 Mar 2026 01:50:52 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 23 Mar 2026 01:50:52 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 10 Minimal"
# Mon, 23 Mar 2026 01:50:52 GMT
LABEL io.openshift.expose-services=""
# Mon, 23 Mar 2026 01:50:52 GMT
LABEL io.openshift.tags="minimal rhel10"
# Mon, 23 Mar 2026 01:50:52 GMT
ENV container oci
# Mon, 23 Mar 2026 01:50:53 GMT
COPY dir:a20807155e5dba5b4fe6159d124b2858e52124008e54fbaacb8e89f074571573 in /      
# Mon, 23 Mar 2026 01:50:53 GMT
COPY file:5de33b5fc08b00635bccf9134a18978dba13e2250aa51838f9969515a3957847 in /etc/yum.repos.d/.      
# Mon, 23 Mar 2026 01:50:53 GMT
CMD ["/bin/bash"]
# Mon, 23 Mar 2026 01:50:53 GMT
COPY file:595171150af68abc798ea385f7988d74b566aa8e84babff137f00b08b2164683 in /usr/share/buildinfo/content-sets.json      
# Mon, 23 Mar 2026 01:50:53 GMT
COPY file:595171150af68abc798ea385f7988d74b566aa8e84babff137f00b08b2164683 in /root/buildinfo/content_manifests/content-sets.json      
# Mon, 23 Mar 2026 01:50:53 GMT
COPY file:f444544eabeceb45eb54e7d25741c29001ce8ceeb34cf764e4e6f1bae0509e32 in /usr/share/buildinfo/labels.json      
# Mon, 23 Mar 2026 01:50:53 GMT
COPY file:f444544eabeceb45eb54e7d25741c29001ce8ceeb34cf764e4e6f1bae0509e32 in /root/buildinfo/labels.json      
# Mon, 23 Mar 2026 01:50:53 GMT
LABEL "architecture"="s390x" "vcs-type"="git" "vcs-ref"="5dc0ef0fb78e16b3f245c8e5fe3428173f80d0b6" "org.opencontainers.image.revision"="5dc0ef0fb78e16b3f245c8e5fe3428173f80d0b6" "build-date"="2026-03-23T01:50:09Z" "org.opencontainers.image.created"="2026-03-23T01:50:09Z" "release"="1774228210"org.opencontainers.image.revision=5dc0ef0fb78e16b3f245c8e5fe3428173f80d0b6,org.opencontainers.image.created=2026-03-23T01:50:09Z
# Mon, 23 Mar 2026 18:13:05 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 23 Mar 2026 18:13:05 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 23 Mar 2026 18:13:05 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 23 Mar 2026 18:13:05 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en         gnupg2     ;     microdnf clean all # buildkit
# Mon, 23 Mar 2026 18:13:05 GMT
ENV JAVA_VERSION=jdk-17.0.18+8
# Mon, 23 Mar 2026 18:13:11 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='592a6702b3a07a0e0b82cb38aaab149bfce1b0c24d6b57ddb410bd9009333095';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jdk_aarch64_linux_hotspot_17.0.18_8.tar.gz';          ;;        ppc64le)          ESUM='5ab89fbde560e1a09386f389dd7881715b896f49c6e9aa974f72d551337dba5e';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jdk_ppc64le_linux_hotspot_17.0.18_8.tar.gz';          ;;        s390x)          ESUM='3693469655bcfa2fa5e70907245a2b3bc4236db7d9fa1b9feb0ab7abd235da09';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jdk_s390x_linux_hotspot_17.0.18_8.tar.gz';          ;;        x86_64)          ESUM='0c94cbb54325c40dcf026143eb621562017db5525727f2d9131a11250f72c450';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jdk_x64_linux_hotspot_17.0.18_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Mon, 23 Mar 2026 18:13:12 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Mon, 23 Mar 2026 18:13:12 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Mon, 23 Mar 2026 18:13:12 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Mon, 23 Mar 2026 18:13:12 GMT
CMD ["jshell"]
# Mon, 23 Mar 2026 19:09:53 GMT
CMD ["gradle"]
# Mon, 23 Mar 2026 19:09:53 GMT
ENV GRADLE_HOME=/opt/gradle
# Mon, 23 Mar 2026 19:09:53 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 101 gradle     && useradd --system --gid gradle --uid 101 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Mon, 23 Mar 2026 19:09:53 GMT
VOLUME [/home/gradle/.gradle]
# Mon, 23 Mar 2026 19:09:53 GMT
WORKDIR /home/gradle
# Mon, 23 Mar 2026 19:10:02 GMT
RUN set -o errexit -o nounset     && microdnf install -y         make         curl-minimal         wget         tar                 findutils                 unzip         which                 git         git-lfs         subversion     && microdnf clean all         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which svn # buildkit
# Mon, 23 Mar 2026 19:10:02 GMT
ENV GRADLE_VERSION=9.4.1
# Mon, 23 Mar 2026 19:10:02 GMT
ARG GRADLE_DOWNLOAD_SHA256=2ab2958f2a1e51120c326cad6f385153bb11ee93b3c216c5fccebfdfbb7ec6cb
# Mon, 23 Mar 2026 19:10:06 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=2ab2958f2a1e51120c326cad6f385153bb11ee93b3c216c5fccebfdfbb7ec6cb
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Mon, 23 Mar 2026 19:10:06 GMT
USER gradle
# Mon, 23 Mar 2026 19:10:06 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=2ab2958f2a1e51120c326cad6f385153bb11ee93b3c216c5fccebfdfbb7ec6cb
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --stacktrace --debug --version # buildkit
# Mon, 23 Mar 2026 19:10:06 GMT
USER root
```

-	Layers:
	-	`sha256:0c4143dec68dd3a33451fd532f787cf2f31d86a312b4b1a8a58cadb88900ac88`  
		Last Modified: Mon, 23 Mar 2026 06:15:08 GMT  
		Size: 34.4 MB (34429605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0096b18c6452ca9362ab2bf91aec0cfa3229770ce6ac58baaf56ec226599a50c`  
		Last Modified: Mon, 23 Mar 2026 18:13:28 GMT  
		Size: 37.8 MB (37827761 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6ea4a8cad356622c1a3733587ae7e96a1aa206acecd55df231c0215b03cd5bc`  
		Last Modified: Mon, 23 Mar 2026 18:13:39 GMT  
		Size: 135.6 MB (135629161 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25f630a3c02fce0dd81ceae66a12f862d3ca88223bf9e4d4d830f2fa98aa8e9d`  
		Last Modified: Mon, 23 Mar 2026 18:13:36 GMT  
		Size: 130.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f22a9c89aa8fca16743b7663c5ad213ef8e345dc4e4ed30b5df9d5bb649ae00`  
		Last Modified: Mon, 23 Mar 2026 18:13:27 GMT  
		Size: 2.3 KB (2289 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e8ceaeffd29dae208ac262764a58b9bba432fd3a1f4d772d5965a137d3b15fc`  
		Last Modified: Mon, 23 Mar 2026 19:10:34 GMT  
		Size: 1.6 KB (1584 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6aafea4538e6946b84155007333fa5ee8df90cf363a7ed6e3c3303ccb23931a5`  
		Last Modified: Mon, 23 Mar 2026 19:10:35 GMT  
		Size: 40.9 MB (40860902 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d092478b0c1b724328d67eede1b29edd11ecd42b5ad8863bd927ea6cd44f1f10`  
		Last Modified: Mon, 23 Mar 2026 19:10:37 GMT  
		Size: 137.8 MB (137808332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa7b3bc8eecc8ef4a16589ee6fa8caf7dd048feec6723a2f42691beb0be0df26`  
		Last Modified: Mon, 23 Mar 2026 19:10:34 GMT  
		Size: 374.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:jdk17-ubi` - unknown; unknown

```console
$ docker pull gradle@sha256:974b4ad1d463e9e1a5e6e74f79078a1febe96b71c56af3884b6995f71465ef3a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 MB (7032012 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:41382993fa5f5ba61da21b0d92544e9fc1c7be698d3b9033903190e6247a3e6b`

```dockerfile
```

-	Layers:
	-	`sha256:900b5e8e3e74c71c6833b51d4a78c312906c9041d83246a26d3319ac69832248`  
		Last Modified: Mon, 23 Mar 2026 19:10:34 GMT  
		Size: 7.0 MB (7007563 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9ce52851c111160983e815afc70b1140be47dfbcb6a6c720251d26a231283b0e`  
		Last Modified: Mon, 23 Mar 2026 19:10:34 GMT  
		Size: 24.4 KB (24449 bytes)  
		MIME: application/vnd.in-toto+json
