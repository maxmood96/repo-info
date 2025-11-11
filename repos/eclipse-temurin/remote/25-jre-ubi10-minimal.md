## `eclipse-temurin:25-jre-ubi10-minimal`

```console
$ docker pull eclipse-temurin@sha256:fe531a3941222142faaee1624f7f518f54812837a42fb1c8fb435a25f99a164e
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
$ docker pull eclipse-temurin@sha256:9d473961afc7f1c87f4ab9c12879a8b24b7c65a974b9ae8983d62bc3f44e92c2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **156.9 MB (156899703 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:90f11db900c53b6ecc6e4b26b43051e0e95768413e8b5ba5d38d6f6ca11f2262`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`

```dockerfile
# Mon, 10 Nov 2025 09:00:40 GMT
LABEL maintainer="Red Hat, Inc."
# Mon, 10 Nov 2025 09:00:40 GMT
LABEL vendor="Red Hat, Inc."
# Mon, 10 Nov 2025 09:00:40 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Mon, 10 Nov 2025 09:00:40 GMT
LABEL com.redhat.component="ubi10-minimal-container"       name="ubi10/ubi-minimal"       version="10.0"       cpe="cpe:/o:redhat:enterprise_linux:10.0"       distribution-scope="public"
# Mon, 10 Nov 2025 09:00:40 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Mon, 10 Nov 2025 09:00:40 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 10."
# Mon, 10 Nov 2025 09:00:40 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 10 Nov 2025 09:00:40 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 10 Nov 2025 09:00:41 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 10 Minimal"
# Mon, 10 Nov 2025 09:00:41 GMT
LABEL io.openshift.expose-services=""
# Mon, 10 Nov 2025 09:00:41 GMT
LABEL io.openshift.tags="minimal rhel10"
# Mon, 10 Nov 2025 09:00:41 GMT
ENV container oci
# Mon, 10 Nov 2025 09:00:41 GMT
COPY dir:1151487a8fe49bf6a88ef514a8355cedfdeab84f41175ca19d399c25d56e0756 in /      
# Mon, 10 Nov 2025 09:00:41 GMT
COPY file:5de33b5fc08b00635bccf9134a18978dba13e2250aa51838f9969515a3957847 in /etc/yum.repos.d/.      
# Mon, 10 Nov 2025 09:00:41 GMT
CMD ["/bin/bash"]
# Mon, 10 Nov 2025 09:00:41 GMT
COPY file:595171150af68abc798ea385f7988d74b566aa8e84babff137f00b08b2164683 in /usr/share/buildinfo/content-sets.json      
# Mon, 10 Nov 2025 09:00:41 GMT
COPY file:595171150af68abc798ea385f7988d74b566aa8e84babff137f00b08b2164683 in /root/buildinfo/content_manifests/content-sets.json      
# Mon, 10 Nov 2025 09:00:41 GMT
COPY file:78d340a91825c21b9da1409e53e49b8dfe282306bad9ddfd7c9094f83382378e in /usr/share/buildinfo/labels.json      
# Mon, 10 Nov 2025 09:00:41 GMT
COPY file:78d340a91825c21b9da1409e53e49b8dfe282306bad9ddfd7c9094f83382378e in /root/buildinfo/labels.json      
# Mon, 10 Nov 2025 09:00:42 GMT
LABEL "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="18068ad623ccc46f729e7cefa6bb8063513ecab3" "org.opencontainers.image.revision"="18068ad623ccc46f729e7cefa6bb8063513ecab3" "build-date"="2025-11-10T09:00:19Z" "release"="1762765041"org.opencontainers.image.revision=18068ad623ccc46f729e7cefa6bb8063513ecab3
# Mon, 10 Nov 2025 20:10:30 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 10 Nov 2025 20:10:30 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 10 Nov 2025 20:10:30 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 10 Nov 2025 20:10:30 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en         gnupg2     ;     microdnf clean all # buildkit
# Mon, 10 Nov 2025 20:10:30 GMT
ENV JAVA_VERSION=jdk-25.0.1+8
# Mon, 10 Nov 2025 20:11:02 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='5371ad922cb4ff571a57c8e5dd14485ebf5b3994cd71e6ea09088312de3bed71';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.1%2B8/OpenJDK25U-jre_aarch64_linux_hotspot_25.0.1_8.tar.gz';          ;;        ppc64le)          ESUM='c812bf806d7ffcd290c6bd814324aa81f0688e2d682fd0b87e2c7c76251a4f2c';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.1%2B8/OpenJDK25U-jre_ppc64le_linux_hotspot_25.0.1_8.tar.gz';          ;;        s390x)          ESUM='c58764b69cb70e7b532f50e8a20e74aa5cb65e85c3e500225e0b64719a6021a0';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.1%2B8/OpenJDK25U-jre_s390x_linux_hotspot_25.0.1_8.tar.gz';          ;;        x86_64)          ESUM='126c7f59b91df97b2e930b0a456422ce29af7f2385117e1c04297eba962b0b1c';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.1%2B8/OpenJDK25U-jre_x64_linux_hotspot_25.0.1_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz; # buildkit
# Mon, 10 Nov 2025 20:11:02 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Mon, 10 Nov 2025 20:11:02 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Mon, 10 Nov 2025 20:11:02 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
```

-	Layers:
	-	`sha256:32b34b6043df53356073fca74558aa4fb64fa2c3d92bc988ada13ba9600db416`  
		Last Modified: Mon, 10 Nov 2025 12:11:59 GMT  
		Size: 33.4 MB (33442309 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8cea1799586f03658b0a5b52e50fbf50deb4e06c8c03463ae4b6f5423231d60`  
		Last Modified: Mon, 10 Nov 2025 20:11:01 GMT  
		Size: 60.9 MB (60858982 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95a6c8a9975b71bd6b36f7aa35cb57422198a5c2446bebb64de7b2f8eb313b46`  
		Last Modified: Mon, 10 Nov 2025 20:11:33 GMT  
		Size: 62.6 MB (62595992 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c357f2e2df61b865f597d08a2890ac2e789ebd75541d94c2dc1a40132ada9116`  
		Last Modified: Mon, 10 Nov 2025 20:11:22 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a444b0c8b7abbc22944da7fb481a11a666e4046acd9c3056e88e301cbc498db`  
		Last Modified: Mon, 10 Nov 2025 20:11:22 GMT  
		Size: 2.3 KB (2292 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:25-jre-ubi10-minimal` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:ea7e14604406359a35de6c964315503c9c1ac0cfae2de18ba853439ec6f6712a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5619209 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a2fb84dba2e66ac004bd1139681c2e9853679d9f1dd45d830cd31fe62391a62`

```dockerfile
```

-	Layers:
	-	`sha256:54bd3e2eca7dc9faa160fbd69e77996731b5013dcc4cb124c2187a13ea566471`  
		Last Modified: Mon, 10 Nov 2025 22:15:58 GMT  
		Size: 5.6 MB (5598879 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0f56a1f2730510226aeccedc1d801e7619e349b2e0be2eac1f2672b5a4579962`  
		Last Modified: Mon, 10 Nov 2025 22:15:59 GMT  
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
$ docker pull eclipse-temurin@sha256:180cae8329575eb3986a7dc3c2f8fa58e7d61fe77715944d5e2b356ed794d366
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **163.1 MB (163129046 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:88f69387372b35c0baa5fe28a24527cd0f14f8d32c76b132b3ef53de8e4346b0`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`

```dockerfile
# Mon, 10 Nov 2025 09:07:33 GMT
LABEL maintainer="Red Hat, Inc."
# Mon, 10 Nov 2025 09:07:33 GMT
LABEL vendor="Red Hat, Inc."
# Mon, 10 Nov 2025 09:07:33 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Mon, 10 Nov 2025 09:07:33 GMT
LABEL com.redhat.component="ubi10-minimal-container"       name="ubi10/ubi-minimal"       version="10.0"       cpe="cpe:/o:redhat:enterprise_linux:10.0"       distribution-scope="public"
# Mon, 10 Nov 2025 09:07:33 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Mon, 10 Nov 2025 09:07:33 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 10."
# Mon, 10 Nov 2025 09:07:33 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 10 Nov 2025 09:07:33 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 10 Nov 2025 09:07:33 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 10 Minimal"
# Mon, 10 Nov 2025 09:07:33 GMT
LABEL io.openshift.expose-services=""
# Mon, 10 Nov 2025 09:07:33 GMT
LABEL io.openshift.tags="minimal rhel10"
# Mon, 10 Nov 2025 09:07:33 GMT
ENV container oci
# Mon, 10 Nov 2025 09:07:33 GMT
COPY dir:3b3b10e38b1604be9ad4399ace6288103b3f832d58ec15ea17ba00ea93e2b9f7 in /      
# Mon, 10 Nov 2025 09:07:33 GMT
COPY file:5de33b5fc08b00635bccf9134a18978dba13e2250aa51838f9969515a3957847 in /etc/yum.repos.d/.      
# Mon, 10 Nov 2025 09:07:33 GMT
CMD ["/bin/bash"]
# Mon, 10 Nov 2025 09:07:33 GMT
COPY file:595171150af68abc798ea385f7988d74b566aa8e84babff137f00b08b2164683 in /usr/share/buildinfo/content-sets.json      
# Mon, 10 Nov 2025 09:07:34 GMT
COPY file:595171150af68abc798ea385f7988d74b566aa8e84babff137f00b08b2164683 in /root/buildinfo/content_manifests/content-sets.json      
# Mon, 10 Nov 2025 09:07:34 GMT
COPY file:c064500eaa9793e932d2f4ef045195d7141f0508959d80bc76c0e4b59b13a481 in /usr/share/buildinfo/labels.json      
# Mon, 10 Nov 2025 09:07:34 GMT
COPY file:c064500eaa9793e932d2f4ef045195d7141f0508959d80bc76c0e4b59b13a481 in /root/buildinfo/labels.json      
# Mon, 10 Nov 2025 09:07:34 GMT
LABEL "architecture"="ppc64le" "vcs-type"="git" "vcs-ref"="18068ad623ccc46f729e7cefa6bb8063513ecab3" "org.opencontainers.image.revision"="18068ad623ccc46f729e7cefa6bb8063513ecab3" "build-date"="2025-11-10T09:07:22Z" "release"="1762765041"org.opencontainers.image.revision=18068ad623ccc46f729e7cefa6bb8063513ecab3
# Mon, 10 Nov 2025 22:20:01 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 10 Nov 2025 22:20:01 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 10 Nov 2025 22:20:01 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 10 Nov 2025 22:20:01 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en         gnupg2     ;     microdnf clean all # buildkit
# Mon, 10 Nov 2025 22:20:01 GMT
ENV JAVA_VERSION=jdk-25.0.1+8
# Mon, 10 Nov 2025 22:29:03 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='5371ad922cb4ff571a57c8e5dd14485ebf5b3994cd71e6ea09088312de3bed71';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.1%2B8/OpenJDK25U-jre_aarch64_linux_hotspot_25.0.1_8.tar.gz';          ;;        ppc64le)          ESUM='c812bf806d7ffcd290c6bd814324aa81f0688e2d682fd0b87e2c7c76251a4f2c';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.1%2B8/OpenJDK25U-jre_ppc64le_linux_hotspot_25.0.1_8.tar.gz';          ;;        s390x)          ESUM='c58764b69cb70e7b532f50e8a20e74aa5cb65e85c3e500225e0b64719a6021a0';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.1%2B8/OpenJDK25U-jre_s390x_linux_hotspot_25.0.1_8.tar.gz';          ;;        x86_64)          ESUM='126c7f59b91df97b2e930b0a456422ce29af7f2385117e1c04297eba962b0b1c';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.1%2B8/OpenJDK25U-jre_x64_linux_hotspot_25.0.1_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz; # buildkit
# Mon, 10 Nov 2025 22:29:04 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Mon, 10 Nov 2025 22:29:05 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Mon, 10 Nov 2025 22:29:05 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
```

-	Layers:
	-	`sha256:4228be713e86c1bedeefae4a08794664efeed4203b55a759503d7eaba4964702`  
		Last Modified: Mon, 10 Nov 2025 12:12:00 GMT  
		Size: 36.8 MB (36758319 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:176c50dcfec7b2b334fc4e91aecba50a60520f8dc961a0ec542db5fcf328613c`  
		Last Modified: Mon, 10 Nov 2025 22:21:05 GMT  
		Size: 64.3 MB (64337609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22617b640a1049778b46ffae8db6bfba544ddce59aa2a124c644028d6ae1c574`  
		Last Modified: Mon, 10 Nov 2025 22:29:49 GMT  
		Size: 62.0 MB (62030699 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84d6e6c8fe0f15ec7b2496e75314c5a54efb4c7e5c88d8d4e2379d33fc28d2b2`  
		Last Modified: Mon, 10 Nov 2025 22:29:45 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8ffeec78d2f040716180b7f874a6197a186297273c1893701e93cc297397b82`  
		Last Modified: Mon, 10 Nov 2025 22:29:45 GMT  
		Size: 2.3 KB (2291 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:25-jre-ubi10-minimal` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:815ae5b31a68749d6d8ee65092c1bc0dc273a4e5aedb26adf9996d82501660d1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5607683 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e82f7f42d876470886bb797c11faffc5791e437712a9baf9c89ddedffcc9609`

```dockerfile
```

-	Layers:
	-	`sha256:f7ad24db4266a4a1f16e0501da5e0541447521b877183b8a236f5e4d9877e28d`  
		Last Modified: Tue, 11 Nov 2025 01:15:19 GMT  
		Size: 5.6 MB (5587323 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c084bb88d493e79cdfb6414f44c2c40c4ede3079fc181c87f8da10fcee473e24`  
		Last Modified: Tue, 11 Nov 2025 01:15:20 GMT  
		Size: 20.4 KB (20360 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-temurin:25-jre-ubi10-minimal` - linux; s390x

```console
$ docker pull eclipse-temurin@sha256:7551b982fbc17c78061a97337af1521420fe77efd9e7aa911b729a193f36a2bc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **154.6 MB (154555866 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:05e1f00953befff9fb747b7ddb7353dbd8e149b2a9062fa5fb919f2e8152cd18`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`

```dockerfile
# Mon, 10 Nov 2025 09:29:45 GMT
LABEL maintainer="Red Hat, Inc."
# Mon, 10 Nov 2025 09:29:45 GMT
LABEL vendor="Red Hat, Inc."
# Mon, 10 Nov 2025 09:29:45 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Mon, 10 Nov 2025 09:29:45 GMT
LABEL com.redhat.component="ubi10-minimal-container"       name="ubi10/ubi-minimal"       version="10.0"       cpe="cpe:/o:redhat:enterprise_linux:10.0"       distribution-scope="public"
# Mon, 10 Nov 2025 09:29:45 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Mon, 10 Nov 2025 09:29:45 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 10."
# Mon, 10 Nov 2025 09:29:45 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 10 Nov 2025 09:29:45 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 10 Nov 2025 09:29:45 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 10 Minimal"
# Mon, 10 Nov 2025 09:29:45 GMT
LABEL io.openshift.expose-services=""
# Mon, 10 Nov 2025 09:29:45 GMT
LABEL io.openshift.tags="minimal rhel10"
# Mon, 10 Nov 2025 09:29:45 GMT
ENV container oci
# Mon, 10 Nov 2025 09:29:46 GMT
COPY dir:6c57839ff9e4376687d005b2dd39ccb2cab51f91439029283a68660066f453ce in /      
# Mon, 10 Nov 2025 09:29:46 GMT
COPY file:5de33b5fc08b00635bccf9134a18978dba13e2250aa51838f9969515a3957847 in /etc/yum.repos.d/.      
# Mon, 10 Nov 2025 09:29:46 GMT
CMD ["/bin/bash"]
# Mon, 10 Nov 2025 09:29:46 GMT
COPY file:595171150af68abc798ea385f7988d74b566aa8e84babff137f00b08b2164683 in /usr/share/buildinfo/content-sets.json      
# Mon, 10 Nov 2025 09:29:46 GMT
COPY file:595171150af68abc798ea385f7988d74b566aa8e84babff137f00b08b2164683 in /root/buildinfo/content_manifests/content-sets.json      
# Mon, 10 Nov 2025 09:29:46 GMT
COPY file:e7aca2e85df2b708be29fcf6492e0a97a7c66021e1c9892fbb96b00e6743eb74 in /usr/share/buildinfo/labels.json      
# Mon, 10 Nov 2025 09:29:47 GMT
COPY file:e7aca2e85df2b708be29fcf6492e0a97a7c66021e1c9892fbb96b00e6743eb74 in /root/buildinfo/labels.json      
# Mon, 10 Nov 2025 09:29:47 GMT
LABEL "architecture"="s390x" "vcs-type"="git" "vcs-ref"="18068ad623ccc46f729e7cefa6bb8063513ecab3" "org.opencontainers.image.revision"="18068ad623ccc46f729e7cefa6bb8063513ecab3" "build-date"="2025-11-10T09:27:31Z" "release"="1762765041"org.opencontainers.image.revision=18068ad623ccc46f729e7cefa6bb8063513ecab3
# Mon, 10 Nov 2025 21:51:19 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 10 Nov 2025 21:51:19 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 10 Nov 2025 21:51:19 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 10 Nov 2025 21:51:19 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en         gnupg2     ;     microdnf clean all # buildkit
# Mon, 10 Nov 2025 21:51:19 GMT
ENV JAVA_VERSION=jdk-25.0.1+8
# Mon, 10 Nov 2025 21:57:55 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='5371ad922cb4ff571a57c8e5dd14485ebf5b3994cd71e6ea09088312de3bed71';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.1%2B8/OpenJDK25U-jre_aarch64_linux_hotspot_25.0.1_8.tar.gz';          ;;        ppc64le)          ESUM='c812bf806d7ffcd290c6bd814324aa81f0688e2d682fd0b87e2c7c76251a4f2c';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.1%2B8/OpenJDK25U-jre_ppc64le_linux_hotspot_25.0.1_8.tar.gz';          ;;        s390x)          ESUM='c58764b69cb70e7b532f50e8a20e74aa5cb65e85c3e500225e0b64719a6021a0';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.1%2B8/OpenJDK25U-jre_s390x_linux_hotspot_25.0.1_8.tar.gz';          ;;        x86_64)          ESUM='126c7f59b91df97b2e930b0a456422ce29af7f2385117e1c04297eba962b0b1c';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.1%2B8/OpenJDK25U-jre_x64_linux_hotspot_25.0.1_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz; # buildkit
# Mon, 10 Nov 2025 21:57:55 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Mon, 10 Nov 2025 21:57:55 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Mon, 10 Nov 2025 21:57:55 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
```

-	Layers:
	-	`sha256:7f1c5bcca4741d297e22f1dc3025949ada86e7918c015239fbbf81971759082f`  
		Last Modified: Mon, 10 Nov 2025 12:11:54 GMT  
		Size: 33.4 MB (33403080 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:753a4bd28d57ae0089cf8c05a2fbb3b40711d6fae82766de9b160ebe59e240fb`  
		Last Modified: Mon, 10 Nov 2025 21:52:19 GMT  
		Size: 60.9 MB (60935183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba27a1f1ade37714519f15d898ddba5462894b850096416ac6a0f0ca37b2e3ba`  
		Last Modified: Mon, 10 Nov 2025 21:58:45 GMT  
		Size: 60.2 MB (60215183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34dfe03a0f755821dd6fd0512085bb3a246e56e25b8a04a921561422ae3c0b4d`  
		Last Modified: Mon, 10 Nov 2025 21:58:38 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21dca3e7b9aff1565767ae85b9da151a412ad5405f0d5978276b69e71f6639cc`  
		Last Modified: Mon, 10 Nov 2025 21:58:38 GMT  
		Size: 2.3 KB (2292 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:25-jre-ubi10-minimal` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:8fc4bfb4bea2f4d907e67c26a6b8ea2e108ba81cf959dc03ebea4e6b42e2bba9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5608514 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d06874a81746896d2be35bc8f42d99bfe8d03743de4ce077ea55c9655b8a98c6`

```dockerfile
```

-	Layers:
	-	`sha256:91ae7e2bc980e68da6a8c29f6d6cf02877a053a70e22e5376e345332853f800f`  
		Last Modified: Mon, 10 Nov 2025 22:16:16 GMT  
		Size: 5.6 MB (5588184 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7c2d151f658adc09ae99d46410fb2c8cdca3b5b4f499c243722b5e842ad35504`  
		Last Modified: Mon, 10 Nov 2025 22:16:17 GMT  
		Size: 20.3 KB (20330 bytes)  
		MIME: application/vnd.in-toto+json
