## `gradle:9-jdk17-ubi9`

```console
$ docker pull gradle@sha256:3207fd3de5731a9164e79d687af512d64550a8ba772fc0d455aaeca1017c0fef
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

### `gradle:9-jdk17-ubi9` - linux; amd64

```console
$ docker pull gradle@sha256:48f7332af5a382e7f70926a0988516e851980b2e78d5febbaba9b72d35349188
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **389.6 MB (389565791 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d4b1e37a64663e1a8eac23d1bb681cf1019790da364ba14d449cdf99546cd2e8`
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
# Thu, 04 Dec 2025 19:47:18 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 04 Dec 2025 19:47:18 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 04 Dec 2025 19:47:18 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 04 Dec 2025 19:47:18 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en     ;     microdnf clean all # buildkit
# Thu, 04 Dec 2025 19:47:18 GMT
ENV JAVA_VERSION=jdk-17.0.17+10
# Thu, 04 Dec 2025 19:47:24 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='dc29ca6d35beb4419b4b00419b8a3dfbf5ae551e1ae2b046b516d9a579d04533';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jdk_aarch64_linux_hotspot_17.0.17_10.tar.gz';          ;;        ppc64le)          ESUM='2a29d1be61940c1bd639018c07f4622e1f145a7ef34e7294fee877e39226d9da';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jdk_ppc64le_linux_hotspot_17.0.17_10.tar.gz';          ;;        s390x)          ESUM='76327b1d00c67f6be91717754fd85fc85ce496d48876f69accb9c53ed31dc546';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jdk_s390x_linux_hotspot_17.0.17_10.tar.gz';          ;;        x86_64)          ESUM='992f96e7995075ac7636bb1a8de52b0c61d71ed3137fafc979ab96b4ab78dd75';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jdk_x64_linux_hotspot_17.0.17_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Thu, 04 Dec 2025 19:47:25 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 04 Dec 2025 19:47:25 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 04 Dec 2025 19:47:25 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 04 Dec 2025 19:47:25 GMT
CMD ["jshell"]
# Fri, 16 Jan 2026 21:44:07 GMT
CMD ["gradle"]
# Fri, 16 Jan 2026 21:44:07 GMT
ENV GRADLE_HOME=/opt/gradle
# Fri, 16 Jan 2026 21:44:07 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 101 gradle     && useradd --system --gid gradle --uid 101 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Fri, 16 Jan 2026 21:44:07 GMT
VOLUME [/home/gradle/.gradle]
# Fri, 16 Jan 2026 21:44:07 GMT
WORKDIR /home/gradle
# Fri, 16 Jan 2026 21:44:11 GMT
RUN set -o errexit -o nounset     && microdnf install -y         make         curl-minimal         wget         tar                 findutils                 unzip         which                 git         git-lfs         subversion     && microdnf clean all         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which svn # buildkit
# Fri, 16 Jan 2026 21:44:11 GMT
ENV GRADLE_VERSION=9.3.0
# Fri, 16 Jan 2026 21:44:11 GMT
ARG GRADLE_DOWNLOAD_SHA256=0d585f69da091fc5b2beced877feab55a3064d43b8a1d46aeb07996b0915e0e0
# Fri, 16 Jan 2026 21:44:14 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=0d585f69da091fc5b2beced877feab55a3064d43b8a1d46aeb07996b0915e0e0
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Fri, 16 Jan 2026 21:44:14 GMT
USER gradle
# Fri, 16 Jan 2026 21:44:14 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=0d585f69da091fc5b2beced877feab55a3064d43b8a1d46aeb07996b0915e0e0
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --stacktrace --debug --version # buildkit
# Fri, 16 Jan 2026 21:44:14 GMT
USER root
```

-	Layers:
	-	`sha256:46a9484471e55e0e501c08ff903616330af0505ba749ef70e8c87e103e07844a`  
		Last Modified: Wed, 03 Dec 2025 21:15:19 GMT  
		Size: 40.0 MB (40040759 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e6671b1c1191b3333fc37f79dd95091f26abc5a2c8373c49b829dcf52a02ef0`  
		Last Modified: Thu, 04 Dec 2025 19:47:53 GMT  
		Size: 30.4 MB (30411081 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d31c91bb9b2c181723b60b7bdd54f5308ec5e87f9469b9ab133f3c917f36bc7`  
		Last Modified: Thu, 04 Dec 2025 20:01:36 GMT  
		Size: 144.9 MB (144852854 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:572ee62225e94dd5ff5e33de0a94ae30843d5cb85c289159c0c40be11e01ef77`  
		Last Modified: Thu, 04 Dec 2025 19:47:50 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aff0a6832e5e0a48f0d7c45a45c6e6ce54406e048fc70bf5badfbd4a044ce42a`  
		Last Modified: Thu, 04 Dec 2025 19:47:51 GMT  
		Size: 2.3 KB (2291 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d95fd0bffa2a9bf7d07993d557082da69f8c7896e3a3745c6d4804160834808`  
		Last Modified: Fri, 16 Jan 2026 21:44:40 GMT  
		Size: 1.7 KB (1716 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb9945909fc4af1f72cdb3237969fa6d57b64f996c761c61279e2a30e9d42c95`  
		Last Modified: Fri, 16 Jan 2026 21:44:43 GMT  
		Size: 37.2 MB (37242456 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e857f822ad15523816ca2230f6380cb44f727c4a69bb7964f87d5386091bd845`  
		Last Modified: Fri, 16 Jan 2026 21:45:06 GMT  
		Size: 137.0 MB (136988880 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0cf357d1715afbbfe03da47992c66ee7f3b6eb588fa7d420dc3e6e58461ca4b5`  
		Last Modified: Fri, 16 Jan 2026 21:44:40 GMT  
		Size: 25.6 KB (25593 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:9-jdk17-ubi9` - unknown; unknown

```console
$ docker pull gradle@sha256:9a780980c76e10882f99d405b6b873232dd169ecf31f3c9573074d5d23f47f68
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5408342 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb0db8010a9373d64138cde7382d496c521d8200fae74bbd4155619cca133383`

```dockerfile
```

-	Layers:
	-	`sha256:782dff30f2d276a0c1e3c143f8c87b0f920a35a13874f33b05d81c30171e269a`  
		Last Modified: Sat, 17 Jan 2026 00:25:01 GMT  
		Size: 5.4 MB (5385143 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0ed76cb637f29dc4e5b3c84497befb89e4f7b7d933598d2f10fe5e1ed57e144c`  
		Last Modified: Fri, 16 Jan 2026 21:44:30 GMT  
		Size: 23.2 KB (23199 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:9-jdk17-ubi9` - linux; arm64 variant v8

```console
$ docker pull gradle@sha256:23f25cad1f2387adedfbbd3235f2a0971b489b776d96bc553c54aa40d045c01a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **386.4 MB (386354867 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b23d0b52360f0ba68dd7c08cb16399e134aef19857d3e03066bae3eeb4d0e868`
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
# Thu, 04 Dec 2025 19:46:21 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 04 Dec 2025 19:46:21 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 04 Dec 2025 19:46:21 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 04 Dec 2025 19:46:21 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en     ;     microdnf clean all # buildkit
# Thu, 04 Dec 2025 19:46:21 GMT
ENV JAVA_VERSION=jdk-17.0.17+10
# Thu, 04 Dec 2025 19:47:51 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='dc29ca6d35beb4419b4b00419b8a3dfbf5ae551e1ae2b046b516d9a579d04533';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jdk_aarch64_linux_hotspot_17.0.17_10.tar.gz';          ;;        ppc64le)          ESUM='2a29d1be61940c1bd639018c07f4622e1f145a7ef34e7294fee877e39226d9da';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jdk_ppc64le_linux_hotspot_17.0.17_10.tar.gz';          ;;        s390x)          ESUM='76327b1d00c67f6be91717754fd85fc85ce496d48876f69accb9c53ed31dc546';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jdk_s390x_linux_hotspot_17.0.17_10.tar.gz';          ;;        x86_64)          ESUM='992f96e7995075ac7636bb1a8de52b0c61d71ed3137fafc979ab96b4ab78dd75';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jdk_x64_linux_hotspot_17.0.17_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Thu, 04 Dec 2025 19:47:52 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 04 Dec 2025 19:47:52 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 04 Dec 2025 19:47:52 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 04 Dec 2025 19:47:52 GMT
CMD ["jshell"]
# Fri, 16 Jan 2026 21:46:47 GMT
CMD ["gradle"]
# Fri, 16 Jan 2026 21:46:47 GMT
ENV GRADLE_HOME=/opt/gradle
# Fri, 16 Jan 2026 21:46:47 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 101 gradle     && useradd --system --gid gradle --uid 101 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Fri, 16 Jan 2026 21:46:47 GMT
VOLUME [/home/gradle/.gradle]
# Fri, 16 Jan 2026 21:46:47 GMT
WORKDIR /home/gradle
# Fri, 16 Jan 2026 21:46:51 GMT
RUN set -o errexit -o nounset     && microdnf install -y         make         curl-minimal         wget         tar                 findutils                 unzip         which                 git         git-lfs         subversion     && microdnf clean all         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which svn # buildkit
# Fri, 16 Jan 2026 21:46:51 GMT
ENV GRADLE_VERSION=9.3.0
# Fri, 16 Jan 2026 21:46:51 GMT
ARG GRADLE_DOWNLOAD_SHA256=0d585f69da091fc5b2beced877feab55a3064d43b8a1d46aeb07996b0915e0e0
# Fri, 16 Jan 2026 21:46:54 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=0d585f69da091fc5b2beced877feab55a3064d43b8a1d46aeb07996b0915e0e0
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Fri, 16 Jan 2026 21:46:54 GMT
USER gradle
# Fri, 16 Jan 2026 21:46:55 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=0d585f69da091fc5b2beced877feab55a3064d43b8a1d46aeb07996b0915e0e0
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --stacktrace --debug --version # buildkit
# Fri, 16 Jan 2026 21:46:55 GMT
USER root
```

-	Layers:
	-	`sha256:15f4b55884339bddb52ca0550d5b1208576ecf31649e067b468dc4e7b90745bd`  
		Last Modified: Wed, 03 Dec 2025 22:01:09 GMT  
		Size: 38.2 MB (38222823 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c83cee7c71c9193c071c958a345e3a74f08ba26ec78d7cbec425ae44c673214d`  
		Last Modified: Thu, 04 Dec 2025 19:47:04 GMT  
		Size: 30.9 MB (30855151 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96ae1953fee8ba7617291cc265a9b6cdacb3397c42e6e9569d0aacfdf459b8ea`  
		Last Modified: Thu, 04 Dec 2025 19:48:13 GMT  
		Size: 143.7 MB (143685374 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f61afefb6ed9b072acbe1b3406f63bfe4f48916f499dc7c2497cc3488b15cbf1`  
		Last Modified: Thu, 04 Dec 2025 19:48:18 GMT  
		Size: 131.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab2e5e473be9c84bc7113fc8758ba71ce89fa40641022ec8e730382d4665eeed`  
		Last Modified: Thu, 04 Dec 2025 19:48:21 GMT  
		Size: 2.3 KB (2290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39d264a1e8dcb47bb72da3b201fb500600ec885b772198e867b8220919b2f291`  
		Last Modified: Fri, 16 Jan 2026 21:47:11 GMT  
		Size: 1.7 KB (1717 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6dc00ea26d34008bcbc3e7dad0af566b6c9f870708dd66f0bdc370ebf019025`  
		Last Modified: Fri, 16 Jan 2026 21:47:25 GMT  
		Size: 36.6 MB (36569156 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5d43f4ef263b4fd6c0c8a937fde7f3d3eec691e508b5238d93f1ad906285f40`  
		Last Modified: Fri, 16 Jan 2026 21:47:34 GMT  
		Size: 137.0 MB (136988873 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82ac0fd50aadbed5230d10af3bcbd00d1bb4ca2895661c5e7d1181a2ddf33d1d`  
		Last Modified: Fri, 16 Jan 2026 21:47:22 GMT  
		Size: 29.3 KB (29320 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:9-jdk17-ubi9` - unknown; unknown

```console
$ docker pull gradle@sha256:b53623edcbea6ab9b913c541f39772ce0d0b81ceb35cada1e4566c24aebeadf7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5407874 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f5718bef92f36340cd63e8f768b8d9ddce5f5dbcbbe159a7ca0c4f388ffe932d`

```dockerfile
```

-	Layers:
	-	`sha256:fbdd5a827170e83448bfae346b7858976bf5a1ce574db86dbbb0890fd8665db9`  
		Last Modified: Fri, 16 Jan 2026 21:47:12 GMT  
		Size: 5.4 MB (5384525 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:273ba284134996f16f26bf3d6ea23157f11929e5b6b691a0b161e498fcaaaf4a`  
		Last Modified: Sat, 17 Jan 2026 00:25:08 GMT  
		Size: 23.3 KB (23349 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:9-jdk17-ubi9` - linux; ppc64le

```console
$ docker pull gradle@sha256:945ea3ff126bed199b1840dbaca3e762a215ac89f439fc2a400c20e07adf17f8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **397.4 MB (397397376 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ce504c5e6cf0b2f90e9decf457d50bc56df4924346536d8db4b2a1ac8a934670`
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
ENV JAVA_VERSION=jdk-17.0.17+10
# Thu, 04 Dec 2025 19:49:05 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='dc29ca6d35beb4419b4b00419b8a3dfbf5ae551e1ae2b046b516d9a579d04533';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jdk_aarch64_linux_hotspot_17.0.17_10.tar.gz';          ;;        ppc64le)          ESUM='2a29d1be61940c1bd639018c07f4622e1f145a7ef34e7294fee877e39226d9da';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jdk_ppc64le_linux_hotspot_17.0.17_10.tar.gz';          ;;        s390x)          ESUM='76327b1d00c67f6be91717754fd85fc85ce496d48876f69accb9c53ed31dc546';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jdk_s390x_linux_hotspot_17.0.17_10.tar.gz';          ;;        x86_64)          ESUM='992f96e7995075ac7636bb1a8de52b0c61d71ed3137fafc979ab96b4ab78dd75';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jdk_x64_linux_hotspot_17.0.17_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Thu, 04 Dec 2025 19:49:09 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 04 Dec 2025 19:49:10 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 04 Dec 2025 19:49:10 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 04 Dec 2025 19:49:10 GMT
CMD ["jshell"]
# Fri, 16 Jan 2026 21:54:08 GMT
CMD ["gradle"]
# Fri, 16 Jan 2026 21:54:08 GMT
ENV GRADLE_HOME=/opt/gradle
# Fri, 16 Jan 2026 21:54:08 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 101 gradle     && useradd --system --gid gradle --uid 101 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Fri, 16 Jan 2026 21:54:08 GMT
VOLUME [/home/gradle/.gradle]
# Fri, 16 Jan 2026 21:54:09 GMT
WORKDIR /home/gradle
# Fri, 16 Jan 2026 21:54:36 GMT
RUN set -o errexit -o nounset     && microdnf install -y         make         curl-minimal         wget         tar                 findutils                 unzip         which                 git         git-lfs         subversion     && microdnf clean all         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which svn # buildkit
# Fri, 16 Jan 2026 21:54:36 GMT
ENV GRADLE_VERSION=9.3.0
# Fri, 16 Jan 2026 21:54:36 GMT
ARG GRADLE_DOWNLOAD_SHA256=0d585f69da091fc5b2beced877feab55a3064d43b8a1d46aeb07996b0915e0e0
# Fri, 16 Jan 2026 21:54:43 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=0d585f69da091fc5b2beced877feab55a3064d43b8a1d46aeb07996b0915e0e0
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Fri, 16 Jan 2026 21:54:43 GMT
USER gradle
# Fri, 16 Jan 2026 21:54:45 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=0d585f69da091fc5b2beced877feab55a3064d43b8a1d46aeb07996b0915e0e0
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --stacktrace --debug --version # buildkit
# Fri, 16 Jan 2026 21:54:45 GMT
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
	-	`sha256:e57935f65a499dbb7928a1974ec7e4e0e7b5ce8789b616c913141f8eb3db8911`  
		Last Modified: Thu, 04 Dec 2025 19:49:50 GMT  
		Size: 144.5 MB (144547856 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6d68fd9816d6c17694b7f8d45afad7b27c1a49204bce080145bbc0355d09e97`  
		Last Modified: Thu, 04 Dec 2025 19:49:46 GMT  
		Size: 131.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f404c6acd8c75fa36f3c1ba86abb138c17956ea0f0f1130fd76126182061330`  
		Last Modified: Thu, 04 Dec 2025 19:49:56 GMT  
		Size: 2.3 KB (2291 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17a299f74e838e57dd59e7c0e64931f87d826820b291e8904812ccaf2d80606c`  
		Last Modified: Fri, 16 Jan 2026 21:55:40 GMT  
		Size: 1.7 KB (1719 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79ab0f5b4b41ff866053588c46ad137a10f6717d7597a90878e7154fe924cfe0`  
		Last Modified: Fri, 16 Jan 2026 21:55:31 GMT  
		Size: 38.5 MB (38519755 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89501f75d5d57e065d28a7bcbbf80b025404bbfbcb74a92b9f5f6a5e79fee4fc`  
		Last Modified: Fri, 16 Jan 2026 21:55:54 GMT  
		Size: 137.0 MB (136988874 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9fc7c5a51b2faf17d7ee11404cf5b0ffa73d7ad01f9bf5d862a20355022e15a`  
		Last Modified: Fri, 16 Jan 2026 21:55:29 GMT  
		Size: 376.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:9-jdk17-ubi9` - unknown; unknown

```console
$ docker pull gradle@sha256:67a10bab34dba35d53034fd9f3ad7247f6d889b2289422d38d090e1f336e5552
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5405702 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd4bec3d5bde3e7b3f925682f922870b4907ad220ef7ebbd95b442a5cd4c194d`

```dockerfile
```

-	Layers:
	-	`sha256:4b53f03b30891630c118cfcf9109b519f857edccecd264fa44e4d69fe3d159fb`  
		Last Modified: Sat, 17 Jan 2026 00:25:14 GMT  
		Size: 5.4 MB (5382454 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:66f584fa85cc6f439532b209ce8f3c061fbc535614042019ea34ee5a8f759d28`  
		Last Modified: Fri, 16 Jan 2026 21:55:29 GMT  
		Size: 23.2 KB (23248 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:9-jdk17-ubi9` - linux; s390x

```console
$ docker pull gradle@sha256:f01f7d3ff30559d4698de0832797450a0e8241c092d40148a85ff8e42029df2d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **377.3 MB (377317665 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6704f90aeeb003316eb95744ed8179880f7f6ada564609cb59c9335d6b642554`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["gradle"]`

```dockerfile
# Wed, 03 Dec 2025 20:42:43 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 03 Dec 2025 20:42:43 GMT
LABEL vendor="Red Hat, Inc."
# Wed, 03 Dec 2025 20:42:43 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Wed, 03 Dec 2025 20:42:43 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.7"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Wed, 03 Dec 2025 20:42:43 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 03 Dec 2025 20:42:43 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Wed, 03 Dec 2025 20:42:43 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 03 Dec 2025 20:42:43 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 03 Dec 2025 20:42:43 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Wed, 03 Dec 2025 20:42:43 GMT
LABEL io.openshift.expose-services=""
# Wed, 03 Dec 2025 20:42:43 GMT
LABEL io.openshift.tags="minimal rhel9"
# Wed, 03 Dec 2025 20:42:43 GMT
ENV container oci
# Wed, 03 Dec 2025 20:42:44 GMT
COPY dir:10eb0792500239f5e33d6b6b7941aff62593a46d7fd8ece7d8112154ea3105b1 in /      
# Wed, 03 Dec 2025 20:42:44 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Wed, 03 Dec 2025 20:42:44 GMT
CMD ["/bin/bash"]
# Wed, 03 Dec 2025 20:42:44 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /usr/share/buildinfo/content-sets.json      
# Wed, 03 Dec 2025 20:42:44 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /root/buildinfo/content_manifests/content-sets.json      
# Wed, 03 Dec 2025 20:42:44 GMT
COPY file:f78d6df7f6c9ff8f12b4cd77c81f39d3e176ca1a669ebe7b8a04c5beb6be6145 in /usr/share/buildinfo/labels.json      
# Wed, 03 Dec 2025 20:42:44 GMT
COPY file:f78d6df7f6c9ff8f12b4cd77c81f39d3e176ca1a669ebe7b8a04c5beb6be6145 in /root/buildinfo/labels.json      
# Wed, 03 Dec 2025 20:42:44 GMT
LABEL "architecture"="s390x" "vcs-type"="git" "vcs-ref"="1595c1bf15cd4327d529f330e61327764327397e" "org.opencontainers.image.revision"="1595c1bf15cd4327d529f330e61327764327397e" "build-date"="2025-12-03T20:42:32Z" "org.opencontainers.image.created"="2025-12-03T20:42:32Z" "release"="1764794109"org.opencontainers.image.revision=1595c1bf15cd4327d529f330e61327764327397e,org.opencontainers.image.created=2025-12-03T20:42:32Z
# Thu, 04 Dec 2025 19:45:27 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 04 Dec 2025 19:45:27 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 04 Dec 2025 19:45:27 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 04 Dec 2025 19:45:27 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en     ;     microdnf clean all # buildkit
# Thu, 04 Dec 2025 19:45:27 GMT
ENV JAVA_VERSION=jdk-17.0.17+10
# Thu, 04 Dec 2025 19:45:35 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='dc29ca6d35beb4419b4b00419b8a3dfbf5ae551e1ae2b046b516d9a579d04533';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jdk_aarch64_linux_hotspot_17.0.17_10.tar.gz';          ;;        ppc64le)          ESUM='2a29d1be61940c1bd639018c07f4622e1f145a7ef34e7294fee877e39226d9da';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jdk_ppc64le_linux_hotspot_17.0.17_10.tar.gz';          ;;        s390x)          ESUM='76327b1d00c67f6be91717754fd85fc85ce496d48876f69accb9c53ed31dc546';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jdk_s390x_linux_hotspot_17.0.17_10.tar.gz';          ;;        x86_64)          ESUM='992f96e7995075ac7636bb1a8de52b0c61d71ed3137fafc979ab96b4ab78dd75';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jdk_x64_linux_hotspot_17.0.17_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Thu, 04 Dec 2025 19:45:38 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 04 Dec 2025 19:45:38 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 04 Dec 2025 19:45:38 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 04 Dec 2025 19:45:38 GMT
CMD ["jshell"]
# Fri, 16 Jan 2026 21:46:23 GMT
CMD ["gradle"]
# Fri, 16 Jan 2026 21:46:23 GMT
ENV GRADLE_HOME=/opt/gradle
# Fri, 16 Jan 2026 21:46:23 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 101 gradle     && useradd --system --gid gradle --uid 101 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Fri, 16 Jan 2026 21:46:23 GMT
VOLUME [/home/gradle/.gradle]
# Fri, 16 Jan 2026 21:46:23 GMT
WORKDIR /home/gradle
# Fri, 16 Jan 2026 21:46:31 GMT
RUN set -o errexit -o nounset     && microdnf install -y         make         curl-minimal         wget         tar                 findutils                 unzip         which                 git         git-lfs         subversion     && microdnf clean all         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which svn # buildkit
# Fri, 16 Jan 2026 21:46:31 GMT
ENV GRADLE_VERSION=9.3.0
# Fri, 16 Jan 2026 21:46:31 GMT
ARG GRADLE_DOWNLOAD_SHA256=0d585f69da091fc5b2beced877feab55a3064d43b8a1d46aeb07996b0915e0e0
# Fri, 16 Jan 2026 21:46:34 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=0d585f69da091fc5b2beced877feab55a3064d43b8a1d46aeb07996b0915e0e0
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Fri, 16 Jan 2026 21:46:34 GMT
USER gradle
# Fri, 16 Jan 2026 21:46:35 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=0d585f69da091fc5b2beced877feab55a3064d43b8a1d46aeb07996b0915e0e0
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --stacktrace --debug --version # buildkit
# Fri, 16 Jan 2026 21:46:35 GMT
USER root
```

-	Layers:
	-	`sha256:8d6bf9619dce2b1902cecb7448c5bfe74272c22bbdc9eb02a2de550b72a7db66`  
		Last Modified: Thu, 04 Dec 2025 00:10:07 GMT  
		Size: 38.1 MB (38133803 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f32d5166444cb69244412d0ff236358d3d5c91712123606bd5849ef6a3411abf`  
		Last Modified: Thu, 04 Dec 2025 19:46:19 GMT  
		Size: 30.4 MB (30445196 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ee2c82989d7b9b7a5a11dae268443c86b6e5cb7c89e5b43217106329ce9a9b7`  
		Last Modified: Thu, 04 Dec 2025 20:02:40 GMT  
		Size: 134.9 MB (134862168 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efe85d8deefa2a670c76e0e0552899c517928f00c5f9f0ca713ad05e99e57b8c`  
		Last Modified: Thu, 04 Dec 2025 19:46:20 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3617aaba8f919a1727faec1d918fb0d302af41426639cba557cbaa995977ca48`  
		Last Modified: Thu, 04 Dec 2025 19:46:20 GMT  
		Size: 2.3 KB (2290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25865cebef8f18100c8ccff69756366e9736dbaa34f6c38a56176c4246ca5ba0`  
		Last Modified: Fri, 16 Jan 2026 21:47:08 GMT  
		Size: 1.7 KB (1715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f08049042d218888faca12553b65b2e28bcd98b0c8d113b362b07842c4cbc15`  
		Last Modified: Fri, 16 Jan 2026 21:47:00 GMT  
		Size: 36.9 MB (36883081 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92b6dbcdb7c2e1a79ba26ddfa71e2d99d2fb6e42f757ba2c0308522677e3dfd2`  
		Last Modified: Sun, 18 Jan 2026 16:07:12 GMT  
		Size: 137.0 MB (136988875 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35efde1115b3260526f7ab6a6a53b2bf8b60c4b075e7fe40f49bf7b231790388`  
		Last Modified: Fri, 16 Jan 2026 21:47:08 GMT  
		Size: 376.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:9-jdk17-ubi9` - unknown; unknown

```console
$ docker pull gradle@sha256:bf6be719fb057c42c55481ba0f4f65b98480068e41c344340af3c5f85492393d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5394946 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2de209e9075eb83e6a3c3d3c1ae44f5060021b965ac76d39317971e921707a8c`

```dockerfile
```

-	Layers:
	-	`sha256:794dbb15739682bc4c70632d3043549413d20217d35d247c8a35ffc504e4abea`  
		Last Modified: Sat, 17 Jan 2026 00:25:26 GMT  
		Size: 5.4 MB (5371748 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:64b631d1042aa4f9b3e49904bf927a7e6ee2e04e8ebf6c93d442ab6b110b2552`  
		Last Modified: Fri, 16 Jan 2026 21:46:59 GMT  
		Size: 23.2 KB (23198 bytes)  
		MIME: application/vnd.in-toto+json
