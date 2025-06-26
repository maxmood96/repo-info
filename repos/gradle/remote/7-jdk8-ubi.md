## `gradle:7-jdk8-ubi`

```console
$ docker pull gradle@sha256:db0fb286cdd4f7d6a3a55802ae0d21d5e8a2af81d30e7abeec2a459e879ab02f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `gradle:7-jdk8-ubi` - linux; amd64

```console
$ docker pull gradle@sha256:426983a993182999a1caa3a85c9d46fdd98ef696d8657e5793c6ee98fdb36c48
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **287.2 MB (287239314 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:87f3315951ff6757ec35f6def6150666f9db268d1c8e7f8598964b21ff09deff`
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
# Wed, 04 Jun 2025 15:28:43 GMT
CMD ["gradle"]
# Wed, 04 Jun 2025 15:28:43 GMT
ENV GRADLE_HOME=/opt/gradle
# Wed, 04 Jun 2025 15:28:43 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 101 gradle     && useradd --system --gid gradle --uid 101 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Wed, 04 Jun 2025 15:28:43 GMT
VOLUME [/home/gradle/.gradle]
# Wed, 04 Jun 2025 15:28:43 GMT
WORKDIR /home/gradle
# Wed, 04 Jun 2025 15:28:43 GMT
RUN set -o errexit -o nounset     && microdnf install -y         make                 findutils                 unzip         which                 git         git-lfs         subversion     && microdnf clean all         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which svn # buildkit
# Wed, 04 Jun 2025 15:28:43 GMT
ENV GRADLE_VERSION=7.6.5
# Wed, 04 Jun 2025 15:28:43 GMT
ARG GRADLE_DOWNLOAD_SHA256=b812fec0edb7d27e0ae35955887bb2954536fa3e44edaf481150da058e154d9a
# Wed, 04 Jun 2025 15:28:43 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=b812fec0edb7d27e0ae35955887bb2954536fa3e44edaf481150da058e154d9a
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Wed, 04 Jun 2025 15:28:43 GMT
USER gradle
# Wed, 04 Jun 2025 15:28:43 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=b812fec0edb7d27e0ae35955887bb2954536fa3e44edaf481150da058e154d9a
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Wed, 04 Jun 2025 15:28:43 GMT
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
	-	`sha256:3f1e43c32a0e7521b114b9b03288b23dccc1a4b9d355b937ca715f73e267852b`  
		Last Modified: Wed, 25 Jun 2025 20:21:17 GMT  
		Size: 1.7 KB (1710 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:141ecf4e55ec2ab232f8256aaac4d3b197c2e0c2998aee3f0aba3d5de384693d`  
		Last Modified: Wed, 25 Jun 2025 20:21:21 GMT  
		Size: 36.8 MB (36797555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2492a854c4a0bef18d220fe1adb99f6d076e25a9ccfe34e2a6fe7fd8c37d89da`  
		Last Modified: Wed, 25 Jun 2025 20:21:29 GMT  
		Size: 128.5 MB (128469908 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26af2828aefdee68bfc9afd7033f6c7e38c5ff953e49311dd69b07d1e614f1cc`  
		Last Modified: Wed, 25 Jun 2025 20:21:18 GMT  
		Size: 54.9 KB (54906 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:7-jdk8-ubi` - unknown; unknown

```console
$ docker pull gradle@sha256:b84f5d50dacabfe1a9b2e17c77d7cab002dcc897d55896c25fb4795724bc9bb1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5433999 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:05859ef612b450d359e67e28ab4eb2e9eecc0928a7e7f9f7ac99a7916036b3ec`

```dockerfile
```

-	Layers:
	-	`sha256:f085d5ba3137170db991e94dd75b0fbcddbde198ce4ff92dbc9b9c99b2aa2af3`  
		Last Modified: Wed, 25 Jun 2025 20:19:08 GMT  
		Size: 5.4 MB (5410380 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d5ad8fed4857cbb19e0a9b5885fe0889009ee1f160a894462b51291a554fd6ea`  
		Last Modified: Wed, 25 Jun 2025 20:19:08 GMT  
		Size: 23.6 KB (23619 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:7-jdk8-ubi` - linux; arm64 variant v8

```console
$ docker pull gradle@sha256:db2cc6fb1dd3f609ab0e31bff9b4f35249dea993c3f9b078d230c0e0e645452a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **284.5 MB (284454306 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:67613fd1acb20113c0322a4ade4a8e202b6d86b81c49bcfd40e5a4c5f2fab4bb`
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
COPY dir:837c51d2245269e7540005032254a14f4d0618334b5c45ecacf5b0c7968d0657 in / 
# Sun, 27 Apr 2025 20:21:59 GMT
COPY file:b37d593713ee21ad52a4cd1424dc019a24f7966f85df0ac4b86d234302695328 in /etc/yum.repos.d/. 
# Sun, 27 Apr 2025 20:21:59 GMT
CMD ["/bin/bash"]
# Sun, 27 Apr 2025 20:21:59 GMT
COPY file:0667e9d31385a24c3aef13f2dd9ab6a7b71b3dfcfef5127d3c1e2ea2c838e5cb in /usr/share/buildinfo/content-sets.json 
# Sun, 27 Apr 2025 20:21:59 GMT
LABEL "build-date"="2025-06-24T16:36:46" "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="69e50e2a07c936e700297091886db408257a857c" "release"="1750782676"
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
# Wed, 04 Jun 2025 15:28:43 GMT
CMD ["gradle"]
# Wed, 04 Jun 2025 15:28:43 GMT
ENV GRADLE_HOME=/opt/gradle
# Wed, 04 Jun 2025 15:28:43 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 101 gradle     && useradd --system --gid gradle --uid 101 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Wed, 04 Jun 2025 15:28:43 GMT
VOLUME [/home/gradle/.gradle]
# Wed, 04 Jun 2025 15:28:43 GMT
WORKDIR /home/gradle
# Wed, 04 Jun 2025 15:28:43 GMT
RUN set -o errexit -o nounset     && microdnf install -y         make                 findutils                 unzip         which                 git         git-lfs         subversion     && microdnf clean all         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which svn # buildkit
# Wed, 04 Jun 2025 15:28:43 GMT
ENV GRADLE_VERSION=7.6.5
# Wed, 04 Jun 2025 15:28:43 GMT
ARG GRADLE_DOWNLOAD_SHA256=b812fec0edb7d27e0ae35955887bb2954536fa3e44edaf481150da058e154d9a
# Wed, 04 Jun 2025 15:28:43 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=b812fec0edb7d27e0ae35955887bb2954536fa3e44edaf481150da058e154d9a
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Wed, 04 Jun 2025 15:28:43 GMT
USER gradle
# Wed, 04 Jun 2025 15:28:43 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=b812fec0edb7d27e0ae35955887bb2954536fa3e44edaf481150da058e154d9a
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Wed, 04 Jun 2025 15:28:43 GMT
USER root
```

-	Layers:
	-	`sha256:ba92c2079b2b21a2f178ace5ca98b5ef2d5cd02901c30e48729b7afe34ecd27e`  
		Last Modified: Tue, 24 Jun 2025 18:09:22 GMT  
		Size: 37.9 MB (37864307 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3125884470194b729e029c422952b37ddb3dfcef76081c7840c9b26da3881d57`  
		Last Modified: Wed, 25 Jun 2025 23:05:10 GMT  
		Size: 28.0 MB (27988538 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6b1344e8de55ffa8dfc7a5cbcfc3e8082cfd88b8edea34ec6c25dd76466b7c0`  
		Last Modified: Wed, 25 Jun 2025 23:05:13 GMT  
		Size: 53.8 MB (53831031 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e270a0a08b7a19952f100927a5b1fc9bd0e2ddbb8e806436eb2e3ab6aa6cf8a6`  
		Last Modified: Wed, 25 Jun 2025 23:05:08 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:919d671207d9546c5e74456e4d81e48c180f6b0794307dd913e52819d0b594f1`  
		Last Modified: Wed, 25 Jun 2025 23:05:09 GMT  
		Size: 2.3 KB (2314 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:351c8d0391f9a076917914a32823810e15591ceef5cb9d26f0ca8acbac9d6542`  
		Last Modified: Thu, 26 Jun 2025 00:55:26 GMT  
		Size: 1.7 KB (1713 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3aa18794d2222e61eabc657d72e4f50391b5293a19740c86e23adab3d43e7e3a`  
		Last Modified: Thu, 26 Jun 2025 00:55:40 GMT  
		Size: 36.2 MB (36236806 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1b61efb65e33f8acd87290fbcc5e30887c6929684ce560f02bd93215147a3f1`  
		Last Modified: Thu, 26 Jun 2025 03:35:00 GMT  
		Size: 128.5 MB (128469911 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fc086e37254327085b8c8aedc4017c376369f8e0bc7f780cb52119f44e46c34`  
		Last Modified: Thu, 26 Jun 2025 00:56:15 GMT  
		Size: 59.5 KB (59527 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:7-jdk8-ubi` - unknown; unknown

```console
$ docker pull gradle@sha256:536b5f7ddaafb9a17834fb30bada1b85566b026ae0e6d9b59f8219138c96e334
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5434282 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c1478a1965962e3f138a434c7f5c393ee1994fd1f281e8a4f397cf6082425d21`

```dockerfile
```

-	Layers:
	-	`sha256:3323507bd68650d3203f1ac142b26e44daefc83cf86f1640c6d1fda0427a5d9a`  
		Last Modified: Thu, 26 Jun 2025 02:18:45 GMT  
		Size: 5.4 MB (5410490 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:81ac9a596866bb08b6527eedda0abc15363280c538735e0efe5afb7894bbc7b8`  
		Last Modified: Thu, 26 Jun 2025 02:18:45 GMT  
		Size: 23.8 KB (23792 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:7-jdk8-ubi` - linux; ppc64le

```console
$ docker pull gradle@sha256:9b423a8e3afabf09575ddcc8ed33353d9929be0f3ab5c7b4d41363a5d9bffbff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **292.8 MB (292829206 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:11e1891ff505fa5dad11a257589fa85152ee72e4d5c55caa4bb04f7310e90ae3`
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
# Wed, 04 Jun 2025 15:28:43 GMT
CMD ["gradle"]
# Wed, 04 Jun 2025 15:28:43 GMT
ENV GRADLE_HOME=/opt/gradle
# Wed, 04 Jun 2025 15:28:43 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 101 gradle     && useradd --system --gid gradle --uid 101 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Wed, 04 Jun 2025 15:28:43 GMT
VOLUME [/home/gradle/.gradle]
# Wed, 04 Jun 2025 15:28:43 GMT
WORKDIR /home/gradle
# Wed, 04 Jun 2025 15:28:43 GMT
RUN set -o errexit -o nounset     && microdnf install -y         make                 findutils                 unzip         which                 git         git-lfs         subversion     && microdnf clean all         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which svn # buildkit
# Wed, 04 Jun 2025 15:28:43 GMT
ENV GRADLE_VERSION=7.6.5
# Wed, 04 Jun 2025 15:28:43 GMT
ARG GRADLE_DOWNLOAD_SHA256=b812fec0edb7d27e0ae35955887bb2954536fa3e44edaf481150da058e154d9a
# Wed, 04 Jun 2025 15:28:43 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=b812fec0edb7d27e0ae35955887bb2954536fa3e44edaf481150da058e154d9a
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Wed, 04 Jun 2025 15:28:43 GMT
USER gradle
# Wed, 04 Jun 2025 15:28:43 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=b812fec0edb7d27e0ae35955887bb2954536fa3e44edaf481150da058e154d9a
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Wed, 04 Jun 2025 15:28:43 GMT
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
	-	`sha256:1395b6a05c483683cdba60b83f956d4c57679fde0bc6780e7518033686a08fd6`  
		Last Modified: Wed, 25 Jun 2025 18:31:58 GMT  
		Size: 128.5 MB (128469913 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bac9fed9c3638d572f5e9d907a4afcfebc05a3de42f568bde09d2f157d695120`  
		Last Modified: Wed, 25 Jun 2025 18:32:25 GMT  
		Size: 35.0 KB (35021 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:7-jdk8-ubi` - unknown; unknown

```console
$ docker pull gradle@sha256:caed477625c4376a3a677141f8609da6e1435ccaf6a7cf6bad63bbb2096d7d28
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5431979 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc2314473dcc11571a98c979c21b1a0a7ce68645573eed0bd006426386940db4`

```dockerfile
```

-	Layers:
	-	`sha256:443d253d375afc3cbd6f36f5b12fd0242c0c55b19602aed99021f3f0cb546121`  
		Last Modified: Wed, 25 Jun 2025 20:19:20 GMT  
		Size: 5.4 MB (5408298 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:832aa6b8c37e11054357e847b2bada37ddbfad08a313ff4a33d8fdbfa8e508db`  
		Last Modified: Wed, 25 Jun 2025 20:19:20 GMT  
		Size: 23.7 KB (23681 bytes)  
		MIME: application/vnd.in-toto+json
