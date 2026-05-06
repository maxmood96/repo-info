## `eclipse-temurin:21-jdk-ubi10-minimal`

```console
$ docker pull eclipse-temurin@sha256:908c10156866d97013d64167a37f475417c744f7e40f27d3b7875bfe993a4f60
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

### `eclipse-temurin:21-jdk-ubi10-minimal` - linux; amd64

```console
$ docker pull eclipse-temurin@sha256:8ec863eb31c81176db6e7611b6a1c8a66c1818b407b26c8078f8c442102653da
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **214.5 MB (214548915 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d79bdc3775a2774c2f8882221071ca6af450c1a51f77a057ffe9f4c8f07a8b8e`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 04 May 2026 01:36:53 GMT
LABEL maintainer="Red Hat, Inc."
# Mon, 04 May 2026 01:36:53 GMT
LABEL vendor="Red Hat, Inc."
# Mon, 04 May 2026 01:36:53 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Mon, 04 May 2026 01:36:53 GMT
LABEL com.redhat.component="ubi10-minimal-container"       name="ubi10/ubi-minimal"       version="10.1"       cpe="cpe:/o:redhat:enterprise_linux:10.1"       distribution-scope="public"
# Mon, 04 May 2026 01:36:53 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Mon, 04 May 2026 01:36:53 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 10."
# Mon, 04 May 2026 01:36:53 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 04 May 2026 01:36:53 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 04 May 2026 01:36:53 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 10 Minimal"
# Mon, 04 May 2026 01:36:53 GMT
LABEL io.openshift.expose-services=""
# Mon, 04 May 2026 01:36:53 GMT
LABEL io.openshift.tags="minimal rhel10"
# Mon, 04 May 2026 01:36:53 GMT
ENV container oci
# Mon, 04 May 2026 01:36:54 GMT
COPY dir:90d4f1f85494d2a8bf17340af60eb04fb8df2adbe40376c2198b52d03b3dce87 in /      
# Mon, 04 May 2026 01:36:54 GMT
COPY file:5de33b5fc08b00635bccf9134a18978dba13e2250aa51838f9969515a3957847 in /etc/yum.repos.d/.      
# Mon, 04 May 2026 01:36:54 GMT
CMD ["/bin/bash"]
# Mon, 04 May 2026 01:36:54 GMT
COPY file:595171150af68abc798ea385f7988d74b566aa8e84babff137f00b08b2164683 in /usr/share/buildinfo/content-sets.json      
# Mon, 04 May 2026 01:36:54 GMT
COPY file:595171150af68abc798ea385f7988d74b566aa8e84babff137f00b08b2164683 in /root/buildinfo/content_manifests/content-sets.json      
# Mon, 04 May 2026 01:36:54 GMT
COPY file:44acb722ff6847a849911ad1532360393cd9c16592e8d1f9e199cff925bbc7d5 in /usr/share/buildinfo/labels.json      
# Mon, 04 May 2026 01:36:54 GMT
COPY file:44acb722ff6847a849911ad1532360393cd9c16592e8d1f9e199cff925bbc7d5 in /root/buildinfo/labels.json      
# Mon, 04 May 2026 01:36:54 GMT
LABEL "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="2c4967ab62628fff803457df7635994ca0e85fbc" "org.opencontainers.image.revision"="2c4967ab62628fff803457df7635994ca0e85fbc" "build-date"="2026-05-04T01:36:38Z" "org.opencontainers.image.created"="2026-05-04T01:36:38Z" "release"="1777858393"org.opencontainers.image.revision=2c4967ab62628fff803457df7635994ca0e85fbc,org.opencontainers.image.created=2026-05-04T01:36:38Z
# Tue, 05 May 2026 23:08:14 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 05 May 2026 23:08:14 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 05 May 2026 23:08:14 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 05 May 2026 23:08:14 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en         gnupg2     ;     microdnf clean all # buildkit
# Tue, 05 May 2026 23:08:14 GMT
ENV JAVA_VERSION=jdk-21.0.10+7
# Tue, 05 May 2026 23:08:41 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='357fee29fb0d5c079f6730db98b28942df13a6eed426f6c61cd4ad703ab27b9a';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.10%2B7/OpenJDK21U-jdk_aarch64_linux_hotspot_21.0.10_7.tar.gz';          ;;        ppc64le)          ESUM='33bdaec351f40cc70d44e251a54c23e4dd15fed8adc041e35c57461c706cf948';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.10%2B7/OpenJDK21U-jdk_ppc64le_linux_hotspot_21.0.10_7.tar.gz';          ;;        s390x)          ESUM='eabb069b59a2e6b9e9926d9c533186aabf1ff3b4af683d0a3620bb7c7d9770c0';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.10%2B7/OpenJDK21U-jdk_s390x_linux_hotspot_21.0.10_7.tar.gz';          ;;        x86_64)          ESUM='ea3b9bd464d6dd253e9a7accf59f7ccd2a36e4aa69640b7251e3370caef896a4';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.10%2B7/OpenJDK21U-jdk_x64_linux_hotspot_21.0.10_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Tue, 05 May 2026 23:08:42 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 05 May 2026 23:08:42 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 05 May 2026 23:08:42 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 05 May 2026 23:08:42 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:6c2848906904fdb30be3302af6950faf3bb49f8acf1fe7da43266ab561f76092`  
		Last Modified: Mon, 04 May 2026 03:13:50 GMT  
		Size: 34.6 MB (34648199 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c18b8fd3323a4e72d45f54bc20f5d7b1d3faff4ea3989c5f1c27e7c27650909c`  
		Last Modified: Tue, 05 May 2026 23:08:29 GMT  
		Size: 22.0 MB (22037273 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce83d96d62df3ff9849f8968920733bffe952aed77019b41b6cdcd81ab7454fc`  
		Last Modified: Tue, 05 May 2026 23:09:00 GMT  
		Size: 157.9 MB (157861023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eeebc903b2ce96d9e7be6f0aa2606171dc645ff433684a7abf23b21218fef7a1`  
		Last Modified: Tue, 05 May 2026 23:08:57 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9ad78efc9601357a49c351e13747cf68855464bb3fa6e80924162167a6dfc70`  
		Last Modified: Tue, 05 May 2026 23:08:57 GMT  
		Size: 2.3 KB (2292 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:21-jdk-ubi10-minimal` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:4bf14c5168b9e2cc88939b44ed5ca94743360b22123f5e9aff387073e1a06995
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3073189 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:045f82abc0773628e1066996b76d4cf20f8c577d7cdc954c7df57d219e342c99`

```dockerfile
```

-	Layers:
	-	`sha256:b174e9add687cef9d91620f8e52639d6f4b3b38fd93cde1b54b3c5c70ea4f3cd`  
		Last Modified: Tue, 05 May 2026 23:08:57 GMT  
		Size: 3.1 MB (3051873 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:684066ca9278d046a3700a095b314f7a8f4787236f3f44eac77bce91c03c6dfe`  
		Last Modified: Tue, 05 May 2026 23:08:57 GMT  
		Size: 21.3 KB (21316 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-temurin:21-jdk-ubi10-minimal` - linux; arm64 variant v8

```console
$ docker pull eclipse-temurin@sha256:2dcf4a12ea8c72daf508660f10bb53384da4411dc1512873102a3da564172df3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **211.2 MB (211152000 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b865c1de99e080fb69d678e92fadc4e57052c1b2758b057a8362b419920074c`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 04 May 2026 01:38:51 GMT
LABEL maintainer="Red Hat, Inc."
# Mon, 04 May 2026 01:38:51 GMT
LABEL vendor="Red Hat, Inc."
# Mon, 04 May 2026 01:38:51 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Mon, 04 May 2026 01:38:51 GMT
LABEL com.redhat.component="ubi10-minimal-container"       name="ubi10/ubi-minimal"       version="10.1"       cpe="cpe:/o:redhat:enterprise_linux:10.1"       distribution-scope="public"
# Mon, 04 May 2026 01:38:51 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Mon, 04 May 2026 01:38:51 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 10."
# Mon, 04 May 2026 01:38:51 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 04 May 2026 01:38:51 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 04 May 2026 01:38:51 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 10 Minimal"
# Mon, 04 May 2026 01:38:51 GMT
LABEL io.openshift.expose-services=""
# Mon, 04 May 2026 01:38:51 GMT
LABEL io.openshift.tags="minimal rhel10"
# Mon, 04 May 2026 01:38:51 GMT
ENV container oci
# Mon, 04 May 2026 01:38:52 GMT
COPY dir:4f490e44b5cd259c269df4e89626a736e4b70875a47bc79b960d52f7b56f7967 in /      
# Mon, 04 May 2026 01:38:52 GMT
COPY file:5de33b5fc08b00635bccf9134a18978dba13e2250aa51838f9969515a3957847 in /etc/yum.repos.d/.      
# Mon, 04 May 2026 01:38:52 GMT
CMD ["/bin/bash"]
# Mon, 04 May 2026 01:38:52 GMT
COPY file:595171150af68abc798ea385f7988d74b566aa8e84babff137f00b08b2164683 in /usr/share/buildinfo/content-sets.json      
# Mon, 04 May 2026 01:38:52 GMT
COPY file:595171150af68abc798ea385f7988d74b566aa8e84babff137f00b08b2164683 in /root/buildinfo/content_manifests/content-sets.json      
# Mon, 04 May 2026 01:38:53 GMT
COPY file:e2c2a2ab213ef0433a1e15d666daa6e664714283c2d03394bbfa240f7cd44679 in /usr/share/buildinfo/labels.json      
# Mon, 04 May 2026 01:38:53 GMT
COPY file:e2c2a2ab213ef0433a1e15d666daa6e664714283c2d03394bbfa240f7cd44679 in /root/buildinfo/labels.json      
# Mon, 04 May 2026 01:38:53 GMT
LABEL "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="2c4967ab62628fff803457df7635994ca0e85fbc" "org.opencontainers.image.revision"="2c4967ab62628fff803457df7635994ca0e85fbc" "build-date"="2026-05-04T01:38:35Z" "org.opencontainers.image.created"="2026-05-04T01:38:35Z" "release"="1777858393"org.opencontainers.image.revision=2c4967ab62628fff803457df7635994ca0e85fbc,org.opencontainers.image.created=2026-05-04T01:38:35Z
# Tue, 05 May 2026 23:08:13 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 05 May 2026 23:08:13 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 05 May 2026 23:08:13 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 05 May 2026 23:08:13 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en         gnupg2     ;     microdnf clean all # buildkit
# Tue, 05 May 2026 23:08:13 GMT
ENV JAVA_VERSION=jdk-21.0.10+7
# Tue, 05 May 2026 23:08:21 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='357fee29fb0d5c079f6730db98b28942df13a6eed426f6c61cd4ad703ab27b9a';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.10%2B7/OpenJDK21U-jdk_aarch64_linux_hotspot_21.0.10_7.tar.gz';          ;;        ppc64le)          ESUM='33bdaec351f40cc70d44e251a54c23e4dd15fed8adc041e35c57461c706cf948';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.10%2B7/OpenJDK21U-jdk_ppc64le_linux_hotspot_21.0.10_7.tar.gz';          ;;        s390x)          ESUM='eabb069b59a2e6b9e9926d9c533186aabf1ff3b4af683d0a3620bb7c7d9770c0';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.10%2B7/OpenJDK21U-jdk_s390x_linux_hotspot_21.0.10_7.tar.gz';          ;;        x86_64)          ESUM='ea3b9bd464d6dd253e9a7accf59f7ccd2a36e4aa69640b7251e3370caef896a4';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.10%2B7/OpenJDK21U-jdk_x64_linux_hotspot_21.0.10_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Tue, 05 May 2026 23:08:22 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 05 May 2026 23:08:22 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 05 May 2026 23:08:22 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 05 May 2026 23:08:22 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:908809553a77ac560aff532a902be43c3a99a0dcb4f759158a75984cb82c4b9d`  
		Last Modified: Mon, 04 May 2026 06:16:39 GMT  
		Size: 32.7 MB (32711611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69245fcf4f18604802b067e726477bdeadade80142d6cddb68d199c37158d038`  
		Last Modified: Tue, 05 May 2026 23:08:41 GMT  
		Size: 22.3 MB (22301730 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b4ccd990a06f99231ae975c07d6e49b46b796d0eed8711614662c37e6f36ce9`  
		Last Modified: Tue, 05 May 2026 23:08:44 GMT  
		Size: 156.1 MB (156136240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e90ea0166f25ae94800ac7c9f80fd970494654edc9b86f6c94805c7ebedf56cd`  
		Last Modified: Tue, 05 May 2026 23:08:40 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eec41f2dc173160877196ba1cd7920c934714831abfaa25d71161dabe295c68d`  
		Last Modified: Tue, 05 May 2026 23:08:40 GMT  
		Size: 2.3 KB (2290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:21-jdk-ubi10-minimal` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:86628aaf845caf35aefd1c2d2b7425a81b0cb80ed93836edf2529a8250bca1ce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3072731 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:022ec3fbacb1c43fb67cd56f048dddd324e4fcb89f67805f20643d485492231c`

```dockerfile
```

-	Layers:
	-	`sha256:9de870a2d2e9ae31e56fe820d435528fb8c1571c3cd69b17dd91ebe22d5a15e2`  
		Last Modified: Tue, 05 May 2026 23:08:40 GMT  
		Size: 3.1 MB (3051299 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:528f2a50df69616f8c2bf4f75bbe02e409b2fd08c9d44a27c2bfb7e04896e022`  
		Last Modified: Tue, 05 May 2026 23:08:40 GMT  
		Size: 21.4 KB (21432 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-temurin:21-jdk-ubi10-minimal` - linux; ppc64le

```console
$ docker pull eclipse-temurin@sha256:0d9df35f4864ccc90c56837d4ac6beae0d39526af767be137dfd9dc6beb290bf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **220.1 MB (220063365 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e8c7c3988e37de488ded22b1cd58a39975dccbae347b780a690501846db99d6`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 04 May 2026 01:39:14 GMT
LABEL maintainer="Red Hat, Inc."
# Mon, 04 May 2026 01:39:14 GMT
LABEL vendor="Red Hat, Inc."
# Mon, 04 May 2026 01:39:14 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Mon, 04 May 2026 01:39:14 GMT
LABEL com.redhat.component="ubi10-minimal-container"       name="ubi10/ubi-minimal"       version="10.1"       cpe="cpe:/o:redhat:enterprise_linux:10.1"       distribution-scope="public"
# Mon, 04 May 2026 01:39:14 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Mon, 04 May 2026 01:39:15 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 10."
# Mon, 04 May 2026 01:39:15 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 04 May 2026 01:39:15 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 04 May 2026 01:39:15 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 10 Minimal"
# Mon, 04 May 2026 01:39:15 GMT
LABEL io.openshift.expose-services=""
# Mon, 04 May 2026 01:39:15 GMT
LABEL io.openshift.tags="minimal rhel10"
# Mon, 04 May 2026 01:39:15 GMT
ENV container oci
# Mon, 04 May 2026 01:39:15 GMT
COPY dir:12413a5bdb80a75f63d061b3c0328d3ec0033dbb6ef2e4efcba8481b6ce277c7 in /      
# Mon, 04 May 2026 01:39:15 GMT
COPY file:5de33b5fc08b00635bccf9134a18978dba13e2250aa51838f9969515a3957847 in /etc/yum.repos.d/.      
# Mon, 04 May 2026 01:39:15 GMT
CMD ["/bin/bash"]
# Mon, 04 May 2026 01:39:15 GMT
COPY file:595171150af68abc798ea385f7988d74b566aa8e84babff137f00b08b2164683 in /usr/share/buildinfo/content-sets.json      
# Mon, 04 May 2026 01:39:15 GMT
COPY file:595171150af68abc798ea385f7988d74b566aa8e84babff137f00b08b2164683 in /root/buildinfo/content_manifests/content-sets.json      
# Mon, 04 May 2026 01:39:15 GMT
COPY file:727a91663c7c1ef3c87416ec38b4c09702b0fa948721f73b1c8c27f7a242068b in /usr/share/buildinfo/labels.json      
# Mon, 04 May 2026 01:39:16 GMT
COPY file:727a91663c7c1ef3c87416ec38b4c09702b0fa948721f73b1c8c27f7a242068b in /root/buildinfo/labels.json      
# Mon, 04 May 2026 01:39:16 GMT
LABEL "architecture"="ppc64le" "vcs-type"="git" "vcs-ref"="2c4967ab62628fff803457df7635994ca0e85fbc" "org.opencontainers.image.revision"="2c4967ab62628fff803457df7635994ca0e85fbc" "build-date"="2026-05-04T01:39:03Z" "org.opencontainers.image.created"="2026-05-04T01:39:03Z" "release"="1777858393"org.opencontainers.image.revision=2c4967ab62628fff803457df7635994ca0e85fbc,org.opencontainers.image.created=2026-05-04T01:39:03Z
# Tue, 05 May 2026 23:47:29 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 05 May 2026 23:47:29 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 05 May 2026 23:47:29 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 05 May 2026 23:47:29 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en         gnupg2     ;     microdnf clean all # buildkit
# Tue, 05 May 2026 23:47:29 GMT
ENV JAVA_VERSION=jdk-21.0.10+7
# Tue, 05 May 2026 23:53:52 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='357fee29fb0d5c079f6730db98b28942df13a6eed426f6c61cd4ad703ab27b9a';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.10%2B7/OpenJDK21U-jdk_aarch64_linux_hotspot_21.0.10_7.tar.gz';          ;;        ppc64le)          ESUM='33bdaec351f40cc70d44e251a54c23e4dd15fed8adc041e35c57461c706cf948';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.10%2B7/OpenJDK21U-jdk_ppc64le_linux_hotspot_21.0.10_7.tar.gz';          ;;        s390x)          ESUM='eabb069b59a2e6b9e9926d9c533186aabf1ff3b4af683d0a3620bb7c7d9770c0';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.10%2B7/OpenJDK21U-jdk_s390x_linux_hotspot_21.0.10_7.tar.gz';          ;;        x86_64)          ESUM='ea3b9bd464d6dd253e9a7accf59f7ccd2a36e4aa69640b7251e3370caef896a4';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.10%2B7/OpenJDK21U-jdk_x64_linux_hotspot_21.0.10_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Tue, 05 May 2026 23:53:54 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 05 May 2026 23:53:55 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 05 May 2026 23:53:55 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 05 May 2026 23:53:55 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:f2dd1d2c3d5fda579799f9becd292589fb99f0abc7f5c226856eb2bbbbc120cc`  
		Last Modified: Mon, 04 May 2026 06:16:51 GMT  
		Size: 38.7 MB (38745905 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc2ee71f34837c204e126c0f30bd59bdd1c1aad2d6a82e82078b6ce249102e06`  
		Last Modified: Tue, 05 May 2026 23:48:16 GMT  
		Size: 23.3 MB (23333693 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10b4df0c2151351f00b86bf904ed4374865dbadbc083c18fed8da6815c15a621`  
		Last Modified: Tue, 05 May 2026 23:54:32 GMT  
		Size: 158.0 MB (157981346 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:332691c767ddeebd25911f2bc535b63db93ea983d894b5e7467f27679c099ea3`  
		Last Modified: Tue, 05 May 2026 23:54:28 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aab1b51621c97c389da0f0ed3b2da5650270743604fe2cfa8a59a0f3f17ffc4d`  
		Last Modified: Tue, 05 May 2026 23:54:28 GMT  
		Size: 2.3 KB (2292 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:21-jdk-ubi10-minimal` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:dcae3d36c54c0aa6e955b8ad94215635cc605813a2e101f94e30d4fd685ce2c5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3066981 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b08a2dcc121490b6b67a11f8f7c3006164ac428762dce7db125f35b7646f650b`

```dockerfile
```

-	Layers:
	-	`sha256:5fa851f45c697a1742d167a99d44651fbff822c0d3761990c1963def9b51fc45`  
		Last Modified: Tue, 05 May 2026 23:54:28 GMT  
		Size: 3.0 MB (3045629 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2cd0e5fd2b94e32cab4ec75e85c87e49ec7b94c427effc461c0574bbaee92142`  
		Last Modified: Tue, 05 May 2026 23:54:28 GMT  
		Size: 21.4 KB (21352 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-temurin:21-jdk-ubi10-minimal` - linux; s390x

```console
$ docker pull eclipse-temurin@sha256:41ce56c359988dcbbc5d6e7e165c8ac31e36146fbb81ebe851b3031ee426021d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **203.9 MB (203902305 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:02f51b5425c62285a80cd3404eeefaa4bfc17d60a3ba99f4340c281a6203fe34`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 04 May 2026 01:46:56 GMT
LABEL maintainer="Red Hat, Inc."
# Mon, 04 May 2026 01:46:56 GMT
LABEL vendor="Red Hat, Inc."
# Mon, 04 May 2026 01:46:56 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Mon, 04 May 2026 01:46:56 GMT
LABEL com.redhat.component="ubi10-minimal-container"       name="ubi10/ubi-minimal"       version="10.1"       cpe="cpe:/o:redhat:enterprise_linux:10.1"       distribution-scope="public"
# Mon, 04 May 2026 01:46:56 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Mon, 04 May 2026 01:46:56 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 10."
# Mon, 04 May 2026 01:46:56 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 04 May 2026 01:46:56 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 04 May 2026 01:46:56 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 10 Minimal"
# Mon, 04 May 2026 01:46:56 GMT
LABEL io.openshift.expose-services=""
# Mon, 04 May 2026 01:46:56 GMT
LABEL io.openshift.tags="minimal rhel10"
# Mon, 04 May 2026 01:46:56 GMT
ENV container oci
# Mon, 04 May 2026 01:46:56 GMT
COPY dir:cacbd48510196fa765f2d5bccb8b2b0023c608fcbd86154b6fe34e775acd2483 in /      
# Mon, 04 May 2026 01:46:56 GMT
COPY file:5de33b5fc08b00635bccf9134a18978dba13e2250aa51838f9969515a3957847 in /etc/yum.repos.d/.      
# Mon, 04 May 2026 01:46:56 GMT
CMD ["/bin/bash"]
# Mon, 04 May 2026 01:46:56 GMT
COPY file:595171150af68abc798ea385f7988d74b566aa8e84babff137f00b08b2164683 in /usr/share/buildinfo/content-sets.json      
# Mon, 04 May 2026 01:46:57 GMT
COPY file:595171150af68abc798ea385f7988d74b566aa8e84babff137f00b08b2164683 in /root/buildinfo/content_manifests/content-sets.json      
# Mon, 04 May 2026 01:46:57 GMT
COPY file:6983ce2775fc6ec74b2d7c54d91fce16f639c26d824bf41c774ba5d5ae4037e9 in /usr/share/buildinfo/labels.json      
# Mon, 04 May 2026 01:46:57 GMT
COPY file:6983ce2775fc6ec74b2d7c54d91fce16f639c26d824bf41c774ba5d5ae4037e9 in /root/buildinfo/labels.json      
# Mon, 04 May 2026 01:46:57 GMT
LABEL "architecture"="s390x" "vcs-type"="git" "vcs-ref"="2c4967ab62628fff803457df7635994ca0e85fbc" "org.opencontainers.image.revision"="2c4967ab62628fff803457df7635994ca0e85fbc" "build-date"="2026-05-04T01:46:14Z" "org.opencontainers.image.created"="2026-05-04T01:46:14Z" "release"="1777858393"org.opencontainers.image.revision=2c4967ab62628fff803457df7635994ca0e85fbc,org.opencontainers.image.created=2026-05-04T01:46:14Z
# Wed, 06 May 2026 00:08:32 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 06 May 2026 00:08:32 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 06 May 2026 00:08:32 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 06 May 2026 00:08:32 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en         gnupg2     ;     microdnf clean all # buildkit
# Wed, 06 May 2026 00:08:32 GMT
ENV JAVA_VERSION=jdk-21.0.10+7
# Wed, 06 May 2026 00:11:58 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='357fee29fb0d5c079f6730db98b28942df13a6eed426f6c61cd4ad703ab27b9a';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.10%2B7/OpenJDK21U-jdk_aarch64_linux_hotspot_21.0.10_7.tar.gz';          ;;        ppc64le)          ESUM='33bdaec351f40cc70d44e251a54c23e4dd15fed8adc041e35c57461c706cf948';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.10%2B7/OpenJDK21U-jdk_ppc64le_linux_hotspot_21.0.10_7.tar.gz';          ;;        s390x)          ESUM='eabb069b59a2e6b9e9926d9c533186aabf1ff3b4af683d0a3620bb7c7d9770c0';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.10%2B7/OpenJDK21U-jdk_s390x_linux_hotspot_21.0.10_7.tar.gz';          ;;        x86_64)          ESUM='ea3b9bd464d6dd253e9a7accf59f7ccd2a36e4aa69640b7251e3370caef896a4';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.10%2B7/OpenJDK21U-jdk_x64_linux_hotspot_21.0.10_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Wed, 06 May 2026 00:12:00 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 06 May 2026 00:12:00 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 06 May 2026 00:12:00 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 06 May 2026 00:12:00 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:e434a7e4a8db18a3b2f706d5c1b2a02cfe20f46083a805f7dcf9e2e92903aa2e`  
		Last Modified: Mon, 04 May 2026 06:16:45 GMT  
		Size: 34.4 MB (34430001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e06a4a5291aa3dc425a53819ce535f60012137e7f9e2faeddeef31090147f8e5`  
		Last Modified: Wed, 06 May 2026 00:09:06 GMT  
		Size: 22.4 MB (22365064 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5051d32580e55a1c44d4d826fe0e6a2dc82c989f316084f91d25b57472998a1a`  
		Last Modified: Wed, 06 May 2026 00:12:35 GMT  
		Size: 147.1 MB (147104823 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:832dc3f469de1277adf5a813b06a225aba4f7be46f9a71b70cf8a66c4dc354da`  
		Last Modified: Wed, 06 May 2026 00:12:33 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c3dbd4b80ac0b0ccfd7fccc7442b4575395f6f7674f7d51522c3624204d0e8d`  
		Last Modified: Wed, 06 May 2026 00:12:33 GMT  
		Size: 2.3 KB (2291 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:21-jdk-ubi10-minimal` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:1fdc13359bd89dce9a58b4a962ba5ce50d27a595a961f8a60c729277f178ea6f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3065703 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a239aed4138240664f4f03c5ae2f748bbdab4e0dee3dc2bd2b6e38a4c399560`

```dockerfile
```

-	Layers:
	-	`sha256:7890e36dce32431fe50b87ca6be54a9799b509a46731dd7f032668584cc8b0de`  
		Last Modified: Wed, 06 May 2026 00:12:33 GMT  
		Size: 3.0 MB (3044387 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4e24bb042d281fdfe7d332ca52d2c3205c5888b78a7c20c494ef4901da985f9c`  
		Last Modified: Wed, 06 May 2026 00:12:32 GMT  
		Size: 21.3 KB (21316 bytes)  
		MIME: application/vnd.in-toto+json
