## `gradle:jdk26-ubi10`

```console
$ docker pull gradle@sha256:e7471d277c102f81674b966e9929e89fff4ec3ec57a5429ed65deb7e5419078e
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

### `gradle:jdk26-ubi10` - linux; amd64

```console
$ docker pull gradle@sha256:0c233746cc98e3e6688318969fa1dc2c126d568354a1ca42d9a58a2556698690
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **345.7 MB (345747999 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:780ec0655d335225382d55a1e686e37b8ccaa3d313124be02d77bdb466a24f1b`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["gradle"]`

```dockerfile
# Tue, 12 May 2026 09:09:41 GMT
LABEL maintainer="Red Hat, Inc."
# Tue, 12 May 2026 09:09:41 GMT
LABEL vendor="Red Hat, Inc."
# Tue, 12 May 2026 09:09:41 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Tue, 12 May 2026 09:09:41 GMT
LABEL com.redhat.component="ubi10-minimal-container"       name="ubi10/ubi-minimal"       version="10.1"       cpe="cpe:/o:redhat:enterprise_linux:10.1"       distribution-scope="public"
# Tue, 12 May 2026 09:09:41 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Tue, 12 May 2026 09:09:41 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 10."
# Tue, 12 May 2026 09:09:41 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Tue, 12 May 2026 09:09:41 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Tue, 12 May 2026 09:09:41 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 10 Minimal"
# Tue, 12 May 2026 09:09:41 GMT
LABEL io.openshift.expose-services=""
# Tue, 12 May 2026 09:09:41 GMT
LABEL io.openshift.tags="minimal rhel10"
# Tue, 12 May 2026 09:09:41 GMT
ENV container oci
# Tue, 12 May 2026 09:09:41 GMT
COPY dir:70c9e4dfd7df3debe1e0457260915a9c0446c87d882b979cfec229a5714bf4c7 in /      
# Tue, 12 May 2026 09:09:41 GMT
COPY file:5de33b5fc08b00635bccf9134a18978dba13e2250aa51838f9969515a3957847 in /etc/yum.repos.d/.      
# Tue, 12 May 2026 09:09:41 GMT
CMD ["/bin/bash"]
# Tue, 12 May 2026 09:09:42 GMT
COPY file:595171150af68abc798ea385f7988d74b566aa8e84babff137f00b08b2164683 in /usr/share/buildinfo/content-sets.json      
# Tue, 12 May 2026 09:09:42 GMT
COPY file:595171150af68abc798ea385f7988d74b566aa8e84babff137f00b08b2164683 in /root/buildinfo/content_manifests/content-sets.json      
# Tue, 12 May 2026 09:09:42 GMT
COPY file:0753abbd85f48d60c6079bc7ee41700b66d3abf1c27ef1da2779ce2ba16ca2c5 in /usr/share/buildinfo/labels.json      
# Tue, 12 May 2026 09:09:42 GMT
COPY file:0753abbd85f48d60c6079bc7ee41700b66d3abf1c27ef1da2779ce2ba16ca2c5 in /root/buildinfo/labels.json      
# Tue, 12 May 2026 09:09:42 GMT
LABEL "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="ad7cdeeb08da8825126b10f488e410b0de5902b0" "org.opencontainers.image.revision"="ad7cdeeb08da8825126b10f488e410b0de5902b0" "build-date"="2026-05-12T09:09:25Z" "org.opencontainers.image.created"="2026-05-12T09:09:25Z" "release"="1778576723"org.opencontainers.image.revision=ad7cdeeb08da8825126b10f488e410b0de5902b0,org.opencontainers.image.created=2026-05-12T09:09:25Z
# Fri, 15 May 2026 20:32:39 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 15 May 2026 20:32:39 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 15 May 2026 20:32:39 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 15 May 2026 20:32:39 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en         gnupg2     ;     microdnf clean all # buildkit
# Fri, 15 May 2026 20:32:39 GMT
ENV JAVA_VERSION=jdk-26.0.1+8
# Fri, 15 May 2026 20:32:45 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='613f9b2861dea937b24d5eca745ef8567733b377d0bb612195acaad0e3f61360';          BINARY_URL='https://github.com/adoptium/temurin26-binaries/releases/download/jdk-26.0.1%2B8/OpenJDK26U-jdk_aarch64_linux_hotspot_26.0.1_8.tar.gz';          ;;        ppc64le)          ESUM='60e016faf4177840430035d948f83f2887d556fe512b78c1d43b320322fe6685';          BINARY_URL='https://github.com/adoptium/temurin26-binaries/releases/download/jdk-26.0.1%2B8/OpenJDK26U-jdk_ppc64le_linux_hotspot_26.0.1_8.tar.gz';          ;;        s390x)          ESUM='942de7ded1427592a2a4b6dbea4083b2d0891de2626c7863e970de3e2819a93f';          BINARY_URL='https://github.com/adoptium/temurin26-binaries/releases/download/jdk-26.0.1%2B8/OpenJDK26U-jdk_s390x_linux_hotspot_26.0.1_8.tar.gz';          ;;        x86_64)          ESUM='8e512f13e575a43655fc92319436c94890c137b9035cc6bd6f9cf24239704d3a';          BINARY_URL='https://github.com/adoptium/temurin26-binaries/releases/download/jdk-26.0.1%2B8/OpenJDK26U-jdk_x64_linux_hotspot_26.0.1_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Fri, 15 May 2026 20:32:47 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Fri, 15 May 2026 20:32:47 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Fri, 15 May 2026 20:32:47 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Fri, 15 May 2026 20:32:47 GMT
CMD ["jshell"]
# Fri, 15 May 2026 21:16:32 GMT
CMD ["gradle"]
# Fri, 15 May 2026 21:16:32 GMT
ENV GRADLE_HOME=/opt/gradle
# Fri, 15 May 2026 21:16:32 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 101 gradle     && useradd --system --gid gradle --uid 101 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Fri, 15 May 2026 21:16:32 GMT
VOLUME [/home/gradle/.gradle]
# Fri, 15 May 2026 21:16:32 GMT
WORKDIR /home/gradle
# Fri, 15 May 2026 21:16:35 GMT
RUN set -o errexit -o nounset     && microdnf install -y         make         curl         wget         tar                 findutils                 unzip         which                 git         git-lfs         subversion     && microdnf clean all         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which svn # buildkit
# Fri, 15 May 2026 21:16:35 GMT
ENV GRADLE_VERSION=9.5.1
# Fri, 15 May 2026 21:16:35 GMT
ARG GRADLE_DOWNLOAD_SHA256=bafc141b619ad6350fd975fc903156dd5c151998cc8b058e8c1044ab5f7b031f
# Fri, 15 May 2026 21:16:38 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=bafc141b619ad6350fd975fc903156dd5c151998cc8b058e8c1044ab5f7b031f
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Fri, 15 May 2026 21:16:38 GMT
USER gradle
# Fri, 15 May 2026 21:16:38 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=bafc141b619ad6350fd975fc903156dd5c151998cc8b058e8c1044ab5f7b031f
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --stacktrace --debug --version # buildkit
# Fri, 15 May 2026 21:16:38 GMT
USER root
```

-	Layers:
	-	`sha256:20e8bbd1fa594932c31db6c97d64754bd505f260fa2792d4a021081374b77b54`  
		Last Modified: Tue, 12 May 2026 10:16:05 GMT  
		Size: 34.6 MB (34624258 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28b0da43c370cb097cfa55cddb565df753956c3601acffe750751bdc1721a6e5`  
		Last Modified: Fri, 15 May 2026 20:33:06 GMT  
		Size: 37.5 MB (37501105 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e24e994140f17848b370f3a466b2ffe7e53362fbf45fad60409814440ef5a438`  
		Last Modified: Fri, 15 May 2026 20:33:08 GMT  
		Size: 94.5 MB (94525454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd6a2f4f6c7ce6dcf42d07588053e0ee39066e570b8ca1d3d9e20e5ad8425e81`  
		Last Modified: Fri, 15 May 2026 20:33:05 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b46e56ff64529d974f9eaaa00c21673f7581d6dd331e7f38ddffff07257d4a5`  
		Last Modified: Fri, 15 May 2026 20:33:05 GMT  
		Size: 2.5 KB (2471 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87d32f2e4c238679bd56881be931092cf846a0b00a5260789916c4a87b79e52b`  
		Last Modified: Fri, 15 May 2026 21:16:55 GMT  
		Size: 1.6 KB (1582 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e5cecf0003799a546f1f4cc53e0430332089d5b1a9cccb1023d441512fa9c50`  
		Last Modified: Fri, 15 May 2026 21:16:57 GMT  
		Size: 38.8 MB (38830375 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:293e5d8b0396059a6e7699f3424e6eb72ce9cc472ffc87713b19536e666373a1`  
		Last Modified: Fri, 15 May 2026 21:17:00 GMT  
		Size: 140.2 MB (140236986 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f685ca972ab7779b53f85f162e4ae388920687ce868da8a97ac7e47387e4492`  
		Last Modified: Fri, 15 May 2026 21:16:55 GMT  
		Size: 25.6 KB (25607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:jdk26-ubi10` - unknown; unknown

```console
$ docker pull gradle@sha256:631c5f09cadfb69e11cecb5f9f50d0d143841cc9765989374f77c59b5090c672
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 MB (7045840 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e06513b2d5ec5be042a0af5fd5d68632010879b8ef51ef11c07fb78bbe517adf`

```dockerfile
```

-	Layers:
	-	`sha256:09ddaef3d297425a6909765f8517bf2202ed82431eafffcbf53324fa39089e59`  
		Last Modified: Fri, 15 May 2026 21:16:56 GMT  
		Size: 7.0 MB (7021419 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:827db64e69057e5460f745c5b1c07a417114dcc7ce18e777c9faa6f96ff7ea8d`  
		Last Modified: Fri, 15 May 2026 21:16:55 GMT  
		Size: 24.4 KB (24421 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:jdk26-ubi10` - linux; arm64 variant v8

```console
$ docker pull gradle@sha256:660b258365852597fb3977a61defa1e9d5d1b7dc399b667a955c90a2ebc5d5f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **342.3 MB (342253078 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:15e4b99a02b8c2285f1d8737295c5209a21ec9da08f29591ac2f0938c247cf82`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["gradle"]`

```dockerfile
# Tue, 12 May 2026 09:11:34 GMT
LABEL maintainer="Red Hat, Inc."
# Tue, 12 May 2026 09:11:34 GMT
LABEL vendor="Red Hat, Inc."
# Tue, 12 May 2026 09:11:34 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Tue, 12 May 2026 09:11:34 GMT
LABEL com.redhat.component="ubi10-minimal-container"       name="ubi10/ubi-minimal"       version="10.1"       cpe="cpe:/o:redhat:enterprise_linux:10.1"       distribution-scope="public"
# Tue, 12 May 2026 09:11:34 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Tue, 12 May 2026 09:11:34 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 10."
# Tue, 12 May 2026 09:11:34 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Tue, 12 May 2026 09:11:34 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Tue, 12 May 2026 09:11:34 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 10 Minimal"
# Tue, 12 May 2026 09:11:35 GMT
LABEL io.openshift.expose-services=""
# Tue, 12 May 2026 09:11:35 GMT
LABEL io.openshift.tags="minimal rhel10"
# Tue, 12 May 2026 09:11:35 GMT
ENV container oci
# Tue, 12 May 2026 09:11:35 GMT
COPY dir:2877d8ca2be54c031321bcf5c5c002de1e88fc4d881af88566c341114955d981 in /      
# Tue, 12 May 2026 09:11:35 GMT
COPY file:5de33b5fc08b00635bccf9134a18978dba13e2250aa51838f9969515a3957847 in /etc/yum.repos.d/.      
# Tue, 12 May 2026 09:11:35 GMT
CMD ["/bin/bash"]
# Tue, 12 May 2026 09:11:36 GMT
COPY file:595171150af68abc798ea385f7988d74b566aa8e84babff137f00b08b2164683 in /usr/share/buildinfo/content-sets.json      
# Tue, 12 May 2026 09:11:36 GMT
COPY file:595171150af68abc798ea385f7988d74b566aa8e84babff137f00b08b2164683 in /root/buildinfo/content_manifests/content-sets.json      
# Tue, 12 May 2026 09:11:36 GMT
COPY file:ed5db005734a9cf660fffe0f9d4de854f99deb1e83b8a69fd4b48dc74dea4448 in /usr/share/buildinfo/labels.json      
# Tue, 12 May 2026 09:11:36 GMT
COPY file:ed5db005734a9cf660fffe0f9d4de854f99deb1e83b8a69fd4b48dc74dea4448 in /root/buildinfo/labels.json      
# Tue, 12 May 2026 09:11:36 GMT
LABEL "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="ad7cdeeb08da8825126b10f488e410b0de5902b0" "org.opencontainers.image.revision"="ad7cdeeb08da8825126b10f488e410b0de5902b0" "build-date"="2026-05-12T09:11:19Z" "org.opencontainers.image.created"="2026-05-12T09:11:19Z" "release"="1778576723"org.opencontainers.image.revision=ad7cdeeb08da8825126b10f488e410b0de5902b0,org.opencontainers.image.created=2026-05-12T09:11:19Z
# Fri, 15 May 2026 20:32:28 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 15 May 2026 20:32:28 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 15 May 2026 20:32:28 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 15 May 2026 20:32:28 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en         gnupg2     ;     microdnf clean all # buildkit
# Fri, 15 May 2026 20:32:28 GMT
ENV JAVA_VERSION=jdk-26.0.1+8
# Fri, 15 May 2026 20:32:34 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='613f9b2861dea937b24d5eca745ef8567733b377d0bb612195acaad0e3f61360';          BINARY_URL='https://github.com/adoptium/temurin26-binaries/releases/download/jdk-26.0.1%2B8/OpenJDK26U-jdk_aarch64_linux_hotspot_26.0.1_8.tar.gz';          ;;        ppc64le)          ESUM='60e016faf4177840430035d948f83f2887d556fe512b78c1d43b320322fe6685';          BINARY_URL='https://github.com/adoptium/temurin26-binaries/releases/download/jdk-26.0.1%2B8/OpenJDK26U-jdk_ppc64le_linux_hotspot_26.0.1_8.tar.gz';          ;;        s390x)          ESUM='942de7ded1427592a2a4b6dbea4083b2d0891de2626c7863e970de3e2819a93f';          BINARY_URL='https://github.com/adoptium/temurin26-binaries/releases/download/jdk-26.0.1%2B8/OpenJDK26U-jdk_s390x_linux_hotspot_26.0.1_8.tar.gz';          ;;        x86_64)          ESUM='8e512f13e575a43655fc92319436c94890c137b9035cc6bd6f9cf24239704d3a';          BINARY_URL='https://github.com/adoptium/temurin26-binaries/releases/download/jdk-26.0.1%2B8/OpenJDK26U-jdk_x64_linux_hotspot_26.0.1_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Fri, 15 May 2026 20:32:36 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Fri, 15 May 2026 20:32:36 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Fri, 15 May 2026 20:32:36 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Fri, 15 May 2026 20:32:36 GMT
CMD ["jshell"]
# Fri, 15 May 2026 20:35:10 GMT
CMD ["gradle"]
# Fri, 15 May 2026 20:35:10 GMT
ENV GRADLE_HOME=/opt/gradle
# Fri, 15 May 2026 20:35:10 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 101 gradle     && useradd --system --gid gradle --uid 101 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Fri, 15 May 2026 20:35:10 GMT
VOLUME [/home/gradle/.gradle]
# Fri, 15 May 2026 20:35:10 GMT
WORKDIR /home/gradle
# Fri, 15 May 2026 20:35:14 GMT
RUN set -o errexit -o nounset     && microdnf install -y         make         curl         wget         tar                 findutils                 unzip         which                 git         git-lfs         subversion     && microdnf clean all         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which svn # buildkit
# Fri, 15 May 2026 20:35:14 GMT
ENV GRADLE_VERSION=9.5.1
# Fri, 15 May 2026 20:35:14 GMT
ARG GRADLE_DOWNLOAD_SHA256=bafc141b619ad6350fd975fc903156dd5c151998cc8b058e8c1044ab5f7b031f
# Fri, 15 May 2026 20:35:17 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=bafc141b619ad6350fd975fc903156dd5c151998cc8b058e8c1044ab5f7b031f
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Fri, 15 May 2026 20:35:17 GMT
USER gradle
# Fri, 15 May 2026 20:35:17 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=bafc141b619ad6350fd975fc903156dd5c151998cc8b058e8c1044ab5f7b031f
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --stacktrace --debug --version # buildkit
# Fri, 15 May 2026 20:35:17 GMT
USER root
```

-	Layers:
	-	`sha256:24bccfaffdcba4dab6b032daed65e4f69253b002d2af6f83ce7d6d966c20583a`  
		Last Modified: Tue, 12 May 2026 10:25:24 GMT  
		Size: 32.7 MB (32711659 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26f46f113310840da4d985371ee53707fdb8ccb269806fd5fc46ad910f3d3b9f`  
		Last Modified: Fri, 15 May 2026 20:32:55 GMT  
		Size: 37.4 MB (37443276 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0cfb4893ec8686de0f1f678fbf792d61662b4f1372945832e0c09169e9ab40e`  
		Last Modified: Fri, 15 May 2026 20:32:56 GMT  
		Size: 93.5 MB (93505313 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11a6a0c0a1026dc89182d600f722dc74ea42237fa0b60ad8a24b4a4e84c1e9d5`  
		Last Modified: Fri, 15 May 2026 20:32:53 GMT  
		Size: 130.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69d566f01039cb0f8c29664ef48f083f5df6fafbc63846a9d3904e3167893453`  
		Last Modified: Fri, 15 May 2026 20:32:53 GMT  
		Size: 2.5 KB (2471 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04e2d05f126ec53837168b0d4926a0bdd6f9e465d93cfde2848bd0eeeaae6678`  
		Last Modified: Fri, 15 May 2026 20:35:36 GMT  
		Size: 1.6 KB (1586 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f25d2c0c31b8dbcf1955896eaab7bfa2f3cbddb3ac492e60685de4e332d6817a`  
		Last Modified: Fri, 15 May 2026 20:35:38 GMT  
		Size: 38.3 MB (38322287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4c3cc97f55c8064f6722290f5e4aa051953798afc6921b329f5a36a4c204e25`  
		Last Modified: Fri, 15 May 2026 20:35:40 GMT  
		Size: 140.2 MB (140236988 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f7f3294eee8d85fab040302f51a0cd40043de204d5826db00880671c0dcc490`  
		Last Modified: Fri, 15 May 2026 20:35:36 GMT  
		Size: 29.3 KB (29336 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:jdk26-ubi10` - unknown; unknown

```console
$ docker pull gradle@sha256:3f34df923010d4c9b1e165cef3686b937d816769c6e42238f3f161b114bffd52
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 MB (7044289 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d05775917a2976631ed5cdcb74bb3aa23b52a6961cbe1c69feedc62527d7e8fd`

```dockerfile
```

-	Layers:
	-	`sha256:ab7691e03729254b31d68e9130df65c3f776143b919ed6bd90bdc73f93f95866`  
		Last Modified: Fri, 15 May 2026 20:35:36 GMT  
		Size: 7.0 MB (7019672 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:079eb02bdf79cd5a0767ec231a18cef1916121d5a320d5feb49f43bc22dd03e6`  
		Last Modified: Fri, 15 May 2026 20:35:36 GMT  
		Size: 24.6 KB (24617 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:jdk26-ubi10` - linux; ppc64le

```console
$ docker pull gradle@sha256:996a60b08613c9004aac1d0b42d82dfd20bbc0ef42b881f117120324c3ba5a1b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **352.8 MB (352770727 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:669829620f981cb29eaee605c79a8ab5bf1e16bf16390890854b8e03b33c3964`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["gradle"]`

```dockerfile
# Tue, 12 May 2026 09:13:30 GMT
LABEL maintainer="Red Hat, Inc."
# Tue, 12 May 2026 09:13:30 GMT
LABEL vendor="Red Hat, Inc."
# Tue, 12 May 2026 09:13:30 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Tue, 12 May 2026 09:13:30 GMT
LABEL com.redhat.component="ubi10-minimal-container"       name="ubi10/ubi-minimal"       version="10.1"       cpe="cpe:/o:redhat:enterprise_linux:10.1"       distribution-scope="public"
# Tue, 12 May 2026 09:13:30 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Tue, 12 May 2026 09:13:30 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 10."
# Tue, 12 May 2026 09:13:30 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Tue, 12 May 2026 09:13:30 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Tue, 12 May 2026 09:13:30 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 10 Minimal"
# Tue, 12 May 2026 09:13:31 GMT
LABEL io.openshift.expose-services=""
# Tue, 12 May 2026 09:13:31 GMT
LABEL io.openshift.tags="minimal rhel10"
# Tue, 12 May 2026 09:13:31 GMT
ENV container oci
# Tue, 12 May 2026 09:13:32 GMT
COPY dir:584fbc93c21a7184a941a4142a12f835dcfca07a9a2dfc5bd8298fc624407c1a in /      
# Tue, 12 May 2026 09:13:32 GMT
COPY file:5de33b5fc08b00635bccf9134a18978dba13e2250aa51838f9969515a3957847 in /etc/yum.repos.d/.      
# Tue, 12 May 2026 09:13:32 GMT
CMD ["/bin/bash"]
# Tue, 12 May 2026 09:13:32 GMT
COPY file:595171150af68abc798ea385f7988d74b566aa8e84babff137f00b08b2164683 in /usr/share/buildinfo/content-sets.json      
# Tue, 12 May 2026 09:13:32 GMT
COPY file:595171150af68abc798ea385f7988d74b566aa8e84babff137f00b08b2164683 in /root/buildinfo/content_manifests/content-sets.json      
# Tue, 12 May 2026 09:13:33 GMT
COPY file:101e1b19e6d0f9785c2d23ecc61947a5882edebf262baa5a4ebcee0c3b40e8a2 in /usr/share/buildinfo/labels.json      
# Tue, 12 May 2026 09:13:33 GMT
COPY file:101e1b19e6d0f9785c2d23ecc61947a5882edebf262baa5a4ebcee0c3b40e8a2 in /root/buildinfo/labels.json      
# Tue, 12 May 2026 09:13:33 GMT
LABEL "architecture"="ppc64le" "vcs-type"="git" "vcs-ref"="ad7cdeeb08da8825126b10f488e410b0de5902b0" "org.opencontainers.image.revision"="ad7cdeeb08da8825126b10f488e410b0de5902b0" "build-date"="2026-05-12T09:13:14Z" "org.opencontainers.image.created"="2026-05-12T09:13:14Z" "release"="1778576723"org.opencontainers.image.revision=ad7cdeeb08da8825126b10f488e410b0de5902b0,org.opencontainers.image.created=2026-05-12T09:13:14Z
# Tue, 12 May 2026 23:31:50 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 12 May 2026 23:31:50 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 May 2026 23:31:50 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 12 May 2026 23:31:50 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en         gnupg2     ;     microdnf clean all # buildkit
# Tue, 12 May 2026 23:31:50 GMT
ENV JAVA_VERSION=jdk-26.0.1+8
# Fri, 15 May 2026 20:38:31 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='613f9b2861dea937b24d5eca745ef8567733b377d0bb612195acaad0e3f61360';          BINARY_URL='https://github.com/adoptium/temurin26-binaries/releases/download/jdk-26.0.1%2B8/OpenJDK26U-jdk_aarch64_linux_hotspot_26.0.1_8.tar.gz';          ;;        ppc64le)          ESUM='60e016faf4177840430035d948f83f2887d556fe512b78c1d43b320322fe6685';          BINARY_URL='https://github.com/adoptium/temurin26-binaries/releases/download/jdk-26.0.1%2B8/OpenJDK26U-jdk_ppc64le_linux_hotspot_26.0.1_8.tar.gz';          ;;        s390x)          ESUM='942de7ded1427592a2a4b6dbea4083b2d0891de2626c7863e970de3e2819a93f';          BINARY_URL='https://github.com/adoptium/temurin26-binaries/releases/download/jdk-26.0.1%2B8/OpenJDK26U-jdk_s390x_linux_hotspot_26.0.1_8.tar.gz';          ;;        x86_64)          ESUM='8e512f13e575a43655fc92319436c94890c137b9035cc6bd6f9cf24239704d3a';          BINARY_URL='https://github.com/adoptium/temurin26-binaries/releases/download/jdk-26.0.1%2B8/OpenJDK26U-jdk_x64_linux_hotspot_26.0.1_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Fri, 15 May 2026 20:38:35 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Fri, 15 May 2026 20:38:35 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Fri, 15 May 2026 20:38:35 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Fri, 15 May 2026 20:38:35 GMT
CMD ["jshell"]
# Fri, 15 May 2026 21:17:02 GMT
CMD ["gradle"]
# Fri, 15 May 2026 21:17:02 GMT
ENV GRADLE_HOME=/opt/gradle
# Fri, 15 May 2026 21:17:02 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 101 gradle     && useradd --system --gid gradle --uid 101 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Fri, 15 May 2026 21:17:02 GMT
VOLUME [/home/gradle/.gradle]
# Fri, 15 May 2026 21:17:03 GMT
WORKDIR /home/gradle
# Fri, 15 May 2026 21:17:45 GMT
RUN set -o errexit -o nounset     && microdnf install -y         make         curl         wget         tar                 findutils                 unzip         which                 git         git-lfs         subversion     && microdnf clean all         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which svn # buildkit
# Fri, 15 May 2026 21:17:45 GMT
ENV GRADLE_VERSION=9.5.1
# Fri, 15 May 2026 21:17:45 GMT
ARG GRADLE_DOWNLOAD_SHA256=bafc141b619ad6350fd975fc903156dd5c151998cc8b058e8c1044ab5f7b031f
# Fri, 15 May 2026 21:17:51 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=bafc141b619ad6350fd975fc903156dd5c151998cc8b058e8c1044ab5f7b031f
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Fri, 15 May 2026 21:17:51 GMT
USER gradle
# Fri, 15 May 2026 21:17:53 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=bafc141b619ad6350fd975fc903156dd5c151998cc8b058e8c1044ab5f7b031f
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --stacktrace --debug --version # buildkit
# Fri, 15 May 2026 21:17:53 GMT
USER root
```

-	Layers:
	-	`sha256:f815e851aa9d271f09d3448e8acc95ebed62472057c9b0368d01b242d1468875`  
		Last Modified: Tue, 12 May 2026 12:16:14 GMT  
		Size: 38.8 MB (38794493 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d1fdf741746dd4482bfc42d70a6f2954201df0346c653d262b3e220a6a63447`  
		Last Modified: Tue, 12 May 2026 23:32:30 GMT  
		Size: 39.3 MB (39255778 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6e65321d2d4bc756ae4aa79534a08a84af5677368435b9b674ce7a563a19e6e`  
		Last Modified: Fri, 15 May 2026 20:39:09 GMT  
		Size: 93.9 MB (93902398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:734a9b50d7fb1d8fe742949ee2054e4289d456a00614bc200873de77d4c7d754`  
		Last Modified: Fri, 15 May 2026 20:39:07 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c0165a83f801000b2ec396e64d8d9eddfa7074b03bb1da7ae486ad90853e35d`  
		Last Modified: Fri, 15 May 2026 20:39:07 GMT  
		Size: 2.5 KB (2470 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:197e60c20e301c384de672be9bff6080ef99c9ce88638330f3b7aa826ea625a2`  
		Last Modified: Fri, 15 May 2026 21:18:30 GMT  
		Size: 1.6 KB (1591 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4fbb6bcaffaafb7eb510cee8da4fa908a408dda0f66289938d9eb6ebb586cca9`  
		Last Modified: Fri, 15 May 2026 21:18:32 GMT  
		Size: 40.6 MB (40576471 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06a22a639d5f741c21707fd9ea603a5c2deacf7eddecd0b34dd32d425d7b4639`  
		Last Modified: Fri, 15 May 2026 21:18:34 GMT  
		Size: 140.2 MB (140236985 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b1b55c67d3dc58c33c3b2a109ef793e8375c03408211f34fa959b1b01fa194f`  
		Last Modified: Fri, 15 May 2026 21:18:30 GMT  
		Size: 380.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:jdk26-ubi10` - unknown; unknown

```console
$ docker pull gradle@sha256:173130d8b38be861acc40e5af24f1db96475cea011a7c16eca49b722afadd50b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 MB (7021266 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:60f209aaaf9809c029c33dd265f211bad4c94c8e0aafa3773b5c92111ed61a05`

```dockerfile
```

-	Layers:
	-	`sha256:e2e4521d261dc86ecd236e6db1aed08e673e081ac39346df3823687206186c24`  
		Last Modified: Fri, 15 May 2026 21:18:30 GMT  
		Size: 7.0 MB (6996773 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7423e139d0cc4b9e493f0ac7304029037317eb0231beacbc6e4dd1775ac81151`  
		Last Modified: Fri, 15 May 2026 21:18:30 GMT  
		Size: 24.5 KB (24493 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:jdk26-ubi10` - linux; s390x

```console
$ docker pull gradle@sha256:19d6041d0b1994ff77cfd8469845a31c915fff0c064d33eb753028ec01b8a4cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **344.0 MB (344037292 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8bfa95253202056c944e019f2af6f13bbe19b711b2a4212423da644156396373`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["gradle"]`

```dockerfile
# Tue, 12 May 2026 09:27:49 GMT
LABEL maintainer="Red Hat, Inc."
# Tue, 12 May 2026 09:27:49 GMT
LABEL vendor="Red Hat, Inc."
# Tue, 12 May 2026 09:27:49 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Tue, 12 May 2026 09:27:49 GMT
LABEL com.redhat.component="ubi10-minimal-container"       name="ubi10/ubi-minimal"       version="10.1"       cpe="cpe:/o:redhat:enterprise_linux:10.1"       distribution-scope="public"
# Tue, 12 May 2026 09:27:49 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Tue, 12 May 2026 09:27:49 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 10."
# Tue, 12 May 2026 09:27:49 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Tue, 12 May 2026 09:27:49 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Tue, 12 May 2026 09:27:49 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 10 Minimal"
# Tue, 12 May 2026 09:27:49 GMT
LABEL io.openshift.expose-services=""
# Tue, 12 May 2026 09:27:49 GMT
LABEL io.openshift.tags="minimal rhel10"
# Tue, 12 May 2026 09:27:49 GMT
ENV container oci
# Tue, 12 May 2026 09:27:49 GMT
COPY dir:ad73fd8372aea6e68c9b3ea90e4901b979a82fb0f4a43074fa7ea61354ab30b9 in /      
# Tue, 12 May 2026 09:27:49 GMT
COPY file:5de33b5fc08b00635bccf9134a18978dba13e2250aa51838f9969515a3957847 in /etc/yum.repos.d/.      
# Tue, 12 May 2026 09:27:49 GMT
CMD ["/bin/bash"]
# Tue, 12 May 2026 09:27:49 GMT
COPY file:595171150af68abc798ea385f7988d74b566aa8e84babff137f00b08b2164683 in /usr/share/buildinfo/content-sets.json      
# Tue, 12 May 2026 09:27:50 GMT
COPY file:595171150af68abc798ea385f7988d74b566aa8e84babff137f00b08b2164683 in /root/buildinfo/content_manifests/content-sets.json      
# Tue, 12 May 2026 09:27:50 GMT
COPY file:f69727366f08991ceef4955068ba3462c331e0d11189e73f45fe959e3f50f354 in /usr/share/buildinfo/labels.json      
# Tue, 12 May 2026 09:27:50 GMT
COPY file:f69727366f08991ceef4955068ba3462c331e0d11189e73f45fe959e3f50f354 in /root/buildinfo/labels.json      
# Tue, 12 May 2026 09:27:50 GMT
LABEL "architecture"="s390x" "vcs-type"="git" "vcs-ref"="ad7cdeeb08da8825126b10f488e410b0de5902b0" "org.opencontainers.image.revision"="ad7cdeeb08da8825126b10f488e410b0de5902b0" "build-date"="2026-05-12T09:27:06Z" "org.opencontainers.image.created"="2026-05-12T09:27:06Z" "release"="1778576723"org.opencontainers.image.revision=ad7cdeeb08da8825126b10f488e410b0de5902b0,org.opencontainers.image.created=2026-05-12T09:27:06Z
# Tue, 12 May 2026 23:33:20 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 12 May 2026 23:33:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 May 2026 23:33:20 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 12 May 2026 23:33:20 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en         gnupg2     ;     microdnf clean all # buildkit
# Tue, 12 May 2026 23:33:20 GMT
ENV JAVA_VERSION=jdk-26.0.1+8
# Fri, 15 May 2026 20:39:39 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='613f9b2861dea937b24d5eca745ef8567733b377d0bb612195acaad0e3f61360';          BINARY_URL='https://github.com/adoptium/temurin26-binaries/releases/download/jdk-26.0.1%2B8/OpenJDK26U-jdk_aarch64_linux_hotspot_26.0.1_8.tar.gz';          ;;        ppc64le)          ESUM='60e016faf4177840430035d948f83f2887d556fe512b78c1d43b320322fe6685';          BINARY_URL='https://github.com/adoptium/temurin26-binaries/releases/download/jdk-26.0.1%2B8/OpenJDK26U-jdk_ppc64le_linux_hotspot_26.0.1_8.tar.gz';          ;;        s390x)          ESUM='942de7ded1427592a2a4b6dbea4083b2d0891de2626c7863e970de3e2819a93f';          BINARY_URL='https://github.com/adoptium/temurin26-binaries/releases/download/jdk-26.0.1%2B8/OpenJDK26U-jdk_s390x_linux_hotspot_26.0.1_8.tar.gz';          ;;        x86_64)          ESUM='8e512f13e575a43655fc92319436c94890c137b9035cc6bd6f9cf24239704d3a';          BINARY_URL='https://github.com/adoptium/temurin26-binaries/releases/download/jdk-26.0.1%2B8/OpenJDK26U-jdk_x64_linux_hotspot_26.0.1_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Fri, 15 May 2026 20:39:43 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Fri, 15 May 2026 20:39:44 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Fri, 15 May 2026 20:39:44 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Fri, 15 May 2026 20:39:44 GMT
CMD ["jshell"]
# Fri, 15 May 2026 21:16:42 GMT
CMD ["gradle"]
# Fri, 15 May 2026 21:16:42 GMT
ENV GRADLE_HOME=/opt/gradle
# Fri, 15 May 2026 21:16:42 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 101 gradle     && useradd --system --gid gradle --uid 101 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Fri, 15 May 2026 21:16:42 GMT
VOLUME [/home/gradle/.gradle]
# Fri, 15 May 2026 21:16:43 GMT
WORKDIR /home/gradle
# Fri, 15 May 2026 21:17:20 GMT
RUN set -o errexit -o nounset     && microdnf install -y         make         curl         wget         tar                 findutils                 unzip         which                 git         git-lfs         subversion     && microdnf clean all         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which svn # buildkit
# Fri, 15 May 2026 21:17:20 GMT
ENV GRADLE_VERSION=9.5.1
# Fri, 15 May 2026 21:17:20 GMT
ARG GRADLE_DOWNLOAD_SHA256=bafc141b619ad6350fd975fc903156dd5c151998cc8b058e8c1044ab5f7b031f
# Fri, 15 May 2026 21:17:26 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=bafc141b619ad6350fd975fc903156dd5c151998cc8b058e8c1044ab5f7b031f
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Fri, 15 May 2026 21:17:26 GMT
USER gradle
# Fri, 15 May 2026 21:17:28 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=bafc141b619ad6350fd975fc903156dd5c151998cc8b058e8c1044ab5f7b031f
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --stacktrace --debug --version # buildkit
# Fri, 15 May 2026 21:17:28 GMT
USER root
```

-	Layers:
	-	`sha256:716b8ccfad2ab26e031483f83283392459a7160cf7d641599a620a485af51f10`  
		Last Modified: Tue, 12 May 2026 12:16:04 GMT  
		Size: 34.5 MB (34450081 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7dec299a1602bf5e0d62202cf77938cca794fdd9ba9bbc56e355abbc7a6a990b`  
		Last Modified: Tue, 12 May 2026 23:33:57 GMT  
		Size: 37.9 MB (37879929 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b73299f4912e862fa2a2cf214ac34578f7ae82f37eb12e612bca48338e9235c`  
		Last Modified: Fri, 15 May 2026 20:41:19 GMT  
		Size: 90.5 MB (90537390 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24141a7d9bdc4d9e494e608278494255fc2c1e5d691b09c5a23f6544525c6b4d`  
		Last Modified: Fri, 15 May 2026 20:41:16 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ac7eb468d8ab4686e91fefc1940b41173f2cb9ac0ecb75fe381480021ed882e`  
		Last Modified: Fri, 15 May 2026 20:41:16 GMT  
		Size: 2.5 KB (2470 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d118f203df5242fe97cdf90106e7ac3e277ab163f2434e24dcdcd228c62b243`  
		Last Modified: Fri, 15 May 2026 21:18:19 GMT  
		Size: 1.6 KB (1594 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd5420276a40c9dc278d6fb2df5d93272cbf5f685eefad8845d5cf357d852dd7`  
		Last Modified: Fri, 15 May 2026 21:18:22 GMT  
		Size: 40.9 MB (40928300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c771fa11dc62e61fbf4c43149e1f7059680acc97249fb320f6651e44d15f8811`  
		Last Modified: Fri, 15 May 2026 21:18:25 GMT  
		Size: 140.2 MB (140236989 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2fa8eda675479755d24fa73aa70c4a72a1088e37b349bcf13051f721ce35110`  
		Last Modified: Fri, 15 May 2026 21:18:19 GMT  
		Size: 379.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:jdk26-ubi10` - unknown; unknown

```console
$ docker pull gradle@sha256:0dc8c5d84139f8c52e0b57afa5158a71ae270be2a1d86ec7834784a302897c17
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 MB (7011668 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd340ac0aeeb90cc892c1870b5347db918ef572b17728d010f3f5087a53417f0`

```dockerfile
```

-	Layers:
	-	`sha256:5d05ae20c33e4700ecad9018f103140fb7a1956dcc9c06e9a5d4ef90152095b0`  
		Last Modified: Fri, 15 May 2026 21:18:20 GMT  
		Size: 7.0 MB (6987252 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3ad3e0d24e684042c908b0a3f7944989be2528571d57adb2fb7e40d76547d13e`  
		Last Modified: Fri, 15 May 2026 21:18:19 GMT  
		Size: 24.4 KB (24416 bytes)  
		MIME: application/vnd.in-toto+json
