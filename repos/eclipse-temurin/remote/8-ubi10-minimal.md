## `eclipse-temurin:8-ubi10-minimal`

```console
$ docker pull eclipse-temurin@sha256:8f5c5933db909a41f19172be2108e604f9d1ad6fe377271e19679fd08b417259
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
$ docker pull eclipse-temurin@sha256:0bfb613d07925e99c70d130ae59204b4dbee5168fd8be021dc4e6ddda57c43bb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **147.4 MB (147430631 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b9ddcbd4741a1d21b9d765a5b608cedeaf76d98da6aa60c842efe5eebe170ec3`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`

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
# Fri, 14 Nov 2025 01:12:19 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 14 Nov 2025 01:12:19 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 14 Nov 2025 01:12:19 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 14 Nov 2025 01:12:19 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en         gnupg2     ;     microdnf clean all # buildkit
# Fri, 14 Nov 2025 01:12:19 GMT
ENV JAVA_VERSION=jdk8u472-b08
# Fri, 14 Nov 2025 01:12:22 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='e2aff19d85d2441e409d6cbdf12ef7c2acabb0de73bca4207947135dcaa935a2';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u472-b08/OpenJDK8U-jdk_aarch64_linux_hotspot_8u472b08.tar.gz';          ;;        ppc64le)          ESUM='eaf57a4564265583b0641c878bea8943d27ef110c096868f686dae179fb45d8f';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u472-b08/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u472b08.tar.gz';          ;;        x86_64)          ESUM='5becaa4ac660e844c5a39e2ebc39ff5ac824c37ff1b625af8c8b111dc13c3592';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u472-b08/OpenJDK8U-jdk_x64_linux_hotspot_8u472b08.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip; # buildkit
# Fri, 14 Nov 2025 01:12:23 GMT
RUN set -eux;     echo "Verifying install ...";     echo "javac -version"; javac -version;     echo "java -version"; java -version;     echo "Complete." # buildkit
# Fri, 14 Nov 2025 01:12:23 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Fri, 14 Nov 2025 01:12:23 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
```

-	Layers:
	-	`sha256:7164be7c15828f5ba5fa7731cf51dad23a5d6c99e19fa840e574def3f4c05894`  
		Last Modified: Wed, 12 Nov 2025 17:56:02 GMT  
		Size: 34.5 MB (34515519 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a0fbb7557ab5bfb244bc549cff06eefb17390e0aeb1692d223a263d5ad8cc47`  
		Last Modified: Fri, 14 Nov 2025 01:12:53 GMT  
		Size: 58.2 MB (58178800 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da3044c3f69fe5b92b9bc865c983d7965a04b72274eb816f27927798093858d0`  
		Last Modified: Fri, 14 Nov 2025 01:12:55 GMT  
		Size: 54.7 MB (54733868 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44f5a30e316ce047665b38e450dad5ae2d1c60917b07f1590bc516f3ccfbafa6`  
		Last Modified: Fri, 14 Nov 2025 01:12:49 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44d58bb6ece1d2f38012bcd746edca9c97d5e9c713f634f86226ede90f075531`  
		Last Modified: Fri, 14 Nov 2025 01:12:49 GMT  
		Size: 2.3 KB (2315 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:8-ubi10-minimal` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:0d9dc0e991acf7fcf18af812c91b78e25e2fbab6c990f052b896a9c956aaddc0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5822153 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e138c7251ac48ccd277bc88691c5b6ffbb9e8c2dcdd604c797462b917ac823b`

```dockerfile
```

-	Layers:
	-	`sha256:7ead98b2fdb7b7abed304060dc0ad5447e55259a5469f8d1b258611f4b25bfe9`  
		Last Modified: Fri, 14 Nov 2025 04:18:36 GMT  
		Size: 5.8 MB (5802114 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6eafe6bc66fbd2af49b4b5994a5ce74fc7652d0ece20b745845c2b01f561b4c6`  
		Last Modified: Fri, 14 Nov 2025 04:18:37 GMT  
		Size: 20.0 KB (20039 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-temurin:8-ubi10-minimal` - linux; arm64 variant v8

```console
$ docker pull eclipse-temurin@sha256:aede6c50aaef921f6cbbb6fa548026c46027be217a2158cbe658d85806ece78c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **144.2 MB (144205162 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:62b942eb2d781f015d7c73d3504a121e307ee54f5d18d43b1de677499ea04062`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`

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
# Fri, 14 Nov 2025 01:28:43 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 14 Nov 2025 01:28:43 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 14 Nov 2025 01:28:43 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 14 Nov 2025 01:28:43 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en         gnupg2     ;     microdnf clean all # buildkit
# Fri, 14 Nov 2025 01:28:43 GMT
ENV JAVA_VERSION=jdk8u472-b08
# Fri, 14 Nov 2025 01:28:47 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='e2aff19d85d2441e409d6cbdf12ef7c2acabb0de73bca4207947135dcaa935a2';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u472-b08/OpenJDK8U-jdk_aarch64_linux_hotspot_8u472b08.tar.gz';          ;;        ppc64le)          ESUM='eaf57a4564265583b0641c878bea8943d27ef110c096868f686dae179fb45d8f';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u472-b08/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u472b08.tar.gz';          ;;        x86_64)          ESUM='5becaa4ac660e844c5a39e2ebc39ff5ac824c37ff1b625af8c8b111dc13c3592';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u472-b08/OpenJDK8U-jdk_x64_linux_hotspot_8u472b08.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip; # buildkit
# Fri, 14 Nov 2025 01:28:48 GMT
RUN set -eux;     echo "Verifying install ...";     echo "javac -version"; javac -version;     echo "java -version"; java -version;     echo "Complete." # buildkit
# Fri, 14 Nov 2025 01:28:48 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Fri, 14 Nov 2025 01:28:48 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
```

-	Layers:
	-	`sha256:372b71efdab733f5ad0749f1537278e34899107888219d8358967ddbd9eb2db3`  
		Last Modified: Wed, 12 Nov 2025 18:16:55 GMT  
		Size: 32.6 MB (32601501 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8dcb0a4fab263866977261141e74dc0ae5937c77e207be4fc79928d7c61d5fd3`  
		Last Modified: Fri, 14 Nov 2025 01:29:28 GMT  
		Size: 57.8 MB (57785591 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e61e63625a81aa3037a49fecb63f5f87db38c7a9102184135ec8a1aaee0fe883`  
		Last Modified: Fri, 14 Nov 2025 01:29:29 GMT  
		Size: 53.8 MB (53815625 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:adfee09fe2931533395f7971a00ae50a56c3ef8139ee43b560c67552027b71ac`  
		Last Modified: Fri, 14 Nov 2025 01:29:18 GMT  
		Size: 130.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a740b15aa05b8b7b76b0cf56f4ba8e0931b1f128bd42275dbe603d00a859ac75`  
		Last Modified: Fri, 14 Nov 2025 01:29:18 GMT  
		Size: 2.3 KB (2315 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:8-ubi10-minimal` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:0bc61af419e53f19611db5fcddf7caddca8b4ce593ae4121eda118babac02015
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5822457 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:60a5a6bf76d1269be6b45a64fb388e85be850a70c2358eb2099e66989929dfdb`

```dockerfile
```

-	Layers:
	-	`sha256:19b35b1d0c7db808ad919c0c10d0cb16c45102e5255ac23516223337af87598a`  
		Last Modified: Fri, 14 Nov 2025 04:18:42 GMT  
		Size: 5.8 MB (5802302 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9b506426ba3fdbd3b18da77ebbfb812850ffe0998b26eaf8a0e3fc4436cfe020`  
		Last Modified: Fri, 14 Nov 2025 04:18:42 GMT  
		Size: 20.2 KB (20155 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-temurin:8-ubi10-minimal` - linux; ppc64le

```console
$ docker pull eclipse-temurin@sha256:d37ffaf925957b5b64372f8699e4b2b0d43e3cc0ebd8ebb48f9148f052b1666f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **151.3 MB (151282656 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:39f2d2844e25eddbe40a17e93973fb552426c1b0c12f8d1f763ba85eb4e35b04`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`

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
ENV JAVA_VERSION=jdk8u472-b08
# Fri, 14 Nov 2025 02:04:11 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='e2aff19d85d2441e409d6cbdf12ef7c2acabb0de73bca4207947135dcaa935a2';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u472-b08/OpenJDK8U-jdk_aarch64_linux_hotspot_8u472b08.tar.gz';          ;;        ppc64le)          ESUM='eaf57a4564265583b0641c878bea8943d27ef110c096868f686dae179fb45d8f';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u472-b08/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u472b08.tar.gz';          ;;        x86_64)          ESUM='5becaa4ac660e844c5a39e2ebc39ff5ac824c37ff1b625af8c8b111dc13c3592';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u472-b08/OpenJDK8U-jdk_x64_linux_hotspot_8u472b08.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip; # buildkit
# Fri, 14 Nov 2025 02:04:13 GMT
RUN set -eux;     echo "Verifying install ...";     echo "javac -version"; javac -version;     echo "java -version"; java -version;     echo "Complete." # buildkit
# Fri, 14 Nov 2025 02:04:13 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Fri, 14 Nov 2025 02:04:13 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
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
	-	`sha256:4fad82e3f63cd10fb96937e6a90098d5139c569a884a3a72a0824d1356c13d36`  
		Last Modified: Fri, 14 Nov 2025 02:05:21 GMT  
		Size: 52.2 MB (52175814 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fcb3c5168ed14183be2f82aa06b10e1424f51c39e4f9d0908e5a1fd7d12da33`  
		Last Modified: Fri, 14 Nov 2025 02:05:13 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32c17342ec2e407c7d918ff7c2d5712a9bb86037516730149ce889c9c52409d8`  
		Last Modified: Fri, 14 Nov 2025 02:05:13 GMT  
		Size: 2.3 KB (2316 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:8-ubi10-minimal` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:7e2ae7fb8ab2bcfff936b3b63ca2bdef65919835bfaa7b605abf83ecaec5f38a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5809934 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:400e1ea7220a004799c52e2f19ac289cc554140370d35c4ae356914627bf7942`

```dockerfile
```

-	Layers:
	-	`sha256:4fda45ff2a914837f9bf6122eda711b4304d45ec9ab8db337870f93646bd0c2d`  
		Last Modified: Fri, 14 Nov 2025 04:18:47 GMT  
		Size: 5.8 MB (5789859 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c1e9c2b4ac30eeb13e773ea70df03d98d37f483fcfac1919b4f52b8452bc9a77`  
		Last Modified: Fri, 14 Nov 2025 04:18:48 GMT  
		Size: 20.1 KB (20075 bytes)  
		MIME: application/vnd.in-toto+json
