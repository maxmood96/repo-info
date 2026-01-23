## `gradle:jdk21-ubi10`

```console
$ docker pull gradle@sha256:1d666c6ee62faae3b7374bc14c89c6dd796763fb9bda590c37b10f197f73de72
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

### `gradle:jdk21-ubi10` - linux; amd64

```console
$ docker pull gradle@sha256:ec08d1789763e532913a84697d776f16eb37f879d88a6e658e47df4391ba1848
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **405.4 MB (405404643 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:093df1819f7e3b19d262dc1fa2831fcde56c21e1bf6c92bd53b6084cd820d676`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["gradle"]`

```dockerfile
# Thu, 22 Jan 2026 14:19:49 GMT
LABEL maintainer="Red Hat, Inc."
# Thu, 22 Jan 2026 14:19:49 GMT
LABEL vendor="Red Hat, Inc."
# Thu, 22 Jan 2026 14:19:49 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Thu, 22 Jan 2026 14:19:49 GMT
LABEL com.redhat.component="ubi10-minimal-container"       name="ubi10/ubi-minimal"       version="10.1"       cpe="cpe:/o:redhat:enterprise_linux:10.1"       distribution-scope="public"
# Thu, 22 Jan 2026 14:19:49 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Thu, 22 Jan 2026 14:19:49 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 10."
# Thu, 22 Jan 2026 14:19:49 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 22 Jan 2026 14:19:49 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 22 Jan 2026 14:19:49 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 10 Minimal"
# Thu, 22 Jan 2026 14:19:49 GMT
LABEL io.openshift.expose-services=""
# Thu, 22 Jan 2026 14:19:49 GMT
LABEL io.openshift.tags="minimal rhel10"
# Thu, 22 Jan 2026 14:19:49 GMT
ENV container oci
# Thu, 22 Jan 2026 14:19:50 GMT
COPY dir:4f39f7f54b1623f2373491e5bcb10b3c35efaa04126f246c1c0ae784bb3d7f42 in /      
# Thu, 22 Jan 2026 14:19:50 GMT
COPY file:5de33b5fc08b00635bccf9134a18978dba13e2250aa51838f9969515a3957847 in /etc/yum.repos.d/.      
# Thu, 22 Jan 2026 14:19:50 GMT
CMD ["/bin/bash"]
# Thu, 22 Jan 2026 14:19:50 GMT
COPY file:595171150af68abc798ea385f7988d74b566aa8e84babff137f00b08b2164683 in /usr/share/buildinfo/content-sets.json      
# Thu, 22 Jan 2026 14:19:50 GMT
COPY file:595171150af68abc798ea385f7988d74b566aa8e84babff137f00b08b2164683 in /root/buildinfo/content_manifests/content-sets.json      
# Thu, 22 Jan 2026 14:19:50 GMT
COPY file:e86693423cdd34ed7ac6eb4c5f916f086a37eeca572019e4cfd639c87f98a6ae in /usr/share/buildinfo/labels.json      
# Thu, 22 Jan 2026 14:19:50 GMT
COPY file:e86693423cdd34ed7ac6eb4c5f916f086a37eeca572019e4cfd639c87f98a6ae in /root/buildinfo/labels.json      
# Thu, 22 Jan 2026 14:19:51 GMT
LABEL "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="0912ab420a80f21132d8a5e29d19a23339176677" "org.opencontainers.image.revision"="0912ab420a80f21132d8a5e29d19a23339176677" "build-date"="2026-01-22T14:19:22Z" "org.opencontainers.image.created"="2026-01-22T14:19:22Z" "release"="1769090502"org.opencontainers.image.revision=0912ab420a80f21132d8a5e29d19a23339176677,org.opencontainers.image.created=2026-01-22T14:19:22Z
# Fri, 23 Jan 2026 00:59:59 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 23 Jan 2026 00:59:59 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 23 Jan 2026 00:59:59 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 23 Jan 2026 00:59:59 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en         gnupg2     ;     microdnf clean all # buildkit
# Fri, 23 Jan 2026 00:59:59 GMT
ENV JAVA_VERSION=jdk-21.0.9+10
# Fri, 23 Jan 2026 01:01:27 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='edf0da4debe7cf475dbe320d174d6eed81479eb363f41e38a2efb740428c603a';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.9%2B10/OpenJDK21U-jdk_aarch64_linux_hotspot_21.0.9_10.tar.gz';          ;;        ppc64le)          ESUM='ac5a0394a234269b4e20459649ac93cb702cde29b3e46a0bcf3aa53958f2d4a4';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.9%2B10/OpenJDK21U-jdk_ppc64le_linux_hotspot_21.0.9_10.tar.gz';          ;;        s390x)          ESUM='e8ede0fb48aaa3a0cc1ac7c8522f8ca7938bdbb8be0d603b61134de7f898aff4';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.9%2B10/OpenJDK21U-jdk_s390x_linux_hotspot_21.0.9_10.tar.gz';          ;;        x86_64)          ESUM='810d3773df7e0d6c4394e4e244b264c8b30e0b05a0acf542d065fd78a6b65c2f';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.9%2B10/OpenJDK21U-jdk_x64_linux_hotspot_21.0.9_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Fri, 23 Jan 2026 01:01:28 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Fri, 23 Jan 2026 01:01:28 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Fri, 23 Jan 2026 01:01:28 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Fri, 23 Jan 2026 01:01:28 GMT
CMD ["jshell"]
# Fri, 23 Jan 2026 01:08:28 GMT
CMD ["gradle"]
# Fri, 23 Jan 2026 01:08:28 GMT
ENV GRADLE_HOME=/opt/gradle
# Fri, 23 Jan 2026 01:08:28 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 101 gradle     && useradd --system --gid gradle --uid 101 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Fri, 23 Jan 2026 01:08:28 GMT
VOLUME [/home/gradle/.gradle]
# Fri, 23 Jan 2026 01:08:28 GMT
WORKDIR /home/gradle
# Fri, 23 Jan 2026 01:08:33 GMT
RUN set -o errexit -o nounset     && microdnf install -y         make         curl-minimal         wget         tar                 findutils                 unzip         which                 git         git-lfs         subversion     && microdnf clean all         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which svn # buildkit
# Fri, 23 Jan 2026 01:08:33 GMT
ENV GRADLE_VERSION=9.3.0
# Fri, 23 Jan 2026 01:08:33 GMT
ARG GRADLE_DOWNLOAD_SHA256=0d585f69da091fc5b2beced877feab55a3064d43b8a1d46aeb07996b0915e0e0
# Fri, 23 Jan 2026 01:08:36 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=0d585f69da091fc5b2beced877feab55a3064d43b8a1d46aeb07996b0915e0e0
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Fri, 23 Jan 2026 01:08:36 GMT
USER gradle
# Fri, 23 Jan 2026 01:08:36 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=0d585f69da091fc5b2beced877feab55a3064d43b8a1d46aeb07996b0915e0e0
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --stacktrace --debug --version # buildkit
# Fri, 23 Jan 2026 01:08:36 GMT
USER root
```

-	Layers:
	-	`sha256:0d4f698c23e56c30d1371a123d48250f3a8dd3de24cc53c15e862c4210c331c2`  
		Last Modified: Thu, 22 Jan 2026 16:13:48 GMT  
		Size: 34.5 MB (34531934 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e058e1cc867cf3feee7d101285b4bc634490d6809fa9fb43631dc7ab3dc368f`  
		Last Modified: Fri, 23 Jan 2026 01:00:16 GMT  
		Size: 37.4 MB (37368491 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e4a9ca4c34bba766e91e844b6560cd8ab4e5fe116feb2397aa30ca18e09b721`  
		Last Modified: Fri, 23 Jan 2026 01:01:47 GMT  
		Size: 157.8 MB (157828948 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d586f34d22082401aab761d5642b646c7ece43f0ed501e588f55c2808c19fd0`  
		Last Modified: Fri, 23 Jan 2026 01:01:43 GMT  
		Size: 130.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fb1fa558bc39a2f90e126aac69cba38f99fb71159206239421322c8a4ca3cbc`  
		Last Modified: Fri, 23 Jan 2026 01:01:43 GMT  
		Size: 2.3 KB (2291 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:299aed22454902742a7608c89b8fd59d2c34f62f7cb55196765146433b71eed8`  
		Last Modified: Fri, 23 Jan 2026 01:08:56 GMT  
		Size: 1.6 KB (1585 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd4ff60322c5ca786610e2d815432f3155322085ca8370cafb13420e53a7d62e`  
		Last Modified: Fri, 23 Jan 2026 01:08:58 GMT  
		Size: 38.7 MB (38656769 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:409424973811832d06c612d2d12f6581f3b6b410ea20cfb6e53cc43bd1b13acc`  
		Last Modified: Fri, 23 Jan 2026 01:09:01 GMT  
		Size: 137.0 MB (136988872 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac24c71f627751aa832876c0402b7c6e85f782c671ba9d84bf09c3b241d46e84`  
		Last Modified: Fri, 23 Jan 2026 01:08:56 GMT  
		Size: 25.6 KB (25591 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:jdk21-ubi10` - unknown; unknown

```console
$ docker pull gradle@sha256:9492140d63dcda3ff8d7cb35bd3fb568a44db53ea532352dc216e2724803ff53
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.1 MB (7050602 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:202158b641a20882a16240392848496e097a6bb4f052c980fa29ddfa5fbd43fb`

```dockerfile
```

-	Layers:
	-	`sha256:5006d1e2a3add0ea1d6265d04bdaace0623c9ab36b9982c7ab264a9c8899aa87`  
		Last Modified: Fri, 23 Jan 2026 01:08:56 GMT  
		Size: 7.0 MB (7026151 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e5028430cc718a34c640aefa16e6d0fd889ada684af65f70ccaa6ef9f296de74`  
		Last Modified: Fri, 23 Jan 2026 01:08:56 GMT  
		Size: 24.5 KB (24451 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:jdk21-ubi10` - linux; arm64 variant v8

```console
$ docker pull gradle@sha256:8cefba1feb2adaa96de0aae9db12d26657a89584293f6491656491231b413dad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **401.2 MB (401212145 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c81de2d738c2856b1bb53d55be628e85c33cdc5ce4901e2e1bec29232792ab7`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["gradle"]`

```dockerfile
# Thu, 22 Jan 2026 14:10:51 GMT
LABEL maintainer="Red Hat, Inc."
# Thu, 22 Jan 2026 14:10:51 GMT
LABEL vendor="Red Hat, Inc."
# Thu, 22 Jan 2026 14:10:51 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Thu, 22 Jan 2026 14:10:51 GMT
LABEL com.redhat.component="ubi10-minimal-container"       name="ubi10/ubi-minimal"       version="10.1"       cpe="cpe:/o:redhat:enterprise_linux:10.1"       distribution-scope="public"
# Thu, 22 Jan 2026 14:10:51 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Thu, 22 Jan 2026 14:10:51 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 10."
# Thu, 22 Jan 2026 14:10:51 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 22 Jan 2026 14:10:51 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 22 Jan 2026 14:10:51 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 10 Minimal"
# Thu, 22 Jan 2026 14:10:51 GMT
LABEL io.openshift.expose-services=""
# Thu, 22 Jan 2026 14:10:51 GMT
LABEL io.openshift.tags="minimal rhel10"
# Thu, 22 Jan 2026 14:10:51 GMT
ENV container oci
# Thu, 22 Jan 2026 14:10:52 GMT
COPY dir:909d569786ad4226e9c77ee4fc4d27953d579517f60f8a0f25e4d85964a100a3 in /      
# Thu, 22 Jan 2026 14:10:52 GMT
COPY file:5de33b5fc08b00635bccf9134a18978dba13e2250aa51838f9969515a3957847 in /etc/yum.repos.d/.      
# Thu, 22 Jan 2026 14:10:52 GMT
CMD ["/bin/bash"]
# Thu, 22 Jan 2026 14:10:52 GMT
COPY file:595171150af68abc798ea385f7988d74b566aa8e84babff137f00b08b2164683 in /usr/share/buildinfo/content-sets.json      
# Thu, 22 Jan 2026 14:10:52 GMT
COPY file:595171150af68abc798ea385f7988d74b566aa8e84babff137f00b08b2164683 in /root/buildinfo/content_manifests/content-sets.json      
# Thu, 22 Jan 2026 14:10:52 GMT
COPY file:ea81599b2ebb991911687a996e9dca425fe171d768273735cf8dd2c299ff0d3d in /usr/share/buildinfo/labels.json      
# Thu, 22 Jan 2026 14:10:52 GMT
COPY file:ea81599b2ebb991911687a996e9dca425fe171d768273735cf8dd2c299ff0d3d in /root/buildinfo/labels.json      
# Thu, 22 Jan 2026 14:10:52 GMT
LABEL "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="0912ab420a80f21132d8a5e29d19a23339176677" "org.opencontainers.image.revision"="0912ab420a80f21132d8a5e29d19a23339176677" "build-date"="2026-01-22T14:10:29Z" "org.opencontainers.image.created"="2026-01-22T14:10:29Z" "release"="1769090502"org.opencontainers.image.revision=0912ab420a80f21132d8a5e29d19a23339176677,org.opencontainers.image.created=2026-01-22T14:10:29Z
# Fri, 23 Jan 2026 00:58:23 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 23 Jan 2026 00:58:23 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 23 Jan 2026 00:58:23 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 23 Jan 2026 00:58:23 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en         gnupg2     ;     microdnf clean all # buildkit
# Fri, 23 Jan 2026 00:58:23 GMT
ENV JAVA_VERSION=jdk-21.0.9+10
# Fri, 23 Jan 2026 00:59:58 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='edf0da4debe7cf475dbe320d174d6eed81479eb363f41e38a2efb740428c603a';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.9%2B10/OpenJDK21U-jdk_aarch64_linux_hotspot_21.0.9_10.tar.gz';          ;;        ppc64le)          ESUM='ac5a0394a234269b4e20459649ac93cb702cde29b3e46a0bcf3aa53958f2d4a4';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.9%2B10/OpenJDK21U-jdk_ppc64le_linux_hotspot_21.0.9_10.tar.gz';          ;;        s390x)          ESUM='e8ede0fb48aaa3a0cc1ac7c8522f8ca7938bdbb8be0d603b61134de7f898aff4';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.9%2B10/OpenJDK21U-jdk_s390x_linux_hotspot_21.0.9_10.tar.gz';          ;;        x86_64)          ESUM='810d3773df7e0d6c4394e4e244b264c8b30e0b05a0acf542d065fd78a6b65c2f';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.9%2B10/OpenJDK21U-jdk_x64_linux_hotspot_21.0.9_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Fri, 23 Jan 2026 00:59:59 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Fri, 23 Jan 2026 00:59:59 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Fri, 23 Jan 2026 00:59:59 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Fri, 23 Jan 2026 00:59:59 GMT
CMD ["jshell"]
# Fri, 23 Jan 2026 01:02:16 GMT
CMD ["gradle"]
# Fri, 23 Jan 2026 01:02:16 GMT
ENV GRADLE_HOME=/opt/gradle
# Fri, 23 Jan 2026 01:02:16 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 101 gradle     && useradd --system --gid gradle --uid 101 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Fri, 23 Jan 2026 01:02:16 GMT
VOLUME [/home/gradle/.gradle]
# Fri, 23 Jan 2026 01:02:16 GMT
WORKDIR /home/gradle
# Fri, 23 Jan 2026 01:02:22 GMT
RUN set -o errexit -o nounset     && microdnf install -y         make         curl-minimal         wget         tar                 findutils                 unzip         which                 git         git-lfs         subversion     && microdnf clean all         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which svn # buildkit
# Fri, 23 Jan 2026 01:02:22 GMT
ENV GRADLE_VERSION=9.3.0
# Fri, 23 Jan 2026 01:02:22 GMT
ARG GRADLE_DOWNLOAD_SHA256=0d585f69da091fc5b2beced877feab55a3064d43b8a1d46aeb07996b0915e0e0
# Fri, 23 Jan 2026 01:02:25 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=0d585f69da091fc5b2beced877feab55a3064d43b8a1d46aeb07996b0915e0e0
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Fri, 23 Jan 2026 01:02:25 GMT
USER gradle
# Fri, 23 Jan 2026 01:02:25 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=0d585f69da091fc5b2beced877feab55a3064d43b8a1d46aeb07996b0915e0e0
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --stacktrace --debug --version # buildkit
# Fri, 23 Jan 2026 01:02:25 GMT
USER root
```

-	Layers:
	-	`sha256:855d6cc175ead513a1945d3f0933680ee64146fa0bb48e8f15fcefa1fe9b0b14`  
		Last Modified: Thu, 22 Jan 2026 17:36:15 GMT  
		Size: 32.6 MB (32613686 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ac781c132d75e81cb50967739184f7c1157b403228369c655282bb8643ac784`  
		Last Modified: Fri, 23 Jan 2026 00:58:43 GMT  
		Size: 37.3 MB (37315606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f5d12680e8b469f3662469f40b0c3662be7647d2953d01057c09438f3d76976`  
		Last Modified: Fri, 23 Jan 2026 01:00:21 GMT  
		Size: 156.1 MB (156111818 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b542af2243f62cfcbaf1b6764fbeb37d494198f84aa2f9562832fa83b47bfbd9`  
		Last Modified: Fri, 23 Jan 2026 01:00:18 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30197c01feaebc15bd09c1c58df8176313c3367aa0fcb6865061faa915f160d7`  
		Last Modified: Fri, 23 Jan 2026 01:00:19 GMT  
		Size: 2.3 KB (2291 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6c3697dc42adca12967cdc30648c9a515936e3b26621c1f211ecdd1b8b09e15`  
		Last Modified: Fri, 23 Jan 2026 01:02:45 GMT  
		Size: 1.6 KB (1585 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:481fdae1bc64f1d994e90e6ea294ec9c1147509f614da0dec7c7fd5f8c4a6bb4`  
		Last Modified: Fri, 23 Jan 2026 01:02:47 GMT  
		Size: 38.1 MB (38148810 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29bc45cda383aba4c99496147cb74ef665d3d04b2c597ba9f117cb849e925346`  
		Last Modified: Fri, 23 Jan 2026 01:02:49 GMT  
		Size: 137.0 MB (136988872 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a798dfa7dfff03b4241054e93ba6fe892c027f2c384496bdbc83d4b9a70ef5d3`  
		Last Modified: Fri, 23 Jan 2026 01:02:45 GMT  
		Size: 29.3 KB (29316 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:jdk21-ubi10` - unknown; unknown

```console
$ docker pull gradle@sha256:4146d81a9ac6e6dcb264cbd480ef79262e901bf5957d1d79800fc7554f6cea16
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 MB (7049055 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4311f69e3cac149183cb9f3f080ca9ab4c51522618fe016904348c4dcd183d17`

```dockerfile
```

-	Layers:
	-	`sha256:11cc149a9362948adc548c4d85dd4a0312dacb39f2fa19e8e7f2841b8e461042`  
		Last Modified: Fri, 23 Jan 2026 01:02:46 GMT  
		Size: 7.0 MB (7024407 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:efa31b03cfa2138fadad532ecc1f94ff36a2863f8f7fbfff8a970b467e3930bb`  
		Last Modified: Fri, 23 Jan 2026 01:02:45 GMT  
		Size: 24.6 KB (24648 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:jdk21-ubi10` - linux; ppc64le

```console
$ docker pull gradle@sha256:3a9a0c0e93ab2804cde4ec9429d51e53a8e601870f3e94c8699f41db9bf3aea9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **413.2 MB (413169993 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c943c5d0df7c2e1a33b51ee4f8166b1a5f50414be9261116f9174ea7706e642`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["gradle"]`

```dockerfile
# Thu, 22 Jan 2026 14:54:45 GMT
LABEL maintainer="Red Hat, Inc."
# Thu, 22 Jan 2026 14:54:45 GMT
LABEL vendor="Red Hat, Inc."
# Thu, 22 Jan 2026 14:54:45 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Thu, 22 Jan 2026 14:54:45 GMT
LABEL com.redhat.component="ubi10-minimal-container"       name="ubi10/ubi-minimal"       version="10.1"       cpe="cpe:/o:redhat:enterprise_linux:10.1"       distribution-scope="public"
# Thu, 22 Jan 2026 14:54:45 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Thu, 22 Jan 2026 14:54:45 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 10."
# Thu, 22 Jan 2026 14:54:45 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 22 Jan 2026 14:54:45 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 22 Jan 2026 14:54:45 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 10 Minimal"
# Thu, 22 Jan 2026 14:54:45 GMT
LABEL io.openshift.expose-services=""
# Thu, 22 Jan 2026 14:54:45 GMT
LABEL io.openshift.tags="minimal rhel10"
# Thu, 22 Jan 2026 14:54:45 GMT
ENV container oci
# Thu, 22 Jan 2026 14:54:45 GMT
COPY dir:7bdbe74d43c251ef87ffde9a283489e444dd9e506bb8c01cd1c97a9f3ac52ddd in /      
# Thu, 22 Jan 2026 14:54:45 GMT
COPY file:5de33b5fc08b00635bccf9134a18978dba13e2250aa51838f9969515a3957847 in /etc/yum.repos.d/.      
# Thu, 22 Jan 2026 14:54:45 GMT
CMD ["/bin/bash"]
# Thu, 22 Jan 2026 14:54:46 GMT
COPY file:595171150af68abc798ea385f7988d74b566aa8e84babff137f00b08b2164683 in /usr/share/buildinfo/content-sets.json      
# Thu, 22 Jan 2026 14:54:46 GMT
COPY file:595171150af68abc798ea385f7988d74b566aa8e84babff137f00b08b2164683 in /root/buildinfo/content_manifests/content-sets.json      
# Thu, 22 Jan 2026 14:54:46 GMT
COPY file:fa7fed90e5fa59b018eb8aa0c4c26e4f0c5e15ab4b12ea84973f9ece212d9ed6 in /usr/share/buildinfo/labels.json      
# Thu, 22 Jan 2026 14:54:46 GMT
COPY file:fa7fed90e5fa59b018eb8aa0c4c26e4f0c5e15ab4b12ea84973f9ece212d9ed6 in /root/buildinfo/labels.json      
# Thu, 22 Jan 2026 14:54:46 GMT
LABEL "architecture"="ppc64le" "vcs-type"="git" "vcs-ref"="0912ab420a80f21132d8a5e29d19a23339176677" "org.opencontainers.image.revision"="0912ab420a80f21132d8a5e29d19a23339176677" "build-date"="2026-01-22T14:54:33Z" "org.opencontainers.image.created"="2026-01-22T14:54:33Z" "release"="1769090502"org.opencontainers.image.revision=0912ab420a80f21132d8a5e29d19a23339176677,org.opencontainers.image.created=2026-01-22T14:54:33Z
# Fri, 23 Jan 2026 00:57:54 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 23 Jan 2026 00:57:54 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 23 Jan 2026 00:57:54 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 23 Jan 2026 00:57:54 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en         gnupg2     ;     microdnf clean all # buildkit
# Fri, 23 Jan 2026 00:57:54 GMT
ENV JAVA_VERSION=jdk-21.0.9+10
# Fri, 23 Jan 2026 01:01:22 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='edf0da4debe7cf475dbe320d174d6eed81479eb363f41e38a2efb740428c603a';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.9%2B10/OpenJDK21U-jdk_aarch64_linux_hotspot_21.0.9_10.tar.gz';          ;;        ppc64le)          ESUM='ac5a0394a234269b4e20459649ac93cb702cde29b3e46a0bcf3aa53958f2d4a4';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.9%2B10/OpenJDK21U-jdk_ppc64le_linux_hotspot_21.0.9_10.tar.gz';          ;;        s390x)          ESUM='e8ede0fb48aaa3a0cc1ac7c8522f8ca7938bdbb8be0d603b61134de7f898aff4';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.9%2B10/OpenJDK21U-jdk_s390x_linux_hotspot_21.0.9_10.tar.gz';          ;;        x86_64)          ESUM='810d3773df7e0d6c4394e4e244b264c8b30e0b05a0acf542d065fd78a6b65c2f';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.9%2B10/OpenJDK21U-jdk_x64_linux_hotspot_21.0.9_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Fri, 23 Jan 2026 01:01:26 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Fri, 23 Jan 2026 01:01:26 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Fri, 23 Jan 2026 01:01:26 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Fri, 23 Jan 2026 01:01:26 GMT
CMD ["jshell"]
# Fri, 23 Jan 2026 01:07:02 GMT
CMD ["gradle"]
# Fri, 23 Jan 2026 01:07:02 GMT
ENV GRADLE_HOME=/opt/gradle
# Fri, 23 Jan 2026 01:07:02 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 101 gradle     && useradd --system --gid gradle --uid 101 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Fri, 23 Jan 2026 01:07:02 GMT
VOLUME [/home/gradle/.gradle]
# Fri, 23 Jan 2026 01:07:03 GMT
WORKDIR /home/gradle
# Fri, 23 Jan 2026 01:07:32 GMT
RUN set -o errexit -o nounset     && microdnf install -y         make         curl-minimal         wget         tar                 findutils                 unzip         which                 git         git-lfs         subversion     && microdnf clean all         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which svn # buildkit
# Fri, 23 Jan 2026 01:07:32 GMT
ENV GRADLE_VERSION=9.3.0
# Fri, 23 Jan 2026 01:07:32 GMT
ARG GRADLE_DOWNLOAD_SHA256=0d585f69da091fc5b2beced877feab55a3064d43b8a1d46aeb07996b0915e0e0
# Fri, 23 Jan 2026 01:07:41 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=0d585f69da091fc5b2beced877feab55a3064d43b8a1d46aeb07996b0915e0e0
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Fri, 23 Jan 2026 01:07:41 GMT
USER gradle
# Fri, 23 Jan 2026 01:07:43 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=0d585f69da091fc5b2beced877feab55a3064d43b8a1d46aeb07996b0915e0e0
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --stacktrace --debug --version # buildkit
# Fri, 23 Jan 2026 01:07:43 GMT
USER root
```

-	Layers:
	-	`sha256:ca7d82d686e4448886b5d40d7ede2a94863423d05f007fae2fdf719fb557a51e`  
		Last Modified: Thu, 22 Jan 2026 18:12:54 GMT  
		Size: 38.7 MB (38718444 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b83cbc42d47e675c60991c0dfbc843db7691ef4e8247a33f719b14ab372f6ea2`  
		Last Modified: Fri, 23 Jan 2026 00:58:44 GMT  
		Size: 39.1 MB (39124637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87228f48a761f1c36de6bb309eb0d148248e0aa1f0a2dfa320dc5be35ed963c9`  
		Last Modified: Fri, 23 Jan 2026 01:02:15 GMT  
		Size: 157.9 MB (157943484 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6c0e46f5ba5fb1a6f2e65a3d2fc5a3dff9cf95d4879254a134e642adfcc0157`  
		Last Modified: Fri, 23 Jan 2026 01:02:11 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b712d5dce91ea9d08ea33e2c7e564e07c0268f08ae2e6c75acbbd2f94c5153b2`  
		Last Modified: Fri, 23 Jan 2026 01:02:11 GMT  
		Size: 2.3 KB (2291 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1192bd690c7d5de501c6323258379d9033d9e5a6938b536a97756c60cc088266`  
		Last Modified: Fri, 23 Jan 2026 01:08:30 GMT  
		Size: 1.6 KB (1583 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14b5455f9d174ee7831147df30a773a606a6f4759b4b82e980a50856fc2c6872`  
		Last Modified: Fri, 23 Jan 2026 01:08:33 GMT  
		Size: 40.4 MB (40390139 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5564defc2456e11edfc83137ce9487f1c39f2a1fa2c3209a809578bb8ece3bb`  
		Last Modified: Fri, 23 Jan 2026 01:08:35 GMT  
		Size: 137.0 MB (136988876 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2652007258257d5f259481cdde867bea1172bda7c427e5c1335ebc1fe1ae376d`  
		Last Modified: Fri, 23 Jan 2026 01:08:30 GMT  
		Size: 378.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:jdk21-ubi10` - unknown; unknown

```console
$ docker pull gradle@sha256:c78fbfb3c3b0aa63d2bd100f02277bbcff79ed7ad98927bbc9c740612c0a87d4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 MB (7042092 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:53021a9a1b4b03224e60c839644a31d68d75e0f7942661ae08acab210979af14`

```dockerfile
```

-	Layers:
	-	`sha256:cdf48563b3715e5c0cfe08acb7bb36381725e65304c0addd038ae8e7d7d55d40`  
		Last Modified: Fri, 23 Jan 2026 01:08:31 GMT  
		Size: 7.0 MB (7017569 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:08c09d6a2772a697393b13f6318505455b612cb2ad4f62344fb018c85275d130`  
		Last Modified: Fri, 23 Jan 2026 01:08:30 GMT  
		Size: 24.5 KB (24523 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:jdk21-ubi10` - linux; s390x

```console
$ docker pull gradle@sha256:f2b7399e4c6f90eac4219fb724c2c57849bc7f680039f8828085b553203acf1f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **396.9 MB (396922733 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b1de723c3e53f0620dc3493a304491644d316b503c2ca6e7b718f5216e2af204`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["gradle"]`

```dockerfile
# Thu, 22 Jan 2026 14:57:07 GMT
LABEL maintainer="Red Hat, Inc."
# Thu, 22 Jan 2026 14:57:07 GMT
LABEL vendor="Red Hat, Inc."
# Thu, 22 Jan 2026 14:57:07 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Thu, 22 Jan 2026 14:57:07 GMT
LABEL com.redhat.component="ubi10-minimal-container"       name="ubi10/ubi-minimal"       version="10.1"       cpe="cpe:/o:redhat:enterprise_linux:10.1"       distribution-scope="public"
# Thu, 22 Jan 2026 14:57:07 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Thu, 22 Jan 2026 14:57:07 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 10."
# Thu, 22 Jan 2026 14:57:07 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 22 Jan 2026 14:57:07 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 22 Jan 2026 14:57:07 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 10 Minimal"
# Thu, 22 Jan 2026 14:57:08 GMT
LABEL io.openshift.expose-services=""
# Thu, 22 Jan 2026 14:57:08 GMT
LABEL io.openshift.tags="minimal rhel10"
# Thu, 22 Jan 2026 14:57:08 GMT
ENV container oci
# Thu, 22 Jan 2026 14:57:08 GMT
COPY dir:b163faed476797909497b9e9cbceacce9d202c7df0108da15dd805a940495105 in /      
# Thu, 22 Jan 2026 14:57:08 GMT
COPY file:5de33b5fc08b00635bccf9134a18978dba13e2250aa51838f9969515a3957847 in /etc/yum.repos.d/.      
# Thu, 22 Jan 2026 14:57:08 GMT
CMD ["/bin/bash"]
# Thu, 22 Jan 2026 14:57:08 GMT
COPY file:595171150af68abc798ea385f7988d74b566aa8e84babff137f00b08b2164683 in /usr/share/buildinfo/content-sets.json      
# Thu, 22 Jan 2026 14:57:08 GMT
COPY file:595171150af68abc798ea385f7988d74b566aa8e84babff137f00b08b2164683 in /root/buildinfo/content_manifests/content-sets.json      
# Thu, 22 Jan 2026 14:57:08 GMT
COPY file:d6bdaa4e7d25601d04555b39b781ff4f9dacbc577ea220997429cff55f920063 in /usr/share/buildinfo/labels.json      
# Thu, 22 Jan 2026 14:57:08 GMT
COPY file:d6bdaa4e7d25601d04555b39b781ff4f9dacbc577ea220997429cff55f920063 in /root/buildinfo/labels.json      
# Thu, 22 Jan 2026 14:57:09 GMT
LABEL "architecture"="s390x" "vcs-type"="git" "vcs-ref"="0912ab420a80f21132d8a5e29d19a23339176677" "org.opencontainers.image.revision"="0912ab420a80f21132d8a5e29d19a23339176677" "build-date"="2026-01-22T14:54:50Z" "org.opencontainers.image.created"="2026-01-22T14:54:50Z" "release"="1769090502"org.opencontainers.image.revision=0912ab420a80f21132d8a5e29d19a23339176677,org.opencontainers.image.created=2026-01-22T14:54:50Z
# Fri, 23 Jan 2026 00:57:41 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 23 Jan 2026 00:57:41 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 23 Jan 2026 00:57:41 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 23 Jan 2026 00:57:41 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en         gnupg2     ;     microdnf clean all # buildkit
# Fri, 23 Jan 2026 00:57:41 GMT
ENV JAVA_VERSION=jdk-21.0.9+10
# Fri, 23 Jan 2026 00:58:26 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='edf0da4debe7cf475dbe320d174d6eed81479eb363f41e38a2efb740428c603a';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.9%2B10/OpenJDK21U-jdk_aarch64_linux_hotspot_21.0.9_10.tar.gz';          ;;        ppc64le)          ESUM='ac5a0394a234269b4e20459649ac93cb702cde29b3e46a0bcf3aa53958f2d4a4';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.9%2B10/OpenJDK21U-jdk_ppc64le_linux_hotspot_21.0.9_10.tar.gz';          ;;        s390x)          ESUM='e8ede0fb48aaa3a0cc1ac7c8522f8ca7938bdbb8be0d603b61134de7f898aff4';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.9%2B10/OpenJDK21U-jdk_s390x_linux_hotspot_21.0.9_10.tar.gz';          ;;        x86_64)          ESUM='810d3773df7e0d6c4394e4e244b264c8b30e0b05a0acf542d065fd78a6b65c2f';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.9%2B10/OpenJDK21U-jdk_x64_linux_hotspot_21.0.9_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Fri, 23 Jan 2026 00:58:27 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Fri, 23 Jan 2026 00:58:27 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Fri, 23 Jan 2026 00:58:27 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Fri, 23 Jan 2026 00:58:27 GMT
CMD ["jshell"]
# Fri, 23 Jan 2026 01:01:58 GMT
CMD ["gradle"]
# Fri, 23 Jan 2026 01:01:58 GMT
ENV GRADLE_HOME=/opt/gradle
# Fri, 23 Jan 2026 01:01:58 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 101 gradle     && useradd --system --gid gradle --uid 101 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Fri, 23 Jan 2026 01:01:58 GMT
VOLUME [/home/gradle/.gradle]
# Fri, 23 Jan 2026 01:01:58 GMT
WORKDIR /home/gradle
# Fri, 23 Jan 2026 01:02:06 GMT
RUN set -o errexit -o nounset     && microdnf install -y         make         curl-minimal         wget         tar                 findutils                 unzip         which                 git         git-lfs         subversion     && microdnf clean all         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which svn # buildkit
# Fri, 23 Jan 2026 01:02:06 GMT
ENV GRADLE_VERSION=9.3.0
# Fri, 23 Jan 2026 01:02:06 GMT
ARG GRADLE_DOWNLOAD_SHA256=0d585f69da091fc5b2beced877feab55a3064d43b8a1d46aeb07996b0915e0e0
# Fri, 23 Jan 2026 01:02:09 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=0d585f69da091fc5b2beced877feab55a3064d43b8a1d46aeb07996b0915e0e0
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Fri, 23 Jan 2026 01:02:09 GMT
USER gradle
# Fri, 23 Jan 2026 01:02:10 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=0d585f69da091fc5b2beced877feab55a3064d43b8a1d46aeb07996b0915e0e0
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --stacktrace --debug --version # buildkit
# Fri, 23 Jan 2026 01:02:10 GMT
USER root
```

-	Layers:
	-	`sha256:4305950dff5b7a63645441b4e7ab741317691b48df386123d1f9cf51b053ff55`  
		Last Modified: Thu, 22 Jan 2026 18:12:46 GMT  
		Size: 34.4 MB (34360531 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60a32a7eba25e3f29f4e39e71b6844c79632eddfad3907c76a741789b46122d0`  
		Last Modified: Fri, 23 Jan 2026 00:58:04 GMT  
		Size: 37.8 MB (37751890 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64d0a6aca915e3647b0f4593c2c1734d812fc6f26c115b5ac930e41a1e463e55`  
		Last Modified: Fri, 23 Jan 2026 00:58:54 GMT  
		Size: 147.1 MB (147068493 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43fa54d6be3f65ae7f0893965920ee243b6f114365fea43c1265270af16422db`  
		Last Modified: Fri, 23 Jan 2026 00:58:51 GMT  
		Size: 131.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1241bb9865204901db68628c77aed68da6f2504de1420eca9fc74f521dc37edd`  
		Last Modified: Fri, 23 Jan 2026 00:58:51 GMT  
		Size: 2.3 KB (2288 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:813cdc2334d1649f131e7ad9364b0d1d938b4341e4be9d47bad92420e52cd30a`  
		Last Modified: Fri, 23 Jan 2026 01:02:41 GMT  
		Size: 1.6 KB (1587 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acbb2f7be3bdff5fdb41748a69baaa0a62175b52c3a8eba41791211afa9c5758`  
		Last Modified: Fri, 23 Jan 2026 01:02:42 GMT  
		Size: 40.7 MB (40748531 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b64bbd89eee7ed3a2ea6e97d5af889190ae7213b7b5439134ea90b41e8178926`  
		Last Modified: Fri, 23 Jan 2026 01:02:43 GMT  
		Size: 137.0 MB (136988873 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b62b47656458bdf8f94a9485392856dea80bf6d71a24d7084ea536f0fa319af`  
		Last Modified: Fri, 23 Jan 2026 01:02:41 GMT  
		Size: 377.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:jdk21-ubi10` - unknown; unknown

```console
$ docker pull gradle@sha256:0c73cc7e2a22629cc24a08c4fda0161ae41beda7011c47c792de833c962254af
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 MB (7031247 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f2569507b17b113694e95c0547f13d5aafe46dcecda66815593cc0c547cd6ea`

```dockerfile
```

-	Layers:
	-	`sha256:f425bf9cba34ed9091c4d570a5ebf97905afc6004594f08a5959bb90ffec216c`  
		Last Modified: Fri, 23 Jan 2026 01:02:41 GMT  
		Size: 7.0 MB (7006798 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9d6f02c7a3ed72d87cbf3feeb1aa1f34cb2fdbca38d3ae7c83dcf170bebef412`  
		Last Modified: Fri, 23 Jan 2026 01:02:41 GMT  
		Size: 24.4 KB (24449 bytes)  
		MIME: application/vnd.in-toto+json
