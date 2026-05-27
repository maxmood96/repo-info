## `eclipse-temurin:8-jdk-ubi10-minimal`

```console
$ docker pull eclipse-temurin@sha256:b511ea52640785965780301070f2fc98af754a2e3e8d0a4bde6033aff6da52ad
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
$ docker pull eclipse-temurin@sha256:d9b23e63e74be4c829ea8069a2b834ac8ef22f3d3375f4e5c08d3db8e5ee7012
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **118.8 MB (118751118 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f20b67b4eef1ab747af3ff4132716a22bb154bf0d4139f2d6f1c5d753338833`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`

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
# Tue, 26 May 2026 23:09:49 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 26 May 2026 23:09:49 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 26 May 2026 23:09:49 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 26 May 2026 23:09:49 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en         gnupg2     ;     microdnf clean all # buildkit
# Tue, 26 May 2026 23:09:49 GMT
ENV JAVA_VERSION=jdk8u492-b09
# Tue, 26 May 2026 23:09:52 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='3c2253b986909c20f79d6de7a0cb957f89c243df57615897836046e24d2e5257';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u492-b09/OpenJDK8U-jdk_aarch64_linux_hotspot_8u492b09.tar.gz';          ;;        ppc64le)          ESUM='867e477e0a54159c7b774c55cfb046767120b1de43f705fa775ece74ea39e341';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u492-b09/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u492b09.tar.gz';          ;;        x86_64)          ESUM='da257f161d7f8c6ca5b0e5d9e4090f65ac28c5e398072e68b8ae87988b1d1a2e';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u492-b09/OpenJDK8U-jdk_x64_linux_hotspot_8u492b09.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip; # buildkit
# Tue, 26 May 2026 23:09:52 GMT
RUN set -eux;     echo "Verifying install ...";     echo "javac -version"; javac -version;     echo "java -version"; java -version;     echo "Complete." # buildkit
# Tue, 26 May 2026 23:09:52 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 26 May 2026 23:09:52 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
```

-	Layers:
	-	`sha256:368dae9e745ec994e59731b33513a5334145ab500bb4162a1597ced6ca7d2dd0`  
		Last Modified: Tue, 26 May 2026 11:30:57 GMT  
		Size: 34.6 MB (34624420 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac43716a98b08ec944c38a5449fb0b465e93449d83d0f1299c6e6770b7eed13f`  
		Last Modified: Tue, 26 May 2026 23:10:06 GMT  
		Size: 28.9 MB (28924933 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74297fb05da7ac51d7f61b4ea3f73c1ae6477a3c17b7343a538db96bcec00e02`  
		Last Modified: Tue, 26 May 2026 23:10:07 GMT  
		Size: 55.2 MB (55199149 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f1928a25316231133f3170e0a6fc22420792abae460d26576538b3d5894c268`  
		Last Modified: Tue, 26 May 2026 23:10:05 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d6a993e7e9d5662f98202513c1f3c9cdcf596fdbef6b20e5ec615537afa1d17`  
		Last Modified: Tue, 26 May 2026 23:10:06 GMT  
		Size: 2.5 KB (2490 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:8-jdk-ubi10-minimal` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:73f7994190fec54750ce12ac51ec0d93bd93f07971316e577b22c8cfcd34b707
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3191537 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:960d904971659633e859c5e8ca1dd84148c629dafa33767ffdbbca3ab2a3d3d0`

```dockerfile
```

-	Layers:
	-	`sha256:5b85758a18befaf5309b87a498481e863266fcc473cab095e9b8355d350032e6`  
		Last Modified: Tue, 26 May 2026 23:10:05 GMT  
		Size: 3.2 MB (3171498 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b196290e60b281ea1ea0240027dbc0198f4e4d102311d60666a009862b7431de`  
		Last Modified: Tue, 26 May 2026 23:10:05 GMT  
		Size: 20.0 KB (20039 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-temurin:8-jdk-ubi10-minimal` - linux; arm64 variant v8

```console
$ docker pull eclipse-temurin@sha256:a96191a85edd7a64b1489eb50541725e2a0de6ea2315ff8e37fc6ae82ed1e855
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.3 MB (115328365 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd26bf614004e128b6502d43aef3259e54abe1df395b841311674ba39a63e772`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`

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
# Tue, 26 May 2026 23:09:28 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 26 May 2026 23:09:28 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 26 May 2026 23:09:28 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 26 May 2026 23:09:28 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en         gnupg2     ;     microdnf clean all # buildkit
# Tue, 26 May 2026 23:09:28 GMT
ENV JAVA_VERSION=jdk8u492-b09
# Tue, 26 May 2026 23:09:32 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='3c2253b986909c20f79d6de7a0cb957f89c243df57615897836046e24d2e5257';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u492-b09/OpenJDK8U-jdk_aarch64_linux_hotspot_8u492b09.tar.gz';          ;;        ppc64le)          ESUM='867e477e0a54159c7b774c55cfb046767120b1de43f705fa775ece74ea39e341';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u492-b09/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u492b09.tar.gz';          ;;        x86_64)          ESUM='da257f161d7f8c6ca5b0e5d9e4090f65ac28c5e398072e68b8ae87988b1d1a2e';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u492-b09/OpenJDK8U-jdk_x64_linux_hotspot_8u492b09.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip; # buildkit
# Tue, 26 May 2026 23:09:32 GMT
RUN set -eux;     echo "Verifying install ...";     echo "javac -version"; javac -version;     echo "java -version"; java -version;     echo "Complete." # buildkit
# Tue, 26 May 2026 23:09:32 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 26 May 2026 23:09:32 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
```

-	Layers:
	-	`sha256:d44582f6016d5b17ffe3577358bcbf1bf84edfe2aba6b73b6461e6631e0a4bc7`  
		Last Modified: Tue, 26 May 2026 11:41:50 GMT  
		Size: 32.7 MB (32711602 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c82da0058728c17c560896c5b358d675eedf5bf5b7a5c1a27b6bb1fa6309d43`  
		Last Modified: Tue, 26 May 2026 23:09:46 GMT  
		Size: 28.3 MB (28340714 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31471cba9dac7b68e411e94c6a9e5c66155361b45827ab95cd0079406137a234`  
		Last Modified: Tue, 26 May 2026 23:09:47 GMT  
		Size: 54.3 MB (54273431 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42af1d6c4fb4e288c44ff43794c44fa627c6873047391e53a92bf9aef1e00eb7`  
		Last Modified: Tue, 26 May 2026 23:09:45 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:217428d3a4242e2549d9bdd1dd0a34fc3a04f995049b9807b7299714957b5ae1`  
		Last Modified: Tue, 26 May 2026 23:09:45 GMT  
		Size: 2.5 KB (2490 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:8-jdk-ubi10-minimal` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:83a5d56c17faf2295dddf58949906b10ba8e81c348b40bc759cffd285e00ea81
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3191779 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1575afcfd1b5020a6f47e87f5646b219f89a2f120371beb7095362ef2d7201f8`

```dockerfile
```

-	Layers:
	-	`sha256:c29d4478236f94b116b55af66e9db21593d96f351406b86f7fb592a86d455a1a`  
		Last Modified: Tue, 26 May 2026 23:09:45 GMT  
		Size: 3.2 MB (3171624 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fbc5adcfc16111b271c83de812844c792084cc30fd4cb2a247221d56e4975db4`  
		Last Modified: Tue, 26 May 2026 23:09:45 GMT  
		Size: 20.2 KB (20155 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-temurin:8-jdk-ubi10-minimal` - linux; ppc64le

```console
$ docker pull eclipse-temurin@sha256:39e390775b814d2e8949f8bf2c5204e4b750a00a535f8e4271b677d1e9d3f5cc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **123.4 MB (123399688 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c56f25e490ea1d046e9097ca7f70cc389ecf7d63402d31f79f8fdabe3ba358e`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`

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
ENV JAVA_VERSION=jdk8u492-b09
# Tue, 26 May 2026 23:08:31 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='3c2253b986909c20f79d6de7a0cb957f89c243df57615897836046e24d2e5257';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u492-b09/OpenJDK8U-jdk_aarch64_linux_hotspot_8u492b09.tar.gz';          ;;        ppc64le)          ESUM='867e477e0a54159c7b774c55cfb046767120b1de43f705fa775ece74ea39e341';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u492-b09/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u492b09.tar.gz';          ;;        x86_64)          ESUM='da257f161d7f8c6ca5b0e5d9e4090f65ac28c5e398072e68b8ae87988b1d1a2e';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u492-b09/OpenJDK8U-jdk_x64_linux_hotspot_8u492b09.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip; # buildkit
# Tue, 26 May 2026 23:08:31 GMT
RUN set -eux;     echo "Verifying install ...";     echo "javac -version"; javac -version;     echo "java -version"; java -version;     echo "Complete." # buildkit
# Tue, 26 May 2026 23:08:32 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 26 May 2026 23:08:32 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
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
	-	`sha256:8174f3ee08e37872394145946983bc169d13d059da1131cfcba4c8d714b21375`  
		Last Modified: Tue, 26 May 2026 23:08:58 GMT  
		Size: 52.7 MB (52669712 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f04b7e39988beecda6f90ccdac19ea0bc11feec23805ab8ad078ea8af4da8e65`  
		Last Modified: Tue, 26 May 2026 23:08:51 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f653c0a4aefaad96a45db30ef4df064deb635d814a3161ec9097a4489f0d358a`  
		Last Modified: Tue, 26 May 2026 23:08:56 GMT  
		Size: 2.5 KB (2490 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:8-jdk-ubi10-minimal` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:ff60a80478d85432f6c9fb21ca646217bee82ed74498fa0154da09f57fdd9eac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3185924 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:38177b04955e0e57ca0550fe95da02894e7a81513d9c9c8eff79adf216dba5d0`

```dockerfile
```

-	Layers:
	-	`sha256:ab6c57f9995d6869154dc5e7697a02866f6c3952a4b69327b99a9dd982a13c53`  
		Last Modified: Tue, 26 May 2026 23:08:55 GMT  
		Size: 3.2 MB (3165849 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0e9332c8fbfaab9100efd0039b3283de4c5503cfdfdf70f4453fc695f01a5a41`  
		Last Modified: Tue, 26 May 2026 23:08:55 GMT  
		Size: 20.1 KB (20075 bytes)  
		MIME: application/vnd.in-toto+json
