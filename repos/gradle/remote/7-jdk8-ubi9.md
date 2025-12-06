## `gradle:7-jdk8-ubi9`

```console
$ docker pull gradle@sha256:3d9ef14b8a40f449d85f0dc74b27661f0c44477b804f739a51badb02fe80a970
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `gradle:7-jdk8-ubi9` - linux; amd64

```console
$ docker pull gradle@sha256:a17b9d2bd2c0bffb3246d92e73f82bdad139b849c379c2da0a8b8c566b0a82d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **290.4 MB (290369074 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3fd2db62cca9b6e950a91fcaaee87ec37095cb28f7a646f6e4166198861bd168`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["gradle"]`

```dockerfile
# Wed, 03 Dec 2025 20:36:20 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 03 Dec 2025 20:36:20 GMT
LABEL vendor="Red Hat, Inc."
# Wed, 03 Dec 2025 20:36:20 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Wed, 03 Dec 2025 20:36:20 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.7"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Wed, 03 Dec 2025 20:36:20 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 03 Dec 2025 20:36:20 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Wed, 03 Dec 2025 20:36:20 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 03 Dec 2025 20:36:20 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 03 Dec 2025 20:36:20 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Wed, 03 Dec 2025 20:36:20 GMT
LABEL io.openshift.expose-services=""
# Wed, 03 Dec 2025 20:36:20 GMT
LABEL io.openshift.tags="minimal rhel9"
# Wed, 03 Dec 2025 20:36:20 GMT
ENV container oci
# Wed, 03 Dec 2025 20:36:21 GMT
COPY dir:be2a521f68bf56126048c385ab01382fd10aa537a578d817938c3b4ce9ee2ae8 in /      
# Wed, 03 Dec 2025 20:36:21 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Wed, 03 Dec 2025 20:36:21 GMT
CMD ["/bin/bash"]
# Wed, 03 Dec 2025 20:36:21 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /usr/share/buildinfo/content-sets.json      
# Wed, 03 Dec 2025 20:36:21 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /root/buildinfo/content_manifests/content-sets.json      
# Wed, 03 Dec 2025 20:36:21 GMT
COPY file:94153b6833d6f050d8e2572e9c332f16148f47aceac72aaf42af4d08feb01e61 in /usr/share/buildinfo/labels.json      
# Wed, 03 Dec 2025 20:36:21 GMT
COPY file:94153b6833d6f050d8e2572e9c332f16148f47aceac72aaf42af4d08feb01e61 in /root/buildinfo/labels.json      
# Wed, 03 Dec 2025 20:36:21 GMT
LABEL "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="1595c1bf15cd4327d529f330e61327764327397e" "org.opencontainers.image.revision"="1595c1bf15cd4327d529f330e61327764327397e" "build-date"="2025-12-03T20:36:05Z" "org.opencontainers.image.created"="2025-12-03T20:36:05Z" "release"="1764794109"org.opencontainers.image.revision=1595c1bf15cd4327d529f330e61327764327397e,org.opencontainers.image.created=2025-12-03T20:36:05Z
# Thu, 04 Dec 2025 19:45:24 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 04 Dec 2025 19:45:24 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 04 Dec 2025 19:45:24 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 04 Dec 2025 19:45:24 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en     ;     microdnf clean all # buildkit
# Thu, 04 Dec 2025 19:45:24 GMT
ENV JAVA_VERSION=jdk8u472-b08
# Thu, 04 Dec 2025 19:45:28 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='e2aff19d85d2441e409d6cbdf12ef7c2acabb0de73bca4207947135dcaa935a2';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u472-b08/OpenJDK8U-jdk_aarch64_linux_hotspot_8u472b08.tar.gz';          ;;        ppc64le)          ESUM='eaf57a4564265583b0641c878bea8943d27ef110c096868f686dae179fb45d8f';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u472-b08/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u472b08.tar.gz';          ;;        x86_64)          ESUM='5becaa4ac660e844c5a39e2ebc39ff5ac824c37ff1b625af8c8b111dc13c3592';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u472-b08/OpenJDK8U-jdk_x64_linux_hotspot_8u472b08.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip; # buildkit
# Thu, 04 Dec 2025 19:45:28 GMT
RUN set -eux;     echo "Verifying install ...";     echo "javac -version"; javac -version;     echo "java -version"; java -version;     echo "Complete." # buildkit
# Thu, 04 Dec 2025 19:45:28 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 04 Dec 2025 19:45:28 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 04 Dec 2025 20:03:21 GMT
CMD ["gradle"]
# Thu, 04 Dec 2025 20:03:21 GMT
ENV GRADLE_HOME=/opt/gradle
# Thu, 04 Dec 2025 20:03:21 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 101 gradle     && useradd --system --gid gradle --uid 101 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Thu, 04 Dec 2025 20:03:21 GMT
VOLUME [/home/gradle/.gradle]
# Thu, 04 Dec 2025 20:03:21 GMT
WORKDIR /home/gradle
# Thu, 04 Dec 2025 20:03:25 GMT
RUN set -o errexit -o nounset     && microdnf install -y         make                 findutils                 unzip         which                 git         git-lfs         subversion     && microdnf clean all         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which svn # buildkit
# Thu, 04 Dec 2025 20:03:25 GMT
ENV GRADLE_VERSION=7.6.6
# Thu, 04 Dec 2025 20:03:25 GMT
ARG GRADLE_DOWNLOAD_SHA256=673d9776f303bc7048fc3329d232d6ebf1051b07893bd9d11616fad9a8673be0
# Thu, 04 Dec 2025 20:05:06 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=673d9776f303bc7048fc3329d232d6ebf1051b07893bd9d11616fad9a8673be0
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Thu, 04 Dec 2025 20:05:06 GMT
USER gradle
# Thu, 04 Dec 2025 20:05:06 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=673d9776f303bc7048fc3329d232d6ebf1051b07893bd9d11616fad9a8673be0
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Thu, 04 Dec 2025 20:05:06 GMT
USER root
```

-	Layers:
	-	`sha256:46a9484471e55e0e501c08ff903616330af0505ba749ef70e8c87e103e07844a`  
		Last Modified: Wed, 03 Dec 2025 21:15:52 GMT  
		Size: 40.0 MB (40040759 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58683a05ac4545db26cedb6bf069ef78065981b9418ff344b989e5547ce25b5f`  
		Last Modified: Thu, 04 Dec 2025 19:45:59 GMT  
		Size: 30.4 MB (30411196 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89fd6d63ce446b3c72b69a2d8e22c1e1bce85e80babbd581ae17c28aedfad9f2`  
		Last Modified: Thu, 04 Dec 2025 19:46:03 GMT  
		Size: 54.7 MB (54733890 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:943d48f1e0be13aedef8fdbef1876c347e0c22eb32b7eadbaa2c8b8392f12f21`  
		Last Modified: Thu, 04 Dec 2025 19:45:57 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ce20366d02268265499b9b612d24e92c58a8fc5b442d8e08eff2351977659e7`  
		Last Modified: Thu, 04 Dec 2025 19:45:57 GMT  
		Size: 2.3 KB (2314 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d4d26c6d668bc3ec300bb51a1d2f429f6993aa4df0d79b19017f0bc243c36be`  
		Last Modified: Thu, 04 Dec 2025 20:03:56 GMT  
		Size: 1.7 KB (1706 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:505f09bcf1936141ffd85894298ab9ac9b33df63f61b306a6ef2bc93a6c72a1e`  
		Last Modified: Thu, 04 Dec 2025 20:04:00 GMT  
		Size: 36.7 MB (36654725 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b941e4d86e3af8c2f3742ed0ac067841e3d3bfc9a198848a58d2dae9da62478`  
		Last Modified: Fri, 05 Dec 2025 10:58:04 GMT  
		Size: 128.5 MB (128469420 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6abea62ab341e675f52eafa18c5f0adba67838f8513a99a71d6bfdfbc7c7d5ee`  
		Last Modified: Thu, 04 Dec 2025 20:05:29 GMT  
		Size: 54.9 KB (54903 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:7-jdk8-ubi9` - unknown; unknown

```console
$ docker pull gradle@sha256:10101d0d4548ff94ccd27f7d6ad2da4ca690d590b00c3db4d4f41d17677ea4ab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5458324 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b45fb2a04ba3b3584feb3406d52ae288fff7caae96c3df0fb41c4141258a679`

```dockerfile
```

-	Layers:
	-	`sha256:954a17aaf6cbdce605a17c92548bc21ef5de23577a25ebb2a115a22017695e85`  
		Last Modified: Thu, 04 Dec 2025 21:19:37 GMT  
		Size: 5.4 MB (5434770 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:70e125785c79ece57c28010da3c1deafb1c14e65f1c71dedec27599f83edf1a6`  
		Last Modified: Thu, 04 Dec 2025 21:19:38 GMT  
		Size: 23.6 KB (23554 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:7-jdk8-ubi9` - linux; arm64 variant v8

```console
$ docker pull gradle@sha256:712faa698f2b794adcc7f0be9630ba97750ca9d0ba1f8c421a84be59098c002d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **287.5 MB (287478056 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8cc746c0f9e0c5770d95237c5018b8b8b549a8889c7e335e74bd7136dab02f33`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["gradle"]`

```dockerfile
# Wed, 03 Dec 2025 20:39:01 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 03 Dec 2025 20:39:01 GMT
LABEL vendor="Red Hat, Inc."
# Wed, 03 Dec 2025 20:39:01 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Wed, 03 Dec 2025 20:39:01 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.7"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Wed, 03 Dec 2025 20:39:01 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 03 Dec 2025 20:39:01 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Wed, 03 Dec 2025 20:39:01 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 03 Dec 2025 20:39:01 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 03 Dec 2025 20:39:01 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Wed, 03 Dec 2025 20:39:01 GMT
LABEL io.openshift.expose-services=""
# Wed, 03 Dec 2025 20:39:01 GMT
LABEL io.openshift.tags="minimal rhel9"
# Wed, 03 Dec 2025 20:39:01 GMT
ENV container oci
# Wed, 03 Dec 2025 20:39:02 GMT
COPY dir:f4ea265792475a3d4d1f704e5646b6b392f1a575aee1ff63417d34e28530c8cb in /      
# Wed, 03 Dec 2025 20:39:02 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Wed, 03 Dec 2025 20:39:02 GMT
CMD ["/bin/bash"]
# Wed, 03 Dec 2025 20:39:02 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /usr/share/buildinfo/content-sets.json      
# Wed, 03 Dec 2025 20:39:02 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /root/buildinfo/content_manifests/content-sets.json      
# Wed, 03 Dec 2025 20:39:02 GMT
COPY file:cac453727cef4359ee0e696635ab5d4ce6ce1ac7334c1d943b8e8f2fb464f41f in /usr/share/buildinfo/labels.json      
# Wed, 03 Dec 2025 20:39:02 GMT
COPY file:cac453727cef4359ee0e696635ab5d4ce6ce1ac7334c1d943b8e8f2fb464f41f in /root/buildinfo/labels.json      
# Wed, 03 Dec 2025 20:39:03 GMT
LABEL "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="1595c1bf15cd4327d529f330e61327764327397e" "org.opencontainers.image.revision"="1595c1bf15cd4327d529f330e61327764327397e" "build-date"="2025-12-03T20:38:45Z" "org.opencontainers.image.created"="2025-12-03T20:38:45Z" "release"="1764794109"org.opencontainers.image.revision=1595c1bf15cd4327d529f330e61327764327397e,org.opencontainers.image.created=2025-12-03T20:38:45Z
# Thu, 04 Dec 2025 19:45:34 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 04 Dec 2025 19:45:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 04 Dec 2025 19:45:34 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 04 Dec 2025 19:45:34 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en     ;     microdnf clean all # buildkit
# Thu, 04 Dec 2025 19:45:34 GMT
ENV JAVA_VERSION=jdk8u472-b08
# Thu, 04 Dec 2025 19:45:39 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='e2aff19d85d2441e409d6cbdf12ef7c2acabb0de73bca4207947135dcaa935a2';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u472-b08/OpenJDK8U-jdk_aarch64_linux_hotspot_8u472b08.tar.gz';          ;;        ppc64le)          ESUM='eaf57a4564265583b0641c878bea8943d27ef110c096868f686dae179fb45d8f';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u472-b08/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u472b08.tar.gz';          ;;        x86_64)          ESUM='5becaa4ac660e844c5a39e2ebc39ff5ac824c37ff1b625af8c8b111dc13c3592';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u472-b08/OpenJDK8U-jdk_x64_linux_hotspot_8u472b08.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip; # buildkit
# Thu, 04 Dec 2025 19:45:39 GMT
RUN set -eux;     echo "Verifying install ...";     echo "javac -version"; javac -version;     echo "java -version"; java -version;     echo "Complete." # buildkit
# Thu, 04 Dec 2025 19:45:39 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 04 Dec 2025 19:45:39 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 04 Dec 2025 20:05:56 GMT
CMD ["gradle"]
# Thu, 04 Dec 2025 20:05:56 GMT
ENV GRADLE_HOME=/opt/gradle
# Thu, 04 Dec 2025 20:05:56 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 101 gradle     && useradd --system --gid gradle --uid 101 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Thu, 04 Dec 2025 20:05:56 GMT
VOLUME [/home/gradle/.gradle]
# Thu, 04 Dec 2025 20:05:56 GMT
WORKDIR /home/gradle
# Thu, 04 Dec 2025 20:06:00 GMT
RUN set -o errexit -o nounset     && microdnf install -y         make                 findutils                 unzip         which                 git         git-lfs         subversion     && microdnf clean all         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which svn # buildkit
# Thu, 04 Dec 2025 20:06:00 GMT
ENV GRADLE_VERSION=7.6.6
# Thu, 04 Dec 2025 20:06:00 GMT
ARG GRADLE_DOWNLOAD_SHA256=673d9776f303bc7048fc3329d232d6ebf1051b07893bd9d11616fad9a8673be0
# Thu, 04 Dec 2025 20:06:02 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=673d9776f303bc7048fc3329d232d6ebf1051b07893bd9d11616fad9a8673be0
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Thu, 04 Dec 2025 20:06:02 GMT
USER gradle
# Thu, 04 Dec 2025 20:06:03 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=673d9776f303bc7048fc3329d232d6ebf1051b07893bd9d11616fad9a8673be0
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Thu, 04 Dec 2025 20:06:03 GMT
USER root
```

-	Layers:
	-	`sha256:15f4b55884339bddb52ca0550d5b1208576ecf31649e067b468dc4e7b90745bd`  
		Last Modified: Wed, 03 Dec 2025 22:01:09 GMT  
		Size: 38.2 MB (38222823 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43ec676fe798b3fc0426feeeb4fb25b636d3dedf7cff93007f9e1941bf91249f`  
		Last Modified: Thu, 04 Dec 2025 19:46:38 GMT  
		Size: 30.9 MB (30855171 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12cc521c9d0c4db0b965c0dc7b34a658f37301b6ce847f2ae95063a7f997e713`  
		Last Modified: Thu, 04 Dec 2025 19:46:22 GMT  
		Size: 53.8 MB (53815554 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cde8ef87532b408fc2bd228eaea1434c41a54fc8e6dea7dbadff9028ebc09446`  
		Last Modified: Thu, 04 Dec 2025 19:46:12 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60e1ff55a59dcacbb0924c7635bb363ee443cbb8e28653d25187b189397b6836`  
		Last Modified: Thu, 04 Dec 2025 19:46:12 GMT  
		Size: 2.3 KB (2314 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8627ebe214388955c92800971aeb31f7041346f8f24471600a829782623ea96`  
		Last Modified: Thu, 04 Dec 2025 20:06:27 GMT  
		Size: 1.7 KB (1710 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c48fd692ee17bec60268d1dcd8347299fdfcb9bafbce3ab75a6e470389f238a`  
		Last Modified: Thu, 04 Dec 2025 20:06:30 GMT  
		Size: 36.1 MB (36051383 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae781259fcdb632c6eb1c590d5a6c55374fe454ef99829650b38bf43ea6b5d94`  
		Last Modified: Sat, 06 Dec 2025 03:13:12 GMT  
		Size: 128.5 MB (128469417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf3117d3d4eb576bc69e64ca420443751ff90c60619020f097cce501099510d1`  
		Last Modified: Thu, 04 Dec 2025 20:06:27 GMT  
		Size: 59.5 KB (59524 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:7-jdk8-ubi9` - unknown; unknown

```console
$ docker pull gradle@sha256:7ff21957509eb047d5e62742a5cd63e65efd5a5669e673f5d96119ab0ebc3c1a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5458605 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1abb3338016cf75e79cc97fd9e244ffe7c1f1f9315a529c3cb85df33eb59fe64`

```dockerfile
```

-	Layers:
	-	`sha256:0a7796caf572337a46eea7b7822fcb2186c3a0c9b5c32995fd5e12324afc0c79`  
		Last Modified: Thu, 04 Dec 2025 21:19:43 GMT  
		Size: 5.4 MB (5434878 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d14fec7175c56d642ddae66f43154960daf7331b1977e9e11fd5cf4ec1360467`  
		Last Modified: Thu, 04 Dec 2025 21:19:43 GMT  
		Size: 23.7 KB (23727 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:7-jdk8-ubi9` - linux; ppc64le

```console
$ docker pull gradle@sha256:448d73c7d3d8348fd4b192bdccab3fb3084e87aa489b46c0a21a59723b685a87
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **295.9 MB (295899824 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:74cfa49dc4bc4706e0b5ccd2a5c7da81ef9b7c62575ee3811356422f9024466d`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["gradle"]`

```dockerfile
# Wed, 03 Dec 2025 20:38:00 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 03 Dec 2025 20:38:00 GMT
LABEL vendor="Red Hat, Inc."
# Wed, 03 Dec 2025 20:38:00 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Wed, 03 Dec 2025 20:38:00 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.7"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Wed, 03 Dec 2025 20:38:00 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 03 Dec 2025 20:38:00 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Wed, 03 Dec 2025 20:38:00 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 03 Dec 2025 20:38:00 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 03 Dec 2025 20:38:00 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Wed, 03 Dec 2025 20:38:00 GMT
LABEL io.openshift.expose-services=""
# Wed, 03 Dec 2025 20:38:00 GMT
LABEL io.openshift.tags="minimal rhel9"
# Wed, 03 Dec 2025 20:38:00 GMT
ENV container oci
# Wed, 03 Dec 2025 20:38:01 GMT
COPY dir:1944394b2cb85c8bd1da6ad676bb75b09725617f627438630bb53946c4695c4a in /      
# Wed, 03 Dec 2025 20:38:01 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Wed, 03 Dec 2025 20:38:01 GMT
CMD ["/bin/bash"]
# Wed, 03 Dec 2025 20:38:01 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /usr/share/buildinfo/content-sets.json      
# Wed, 03 Dec 2025 20:38:01 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /root/buildinfo/content_manifests/content-sets.json      
# Wed, 03 Dec 2025 20:38:01 GMT
COPY file:e9df47e0f73aa3fdb7704b0b5f90208619f4101460f662007af9ba5df5a06a9e in /usr/share/buildinfo/labels.json      
# Wed, 03 Dec 2025 20:38:01 GMT
COPY file:e9df47e0f73aa3fdb7704b0b5f90208619f4101460f662007af9ba5df5a06a9e in /root/buildinfo/labels.json      
# Wed, 03 Dec 2025 20:38:01 GMT
LABEL "architecture"="ppc64le" "vcs-type"="git" "vcs-ref"="1595c1bf15cd4327d529f330e61327764327397e" "org.opencontainers.image.revision"="1595c1bf15cd4327d529f330e61327764327397e" "build-date"="2025-12-03T20:37:49Z" "org.opencontainers.image.created"="2025-12-03T20:37:49Z" "release"="1764794109"org.opencontainers.image.revision=1595c1bf15cd4327d529f330e61327764327397e,org.opencontainers.image.created=2025-12-03T20:37:49Z
# Thu, 04 Dec 2025 19:45:52 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 04 Dec 2025 19:45:52 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 04 Dec 2025 19:45:52 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 04 Dec 2025 19:45:52 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en     ;     microdnf clean all # buildkit
# Thu, 04 Dec 2025 19:45:52 GMT
ENV JAVA_VERSION=jdk8u472-b08
# Thu, 04 Dec 2025 19:46:02 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='e2aff19d85d2441e409d6cbdf12ef7c2acabb0de73bca4207947135dcaa935a2';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u472-b08/OpenJDK8U-jdk_aarch64_linux_hotspot_8u472b08.tar.gz';          ;;        ppc64le)          ESUM='eaf57a4564265583b0641c878bea8943d27ef110c096868f686dae179fb45d8f';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u472-b08/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u472b08.tar.gz';          ;;        x86_64)          ESUM='5becaa4ac660e844c5a39e2ebc39ff5ac824c37ff1b625af8c8b111dc13c3592';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u472-b08/OpenJDK8U-jdk_x64_linux_hotspot_8u472b08.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip; # buildkit
# Thu, 04 Dec 2025 19:46:04 GMT
RUN set -eux;     echo "Verifying install ...";     echo "javac -version"; javac -version;     echo "java -version"; java -version;     echo "Complete." # buildkit
# Thu, 04 Dec 2025 19:46:05 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 04 Dec 2025 19:46:05 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 04 Dec 2025 20:10:44 GMT
CMD ["gradle"]
# Thu, 04 Dec 2025 20:10:44 GMT
ENV GRADLE_HOME=/opt/gradle
# Thu, 04 Dec 2025 20:10:44 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 101 gradle     && useradd --system --gid gradle --uid 101 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Thu, 04 Dec 2025 20:10:44 GMT
VOLUME [/home/gradle/.gradle]
# Thu, 04 Dec 2025 20:10:45 GMT
WORKDIR /home/gradle
# Thu, 04 Dec 2025 20:11:05 GMT
RUN set -o errexit -o nounset     && microdnf install -y         make                 findutils                 unzip         which                 git         git-lfs         subversion     && microdnf clean all         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which svn # buildkit
# Thu, 04 Dec 2025 20:11:05 GMT
ENV GRADLE_VERSION=7.6.6
# Thu, 04 Dec 2025 20:11:05 GMT
ARG GRADLE_DOWNLOAD_SHA256=673d9776f303bc7048fc3329d232d6ebf1051b07893bd9d11616fad9a8673be0
# Thu, 04 Dec 2025 20:13:01 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=673d9776f303bc7048fc3329d232d6ebf1051b07893bd9d11616fad9a8673be0
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Thu, 04 Dec 2025 20:13:01 GMT
USER gradle
# Thu, 04 Dec 2025 20:13:07 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=673d9776f303bc7048fc3329d232d6ebf1051b07893bd9d11616fad9a8673be0
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Thu, 04 Dec 2025 20:13:07 GMT
USER root
```

-	Layers:
	-	`sha256:0dbaabed7cc8118dfa57a21ab03f83f55ba784110782e2081afc710ef3eb3c16`  
		Last Modified: Thu, 04 Dec 2025 00:10:07 GMT  
		Size: 44.4 MB (44445850 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5bbc041c92aa38c134e96bedbac7c177760045bc5616488fd3fda3e26cca1a60`  
		Last Modified: Thu, 04 Dec 2025 19:46:52 GMT  
		Size: 32.9 MB (32890492 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5be981d78ff474337627c1818baada0068c41f6d548ca2498e2a5ae34de807f`  
		Last Modified: Thu, 04 Dec 2025 19:46:58 GMT  
		Size: 52.2 MB (52175843 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95b913ac54b70e89f669c894f683f01eda37a6620d448aef1f81377704dfe8b5`  
		Last Modified: Thu, 04 Dec 2025 19:46:49 GMT  
		Size: 130.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb24c161862c2a4a0cd62cd5dc5e55f2587ee36d66ccf679bcd929fb5e910b68`  
		Last Modified: Thu, 04 Dec 2025 19:46:49 GMT  
		Size: 2.3 KB (2316 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88009bd22eb9db46b7c23909c617af363188bb2b1e2ae15f4297728cc01214cd`  
		Last Modified: Thu, 04 Dec 2025 20:12:04 GMT  
		Size: 1.7 KB (1707 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3eb64a3d5b2224973fe13ddcb97f7305830ab6754e96bd2dd8e1fbd42cbf0802`  
		Last Modified: Thu, 04 Dec 2025 20:12:21 GMT  
		Size: 37.9 MB (37879030 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1aea759a24dc027725df365d3a70d6005c77a08df75aa3919e0a677973df622a`  
		Last Modified: Thu, 04 Dec 2025 20:13:43 GMT  
		Size: 128.5 MB (128469419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67bcde04cc8b0b7d2bc67240b215d93d6677eca2e2e1472e56617a4f168f7ed3`  
		Last Modified: Thu, 04 Dec 2025 20:13:55 GMT  
		Size: 35.0 KB (35005 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:7-jdk8-ubi9` - unknown; unknown

```console
$ docker pull gradle@sha256:a93186ef2828903e00142f4e5e981890fbe124c04da418a024166d6e163df584
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5456306 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb24c1719992a69aaca8aa90e7ea0870124eb1ec0452c6bc9ea70beedef60fab`

```dockerfile
```

-	Layers:
	-	`sha256:0ff7a3201639cf9e734c712ee3065ed410af2a181e9c0d9dfa27fac5b3b91377`  
		Last Modified: Thu, 04 Dec 2025 21:19:49 GMT  
		Size: 5.4 MB (5432690 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6446eee542c6bd6f3ecd2a91662f70ac5b9f5f56d76bea70e285f21f5b355ff3`  
		Last Modified: Thu, 04 Dec 2025 21:19:50 GMT  
		Size: 23.6 KB (23616 bytes)  
		MIME: application/vnd.in-toto+json
