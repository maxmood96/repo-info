## `eclipse-temurin:8-ubi10-minimal`

```console
$ docker pull eclipse-temurin@sha256:b1bdee8c2388837ab689bdf64e2403278f9730658aae5f6fe2ca1179c2eff5a0
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `eclipse-temurin:8-ubi10-minimal` - linux; amd64

```console
$ docker pull eclipse-temurin@sha256:059bc04ea764035abe26feba11fb6ab930292a97e5be05e1c6cd085a25ed0a34
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **143.3 MB (143323484 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e4a3b0a1601ca0a4d042cd74e419b8d8bad5fe4b58f32e8765346484f4947603`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`

```dockerfile
# Fri, 01 Aug 2025 11:04:34 GMT
LABEL maintainer="Red Hat, Inc."
# Fri, 01 Aug 2025 11:04:34 GMT
LABEL vendor="Red Hat, Inc."
# Fri, 01 Aug 2025 11:04:34 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Fri, 01 Aug 2025 11:04:34 GMT
LABEL com.redhat.component="ubi10-minimal-container"       name="ubi10-minimal"       version="10.0"       distribution-scope="public"
# Fri, 01 Aug 2025 11:04:34 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Fri, 01 Aug 2025 11:04:34 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 10."
# Fri, 01 Aug 2025 11:04:34 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Fri, 01 Aug 2025 11:04:34 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Fri, 01 Aug 2025 11:04:34 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 10 Minimal"
# Fri, 01 Aug 2025 11:04:34 GMT
LABEL io.openshift.expose-services=""
# Fri, 01 Aug 2025 11:04:34 GMT
LABEL io.openshift.tags="minimal rhel10"
# Fri, 01 Aug 2025 11:04:34 GMT
ENV container oci
# Fri, 01 Aug 2025 11:04:34 GMT
COPY dir:d7d46744a920e661eed10a42e2080d8056941b338e371ab560c4c2eee7e7a070 in / 
# Fri, 01 Aug 2025 11:04:34 GMT
COPY file:6192e582bf96f2051240bfa3d022551f4c03d701d98b39d8aa709ddb4276e7a6 in /etc/yum.repos.d/. 
# Fri, 01 Aug 2025 11:04:34 GMT
CMD ["/bin/bash"]
# Fri, 01 Aug 2025 11:04:34 GMT
COPY file:2c9300aa2a82321bdb1295eb5cf59270c200f77d73b01c9b866932f5e4bf93c1 in /usr/share/buildinfo/content-sets.json 
# Fri, 01 Aug 2025 11:04:34 GMT
LABEL "build-date"="2025-08-07T17:00:12" "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="465bf4251c2aa299ea79fe7ffa726f3ee5f73787" "release"="1754585875"
# Fri, 01 Aug 2025 11:04:34 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 01 Aug 2025 11:04:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 01 Aug 2025 11:04:34 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 01 Aug 2025 11:04:34 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en         gnupg2     ;     microdnf clean all # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
ENV JAVA_VERSION=jdk8u462-b08
# Fri, 01 Aug 2025 11:04:34 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='19552c1cf7f5c18290a6bdcd6757f70ea5c331a2bc0dd7a3b3120e8dbc4b4891';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u462-b08/OpenJDK8U-jdk_aarch64_linux_hotspot_8u462b08.tar.gz';          ;;        ppc64le)          ESUM='3e4dbc94ebd299b60d8168b1d33cdae1f619db9403aaefd65d0b643615d596cc';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u462-b08/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u462b08.tar.gz';          ;;        x86_64)          ESUM='5d64ae542b59a962b3caadadd346f4b1c3010879a28bb02d928326993de16e79';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u462-b08/OpenJDK8U-jdk_x64_linux_hotspot_8u462b08.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip; # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
RUN set -eux;     echo "Verifying install ...";     echo "javac -version"; javac -version;     echo "java -version"; java -version;     echo "Complete." # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
```

-	Layers:
	-	`sha256:fe33f3d694b6e20455a988c4bdb920e5a216d54c81a4c79494b6d0debd58f76f`  
		Last Modified: Fri, 08 Aug 2025 00:12:36 GMT  
		Size: 33.5 MB (33498072 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a556805ebffe6205893c7dde55dcb8aaffd6f3461b7799657c3e9886d81671c`  
		Last Modified: Wed, 13 Aug 2025 23:02:21 GMT  
		Size: 55.1 MB (55091040 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32d597c8f1f86b648936488025b45aa165f0d2b30901e84f53f80e084e8cdbcc`  
		Last Modified: Wed, 13 Aug 2025 23:02:09 GMT  
		Size: 54.7 MB (54731930 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4246482e17cd524fd3021e7fc08418c86cff53dafa34f218498317476e7cc7d3`  
		Last Modified: Wed, 13 Aug 2025 23:01:54 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7fe4f027b093e502b20c744c0164fffe154feea3ca64191ee915a4d13f46aa03`  
		Last Modified: Wed, 13 Aug 2025 23:01:54 GMT  
		Size: 2.3 KB (2314 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:8-ubi10-minimal` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:3daec0f51b6a3cc5ab519634b20b90ac474c294c0dba9fe7fb9cfe94d7813ccd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5815643 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:acd192404011c26f04cd2cc213fa7e3e929ba3cac2bea17f5f9540ad8b138fb9`

```dockerfile
```

-	Layers:
	-	`sha256:668584411992d2359dcbe7a0df810aac84b7b01b1db16d9b9a3259aa4eccfd9a`  
		Last Modified: Thu, 14 Aug 2025 00:16:53 GMT  
		Size: 5.8 MB (5795561 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:81163788dd6081fd7401889e527a0810092698cde5c3592e958afa26ba108ac0`  
		Last Modified: Thu, 14 Aug 2025 00:16:53 GMT  
		Size: 20.1 KB (20082 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-temurin:8-ubi10-minimal` - linux; arm64 variant v8

```console
$ docker pull eclipse-temurin@sha256:b4bcdd4b99a668963c1190172f70be751b0f2298ce45e0049ba83503500ec4be
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **140.2 MB (140247757 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2435d9cbffbd4089888b39fa504b9eabecaf9ff12c111bbf7ba76d250b3aa6c2`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`

```dockerfile
# Fri, 01 Aug 2025 11:04:34 GMT
LABEL maintainer="Red Hat, Inc."
# Fri, 01 Aug 2025 11:04:34 GMT
LABEL vendor="Red Hat, Inc."
# Fri, 01 Aug 2025 11:04:34 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Fri, 01 Aug 2025 11:04:34 GMT
LABEL com.redhat.component="ubi10-minimal-container"       name="ubi10-minimal"       version="10.0"       distribution-scope="public"
# Fri, 01 Aug 2025 11:04:34 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Fri, 01 Aug 2025 11:04:34 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 10."
# Fri, 01 Aug 2025 11:04:34 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Fri, 01 Aug 2025 11:04:34 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Fri, 01 Aug 2025 11:04:34 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 10 Minimal"
# Fri, 01 Aug 2025 11:04:34 GMT
LABEL io.openshift.expose-services=""
# Fri, 01 Aug 2025 11:04:34 GMT
LABEL io.openshift.tags="minimal rhel10"
# Fri, 01 Aug 2025 11:04:34 GMT
ENV container oci
# Fri, 01 Aug 2025 11:04:34 GMT
COPY dir:8385fc5490591ca16c81e8d24d20265b9384f30798583b224537cb1d56b1a850 in / 
# Fri, 01 Aug 2025 11:04:34 GMT
COPY file:6192e582bf96f2051240bfa3d022551f4c03d701d98b39d8aa709ddb4276e7a6 in /etc/yum.repos.d/. 
# Fri, 01 Aug 2025 11:04:34 GMT
CMD ["/bin/bash"]
# Fri, 01 Aug 2025 11:04:34 GMT
COPY file:1336e2c89d9703119ed187d44098eb09fce9ba3e18cdf59cca6e0af5a093beef in /usr/share/buildinfo/content-sets.json 
# Fri, 01 Aug 2025 11:04:34 GMT
LABEL "build-date"="2025-08-07T17:06:24" "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="465bf4251c2aa299ea79fe7ffa726f3ee5f73787" "release"="1754585875"
# Fri, 01 Aug 2025 11:04:34 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 01 Aug 2025 11:04:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 01 Aug 2025 11:04:34 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 01 Aug 2025 11:04:34 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en         gnupg2     ;     microdnf clean all # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
ENV JAVA_VERSION=jdk8u462-b08
# Fri, 01 Aug 2025 11:04:34 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='19552c1cf7f5c18290a6bdcd6757f70ea5c331a2bc0dd7a3b3120e8dbc4b4891';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u462-b08/OpenJDK8U-jdk_aarch64_linux_hotspot_8u462b08.tar.gz';          ;;        ppc64le)          ESUM='3e4dbc94ebd299b60d8168b1d33cdae1f619db9403aaefd65d0b643615d596cc';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u462-b08/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u462b08.tar.gz';          ;;        x86_64)          ESUM='5d64ae542b59a962b3caadadd346f4b1c3010879a28bb02d928326993de16e79';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u462-b08/OpenJDK8U-jdk_x64_linux_hotspot_8u462b08.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip; # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
RUN set -eux;     echo "Verifying install ...";     echo "javac -version"; javac -version;     echo "java -version"; java -version;     echo "Complete." # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
```

-	Layers:
	-	`sha256:3ed98dc7fc2264d2da8c020e12ea4548801fafd192d4c74444ac087ada4c6d75`  
		Last Modified: Fri, 08 Aug 2025 00:12:34 GMT  
		Size: 31.5 MB (31546088 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0156aa0baa8f8522aa7e2a1820c735e597ad956ddf096f06ab53a2967160bae`  
		Last Modified: Thu, 14 Aug 2025 10:11:05 GMT  
		Size: 54.9 MB (54863066 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e521558598c000bba7aee90734c39034bf0abc40d81b724f7f5dae74d2f6ba33`  
		Last Modified: Thu, 14 Aug 2025 17:41:38 GMT  
		Size: 53.8 MB (53836159 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:309fc6d3620385e8ae3d08b746bff9c8ec26a7e534125b5ab07a6230bf525257`  
		Last Modified: Thu, 14 Aug 2025 09:56:15 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b67e22b1037dffa580adda012a4948c3b4ae7b7fdf1297beb55981b46664a4d`  
		Last Modified: Thu, 14 Aug 2025 09:56:15 GMT  
		Size: 2.3 KB (2316 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:8-ubi10-minimal` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:ab42155b441e124054a29a161dd51d1794ea7832307f9ccf5c9972884fba05ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5815946 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7f2e4878046a06af945f27272e8ee1571034cb396ef0c476d8307c2f53e1bcbd`

```dockerfile
```

-	Layers:
	-	`sha256:b23b512590fe467b8baa118b5c874416647aaf01a9cb1fa9eb82c3893966be3d`  
		Last Modified: Thu, 14 Aug 2025 12:17:08 GMT  
		Size: 5.8 MB (5795749 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f153cde2be2cce1a0807f77e909054fee8bc2b9b6c7a37fded3defb0f8b03aad`  
		Last Modified: Thu, 14 Aug 2025 12:17:10 GMT  
		Size: 20.2 KB (20197 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-temurin:8-ubi10-minimal` - linux; ppc64le

```console
$ docker pull eclipse-temurin@sha256:d6f992aca0ef6f51c5967ef0aad5ade7184f03c2705fdf029695637789c9e797
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **146.1 MB (146078860 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e524e17138d2383f56b107b73c4a2b297af9ff98d1db3a330216eb722da5ab92`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`

```dockerfile
# Fri, 01 Aug 2025 11:04:34 GMT
LABEL maintainer="Red Hat, Inc."
# Fri, 01 Aug 2025 11:04:34 GMT
LABEL vendor="Red Hat, Inc."
# Fri, 01 Aug 2025 11:04:34 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Fri, 01 Aug 2025 11:04:34 GMT
LABEL com.redhat.component="ubi10-minimal-container"       name="ubi10-minimal"       version="10.0"       distribution-scope="public"
# Fri, 01 Aug 2025 11:04:34 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Fri, 01 Aug 2025 11:04:34 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 10."
# Fri, 01 Aug 2025 11:04:34 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Fri, 01 Aug 2025 11:04:34 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Fri, 01 Aug 2025 11:04:34 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 10 Minimal"
# Fri, 01 Aug 2025 11:04:34 GMT
LABEL io.openshift.expose-services=""
# Fri, 01 Aug 2025 11:04:34 GMT
LABEL io.openshift.tags="minimal rhel10"
# Fri, 01 Aug 2025 11:04:34 GMT
ENV container oci
# Fri, 01 Aug 2025 11:04:34 GMT
COPY dir:640e0e573d0fea25191602587d27a678361464a59a51c46e7e2ad55c65a20739 in / 
# Fri, 01 Aug 2025 11:04:34 GMT
COPY file:6192e582bf96f2051240bfa3d022551f4c03d701d98b39d8aa709ddb4276e7a6 in /etc/yum.repos.d/. 
# Fri, 01 Aug 2025 11:04:34 GMT
CMD ["/bin/bash"]
# Fri, 01 Aug 2025 11:04:34 GMT
COPY file:1336e2c89d9703119ed187d44098eb09fce9ba3e18cdf59cca6e0af5a093beef in /usr/share/buildinfo/content-sets.json 
# Fri, 01 Aug 2025 11:04:34 GMT
LABEL "build-date"="2025-08-07T17:14:08" "architecture"="ppc64le" "vcs-type"="git" "vcs-ref"="465bf4251c2aa299ea79fe7ffa726f3ee5f73787" "release"="1754585875"
# Fri, 01 Aug 2025 11:04:34 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 01 Aug 2025 11:04:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 01 Aug 2025 11:04:34 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 01 Aug 2025 11:04:34 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en         gnupg2     ;     microdnf clean all # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
ENV JAVA_VERSION=jdk8u462-b08
# Fri, 01 Aug 2025 11:04:34 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='19552c1cf7f5c18290a6bdcd6757f70ea5c331a2bc0dd7a3b3120e8dbc4b4891';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u462-b08/OpenJDK8U-jdk_aarch64_linux_hotspot_8u462b08.tar.gz';          ;;        ppc64le)          ESUM='3e4dbc94ebd299b60d8168b1d33cdae1f619db9403aaefd65d0b643615d596cc';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u462-b08/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u462b08.tar.gz';          ;;        x86_64)          ESUM='5d64ae542b59a962b3caadadd346f4b1c3010879a28bb02d928326993de16e79';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u462-b08/OpenJDK8U-jdk_x64_linux_hotspot_8u462b08.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip; # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
RUN set -eux;     echo "Verifying install ...";     echo "javac -version"; javac -version;     echo "java -version"; java -version;     echo "Complete." # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Fri, 01 Aug 2025 11:04:34 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
```

-	Layers:
	-	`sha256:fbda37dec747d2d48a0b731bbc4647a80d0ad38995d3e592715932bca71e095c`  
		Last Modified: Fri, 08 Aug 2025 00:12:35 GMT  
		Size: 36.8 MB (36811145 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:624c78cc03453e81963d16cbd8cf44b57233f3676f5c0b5a6ae9b680b7e1aca3`  
		Last Modified: Thu, 14 Aug 2025 04:45:35 GMT  
		Size: 57.1 MB (57099241 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:781210be8310463ecb8251d343e0ffea10706865af14a9417bc281e98eb77fca`  
		Last Modified: Thu, 14 Aug 2025 04:45:39 GMT  
		Size: 52.2 MB (52166030 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d98e22e4f3d33a623a4e1365426b9f46a46e1075c9904f32a4d2deb78413b880`  
		Last Modified: Thu, 14 Aug 2025 04:45:12 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c46c5ac8931bc8bc62ad8fdfc77ff1e1efcab7d5de13202da7456b6c3693bcc`  
		Last Modified: Thu, 14 Aug 2025 04:45:13 GMT  
		Size: 2.3 KB (2316 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:8-ubi10-minimal` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:120177db3f9cdb691b7dcd6533687a0f10d96cefd477ec0d66ab171fd6545c4f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5803424 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f6272d04f7cd5aec692bf2c86452f7f729fa402b363e7220c07badf2b9cd421`

```dockerfile
```

-	Layers:
	-	`sha256:e5662d80e31d4e8e4d7ae73437d78cfca8bd347b46291919282420147407de06`  
		Last Modified: Thu, 14 Aug 2025 06:17:26 GMT  
		Size: 5.8 MB (5783306 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6d3dc66d569364f968f30e236235e720e67550d4443f3028694d5624c941cec4`  
		Last Modified: Thu, 14 Aug 2025 06:17:27 GMT  
		Size: 20.1 KB (20118 bytes)  
		MIME: application/vnd.in-toto+json
