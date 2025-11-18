## `gradle:jdk25-ubi-minimal`

```console
$ docker pull gradle@sha256:a0a32fbec140bb02626019a4c0745a76879e39147b634a41ddac304f939071ff
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
$ docker pull gradle@sha256:943af8bcba8d57f3ea48519bb02239781656f2d9a776b464d7da0c2357287027
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **359.4 MB (359392900 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f7d5b8c7a47d18f2fccbe8facfa33aacd50b0e35820eeed58dc491b96b854364`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["gradle"]`

```dockerfile
# Wed, 12 Nov 2025 13:01:22 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 12 Nov 2025 13:01:22 GMT
LABEL vendor="Red Hat, Inc."
# Wed, 12 Nov 2025 13:01:22 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Wed, 12 Nov 2025 13:01:22 GMT
LABEL com.redhat.component="ubi10-minimal-container"       name="ubi10/ubi-minimal"       version="10.1"       cpe="cpe:/o:redhat:enterprise_linux:10.1"       distribution-scope="public"
# Wed, 12 Nov 2025 13:01:22 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 12 Nov 2025 13:01:22 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 10."
# Wed, 12 Nov 2025 13:01:22 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 12 Nov 2025 13:01:22 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 12 Nov 2025 13:01:22 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 10 Minimal"
# Wed, 12 Nov 2025 13:01:22 GMT
LABEL io.openshift.expose-services=""
# Wed, 12 Nov 2025 13:01:22 GMT
LABEL io.openshift.tags="minimal rhel10"
# Wed, 12 Nov 2025 13:01:22 GMT
ENV container oci
# Wed, 12 Nov 2025 13:01:23 GMT
COPY dir:f2440371cac1ecd5821b1d2fdba3a255aaff3a1a77b5c3da42649fb9aa41eacf in /      
# Wed, 12 Nov 2025 13:01:23 GMT
COPY file:5de33b5fc08b00635bccf9134a18978dba13e2250aa51838f9969515a3957847 in /etc/yum.repos.d/.      
# Wed, 12 Nov 2025 13:01:23 GMT
CMD ["/bin/bash"]
# Wed, 12 Nov 2025 13:01:23 GMT
COPY file:595171150af68abc798ea385f7988d74b566aa8e84babff137f00b08b2164683 in /usr/share/buildinfo/content-sets.json      
# Wed, 12 Nov 2025 13:01:23 GMT
COPY file:595171150af68abc798ea385f7988d74b566aa8e84babff137f00b08b2164683 in /root/buildinfo/content_manifests/content-sets.json      
# Wed, 12 Nov 2025 13:01:23 GMT
COPY file:38c762d98ec7c6a2f80e50bd0d7f55f749ddc727f82c6ec0ecf03ddb34a3b284 in /usr/share/buildinfo/labels.json      
# Wed, 12 Nov 2025 13:01:23 GMT
COPY file:38c762d98ec7c6a2f80e50bd0d7f55f749ddc727f82c6ec0ecf03ddb34a3b284 in /root/buildinfo/labels.json      
# Wed, 12 Nov 2025 13:01:23 GMT
LABEL "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="c2904cc9bad715599f86f4c20562b90929d43731" "org.opencontainers.image.revision"="c2904cc9bad715599f86f4c20562b90929d43731" "build-date"="2025-11-12T13:01:03Z" "release"="1762952303"org.opencontainers.image.revision=c2904cc9bad715599f86f4c20562b90929d43731
# Fri, 14 Nov 2025 01:12:48 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 14 Nov 2025 01:12:48 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 14 Nov 2025 01:12:48 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 14 Nov 2025 01:12:48 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en         gnupg2     ;     microdnf clean all # buildkit
# Fri, 14 Nov 2025 01:12:48 GMT
ENV JAVA_VERSION=jdk-25.0.1+8
# Fri, 14 Nov 2025 01:13:25 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='5c83b7d2121ed482fd06831a1eba1633dbab818aba6addddf48e075b97e6e9b8';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.1%2B8/OpenJDK25U-jdk_aarch64_linux_hotspot_25.0.1_8.tar.gz';          ;;        ppc64le)          ESUM='54fdfbfa2c463863bd0c2c9c19901320d25ca533f31daa0bd866c4104af7ce5b';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.1%2B8/OpenJDK25U-jdk_ppc64le_linux_hotspot_25.0.1_8.tar.gz';          ;;        s390x)          ESUM='1b627ec601998e5450fd1af91ae26a43b4d646403a8938d7efe4dfb2848fd896';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.1%2B8/OpenJDK25U-jdk_s390x_linux_hotspot_25.0.1_8.tar.gz';          ;;        x86_64)          ESUM='8daf77d1aacffe38c9889689bc224a13557de77559d9a5bb91991e6a298baa0d';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.1%2B8/OpenJDK25U-jdk_x64_linux_hotspot_25.0.1_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Fri, 14 Nov 2025 01:13:26 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Fri, 14 Nov 2025 01:13:26 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Fri, 14 Nov 2025 01:13:26 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Fri, 14 Nov 2025 01:13:26 GMT
CMD ["jshell"]
# Mon, 17 Nov 2025 19:58:00 GMT
CMD ["gradle"]
# Mon, 17 Nov 2025 19:58:00 GMT
ENV GRADLE_HOME=/opt/gradle
# Mon, 17 Nov 2025 19:58:00 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 101 gradle     && useradd --system --gid gradle --uid 101 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Mon, 17 Nov 2025 19:58:00 GMT
VOLUME [/home/gradle/.gradle]
# Mon, 17 Nov 2025 19:58:00 GMT
WORKDIR /home/gradle
# Mon, 17 Nov 2025 19:58:05 GMT
RUN set -o errexit -o nounset     && microdnf install -y         make         curl         wget         tar                 findutils                 unzip         which                 git         git-lfs         subversion     && microdnf clean all         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which svn # buildkit
# Mon, 17 Nov 2025 19:58:05 GMT
ENV GRADLE_VERSION=9.2.1
# Mon, 17 Nov 2025 19:58:05 GMT
ARG GRADLE_DOWNLOAD_SHA256=72f44c9f8ebcb1af43838f45ee5c4aa9c5444898b3468ab3f4af7b6076c5bc3f
# Mon, 17 Nov 2025 19:58:07 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=72f44c9f8ebcb1af43838f45ee5c4aa9c5444898b3468ab3f4af7b6076c5bc3f
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Mon, 17 Nov 2025 19:58:07 GMT
USER gradle
# Mon, 17 Nov 2025 19:58:08 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=72f44c9f8ebcb1af43838f45ee5c4aa9c5444898b3468ab3f4af7b6076c5bc3f
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --stacktrace --debug --version # buildkit
# Mon, 17 Nov 2025 19:58:08 GMT
USER root
```

-	Layers:
	-	`sha256:7164be7c15828f5ba5fa7731cf51dad23a5d6c99e19fa840e574def3f4c05894`  
		Last Modified: Wed, 12 Nov 2025 17:56:02 GMT  
		Size: 34.5 MB (34515519 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b97d03b24539b592900c6da5a05a15d58c5f0277fab11e67baf0cf20007fee4e`  
		Last Modified: Fri, 14 Nov 2025 01:13:26 GMT  
		Size: 58.2 MB (58179097 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93b96acd8dde5a7450830ab85f084ef2ecc0b51d8faf57d19b33c5346ce200d5`  
		Last Modified: Fri, 14 Nov 2025 01:14:00 GMT  
		Size: 92.0 MB (92046744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8e68da23e57f968e2b7ff346efdcb72cc45b2a2272bcc0a11191ca94c3f47a1`  
		Last Modified: Fri, 14 Nov 2025 01:13:48 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33ed3c765bdccfbea56d1caccd31a875b84d3872baf9d86a0fb08d380e05df8c`  
		Last Modified: Fri, 14 Nov 2025 01:13:48 GMT  
		Size: 2.3 KB (2289 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6aa5793d1e585bc4aed22cc2febfe141163dc0929944f36a4d1891cb86c97636`  
		Last Modified: Mon, 17 Nov 2025 19:58:42 GMT  
		Size: 1.6 KB (1624 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f53cee27d305dfa80364b110dc97907db179a284e17793a5a8c96732fd8c642`  
		Last Modified: Mon, 17 Nov 2025 19:58:47 GMT  
		Size: 39.1 MB (39070592 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3fe48af8baec41f82af821d52010032fca81bcd79b55e139fdf7866764655e2`  
		Last Modified: Mon, 17 Nov 2025 23:39:21 GMT  
		Size: 135.5 MB (135521970 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b124076a0c120afa24d79fcb6a18a0a44f41b09e80950e7efdb18b1241b8f332`  
		Last Modified: Mon, 17 Nov 2025 19:58:42 GMT  
		Size: 54.9 KB (54904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:jdk25-ubi-minimal` - unknown; unknown

```console
$ docker pull gradle@sha256:ce4a1b5016c3b9c29a620d25eaef4a7a7d1f536a399c2be6981a69fcdf4f1f83
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.9 MB (8902505 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cceb883a410a439f91e4b1649e8a65d9ed96d29dd9d800655da2e6cf45dc4280`

```dockerfile
```

-	Layers:
	-	`sha256:26c96b864433a36d8b2c33bc1806a85aa963e79498870e8880cb82283e307899`  
		Last Modified: Mon, 17 Nov 2025 21:26:09 GMT  
		Size: 8.9 MB (8877436 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:036ce8c56cf1a775814cc59eb19d1ccd517fdc7e33cc901d3cf1311efbcab300`  
		Last Modified: Mon, 17 Nov 2025 21:26:10 GMT  
		Size: 25.1 KB (25069 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:jdk25-ubi-minimal` - linux; arm64 variant v8

```console
$ docker pull gradle@sha256:19c21f5283043275dcbead5d24033f70f81111165e3f57d05fe76b1270d4820a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **355.6 MB (355636825 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa4b9ff9e0043a0cf17028b4375ec20df08a6ea345e46d47436652ce13ff1c57`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["gradle"]`

```dockerfile
# Wed, 12 Nov 2025 13:07:41 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 12 Nov 2025 13:07:41 GMT
LABEL vendor="Red Hat, Inc."
# Wed, 12 Nov 2025 13:07:41 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Wed, 12 Nov 2025 13:07:41 GMT
LABEL com.redhat.component="ubi10-minimal-container"       name="ubi10/ubi-minimal"       version="10.1"       cpe="cpe:/o:redhat:enterprise_linux:10.1"       distribution-scope="public"
# Wed, 12 Nov 2025 13:07:41 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 12 Nov 2025 13:07:41 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 10."
# Wed, 12 Nov 2025 13:07:41 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 12 Nov 2025 13:07:41 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 12 Nov 2025 13:07:41 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 10 Minimal"
# Wed, 12 Nov 2025 13:07:41 GMT
LABEL io.openshift.expose-services=""
# Wed, 12 Nov 2025 13:07:41 GMT
LABEL io.openshift.tags="minimal rhel10"
# Wed, 12 Nov 2025 13:07:41 GMT
ENV container oci
# Wed, 12 Nov 2025 13:07:42 GMT
COPY dir:7dfb9511ae2d70910df52107d5c96c0335e87f2a1f5d8a5592e4e62e34a4c8d6 in /      
# Wed, 12 Nov 2025 13:07:42 GMT
COPY file:5de33b5fc08b00635bccf9134a18978dba13e2250aa51838f9969515a3957847 in /etc/yum.repos.d/.      
# Wed, 12 Nov 2025 13:07:42 GMT
CMD ["/bin/bash"]
# Wed, 12 Nov 2025 13:07:42 GMT
COPY file:595171150af68abc798ea385f7988d74b566aa8e84babff137f00b08b2164683 in /usr/share/buildinfo/content-sets.json      
# Wed, 12 Nov 2025 13:07:42 GMT
COPY file:595171150af68abc798ea385f7988d74b566aa8e84babff137f00b08b2164683 in /root/buildinfo/content_manifests/content-sets.json      
# Wed, 12 Nov 2025 13:07:42 GMT
COPY file:5949e56b1cb83ef43c9cba7c361cdb23e3aace250acdaec4205faff29b91de6c in /usr/share/buildinfo/labels.json      
# Wed, 12 Nov 2025 13:07:42 GMT
COPY file:5949e56b1cb83ef43c9cba7c361cdb23e3aace250acdaec4205faff29b91de6c in /root/buildinfo/labels.json      
# Wed, 12 Nov 2025 13:07:42 GMT
LABEL "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="c2904cc9bad715599f86f4c20562b90929d43731" "org.opencontainers.image.revision"="c2904cc9bad715599f86f4c20562b90929d43731" "build-date"="2025-11-12T13:07:20Z" "release"="1762952303"org.opencontainers.image.revision=c2904cc9bad715599f86f4c20562b90929d43731
# Fri, 14 Nov 2025 01:29:20 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 14 Nov 2025 01:29:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 14 Nov 2025 01:29:20 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 14 Nov 2025 01:29:20 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en         gnupg2     ;     microdnf clean all # buildkit
# Fri, 14 Nov 2025 01:29:20 GMT
ENV JAVA_VERSION=jdk-25.0.1+8
# Fri, 14 Nov 2025 01:29:26 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='5c83b7d2121ed482fd06831a1eba1633dbab818aba6addddf48e075b97e6e9b8';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.1%2B8/OpenJDK25U-jdk_aarch64_linux_hotspot_25.0.1_8.tar.gz';          ;;        ppc64le)          ESUM='54fdfbfa2c463863bd0c2c9c19901320d25ca533f31daa0bd866c4104af7ce5b';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.1%2B8/OpenJDK25U-jdk_ppc64le_linux_hotspot_25.0.1_8.tar.gz';          ;;        s390x)          ESUM='1b627ec601998e5450fd1af91ae26a43b4d646403a8938d7efe4dfb2848fd896';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.1%2B8/OpenJDK25U-jdk_s390x_linux_hotspot_25.0.1_8.tar.gz';          ;;        x86_64)          ESUM='8daf77d1aacffe38c9889689bc224a13557de77559d9a5bb91991e6a298baa0d';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.1%2B8/OpenJDK25U-jdk_x64_linux_hotspot_25.0.1_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Fri, 14 Nov 2025 01:29:27 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Fri, 14 Nov 2025 01:29:27 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Fri, 14 Nov 2025 01:29:27 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Fri, 14 Nov 2025 01:29:27 GMT
CMD ["jshell"]
# Mon, 17 Nov 2025 19:56:32 GMT
CMD ["gradle"]
# Mon, 17 Nov 2025 19:56:32 GMT
ENV GRADLE_HOME=/opt/gradle
# Mon, 17 Nov 2025 19:56:32 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 101 gradle     && useradd --system --gid gradle --uid 101 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Mon, 17 Nov 2025 19:56:32 GMT
VOLUME [/home/gradle/.gradle]
# Mon, 17 Nov 2025 19:56:32 GMT
WORKDIR /home/gradle
# Mon, 17 Nov 2025 19:56:38 GMT
RUN set -o errexit -o nounset     && microdnf install -y         make         curl         wget         tar                 findutils                 unzip         which                 git         git-lfs         subversion     && microdnf clean all         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which svn # buildkit
# Mon, 17 Nov 2025 19:56:38 GMT
ENV GRADLE_VERSION=9.2.1
# Mon, 17 Nov 2025 19:56:38 GMT
ARG GRADLE_DOWNLOAD_SHA256=72f44c9f8ebcb1af43838f45ee5c4aa9c5444898b3468ab3f4af7b6076c5bc3f
# Mon, 17 Nov 2025 19:56:41 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=72f44c9f8ebcb1af43838f45ee5c4aa9c5444898b3468ab3f4af7b6076c5bc3f
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Mon, 17 Nov 2025 19:56:41 GMT
USER gradle
# Mon, 17 Nov 2025 19:56:41 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=72f44c9f8ebcb1af43838f45ee5c4aa9c5444898b3468ab3f4af7b6076c5bc3f
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --stacktrace --debug --version # buildkit
# Mon, 17 Nov 2025 19:56:41 GMT
USER root
```

-	Layers:
	-	`sha256:372b71efdab733f5ad0749f1537278e34899107888219d8358967ddbd9eb2db3`  
		Last Modified: Wed, 12 Nov 2025 18:16:55 GMT  
		Size: 32.6 MB (32601501 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3ea32a55604be9b61bbd1134a583b5f266e08be6a4b92ea763511068962be54`  
		Last Modified: Fri, 14 Nov 2025 01:30:02 GMT  
		Size: 57.8 MB (57785742 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53fda75791e8caab698ce2df26af1bc07f9dc8c1e6811d0d866faffe9283cf83`  
		Last Modified: Fri, 14 Nov 2025 01:30:03 GMT  
		Size: 91.1 MB (91056292 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b93e5ff814c8670707afd390a8245a0ec88bd0554b9aaf62e31f78ad1405cdea`  
		Last Modified: Fri, 14 Nov 2025 01:29:55 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ccf1896e5d2344eca2fb07323738e9285bb06acceb1f57589d914d94d376e5b`  
		Last Modified: Fri, 14 Nov 2025 01:29:56 GMT  
		Size: 2.3 KB (2290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9feef994a96de713f35b464dcd5ea5eac5c9ab15496609cb71fa63c1ab47a447`  
		Last Modified: Mon, 17 Nov 2025 19:57:12 GMT  
		Size: 1.6 KB (1619 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b329ed37a522f6a7d048e67a2cac17184cc67bb2695d2176d00b43966463ed28`  
		Last Modified: Mon, 17 Nov 2025 19:57:16 GMT  
		Size: 38.6 MB (38607724 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2805c5fa0768a448aa7ae07f9a457b18c0c1036fd80901fe130ed8ee9e168420`  
		Last Modified: Mon, 17 Nov 2025 19:57:06 GMT  
		Size: 135.5 MB (135521970 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96ee87ffb1dee1d6234b4b492bbf2b78da9769b74856b914a712895a8f01dfa1`  
		Last Modified: Mon, 17 Nov 2025 19:57:12 GMT  
		Size: 59.5 KB (59526 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:jdk25-ubi-minimal` - unknown; unknown

```console
$ docker pull gradle@sha256:b6d3cd67a3cec11e19efa1e343ffc12452caa53d44918ec0f6b946fd16f61b72
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.9 MB (8901067 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb557cf08bf50fe85cfc792652ab0c826067ca1b7ed3d882ccca317b8984082a`

```dockerfile
```

-	Layers:
	-	`sha256:e702de1e6e69aff2ddef81d3999b138979f676127cebb4c7999bc5308bfee3be`  
		Last Modified: Mon, 17 Nov 2025 21:26:19 GMT  
		Size: 8.9 MB (8875777 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7fedbd4cb85c512610c99a10ff9074ceab0208496f83f9d7271d30ffb1f2e76c`  
		Last Modified: Mon, 17 Nov 2025 21:26:20 GMT  
		Size: 25.3 KB (25290 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:jdk25-ubi-minimal` - linux; ppc64le

```console
$ docker pull gradle@sha256:6a6e7161ffc410f2715ffc40a0d32b22112addc1fb41b0528f957b5feb19830e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **367.1 MB (367074635 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e536a1bd1597ca44d02598357ab487992d82b8bb38deb3d793c10902697b0169`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["gradle"]`

```dockerfile
# Wed, 12 Nov 2025 13:21:41 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 12 Nov 2025 13:21:41 GMT
LABEL vendor="Red Hat, Inc."
# Wed, 12 Nov 2025 13:21:41 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Wed, 12 Nov 2025 13:21:41 GMT
LABEL com.redhat.component="ubi10-minimal-container"       name="ubi10/ubi-minimal"       version="10.1"       cpe="cpe:/o:redhat:enterprise_linux:10.1"       distribution-scope="public"
# Wed, 12 Nov 2025 13:21:41 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 12 Nov 2025 13:21:41 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 10."
# Wed, 12 Nov 2025 13:21:41 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 12 Nov 2025 13:21:41 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 12 Nov 2025 13:21:41 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 10 Minimal"
# Wed, 12 Nov 2025 13:21:41 GMT
LABEL io.openshift.expose-services=""
# Wed, 12 Nov 2025 13:21:41 GMT
LABEL io.openshift.tags="minimal rhel10"
# Wed, 12 Nov 2025 13:21:41 GMT
ENV container oci
# Wed, 12 Nov 2025 13:21:42 GMT
COPY dir:7f428fa29fa8f7e829b041452235ccc73eb7caf26242995ea3907c084b7e797f in /      
# Wed, 12 Nov 2025 13:21:42 GMT
COPY file:5de33b5fc08b00635bccf9134a18978dba13e2250aa51838f9969515a3957847 in /etc/yum.repos.d/.      
# Wed, 12 Nov 2025 13:21:42 GMT
CMD ["/bin/bash"]
# Wed, 12 Nov 2025 13:21:42 GMT
COPY file:595171150af68abc798ea385f7988d74b566aa8e84babff137f00b08b2164683 in /usr/share/buildinfo/content-sets.json      
# Wed, 12 Nov 2025 13:21:42 GMT
COPY file:595171150af68abc798ea385f7988d74b566aa8e84babff137f00b08b2164683 in /root/buildinfo/content_manifests/content-sets.json      
# Wed, 12 Nov 2025 13:21:42 GMT
COPY file:aa98cda558c12f3c05f9e28e398d23d3217b73b93e9d498cde74f10837d73035 in /usr/share/buildinfo/labels.json      
# Wed, 12 Nov 2025 13:21:42 GMT
COPY file:aa98cda558c12f3c05f9e28e398d23d3217b73b93e9d498cde74f10837d73035 in /root/buildinfo/labels.json      
# Wed, 12 Nov 2025 13:21:42 GMT
LABEL "architecture"="ppc64le" "vcs-type"="git" "vcs-ref"="c2904cc9bad715599f86f4c20562b90929d43731" "org.opencontainers.image.revision"="c2904cc9bad715599f86f4c20562b90929d43731" "build-date"="2025-11-12T13:21:30Z" "release"="1762952303"org.opencontainers.image.revision=c2904cc9bad715599f86f4c20562b90929d43731
# Fri, 14 Nov 2025 02:04:01 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 14 Nov 2025 02:04:01 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 14 Nov 2025 02:04:01 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 14 Nov 2025 02:04:01 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en         gnupg2     ;     microdnf clean all # buildkit
# Fri, 14 Nov 2025 02:04:01 GMT
ENV JAVA_VERSION=jdk-25.0.1+8
# Fri, 14 Nov 2025 02:24:23 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='5c83b7d2121ed482fd06831a1eba1633dbab818aba6addddf48e075b97e6e9b8';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.1%2B8/OpenJDK25U-jdk_aarch64_linux_hotspot_25.0.1_8.tar.gz';          ;;        ppc64le)          ESUM='54fdfbfa2c463863bd0c2c9c19901320d25ca533f31daa0bd866c4104af7ce5b';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.1%2B8/OpenJDK25U-jdk_ppc64le_linux_hotspot_25.0.1_8.tar.gz';          ;;        s390x)          ESUM='1b627ec601998e5450fd1af91ae26a43b4d646403a8938d7efe4dfb2848fd896';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.1%2B8/OpenJDK25U-jdk_s390x_linux_hotspot_25.0.1_8.tar.gz';          ;;        x86_64)          ESUM='8daf77d1aacffe38c9889689bc224a13557de77559d9a5bb91991e6a298baa0d';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.1%2B8/OpenJDK25U-jdk_x64_linux_hotspot_25.0.1_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Fri, 14 Nov 2025 02:24:26 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Fri, 14 Nov 2025 02:24:26 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Fri, 14 Nov 2025 02:24:26 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Fri, 14 Nov 2025 02:24:26 GMT
CMD ["jshell"]
# Mon, 17 Nov 2025 19:54:03 GMT
CMD ["gradle"]
# Mon, 17 Nov 2025 19:54:03 GMT
ENV GRADLE_HOME=/opt/gradle
# Mon, 17 Nov 2025 19:54:03 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 101 gradle     && useradd --system --gid gradle --uid 101 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Mon, 17 Nov 2025 19:54:03 GMT
VOLUME [/home/gradle/.gradle]
# Mon, 17 Nov 2025 19:54:04 GMT
WORKDIR /home/gradle
# Mon, 17 Nov 2025 19:54:26 GMT
RUN set -o errexit -o nounset     && microdnf install -y         make         curl         wget         tar                 findutils                 unzip         which                 git         git-lfs         subversion     && microdnf clean all         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which svn # buildkit
# Mon, 17 Nov 2025 19:54:26 GMT
ENV GRADLE_VERSION=9.2.1
# Mon, 17 Nov 2025 19:54:26 GMT
ARG GRADLE_DOWNLOAD_SHA256=72f44c9f8ebcb1af43838f45ee5c4aa9c5444898b3468ab3f4af7b6076c5bc3f
# Mon, 17 Nov 2025 19:54:32 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=72f44c9f8ebcb1af43838f45ee5c4aa9c5444898b3468ab3f4af7b6076c5bc3f
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Mon, 17 Nov 2025 19:54:32 GMT
USER gradle
# Mon, 17 Nov 2025 19:54:34 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=72f44c9f8ebcb1af43838f45ee5c4aa9c5444898b3468ab3f4af7b6076c5bc3f
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --stacktrace --debug --version # buildkit
# Mon, 17 Nov 2025 19:54:34 GMT
USER root
```

-	Layers:
	-	`sha256:402f9c025c3a63d9edbbd78a8cf9e2813de76854342058db2814aa404ddbcf6c`  
		Last Modified: Wed, 12 Nov 2025 18:16:57 GMT  
		Size: 38.7 MB (38746677 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6af666f8de2b0c285f4b7d038631ab495275355fdde5c07cca653c2f3d29143`  
		Last Modified: Fri, 14 Nov 2025 02:05:21 GMT  
		Size: 60.4 MB (60357723 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca868fea327a6b4f948380f87e107332a176485331e94119f93a5cd3a775bb27`  
		Last Modified: Fri, 14 Nov 2025 02:25:23 GMT  
		Size: 91.6 MB (91613046 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b47d62e60d4177eaa8b062292c8eff2e642b56652b1f3e97282f2d5f7862b9f`  
		Last Modified: Fri, 14 Nov 2025 02:25:13 GMT  
		Size: 130.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f8f78909fbf80269bbf2cf438fb4c82e6f5d9540e3866ccb7c9f8083854c383`  
		Last Modified: Fri, 14 Nov 2025 02:25:14 GMT  
		Size: 2.3 KB (2290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83f51f54b7036fdef128bbeb504e4192cdb679fcb114937c6a64a65a60918689`  
		Last Modified: Mon, 17 Nov 2025 19:56:16 GMT  
		Size: 1.6 KB (1624 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b520f0d3e326bfd80b2ceae5ef4c38a341a02c9b19f39ef2be242fe97aa90a80`  
		Last Modified: Mon, 17 Nov 2025 19:56:21 GMT  
		Size: 40.8 MB (40796135 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61cb9679e7a6c4a1a3fe971862e895428b27b9013fe9034faf3efa288b81ca80`  
		Last Modified: Mon, 17 Nov 2025 19:55:49 GMT  
		Size: 135.5 MB (135521970 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:094b04a734596a87be62106e5e9539d9465a9235c64b56050fef2a5ff3fb8517`  
		Last Modified: Mon, 17 Nov 2025 19:56:16 GMT  
		Size: 35.0 KB (35008 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:jdk25-ubi-minimal` - unknown; unknown

```console
$ docker pull gradle@sha256:1b7e1403a70c9031e0ec0d0f63f2cdb1f83e49085da9931b28fec4a222608779
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.9 MB (8895639 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:158a01a0961a3313fcfd584425cdd61986062400cc1528ede11c69528b5c5cbe`

```dockerfile
```

-	Layers:
	-	`sha256:e3d8ac2c65e5c0933175ec1e147132525c1241d7828fff90b22f91ef16dec1cd`  
		Last Modified: Mon, 17 Nov 2025 21:26:28 GMT  
		Size: 8.9 MB (8870484 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4cb9e92b1127f969941837dc86fe5942ba70d54c779ec854146990541ae5bf8e`  
		Last Modified: Mon, 17 Nov 2025 21:26:29 GMT  
		Size: 25.2 KB (25155 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:jdk25-ubi-minimal` - linux; s390x

```console
$ docker pull gradle@sha256:f2e78545c8f3635d6ad494b8cf6bfad9e619135413a391bfa857f5063edaf9ce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **357.9 MB (357850719 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2017e4a00093c141a10fe3aa739d98bca8cca923c0d27de71e902ecb17f8e5fa`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["gradle"]`

```dockerfile
# Wed, 12 Nov 2025 13:48:02 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 12 Nov 2025 13:48:02 GMT
LABEL vendor="Red Hat, Inc."
# Wed, 12 Nov 2025 13:48:02 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Wed, 12 Nov 2025 13:48:02 GMT
LABEL com.redhat.component="ubi10-minimal-container"       name="ubi10/ubi-minimal"       version="10.1"       cpe="cpe:/o:redhat:enterprise_linux:10.1"       distribution-scope="public"
# Wed, 12 Nov 2025 13:48:02 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 12 Nov 2025 13:48:02 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 10."
# Wed, 12 Nov 2025 13:48:02 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 12 Nov 2025 13:48:02 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 12 Nov 2025 13:48:02 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 10 Minimal"
# Wed, 12 Nov 2025 13:48:02 GMT
LABEL io.openshift.expose-services=""
# Wed, 12 Nov 2025 13:48:02 GMT
LABEL io.openshift.tags="minimal rhel10"
# Wed, 12 Nov 2025 13:48:02 GMT
ENV container oci
# Wed, 12 Nov 2025 13:48:02 GMT
COPY dir:9f3cd8bad135d97a4278eb0e74f1a89cc165a45d6f123e529f2973da46a240af in /      
# Wed, 12 Nov 2025 13:48:02 GMT
COPY file:5de33b5fc08b00635bccf9134a18978dba13e2250aa51838f9969515a3957847 in /etc/yum.repos.d/.      
# Wed, 12 Nov 2025 13:48:02 GMT
CMD ["/bin/bash"]
# Wed, 12 Nov 2025 13:48:02 GMT
COPY file:595171150af68abc798ea385f7988d74b566aa8e84babff137f00b08b2164683 in /usr/share/buildinfo/content-sets.json      
# Wed, 12 Nov 2025 13:48:02 GMT
COPY file:595171150af68abc798ea385f7988d74b566aa8e84babff137f00b08b2164683 in /root/buildinfo/content_manifests/content-sets.json      
# Wed, 12 Nov 2025 13:48:03 GMT
COPY file:cb4b6de2d10271c95dac78e592bde3a3d1599b2eb6bebad022cd5ead593fccb8 in /usr/share/buildinfo/labels.json      
# Wed, 12 Nov 2025 13:48:03 GMT
COPY file:cb4b6de2d10271c95dac78e592bde3a3d1599b2eb6bebad022cd5ead593fccb8 in /root/buildinfo/labels.json      
# Wed, 12 Nov 2025 13:48:03 GMT
LABEL "architecture"="s390x" "vcs-type"="git" "vcs-ref"="c2904cc9bad715599f86f4c20562b90929d43731" "org.opencontainers.image.revision"="c2904cc9bad715599f86f4c20562b90929d43731" "build-date"="2025-11-12T13:45:41Z" "release"="1762952303"org.opencontainers.image.revision=c2904cc9bad715599f86f4c20562b90929d43731
# Fri, 14 Nov 2025 01:36:56 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 14 Nov 2025 01:36:56 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 14 Nov 2025 01:36:56 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 14 Nov 2025 01:36:56 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en         gnupg2     ;     microdnf clean all # buildkit
# Fri, 14 Nov 2025 01:36:56 GMT
ENV JAVA_VERSION=jdk-25.0.1+8
# Fri, 14 Nov 2025 01:40:54 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='5c83b7d2121ed482fd06831a1eba1633dbab818aba6addddf48e075b97e6e9b8';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.1%2B8/OpenJDK25U-jdk_aarch64_linux_hotspot_25.0.1_8.tar.gz';          ;;        ppc64le)          ESUM='54fdfbfa2c463863bd0c2c9c19901320d25ca533f31daa0bd866c4104af7ce5b';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.1%2B8/OpenJDK25U-jdk_ppc64le_linux_hotspot_25.0.1_8.tar.gz';          ;;        s390x)          ESUM='1b627ec601998e5450fd1af91ae26a43b4d646403a8938d7efe4dfb2848fd896';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.1%2B8/OpenJDK25U-jdk_s390x_linux_hotspot_25.0.1_8.tar.gz';          ;;        x86_64)          ESUM='8daf77d1aacffe38c9889689bc224a13557de77559d9a5bb91991e6a298baa0d';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.1%2B8/OpenJDK25U-jdk_x64_linux_hotspot_25.0.1_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Fri, 14 Nov 2025 01:40:55 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Fri, 14 Nov 2025 01:40:55 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Fri, 14 Nov 2025 01:40:55 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Fri, 14 Nov 2025 01:40:55 GMT
CMD ["jshell"]
# Mon, 17 Nov 2025 19:54:17 GMT
CMD ["gradle"]
# Mon, 17 Nov 2025 19:54:17 GMT
ENV GRADLE_HOME=/opt/gradle
# Mon, 17 Nov 2025 19:54:17 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 101 gradle     && useradd --system --gid gradle --uid 101 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Mon, 17 Nov 2025 19:54:17 GMT
VOLUME [/home/gradle/.gradle]
# Mon, 17 Nov 2025 19:54:17 GMT
WORKDIR /home/gradle
# Mon, 17 Nov 2025 19:54:41 GMT
RUN set -o errexit -o nounset     && microdnf install -y         make         curl         wget         tar                 findutils                 unzip         which                 git         git-lfs         subversion     && microdnf clean all         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which svn # buildkit
# Mon, 17 Nov 2025 19:54:41 GMT
ENV GRADLE_VERSION=9.2.1
# Mon, 17 Nov 2025 19:54:41 GMT
ARG GRADLE_DOWNLOAD_SHA256=72f44c9f8ebcb1af43838f45ee5c4aa9c5444898b3468ab3f4af7b6076c5bc3f
# Mon, 17 Nov 2025 19:54:46 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=72f44c9f8ebcb1af43838f45ee5c4aa9c5444898b3468ab3f4af7b6076c5bc3f
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Mon, 17 Nov 2025 19:54:46 GMT
USER gradle
# Mon, 17 Nov 2025 19:54:47 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=72f44c9f8ebcb1af43838f45ee5c4aa9c5444898b3468ab3f4af7b6076c5bc3f
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --stacktrace --debug --version # buildkit
# Mon, 17 Nov 2025 19:54:47 GMT
USER root
```

-	Layers:
	-	`sha256:2c5bd53b2567eef590494f06f626482f402fa97fb095307b2a27e75fe98f195b`  
		Last Modified: Wed, 12 Nov 2025 18:16:54 GMT  
		Size: 34.4 MB (34378541 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a86b5f1c27d55d732e1d564e35c7811cd6d8226b38c683337005753638213a52`  
		Last Modified: Fri, 14 Nov 2025 01:37:38 GMT  
		Size: 58.6 MB (58551503 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfdb395fd8dd8c8fb8c89d520d07884be6a92625122107793ed4ccc8da28d9e7`  
		Last Modified: Fri, 14 Nov 2025 01:41:41 GMT  
		Size: 88.2 MB (88211719 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb579f16800ae105935f1dfe284dc8c593a14fee16b440ff30d9fdbb6054b83b`  
		Last Modified: Fri, 14 Nov 2025 01:41:27 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbb30759b01530e17bd781ece7a95c9f53ca78580e84232e873ca0db53b3ad2e`  
		Last Modified: Fri, 14 Nov 2025 01:41:26 GMT  
		Size: 2.3 KB (2291 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae4df47a1e473cb61cc68cd1f3cd0e1a2b1acf2c22ee96f0870f03a2fa3915f0`  
		Last Modified: Mon, 17 Nov 2025 19:56:13 GMT  
		Size: 1.6 KB (1623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0cfb54b3720d7ccfc1321781c31da405063cdbff19f68fb96df3b5a8623d89c`  
		Last Modified: Mon, 17 Nov 2025 19:56:21 GMT  
		Size: 41.1 MB (41147906 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae4a0de1fdadf548460017b8b5bf6e8a82adea50ab222dda062996be13e235b2`  
		Last Modified: Mon, 17 Nov 2025 23:39:50 GMT  
		Size: 135.5 MB (135521969 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90d81846b241f954c166da18c6a9c010bba05f4be85641bb48a22aeaba647f31`  
		Last Modified: Mon, 17 Nov 2025 19:56:13 GMT  
		Size: 35.0 KB (35007 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:jdk25-ubi-minimal` - unknown; unknown

```console
$ docker pull gradle@sha256:e41f2224089f0f6a039452600b6cfb353d9484421362cab72a8014b79280650d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.9 MB (8885636 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4304a2c9f25d6f527adaf2ceb2316aeaa59bd27f28abd8efaa1c651e54cf912a`

```dockerfile
```

-	Layers:
	-	`sha256:e4c6837bf6690bdb41c159672e63181b589176859119903cde867d2afec0df0a`  
		Last Modified: Mon, 17 Nov 2025 21:26:36 GMT  
		Size: 8.9 MB (8860567 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2297413f433a2b98147f195787302a537b0398e2ade0be6d6a9677d764c29c58`  
		Last Modified: Mon, 17 Nov 2025 21:26:37 GMT  
		Size: 25.1 KB (25069 bytes)  
		MIME: application/vnd.in-toto+json
