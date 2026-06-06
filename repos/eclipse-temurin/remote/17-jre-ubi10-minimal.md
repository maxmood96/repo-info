## `eclipse-temurin:17-jre-ubi10-minimal`

```console
$ docker pull eclipse-temurin@sha256:9907bc13437641daf2d1d9f85ea98b15c4bbe929cd38f3dc01e6a59d4599cc3c
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

### `eclipse-temurin:17-jre-ubi10-minimal` - linux; amd64

```console
$ docker pull eclipse-temurin@sha256:9b6589e191c5390b0ba0caa706617f13ed25e7bbacb6fa10f84e68950ce2bfe5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **120.2 MB (120181300 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:66e65959d86336bd1bcc975862c40726a397a5100f83fb9aa1be4dac46cf169f`
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
ENV JAVA_VERSION=jdk-17.0.19+10
# Fri, 05 Jun 2026 22:43:03 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='aae834297a87736869745be7c1fca3207ea9167c5824f41c88b0ebb2e3ccb9b1';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.19%2B10/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.19_10.tar.gz';          ;;        ppc64le)          ESUM='1b028a08d96054ef29a3b6c424537d9644e0ec5fb5742a64d967dd56d5571b6b';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.19%2B10/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.19_10.tar.gz';          ;;        s390x)          ESUM='674547d46dad6909fdcdafe5a691c131b048a8d226ccd7d0a4e96f2b208d772a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.19%2B10/OpenJDK17U-jre_s390x_linux_hotspot_17.0.19_10.tar.gz';          ;;        x86_64)          ESUM='adb5a2364baa51de1ef91bb9911f5a61d24b045fe1d6647cb8050272a3a8ee75';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.19%2B10/OpenJDK17U-jre_x64_linux_hotspot_17.0.19_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz; # buildkit
# Fri, 05 Jun 2026 22:43:03 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Fri, 05 Jun 2026 22:43:03 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Fri, 05 Jun 2026 22:43:03 GMT
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
	-	`sha256:90eb291bb1e068f87151c8eddde7af6d3a8347ce527854df215a0e0bb73ee155`  
		Last Modified: Fri, 05 Jun 2026 22:43:16 GMT  
		Size: 47.6 MB (47563556 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9395ab70427f98b81297fb4c0226aef8c3c53da5b39c787c7f329f9d1ab16507`  
		Last Modified: Fri, 05 Jun 2026 22:43:14 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efa4405931699ae50f562f4aef5fd25c5650fa9f0b1786ce2b29802e51ffcdee`  
		Last Modified: Fri, 05 Jun 2026 22:43:14 GMT  
		Size: 2.3 KB (2290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:17-jre-ubi10-minimal` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:69ba3502a4e4fc5239c0717be04948febc861b449ee2a4491c897923fe48b3d9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3728250 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:62fcb2fc4c994d7e5f352c50f7489aec8aa5a9ce366284d231aaa1b0a229a7d5`

```dockerfile
```

-	Layers:
	-	`sha256:50eaa3c86f93d660e0a971bf1f268d04f72834eb338d947db1d382aba05b6db8`  
		Last Modified: Fri, 05 Jun 2026 22:43:14 GMT  
		Size: 3.7 MB (3707872 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:78624a66f5511b3cf65b1228b3d10b67018c4904da126ad6618549fedf4943d0`  
		Last Modified: Fri, 05 Jun 2026 22:43:14 GMT  
		Size: 20.4 KB (20378 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-temurin:17-jre-ubi10-minimal` - linux; arm64 variant v8

```console
$ docker pull eclipse-temurin@sha256:56c64e344846adea456c12a067f3bf6d3e5db4f22043893198e256dadcbd1e41
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **117.8 MB (117778253 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a407dada7129259e6a008268e58cf593ad97397b6232ed8bce0b04bfee211dd`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`

```dockerfile
# Thu, 04 Jun 2026 05:32:13 GMT
LABEL maintainer="Red Hat, Inc."
# Thu, 04 Jun 2026 05:32:13 GMT
LABEL vendor="Red Hat, Inc."
# Thu, 04 Jun 2026 05:32:13 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Thu, 04 Jun 2026 05:32:13 GMT
LABEL com.redhat.component="ubi10-minimal-container"       name="ubi10/ubi-minimal"       version="10.2"       cpe="cpe:/o:redhat:enterprise_linux:10.2"       distribution-scope="public"
# Thu, 04 Jun 2026 05:32:13 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Thu, 04 Jun 2026 05:32:13 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 10."
# Thu, 04 Jun 2026 05:32:13 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 04 Jun 2026 05:32:13 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 04 Jun 2026 05:32:13 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 10 Minimal"
# Thu, 04 Jun 2026 05:32:13 GMT
LABEL io.openshift.expose-services=""
# Thu, 04 Jun 2026 05:32:13 GMT
LABEL io.openshift.tags="minimal rhel10"
# Thu, 04 Jun 2026 05:32:13 GMT
ENV container oci
# Thu, 04 Jun 2026 05:32:14 GMT
COPY dir:742cf4548328149a0d3b299bb0ecd0a71c615bfaf88aa6d4360ecf931aab8785 in /      
# Thu, 04 Jun 2026 05:32:14 GMT
COPY file:5de33b5fc08b00635bccf9134a18978dba13e2250aa51838f9969515a3957847 in /etc/yum.repos.d/.      
# Thu, 04 Jun 2026 05:32:14 GMT
CMD ["/bin/bash"]
# Thu, 04 Jun 2026 05:32:14 GMT
COPY file:595171150af68abc798ea385f7988d74b566aa8e84babff137f00b08b2164683 in /usr/share/buildinfo/content-sets.json      
# Thu, 04 Jun 2026 05:32:14 GMT
COPY file:595171150af68abc798ea385f7988d74b566aa8e84babff137f00b08b2164683 in /root/buildinfo/content_manifests/content-sets.json      
# Thu, 04 Jun 2026 05:32:14 GMT
COPY file:857742e0cb2c063297a5d6df57ad39367bc23ea5335b6bce896696d17d2eb019 in /usr/share/buildinfo/labels.json      
# Thu, 04 Jun 2026 05:32:14 GMT
COPY file:857742e0cb2c063297a5d6df57ad39367bc23ea5335b6bce896696d17d2eb019 in /root/buildinfo/labels.json      
# Thu, 04 Jun 2026 05:32:14 GMT
LABEL "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="21e748607cdf3bfe567bea40c2e0c654a3c7766c" "org.opencontainers.image.revision"="21e748607cdf3bfe567bea40c2e0c654a3c7766c" "build-date"="2026-06-04T05:31:57Z" "org.opencontainers.image.created"="2026-06-04T05:31:57Z" "release"="1780550715"org.opencontainers.image.revision=21e748607cdf3bfe567bea40c2e0c654a3c7766c,org.opencontainers.image.created=2026-06-04T05:31:57Z
# Fri, 05 Jun 2026 22:43:30 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 05 Jun 2026 22:43:30 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 05 Jun 2026 22:43:30 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 05 Jun 2026 22:43:30 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en         gnupg2     ;     microdnf clean all # buildkit
# Fri, 05 Jun 2026 22:43:30 GMT
ENV JAVA_VERSION=jdk-17.0.19+10
# Fri, 05 Jun 2026 22:43:34 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='aae834297a87736869745be7c1fca3207ea9167c5824f41c88b0ebb2e3ccb9b1';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.19%2B10/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.19_10.tar.gz';          ;;        ppc64le)          ESUM='1b028a08d96054ef29a3b6c424537d9644e0ec5fb5742a64d967dd56d5571b6b';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.19%2B10/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.19_10.tar.gz';          ;;        s390x)          ESUM='674547d46dad6909fdcdafe5a691c131b048a8d226ccd7d0a4e96f2b208d772a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.19%2B10/OpenJDK17U-jre_s390x_linux_hotspot_17.0.19_10.tar.gz';          ;;        x86_64)          ESUM='adb5a2364baa51de1ef91bb9911f5a61d24b045fe1d6647cb8050272a3a8ee75';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.19%2B10/OpenJDK17U-jre_x64_linux_hotspot_17.0.19_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz; # buildkit
# Fri, 05 Jun 2026 22:43:34 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Fri, 05 Jun 2026 22:43:34 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Fri, 05 Jun 2026 22:43:34 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
```

-	Layers:
	-	`sha256:ebf3c43a43d516c400d687e8a210bad7522ec8a8a6c34ae1d72a70004f06bc71`  
		Last Modified: Thu, 04 Jun 2026 06:53:34 GMT  
		Size: 33.0 MB (33039715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7db728573d68b378753f426bcee6070cc0a8a21f8800984d0ca963625ef9dae`  
		Last Modified: Fri, 05 Jun 2026 22:43:49 GMT  
		Size: 37.7 MB (37686409 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b058bb579b4f62cee1358867cca4daea47d6f193bb0aea2d38141cb59e760a25`  
		Last Modified: Fri, 05 Jun 2026 22:43:49 GMT  
		Size: 47.0 MB (47049711 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aff7504680c2938656ef626d0faaee8bef3308b7737abae4e7906c920bc1f490`  
		Last Modified: Fri, 05 Jun 2026 22:43:47 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6558bf5365ae5c00416a93025e26e0b0af14a9ffea031b296551471707b48c2`  
		Last Modified: Fri, 05 Jun 2026 22:43:47 GMT  
		Size: 2.3 KB (2290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:17-jre-ubi10-minimal` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:1c9a393b88cb81eaff34747cea85fc753bfa8db158dc58d2c5cf14d147288c5f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3727768 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6af0e80cd5569e341948db6ed24b9b036b118fe03427bf70cbd03f2a60847501`

```dockerfile
```

-	Layers:
	-	`sha256:8ecadbb1fd7192b9f655ac7fe4ab2f5c0440a08e3c642509cc19b1d671c00913`  
		Last Modified: Fri, 05 Jun 2026 22:43:47 GMT  
		Size: 3.7 MB (3707286 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d977e2e1a3d27012680a967deda6fe91e2d741f03c593faa74b1ab55bff47704`  
		Last Modified: Fri, 05 Jun 2026 22:43:47 GMT  
		Size: 20.5 KB (20482 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-temurin:17-jre-ubi10-minimal` - linux; ppc64le

```console
$ docker pull eclipse-temurin@sha256:f70e1ca39751e20c9cf0b0ed6fcf8614881f54eb729dcedf8eb53b2b8ebe6f64
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **126.0 MB (126033335 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6cf2a991fbfe6ea48c5f8ce43bb9898af9f57410911f59ea16331bba73ce95fe`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`

```dockerfile
# Thu, 04 Jun 2026 05:32:40 GMT
LABEL maintainer="Red Hat, Inc."
# Thu, 04 Jun 2026 05:32:40 GMT
LABEL vendor="Red Hat, Inc."
# Thu, 04 Jun 2026 05:32:40 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Thu, 04 Jun 2026 05:32:40 GMT
LABEL com.redhat.component="ubi10-minimal-container"       name="ubi10/ubi-minimal"       version="10.2"       cpe="cpe:/o:redhat:enterprise_linux:10.2"       distribution-scope="public"
# Thu, 04 Jun 2026 05:32:40 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Thu, 04 Jun 2026 05:32:40 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 10."
# Thu, 04 Jun 2026 05:32:40 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 04 Jun 2026 05:32:40 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 04 Jun 2026 05:32:40 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 10 Minimal"
# Thu, 04 Jun 2026 05:32:40 GMT
LABEL io.openshift.expose-services=""
# Thu, 04 Jun 2026 05:32:40 GMT
LABEL io.openshift.tags="minimal rhel10"
# Thu, 04 Jun 2026 05:32:40 GMT
ENV container oci
# Thu, 04 Jun 2026 05:32:41 GMT
COPY dir:39feacb07d6a39793cfb5ecb8ce42cbba48072d5e83b48decf5ed170f1dae59f in /      
# Thu, 04 Jun 2026 05:32:41 GMT
COPY file:5de33b5fc08b00635bccf9134a18978dba13e2250aa51838f9969515a3957847 in /etc/yum.repos.d/.      
# Thu, 04 Jun 2026 05:32:41 GMT
CMD ["/bin/bash"]
# Thu, 04 Jun 2026 05:32:41 GMT
COPY file:595171150af68abc798ea385f7988d74b566aa8e84babff137f00b08b2164683 in /usr/share/buildinfo/content-sets.json      
# Thu, 04 Jun 2026 05:32:41 GMT
COPY file:595171150af68abc798ea385f7988d74b566aa8e84babff137f00b08b2164683 in /root/buildinfo/content_manifests/content-sets.json      
# Thu, 04 Jun 2026 05:32:41 GMT
COPY file:5a88f34d22fc0aaa3bcdde8758372a2e49b97b3dec16ffb3a17985ea3396531b in /usr/share/buildinfo/labels.json      
# Thu, 04 Jun 2026 05:32:41 GMT
COPY file:5a88f34d22fc0aaa3bcdde8758372a2e49b97b3dec16ffb3a17985ea3396531b in /root/buildinfo/labels.json      
# Thu, 04 Jun 2026 05:32:42 GMT
LABEL "architecture"="ppc64le" "vcs-type"="git" "vcs-ref"="21e748607cdf3bfe567bea40c2e0c654a3c7766c" "org.opencontainers.image.revision"="21e748607cdf3bfe567bea40c2e0c654a3c7766c" "build-date"="2026-06-04T05:32:29Z" "org.opencontainers.image.created"="2026-06-04T05:32:29Z" "release"="1780550715"org.opencontainers.image.revision=21e748607cdf3bfe567bea40c2e0c654a3c7766c,org.opencontainers.image.created=2026-06-04T05:32:29Z
# Fri, 05 Jun 2026 23:18:00 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 05 Jun 2026 23:18:00 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 05 Jun 2026 23:18:00 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 05 Jun 2026 23:18:00 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en         gnupg2     ;     microdnf clean all # buildkit
# Fri, 05 Jun 2026 23:18:00 GMT
ENV JAVA_VERSION=jdk-17.0.19+10
# Fri, 05 Jun 2026 23:19:53 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='aae834297a87736869745be7c1fca3207ea9167c5824f41c88b0ebb2e3ccb9b1';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.19%2B10/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.19_10.tar.gz';          ;;        ppc64le)          ESUM='1b028a08d96054ef29a3b6c424537d9644e0ec5fb5742a64d967dd56d5571b6b';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.19%2B10/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.19_10.tar.gz';          ;;        s390x)          ESUM='674547d46dad6909fdcdafe5a691c131b048a8d226ccd7d0a4e96f2b208d772a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.19%2B10/OpenJDK17U-jre_s390x_linux_hotspot_17.0.19_10.tar.gz';          ;;        x86_64)          ESUM='adb5a2364baa51de1ef91bb9911f5a61d24b045fe1d6647cb8050272a3a8ee75';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.19%2B10/OpenJDK17U-jre_x64_linux_hotspot_17.0.19_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz; # buildkit
# Fri, 05 Jun 2026 23:19:54 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Fri, 05 Jun 2026 23:19:55 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Fri, 05 Jun 2026 23:19:55 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
```

-	Layers:
	-	`sha256:0548d638ade0e4394f010f8571f1879c4b09c3ac5cba2ccff7dfa8b2c88574b5`  
		Last Modified: Thu, 04 Jun 2026 06:53:50 GMT  
		Size: 39.0 MB (39010615 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:386aabc3a75f4ee1e9a3070c6e92d370f6789fef7ef5aa8020778d4f20d9234b`  
		Last Modified: Fri, 05 Jun 2026 23:18:37 GMT  
		Size: 39.5 MB (39520609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8d1c9b9ed444c8e67c285d73e7f48346ba06fad2d638a4f6db0c3c9bedce838`  
		Last Modified: Fri, 05 Jun 2026 23:20:21 GMT  
		Size: 47.5 MB (47499693 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3f4893e82003403e82e072ee474c049faa9c390918e58ee465d6b15b13bead3`  
		Last Modified: Fri, 05 Jun 2026 23:20:19 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:322e1a201c2dd30e61194f887e8b679a00089a02f7a03d8b3a57878f760f55bd`  
		Last Modified: Fri, 05 Jun 2026 23:20:19 GMT  
		Size: 2.3 KB (2290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:17-jre-ubi10-minimal` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:3c01d27423378951bb8735175662c8b39d7b2f8d4d93e33512d921b453271cff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3717025 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e261e2ec3b5fe46a75ccce03c1d017c899b5a50e659f4131d9db3fec02f0c1e3`

```dockerfile
```

-	Layers:
	-	`sha256:83252669f455f00b5c9ccf6d7b455f7393a9a51f372ea1f07f28e1799d180130`  
		Last Modified: Fri, 05 Jun 2026 23:20:19 GMT  
		Size: 3.7 MB (3696617 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7e334f4e8fe4bf052f6f1359928264720c8b650c4bfa72c37040f40dbee7f75a`  
		Last Modified: Fri, 05 Jun 2026 23:20:19 GMT  
		Size: 20.4 KB (20408 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-temurin:17-jre-ubi10-minimal` - linux; s390x

```console
$ docker pull eclipse-temurin@sha256:c962484621beac28bd07e099635230714ea3473df50d0e2d7240ae979e863c4d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **117.4 MB (117399344 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b273610321cbb2baef1b0babd72ccddec6074e6b19e68d43caf8231d22b83e30`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`

```dockerfile
# Thu, 04 Jun 2026 05:41:17 GMT
LABEL maintainer="Red Hat, Inc."
# Thu, 04 Jun 2026 05:41:17 GMT
LABEL vendor="Red Hat, Inc."
# Thu, 04 Jun 2026 05:41:17 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Thu, 04 Jun 2026 05:41:17 GMT
LABEL com.redhat.component="ubi10-minimal-container"       name="ubi10/ubi-minimal"       version="10.2"       cpe="cpe:/o:redhat:enterprise_linux:10.2"       distribution-scope="public"
# Thu, 04 Jun 2026 05:41:17 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Thu, 04 Jun 2026 05:41:17 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 10."
# Thu, 04 Jun 2026 05:41:17 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 04 Jun 2026 05:41:17 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 04 Jun 2026 05:41:17 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 10 Minimal"
# Thu, 04 Jun 2026 05:41:17 GMT
LABEL io.openshift.expose-services=""
# Thu, 04 Jun 2026 05:41:17 GMT
LABEL io.openshift.tags="minimal rhel10"
# Thu, 04 Jun 2026 05:41:17 GMT
ENV container oci
# Thu, 04 Jun 2026 05:41:17 GMT
COPY dir:9a20d45e3984f98caa7a89f40c9769c8ed59b525d31291027bc9643813420c60 in /      
# Thu, 04 Jun 2026 05:41:18 GMT
COPY file:5de33b5fc08b00635bccf9134a18978dba13e2250aa51838f9969515a3957847 in /etc/yum.repos.d/.      
# Thu, 04 Jun 2026 05:41:18 GMT
CMD ["/bin/bash"]
# Thu, 04 Jun 2026 05:41:18 GMT
COPY file:595171150af68abc798ea385f7988d74b566aa8e84babff137f00b08b2164683 in /usr/share/buildinfo/content-sets.json      
# Thu, 04 Jun 2026 05:41:18 GMT
COPY file:595171150af68abc798ea385f7988d74b566aa8e84babff137f00b08b2164683 in /root/buildinfo/content_manifests/content-sets.json      
# Thu, 04 Jun 2026 05:41:18 GMT
COPY file:145c21488b7dd243862f15c5b9a62cfc5fc22a0ba135ab81b80fd5dfaa1db619 in /usr/share/buildinfo/labels.json      
# Thu, 04 Jun 2026 05:41:18 GMT
COPY file:145c21488b7dd243862f15c5b9a62cfc5fc22a0ba135ab81b80fd5dfaa1db619 in /root/buildinfo/labels.json      
# Thu, 04 Jun 2026 05:41:18 GMT
LABEL "architecture"="s390x" "vcs-type"="git" "vcs-ref"="21e748607cdf3bfe567bea40c2e0c654a3c7766c" "org.opencontainers.image.revision"="21e748607cdf3bfe567bea40c2e0c654a3c7766c" "build-date"="2026-06-04T05:40:37Z" "org.opencontainers.image.created"="2026-06-04T05:40:37Z" "release"="1780550715"org.opencontainers.image.revision=21e748607cdf3bfe567bea40c2e0c654a3c7766c,org.opencontainers.image.created=2026-06-04T05:40:37Z
# Fri, 05 Jun 2026 22:54:39 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 05 Jun 2026 22:54:39 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 05 Jun 2026 22:54:39 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 05 Jun 2026 22:54:39 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en         gnupg2     ;     microdnf clean all # buildkit
# Fri, 05 Jun 2026 22:54:39 GMT
ENV JAVA_VERSION=jdk-17.0.19+10
# Fri, 05 Jun 2026 22:55:34 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='aae834297a87736869745be7c1fca3207ea9167c5824f41c88b0ebb2e3ccb9b1';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.19%2B10/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.19_10.tar.gz';          ;;        ppc64le)          ESUM='1b028a08d96054ef29a3b6c424537d9644e0ec5fb5742a64d967dd56d5571b6b';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.19%2B10/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.19_10.tar.gz';          ;;        s390x)          ESUM='674547d46dad6909fdcdafe5a691c131b048a8d226ccd7d0a4e96f2b208d772a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.19%2B10/OpenJDK17U-jre_s390x_linux_hotspot_17.0.19_10.tar.gz';          ;;        x86_64)          ESUM='adb5a2364baa51de1ef91bb9911f5a61d24b045fe1d6647cb8050272a3a8ee75';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.19%2B10/OpenJDK17U-jre_x64_linux_hotspot_17.0.19_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz; # buildkit
# Fri, 05 Jun 2026 22:55:34 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Fri, 05 Jun 2026 22:55:34 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Fri, 05 Jun 2026 22:55:34 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
```

-	Layers:
	-	`sha256:508908cfb0e80bf20878a35fc50b1b96d43933820f4d9e8454cbdb960c52bdb5`  
		Last Modified: Thu, 04 Jun 2026 06:53:41 GMT  
		Size: 34.7 MB (34726577 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6b711f2b1010b3a0bdac6f6c9c90783837f411ad3aff4e3fda9b12ef7924d85`  
		Last Modified: Fri, 05 Jun 2026 22:55:03 GMT  
		Size: 38.1 MB (38139315 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e34c784f3426edbd4797dc64faaa7493357c82d38e0e60af38a68b0ad9b0342f`  
		Last Modified: Fri, 05 Jun 2026 22:55:57 GMT  
		Size: 44.5 MB (44531036 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97342eb52076c99806098b2c9adaf6fb9e47b9fd28384f1e0ee50733f5e319df`  
		Last Modified: Fri, 05 Jun 2026 22:55:56 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e199a6214f14a62c872ab331f18a54e0d70de5f4232f02ec4e930ddcc04f1a49`  
		Last Modified: Fri, 05 Jun 2026 22:55:56 GMT  
		Size: 2.3 KB (2290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:17-jre-ubi10-minimal` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:38fc87396c79c537de305a393cdb1f1fd0ae661dfa7ebf996b230fe83f303711
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3718240 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bbad3c8ac418d74d0067edad1bad92f54e60e9470dd23d5224da06d406a30fbd`

```dockerfile
```

-	Layers:
	-	`sha256:40e7ae72af63cb63958d668e8d67de19beece744da39a5052d42733764f6f9d9`  
		Last Modified: Fri, 05 Jun 2026 22:55:56 GMT  
		Size: 3.7 MB (3697862 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4079a6e3703b9ff96a125e074cc004cb16396c22f8d314e90c5127fdd3fc31b1`  
		Last Modified: Fri, 05 Jun 2026 22:55:56 GMT  
		Size: 20.4 KB (20378 bytes)  
		MIME: application/vnd.in-toto+json
