## `gradle:7-jdk8-ubi9`

```console
$ docker pull gradle@sha256:67c172d756cc7c819055cc1f1ce603e33d98d69c1505dcaa8989276031237bbc
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `gradle:7-jdk8-ubi9` - linux; amd64

```console
$ docker pull gradle@sha256:49eabea8a1690d2115bb200a6eb03f039f3dbf1a6b6c9493f621de85079b2c11
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **290.8 MB (290779760 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac1b7a7dbba4f848a75661f73fcd6df5af736ac2d7072867dfcfca7d9bce78f9`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["gradle"]`

```dockerfile
# Mon, 13 Apr 2026 18:26:37 GMT
LABEL maintainer="Red Hat, Inc."
# Mon, 13 Apr 2026 18:26:37 GMT
LABEL vendor="Red Hat, Inc."
# Mon, 13 Apr 2026 18:26:37 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Mon, 13 Apr 2026 18:26:37 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.7"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Mon, 13 Apr 2026 18:26:37 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Mon, 13 Apr 2026 18:26:37 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Mon, 13 Apr 2026 18:26:37 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 13 Apr 2026 18:26:37 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 13 Apr 2026 18:26:37 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Mon, 13 Apr 2026 18:26:37 GMT
LABEL io.openshift.expose-services=""
# Mon, 13 Apr 2026 18:26:37 GMT
LABEL io.openshift.tags="minimal rhel9"
# Mon, 13 Apr 2026 18:26:37 GMT
ENV container oci
# Mon, 13 Apr 2026 18:26:38 GMT
COPY dir:5191e1ce97881b91cd281225b61de5b907dbc286c69b6681e228608a9d6bab0b in /      
# Mon, 13 Apr 2026 18:26:38 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Mon, 13 Apr 2026 18:26:38 GMT
CMD ["/bin/bash"]
# Mon, 13 Apr 2026 18:26:38 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /usr/share/buildinfo/content-sets.json      
# Mon, 13 Apr 2026 18:26:38 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /root/buildinfo/content_manifests/content-sets.json      
# Mon, 13 Apr 2026 18:26:38 GMT
COPY file:22a393f43688b6747c863a4550da665d92705a5e9519cc2d1c97b9f7499127bb in /usr/share/buildinfo/labels.json      
# Mon, 13 Apr 2026 18:26:38 GMT
COPY file:22a393f43688b6747c863a4550da665d92705a5e9519cc2d1c97b9f7499127bb in /root/buildinfo/labels.json      
# Mon, 13 Apr 2026 18:26:39 GMT
LABEL "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="49cc6237764cacc4684bc968dd9fc53fb8abd12c" "org.opencontainers.image.revision"="49cc6237764cacc4684bc968dd9fc53fb8abd12c" "build-date"="2026-04-13T18:26:26Z" "org.opencontainers.image.created"="2026-04-13T18:26:26Z" "release"="1776104705"org.opencontainers.image.revision=49cc6237764cacc4684bc968dd9fc53fb8abd12c,org.opencontainers.image.created=2026-04-13T18:26:26Z
# Tue, 14 Apr 2026 20:45:31 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 14 Apr 2026 20:45:31 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 14 Apr 2026 20:45:31 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 14 Apr 2026 20:45:31 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en     ;     microdnf clean all # buildkit
# Tue, 14 Apr 2026 20:45:31 GMT
ENV JAVA_VERSION=jdk8u482-b08
# Tue, 14 Apr 2026 20:45:35 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='ada72fbf191fb287b4c1e54be372b64c40c27c2ffbfa01f880c92af11f4e7c94';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u482-b08/OpenJDK8U-jdk_aarch64_linux_hotspot_8u482b08.tar.gz';          ;;        ppc64le)          ESUM='e77ba337c3ebb37fbef4961299f13fc4db87996ffd5470bdfb460cfc2ddb6053';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u482-b08/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u482b08.tar.gz';          ;;        x86_64)          ESUM='e74becad56b4cc01f1556a671e578d3788789f5257f9499f6fbed84e63a55ecf';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u482-b08/OpenJDK8U-jdk_x64_linux_hotspot_8u482b08.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip; # buildkit
# Tue, 14 Apr 2026 20:45:35 GMT
RUN set -eux;     echo "Verifying install ...";     echo "javac -version"; javac -version;     echo "java -version"; java -version;     echo "Complete." # buildkit
# Tue, 14 Apr 2026 20:45:35 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 14 Apr 2026 20:45:35 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 14 Apr 2026 21:00:16 GMT
CMD ["gradle"]
# Tue, 14 Apr 2026 21:00:16 GMT
ENV GRADLE_HOME=/opt/gradle
# Tue, 14 Apr 2026 21:00:16 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 101 gradle     && useradd --system --gid gradle --uid 101 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Tue, 14 Apr 2026 21:00:16 GMT
VOLUME [/home/gradle/.gradle]
# Tue, 14 Apr 2026 21:00:16 GMT
WORKDIR /home/gradle
# Tue, 14 Apr 2026 21:00:20 GMT
RUN set -o errexit -o nounset     && microdnf install -y         make                 findutils                 unzip         which                 git         git-lfs         subversion     && microdnf clean all         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which svn # buildkit
# Tue, 14 Apr 2026 21:00:20 GMT
ENV GRADLE_VERSION=7.6.6
# Tue, 14 Apr 2026 21:00:20 GMT
ARG GRADLE_DOWNLOAD_SHA256=673d9776f303bc7048fc3329d232d6ebf1051b07893bd9d11616fad9a8673be0
# Tue, 14 Apr 2026 21:00:54 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=673d9776f303bc7048fc3329d232d6ebf1051b07893bd9d11616fad9a8673be0
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Tue, 14 Apr 2026 21:00:54 GMT
USER gradle
# Tue, 14 Apr 2026 21:00:55 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=673d9776f303bc7048fc3329d232d6ebf1051b07893bd9d11616fad9a8673be0
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Tue, 14 Apr 2026 21:00:55 GMT
USER root
```

-	Layers:
	-	`sha256:b1ed13c5ef0ac6dbcd255a5c1be9e3c9c2903872aa4ae5fa877850a48fdaee26`  
		Last Modified: Mon, 13 Apr 2026 19:17:03 GMT  
		Size: 40.0 MB (40016560 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59a5454c0753beade210064a63915108f68d4a2aa79598a76cd9ad9955284bce`  
		Last Modified: Tue, 14 Apr 2026 20:45:48 GMT  
		Size: 30.4 MB (30369685 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4780b7b1f250206c4ab66fd183ea0ab3c2149904f0abe5db9aaaf07df00042df`  
		Last Modified: Tue, 14 Apr 2026 20:45:49 GMT  
		Size: 55.2 MB (55170654 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc403ba4afeb5234d04ea6f413d21d08f6d791b33f92530f7ed7f0676a1f99b2`  
		Last Modified: Tue, 14 Apr 2026 20:45:44 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:048ab002179e5dc7aaa139532e606e3ad112fd87f8fa2c18287c80ecd8d69a4b`  
		Last Modified: Tue, 14 Apr 2026 20:45:47 GMT  
		Size: 2.3 KB (2317 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ea2f3f82be74accda498d4047dd116a959e86ae5233efb3f53542508045b030`  
		Last Modified: Tue, 14 Apr 2026 21:00:39 GMT  
		Size: 1.7 KB (1707 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3bbbf748659f9fba3c400186a344e8838c4ff5810145e0e191da14ab24dc89d4`  
		Last Modified: Tue, 14 Apr 2026 21:00:41 GMT  
		Size: 36.7 MB (36694365 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a72bec848151f4899202f269f13d16cce0ed2a538b1c9d3c9f71df58d07e48dd`  
		Last Modified: Tue, 14 Apr 2026 21:01:11 GMT  
		Size: 128.5 MB (128469407 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffe7012aca883472ca3849df6325d7d80796f677dffe4dd6e7b75b7a682a1cdf`  
		Last Modified: Tue, 14 Apr 2026 21:01:09 GMT  
		Size: 54.9 KB (54906 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:7-jdk8-ubi9` - unknown; unknown

```console
$ docker pull gradle@sha256:68e187f6466a49ef429b95d55d31e53fe2ec51963481148023b3061a1f38c90b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5459097 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:387f2c887bed6e3de5482b06a3788bd86cc3368b54076cec223ffe72de58b3df`

```dockerfile
```

-	Layers:
	-	`sha256:7dae8602d3975879e3ca7f07b60b41e688d27dba48bbca4e677ac0ae9abdb441`  
		Last Modified: Tue, 14 Apr 2026 21:01:09 GMT  
		Size: 5.4 MB (5435543 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5da57bd5a4eddae8611623afb03ad2cf0e18dfd1a07e4c3d1424f750c9b2997d`  
		Last Modified: Tue, 14 Apr 2026 21:01:08 GMT  
		Size: 23.6 KB (23554 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:7-jdk8-ubi9` - linux; arm64 variant v8

```console
$ docker pull gradle@sha256:c1e1dd33b772c69fada806af576151f389af176e97a53d50f721373b0fc3f49b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **287.8 MB (287808930 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c5e857518d2225c317a4bc597136b7526b990fa832aa747a90849df64964c7c9`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["gradle"]`

```dockerfile
# Mon, 13 Apr 2026 18:28:23 GMT
LABEL maintainer="Red Hat, Inc."
# Mon, 13 Apr 2026 18:28:23 GMT
LABEL vendor="Red Hat, Inc."
# Mon, 13 Apr 2026 18:28:23 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Mon, 13 Apr 2026 18:28:23 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.7"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Mon, 13 Apr 2026 18:28:23 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Mon, 13 Apr 2026 18:28:23 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Mon, 13 Apr 2026 18:28:23 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 13 Apr 2026 18:28:23 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 13 Apr 2026 18:28:23 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Mon, 13 Apr 2026 18:28:23 GMT
LABEL io.openshift.expose-services=""
# Mon, 13 Apr 2026 18:28:23 GMT
LABEL io.openshift.tags="minimal rhel9"
# Mon, 13 Apr 2026 18:28:23 GMT
ENV container oci
# Mon, 13 Apr 2026 18:28:24 GMT
COPY dir:50ceff14380ca413ec2568b248e47effdceffdd30707fc734a4741e902f97450 in /      
# Mon, 13 Apr 2026 18:28:24 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Mon, 13 Apr 2026 18:28:24 GMT
CMD ["/bin/bash"]
# Mon, 13 Apr 2026 18:28:24 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /usr/share/buildinfo/content-sets.json      
# Mon, 13 Apr 2026 18:28:24 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /root/buildinfo/content_manifests/content-sets.json      
# Mon, 13 Apr 2026 18:28:24 GMT
COPY file:20aaf8ce1e0136dca2eb48dbc70df34738ee917c73847beed0478c7b853d8231 in /usr/share/buildinfo/labels.json      
# Mon, 13 Apr 2026 18:28:24 GMT
COPY file:20aaf8ce1e0136dca2eb48dbc70df34738ee917c73847beed0478c7b853d8231 in /root/buildinfo/labels.json      
# Mon, 13 Apr 2026 18:28:24 GMT
LABEL "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="49cc6237764cacc4684bc968dd9fc53fb8abd12c" "org.opencontainers.image.revision"="49cc6237764cacc4684bc968dd9fc53fb8abd12c" "build-date"="2026-04-13T18:28:10Z" "org.opencontainers.image.created"="2026-04-13T18:28:10Z" "release"="1776104705"org.opencontainers.image.revision=49cc6237764cacc4684bc968dd9fc53fb8abd12c,org.opencontainers.image.created=2026-04-13T18:28:10Z
# Tue, 14 Apr 2026 20:45:05 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 14 Apr 2026 20:45:05 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 14 Apr 2026 20:45:05 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 14 Apr 2026 20:45:05 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en     ;     microdnf clean all # buildkit
# Tue, 14 Apr 2026 20:45:05 GMT
ENV JAVA_VERSION=jdk8u482-b08
# Tue, 14 Apr 2026 20:45:09 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='ada72fbf191fb287b4c1e54be372b64c40c27c2ffbfa01f880c92af11f4e7c94';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u482-b08/OpenJDK8U-jdk_aarch64_linux_hotspot_8u482b08.tar.gz';          ;;        ppc64le)          ESUM='e77ba337c3ebb37fbef4961299f13fc4db87996ffd5470bdfb460cfc2ddb6053';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u482-b08/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u482b08.tar.gz';          ;;        x86_64)          ESUM='e74becad56b4cc01f1556a671e578d3788789f5257f9499f6fbed84e63a55ecf';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u482-b08/OpenJDK8U-jdk_x64_linux_hotspot_8u482b08.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip; # buildkit
# Tue, 14 Apr 2026 20:45:10 GMT
RUN set -eux;     echo "Verifying install ...";     echo "javac -version"; javac -version;     echo "java -version"; java -version;     echo "Complete." # buildkit
# Tue, 14 Apr 2026 20:45:10 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 14 Apr 2026 20:45:10 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 14 Apr 2026 20:56:22 GMT
CMD ["gradle"]
# Tue, 14 Apr 2026 20:56:22 GMT
ENV GRADLE_HOME=/opt/gradle
# Tue, 14 Apr 2026 20:56:22 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 101 gradle     && useradd --system --gid gradle --uid 101 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Tue, 14 Apr 2026 20:56:22 GMT
VOLUME [/home/gradle/.gradle]
# Tue, 14 Apr 2026 20:56:22 GMT
WORKDIR /home/gradle
# Tue, 14 Apr 2026 20:56:25 GMT
RUN set -o errexit -o nounset     && microdnf install -y         make                 findutils                 unzip         which                 git         git-lfs         subversion     && microdnf clean all         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which svn # buildkit
# Tue, 14 Apr 2026 20:56:25 GMT
ENV GRADLE_VERSION=7.6.6
# Tue, 14 Apr 2026 20:56:25 GMT
ARG GRADLE_DOWNLOAD_SHA256=673d9776f303bc7048fc3329d232d6ebf1051b07893bd9d11616fad9a8673be0
# Tue, 14 Apr 2026 20:56:28 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=673d9776f303bc7048fc3329d232d6ebf1051b07893bd9d11616fad9a8673be0
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Tue, 14 Apr 2026 20:56:28 GMT
USER gradle
# Tue, 14 Apr 2026 20:56:29 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=673d9776f303bc7048fc3329d232d6ebf1051b07893bd9d11616fad9a8673be0
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Tue, 14 Apr 2026 20:56:29 GMT
USER root
```

-	Layers:
	-	`sha256:f7c1b31b8294524de5dff6550312e7fc2a074a842daad5dd610d9bfdab56527d`  
		Last Modified: Mon, 13 Apr 2026 19:17:00 GMT  
		Size: 38.2 MB (38200105 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c42059e2141194639aa74bba015b498b3a51e3359cfe4e8dc35cd36da94a578`  
		Last Modified: Tue, 14 Apr 2026 20:45:24 GMT  
		Size: 30.8 MB (30797594 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51966ee226c1e26469b0e736cb2937a71efd182d8c0af2af3ecf6cb03839328b`  
		Last Modified: Tue, 14 Apr 2026 20:45:24 GMT  
		Size: 54.3 MB (54252022 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6793765bc755f2b79121257a21cc9430e889f7bdcd7bc2bca6da9b3f11de6ba4`  
		Last Modified: Tue, 14 Apr 2026 20:45:21 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88ff4bdd932405390e7d651d616c546c97f3c25b9081e5567cce08b583b25b56`  
		Last Modified: Tue, 14 Apr 2026 20:45:23 GMT  
		Size: 2.3 KB (2316 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68182b69ea3a84a676ccf450e22cb5237a4254fb459238baa7cce790e5838d06`  
		Last Modified: Tue, 14 Apr 2026 20:56:44 GMT  
		Size: 1.7 KB (1706 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d89585b0f2331d992181490baef9ce7b03842bedb0024900887d0c654cda2fb7`  
		Last Modified: Tue, 14 Apr 2026 20:56:45 GMT  
		Size: 36.0 MB (36026095 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3706df1f72f38e44745f8957ad6f441256fb0436cd1e0cd615ddbf7546b2175`  
		Last Modified: Tue, 14 Apr 2026 20:56:47 GMT  
		Size: 128.5 MB (128469407 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39b21004080624d744931443b4397aad2347a2a6da7cd48b5786526b5e53159a`  
		Last Modified: Tue, 14 Apr 2026 20:56:44 GMT  
		Size: 59.5 KB (59525 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:7-jdk8-ubi9` - unknown; unknown

```console
$ docker pull gradle@sha256:5ce2be86e0926119fa8e55b44d680e0e2ddc9ee83ebc77c973d6c5b4609a96c9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5459380 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:276ad63da24904644c6b568531d57b3bf4e4ba9df5b861c75200f8c1b5a4ff61`

```dockerfile
```

-	Layers:
	-	`sha256:98573fcfc417d2f7ef2d1552c7411704e3f1dd66338d67b021dbcfa614ec91d2`  
		Last Modified: Tue, 14 Apr 2026 20:56:44 GMT  
		Size: 5.4 MB (5435653 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:941f381be85586c8012ac0d81ba82c745de08f6dc62d76141ef38cd6f2769807`  
		Last Modified: Tue, 14 Apr 2026 20:56:44 GMT  
		Size: 23.7 KB (23727 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:7-jdk8-ubi9` - linux; ppc64le

```console
$ docker pull gradle@sha256:b76db8a93fb5fe9c5e5b19d4117cf29a911fa12433c5a59006bd880db0076807
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **296.4 MB (296383742 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae4bc4e1e163358f3c4684bc3da8e5d50c3a11ab234cf385cd7872e1f575e3fa`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["gradle"]`

```dockerfile
# Mon, 13 Apr 2026 18:29:33 GMT
LABEL maintainer="Red Hat, Inc."
# Mon, 13 Apr 2026 18:29:33 GMT
LABEL vendor="Red Hat, Inc."
# Mon, 13 Apr 2026 18:29:33 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Mon, 13 Apr 2026 18:29:33 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.7"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Mon, 13 Apr 2026 18:29:33 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Mon, 13 Apr 2026 18:29:33 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Mon, 13 Apr 2026 18:29:33 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 13 Apr 2026 18:29:33 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 13 Apr 2026 18:29:33 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Mon, 13 Apr 2026 18:29:33 GMT
LABEL io.openshift.expose-services=""
# Mon, 13 Apr 2026 18:29:33 GMT
LABEL io.openshift.tags="minimal rhel9"
# Mon, 13 Apr 2026 18:29:33 GMT
ENV container oci
# Mon, 13 Apr 2026 18:29:34 GMT
COPY dir:24fb0b263f289ef569c594958817053360bec0e0bfe2720b67eb4bf6d63e4515 in /      
# Mon, 13 Apr 2026 18:29:34 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Mon, 13 Apr 2026 18:29:34 GMT
CMD ["/bin/bash"]
# Mon, 13 Apr 2026 18:29:34 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /usr/share/buildinfo/content-sets.json      
# Mon, 13 Apr 2026 18:29:34 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /root/buildinfo/content_manifests/content-sets.json      
# Mon, 13 Apr 2026 18:29:34 GMT
COPY file:7062c8f1fa2df3b89f0d90bf3890fde04fbbd54d614aefabecd07515e8bba176 in /usr/share/buildinfo/labels.json      
# Mon, 13 Apr 2026 18:29:34 GMT
COPY file:7062c8f1fa2df3b89f0d90bf3890fde04fbbd54d614aefabecd07515e8bba176 in /root/buildinfo/labels.json      
# Mon, 13 Apr 2026 18:29:35 GMT
LABEL "architecture"="ppc64le" "vcs-type"="git" "vcs-ref"="49cc6237764cacc4684bc968dd9fc53fb8abd12c" "org.opencontainers.image.revision"="49cc6237764cacc4684bc968dd9fc53fb8abd12c" "build-date"="2026-04-13T18:29:23Z" "org.opencontainers.image.created"="2026-04-13T18:29:23Z" "release"="1776104705"org.opencontainers.image.revision=49cc6237764cacc4684bc968dd9fc53fb8abd12c,org.opencontainers.image.created=2026-04-13T18:29:23Z
# Tue, 14 Apr 2026 20:44:11 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 14 Apr 2026 20:44:11 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 14 Apr 2026 20:44:11 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 14 Apr 2026 20:44:11 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en     ;     microdnf clean all # buildkit
# Tue, 14 Apr 2026 20:44:11 GMT
ENV JAVA_VERSION=jdk8u482-b08
# Tue, 14 Apr 2026 20:44:18 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='ada72fbf191fb287b4c1e54be372b64c40c27c2ffbfa01f880c92af11f4e7c94';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u482-b08/OpenJDK8U-jdk_aarch64_linux_hotspot_8u482b08.tar.gz';          ;;        ppc64le)          ESUM='e77ba337c3ebb37fbef4961299f13fc4db87996ffd5470bdfb460cfc2ddb6053';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u482-b08/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u482b08.tar.gz';          ;;        x86_64)          ESUM='e74becad56b4cc01f1556a671e578d3788789f5257f9499f6fbed84e63a55ecf';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u482-b08/OpenJDK8U-jdk_x64_linux_hotspot_8u482b08.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip; # buildkit
# Tue, 14 Apr 2026 20:44:19 GMT
RUN set -eux;     echo "Verifying install ...";     echo "javac -version"; javac -version;     echo "java -version"; java -version;     echo "Complete." # buildkit
# Tue, 14 Apr 2026 20:44:19 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 14 Apr 2026 20:44:19 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 14 Apr 2026 20:57:47 GMT
CMD ["gradle"]
# Tue, 14 Apr 2026 20:57:47 GMT
ENV GRADLE_HOME=/opt/gradle
# Tue, 14 Apr 2026 20:57:47 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 101 gradle     && useradd --system --gid gradle --uid 101 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Tue, 14 Apr 2026 20:57:47 GMT
VOLUME [/home/gradle/.gradle]
# Tue, 14 Apr 2026 20:57:49 GMT
WORKDIR /home/gradle
# Tue, 14 Apr 2026 20:58:05 GMT
RUN set -o errexit -o nounset     && microdnf install -y         make                 findutils                 unzip         which                 git         git-lfs         subversion     && microdnf clean all         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which svn # buildkit
# Tue, 14 Apr 2026 20:58:05 GMT
ENV GRADLE_VERSION=7.6.6
# Tue, 14 Apr 2026 20:58:05 GMT
ARG GRADLE_DOWNLOAD_SHA256=673d9776f303bc7048fc3329d232d6ebf1051b07893bd9d11616fad9a8673be0
# Tue, 14 Apr 2026 21:00:44 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=673d9776f303bc7048fc3329d232d6ebf1051b07893bd9d11616fad9a8673be0
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Tue, 14 Apr 2026 21:00:44 GMT
USER gradle
# Tue, 14 Apr 2026 21:00:45 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=673d9776f303bc7048fc3329d232d6ebf1051b07893bd9d11616fad9a8673be0
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Tue, 14 Apr 2026 21:00:45 GMT
USER root
```

-	Layers:
	-	`sha256:a8de600aa1d03790e68a950fc8a9160a10a53282e2415c939e6f6e1b5180c553`  
		Last Modified: Tue, 14 Apr 2026 00:13:55 GMT  
		Size: 44.4 MB (44444159 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8eea7503b93e046e3992230236cc9f313ea26fd31522ce2a84d764d8f98a753d`  
		Last Modified: Tue, 14 Apr 2026 20:44:47 GMT  
		Size: 32.8 MB (32849099 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f0588fe833b0bf8694d5c51b4f9e575507dae58fe2b881f48a70c266cbf2516`  
		Last Modified: Tue, 14 Apr 2026 20:44:49 GMT  
		Size: 52.7 MB (52650933 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47f53785dc827bf535af847387154672d757e5cc2febdc38252497e33d10db4f`  
		Last Modified: Tue, 14 Apr 2026 20:44:44 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf56ed70e0c5c6e2b8aaca66de304b481d6d4881c6623a8146a189a4387ac8fc`  
		Last Modified: Tue, 14 Apr 2026 20:44:46 GMT  
		Size: 2.3 KB (2317 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b71087b66eaa2f76f12caf597d5fed16b75f4ab857ee4c7597974fb31fcad209`  
		Last Modified: Tue, 14 Apr 2026 20:58:53 GMT  
		Size: 1.7 KB (1722 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de86b8dab14ab78c85470893159190c3dc7c5005550ac2e3777f56443e576264`  
		Last Modified: Tue, 14 Apr 2026 20:58:55 GMT  
		Size: 37.9 MB (37930923 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:569d31faf1897df278df9e71bf228edc4fb53580fe553c08eeb26507238a717d`  
		Last Modified: Tue, 14 Apr 2026 21:01:18 GMT  
		Size: 128.5 MB (128469419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:974128b21c2a149876dc704230c36b8068df877061b31b62cab643aa3e364aba`  
		Last Modified: Tue, 14 Apr 2026 21:01:15 GMT  
		Size: 35.0 KB (35009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:7-jdk8-ubi9` - unknown; unknown

```console
$ docker pull gradle@sha256:e3767d14adfd513b30df5df1c2ad55200e87d85db87bb2ac77190ba44f4a1897
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5457081 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2be8c4dcca799537d3ad94f9469074a3d70f740e73e898c506211092c2ea6c57`

```dockerfile
```

-	Layers:
	-	`sha256:b65ebed9a5cc6757dcaf8c9c4d69a8f890d5a1f628aa11b123a28af63cd73f67`  
		Last Modified: Tue, 14 Apr 2026 21:01:15 GMT  
		Size: 5.4 MB (5433465 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:783f5bd08c0b26fdb974ebfd5a2bb5d8a6bd8601e94c6a4a892990a9c7a61f38`  
		Last Modified: Tue, 14 Apr 2026 21:01:15 GMT  
		Size: 23.6 KB (23616 bytes)  
		MIME: application/vnd.in-toto+json
