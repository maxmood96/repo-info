## `gradle:ubi10`

```console
$ docker pull gradle@sha256:17ea959bd2a402a7d0900113125272ec3757142beb9830c62a8bec0e1dcd6eb9
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

### `gradle:ubi10` - linux; amd64

```console
$ docker pull gradle@sha256:d9b79ccbd3e894ece9a26a7599161654ba752ab43ff1dd046a37afe0679b32de
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **343.8 MB (343801778 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:05a829b592f398bf7116685b9bb060a552ab0520d691895aa3b6b11e39cecdf8`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["gradle"]`

```dockerfile
# Tue, 12 May 2026 09:09:41 GMT
LABEL maintainer="Red Hat, Inc."
# Tue, 12 May 2026 09:09:41 GMT
LABEL vendor="Red Hat, Inc."
# Tue, 12 May 2026 09:09:41 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Tue, 12 May 2026 09:09:41 GMT
LABEL com.redhat.component="ubi10-minimal-container"       name="ubi10/ubi-minimal"       version="10.1"       cpe="cpe:/o:redhat:enterprise_linux:10.1"       distribution-scope="public"
# Tue, 12 May 2026 09:09:41 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Tue, 12 May 2026 09:09:41 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 10."
# Tue, 12 May 2026 09:09:41 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Tue, 12 May 2026 09:09:41 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Tue, 12 May 2026 09:09:41 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 10 Minimal"
# Tue, 12 May 2026 09:09:41 GMT
LABEL io.openshift.expose-services=""
# Tue, 12 May 2026 09:09:41 GMT
LABEL io.openshift.tags="minimal rhel10"
# Tue, 12 May 2026 09:09:41 GMT
ENV container oci
# Tue, 12 May 2026 09:09:41 GMT
COPY dir:70c9e4dfd7df3debe1e0457260915a9c0446c87d882b979cfec229a5714bf4c7 in /      
# Tue, 12 May 2026 09:09:41 GMT
COPY file:5de33b5fc08b00635bccf9134a18978dba13e2250aa51838f9969515a3957847 in /etc/yum.repos.d/.      
# Tue, 12 May 2026 09:09:41 GMT
CMD ["/bin/bash"]
# Tue, 12 May 2026 09:09:42 GMT
COPY file:595171150af68abc798ea385f7988d74b566aa8e84babff137f00b08b2164683 in /usr/share/buildinfo/content-sets.json      
# Tue, 12 May 2026 09:09:42 GMT
COPY file:595171150af68abc798ea385f7988d74b566aa8e84babff137f00b08b2164683 in /root/buildinfo/content_manifests/content-sets.json      
# Tue, 12 May 2026 09:09:42 GMT
COPY file:0753abbd85f48d60c6079bc7ee41700b66d3abf1c27ef1da2779ce2ba16ca2c5 in /usr/share/buildinfo/labels.json      
# Tue, 12 May 2026 09:09:42 GMT
COPY file:0753abbd85f48d60c6079bc7ee41700b66d3abf1c27ef1da2779ce2ba16ca2c5 in /root/buildinfo/labels.json      
# Tue, 12 May 2026 09:09:42 GMT
LABEL "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="ad7cdeeb08da8825126b10f488e410b0de5902b0" "org.opencontainers.image.revision"="ad7cdeeb08da8825126b10f488e410b0de5902b0" "build-date"="2026-05-12T09:09:25Z" "org.opencontainers.image.created"="2026-05-12T09:09:25Z" "release"="1778576723"org.opencontainers.image.revision=ad7cdeeb08da8825126b10f488e410b0de5902b0,org.opencontainers.image.created=2026-05-12T09:09:25Z
# Tue, 12 May 2026 23:33:23 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 12 May 2026 23:33:23 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 May 2026 23:33:23 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 12 May 2026 23:33:23 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en         gnupg2     ;     microdnf clean all # buildkit
# Tue, 12 May 2026 23:33:23 GMT
ENV JAVA_VERSION=jdk-25.0.3+9
# Tue, 12 May 2026 23:34:03 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='3e4287cb98870ba824ed698854bdc27cff984254caf66dd12cc291e7bfdde26b';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.3%2B9/OpenJDK25U-jdk_aarch64_linux_hotspot_25.0.3_9.tar.gz';          ;;        ppc64le)          ESUM='72b0fbb201716ca465ab704ec0fb12971abab3fdde5ae8d03b125a273522cf05';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.3%2B9/OpenJDK25U-jdk_ppc64le_linux_hotspot_25.0.3_9.tar.gz';          ;;        s390x)          ESUM='24b497d10acb6ee706ca30e1c8a929785c250cad54c5c12f1f8f93c3c06a53f7';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.3%2B9/OpenJDK25U-jdk_s390x_linux_hotspot_25.0.3_9.tar.gz';          ;;        x86_64)          ESUM='69264a7a211bf5029830d07bc3370f879769d62ebc5b5488e90c9343a2da0e1f';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.3%2B9/OpenJDK25U-jdk_x64_linux_hotspot_25.0.3_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Tue, 12 May 2026 23:34:05 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 12 May 2026 23:34:05 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 12 May 2026 23:34:05 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 12 May 2026 23:34:05 GMT
CMD ["jshell"]
# Wed, 13 May 2026 00:12:34 GMT
CMD ["gradle"]
# Wed, 13 May 2026 00:12:34 GMT
ENV GRADLE_HOME=/opt/gradle
# Wed, 13 May 2026 00:12:34 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 101 gradle     && useradd --system --gid gradle --uid 101 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Wed, 13 May 2026 00:12:34 GMT
VOLUME [/home/gradle/.gradle]
# Wed, 13 May 2026 00:12:34 GMT
WORKDIR /home/gradle
# Wed, 13 May 2026 00:12:37 GMT
RUN set -o errexit -o nounset     && microdnf install -y         make         curl         wget         tar                 findutils                 unzip         which                 git         git-lfs         subversion     && microdnf clean all         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which svn # buildkit
# Wed, 13 May 2026 00:12:37 GMT
ENV GRADLE_VERSION=9.5.1
# Wed, 13 May 2026 00:12:37 GMT
ARG GRADLE_DOWNLOAD_SHA256=bafc141b619ad6350fd975fc903156dd5c151998cc8b058e8c1044ab5f7b031f
# Wed, 13 May 2026 00:12:40 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=bafc141b619ad6350fd975fc903156dd5c151998cc8b058e8c1044ab5f7b031f
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Wed, 13 May 2026 00:12:40 GMT
USER gradle
# Wed, 13 May 2026 00:12:40 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=bafc141b619ad6350fd975fc903156dd5c151998cc8b058e8c1044ab5f7b031f
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --stacktrace --debug --version # buildkit
# Wed, 13 May 2026 00:12:40 GMT
USER root
```

-	Layers:
	-	`sha256:20e8bbd1fa594932c31db6c97d64754bd505f260fa2792d4a021081374b77b54`  
		Last Modified: Tue, 12 May 2026 10:16:05 GMT  
		Size: 34.6 MB (34624258 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0d3f1bd2a9f8d1a33f319ef5cf58e41aa68e03e0effba2fed48090f6e3afcf9`  
		Last Modified: Tue, 12 May 2026 23:33:48 GMT  
		Size: 37.5 MB (37500978 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e9d32aefd0a4d2b0cdce509e50b29daeb09f06244f5f4cedf86727ed3b97d11`  
		Last Modified: Tue, 12 May 2026 23:34:22 GMT  
		Size: 92.6 MB (92579375 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a5fa3b410255f3b2b62f6ac3916ef23325954c85c394b39961e6ae602528c0b`  
		Last Modified: Tue, 12 May 2026 23:34:19 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:469c27ec93aaad33e08ab881f6ccf5572762a3131d409055b8451fc4e5cce1f0`  
		Last Modified: Tue, 12 May 2026 23:34:20 GMT  
		Size: 2.3 KB (2290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5b12d52df5a2f95413598a428958d3cf7eefa4d437b56ee3ef8954f1757101e`  
		Last Modified: Wed, 13 May 2026 00:12:59 GMT  
		Size: 1.6 KB (1586 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5bf86b5872ff60c8f80dc7c46822f412e1a01e5b3661db51b3c4ad405888409d`  
		Last Modified: Wed, 13 May 2026 00:13:00 GMT  
		Size: 38.8 MB (38830531 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4736ab5f188d25a6f2cb56d83e05aef83fd471cc7f4fa391b14b4745ff4a6f1f`  
		Last Modified: Wed, 13 May 2026 00:13:05 GMT  
		Size: 140.2 MB (140236986 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d77794c933fcf10748785d55580b044bea7cd0a08f2d9af29e3eea051503e59b`  
		Last Modified: Wed, 13 May 2026 00:12:59 GMT  
		Size: 25.6 KB (25613 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:ubi10` - unknown; unknown

```console
$ docker pull gradle@sha256:ca3bfe5988fd1c00493bbfa084dbeedfe459f14ca76ca8b61657b7841ae008be
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 MB (7049519 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:188fc3fcb059b205005d1764a4995d5415c2e85e74fbe1bdbc0e592d239e914d`

```dockerfile
```

-	Layers:
	-	`sha256:bdfea2ff911b37d9e5d578ed450cd5896e18491b69d64ce5750cd8d439571a9c`  
		Last Modified: Wed, 13 May 2026 00:12:59 GMT  
		Size: 7.0 MB (7024510 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:af565f3c35a6c468bd1482c9eef89b2b1f595182ffc46efa34d71deefaec74d3`  
		Last Modified: Wed, 13 May 2026 00:12:59 GMT  
		Size: 25.0 KB (25009 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:ubi10` - linux; arm64 variant v8

```console
$ docker pull gradle@sha256:730d80459bab1e9885382f3fc15f3d033a01c050fe743b9521d8e947c7f891bd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **340.3 MB (340296620 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0605d7e84d40b352e678392f8a880e15706798a627fbf9b15c0c9224900f009a`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["gradle"]`

```dockerfile
# Tue, 12 May 2026 09:11:34 GMT
LABEL maintainer="Red Hat, Inc."
# Tue, 12 May 2026 09:11:34 GMT
LABEL vendor="Red Hat, Inc."
# Tue, 12 May 2026 09:11:34 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Tue, 12 May 2026 09:11:34 GMT
LABEL com.redhat.component="ubi10-minimal-container"       name="ubi10/ubi-minimal"       version="10.1"       cpe="cpe:/o:redhat:enterprise_linux:10.1"       distribution-scope="public"
# Tue, 12 May 2026 09:11:34 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Tue, 12 May 2026 09:11:34 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 10."
# Tue, 12 May 2026 09:11:34 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Tue, 12 May 2026 09:11:34 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Tue, 12 May 2026 09:11:34 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 10 Minimal"
# Tue, 12 May 2026 09:11:35 GMT
LABEL io.openshift.expose-services=""
# Tue, 12 May 2026 09:11:35 GMT
LABEL io.openshift.tags="minimal rhel10"
# Tue, 12 May 2026 09:11:35 GMT
ENV container oci
# Tue, 12 May 2026 09:11:35 GMT
COPY dir:2877d8ca2be54c031321bcf5c5c002de1e88fc4d881af88566c341114955d981 in /      
# Tue, 12 May 2026 09:11:35 GMT
COPY file:5de33b5fc08b00635bccf9134a18978dba13e2250aa51838f9969515a3957847 in /etc/yum.repos.d/.      
# Tue, 12 May 2026 09:11:35 GMT
CMD ["/bin/bash"]
# Tue, 12 May 2026 09:11:36 GMT
COPY file:595171150af68abc798ea385f7988d74b566aa8e84babff137f00b08b2164683 in /usr/share/buildinfo/content-sets.json      
# Tue, 12 May 2026 09:11:36 GMT
COPY file:595171150af68abc798ea385f7988d74b566aa8e84babff137f00b08b2164683 in /root/buildinfo/content_manifests/content-sets.json      
# Tue, 12 May 2026 09:11:36 GMT
COPY file:ed5db005734a9cf660fffe0f9d4de854f99deb1e83b8a69fd4b48dc74dea4448 in /usr/share/buildinfo/labels.json      
# Tue, 12 May 2026 09:11:36 GMT
COPY file:ed5db005734a9cf660fffe0f9d4de854f99deb1e83b8a69fd4b48dc74dea4448 in /root/buildinfo/labels.json      
# Tue, 12 May 2026 09:11:36 GMT
LABEL "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="ad7cdeeb08da8825126b10f488e410b0de5902b0" "org.opencontainers.image.revision"="ad7cdeeb08da8825126b10f488e410b0de5902b0" "build-date"="2026-05-12T09:11:19Z" "org.opencontainers.image.created"="2026-05-12T09:11:19Z" "release"="1778576723"org.opencontainers.image.revision=ad7cdeeb08da8825126b10f488e410b0de5902b0,org.opencontainers.image.created=2026-05-12T09:11:19Z
# Tue, 12 May 2026 23:33:47 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 12 May 2026 23:33:47 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 May 2026 23:33:47 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 12 May 2026 23:33:47 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en         gnupg2     ;     microdnf clean all # buildkit
# Tue, 12 May 2026 23:33:47 GMT
ENV JAVA_VERSION=jdk-25.0.3+9
# Tue, 12 May 2026 23:33:53 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='3e4287cb98870ba824ed698854bdc27cff984254caf66dd12cc291e7bfdde26b';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.3%2B9/OpenJDK25U-jdk_aarch64_linux_hotspot_25.0.3_9.tar.gz';          ;;        ppc64le)          ESUM='72b0fbb201716ca465ab704ec0fb12971abab3fdde5ae8d03b125a273522cf05';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.3%2B9/OpenJDK25U-jdk_ppc64le_linux_hotspot_25.0.3_9.tar.gz';          ;;        s390x)          ESUM='24b497d10acb6ee706ca30e1c8a929785c250cad54c5c12f1f8f93c3c06a53f7';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.3%2B9/OpenJDK25U-jdk_s390x_linux_hotspot_25.0.3_9.tar.gz';          ;;        x86_64)          ESUM='69264a7a211bf5029830d07bc3370f879769d62ebc5b5488e90c9343a2da0e1f';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.3%2B9/OpenJDK25U-jdk_x64_linux_hotspot_25.0.3_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Tue, 12 May 2026 23:33:55 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 12 May 2026 23:33:55 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 12 May 2026 23:33:55 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 12 May 2026 23:33:55 GMT
CMD ["jshell"]
# Wed, 13 May 2026 00:12:39 GMT
CMD ["gradle"]
# Wed, 13 May 2026 00:12:39 GMT
ENV GRADLE_HOME=/opt/gradle
# Wed, 13 May 2026 00:12:39 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 101 gradle     && useradd --system --gid gradle --uid 101 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Wed, 13 May 2026 00:12:39 GMT
VOLUME [/home/gradle/.gradle]
# Wed, 13 May 2026 00:12:39 GMT
WORKDIR /home/gradle
# Wed, 13 May 2026 00:12:42 GMT
RUN set -o errexit -o nounset     && microdnf install -y         make         curl         wget         tar                 findutils                 unzip         which                 git         git-lfs         subversion     && microdnf clean all         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which svn # buildkit
# Wed, 13 May 2026 00:12:42 GMT
ENV GRADLE_VERSION=9.5.1
# Wed, 13 May 2026 00:12:42 GMT
ARG GRADLE_DOWNLOAD_SHA256=bafc141b619ad6350fd975fc903156dd5c151998cc8b058e8c1044ab5f7b031f
# Wed, 13 May 2026 00:12:45 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=bafc141b619ad6350fd975fc903156dd5c151998cc8b058e8c1044ab5f7b031f
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Wed, 13 May 2026 00:12:45 GMT
USER gradle
# Wed, 13 May 2026 00:12:46 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=bafc141b619ad6350fd975fc903156dd5c151998cc8b058e8c1044ab5f7b031f
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --stacktrace --debug --version # buildkit
# Wed, 13 May 2026 00:12:46 GMT
USER root
```

-	Layers:
	-	`sha256:24bccfaffdcba4dab6b032daed65e4f69253b002d2af6f83ce7d6d966c20583a`  
		Last Modified: Tue, 12 May 2026 10:25:24 GMT  
		Size: 32.7 MB (32711659 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6280801a96a53ebe9490a0ee9801a9d3fb3baf89f3adf4059f23723058020352`  
		Last Modified: Tue, 12 May 2026 23:34:14 GMT  
		Size: 37.4 MB (37443351 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93fe54150cf683ad5e4916ec4469037ac4d9dfd15f5c21501d102f50d619414e`  
		Last Modified: Tue, 12 May 2026 23:34:15 GMT  
		Size: 91.5 MB (91548883 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bda0d41ee10ff104a3336bdc5996fd0eb1232709fa12c9449f9b3470be1c8ece`  
		Last Modified: Tue, 12 May 2026 23:34:12 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1bb10b834c55909f01b944f9fffbf49a159db44bb1a6f63a6e8bc21b81769fe3`  
		Last Modified: Tue, 12 May 2026 23:34:12 GMT  
		Size: 2.3 KB (2291 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86385cfef9c2255c915f67055ea65aa898035e976830f516a3362fe56dd37016`  
		Last Modified: Wed, 13 May 2026 00:13:06 GMT  
		Size: 1.6 KB (1585 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fae30b104500dfce460c4b0e21a13e5c0b5a9c7b74c55113b0e79ccc6b3dced`  
		Last Modified: Wed, 13 May 2026 00:13:08 GMT  
		Size: 38.3 MB (38322367 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:315febb9d78dd0e3ab65a92b9333974eff3e60e8311c54c7ef7e5ba5026257d6`  
		Last Modified: Wed, 13 May 2026 00:13:10 GMT  
		Size: 140.2 MB (140236986 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c32effc8561cedf44bef019a1600f2ae3ee43d4e6d88c260b63911161cce0a09`  
		Last Modified: Wed, 13 May 2026 00:13:06 GMT  
		Size: 29.3 KB (29337 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:ubi10` - unknown; unknown

```console
$ docker pull gradle@sha256:c40e01db7f1a923fde9d44525910b54b11f25ef75bafc4148996693c4f4e1fcb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 MB (7048017 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:43115ee1079e5a93cec7c37e5c3e511ff6b3130a9b2969622ab3f7dce2e4843d`

```dockerfile
```

-	Layers:
	-	`sha256:d3353eea584f7fef90a469af3d87330751049410351e312797e30d4aca83323c`  
		Last Modified: Wed, 13 May 2026 00:13:06 GMT  
		Size: 7.0 MB (7022787 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:98ef3a2c8bf6b585d37035009463900fc2c9787b01f1146eb2fc3a6d816e2bab`  
		Last Modified: Wed, 13 May 2026 00:13:05 GMT  
		Size: 25.2 KB (25230 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:ubi10` - linux; ppc64le

```console
$ docker pull gradle@sha256:c97946c4ea543359b7da96eb773a8c1b8a44043a19ecffb3644dcb2938e84768
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **350.8 MB (350780995 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:228d09439b5f344b039ccae6aa5adb98b05353696f1e1454bc31f09991e70e6f`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["gradle"]`

```dockerfile
# Tue, 12 May 2026 09:13:30 GMT
LABEL maintainer="Red Hat, Inc."
# Tue, 12 May 2026 09:13:30 GMT
LABEL vendor="Red Hat, Inc."
# Tue, 12 May 2026 09:13:30 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Tue, 12 May 2026 09:13:30 GMT
LABEL com.redhat.component="ubi10-minimal-container"       name="ubi10/ubi-minimal"       version="10.1"       cpe="cpe:/o:redhat:enterprise_linux:10.1"       distribution-scope="public"
# Tue, 12 May 2026 09:13:30 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Tue, 12 May 2026 09:13:30 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 10."
# Tue, 12 May 2026 09:13:30 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Tue, 12 May 2026 09:13:30 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Tue, 12 May 2026 09:13:30 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 10 Minimal"
# Tue, 12 May 2026 09:13:31 GMT
LABEL io.openshift.expose-services=""
# Tue, 12 May 2026 09:13:31 GMT
LABEL io.openshift.tags="minimal rhel10"
# Tue, 12 May 2026 09:13:31 GMT
ENV container oci
# Tue, 12 May 2026 09:13:32 GMT
COPY dir:584fbc93c21a7184a941a4142a12f835dcfca07a9a2dfc5bd8298fc624407c1a in /      
# Tue, 12 May 2026 09:13:32 GMT
COPY file:5de33b5fc08b00635bccf9134a18978dba13e2250aa51838f9969515a3957847 in /etc/yum.repos.d/.      
# Tue, 12 May 2026 09:13:32 GMT
CMD ["/bin/bash"]
# Tue, 12 May 2026 09:13:32 GMT
COPY file:595171150af68abc798ea385f7988d74b566aa8e84babff137f00b08b2164683 in /usr/share/buildinfo/content-sets.json      
# Tue, 12 May 2026 09:13:32 GMT
COPY file:595171150af68abc798ea385f7988d74b566aa8e84babff137f00b08b2164683 in /root/buildinfo/content_manifests/content-sets.json      
# Tue, 12 May 2026 09:13:33 GMT
COPY file:101e1b19e6d0f9785c2d23ecc61947a5882edebf262baa5a4ebcee0c3b40e8a2 in /usr/share/buildinfo/labels.json      
# Tue, 12 May 2026 09:13:33 GMT
COPY file:101e1b19e6d0f9785c2d23ecc61947a5882edebf262baa5a4ebcee0c3b40e8a2 in /root/buildinfo/labels.json      
# Tue, 12 May 2026 09:13:33 GMT
LABEL "architecture"="ppc64le" "vcs-type"="git" "vcs-ref"="ad7cdeeb08da8825126b10f488e410b0de5902b0" "org.opencontainers.image.revision"="ad7cdeeb08da8825126b10f488e410b0de5902b0" "build-date"="2026-05-12T09:13:14Z" "org.opencontainers.image.created"="2026-05-12T09:13:14Z" "release"="1778576723"org.opencontainers.image.revision=ad7cdeeb08da8825126b10f488e410b0de5902b0,org.opencontainers.image.created=2026-05-12T09:13:14Z
# Tue, 12 May 2026 23:31:50 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 12 May 2026 23:31:50 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 May 2026 23:31:50 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 12 May 2026 23:31:50 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en         gnupg2     ;     microdnf clean all # buildkit
# Tue, 12 May 2026 23:31:50 GMT
ENV JAVA_VERSION=jdk-25.0.3+9
# Tue, 12 May 2026 23:40:01 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='3e4287cb98870ba824ed698854bdc27cff984254caf66dd12cc291e7bfdde26b';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.3%2B9/OpenJDK25U-jdk_aarch64_linux_hotspot_25.0.3_9.tar.gz';          ;;        ppc64le)          ESUM='72b0fbb201716ca465ab704ec0fb12971abab3fdde5ae8d03b125a273522cf05';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.3%2B9/OpenJDK25U-jdk_ppc64le_linux_hotspot_25.0.3_9.tar.gz';          ;;        s390x)          ESUM='24b497d10acb6ee706ca30e1c8a929785c250cad54c5c12f1f8f93c3c06a53f7';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.3%2B9/OpenJDK25U-jdk_s390x_linux_hotspot_25.0.3_9.tar.gz';          ;;        x86_64)          ESUM='69264a7a211bf5029830d07bc3370f879769d62ebc5b5488e90c9343a2da0e1f';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.3%2B9/OpenJDK25U-jdk_x64_linux_hotspot_25.0.3_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Tue, 12 May 2026 23:40:05 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 12 May 2026 23:40:05 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 12 May 2026 23:40:05 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 12 May 2026 23:40:05 GMT
CMD ["jshell"]
# Wed, 13 May 2026 00:11:32 GMT
CMD ["gradle"]
# Wed, 13 May 2026 00:11:32 GMT
ENV GRADLE_HOME=/opt/gradle
# Wed, 13 May 2026 00:11:32 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 101 gradle     && useradd --system --gid gradle --uid 101 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Wed, 13 May 2026 00:11:32 GMT
VOLUME [/home/gradle/.gradle]
# Wed, 13 May 2026 00:11:32 GMT
WORKDIR /home/gradle
# Wed, 13 May 2026 00:11:45 GMT
RUN set -o errexit -o nounset     && microdnf install -y         make         curl         wget         tar                 findutils                 unzip         which                 git         git-lfs         subversion     && microdnf clean all         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which svn # buildkit
# Wed, 13 May 2026 00:11:45 GMT
ENV GRADLE_VERSION=9.5.1
# Wed, 13 May 2026 00:11:45 GMT
ARG GRADLE_DOWNLOAD_SHA256=bafc141b619ad6350fd975fc903156dd5c151998cc8b058e8c1044ab5f7b031f
# Wed, 13 May 2026 00:11:51 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=bafc141b619ad6350fd975fc903156dd5c151998cc8b058e8c1044ab5f7b031f
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Wed, 13 May 2026 00:11:51 GMT
USER gradle
# Wed, 13 May 2026 00:11:53 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=bafc141b619ad6350fd975fc903156dd5c151998cc8b058e8c1044ab5f7b031f
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --stacktrace --debug --version # buildkit
# Wed, 13 May 2026 00:11:53 GMT
USER root
```

-	Layers:
	-	`sha256:f815e851aa9d271f09d3448e8acc95ebed62472057c9b0368d01b242d1468875`  
		Last Modified: Tue, 12 May 2026 12:16:14 GMT  
		Size: 38.8 MB (38794493 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d1fdf741746dd4482bfc42d70a6f2954201df0346c653d262b3e220a6a63447`  
		Last Modified: Tue, 12 May 2026 23:32:30 GMT  
		Size: 39.3 MB (39255778 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1634e92fd1ea2798cdc53e66f4eb0f19bc0143eba8e6643bc85664ef940da8c`  
		Last Modified: Tue, 12 May 2026 23:40:39 GMT  
		Size: 91.9 MB (91912874 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e8f4b7beb23319efa4fd64d580e9dfa59886704c2287b2a4a2397a036c564f1`  
		Last Modified: Tue, 12 May 2026 23:40:37 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:131d055c02cb8ea0dd6429d816882cc7f447585fdf555a31f56912b66fc9d09e`  
		Last Modified: Tue, 12 May 2026 23:40:37 GMT  
		Size: 2.3 KB (2291 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb9223067ce6a5c947681d7779fc27038fe9a7c2a950a407c7f24ef575ccbe56`  
		Last Modified: Wed, 13 May 2026 00:12:34 GMT  
		Size: 1.6 KB (1589 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa09eb88e40233fca63ac234e507658a4f6c7792c5f574bf2fc265d699dbf347`  
		Last Modified: Wed, 13 May 2026 00:12:36 GMT  
		Size: 40.6 MB (40576441 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df710fbc9f3ffd7727a8d4450b63738e7ed11507c07a8010ec49e609c8e0c089`  
		Last Modified: Wed, 13 May 2026 00:12:39 GMT  
		Size: 140.2 MB (140236988 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a59eb027a40153dc8ffd1ffeff8040449fb081880449f06ee0868785355b62fa`  
		Last Modified: Wed, 13 May 2026 00:12:35 GMT  
		Size: 380.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:ubi10` - unknown; unknown

```console
$ docker pull gradle@sha256:3999321d3f97e9535835df85c976a919f782238d7a0ec0bcba0ff2f1c72c2b5c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 MB (7024345 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:45864e5511123a6269ec4d206c8f88b40015479022aac94bfe874c9cda09051f`

```dockerfile
```

-	Layers:
	-	`sha256:0d189a0025c017e6bdd0330e8a0c96592e8b7e82d330417a07d29fd90d9f630f`  
		Last Modified: Wed, 13 May 2026 00:12:35 GMT  
		Size: 7.0 MB (6999252 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9c77ffe83e09f4a12085934547778fe55429c1563dbd95c91609979e6b4ce282`  
		Last Modified: Wed, 13 May 2026 00:12:34 GMT  
		Size: 25.1 KB (25093 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:ubi10` - linux; s390x

```console
$ docker pull gradle@sha256:0d69a7e5d8fad66e59efeba1cba41731b90196fa853db2ebfdb3eef099aea77f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **341.9 MB (341922057 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:706d737fa24c3457770666d76eb26d1a2a67ea44b60c4623d1f48202d318af8d`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["gradle"]`

```dockerfile
# Tue, 12 May 2026 09:27:49 GMT
LABEL maintainer="Red Hat, Inc."
# Tue, 12 May 2026 09:27:49 GMT
LABEL vendor="Red Hat, Inc."
# Tue, 12 May 2026 09:27:49 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Tue, 12 May 2026 09:27:49 GMT
LABEL com.redhat.component="ubi10-minimal-container"       name="ubi10/ubi-minimal"       version="10.1"       cpe="cpe:/o:redhat:enterprise_linux:10.1"       distribution-scope="public"
# Tue, 12 May 2026 09:27:49 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Tue, 12 May 2026 09:27:49 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 10."
# Tue, 12 May 2026 09:27:49 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Tue, 12 May 2026 09:27:49 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Tue, 12 May 2026 09:27:49 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 10 Minimal"
# Tue, 12 May 2026 09:27:49 GMT
LABEL io.openshift.expose-services=""
# Tue, 12 May 2026 09:27:49 GMT
LABEL io.openshift.tags="minimal rhel10"
# Tue, 12 May 2026 09:27:49 GMT
ENV container oci
# Tue, 12 May 2026 09:27:49 GMT
COPY dir:ad73fd8372aea6e68c9b3ea90e4901b979a82fb0f4a43074fa7ea61354ab30b9 in /      
# Tue, 12 May 2026 09:27:49 GMT
COPY file:5de33b5fc08b00635bccf9134a18978dba13e2250aa51838f9969515a3957847 in /etc/yum.repos.d/.      
# Tue, 12 May 2026 09:27:49 GMT
CMD ["/bin/bash"]
# Tue, 12 May 2026 09:27:49 GMT
COPY file:595171150af68abc798ea385f7988d74b566aa8e84babff137f00b08b2164683 in /usr/share/buildinfo/content-sets.json      
# Tue, 12 May 2026 09:27:50 GMT
COPY file:595171150af68abc798ea385f7988d74b566aa8e84babff137f00b08b2164683 in /root/buildinfo/content_manifests/content-sets.json      
# Tue, 12 May 2026 09:27:50 GMT
COPY file:f69727366f08991ceef4955068ba3462c331e0d11189e73f45fe959e3f50f354 in /usr/share/buildinfo/labels.json      
# Tue, 12 May 2026 09:27:50 GMT
COPY file:f69727366f08991ceef4955068ba3462c331e0d11189e73f45fe959e3f50f354 in /root/buildinfo/labels.json      
# Tue, 12 May 2026 09:27:50 GMT
LABEL "architecture"="s390x" "vcs-type"="git" "vcs-ref"="ad7cdeeb08da8825126b10f488e410b0de5902b0" "org.opencontainers.image.revision"="ad7cdeeb08da8825126b10f488e410b0de5902b0" "build-date"="2026-05-12T09:27:06Z" "org.opencontainers.image.created"="2026-05-12T09:27:06Z" "release"="1778576723"org.opencontainers.image.revision=ad7cdeeb08da8825126b10f488e410b0de5902b0,org.opencontainers.image.created=2026-05-12T09:27:06Z
# Tue, 12 May 2026 23:33:20 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 12 May 2026 23:33:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 May 2026 23:33:20 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 12 May 2026 23:33:20 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en         gnupg2     ;     microdnf clean all # buildkit
# Tue, 12 May 2026 23:33:20 GMT
ENV JAVA_VERSION=jdk-25.0.3+9
# Tue, 12 May 2026 23:38:03 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='3e4287cb98870ba824ed698854bdc27cff984254caf66dd12cc291e7bfdde26b';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.3%2B9/OpenJDK25U-jdk_aarch64_linux_hotspot_25.0.3_9.tar.gz';          ;;        ppc64le)          ESUM='72b0fbb201716ca465ab704ec0fb12971abab3fdde5ae8d03b125a273522cf05';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.3%2B9/OpenJDK25U-jdk_ppc64le_linux_hotspot_25.0.3_9.tar.gz';          ;;        s390x)          ESUM='24b497d10acb6ee706ca30e1c8a929785c250cad54c5c12f1f8f93c3c06a53f7';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.3%2B9/OpenJDK25U-jdk_s390x_linux_hotspot_25.0.3_9.tar.gz';          ;;        x86_64)          ESUM='69264a7a211bf5029830d07bc3370f879769d62ebc5b5488e90c9343a2da0e1f';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.3%2B9/OpenJDK25U-jdk_x64_linux_hotspot_25.0.3_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Tue, 12 May 2026 23:38:05 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 12 May 2026 23:38:05 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 12 May 2026 23:38:05 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 12 May 2026 23:38:05 GMT
CMD ["jshell"]
# Wed, 13 May 2026 00:12:13 GMT
CMD ["gradle"]
# Wed, 13 May 2026 00:12:13 GMT
ENV GRADLE_HOME=/opt/gradle
# Wed, 13 May 2026 00:12:13 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 101 gradle     && useradd --system --gid gradle --uid 101 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Wed, 13 May 2026 00:12:13 GMT
VOLUME [/home/gradle/.gradle]
# Wed, 13 May 2026 00:12:15 GMT
WORKDIR /home/gradle
# Wed, 13 May 2026 00:13:10 GMT
RUN set -o errexit -o nounset     && microdnf install -y         make         curl         wget         tar                 findutils                 unzip         which                 git         git-lfs         subversion     && microdnf clean all         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which svn # buildkit
# Wed, 13 May 2026 00:13:10 GMT
ENV GRADLE_VERSION=9.5.1
# Wed, 13 May 2026 00:13:10 GMT
ARG GRADLE_DOWNLOAD_SHA256=bafc141b619ad6350fd975fc903156dd5c151998cc8b058e8c1044ab5f7b031f
# Wed, 13 May 2026 00:13:17 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=bafc141b619ad6350fd975fc903156dd5c151998cc8b058e8c1044ab5f7b031f
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Wed, 13 May 2026 00:13:17 GMT
USER gradle
# Wed, 13 May 2026 00:13:19 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=bafc141b619ad6350fd975fc903156dd5c151998cc8b058e8c1044ab5f7b031f
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --stacktrace --debug --version # buildkit
# Wed, 13 May 2026 00:13:19 GMT
USER root
```

-	Layers:
	-	`sha256:716b8ccfad2ab26e031483f83283392459a7160cf7d641599a620a485af51f10`  
		Last Modified: Tue, 12 May 2026 12:16:04 GMT  
		Size: 34.5 MB (34450081 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7dec299a1602bf5e0d62202cf77938cca794fdd9ba9bbc56e355abbc7a6a990b`  
		Last Modified: Tue, 12 May 2026 23:33:57 GMT  
		Size: 37.9 MB (37879929 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f126ae1f9a409f23ce2abb8bb3bce6365a0c32867c0ee124010c71cb0006ffe5`  
		Last Modified: Tue, 12 May 2026 23:38:35 GMT  
		Size: 88.4 MB (88421662 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:086b3f91ad7ef8a79af0abcd90470d511222be4ed365908610ca71a91e5fd3c8`  
		Last Modified: Tue, 12 May 2026 23:38:33 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3c15316eeb777f48647e2ac80988395b632a36ea1cefed7ccccabd82bbe9e98`  
		Last Modified: Tue, 12 May 2026 23:38:33 GMT  
		Size: 2.3 KB (2291 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63ef2cd7dfdfb228f4366869dfc3cdbd263958b796b2bbda5bd0615132d73fc9`  
		Last Modified: Wed, 13 May 2026 00:14:34 GMT  
		Size: 1.6 KB (1596 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f339ea7e41e0186ff62c39e695647c74365ff3f2426d6eb676792bef98c5298`  
		Last Modified: Wed, 13 May 2026 00:14:39 GMT  
		Size: 40.9 MB (40928967 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b25c8640f87216c99ae36341b8db08a76a149ac4acc488b187e86204fc85c383`  
		Last Modified: Wed, 13 May 2026 00:14:43 GMT  
		Size: 140.2 MB (140236990 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:360b02859fa56cce3ca29c6239788daf3745622b3a2735a2420d79edba24e162`  
		Last Modified: Wed, 13 May 2026 00:14:35 GMT  
		Size: 380.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:ubi10` - unknown; unknown

```console
$ docker pull gradle@sha256:2ab9f3f1d6ee3d00b966d88103c7d0e24725042ea969e8016cfe85cb44162c34
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 MB (7014726 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:18f120cb5a0c2b3e01ab429d3367dd0a753b4f782d31eca3757633049431c948`

```dockerfile
```

-	Layers:
	-	`sha256:fdd831a9bc843798bbab6bbe9e5ba194f19548a7bce22326f1b2397e503162c7`  
		Last Modified: Wed, 13 May 2026 00:14:35 GMT  
		Size: 7.0 MB (6989719 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:05919e6df1c13f77de8652f9abf810e106a6f89697bb97b25271968fbeb45967`  
		Last Modified: Wed, 13 May 2026 00:14:34 GMT  
		Size: 25.0 KB (25007 bytes)  
		MIME: application/vnd.in-toto+json
