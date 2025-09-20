## `gradle:9-jdk24-ubi`

```console
$ docker pull gradle@sha256:3c62098fcbd285d766352486503dbc6b0d4fa052193f9c16bf54c5b96bdf3cc1
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

### `gradle:9-jdk24-ubi` - linux; amd64

```console
$ docker pull gradle@sha256:ce0f51c2e8bb42beb09e4205d9c1a9b898f855d27a624fe02ae0f45ad194bd65
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **328.5 MB (328523215 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c378bf9b61bbe6d1412373f67bef82262f1a28f7daf6cf40c57fdc5a557e87c5`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["gradle"]`

```dockerfile
# Fri, 01 Aug 2025 11:04:34 GMT
LABEL maintainer="Red Hat, Inc."
# Fri, 01 Aug 2025 11:04:34 GMT
LABEL vendor="Red Hat, Inc."
# Fri, 01 Aug 2025 11:04:34 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Fri, 01 Aug 2025 11:04:34 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.6"       distribution-scope="public"
# Fri, 01 Aug 2025 11:04:34 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Fri, 01 Aug 2025 11:04:34 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Fri, 01 Aug 2025 11:04:34 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Fri, 01 Aug 2025 11:04:34 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Fri, 01 Aug 2025 11:04:34 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Fri, 01 Aug 2025 11:04:34 GMT
LABEL io.openshift.expose-services=""
# Fri, 01 Aug 2025 11:04:34 GMT
LABEL io.openshift.tags="minimal rhel9"
# Fri, 01 Aug 2025 11:04:34 GMT
ENV container oci
# Fri, 01 Aug 2025 11:04:34 GMT
COPY dir:c341d431f712f164558c0a23b4ff14b886e2ce5a998d4c5baaaa381ffd7c3b00 in / 
# Fri, 01 Aug 2025 11:04:34 GMT
COPY file:b37d593713ee21ad52a4cd1424dc019a24f7966f85df0ac4b86d234302695328 in /etc/yum.repos.d/. 
# Fri, 01 Aug 2025 11:04:34 GMT
CMD ["/bin/bash"]
# Fri, 01 Aug 2025 11:04:34 GMT
COPY file:58cc94f5b3b2d60de2c77a6ed4b1797dcede502ccdb429a72e7a72d994235b3c in /usr/share/buildinfo/content-sets.json 
# Fri, 01 Aug 2025 11:04:34 GMT
COPY file:58cc94f5b3b2d60de2c77a6ed4b1797dcede502ccdb429a72e7a72d994235b3c in /root/buildinfo/content_manifests/content-sets.json 
# Fri, 01 Aug 2025 11:04:34 GMT
COPY file:097ec12a5c22da979b55e75443e50150904b478d4249b64b2431aae8901ea4d2 in /root/buildinfo/labels.json 
# Fri, 01 Aug 2025 11:04:34 GMT
LABEL "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="0c20ee48321f5d64135f6208d1332c0b032df6c3" "org.opencontainers.image.revision"="0c20ee48321f5d64135f6208d1332c0b032df6c3" "build-date"="2025-09-18T08:36:33Z" "release"="1758184547"
# Fri, 01 Aug 2025 11:04:34 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 01 Aug 2025 11:04:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 01 Aug 2025 11:04:34 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 01 Aug 2025 11:04:34 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en     ;     microdnf clean all # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
ENV JAVA_VERSION=jdk-24.0.2+12
# Fri, 01 Aug 2025 11:04:34 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='6f8725d186d05c627176db9c46c732a6ef3ba41d9e9b3775c4727fc8ac642bb2';          BINARY_URL='https://github.com/adoptium/temurin24-binaries/releases/download/jdk-24.0.2%2B12/OpenJDK24U-jdk_aarch64_linux_hotspot_24.0.2_12.tar.gz';          ;;        ppc64le)          ESUM='00f55805b4fa34c2557428e7f43ac847a8af0177ecb0b9dd8a6016f313ec43a9';          BINARY_URL='https://github.com/adoptium/temurin24-binaries/releases/download/jdk-24.0.2%2B12/OpenJDK24U-jdk_ppc64le_linux_hotspot_24.0.2_12.tar.gz';          ;;        s390x)          ESUM='555059f4929ab6435eb83b496d0b969bc6a9a5c07915d5f7607f5d833e38fb39';          BINARY_URL='https://github.com/adoptium/temurin24-binaries/releases/download/jdk-24.0.2%2B12/OpenJDK24U-jdk_s390x_linux_hotspot_24.0.2_12.tar.gz';          ;;        x86_64)          ESUM='aea1cc55e51cf651c85f2f00ad021603fe269c4bb6493fa97a321ad770c9b096';          BINARY_URL='https://github.com/adoptium/temurin24-binaries/releases/download/jdk-24.0.2%2B12/OpenJDK24U-jdk_x64_linux_hotspot_24.0.2_12.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Fri, 01 Aug 2025 11:04:34 GMT
CMD ["jshell"]
# Fri, 19 Sep 2025 14:40:42 GMT
CMD ["gradle"]
# Fri, 19 Sep 2025 14:40:42 GMT
ENV GRADLE_HOME=/opt/gradle
# Fri, 19 Sep 2025 14:40:42 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 101 gradle     && useradd --system --gid gradle --uid 101 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Fri, 19 Sep 2025 14:40:42 GMT
VOLUME [/home/gradle/.gradle]
# Fri, 19 Sep 2025 14:40:42 GMT
WORKDIR /home/gradle
# Fri, 19 Sep 2025 14:40:42 GMT
RUN set -o errexit -o nounset     && microdnf install -y         make                 findutils                 unzip         which                 git         git-lfs         subversion     && microdnf clean all         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which svn # buildkit
# Fri, 19 Sep 2025 14:40:42 GMT
ENV GRADLE_VERSION=9.1.0
# Fri, 19 Sep 2025 14:40:42 GMT
ARG GRADLE_DOWNLOAD_SHA256=a17ddd85a26b6a7f5ddb71ff8b05fc5104c0202c6e64782429790c933686c806
# Fri, 19 Sep 2025 14:40:42 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=a17ddd85a26b6a7f5ddb71ff8b05fc5104c0202c6e64782429790c933686c806
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Fri, 19 Sep 2025 14:40:42 GMT
USER gradle
# Fri, 19 Sep 2025 14:40:42 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=a17ddd85a26b6a7f5ddb71ff8b05fc5104c0202c6e64782429790c933686c806
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Fri, 19 Sep 2025 14:40:42 GMT
USER root
```

-	Layers:
	-	`sha256:9f4bff248214d12c7254dc3c25ef82bd14ff143e2a06d159f2a8cc1c9e6ef1fd`  
		Last Modified: Thu, 18 Sep 2025 15:30:42 GMT  
		Size: 39.6 MB (39648249 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4af5d4b50253b7cf0a1cf05677b5e6c4a456bc860261fe786afa131524a79d9`  
		Last Modified: Fri, 19 Sep 2025 20:45:17 GMT  
		Size: 27.5 MB (27534314 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:746876396ae5cb78921e7f8db425311d589d98c1af68eb722b9b44e35a9553ed`  
		Last Modified: Fri, 19 Sep 2025 20:45:25 GMT  
		Size: 90.0 MB (89974219 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c7568a323d754544473a07cc7fdcaf320be8de8ee4b7f34d48bca9c14c57ef1`  
		Last Modified: Fri, 19 Sep 2025 20:45:14 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c3f9dd15f4812029b79e99856576cc231b2c4307b20af7659de8e4b35cf0bc4`  
		Last Modified: Fri, 19 Sep 2025 20:45:19 GMT  
		Size: 2.3 KB (2290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b3d19c19cb3be536a2de225763ce638d7eead504f15d89441c65b5fdd3ee356`  
		Last Modified: Fri, 19 Sep 2025 21:13:20 GMT  
		Size: 1.7 KB (1707 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ce38078f0e34775baabff9b547825b3a5a3d6cd13e1224b820d917ace240384`  
		Last Modified: Fri, 19 Sep 2025 21:13:24 GMT  
		Size: 36.8 MB (36792642 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7bb07811c7cd64c7670ccc00a3e9824c4d171fac24128ca0d3350d7d57462a7`  
		Last Modified: Sat, 20 Sep 2025 00:15:37 GMT  
		Size: 134.5 MB (134514732 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d383b30d6b166741138e1c70c5c0165512807bddc2e5c227e4b629483d1cb37`  
		Last Modified: Fri, 19 Sep 2025 21:13:21 GMT  
		Size: 54.9 KB (54901 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:9-jdk24-ubi` - unknown; unknown

```console
$ docker pull gradle@sha256:9192138c1cfa0085f2466feeff2de73617055c3cb51f05b813727ba0eaa06a3d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5351108 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:760a1a76e6ba9751598c39a595147c118f649d9dcf23e9598a3f400de000b00d`

```dockerfile
```

-	Layers:
	-	`sha256:1e35d1c2f14f54e6df77bf6634c209707400a16578f843331d38a6129002b097`  
		Last Modified: Fri, 19 Sep 2025 23:25:24 GMT  
		Size: 5.3 MB (5326862 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f68458da230479970041200582c8195d1d04a4076e2d9a033e4a19c63c938edf`  
		Last Modified: Fri, 19 Sep 2025 23:25:25 GMT  
		Size: 24.2 KB (24246 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:9-jdk24-ubi` - linux; arm64 variant v8

```console
$ docker pull gradle@sha256:f59204d4a81827f6633d2b9341e5137cdb064b1e9b0f22d30f4f2f2c65fe0391
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **325.8 MB (325793898 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e12506fe9a81f1262034a4b7d482d9a1e86aa37ae45c17cad947ec0037daa43`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["gradle"]`

```dockerfile
# Fri, 01 Aug 2025 11:04:34 GMT
LABEL maintainer="Red Hat, Inc."
# Fri, 01 Aug 2025 11:04:34 GMT
LABEL vendor="Red Hat, Inc."
# Fri, 01 Aug 2025 11:04:34 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Fri, 01 Aug 2025 11:04:34 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.6"       distribution-scope="public"
# Fri, 01 Aug 2025 11:04:34 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Fri, 01 Aug 2025 11:04:34 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Fri, 01 Aug 2025 11:04:34 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Fri, 01 Aug 2025 11:04:34 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Fri, 01 Aug 2025 11:04:34 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Fri, 01 Aug 2025 11:04:34 GMT
LABEL io.openshift.expose-services=""
# Fri, 01 Aug 2025 11:04:34 GMT
LABEL io.openshift.tags="minimal rhel9"
# Fri, 01 Aug 2025 11:04:34 GMT
ENV container oci
# Fri, 01 Aug 2025 11:04:34 GMT
COPY dir:9f6ea5fd9a48598d911c3860918a4b145eb452cb81a81a77f69e1ed6481637df in / 
# Fri, 01 Aug 2025 11:04:34 GMT
COPY file:b37d593713ee21ad52a4cd1424dc019a24f7966f85df0ac4b86d234302695328 in /etc/yum.repos.d/. 
# Fri, 01 Aug 2025 11:04:34 GMT
CMD ["/bin/bash"]
# Fri, 01 Aug 2025 11:04:34 GMT
COPY file:0667e9d31385a24c3aef13f2dd9ab6a7b71b3dfcfef5127d3c1e2ea2c838e5cb in /usr/share/buildinfo/content-sets.json 
# Fri, 01 Aug 2025 11:04:34 GMT
COPY file:0667e9d31385a24c3aef13f2dd9ab6a7b71b3dfcfef5127d3c1e2ea2c838e5cb in /root/buildinfo/content_manifests/content-sets.json 
# Fri, 01 Aug 2025 11:04:34 GMT
COPY file:f5f06837bcbb5ebacc66d8764dd5ddb2c916d273cd4f80d9b8b34880aba3bbeb in /root/buildinfo/labels.json 
# Fri, 01 Aug 2025 11:04:34 GMT
LABEL "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="0c20ee48321f5d64135f6208d1332c0b032df6c3" "org.opencontainers.image.revision"="0c20ee48321f5d64135f6208d1332c0b032df6c3" "build-date"="2025-09-18T08:39:36Z" "release"="1758184547"
# Fri, 01 Aug 2025 11:04:34 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 01 Aug 2025 11:04:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 01 Aug 2025 11:04:34 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 01 Aug 2025 11:04:34 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en     ;     microdnf clean all # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
ENV JAVA_VERSION=jdk-24.0.2+12
# Fri, 01 Aug 2025 11:04:34 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='6f8725d186d05c627176db9c46c732a6ef3ba41d9e9b3775c4727fc8ac642bb2';          BINARY_URL='https://github.com/adoptium/temurin24-binaries/releases/download/jdk-24.0.2%2B12/OpenJDK24U-jdk_aarch64_linux_hotspot_24.0.2_12.tar.gz';          ;;        ppc64le)          ESUM='00f55805b4fa34c2557428e7f43ac847a8af0177ecb0b9dd8a6016f313ec43a9';          BINARY_URL='https://github.com/adoptium/temurin24-binaries/releases/download/jdk-24.0.2%2B12/OpenJDK24U-jdk_ppc64le_linux_hotspot_24.0.2_12.tar.gz';          ;;        s390x)          ESUM='555059f4929ab6435eb83b496d0b969bc6a9a5c07915d5f7607f5d833e38fb39';          BINARY_URL='https://github.com/adoptium/temurin24-binaries/releases/download/jdk-24.0.2%2B12/OpenJDK24U-jdk_s390x_linux_hotspot_24.0.2_12.tar.gz';          ;;        x86_64)          ESUM='aea1cc55e51cf651c85f2f00ad021603fe269c4bb6493fa97a321ad770c9b096';          BINARY_URL='https://github.com/adoptium/temurin24-binaries/releases/download/jdk-24.0.2%2B12/OpenJDK24U-jdk_x64_linux_hotspot_24.0.2_12.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Fri, 01 Aug 2025 11:04:34 GMT
CMD ["jshell"]
# Fri, 19 Sep 2025 14:40:42 GMT
CMD ["gradle"]
# Fri, 19 Sep 2025 14:40:42 GMT
ENV GRADLE_HOME=/opt/gradle
# Fri, 19 Sep 2025 14:40:42 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 101 gradle     && useradd --system --gid gradle --uid 101 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Fri, 19 Sep 2025 14:40:42 GMT
VOLUME [/home/gradle/.gradle]
# Fri, 19 Sep 2025 14:40:42 GMT
WORKDIR /home/gradle
# Fri, 19 Sep 2025 14:40:42 GMT
RUN set -o errexit -o nounset     && microdnf install -y         make                 findutils                 unzip         which                 git         git-lfs         subversion     && microdnf clean all         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which svn # buildkit
# Fri, 19 Sep 2025 14:40:42 GMT
ENV GRADLE_VERSION=9.1.0
# Fri, 19 Sep 2025 14:40:42 GMT
ARG GRADLE_DOWNLOAD_SHA256=a17ddd85a26b6a7f5ddb71ff8b05fc5104c0202c6e64782429790c933686c806
# Fri, 19 Sep 2025 14:40:42 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=a17ddd85a26b6a7f5ddb71ff8b05fc5104c0202c6e64782429790c933686c806
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Fri, 19 Sep 2025 14:40:42 GMT
USER gradle
# Fri, 19 Sep 2025 14:40:42 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=a17ddd85a26b6a7f5ddb71ff8b05fc5104c0202c6e64782429790c933686c806
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Fri, 19 Sep 2025 14:40:42 GMT
USER root
```

-	Layers:
	-	`sha256:a9f9218e937ae927e68fe68d00604365ddda1b238616443bc0a4b9e574067342`  
		Last Modified: Thu, 18 Sep 2025 15:44:52 GMT  
		Size: 37.9 MB (37900151 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac650a9e81555db96efb5d02472d4cbbcd8423ec4bd98a5355cc81ba637b5bd8`  
		Last Modified: Fri, 19 Sep 2025 20:44:52 GMT  
		Size: 28.0 MB (27977177 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78704386bfa8b32114107e509dd7bf9ece2cd563368cd3b7c63aaae2acdd1e11`  
		Last Modified: Fri, 19 Sep 2025 20:45:07 GMT  
		Size: 89.1 MB (89100493 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9bfa639ca5cffc4c6ad3c42133a02f67b609629e203f3ea68aaf842bababda95`  
		Last Modified: Fri, 19 Sep 2025 20:44:50 GMT  
		Size: 130.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39a35fb2bf5a9e82f8ab81973e0abdf2c4ca632632d5c1c94c3ec81117875e9f`  
		Last Modified: Fri, 19 Sep 2025 20:44:50 GMT  
		Size: 2.3 KB (2290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4646073d02b4e63153e3229ca2a6f80b0bfa41183e4db3eff6c6c605e80b97ec`  
		Last Modified: Fri, 19 Sep 2025 21:13:21 GMT  
		Size: 1.7 KB (1707 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df619ea11e8255c21d5e7babef69808957fcd99b426c6d4e9788d58712d03682`  
		Last Modified: Fri, 19 Sep 2025 21:13:23 GMT  
		Size: 36.2 MB (36237708 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3bd60f0994acf0ddd1fc3c74379b7cf37cbc7194cd1387e2e206f76c17cd99a`  
		Last Modified: Sat, 20 Sep 2025 00:22:00 GMT  
		Size: 134.5 MB (134514683 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c671e57fa749977050e06ca157f07873ade0cb441042d0620213541a696af873`  
		Last Modified: Fri, 19 Sep 2025 21:13:21 GMT  
		Size: 59.5 KB (59527 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:9-jdk24-ubi` - unknown; unknown

```console
$ docker pull gradle@sha256:33de51d41754d0b785beccf90ca9471b36a059e90bc2dd47c8c2a0d805f0cf70
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5350734 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9474309dbdcf3300310d6734d7457c174ef935b00f029544a512a6a9c6ad2462`

```dockerfile
```

-	Layers:
	-	`sha256:4d73281048c06913a3edc6c44245d50b52dea97f051c51fdcc2b663523777346`  
		Last Modified: Fri, 19 Sep 2025 23:25:30 GMT  
		Size: 5.3 MB (5326291 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e54100bd4c6c0c7105235193a3894f227c5e5c6e885c5c40e0220882567675f0`  
		Last Modified: Fri, 19 Sep 2025 23:25:31 GMT  
		Size: 24.4 KB (24443 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:9-jdk24-ubi` - linux; ppc64le

```console
$ docker pull gradle@sha256:76b980fdc141ab41646247032606088a281ddb71d6943723f8add6f316eaa475
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **336.6 MB (336639319 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c1d4ef3056a928de51c51c93927ba23c0e4644e4fd20566fe05d16c33376799`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["gradle"]`

```dockerfile
# Fri, 01 Aug 2025 11:04:34 GMT
LABEL maintainer="Red Hat, Inc."
# Fri, 01 Aug 2025 11:04:34 GMT
LABEL vendor="Red Hat, Inc."
# Fri, 01 Aug 2025 11:04:34 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Fri, 01 Aug 2025 11:04:34 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.6"       distribution-scope="public"
# Fri, 01 Aug 2025 11:04:34 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Fri, 01 Aug 2025 11:04:34 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Fri, 01 Aug 2025 11:04:34 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Fri, 01 Aug 2025 11:04:34 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Fri, 01 Aug 2025 11:04:34 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Fri, 01 Aug 2025 11:04:34 GMT
LABEL io.openshift.expose-services=""
# Fri, 01 Aug 2025 11:04:34 GMT
LABEL io.openshift.tags="minimal rhel9"
# Fri, 01 Aug 2025 11:04:34 GMT
ENV container oci
# Fri, 01 Aug 2025 11:04:34 GMT
COPY dir:d2207f84596636cf1f42082a4111b6c38656ec970ae8b2e1ce2cacd7d29f1510 in / 
# Fri, 01 Aug 2025 11:04:34 GMT
COPY file:b37d593713ee21ad52a4cd1424dc019a24f7966f85df0ac4b86d234302695328 in /etc/yum.repos.d/. 
# Fri, 01 Aug 2025 11:04:34 GMT
CMD ["/bin/bash"]
# Fri, 01 Aug 2025 11:04:34 GMT
COPY file:0667e9d31385a24c3aef13f2dd9ab6a7b71b3dfcfef5127d3c1e2ea2c838e5cb in /usr/share/buildinfo/content-sets.json 
# Fri, 01 Aug 2025 11:04:34 GMT
COPY file:0667e9d31385a24c3aef13f2dd9ab6a7b71b3dfcfef5127d3c1e2ea2c838e5cb in /root/buildinfo/content_manifests/content-sets.json 
# Fri, 01 Aug 2025 11:04:34 GMT
LABEL "build-date"="2025-08-20T13:11:42" "architecture"="ppc64le" "vcs-type"="git" "vcs-ref"="f4b088292653bbf5ca8188a5e59ffd06a8671d4b" "release"="1755695350"
# Fri, 01 Aug 2025 11:04:34 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 01 Aug 2025 11:04:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 01 Aug 2025 11:04:34 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 01 Aug 2025 11:04:34 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en     ;     microdnf clean all # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
ENV JAVA_VERSION=jdk-24.0.2+12
# Fri, 01 Aug 2025 11:04:34 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='6f8725d186d05c627176db9c46c732a6ef3ba41d9e9b3775c4727fc8ac642bb2';          BINARY_URL='https://github.com/adoptium/temurin24-binaries/releases/download/jdk-24.0.2%2B12/OpenJDK24U-jdk_aarch64_linux_hotspot_24.0.2_12.tar.gz';          ;;        ppc64le)          ESUM='00f55805b4fa34c2557428e7f43ac847a8af0177ecb0b9dd8a6016f313ec43a9';          BINARY_URL='https://github.com/adoptium/temurin24-binaries/releases/download/jdk-24.0.2%2B12/OpenJDK24U-jdk_ppc64le_linux_hotspot_24.0.2_12.tar.gz';          ;;        s390x)          ESUM='555059f4929ab6435eb83b496d0b969bc6a9a5c07915d5f7607f5d833e38fb39';          BINARY_URL='https://github.com/adoptium/temurin24-binaries/releases/download/jdk-24.0.2%2B12/OpenJDK24U-jdk_s390x_linux_hotspot_24.0.2_12.tar.gz';          ;;        x86_64)          ESUM='aea1cc55e51cf651c85f2f00ad021603fe269c4bb6493fa97a321ad770c9b096';          BINARY_URL='https://github.com/adoptium/temurin24-binaries/releases/download/jdk-24.0.2%2B12/OpenJDK24U-jdk_x64_linux_hotspot_24.0.2_12.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Fri, 01 Aug 2025 11:04:34 GMT
CMD ["jshell"]
# Fri, 19 Sep 2025 14:40:42 GMT
CMD ["gradle"]
# Fri, 19 Sep 2025 14:40:42 GMT
ENV GRADLE_HOME=/opt/gradle
# Fri, 19 Sep 2025 14:40:42 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 101 gradle     && useradd --system --gid gradle --uid 101 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Fri, 19 Sep 2025 14:40:42 GMT
VOLUME [/home/gradle/.gradle]
# Fri, 19 Sep 2025 14:40:42 GMT
WORKDIR /home/gradle
# Fri, 19 Sep 2025 14:40:42 GMT
RUN set -o errexit -o nounset     && microdnf install -y         make                 findutils                 unzip         which                 git         git-lfs         subversion     && microdnf clean all         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which svn # buildkit
# Fri, 19 Sep 2025 14:40:42 GMT
ENV GRADLE_VERSION=9.1.0
# Fri, 19 Sep 2025 14:40:42 GMT
ARG GRADLE_DOWNLOAD_SHA256=a17ddd85a26b6a7f5ddb71ff8b05fc5104c0202c6e64782429790c933686c806
# Fri, 19 Sep 2025 14:40:42 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=a17ddd85a26b6a7f5ddb71ff8b05fc5104c0202c6e64782429790c933686c806
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Fri, 19 Sep 2025 14:40:42 GMT
USER gradle
# Fri, 19 Sep 2025 14:40:42 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=a17ddd85a26b6a7f5ddb71ff8b05fc5104c0202c6e64782429790c933686c806
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Fri, 19 Sep 2025 14:40:42 GMT
USER root
```

-	Layers:
	-	`sha256:ebd7c9ee3cc0108f33ad80f84c3da96a78c10cc76b3dfe38b2b8ab879a83a307`  
		Last Modified: Wed, 20 Aug 2025 18:13:19 GMT  
		Size: 44.1 MB (44057494 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b9b8d104c4d92c5fde801246053d3fe5d18514fbdb85ec097aafc6d73271add`  
		Last Modified: Thu, 21 Aug 2025 18:58:27 GMT  
		Size: 30.0 MB (29977366 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b47ae6a8841c8c80b698da50154046aadba3c0dacc3a01bbd4dec94c5874748f`  
		Last Modified: Fri, 22 Aug 2025 18:12:13 GMT  
		Size: 89.9 MB (89925034 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6e4272ad432728ee97f183fca1457a0bea75b2c825574f653ef58a205126b87`  
		Last Modified: Thu, 21 Aug 2025 19:13:13 GMT  
		Size: 130.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0eba3a5891e4721fce130ee1ec4f2e7d2a84dc078af4e760ccae7742827e735e`  
		Last Modified: Thu, 21 Aug 2025 19:13:06 GMT  
		Size: 2.3 KB (2290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e93f29b3a25f3fb39a7b84eaa28c195015325d6a10944b9953d9ed7a3b3c7b9`  
		Last Modified: Fri, 19 Sep 2025 17:47:10 GMT  
		Size: 1.7 KB (1720 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:687e4b10977e3d1707550cd76fb5d7dc18229713accef6ff11e7a67f7923da4a`  
		Last Modified: Fri, 19 Sep 2025 17:47:15 GMT  
		Size: 38.1 MB (38125566 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b96f45bc1f048b90943f6d6022f5a7c1c96b2a9a27d415d0e2bffc4cc4625b5`  
		Last Modified: Fri, 19 Sep 2025 17:46:56 GMT  
		Size: 134.5 MB (134514680 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1f7e3a501d036f308b87c1dcbe3d08422df3aec83566f1d37d81a36b87271f9`  
		Last Modified: Fri, 19 Sep 2025 17:47:10 GMT  
		Size: 35.0 KB (35007 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:9-jdk24-ubi` - unknown; unknown

```console
$ docker pull gradle@sha256:ac5919aa6d7e317a6847faf321cc8dc2e941d3c1cdad01ea23a2c39258b13cbc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5349809 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e92db4ceabbc7a6ac11192a268ff8697544283a4a9aaf2e57eafb2ed0cd29584`

```dockerfile
```

-	Layers:
	-	`sha256:34f24d4c2b50ffba56f9ffdbbd9901d4c4091fa5ed6c7e389fa01e17fcf7197c`  
		Last Modified: Fri, 19 Sep 2025 20:27:05 GMT  
		Size: 5.3 MB (5325489 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bbd85971576db96c383e3d9949d54040a7af927751600c34a37ea740db56fd33`  
		Last Modified: Fri, 19 Sep 2025 20:27:06 GMT  
		Size: 24.3 KB (24320 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:9-jdk24-ubi` - linux; s390x

```console
$ docker pull gradle@sha256:eabc47aa21208c41733d300b6fd1a39b99ac9a4d0d2739ba49119d8f6e435293
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **321.5 MB (321545718 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b69dce4868afec29e533532269439f5a65df6842bf3b795649d37eaeb1e8a6a7`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["gradle"]`

```dockerfile
# Fri, 01 Aug 2025 11:04:34 GMT
LABEL maintainer="Red Hat, Inc."
# Fri, 01 Aug 2025 11:04:34 GMT
LABEL vendor="Red Hat, Inc."
# Fri, 01 Aug 2025 11:04:34 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Fri, 01 Aug 2025 11:04:34 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.6"       distribution-scope="public"
# Fri, 01 Aug 2025 11:04:34 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Fri, 01 Aug 2025 11:04:34 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Fri, 01 Aug 2025 11:04:34 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Fri, 01 Aug 2025 11:04:34 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Fri, 01 Aug 2025 11:04:34 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Fri, 01 Aug 2025 11:04:34 GMT
LABEL io.openshift.expose-services=""
# Fri, 01 Aug 2025 11:04:34 GMT
LABEL io.openshift.tags="minimal rhel9"
# Fri, 01 Aug 2025 11:04:34 GMT
ENV container oci
# Fri, 01 Aug 2025 11:04:34 GMT
COPY dir:ca02a93ff70da2bab2b2f1d0d7fd03fa68c8a6658034c4646addb693d26890ce in / 
# Fri, 01 Aug 2025 11:04:34 GMT
COPY file:b37d593713ee21ad52a4cd1424dc019a24f7966f85df0ac4b86d234302695328 in /etc/yum.repos.d/. 
# Fri, 01 Aug 2025 11:04:34 GMT
CMD ["/bin/bash"]
# Fri, 01 Aug 2025 11:04:34 GMT
COPY file:0667e9d31385a24c3aef13f2dd9ab6a7b71b3dfcfef5127d3c1e2ea2c838e5cb in /usr/share/buildinfo/content-sets.json 
# Fri, 01 Aug 2025 11:04:34 GMT
COPY file:0667e9d31385a24c3aef13f2dd9ab6a7b71b3dfcfef5127d3c1e2ea2c838e5cb in /root/buildinfo/content_manifests/content-sets.json 
# Fri, 01 Aug 2025 11:04:34 GMT
COPY file:619acf656a444acd42301f36c5665fddce29fe2436cec48d428c3348227c6877 in /root/buildinfo/labels.json 
# Fri, 01 Aug 2025 11:04:34 GMT
LABEL "architecture"="s390x" "vcs-type"="git" "vcs-ref"="0c20ee48321f5d64135f6208d1332c0b032df6c3" "org.opencontainers.image.revision"="0c20ee48321f5d64135f6208d1332c0b032df6c3" "build-date"="2025-09-18T08:47:22Z" "release"="1758184547"
# Fri, 01 Aug 2025 11:04:34 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 01 Aug 2025 11:04:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 01 Aug 2025 11:04:34 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 01 Aug 2025 11:04:34 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en     ;     microdnf clean all # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
ENV JAVA_VERSION=jdk-24.0.2+12
# Fri, 01 Aug 2025 11:04:34 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='6f8725d186d05c627176db9c46c732a6ef3ba41d9e9b3775c4727fc8ac642bb2';          BINARY_URL='https://github.com/adoptium/temurin24-binaries/releases/download/jdk-24.0.2%2B12/OpenJDK24U-jdk_aarch64_linux_hotspot_24.0.2_12.tar.gz';          ;;        ppc64le)          ESUM='00f55805b4fa34c2557428e7f43ac847a8af0177ecb0b9dd8a6016f313ec43a9';          BINARY_URL='https://github.com/adoptium/temurin24-binaries/releases/download/jdk-24.0.2%2B12/OpenJDK24U-jdk_ppc64le_linux_hotspot_24.0.2_12.tar.gz';          ;;        s390x)          ESUM='555059f4929ab6435eb83b496d0b969bc6a9a5c07915d5f7607f5d833e38fb39';          BINARY_URL='https://github.com/adoptium/temurin24-binaries/releases/download/jdk-24.0.2%2B12/OpenJDK24U-jdk_s390x_linux_hotspot_24.0.2_12.tar.gz';          ;;        x86_64)          ESUM='aea1cc55e51cf651c85f2f00ad021603fe269c4bb6493fa97a321ad770c9b096';          BINARY_URL='https://github.com/adoptium/temurin24-binaries/releases/download/jdk-24.0.2%2B12/OpenJDK24U-jdk_x64_linux_hotspot_24.0.2_12.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Fri, 01 Aug 2025 11:04:34 GMT
CMD ["jshell"]
# Fri, 19 Sep 2025 14:40:42 GMT
CMD ["gradle"]
# Fri, 19 Sep 2025 14:40:42 GMT
ENV GRADLE_HOME=/opt/gradle
# Fri, 19 Sep 2025 14:40:42 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 101 gradle     && useradd --system --gid gradle --uid 101 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Fri, 19 Sep 2025 14:40:42 GMT
VOLUME [/home/gradle/.gradle]
# Fri, 19 Sep 2025 14:40:42 GMT
WORKDIR /home/gradle
# Fri, 19 Sep 2025 14:40:42 GMT
RUN set -o errexit -o nounset     && microdnf install -y         make                 findutils                 unzip         which                 git         git-lfs         subversion     && microdnf clean all         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which svn # buildkit
# Fri, 19 Sep 2025 14:40:42 GMT
ENV GRADLE_VERSION=9.1.0
# Fri, 19 Sep 2025 14:40:42 GMT
ARG GRADLE_DOWNLOAD_SHA256=a17ddd85a26b6a7f5ddb71ff8b05fc5104c0202c6e64782429790c933686c806
# Fri, 19 Sep 2025 14:40:42 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=a17ddd85a26b6a7f5ddb71ff8b05fc5104c0202c6e64782429790c933686c806
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Fri, 19 Sep 2025 14:40:42 GMT
USER gradle
# Fri, 19 Sep 2025 14:40:42 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=a17ddd85a26b6a7f5ddb71ff8b05fc5104c0202c6e64782429790c933686c806
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Fri, 19 Sep 2025 14:40:42 GMT
USER root
```

-	Layers:
	-	`sha256:b322a817ffd9f83026b8f9efe6c6ddcc3a31ddf2949fc8f9081c2189682f7ec8`  
		Last Modified: Thu, 18 Sep 2025 18:10:26 GMT  
		Size: 37.8 MB (37776263 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed621710547cce0ed2f7e6267cba0e2a3b03a4580b06ded38ff3c5d6fa70e078`  
		Last Modified: Fri, 19 Sep 2025 21:49:25 GMT  
		Size: 27.6 MB (27571560 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69863d0e73b26e2bd5e2d4390cfc9440cf3f4a9c0e3f57a61149eb788aecb05c`  
		Last Modified: Fri, 19 Sep 2025 22:01:53 GMT  
		Size: 85.2 MB (85226385 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6902f5d2e1ac6abb045ac0f06e5679af3de73f1a7fdd29376d4d05b0b0a89e70`  
		Last Modified: Fri, 19 Sep 2025 22:01:48 GMT  
		Size: 130.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb610dbe4e5c0ff8b7c4b0ad6cc9c526c99d19c4f89f384f178e154e131a6cc6`  
		Last Modified: Fri, 19 Sep 2025 22:01:48 GMT  
		Size: 2.3 KB (2290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f66dc24b147cfcec9a998abf1ca7a0abb774ce67a0cec9ed37a7bb3dc1a33b0`  
		Last Modified: Fri, 19 Sep 2025 22:18:48 GMT  
		Size: 1.7 KB (1707 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79911bf26b2a8aa738481967c99933f152abeec164bd20a587068f8ed455d0e0`  
		Last Modified: Fri, 19 Sep 2025 22:18:50 GMT  
		Size: 36.4 MB (36417669 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:904dfed6bd3e61776b67fe223569067480d296feafd16edad0fe196781550ebf`  
		Last Modified: Fri, 19 Sep 2025 22:18:30 GMT  
		Size: 134.5 MB (134514678 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35c74135008cc72fbc12b51489cedb5a73ee00553706c57d8e65b6e5013d0fc5`  
		Last Modified: Fri, 19 Sep 2025 22:18:48 GMT  
		Size: 35.0 KB (35004 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:9-jdk24-ubi` - unknown; unknown

```console
$ docker pull gradle@sha256:6544c5eb0467d7304cd452718fed0325aa8bc95a38603b112134abe4e01d1302
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5340263 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a1f4c73c3e092731612b78ce62bce56955f3e6b53c52d57df6e2acd4e81db057`

```dockerfile
```

-	Layers:
	-	`sha256:e24637f7efcfb7a01ec8acf941df43a28ba3bf48a21bf2915ca141763d404f0f`  
		Last Modified: Fri, 19 Sep 2025 23:25:39 GMT  
		Size: 5.3 MB (5316017 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7872ceaa23207dd9c481099cd84291bd1e1c5c55ace7578808fd373af36ae420`  
		Last Modified: Fri, 19 Sep 2025 23:25:39 GMT  
		Size: 24.2 KB (24246 bytes)  
		MIME: application/vnd.in-toto+json
