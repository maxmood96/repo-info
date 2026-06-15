## `eclipse-temurin:8-jdk-ubi10-minimal`

```console
$ docker pull eclipse-temurin@sha256:98995abf92010abad9596ab91579f2204bc0bb16397500c4f514bc8de59a9705
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `eclipse-temurin:8-jdk-ubi10-minimal` - linux; amd64

```console
$ docker pull eclipse-temurin@sha256:55f893cc4da6a70d38d5f6b7a17fd2f0cf941cb0a0cfdff8aa413bd1feaa8c07
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.8 MB (127817100 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:15e013f397405107416febd6e8efd3f14f33bdfce98ca63e6ead4dbf43dd499a`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`

```dockerfile
# Thu, 04 Jun 2026 05:28:17 GMT
LABEL maintainer="Red Hat, Inc."
# Thu, 04 Jun 2026 05:28:17 GMT
LABEL vendor="Red Hat, Inc."
# Thu, 04 Jun 2026 05:28:17 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Thu, 04 Jun 2026 05:28:17 GMT
LABEL com.redhat.component="ubi10-minimal-container"       name="ubi10/ubi-minimal"       version="10.2"       cpe="cpe:/o:redhat:enterprise_linux:10.2"       distribution-scope="public"
# Thu, 04 Jun 2026 05:28:17 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Thu, 04 Jun 2026 05:28:17 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 10."
# Thu, 04 Jun 2026 05:28:17 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 04 Jun 2026 05:28:17 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 04 Jun 2026 05:28:17 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 10 Minimal"
# Thu, 04 Jun 2026 05:28:17 GMT
LABEL io.openshift.expose-services=""
# Thu, 04 Jun 2026 05:28:17 GMT
LABEL io.openshift.tags="minimal rhel10"
# Thu, 04 Jun 2026 05:28:17 GMT
ENV container oci
# Thu, 04 Jun 2026 05:28:18 GMT
COPY dir:66f2b108fa49d46a69e413fb7db9e6ed9263f39ff05950d04e99329222ef439c in /      
# Thu, 04 Jun 2026 05:28:18 GMT
COPY file:5de33b5fc08b00635bccf9134a18978dba13e2250aa51838f9969515a3957847 in /etc/yum.repos.d/.      
# Thu, 04 Jun 2026 05:28:18 GMT
CMD ["/bin/bash"]
# Thu, 04 Jun 2026 05:28:18 GMT
COPY file:595171150af68abc798ea385f7988d74b566aa8e84babff137f00b08b2164683 in /usr/share/buildinfo/content-sets.json      
# Thu, 04 Jun 2026 05:28:18 GMT
COPY file:595171150af68abc798ea385f7988d74b566aa8e84babff137f00b08b2164683 in /root/buildinfo/content_manifests/content-sets.json      
# Thu, 04 Jun 2026 05:28:18 GMT
COPY file:fd262bedfa32870622b193d94f9285fa7e55dee323c33ad89ff9af707ddb8c11 in /usr/share/buildinfo/labels.json      
# Thu, 04 Jun 2026 05:28:18 GMT
COPY file:fd262bedfa32870622b193d94f9285fa7e55dee323c33ad89ff9af707ddb8c11 in /root/buildinfo/labels.json      
# Thu, 04 Jun 2026 05:28:18 GMT
LABEL "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="21e748607cdf3bfe567bea40c2e0c654a3c7766c" "org.opencontainers.image.revision"="21e748607cdf3bfe567bea40c2e0c654a3c7766c" "build-date"="2026-06-04T05:28:04Z" "org.opencontainers.image.created"="2026-06-04T05:28:04Z" "release"="1780550715"org.opencontainers.image.revision=21e748607cdf3bfe567bea40c2e0c654a3c7766c,org.opencontainers.image.created=2026-06-04T05:28:04Z
# Fri, 05 Jun 2026 22:42:35 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 05 Jun 2026 22:42:35 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 05 Jun 2026 22:42:35 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 05 Jun 2026 22:42:35 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en         gnupg2     ;     microdnf clean all # buildkit
# Fri, 05 Jun 2026 22:42:35 GMT
ENV JAVA_VERSION=jdk8u492-b09
# Fri, 05 Jun 2026 22:42:39 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='3c2253b986909c20f79d6de7a0cb957f89c243df57615897836046e24d2e5257';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u492-b09/OpenJDK8U-jdk_aarch64_linux_hotspot_8u492b09.tar.gz';          ;;        ppc64le)          ESUM='867e477e0a54159c7b774c55cfb046767120b1de43f705fa775ece74ea39e341';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u492-b09/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u492b09.tar.gz';          ;;        x86_64)          ESUM='da257f161d7f8c6ca5b0e5d9e4090f65ac28c5e398072e68b8ae87988b1d1a2e';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u492-b09/OpenJDK8U-jdk_x64_linux_hotspot_8u492b09.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip; # buildkit
# Fri, 05 Jun 2026 22:42:39 GMT
RUN set -eux;     echo "Verifying install ...";     echo "javac -version"; javac -version;     echo "java -version"; java -version;     echo "Complete." # buildkit
# Fri, 05 Jun 2026 22:42:39 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Fri, 05 Jun 2026 22:42:39 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
```

-	Layers:
	-	`sha256:39798aa98bd37b2e4ff77c414dd42bca72e522aa2cb338296f10696a239cb2b2`  
		Last Modified: Thu, 04 Jun 2026 06:53:25 GMT  
		Size: 34.9 MB (34854739 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38e4e7fb79039e32f144680cddeca9d1aa30eb34e7e1ae396f3ca18fe20f2007`  
		Last Modified: Fri, 05 Jun 2026 22:42:53 GMT  
		Size: 37.8 MB (37760588 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99d522909d68e6d8b57716e1fe3f89f8e4095591be1c20713f676071459a1c21`  
		Last Modified: Fri, 05 Jun 2026 22:42:54 GMT  
		Size: 55.2 MB (55199158 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6fdeb95ca00e44154d56e6358495ef8485fd27876409d14625f3a0e787ea0f1`  
		Last Modified: Fri, 05 Jun 2026 22:42:51 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f36a79085776b952a3b7c1812243f17bc468de4c47762554fa8b4a4bfb8b2fe1`  
		Last Modified: Fri, 05 Jun 2026 22:42:52 GMT  
		Size: 2.5 KB (2489 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:8-jdk-ubi10-minimal` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:c6a6ea1071d1decfd026c78cf25c7e5043aeb3e86bfb12d60fb71c98e56609c9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3932753 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:82064d1e3b320e52b9837554ad1b01d030dfd472c53d06489dab52ae31fb4f1e`

```dockerfile
```

-	Layers:
	-	`sha256:28c44da8e1f42501f0fdd25c1b8387372fa947ea0618aed4826cf4377a27177a`  
		Last Modified: Fri, 05 Jun 2026 22:42:51 GMT  
		Size: 3.9 MB (3912715 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:26e95130a2af5cad51ea0161618a7af032dcc4d66e53251ba4828664ba8da820`  
		Last Modified: Fri, 05 Jun 2026 22:42:51 GMT  
		Size: 20.0 KB (20038 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-temurin:8-jdk-ubi10-minimal` - linux; arm64 variant v8

```console
$ docker pull eclipse-temurin@sha256:16c85aebb63acdf2891fff38b9bbf0f1bb0fa643b92db0249e37bf0bc0bb7e2a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **125.0 MB (124992898 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:19fe96460cc62171169d19e7320108e4d3e31c5fd86e78a4c6d3e70fc217c548`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`

```dockerfile
# Mon, 15 Jun 2026 07:49:48 GMT
LABEL maintainer="Red Hat, Inc."
# Mon, 15 Jun 2026 07:49:48 GMT
LABEL vendor="Red Hat, Inc."
# Mon, 15 Jun 2026 07:49:48 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Mon, 15 Jun 2026 07:49:48 GMT
LABEL com.redhat.component="ubi10-minimal-container"       name="ubi10/ubi-minimal"       version="10.2"       cpe="cpe:/o:redhat:enterprise_linux:10.2"       distribution-scope="public"
# Mon, 15 Jun 2026 07:49:48 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Mon, 15 Jun 2026 07:49:48 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 10."
# Mon, 15 Jun 2026 07:49:49 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 15 Jun 2026 07:49:49 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 15 Jun 2026 07:49:49 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 10 Minimal"
# Mon, 15 Jun 2026 07:49:49 GMT
LABEL io.openshift.expose-services=""
# Mon, 15 Jun 2026 07:49:49 GMT
LABEL io.openshift.tags="minimal rhel10"
# Mon, 15 Jun 2026 07:49:49 GMT
ENV container oci
# Mon, 15 Jun 2026 07:49:49 GMT
COPY dir:96cf4a952c323db93c5acbd83a80198d6d4c582c6075283779408766bc1f06a0 in /      
# Mon, 15 Jun 2026 07:49:49 GMT
COPY file:5de33b5fc08b00635bccf9134a18978dba13e2250aa51838f9969515a3957847 in /etc/yum.repos.d/.      
# Mon, 15 Jun 2026 07:49:50 GMT
CMD ["/bin/bash"]
# Mon, 15 Jun 2026 07:49:50 GMT
COPY file:595171150af68abc798ea385f7988d74b566aa8e84babff137f00b08b2164683 in /usr/share/buildinfo/content-sets.json      
# Mon, 15 Jun 2026 07:49:50 GMT
COPY file:595171150af68abc798ea385f7988d74b566aa8e84babff137f00b08b2164683 in /root/buildinfo/content_manifests/content-sets.json      
# Mon, 15 Jun 2026 07:49:50 GMT
COPY file:d017e9e035ec2f71c8ca63bbb7b57216ba5aad41669dc424f097659ae0649922 in /usr/share/buildinfo/labels.json      
# Mon, 15 Jun 2026 07:49:50 GMT
COPY file:d017e9e035ec2f71c8ca63bbb7b57216ba5aad41669dc424f097659ae0649922 in /root/buildinfo/labels.json      
# Mon, 15 Jun 2026 07:49:50 GMT
LABEL "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="a079bd1cc91523a60704cf840463d737ba8b63de" "org.opencontainers.image.revision"="a079bd1cc91523a60704cf840463d737ba8b63de" "build-date"="2026-06-15T07:49:33Z" "org.opencontainers.image.created"="2026-06-15T07:49:33Z" "release"="1781509346"org.opencontainers.image.revision=a079bd1cc91523a60704cf840463d737ba8b63de,org.opencontainers.image.created=2026-06-15T07:49:33Z
# Mon, 15 Jun 2026 23:13:14 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 15 Jun 2026 23:13:14 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 15 Jun 2026 23:13:14 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 15 Jun 2026 23:13:14 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en         gnupg2     ;     microdnf clean all # buildkit
# Mon, 15 Jun 2026 23:13:14 GMT
ENV JAVA_VERSION=jdk8u492-b09
# Mon, 15 Jun 2026 23:13:18 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='3c2253b986909c20f79d6de7a0cb957f89c243df57615897836046e24d2e5257';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u492-b09/OpenJDK8U-jdk_aarch64_linux_hotspot_8u492b09.tar.gz';          ;;        ppc64le)          ESUM='867e477e0a54159c7b774c55cfb046767120b1de43f705fa775ece74ea39e341';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u492-b09/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u492b09.tar.gz';          ;;        x86_64)          ESUM='da257f161d7f8c6ca5b0e5d9e4090f65ac28c5e398072e68b8ae87988b1d1a2e';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u492-b09/OpenJDK8U-jdk_x64_linux_hotspot_8u492b09.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip; # buildkit
# Mon, 15 Jun 2026 23:13:18 GMT
RUN set -eux;     echo "Verifying install ...";     echo "javac -version"; javac -version;     echo "java -version"; java -version;     echo "Complete." # buildkit
# Mon, 15 Jun 2026 23:13:18 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Mon, 15 Jun 2026 23:13:18 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
```

-	Layers:
	-	`sha256:2181b76d100cfec8fecaf70c9c757671f616064b9f875b0fb509a7b6a6788ac5`  
		Last Modified: Mon, 15 Jun 2026 09:25:44 GMT  
		Size: 33.0 MB (33030316 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d77be5ab4486c50b066d6767d2553495020dc6532a6d9f87269f718bd482b5b7`  
		Last Modified: Mon, 15 Jun 2026 23:13:33 GMT  
		Size: 37.7 MB (37686528 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1bd75f0d05790162e97b4a4a6b10070d4c6590f4dafb7b1a5a8482e7d281b756`  
		Last Modified: Mon, 15 Jun 2026 23:13:34 GMT  
		Size: 54.3 MB (54273435 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e32c810d54b99729b95914e9e53fa2b69d3da49001fff13a8245c23c8db8d0fd`  
		Last Modified: Mon, 15 Jun 2026 23:13:32 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bea3eaaadf948682b62a44ffa1d6ce61aff4c300efd999d3c4316340d971299`  
		Last Modified: Mon, 15 Jun 2026 23:13:32 GMT  
		Size: 2.5 KB (2491 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:8-jdk-ubi10-minimal` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:69f26551d68257ed678b928643d000cddc3152e2fb8fea8e90e2da4860ffd4a2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3932996 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f7273644a9f928ff0960a67eedb6b288bd1fd2f9e4295ab4b5f5d2e26f8d1e9`

```dockerfile
```

-	Layers:
	-	`sha256:9fa1c1f782e2e897eb983d98286e1de8d648d5fe06eb5aaed7ddfe1d9d9aa321`  
		Last Modified: Mon, 15 Jun 2026 23:13:32 GMT  
		Size: 3.9 MB (3912841 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:76743a440a402d6f4caa8d83596046db2898edf495da97ff8178241bad893b37`  
		Last Modified: Mon, 15 Jun 2026 23:13:32 GMT  
		Size: 20.2 KB (20155 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-temurin:8-jdk-ubi10-minimal` - linux; ppc64le

```console
$ docker pull eclipse-temurin@sha256:739780e9ac484c6f2ad495ede9faedbfba3e0fb6ad8444f67d8dcc93f8993c27
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **131.2 MB (131231725 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:957ea55894e29f3e5f182b552a3480e01531330811b018966a584c626989bd86`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`

```dockerfile
# Mon, 15 Jun 2026 07:46:33 GMT
LABEL maintainer="Red Hat, Inc."
# Mon, 15 Jun 2026 07:46:33 GMT
LABEL vendor="Red Hat, Inc."
# Mon, 15 Jun 2026 07:46:33 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Mon, 15 Jun 2026 07:46:33 GMT
LABEL com.redhat.component="ubi10-minimal-container"       name="ubi10/ubi-minimal"       version="10.2"       cpe="cpe:/o:redhat:enterprise_linux:10.2"       distribution-scope="public"
# Mon, 15 Jun 2026 07:46:33 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Mon, 15 Jun 2026 07:46:33 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 10."
# Mon, 15 Jun 2026 07:46:33 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 15 Jun 2026 07:46:33 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 15 Jun 2026 07:46:33 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 10 Minimal"
# Mon, 15 Jun 2026 07:46:33 GMT
LABEL io.openshift.expose-services=""
# Mon, 15 Jun 2026 07:46:33 GMT
LABEL io.openshift.tags="minimal rhel10"
# Mon, 15 Jun 2026 07:46:33 GMT
ENV container oci
# Mon, 15 Jun 2026 07:46:34 GMT
COPY dir:83033203513f54fa7ad30157591855861b9bdeeadfcfaa7b39d928026e30a43e in /      
# Mon, 15 Jun 2026 07:46:34 GMT
COPY file:5de33b5fc08b00635bccf9134a18978dba13e2250aa51838f9969515a3957847 in /etc/yum.repos.d/.      
# Mon, 15 Jun 2026 07:46:34 GMT
CMD ["/bin/bash"]
# Mon, 15 Jun 2026 07:46:34 GMT
COPY file:595171150af68abc798ea385f7988d74b566aa8e84babff137f00b08b2164683 in /usr/share/buildinfo/content-sets.json      
# Mon, 15 Jun 2026 07:46:34 GMT
COPY file:595171150af68abc798ea385f7988d74b566aa8e84babff137f00b08b2164683 in /root/buildinfo/content_manifests/content-sets.json      
# Mon, 15 Jun 2026 07:46:34 GMT
COPY file:947556a1605dd2da1e7f452e2373e0e1a5352a517c46fbfad7c39a76efb34831 in /usr/share/buildinfo/labels.json      
# Mon, 15 Jun 2026 07:46:34 GMT
COPY file:947556a1605dd2da1e7f452e2373e0e1a5352a517c46fbfad7c39a76efb34831 in /root/buildinfo/labels.json      
# Mon, 15 Jun 2026 07:46:34 GMT
LABEL "architecture"="ppc64le" "vcs-type"="git" "vcs-ref"="a079bd1cc91523a60704cf840463d737ba8b63de" "org.opencontainers.image.revision"="a079bd1cc91523a60704cf840463d737ba8b63de" "build-date"="2026-06-15T07:46:22Z" "org.opencontainers.image.created"="2026-06-15T07:46:22Z" "release"="1781509346"org.opencontainers.image.revision=a079bd1cc91523a60704cf840463d737ba8b63de,org.opencontainers.image.created=2026-06-15T07:46:22Z
# Mon, 15 Jun 2026 23:14:23 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 15 Jun 2026 23:14:23 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 15 Jun 2026 23:14:23 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 15 Jun 2026 23:14:23 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en         gnupg2     ;     microdnf clean all # buildkit
# Mon, 15 Jun 2026 23:14:23 GMT
ENV JAVA_VERSION=jdk8u492-b09
# Mon, 15 Jun 2026 23:14:29 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='3c2253b986909c20f79d6de7a0cb957f89c243df57615897836046e24d2e5257';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u492-b09/OpenJDK8U-jdk_aarch64_linux_hotspot_8u492b09.tar.gz';          ;;        ppc64le)          ESUM='867e477e0a54159c7b774c55cfb046767120b1de43f705fa775ece74ea39e341';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u492-b09/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u492b09.tar.gz';          ;;        x86_64)          ESUM='da257f161d7f8c6ca5b0e5d9e4090f65ac28c5e398072e68b8ae87988b1d1a2e';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u492-b09/OpenJDK8U-jdk_x64_linux_hotspot_8u492b09.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip; # buildkit
# Mon, 15 Jun 2026 23:14:30 GMT
RUN set -eux;     echo "Verifying install ...";     echo "javac -version"; javac -version;     echo "java -version"; java -version;     echo "Complete." # buildkit
# Mon, 15 Jun 2026 23:14:30 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Mon, 15 Jun 2026 23:14:30 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
```

-	Layers:
	-	`sha256:2228c93141e55e5881a02fe1a8f242a1e8a66f3a905f628abec2236bd3b86b02`  
		Last Modified: Mon, 15 Jun 2026 12:17:19 GMT  
		Size: 39.0 MB (39037515 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5db47c543a6c879ca8da9aa74d1ba869d99590c43dc077909f584eca08199b2a`  
		Last Modified: Mon, 15 Jun 2026 23:15:00 GMT  
		Size: 39.5 MB (39521864 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:111321d3188ea29432dff9af02550c28918d595330adb7255e3fc322071171eb`  
		Last Modified: Mon, 15 Jun 2026 23:15:00 GMT  
		Size: 52.7 MB (52669727 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f7c53e6db5c7a1ca771c2fdff58966e30f9fbbfc161d2e85c88ed7e1212feae`  
		Last Modified: Mon, 15 Jun 2026 23:14:57 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:091baecea99edd0282ebdd17fdbb6b2a738d8741eab57720382a8509e98bbaf3`  
		Last Modified: Mon, 15 Jun 2026 23:14:50 GMT  
		Size: 2.5 KB (2491 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:8-jdk-ubi10-minimal` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:45786a31362cd45a16585ce6ac3a4e4e2ca0863414bcd7ed5bdf5083c35f5426
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3920216 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c469e3cba6bead7727bf3df361dd3381119c9489b5120c22358ba4b1d51ec09f`

```dockerfile
```

-	Layers:
	-	`sha256:f7f9a9ccf8c2032fa2ee56c94607e98e2978ea937092fd682fc865ba1fce989f`  
		Last Modified: Mon, 15 Jun 2026 23:14:57 GMT  
		Size: 3.9 MB (3900142 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8abfa29b074ede5c67111e043f12ab64521d3712098ab2cf985a3c2333106b7a`  
		Last Modified: Mon, 15 Jun 2026 23:14:57 GMT  
		Size: 20.1 KB (20074 bytes)  
		MIME: application/vnd.in-toto+json
