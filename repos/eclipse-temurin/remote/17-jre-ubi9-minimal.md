## `eclipse-temurin:17-jre-ubi9-minimal`

```console
$ docker pull eclipse-temurin@sha256:958c7acd16f2e333ca33530cad909cf111bc62d478192d6e9aa553c65efc9e2b
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

### `eclipse-temurin:17-jre-ubi9-minimal` - linux; amd64

```console
$ docker pull eclipse-temurin@sha256:f090e13eb528f1ebd3e31847fa033c85d6aea2c822897f156bfc9c424ff55a34
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **123.3 MB (123299147 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f3a1c8bf2fa75a774d8bfd054c6d4ccb698b039d7de04fff5607d5b373fcb677`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`

```dockerfile
# Thu, 30 Jan 2025 14:32:57 GMT
LABEL maintainer="Red Hat, Inc."
# Thu, 30 Jan 2025 14:32:57 GMT
LABEL vendor="Red Hat, Inc."
# Thu, 30 Jan 2025 14:32:57 GMT
LABEL url="https://www.redhat.com"
# Thu, 30 Jan 2025 14:32:57 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.5"       distribution-scope="public"
# Thu, 30 Jan 2025 14:32:57 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Thu, 30 Jan 2025 14:32:57 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Thu, 30 Jan 2025 14:32:57 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 30 Jan 2025 14:32:57 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 30 Jan 2025 14:32:57 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Thu, 30 Jan 2025 14:32:57 GMT
LABEL io.openshift.expose-services=""
# Thu, 30 Jan 2025 14:32:57 GMT
LABEL io.openshift.tags="minimal rhel9"
# Thu, 30 Jan 2025 14:32:57 GMT
ENV container oci
# Thu, 30 Jan 2025 14:32:57 GMT
COPY dir:0423d0cd4a34047821e55a2806cb02fc682f017fba03e4344223878a61041986 in / 
# Thu, 30 Jan 2025 14:32:57 GMT
COPY file:b37d593713ee21ad52a4cd1424dc019a24f7966f85df0ac4b86d234302695328 in /etc/yum.repos.d/. 
# Thu, 30 Jan 2025 14:32:57 GMT
CMD ["/bin/bash"]
# Thu, 30 Jan 2025 14:32:57 GMT
RUN . /cachi2/cachi2.env &&     rm -rf /var/log/*
# Thu, 30 Jan 2025 14:32:57 GMT
LABEL "build-date"="2025-02-13T04:19:45" "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="c0546ad1ce412f8077a547cb8d0d68d04f08815c" "build-date"="2025-02-13T04:15:47Z" "release"="1739420147"
# Thu, 30 Jan 2025 14:32:57 GMT
RUN /bin/sh
# Thu, 30 Jan 2025 14:32:57 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 30 Jan 2025 14:32:57 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 30 Jan 2025 14:32:57 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 30 Jan 2025 14:32:57 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         fontconfig         glibc-langpack-en     ;     microdnf clean all # buildkit
# Thu, 30 Jan 2025 14:32:57 GMT
ENV JAVA_VERSION=jdk-17.0.14+7
# Thu, 30 Jan 2025 14:32:57 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='bab3f352fc7144ac1435924f056872d16f4b32c8bcda58b9a77b636eb1c664f4';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.14_7.tar.gz';          ;;        ppc64le)          ESUM='2a730e9d34cce4d588739b626a034ed68c065a2db61048ee7886be48ec9fe460';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.14_7.tar.gz';          ;;        s390x)          ESUM='3887f14f95a14e65a985cfcee6696e01aadee06d3347ab70eb7d6b16ce397238';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_s390x_linux_hotspot_17.0.14_7.tar.gz';          ;;        x86_64)          ESUM='a4b0015872758aac6a5d17139e952a3951ee536ae6d9a99828823a80a71add56';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_x64_linux_hotspot_17.0.14_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz; # buildkit
# Thu, 30 Jan 2025 14:32:57 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 30 Jan 2025 14:32:57 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 30 Jan 2025 14:32:57 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
```

-	Layers:
	-	`sha256:3333307dcd2e4279579646a05a5f99082a61a20906175240445b0e15f73b6d6e`  
		Last Modified: Thu, 13 Feb 2025 06:13:39 GMT  
		Size: 39.4 MB (39366553 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5025173ec0b35686a33458b367c2a6e898c824f57a07925c25d26a0cfb5f2e50`  
		Last Modified: Thu, 13 Feb 2025 06:13:37 GMT  
		Size: 461.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dab594ebef542d8a0b0f8f7b99dedf9777ee9ad4566adc5c0407f464856a0e5a`  
		Last Modified: Fri, 14 Feb 2025 04:14:01 GMT  
		Size: 37.0 MB (36979801 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de35d4cd6d3caeaf58cacc422dc59452e55e5b43093325d680136b27ad95ed89`  
		Last Modified: Fri, 14 Feb 2025 04:14:02 GMT  
		Size: 46.9 MB (46949914 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d10a54d8e62e2e94521cab682b169276d7fade19a225309c2c7bd3c047fee584`  
		Last Modified: Fri, 14 Feb 2025 04:14:00 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31f385c99999cf91b8da1399a6b3abbe3141cfe31b4d9252e15402174045b933`  
		Last Modified: Fri, 14 Feb 2025 01:27:33 GMT  
		Size: 2.3 KB (2291 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:17-jre-ubi9-minimal` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:a6a92e8e700bfb9f8fbca855de298403f67e1edfc6cb4efa404c1fff0ab6d396
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3603106 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba9917e42e40883b5139f85d6d4d97191506fba7bd3b53c004e775d1122e39e8`

```dockerfile
```

-	Layers:
	-	`sha256:76883b80d26d3ed756e7507f7f3fe8025aa4546b3b588c5dbeeab1d94d5f3a93`  
		Last Modified: Fri, 14 Feb 2025 04:13:58 GMT  
		Size: 3.6 MB (3582349 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e14b78b8f13f88361e5b636ea7fb057fc676f7c5aa1c463cbf0577d9c3134166`  
		Last Modified: Fri, 14 Feb 2025 04:13:58 GMT  
		Size: 20.8 KB (20757 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-temurin:17-jre-ubi9-minimal` - linux; arm64 variant v8

```console
$ docker pull eclipse-temurin@sha256:01e697861f353888449d8664efe3e5b50bf938734e6a9f3c962a4a40fc1ba7e3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **121.5 MB (121529511 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:109d70fb99c70768eb7b635334d63795b3d0307b5e2061b64ba994049a9949b9`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`

```dockerfile
# Thu, 30 Jan 2025 14:32:57 GMT
LABEL maintainer="Red Hat, Inc."
# Thu, 30 Jan 2025 14:32:57 GMT
LABEL vendor="Red Hat, Inc."
# Thu, 30 Jan 2025 14:32:57 GMT
LABEL url="https://www.redhat.com"
# Thu, 30 Jan 2025 14:32:57 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.5"       distribution-scope="public"
# Thu, 30 Jan 2025 14:32:57 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Thu, 30 Jan 2025 14:32:57 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Thu, 30 Jan 2025 14:32:57 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 30 Jan 2025 14:32:57 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 30 Jan 2025 14:32:57 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Thu, 30 Jan 2025 14:32:57 GMT
LABEL io.openshift.expose-services=""
# Thu, 30 Jan 2025 14:32:57 GMT
LABEL io.openshift.tags="minimal rhel9"
# Thu, 30 Jan 2025 14:32:57 GMT
ENV container oci
# Thu, 30 Jan 2025 14:32:57 GMT
COPY dir:5809c16e2c5c048de6a8d8eea9437ac183b7d2503e26b24a2422ead5736aecad in / 
# Thu, 30 Jan 2025 14:32:57 GMT
COPY file:b37d593713ee21ad52a4cd1424dc019a24f7966f85df0ac4b86d234302695328 in /etc/yum.repos.d/. 
# Thu, 30 Jan 2025 14:32:57 GMT
CMD ["/bin/bash"]
# Thu, 30 Jan 2025 14:32:57 GMT
RUN . /cachi2/cachi2.env &&     rm -rf /var/log/*
# Thu, 30 Jan 2025 14:32:57 GMT
LABEL "build-date"="2025-02-13T04:25:01" "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="c0546ad1ce412f8077a547cb8d0d68d04f08815c" "build-date"="2025-02-13T04:15:47Z" "release"="1739420147"
# Thu, 30 Jan 2025 14:32:57 GMT
RUN /bin/sh
# Thu, 30 Jan 2025 14:32:57 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 30 Jan 2025 14:32:57 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 30 Jan 2025 14:32:57 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 30 Jan 2025 14:32:57 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         fontconfig         glibc-langpack-en     ;     microdnf clean all # buildkit
# Thu, 30 Jan 2025 14:32:57 GMT
ENV JAVA_VERSION=jdk-17.0.14+7
# Thu, 30 Jan 2025 14:32:57 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='bab3f352fc7144ac1435924f056872d16f4b32c8bcda58b9a77b636eb1c664f4';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.14_7.tar.gz';          ;;        ppc64le)          ESUM='2a730e9d34cce4d588739b626a034ed68c065a2db61048ee7886be48ec9fe460';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.14_7.tar.gz';          ;;        s390x)          ESUM='3887f14f95a14e65a985cfcee6696e01aadee06d3347ab70eb7d6b16ce397238';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_s390x_linux_hotspot_17.0.14_7.tar.gz';          ;;        x86_64)          ESUM='a4b0015872758aac6a5d17139e952a3951ee536ae6d9a99828823a80a71add56';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_x64_linux_hotspot_17.0.14_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz; # buildkit
# Thu, 30 Jan 2025 14:32:57 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 30 Jan 2025 14:32:57 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 30 Jan 2025 14:32:57 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
```

-	Layers:
	-	`sha256:56631da24b0de345717238daea2e3e61c768d081572916ae06b08b19126a740d`  
		Last Modified: Thu, 13 Feb 2025 06:13:39 GMT  
		Size: 37.6 MB (37626059 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5aee836c3728069e82153bf7b209c409d3343adaea6ab6b31546e5ce09250db5`  
		Last Modified: Thu, 13 Feb 2025 06:13:36 GMT  
		Size: 460.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d886f1d0418fbd67439d630adb0cd82ab5ccf9bc0d3c039cbd36d622e8eaa96`  
		Last Modified: Fri, 14 Feb 2025 04:27:18 GMT  
		Size: 37.4 MB (37436415 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed361d4bb16ef77e10eaff8cc034d1961e73e12c1de7abd7eabf177c13a7677a`  
		Last Modified: Fri, 14 Feb 2025 02:00:42 GMT  
		Size: 46.5 MB (46464156 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0bb5efabeb0ddea89014e04203a71174c9cb68c4fa8d1df4044f1e30417db8d2`  
		Last Modified: Fri, 14 Feb 2025 02:00:41 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77ef07a22071062325d876398b75b39fd501dc977be4ad6456a1b8e17736e1ff`  
		Last Modified: Fri, 14 Feb 2025 02:27:28 GMT  
		Size: 2.3 KB (2292 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:17-jre-ubi9-minimal` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:27f781e93c2d1d46d5c8e5173c127e2160001eb7e5f62be7abf754d3af28d32c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3602393 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db2ca8c9635b04c3d046cf41807bdca64054364897e9f0b3073e9e1cc62fa253`

```dockerfile
```

-	Layers:
	-	`sha256:6007de16bc0d83c6024a0f306c17185515a11b3a4ad11ecdbbbf00774eb7d5b0`  
		Last Modified: Fri, 14 Feb 2025 04:14:00 GMT  
		Size: 3.6 MB (3581532 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5d825028ef4d57182ea519e00591b16fd6ea7820a536245e6434a7c74603da79`  
		Last Modified: Fri, 14 Feb 2025 04:14:01 GMT  
		Size: 20.9 KB (20861 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-temurin:17-jre-ubi9-minimal` - linux; ppc64le

```console
$ docker pull eclipse-temurin@sha256:7c7f9f7bba61d17e232f82b629b805f794559a4c9d937bf258249fa1dcbedcf7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **130.0 MB (130027739 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:20e54722924b1f9494dddaa6bc989b5f52c1c10f9a7aea634b6976b9022e5f93`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`

```dockerfile
# Thu, 30 Jan 2025 14:32:57 GMT
LABEL maintainer="Red Hat, Inc."
# Thu, 30 Jan 2025 14:32:57 GMT
LABEL vendor="Red Hat, Inc."
# Thu, 30 Jan 2025 14:32:57 GMT
LABEL url="https://www.redhat.com"
# Thu, 30 Jan 2025 14:32:57 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.5"       distribution-scope="public"
# Thu, 30 Jan 2025 14:32:57 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Thu, 30 Jan 2025 14:32:57 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Thu, 30 Jan 2025 14:32:57 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 30 Jan 2025 14:32:57 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 30 Jan 2025 14:32:57 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Thu, 30 Jan 2025 14:32:57 GMT
LABEL io.openshift.expose-services=""
# Thu, 30 Jan 2025 14:32:57 GMT
LABEL io.openshift.tags="minimal rhel9"
# Thu, 30 Jan 2025 14:32:57 GMT
ENV container oci
# Thu, 30 Jan 2025 14:32:57 GMT
COPY dir:2c0c7900d5f6c40d02b1787c7aed15027e6a404d210587076552b87add6a3c87 in / 
# Thu, 30 Jan 2025 14:32:57 GMT
COPY file:b37d593713ee21ad52a4cd1424dc019a24f7966f85df0ac4b86d234302695328 in /etc/yum.repos.d/. 
# Thu, 30 Jan 2025 14:32:57 GMT
CMD ["/bin/bash"]
# Thu, 30 Jan 2025 14:32:57 GMT
RUN . /cachi2/cachi2.env &&     rm -rf /var/log/*
# Thu, 30 Jan 2025 14:32:57 GMT
LABEL "build-date"="2025-02-13T04:27:14" "architecture"="ppc64le" "vcs-type"="git" "vcs-ref"="c0546ad1ce412f8077a547cb8d0d68d04f08815c" "build-date"="2025-02-13T04:15:47Z" "release"="1739420147"
# Thu, 30 Jan 2025 14:32:57 GMT
RUN /bin/sh
# Thu, 30 Jan 2025 14:32:57 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 30 Jan 2025 14:32:57 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 30 Jan 2025 14:32:57 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 30 Jan 2025 14:32:57 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         fontconfig         glibc-langpack-en     ;     microdnf clean all # buildkit
# Thu, 30 Jan 2025 14:32:57 GMT
ENV JAVA_VERSION=jdk-17.0.14+7
# Thu, 30 Jan 2025 14:32:57 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='bab3f352fc7144ac1435924f056872d16f4b32c8bcda58b9a77b636eb1c664f4';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.14_7.tar.gz';          ;;        ppc64le)          ESUM='2a730e9d34cce4d588739b626a034ed68c065a2db61048ee7886be48ec9fe460';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.14_7.tar.gz';          ;;        s390x)          ESUM='3887f14f95a14e65a985cfcee6696e01aadee06d3347ab70eb7d6b16ce397238';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_s390x_linux_hotspot_17.0.14_7.tar.gz';          ;;        x86_64)          ESUM='a4b0015872758aac6a5d17139e952a3951ee536ae6d9a99828823a80a71add56';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_x64_linux_hotspot_17.0.14_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz; # buildkit
# Thu, 30 Jan 2025 14:32:57 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 30 Jan 2025 14:32:57 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 30 Jan 2025 14:32:57 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
```

-	Layers:
	-	`sha256:9e6b2a031935c86976201f383962f66d759b1c458d46f7f8db9cd32663dd945f`  
		Last Modified: Thu, 13 Feb 2025 06:13:41 GMT  
		Size: 43.8 MB (43777674 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f65b64183df0b784e7e5f8c0c986254fe70af80954963d80c5fa6ab3c2e153af`  
		Last Modified: Thu, 13 Feb 2025 06:13:37 GMT  
		Size: 460.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8145a963593a244638406fe09abc4846c151008fbc794c259f3023bea468137`  
		Last Modified: Fri, 14 Feb 2025 00:28:47 GMT  
		Size: 39.5 MB (39470783 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f4f1ee1697542beba937449cff73ec27a9b857d90dd3807725c5af37c9a1924`  
		Last Modified: Fri, 14 Feb 2025 00:45:30 GMT  
		Size: 46.8 MB (46776406 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4978eb1bb2ef1f97a983ad06e452b27ed96aec48a03b7f4d19d7c16ad99151f`  
		Last Modified: Fri, 14 Feb 2025 00:45:28 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40de9f9646d4c62e10c7b18f80a141d8fe97ec73ef48cec6c56a217edb42368f`  
		Last Modified: Fri, 14 Feb 2025 01:26:22 GMT  
		Size: 2.3 KB (2290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:17-jre-ubi9-minimal` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:5b819692022d227eb56a91e2a08918554e6922eefc20cde1910b479bef744799
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3602966 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:95b6f05ad5c480c76ed2b48a53d7614ef4843a70ee038c83472ed50ad653512f`

```dockerfile
```

-	Layers:
	-	`sha256:8d6778ddc6c36b5abbcfaba0972f964cb314a8bf0716dc83840ca07c07d9732a`  
		Last Modified: Fri, 14 Feb 2025 04:14:03 GMT  
		Size: 3.6 MB (3582179 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:19a2a0dc2609e12374f6d4787b0cedfd85317772ca5a4d2bea557462e80e11ca`  
		Last Modified: Fri, 14 Feb 2025 04:14:03 GMT  
		Size: 20.8 KB (20787 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-temurin:17-jre-ubi9-minimal` - linux; s390x

```console
$ docker pull eclipse-temurin@sha256:43d03aea7a15860381998f8a489e6d523265a7ae726d85f7bc3bead238045ef5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **118.5 MB (118458029 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c02d2b311a0ae71b12c5f539ae48e37c760b2f5690dafc0e5eefb76fa432719`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`

```dockerfile
# Thu, 30 Jan 2025 14:32:57 GMT
LABEL maintainer="Red Hat, Inc."
# Thu, 30 Jan 2025 14:32:57 GMT
LABEL vendor="Red Hat, Inc."
# Thu, 30 Jan 2025 14:32:57 GMT
LABEL url="https://www.redhat.com"
# Thu, 30 Jan 2025 14:32:57 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.5"       distribution-scope="public"
# Thu, 30 Jan 2025 14:32:57 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Thu, 30 Jan 2025 14:32:57 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Thu, 30 Jan 2025 14:32:57 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 30 Jan 2025 14:32:57 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 30 Jan 2025 14:32:57 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Thu, 30 Jan 2025 14:32:57 GMT
LABEL io.openshift.expose-services=""
# Thu, 30 Jan 2025 14:32:57 GMT
LABEL io.openshift.tags="minimal rhel9"
# Thu, 30 Jan 2025 14:32:57 GMT
ENV container oci
# Thu, 30 Jan 2025 14:32:57 GMT
COPY dir:86825579d6c6c7e4802643396fb14124acbbf3b24f22947be66f890a734b7e7b in / 
# Thu, 30 Jan 2025 14:32:57 GMT
COPY file:b37d593713ee21ad52a4cd1424dc019a24f7966f85df0ac4b86d234302695328 in /etc/yum.repos.d/. 
# Thu, 30 Jan 2025 14:32:57 GMT
CMD ["/bin/bash"]
# Thu, 30 Jan 2025 14:32:57 GMT
RUN . /cachi2/cachi2.env &&     rm -rf /var/log/*
# Thu, 30 Jan 2025 14:32:57 GMT
LABEL "build-date"="2025-02-06T04:49:32" "architecture"="s390x" "vcs-type"="git" "vcs-ref"="adfffabe9acacc27d15fc0ceb8e083254ca7b450" "build-date"="2025-02-06T04:39:35Z" "release"="1738816775"
# Thu, 30 Jan 2025 14:32:57 GMT
RUN /bin/sh
# Thu, 30 Jan 2025 14:32:57 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 30 Jan 2025 14:32:57 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 30 Jan 2025 14:32:57 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 30 Jan 2025 14:32:57 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         fontconfig         glibc-langpack-en     ;     microdnf clean all # buildkit
# Thu, 30 Jan 2025 14:32:57 GMT
ENV JAVA_VERSION=jdk-17.0.14+7
# Thu, 30 Jan 2025 14:32:57 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='bab3f352fc7144ac1435924f056872d16f4b32c8bcda58b9a77b636eb1c664f4';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.14_7.tar.gz';          ;;        ppc64le)          ESUM='2a730e9d34cce4d588739b626a034ed68c065a2db61048ee7886be48ec9fe460';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.14_7.tar.gz';          ;;        s390x)          ESUM='3887f14f95a14e65a985cfcee6696e01aadee06d3347ab70eb7d6b16ce397238';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_s390x_linux_hotspot_17.0.14_7.tar.gz';          ;;        x86_64)          ESUM='a4b0015872758aac6a5d17139e952a3951ee536ae6d9a99828823a80a71add56';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.14%2B7/OpenJDK17U-jre_x64_linux_hotspot_17.0.14_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz; # buildkit
# Thu, 30 Jan 2025 14:32:57 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 30 Jan 2025 14:32:57 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 30 Jan 2025 14:32:57 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
```

-	Layers:
	-	`sha256:dff3dae8634485c4d1f14243b55a740b473ee901b87cfd847a4234dc5a1b876d`  
		Last Modified: Thu, 06 Feb 2025 07:04:17 GMT  
		Size: 37.5 MB (37509515 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8ba975a618e9922cb358fe027051fa5621498ddb470d175378812c757e5d91c`  
		Last Modified: Thu, 06 Feb 2025 07:04:18 GMT  
		Size: 461.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86a94d5be3d999c406cf4b6c9139018b7dc00cef5387313637ff1e80cd68cb67`  
		Last Modified: Fri, 07 Feb 2025 05:30:50 GMT  
		Size: 37.0 MB (37004700 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a655bcb7492ece3c0ed65a4956b53a0ce16e0965c8507a5578af9d4316424525`  
		Last Modified: Fri, 07 Feb 2025 01:49:52 GMT  
		Size: 43.9 MB (43940934 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61f539fc34593a5dead9cb4a718a8e0206da63050f890cfa3f3beaf38df1ab4c`  
		Last Modified: Fri, 07 Feb 2025 01:49:50 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f515dc5c18017145678308af680e15dff4f8d90fdfc33a24e445864b00dda8af`  
		Last Modified: Fri, 07 Feb 2025 05:30:53 GMT  
		Size: 2.3 KB (2290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:17-jre-ubi9-minimal` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:76538c556ca1ccbb862d563b2b6e24b1b36a47c20d60f2c5c65c66e6a03e155f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3594695 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b51683ab03fde01f6fc7ed702907812cef988072689054aaa8b08625b240d2d`

```dockerfile
```

-	Layers:
	-	`sha256:25cccfeede996edb8ab545e6e08ed4bdb92151cfb0eb4cd0f8ad2b0fc2aaee38`  
		Last Modified: Fri, 07 Feb 2025 05:30:56 GMT  
		Size: 3.6 MB (3573938 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:57e9feda641e201db1aef7223e5a02c37a717358b7097039aff9f6fa77717072`  
		Last Modified: Fri, 14 Feb 2025 04:14:05 GMT  
		Size: 20.8 KB (20757 bytes)  
		MIME: application/vnd.in-toto+json
