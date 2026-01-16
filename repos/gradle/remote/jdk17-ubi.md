## `gradle:jdk17-ubi`

```console
$ docker pull gradle@sha256:71a27f955982702f97a15bba25cacdcd34d7013a306468c67929439491c39794
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

### `gradle:jdk17-ubi` - linux; amd64

```console
$ docker pull gradle@sha256:eae814660b9d4288257e87d39ca5f590b064a875a804965532f7494a6fb2d494
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **409.4 MB (409436822 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:da4170ce7e5c0c6ba684f597c954ba70f4bcec7af4ef19d43da904495cb4e0b7`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["gradle"]`

```dockerfile
# Thu, 18 Dec 2025 04:59:16 GMT
LABEL maintainer="Red Hat, Inc."
# Thu, 18 Dec 2025 04:59:16 GMT
LABEL vendor="Red Hat, Inc."
# Thu, 18 Dec 2025 04:59:16 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Thu, 18 Dec 2025 04:59:16 GMT
LABEL com.redhat.component="ubi10-minimal-container"       name="ubi10/ubi-minimal"       version="10.1"       cpe="cpe:/o:redhat:enterprise_linux:10.1"       distribution-scope="public"
# Thu, 18 Dec 2025 04:59:16 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Thu, 18 Dec 2025 04:59:16 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 10."
# Thu, 18 Dec 2025 04:59:16 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 18 Dec 2025 04:59:16 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 18 Dec 2025 04:59:16 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 10 Minimal"
# Thu, 18 Dec 2025 04:59:16 GMT
LABEL io.openshift.expose-services=""
# Thu, 18 Dec 2025 04:59:16 GMT
LABEL io.openshift.tags="minimal rhel10"
# Thu, 18 Dec 2025 04:59:16 GMT
ENV container oci
# Thu, 18 Dec 2025 04:59:17 GMT
COPY dir:fdc8c39dddd7104eb139c404c8e963d7763f4f2dba800adb3cb1affa751115f3 in /      
# Thu, 18 Dec 2025 04:59:17 GMT
COPY file:5de33b5fc08b00635bccf9134a18978dba13e2250aa51838f9969515a3957847 in /etc/yum.repos.d/.      
# Thu, 18 Dec 2025 04:59:17 GMT
CMD ["/bin/bash"]
# Thu, 18 Dec 2025 04:59:17 GMT
COPY file:595171150af68abc798ea385f7988d74b566aa8e84babff137f00b08b2164683 in /usr/share/buildinfo/content-sets.json      
# Thu, 18 Dec 2025 04:59:17 GMT
COPY file:595171150af68abc798ea385f7988d74b566aa8e84babff137f00b08b2164683 in /root/buildinfo/content_manifests/content-sets.json      
# Thu, 18 Dec 2025 04:59:17 GMT
COPY file:7bed867b68b82c11d96a326acbe92a53eeb4b701a4a63e4b069dab774da39ed9 in /usr/share/buildinfo/labels.json      
# Thu, 18 Dec 2025 04:59:17 GMT
COPY file:7bed867b68b82c11d96a326acbe92a53eeb4b701a4a63e4b069dab774da39ed9 in /root/buildinfo/labels.json      
# Thu, 18 Dec 2025 04:59:17 GMT
LABEL "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="3dbd4aac2bce2ca6b13274bf0662e947c80b18b9" "org.opencontainers.image.revision"="3dbd4aac2bce2ca6b13274bf0662e947c80b18b9" "build-date"="2025-12-18T04:58:54Z" "org.opencontainers.image.created"="2025-12-18T04:58:54Z" "release"="1766033715"org.opencontainers.image.revision=3dbd4aac2bce2ca6b13274bf0662e947c80b18b9,org.opencontainers.image.created=2025-12-18T04:58:54Z
# Thu, 18 Dec 2025 22:23:40 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 18 Dec 2025 22:23:40 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 18 Dec 2025 22:23:40 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 18 Dec 2025 22:23:40 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en         gnupg2     ;     microdnf clean all # buildkit
# Thu, 18 Dec 2025 22:23:40 GMT
ENV JAVA_VERSION=jdk-17.0.17+10
# Thu, 18 Dec 2025 22:23:46 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='dc29ca6d35beb4419b4b00419b8a3dfbf5ae551e1ae2b046b516d9a579d04533';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jdk_aarch64_linux_hotspot_17.0.17_10.tar.gz';          ;;        ppc64le)          ESUM='2a29d1be61940c1bd639018c07f4622e1f145a7ef34e7294fee877e39226d9da';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jdk_ppc64le_linux_hotspot_17.0.17_10.tar.gz';          ;;        s390x)          ESUM='76327b1d00c67f6be91717754fd85fc85ce496d48876f69accb9c53ed31dc546';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jdk_s390x_linux_hotspot_17.0.17_10.tar.gz';          ;;        x86_64)          ESUM='992f96e7995075ac7636bb1a8de52b0c61d71ed3137fafc979ab96b4ab78dd75';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jdk_x64_linux_hotspot_17.0.17_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Thu, 18 Dec 2025 22:23:47 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 18 Dec 2025 22:23:47 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 18 Dec 2025 22:23:47 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 18 Dec 2025 22:23:47 GMT
CMD ["jshell"]
# Thu, 18 Dec 2025 22:56:33 GMT
CMD ["gradle"]
# Thu, 18 Dec 2025 22:56:33 GMT
ENV GRADLE_HOME=/opt/gradle
# Thu, 18 Dec 2025 22:56:33 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 101 gradle     && useradd --system --gid gradle --uid 101 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Thu, 18 Dec 2025 22:56:33 GMT
VOLUME [/home/gradle/.gradle]
# Thu, 18 Dec 2025 22:56:33 GMT
WORKDIR /home/gradle
# Thu, 18 Dec 2025 22:56:39 GMT
RUN set -o errexit -o nounset     && microdnf install -y         make         curl-minimal         wget         tar                 findutils                 unzip         which                 git         git-lfs         subversion     && microdnf clean all         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which svn # buildkit
# Thu, 18 Dec 2025 22:56:39 GMT
ENV GRADLE_VERSION=9.2.1
# Thu, 18 Dec 2025 22:56:39 GMT
ARG GRADLE_DOWNLOAD_SHA256=72f44c9f8ebcb1af43838f45ee5c4aa9c5444898b3468ab3f4af7b6076c5bc3f
# Thu, 18 Dec 2025 22:56:41 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=72f44c9f8ebcb1af43838f45ee5c4aa9c5444898b3468ab3f4af7b6076c5bc3f
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Thu, 18 Dec 2025 22:56:41 GMT
USER gradle
# Thu, 18 Dec 2025 22:56:42 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=72f44c9f8ebcb1af43838f45ee5c4aa9c5444898b3468ab3f4af7b6076c5bc3f
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --stacktrace --debug --version # buildkit
# Thu, 18 Dec 2025 22:56:42 GMT
USER root
```

-	Layers:
	-	`sha256:bbf656ece02bf42bcb72be26aaced8f9084f91250ae2336e1f2b7b9e8b979727`  
		Last Modified: Thu, 18 Dec 2025 11:19:29 GMT  
		Size: 34.5 MB (34531778 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff3edaec2a8085b53169aad00e500cf23a536467b74e25d584ed4acb2e687224`  
		Last Modified: Thu, 18 Dec 2025 22:24:22 GMT  
		Size: 55.3 MB (55325379 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1eb60cfd75dd4fc77f99cf2a8b6d3f6f8096a4ad985f32c7f9ca790ae3338e0`  
		Last Modified: Thu, 18 Dec 2025 22:24:27 GMT  
		Size: 144.9 MB (144852890 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89ea47bf79f4686431f239f9867a8d5d46f991862612adc2bb48503fd471419e`  
		Last Modified: Thu, 18 Dec 2025 22:24:16 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0200b26b13e4ec50e65be104cd1ea9b5bf7714b3371732961563cc3c461267c6`  
		Last Modified: Thu, 18 Dec 2025 22:24:16 GMT  
		Size: 2.3 KB (2291 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65422698705bb05f66339fea69986fed295d60bd6cd66c7543a0e22f05cdacba`  
		Last Modified: Thu, 18 Dec 2025 22:57:11 GMT  
		Size: 1.6 KB (1623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8311a158c335516df3df04d7a91691cca38d2f506205818404943547cd219478`  
		Last Modified: Thu, 18 Dec 2025 22:57:14 GMT  
		Size: 39.1 MB (39145824 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aafe801e2ba5210b7f10ad5cc1c43d7646ce0653d61a0afd14708cfd4e7b462c`  
		Last Modified: Thu, 18 Dec 2025 22:58:30 GMT  
		Size: 135.5 MB (135521972 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1f5c14f3efc608a06ed17bd6a61d14238def93a35781e7b8b56e16fcfa00e9a`  
		Last Modified: Thu, 18 Dec 2025 22:57:11 GMT  
		Size: 54.9 KB (54905 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:jdk17-ubi` - unknown; unknown

```console
$ docker pull gradle@sha256:0da8522536e16cb204f9e8318bfaf692cddcf9ecd39528a8bcf09756a4677ad9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.0 MB (8950617 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f8713f373d1f9ec0f0deea63b3c3f95d374270cc7b2df4af6a1854495c3be73a`

```dockerfile
```

-	Layers:
	-	`sha256:31ab8f0c309d9f364792198a4bb877f330e451ea994c3917a5ab92aed41f58d3`  
		Last Modified: Fri, 19 Dec 2025 00:21:12 GMT  
		Size: 8.9 MB (8926162 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:78783a179203e1264de193a1638644f71005fa5abed7c5944ce9f1b17fd0eca2`  
		Last Modified: Fri, 19 Dec 2025 00:21:13 GMT  
		Size: 24.5 KB (24455 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:jdk17-ubi` - linux; arm64 variant v8

```console
$ docker pull gradle@sha256:1260e4d540b0822323c5829296cdd05b061399f600166568892ac2c03a0230dd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **405.6 MB (405640169 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:36f94c87254d2115e6289f518b08c3973b3d5f5b832602960227a745a63b7bb3`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["gradle"]`

```dockerfile
# Thu, 18 Dec 2025 05:04:19 GMT
LABEL maintainer="Red Hat, Inc."
# Thu, 18 Dec 2025 05:04:19 GMT
LABEL vendor="Red Hat, Inc."
# Thu, 18 Dec 2025 05:04:19 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Thu, 18 Dec 2025 05:04:19 GMT
LABEL com.redhat.component="ubi10-minimal-container"       name="ubi10/ubi-minimal"       version="10.1"       cpe="cpe:/o:redhat:enterprise_linux:10.1"       distribution-scope="public"
# Thu, 18 Dec 2025 05:04:19 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Thu, 18 Dec 2025 05:04:19 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 10."
# Thu, 18 Dec 2025 05:04:19 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 18 Dec 2025 05:04:19 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 18 Dec 2025 05:04:19 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 10 Minimal"
# Thu, 18 Dec 2025 05:04:19 GMT
LABEL io.openshift.expose-services=""
# Thu, 18 Dec 2025 05:04:19 GMT
LABEL io.openshift.tags="minimal rhel10"
# Thu, 18 Dec 2025 05:04:19 GMT
ENV container oci
# Thu, 18 Dec 2025 05:04:20 GMT
COPY dir:04b750083472751a7f5154bb88e2ce4d0526c13f7486508dfd32af911f2d6c12 in /      
# Thu, 18 Dec 2025 05:04:20 GMT
COPY file:5de33b5fc08b00635bccf9134a18978dba13e2250aa51838f9969515a3957847 in /etc/yum.repos.d/.      
# Thu, 18 Dec 2025 05:04:20 GMT
CMD ["/bin/bash"]
# Thu, 18 Dec 2025 05:04:20 GMT
COPY file:595171150af68abc798ea385f7988d74b566aa8e84babff137f00b08b2164683 in /usr/share/buildinfo/content-sets.json      
# Thu, 18 Dec 2025 05:04:20 GMT
COPY file:595171150af68abc798ea385f7988d74b566aa8e84babff137f00b08b2164683 in /root/buildinfo/content_manifests/content-sets.json      
# Thu, 18 Dec 2025 05:04:20 GMT
COPY file:3a827beb44c0bded02518913eace1a58024dbf0ce6482c0f23a932e3e59b2536 in /usr/share/buildinfo/labels.json      
# Thu, 18 Dec 2025 05:04:20 GMT
COPY file:3a827beb44c0bded02518913eace1a58024dbf0ce6482c0f23a932e3e59b2536 in /root/buildinfo/labels.json      
# Thu, 18 Dec 2025 05:04:20 GMT
LABEL "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="3dbd4aac2bce2ca6b13274bf0662e947c80b18b9" "org.opencontainers.image.revision"="3dbd4aac2bce2ca6b13274bf0662e947c80b18b9" "build-date"="2025-12-18T05:03:56Z" "org.opencontainers.image.created"="2025-12-18T05:03:56Z" "release"="1766033715"org.opencontainers.image.revision=3dbd4aac2bce2ca6b13274bf0662e947c80b18b9,org.opencontainers.image.created=2025-12-18T05:03:56Z
# Thu, 18 Dec 2025 22:30:35 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 18 Dec 2025 22:30:35 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 18 Dec 2025 22:30:35 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 18 Dec 2025 22:30:35 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en         gnupg2     ;     microdnf clean all # buildkit
# Thu, 18 Dec 2025 22:30:35 GMT
ENV JAVA_VERSION=jdk-17.0.17+10
# Thu, 18 Dec 2025 22:30:41 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='dc29ca6d35beb4419b4b00419b8a3dfbf5ae551e1ae2b046b516d9a579d04533';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jdk_aarch64_linux_hotspot_17.0.17_10.tar.gz';          ;;        ppc64le)          ESUM='2a29d1be61940c1bd639018c07f4622e1f145a7ef34e7294fee877e39226d9da';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jdk_ppc64le_linux_hotspot_17.0.17_10.tar.gz';          ;;        s390x)          ESUM='76327b1d00c67f6be91717754fd85fc85ce496d48876f69accb9c53ed31dc546';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jdk_s390x_linux_hotspot_17.0.17_10.tar.gz';          ;;        x86_64)          ESUM='992f96e7995075ac7636bb1a8de52b0c61d71ed3137fafc979ab96b4ab78dd75';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jdk_x64_linux_hotspot_17.0.17_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Thu, 18 Dec 2025 22:30:43 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 18 Dec 2025 22:30:43 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 18 Dec 2025 22:30:43 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 18 Dec 2025 22:30:43 GMT
CMD ["jshell"]
# Thu, 18 Dec 2025 23:00:01 GMT
CMD ["gradle"]
# Thu, 18 Dec 2025 23:00:01 GMT
ENV GRADLE_HOME=/opt/gradle
# Thu, 18 Dec 2025 23:00:01 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 101 gradle     && useradd --system --gid gradle --uid 101 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Thu, 18 Dec 2025 23:00:01 GMT
VOLUME [/home/gradle/.gradle]
# Thu, 18 Dec 2025 23:00:01 GMT
WORKDIR /home/gradle
# Thu, 18 Dec 2025 23:00:07 GMT
RUN set -o errexit -o nounset     && microdnf install -y         make         curl-minimal         wget         tar                 findutils                 unzip         which                 git         git-lfs         subversion     && microdnf clean all         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which svn # buildkit
# Thu, 18 Dec 2025 23:00:07 GMT
ENV GRADLE_VERSION=9.2.1
# Thu, 18 Dec 2025 23:00:07 GMT
ARG GRADLE_DOWNLOAD_SHA256=72f44c9f8ebcb1af43838f45ee5c4aa9c5444898b3468ab3f4af7b6076c5bc3f
# Thu, 18 Dec 2025 23:00:10 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=72f44c9f8ebcb1af43838f45ee5c4aa9c5444898b3468ab3f4af7b6076c5bc3f
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Thu, 18 Dec 2025 23:00:10 GMT
USER gradle
# Thu, 18 Dec 2025 23:00:10 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=72f44c9f8ebcb1af43838f45ee5c4aa9c5444898b3468ab3f4af7b6076c5bc3f
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --stacktrace --debug --version # buildkit
# Thu, 18 Dec 2025 23:00:10 GMT
USER root
```

-	Layers:
	-	`sha256:f416e7c13e96a1bec342af3e79184aaf45de55dd66939245eb76ca02465c54c7`  
		Last Modified: Thu, 18 Dec 2025 12:14:44 GMT  
		Size: 32.6 MB (32633678 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e61b0adcf4dfc94959f8c24835e9abdd7725d04bbce687fb4a2960fd5a01bd0`  
		Last Modified: Thu, 18 Dec 2025 22:31:21 GMT  
		Size: 55.1 MB (55118684 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84d58fedeb1b3cb3b0d1cec92ce6450469c5d2a526b057e593368f225cafe59c`  
		Last Modified: Thu, 18 Dec 2025 22:31:31 GMT  
		Size: 143.7 MB (143685415 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b62062e9551742241b8c9963a44cf30627e1b3d3704e27f766fbd370a0765d15`  
		Last Modified: Thu, 18 Dec 2025 22:31:10 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4da885a238dc54e31835a16697bbe5f703e3318bcc4f3517fcbc7005d4537b3`  
		Last Modified: Thu, 18 Dec 2025 22:31:10 GMT  
		Size: 2.3 KB (2288 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1a881f6d30dea7c2a4d2347a59a139635ebe634568cc1188af34ae66b437a4a`  
		Last Modified: Thu, 18 Dec 2025 23:00:39 GMT  
		Size: 1.6 KB (1622 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:adbdd66e5bfd74c2927456ff06c0ce43e1f695c676bf06df23258769f49241b7`  
		Last Modified: Thu, 18 Dec 2025 23:00:45 GMT  
		Size: 38.6 MB (38616823 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee382600956dbc7988de8614aa43472531fa14f58374d12f4b4bd36b1e3c18c9`  
		Last Modified: Thu, 18 Dec 2025 23:01:01 GMT  
		Size: 135.5 MB (135521971 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7222a3470d4f8444a7f1c9939f34d792540f48b984008ed5cd96c6e09fcda76`  
		Last Modified: Thu, 18 Dec 2025 23:00:39 GMT  
		Size: 59.5 KB (59527 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:jdk17-ubi` - unknown; unknown

```console
$ docker pull gradle@sha256:58117565874e9caa9df42cf47e243fe8dc5afa20c94503a45eacf35a86c903fb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.9 MB (8949130 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3329afe18710bea8a527e4e22def78b1717a4fa367fe14bcdf88e60dff273f5c`

```dockerfile
```

-	Layers:
	-	`sha256:24a0bf235575256c8a20f8de2b0448ca4e21ccdc427113ebc7d0f6de2b7d7f53`  
		Last Modified: Fri, 19 Dec 2025 00:21:22 GMT  
		Size: 8.9 MB (8924478 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:db9ad813b9f47bfeac5f36e408d88114d8a09c586bbfc5a055b0389106f0ce35`  
		Last Modified: Fri, 19 Dec 2025 00:21:23 GMT  
		Size: 24.7 KB (24652 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:jdk17-ubi` - linux; ppc64le

```console
$ docker pull gradle@sha256:cb63b566e5a66585285f76abfb258439e8e83db6c8cec22b38a4888dea188738
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **417.0 MB (417005623 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:12169c3485f77c48ed481fb97be835e9b49aa35a25af76459407b4b5ddca6979`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["gradle"]`

```dockerfile
# Thu, 18 Dec 2025 07:03:44 GMT
LABEL maintainer="Red Hat, Inc."
# Thu, 18 Dec 2025 07:03:44 GMT
LABEL vendor="Red Hat, Inc."
# Thu, 18 Dec 2025 07:03:44 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Thu, 18 Dec 2025 07:03:44 GMT
LABEL com.redhat.component="ubi10-minimal-container"       name="ubi10/ubi-minimal"       version="10.1"       cpe="cpe:/o:redhat:enterprise_linux:10.1"       distribution-scope="public"
# Thu, 18 Dec 2025 07:03:44 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Thu, 18 Dec 2025 07:03:44 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 10."
# Thu, 18 Dec 2025 07:03:44 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 18 Dec 2025 07:03:44 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 18 Dec 2025 07:03:44 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 10 Minimal"
# Thu, 18 Dec 2025 07:03:44 GMT
LABEL io.openshift.expose-services=""
# Thu, 18 Dec 2025 07:03:44 GMT
LABEL io.openshift.tags="minimal rhel10"
# Thu, 18 Dec 2025 07:03:44 GMT
ENV container oci
# Thu, 18 Dec 2025 07:03:45 GMT
COPY dir:530980282317924eec1c6623b725ebfc8622f7b70907079d2b485327f826b92a in /      
# Thu, 18 Dec 2025 07:03:45 GMT
COPY file:5de33b5fc08b00635bccf9134a18978dba13e2250aa51838f9969515a3957847 in /etc/yum.repos.d/.      
# Thu, 18 Dec 2025 07:03:45 GMT
CMD ["/bin/bash"]
# Thu, 18 Dec 2025 07:03:45 GMT
COPY file:595171150af68abc798ea385f7988d74b566aa8e84babff137f00b08b2164683 in /usr/share/buildinfo/content-sets.json      
# Thu, 18 Dec 2025 07:03:45 GMT
COPY file:595171150af68abc798ea385f7988d74b566aa8e84babff137f00b08b2164683 in /root/buildinfo/content_manifests/content-sets.json      
# Thu, 18 Dec 2025 07:03:45 GMT
COPY file:c62fb4530a421926bb6d3aa12f09ef125c8c4fff4293e7e931975ad4241f6f26 in /usr/share/buildinfo/labels.json      
# Thu, 18 Dec 2025 07:03:45 GMT
COPY file:c62fb4530a421926bb6d3aa12f09ef125c8c4fff4293e7e931975ad4241f6f26 in /root/buildinfo/labels.json      
# Thu, 18 Dec 2025 07:03:46 GMT
LABEL "architecture"="ppc64le" "vcs-type"="git" "vcs-ref"="3dbd4aac2bce2ca6b13274bf0662e947c80b18b9" "org.opencontainers.image.revision"="3dbd4aac2bce2ca6b13274bf0662e947c80b18b9" "build-date"="2025-12-18T07:03:33Z" "org.opencontainers.image.created"="2025-12-18T07:03:33Z" "release"="1766033715"org.opencontainers.image.revision=3dbd4aac2bce2ca6b13274bf0662e947c80b18b9,org.opencontainers.image.created=2025-12-18T07:03:33Z
# Thu, 18 Dec 2025 22:39:15 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 18 Dec 2025 22:39:15 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 18 Dec 2025 22:39:15 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 18 Dec 2025 22:39:15 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en         gnupg2     ;     microdnf clean all # buildkit
# Thu, 18 Dec 2025 22:39:15 GMT
ENV JAVA_VERSION=jdk-17.0.17+10
# Thu, 18 Dec 2025 22:41:29 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='dc29ca6d35beb4419b4b00419b8a3dfbf5ae551e1ae2b046b516d9a579d04533';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jdk_aarch64_linux_hotspot_17.0.17_10.tar.gz';          ;;        ppc64le)          ESUM='2a29d1be61940c1bd639018c07f4622e1f145a7ef34e7294fee877e39226d9da';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jdk_ppc64le_linux_hotspot_17.0.17_10.tar.gz';          ;;        s390x)          ESUM='76327b1d00c67f6be91717754fd85fc85ce496d48876f69accb9c53ed31dc546';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jdk_s390x_linux_hotspot_17.0.17_10.tar.gz';          ;;        x86_64)          ESUM='992f96e7995075ac7636bb1a8de52b0c61d71ed3137fafc979ab96b4ab78dd75';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jdk_x64_linux_hotspot_17.0.17_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Thu, 18 Dec 2025 22:41:31 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 18 Dec 2025 22:41:32 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 18 Dec 2025 22:41:32 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 18 Dec 2025 22:41:32 GMT
CMD ["jshell"]
# Fri, 19 Dec 2025 01:03:57 GMT
CMD ["gradle"]
# Fri, 19 Dec 2025 01:03:57 GMT
ENV GRADLE_HOME=/opt/gradle
# Fri, 19 Dec 2025 01:03:57 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 101 gradle     && useradd --system --gid gradle --uid 101 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Fri, 19 Dec 2025 01:03:57 GMT
VOLUME [/home/gradle/.gradle]
# Fri, 19 Dec 2025 01:03:57 GMT
WORKDIR /home/gradle
# Fri, 19 Dec 2025 01:04:10 GMT
RUN set -o errexit -o nounset     && microdnf install -y         make         curl-minimal         wget         tar                 findutils                 unzip         which                 git         git-lfs         subversion     && microdnf clean all         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which svn # buildkit
# Fri, 19 Dec 2025 01:04:10 GMT
ENV GRADLE_VERSION=9.2.1
# Fri, 19 Dec 2025 01:04:10 GMT
ARG GRADLE_DOWNLOAD_SHA256=72f44c9f8ebcb1af43838f45ee5c4aa9c5444898b3468ab3f4af7b6076c5bc3f
# Fri, 19 Dec 2025 01:04:18 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=72f44c9f8ebcb1af43838f45ee5c4aa9c5444898b3468ab3f4af7b6076c5bc3f
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Fri, 19 Dec 2025 01:04:18 GMT
USER gradle
# Fri, 19 Dec 2025 01:04:20 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=72f44c9f8ebcb1af43838f45ee5c4aa9c5444898b3468ab3f4af7b6076c5bc3f
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --stacktrace --debug --version # buildkit
# Fri, 19 Dec 2025 01:04:20 GMT
USER root
```

-	Layers:
	-	`sha256:97de3b33554c63d2e40af1481c1da99bde18eb30eff5e4d230d8ec855811f50c`  
		Last Modified: Thu, 18 Dec 2025 12:14:46 GMT  
		Size: 38.7 MB (38688551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4559e7867acf4f05baf702a54db8a3e2cc5bd1a16c2dcecfa940d5c1ad1b6dfd`  
		Last Modified: Thu, 18 Dec 2025 22:40:19 GMT  
		Size: 57.3 MB (57343233 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a85df18c6dbb78b5ab81911a4f2b8dcbecb7644cb147e1d39f6db9e9e6c7274`  
		Last Modified: Fri, 19 Dec 2025 13:59:40 GMT  
		Size: 144.5 MB (144547846 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd608fb95264e7759f937cd7eb538270370998d72adfe9dc8fb3f82635c94028`  
		Last Modified: Thu, 18 Dec 2025 22:42:22 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abd3d371d3c17a3035a31a196fc0cf23d5214c4eb85bd00f1e8e2925725ba49e`  
		Last Modified: Thu, 18 Dec 2025 22:42:04 GMT  
		Size: 2.3 KB (2289 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a5a58ba3f8a9364493227f9df0c7d74a80f839b36cb607b0ee228bc629facbd`  
		Last Modified: Fri, 19 Dec 2025 01:05:31 GMT  
		Size: 1.6 KB (1627 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8967255553b22e7e19c28e05cc7ecc968ddd69dda388a5ff6ddf7fe14529158`  
		Last Modified: Fri, 19 Dec 2025 01:05:35 GMT  
		Size: 40.9 MB (40864930 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b0d19554b9cdd72f94e9f6f69b3737f01d84e55a09c7d018e2e117768272a81`  
		Last Modified: Fri, 19 Dec 2025 13:59:09 GMT  
		Size: 135.5 MB (135521975 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1aeeae6698160b9be7675240b12023333d61763c7b9c2832beb6e462b6e5c4ca`  
		Last Modified: Fri, 19 Dec 2025 01:05:31 GMT  
		Size: 35.0 KB (35011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:jdk17-ubi` - unknown; unknown

```console
$ docker pull gradle@sha256:f314cb398dfeea571bf118c5cf518e281eccbfb99c15ef996e0165d90ee8aa84
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.9 MB (8942429 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d2e50dcfe8ac37a70f8a8da343c4266e220ceca66f59f4ea1af1300924258ff8`

```dockerfile
```

-	Layers:
	-	`sha256:bb04c846e621286c7671b3142b3c59eab1013b805009bcf0dccd14e56ba65aab`  
		Last Modified: Fri, 19 Dec 2025 03:21:03 GMT  
		Size: 8.9 MB (8917900 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3f0192d93a1ed1f835a2f3d86a584df741064de16f8c2bc4c46756e49561183f`  
		Last Modified: Fri, 19 Dec 2025 03:21:04 GMT  
		Size: 24.5 KB (24529 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:jdk17-ubi` - linux; s390x

```console
$ docker pull gradle@sha256:21df0f08b7dbede12cc3a569917e51e2290af17d729a7de2404f815f7f029593
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **401.8 MB (401829602 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a563faed2c567592ff9bea34844df82a7e96e103a3b6ac14d4ebd710f6873444`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["gradle"]`

```dockerfile
# Thu, 18 Dec 2025 07:10:02 GMT
LABEL maintainer="Red Hat, Inc."
# Thu, 18 Dec 2025 07:10:02 GMT
LABEL vendor="Red Hat, Inc."
# Thu, 18 Dec 2025 07:10:02 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Thu, 18 Dec 2025 07:10:02 GMT
LABEL com.redhat.component="ubi10-minimal-container"       name="ubi10/ubi-minimal"       version="10.1"       cpe="cpe:/o:redhat:enterprise_linux:10.1"       distribution-scope="public"
# Thu, 18 Dec 2025 07:10:02 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Thu, 18 Dec 2025 07:10:02 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 10."
# Thu, 18 Dec 2025 07:10:02 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 18 Dec 2025 07:10:02 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 18 Dec 2025 07:10:02 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 10 Minimal"
# Thu, 18 Dec 2025 07:10:02 GMT
LABEL io.openshift.expose-services=""
# Thu, 18 Dec 2025 07:10:03 GMT
LABEL io.openshift.tags="minimal rhel10"
# Thu, 18 Dec 2025 07:10:03 GMT
ENV container oci
# Thu, 18 Dec 2025 07:10:03 GMT
COPY dir:7d54469de7c29eaa832f7e98c75ae08842b7fae9314e66ea7e9e482c3966eeca in /      
# Thu, 18 Dec 2025 07:10:03 GMT
COPY file:5de33b5fc08b00635bccf9134a18978dba13e2250aa51838f9969515a3957847 in /etc/yum.repos.d/.      
# Thu, 18 Dec 2025 07:10:03 GMT
CMD ["/bin/bash"]
# Thu, 18 Dec 2025 07:10:03 GMT
COPY file:595171150af68abc798ea385f7988d74b566aa8e84babff137f00b08b2164683 in /usr/share/buildinfo/content-sets.json      
# Thu, 18 Dec 2025 07:10:03 GMT
COPY file:595171150af68abc798ea385f7988d74b566aa8e84babff137f00b08b2164683 in /root/buildinfo/content_manifests/content-sets.json      
# Thu, 18 Dec 2025 07:10:03 GMT
COPY file:bea094e4f4ee0e91f623d002425004416b4556dc8f71bf399fffb85c16bafec5 in /usr/share/buildinfo/labels.json      
# Thu, 18 Dec 2025 07:10:03 GMT
COPY file:bea094e4f4ee0e91f623d002425004416b4556dc8f71bf399fffb85c16bafec5 in /root/buildinfo/labels.json      
# Thu, 18 Dec 2025 07:10:03 GMT
LABEL "architecture"="s390x" "vcs-type"="git" "vcs-ref"="3dbd4aac2bce2ca6b13274bf0662e947c80b18b9" "org.opencontainers.image.revision"="3dbd4aac2bce2ca6b13274bf0662e947c80b18b9" "build-date"="2025-12-18T07:07:43Z" "org.opencontainers.image.created"="2025-12-18T07:07:43Z" "release"="1766033715"org.opencontainers.image.revision=3dbd4aac2bce2ca6b13274bf0662e947c80b18b9,org.opencontainers.image.created=2025-12-18T07:07:43Z
# Thu, 18 Dec 2025 22:41:25 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 18 Dec 2025 22:41:25 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 18 Dec 2025 22:41:25 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 18 Dec 2025 22:41:25 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en         gnupg2     ;     microdnf clean all # buildkit
# Thu, 18 Dec 2025 22:41:25 GMT
ENV JAVA_VERSION=jdk-17.0.17+10
# Thu, 18 Dec 2025 22:41:31 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='dc29ca6d35beb4419b4b00419b8a3dfbf5ae551e1ae2b046b516d9a579d04533';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jdk_aarch64_linux_hotspot_17.0.17_10.tar.gz';          ;;        ppc64le)          ESUM='2a29d1be61940c1bd639018c07f4622e1f145a7ef34e7294fee877e39226d9da';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jdk_ppc64le_linux_hotspot_17.0.17_10.tar.gz';          ;;        s390x)          ESUM='76327b1d00c67f6be91717754fd85fc85ce496d48876f69accb9c53ed31dc546';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jdk_s390x_linux_hotspot_17.0.17_10.tar.gz';          ;;        x86_64)          ESUM='992f96e7995075ac7636bb1a8de52b0c61d71ed3137fafc979ab96b4ab78dd75';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jdk_x64_linux_hotspot_17.0.17_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Thu, 18 Dec 2025 22:41:32 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 18 Dec 2025 22:41:32 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 18 Dec 2025 22:41:32 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 18 Dec 2025 22:41:32 GMT
CMD ["jshell"]
# Thu, 18 Dec 2025 23:08:28 GMT
CMD ["gradle"]
# Thu, 18 Dec 2025 23:08:28 GMT
ENV GRADLE_HOME=/opt/gradle
# Thu, 18 Dec 2025 23:08:28 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 101 gradle     && useradd --system --gid gradle --uid 101 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Thu, 18 Dec 2025 23:08:28 GMT
VOLUME [/home/gradle/.gradle]
# Thu, 18 Dec 2025 23:08:28 GMT
WORKDIR /home/gradle
# Thu, 18 Dec 2025 23:08:34 GMT
RUN set -o errexit -o nounset     && microdnf install -y         make         curl-minimal         wget         tar                 findutils                 unzip         which                 git         git-lfs         subversion     && microdnf clean all         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which svn # buildkit
# Thu, 18 Dec 2025 23:08:34 GMT
ENV GRADLE_VERSION=9.2.1
# Thu, 18 Dec 2025 23:08:34 GMT
ARG GRADLE_DOWNLOAD_SHA256=72f44c9f8ebcb1af43838f45ee5c4aa9c5444898b3468ab3f4af7b6076c5bc3f
# Thu, 18 Dec 2025 23:08:38 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=72f44c9f8ebcb1af43838f45ee5c4aa9c5444898b3468ab3f4af7b6076c5bc3f
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Thu, 18 Dec 2025 23:08:38 GMT
USER gradle
# Thu, 18 Dec 2025 23:08:39 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=72f44c9f8ebcb1af43838f45ee5c4aa9c5444898b3468ab3f4af7b6076c5bc3f
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --stacktrace --debug --version # buildkit
# Thu, 18 Dec 2025 23:08:39 GMT
USER root
```

-	Layers:
	-	`sha256:27a76ad55c4b879c1269027dfeec6783f235d82059544eeb7c62ecb7ad66011a`  
		Last Modified: Thu, 18 Dec 2025 12:14:48 GMT  
		Size: 34.3 MB (34340329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df1d3cf471e26ffcdb87047fde314dc15dda443a859121fd8a7f0a4295aa2e08`  
		Last Modified: Thu, 18 Dec 2025 22:41:53 GMT  
		Size: 55.9 MB (55920917 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29262ed9bc3b2acd928fbd26876ee259cdc8bac4893636200d240fafd5e748ed`  
		Last Modified: Fri, 19 Dec 2025 01:53:03 GMT  
		Size: 134.9 MB (134862207 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:807da3ed1e940fab0a5dc01fa92c97f7390e490de3e473bc3ef56ded78956e39`  
		Last Modified: Thu, 18 Dec 2025 22:41:58 GMT  
		Size: 130.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abd3d371d3c17a3035a31a196fc0cf23d5214c4eb85bd00f1e8e2925725ba49e`  
		Last Modified: Thu, 18 Dec 2025 22:42:04 GMT  
		Size: 2.3 KB (2289 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18670fb99db5d2c9f7474f8cf6d2c9287a2b893db540952c659bf16418499fc4`  
		Last Modified: Thu, 18 Dec 2025 23:09:15 GMT  
		Size: 1.6 KB (1619 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec87bb317cf3f3dd5b175aea94d7487fdf9a9e26aa0b87ce9302f68631fb980c`  
		Last Modified: Thu, 18 Dec 2025 23:09:20 GMT  
		Size: 41.1 MB (41145102 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0938db8b1a2e462311f184c9bf0d13b3afa5c6b985203655ca1c6303b06253b1`  
		Last Modified: Thu, 18 Dec 2025 23:09:33 GMT  
		Size: 135.5 MB (135521969 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22a38b841f9475e394b655e9590e05ac69706344b808ca06b9891a898cd12ae3`  
		Last Modified: Thu, 18 Dec 2025 23:09:16 GMT  
		Size: 35.0 KB (35008 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:jdk17-ubi` - unknown; unknown

```console
$ docker pull gradle@sha256:7c952e161ffe987be4f616c05745e2f8b5190ff04d30380ba60168aed52b584f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.9 MB (8931196 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:090acfef398354c127de43e2bcbed658b108aa3a09f83a0347e91bbb83b6beed`

```dockerfile
```

-	Layers:
	-	`sha256:767bd074ab970dab022216f9759f6e099fe2b12bfb7564405d0a09da718adffd`  
		Last Modified: Fri, 19 Dec 2025 00:21:37 GMT  
		Size: 8.9 MB (8906741 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:28afe5fe0f640f80e9203aac0ddb05ffb440f088b8bfcd61849467be70312ba4`  
		Last Modified: Fri, 19 Dec 2025 00:21:44 GMT  
		Size: 24.5 KB (24455 bytes)  
		MIME: application/vnd.in-toto+json
