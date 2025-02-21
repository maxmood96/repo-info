## `eclipse-temurin:8u442-b06-jre-ubi9-minimal`

```console
$ docker pull eclipse-temurin@sha256:e5a629bacf1037700815c45e9c6c7a6d96d5a3500e2da2edf38f64ed5e9d07ea
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `eclipse-temurin:8u442-b06-jre-ubi9-minimal` - linux; amd64

```console
$ docker pull eclipse-temurin@sha256:cf02210eaf4c18f8f68aa09a7ad949a911391cf0785d760de2fc5ffde6ac9ed2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **118.2 MB (118227061 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a195899cbdeb3c8a6baf3eaad3f543e7df9527648171e658d50b86104972486`
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
ENV JAVA_VERSION=jdk8u442-b06
# Thu, 30 Jan 2025 14:32:57 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='730ed649ee973b7408cf7107e90576b67e8ed4b3aebb9e3e8a1056151f373152';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u442-b06/OpenJDK8U-jre_aarch64_linux_hotspot_8u442b06.tar.gz';          ;;        ppc64le)          ESUM='812ebf110f1d1cfc26a135368850064f96689e7918aa6bbac1c8f210fad5752f';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u442-b06/OpenJDK8U-jre_ppc64le_linux_hotspot_8u442b06.tar.gz';          ;;        x86_64)          ESUM='730fe33b1fc1f7da1e325d007b475d25a063850a167b548ea4bf689d4fcd867d';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u442-b06/OpenJDK8U-jre_x64_linux_hotspot_8u442b06.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz; # buildkit
# Thu, 30 Jan 2025 14:32:57 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java -version"; java -version;     echo "Complete." # buildkit
# Thu, 30 Jan 2025 14:32:57 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 30 Jan 2025 14:32:57 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
```

-	Layers:
	-	`sha256:3333307dcd2e4279579646a05a5f99082a61a20906175240445b0e15f73b6d6e`  
		Last Modified: Thu, 13 Feb 2025 05:39:37 GMT  
		Size: 39.4 MB (39366553 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5025173ec0b35686a33458b367c2a6e898c824f57a07925c25d26a0cfb5f2e50`  
		Last Modified: Thu, 13 Feb 2025 05:39:36 GMT  
		Size: 461.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d926f140f4473dd71a27e273cb5d45a9955c4d4f066e213cfa129bec6aff8a7a`  
		Last Modified: Fri, 14 Feb 2025 00:27:49 GMT  
		Size: 37.0 MB (36981355 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91b37119ebbcc4c112b8c5bdfc0fc2e35c5b80417b3162ccd9afdc658d60aeba`  
		Last Modified: Fri, 14 Feb 2025 00:27:50 GMT  
		Size: 41.9 MB (41876274 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:951dcd666b5b5ddd4960c9bcde5ee6d01c59aa3b11a2bb8baf0e1f34270ee73d`  
		Last Modified: Fri, 14 Feb 2025 00:27:49 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:375546e29f3df5053e4b131c287e8c107d0d707d8e2182c3a0651ffddd7ab922`  
		Last Modified: Fri, 14 Feb 2025 00:27:50 GMT  
		Size: 2.3 KB (2291 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:8u442-b06-jre-ubi9-minimal` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:b7fea7be9bf0ebfb3c11de31519e2e5f74f66ab6881e179e319dc3cd3690fcb5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3632376 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1150a88f2029d426d4eeb5a3cde604b6e164d806c498105c1c44c467b10f4842`

```dockerfile
```

-	Layers:
	-	`sha256:be626d6e5f065e7c0ff196bacfcbc7ce03a279d409028a437f5cf445acbc59aa`  
		Last Modified: Fri, 14 Feb 2025 00:27:49 GMT  
		Size: 3.6 MB (3612460 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0e9aaeaaa5ab5d0b5d537e35134281dd7e84fc03099ef9e76a4a64ce9186b873`  
		Last Modified: Fri, 14 Feb 2025 00:27:49 GMT  
		Size: 19.9 KB (19916 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-temurin:8u442-b06-jre-ubi9-minimal` - linux; arm64 variant v8

```console
$ docker pull eclipse-temurin@sha256:180825c2ef461a486d7ff489e4a28bc94f86ea65d86c48e3b7d6393152bfdf6b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.9 MB (115941376 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:73d2f255e397b8ae69e14a795bec3c6b788d616d259c5d34a63836d5a75e7d55`
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
ENV JAVA_VERSION=jdk8u442-b06
# Thu, 30 Jan 2025 14:32:57 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='730ed649ee973b7408cf7107e90576b67e8ed4b3aebb9e3e8a1056151f373152';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u442-b06/OpenJDK8U-jre_aarch64_linux_hotspot_8u442b06.tar.gz';          ;;        ppc64le)          ESUM='812ebf110f1d1cfc26a135368850064f96689e7918aa6bbac1c8f210fad5752f';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u442-b06/OpenJDK8U-jre_ppc64le_linux_hotspot_8u442b06.tar.gz';          ;;        x86_64)          ESUM='730fe33b1fc1f7da1e325d007b475d25a063850a167b548ea4bf689d4fcd867d';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u442-b06/OpenJDK8U-jre_x64_linux_hotspot_8u442b06.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz; # buildkit
# Thu, 30 Jan 2025 14:32:57 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java -version"; java -version;     echo "Complete." # buildkit
# Thu, 30 Jan 2025 14:32:57 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 30 Jan 2025 14:32:57 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
```

-	Layers:
	-	`sha256:56631da24b0de345717238daea2e3e61c768d081572916ae06b08b19126a740d`  
		Last Modified: Thu, 13 Feb 2025 06:13:12 GMT  
		Size: 37.6 MB (37626059 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5aee836c3728069e82153bf7b209c409d3343adaea6ab6b31546e5ce09250db5`  
		Last Modified: Thu, 13 Feb 2025 06:13:10 GMT  
		Size: 460.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d886f1d0418fbd67439d630adb0cd82ab5ccf9bc0d3c039cbd36d622e8eaa96`  
		Last Modified: Fri, 14 Feb 2025 01:07:28 GMT  
		Size: 37.4 MB (37436415 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59e2267a868506538805be1b6a4684143a0655742431127abfa7688321989a2c`  
		Last Modified: Fri, 14 Feb 2025 01:07:56 GMT  
		Size: 40.9 MB (40876022 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8e9f15a1e09defe02c85f08fea8f60ab15b1fe528a9527f1a436678fd07a7e3`  
		Last Modified: Fri, 14 Feb 2025 01:07:55 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:725922f5b251be96770dcbdeadd3335e1849942d3970525efacb8f15b4fd65f0`  
		Last Modified: Fri, 14 Feb 2025 01:07:55 GMT  
		Size: 2.3 KB (2292 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:8u442-b06-jre-ubi9-minimal` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:07233dbcda559ebd5f148db8ad52509b264e95759c0ca0c12a144526140428f6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3632355 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b73e5f3877f9500f34e30b78a6ca02fde7cbdff271a5c8ff5b6e125808e1709d`

```dockerfile
```

-	Layers:
	-	`sha256:d34077778adb36aee182740bfc2a1ebb1104f325c4384ba08b8b8063a2108e4d`  
		Last Modified: Fri, 14 Feb 2025 01:07:55 GMT  
		Size: 3.6 MB (3612333 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:921840a43ce2496fe13f1178d4e2327d0b548102ad59c7a75cfbdf9fe3fde135`  
		Last Modified: Fri, 14 Feb 2025 01:07:55 GMT  
		Size: 20.0 KB (20022 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-temurin:8u442-b06-jre-ubi9-minimal` - linux; ppc64le

```console
$ docker pull eclipse-temurin@sha256:fbec0e4f413758de8163b3e0a8ecfab2f37f70fa96b80b818ad6a1272dd54dd2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.5 MB (124505141 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f87dcb86c8c7da522ea28098ecb0c56eea34c55ef60c1cd3a4884ae48e74b1f`
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
ENV JAVA_VERSION=jdk8u442-b06
# Thu, 30 Jan 2025 14:32:57 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='730ed649ee973b7408cf7107e90576b67e8ed4b3aebb9e3e8a1056151f373152';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u442-b06/OpenJDK8U-jre_aarch64_linux_hotspot_8u442b06.tar.gz';          ;;        ppc64le)          ESUM='812ebf110f1d1cfc26a135368850064f96689e7918aa6bbac1c8f210fad5752f';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u442-b06/OpenJDK8U-jre_ppc64le_linux_hotspot_8u442b06.tar.gz';          ;;        x86_64)          ESUM='730fe33b1fc1f7da1e325d007b475d25a063850a167b548ea4bf689d4fcd867d';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u442-b06/OpenJDK8U-jre_x64_linux_hotspot_8u442b06.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz; # buildkit
# Thu, 30 Jan 2025 14:32:57 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java -version"; java -version;     echo "Complete." # buildkit
# Thu, 30 Jan 2025 14:32:57 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 30 Jan 2025 14:32:57 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
```

-	Layers:
	-	`sha256:9e6b2a031935c86976201f383962f66d759b1c458d46f7f8db9cd32663dd945f`  
		Last Modified: Thu, 13 Feb 2025 06:13:22 GMT  
		Size: 43.8 MB (43777674 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f65b64183df0b784e7e5f8c0c986254fe70af80954963d80c5fa6ab3c2e153af`  
		Last Modified: Thu, 13 Feb 2025 06:13:20 GMT  
		Size: 460.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8145a963593a244638406fe09abc4846c151008fbc794c259f3023bea468137`  
		Last Modified: Fri, 14 Feb 2025 00:28:47 GMT  
		Size: 39.5 MB (39470783 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be092f2943527913f163d67c0413870614853a2f5f1fb65d7c4adc8a9a2077f8`  
		Last Modified: Fri, 14 Feb 2025 00:29:56 GMT  
		Size: 41.3 MB (41253807 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e6e8669e1ae7a82e7728d36eb3b1c11ef041de6ace687d64b6977191047f4bf`  
		Last Modified: Fri, 14 Feb 2025 00:29:54 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:142bf3a418180d3aff5dc017ce1c660b173ac6acd19d9ecbf5d05260da629936`  
		Last Modified: Fri, 14 Feb 2025 00:29:54 GMT  
		Size: 2.3 KB (2291 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:8u442-b06-jre-ubi9-minimal` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:ec9932d167e237f184ed6c6827c2a54b84f06d66c0a50830e0e8bddc3da0ac81
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3632928 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b7ec2a7f9872c0ea963b6cc558d206f156e42aff68e5d24c21d225ca7768ab87`

```dockerfile
```

-	Layers:
	-	`sha256:eb077603127cd004216aa32abf3a10bf7d7f8c231dd933b7228f87ccb3679d4b`  
		Last Modified: Fri, 14 Feb 2025 00:29:55 GMT  
		Size: 3.6 MB (3612980 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:345cb9aa33925d4948879242bb265d99e64e44f7fc713cda7606ca28ecb7e9fb`  
		Last Modified: Fri, 14 Feb 2025 00:29:54 GMT  
		Size: 19.9 KB (19948 bytes)  
		MIME: application/vnd.in-toto+json
