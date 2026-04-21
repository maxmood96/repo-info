## `gradle:6-jdk8-ubi9`

```console
$ docker pull gradle@sha256:13ff26453972a142fb612720aeadefe67679e45e337f82124006cc2ef84768b2
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `gradle:6-jdk8-ubi9` - linux; amd64

```console
$ docker pull gradle@sha256:33f2010a3a93a3ee4b07f6f01e096133123804d5aea0c088cb21436eb2e06b90
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **270.4 MB (270378185 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:42b357c4be2efff3d93566954afeeea793a47ab4c0543a58b816b485fdab4187`
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
# Mon, 20 Apr 2026 23:04:48 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 20 Apr 2026 23:04:48 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 20 Apr 2026 23:04:48 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 20 Apr 2026 23:04:48 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en     ;     microdnf clean all # buildkit
# Mon, 20 Apr 2026 23:04:48 GMT
ENV JAVA_VERSION=jdk8u482-b08
# Mon, 20 Apr 2026 23:04:52 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='ada72fbf191fb287b4c1e54be372b64c40c27c2ffbfa01f880c92af11f4e7c94';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u482-b08/OpenJDK8U-jdk_aarch64_linux_hotspot_8u482b08.tar.gz';          ;;        ppc64le)          ESUM='e77ba337c3ebb37fbef4961299f13fc4db87996ffd5470bdfb460cfc2ddb6053';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u482-b08/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u482b08.tar.gz';          ;;        x86_64)          ESUM='e74becad56b4cc01f1556a671e578d3788789f5257f9499f6fbed84e63a55ecf';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u482-b08/OpenJDK8U-jdk_x64_linux_hotspot_8u482b08.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip; # buildkit
# Mon, 20 Apr 2026 23:04:52 GMT
RUN set -eux;     echo "Verifying install ...";     echo "javac -version"; javac -version;     echo "java -version"; java -version;     echo "Complete." # buildkit
# Mon, 20 Apr 2026 23:04:52 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Mon, 20 Apr 2026 23:04:52 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Mon, 20 Apr 2026 23:18:16 GMT
CMD ["gradle"]
# Mon, 20 Apr 2026 23:18:16 GMT
ENV GRADLE_HOME=/opt/gradle
# Mon, 20 Apr 2026 23:18:16 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 101 gradle     && useradd --system --gid gradle --uid 101 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Mon, 20 Apr 2026 23:18:16 GMT
VOLUME [/home/gradle/.gradle]
# Mon, 20 Apr 2026 23:18:17 GMT
WORKDIR /home/gradle
# Mon, 20 Apr 2026 23:18:21 GMT
RUN set -o errexit -o nounset     && microdnf install -y         make                 findutils                 unzip         which                 git         git-lfs         subversion     && microdnf clean all         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which svn # buildkit
# Mon, 20 Apr 2026 23:18:21 GMT
ENV GRADLE_VERSION=6.9.4
# Mon, 20 Apr 2026 23:18:21 GMT
ARG GRADLE_DOWNLOAD_SHA256=3e240228538de9f18772a574e99a0ba959e83d6ef351014381acd9631781389a
# Mon, 20 Apr 2026 23:18:23 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=3e240228538de9f18772a574e99a0ba959e83d6ef351014381acd9631781389a
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Mon, 20 Apr 2026 23:18:23 GMT
USER gradle
# Mon, 20 Apr 2026 23:18:24 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=3e240228538de9f18772a574e99a0ba959e83d6ef351014381acd9631781389a
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Mon, 20 Apr 2026 23:18:24 GMT
USER root
```

-	Layers:
	-	`sha256:506ce31776365fae45515fb4603e1b4cd9f533160c24bb2a7a51662fbf43622c`  
		Last Modified: Mon, 20 Apr 2026 08:04:44 GMT  
		Size: 40.0 MB (40016295 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8754ca9d635ad77edbfd7556b29116632cfb93e5d36175e5d65bef8202590e75`  
		Last Modified: Mon, 20 Apr 2026 23:05:06 GMT  
		Size: 30.4 MB (30366910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fddd6250af4ed1cf05977c18922aee7d88b91c2298befaae82c25742b043ac6d`  
		Last Modified: Mon, 20 Apr 2026 23:05:07 GMT  
		Size: 55.2 MB (55170682 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec6eb4a0b13e7f77abd8b6a47a5496ad23afc1daf251fb4bcb7ee4bf3525b456`  
		Last Modified: Mon, 20 Apr 2026 23:05:04 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9474c081aebec0c023b2b27f6d71fff098c8230fae1083779461d18a03169124`  
		Last Modified: Mon, 20 Apr 2026 23:05:04 GMT  
		Size: 2.3 KB (2314 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce247da52fa52c96f5fe8ad93ded541d2caa7b935e2aae9dce642a869414a17d`  
		Last Modified: Mon, 20 Apr 2026 23:18:38 GMT  
		Size: 1.7 KB (1709 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56f72aa2823c0d3c1b3292309ab619689466df9b989ea2e5f014f5055538e4ee`  
		Last Modified: Mon, 20 Apr 2026 23:18:40 GMT  
		Size: 36.7 MB (36692167 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2b809509c87c26a4dabdf17d5a847da42220d0bfa548e2574bc683a06b69788`  
		Last Modified: Mon, 20 Apr 2026 23:18:41 GMT  
		Size: 107.7 MB (107696668 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19afcb60bb1e67b71ebc9cdbad059d5e0fcaa749eae57a6595709322ff0922e5`  
		Last Modified: Mon, 20 Apr 2026 23:18:38 GMT  
		Size: 431.3 KB (431280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:6-jdk8-ubi9` - unknown; unknown

```console
$ docker pull gradle@sha256:b1506a159ceec543fab73fc5484d289fd8300aa20a224370490ef472c589d2e1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5441201 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e1abf3f7aca9191274618c0679c4b7460f55acbfacf6f6de36869c6090602153`

```dockerfile
```

-	Layers:
	-	`sha256:190d3d54fdfd6c82b53813cfe53c505750b5885f6cbef230b7e01edea7af9b2c`  
		Last Modified: Mon, 20 Apr 2026 23:18:38 GMT  
		Size: 5.4 MB (5417647 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5ebc9b3a7fe0af0b3e747557eabb852a86c004e9ff5a73c08a999f90d8b71244`  
		Last Modified: Mon, 20 Apr 2026 23:18:38 GMT  
		Size: 23.6 KB (23554 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:6-jdk8-ubi9` - linux; arm64 variant v8

```console
$ docker pull gradle@sha256:f5ec005606c3c40a0b4d6d29534ceaaa629049c4e684c36d4f15ad12b6eff4d3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **267.4 MB (267403659 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0719a5bca696180aa25973662fc823fc967650320b2f604e4ab8988dda8fbcfc`
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
ENV JAVA_VERSION=jdk8u482-b08
# Mon, 20 Apr 2026 23:02:17 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='ada72fbf191fb287b4c1e54be372b64c40c27c2ffbfa01f880c92af11f4e7c94';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u482-b08/OpenJDK8U-jdk_aarch64_linux_hotspot_8u482b08.tar.gz';          ;;        ppc64le)          ESUM='e77ba337c3ebb37fbef4961299f13fc4db87996ffd5470bdfb460cfc2ddb6053';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u482-b08/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u482b08.tar.gz';          ;;        x86_64)          ESUM='e74becad56b4cc01f1556a671e578d3788789f5257f9499f6fbed84e63a55ecf';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u482-b08/OpenJDK8U-jdk_x64_linux_hotspot_8u482b08.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip; # buildkit
# Mon, 20 Apr 2026 23:02:17 GMT
RUN set -eux;     echo "Verifying install ...";     echo "javac -version"; javac -version;     echo "java -version"; java -version;     echo "Complete." # buildkit
# Mon, 20 Apr 2026 23:02:17 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Mon, 20 Apr 2026 23:02:17 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Mon, 20 Apr 2026 23:14:57 GMT
CMD ["gradle"]
# Mon, 20 Apr 2026 23:14:57 GMT
ENV GRADLE_HOME=/opt/gradle
# Mon, 20 Apr 2026 23:14:57 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 101 gradle     && useradd --system --gid gradle --uid 101 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Mon, 20 Apr 2026 23:14:57 GMT
VOLUME [/home/gradle/.gradle]
# Mon, 20 Apr 2026 23:14:57 GMT
WORKDIR /home/gradle
# Mon, 20 Apr 2026 23:15:01 GMT
RUN set -o errexit -o nounset     && microdnf install -y         make                 findutils                 unzip         which                 git         git-lfs         subversion     && microdnf clean all         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which svn # buildkit
# Mon, 20 Apr 2026 23:15:01 GMT
ENV GRADLE_VERSION=6.9.4
# Mon, 20 Apr 2026 23:15:01 GMT
ARG GRADLE_DOWNLOAD_SHA256=3e240228538de9f18772a574e99a0ba959e83d6ef351014381acd9631781389a
# Mon, 20 Apr 2026 23:15:04 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=3e240228538de9f18772a574e99a0ba959e83d6ef351014381acd9631781389a
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Mon, 20 Apr 2026 23:15:04 GMT
USER gradle
# Mon, 20 Apr 2026 23:15:04 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=3e240228538de9f18772a574e99a0ba959e83d6ef351014381acd9631781389a
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Mon, 20 Apr 2026 23:15:04 GMT
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
	-	`sha256:05895880dbaa34b16ea705d659f38e4f47c837778a0fce264b01c10e1100ba08`  
		Last Modified: Mon, 20 Apr 2026 23:02:32 GMT  
		Size: 54.3 MB (54252053 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:767c673ae56a5315e67b900171cd91d6dd88b2b08c0f08a974e8cdd0deb83e16`  
		Last Modified: Mon, 20 Apr 2026 23:02:29 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c15071284e466cbd8b37b7e9f89225285b32c180467f1ce62993dbcfcc74567d`  
		Last Modified: Mon, 20 Apr 2026 23:02:31 GMT  
		Size: 2.3 KB (2314 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db26e371b9a05adccf1fc98e056f63dd28e0a6995e59b5d69c6c159474dcd0db`  
		Last Modified: Mon, 20 Apr 2026 23:15:19 GMT  
		Size: 1.7 KB (1706 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aeab968c9cca5cc2329a54b98c52acb63a9c6288fdaadadded07fcef4c99bb3c`  
		Last Modified: Mon, 20 Apr 2026 23:15:20 GMT  
		Size: 36.0 MB (36027552 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ba9a378134d7b0501f3f1ac618d17400db78b1abe7dfa8a2cb4645480d9273f`  
		Last Modified: Mon, 20 Apr 2026 23:15:22 GMT  
		Size: 107.7 MB (107696669 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:433aeb9774118903cf1003f43bec2144a588105497e9d13ce2dba66d3f50cd2e`  
		Last Modified: Mon, 20 Apr 2026 23:15:19 GMT  
		Size: 425.0 KB (425020 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:6-jdk8-ubi9` - unknown; unknown

```console
$ docker pull gradle@sha256:f453bc570c41cda5a7364ab9403f0fc740987af85591bd8db4105c951227c9af
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5441481 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:73d2699bbaa745c534cd0516207f8af355175a51849f53aedcad414b28164162`

```dockerfile
```

-	Layers:
	-	`sha256:7123d0cea0dcf3c75d97d100d65e438f7be9363d386eb2de1c9905813d667335`  
		Last Modified: Mon, 20 Apr 2026 23:15:19 GMT  
		Size: 5.4 MB (5417753 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b0190a0436384f1621bf38d51fe916534b71bc003a61cb9a90fb60572508633b`  
		Last Modified: Mon, 20 Apr 2026 23:15:19 GMT  
		Size: 23.7 KB (23728 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:6-jdk8-ubi9` - linux; ppc64le

```console
$ docker pull gradle@sha256:a79e84ac962aa09b7004bdf614e8749c03ce8b6ba8db17ebfe5ffffd868432bd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **275.6 MB (275606524 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb5478cd0988d5f42a64188cd08871500c6bee6a7db4784979b0552ba0c5c101`
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
ENV JAVA_VERSION=jdk8u482-b08
# Mon, 20 Apr 2026 23:01:01 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='ada72fbf191fb287b4c1e54be372b64c40c27c2ffbfa01f880c92af11f4e7c94';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u482-b08/OpenJDK8U-jdk_aarch64_linux_hotspot_8u482b08.tar.gz';          ;;        ppc64le)          ESUM='e77ba337c3ebb37fbef4961299f13fc4db87996ffd5470bdfb460cfc2ddb6053';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u482-b08/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u482b08.tar.gz';          ;;        x86_64)          ESUM='e74becad56b4cc01f1556a671e578d3788789f5257f9499f6fbed84e63a55ecf';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u482-b08/OpenJDK8U-jdk_x64_linux_hotspot_8u482b08.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip; # buildkit
# Mon, 20 Apr 2026 23:01:02 GMT
RUN set -eux;     echo "Verifying install ...";     echo "javac -version"; javac -version;     echo "java -version"; java -version;     echo "Complete." # buildkit
# Mon, 20 Apr 2026 23:01:02 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Mon, 20 Apr 2026 23:01:02 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Mon, 20 Apr 2026 23:20:56 GMT
CMD ["gradle"]
# Mon, 20 Apr 2026 23:20:56 GMT
ENV GRADLE_HOME=/opt/gradle
# Mon, 20 Apr 2026 23:20:56 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 101 gradle     && useradd --system --gid gradle --uid 101 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Mon, 20 Apr 2026 23:20:56 GMT
VOLUME [/home/gradle/.gradle]
# Mon, 20 Apr 2026 23:20:57 GMT
WORKDIR /home/gradle
# Mon, 20 Apr 2026 23:21:16 GMT
RUN set -o errexit -o nounset     && microdnf install -y         make                 findutils                 unzip         which                 git         git-lfs         subversion     && microdnf clean all         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which svn # buildkit
# Mon, 20 Apr 2026 23:21:16 GMT
ENV GRADLE_VERSION=6.9.4
# Mon, 20 Apr 2026 23:21:16 GMT
ARG GRADLE_DOWNLOAD_SHA256=3e240228538de9f18772a574e99a0ba959e83d6ef351014381acd9631781389a
# Mon, 20 Apr 2026 23:23:07 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=3e240228538de9f18772a574e99a0ba959e83d6ef351014381acd9631781389a
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Mon, 20 Apr 2026 23:23:07 GMT
USER gradle
# Mon, 20 Apr 2026 23:23:08 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=3e240228538de9f18772a574e99a0ba959e83d6ef351014381acd9631781389a
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Mon, 20 Apr 2026 23:23:08 GMT
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
	-	`sha256:aa0223b5bba3a24a61223e695ef63fb88ada0769d482fef46112476e17c806f1`  
		Last Modified: Mon, 20 Apr 2026 23:01:36 GMT  
		Size: 52.7 MB (52650935 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7af817865ea173c7f075bf41861f64df6f193de215cad24960eb8fcb7b9df9a9`  
		Last Modified: Mon, 20 Apr 2026 23:01:33 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a9c720ef1359090bb4052ef4152e3c095b19e7bc48701b2451ad0f0d0f83cb6`  
		Last Modified: Mon, 20 Apr 2026 23:01:34 GMT  
		Size: 2.3 KB (2317 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf350ffd1558bc4cae54bd344e20137e914aad035ecef32cffa16523bf3db944`  
		Last Modified: Mon, 20 Apr 2026 23:21:59 GMT  
		Size: 1.7 KB (1713 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:119a1de4d7a71df0545e9f7dc10a253c9073be2ac1da790226f0da87851c018b`  
		Last Modified: Mon, 20 Apr 2026 23:22:01 GMT  
		Size: 37.9 MB (37927376 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:faa2f0503d77e77ddec72dedf90c85fe2280dfe2e10b081a7b27ca9728b7826a`  
		Last Modified: Mon, 20 Apr 2026 23:23:44 GMT  
		Size: 107.7 MB (107696666 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22f9b31db2ea2bcf533020d2b1ca105df97e49fc75278de76d9e546b480dba5c`  
		Last Modified: Mon, 20 Apr 2026 23:23:41 GMT  
		Size: 35.0 KB (34985 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:6-jdk8-ubi9` - unknown; unknown

```console
$ docker pull gradle@sha256:e407b6284f54ae29edcb34650b4a80bd15e5938b61c1ff4e34c9a98d6fb23e36
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5439181 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:90fb291e2aeb746fdb0b75ad8f8276f96fd7d910b21ec5645ad2f73649a33a09`

```dockerfile
```

-	Layers:
	-	`sha256:f93c52ff61d65cf5ff7869e7c1c8d6f0f4602139ade20eed725bafbbe900bca9`  
		Last Modified: Mon, 20 Apr 2026 23:23:41 GMT  
		Size: 5.4 MB (5415565 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9951a3a54b6b149950baceaffaced3c8022b7b5e70697c1cc9280c77cd01b774`  
		Last Modified: Mon, 20 Apr 2026 23:23:41 GMT  
		Size: 23.6 KB (23616 bytes)  
		MIME: application/vnd.in-toto+json
