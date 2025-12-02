## `gradle:jdk11-ubi`

```console
$ docker pull gradle@sha256:c2714f2ea6fbab5f05c283daf8a309ebea254e30887e8f4d29597624c8857d5d
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

### `gradle:jdk11-ubi` - linux; amd64

```console
$ docker pull gradle@sha256:7fb0275be63c1a463da44c418918781943acbab95ebaf24dadb9826508072e74
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **386.0 MB (385980040 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:72baf521e9843d7ae56d9007bc91e0bb265103477e7ca4ff2c18dffe992a9116`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["gradle"]`

```dockerfile
# Mon, 01 Dec 2025 08:46:04 GMT
LABEL maintainer="Red Hat, Inc."
# Mon, 01 Dec 2025 08:46:04 GMT
LABEL vendor="Red Hat, Inc."
# Mon, 01 Dec 2025 08:46:04 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Mon, 01 Dec 2025 08:46:04 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.7"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Mon, 01 Dec 2025 08:46:04 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Mon, 01 Dec 2025 08:46:04 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Mon, 01 Dec 2025 08:46:04 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 01 Dec 2025 08:46:04 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 01 Dec 2025 08:46:04 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Mon, 01 Dec 2025 08:46:04 GMT
LABEL io.openshift.expose-services=""
# Mon, 01 Dec 2025 08:46:04 GMT
LABEL io.openshift.tags="minimal rhel9"
# Mon, 01 Dec 2025 08:46:04 GMT
ENV container oci
# Mon, 01 Dec 2025 08:46:05 GMT
COPY dir:9e1be6ea7c9ab655dce87115dc5a86f74430f6cce27de363947899ca9c40a12b in /      
# Mon, 01 Dec 2025 08:46:05 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Mon, 01 Dec 2025 08:46:05 GMT
CMD ["/bin/bash"]
# Mon, 01 Dec 2025 08:46:05 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /usr/share/buildinfo/content-sets.json      
# Mon, 01 Dec 2025 08:46:05 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /root/buildinfo/content_manifests/content-sets.json      
# Mon, 01 Dec 2025 08:46:05 GMT
COPY file:b2d99215ad0f777fc208a0abcf88392b89d81310198466ef08702f0413990c72 in /usr/share/buildinfo/labels.json      
# Mon, 01 Dec 2025 08:46:06 GMT
COPY file:b2d99215ad0f777fc208a0abcf88392b89d81310198466ef08702f0413990c72 in /root/buildinfo/labels.json      
# Mon, 01 Dec 2025 08:46:06 GMT
LABEL "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="aa778ff26f397863d5f50a6cf5f17a2343e5a626" "org.opencontainers.image.revision"="aa778ff26f397863d5f50a6cf5f17a2343e5a626" "build-date"="2025-12-01T08:45:48Z" "org.opencontainers.image.created"="2025-12-01T08:45:48Z" "release"="1764578379"org.opencontainers.image.revision=aa778ff26f397863d5f50a6cf5f17a2343e5a626,org.opencontainers.image.created=2025-12-01T08:45:48Z
# Tue, 02 Dec 2025 00:37:52 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 02 Dec 2025 00:37:52 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Dec 2025 00:37:52 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 02 Dec 2025 00:37:52 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en     ;     microdnf clean all # buildkit
# Tue, 02 Dec 2025 00:37:52 GMT
ENV JAVA_VERSION=jdk-11.0.29+7
# Tue, 02 Dec 2025 00:38:44 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='71e00cd0ab4371a4e9d67d1a2ca3e8ed2f126dff6a6ab152a6ecdec60100fbdd';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.29%2B7/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.29_7.tar.gz';          ;;        ppc64le)          ESUM='d6136c0baafd588ba4f9be9f81285052f03b5366868e98fcd38fa5fb43c9121d';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.29%2B7/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.29_7.tar.gz';          ;;        s390x)          ESUM='12a494209c04a4cacee1615708b6856a770391d2588251a9a36e767ca4a07ac4';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.29%2B7/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.29_7.tar.gz';          ;;        x86_64)          ESUM='3c8f2b53dd137cd86e54f40df96fd0fc56df72c749c06469e7eab216503bc7cf';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.29%2B7/OpenJDK11U-jdk_x64_linux_hotspot_11.0.29_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Tue, 02 Dec 2025 00:38:46 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 02 Dec 2025 00:38:46 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 02 Dec 2025 00:38:46 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 02 Dec 2025 00:38:46 GMT
CMD ["jshell"]
# Tue, 02 Dec 2025 01:07:23 GMT
CMD ["gradle"]
# Tue, 02 Dec 2025 01:07:23 GMT
ENV GRADLE_HOME=/opt/gradle
# Tue, 02 Dec 2025 01:07:23 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 101 gradle     && useradd --system --gid gradle --uid 101 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Tue, 02 Dec 2025 01:07:23 GMT
VOLUME [/home/gradle/.gradle]
# Tue, 02 Dec 2025 01:07:23 GMT
WORKDIR /home/gradle
# Tue, 02 Dec 2025 01:07:27 GMT
RUN set -o errexit -o nounset     && microdnf install -y         make                 findutils                 unzip         which                 git         git-lfs         subversion     && microdnf clean all         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which svn # buildkit
# Tue, 02 Dec 2025 01:07:27 GMT
ENV GRADLE_VERSION=8.14.3
# Tue, 02 Dec 2025 01:07:27 GMT
ARG GRADLE_DOWNLOAD_SHA256=bd71102213493060956ec229d946beee57158dbd89d0e62b91bca0fa2c5f3531
# Tue, 02 Dec 2025 01:07:29 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=bd71102213493060956ec229d946beee57158dbd89d0e62b91bca0fa2c5f3531
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Tue, 02 Dec 2025 01:07:29 GMT
USER gradle
# Tue, 02 Dec 2025 01:07:30 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=bd71102213493060956ec229d946beee57158dbd89d0e62b91bca0fa2c5f3531
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Tue, 02 Dec 2025 01:07:30 GMT
USER root
```

-	Layers:
	-	`sha256:e33884b9ee6fd9f34b4688c1f3f27e3a36be1a8633a805f0780dcfa23073efcb`  
		Last Modified: Mon, 01 Dec 2025 09:26:00 GMT  
		Size: 40.0 MB (40040081 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7684bd6ea6b6d7232aa145adc30f5e6adb974b545e91d61990706b3096865481`  
		Last Modified: Tue, 02 Dec 2025 00:38:37 GMT  
		Size: 30.4 MB (30407377 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:900ca4809d322aad21eecc7bb3d7d6682551d4abc1d40a2e643205609cbeab39`  
		Last Modified: Tue, 02 Dec 2025 01:07:13 GMT  
		Size: 141.4 MB (141425231 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08351b7676aa05bc9ad79fed4d2b9a3ac90231f68c4805bdbe42b88b8e1bd004`  
		Last Modified: Tue, 02 Dec 2025 01:07:03 GMT  
		Size: 130.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:605c57f53b9d85d090d610fcf1f6449c9fe072d00bcef989b85385f73120bc0a`  
		Last Modified: Tue, 02 Dec 2025 01:07:02 GMT  
		Size: 2.3 KB (2290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de88e0e155b2346749d5249600ad76fc29e40effd5a2b6318aae5fadf224bff1`  
		Last Modified: Tue, 02 Dec 2025 01:08:17 GMT  
		Size: 1.7 KB (1709 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aab01de00a6bd64406ddd260474a6f23eda8652781e82eb50e575a6b3e35dcdb`  
		Last Modified: Tue, 02 Dec 2025 01:08:24 GMT  
		Size: 36.7 MB (36653151 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6a6427fff94a697fb0e7fa851553f3786e4a6bb493617db80a8e1ab652bde8b`  
		Last Modified: Tue, 02 Dec 2025 12:05:57 GMT  
		Size: 137.4 MB (137395133 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1558d526400a72d968338a3fd1a2403d56062a009ec971fc11a8f18b9aebf710`  
		Last Modified: Tue, 02 Dec 2025 01:08:18 GMT  
		Size: 54.9 KB (54906 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:jdk11-ubi` - unknown; unknown

```console
$ docker pull gradle@sha256:ada237876cc648d4ed101f4aa55b72e549877374aa9999e3d9e3cfe2723b8c90
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5446838 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:43a6915d7615bd5ddb29d3ed4e5a1e493d5198c005944c76495d88a2c5b2cdb1`

```dockerfile
```

-	Layers:
	-	`sha256:c69ec649124aed2acd01b48489c641c808a30654e3db8bf1275d33c682baa5ca`  
		Last Modified: Tue, 02 Dec 2025 03:21:12 GMT  
		Size: 5.4 MB (5422675 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:458e3fa3c225066851fd9d0d005ebdba3ddb2a0e3f499a9260b5c13946809df1`  
		Last Modified: Tue, 02 Dec 2025 03:21:13 GMT  
		Size: 24.2 KB (24163 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:jdk11-ubi` - linux; arm64 variant v8

```console
$ docker pull gradle@sha256:0826c6fc9b965eeb5d17f76c5381b3f2cde7d54770e539fb815b54d7c0a98481
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **380.8 MB (380764053 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ba10d71b900a471862e8bcc2c7dc418bd4ef064969e9a423809ced3489525a5`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["gradle"]`

```dockerfile
# Mon, 01 Dec 2025 08:45:36 GMT
LABEL maintainer="Red Hat, Inc."
# Mon, 01 Dec 2025 08:45:36 GMT
LABEL vendor="Red Hat, Inc."
# Mon, 01 Dec 2025 08:45:36 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Mon, 01 Dec 2025 08:45:36 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.7"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Mon, 01 Dec 2025 08:45:36 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Mon, 01 Dec 2025 08:45:36 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Mon, 01 Dec 2025 08:45:36 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 01 Dec 2025 08:45:36 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 01 Dec 2025 08:45:36 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Mon, 01 Dec 2025 08:45:36 GMT
LABEL io.openshift.expose-services=""
# Mon, 01 Dec 2025 08:45:36 GMT
LABEL io.openshift.tags="minimal rhel9"
# Mon, 01 Dec 2025 08:45:36 GMT
ENV container oci
# Mon, 01 Dec 2025 08:45:37 GMT
COPY dir:0300512c6394db4e597803fcc03b9993a2a4c4d9c6e4eb31c5a64534316ae291 in /      
# Mon, 01 Dec 2025 08:45:37 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Mon, 01 Dec 2025 08:45:37 GMT
CMD ["/bin/bash"]
# Mon, 01 Dec 2025 08:45:37 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /usr/share/buildinfo/content-sets.json      
# Mon, 01 Dec 2025 08:45:37 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /root/buildinfo/content_manifests/content-sets.json      
# Mon, 01 Dec 2025 08:45:37 GMT
COPY file:9ba4e215cc648b0ee2f7a9114145896fc716da8ab330689b6c8358fccff02c52 in /usr/share/buildinfo/labels.json      
# Mon, 01 Dec 2025 08:45:37 GMT
COPY file:9ba4e215cc648b0ee2f7a9114145896fc716da8ab330689b6c8358fccff02c52 in /root/buildinfo/labels.json      
# Mon, 01 Dec 2025 08:45:38 GMT
LABEL "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="aa778ff26f397863d5f50a6cf5f17a2343e5a626" "org.opencontainers.image.revision"="aa778ff26f397863d5f50a6cf5f17a2343e5a626" "build-date"="2025-12-01T08:45:20Z" "org.opencontainers.image.created"="2025-12-01T08:45:20Z" "release"="1764578379"org.opencontainers.image.revision=aa778ff26f397863d5f50a6cf5f17a2343e5a626,org.opencontainers.image.created=2025-12-01T08:45:20Z
# Tue, 02 Dec 2025 00:43:28 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 02 Dec 2025 00:43:28 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Dec 2025 00:43:28 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 02 Dec 2025 00:43:28 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en     ;     microdnf clean all # buildkit
# Tue, 02 Dec 2025 00:43:28 GMT
ENV JAVA_VERSION=jdk-11.0.29+7
# Tue, 02 Dec 2025 00:45:47 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='71e00cd0ab4371a4e9d67d1a2ca3e8ed2f126dff6a6ab152a6ecdec60100fbdd';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.29%2B7/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.29_7.tar.gz';          ;;        ppc64le)          ESUM='d6136c0baafd588ba4f9be9f81285052f03b5366868e98fcd38fa5fb43c9121d';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.29%2B7/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.29_7.tar.gz';          ;;        s390x)          ESUM='12a494209c04a4cacee1615708b6856a770391d2588251a9a36e767ca4a07ac4';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.29%2B7/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.29_7.tar.gz';          ;;        x86_64)          ESUM='3c8f2b53dd137cd86e54f40df96fd0fc56df72c749c06469e7eab216503bc7cf';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.29%2B7/OpenJDK11U-jdk_x64_linux_hotspot_11.0.29_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Tue, 02 Dec 2025 00:45:49 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 02 Dec 2025 00:45:49 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 02 Dec 2025 00:45:49 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 02 Dec 2025 00:45:49 GMT
CMD ["jshell"]
# Tue, 02 Dec 2025 02:29:22 GMT
CMD ["gradle"]
# Tue, 02 Dec 2025 02:29:22 GMT
ENV GRADLE_HOME=/opt/gradle
# Tue, 02 Dec 2025 02:29:22 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 101 gradle     && useradd --system --gid gradle --uid 101 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Tue, 02 Dec 2025 02:29:22 GMT
VOLUME [/home/gradle/.gradle]
# Tue, 02 Dec 2025 02:29:22 GMT
WORKDIR /home/gradle
# Tue, 02 Dec 2025 02:29:26 GMT
RUN set -o errexit -o nounset     && microdnf install -y         make                 findutils                 unzip         which                 git         git-lfs         subversion     && microdnf clean all         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which svn # buildkit
# Tue, 02 Dec 2025 02:29:26 GMT
ENV GRADLE_VERSION=8.14.3
# Tue, 02 Dec 2025 02:29:26 GMT
ARG GRADLE_DOWNLOAD_SHA256=bd71102213493060956ec229d946beee57158dbd89d0e62b91bca0fa2c5f3531
# Tue, 02 Dec 2025 02:29:29 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=bd71102213493060956ec229d946beee57158dbd89d0e62b91bca0fa2c5f3531
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Tue, 02 Dec 2025 02:29:29 GMT
USER gradle
# Tue, 02 Dec 2025 02:29:30 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=bd71102213493060956ec229d946beee57158dbd89d0e62b91bca0fa2c5f3531
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Tue, 02 Dec 2025 02:29:30 GMT
USER root
```

-	Layers:
	-	`sha256:2318060655d9ba0a61831256291e1482c38f67e2e0879a90ccd9008c0ed03b36`  
		Last Modified: Mon, 01 Dec 2025 12:11:26 GMT  
		Size: 38.2 MB (38221706 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0fd4ef6da9f9ae1a10f689ed0d4112554c216caf370d452faa417f248e8e211`  
		Last Modified: Tue, 02 Dec 2025 00:43:56 GMT  
		Size: 30.9 MB (30853297 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4377d1cdf0184ee19033cb8f7ed75d75c174d6fbef9a89f60888fa691b6fc894`  
		Last Modified: Tue, 02 Dec 2025 02:29:20 GMT  
		Size: 138.2 MB (138190254 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c75c76d491126aa8ccf01ff2a8b2469e6bb263f67110969ce249358c25fcb617`  
		Last Modified: Tue, 02 Dec 2025 00:46:13 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1d8e6c5cc901205c7ed0f9c7f27b6086dd445a3f4bde8e2a214556aec66ec8e`  
		Last Modified: Tue, 02 Dec 2025 00:46:13 GMT  
		Size: 2.3 KB (2291 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfafcbbea40202d6a662316f0ef68a22a37e500412d0151be35272a13d6cced1`  
		Last Modified: Tue, 02 Dec 2025 02:29:55 GMT  
		Size: 1.7 KB (1711 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8723537e93d561ae00c156cdb8ec7b2c2ede0655f13fa3526bf94db994c04ba9`  
		Last Modified: Tue, 02 Dec 2025 02:30:00 GMT  
		Size: 36.0 MB (36039906 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1d6b6def935d6932695da21476d54fac5ec9b478b651b7acc457a5fa95ef5f6`  
		Last Modified: Tue, 02 Dec 2025 12:04:42 GMT  
		Size: 137.4 MB (137395199 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ee165ed4702174b32282aece88de59c29a4afbc14508f6e8ab2107ad37e0453`  
		Last Modified: Tue, 02 Dec 2025 02:29:55 GMT  
		Size: 59.5 KB (59528 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:jdk11-ubi` - unknown; unknown

```console
$ docker pull gradle@sha256:377a1001b57554f105eef8b1f26f3a8d5d3c0240aa621491977a33bee963540d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5447082 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:71ee5378b7fb4d718dc626edfecd8097fdfea876871aa03624410b4ed8e98831`

```dockerfile
```

-	Layers:
	-	`sha256:4754d5742494f55ce5a5aba5fc9f6b58fea955ba4c018582a7a0ffbf01b519f1`  
		Last Modified: Tue, 02 Dec 2025 03:21:17 GMT  
		Size: 5.4 MB (5422723 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9e283d000fd30e918aa20468b230443e5f4a49a4f3fb09c5a0e70eeed3bf373f`  
		Last Modified: Tue, 02 Dec 2025 03:21:18 GMT  
		Size: 24.4 KB (24359 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:jdk11-ubi` - linux; ppc64le

```console
$ docker pull gradle@sha256:e4629777636ec41d7af17b4c006aaa78d4a303e55a43142a93273ec93b60106f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **381.2 MB (381229817 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c97b310d3bdff794018b2ae3e0fe6878b8f24ef30f30139bf413e08809efc9c`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["gradle"]`

```dockerfile
# Mon, 01 Dec 2025 08:47:38 GMT
LABEL maintainer="Red Hat, Inc."
# Mon, 01 Dec 2025 08:47:38 GMT
LABEL vendor="Red Hat, Inc."
# Mon, 01 Dec 2025 08:47:38 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Mon, 01 Dec 2025 08:47:38 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.7"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Mon, 01 Dec 2025 08:47:38 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Mon, 01 Dec 2025 08:47:38 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Mon, 01 Dec 2025 08:47:38 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 01 Dec 2025 08:47:38 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 01 Dec 2025 08:47:39 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Mon, 01 Dec 2025 08:47:39 GMT
LABEL io.openshift.expose-services=""
# Mon, 01 Dec 2025 08:47:39 GMT
LABEL io.openshift.tags="minimal rhel9"
# Mon, 01 Dec 2025 08:47:39 GMT
ENV container oci
# Mon, 01 Dec 2025 08:47:39 GMT
COPY dir:424f5571363f754c607532e039ce86b38717a7177a891010344bc14523fcb50d in /      
# Mon, 01 Dec 2025 08:47:39 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Mon, 01 Dec 2025 08:47:39 GMT
CMD ["/bin/bash"]
# Mon, 01 Dec 2025 08:47:39 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /usr/share/buildinfo/content-sets.json      
# Mon, 01 Dec 2025 08:47:39 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /root/buildinfo/content_manifests/content-sets.json      
# Mon, 01 Dec 2025 08:47:39 GMT
COPY file:884927636b9162a0889bd8a915394fcd0f689b0bb04949b3f37755442e38a305 in /usr/share/buildinfo/labels.json      
# Mon, 01 Dec 2025 08:47:40 GMT
COPY file:884927636b9162a0889bd8a915394fcd0f689b0bb04949b3f37755442e38a305 in /root/buildinfo/labels.json      
# Mon, 01 Dec 2025 08:47:40 GMT
LABEL "architecture"="ppc64le" "vcs-type"="git" "vcs-ref"="aa778ff26f397863d5f50a6cf5f17a2343e5a626" "org.opencontainers.image.revision"="aa778ff26f397863d5f50a6cf5f17a2343e5a626" "build-date"="2025-12-01T08:47:28Z" "org.opencontainers.image.created"="2025-12-01T08:47:28Z" "release"="1764578379"org.opencontainers.image.revision=aa778ff26f397863d5f50a6cf5f17a2343e5a626,org.opencontainers.image.created=2025-12-01T08:47:28Z
# Tue, 02 Dec 2025 02:32:36 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 02 Dec 2025 02:32:36 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Dec 2025 02:32:36 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 02 Dec 2025 02:32:36 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en     ;     microdnf clean all # buildkit
# Tue, 02 Dec 2025 02:32:36 GMT
ENV JAVA_VERSION=jdk-11.0.29+7
# Tue, 02 Dec 2025 02:36:08 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='71e00cd0ab4371a4e9d67d1a2ca3e8ed2f126dff6a6ab152a6ecdec60100fbdd';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.29%2B7/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.29_7.tar.gz';          ;;        ppc64le)          ESUM='d6136c0baafd588ba4f9be9f81285052f03b5366868e98fcd38fa5fb43c9121d';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.29%2B7/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.29_7.tar.gz';          ;;        s390x)          ESUM='12a494209c04a4cacee1615708b6856a770391d2588251a9a36e767ca4a07ac4';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.29%2B7/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.29_7.tar.gz';          ;;        x86_64)          ESUM='3c8f2b53dd137cd86e54f40df96fd0fc56df72c749c06469e7eab216503bc7cf';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.29%2B7/OpenJDK11U-jdk_x64_linux_hotspot_11.0.29_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Tue, 02 Dec 2025 02:36:10 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 02 Dec 2025 02:36:11 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 02 Dec 2025 02:36:11 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 02 Dec 2025 02:36:11 GMT
CMD ["jshell"]
# Tue, 02 Dec 2025 04:50:10 GMT
CMD ["gradle"]
# Tue, 02 Dec 2025 04:50:10 GMT
ENV GRADLE_HOME=/opt/gradle
# Tue, 02 Dec 2025 04:50:10 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 101 gradle     && useradd --system --gid gradle --uid 101 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Tue, 02 Dec 2025 04:50:10 GMT
VOLUME [/home/gradle/.gradle]
# Tue, 02 Dec 2025 04:50:11 GMT
WORKDIR /home/gradle
# Tue, 02 Dec 2025 04:50:23 GMT
RUN set -o errexit -o nounset     && microdnf install -y         make                 findutils                 unzip         which                 git         git-lfs         subversion     && microdnf clean all         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which svn # buildkit
# Tue, 02 Dec 2025 04:50:23 GMT
ENV GRADLE_VERSION=8.14.3
# Tue, 02 Dec 2025 04:50:23 GMT
ARG GRADLE_DOWNLOAD_SHA256=bd71102213493060956ec229d946beee57158dbd89d0e62b91bca0fa2c5f3531
# Tue, 02 Dec 2025 04:50:29 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=bd71102213493060956ec229d946beee57158dbd89d0e62b91bca0fa2c5f3531
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Tue, 02 Dec 2025 04:50:29 GMT
USER gradle
# Tue, 02 Dec 2025 04:50:31 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=bd71102213493060956ec229d946beee57158dbd89d0e62b91bca0fa2c5f3531
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Tue, 02 Dec 2025 04:50:31 GMT
USER root
```

-	Layers:
	-	`sha256:1b4d94c49d931c12c52e0f1b89ae86e69536f3ba1c82bcb08e6fa7611333b0ff`  
		Last Modified: Mon, 01 Dec 2025 12:11:27 GMT  
		Size: 44.4 MB (44438693 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4a4568ee02dabf005e49fa2cd2cad02fbd1aae3c8f60bcfaa3adc88e1a7c443`  
		Last Modified: Tue, 02 Dec 2025 02:33:36 GMT  
		Size: 32.9 MB (32893278 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3be85640062eaa2b9d76a7724e5e7426d457d8a6f0d5e206d1a1d44a81df136f`  
		Last Modified: Tue, 02 Dec 2025 04:46:57 GMT  
		Size: 128.6 MB (128584293 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:939c443bbb9982a382b713388d281d2aa6137d5e782609c503ab337ac902f42d`  
		Last Modified: Tue, 02 Dec 2025 02:36:53 GMT  
		Size: 130.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b466b67795d913297ce7134cc1d5d2ceba2be869d1d2d85e07be7049a45a321c`  
		Last Modified: Tue, 02 Dec 2025 02:36:53 GMT  
		Size: 2.3 KB (2290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b42827b9fe9cf369c33ed86fe34fba3fe940026ed4b4fbb7b555d24894c8807a`  
		Last Modified: Tue, 02 Dec 2025 04:51:20 GMT  
		Size: 1.7 KB (1710 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a86da3be69aeadbab3bf0c0c4dee8e40043ab26d6c5268992238a53760f6a92c`  
		Last Modified: Tue, 02 Dec 2025 04:51:23 GMT  
		Size: 37.9 MB (37879182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec8cd7c379d9b80b9e58933862aa156a9a0686cab0483784a055b3528c2e31c9`  
		Last Modified: Tue, 02 Dec 2025 21:23:28 GMT  
		Size: 137.4 MB (137395200 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a89230273394659f6555e28622c61175c3419a06057e850fbcdf108d77a56002`  
		Last Modified: Tue, 02 Dec 2025 04:51:20 GMT  
		Size: 35.0 KB (35009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:jdk11-ubi` - unknown; unknown

```console
$ docker pull gradle@sha256:552af688509a913bfa5175357aecf2b5d450a920e19656d4059449565d2449fc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5443668 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d39fcdab7ec1ab0d6528d8fc1163f96e1d5d015c7c01d8d643aed2be9c9bf26`

```dockerfile
```

-	Layers:
	-	`sha256:a655aad7d457f7a1c74c62c59390b0e70295acc9d740888990629d13e6fd62da`  
		Last Modified: Tue, 02 Dec 2025 06:20:25 GMT  
		Size: 5.4 MB (5419395 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d58e0f3026f9976cf29eac5ca2ac83f5af78640705e1a03f6b6eafb3e3a95bef`  
		Last Modified: Tue, 02 Dec 2025 06:20:26 GMT  
		Size: 24.3 KB (24273 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:jdk11-ubi` - linux; s390x

```console
$ docker pull gradle@sha256:3b9d21ae065bfed3efff519b2ad9b17210ce55c0a5a5e433a8643c9099668e11
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **364.4 MB (364390422 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2dfaf5105bde9e85962fb28c67ecf2b8dd71b271ac6b66560a8efd9bbb77a602`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["gradle"]`

```dockerfile
# Mon, 01 Dec 2025 08:55:28 GMT
LABEL maintainer="Red Hat, Inc."
# Mon, 01 Dec 2025 08:55:28 GMT
LABEL vendor="Red Hat, Inc."
# Mon, 01 Dec 2025 08:55:28 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Mon, 01 Dec 2025 08:55:28 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.7"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Mon, 01 Dec 2025 08:55:28 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Mon, 01 Dec 2025 08:55:28 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Mon, 01 Dec 2025 08:55:28 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 01 Dec 2025 08:55:28 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 01 Dec 2025 08:55:28 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Mon, 01 Dec 2025 08:55:28 GMT
LABEL io.openshift.expose-services=""
# Mon, 01 Dec 2025 08:55:28 GMT
LABEL io.openshift.tags="minimal rhel9"
# Mon, 01 Dec 2025 08:55:28 GMT
ENV container oci
# Mon, 01 Dec 2025 08:55:29 GMT
COPY dir:fd64e83e16406d5844580a74bf276e335ef1e91b51af6932a1c38280460b502b in /      
# Mon, 01 Dec 2025 08:55:29 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Mon, 01 Dec 2025 08:55:29 GMT
CMD ["/bin/bash"]
# Mon, 01 Dec 2025 08:55:29 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /usr/share/buildinfo/content-sets.json      
# Mon, 01 Dec 2025 08:55:29 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /root/buildinfo/content_manifests/content-sets.json      
# Mon, 01 Dec 2025 08:55:29 GMT
COPY file:b9982a341e331d0c55380d80e2a0ce568511a3c088f1b8a4ab833ee5de68d530 in /usr/share/buildinfo/labels.json      
# Mon, 01 Dec 2025 08:55:29 GMT
COPY file:b9982a341e331d0c55380d80e2a0ce568511a3c088f1b8a4ab833ee5de68d530 in /root/buildinfo/labels.json      
# Mon, 01 Dec 2025 08:55:29 GMT
LABEL "architecture"="s390x" "vcs-type"="git" "vcs-ref"="aa778ff26f397863d5f50a6cf5f17a2343e5a626" "org.opencontainers.image.revision"="aa778ff26f397863d5f50a6cf5f17a2343e5a626" "build-date"="2025-12-01T08:54:26Z" "org.opencontainers.image.created"="2025-12-01T08:54:26Z" "release"="1764578379"org.opencontainers.image.revision=aa778ff26f397863d5f50a6cf5f17a2343e5a626,org.opencontainers.image.created=2025-12-01T08:54:26Z
# Tue, 02 Dec 2025 00:33:28 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 02 Dec 2025 00:33:28 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Dec 2025 00:33:28 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 02 Dec 2025 00:33:28 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en     ;     microdnf clean all # buildkit
# Tue, 02 Dec 2025 00:33:28 GMT
ENV JAVA_VERSION=jdk-11.0.29+7
# Tue, 02 Dec 2025 00:33:36 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='71e00cd0ab4371a4e9d67d1a2ca3e8ed2f126dff6a6ab152a6ecdec60100fbdd';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.29%2B7/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.29_7.tar.gz';          ;;        ppc64le)          ESUM='d6136c0baafd588ba4f9be9f81285052f03b5366868e98fcd38fa5fb43c9121d';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.29%2B7/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.29_7.tar.gz';          ;;        s390x)          ESUM='12a494209c04a4cacee1615708b6856a770391d2588251a9a36e767ca4a07ac4';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.29%2B7/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.29_7.tar.gz';          ;;        x86_64)          ESUM='3c8f2b53dd137cd86e54f40df96fd0fc56df72c749c06469e7eab216503bc7cf';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.29%2B7/OpenJDK11U-jdk_x64_linux_hotspot_11.0.29_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Tue, 02 Dec 2025 00:33:39 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 02 Dec 2025 00:33:40 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 02 Dec 2025 00:33:40 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 02 Dec 2025 00:33:40 GMT
CMD ["jshell"]
# Tue, 02 Dec 2025 01:05:12 GMT
CMD ["gradle"]
# Tue, 02 Dec 2025 01:05:12 GMT
ENV GRADLE_HOME=/opt/gradle
# Tue, 02 Dec 2025 01:05:12 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 101 gradle     && useradd --system --gid gradle --uid 101 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Tue, 02 Dec 2025 01:05:12 GMT
VOLUME [/home/gradle/.gradle]
# Tue, 02 Dec 2025 01:05:12 GMT
WORKDIR /home/gradle
# Tue, 02 Dec 2025 01:05:31 GMT
RUN set -o errexit -o nounset     && microdnf install -y         make                 findutils                 unzip         which                 git         git-lfs         subversion     && microdnf clean all         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which svn # buildkit
# Tue, 02 Dec 2025 01:05:31 GMT
ENV GRADLE_VERSION=8.14.3
# Tue, 02 Dec 2025 01:05:31 GMT
ARG GRADLE_DOWNLOAD_SHA256=bd71102213493060956ec229d946beee57158dbd89d0e62b91bca0fa2c5f3531
# Tue, 02 Dec 2025 01:05:38 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=bd71102213493060956ec229d946beee57158dbd89d0e62b91bca0fa2c5f3531
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Tue, 02 Dec 2025 01:05:38 GMT
USER gradle
# Tue, 02 Dec 2025 01:05:41 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=bd71102213493060956ec229d946beee57158dbd89d0e62b91bca0fa2c5f3531
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Tue, 02 Dec 2025 01:05:41 GMT
USER root
```

-	Layers:
	-	`sha256:c146ac3b9c14a1ecaff446a02862f803385ae46be28b17ca9bd879732615d0a0`  
		Last Modified: Mon, 01 Dec 2025 12:11:28 GMT  
		Size: 38.1 MB (38134676 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9672b4ccf7dda7bee014c587130265e9d6ff2697b86542083325bac8f3102a0b`  
		Last Modified: Tue, 02 Dec 2025 01:04:50 GMT  
		Size: 30.4 MB (30445670 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e58ba8b17ddc014b59216f1a2de4994cb309c5f55eda07d1e08071f9e5c199b2`  
		Last Modified: Tue, 02 Dec 2025 01:07:35 GMT  
		Size: 122.1 MB (122103859 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e5e5b64b8b99651be53d25b8766c9bef15839c40fe11b1ff374039b04dc786a`  
		Last Modified: Tue, 02 Dec 2025 01:07:26 GMT  
		Size: 130.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74d6c95e8472c3cab86524e69b3f77bdefd2a7a895edd233c6013a2026f7ef7d`  
		Last Modified: Tue, 02 Dec 2025 01:07:26 GMT  
		Size: 2.3 KB (2290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3861548b386201eec794ef47f5c7085ba399ecfc242f5cee273998cbfc21c08`  
		Last Modified: Tue, 02 Dec 2025 01:06:49 GMT  
		Size: 1.7 KB (1715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60d8d03d5d4438af72576a85bd91cbb696d622fa5a6e9b8de9052f56f262a423`  
		Last Modified: Tue, 02 Dec 2025 01:06:53 GMT  
		Size: 36.3 MB (36271910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71437ed75eebb31fc00c7b33a7a60220e476d9f10ec13c2c7e7dc9d28424fc1f`  
		Last Modified: Tue, 02 Dec 2025 12:07:13 GMT  
		Size: 137.4 MB (137395132 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4a452bb12c5e27677e29ee174ddceb98899424932ba6f7ab8b83e6e5523ebe5`  
		Last Modified: Tue, 02 Dec 2025 01:06:50 GMT  
		Size: 35.0 KB (35008 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:jdk11-ubi` - unknown; unknown

```console
$ docker pull gradle@sha256:f2ff5b76c963bf4b893f0a65d457439f4cd4aef68a073a835d16aa0302b107da
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5433483 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3a7f3d8e9ba02c00421c3bb09628d459e307f1897de1537b6ff3d21415f0908`

```dockerfile
```

-	Layers:
	-	`sha256:856097e3c324674e7a13fef5c53d3544665b452703d446782bfc5dc1ae60203f`  
		Last Modified: Tue, 02 Dec 2025 03:21:29 GMT  
		Size: 5.4 MB (5409284 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:caac6262d01085843257334c7c6ebec72c5123b06fcfd4bcfe75f437368dd24f`  
		Last Modified: Tue, 02 Dec 2025 03:21:30 GMT  
		Size: 24.2 KB (24199 bytes)  
		MIME: application/vnd.in-toto+json
