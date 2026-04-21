## `gradle:9-jdk17-ubi9`

```console
$ docker pull gradle@sha256:58ba31e67be019981a040143f537e699d42284e7b30a32c27aa37662145d4555
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

### `gradle:9-jdk17-ubi9` - linux; amd64

```console
$ docker pull gradle@sha256:90da5ec057cb712609965a01833c1c5f0b14bfaa0c73094d771f1ef67f69c283
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **390.6 MB (390550817 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6d0e6b6f2779884f8ad2c0cc7bc5c31ec4974d04593415b962b4dedbb23f4fbb`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["gradle"]`

```dockerfile
# Mon, 20 Apr 2026 00:47:05 GMT
LABEL maintainer="Red Hat, Inc."
# Mon, 20 Apr 2026 00:47:05 GMT
LABEL vendor="Red Hat, Inc."
# Mon, 20 Apr 2026 00:47:05 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Mon, 20 Apr 2026 00:47:05 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.7"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Mon, 20 Apr 2026 00:47:05 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Mon, 20 Apr 2026 00:47:05 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Mon, 20 Apr 2026 00:47:05 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 20 Apr 2026 00:47:05 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 20 Apr 2026 00:47:05 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Mon, 20 Apr 2026 00:47:05 GMT
LABEL io.openshift.expose-services=""
# Mon, 20 Apr 2026 00:47:05 GMT
LABEL io.openshift.tags="minimal rhel9"
# Mon, 20 Apr 2026 00:47:05 GMT
ENV container oci
# Mon, 20 Apr 2026 00:47:06 GMT
COPY dir:95d17c57ef40a5dba79704e92b9c5527d3acb3226364e42c0d41763471e61ce6 in /      
# Mon, 20 Apr 2026 00:47:06 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Mon, 20 Apr 2026 00:47:06 GMT
CMD ["/bin/bash"]
# Mon, 20 Apr 2026 00:47:06 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /usr/share/buildinfo/content-sets.json      
# Mon, 20 Apr 2026 00:47:06 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /root/buildinfo/content_manifests/content-sets.json      
# Mon, 20 Apr 2026 00:47:06 GMT
COPY file:40b821b4439524877f4c01a660d9685262f2f008f6c6de9ba8b690c7e2740303 in /usr/share/buildinfo/labels.json      
# Mon, 20 Apr 2026 00:47:06 GMT
COPY file:40b821b4439524877f4c01a660d9685262f2f008f6c6de9ba8b690c7e2740303 in /root/buildinfo/labels.json      
# Mon, 20 Apr 2026 00:47:06 GMT
LABEL "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="0bc61a274edddc1467c2ad0ddc3139543c4da4da" "org.opencontainers.image.revision"="0bc61a274edddc1467c2ad0ddc3139543c4da4da" "build-date"="2026-04-20T00:46:48Z" "org.opencontainers.image.created"="2026-04-20T00:46:48Z" "release"="1776645941"org.opencontainers.image.revision=0bc61a274edddc1467c2ad0ddc3139543c4da4da,org.opencontainers.image.created=2026-04-20T00:46:48Z
# Mon, 20 Apr 2026 23:06:16 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 20 Apr 2026 23:06:16 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 20 Apr 2026 23:06:16 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 20 Apr 2026 23:06:16 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en     ;     microdnf clean all # buildkit
# Mon, 20 Apr 2026 23:06:16 GMT
ENV JAVA_VERSION=jdk-17.0.18+8
# Mon, 20 Apr 2026 23:06:23 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='592a6702b3a07a0e0b82cb38aaab149bfce1b0c24d6b57ddb410bd9009333095';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jdk_aarch64_linux_hotspot_17.0.18_8.tar.gz';          ;;        ppc64le)          ESUM='5ab89fbde560e1a09386f389dd7881715b896f49c6e9aa974f72d551337dba5e';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jdk_ppc64le_linux_hotspot_17.0.18_8.tar.gz';          ;;        s390x)          ESUM='3693469655bcfa2fa5e70907245a2b3bc4236db7d9fa1b9feb0ab7abd235da09';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jdk_s390x_linux_hotspot_17.0.18_8.tar.gz';          ;;        x86_64)          ESUM='0c94cbb54325c40dcf026143eb621562017db5525727f2d9131a11250f72c450';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jdk_x64_linux_hotspot_17.0.18_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Mon, 20 Apr 2026 23:06:24 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Mon, 20 Apr 2026 23:06:24 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Mon, 20 Apr 2026 23:06:24 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Mon, 20 Apr 2026 23:06:24 GMT
CMD ["jshell"]
# Tue, 21 Apr 2026 00:01:30 GMT
CMD ["gradle"]
# Tue, 21 Apr 2026 00:01:30 GMT
ENV GRADLE_HOME=/opt/gradle
# Tue, 21 Apr 2026 00:01:30 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 101 gradle     && useradd --system --gid gradle --uid 101 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Tue, 21 Apr 2026 00:01:30 GMT
VOLUME [/home/gradle/.gradle]
# Tue, 21 Apr 2026 00:01:30 GMT
WORKDIR /home/gradle
# Tue, 21 Apr 2026 00:01:36 GMT
RUN set -o errexit -o nounset     && microdnf install -y         make         curl-minimal         wget         tar                 findutils                 unzip         which                 git         git-lfs         subversion     && microdnf clean all         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which svn # buildkit
# Tue, 21 Apr 2026 00:01:36 GMT
ENV GRADLE_VERSION=9.4.1
# Tue, 21 Apr 2026 00:01:36 GMT
ARG GRADLE_DOWNLOAD_SHA256=2ab2958f2a1e51120c326cad6f385153bb11ee93b3c216c5fccebfdfbb7ec6cb
# Tue, 21 Apr 2026 00:01:39 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=2ab2958f2a1e51120c326cad6f385153bb11ee93b3c216c5fccebfdfbb7ec6cb
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Tue, 21 Apr 2026 00:01:39 GMT
USER gradle
# Tue, 21 Apr 2026 00:01:39 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=2ab2958f2a1e51120c326cad6f385153bb11ee93b3c216c5fccebfdfbb7ec6cb
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --stacktrace --debug --version # buildkit
# Tue, 21 Apr 2026 00:01:39 GMT
USER root
```

-	Layers:
	-	`sha256:506ce31776365fae45515fb4603e1b4cd9f533160c24bb2a7a51662fbf43622c`  
		Last Modified: Mon, 20 Apr 2026 08:04:44 GMT  
		Size: 40.0 MB (40016295 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca40519c7dfd99a5d3b9acf4887465a30e4d4d6a28eab86d412410efb4d4a0b2`  
		Last Modified: Mon, 20 Apr 2026 23:06:40 GMT  
		Size: 30.4 MB (30366915 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5586b9e564b8c72cfa54fb596874e91a0c0171d5afbd905ed64613f5cf52c710`  
		Last Modified: Mon, 20 Apr 2026 23:06:43 GMT  
		Size: 145.6 MB (145637119 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4513f0ba9b76c8fa2734f9e944dfc4009d3cb3ae7460cc609f94177dc93d0ae`  
		Last Modified: Mon, 20 Apr 2026 23:06:38 GMT  
		Size: 130.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f50d31652564b110e78ad9a1b13e0e83479b13c640148aed749f0e2071233655`  
		Last Modified: Mon, 20 Apr 2026 23:06:39 GMT  
		Size: 2.3 KB (2290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10c50e66a04a7941e80af0f475c748f2b0b4a01a7d183e221cdf2f6e346daac5`  
		Last Modified: Tue, 21 Apr 2026 00:01:55 GMT  
		Size: 1.7 KB (1710 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4902998a8968f910c9978063b3b5fbf83a5f2b1379abb241917dd33e16c40ae`  
		Last Modified: Tue, 21 Apr 2026 00:01:58 GMT  
		Size: 36.7 MB (36692381 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a559132733db884433f8614a8ccf53209c8036739f23cdc0ae4047080bf7e17`  
		Last Modified: Tue, 21 Apr 2026 00:02:02 GMT  
		Size: 137.8 MB (137808334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:301a7b2a1908440e20b9bdca583ff8238b90cba1d931dfa584cf38095ec8f77a`  
		Last Modified: Tue, 21 Apr 2026 00:01:57 GMT  
		Size: 25.6 KB (25611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:9-jdk17-ubi9` - unknown; unknown

```console
$ docker pull gradle@sha256:29100fbee67e4ab749c2e6f70f2ac8909d3885efb8ce8b5d403d3b3d9440e439
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5412254 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e6126f47bee1cfb3d023810fc349a617568e24a0a4f58eb7990b4c685863aa5`

```dockerfile
```

-	Layers:
	-	`sha256:03027de4d7d5cba58fc37934a882d70d5c33d51609a98e565afae1888cbae9b4`  
		Last Modified: Tue, 21 Apr 2026 00:01:56 GMT  
		Size: 5.4 MB (5389058 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fb653918e64511518505ad2d2ba2101ca51d6ab1760c1ed7dc5a44c4fb504391`  
		Last Modified: Tue, 21 Apr 2026 00:01:56 GMT  
		Size: 23.2 KB (23196 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:9-jdk17-ubi9` - linux; arm64 variant v8

```console
$ docker pull gradle@sha256:99ab20b270105cad109b96e7467f72913419b0f8531b9a09c0adf202fd335261
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **387.3 MB (387314038 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7f71902449a1a25b81ef706cbd6c7c1b9b2fc59bedc4d5239da83b27b7ed9d5c`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["gradle"]`

```dockerfile
# Mon, 20 Apr 2026 00:49:28 GMT
LABEL maintainer="Red Hat, Inc."
# Mon, 20 Apr 2026 00:49:28 GMT
LABEL vendor="Red Hat, Inc."
# Mon, 20 Apr 2026 00:49:28 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Mon, 20 Apr 2026 00:49:28 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.7"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Mon, 20 Apr 2026 00:49:28 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Mon, 20 Apr 2026 00:49:28 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Mon, 20 Apr 2026 00:49:28 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 20 Apr 2026 00:49:28 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 20 Apr 2026 00:49:28 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Mon, 20 Apr 2026 00:49:28 GMT
LABEL io.openshift.expose-services=""
# Mon, 20 Apr 2026 00:49:28 GMT
LABEL io.openshift.tags="minimal rhel9"
# Mon, 20 Apr 2026 00:49:28 GMT
ENV container oci
# Mon, 20 Apr 2026 00:49:29 GMT
COPY dir:2db86b8c6d033296a751d728266ea755c08c1579f6b374a8f32773f7c153c4a3 in /      
# Mon, 20 Apr 2026 00:49:29 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Mon, 20 Apr 2026 00:49:29 GMT
CMD ["/bin/bash"]
# Mon, 20 Apr 2026 00:49:29 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /usr/share/buildinfo/content-sets.json      
# Mon, 20 Apr 2026 00:49:29 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /root/buildinfo/content_manifests/content-sets.json      
# Mon, 20 Apr 2026 00:49:29 GMT
COPY file:74d0fd4df8d5867dbb736f15eb7a260d4e3e75a29dc48c257ee3c5fddc6b08bc in /usr/share/buildinfo/labels.json      
# Mon, 20 Apr 2026 00:49:29 GMT
COPY file:74d0fd4df8d5867dbb736f15eb7a260d4e3e75a29dc48c257ee3c5fddc6b08bc in /root/buildinfo/labels.json      
# Mon, 20 Apr 2026 00:49:30 GMT
LABEL "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="0bc61a274edddc1467c2ad0ddc3139543c4da4da" "org.opencontainers.image.revision"="0bc61a274edddc1467c2ad0ddc3139543c4da4da" "build-date"="2026-04-20T00:49:15Z" "org.opencontainers.image.created"="2026-04-20T00:49:15Z" "release"="1776645941"org.opencontainers.image.revision=0bc61a274edddc1467c2ad0ddc3139543c4da4da,org.opencontainers.image.created=2026-04-20T00:49:15Z
# Mon, 20 Apr 2026 23:02:12 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 20 Apr 2026 23:02:12 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 20 Apr 2026 23:02:12 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 20 Apr 2026 23:02:12 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en     ;     microdnf clean all # buildkit
# Mon, 20 Apr 2026 23:02:12 GMT
ENV JAVA_VERSION=jdk-17.0.18+8
# Mon, 20 Apr 2026 23:03:28 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='592a6702b3a07a0e0b82cb38aaab149bfce1b0c24d6b57ddb410bd9009333095';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jdk_aarch64_linux_hotspot_17.0.18_8.tar.gz';          ;;        ppc64le)          ESUM='5ab89fbde560e1a09386f389dd7881715b896f49c6e9aa974f72d551337dba5e';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jdk_ppc64le_linux_hotspot_17.0.18_8.tar.gz';          ;;        s390x)          ESUM='3693469655bcfa2fa5e70907245a2b3bc4236db7d9fa1b9feb0ab7abd235da09';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jdk_s390x_linux_hotspot_17.0.18_8.tar.gz';          ;;        x86_64)          ESUM='0c94cbb54325c40dcf026143eb621562017db5525727f2d9131a11250f72c450';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jdk_x64_linux_hotspot_17.0.18_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Mon, 20 Apr 2026 23:03:29 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Mon, 20 Apr 2026 23:03:29 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Mon, 20 Apr 2026 23:03:29 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Mon, 20 Apr 2026 23:03:29 GMT
CMD ["jshell"]
# Mon, 20 Apr 2026 23:14:20 GMT
CMD ["gradle"]
# Mon, 20 Apr 2026 23:14:20 GMT
ENV GRADLE_HOME=/opt/gradle
# Mon, 20 Apr 2026 23:14:20 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 101 gradle     && useradd --system --gid gradle --uid 101 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Mon, 20 Apr 2026 23:14:20 GMT
VOLUME [/home/gradle/.gradle]
# Mon, 20 Apr 2026 23:14:20 GMT
WORKDIR /home/gradle
# Mon, 20 Apr 2026 23:14:24 GMT
RUN set -o errexit -o nounset     && microdnf install -y         make         curl-minimal         wget         tar                 findutils                 unzip         which                 git         git-lfs         subversion     && microdnf clean all         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which svn # buildkit
# Mon, 20 Apr 2026 23:14:24 GMT
ENV GRADLE_VERSION=9.4.1
# Mon, 20 Apr 2026 23:14:24 GMT
ARG GRADLE_DOWNLOAD_SHA256=2ab2958f2a1e51120c326cad6f385153bb11ee93b3c216c5fccebfdfbb7ec6cb
# Mon, 20 Apr 2026 23:14:27 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=2ab2958f2a1e51120c326cad6f385153bb11ee93b3c216c5fccebfdfbb7ec6cb
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Mon, 20 Apr 2026 23:14:27 GMT
USER gradle
# Mon, 20 Apr 2026 23:14:28 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=2ab2958f2a1e51120c326cad6f385153bb11ee93b3c216c5fccebfdfbb7ec6cb
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --stacktrace --debug --version # buildkit
# Mon, 20 Apr 2026 23:14:28 GMT
USER root
```

-	Layers:
	-	`sha256:e8debca61d243d998bf3bf52e935df4db45aecedd074c5f013abc40fd316c45f`  
		Last Modified: Mon, 20 Apr 2026 08:07:44 GMT  
		Size: 38.2 MB (38200123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1c0c0164a66cc90978094bc89f38b831bba2bdea363b5b4770ba1e73ba24af7`  
		Last Modified: Mon, 20 Apr 2026 23:02:31 GMT  
		Size: 30.8 MB (30798063 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e28a814a3ae4708388cfb0bbdc05be047cb7b1fe6d68f1945f470fa49a5eac4`  
		Last Modified: Mon, 20 Apr 2026 23:03:48 GMT  
		Size: 144.4 MB (144446554 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c91abe0f05e5b9681822ba2392097829ece297fe6c1df4ff55735a41d016c12`  
		Last Modified: Mon, 20 Apr 2026 23:03:44 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9832f50280c505732017ab0f4e69b87e18d4b075e299c688f84961ad505b6275`  
		Last Modified: Mon, 20 Apr 2026 23:03:45 GMT  
		Size: 2.3 KB (2289 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7789d5d6e5b5412478dda69dc559780a5f823572b7e9876ccd1e2bcc39f53d0b`  
		Last Modified: Mon, 20 Apr 2026 23:14:44 GMT  
		Size: 1.7 KB (1709 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3358ba8ee511ab5fce927d6070a0bb81653238898ed06df0fcb55d78d3b45d4`  
		Last Modified: Mon, 20 Apr 2026 23:14:45 GMT  
		Size: 36.0 MB (36027451 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f493f3ff4ea3f3b4c23cb1ffca19e799e0e926dbc30a0e7e3f5e2e6bd247d55c`  
		Last Modified: Mon, 20 Apr 2026 23:14:47 GMT  
		Size: 137.8 MB (137808338 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3dd1f84b4d80bef74fc47b6777a134d0c6bd9264e88fcbf32d71b5165662fa1`  
		Last Modified: Mon, 20 Apr 2026 23:14:44 GMT  
		Size: 29.4 KB (29350 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:9-jdk17-ubi9` - unknown; unknown

```console
$ docker pull gradle@sha256:10f3adc48a1ed9ac0fb5cbb129e5bd5e3204c7db83c8a80e0ea59648f7d3adb6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5411821 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e274bd38494cb6fb4e1e34d2e3d5651b732b26a9cb7cb1bccbeb46124f2f2887`

```dockerfile
```

-	Layers:
	-	`sha256:4263428a5af5b12d668efdbf309cb793f3d936a967c4445719f6aabb80bce0ea`  
		Last Modified: Mon, 20 Apr 2026 23:14:44 GMT  
		Size: 5.4 MB (5388440 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:169078a753fc998ddce6c13df66b12a90cb2ac0bf2b698e66a0a01f5b140196a`  
		Last Modified: Mon, 20 Apr 2026 23:14:43 GMT  
		Size: 23.4 KB (23381 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:9-jdk17-ubi9` - linux; ppc64le

```console
$ docker pull gradle@sha256:9cd6e7d2473c1d1cf9c2c138555fe8839101968371585f35e962e65fc6fcbf4a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **398.5 MB (398492433 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ab9a2fc0d7e164a51d2df53088ab73e296543c2e39e5aa13fea0c3505a1e053`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["gradle"]`

```dockerfile
# Mon, 20 Apr 2026 00:48:23 GMT
LABEL maintainer="Red Hat, Inc."
# Mon, 20 Apr 2026 00:48:23 GMT
LABEL vendor="Red Hat, Inc."
# Mon, 20 Apr 2026 00:48:23 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Mon, 20 Apr 2026 00:48:23 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.7"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Mon, 20 Apr 2026 00:48:23 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Mon, 20 Apr 2026 00:48:23 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Mon, 20 Apr 2026 00:48:23 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 20 Apr 2026 00:48:23 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 20 Apr 2026 00:48:23 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Mon, 20 Apr 2026 00:48:23 GMT
LABEL io.openshift.expose-services=""
# Mon, 20 Apr 2026 00:48:23 GMT
LABEL io.openshift.tags="minimal rhel9"
# Mon, 20 Apr 2026 00:48:23 GMT
ENV container oci
# Mon, 20 Apr 2026 00:48:24 GMT
COPY dir:8240d23726e865ba51f291ba4ea188782a75a0af67ec349dc8d9d3bc145ecd05 in /      
# Mon, 20 Apr 2026 00:48:24 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Mon, 20 Apr 2026 00:48:24 GMT
CMD ["/bin/bash"]
# Mon, 20 Apr 2026 00:48:24 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /usr/share/buildinfo/content-sets.json      
# Mon, 20 Apr 2026 00:48:24 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /root/buildinfo/content_manifests/content-sets.json      
# Mon, 20 Apr 2026 00:48:24 GMT
COPY file:54c55160da8e94b0ed06988eaccac768df07b2ab8418806d9245b992ab4c1444 in /usr/share/buildinfo/labels.json      
# Mon, 20 Apr 2026 00:48:24 GMT
COPY file:54c55160da8e94b0ed06988eaccac768df07b2ab8418806d9245b992ab4c1444 in /root/buildinfo/labels.json      
# Mon, 20 Apr 2026 00:48:25 GMT
LABEL "architecture"="ppc64le" "vcs-type"="git" "vcs-ref"="0bc61a274edddc1467c2ad0ddc3139543c4da4da" "org.opencontainers.image.revision"="0bc61a274edddc1467c2ad0ddc3139543c4da4da" "build-date"="2026-04-20T00:48:13Z" "org.opencontainers.image.created"="2026-04-20T00:48:13Z" "release"="1776645941"org.opencontainers.image.revision=0bc61a274edddc1467c2ad0ddc3139543c4da4da,org.opencontainers.image.created=2026-04-20T00:48:13Z
# Mon, 20 Apr 2026 23:00:52 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 20 Apr 2026 23:00:52 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 20 Apr 2026 23:00:52 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 20 Apr 2026 23:00:52 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en     ;     microdnf clean all # buildkit
# Mon, 20 Apr 2026 23:00:52 GMT
ENV JAVA_VERSION=jdk-17.0.18+8
# Mon, 20 Apr 2026 23:04:49 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='592a6702b3a07a0e0b82cb38aaab149bfce1b0c24d6b57ddb410bd9009333095';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jdk_aarch64_linux_hotspot_17.0.18_8.tar.gz';          ;;        ppc64le)          ESUM='5ab89fbde560e1a09386f389dd7881715b896f49c6e9aa974f72d551337dba5e';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jdk_ppc64le_linux_hotspot_17.0.18_8.tar.gz';          ;;        s390x)          ESUM='3693469655bcfa2fa5e70907245a2b3bc4236db7d9fa1b9feb0ab7abd235da09';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jdk_s390x_linux_hotspot_17.0.18_8.tar.gz';          ;;        x86_64)          ESUM='0c94cbb54325c40dcf026143eb621562017db5525727f2d9131a11250f72c450';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jdk_x64_linux_hotspot_17.0.18_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Mon, 20 Apr 2026 23:04:53 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Mon, 20 Apr 2026 23:04:54 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Mon, 20 Apr 2026 23:04:54 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Mon, 20 Apr 2026 23:04:54 GMT
CMD ["jshell"]
# Mon, 20 Apr 2026 23:17:58 GMT
CMD ["gradle"]
# Mon, 20 Apr 2026 23:17:58 GMT
ENV GRADLE_HOME=/opt/gradle
# Mon, 20 Apr 2026 23:17:58 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 101 gradle     && useradd --system --gid gradle --uid 101 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Mon, 20 Apr 2026 23:17:58 GMT
VOLUME [/home/gradle/.gradle]
# Mon, 20 Apr 2026 23:17:59 GMT
WORKDIR /home/gradle
# Mon, 20 Apr 2026 23:18:13 GMT
RUN set -o errexit -o nounset     && microdnf install -y         make         curl-minimal         wget         tar                 findutils                 unzip         which                 git         git-lfs         subversion     && microdnf clean all         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which svn # buildkit
# Mon, 20 Apr 2026 23:18:13 GMT
ENV GRADLE_VERSION=9.4.1
# Mon, 20 Apr 2026 23:18:13 GMT
ARG GRADLE_DOWNLOAD_SHA256=2ab2958f2a1e51120c326cad6f385153bb11ee93b3c216c5fccebfdfbb7ec6cb
# Mon, 20 Apr 2026 23:18:18 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=2ab2958f2a1e51120c326cad6f385153bb11ee93b3c216c5fccebfdfbb7ec6cb
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Mon, 20 Apr 2026 23:18:18 GMT
USER gradle
# Mon, 20 Apr 2026 23:18:20 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=2ab2958f2a1e51120c326cad6f385153bb11ee93b3c216c5fccebfdfbb7ec6cb
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --stacktrace --debug --version # buildkit
# Mon, 20 Apr 2026 23:18:20 GMT
USER root
```

-	Layers:
	-	`sha256:9d0996bd7c74d1634fd0ba1753a8f74e86b97c5b41318f888d6b7bcc768131db`  
		Last Modified: Mon, 20 Apr 2026 12:13:59 GMT  
		Size: 44.4 MB (44443917 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:242b1bfcc64f23f4a2cc6ba069104831d0f144abd63cec2aa7e370ca093096b9`  
		Last Modified: Mon, 20 Apr 2026 23:01:35 GMT  
		Size: 32.8 MB (32848454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:082ff469cbb8d93d911870a5bf1b3cefbef1fa1bc4359a18fd8590fb9aca117e`  
		Last Modified: Mon, 20 Apr 2026 23:05:34 GMT  
		Size: 145.5 MB (145459979 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a718dbfc0e00f28acba01f504a7b31b798b1de252edd60c75230f9bb582b510`  
		Last Modified: Mon, 20 Apr 2026 23:05:31 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4862009d1663471eec2b3369c026649e4b922bd836be18d1f6017106c7158057`  
		Last Modified: Mon, 20 Apr 2026 23:05:31 GMT  
		Size: 2.3 KB (2292 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63b38747f6301e550b40d405d263adcb6b4c316079534e1a6e0eb625d9aa82af`  
		Last Modified: Mon, 20 Apr 2026 23:18:58 GMT  
		Size: 1.7 KB (1709 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05aba31a19de537db17bc734d0f57da1c7ec33965ab7a144caa930d562d0ecbe`  
		Last Modified: Mon, 20 Apr 2026 23:19:00 GMT  
		Size: 37.9 MB (37927206 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2131eab1f2df9a6d856a6d2f69fa6e72feb81d802b765079a73c61f2a7c42585`  
		Last Modified: Mon, 20 Apr 2026 23:19:03 GMT  
		Size: 137.8 MB (137808337 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a7c511086dcdbf29c3df2ec148d215844a334c29d5a5d4759766d680016248e`  
		Last Modified: Mon, 20 Apr 2026 23:18:58 GMT  
		Size: 379.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:9-jdk17-ubi9` - unknown; unknown

```console
$ docker pull gradle@sha256:cf456c425f3a7f2bf8e0ad1683b21c73f46602140d7d2997066d97d298d85a11
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5409648 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:818ded59b21756c5545afe0f8d330ddee150cf1e4756076beefb3abb70f6e8e2`

```dockerfile
```

-	Layers:
	-	`sha256:fe224cd2222193c77473087a37af2250bb559434643bef0c3327f07cbd3242df`  
		Last Modified: Mon, 20 Apr 2026 23:18:58 GMT  
		Size: 5.4 MB (5386369 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e1e4536f54240c99000577f3daaf0c2aa3946a0fb957d177f8a1a00a82003735`  
		Last Modified: Mon, 20 Apr 2026 23:18:58 GMT  
		Size: 23.3 KB (23279 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:9-jdk17-ubi9` - linux; s390x

```console
$ docker pull gradle@sha256:c0414ebc75912444d3db8aaaeda1694346cc344cba8323b0cd8f828f515fdbb4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **378.3 MB (378274559 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2670059ef53d3c30c1e710d10020a0816e4d963e2948094154a7b3b9fd497bc4`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["gradle"]`

```dockerfile
# Mon, 20 Apr 2026 00:51:15 GMT
LABEL maintainer="Red Hat, Inc."
# Mon, 20 Apr 2026 00:51:15 GMT
LABEL vendor="Red Hat, Inc."
# Mon, 20 Apr 2026 00:51:15 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Mon, 20 Apr 2026 00:51:15 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.7"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Mon, 20 Apr 2026 00:51:15 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Mon, 20 Apr 2026 00:51:15 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Mon, 20 Apr 2026 00:51:15 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 20 Apr 2026 00:51:15 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 20 Apr 2026 00:51:15 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Mon, 20 Apr 2026 00:51:15 GMT
LABEL io.openshift.expose-services=""
# Mon, 20 Apr 2026 00:51:15 GMT
LABEL io.openshift.tags="minimal rhel9"
# Mon, 20 Apr 2026 00:51:15 GMT
ENV container oci
# Mon, 20 Apr 2026 00:51:15 GMT
COPY dir:b4a1afe8106f1085d0935fb4f5d1d721db68a582913c2d55b2d9aaa1600bd93e in /      
# Mon, 20 Apr 2026 00:51:16 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Mon, 20 Apr 2026 00:51:16 GMT
CMD ["/bin/bash"]
# Mon, 20 Apr 2026 00:51:16 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /usr/share/buildinfo/content-sets.json      
# Mon, 20 Apr 2026 00:51:16 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /root/buildinfo/content_manifests/content-sets.json      
# Mon, 20 Apr 2026 00:51:16 GMT
COPY file:3dec04e5e5d89154231655b5548184917b8c190a374813ff448dab4392492998 in /usr/share/buildinfo/labels.json      
# Mon, 20 Apr 2026 00:51:16 GMT
COPY file:3dec04e5e5d89154231655b5548184917b8c190a374813ff448dab4392492998 in /root/buildinfo/labels.json      
# Mon, 20 Apr 2026 00:51:16 GMT
LABEL "architecture"="s390x" "vcs-type"="git" "vcs-ref"="0bc61a274edddc1467c2ad0ddc3139543c4da4da" "org.opencontainers.image.revision"="0bc61a274edddc1467c2ad0ddc3139543c4da4da" "build-date"="2026-04-20T00:51:04Z" "org.opencontainers.image.created"="2026-04-20T00:51:04Z" "release"="1776645941"org.opencontainers.image.revision=0bc61a274edddc1467c2ad0ddc3139543c4da4da,org.opencontainers.image.created=2026-04-20T00:51:04Z
# Mon, 20 Apr 2026 23:04:26 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 20 Apr 2026 23:04:26 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 20 Apr 2026 23:04:26 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 20 Apr 2026 23:04:26 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en     ;     microdnf clean all # buildkit
# Mon, 20 Apr 2026 23:04:26 GMT
ENV JAVA_VERSION=jdk-17.0.18+8
# Mon, 20 Apr 2026 23:09:16 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='592a6702b3a07a0e0b82cb38aaab149bfce1b0c24d6b57ddb410bd9009333095';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jdk_aarch64_linux_hotspot_17.0.18_8.tar.gz';          ;;        ppc64le)          ESUM='5ab89fbde560e1a09386f389dd7881715b896f49c6e9aa974f72d551337dba5e';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jdk_ppc64le_linux_hotspot_17.0.18_8.tar.gz';          ;;        s390x)          ESUM='3693469655bcfa2fa5e70907245a2b3bc4236db7d9fa1b9feb0ab7abd235da09';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jdk_s390x_linux_hotspot_17.0.18_8.tar.gz';          ;;        x86_64)          ESUM='0c94cbb54325c40dcf026143eb621562017db5525727f2d9131a11250f72c450';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jdk_x64_linux_hotspot_17.0.18_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Mon, 20 Apr 2026 23:09:25 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Mon, 20 Apr 2026 23:09:29 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Mon, 20 Apr 2026 23:09:29 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Mon, 20 Apr 2026 23:09:29 GMT
CMD ["jshell"]
# Tue, 21 Apr 2026 00:05:06 GMT
CMD ["gradle"]
# Tue, 21 Apr 2026 00:05:06 GMT
ENV GRADLE_HOME=/opt/gradle
# Tue, 21 Apr 2026 00:05:06 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 101 gradle     && useradd --system --gid gradle --uid 101 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Tue, 21 Apr 2026 00:05:06 GMT
VOLUME [/home/gradle/.gradle]
# Tue, 21 Apr 2026 00:05:07 GMT
WORKDIR /home/gradle
# Tue, 21 Apr 2026 00:06:33 GMT
RUN set -o errexit -o nounset     && microdnf install -y         make         curl-minimal         wget         tar                 findutils                 unzip         which                 git         git-lfs         subversion     && microdnf clean all         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which svn # buildkit
# Tue, 21 Apr 2026 00:06:33 GMT
ENV GRADLE_VERSION=9.4.1
# Tue, 21 Apr 2026 00:06:33 GMT
ARG GRADLE_DOWNLOAD_SHA256=2ab2958f2a1e51120c326cad6f385153bb11ee93b3c216c5fccebfdfbb7ec6cb
# Tue, 21 Apr 2026 00:06:51 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=2ab2958f2a1e51120c326cad6f385153bb11ee93b3c216c5fccebfdfbb7ec6cb
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Tue, 21 Apr 2026 00:06:51 GMT
USER gradle
# Tue, 21 Apr 2026 00:06:56 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=2ab2958f2a1e51120c326cad6f385153bb11ee93b3c216c5fccebfdfbb7ec6cb
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --stacktrace --debug --version # buildkit
# Tue, 21 Apr 2026 00:06:56 GMT
USER root
```

-	Layers:
	-	`sha256:32c0d17b4c811788343ca79dbd73a2cbd36ad958598e189725c863447313e0d3`  
		Last Modified: Mon, 20 Apr 2026 12:13:49 GMT  
		Size: 38.1 MB (38114922 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd300f82eb1e8ecf5492fb727d38ad64a99b25f79e39a70bc453a3b2d46ba5a7`  
		Last Modified: Mon, 20 Apr 2026 23:06:58 GMT  
		Size: 30.4 MB (30388716 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:615796b357e798f1e714bc51ac74a158e5f08465460035b7e303b9fd6cba0e6d`  
		Last Modified: Mon, 20 Apr 2026 23:11:43 GMT  
		Size: 135.6 MB (135629100 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d560c14beffa44139e9725bab024db18b83466a01c52e1a4bf8ef303b8f9dd31`  
		Last Modified: Mon, 20 Apr 2026 23:11:24 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d11636bae8af6d1a553c601f4a967e825dea4e4c6de3e90d0135bad528da7ecd`  
		Last Modified: Mon, 20 Apr 2026 23:11:25 GMT  
		Size: 2.3 KB (2292 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdb163d3281a9211445bb38861f3bc905964b4761e9d8589c294903992d8a0d2`  
		Last Modified: Tue, 21 Apr 2026 00:08:25 GMT  
		Size: 1.7 KB (1715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd46a55f0fb5bce2a0c17ec134eb5294366306eb0629702d3a92bda374614abc`  
		Last Modified: Tue, 21 Apr 2026 00:08:32 GMT  
		Size: 36.3 MB (36328935 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d588690e4f3825273eba25e6023511e21c900757ebcb934f9273ef0053ce59b7`  
		Last Modified: Tue, 21 Apr 2026 00:08:35 GMT  
		Size: 137.8 MB (137808341 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ae1878425f73f7bf1aaae62c8d12376cb2b3753a604fee167dee691e7f02cd3`  
		Last Modified: Tue, 21 Apr 2026 00:08:24 GMT  
		Size: 377.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:9-jdk17-ubi9` - unknown; unknown

```console
$ docker pull gradle@sha256:09e56fe4b728e1e6dafe4d31140b1136174808dafcf2155c0333f57bb23c20a2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5398893 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f298df6a669f8a08c7d9af5b7effc1426f545c36ffe52ce315677005478cbc29`

```dockerfile
```

-	Layers:
	-	`sha256:a01c25e7943de96053668bbc011b80af61021057213062313403210122338a3e`  
		Last Modified: Tue, 21 Apr 2026 00:08:27 GMT  
		Size: 5.4 MB (5375663 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1b5d557dc0938b2c9fcccb2aa3809ffefaabc464e13fb53b4f2a94e5da1735d5`  
		Last Modified: Tue, 21 Apr 2026 00:08:24 GMT  
		Size: 23.2 KB (23230 bytes)  
		MIME: application/vnd.in-toto+json
