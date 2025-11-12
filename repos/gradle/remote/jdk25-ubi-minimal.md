## `gradle:jdk25-ubi-minimal`

```console
$ docker pull gradle@sha256:979dd1e2a674075a92fbe84b49c052eb72b535e2a962aed127dc26afd9dc43df
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

### `gradle:jdk25-ubi-minimal` - linux; amd64

```console
$ docker pull gradle@sha256:89dbb4a5494c50cb4a93370bc272b7b4adf7fb46d8895d2127edfc544f56f7a1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **349.5 MB (349546259 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:01d3456eb1c101bbeca60912e6f6b67941f8f28bab67c904ad3a9fe59d3a3417`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["gradle"]`

```dockerfile
# Tue, 11 Nov 2025 09:06:02 GMT
LABEL maintainer="Red Hat, Inc."
# Tue, 11 Nov 2025 09:06:02 GMT
LABEL vendor="Red Hat, Inc."
# Tue, 11 Nov 2025 09:06:02 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Tue, 11 Nov 2025 09:06:02 GMT
LABEL com.redhat.component="ubi10-minimal-container"       name="ubi10/ubi-minimal"       version="10.0"       cpe="cpe:/o:redhat:enterprise_linux:10.0"       distribution-scope="public"
# Tue, 11 Nov 2025 09:06:02 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Tue, 11 Nov 2025 09:06:02 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 10."
# Tue, 11 Nov 2025 09:06:02 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Tue, 11 Nov 2025 09:06:02 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Tue, 11 Nov 2025 09:06:02 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 10 Minimal"
# Tue, 11 Nov 2025 09:06:02 GMT
LABEL io.openshift.expose-services=""
# Tue, 11 Nov 2025 09:06:02 GMT
LABEL io.openshift.tags="minimal rhel10"
# Tue, 11 Nov 2025 09:06:02 GMT
ENV container oci
# Tue, 11 Nov 2025 09:06:03 GMT
COPY dir:12e55fa9ec97d580ad96af4c6b8bc6d7173cab511e970c1110242c0e2fdfd563 in /      
# Tue, 11 Nov 2025 09:06:03 GMT
COPY file:5de33b5fc08b00635bccf9134a18978dba13e2250aa51838f9969515a3957847 in /etc/yum.repos.d/.      
# Tue, 11 Nov 2025 09:06:04 GMT
CMD ["/bin/bash"]
# Tue, 11 Nov 2025 09:06:04 GMT
COPY file:595171150af68abc798ea385f7988d74b566aa8e84babff137f00b08b2164683 in /usr/share/buildinfo/content-sets.json      
# Tue, 11 Nov 2025 09:06:04 GMT
COPY file:595171150af68abc798ea385f7988d74b566aa8e84babff137f00b08b2164683 in /root/buildinfo/content_manifests/content-sets.json      
# Tue, 11 Nov 2025 09:06:04 GMT
COPY file:5242942be8b194fbd84cd7044c6fa40353e4b9386fa7dee8863482e2eb6a0f3e in /usr/share/buildinfo/labels.json      
# Tue, 11 Nov 2025 09:06:05 GMT
COPY file:5242942be8b194fbd84cd7044c6fa40353e4b9386fa7dee8863482e2eb6a0f3e in /root/buildinfo/labels.json      
# Tue, 11 Nov 2025 09:06:05 GMT
LABEL "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="0a583d401ee29f56bb3786d762c71b4349cd93d9" "org.opencontainers.image.revision"="0a583d401ee29f56bb3786d762c71b4349cd93d9" "build-date"="2025-11-11T09:05:41Z" "release"="1762851739"org.opencontainers.image.revision=0a583d401ee29f56bb3786d762c71b4349cd93d9
# Wed, 12 Nov 2025 00:27:11 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 12 Nov 2025 00:27:11 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 12 Nov 2025 00:27:11 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 12 Nov 2025 00:27:11 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en         gnupg2     ;     microdnf clean all # buildkit
# Wed, 12 Nov 2025 00:27:11 GMT
ENV JAVA_VERSION=jdk-25.0.1+8
# Wed, 12 Nov 2025 00:28:45 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='5c83b7d2121ed482fd06831a1eba1633dbab818aba6addddf48e075b97e6e9b8';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.1%2B8/OpenJDK25U-jdk_aarch64_linux_hotspot_25.0.1_8.tar.gz';          ;;        ppc64le)          ESUM='54fdfbfa2c463863bd0c2c9c19901320d25ca533f31daa0bd866c4104af7ce5b';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.1%2B8/OpenJDK25U-jdk_ppc64le_linux_hotspot_25.0.1_8.tar.gz';          ;;        s390x)          ESUM='1b627ec601998e5450fd1af91ae26a43b4d646403a8938d7efe4dfb2848fd896';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.1%2B8/OpenJDK25U-jdk_s390x_linux_hotspot_25.0.1_8.tar.gz';          ;;        x86_64)          ESUM='8daf77d1aacffe38c9889689bc224a13557de77559d9a5bb91991e6a298baa0d';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.1%2B8/OpenJDK25U-jdk_x64_linux_hotspot_25.0.1_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Wed, 12 Nov 2025 00:28:46 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 12 Nov 2025 00:28:46 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 12 Nov 2025 00:28:46 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 12 Nov 2025 00:28:46 GMT
CMD ["jshell"]
# Wed, 12 Nov 2025 01:10:16 GMT
CMD ["gradle"]
# Wed, 12 Nov 2025 01:10:16 GMT
ENV GRADLE_HOME=/opt/gradle
# Wed, 12 Nov 2025 01:10:16 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 101 gradle     && useradd --system --gid gradle --uid 101 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Wed, 12 Nov 2025 01:10:16 GMT
VOLUME [/home/gradle/.gradle]
# Wed, 12 Nov 2025 01:10:16 GMT
WORKDIR /home/gradle
# Wed, 12 Nov 2025 01:10:29 GMT
RUN set -o errexit -o nounset     && microdnf install -y         make         curl         wget         tar                 findutils                 unzip         which                 git         git-lfs         subversion     && microdnf clean all         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which svn # buildkit
# Wed, 12 Nov 2025 01:10:29 GMT
ENV GRADLE_VERSION=9.2.0
# Wed, 12 Nov 2025 01:10:29 GMT
ARG GRADLE_DOWNLOAD_SHA256=df67a32e86e3276d011735facb1535f64d0d88df84fa87521e90becc2d735444
# Wed, 12 Nov 2025 01:10:32 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=df67a32e86e3276d011735facb1535f64d0d88df84fa87521e90becc2d735444
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Wed, 12 Nov 2025 01:10:32 GMT
USER gradle
# Wed, 12 Nov 2025 01:10:32 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=df67a32e86e3276d011735facb1535f64d0d88df84fa87521e90becc2d735444
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Wed, 12 Nov 2025 01:10:32 GMT
USER root
```

-	Layers:
	-	`sha256:97d2336739ce8e6158d60016e45d04595e4f80b1d11dd60990e6748ac4fea4f0`  
		Last Modified: Tue, 11 Nov 2025 12:10:43 GMT  
		Size: 33.8 MB (33814455 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f65a2520aeb6c13cc4e822e3d8132acb3e0da55d95b9436e330bfe038b9b792`  
		Last Modified: Wed, 12 Nov 2025 00:27:47 GMT  
		Size: 32.3 MB (32336994 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:484b873d81d8a59b0ee4d61b2ce17e13118493dda2306da6f43b81f1510c02da`  
		Last Modified: Wed, 12 Nov 2025 00:29:16 GMT  
		Size: 92.0 MB (92046702 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b790b2cbc36b920731d01ff0e52e951cc20e47cbf68453561de10b90de55ce8e`  
		Last Modified: Wed, 12 Nov 2025 00:29:11 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52b206a586b597decc8685a65ef855e2778fe5861e4cec53f987c96a0a2de525`  
		Last Modified: Wed, 12 Nov 2025 00:29:11 GMT  
		Size: 2.3 KB (2290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:faf75c0450ba523b49253c80f87f9de87299772e1edeab9210c9aae39c7f94fe`  
		Last Modified: Wed, 12 Nov 2025 01:11:08 GMT  
		Size: 1.4 KB (1436 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41b84e60c5afe375879e061c1783e635af5f3c6f4b961f192592a21552e415ad`  
		Last Modified: Wed, 12 Nov 2025 01:11:15 GMT  
		Size: 55.8 MB (55767592 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:186c91f9d2b296ba81ed21e995c36a1318bd1d1b4fc524f1bc04cb41f3090537`  
		Last Modified: Wed, 12 Nov 2025 01:11:47 GMT  
		Size: 135.5 MB (135521733 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3016c0bb802644b75619523ab64e0e87e01aeab218271cdfec032eb62f1aa7fe`  
		Last Modified: Wed, 12 Nov 2025 01:11:08 GMT  
		Size: 54.9 KB (54897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:jdk25-ubi-minimal` - unknown; unknown

```console
$ docker pull gradle@sha256:fb636fa7a824e2116d2e808f2c7c3c9399474151b5a2d1c81907da4c2b8455c7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 MB (7035538 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ab8c0999234daec9a54200fd32ca727ae672da7e5b2578cf029c4b520c463e7`

```dockerfile
```

-	Layers:
	-	`sha256:98f9252615802bbf7be5b55e3199cd29e40a26fd1116bd457a878c751cb38a12`  
		Last Modified: Wed, 12 Nov 2025 03:24:42 GMT  
		Size: 7.0 MB (7010518 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d417f932057c68f3e79b2f7c2ef09cdd954507c0d4f50e1cb3df8f2988d9dacf`  
		Last Modified: Wed, 12 Nov 2025 03:24:43 GMT  
		Size: 25.0 KB (25020 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:jdk25-ubi-minimal` - linux; arm64 variant v8

```console
$ docker pull gradle@sha256:f6b0754ba8f4e61e18ef32f23be82cf28b7eae6e914744c617be18f0444bec6b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **356.5 MB (356544251 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:911da2c09f5ef2d2294e009e59e9fc1611980778a84d849d23fd7faa599e7d14`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["gradle"]`

```dockerfile
# Mon, 10 Nov 2025 09:03:37 GMT
LABEL maintainer="Red Hat, Inc."
# Mon, 10 Nov 2025 09:03:37 GMT
LABEL vendor="Red Hat, Inc."
# Mon, 10 Nov 2025 09:03:37 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Mon, 10 Nov 2025 09:03:37 GMT
LABEL com.redhat.component="ubi10-minimal-container"       name="ubi10/ubi-minimal"       version="10.0"       cpe="cpe:/o:redhat:enterprise_linux:10.0"       distribution-scope="public"
# Mon, 10 Nov 2025 09:03:37 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Mon, 10 Nov 2025 09:03:37 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 10."
# Mon, 10 Nov 2025 09:03:37 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 10 Nov 2025 09:03:37 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 10 Nov 2025 09:03:37 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 10 Minimal"
# Mon, 10 Nov 2025 09:03:37 GMT
LABEL io.openshift.expose-services=""
# Mon, 10 Nov 2025 09:03:37 GMT
LABEL io.openshift.tags="minimal rhel10"
# Mon, 10 Nov 2025 09:03:37 GMT
ENV container oci
# Mon, 10 Nov 2025 09:03:38 GMT
COPY dir:5f27c3cb719e482fe521704b0fcfe8823184f7bac7981ef4facb5aa58eacca9f in /      
# Mon, 10 Nov 2025 09:03:38 GMT
COPY file:5de33b5fc08b00635bccf9134a18978dba13e2250aa51838f9969515a3957847 in /etc/yum.repos.d/.      
# Mon, 10 Nov 2025 09:03:38 GMT
CMD ["/bin/bash"]
# Mon, 10 Nov 2025 09:03:38 GMT
COPY file:595171150af68abc798ea385f7988d74b566aa8e84babff137f00b08b2164683 in /usr/share/buildinfo/content-sets.json      
# Mon, 10 Nov 2025 09:03:38 GMT
COPY file:595171150af68abc798ea385f7988d74b566aa8e84babff137f00b08b2164683 in /root/buildinfo/content_manifests/content-sets.json      
# Mon, 10 Nov 2025 09:03:38 GMT
COPY file:b708d1caa910d276ff58faaae8986ef542efb0b7b3e35c86e7086c7765f4ff1a in /usr/share/buildinfo/labels.json      
# Mon, 10 Nov 2025 09:03:38 GMT
COPY file:b708d1caa910d276ff58faaae8986ef542efb0b7b3e35c86e7086c7765f4ff1a in /root/buildinfo/labels.json      
# Mon, 10 Nov 2025 09:03:39 GMT
LABEL "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="18068ad623ccc46f729e7cefa6bb8063513ecab3" "org.opencontainers.image.revision"="18068ad623ccc46f729e7cefa6bb8063513ecab3" "build-date"="2025-11-10T09:03:16Z" "release"="1762765041"org.opencontainers.image.revision=18068ad623ccc46f729e7cefa6bb8063513ecab3
# Mon, 10 Nov 2025 20:14:34 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 10 Nov 2025 20:14:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 10 Nov 2025 20:14:34 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 10 Nov 2025 20:14:34 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en         gnupg2     ;     microdnf clean all # buildkit
# Mon, 10 Nov 2025 20:14:34 GMT
ENV JAVA_VERSION=jdk-25.0.1+8
# Mon, 10 Nov 2025 20:15:10 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='5c83b7d2121ed482fd06831a1eba1633dbab818aba6addddf48e075b97e6e9b8';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.1%2B8/OpenJDK25U-jdk_aarch64_linux_hotspot_25.0.1_8.tar.gz';          ;;        ppc64le)          ESUM='54fdfbfa2c463863bd0c2c9c19901320d25ca533f31daa0bd866c4104af7ce5b';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.1%2B8/OpenJDK25U-jdk_ppc64le_linux_hotspot_25.0.1_8.tar.gz';          ;;        s390x)          ESUM='1b627ec601998e5450fd1af91ae26a43b4d646403a8938d7efe4dfb2848fd896';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.1%2B8/OpenJDK25U-jdk_s390x_linux_hotspot_25.0.1_8.tar.gz';          ;;        x86_64)          ESUM='8daf77d1aacffe38c9889689bc224a13557de77559d9a5bb91991e6a298baa0d';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.1%2B8/OpenJDK25U-jdk_x64_linux_hotspot_25.0.1_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Mon, 10 Nov 2025 20:15:11 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Mon, 10 Nov 2025 20:15:11 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Mon, 10 Nov 2025 20:15:11 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Mon, 10 Nov 2025 20:15:11 GMT
CMD ["jshell"]
# Mon, 10 Nov 2025 21:10:53 GMT
CMD ["gradle"]
# Mon, 10 Nov 2025 21:10:53 GMT
ENV GRADLE_HOME=/opt/gradle
# Mon, 10 Nov 2025 21:10:53 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 101 gradle     && useradd --system --gid gradle --uid 101 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Mon, 10 Nov 2025 21:10:53 GMT
VOLUME [/home/gradle/.gradle]
# Mon, 10 Nov 2025 21:10:53 GMT
WORKDIR /home/gradle
# Mon, 10 Nov 2025 21:11:01 GMT
RUN set -o errexit -o nounset     && microdnf install -y         make         curl         wget         tar                 findutils                 unzip         which                 git         git-lfs         subversion     && microdnf clean all         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which svn # buildkit
# Mon, 10 Nov 2025 21:11:01 GMT
ENV GRADLE_VERSION=9.2.0
# Mon, 10 Nov 2025 21:11:01 GMT
ARG GRADLE_DOWNLOAD_SHA256=df67a32e86e3276d011735facb1535f64d0d88df84fa87521e90becc2d735444
# Mon, 10 Nov 2025 21:11:04 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=df67a32e86e3276d011735facb1535f64d0d88df84fa87521e90becc2d735444
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Mon, 10 Nov 2025 21:11:04 GMT
USER gradle
# Mon, 10 Nov 2025 21:11:04 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=df67a32e86e3276d011735facb1535f64d0d88df84fa87521e90becc2d735444
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Mon, 10 Nov 2025 21:11:04 GMT
USER root
```

-	Layers:
	-	`sha256:bcfce2f653765e7fbc0157676a8995e7c79e4d29c562744818763bd665844191`  
		Last Modified: Mon, 10 Nov 2025 12:11:55 GMT  
		Size: 31.6 MB (31555554 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5793af67cb3aa19951f43fe6e39959896079611172ac01ca8340869d69503c7`  
		Last Modified: Mon, 10 Nov 2025 20:15:14 GMT  
		Size: 59.9 MB (59905300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6cb24325116e322d7c6ad9f803974ff877a9054dbf84d401db02455cce54fbd`  
		Last Modified: Mon, 10 Nov 2025 20:15:43 GMT  
		Size: 91.1 MB (91056295 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e8a7d0f823d971b3d89ad0e1dfb92a338d2b741532cf4e592d1362c487a7841`  
		Last Modified: Mon, 10 Nov 2025 20:15:36 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:605905de5012b0f7f202df4e38ff9f40ee5357745b0ef9b42aef52f6208280c8`  
		Last Modified: Mon, 10 Nov 2025 20:15:37 GMT  
		Size: 2.3 KB (2291 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01a158fd8503b9f6fc3776a4cc7eeb78af5408f654e4bb169ec0a4d5ccddf65e`  
		Last Modified: Mon, 10 Nov 2025 21:11:35 GMT  
		Size: 1.6 KB (1612 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f76f6dfbf63d6c68cfad73c92981e395a8f80f0efe1632d7ef4b4b2a0c651144`  
		Last Modified: Mon, 10 Nov 2025 21:11:45 GMT  
		Size: 38.4 MB (38441851 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:817900e57706e4432cd418017ad21b94cb49134d1d45e8c051829d6d5cdb1ce1`  
		Last Modified: Tue, 11 Nov 2025 13:02:58 GMT  
		Size: 135.5 MB (135521665 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8eeccb8e2b9b810b40178dd9172b8790709ec1ceab954ce55a770aa24c58025`  
		Last Modified: Mon, 10 Nov 2025 21:11:42 GMT  
		Size: 59.5 KB (59523 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:jdk25-ubi-minimal` - unknown; unknown

```console
$ docker pull gradle@sha256:c36272cbe6ff89c6506d8b1286534c91b921ad284673bc9bf1c4ee403679fa04
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.9 MB (8892575 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ff6dd2c9a63ae06a8ae61a8a5c379de0b36bbec73ee069694bc6bd3e0284fb5`

```dockerfile
```

-	Layers:
	-	`sha256:51af9d27443136c533e1ae0c378af391a31072003f7dddb2c6797d60c5bba783`  
		Last Modified: Tue, 11 Nov 2025 00:21:19 GMT  
		Size: 8.9 MB (8867334 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0a66a92bbdc9b23e0f94bc4a0eea8307e353a42e271debb2e95abebd56633fd1`  
		Last Modified: Tue, 11 Nov 2025 00:21:20 GMT  
		Size: 25.2 KB (25241 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:jdk25-ubi-minimal` - linux; ppc64le

```console
$ docker pull gradle@sha256:df7b6a77bdb6cf751336247430d7b995b3120842827c10bb838641f4ef72f714
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **360.6 MB (360648169 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b4a6cfc3439fea8c3cb0fb6570cb8bc70cbdcbd9270d8c7c956ea99f72fcd46`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["gradle"]`

```dockerfile
# Wed, 24 Sep 2025 07:41:36 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 24 Sep 2025 07:41:36 GMT
LABEL vendor="Red Hat, Inc."
# Wed, 24 Sep 2025 07:41:36 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Wed, 24 Sep 2025 07:41:36 GMT
LABEL com.redhat.component="ubi10-minimal-container"       name="ubi10/ubi-minimal"       version="10.0"       cpe="cpe:/o:redhat:enterprise_linux:10.0"       distribution-scope="public"
# Wed, 24 Sep 2025 07:41:36 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 24 Sep 2025 07:41:36 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 10."
# Wed, 24 Sep 2025 07:41:36 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 24 Sep 2025 07:41:36 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 24 Sep 2025 07:41:37 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 10 Minimal"
# Wed, 24 Sep 2025 07:41:37 GMT
LABEL io.openshift.expose-services=""
# Wed, 24 Sep 2025 07:41:37 GMT
LABEL io.openshift.tags="minimal rhel10"
# Wed, 24 Sep 2025 07:41:37 GMT
ENV container oci
# Wed, 24 Sep 2025 07:41:37 GMT
COPY dir:8763112df95fa3ba21bfe4559d1c3d20c94187edd97f0aa385c49c1a78ac67c8 in /      
# Wed, 24 Sep 2025 07:41:37 GMT
COPY file:5de33b5fc08b00635bccf9134a18978dba13e2250aa51838f9969515a3957847 in /etc/yum.repos.d/.      
# Wed, 24 Sep 2025 07:41:37 GMT
CMD ["/bin/bash"]
# Wed, 24 Sep 2025 07:41:37 GMT
COPY file:595171150af68abc798ea385f7988d74b566aa8e84babff137f00b08b2164683 in /usr/share/buildinfo/content-sets.json      
# Wed, 24 Sep 2025 07:41:37 GMT
COPY file:595171150af68abc798ea385f7988d74b566aa8e84babff137f00b08b2164683 in /root/buildinfo/content_manifests/content-sets.json      
# Wed, 24 Sep 2025 07:41:37 GMT
COPY file:9d60118773670fbee148c27ca84d2373a59792c5d57f8118d19be9e19f60f51c in /root/buildinfo/labels.json      
# Wed, 24 Sep 2025 07:41:38 GMT
LABEL "architecture"="ppc64le" "vcs-type"="git" "vcs-ref"="1cf4bca0a0a9b1becc90c8497d13ba99950d480a" "org.opencontainers.image.revision"="1cf4bca0a0a9b1becc90c8497d13ba99950d480a" "build-date"="2025-09-24T07:41:26Z" "release"="1758699349"org.opencontainers.image.revision=1cf4bca0a0a9b1becc90c8497d13ba99950d480a
# Thu, 25 Sep 2025 19:59:06 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 25 Sep 2025 19:59:06 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 25 Sep 2025 19:59:06 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 25 Sep 2025 19:59:06 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en         gnupg2     ;     microdnf clean all # buildkit
# Thu, 25 Sep 2025 19:59:06 GMT
ENV JAVA_VERSION=jdk-25+36
# Thu, 25 Sep 2025 19:59:06 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='95716d04bdfc8b10c94f4448ea8d57a3ba872d98b53c752e4c6b48f1c95bc582';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25%2B36/OpenJDK25U-jdk_aarch64_linux_hotspot_25_36.tar.gz';          ;;        ppc64le)          ESUM='b060bb12b3a192a0599f03ebb9495492f78c48cb61e291e336a8b00e7798ffb0';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25%2B36/OpenJDK25U-jdk_ppc64le_linux_hotspot_25_36.tar.gz';          ;;        s390x)          ESUM='3e476e40f920ccfb1915d200bc7a1fba9d68c4adcc0358c5968d15613690b915';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25%2B36/OpenJDK25U-jdk_s390x_linux_hotspot_25_36.tar.gz';          ;;        x86_64)          ESUM='ee04de95ab9da7287d40bd2173076ecc2a6dd662f007bedfc6eb0380c0ef90e8';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25%2B36/OpenJDK25U-jdk_x64_linux_hotspot_25_36.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Thu, 25 Sep 2025 19:59:06 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 25 Sep 2025 19:59:06 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 25 Sep 2025 19:59:06 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 25 Sep 2025 19:59:06 GMT
CMD ["jshell"]
# Tue, 30 Sep 2025 09:31:25 GMT
CMD ["gradle"]
# Tue, 30 Sep 2025 09:31:25 GMT
ENV GRADLE_HOME=/opt/gradle
# Tue, 30 Sep 2025 09:31:25 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 101 gradle     && useradd --system --gid gradle --uid 101 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Tue, 30 Sep 2025 09:31:25 GMT
VOLUME [/home/gradle/.gradle]
# Tue, 30 Sep 2025 09:31:25 GMT
WORKDIR /home/gradle
# Tue, 30 Sep 2025 09:31:25 GMT
RUN set -o errexit -o nounset     && microdnf install -y         make         curl         wget         tar                 findutils                 unzip         which                 git         git-lfs         subversion     && microdnf clean all         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which svn # buildkit
# Tue, 30 Sep 2025 09:31:25 GMT
ENV GRADLE_VERSION=9.1.0
# Tue, 30 Sep 2025 09:31:25 GMT
ARG GRADLE_DOWNLOAD_SHA256=a17ddd85a26b6a7f5ddb71ff8b05fc5104c0202c6e64782429790c933686c806
# Tue, 30 Sep 2025 09:31:25 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=a17ddd85a26b6a7f5ddb71ff8b05fc5104c0202c6e64782429790c933686c806
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Tue, 30 Sep 2025 09:31:25 GMT
USER gradle
# Tue, 30 Sep 2025 09:31:25 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=a17ddd85a26b6a7f5ddb71ff8b05fc5104c0202c6e64782429790c933686c806
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Tue, 30 Sep 2025 09:31:25 GMT
USER root
```

-	Layers:
	-	`sha256:03509b72270b34907502615cd7096986a2eeeff33db581c7c8a4d6e63773a680`  
		Last Modified: Wed, 24 Sep 2025 12:11:54 GMT  
		Size: 36.8 MB (36778911 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7594fd32628be065d0a211a204c694db88e721d2972b272697f3be160b1b4984`  
		Last Modified: Wed, 24 Sep 2025 21:32:05 GMT  
		Size: 57.1 MB (57088198 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:873d189906773da04504ca1b699f0893cd338fca6821944cb18078e73caab3fc`  
		Last Modified: Thu, 25 Sep 2025 21:11:10 GMT  
		Size: 91.6 MB (91608624 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9bb4e497e69e481a933f35e40151aab55ebec66603c8f528e33ff70746ea0b2c`  
		Last Modified: Thu, 25 Sep 2025 21:11:02 GMT  
		Size: 130.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b279e8454cdf4b892bd2a109b64615c6fe30d47e3b5f0e374b9c68c91dbab17`  
		Last Modified: Thu, 25 Sep 2025 21:11:02 GMT  
		Size: 2.3 KB (2290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9e7d31581661d7869662d93478938943f3670fc314de27eec33e955ffdb1bb1`  
		Last Modified: Tue, 30 Sep 2025 19:55:30 GMT  
		Size: 1.6 KB (1616 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe586144c5eb73e9fa8f48d4dcba25cad818d220700a3743c5aade7e3fa2baee`  
		Last Modified: Tue, 30 Sep 2025 19:55:36 GMT  
		Size: 40.6 MB (40618607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8d42b40a212feab67ee1c1b180a68bac275445fb6e934e63015a47cde61de7a`  
		Last Modified: Thu, 02 Oct 2025 15:14:11 GMT  
		Size: 134.5 MB (134514750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6723789153752ecbda0aedf89c66e2e70649384925a58a8f3dd97d2b8353eca`  
		Last Modified: Tue, 30 Sep 2025 19:55:31 GMT  
		Size: 35.0 KB (35011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:jdk25-ubi-minimal` - unknown; unknown

```console
$ docker pull gradle@sha256:d129b1573e3e395ce774981ebd6b3252aeb2a140694383d221a4d1c1366a6568
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.9 MB (8879800 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a51567f0382bdc7658b2e0dfc428c88e1118de622ddb4f9f0c5395ec2311f2d`

```dockerfile
```

-	Layers:
	-	`sha256:dde29fac0426577b537eb9afd997169bd3e8f2372d534d4d4db2aa2fb72850e6`  
		Last Modified: Wed, 01 Oct 2025 20:25:15 GMT  
		Size: 8.9 MB (8854663 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:27793fd35029fb42eff27fb25f77b844e55a73e90816620d83b5a7520416dc4d`  
		Last Modified: Wed, 01 Oct 2025 20:25:16 GMT  
		Size: 25.1 KB (25137 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:jdk25-ubi-minimal` - linux; s390x

```console
$ docker pull gradle@sha256:cad864d4418f28e0fbc9deda0b18efa6c6891c4bfc9d075555694718ffe7a4c5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **352.8 MB (352806175 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9fc001a75c7cc37c89f64c1c96e0a4edd52e458a2bebc3b11e90d9428469e8a4`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["gradle"]`

```dockerfile
# Wed, 24 Sep 2025 07:53:07 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 24 Sep 2025 07:53:07 GMT
LABEL vendor="Red Hat, Inc."
# Wed, 24 Sep 2025 07:53:07 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Wed, 24 Sep 2025 07:53:07 GMT
LABEL com.redhat.component="ubi10-minimal-container"       name="ubi10/ubi-minimal"       version="10.0"       cpe="cpe:/o:redhat:enterprise_linux:10.0"       distribution-scope="public"
# Wed, 24 Sep 2025 07:53:07 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 24 Sep 2025 07:53:07 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 10."
# Wed, 24 Sep 2025 07:53:07 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 24 Sep 2025 07:53:07 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 24 Sep 2025 07:53:07 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 10 Minimal"
# Wed, 24 Sep 2025 07:53:07 GMT
LABEL io.openshift.expose-services=""
# Wed, 24 Sep 2025 07:53:07 GMT
LABEL io.openshift.tags="minimal rhel10"
# Wed, 24 Sep 2025 07:53:07 GMT
ENV container oci
# Wed, 24 Sep 2025 07:53:07 GMT
COPY dir:2c1fa1bd656078246346d6555e4507761c570da8e180dc87eb26a8c737f74cd5 in /      
# Wed, 24 Sep 2025 07:53:07 GMT
COPY file:5de33b5fc08b00635bccf9134a18978dba13e2250aa51838f9969515a3957847 in /etc/yum.repos.d/.      
# Wed, 24 Sep 2025 07:53:07 GMT
CMD ["/bin/bash"]
# Wed, 24 Sep 2025 07:53:08 GMT
COPY file:595171150af68abc798ea385f7988d74b566aa8e84babff137f00b08b2164683 in /usr/share/buildinfo/content-sets.json      
# Wed, 24 Sep 2025 07:53:08 GMT
COPY file:595171150af68abc798ea385f7988d74b566aa8e84babff137f00b08b2164683 in /root/buildinfo/content_manifests/content-sets.json      
# Wed, 24 Sep 2025 07:53:08 GMT
COPY file:2603c76e37273f3a1d2d759b3376cb903e3b2c81e82bfad6aa27546d2fc0b0c4 in /root/buildinfo/labels.json      
# Wed, 24 Sep 2025 07:53:08 GMT
LABEL "architecture"="s390x" "vcs-type"="git" "vcs-ref"="1cf4bca0a0a9b1becc90c8497d13ba99950d480a" "org.opencontainers.image.revision"="1cf4bca0a0a9b1becc90c8497d13ba99950d480a" "build-date"="2025-09-24T07:50:56Z" "release"="1758699349"org.opencontainers.image.revision=1cf4bca0a0a9b1becc90c8497d13ba99950d480a
# Thu, 25 Sep 2025 19:59:06 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 25 Sep 2025 19:59:06 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 25 Sep 2025 19:59:06 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 25 Sep 2025 19:59:06 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en         gnupg2     ;     microdnf clean all # buildkit
# Thu, 25 Sep 2025 19:59:06 GMT
ENV JAVA_VERSION=jdk-25+36
# Thu, 25 Sep 2025 19:59:06 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='95716d04bdfc8b10c94f4448ea8d57a3ba872d98b53c752e4c6b48f1c95bc582';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25%2B36/OpenJDK25U-jdk_aarch64_linux_hotspot_25_36.tar.gz';          ;;        ppc64le)          ESUM='b060bb12b3a192a0599f03ebb9495492f78c48cb61e291e336a8b00e7798ffb0';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25%2B36/OpenJDK25U-jdk_ppc64le_linux_hotspot_25_36.tar.gz';          ;;        s390x)          ESUM='3e476e40f920ccfb1915d200bc7a1fba9d68c4adcc0358c5968d15613690b915';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25%2B36/OpenJDK25U-jdk_s390x_linux_hotspot_25_36.tar.gz';          ;;        x86_64)          ESUM='ee04de95ab9da7287d40bd2173076ecc2a6dd662f007bedfc6eb0380c0ef90e8';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25%2B36/OpenJDK25U-jdk_x64_linux_hotspot_25_36.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Thu, 25 Sep 2025 19:59:06 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 25 Sep 2025 19:59:06 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 25 Sep 2025 19:59:06 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 25 Sep 2025 19:59:06 GMT
CMD ["jshell"]
# Tue, 30 Sep 2025 09:31:25 GMT
CMD ["gradle"]
# Tue, 30 Sep 2025 09:31:25 GMT
ENV GRADLE_HOME=/opt/gradle
# Tue, 30 Sep 2025 09:31:25 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 101 gradle     && useradd --system --gid gradle --uid 101 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Tue, 30 Sep 2025 09:31:25 GMT
VOLUME [/home/gradle/.gradle]
# Tue, 30 Sep 2025 09:31:25 GMT
WORKDIR /home/gradle
# Tue, 30 Sep 2025 09:31:25 GMT
RUN set -o errexit -o nounset     && microdnf install -y         make         curl         wget         tar                 findutils                 unzip         which                 git         git-lfs         subversion     && microdnf clean all         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which svn # buildkit
# Tue, 30 Sep 2025 09:31:25 GMT
ENV GRADLE_VERSION=9.1.0
# Tue, 30 Sep 2025 09:31:25 GMT
ARG GRADLE_DOWNLOAD_SHA256=a17ddd85a26b6a7f5ddb71ff8b05fc5104c0202c6e64782429790c933686c806
# Tue, 30 Sep 2025 09:31:25 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=a17ddd85a26b6a7f5ddb71ff8b05fc5104c0202c6e64782429790c933686c806
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Tue, 30 Sep 2025 09:31:25 GMT
USER gradle
# Tue, 30 Sep 2025 09:31:25 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=a17ddd85a26b6a7f5ddb71ff8b05fc5104c0202c6e64782429790c933686c806
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Tue, 30 Sep 2025 09:31:25 GMT
USER root
```

-	Layers:
	-	`sha256:2ef2239186ea9c000a30f781ed39af7418e33d673b592070070773399ccd8411`  
		Last Modified: Wed, 24 Sep 2025 12:11:54 GMT  
		Size: 33.4 MB (33412405 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e96d81b8156c358ceeb24f51d3a912a38aae04fedf9060e1f8c03816d669cdf`  
		Last Modified: Wed, 24 Sep 2025 20:38:11 GMT  
		Size: 55.7 MB (55675136 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94d67a0f289d84d40426a5d667784a56dfdbf64746e610fb6ebc7eb16fd2d4cb`  
		Last Modified: Thu, 25 Sep 2025 21:10:29 GMT  
		Size: 88.2 MB (88209134 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:baafeb1fba5ea3c93d8e5d2dca10ffe492ba450ab9d32738f2a93a7d4583469f`  
		Last Modified: Thu, 25 Sep 2025 21:10:25 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0237ddcc03a286cda63dd78be7d946e71a6711cdf52d4de42c1ec1c94420e68f`  
		Last Modified: Thu, 25 Sep 2025 21:10:26 GMT  
		Size: 2.3 KB (2291 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0152e2d49a86ce751c5e9ee858017f4a546fa7242f7c9e80770e3ced27c5da4`  
		Last Modified: Tue, 30 Sep 2025 23:58:29 GMT  
		Size: 1.6 KB (1614 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:282a07963dc1d59ba333401c2dec07edbb9ae18bf5c0131ef2443dbfbb36324f`  
		Last Modified: Tue, 30 Sep 2025 23:58:32 GMT  
		Size: 41.0 MB (40955753 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:611d3ac407094136131b618cea1e7f34e09f203ec07ea35eba3a1ccd9a771a5a`  
		Last Modified: Thu, 02 Oct 2025 14:51:37 GMT  
		Size: 134.5 MB (134514680 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81265919eee36212049643413c86668f6023560f50b0c62ec17f522c15fbb794`  
		Last Modified: Tue, 30 Sep 2025 23:58:29 GMT  
		Size: 35.0 KB (35002 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:jdk25-ubi-minimal` - unknown; unknown

```console
$ docker pull gradle@sha256:3644cb48e31068102d36c3183bc98eba202d087714d34a6633a5432fd26a490c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.9 MB (8869797 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1deaf733abaef460064f8e2ee9ab79d8689886faf9c84e12ed01aa6df65a6bab`

```dockerfile
```

-	Layers:
	-	`sha256:ef4925dc6f2297f1d85df8b77d82af9e613ed2a0583da379f9dcc728afa292e8`  
		Last Modified: Wed, 01 Oct 2025 20:25:23 GMT  
		Size: 8.8 MB (8844746 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e4ff81cc0fab7f6c4b8e0d69bd687d4fdc237653820e529554d7c6ff8bdaa303`  
		Last Modified: Wed, 01 Oct 2025 20:25:24 GMT  
		Size: 25.1 KB (25051 bytes)  
		MIME: application/vnd.in-toto+json
