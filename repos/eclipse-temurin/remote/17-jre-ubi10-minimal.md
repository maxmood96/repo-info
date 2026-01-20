## `eclipse-temurin:17-jre-ubi10-minimal`

```console
$ docker pull eclipse-temurin@sha256:ca60ddc50469fecd6726ab376d706c5554fcfa633bbc34c1c4a6eadeb68041d9
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
$ docker pull eclipse-temurin@sha256:e027eeccdc62bfc46d42a20a688a6e2d081b492a142993cdfed6e245b4552914
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **136.9 MB (136913999 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eab92d0081be48c672d6086f26ef83d966eb41c536d090e8b9f0d297dc023162`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`

```dockerfile
# Thu, 18 Dec 2025 04:59:16 GMT
LABEL maintainer="Red Hat, Inc."
# Thu, 18 Dec 2025 04:59:16 GMT
LABEL vendor="Red Hat, Inc."
# Thu, 18 Dec 2025 04:59:16 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Thu, 18 Dec 2025 04:59:16 GMT
LABEL com.redhat.component="ubi10-minimal-container"       name="ubi10/ubi-minimal"       version="10.1"       cpe="cpe:/o:redhat:enterprise_linux:10.1"       distribution-scope="public"
# Thu, 18 Dec 2025 04:59:16 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Thu, 18 Dec 2025 04:59:16 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 10."
# Thu, 18 Dec 2025 04:59:16 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 18 Dec 2025 04:59:16 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 18 Dec 2025 04:59:16 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 10 Minimal"
# Thu, 18 Dec 2025 04:59:16 GMT
LABEL io.openshift.expose-services=""
# Thu, 18 Dec 2025 04:59:16 GMT
LABEL io.openshift.tags="minimal rhel10"
# Thu, 18 Dec 2025 04:59:16 GMT
ENV container oci
# Thu, 18 Dec 2025 04:59:17 GMT
COPY dir:fdc8c39dddd7104eb139c404c8e963d7763f4f2dba800adb3cb1affa751115f3 in /      
# Thu, 18 Dec 2025 04:59:17 GMT
COPY file:5de33b5fc08b00635bccf9134a18978dba13e2250aa51838f9969515a3957847 in /etc/yum.repos.d/.      
# Thu, 18 Dec 2025 04:59:17 GMT
CMD ["/bin/bash"]
# Thu, 18 Dec 2025 04:59:17 GMT
COPY file:595171150af68abc798ea385f7988d74b566aa8e84babff137f00b08b2164683 in /usr/share/buildinfo/content-sets.json      
# Thu, 18 Dec 2025 04:59:17 GMT
COPY file:595171150af68abc798ea385f7988d74b566aa8e84babff137f00b08b2164683 in /root/buildinfo/content_manifests/content-sets.json      
# Thu, 18 Dec 2025 04:59:17 GMT
COPY file:7bed867b68b82c11d96a326acbe92a53eeb4b701a4a63e4b069dab774da39ed9 in /usr/share/buildinfo/labels.json      
# Thu, 18 Dec 2025 04:59:17 GMT
COPY file:7bed867b68b82c11d96a326acbe92a53eeb4b701a4a63e4b069dab774da39ed9 in /root/buildinfo/labels.json      
# Thu, 18 Dec 2025 04:59:17 GMT
LABEL "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="3dbd4aac2bce2ca6b13274bf0662e947c80b18b9" "org.opencontainers.image.revision"="3dbd4aac2bce2ca6b13274bf0662e947c80b18b9" "build-date"="2025-12-18T04:58:54Z" "org.opencontainers.image.created"="2025-12-18T04:58:54Z" "release"="1766033715"org.opencontainers.image.revision=3dbd4aac2bce2ca6b13274bf0662e947c80b18b9,org.opencontainers.image.created=2025-12-18T04:58:54Z
# Thu, 18 Dec 2025 22:23:45 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 18 Dec 2025 22:23:45 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 18 Dec 2025 22:23:45 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 18 Dec 2025 22:23:45 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en         gnupg2     ;     microdnf clean all # buildkit
# Thu, 18 Dec 2025 22:23:45 GMT
ENV JAVA_VERSION=jdk-17.0.17+10
# Thu, 18 Dec 2025 22:23:49 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='d184e8d5caabe51b7ce9d4e0410f51b447a703eab3cec60ca94b7c59fecdad01';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.17_10.tar.gz';          ;;        ppc64le)          ESUM='bc39038e7a874da232f80f49f90f7ec08213fc66b956405f6cc45eed3658cd0a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.17_10.tar.gz';          ;;        s390x)          ESUM='489f8187a939a1e065c2e8f13ff7f26514dd7391b4784ae36e21d9f96972e3f2';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_s390x_linux_hotspot_17.0.17_10.tar.gz';          ;;        x86_64)          ESUM='1c607fb19f153b23a7d62ff980eb55cff1a7d47ce565bbc44d14947c93bd33c9';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_x64_linux_hotspot_17.0.17_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz; # buildkit
# Thu, 18 Dec 2025 22:23:49 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 18 Dec 2025 22:23:49 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 18 Dec 2025 22:23:49 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
```

-	Layers:
	-	`sha256:bbf656ece02bf42bcb72be26aaced8f9084f91250ae2336e1f2b7b9e8b979727`  
		Last Modified: Thu, 18 Dec 2025 11:19:29 GMT  
		Size: 34.5 MB (34531778 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4b4f23dde7a6c718caf4482f654498e08400b18031dc1f76517c82d6cb94dbe`  
		Last Modified: Thu, 18 Dec 2025 22:24:05 GMT  
		Size: 55.3 MB (55325348 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc0804bafee7d75d3a07b13f7b02760d915dd1893f45f881aefd028d907ed5fe`  
		Last Modified: Thu, 18 Dec 2025 22:24:05 GMT  
		Size: 47.1 MB (47054457 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bed17945edbe915b46d6068a079c4237e4668e453afac39c28cbf4d4d5eb859d`  
		Last Modified: Thu, 18 Dec 2025 22:24:09 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29ffa769bcc36b5a36a02bb459705892411d642ba83a40351971e91176063ba1`  
		Last Modified: Thu, 18 Dec 2025 22:24:09 GMT  
		Size: 2.3 KB (2290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:17-jre-ubi10-minimal` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:b474fb6761311a06224b56112df99d565accdd887b8c30b4580bdec4f40cb2c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5616425 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc22d84ac174f43bba4ab5e7c807de54a32dcacf361ffb3f6dc7ddaeb10ab45c`

```dockerfile
```

-	Layers:
	-	`sha256:b3a76efc043e5a47955ef60097bcbc5694361b22ee589746c9aaecbf29600a9d`  
		Last Modified: Thu, 18 Dec 2025 22:24:02 GMT  
		Size: 5.6 MB (5596047 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b43110260cc29cb55c4097aa314034ec5b6ce576a42587bcfada1ad5e04288bb`  
		Last Modified: Thu, 18 Dec 2025 22:24:02 GMT  
		Size: 20.4 KB (20378 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-temurin:17-jre-ubi10-minimal` - linux; arm64 variant v8

```console
$ docker pull eclipse-temurin@sha256:b4ebc0765134875cf792c75c54b3bf7171e02f2e1d017f84799495244470494f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.3 MB (134289184 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:57741918cc6d3fa97fb81a45324a325d324dc96386084eb869e8c82d5e51a77c`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`

```dockerfile
# Thu, 18 Dec 2025 05:04:19 GMT
LABEL maintainer="Red Hat, Inc."
# Thu, 18 Dec 2025 05:04:19 GMT
LABEL vendor="Red Hat, Inc."
# Thu, 18 Dec 2025 05:04:19 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Thu, 18 Dec 2025 05:04:19 GMT
LABEL com.redhat.component="ubi10-minimal-container"       name="ubi10/ubi-minimal"       version="10.1"       cpe="cpe:/o:redhat:enterprise_linux:10.1"       distribution-scope="public"
# Thu, 18 Dec 2025 05:04:19 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Thu, 18 Dec 2025 05:04:19 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 10."
# Thu, 18 Dec 2025 05:04:19 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 18 Dec 2025 05:04:19 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 18 Dec 2025 05:04:19 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 10 Minimal"
# Thu, 18 Dec 2025 05:04:19 GMT
LABEL io.openshift.expose-services=""
# Thu, 18 Dec 2025 05:04:19 GMT
LABEL io.openshift.tags="minimal rhel10"
# Thu, 18 Dec 2025 05:04:19 GMT
ENV container oci
# Thu, 18 Dec 2025 05:04:20 GMT
COPY dir:04b750083472751a7f5154bb88e2ce4d0526c13f7486508dfd32af911f2d6c12 in /      
# Thu, 18 Dec 2025 05:04:20 GMT
COPY file:5de33b5fc08b00635bccf9134a18978dba13e2250aa51838f9969515a3957847 in /etc/yum.repos.d/.      
# Thu, 18 Dec 2025 05:04:20 GMT
CMD ["/bin/bash"]
# Thu, 18 Dec 2025 05:04:20 GMT
COPY file:595171150af68abc798ea385f7988d74b566aa8e84babff137f00b08b2164683 in /usr/share/buildinfo/content-sets.json      
# Thu, 18 Dec 2025 05:04:20 GMT
COPY file:595171150af68abc798ea385f7988d74b566aa8e84babff137f00b08b2164683 in /root/buildinfo/content_manifests/content-sets.json      
# Thu, 18 Dec 2025 05:04:20 GMT
COPY file:3a827beb44c0bded02518913eace1a58024dbf0ce6482c0f23a932e3e59b2536 in /usr/share/buildinfo/labels.json      
# Thu, 18 Dec 2025 05:04:20 GMT
COPY file:3a827beb44c0bded02518913eace1a58024dbf0ce6482c0f23a932e3e59b2536 in /root/buildinfo/labels.json      
# Thu, 18 Dec 2025 05:04:20 GMT
LABEL "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="3dbd4aac2bce2ca6b13274bf0662e947c80b18b9" "org.opencontainers.image.revision"="3dbd4aac2bce2ca6b13274bf0662e947c80b18b9" "build-date"="2025-12-18T05:03:56Z" "org.opencontainers.image.created"="2025-12-18T05:03:56Z" "release"="1766033715"org.opencontainers.image.revision=3dbd4aac2bce2ca6b13274bf0662e947c80b18b9,org.opencontainers.image.created=2025-12-18T05:03:56Z
# Thu, 18 Dec 2025 22:30:43 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 18 Dec 2025 22:30:43 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 18 Dec 2025 22:30:43 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 18 Dec 2025 22:30:43 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en         gnupg2     ;     microdnf clean all # buildkit
# Thu, 18 Dec 2025 22:30:43 GMT
ENV JAVA_VERSION=jdk-17.0.17+10
# Thu, 18 Dec 2025 22:30:47 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='d184e8d5caabe51b7ce9d4e0410f51b447a703eab3cec60ca94b7c59fecdad01';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.17_10.tar.gz';          ;;        ppc64le)          ESUM='bc39038e7a874da232f80f49f90f7ec08213fc66b956405f6cc45eed3658cd0a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.17_10.tar.gz';          ;;        s390x)          ESUM='489f8187a939a1e065c2e8f13ff7f26514dd7391b4784ae36e21d9f96972e3f2';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_s390x_linux_hotspot_17.0.17_10.tar.gz';          ;;        x86_64)          ESUM='1c607fb19f153b23a7d62ff980eb55cff1a7d47ce565bbc44d14947c93bd33c9';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_x64_linux_hotspot_17.0.17_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz; # buildkit
# Thu, 18 Dec 2025 22:30:47 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 18 Dec 2025 22:30:47 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 18 Dec 2025 22:30:47 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
```

-	Layers:
	-	`sha256:f416e7c13e96a1bec342af3e79184aaf45de55dd66939245eb76ca02465c54c7`  
		Last Modified: Thu, 18 Dec 2025 12:14:44 GMT  
		Size: 32.6 MB (32633678 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c30a5d21dc3fcb917d7c66a10da5857e59becea679acadc26259ba2631cff43`  
		Last Modified: Thu, 18 Dec 2025 22:31:24 GMT  
		Size: 55.1 MB (55118566 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dcb4f767be14d03e01e70f47ef0bbbdb02c45a95f80adcf3d17d847a566d30e2`  
		Last Modified: Thu, 18 Dec 2025 22:31:04 GMT  
		Size: 46.5 MB (46534523 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fe83d846651fc02dcbad5fff45c07456029ffeeb1a1b571388459a9769717d7`  
		Last Modified: Thu, 18 Dec 2025 22:31:12 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f6fd4c78f63c9d76baca5d904b5c95c16bb66723ed25960eb455830550f007e`  
		Last Modified: Thu, 18 Dec 2025 22:31:02 GMT  
		Size: 2.3 KB (2290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:17-jre-ubi10-minimal` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:722d3cb633a9f533a58f0225b9723410f67969269d039712dfc76722f535165f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5616007 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:15d1aad4ac253260012ddcdd0fdc9f21c3ea7d7d8dd6349d504a1140405ac157`

```dockerfile
```

-	Layers:
	-	`sha256:8198c7bdd0a266d2b7d13784ff939a5f34b26d8d619b53979cc94b7e8ef20262`  
		Last Modified: Thu, 18 Dec 2025 22:31:02 GMT  
		Size: 5.6 MB (5595525 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:00465717ec0e451f80834e737bfd886bbc0c800a4bd2097e6dde19d08a36c70e`  
		Last Modified: Thu, 18 Dec 2025 22:31:02 GMT  
		Size: 20.5 KB (20482 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-temurin:17-jre-ubi10-minimal` - linux; ppc64le

```console
$ docker pull eclipse-temurin@sha256:b450fc196e0360fadd8242618b79e5f6df7fba607ec9627ae6523e91bb18869c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **142.9 MB (142927195 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:29928f019c5940383d88baf07a41799a48e31ff05366ef7ba7b8ac0c3fb9fc42`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`

```dockerfile
# Thu, 18 Dec 2025 07:03:44 GMT
LABEL maintainer="Red Hat, Inc."
# Thu, 18 Dec 2025 07:03:44 GMT
LABEL vendor="Red Hat, Inc."
# Thu, 18 Dec 2025 07:03:44 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Thu, 18 Dec 2025 07:03:44 GMT
LABEL com.redhat.component="ubi10-minimal-container"       name="ubi10/ubi-minimal"       version="10.1"       cpe="cpe:/o:redhat:enterprise_linux:10.1"       distribution-scope="public"
# Thu, 18 Dec 2025 07:03:44 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Thu, 18 Dec 2025 07:03:44 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 10."
# Thu, 18 Dec 2025 07:03:44 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 18 Dec 2025 07:03:44 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 18 Dec 2025 07:03:44 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 10 Minimal"
# Thu, 18 Dec 2025 07:03:44 GMT
LABEL io.openshift.expose-services=""
# Thu, 18 Dec 2025 07:03:44 GMT
LABEL io.openshift.tags="minimal rhel10"
# Thu, 18 Dec 2025 07:03:44 GMT
ENV container oci
# Thu, 18 Dec 2025 07:03:45 GMT
COPY dir:530980282317924eec1c6623b725ebfc8622f7b70907079d2b485327f826b92a in /      
# Thu, 18 Dec 2025 07:03:45 GMT
COPY file:5de33b5fc08b00635bccf9134a18978dba13e2250aa51838f9969515a3957847 in /etc/yum.repos.d/.      
# Thu, 18 Dec 2025 07:03:45 GMT
CMD ["/bin/bash"]
# Thu, 18 Dec 2025 07:03:45 GMT
COPY file:595171150af68abc798ea385f7988d74b566aa8e84babff137f00b08b2164683 in /usr/share/buildinfo/content-sets.json      
# Thu, 18 Dec 2025 07:03:45 GMT
COPY file:595171150af68abc798ea385f7988d74b566aa8e84babff137f00b08b2164683 in /root/buildinfo/content_manifests/content-sets.json      
# Thu, 18 Dec 2025 07:03:45 GMT
COPY file:c62fb4530a421926bb6d3aa12f09ef125c8c4fff4293e7e931975ad4241f6f26 in /usr/share/buildinfo/labels.json      
# Thu, 18 Dec 2025 07:03:45 GMT
COPY file:c62fb4530a421926bb6d3aa12f09ef125c8c4fff4293e7e931975ad4241f6f26 in /root/buildinfo/labels.json      
# Thu, 18 Dec 2025 07:03:46 GMT
LABEL "architecture"="ppc64le" "vcs-type"="git" "vcs-ref"="3dbd4aac2bce2ca6b13274bf0662e947c80b18b9" "org.opencontainers.image.revision"="3dbd4aac2bce2ca6b13274bf0662e947c80b18b9" "build-date"="2025-12-18T07:03:33Z" "org.opencontainers.image.created"="2025-12-18T07:03:33Z" "release"="1766033715"org.opencontainers.image.revision=3dbd4aac2bce2ca6b13274bf0662e947c80b18b9,org.opencontainers.image.created=2025-12-18T07:03:33Z
# Thu, 18 Dec 2025 22:39:15 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 18 Dec 2025 22:39:15 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 18 Dec 2025 22:39:15 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 18 Dec 2025 22:39:15 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en         gnupg2     ;     microdnf clean all # buildkit
# Thu, 18 Dec 2025 22:39:15 GMT
ENV JAVA_VERSION=jdk-17.0.17+10
# Thu, 18 Dec 2025 22:41:44 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='d184e8d5caabe51b7ce9d4e0410f51b447a703eab3cec60ca94b7c59fecdad01';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.17_10.tar.gz';          ;;        ppc64le)          ESUM='bc39038e7a874da232f80f49f90f7ec08213fc66b956405f6cc45eed3658cd0a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.17_10.tar.gz';          ;;        s390x)          ESUM='489f8187a939a1e065c2e8f13ff7f26514dd7391b4784ae36e21d9f96972e3f2';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_s390x_linux_hotspot_17.0.17_10.tar.gz';          ;;        x86_64)          ESUM='1c607fb19f153b23a7d62ff980eb55cff1a7d47ce565bbc44d14947c93bd33c9';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_x64_linux_hotspot_17.0.17_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz; # buildkit
# Thu, 18 Dec 2025 22:41:45 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 18 Dec 2025 22:41:48 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 18 Dec 2025 22:41:48 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
```

-	Layers:
	-	`sha256:97de3b33554c63d2e40af1481c1da99bde18eb30eff5e4d230d8ec855811f50c`  
		Last Modified: Thu, 18 Dec 2025 12:14:46 GMT  
		Size: 38.7 MB (38688551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4559e7867acf4f05baf702a54db8a3e2cc5bd1a16c2dcecfa940d5c1ad1b6dfd`  
		Last Modified: Thu, 18 Dec 2025 22:40:05 GMT  
		Size: 57.3 MB (57343233 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0325ae4c648b3e23ac6b1b3fe8f60257a83c29fd10c7cb5ba9d859788b863781`  
		Last Modified: Thu, 18 Dec 2025 22:42:38 GMT  
		Size: 46.9 MB (46892992 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2df0412ee8c6ca0bf29970e80dd0b7eff9c864a649037ab37b3eeba0fe106ea`  
		Last Modified: Thu, 18 Dec 2025 22:42:32 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:533d8c649ab06e594ed1c0e5642c49d396df8551ae0d70b91d60de474b31f478`  
		Last Modified: Thu, 18 Dec 2025 22:42:32 GMT  
		Size: 2.3 KB (2291 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:17-jre-ubi10-minimal` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:0f6235770ec63723e8a71a5f63edb836bb7a7aa92a815de0c6b8e633d4446bdf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5605520 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d2e91f54a01f1d7fd4c02b80fbd118bfa002c788184d039852059c084aa27bbc`

```dockerfile
```

-	Layers:
	-	`sha256:21a75aff014aa31422f0b6687a8e742352b7657514fa9c8e34b02ad61fd10dbb`  
		Last Modified: Thu, 18 Dec 2025 22:42:20 GMT  
		Size: 5.6 MB (5585112 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f2f43dbb71b8955720c8788f5113c3a666fdbb7b0957b5466a40433d36dd73c6`  
		Last Modified: Fri, 19 Dec 2025 01:14:20 GMT  
		Size: 20.4 KB (20408 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-temurin:17-jre-ubi10-minimal` - linux; s390x

```console
$ docker pull eclipse-temurin@sha256:83b52c4c852a900a4fd7df74690741d71ab59cdcf40711f8933e81f9e343c479
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.3 MB (134289911 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fda3c311a15521c479b053c9d32688412dc447617552c1b0abf0436569615508`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`

```dockerfile
# Thu, 18 Dec 2025 07:10:02 GMT
LABEL maintainer="Red Hat, Inc."
# Thu, 18 Dec 2025 07:10:02 GMT
LABEL vendor="Red Hat, Inc."
# Thu, 18 Dec 2025 07:10:02 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Thu, 18 Dec 2025 07:10:02 GMT
LABEL com.redhat.component="ubi10-minimal-container"       name="ubi10/ubi-minimal"       version="10.1"       cpe="cpe:/o:redhat:enterprise_linux:10.1"       distribution-scope="public"
# Thu, 18 Dec 2025 07:10:02 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Thu, 18 Dec 2025 07:10:02 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 10."
# Thu, 18 Dec 2025 07:10:02 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 18 Dec 2025 07:10:02 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 18 Dec 2025 07:10:02 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 10 Minimal"
# Thu, 18 Dec 2025 07:10:02 GMT
LABEL io.openshift.expose-services=""
# Thu, 18 Dec 2025 07:10:03 GMT
LABEL io.openshift.tags="minimal rhel10"
# Thu, 18 Dec 2025 07:10:03 GMT
ENV container oci
# Thu, 18 Dec 2025 07:10:03 GMT
COPY dir:7d54469de7c29eaa832f7e98c75ae08842b7fae9314e66ea7e9e482c3966eeca in /      
# Thu, 18 Dec 2025 07:10:03 GMT
COPY file:5de33b5fc08b00635bccf9134a18978dba13e2250aa51838f9969515a3957847 in /etc/yum.repos.d/.      
# Thu, 18 Dec 2025 07:10:03 GMT
CMD ["/bin/bash"]
# Thu, 18 Dec 2025 07:10:03 GMT
COPY file:595171150af68abc798ea385f7988d74b566aa8e84babff137f00b08b2164683 in /usr/share/buildinfo/content-sets.json      
# Thu, 18 Dec 2025 07:10:03 GMT
COPY file:595171150af68abc798ea385f7988d74b566aa8e84babff137f00b08b2164683 in /root/buildinfo/content_manifests/content-sets.json      
# Thu, 18 Dec 2025 07:10:03 GMT
COPY file:bea094e4f4ee0e91f623d002425004416b4556dc8f71bf399fffb85c16bafec5 in /usr/share/buildinfo/labels.json      
# Thu, 18 Dec 2025 07:10:03 GMT
COPY file:bea094e4f4ee0e91f623d002425004416b4556dc8f71bf399fffb85c16bafec5 in /root/buildinfo/labels.json      
# Thu, 18 Dec 2025 07:10:03 GMT
LABEL "architecture"="s390x" "vcs-type"="git" "vcs-ref"="3dbd4aac2bce2ca6b13274bf0662e947c80b18b9" "org.opencontainers.image.revision"="3dbd4aac2bce2ca6b13274bf0662e947c80b18b9" "build-date"="2025-12-18T07:07:43Z" "org.opencontainers.image.created"="2025-12-18T07:07:43Z" "release"="1766033715"org.opencontainers.image.revision=3dbd4aac2bce2ca6b13274bf0662e947c80b18b9,org.opencontainers.image.created=2025-12-18T07:07:43Z
# Thu, 18 Dec 2025 22:41:25 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 18 Dec 2025 22:41:25 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 18 Dec 2025 22:41:25 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 18 Dec 2025 22:41:25 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en         gnupg2     ;     microdnf clean all # buildkit
# Thu, 18 Dec 2025 22:41:25 GMT
ENV JAVA_VERSION=jdk-17.0.17+10
# Thu, 18 Dec 2025 22:41:30 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='d184e8d5caabe51b7ce9d4e0410f51b447a703eab3cec60ca94b7c59fecdad01';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.17_10.tar.gz';          ;;        ppc64le)          ESUM='bc39038e7a874da232f80f49f90f7ec08213fc66b956405f6cc45eed3658cd0a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.17_10.tar.gz';          ;;        s390x)          ESUM='489f8187a939a1e065c2e8f13ff7f26514dd7391b4784ae36e21d9f96972e3f2';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_s390x_linux_hotspot_17.0.17_10.tar.gz';          ;;        x86_64)          ESUM='1c607fb19f153b23a7d62ff980eb55cff1a7d47ce565bbc44d14947c93bd33c9';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_x64_linux_hotspot_17.0.17_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz; # buildkit
# Thu, 18 Dec 2025 22:41:30 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 18 Dec 2025 22:41:30 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 18 Dec 2025 22:41:30 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
```

-	Layers:
	-	`sha256:27a76ad55c4b879c1269027dfeec6783f235d82059544eeb7c62ecb7ad66011a`  
		Last Modified: Thu, 18 Dec 2025 12:14:48 GMT  
		Size: 34.3 MB (34340329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e63f770e95bcd442fbd4b8fd68cccd7a912d2dd01d01bf876299e3b9c4b8eeda`  
		Last Modified: Thu, 18 Dec 2025 22:41:54 GMT  
		Size: 55.9 MB (55921082 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea5d5e0bae947a4573124a2c56e7965c8427270e14f1056607d7e07eb5d9e505`  
		Last Modified: Thu, 18 Dec 2025 22:42:08 GMT  
		Size: 44.0 MB (44026083 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c132439bd45dfd999882bac9694c372ab1d9acd050fa38285c17ab60e5c3d40`  
		Last Modified: Thu, 18 Dec 2025 22:41:52 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:923c45004cea8b456d3b78350c8bd8c4392c6b32104d852332d2861e0a09ff90`  
		Last Modified: Thu, 18 Dec 2025 22:41:57 GMT  
		Size: 2.3 KB (2289 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:17-jre-ubi10-minimal` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:ecbfecaada0298b3d86e34f84048bd81507505bf6e6db612a5df2b22e579163d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5606351 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:42a0c556da1001a1a34929704125064428b594b223af095970b66d14ea7a93b4`

```dockerfile
```

-	Layers:
	-	`sha256:0c8fee9a0a223e8a60ddcc5cbca5d29e4a2084b6910bea8d564a467c5fc1641b`  
		Last Modified: Thu, 18 Dec 2025 22:41:53 GMT  
		Size: 5.6 MB (5585973 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4d9ec787bd790f425318f0f76feeafa07800b8f56acdb1ff2893bbd385234985`  
		Last Modified: Fri, 19 Dec 2025 01:14:28 GMT  
		Size: 20.4 KB (20378 bytes)  
		MIME: application/vnd.in-toto+json
