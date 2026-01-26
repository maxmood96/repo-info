## `gradle:8-jdk8-ubi`

```console
$ docker pull gradle@sha256:c2b8f36508b8d5453a2c5a327da801f07117300dc8d4caa9a41e60bf554ab4b9
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `gradle:8-jdk8-ubi` - linux; amd64

```console
$ docker pull gradle@sha256:b0d48d2581df9f0768d0c8cfe574bbdfd18e03313b4ddf37243d69e58d9abdf6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **299.4 MB (299355505 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d9d63d2bf5ea777ff862bd5e088449d891c70417af9e96bcb450915d39b3dcf`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["gradle"]`

```dockerfile
# Mon, 19 Jan 2026 00:54:03 GMT
LABEL maintainer="Red Hat, Inc."
# Mon, 19 Jan 2026 00:54:03 GMT
LABEL vendor="Red Hat, Inc."
# Mon, 19 Jan 2026 00:54:04 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Mon, 19 Jan 2026 00:54:04 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.7"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Mon, 19 Jan 2026 00:54:04 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Mon, 19 Jan 2026 00:54:04 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Mon, 19 Jan 2026 00:54:04 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 19 Jan 2026 00:54:04 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 19 Jan 2026 00:54:04 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Mon, 19 Jan 2026 00:54:04 GMT
LABEL io.openshift.expose-services=""
# Mon, 19 Jan 2026 00:54:05 GMT
LABEL io.openshift.tags="minimal rhel9"
# Mon, 19 Jan 2026 00:54:05 GMT
ENV container oci
# Mon, 19 Jan 2026 00:54:05 GMT
COPY dir:add769031e8da293a85a3b4d1de9d9caa670962dd1067e1e063336823e094054 in /      
# Mon, 19 Jan 2026 00:54:05 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Mon, 19 Jan 2026 00:54:05 GMT
CMD ["/bin/bash"]
# Mon, 19 Jan 2026 00:54:06 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /usr/share/buildinfo/content-sets.json      
# Mon, 19 Jan 2026 00:54:06 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /root/buildinfo/content_manifests/content-sets.json      
# Mon, 19 Jan 2026 00:54:06 GMT
COPY file:e5cdde1c4ba4b2b156fe95664c6aa883d51ceb58bffc4282d8d097d8b741d55b in /usr/share/buildinfo/labels.json      
# Mon, 19 Jan 2026 00:54:06 GMT
COPY file:e5cdde1c4ba4b2b156fe95664c6aa883d51ceb58bffc4282d8d097d8b741d55b in /root/buildinfo/labels.json      
# Mon, 19 Jan 2026 00:54:06 GMT
LABEL "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="d9151f7dd4dfe1cc8a2df524b85cddd483628d5e" "org.opencontainers.image.revision"="d9151f7dd4dfe1cc8a2df524b85cddd483628d5e" "build-date"="2026-01-19T00:53:42Z" "org.opencontainers.image.created"="2026-01-19T00:53:42Z" "release"="1768783948"org.opencontainers.image.revision=d9151f7dd4dfe1cc8a2df524b85cddd483628d5e,org.opencontainers.image.created=2026-01-19T00:53:42Z
# Tue, 20 Jan 2026 19:14:51 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 20 Jan 2026 19:14:51 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 20 Jan 2026 19:14:51 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 20 Jan 2026 19:14:51 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en     ;     microdnf clean all # buildkit
# Tue, 20 Jan 2026 19:14:51 GMT
ENV JAVA_VERSION=jdk8u472-b08
# Tue, 20 Jan 2026 19:14:55 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='e2aff19d85d2441e409d6cbdf12ef7c2acabb0de73bca4207947135dcaa935a2';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u472-b08/OpenJDK8U-jdk_aarch64_linux_hotspot_8u472b08.tar.gz';          ;;        ppc64le)          ESUM='eaf57a4564265583b0641c878bea8943d27ef110c096868f686dae179fb45d8f';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u472-b08/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u472b08.tar.gz';          ;;        x86_64)          ESUM='5becaa4ac660e844c5a39e2ebc39ff5ac824c37ff1b625af8c8b111dc13c3592';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u472-b08/OpenJDK8U-jdk_x64_linux_hotspot_8u472b08.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip; # buildkit
# Tue, 20 Jan 2026 19:14:55 GMT
RUN set -eux;     echo "Verifying install ...";     echo "javac -version"; javac -version;     echo "java -version"; java -version;     echo "Complete." # buildkit
# Tue, 20 Jan 2026 19:14:55 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 20 Jan 2026 19:14:55 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Mon, 26 Jan 2026 19:19:29 GMT
CMD ["gradle"]
# Mon, 26 Jan 2026 19:19:29 GMT
ENV GRADLE_HOME=/opt/gradle
# Mon, 26 Jan 2026 19:19:29 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 101 gradle     && useradd --system --gid gradle --uid 101 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Mon, 26 Jan 2026 19:19:29 GMT
VOLUME [/home/gradle/.gradle]
# Mon, 26 Jan 2026 19:19:29 GMT
WORKDIR /home/gradle
# Mon, 26 Jan 2026 19:19:34 GMT
RUN set -o errexit -o nounset     && microdnf install -y         make                 findutils                 unzip         which                 git         git-lfs         subversion     && microdnf clean all         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which svn # buildkit
# Mon, 26 Jan 2026 19:19:34 GMT
ENV GRADLE_VERSION=8.14.4
# Mon, 26 Jan 2026 19:19:34 GMT
ARG GRADLE_DOWNLOAD_SHA256=f1771298a70f6db5a29daf62378c4e18a17fc33c9ba6b14362e0cdf40610380d
# Mon, 26 Jan 2026 19:19:36 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=f1771298a70f6db5a29daf62378c4e18a17fc33c9ba6b14362e0cdf40610380d
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Mon, 26 Jan 2026 19:19:36 GMT
USER gradle
# Mon, 26 Jan 2026 19:19:37 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=f1771298a70f6db5a29daf62378c4e18a17fc33c9ba6b14362e0cdf40610380d
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Mon, 26 Jan 2026 19:19:37 GMT
USER root
```

-	Layers:
	-	`sha256:8369c500d2f32a6ea3a82d87ee6ca148febba026765ac200615b9de6130b7805`  
		Last Modified: Mon, 19 Jan 2026 05:33:34 GMT  
		Size: 40.0 MB (40033212 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72dd970ddf7b9dbf2f72b498619864718ba33f2b140c78405ec6bad3e4bfe331`  
		Last Modified: Tue, 20 Jan 2026 19:15:09 GMT  
		Size: 30.4 MB (30416135 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a2fa469865e0e04c0a1ae23e2977e49834572a98f2b807158fe084afb8f7ae4`  
		Last Modified: Tue, 20 Jan 2026 19:15:10 GMT  
		Size: 54.7 MB (54733842 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:193e4f6f477523e0e3a40452eb1268279612b34a5052b264a304f56e3fa2b7d4`  
		Last Modified: Tue, 20 Jan 2026 19:15:07 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f124172e5085360c23e7f2f28c75de76ef13a7e6cb6a328e855aab69db7aa4a8`  
		Last Modified: Tue, 20 Jan 2026 19:15:08 GMT  
		Size: 2.3 KB (2314 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:165912c184162fcf69160acd7eea2ea6b422f02e1f809bfb45f65551ba4c5c58`  
		Last Modified: Mon, 26 Jan 2026 19:19:53 GMT  
		Size: 1.7 KB (1712 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5a7ad15bc4ac18830a3f13d962f0a86df297c3fc61bced57d026e7166b5c0a9`  
		Last Modified: Mon, 26 Jan 2026 19:19:55 GMT  
		Size: 36.7 MB (36724959 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24f092482464dc931769884eb0b219c9c9c369f1050efad6e9d86b479f0ec556`  
		Last Modified: Mon, 26 Jan 2026 19:19:57 GMT  
		Size: 137.4 MB (137388272 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8b256402a6805c426d817d340eb4f10fe547b608cab6b002cb099d854b667b2`  
		Last Modified: Mon, 26 Jan 2026 19:19:53 GMT  
		Size: 54.9 KB (54900 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:8-jdk8-ubi` - unknown; unknown

```console
$ docker pull gradle@sha256:c54ee9b59c847d6bf68929567f7b286b460a9bbdb14e022c46bfa0ca69f12398
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5548927 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f608f296d3ef8ba3b114ba18718d4e4d14694fac4bc9146c98bf7f6358697621`

```dockerfile
```

-	Layers:
	-	`sha256:1994fa3eec03c5c896b4bca57a136ee8b338a8f4b2cc1f317e36eecd1829cf97`  
		Last Modified: Mon, 26 Jan 2026 19:19:53 GMT  
		Size: 5.5 MB (5524793 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c7858e138c971ec63edceeab699d5e1007bc4194d28e11a65af31fbec8a0537b`  
		Last Modified: Mon, 26 Jan 2026 19:19:53 GMT  
		Size: 24.1 KB (24134 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:8-jdk8-ubi` - linux; arm64 variant v8

```console
$ docker pull gradle@sha256:53d29180229822ff33b139349b21c65cf93df4f228f405b778abb88ff9de8579
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **296.4 MB (296395599 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c4a0e1859040e5b4edf8f4ca13d6ea7726631946ddcd92cb084665fedc2bbb1`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["gradle"]`

```dockerfile
# Mon, 19 Jan 2026 00:56:35 GMT
LABEL maintainer="Red Hat, Inc."
# Mon, 19 Jan 2026 00:56:35 GMT
LABEL vendor="Red Hat, Inc."
# Mon, 19 Jan 2026 00:56:35 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Mon, 19 Jan 2026 00:56:35 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.7"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Mon, 19 Jan 2026 00:56:35 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Mon, 19 Jan 2026 00:56:35 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Mon, 19 Jan 2026 00:56:35 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 19 Jan 2026 00:56:35 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 19 Jan 2026 00:56:35 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Mon, 19 Jan 2026 00:56:35 GMT
LABEL io.openshift.expose-services=""
# Mon, 19 Jan 2026 00:56:35 GMT
LABEL io.openshift.tags="minimal rhel9"
# Mon, 19 Jan 2026 00:56:35 GMT
ENV container oci
# Mon, 19 Jan 2026 00:56:36 GMT
COPY dir:d1a1d4e8d07e3fe5bb075a89525931e1e2ca1718af0db53956bd13b04036076a in /      
# Mon, 19 Jan 2026 00:56:36 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Mon, 19 Jan 2026 00:56:36 GMT
CMD ["/bin/bash"]
# Mon, 19 Jan 2026 00:56:36 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /usr/share/buildinfo/content-sets.json      
# Mon, 19 Jan 2026 00:56:36 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /root/buildinfo/content_manifests/content-sets.json      
# Mon, 19 Jan 2026 00:56:36 GMT
COPY file:7445748dd3ef455f458b53843ef5c84a205f42d376fb68389e78914c94988e3c in /usr/share/buildinfo/labels.json      
# Mon, 19 Jan 2026 00:56:36 GMT
COPY file:7445748dd3ef455f458b53843ef5c84a205f42d376fb68389e78914c94988e3c in /root/buildinfo/labels.json      
# Mon, 19 Jan 2026 00:56:36 GMT
LABEL "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="d9151f7dd4dfe1cc8a2df524b85cddd483628d5e" "org.opencontainers.image.revision"="d9151f7dd4dfe1cc8a2df524b85cddd483628d5e" "build-date"="2026-01-19T00:56:19Z" "org.opencontainers.image.created"="2026-01-19T00:56:19Z" "release"="1768783948"org.opencontainers.image.revision=d9151f7dd4dfe1cc8a2df524b85cddd483628d5e,org.opencontainers.image.created=2026-01-19T00:56:19Z
# Tue, 20 Jan 2026 19:12:15 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 20 Jan 2026 19:12:15 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 20 Jan 2026 19:12:15 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 20 Jan 2026 19:12:15 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en     ;     microdnf clean all # buildkit
# Tue, 20 Jan 2026 19:12:15 GMT
ENV JAVA_VERSION=jdk8u472-b08
# Tue, 20 Jan 2026 19:12:19 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='e2aff19d85d2441e409d6cbdf12ef7c2acabb0de73bca4207947135dcaa935a2';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u472-b08/OpenJDK8U-jdk_aarch64_linux_hotspot_8u472b08.tar.gz';          ;;        ppc64le)          ESUM='eaf57a4564265583b0641c878bea8943d27ef110c096868f686dae179fb45d8f';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u472-b08/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u472b08.tar.gz';          ;;        x86_64)          ESUM='5becaa4ac660e844c5a39e2ebc39ff5ac824c37ff1b625af8c8b111dc13c3592';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u472-b08/OpenJDK8U-jdk_x64_linux_hotspot_8u472b08.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip; # buildkit
# Tue, 20 Jan 2026 19:12:19 GMT
RUN set -eux;     echo "Verifying install ...";     echo "javac -version"; javac -version;     echo "java -version"; java -version;     echo "Complete." # buildkit
# Tue, 20 Jan 2026 19:12:19 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 20 Jan 2026 19:12:19 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Mon, 26 Jan 2026 19:19:10 GMT
CMD ["gradle"]
# Mon, 26 Jan 2026 19:19:10 GMT
ENV GRADLE_HOME=/opt/gradle
# Mon, 26 Jan 2026 19:19:10 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 101 gradle     && useradd --system --gid gradle --uid 101 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Mon, 26 Jan 2026 19:19:10 GMT
VOLUME [/home/gradle/.gradle]
# Mon, 26 Jan 2026 19:19:10 GMT
WORKDIR /home/gradle
# Mon, 26 Jan 2026 19:19:15 GMT
RUN set -o errexit -o nounset     && microdnf install -y         make                 findutils                 unzip         which                 git         git-lfs         subversion     && microdnf clean all         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which svn # buildkit
# Mon, 26 Jan 2026 19:19:15 GMT
ENV GRADLE_VERSION=8.14.4
# Mon, 26 Jan 2026 19:19:15 GMT
ARG GRADLE_DOWNLOAD_SHA256=f1771298a70f6db5a29daf62378c4e18a17fc33c9ba6b14362e0cdf40610380d
# Mon, 26 Jan 2026 19:19:17 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=f1771298a70f6db5a29daf62378c4e18a17fc33c9ba6b14362e0cdf40610380d
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Mon, 26 Jan 2026 19:19:17 GMT
USER gradle
# Mon, 26 Jan 2026 19:19:18 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=f1771298a70f6db5a29daf62378c4e18a17fc33c9ba6b14362e0cdf40610380d
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Mon, 26 Jan 2026 19:19:18 GMT
USER root
```

-	Layers:
	-	`sha256:c678760be1bb4697117294f3c0870d24a7c58498b99f14e293dc60361233dcc4`  
		Last Modified: Mon, 19 Jan 2026 05:33:32 GMT  
		Size: 38.2 MB (38208676 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6448c36239b0fa1e6accdcdd50351634324e10bc5c9676b3d49d9cf0b2b28c6c`  
		Last Modified: Tue, 20 Jan 2026 19:12:34 GMT  
		Size: 30.9 MB (30859235 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1fa576f4a545e15d3bfd4f913059d668337f56ca016cb791a2997967a45cc26`  
		Last Modified: Tue, 20 Jan 2026 19:12:35 GMT  
		Size: 53.8 MB (53815561 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e3dc88b80b4f18f088423d4c37b993f45d4f8a3735132880c78e74be54526f6`  
		Last Modified: Tue, 20 Jan 2026 19:12:31 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b580508c57791bb12b1b60c2883e738841a1e880cee238e86455b798395859b2`  
		Last Modified: Tue, 20 Jan 2026 19:12:33 GMT  
		Size: 2.3 KB (2316 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff4e773c509f5d4dabcad86f56f8c6017d5d5b9bb3e7a1ee6f76e8606e470a97`  
		Last Modified: Mon, 26 Jan 2026 19:19:33 GMT  
		Size: 1.7 KB (1707 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5ae33e076939a8f8a4f2ff1d584db14133f315b5936e5b980f8556eaba76c82`  
		Last Modified: Mon, 26 Jan 2026 19:19:35 GMT  
		Size: 36.1 MB (36060147 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d58719623c03539a83404933121ad0801a9b54b99592fcd9c7463c0eb80c91b2`  
		Last Modified: Mon, 26 Jan 2026 19:19:37 GMT  
		Size: 137.4 MB (137388273 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:713809206ee195069905de7a9cf10419d60239936991be79802dc022c4fc63cb`  
		Last Modified: Mon, 26 Jan 2026 19:19:33 GMT  
		Size: 59.5 KB (59524 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:8-jdk8-ubi` - unknown; unknown

```console
$ docker pull gradle@sha256:7bb2079d91951e5b12890e2c2ae4b69444022c379005c140fab17e62f200b7c6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5549251 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b24d7a3b67517bf2dfe1cf21eb1ac6f7ee692935da3b43949ab359f76b42a03e`

```dockerfile
```

-	Layers:
	-	`sha256:0025d37d862fd95f7515c7f5e045afa1e1e0d5e563a07ac0b31e7212e3da7313`  
		Last Modified: Mon, 26 Jan 2026 19:19:33 GMT  
		Size: 5.5 MB (5524921 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3eb7f7a9103fbf3708a20fba68943c4097557b6345aa8e18618aa41a22d7f344`  
		Last Modified: Mon, 26 Jan 2026 19:19:33 GMT  
		Size: 24.3 KB (24330 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:8-jdk8-ubi` - linux; ppc64le

```console
$ docker pull gradle@sha256:c4f4205510a444c023eb31c1192a4731b898821eea47cb9f2eed078aca953944
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **304.9 MB (304921690 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:642a6393e44c672c6739f27ea569daff77c82230b0b22d8b7acf3468c14814ed`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["gradle"]`

```dockerfile
# Mon, 19 Jan 2026 01:08:41 GMT
LABEL maintainer="Red Hat, Inc."
# Mon, 19 Jan 2026 01:08:41 GMT
LABEL vendor="Red Hat, Inc."
# Mon, 19 Jan 2026 01:08:41 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Mon, 19 Jan 2026 01:08:41 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.7"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Mon, 19 Jan 2026 01:08:41 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Mon, 19 Jan 2026 01:08:41 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Mon, 19 Jan 2026 01:08:41 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 19 Jan 2026 01:08:41 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 19 Jan 2026 01:08:41 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Mon, 19 Jan 2026 01:08:41 GMT
LABEL io.openshift.expose-services=""
# Mon, 19 Jan 2026 01:08:41 GMT
LABEL io.openshift.tags="minimal rhel9"
# Mon, 19 Jan 2026 01:08:41 GMT
ENV container oci
# Mon, 19 Jan 2026 01:08:42 GMT
COPY dir:3bd7ec6f425d769a16814adff3b957a15c4cbdec659c93cd45b1a546561564a3 in /      
# Mon, 19 Jan 2026 01:08:42 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Mon, 19 Jan 2026 01:08:42 GMT
CMD ["/bin/bash"]
# Mon, 19 Jan 2026 01:08:42 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /usr/share/buildinfo/content-sets.json      
# Mon, 19 Jan 2026 01:08:42 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /root/buildinfo/content_manifests/content-sets.json      
# Mon, 19 Jan 2026 01:08:42 GMT
COPY file:fe8dfccf0fa987a5d4946f1b72ab0cc09a6e656396d24bdd16b87ea3307e9302 in /usr/share/buildinfo/labels.json      
# Mon, 19 Jan 2026 01:08:42 GMT
COPY file:fe8dfccf0fa987a5d4946f1b72ab0cc09a6e656396d24bdd16b87ea3307e9302 in /root/buildinfo/labels.json      
# Mon, 19 Jan 2026 01:08:43 GMT
LABEL "architecture"="ppc64le" "vcs-type"="git" "vcs-ref"="d9151f7dd4dfe1cc8a2df524b85cddd483628d5e" "org.opencontainers.image.revision"="d9151f7dd4dfe1cc8a2df524b85cddd483628d5e" "build-date"="2026-01-19T01:08:31Z" "org.opencontainers.image.created"="2026-01-19T01:08:31Z" "release"="1768783948"org.opencontainers.image.revision=d9151f7dd4dfe1cc8a2df524b85cddd483628d5e,org.opencontainers.image.created=2026-01-19T01:08:31Z
# Tue, 20 Jan 2026 19:12:37 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 20 Jan 2026 19:12:37 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 20 Jan 2026 19:12:37 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 20 Jan 2026 19:12:37 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en     ;     microdnf clean all # buildkit
# Tue, 20 Jan 2026 19:12:37 GMT
ENV JAVA_VERSION=jdk8u472-b08
# Tue, 20 Jan 2026 19:12:46 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='e2aff19d85d2441e409d6cbdf12ef7c2acabb0de73bca4207947135dcaa935a2';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u472-b08/OpenJDK8U-jdk_aarch64_linux_hotspot_8u472b08.tar.gz';          ;;        ppc64le)          ESUM='eaf57a4564265583b0641c878bea8943d27ef110c096868f686dae179fb45d8f';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u472-b08/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u472b08.tar.gz';          ;;        x86_64)          ESUM='5becaa4ac660e844c5a39e2ebc39ff5ac824c37ff1b625af8c8b111dc13c3592';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u472-b08/OpenJDK8U-jdk_x64_linux_hotspot_8u472b08.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip; # buildkit
# Tue, 20 Jan 2026 19:12:47 GMT
RUN set -eux;     echo "Verifying install ...";     echo "javac -version"; javac -version;     echo "java -version"; java -version;     echo "Complete." # buildkit
# Tue, 20 Jan 2026 19:12:48 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 20 Jan 2026 19:12:48 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Mon, 26 Jan 2026 19:23:42 GMT
CMD ["gradle"]
# Mon, 26 Jan 2026 19:23:42 GMT
ENV GRADLE_HOME=/opt/gradle
# Mon, 26 Jan 2026 19:23:42 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 101 gradle     && useradd --system --gid gradle --uid 101 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Mon, 26 Jan 2026 19:23:42 GMT
VOLUME [/home/gradle/.gradle]
# Mon, 26 Jan 2026 19:23:43 GMT
WORKDIR /home/gradle
# Mon, 26 Jan 2026 19:23:58 GMT
RUN set -o errexit -o nounset     && microdnf install -y         make                 findutils                 unzip         which                 git         git-lfs         subversion     && microdnf clean all         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which svn # buildkit
# Mon, 26 Jan 2026 19:23:58 GMT
ENV GRADLE_VERSION=8.14.4
# Mon, 26 Jan 2026 19:23:58 GMT
ARG GRADLE_DOWNLOAD_SHA256=f1771298a70f6db5a29daf62378c4e18a17fc33c9ba6b14362e0cdf40610380d
# Mon, 26 Jan 2026 19:24:03 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=f1771298a70f6db5a29daf62378c4e18a17fc33c9ba6b14362e0cdf40610380d
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Mon, 26 Jan 2026 19:24:03 GMT
USER gradle
# Mon, 26 Jan 2026 19:24:05 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=f1771298a70f6db5a29daf62378c4e18a17fc33c9ba6b14362e0cdf40610380d
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Mon, 26 Jan 2026 19:24:05 GMT
USER root
```

-	Layers:
	-	`sha256:cb3df95d99fa30c8131b824671f0e15d0c34235a2e7bda21e4a361d100760346`  
		Last Modified: Mon, 19 Jan 2026 06:13:36 GMT  
		Size: 44.5 MB (44459713 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5c7d8e1a879073a2bb5883fd40b014f62a8e14ba675ff25067ab8b020299f7b`  
		Last Modified: Tue, 20 Jan 2026 19:13:32 GMT  
		Size: 32.9 MB (32898320 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:439859e84a705e80fafb65158577618041d2f25202b097dcf8c736fefa243daa`  
		Last Modified: Tue, 20 Jan 2026 19:13:33 GMT  
		Size: 52.2 MB (52175807 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ef62987b042714c89ac3ca3e795b8af531ad6f54cd74fa5b6b26366c3c6cb77`  
		Last Modified: Tue, 20 Jan 2026 19:13:05 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10160bf06491630a1a0b08c6a47cafb5416eed41e395713b64bee58513b47534`  
		Last Modified: Tue, 20 Jan 2026 19:13:31 GMT  
		Size: 2.3 KB (2317 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9bfc4f713025cbb1d8596b6ed942c5b1494a6625fafdb87e12b5a008623aa90`  
		Last Modified: Mon, 26 Jan 2026 19:24:54 GMT  
		Size: 1.7 KB (1713 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fba6ac79ffb44d3463698142799c5b8daed6c1c27eb4ce50bce85640672a64ee`  
		Last Modified: Mon, 26 Jan 2026 19:24:56 GMT  
		Size: 38.0 MB (37960373 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b21ed1b596abf265c76bbeec5f76a156d4c0ed2dc4a160be3ceee36d61802ab`  
		Last Modified: Mon, 26 Jan 2026 19:24:58 GMT  
		Size: 137.4 MB (137388274 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed59a8982e516867955a6c04ca8c8acf605e6a0a609e8afeb0e3e475dafc90ea`  
		Last Modified: Mon, 26 Jan 2026 19:24:54 GMT  
		Size: 35.0 KB (35013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:8-jdk8-ubi` - unknown; unknown

```console
$ docker pull gradle@sha256:3d98ecceaa84508f199a633c13ba2a54ec175e4e6473fc2fc4fdcd88a26c34cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5546965 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f77cb1d8e9bee469e99edd132c629f2a1e579782aeadce9f2a1b7d2ff0e2597`

```dockerfile
```

-	Layers:
	-	`sha256:57d315ff66da26b8e1ca12752a8074ee88dfdef618a54e8ac18702cb8bb450b4`  
		Last Modified: Mon, 26 Jan 2026 19:24:55 GMT  
		Size: 5.5 MB (5522721 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a55258faf3bb9bd099c611e688c540b3432cbd9939817ef9925a808227a1cf93`  
		Last Modified: Mon, 26 Jan 2026 19:24:54 GMT  
		Size: 24.2 KB (24244 bytes)  
		MIME: application/vnd.in-toto+json
