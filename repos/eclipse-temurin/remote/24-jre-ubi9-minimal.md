## `eclipse-temurin:24-jre-ubi9-minimal`

```console
$ docker pull eclipse-temurin@sha256:65b8a1a4bdfdfab07f8c303db136e692223156cae89af62e5c1cc4692372b0eb
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

### `eclipse-temurin:24-jre-ubi9-minimal` - linux; amd64

```console
$ docker pull eclipse-temurin@sha256:8029d41203177fb7e90724fdadefca57ea828a3a9575df09bf2fce4c435f0775
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.6 MB (127560532 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ea9d51562e42e0ceec254d4d7e4215426c532ea0e4c6f7e5e4e3b7d41344367`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`

```dockerfile
# Tue, 25 Mar 2025 15:00:05 GMT
LABEL maintainer="Red Hat, Inc."
# Tue, 25 Mar 2025 15:00:05 GMT
LABEL vendor="Red Hat, Inc."
# Tue, 25 Mar 2025 15:00:06 GMT
LABEL url="https://www.redhat.com"
# Tue, 25 Mar 2025 15:00:06 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.5"       distribution-scope="public"
# Tue, 25 Mar 2025 15:00:06 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Tue, 25 Mar 2025 15:00:06 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Tue, 25 Mar 2025 15:00:06 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Tue, 25 Mar 2025 15:00:06 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Tue, 25 Mar 2025 15:00:06 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Tue, 25 Mar 2025 15:00:06 GMT
LABEL io.openshift.expose-services=""
# Tue, 25 Mar 2025 15:00:06 GMT
LABEL io.openshift.tags="minimal rhel9"
# Tue, 25 Mar 2025 15:00:06 GMT
ENV container oci
# Tue, 25 Mar 2025 15:00:06 GMT
COPY dir:df27096315f97be2134faf11df5dc31f92c8dd671e0b8267905e1f2330865336 in / 
# Tue, 25 Mar 2025 15:00:06 GMT
COPY file:b37d593713ee21ad52a4cd1424dc019a24f7966f85df0ac4b86d234302695328 in /etc/yum.repos.d/. 
# Tue, 25 Mar 2025 15:00:06 GMT
CMD ["/bin/bash"]
# Tue, 25 Mar 2025 15:00:06 GMT
RUN . /cachi2/cachi2.env &&     rm -rf /var/log/*
# Tue, 25 Mar 2025 15:00:07 GMT
LABEL "build-date"="2025-03-25T14:59:41" "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="63823c7605fee63261a8e33cad8085bc4bb24676" "build-date"="2025-03-25T14:50:12Z" "release"="1742914212"
# Tue, 25 Mar 2025 15:00:12 GMT
RUN /bin/sh
# Tue, 25 Mar 2025 17:58:27 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 25 Mar 2025 17:58:27 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 25 Mar 2025 17:58:27 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 25 Mar 2025 17:58:27 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en     ;     microdnf clean all # buildkit
# Tue, 25 Mar 2025 17:58:27 GMT
ENV JAVA_VERSION=jdk-24+36
# Tue, 25 Mar 2025 17:58:27 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='782a46008490272affe0b797155c2ae8e759e10c8ba4540f1f7285ef3d2902de';          BINARY_URL='https://github.com/adoptium/temurin24-binaries/releases/download/jdk-24%2B36/OpenJDK24U-jre_aarch64_linux_hotspot_24_36.tar.gz';          ;;        ppc64le)          ESUM='e7c90ab80d5e9419f794aee63c8f1bf3ed29e656d4e8e967a45d3069bd643c07';          BINARY_URL='https://github.com/adoptium/temurin24-binaries/releases/download/jdk-24%2B36/OpenJDK24U-jre_ppc64le_linux_hotspot_24_36.tar.gz';          ;;        s390x)          ESUM='65a9a1e685b81bf80d89a5b45d5f49655e938f3e175accf98c2cb13df07753fd';          BINARY_URL='https://github.com/adoptium/temurin24-binaries/releases/download/jdk-24%2B36/OpenJDK24U-jre_s390x_linux_hotspot_24_36.tar.gz';          ;;        x86_64)          ESUM='e8d8f5707d765a6bfca3de61320e0bb2618191c77947bc467ac5021e6193f351';          BINARY_URL='https://github.com/adoptium/temurin24-binaries/releases/download/jdk-24%2B36/OpenJDK24U-jre_x64_linux_hotspot_24_36.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz; # buildkit
# Tue, 25 Mar 2025 17:58:27 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 25 Mar 2025 17:58:27 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 25 Mar 2025 17:58:27 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
```

-	Layers:
	-	`sha256:9d561c17444a5f9cb82fc40d3d0e3f59b9f53e51dfb1c9e3d71c5c3ff898d151`  
		Last Modified: Tue, 25 Mar 2025 17:57:41 GMT  
		Size: 39.4 MB (39406022 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:adc97f92dbce4567ee13d265c17bca44426acd9f0e61a1f559344ae03bb336d2`  
		Last Modified: Tue, 25 Mar 2025 17:57:40 GMT  
		Size: 453.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4226d285fcae4b262c19742acd10eb1d376687d92b3e00a7ae74a26486357056`  
		Last Modified: Thu, 27 Mar 2025 17:59:36 GMT  
		Size: 27.3 MB (27325799 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73057cfedd41b6efd0f6e99ed91a35c5a4a3a507adf9534b572211bbacdbc20b`  
		Last Modified: Thu, 27 Mar 2025 17:59:37 GMT  
		Size: 60.8 MB (60825839 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:816607f37af3ef9c6099e39198e3d689e444ff7c4183cdc5ce823ec925b21ffc`  
		Last Modified: Thu, 27 Mar 2025 17:59:35 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b43452e8e8389c48b99b7574cc89f886fc1d407ab1f1ac5790141ae49818430c`  
		Last Modified: Thu, 27 Mar 2025 17:59:35 GMT  
		Size: 2.3 KB (2291 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:24-jre-ubi9-minimal` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:55fe028c294b4ad04b07b0a35cd354f5722595e03de261615de53973ccacffec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2401244 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:217f38b999777db6bdb60a39a8f4cb8f10a97d96e7ec34a9b825a5eb780b0f8a`

```dockerfile
```

-	Layers:
	-	`sha256:e03f07d2b9f9ac76bf18d6a12bcf8d9bd45aa08e21a20da34b2d54be7be8ee03`  
		Last Modified: Thu, 27 Mar 2025 17:59:36 GMT  
		Size: 2.4 MB (2380371 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e63c38ec7f25af8fee9bd4b02131ce95d24d0ed784614bf20a9ba997befa7183`  
		Last Modified: Thu, 27 Mar 2025 17:59:35 GMT  
		Size: 20.9 KB (20873 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-temurin:24-jre-ubi9-minimal` - linux; arm64 variant v8

```console
$ docker pull eclipse-temurin@sha256:5640df402614d0e25ad4302202095f5631116d93593aa46eff4cfc32e256bcc0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **125.2 MB (125218641 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:083388984feb2d3c97dff6576780c615221a762a24876bbd1db93b7532fc50a1`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`

```dockerfile
# Tue, 25 Mar 2025 15:05:12 GMT
LABEL maintainer="Red Hat, Inc."
# Tue, 25 Mar 2025 15:05:12 GMT
LABEL vendor="Red Hat, Inc."
# Tue, 25 Mar 2025 15:05:12 GMT
LABEL url="https://www.redhat.com"
# Tue, 25 Mar 2025 15:05:12 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.5"       distribution-scope="public"
# Tue, 25 Mar 2025 15:05:12 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Tue, 25 Mar 2025 15:05:13 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Tue, 25 Mar 2025 15:05:13 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Tue, 25 Mar 2025 15:05:13 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Tue, 25 Mar 2025 15:05:13 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Tue, 25 Mar 2025 15:05:13 GMT
LABEL io.openshift.expose-services=""
# Tue, 25 Mar 2025 15:05:13 GMT
LABEL io.openshift.tags="minimal rhel9"
# Tue, 25 Mar 2025 15:05:13 GMT
ENV container oci
# Tue, 25 Mar 2025 15:05:14 GMT
COPY dir:36dabe56d778e21d6cac6872809f7ae0932c9956fe7621a40aed471a4eb28b35 in / 
# Tue, 25 Mar 2025 15:05:14 GMT
COPY file:b37d593713ee21ad52a4cd1424dc019a24f7966f85df0ac4b86d234302695328 in /etc/yum.repos.d/. 
# Tue, 25 Mar 2025 15:05:14 GMT
CMD ["/bin/bash"]
# Tue, 25 Mar 2025 15:05:14 GMT
RUN . /cachi2/cachi2.env &&     rm -rf /var/log/*
# Tue, 25 Mar 2025 15:05:14 GMT
LABEL "build-date"="2025-03-25T15:04:42" "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="63823c7605fee63261a8e33cad8085bc4bb24676" "build-date"="2025-03-25T14:50:12Z" "release"="1742914212"
# Tue, 25 Mar 2025 15:05:25 GMT
RUN /bin/sh
# Tue, 25 Mar 2025 17:58:27 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 25 Mar 2025 17:58:27 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 25 Mar 2025 17:58:27 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 25 Mar 2025 17:58:27 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en     ;     microdnf clean all # buildkit
# Tue, 25 Mar 2025 17:58:27 GMT
ENV JAVA_VERSION=jdk-24+36
# Tue, 25 Mar 2025 17:58:27 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='782a46008490272affe0b797155c2ae8e759e10c8ba4540f1f7285ef3d2902de';          BINARY_URL='https://github.com/adoptium/temurin24-binaries/releases/download/jdk-24%2B36/OpenJDK24U-jre_aarch64_linux_hotspot_24_36.tar.gz';          ;;        ppc64le)          ESUM='e7c90ab80d5e9419f794aee63c8f1bf3ed29e656d4e8e967a45d3069bd643c07';          BINARY_URL='https://github.com/adoptium/temurin24-binaries/releases/download/jdk-24%2B36/OpenJDK24U-jre_ppc64le_linux_hotspot_24_36.tar.gz';          ;;        s390x)          ESUM='65a9a1e685b81bf80d89a5b45d5f49655e938f3e175accf98c2cb13df07753fd';          BINARY_URL='https://github.com/adoptium/temurin24-binaries/releases/download/jdk-24%2B36/OpenJDK24U-jre_s390x_linux_hotspot_24_36.tar.gz';          ;;        x86_64)          ESUM='e8d8f5707d765a6bfca3de61320e0bb2618191c77947bc467ac5021e6193f351';          BINARY_URL='https://github.com/adoptium/temurin24-binaries/releases/download/jdk-24%2B36/OpenJDK24U-jre_x64_linux_hotspot_24_36.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz; # buildkit
# Tue, 25 Mar 2025 17:58:27 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 25 Mar 2025 17:58:27 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 25 Mar 2025 17:58:27 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
```

-	Layers:
	-	`sha256:7b061f511294c383e785796c55415ec3bed7fbb0a98d6cee8c8c6a1436d4ada8`  
		Last Modified: Tue, 25 Mar 2025 18:27:33 GMT  
		Size: 37.6 MB (37588703 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d6607d3dbc4fd04e0d544f944d20a47a5af1fa8a7520e1f37683ab236e23734`  
		Last Modified: Tue, 25 Mar 2025 18:27:31 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4fe6d8a840a9a19a4792a64986c4f2705bdfa57e1b81dec892e5e52397ad6ca`  
		Last Modified: Thu, 27 Mar 2025 18:07:23 GMT  
		Size: 27.7 MB (27743807 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b045901d4107ce3989177ebcd6430a64f45cc7682cf4c5cee2ce16998a90acb`  
		Last Modified: Thu, 27 Mar 2025 18:12:29 GMT  
		Size: 59.9 MB (59883259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fac218001a9eb02cad668c135f5f42e5ac6db55e8ad4c9f9bfe8f723db1bf12f`  
		Last Modified: Thu, 27 Mar 2025 18:12:27 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d627070907f0a573da4eb43beffc61f44025e091c3f943fee84e40b95b5c2397`  
		Last Modified: Thu, 27 Mar 2025 18:12:27 GMT  
		Size: 2.3 KB (2290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:24-jre-ubi9-minimal` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:a60d605fe323e0ae6384a253a909edebd74aa42025c3aca082269903400075c9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2400528 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:12aed1f24b01615fb6b617d87c6611494288c22d6e700efe457b45a2bbfbf0d1`

```dockerfile
```

-	Layers:
	-	`sha256:0fc6768bf46322e4880a14c2b8b6505c479e0364ec73573c9fb6fa5edae0444a`  
		Last Modified: Thu, 27 Mar 2025 18:12:27 GMT  
		Size: 2.4 MB (2379551 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:27eb8668634054e7672226abccd277e00d533651a4b5f327dd003a4290fec240`  
		Last Modified: Thu, 27 Mar 2025 18:12:27 GMT  
		Size: 21.0 KB (20977 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-temurin:24-jre-ubi9-minimal` - linux; ppc64le

```console
$ docker pull eclipse-temurin@sha256:41d173517dcfd68e00ffe1dce4026a33905dd3c3609e3eb8526e03ec955fa876
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.2 MB (134199830 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f8064c72c3581d3baa9a6c250c7fbad3612ed96e180b6f8d7adbeb32aceb0f2f`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`

```dockerfile
# Tue, 25 Mar 2025 15:07:41 GMT
LABEL maintainer="Red Hat, Inc."
# Tue, 25 Mar 2025 15:07:41 GMT
LABEL vendor="Red Hat, Inc."
# Tue, 25 Mar 2025 15:07:41 GMT
LABEL url="https://www.redhat.com"
# Tue, 25 Mar 2025 15:07:41 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.5"       distribution-scope="public"
# Tue, 25 Mar 2025 15:07:41 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Tue, 25 Mar 2025 15:07:41 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Tue, 25 Mar 2025 15:07:41 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Tue, 25 Mar 2025 15:07:41 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Tue, 25 Mar 2025 15:07:41 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Tue, 25 Mar 2025 15:07:41 GMT
LABEL io.openshift.expose-services=""
# Tue, 25 Mar 2025 15:07:41 GMT
LABEL io.openshift.tags="minimal rhel9"
# Tue, 25 Mar 2025 15:07:41 GMT
ENV container oci
# Tue, 25 Mar 2025 15:07:42 GMT
COPY dir:b00ac549f2dec3c1bd1264d0d7e9b7a2b7f966cc212ebc6aee6ca6e7f8acdce4 in / 
# Tue, 25 Mar 2025 15:07:42 GMT
COPY file:b37d593713ee21ad52a4cd1424dc019a24f7966f85df0ac4b86d234302695328 in /etc/yum.repos.d/. 
# Tue, 25 Mar 2025 15:07:42 GMT
CMD ["/bin/bash"]
# Tue, 25 Mar 2025 15:07:43 GMT
RUN . /cachi2/cachi2.env &&     rm -rf /var/log/*
# Tue, 25 Mar 2025 15:07:43 GMT
LABEL "build-date"="2025-03-25T15:07:15" "architecture"="ppc64le" "vcs-type"="git" "vcs-ref"="63823c7605fee63261a8e33cad8085bc4bb24676" "build-date"="2025-03-25T14:50:12Z" "release"="1742914212"
# Tue, 25 Mar 2025 15:08:06 GMT
RUN /bin/sh
# Tue, 25 Mar 2025 17:58:27 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 25 Mar 2025 17:58:27 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 25 Mar 2025 17:58:27 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 25 Mar 2025 17:58:27 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en     ;     microdnf clean all # buildkit
# Tue, 25 Mar 2025 17:58:27 GMT
ENV JAVA_VERSION=jdk-24+36
# Tue, 25 Mar 2025 17:58:27 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='782a46008490272affe0b797155c2ae8e759e10c8ba4540f1f7285ef3d2902de';          BINARY_URL='https://github.com/adoptium/temurin24-binaries/releases/download/jdk-24%2B36/OpenJDK24U-jre_aarch64_linux_hotspot_24_36.tar.gz';          ;;        ppc64le)          ESUM='e7c90ab80d5e9419f794aee63c8f1bf3ed29e656d4e8e967a45d3069bd643c07';          BINARY_URL='https://github.com/adoptium/temurin24-binaries/releases/download/jdk-24%2B36/OpenJDK24U-jre_ppc64le_linux_hotspot_24_36.tar.gz';          ;;        s390x)          ESUM='65a9a1e685b81bf80d89a5b45d5f49655e938f3e175accf98c2cb13df07753fd';          BINARY_URL='https://github.com/adoptium/temurin24-binaries/releases/download/jdk-24%2B36/OpenJDK24U-jre_s390x_linux_hotspot_24_36.tar.gz';          ;;        x86_64)          ESUM='e8d8f5707d765a6bfca3de61320e0bb2618191c77947bc467ac5021e6193f351';          BINARY_URL='https://github.com/adoptium/temurin24-binaries/releases/download/jdk-24%2B36/OpenJDK24U-jre_x64_linux_hotspot_24_36.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz; # buildkit
# Tue, 25 Mar 2025 17:58:27 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 25 Mar 2025 17:58:27 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 25 Mar 2025 17:58:27 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
```

-	Layers:
	-	`sha256:32cf36dcf251c02cfc81f25bda80482c1e6394e4c1c7cb07317eebdc82a6ef45`  
		Last Modified: Tue, 25 Mar 2025 18:27:46 GMT  
		Size: 43.8 MB (43784360 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37f45749a0d155c224422d2f971c243e88e0afd5c485b88efda6760e3b544483`  
		Last Modified: Tue, 25 Mar 2025 18:27:43 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87fed99b32c92f36f6b421efa94367eed10b83edeecbacfa18dca2b5821dfb3b`  
		Last Modified: Thu, 27 Mar 2025 18:00:08 GMT  
		Size: 29.7 MB (29745465 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bab116c0e038fff780243be93e8da91c2b3695f0753ca4fbf5a5cb426932ad4b`  
		Last Modified: Thu, 27 Mar 2025 18:09:14 GMT  
		Size: 60.7 MB (60667132 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df8943cedb1a9ea772c50631e1c1d107f3f710a75c94c072441ebd9576e72213`  
		Last Modified: Thu, 27 Mar 2025 18:09:12 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e8201bf06cb08348dec45dd781f97429b668595878cf6493aec4b7fa5c5d30c`  
		Last Modified: Thu, 27 Mar 2025 18:09:12 GMT  
		Size: 2.3 KB (2291 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:24-jre-ubi9-minimal` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:8f2141c2c38d64021284a1cd87e80d11acf6ad48283386be9055ad97e79fe229
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2400482 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:16cec682c92a8d1015ee733e36fbaa398c54f1dd439ed9535ce91cbca0a0adc6`

```dockerfile
```

-	Layers:
	-	`sha256:6dfd6877adb0481bdb58052d14c9a1a9486cfaf88de5f391fa20f0f4a99572d4`  
		Last Modified: Thu, 27 Mar 2025 18:09:12 GMT  
		Size: 2.4 MB (2379580 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:09e9679e4902b402aee4c25e5841d124e3ab859c6dda07d7bf51b5f67ae11dfb`  
		Last Modified: Thu, 27 Mar 2025 18:09:12 GMT  
		Size: 20.9 KB (20902 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-temurin:24-jre-ubi9-minimal` - linux; s390x

```console
$ docker pull eclipse-temurin@sha256:ac27e8817222597290e714a7a92beb2d770b135d86389a279098b7cb17f9e330
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **122.4 MB (122440524 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:49d32bd0e386b1dc2056e11f0fa81b2e414be095f4e66972df09f4efc622a8e1`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`

```dockerfile
# Tue, 25 Mar 2025 15:02:51 GMT
LABEL maintainer="Red Hat, Inc."
# Tue, 25 Mar 2025 15:02:51 GMT
LABEL vendor="Red Hat, Inc."
# Tue, 25 Mar 2025 15:02:51 GMT
LABEL url="https://www.redhat.com"
# Tue, 25 Mar 2025 15:02:51 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.5"       distribution-scope="public"
# Tue, 25 Mar 2025 15:02:51 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Tue, 25 Mar 2025 15:02:51 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Tue, 25 Mar 2025 15:02:51 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Tue, 25 Mar 2025 15:02:51 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Tue, 25 Mar 2025 15:02:51 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Tue, 25 Mar 2025 15:02:51 GMT
LABEL io.openshift.expose-services=""
# Tue, 25 Mar 2025 15:02:51 GMT
LABEL io.openshift.tags="minimal rhel9"
# Tue, 25 Mar 2025 15:02:51 GMT
ENV container oci
# Tue, 25 Mar 2025 15:02:52 GMT
COPY dir:a7bb5171f825e631f2fbfeb72bf76644ef5188e2e0888380a0572aaba26faac9 in / 
# Tue, 25 Mar 2025 15:02:52 GMT
COPY file:b37d593713ee21ad52a4cd1424dc019a24f7966f85df0ac4b86d234302695328 in /etc/yum.repos.d/. 
# Tue, 25 Mar 2025 15:02:52 GMT
CMD ["/bin/bash"]
# Tue, 25 Mar 2025 15:02:53 GMT
RUN . /cachi2/cachi2.env &&     rm -rf /var/log/*
# Tue, 25 Mar 2025 15:02:53 GMT
LABEL "build-date"="2025-03-25T15:02:03" "architecture"="s390x" "vcs-type"="git" "vcs-ref"="63823c7605fee63261a8e33cad8085bc4bb24676" "build-date"="2025-03-25T14:50:12Z" "release"="1742914212"
# Tue, 25 Mar 2025 15:03:05 GMT
RUN /bin/sh
# Tue, 25 Mar 2025 17:58:27 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 25 Mar 2025 17:58:27 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 25 Mar 2025 17:58:27 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 25 Mar 2025 17:58:27 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en     ;     microdnf clean all # buildkit
# Tue, 25 Mar 2025 17:58:27 GMT
ENV JAVA_VERSION=jdk-24+36
# Tue, 25 Mar 2025 17:58:27 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='782a46008490272affe0b797155c2ae8e759e10c8ba4540f1f7285ef3d2902de';          BINARY_URL='https://github.com/adoptium/temurin24-binaries/releases/download/jdk-24%2B36/OpenJDK24U-jre_aarch64_linux_hotspot_24_36.tar.gz';          ;;        ppc64le)          ESUM='e7c90ab80d5e9419f794aee63c8f1bf3ed29e656d4e8e967a45d3069bd643c07';          BINARY_URL='https://github.com/adoptium/temurin24-binaries/releases/download/jdk-24%2B36/OpenJDK24U-jre_ppc64le_linux_hotspot_24_36.tar.gz';          ;;        s390x)          ESUM='65a9a1e685b81bf80d89a5b45d5f49655e938f3e175accf98c2cb13df07753fd';          BINARY_URL='https://github.com/adoptium/temurin24-binaries/releases/download/jdk-24%2B36/OpenJDK24U-jre_s390x_linux_hotspot_24_36.tar.gz';          ;;        x86_64)          ESUM='e8d8f5707d765a6bfca3de61320e0bb2618191c77947bc467ac5021e6193f351';          BINARY_URL='https://github.com/adoptium/temurin24-binaries/releases/download/jdk-24%2B36/OpenJDK24U-jre_x64_linux_hotspot_24_36.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz; # buildkit
# Tue, 25 Mar 2025 17:58:27 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 25 Mar 2025 17:58:27 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 25 Mar 2025 17:58:27 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
```

-	Layers:
	-	`sha256:74f4d563c72f05b431ebba5e82692949551dc223392c5db8c42b58bb6f55d86e`  
		Last Modified: Tue, 25 Mar 2025 18:27:40 GMT  
		Size: 37.5 MB (37501550 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ad3638df35816097dbfdec8d194c1189b9a49dd23bab5049024abcbef9c3efd`  
		Last Modified: Tue, 25 Mar 2025 18:27:37 GMT  
		Size: 459.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c8d675bd80e5be8d9b7a9270e457848dbc6a4a7bd4b57766275a687b3548f37`  
		Last Modified: Thu, 27 Mar 2025 18:02:24 GMT  
		Size: 27.3 MB (27334345 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9c064e93095e0765dad29f16c2be68c3418446673f08dec495a9a74418c4804`  
		Last Modified: Thu, 27 Mar 2025 18:12:26 GMT  
		Size: 57.6 MB (57601753 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db979f2644c77ac96808ad5c4aca70c630810cc1dc0a8dbbe81363c30552ba4f`  
		Last Modified: Thu, 27 Mar 2025 18:12:24 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2bc42f90f18f2abf51d43ee0c1cbc0e5f40f52e03f768959af6c2dfc3862cb9d`  
		Last Modified: Thu, 27 Mar 2025 18:12:24 GMT  
		Size: 2.3 KB (2290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:24-jre-ubi9-minimal` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:3260f37162aede256afdfb7d9aea856a16303fcafb8ceba993d292ecfce419f1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2392240 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:81034622e7085b3bd8d67edfdeb412ca0845849a9cd38ca8ce7cc51ea3872578`

```dockerfile
```

-	Layers:
	-	`sha256:fc9674bf74f811beb9cf6d5c374fd33c06b1ab195a61051acf9a60e4af1ffa92`  
		Last Modified: Thu, 27 Mar 2025 18:12:25 GMT  
		Size: 2.4 MB (2371367 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:80a2417b425ec691dab24e79209078e1c9c0bf678a7e87c53464337b2c16d9af`  
		Last Modified: Thu, 27 Mar 2025 18:12:24 GMT  
		Size: 20.9 KB (20873 bytes)  
		MIME: application/vnd.in-toto+json
