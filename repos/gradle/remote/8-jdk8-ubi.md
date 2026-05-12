## `gradle:8-jdk8-ubi`

```console
$ docker pull gradle@sha256:a76ef00deaa6c4ac7faab94736ec5b1966dd9da8538e463ad772d22bb3c44fa5
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
$ docker pull gradle@sha256:dc077795019b8d586068c034582e258cb6ca1faf90f3708617e0e559cab18473
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **300.4 MB (300383929 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:92213766aba277306e21a5c3563c4be9e5a0d72726d5976b2c140da57097c70c`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["gradle"]`

```dockerfile
# Mon, 11 May 2026 01:07:55 GMT
LABEL maintainer="Red Hat, Inc."
# Mon, 11 May 2026 01:07:55 GMT
LABEL vendor="Red Hat, Inc."
# Mon, 11 May 2026 01:07:55 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Mon, 11 May 2026 01:07:55 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.7"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Mon, 11 May 2026 01:07:55 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Mon, 11 May 2026 01:07:55 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Mon, 11 May 2026 01:07:55 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 11 May 2026 01:07:55 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 11 May 2026 01:07:55 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Mon, 11 May 2026 01:07:55 GMT
LABEL io.openshift.expose-services=""
# Mon, 11 May 2026 01:07:55 GMT
LABEL io.openshift.tags="minimal rhel9"
# Mon, 11 May 2026 01:07:55 GMT
ENV container oci
# Mon, 11 May 2026 01:07:56 GMT
COPY dir:d396e6c334ec17a1ba4a03f21481f526666f77d114978313ef1df55edd8e1412 in /      
# Mon, 11 May 2026 01:07:56 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Mon, 11 May 2026 01:07:56 GMT
CMD ["/bin/bash"]
# Mon, 11 May 2026 01:07:56 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /usr/share/buildinfo/content-sets.json      
# Mon, 11 May 2026 01:07:56 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /root/buildinfo/content_manifests/content-sets.json      
# Mon, 11 May 2026 01:07:56 GMT
COPY file:1b5a90f3ed08efd6f44de46e666565e2a9b8e1a168d7a249c016b23dc19bcaac in /usr/share/buildinfo/labels.json      
# Mon, 11 May 2026 01:07:56 GMT
COPY file:1b5a90f3ed08efd6f44de46e666565e2a9b8e1a168d7a249c016b23dc19bcaac in /root/buildinfo/labels.json      
# Mon, 11 May 2026 01:07:57 GMT
LABEL "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="15c06b7b1c40ffa5f97dc04e88d2d76dc1a15bc1" "org.opencontainers.image.revision"="15c06b7b1c40ffa5f97dc04e88d2d76dc1a15bc1" "build-date"="2026-05-11T01:07:39Z" "org.opencontainers.image.created"="2026-05-11T01:07:39Z" "release"="1778461551"org.opencontainers.image.revision=15c06b7b1c40ffa5f97dc04e88d2d76dc1a15bc1,org.opencontainers.image.created=2026-05-11T01:07:39Z
# Tue, 12 May 2026 21:25:23 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 12 May 2026 21:25:23 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 May 2026 21:25:23 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 12 May 2026 21:25:23 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en     ;     microdnf clean all # buildkit
# Tue, 12 May 2026 21:25:23 GMT
ENV JAVA_VERSION=jdk8u492-b09
# Tue, 12 May 2026 21:25:28 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='3c2253b986909c20f79d6de7a0cb957f89c243df57615897836046e24d2e5257';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u492-b09/OpenJDK8U-jdk_aarch64_linux_hotspot_8u492b09.tar.gz';          ;;        ppc64le)          ESUM='867e477e0a54159c7b774c55cfb046767120b1de43f705fa775ece74ea39e341';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u492-b09/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u492b09.tar.gz';          ;;        x86_64)          ESUM='da257f161d7f8c6ca5b0e5d9e4090f65ac28c5e398072e68b8ae87988b1d1a2e';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u492-b09/OpenJDK8U-jdk_x64_linux_hotspot_8u492b09.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip; # buildkit
# Tue, 12 May 2026 21:25:28 GMT
RUN set -eux;     echo "Verifying install ...";     echo "javac -version"; javac -version;     echo "java -version"; java -version;     echo "Complete." # buildkit
# Tue, 12 May 2026 21:25:28 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 12 May 2026 21:25:28 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 12 May 2026 21:42:26 GMT
CMD ["gradle"]
# Tue, 12 May 2026 21:42:26 GMT
ENV GRADLE_HOME=/opt/gradle
# Tue, 12 May 2026 21:42:26 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 101 gradle     && useradd --system --gid gradle --uid 101 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Tue, 12 May 2026 21:42:26 GMT
VOLUME [/home/gradle/.gradle]
# Tue, 12 May 2026 21:42:26 GMT
WORKDIR /home/gradle
# Tue, 12 May 2026 21:42:29 GMT
RUN set -o errexit -o nounset     && microdnf install -y         make         curl-minimal         wget         tar                 findutils                 unzip         which                 git         git-lfs         subversion     && microdnf clean all         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which svn # buildkit
# Tue, 12 May 2026 21:42:29 GMT
ENV GRADLE_VERSION=8.14.5
# Tue, 12 May 2026 21:42:29 GMT
ARG GRADLE_DOWNLOAD_SHA256=6f74b601422d6d6fc4e1f9a1ab6522f642c2fdcbc15ae33ebd30ba3d7198e854
# Tue, 12 May 2026 21:42:32 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=6f74b601422d6d6fc4e1f9a1ab6522f642c2fdcbc15ae33ebd30ba3d7198e854
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Tue, 12 May 2026 21:42:32 GMT
USER gradle
# Tue, 12 May 2026 21:42:33 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=6f74b601422d6d6fc4e1f9a1ab6522f642c2fdcbc15ae33ebd30ba3d7198e854
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --stacktrace --debug --version # buildkit
# Tue, 12 May 2026 21:42:33 GMT
USER root
```

-	Layers:
	-	`sha256:34f4a557df8123a31168a9ed57304a4ee0a79b26712d1770dcf7c798372b100b`  
		Last Modified: Mon, 11 May 2026 02:10:30 GMT  
		Size: 40.0 MB (39994724 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fe21041e867eb9dd2a87956e25f0082cadffc9abdc86be1bf28620cb851c3f4`  
		Last Modified: Tue, 12 May 2026 21:25:41 GMT  
		Size: 30.4 MB (30368834 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a4eabbb9aaef5aa548038c234c3c50c7c87ce4eeeb0659239a9d78e73ddc4bd`  
		Last Modified: Tue, 12 May 2026 21:25:42 GMT  
		Size: 55.2 MB (55199115 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b38f78e1fabe02f989bd20eb300e6d2495ac8e584e2396f3e79bf2cd4dfbc9b3`  
		Last Modified: Tue, 12 May 2026 21:25:39 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e11d4e6c105432b1819fe0557879192e68a5aff94e317559a40efd4640ec507`  
		Last Modified: Tue, 12 May 2026 21:25:39 GMT  
		Size: 2.5 KB (2490 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:560d5df71e6fcafdbb8ee4217f7e41a6b9041f3ecba60d8f348c28473c9a498e`  
		Last Modified: Tue, 12 May 2026 21:42:48 GMT  
		Size: 1.7 KB (1707 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8515f363a9f7c26b4c7d250bbf3f169f8a0f4d48d2d37d081ee25bb201ad13db`  
		Last Modified: Tue, 12 May 2026 21:42:50 GMT  
		Size: 36.7 MB (36693460 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2fb568d7a362090ac32cba6393d08e462d69b527fe5536f8fc0532299875f533`  
		Last Modified: Tue, 12 May 2026 21:42:57 GMT  
		Size: 138.1 MB (138068537 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4de039373320b39696a49918a753794f5bfdf132301e606e867b51045c71732`  
		Last Modified: Tue, 12 May 2026 21:42:48 GMT  
		Size: 54.9 KB (54904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:8-jdk8-ubi` - unknown; unknown

```console
$ docker pull gradle@sha256:7c53159955ad63793f5947496faf2455eed4c5d7c93d190d6916e92861bc6ce6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5549962 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:23ee9d5f7c582379d8b104a9b0e4ead311229e1759fa5e15ea67493486659175`

```dockerfile
```

-	Layers:
	-	`sha256:ab5035f6fe95a8b4ead09fdaa9aa58bf4ef10d030aefdd85e86634b081dffa03`  
		Last Modified: Tue, 12 May 2026 21:42:48 GMT  
		Size: 5.5 MB (5525510 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a3e0278665d82ef8a87557dbefa63fb554c69d942fa5703dbfd5f6fa20a7dbbb`  
		Last Modified: Tue, 12 May 2026 21:42:48 GMT  
		Size: 24.5 KB (24452 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:8-jdk8-ubi` - linux; arm64 variant v8

```console
$ docker pull gradle@sha256:739ac3be888b98d1aa10e65b4087db29dfaf9c518c906cf681f2e3abbdba7fa1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **297.4 MB (297427705 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf747f21cef2a6fed6626e3a7afdc361d6f9cfced7217dbecfbdf18e54ae33a0`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["gradle"]`

```dockerfile
# Mon, 11 May 2026 01:10:03 GMT
LABEL maintainer="Red Hat, Inc."
# Mon, 11 May 2026 01:10:03 GMT
LABEL vendor="Red Hat, Inc."
# Mon, 11 May 2026 01:10:03 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Mon, 11 May 2026 01:10:03 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.7"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Mon, 11 May 2026 01:10:03 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Mon, 11 May 2026 01:10:03 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Mon, 11 May 2026 01:10:03 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 11 May 2026 01:10:04 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 11 May 2026 01:10:04 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Mon, 11 May 2026 01:10:04 GMT
LABEL io.openshift.expose-services=""
# Mon, 11 May 2026 01:10:04 GMT
LABEL io.openshift.tags="minimal rhel9"
# Mon, 11 May 2026 01:10:04 GMT
ENV container oci
# Mon, 11 May 2026 01:10:05 GMT
COPY dir:f96b78a7f24437106ae6a323adf2c06c98f78157637998e58adf24d336fc59f9 in /      
# Mon, 11 May 2026 01:10:05 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Mon, 11 May 2026 01:10:05 GMT
CMD ["/bin/bash"]
# Mon, 11 May 2026 01:10:05 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /usr/share/buildinfo/content-sets.json      
# Mon, 11 May 2026 01:10:05 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /root/buildinfo/content_manifests/content-sets.json      
# Mon, 11 May 2026 01:10:05 GMT
COPY file:4815587a81c6816403ce960a517de92d74cd550eeda95c6164f5b3614ab4c3fe in /usr/share/buildinfo/labels.json      
# Mon, 11 May 2026 01:10:05 GMT
COPY file:4815587a81c6816403ce960a517de92d74cd550eeda95c6164f5b3614ab4c3fe in /root/buildinfo/labels.json      
# Mon, 11 May 2026 01:10:05 GMT
LABEL "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="15c06b7b1c40ffa5f97dc04e88d2d76dc1a15bc1" "org.opencontainers.image.revision"="15c06b7b1c40ffa5f97dc04e88d2d76dc1a15bc1" "build-date"="2026-05-11T01:09:50Z" "org.opencontainers.image.created"="2026-05-11T01:09:50Z" "release"="1778461551"org.opencontainers.image.revision=15c06b7b1c40ffa5f97dc04e88d2d76dc1a15bc1,org.opencontainers.image.created=2026-05-11T01:09:50Z
# Tue, 12 May 2026 21:25:31 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 12 May 2026 21:25:31 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 May 2026 21:25:31 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 12 May 2026 21:25:31 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en     ;     microdnf clean all # buildkit
# Tue, 12 May 2026 21:25:31 GMT
ENV JAVA_VERSION=jdk8u492-b09
# Tue, 12 May 2026 21:25:36 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='3c2253b986909c20f79d6de7a0cb957f89c243df57615897836046e24d2e5257';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u492-b09/OpenJDK8U-jdk_aarch64_linux_hotspot_8u492b09.tar.gz';          ;;        ppc64le)          ESUM='867e477e0a54159c7b774c55cfb046767120b1de43f705fa775ece74ea39e341';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u492-b09/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u492b09.tar.gz';          ;;        x86_64)          ESUM='da257f161d7f8c6ca5b0e5d9e4090f65ac28c5e398072e68b8ae87988b1d1a2e';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u492-b09/OpenJDK8U-jdk_x64_linux_hotspot_8u492b09.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip; # buildkit
# Tue, 12 May 2026 21:25:36 GMT
RUN set -eux;     echo "Verifying install ...";     echo "javac -version"; javac -version;     echo "java -version"; java -version;     echo "Complete." # buildkit
# Tue, 12 May 2026 21:25:36 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 12 May 2026 21:25:36 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 12 May 2026 21:41:49 GMT
CMD ["gradle"]
# Tue, 12 May 2026 21:41:49 GMT
ENV GRADLE_HOME=/opt/gradle
# Tue, 12 May 2026 21:41:49 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 101 gradle     && useradd --system --gid gradle --uid 101 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Tue, 12 May 2026 21:41:49 GMT
VOLUME [/home/gradle/.gradle]
# Tue, 12 May 2026 21:41:49 GMT
WORKDIR /home/gradle
# Tue, 12 May 2026 21:41:52 GMT
RUN set -o errexit -o nounset     && microdnf install -y         make         curl-minimal         wget         tar                 findutils                 unzip         which                 git         git-lfs         subversion     && microdnf clean all         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which svn # buildkit
# Tue, 12 May 2026 21:41:52 GMT
ENV GRADLE_VERSION=8.14.5
# Tue, 12 May 2026 21:41:52 GMT
ARG GRADLE_DOWNLOAD_SHA256=6f74b601422d6d6fc4e1f9a1ab6522f642c2fdcbc15ae33ebd30ba3d7198e854
# Tue, 12 May 2026 21:41:55 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=6f74b601422d6d6fc4e1f9a1ab6522f642c2fdcbc15ae33ebd30ba3d7198e854
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Tue, 12 May 2026 21:41:55 GMT
USER gradle
# Tue, 12 May 2026 21:41:56 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=6f74b601422d6d6fc4e1f9a1ab6522f642c2fdcbc15ae33ebd30ba3d7198e854
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --stacktrace --debug --version # buildkit
# Tue, 12 May 2026 21:41:56 GMT
USER root
```

-	Layers:
	-	`sha256:07b48350f3398d184075c56877eb97837294903946c9a6c10031807b6c4f549d`  
		Last Modified: Mon, 11 May 2026 02:11:01 GMT  
		Size: 38.2 MB (38205518 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b62e104752fa9cc72558e8ed79800a3605c59ba7017158f306633ebb2d00273a`  
		Last Modified: Tue, 12 May 2026 21:25:52 GMT  
		Size: 30.8 MB (30789524 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62615fa3311d493f939575d334c0f314735b0295464f0f4db440f9ebf5b25103`  
		Last Modified: Tue, 12 May 2026 21:25:53 GMT  
		Size: 54.3 MB (54273414 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49404b9bbb38390c0ececb6f0b8230839ead1a7196ee2fc66440fb31838d7862`  
		Last Modified: Tue, 12 May 2026 21:25:49 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10802941cc5ae96701a59b2008f427a2ea900606892b3fcbdfc8c64531d62dd6`  
		Last Modified: Tue, 12 May 2026 21:25:49 GMT  
		Size: 2.5 KB (2490 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0fd2352a7832095baa06c51e803bc0b97a08f3c1408897a1d6b2a673caa1278b`  
		Last Modified: Tue, 12 May 2026 21:42:11 GMT  
		Size: 1.7 KB (1709 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:373f41ddb49d1574a239952843244b5563726de0e0f914f871e59fb327d0c74a`  
		Last Modified: Tue, 12 May 2026 21:42:13 GMT  
		Size: 36.0 MB (36026832 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1af24f68fc8890a78b1f670827fa8d80a180a8f607f21d9ce0c1af368a6cb381`  
		Last Modified: Tue, 12 May 2026 21:42:16 GMT  
		Size: 138.1 MB (138068535 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e858712beca68f0825112eed60b27fba4e746fa661106c33f3cef66d5580ed85`  
		Last Modified: Tue, 12 May 2026 21:42:12 GMT  
		Size: 59.5 KB (59524 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:8-jdk8-ubi` - unknown; unknown

```console
$ docker pull gradle@sha256:1ceb7143c23e6a4afb290bbb70f16858e4ea5770ecd2caacf67261df38fe6f9c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5550289 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:432ada9213c9d1faeb0a104e0769698f343e8f090a01a0d0bd949caa57f559d1`

```dockerfile
```

-	Layers:
	-	`sha256:1aa8daa5daeabfdf37de54f7f9d75e5ab398d1d1c523e9f176be7a668c0f3e8a`  
		Last Modified: Tue, 12 May 2026 21:42:12 GMT  
		Size: 5.5 MB (5525640 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d3760e178e35b4048748545fe694a177216f76614ea258ebf3e82fda71d576ec`  
		Last Modified: Tue, 12 May 2026 21:42:11 GMT  
		Size: 24.6 KB (24649 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:8-jdk8-ubi` - linux; ppc64le

```console
$ docker pull gradle@sha256:7f90c8c099be803255eebc67e83b9d865c07054a68163e21929864c7b3a9653b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **306.0 MB (306001108 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4097ca99b37520393c9248342c36fde9777180866a6356c7917ac832ceeb494f`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["gradle"]`

```dockerfile
# Mon, 11 May 2026 01:08:39 GMT
LABEL maintainer="Red Hat, Inc."
# Mon, 11 May 2026 01:08:39 GMT
LABEL vendor="Red Hat, Inc."
# Mon, 11 May 2026 01:08:39 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Mon, 11 May 2026 01:08:39 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.7"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Mon, 11 May 2026 01:08:39 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Mon, 11 May 2026 01:08:39 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Mon, 11 May 2026 01:08:39 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 11 May 2026 01:08:39 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 11 May 2026 01:08:39 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Mon, 11 May 2026 01:08:39 GMT
LABEL io.openshift.expose-services=""
# Mon, 11 May 2026 01:08:39 GMT
LABEL io.openshift.tags="minimal rhel9"
# Mon, 11 May 2026 01:08:39 GMT
ENV container oci
# Mon, 11 May 2026 01:08:40 GMT
COPY dir:965cbe659c4ef641a7d8453ee3646d27f67083aabd851e0d0e8ae579e1a5219a in /      
# Mon, 11 May 2026 01:08:40 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Mon, 11 May 2026 01:08:40 GMT
CMD ["/bin/bash"]
# Mon, 11 May 2026 01:08:40 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /usr/share/buildinfo/content-sets.json      
# Mon, 11 May 2026 01:08:40 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /root/buildinfo/content_manifests/content-sets.json      
# Mon, 11 May 2026 01:08:40 GMT
COPY file:5ab8055b01479fa72fe220e6096452a3966616329925346e0d128323be1372ea in /usr/share/buildinfo/labels.json      
# Mon, 11 May 2026 01:08:40 GMT
COPY file:5ab8055b01479fa72fe220e6096452a3966616329925346e0d128323be1372ea in /root/buildinfo/labels.json      
# Mon, 11 May 2026 01:08:41 GMT
LABEL "architecture"="ppc64le" "vcs-type"="git" "vcs-ref"="15c06b7b1c40ffa5f97dc04e88d2d76dc1a15bc1" "org.opencontainers.image.revision"="15c06b7b1c40ffa5f97dc04e88d2d76dc1a15bc1" "build-date"="2026-05-11T01:08:29Z" "org.opencontainers.image.created"="2026-05-11T01:08:29Z" "release"="1778461551"org.opencontainers.image.revision=15c06b7b1c40ffa5f97dc04e88d2d76dc1a15bc1,org.opencontainers.image.created=2026-05-11T01:08:29Z
# Tue, 12 May 2026 00:29:05 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 12 May 2026 00:29:05 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 May 2026 00:29:05 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 12 May 2026 00:29:05 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en     ;     microdnf clean all # buildkit
# Tue, 12 May 2026 00:29:05 GMT
ENV JAVA_VERSION=jdk8u492-b09
# Tue, 12 May 2026 21:27:11 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='3c2253b986909c20f79d6de7a0cb957f89c243df57615897836046e24d2e5257';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u492-b09/OpenJDK8U-jdk_aarch64_linux_hotspot_8u492b09.tar.gz';          ;;        ppc64le)          ESUM='867e477e0a54159c7b774c55cfb046767120b1de43f705fa775ece74ea39e341';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u492-b09/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u492b09.tar.gz';          ;;        x86_64)          ESUM='da257f161d7f8c6ca5b0e5d9e4090f65ac28c5e398072e68b8ae87988b1d1a2e';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u492-b09/OpenJDK8U-jdk_x64_linux_hotspot_8u492b09.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip; # buildkit
# Tue, 12 May 2026 21:27:12 GMT
RUN set -eux;     echo "Verifying install ...";     echo "javac -version"; javac -version;     echo "java -version"; java -version;     echo "Complete." # buildkit
# Tue, 12 May 2026 21:27:13 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 12 May 2026 21:27:13 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 12 May 2026 21:39:39 GMT
CMD ["gradle"]
# Tue, 12 May 2026 21:39:39 GMT
ENV GRADLE_HOME=/opt/gradle
# Tue, 12 May 2026 21:39:39 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 101 gradle     && useradd --system --gid gradle --uid 101 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Tue, 12 May 2026 21:39:39 GMT
VOLUME [/home/gradle/.gradle]
# Tue, 12 May 2026 21:39:40 GMT
WORKDIR /home/gradle
# Tue, 12 May 2026 21:39:52 GMT
RUN set -o errexit -o nounset     && microdnf install -y         make         curl-minimal         wget         tar                 findutils                 unzip         which                 git         git-lfs         subversion     && microdnf clean all         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which svn # buildkit
# Tue, 12 May 2026 21:39:52 GMT
ENV GRADLE_VERSION=8.14.5
# Tue, 12 May 2026 21:39:52 GMT
ARG GRADLE_DOWNLOAD_SHA256=6f74b601422d6d6fc4e1f9a1ab6522f642c2fdcbc15ae33ebd30ba3d7198e854
# Tue, 12 May 2026 21:39:59 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=6f74b601422d6d6fc4e1f9a1ab6522f642c2fdcbc15ae33ebd30ba3d7198e854
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Tue, 12 May 2026 21:39:59 GMT
USER gradle
# Tue, 12 May 2026 21:40:00 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=6f74b601422d6d6fc4e1f9a1ab6522f642c2fdcbc15ae33ebd30ba3d7198e854
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --stacktrace --debug --version # buildkit
# Tue, 12 May 2026 21:40:00 GMT
USER root
```

-	Layers:
	-	`sha256:63f20427e281fbcfcf4050232e679771a690d7b2cb4885d2fa139012ed9194ac`  
		Last Modified: Mon, 11 May 2026 06:12:17 GMT  
		Size: 44.5 MB (44457236 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:794d7e1260962e3beb07f3313ca46feec37bccd1dcc87637de2655c117ec19a4`  
		Last Modified: Tue, 12 May 2026 00:29:41 GMT  
		Size: 32.8 MB (32844103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b39ea09a165f7aff1d4dc6ccefa4e6c08a367e9b11be08d116a80a7b620527ab`  
		Last Modified: Tue, 12 May 2026 21:27:37 GMT  
		Size: 52.7 MB (52669670 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:968ed2624c1df274073fe8bcba59fd1a7a605c55f0c00f502d44959cd9018bd3`  
		Last Modified: Tue, 12 May 2026 21:27:35 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0945b39b1f3b22d538a126ae65e120e9fe08c32c820645d53e1ea471406bf168`  
		Last Modified: Tue, 12 May 2026 21:27:35 GMT  
		Size: 2.5 KB (2490 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3615350076061637ed327e18189559101b529a4056b3e3271a9ec3144ba81c66`  
		Last Modified: Tue, 12 May 2026 21:40:33 GMT  
		Size: 1.7 KB (1711 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9dae45f421419d65373c248db06c8a0d7b20778feebbd16b80bb03de2d4b0912`  
		Last Modified: Tue, 12 May 2026 21:40:35 GMT  
		Size: 37.9 MB (37922165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08b96bf954676fec78bf61fa2e30091170e2ef1c76b23ceb86bd0e59fb736cf1`  
		Last Modified: Tue, 12 May 2026 21:40:38 GMT  
		Size: 138.1 MB (138068565 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5a563384909922c5445333c4115f1d2abce9f46c456c254bb19e24315a83253`  
		Last Modified: Tue, 12 May 2026 21:40:33 GMT  
		Size: 35.0 KB (35009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:8-jdk8-ubi` - unknown; unknown

```console
$ docker pull gradle@sha256:23d786d52c2cb5d54f616c0e25bba2c3d7fc5007c428cd05afc2c39dc5b2531a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5547966 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6cd8c5d3300771e0326c2bf9df369c8f6cf50f71fbc819c2dd425c2e4b6159df`

```dockerfile
```

-	Layers:
	-	`sha256:529648fd7cce637b71c3714aa6d248e248b7195314e087aa953ed79123c9df8e`  
		Last Modified: Tue, 12 May 2026 21:40:33 GMT  
		Size: 5.5 MB (5523440 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1c8a99d424e1c31ac5d4b5e85abc08aaf991ea331dde8f8bed0e4a085dd21492`  
		Last Modified: Tue, 12 May 2026 21:40:33 GMT  
		Size: 24.5 KB (24526 bytes)  
		MIME: application/vnd.in-toto+json
