## `eclipse-temurin:11-jdk-ubi10-minimal`

```console
$ docker pull eclipse-temurin@sha256:c16374cfc3cdfbd9aa15f75636c23973da6d425a8dc3855e54a46d5c6c54027a
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

### `eclipse-temurin:11-jdk-ubi10-minimal` - linux; amd64

```console
$ docker pull eclipse-temurin@sha256:f5abbb3e228179af0cf727b757a2a691dcf38a649f31798c36428bb1f21156dd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **205.9 MB (205900538 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac59e879890fef7e32703a4d8ff799bfb011cac19ee503d0b42f55c0dc3463fc`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 26 May 2026 09:52:44 GMT
LABEL maintainer="Red Hat, Inc."
# Tue, 26 May 2026 09:52:44 GMT
LABEL vendor="Red Hat, Inc."
# Tue, 26 May 2026 09:52:44 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Tue, 26 May 2026 09:52:44 GMT
LABEL com.redhat.component="ubi10-minimal-container"       name="ubi10/ubi-minimal"       version="10.1"       cpe="cpe:/o:redhat:enterprise_linux:10.1"       distribution-scope="public"
# Tue, 26 May 2026 09:52:44 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Tue, 26 May 2026 09:52:44 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 10."
# Tue, 26 May 2026 09:52:44 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Tue, 26 May 2026 09:52:44 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Tue, 26 May 2026 09:52:45 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 10 Minimal"
# Tue, 26 May 2026 09:52:45 GMT
LABEL io.openshift.expose-services=""
# Tue, 26 May 2026 09:52:45 GMT
LABEL io.openshift.tags="minimal rhel10"
# Tue, 26 May 2026 09:52:45 GMT
ENV container oci
# Tue, 26 May 2026 09:52:46 GMT
COPY dir:4a65961322c03a42263a9993a9e455b03f91a19ddc042f14a91b2092bee12ade in /      
# Tue, 26 May 2026 09:52:46 GMT
COPY file:5de33b5fc08b00635bccf9134a18978dba13e2250aa51838f9969515a3957847 in /etc/yum.repos.d/.      
# Tue, 26 May 2026 09:52:46 GMT
CMD ["/bin/bash"]
# Tue, 26 May 2026 09:52:46 GMT
COPY file:595171150af68abc798ea385f7988d74b566aa8e84babff137f00b08b2164683 in /usr/share/buildinfo/content-sets.json      
# Tue, 26 May 2026 09:52:47 GMT
COPY file:595171150af68abc798ea385f7988d74b566aa8e84babff137f00b08b2164683 in /root/buildinfo/content_manifests/content-sets.json      
# Tue, 26 May 2026 09:52:47 GMT
COPY file:3ad71f7fdda6857fd6a2d3e0ee5ab780c0c840fe960653943407106cbf070684 in /usr/share/buildinfo/labels.json      
# Tue, 26 May 2026 09:52:47 GMT
COPY file:3ad71f7fdda6857fd6a2d3e0ee5ab780c0c840fe960653943407106cbf070684 in /root/buildinfo/labels.json      
# Tue, 26 May 2026 09:52:47 GMT
LABEL "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="28a4d5c7cdb1969ee63337adb47fcb350a380874" "org.opencontainers.image.revision"="28a4d5c7cdb1969ee63337adb47fcb350a380874" "build-date"="2026-05-26T09:52:24Z" "org.opencontainers.image.created"="2026-05-26T09:52:24Z" "release"="1779788807"org.opencontainers.image.revision=28a4d5c7cdb1969ee63337adb47fcb350a380874,org.opencontainers.image.created=2026-05-26T09:52:24Z
# Tue, 26 May 2026 23:09:56 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 26 May 2026 23:09:56 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 26 May 2026 23:09:56 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 26 May 2026 23:09:56 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en         gnupg2     ;     microdnf clean all # buildkit
# Tue, 26 May 2026 23:09:56 GMT
ENV JAVA_VERSION=jdk-11.0.31+11
# Tue, 26 May 2026 23:10:02 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='257f4d39e060658fc2eb89a803ca43b3f337e64e253f2d94ebae1d85c9ef5f69';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.31%2B11/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.31_11.tar.gz';          ;;        ppc64le)          ESUM='e473d10c3c44f67301fd90abd9e4b7ae312eae8a2399b333fcf4179daf35a743';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.31%2B11/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.31_11.tar.gz';          ;;        s390x)          ESUM='4d3709cdc03de1a00f14f530c2ebad1883d9bcc8a556fc419f083bec87b4687a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.31%2B11/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.31_11.tar.gz';          ;;        x86_64)          ESUM='1e9de64586b519c0a981319489257cabedd9457599f3823424a87c3158fbe939';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.31%2B11/OpenJDK11U-jdk_x64_linux_hotspot_11.0.31_11.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Tue, 26 May 2026 23:10:04 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 26 May 2026 23:10:04 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 26 May 2026 23:10:04 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 26 May 2026 23:10:04 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:368dae9e745ec994e59731b33513a5334145ab500bb4162a1597ced6ca7d2dd0`  
		Last Modified: Tue, 26 May 2026 11:30:57 GMT  
		Size: 34.6 MB (34624420 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72a642c9dfe94730fdbaac70729d607112b529ca656b7aa88c7d79673e9fceb0`  
		Last Modified: Tue, 26 May 2026 23:10:21 GMT  
		Size: 28.9 MB (28924861 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d100cbc9825cd2f0f7f565f7b5ac4ec97ef9fb0cdd2deaf106491d8119bc7534`  
		Last Modified: Tue, 26 May 2026 23:10:24 GMT  
		Size: 142.3 MB (142348836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4a7771c90c4e4b58ad03ccc4cbe925a606472104dd944723fd4671cee5d6a5b`  
		Last Modified: Tue, 26 May 2026 23:10:20 GMT  
		Size: 130.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd2f909ca4994c7f3324fdf066c4162867c71db6bd4703974f0052ce0adc12af`  
		Last Modified: Tue, 26 May 2026 23:10:20 GMT  
		Size: 2.3 KB (2291 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:11-jdk-ubi10-minimal` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:5efc22a5feef87d50c45701a5204e174f13b4c3111b4a44266c8db9150483d94
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3091369 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3530933977686cca3c91337da164c9738af9e2c5e32d9d2a7d626bd42547ae12`

```dockerfile
```

-	Layers:
	-	`sha256:c52158a205d9dd5fe37f02017f7d033a2f6008fecfba7af9778fcbeea140f627`  
		Last Modified: Tue, 26 May 2026 23:10:20 GMT  
		Size: 3.1 MB (3070029 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a6617dd62fb0702260311ac73ab0cdc13cf74e61bc1532c35319e815f97083a7`  
		Last Modified: Tue, 26 May 2026 23:10:20 GMT  
		Size: 21.3 KB (21340 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-temurin:11-jdk-ubi10-minimal` - linux; arm64 variant v8

```console
$ docker pull eclipse-temurin@sha256:a8647d10f34cb1fa383214d044a27d57f3621123b78f63e8852e38fe5780ee82
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **200.1 MB (200095348 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a6f9fd57e78be534f55a08dc6ccdf82e2c0233fd060adb4469c15273a076de3`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 26 May 2026 09:56:13 GMT
LABEL maintainer="Red Hat, Inc."
# Tue, 26 May 2026 09:56:13 GMT
LABEL vendor="Red Hat, Inc."
# Tue, 26 May 2026 09:56:13 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Tue, 26 May 2026 09:56:13 GMT
LABEL com.redhat.component="ubi10-minimal-container"       name="ubi10/ubi-minimal"       version="10.1"       cpe="cpe:/o:redhat:enterprise_linux:10.1"       distribution-scope="public"
# Tue, 26 May 2026 09:56:13 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Tue, 26 May 2026 09:56:13 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 10."
# Tue, 26 May 2026 09:56:13 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Tue, 26 May 2026 09:56:13 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Tue, 26 May 2026 09:56:13 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 10 Minimal"
# Tue, 26 May 2026 09:56:13 GMT
LABEL io.openshift.expose-services=""
# Tue, 26 May 2026 09:56:13 GMT
LABEL io.openshift.tags="minimal rhel10"
# Tue, 26 May 2026 09:56:13 GMT
ENV container oci
# Tue, 26 May 2026 09:56:14 GMT
COPY dir:ae54dc874bd5ff821c9cac1615bdf50508b14bc07c449a11310a695d880fa906 in /      
# Tue, 26 May 2026 09:56:14 GMT
COPY file:5de33b5fc08b00635bccf9134a18978dba13e2250aa51838f9969515a3957847 in /etc/yum.repos.d/.      
# Tue, 26 May 2026 09:56:14 GMT
CMD ["/bin/bash"]
# Tue, 26 May 2026 09:56:14 GMT
COPY file:595171150af68abc798ea385f7988d74b566aa8e84babff137f00b08b2164683 in /usr/share/buildinfo/content-sets.json      
# Tue, 26 May 2026 09:56:14 GMT
COPY file:595171150af68abc798ea385f7988d74b566aa8e84babff137f00b08b2164683 in /root/buildinfo/content_manifests/content-sets.json      
# Tue, 26 May 2026 09:56:15 GMT
COPY file:cbda7134a1becb5efcab0aac781af893c81e3d1aab44f2af20045a4a249708c1 in /usr/share/buildinfo/labels.json      
# Tue, 26 May 2026 09:56:15 GMT
COPY file:cbda7134a1becb5efcab0aac781af893c81e3d1aab44f2af20045a4a249708c1 in /root/buildinfo/labels.json      
# Tue, 26 May 2026 09:56:15 GMT
LABEL "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="28a4d5c7cdb1969ee63337adb47fcb350a380874" "org.opencontainers.image.revision"="28a4d5c7cdb1969ee63337adb47fcb350a380874" "build-date"="2026-05-26T09:55:58Z" "org.opencontainers.image.created"="2026-05-26T09:55:58Z" "release"="1779788807"org.opencontainers.image.revision=28a4d5c7cdb1969ee63337adb47fcb350a380874,org.opencontainers.image.created=2026-05-26T09:55:58Z
# Tue, 26 May 2026 23:09:43 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 26 May 2026 23:09:43 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 26 May 2026 23:09:43 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 26 May 2026 23:09:43 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en         gnupg2     ;     microdnf clean all # buildkit
# Tue, 26 May 2026 23:09:43 GMT
ENV JAVA_VERSION=jdk-11.0.31+11
# Tue, 26 May 2026 23:09:49 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='257f4d39e060658fc2eb89a803ca43b3f337e64e253f2d94ebae1d85c9ef5f69';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.31%2B11/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.31_11.tar.gz';          ;;        ppc64le)          ESUM='e473d10c3c44f67301fd90abd9e4b7ae312eae8a2399b333fcf4179daf35a743';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.31%2B11/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.31_11.tar.gz';          ;;        s390x)          ESUM='4d3709cdc03de1a00f14f530c2ebad1883d9bcc8a556fc419f083bec87b4687a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.31%2B11/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.31_11.tar.gz';          ;;        x86_64)          ESUM='1e9de64586b519c0a981319489257cabedd9457599f3823424a87c3158fbe939';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.31%2B11/OpenJDK11U-jdk_x64_linux_hotspot_11.0.31_11.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Tue, 26 May 2026 23:09:51 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 26 May 2026 23:09:51 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 26 May 2026 23:09:51 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 26 May 2026 23:09:51 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:d44582f6016d5b17ffe3577358bcbf1bf84edfe2aba6b73b6461e6631e0a4bc7`  
		Last Modified: Tue, 26 May 2026 11:41:50 GMT  
		Size: 32.7 MB (32711602 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34c1df6c230f9d35da82702251db2c1f7d008413743e0abf5a54a62a8f4d276a`  
		Last Modified: Tue, 26 May 2026 23:10:08 GMT  
		Size: 28.3 MB (28340639 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5266e943b72844e9cf78ab2f7a1d4f6a473d59b4465c41de6656cc4dfb03bce8`  
		Last Modified: Tue, 26 May 2026 23:10:10 GMT  
		Size: 139.0 MB (139040690 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0ad3ea6a0513ac72b388b43fcccf014c35a7331a19f09be3ad41f41b3557de0`  
		Last Modified: Tue, 26 May 2026 23:10:06 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e9b10d9183c6fce9189e377f631e52910582a8d3faf0d48e1f27ab7900c3560`  
		Last Modified: Tue, 26 May 2026 23:10:06 GMT  
		Size: 2.3 KB (2290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:11-jdk-ubi10-minimal` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:51ba9defa78122435504a3f654eb99946b84b2e4ca952d8127a00fce87343966
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3091529 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a36ee9c544be58541841a5bd369b7f2a0415e71096947ec1f8d0f378d81b131f`

```dockerfile
```

-	Layers:
	-	`sha256:099b6839fd7b24b73331c97f4cd470d32db6e473220c5f1377bfab8059406921`  
		Last Modified: Tue, 26 May 2026 23:10:07 GMT  
		Size: 3.1 MB (3070073 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:196f4755de235072c0aed39eb5eb774325c7b6425da3f099867ba4b135b400d7`  
		Last Modified: Tue, 26 May 2026 23:10:06 GMT  
		Size: 21.5 KB (21456 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-temurin:11-jdk-ubi10-minimal` - linux; ppc64le

```console
$ docker pull eclipse-temurin@sha256:5a44b83401e5ce71eb21ec8828c2bef86e177152fe318de792114220e04be69c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **200.3 MB (200344026 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9294c5c2903ca89d65ab0643f835c0692396c47381125e166a528fdf6970aeb0`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 26 May 2026 10:05:34 GMT
LABEL maintainer="Red Hat, Inc."
# Tue, 26 May 2026 10:05:34 GMT
LABEL vendor="Red Hat, Inc."
# Tue, 26 May 2026 10:05:34 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Tue, 26 May 2026 10:05:34 GMT
LABEL com.redhat.component="ubi10-minimal-container"       name="ubi10/ubi-minimal"       version="10.1"       cpe="cpe:/o:redhat:enterprise_linux:10.1"       distribution-scope="public"
# Tue, 26 May 2026 10:05:35 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Tue, 26 May 2026 10:05:35 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 10."
# Tue, 26 May 2026 10:05:35 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Tue, 26 May 2026 10:05:35 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Tue, 26 May 2026 10:05:35 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 10 Minimal"
# Tue, 26 May 2026 10:05:35 GMT
LABEL io.openshift.expose-services=""
# Tue, 26 May 2026 10:05:35 GMT
LABEL io.openshift.tags="minimal rhel10"
# Tue, 26 May 2026 10:05:35 GMT
ENV container oci
# Tue, 26 May 2026 10:05:37 GMT
COPY dir:d4fda96d22b28f66ff1bcd2a6fa4e35fa9ad60695678918f055282f9b91f573c in /      
# Tue, 26 May 2026 10:05:37 GMT
COPY file:5de33b5fc08b00635bccf9134a18978dba13e2250aa51838f9969515a3957847 in /etc/yum.repos.d/.      
# Tue, 26 May 2026 10:05:37 GMT
CMD ["/bin/bash"]
# Tue, 26 May 2026 10:05:37 GMT
COPY file:595171150af68abc798ea385f7988d74b566aa8e84babff137f00b08b2164683 in /usr/share/buildinfo/content-sets.json      
# Tue, 26 May 2026 10:05:37 GMT
COPY file:595171150af68abc798ea385f7988d74b566aa8e84babff137f00b08b2164683 in /root/buildinfo/content_manifests/content-sets.json      
# Tue, 26 May 2026 10:05:38 GMT
COPY file:5e4784a2db9f1899592c7ac2b4556c3bb602168493a8e32d224b97a462909960 in /usr/share/buildinfo/labels.json      
# Tue, 26 May 2026 10:05:38 GMT
COPY file:5e4784a2db9f1899592c7ac2b4556c3bb602168493a8e32d224b97a462909960 in /root/buildinfo/labels.json      
# Tue, 26 May 2026 10:05:39 GMT
LABEL "architecture"="ppc64le" "vcs-type"="git" "vcs-ref"="28a4d5c7cdb1969ee63337adb47fcb350a380874" "org.opencontainers.image.revision"="28a4d5c7cdb1969ee63337adb47fcb350a380874" "build-date"="2026-05-26T10:05:11Z" "org.opencontainers.image.created"="2026-05-26T10:05:11Z" "release"="1779788807"org.opencontainers.image.revision=28a4d5c7cdb1969ee63337adb47fcb350a380874,org.opencontainers.image.created=2026-05-26T10:05:11Z
# Tue, 26 May 2026 23:08:26 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 26 May 2026 23:08:26 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 26 May 2026 23:08:26 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 26 May 2026 23:08:26 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en         gnupg2     ;     microdnf clean all # buildkit
# Tue, 26 May 2026 23:08:26 GMT
ENV JAVA_VERSION=jdk-11.0.31+11
# Tue, 26 May 2026 23:09:59 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='257f4d39e060658fc2eb89a803ca43b3f337e64e253f2d94ebae1d85c9ef5f69';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.31%2B11/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.31_11.tar.gz';          ;;        ppc64le)          ESUM='e473d10c3c44f67301fd90abd9e4b7ae312eae8a2399b333fcf4179daf35a743';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.31%2B11/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.31_11.tar.gz';          ;;        s390x)          ESUM='4d3709cdc03de1a00f14f530c2ebad1883d9bcc8a556fc419f083bec87b4687a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.31%2B11/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.31_11.tar.gz';          ;;        x86_64)          ESUM='1e9de64586b519c0a981319489257cabedd9457599f3823424a87c3158fbe939';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.31%2B11/OpenJDK11U-jdk_x64_linux_hotspot_11.0.31_11.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Tue, 26 May 2026 23:10:02 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 26 May 2026 23:10:03 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 26 May 2026 23:10:03 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 26 May 2026 23:10:03 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:b4743f929036f49c12be6a577cbf8dbf4b9feeebdd83aef3c82da2056289053c`  
		Last Modified: Tue, 26 May 2026 12:17:22 GMT  
		Size: 38.8 MB (38794684 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e600a5e4b5bd9ee674e2def8e4bcf01be8963cfc1697cc6243834b5ac188e995`  
		Last Modified: Tue, 26 May 2026 23:08:57 GMT  
		Size: 31.9 MB (31932676 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:addb3be69484eb93645d5765cf23efe412e0d2d0bb3d729414c2b9b7b1ae79b6`  
		Last Modified: Tue, 26 May 2026 23:10:45 GMT  
		Size: 129.6 MB (129614247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99c0f6bdf8717698b38ab1135a6b8018c65ceaddeff0cf08955469f214e67dd7`  
		Last Modified: Tue, 26 May 2026 23:10:42 GMT  
		Size: 130.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f601c8205ae8a2760558d6d20b007e82c162e7e091098212a778d53d2fdf9eee`  
		Last Modified: Tue, 26 May 2026 23:10:42 GMT  
		Size: 2.3 KB (2289 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:11-jdk-ubi10-minimal` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:58ee9470d8f556fabb73aabf8f68445eb7a3567d3090064b7d0a43e5331c182f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3084546 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e4785999a0184af2989a39bfbf02c96e2d46926f3ee3ae86b327ca01f33ea050`

```dockerfile
```

-	Layers:
	-	`sha256:708090f9ee1f9939d96e75a2df67a662b82293c983af569a65f66da17055e0fd`  
		Last Modified: Tue, 26 May 2026 23:10:42 GMT  
		Size: 3.1 MB (3063170 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7e403296dd108e34c3991299b042b121509c5931dc2cf5253f01aeecc15e562d`  
		Last Modified: Tue, 26 May 2026 23:10:42 GMT  
		Size: 21.4 KB (21376 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-temurin:11-jdk-ubi10-minimal` - linux; s390x

```console
$ docker pull eclipse-temurin@sha256:46d4ac8954b709fd8eaa2cfceb7c8227afe8deec227dde8a31aa1ca1859e9172
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **186.0 MB (186039211 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c1beef9741886513f3ac8e404a0529423ec72d4d27bea3de30c11d20d64dede`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 26 May 2026 10:43:18 GMT
LABEL maintainer="Red Hat, Inc."
# Tue, 26 May 2026 10:43:18 GMT
LABEL vendor="Red Hat, Inc."
# Tue, 26 May 2026 10:43:18 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Tue, 26 May 2026 10:43:18 GMT
LABEL com.redhat.component="ubi10-minimal-container"       name="ubi10/ubi-minimal"       version="10.1"       cpe="cpe:/o:redhat:enterprise_linux:10.1"       distribution-scope="public"
# Tue, 26 May 2026 10:43:18 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Tue, 26 May 2026 10:43:18 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 10."
# Tue, 26 May 2026 10:43:18 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Tue, 26 May 2026 10:43:18 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Tue, 26 May 2026 10:43:18 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 10 Minimal"
# Tue, 26 May 2026 10:43:18 GMT
LABEL io.openshift.expose-services=""
# Tue, 26 May 2026 10:43:18 GMT
LABEL io.openshift.tags="minimal rhel10"
# Tue, 26 May 2026 10:43:18 GMT
ENV container oci
# Tue, 26 May 2026 10:43:19 GMT
COPY dir:a7c5d9f6499c23f09ef7d337bda5192f5b4deca45553e74bfae9fae1b20a60ef in /      
# Tue, 26 May 2026 10:43:19 GMT
COPY file:5de33b5fc08b00635bccf9134a18978dba13e2250aa51838f9969515a3957847 in /etc/yum.repos.d/.      
# Tue, 26 May 2026 10:43:19 GMT
CMD ["/bin/bash"]
# Tue, 26 May 2026 10:43:19 GMT
COPY file:595171150af68abc798ea385f7988d74b566aa8e84babff137f00b08b2164683 in /usr/share/buildinfo/content-sets.json      
# Tue, 26 May 2026 10:43:19 GMT
COPY file:595171150af68abc798ea385f7988d74b566aa8e84babff137f00b08b2164683 in /root/buildinfo/content_manifests/content-sets.json      
# Tue, 26 May 2026 10:43:21 GMT
COPY file:cf7bfba0ea2e3c47e53590ead66a27ae21af2a1dca6091ce8837539a1df6f22a in /usr/share/buildinfo/labels.json      
# Tue, 26 May 2026 10:43:21 GMT
COPY file:cf7bfba0ea2e3c47e53590ead66a27ae21af2a1dca6091ce8837539a1df6f22a in /root/buildinfo/labels.json      
# Tue, 26 May 2026 10:43:22 GMT
LABEL "architecture"="s390x" "vcs-type"="git" "vcs-ref"="28a4d5c7cdb1969ee63337adb47fcb350a380874" "org.opencontainers.image.revision"="28a4d5c7cdb1969ee63337adb47fcb350a380874" "build-date"="2026-05-26T10:43:06Z" "org.opencontainers.image.created"="2026-05-26T10:43:06Z" "release"="1779788807"org.opencontainers.image.revision=28a4d5c7cdb1969ee63337adb47fcb350a380874,org.opencontainers.image.created=2026-05-26T10:43:06Z
# Tue, 26 May 2026 23:08:25 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 26 May 2026 23:08:25 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 26 May 2026 23:08:25 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 26 May 2026 23:08:25 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en         gnupg2     ;     microdnf clean all # buildkit
# Tue, 26 May 2026 23:08:25 GMT
ENV JAVA_VERSION=jdk-11.0.31+11
# Tue, 26 May 2026 23:08:31 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='257f4d39e060658fc2eb89a803ca43b3f337e64e253f2d94ebae1d85c9ef5f69';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.31%2B11/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.31_11.tar.gz';          ;;        ppc64le)          ESUM='e473d10c3c44f67301fd90abd9e4b7ae312eae8a2399b333fcf4179daf35a743';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.31%2B11/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.31_11.tar.gz';          ;;        s390x)          ESUM='4d3709cdc03de1a00f14f530c2ebad1883d9bcc8a556fc419f083bec87b4687a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.31%2B11/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.31_11.tar.gz';          ;;        x86_64)          ESUM='1e9de64586b519c0a981319489257cabedd9457599f3823424a87c3158fbe939';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.31%2B11/OpenJDK11U-jdk_x64_linux_hotspot_11.0.31_11.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Tue, 26 May 2026 23:08:33 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 26 May 2026 23:08:33 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 26 May 2026 23:08:33 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 26 May 2026 23:08:33 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:3f3af3c01ebb5e415417fa01cdc18de3e0533f557596f831f5cdf4441dd071e3`  
		Last Modified: Tue, 26 May 2026 12:17:14 GMT  
		Size: 34.4 MB (34449572 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c036331f082117718d32b7a6dcfa78b23ee5fa1dcd892f2d797f021397b44fb8`  
		Last Modified: Tue, 26 May 2026 23:08:58 GMT  
		Size: 28.5 MB (28525803 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c404615501b691f910e581aaacb2fe7baa2fe758777fef6d4e6667c933fb85b6`  
		Last Modified: Tue, 26 May 2026 23:09:00 GMT  
		Size: 123.1 MB (123061416 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:916c118fd0f0db625b4753b69dd73913de1df284d1c9fff867469f4f973ac56f`  
		Last Modified: Tue, 26 May 2026 23:08:57 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27ac5c36f79853313b82c616b9ae74eb74d427dacc63001d3041c97ef3ca2293`  
		Last Modified: Tue, 26 May 2026 23:08:57 GMT  
		Size: 2.3 KB (2291 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:11-jdk-ubi10-minimal` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:468fcda798cf4129e9cf3ccd8c60b34e567945604d6b1f1776a47df28f7e13ee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3083887 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b3948799fb279617d01191641db3b4ab9e4eaa0eba67db654e9e0541bdec540a`

```dockerfile
```

-	Layers:
	-	`sha256:89a70fc8eae4c1a733c6a302401021ddbbb7fb2d5c0b179aa9da647efa445b9d`  
		Last Modified: Tue, 26 May 2026 23:08:57 GMT  
		Size: 3.1 MB (3062547 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:147898a46c06b8b8f369f81cb7a790860005c6a436897d0ed680f2df62146a3d`  
		Last Modified: Tue, 26 May 2026 23:08:57 GMT  
		Size: 21.3 KB (21340 bytes)  
		MIME: application/vnd.in-toto+json
