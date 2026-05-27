## `gradle:ubi10`

```console
$ docker pull gradle@sha256:f5826552b9a6c17990cd5ff207bdf622ae88d11888be2df2ee619eaa7a84cce1
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

### `gradle:ubi10` - linux; amd64

```console
$ docker pull gradle@sha256:d873148df3621d2825c506aa8ca568a88c91c1878da84e376f9d5668475be48d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **353.4 MB (353429345 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9d0a028c5111506b925671fbbeb0cb8fd76ada9dd9c39b8fd4cb2e0e4a77b3bb`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["gradle"]`

```dockerfile
# Tue, 26 May 2026 09:52:44 GMT
LABEL maintainer="Red Hat, Inc."
# Tue, 26 May 2026 09:52:44 GMT
LABEL vendor="Red Hat, Inc."
# Tue, 26 May 2026 09:52:44 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Tue, 26 May 2026 09:52:44 GMT
LABEL com.redhat.component="ubi10-minimal-container"       name="ubi10/ubi-minimal"       version="10.1"       cpe="cpe:/o:redhat:enterprise_linux:10.1"       distribution-scope="public"
# Tue, 26 May 2026 09:52:44 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Tue, 26 May 2026 09:52:44 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 10."
# Tue, 26 May 2026 09:52:44 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Tue, 26 May 2026 09:52:44 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Tue, 26 May 2026 09:52:45 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 10 Minimal"
# Tue, 26 May 2026 09:52:45 GMT
LABEL io.openshift.expose-services=""
# Tue, 26 May 2026 09:52:45 GMT
LABEL io.openshift.tags="minimal rhel10"
# Tue, 26 May 2026 09:52:45 GMT
ENV container oci
# Tue, 26 May 2026 09:52:46 GMT
COPY dir:4a65961322c03a42263a9993a9e455b03f91a19ddc042f14a91b2092bee12ade in /      
# Tue, 26 May 2026 09:52:46 GMT
COPY file:5de33b5fc08b00635bccf9134a18978dba13e2250aa51838f9969515a3957847 in /etc/yum.repos.d/.      
# Tue, 26 May 2026 09:52:46 GMT
CMD ["/bin/bash"]
# Tue, 26 May 2026 09:52:46 GMT
COPY file:595171150af68abc798ea385f7988d74b566aa8e84babff137f00b08b2164683 in /usr/share/buildinfo/content-sets.json      
# Tue, 26 May 2026 09:52:47 GMT
COPY file:595171150af68abc798ea385f7988d74b566aa8e84babff137f00b08b2164683 in /root/buildinfo/content_manifests/content-sets.json      
# Tue, 26 May 2026 09:52:47 GMT
COPY file:3ad71f7fdda6857fd6a2d3e0ee5ab780c0c840fe960653943407106cbf070684 in /usr/share/buildinfo/labels.json      
# Tue, 26 May 2026 09:52:47 GMT
COPY file:3ad71f7fdda6857fd6a2d3e0ee5ab780c0c840fe960653943407106cbf070684 in /root/buildinfo/labels.json      
# Tue, 26 May 2026 09:52:47 GMT
LABEL "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="28a4d5c7cdb1969ee63337adb47fcb350a380874" "org.opencontainers.image.revision"="28a4d5c7cdb1969ee63337adb47fcb350a380874" "build-date"="2026-05-26T09:52:24Z" "org.opencontainers.image.created"="2026-05-26T09:52:24Z" "release"="1779788807"org.opencontainers.image.revision=28a4d5c7cdb1969ee63337adb47fcb350a380874,org.opencontainers.image.created=2026-05-26T09:52:24Z
# Tue, 26 May 2026 23:09:53 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 26 May 2026 23:09:53 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 26 May 2026 23:09:53 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 26 May 2026 23:09:53 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en         gnupg2     ;     microdnf clean all # buildkit
# Tue, 26 May 2026 23:09:53 GMT
ENV JAVA_VERSION=jdk-25.0.3+9
# Tue, 26 May 2026 23:10:48 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='3e4287cb98870ba824ed698854bdc27cff984254caf66dd12cc291e7bfdde26b';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.3%2B9/OpenJDK25U-jdk_aarch64_linux_hotspot_25.0.3_9.tar.gz';          ;;        ppc64le)          ESUM='72b0fbb201716ca465ab704ec0fb12971abab3fdde5ae8d03b125a273522cf05';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.3%2B9/OpenJDK25U-jdk_ppc64le_linux_hotspot_25.0.3_9.tar.gz';          ;;        s390x)          ESUM='24b497d10acb6ee706ca30e1c8a929785c250cad54c5c12f1f8f93c3c06a53f7';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.3%2B9/OpenJDK25U-jdk_s390x_linux_hotspot_25.0.3_9.tar.gz';          ;;        x86_64)          ESUM='69264a7a211bf5029830d07bc3370f879769d62ebc5b5488e90c9343a2da0e1f';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.3%2B9/OpenJDK25U-jdk_x64_linux_hotspot_25.0.3_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Tue, 26 May 2026 23:10:49 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 26 May 2026 23:10:49 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 26 May 2026 23:10:49 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 26 May 2026 23:10:49 GMT
CMD ["jshell"]
# Wed, 27 May 2026 00:09:39 GMT
CMD ["gradle"]
# Wed, 27 May 2026 00:09:39 GMT
ENV GRADLE_HOME=/opt/gradle
# Wed, 27 May 2026 00:09:39 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 101 gradle     && useradd --system --gid gradle --uid 101 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Wed, 27 May 2026 00:09:39 GMT
VOLUME [/home/gradle/.gradle]
# Wed, 27 May 2026 00:09:39 GMT
WORKDIR /home/gradle
# Wed, 27 May 2026 00:09:43 GMT
RUN set -o errexit -o nounset     && microdnf install -y         make         curl         wget         tar                 findutils                 unzip         which                 git         git-lfs         subversion     && microdnf clean all         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which svn # buildkit
# Wed, 27 May 2026 00:09:43 GMT
ENV GRADLE_VERSION=9.5.1
# Wed, 27 May 2026 00:09:43 GMT
ARG GRADLE_DOWNLOAD_SHA256=bafc141b619ad6350fd975fc903156dd5c151998cc8b058e8c1044ab5f7b031f
# Wed, 27 May 2026 00:09:46 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=bafc141b619ad6350fd975fc903156dd5c151998cc8b058e8c1044ab5f7b031f
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Wed, 27 May 2026 00:09:46 GMT
USER gradle
# Wed, 27 May 2026 00:09:46 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=bafc141b619ad6350fd975fc903156dd5c151998cc8b058e8c1044ab5f7b031f
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --stacktrace --debug --version # buildkit
# Wed, 27 May 2026 00:09:46 GMT
USER root
```

-	Layers:
	-	`sha256:368dae9e745ec994e59731b33513a5334145ab500bb4162a1597ced6ca7d2dd0`  
		Last Modified: Tue, 26 May 2026 11:30:57 GMT  
		Size: 34.6 MB (34624420 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2bd923dc421fa93848bf3fcd2b19fe2f94d0874b4d499b1fd92e8662fe320af`  
		Last Modified: Tue, 26 May 2026 23:10:08 GMT  
		Size: 28.9 MB (28924970 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ba96a834e39f1b206b9c792b9c19b278275c4978e8d1495e5f3420ca557abfa`  
		Last Modified: Tue, 26 May 2026 23:11:06 GMT  
		Size: 92.6 MB (92579378 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c243ef86ca970077e72d81f25799abae1daac6ef319fa7803255cfa32d16055c`  
		Last Modified: Tue, 26 May 2026 23:11:03 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26da59f03f293200cdc4ea499b527e74cefc987306a7440c89ca96f67ae0143f`  
		Last Modified: Tue, 26 May 2026 23:11:03 GMT  
		Size: 2.3 KB (2291 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24a39a9326155b0a90e42f344e6cd88cb70fc1f8112ecf8022e37d2006c87a7b`  
		Last Modified: Wed, 27 May 2026 00:10:05 GMT  
		Size: 1.4 KB (1449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9773237b4d3876367aebc740ee937d5f0a937d7029417facf2d033fa0d70321`  
		Last Modified: Wed, 27 May 2026 00:10:07 GMT  
		Size: 57.0 MB (57034085 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9361628f24c044754346d33a9800fe7cc11fb46a5bb980f672cc8a381cb9cb32`  
		Last Modified: Wed, 27 May 2026 00:10:09 GMT  
		Size: 140.2 MB (140236985 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7475a66d1413ddafa39b5e41619e95bcb4eaa28868501070a38cdaf5e512da9f`  
		Last Modified: Wed, 27 May 2026 00:10:05 GMT  
		Size: 25.6 KB (25607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:ubi10` - unknown; unknown

```console
$ docker pull gradle@sha256:0c3c0b398e94ca3e8959da282d4739d2773fed68aa49f7bb48e30dc0ce631a9f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.1 MB (7075624 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1173bec11b8b1a3008a7d515a77ca8fe2d5d434c1406702eb46184ea3784a103`

```dockerfile
```

-	Layers:
	-	`sha256:daa63c18c7b261cf6209174dc6c9779f4d8a22cbf73b96352cccbddc1c885704`  
		Last Modified: Wed, 27 May 2026 00:10:05 GMT  
		Size: 7.1 MB (7050616 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6d1f7f729cc82337ce378136754243e513d7b5a22d3b74d674e0e0153f5ee673`  
		Last Modified: Wed, 27 May 2026 00:10:04 GMT  
		Size: 25.0 KB (25008 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:ubi10` - linux; arm64 variant v8

```console
$ docker pull gradle@sha256:2a5eba44bc6a3d0b682d5bfc30f6fec513b6a7a9b5d3b8eb2db869332a1968e5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **349.0 MB (348996937 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cfc6eebd8c9315d9a7358276a785abee28b01331bfbcb83fd38d15b22139aee9`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["gradle"]`

```dockerfile
# Tue, 26 May 2026 09:56:13 GMT
LABEL maintainer="Red Hat, Inc."
# Tue, 26 May 2026 09:56:13 GMT
LABEL vendor="Red Hat, Inc."
# Tue, 26 May 2026 09:56:13 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Tue, 26 May 2026 09:56:13 GMT
LABEL com.redhat.component="ubi10-minimal-container"       name="ubi10/ubi-minimal"       version="10.1"       cpe="cpe:/o:redhat:enterprise_linux:10.1"       distribution-scope="public"
# Tue, 26 May 2026 09:56:13 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Tue, 26 May 2026 09:56:13 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 10."
# Tue, 26 May 2026 09:56:13 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Tue, 26 May 2026 09:56:13 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Tue, 26 May 2026 09:56:13 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 10 Minimal"
# Tue, 26 May 2026 09:56:13 GMT
LABEL io.openshift.expose-services=""
# Tue, 26 May 2026 09:56:13 GMT
LABEL io.openshift.tags="minimal rhel10"
# Tue, 26 May 2026 09:56:13 GMT
ENV container oci
# Tue, 26 May 2026 09:56:14 GMT
COPY dir:ae54dc874bd5ff821c9cac1615bdf50508b14bc07c449a11310a695d880fa906 in /      
# Tue, 26 May 2026 09:56:14 GMT
COPY file:5de33b5fc08b00635bccf9134a18978dba13e2250aa51838f9969515a3957847 in /etc/yum.repos.d/.      
# Tue, 26 May 2026 09:56:14 GMT
CMD ["/bin/bash"]
# Tue, 26 May 2026 09:56:14 GMT
COPY file:595171150af68abc798ea385f7988d74b566aa8e84babff137f00b08b2164683 in /usr/share/buildinfo/content-sets.json      
# Tue, 26 May 2026 09:56:14 GMT
COPY file:595171150af68abc798ea385f7988d74b566aa8e84babff137f00b08b2164683 in /root/buildinfo/content_manifests/content-sets.json      
# Tue, 26 May 2026 09:56:15 GMT
COPY file:cbda7134a1becb5efcab0aac781af893c81e3d1aab44f2af20045a4a249708c1 in /usr/share/buildinfo/labels.json      
# Tue, 26 May 2026 09:56:15 GMT
COPY file:cbda7134a1becb5efcab0aac781af893c81e3d1aab44f2af20045a4a249708c1 in /root/buildinfo/labels.json      
# Tue, 26 May 2026 09:56:15 GMT
LABEL "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="28a4d5c7cdb1969ee63337adb47fcb350a380874" "org.opencontainers.image.revision"="28a4d5c7cdb1969ee63337adb47fcb350a380874" "build-date"="2026-05-26T09:55:58Z" "org.opencontainers.image.created"="2026-05-26T09:55:58Z" "release"="1779788807"org.opencontainers.image.revision=28a4d5c7cdb1969ee63337adb47fcb350a380874,org.opencontainers.image.created=2026-05-26T09:55:58Z
# Tue, 26 May 2026 23:09:43 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 26 May 2026 23:09:43 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 26 May 2026 23:09:43 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 26 May 2026 23:09:43 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en         gnupg2     ;     microdnf clean all # buildkit
# Tue, 26 May 2026 23:09:43 GMT
ENV JAVA_VERSION=jdk-25.0.3+9
# Tue, 26 May 2026 23:10:23 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='3e4287cb98870ba824ed698854bdc27cff984254caf66dd12cc291e7bfdde26b';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.3%2B9/OpenJDK25U-jdk_aarch64_linux_hotspot_25.0.3_9.tar.gz';          ;;        ppc64le)          ESUM='72b0fbb201716ca465ab704ec0fb12971abab3fdde5ae8d03b125a273522cf05';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.3%2B9/OpenJDK25U-jdk_ppc64le_linux_hotspot_25.0.3_9.tar.gz';          ;;        s390x)          ESUM='24b497d10acb6ee706ca30e1c8a929785c250cad54c5c12f1f8f93c3c06a53f7';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.3%2B9/OpenJDK25U-jdk_s390x_linux_hotspot_25.0.3_9.tar.gz';          ;;        x86_64)          ESUM='69264a7a211bf5029830d07bc3370f879769d62ebc5b5488e90c9343a2da0e1f';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.3%2B9/OpenJDK25U-jdk_x64_linux_hotspot_25.0.3_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Tue, 26 May 2026 23:10:25 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 26 May 2026 23:10:25 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 26 May 2026 23:10:25 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 26 May 2026 23:10:25 GMT
CMD ["jshell"]
# Wed, 27 May 2026 00:09:19 GMT
CMD ["gradle"]
# Wed, 27 May 2026 00:09:19 GMT
ENV GRADLE_HOME=/opt/gradle
# Wed, 27 May 2026 00:09:19 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 101 gradle     && useradd --system --gid gradle --uid 101 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Wed, 27 May 2026 00:09:19 GMT
VOLUME [/home/gradle/.gradle]
# Wed, 27 May 2026 00:09:19 GMT
WORKDIR /home/gradle
# Wed, 27 May 2026 00:09:28 GMT
RUN set -o errexit -o nounset     && microdnf install -y         make         curl         wget         tar                 findutils                 unzip         which                 git         git-lfs         subversion     && microdnf clean all         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which svn # buildkit
# Wed, 27 May 2026 00:09:28 GMT
ENV GRADLE_VERSION=9.5.1
# Wed, 27 May 2026 00:09:28 GMT
ARG GRADLE_DOWNLOAD_SHA256=bafc141b619ad6350fd975fc903156dd5c151998cc8b058e8c1044ab5f7b031f
# Wed, 27 May 2026 00:09:32 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=bafc141b619ad6350fd975fc903156dd5c151998cc8b058e8c1044ab5f7b031f
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Wed, 27 May 2026 00:09:32 GMT
USER gradle
# Wed, 27 May 2026 00:09:32 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=bafc141b619ad6350fd975fc903156dd5c151998cc8b058e8c1044ab5f7b031f
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --stacktrace --debug --version # buildkit
# Wed, 27 May 2026 00:09:32 GMT
USER root
```

-	Layers:
	-	`sha256:d44582f6016d5b17ffe3577358bcbf1bf84edfe2aba6b73b6461e6631e0a4bc7`  
		Last Modified: Tue, 26 May 2026 11:41:50 GMT  
		Size: 32.7 MB (32711602 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34c1df6c230f9d35da82702251db2c1f7d008413743e0abf5a54a62a8f4d276a`  
		Last Modified: Tue, 26 May 2026 23:10:08 GMT  
		Size: 28.3 MB (28340639 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00745369746deb246d27f8a70ad0644fa1c2866e1cb371da5d63e9c92ac6ce39`  
		Last Modified: Tue, 26 May 2026 23:10:45 GMT  
		Size: 91.5 MB (91548890 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a76bf23b050f9230df26dc96badf721eabfc33286513f54d638d89ccc2364e73`  
		Last Modified: Tue, 26 May 2026 23:10:41 GMT  
		Size: 130.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:339749c5b1dacc298eccc71697176da567ef6e7bc1ec427f7f0446cd08276aff`  
		Last Modified: Tue, 26 May 2026 23:10:41 GMT  
		Size: 2.3 KB (2291 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b592766737c345a26014327552ed72580ab0a6c255b98329a5c86b31810bcb04`  
		Last Modified: Wed, 27 May 2026 00:09:53 GMT  
		Size: 1.5 KB (1451 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12a0ae6b292431a29298a48bd8d6dfbd1d0cde50e36cf006420be80be0e04222`  
		Last Modified: Wed, 27 May 2026 00:09:58 GMT  
		Size: 56.1 MB (56125616 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9d5d07aa567890a46d24d89a72de6d55e92d423eb43c1a8eb3f203fb30ab04d`  
		Last Modified: Wed, 27 May 2026 00:09:57 GMT  
		Size: 140.2 MB (140236949 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:108afc2603fb8c94aa5b80afd7cf1fd1375c62b6fc0a29f9a8c888f4b0621cc4`  
		Last Modified: Wed, 27 May 2026 00:09:53 GMT  
		Size: 29.3 KB (29337 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:ubi10` - unknown; unknown

```console
$ docker pull gradle@sha256:bdc6947a4e768aa08ea69c169b8e39b2c52e4209483e900aedc69dbe90600bd2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.1 MB (7074123 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c24d8fb847b7963e6186786ba1597d22924df11f49ee6191eadff8f45ea03f5`

```dockerfile
```

-	Layers:
	-	`sha256:52ca8906cac15e49e17cc1a5a613b175ede041a6f92661748fffd0820358ac94`  
		Last Modified: Wed, 27 May 2026 00:09:53 GMT  
		Size: 7.0 MB (7048893 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:24211c8828cda2124f704bb97412941fa1bd28af300cab0587e10877a05cf6fc`  
		Last Modified: Wed, 27 May 2026 00:09:53 GMT  
		Size: 25.2 KB (25230 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:ubi10` - linux; ppc64le

```console
$ docker pull gradle@sha256:a5c8f07ef045a430874fb6ade4bdbe6a6e79cc7550a2eb940918fc842d7ed5f5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **362.4 MB (362351325 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af162414151b86734a19314d544dbd72d2de9e53660a56cab79b114f508911a2`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["gradle"]`

```dockerfile
# Tue, 26 May 2026 10:05:34 GMT
LABEL maintainer="Red Hat, Inc."
# Tue, 26 May 2026 10:05:34 GMT
LABEL vendor="Red Hat, Inc."
# Tue, 26 May 2026 10:05:34 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Tue, 26 May 2026 10:05:34 GMT
LABEL com.redhat.component="ubi10-minimal-container"       name="ubi10/ubi-minimal"       version="10.1"       cpe="cpe:/o:redhat:enterprise_linux:10.1"       distribution-scope="public"
# Tue, 26 May 2026 10:05:35 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Tue, 26 May 2026 10:05:35 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 10."
# Tue, 26 May 2026 10:05:35 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Tue, 26 May 2026 10:05:35 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Tue, 26 May 2026 10:05:35 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 10 Minimal"
# Tue, 26 May 2026 10:05:35 GMT
LABEL io.openshift.expose-services=""
# Tue, 26 May 2026 10:05:35 GMT
LABEL io.openshift.tags="minimal rhel10"
# Tue, 26 May 2026 10:05:35 GMT
ENV container oci
# Tue, 26 May 2026 10:05:37 GMT
COPY dir:d4fda96d22b28f66ff1bcd2a6fa4e35fa9ad60695678918f055282f9b91f573c in /      
# Tue, 26 May 2026 10:05:37 GMT
COPY file:5de33b5fc08b00635bccf9134a18978dba13e2250aa51838f9969515a3957847 in /etc/yum.repos.d/.      
# Tue, 26 May 2026 10:05:37 GMT
CMD ["/bin/bash"]
# Tue, 26 May 2026 10:05:37 GMT
COPY file:595171150af68abc798ea385f7988d74b566aa8e84babff137f00b08b2164683 in /usr/share/buildinfo/content-sets.json      
# Tue, 26 May 2026 10:05:37 GMT
COPY file:595171150af68abc798ea385f7988d74b566aa8e84babff137f00b08b2164683 in /root/buildinfo/content_manifests/content-sets.json      
# Tue, 26 May 2026 10:05:38 GMT
COPY file:5e4784a2db9f1899592c7ac2b4556c3bb602168493a8e32d224b97a462909960 in /usr/share/buildinfo/labels.json      
# Tue, 26 May 2026 10:05:38 GMT
COPY file:5e4784a2db9f1899592c7ac2b4556c3bb602168493a8e32d224b97a462909960 in /root/buildinfo/labels.json      
# Tue, 26 May 2026 10:05:39 GMT
LABEL "architecture"="ppc64le" "vcs-type"="git" "vcs-ref"="28a4d5c7cdb1969ee63337adb47fcb350a380874" "org.opencontainers.image.revision"="28a4d5c7cdb1969ee63337adb47fcb350a380874" "build-date"="2026-05-26T10:05:11Z" "org.opencontainers.image.created"="2026-05-26T10:05:11Z" "release"="1779788807"org.opencontainers.image.revision=28a4d5c7cdb1969ee63337adb47fcb350a380874,org.opencontainers.image.created=2026-05-26T10:05:11Z
# Tue, 26 May 2026 23:08:26 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 26 May 2026 23:08:26 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 26 May 2026 23:08:26 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 26 May 2026 23:08:26 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en         gnupg2     ;     microdnf clean all # buildkit
# Tue, 26 May 2026 23:08:26 GMT
ENV JAVA_VERSION=jdk-25.0.3+9
# Tue, 26 May 2026 23:16:05 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='3e4287cb98870ba824ed698854bdc27cff984254caf66dd12cc291e7bfdde26b';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.3%2B9/OpenJDK25U-jdk_aarch64_linux_hotspot_25.0.3_9.tar.gz';          ;;        ppc64le)          ESUM='72b0fbb201716ca465ab704ec0fb12971abab3fdde5ae8d03b125a273522cf05';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.3%2B9/OpenJDK25U-jdk_ppc64le_linux_hotspot_25.0.3_9.tar.gz';          ;;        s390x)          ESUM='24b497d10acb6ee706ca30e1c8a929785c250cad54c5c12f1f8f93c3c06a53f7';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.3%2B9/OpenJDK25U-jdk_s390x_linux_hotspot_25.0.3_9.tar.gz';          ;;        x86_64)          ESUM='69264a7a211bf5029830d07bc3370f879769d62ebc5b5488e90c9343a2da0e1f';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.3%2B9/OpenJDK25U-jdk_x64_linux_hotspot_25.0.3_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Tue, 26 May 2026 23:16:10 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 26 May 2026 23:16:11 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 26 May 2026 23:16:11 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 26 May 2026 23:16:11 GMT
CMD ["jshell"]
# Wed, 27 May 2026 00:07:57 GMT
CMD ["gradle"]
# Wed, 27 May 2026 00:07:57 GMT
ENV GRADLE_HOME=/opt/gradle
# Wed, 27 May 2026 00:07:57 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 101 gradle     && useradd --system --gid gradle --uid 101 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Wed, 27 May 2026 00:07:57 GMT
VOLUME [/home/gradle/.gradle]
# Wed, 27 May 2026 00:07:57 GMT
WORKDIR /home/gradle
# Wed, 27 May 2026 00:08:30 GMT
RUN set -o errexit -o nounset     && microdnf install -y         make         curl         wget         tar                 findutils                 unzip         which                 git         git-lfs         subversion     && microdnf clean all         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which svn # buildkit
# Wed, 27 May 2026 00:08:30 GMT
ENV GRADLE_VERSION=9.5.1
# Wed, 27 May 2026 00:08:30 GMT
ARG GRADLE_DOWNLOAD_SHA256=bafc141b619ad6350fd975fc903156dd5c151998cc8b058e8c1044ab5f7b031f
# Wed, 27 May 2026 00:08:33 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=bafc141b619ad6350fd975fc903156dd5c151998cc8b058e8c1044ab5f7b031f
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Wed, 27 May 2026 00:08:33 GMT
USER gradle
# Wed, 27 May 2026 00:08:35 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=bafc141b619ad6350fd975fc903156dd5c151998cc8b058e8c1044ab5f7b031f
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --stacktrace --debug --version # buildkit
# Wed, 27 May 2026 00:08:35 GMT
USER root
```

-	Layers:
	-	`sha256:b4743f929036f49c12be6a577cbf8dbf4b9feeebdd83aef3c82da2056289053c`  
		Last Modified: Tue, 26 May 2026 12:17:22 GMT  
		Size: 38.8 MB (38794684 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e600a5e4b5bd9ee674e2def8e4bcf01be8963cfc1697cc6243834b5ac188e995`  
		Last Modified: Tue, 26 May 2026 23:08:57 GMT  
		Size: 31.9 MB (31932676 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86e74483bc9266336c56fe0b95889ddfedae62cb547839f425b4ea9b0efff8bd`  
		Last Modified: Tue, 26 May 2026 23:16:46 GMT  
		Size: 91.9 MB (91912916 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f0cb6a21247830051c439f1ad7e2dabb7cb19cedb5eb730b4eda048ae473110`  
		Last Modified: Tue, 26 May 2026 23:16:44 GMT  
		Size: 132.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff9acfedf0029c430cacdd169d7bae8fbbe11fe82e1a83fe1a74d41828a13e20`  
		Last Modified: Tue, 26 May 2026 23:16:44 GMT  
		Size: 2.3 KB (2291 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3aded828fb18a3b1cae36292b90c3c8ec918e2a00d62e6d2f2a3e021d0a4f268`  
		Last Modified: Wed, 27 May 2026 00:09:17 GMT  
		Size: 1.4 KB (1449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f2c1c55b304e298ecd58cd1dc7d145d2a0b9f33e8d736c92dde1bf249223155`  
		Last Modified: Wed, 27 May 2026 00:09:21 GMT  
		Size: 59.5 MB (59469771 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6886bb2bd8891af639bb5f5842b108f668630032e637d129c478f24d9f0ea1f1`  
		Last Modified: Wed, 27 May 2026 00:09:23 GMT  
		Size: 140.2 MB (140236987 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf81b743312293bf56effaad5868065985edb6ce2def7a2122fa09c09b13c393`  
		Last Modified: Wed, 27 May 2026 00:09:17 GMT  
		Size: 387.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:ubi10` - unknown; unknown

```console
$ docker pull gradle@sha256:363bf733e096ab2835b5799cdbf9606ba31a0e5f3ee0e62e283fac6a7be36f55
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.1 MB (7050451 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3fba48479c1e7599ca064706c8eb572f74e00d1b6450224e136dbe6d0ceedfb1`

```dockerfile
```

-	Layers:
	-	`sha256:663615bf18c0560da87bd02ae854a7f794b3d60858da856bdbdeb1a6e3d8300c`  
		Last Modified: Wed, 27 May 2026 00:09:17 GMT  
		Size: 7.0 MB (7025358 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6c216cd61187179912d95d3224712efea8ef183497c5d9a30ecdb2e4a1e63b37`  
		Last Modified: Wed, 27 May 2026 00:09:16 GMT  
		Size: 25.1 KB (25093 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:ubi10` - linux; s390x

```console
$ docker pull gradle@sha256:bd689062cf20cdc4e93cc0a44196859a7fc7e7e425bba81f6def6b05c78da21d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **350.9 MB (350924109 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e01eb4ae884050a8af5591a3f6b2d7a0b6801b8a6b3f657856e6be78ea284a3`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["gradle"]`

```dockerfile
# Tue, 26 May 2026 10:43:18 GMT
LABEL maintainer="Red Hat, Inc."
# Tue, 26 May 2026 10:43:18 GMT
LABEL vendor="Red Hat, Inc."
# Tue, 26 May 2026 10:43:18 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Tue, 26 May 2026 10:43:18 GMT
LABEL com.redhat.component="ubi10-minimal-container"       name="ubi10/ubi-minimal"       version="10.1"       cpe="cpe:/o:redhat:enterprise_linux:10.1"       distribution-scope="public"
# Tue, 26 May 2026 10:43:18 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Tue, 26 May 2026 10:43:18 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 10."
# Tue, 26 May 2026 10:43:18 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Tue, 26 May 2026 10:43:18 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Tue, 26 May 2026 10:43:18 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 10 Minimal"
# Tue, 26 May 2026 10:43:18 GMT
LABEL io.openshift.expose-services=""
# Tue, 26 May 2026 10:43:18 GMT
LABEL io.openshift.tags="minimal rhel10"
# Tue, 26 May 2026 10:43:18 GMT
ENV container oci
# Tue, 26 May 2026 10:43:19 GMT
COPY dir:a7c5d9f6499c23f09ef7d337bda5192f5b4deca45553e74bfae9fae1b20a60ef in /      
# Tue, 26 May 2026 10:43:19 GMT
COPY file:5de33b5fc08b00635bccf9134a18978dba13e2250aa51838f9969515a3957847 in /etc/yum.repos.d/.      
# Tue, 26 May 2026 10:43:19 GMT
CMD ["/bin/bash"]
# Tue, 26 May 2026 10:43:19 GMT
COPY file:595171150af68abc798ea385f7988d74b566aa8e84babff137f00b08b2164683 in /usr/share/buildinfo/content-sets.json      
# Tue, 26 May 2026 10:43:19 GMT
COPY file:595171150af68abc798ea385f7988d74b566aa8e84babff137f00b08b2164683 in /root/buildinfo/content_manifests/content-sets.json      
# Tue, 26 May 2026 10:43:21 GMT
COPY file:cf7bfba0ea2e3c47e53590ead66a27ae21af2a1dca6091ce8837539a1df6f22a in /usr/share/buildinfo/labels.json      
# Tue, 26 May 2026 10:43:21 GMT
COPY file:cf7bfba0ea2e3c47e53590ead66a27ae21af2a1dca6091ce8837539a1df6f22a in /root/buildinfo/labels.json      
# Tue, 26 May 2026 10:43:22 GMT
LABEL "architecture"="s390x" "vcs-type"="git" "vcs-ref"="28a4d5c7cdb1969ee63337adb47fcb350a380874" "org.opencontainers.image.revision"="28a4d5c7cdb1969ee63337adb47fcb350a380874" "build-date"="2026-05-26T10:43:06Z" "org.opencontainers.image.created"="2026-05-26T10:43:06Z" "release"="1779788807"org.opencontainers.image.revision=28a4d5c7cdb1969ee63337adb47fcb350a380874,org.opencontainers.image.created=2026-05-26T10:43:06Z
# Tue, 26 May 2026 23:08:25 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 26 May 2026 23:08:25 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 26 May 2026 23:08:25 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 26 May 2026 23:08:25 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en         gnupg2     ;     microdnf clean all # buildkit
# Tue, 26 May 2026 23:08:25 GMT
ENV JAVA_VERSION=jdk-25.0.3+9
# Tue, 26 May 2026 23:10:51 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='3e4287cb98870ba824ed698854bdc27cff984254caf66dd12cc291e7bfdde26b';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.3%2B9/OpenJDK25U-jdk_aarch64_linux_hotspot_25.0.3_9.tar.gz';          ;;        ppc64le)          ESUM='72b0fbb201716ca465ab704ec0fb12971abab3fdde5ae8d03b125a273522cf05';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.3%2B9/OpenJDK25U-jdk_ppc64le_linux_hotspot_25.0.3_9.tar.gz';          ;;        s390x)          ESUM='24b497d10acb6ee706ca30e1c8a929785c250cad54c5c12f1f8f93c3c06a53f7';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.3%2B9/OpenJDK25U-jdk_s390x_linux_hotspot_25.0.3_9.tar.gz';          ;;        x86_64)          ESUM='69264a7a211bf5029830d07bc3370f879769d62ebc5b5488e90c9343a2da0e1f';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.3%2B9/OpenJDK25U-jdk_x64_linux_hotspot_25.0.3_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Tue, 26 May 2026 23:10:53 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 26 May 2026 23:10:53 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 26 May 2026 23:10:53 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 26 May 2026 23:10:53 GMT
CMD ["jshell"]
# Wed, 27 May 2026 00:08:29 GMT
CMD ["gradle"]
# Wed, 27 May 2026 00:08:29 GMT
ENV GRADLE_HOME=/opt/gradle
# Wed, 27 May 2026 00:08:29 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 101 gradle     && useradd --system --gid gradle --uid 101 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Wed, 27 May 2026 00:08:29 GMT
VOLUME [/home/gradle/.gradle]
# Wed, 27 May 2026 00:08:29 GMT
WORKDIR /home/gradle
# Wed, 27 May 2026 00:08:51 GMT
RUN set -o errexit -o nounset     && microdnf install -y         make         curl         wget         tar                 findutils                 unzip         which                 git         git-lfs         subversion     && microdnf clean all         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which svn # buildkit
# Wed, 27 May 2026 00:08:51 GMT
ENV GRADLE_VERSION=9.5.1
# Wed, 27 May 2026 00:08:51 GMT
ARG GRADLE_DOWNLOAD_SHA256=bafc141b619ad6350fd975fc903156dd5c151998cc8b058e8c1044ab5f7b031f
# Wed, 27 May 2026 00:08:59 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=bafc141b619ad6350fd975fc903156dd5c151998cc8b058e8c1044ab5f7b031f
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Wed, 27 May 2026 00:08:59 GMT
USER gradle
# Wed, 27 May 2026 00:09:01 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=bafc141b619ad6350fd975fc903156dd5c151998cc8b058e8c1044ab5f7b031f
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --stacktrace --debug --version # buildkit
# Wed, 27 May 2026 00:09:01 GMT
USER root
```

-	Layers:
	-	`sha256:3f3af3c01ebb5e415417fa01cdc18de3e0533f557596f831f5cdf4441dd071e3`  
		Last Modified: Tue, 26 May 2026 12:17:14 GMT  
		Size: 34.4 MB (34449572 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c036331f082117718d32b7a6dcfa78b23ee5fa1dcd892f2d797f021397b44fb8`  
		Last Modified: Tue, 26 May 2026 23:08:58 GMT  
		Size: 28.5 MB (28525803 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d31f2b74279c2a6192c5bd0f0e09da192c544c80a3e43c8e12dfcb867f2c47d7`  
		Last Modified: Tue, 26 May 2026 23:11:20 GMT  
		Size: 88.4 MB (88421668 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:011ac04ed91d185622a64c578deac5ba82ab094f42168d036a2c3b9ffedf9de3`  
		Last Modified: Tue, 26 May 2026 23:11:18 GMT  
		Size: 130.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74218558a996ec2f93c4bce3c7ee118e63bdf857075c3bdeeea21f6592a08cb8`  
		Last Modified: Tue, 26 May 2026 23:11:12 GMT  
		Size: 2.3 KB (2291 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de888590bb326e6965ba3b77cc14eb6764a7f613a2c92465543057b08cc421d3`  
		Last Modified: Wed, 27 May 2026 00:09:46 GMT  
		Size: 1.4 KB (1450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ecc2d1e9f19232e91f91146ad9fe6f600433b732b7ede6246607bc4aa1b429d`  
		Last Modified: Wed, 27 May 2026 00:09:48 GMT  
		Size: 59.3 MB (59285794 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c973e2c538c551d575d839b9207d41f492a60fe93a6e64a62ab34cb56b0de89`  
		Last Modified: Wed, 27 May 2026 00:09:50 GMT  
		Size: 140.2 MB (140236985 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ec618a5eaab1ec532a0927a081ef51afeb9635928be46bf7fe04f58288f31e4`  
		Last Modified: Wed, 27 May 2026 00:09:46 GMT  
		Size: 384.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:ubi10` - unknown; unknown

```console
$ docker pull gradle@sha256:f427c1e0627741ee2be2519cf9075549eeea38e5b665e52a8e16750543c8db73
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 MB (7040832 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:12eac8aa699933e26fb6aa0de9931aadfb48c58f2d612f0b8842773673970d4a`

```dockerfile
```

-	Layers:
	-	`sha256:a67f5e1cddbcd9b4b910b4c28dd4c27c1be72b37c3e5dbee28dab1d276c5f4d2`  
		Last Modified: Wed, 27 May 2026 00:09:47 GMT  
		Size: 7.0 MB (7015825 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:34d3f626b61f218052773c040e2367878ad6b84de5d4338061fd8500589f4a67`  
		Last Modified: Wed, 27 May 2026 00:09:46 GMT  
		Size: 25.0 KB (25007 bytes)  
		MIME: application/vnd.in-toto+json
