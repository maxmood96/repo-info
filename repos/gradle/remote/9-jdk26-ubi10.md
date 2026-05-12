## `gradle:9-jdk26-ubi10`

```console
$ docker pull gradle@sha256:92fc2c0ce7dfa28430e4b3e4f71697bea4be540f7a595a54ee319ff4fd21750b
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

### `gradle:9-jdk26-ubi10` - linux; amd64

```console
$ docker pull gradle@sha256:3ae6c54d97734939c68161fe13b2712860873af789feac99e814398269b7d6d4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **345.7 MB (345676319 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b1d2ebc020ca3932992d651b01b8eb02b4e01ecd213930597638f05e1a02cc81`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["gradle"]`

```dockerfile
# Mon, 11 May 2026 01:16:15 GMT
LABEL maintainer="Red Hat, Inc."
# Mon, 11 May 2026 01:16:15 GMT
LABEL vendor="Red Hat, Inc."
# Mon, 11 May 2026 01:16:15 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Mon, 11 May 2026 01:16:15 GMT
LABEL com.redhat.component="ubi10-minimal-container"       name="ubi10/ubi-minimal"       version="10.1"       cpe="cpe:/o:redhat:enterprise_linux:10.1"       distribution-scope="public"
# Mon, 11 May 2026 01:16:15 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Mon, 11 May 2026 01:16:15 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 10."
# Mon, 11 May 2026 01:16:15 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 11 May 2026 01:16:15 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 11 May 2026 01:16:15 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 10 Minimal"
# Mon, 11 May 2026 01:16:15 GMT
LABEL io.openshift.expose-services=""
# Mon, 11 May 2026 01:16:15 GMT
LABEL io.openshift.tags="minimal rhel10"
# Mon, 11 May 2026 01:16:15 GMT
ENV container oci
# Mon, 11 May 2026 01:16:15 GMT
COPY dir:944b21b5e56ba1540a32a325c037508b8301ec37c6f3e20f96a07c3b3ab330c2 in /      
# Mon, 11 May 2026 01:16:16 GMT
COPY file:5de33b5fc08b00635bccf9134a18978dba13e2250aa51838f9969515a3957847 in /etc/yum.repos.d/.      
# Mon, 11 May 2026 01:16:16 GMT
CMD ["/bin/bash"]
# Mon, 11 May 2026 01:16:16 GMT
COPY file:595171150af68abc798ea385f7988d74b566aa8e84babff137f00b08b2164683 in /usr/share/buildinfo/content-sets.json      
# Mon, 11 May 2026 01:16:16 GMT
COPY file:595171150af68abc798ea385f7988d74b566aa8e84babff137f00b08b2164683 in /root/buildinfo/content_manifests/content-sets.json      
# Mon, 11 May 2026 01:16:16 GMT
COPY file:2c395ff24a52d293bfab5aa19a14f53b1efe7d5e8864bf90f387296119a55f72 in /usr/share/buildinfo/labels.json      
# Mon, 11 May 2026 01:16:16 GMT
COPY file:2c395ff24a52d293bfab5aa19a14f53b1efe7d5e8864bf90f387296119a55f72 in /root/buildinfo/labels.json      
# Mon, 11 May 2026 01:16:16 GMT
LABEL "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="356ecb8b806b04797740ef169abe27bf41ac3f8c" "org.opencontainers.image.revision"="356ecb8b806b04797740ef169abe27bf41ac3f8c" "build-date"="2026-05-11T01:16:01Z" "org.opencontainers.image.created"="2026-05-11T01:16:01Z" "release"="1778461919"org.opencontainers.image.revision=356ecb8b806b04797740ef169abe27bf41ac3f8c,org.opencontainers.image.created=2026-05-11T01:16:01Z
# Tue, 12 May 2026 00:06:41 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 12 May 2026 00:06:41 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 May 2026 00:06:41 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 12 May 2026 00:06:41 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en         gnupg2     ;     microdnf clean all # buildkit
# Tue, 12 May 2026 00:06:41 GMT
ENV JAVA_VERSION=jdk-26+35
# Tue, 12 May 2026 00:06:49 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='e8ff1f23c5acef74d1b4937dadd67286d67be06758f5d9dca5478c35bf404e83';          BINARY_URL='https://github.com/adoptium/temurin26-binaries/releases/download/jdk-26%2B35/OpenJDK26U-jdk_aarch64_linux_hotspot_26_35.tar.gz';          ;;        ppc64le)          ESUM='7396fc32c311429c4b1573ebfc98eca6b82c2735f9f0e23acbccdcb43e0edee9';          BINARY_URL='https://github.com/adoptium/temurin26-binaries/releases/download/jdk-26%2B35/OpenJDK26U-jdk_ppc64le_linux_hotspot_26_35.tar.gz';          ;;        s390x)          ESUM='87fcdbbfd0adfd458922d8f8019eda23755aba597e386de2397f84cdf1b58808';          BINARY_URL='https://github.com/adoptium/temurin26-binaries/releases/download/jdk-26%2B35/OpenJDK26U-jdk_s390x_linux_hotspot_26_35.tar.gz';          ;;        x86_64)          ESUM='68e19ba53b7f1f74635c13f809e5db36cebccf3ae9e752423dd92d2ad7d831ef';          BINARY_URL='https://github.com/adoptium/temurin26-binaries/releases/download/jdk-26%2B35/OpenJDK26U-jdk_x64_linux_hotspot_26_35.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Tue, 12 May 2026 00:06:50 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 12 May 2026 00:06:50 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 12 May 2026 00:06:50 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 12 May 2026 00:06:50 GMT
CMD ["jshell"]
# Tue, 12 May 2026 00:18:07 GMT
CMD ["gradle"]
# Tue, 12 May 2026 00:18:07 GMT
ENV GRADLE_HOME=/opt/gradle
# Tue, 12 May 2026 00:18:07 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 101 gradle     && useradd --system --gid gradle --uid 101 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Tue, 12 May 2026 00:18:07 GMT
VOLUME [/home/gradle/.gradle]
# Tue, 12 May 2026 00:18:07 GMT
WORKDIR /home/gradle
# Tue, 12 May 2026 00:18:10 GMT
RUN set -o errexit -o nounset     && microdnf install -y         make         curl         wget         tar                 findutils                 unzip         which                 git         git-lfs         subversion     && microdnf clean all         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which svn # buildkit
# Tue, 12 May 2026 00:18:10 GMT
ENV GRADLE_VERSION=9.5.0
# Tue, 12 May 2026 00:18:10 GMT
ARG GRADLE_DOWNLOAD_SHA256=553c78f50dafcd54d65b9a444649057857469edf836431389695608536d6b746
# Tue, 12 May 2026 00:18:12 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=553c78f50dafcd54d65b9a444649057857469edf836431389695608536d6b746
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Tue, 12 May 2026 00:18:12 GMT
USER gradle
# Tue, 12 May 2026 00:18:13 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=553c78f50dafcd54d65b9a444649057857469edf836431389695608536d6b746
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --stacktrace --debug --version # buildkit
# Tue, 12 May 2026 00:18:13 GMT
USER root
```

-	Layers:
	-	`sha256:288c81655277add7fa3f1d2c80956ecdc30e861ea53ff003f0eb7d1f488bf24b`  
		Last Modified: Mon, 11 May 2026 02:07:21 GMT  
		Size: 34.6 MB (34622430 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ea17d990d34dd314d0384926b2b829ac49951286972ddb7c6129b0db1f71b43`  
		Last Modified: Tue, 12 May 2026 00:07:10 GMT  
		Size: 37.5 MB (37498211 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3ab68289ffb3807929ee218bd9544fa077932972613ccfa3a7bcd739fe99fc2`  
		Last Modified: Tue, 12 May 2026 00:07:10 GMT  
		Size: 94.5 MB (94454019 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b54e49e7f4779fe58c34cfe258cb6f73de533d793bf2c2045214eb18d714cba1`  
		Last Modified: Tue, 12 May 2026 00:07:07 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25b4373ef3aa3d590a81b534707b8e9575757cfaa47d62b0f62d201d90ec82cb`  
		Last Modified: Tue, 12 May 2026 00:07:00 GMT  
		Size: 2.3 KB (2291 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61f00fcbd965720d9d3246ec4f948c67f33112bd687ddb66a0c54a283c8fb54e`  
		Last Modified: Tue, 12 May 2026 00:18:31 GMT  
		Size: 1.6 KB (1581 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dda65f16daa2344795c57052edeaeab67f94eb7164505a4c10d93162cad7bd3c`  
		Last Modified: Tue, 12 May 2026 00:18:33 GMT  
		Size: 38.8 MB (38836106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:555c4e360ddf71b15d2d12c124b5efb0fe077d07d05f503157886641a6719e3a`  
		Last Modified: Tue, 12 May 2026 00:18:35 GMT  
		Size: 140.2 MB (140235906 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34c0b24234dae62ae5bedf1aeb5854747688cb8b040ab13e2c2c76ac2c081ca4`  
		Last Modified: Tue, 12 May 2026 00:18:30 GMT  
		Size: 25.6 KB (25614 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:9-jdk26-ubi10` - unknown; unknown

```console
$ docker pull gradle@sha256:db647417d0dd7bda402c908b07ce997fb4ac3dffce16f73ddc685cceaff04e17
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 MB (7045814 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0712c5afc7c032b7e926faa5b12ddb24dc31262247f1b6f6fb52095f91e0651f`

```dockerfile
```

-	Layers:
	-	`sha256:6042913a8d8fedd6a08b6c7ad13c5254adf21bac274677d03fb85fd68173198d`  
		Last Modified: Tue, 12 May 2026 00:18:31 GMT  
		Size: 7.0 MB (7021405 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b554f2d06cb2adf1d88e7c56d350418a2c7f97a7e2ee626096aaa424ad509346`  
		Last Modified: Tue, 12 May 2026 00:18:30 GMT  
		Size: 24.4 KB (24409 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:9-jdk26-ubi10` - linux; arm64 variant v8

```console
$ docker pull gradle@sha256:8d84b1ceab4de2e804f8a51a9e66ce32894308e49cf592927869e302b8f49fe5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **342.2 MB (342178284 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e63584952e12484582ddf5de1fb057406e562908fb6cb3f5113f7e508cf2668`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["gradle"]`

```dockerfile
# Mon, 11 May 2026 01:17:49 GMT
LABEL maintainer="Red Hat, Inc."
# Mon, 11 May 2026 01:17:49 GMT
LABEL vendor="Red Hat, Inc."
# Mon, 11 May 2026 01:17:49 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Mon, 11 May 2026 01:17:49 GMT
LABEL com.redhat.component="ubi10-minimal-container"       name="ubi10/ubi-minimal"       version="10.1"       cpe="cpe:/o:redhat:enterprise_linux:10.1"       distribution-scope="public"
# Mon, 11 May 2026 01:17:49 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Mon, 11 May 2026 01:17:49 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 10."
# Mon, 11 May 2026 01:17:49 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 11 May 2026 01:17:49 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 11 May 2026 01:17:49 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 10 Minimal"
# Mon, 11 May 2026 01:17:49 GMT
LABEL io.openshift.expose-services=""
# Mon, 11 May 2026 01:17:49 GMT
LABEL io.openshift.tags="minimal rhel10"
# Mon, 11 May 2026 01:17:49 GMT
ENV container oci
# Mon, 11 May 2026 01:17:50 GMT
COPY dir:c6e5c961b244885bbae5433f1eb0e567eb7e34fa66cb14c7f643fbc5449440ea in /      
# Mon, 11 May 2026 01:17:50 GMT
COPY file:5de33b5fc08b00635bccf9134a18978dba13e2250aa51838f9969515a3957847 in /etc/yum.repos.d/.      
# Mon, 11 May 2026 01:17:50 GMT
CMD ["/bin/bash"]
# Mon, 11 May 2026 01:17:50 GMT
COPY file:595171150af68abc798ea385f7988d74b566aa8e84babff137f00b08b2164683 in /usr/share/buildinfo/content-sets.json      
# Mon, 11 May 2026 01:17:50 GMT
COPY file:595171150af68abc798ea385f7988d74b566aa8e84babff137f00b08b2164683 in /root/buildinfo/content_manifests/content-sets.json      
# Mon, 11 May 2026 01:17:50 GMT
COPY file:10669f015105b6d7eaedf2ab202dda1098c84203dd610f6bad742d23a54f4858 in /usr/share/buildinfo/labels.json      
# Mon, 11 May 2026 01:17:50 GMT
COPY file:10669f015105b6d7eaedf2ab202dda1098c84203dd610f6bad742d23a54f4858 in /root/buildinfo/labels.json      
# Mon, 11 May 2026 01:17:51 GMT
LABEL "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="356ecb8b806b04797740ef169abe27bf41ac3f8c" "org.opencontainers.image.revision"="356ecb8b806b04797740ef169abe27bf41ac3f8c" "build-date"="2026-05-11T01:17:34Z" "org.opencontainers.image.created"="2026-05-11T01:17:34Z" "release"="1778461919"org.opencontainers.image.revision=356ecb8b806b04797740ef169abe27bf41ac3f8c,org.opencontainers.image.created=2026-05-11T01:17:34Z
# Tue, 12 May 2026 00:00:30 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 12 May 2026 00:00:30 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 May 2026 00:00:30 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 12 May 2026 00:00:30 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en         gnupg2     ;     microdnf clean all # buildkit
# Tue, 12 May 2026 00:00:30 GMT
ENV JAVA_VERSION=jdk-26+35
# Tue, 12 May 2026 00:04:45 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='e8ff1f23c5acef74d1b4937dadd67286d67be06758f5d9dca5478c35bf404e83';          BINARY_URL='https://github.com/adoptium/temurin26-binaries/releases/download/jdk-26%2B35/OpenJDK26U-jdk_aarch64_linux_hotspot_26_35.tar.gz';          ;;        ppc64le)          ESUM='7396fc32c311429c4b1573ebfc98eca6b82c2735f9f0e23acbccdcb43e0edee9';          BINARY_URL='https://github.com/adoptium/temurin26-binaries/releases/download/jdk-26%2B35/OpenJDK26U-jdk_ppc64le_linux_hotspot_26_35.tar.gz';          ;;        s390x)          ESUM='87fcdbbfd0adfd458922d8f8019eda23755aba597e386de2397f84cdf1b58808';          BINARY_URL='https://github.com/adoptium/temurin26-binaries/releases/download/jdk-26%2B35/OpenJDK26U-jdk_s390x_linux_hotspot_26_35.tar.gz';          ;;        x86_64)          ESUM='68e19ba53b7f1f74635c13f809e5db36cebccf3ae9e752423dd92d2ad7d831ef';          BINARY_URL='https://github.com/adoptium/temurin26-binaries/releases/download/jdk-26%2B35/OpenJDK26U-jdk_x64_linux_hotspot_26_35.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Tue, 12 May 2026 00:04:47 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 12 May 2026 00:04:47 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 12 May 2026 00:04:47 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 12 May 2026 00:04:47 GMT
CMD ["jshell"]
# Tue, 12 May 2026 00:16:59 GMT
CMD ["gradle"]
# Tue, 12 May 2026 00:16:59 GMT
ENV GRADLE_HOME=/opt/gradle
# Tue, 12 May 2026 00:16:59 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 101 gradle     && useradd --system --gid gradle --uid 101 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Tue, 12 May 2026 00:16:59 GMT
VOLUME [/home/gradle/.gradle]
# Tue, 12 May 2026 00:17:00 GMT
WORKDIR /home/gradle
# Tue, 12 May 2026 00:17:03 GMT
RUN set -o errexit -o nounset     && microdnf install -y         make         curl         wget         tar                 findutils                 unzip         which                 git         git-lfs         subversion     && microdnf clean all         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which svn # buildkit
# Tue, 12 May 2026 00:17:03 GMT
ENV GRADLE_VERSION=9.5.0
# Tue, 12 May 2026 00:17:03 GMT
ARG GRADLE_DOWNLOAD_SHA256=553c78f50dafcd54d65b9a444649057857469edf836431389695608536d6b746
# Tue, 12 May 2026 00:17:05 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=553c78f50dafcd54d65b9a444649057857469edf836431389695608536d6b746
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Tue, 12 May 2026 00:17:05 GMT
USER gradle
# Tue, 12 May 2026 00:17:06 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=553c78f50dafcd54d65b9a444649057857469edf836431389695608536d6b746
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --stacktrace --debug --version # buildkit
# Tue, 12 May 2026 00:17:06 GMT
USER root
```

-	Layers:
	-	`sha256:b0d48ca6ae597735e3215ce3085802fb19010a7e5256d1d09af0257d955c5185`  
		Last Modified: Mon, 11 May 2026 02:10:59 GMT  
		Size: 32.7 MB (32747172 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86b2bbbc039e52cf7032fc21058b8f80378325cca9d0b828bf4b06b3851e034a`  
		Last Modified: Tue, 12 May 2026 00:00:50 GMT  
		Size: 37.4 MB (37444541 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d6bd6efded2a390fbff2d3a789325bc1f332d5990ed553e72a667717afb847d`  
		Last Modified: Tue, 12 May 2026 00:05:07 GMT  
		Size: 93.4 MB (93395891 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8973466aeedee93978a0ff508e441a3edc864233f84c6aa008256a2f13b0b4c6`  
		Last Modified: Tue, 12 May 2026 00:05:04 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c2f07fbe8cdc6d457b2cf907d2671a04090d5c20a56cb9b3706e14a5347d1c1`  
		Last Modified: Tue, 12 May 2026 00:05:05 GMT  
		Size: 2.3 KB (2290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd758e35a14eef7ce3279d518654d0360be5cb47f2fc3dc9288c329c5a6688a3`  
		Last Modified: Tue, 12 May 2026 00:17:24 GMT  
		Size: 1.6 KB (1583 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:852369304ce7193b598b1aa6d10e0331fc9232304285ca63945c48731f29b8bd`  
		Last Modified: Tue, 12 May 2026 00:17:26 GMT  
		Size: 38.3 MB (38321405 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d18f2533afda8a27a2992cfdb0c151bce6953e9df89b6f82f4d62a226b379ec0`  
		Last Modified: Tue, 12 May 2026 00:17:28 GMT  
		Size: 140.2 MB (140235903 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73afad58455fcb4195a85c325e98751a306b7515f8c18690083a6916837400b7`  
		Last Modified: Tue, 12 May 2026 00:17:23 GMT  
		Size: 29.3 KB (29338 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:9-jdk26-ubi10` - unknown; unknown

```console
$ docker pull gradle@sha256:976f9c4d2e6cb63ce89d32466942956dbe47b4f2a19f9c8562550c18236ca100
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 MB (7044263 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:edfd4383502fad03245dfb779f5e669c0aa06883836facc749953a2f1c95dd6c`

```dockerfile
```

-	Layers:
	-	`sha256:5607fecef09a57b147aa625ed29324d719a350e7e5519e489e9721c41481fd7d`  
		Last Modified: Tue, 12 May 2026 00:17:24 GMT  
		Size: 7.0 MB (7019658 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:287dfcc5c742f321475ac82a0d3c83e689be7f2e9f046c0ba10ca9254b6c7ac4`  
		Last Modified: Tue, 12 May 2026 00:17:24 GMT  
		Size: 24.6 KB (24605 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:9-jdk26-ubi10` - linux; ppc64le

```console
$ docker pull gradle@sha256:f000f184299bb3f4c1b0e5fc1548220274c58639e16caf3d4720acc3d9f642a6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **352.6 MB (352609039 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9d736f9a44d71ede8dc6145430cec36270b694dc61fcb30f3f3d449576fb215d`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["gradle"]`

```dockerfile
# Mon, 11 May 2026 01:17:29 GMT
LABEL maintainer="Red Hat, Inc."
# Mon, 11 May 2026 01:17:29 GMT
LABEL vendor="Red Hat, Inc."
# Mon, 11 May 2026 01:17:29 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Mon, 11 May 2026 01:17:29 GMT
LABEL com.redhat.component="ubi10-minimal-container"       name="ubi10/ubi-minimal"       version="10.1"       cpe="cpe:/o:redhat:enterprise_linux:10.1"       distribution-scope="public"
# Mon, 11 May 2026 01:17:29 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Mon, 11 May 2026 01:17:29 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 10."
# Mon, 11 May 2026 01:17:29 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 11 May 2026 01:17:29 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 11 May 2026 01:17:29 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 10 Minimal"
# Mon, 11 May 2026 01:17:29 GMT
LABEL io.openshift.expose-services=""
# Mon, 11 May 2026 01:17:29 GMT
LABEL io.openshift.tags="minimal rhel10"
# Mon, 11 May 2026 01:17:29 GMT
ENV container oci
# Mon, 11 May 2026 01:17:29 GMT
COPY dir:f86ae0d0c4a87090459f5dd2e52db1242d0bf9305bb73e66dc55f51f70971c00 in /      
# Mon, 11 May 2026 01:17:29 GMT
COPY file:5de33b5fc08b00635bccf9134a18978dba13e2250aa51838f9969515a3957847 in /etc/yum.repos.d/.      
# Mon, 11 May 2026 01:17:29 GMT
CMD ["/bin/bash"]
# Mon, 11 May 2026 01:17:29 GMT
COPY file:595171150af68abc798ea385f7988d74b566aa8e84babff137f00b08b2164683 in /usr/share/buildinfo/content-sets.json      
# Mon, 11 May 2026 01:17:30 GMT
COPY file:595171150af68abc798ea385f7988d74b566aa8e84babff137f00b08b2164683 in /root/buildinfo/content_manifests/content-sets.json      
# Mon, 11 May 2026 01:17:30 GMT
COPY file:3937609775d6da2876c2843dd2634469abf69886b03de03bc99d3e8daa564f9c in /usr/share/buildinfo/labels.json      
# Mon, 11 May 2026 01:17:30 GMT
COPY file:3937609775d6da2876c2843dd2634469abf69886b03de03bc99d3e8daa564f9c in /root/buildinfo/labels.json      
# Mon, 11 May 2026 01:17:30 GMT
LABEL "architecture"="ppc64le" "vcs-type"="git" "vcs-ref"="356ecb8b806b04797740ef169abe27bf41ac3f8c" "org.opencontainers.image.revision"="356ecb8b806b04797740ef169abe27bf41ac3f8c" "build-date"="2026-05-11T01:17:17Z" "org.opencontainers.image.created"="2026-05-11T01:17:17Z" "release"="1778461919"org.opencontainers.image.revision=356ecb8b806b04797740ef169abe27bf41ac3f8c,org.opencontainers.image.created=2026-05-11T01:17:17Z
# Tue, 12 May 2026 00:28:47 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 12 May 2026 00:28:47 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 May 2026 00:28:47 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 12 May 2026 00:28:47 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en         gnupg2     ;     microdnf clean all # buildkit
# Tue, 12 May 2026 00:28:47 GMT
ENV JAVA_VERSION=jdk-26+35
# Tue, 12 May 2026 00:37:38 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='e8ff1f23c5acef74d1b4937dadd67286d67be06758f5d9dca5478c35bf404e83';          BINARY_URL='https://github.com/adoptium/temurin26-binaries/releases/download/jdk-26%2B35/OpenJDK26U-jdk_aarch64_linux_hotspot_26_35.tar.gz';          ;;        ppc64le)          ESUM='7396fc32c311429c4b1573ebfc98eca6b82c2735f9f0e23acbccdcb43e0edee9';          BINARY_URL='https://github.com/adoptium/temurin26-binaries/releases/download/jdk-26%2B35/OpenJDK26U-jdk_ppc64le_linux_hotspot_26_35.tar.gz';          ;;        s390x)          ESUM='87fcdbbfd0adfd458922d8f8019eda23755aba597e386de2397f84cdf1b58808';          BINARY_URL='https://github.com/adoptium/temurin26-binaries/releases/download/jdk-26%2B35/OpenJDK26U-jdk_s390x_linux_hotspot_26_35.tar.gz';          ;;        x86_64)          ESUM='68e19ba53b7f1f74635c13f809e5db36cebccf3ae9e752423dd92d2ad7d831ef';          BINARY_URL='https://github.com/adoptium/temurin26-binaries/releases/download/jdk-26%2B35/OpenJDK26U-jdk_x64_linux_hotspot_26_35.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Tue, 12 May 2026 00:37:45 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 12 May 2026 00:37:46 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 12 May 2026 00:37:46 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 12 May 2026 00:37:46 GMT
CMD ["jshell"]
# Tue, 12 May 2026 01:14:20 GMT
CMD ["gradle"]
# Tue, 12 May 2026 01:14:20 GMT
ENV GRADLE_HOME=/opt/gradle
# Tue, 12 May 2026 01:14:20 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 101 gradle     && useradd --system --gid gradle --uid 101 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Tue, 12 May 2026 01:14:20 GMT
VOLUME [/home/gradle/.gradle]
# Tue, 12 May 2026 01:14:20 GMT
WORKDIR /home/gradle
# Tue, 12 May 2026 01:14:40 GMT
RUN set -o errexit -o nounset     && microdnf install -y         make         curl         wget         tar                 findutils                 unzip         which                 git         git-lfs         subversion     && microdnf clean all         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which svn # buildkit
# Tue, 12 May 2026 01:14:40 GMT
ENV GRADLE_VERSION=9.5.0
# Tue, 12 May 2026 01:14:40 GMT
ARG GRADLE_DOWNLOAD_SHA256=553c78f50dafcd54d65b9a444649057857469edf836431389695608536d6b746
# Tue, 12 May 2026 01:14:45 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=553c78f50dafcd54d65b9a444649057857469edf836431389695608536d6b746
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Tue, 12 May 2026 01:14:45 GMT
USER gradle
# Tue, 12 May 2026 01:14:46 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=553c78f50dafcd54d65b9a444649057857469edf836431389695608536d6b746
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --stacktrace --debug --version # buildkit
# Tue, 12 May 2026 01:14:46 GMT
USER root
```

-	Layers:
	-	`sha256:dfc37eccb37a052e4fa7be870ee6db7544ef15834a2dfa05156adc7b3f0064f8`  
		Last Modified: Mon, 11 May 2026 06:17:19 GMT  
		Size: 38.8 MB (38752382 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5b57514fb022bd5104b331922465798e8b81622c1daf6f728be81eb5ba7748c`  
		Last Modified: Tue, 12 May 2026 00:29:32 GMT  
		Size: 39.3 MB (39255864 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89d363228c855ba779b90883eb815f0f669aebfc8ebd979a50a7af26b9fbe786`  
		Last Modified: Tue, 12 May 2026 00:38:20 GMT  
		Size: 93.8 MB (93782993 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3cbc37d163e6db523230b12a3f4b2f65179cda3a7ddfb4c3566558c207e3a6c`  
		Last Modified: Tue, 12 May 2026 00:38:17 GMT  
		Size: 130.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:372b9f4df7b9ee6e8660ecec2429ed01019274a7fa0941281f81b86d000ec334`  
		Last Modified: Tue, 12 May 2026 00:38:17 GMT  
		Size: 2.3 KB (2291 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:698c09462182e287cd1e4dc75d30ef403677ec73d30e831af31ce1379cef01f6`  
		Last Modified: Tue, 12 May 2026 01:15:25 GMT  
		Size: 1.6 KB (1580 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de4162a356c3a9154ca58749025fe6e8f7cb483c49cf9add38321c1a09d1f779`  
		Last Modified: Tue, 12 May 2026 01:15:27 GMT  
		Size: 40.6 MB (40577487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:731906cd8c7ba4f3b113eae7a1d368b6a8bfc461f7dbca67c06ef904a94f0307`  
		Last Modified: Tue, 12 May 2026 01:15:29 GMT  
		Size: 140.2 MB (140235903 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b7412e8f4ca5dea667723ab34498c460f838a9500bf0eef8ddf88de429a1caf`  
		Last Modified: Tue, 12 May 2026 01:15:25 GMT  
		Size: 377.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:9-jdk26-ubi10` - unknown; unknown

```console
$ docker pull gradle@sha256:7ea267af1bbc8203472a117d610fc917ea8740d9e86ad493b98feb35714fb72d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 MB (7021240 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9da16716cf50ea56178398bdf9fba0007bbbdd88c08b9669d24a74b6a0786cc0`

```dockerfile
```

-	Layers:
	-	`sha256:a8d7172f1b1d0e4696912653fd17488d9169a8ff423b9e14315162d5fbe2bc32`  
		Last Modified: Tue, 12 May 2026 01:15:25 GMT  
		Size: 7.0 MB (6996759 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0303a486f38c83baf6814d1c9a8684bd586c6e61721b67ff2dde70843eca5464`  
		Last Modified: Tue, 12 May 2026 01:15:25 GMT  
		Size: 24.5 KB (24481 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:9-jdk26-ubi10` - linux; s390x

```console
$ docker pull gradle@sha256:c4630ed04b079ea56df1a2a265a3c501aa1d0baef2d45ad9d61f57e05c834ba6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **344.0 MB (344044512 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9cabe1a8a7b8829e979c09d337cbbd19f5075e10177be81756e7e1c9902f8a2c`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["gradle"]`

```dockerfile
# Mon, 11 May 2026 01:23:16 GMT
LABEL maintainer="Red Hat, Inc."
# Mon, 11 May 2026 01:23:16 GMT
LABEL vendor="Red Hat, Inc."
# Mon, 11 May 2026 01:23:16 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Mon, 11 May 2026 01:23:16 GMT
LABEL com.redhat.component="ubi10-minimal-container"       name="ubi10/ubi-minimal"       version="10.1"       cpe="cpe:/o:redhat:enterprise_linux:10.1"       distribution-scope="public"
# Mon, 11 May 2026 01:23:16 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Mon, 11 May 2026 01:23:16 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 10."
# Mon, 11 May 2026 01:23:16 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 11 May 2026 01:23:16 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 11 May 2026 01:23:16 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 10 Minimal"
# Mon, 11 May 2026 01:23:16 GMT
LABEL io.openshift.expose-services=""
# Mon, 11 May 2026 01:23:16 GMT
LABEL io.openshift.tags="minimal rhel10"
# Mon, 11 May 2026 01:23:16 GMT
ENV container oci
# Mon, 11 May 2026 01:23:17 GMT
COPY dir:0579bc85c05b217dd77b2ce225f64d3cb10f81a6a3726b91387ffbc978d6e453 in /      
# Mon, 11 May 2026 01:23:17 GMT
COPY file:5de33b5fc08b00635bccf9134a18978dba13e2250aa51838f9969515a3957847 in /etc/yum.repos.d/.      
# Mon, 11 May 2026 01:23:17 GMT
CMD ["/bin/bash"]
# Mon, 11 May 2026 01:23:17 GMT
COPY file:595171150af68abc798ea385f7988d74b566aa8e84babff137f00b08b2164683 in /usr/share/buildinfo/content-sets.json      
# Mon, 11 May 2026 01:23:17 GMT
COPY file:595171150af68abc798ea385f7988d74b566aa8e84babff137f00b08b2164683 in /root/buildinfo/content_manifests/content-sets.json      
# Mon, 11 May 2026 01:23:17 GMT
COPY file:81f827a1784652793e747198fea65ce1ad402e9b3c1587adce62db262e60fb88 in /usr/share/buildinfo/labels.json      
# Mon, 11 May 2026 01:23:17 GMT
COPY file:81f827a1784652793e747198fea65ce1ad402e9b3c1587adce62db262e60fb88 in /root/buildinfo/labels.json      
# Mon, 11 May 2026 01:23:17 GMT
LABEL "architecture"="s390x" "vcs-type"="git" "vcs-ref"="356ecb8b806b04797740ef169abe27bf41ac3f8c" "org.opencontainers.image.revision"="356ecb8b806b04797740ef169abe27bf41ac3f8c" "build-date"="2026-05-11T01:22:36Z" "org.opencontainers.image.created"="2026-05-11T01:22:36Z" "release"="1778461919"org.opencontainers.image.revision=356ecb8b806b04797740ef169abe27bf41ac3f8c,org.opencontainers.image.created=2026-05-11T01:22:36Z
# Tue, 12 May 2026 00:00:32 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 12 May 2026 00:00:32 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 May 2026 00:00:32 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 12 May 2026 00:00:32 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en         gnupg2     ;     microdnf clean all # buildkit
# Tue, 12 May 2026 00:00:32 GMT
ENV JAVA_VERSION=jdk-26+35
# Tue, 12 May 2026 00:03:17 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='e8ff1f23c5acef74d1b4937dadd67286d67be06758f5d9dca5478c35bf404e83';          BINARY_URL='https://github.com/adoptium/temurin26-binaries/releases/download/jdk-26%2B35/OpenJDK26U-jdk_aarch64_linux_hotspot_26_35.tar.gz';          ;;        ppc64le)          ESUM='7396fc32c311429c4b1573ebfc98eca6b82c2735f9f0e23acbccdcb43e0edee9';          BINARY_URL='https://github.com/adoptium/temurin26-binaries/releases/download/jdk-26%2B35/OpenJDK26U-jdk_ppc64le_linux_hotspot_26_35.tar.gz';          ;;        s390x)          ESUM='87fcdbbfd0adfd458922d8f8019eda23755aba597e386de2397f84cdf1b58808';          BINARY_URL='https://github.com/adoptium/temurin26-binaries/releases/download/jdk-26%2B35/OpenJDK26U-jdk_s390x_linux_hotspot_26_35.tar.gz';          ;;        x86_64)          ESUM='68e19ba53b7f1f74635c13f809e5db36cebccf3ae9e752423dd92d2ad7d831ef';          BINARY_URL='https://github.com/adoptium/temurin26-binaries/releases/download/jdk-26%2B35/OpenJDK26U-jdk_x64_linux_hotspot_26_35.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Tue, 12 May 2026 00:03:18 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 12 May 2026 00:03:18 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 12 May 2026 00:03:18 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 12 May 2026 00:03:18 GMT
CMD ["jshell"]
# Tue, 12 May 2026 00:13:44 GMT
CMD ["gradle"]
# Tue, 12 May 2026 00:13:44 GMT
ENV GRADLE_HOME=/opt/gradle
# Tue, 12 May 2026 00:13:44 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 101 gradle     && useradd --system --gid gradle --uid 101 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Tue, 12 May 2026 00:13:44 GMT
VOLUME [/home/gradle/.gradle]
# Tue, 12 May 2026 00:13:44 GMT
WORKDIR /home/gradle
# Tue, 12 May 2026 00:13:49 GMT
RUN set -o errexit -o nounset     && microdnf install -y         make         curl         wget         tar                 findutils                 unzip         which                 git         git-lfs         subversion     && microdnf clean all         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which svn # buildkit
# Tue, 12 May 2026 00:13:49 GMT
ENV GRADLE_VERSION=9.5.0
# Tue, 12 May 2026 00:13:49 GMT
ARG GRADLE_DOWNLOAD_SHA256=553c78f50dafcd54d65b9a444649057857469edf836431389695608536d6b746
# Tue, 12 May 2026 00:13:54 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=553c78f50dafcd54d65b9a444649057857469edf836431389695608536d6b746
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Tue, 12 May 2026 00:13:54 GMT
USER gradle
# Tue, 12 May 2026 00:13:55 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=553c78f50dafcd54d65b9a444649057857469edf836431389695608536d6b746
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --stacktrace --debug --version # buildkit
# Tue, 12 May 2026 00:13:55 GMT
USER root
```

-	Layers:
	-	`sha256:c8191d3132a8f64ba77e2e7e35ea28fba961048b0be562036986e4b4138e5000`  
		Last Modified: Mon, 11 May 2026 06:17:00 GMT  
		Size: 34.4 MB (34447893 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48e45d6f5b7b2ae6b57d4c8f61a19d4016477e8b833954767b9f45a07aaccf21`  
		Last Modified: Tue, 12 May 2026 00:00:54 GMT  
		Size: 37.9 MB (37883315 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:935a549460bf05e5fd09abbe56d4de3d4cf5c44856e9422759e244aaa4fbaf08`  
		Last Modified: Tue, 12 May 2026 00:03:43 GMT  
		Size: 90.5 MB (90548267 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:405ac60957b8741ddf8c7b9a9aef83dc5b480389dc8e9d3aae885d08feba3234`  
		Last Modified: Tue, 12 May 2026 00:03:41 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a14c8a3284bda8379b8814dbe9e09bcd07eaa7d66843915f6cab9418faff06f`  
		Last Modified: Tue, 12 May 2026 00:03:41 GMT  
		Size: 2.3 KB (2287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91b23eb9773e62d1e43456461c87b6e5300bed91ed1dbe825dfa6d8e2d205a07`  
		Last Modified: Tue, 12 May 2026 00:14:21 GMT  
		Size: 1.6 KB (1585 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a2a5a434aeaaf19d3785384dc6a1844af65d53e8f36e7926fe7ee3b16acf8e5`  
		Last Modified: Tue, 12 May 2026 00:14:24 GMT  
		Size: 40.9 MB (40924721 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbad5051907253c09d124e70445a30dbf266f3794f3624a5cf576566ab1fdac0`  
		Last Modified: Tue, 12 May 2026 00:14:26 GMT  
		Size: 140.2 MB (140235907 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0bbf4ff1d08639519951db8a8d6bf047956e646581cc57bc9f062ba83882b9e9`  
		Last Modified: Tue, 12 May 2026 00:14:22 GMT  
		Size: 377.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:9-jdk26-ubi10` - unknown; unknown

```console
$ docker pull gradle@sha256:2bd22cd59e3eebfa0cd5c253774576423338f5257b73ff6e6535629152228724
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 MB (7011645 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:23c1340b62d738e03c13aaec8873e49a443d0215438890a79301a5580ed80332`

```dockerfile
```

-	Layers:
	-	`sha256:d44cd4e5d94acd7daf94c7b61793aa9ed62ba9c554c5d7570f69a15df2dcdc30`  
		Last Modified: Tue, 12 May 2026 00:14:22 GMT  
		Size: 7.0 MB (6987238 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:604df685eeb9bda0fcb490812ffa043bf2f69a23aa1c8995c61d7cc61d3e367b`  
		Last Modified: Tue, 12 May 2026 00:14:21 GMT  
		Size: 24.4 KB (24407 bytes)  
		MIME: application/vnd.in-toto+json
