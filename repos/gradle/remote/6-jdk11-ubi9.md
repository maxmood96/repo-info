## `gradle:6-jdk11-ubi9`

```console
$ docker pull gradle@sha256:bb812376b81106cff58ea97d8f88c25f52b9a61d05e2ef4ad86f9a473be8a9f5
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

### `gradle:6-jdk11-ubi9` - linux; amd64

```console
$ docker pull gradle@sha256:5ecb1cb418c42825ff2660fe77e414abad51f88ca8f18b12ca0294bfa06b250f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **357.5 MB (357538146 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:139508abaef98fe167c6c5d827aa38b99b0361f165f98b4c75acb9073c2efde2`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["gradle"]`

```dockerfile
# Wed, 06 May 2026 12:56:14 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 06 May 2026 12:56:14 GMT
LABEL vendor="Red Hat, Inc."
# Wed, 06 May 2026 12:56:14 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Wed, 06 May 2026 12:56:14 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.7"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Wed, 06 May 2026 12:56:14 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 06 May 2026 12:56:14 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Wed, 06 May 2026 12:56:14 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 06 May 2026 12:56:14 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 06 May 2026 12:56:14 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Wed, 06 May 2026 12:56:14 GMT
LABEL io.openshift.expose-services=""
# Wed, 06 May 2026 12:56:14 GMT
LABEL io.openshift.tags="minimal rhel9"
# Wed, 06 May 2026 12:56:14 GMT
ENV container oci
# Wed, 06 May 2026 12:56:14 GMT
COPY dir:4c4996e917f33023b976824d7cb68c72b897d6d36b90e718143d5c6b6644b5f2 in /      
# Wed, 06 May 2026 12:56:15 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Wed, 06 May 2026 12:56:15 GMT
CMD ["/bin/bash"]
# Wed, 06 May 2026 12:56:15 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /usr/share/buildinfo/content-sets.json      
# Wed, 06 May 2026 12:56:15 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /root/buildinfo/content_manifests/content-sets.json      
# Wed, 06 May 2026 12:56:15 GMT
COPY file:9d5fe0edb9a65123afda28f8a8cf6e139537dee71d7b2bc90f9c46d89a207386 in /usr/share/buildinfo/labels.json      
# Wed, 06 May 2026 12:56:15 GMT
COPY file:9d5fe0edb9a65123afda28f8a8cf6e139537dee71d7b2bc90f9c46d89a207386 in /root/buildinfo/labels.json      
# Wed, 06 May 2026 12:56:15 GMT
LABEL "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="8def05a6f0dfabdc25ea20a79b0d11f8f9b12c5c" "org.opencontainers.image.revision"="8def05a6f0dfabdc25ea20a79b0d11f8f9b12c5c" "build-date"="2026-05-06T12:56:03Z" "org.opencontainers.image.created"="2026-05-06T12:56:03Z" "release"="1778072020"org.opencontainers.image.revision=8def05a6f0dfabdc25ea20a79b0d11f8f9b12c5c,org.opencontainers.image.created=2026-05-06T12:56:03Z
# Fri, 08 May 2026 16:20:41 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 08 May 2026 16:20:41 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 08 May 2026 16:20:41 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 08 May 2026 16:20:41 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en     ;     microdnf clean all # buildkit
# Fri, 08 May 2026 16:20:41 GMT
ENV JAVA_VERSION=jdk-11.0.31+11
# Fri, 08 May 2026 16:20:48 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='257f4d39e060658fc2eb89a803ca43b3f337e64e253f2d94ebae1d85c9ef5f69';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.31%2B11/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.31_11.tar.gz';          ;;        ppc64le)          ESUM='e473d10c3c44f67301fd90abd9e4b7ae312eae8a2399b333fcf4179daf35a743';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.31%2B11/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.31_11.tar.gz';          ;;        s390x)          ESUM='4d3709cdc03de1a00f14f530c2ebad1883d9bcc8a556fc419f083bec87b4687a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.31%2B11/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.31_11.tar.gz';          ;;        x86_64)          ESUM='1e9de64586b519c0a981319489257cabedd9457599f3823424a87c3158fbe939';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.31%2B11/OpenJDK11U-jdk_x64_linux_hotspot_11.0.31_11.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Fri, 08 May 2026 16:20:49 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Fri, 08 May 2026 16:20:49 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Fri, 08 May 2026 16:20:49 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Fri, 08 May 2026 16:20:49 GMT
CMD ["jshell"]
# Fri, 08 May 2026 16:39:56 GMT
CMD ["gradle"]
# Fri, 08 May 2026 16:39:56 GMT
ENV GRADLE_HOME=/opt/gradle
# Fri, 08 May 2026 16:39:56 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 101 gradle     && useradd --system --gid gradle --uid 101 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Fri, 08 May 2026 16:39:56 GMT
VOLUME [/home/gradle/.gradle]
# Fri, 08 May 2026 16:39:56 GMT
WORKDIR /home/gradle
# Fri, 08 May 2026 16:39:59 GMT
RUN set -o errexit -o nounset     && microdnf install -y         make                 findutils                 unzip         which                 git         git-lfs         subversion     && microdnf clean all         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which svn # buildkit
# Fri, 08 May 2026 16:39:59 GMT
ENV GRADLE_VERSION=6.9.4
# Fri, 08 May 2026 16:39:59 GMT
ARG GRADLE_DOWNLOAD_SHA256=3e240228538de9f18772a574e99a0ba959e83d6ef351014381acd9631781389a
# Fri, 08 May 2026 16:40:02 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=3e240228538de9f18772a574e99a0ba959e83d6ef351014381acd9631781389a
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Fri, 08 May 2026 16:40:02 GMT
USER gradle
# Fri, 08 May 2026 16:40:02 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=3e240228538de9f18772a574e99a0ba959e83d6ef351014381acd9631781389a
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Fri, 08 May 2026 16:40:02 GMT
USER root
```

-	Layers:
	-	`sha256:df0edd575569e5cb7e2e34f252e4cf36c13679e9633d7c97be861b8b247c70bc`  
		Last Modified: Wed, 06 May 2026 13:26:44 GMT  
		Size: 40.0 MB (39994775 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87bd5a4bae36c07630052838817a99e621eb1bd38e0922a8e4bf45a1f218f24d`  
		Last Modified: Fri, 08 May 2026 16:21:07 GMT  
		Size: 30.4 MB (30368763 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca7aecab191d3701d2bfa0cf45df369669d79fbe43dae4c71de3abbfa4046d9f`  
		Last Modified: Fri, 08 May 2026 16:21:09 GMT  
		Size: 142.3 MB (142348853 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:433dceb2c15311053fa98598bcc7d27863de625d6f6568d1f26e2579554b9373`  
		Last Modified: Fri, 08 May 2026 16:21:05 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:885cf69ffa9c18f21428e738a075b405829547390237f88736679e1a5bd695a6`  
		Last Modified: Fri, 08 May 2026 16:21:05 GMT  
		Size: 2.3 KB (2291 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:719e7e94789cd7bdc11b211c69eda3cbd74d5a9e437672c2f94263d959718d74`  
		Last Modified: Fri, 08 May 2026 16:40:17 GMT  
		Size: 1.7 KB (1707 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e63fa417eabcdf9121a5b93bfc71d8c89ee24fc096b88ad67603c42585d56b7`  
		Last Modified: Fri, 08 May 2026 16:40:20 GMT  
		Size: 36.7 MB (36693654 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f96be1e2c9e379f96bd90bba7c220f7713acee83b9ec50a12ccd12aaf3f61be`  
		Last Modified: Fri, 08 May 2026 16:40:21 GMT  
		Size: 107.7 MB (107696669 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af912da37db66c05b13041bc8d497b9946ba9b381d1e8e480a7300ae227ce472`  
		Last Modified: Fri, 08 May 2026 16:40:18 GMT  
		Size: 431.3 KB (431274 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:6-jdk11-ubi9` - unknown; unknown

```console
$ docker pull gradle@sha256:846c53f8fed21167e5fbda0ce1813de3f97e32dbc4d0cab336836311b7ef25cf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5339780 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1446f4ce870df963cb3ae9b5ced52ce18a4357b54f041c81a72d9dfa5b75ba39`

```dockerfile
```

-	Layers:
	-	`sha256:a15a1f077d7f95852233ceba66f804c3a8bbcbbdd12701f6c0b64012b94ef238`  
		Last Modified: Fri, 08 May 2026 16:40:18 GMT  
		Size: 5.3 MB (5316196 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f8c246a92ef4e9dd0c22e3e4d471e530f479b4dd3dc10a104b8cdcf2429b8a6d`  
		Last Modified: Fri, 08 May 2026 16:40:17 GMT  
		Size: 23.6 KB (23584 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:6-jdk11-ubi9` - linux; arm64 variant v8

```console
$ docker pull gradle@sha256:4167489627c720d7366dc33df146e6f4a56755993dad9afc1ffd27e132a4ac4e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **352.2 MB (352187663 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9efdd1c618513db402aa2439e54ed69e2cba512c21dc91f80915c75eb27840ed`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["gradle"]`

```dockerfile
# Wed, 06 May 2026 12:57:02 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 06 May 2026 12:57:02 GMT
LABEL vendor="Red Hat, Inc."
# Wed, 06 May 2026 12:57:02 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Wed, 06 May 2026 12:57:02 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.7"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Wed, 06 May 2026 12:57:02 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 06 May 2026 12:57:02 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Wed, 06 May 2026 12:57:02 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 06 May 2026 12:57:02 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 06 May 2026 12:57:02 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Wed, 06 May 2026 12:57:02 GMT
LABEL io.openshift.expose-services=""
# Wed, 06 May 2026 12:57:02 GMT
LABEL io.openshift.tags="minimal rhel9"
# Wed, 06 May 2026 12:57:02 GMT
ENV container oci
# Wed, 06 May 2026 12:57:03 GMT
COPY dir:658522d0a080af3309d9cd140f39d4866e8d82f0dbb45a592dba1356f2d8aac5 in /      
# Wed, 06 May 2026 12:57:03 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Wed, 06 May 2026 12:57:03 GMT
CMD ["/bin/bash"]
# Wed, 06 May 2026 12:57:04 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /usr/share/buildinfo/content-sets.json      
# Wed, 06 May 2026 12:57:04 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /root/buildinfo/content_manifests/content-sets.json      
# Wed, 06 May 2026 12:57:04 GMT
COPY file:d64d419d706e46f4d286cf24b8afd9f437d1a94efd91154dd762c8135440b692 in /usr/share/buildinfo/labels.json      
# Wed, 06 May 2026 12:57:04 GMT
COPY file:d64d419d706e46f4d286cf24b8afd9f437d1a94efd91154dd762c8135440b692 in /root/buildinfo/labels.json      
# Wed, 06 May 2026 12:57:04 GMT
LABEL "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="8def05a6f0dfabdc25ea20a79b0d11f8f9b12c5c" "org.opencontainers.image.revision"="8def05a6f0dfabdc25ea20a79b0d11f8f9b12c5c" "build-date"="2026-05-06T12:56:50Z" "org.opencontainers.image.created"="2026-05-06T12:56:50Z" "release"="1778072020"org.opencontainers.image.revision=8def05a6f0dfabdc25ea20a79b0d11f8f9b12c5c,org.opencontainers.image.created=2026-05-06T12:56:50Z
# Fri, 08 May 2026 16:20:38 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 08 May 2026 16:20:38 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 08 May 2026 16:20:38 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 08 May 2026 16:20:38 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en     ;     microdnf clean all # buildkit
# Fri, 08 May 2026 16:20:38 GMT
ENV JAVA_VERSION=jdk-11.0.31+11
# Fri, 08 May 2026 16:20:45 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='257f4d39e060658fc2eb89a803ca43b3f337e64e253f2d94ebae1d85c9ef5f69';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.31%2B11/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.31_11.tar.gz';          ;;        ppc64le)          ESUM='e473d10c3c44f67301fd90abd9e4b7ae312eae8a2399b333fcf4179daf35a743';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.31%2B11/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.31_11.tar.gz';          ;;        s390x)          ESUM='4d3709cdc03de1a00f14f530c2ebad1883d9bcc8a556fc419f083bec87b4687a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.31%2B11/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.31_11.tar.gz';          ;;        x86_64)          ESUM='1e9de64586b519c0a981319489257cabedd9457599f3823424a87c3158fbe939';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.31%2B11/OpenJDK11U-jdk_x64_linux_hotspot_11.0.31_11.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Fri, 08 May 2026 16:20:46 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Fri, 08 May 2026 16:20:46 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Fri, 08 May 2026 16:20:46 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Fri, 08 May 2026 16:20:46 GMT
CMD ["jshell"]
# Fri, 08 May 2026 16:36:39 GMT
CMD ["gradle"]
# Fri, 08 May 2026 16:36:39 GMT
ENV GRADLE_HOME=/opt/gradle
# Fri, 08 May 2026 16:36:39 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 101 gradle     && useradd --system --gid gradle --uid 101 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Fri, 08 May 2026 16:36:39 GMT
VOLUME [/home/gradle/.gradle]
# Fri, 08 May 2026 16:36:39 GMT
WORKDIR /home/gradle
# Fri, 08 May 2026 16:36:43 GMT
RUN set -o errexit -o nounset     && microdnf install -y         make                 findutils                 unzip         which                 git         git-lfs         subversion     && microdnf clean all         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which svn # buildkit
# Fri, 08 May 2026 16:36:43 GMT
ENV GRADLE_VERSION=6.9.4
# Fri, 08 May 2026 16:36:43 GMT
ARG GRADLE_DOWNLOAD_SHA256=3e240228538de9f18772a574e99a0ba959e83d6ef351014381acd9631781389a
# Fri, 08 May 2026 16:36:45 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=3e240228538de9f18772a574e99a0ba959e83d6ef351014381acd9631781389a
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Fri, 08 May 2026 16:36:45 GMT
USER gradle
# Fri, 08 May 2026 16:36:46 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=3e240228538de9f18772a574e99a0ba959e83d6ef351014381acd9631781389a
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Fri, 08 May 2026 16:36:46 GMT
USER root
```

-	Layers:
	-	`sha256:4432ba7926545d58c5c1a534c052b34ad23c14c54c95de1caf5071ea5ef8f194`  
		Last Modified: Wed, 06 May 2026 13:31:32 GMT  
		Size: 38.2 MB (38205674 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e7dc6b9b52a51cfd05161ebda0b33e8a7a98c5614fb854e031c1e247dec9b9b`  
		Last Modified: Fri, 08 May 2026 16:21:03 GMT  
		Size: 30.8 MB (30789352 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:194844800a0f6df4c9d190f043cc552086c2394e761fc6695a15a5ab9f9914a4`  
		Last Modified: Fri, 08 May 2026 16:21:06 GMT  
		Size: 139.0 MB (139040651 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee4187e99509f3d854443d45b68dfc97dfb9853c99f1064824153bf20227963f`  
		Last Modified: Fri, 08 May 2026 16:21:02 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:deccb1ea8cc65f04c37e2aee38afe6374f46992cdb5d3c4bffea73c36877726c`  
		Last Modified: Fri, 08 May 2026 16:21:02 GMT  
		Size: 2.3 KB (2291 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a921fc010f40456e220256e60bf35e4c079171844a30f72dcc7e6ea62465d25`  
		Last Modified: Fri, 08 May 2026 16:37:00 GMT  
		Size: 1.7 KB (1707 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:383e9cde12c29a9b40dbed6d674eff416de1b7a10779940f516db22d524416c4`  
		Last Modified: Fri, 08 May 2026 16:37:02 GMT  
		Size: 36.0 MB (36026136 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7752339a6dd453992be915ad0aee7c4293235cc0688dee4e30bfaf61a1b0a6b`  
		Last Modified: Fri, 08 May 2026 16:37:04 GMT  
		Size: 107.7 MB (107696668 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:993b70b309736264a6c0db37c58ecad42b591f0b3e0d5989851428ff9fb5254d`  
		Last Modified: Fri, 08 May 2026 16:37:01 GMT  
		Size: 425.0 KB (425023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:6-jdk11-ubi9` - unknown; unknown

```console
$ docker pull gradle@sha256:9e3de88863111d735a93984c6c5a00dea5e4bf8bbcd389d09729c8c7ca31a656
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5339976 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9108e1d35ee6368961283f0fd675c16589c6b858ce203e3d8a00e3b047383749`

```dockerfile
```

-	Layers:
	-	`sha256:67e810c865300e47eb59efd2e61bc972a73c3fb10a524882f6198f73c293bcb5`  
		Last Modified: Fri, 08 May 2026 16:37:01 GMT  
		Size: 5.3 MB (5316220 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c79e71932fdcd7a414843ee111e5fcad48a1e108fa10adc9c5bb8b245d14cd24`  
		Last Modified: Fri, 08 May 2026 16:37:00 GMT  
		Size: 23.8 KB (23756 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:6-jdk11-ubi9` - linux; ppc64le

```console
$ docker pull gradle@sha256:7c2df9de643e709f569b3b66fce09e5d45fe25e51c430c701a51b264f5b6aa5e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **352.6 MB (352573022 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e074f465c43e062e5737d8c2fc5e8afc1900ca96eda89069d973ed4f46786db`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["gradle"]`

```dockerfile
# Wed, 06 May 2026 12:56:35 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 06 May 2026 12:56:35 GMT
LABEL vendor="Red Hat, Inc."
# Wed, 06 May 2026 12:56:35 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Wed, 06 May 2026 12:56:35 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.7"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Wed, 06 May 2026 12:56:35 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 06 May 2026 12:56:35 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Wed, 06 May 2026 12:56:35 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 06 May 2026 12:56:35 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 06 May 2026 12:56:35 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Wed, 06 May 2026 12:56:35 GMT
LABEL io.openshift.expose-services=""
# Wed, 06 May 2026 12:56:35 GMT
LABEL io.openshift.tags="minimal rhel9"
# Wed, 06 May 2026 12:56:35 GMT
ENV container oci
# Wed, 06 May 2026 12:56:36 GMT
COPY dir:80e7e7cac97ce232e3c4b678751f9a2b11cc4a26beaae93a957f83f1fc548f95 in /      
# Wed, 06 May 2026 12:56:36 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Wed, 06 May 2026 12:56:36 GMT
CMD ["/bin/bash"]
# Wed, 06 May 2026 12:56:36 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /usr/share/buildinfo/content-sets.json      
# Wed, 06 May 2026 12:56:36 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /root/buildinfo/content_manifests/content-sets.json      
# Wed, 06 May 2026 12:56:36 GMT
COPY file:bffe3875426b01ab6d752ed5055c4e2d920bf40e31b44b873a80786da1d0750b in /usr/share/buildinfo/labels.json      
# Wed, 06 May 2026 12:56:36 GMT
COPY file:bffe3875426b01ab6d752ed5055c4e2d920bf40e31b44b873a80786da1d0750b in /root/buildinfo/labels.json      
# Wed, 06 May 2026 12:56:37 GMT
LABEL "architecture"="ppc64le" "vcs-type"="git" "vcs-ref"="8def05a6f0dfabdc25ea20a79b0d11f8f9b12c5c" "org.opencontainers.image.revision"="8def05a6f0dfabdc25ea20a79b0d11f8f9b12c5c" "build-date"="2026-05-06T12:56:25Z" "org.opencontainers.image.created"="2026-05-06T12:56:25Z" "release"="1778072020"org.opencontainers.image.revision=8def05a6f0dfabdc25ea20a79b0d11f8f9b12c5c,org.opencontainers.image.created=2026-05-06T12:56:25Z
# Fri, 08 May 2026 16:18:41 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 08 May 2026 16:18:41 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 08 May 2026 16:18:41 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 08 May 2026 16:18:41 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en     ;     microdnf clean all # buildkit
# Fri, 08 May 2026 16:18:41 GMT
ENV JAVA_VERSION=jdk-11.0.31+11
# Fri, 08 May 2026 16:20:40 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='257f4d39e060658fc2eb89a803ca43b3f337e64e253f2d94ebae1d85c9ef5f69';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.31%2B11/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.31_11.tar.gz';          ;;        ppc64le)          ESUM='e473d10c3c44f67301fd90abd9e4b7ae312eae8a2399b333fcf4179daf35a743';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.31%2B11/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.31_11.tar.gz';          ;;        s390x)          ESUM='4d3709cdc03de1a00f14f530c2ebad1883d9bcc8a556fc419f083bec87b4687a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.31%2B11/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.31_11.tar.gz';          ;;        x86_64)          ESUM='1e9de64586b519c0a981319489257cabedd9457599f3823424a87c3158fbe939';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.31%2B11/OpenJDK11U-jdk_x64_linux_hotspot_11.0.31_11.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Fri, 08 May 2026 16:20:43 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Fri, 08 May 2026 16:20:43 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Fri, 08 May 2026 16:20:43 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Fri, 08 May 2026 16:20:43 GMT
CMD ["jshell"]
# Fri, 08 May 2026 16:46:19 GMT
CMD ["gradle"]
# Fri, 08 May 2026 16:46:19 GMT
ENV GRADLE_HOME=/opt/gradle
# Fri, 08 May 2026 16:46:19 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 101 gradle     && useradd --system --gid gradle --uid 101 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Fri, 08 May 2026 16:46:19 GMT
VOLUME [/home/gradle/.gradle]
# Fri, 08 May 2026 16:46:19 GMT
WORKDIR /home/gradle
# Fri, 08 May 2026 16:46:28 GMT
RUN set -o errexit -o nounset     && microdnf install -y         make                 findutils                 unzip         which                 git         git-lfs         subversion     && microdnf clean all         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which svn # buildkit
# Fri, 08 May 2026 16:46:28 GMT
ENV GRADLE_VERSION=6.9.4
# Fri, 08 May 2026 16:46:28 GMT
ARG GRADLE_DOWNLOAD_SHA256=3e240228538de9f18772a574e99a0ba959e83d6ef351014381acd9631781389a
# Fri, 08 May 2026 16:51:13 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=3e240228538de9f18772a574e99a0ba959e83d6ef351014381acd9631781389a
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Fri, 08 May 2026 16:51:13 GMT
USER gradle
# Fri, 08 May 2026 16:51:14 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=3e240228538de9f18772a574e99a0ba959e83d6ef351014381acd9631781389a
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Fri, 08 May 2026 16:51:14 GMT
USER root
```

-	Layers:
	-	`sha256:e3c3e69dacc2a761a2218333f5a3c6de6e1ae1b3afa56e02bcb3f2e70f91db2c`  
		Last Modified: Wed, 06 May 2026 18:13:19 GMT  
		Size: 44.5 MB (44456866 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e30e4b2f46114bf6e128a1cbe09e30dd7493dd7f6692477ad27cf63291c7e84f`  
		Last Modified: Fri, 08 May 2026 16:19:19 GMT  
		Size: 32.8 MB (32843917 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25e9475f98d3e3a0589b1f692f8704ca21321d574cee263d6e3dad76d8d2be1a`  
		Last Modified: Fri, 08 May 2026 16:21:18 GMT  
		Size: 129.6 MB (129614170 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:141a4747ae4ddf0ac3e44ff352c87c40e83a17ec2057b10a63297c3d9583700b`  
		Last Modified: Fri, 08 May 2026 16:21:14 GMT  
		Size: 131.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7fd931c1ddc1e980d9d7570558a50df519a9b3b27c8969b0f371ec19da3f1b1`  
		Last Modified: Fri, 08 May 2026 16:21:14 GMT  
		Size: 2.3 KB (2290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:896fb134bcb3bbdfbb888ead553d25ca62e6419c7b592d8bd3f6509db00c782d`  
		Last Modified: Fri, 08 May 2026 16:47:05 GMT  
		Size: 1.7 KB (1709 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0fbbef53a598f0671df6b5e3ea2725536fa3426100f5eff1db548a702e5292b`  
		Last Modified: Fri, 08 May 2026 16:47:07 GMT  
		Size: 37.9 MB (37922330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:735f08ad36d06d3d76870e66a3b3612d4f50aaef477c9c61d571247aae4ee7a4`  
		Last Modified: Fri, 08 May 2026 16:51:42 GMT  
		Size: 107.7 MB (107696594 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c499ba4747cdedaa99b417a52296fc6566f103dee3da9064f845e7e68987b37c`  
		Last Modified: Fri, 08 May 2026 16:51:39 GMT  
		Size: 35.0 KB (34983 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:6-jdk11-ubi9` - unknown; unknown

```console
$ docker pull gradle@sha256:abbc514a8dd4956a067e065dae4dfe3b6528d12010d52a0abb85766cb6d2f9f8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5336549 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:998ad836b021ec5c2b9e19a19afbcfc10d37f9ee5c1c934686c7ce41ac30a20c`

```dockerfile
```

-	Layers:
	-	`sha256:cdf2b680997661917aef66f2b266c78ba2e4ca6196c3095a65eba5a338d98e03`  
		Last Modified: Fri, 08 May 2026 16:51:40 GMT  
		Size: 5.3 MB (5312904 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:184063d1943040efe6ab82fe5447062464c496c44f24b05fadd4ba5aac63ccbd`  
		Last Modified: Fri, 08 May 2026 16:51:39 GMT  
		Size: 23.6 KB (23645 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:6-jdk11-ubi9` - linux; s390x

```console
$ docker pull gradle@sha256:dbdaae50d246bf9d785aefb29e117f2c4f22af1db0d2f706d0087d76437221f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **335.6 MB (335641973 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:297779e17eb404e0223d4fc8b178a07c9ba9389c8cb89c92e6414ba6636fed46`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["gradle"]`

```dockerfile
# Wed, 06 May 2026 12:58:38 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 06 May 2026 12:58:38 GMT
LABEL vendor="Red Hat, Inc."
# Wed, 06 May 2026 12:58:38 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Wed, 06 May 2026 12:58:38 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.7"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Wed, 06 May 2026 12:58:38 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 06 May 2026 12:58:38 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Wed, 06 May 2026 12:58:38 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 06 May 2026 12:58:38 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 06 May 2026 12:58:38 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Wed, 06 May 2026 12:58:38 GMT
LABEL io.openshift.expose-services=""
# Wed, 06 May 2026 12:58:38 GMT
LABEL io.openshift.tags="minimal rhel9"
# Wed, 06 May 2026 12:58:38 GMT
ENV container oci
# Wed, 06 May 2026 12:58:39 GMT
COPY dir:250395052a40de9f7889404c39a2210eeb69810388356e3199f203bccf8ea29a in /      
# Wed, 06 May 2026 12:58:39 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Wed, 06 May 2026 12:58:39 GMT
CMD ["/bin/bash"]
# Wed, 06 May 2026 12:58:39 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /usr/share/buildinfo/content-sets.json      
# Wed, 06 May 2026 12:58:39 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /root/buildinfo/content_manifests/content-sets.json      
# Wed, 06 May 2026 12:58:39 GMT
COPY file:9bfc8864fac218dad35298e422b5699ec3450e18977e43381ee12e6d5ca8febe in /usr/share/buildinfo/labels.json      
# Wed, 06 May 2026 12:58:39 GMT
COPY file:9bfc8864fac218dad35298e422b5699ec3450e18977e43381ee12e6d5ca8febe in /root/buildinfo/labels.json      
# Wed, 06 May 2026 12:58:39 GMT
LABEL "architecture"="s390x" "vcs-type"="git" "vcs-ref"="8def05a6f0dfabdc25ea20a79b0d11f8f9b12c5c" "org.opencontainers.image.revision"="8def05a6f0dfabdc25ea20a79b0d11f8f9b12c5c" "build-date"="2026-05-06T12:58:27Z" "org.opencontainers.image.created"="2026-05-06T12:58:27Z" "release"="1778072020"org.opencontainers.image.revision=8def05a6f0dfabdc25ea20a79b0d11f8f9b12c5c,org.opencontainers.image.created=2026-05-06T12:58:27Z
# Fri, 08 May 2026 16:18:51 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 08 May 2026 16:18:51 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 08 May 2026 16:18:51 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 08 May 2026 16:18:51 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en     ;     microdnf clean all # buildkit
# Fri, 08 May 2026 16:18:51 GMT
ENV JAVA_VERSION=jdk-11.0.31+11
# Fri, 08 May 2026 16:18:57 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='257f4d39e060658fc2eb89a803ca43b3f337e64e253f2d94ebae1d85c9ef5f69';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.31%2B11/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.31_11.tar.gz';          ;;        ppc64le)          ESUM='e473d10c3c44f67301fd90abd9e4b7ae312eae8a2399b333fcf4179daf35a743';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.31%2B11/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.31_11.tar.gz';          ;;        s390x)          ESUM='4d3709cdc03de1a00f14f530c2ebad1883d9bcc8a556fc419f083bec87b4687a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.31%2B11/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.31_11.tar.gz';          ;;        x86_64)          ESUM='1e9de64586b519c0a981319489257cabedd9457599f3823424a87c3158fbe939';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.31%2B11/OpenJDK11U-jdk_x64_linux_hotspot_11.0.31_11.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Fri, 08 May 2026 16:18:59 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Fri, 08 May 2026 16:18:59 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Fri, 08 May 2026 16:18:59 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Fri, 08 May 2026 16:18:59 GMT
CMD ["jshell"]
# Fri, 08 May 2026 16:28:51 GMT
CMD ["gradle"]
# Fri, 08 May 2026 16:28:51 GMT
ENV GRADLE_HOME=/opt/gradle
# Fri, 08 May 2026 16:28:51 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 101 gradle     && useradd --system --gid gradle --uid 101 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Fri, 08 May 2026 16:28:51 GMT
VOLUME [/home/gradle/.gradle]
# Fri, 08 May 2026 16:28:51 GMT
WORKDIR /home/gradle
# Fri, 08 May 2026 16:28:57 GMT
RUN set -o errexit -o nounset     && microdnf install -y         make                 findutils                 unzip         which                 git         git-lfs         subversion     && microdnf clean all         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which svn # buildkit
# Fri, 08 May 2026 16:28:57 GMT
ENV GRADLE_VERSION=6.9.4
# Fri, 08 May 2026 16:28:57 GMT
ARG GRADLE_DOWNLOAD_SHA256=3e240228538de9f18772a574e99a0ba959e83d6ef351014381acd9631781389a
# Fri, 08 May 2026 16:29:02 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=3e240228538de9f18772a574e99a0ba959e83d6ef351014381acd9631781389a
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Fri, 08 May 2026 16:29:02 GMT
USER gradle
# Fri, 08 May 2026 16:29:03 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=3e240228538de9f18772a574e99a0ba959e83d6ef351014381acd9631781389a
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Fri, 08 May 2026 16:29:03 GMT
USER root
```

-	Layers:
	-	`sha256:a56758fa2ad3a40734485cf04844d90c8ea5263253fa4b0f660db9b8fd177029`  
		Last Modified: Wed, 06 May 2026 16:37:40 GMT  
		Size: 38.1 MB (38128488 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b82d7924b147679b7f6c6aee81aed24ae8fb0dfec5dc6fc7652492eb8bb1dad8`  
		Last Modified: Fri, 08 May 2026 16:19:28 GMT  
		Size: 30.4 MB (30382391 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3805f29a7c4e22938585bf3aa95d0cad7f3c7b6f6f60a4370424c52b759cadee`  
		Last Modified: Fri, 08 May 2026 16:19:30 GMT  
		Size: 123.1 MB (123061426 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3cf385574e7eaee23dd458cab38c8a9f25496072398ff9f6aa4ee39ed8fabe60`  
		Last Modified: Fri, 08 May 2026 16:19:27 GMT  
		Size: 130.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5550faf19fc1dbddbdda153cb82291817a159082f81d9c2e01a32e7a5261b954`  
		Last Modified: Fri, 08 May 2026 16:19:19 GMT  
		Size: 2.3 KB (2291 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f5c91b6b6da99dd07fee074b9654a246ca521c2bf3c8d4e710b01998a106e2c`  
		Last Modified: Fri, 08 May 2026 16:29:30 GMT  
		Size: 1.7 KB (1709 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0613c81924b7c07bd9083387b64a76d45e5c7f34fb36476cc11c68c7b403a672`  
		Last Modified: Fri, 08 May 2026 16:29:32 GMT  
		Size: 36.3 MB (36333848 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a50fc9439d6db6926a54d5a6c64faa324053dd8fdccd9cb9d078671e04643fd9`  
		Last Modified: Fri, 08 May 2026 16:29:33 GMT  
		Size: 107.7 MB (107696669 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c2c87c27ffc99b87ec034e94a903812ca19fa9640cc55aa7e21302df26c30a4`  
		Last Modified: Fri, 08 May 2026 16:29:30 GMT  
		Size: 35.0 KB (34989 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:6-jdk11-ubi9` - unknown; unknown

```console
$ docker pull gradle@sha256:d1aff3588ce78c48d64040c85801a43d2d246b30af199b0b9c8caf686fe6828d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5326388 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:baf8712259695a3facbfaf449f59cbbc3b91c69e98471dedaa99b92a25bec3e2`

```dockerfile
```

-	Layers:
	-	`sha256:980f0fa7fbfd0117ba20f761f9fc75ba43fc7fe2276fa95f65707375bfcc59ad`  
		Last Modified: Fri, 08 May 2026 16:29:30 GMT  
		Size: 5.3 MB (5302805 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:db17c94b092d174bd09a2b71b730c86e26be76210338425c39463bb0acfd31c1`  
		Last Modified: Fri, 08 May 2026 16:29:30 GMT  
		Size: 23.6 KB (23583 bytes)  
		MIME: application/vnd.in-toto+json
