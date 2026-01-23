## `eclipse-temurin:17-ubi10-minimal`

```console
$ docker pull eclipse-temurin@sha256:cac0d78031dcacdff815694de6fcf9707b0461e996ab88b61e13234135c6b4b2
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

### `eclipse-temurin:17-ubi10-minimal` - linux; amd64

```console
$ docker pull eclipse-temurin@sha256:7bd993a6aae6d390eaf428ddeef0ad6d882ecdc5451aac425dd2b42c3deb12e6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **216.8 MB (216755706 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:316622eda091413df3091f0701832846a693cfd8dbe9b9a0c39fa3311fc9fb1b`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 22 Jan 2026 14:19:49 GMT
LABEL maintainer="Red Hat, Inc."
# Thu, 22 Jan 2026 14:19:49 GMT
LABEL vendor="Red Hat, Inc."
# Thu, 22 Jan 2026 14:19:49 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Thu, 22 Jan 2026 14:19:49 GMT
LABEL com.redhat.component="ubi10-minimal-container"       name="ubi10/ubi-minimal"       version="10.1"       cpe="cpe:/o:redhat:enterprise_linux:10.1"       distribution-scope="public"
# Thu, 22 Jan 2026 14:19:49 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Thu, 22 Jan 2026 14:19:49 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 10."
# Thu, 22 Jan 2026 14:19:49 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 22 Jan 2026 14:19:49 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 22 Jan 2026 14:19:49 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 10 Minimal"
# Thu, 22 Jan 2026 14:19:49 GMT
LABEL io.openshift.expose-services=""
# Thu, 22 Jan 2026 14:19:49 GMT
LABEL io.openshift.tags="minimal rhel10"
# Thu, 22 Jan 2026 14:19:49 GMT
ENV container oci
# Thu, 22 Jan 2026 14:19:50 GMT
COPY dir:4f39f7f54b1623f2373491e5bcb10b3c35efaa04126f246c1c0ae784bb3d7f42 in /      
# Thu, 22 Jan 2026 14:19:50 GMT
COPY file:5de33b5fc08b00635bccf9134a18978dba13e2250aa51838f9969515a3957847 in /etc/yum.repos.d/.      
# Thu, 22 Jan 2026 14:19:50 GMT
CMD ["/bin/bash"]
# Thu, 22 Jan 2026 14:19:50 GMT
COPY file:595171150af68abc798ea385f7988d74b566aa8e84babff137f00b08b2164683 in /usr/share/buildinfo/content-sets.json      
# Thu, 22 Jan 2026 14:19:50 GMT
COPY file:595171150af68abc798ea385f7988d74b566aa8e84babff137f00b08b2164683 in /root/buildinfo/content_manifests/content-sets.json      
# Thu, 22 Jan 2026 14:19:50 GMT
COPY file:e86693423cdd34ed7ac6eb4c5f916f086a37eeca572019e4cfd639c87f98a6ae in /usr/share/buildinfo/labels.json      
# Thu, 22 Jan 2026 14:19:50 GMT
COPY file:e86693423cdd34ed7ac6eb4c5f916f086a37eeca572019e4cfd639c87f98a6ae in /root/buildinfo/labels.json      
# Thu, 22 Jan 2026 14:19:51 GMT
LABEL "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="0912ab420a80f21132d8a5e29d19a23339176677" "org.opencontainers.image.revision"="0912ab420a80f21132d8a5e29d19a23339176677" "build-date"="2026-01-22T14:19:22Z" "org.opencontainers.image.created"="2026-01-22T14:19:22Z" "release"="1769090502"org.opencontainers.image.revision=0912ab420a80f21132d8a5e29d19a23339176677,org.opencontainers.image.created=2026-01-22T14:19:22Z
# Fri, 23 Jan 2026 00:59:59 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 23 Jan 2026 00:59:59 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 23 Jan 2026 00:59:59 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 23 Jan 2026 00:59:59 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en         gnupg2     ;     microdnf clean all # buildkit
# Fri, 23 Jan 2026 00:59:59 GMT
ENV JAVA_VERSION=jdk-17.0.17+10
# Fri, 23 Jan 2026 01:00:54 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='dc29ca6d35beb4419b4b00419b8a3dfbf5ae551e1ae2b046b516d9a579d04533';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jdk_aarch64_linux_hotspot_17.0.17_10.tar.gz';          ;;        ppc64le)          ESUM='2a29d1be61940c1bd639018c07f4622e1f145a7ef34e7294fee877e39226d9da';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jdk_ppc64le_linux_hotspot_17.0.17_10.tar.gz';          ;;        s390x)          ESUM='76327b1d00c67f6be91717754fd85fc85ce496d48876f69accb9c53ed31dc546';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jdk_s390x_linux_hotspot_17.0.17_10.tar.gz';          ;;        x86_64)          ESUM='992f96e7995075ac7636bb1a8de52b0c61d71ed3137fafc979ab96b4ab78dd75';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jdk_x64_linux_hotspot_17.0.17_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Fri, 23 Jan 2026 01:00:55 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Fri, 23 Jan 2026 01:00:55 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Fri, 23 Jan 2026 01:00:55 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Fri, 23 Jan 2026 01:00:55 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:0d4f698c23e56c30d1371a123d48250f3a8dd3de24cc53c15e862c4210c331c2`  
		Last Modified: Thu, 22 Jan 2026 16:13:48 GMT  
		Size: 34.5 MB (34531934 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e058e1cc867cf3feee7d101285b4bc634490d6809fa9fb43631dc7ab3dc368f`  
		Last Modified: Fri, 23 Jan 2026 01:00:16 GMT  
		Size: 37.4 MB (37368491 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b56691cf59dd228c7afdcdb4630f367379d486e15b94ed7ab18e853097dd891`  
		Last Modified: Fri, 23 Jan 2026 01:01:13 GMT  
		Size: 144.9 MB (144852860 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a50e9e63c339bb30bc24d3c720a3e5520942452c4b45287092e08e2ae2363efd`  
		Last Modified: Fri, 23 Jan 2026 01:01:10 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84c033db1e4627e0a9a65a0683b2079cf75a1591a917cbc3738c311f355f8180`  
		Last Modified: Fri, 23 Jan 2026 01:01:10 GMT  
		Size: 2.3 KB (2292 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:17-ubi10-minimal` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:6efab03ae9bc543429a0d478482efa1d79e0cf66b4739ca39cb029ae959f1c99
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3809797 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c8c5d8cbfb54a1a11e947729e2f949ca86236735ac6c8498b3a46a796db8fddf`

```dockerfile
```

-	Layers:
	-	`sha256:fbb9947b4a1b4481e2bf5b22ab85654675cfa5ba4da80e711100570e03e481a5`  
		Last Modified: Fri, 23 Jan 2026 01:01:10 GMT  
		Size: 3.8 MB (3788457 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2668846c30021953e99006236c289593e06e9c21b3b15f6cd7a2d93184a8b239`  
		Last Modified: Fri, 23 Jan 2026 01:01:10 GMT  
		Size: 21.3 KB (21340 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-temurin:17-ubi10-minimal` - linux; arm64 variant v8

```console
$ docker pull eclipse-temurin@sha256:ffbf90e78769ee889cf4b2b9992c7e1f919976d4272c92fa7499d9a2227ffe89
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **213.6 MB (213617086 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b617c66b8c6d1ea5fbb800f20cb2ee9d744c531a5e4d59947e88582f11d142a`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 22 Jan 2026 14:10:51 GMT
LABEL maintainer="Red Hat, Inc."
# Thu, 22 Jan 2026 14:10:51 GMT
LABEL vendor="Red Hat, Inc."
# Thu, 22 Jan 2026 14:10:51 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Thu, 22 Jan 2026 14:10:51 GMT
LABEL com.redhat.component="ubi10-minimal-container"       name="ubi10/ubi-minimal"       version="10.1"       cpe="cpe:/o:redhat:enterprise_linux:10.1"       distribution-scope="public"
# Thu, 22 Jan 2026 14:10:51 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Thu, 22 Jan 2026 14:10:51 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 10."
# Thu, 22 Jan 2026 14:10:51 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 22 Jan 2026 14:10:51 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 22 Jan 2026 14:10:51 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 10 Minimal"
# Thu, 22 Jan 2026 14:10:51 GMT
LABEL io.openshift.expose-services=""
# Thu, 22 Jan 2026 14:10:51 GMT
LABEL io.openshift.tags="minimal rhel10"
# Thu, 22 Jan 2026 14:10:51 GMT
ENV container oci
# Thu, 22 Jan 2026 14:10:52 GMT
COPY dir:909d569786ad4226e9c77ee4fc4d27953d579517f60f8a0f25e4d85964a100a3 in /      
# Thu, 22 Jan 2026 14:10:52 GMT
COPY file:5de33b5fc08b00635bccf9134a18978dba13e2250aa51838f9969515a3957847 in /etc/yum.repos.d/.      
# Thu, 22 Jan 2026 14:10:52 GMT
CMD ["/bin/bash"]
# Thu, 22 Jan 2026 14:10:52 GMT
COPY file:595171150af68abc798ea385f7988d74b566aa8e84babff137f00b08b2164683 in /usr/share/buildinfo/content-sets.json      
# Thu, 22 Jan 2026 14:10:52 GMT
COPY file:595171150af68abc798ea385f7988d74b566aa8e84babff137f00b08b2164683 in /root/buildinfo/content_manifests/content-sets.json      
# Thu, 22 Jan 2026 14:10:52 GMT
COPY file:ea81599b2ebb991911687a996e9dca425fe171d768273735cf8dd2c299ff0d3d in /usr/share/buildinfo/labels.json      
# Thu, 22 Jan 2026 14:10:52 GMT
COPY file:ea81599b2ebb991911687a996e9dca425fe171d768273735cf8dd2c299ff0d3d in /root/buildinfo/labels.json      
# Thu, 22 Jan 2026 14:10:52 GMT
LABEL "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="0912ab420a80f21132d8a5e29d19a23339176677" "org.opencontainers.image.revision"="0912ab420a80f21132d8a5e29d19a23339176677" "build-date"="2026-01-22T14:10:29Z" "org.opencontainers.image.created"="2026-01-22T14:10:29Z" "release"="1769090502"org.opencontainers.image.revision=0912ab420a80f21132d8a5e29d19a23339176677,org.opencontainers.image.created=2026-01-22T14:10:29Z
# Fri, 23 Jan 2026 00:58:23 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 23 Jan 2026 00:58:23 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 23 Jan 2026 00:58:23 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 23 Jan 2026 00:58:23 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en         gnupg2     ;     microdnf clean all # buildkit
# Fri, 23 Jan 2026 00:58:23 GMT
ENV JAVA_VERSION=jdk-17.0.17+10
# Fri, 23 Jan 2026 00:59:21 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='dc29ca6d35beb4419b4b00419b8a3dfbf5ae551e1ae2b046b516d9a579d04533';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jdk_aarch64_linux_hotspot_17.0.17_10.tar.gz';          ;;        ppc64le)          ESUM='2a29d1be61940c1bd639018c07f4622e1f145a7ef34e7294fee877e39226d9da';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jdk_ppc64le_linux_hotspot_17.0.17_10.tar.gz';          ;;        s390x)          ESUM='76327b1d00c67f6be91717754fd85fc85ce496d48876f69accb9c53ed31dc546';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jdk_s390x_linux_hotspot_17.0.17_10.tar.gz';          ;;        x86_64)          ESUM='992f96e7995075ac7636bb1a8de52b0c61d71ed3137fafc979ab96b4ab78dd75';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jdk_x64_linux_hotspot_17.0.17_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Fri, 23 Jan 2026 00:59:23 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Fri, 23 Jan 2026 00:59:23 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Fri, 23 Jan 2026 00:59:23 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Fri, 23 Jan 2026 00:59:23 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:855d6cc175ead513a1945d3f0933680ee64146fa0bb48e8f15fcefa1fe9b0b14`  
		Last Modified: Thu, 22 Jan 2026 17:36:15 GMT  
		Size: 32.6 MB (32613686 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ac781c132d75e81cb50967739184f7c1157b403228369c655282bb8643ac784`  
		Last Modified: Fri, 23 Jan 2026 00:58:43 GMT  
		Size: 37.3 MB (37315606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6efd3a4d2b9fdb4bf6f18a10fc082168f050e04ca0844b2e9c9b67de5d0cdba6`  
		Last Modified: Fri, 23 Jan 2026 00:59:43 GMT  
		Size: 143.7 MB (143685375 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6351df77e6a723f16d7cc7941c40cf8da0f16203d0facec77e6de8a3b27ebd1f`  
		Last Modified: Fri, 23 Jan 2026 00:59:40 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7609f5821a18741fde08ee901689dceeebd634640ffee6d4f224164452f79e97`  
		Last Modified: Fri, 23 Jan 2026 00:59:40 GMT  
		Size: 2.3 KB (2292 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:17-ubi10-minimal` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:7f24fa14c454bf6d1502ef882e9f25d149da2cc90f85b0d60d3f09db68b4947d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3809339 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb721a560ace6af37e24d15ff110c650860258816340c521d1b0ee7b23ac7429`

```dockerfile
```

-	Layers:
	-	`sha256:6f92707c39cc550dcdd66ec433af8c5f58e7177c6fcd9f17942dc006f0ee8929`  
		Last Modified: Fri, 23 Jan 2026 00:59:40 GMT  
		Size: 3.8 MB (3787883 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2a45fd10e4394e13c16081d9a8993ed6ce45218de738db76c5ee5958eeec9e2a`  
		Last Modified: Fri, 23 Jan 2026 00:59:40 GMT  
		Size: 21.5 KB (21456 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-temurin:17-ubi10-minimal` - linux; ppc64le

```console
$ docker pull eclipse-temurin@sha256:8132b09969e940f444d8271467c64d4ce29b695c33d6db58232abe8f1916e44a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **222.4 MB (222393342 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:687ae8f10d1c20a6fcced881f4d4b991e8846598e8b824621eebb8eb1d09cfc9`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 22 Jan 2026 14:54:45 GMT
LABEL maintainer="Red Hat, Inc."
# Thu, 22 Jan 2026 14:54:45 GMT
LABEL vendor="Red Hat, Inc."
# Thu, 22 Jan 2026 14:54:45 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Thu, 22 Jan 2026 14:54:45 GMT
LABEL com.redhat.component="ubi10-minimal-container"       name="ubi10/ubi-minimal"       version="10.1"       cpe="cpe:/o:redhat:enterprise_linux:10.1"       distribution-scope="public"
# Thu, 22 Jan 2026 14:54:45 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Thu, 22 Jan 2026 14:54:45 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 10."
# Thu, 22 Jan 2026 14:54:45 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 22 Jan 2026 14:54:45 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 22 Jan 2026 14:54:45 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 10 Minimal"
# Thu, 22 Jan 2026 14:54:45 GMT
LABEL io.openshift.expose-services=""
# Thu, 22 Jan 2026 14:54:45 GMT
LABEL io.openshift.tags="minimal rhel10"
# Thu, 22 Jan 2026 14:54:45 GMT
ENV container oci
# Thu, 22 Jan 2026 14:54:45 GMT
COPY dir:7bdbe74d43c251ef87ffde9a283489e444dd9e506bb8c01cd1c97a9f3ac52ddd in /      
# Thu, 22 Jan 2026 14:54:45 GMT
COPY file:5de33b5fc08b00635bccf9134a18978dba13e2250aa51838f9969515a3957847 in /etc/yum.repos.d/.      
# Thu, 22 Jan 2026 14:54:45 GMT
CMD ["/bin/bash"]
# Thu, 22 Jan 2026 14:54:46 GMT
COPY file:595171150af68abc798ea385f7988d74b566aa8e84babff137f00b08b2164683 in /usr/share/buildinfo/content-sets.json      
# Thu, 22 Jan 2026 14:54:46 GMT
COPY file:595171150af68abc798ea385f7988d74b566aa8e84babff137f00b08b2164683 in /root/buildinfo/content_manifests/content-sets.json      
# Thu, 22 Jan 2026 14:54:46 GMT
COPY file:fa7fed90e5fa59b018eb8aa0c4c26e4f0c5e15ab4b12ea84973f9ece212d9ed6 in /usr/share/buildinfo/labels.json      
# Thu, 22 Jan 2026 14:54:46 GMT
COPY file:fa7fed90e5fa59b018eb8aa0c4c26e4f0c5e15ab4b12ea84973f9ece212d9ed6 in /root/buildinfo/labels.json      
# Thu, 22 Jan 2026 14:54:46 GMT
LABEL "architecture"="ppc64le" "vcs-type"="git" "vcs-ref"="0912ab420a80f21132d8a5e29d19a23339176677" "org.opencontainers.image.revision"="0912ab420a80f21132d8a5e29d19a23339176677" "build-date"="2026-01-22T14:54:33Z" "org.opencontainers.image.created"="2026-01-22T14:54:33Z" "release"="1769090502"org.opencontainers.image.revision=0912ab420a80f21132d8a5e29d19a23339176677,org.opencontainers.image.created=2026-01-22T14:54:33Z
# Fri, 23 Jan 2026 00:57:54 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 23 Jan 2026 00:57:54 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 23 Jan 2026 00:57:54 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 23 Jan 2026 00:57:54 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en         gnupg2     ;     microdnf clean all # buildkit
# Fri, 23 Jan 2026 00:57:54 GMT
ENV JAVA_VERSION=jdk-17.0.17+10
# Fri, 23 Jan 2026 01:00:11 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='dc29ca6d35beb4419b4b00419b8a3dfbf5ae551e1ae2b046b516d9a579d04533';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jdk_aarch64_linux_hotspot_17.0.17_10.tar.gz';          ;;        ppc64le)          ESUM='2a29d1be61940c1bd639018c07f4622e1f145a7ef34e7294fee877e39226d9da';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jdk_ppc64le_linux_hotspot_17.0.17_10.tar.gz';          ;;        s390x)          ESUM='76327b1d00c67f6be91717754fd85fc85ce496d48876f69accb9c53ed31dc546';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jdk_s390x_linux_hotspot_17.0.17_10.tar.gz';          ;;        x86_64)          ESUM='992f96e7995075ac7636bb1a8de52b0c61d71ed3137fafc979ab96b4ab78dd75';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jdk_x64_linux_hotspot_17.0.17_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Fri, 23 Jan 2026 01:00:14 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Fri, 23 Jan 2026 01:00:14 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Fri, 23 Jan 2026 01:00:14 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Fri, 23 Jan 2026 01:00:14 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:ca7d82d686e4448886b5d40d7ede2a94863423d05f007fae2fdf719fb557a51e`  
		Last Modified: Thu, 22 Jan 2026 18:12:54 GMT  
		Size: 38.7 MB (38718444 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b83cbc42d47e675c60991c0dfbc843db7691ef4e8247a33f719b14ab372f6ea2`  
		Last Modified: Fri, 23 Jan 2026 00:58:44 GMT  
		Size: 39.1 MB (39124637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fcefcb0a57cf665be4d33e889f51516effdb26d7b327b72768b0d34a8133a12f`  
		Last Modified: Fri, 23 Jan 2026 01:00:56 GMT  
		Size: 144.5 MB (144547841 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b818e7efdc107c03f78228fe3f2ceda757958910460eb94fe3a313abd13b168`  
		Last Modified: Fri, 23 Jan 2026 01:00:52 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ca4475700b20730eff28d97fb488213dab18a3cba74d20a6204ab26969bae00`  
		Last Modified: Fri, 23 Jan 2026 01:00:53 GMT  
		Size: 2.3 KB (2291 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:17-ubi10-minimal` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:8760577c2603484b54c4e856c67b3467aab8152da6c9070c5d05843321f9b0ba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3796665 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:00c0ce4137fc636782caea937ea9458bffaea7e56da8ad30b2e4e1359456ce11`

```dockerfile
```

-	Layers:
	-	`sha256:d13f9450964b8a0b811e654a1e46dc682bd93e55a71646dafc2737f5818043a9`  
		Last Modified: Fri, 23 Jan 2026 01:00:52 GMT  
		Size: 3.8 MB (3775289 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:aed50718e74c3c285f6640582053eb429bc939d8790afc970bd34714cc152a42`  
		Last Modified: Fri, 23 Jan 2026 01:00:52 GMT  
		Size: 21.4 KB (21376 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-temurin:17-ubi10-minimal` - linux; s390x

```console
$ docker pull eclipse-temurin@sha256:3eadf08093528bc21464cbf8f177b37bb6e06ffe859142546bb2e9d90edd43d3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **207.0 MB (206976798 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a12027947ae39603fea7c11ebf7758d844915ae1e9498754bdcf694b37c7f99`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 22 Jan 2026 14:57:07 GMT
LABEL maintainer="Red Hat, Inc."
# Thu, 22 Jan 2026 14:57:07 GMT
LABEL vendor="Red Hat, Inc."
# Thu, 22 Jan 2026 14:57:07 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Thu, 22 Jan 2026 14:57:07 GMT
LABEL com.redhat.component="ubi10-minimal-container"       name="ubi10/ubi-minimal"       version="10.1"       cpe="cpe:/o:redhat:enterprise_linux:10.1"       distribution-scope="public"
# Thu, 22 Jan 2026 14:57:07 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Thu, 22 Jan 2026 14:57:07 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 10."
# Thu, 22 Jan 2026 14:57:07 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 22 Jan 2026 14:57:07 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 22 Jan 2026 14:57:07 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 10 Minimal"
# Thu, 22 Jan 2026 14:57:08 GMT
LABEL io.openshift.expose-services=""
# Thu, 22 Jan 2026 14:57:08 GMT
LABEL io.openshift.tags="minimal rhel10"
# Thu, 22 Jan 2026 14:57:08 GMT
ENV container oci
# Thu, 22 Jan 2026 14:57:08 GMT
COPY dir:b163faed476797909497b9e9cbceacce9d202c7df0108da15dd805a940495105 in /      
# Thu, 22 Jan 2026 14:57:08 GMT
COPY file:5de33b5fc08b00635bccf9134a18978dba13e2250aa51838f9969515a3957847 in /etc/yum.repos.d/.      
# Thu, 22 Jan 2026 14:57:08 GMT
CMD ["/bin/bash"]
# Thu, 22 Jan 2026 14:57:08 GMT
COPY file:595171150af68abc798ea385f7988d74b566aa8e84babff137f00b08b2164683 in /usr/share/buildinfo/content-sets.json      
# Thu, 22 Jan 2026 14:57:08 GMT
COPY file:595171150af68abc798ea385f7988d74b566aa8e84babff137f00b08b2164683 in /root/buildinfo/content_manifests/content-sets.json      
# Thu, 22 Jan 2026 14:57:08 GMT
COPY file:d6bdaa4e7d25601d04555b39b781ff4f9dacbc577ea220997429cff55f920063 in /usr/share/buildinfo/labels.json      
# Thu, 22 Jan 2026 14:57:08 GMT
COPY file:d6bdaa4e7d25601d04555b39b781ff4f9dacbc577ea220997429cff55f920063 in /root/buildinfo/labels.json      
# Thu, 22 Jan 2026 14:57:09 GMT
LABEL "architecture"="s390x" "vcs-type"="git" "vcs-ref"="0912ab420a80f21132d8a5e29d19a23339176677" "org.opencontainers.image.revision"="0912ab420a80f21132d8a5e29d19a23339176677" "build-date"="2026-01-22T14:54:50Z" "org.opencontainers.image.created"="2026-01-22T14:54:50Z" "release"="1769090502"org.opencontainers.image.revision=0912ab420a80f21132d8a5e29d19a23339176677,org.opencontainers.image.created=2026-01-22T14:54:50Z
# Fri, 23 Jan 2026 00:57:42 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 23 Jan 2026 00:57:42 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 23 Jan 2026 00:57:42 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 23 Jan 2026 00:57:42 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en         gnupg2     ;     microdnf clean all # buildkit
# Fri, 23 Jan 2026 00:57:42 GMT
ENV JAVA_VERSION=jdk-17.0.17+10
# Fri, 23 Jan 2026 00:57:48 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='dc29ca6d35beb4419b4b00419b8a3dfbf5ae551e1ae2b046b516d9a579d04533';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jdk_aarch64_linux_hotspot_17.0.17_10.tar.gz';          ;;        ppc64le)          ESUM='2a29d1be61940c1bd639018c07f4622e1f145a7ef34e7294fee877e39226d9da';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jdk_ppc64le_linux_hotspot_17.0.17_10.tar.gz';          ;;        s390x)          ESUM='76327b1d00c67f6be91717754fd85fc85ce496d48876f69accb9c53ed31dc546';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jdk_s390x_linux_hotspot_17.0.17_10.tar.gz';          ;;        x86_64)          ESUM='992f96e7995075ac7636bb1a8de52b0c61d71ed3137fafc979ab96b4ab78dd75';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jdk_x64_linux_hotspot_17.0.17_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Fri, 23 Jan 2026 00:57:49 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Fri, 23 Jan 2026 00:57:49 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Fri, 23 Jan 2026 00:57:49 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Fri, 23 Jan 2026 00:57:49 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:4305950dff5b7a63645441b4e7ab741317691b48df386123d1f9cf51b053ff55`  
		Last Modified: Thu, 22 Jan 2026 18:12:46 GMT  
		Size: 34.4 MB (34360531 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:837e8e06eae984f24eeb3bba4016e3a03487cc51453ac39f13a90e683537e12d`  
		Last Modified: Fri, 23 Jan 2026 00:58:06 GMT  
		Size: 37.8 MB (37751630 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebf5ad4c3c1d6c87ae2d6e668132b6b568658a34e1f3c2685c870bc004a502ff`  
		Last Modified: Fri, 23 Jan 2026 00:58:16 GMT  
		Size: 134.9 MB (134862215 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e731134e8a3e324a067e22655e5c78925993a71988aa5fdc23c27a6e0af1bc8`  
		Last Modified: Fri, 23 Jan 2026 00:58:13 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00f13186450713b3ca26259127126905e7c1f8e3584e7cbb1415641446d18fd8`  
		Last Modified: Fri, 23 Jan 2026 00:58:13 GMT  
		Size: 2.3 KB (2293 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:17-ubi10-minimal` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:d69830f7e28582a8cc7e4ed87b14c7bf6aa12ad8edcf91f04cb0cbe1391ecabd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3795387 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f89b96ed234a8a51649d2833a952385785ccbbd7bd955d5d68b1070840057b93`

```dockerfile
```

-	Layers:
	-	`sha256:88cb88448c8ac2b7577f2ca0229fa80d8e23bedb8789dcbc7c8b77d60e511e49`  
		Last Modified: Fri, 23 Jan 2026 00:58:13 GMT  
		Size: 3.8 MB (3774047 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6fbdbd83de7fba6bb33af4f125441afd91376149656fd470a28c54cd21a5e983`  
		Last Modified: Fri, 23 Jan 2026 00:58:13 GMT  
		Size: 21.3 KB (21340 bytes)  
		MIME: application/vnd.in-toto+json
