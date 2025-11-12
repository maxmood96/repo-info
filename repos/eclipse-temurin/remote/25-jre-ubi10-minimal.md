## `eclipse-temurin:25-jre-ubi10-minimal`

```console
$ docker pull eclipse-temurin@sha256:d8a5660874834ae47cf464943a37544be05ae0f7ebc3ef2ed4b957b405ee152a
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
$ docker pull eclipse-temurin@sha256:6b4c56ebbcaf52b31a279015fe27eb6de24f1e9d263d289aea1b3aa6f5fc5aa0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **128.7 MB (128749915 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1becbf1cd96be3ca495c36ba67b6d2f180b661aa234d05f5beab2d50291233a7`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`

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
# Wed, 12 Nov 2025 00:28:25 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 12 Nov 2025 00:28:25 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 12 Nov 2025 00:28:25 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 12 Nov 2025 00:28:25 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en         gnupg2     ;     microdnf clean all # buildkit
# Wed, 12 Nov 2025 00:28:25 GMT
ENV JAVA_VERSION=jdk-25.0.1+8
# Wed, 12 Nov 2025 00:28:50 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='5371ad922cb4ff571a57c8e5dd14485ebf5b3994cd71e6ea09088312de3bed71';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.1%2B8/OpenJDK25U-jre_aarch64_linux_hotspot_25.0.1_8.tar.gz';          ;;        ppc64le)          ESUM='c812bf806d7ffcd290c6bd814324aa81f0688e2d682fd0b87e2c7c76251a4f2c';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.1%2B8/OpenJDK25U-jre_ppc64le_linux_hotspot_25.0.1_8.tar.gz';          ;;        s390x)          ESUM='c58764b69cb70e7b532f50e8a20e74aa5cb65e85c3e500225e0b64719a6021a0';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.1%2B8/OpenJDK25U-jre_s390x_linux_hotspot_25.0.1_8.tar.gz';          ;;        x86_64)          ESUM='126c7f59b91df97b2e930b0a456422ce29af7f2385117e1c04297eba962b0b1c';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.1%2B8/OpenJDK25U-jre_x64_linux_hotspot_25.0.1_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz; # buildkit
# Wed, 12 Nov 2025 00:28:50 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 12 Nov 2025 00:28:50 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 12 Nov 2025 00:28:50 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
```

-	Layers:
	-	`sha256:97d2336739ce8e6158d60016e45d04595e4f80b1d11dd60990e6748ac4fea4f0`  
		Last Modified: Tue, 11 Nov 2025 12:10:43 GMT  
		Size: 33.8 MB (33814455 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6722c287a68e41b04a9955790b5d2fac14f8eb6ccd583fa5b4a3d83473eb5896`  
		Last Modified: Wed, 12 Nov 2025 00:28:57 GMT  
		Size: 32.3 MB (32337080 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0030d67dcbadf6000261051752a5ee6e041eb612aed21d64d97a3de0d926a326`  
		Last Modified: Wed, 12 Nov 2025 00:29:17 GMT  
		Size: 62.6 MB (62595964 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f2fb6b78503be690e5bd2b10fc7babfea074f8caed92a2db03b3d5249b03885`  
		Last Modified: Wed, 12 Nov 2025 00:29:09 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f27eee4ac8e0861dafd40426bfeb5208d6ba2e53d6e0e32820a5acfd00487555`  
		Last Modified: Wed, 12 Nov 2025 00:29:10 GMT  
		Size: 2.3 KB (2290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:25-jre-ubi10-minimal` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:f658803eac38615fe51a09cf73782c58b36192af52da54757a53619696be4ec0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (3011175 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:83fefd14bf733a2193a9c318f851686d14ca287a197da495d0241655983c330a`

```dockerfile
```

-	Layers:
	-	`sha256:39e323cca238fb85b9faba7d265e80d82c1671fd133b65948f58c160505f34b1`  
		Last Modified: Wed, 12 Nov 2025 01:17:28 GMT  
		Size: 3.0 MB (2990845 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2995ddf6f7d7595012677fac771c108249807baf86b576fefb946f59e8fabc8d`  
		Last Modified: Wed, 12 Nov 2025 01:17:29 GMT  
		Size: 20.3 KB (20330 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-temurin:25-jre-ubi10-minimal` - linux; arm64 variant v8

```console
$ docker pull eclipse-temurin@sha256:7291ff45c74ecf312261ee75bf1b138d54f316af65b8a3b426d5fd98649445b9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **153.0 MB (153007068 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f12811e6332e603c770ecef118fafc45605d4926af99553d74947f401dc0236`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`

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
# Mon, 10 Nov 2025 20:14:15 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 10 Nov 2025 20:14:15 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 10 Nov 2025 20:14:15 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 10 Nov 2025 20:14:15 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en         gnupg2     ;     microdnf clean all # buildkit
# Mon, 10 Nov 2025 20:14:15 GMT
ENV JAVA_VERSION=jdk-25.0.1+8
# Mon, 10 Nov 2025 20:15:18 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='5371ad922cb4ff571a57c8e5dd14485ebf5b3994cd71e6ea09088312de3bed71';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.1%2B8/OpenJDK25U-jre_aarch64_linux_hotspot_25.0.1_8.tar.gz';          ;;        ppc64le)          ESUM='c812bf806d7ffcd290c6bd814324aa81f0688e2d682fd0b87e2c7c76251a4f2c';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.1%2B8/OpenJDK25U-jre_ppc64le_linux_hotspot_25.0.1_8.tar.gz';          ;;        s390x)          ESUM='c58764b69cb70e7b532f50e8a20e74aa5cb65e85c3e500225e0b64719a6021a0';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.1%2B8/OpenJDK25U-jre_s390x_linux_hotspot_25.0.1_8.tar.gz';          ;;        x86_64)          ESUM='126c7f59b91df97b2e930b0a456422ce29af7f2385117e1c04297eba962b0b1c';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.1%2B8/OpenJDK25U-jre_x64_linux_hotspot_25.0.1_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz; # buildkit
# Mon, 10 Nov 2025 20:15:18 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Mon, 10 Nov 2025 20:15:18 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Mon, 10 Nov 2025 20:15:18 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
```

-	Layers:
	-	`sha256:bcfce2f653765e7fbc0157676a8995e7c79e4d29c562744818763bd665844191`  
		Last Modified: Mon, 10 Nov 2025 12:11:55 GMT  
		Size: 31.6 MB (31555554 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7137d12faf649745198d2dd94cffa0a18516d5f53ceb1050b83d5f6d1b8b3410`  
		Last Modified: Mon, 10 Nov 2025 20:14:51 GMT  
		Size: 59.9 MB (59906018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7389f0e0524f51e7a347d4c2ace964c82146060fa191ac14ea0bbbe68328216`  
		Last Modified: Mon, 10 Nov 2025 20:15:45 GMT  
		Size: 61.5 MB (61543077 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:030fe0b97deff8b511d22c7096466e8bc0cd29964a1e6de7fedf0ebbf55bca1d`  
		Last Modified: Mon, 10 Nov 2025 20:15:41 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fa946b745543981b2074e9032e441a1cadc1a5efebe70705bc1c61c7e9e971c`  
		Last Modified: Mon, 10 Nov 2025 20:15:41 GMT  
		Size: 2.3 KB (2291 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:25-jre-ubi10-minimal` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:82d0c9adf3d0c80e3f1b92ad71c288e78ff101dd78414d10371f27858d5c774e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5618788 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e463393086be5a7a057d757bedf941de98dc3230252f4b2b2fc62c61f2383821`

```dockerfile
```

-	Layers:
	-	`sha256:d4c31ff6fc375ee39c89e8484fe037344499fac8c79e32e9bf108beebbe6b6ad`  
		Last Modified: Mon, 10 Nov 2025 22:16:04 GMT  
		Size: 5.6 MB (5598354 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d4651ba49627c2aef51e4cedf8428e2c5ac02032b7de074e39457b5e4d3d18b9`  
		Last Modified: Mon, 10 Nov 2025 22:16:05 GMT  
		Size: 20.4 KB (20434 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-temurin:25-jre-ubi10-minimal` - linux; ppc64le

```console
$ docker pull eclipse-temurin@sha256:430d30eacd651bf3e5f75a7194918f5a0b080530b4e68478b25ac5983317ee57
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.6 MB (134611206 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:94091ec485734cb1f9319dbe8200e9ad9cf92f6c3c9033f7b5b7fb2dabbeb072`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`

```dockerfile
# Tue, 11 Nov 2025 09:46:38 GMT
LABEL maintainer="Red Hat, Inc."
# Tue, 11 Nov 2025 09:46:38 GMT
LABEL vendor="Red Hat, Inc."
# Tue, 11 Nov 2025 09:46:38 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Tue, 11 Nov 2025 09:46:38 GMT
LABEL com.redhat.component="ubi10-minimal-container"       name="ubi10/ubi-minimal"       version="10.0"       cpe="cpe:/o:redhat:enterprise_linux:10.0"       distribution-scope="public"
# Tue, 11 Nov 2025 09:46:38 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Tue, 11 Nov 2025 09:46:38 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 10."
# Tue, 11 Nov 2025 09:46:38 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Tue, 11 Nov 2025 09:46:38 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Tue, 11 Nov 2025 09:46:38 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 10 Minimal"
# Tue, 11 Nov 2025 09:46:38 GMT
LABEL io.openshift.expose-services=""
# Tue, 11 Nov 2025 09:46:38 GMT
LABEL io.openshift.tags="minimal rhel10"
# Tue, 11 Nov 2025 09:46:38 GMT
ENV container oci
# Tue, 11 Nov 2025 09:46:38 GMT
COPY dir:9eff4e38dcc190900aead322c6b5d4b07dfedc6eaef5a1d45538bdb73a45f14d in /      
# Tue, 11 Nov 2025 09:46:39 GMT
COPY file:5de33b5fc08b00635bccf9134a18978dba13e2250aa51838f9969515a3957847 in /etc/yum.repos.d/.      
# Tue, 11 Nov 2025 09:46:39 GMT
CMD ["/bin/bash"]
# Tue, 11 Nov 2025 09:46:39 GMT
COPY file:595171150af68abc798ea385f7988d74b566aa8e84babff137f00b08b2164683 in /usr/share/buildinfo/content-sets.json      
# Tue, 11 Nov 2025 09:46:39 GMT
COPY file:595171150af68abc798ea385f7988d74b566aa8e84babff137f00b08b2164683 in /root/buildinfo/content_manifests/content-sets.json      
# Tue, 11 Nov 2025 09:46:39 GMT
COPY file:5560f9de0cd27b658b5fcbd57b28e53dd717804f3fa1835c47d63e629ad7d5b3 in /usr/share/buildinfo/labels.json      
# Tue, 11 Nov 2025 09:46:39 GMT
COPY file:5560f9de0cd27b658b5fcbd57b28e53dd717804f3fa1835c47d63e629ad7d5b3 in /root/buildinfo/labels.json      
# Tue, 11 Nov 2025 09:46:39 GMT
LABEL "architecture"="ppc64le" "vcs-type"="git" "vcs-ref"="0a583d401ee29f56bb3786d762c71b4349cd93d9" "org.opencontainers.image.revision"="0a583d401ee29f56bb3786d762c71b4349cd93d9" "build-date"="2025-11-11T09:46:27Z" "release"="1762851739"org.opencontainers.image.revision=0a583d401ee29f56bb3786d762c71b4349cd93d9
# Wed, 12 Nov 2025 00:25:28 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 12 Nov 2025 00:25:28 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 12 Nov 2025 00:25:28 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 12 Nov 2025 00:25:28 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en         gnupg2     ;     microdnf clean all # buildkit
# Wed, 12 Nov 2025 00:25:28 GMT
ENV JAVA_VERSION=jdk-25.0.1+8
# Wed, 12 Nov 2025 00:42:27 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='5371ad922cb4ff571a57c8e5dd14485ebf5b3994cd71e6ea09088312de3bed71';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.1%2B8/OpenJDK25U-jre_aarch64_linux_hotspot_25.0.1_8.tar.gz';          ;;        ppc64le)          ESUM='c812bf806d7ffcd290c6bd814324aa81f0688e2d682fd0b87e2c7c76251a4f2c';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.1%2B8/OpenJDK25U-jre_ppc64le_linux_hotspot_25.0.1_8.tar.gz';          ;;        s390x)          ESUM='c58764b69cb70e7b532f50e8a20e74aa5cb65e85c3e500225e0b64719a6021a0';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.1%2B8/OpenJDK25U-jre_s390x_linux_hotspot_25.0.1_8.tar.gz';          ;;        x86_64)          ESUM='126c7f59b91df97b2e930b0a456422ce29af7f2385117e1c04297eba962b0b1c';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.1%2B8/OpenJDK25U-jre_x64_linux_hotspot_25.0.1_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz; # buildkit
# Wed, 12 Nov 2025 00:42:28 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 12 Nov 2025 00:42:28 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 12 Nov 2025 00:42:28 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
```

-	Layers:
	-	`sha256:313f119ed94e0e93e4e07bcb4d3db80804a7bc9d20c291facac59a8ea7e2c521`  
		Last Modified: Tue, 11 Nov 2025 12:10:55 GMT  
		Size: 37.2 MB (37214430 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf04b7e6936b169feac64de9cb456185ed1148dc31d8014c6000367570a87d21`  
		Last Modified: Wed, 12 Nov 2025 00:26:27 GMT  
		Size: 35.4 MB (35363634 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a03bb8a948ceada94781e03f361e3fd2b83baa61b74e03380dea84350932a7d`  
		Last Modified: Wed, 12 Nov 2025 00:43:22 GMT  
		Size: 62.0 MB (62030722 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6be897ec36267d755763b9a46a6599eb73964509ad9f358bbc29d58e6712ea3`  
		Last Modified: Wed, 12 Nov 2025 00:43:09 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:378dcd7f033bb215c44fe3ad39df7cbb4af4fd635195d811c6c85b6e6844212a`  
		Last Modified: Wed, 12 Nov 2025 00:43:09 GMT  
		Size: 2.3 KB (2292 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:25-jre-ubi10-minimal` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:d96b673e2ff5d6ffd2b74e2b8658bf3e7c2afbc491db7adfb41e3a31eca8cfc4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (3006252 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:29ac39d3a2e0a1841c760d1adf872b65be7da143225d308576196ad613e0462a`

```dockerfile
```

-	Layers:
	-	`sha256:78d2b46cb188335a4d1fb8ee130dafe6a74de33f2061ec84eb00c3fd642624f1`  
		Last Modified: Wed, 12 Nov 2025 01:17:39 GMT  
		Size: 3.0 MB (2985893 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0d2f9d134cef6f4b619adbec02cc1c00e9bb85f7071fa866bfb36f0b1bd7bfac`  
		Last Modified: Wed, 12 Nov 2025 01:17:40 GMT  
		Size: 20.4 KB (20359 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-temurin:25-jre-ubi10-minimal` - linux; s390x

```console
$ docker pull eclipse-temurin@sha256:584539267783bd9cee4d1b8077a920f8318f0692fe256f1f6292f2f5fa97a2b3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **125.7 MB (125670235 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:815a0a56e26dc738bb0e7c823e748a804e85eedf7bd17199d1b5d877c570dd35`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`

```dockerfile
# Tue, 11 Nov 2025 09:53:25 GMT
LABEL maintainer="Red Hat, Inc."
# Tue, 11 Nov 2025 09:53:25 GMT
LABEL vendor="Red Hat, Inc."
# Tue, 11 Nov 2025 09:53:25 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Tue, 11 Nov 2025 09:53:25 GMT
LABEL com.redhat.component="ubi10-minimal-container"       name="ubi10/ubi-minimal"       version="10.0"       cpe="cpe:/o:redhat:enterprise_linux:10.0"       distribution-scope="public"
# Tue, 11 Nov 2025 09:53:25 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Tue, 11 Nov 2025 09:53:25 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 10."
# Tue, 11 Nov 2025 09:53:25 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Tue, 11 Nov 2025 09:53:26 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Tue, 11 Nov 2025 09:53:26 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 10 Minimal"
# Tue, 11 Nov 2025 09:53:26 GMT
LABEL io.openshift.expose-services=""
# Tue, 11 Nov 2025 09:53:26 GMT
LABEL io.openshift.tags="minimal rhel10"
# Tue, 11 Nov 2025 09:53:26 GMT
ENV container oci
# Tue, 11 Nov 2025 09:53:26 GMT
COPY dir:9f1f5449cb9454b7c05550f990009868329830ff5f598e41882e09b2985f76ce in /      
# Tue, 11 Nov 2025 09:53:26 GMT
COPY file:5de33b5fc08b00635bccf9134a18978dba13e2250aa51838f9969515a3957847 in /etc/yum.repos.d/.      
# Tue, 11 Nov 2025 09:53:26 GMT
CMD ["/bin/bash"]
# Tue, 11 Nov 2025 09:53:26 GMT
COPY file:595171150af68abc798ea385f7988d74b566aa8e84babff137f00b08b2164683 in /usr/share/buildinfo/content-sets.json      
# Tue, 11 Nov 2025 09:53:26 GMT
COPY file:595171150af68abc798ea385f7988d74b566aa8e84babff137f00b08b2164683 in /root/buildinfo/content_manifests/content-sets.json      
# Tue, 11 Nov 2025 09:53:27 GMT
COPY file:d3b5fde18206481b740a53df7391a42dcce042cfdd4edd5afeeb9637f6b9111a in /usr/share/buildinfo/labels.json      
# Tue, 11 Nov 2025 09:53:27 GMT
COPY file:d3b5fde18206481b740a53df7391a42dcce042cfdd4edd5afeeb9637f6b9111a in /root/buildinfo/labels.json      
# Tue, 11 Nov 2025 09:53:27 GMT
LABEL "architecture"="s390x" "vcs-type"="git" "vcs-ref"="0a583d401ee29f56bb3786d762c71b4349cd93d9" "org.opencontainers.image.revision"="0a583d401ee29f56bb3786d762c71b4349cd93d9" "build-date"="2025-11-11T09:51:11Z" "release"="1762851739"org.opencontainers.image.revision=0a583d401ee29f56bb3786d762c71b4349cd93d9
# Wed, 12 Nov 2025 00:25:26 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 12 Nov 2025 00:25:26 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 12 Nov 2025 00:25:26 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 12 Nov 2025 00:25:26 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en         gnupg2     ;     microdnf clean all # buildkit
# Wed, 12 Nov 2025 00:25:26 GMT
ENV JAVA_VERSION=jdk-25.0.1+8
# Wed, 12 Nov 2025 00:44:24 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='5371ad922cb4ff571a57c8e5dd14485ebf5b3994cd71e6ea09088312de3bed71';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.1%2B8/OpenJDK25U-jre_aarch64_linux_hotspot_25.0.1_8.tar.gz';          ;;        ppc64le)          ESUM='c812bf806d7ffcd290c6bd814324aa81f0688e2d682fd0b87e2c7c76251a4f2c';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.1%2B8/OpenJDK25U-jre_ppc64le_linux_hotspot_25.0.1_8.tar.gz';          ;;        s390x)          ESUM='c58764b69cb70e7b532f50e8a20e74aa5cb65e85c3e500225e0b64719a6021a0';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.1%2B8/OpenJDK25U-jre_s390x_linux_hotspot_25.0.1_8.tar.gz';          ;;        x86_64)          ESUM='126c7f59b91df97b2e930b0a456422ce29af7f2385117e1c04297eba962b0b1c';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.1%2B8/OpenJDK25U-jre_x64_linux_hotspot_25.0.1_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz; # buildkit
# Wed, 12 Nov 2025 00:44:25 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 12 Nov 2025 00:44:26 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 12 Nov 2025 00:44:26 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
```

-	Layers:
	-	`sha256:1276be387a6a7c4ba51d350a6bfba6a1c72fe42d07414791e01dad4ca06bc732`  
		Last Modified: Tue, 11 Nov 2025 12:10:44 GMT  
		Size: 33.8 MB (33797474 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f94e9c54bbb60d78e3a1b2c270640fe5278b731547a8566cca26aacb7fbf74d5`  
		Last Modified: Wed, 12 Nov 2025 00:26:59 GMT  
		Size: 31.7 MB (31655122 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd7ec9c3ce14e48a5fcc7b4a37a84f8b222e7334a58456d098ed253c9d28f666`  
		Last Modified: Wed, 12 Nov 2025 00:45:22 GMT  
		Size: 60.2 MB (60215219 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb2f8f4b904ef56e184ca58a5dd80c5f620ded8712cb45cef96178367820c4e0`  
		Last Modified: Wed, 12 Nov 2025 00:45:14 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc2b20254c91c4e6d4d4b9a78d94b377bb1725888b08e69beb125cc8ce34f5d1`  
		Last Modified: Wed, 12 Nov 2025 00:45:15 GMT  
		Size: 2.3 KB (2292 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:25-jre-ubi10-minimal` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:2d0fb48a9cbee4d0d99862622448eb8216a68866adf511478ae0ac2a44f14bae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (3007468 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:42c46eee3db2d925f23110f31dc950e9aa8ff8ab9f2c3acbe33db3252b5e4992`

```dockerfile
```

-	Layers:
	-	`sha256:771de72dad05dbd59ce1c96d89a582413f30e3d20a99ecd54c5a2d1b6aba8fe2`  
		Last Modified: Wed, 12 Nov 2025 01:17:45 GMT  
		Size: 3.0 MB (2987138 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6978cc9b47c3136d7d9a0f4635ed86fabdfa6285a8048ef74af07ffd2f85df1a`  
		Last Modified: Wed, 12 Nov 2025 01:17:45 GMT  
		Size: 20.3 KB (20330 bytes)  
		MIME: application/vnd.in-toto+json
