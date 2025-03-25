## `gradle:8-jdk11-ubi`

```console
$ docker pull gradle@sha256:ef7c9f8178b2064f0275e69575c18a765050c637c7c44fd98b9aae760336663b
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

### `gradle:8-jdk11-ubi` - linux; amd64

```console
$ docker pull gradle@sha256:796fe63270d8d634be7c2a27a6503d74aa73f5e0efaefecf5d7da17424c94f84
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **381.4 MB (381413222 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e56dfa3660b7eee7b199c1f2bb135323aa6a335cab81a53488bc1708dbc54a62`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["gradle"]`

```dockerfile
# Tue, 04 Mar 2025 19:20:27 GMT
LABEL maintainer="Red Hat, Inc."
# Tue, 04 Mar 2025 19:20:27 GMT
LABEL vendor="Red Hat, Inc."
# Tue, 04 Mar 2025 19:20:27 GMT
LABEL url="https://www.redhat.com"
# Tue, 04 Mar 2025 19:20:27 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.5"       distribution-scope="public"
# Tue, 04 Mar 2025 19:20:27 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Tue, 04 Mar 2025 19:20:27 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Tue, 04 Mar 2025 19:20:27 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Tue, 04 Mar 2025 19:20:27 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Tue, 04 Mar 2025 19:20:27 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Tue, 04 Mar 2025 19:20:27 GMT
LABEL io.openshift.expose-services=""
# Tue, 04 Mar 2025 19:20:27 GMT
LABEL io.openshift.tags="minimal rhel9"
# Tue, 04 Mar 2025 19:20:27 GMT
ENV container oci
# Tue, 04 Mar 2025 19:20:27 GMT
COPY dir:15b23b07af120e2e0a5f4d490f44d738ca8fb631feddbf3564dd5d54104ea356 in / 
# Tue, 04 Mar 2025 19:20:27 GMT
COPY file:b37d593713ee21ad52a4cd1424dc019a24f7966f85df0ac4b86d234302695328 in /etc/yum.repos.d/. 
# Tue, 04 Mar 2025 19:20:27 GMT
CMD ["/bin/bash"]
# Tue, 04 Mar 2025 19:20:27 GMT
RUN . /cachi2/cachi2.env &&     rm -rf /var/log/*
# Tue, 04 Mar 2025 19:20:27 GMT
LABEL "build-date"="2025-03-13T07:20:00" "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="7865437f00d10c54ee1c3a6268b5ff65b38afba5" "build-date"="2025-03-13T07:15:09Z" "release"="1741850109"
# Tue, 04 Mar 2025 19:20:27 GMT
RUN /bin/sh
# Tue, 04 Mar 2025 19:20:27 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 04 Mar 2025 19:20:27 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Mar 2025 19:20:27 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 04 Mar 2025 19:20:27 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en     ;     microdnf clean all # buildkit
# Tue, 04 Mar 2025 19:20:27 GMT
ENV JAVA_VERSION=jdk-11.0.26+4
# Tue, 04 Mar 2025 19:20:27 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='e7b3d37c347fe7af2a53711f16da8b9b164748ce4a84e47bb0739c3be7f1c421';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.26%2B4/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.26_4.tar.gz';          ;;        ppc64le)          ESUM='42c63651125a149cee2ba781300d75ffa67a25032f95038d50ee6d6177cb2e41';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.26%2B4/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.26_4.tar.gz';          ;;        s390x)          ESUM='0da13d990da34ecc666399cf0efa72a4b4e295f05c0686ea25a4a173a6f4414b';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.26%2B4/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.26_4.tar.gz';          ;;        x86_64)          ESUM='7def4c5807b38ef1a7bb30a86572a795ca604127cc8d1f5b370abf23618104e6';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.26%2B4/OpenJDK11U-jdk_x64_linux_hotspot_11.0.26_4.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Tue, 04 Mar 2025 19:20:27 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 04 Mar 2025 19:20:27 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 04 Mar 2025 19:20:27 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 04 Mar 2025 19:20:27 GMT
CMD ["jshell"]
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
	-	`sha256:533b69cfd644e5f3e5bde1a8c302567c595a28af93b9318ac6a3e9394740fb4d`  
		Last Modified: Thu, 13 Mar 2025 08:27:55 GMT  
		Size: 39.4 MB (39359404 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:863e9a7e21028fb223595c360e0b25839f814e468af01725b95defa89bd29b53`  
		Last Modified: Thu, 13 Mar 2025 08:27:58 GMT  
		Size: 461.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee516c21f5d533f5a2ceaf077447a0ea8ed6fdbf85fc62c737fca01b614b21a0`  
		Last Modified: Tue, 25 Mar 2025 21:57:38 GMT  
		Size: 13.1 MB (13088173 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4095bc45b54206615d7d29cceaf798b2dbea560af1c5efdaabf6e53544527a7a`  
		Last Modified: Tue, 25 Mar 2025 21:57:40 GMT  
		Size: 142.1 MB (142058248 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d8d6f57e488c863764bf57f3d71f5213ec853b95be83a32ad6ec1d02d022eed`  
		Last Modified: Tue, 25 Mar 2025 21:57:38 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:006595098e07010b8358d4cbeda2e931671875e64492d8e60e67b8691df79e48`  
		Last Modified: Tue, 25 Mar 2025 21:57:37 GMT  
		Size: 2.3 KB (2291 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:805ebb9b513bf455aaf230e0a6437d37a2b7101585945adfe72369ad5dfd98b5`  
		Last Modified: Tue, 25 Mar 2025 22:08:14 GMT  
		Size: 1.4 KB (1419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f19723f4a94fba23ae392ee7441e9cc537fd00109e326b37cf8e55508f98f8bf`  
		Last Modified: Tue, 25 Mar 2025 22:08:16 GMT  
		Size: 49.9 MB (49859983 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76b3f46061c22033ec0088030375d54fc7f50ee1c41ab9e92022b7b627497e8b`  
		Last Modified: Tue, 25 Mar 2025 22:08:18 GMT  
		Size: 137.0 MB (136988181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64cf94405682ec8575f7a1e17d9a25593e12831e03e79146fbc31268f95cc648`  
		Last Modified: Tue, 25 Mar 2025 22:08:14 GMT  
		Size: 54.9 KB (54901 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:8-jdk11-ubi` - unknown; unknown

```console
$ docker pull gradle@sha256:0267d4e3686dd5b2b1313f23bd4e3a5a622612f28e162c3d02c7b9e2aa519329
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5341033 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5529634c6859f09663c86d2b71fde84cece640c8c9a4a96932ffcfef1959daca`

```dockerfile
```

-	Layers:
	-	`sha256:d97bc09548262b4daa821f7c638e6a2815ae2c22d0440f3f937e3e818fd391b6`  
		Last Modified: Tue, 25 Mar 2025 22:08:15 GMT  
		Size: 5.3 MB (5317217 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c682aaf40874858e571383b8b02a404b7ee57f0de0b839da1ae984a78303bbb4`  
		Last Modified: Tue, 25 Mar 2025 22:08:14 GMT  
		Size: 23.8 KB (23816 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:8-jdk11-ubi` - linux; arm64 variant v8

```console
$ docker pull gradle@sha256:daa408fbfe1b5591295a664ac60ce1ba78a0306414c6358a600f9b9ebd31211c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **376.3 MB (376335950 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:584d60e8ca904c8241512cb4ae635dd37445848c22266602e92ca5243edf4502`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["gradle"]`

```dockerfile
# Tue, 04 Mar 2025 19:20:27 GMT
LABEL maintainer="Red Hat, Inc."
# Tue, 04 Mar 2025 19:20:27 GMT
LABEL vendor="Red Hat, Inc."
# Tue, 04 Mar 2025 19:20:27 GMT
LABEL url="https://www.redhat.com"
# Tue, 04 Mar 2025 19:20:27 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.5"       distribution-scope="public"
# Tue, 04 Mar 2025 19:20:27 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Tue, 04 Mar 2025 19:20:27 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Tue, 04 Mar 2025 19:20:27 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Tue, 04 Mar 2025 19:20:27 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Tue, 04 Mar 2025 19:20:27 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Tue, 04 Mar 2025 19:20:27 GMT
LABEL io.openshift.expose-services=""
# Tue, 04 Mar 2025 19:20:27 GMT
LABEL io.openshift.tags="minimal rhel9"
# Tue, 04 Mar 2025 19:20:27 GMT
ENV container oci
# Tue, 04 Mar 2025 19:20:27 GMT
COPY dir:b7138ac36fc7710c19e28655d453b8712ae774de42fbfc7d7975b03b9664b7ae in / 
# Tue, 04 Mar 2025 19:20:27 GMT
COPY file:b37d593713ee21ad52a4cd1424dc019a24f7966f85df0ac4b86d234302695328 in /etc/yum.repos.d/. 
# Tue, 04 Mar 2025 19:20:27 GMT
CMD ["/bin/bash"]
# Tue, 04 Mar 2025 19:20:27 GMT
RUN . /cachi2/cachi2.env &&     rm -rf /var/log/*
# Tue, 04 Mar 2025 19:20:27 GMT
LABEL "build-date"="2025-03-13T07:21:58" "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="7865437f00d10c54ee1c3a6268b5ff65b38afba5" "build-date"="2025-03-13T07:15:09Z" "release"="1741850109"
# Tue, 04 Mar 2025 19:20:27 GMT
RUN /bin/sh
# Tue, 04 Mar 2025 19:20:27 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 04 Mar 2025 19:20:27 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Mar 2025 19:20:27 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 04 Mar 2025 19:20:27 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en     ;     microdnf clean all # buildkit
# Tue, 04 Mar 2025 19:20:27 GMT
ENV JAVA_VERSION=jdk-11.0.26+4
# Tue, 04 Mar 2025 19:20:27 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='e7b3d37c347fe7af2a53711f16da8b9b164748ce4a84e47bb0739c3be7f1c421';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.26%2B4/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.26_4.tar.gz';          ;;        ppc64le)          ESUM='42c63651125a149cee2ba781300d75ffa67a25032f95038d50ee6d6177cb2e41';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.26%2B4/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.26_4.tar.gz';          ;;        s390x)          ESUM='0da13d990da34ecc666399cf0efa72a4b4e295f05c0686ea25a4a173a6f4414b';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.26%2B4/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.26_4.tar.gz';          ;;        x86_64)          ESUM='7def4c5807b38ef1a7bb30a86572a795ca604127cc8d1f5b370abf23618104e6';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.26%2B4/OpenJDK11U-jdk_x64_linux_hotspot_11.0.26_4.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Tue, 04 Mar 2025 19:20:27 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 04 Mar 2025 19:20:27 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 04 Mar 2025 19:20:27 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 04 Mar 2025 19:20:27 GMT
CMD ["jshell"]
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
	-	`sha256:8f0b1160a7bdb1abc6f59217ba0a1ed1eb53a9ddbbcaddd95d709604e095f742`  
		Last Modified: Thu, 13 Mar 2025 08:37:12 GMT  
		Size: 37.6 MB (37590719 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2e019691d61a0d5163ed02fe7a0cee4161254fd2d91b44221c46f8f765e011b`  
		Last Modified: Thu, 13 Mar 2025 08:37:13 GMT  
		Size: 459.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cecaa9a0e7b9e986580faf82cb0f61b4b374585587485ca9f2f92ea54752543`  
		Last Modified: Tue, 25 Mar 2025 21:57:40 GMT  
		Size: 13.6 MB (13624229 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6978f94d4b72aa1378ba2f3f89acd8035b9ce2fe7c325a7fc0f9748766cf2b1`  
		Last Modified: Tue, 25 Mar 2025 21:58:44 GMT  
		Size: 138.8 MB (138846307 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2020a3795b23e920450994407e134022eff3fd804e2060bc487bc3a45ebda86`  
		Last Modified: Tue, 25 Mar 2025 21:58:40 GMT  
		Size: 130.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:641e6d3f0e9c4c8639d6bc0baa608750adf725641d5bbc90d2c4aeee89b4ab25`  
		Last Modified: Tue, 25 Mar 2025 21:58:40 GMT  
		Size: 2.3 KB (2292 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6327582a65ac83d097d7126295d4ee571dec211e7c559504ccdd5825c8a1cf1`  
		Last Modified: Tue, 25 Mar 2025 22:10:23 GMT  
		Size: 1.4 KB (1419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8bf6fe8b2c9bb52529e80d251c95ef204f02125d8e2c30717d078eaf21bbcba`  
		Last Modified: Tue, 25 Mar 2025 22:10:26 GMT  
		Size: 49.2 MB (49222653 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c0b4cdfb91f94f489b746c419864d1aa62b2c5c2f5506e6aab5718b2691b9db`  
		Last Modified: Tue, 25 Mar 2025 22:10:28 GMT  
		Size: 137.0 MB (136988184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f614e4203d38a24ccbc4f508c72e19885af29c429852c1b8563a89fe05cf35c5`  
		Last Modified: Tue, 25 Mar 2025 22:10:24 GMT  
		Size: 59.5 KB (59526 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:8-jdk11-ubi` - unknown; unknown

```console
$ docker pull gradle@sha256:61c13f9544b0f9e005e292fa832945b58899ca12d0abcc40a2839c0e3cd3671f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5341104 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:98185a9ac19c769628af479ba28845de82b839ea8d85028554dbb879a43ab3fe`

```dockerfile
```

-	Layers:
	-	`sha256:db32b53004a8f558f6749af00baa10ddffac1b00b7c50f367184ae971976cff3`  
		Last Modified: Tue, 25 Mar 2025 22:10:24 GMT  
		Size: 5.3 MB (5317090 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7b28e44e91b1e2e4793406b967c4a1b99e61d02f35f0108e4702ad922fbfeae6`  
		Last Modified: Tue, 25 Mar 2025 22:10:23 GMT  
		Size: 24.0 KB (24014 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:8-jdk11-ubi` - linux; ppc64le

```console
$ docker pull gradle@sha256:bf90c5002e614a20885d047efafa84adbe274efefb3b908d851d8a33ac1a0e14
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **376.8 MB (376756485 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7fa3550815ad437e28fb4e13816b1351c58564765d5113d243514d102265f26a`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["gradle"]`

```dockerfile
# Tue, 04 Mar 2025 19:20:27 GMT
LABEL maintainer="Red Hat, Inc."
# Tue, 04 Mar 2025 19:20:27 GMT
LABEL vendor="Red Hat, Inc."
# Tue, 04 Mar 2025 19:20:27 GMT
LABEL url="https://www.redhat.com"
# Tue, 04 Mar 2025 19:20:27 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.5"       distribution-scope="public"
# Tue, 04 Mar 2025 19:20:27 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Tue, 04 Mar 2025 19:20:27 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Tue, 04 Mar 2025 19:20:27 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Tue, 04 Mar 2025 19:20:27 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Tue, 04 Mar 2025 19:20:27 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Tue, 04 Mar 2025 19:20:27 GMT
LABEL io.openshift.expose-services=""
# Tue, 04 Mar 2025 19:20:27 GMT
LABEL io.openshift.tags="minimal rhel9"
# Tue, 04 Mar 2025 19:20:27 GMT
ENV container oci
# Tue, 04 Mar 2025 19:20:27 GMT
COPY dir:2930069cafd499c2bb484a4452129437fee8075431fe0148ba9db5d528b083c7 in / 
# Tue, 04 Mar 2025 19:20:27 GMT
COPY file:b37d593713ee21ad52a4cd1424dc019a24f7966f85df0ac4b86d234302695328 in /etc/yum.repos.d/. 
# Tue, 04 Mar 2025 19:20:27 GMT
CMD ["/bin/bash"]
# Tue, 04 Mar 2025 19:20:27 GMT
RUN . /cachi2/cachi2.env &&     rm -rf /var/log/*
# Tue, 04 Mar 2025 19:20:27 GMT
LABEL "build-date"="2025-03-13T07:26:37" "architecture"="ppc64le" "vcs-type"="git" "vcs-ref"="7865437f00d10c54ee1c3a6268b5ff65b38afba5" "build-date"="2025-03-13T07:15:09Z" "release"="1741850109"
# Tue, 04 Mar 2025 19:20:27 GMT
RUN /bin/sh
# Tue, 04 Mar 2025 19:20:27 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 04 Mar 2025 19:20:27 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Mar 2025 19:20:27 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 04 Mar 2025 19:20:27 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en     ;     microdnf clean all # buildkit
# Tue, 04 Mar 2025 19:20:27 GMT
ENV JAVA_VERSION=jdk-11.0.26+4
# Tue, 04 Mar 2025 19:20:27 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='e7b3d37c347fe7af2a53711f16da8b9b164748ce4a84e47bb0739c3be7f1c421';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.26%2B4/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.26_4.tar.gz';          ;;        ppc64le)          ESUM='42c63651125a149cee2ba781300d75ffa67a25032f95038d50ee6d6177cb2e41';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.26%2B4/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.26_4.tar.gz';          ;;        s390x)          ESUM='0da13d990da34ecc666399cf0efa72a4b4e295f05c0686ea25a4a173a6f4414b';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.26%2B4/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.26_4.tar.gz';          ;;        x86_64)          ESUM='7def4c5807b38ef1a7bb30a86572a795ca604127cc8d1f5b370abf23618104e6';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.26%2B4/OpenJDK11U-jdk_x64_linux_hotspot_11.0.26_4.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Tue, 04 Mar 2025 19:20:27 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 04 Mar 2025 19:20:27 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 04 Mar 2025 19:20:27 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 04 Mar 2025 19:20:27 GMT
CMD ["jshell"]
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
	-	`sha256:45bd43bfc7accd96f346d44555dfd3c49fe61e223a5edc723f7e6e800686210b`  
		Last Modified: Thu, 13 Mar 2025 12:28:04 GMT  
		Size: 43.8 MB (43765030 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8dd5893f1906dca44bb5215e6c9cec6ab4d26c1be7354e08d4a40339ea1bd0ad`  
		Last Modified: Thu, 13 Mar 2025 12:28:03 GMT  
		Size: 459.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:914af573e0553dbd0d38d7286a66c85ce9c38d0316f769a5f0399abff06eab9e`  
		Last Modified: Tue, 25 Mar 2025 21:58:18 GMT  
		Size: 14.7 MB (14724882 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7de2b2b6b6284905383c04f687ac4db47913193aaaee6e05551bb939a50f657d`  
		Last Modified: Tue, 25 Mar 2025 22:00:35 GMT  
		Size: 129.3 MB (129289595 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3374ea28419f99c084e4e407ffa5e1e403fc41243e778897cf8619b9a5d1912`  
		Last Modified: Tue, 25 Mar 2025 22:00:31 GMT  
		Size: 131.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a308b07640018e2c42050aa5a07cbfad3a99cdb29a70de63414802a80f9f3a94`  
		Last Modified: Tue, 25 Mar 2025 22:00:31 GMT  
		Size: 2.3 KB (2290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b8cef4b03215b2462ba18c201ae6e63b0a6dab2519e1b6c035f3ad5192308c4`  
		Last Modified: Tue, 25 Mar 2025 22:16:54 GMT  
		Size: 1.4 KB (1423 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eaa9c9d42e7aa2a56de676fb4471250cf5b51ff6ce80834f1de59dd1d2496545`  
		Last Modified: Tue, 25 Mar 2025 22:16:57 GMT  
		Size: 51.9 MB (51949450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:858953a070b6683eb1793f604497e164f1f5c09945c698b55f8b5076ad574d2d`  
		Last Modified: Tue, 25 Mar 2025 22:17:01 GMT  
		Size: 137.0 MB (136988186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e9c7c477356ea8614a44c623632ac6c0581dabcc55537ab3306548873a659e0`  
		Last Modified: Tue, 25 Mar 2025 22:16:55 GMT  
		Size: 35.0 KB (35007 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:8-jdk11-ubi` - unknown; unknown

```console
$ docker pull gradle@sha256:247005f4ef7750b62cb7d48eebb7675a10707270d68ee4e188232a120e2cead8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5337653 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:84d8e3adef1ef31b1f87b0dbf0de3e7c45a7441648593e7b08f403f805998d1b`

```dockerfile
```

-	Layers:
	-	`sha256:fcd25184ce42e0985830389523e1c7c6bf8496fbc0a3ebbe36c84efc27a71d13`  
		Last Modified: Tue, 25 Mar 2025 22:16:55 GMT  
		Size: 5.3 MB (5313762 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b462c6072fca3bc9e81e4d886d01a7f8150d6b203f51492feeb771334c46ce95`  
		Last Modified: Tue, 25 Mar 2025 22:16:54 GMT  
		Size: 23.9 KB (23891 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:8-jdk11-ubi` - linux; s390x

```console
$ docker pull gradle@sha256:32a949e70fcde09f431581397b18694f4a9799e25640cd603887bf61bb4832cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **359.1 MB (359136846 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:57fc2c1ccd7ca54da5ed1ac9da0d3795f7ab012c5875172682d47a7f43e12ae1`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["gradle"]`

```dockerfile
# Tue, 04 Mar 2025 19:20:27 GMT
LABEL maintainer="Red Hat, Inc."
# Tue, 04 Mar 2025 19:20:27 GMT
LABEL vendor="Red Hat, Inc."
# Tue, 04 Mar 2025 19:20:27 GMT
LABEL url="https://www.redhat.com"
# Tue, 04 Mar 2025 19:20:27 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.5"       distribution-scope="public"
# Tue, 04 Mar 2025 19:20:27 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Tue, 04 Mar 2025 19:20:27 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Tue, 04 Mar 2025 19:20:27 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Tue, 04 Mar 2025 19:20:27 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Tue, 04 Mar 2025 19:20:27 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Tue, 04 Mar 2025 19:20:27 GMT
LABEL io.openshift.expose-services=""
# Tue, 04 Mar 2025 19:20:27 GMT
LABEL io.openshift.tags="minimal rhel9"
# Tue, 04 Mar 2025 19:20:27 GMT
ENV container oci
# Tue, 04 Mar 2025 19:20:27 GMT
COPY dir:0bd2f8345c36703c483db0ee0404e33109a312f452aed24ac4080629e2197763 in / 
# Tue, 04 Mar 2025 19:20:27 GMT
COPY file:b37d593713ee21ad52a4cd1424dc019a24f7966f85df0ac4b86d234302695328 in /etc/yum.repos.d/. 
# Tue, 04 Mar 2025 19:20:27 GMT
CMD ["/bin/bash"]
# Tue, 04 Mar 2025 19:20:27 GMT
RUN . /cachi2/cachi2.env &&     rm -rf /var/log/*
# Tue, 04 Mar 2025 19:20:27 GMT
LABEL "build-date"="2025-03-13T07:25:32" "architecture"="s390x" "vcs-type"="git" "vcs-ref"="7865437f00d10c54ee1c3a6268b5ff65b38afba5" "build-date"="2025-03-13T07:15:09Z" "release"="1741850109"
# Tue, 04 Mar 2025 19:20:27 GMT
RUN /bin/sh
# Tue, 04 Mar 2025 19:20:27 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 04 Mar 2025 19:20:27 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Mar 2025 19:20:27 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 04 Mar 2025 19:20:27 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en     ;     microdnf clean all # buildkit
# Tue, 04 Mar 2025 19:20:27 GMT
ENV JAVA_VERSION=jdk-11.0.26+4
# Tue, 04 Mar 2025 19:20:27 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='e7b3d37c347fe7af2a53711f16da8b9b164748ce4a84e47bb0739c3be7f1c421';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.26%2B4/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.26_4.tar.gz';          ;;        ppc64le)          ESUM='42c63651125a149cee2ba781300d75ffa67a25032f95038d50ee6d6177cb2e41';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.26%2B4/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.26_4.tar.gz';          ;;        s390x)          ESUM='0da13d990da34ecc666399cf0efa72a4b4e295f05c0686ea25a4a173a6f4414b';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.26%2B4/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.26_4.tar.gz';          ;;        x86_64)          ESUM='7def4c5807b38ef1a7bb30a86572a795ca604127cc8d1f5b370abf23618104e6';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.26%2B4/OpenJDK11U-jdk_x64_linux_hotspot_11.0.26_4.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Tue, 04 Mar 2025 19:20:27 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 04 Mar 2025 19:20:27 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 04 Mar 2025 19:20:27 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 04 Mar 2025 19:20:27 GMT
CMD ["jshell"]
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
	-	`sha256:5c803ecc47a0d9d9d66bd6164bdefc7148562b976f8369af7f3ec1cc62c37cca`  
		Last Modified: Thu, 13 Mar 2025 12:27:57 GMT  
		Size: 37.5 MB (37504197 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:094529012ae62f39a61b16721406ec6b3762288ce40141f72e6917263ab122de`  
		Last Modified: Thu, 13 Mar 2025 12:27:56 GMT  
		Size: 458.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3eb8106808808f1d5a5b735787511265d305fd4624296a16f2d1eb222401d55a`  
		Last Modified: Tue, 25 Mar 2025 21:57:55 GMT  
		Size: 13.4 MB (13446471 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f49b92a2490847040e4398532a3b51127798d8c204ebda0b1d6278cdbfb78ec4`  
		Last Modified: Tue, 25 Mar 2025 21:57:57 GMT  
		Size: 122.0 MB (121978359 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52aa53e42dc85af196835b73904870a796f4d5c27e8ac0237aa784d89bd16eee`  
		Last Modified: Tue, 25 Mar 2025 21:57:52 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d7d34ccb3a7b7128b2da8ad8de234035907fa02d017882b5f85d161332bdcbd`  
		Last Modified: Tue, 25 Mar 2025 21:57:55 GMT  
		Size: 2.3 KB (2291 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55f4be6aca7ce64c9f0531561f2a90606e4d9fa9512b2a0355c61ef05b667c3f`  
		Last Modified: Tue, 25 Mar 2025 22:11:51 GMT  
		Size: 1.4 KB (1419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:168bbf6c7c8755e51b711620776d17b997f542f9f9c7cebcc565e7d268c48db6`  
		Last Modified: Tue, 25 Mar 2025 22:11:55 GMT  
		Size: 49.2 MB (49180296 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04277f3b357f17d7bcc0325797ff236d1d2f0504a1cf7d17c53007abb207a86c`  
		Last Modified: Tue, 25 Mar 2025 22:11:55 GMT  
		Size: 137.0 MB (136988184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:010ea810ebae8020e75b986630f0b1d1baa640a831fff2d1598005408107911f`  
		Last Modified: Tue, 25 Mar 2025 22:11:52 GMT  
		Size: 35.0 KB (35010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:8-jdk11-ubi` - unknown; unknown

```console
$ docker pull gradle@sha256:a714be4f44b906d3fd23c755d939357d445e679438b7c4b7cdf751fccd78373e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5327467 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b2e65058fba6c2406ce4b1a9435952f5aea1e9106a4491b5f65a5fa47d55612b`

```dockerfile
```

-	Layers:
	-	`sha256:e24220b13bedec8998c5b7fa48836c1fb77580759dfe84a5b7686b8faa9ae644`  
		Last Modified: Tue, 25 Mar 2025 22:11:52 GMT  
		Size: 5.3 MB (5303651 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:320baedf21783e6014e943adf63e2c9bf43f333a56bec23b2bf8f9e78129416e`  
		Last Modified: Tue, 25 Mar 2025 22:11:51 GMT  
		Size: 23.8 KB (23816 bytes)  
		MIME: application/vnd.in-toto+json
