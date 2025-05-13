## `gradle:8-jdk8-ubi-minimal`

```console
$ docker pull gradle@sha256:942f9dbe93d1bc5f4bddf052ac0b7cbcf4f9ff42ad0c0403bc58c0b07816d58c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `gradle:8-jdk8-ubi-minimal` - linux; amd64

```console
$ docker pull gradle@sha256:f55e95b8311fd38752155075ef5af9553da10345d479d429273aa868ae80c063
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **299.9 MB (299876656 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2ba0b6d3fd13cf6729782cae0ffc5b25d89c494e3e20c575654b41616f69b18b`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["gradle"]`

```dockerfile
# Sat, 26 Apr 2025 01:26:29 GMT
LABEL maintainer="Red Hat, Inc."
# Sat, 26 Apr 2025 01:26:29 GMT
LABEL vendor="Red Hat, Inc."
# Sat, 26 Apr 2025 01:26:29 GMT
LABEL url="https://www.redhat.com"
# Sat, 26 Apr 2025 01:26:29 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.5"       distribution-scope="public"
# Sat, 26 Apr 2025 01:26:29 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Sat, 26 Apr 2025 01:26:29 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Sat, 26 Apr 2025 01:26:29 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Sat, 26 Apr 2025 01:26:29 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Sat, 26 Apr 2025 01:26:29 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Sat, 26 Apr 2025 01:26:29 GMT
LABEL io.openshift.expose-services=""
# Sat, 26 Apr 2025 01:26:29 GMT
LABEL io.openshift.tags="minimal rhel9"
# Sat, 26 Apr 2025 01:26:29 GMT
ENV container oci
# Sat, 26 Apr 2025 01:26:29 GMT
COPY dir:2dc25289c3b10f6fae681d085452474bf4d133d8f435510e0e9aa64114b861ab in / 
# Sat, 26 Apr 2025 01:26:29 GMT
COPY file:b37d593713ee21ad52a4cd1424dc019a24f7966f85df0ac4b86d234302695328 in /etc/yum.repos.d/. 
# Sat, 26 Apr 2025 01:26:29 GMT
CMD ["/bin/bash"]
# Sat, 26 Apr 2025 01:26:29 GMT
RUN . /cachi2/cachi2.env &&     rm -rf /var/log/*
# Sat, 26 Apr 2025 01:26:29 GMT
COPY file:58cc94f5b3b2d60de2c77a6ed4b1797dcede502ccdb429a72e7a72d994235b3c in /usr/share/buildinfo/content-sets.json 
# Sat, 26 Apr 2025 01:26:29 GMT
LABEL "build-date"="2025-05-13T04:42:10" "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="7575d7eb45eb7f545fef31ba067dfe3d8e52c4eb" "release"="1747111267"
# Sat, 26 Apr 2025 01:26:29 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 26 Apr 2025 01:26:29 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 26 Apr 2025 01:26:29 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Sat, 26 Apr 2025 01:26:29 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en     ;     microdnf clean all # buildkit
# Sat, 26 Apr 2025 01:26:29 GMT
ENV JAVA_VERSION=jdk8u452-b09
# Sat, 26 Apr 2025 01:26:29 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='d8a1aecea0913b7a1e0d737ba6f7ea99059b3f6fd17813d4a24e8b3fc3aee278';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u452-b09/OpenJDK8U-jdk_aarch64_linux_hotspot_8u452b09.tar.gz';          ;;        ppc64le)          ESUM='ff6e0f7fad0f46fea47193b95e4187e294ba69bb9059704f5df9f2fb74125732';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u452-b09/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u452b09.tar.gz';          ;;        x86_64)          ESUM='9448308a21841960a591b47927cf2d44fdc4c0533a5f8111a4b243a6bafb5d27';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u452-b09/OpenJDK8U-jdk_x64_linux_hotspot_8u452b09.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip; # buildkit
# Sat, 26 Apr 2025 01:26:29 GMT
RUN set -eux;     echo "Verifying install ...";     echo "javac -version"; javac -version;     echo "java -version"; java -version;     echo "Complete." # buildkit
# Sat, 26 Apr 2025 01:26:29 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Sat, 26 Apr 2025 01:26:29 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Sat, 26 Apr 2025 01:26:29 GMT
CMD ["gradle"]
# Sat, 26 Apr 2025 01:26:29 GMT
ENV GRADLE_HOME=/opt/gradle
# Sat, 26 Apr 2025 01:26:29 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 101 gradle     && useradd --system --gid gradle --uid 101 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Sat, 26 Apr 2025 01:26:29 GMT
VOLUME [/home/gradle/.gradle]
# Sat, 26 Apr 2025 01:26:29 GMT
WORKDIR /home/gradle
# Sat, 26 Apr 2025 01:26:29 GMT
RUN set -o errexit -o nounset     && microdnf install -y         findutils                 unzip         wget         which                 git         git-lfs         subversion     && microdnf clean all         && echo "Testing VCSes"     && which git     && which git-lfs     && which svn # buildkit
# Sat, 26 Apr 2025 01:26:29 GMT
ENV GRADLE_VERSION=8.14
# Sat, 26 Apr 2025 01:26:29 GMT
ARG GRADLE_DOWNLOAD_SHA256=61ad310d3c7d3e5da131b76bbf22b5a4c0786e9d892dae8c1658d4b484de3caa
# Sat, 26 Apr 2025 01:26:29 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=61ad310d3c7d3e5da131b76bbf22b5a4c0786e9d892dae8c1658d4b484de3caa
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Sat, 26 Apr 2025 01:26:29 GMT
USER gradle
# Sat, 26 Apr 2025 01:26:29 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=61ad310d3c7d3e5da131b76bbf22b5a4c0786e9d892dae8c1658d4b484de3caa
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Sat, 26 Apr 2025 01:26:29 GMT
USER root
```

-	Layers:
	-	`sha256:719fed365262e942a8d13a9f7c6f9e87e6274c4e3ad3d0efc81666b12229084d`  
		Last Modified: Tue, 13 May 2025 05:25:18 GMT  
		Size: 39.7 MB (39714170 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74b89d2017cda6f592a4b400b92f7b76bda841f22aa7f97a2cdfd1cc5eccd423`  
		Last Modified: Tue, 13 May 2025 19:54:13 GMT  
		Size: 16.6 MB (16610229 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ab2f64bccee888f093cc3873031af96886467c7c92aaccb302763e037d72ca7`  
		Last Modified: Tue, 13 May 2025 19:54:14 GMT  
		Size: 54.7 MB (54716740 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba2ff67dc2a42ffb14ace164ffed798c3e2db9808ad20eb49470be92be7c77a6`  
		Last Modified: Tue, 13 May 2025 19:54:11 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a1fc948140fec03ba6cdd141fc6594e0d96f2f4780c1d59f47b95634595a9d2`  
		Last Modified: Tue, 13 May 2025 19:54:13 GMT  
		Size: 2.3 KB (2314 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52dd0dd7188e79c1ba93fe2e88f7bd906b44160ceb2f9f040fc7bddc50fbb29c`  
		Last Modified: Tue, 13 May 2025 19:58:05 GMT  
		Size: 1.4 KB (1416 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3e48fc950b296b0ac5f81c83c8b10abf9ef6c64c0cbd90e1efd368f16e5e9f1`  
		Last Modified: Tue, 13 May 2025 19:58:06 GMT  
		Size: 51.4 MB (51382181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7fdce4a266b92288aabf01b6b00e0176e6a33c5182e68161d3a1fb617db65d70`  
		Last Modified: Tue, 13 May 2025 19:58:07 GMT  
		Size: 137.4 MB (137394550 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b07522efbf34e86a25e34626e2a792e97afb3f9035f96e4512e5a5d40aadc8c6`  
		Last Modified: Tue, 13 May 2025 19:58:05 GMT  
		Size: 54.9 KB (54897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:8-jdk8-ubi-minimal` - unknown; unknown

```console
$ docker pull gradle@sha256:e391a8e2c7f1caed5e4bce371711ebfa4b0658815262e4c9e5e2936dad156e17
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5473035 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:52db8e175cdc0eb9584ba451419d33c82158d66d9234e3a33ab87a1f53057676`

```dockerfile
```

-	Layers:
	-	`sha256:59c8920d06d1b616482cf360d63be960d5dc7fc776146755241bd669cafe5a82`  
		Last Modified: Tue, 13 May 2025 19:58:05 GMT  
		Size: 5.5 MB (5450176 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1b0217e0e8d1fe5540066e8a4adcc8109248bb3db587d676b237e2a7f8ae2cd8`  
		Last Modified: Tue, 13 May 2025 19:58:05 GMT  
		Size: 22.9 KB (22859 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:8-jdk8-ubi-minimal` - linux; arm64 variant v8

```console
$ docker pull gradle@sha256:ad8c05d9fb5c92a4819b231a1108f01ac065f990a04dbf46ad7c05d09b3d9f53
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **292.0 MB (291981013 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e2c8ed2ddbc6b691bb9d83609d142a59b5b2cfd8ce9ab7eff494571b3faa364`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["gradle"]`

```dockerfile
# Sat, 26 Apr 2025 01:26:29 GMT
LABEL maintainer="Red Hat, Inc."
# Sat, 26 Apr 2025 01:26:29 GMT
LABEL vendor="Red Hat, Inc."
# Sat, 26 Apr 2025 01:26:29 GMT
LABEL url="https://www.redhat.com"
# Sat, 26 Apr 2025 01:26:29 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.5"       distribution-scope="public"
# Sat, 26 Apr 2025 01:26:29 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Sat, 26 Apr 2025 01:26:29 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Sat, 26 Apr 2025 01:26:29 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Sat, 26 Apr 2025 01:26:29 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Sat, 26 Apr 2025 01:26:29 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Sat, 26 Apr 2025 01:26:29 GMT
LABEL io.openshift.expose-services=""
# Sat, 26 Apr 2025 01:26:29 GMT
LABEL io.openshift.tags="minimal rhel9"
# Sat, 26 Apr 2025 01:26:29 GMT
ENV container oci
# Sat, 26 Apr 2025 01:26:29 GMT
COPY dir:37e2781211ed66b85e838f75f63c4036aeedc358075b7ac677bbe4ad43998692 in / 
# Sat, 26 Apr 2025 01:26:29 GMT
COPY file:b37d593713ee21ad52a4cd1424dc019a24f7966f85df0ac4b86d234302695328 in /etc/yum.repos.d/. 
# Sat, 26 Apr 2025 01:26:29 GMT
CMD ["/bin/bash"]
# Sat, 26 Apr 2025 01:26:29 GMT
RUN . /cachi2/cachi2.env &&     rm -rf /var/log/*
# Sat, 26 Apr 2025 01:26:29 GMT
COPY file:0667e9d31385a24c3aef13f2dd9ab6a7b71b3dfcfef5127d3c1e2ea2c838e5cb in /usr/share/buildinfo/content-sets.json 
# Sat, 26 Apr 2025 01:26:29 GMT
LABEL "build-date"="2025-04-28T15:48:27" "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="f072486a5ead2d7d882ba4af2ce72e19cce20791" "release"="1745855087"
# Sat, 26 Apr 2025 01:26:29 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 26 Apr 2025 01:26:29 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 26 Apr 2025 01:26:29 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Sat, 26 Apr 2025 01:26:29 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en     ;     microdnf clean all # buildkit
# Sat, 26 Apr 2025 01:26:29 GMT
ENV JAVA_VERSION=jdk8u452-b09
# Sat, 26 Apr 2025 01:26:29 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='d8a1aecea0913b7a1e0d737ba6f7ea99059b3f6fd17813d4a24e8b3fc3aee278';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u452-b09/OpenJDK8U-jdk_aarch64_linux_hotspot_8u452b09.tar.gz';          ;;        ppc64le)          ESUM='ff6e0f7fad0f46fea47193b95e4187e294ba69bb9059704f5df9f2fb74125732';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u452-b09/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u452b09.tar.gz';          ;;        x86_64)          ESUM='9448308a21841960a591b47927cf2d44fdc4c0533a5f8111a4b243a6bafb5d27';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u452-b09/OpenJDK8U-jdk_x64_linux_hotspot_8u452b09.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip; # buildkit
# Sat, 26 Apr 2025 01:26:29 GMT
RUN set -eux;     echo "Verifying install ...";     echo "javac -version"; javac -version;     echo "java -version"; java -version;     echo "Complete." # buildkit
# Sat, 26 Apr 2025 01:26:29 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Sat, 26 Apr 2025 01:26:29 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Sat, 26 Apr 2025 01:26:29 GMT
CMD ["gradle"]
# Sat, 26 Apr 2025 01:26:29 GMT
ENV GRADLE_HOME=/opt/gradle
# Sat, 26 Apr 2025 01:26:29 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 101 gradle     && useradd --system --gid gradle --uid 101 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Sat, 26 Apr 2025 01:26:29 GMT
VOLUME [/home/gradle/.gradle]
# Sat, 26 Apr 2025 01:26:29 GMT
WORKDIR /home/gradle
# Sat, 26 Apr 2025 01:26:29 GMT
RUN set -o errexit -o nounset     && microdnf install -y         findutils                 unzip         wget         which                 git         git-lfs         subversion     && microdnf clean all         && echo "Testing VCSes"     && which git     && which git-lfs     && which svn # buildkit
# Sat, 26 Apr 2025 01:26:29 GMT
ENV GRADLE_VERSION=8.14
# Sat, 26 Apr 2025 01:26:29 GMT
ARG GRADLE_DOWNLOAD_SHA256=61ad310d3c7d3e5da131b76bbf22b5a4c0786e9d892dae8c1658d4b484de3caa
# Sat, 26 Apr 2025 01:26:29 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=61ad310d3c7d3e5da131b76bbf22b5a4c0786e9d892dae8c1658d4b484de3caa
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Sat, 26 Apr 2025 01:26:29 GMT
USER gradle
# Sat, 26 Apr 2025 01:26:29 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=61ad310d3c7d3e5da131b76bbf22b5a4c0786e9d892dae8c1658d4b484de3caa
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Sat, 26 Apr 2025 01:26:29 GMT
USER root
```

-	Layers:
	-	`sha256:2aa6bd15812764b98217de512ddcd6b7fc8cb96437e1fa30d7963118dce559ff`  
		Last Modified: Mon, 28 Apr 2025 16:55:35 GMT  
		Size: 37.9 MB (37887470 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24ce9f57aa1d6908dcd943f34d1cb9f35acee0f7b2adadaef31267686265fc09`  
		Last Modified: Tue, 29 Apr 2025 17:51:14 GMT  
		Size: 28.0 MB (27986783 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acb2971cd3cd729a4be656648a347756b38a9b67e6a29aaee0bb77dc97e921b5`  
		Last Modified: Tue, 29 Apr 2025 17:51:14 GMT  
		Size: 53.8 MB (53831016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5cd6c7c9d8bd1e58d3be55495df287f20006033cabadbf7a2ad30bc3ee4b6ca`  
		Last Modified: Tue, 29 Apr 2025 17:51:12 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:092abc1a5b2979bf89c9e0f3368b570bf063e4600d7d2a506f5a2c2a794785db`  
		Last Modified: Tue, 29 Apr 2025 17:51:13 GMT  
		Size: 2.3 KB (2314 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b54a720d4e53c09fd385062ab86964e738da97a4d1c3e5069cfe455ea3376ad5`  
		Last Modified: Wed, 30 Apr 2025 02:39:40 GMT  
		Size: 1.7 KB (1706 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12a7a33811f6a5b65cd21c538345e2be280272da842e63c71bf6917b0f82204c`  
		Last Modified: Wed, 30 Apr 2025 02:39:41 GMT  
		Size: 34.8 MB (34817486 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5b56c107693991eb0e54d7e190dae83d41a0c73ad7da77b3ef3383d2e823529`  
		Last Modified: Wed, 30 Apr 2025 02:39:44 GMT  
		Size: 137.4 MB (137394552 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9adabfb02169c0c5691651f16e38170c412f683c2c9165bb327c07eda268ff6a`  
		Last Modified: Wed, 30 Apr 2025 02:39:40 GMT  
		Size: 59.5 KB (59528 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:8-jdk8-ubi-minimal` - unknown; unknown

```console
$ docker pull gradle@sha256:cbc7f238deca70aa5213e10ce7887d26688340d37199eb5ea5f6b95da3ae179d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5444569 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c05c6d05fa62b90bd890cc5a1410c97f89ad73a5e671e14d1bf9e0cc2be48c2c`

```dockerfile
```

-	Layers:
	-	`sha256:c8c8098794f2996c18ea102ef8fd3545222db5505855d3f8f0e806132e520fa5`  
		Last Modified: Wed, 30 Apr 2025 02:39:40 GMT  
		Size: 5.4 MB (5421513 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6c78c2789b698b8d55b2a8ffad125907ef07aa4eee461942f46841cbff338412`  
		Last Modified: Wed, 30 Apr 2025 02:39:40 GMT  
		Size: 23.1 KB (23056 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:8-jdk8-ubi-minimal` - linux; ppc64le

```console
$ docker pull gradle@sha256:b15200471627f2f5ada289ef18f8aed7c1482fb41a05485af1be268ddc75f6cf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **300.2 MB (300198491 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:08e44918defc71296ae885d3543031b0cd2802f8124016f0e05cf6f6670df195`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["gradle"]`

```dockerfile
# Sat, 26 Apr 2025 01:26:29 GMT
LABEL maintainer="Red Hat, Inc."
# Sat, 26 Apr 2025 01:26:29 GMT
LABEL vendor="Red Hat, Inc."
# Sat, 26 Apr 2025 01:26:29 GMT
LABEL url="https://www.redhat.com"
# Sat, 26 Apr 2025 01:26:29 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.5"       distribution-scope="public"
# Sat, 26 Apr 2025 01:26:29 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Sat, 26 Apr 2025 01:26:29 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Sat, 26 Apr 2025 01:26:29 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Sat, 26 Apr 2025 01:26:29 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Sat, 26 Apr 2025 01:26:29 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Sat, 26 Apr 2025 01:26:29 GMT
LABEL io.openshift.expose-services=""
# Sat, 26 Apr 2025 01:26:29 GMT
LABEL io.openshift.tags="minimal rhel9"
# Sat, 26 Apr 2025 01:26:29 GMT
ENV container oci
# Sat, 26 Apr 2025 01:26:29 GMT
COPY dir:352b288c8223eaef7c671c611c93e11c1f1a08ec40f3f05f199babc323ce9c37 in / 
# Sat, 26 Apr 2025 01:26:29 GMT
COPY file:b37d593713ee21ad52a4cd1424dc019a24f7966f85df0ac4b86d234302695328 in /etc/yum.repos.d/. 
# Sat, 26 Apr 2025 01:26:29 GMT
CMD ["/bin/bash"]
# Sat, 26 Apr 2025 01:26:29 GMT
RUN . /cachi2/cachi2.env &&     rm -rf /var/log/*
# Sat, 26 Apr 2025 01:26:29 GMT
COPY file:0667e9d31385a24c3aef13f2dd9ab6a7b71b3dfcfef5127d3c1e2ea2c838e5cb in /usr/share/buildinfo/content-sets.json 
# Sat, 26 Apr 2025 01:26:29 GMT
LABEL "build-date"="2025-04-28T15:57:47" "architecture"="ppc64le" "vcs-type"="git" "vcs-ref"="f072486a5ead2d7d882ba4af2ce72e19cce20791" "release"="1745855087"
# Sat, 26 Apr 2025 01:26:29 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 26 Apr 2025 01:26:29 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 26 Apr 2025 01:26:29 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Sat, 26 Apr 2025 01:26:29 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en     ;     microdnf clean all # buildkit
# Sat, 26 Apr 2025 01:26:29 GMT
ENV JAVA_VERSION=jdk8u452-b09
# Sat, 26 Apr 2025 01:26:29 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='d8a1aecea0913b7a1e0d737ba6f7ea99059b3f6fd17813d4a24e8b3fc3aee278';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u452-b09/OpenJDK8U-jdk_aarch64_linux_hotspot_8u452b09.tar.gz';          ;;        ppc64le)          ESUM='ff6e0f7fad0f46fea47193b95e4187e294ba69bb9059704f5df9f2fb74125732';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u452-b09/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u452b09.tar.gz';          ;;        x86_64)          ESUM='9448308a21841960a591b47927cf2d44fdc4c0533a5f8111a4b243a6bafb5d27';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u452-b09/OpenJDK8U-jdk_x64_linux_hotspot_8u452b09.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip; # buildkit
# Sat, 26 Apr 2025 01:26:29 GMT
RUN set -eux;     echo "Verifying install ...";     echo "javac -version"; javac -version;     echo "java -version"; java -version;     echo "Complete." # buildkit
# Sat, 26 Apr 2025 01:26:29 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Sat, 26 Apr 2025 01:26:29 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Sat, 26 Apr 2025 01:26:29 GMT
CMD ["gradle"]
# Sat, 26 Apr 2025 01:26:29 GMT
ENV GRADLE_HOME=/opt/gradle
# Sat, 26 Apr 2025 01:26:29 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 101 gradle     && useradd --system --gid gradle --uid 101 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Sat, 26 Apr 2025 01:26:29 GMT
VOLUME [/home/gradle/.gradle]
# Sat, 26 Apr 2025 01:26:29 GMT
WORKDIR /home/gradle
# Sat, 26 Apr 2025 01:26:29 GMT
RUN set -o errexit -o nounset     && microdnf install -y         findutils                 unzip         wget         which                 git         git-lfs         subversion     && microdnf clean all         && echo "Testing VCSes"     && which git     && which git-lfs     && which svn # buildkit
# Sat, 26 Apr 2025 01:26:29 GMT
ENV GRADLE_VERSION=8.14
# Sat, 26 Apr 2025 01:26:29 GMT
ARG GRADLE_DOWNLOAD_SHA256=61ad310d3c7d3e5da131b76bbf22b5a4c0786e9d892dae8c1658d4b484de3caa
# Sat, 26 Apr 2025 01:26:29 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=61ad310d3c7d3e5da131b76bbf22b5a4c0786e9d892dae8c1658d4b484de3caa
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Sat, 26 Apr 2025 01:26:29 GMT
USER gradle
# Sat, 26 Apr 2025 01:26:29 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=61ad310d3c7d3e5da131b76bbf22b5a4c0786e9d892dae8c1658d4b484de3caa
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Sat, 26 Apr 2025 01:26:29 GMT
USER root
```

-	Layers:
	-	`sha256:e32416660495649b2ba0129e756351f46ec1023f3bc9594febaf780fbab240ec`  
		Last Modified: Mon, 28 Apr 2025 18:29:40 GMT  
		Size: 44.1 MB (44107495 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6996b2f2feb522ede46945b0975b09aeb2bfb6324b3f69796498cf5a57bfc426`  
		Last Modified: Tue, 29 Apr 2025 18:41:13 GMT  
		Size: 30.0 MB (29966503 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16eb37f71745f573a9e73982fb3a92f48e6e8979ebb074b35ec8bb96f263ba56`  
		Last Modified: Tue, 29 Apr 2025 18:41:13 GMT  
		Size: 52.2 MB (52168556 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66a493b90ec5d6d9bde43053caadd1bf0c8e1b0c38269331c496612f0dc21b19`  
		Last Modified: Tue, 29 Apr 2025 18:41:11 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccebdb419bba02a39c4f4c69a59926d4c64d013ecae394cad722487d9db70fee`  
		Last Modified: Tue, 29 Apr 2025 18:41:12 GMT  
		Size: 2.3 KB (2314 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38473a71d51c2b282f21b7f831b370e4cdfc331d13106ce5bcabf83de1511219`  
		Last Modified: Tue, 29 Apr 2025 19:34:13 GMT  
		Size: 1.7 KB (1708 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a3d230dbae09ed714d2080d4d85e8ba2d1439cd753c97c5c82a588d47153f3f`  
		Last Modified: Tue, 29 Apr 2025 19:34:15 GMT  
		Size: 36.5 MB (36522192 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f974ff5d205c1f039cb57e12caba7137385cb6ef7f5f031ccd1a119ee1d9d48`  
		Last Modified: Tue, 29 Apr 2025 19:34:24 GMT  
		Size: 137.4 MB (137394557 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:893c6a72ed9a6f92a0d464aae55a75c26d56cdb222838d931872f5023fe60dad`  
		Last Modified: Tue, 29 Apr 2025 19:34:13 GMT  
		Size: 35.0 KB (35007 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:8-jdk8-ubi-minimal` - unknown; unknown

```console
$ docker pull gradle@sha256:911c5ac65ea22d4ae214bb3486cee46ceaec3ed54cf5a382137ac5409872e500
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5442247 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b98bd1c5da20057096ca3c8a2b5baf0ffe2bef19c323d71d9675f12b9bb14884`

```dockerfile
```

-	Layers:
	-	`sha256:c373f24e04a8c006a207772febc570c4599481249d0549d385a88df9c0b74e3b`  
		Last Modified: Tue, 29 Apr 2025 19:34:13 GMT  
		Size: 5.4 MB (5419313 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:92f52fadf3584ed2586f3cef0f25ff1419b67a82b4d824f58e89bc1c2dd7404c`  
		Last Modified: Tue, 29 Apr 2025 19:34:12 GMT  
		Size: 22.9 KB (22934 bytes)  
		MIME: application/vnd.in-toto+json
