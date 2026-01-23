## `eclipse-temurin:21-ubi10-minimal`

```console
$ docker pull eclipse-temurin@sha256:2dd8e3a956b57579c9608db9097768dc6424eb9925f5659e103bd17c0250a3ba
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

### `eclipse-temurin:21-ubi10-minimal` - linux; amd64

```console
$ docker pull eclipse-temurin@sha256:eeb75e97919be8009bec8a929f8d30076f777a2d7ba447753a5edb5e093df74d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **229.7 MB (229731794 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a48a95311998f879b575bd4aed6d28d4a892d9942569926a4f71f7a93277c2a`
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
ENV JAVA_VERSION=jdk-21.0.9+10
# Fri, 23 Jan 2026 01:01:27 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='edf0da4debe7cf475dbe320d174d6eed81479eb363f41e38a2efb740428c603a';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.9%2B10/OpenJDK21U-jdk_aarch64_linux_hotspot_21.0.9_10.tar.gz';          ;;        ppc64le)          ESUM='ac5a0394a234269b4e20459649ac93cb702cde29b3e46a0bcf3aa53958f2d4a4';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.9%2B10/OpenJDK21U-jdk_ppc64le_linux_hotspot_21.0.9_10.tar.gz';          ;;        s390x)          ESUM='e8ede0fb48aaa3a0cc1ac7c8522f8ca7938bdbb8be0d603b61134de7f898aff4';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.9%2B10/OpenJDK21U-jdk_s390x_linux_hotspot_21.0.9_10.tar.gz';          ;;        x86_64)          ESUM='810d3773df7e0d6c4394e4e244b264c8b30e0b05a0acf542d065fd78a6b65c2f';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.9%2B10/OpenJDK21U-jdk_x64_linux_hotspot_21.0.9_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Fri, 23 Jan 2026 01:01:28 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Fri, 23 Jan 2026 01:01:28 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Fri, 23 Jan 2026 01:01:28 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Fri, 23 Jan 2026 01:01:28 GMT
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
	-	`sha256:4e4a9ca4c34bba766e91e844b6560cd8ab4e5fe116feb2397aa30ca18e09b721`  
		Last Modified: Fri, 23 Jan 2026 01:01:47 GMT  
		Size: 157.8 MB (157828948 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d586f34d22082401aab761d5642b646c7ece43f0ed501e588f55c2808c19fd0`  
		Last Modified: Fri, 23 Jan 2026 01:01:43 GMT  
		Size: 130.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fb1fa558bc39a2f90e126aac69cba38f99fb71159206239421322c8a4ca3cbc`  
		Last Modified: Fri, 23 Jan 2026 01:01:43 GMT  
		Size: 2.3 KB (2291 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:21-ubi10-minimal` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:3c4dd644e6d6df46a259acf536f7fc0c2dbdb4d4a0f004be19614093438ceda8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3812873 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6946f5ca0b7db75db314f59a92b144c367070c621977a8a6db8e7ff9d406fd2e`

```dockerfile
```

-	Layers:
	-	`sha256:252fe93536748f91f841479202f9033c79d51b5a1d0ecf21dc2b0872fce95f8e`  
		Last Modified: Fri, 23 Jan 2026 01:01:43 GMT  
		Size: 3.8 MB (3791557 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7515f3755558ae7b044680a0695fe80fda95139cc3b69704bd1c3635279f3807`  
		Last Modified: Fri, 23 Jan 2026 01:01:43 GMT  
		Size: 21.3 KB (21316 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-temurin:21-ubi10-minimal` - linux; arm64 variant v8

```console
$ docker pull eclipse-temurin@sha256:22e3f1114fbc0491f9cedf81ec624e004e0eab52c79ab1ddd320ac02968fc76e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **226.0 MB (226043530 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f1827c29d0fcb1c3fbcc8f6e576622a0588c31095c9bb35c0758be5da34eb0f`
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
ENV JAVA_VERSION=jdk-21.0.9+10
# Fri, 23 Jan 2026 00:59:58 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='edf0da4debe7cf475dbe320d174d6eed81479eb363f41e38a2efb740428c603a';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.9%2B10/OpenJDK21U-jdk_aarch64_linux_hotspot_21.0.9_10.tar.gz';          ;;        ppc64le)          ESUM='ac5a0394a234269b4e20459649ac93cb702cde29b3e46a0bcf3aa53958f2d4a4';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.9%2B10/OpenJDK21U-jdk_ppc64le_linux_hotspot_21.0.9_10.tar.gz';          ;;        s390x)          ESUM='e8ede0fb48aaa3a0cc1ac7c8522f8ca7938bdbb8be0d603b61134de7f898aff4';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.9%2B10/OpenJDK21U-jdk_s390x_linux_hotspot_21.0.9_10.tar.gz';          ;;        x86_64)          ESUM='810d3773df7e0d6c4394e4e244b264c8b30e0b05a0acf542d065fd78a6b65c2f';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.9%2B10/OpenJDK21U-jdk_x64_linux_hotspot_21.0.9_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Fri, 23 Jan 2026 00:59:59 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Fri, 23 Jan 2026 00:59:59 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Fri, 23 Jan 2026 00:59:59 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Fri, 23 Jan 2026 00:59:59 GMT
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
	-	`sha256:3f5d12680e8b469f3662469f40b0c3662be7647d2953d01057c09438f3d76976`  
		Last Modified: Fri, 23 Jan 2026 01:00:21 GMT  
		Size: 156.1 MB (156111818 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b542af2243f62cfcbaf1b6764fbeb37d494198f84aa2f9562832fa83b47bfbd9`  
		Last Modified: Fri, 23 Jan 2026 01:00:18 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30197c01feaebc15bd09c1c58df8176313c3367aa0fcb6865061faa915f160d7`  
		Last Modified: Fri, 23 Jan 2026 01:00:19 GMT  
		Size: 2.3 KB (2291 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:21-ubi10-minimal` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:8a78d2d3312c4e8a8160415bca140849034798a5281f7ef52ed47220825567c9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3812415 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d2eb778b07dfa23f21bb0ebaed1b0dc2afd0609c24dcd85b58443a4757871961`

```dockerfile
```

-	Layers:
	-	`sha256:ed84a4529487424faecba6cd43be1b968a6fef2da1ff3b35e14880933966c9bb`  
		Last Modified: Fri, 23 Jan 2026 01:00:18 GMT  
		Size: 3.8 MB (3790983 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9083cf75b3b808dae5fa312e279bf335aa3a278c4e9c6527c64ab5a8886a37c3`  
		Last Modified: Fri, 23 Jan 2026 01:00:19 GMT  
		Size: 21.4 KB (21432 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-temurin:21-ubi10-minimal` - linux; ppc64le

```console
$ docker pull eclipse-temurin@sha256:33adedf08d8a7b94b474454d5a603237b581b7e0a819b297d645381971f8dfa2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **235.8 MB (235788985 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:27c6b71628efa59fef34dca9a60c7d31e0d7d1fdd8b8f2a51dd620117aafaf99`
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
ENV JAVA_VERSION=jdk-21.0.9+10
# Fri, 23 Jan 2026 01:01:22 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='edf0da4debe7cf475dbe320d174d6eed81479eb363f41e38a2efb740428c603a';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.9%2B10/OpenJDK21U-jdk_aarch64_linux_hotspot_21.0.9_10.tar.gz';          ;;        ppc64le)          ESUM='ac5a0394a234269b4e20459649ac93cb702cde29b3e46a0bcf3aa53958f2d4a4';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.9%2B10/OpenJDK21U-jdk_ppc64le_linux_hotspot_21.0.9_10.tar.gz';          ;;        s390x)          ESUM='e8ede0fb48aaa3a0cc1ac7c8522f8ca7938bdbb8be0d603b61134de7f898aff4';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.9%2B10/OpenJDK21U-jdk_s390x_linux_hotspot_21.0.9_10.tar.gz';          ;;        x86_64)          ESUM='810d3773df7e0d6c4394e4e244b264c8b30e0b05a0acf542d065fd78a6b65c2f';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.9%2B10/OpenJDK21U-jdk_x64_linux_hotspot_21.0.9_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Fri, 23 Jan 2026 01:01:26 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Fri, 23 Jan 2026 01:01:26 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Fri, 23 Jan 2026 01:01:26 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Fri, 23 Jan 2026 01:01:26 GMT
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
	-	`sha256:87228f48a761f1c36de6bb309eb0d148248e0aa1f0a2dfa320dc5be35ed963c9`  
		Last Modified: Fri, 23 Jan 2026 01:02:15 GMT  
		Size: 157.9 MB (157943484 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6c0e46f5ba5fb1a6f2e65a3d2fc5a3dff9cf95d4879254a134e642adfcc0157`  
		Last Modified: Fri, 23 Jan 2026 01:02:11 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b712d5dce91ea9d08ea33e2c7e564e07c0268f08ae2e6c75acbbd2f94c5153b2`  
		Last Modified: Fri, 23 Jan 2026 01:02:11 GMT  
		Size: 2.3 KB (2291 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:21-ubi10-minimal` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:207ece4b4f1c2664a3bd93ad5f70c0762e320e4240a7ce5902c75f18b4b69ddd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3799741 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb8ba3df28c60adf30841d249e434255faa41261487a51cdd82aec55eabd65a0`

```dockerfile
```

-	Layers:
	-	`sha256:47f0d91c73595bc4e75c5a7811ac4d63908a38906cd6b384b317cf0ca714a972`  
		Last Modified: Fri, 23 Jan 2026 01:02:12 GMT  
		Size: 3.8 MB (3778389 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dc921abe0ff0bb1f50f9b27986f2f0b7eca51d739ca708324a3177b4a0025541`  
		Last Modified: Fri, 23 Jan 2026 01:02:11 GMT  
		Size: 21.4 KB (21352 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-temurin:21-ubi10-minimal` - linux; s390x

```console
$ docker pull eclipse-temurin@sha256:5d293001eb056e04495f0408cbcdd8026aa5869a96de518df6cb27d20d205f62
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **219.2 MB (219183333 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e9fa00660a2f45fa9c6cd8335994c2af72433456c43ecc69427b66ffff1499e`
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
# Fri, 23 Jan 2026 00:57:41 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 23 Jan 2026 00:57:41 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 23 Jan 2026 00:57:41 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 23 Jan 2026 00:57:41 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en         gnupg2     ;     microdnf clean all # buildkit
# Fri, 23 Jan 2026 00:57:41 GMT
ENV JAVA_VERSION=jdk-21.0.9+10
# Fri, 23 Jan 2026 00:58:26 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='edf0da4debe7cf475dbe320d174d6eed81479eb363f41e38a2efb740428c603a';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.9%2B10/OpenJDK21U-jdk_aarch64_linux_hotspot_21.0.9_10.tar.gz';          ;;        ppc64le)          ESUM='ac5a0394a234269b4e20459649ac93cb702cde29b3e46a0bcf3aa53958f2d4a4';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.9%2B10/OpenJDK21U-jdk_ppc64le_linux_hotspot_21.0.9_10.tar.gz';          ;;        s390x)          ESUM='e8ede0fb48aaa3a0cc1ac7c8522f8ca7938bdbb8be0d603b61134de7f898aff4';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.9%2B10/OpenJDK21U-jdk_s390x_linux_hotspot_21.0.9_10.tar.gz';          ;;        x86_64)          ESUM='810d3773df7e0d6c4394e4e244b264c8b30e0b05a0acf542d065fd78a6b65c2f';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.9%2B10/OpenJDK21U-jdk_x64_linux_hotspot_21.0.9_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Fri, 23 Jan 2026 00:58:27 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Fri, 23 Jan 2026 00:58:27 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Fri, 23 Jan 2026 00:58:27 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Fri, 23 Jan 2026 00:58:27 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:4305950dff5b7a63645441b4e7ab741317691b48df386123d1f9cf51b053ff55`  
		Last Modified: Thu, 22 Jan 2026 18:12:46 GMT  
		Size: 34.4 MB (34360531 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60a32a7eba25e3f29f4e39e71b6844c79632eddfad3907c76a741789b46122d0`  
		Last Modified: Fri, 23 Jan 2026 00:58:04 GMT  
		Size: 37.8 MB (37751890 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64d0a6aca915e3647b0f4593c2c1734d812fc6f26c115b5ac930e41a1e463e55`  
		Last Modified: Fri, 23 Jan 2026 00:58:54 GMT  
		Size: 147.1 MB (147068493 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43fa54d6be3f65ae7f0893965920ee243b6f114365fea43c1265270af16422db`  
		Last Modified: Fri, 23 Jan 2026 00:58:51 GMT  
		Size: 131.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1241bb9865204901db68628c77aed68da6f2504de1420eca9fc74f521dc37edd`  
		Last Modified: Fri, 23 Jan 2026 00:58:51 GMT  
		Size: 2.3 KB (2288 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:21-ubi10-minimal` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:958211bb72143faf415a2b7e26e7d17a0d991634175ce42250aee132aa42d986
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3798463 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f479ceeafd88fdc4c6e6b4b0885227e1cde46d87f4fd7e9be68909ef683cd00d`

```dockerfile
```

-	Layers:
	-	`sha256:26d81f4646606e651a6273ace6a7bf7e08f5d322bac510fccc8fa8acaec896e9`  
		Last Modified: Fri, 23 Jan 2026 00:58:51 GMT  
		Size: 3.8 MB (3777147 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:73c5d6a50c67e4988928a8c553da70a7d538ba0943c34f87bf1df1e4d50d11b6`  
		Last Modified: Fri, 23 Jan 2026 00:58:51 GMT  
		Size: 21.3 KB (21316 bytes)  
		MIME: application/vnd.in-toto+json
