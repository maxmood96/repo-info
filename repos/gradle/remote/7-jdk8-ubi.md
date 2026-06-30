## `gradle:7-jdk8-ubi`

```console
$ docker pull gradle@sha256:a22f2eefcf71683ab26f1be3a44858f8fb5b161493a2b5662748f2a6890983f7
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `gradle:7-jdk8-ubi` - linux; amd64

```console
$ docker pull gradle@sha256:d024f9ef6e1a4cc580308477f7d6a9fb2a16a3e29daddd1baa333d8003f6cff6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **293.2 MB (293233830 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d12f7f6e5a88e7626dbb9bea9a18b1a08708d204d3d1fe96c4eee122a3d0dec4`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["gradle"]`

```dockerfile
# Mon, 29 Jun 2026 04:51:28 GMT
LABEL maintainer="Red Hat, Inc."
# Mon, 29 Jun 2026 04:51:28 GMT
LABEL vendor="Red Hat, Inc."
# Mon, 29 Jun 2026 04:51:28 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Mon, 29 Jun 2026 04:51:28 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.8"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Mon, 29 Jun 2026 04:51:28 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Mon, 29 Jun 2026 04:51:28 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Mon, 29 Jun 2026 04:51:28 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 29 Jun 2026 04:51:28 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 29 Jun 2026 04:51:28 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Mon, 29 Jun 2026 04:51:28 GMT
LABEL io.openshift.expose-services=""
# Mon, 29 Jun 2026 04:51:29 GMT
LABEL io.openshift.tags="minimal rhel9"
# Mon, 29 Jun 2026 04:51:29 GMT
ENV container oci
# Mon, 29 Jun 2026 04:51:29 GMT
COPY dir:739d9f5e7f28cc70aad7ae94223fd7338511092b65f74c794a7b61ab61297289 in /      
# Mon, 29 Jun 2026 04:51:29 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Mon, 29 Jun 2026 04:51:29 GMT
CMD ["/bin/bash"]
# Mon, 29 Jun 2026 04:51:30 GMT
COPY dir:0d9e9fcd450f7954ea82dd60c01a9062c55769458d716bb966e758775cf44d8c in /usr/share/buildinfo/      
# Mon, 29 Jun 2026 04:51:30 GMT
COPY dir:0d9e9fcd450f7954ea82dd60c01a9062c55769458d716bb966e758775cf44d8c in /root/buildinfo/      
# Mon, 29 Jun 2026 04:51:30 GMT
LABEL "org.opencontainers.image.created"="2026-06-29T04:50:08Z" "org.opencontainers.image.revision"="b0536a5d45ebd046bef183288a4f1cd5e6d68f66" "build-date"="2026-06-29T04:50:08Z" "architecture"="x86_64" "vcs-ref"="b0536a5d45ebd046bef183288a4f1cd5e6d68f66" "vcs-type"="git" "release"="1782708562"org.opencontainers.image.created=2026-06-29T04:50:08Z,org.opencontainers.image.revision=b0536a5d45ebd046bef183288a4f1cd5e6d68f66
# Tue, 30 Jun 2026 00:10:33 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 30 Jun 2026 00:10:33 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 30 Jun 2026 00:10:33 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 30 Jun 2026 00:10:33 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en     ;     microdnf clean all # buildkit
# Tue, 30 Jun 2026 00:10:33 GMT
ENV JAVA_VERSION=jdk8u492-b09
# Tue, 30 Jun 2026 00:10:38 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='3c2253b986909c20f79d6de7a0cb957f89c243df57615897836046e24d2e5257';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u492-b09/OpenJDK8U-jdk_aarch64_linux_hotspot_8u492b09.tar.gz';          ;;        ppc64le)          ESUM='867e477e0a54159c7b774c55cfb046767120b1de43f705fa775ece74ea39e341';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u492-b09/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u492b09.tar.gz';          ;;        x86_64)          ESUM='da257f161d7f8c6ca5b0e5d9e4090f65ac28c5e398072e68b8ae87988b1d1a2e';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u492-b09/OpenJDK8U-jdk_x64_linux_hotspot_8u492b09.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip; # buildkit
# Tue, 30 Jun 2026 00:10:38 GMT
RUN set -eux;     echo "Verifying install ...";     echo "javac -version"; javac -version;     echo "java -version"; java -version;     echo "Complete." # buildkit
# Tue, 30 Jun 2026 00:10:38 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 30 Jun 2026 00:10:38 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 30 Jun 2026 01:11:17 GMT
CMD ["gradle"]
# Tue, 30 Jun 2026 01:11:17 GMT
ENV GRADLE_HOME=/opt/gradle
# Tue, 30 Jun 2026 01:11:17 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 101 gradle     && useradd --system --gid gradle --uid 101 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Tue, 30 Jun 2026 01:11:17 GMT
VOLUME [/home/gradle/.gradle]
# Tue, 30 Jun 2026 01:11:18 GMT
WORKDIR /home/gradle
# Tue, 30 Jun 2026 01:11:21 GMT
RUN set -o errexit -o nounset     && microdnf install -y         make                 findutils                 unzip         which                 git         git-lfs         subversion     && microdnf clean all         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which svn # buildkit
# Tue, 30 Jun 2026 01:11:21 GMT
ENV GRADLE_VERSION=7.6.6
# Tue, 30 Jun 2026 01:11:21 GMT
ARG GRADLE_DOWNLOAD_SHA256=673d9776f303bc7048fc3329d232d6ebf1051b07893bd9d11616fad9a8673be0
# Tue, 30 Jun 2026 01:11:24 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=673d9776f303bc7048fc3329d232d6ebf1051b07893bd9d11616fad9a8673be0
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Tue, 30 Jun 2026 01:11:24 GMT
USER gradle
# Tue, 30 Jun 2026 01:11:25 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=673d9776f303bc7048fc3329d232d6ebf1051b07893bd9d11616fad9a8673be0
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Tue, 30 Jun 2026 01:11:25 GMT
USER root
```

-	Layers:
	-	`sha256:49d891c4faa7e711f5655dc8fb5604fa8b30c65842b722ab503bcb4a08c3f5cc`  
		Last Modified: Mon, 29 Jun 2026 06:11:20 GMT  
		Size: 40.7 MB (40686817 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bf863bfad5c865bbca7848dc24c7d66181ab857c5ce404e8e90bea2c793f983`  
		Last Modified: Tue, 30 Jun 2026 00:10:52 GMT  
		Size: 30.9 MB (30877463 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3d96b2cdc20bfeceb3f97772019dfd553c843d2c262a454d159d276ea338ad1`  
		Last Modified: Tue, 30 Jun 2026 00:10:53 GMT  
		Size: 55.2 MB (55199136 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6b4883a9f302d5f50cc566da8b06f72414156325a1c6c7fc98972f49765e317`  
		Last Modified: Tue, 30 Jun 2026 00:10:50 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06d9036a50542871e6078a2fbef65230e259c6a1787f29f303b9983303d5d0b4`  
		Last Modified: Tue, 30 Jun 2026 00:10:51 GMT  
		Size: 2.5 KB (2489 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a30680332f5b1f063112e74912e974a5d2a5b86e3a9293a6047a3630bef001e`  
		Last Modified: Tue, 30 Jun 2026 01:11:40 GMT  
		Size: 1.7 KB (1704 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c72641ffd72de128dfcdf44cbe60cc416fbf33c5aa68c9cf5020a8dd56223f1d`  
		Last Modified: Tue, 30 Jun 2026 01:11:42 GMT  
		Size: 37.9 MB (37941709 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18eb66fedf4191f81016ee1b6b6518b379530be3b6e9db7ea408a08e7880e41f`  
		Last Modified: Tue, 30 Jun 2026 01:11:44 GMT  
		Size: 128.5 MB (128469423 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98225f55060b960fe02928bed04e3b56d1edea3b56c099ddc6ca5445e22dbab9`  
		Last Modified: Tue, 30 Jun 2026 01:11:40 GMT  
		Size: 54.9 KB (54929 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:7-jdk8-ubi` - unknown; unknown

```console
$ docker pull gradle@sha256:c4435c847632a08a41e76205644e952c43c368581d649cbabfd5b28a65061c7a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5461621 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d37ec47a4423d41abc67c34a3a9d530a195c1569421b52da95f72d7ac318be6`

```dockerfile
```

-	Layers:
	-	`sha256:59011e27217c0ce5adefa329d85cb7117ef1bc7c90433f56c3e2d2ae6a4156b7`  
		Last Modified: Tue, 30 Jun 2026 01:11:40 GMT  
		Size: 5.4 MB (5438103 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4b3db62257592b1f81818e359ccfd6aa8437e2381b7573e07833e5774f3fa53e`  
		Last Modified: Tue, 30 Jun 2026 01:11:40 GMT  
		Size: 23.5 KB (23518 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:7-jdk8-ubi` - linux; arm64 variant v8

```console
$ docker pull gradle@sha256:ea81d76f6dde5f1eae89b32b61f5886a782973865769b5321f8e965121278d2a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **289.6 MB (289647624 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd241df35ee42604e8f867b95a29bded6486f9f598ecedede05241922047e7fc`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["gradle"]`

```dockerfile
# Mon, 29 Jun 2026 04:52:39 GMT
LABEL maintainer="Red Hat, Inc."
# Mon, 29 Jun 2026 04:52:39 GMT
LABEL vendor="Red Hat, Inc."
# Mon, 29 Jun 2026 04:52:39 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Mon, 29 Jun 2026 04:52:39 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.8"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Mon, 29 Jun 2026 04:52:39 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Mon, 29 Jun 2026 04:52:39 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Mon, 29 Jun 2026 04:52:39 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 29 Jun 2026 04:52:39 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 29 Jun 2026 04:52:40 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Mon, 29 Jun 2026 04:52:40 GMT
LABEL io.openshift.expose-services=""
# Mon, 29 Jun 2026 04:52:40 GMT
LABEL io.openshift.tags="minimal rhel9"
# Mon, 29 Jun 2026 04:52:40 GMT
ENV container oci
# Mon, 29 Jun 2026 04:52:40 GMT
COPY dir:e6026d5a9734bc68758c885a994b1d95fd048fb5657a86e6b5e51129e847f4d9 in /      
# Mon, 29 Jun 2026 04:52:40 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Mon, 29 Jun 2026 04:52:40 GMT
CMD ["/bin/bash"]
# Mon, 29 Jun 2026 04:52:40 GMT
COPY dir:f71705f172541ee791b12a4ded058a688a198aeab58382823b47b8b83bf77d5d in /usr/share/buildinfo/      
# Mon, 29 Jun 2026 04:52:41 GMT
COPY dir:f71705f172541ee791b12a4ded058a688a198aeab58382823b47b8b83bf77d5d in /root/buildinfo/      
# Mon, 29 Jun 2026 04:52:41 GMT
LABEL "org.opencontainers.image.created"="2026-06-29T04:52:17Z" "org.opencontainers.image.revision"="b0536a5d45ebd046bef183288a4f1cd5e6d68f66" "build-date"="2026-06-29T04:52:17Z" "architecture"="aarch64" "vcs-ref"="b0536a5d45ebd046bef183288a4f1cd5e6d68f66" "vcs-type"="git" "release"="1782708562"org.opencontainers.image.created=2026-06-29T04:52:17Z,org.opencontainers.image.revision=b0536a5d45ebd046bef183288a4f1cd5e6d68f66
# Tue, 30 Jun 2026 00:09:15 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 30 Jun 2026 00:09:15 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 30 Jun 2026 00:09:15 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 30 Jun 2026 00:09:15 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en     ;     microdnf clean all # buildkit
# Tue, 30 Jun 2026 00:09:15 GMT
ENV JAVA_VERSION=jdk8u492-b09
# Tue, 30 Jun 2026 00:09:20 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='3c2253b986909c20f79d6de7a0cb957f89c243df57615897836046e24d2e5257';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u492-b09/OpenJDK8U-jdk_aarch64_linux_hotspot_8u492b09.tar.gz';          ;;        ppc64le)          ESUM='867e477e0a54159c7b774c55cfb046767120b1de43f705fa775ece74ea39e341';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u492-b09/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u492b09.tar.gz';          ;;        x86_64)          ESUM='da257f161d7f8c6ca5b0e5d9e4090f65ac28c5e398072e68b8ae87988b1d1a2e';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u492-b09/OpenJDK8U-jdk_x64_linux_hotspot_8u492b09.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip; # buildkit
# Tue, 30 Jun 2026 00:09:20 GMT
RUN set -eux;     echo "Verifying install ...";     echo "javac -version"; javac -version;     echo "java -version"; java -version;     echo "Complete." # buildkit
# Tue, 30 Jun 2026 00:09:20 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 30 Jun 2026 00:09:20 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 30 Jun 2026 01:11:39 GMT
CMD ["gradle"]
# Tue, 30 Jun 2026 01:11:39 GMT
ENV GRADLE_HOME=/opt/gradle
# Tue, 30 Jun 2026 01:11:39 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 101 gradle     && useradd --system --gid gradle --uid 101 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Tue, 30 Jun 2026 01:11:39 GMT
VOLUME [/home/gradle/.gradle]
# Tue, 30 Jun 2026 01:11:39 GMT
WORKDIR /home/gradle
# Tue, 30 Jun 2026 01:11:43 GMT
RUN set -o errexit -o nounset     && microdnf install -y         make                 findutils                 unzip         which                 git         git-lfs         subversion     && microdnf clean all         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which svn # buildkit
# Tue, 30 Jun 2026 01:11:43 GMT
ENV GRADLE_VERSION=7.6.6
# Tue, 30 Jun 2026 01:11:43 GMT
ARG GRADLE_DOWNLOAD_SHA256=673d9776f303bc7048fc3329d232d6ebf1051b07893bd9d11616fad9a8673be0
# Tue, 30 Jun 2026 01:11:46 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=673d9776f303bc7048fc3329d232d6ebf1051b07893bd9d11616fad9a8673be0
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Tue, 30 Jun 2026 01:11:46 GMT
USER gradle
# Tue, 30 Jun 2026 01:11:46 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=673d9776f303bc7048fc3329d232d6ebf1051b07893bd9d11616fad9a8673be0
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Tue, 30 Jun 2026 01:11:46 GMT
USER root
```

-	Layers:
	-	`sha256:6415421793d9d3697d4a730b8a3f7869954a938b640547194c623cb3a001e6c2`  
		Last Modified: Mon, 29 Jun 2026 06:11:28 GMT  
		Size: 38.8 MB (38819449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c609dcbef36918d198f81c35e8f83dfa4f97ee71e4867f46913b3e81183289f6`  
		Last Modified: Tue, 30 Jun 2026 00:09:34 GMT  
		Size: 30.8 MB (30794487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52fa42bd1fbc66a6733eff53b439d8005ae619a3608d8114f7045de29aa5f668`  
		Last Modified: Tue, 30 Jun 2026 00:09:35 GMT  
		Size: 54.3 MB (54273411 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17aea52ccdb27fd42ffdd883152dd65bc239c60365ef01b8b9a9f4f364715122`  
		Last Modified: Tue, 30 Jun 2026 00:09:32 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6479083c2d373fd922d876a7e81bb2ba75421bab6df102fc8df186e054acbd8a`  
		Last Modified: Tue, 30 Jun 2026 00:09:33 GMT  
		Size: 2.5 KB (2490 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02f59f02339b15098f6f04a21b6df39455b0aec9394b2c57f412df847e999134`  
		Last Modified: Tue, 30 Jun 2026 01:12:01 GMT  
		Size: 1.7 KB (1709 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:500fa838ac94fdcc2173a38f6b5c668fc647074cf843fdafcb6667ad93e528c7`  
		Last Modified: Tue, 30 Jun 2026 01:12:03 GMT  
		Size: 37.2 MB (37226982 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43f9fe1da2bdc92e7f45807c1f7196f95bc03b702e1635e825cb107dc95cb267`  
		Last Modified: Tue, 30 Jun 2026 01:12:05 GMT  
		Size: 128.5 MB (128469416 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01ee91346079f01433617bf53e9f28f9534eef33aea64347dca51f65d19d725d`  
		Last Modified: Tue, 30 Jun 2026 01:12:01 GMT  
		Size: 59.5 KB (59522 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:7-jdk8-ubi` - unknown; unknown

```console
$ docker pull gradle@sha256:6a39f540d85dc1843783c8842e393134b4c2e884a77d35f5bbd36a8dba51dbf8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5460122 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b1cd38b2a3a4a2e3bb2ebb0314629db1199e356c649832e98eebc03a1570f3b7`

```dockerfile
```

-	Layers:
	-	`sha256:e395df6c88cbc55813d8e994a2fb857391ff1b3cec2d79782527080b98177388`  
		Last Modified: Tue, 30 Jun 2026 01:12:01 GMT  
		Size: 5.4 MB (5436431 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9f6011cb88ec36385e030f8f560474f85ef591f59f7ab1ce96ec711e738c80de`  
		Last Modified: Tue, 30 Jun 2026 01:12:01 GMT  
		Size: 23.7 KB (23691 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:7-jdk8-ubi` - linux; ppc64le

```console
$ docker pull gradle@sha256:426ddf9b849945ed8b95a786b51ea3b906b7a063ebc8ab4c74da921ac45be0be
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **295.5 MB (295531219 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:99bd35d9505a687535824465ea769ee3ee12a26e90cfba67206e0d0b87e6b110`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["gradle"]`

```dockerfile
# Mon, 29 Jun 2026 04:51:43 GMT
LABEL maintainer="Red Hat, Inc."
# Mon, 29 Jun 2026 04:51:43 GMT
LABEL vendor="Red Hat, Inc."
# Mon, 29 Jun 2026 04:51:43 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Mon, 29 Jun 2026 04:51:43 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.8"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Mon, 29 Jun 2026 04:51:43 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Mon, 29 Jun 2026 04:51:43 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Mon, 29 Jun 2026 04:51:43 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 29 Jun 2026 04:51:43 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 29 Jun 2026 04:51:43 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Mon, 29 Jun 2026 04:51:43 GMT
LABEL io.openshift.expose-services=""
# Mon, 29 Jun 2026 04:51:43 GMT
LABEL io.openshift.tags="minimal rhel9"
# Mon, 29 Jun 2026 04:51:43 GMT
ENV container oci
# Mon, 29 Jun 2026 04:51:44 GMT
COPY dir:4c1c925f52e2bf94f6f51ed2040707135dad2469062fae485083f1e3880aa690 in /      
# Mon, 29 Jun 2026 04:51:44 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Mon, 29 Jun 2026 04:51:44 GMT
CMD ["/bin/bash"]
# Mon, 29 Jun 2026 04:51:44 GMT
COPY dir:b37bcc35410383d4962d130d7f52524a29de2416d65cdbb7496d3441baade925 in /usr/share/buildinfo/      
# Mon, 29 Jun 2026 04:51:44 GMT
COPY dir:b37bcc35410383d4962d130d7f52524a29de2416d65cdbb7496d3441baade925 in /root/buildinfo/      
# Mon, 29 Jun 2026 04:51:44 GMT
LABEL "org.opencontainers.image.created"="2026-06-29T04:51:26Z" "org.opencontainers.image.revision"="b0536a5d45ebd046bef183288a4f1cd5e6d68f66" "build-date"="2026-06-29T04:51:26Z" "architecture"="ppc64le" "vcs-ref"="b0536a5d45ebd046bef183288a4f1cd5e6d68f66" "vcs-type"="git" "release"="1782708562"org.opencontainers.image.created=2026-06-29T04:51:26Z,org.opencontainers.image.revision=b0536a5d45ebd046bef183288a4f1cd5e6d68f66
# Tue, 30 Jun 2026 00:11:34 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 30 Jun 2026 00:11:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 30 Jun 2026 00:11:34 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 30 Jun 2026 00:11:34 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en     ;     microdnf clean all # buildkit
# Tue, 30 Jun 2026 00:11:34 GMT
ENV JAVA_VERSION=jdk8u492-b09
# Tue, 30 Jun 2026 00:11:42 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='3c2253b986909c20f79d6de7a0cb957f89c243df57615897836046e24d2e5257';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u492-b09/OpenJDK8U-jdk_aarch64_linux_hotspot_8u492b09.tar.gz';          ;;        ppc64le)          ESUM='867e477e0a54159c7b774c55cfb046767120b1de43f705fa775ece74ea39e341';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u492-b09/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u492b09.tar.gz';          ;;        x86_64)          ESUM='da257f161d7f8c6ca5b0e5d9e4090f65ac28c5e398072e68b8ae87988b1d1a2e';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u492-b09/OpenJDK8U-jdk_x64_linux_hotspot_8u492b09.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip; # buildkit
# Tue, 30 Jun 2026 00:11:42 GMT
RUN set -eux;     echo "Verifying install ...";     echo "javac -version"; javac -version;     echo "java -version"; java -version;     echo "Complete." # buildkit
# Tue, 30 Jun 2026 00:11:43 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 30 Jun 2026 00:11:43 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 30 Jun 2026 01:10:56 GMT
CMD ["gradle"]
# Tue, 30 Jun 2026 01:10:56 GMT
ENV GRADLE_HOME=/opt/gradle
# Tue, 30 Jun 2026 01:10:56 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 101 gradle     && useradd --system --gid gradle --uid 101 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Tue, 30 Jun 2026 01:10:56 GMT
VOLUME [/home/gradle/.gradle]
# Tue, 30 Jun 2026 01:10:56 GMT
WORKDIR /home/gradle
# Tue, 30 Jun 2026 01:13:19 GMT
RUN set -o errexit -o nounset     && microdnf install -y         make                 findutils                 unzip         which                 git         git-lfs         subversion     && microdnf clean all         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which svn # buildkit
# Tue, 30 Jun 2026 01:13:19 GMT
ENV GRADLE_VERSION=7.6.6
# Tue, 30 Jun 2026 01:13:19 GMT
ARG GRADLE_DOWNLOAD_SHA256=673d9776f303bc7048fc3329d232d6ebf1051b07893bd9d11616fad9a8673be0
# Tue, 30 Jun 2026 01:13:23 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=673d9776f303bc7048fc3329d232d6ebf1051b07893bd9d11616fad9a8673be0
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Tue, 30 Jun 2026 01:13:23 GMT
USER gradle
# Tue, 30 Jun 2026 01:13:24 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=673d9776f303bc7048fc3329d232d6ebf1051b07893bd9d11616fad9a8673be0
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Tue, 30 Jun 2026 01:13:24 GMT
USER root
```

-	Layers:
	-	`sha256:cab5e0c171012774531d882f585d3be1eb8a97b88a5126afe48b35169caafc50`  
		Last Modified: Mon, 29 Jun 2026 06:11:46 GMT  
		Size: 45.1 MB (45078234 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3383a7a24164308cd34dd0b3f319e45e2be49008abc404e48fcc73abdb8e02b0`  
		Last Modified: Tue, 30 Jun 2026 00:12:08 GMT  
		Size: 30.1 MB (30082685 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aea97e0132e173dedefb9a4d076c4c6d1bbda6eb563e9dc215e7e3813513e27c`  
		Last Modified: Tue, 30 Jun 2026 00:12:13 GMT  
		Size: 52.7 MB (52669706 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2cfd791e9904342f22f990eaa7baff59c8c22a6ad00a41349f18bf1e1b35f87`  
		Last Modified: Tue, 30 Jun 2026 00:12:06 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1b03050b22047f98e735bf4c6b9bc9afc4ab68c98ec31623707ba70fd8a1ae5`  
		Last Modified: Tue, 30 Jun 2026 00:12:12 GMT  
		Size: 2.5 KB (2489 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa71042449cd520208a41d64796d39d6ccdd6b8790b8dc1cfeb3303ec4ffabe0`  
		Last Modified: Tue, 30 Jun 2026 01:11:43 GMT  
		Size: 1.7 KB (1716 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b315a0d93a13a6e43fcfdf13e10ef9efb92b2d646d7d19bf5a6b080cd5976ab0`  
		Last Modified: Tue, 30 Jun 2026 01:13:58 GMT  
		Size: 39.2 MB (39191797 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5844f03ef31d5ae7164651f26d91e55aa4e6e383970a6d96fab43eaa3e0ec95e`  
		Last Modified: Tue, 30 Jun 2026 01:14:00 GMT  
		Size: 128.5 MB (128469420 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5208f56a566dffba184522d04b82d93f68a3ae4d88999d55b188a5f9e3dec6d9`  
		Last Modified: Tue, 30 Jun 2026 01:13:56 GMT  
		Size: 35.0 KB (35012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:7-jdk8-ubi` - unknown; unknown

```console
$ docker pull gradle@sha256:be28e858b2e722da714c9e1f23d4ae99dcf51acf238e802392a49d364f1f5eb9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5457897 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e882ea2b4758575c283c2f906a52ab87a23a38b430ac1d03cc0fd39c6b1ee08c`

```dockerfile
```

-	Layers:
	-	`sha256:4a06e1f6c6f89dd55da15aae53e741f1903c90f36803b86e82ab098f381824aa`  
		Last Modified: Tue, 30 Jun 2026 01:13:56 GMT  
		Size: 5.4 MB (5434281 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5ba2217c9d5751aaba42d5e74253533eefe6626a3e84e538c61846104d112b40`  
		Last Modified: Tue, 30 Jun 2026 01:13:56 GMT  
		Size: 23.6 KB (23616 bytes)  
		MIME: application/vnd.in-toto+json
