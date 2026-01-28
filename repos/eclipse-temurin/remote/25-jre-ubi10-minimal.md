## `eclipse-temurin:25-jre-ubi10-minimal`

```console
$ docker pull eclipse-temurin@sha256:34a1044b0cbaeacf77b71f985c44b631a0d5d3c42dd4ebd216a8b4781eb9d1ab
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

### `eclipse-temurin:25-jre-ubi10-minimal` - linux; amd64

```console
$ docker pull eclipse-temurin@sha256:a69828f4a85daf453d949f4cbc855f0cae5d01c02c536590bbad0ac38db50d6f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **137.4 MB (137372353 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c000b693e9b14128e8150c455a9571fdc00135b4921145f816bd526ef6538341`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`

```dockerfile
# Tue, 27 Jan 2026 13:43:38 GMT
LABEL maintainer="Red Hat, Inc."
# Tue, 27 Jan 2026 13:43:38 GMT
LABEL vendor="Red Hat, Inc."
# Tue, 27 Jan 2026 13:43:38 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Tue, 27 Jan 2026 13:43:38 GMT
LABEL com.redhat.component="ubi10-minimal-container"       name="ubi10/ubi-minimal"       version="10.1"       cpe="cpe:/o:redhat:enterprise_linux:10.1"       distribution-scope="public"
# Tue, 27 Jan 2026 13:43:38 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Tue, 27 Jan 2026 13:43:39 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 10."
# Tue, 27 Jan 2026 13:43:39 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Tue, 27 Jan 2026 13:43:39 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Tue, 27 Jan 2026 13:43:39 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 10 Minimal"
# Tue, 27 Jan 2026 13:43:39 GMT
LABEL io.openshift.expose-services=""
# Tue, 27 Jan 2026 13:43:39 GMT
LABEL io.openshift.tags="minimal rhel10"
# Tue, 27 Jan 2026 13:43:39 GMT
ENV container oci
# Tue, 27 Jan 2026 13:43:40 GMT
COPY dir:c206a7c74c2764db52e4fe9e9bb5506227dd2a550e47afa696c9a7c923f9a0ff in /      
# Tue, 27 Jan 2026 13:43:40 GMT
COPY file:5de33b5fc08b00635bccf9134a18978dba13e2250aa51838f9969515a3957847 in /etc/yum.repos.d/.      
# Tue, 27 Jan 2026 13:43:40 GMT
CMD ["/bin/bash"]
# Tue, 27 Jan 2026 13:43:40 GMT
COPY file:595171150af68abc798ea385f7988d74b566aa8e84babff137f00b08b2164683 in /usr/share/buildinfo/content-sets.json      
# Tue, 27 Jan 2026 13:43:40 GMT
COPY file:595171150af68abc798ea385f7988d74b566aa8e84babff137f00b08b2164683 in /root/buildinfo/content_manifests/content-sets.json      
# Tue, 27 Jan 2026 13:43:40 GMT
COPY file:8db1dc4b84412d8a3137b92a8b51dc81382218dadd1dc925bd2c056986c8eb72 in /usr/share/buildinfo/labels.json      
# Tue, 27 Jan 2026 13:43:40 GMT
COPY file:8db1dc4b84412d8a3137b92a8b51dc81382218dadd1dc925bd2c056986c8eb72 in /root/buildinfo/labels.json      
# Tue, 27 Jan 2026 13:43:40 GMT
LABEL "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="2945215ed3e1eed38f41b60201d6d7def9446c9f" "org.opencontainers.image.revision"="2945215ed3e1eed38f41b60201d6d7def9446c9f" "build-date"="2026-01-27T13:43:17Z" "org.opencontainers.image.created"="2026-01-27T13:43:17Z" "release"="1769521234"org.opencontainers.image.revision=2945215ed3e1eed38f41b60201d6d7def9446c9f,org.opencontainers.image.created=2026-01-27T13:43:17Z
# Wed, 28 Jan 2026 19:01:09 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 28 Jan 2026 19:01:09 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 28 Jan 2026 19:01:09 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 28 Jan 2026 19:01:09 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en         gnupg2     ;     microdnf clean all # buildkit
# Wed, 28 Jan 2026 19:01:09 GMT
ENV JAVA_VERSION=jdk-25.0.1+8
# Wed, 28 Jan 2026 19:03:08 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='5371ad922cb4ff571a57c8e5dd14485ebf5b3994cd71e6ea09088312de3bed71';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.1%2B8/OpenJDK25U-jre_aarch64_linux_hotspot_25.0.1_8.tar.gz';          ;;        ppc64le)          ESUM='c812bf806d7ffcd290c6bd814324aa81f0688e2d682fd0b87e2c7c76251a4f2c';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.1%2B8/OpenJDK25U-jre_ppc64le_linux_hotspot_25.0.1_8.tar.gz';          ;;        s390x)          ESUM='c58764b69cb70e7b532f50e8a20e74aa5cb65e85c3e500225e0b64719a6021a0';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.1%2B8/OpenJDK25U-jre_s390x_linux_hotspot_25.0.1_8.tar.gz';          ;;        x86_64)          ESUM='126c7f59b91df97b2e930b0a456422ce29af7f2385117e1c04297eba962b0b1c';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.1%2B8/OpenJDK25U-jre_x64_linux_hotspot_25.0.1_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz; # buildkit
# Wed, 28 Jan 2026 19:03:08 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 28 Jan 2026 19:03:08 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 28 Jan 2026 19:03:08 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
```

-	Layers:
	-	`sha256:6af7d70117fb54a1c19fa7ab0dd6387be5ab897497b2986acffbb49ebe56b290`  
		Last Modified: Tue, 27 Jan 2026 17:15:27 GMT  
		Size: 34.6 MB (34556452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d07c4b90ad1632b62807fa00118e5bba9f56eab391acf26fe0b078e2f530e69d`  
		Last Modified: Wed, 28 Jan 2026 19:01:29 GMT  
		Size: 40.2 MB (40217484 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e98411e0e9f77e6833d982797a5057714f38655d0c1ea42013952540fd37d02`  
		Last Modified: Wed, 28 Jan 2026 19:03:24 GMT  
		Size: 62.6 MB (62595998 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a6dd536d673927bf7ed6c6f68f3a312cc7d605a73b81e775ba0dfd6f9f9a52b`  
		Last Modified: Wed, 28 Jan 2026 19:03:22 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d650cb48cedb4c451c39614998d5289d774c4ba9cd65e9919eff817c96e458c9`  
		Last Modified: Wed, 28 Jan 2026 19:03:22 GMT  
		Size: 2.3 KB (2291 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:25-jre-ubi10-minimal` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:def0b4dc3c93ca956e69d96e723fdba1cb1babdc928db263a19ab7486a7fac96
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3733124 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f8b66ddb5f81e4f4411465557c939014165cb2c5892dc4b38c9f5105b55df04b`

```dockerfile
```

-	Layers:
	-	`sha256:cfe3ff119d6523966c308c369c8a76988d816ff8ac177ceebc6ffe22d8fcb87d`  
		Last Modified: Wed, 28 Jan 2026 19:03:22 GMT  
		Size: 3.7 MB (3712794 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8df4dc6da26dd693c8aa5459cb0d09807d69724b08c81cd2ef95ebc627bf6149`  
		Last Modified: Wed, 28 Jan 2026 19:03:22 GMT  
		Size: 20.3 KB (20330 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-temurin:25-jre-ubi10-minimal` - linux; arm64 variant v8

```console
$ docker pull eclipse-temurin@sha256:22371bac152eab11ec3e64cf94dcbee71823917c4321a80a91b3e19686b81a2c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **131.5 MB (131474794 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:47d62391e528b625841d0083f4f9a8b87c7d51632eb174c9605ed2e65d1f9e3d`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`

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
ENV JAVA_VERSION=jdk-25.0.1+8
# Fri, 23 Jan 2026 01:00:39 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='5371ad922cb4ff571a57c8e5dd14485ebf5b3994cd71e6ea09088312de3bed71';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.1%2B8/OpenJDK25U-jre_aarch64_linux_hotspot_25.0.1_8.tar.gz';          ;;        ppc64le)          ESUM='c812bf806d7ffcd290c6bd814324aa81f0688e2d682fd0b87e2c7c76251a4f2c';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.1%2B8/OpenJDK25U-jre_ppc64le_linux_hotspot_25.0.1_8.tar.gz';          ;;        s390x)          ESUM='c58764b69cb70e7b532f50e8a20e74aa5cb65e85c3e500225e0b64719a6021a0';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.1%2B8/OpenJDK25U-jre_s390x_linux_hotspot_25.0.1_8.tar.gz';          ;;        x86_64)          ESUM='126c7f59b91df97b2e930b0a456422ce29af7f2385117e1c04297eba962b0b1c';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.1%2B8/OpenJDK25U-jre_x64_linux_hotspot_25.0.1_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz; # buildkit
# Fri, 23 Jan 2026 01:00:39 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Fri, 23 Jan 2026 01:00:39 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Fri, 23 Jan 2026 01:00:39 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
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
	-	`sha256:9131a353d4ff6d527a76f57998376299a516f532ce2d728533d986e098452d6d`  
		Last Modified: Fri, 23 Jan 2026 01:00:56 GMT  
		Size: 61.5 MB (61543082 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ec3f9fc3f8dd430b5bab0ef3332c39d2354a16b7f95f3ce78c3a8dc44c7b444`  
		Last Modified: Fri, 23 Jan 2026 01:00:54 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9dbdf30ebebfb25cd7ac499cc98995aa85bd788b064ad58d22f34523993209ba`  
		Last Modified: Fri, 23 Jan 2026 01:00:54 GMT  
		Size: 2.3 KB (2291 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:25-jre-ubi10-minimal` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:207c4595d94bf058c100f1366689f103b4e598cf04b3d0cadcc635fbd475a22e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3732639 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3b821769849929d204598c9a2052aca844025e6655e8347e190ee35cd9d1fea5`

```dockerfile
```

-	Layers:
	-	`sha256:fc897cc082efb13dcdb0859fd95d4593e21a90f673c5f3213ba2728f7bbcff85`  
		Last Modified: Fri, 23 Jan 2026 01:00:54 GMT  
		Size: 3.7 MB (3712205 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5d919da7385bdd9aae7dd72013db9302b679579c26fe44bc3125e3fed1340edd`  
		Last Modified: Fri, 23 Jan 2026 01:00:55 GMT  
		Size: 20.4 KB (20434 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-temurin:25-jre-ubi10-minimal` - linux; ppc64le

```console
$ docker pull eclipse-temurin@sha256:7343fca326964d5b3daea98bc921c9b7a1c95c4a3eead6b90b8ad25269b82064
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **139.8 MB (139798213 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aac95938b120efaa3c601166ead8ce6567cd97bbace439ff254f9a0b8c0e2712`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`

```dockerfile
# Tue, 27 Jan 2026 15:50:35 GMT
LABEL maintainer="Red Hat, Inc."
# Tue, 27 Jan 2026 15:50:35 GMT
LABEL vendor="Red Hat, Inc."
# Tue, 27 Jan 2026 15:50:35 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Tue, 27 Jan 2026 15:50:35 GMT
LABEL com.redhat.component="ubi10-minimal-container"       name="ubi10/ubi-minimal"       version="10.1"       cpe="cpe:/o:redhat:enterprise_linux:10.1"       distribution-scope="public"
# Tue, 27 Jan 2026 15:50:35 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Tue, 27 Jan 2026 15:50:35 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 10."
# Tue, 27 Jan 2026 15:50:35 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Tue, 27 Jan 2026 15:50:35 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Tue, 27 Jan 2026 15:50:35 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 10 Minimal"
# Tue, 27 Jan 2026 15:50:35 GMT
LABEL io.openshift.expose-services=""
# Tue, 27 Jan 2026 15:50:35 GMT
LABEL io.openshift.tags="minimal rhel10"
# Tue, 27 Jan 2026 15:50:35 GMT
ENV container oci
# Tue, 27 Jan 2026 15:50:36 GMT
COPY dir:b1fb54cba477aa8e5cc12c75f143c33f00068a49e572e2a9058ca695db013356 in /      
# Tue, 27 Jan 2026 15:50:36 GMT
COPY file:5de33b5fc08b00635bccf9134a18978dba13e2250aa51838f9969515a3957847 in /etc/yum.repos.d/.      
# Tue, 27 Jan 2026 15:50:36 GMT
CMD ["/bin/bash"]
# Tue, 27 Jan 2026 15:50:36 GMT
COPY file:595171150af68abc798ea385f7988d74b566aa8e84babff137f00b08b2164683 in /usr/share/buildinfo/content-sets.json      
# Tue, 27 Jan 2026 15:50:36 GMT
COPY file:595171150af68abc798ea385f7988d74b566aa8e84babff137f00b08b2164683 in /root/buildinfo/content_manifests/content-sets.json      
# Tue, 27 Jan 2026 15:50:36 GMT
COPY file:7b0b7973b756ae5fa48a994ea290e7e8ecbd19057a845071702a88d3f44c82d7 in /usr/share/buildinfo/labels.json      
# Tue, 27 Jan 2026 15:50:36 GMT
COPY file:7b0b7973b756ae5fa48a994ea290e7e8ecbd19057a845071702a88d3f44c82d7 in /root/buildinfo/labels.json      
# Tue, 27 Jan 2026 15:50:36 GMT
LABEL "architecture"="ppc64le" "vcs-type"="git" "vcs-ref"="2945215ed3e1eed38f41b60201d6d7def9446c9f" "org.opencontainers.image.revision"="2945215ed3e1eed38f41b60201d6d7def9446c9f" "build-date"="2026-01-27T15:50:23Z" "org.opencontainers.image.created"="2026-01-27T15:50:23Z" "release"="1769521234"org.opencontainers.image.revision=2945215ed3e1eed38f41b60201d6d7def9446c9f,org.opencontainers.image.created=2026-01-27T15:50:23Z
# Wed, 28 Jan 2026 18:56:47 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 28 Jan 2026 18:56:47 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 28 Jan 2026 18:56:47 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 28 Jan 2026 18:56:47 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en         gnupg2     ;     microdnf clean all # buildkit
# Wed, 28 Jan 2026 18:56:47 GMT
ENV JAVA_VERSION=jdk-25.0.1+8
# Wed, 28 Jan 2026 19:01:36 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='5371ad922cb4ff571a57c8e5dd14485ebf5b3994cd71e6ea09088312de3bed71';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.1%2B8/OpenJDK25U-jre_aarch64_linux_hotspot_25.0.1_8.tar.gz';          ;;        ppc64le)          ESUM='c812bf806d7ffcd290c6bd814324aa81f0688e2d682fd0b87e2c7c76251a4f2c';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.1%2B8/OpenJDK25U-jre_ppc64le_linux_hotspot_25.0.1_8.tar.gz';          ;;        s390x)          ESUM='c58764b69cb70e7b532f50e8a20e74aa5cb65e85c3e500225e0b64719a6021a0';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.1%2B8/OpenJDK25U-jre_s390x_linux_hotspot_25.0.1_8.tar.gz';          ;;        x86_64)          ESUM='126c7f59b91df97b2e930b0a456422ce29af7f2385117e1c04297eba962b0b1c';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.1%2B8/OpenJDK25U-jre_x64_linux_hotspot_25.0.1_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz; # buildkit
# Wed, 28 Jan 2026 19:01:37 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 28 Jan 2026 19:01:38 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 28 Jan 2026 19:01:38 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
```

-	Layers:
	-	`sha256:ae80e80c08d44fa3239f0258ba6b08c404cdebc7b53393a151fa1f93bcf7bf6e`  
		Last Modified: Tue, 27 Jan 2026 18:12:32 GMT  
		Size: 38.6 MB (38638820 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a3882d9c01ea5c0cb5dd62cb2df6f92c42b9844d566e2f851eefbf5dc55868c`  
		Last Modified: Wed, 28 Jan 2026 18:57:36 GMT  
		Size: 39.1 MB (39126257 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6f77194bef86185a76287689ed2a2cf7703bed8f1403612dafc5a604a1427f4`  
		Last Modified: Wed, 28 Jan 2026 19:02:14 GMT  
		Size: 62.0 MB (62030719 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b31a672559f6b45fc44b8fab707fb7a40d872c7a328496c951591c5df9b65c6e`  
		Last Modified: Wed, 28 Jan 2026 19:02:07 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b591da3f7709a651574d0214a88d96389a15e881b628f2dc2117702b9ccc976d`  
		Last Modified: Wed, 28 Jan 2026 19:02:07 GMT  
		Size: 2.3 KB (2289 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:25-jre-ubi10-minimal` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:32d761e2cc84b3b2179360a401e3253d059a28235c1047c1877152cc42c0684c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3721278 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5bd0d89c930527a5a79732fb7c13f93b863706960bf5aaa9359b45a911d01d6b`

```dockerfile
```

-	Layers:
	-	`sha256:e3aceb8023c55a529a7cd573e781bac13dd2293d749139f2a78cd837cea0e6bd`  
		Last Modified: Wed, 28 Jan 2026 19:02:08 GMT  
		Size: 3.7 MB (3700918 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:79c9be85eb6c5451da552f88c733635cceb71848810fbed2a3efd9b4aae63ba3`  
		Last Modified: Wed, 28 Jan 2026 19:02:07 GMT  
		Size: 20.4 KB (20360 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-temurin:25-jre-ubi10-minimal` - linux; s390x

```console
$ docker pull eclipse-temurin@sha256:8e1aac04dd793a42bfbe95fcd88cfc38ca3f2b4b862eb7e6a5953d8c68e59301
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **135.0 MB (134954335 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:49ba57194689ead03249898db09ff0392fb4da426cdb4e8a57e04eda86b50ca4`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`

```dockerfile
# Tue, 27 Jan 2026 16:00:26 GMT
LABEL maintainer="Red Hat, Inc."
# Tue, 27 Jan 2026 16:00:26 GMT
LABEL vendor="Red Hat, Inc."
# Tue, 27 Jan 2026 16:00:26 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Tue, 27 Jan 2026 16:00:26 GMT
LABEL com.redhat.component="ubi10-minimal-container"       name="ubi10/ubi-minimal"       version="10.1"       cpe="cpe:/o:redhat:enterprise_linux:10.1"       distribution-scope="public"
# Tue, 27 Jan 2026 16:00:26 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Tue, 27 Jan 2026 16:00:26 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 10."
# Tue, 27 Jan 2026 16:00:26 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Tue, 27 Jan 2026 16:00:26 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Tue, 27 Jan 2026 16:00:26 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 10 Minimal"
# Tue, 27 Jan 2026 16:00:26 GMT
LABEL io.openshift.expose-services=""
# Tue, 27 Jan 2026 16:00:26 GMT
LABEL io.openshift.tags="minimal rhel10"
# Tue, 27 Jan 2026 16:00:26 GMT
ENV container oci
# Tue, 27 Jan 2026 16:00:27 GMT
COPY dir:4f1adb6a08f1772cc4a3a6f7fb169c42da3905eda1382dfd020cde9bf8ce54ed in /      
# Tue, 27 Jan 2026 16:00:27 GMT
COPY file:5de33b5fc08b00635bccf9134a18978dba13e2250aa51838f9969515a3957847 in /etc/yum.repos.d/.      
# Tue, 27 Jan 2026 16:00:27 GMT
CMD ["/bin/bash"]
# Tue, 27 Jan 2026 16:00:27 GMT
COPY file:595171150af68abc798ea385f7988d74b566aa8e84babff137f00b08b2164683 in /usr/share/buildinfo/content-sets.json      
# Tue, 27 Jan 2026 16:00:27 GMT
COPY file:595171150af68abc798ea385f7988d74b566aa8e84babff137f00b08b2164683 in /root/buildinfo/content_manifests/content-sets.json      
# Tue, 27 Jan 2026 16:00:27 GMT
COPY file:7d6813f56262fe28e046f6d0aae045479ae2fad09337cb7cdde0415772e612fe in /usr/share/buildinfo/labels.json      
# Tue, 27 Jan 2026 16:00:27 GMT
COPY file:7d6813f56262fe28e046f6d0aae045479ae2fad09337cb7cdde0415772e612fe in /root/buildinfo/labels.json      
# Tue, 27 Jan 2026 16:00:27 GMT
LABEL "architecture"="s390x" "vcs-type"="git" "vcs-ref"="2945215ed3e1eed38f41b60201d6d7def9446c9f" "org.opencontainers.image.revision"="2945215ed3e1eed38f41b60201d6d7def9446c9f" "build-date"="2026-01-27T15:58:08Z" "org.opencontainers.image.created"="2026-01-27T15:58:08Z" "release"="1769521234"org.opencontainers.image.revision=2945215ed3e1eed38f41b60201d6d7def9446c9f,org.opencontainers.image.created=2026-01-27T15:58:08Z
# Wed, 28 Jan 2026 18:57:03 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 28 Jan 2026 18:57:03 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 28 Jan 2026 18:57:03 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 28 Jan 2026 18:57:03 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en         gnupg2     ;     microdnf clean all # buildkit
# Wed, 28 Jan 2026 18:57:03 GMT
ENV JAVA_VERSION=jdk-25.0.1+8
# Wed, 28 Jan 2026 18:57:59 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='5371ad922cb4ff571a57c8e5dd14485ebf5b3994cd71e6ea09088312de3bed71';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.1%2B8/OpenJDK25U-jre_aarch64_linux_hotspot_25.0.1_8.tar.gz';          ;;        ppc64le)          ESUM='c812bf806d7ffcd290c6bd814324aa81f0688e2d682fd0b87e2c7c76251a4f2c';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.1%2B8/OpenJDK25U-jre_ppc64le_linux_hotspot_25.0.1_8.tar.gz';          ;;        s390x)          ESUM='c58764b69cb70e7b532f50e8a20e74aa5cb65e85c3e500225e0b64719a6021a0';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.1%2B8/OpenJDK25U-jre_s390x_linux_hotspot_25.0.1_8.tar.gz';          ;;        x86_64)          ESUM='126c7f59b91df97b2e930b0a456422ce29af7f2385117e1c04297eba962b0b1c';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.1%2B8/OpenJDK25U-jre_x64_linux_hotspot_25.0.1_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz; # buildkit
# Wed, 28 Jan 2026 18:57:59 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 28 Jan 2026 18:57:59 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 28 Jan 2026 18:57:59 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
```

-	Layers:
	-	`sha256:9d64b2731e63f62ba158833fc228878293975e79a79748090a59385ed70b4508`  
		Last Modified: Tue, 27 Jan 2026 18:12:24 GMT  
		Size: 34.4 MB (34372082 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fec036fcfe60084971e44fdfa9e8e4d4958b862be6f2c627225ff2410685c3ba`  
		Last Modified: Wed, 28 Jan 2026 18:57:29 GMT  
		Size: 40.4 MB (40364641 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94ec09a852c3f904ae1b06fdd01151a34068ddb1748a3a76fa81bb717f530c98`  
		Last Modified: Wed, 28 Jan 2026 18:58:23 GMT  
		Size: 60.2 MB (60215193 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b31d7746164d3ef4d695fd8833d2424e947f707eb0da2411bd8c5e84174c0684`  
		Last Modified: Wed, 28 Jan 2026 18:58:21 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6da355fb72b829b189c3c45fe3ddb07cfb96618cea44bef56f355880f9345093`  
		Last Modified: Wed, 28 Jan 2026 18:58:21 GMT  
		Size: 2.3 KB (2291 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:25-jre-ubi10-minimal` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:59689c6c3527d2b8077e19cd20b1276766a81d79e872980161ee77d17f8e4413
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3722493 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e93b9758fd100223fc25255c68f99d121ba57f5e2d32e94286a63cdc2ec92567`

```dockerfile
```

-	Layers:
	-	`sha256:3d6fcdd8a54a636e4529e575aa673d3d75eacdc8a9375a8515c97f3e0a08bfd9`  
		Last Modified: Wed, 28 Jan 2026 18:58:21 GMT  
		Size: 3.7 MB (3702163 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:43c07a98695865b6ed3adfa7ab39f204a408c55f3fbda76cc31cce9f62ea9bf9`  
		Last Modified: Wed, 28 Jan 2026 18:58:21 GMT  
		Size: 20.3 KB (20330 bytes)  
		MIME: application/vnd.in-toto+json
