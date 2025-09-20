## `gradle:7-jdk11-ubi`

```console
$ docker pull gradle@sha256:25e39bb5d7090db99d8dc76e60920c12716ed5be8d682410c55981eaab95e21d
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

### `gradle:7-jdk11-ubi` - linux; amd64

```console
$ docker pull gradle@sha256:2dd6b9e7e8ff4219553e184268cd13f8406000cb4976b237e8a362f6e54ee014
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **374.6 MB (374621658 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fdc69b6270c43c5d38e2e9861bd1bf3d3a52d0a559e228f352db9ca0a696036c`
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
ENV JAVA_VERSION=jdk-11.0.28+6
# Fri, 01 Aug 2025 11:04:34 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='32c316cb3998a9c9dee2829fbb577ea1c0ed666700cec73e049d44c342bb19af';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.28%2B6/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.28_6.tar.gz';          ;;        ppc64le)          ESUM='e272abd162b3de68093630929453feba3e63a5ab1bbb912379f6a4aa968ef06a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.28%2B6/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.28_6.tar.gz';          ;;        s390x)          ESUM='ac3f94fdcc5372e90f44fad9cd03ec0e3fd3535fea06c120f85e4a7534c6de04';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.28%2B6/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.28_6.tar.gz';          ;;        x86_64)          ESUM='7dfd551795a8884b26cbb02e0301da95db40160bb194f48271dc2ef9367f50c2';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.28%2B6/OpenJDK11U-jdk_x64_linux_hotspot_11.0.28_6.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Fri, 01 Aug 2025 11:04:34 GMT
CMD ["jshell"]
# Wed, 10 Sep 2025 15:58:43 GMT
CMD ["gradle"]
# Wed, 10 Sep 2025 15:58:43 GMT
ENV GRADLE_HOME=/opt/gradle
# Wed, 10 Sep 2025 15:58:43 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 101 gradle     && useradd --system --gid gradle --uid 101 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Wed, 10 Sep 2025 15:58:43 GMT
VOLUME [/home/gradle/.gradle]
# Wed, 10 Sep 2025 15:58:43 GMT
WORKDIR /home/gradle
# Wed, 10 Sep 2025 15:58:43 GMT
RUN set -o errexit -o nounset     && microdnf install -y         make                 findutils                 unzip         which                 git         git-lfs         subversion     && microdnf clean all         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which svn # buildkit
# Wed, 10 Sep 2025 15:58:43 GMT
ENV GRADLE_VERSION=7.6.6
# Wed, 10 Sep 2025 15:58:43 GMT
ARG GRADLE_DOWNLOAD_SHA256=673d9776f303bc7048fc3329d232d6ebf1051b07893bd9d11616fad9a8673be0
# Wed, 10 Sep 2025 15:58:43 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=673d9776f303bc7048fc3329d232d6ebf1051b07893bd9d11616fad9a8673be0
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Wed, 10 Sep 2025 15:58:43 GMT
USER gradle
# Wed, 10 Sep 2025 15:58:43 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=673d9776f303bc7048fc3329d232d6ebf1051b07893bd9d11616fad9a8673be0
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Wed, 10 Sep 2025 15:58:43 GMT
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
	-	`sha256:329e326b4294f3bb6780b01364b3a84ecb816220cc3b31ed9de34c314d9bf6b4`  
		Last Modified: Fri, 19 Sep 2025 21:13:17 GMT  
		Size: 142.1 MB (142117857 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:edafe681d37a19ed6e9e00623530db6c907559f91649eb73cff083fc6632f5f3`  
		Last Modified: Fri, 19 Sep 2025 21:13:01 GMT  
		Size: 130.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72eaa86f2cf53e072b3bcf745361c883f94d802401892bd293d064702bb66011`  
		Last Modified: Fri, 19 Sep 2025 21:13:01 GMT  
		Size: 2.3 KB (2290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7548702896794f05e4b7d07473e789536fde387971dde0ae09394c47c5353d77`  
		Last Modified: Fri, 19 Sep 2025 21:59:23 GMT  
		Size: 1.7 KB (1706 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c85a230ae70152e468bf18bf2bb8dc106c4a9fdb4a2aac8c2b4876eae1c3bcf`  
		Last Modified: Fri, 19 Sep 2025 21:13:44 GMT  
		Size: 36.8 MB (36792764 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0dc0f7f81818b9598882eccb01a2531719132ca68d841f8f474fc133d6e35d9f`  
		Last Modified: Fri, 19 Sep 2025 21:13:46 GMT  
		Size: 128.5 MB (128469411 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0eeb7b92a7b04f7b22be0f587c86273e6d0cf61048f35c02c676e621dfe5a0ef`  
		Last Modified: Fri, 19 Sep 2025 21:59:23 GMT  
		Size: 54.9 KB (54905 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:7-jdk11-ubi` - unknown; unknown

```console
$ docker pull gradle@sha256:d923aa52946df65d2b8c610fa2c057bff06d50caf9128ed9722eacbaecbd5370
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5341906 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2ad7f00db96fa11b65b423c3d8bc02c19a1a23869b8c153846eebd1cf20ca598`

```dockerfile
```

-	Layers:
	-	`sha256:35d096db574f621e2c0bf0bf6f1b488579720c6c2b7e62e6e2f9cdb07bbdb483`  
		Last Modified: Fri, 19 Sep 2025 23:18:52 GMT  
		Size: 5.3 MB (5318278 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:173bb858710735437a6bdf869ddc6a0b7cca364489c63a45192bf2863f864aa5`  
		Last Modified: Fri, 19 Sep 2025 23:18:53 GMT  
		Size: 23.6 KB (23628 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:7-jdk11-ubi` - linux; arm64 variant v8

```console
$ docker pull gradle@sha256:d0e6355e5908b2a20fdbf913c375db32ed990cb20d22cce0eebe86c73a56c422
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **369.6 MB (369571795 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:81a48e2502b4a94bb3a5045ef40f24a24feab26f109850c68866c47201a12ac3`
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
ENV JAVA_VERSION=jdk-11.0.28+6
# Fri, 01 Aug 2025 11:04:34 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='32c316cb3998a9c9dee2829fbb577ea1c0ed666700cec73e049d44c342bb19af';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.28%2B6/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.28_6.tar.gz';          ;;        ppc64le)          ESUM='e272abd162b3de68093630929453feba3e63a5ab1bbb912379f6a4aa968ef06a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.28%2B6/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.28_6.tar.gz';          ;;        s390x)          ESUM='ac3f94fdcc5372e90f44fad9cd03ec0e3fd3535fea06c120f85e4a7534c6de04';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.28%2B6/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.28_6.tar.gz';          ;;        x86_64)          ESUM='7dfd551795a8884b26cbb02e0301da95db40160bb194f48271dc2ef9367f50c2';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.28%2B6/OpenJDK11U-jdk_x64_linux_hotspot_11.0.28_6.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Fri, 01 Aug 2025 11:04:34 GMT
CMD ["jshell"]
# Wed, 10 Sep 2025 15:58:43 GMT
CMD ["gradle"]
# Wed, 10 Sep 2025 15:58:43 GMT
ENV GRADLE_HOME=/opt/gradle
# Wed, 10 Sep 2025 15:58:43 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 101 gradle     && useradd --system --gid gradle --uid 101 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Wed, 10 Sep 2025 15:58:43 GMT
VOLUME [/home/gradle/.gradle]
# Wed, 10 Sep 2025 15:58:43 GMT
WORKDIR /home/gradle
# Wed, 10 Sep 2025 15:58:43 GMT
RUN set -o errexit -o nounset     && microdnf install -y         make                 findutils                 unzip         which                 git         git-lfs         subversion     && microdnf clean all         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which svn # buildkit
# Wed, 10 Sep 2025 15:58:43 GMT
ENV GRADLE_VERSION=7.6.6
# Wed, 10 Sep 2025 15:58:43 GMT
ARG GRADLE_DOWNLOAD_SHA256=673d9776f303bc7048fc3329d232d6ebf1051b07893bd9d11616fad9a8673be0
# Wed, 10 Sep 2025 15:58:43 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=673d9776f303bc7048fc3329d232d6ebf1051b07893bd9d11616fad9a8673be0
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Wed, 10 Sep 2025 15:58:43 GMT
USER gradle
# Wed, 10 Sep 2025 15:58:43 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=673d9776f303bc7048fc3329d232d6ebf1051b07893bd9d11616fad9a8673be0
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Wed, 10 Sep 2025 15:58:43 GMT
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
	-	`sha256:8c584e6a6ea6e8823d4f9df3748cc3ad4cbc45ba1a2b8d1cf91eaa549bbe90f9`  
		Last Modified: Fri, 19 Sep 2025 21:13:09 GMT  
		Size: 138.9 MB (138923665 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:606da87aca921bc3a1fecfa3666273abc8150b39295a0462873aa8512c74f87f`  
		Last Modified: Fri, 19 Sep 2025 21:12:54 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31b9b91cb98245f3f30ef66d8551908148872b672eeb4736f6ded61379610015`  
		Last Modified: Fri, 19 Sep 2025 21:12:54 GMT  
		Size: 2.3 KB (2290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4147c24961c3172259d3cc29a5c55105a4b35faa88b55661e0b3bd45268535b`  
		Last Modified: Fri, 19 Sep 2025 21:14:08 GMT  
		Size: 1.7 KB (1708 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:876bb156fc033d3c1ad7d79776bccb2c28834315f32af5e9d8ab0e599e1c43d2`  
		Last Modified: Fri, 19 Sep 2025 21:14:12 GMT  
		Size: 36.2 MB (36237714 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4339c3ac0dc0e4a6ddecd3363d9b16ed50811232155a0ffc662cb9c8beb0254`  
		Last Modified: Fri, 19 Sep 2025 21:13:38 GMT  
		Size: 128.5 MB (128469411 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:758027c2c18860df47fb562ad4dbf39e5a7d53d31278ee612bfaf4c885756b0a`  
		Last Modified: Fri, 19 Sep 2025 21:14:08 GMT  
		Size: 59.5 KB (59518 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:7-jdk11-ubi` - unknown; unknown

```console
$ docker pull gradle@sha256:cda542dc3c8533187929d7a293e0004a4b4b66caf74d350cb2135b70b6cdd0f6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5342105 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:acebd43b84f404de63157986f04ab3d785b73bd21c7ddedc60f7525155e00fa9`

```dockerfile
```

-	Layers:
	-	`sha256:6efa6043692353e973b9ab77ec9ab1a78d0fa43998c1e2b4cd68885c11f699b2`  
		Last Modified: Fri, 19 Sep 2025 23:18:58 GMT  
		Size: 5.3 MB (5318304 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7cac379fca01e525ccf56fd089f50fd146e11db143594557e975d80d94c44704`  
		Last Modified: Fri, 19 Sep 2025 23:18:59 GMT  
		Size: 23.8 KB (23801 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:7-jdk11-ubi` - linux; ppc64le

```console
$ docker pull gradle@sha256:c942525d462565b2153bd0456a585088522eea71db62a1c0ac186ddf151dec4a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **370.0 MB (370025639 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2727b8b95a802ad5e6e546cd1d0e262c549d38e9503ddf044fc904d385e9858e`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["gradle"]`

```dockerfile
# Sat, 05 Jul 2025 02:17:41 GMT
LABEL maintainer="Red Hat, Inc."
# Sat, 05 Jul 2025 02:17:41 GMT
LABEL vendor="Red Hat, Inc."
# Sat, 05 Jul 2025 02:17:41 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Sat, 05 Jul 2025 02:17:41 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.6"       distribution-scope="public"
# Sat, 05 Jul 2025 02:17:41 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Sat, 05 Jul 2025 02:17:41 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Sat, 05 Jul 2025 02:17:41 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Sat, 05 Jul 2025 02:17:41 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Sat, 05 Jul 2025 02:17:41 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Sat, 05 Jul 2025 02:17:41 GMT
LABEL io.openshift.expose-services=""
# Sat, 05 Jul 2025 02:17:41 GMT
LABEL io.openshift.tags="minimal rhel9"
# Sat, 05 Jul 2025 02:17:41 GMT
ENV container oci
# Sat, 05 Jul 2025 02:17:41 GMT
COPY dir:d2207f84596636cf1f42082a4111b6c38656ec970ae8b2e1ce2cacd7d29f1510 in / 
# Sat, 05 Jul 2025 02:17:41 GMT
COPY file:b37d593713ee21ad52a4cd1424dc019a24f7966f85df0ac4b86d234302695328 in /etc/yum.repos.d/. 
# Sat, 05 Jul 2025 02:17:41 GMT
CMD ["/bin/bash"]
# Sat, 05 Jul 2025 02:17:41 GMT
COPY file:0667e9d31385a24c3aef13f2dd9ab6a7b71b3dfcfef5127d3c1e2ea2c838e5cb in /usr/share/buildinfo/content-sets.json 
# Sat, 05 Jul 2025 02:17:41 GMT
COPY file:0667e9d31385a24c3aef13f2dd9ab6a7b71b3dfcfef5127d3c1e2ea2c838e5cb in /root/buildinfo/content_manifests/content-sets.json 
# Sat, 05 Jul 2025 02:17:41 GMT
LABEL "build-date"="2025-08-20T13:11:42" "architecture"="ppc64le" "vcs-type"="git" "vcs-ref"="f4b088292653bbf5ca8188a5e59ffd06a8671d4b" "release"="1755695350"
# Sat, 05 Jul 2025 02:17:41 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 05 Jul 2025 02:17:41 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 05 Jul 2025 02:17:41 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Sat, 05 Jul 2025 02:17:41 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en     ;     microdnf clean all # buildkit
# Sat, 05 Jul 2025 02:17:41 GMT
ENV JAVA_VERSION=jdk-11.0.28+6
# Sat, 05 Jul 2025 02:17:41 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='32c316cb3998a9c9dee2829fbb577ea1c0ed666700cec73e049d44c342bb19af';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.28%2B6/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.28_6.tar.gz';          ;;        ppc64le)          ESUM='e272abd162b3de68093630929453feba3e63a5ab1bbb912379f6a4aa968ef06a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.28%2B6/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.28_6.tar.gz';          ;;        s390x)          ESUM='ac3f94fdcc5372e90f44fad9cd03ec0e3fd3535fea06c120f85e4a7534c6de04';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.28%2B6/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.28_6.tar.gz';          ;;        x86_64)          ESUM='7dfd551795a8884b26cbb02e0301da95db40160bb194f48271dc2ef9367f50c2';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.28%2B6/OpenJDK11U-jdk_x64_linux_hotspot_11.0.28_6.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Sat, 05 Jul 2025 02:17:41 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Sat, 05 Jul 2025 02:17:41 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Sat, 05 Jul 2025 02:17:41 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Sat, 05 Jul 2025 02:17:41 GMT
CMD ["jshell"]
# Sat, 05 Jul 2025 02:17:41 GMT
CMD ["gradle"]
# Sat, 05 Jul 2025 02:17:41 GMT
ENV GRADLE_HOME=/opt/gradle
# Sat, 05 Jul 2025 02:17:41 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 101 gradle     && useradd --system --gid gradle --uid 101 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Sat, 05 Jul 2025 02:17:41 GMT
VOLUME [/home/gradle/.gradle]
# Sat, 05 Jul 2025 02:17:41 GMT
WORKDIR /home/gradle
# Sat, 05 Jul 2025 02:17:41 GMT
RUN set -o errexit -o nounset     && microdnf install -y         make                 findutils                 unzip         which                 git         git-lfs         subversion     && microdnf clean all         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which svn # buildkit
# Sat, 05 Jul 2025 02:17:41 GMT
ENV GRADLE_VERSION=7.6.6
# Sat, 05 Jul 2025 02:17:41 GMT
ARG GRADLE_DOWNLOAD_SHA256=673d9776f303bc7048fc3329d232d6ebf1051b07893bd9d11616fad9a8673be0
# Sat, 05 Jul 2025 02:17:41 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=673d9776f303bc7048fc3329d232d6ebf1051b07893bd9d11616fad9a8673be0
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Sat, 05 Jul 2025 02:17:41 GMT
USER gradle
# Sat, 05 Jul 2025 02:17:41 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=673d9776f303bc7048fc3329d232d6ebf1051b07893bd9d11616fad9a8673be0
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Sat, 05 Jul 2025 02:17:41 GMT
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
	-	`sha256:642815719b1c3a83dade204b3f9b2e56294311354ce9169ff3735d8c547cf75f`  
		Last Modified: Thu, 21 Aug 2025 21:58:13 GMT  
		Size: 129.4 MB (129356802 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26086e8bdadce9e50085d45606e9ae2f37c7f42c15d6d9753ecb486578b10bb8`  
		Last Modified: Thu, 21 Aug 2025 19:01:46 GMT  
		Size: 130.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b28ae41a4b58e013a32e5fbdd5325f47da9bd694752b754ccdc688eef5a7feda`  
		Last Modified: Thu, 21 Aug 2025 19:01:45 GMT  
		Size: 2.3 KB (2291 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:852ac7f5fd1d129397124f2e31da421d8779169cc61dfef661f4b635564d610d`  
		Last Modified: Thu, 21 Aug 2025 19:32:18 GMT  
		Size: 1.7 KB (1708 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af2cd29f94d6c11e9bb9950f6a1bd5fa0dd608c49235011edfc930912389a400`  
		Last Modified: Thu, 21 Aug 2025 19:32:22 GMT  
		Size: 38.1 MB (38125393 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72bc72689cd87d28ec7cf4883324e28dd39c4f97bf8b6204067e6e14f8b18020`  
		Last Modified: Sun, 24 Aug 2025 15:04:41 GMT  
		Size: 128.5 MB (128469418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef67b6d66ac76f791c9dde480553b2d5b67908df86c0dc5c14fa6909d7d0c00f`  
		Last Modified: Thu, 21 Aug 2025 19:36:05 GMT  
		Size: 35.0 KB (35005 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:7-jdk11-ubi` - unknown; unknown

```console
$ docker pull gradle@sha256:648ce3c1ecca67c6018f2bf9856b4eceb21a9a9a380a67aa982d6f98e591868c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5338673 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:11951fccf27825318125afe0c3a3c85eecc299bca270795f2e47464db2d7a491`

```dockerfile
```

-	Layers:
	-	`sha256:198078dbbade953b20085879108d8788a9b7c6aa2ed952cba034b0cab6fc64cd`  
		Last Modified: Thu, 21 Aug 2025 20:18:50 GMT  
		Size: 5.3 MB (5314984 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9f40155441918d7c73bce418affc1ae803ec38566379b2d7ea4aee2ff8071801`  
		Last Modified: Thu, 21 Aug 2025 20:18:51 GMT  
		Size: 23.7 KB (23689 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:7-jdk11-ubi` - linux; s390x

```console
$ docker pull gradle@sha256:8fd71f071917139478ebca6772c0e94289079c3a6a40a6640402210b9cedb9db
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **352.3 MB (352304850 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e287849c858b93fec19c8fa975b0b61a1db487ffe57e8960136ea0a8b64e9d17`
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
ENV JAVA_VERSION=jdk-11.0.28+6
# Fri, 01 Aug 2025 11:04:34 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='32c316cb3998a9c9dee2829fbb577ea1c0ed666700cec73e049d44c342bb19af';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.28%2B6/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.28_6.tar.gz';          ;;        ppc64le)          ESUM='e272abd162b3de68093630929453feba3e63a5ab1bbb912379f6a4aa968ef06a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.28%2B6/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.28_6.tar.gz';          ;;        s390x)          ESUM='ac3f94fdcc5372e90f44fad9cd03ec0e3fd3535fea06c120f85e4a7534c6de04';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.28%2B6/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.28_6.tar.gz';          ;;        x86_64)          ESUM='7dfd551795a8884b26cbb02e0301da95db40160bb194f48271dc2ef9367f50c2';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.28%2B6/OpenJDK11U-jdk_x64_linux_hotspot_11.0.28_6.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Fri, 01 Aug 2025 11:04:34 GMT
CMD ["jshell"]
# Wed, 10 Sep 2025 15:58:43 GMT
CMD ["gradle"]
# Wed, 10 Sep 2025 15:58:43 GMT
ENV GRADLE_HOME=/opt/gradle
# Wed, 10 Sep 2025 15:58:43 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 101 gradle     && useradd --system --gid gradle --uid 101 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Wed, 10 Sep 2025 15:58:43 GMT
VOLUME [/home/gradle/.gradle]
# Wed, 10 Sep 2025 15:58:43 GMT
WORKDIR /home/gradle
# Wed, 10 Sep 2025 15:58:43 GMT
RUN set -o errexit -o nounset     && microdnf install -y         make                 findutils                 unzip         which                 git         git-lfs         subversion     && microdnf clean all         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which svn # buildkit
# Wed, 10 Sep 2025 15:58:43 GMT
ENV GRADLE_VERSION=7.6.6
# Wed, 10 Sep 2025 15:58:43 GMT
ARG GRADLE_DOWNLOAD_SHA256=673d9776f303bc7048fc3329d232d6ebf1051b07893bd9d11616fad9a8673be0
# Wed, 10 Sep 2025 15:58:43 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=673d9776f303bc7048fc3329d232d6ebf1051b07893bd9d11616fad9a8673be0
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Wed, 10 Sep 2025 15:58:43 GMT
USER gradle
# Wed, 10 Sep 2025 15:58:43 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=673d9776f303bc7048fc3329d232d6ebf1051b07893bd9d11616fad9a8673be0
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Wed, 10 Sep 2025 15:58:43 GMT
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
	-	`sha256:b87e47aab21499c0825133396568b61e08a377b1e716fcaf1c46be12377514c9`  
		Last Modified: Fri, 19 Sep 2025 21:49:35 GMT  
		Size: 122.0 MB (122030652 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c68c4019099cbb3da23993590677a6c00540fc853d2e21b623e624c93d2a5fc6`  
		Last Modified: Fri, 19 Sep 2025 21:49:22 GMT  
		Size: 130.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a9f41571093c3301ea8cb1134493cb8cdcd58b880e3c365d52a35afa0591537`  
		Last Modified: Fri, 19 Sep 2025 21:49:22 GMT  
		Size: 2.3 KB (2292 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2bf563cb682084bb46e59ff6206abc018c13b99524db3125deb75aaaead9aff`  
		Last Modified: Fri, 19 Sep 2025 22:21:52 GMT  
		Size: 1.7 KB (1708 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c224377868ee3948b89decbe8cc0cc0d2868418646fd8ab65528a5da30ce058`  
		Last Modified: Fri, 19 Sep 2025 22:21:53 GMT  
		Size: 36.4 MB (36417734 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1da6c5a586bf380d8d8ad2b7bce4fb0c5b1c83685914ddf0054b216ba9fbd9e3`  
		Last Modified: Fri, 19 Sep 2025 22:24:34 GMT  
		Size: 128.5 MB (128469468 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be34be62cf9e5f52e7a0655a0a5b1b5c0a1623c3201feb86fd9b3bc65167a8b0`  
		Last Modified: Fri, 19 Sep 2025 22:24:50 GMT  
		Size: 35.0 KB (35011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:7-jdk11-ubi` - unknown; unknown

```console
$ docker pull gradle@sha256:5556116128774006f8c3c6e880a20d9a0d7b8a338d882fed39ba7145656e9497
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5328520 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:91c1ea90e14c33aea408a553d5e17af696bc0d33aace59b90201f9c32a4375f2`

```dockerfile
```

-	Layers:
	-	`sha256:e2077cc9d6839a951d013c2d152274c2c89d09cbdba848ccc8f611a39965faa4`  
		Last Modified: Fri, 19 Sep 2025 23:19:08 GMT  
		Size: 5.3 MB (5304893 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ef19ec578e228a9d52c706738cf540f31effd36f52a2528473c8134f54373824`  
		Last Modified: Fri, 19 Sep 2025 23:19:09 GMT  
		Size: 23.6 KB (23627 bytes)  
		MIME: application/vnd.in-toto+json
