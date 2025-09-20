## `gradle:8-jdk8-ubi`

```console
$ docker pull gradle@sha256:1b4a6081febf51f65613bf5004e0e50772b62811b0c10143dc17fbab3c883427
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
$ docker pull gradle@sha256:468f74dd50dce5a64de126bd772125ae5bf1aed376faa39f795a71b2ab690b48
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **296.2 MB (296162137 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a8f2cbc29b0edddd261a85af2295d4b77afc92b3844d1f27e88bb530d452259e`
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
ENV JAVA_VERSION=jdk8u462-b08
# Fri, 01 Aug 2025 11:04:34 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='19552c1cf7f5c18290a6bdcd6757f70ea5c331a2bc0dd7a3b3120e8dbc4b4891';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u462-b08/OpenJDK8U-jdk_aarch64_linux_hotspot_8u462b08.tar.gz';          ;;        ppc64le)          ESUM='3e4dbc94ebd299b60d8168b1d33cdae1f619db9403aaefd65d0b643615d596cc';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u462-b08/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u462b08.tar.gz';          ;;        x86_64)          ESUM='5d64ae542b59a962b3caadadd346f4b1c3010879a28bb02d928326993de16e79';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u462-b08/OpenJDK8U-jdk_x64_linux_hotspot_8u462b08.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip; # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
RUN set -eux;     echo "Verifying install ...";     echo "javac -version"; javac -version;     echo "java -version"; java -version;     echo "Complete." # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Fri, 12 Sep 2025 13:29:01 GMT
CMD ["gradle"]
# Fri, 12 Sep 2025 13:29:01 GMT
ENV GRADLE_HOME=/opt/gradle
# Fri, 12 Sep 2025 13:29:01 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 101 gradle     && useradd --system --gid gradle --uid 101 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Fri, 12 Sep 2025 13:29:01 GMT
VOLUME [/home/gradle/.gradle]
# Fri, 12 Sep 2025 13:29:01 GMT
WORKDIR /home/gradle
# Fri, 12 Sep 2025 13:29:01 GMT
RUN set -o errexit -o nounset     && microdnf install -y         make                 findutils                 unzip         which                 git         git-lfs         subversion     && microdnf clean all         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which svn # buildkit
# Fri, 12 Sep 2025 13:29:01 GMT
ENV GRADLE_VERSION=8.14.3
# Fri, 12 Sep 2025 13:29:01 GMT
ARG GRADLE_DOWNLOAD_SHA256=bd71102213493060956ec229d946beee57158dbd89d0e62b91bca0fa2c5f3531
# Fri, 12 Sep 2025 13:29:01 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=bd71102213493060956ec229d946beee57158dbd89d0e62b91bca0fa2c5f3531
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Fri, 12 Sep 2025 13:29:01 GMT
USER gradle
# Fri, 12 Sep 2025 13:29:01 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=bd71102213493060956ec229d946beee57158dbd89d0e62b91bca0fa2c5f3531
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Fri, 12 Sep 2025 13:29:01 GMT
USER root
```

-	Layers:
	-	`sha256:9f4bff248214d12c7254dc3c25ef82bd14ff143e2a06d159f2a8cc1c9e6ef1fd`  
		Last Modified: Thu, 18 Sep 2025 15:30:42 GMT  
		Size: 39.6 MB (39648249 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2040a91dbba30259f1076e8c96ca81ce2cc53db997390a384a16be3a187fa14f`  
		Last Modified: Fri, 19 Sep 2025 21:13:18 GMT  
		Size: 27.5 MB (27534893 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a992d5343fb2da7bef495562913accfa8be00754c522cbb3afaa04c99748a9b0`  
		Last Modified: Fri, 19 Sep 2025 21:13:22 GMT  
		Size: 54.7 MB (54731868 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48ac474d105d03c12b533a317900b8edb396d549909d6d0fb2dee5398c604459`  
		Last Modified: Fri, 19 Sep 2025 21:13:16 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b871afef90ac1069e327c4d1ee42e4c91434e8a0eb87c1596b79c3be1e84e88`  
		Last Modified: Fri, 19 Sep 2025 21:13:16 GMT  
		Size: 2.3 KB (2315 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb9f19e617bdfc1cc7b0433ee7ae18487e8ca2daead9d55317352b9eef1ed6e8`  
		Last Modified: Fri, 19 Sep 2025 21:59:23 GMT  
		Size: 1.7 KB (1710 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16a0709e13893a32e753fcd4ad261ec7edbd52be3c5bcf07921a4fa27317be76`  
		Last Modified: Sat, 20 Sep 2025 00:07:26 GMT  
		Size: 36.8 MB (36792913 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab4de79a703c2e6d865279a19febe9e0651269470c2876696eb2493fd44c8449`  
		Last Modified: Sat, 20 Sep 2025 00:07:29 GMT  
		Size: 137.4 MB (137395131 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82c9d6a0873b58c613604243fafcdb3b4d6d6ebef3b22689d3ee185f599819c2`  
		Last Modified: Fri, 19 Sep 2025 21:59:22 GMT  
		Size: 54.9 KB (54898 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:8-jdk8-ubi` - unknown; unknown

```console
$ docker pull gradle@sha256:02cf86bf7a2a60105a03c405c2f2df168601369ffea0c285890cb5998801f6b3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5534602 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aaa45745ee1b63f1f84d0ea1dea5ba24f8ad525d3b42680648a4c4c57ac8d8b0`

```dockerfile
```

-	Layers:
	-	`sha256:11c9ad6153f770abdf04526553f862560d5ea8d704ef32d7ce3a9098fdfeec74`  
		Last Modified: Fri, 19 Sep 2025 23:22:17 GMT  
		Size: 5.5 MB (5510369 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b04de22d70a99221c1aa46280b2efcb3e0fa3e1488e4ae00d9126e05a83839b4`  
		Last Modified: Fri, 19 Sep 2025 23:22:18 GMT  
		Size: 24.2 KB (24233 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:8-jdk8-ubi` - linux; arm64 variant v8

```console
$ docker pull gradle@sha256:57b9e3b12a32d28b2385746bbf342dad3eff32baf44331afc66dbbeb8019fbcc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **293.4 MB (293410109 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c5aabfed1ce263f8834b23e3e02f25a12765b3404d7b66eb8a1fbc046537be66`
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
ENV JAVA_VERSION=jdk8u462-b08
# Fri, 01 Aug 2025 11:04:34 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='19552c1cf7f5c18290a6bdcd6757f70ea5c331a2bc0dd7a3b3120e8dbc4b4891';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u462-b08/OpenJDK8U-jdk_aarch64_linux_hotspot_8u462b08.tar.gz';          ;;        ppc64le)          ESUM='3e4dbc94ebd299b60d8168b1d33cdae1f619db9403aaefd65d0b643615d596cc';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u462-b08/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u462b08.tar.gz';          ;;        x86_64)          ESUM='5d64ae542b59a962b3caadadd346f4b1c3010879a28bb02d928326993de16e79';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u462-b08/OpenJDK8U-jdk_x64_linux_hotspot_8u462b08.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip; # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
RUN set -eux;     echo "Verifying install ...";     echo "javac -version"; javac -version;     echo "java -version"; java -version;     echo "Complete." # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Fri, 12 Sep 2025 13:29:01 GMT
CMD ["gradle"]
# Fri, 12 Sep 2025 13:29:01 GMT
ENV GRADLE_HOME=/opt/gradle
# Fri, 12 Sep 2025 13:29:01 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 101 gradle     && useradd --system --gid gradle --uid 101 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Fri, 12 Sep 2025 13:29:01 GMT
VOLUME [/home/gradle/.gradle]
# Fri, 12 Sep 2025 13:29:01 GMT
WORKDIR /home/gradle
# Fri, 12 Sep 2025 13:29:01 GMT
RUN set -o errexit -o nounset     && microdnf install -y         make                 findutils                 unzip         which                 git         git-lfs         subversion     && microdnf clean all         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which svn # buildkit
# Fri, 12 Sep 2025 13:29:01 GMT
ENV GRADLE_VERSION=8.14.3
# Fri, 12 Sep 2025 13:29:01 GMT
ARG GRADLE_DOWNLOAD_SHA256=bd71102213493060956ec229d946beee57158dbd89d0e62b91bca0fa2c5f3531
# Fri, 12 Sep 2025 13:29:01 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=bd71102213493060956ec229d946beee57158dbd89d0e62b91bca0fa2c5f3531
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Fri, 12 Sep 2025 13:29:01 GMT
USER gradle
# Fri, 12 Sep 2025 13:29:01 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=bd71102213493060956ec229d946beee57158dbd89d0e62b91bca0fa2c5f3531
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Fri, 12 Sep 2025 13:29:01 GMT
USER root
```

-	Layers:
	-	`sha256:a9f9218e937ae927e68fe68d00604365ddda1b238616443bc0a4b9e574067342`  
		Last Modified: Thu, 18 Sep 2025 15:44:52 GMT  
		Size: 37.9 MB (37900151 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c3d31d032499afaecb2cf97e61502f4430a491f53a1ad8d9fc2002347f64593`  
		Last Modified: Fri, 19 Sep 2025 20:44:09 GMT  
		Size: 28.0 MB (27977256 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70639a338eafc99dbad75194222495c6502ddbd8646f16cf4f320b4479977880`  
		Last Modified: Fri, 19 Sep 2025 20:44:14 GMT  
		Size: 53.8 MB (53836128 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bb43ac85d02375af6a139bb5683dc9c73e7a2a4f45e466120b0604dba4d3a46`  
		Last Modified: Fri, 19 Sep 2025 20:44:06 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3eb5602f7995b7dc56045f6dc012fb251c353f6dbb1730cf079d614c1b916eae`  
		Last Modified: Fri, 19 Sep 2025 20:44:06 GMT  
		Size: 2.3 KB (2314 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39e37ffffcec14c272fe4190750fa6648ea6009b06881f10dc46fa220eeca890`  
		Last Modified: Fri, 19 Sep 2025 21:14:03 GMT  
		Size: 1.7 KB (1705 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58b02797e0fc01ff1b0f6ff72413dbd1ef84edf796df05ef930389de5b9be13a`  
		Last Modified: Fri, 19 Sep 2025 21:14:12 GMT  
		Size: 36.2 MB (36237667 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbb6ee19c96c718c3ca6f92f0e749893e4b933be8ab57a49f65fe0a126f99409`  
		Last Modified: Fri, 19 Sep 2025 21:13:42 GMT  
		Size: 137.4 MB (137395205 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d76f515a7f079310125764c231370efda951faa0ae4e92c5860b92e73be3b347`  
		Last Modified: Fri, 19 Sep 2025 21:14:08 GMT  
		Size: 59.5 KB (59523 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:8-jdk8-ubi` - unknown; unknown

```console
$ docker pull gradle@sha256:1876c553e18c5d2fe3a0d002d0e3a92c6b354314dcb73c9b478d972d1b803e0f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5534929 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ab32e26d4cd56de5e8e4f33223a1396818463b126c7e5c47ab779e24207e0bb`

```dockerfile
```

-	Layers:
	-	`sha256:9e24ebfb588316111c228cfe388c408ecdf1ca9d3399525d4ad294a2c72abe67`  
		Last Modified: Fri, 19 Sep 2025 23:22:23 GMT  
		Size: 5.5 MB (5510499 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:51585470ce56372fdfe73195d1edbcbef134e0ba466c7e0138f3763fa31537e0`  
		Last Modified: Fri, 19 Sep 2025 23:22:24 GMT  
		Size: 24.4 KB (24430 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:8-jdk8-ubi` - linux; ppc64le

```console
$ docker pull gradle@sha256:df1cb7770af52ea6b1b6d8c9f1871b3d559ad6e04123eba34a4646ed5a4363b3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **301.8 MB (301760651 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:396d19ec2e76f82a47af1cf77c31fc6140be94344373bb2668ab4bf3b361d846`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["gradle"]`

```dockerfile
# Thu, 17 Jul 2025 03:50:10 GMT
LABEL maintainer="Red Hat, Inc."
# Thu, 17 Jul 2025 03:50:10 GMT
LABEL vendor="Red Hat, Inc."
# Thu, 17 Jul 2025 03:50:10 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Thu, 17 Jul 2025 03:50:10 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.6"       distribution-scope="public"
# Thu, 17 Jul 2025 03:50:10 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Thu, 17 Jul 2025 03:50:10 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Thu, 17 Jul 2025 03:50:10 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 17 Jul 2025 03:50:10 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 17 Jul 2025 03:50:10 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Thu, 17 Jul 2025 03:50:10 GMT
LABEL io.openshift.expose-services=""
# Thu, 17 Jul 2025 03:50:10 GMT
LABEL io.openshift.tags="minimal rhel9"
# Thu, 17 Jul 2025 03:50:10 GMT
ENV container oci
# Thu, 17 Jul 2025 03:50:10 GMT
COPY dir:d2207f84596636cf1f42082a4111b6c38656ec970ae8b2e1ce2cacd7d29f1510 in / 
# Thu, 17 Jul 2025 03:50:10 GMT
COPY file:b37d593713ee21ad52a4cd1424dc019a24f7966f85df0ac4b86d234302695328 in /etc/yum.repos.d/. 
# Thu, 17 Jul 2025 03:50:10 GMT
CMD ["/bin/bash"]
# Thu, 17 Jul 2025 03:50:10 GMT
COPY file:0667e9d31385a24c3aef13f2dd9ab6a7b71b3dfcfef5127d3c1e2ea2c838e5cb in /usr/share/buildinfo/content-sets.json 
# Thu, 17 Jul 2025 03:50:10 GMT
COPY file:0667e9d31385a24c3aef13f2dd9ab6a7b71b3dfcfef5127d3c1e2ea2c838e5cb in /root/buildinfo/content_manifests/content-sets.json 
# Thu, 17 Jul 2025 03:50:10 GMT
LABEL "build-date"="2025-08-20T13:11:42" "architecture"="ppc64le" "vcs-type"="git" "vcs-ref"="f4b088292653bbf5ca8188a5e59ffd06a8671d4b" "release"="1755695350"
# Thu, 17 Jul 2025 03:50:10 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 17 Jul 2025 03:50:10 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 17 Jul 2025 03:50:10 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 17 Jul 2025 03:50:10 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en     ;     microdnf clean all # buildkit
# Thu, 17 Jul 2025 03:50:10 GMT
ENV JAVA_VERSION=jdk8u462-b08
# Thu, 17 Jul 2025 03:50:10 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='19552c1cf7f5c18290a6bdcd6757f70ea5c331a2bc0dd7a3b3120e8dbc4b4891';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u462-b08/OpenJDK8U-jdk_aarch64_linux_hotspot_8u462b08.tar.gz';          ;;        ppc64le)          ESUM='3e4dbc94ebd299b60d8168b1d33cdae1f619db9403aaefd65d0b643615d596cc';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u462-b08/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u462b08.tar.gz';          ;;        x86_64)          ESUM='5d64ae542b59a962b3caadadd346f4b1c3010879a28bb02d928326993de16e79';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u462-b08/OpenJDK8U-jdk_x64_linux_hotspot_8u462b08.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip; # buildkit
# Thu, 17 Jul 2025 03:50:10 GMT
RUN set -eux;     echo "Verifying install ...";     echo "javac -version"; javac -version;     echo "java -version"; java -version;     echo "Complete." # buildkit
# Thu, 17 Jul 2025 03:50:10 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 17 Jul 2025 03:50:10 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 17 Jul 2025 03:50:10 GMT
CMD ["gradle"]
# Thu, 17 Jul 2025 03:50:10 GMT
ENV GRADLE_HOME=/opt/gradle
# Thu, 17 Jul 2025 03:50:10 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 101 gradle     && useradd --system --gid gradle --uid 101 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Thu, 17 Jul 2025 03:50:10 GMT
VOLUME [/home/gradle/.gradle]
# Thu, 17 Jul 2025 03:50:10 GMT
WORKDIR /home/gradle
# Thu, 17 Jul 2025 03:50:10 GMT
RUN set -o errexit -o nounset     && microdnf install -y         make                 findutils                 unzip         which                 git         git-lfs         subversion     && microdnf clean all         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which svn # buildkit
# Thu, 17 Jul 2025 03:50:10 GMT
ENV GRADLE_VERSION=8.14.3
# Thu, 17 Jul 2025 03:50:10 GMT
ARG GRADLE_DOWNLOAD_SHA256=bd71102213493060956ec229d946beee57158dbd89d0e62b91bca0fa2c5f3531
# Thu, 17 Jul 2025 03:50:10 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=bd71102213493060956ec229d946beee57158dbd89d0e62b91bca0fa2c5f3531
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Thu, 17 Jul 2025 03:50:10 GMT
USER gradle
# Thu, 17 Jul 2025 03:50:10 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=bd71102213493060956ec229d946beee57158dbd89d0e62b91bca0fa2c5f3531
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Thu, 17 Jul 2025 03:50:10 GMT
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
	-	`sha256:45b39f1b0a464ef4fe4cb0c1a7b93feabcbade1e0e63b08f41ae89015678c17f`  
		Last Modified: Thu, 21 Aug 2025 18:58:24 GMT  
		Size: 52.2 MB (52165988 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8fc10cbfe25c3663243f96372cd81532973338e92366aa153e9b40351b02f00`  
		Last Modified: Thu, 21 Aug 2025 18:58:16 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2f5a3db82c809f18b027511fd040e839c102b12b5103032d1c3c1344d033710`  
		Last Modified: Thu, 21 Aug 2025 18:58:23 GMT  
		Size: 2.3 KB (2316 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5447969ac700a84fb53d8b7504400744528e0bb23355e13a261f266ce4771fc8`  
		Last Modified: Thu, 21 Aug 2025 19:33:59 GMT  
		Size: 1.7 KB (1708 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fce78aaf6cfc04da37a4110bfd74c30de2cf137f22e65525cfd26255afdc8232`  
		Last Modified: Thu, 21 Aug 2025 19:34:04 GMT  
		Size: 38.1 MB (38125419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ece8fe48121fb88aca02a7c4c85e21b88627c6afbd8059e9de1f3989d6fd448c`  
		Last Modified: Sun, 24 Aug 2025 14:34:42 GMT  
		Size: 137.4 MB (137395195 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e09ff10e4fad25685cc65dbe6e19ab7329f89a08bdbf027516676c5484a20124`  
		Last Modified: Thu, 21 Aug 2025 19:34:02 GMT  
		Size: 35.0 KB (35007 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:8-jdk8-ubi` - unknown; unknown

```console
$ docker pull gradle@sha256:fda5392ea742f70821a92a3a1d93f634553e0ee016aec301a1211b0cd377c4cf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5532598 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3800b29686459b82c7c99602dd6e4059da84ac9a5539dee6d010d7d4468da61e`

```dockerfile
```

-	Layers:
	-	`sha256:d388306af60834062d134bd30b7635a55614d0c752a47fd9609e62a2651e9556`  
		Last Modified: Thu, 21 Aug 2025 20:22:19 GMT  
		Size: 5.5 MB (5508291 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f71de5a4feb2fc9911185b8f30a4f29f8256d2ee7aab288bb39acf186886858e`  
		Last Modified: Thu, 21 Aug 2025 20:22:19 GMT  
		Size: 24.3 KB (24307 bytes)  
		MIME: application/vnd.in-toto+json
