## `gradle:8-jdk11-ubi9`

```console
$ docker pull gradle@sha256:d401b08f0f7e70065858f6252770044b361ecc3344186f04e2abeb36f4b5d180
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

### `gradle:8-jdk11-ubi9` - linux; amd64

```console
$ docker pull gradle@sha256:f43553808924ebf77ec77d38cb8354e572f3fc081eeccd7f375d1360fb238c34
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **387.5 MB (387533372 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d09e4bcb6c1cd356337cf2b44e31e50dd248f612f0422c865f889e64d87be87a`
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
# Fri, 08 May 2026 17:48:13 GMT
CMD ["gradle"]
# Fri, 08 May 2026 17:48:13 GMT
ENV GRADLE_HOME=/opt/gradle
# Fri, 08 May 2026 17:48:13 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 101 gradle     && useradd --system --gid gradle --uid 101 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Fri, 08 May 2026 17:48:13 GMT
VOLUME [/home/gradle/.gradle]
# Fri, 08 May 2026 17:48:13 GMT
WORKDIR /home/gradle
# Fri, 08 May 2026 17:48:17 GMT
RUN set -o errexit -o nounset     && microdnf install -y         make         curl-minimal         wget         tar                 findutils                 unzip         which                 git         git-lfs         subversion     && microdnf clean all         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which svn # buildkit
# Fri, 08 May 2026 17:48:17 GMT
ENV GRADLE_VERSION=8.14.5
# Fri, 08 May 2026 17:48:17 GMT
ARG GRADLE_DOWNLOAD_SHA256=6f74b601422d6d6fc4e1f9a1ab6522f642c2fdcbc15ae33ebd30ba3d7198e854
# Fri, 08 May 2026 17:48:19 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=6f74b601422d6d6fc4e1f9a1ab6522f642c2fdcbc15ae33ebd30ba3d7198e854
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Fri, 08 May 2026 17:48:19 GMT
USER gradle
# Fri, 08 May 2026 17:48:20 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=6f74b601422d6d6fc4e1f9a1ab6522f642c2fdcbc15ae33ebd30ba3d7198e854
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --stacktrace --debug --version # buildkit
# Fri, 08 May 2026 17:48:20 GMT
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
	-	`sha256:ac2bc36e13df4662603ecc1ca816890cc27c0ca5d795e414f1f2ac368f13864c`  
		Last Modified: Fri, 08 May 2026 17:48:37 GMT  
		Size: 1.7 KB (1708 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91a9b3767033bfe6582213445ad8b92ae55d6bbef671cf24587553bab9623638`  
		Last Modified: Fri, 08 May 2026 17:48:39 GMT  
		Size: 36.7 MB (36693373 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:111193db5c3caefd3755dcf9ea8da682a505153d6088321a5d313961e5feef5f`  
		Last Modified: Fri, 08 May 2026 17:48:41 GMT  
		Size: 138.1 MB (138068549 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0c561ef8fff4106119f3c37d617223ab24096bc2846b825470a901be07fbf9f`  
		Last Modified: Fri, 08 May 2026 17:48:37 GMT  
		Size: 54.9 KB (54900 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:8-jdk11-ubi9` - unknown; unknown

```console
$ docker pull gradle@sha256:cabe77cf70fcf659fac8508e4747e85a67ec6714d91113092ede48f0d77e5b56
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5448503 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7722d4d67683c2a16baafed50555ad71c06bccd2d60b8db4e0465634bf0e6b52`

```dockerfile
```

-	Layers:
	-	`sha256:3fb6901c2cbd5d77f5b9fdd87aff48914d297fd1705b63a1491a40238a21bcde`  
		Last Modified: Fri, 08 May 2026 17:48:37 GMT  
		Size: 5.4 MB (5424049 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:60ecfcd94ce14d0dc40b92a964a53b0e133efb62f7e69898f1969e5661b82eda`  
		Last Modified: Fri, 08 May 2026 17:48:37 GMT  
		Size: 24.5 KB (24454 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:8-jdk11-ubi9` - linux; arm64 variant v8

```console
$ docker pull gradle@sha256:52e70d262976284cfd50ec2bdf791830fa8118d45ec1aa53cf0fc8bb12c1b4b9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **382.2 MB (382194403 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:055837c28bd70451ca6889f297fd35f1a213334024b4d02aa8f10733d821f7ef`
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
# Fri, 08 May 2026 17:48:39 GMT
CMD ["gradle"]
# Fri, 08 May 2026 17:48:39 GMT
ENV GRADLE_HOME=/opt/gradle
# Fri, 08 May 2026 17:48:39 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 101 gradle     && useradd --system --gid gradle --uid 101 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Fri, 08 May 2026 17:48:39 GMT
VOLUME [/home/gradle/.gradle]
# Fri, 08 May 2026 17:48:39 GMT
WORKDIR /home/gradle
# Fri, 08 May 2026 17:48:46 GMT
RUN set -o errexit -o nounset     && microdnf install -y         make         curl-minimal         wget         tar                 findutils                 unzip         which                 git         git-lfs         subversion     && microdnf clean all         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which svn # buildkit
# Fri, 08 May 2026 17:48:46 GMT
ENV GRADLE_VERSION=8.14.5
# Fri, 08 May 2026 17:48:46 GMT
ARG GRADLE_DOWNLOAD_SHA256=6f74b601422d6d6fc4e1f9a1ab6522f642c2fdcbc15ae33ebd30ba3d7198e854
# Fri, 08 May 2026 17:48:49 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=6f74b601422d6d6fc4e1f9a1ab6522f642c2fdcbc15ae33ebd30ba3d7198e854
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Fri, 08 May 2026 17:48:49 GMT
USER gradle
# Fri, 08 May 2026 17:48:49 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=6f74b601422d6d6fc4e1f9a1ab6522f642c2fdcbc15ae33ebd30ba3d7198e854
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --stacktrace --debug --version # buildkit
# Fri, 08 May 2026 17:48:49 GMT
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
	-	`sha256:9076ebd5281eb57eb73673069e1452bf580b54d34ab04298794ea11079c6208a`  
		Last Modified: Fri, 08 May 2026 17:49:06 GMT  
		Size: 1.7 KB (1707 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ba148496696147a8863814d355cb280036a89eed1d0108288ffe5a3aeabecb7`  
		Last Modified: Fri, 08 May 2026 17:49:07 GMT  
		Size: 36.0 MB (36026472 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8d26d1df43a60927607fbdf9e4774abf60f2b9b991270f77f4d0fc485f5e6ea`  
		Last Modified: Fri, 08 May 2026 17:49:11 GMT  
		Size: 138.1 MB (138068570 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37fdf3055d35e1b3b56208fca7c5b83a5c804fcb27384304ab7c25825671d25d`  
		Last Modified: Fri, 08 May 2026 17:49:06 GMT  
		Size: 59.5 KB (59525 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:8-jdk11-ubi9` - unknown; unknown

```console
$ docker pull gradle@sha256:b35bc9fe5182da6b52e010f401414a95e4a22ea22d012417a3f68954b0361b32
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5448748 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b07bb590b987f93128cfbba55d3a44d6807b795ee1d90ba5ce2c03032189cab2`

```dockerfile
```

-	Layers:
	-	`sha256:c8430883bcd9044e45dc7605561ddfaadfe655ab07610ca1aefe15deadd38a82`  
		Last Modified: Fri, 08 May 2026 17:49:06 GMT  
		Size: 5.4 MB (5424097 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a16741784296c6cd6c8f87de9e73cf70c4151bd3d08ccc5f1cf23e534d0506d2`  
		Last Modified: Fri, 08 May 2026 17:49:06 GMT  
		Size: 24.7 KB (24651 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:8-jdk11-ubi9` - linux; ppc64le

```console
$ docker pull gradle@sha256:b4dee887cf34c28e447881e42081e3f9cb93baed50e0084797a5f8e145029494
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **382.9 MB (382945266 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a458145460e2f86d4a940d04eb53a8685583315f29b3aaa5b3b76c0fbdbee4b3`
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
# Fri, 08 May 2026 20:08:38 GMT
RUN set -o errexit -o nounset     && microdnf install -y         make         curl-minimal         wget         tar                 findutils                 unzip         which                 git         git-lfs         subversion     && microdnf clean all         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which svn # buildkit
# Fri, 08 May 2026 20:08:38 GMT
ENV GRADLE_VERSION=8.14.5
# Fri, 08 May 2026 20:08:38 GMT
ARG GRADLE_DOWNLOAD_SHA256=6f74b601422d6d6fc4e1f9a1ab6522f642c2fdcbc15ae33ebd30ba3d7198e854
# Fri, 08 May 2026 20:08:43 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=6f74b601422d6d6fc4e1f9a1ab6522f642c2fdcbc15ae33ebd30ba3d7198e854
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Fri, 08 May 2026 20:08:43 GMT
USER gradle
# Fri, 08 May 2026 20:08:44 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=6f74b601422d6d6fc4e1f9a1ab6522f642c2fdcbc15ae33ebd30ba3d7198e854
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --stacktrace --debug --version # buildkit
# Fri, 08 May 2026 20:08:44 GMT
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
	-	`sha256:15be912a0d21e2a2e7c180a40c812220def0680ee6cf87702a7784f9852d5e53`  
		Last Modified: Fri, 08 May 2026 20:09:20 GMT  
		Size: 37.9 MB (37922603 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d06e185fc5bcf3e54c6a906edcaccec8537141943adbf0302b19a6afe0668e81`  
		Last Modified: Fri, 08 May 2026 20:09:22 GMT  
		Size: 138.1 MB (138068540 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5a635f87b8f8151c8a9a579db84f10bc70662b39c0f584cea1d77db32891b1a`  
		Last Modified: Fri, 08 May 2026 20:09:18 GMT  
		Size: 35.0 KB (35008 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:8-jdk11-ubi9` - unknown; unknown

```console
$ docker pull gradle@sha256:cbd63b5c369e4fbb108d0b344b0bf423a08dd2a7847b9b5a21f2e3ea0104e8cf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5445333 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dcbc856b45039dd29d2aafce0c05c5d8c64e81c99af2f21bd8a2be8157e9596b`

```dockerfile
```

-	Layers:
	-	`sha256:906231a81e7fda2755afcac81dda0b537ceb06832e41037e8efe9a43e16738da`  
		Last Modified: Fri, 08 May 2026 20:09:18 GMT  
		Size: 5.4 MB (5420769 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d67997d56122c6bb50933b740940a5c5e94f1d16536904967d256254886bc1b5`  
		Last Modified: Fri, 08 May 2026 20:09:17 GMT  
		Size: 24.6 KB (24564 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:8-jdk11-ubi9` - linux; s390x

```console
$ docker pull gradle@sha256:c078ec0f8cd83ef03f60602b544697ebdea87f8a1436df760e622516d5adbc8c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **366.0 MB (366013250 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:278718b1dc1100ef8669c7bb2c85085f9115661e56f835e292152f4bff6a6e34`
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
# Fri, 08 May 2026 16:28:34 GMT
CMD ["gradle"]
# Fri, 08 May 2026 16:28:34 GMT
ENV GRADLE_HOME=/opt/gradle
# Fri, 08 May 2026 16:28:34 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 101 gradle     && useradd --system --gid gradle --uid 101 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Fri, 08 May 2026 16:28:34 GMT
VOLUME [/home/gradle/.gradle]
# Fri, 08 May 2026 16:28:34 GMT
WORKDIR /home/gradle
# Fri, 08 May 2026 17:53:15 GMT
RUN set -o errexit -o nounset     && microdnf install -y         make         curl-minimal         wget         tar                 findutils                 unzip         which                 git         git-lfs         subversion     && microdnf clean all         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which svn # buildkit
# Fri, 08 May 2026 17:53:15 GMT
ENV GRADLE_VERSION=8.14.5
# Fri, 08 May 2026 17:53:15 GMT
ARG GRADLE_DOWNLOAD_SHA256=6f74b601422d6d6fc4e1f9a1ab6522f642c2fdcbc15ae33ebd30ba3d7198e854
# Fri, 08 May 2026 17:53:19 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=6f74b601422d6d6fc4e1f9a1ab6522f642c2fdcbc15ae33ebd30ba3d7198e854
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Fri, 08 May 2026 17:53:19 GMT
USER gradle
# Fri, 08 May 2026 17:53:19 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=6f74b601422d6d6fc4e1f9a1ab6522f642c2fdcbc15ae33ebd30ba3d7198e854
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --stacktrace --debug --version # buildkit
# Fri, 08 May 2026 17:53:19 GMT
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
	-	`sha256:bb03fd65482855dc159ef0b4ab097f8815a9d402187339895e34381aced95c7c`  
		Last Modified: Fri, 08 May 2026 16:29:13 GMT  
		Size: 1.7 KB (1708 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e988bea0ddac5b73eaf287c1f7adb220ca51b9524d3f6b0adda1e6a30773779a`  
		Last Modified: Fri, 08 May 2026 17:53:44 GMT  
		Size: 36.3 MB (36333240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80a5d00df36bb0670cbb61b4944dbf88f43404448da9946b52beddc3c95ec268`  
		Last Modified: Fri, 08 May 2026 17:53:47 GMT  
		Size: 138.1 MB (138068540 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d0c140227dcf60cc89f4830669a072a76278b78ad72cc763edb353fe8bb08af`  
		Last Modified: Fri, 08 May 2026 17:53:43 GMT  
		Size: 35.0 KB (35004 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:8-jdk11-ubi9` - unknown; unknown

```console
$ docker pull gradle@sha256:b98ece62036e13356d472de85365206a7d33dd4d7b6142f4dc8720cfec8414e9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5435148 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea9c6ddc514756baca131c82be8808d75ecef7482310a37b8246f8afc72e4e98`

```dockerfile
```

-	Layers:
	-	`sha256:b2b4f425d7bb93cd86dfe36912bd05ebbb327a5f1a544686331db58ec58648a3`  
		Last Modified: Fri, 08 May 2026 17:53:43 GMT  
		Size: 5.4 MB (5410658 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:99f9578f771446ce0529bec36e1ad9b3cfb70e7e1e046b915cade9ebec41a9d2`  
		Last Modified: Fri, 08 May 2026 17:53:43 GMT  
		Size: 24.5 KB (24490 bytes)  
		MIME: application/vnd.in-toto+json
