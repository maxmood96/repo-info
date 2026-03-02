## `eclipse-temurin:8u482-b08-jre-ubi10-minimal`

```console
$ docker pull eclipse-temurin@sha256:cea684a7a5585a9b5efc7b0ef7215c7a8c5e4f51f59523b17a7d5a169823e10f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `eclipse-temurin:8u482-b08-jre-ubi10-minimal` - linux; amd64

```console
$ docker pull eclipse-temurin@sha256:fae86d6a4d147ce358014049ac3b5f3ef7e30aa4c4490bd587ea88474cce3310
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.4 MB (114367235 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:947bd3746fb84015bb1ec018bbef4088683feedc0e90b458c75f85c0dba9be2a`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`

```dockerfile
# Mon, 02 Mar 2026 08:55:54 GMT
LABEL maintainer="Red Hat, Inc."
# Mon, 02 Mar 2026 08:55:54 GMT
LABEL vendor="Red Hat, Inc."
# Mon, 02 Mar 2026 08:55:54 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Mon, 02 Mar 2026 08:55:54 GMT
LABEL com.redhat.component="ubi10-minimal-container"       name="ubi10/ubi-minimal"       version="10.1"       cpe="cpe:/o:redhat:enterprise_linux:10.1"       distribution-scope="public"
# Mon, 02 Mar 2026 08:55:55 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Mon, 02 Mar 2026 08:55:55 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 10."
# Mon, 02 Mar 2026 08:55:55 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 02 Mar 2026 08:55:55 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 02 Mar 2026 08:55:55 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 10 Minimal"
# Mon, 02 Mar 2026 08:55:55 GMT
LABEL io.openshift.expose-services=""
# Mon, 02 Mar 2026 08:55:55 GMT
LABEL io.openshift.tags="minimal rhel10"
# Mon, 02 Mar 2026 08:55:55 GMT
ENV container oci
# Mon, 02 Mar 2026 08:55:55 GMT
COPY dir:bc9a8a44e634605c4ff89328666c26f0c256afabea6c375c1017a88a80500ea2 in /      
# Mon, 02 Mar 2026 08:55:55 GMT
COPY file:5de33b5fc08b00635bccf9134a18978dba13e2250aa51838f9969515a3957847 in /etc/yum.repos.d/.      
# Mon, 02 Mar 2026 08:55:55 GMT
CMD ["/bin/bash"]
# Mon, 02 Mar 2026 08:55:55 GMT
COPY file:595171150af68abc798ea385f7988d74b566aa8e84babff137f00b08b2164683 in /usr/share/buildinfo/content-sets.json      
# Mon, 02 Mar 2026 08:55:55 GMT
COPY file:595171150af68abc798ea385f7988d74b566aa8e84babff137f00b08b2164683 in /root/buildinfo/content_manifests/content-sets.json      
# Mon, 02 Mar 2026 08:55:56 GMT
COPY file:c0327936eac36593f0ab8d7da594e1a816cbe84da917c4d0a34bfcc7a914e024 in /usr/share/buildinfo/labels.json      
# Mon, 02 Mar 2026 08:55:56 GMT
COPY file:c0327936eac36593f0ab8d7da594e1a816cbe84da917c4d0a34bfcc7a914e024 in /root/buildinfo/labels.json      
# Mon, 02 Mar 2026 08:55:56 GMT
LABEL "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="22680d9fff6e4cead236be943e791fde5247c69a" "org.opencontainers.image.revision"="22680d9fff6e4cead236be943e791fde5247c69a" "build-date"="2026-03-02T08:55:38Z" "org.opencontainers.image.created"="2026-03-02T08:55:38Z" "release"="1772441549"org.opencontainers.image.revision=22680d9fff6e4cead236be943e791fde5247c69a,org.opencontainers.image.created=2026-03-02T08:55:38Z
# Mon, 02 Mar 2026 22:05:12 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 02 Mar 2026 22:05:12 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 02 Mar 2026 22:05:12 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 02 Mar 2026 22:05:12 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en         gnupg2     ;     microdnf clean all # buildkit
# Mon, 02 Mar 2026 22:05:12 GMT
ENV JAVA_VERSION=jdk8u482-b08
# Mon, 02 Mar 2026 22:05:15 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='46496dfa7e58784adf96a3a2bd1ac8be9fda2d8749a9c52bf74fb582aa1449e2';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u482-b08/OpenJDK8U-jre_aarch64_linux_hotspot_8u482b08.tar.gz';          ;;        ppc64le)          ESUM='b563c5c90dcff0c1cf5a1bdc3110e560c979254a17e696902e922631264cf342';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u482-b08/OpenJDK8U-jre_ppc64le_linux_hotspot_8u482b08.tar.gz';          ;;        x86_64)          ESUM='01672ca52509f4cb1ffa8aed905808fed7b984f3e279cb13d90a6e865ff6199f';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u482-b08/OpenJDK8U-jre_x64_linux_hotspot_8u482b08.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz; # buildkit
# Mon, 02 Mar 2026 22:05:15 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java -version"; java -version;     echo "Complete." # buildkit
# Mon, 02 Mar 2026 22:05:15 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Mon, 02 Mar 2026 22:05:15 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
```

-	Layers:
	-	`sha256:4377b1aab54b81e1e3b39331172fb1424f433cdfe28e8bf6f9cd313a971d0d61`  
		Last Modified: Mon, 02 Mar 2026 10:45:10 GMT  
		Size: 34.6 MB (34610905 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73ccd897668e75fe4ef478ad40e40cf6065c2c61c6a932e4a705ef55a6a0f3e1`  
		Last Modified: Mon, 02 Mar 2026 22:05:29 GMT  
		Size: 37.4 MB (37429200 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cea4116788496a94beaad28927f1bb6df2fc1ae634e3a14f44c5fe0243bcc116`  
		Last Modified: Mon, 02 Mar 2026 22:05:30 GMT  
		Size: 42.3 MB (42324711 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8baa58f24592a8b0e5594b3134d22c51944b32da2a979080290401e1d72dc041`  
		Last Modified: Mon, 02 Mar 2026 22:05:27 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a681e52a27e5fbdaad447a79e166c3b7698935e9089185e1e808211653710685`  
		Last Modified: Mon, 02 Mar 2026 22:05:28 GMT  
		Size: 2.3 KB (2291 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:8u482-b08-jre-ubi10-minimal` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:65a047199b41f4a331a4e56c5ba02cb26b4353620513fc7de862c6673e8b6902
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3754279 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:664a92bc703c9ff3d8b8ebeafa31d7333d29bf7e020e1b4387b85181bab4df41`

```dockerfile
```

-	Layers:
	-	`sha256:60aa10277f864a79af2578c8cb9196c107a703be36a18f4ebaf20edb389f2d46`  
		Last Modified: Mon, 02 Mar 2026 22:05:27 GMT  
		Size: 3.7 MB (3734768 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8a610a6545cfa0cd49c5d3650e471a360d2537d147ad3e459a8d939321223f67`  
		Last Modified: Mon, 02 Mar 2026 22:05:27 GMT  
		Size: 19.5 KB (19511 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-temurin:8u482-b08-jre-ubi10-minimal` - linux; arm64 variant v8

```console
$ docker pull eclipse-temurin@sha256:47bc48b3781fe8e8aafabf9bc3d99f719d37f428699bd3f87e4924f94431cd36
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **111.3 MB (111348456 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3aa12907e3e268383a26b59c534595d4415ac56ca52003098749a6e8a848c5ce`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`

```dockerfile
# Mon, 02 Mar 2026 08:58:05 GMT
LABEL maintainer="Red Hat, Inc."
# Mon, 02 Mar 2026 08:58:05 GMT
LABEL vendor="Red Hat, Inc."
# Mon, 02 Mar 2026 08:58:05 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Mon, 02 Mar 2026 08:58:05 GMT
LABEL com.redhat.component="ubi10-minimal-container"       name="ubi10/ubi-minimal"       version="10.1"       cpe="cpe:/o:redhat:enterprise_linux:10.1"       distribution-scope="public"
# Mon, 02 Mar 2026 08:58:05 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Mon, 02 Mar 2026 08:58:05 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 10."
# Mon, 02 Mar 2026 08:58:05 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 02 Mar 2026 08:58:05 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 02 Mar 2026 08:58:05 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 10 Minimal"
# Mon, 02 Mar 2026 08:58:05 GMT
LABEL io.openshift.expose-services=""
# Mon, 02 Mar 2026 08:58:05 GMT
LABEL io.openshift.tags="minimal rhel10"
# Mon, 02 Mar 2026 08:58:05 GMT
ENV container oci
# Mon, 02 Mar 2026 08:58:06 GMT
COPY dir:c8a0e6b85769dc5b1153f2d95c0dab0c21c76be6878d56a453a175f235aec4f0 in /      
# Mon, 02 Mar 2026 08:58:06 GMT
COPY file:5de33b5fc08b00635bccf9134a18978dba13e2250aa51838f9969515a3957847 in /etc/yum.repos.d/.      
# Mon, 02 Mar 2026 08:58:06 GMT
CMD ["/bin/bash"]
# Mon, 02 Mar 2026 08:58:07 GMT
COPY file:595171150af68abc798ea385f7988d74b566aa8e84babff137f00b08b2164683 in /usr/share/buildinfo/content-sets.json      
# Mon, 02 Mar 2026 08:58:07 GMT
COPY file:595171150af68abc798ea385f7988d74b566aa8e84babff137f00b08b2164683 in /root/buildinfo/content_manifests/content-sets.json      
# Mon, 02 Mar 2026 08:58:07 GMT
COPY file:09f44631adf2e487fe312f2a1e81a1022d21dd1ab82974e6dcdb1c9761ad2ce6 in /usr/share/buildinfo/labels.json      
# Mon, 02 Mar 2026 08:58:07 GMT
COPY file:09f44631adf2e487fe312f2a1e81a1022d21dd1ab82974e6dcdb1c9761ad2ce6 in /root/buildinfo/labels.json      
# Mon, 02 Mar 2026 08:58:07 GMT
LABEL "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="22680d9fff6e4cead236be943e791fde5247c69a" "org.opencontainers.image.revision"="22680d9fff6e4cead236be943e791fde5247c69a" "build-date"="2026-03-02T08:57:50Z" "org.opencontainers.image.created"="2026-03-02T08:57:50Z" "release"="1772441549"org.opencontainers.image.revision=22680d9fff6e4cead236be943e791fde5247c69a,org.opencontainers.image.created=2026-03-02T08:57:50Z
# Mon, 02 Mar 2026 22:08:14 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 02 Mar 2026 22:08:14 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 02 Mar 2026 22:08:14 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 02 Mar 2026 22:08:14 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en         gnupg2     ;     microdnf clean all # buildkit
# Mon, 02 Mar 2026 22:08:14 GMT
ENV JAVA_VERSION=jdk8u482-b08
# Mon, 02 Mar 2026 22:08:18 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='46496dfa7e58784adf96a3a2bd1ac8be9fda2d8749a9c52bf74fb582aa1449e2';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u482-b08/OpenJDK8U-jre_aarch64_linux_hotspot_8u482b08.tar.gz';          ;;        ppc64le)          ESUM='b563c5c90dcff0c1cf5a1bdc3110e560c979254a17e696902e922631264cf342';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u482-b08/OpenJDK8U-jre_ppc64le_linux_hotspot_8u482b08.tar.gz';          ;;        x86_64)          ESUM='01672ca52509f4cb1ffa8aed905808fed7b984f3e279cb13d90a6e865ff6199f';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u482-b08/OpenJDK8U-jre_x64_linux_hotspot_8u482b08.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz; # buildkit
# Mon, 02 Mar 2026 22:08:18 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java -version"; java -version;     echo "Complete." # buildkit
# Mon, 02 Mar 2026 22:08:18 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Mon, 02 Mar 2026 22:08:18 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
```

-	Layers:
	-	`sha256:ab71f30be3b758ee5a6fbf5d72df781f51e8cf5753ddf02671b2d7e13e4932fb`  
		Last Modified: Mon, 02 Mar 2026 11:28:23 GMT  
		Size: 32.7 MB (32683006 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b3889f3884aa943c26e1c1b3de15da7a5aebe5f569d872cc163230b47be37b7`  
		Last Modified: Mon, 02 Mar 2026 22:08:32 GMT  
		Size: 37.4 MB (37374475 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a63193b3363c2b9089ecd9d1d9f22e79daf9b105a0a26d18bc6e0d913af416b0`  
		Last Modified: Mon, 02 Mar 2026 22:08:32 GMT  
		Size: 41.3 MB (41288560 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66010cd28322a986ed7f52b8272210f35919b887c53db1d970bdba87c33e2d4c`  
		Last Modified: Mon, 02 Mar 2026 22:08:29 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8dc6e6894a41a068a2b499c65a0a26d4ca50e9bcde70d7b9b0fb555def53837d`  
		Last Modified: Mon, 02 Mar 2026 22:08:31 GMT  
		Size: 2.3 KB (2289 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:8u482-b08-jre-ubi10-minimal` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:7529307cb47b7eaf2d0bafdc5c932fdfb2223dfd1744ee3dc1bb488b03820ffa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3754489 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ebb9376f2dcb6be55ed862843eb906fe6dc6509fec697cbc27d711d7139f1e1f`

```dockerfile
```

-	Layers:
	-	`sha256:d5324cc09b4dda2c0ba347d968d9fe6748a86842881ed13cc93970d56543e1b6`  
		Last Modified: Mon, 02 Mar 2026 22:08:30 GMT  
		Size: 3.7 MB (3734874 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c5b0cc88169dc033c3f8c4759afcd47a931a918c84bc74dbdf3df2cb4f5f4dd1`  
		Last Modified: Mon, 02 Mar 2026 22:08:29 GMT  
		Size: 19.6 KB (19615 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-temurin:8u482-b08-jre-ubi10-minimal` - linux; ppc64le

```console
$ docker pull eclipse-temurin@sha256:70b498cb00f50fa51f5f2a4018a59f13a923c5c122e67179c115cb64b4843a73
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **119.6 MB (119638572 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:924fddac4dfbb7f9e71ade4ed4da57b25b8d9e3b2c1f68b524bddc74a9c65fea`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`

```dockerfile
# Mon, 02 Mar 2026 09:04:59 GMT
LABEL maintainer="Red Hat, Inc."
# Mon, 02 Mar 2026 09:04:59 GMT
LABEL vendor="Red Hat, Inc."
# Mon, 02 Mar 2026 09:04:59 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Mon, 02 Mar 2026 09:04:59 GMT
LABEL com.redhat.component="ubi10-minimal-container"       name="ubi10/ubi-minimal"       version="10.1"       cpe="cpe:/o:redhat:enterprise_linux:10.1"       distribution-scope="public"
# Mon, 02 Mar 2026 09:04:59 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Mon, 02 Mar 2026 09:04:59 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 10."
# Mon, 02 Mar 2026 09:04:59 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 02 Mar 2026 09:04:59 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 02 Mar 2026 09:04:59 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 10 Minimal"
# Mon, 02 Mar 2026 09:04:59 GMT
LABEL io.openshift.expose-services=""
# Mon, 02 Mar 2026 09:04:59 GMT
LABEL io.openshift.tags="minimal rhel10"
# Mon, 02 Mar 2026 09:04:59 GMT
ENV container oci
# Mon, 02 Mar 2026 09:05:00 GMT
COPY dir:e20d8c9b5112eae2ec3cf27567703617b532b3d50e37e22798356175a81af012 in /      
# Mon, 02 Mar 2026 09:05:00 GMT
COPY file:5de33b5fc08b00635bccf9134a18978dba13e2250aa51838f9969515a3957847 in /etc/yum.repos.d/.      
# Mon, 02 Mar 2026 09:05:00 GMT
CMD ["/bin/bash"]
# Mon, 02 Mar 2026 09:05:00 GMT
COPY file:595171150af68abc798ea385f7988d74b566aa8e84babff137f00b08b2164683 in /usr/share/buildinfo/content-sets.json      
# Mon, 02 Mar 2026 09:05:00 GMT
COPY file:595171150af68abc798ea385f7988d74b566aa8e84babff137f00b08b2164683 in /root/buildinfo/content_manifests/content-sets.json      
# Mon, 02 Mar 2026 09:05:00 GMT
COPY file:f249adc52ffecf442b4262c353b6483cbd86a0119b4a0d56c2ae3482dda5e6dd in /usr/share/buildinfo/labels.json      
# Mon, 02 Mar 2026 09:05:00 GMT
COPY file:f249adc52ffecf442b4262c353b6483cbd86a0119b4a0d56c2ae3482dda5e6dd in /root/buildinfo/labels.json      
# Mon, 02 Mar 2026 09:05:01 GMT
LABEL "architecture"="ppc64le" "vcs-type"="git" "vcs-ref"="22680d9fff6e4cead236be943e791fde5247c69a" "org.opencontainers.image.revision"="22680d9fff6e4cead236be943e791fde5247c69a" "build-date"="2026-03-02T09:04:48Z" "org.opencontainers.image.created"="2026-03-02T09:04:48Z" "release"="1772441549"org.opencontainers.image.revision=22680d9fff6e4cead236be943e791fde5247c69a,org.opencontainers.image.created=2026-03-02T09:04:48Z
# Mon, 02 Mar 2026 22:11:17 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 02 Mar 2026 22:11:17 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 02 Mar 2026 22:11:17 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 02 Mar 2026 22:11:17 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en         gnupg2     ;     microdnf clean all # buildkit
# Mon, 02 Mar 2026 22:11:17 GMT
ENV JAVA_VERSION=jdk8u482-b08
# Mon, 02 Mar 2026 22:11:24 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='46496dfa7e58784adf96a3a2bd1ac8be9fda2d8749a9c52bf74fb582aa1449e2';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u482-b08/OpenJDK8U-jre_aarch64_linux_hotspot_8u482b08.tar.gz';          ;;        ppc64le)          ESUM='b563c5c90dcff0c1cf5a1bdc3110e560c979254a17e696902e922631264cf342';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u482-b08/OpenJDK8U-jre_ppc64le_linux_hotspot_8u482b08.tar.gz';          ;;        x86_64)          ESUM='01672ca52509f4cb1ffa8aed905808fed7b984f3e279cb13d90a6e865ff6199f';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u482-b08/OpenJDK8U-jre_x64_linux_hotspot_8u482b08.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz; # buildkit
# Mon, 02 Mar 2026 22:11:26 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java -version"; java -version;     echo "Complete." # buildkit
# Mon, 02 Mar 2026 22:11:27 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Mon, 02 Mar 2026 22:11:27 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
```

-	Layers:
	-	`sha256:52175d44fca07e14e1039fd9cb5b5c7a4f5a641951f3018cac642ab2b0d7aa2d`  
		Last Modified: Mon, 02 Mar 2026 12:12:22 GMT  
		Size: 38.7 MB (38730989 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40df108a302998b0b0c1beb639de829388ba26f170d0578e18c4fcfeb7e8204b`  
		Last Modified: Mon, 02 Mar 2026 22:11:53 GMT  
		Size: 39.2 MB (39183318 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f304e99eb88effa9aa6b4ccd61b736f772c7cbf5e16362bacb306a9157f64daa`  
		Last Modified: Mon, 02 Mar 2026 22:11:53 GMT  
		Size: 41.7 MB (41721847 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46677a0e0fc0c45b6cfe387fe338cf1a20821df989391d2ab87d1224fd293f62`  
		Last Modified: Mon, 02 Mar 2026 22:11:51 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf956a5c588b7d2cd50ae91d8f44faf00ba242acfd546d6339c03c89ba5be3a7`  
		Last Modified: Mon, 02 Mar 2026 22:11:52 GMT  
		Size: 2.3 KB (2291 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:8u482-b08-jre-ubi10-minimal` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:d3af9ae91988165e20eab500fc27b7bfec156a65a359bdbc6fa0feadd753774c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3743746 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:62c6bec899f50b56ccead2a265f1e55274c1f8344996d14a31a276f28f495a75`

```dockerfile
```

-	Layers:
	-	`sha256:fd6e5e75a803c463602dea81fcc5e104fb961eb83afd8f1e09222a8574ed918d`  
		Last Modified: Mon, 02 Mar 2026 22:11:51 GMT  
		Size: 3.7 MB (3724205 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b542eca4a232f97eee5ad8c07119a005fd906dfce58699b4199c8b7e3f847285`  
		Last Modified: Mon, 02 Mar 2026 22:11:51 GMT  
		Size: 19.5 KB (19541 bytes)  
		MIME: application/vnd.in-toto+json
