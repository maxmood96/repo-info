## `gradle:ubi`

```console
$ docker pull gradle@sha256:33c8d70e20e7fdad216e29b176a00d274b77ebcbc65e7e74baf138ea8a83b43e
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

### `gradle:ubi` - linux; amd64

```console
$ docker pull gradle@sha256:dab4f5758830963e37b510958511c541e89677ee42e547a34408bd8a52735bf1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **343.8 MB (343801392 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b0fc5213f65ea8f3d74b53809d2674be35a636829eadb2fa0f8584a53bc024b`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["gradle"]`

```dockerfile
# Mon, 11 May 2026 01:16:15 GMT
LABEL maintainer="Red Hat, Inc."
# Mon, 11 May 2026 01:16:15 GMT
LABEL vendor="Red Hat, Inc."
# Mon, 11 May 2026 01:16:15 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Mon, 11 May 2026 01:16:15 GMT
LABEL com.redhat.component="ubi10-minimal-container"       name="ubi10/ubi-minimal"       version="10.1"       cpe="cpe:/o:redhat:enterprise_linux:10.1"       distribution-scope="public"
# Mon, 11 May 2026 01:16:15 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Mon, 11 May 2026 01:16:15 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 10."
# Mon, 11 May 2026 01:16:15 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 11 May 2026 01:16:15 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 11 May 2026 01:16:15 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 10 Minimal"
# Mon, 11 May 2026 01:16:15 GMT
LABEL io.openshift.expose-services=""
# Mon, 11 May 2026 01:16:15 GMT
LABEL io.openshift.tags="minimal rhel10"
# Mon, 11 May 2026 01:16:15 GMT
ENV container oci
# Mon, 11 May 2026 01:16:15 GMT
COPY dir:944b21b5e56ba1540a32a325c037508b8301ec37c6f3e20f96a07c3b3ab330c2 in /      
# Mon, 11 May 2026 01:16:16 GMT
COPY file:5de33b5fc08b00635bccf9134a18978dba13e2250aa51838f9969515a3957847 in /etc/yum.repos.d/.      
# Mon, 11 May 2026 01:16:16 GMT
CMD ["/bin/bash"]
# Mon, 11 May 2026 01:16:16 GMT
COPY file:595171150af68abc798ea385f7988d74b566aa8e84babff137f00b08b2164683 in /usr/share/buildinfo/content-sets.json      
# Mon, 11 May 2026 01:16:16 GMT
COPY file:595171150af68abc798ea385f7988d74b566aa8e84babff137f00b08b2164683 in /root/buildinfo/content_manifests/content-sets.json      
# Mon, 11 May 2026 01:16:16 GMT
COPY file:2c395ff24a52d293bfab5aa19a14f53b1efe7d5e8864bf90f387296119a55f72 in /usr/share/buildinfo/labels.json      
# Mon, 11 May 2026 01:16:16 GMT
COPY file:2c395ff24a52d293bfab5aa19a14f53b1efe7d5e8864bf90f387296119a55f72 in /root/buildinfo/labels.json      
# Mon, 11 May 2026 01:16:16 GMT
LABEL "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="356ecb8b806b04797740ef169abe27bf41ac3f8c" "org.opencontainers.image.revision"="356ecb8b806b04797740ef169abe27bf41ac3f8c" "build-date"="2026-05-11T01:16:01Z" "org.opencontainers.image.created"="2026-05-11T01:16:01Z" "release"="1778461919"org.opencontainers.image.revision=356ecb8b806b04797740ef169abe27bf41ac3f8c,org.opencontainers.image.created=2026-05-11T01:16:01Z
# Tue, 12 May 2026 00:06:38 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 12 May 2026 00:06:38 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 May 2026 00:06:38 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 12 May 2026 00:06:38 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en         gnupg2     ;     microdnf clean all # buildkit
# Tue, 12 May 2026 00:06:38 GMT
ENV JAVA_VERSION=jdk-25.0.3+9
# Tue, 12 May 2026 00:06:44 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='3e4287cb98870ba824ed698854bdc27cff984254caf66dd12cc291e7bfdde26b';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.3%2B9/OpenJDK25U-jdk_aarch64_linux_hotspot_25.0.3_9.tar.gz';          ;;        ppc64le)          ESUM='72b0fbb201716ca465ab704ec0fb12971abab3fdde5ae8d03b125a273522cf05';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.3%2B9/OpenJDK25U-jdk_ppc64le_linux_hotspot_25.0.3_9.tar.gz';          ;;        s390x)          ESUM='24b497d10acb6ee706ca30e1c8a929785c250cad54c5c12f1f8f93c3c06a53f7';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.3%2B9/OpenJDK25U-jdk_s390x_linux_hotspot_25.0.3_9.tar.gz';          ;;        x86_64)          ESUM='69264a7a211bf5029830d07bc3370f879769d62ebc5b5488e90c9343a2da0e1f';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.3%2B9/OpenJDK25U-jdk_x64_linux_hotspot_25.0.3_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Tue, 12 May 2026 00:06:45 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 12 May 2026 00:06:45 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 12 May 2026 00:06:45 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 12 May 2026 00:06:45 GMT
CMD ["jshell"]
# Tue, 12 May 2026 00:17:22 GMT
CMD ["gradle"]
# Tue, 12 May 2026 00:17:22 GMT
ENV GRADLE_HOME=/opt/gradle
# Tue, 12 May 2026 00:17:22 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 101 gradle     && useradd --system --gid gradle --uid 101 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Tue, 12 May 2026 00:17:22 GMT
VOLUME [/home/gradle/.gradle]
# Tue, 12 May 2026 00:17:22 GMT
WORKDIR /home/gradle
# Tue, 12 May 2026 00:17:26 GMT
RUN set -o errexit -o nounset     && microdnf install -y         make         curl         wget         tar                 findutils                 unzip         which                 git         git-lfs         subversion     && microdnf clean all         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which svn # buildkit
# Tue, 12 May 2026 00:17:26 GMT
ENV GRADLE_VERSION=9.5.0
# Tue, 12 May 2026 00:17:26 GMT
ARG GRADLE_DOWNLOAD_SHA256=553c78f50dafcd54d65b9a444649057857469edf836431389695608536d6b746
# Tue, 12 May 2026 00:17:29 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=553c78f50dafcd54d65b9a444649057857469edf836431389695608536d6b746
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Tue, 12 May 2026 00:17:29 GMT
USER gradle
# Tue, 12 May 2026 00:17:29 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=553c78f50dafcd54d65b9a444649057857469edf836431389695608536d6b746
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --stacktrace --debug --version # buildkit
# Tue, 12 May 2026 00:17:29 GMT
USER root
```

-	Layers:
	-	`sha256:288c81655277add7fa3f1d2c80956ecdc30e861ea53ff003f0eb7d1f488bf24b`  
		Last Modified: Mon, 11 May 2026 02:07:21 GMT  
		Size: 34.6 MB (34622430 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e27a02287ca5c4a6c9d1ca91b2c7e5ed4efdce2614272f36fbc8389c9176355`  
		Last Modified: Tue, 12 May 2026 00:07:03 GMT  
		Size: 37.5 MB (37498212 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79287fe079f67a4ef64ead5b0ac893ac193e3be73fac9f77e722d1df8737a689`  
		Last Modified: Tue, 12 May 2026 00:07:04 GMT  
		Size: 92.6 MB (92579350 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d3f5639c92ee02a17c52f46ecab9e77fb0394e7f2e895655f871c3a64fb677d`  
		Last Modified: Tue, 12 May 2026 00:07:01 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14f9e34d26c44224172663cb730088fdac8b500f93f314afaed741f6d53492c7`  
		Last Modified: Tue, 12 May 2026 00:07:01 GMT  
		Size: 2.3 KB (2290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05bd777bed303f96b1b360f7e47d054db760afd611806c724b28e8a4b25ba6f4`  
		Last Modified: Tue, 12 May 2026 00:17:47 GMT  
		Size: 1.6 KB (1586 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2554db6a1c40f2469eba7c5745e66328423ea1a05dd795f38f78b2102db80935`  
		Last Modified: Tue, 12 May 2026 00:17:49 GMT  
		Size: 38.8 MB (38835855 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d220cd12b08afcc3f83c012f9360de567ae36f22372f4eb742f86b5d87fc38ca`  
		Last Modified: Tue, 12 May 2026 00:17:52 GMT  
		Size: 140.2 MB (140235900 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5165f0805912db9b76f584da42197b4c52f7131f941a1aef689f1727c6189c1b`  
		Last Modified: Tue, 12 May 2026 00:17:47 GMT  
		Size: 25.6 KB (25609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:ubi` - unknown; unknown

```console
$ docker pull gradle@sha256:b232694d527f11aaf860198817b5494811205cc1cbb36ab9e33a62b1169d2a60
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 MB (7049519 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b3791505b3543577c2773c4aae1a3b9dd9af190b53ff95d366364939a36d5cfe`

```dockerfile
```

-	Layers:
	-	`sha256:3a3179344420029db21f2fc4a680a5e7dca34142b3d99ba5e31f22be8c2b5044`  
		Last Modified: Tue, 12 May 2026 00:17:48 GMT  
		Size: 7.0 MB (7024510 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:872f5f77cae20d662e13133dc583fab01844153ca51a4029a16846cfff8045dc`  
		Last Modified: Tue, 12 May 2026 00:17:47 GMT  
		Size: 25.0 KB (25009 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:ubi` - linux; arm64 variant v8

```console
$ docker pull gradle@sha256:e91621ecbc33802c4c0e3a31604b5952c9e10847f2fea0f27464a269c8c6f6f6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **340.3 MB (340331094 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:42cd7ed01a95c968d566e5aca9ca8cfce0593311e606c6877235edf5506a8320`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["gradle"]`

```dockerfile
# Mon, 11 May 2026 01:17:49 GMT
LABEL maintainer="Red Hat, Inc."
# Mon, 11 May 2026 01:17:49 GMT
LABEL vendor="Red Hat, Inc."
# Mon, 11 May 2026 01:17:49 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Mon, 11 May 2026 01:17:49 GMT
LABEL com.redhat.component="ubi10-minimal-container"       name="ubi10/ubi-minimal"       version="10.1"       cpe="cpe:/o:redhat:enterprise_linux:10.1"       distribution-scope="public"
# Mon, 11 May 2026 01:17:49 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Mon, 11 May 2026 01:17:49 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 10."
# Mon, 11 May 2026 01:17:49 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 11 May 2026 01:17:49 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 11 May 2026 01:17:49 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 10 Minimal"
# Mon, 11 May 2026 01:17:49 GMT
LABEL io.openshift.expose-services=""
# Mon, 11 May 2026 01:17:49 GMT
LABEL io.openshift.tags="minimal rhel10"
# Mon, 11 May 2026 01:17:49 GMT
ENV container oci
# Mon, 11 May 2026 01:17:50 GMT
COPY dir:c6e5c961b244885bbae5433f1eb0e567eb7e34fa66cb14c7f643fbc5449440ea in /      
# Mon, 11 May 2026 01:17:50 GMT
COPY file:5de33b5fc08b00635bccf9134a18978dba13e2250aa51838f9969515a3957847 in /etc/yum.repos.d/.      
# Mon, 11 May 2026 01:17:50 GMT
CMD ["/bin/bash"]
# Mon, 11 May 2026 01:17:50 GMT
COPY file:595171150af68abc798ea385f7988d74b566aa8e84babff137f00b08b2164683 in /usr/share/buildinfo/content-sets.json      
# Mon, 11 May 2026 01:17:50 GMT
COPY file:595171150af68abc798ea385f7988d74b566aa8e84babff137f00b08b2164683 in /root/buildinfo/content_manifests/content-sets.json      
# Mon, 11 May 2026 01:17:50 GMT
COPY file:10669f015105b6d7eaedf2ab202dda1098c84203dd610f6bad742d23a54f4858 in /usr/share/buildinfo/labels.json      
# Mon, 11 May 2026 01:17:50 GMT
COPY file:10669f015105b6d7eaedf2ab202dda1098c84203dd610f6bad742d23a54f4858 in /root/buildinfo/labels.json      
# Mon, 11 May 2026 01:17:51 GMT
LABEL "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="356ecb8b806b04797740ef169abe27bf41ac3f8c" "org.opencontainers.image.revision"="356ecb8b806b04797740ef169abe27bf41ac3f8c" "build-date"="2026-05-11T01:17:34Z" "org.opencontainers.image.created"="2026-05-11T01:17:34Z" "release"="1778461919"org.opencontainers.image.revision=356ecb8b806b04797740ef169abe27bf41ac3f8c,org.opencontainers.image.created=2026-05-11T01:17:34Z
# Mon, 11 May 2026 23:59:44 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 11 May 2026 23:59:44 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 11 May 2026 23:59:44 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 11 May 2026 23:59:44 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en         gnupg2     ;     microdnf clean all # buildkit
# Mon, 11 May 2026 23:59:44 GMT
ENV JAVA_VERSION=jdk-25.0.3+9
# Tue, 12 May 2026 00:04:09 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='3e4287cb98870ba824ed698854bdc27cff984254caf66dd12cc291e7bfdde26b';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.3%2B9/OpenJDK25U-jdk_aarch64_linux_hotspot_25.0.3_9.tar.gz';          ;;        ppc64le)          ESUM='72b0fbb201716ca465ab704ec0fb12971abab3fdde5ae8d03b125a273522cf05';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.3%2B9/OpenJDK25U-jdk_ppc64le_linux_hotspot_25.0.3_9.tar.gz';          ;;        s390x)          ESUM='24b497d10acb6ee706ca30e1c8a929785c250cad54c5c12f1f8f93c3c06a53f7';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.3%2B9/OpenJDK25U-jdk_s390x_linux_hotspot_25.0.3_9.tar.gz';          ;;        x86_64)          ESUM='69264a7a211bf5029830d07bc3370f879769d62ebc5b5488e90c9343a2da0e1f';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.3%2B9/OpenJDK25U-jdk_x64_linux_hotspot_25.0.3_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Tue, 12 May 2026 00:04:11 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 12 May 2026 00:04:11 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 12 May 2026 00:04:11 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 12 May 2026 00:04:11 GMT
CMD ["jshell"]
# Tue, 12 May 2026 00:16:36 GMT
CMD ["gradle"]
# Tue, 12 May 2026 00:16:36 GMT
ENV GRADLE_HOME=/opt/gradle
# Tue, 12 May 2026 00:16:36 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 101 gradle     && useradd --system --gid gradle --uid 101 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Tue, 12 May 2026 00:16:36 GMT
VOLUME [/home/gradle/.gradle]
# Tue, 12 May 2026 00:16:36 GMT
WORKDIR /home/gradle
# Tue, 12 May 2026 00:16:42 GMT
RUN set -o errexit -o nounset     && microdnf install -y         make         curl         wget         tar                 findutils                 unzip         which                 git         git-lfs         subversion     && microdnf clean all         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which svn # buildkit
# Tue, 12 May 2026 00:16:42 GMT
ENV GRADLE_VERSION=9.5.0
# Tue, 12 May 2026 00:16:42 GMT
ARG GRADLE_DOWNLOAD_SHA256=553c78f50dafcd54d65b9a444649057857469edf836431389695608536d6b746
# Tue, 12 May 2026 00:16:44 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=553c78f50dafcd54d65b9a444649057857469edf836431389695608536d6b746
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Tue, 12 May 2026 00:16:44 GMT
USER gradle
# Tue, 12 May 2026 00:16:45 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=553c78f50dafcd54d65b9a444649057857469edf836431389695608536d6b746
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --stacktrace --debug --version # buildkit
# Tue, 12 May 2026 00:16:45 GMT
USER root
```

-	Layers:
	-	`sha256:b0d48ca6ae597735e3215ce3085802fb19010a7e5256d1d09af0257d955c5185`  
		Last Modified: Mon, 11 May 2026 02:10:59 GMT  
		Size: 32.7 MB (32747172 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e535de146c71409c11cf88a63583572bd33e66987e6acf72dee80eb746c5b27`  
		Last Modified: Tue, 12 May 2026 00:00:08 GMT  
		Size: 37.4 MB (37444321 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:033fb5cb2c478ea8ddc1651cb52d76999643bb77425646700f2985c5768c509d`  
		Last Modified: Tue, 12 May 2026 00:04:30 GMT  
		Size: 91.5 MB (91548923 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7aa4530e01a8b71adf2b1ec56fd42d0e20d8a823aa50ac8f03d271b618f89a7`  
		Last Modified: Tue, 12 May 2026 00:04:28 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8b9691763aa2845f33f610d268b6620701ed92f47521b2da2c5bd2fae3af2eb`  
		Last Modified: Tue, 12 May 2026 00:04:28 GMT  
		Size: 2.3 KB (2290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab19645d3b3adeb475f8082b4d02a00e00abd59c9c421ffd12c478253518e123`  
		Last Modified: Tue, 12 May 2026 00:17:03 GMT  
		Size: 1.6 KB (1588 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18669b33e0c7e9eb775364e28e02f33c94a07c09060c6baee4e5f1fd26f7d3d0`  
		Last Modified: Tue, 12 May 2026 00:17:06 GMT  
		Size: 38.3 MB (38321405 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91e28165b661298ab83cb7998baa2d23f28d1f3775e5b144da23e5f9a28289ff`  
		Last Modified: Tue, 12 May 2026 00:17:08 GMT  
		Size: 140.2 MB (140235892 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59979a38bde30c3de7b5faef1360722dc2bb20b8f3611b810086ac86ef761795`  
		Last Modified: Tue, 12 May 2026 00:17:04 GMT  
		Size: 29.3 KB (29342 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:ubi` - unknown; unknown

```console
$ docker pull gradle@sha256:073ab5efd26e5193cedba8ca131f8f812e205cc3dcc528e26236d4bf6c908199
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 MB (7048017 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b56bf38d72aba94b3a11a51613313d3c005c2c066d9814ccb3b1db1cd3c36f63`

```dockerfile
```

-	Layers:
	-	`sha256:7ff6ea0cc156bba19d77c00c43d586e49564716148bb29336eadc233b8681268`  
		Last Modified: Tue, 12 May 2026 00:17:04 GMT  
		Size: 7.0 MB (7022787 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ed7bf0284cafb2d51dc105f51029e839453a0950f81622162c50374b05046d2a`  
		Last Modified: Tue, 12 May 2026 00:17:04 GMT  
		Size: 25.2 KB (25230 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:ubi` - linux; ppc64le

```console
$ docker pull gradle@sha256:a749b0a0f24e5bfa1d22bb3d4e754180bf7e28918a995163cc4fa9819b29841f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **350.7 MB (350738961 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf247c7da4a61d96bbe4a56c8347f0b262b5259e0f7ba07e3709b22ec39c0dc5`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["gradle"]`

```dockerfile
# Mon, 11 May 2026 01:17:29 GMT
LABEL maintainer="Red Hat, Inc."
# Mon, 11 May 2026 01:17:29 GMT
LABEL vendor="Red Hat, Inc."
# Mon, 11 May 2026 01:17:29 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Mon, 11 May 2026 01:17:29 GMT
LABEL com.redhat.component="ubi10-minimal-container"       name="ubi10/ubi-minimal"       version="10.1"       cpe="cpe:/o:redhat:enterprise_linux:10.1"       distribution-scope="public"
# Mon, 11 May 2026 01:17:29 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Mon, 11 May 2026 01:17:29 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 10."
# Mon, 11 May 2026 01:17:29 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 11 May 2026 01:17:29 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 11 May 2026 01:17:29 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 10 Minimal"
# Mon, 11 May 2026 01:17:29 GMT
LABEL io.openshift.expose-services=""
# Mon, 11 May 2026 01:17:29 GMT
LABEL io.openshift.tags="minimal rhel10"
# Mon, 11 May 2026 01:17:29 GMT
ENV container oci
# Mon, 11 May 2026 01:17:29 GMT
COPY dir:f86ae0d0c4a87090459f5dd2e52db1242d0bf9305bb73e66dc55f51f70971c00 in /      
# Mon, 11 May 2026 01:17:29 GMT
COPY file:5de33b5fc08b00635bccf9134a18978dba13e2250aa51838f9969515a3957847 in /etc/yum.repos.d/.      
# Mon, 11 May 2026 01:17:29 GMT
CMD ["/bin/bash"]
# Mon, 11 May 2026 01:17:29 GMT
COPY file:595171150af68abc798ea385f7988d74b566aa8e84babff137f00b08b2164683 in /usr/share/buildinfo/content-sets.json      
# Mon, 11 May 2026 01:17:30 GMT
COPY file:595171150af68abc798ea385f7988d74b566aa8e84babff137f00b08b2164683 in /root/buildinfo/content_manifests/content-sets.json      
# Mon, 11 May 2026 01:17:30 GMT
COPY file:3937609775d6da2876c2843dd2634469abf69886b03de03bc99d3e8daa564f9c in /usr/share/buildinfo/labels.json      
# Mon, 11 May 2026 01:17:30 GMT
COPY file:3937609775d6da2876c2843dd2634469abf69886b03de03bc99d3e8daa564f9c in /root/buildinfo/labels.json      
# Mon, 11 May 2026 01:17:30 GMT
LABEL "architecture"="ppc64le" "vcs-type"="git" "vcs-ref"="356ecb8b806b04797740ef169abe27bf41ac3f8c" "org.opencontainers.image.revision"="356ecb8b806b04797740ef169abe27bf41ac3f8c" "build-date"="2026-05-11T01:17:17Z" "org.opencontainers.image.created"="2026-05-11T01:17:17Z" "release"="1778461919"org.opencontainers.image.revision=356ecb8b806b04797740ef169abe27bf41ac3f8c,org.opencontainers.image.created=2026-05-11T01:17:17Z
# Tue, 12 May 2026 00:28:47 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 12 May 2026 00:28:47 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 May 2026 00:28:47 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 12 May 2026 00:28:47 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en         gnupg2     ;     microdnf clean all # buildkit
# Tue, 12 May 2026 00:28:47 GMT
ENV JAVA_VERSION=jdk-25.0.3+9
# Tue, 12 May 2026 00:36:34 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='3e4287cb98870ba824ed698854bdc27cff984254caf66dd12cc291e7bfdde26b';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.3%2B9/OpenJDK25U-jdk_aarch64_linux_hotspot_25.0.3_9.tar.gz';          ;;        ppc64le)          ESUM='72b0fbb201716ca465ab704ec0fb12971abab3fdde5ae8d03b125a273522cf05';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.3%2B9/OpenJDK25U-jdk_ppc64le_linux_hotspot_25.0.3_9.tar.gz';          ;;        s390x)          ESUM='24b497d10acb6ee706ca30e1c8a929785c250cad54c5c12f1f8f93c3c06a53f7';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.3%2B9/OpenJDK25U-jdk_s390x_linux_hotspot_25.0.3_9.tar.gz';          ;;        x86_64)          ESUM='69264a7a211bf5029830d07bc3370f879769d62ebc5b5488e90c9343a2da0e1f';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.3%2B9/OpenJDK25U-jdk_x64_linux_hotspot_25.0.3_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Tue, 12 May 2026 00:36:37 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 12 May 2026 00:36:37 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 12 May 2026 00:36:37 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 12 May 2026 00:36:37 GMT
CMD ["jshell"]
# Tue, 12 May 2026 01:11:17 GMT
CMD ["gradle"]
# Tue, 12 May 2026 01:11:17 GMT
ENV GRADLE_HOME=/opt/gradle
# Tue, 12 May 2026 01:11:17 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 101 gradle     && useradd --system --gid gradle --uid 101 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Tue, 12 May 2026 01:11:17 GMT
VOLUME [/home/gradle/.gradle]
# Tue, 12 May 2026 01:11:18 GMT
WORKDIR /home/gradle
# Tue, 12 May 2026 01:11:39 GMT
RUN set -o errexit -o nounset     && microdnf install -y         make         curl         wget         tar                 findutils                 unzip         which                 git         git-lfs         subversion     && microdnf clean all         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which svn # buildkit
# Tue, 12 May 2026 01:11:39 GMT
ENV GRADLE_VERSION=9.5.0
# Tue, 12 May 2026 01:11:39 GMT
ARG GRADLE_DOWNLOAD_SHA256=553c78f50dafcd54d65b9a444649057857469edf836431389695608536d6b746
# Tue, 12 May 2026 01:11:45 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=553c78f50dafcd54d65b9a444649057857469edf836431389695608536d6b746
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Tue, 12 May 2026 01:11:45 GMT
USER gradle
# Tue, 12 May 2026 01:11:46 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=553c78f50dafcd54d65b9a444649057857469edf836431389695608536d6b746
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --stacktrace --debug --version # buildkit
# Tue, 12 May 2026 01:11:46 GMT
USER root
```

-	Layers:
	-	`sha256:dfc37eccb37a052e4fa7be870ee6db7544ef15834a2dfa05156adc7b3f0064f8`  
		Last Modified: Mon, 11 May 2026 06:17:19 GMT  
		Size: 38.8 MB (38752382 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5b57514fb022bd5104b331922465798e8b81622c1daf6f728be81eb5ba7748c`  
		Last Modified: Tue, 12 May 2026 00:29:32 GMT  
		Size: 39.3 MB (39255864 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04b3e0a17c41cf7a5aeeae7acf147ced94823f541e783d57985b9a264ed137ea`  
		Last Modified: Tue, 12 May 2026 00:37:12 GMT  
		Size: 91.9 MB (91912868 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee8848dd7093dce3e02ee5be98786e5f6a7fec15530792f8d3f3b9467eeecf09`  
		Last Modified: Tue, 12 May 2026 00:37:10 GMT  
		Size: 130.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0788b12adc948478cf16ea6cf9c50be9c22cee18703ddc6310c9d627b0e017e`  
		Last Modified: Tue, 12 May 2026 00:37:10 GMT  
		Size: 2.3 KB (2289 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9203850d63f38a223a38927543403af9af7f30af1bd0994c17c6aa5fd46866de`  
		Last Modified: Tue, 12 May 2026 01:12:26 GMT  
		Size: 1.6 KB (1583 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:caa664cc852e71d8383801c5f63dae7efadd3da6a70753a9212465fa513a4328`  
		Last Modified: Tue, 12 May 2026 01:12:29 GMT  
		Size: 40.6 MB (40577529 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3391922483a4a2a05ccfd56ced7a2657050c738d95604bc0e6fab8825c6a894e`  
		Last Modified: Tue, 12 May 2026 01:12:31 GMT  
		Size: 140.2 MB (140235906 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f291e2b74f02c8aa3778f1af9cd6be46f43fe4b724fab15d8c0bb1a4691f3d12`  
		Last Modified: Tue, 12 May 2026 01:12:27 GMT  
		Size: 378.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:ubi` - unknown; unknown

```console
$ docker pull gradle@sha256:367a53c4f0402fb6d0234aa3be857defba233509250d82510db25a4bede842c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 MB (7024345 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe766c5b8b602105f9e7b742d26be932c253094d2fe5d069c618edc627dbda28`

```dockerfile
```

-	Layers:
	-	`sha256:6cf787bc368a4d2515ed5d5bd6340c362740987b4e99304ebfcae6fdfec86a93`  
		Last Modified: Tue, 12 May 2026 01:12:28 GMT  
		Size: 7.0 MB (6999252 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:96bcc1fbe50b2200e6134ceeb412fd56c55aebd416e49610aaa359ca2be90c13`  
		Last Modified: Tue, 12 May 2026 01:12:27 GMT  
		Size: 25.1 KB (25093 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:ubi` - linux; s390x

```console
$ docker pull gradle@sha256:6fe25a52162cb8635a82ccfd0371da22f5cc0939f47aa8b2e0af8699d1c5c158
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **341.9 MB (341917993 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:083e5a1024b9366594ae3be85aa572e589df4ab45fb0b83d639d87d969168462`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["gradle"]`

```dockerfile
# Mon, 11 May 2026 01:23:16 GMT
LABEL maintainer="Red Hat, Inc."
# Mon, 11 May 2026 01:23:16 GMT
LABEL vendor="Red Hat, Inc."
# Mon, 11 May 2026 01:23:16 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Mon, 11 May 2026 01:23:16 GMT
LABEL com.redhat.component="ubi10-minimal-container"       name="ubi10/ubi-minimal"       version="10.1"       cpe="cpe:/o:redhat:enterprise_linux:10.1"       distribution-scope="public"
# Mon, 11 May 2026 01:23:16 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Mon, 11 May 2026 01:23:16 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 10."
# Mon, 11 May 2026 01:23:16 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 11 May 2026 01:23:16 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 11 May 2026 01:23:16 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 10 Minimal"
# Mon, 11 May 2026 01:23:16 GMT
LABEL io.openshift.expose-services=""
# Mon, 11 May 2026 01:23:16 GMT
LABEL io.openshift.tags="minimal rhel10"
# Mon, 11 May 2026 01:23:16 GMT
ENV container oci
# Mon, 11 May 2026 01:23:17 GMT
COPY dir:0579bc85c05b217dd77b2ce225f64d3cb10f81a6a3726b91387ffbc978d6e453 in /      
# Mon, 11 May 2026 01:23:17 GMT
COPY file:5de33b5fc08b00635bccf9134a18978dba13e2250aa51838f9969515a3957847 in /etc/yum.repos.d/.      
# Mon, 11 May 2026 01:23:17 GMT
CMD ["/bin/bash"]
# Mon, 11 May 2026 01:23:17 GMT
COPY file:595171150af68abc798ea385f7988d74b566aa8e84babff137f00b08b2164683 in /usr/share/buildinfo/content-sets.json      
# Mon, 11 May 2026 01:23:17 GMT
COPY file:595171150af68abc798ea385f7988d74b566aa8e84babff137f00b08b2164683 in /root/buildinfo/content_manifests/content-sets.json      
# Mon, 11 May 2026 01:23:17 GMT
COPY file:81f827a1784652793e747198fea65ce1ad402e9b3c1587adce62db262e60fb88 in /usr/share/buildinfo/labels.json      
# Mon, 11 May 2026 01:23:17 GMT
COPY file:81f827a1784652793e747198fea65ce1ad402e9b3c1587adce62db262e60fb88 in /root/buildinfo/labels.json      
# Mon, 11 May 2026 01:23:17 GMT
LABEL "architecture"="s390x" "vcs-type"="git" "vcs-ref"="356ecb8b806b04797740ef169abe27bf41ac3f8c" "org.opencontainers.image.revision"="356ecb8b806b04797740ef169abe27bf41ac3f8c" "build-date"="2026-05-11T01:22:36Z" "org.opencontainers.image.created"="2026-05-11T01:22:36Z" "release"="1778461919"org.opencontainers.image.revision=356ecb8b806b04797740ef169abe27bf41ac3f8c,org.opencontainers.image.created=2026-05-11T01:22:36Z
# Tue, 12 May 2026 00:00:32 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 12 May 2026 00:00:32 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 May 2026 00:00:32 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 12 May 2026 00:00:32 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en         gnupg2     ;     microdnf clean all # buildkit
# Tue, 12 May 2026 00:00:32 GMT
ENV JAVA_VERSION=jdk-25.0.3+9
# Tue, 12 May 2026 00:03:06 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='3e4287cb98870ba824ed698854bdc27cff984254caf66dd12cc291e7bfdde26b';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.3%2B9/OpenJDK25U-jdk_aarch64_linux_hotspot_25.0.3_9.tar.gz';          ;;        ppc64le)          ESUM='72b0fbb201716ca465ab704ec0fb12971abab3fdde5ae8d03b125a273522cf05';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.3%2B9/OpenJDK25U-jdk_ppc64le_linux_hotspot_25.0.3_9.tar.gz';          ;;        s390x)          ESUM='24b497d10acb6ee706ca30e1c8a929785c250cad54c5c12f1f8f93c3c06a53f7';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.3%2B9/OpenJDK25U-jdk_s390x_linux_hotspot_25.0.3_9.tar.gz';          ;;        x86_64)          ESUM='69264a7a211bf5029830d07bc3370f879769d62ebc5b5488e90c9343a2da0e1f';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.3%2B9/OpenJDK25U-jdk_x64_linux_hotspot_25.0.3_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Tue, 12 May 2026 00:03:07 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 12 May 2026 00:03:08 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 12 May 2026 00:03:08 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 12 May 2026 00:03:08 GMT
CMD ["jshell"]
# Tue, 12 May 2026 00:12:42 GMT
CMD ["gradle"]
# Tue, 12 May 2026 00:12:42 GMT
ENV GRADLE_HOME=/opt/gradle
# Tue, 12 May 2026 00:12:42 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 101 gradle     && useradd --system --gid gradle --uid 101 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Tue, 12 May 2026 00:12:42 GMT
VOLUME [/home/gradle/.gradle]
# Tue, 12 May 2026 00:12:42 GMT
WORKDIR /home/gradle
# Tue, 12 May 2026 00:12:47 GMT
RUN set -o errexit -o nounset     && microdnf install -y         make         curl         wget         tar                 findutils                 unzip         which                 git         git-lfs         subversion     && microdnf clean all         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which svn # buildkit
# Tue, 12 May 2026 00:12:47 GMT
ENV GRADLE_VERSION=9.5.0
# Tue, 12 May 2026 00:12:47 GMT
ARG GRADLE_DOWNLOAD_SHA256=553c78f50dafcd54d65b9a444649057857469edf836431389695608536d6b746
# Tue, 12 May 2026 00:12:50 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=553c78f50dafcd54d65b9a444649057857469edf836431389695608536d6b746
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Tue, 12 May 2026 00:12:50 GMT
USER gradle
# Tue, 12 May 2026 00:12:51 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=553c78f50dafcd54d65b9a444649057857469edf836431389695608536d6b746
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --stacktrace --debug --version # buildkit
# Tue, 12 May 2026 00:12:51 GMT
USER root
```

-	Layers:
	-	`sha256:c8191d3132a8f64ba77e2e7e35ea28fba961048b0be562036986e4b4138e5000`  
		Last Modified: Mon, 11 May 2026 06:17:00 GMT  
		Size: 34.4 MB (34447893 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48e45d6f5b7b2ae6b57d4c8f61a19d4016477e8b833954767b9f45a07aaccf21`  
		Last Modified: Tue, 12 May 2026 00:00:54 GMT  
		Size: 37.9 MB (37883315 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10d9c6a0bb2e8553d00a7534776d0de69a8d3c8335f45789719560fe38ed8e3f`  
		Last Modified: Tue, 12 May 2026 00:03:32 GMT  
		Size: 88.4 MB (88421668 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:453b8114bccb4301ccffdb7c467507d1eab906b492639942c1bc63f87953b65d`  
		Last Modified: Tue, 12 May 2026 00:03:30 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:942875047dfaa4c900ced58665fac899818215d5f249ab42c855b373919f479d`  
		Last Modified: Tue, 12 May 2026 00:03:25 GMT  
		Size: 2.3 KB (2291 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98e00d0e3ae7af73fd351ddfd1be9c865ede552c4713265facdab3e4b303bdff`  
		Last Modified: Tue, 12 May 2026 00:13:18 GMT  
		Size: 1.6 KB (1583 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1213ea192258cdc1e1d82aa00388bf1180729bf70caf7cf51f89c28f7edd9526`  
		Last Modified: Tue, 12 May 2026 00:13:19 GMT  
		Size: 40.9 MB (40924806 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6b1f3e1bbc94b98234504c2d40055fae25876ca6de6cc0016c16d7df15928c3`  
		Last Modified: Tue, 12 May 2026 00:13:22 GMT  
		Size: 140.2 MB (140235903 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0393f8c865cb2d8607aab383eb21f3c1f70b24b80750b23c3feee6d01afa1aa0`  
		Last Modified: Tue, 12 May 2026 00:13:18 GMT  
		Size: 374.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:ubi` - unknown; unknown

```console
$ docker pull gradle@sha256:defb808b9449d4973588696c3e08af354b059e3a651dc999704d1d9542063b9f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 MB (7014726 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:446d342a6f76a26b9f857c6176ee32f1dfce76609450104de07081f8a529dfd7`

```dockerfile
```

-	Layers:
	-	`sha256:8149e71b695c8b97c6fbd4ddcc5cd1749fa7279ad95badc87ded30f69c8df4de`  
		Last Modified: Tue, 12 May 2026 00:13:18 GMT  
		Size: 7.0 MB (6989719 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a2a1193f11021dad2d7622fa0da777a5a1c8fde217cec0c99232e6f0f92bcefe`  
		Last Modified: Tue, 12 May 2026 00:13:18 GMT  
		Size: 25.0 KB (25007 bytes)  
		MIME: application/vnd.in-toto+json
