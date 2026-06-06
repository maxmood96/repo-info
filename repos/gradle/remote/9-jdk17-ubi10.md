## `gradle:9-jdk17-ubi10`

```console
$ docker pull gradle@sha256:b9f075fc9df45ab8392526c8a69703c063a30e3cc5869ef5fcfa9a9f0d8099be
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

### `gradle:9-jdk17-ubi10` - linux; amd64

```console
$ docker pull gradle@sha256:32859807cd703366abf7dfc3de538a2714a028399863bbaf6999a0d784a239ac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **398.6 MB (398648038 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:119d4a59dd52848d933adeb6872800908383a247a84f0085e0eb97c914d7e009`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["gradle"]`

```dockerfile
# Thu, 04 Jun 2026 05:28:17 GMT
LABEL maintainer="Red Hat, Inc."
# Thu, 04 Jun 2026 05:28:17 GMT
LABEL vendor="Red Hat, Inc."
# Thu, 04 Jun 2026 05:28:17 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Thu, 04 Jun 2026 05:28:17 GMT
LABEL com.redhat.component="ubi10-minimal-container"       name="ubi10/ubi-minimal"       version="10.2"       cpe="cpe:/o:redhat:enterprise_linux:10.2"       distribution-scope="public"
# Thu, 04 Jun 2026 05:28:17 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Thu, 04 Jun 2026 05:28:17 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 10."
# Thu, 04 Jun 2026 05:28:17 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 04 Jun 2026 05:28:17 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 04 Jun 2026 05:28:17 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 10 Minimal"
# Thu, 04 Jun 2026 05:28:17 GMT
LABEL io.openshift.expose-services=""
# Thu, 04 Jun 2026 05:28:17 GMT
LABEL io.openshift.tags="minimal rhel10"
# Thu, 04 Jun 2026 05:28:17 GMT
ENV container oci
# Thu, 04 Jun 2026 05:28:18 GMT
COPY dir:66f2b108fa49d46a69e413fb7db9e6ed9263f39ff05950d04e99329222ef439c in /      
# Thu, 04 Jun 2026 05:28:18 GMT
COPY file:5de33b5fc08b00635bccf9134a18978dba13e2250aa51838f9969515a3957847 in /etc/yum.repos.d/.      
# Thu, 04 Jun 2026 05:28:18 GMT
CMD ["/bin/bash"]
# Thu, 04 Jun 2026 05:28:18 GMT
COPY file:595171150af68abc798ea385f7988d74b566aa8e84babff137f00b08b2164683 in /usr/share/buildinfo/content-sets.json      
# Thu, 04 Jun 2026 05:28:18 GMT
COPY file:595171150af68abc798ea385f7988d74b566aa8e84babff137f00b08b2164683 in /root/buildinfo/content_manifests/content-sets.json      
# Thu, 04 Jun 2026 05:28:18 GMT
COPY file:fd262bedfa32870622b193d94f9285fa7e55dee323c33ad89ff9af707ddb8c11 in /usr/share/buildinfo/labels.json      
# Thu, 04 Jun 2026 05:28:18 GMT
COPY file:fd262bedfa32870622b193d94f9285fa7e55dee323c33ad89ff9af707ddb8c11 in /root/buildinfo/labels.json      
# Thu, 04 Jun 2026 05:28:18 GMT
LABEL "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="21e748607cdf3bfe567bea40c2e0c654a3c7766c" "org.opencontainers.image.revision"="21e748607cdf3bfe567bea40c2e0c654a3c7766c" "build-date"="2026-06-04T05:28:04Z" "org.opencontainers.image.created"="2026-06-04T05:28:04Z" "release"="1780550715"org.opencontainers.image.revision=21e748607cdf3bfe567bea40c2e0c654a3c7766c,org.opencontainers.image.created=2026-06-04T05:28:04Z
# Fri, 05 Jun 2026 22:42:55 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 05 Jun 2026 22:42:55 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 05 Jun 2026 22:42:55 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 05 Jun 2026 22:42:55 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en         gnupg2     ;     microdnf clean all # buildkit
# Fri, 05 Jun 2026 22:42:55 GMT
ENV JAVA_VERSION=jdk-17.0.19+10
# Fri, 05 Jun 2026 22:43:01 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='83a52172678ec8975164648654869cb2e71d7c748b47aca94b29bbfa10c18e81';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.19%2B10/OpenJDK17U-jdk_aarch64_linux_hotspot_17.0.19_10.tar.gz';          ;;        ppc64le)          ESUM='c9d8dc52960ff00aa8c321e211cc5284a2151cffdedeac998f5297066cbad245';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.19%2B10/OpenJDK17U-jdk_ppc64le_linux_hotspot_17.0.19_10.tar.gz';          ;;        s390x)          ESUM='00363a5ceda57aa0dee89d20b3f6b2966e3c1f3fb6dcf57e66d2264573d3c63e';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.19%2B10/OpenJDK17U-jdk_s390x_linux_hotspot_17.0.19_10.tar.gz';          ;;        x86_64)          ESUM='d8afc263758141a66e0e3aafc321e783f7016696f4eaea067d340a269037d331';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.19%2B10/OpenJDK17U-jdk_x64_linux_hotspot_17.0.19_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Fri, 05 Jun 2026 22:43:02 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Fri, 05 Jun 2026 22:43:02 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Fri, 05 Jun 2026 22:43:02 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Fri, 05 Jun 2026 22:43:02 GMT
CMD ["jshell"]
# Sat, 06 Jun 2026 00:16:12 GMT
CMD ["gradle"]
# Sat, 06 Jun 2026 00:16:12 GMT
ENV GRADLE_HOME=/opt/gradle
# Sat, 06 Jun 2026 00:16:12 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 101 gradle     && useradd --system --gid gradle --uid 101 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Sat, 06 Jun 2026 00:16:12 GMT
VOLUME [/home/gradle/.gradle]
# Sat, 06 Jun 2026 00:16:12 GMT
WORKDIR /home/gradle
# Sat, 06 Jun 2026 00:16:15 GMT
RUN set -o errexit -o nounset     && microdnf install -y         make         curl-minimal         wget         tar                 findutils                 unzip         which                 git         git-lfs         subversion     && microdnf clean all         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which svn # buildkit
# Sat, 06 Jun 2026 00:16:15 GMT
ENV GRADLE_VERSION=9.5.1
# Sat, 06 Jun 2026 00:16:15 GMT
ARG GRADLE_DOWNLOAD_SHA256=bafc141b619ad6350fd975fc903156dd5c151998cc8b058e8c1044ab5f7b031f
# Sat, 06 Jun 2026 00:16:18 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=bafc141b619ad6350fd975fc903156dd5c151998cc8b058e8c1044ab5f7b031f
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Sat, 06 Jun 2026 00:16:18 GMT
USER gradle
# Sat, 06 Jun 2026 00:16:18 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=bafc141b619ad6350fd975fc903156dd5c151998cc8b058e8c1044ab5f7b031f
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --stacktrace --debug --version # buildkit
# Sat, 06 Jun 2026 00:16:18 GMT
USER root
```

-	Layers:
	-	`sha256:39798aa98bd37b2e4ff77c414dd42bca72e522aa2cb338296f10696a239cb2b2`  
		Last Modified: Thu, 04 Jun 2026 06:53:25 GMT  
		Size: 34.9 MB (34854739 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e9c9875edda4235ada509a4d7b209421ff54e07ffbcd838fac042fc04c773eb`  
		Last Modified: Fri, 05 Jun 2026 22:43:21 GMT  
		Size: 37.8 MB (37760550 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e3b70cd3bffb99217c88ee42cdfae79e7bd03e8dbc8f477f849476ef1e7c922`  
		Last Modified: Fri, 05 Jun 2026 22:43:23 GMT  
		Size: 145.9 MB (145915466 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28e497c04e41694ac5bf93dd28464b142efb692ff9451b8f1839060b925c5028`  
		Last Modified: Fri, 05 Jun 2026 22:43:19 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7066237271f2740e15cacfb1ec139ea3c3cad8307b7b4873c8d93d85d3de3d6`  
		Last Modified: Fri, 05 Jun 2026 22:43:19 GMT  
		Size: 2.3 KB (2290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2db529f0f3d15499e3907b20a075e99d1c8d2f6cfba60f41f1074e45333c6a5`  
		Last Modified: Sat, 06 Jun 2026 00:16:36 GMT  
		Size: 1.6 KB (1590 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e2d404a646f053f9b424978fcacabbd830fe07815d12fa50a9a09a9d45c5801`  
		Last Modified: Sat, 06 Jun 2026 00:16:38 GMT  
		Size: 39.9 MB (39850645 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1a1bf23382873d532af0ef511a88038fb7ba7f6619a1b0c767f2713bbc3dc79`  
		Last Modified: Sat, 06 Jun 2026 00:16:41 GMT  
		Size: 140.2 MB (140236988 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a0efa49d3099d6a2cd4e57ca5e5a0942b12ff3c85609a09bcec091ed027704e`  
		Last Modified: Sat, 06 Jun 2026 00:16:36 GMT  
		Size: 25.6 KB (25610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:9-jdk17-ubi10` - unknown; unknown

```console
$ docker pull gradle@sha256:1f094fd6897b5e19444fe63be3167623a3cf4b79bd45fcf1046307fb684f3a0c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.1 MB (7101199 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c7d351118528bcbcf3489a2089fa935f8dadca1abd4e835867454d5cd616f2f7`

```dockerfile
```

-	Layers:
	-	`sha256:e4dbf680c8eb53c422f2f14167249a5e35cac2fc1061f94fda7d6db58a7fde2d`  
		Last Modified: Sat, 06 Jun 2026 00:16:37 GMT  
		Size: 7.1 MB (7076744 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2a6100bac4e85075fe9c845adfe4a6fcf1ade6b78e32272ffa054cbbd1016b4d`  
		Last Modified: Sat, 06 Jun 2026 00:16:36 GMT  
		Size: 24.5 KB (24455 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:9-jdk17-ubi10` - linux; arm64 variant v8

```console
$ docker pull gradle@sha256:c35eff77a33a80e3117d205316cc1182129a67a623224a22dc5b48a51d1bf300
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **395.0 MB (395040516 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b1954465aa0936ab8c0cf76cf23c17da91f959a9f5de7e9a8e930d15d7d05e84`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["gradle"]`

```dockerfile
# Thu, 04 Jun 2026 05:32:13 GMT
LABEL maintainer="Red Hat, Inc."
# Thu, 04 Jun 2026 05:32:13 GMT
LABEL vendor="Red Hat, Inc."
# Thu, 04 Jun 2026 05:32:13 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Thu, 04 Jun 2026 05:32:13 GMT
LABEL com.redhat.component="ubi10-minimal-container"       name="ubi10/ubi-minimal"       version="10.2"       cpe="cpe:/o:redhat:enterprise_linux:10.2"       distribution-scope="public"
# Thu, 04 Jun 2026 05:32:13 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Thu, 04 Jun 2026 05:32:13 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 10."
# Thu, 04 Jun 2026 05:32:13 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 04 Jun 2026 05:32:13 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 04 Jun 2026 05:32:13 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 10 Minimal"
# Thu, 04 Jun 2026 05:32:13 GMT
LABEL io.openshift.expose-services=""
# Thu, 04 Jun 2026 05:32:13 GMT
LABEL io.openshift.tags="minimal rhel10"
# Thu, 04 Jun 2026 05:32:13 GMT
ENV container oci
# Thu, 04 Jun 2026 05:32:14 GMT
COPY dir:742cf4548328149a0d3b299bb0ecd0a71c615bfaf88aa6d4360ecf931aab8785 in /      
# Thu, 04 Jun 2026 05:32:14 GMT
COPY file:5de33b5fc08b00635bccf9134a18978dba13e2250aa51838f9969515a3957847 in /etc/yum.repos.d/.      
# Thu, 04 Jun 2026 05:32:14 GMT
CMD ["/bin/bash"]
# Thu, 04 Jun 2026 05:32:14 GMT
COPY file:595171150af68abc798ea385f7988d74b566aa8e84babff137f00b08b2164683 in /usr/share/buildinfo/content-sets.json      
# Thu, 04 Jun 2026 05:32:14 GMT
COPY file:595171150af68abc798ea385f7988d74b566aa8e84babff137f00b08b2164683 in /root/buildinfo/content_manifests/content-sets.json      
# Thu, 04 Jun 2026 05:32:14 GMT
COPY file:857742e0cb2c063297a5d6df57ad39367bc23ea5335b6bce896696d17d2eb019 in /usr/share/buildinfo/labels.json      
# Thu, 04 Jun 2026 05:32:14 GMT
COPY file:857742e0cb2c063297a5d6df57ad39367bc23ea5335b6bce896696d17d2eb019 in /root/buildinfo/labels.json      
# Thu, 04 Jun 2026 05:32:14 GMT
LABEL "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="21e748607cdf3bfe567bea40c2e0c654a3c7766c" "org.opencontainers.image.revision"="21e748607cdf3bfe567bea40c2e0c654a3c7766c" "build-date"="2026-06-04T05:31:57Z" "org.opencontainers.image.created"="2026-06-04T05:31:57Z" "release"="1780550715"org.opencontainers.image.revision=21e748607cdf3bfe567bea40c2e0c654a3c7766c,org.opencontainers.image.created=2026-06-04T05:31:57Z
# Fri, 05 Jun 2026 22:43:17 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 05 Jun 2026 22:43:17 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 05 Jun 2026 22:43:17 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 05 Jun 2026 22:43:17 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en         gnupg2     ;     microdnf clean all # buildkit
# Fri, 05 Jun 2026 22:43:17 GMT
ENV JAVA_VERSION=jdk-17.0.19+10
# Fri, 05 Jun 2026 22:43:23 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='83a52172678ec8975164648654869cb2e71d7c748b47aca94b29bbfa10c18e81';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.19%2B10/OpenJDK17U-jdk_aarch64_linux_hotspot_17.0.19_10.tar.gz';          ;;        ppc64le)          ESUM='c9d8dc52960ff00aa8c321e211cc5284a2151cffdedeac998f5297066cbad245';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.19%2B10/OpenJDK17U-jdk_ppc64le_linux_hotspot_17.0.19_10.tar.gz';          ;;        s390x)          ESUM='00363a5ceda57aa0dee89d20b3f6b2966e3c1f3fb6dcf57e66d2264573d3c63e';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.19%2B10/OpenJDK17U-jdk_s390x_linux_hotspot_17.0.19_10.tar.gz';          ;;        x86_64)          ESUM='d8afc263758141a66e0e3aafc321e783f7016696f4eaea067d340a269037d331';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.19%2B10/OpenJDK17U-jdk_x64_linux_hotspot_17.0.19_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Fri, 05 Jun 2026 22:43:24 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Fri, 05 Jun 2026 22:43:24 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Fri, 05 Jun 2026 22:43:24 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Fri, 05 Jun 2026 22:43:24 GMT
CMD ["jshell"]
# Sat, 06 Jun 2026 00:16:13 GMT
CMD ["gradle"]
# Sat, 06 Jun 2026 00:16:13 GMT
ENV GRADLE_HOME=/opt/gradle
# Sat, 06 Jun 2026 00:16:13 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 101 gradle     && useradd --system --gid gradle --uid 101 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Sat, 06 Jun 2026 00:16:13 GMT
VOLUME [/home/gradle/.gradle]
# Sat, 06 Jun 2026 00:16:13 GMT
WORKDIR /home/gradle
# Sat, 06 Jun 2026 00:16:17 GMT
RUN set -o errexit -o nounset     && microdnf install -y         make         curl-minimal         wget         tar                 findutils                 unzip         which                 git         git-lfs         subversion     && microdnf clean all         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which svn # buildkit
# Sat, 06 Jun 2026 00:16:17 GMT
ENV GRADLE_VERSION=9.5.1
# Sat, 06 Jun 2026 00:16:17 GMT
ARG GRADLE_DOWNLOAD_SHA256=bafc141b619ad6350fd975fc903156dd5c151998cc8b058e8c1044ab5f7b031f
# Sat, 06 Jun 2026 00:16:20 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=bafc141b619ad6350fd975fc903156dd5c151998cc8b058e8c1044ab5f7b031f
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Sat, 06 Jun 2026 00:16:20 GMT
USER gradle
# Sat, 06 Jun 2026 00:16:20 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=bafc141b619ad6350fd975fc903156dd5c151998cc8b058e8c1044ab5f7b031f
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --stacktrace --debug --version # buildkit
# Sat, 06 Jun 2026 00:16:20 GMT
USER root
```

-	Layers:
	-	`sha256:ebf3c43a43d516c400d687e8a210bad7522ec8a8a6c34ae1d72a70004f06bc71`  
		Last Modified: Thu, 04 Jun 2026 06:53:34 GMT  
		Size: 33.0 MB (33039715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ef1e960ca25feef989ecc0441aa2d6e0b0c0891ecb7a4320e565296fa8cddfc`  
		Last Modified: Fri, 05 Jun 2026 22:43:43 GMT  
		Size: 37.7 MB (37686393 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca9fbc0db2f094f82db85188bdfd0b81d5f91e845eb9fb57019b74786ca8df58`  
		Last Modified: Fri, 05 Jun 2026 22:43:45 GMT  
		Size: 144.7 MB (144734872 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5314fef722eddaf148b633f6d3891c60dcaa0565a9bb5f5bc6036d527e7e7ae7`  
		Last Modified: Fri, 05 Jun 2026 22:43:41 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac0e7f2c44b7cbb5f85383168af7f7a016b5b533fc14c2e0a91f72b234c0efce`  
		Last Modified: Fri, 05 Jun 2026 22:43:33 GMT  
		Size: 2.3 KB (2291 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8ff07b527797b7bf9775df0aad9bfeb0ff22135c21b110d7d30f0373d9fdaa2`  
		Last Modified: Sat, 06 Jun 2026 00:16:40 GMT  
		Size: 1.6 KB (1587 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6735afe5a10daf8b4cb1cd11870145422d6dcbe25b9a8cf6f1091a21697517c`  
		Last Modified: Sat, 06 Jun 2026 00:16:42 GMT  
		Size: 39.3 MB (39309175 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c49ff9d12440456c422080d56d4b68e7649e791fb2a0eb78505e394a6a00c4bc`  
		Last Modified: Sat, 06 Jun 2026 00:16:44 GMT  
		Size: 140.2 MB (140236986 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3cc53c7a119681fa4765d27e62e77ec727e489cbd37f666f609b1a764c3a55ba`  
		Last Modified: Sat, 06 Jun 2026 00:16:40 GMT  
		Size: 29.3 KB (29339 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:9-jdk17-ubi10` - unknown; unknown

```console
$ docker pull gradle@sha256:0dcae1b5bc0a74100d18b5363e55e0922e515ecf20b3c1e5447cc6dec6decc72
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.1 MB (7099651 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:181870d62f630ca8b10ec732c933b00f09358320527e15f532b95166926de850`

```dockerfile
```

-	Layers:
	-	`sha256:e2e477092334ccb96c4a8e55cf67614f54c8fa4f422cc9604cb797202110c5f4`  
		Last Modified: Sat, 06 Jun 2026 00:16:40 GMT  
		Size: 7.1 MB (7075000 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c8d78925d79f6613ae532571d47a152ede4aa3f714b0e302c80e3bc5525f88b7`  
		Last Modified: Sat, 06 Jun 2026 00:16:40 GMT  
		Size: 24.7 KB (24651 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:9-jdk17-ubi10` - linux; ppc64le

```console
$ docker pull gradle@sha256:078f172860ac243c4ab97320df833d257a2538f7b3e9a5b40d3d5c3cd0b3269d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **406.2 MB (406176703 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:65231e23abd6d23a2b331775cb89516179306ebd1bc62dc02777cc54f2038c0d`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["gradle"]`

```dockerfile
# Thu, 04 Jun 2026 05:32:40 GMT
LABEL maintainer="Red Hat, Inc."
# Thu, 04 Jun 2026 05:32:40 GMT
LABEL vendor="Red Hat, Inc."
# Thu, 04 Jun 2026 05:32:40 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Thu, 04 Jun 2026 05:32:40 GMT
LABEL com.redhat.component="ubi10-minimal-container"       name="ubi10/ubi-minimal"       version="10.2"       cpe="cpe:/o:redhat:enterprise_linux:10.2"       distribution-scope="public"
# Thu, 04 Jun 2026 05:32:40 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Thu, 04 Jun 2026 05:32:40 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 10."
# Thu, 04 Jun 2026 05:32:40 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 04 Jun 2026 05:32:40 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 04 Jun 2026 05:32:40 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 10 Minimal"
# Thu, 04 Jun 2026 05:32:40 GMT
LABEL io.openshift.expose-services=""
# Thu, 04 Jun 2026 05:32:40 GMT
LABEL io.openshift.tags="minimal rhel10"
# Thu, 04 Jun 2026 05:32:40 GMT
ENV container oci
# Thu, 04 Jun 2026 05:32:41 GMT
COPY dir:39feacb07d6a39793cfb5ecb8ce42cbba48072d5e83b48decf5ed170f1dae59f in /      
# Thu, 04 Jun 2026 05:32:41 GMT
COPY file:5de33b5fc08b00635bccf9134a18978dba13e2250aa51838f9969515a3957847 in /etc/yum.repos.d/.      
# Thu, 04 Jun 2026 05:32:41 GMT
CMD ["/bin/bash"]
# Thu, 04 Jun 2026 05:32:41 GMT
COPY file:595171150af68abc798ea385f7988d74b566aa8e84babff137f00b08b2164683 in /usr/share/buildinfo/content-sets.json      
# Thu, 04 Jun 2026 05:32:41 GMT
COPY file:595171150af68abc798ea385f7988d74b566aa8e84babff137f00b08b2164683 in /root/buildinfo/content_manifests/content-sets.json      
# Thu, 04 Jun 2026 05:32:41 GMT
COPY file:5a88f34d22fc0aaa3bcdde8758372a2e49b97b3dec16ffb3a17985ea3396531b in /usr/share/buildinfo/labels.json      
# Thu, 04 Jun 2026 05:32:41 GMT
COPY file:5a88f34d22fc0aaa3bcdde8758372a2e49b97b3dec16ffb3a17985ea3396531b in /root/buildinfo/labels.json      
# Thu, 04 Jun 2026 05:32:42 GMT
LABEL "architecture"="ppc64le" "vcs-type"="git" "vcs-ref"="21e748607cdf3bfe567bea40c2e0c654a3c7766c" "org.opencontainers.image.revision"="21e748607cdf3bfe567bea40c2e0c654a3c7766c" "build-date"="2026-06-04T05:32:29Z" "org.opencontainers.image.created"="2026-06-04T05:32:29Z" "release"="1780550715"org.opencontainers.image.revision=21e748607cdf3bfe567bea40c2e0c654a3c7766c,org.opencontainers.image.created=2026-06-04T05:32:29Z
# Fri, 05 Jun 2026 23:18:00 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 05 Jun 2026 23:18:00 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 05 Jun 2026 23:18:00 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 05 Jun 2026 23:18:00 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en         gnupg2     ;     microdnf clean all # buildkit
# Fri, 05 Jun 2026 23:18:00 GMT
ENV JAVA_VERSION=jdk-17.0.19+10
# Fri, 05 Jun 2026 23:19:57 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='83a52172678ec8975164648654869cb2e71d7c748b47aca94b29bbfa10c18e81';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.19%2B10/OpenJDK17U-jdk_aarch64_linux_hotspot_17.0.19_10.tar.gz';          ;;        ppc64le)          ESUM='c9d8dc52960ff00aa8c321e211cc5284a2151cffdedeac998f5297066cbad245';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.19%2B10/OpenJDK17U-jdk_ppc64le_linux_hotspot_17.0.19_10.tar.gz';          ;;        s390x)          ESUM='00363a5ceda57aa0dee89d20b3f6b2966e3c1f3fb6dcf57e66d2264573d3c63e';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.19%2B10/OpenJDK17U-jdk_s390x_linux_hotspot_17.0.19_10.tar.gz';          ;;        x86_64)          ESUM='d8afc263758141a66e0e3aafc321e783f7016696f4eaea067d340a269037d331';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.19%2B10/OpenJDK17U-jdk_x64_linux_hotspot_17.0.19_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Fri, 05 Jun 2026 23:20:00 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Fri, 05 Jun 2026 23:20:00 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Fri, 05 Jun 2026 23:20:00 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Fri, 05 Jun 2026 23:20:00 GMT
CMD ["jshell"]
# Sat, 06 Jun 2026 00:38:27 GMT
CMD ["gradle"]
# Sat, 06 Jun 2026 00:38:27 GMT
ENV GRADLE_HOME=/opt/gradle
# Sat, 06 Jun 2026 00:38:27 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 101 gradle     && useradd --system --gid gradle --uid 101 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Sat, 06 Jun 2026 00:38:27 GMT
VOLUME [/home/gradle/.gradle]
# Sat, 06 Jun 2026 00:38:27 GMT
WORKDIR /home/gradle
# Sat, 06 Jun 2026 00:38:41 GMT
RUN set -o errexit -o nounset     && microdnf install -y         make         curl-minimal         wget         tar                 findutils                 unzip         which                 git         git-lfs         subversion     && microdnf clean all         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which svn # buildkit
# Sat, 06 Jun 2026 00:38:41 GMT
ENV GRADLE_VERSION=9.5.1
# Sat, 06 Jun 2026 00:38:41 GMT
ARG GRADLE_DOWNLOAD_SHA256=bafc141b619ad6350fd975fc903156dd5c151998cc8b058e8c1044ab5f7b031f
# Sat, 06 Jun 2026 00:38:47 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=bafc141b619ad6350fd975fc903156dd5c151998cc8b058e8c1044ab5f7b031f
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Sat, 06 Jun 2026 00:38:47 GMT
USER gradle
# Sat, 06 Jun 2026 00:38:51 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=bafc141b619ad6350fd975fc903156dd5c151998cc8b058e8c1044ab5f7b031f
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --stacktrace --debug --version # buildkit
# Sat, 06 Jun 2026 00:38:51 GMT
USER root
```

-	Layers:
	-	`sha256:0548d638ade0e4394f010f8571f1879c4b09c3ac5cba2ccff7dfa8b2c88574b5`  
		Last Modified: Thu, 04 Jun 2026 06:53:50 GMT  
		Size: 39.0 MB (39010615 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:386aabc3a75f4ee1e9a3070c6e92d370f6789fef7ef5aa8020778d4f20d9234b`  
		Last Modified: Fri, 05 Jun 2026 23:18:37 GMT  
		Size: 39.5 MB (39520609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ea16818fc3ff1477abccac281cd700ca97669cf40b7d43e7dd25b8712ab1c6e`  
		Last Modified: Fri, 05 Jun 2026 23:20:37 GMT  
		Size: 145.8 MB (145788699 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1200ce0fd5ab383a9574e9810681104e601ebbc9911f1e8ab7a21aba37ce26f4`  
		Last Modified: Fri, 05 Jun 2026 23:20:32 GMT  
		Size: 132.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a98b9b76b446e5a4838292051c2fbaf7d76529e8769f979205595a533b1f2ef8`  
		Last Modified: Fri, 05 Jun 2026 23:20:33 GMT  
		Size: 2.3 KB (2291 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d8ddfae1c1c1919c230223f66e22dd523b3302f224594cb81037da8d2c7782b`  
		Last Modified: Sat, 06 Jun 2026 00:39:32 GMT  
		Size: 1.6 KB (1588 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6029fa8724dab20ea195e633201cd31eb7bf79b28b92296a9e7c47716e88983`  
		Last Modified: Sat, 06 Jun 2026 00:39:34 GMT  
		Size: 41.6 MB (41615366 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:582a7bc99661d85ab1c5bce40dcc9baefa441d6cc2a3033aa138190f7e3df788`  
		Last Modified: Sat, 06 Jun 2026 00:39:36 GMT  
		Size: 140.2 MB (140236988 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fda8b59e7f75cf9ebd5541508c0a071d79fb9925cb69014709893974bed8d01`  
		Last Modified: Sat, 06 Jun 2026 00:39:32 GMT  
		Size: 383.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:9-jdk17-ubi10` - unknown; unknown

```console
$ docker pull gradle@sha256:bbe199a94add8fe7b4597523d0d8f0af1a33c76c1824f3b6208b8bc72dd6f0bd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.1 MB (7092689 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b1b1de487c9d13a35231b9159cb0142019563949fb158ad52b5c5892608e5b0d`

```dockerfile
```

-	Layers:
	-	`sha256:cad4f06592e7b423f056038d497367e4fbd39f0a256c584f4f3505ef70263cce`  
		Last Modified: Sat, 06 Jun 2026 00:39:32 GMT  
		Size: 7.1 MB (7068162 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1b9f84469aef4850fdb922691fd508d5f790a7ea67eb568b73e3487feb532e5b`  
		Last Modified: Sat, 06 Jun 2026 00:39:31 GMT  
		Size: 24.5 KB (24527 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:9-jdk17-ubi10` - linux; s390x

```console
$ docker pull gradle@sha256:e1a9b9e2752666551e408e5f9405ce119f4e2c4e9088c8c9ee8bde7a3b42c580
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **391.0 MB (390978525 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b56e57c78f48f9b5fa0150f71d793cecc94b77246f21ba0521ed962bafb59eeb`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["gradle"]`

```dockerfile
# Thu, 04 Jun 2026 05:41:17 GMT
LABEL maintainer="Red Hat, Inc."
# Thu, 04 Jun 2026 05:41:17 GMT
LABEL vendor="Red Hat, Inc."
# Thu, 04 Jun 2026 05:41:17 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Thu, 04 Jun 2026 05:41:17 GMT
LABEL com.redhat.component="ubi10-minimal-container"       name="ubi10/ubi-minimal"       version="10.2"       cpe="cpe:/o:redhat:enterprise_linux:10.2"       distribution-scope="public"
# Thu, 04 Jun 2026 05:41:17 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Thu, 04 Jun 2026 05:41:17 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 10."
# Thu, 04 Jun 2026 05:41:17 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 04 Jun 2026 05:41:17 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 04 Jun 2026 05:41:17 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 10 Minimal"
# Thu, 04 Jun 2026 05:41:17 GMT
LABEL io.openshift.expose-services=""
# Thu, 04 Jun 2026 05:41:17 GMT
LABEL io.openshift.tags="minimal rhel10"
# Thu, 04 Jun 2026 05:41:17 GMT
ENV container oci
# Thu, 04 Jun 2026 05:41:17 GMT
COPY dir:9a20d45e3984f98caa7a89f40c9769c8ed59b525d31291027bc9643813420c60 in /      
# Thu, 04 Jun 2026 05:41:18 GMT
COPY file:5de33b5fc08b00635bccf9134a18978dba13e2250aa51838f9969515a3957847 in /etc/yum.repos.d/.      
# Thu, 04 Jun 2026 05:41:18 GMT
CMD ["/bin/bash"]
# Thu, 04 Jun 2026 05:41:18 GMT
COPY file:595171150af68abc798ea385f7988d74b566aa8e84babff137f00b08b2164683 in /usr/share/buildinfo/content-sets.json      
# Thu, 04 Jun 2026 05:41:18 GMT
COPY file:595171150af68abc798ea385f7988d74b566aa8e84babff137f00b08b2164683 in /root/buildinfo/content_manifests/content-sets.json      
# Thu, 04 Jun 2026 05:41:18 GMT
COPY file:145c21488b7dd243862f15c5b9a62cfc5fc22a0ba135ab81b80fd5dfaa1db619 in /usr/share/buildinfo/labels.json      
# Thu, 04 Jun 2026 05:41:18 GMT
COPY file:145c21488b7dd243862f15c5b9a62cfc5fc22a0ba135ab81b80fd5dfaa1db619 in /root/buildinfo/labels.json      
# Thu, 04 Jun 2026 05:41:18 GMT
LABEL "architecture"="s390x" "vcs-type"="git" "vcs-ref"="21e748607cdf3bfe567bea40c2e0c654a3c7766c" "org.opencontainers.image.revision"="21e748607cdf3bfe567bea40c2e0c654a3c7766c" "build-date"="2026-06-04T05:40:37Z" "org.opencontainers.image.created"="2026-06-04T05:40:37Z" "release"="1780550715"org.opencontainers.image.revision=21e748607cdf3bfe567bea40c2e0c654a3c7766c,org.opencontainers.image.created=2026-06-04T05:40:37Z
# Fri, 05 Jun 2026 22:54:39 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 05 Jun 2026 22:54:39 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 05 Jun 2026 22:54:39 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 05 Jun 2026 22:54:39 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en         gnupg2     ;     microdnf clean all # buildkit
# Fri, 05 Jun 2026 22:54:39 GMT
ENV JAVA_VERSION=jdk-17.0.19+10
# Fri, 05 Jun 2026 22:55:33 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='83a52172678ec8975164648654869cb2e71d7c748b47aca94b29bbfa10c18e81';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.19%2B10/OpenJDK17U-jdk_aarch64_linux_hotspot_17.0.19_10.tar.gz';          ;;        ppc64le)          ESUM='c9d8dc52960ff00aa8c321e211cc5284a2151cffdedeac998f5297066cbad245';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.19%2B10/OpenJDK17U-jdk_ppc64le_linux_hotspot_17.0.19_10.tar.gz';          ;;        s390x)          ESUM='00363a5ceda57aa0dee89d20b3f6b2966e3c1f3fb6dcf57e66d2264573d3c63e';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.19%2B10/OpenJDK17U-jdk_s390x_linux_hotspot_17.0.19_10.tar.gz';          ;;        x86_64)          ESUM='d8afc263758141a66e0e3aafc321e783f7016696f4eaea067d340a269037d331';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.19%2B10/OpenJDK17U-jdk_x64_linux_hotspot_17.0.19_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Fri, 05 Jun 2026 22:55:34 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Fri, 05 Jun 2026 22:55:34 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Fri, 05 Jun 2026 22:55:34 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Fri, 05 Jun 2026 22:55:34 GMT
CMD ["jshell"]
# Sat, 06 Jun 2026 00:21:46 GMT
CMD ["gradle"]
# Sat, 06 Jun 2026 00:21:46 GMT
ENV GRADLE_HOME=/opt/gradle
# Sat, 06 Jun 2026 00:21:46 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 101 gradle     && useradd --system --gid gradle --uid 101 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Sat, 06 Jun 2026 00:21:46 GMT
VOLUME [/home/gradle/.gradle]
# Sat, 06 Jun 2026 00:21:46 GMT
WORKDIR /home/gradle
# Sat, 06 Jun 2026 00:21:50 GMT
RUN set -o errexit -o nounset     && microdnf install -y         make         curl-minimal         wget         tar                 findutils                 unzip         which                 git         git-lfs         subversion     && microdnf clean all         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which svn # buildkit
# Sat, 06 Jun 2026 00:21:50 GMT
ENV GRADLE_VERSION=9.5.1
# Sat, 06 Jun 2026 00:21:50 GMT
ARG GRADLE_DOWNLOAD_SHA256=bafc141b619ad6350fd975fc903156dd5c151998cc8b058e8c1044ab5f7b031f
# Sat, 06 Jun 2026 00:21:54 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=bafc141b619ad6350fd975fc903156dd5c151998cc8b058e8c1044ab5f7b031f
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Sat, 06 Jun 2026 00:21:54 GMT
USER gradle
# Sat, 06 Jun 2026 00:21:54 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=bafc141b619ad6350fd975fc903156dd5c151998cc8b058e8c1044ab5f7b031f
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --stacktrace --debug --version # buildkit
# Sat, 06 Jun 2026 00:21:54 GMT
USER root
```

-	Layers:
	-	`sha256:508908cfb0e80bf20878a35fc50b1b96d43933820f4d9e8454cbdb960c52bdb5`  
		Last Modified: Thu, 04 Jun 2026 06:53:41 GMT  
		Size: 34.7 MB (34726577 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6b711f2b1010b3a0bdac6f6c9c90783837f411ad3aff4e3fda9b12ef7924d85`  
		Last Modified: Fri, 05 Jun 2026 22:55:03 GMT  
		Size: 38.1 MB (38139315 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b8f05f9288a57ef06f7f3f51033d2fb9646b4fe43769338c59a3d6767b9f296`  
		Last Modified: Fri, 05 Jun 2026 22:56:03 GMT  
		Size: 135.9 MB (135912350 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:067155490b2468f0f038b9ff7015eb9435d8b0b84ae531a6e9c5a2f9a48befea`  
		Last Modified: Fri, 05 Jun 2026 22:56:00 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3aae35083185c44741fab692da4f101c7f895eb5e62ec6f0c3317737cbccf1e`  
		Last Modified: Fri, 05 Jun 2026 22:56:00 GMT  
		Size: 2.3 KB (2290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89d483806799ee0f3c926bed7234c4c50fafe41f5481403ff2202b5b9be046f1`  
		Last Modified: Sat, 06 Jun 2026 00:22:23 GMT  
		Size: 1.6 KB (1588 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc92552a8e2950b0937fb4a91bda408a6c3b62594e3c331c16f952ff6e0e49ef`  
		Last Modified: Sat, 06 Jun 2026 00:22:25 GMT  
		Size: 42.0 MB (41958888 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ed3ce2fee255cb2bea97bdc7f51d5fd659b7b7e122da4fb4b5971fcb7fd9a02`  
		Last Modified: Sat, 06 Jun 2026 00:22:27 GMT  
		Size: 140.2 MB (140236981 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91c9120fd89756f593b742797aa06a9ee522ddbd4d2bf786eb3a6fd8676ffbbf`  
		Last Modified: Sat, 06 Jun 2026 00:22:23 GMT  
		Size: 376.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:9-jdk17-ubi10` - unknown; unknown

```console
$ docker pull gradle@sha256:4f011569ae933d3ae59edf58a36847bfcd1e3e3a43650d610e6b1fbc8b1644de
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.1 MB (7081843 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d554d5ad86c45c192a5564bc200246b49d3450bc7bb5a46eb295bf5ae9f34d2`

```dockerfile
```

-	Layers:
	-	`sha256:1a0e2f1a336511e5baa89520f7e4434a13be147427a4fb23c3679307d7ffe4da`  
		Last Modified: Sat, 06 Jun 2026 00:22:23 GMT  
		Size: 7.1 MB (7057391 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5c42e6e171314e60e5e4b04aa8e12519ef13b337990b16cdc63fc6bfbc68a55e`  
		Last Modified: Sat, 06 Jun 2026 00:22:23 GMT  
		Size: 24.5 KB (24452 bytes)  
		MIME: application/vnd.in-toto+json
