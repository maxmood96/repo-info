## `gradle:jdk8-ubi`

```console
$ docker pull gradle@sha256:83653c4f0f71173ddeef1e84367e9fdde765212fe18b7c9f5d1aab422f567fd8
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `gradle:jdk8-ubi` - linux; amd64

```console
$ docker pull gradle@sha256:e7d68a6bab700b1e6d18ea1563e1cf8d722719831bcbbc4f8df4442fd7f63e90
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **303.7 MB (303719512 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cfd7531a956a3290a50c899f7efd70d4fbc7520df2926d805cc2aa4e36f20025`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["gradle"]`

```dockerfile
# Thu, 30 Jan 2025 14:32:57 GMT
LABEL maintainer="Red Hat, Inc."
# Thu, 30 Jan 2025 14:32:57 GMT
LABEL vendor="Red Hat, Inc."
# Thu, 30 Jan 2025 14:32:57 GMT
LABEL url="https://www.redhat.com"
# Thu, 30 Jan 2025 14:32:57 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.5"       distribution-scope="public"
# Thu, 30 Jan 2025 14:32:57 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Thu, 30 Jan 2025 14:32:57 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Thu, 30 Jan 2025 14:32:57 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 30 Jan 2025 14:32:57 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 30 Jan 2025 14:32:57 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Thu, 30 Jan 2025 14:32:57 GMT
LABEL io.openshift.expose-services=""
# Thu, 30 Jan 2025 14:32:57 GMT
LABEL io.openshift.tags="minimal rhel9"
# Thu, 30 Jan 2025 14:32:57 GMT
ENV container oci
# Thu, 30 Jan 2025 14:32:57 GMT
COPY dir:a07d6464b408a07384eb87b8e371fb05260f293df1fdae9e20c1a6653e15e37b in / 
# Thu, 30 Jan 2025 14:32:57 GMT
COPY file:b37d593713ee21ad52a4cd1424dc019a24f7966f85df0ac4b86d234302695328 in /etc/yum.repos.d/. 
# Thu, 30 Jan 2025 14:32:57 GMT
CMD ["/bin/bash"]
# Thu, 30 Jan 2025 14:32:57 GMT
RUN . /cachi2/cachi2.env &&     rm -rf /var/log/*
# Thu, 30 Jan 2025 14:32:57 GMT
LABEL "build-date"="2025-03-10T09:47:15" "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="2f8e6c4d7ad22789d5663bf4bd66603301fba889" "build-date"="2025-03-10T09:43:12Z" "release"="1741599792"
# Thu, 30 Jan 2025 14:32:57 GMT
RUN /bin/sh
# Thu, 30 Jan 2025 14:32:57 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 30 Jan 2025 14:32:57 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 30 Jan 2025 14:32:57 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 30 Jan 2025 14:32:57 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         fontconfig         glibc-langpack-en     ;     microdnf clean all # buildkit
# Thu, 30 Jan 2025 14:32:57 GMT
ENV JAVA_VERSION=jdk8u442-b06
# Thu, 30 Jan 2025 14:32:57 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='1d1662bd8ca7edc9281c723d9eebafea940e6a41464bdc43a83b564bc974c7e5';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u442-b06/OpenJDK8U-jdk_aarch64_linux_hotspot_8u442b06.tar.gz';          ;;        ppc64le)          ESUM='7eac77deb8fc6c6130f9445c9a68af0bcc40bf6736b5672ef5c3d737c025e84d';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u442-b06/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u442b06.tar.gz';          ;;        x86_64)          ESUM='5b0a0145e7790552a9c8767b4680074c4628ec276e5bb278b61d85cf90facafa';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u442-b06/OpenJDK8U-jdk_x64_linux_hotspot_8u442b06.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip; # buildkit
# Thu, 30 Jan 2025 14:32:57 GMT
RUN set -eux;     echo "Verifying install ...";     echo "javac -version"; javac -version;     echo "java -version"; java -version;     echo "Complete." # buildkit
# Thu, 30 Jan 2025 14:32:57 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 30 Jan 2025 14:32:57 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 04 Mar 2025 19:20:27 GMT
CMD ["gradle"]
# Tue, 04 Mar 2025 19:20:27 GMT
ENV GRADLE_HOME=/opt/gradle
# Tue, 04 Mar 2025 19:20:27 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 101 gradle     && useradd --system --gid gradle --uid 101 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Tue, 04 Mar 2025 19:20:27 GMT
VOLUME [/home/gradle/.gradle]
# Tue, 04 Mar 2025 19:20:27 GMT
WORKDIR /home/gradle
# Tue, 04 Mar 2025 19:20:27 GMT
RUN set -o errexit -o nounset     && microdnf install -y         findutils                 unzip         wget         which                 git         git-lfs         subversion     && microdnf clean all         && echo "Testing VCSes"     && which git     && which git-lfs     && which svn # buildkit
# Tue, 04 Mar 2025 19:20:27 GMT
ENV GRADLE_VERSION=8.13
# Tue, 04 Mar 2025 19:20:27 GMT
ARG GRADLE_DOWNLOAD_SHA256=20f1b1176237254a6fc204d8434196fa11a4cfb387567519c61556e8710aed78
# Tue, 04 Mar 2025 19:20:27 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=20f1b1176237254a6fc204d8434196fa11a4cfb387567519c61556e8710aed78
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Tue, 04 Mar 2025 19:20:27 GMT
USER gradle
# Tue, 04 Mar 2025 19:20:27 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=20f1b1176237254a6fc204d8434196fa11a4cfb387567519c61556e8710aed78
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Tue, 04 Mar 2025 19:20:27 GMT
USER root
```

-	Layers:
	-	`sha256:ecb02bde81105b662eaf8da4b200f811c2ac8a0dd37e0c09f19de54603c5c8fb`  
		Last Modified: Mon, 10 Mar 2025 10:32:31 GMT  
		Size: 39.4 MB (39376539 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e92b0a09d78952dd6b3d60aa8a9f9ef1c8282b59a65bcc5aa506acb82686576`  
		Last Modified: Mon, 10 Mar 2025 10:32:31 GMT  
		Size: 462.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:947912d0364243a56a7753f18fa800e7eb99a07684bd7d1f85bfe4469c3023e1`  
		Last Modified: Mon, 10 Mar 2025 21:05:52 GMT  
		Size: 37.0 MB (36972891 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32f92f4c6ac845dc3089af5d658aa3e48de77025e36fd261222831a1be862319`  
		Last Modified: Mon, 10 Mar 2025 21:05:52 GMT  
		Size: 54.7 MB (54721731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:028cb8c0898a4372760e4e74c656a8be158e8c1122c3353225fcf16b7c82ce6a`  
		Last Modified: Mon, 10 Mar 2025 21:05:50 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3eab0a17af2d4c55016962b575120bb6a025e33f02aee84e6954ca339de91345`  
		Last Modified: Mon, 10 Mar 2025 21:05:50 GMT  
		Size: 2.3 KB (2317 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf3271f303b52708ce5fd5d2dd0957c1af44d20f77f30b52549b7669291ba720`  
		Last Modified: Mon, 10 Mar 2025 21:09:06 GMT  
		Size: 1.7 KB (1705 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:974b68d9969bdd18e14dbcd3db4c6fe59c712c5f4654fbe0575b3dac005072ed`  
		Last Modified: Mon, 10 Mar 2025 21:09:08 GMT  
		Size: 35.6 MB (35600617 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f56780f57b308ed090cecae34308e488378594629365c9da2d69c54649b3f66`  
		Last Modified: Mon, 10 Mar 2025 21:09:10 GMT  
		Size: 137.0 MB (136988190 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba1be5a4a772b9c46350fdd5271f89612361ec8d2d739ee6f66e41d690308dcd`  
		Last Modified: Mon, 10 Mar 2025 21:09:06 GMT  
		Size: 54.9 KB (54900 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:jdk8-ubi` - unknown; unknown

```console
$ docker pull gradle@sha256:4308fc7c5652e52f8408b81827726c06c732b6b85949a519fa954610d8584360
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6650790 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3b17cf10804d6ae0f1edf374846cc8dd201de56480c4526aeeee1003f079891c`

```dockerfile
```

-	Layers:
	-	`sha256:03fb54a33e010ab53526d70e1e9888de5e58b1a6c88e17a5cf62504f25305a84`  
		Last Modified: Mon, 10 Mar 2025 21:09:07 GMT  
		Size: 6.6 MB (6627654 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1aa7b9bb19a6ec7881d9242ac95e15fe5e6469b574ab772da7b0632f7d6c7134`  
		Last Modified: Mon, 10 Mar 2025 21:09:06 GMT  
		Size: 23.1 KB (23136 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:jdk8-ubi` - linux; arm64 variant v8

```console
$ docker pull gradle@sha256:f9b3551726912d06916668d8f0cfc8b9b0f1f2ce00417c1e6070a73020be5795
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **301.0 MB (300979174 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d5cb5a7047941eef3f91600bd315ec87a095db5876c5752638c452b3e47e841`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["gradle"]`

```dockerfile
# Thu, 30 Jan 2025 14:32:57 GMT
LABEL maintainer="Red Hat, Inc."
# Thu, 30 Jan 2025 14:32:57 GMT
LABEL vendor="Red Hat, Inc."
# Thu, 30 Jan 2025 14:32:57 GMT
LABEL url="https://www.redhat.com"
# Thu, 30 Jan 2025 14:32:57 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.5"       distribution-scope="public"
# Thu, 30 Jan 2025 14:32:57 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Thu, 30 Jan 2025 14:32:57 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Thu, 30 Jan 2025 14:32:57 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 30 Jan 2025 14:32:57 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 30 Jan 2025 14:32:57 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Thu, 30 Jan 2025 14:32:57 GMT
LABEL io.openshift.expose-services=""
# Thu, 30 Jan 2025 14:32:57 GMT
LABEL io.openshift.tags="minimal rhel9"
# Thu, 30 Jan 2025 14:32:57 GMT
ENV container oci
# Thu, 30 Jan 2025 14:32:57 GMT
COPY dir:7cf9b7b9f60ce494e82504114b8e4e8497504001337c87ffc50d4a40fe4f9edc in / 
# Thu, 30 Jan 2025 14:32:57 GMT
COPY file:b37d593713ee21ad52a4cd1424dc019a24f7966f85df0ac4b86d234302695328 in /etc/yum.repos.d/. 
# Thu, 30 Jan 2025 14:32:57 GMT
CMD ["/bin/bash"]
# Thu, 30 Jan 2025 14:32:57 GMT
RUN . /cachi2/cachi2.env &&     rm -rf /var/log/*
# Thu, 30 Jan 2025 14:32:57 GMT
LABEL "build-date"="2025-03-10T09:50:07" "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="2f8e6c4d7ad22789d5663bf4bd66603301fba889" "build-date"="2025-03-10T09:43:12Z" "release"="1741599792"
# Thu, 30 Jan 2025 14:32:57 GMT
RUN /bin/sh
# Thu, 30 Jan 2025 14:32:57 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 30 Jan 2025 14:32:57 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 30 Jan 2025 14:32:57 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 30 Jan 2025 14:32:57 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         fontconfig         glibc-langpack-en     ;     microdnf clean all # buildkit
# Thu, 30 Jan 2025 14:32:57 GMT
ENV JAVA_VERSION=jdk8u442-b06
# Thu, 30 Jan 2025 14:32:57 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='1d1662bd8ca7edc9281c723d9eebafea940e6a41464bdc43a83b564bc974c7e5';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u442-b06/OpenJDK8U-jdk_aarch64_linux_hotspot_8u442b06.tar.gz';          ;;        ppc64le)          ESUM='7eac77deb8fc6c6130f9445c9a68af0bcc40bf6736b5672ef5c3d737c025e84d';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u442-b06/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u442b06.tar.gz';          ;;        x86_64)          ESUM='5b0a0145e7790552a9c8767b4680074c4628ec276e5bb278b61d85cf90facafa';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u442-b06/OpenJDK8U-jdk_x64_linux_hotspot_8u442b06.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip; # buildkit
# Thu, 30 Jan 2025 14:32:57 GMT
RUN set -eux;     echo "Verifying install ...";     echo "javac -version"; javac -version;     echo "java -version"; java -version;     echo "Complete." # buildkit
# Thu, 30 Jan 2025 14:32:57 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 30 Jan 2025 14:32:57 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 04 Mar 2025 19:20:27 GMT
CMD ["gradle"]
# Tue, 04 Mar 2025 19:20:27 GMT
ENV GRADLE_HOME=/opt/gradle
# Tue, 04 Mar 2025 19:20:27 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 101 gradle     && useradd --system --gid gradle --uid 101 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Tue, 04 Mar 2025 19:20:27 GMT
VOLUME [/home/gradle/.gradle]
# Tue, 04 Mar 2025 19:20:27 GMT
WORKDIR /home/gradle
# Tue, 04 Mar 2025 19:20:27 GMT
RUN set -o errexit -o nounset     && microdnf install -y         findutils                 unzip         wget         which                 git         git-lfs         subversion     && microdnf clean all         && echo "Testing VCSes"     && which git     && which git-lfs     && which svn # buildkit
# Tue, 04 Mar 2025 19:20:27 GMT
ENV GRADLE_VERSION=8.13
# Tue, 04 Mar 2025 19:20:27 GMT
ARG GRADLE_DOWNLOAD_SHA256=20f1b1176237254a6fc204d8434196fa11a4cfb387567519c61556e8710aed78
# Tue, 04 Mar 2025 19:20:27 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=20f1b1176237254a6fc204d8434196fa11a4cfb387567519c61556e8710aed78
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Tue, 04 Mar 2025 19:20:27 GMT
USER gradle
# Tue, 04 Mar 2025 19:20:27 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=20f1b1176237254a6fc204d8434196fa11a4cfb387567519c61556e8710aed78
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Tue, 04 Mar 2025 19:20:27 GMT
USER root
```

-	Layers:
	-	`sha256:f7b8fe7f82e9c2744a37d9d57d915bba00fe3879ae010a254770d6de52407d6b`  
		Last Modified: Mon, 10 Mar 2025 10:36:22 GMT  
		Size: 37.6 MB (37585537 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b83df990133b9bdb95a233cede88e14a9e9f42d8a90daca3368a0795857bbf6`  
		Last Modified: Mon, 10 Mar 2025 10:36:20 GMT  
		Size: 460.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac9ed2e900cb7085312fdb231cce5437b781a3044b7d2f27cc07d6e098d2d925`  
		Last Modified: Mon, 10 Mar 2025 21:19:31 GMT  
		Size: 37.4 MB (37433861 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f91edd6d26dd0b100a563a076744f944168d755c70d1b7d0b39388f1d26e947`  
		Last Modified: Mon, 10 Mar 2025 21:19:31 GMT  
		Size: 53.8 MB (53823300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:417a3b5b3f907eb0b13339e662d3996f1cdaba9825356a5c9fcee3e3b93ad3a7`  
		Last Modified: Mon, 10 Mar 2025 21:19:30 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36fbf52f2fd4adf7ccc6cd665902bf33411a225f89591333a095045595d39636`  
		Last Modified: Mon, 10 Mar 2025 21:19:31 GMT  
		Size: 2.3 KB (2316 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5ed13151d28ace6b0f608ec10b5ebcbaa5381112241d1efc07e9c976f966e1c`  
		Last Modified: Mon, 10 Mar 2025 22:15:22 GMT  
		Size: 1.7 KB (1703 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71957f44233ffc5fa2b8c6213bdbe1b8b5a676c0455e5ec6922d131226c8d2e4`  
		Last Modified: Mon, 10 Mar 2025 22:15:23 GMT  
		Size: 35.1 MB (35084126 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d834cc712ea7378c9ae818773f9aee1b1ca72f84e19d0946f0abfceccd2ce5fc`  
		Last Modified: Mon, 10 Mar 2025 22:15:27 GMT  
		Size: 137.0 MB (136988181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a33fb649c8175d54a737f5f84dc9638b15bd14a70f7c221fcda011093adb3cd`  
		Last Modified: Mon, 10 Mar 2025 22:15:22 GMT  
		Size: 59.5 KB (59530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:jdk8-ubi` - unknown; unknown

```console
$ docker pull gradle@sha256:5827307b5dd90b4ca557425132b8f9cf694f8de797d753176e3661f703d134c4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6650892 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eef15235c0b40e3e15aa8c21ae21a746ccd7af42a8dd4fd03cf2d218a3d15476`

```dockerfile
```

-	Layers:
	-	`sha256:c401da7228f3860520f3389bd693cd2b44b0cf9bc5d3d6ecce2dbe1165bef3b1`  
		Last Modified: Mon, 10 Mar 2025 22:15:22 GMT  
		Size: 6.6 MB (6627583 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e78baf2eda35d47a7b68ac86a644342660309a043ab11197179bc904a0d6a67b`  
		Last Modified: Mon, 10 Mar 2025 22:15:21 GMT  
		Size: 23.3 KB (23309 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:jdk8-ubi` - linux; ppc64le

```console
$ docker pull gradle@sha256:bb3d28b45bfa090e1608a70d5c3a0e93a4a894d24908a2cdf9bbe6177c61a495
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **309.3 MB (309253831 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff33d50798ac15871cd082fa6205790ca46ef259e84f38eda03b3df38413df53`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["gradle"]`

```dockerfile
# Thu, 30 Jan 2025 14:32:57 GMT
LABEL maintainer="Red Hat, Inc."
# Thu, 30 Jan 2025 14:32:57 GMT
LABEL vendor="Red Hat, Inc."
# Thu, 30 Jan 2025 14:32:57 GMT
LABEL url="https://www.redhat.com"
# Thu, 30 Jan 2025 14:32:57 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.5"       distribution-scope="public"
# Thu, 30 Jan 2025 14:32:57 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Thu, 30 Jan 2025 14:32:57 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Thu, 30 Jan 2025 14:32:57 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 30 Jan 2025 14:32:57 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 30 Jan 2025 14:32:57 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Thu, 30 Jan 2025 14:32:57 GMT
LABEL io.openshift.expose-services=""
# Thu, 30 Jan 2025 14:32:57 GMT
LABEL io.openshift.tags="minimal rhel9"
# Thu, 30 Jan 2025 14:32:57 GMT
ENV container oci
# Thu, 30 Jan 2025 14:32:57 GMT
COPY dir:da1ec7f34262056221a653ac74b71b17804f2abbdaaf0edf8f887dc2c1eeeb91 in / 
# Thu, 30 Jan 2025 14:32:57 GMT
COPY file:b37d593713ee21ad52a4cd1424dc019a24f7966f85df0ac4b86d234302695328 in /etc/yum.repos.d/. 
# Thu, 30 Jan 2025 14:32:57 GMT
CMD ["/bin/bash"]
# Thu, 30 Jan 2025 14:32:57 GMT
RUN . /cachi2/cachi2.env &&     rm -rf /var/log/*
# Thu, 30 Jan 2025 14:32:57 GMT
LABEL "build-date"="2025-03-10T09:54:50" "architecture"="ppc64le" "vcs-type"="git" "vcs-ref"="2f8e6c4d7ad22789d5663bf4bd66603301fba889" "build-date"="2025-03-10T09:43:12Z" "release"="1741599792"
# Thu, 30 Jan 2025 14:32:57 GMT
RUN /bin/sh
# Thu, 30 Jan 2025 14:32:57 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 30 Jan 2025 14:32:57 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 30 Jan 2025 14:32:57 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 30 Jan 2025 14:32:57 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         fontconfig         glibc-langpack-en     ;     microdnf clean all # buildkit
# Thu, 30 Jan 2025 14:32:57 GMT
ENV JAVA_VERSION=jdk8u442-b06
# Thu, 30 Jan 2025 14:32:57 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='1d1662bd8ca7edc9281c723d9eebafea940e6a41464bdc43a83b564bc974c7e5';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u442-b06/OpenJDK8U-jdk_aarch64_linux_hotspot_8u442b06.tar.gz';          ;;        ppc64le)          ESUM='7eac77deb8fc6c6130f9445c9a68af0bcc40bf6736b5672ef5c3d737c025e84d';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u442-b06/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u442b06.tar.gz';          ;;        x86_64)          ESUM='5b0a0145e7790552a9c8767b4680074c4628ec276e5bb278b61d85cf90facafa';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u442-b06/OpenJDK8U-jdk_x64_linux_hotspot_8u442b06.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip; # buildkit
# Thu, 30 Jan 2025 14:32:57 GMT
RUN set -eux;     echo "Verifying install ...";     echo "javac -version"; javac -version;     echo "java -version"; java -version;     echo "Complete." # buildkit
# Thu, 30 Jan 2025 14:32:57 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 30 Jan 2025 14:32:57 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 04 Mar 2025 19:20:27 GMT
CMD ["gradle"]
# Tue, 04 Mar 2025 19:20:27 GMT
ENV GRADLE_HOME=/opt/gradle
# Tue, 04 Mar 2025 19:20:27 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 101 gradle     && useradd --system --gid gradle --uid 101 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Tue, 04 Mar 2025 19:20:27 GMT
VOLUME [/home/gradle/.gradle]
# Tue, 04 Mar 2025 19:20:27 GMT
WORKDIR /home/gradle
# Tue, 04 Mar 2025 19:20:27 GMT
RUN set -o errexit -o nounset     && microdnf install -y         findutils                 unzip         wget         which                 git         git-lfs         subversion     && microdnf clean all         && echo "Testing VCSes"     && which git     && which git-lfs     && which svn # buildkit
# Tue, 04 Mar 2025 19:20:27 GMT
ENV GRADLE_VERSION=8.13
# Tue, 04 Mar 2025 19:20:27 GMT
ARG GRADLE_DOWNLOAD_SHA256=20f1b1176237254a6fc204d8434196fa11a4cfb387567519c61556e8710aed78
# Tue, 04 Mar 2025 19:20:27 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=20f1b1176237254a6fc204d8434196fa11a4cfb387567519c61556e8710aed78
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Tue, 04 Mar 2025 19:20:27 GMT
USER gradle
# Tue, 04 Mar 2025 19:20:27 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=20f1b1176237254a6fc204d8434196fa11a4cfb387567519c61556e8710aed78
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Tue, 04 Mar 2025 19:20:27 GMT
USER root
```

-	Layers:
	-	`sha256:2ad90c0e47251160a30b1b70efa8a3c13ef0ce7a213f619f4ac82370a7ac2dae`  
		Last Modified: Mon, 10 Mar 2025 12:25:37 GMT  
		Size: 43.8 MB (43784081 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4046f47b13f500df13fbbe4b00a43b66c2ff9fcbf6923a82edf7ae12f8ac46d9`  
		Last Modified: Mon, 10 Mar 2025 12:25:36 GMT  
		Size: 462.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7cac67f3417b20c312f6f519732ea676adf524a26cd705e32535b9523e7a04a8`  
		Last Modified: Mon, 10 Mar 2025 21:07:28 GMT  
		Size: 39.5 MB (39465367 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b306adf11f3bea94a668274e3946e7a63f68d078a612a59de36833acffb4362a`  
		Last Modified: Mon, 10 Mar 2025 21:07:29 GMT  
		Size: 52.2 MB (52170115 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:886ce5f57bdb94fd9ce0f689005deb7cbe3892d59edec445380be867b1e38147`  
		Last Modified: Mon, 10 Mar 2025 21:07:27 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5553bf92293f5cad432a5164da184066bafff7dcb2c7af2e993a07ab8fdb45c2`  
		Last Modified: Mon, 10 Mar 2025 21:07:28 GMT  
		Size: 2.3 KB (2316 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4641dc760cb2e75467cda4dae6314967566769c31ed4058890bb984466bdbcc`  
		Last Modified: Mon, 10 Mar 2025 22:19:38 GMT  
		Size: 1.7 KB (1700 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8d449869d2bb6a034f3383e59cc582dcbea9b72bfcfecadd7d2c8ac180e15fb`  
		Last Modified: Mon, 10 Mar 2025 22:19:40 GMT  
		Size: 36.8 MB (36806442 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2933594a7c71b364a22c2fae5a20734fb635c9ce9167438c52c38a1fe89ef3af`  
		Last Modified: Mon, 10 Mar 2025 22:19:44 GMT  
		Size: 137.0 MB (136988180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53618d208a9412f2dee7f4a131141f096a7cd25180b52888c249974a4037db3b`  
		Last Modified: Mon, 10 Mar 2025 22:19:39 GMT  
		Size: 35.0 KB (35008 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:jdk8-ubi` - unknown; unknown

```console
$ docker pull gradle@sha256:f8423a7b52809d965cbd2f7a36372a819d499093973384a1ff7b14f9934ba481
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 MB (6648592 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5cc44462257927db074d631a13e779feda85ca6f4fd4e10d9830f482dddb1002`

```dockerfile
```

-	Layers:
	-	`sha256:9ebe82e8a9db23a2154cb16729ae12bec48bec98c1f99aca45ceef8508921e74`  
		Last Modified: Mon, 10 Mar 2025 22:19:39 GMT  
		Size: 6.6 MB (6625395 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d9a79eab0c648bf28b80210d53b49f6458066a0b167fca6a4986aaaa78423676`  
		Last Modified: Mon, 10 Mar 2025 22:19:38 GMT  
		Size: 23.2 KB (23197 bytes)  
		MIME: application/vnd.in-toto+json
