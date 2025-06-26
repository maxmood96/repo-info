## `gradle:8-jdk8-ubi`

```console
$ docker pull gradle@sha256:d6a24d3c13908f4ad303338b2410edf317624f19e9b40e78f052361366169899
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
$ docker pull gradle@sha256:82840922a541b47b8ac6a7da5a58243460b9477e5fc2e7966637f18d6a192293
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **296.2 MB (296164885 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a9615e63b4d71a11711fbef549f446ff8b40dd9a74e5d69ee6a92497e40d7432`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["gradle"]`

```dockerfile
# Sun, 27 Apr 2025 20:21:59 GMT
LABEL maintainer="Red Hat, Inc."
# Sun, 27 Apr 2025 20:21:59 GMT
LABEL vendor="Red Hat, Inc."
# Sun, 27 Apr 2025 20:21:59 GMT
LABEL url="https://www.redhat.com"
# Sun, 27 Apr 2025 20:21:59 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.6"       distribution-scope="public"
# Sun, 27 Apr 2025 20:21:59 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Sun, 27 Apr 2025 20:21:59 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Sun, 27 Apr 2025 20:21:59 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Sun, 27 Apr 2025 20:21:59 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Sun, 27 Apr 2025 20:21:59 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Sun, 27 Apr 2025 20:21:59 GMT
LABEL io.openshift.expose-services=""
# Sun, 27 Apr 2025 20:21:59 GMT
LABEL io.openshift.tags="minimal rhel9"
# Sun, 27 Apr 2025 20:21:59 GMT
ENV container oci
# Sun, 27 Apr 2025 20:21:59 GMT
COPY dir:9f1e3d7980aa1b8b007cf8dcf05575fff696655332be09ae87c8f7de7f00e923 in / 
# Sun, 27 Apr 2025 20:21:59 GMT
COPY file:b37d593713ee21ad52a4cd1424dc019a24f7966f85df0ac4b86d234302695328 in /etc/yum.repos.d/. 
# Sun, 27 Apr 2025 20:21:59 GMT
CMD ["/bin/bash"]
# Sun, 27 Apr 2025 20:21:59 GMT
COPY file:58cc94f5b3b2d60de2c77a6ed4b1797dcede502ccdb429a72e7a72d994235b3c in /usr/share/buildinfo/content-sets.json 
# Sun, 27 Apr 2025 20:21:59 GMT
LABEL "build-date"="2025-06-24T16:31:57" "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="69e50e2a07c936e700297091886db408257a857c" "release"="1750782676"
# Sun, 27 Apr 2025 20:21:59 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sun, 27 Apr 2025 20:21:59 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sun, 27 Apr 2025 20:21:59 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Sun, 27 Apr 2025 20:21:59 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en     ;     microdnf clean all # buildkit
# Sun, 27 Apr 2025 20:21:59 GMT
ENV JAVA_VERSION=jdk8u452-b09
# Sun, 27 Apr 2025 20:21:59 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='d8a1aecea0913b7a1e0d737ba6f7ea99059b3f6fd17813d4a24e8b3fc3aee278';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u452-b09/OpenJDK8U-jdk_aarch64_linux_hotspot_8u452b09.tar.gz';          ;;        ppc64le)          ESUM='ff6e0f7fad0f46fea47193b95e4187e294ba69bb9059704f5df9f2fb74125732';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u452-b09/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u452b09.tar.gz';          ;;        x86_64)          ESUM='9448308a21841960a591b47927cf2d44fdc4c0533a5f8111a4b243a6bafb5d27';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u452-b09/OpenJDK8U-jdk_x64_linux_hotspot_8u452b09.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip; # buildkit
# Sun, 27 Apr 2025 20:21:59 GMT
RUN set -eux;     echo "Verifying install ...";     echo "javac -version"; javac -version;     echo "java -version"; java -version;     echo "Complete." # buildkit
# Sun, 27 Apr 2025 20:21:59 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Sun, 27 Apr 2025 20:21:59 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 05 Jun 2025 16:04:16 GMT
CMD ["gradle"]
# Thu, 05 Jun 2025 16:04:16 GMT
ENV GRADLE_HOME=/opt/gradle
# Thu, 05 Jun 2025 16:04:16 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 101 gradle     && useradd --system --gid gradle --uid 101 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Thu, 05 Jun 2025 16:04:16 GMT
VOLUME [/home/gradle/.gradle]
# Thu, 05 Jun 2025 16:04:16 GMT
WORKDIR /home/gradle
# Thu, 05 Jun 2025 16:04:16 GMT
RUN set -o errexit -o nounset     && microdnf install -y         make                 findutils                 unzip         which                 git         git-lfs         subversion     && microdnf clean all         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which svn # buildkit
# Thu, 05 Jun 2025 16:04:16 GMT
ENV GRADLE_VERSION=8.14.2
# Thu, 05 Jun 2025 16:04:16 GMT
ARG GRADLE_DOWNLOAD_SHA256=7197a12f450794931532469d4ff21a59ea2c1cd59a3ec3f89c035c3c420a6999
# Thu, 05 Jun 2025 16:04:16 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=7197a12f450794931532469d4ff21a59ea2c1cd59a3ec3f89c035c3c420a6999
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Thu, 05 Jun 2025 16:04:16 GMT
USER gradle
# Thu, 05 Jun 2025 16:04:16 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=7197a12f450794931532469d4ff21a59ea2c1cd59a3ec3f89c035c3c420a6999
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Thu, 05 Jun 2025 16:04:16 GMT
USER root
```

-	Layers:
	-	`sha256:7073092d8bcd7b6d72345cfa87d8389a33f629b3c49ff887ad3a51c6ed8dfd83`  
		Last Modified: Tue, 24 Jun 2025 18:09:29 GMT  
		Size: 39.7 MB (39650665 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11639d3ade5646ac48c61fedaf87359d092793cd58f94a0527c59b4142f2b1b6`  
		Last Modified: Wed, 25 Jun 2025 17:54:26 GMT  
		Size: 27.5 MB (27545286 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75ec5507fad877b6cb578f3fc5c776ccf18d5f75ca04eb53c098748b8a0cb25e`  
		Last Modified: Wed, 25 Jun 2025 17:54:32 GMT  
		Size: 54.7 MB (54716810 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7783baa0d2cb024b743fc875c87d2da2b7614fc6094e9927f878d7aa7dfc83f6`  
		Last Modified: Wed, 25 Jun 2025 17:54:23 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08cbcdb31940222773b2a963f1e0a889b73626f9f15649b1e1493f382cfdc9a5`  
		Last Modified: Wed, 25 Jun 2025 17:54:24 GMT  
		Size: 2.3 KB (2316 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e30c6dcc2ca666cee9bc9d5e1ca03ce6bce1376ed1573c848627a21df37a619`  
		Last Modified: Wed, 25 Jun 2025 18:00:42 GMT  
		Size: 1.7 KB (1711 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6eaaa47e4287f7a776a858a87fe3f42f694a0037f3e83b1a8c3ac5aea6428adb`  
		Last Modified: Wed, 25 Jun 2025 18:00:47 GMT  
		Size: 36.8 MB (36797511 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94603e182dc7c0085b6cd61e89eee1c12d428a519839f7e6c1540138cef18aae`  
		Last Modified: Wed, 25 Jun 2025 23:53:11 GMT  
		Size: 137.4 MB (137395507 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd3cc7925e5e3415f156d6c286427a23a86b0a1cb1aac0e27fb43ea51b0a4851`  
		Last Modified: Wed, 25 Jun 2025 18:00:44 GMT  
		Size: 54.9 KB (54921 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:8-jdk8-ubi` - unknown; unknown

```console
$ docker pull gradle@sha256:17a26416721c08ea97ae214e8049a129619eef9f6aa342ed42583f387f0e7096
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5524632 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0bb01e7d14634b2e6b9f44e8f2661b9aff158830acf57d90b5f33ebd229e9704`

```dockerfile
```

-	Layers:
	-	`sha256:19554a254f97f048d12e7acb4a971e5e676fecab1b688919eba36d19ba693b48`  
		Last Modified: Wed, 25 Jun 2025 20:21:37 GMT  
		Size: 5.5 MB (5500383 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7349cc30fd39f133a8446dc2770049993ae06e8ce9fbe64ac9cd8cb972df5bf8`  
		Last Modified: Wed, 25 Jun 2025 20:21:38 GMT  
		Size: 24.2 KB (24249 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:8-jdk8-ubi` - linux; arm64 variant v8

```console
$ docker pull gradle@sha256:3926bd43edb074be931c9fac8f85b814ae42d2ca78e837e62db0edc534c7dd60
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **293.5 MB (293464037 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e0e27e3c3d5b3145dd9e1cc5e34cabb0aa4c9600872d0199f80c8b769ac323a`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["gradle"]`

```dockerfile
# Sun, 27 Apr 2025 20:21:59 GMT
LABEL maintainer="Red Hat, Inc."
# Sun, 27 Apr 2025 20:21:59 GMT
LABEL vendor="Red Hat, Inc."
# Sun, 27 Apr 2025 20:21:59 GMT
LABEL url="https://www.redhat.com"
# Sun, 27 Apr 2025 20:21:59 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.6"       distribution-scope="public"
# Sun, 27 Apr 2025 20:21:59 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Sun, 27 Apr 2025 20:21:59 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Sun, 27 Apr 2025 20:21:59 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Sun, 27 Apr 2025 20:21:59 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Sun, 27 Apr 2025 20:21:59 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Sun, 27 Apr 2025 20:21:59 GMT
LABEL io.openshift.expose-services=""
# Sun, 27 Apr 2025 20:21:59 GMT
LABEL io.openshift.tags="minimal rhel9"
# Sun, 27 Apr 2025 20:21:59 GMT
ENV container oci
# Sun, 27 Apr 2025 20:21:59 GMT
COPY dir:dd3dc18ab466569b07043336c84190595a673cf78699fcf70dbf83deddf44d87 in / 
# Sun, 27 Apr 2025 20:21:59 GMT
COPY file:b37d593713ee21ad52a4cd1424dc019a24f7966f85df0ac4b86d234302695328 in /etc/yum.repos.d/. 
# Sun, 27 Apr 2025 20:21:59 GMT
CMD ["/bin/bash"]
# Sun, 27 Apr 2025 20:21:59 GMT
COPY file:0667e9d31385a24c3aef13f2dd9ab6a7b71b3dfcfef5127d3c1e2ea2c838e5cb in /usr/share/buildinfo/content-sets.json 
# Sun, 27 Apr 2025 20:21:59 GMT
LABEL "build-date"="2025-06-09T17:24:02" "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="7e18551b8a7ac3e7aa6347d84b9f0b5c8cc8fe52" "release"="1749489516"
# Sun, 27 Apr 2025 20:21:59 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sun, 27 Apr 2025 20:21:59 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sun, 27 Apr 2025 20:21:59 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Sun, 27 Apr 2025 20:21:59 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en     ;     microdnf clean all # buildkit
# Sun, 27 Apr 2025 20:21:59 GMT
ENV JAVA_VERSION=jdk8u452-b09
# Sun, 27 Apr 2025 20:21:59 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='d8a1aecea0913b7a1e0d737ba6f7ea99059b3f6fd17813d4a24e8b3fc3aee278';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u452-b09/OpenJDK8U-jdk_aarch64_linux_hotspot_8u452b09.tar.gz';          ;;        ppc64le)          ESUM='ff6e0f7fad0f46fea47193b95e4187e294ba69bb9059704f5df9f2fb74125732';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u452-b09/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u452b09.tar.gz';          ;;        x86_64)          ESUM='9448308a21841960a591b47927cf2d44fdc4c0533a5f8111a4b243a6bafb5d27';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u452-b09/OpenJDK8U-jdk_x64_linux_hotspot_8u452b09.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip; # buildkit
# Sun, 27 Apr 2025 20:21:59 GMT
RUN set -eux;     echo "Verifying install ...";     echo "javac -version"; javac -version;     echo "java -version"; java -version;     echo "Complete." # buildkit
# Sun, 27 Apr 2025 20:21:59 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Sun, 27 Apr 2025 20:21:59 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 05 Jun 2025 16:04:16 GMT
CMD ["gradle"]
# Thu, 05 Jun 2025 16:04:16 GMT
ENV GRADLE_HOME=/opt/gradle
# Thu, 05 Jun 2025 16:04:16 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 101 gradle     && useradd --system --gid gradle --uid 101 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Thu, 05 Jun 2025 16:04:16 GMT
VOLUME [/home/gradle/.gradle]
# Thu, 05 Jun 2025 16:04:16 GMT
WORKDIR /home/gradle
# Thu, 05 Jun 2025 16:04:16 GMT
RUN set -o errexit -o nounset     && microdnf install -y         make                 findutils                 unzip         which                 git         git-lfs         subversion     && microdnf clean all         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which svn # buildkit
# Thu, 05 Jun 2025 16:04:16 GMT
ENV GRADLE_VERSION=8.14.2
# Thu, 05 Jun 2025 16:04:16 GMT
ARG GRADLE_DOWNLOAD_SHA256=7197a12f450794931532469d4ff21a59ea2c1cd59a3ec3f89c035c3c420a6999
# Thu, 05 Jun 2025 16:04:16 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=7197a12f450794931532469d4ff21a59ea2c1cd59a3ec3f89c035c3c420a6999
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Thu, 05 Jun 2025 16:04:16 GMT
USER gradle
# Thu, 05 Jun 2025 16:04:16 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=7197a12f450794931532469d4ff21a59ea2c1cd59a3ec3f89c035c3c420a6999
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Thu, 05 Jun 2025 16:04:16 GMT
USER root
```

-	Layers:
	-	`sha256:f258ee7f14ce0e3998c50b14ce17a0c0115edefcb69d96c3ef016548422246c8`  
		Last Modified: Mon, 09 Jun 2025 18:09:34 GMT  
		Size: 37.9 MB (37922296 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54c92d528d56d0b425ec1ece8f3484b678fe8fbdfc0181c1023bc51b43374538`  
		Last Modified: Tue, 10 Jun 2025 17:44:06 GMT  
		Size: 28.0 MB (28005980 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c27fdcf0ac78087ad292954cd583f2f96566483816768cff3a85753e5bca5830`  
		Last Modified: Tue, 10 Jun 2025 17:44:18 GMT  
		Size: 53.8 MB (53831027 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a432173bb3f9a0b181bcc220e3f2252084b68c0e3f2824765e89c390e48d99fc`  
		Last Modified: Tue, 10 Jun 2025 17:44:01 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:493dfaa6c9345c47486c857b533c7287cdc922c7785238228331d8d649f4c471`  
		Last Modified: Tue, 10 Jun 2025 17:44:01 GMT  
		Size: 2.3 KB (2315 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2677bc626945ac2f44b537566b170e55bfbbec930b105419ac6cee990cc51641`  
		Last Modified: Tue, 10 Jun 2025 18:17:22 GMT  
		Size: 1.7 KB (1709 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c05cd38b1572fc01e1a1b6928f76cebaf04e18406c9982576ba25e3333b3245`  
		Last Modified: Tue, 10 Jun 2025 18:17:28 GMT  
		Size: 36.2 MB (36245508 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:426d0017b2221259cb5971a3e535234e1495e648a679da4bc21efcff40e04063`  
		Last Modified: Tue, 10 Jun 2025 23:27:44 GMT  
		Size: 137.4 MB (137395511 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d132b500e0cbffd5fb11f3a47c454a92d097edf99e8f99de1627af148b0afab1`  
		Last Modified: Tue, 10 Jun 2025 18:17:23 GMT  
		Size: 59.5 KB (59533 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:8-jdk8-ubi` - unknown; unknown

```console
$ docker pull gradle@sha256:4490748da37716a5ea48b81cece976de2fd9245e578fcbbd9fe80dec415b3d9b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5524875 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a40ca1402576f22e7a28125a965b60783a461a482635d8733e6e9e3a77e9d0ce`

```dockerfile
```

-	Layers:
	-	`sha256:2d93d079e1427521d074b34f9fbc8e4df5530814be61e7f096f213e694c2c245`  
		Last Modified: Tue, 10 Jun 2025 20:22:28 GMT  
		Size: 5.5 MB (5500429 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:657c6674d1afc803ab3df7657f586fc8ba55ad94b05965d56f15f8ca94adbed5`  
		Last Modified: Tue, 10 Jun 2025 20:22:28 GMT  
		Size: 24.4 KB (24446 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:8-jdk8-ubi` - linux; ppc64le

```console
$ docker pull gradle@sha256:71b28c9580c0a7064b39e85e2c01ec41841c1d90a556c85bd8bd19d5fddfeef8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **301.8 MB (301754792 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21e94521521ef674d4ad735ed22085dd7638444e43321723cbf2ac92b92a40f5`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["gradle"]`

```dockerfile
# Sun, 27 Apr 2025 20:21:59 GMT
LABEL maintainer="Red Hat, Inc."
# Sun, 27 Apr 2025 20:21:59 GMT
LABEL vendor="Red Hat, Inc."
# Sun, 27 Apr 2025 20:21:59 GMT
LABEL url="https://www.redhat.com"
# Sun, 27 Apr 2025 20:21:59 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.6"       distribution-scope="public"
# Sun, 27 Apr 2025 20:21:59 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Sun, 27 Apr 2025 20:21:59 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Sun, 27 Apr 2025 20:21:59 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Sun, 27 Apr 2025 20:21:59 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Sun, 27 Apr 2025 20:21:59 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Sun, 27 Apr 2025 20:21:59 GMT
LABEL io.openshift.expose-services=""
# Sun, 27 Apr 2025 20:21:59 GMT
LABEL io.openshift.tags="minimal rhel9"
# Sun, 27 Apr 2025 20:21:59 GMT
ENV container oci
# Sun, 27 Apr 2025 20:21:59 GMT
COPY dir:d83abf82dbf4be7abfad8c73a5c54416daede00b99a88ceef5492299e80e8120 in / 
# Sun, 27 Apr 2025 20:21:59 GMT
COPY file:b37d593713ee21ad52a4cd1424dc019a24f7966f85df0ac4b86d234302695328 in /etc/yum.repos.d/. 
# Sun, 27 Apr 2025 20:21:59 GMT
CMD ["/bin/bash"]
# Sun, 27 Apr 2025 20:21:59 GMT
COPY file:0667e9d31385a24c3aef13f2dd9ab6a7b71b3dfcfef5127d3c1e2ea2c838e5cb in /usr/share/buildinfo/content-sets.json 
# Sun, 27 Apr 2025 20:21:59 GMT
LABEL "build-date"="2025-06-24T16:34:39" "architecture"="ppc64le" "vcs-type"="git" "vcs-ref"="69e50e2a07c936e700297091886db408257a857c" "release"="1750782676"
# Sun, 27 Apr 2025 20:21:59 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sun, 27 Apr 2025 20:21:59 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sun, 27 Apr 2025 20:21:59 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Sun, 27 Apr 2025 20:21:59 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en     ;     microdnf clean all # buildkit
# Sun, 27 Apr 2025 20:21:59 GMT
ENV JAVA_VERSION=jdk8u452-b09
# Sun, 27 Apr 2025 20:21:59 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='d8a1aecea0913b7a1e0d737ba6f7ea99059b3f6fd17813d4a24e8b3fc3aee278';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u452-b09/OpenJDK8U-jdk_aarch64_linux_hotspot_8u452b09.tar.gz';          ;;        ppc64le)          ESUM='ff6e0f7fad0f46fea47193b95e4187e294ba69bb9059704f5df9f2fb74125732';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u452-b09/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u452b09.tar.gz';          ;;        x86_64)          ESUM='9448308a21841960a591b47927cf2d44fdc4c0533a5f8111a4b243a6bafb5d27';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u452-b09/OpenJDK8U-jdk_x64_linux_hotspot_8u452b09.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip; # buildkit
# Sun, 27 Apr 2025 20:21:59 GMT
RUN set -eux;     echo "Verifying install ...";     echo "javac -version"; javac -version;     echo "java -version"; java -version;     echo "Complete." # buildkit
# Sun, 27 Apr 2025 20:21:59 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Sun, 27 Apr 2025 20:21:59 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 05 Jun 2025 16:04:16 GMT
CMD ["gradle"]
# Thu, 05 Jun 2025 16:04:16 GMT
ENV GRADLE_HOME=/opt/gradle
# Thu, 05 Jun 2025 16:04:16 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 101 gradle     && useradd --system --gid gradle --uid 101 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Thu, 05 Jun 2025 16:04:16 GMT
VOLUME [/home/gradle/.gradle]
# Thu, 05 Jun 2025 16:04:16 GMT
WORKDIR /home/gradle
# Thu, 05 Jun 2025 16:04:16 GMT
RUN set -o errexit -o nounset     && microdnf install -y         make                 findutils                 unzip         which                 git         git-lfs         subversion     && microdnf clean all         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which svn # buildkit
# Thu, 05 Jun 2025 16:04:16 GMT
ENV GRADLE_VERSION=8.14.2
# Thu, 05 Jun 2025 16:04:16 GMT
ARG GRADLE_DOWNLOAD_SHA256=7197a12f450794931532469d4ff21a59ea2c1cd59a3ec3f89c035c3c420a6999
# Thu, 05 Jun 2025 16:04:16 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=7197a12f450794931532469d4ff21a59ea2c1cd59a3ec3f89c035c3c420a6999
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Thu, 05 Jun 2025 16:04:16 GMT
USER gradle
# Thu, 05 Jun 2025 16:04:16 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=7197a12f450794931532469d4ff21a59ea2c1cd59a3ec3f89c035c3c420a6999
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Thu, 05 Jun 2025 16:04:16 GMT
USER root
```

-	Layers:
	-	`sha256:8374cdcea99a5f341eb5030b5ece88085798cef7a6357cfcc46f8db2ab3dcbc9`  
		Last Modified: Tue, 24 Jun 2025 18:09:28 GMT  
		Size: 44.0 MB (44041398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5872ee8c9a0f398b2cc0631abe2164a5c0397d35045d1f9af834e8f8f4da60c2`  
		Last Modified: Wed, 25 Jun 2025 17:54:51 GMT  
		Size: 30.0 MB (29977285 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e30567529ed8ba7cf1aa1fe22bb2e18a34b6a842c87ee9edc17699fc86245612`  
		Last Modified: Wed, 25 Jun 2025 17:54:56 GMT  
		Size: 52.2 MB (52168600 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c00db75dd70d27c991465d78951019bb0bf48ff1376711cf100d7227488281a4`  
		Last Modified: Wed, 25 Jun 2025 17:54:47 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea5fee28c835d628dbdc5c5023050174ba606350a75461181842779b5978f862`  
		Last Modified: Wed, 25 Jun 2025 17:54:47 GMT  
		Size: 2.3 KB (2316 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be5971d1899afb91da8aa63d3315432ee0f4f1fee0220c788ae4e62d6ddafbe0`  
		Last Modified: Wed, 25 Jun 2025 18:27:50 GMT  
		Size: 1.7 KB (1709 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6d61910c65958fd0d5224a1f159e08cdd5817fa512a78c3d5ef781ac949ea32`  
		Last Modified: Wed, 25 Jun 2025 18:27:52 GMT  
		Size: 38.1 MB (38132806 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:924c4f09a39209b18006ff1b8f78f2d5b36f7e5d795762491284dc08ddf53645`  
		Last Modified: Wed, 25 Jun 2025 18:27:56 GMT  
		Size: 137.4 MB (137395509 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:735fba7b693c6d87ff1c5e3bff3181d11606fe9f6f865a9cdc970b2f5aa8cdbb`  
		Last Modified: Wed, 25 Jun 2025 18:27:51 GMT  
		Size: 35.0 KB (35011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:8-jdk8-ubi` - unknown; unknown

```console
$ docker pull gradle@sha256:0706953ad01c16fdcac006d31e063e9e8d7be9a848b6c7ad8becc417d03fe22e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5522636 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:da5ac4987d30be7ed76bf0f67c9040637144c9fcd88c08eb8d8d0a9454ea0a36`

```dockerfile
```

-	Layers:
	-	`sha256:3fa263bc5f8251bf415b90da5382aec917932fbbd4e9e72cfd4d024aeeb9cc31`  
		Last Modified: Wed, 25 Jun 2025 20:21:48 GMT  
		Size: 5.5 MB (5498313 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:58cfd0910460f656fbb249fbddfe1869c2770f50661c6fe9518f2c123e503097`  
		Last Modified: Wed, 25 Jun 2025 20:21:49 GMT  
		Size: 24.3 KB (24323 bytes)  
		MIME: application/vnd.in-toto+json
