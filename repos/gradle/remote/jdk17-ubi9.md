## `gradle:jdk17-ubi9`

```console
$ docker pull gradle@sha256:ceaa510e5614be8520346d062be6d05675dfab18d88ae9257bc342bc5809e1d4
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

### `gradle:jdk17-ubi9` - linux; amd64

```console
$ docker pull gradle@sha256:f0af631471a9f5ad13c54da26e97a3316d907d26ba2a1fd8bcd76c49389e8b63
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **392.8 MB (392811456 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:66a63b9523a1ab6be3695ab54df831285d4b86421d771708b84ccd1754d35e6f`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["gradle"]`

```dockerfile
# Thu, 25 Jun 2026 05:47:54 GMT
LABEL maintainer="Red Hat, Inc."
# Thu, 25 Jun 2026 05:47:54 GMT
LABEL vendor="Red Hat, Inc."
# Thu, 25 Jun 2026 05:47:54 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Thu, 25 Jun 2026 05:47:54 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.8"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Thu, 25 Jun 2026 05:47:54 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Thu, 25 Jun 2026 05:47:54 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Thu, 25 Jun 2026 05:47:54 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 25 Jun 2026 05:47:54 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 25 Jun 2026 05:47:54 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Thu, 25 Jun 2026 05:47:54 GMT
LABEL io.openshift.expose-services=""
# Thu, 25 Jun 2026 05:47:54 GMT
LABEL io.openshift.tags="minimal rhel9"
# Thu, 25 Jun 2026 05:47:54 GMT
ENV container oci
# Thu, 25 Jun 2026 05:47:55 GMT
COPY dir:a7d61486b18f71651e6d0b0c0267c96964cdf86a5c99a34dafc1bfd05eac4cc1 in /      
# Thu, 25 Jun 2026 05:47:55 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Thu, 25 Jun 2026 05:47:55 GMT
CMD ["/bin/bash"]
# Thu, 25 Jun 2026 05:47:55 GMT
COPY dir:bc9ddd3d40bc004a03f930c7616b544996fd5453e30f14853f7ba4b54693ba2e in /usr/share/buildinfo/      
# Thu, 25 Jun 2026 05:47:55 GMT
COPY dir:bc9ddd3d40bc004a03f930c7616b544996fd5453e30f14853f7ba4b54693ba2e in /root/buildinfo/      
# Thu, 25 Jun 2026 05:47:55 GMT
LABEL "org.opencontainers.image.created"="2026-06-25T05:47:36Z" "org.opencontainers.image.revision"="b76cbbe03678b6bed00cb452eb031ce6d202c981" "build-date"="2026-06-25T05:47:36Z" "architecture"="x86_64" "vcs-ref"="b76cbbe03678b6bed00cb452eb031ce6d202c981" "vcs-type"="git" "release"="1782366411"org.opencontainers.image.created=2026-06-25T05:47:36Z,org.opencontainers.image.revision=b76cbbe03678b6bed00cb452eb031ce6d202c981
# Thu, 25 Jun 2026 23:26:57 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 25 Jun 2026 23:26:57 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 25 Jun 2026 23:26:57 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 25 Jun 2026 23:26:57 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en     ;     microdnf clean all # buildkit
# Thu, 25 Jun 2026 23:26:57 GMT
ENV JAVA_VERSION=jdk-17.0.19+10
# Thu, 25 Jun 2026 23:27:04 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='83a52172678ec8975164648654869cb2e71d7c748b47aca94b29bbfa10c18e81';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.19%2B10/OpenJDK17U-jdk_aarch64_linux_hotspot_17.0.19_10.tar.gz';          ;;        ppc64le)          ESUM='c9d8dc52960ff00aa8c321e211cc5284a2151cffdedeac998f5297066cbad245';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.19%2B10/OpenJDK17U-jdk_ppc64le_linux_hotspot_17.0.19_10.tar.gz';          ;;        s390x)          ESUM='00363a5ceda57aa0dee89d20b3f6b2966e3c1f3fb6dcf57e66d2264573d3c63e';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.19%2B10/OpenJDK17U-jdk_s390x_linux_hotspot_17.0.19_10.tar.gz';          ;;        x86_64)          ESUM='d8afc263758141a66e0e3aafc321e783f7016696f4eaea067d340a269037d331';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.19%2B10/OpenJDK17U-jdk_x64_linux_hotspot_17.0.19_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Thu, 25 Jun 2026 23:27:05 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 25 Jun 2026 23:27:05 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 25 Jun 2026 23:27:05 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 25 Jun 2026 23:27:05 GMT
CMD ["jshell"]
# Mon, 29 Jun 2026 17:13:12 GMT
CMD ["gradle"]
# Mon, 29 Jun 2026 17:13:12 GMT
ENV GRADLE_HOME=/opt/gradle
# Mon, 29 Jun 2026 17:13:12 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 101 gradle     && useradd --system --gid gradle --uid 101 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Mon, 29 Jun 2026 17:13:12 GMT
VOLUME [/home/gradle/.gradle]
# Mon, 29 Jun 2026 17:13:12 GMT
WORKDIR /home/gradle
# Mon, 29 Jun 2026 17:13:16 GMT
RUN set -o errexit -o nounset     && microdnf install -y         make         curl-minimal         wget         tar                 findutils                 unzip         which                 git         git-lfs         subversion     && microdnf clean all         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which svn # buildkit
# Mon, 29 Jun 2026 17:13:16 GMT
ENV GRADLE_VERSION=9.6.1
# Mon, 29 Jun 2026 17:13:16 GMT
ARG GRADLE_DOWNLOAD_SHA256=9c0f7faeeb306cb14e4279a3e084ca6b596894089a0638e68a07c945a32c9e14
# Mon, 29 Jun 2026 17:13:18 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=9c0f7faeeb306cb14e4279a3e084ca6b596894089a0638e68a07c945a32c9e14
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Mon, 29 Jun 2026 17:13:18 GMT
USER gradle
# Mon, 29 Jun 2026 17:13:19 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=9c0f7faeeb306cb14e4279a3e084ca6b596894089a0638e68a07c945a32c9e14
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --stacktrace --debug --version # buildkit
# Mon, 29 Jun 2026 17:13:19 GMT
USER root
```

-	Layers:
	-	`sha256:837b9d7bd4c8301d318ec8c5cd7e5aab81e392d60e90b733f39c67bbadc97aef`  
		Last Modified: Thu, 25 Jun 2026 06:49:07 GMT  
		Size: 40.7 MB (40689274 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54f8d592b0a99999546239f22395bd0d607e80234d8dfaba30792d1b45312da6`  
		Last Modified: Thu, 25 Jun 2026 23:27:21 GMT  
		Size: 27.7 MB (27660246 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ab1a9e7bcbb0e64ed338aaeb631fd51bf9e42380ca540ca0c5ee5eb312db9f0`  
		Last Modified: Thu, 25 Jun 2026 23:27:25 GMT  
		Size: 145.9 MB (145915433 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7569802730cf38a707c3b1765a8a51d8edb8d90f9369c9ce9984f13240b110bc`  
		Last Modified: Thu, 25 Jun 2026 23:27:20 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec94efb62548db8274a34bab0d2e0aeba3608bd2f2a005a68677835e642c38f6`  
		Last Modified: Thu, 25 Jun 2026 23:27:20 GMT  
		Size: 2.3 KB (2292 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:281213d0ae2c1726410414f433cfe7a93a9b930c40bc9e49e2f1b25293e58e17`  
		Last Modified: Mon, 29 Jun 2026 17:13:36 GMT  
		Size: 1.7 KB (1719 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1e86772860acce6bae31792c2aedea087de5ba936634914a73a516517c650c9`  
		Last Modified: Mon, 29 Jun 2026 17:13:37 GMT  
		Size: 37.9 MB (37920691 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05a517dd8c99f19d2728c31beb5b844d8d1ae63958cc07c0863066b0306bfcdc`  
		Last Modified: Mon, 29 Jun 2026 17:13:40 GMT  
		Size: 140.6 MB (140596028 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c72be59c5c791c9d9d6de966c5ddf9fd73d13e127156201aced346f76612f073`  
		Last Modified: Mon, 29 Jun 2026 17:13:36 GMT  
		Size: 25.6 KB (25613 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:jdk17-ubi9` - unknown; unknown

```console
$ docker pull gradle@sha256:0b5fe506d82c74cb502c5b9fcb9f741fc96be15121046ad9bb972faca60f29d6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5456174 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe45f6479658d44a3ae6658965ffa157cac2ef0e656d37e4e5a6a8d9f3403777`

```dockerfile
```

-	Layers:
	-	`sha256:ec9e311ca07c61ddebd82a7de40832bc0ab3025df07ffc0ab8c93ea082d76834`  
		Last Modified: Mon, 29 Jun 2026 17:13:36 GMT  
		Size: 5.4 MB (5432974 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:079f6beef03b8e7220f19791e05ffbbbfffeecb62818a6306518592804d2e056`  
		Last Modified: Mon, 29 Jun 2026 17:13:36 GMT  
		Size: 23.2 KB (23200 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:jdk17-ubi9` - linux; arm64 variant v8

```console
$ docker pull gradle@sha256:c6a8b5c50d5be2c127e6e7138243235698d78c73789c787535e5095e3fe800bf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **389.5 MB (389486735 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9cd4fd4f8affb34e010d7c4969df6512436f4fd57a2d1bea7c062219f80e248e`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["gradle"]`

```dockerfile
# Thu, 25 Jun 2026 05:49:52 GMT
LABEL maintainer="Red Hat, Inc."
# Thu, 25 Jun 2026 05:49:52 GMT
LABEL vendor="Red Hat, Inc."
# Thu, 25 Jun 2026 05:49:52 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Thu, 25 Jun 2026 05:49:52 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.8"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Thu, 25 Jun 2026 05:49:52 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Thu, 25 Jun 2026 05:49:52 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Thu, 25 Jun 2026 05:49:52 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 25 Jun 2026 05:49:52 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 25 Jun 2026 05:49:52 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Thu, 25 Jun 2026 05:49:52 GMT
LABEL io.openshift.expose-services=""
# Thu, 25 Jun 2026 05:49:52 GMT
LABEL io.openshift.tags="minimal rhel9"
# Thu, 25 Jun 2026 05:49:52 GMT
ENV container oci
# Thu, 25 Jun 2026 05:49:53 GMT
COPY dir:b536f0b76258d9997dadb73f000a4dcb4ac61a94c87f2002404cf80795af1987 in /      
# Thu, 25 Jun 2026 05:49:53 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Thu, 25 Jun 2026 05:49:53 GMT
CMD ["/bin/bash"]
# Thu, 25 Jun 2026 05:49:53 GMT
COPY dir:b92b494a8ba7f60e9dc6ef43f3b9b86d3f1fe0910e706399a14b6f518777f64a in /usr/share/buildinfo/      
# Thu, 25 Jun 2026 05:49:53 GMT
COPY dir:b92b494a8ba7f60e9dc6ef43f3b9b86d3f1fe0910e706399a14b6f518777f64a in /root/buildinfo/      
# Thu, 25 Jun 2026 05:49:54 GMT
LABEL "org.opencontainers.image.created"="2026-06-25T05:49:31Z" "org.opencontainers.image.revision"="b76cbbe03678b6bed00cb452eb031ce6d202c981" "build-date"="2026-06-25T05:49:31Z" "architecture"="aarch64" "vcs-ref"="b76cbbe03678b6bed00cb452eb031ce6d202c981" "vcs-type"="git" "release"="1782366411"org.opencontainers.image.created=2026-06-25T05:49:31Z,org.opencontainers.image.revision=b76cbbe03678b6bed00cb452eb031ce6d202c981
# Thu, 25 Jun 2026 23:26:47 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 25 Jun 2026 23:26:47 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 25 Jun 2026 23:26:47 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 25 Jun 2026 23:26:47 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en     ;     microdnf clean all # buildkit
# Thu, 25 Jun 2026 23:26:47 GMT
ENV JAVA_VERSION=jdk-17.0.19+10
# Thu, 25 Jun 2026 23:26:54 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='83a52172678ec8975164648654869cb2e71d7c748b47aca94b29bbfa10c18e81';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.19%2B10/OpenJDK17U-jdk_aarch64_linux_hotspot_17.0.19_10.tar.gz';          ;;        ppc64le)          ESUM='c9d8dc52960ff00aa8c321e211cc5284a2151cffdedeac998f5297066cbad245';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.19%2B10/OpenJDK17U-jdk_ppc64le_linux_hotspot_17.0.19_10.tar.gz';          ;;        s390x)          ESUM='00363a5ceda57aa0dee89d20b3f6b2966e3c1f3fb6dcf57e66d2264573d3c63e';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.19%2B10/OpenJDK17U-jdk_s390x_linux_hotspot_17.0.19_10.tar.gz';          ;;        x86_64)          ESUM='d8afc263758141a66e0e3aafc321e783f7016696f4eaea067d340a269037d331';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.19%2B10/OpenJDK17U-jdk_x64_linux_hotspot_17.0.19_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Thu, 25 Jun 2026 23:26:55 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 25 Jun 2026 23:26:55 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 25 Jun 2026 23:26:55 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 25 Jun 2026 23:26:55 GMT
CMD ["jshell"]
# Mon, 29 Jun 2026 17:12:57 GMT
CMD ["gradle"]
# Mon, 29 Jun 2026 17:12:57 GMT
ENV GRADLE_HOME=/opt/gradle
# Mon, 29 Jun 2026 17:12:57 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 101 gradle     && useradd --system --gid gradle --uid 101 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Mon, 29 Jun 2026 17:12:57 GMT
VOLUME [/home/gradle/.gradle]
# Mon, 29 Jun 2026 17:12:57 GMT
WORKDIR /home/gradle
# Mon, 29 Jun 2026 17:13:00 GMT
RUN set -o errexit -o nounset     && microdnf install -y         make         curl-minimal         wget         tar                 findutils                 unzip         which                 git         git-lfs         subversion     && microdnf clean all         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which svn # buildkit
# Mon, 29 Jun 2026 17:13:00 GMT
ENV GRADLE_VERSION=9.6.1
# Mon, 29 Jun 2026 17:13:00 GMT
ARG GRADLE_DOWNLOAD_SHA256=9c0f7faeeb306cb14e4279a3e084ca6b596894089a0638e68a07c945a32c9e14
# Mon, 29 Jun 2026 17:13:03 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=9c0f7faeeb306cb14e4279a3e084ca6b596894089a0638e68a07c945a32c9e14
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Mon, 29 Jun 2026 17:13:03 GMT
USER gradle
# Mon, 29 Jun 2026 17:13:03 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=9c0f7faeeb306cb14e4279a3e084ca6b596894089a0638e68a07c945a32c9e14
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --stacktrace --debug --version # buildkit
# Mon, 29 Jun 2026 17:13:03 GMT
USER root
```

-	Layers:
	-	`sha256:f224574d4b82cf6adf57df98fdab92768ce7f1579fbe0678919b872f4d435c0e`  
		Last Modified: Thu, 25 Jun 2026 06:49:07 GMT  
		Size: 38.8 MB (38818113 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce2a20bd928a551c4dae61fca1688fa5a77e6ba138bd3fbd4ef9332c34474f42`  
		Last Modified: Thu, 25 Jun 2026 23:27:13 GMT  
		Size: 28.1 MB (28100333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4394a79745f0cfee448efe59395987c09ec229fcb4e52e75e7964233b7ec40c2`  
		Last Modified: Thu, 25 Jun 2026 23:27:15 GMT  
		Size: 144.7 MB (144734847 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc4b7685d18f9dad3fe47198bee715bec4017fa3573fb501ba40517f1f3df88f`  
		Last Modified: Thu, 25 Jun 2026 23:27:12 GMT  
		Size: 130.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7446ad7f712a6287e84abf6706a36b80292d1a4e179508cb3919650843731285`  
		Last Modified: Thu, 25 Jun 2026 23:27:12 GMT  
		Size: 2.3 KB (2292 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ec517b5e05e243c0e6628a7ab4f6bbc7e344e94a5b6b568e9cd48aa14269918`  
		Last Modified: Mon, 29 Jun 2026 17:13:21 GMT  
		Size: 1.7 KB (1713 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7a66c1db8982e536751fecebbd26d07ac1efb6b6697bc358711be6f87b4131b`  
		Last Modified: Mon, 29 Jun 2026 17:13:22 GMT  
		Size: 37.2 MB (37203915 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8cc0a5e0f44779432b3406f7caa4520b44a18e34883d1c5c88d98babbac8c47`  
		Last Modified: Mon, 29 Jun 2026 17:13:24 GMT  
		Size: 140.6 MB (140596025 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1739c07101206b3b9215109cb3b10cb8f2adea4a4f9dbcdad48d2f6025203841`  
		Last Modified: Mon, 29 Jun 2026 17:13:21 GMT  
		Size: 29.3 KB (29335 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:jdk17-ubi9` - unknown; unknown

```console
$ docker pull gradle@sha256:5e00dc19c1542fc65706577b048b6d10543835007f2ccde46d32919e8402c047
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5453923 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3d883f27769b81a8a2624821c174c8911ff8a7b008a5eafcf4d0bea66580b18`

```dockerfile
```

-	Layers:
	-	`sha256:464e70421f580465353f74e1c4cca0d2756be00ee46e02121c3753113cf1d122`  
		Last Modified: Mon, 29 Jun 2026 17:13:21 GMT  
		Size: 5.4 MB (5430574 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:75d914fd1cc6f38e37f9a03419850a78ef976a9827ea7adfb721b35e4035d002`  
		Last Modified: Mon, 29 Jun 2026 17:13:20 GMT  
		Size: 23.3 KB (23349 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:jdk17-ubi9` - linux; ppc64le

```console
$ docker pull gradle@sha256:eacc069b41c620a5d0ea59b34d83658a06506339d9df9d5f502bf11b27f50eff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **400.7 MB (400748307 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:417d14c6007eea31cd0ce852a8a1bff7cd7f74b0dfb51670ae48b813f18c3f52`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["gradle"]`

```dockerfile
# Thu, 25 Jun 2026 05:49:04 GMT
LABEL maintainer="Red Hat, Inc."
# Thu, 25 Jun 2026 05:49:04 GMT
LABEL vendor="Red Hat, Inc."
# Thu, 25 Jun 2026 05:49:04 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Thu, 25 Jun 2026 05:49:04 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.8"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Thu, 25 Jun 2026 05:49:04 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Thu, 25 Jun 2026 05:49:04 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Thu, 25 Jun 2026 05:49:04 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 25 Jun 2026 05:49:04 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 25 Jun 2026 05:49:04 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Thu, 25 Jun 2026 05:49:04 GMT
LABEL io.openshift.expose-services=""
# Thu, 25 Jun 2026 05:49:04 GMT
LABEL io.openshift.tags="minimal rhel9"
# Thu, 25 Jun 2026 05:49:04 GMT
ENV container oci
# Thu, 25 Jun 2026 05:49:05 GMT
COPY dir:f90c99a59bd474ed6a51399eee7df05393563fdaaa902130421d08a1a3fedeec in /      
# Thu, 25 Jun 2026 05:49:05 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Thu, 25 Jun 2026 05:49:05 GMT
CMD ["/bin/bash"]
# Thu, 25 Jun 2026 05:49:05 GMT
COPY dir:cb70b1c584e490eac8673058fb514f718bb38524b957a3c5934b6749eca2ca95 in /usr/share/buildinfo/      
# Thu, 25 Jun 2026 05:49:05 GMT
COPY dir:cb70b1c584e490eac8673058fb514f718bb38524b957a3c5934b6749eca2ca95 in /root/buildinfo/      
# Thu, 25 Jun 2026 05:49:05 GMT
LABEL "org.opencontainers.image.created"="2026-06-25T05:48:49Z" "org.opencontainers.image.revision"="b76cbbe03678b6bed00cb452eb031ce6d202c981" "build-date"="2026-06-25T05:48:49Z" "architecture"="ppc64le" "vcs-ref"="b76cbbe03678b6bed00cb452eb031ce6d202c981" "vcs-type"="git" "release"="1782366411"org.opencontainers.image.created=2026-06-25T05:48:49Z,org.opencontainers.image.revision=b76cbbe03678b6bed00cb452eb031ce6d202c981
# Thu, 25 Jun 2026 23:26:15 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 25 Jun 2026 23:26:15 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 25 Jun 2026 23:26:15 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 25 Jun 2026 23:26:15 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en     ;     microdnf clean all # buildkit
# Thu, 25 Jun 2026 23:26:15 GMT
ENV JAVA_VERSION=jdk-17.0.19+10
# Thu, 25 Jun 2026 23:27:54 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='83a52172678ec8975164648654869cb2e71d7c748b47aca94b29bbfa10c18e81';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.19%2B10/OpenJDK17U-jdk_aarch64_linux_hotspot_17.0.19_10.tar.gz';          ;;        ppc64le)          ESUM='c9d8dc52960ff00aa8c321e211cc5284a2151cffdedeac998f5297066cbad245';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.19%2B10/OpenJDK17U-jdk_ppc64le_linux_hotspot_17.0.19_10.tar.gz';          ;;        s390x)          ESUM='00363a5ceda57aa0dee89d20b3f6b2966e3c1f3fb6dcf57e66d2264573d3c63e';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.19%2B10/OpenJDK17U-jdk_s390x_linux_hotspot_17.0.19_10.tar.gz';          ;;        x86_64)          ESUM='d8afc263758141a66e0e3aafc321e783f7016696f4eaea067d340a269037d331';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.19%2B10/OpenJDK17U-jdk_x64_linux_hotspot_17.0.19_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Thu, 25 Jun 2026 23:27:58 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 25 Jun 2026 23:27:58 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 25 Jun 2026 23:27:58 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 25 Jun 2026 23:27:58 GMT
CMD ["jshell"]
# Mon, 29 Jun 2026 17:20:11 GMT
CMD ["gradle"]
# Mon, 29 Jun 2026 17:20:11 GMT
ENV GRADLE_HOME=/opt/gradle
# Mon, 29 Jun 2026 17:20:11 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 101 gradle     && useradd --system --gid gradle --uid 101 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Mon, 29 Jun 2026 17:20:11 GMT
VOLUME [/home/gradle/.gradle]
# Mon, 29 Jun 2026 17:20:11 GMT
WORKDIR /home/gradle
# Mon, 29 Jun 2026 17:20:21 GMT
RUN set -o errexit -o nounset     && microdnf install -y         make         curl-minimal         wget         tar                 findutils                 unzip         which                 git         git-lfs         subversion     && microdnf clean all         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which svn # buildkit
# Mon, 29 Jun 2026 17:20:21 GMT
ENV GRADLE_VERSION=9.6.1
# Mon, 29 Jun 2026 17:20:21 GMT
ARG GRADLE_DOWNLOAD_SHA256=9c0f7faeeb306cb14e4279a3e084ca6b596894089a0638e68a07c945a32c9e14
# Mon, 29 Jun 2026 17:20:25 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=9c0f7faeeb306cb14e4279a3e084ca6b596894089a0638e68a07c945a32c9e14
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Mon, 29 Jun 2026 17:20:25 GMT
USER gradle
# Mon, 29 Jun 2026 17:20:27 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=9c0f7faeeb306cb14e4279a3e084ca6b596894089a0638e68a07c945a32c9e14
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --stacktrace --debug --version # buildkit
# Mon, 29 Jun 2026 17:20:27 GMT
USER root
```

-	Layers:
	-	`sha256:1ce5d05f6e5641b082a71f1e9acc2940448540498097c2a35b74cf93310f5178`  
		Last Modified: Thu, 25 Jun 2026 12:13:27 GMT  
		Size: 45.1 MB (45075525 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:454ffa9ad55609063881c74aef17705d7d65e97d1f5ceadb3fe8c414ff22b193`  
		Last Modified: Thu, 25 Jun 2026 23:26:50 GMT  
		Size: 30.1 MB (30082746 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30f570731b969781599ddfaa1bf88f9f03fcecf993cb7134c9355db8c548e219`  
		Last Modified: Thu, 25 Jun 2026 23:28:34 GMT  
		Size: 145.8 MB (145788799 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17572c83d7f117ee7aa02873303bdabd2ac89a64c89d9015d7223daaa0c8a9b3`  
		Last Modified: Thu, 25 Jun 2026 23:28:31 GMT  
		Size: 130.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:728cda52b8b404bc80686a3419f4501c59034d916f06533c70cfe6ba51122edb`  
		Last Modified: Thu, 25 Jun 2026 23:28:31 GMT  
		Size: 2.3 KB (2288 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63e98d3b2d91b55759d124637f5f99f27d2dea62db5c28dd3379e007761ecddd`  
		Last Modified: Mon, 29 Jun 2026 17:21:02 GMT  
		Size: 1.7 KB (1715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69e691af32bfd95c5ea209a955586f6e43fe1761e636689c806d66678ee2604c`  
		Last Modified: Mon, 29 Jun 2026 17:21:04 GMT  
		Size: 39.2 MB (39200665 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e19e36d9f3704b40b490fe84e9f58400d9e78b04863863cb1a546d1c0ff3dfac`  
		Last Modified: Mon, 29 Jun 2026 17:21:07 GMT  
		Size: 140.6 MB (140596027 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2f3374ba44bcb5720f2bcff7cdfc2ba6f281b5ec44613d685f312fa936ae777`  
		Last Modified: Mon, 29 Jun 2026 17:21:02 GMT  
		Size: 380.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:jdk17-ubi9` - unknown; unknown

```console
$ docker pull gradle@sha256:63bff68b43aaf8af5522ad521cfde24a0fc9de6f837f05540348cb6fd2439e08
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5451825 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b926103a1faff25380a5ccb7fe459606471952c5418ef5515d3dea9b35b7a95`

```dockerfile
```

-	Layers:
	-	`sha256:1d8802399add5f745a8e1c99d700e8a01afb371e79d569376ccfd37af3cacec2`  
		Last Modified: Mon, 29 Jun 2026 17:21:02 GMT  
		Size: 5.4 MB (5428541 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2915b7a17bb4f00d419a9419b1d26c69543f4b3ff1da004172f9a31686c80b3a`  
		Last Modified: Mon, 29 Jun 2026 17:21:02 GMT  
		Size: 23.3 KB (23284 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:jdk17-ubi9` - linux; s390x

```console
$ docker pull gradle@sha256:c8873016c3fb3c01f07654fe90f32b9fe04610e50092227b669b53c2ccca24c7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **380.5 MB (380456348 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e67d3bf2293a078d0920639fe8301f8f3266d34981625d13817f8dc4b1ee1053`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["gradle"]`

```dockerfile
# Thu, 25 Jun 2026 05:52:27 GMT
LABEL maintainer="Red Hat, Inc."
# Thu, 25 Jun 2026 05:52:27 GMT
LABEL vendor="Red Hat, Inc."
# Thu, 25 Jun 2026 05:52:27 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Thu, 25 Jun 2026 05:52:27 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.8"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Thu, 25 Jun 2026 05:52:27 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Thu, 25 Jun 2026 05:52:27 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Thu, 25 Jun 2026 05:52:27 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 25 Jun 2026 05:52:27 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 25 Jun 2026 05:52:27 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Thu, 25 Jun 2026 05:52:27 GMT
LABEL io.openshift.expose-services=""
# Thu, 25 Jun 2026 05:52:27 GMT
LABEL io.openshift.tags="minimal rhel9"
# Thu, 25 Jun 2026 05:52:27 GMT
ENV container oci
# Thu, 25 Jun 2026 05:52:27 GMT
COPY dir:1e4f533284314158fe9071edbf6e5a91d133d00a252b00de728bc4926b26b337 in /      
# Thu, 25 Jun 2026 05:52:27 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Thu, 25 Jun 2026 05:52:27 GMT
CMD ["/bin/bash"]
# Thu, 25 Jun 2026 05:52:27 GMT
COPY dir:5b21c0bd8fdb721477bc5c6da5a748382232df7791527a89e418bc39ef6e03ed in /usr/share/buildinfo/      
# Thu, 25 Jun 2026 05:52:28 GMT
COPY dir:5b21c0bd8fdb721477bc5c6da5a748382232df7791527a89e418bc39ef6e03ed in /root/buildinfo/      
# Thu, 25 Jun 2026 05:52:28 GMT
LABEL "org.opencontainers.image.created"="2026-06-25T05:51:47Z" "org.opencontainers.image.revision"="b76cbbe03678b6bed00cb452eb031ce6d202c981" "build-date"="2026-06-25T05:51:47Z" "architecture"="s390x" "vcs-ref"="b76cbbe03678b6bed00cb452eb031ce6d202c981" "vcs-type"="git" "release"="1782366411"org.opencontainers.image.created=2026-06-25T05:51:47Z,org.opencontainers.image.revision=b76cbbe03678b6bed00cb452eb031ce6d202c981
# Thu, 25 Jun 2026 23:24:53 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 25 Jun 2026 23:24:53 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 25 Jun 2026 23:24:53 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 25 Jun 2026 23:24:53 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en     ;     microdnf clean all # buildkit
# Thu, 25 Jun 2026 23:24:53 GMT
ENV JAVA_VERSION=jdk-17.0.19+10
# Thu, 25 Jun 2026 23:25:47 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='83a52172678ec8975164648654869cb2e71d7c748b47aca94b29bbfa10c18e81';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.19%2B10/OpenJDK17U-jdk_aarch64_linux_hotspot_17.0.19_10.tar.gz';          ;;        ppc64le)          ESUM='c9d8dc52960ff00aa8c321e211cc5284a2151cffdedeac998f5297066cbad245';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.19%2B10/OpenJDK17U-jdk_ppc64le_linux_hotspot_17.0.19_10.tar.gz';          ;;        s390x)          ESUM='00363a5ceda57aa0dee89d20b3f6b2966e3c1f3fb6dcf57e66d2264573d3c63e';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.19%2B10/OpenJDK17U-jdk_s390x_linux_hotspot_17.0.19_10.tar.gz';          ;;        x86_64)          ESUM='d8afc263758141a66e0e3aafc321e783f7016696f4eaea067d340a269037d331';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.19%2B10/OpenJDK17U-jdk_x64_linux_hotspot_17.0.19_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Thu, 25 Jun 2026 23:25:48 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 25 Jun 2026 23:25:48 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 25 Jun 2026 23:25:48 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 25 Jun 2026 23:25:48 GMT
CMD ["jshell"]
# Mon, 29 Jun 2026 17:13:05 GMT
CMD ["gradle"]
# Mon, 29 Jun 2026 17:13:05 GMT
ENV GRADLE_HOME=/opt/gradle
# Mon, 29 Jun 2026 17:13:05 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 101 gradle     && useradd --system --gid gradle --uid 101 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Mon, 29 Jun 2026 17:13:05 GMT
VOLUME [/home/gradle/.gradle]
# Mon, 29 Jun 2026 17:13:05 GMT
WORKDIR /home/gradle
# Mon, 29 Jun 2026 17:13:10 GMT
RUN set -o errexit -o nounset     && microdnf install -y         make         curl-minimal         wget         tar                 findutils                 unzip         which                 git         git-lfs         subversion     && microdnf clean all         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which svn # buildkit
# Mon, 29 Jun 2026 17:13:10 GMT
ENV GRADLE_VERSION=9.6.1
# Mon, 29 Jun 2026 17:13:10 GMT
ARG GRADLE_DOWNLOAD_SHA256=9c0f7faeeb306cb14e4279a3e084ca6b596894089a0638e68a07c945a32c9e14
# Mon, 29 Jun 2026 17:13:15 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=9c0f7faeeb306cb14e4279a3e084ca6b596894089a0638e68a07c945a32c9e14
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Mon, 29 Jun 2026 17:13:15 GMT
USER gradle
# Mon, 29 Jun 2026 17:13:15 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=9c0f7faeeb306cb14e4279a3e084ca6b596894089a0638e68a07c945a32c9e14
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --stacktrace --debug --version # buildkit
# Mon, 29 Jun 2026 17:13:15 GMT
USER root
```

-	Layers:
	-	`sha256:601b4838142f06d7d4e767a327592a762187b9af6287ad5286218612b47da08f`  
		Last Modified: Thu, 25 Jun 2026 12:13:18 GMT  
		Size: 38.7 MB (38740623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4d56fdf4a501fd1e5907df8f4855ca4cdce9cce7c88c365b62d0c0c6c2c13b2`  
		Last Modified: Thu, 25 Jun 2026 23:25:23 GMT  
		Size: 27.7 MB (27683811 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd3e6372422429ca90637b9dee5a058b20527a4b804f9c19a298599a1e6c2ee8`  
		Last Modified: Thu, 25 Jun 2026 23:26:12 GMT  
		Size: 135.9 MB (135912248 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aba85f00f9286be247f172bfa811da01b510275ad0774b3250d36ba90544c35e`  
		Last Modified: Thu, 25 Jun 2026 23:26:10 GMT  
		Size: 130.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f857fbbd9681314b972219fe0d647f87a380ca2cd5d338719621c22c660086fb`  
		Last Modified: Thu, 25 Jun 2026 23:26:10 GMT  
		Size: 2.3 KB (2292 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7863ddec08374866aea8934ed353af7c5ab37887be90b0d617059926f8a8e3d8`  
		Last Modified: Mon, 29 Jun 2026 17:13:40 GMT  
		Size: 1.7 KB (1716 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e1e8cdffc14344871ef9ca83e768d71d1c7a885a7b5d293a607f1e91cd32b86`  
		Last Modified: Mon, 29 Jun 2026 17:13:41 GMT  
		Size: 37.5 MB (37519145 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45db4d78abd48e1e9042c31c2a60653ecd97814861582466256cc881abeb5af6`  
		Last Modified: Mon, 29 Jun 2026 17:13:43 GMT  
		Size: 140.6 MB (140595976 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec98a9756efe3269aa80506d25b31f4b9f53342e7ac6cbeae5e5fb413e96d6c2`  
		Last Modified: Mon, 29 Jun 2026 17:13:40 GMT  
		Size: 375.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:jdk17-ubi9` - unknown; unknown

```console
$ docker pull gradle@sha256:78957e2eeabe8c8273d04ebcaa3083fbcfe6b855fb7e6dcd28ee9771322d9dd8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5441031 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d914f9059fcf43b1ccfc4210d4b033e04444f95f35ba72bea334b4bfac2f1c45`

```dockerfile
```

-	Layers:
	-	`sha256:1124d3b25270375af0fe2e2e122ed2721657ee19b6d947a61389cc71bf5791db`  
		Last Modified: Mon, 29 Jun 2026 17:13:40 GMT  
		Size: 5.4 MB (5417797 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:235f57294f4a3026ed251d2429b5d0170b31f9a0343f6c50556bfcc5f7824468`  
		Last Modified: Mon, 29 Jun 2026 17:13:40 GMT  
		Size: 23.2 KB (23234 bytes)  
		MIME: application/vnd.in-toto+json
