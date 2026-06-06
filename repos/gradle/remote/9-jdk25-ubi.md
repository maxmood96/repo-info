## `gradle:9-jdk25-ubi`

```console
$ docker pull gradle@sha256:c9740264f5ec422aa26004b2c8e27aa09dfab1963ffcf016563aa23197a7004e
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

### `gradle:9-jdk25-ubi` - linux; amd64

```console
$ docker pull gradle@sha256:0cf91abcf8e5b8150f2a96d9f42c825eb962aab66bf41f0775bfa56de042c34e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **345.3 MB (345311521 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df720dfe9efcd55e7002d1fffa059db071f98f8d073abf9785eab556ddab1f6c`
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
# Fri, 05 Jun 2026 22:42:52 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 05 Jun 2026 22:42:52 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 05 Jun 2026 22:42:52 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 05 Jun 2026 22:42:52 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en         gnupg2     ;     microdnf clean all # buildkit
# Fri, 05 Jun 2026 22:42:52 GMT
ENV JAVA_VERSION=jdk-25.0.3+9
# Fri, 05 Jun 2026 22:43:21 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='3e4287cb98870ba824ed698854bdc27cff984254caf66dd12cc291e7bfdde26b';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.3%2B9/OpenJDK25U-jdk_aarch64_linux_hotspot_25.0.3_9.tar.gz';          ;;        ppc64le)          ESUM='72b0fbb201716ca465ab704ec0fb12971abab3fdde5ae8d03b125a273522cf05';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.3%2B9/OpenJDK25U-jdk_ppc64le_linux_hotspot_25.0.3_9.tar.gz';          ;;        s390x)          ESUM='24b497d10acb6ee706ca30e1c8a929785c250cad54c5c12f1f8f93c3c06a53f7';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.3%2B9/OpenJDK25U-jdk_s390x_linux_hotspot_25.0.3_9.tar.gz';          ;;        x86_64)          ESUM='69264a7a211bf5029830d07bc3370f879769d62ebc5b5488e90c9343a2da0e1f';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.3%2B9/OpenJDK25U-jdk_x64_linux_hotspot_25.0.3_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Fri, 05 Jun 2026 22:43:22 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Fri, 05 Jun 2026 22:43:22 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Fri, 05 Jun 2026 22:43:22 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Fri, 05 Jun 2026 22:43:22 GMT
CMD ["jshell"]
# Sat, 06 Jun 2026 00:15:35 GMT
CMD ["gradle"]
# Sat, 06 Jun 2026 00:15:35 GMT
ENV GRADLE_HOME=/opt/gradle
# Sat, 06 Jun 2026 00:15:35 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 101 gradle     && useradd --system --gid gradle --uid 101 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Sat, 06 Jun 2026 00:15:35 GMT
VOLUME [/home/gradle/.gradle]
# Sat, 06 Jun 2026 00:15:35 GMT
WORKDIR /home/gradle
# Sat, 06 Jun 2026 00:15:38 GMT
RUN set -o errexit -o nounset     && microdnf install -y         make         curl         wget         tar                 findutils                 unzip         which                 git         git-lfs         subversion     && microdnf clean all         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which svn # buildkit
# Sat, 06 Jun 2026 00:15:38 GMT
ENV GRADLE_VERSION=9.5.1
# Sat, 06 Jun 2026 00:15:38 GMT
ARG GRADLE_DOWNLOAD_SHA256=bafc141b619ad6350fd975fc903156dd5c151998cc8b058e8c1044ab5f7b031f
# Sat, 06 Jun 2026 00:15:40 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=bafc141b619ad6350fd975fc903156dd5c151998cc8b058e8c1044ab5f7b031f
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Sat, 06 Jun 2026 00:15:40 GMT
USER gradle
# Sat, 06 Jun 2026 00:15:41 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=bafc141b619ad6350fd975fc903156dd5c151998cc8b058e8c1044ab5f7b031f
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --stacktrace --debug --version # buildkit
# Sat, 06 Jun 2026 00:15:41 GMT
USER root
```

-	Layers:
	-	`sha256:39798aa98bd37b2e4ff77c414dd42bca72e522aa2cb338296f10696a239cb2b2`  
		Last Modified: Thu, 04 Jun 2026 06:53:25 GMT  
		Size: 34.9 MB (34854739 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aafae88de2327d6ae8c0b5b7750f14d9044ddf8345692d9612dab8a0628ccf19`  
		Last Modified: Fri, 05 Jun 2026 22:43:08 GMT  
		Size: 37.8 MB (37760494 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17ec308c2be2817c28a7db8875f5d07fa762af278c8603f2c20c909f206f375c`  
		Last Modified: Fri, 05 Jun 2026 22:43:40 GMT  
		Size: 92.6 MB (92579381 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38b12406fa4d78e8a7b98afe346f407380d541d5daaa762154c7994abea3b6e3`  
		Last Modified: Fri, 05 Jun 2026 22:43:37 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33d673d3ad76bbe183a8f40c09a61f01728144133fdccd98df6d9af307b95dad`  
		Last Modified: Fri, 05 Jun 2026 22:43:37 GMT  
		Size: 2.3 KB (2291 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86f1da7172fdd8d8e83c3cf5706f998fdc2ab6de661e9a4395d226dc2a8877b3`  
		Last Modified: Sat, 06 Jun 2026 00:15:57 GMT  
		Size: 1.6 KB (1592 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:029f23a14091018225c3cbbcfabdd327af0fe71d9021d245f8467058d4159ae1`  
		Last Modified: Sat, 06 Jun 2026 00:15:59 GMT  
		Size: 39.9 MB (39850268 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b76d9b691b7d09f1d77c9049d0dca0a7fc590da0d80d0b5285b9c2a7e221907`  
		Last Modified: Sat, 06 Jun 2026 00:16:02 GMT  
		Size: 140.2 MB (140236984 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92c6445ce3d80970df1ae7889fd910a3a4838024b5be693caa26076d02a85b7f`  
		Last Modified: Sat, 06 Jun 2026 00:15:57 GMT  
		Size: 25.6 KB (25611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:9-jdk25-ubi` - unknown; unknown

```console
$ docker pull gradle@sha256:4abdce8a0a857c10d0d84947247f9f686b579ce857a55e48cf5935918a08f928
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.1 MB (7069735 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f3832552bab35da8b306d62f94a3993e14793b34cb97e21ee5dff85cc42ef0e7`

```dockerfile
```

-	Layers:
	-	`sha256:8c054b32816b9ff6bb58c844f2fc294c68dc7823728d78d00c3436ca1beb4620`  
		Last Modified: Sat, 06 Jun 2026 00:15:58 GMT  
		Size: 7.0 MB (7044726 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c518578d99cf0afa0c4c3cbce2cdeb546dde164f50212be1447f7918944811e1`  
		Last Modified: Sat, 06 Jun 2026 00:15:57 GMT  
		Size: 25.0 KB (25009 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:9-jdk25-ubi` - linux; arm64 variant v8

```console
$ docker pull gradle@sha256:9120c820fa3815bc5502c6d7deb45ce6f214287c98455ba9b9711eaff1e0a786
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **341.9 MB (341854590 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b3304843eb46522e5711a4745b46dfa069bd1d64d3872f02f483b4a136ad705`
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
# Fri, 05 Jun 2026 22:43:18 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 05 Jun 2026 22:43:18 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 05 Jun 2026 22:43:18 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 05 Jun 2026 22:43:18 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en         gnupg2     ;     microdnf clean all # buildkit
# Fri, 05 Jun 2026 22:43:18 GMT
ENV JAVA_VERSION=jdk-25.0.3+9
# Fri, 05 Jun 2026 22:43:48 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='3e4287cb98870ba824ed698854bdc27cff984254caf66dd12cc291e7bfdde26b';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.3%2B9/OpenJDK25U-jdk_aarch64_linux_hotspot_25.0.3_9.tar.gz';          ;;        ppc64le)          ESUM='72b0fbb201716ca465ab704ec0fb12971abab3fdde5ae8d03b125a273522cf05';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.3%2B9/OpenJDK25U-jdk_ppc64le_linux_hotspot_25.0.3_9.tar.gz';          ;;        s390x)          ESUM='24b497d10acb6ee706ca30e1c8a929785c250cad54c5c12f1f8f93c3c06a53f7';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.3%2B9/OpenJDK25U-jdk_s390x_linux_hotspot_25.0.3_9.tar.gz';          ;;        x86_64)          ESUM='69264a7a211bf5029830d07bc3370f879769d62ebc5b5488e90c9343a2da0e1f';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.3%2B9/OpenJDK25U-jdk_x64_linux_hotspot_25.0.3_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Fri, 05 Jun 2026 22:43:50 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Fri, 05 Jun 2026 22:43:50 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Fri, 05 Jun 2026 22:43:50 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Fri, 05 Jun 2026 22:43:50 GMT
CMD ["jshell"]
# Sat, 06 Jun 2026 00:16:07 GMT
CMD ["gradle"]
# Sat, 06 Jun 2026 00:16:07 GMT
ENV GRADLE_HOME=/opt/gradle
# Sat, 06 Jun 2026 00:16:07 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 101 gradle     && useradd --system --gid gradle --uid 101 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Sat, 06 Jun 2026 00:16:07 GMT
VOLUME [/home/gradle/.gradle]
# Sat, 06 Jun 2026 00:16:07 GMT
WORKDIR /home/gradle
# Sat, 06 Jun 2026 00:16:11 GMT
RUN set -o errexit -o nounset     && microdnf install -y         make         curl         wget         tar                 findutils                 unzip         which                 git         git-lfs         subversion     && microdnf clean all         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which svn # buildkit
# Sat, 06 Jun 2026 00:16:11 GMT
ENV GRADLE_VERSION=9.5.1
# Sat, 06 Jun 2026 00:16:11 GMT
ARG GRADLE_DOWNLOAD_SHA256=bafc141b619ad6350fd975fc903156dd5c151998cc8b058e8c1044ab5f7b031f
# Sat, 06 Jun 2026 00:16:13 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=bafc141b619ad6350fd975fc903156dd5c151998cc8b058e8c1044ab5f7b031f
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Sat, 06 Jun 2026 00:16:13 GMT
USER gradle
# Sat, 06 Jun 2026 00:16:14 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=bafc141b619ad6350fd975fc903156dd5c151998cc8b058e8c1044ab5f7b031f
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --stacktrace --debug --version # buildkit
# Sat, 06 Jun 2026 00:16:14 GMT
USER root
```

-	Layers:
	-	`sha256:ebf3c43a43d516c400d687e8a210bad7522ec8a8a6c34ae1d72a70004f06bc71`  
		Last Modified: Thu, 04 Jun 2026 06:53:34 GMT  
		Size: 33.0 MB (33039715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fc4d425caa67df0867ba8b5668aaf92b64f8d1e58cfe5c582525338c6cf5da3`  
		Last Modified: Fri, 05 Jun 2026 22:43:35 GMT  
		Size: 37.7 MB (37686371 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79cce4f38a9d6cb07f88c887319bbb81b030c6cc6ac9d3d583ca651422563aa4`  
		Last Modified: Fri, 05 Jun 2026 22:44:09 GMT  
		Size: 91.5 MB (91548922 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72b9416a89ff62c9ce6bb8aa12b94aefa60c1c43126c866b92193404d374b3bb`  
		Last Modified: Fri, 05 Jun 2026 22:44:06 GMT  
		Size: 130.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6be6d85c5fa8583ec8da3c5c15eb5e332469b4d36b379a2ff9c0427162392f5f`  
		Last Modified: Fri, 05 Jun 2026 22:44:06 GMT  
		Size: 2.3 KB (2290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:652001977e56d277cd7fecc20c11e846d3805e5cb5a892bcbab37f59311cb9cd`  
		Last Modified: Sat, 06 Jun 2026 00:16:33 GMT  
		Size: 1.6 KB (1587 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e7b944c86d7d8a28d3340bb50eb412a45347b9a61c65e645c30f768a91901fb`  
		Last Modified: Sat, 06 Jun 2026 00:16:35 GMT  
		Size: 39.3 MB (39309256 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:808433891d34ae18e3baded8cd0f50c3fe74446e503058e486830e039dae14c3`  
		Last Modified: Sat, 06 Jun 2026 00:16:38 GMT  
		Size: 140.2 MB (140236951 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f81d9c89d80c92d775f76e1a5652a0dbd91f3664f6f8e529c4e396a91918c298`  
		Last Modified: Sat, 06 Jun 2026 00:16:33 GMT  
		Size: 29.3 KB (29336 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:9-jdk25-ubi` - unknown; unknown

```console
$ docker pull gradle@sha256:a252bbc8725e4ce170028c457fe00b985e70bc51b28cd1c8892532c9dac11b7f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.1 MB (7068233 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f44fbee5db8454589ccb4e067e306a458d0f9478b7af024eac7ab4aefe5280ca`

```dockerfile
```

-	Layers:
	-	`sha256:79ecc2c45becf0792d46ad95f0b84c1cf8b9dc2a6c2ac39c4a69d63b841adf3b`  
		Last Modified: Sat, 06 Jun 2026 00:16:33 GMT  
		Size: 7.0 MB (7043003 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c10fca862d9f85a9050fc575f573423db81e3252afa72ad69a8c6c1a9b3e5896`  
		Last Modified: Sat, 06 Jun 2026 00:16:33 GMT  
		Size: 25.2 KB (25230 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:9-jdk25-ubi` - linux; ppc64le

```console
$ docker pull gradle@sha256:90bebd77ec3889196b1e07c7ef8e934d2f453e20e0af3b928f9c2494621761ef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **352.3 MB (352300656 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:caddb4a6f6a0bc9f7bf02e8b822c82f665b3047e2d8d24a297b1d2c0d7ae5fa0`
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
ENV JAVA_VERSION=jdk-25.0.3+9
# Fri, 05 Jun 2026 23:21:59 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='3e4287cb98870ba824ed698854bdc27cff984254caf66dd12cc291e7bfdde26b';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.3%2B9/OpenJDK25U-jdk_aarch64_linux_hotspot_25.0.3_9.tar.gz';          ;;        ppc64le)          ESUM='72b0fbb201716ca465ab704ec0fb12971abab3fdde5ae8d03b125a273522cf05';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.3%2B9/OpenJDK25U-jdk_ppc64le_linux_hotspot_25.0.3_9.tar.gz';          ;;        s390x)          ESUM='24b497d10acb6ee706ca30e1c8a929785c250cad54c5c12f1f8f93c3c06a53f7';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.3%2B9/OpenJDK25U-jdk_s390x_linux_hotspot_25.0.3_9.tar.gz';          ;;        x86_64)          ESUM='69264a7a211bf5029830d07bc3370f879769d62ebc5b5488e90c9343a2da0e1f';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.3%2B9/OpenJDK25U-jdk_x64_linux_hotspot_25.0.3_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Fri, 05 Jun 2026 23:22:03 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Fri, 05 Jun 2026 23:22:04 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Fri, 05 Jun 2026 23:22:04 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Fri, 05 Jun 2026 23:22:04 GMT
CMD ["jshell"]
# Sat, 06 Jun 2026 00:37:10 GMT
CMD ["gradle"]
# Sat, 06 Jun 2026 00:37:10 GMT
ENV GRADLE_HOME=/opt/gradle
# Sat, 06 Jun 2026 00:37:10 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 101 gradle     && useradd --system --gid gradle --uid 101 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Sat, 06 Jun 2026 00:37:10 GMT
VOLUME [/home/gradle/.gradle]
# Sat, 06 Jun 2026 00:37:10 GMT
WORKDIR /home/gradle
# Sat, 06 Jun 2026 00:37:25 GMT
RUN set -o errexit -o nounset     && microdnf install -y         make         curl         wget         tar                 findutils                 unzip         which                 git         git-lfs         subversion     && microdnf clean all         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which svn # buildkit
# Sat, 06 Jun 2026 00:37:25 GMT
ENV GRADLE_VERSION=9.5.1
# Sat, 06 Jun 2026 00:37:25 GMT
ARG GRADLE_DOWNLOAD_SHA256=bafc141b619ad6350fd975fc903156dd5c151998cc8b058e8c1044ab5f7b031f
# Sat, 06 Jun 2026 00:37:30 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=bafc141b619ad6350fd975fc903156dd5c151998cc8b058e8c1044ab5f7b031f
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Sat, 06 Jun 2026 00:37:30 GMT
USER gradle
# Sat, 06 Jun 2026 00:37:32 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=bafc141b619ad6350fd975fc903156dd5c151998cc8b058e8c1044ab5f7b031f
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --stacktrace --debug --version # buildkit
# Sat, 06 Jun 2026 00:37:32 GMT
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
	-	`sha256:f466d1d548c4da503bf1394e6071455bf2fb551c32e52958d94fe011af608e7e`  
		Last Modified: Fri, 05 Jun 2026 23:22:38 GMT  
		Size: 91.9 MB (91912899 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac2c8809162032d2056f22b37ea491e782503f14d3ac30d926d39ad60b3c61c9`  
		Last Modified: Fri, 05 Jun 2026 23:22:36 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c44cdc1c452835a0aee1af8b76ae62414a538277e22c885626383819ae80877`  
		Last Modified: Fri, 05 Jun 2026 23:22:36 GMT  
		Size: 2.3 KB (2290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0769d4ac76b01bf17eeda795d18e63e4ede3adc9092cb25ea1756cf36342ca7e`  
		Last Modified: Sat, 06 Jun 2026 00:38:08 GMT  
		Size: 1.6 KB (1592 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08c8951cd6ca693110413609e68c00ffe05e65ddb3f4af622ae9fd11acdfe291`  
		Last Modified: Sat, 06 Jun 2026 00:38:10 GMT  
		Size: 41.6 MB (41615117 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:561d6cfdd35fcc455a093de5dfcc1ae2e73861b207b40b4896b1efb238fe14e3`  
		Last Modified: Sat, 06 Jun 2026 00:38:12 GMT  
		Size: 140.2 MB (140236992 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21285a46699dd023f5ea8e0d823b434f5ca0f42523845ba8bcb942a118ecdf9f`  
		Last Modified: Sat, 06 Jun 2026 00:38:08 GMT  
		Size: 381.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:9-jdk25-ubi` - unknown; unknown

```console
$ docker pull gradle@sha256:c60e7ac547b397495a6804d0b3706a0280494188469ee30c0846f5baa4adb893
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 MB (7044561 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9562ae92ec315fc21252a3e150a631af73b39e1a9a9e2c3f267a8a5b5806cbe0`

```dockerfile
```

-	Layers:
	-	`sha256:ff34c46ea06760145801558979a1597692984ebff143c5e36730d4177fe24272`  
		Last Modified: Sat, 06 Jun 2026 00:38:08 GMT  
		Size: 7.0 MB (7019468 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:47ab485975d747d27c0b1177f77a8ba9538944d1133acc620b5e2b34864a7347`  
		Last Modified: Sat, 06 Jun 2026 00:38:07 GMT  
		Size: 25.1 KB (25093 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:9-jdk25-ubi` - linux; s390x

```console
$ docker pull gradle@sha256:f5da13e695e9d1c10a1113b584f17608ee3f72326a0f5babb1fcb0ea25aa5b03
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **343.5 MB (343488269 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f2e22449efb7cff4a0796e98fbc8ce3ad81d3585a814429c2eed139f86b70df2`
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
ENV JAVA_VERSION=jdk-25.0.3+9
# Fri, 05 Jun 2026 22:57:09 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='3e4287cb98870ba824ed698854bdc27cff984254caf66dd12cc291e7bfdde26b';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.3%2B9/OpenJDK25U-jdk_aarch64_linux_hotspot_25.0.3_9.tar.gz';          ;;        ppc64le)          ESUM='72b0fbb201716ca465ab704ec0fb12971abab3fdde5ae8d03b125a273522cf05';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.3%2B9/OpenJDK25U-jdk_ppc64le_linux_hotspot_25.0.3_9.tar.gz';          ;;        s390x)          ESUM='24b497d10acb6ee706ca30e1c8a929785c250cad54c5c12f1f8f93c3c06a53f7';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.3%2B9/OpenJDK25U-jdk_s390x_linux_hotspot_25.0.3_9.tar.gz';          ;;        x86_64)          ESUM='69264a7a211bf5029830d07bc3370f879769d62ebc5b5488e90c9343a2da0e1f';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.3%2B9/OpenJDK25U-jdk_x64_linux_hotspot_25.0.3_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Fri, 05 Jun 2026 22:57:10 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Fri, 05 Jun 2026 22:57:10 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Fri, 05 Jun 2026 22:57:10 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Fri, 05 Jun 2026 22:57:10 GMT
CMD ["jshell"]
# Sat, 06 Jun 2026 00:21:07 GMT
CMD ["gradle"]
# Sat, 06 Jun 2026 00:21:07 GMT
ENV GRADLE_HOME=/opt/gradle
# Sat, 06 Jun 2026 00:21:07 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 101 gradle     && useradd --system --gid gradle --uid 101 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Sat, 06 Jun 2026 00:21:07 GMT
VOLUME [/home/gradle/.gradle]
# Sat, 06 Jun 2026 00:21:07 GMT
WORKDIR /home/gradle
# Sat, 06 Jun 2026 00:21:12 GMT
RUN set -o errexit -o nounset     && microdnf install -y         make         curl         wget         tar                 findutils                 unzip         which                 git         git-lfs         subversion     && microdnf clean all         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which svn # buildkit
# Sat, 06 Jun 2026 00:21:12 GMT
ENV GRADLE_VERSION=9.5.1
# Sat, 06 Jun 2026 00:21:12 GMT
ARG GRADLE_DOWNLOAD_SHA256=bafc141b619ad6350fd975fc903156dd5c151998cc8b058e8c1044ab5f7b031f
# Sat, 06 Jun 2026 00:21:16 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=bafc141b619ad6350fd975fc903156dd5c151998cc8b058e8c1044ab5f7b031f
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Sat, 06 Jun 2026 00:21:16 GMT
USER gradle
# Sat, 06 Jun 2026 00:21:16 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=bafc141b619ad6350fd975fc903156dd5c151998cc8b058e8c1044ab5f7b031f
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --stacktrace --debug --version # buildkit
# Sat, 06 Jun 2026 00:21:16 GMT
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
	-	`sha256:98d5782ab9fe562fafbbdfb885d7de05c83043f428f3b137aec0084b6fc315b0`  
		Last Modified: Fri, 05 Jun 2026 22:57:38 GMT  
		Size: 88.4 MB (88421715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44ca4cd309b9c6878632680539c95cee87606ff706331056cf07e470a37b0b3f`  
		Last Modified: Fri, 05 Jun 2026 22:57:36 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a69a3a1b0eeca8e61b33e879fd43b87355e6f875104f31d6e685803591849bf`  
		Last Modified: Fri, 05 Jun 2026 22:57:36 GMT  
		Size: 2.3 KB (2287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:248d37a3bab493ce05eafdef85bede7d1b4561f3ee360c5ece23871cad443ebe`  
		Last Modified: Sat, 06 Jun 2026 00:21:45 GMT  
		Size: 1.6 KB (1587 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0aa8b76a2105228145afbe5e3ae21a89c16cb17638c1fb9b130d1982f30342ee`  
		Last Modified: Sat, 06 Jun 2026 00:21:46 GMT  
		Size: 42.0 MB (41959266 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:feca502fd5d3365e7cffe67fbdac671e53cc498ef3bd9eee4a73ea9b21dcdfba`  
		Last Modified: Sat, 06 Jun 2026 00:21:48 GMT  
		Size: 140.2 MB (140236989 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11e6d7d10be20d7080b68f332020a829679d1148c8985f657e774e053f802d21`  
		Last Modified: Sat, 06 Jun 2026 00:21:45 GMT  
		Size: 372.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:9-jdk25-ubi` - unknown; unknown

```console
$ docker pull gradle@sha256:ffb5a10fd8f5f89b578d494a9418894117a39efb473f26a764cbad99b3802782
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 MB (7034941 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a6599e8763f857dd71f452d74ed358af7b5c8b44424172654466e10935667578`

```dockerfile
```

-	Layers:
	-	`sha256:f1a5b86241bfe2d515dfc20ce97a28862797960bd4ae173ef1251434e4d5779e`  
		Last Modified: Sat, 06 Jun 2026 00:21:46 GMT  
		Size: 7.0 MB (7009935 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1417a3290214a0d7cece6f0f37915dc52f600270046ff89e8a2d289656053036`  
		Last Modified: Sat, 06 Jun 2026 00:21:45 GMT  
		Size: 25.0 KB (25006 bytes)  
		MIME: application/vnd.in-toto+json
