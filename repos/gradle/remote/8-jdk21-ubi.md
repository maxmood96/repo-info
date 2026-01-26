## `gradle:8-jdk21-ubi`

```console
$ docker pull gradle@sha256:38882b8d1880b52f47c2c4b30efa03b4a58aa7f2aab3b007573ccf540157459f
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
$ docker pull gradle@sha256:197b24bcb1a03237ed7657db3f4e0946750d7b81377026aa7de7f13ee517a28f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **402.5 MB (402450588 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:da85ed4cc4cc950aa4c6a5c137766f72b5fce8598c9accbd0c4a2042d71ef044`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["gradle"]`

```dockerfile
# Mon, 19 Jan 2026 00:54:03 GMT
LABEL maintainer="Red Hat, Inc."
# Mon, 19 Jan 2026 00:54:03 GMT
LABEL vendor="Red Hat, Inc."
# Mon, 19 Jan 2026 00:54:04 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Mon, 19 Jan 2026 00:54:04 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.7"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Mon, 19 Jan 2026 00:54:04 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Mon, 19 Jan 2026 00:54:04 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Mon, 19 Jan 2026 00:54:04 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 19 Jan 2026 00:54:04 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 19 Jan 2026 00:54:04 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Mon, 19 Jan 2026 00:54:04 GMT
LABEL io.openshift.expose-services=""
# Mon, 19 Jan 2026 00:54:05 GMT
LABEL io.openshift.tags="minimal rhel9"
# Mon, 19 Jan 2026 00:54:05 GMT
ENV container oci
# Mon, 19 Jan 2026 00:54:05 GMT
COPY dir:add769031e8da293a85a3b4d1de9d9caa670962dd1067e1e063336823e094054 in /      
# Mon, 19 Jan 2026 00:54:05 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Mon, 19 Jan 2026 00:54:05 GMT
CMD ["/bin/bash"]
# Mon, 19 Jan 2026 00:54:06 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /usr/share/buildinfo/content-sets.json      
# Mon, 19 Jan 2026 00:54:06 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /root/buildinfo/content_manifests/content-sets.json      
# Mon, 19 Jan 2026 00:54:06 GMT
COPY file:e5cdde1c4ba4b2b156fe95664c6aa883d51ceb58bffc4282d8d097d8b741d55b in /usr/share/buildinfo/labels.json      
# Mon, 19 Jan 2026 00:54:06 GMT
COPY file:e5cdde1c4ba4b2b156fe95664c6aa883d51ceb58bffc4282d8d097d8b741d55b in /root/buildinfo/labels.json      
# Mon, 19 Jan 2026 00:54:06 GMT
LABEL "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="d9151f7dd4dfe1cc8a2df524b85cddd483628d5e" "org.opencontainers.image.revision"="d9151f7dd4dfe1cc8a2df524b85cddd483628d5e" "build-date"="2026-01-19T00:53:42Z" "org.opencontainers.image.created"="2026-01-19T00:53:42Z" "release"="1768783948"org.opencontainers.image.revision=d9151f7dd4dfe1cc8a2df524b85cddd483628d5e,org.opencontainers.image.created=2026-01-19T00:53:42Z
# Tue, 20 Jan 2026 19:15:40 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 20 Jan 2026 19:15:40 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 20 Jan 2026 19:15:40 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 20 Jan 2026 19:15:40 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en     ;     microdnf clean all # buildkit
# Tue, 20 Jan 2026 19:15:40 GMT
ENV JAVA_VERSION=jdk-21.0.9+10
# Tue, 20 Jan 2026 19:15:47 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='edf0da4debe7cf475dbe320d174d6eed81479eb363f41e38a2efb740428c603a';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.9%2B10/OpenJDK21U-jdk_aarch64_linux_hotspot_21.0.9_10.tar.gz';          ;;        ppc64le)          ESUM='ac5a0394a234269b4e20459649ac93cb702cde29b3e46a0bcf3aa53958f2d4a4';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.9%2B10/OpenJDK21U-jdk_ppc64le_linux_hotspot_21.0.9_10.tar.gz';          ;;        s390x)          ESUM='e8ede0fb48aaa3a0cc1ac7c8522f8ca7938bdbb8be0d603b61134de7f898aff4';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.9%2B10/OpenJDK21U-jdk_s390x_linux_hotspot_21.0.9_10.tar.gz';          ;;        x86_64)          ESUM='810d3773df7e0d6c4394e4e244b264c8b30e0b05a0acf542d065fd78a6b65c2f';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.9%2B10/OpenJDK21U-jdk_x64_linux_hotspot_21.0.9_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Tue, 20 Jan 2026 19:15:48 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 20 Jan 2026 19:15:48 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 20 Jan 2026 19:15:48 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 20 Jan 2026 19:15:48 GMT
CMD ["jshell"]
# Mon, 26 Jan 2026 19:18:27 GMT
CMD ["gradle"]
# Mon, 26 Jan 2026 19:18:27 GMT
ENV GRADLE_HOME=/opt/gradle
# Mon, 26 Jan 2026 19:18:27 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 101 gradle     && useradd --system --gid gradle --uid 101 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Mon, 26 Jan 2026 19:18:27 GMT
VOLUME [/home/gradle/.gradle]
# Mon, 26 Jan 2026 19:18:27 GMT
WORKDIR /home/gradle
# Mon, 26 Jan 2026 19:18:31 GMT
RUN set -o errexit -o nounset     && microdnf install -y         make                 findutils                 unzip         which                 git         git-lfs         subversion     && microdnf clean all         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which svn # buildkit
# Mon, 26 Jan 2026 19:18:31 GMT
ENV GRADLE_VERSION=8.14.4
# Mon, 26 Jan 2026 19:18:31 GMT
ARG GRADLE_DOWNLOAD_SHA256=f1771298a70f6db5a29daf62378c4e18a17fc33c9ba6b14362e0cdf40610380d
# Mon, 26 Jan 2026 19:18:34 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=f1771298a70f6db5a29daf62378c4e18a17fc33c9ba6b14362e0cdf40610380d
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Mon, 26 Jan 2026 19:18:34 GMT
USER gradle
# Mon, 26 Jan 2026 19:18:34 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=f1771298a70f6db5a29daf62378c4e18a17fc33c9ba6b14362e0cdf40610380d
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Mon, 26 Jan 2026 19:18:34 GMT
USER root
```

-	Layers:
	-	`sha256:8369c500d2f32a6ea3a82d87ee6ca148febba026765ac200615b9de6130b7805`  
		Last Modified: Mon, 19 Jan 2026 05:33:34 GMT  
		Size: 40.0 MB (40033212 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0112d9cfd44ec26dbcdbd11d04761d724c878cfc02faab2cce0302ece1c34fb6`  
		Last Modified: Tue, 20 Jan 2026 19:16:05 GMT  
		Size: 30.4 MB (30416076 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa08f636bb59bb64c88d8af62f734b82d47994bae8f2c3fa6ae2bc1bb6f33bd5`  
		Last Modified: Tue, 20 Jan 2026 19:16:08 GMT  
		Size: 157.8 MB (157828905 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92780808fb2b5124cdd1d3e8bee1788cddbc400135a7a52c6060e14956278f2d`  
		Last Modified: Tue, 20 Jan 2026 19:16:04 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39791b4c4424bc4792c4f7791a8f4c266ba3f7edaba8605a97bf3b8f882a70b7`  
		Last Modified: Tue, 20 Jan 2026 19:16:04 GMT  
		Size: 2.3 KB (2292 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0988a9d605fdf14928ce1527f72861b67959de0446eda2d32f87a68b5dfbf46b`  
		Last Modified: Mon, 26 Jan 2026 19:18:51 GMT  
		Size: 1.7 KB (1711 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d670caa461e8d292873feb21c28c22cd54c1d887ae04d5654d905f57c4bd97c`  
		Last Modified: Mon, 26 Jan 2026 19:18:53 GMT  
		Size: 36.7 MB (36725058 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:888d80552354ea640f4797b738e613593ce39412e2deb6d795ee9fd0eeb0cbb5`  
		Last Modified: Mon, 26 Jan 2026 19:18:55 GMT  
		Size: 137.4 MB (137388275 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fecad5baeacd2d6a15d148e798cf597417155cc4fb8292d06f6a1775441d7421`  
		Last Modified: Mon, 26 Jan 2026 19:18:51 GMT  
		Size: 54.9 KB (54898 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:8-jdk21-ubi` - unknown; unknown

```console
$ docker pull gradle@sha256:dcc156db57874889055ea5b5276ef119d8d99ee33f22547f643bf049743065db
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5429240 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd32d44d86a919a4294e1e995399cda61b526a7f6e99ab358eb9efddbb1a3b40`

```dockerfile
```

-	Layers:
	-	`sha256:570f0a11a9db107ce750667b937cbbc1052934b52a585c5021595252334e47a2`  
		Last Modified: Mon, 26 Jan 2026 19:18:51 GMT  
		Size: 5.4 MB (5405687 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fdcac3ba479922a4f35d318af67015976905b0958a61e60fcd789dacf5949f88`  
		Last Modified: Mon, 26 Jan 2026 19:18:51 GMT  
		Size: 23.6 KB (23553 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:8-jdk21-ubi` - linux; arm64 variant v8

```console
$ docker pull gradle@sha256:2b1e5d56f8fcc15074605eec8a160e27ad7acbcc176543ec540161d8a7c13f52
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **398.7 MB (398691703 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:453d831bb388f5cdd63f06702cfe3e333eff4b57349929e16695c3d7763ecf36`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["gradle"]`

```dockerfile
# Mon, 19 Jan 2026 00:56:35 GMT
LABEL maintainer="Red Hat, Inc."
# Mon, 19 Jan 2026 00:56:35 GMT
LABEL vendor="Red Hat, Inc."
# Mon, 19 Jan 2026 00:56:35 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Mon, 19 Jan 2026 00:56:35 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.7"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Mon, 19 Jan 2026 00:56:35 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Mon, 19 Jan 2026 00:56:35 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Mon, 19 Jan 2026 00:56:35 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 19 Jan 2026 00:56:35 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 19 Jan 2026 00:56:35 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Mon, 19 Jan 2026 00:56:35 GMT
LABEL io.openshift.expose-services=""
# Mon, 19 Jan 2026 00:56:35 GMT
LABEL io.openshift.tags="minimal rhel9"
# Mon, 19 Jan 2026 00:56:35 GMT
ENV container oci
# Mon, 19 Jan 2026 00:56:36 GMT
COPY dir:d1a1d4e8d07e3fe5bb075a89525931e1e2ca1718af0db53956bd13b04036076a in /      
# Mon, 19 Jan 2026 00:56:36 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Mon, 19 Jan 2026 00:56:36 GMT
CMD ["/bin/bash"]
# Mon, 19 Jan 2026 00:56:36 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /usr/share/buildinfo/content-sets.json      
# Mon, 19 Jan 2026 00:56:36 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /root/buildinfo/content_manifests/content-sets.json      
# Mon, 19 Jan 2026 00:56:36 GMT
COPY file:7445748dd3ef455f458b53843ef5c84a205f42d376fb68389e78914c94988e3c in /usr/share/buildinfo/labels.json      
# Mon, 19 Jan 2026 00:56:36 GMT
COPY file:7445748dd3ef455f458b53843ef5c84a205f42d376fb68389e78914c94988e3c in /root/buildinfo/labels.json      
# Mon, 19 Jan 2026 00:56:36 GMT
LABEL "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="d9151f7dd4dfe1cc8a2df524b85cddd483628d5e" "org.opencontainers.image.revision"="d9151f7dd4dfe1cc8a2df524b85cddd483628d5e" "build-date"="2026-01-19T00:56:19Z" "org.opencontainers.image.created"="2026-01-19T00:56:19Z" "release"="1768783948"org.opencontainers.image.revision=d9151f7dd4dfe1cc8a2df524b85cddd483628d5e,org.opencontainers.image.created=2026-01-19T00:56:19Z
# Tue, 20 Jan 2026 19:15:02 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 20 Jan 2026 19:15:02 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 20 Jan 2026 19:15:02 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 20 Jan 2026 19:15:02 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en     ;     microdnf clean all # buildkit
# Tue, 20 Jan 2026 19:15:02 GMT
ENV JAVA_VERSION=jdk-21.0.9+10
# Tue, 20 Jan 2026 19:15:10 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='edf0da4debe7cf475dbe320d174d6eed81479eb363f41e38a2efb740428c603a';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.9%2B10/OpenJDK21U-jdk_aarch64_linux_hotspot_21.0.9_10.tar.gz';          ;;        ppc64le)          ESUM='ac5a0394a234269b4e20459649ac93cb702cde29b3e46a0bcf3aa53958f2d4a4';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.9%2B10/OpenJDK21U-jdk_ppc64le_linux_hotspot_21.0.9_10.tar.gz';          ;;        s390x)          ESUM='e8ede0fb48aaa3a0cc1ac7c8522f8ca7938bdbb8be0d603b61134de7f898aff4';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.9%2B10/OpenJDK21U-jdk_s390x_linux_hotspot_21.0.9_10.tar.gz';          ;;        x86_64)          ESUM='810d3773df7e0d6c4394e4e244b264c8b30e0b05a0acf542d065fd78a6b65c2f';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.9%2B10/OpenJDK21U-jdk_x64_linux_hotspot_21.0.9_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Tue, 20 Jan 2026 19:15:11 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 20 Jan 2026 19:15:11 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 20 Jan 2026 19:15:11 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 20 Jan 2026 19:15:11 GMT
CMD ["jshell"]
# Mon, 26 Jan 2026 19:18:28 GMT
CMD ["gradle"]
# Mon, 26 Jan 2026 19:18:28 GMT
ENV GRADLE_HOME=/opt/gradle
# Mon, 26 Jan 2026 19:18:28 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 101 gradle     && useradd --system --gid gradle --uid 101 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Mon, 26 Jan 2026 19:18:28 GMT
VOLUME [/home/gradle/.gradle]
# Mon, 26 Jan 2026 19:18:28 GMT
WORKDIR /home/gradle
# Mon, 26 Jan 2026 19:18:34 GMT
RUN set -o errexit -o nounset     && microdnf install -y         make                 findutils                 unzip         which                 git         git-lfs         subversion     && microdnf clean all         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which svn # buildkit
# Mon, 26 Jan 2026 19:18:34 GMT
ENV GRADLE_VERSION=8.14.4
# Mon, 26 Jan 2026 19:18:34 GMT
ARG GRADLE_DOWNLOAD_SHA256=f1771298a70f6db5a29daf62378c4e18a17fc33c9ba6b14362e0cdf40610380d
# Mon, 26 Jan 2026 19:18:36 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=f1771298a70f6db5a29daf62378c4e18a17fc33c9ba6b14362e0cdf40610380d
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Mon, 26 Jan 2026 19:18:36 GMT
USER gradle
# Mon, 26 Jan 2026 19:18:37 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=f1771298a70f6db5a29daf62378c4e18a17fc33c9ba6b14362e0cdf40610380d
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Mon, 26 Jan 2026 19:18:37 GMT
USER root
```

-	Layers:
	-	`sha256:c678760be1bb4697117294f3c0870d24a7c58498b99f14e293dc60361233dcc4`  
		Last Modified: Mon, 19 Jan 2026 05:33:32 GMT  
		Size: 38.2 MB (38208676 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6ef713f7d74f112c431582808345115fc40b2efe9474d13152e63fcc41e6543`  
		Last Modified: Tue, 20 Jan 2026 19:15:30 GMT  
		Size: 30.9 MB (30859031 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f431a935125656428ddd42afd322c4c4402255d38e42ed066f87becf747bce7b`  
		Last Modified: Tue, 20 Jan 2026 19:15:32 GMT  
		Size: 156.1 MB (156111790 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2df4a4f9b76fbbc648a0f9cd91ac81f077e54be6eb820d51eaea83edcbb4fb0`  
		Last Modified: Tue, 20 Jan 2026 19:15:28 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46a1435850681bacab54d6ec7daf579c7426f5498850d72d2edc1514c5b80fe5`  
		Last Modified: Tue, 20 Jan 2026 19:15:17 GMT  
		Size: 2.3 KB (2292 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d926d93f70b2bb28112d58399814d7262f3a925b0974a7dc1541b90de57a686`  
		Last Modified: Mon, 26 Jan 2026 19:18:54 GMT  
		Size: 1.7 KB (1712 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60e74e085e9aa70964b18efc1b7b4d36f463946437f938839a7352d034db428a`  
		Last Modified: Mon, 26 Jan 2026 19:18:55 GMT  
		Size: 36.1 MB (36060218 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad2864474430dabb6a4d3bf6a6eda4e5bcb5a147833fc4468c5d0b9d56711085`  
		Last Modified: Mon, 26 Jan 2026 19:18:58 GMT  
		Size: 137.4 MB (137388273 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75cda8c70ded7798c5ba75ffb6710af0f2d510873a2059ab9c81b005059f695c`  
		Last Modified: Mon, 26 Jan 2026 19:18:54 GMT  
		Size: 59.6 KB (59551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:8-jdk21-ubi` - unknown; unknown

```console
$ docker pull gradle@sha256:05acdff90291369679685d98db9d7e914b67979aa7a3f1aa4e414eb8b9b25e40
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5428819 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7689efcbb5424bd839d96a630ba507034ef0c8e2d1d37b4eb2c4f5c17ecb3d46`

```dockerfile
```

-	Layers:
	-	`sha256:9b0e107c013873412e556959a6ba6227a1922abb94891b9b979ff727723b3aa3`  
		Last Modified: Mon, 26 Jan 2026 19:18:54 GMT  
		Size: 5.4 MB (5405093 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:587394b7b833a00a1a749147a3c264fde1d58839fe4675cad3b1b137b4a8ff6b`  
		Last Modified: Mon, 26 Jan 2026 19:18:54 GMT  
		Size: 23.7 KB (23726 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:8-jdk21-ubi` - linux; ppc64le

```console
$ docker pull gradle@sha256:ccac6e8ce2ad81892150b01b729377a44697d8c282896c73dbfdb4867145c2eb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **410.7 MB (410689285 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6af9b10fcb534cad184e076b4a4b15050566ed5fc1903f1d3ab35cc9a8812586`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["gradle"]`

```dockerfile
# Mon, 19 Jan 2026 01:08:41 GMT
LABEL maintainer="Red Hat, Inc."
# Mon, 19 Jan 2026 01:08:41 GMT
LABEL vendor="Red Hat, Inc."
# Mon, 19 Jan 2026 01:08:41 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Mon, 19 Jan 2026 01:08:41 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.7"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Mon, 19 Jan 2026 01:08:41 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Mon, 19 Jan 2026 01:08:41 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Mon, 19 Jan 2026 01:08:41 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 19 Jan 2026 01:08:41 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 19 Jan 2026 01:08:41 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Mon, 19 Jan 2026 01:08:41 GMT
LABEL io.openshift.expose-services=""
# Mon, 19 Jan 2026 01:08:41 GMT
LABEL io.openshift.tags="minimal rhel9"
# Mon, 19 Jan 2026 01:08:41 GMT
ENV container oci
# Mon, 19 Jan 2026 01:08:42 GMT
COPY dir:3bd7ec6f425d769a16814adff3b957a15c4cbdec659c93cd45b1a546561564a3 in /      
# Mon, 19 Jan 2026 01:08:42 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Mon, 19 Jan 2026 01:08:42 GMT
CMD ["/bin/bash"]
# Mon, 19 Jan 2026 01:08:42 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /usr/share/buildinfo/content-sets.json      
# Mon, 19 Jan 2026 01:08:42 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /root/buildinfo/content_manifests/content-sets.json      
# Mon, 19 Jan 2026 01:08:42 GMT
COPY file:fe8dfccf0fa987a5d4946f1b72ab0cc09a6e656396d24bdd16b87ea3307e9302 in /usr/share/buildinfo/labels.json      
# Mon, 19 Jan 2026 01:08:42 GMT
COPY file:fe8dfccf0fa987a5d4946f1b72ab0cc09a6e656396d24bdd16b87ea3307e9302 in /root/buildinfo/labels.json      
# Mon, 19 Jan 2026 01:08:43 GMT
LABEL "architecture"="ppc64le" "vcs-type"="git" "vcs-ref"="d9151f7dd4dfe1cc8a2df524b85cddd483628d5e" "org.opencontainers.image.revision"="d9151f7dd4dfe1cc8a2df524b85cddd483628d5e" "build-date"="2026-01-19T01:08:31Z" "org.opencontainers.image.created"="2026-01-19T01:08:31Z" "release"="1768783948"org.opencontainers.image.revision=d9151f7dd4dfe1cc8a2df524b85cddd483628d5e,org.opencontainers.image.created=2026-01-19T01:08:31Z
# Tue, 20 Jan 2026 19:12:37 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 20 Jan 2026 19:12:37 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 20 Jan 2026 19:12:37 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 20 Jan 2026 19:12:37 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en     ;     microdnf clean all # buildkit
# Tue, 20 Jan 2026 19:12:37 GMT
ENV JAVA_VERSION=jdk-21.0.9+10
# Tue, 20 Jan 2026 19:17:25 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='edf0da4debe7cf475dbe320d174d6eed81479eb363f41e38a2efb740428c603a';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.9%2B10/OpenJDK21U-jdk_aarch64_linux_hotspot_21.0.9_10.tar.gz';          ;;        ppc64le)          ESUM='ac5a0394a234269b4e20459649ac93cb702cde29b3e46a0bcf3aa53958f2d4a4';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.9%2B10/OpenJDK21U-jdk_ppc64le_linux_hotspot_21.0.9_10.tar.gz';          ;;        s390x)          ESUM='e8ede0fb48aaa3a0cc1ac7c8522f8ca7938bdbb8be0d603b61134de7f898aff4';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.9%2B10/OpenJDK21U-jdk_s390x_linux_hotspot_21.0.9_10.tar.gz';          ;;        x86_64)          ESUM='810d3773df7e0d6c4394e4e244b264c8b30e0b05a0acf542d065fd78a6b65c2f';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.9%2B10/OpenJDK21U-jdk_x64_linux_hotspot_21.0.9_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Tue, 20 Jan 2026 19:17:28 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 20 Jan 2026 19:17:29 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 20 Jan 2026 19:17:29 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 20 Jan 2026 19:17:29 GMT
CMD ["jshell"]
# Mon, 26 Jan 2026 19:17:50 GMT
CMD ["gradle"]
# Mon, 26 Jan 2026 19:17:50 GMT
ENV GRADLE_HOME=/opt/gradle
# Mon, 26 Jan 2026 19:17:50 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 101 gradle     && useradd --system --gid gradle --uid 101 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Mon, 26 Jan 2026 19:17:50 GMT
VOLUME [/home/gradle/.gradle]
# Mon, 26 Jan 2026 19:17:50 GMT
WORKDIR /home/gradle
# Mon, 26 Jan 2026 19:18:24 GMT
RUN set -o errexit -o nounset     && microdnf install -y         make                 findutils                 unzip         which                 git         git-lfs         subversion     && microdnf clean all         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which svn # buildkit
# Mon, 26 Jan 2026 19:18:24 GMT
ENV GRADLE_VERSION=8.14.4
# Mon, 26 Jan 2026 19:18:24 GMT
ARG GRADLE_DOWNLOAD_SHA256=f1771298a70f6db5a29daf62378c4e18a17fc33c9ba6b14362e0cdf40610380d
# Mon, 26 Jan 2026 19:18:29 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=f1771298a70f6db5a29daf62378c4e18a17fc33c9ba6b14362e0cdf40610380d
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Mon, 26 Jan 2026 19:18:29 GMT
USER gradle
# Mon, 26 Jan 2026 19:18:31 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=f1771298a70f6db5a29daf62378c4e18a17fc33c9ba6b14362e0cdf40610380d
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Mon, 26 Jan 2026 19:18:31 GMT
USER root
```

-	Layers:
	-	`sha256:cb3df95d99fa30c8131b824671f0e15d0c34235a2e7bda21e4a361d100760346`  
		Last Modified: Mon, 19 Jan 2026 06:13:36 GMT  
		Size: 44.5 MB (44459713 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5c7d8e1a879073a2bb5883fd40b014f62a8e14ba675ff25067ab8b020299f7b`  
		Last Modified: Tue, 20 Jan 2026 19:13:32 GMT  
		Size: 32.9 MB (32898320 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1552038862d549c75d2a7cd8285b5cd3055837aa0d8b64c9174c0162eff80961`  
		Last Modified: Tue, 20 Jan 2026 19:18:21 GMT  
		Size: 157.9 MB (157943440 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7ecf4c47a37bfd970c6e2631c98b4e5aea4064b8fb545cf4b64702ce80524b4`  
		Last Modified: Tue, 20 Jan 2026 19:18:16 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5b4a35c9f4b8d306e00e1d1c746c41458cb76254ad1c1ddd342e87ec9fb78ff`  
		Last Modified: Tue, 20 Jan 2026 19:18:17 GMT  
		Size: 2.3 KB (2291 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c08886c047d8fd77aa99a2084151011431caf345936c63b88b129aba98a7a69`  
		Last Modified: Mon, 26 Jan 2026 19:19:10 GMT  
		Size: 1.7 KB (1715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f46e71ed9f200c979905a9a7bf5b6b7cd8ee385bca1d650d996ed9b38a02920`  
		Last Modified: Mon, 26 Jan 2026 19:19:12 GMT  
		Size: 38.0 MB (37960367 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40228ad7a509b99a2b70427b4ed0eacd1145086418694dad80d3aec520d2901b`  
		Last Modified: Mon, 26 Jan 2026 19:19:15 GMT  
		Size: 137.4 MB (137388275 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46224a0f301c9a7b5b642b00a24489940f5d251b91e9a087c0197205c619a1de`  
		Last Modified: Mon, 26 Jan 2026 19:19:10 GMT  
		Size: 35.0 KB (35004 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:8-jdk21-ubi` - unknown; unknown

```console
$ docker pull gradle@sha256:95c0c2ed6ce7aa9eb4207a7080ea8b4d7497cd025a5b5fdd33bc3fe64e29e7da
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5426661 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:18efc75a698988a8a6405fc9e6e95b815cbeec70a850ebb1719b2fcdafa5c4c4`

```dockerfile
```

-	Layers:
	-	`sha256:330b5cc59e78bb39fad72a505414d60533d5500289ff370001c4ed93b63c3f17`  
		Last Modified: Mon, 26 Jan 2026 19:19:10 GMT  
		Size: 5.4 MB (5403010 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2565498b87c77ccd94964f1b5e6c96e6490688ac49d86b8c40c0bd6343979533`  
		Last Modified: Mon, 26 Jan 2026 19:19:09 GMT  
		Size: 23.7 KB (23651 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:8-jdk21-ubi` - linux; s390x

```console
$ docker pull gradle@sha256:9edd7b08bf9dc7ff04a10efb3b04518428e3f60fca61682797b260af8702a94e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **389.4 MB (389417164 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:25d6d55d6e4489aea705b658211573e5383466b1348256c1e9a2f1ff3920a431`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["gradle"]`

```dockerfile
# Mon, 19 Jan 2026 00:56:30 GMT
LABEL maintainer="Red Hat, Inc."
# Mon, 19 Jan 2026 00:56:34 GMT
LABEL vendor="Red Hat, Inc."
# Mon, 19 Jan 2026 00:56:38 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Mon, 19 Jan 2026 00:56:44 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.7"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Mon, 19 Jan 2026 00:56:51 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Mon, 19 Jan 2026 00:56:54 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Mon, 19 Jan 2026 00:56:59 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 19 Jan 2026 00:57:03 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 19 Jan 2026 00:57:08 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Mon, 19 Jan 2026 00:57:08 GMT
LABEL io.openshift.expose-services=""
# Mon, 19 Jan 2026 00:57:08 GMT
LABEL io.openshift.tags="minimal rhel9"
# Mon, 19 Jan 2026 00:57:08 GMT
ENV container oci
# Mon, 19 Jan 2026 00:57:08 GMT
COPY dir:60e8b920663668133ad1c0beb8ddee0ed0404da0ad2cb12d0bdf023f3692297c in /      
# Mon, 19 Jan 2026 00:57:08 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Mon, 19 Jan 2026 00:57:08 GMT
CMD ["/bin/bash"]
# Mon, 19 Jan 2026 00:57:09 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /usr/share/buildinfo/content-sets.json      
# Mon, 19 Jan 2026 00:57:09 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /root/buildinfo/content_manifests/content-sets.json      
# Mon, 19 Jan 2026 00:57:09 GMT
COPY file:3606e23b291d122a467fe42706adc9bb412f4262f39a03046011b69272713a85 in /usr/share/buildinfo/labels.json      
# Mon, 19 Jan 2026 00:57:09 GMT
COPY file:3606e23b291d122a467fe42706adc9bb412f4262f39a03046011b69272713a85 in /root/buildinfo/labels.json      
# Mon, 19 Jan 2026 00:57:09 GMT
LABEL "architecture"="s390x" "vcs-type"="git" "vcs-ref"="d9151f7dd4dfe1cc8a2df524b85cddd483628d5e" "org.opencontainers.image.revision"="d9151f7dd4dfe1cc8a2df524b85cddd483628d5e" "build-date"="2026-01-19T00:56:09Z" "org.opencontainers.image.created"="2026-01-19T00:56:09Z" "release"="1768783948"org.opencontainers.image.revision=d9151f7dd4dfe1cc8a2df524b85cddd483628d5e,org.opencontainers.image.created=2026-01-19T00:56:09Z
# Tue, 20 Jan 2026 19:11:50 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 20 Jan 2026 19:11:50 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 20 Jan 2026 19:11:50 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 20 Jan 2026 19:11:50 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en     ;     microdnf clean all # buildkit
# Tue, 20 Jan 2026 19:11:50 GMT
ENV JAVA_VERSION=jdk-21.0.9+10
# Tue, 20 Jan 2026 19:12:39 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='edf0da4debe7cf475dbe320d174d6eed81479eb363f41e38a2efb740428c603a';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.9%2B10/OpenJDK21U-jdk_aarch64_linux_hotspot_21.0.9_10.tar.gz';          ;;        ppc64le)          ESUM='ac5a0394a234269b4e20459649ac93cb702cde29b3e46a0bcf3aa53958f2d4a4';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.9%2B10/OpenJDK21U-jdk_ppc64le_linux_hotspot_21.0.9_10.tar.gz';          ;;        s390x)          ESUM='e8ede0fb48aaa3a0cc1ac7c8522f8ca7938bdbb8be0d603b61134de7f898aff4';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.9%2B10/OpenJDK21U-jdk_s390x_linux_hotspot_21.0.9_10.tar.gz';          ;;        x86_64)          ESUM='810d3773df7e0d6c4394e4e244b264c8b30e0b05a0acf542d065fd78a6b65c2f';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.9%2B10/OpenJDK21U-jdk_x64_linux_hotspot_21.0.9_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Tue, 20 Jan 2026 19:12:41 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 20 Jan 2026 19:12:41 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 20 Jan 2026 19:12:41 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 20 Jan 2026 19:12:41 GMT
CMD ["jshell"]
# Tue, 20 Jan 2026 21:09:59 GMT
CMD ["gradle"]
# Tue, 20 Jan 2026 21:09:59 GMT
ENV GRADLE_HOME=/opt/gradle
# Tue, 20 Jan 2026 21:09:59 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 101 gradle     && useradd --system --gid gradle --uid 101 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Tue, 20 Jan 2026 21:09:59 GMT
VOLUME [/home/gradle/.gradle]
# Tue, 20 Jan 2026 21:09:59 GMT
WORKDIR /home/gradle
# Tue, 20 Jan 2026 21:10:05 GMT
RUN set -o errexit -o nounset     && microdnf install -y         make                 findutils                 unzip         which                 git         git-lfs         subversion     && microdnf clean all         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which svn # buildkit
# Tue, 20 Jan 2026 21:10:05 GMT
ENV GRADLE_VERSION=8.14.4
# Tue, 20 Jan 2026 21:10:05 GMT
ARG GRADLE_DOWNLOAD_SHA256=f1771298a70f6db5a29daf62378c4e18a17fc33c9ba6b14362e0cdf40610380d
# Mon, 26 Jan 2026 19:16:17 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=f1771298a70f6db5a29daf62378c4e18a17fc33c9ba6b14362e0cdf40610380d
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Mon, 26 Jan 2026 19:16:17 GMT
USER gradle
# Mon, 26 Jan 2026 19:16:18 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=f1771298a70f6db5a29daf62378c4e18a17fc33c9ba6b14362e0cdf40610380d
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Mon, 26 Jan 2026 19:16:18 GMT
USER root
```

-	Layers:
	-	`sha256:8d0fd9f50ed7506edfb499eb958eedd9d04f1fe7d6ebb11e4c454c579c856a27`  
		Last Modified: Mon, 19 Jan 2026 06:13:30 GMT  
		Size: 38.1 MB (38120160 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53c1899ea409ad5dc72be7103ffc18eadcabc3eed0be0dc073945f83328d91a3`  
		Last Modified: Tue, 20 Jan 2026 19:12:12 GMT  
		Size: 30.5 MB (30452733 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7590ded7dab81f7181b672816012cab43513ee2db14521513f4dc4fded04ad38`  
		Last Modified: Tue, 20 Jan 2026 19:13:08 GMT  
		Size: 147.1 MB (147068448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1eb723733d2dd099502b71851e962096c129d253d32db134bc41d598ecc4a0c7`  
		Last Modified: Tue, 20 Jan 2026 19:13:04 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f768e86aaf47bb1f61b35e65d0c5fdcff9e40cd92c4ed631757d64996681a92`  
		Last Modified: Tue, 20 Jan 2026 19:13:04 GMT  
		Size: 2.3 KB (2291 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:453cefb3cd755f0201b02d44889ce198ff8fec947ba766d39f96c83ea1278e45`  
		Last Modified: Tue, 20 Jan 2026 21:10:36 GMT  
		Size: 1.7 KB (1709 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c013d87b58d6db46b3443dc9fd80ded2ef64d6638096c3c280d1a9e19f10930`  
		Last Modified: Tue, 20 Jan 2026 21:10:40 GMT  
		Size: 36.3 MB (36348367 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa299e531b3833b387df6f3b82a49f0854b6506edfde9a5062c1c4d7f146e7f9`  
		Last Modified: Mon, 26 Jan 2026 19:16:51 GMT  
		Size: 137.4 MB (137388281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15b254a58b87a2555158afc0797386ba821e07d2c99267b7f5f2042d4dabf37b`  
		Last Modified: Mon, 26 Jan 2026 19:16:47 GMT  
		Size: 35.0 KB (35014 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:8-jdk21-ubi` - unknown; unknown

```console
$ docker pull gradle@sha256:610d882c7a79ca462a3f83ddf7edc430e7d33c94048cf776061d3b809fb8f0c8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5415880 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9cf2d0691b40f612f10aed7772f7b943ef57706d7f2f7db95165fbe73ce9b006`

```dockerfile
```

-	Layers:
	-	`sha256:324401eabc7c75131d5c44cc79235c4736362e84459432338e51d8c654c8c20a`  
		Last Modified: Mon, 26 Jan 2026 19:16:47 GMT  
		Size: 5.4 MB (5392292 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7c81ca12ff21489f58f949028f2a5d72c27ebaac1e6e60d0c7d644598c92579b`  
		Last Modified: Mon, 26 Jan 2026 19:16:47 GMT  
		Size: 23.6 KB (23588 bytes)  
		MIME: application/vnd.in-toto+json
