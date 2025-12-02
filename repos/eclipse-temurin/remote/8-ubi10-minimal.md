## `eclipse-temurin:8-ubi10-minimal`

```console
$ docker pull eclipse-temurin@sha256:dfcdab11fb4e6ff4e4eb77361fb6144c1bb65744917415a1b9b9d40962289884
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `eclipse-temurin:8-ubi10-minimal` - linux; amd64

```console
$ docker pull eclipse-temurin@sha256:5798e93918812dad2d79d0e2c3fefb8b5caa67f133af6ec98dd5379548e38a21
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **144.7 MB (144698496 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d1d256898b05bef153544c041ec0fb8c7903a898443053cafee7bc4536992783`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`

```dockerfile
# Mon, 01 Dec 2025 15:52:04 GMT
LABEL maintainer="Red Hat, Inc."
# Mon, 01 Dec 2025 15:52:04 GMT
LABEL vendor="Red Hat, Inc."
# Mon, 01 Dec 2025 15:52:04 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Mon, 01 Dec 2025 15:52:04 GMT
LABEL com.redhat.component="ubi10-minimal-container"       name="ubi10/ubi-minimal"       version="10.1"       cpe="cpe:/o:redhat:enterprise_linux:10.1"       distribution-scope="public"
# Mon, 01 Dec 2025 15:52:04 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Mon, 01 Dec 2025 15:52:04 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 10."
# Mon, 01 Dec 2025 15:52:04 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 01 Dec 2025 15:52:04 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 01 Dec 2025 15:52:04 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 10 Minimal"
# Mon, 01 Dec 2025 15:52:04 GMT
LABEL io.openshift.expose-services=""
# Mon, 01 Dec 2025 15:52:05 GMT
LABEL io.openshift.tags="minimal rhel10"
# Mon, 01 Dec 2025 15:52:05 GMT
ENV container oci
# Mon, 01 Dec 2025 15:52:05 GMT
COPY dir:e3f52ba99077b3bc7b7921467816c9e1d6afafe638b5c85f61d17a96c866d5a4 in /      
# Mon, 01 Dec 2025 15:52:06 GMT
COPY file:5de33b5fc08b00635bccf9134a18978dba13e2250aa51838f9969515a3957847 in /etc/yum.repos.d/.      
# Mon, 01 Dec 2025 15:52:06 GMT
CMD ["/bin/bash"]
# Mon, 01 Dec 2025 15:52:06 GMT
COPY file:595171150af68abc798ea385f7988d74b566aa8e84babff137f00b08b2164683 in /usr/share/buildinfo/content-sets.json      
# Mon, 01 Dec 2025 15:52:06 GMT
COPY file:595171150af68abc798ea385f7988d74b566aa8e84babff137f00b08b2164683 in /root/buildinfo/content_manifests/content-sets.json      
# Mon, 01 Dec 2025 15:52:06 GMT
COPY file:922399bb1f6dd7741b16f1cdd9842f87612db7b462e38b1bbeae37d5c71e21d7 in /usr/share/buildinfo/labels.json      
# Mon, 01 Dec 2025 15:52:07 GMT
COPY file:922399bb1f6dd7741b16f1cdd9842f87612db7b462e38b1bbeae37d5c71e21d7 in /root/buildinfo/labels.json      
# Mon, 01 Dec 2025 15:52:07 GMT
LABEL "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="f3ce7416a648177fb2c54fd1c28cc0dab0304a68" "org.opencontainers.image.revision"="f3ce7416a648177fb2c54fd1c28cc0dab0304a68" "build-date"="2025-12-01T15:51:47Z" "org.opencontainers.image.created"="2025-12-01T15:51:47Z" "release"="1764604111"org.opencontainers.image.revision=f3ce7416a648177fb2c54fd1c28cc0dab0304a68,org.opencontainers.image.created=2025-12-01T15:51:47Z
# Tue, 02 Dec 2025 00:37:44 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 02 Dec 2025 00:37:44 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Dec 2025 00:37:44 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 02 Dec 2025 00:37:44 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en         gnupg2     ;     microdnf clean all # buildkit
# Tue, 02 Dec 2025 00:37:44 GMT
ENV JAVA_VERSION=jdk8u472-b08
# Tue, 02 Dec 2025 00:37:47 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='e2aff19d85d2441e409d6cbdf12ef7c2acabb0de73bca4207947135dcaa935a2';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u472-b08/OpenJDK8U-jdk_aarch64_linux_hotspot_8u472b08.tar.gz';          ;;        ppc64le)          ESUM='eaf57a4564265583b0641c878bea8943d27ef110c096868f686dae179fb45d8f';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u472-b08/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u472b08.tar.gz';          ;;        x86_64)          ESUM='5becaa4ac660e844c5a39e2ebc39ff5ac824c37ff1b625af8c8b111dc13c3592';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u472-b08/OpenJDK8U-jdk_x64_linux_hotspot_8u472b08.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip; # buildkit
# Tue, 02 Dec 2025 00:37:47 GMT
RUN set -eux;     echo "Verifying install ...";     echo "javac -version"; javac -version;     echo "java -version"; java -version;     echo "Complete." # buildkit
# Tue, 02 Dec 2025 00:37:48 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 02 Dec 2025 00:37:48 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
```

-	Layers:
	-	`sha256:3fe7185a3562260af267162d9816b8c41f88072fc86a6884c33d874ef0a74688`  
		Last Modified: Mon, 01 Dec 2025 18:12:29 GMT  
		Size: 34.6 MB (34621933 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1dfd0be18fe4c33d84edfb20868c6ad1174990231e9a127a60cb06607ff7fab8`  
		Last Modified: Tue, 02 Dec 2025 01:02:53 GMT  
		Size: 55.3 MB (55340248 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c3b21d46d6b81bf2f0ec1d10bcc0e5d907bfc580b58dc081a085ba5db5717d3`  
		Last Modified: Tue, 02 Dec 2025 02:15:18 GMT  
		Size: 54.7 MB (54733872 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb976bbcc9fd8821dbe51ac57e57cacb5b98c22022ae1f198fdea6245ded286a`  
		Last Modified: Tue, 02 Dec 2025 00:48:02 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05ac33895da7afc5296180b6c59fc25bb0405f9592e104aeeea5fb9150a48d19`  
		Last Modified: Tue, 02 Dec 2025 00:48:05 GMT  
		Size: 2.3 KB (2315 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:8-ubi10-minimal` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:72e47f066cdf45fa43b90bcc2b4c5938338adb8f17e08649d97a6c57ca6ee652
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5822153 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a6d03514f01613c8376dd5d8baeef1fad955a0b51b3abf1b70cc4c33d8eaf56e`

```dockerfile
```

-	Layers:
	-	`sha256:2dd3bed84e0ee56b3e6d4a9505c3c1640a5f4317fb18b2856103e494ab6d8081`  
		Last Modified: Tue, 02 Dec 2025 01:18:13 GMT  
		Size: 5.8 MB (5802114 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e7b812a83874eda8e108540872f6efab6aca373c19ad0186a19e84b0abbd52c4`  
		Last Modified: Tue, 02 Dec 2025 01:18:14 GMT  
		Size: 20.0 KB (20039 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-temurin:8-ubi10-minimal` - linux; arm64 variant v8

```console
$ docker pull eclipse-temurin@sha256:4dacbe9d7a59e448f2bd778608d1dca17f408b75f442acb871c95e775cd3414d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **141.6 MB (141558628 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2232f7520a666728f24b8a0dc20dbfca04db685d413a39c2c4b6f7687b40bb53`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`

```dockerfile
# Mon, 01 Dec 2025 16:14:10 GMT
LABEL maintainer="Red Hat, Inc."
# Mon, 01 Dec 2025 16:14:10 GMT
LABEL vendor="Red Hat, Inc."
# Mon, 01 Dec 2025 16:14:10 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Mon, 01 Dec 2025 16:14:10 GMT
LABEL com.redhat.component="ubi10-minimal-container"       name="ubi10/ubi-minimal"       version="10.1"       cpe="cpe:/o:redhat:enterprise_linux:10.1"       distribution-scope="public"
# Mon, 01 Dec 2025 16:14:10 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Mon, 01 Dec 2025 16:14:10 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 10."
# Mon, 01 Dec 2025 16:14:10 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 01 Dec 2025 16:14:10 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 01 Dec 2025 16:14:10 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 10 Minimal"
# Mon, 01 Dec 2025 16:14:10 GMT
LABEL io.openshift.expose-services=""
# Mon, 01 Dec 2025 16:14:10 GMT
LABEL io.openshift.tags="minimal rhel10"
# Mon, 01 Dec 2025 16:14:10 GMT
ENV container oci
# Mon, 01 Dec 2025 16:14:11 GMT
COPY dir:69dd4a0b5ba0f5bf7a4e00ffeb7ef3c8fe0f0bfc2283402327c0309bf841d6fa in /      
# Mon, 01 Dec 2025 16:14:11 GMT
COPY file:5de33b5fc08b00635bccf9134a18978dba13e2250aa51838f9969515a3957847 in /etc/yum.repos.d/.      
# Mon, 01 Dec 2025 16:14:11 GMT
CMD ["/bin/bash"]
# Mon, 01 Dec 2025 16:14:11 GMT
COPY file:595171150af68abc798ea385f7988d74b566aa8e84babff137f00b08b2164683 in /usr/share/buildinfo/content-sets.json      
# Mon, 01 Dec 2025 16:14:11 GMT
COPY file:595171150af68abc798ea385f7988d74b566aa8e84babff137f00b08b2164683 in /root/buildinfo/content_manifests/content-sets.json      
# Mon, 01 Dec 2025 16:14:11 GMT
COPY file:6f341067110dc29b8758b5d271970b09cd64dcb0e30a85b18012a177bb71753e in /usr/share/buildinfo/labels.json      
# Mon, 01 Dec 2025 16:14:11 GMT
COPY file:6f341067110dc29b8758b5d271970b09cd64dcb0e30a85b18012a177bb71753e in /root/buildinfo/labels.json      
# Mon, 01 Dec 2025 16:14:11 GMT
LABEL "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="f3ce7416a648177fb2c54fd1c28cc0dab0304a68" "org.opencontainers.image.revision"="f3ce7416a648177fb2c54fd1c28cc0dab0304a68" "build-date"="2025-12-01T16:13:49Z" "org.opencontainers.image.created"="2025-12-01T16:13:49Z" "release"="1764604111"org.opencontainers.image.revision=f3ce7416a648177fb2c54fd1c28cc0dab0304a68,org.opencontainers.image.created=2025-12-01T16:13:49Z
# Tue, 02 Dec 2025 00:42:46 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 02 Dec 2025 00:42:46 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Dec 2025 00:42:46 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 02 Dec 2025 00:42:46 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en         gnupg2     ;     microdnf clean all # buildkit
# Tue, 02 Dec 2025 00:42:46 GMT
ENV JAVA_VERSION=jdk8u472-b08
# Tue, 02 Dec 2025 00:42:50 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='e2aff19d85d2441e409d6cbdf12ef7c2acabb0de73bca4207947135dcaa935a2';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u472-b08/OpenJDK8U-jdk_aarch64_linux_hotspot_8u472b08.tar.gz';          ;;        ppc64le)          ESUM='eaf57a4564265583b0641c878bea8943d27ef110c096868f686dae179fb45d8f';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u472-b08/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u472b08.tar.gz';          ;;        x86_64)          ESUM='5becaa4ac660e844c5a39e2ebc39ff5ac824c37ff1b625af8c8b111dc13c3592';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u472-b08/OpenJDK8U-jdk_x64_linux_hotspot_8u472b08.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip; # buildkit
# Tue, 02 Dec 2025 00:42:50 GMT
RUN set -eux;     echo "Verifying install ...";     echo "javac -version"; javac -version;     echo "java -version"; java -version;     echo "Complete." # buildkit
# Tue, 02 Dec 2025 00:42:50 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 02 Dec 2025 00:42:50 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
```

-	Layers:
	-	`sha256:9c27140b3e778c26a038c982eb0b0d7c55918358b1c1e3afdb013d53d318ad1f`  
		Last Modified: Mon, 01 Dec 2025 18:12:35 GMT  
		Size: 32.6 MB (32592499 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:272c1596a90b8edab1636e1e07b23392699072b955939a84b61846f1d64bdb40`  
		Last Modified: Tue, 02 Dec 2025 00:43:42 GMT  
		Size: 55.1 MB (55148104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2cd100b99d7c31cee8867016620962b4a5cdde9c51c0fa1e9eff183fee1acf9`  
		Last Modified: Tue, 02 Dec 2025 00:43:46 GMT  
		Size: 53.8 MB (53815583 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:257a888f387f644c480b17d0fdace6629c4c0fba377f7f8e7a668f374d565784`  
		Last Modified: Tue, 02 Dec 2025 00:43:37 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b4e791e2c2ce9c11b2ba53b767568efe20263c6862b6d86565539d39d8cfb50`  
		Last Modified: Tue, 02 Dec 2025 00:43:38 GMT  
		Size: 2.3 KB (2314 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:8-ubi10-minimal` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:6e252cba1c230c74dbd6604da88c4677f1d9e3b03f78862d0a7269a008afafd0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5822456 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cab497183d84fd415f2f8815486e229d1e0b9569db830568548bcd6ef24b58fa`

```dockerfile
```

-	Layers:
	-	`sha256:a62d3065e8731e1668488bf4c637955856f93abee041a05b5f95bf892bfa0d53`  
		Last Modified: Tue, 02 Dec 2025 01:18:20 GMT  
		Size: 5.8 MB (5802302 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:46bdd764120b7dd711a7b74ef1fa342f286e37991c5d9cb51c476b951901db56`  
		Last Modified: Tue, 02 Dec 2025 01:18:20 GMT  
		Size: 20.2 KB (20154 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-temurin:8-ubi10-minimal` - linux; ppc64le

```console
$ docker pull eclipse-temurin@sha256:62a2a3d9f51d9d004680015d73313896ba4d7d102297536f15b0bafca3478ba1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **148.3 MB (148253455 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:01e8b84c42a9c4598a422c57540fa068aa24850b5f54880eb671058454ecbcc1`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`

```dockerfile
# Mon, 17 Nov 2025 07:03:31 GMT
LABEL maintainer="Red Hat, Inc."
# Mon, 17 Nov 2025 07:03:31 GMT
LABEL vendor="Red Hat, Inc."
# Mon, 17 Nov 2025 07:03:31 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Mon, 17 Nov 2025 07:03:31 GMT
LABEL com.redhat.component="ubi10-minimal-container"       name="ubi10/ubi-minimal"       version="10.1"       cpe="cpe:/o:redhat:enterprise_linux:10.1"       distribution-scope="public"
# Mon, 17 Nov 2025 07:03:31 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Mon, 17 Nov 2025 07:03:31 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 10."
# Mon, 17 Nov 2025 07:03:31 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 17 Nov 2025 07:03:31 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 17 Nov 2025 07:03:31 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 10 Minimal"
# Mon, 17 Nov 2025 07:03:31 GMT
LABEL io.openshift.expose-services=""
# Mon, 17 Nov 2025 07:03:31 GMT
LABEL io.openshift.tags="minimal rhel10"
# Mon, 17 Nov 2025 07:03:31 GMT
ENV container oci
# Mon, 17 Nov 2025 07:03:32 GMT
COPY dir:3f836289fcb5e4834914ff52d15c42d6b925906d318eaeb6e7ece83b813f7798 in /      
# Mon, 17 Nov 2025 07:03:32 GMT
COPY file:5de33b5fc08b00635bccf9134a18978dba13e2250aa51838f9969515a3957847 in /etc/yum.repos.d/.      
# Mon, 17 Nov 2025 07:03:32 GMT
CMD ["/bin/bash"]
# Mon, 17 Nov 2025 07:03:32 GMT
COPY file:595171150af68abc798ea385f7988d74b566aa8e84babff137f00b08b2164683 in /usr/share/buildinfo/content-sets.json      
# Mon, 17 Nov 2025 07:03:32 GMT
COPY file:595171150af68abc798ea385f7988d74b566aa8e84babff137f00b08b2164683 in /root/buildinfo/content_manifests/content-sets.json      
# Mon, 17 Nov 2025 07:03:32 GMT
COPY file:040b4789124c20d56e0f81f37d756e271408963b29b2b4b1e2a7e2c073e4ad50 in /usr/share/buildinfo/labels.json      
# Mon, 17 Nov 2025 07:03:32 GMT
COPY file:040b4789124c20d56e0f81f37d756e271408963b29b2b4b1e2a7e2c073e4ad50 in /root/buildinfo/labels.json      
# Mon, 17 Nov 2025 07:03:33 GMT
LABEL "architecture"="ppc64le" "vcs-type"="git" "vcs-ref"="f3ce7416a648177fb2c54fd1c28cc0dab0304a68" "org.opencontainers.image.revision"="f3ce7416a648177fb2c54fd1c28cc0dab0304a68" "build-date"="2025-11-17T07:03:20Z" "release"="1763362715"org.opencontainers.image.revision=f3ce7416a648177fb2c54fd1c28cc0dab0304a68
# Mon, 17 Nov 2025 23:14:49 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 17 Nov 2025 23:14:49 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 17 Nov 2025 23:14:49 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 17 Nov 2025 23:14:49 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en         gnupg2     ;     microdnf clean all # buildkit
# Mon, 17 Nov 2025 23:14:49 GMT
ENV JAVA_VERSION=jdk8u472-b08
# Mon, 17 Nov 2025 23:15:04 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='e2aff19d85d2441e409d6cbdf12ef7c2acabb0de73bca4207947135dcaa935a2';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u472-b08/OpenJDK8U-jdk_aarch64_linux_hotspot_8u472b08.tar.gz';          ;;        ppc64le)          ESUM='eaf57a4564265583b0641c878bea8943d27ef110c096868f686dae179fb45d8f';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u472-b08/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u472b08.tar.gz';          ;;        x86_64)          ESUM='5becaa4ac660e844c5a39e2ebc39ff5ac824c37ff1b625af8c8b111dc13c3592';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u472-b08/OpenJDK8U-jdk_x64_linux_hotspot_8u472b08.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip; # buildkit
# Mon, 17 Nov 2025 23:15:07 GMT
RUN set -eux;     echo "Verifying install ...";     echo "javac -version"; javac -version;     echo "java -version"; java -version;     echo "Complete." # buildkit
# Mon, 17 Nov 2025 23:15:11 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Mon, 17 Nov 2025 23:15:11 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
```

-	Layers:
	-	`sha256:6e24e81139d30a463716e63229e1184a2b4250bb139ff88e3682c9e552661b81`  
		Last Modified: Mon, 17 Nov 2025 12:13:13 GMT  
		Size: 38.7 MB (38721761 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:106e259b55af997c3f2efc1cf8633c914cd06061615b03cbef4967d4541d920a`  
		Last Modified: Mon, 17 Nov 2025 23:16:28 GMT  
		Size: 57.4 MB (57353400 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16c98c25f59b323b4b9b1d817a982443c1f1ac73552b7dce037be4ce51467092`  
		Last Modified: Mon, 17 Nov 2025 23:16:30 GMT  
		Size: 52.2 MB (52175851 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:087db38746d7fe31248758e28d4c5501b5dd6a93d3d4fc580a804aaf37434f97`  
		Last Modified: Mon, 17 Nov 2025 23:15:31 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44eb1f3890e10788f3681e62f9ecd6ef3eab7ddba47e3bc0aee9d094f3c09a94`  
		Last Modified: Mon, 17 Nov 2025 23:16:20 GMT  
		Size: 2.3 KB (2316 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:8-ubi10-minimal` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:c8ae1b5d9625a1c7261d42a527ddc360b1e33dd465390787c5d2b1028c566228
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5809934 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:18bffcc40884215789b9df39957199ccddacca65a9b1f7253ee6379a89a2384c`

```dockerfile
```

-	Layers:
	-	`sha256:b9864a36a4b7f06055401e382c9b2d625ea4f1f36844871a5bfe2b31b964a45e`  
		Last Modified: Tue, 18 Nov 2025 01:19:37 GMT  
		Size: 5.8 MB (5789859 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:14fd4ad5cb70853c24cdf8e404ea7118cada007483df20e3c261a6b7edc786d9`  
		Last Modified: Tue, 18 Nov 2025 01:19:38 GMT  
		Size: 20.1 KB (20075 bytes)  
		MIME: application/vnd.in-toto+json
