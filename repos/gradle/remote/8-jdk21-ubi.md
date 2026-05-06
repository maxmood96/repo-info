## `gradle:8-jdk21-ubi`

```console
$ docker pull gradle@sha256:139898667be4db26ec2fe69251329eae3f0202ce922ebfd115ff7a233e519b95
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

### `gradle:8-jdk21-ubi` - linux; amd64

```console
$ docker pull gradle@sha256:88682bcb1bfb8125487b3c55bc74828f22943e25d17c17cb32300aec4281200a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **402.8 MB (402798987 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6103dc4ad40e54bdb906ad2b55e9de8093f68e8ea450b79f2722d60df176e151`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["gradle"]`

```dockerfile
# Mon, 04 May 2026 01:27:16 GMT
LABEL maintainer="Red Hat, Inc."
# Mon, 04 May 2026 01:27:16 GMT
LABEL vendor="Red Hat, Inc."
# Mon, 04 May 2026 01:27:16 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Mon, 04 May 2026 01:27:16 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.7"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Mon, 04 May 2026 01:27:16 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Mon, 04 May 2026 01:27:16 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Mon, 04 May 2026 01:27:17 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 04 May 2026 01:27:17 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 04 May 2026 01:27:17 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Mon, 04 May 2026 01:27:17 GMT
LABEL io.openshift.expose-services=""
# Mon, 04 May 2026 01:27:17 GMT
LABEL io.openshift.tags="minimal rhel9"
# Mon, 04 May 2026 01:27:17 GMT
ENV container oci
# Mon, 04 May 2026 01:27:17 GMT
COPY dir:65829633e0a732ee03a3da731062eca14df67dc0e6bab86d02002ef9d123d97c in /      
# Mon, 04 May 2026 01:27:17 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Mon, 04 May 2026 01:27:17 GMT
CMD ["/bin/bash"]
# Mon, 04 May 2026 01:27:17 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /usr/share/buildinfo/content-sets.json      
# Mon, 04 May 2026 01:27:17 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /root/buildinfo/content_manifests/content-sets.json      
# Mon, 04 May 2026 01:27:18 GMT
COPY file:c2149fceb878782b97b2875047824d21e0e5ecd57a50bf8e1dd5d47550f18358 in /usr/share/buildinfo/labels.json      
# Mon, 04 May 2026 01:27:18 GMT
COPY file:c2149fceb878782b97b2875047824d21e0e5ecd57a50bf8e1dd5d47550f18358 in /root/buildinfo/labels.json      
# Mon, 04 May 2026 01:27:18 GMT
LABEL "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="dbf428e1775c5e4c4802b4c714d3b50b652d0c8a" "org.opencontainers.image.revision"="dbf428e1775c5e4c4802b4c714d3b50b652d0c8a" "build-date"="2026-05-04T01:27:05Z" "org.opencontainers.image.created"="2026-05-04T01:27:05Z" "release"="1777857961"org.opencontainers.image.revision=dbf428e1775c5e4c4802b4c714d3b50b652d0c8a,org.opencontainers.image.created=2026-05-04T01:27:05Z
# Tue, 05 May 2026 23:08:41 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 05 May 2026 23:08:41 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 05 May 2026 23:08:41 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 05 May 2026 23:08:41 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en     ;     microdnf clean all # buildkit
# Tue, 05 May 2026 23:08:41 GMT
ENV JAVA_VERSION=jdk-21.0.10+7
# Tue, 05 May 2026 23:08:48 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='357fee29fb0d5c079f6730db98b28942df13a6eed426f6c61cd4ad703ab27b9a';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.10%2B7/OpenJDK21U-jdk_aarch64_linux_hotspot_21.0.10_7.tar.gz';          ;;        ppc64le)          ESUM='33bdaec351f40cc70d44e251a54c23e4dd15fed8adc041e35c57461c706cf948';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.10%2B7/OpenJDK21U-jdk_ppc64le_linux_hotspot_21.0.10_7.tar.gz';          ;;        s390x)          ESUM='eabb069b59a2e6b9e9926d9c533186aabf1ff3b4af683d0a3620bb7c7d9770c0';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.10%2B7/OpenJDK21U-jdk_s390x_linux_hotspot_21.0.10_7.tar.gz';          ;;        x86_64)          ESUM='ea3b9bd464d6dd253e9a7accf59f7ccd2a36e4aa69640b7251e3370caef896a4';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.10%2B7/OpenJDK21U-jdk_x64_linux_hotspot_21.0.10_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Tue, 05 May 2026 23:08:49 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 05 May 2026 23:08:49 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 05 May 2026 23:08:49 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 05 May 2026 23:08:49 GMT
CMD ["jshell"]
# Wed, 06 May 2026 00:12:03 GMT
CMD ["gradle"]
# Wed, 06 May 2026 00:12:03 GMT
ENV GRADLE_HOME=/opt/gradle
# Wed, 06 May 2026 00:12:03 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 101 gradle     && useradd --system --gid gradle --uid 101 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Wed, 06 May 2026 00:12:03 GMT
VOLUME [/home/gradle/.gradle]
# Wed, 06 May 2026 00:12:03 GMT
WORKDIR /home/gradle
# Wed, 06 May 2026 00:12:08 GMT
RUN set -o errexit -o nounset     && microdnf install -y         make                 findutils                 unzip         which                 git         git-lfs         subversion     && microdnf clean all         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which svn # buildkit
# Wed, 06 May 2026 00:12:08 GMT
ENV GRADLE_VERSION=8.14.4
# Wed, 06 May 2026 00:12:08 GMT
ARG GRADLE_DOWNLOAD_SHA256=f1771298a70f6db5a29daf62378c4e18a17fc33c9ba6b14362e0cdf40610380d
# Wed, 06 May 2026 00:12:11 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=f1771298a70f6db5a29daf62378c4e18a17fc33c9ba6b14362e0cdf40610380d
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Wed, 06 May 2026 00:12:11 GMT
USER gradle
# Wed, 06 May 2026 00:12:12 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=f1771298a70f6db5a29daf62378c4e18a17fc33c9ba6b14362e0cdf40610380d
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Wed, 06 May 2026 00:12:12 GMT
USER root
```

-	Layers:
	-	`sha256:cd8d59cb7a894fbcbefe70d3cdbc433492e715351e24e77b24a441609ab2de47`  
		Last Modified: Mon, 04 May 2026 03:52:20 GMT  
		Size: 40.0 MB (40019116 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8867db3a979255b166fe2ee9866a48f6cd0dcaf69b21c994b156a97cdf550f1`  
		Last Modified: Tue, 05 May 2026 23:09:05 GMT  
		Size: 16.2 MB (16237648 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:786b17fb0a5905b7583e3ff0dc83a422314e0281f742a17a121af516fad55ab4`  
		Last Modified: Tue, 05 May 2026 23:09:08 GMT  
		Size: 157.9 MB (157860988 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b14c443505862b03aa95ad6113fd818d05ca0969e81d07e6c3ea81c1c8174975`  
		Last Modified: Tue, 05 May 2026 23:09:04 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0bb7034a44415ca4745376b12cd09cb68921c39738e57a13a42d006ffb169b9a`  
		Last Modified: Tue, 05 May 2026 23:09:04 GMT  
		Size: 2.3 KB (2292 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82beff65545a8ae6ab12949ccdd8c7674190e7a9600f752b081fabc6b81fb54d`  
		Last Modified: Wed, 06 May 2026 00:12:28 GMT  
		Size: 1.4 KB (1418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e1dfe4045c0930d0c8ee8c26d68d3bc9397703d6f25a9c12f78d08edc475704`  
		Last Modified: Wed, 06 May 2026 00:12:31 GMT  
		Size: 51.2 MB (51234190 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2add2ea67b3d28f8a20b59144687dbbd7190be0669fb87c63f9d9d5095260581`  
		Last Modified: Wed, 06 May 2026 00:12:33 GMT  
		Size: 137.4 MB (137388270 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de48e90af21e99cf43d87909e127781528e66592b7fcbaac41dcfc26a8ac58e9`  
		Last Modified: Wed, 06 May 2026 00:12:29 GMT  
		Size: 54.9 KB (54905 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:8-jdk21-ubi` - unknown; unknown

```console
$ docker pull gradle@sha256:7a5cc35f48c71bfdbfcd223b1786d661a1bfd956720a39f86ddd0615f16b6363
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5431734 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:64b1a6c9a3d07e13b5622b78e8b08df8675458268a5cd49b37ac94706e4f2fdb`

```dockerfile
```

-	Layers:
	-	`sha256:d8ad604abed19e71a06c06412bfebc5d8d01d8e210cfad825bccad3b76d5db41`  
		Last Modified: Wed, 06 May 2026 00:12:29 GMT  
		Size: 5.4 MB (5408181 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bc378cb3d1f4c2531623018960c343a7ab64e7521e61fb168e0a94837fdf45ff`  
		Last Modified: Wed, 06 May 2026 00:12:29 GMT  
		Size: 23.6 KB (23553 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:8-jdk21-ubi` - linux; arm64 variant v8

```console
$ docker pull gradle@sha256:a6d6fb521fab63758866995bc33be8199fffeb33f6537d76c8e750128148a1cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **399.0 MB (399001935 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d173030a7cd63712dca0c68ef1e2f594c5afe68c7e34efbfd9fcd27617f1ead`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["gradle"]`

```dockerfile
# Mon, 04 May 2026 01:30:08 GMT
LABEL maintainer="Red Hat, Inc."
# Mon, 04 May 2026 01:30:08 GMT
LABEL vendor="Red Hat, Inc."
# Mon, 04 May 2026 01:30:08 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Mon, 04 May 2026 01:30:08 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.7"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Mon, 04 May 2026 01:30:08 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Mon, 04 May 2026 01:30:08 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Mon, 04 May 2026 01:30:08 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 04 May 2026 01:30:08 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 04 May 2026 01:30:08 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Mon, 04 May 2026 01:30:08 GMT
LABEL io.openshift.expose-services=""
# Mon, 04 May 2026 01:30:08 GMT
LABEL io.openshift.tags="minimal rhel9"
# Mon, 04 May 2026 01:30:08 GMT
ENV container oci
# Mon, 04 May 2026 01:30:09 GMT
COPY dir:5ad712b8248d48b2932fa5bdcc0ad50ec37c7d49fe231a7db1a1c2391217329a in /      
# Mon, 04 May 2026 01:30:09 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Mon, 04 May 2026 01:30:09 GMT
CMD ["/bin/bash"]
# Mon, 04 May 2026 01:30:09 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /usr/share/buildinfo/content-sets.json      
# Mon, 04 May 2026 01:30:09 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /root/buildinfo/content_manifests/content-sets.json      
# Mon, 04 May 2026 01:30:09 GMT
COPY file:11a91ebd5ef22e4f28676b4a9dc8447f7af7f01609b0311ebd76ca9c6631f340 in /usr/share/buildinfo/labels.json      
# Mon, 04 May 2026 01:30:10 GMT
COPY file:11a91ebd5ef22e4f28676b4a9dc8447f7af7f01609b0311ebd76ca9c6631f340 in /root/buildinfo/labels.json      
# Mon, 04 May 2026 01:30:10 GMT
LABEL "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="dbf428e1775c5e4c4802b4c714d3b50b652d0c8a" "org.opencontainers.image.revision"="dbf428e1775c5e4c4802b4c714d3b50b652d0c8a" "build-date"="2026-05-04T01:29:56Z" "org.opencontainers.image.created"="2026-05-04T01:29:56Z" "release"="1777857961"org.opencontainers.image.revision=dbf428e1775c5e4c4802b4c714d3b50b652d0c8a,org.opencontainers.image.created=2026-05-04T01:29:56Z
# Tue, 05 May 2026 23:08:23 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 05 May 2026 23:08:23 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 05 May 2026 23:08:23 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 05 May 2026 23:08:23 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en     ;     microdnf clean all # buildkit
# Tue, 05 May 2026 23:08:23 GMT
ENV JAVA_VERSION=jdk-21.0.10+7
# Tue, 05 May 2026 23:08:30 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='357fee29fb0d5c079f6730db98b28942df13a6eed426f6c61cd4ad703ab27b9a';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.10%2B7/OpenJDK21U-jdk_aarch64_linux_hotspot_21.0.10_7.tar.gz';          ;;        ppc64le)          ESUM='33bdaec351f40cc70d44e251a54c23e4dd15fed8adc041e35c57461c706cf948';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.10%2B7/OpenJDK21U-jdk_ppc64le_linux_hotspot_21.0.10_7.tar.gz';          ;;        s390x)          ESUM='eabb069b59a2e6b9e9926d9c533186aabf1ff3b4af683d0a3620bb7c7d9770c0';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.10%2B7/OpenJDK21U-jdk_s390x_linux_hotspot_21.0.10_7.tar.gz';          ;;        x86_64)          ESUM='ea3b9bd464d6dd253e9a7accf59f7ccd2a36e4aa69640b7251e3370caef896a4';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.10%2B7/OpenJDK21U-jdk_x64_linux_hotspot_21.0.10_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Tue, 05 May 2026 23:08:32 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 05 May 2026 23:08:32 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 05 May 2026 23:08:32 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 05 May 2026 23:08:32 GMT
CMD ["jshell"]
# Wed, 06 May 2026 00:12:29 GMT
CMD ["gradle"]
# Wed, 06 May 2026 00:12:29 GMT
ENV GRADLE_HOME=/opt/gradle
# Wed, 06 May 2026 00:12:29 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 101 gradle     && useradd --system --gid gradle --uid 101 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Wed, 06 May 2026 00:12:29 GMT
VOLUME [/home/gradle/.gradle]
# Wed, 06 May 2026 00:12:29 GMT
WORKDIR /home/gradle
# Wed, 06 May 2026 00:12:35 GMT
RUN set -o errexit -o nounset     && microdnf install -y         make                 findutils                 unzip         which                 git         git-lfs         subversion     && microdnf clean all         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which svn # buildkit
# Wed, 06 May 2026 00:12:35 GMT
ENV GRADLE_VERSION=8.14.4
# Wed, 06 May 2026 00:12:35 GMT
ARG GRADLE_DOWNLOAD_SHA256=f1771298a70f6db5a29daf62378c4e18a17fc33c9ba6b14362e0cdf40610380d
# Wed, 06 May 2026 00:12:39 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=f1771298a70f6db5a29daf62378c4e18a17fc33c9ba6b14362e0cdf40610380d
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Wed, 06 May 2026 00:12:39 GMT
USER gradle
# Wed, 06 May 2026 00:12:39 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=f1771298a70f6db5a29daf62378c4e18a17fc33c9ba6b14362e0cdf40610380d
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Wed, 06 May 2026 00:12:39 GMT
USER root
```

-	Layers:
	-	`sha256:eae0b4c39ea6d65927abe502bd11bbd574acc09733cb468c989628c5b204a24b`  
		Last Modified: Mon, 04 May 2026 05:13:02 GMT  
		Size: 38.2 MB (38205818 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07eef3e47e9e52d67c80563c4a034b09c4a46c4913227de3f5cfdb8cd463d4a9`  
		Last Modified: Tue, 05 May 2026 23:08:49 GMT  
		Size: 16.8 MB (16767572 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f5c9b526bf1ec6471edacef88ab743a6dd79a132edcda020db4688aac607b64`  
		Last Modified: Tue, 05 May 2026 23:08:54 GMT  
		Size: 156.1 MB (156136155 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83332b3db9a7726a6d3ba4773669284dd53702758eb71dc3bfca873b48fc34d8`  
		Last Modified: Tue, 05 May 2026 23:08:48 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e987ddb28ab58101424545972ffd0bbbf0333cec9348b32b02b187092d5b72e`  
		Last Modified: Tue, 05 May 2026 23:08:45 GMT  
		Size: 2.3 KB (2291 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:487ac0a3261a2c66f06f23b6a1b8ec750201f9e5d5b55aa51778add401e9c56c`  
		Last Modified: Wed, 06 May 2026 00:12:57 GMT  
		Size: 1.4 KB (1419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36fbad3395a3eb82641b9718d7477f8eaba9e141a1156ef61ea1ee7093d47126`  
		Last Modified: Wed, 06 May 2026 00:12:59 GMT  
		Size: 50.4 MB (50440718 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3acafe30d89b8486d00d82ae90beaa40c7204b9c110861e6beefc1bfe31863a`  
		Last Modified: Wed, 06 May 2026 00:13:02 GMT  
		Size: 137.4 MB (137388272 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1eaa90bc788936d5b15d482fad67e48640d91bfb18f468bd0043989e16da3c84`  
		Last Modified: Wed, 06 May 2026 00:12:57 GMT  
		Size: 59.5 KB (59530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:8-jdk21-ubi` - unknown; unknown

```console
$ docker pull gradle@sha256:bd816ce59ccbdd97fd606986d86fae2210a204f9944e37c4c29097767df3a738
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5431313 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7228080e10a02b71122fbef9a0737b820a3db6b8669ad7397b091260b30e8176`

```dockerfile
```

-	Layers:
	-	`sha256:e37f1bf62eb35145dda8be8f464c8a57f3ae276c2c846a62de5939ce5bc97481`  
		Last Modified: Wed, 06 May 2026 00:12:57 GMT  
		Size: 5.4 MB (5407587 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2f0e52cdced8dec20b16ff7ee3ffd298d7c6ad4bf626ebd7d74fc5127bbadb3f`  
		Last Modified: Wed, 06 May 2026 00:12:57 GMT  
		Size: 23.7 KB (23726 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:8-jdk21-ubi` - linux; ppc64le

```console
$ docker pull gradle@sha256:c16cc2f659cb51fc4e9e7b1f790ff93077ad12fc431b914de19ebd4fc1036abf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **411.1 MB (411108565 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e0e43dd99365c8bf7f050d4b54cd97eb2a954333d35607982d10632f5bf24c2`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["gradle"]`

```dockerfile
# Mon, 04 May 2026 01:28:51 GMT
LABEL maintainer="Red Hat, Inc."
# Mon, 04 May 2026 01:28:51 GMT
LABEL vendor="Red Hat, Inc."
# Mon, 04 May 2026 01:28:51 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Mon, 04 May 2026 01:28:52 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.7"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Mon, 04 May 2026 01:28:52 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Mon, 04 May 2026 01:28:52 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Mon, 04 May 2026 01:28:52 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 04 May 2026 01:28:52 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 04 May 2026 01:28:52 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Mon, 04 May 2026 01:28:52 GMT
LABEL io.openshift.expose-services=""
# Mon, 04 May 2026 01:28:52 GMT
LABEL io.openshift.tags="minimal rhel9"
# Mon, 04 May 2026 01:28:52 GMT
ENV container oci
# Mon, 04 May 2026 01:28:52 GMT
COPY dir:95ecb7253fddf635ae6d975427ddb73b0a49c785b217cf296b0a0358678fc43f in /      
# Mon, 04 May 2026 01:28:52 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Mon, 04 May 2026 01:28:52 GMT
CMD ["/bin/bash"]
# Mon, 04 May 2026 01:28:52 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /usr/share/buildinfo/content-sets.json      
# Mon, 04 May 2026 01:28:52 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /root/buildinfo/content_manifests/content-sets.json      
# Mon, 04 May 2026 01:28:53 GMT
COPY file:21c41e3d00d3a684fc39637052cae774dab908d634556245b0fd07fa3273162a in /usr/share/buildinfo/labels.json      
# Mon, 04 May 2026 01:28:53 GMT
COPY file:21c41e3d00d3a684fc39637052cae774dab908d634556245b0fd07fa3273162a in /root/buildinfo/labels.json      
# Mon, 04 May 2026 01:28:53 GMT
LABEL "architecture"="ppc64le" "vcs-type"="git" "vcs-ref"="dbf428e1775c5e4c4802b4c714d3b50b652d0c8a" "org.opencontainers.image.revision"="dbf428e1775c5e4c4802b4c714d3b50b652d0c8a" "build-date"="2026-05-04T01:28:41Z" "org.opencontainers.image.created"="2026-05-04T01:28:41Z" "release"="1777857961"org.opencontainers.image.revision=dbf428e1775c5e4c4802b4c714d3b50b652d0c8a,org.opencontainers.image.created=2026-05-04T01:28:41Z
# Tue, 05 May 2026 23:48:45 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 05 May 2026 23:48:45 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 05 May 2026 23:48:45 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 05 May 2026 23:48:45 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en     ;     microdnf clean all # buildkit
# Tue, 05 May 2026 23:48:45 GMT
ENV JAVA_VERSION=jdk-21.0.10+7
# Tue, 05 May 2026 23:54:16 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='357fee29fb0d5c079f6730db98b28942df13a6eed426f6c61cd4ad703ab27b9a';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.10%2B7/OpenJDK21U-jdk_aarch64_linux_hotspot_21.0.10_7.tar.gz';          ;;        ppc64le)          ESUM='33bdaec351f40cc70d44e251a54c23e4dd15fed8adc041e35c57461c706cf948';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.10%2B7/OpenJDK21U-jdk_ppc64le_linux_hotspot_21.0.10_7.tar.gz';          ;;        s390x)          ESUM='eabb069b59a2e6b9e9926d9c533186aabf1ff3b4af683d0a3620bb7c7d9770c0';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.10%2B7/OpenJDK21U-jdk_s390x_linux_hotspot_21.0.10_7.tar.gz';          ;;        x86_64)          ESUM='ea3b9bd464d6dd253e9a7accf59f7ccd2a36e4aa69640b7251e3370caef896a4';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.10%2B7/OpenJDK21U-jdk_x64_linux_hotspot_21.0.10_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Tue, 05 May 2026 23:54:19 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 05 May 2026 23:54:20 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 05 May 2026 23:54:20 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 05 May 2026 23:54:20 GMT
CMD ["jshell"]
# Wed, 06 May 2026 00:17:06 GMT
CMD ["gradle"]
# Wed, 06 May 2026 00:17:06 GMT
ENV GRADLE_HOME=/opt/gradle
# Wed, 06 May 2026 00:17:06 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 101 gradle     && useradd --system --gid gradle --uid 101 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Wed, 06 May 2026 00:17:06 GMT
VOLUME [/home/gradle/.gradle]
# Wed, 06 May 2026 00:17:06 GMT
WORKDIR /home/gradle
# Wed, 06 May 2026 00:20:41 GMT
RUN set -o errexit -o nounset     && microdnf install -y         make                 findutils                 unzip         which                 git         git-lfs         subversion     && microdnf clean all         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which svn # buildkit
# Wed, 06 May 2026 00:20:41 GMT
ENV GRADLE_VERSION=8.14.4
# Wed, 06 May 2026 00:20:41 GMT
ARG GRADLE_DOWNLOAD_SHA256=f1771298a70f6db5a29daf62378c4e18a17fc33c9ba6b14362e0cdf40610380d
# Wed, 06 May 2026 00:20:47 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=f1771298a70f6db5a29daf62378c4e18a17fc33c9ba6b14362e0cdf40610380d
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Wed, 06 May 2026 00:20:47 GMT
USER gradle
# Wed, 06 May 2026 00:20:49 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=f1771298a70f6db5a29daf62378c4e18a17fc33c9ba6b14362e0cdf40610380d
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Wed, 06 May 2026 00:20:49 GMT
USER root
```

-	Layers:
	-	`sha256:651dc6a385386e8e87790c18da9695023b6028435c56101235d26c0359b72932`  
		Last Modified: Mon, 04 May 2026 06:11:22 GMT  
		Size: 44.4 MB (44437692 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1767d5eb85065ec07c318883803129ba6d9958ad6e2956b0bc74061b3eaad718`  
		Last Modified: Tue, 05 May 2026 23:49:22 GMT  
		Size: 17.9 MB (17908683 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06c84d92d2fe8f6a96cf83e39e006bf86e825b6f591f8b209ca60aabf7781c37`  
		Last Modified: Tue, 05 May 2026 23:55:04 GMT  
		Size: 158.0 MB (157981319 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b14af0d9abc495842efce701dae797f5db8d69d630e9f57da85fceb8c4d24ab`  
		Last Modified: Tue, 05 May 2026 23:55:00 GMT  
		Size: 130.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1940be7d4515f9a740cd431e8b0113c0866d266946473a820afa92d5d3131de`  
		Last Modified: Tue, 05 May 2026 23:55:00 GMT  
		Size: 2.3 KB (2290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:975234d05e145a53db6c4eff4ecc7cba6f5d591e304ba4394593cc34caba155f`  
		Last Modified: Wed, 06 May 2026 00:18:36 GMT  
		Size: 1.4 KB (1426 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee75eaf8116d9d407cb20dd7d07620edeebf82834df78fc9aeac7e5c8e3fc811`  
		Last Modified: Wed, 06 May 2026 00:21:24 GMT  
		Size: 53.4 MB (53353708 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f70e4ecb8aa0dc489c314baef9937c5a587640636d236f1a74e719e77f9aa9b0`  
		Last Modified: Wed, 06 May 2026 00:21:26 GMT  
		Size: 137.4 MB (137388274 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45f133b078fdce4f08d76bf6f0674f05a45fdb588cfba3f7f18542d47bc10ccb`  
		Last Modified: Wed, 06 May 2026 00:21:21 GMT  
		Size: 35.0 KB (35011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:8-jdk21-ubi` - unknown; unknown

```console
$ docker pull gradle@sha256:790457efc52f979910bcd419e834e08b390971ad0f5bee913c80fe9a29177f1c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5429155 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c73e143c774d73440a7bc2f95cdb2cced47afe2c476c5a2efcba00d5e12ab7c0`

```dockerfile
```

-	Layers:
	-	`sha256:3142c451c59388a35391976d0418f21262441fb559eaf5509ce6ff5b8bab7c02`  
		Last Modified: Wed, 06 May 2026 00:21:21 GMT  
		Size: 5.4 MB (5405504 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3ab1a26d2df6dbc224c8d12b9bd6e977e0106c9cbecfb1d76a7169bb4bae96d3`  
		Last Modified: Wed, 06 May 2026 00:21:21 GMT  
		Size: 23.7 KB (23651 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:8-jdk21-ubi` - linux; s390x

```console
$ docker pull gradle@sha256:bcb8fe3fa4f0a24a9388400288202284894d359354ede572c710b155a466be7a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **389.4 MB (389370635 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:76f3d42e94dadc3579ee430a90e09b6686b75ec710335da4c9d6ca8098406279`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["gradle"]`

```dockerfile
# Wed, 22 Apr 2026 05:05:14 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 22 Apr 2026 05:05:14 GMT
LABEL vendor="Red Hat, Inc."
# Wed, 22 Apr 2026 05:05:14 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Wed, 22 Apr 2026 05:05:14 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.7"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Wed, 22 Apr 2026 05:05:14 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 22 Apr 2026 05:05:14 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Wed, 22 Apr 2026 05:05:14 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 22 Apr 2026 05:05:14 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 22 Apr 2026 05:05:14 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Wed, 22 Apr 2026 05:05:14 GMT
LABEL io.openshift.expose-services=""
# Wed, 22 Apr 2026 05:05:14 GMT
LABEL io.openshift.tags="minimal rhel9"
# Wed, 22 Apr 2026 05:05:14 GMT
ENV container oci
# Wed, 22 Apr 2026 05:05:14 GMT
COPY dir:c10b61f0eaab474f87333058b5f0be076d9ca7550d40201126b259b146635cf0 in /      
# Wed, 22 Apr 2026 05:05:15 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Wed, 22 Apr 2026 05:05:15 GMT
CMD ["/bin/bash"]
# Wed, 22 Apr 2026 05:05:15 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /usr/share/buildinfo/content-sets.json      
# Wed, 22 Apr 2026 05:05:15 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /root/buildinfo/content_manifests/content-sets.json      
# Wed, 22 Apr 2026 05:05:15 GMT
COPY file:94195acb2e6e678de51e9e05a9e10397a92e2f336a7de1f63b19aacc4230b754 in /usr/share/buildinfo/labels.json      
# Wed, 22 Apr 2026 05:05:15 GMT
COPY file:94195acb2e6e678de51e9e05a9e10397a92e2f336a7de1f63b19aacc4230b754 in /root/buildinfo/labels.json      
# Wed, 22 Apr 2026 05:05:15 GMT
LABEL "architecture"="s390x" "vcs-type"="git" "vcs-ref"="5bb1e5f6eb0dd42dce5d2f21f64a3a9feec995f1" "org.opencontainers.image.revision"="5bb1e5f6eb0dd42dce5d2f21f64a3a9feec995f1" "build-date"="2026-04-22T05:05:02Z" "org.opencontainers.image.created"="2026-04-22T05:05:02Z" "release"="1776833838"org.opencontainers.image.revision=5bb1e5f6eb0dd42dce5d2f21f64a3a9feec995f1,org.opencontainers.image.created=2026-04-22T05:05:02Z
# Wed, 22 Apr 2026 18:16:28 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 22 Apr 2026 18:16:28 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 Apr 2026 18:16:28 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 22 Apr 2026 18:16:28 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en     ;     microdnf clean all # buildkit
# Wed, 22 Apr 2026 18:16:28 GMT
ENV JAVA_VERSION=jdk-21.0.10+7
# Wed, 22 Apr 2026 18:20:59 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='357fee29fb0d5c079f6730db98b28942df13a6eed426f6c61cd4ad703ab27b9a';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.10%2B7/OpenJDK21U-jdk_aarch64_linux_hotspot_21.0.10_7.tar.gz';          ;;        ppc64le)          ESUM='33bdaec351f40cc70d44e251a54c23e4dd15fed8adc041e35c57461c706cf948';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.10%2B7/OpenJDK21U-jdk_ppc64le_linux_hotspot_21.0.10_7.tar.gz';          ;;        s390x)          ESUM='eabb069b59a2e6b9e9926d9c533186aabf1ff3b4af683d0a3620bb7c7d9770c0';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.10%2B7/OpenJDK21U-jdk_s390x_linux_hotspot_21.0.10_7.tar.gz';          ;;        x86_64)          ESUM='ea3b9bd464d6dd253e9a7accf59f7ccd2a36e4aa69640b7251e3370caef896a4';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.10%2B7/OpenJDK21U-jdk_x64_linux_hotspot_21.0.10_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Wed, 22 Apr 2026 18:21:04 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 22 Apr 2026 18:21:07 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 22 Apr 2026 18:21:07 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 22 Apr 2026 18:21:07 GMT
CMD ["jshell"]
# Wed, 22 Apr 2026 19:11:05 GMT
CMD ["gradle"]
# Wed, 22 Apr 2026 19:11:05 GMT
ENV GRADLE_HOME=/opt/gradle
# Wed, 22 Apr 2026 19:11:05 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 101 gradle     && useradd --system --gid gradle --uid 101 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Wed, 22 Apr 2026 19:11:05 GMT
VOLUME [/home/gradle/.gradle]
# Wed, 22 Apr 2026 19:11:09 GMT
WORKDIR /home/gradle
# Wed, 22 Apr 2026 19:21:11 GMT
RUN set -o errexit -o nounset     && microdnf install -y         make                 findutils                 unzip         which                 git         git-lfs         subversion     && microdnf clean all         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which svn # buildkit
# Wed, 22 Apr 2026 19:21:11 GMT
ENV GRADLE_VERSION=8.14.4
# Wed, 22 Apr 2026 19:21:11 GMT
ARG GRADLE_DOWNLOAD_SHA256=f1771298a70f6db5a29daf62378c4e18a17fc33c9ba6b14362e0cdf40610380d
# Wed, 22 Apr 2026 19:21:29 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=f1771298a70f6db5a29daf62378c4e18a17fc33c9ba6b14362e0cdf40610380d
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Wed, 22 Apr 2026 19:21:29 GMT
USER gradle
# Wed, 22 Apr 2026 19:21:37 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=f1771298a70f6db5a29daf62378c4e18a17fc33c9ba6b14362e0cdf40610380d
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Wed, 22 Apr 2026 19:21:37 GMT
USER root
```

-	Layers:
	-	`sha256:aac8159c3d9a48859bb2e3c581e3c2dc900b6a0665fa45fbd980e797d234b4a6`  
		Last Modified: Wed, 22 Apr 2026 06:11:17 GMT  
		Size: 38.1 MB (38131833 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85cefc06fb734705141e3ba7751f638e5dad788e10e5601931ca6ea642ff02df`  
		Last Modified: Wed, 22 Apr 2026 18:17:51 GMT  
		Size: 30.4 MB (30386268 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8208312e7b549452f12d7e84f531585dfbf7ec651a171f02198dd64080735c9`  
		Last Modified: Wed, 22 Apr 2026 18:22:32 GMT  
		Size: 147.1 MB (147104809 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:806ea2ba8b61385fce5b33cd4c5de14bd355deb0e3908ef9f5173046cc707d69`  
		Last Modified: Wed, 22 Apr 2026 18:22:22 GMT  
		Size: 130.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fa09734b6f3a7274b6eefeeee10fb6b7f6bbea490b49b54b534f32afdca7282`  
		Last Modified: Wed, 22 Apr 2026 18:22:23 GMT  
		Size: 2.3 KB (2290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4e792722c3d391e15f5ca525f579d0211be6f5789153e5aa12af8c5269f6552`  
		Last Modified: Wed, 22 Apr 2026 19:16:14 GMT  
		Size: 1.7 KB (1722 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aef5bb4e71b45c0721562b3d4d1eef942e4440f1afc669c4fbcab0be5a226b22`  
		Last Modified: Wed, 22 Apr 2026 19:24:17 GMT  
		Size: 36.3 MB (36320261 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed5c2a6609a66ed8b7718ce543428664c852b5cebe9aa31cc4cc810158ae777f`  
		Last Modified: Wed, 22 Apr 2026 19:24:22 GMT  
		Size: 137.4 MB (137388277 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:118077b90840e87932290ec123a5d7f5988c2faffad1b541aaa8f5815af11833`  
		Last Modified: Wed, 22 Apr 2026 19:24:05 GMT  
		Size: 35.0 KB (35013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:8-jdk21-ubi` - unknown; unknown

```console
$ docker pull gradle@sha256:7ce4a7536b9d451e16c9c617b3405a08890ded27c6d2f5f2ba8d903b9abcb658
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5415973 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7401741cce09ab25513f12d27c862f82d4d1ef55031c256de32d161be6f8d75c`

```dockerfile
```

-	Layers:
	-	`sha256:22aee80f26bfc1442adc44ef5c6b1cde2b0a94f2978e3e7e2029fbe768c04c09`  
		Last Modified: Wed, 22 Apr 2026 19:24:09 GMT  
		Size: 5.4 MB (5392384 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cb1ce32ff0a4022d4385d532f136a428b8058e998e137344d755f73e16633455`  
		Last Modified: Wed, 22 Apr 2026 19:24:03 GMT  
		Size: 23.6 KB (23589 bytes)  
		MIME: application/vnd.in-toto+json
