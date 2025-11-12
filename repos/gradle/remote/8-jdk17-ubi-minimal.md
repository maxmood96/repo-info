## `gradle:8-jdk17-ubi-minimal`

```console
$ docker pull gradle@sha256:28319950c5026895397647687ddc27411a5ef925a80fa261394259665faeb6ff
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

### `gradle:8-jdk17-ubi-minimal` - linux; amd64

```console
$ docker pull gradle@sha256:911bb4ac04d55d24aa6c9810b50cf5442383ff20f52ed9f4059bd07af85af7a9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **387.0 MB (387021380 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c4aefd1b4a4380be9603f37557428b96bc2689345719341dc94e1b83b83d6df1`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["gradle"]`

```dockerfile
# Mon, 03 Nov 2025 14:28:07 GMT
LABEL maintainer="Red Hat, Inc."
# Mon, 03 Nov 2025 14:28:07 GMT
LABEL vendor="Red Hat, Inc."
# Mon, 03 Nov 2025 14:28:07 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Mon, 03 Nov 2025 14:28:07 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.7"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Mon, 03 Nov 2025 14:28:07 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Mon, 03 Nov 2025 14:28:07 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Mon, 03 Nov 2025 14:28:07 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 03 Nov 2025 14:28:07 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 03 Nov 2025 14:28:07 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Mon, 03 Nov 2025 14:28:07 GMT
LABEL io.openshift.expose-services=""
# Mon, 03 Nov 2025 14:28:07 GMT
LABEL io.openshift.tags="minimal rhel9"
# Mon, 03 Nov 2025 14:28:07 GMT
LABEL compose-id="RHEL-9.7.0-updates-20251029.7"
# Mon, 03 Nov 2025 14:28:07 GMT
ENV container oci
# Mon, 03 Nov 2025 14:28:08 GMT
COPY dir:39710e73aef560d625154347dc7e6b417064723d33d900483645d9d706c0f7a2 in /      
# Mon, 03 Nov 2025 14:28:08 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Mon, 03 Nov 2025 14:28:08 GMT
CMD ["/bin/bash"]
# Mon, 03 Nov 2025 14:28:08 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /usr/share/buildinfo/content-sets.json      
# Mon, 03 Nov 2025 14:28:08 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /root/buildinfo/content_manifests/content-sets.json      
# Mon, 03 Nov 2025 14:28:08 GMT
COPY file:90c5e1a95185d091ee07721ff43a8413d78a6f7cb920f7ce46a03a173e5f926a in /usr/share/buildinfo/labels.json      
# Mon, 03 Nov 2025 14:28:08 GMT
COPY file:90c5e1a95185d091ee07721ff43a8413d78a6f7cb920f7ce46a03a173e5f926a in /root/buildinfo/labels.json      
# Mon, 03 Nov 2025 14:28:09 GMT
LABEL "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="02d02ad5d9d5ef0add399eb1c8d5f2a4b9261204" "org.opencontainers.image.revision"="02d02ad5d9d5ef0add399eb1c8d5f2a4b9261204" "build-date"="2025-11-03T14:27:54Z" "release"="1762180032"org.opencontainers.image.revision=02d02ad5d9d5ef0add399eb1c8d5f2a4b9261204
# Wed, 12 Nov 2025 00:27:03 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 12 Nov 2025 00:27:03 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 12 Nov 2025 00:27:03 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 12 Nov 2025 00:27:03 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en     ;     microdnf clean all # buildkit
# Wed, 12 Nov 2025 00:27:03 GMT
ENV JAVA_VERSION=jdk-17.0.17+10
# Wed, 12 Nov 2025 00:27:10 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='dc29ca6d35beb4419b4b00419b8a3dfbf5ae551e1ae2b046b516d9a579d04533';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jdk_aarch64_linux_hotspot_17.0.17_10.tar.gz';          ;;        ppc64le)          ESUM='2a29d1be61940c1bd639018c07f4622e1f145a7ef34e7294fee877e39226d9da';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jdk_ppc64le_linux_hotspot_17.0.17_10.tar.gz';          ;;        s390x)          ESUM='76327b1d00c67f6be91717754fd85fc85ce496d48876f69accb9c53ed31dc546';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jdk_s390x_linux_hotspot_17.0.17_10.tar.gz';          ;;        x86_64)          ESUM='992f96e7995075ac7636bb1a8de52b0c61d71ed3137fafc979ab96b4ab78dd75';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jdk_x64_linux_hotspot_17.0.17_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Wed, 12 Nov 2025 00:27:11 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 12 Nov 2025 00:27:11 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 12 Nov 2025 00:27:11 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 12 Nov 2025 00:27:11 GMT
CMD ["jshell"]
# Wed, 12 Nov 2025 01:11:27 GMT
CMD ["gradle"]
# Wed, 12 Nov 2025 01:11:27 GMT
ENV GRADLE_HOME=/opt/gradle
# Wed, 12 Nov 2025 01:11:27 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 101 gradle     && useradd --system --gid gradle --uid 101 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Wed, 12 Nov 2025 01:11:27 GMT
VOLUME [/home/gradle/.gradle]
# Wed, 12 Nov 2025 01:11:27 GMT
WORKDIR /home/gradle
# Wed, 12 Nov 2025 01:11:31 GMT
RUN set -o errexit -o nounset     && microdnf install -y         make                 findutils                 unzip         which                 git         git-lfs         subversion     && microdnf clean all         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which svn # buildkit
# Wed, 12 Nov 2025 01:11:31 GMT
ENV GRADLE_VERSION=8.14.3
# Wed, 12 Nov 2025 01:11:31 GMT
ARG GRADLE_DOWNLOAD_SHA256=bd71102213493060956ec229d946beee57158dbd89d0e62b91bca0fa2c5f3531
# Wed, 12 Nov 2025 01:11:35 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=bd71102213493060956ec229d946beee57158dbd89d0e62b91bca0fa2c5f3531
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Wed, 12 Nov 2025 01:11:35 GMT
USER gradle
# Wed, 12 Nov 2025 01:11:36 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=bd71102213493060956ec229d946beee57158dbd89d0e62b91bca0fa2c5f3531
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Wed, 12 Nov 2025 01:11:36 GMT
USER root
```

-	Layers:
	-	`sha256:ef1934e719674e24c0e9879fad65a4a167d4510bb71da2c3ed5e85f5d800bd89`  
		Last Modified: Tue, 11 Nov 2025 17:18:44 GMT  
		Size: 40.0 MB (40000743 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:249d178bda30c43daf7695e582dcecd47610e85fc4ddcf25321478d42c77c8d3`  
		Last Modified: Wed, 12 Nov 2025 00:27:40 GMT  
		Size: 27.7 MB (27693602 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3bed90e6312090bd04f5469822362518e24edee47975c956ff2aa94f69a312b`  
		Last Modified: Wed, 12 Nov 2025 01:11:18 GMT  
		Size: 144.9 MB (144852864 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:714cd9b228db7971f6302bd821e59337bddf43069061c351cbed1d5ba9efbaef`  
		Last Modified: Wed, 12 Nov 2025 00:27:37 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abc477993c5d54a5c4d99a80e1aadd0eb02c3abf5c46277c4a60a012344bed4c`  
		Last Modified: Wed, 12 Nov 2025 00:27:37 GMT  
		Size: 2.3 KB (2291 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ed5c5b7ac5a465d7504dab5c53a1793875964972931e6e52727718896094784`  
		Last Modified: Wed, 12 Nov 2025 01:12:02 GMT  
		Size: 1.7 KB (1708 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c693e73093d097fe583a18e7268696e94d725df893341d54416810fdf58956fc`  
		Last Modified: Wed, 12 Nov 2025 01:12:05 GMT  
		Size: 37.0 MB (37019905 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2cbefcfce9a1d1677440754853ca2b56810a33bc5b0f5676e1ed50b2c39950e9`  
		Last Modified: Wed, 12 Nov 2025 04:33:29 GMT  
		Size: 137.4 MB (137395200 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05daf37dce68257ba97adfa6cf5c459a65b347988d9b2f87dfab5d8d078ed3c1`  
		Last Modified: Wed, 12 Nov 2025 01:12:01 GMT  
		Size: 54.9 KB (54906 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:8-jdk17-ubi-minimal` - unknown; unknown

```console
$ docker pull gradle@sha256:c42580852da7a8d680a8fac80bd03c3338917d1f5e889bca4526bed66abb6138
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5426277 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9918ce3fa0ad82008995505e097710e1e3d58ff5b40edcaa2c773b2df61703e6`

```dockerfile
```

-	Layers:
	-	`sha256:df810dbd2b11a4ef25f4afb01d65e4f7c65b02b1aa0bba42cf9441563fbab3c9`  
		Last Modified: Wed, 12 Nov 2025 03:21:34 GMT  
		Size: 5.4 MB (5402678 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7b8a3a6583a869c01d41074f9572b5dd7eb1b5af2a405f400ae237050aece704`  
		Last Modified: Wed, 12 Nov 2025 03:21:35 GMT  
		Size: 23.6 KB (23599 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:8-jdk17-ubi-minimal` - linux; arm64 variant v8

```console
$ docker pull gradle@sha256:9bafe58e596094886dc487d7059ae1d004aea445ab9433f30dc7111b18f409a3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **383.9 MB (383878366 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1200b3d907f8594e5f460cb5777bb0543fc9c8844490933139ac5b17c58e0bb4`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["gradle"]`

```dockerfile
# Mon, 03 Nov 2025 14:39:20 GMT
LABEL maintainer="Red Hat, Inc."
# Mon, 03 Nov 2025 14:39:20 GMT
LABEL vendor="Red Hat, Inc."
# Mon, 03 Nov 2025 14:39:20 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Mon, 03 Nov 2025 14:39:20 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.7"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Mon, 03 Nov 2025 14:39:20 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Mon, 03 Nov 2025 14:39:20 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Mon, 03 Nov 2025 14:39:20 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 03 Nov 2025 14:39:20 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 03 Nov 2025 14:39:20 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Mon, 03 Nov 2025 14:39:20 GMT
LABEL io.openshift.expose-services=""
# Mon, 03 Nov 2025 14:39:20 GMT
LABEL io.openshift.tags="minimal rhel9"
# Mon, 03 Nov 2025 14:39:20 GMT
LABEL compose-id="RHEL-9.7.0-updates-20251029.7"
# Mon, 03 Nov 2025 14:39:20 GMT
ENV container oci
# Mon, 03 Nov 2025 14:39:21 GMT
COPY dir:e6638cbef7baa2be94a007ecfd2531710d358328001d7cc1a125e3837ced3f20 in /      
# Mon, 03 Nov 2025 14:39:21 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Mon, 03 Nov 2025 14:39:21 GMT
CMD ["/bin/bash"]
# Mon, 03 Nov 2025 14:39:21 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /usr/share/buildinfo/content-sets.json      
# Mon, 03 Nov 2025 14:39:21 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /root/buildinfo/content_manifests/content-sets.json      
# Mon, 03 Nov 2025 14:39:21 GMT
COPY file:e6c4ae052c98b0a8455fbdd83ea8c94d3ab007cf48a3ddf7f4cddb8006394bb4 in /usr/share/buildinfo/labels.json      
# Mon, 03 Nov 2025 14:39:21 GMT
COPY file:e6c4ae052c98b0a8455fbdd83ea8c94d3ab007cf48a3ddf7f4cddb8006394bb4 in /root/buildinfo/labels.json      
# Mon, 03 Nov 2025 14:39:21 GMT
LABEL "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="02d02ad5d9d5ef0add399eb1c8d5f2a4b9261204" "org.opencontainers.image.revision"="02d02ad5d9d5ef0add399eb1c8d5f2a4b9261204" "build-date"="2025-11-03T14:39:04Z" "release"="1762180032"org.opencontainers.image.revision=02d02ad5d9d5ef0add399eb1c8d5f2a4b9261204
# Wed, 12 Nov 2025 00:26:43 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 12 Nov 2025 00:26:43 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 12 Nov 2025 00:26:43 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 12 Nov 2025 00:26:43 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en     ;     microdnf clean all # buildkit
# Wed, 12 Nov 2025 00:26:43 GMT
ENV JAVA_VERSION=jdk-17.0.17+10
# Wed, 12 Nov 2025 00:26:51 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='dc29ca6d35beb4419b4b00419b8a3dfbf5ae551e1ae2b046b516d9a579d04533';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jdk_aarch64_linux_hotspot_17.0.17_10.tar.gz';          ;;        ppc64le)          ESUM='2a29d1be61940c1bd639018c07f4622e1f145a7ef34e7294fee877e39226d9da';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jdk_ppc64le_linux_hotspot_17.0.17_10.tar.gz';          ;;        s390x)          ESUM='76327b1d00c67f6be91717754fd85fc85ce496d48876f69accb9c53ed31dc546';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jdk_s390x_linux_hotspot_17.0.17_10.tar.gz';          ;;        x86_64)          ESUM='992f96e7995075ac7636bb1a8de52b0c61d71ed3137fafc979ab96b4ab78dd75';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jdk_x64_linux_hotspot_17.0.17_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Wed, 12 Nov 2025 00:26:52 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 12 Nov 2025 00:26:52 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 12 Nov 2025 00:26:52 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 12 Nov 2025 00:26:52 GMT
CMD ["jshell"]
# Wed, 12 Nov 2025 01:11:02 GMT
CMD ["gradle"]
# Wed, 12 Nov 2025 01:11:02 GMT
ENV GRADLE_HOME=/opt/gradle
# Wed, 12 Nov 2025 01:11:02 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 101 gradle     && useradd --system --gid gradle --uid 101 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Wed, 12 Nov 2025 01:11:02 GMT
VOLUME [/home/gradle/.gradle]
# Wed, 12 Nov 2025 01:11:02 GMT
WORKDIR /home/gradle
# Wed, 12 Nov 2025 01:11:08 GMT
RUN set -o errexit -o nounset     && microdnf install -y         make                 findutils                 unzip         which                 git         git-lfs         subversion     && microdnf clean all         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which svn # buildkit
# Wed, 12 Nov 2025 01:11:08 GMT
ENV GRADLE_VERSION=8.14.3
# Wed, 12 Nov 2025 01:11:08 GMT
ARG GRADLE_DOWNLOAD_SHA256=bd71102213493060956ec229d946beee57158dbd89d0e62b91bca0fa2c5f3531
# Wed, 12 Nov 2025 01:11:11 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=bd71102213493060956ec229d946beee57158dbd89d0e62b91bca0fa2c5f3531
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Wed, 12 Nov 2025 01:11:11 GMT
USER gradle
# Wed, 12 Nov 2025 01:11:11 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=bd71102213493060956ec229d946beee57158dbd89d0e62b91bca0fa2c5f3531
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Wed, 12 Nov 2025 01:11:11 GMT
USER root
```

-	Layers:
	-	`sha256:fccdcd3fc47f898d65f9d4531d01539ce33a7ec8038500d557bfe58eb4b6ae87`  
		Last Modified: Tue, 11 Nov 2025 18:10:59 GMT  
		Size: 38.2 MB (38211473 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7fddb067dc6727b2c9805cd87eae853409ac4ae59175c3cd14fe5555f6c29060`  
		Last Modified: Wed, 12 Nov 2025 00:27:21 GMT  
		Size: 28.1 MB (28122922 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80316948064aeba97e92e9d3b1739510de46d661d133291acca1a590eb371b27`  
		Last Modified: Wed, 12 Nov 2025 01:10:58 GMT  
		Size: 143.7 MB (143685356 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2f19d8c92f81cfb06df2cd6e5dfc99570906fb39358581d1b2f1c01e547479c`  
		Last Modified: Wed, 12 Nov 2025 00:27:19 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f8a34f63a93d3d2e4024baa33bbd40b59a0d1ef95c4bbfe5205a36f2a05ebca`  
		Last Modified: Wed, 12 Nov 2025 00:27:19 GMT  
		Size: 2.3 KB (2290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a1a057aec17354f8dabdd61c80dd65d9a72a03c03d4e8d4e917a1218e56d676`  
		Last Modified: Wed, 12 Nov 2025 01:11:40 GMT  
		Size: 1.7 KB (1707 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dec818f904a77af840dfa0aa88fa37ae35dc662a5bafaf680c0b861a4a091396`  
		Last Modified: Wed, 12 Nov 2025 01:11:44 GMT  
		Size: 36.4 MB (36399728 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b815fc7f8190cb70a9177de8467bfaa1efb22e61507cfd112cc7eabab546dc3d`  
		Last Modified: Wed, 12 Nov 2025 18:56:46 GMT  
		Size: 137.4 MB (137395201 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12062e3e20c8546d92ab4f216ca9dc8a6eecafde8dfb008b16bbdc117cf791a9`  
		Last Modified: Wed, 12 Nov 2025 01:11:40 GMT  
		Size: 59.5 KB (59529 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:8-jdk17-ubi-minimal` - unknown; unknown

```console
$ docker pull gradle@sha256:6c17c31b1bee61cbef64886e439ed587f3a3843df19ee75318862cc8501cbe0d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5425856 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:911ea05dce32b240dc4fef0aa115ef74f6fea53c750e6ce0e8c62aa09b7ba85e`

```dockerfile
```

-	Layers:
	-	`sha256:164de8ee6b5a5c662f61e4718df586e3175c2f572b3f7a67207ffdef1c35380b`  
		Last Modified: Wed, 12 Nov 2025 03:21:40 GMT  
		Size: 5.4 MB (5402084 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:626d595b091df77d852d02e37bb5aca9e8db7ba34b6cd8f3b7d1045767b3cc29`  
		Last Modified: Wed, 12 Nov 2025 03:21:41 GMT  
		Size: 23.8 KB (23772 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:8-jdk17-ubi-minimal` - linux; ppc64le

```console
$ docker pull gradle@sha256:0440e61b0b784fa09a47a3dba2465f8f4949ee6c0b3fc114131237815ed7ac1f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **394.8 MB (394843228 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ad4359e5cb83b309e1fe63013c6e3f9716cc26ccdb95dc3e96636312948ceb4`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["gradle"]`

```dockerfile
# Mon, 03 Nov 2025 14:29:54 GMT
LABEL maintainer="Red Hat, Inc."
# Mon, 03 Nov 2025 14:29:54 GMT
LABEL vendor="Red Hat, Inc."
# Mon, 03 Nov 2025 14:29:54 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Mon, 03 Nov 2025 14:29:54 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.7"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Mon, 03 Nov 2025 14:29:54 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Mon, 03 Nov 2025 14:29:54 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Mon, 03 Nov 2025 14:29:54 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 03 Nov 2025 14:29:54 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 03 Nov 2025 14:29:54 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Mon, 03 Nov 2025 14:29:54 GMT
LABEL io.openshift.expose-services=""
# Mon, 03 Nov 2025 14:29:54 GMT
LABEL io.openshift.tags="minimal rhel9"
# Mon, 03 Nov 2025 14:29:54 GMT
LABEL compose-id="RHEL-9.7.0-updates-20251029.7"
# Mon, 03 Nov 2025 14:29:54 GMT
ENV container oci
# Mon, 03 Nov 2025 14:29:55 GMT
COPY dir:2aa80c9d25b835f7579e139a16e61166355d7a0c67f0d21fa8b083adaa3d9f42 in /      
# Mon, 03 Nov 2025 14:29:55 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Mon, 03 Nov 2025 14:29:55 GMT
CMD ["/bin/bash"]
# Mon, 03 Nov 2025 14:29:55 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /usr/share/buildinfo/content-sets.json      
# Mon, 03 Nov 2025 14:29:55 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /root/buildinfo/content_manifests/content-sets.json      
# Mon, 03 Nov 2025 14:29:55 GMT
COPY file:49b4417acc3f1574e50c559322db7a558c77ea96ef2fd7003d92b0d6c0bc4675 in /usr/share/buildinfo/labels.json      
# Mon, 03 Nov 2025 14:29:55 GMT
COPY file:49b4417acc3f1574e50c559322db7a558c77ea96ef2fd7003d92b0d6c0bc4675 in /root/buildinfo/labels.json      
# Mon, 03 Nov 2025 14:29:55 GMT
LABEL "architecture"="ppc64le" "vcs-type"="git" "vcs-ref"="02d02ad5d9d5ef0add399eb1c8d5f2a4b9261204" "org.opencontainers.image.revision"="02d02ad5d9d5ef0add399eb1c8d5f2a4b9261204" "build-date"="2025-11-03T14:29:44Z" "release"="1762180032"org.opencontainers.image.revision=02d02ad5d9d5ef0add399eb1c8d5f2a4b9261204
# Wed, 12 Nov 2025 00:27:00 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 12 Nov 2025 00:27:00 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 12 Nov 2025 00:27:00 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 12 Nov 2025 00:27:00 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en     ;     microdnf clean all # buildkit
# Wed, 12 Nov 2025 00:27:00 GMT
ENV JAVA_VERSION=jdk-17.0.17+10
# Wed, 12 Nov 2025 00:34:31 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='dc29ca6d35beb4419b4b00419b8a3dfbf5ae551e1ae2b046b516d9a579d04533';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jdk_aarch64_linux_hotspot_17.0.17_10.tar.gz';          ;;        ppc64le)          ESUM='2a29d1be61940c1bd639018c07f4622e1f145a7ef34e7294fee877e39226d9da';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jdk_ppc64le_linux_hotspot_17.0.17_10.tar.gz';          ;;        s390x)          ESUM='76327b1d00c67f6be91717754fd85fc85ce496d48876f69accb9c53ed31dc546';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jdk_s390x_linux_hotspot_17.0.17_10.tar.gz';          ;;        x86_64)          ESUM='992f96e7995075ac7636bb1a8de52b0c61d71ed3137fafc979ab96b4ab78dd75';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jdk_x64_linux_hotspot_17.0.17_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Wed, 12 Nov 2025 00:34:34 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 12 Nov 2025 00:34:34 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 12 Nov 2025 00:34:34 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 12 Nov 2025 00:34:34 GMT
CMD ["jshell"]
# Wed, 12 Nov 2025 01:11:22 GMT
CMD ["gradle"]
# Wed, 12 Nov 2025 01:11:22 GMT
ENV GRADLE_HOME=/opt/gradle
# Wed, 12 Nov 2025 01:11:22 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 101 gradle     && useradd --system --gid gradle --uid 101 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Wed, 12 Nov 2025 01:11:22 GMT
VOLUME [/home/gradle/.gradle]
# Wed, 12 Nov 2025 01:11:22 GMT
WORKDIR /home/gradle
# Wed, 12 Nov 2025 01:13:12 GMT
RUN set -o errexit -o nounset     && microdnf install -y         make                 findutils                 unzip         which                 git         git-lfs         subversion     && microdnf clean all         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which svn # buildkit
# Wed, 12 Nov 2025 01:13:12 GMT
ENV GRADLE_VERSION=8.14.3
# Wed, 12 Nov 2025 01:13:12 GMT
ARG GRADLE_DOWNLOAD_SHA256=bd71102213493060956ec229d946beee57158dbd89d0e62b91bca0fa2c5f3531
# Wed, 12 Nov 2025 01:13:19 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=bd71102213493060956ec229d946beee57158dbd89d0e62b91bca0fa2c5f3531
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Wed, 12 Nov 2025 01:13:19 GMT
USER gradle
# Wed, 12 Nov 2025 01:13:20 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=bd71102213493060956ec229d946beee57158dbd89d0e62b91bca0fa2c5f3531
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Wed, 12 Nov 2025 01:13:20 GMT
USER root
```

-	Layers:
	-	`sha256:04de4da8229cfd129cfea893dac88ba696a562db55dbc18bd0f1170c64597ec0`  
		Last Modified: Tue, 11 Nov 2025 18:11:00 GMT  
		Size: 44.4 MB (44446682 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10811e923266c33db9d8e2226dde2a6e4344e022c251901b43e9588926da8eac`  
		Last Modified: Wed, 12 Nov 2025 00:27:44 GMT  
		Size: 30.1 MB (30115412 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94a5d373efee9edbf90a8876ad14ac0be8ac6c4957fa89e8f48ef2cc332cebc3`  
		Last Modified: Wed, 12 Nov 2025 06:01:09 GMT  
		Size: 144.5 MB (144547847 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c25e8e94617012dd0e05109d365a4cb995ec2378496623e142a6b0aa0de22337`  
		Last Modified: Wed, 12 Nov 2025 00:35:38 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5184e7f11579e8c7e0583fd6dc96f205b7eeae8a8788c503427e16e16ecae1fb`  
		Last Modified: Wed, 12 Nov 2025 00:35:39 GMT  
		Size: 2.3 KB (2290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:782301c7881539f911cd6ad8824557df18a951512835e2a01fb0cacd82da7d19`  
		Last Modified: Wed, 12 Nov 2025 01:14:08 GMT  
		Size: 1.7 KB (1712 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f6679f9a92b041adf48e11a9763ce954b770294a448c7203de315d720519730`  
		Last Modified: Wed, 12 Nov 2025 01:14:23 GMT  
		Size: 38.3 MB (38298981 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2b8fd9ac4a421a8de18d88638363a161a26bbca2756ab80cd0ea3cf58f58e67`  
		Last Modified: Wed, 12 Nov 2025 13:51:03 GMT  
		Size: 137.4 MB (137395136 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bafd135bf10b68b27af1042d429866a7c5c785e2fd1b17081ff5b87d1b662f0c`  
		Last Modified: Wed, 12 Nov 2025 01:14:08 GMT  
		Size: 35.0 KB (35007 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:8-jdk17-ubi-minimal` - unknown; unknown

```console
$ docker pull gradle@sha256:b6626876dcfd64aea34df4e89842a6f2677c9bcc63521c0a2801090adb2dbb25
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5423698 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c1a0c3f9ee9d930387db03e68c751cc6b104c67ddc19613cdfe99bc061d69def`

```dockerfile
```

-	Layers:
	-	`sha256:eddca250f4ae821e6d1c93c62f332ea7eb1bd46f0ed797685f930b8a9d9a7521`  
		Last Modified: Wed, 12 Nov 2025 03:21:46 GMT  
		Size: 5.4 MB (5400001 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:de5c791dc3fa039dff568e296c7e50d59f8fb38b183a798242ccf5bfe3ad1f58`  
		Last Modified: Wed, 12 Nov 2025 03:21:46 GMT  
		Size: 23.7 KB (23697 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:8-jdk17-ubi-minimal` - linux; s390x

```console
$ docker pull gradle@sha256:df6de07ed1798b6a93a6fa26ae20b3cf3e54c9f5889bc929cbd6e6602d2959f2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **374.7 MB (374749684 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c3d0e10099616d973a40b7d483e68aed29210c670080b77ac2dec07ea31fabda`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["gradle"]`

```dockerfile
# Mon, 03 Nov 2025 14:33:38 GMT
LABEL maintainer="Red Hat, Inc."
# Mon, 03 Nov 2025 14:33:38 GMT
LABEL vendor="Red Hat, Inc."
# Mon, 03 Nov 2025 14:33:38 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Mon, 03 Nov 2025 14:33:38 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.7"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Mon, 03 Nov 2025 14:33:38 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Mon, 03 Nov 2025 14:33:38 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Mon, 03 Nov 2025 14:33:38 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 03 Nov 2025 14:33:38 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 03 Nov 2025 14:33:38 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Mon, 03 Nov 2025 14:33:38 GMT
LABEL io.openshift.expose-services=""
# Mon, 03 Nov 2025 14:33:38 GMT
LABEL io.openshift.tags="minimal rhel9"
# Mon, 03 Nov 2025 14:33:38 GMT
LABEL compose-id="RHEL-9.7.0-updates-20251029.7"
# Mon, 03 Nov 2025 14:33:38 GMT
ENV container oci
# Mon, 03 Nov 2025 14:33:39 GMT
COPY dir:4313191826dc185994c19ee88d8ddab5ddb686f1921897eccce6c2d562c2a5c1 in /      
# Mon, 03 Nov 2025 14:33:39 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Mon, 03 Nov 2025 14:33:39 GMT
CMD ["/bin/bash"]
# Mon, 03 Nov 2025 14:33:39 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /usr/share/buildinfo/content-sets.json      
# Mon, 03 Nov 2025 14:33:39 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /root/buildinfo/content_manifests/content-sets.json      
# Mon, 03 Nov 2025 14:33:39 GMT
COPY file:c90c246b59f4221d0cd18be4f14643c9bdaf01fb70eeff22753968d4aa0e9154 in /usr/share/buildinfo/labels.json      
# Mon, 03 Nov 2025 14:33:39 GMT
COPY file:c90c246b59f4221d0cd18be4f14643c9bdaf01fb70eeff22753968d4aa0e9154 in /root/buildinfo/labels.json      
# Mon, 03 Nov 2025 14:33:39 GMT
LABEL "architecture"="s390x" "vcs-type"="git" "vcs-ref"="02d02ad5d9d5ef0add399eb1c8d5f2a4b9261204" "org.opencontainers.image.revision"="02d02ad5d9d5ef0add399eb1c8d5f2a4b9261204" "build-date"="2025-11-03T14:33:20Z" "release"="1762180032"org.opencontainers.image.revision=02d02ad5d9d5ef0add399eb1c8d5f2a4b9261204
# Wed, 12 Nov 2025 00:27:45 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 12 Nov 2025 00:27:45 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 12 Nov 2025 00:27:45 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 12 Nov 2025 00:27:45 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en     ;     microdnf clean all # buildkit
# Wed, 12 Nov 2025 00:27:45 GMT
ENV JAVA_VERSION=jdk-17.0.17+10
# Wed, 12 Nov 2025 00:33:37 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='dc29ca6d35beb4419b4b00419b8a3dfbf5ae551e1ae2b046b516d9a579d04533';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jdk_aarch64_linux_hotspot_17.0.17_10.tar.gz';          ;;        ppc64le)          ESUM='2a29d1be61940c1bd639018c07f4622e1f145a7ef34e7294fee877e39226d9da';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jdk_ppc64le_linux_hotspot_17.0.17_10.tar.gz';          ;;        s390x)          ESUM='76327b1d00c67f6be91717754fd85fc85ce496d48876f69accb9c53ed31dc546';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jdk_s390x_linux_hotspot_17.0.17_10.tar.gz';          ;;        x86_64)          ESUM='992f96e7995075ac7636bb1a8de52b0c61d71ed3137fafc979ab96b4ab78dd75';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jdk_x64_linux_hotspot_17.0.17_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Wed, 12 Nov 2025 00:33:40 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 12 Nov 2025 00:33:41 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 12 Nov 2025 00:33:41 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 12 Nov 2025 00:33:41 GMT
CMD ["jshell"]
# Wed, 12 Nov 2025 01:12:11 GMT
CMD ["gradle"]
# Wed, 12 Nov 2025 01:12:11 GMT
ENV GRADLE_HOME=/opt/gradle
# Wed, 12 Nov 2025 01:12:11 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 101 gradle     && useradd --system --gid gradle --uid 101 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Wed, 12 Nov 2025 01:12:11 GMT
VOLUME [/home/gradle/.gradle]
# Wed, 12 Nov 2025 01:12:11 GMT
WORKDIR /home/gradle
# Wed, 12 Nov 2025 01:13:49 GMT
RUN set -o errexit -o nounset     && microdnf install -y         make                 findutils                 unzip         which                 git         git-lfs         subversion     && microdnf clean all         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which svn # buildkit
# Wed, 12 Nov 2025 01:13:49 GMT
ENV GRADLE_VERSION=8.14.3
# Wed, 12 Nov 2025 01:13:49 GMT
ARG GRADLE_DOWNLOAD_SHA256=bd71102213493060956ec229d946beee57158dbd89d0e62b91bca0fa2c5f3531
# Wed, 12 Nov 2025 01:13:58 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=bd71102213493060956ec229d946beee57158dbd89d0e62b91bca0fa2c5f3531
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Wed, 12 Nov 2025 01:13:58 GMT
USER gradle
# Wed, 12 Nov 2025 01:13:58 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=bd71102213493060956ec229d946beee57158dbd89d0e62b91bca0fa2c5f3531
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Wed, 12 Nov 2025 01:13:58 GMT
USER root
```

-	Layers:
	-	`sha256:7b39cb29f2067b725deaac42d8019f933193965ff0a38d09119fd6bf8a78524b`  
		Last Modified: Tue, 11 Nov 2025 18:10:59 GMT  
		Size: 38.1 MB (38115745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c55049a5374567663fdf5afdbe84f630b277e0cb88fccb2904b26f680ea83b82`  
		Last Modified: Wed, 12 Nov 2025 00:29:35 GMT  
		Size: 27.7 MB (27715037 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d2daed877c184f6894a923e05020dd5878f060b4a4b01e41176631833eea8f0`  
		Last Modified: Wed, 12 Nov 2025 13:52:17 GMT  
		Size: 134.9 MB (134862184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b78a2dc5251b436c7f647646fc41435a883930bf3b87526997d2c3f933cea34b`  
		Last Modified: Wed, 12 Nov 2025 00:34:38 GMT  
		Size: 130.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1fa39054a3e52f726cf6fded0720e4cad35117e740dd7b8e19902e2190c2093`  
		Last Modified: Wed, 12 Nov 2025 00:34:38 GMT  
		Size: 2.3 KB (2290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c1447da9b9787610744290cedde95c64a6619fa9d35db13c321d9135764c23d`  
		Last Modified: Wed, 12 Nov 2025 01:14:36 GMT  
		Size: 1.7 KB (1706 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:707fb2f6917833164c0fa1b769ba4881a431bcec2690d800a221349e7958a658`  
		Last Modified: Wed, 12 Nov 2025 01:14:38 GMT  
		Size: 36.6 MB (36622347 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a21ccc3dd6f8246c118c57b34f34a6c660f194037db315fb5aa9aebf5b264f74`  
		Last Modified: Wed, 12 Nov 2025 13:51:06 GMT  
		Size: 137.4 MB (137395205 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eed5ed8fa3e9df6fddd208dbc0c9bf4185f4a0f7b2ff373a38333ac887d3c8d0`  
		Last Modified: Wed, 12 Nov 2025 01:14:37 GMT  
		Size: 35.0 KB (35008 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:8-jdk17-ubi-minimal` - unknown; unknown

```console
$ docker pull gradle@sha256:5ee0d6ca3eb0692897481a2a62968454f49ff28b91f113913323044c2ec22b92
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5412917 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5fc9efcde8aa3e174a85f55e646119faae78aff52f3897c12777d7f04c9aaf4d`

```dockerfile
```

-	Layers:
	-	`sha256:8417bd0e5c39d4ea1b8b4693ab470b75a95fec8de1c3a3571f00f08d68cd404b`  
		Last Modified: Wed, 12 Nov 2025 03:21:51 GMT  
		Size: 5.4 MB (5389283 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2bc9ecf8a3a1e91c27fa1130fb24638b9d20f723b0465943c9237b6aa200ade2`  
		Last Modified: Wed, 12 Nov 2025 03:21:52 GMT  
		Size: 23.6 KB (23634 bytes)  
		MIME: application/vnd.in-toto+json
