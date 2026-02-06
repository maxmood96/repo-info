## `eclipse-temurin:25-jre-ubi10-minimal`

```console
$ docker pull eclipse-temurin@sha256:be62076f857b924807d6d0a600c6fe5a4f2f1aa16849e02dbcbb90498a518c43
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
$ docker pull eclipse-temurin@sha256:ae88ac42c852fc74f59bc18542bf8c7327427d06e1a896f7f9219f74f48ba0c9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.6 MB (134594137 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:10d644cf4fe9c7b83d5b3c4d649e232dc43b18de867e6546dc23ff4d49679b9e`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`

```dockerfile
# Wed, 04 Feb 2026 04:55:05 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 04 Feb 2026 04:55:05 GMT
LABEL vendor="Red Hat, Inc."
# Wed, 04 Feb 2026 04:55:05 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Wed, 04 Feb 2026 04:55:05 GMT
LABEL com.redhat.component="ubi10-minimal-container"       name="ubi10/ubi-minimal"       version="10.1"       cpe="cpe:/o:redhat:enterprise_linux:10.1"       distribution-scope="public"
# Wed, 04 Feb 2026 04:55:06 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 04 Feb 2026 04:55:06 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 10."
# Wed, 04 Feb 2026 04:55:06 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 04 Feb 2026 04:55:06 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 04 Feb 2026 04:55:06 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 10 Minimal"
# Wed, 04 Feb 2026 04:55:06 GMT
LABEL io.openshift.expose-services=""
# Wed, 04 Feb 2026 04:55:06 GMT
LABEL io.openshift.tags="minimal rhel10"
# Wed, 04 Feb 2026 04:55:06 GMT
ENV container oci
# Wed, 04 Feb 2026 04:55:06 GMT
COPY dir:ab88dbc5c421721056a4539f41aea4ce909f7032f536329269fb1718e0c3e67d in /      
# Wed, 04 Feb 2026 04:55:07 GMT
COPY file:5de33b5fc08b00635bccf9134a18978dba13e2250aa51838f9969515a3957847 in /etc/yum.repos.d/.      
# Wed, 04 Feb 2026 04:55:07 GMT
CMD ["/bin/bash"]
# Wed, 04 Feb 2026 04:55:07 GMT
COPY file:595171150af68abc798ea385f7988d74b566aa8e84babff137f00b08b2164683 in /usr/share/buildinfo/content-sets.json      
# Wed, 04 Feb 2026 04:55:07 GMT
COPY file:595171150af68abc798ea385f7988d74b566aa8e84babff137f00b08b2164683 in /root/buildinfo/content_manifests/content-sets.json      
# Wed, 04 Feb 2026 04:55:07 GMT
COPY file:6cb7b50636b55f291cf75a2750279d2c83bd2761ac9a492a49d90a49cb72e8ac in /usr/share/buildinfo/labels.json      
# Wed, 04 Feb 2026 04:55:07 GMT
COPY file:6cb7b50636b55f291cf75a2750279d2c83bd2761ac9a492a49d90a49cb72e8ac in /root/buildinfo/labels.json      
# Wed, 04 Feb 2026 04:55:08 GMT
LABEL "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="1b6103ed0475d35e7b65ab0a0bcaa2f6d4bde92b" "org.opencontainers.image.revision"="1b6103ed0475d35e7b65ab0a0bcaa2f6d4bde92b" "build-date"="2026-02-04T04:54:43Z" "org.opencontainers.image.created"="2026-02-04T04:54:43Z" "release"="1770180557"org.opencontainers.image.revision=1b6103ed0475d35e7b65ab0a0bcaa2f6d4bde92b,org.opencontainers.image.created=2026-02-04T04:54:43Z
# Thu, 05 Feb 2026 22:21:21 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 05 Feb 2026 22:21:21 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 05 Feb 2026 22:21:21 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 05 Feb 2026 22:21:21 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en         gnupg2     ;     microdnf clean all # buildkit
# Thu, 05 Feb 2026 22:21:21 GMT
ENV JAVA_VERSION=jdk-25.0.2+10
# Thu, 05 Feb 2026 22:21:26 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='e90ad4a618a0228a2126e7c6abfbc0729e2649d7d72cef45fd640239866eb050';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.2%2B10/OpenJDK25U-jre_aarch64_linux_hotspot_25.0.2_10.tar.gz';          ;;        ppc64le)          ESUM='1cc773ab86cbdbb02732398ad4550950db859fb08f8eb6548c8c5e188f697455';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.2%2B10/OpenJDK25U-jre_ppc64le_linux_hotspot_25.0.2_10.tar.gz';          ;;        s390x)          ESUM='ccb977223490643318230b53107aaa23c136d2793b5174dc38d4b0daab9a18e3';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.2%2B10/OpenJDK25U-jre_s390x_linux_hotspot_25.0.2_10.tar.gz';          ;;        x86_64)          ESUM='d6c89e08f42be94cd55eab20190958a35b993625018a3ac59cb3d16d8445cf98';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.2%2B10/OpenJDK25U-jre_x64_linux_hotspot_25.0.2_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz; # buildkit
# Thu, 05 Feb 2026 22:21:26 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 05 Feb 2026 22:21:26 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 05 Feb 2026 22:21:26 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
```

-	Layers:
	-	`sha256:819501e18c85a616b033a682e2078167e38cd15970dd3534932af6715532259f`  
		Last Modified: Wed, 04 Feb 2026 05:56:28 GMT  
		Size: 34.6 MB (34565108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27336a416d3a31fc9d4d88c5fb9db6b11c3f730f87173d53b7ff51e65baca1f4`  
		Last Modified: Thu, 05 Feb 2026 22:21:42 GMT  
		Size: 37.4 MB (37413774 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd6eca43febc48b3fe815fbd7ef624690e2a44cfd35ce4e00b410bd1147bbf42`  
		Last Modified: Thu, 05 Feb 2026 22:21:43 GMT  
		Size: 62.6 MB (62612837 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b90b330cea793354121069b0f224eee4d0baf0326944116e3758775bd6eb0814`  
		Last Modified: Thu, 05 Feb 2026 22:21:41 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:809d6950436ecafb218a9c203cf455398d885a012b6ba9ac929e66ef27417a2e`  
		Last Modified: Thu, 05 Feb 2026 22:21:41 GMT  
		Size: 2.3 KB (2291 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:25-jre-ubi10-minimal` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:06e3082106998006e50b6ffd8203ee295095826e4f8743907390ee42ff43dd27
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3733207 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba8822233707396b1cc2e21d61643467db9ce4478e468148809f1a0104d93199`

```dockerfile
```

-	Layers:
	-	`sha256:e3b4bf990f2fb29f0154ecb1d075c7bebc67c4ab3b210c0a43336210971f1fd8`  
		Last Modified: Thu, 05 Feb 2026 22:21:41 GMT  
		Size: 3.7 MB (3712854 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d0ce2e8810ea0448a340551d9bd58e16a52e49365233d97c8290db13173fcfd4`  
		Last Modified: Thu, 05 Feb 2026 22:21:41 GMT  
		Size: 20.4 KB (20353 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-temurin:25-jre-ubi10-minimal` - linux; arm64 variant v8

```console
$ docker pull eclipse-temurin@sha256:3a8a013c077ad6fd5dcf817d4d483e498e506a5345dcd1b50dc55afa1fadda06
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **131.6 MB (131603407 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df9bb383d79d47a96650eb8096bea085fc5acd6add5b77a5ab5c97a9684343c3`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`

```dockerfile
# Wed, 04 Feb 2026 04:56:41 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 04 Feb 2026 04:56:41 GMT
LABEL vendor="Red Hat, Inc."
# Wed, 04 Feb 2026 04:56:41 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Wed, 04 Feb 2026 04:56:41 GMT
LABEL com.redhat.component="ubi10-minimal-container"       name="ubi10/ubi-minimal"       version="10.1"       cpe="cpe:/o:redhat:enterprise_linux:10.1"       distribution-scope="public"
# Wed, 04 Feb 2026 04:56:41 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 04 Feb 2026 04:56:41 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 10."
# Wed, 04 Feb 2026 04:56:41 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 04 Feb 2026 04:56:41 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 04 Feb 2026 04:56:41 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 10 Minimal"
# Wed, 04 Feb 2026 04:56:41 GMT
LABEL io.openshift.expose-services=""
# Wed, 04 Feb 2026 04:56:41 GMT
LABEL io.openshift.tags="minimal rhel10"
# Wed, 04 Feb 2026 04:56:41 GMT
ENV container oci
# Wed, 04 Feb 2026 04:56:42 GMT
COPY dir:67028d43c1066b84b1209232f64f1a4cc4b9dbbfba57178bd9cbb9c32d30e9e7 in /      
# Wed, 04 Feb 2026 04:56:42 GMT
COPY file:5de33b5fc08b00635bccf9134a18978dba13e2250aa51838f9969515a3957847 in /etc/yum.repos.d/.      
# Wed, 04 Feb 2026 04:56:42 GMT
CMD ["/bin/bash"]
# Wed, 04 Feb 2026 04:56:42 GMT
COPY file:595171150af68abc798ea385f7988d74b566aa8e84babff137f00b08b2164683 in /usr/share/buildinfo/content-sets.json      
# Wed, 04 Feb 2026 04:56:42 GMT
COPY file:595171150af68abc798ea385f7988d74b566aa8e84babff137f00b08b2164683 in /root/buildinfo/content_manifests/content-sets.json      
# Wed, 04 Feb 2026 04:56:42 GMT
COPY file:6daaa71ff7be172f731620b1d0190bb9c2177930f1dd64e2221f2ce09f100fc6 in /usr/share/buildinfo/labels.json      
# Wed, 04 Feb 2026 04:56:42 GMT
COPY file:6daaa71ff7be172f731620b1d0190bb9c2177930f1dd64e2221f2ce09f100fc6 in /root/buildinfo/labels.json      
# Wed, 04 Feb 2026 04:56:43 GMT
LABEL "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="1b6103ed0475d35e7b65ab0a0bcaa2f6d4bde92b" "org.opencontainers.image.revision"="1b6103ed0475d35e7b65ab0a0bcaa2f6d4bde92b" "build-date"="2026-02-04T04:56:21Z" "org.opencontainers.image.created"="2026-02-04T04:56:21Z" "release"="1770180557"org.opencontainers.image.revision=1b6103ed0475d35e7b65ab0a0bcaa2f6d4bde92b,org.opencontainers.image.created=2026-02-04T04:56:21Z
# Thu, 05 Feb 2026 22:20:23 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 05 Feb 2026 22:20:23 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 05 Feb 2026 22:20:23 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 05 Feb 2026 22:20:23 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en         gnupg2     ;     microdnf clean all # buildkit
# Thu, 05 Feb 2026 22:20:23 GMT
ENV JAVA_VERSION=jdk-25.0.2+10
# Thu, 05 Feb 2026 22:20:28 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='e90ad4a618a0228a2126e7c6abfbc0729e2649d7d72cef45fd640239866eb050';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.2%2B10/OpenJDK25U-jre_aarch64_linux_hotspot_25.0.2_10.tar.gz';          ;;        ppc64le)          ESUM='1cc773ab86cbdbb02732398ad4550950db859fb08f8eb6548c8c5e188f697455';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.2%2B10/OpenJDK25U-jre_ppc64le_linux_hotspot_25.0.2_10.tar.gz';          ;;        s390x)          ESUM='ccb977223490643318230b53107aaa23c136d2793b5174dc38d4b0daab9a18e3';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.2%2B10/OpenJDK25U-jre_s390x_linux_hotspot_25.0.2_10.tar.gz';          ;;        x86_64)          ESUM='d6c89e08f42be94cd55eab20190958a35b993625018a3ac59cb3d16d8445cf98';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.2%2B10/OpenJDK25U-jre_x64_linux_hotspot_25.0.2_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz; # buildkit
# Thu, 05 Feb 2026 22:20:28 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 05 Feb 2026 22:20:28 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 05 Feb 2026 22:20:28 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
```

-	Layers:
	-	`sha256:e7aaef72f9aac8066ddd0c18bcd7c76fcc63212a965d38f195e0959c666aa7ce`  
		Last Modified: Wed, 04 Feb 2026 06:11:32 GMT  
		Size: 32.7 MB (32661097 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffb4ab428ac9bae3c0372d8914c448f17390c872b77fda103653a6b129e1a98c`  
		Last Modified: Thu, 05 Feb 2026 22:20:45 GMT  
		Size: 37.4 MB (37361774 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f4d1269a0f96b74e2af51f899e70312c5513d3cda848a0b3d3cddc6c28432fb`  
		Last Modified: Thu, 05 Feb 2026 22:20:45 GMT  
		Size: 61.6 MB (61578118 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45c31c99317fe9f775a323cc46f67e1f4b065571950c776e47f9441dcf964393`  
		Last Modified: Thu, 05 Feb 2026 22:20:43 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16da0f493066e89f303999ae2b2122cf5c932da7bac8ac031238395adff10f02`  
		Last Modified: Thu, 05 Feb 2026 22:20:43 GMT  
		Size: 2.3 KB (2290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:25-jre-ubi10-minimal` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:04c664273447b44af2d8536badffed6b85e3e446e4731664741b39938b051a06
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3732723 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bae539c7f86a6f7ff0037c64c43fb9a393f4efb0eebed809dce953541c5f69ff`

```dockerfile
```

-	Layers:
	-	`sha256:d00573eb7bd57a0317ace0cff237fc2d627bfa5f2cac1b5d42f6930a238c2f66`  
		Last Modified: Thu, 05 Feb 2026 22:20:43 GMT  
		Size: 3.7 MB (3712265 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9ba5250905bd642c2078b79c3039853e2726e8c2ffe8aef2c5a1a332f2a26c37`  
		Last Modified: Thu, 05 Feb 2026 22:20:43 GMT  
		Size: 20.5 KB (20458 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-temurin:25-jre-ubi10-minimal` - linux; ppc64le

```console
$ docker pull eclipse-temurin@sha256:da469b4cb08bb418038d197b76ea9f6e8e63f39d2f26c46a2d0d3358f1ed22b8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **139.9 MB (139901273 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:609dc3e0d52ed6cf01956f081b2c801176fda719d74daf6910961973ec0c144e`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`

```dockerfile
# Wed, 04 Feb 2026 04:58:36 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 04 Feb 2026 04:58:36 GMT
LABEL vendor="Red Hat, Inc."
# Wed, 04 Feb 2026 04:58:36 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Wed, 04 Feb 2026 04:58:36 GMT
LABEL com.redhat.component="ubi10-minimal-container"       name="ubi10/ubi-minimal"       version="10.1"       cpe="cpe:/o:redhat:enterprise_linux:10.1"       distribution-scope="public"
# Wed, 04 Feb 2026 04:58:36 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 04 Feb 2026 04:58:36 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 10."
# Wed, 04 Feb 2026 04:58:36 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 04 Feb 2026 04:58:36 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 04 Feb 2026 04:58:36 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 10 Minimal"
# Wed, 04 Feb 2026 04:58:36 GMT
LABEL io.openshift.expose-services=""
# Wed, 04 Feb 2026 04:58:36 GMT
LABEL io.openshift.tags="minimal rhel10"
# Wed, 04 Feb 2026 04:58:36 GMT
ENV container oci
# Wed, 04 Feb 2026 04:58:37 GMT
COPY dir:09fdad4b579363b2c8418a42c62ea4dc38d67115c8d53cd4a2ec14253ecaf9ad in /      
# Wed, 04 Feb 2026 04:58:37 GMT
COPY file:5de33b5fc08b00635bccf9134a18978dba13e2250aa51838f9969515a3957847 in /etc/yum.repos.d/.      
# Wed, 04 Feb 2026 04:58:37 GMT
CMD ["/bin/bash"]
# Wed, 04 Feb 2026 04:58:37 GMT
COPY file:595171150af68abc798ea385f7988d74b566aa8e84babff137f00b08b2164683 in /usr/share/buildinfo/content-sets.json      
# Wed, 04 Feb 2026 04:58:37 GMT
COPY file:595171150af68abc798ea385f7988d74b566aa8e84babff137f00b08b2164683 in /root/buildinfo/content_manifests/content-sets.json      
# Wed, 04 Feb 2026 04:58:37 GMT
COPY file:0c67174697cfbd406f6852cad47660b65db0ae88b3ec344fd5c165877edf759b in /usr/share/buildinfo/labels.json      
# Wed, 04 Feb 2026 04:58:37 GMT
COPY file:0c67174697cfbd406f6852cad47660b65db0ae88b3ec344fd5c165877edf759b in /root/buildinfo/labels.json      
# Wed, 04 Feb 2026 04:58:38 GMT
LABEL "architecture"="ppc64le" "vcs-type"="git" "vcs-ref"="1b6103ed0475d35e7b65ab0a0bcaa2f6d4bde92b" "org.opencontainers.image.revision"="1b6103ed0475d35e7b65ab0a0bcaa2f6d4bde92b" "build-date"="2026-02-04T04:58:25Z" "org.opencontainers.image.created"="2026-02-04T04:58:25Z" "release"="1770180557"org.opencontainers.image.revision=1b6103ed0475d35e7b65ab0a0bcaa2f6d4bde92b,org.opencontainers.image.created=2026-02-04T04:58:25Z
# Thu, 05 Feb 2026 01:21:18 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 05 Feb 2026 01:21:18 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 05 Feb 2026 01:21:18 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 05 Feb 2026 01:21:18 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en         gnupg2     ;     microdnf clean all # buildkit
# Thu, 05 Feb 2026 01:21:18 GMT
ENV JAVA_VERSION=jdk-25.0.2+10
# Thu, 05 Feb 2026 22:35:51 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='e90ad4a618a0228a2126e7c6abfbc0729e2649d7d72cef45fd640239866eb050';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.2%2B10/OpenJDK25U-jre_aarch64_linux_hotspot_25.0.2_10.tar.gz';          ;;        ppc64le)          ESUM='1cc773ab86cbdbb02732398ad4550950db859fb08f8eb6548c8c5e188f697455';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.2%2B10/OpenJDK25U-jre_ppc64le_linux_hotspot_25.0.2_10.tar.gz';          ;;        s390x)          ESUM='ccb977223490643318230b53107aaa23c136d2793b5174dc38d4b0daab9a18e3';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.2%2B10/OpenJDK25U-jre_s390x_linux_hotspot_25.0.2_10.tar.gz';          ;;        x86_64)          ESUM='d6c89e08f42be94cd55eab20190958a35b993625018a3ac59cb3d16d8445cf98';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.2%2B10/OpenJDK25U-jre_x64_linux_hotspot_25.0.2_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz; # buildkit
# Thu, 05 Feb 2026 22:35:52 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 05 Feb 2026 22:35:52 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 05 Feb 2026 22:35:52 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
```

-	Layers:
	-	`sha256:1cff691ae927c200ee804ea0243a79390de10e4d7f5f6687bde708134b9917c4`  
		Last Modified: Wed, 04 Feb 2026 06:11:59 GMT  
		Size: 38.7 MB (38689551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:907a9332059e30e789362eb783b19695b44bab5a28726fe9fd59ec73d342defd`  
		Last Modified: Thu, 05 Feb 2026 01:22:04 GMT  
		Size: 39.2 MB (39172221 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e13386b1b5fd78e00873477b6cbc328f7f1ccb295c6f594da92c52966a26589`  
		Last Modified: Thu, 05 Feb 2026 22:36:26 GMT  
		Size: 62.0 MB (62037084 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6dd4cbcbbae862b19418f4ce9cec2084bc2000ed3ef86813ef3292b8807b4a10`  
		Last Modified: Thu, 05 Feb 2026 22:36:24 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:278f89a035f90e97fc67b94fc498b2731d3905361d6031aeaa3b40f28ea802cb`  
		Last Modified: Thu, 05 Feb 2026 22:36:24 GMT  
		Size: 2.3 KB (2290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:25-jre-ubi10-minimal` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:64a848cac83fb84e7ff20b2327a4d7fdedb5295e66b95af5b89e63f51aa71bff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3721362 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:29c6074acbb542149c62a18131e1430019f89f31d83e3a11c3548ee3750b77f3`

```dockerfile
```

-	Layers:
	-	`sha256:a843f5c134074a207994abb1e865ebc1f12582ae2a9e76c172af08123a0c652f`  
		Last Modified: Thu, 05 Feb 2026 22:36:24 GMT  
		Size: 3.7 MB (3700978 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:307f1695af7baf954142f87180a7cfed37f7df033854b95bd847b1a9fb22eab6`  
		Last Modified: Thu, 05 Feb 2026 22:36:24 GMT  
		Size: 20.4 KB (20384 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-temurin:25-jre-ubi10-minimal` - linux; s390x

```console
$ docker pull eclipse-temurin@sha256:8d9baa4babbd9f9e6c4a01899e100b2b3965f6f06172331807aad4713cf30a09
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **132.4 MB (132422781 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ddf2dc9e4de07ac93dc14ece16a91bafb6db2bced022fc90bd636587565094e5`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`

```dockerfile
# Wed, 04 Feb 2026 05:11:29 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 04 Feb 2026 05:11:29 GMT
LABEL vendor="Red Hat, Inc."
# Wed, 04 Feb 2026 05:11:29 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Wed, 04 Feb 2026 05:11:29 GMT
LABEL com.redhat.component="ubi10-minimal-container"       name="ubi10/ubi-minimal"       version="10.1"       cpe="cpe:/o:redhat:enterprise_linux:10.1"       distribution-scope="public"
# Wed, 04 Feb 2026 05:11:29 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 04 Feb 2026 05:11:29 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 10."
# Wed, 04 Feb 2026 05:11:29 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 04 Feb 2026 05:11:29 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 04 Feb 2026 05:11:29 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 10 Minimal"
# Wed, 04 Feb 2026 05:11:29 GMT
LABEL io.openshift.expose-services=""
# Wed, 04 Feb 2026 05:11:29 GMT
LABEL io.openshift.tags="minimal rhel10"
# Wed, 04 Feb 2026 05:11:29 GMT
ENV container oci
# Wed, 04 Feb 2026 05:11:30 GMT
COPY dir:9d4ac575a92f53870377be4b68b1588c9bc427ee283102569774f3d9158a16f9 in /      
# Wed, 04 Feb 2026 05:11:30 GMT
COPY file:5de33b5fc08b00635bccf9134a18978dba13e2250aa51838f9969515a3957847 in /etc/yum.repos.d/.      
# Wed, 04 Feb 2026 05:11:30 GMT
CMD ["/bin/bash"]
# Wed, 04 Feb 2026 05:11:30 GMT
COPY file:595171150af68abc798ea385f7988d74b566aa8e84babff137f00b08b2164683 in /usr/share/buildinfo/content-sets.json      
# Wed, 04 Feb 2026 05:11:30 GMT
COPY file:595171150af68abc798ea385f7988d74b566aa8e84babff137f00b08b2164683 in /root/buildinfo/content_manifests/content-sets.json      
# Wed, 04 Feb 2026 05:11:30 GMT
COPY file:bd2f18d5b9d97db31e1a3f98a0670c0f15ee13ca2c036700589166ed0ad3221a in /usr/share/buildinfo/labels.json      
# Wed, 04 Feb 2026 05:11:30 GMT
COPY file:bd2f18d5b9d97db31e1a3f98a0670c0f15ee13ca2c036700589166ed0ad3221a in /root/buildinfo/labels.json      
# Wed, 04 Feb 2026 05:11:30 GMT
LABEL "architecture"="s390x" "vcs-type"="git" "vcs-ref"="1b6103ed0475d35e7b65ab0a0bcaa2f6d4bde92b" "org.opencontainers.image.revision"="1b6103ed0475d35e7b65ab0a0bcaa2f6d4bde92b" "build-date"="2026-02-04T05:09:09Z" "org.opencontainers.image.created"="2026-02-04T05:09:09Z" "release"="1770180557"org.opencontainers.image.revision=1b6103ed0475d35e7b65ab0a0bcaa2f6d4bde92b,org.opencontainers.image.created=2026-02-04T05:09:09Z
# Thu, 05 Feb 2026 00:08:00 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 05 Feb 2026 00:08:00 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 05 Feb 2026 00:08:00 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 05 Feb 2026 00:08:00 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en         gnupg2     ;     microdnf clean all # buildkit
# Thu, 05 Feb 2026 00:08:00 GMT
ENV JAVA_VERSION=jdk-25.0.2+10
# Thu, 05 Feb 2026 22:25:16 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='e90ad4a618a0228a2126e7c6abfbc0729e2649d7d72cef45fd640239866eb050';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.2%2B10/OpenJDK25U-jre_aarch64_linux_hotspot_25.0.2_10.tar.gz';          ;;        ppc64le)          ESUM='1cc773ab86cbdbb02732398ad4550950db859fb08f8eb6548c8c5e188f697455';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.2%2B10/OpenJDK25U-jre_ppc64le_linux_hotspot_25.0.2_10.tar.gz';          ;;        s390x)          ESUM='ccb977223490643318230b53107aaa23c136d2793b5174dc38d4b0daab9a18e3';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.2%2B10/OpenJDK25U-jre_s390x_linux_hotspot_25.0.2_10.tar.gz';          ;;        x86_64)          ESUM='d6c89e08f42be94cd55eab20190958a35b993625018a3ac59cb3d16d8445cf98';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.2%2B10/OpenJDK25U-jre_x64_linux_hotspot_25.0.2_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz; # buildkit
# Thu, 05 Feb 2026 22:25:16 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 05 Feb 2026 22:25:17 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 05 Feb 2026 22:25:17 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
```

-	Layers:
	-	`sha256:3c5e6ba1d838b1d4e103e0457068eaff01f71c8436e4442eaa2f5c701ccbe1c6`  
		Last Modified: Wed, 04 Feb 2026 06:11:43 GMT  
		Size: 34.4 MB (34399700 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33f62941b4842166327c9c075b3f2cabd375978482a43694cc3006f9826a62ce`  
		Last Modified: Thu, 05 Feb 2026 00:08:22 GMT  
		Size: 37.8 MB (37794446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9637a4ac12e209d19d863cb8fbcd182360505fc342d92bc943cbbc3c71172519`  
		Last Modified: Thu, 05 Feb 2026 22:25:48 GMT  
		Size: 60.2 MB (60226216 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b229f9ceda4569a23d81afe0e9f6c51dbdbd02cf9c3d5fb71f95fbaa584b6f26`  
		Last Modified: Thu, 05 Feb 2026 22:25:47 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14c11cbd1d54156ee174abaec741ca1d1189e971a6db0caf8e1a9984f3cb05ea`  
		Last Modified: Thu, 05 Feb 2026 22:25:46 GMT  
		Size: 2.3 KB (2291 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:25-jre-ubi10-minimal` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:d41192639d3ceb232a7f69a3c5aadce0c54ec08733e05171e10fa391bea0665f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3722577 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e13a3913cfa3355994d1458b61e7b8ec10f47fff6c3c975ef90e44779c17dd92`

```dockerfile
```

-	Layers:
	-	`sha256:7ced0c2e94b3c2945de78593f0de15e58a9b44b54e199293ac6b38dc169bacd0`  
		Last Modified: Thu, 05 Feb 2026 22:25:47 GMT  
		Size: 3.7 MB (3702223 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e4451fc56fa5c89327c5485a96815355639d72d761489f505c059e3f578e2001`  
		Last Modified: Thu, 05 Feb 2026 22:25:46 GMT  
		Size: 20.4 KB (20354 bytes)  
		MIME: application/vnd.in-toto+json
