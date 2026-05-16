## `eclipse-temurin:26-ubi10-minimal`

```console
$ docker pull eclipse-temurin@sha256:1ae3f11f72f5f2434b0455fb3ab97c8da738c42c38d205a0c7ef3c391f517a39
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

### `eclipse-temurin:26-ubi10-minimal` - linux; amd64

```console
$ docker pull eclipse-temurin@sha256:8d2e34ee35aa59ddc539bca1662797e7b13e63abb793a0a29557ef813f050db0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **166.7 MB (166653417 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:02e76e4a287140fcecdf7aafe0ab42ffb419cdb5880b6bd2e535dcfac6e9ca19`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 12 May 2026 09:09:41 GMT
LABEL maintainer="Red Hat, Inc."
# Tue, 12 May 2026 09:09:41 GMT
LABEL vendor="Red Hat, Inc."
# Tue, 12 May 2026 09:09:41 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Tue, 12 May 2026 09:09:41 GMT
LABEL com.redhat.component="ubi10-minimal-container"       name="ubi10/ubi-minimal"       version="10.1"       cpe="cpe:/o:redhat:enterprise_linux:10.1"       distribution-scope="public"
# Tue, 12 May 2026 09:09:41 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Tue, 12 May 2026 09:09:41 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 10."
# Tue, 12 May 2026 09:09:41 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Tue, 12 May 2026 09:09:41 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Tue, 12 May 2026 09:09:41 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 10 Minimal"
# Tue, 12 May 2026 09:09:41 GMT
LABEL io.openshift.expose-services=""
# Tue, 12 May 2026 09:09:41 GMT
LABEL io.openshift.tags="minimal rhel10"
# Tue, 12 May 2026 09:09:41 GMT
ENV container oci
# Tue, 12 May 2026 09:09:41 GMT
COPY dir:70c9e4dfd7df3debe1e0457260915a9c0446c87d882b979cfec229a5714bf4c7 in /      
# Tue, 12 May 2026 09:09:41 GMT
COPY file:5de33b5fc08b00635bccf9134a18978dba13e2250aa51838f9969515a3957847 in /etc/yum.repos.d/.      
# Tue, 12 May 2026 09:09:41 GMT
CMD ["/bin/bash"]
# Tue, 12 May 2026 09:09:42 GMT
COPY file:595171150af68abc798ea385f7988d74b566aa8e84babff137f00b08b2164683 in /usr/share/buildinfo/content-sets.json      
# Tue, 12 May 2026 09:09:42 GMT
COPY file:595171150af68abc798ea385f7988d74b566aa8e84babff137f00b08b2164683 in /root/buildinfo/content_manifests/content-sets.json      
# Tue, 12 May 2026 09:09:42 GMT
COPY file:0753abbd85f48d60c6079bc7ee41700b66d3abf1c27ef1da2779ce2ba16ca2c5 in /usr/share/buildinfo/labels.json      
# Tue, 12 May 2026 09:09:42 GMT
COPY file:0753abbd85f48d60c6079bc7ee41700b66d3abf1c27ef1da2779ce2ba16ca2c5 in /root/buildinfo/labels.json      
# Tue, 12 May 2026 09:09:42 GMT
LABEL "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="ad7cdeeb08da8825126b10f488e410b0de5902b0" "org.opencontainers.image.revision"="ad7cdeeb08da8825126b10f488e410b0de5902b0" "build-date"="2026-05-12T09:09:25Z" "org.opencontainers.image.created"="2026-05-12T09:09:25Z" "release"="1778576723"org.opencontainers.image.revision=ad7cdeeb08da8825126b10f488e410b0de5902b0,org.opencontainers.image.created=2026-05-12T09:09:25Z
# Fri, 15 May 2026 20:32:39 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 15 May 2026 20:32:39 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 15 May 2026 20:32:39 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 15 May 2026 20:32:39 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en         gnupg2     ;     microdnf clean all # buildkit
# Fri, 15 May 2026 20:32:39 GMT
ENV JAVA_VERSION=jdk-26.0.1+8
# Fri, 15 May 2026 20:32:45 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='613f9b2861dea937b24d5eca745ef8567733b377d0bb612195acaad0e3f61360';          BINARY_URL='https://github.com/adoptium/temurin26-binaries/releases/download/jdk-26.0.1%2B8/OpenJDK26U-jdk_aarch64_linux_hotspot_26.0.1_8.tar.gz';          ;;        ppc64le)          ESUM='60e016faf4177840430035d948f83f2887d556fe512b78c1d43b320322fe6685';          BINARY_URL='https://github.com/adoptium/temurin26-binaries/releases/download/jdk-26.0.1%2B8/OpenJDK26U-jdk_ppc64le_linux_hotspot_26.0.1_8.tar.gz';          ;;        s390x)          ESUM='942de7ded1427592a2a4b6dbea4083b2d0891de2626c7863e970de3e2819a93f';          BINARY_URL='https://github.com/adoptium/temurin26-binaries/releases/download/jdk-26.0.1%2B8/OpenJDK26U-jdk_s390x_linux_hotspot_26.0.1_8.tar.gz';          ;;        x86_64)          ESUM='8e512f13e575a43655fc92319436c94890c137b9035cc6bd6f9cf24239704d3a';          BINARY_URL='https://github.com/adoptium/temurin26-binaries/releases/download/jdk-26.0.1%2B8/OpenJDK26U-jdk_x64_linux_hotspot_26.0.1_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Fri, 15 May 2026 20:32:47 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Fri, 15 May 2026 20:32:47 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Fri, 15 May 2026 20:32:47 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Fri, 15 May 2026 20:32:47 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:20e8bbd1fa594932c31db6c97d64754bd505f260fa2792d4a021081374b77b54`  
		Last Modified: Tue, 12 May 2026 10:16:05 GMT  
		Size: 34.6 MB (34624258 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28b0da43c370cb097cfa55cddb565df753956c3601acffe750751bdc1721a6e5`  
		Last Modified: Fri, 15 May 2026 20:33:06 GMT  
		Size: 37.5 MB (37501105 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e24e994140f17848b370f3a466b2ffe7e53362fbf45fad60409814440ef5a438`  
		Last Modified: Fri, 15 May 2026 20:33:08 GMT  
		Size: 94.5 MB (94525454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd6a2f4f6c7ce6dcf42d07588053e0ee39066e570b8ca1d3d9e20e5ad8425e81`  
		Last Modified: Fri, 15 May 2026 20:33:05 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b46e56ff64529d974f9eaaa00c21673f7581d6dd331e7f38ddffff07257d4a5`  
		Last Modified: Fri, 15 May 2026 20:33:05 GMT  
		Size: 2.5 KB (2471 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:26-ubi10-minimal` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:11ed9943f2bf592252959857257c82c03b01f8b328c09b8f798c660d540ba83b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3776653 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:340d659e390cbbbc6d87d23144928f79b8ee338e71b03d6de3ba3c99bc2f8724`

```dockerfile
```

-	Layers:
	-	`sha256:5341772a28e41a5df73d56598c1749d20a334c39b8f531999d39f8a40cea42ac`  
		Last Modified: Fri, 15 May 2026 20:33:05 GMT  
		Size: 3.8 MB (3755365 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fd52c7d6c06fd728514d91e67c1ef11c460a011a8983e7dd339e9b6efa8c570d`  
		Last Modified: Fri, 15 May 2026 20:33:05 GMT  
		Size: 21.3 KB (21288 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-temurin:26-ubi10-minimal` - linux; arm64 variant v8

```console
$ docker pull eclipse-temurin@sha256:70d19100803dab8b0c9afdd04ceb65dfb935b459981f0291566ebe651bb16cf4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **163.7 MB (163662849 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7f9d25e1aa041315d18bd828a773c1a88db61816c5c5c3a2952de36a00ada5c6`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 12 May 2026 09:11:34 GMT
LABEL maintainer="Red Hat, Inc."
# Tue, 12 May 2026 09:11:34 GMT
LABEL vendor="Red Hat, Inc."
# Tue, 12 May 2026 09:11:34 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Tue, 12 May 2026 09:11:34 GMT
LABEL com.redhat.component="ubi10-minimal-container"       name="ubi10/ubi-minimal"       version="10.1"       cpe="cpe:/o:redhat:enterprise_linux:10.1"       distribution-scope="public"
# Tue, 12 May 2026 09:11:34 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Tue, 12 May 2026 09:11:34 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 10."
# Tue, 12 May 2026 09:11:34 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Tue, 12 May 2026 09:11:34 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Tue, 12 May 2026 09:11:34 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 10 Minimal"
# Tue, 12 May 2026 09:11:35 GMT
LABEL io.openshift.expose-services=""
# Tue, 12 May 2026 09:11:35 GMT
LABEL io.openshift.tags="minimal rhel10"
# Tue, 12 May 2026 09:11:35 GMT
ENV container oci
# Tue, 12 May 2026 09:11:35 GMT
COPY dir:2877d8ca2be54c031321bcf5c5c002de1e88fc4d881af88566c341114955d981 in /      
# Tue, 12 May 2026 09:11:35 GMT
COPY file:5de33b5fc08b00635bccf9134a18978dba13e2250aa51838f9969515a3957847 in /etc/yum.repos.d/.      
# Tue, 12 May 2026 09:11:35 GMT
CMD ["/bin/bash"]
# Tue, 12 May 2026 09:11:36 GMT
COPY file:595171150af68abc798ea385f7988d74b566aa8e84babff137f00b08b2164683 in /usr/share/buildinfo/content-sets.json      
# Tue, 12 May 2026 09:11:36 GMT
COPY file:595171150af68abc798ea385f7988d74b566aa8e84babff137f00b08b2164683 in /root/buildinfo/content_manifests/content-sets.json      
# Tue, 12 May 2026 09:11:36 GMT
COPY file:ed5db005734a9cf660fffe0f9d4de854f99deb1e83b8a69fd4b48dc74dea4448 in /usr/share/buildinfo/labels.json      
# Tue, 12 May 2026 09:11:36 GMT
COPY file:ed5db005734a9cf660fffe0f9d4de854f99deb1e83b8a69fd4b48dc74dea4448 in /root/buildinfo/labels.json      
# Tue, 12 May 2026 09:11:36 GMT
LABEL "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="ad7cdeeb08da8825126b10f488e410b0de5902b0" "org.opencontainers.image.revision"="ad7cdeeb08da8825126b10f488e410b0de5902b0" "build-date"="2026-05-12T09:11:19Z" "org.opencontainers.image.created"="2026-05-12T09:11:19Z" "release"="1778576723"org.opencontainers.image.revision=ad7cdeeb08da8825126b10f488e410b0de5902b0,org.opencontainers.image.created=2026-05-12T09:11:19Z
# Fri, 15 May 2026 20:32:28 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 15 May 2026 20:32:28 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 15 May 2026 20:32:28 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 15 May 2026 20:32:28 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en         gnupg2     ;     microdnf clean all # buildkit
# Fri, 15 May 2026 20:32:28 GMT
ENV JAVA_VERSION=jdk-26.0.1+8
# Fri, 15 May 2026 20:32:34 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='613f9b2861dea937b24d5eca745ef8567733b377d0bb612195acaad0e3f61360';          BINARY_URL='https://github.com/adoptium/temurin26-binaries/releases/download/jdk-26.0.1%2B8/OpenJDK26U-jdk_aarch64_linux_hotspot_26.0.1_8.tar.gz';          ;;        ppc64le)          ESUM='60e016faf4177840430035d948f83f2887d556fe512b78c1d43b320322fe6685';          BINARY_URL='https://github.com/adoptium/temurin26-binaries/releases/download/jdk-26.0.1%2B8/OpenJDK26U-jdk_ppc64le_linux_hotspot_26.0.1_8.tar.gz';          ;;        s390x)          ESUM='942de7ded1427592a2a4b6dbea4083b2d0891de2626c7863e970de3e2819a93f';          BINARY_URL='https://github.com/adoptium/temurin26-binaries/releases/download/jdk-26.0.1%2B8/OpenJDK26U-jdk_s390x_linux_hotspot_26.0.1_8.tar.gz';          ;;        x86_64)          ESUM='8e512f13e575a43655fc92319436c94890c137b9035cc6bd6f9cf24239704d3a';          BINARY_URL='https://github.com/adoptium/temurin26-binaries/releases/download/jdk-26.0.1%2B8/OpenJDK26U-jdk_x64_linux_hotspot_26.0.1_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Fri, 15 May 2026 20:32:36 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Fri, 15 May 2026 20:32:36 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Fri, 15 May 2026 20:32:36 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Fri, 15 May 2026 20:32:36 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:24bccfaffdcba4dab6b032daed65e4f69253b002d2af6f83ce7d6d966c20583a`  
		Last Modified: Tue, 12 May 2026 10:25:24 GMT  
		Size: 32.7 MB (32711659 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26f46f113310840da4d985371ee53707fdb8ccb269806fd5fc46ad910f3d3b9f`  
		Last Modified: Fri, 15 May 2026 20:32:55 GMT  
		Size: 37.4 MB (37443276 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0cfb4893ec8686de0f1f678fbf792d61662b4f1372945832e0c09169e9ab40e`  
		Last Modified: Fri, 15 May 2026 20:32:56 GMT  
		Size: 93.5 MB (93505313 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11a6a0c0a1026dc89182d600f722dc74ea42237fa0b60ad8a24b4a4e84c1e9d5`  
		Last Modified: Fri, 15 May 2026 20:32:53 GMT  
		Size: 130.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69d566f01039cb0f8c29664ef48f083f5df6fafbc63846a9d3904e3167893453`  
		Last Modified: Fri, 15 May 2026 20:32:53 GMT  
		Size: 2.5 KB (2471 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:26-ubi10-minimal` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:55bccf3080f536d4b0b0874556214052b3bffe64c74d2f45d55ff7a60093d47f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3776192 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e7cdf71f945a65e5728e70a0536af9bb4b36bd4eefd10f1b08b18ece9cc62fa`

```dockerfile
```

-	Layers:
	-	`sha256:5ddbff5b93609bd41b62286fed6b116b32d3cbdb9719b3b9693bf52dfa44f2ad`  
		Last Modified: Fri, 15 May 2026 20:32:53 GMT  
		Size: 3.8 MB (3754788 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a6b2b48e6ded30169b0e1cf21f78236d4a640900f698198674076ea6aa8c2702`  
		Last Modified: Fri, 15 May 2026 20:32:53 GMT  
		Size: 21.4 KB (21404 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-temurin:26-ubi10-minimal` - linux; ppc64le

```console
$ docker pull eclipse-temurin@sha256:9d86135551eec8b2c6eab4006af1f5a8828375dde264ebe1f8bb582bf195a4a1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **172.0 MB (171955268 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:540c27f9fcf29a6aeb29ffae56e5320cf1d3fb744f6aff905f5d30f8e84e39b4`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 12 May 2026 09:13:30 GMT
LABEL maintainer="Red Hat, Inc."
# Tue, 12 May 2026 09:13:30 GMT
LABEL vendor="Red Hat, Inc."
# Tue, 12 May 2026 09:13:30 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Tue, 12 May 2026 09:13:30 GMT
LABEL com.redhat.component="ubi10-minimal-container"       name="ubi10/ubi-minimal"       version="10.1"       cpe="cpe:/o:redhat:enterprise_linux:10.1"       distribution-scope="public"
# Tue, 12 May 2026 09:13:30 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Tue, 12 May 2026 09:13:30 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 10."
# Tue, 12 May 2026 09:13:30 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Tue, 12 May 2026 09:13:30 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Tue, 12 May 2026 09:13:30 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 10 Minimal"
# Tue, 12 May 2026 09:13:31 GMT
LABEL io.openshift.expose-services=""
# Tue, 12 May 2026 09:13:31 GMT
LABEL io.openshift.tags="minimal rhel10"
# Tue, 12 May 2026 09:13:31 GMT
ENV container oci
# Tue, 12 May 2026 09:13:32 GMT
COPY dir:584fbc93c21a7184a941a4142a12f835dcfca07a9a2dfc5bd8298fc624407c1a in /      
# Tue, 12 May 2026 09:13:32 GMT
COPY file:5de33b5fc08b00635bccf9134a18978dba13e2250aa51838f9969515a3957847 in /etc/yum.repos.d/.      
# Tue, 12 May 2026 09:13:32 GMT
CMD ["/bin/bash"]
# Tue, 12 May 2026 09:13:32 GMT
COPY file:595171150af68abc798ea385f7988d74b566aa8e84babff137f00b08b2164683 in /usr/share/buildinfo/content-sets.json      
# Tue, 12 May 2026 09:13:32 GMT
COPY file:595171150af68abc798ea385f7988d74b566aa8e84babff137f00b08b2164683 in /root/buildinfo/content_manifests/content-sets.json      
# Tue, 12 May 2026 09:13:33 GMT
COPY file:101e1b19e6d0f9785c2d23ecc61947a5882edebf262baa5a4ebcee0c3b40e8a2 in /usr/share/buildinfo/labels.json      
# Tue, 12 May 2026 09:13:33 GMT
COPY file:101e1b19e6d0f9785c2d23ecc61947a5882edebf262baa5a4ebcee0c3b40e8a2 in /root/buildinfo/labels.json      
# Tue, 12 May 2026 09:13:33 GMT
LABEL "architecture"="ppc64le" "vcs-type"="git" "vcs-ref"="ad7cdeeb08da8825126b10f488e410b0de5902b0" "org.opencontainers.image.revision"="ad7cdeeb08da8825126b10f488e410b0de5902b0" "build-date"="2026-05-12T09:13:14Z" "org.opencontainers.image.created"="2026-05-12T09:13:14Z" "release"="1778576723"org.opencontainers.image.revision=ad7cdeeb08da8825126b10f488e410b0de5902b0,org.opencontainers.image.created=2026-05-12T09:13:14Z
# Tue, 12 May 2026 23:31:50 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 12 May 2026 23:31:50 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 May 2026 23:31:50 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 12 May 2026 23:31:50 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en         gnupg2     ;     microdnf clean all # buildkit
# Tue, 12 May 2026 23:31:50 GMT
ENV JAVA_VERSION=jdk-26.0.1+8
# Fri, 15 May 2026 20:38:31 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='613f9b2861dea937b24d5eca745ef8567733b377d0bb612195acaad0e3f61360';          BINARY_URL='https://github.com/adoptium/temurin26-binaries/releases/download/jdk-26.0.1%2B8/OpenJDK26U-jdk_aarch64_linux_hotspot_26.0.1_8.tar.gz';          ;;        ppc64le)          ESUM='60e016faf4177840430035d948f83f2887d556fe512b78c1d43b320322fe6685';          BINARY_URL='https://github.com/adoptium/temurin26-binaries/releases/download/jdk-26.0.1%2B8/OpenJDK26U-jdk_ppc64le_linux_hotspot_26.0.1_8.tar.gz';          ;;        s390x)          ESUM='942de7ded1427592a2a4b6dbea4083b2d0891de2626c7863e970de3e2819a93f';          BINARY_URL='https://github.com/adoptium/temurin26-binaries/releases/download/jdk-26.0.1%2B8/OpenJDK26U-jdk_s390x_linux_hotspot_26.0.1_8.tar.gz';          ;;        x86_64)          ESUM='8e512f13e575a43655fc92319436c94890c137b9035cc6bd6f9cf24239704d3a';          BINARY_URL='https://github.com/adoptium/temurin26-binaries/releases/download/jdk-26.0.1%2B8/OpenJDK26U-jdk_x64_linux_hotspot_26.0.1_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Fri, 15 May 2026 20:38:35 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Fri, 15 May 2026 20:38:35 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Fri, 15 May 2026 20:38:35 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Fri, 15 May 2026 20:38:35 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:f815e851aa9d271f09d3448e8acc95ebed62472057c9b0368d01b242d1468875`  
		Last Modified: Tue, 12 May 2026 12:16:14 GMT  
		Size: 38.8 MB (38794493 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d1fdf741746dd4482bfc42d70a6f2954201df0346c653d262b3e220a6a63447`  
		Last Modified: Tue, 12 May 2026 23:32:30 GMT  
		Size: 39.3 MB (39255778 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6e65321d2d4bc756ae4aa79534a08a84af5677368435b9b674ce7a563a19e6e`  
		Last Modified: Fri, 15 May 2026 20:39:09 GMT  
		Size: 93.9 MB (93902398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:734a9b50d7fb1d8fe742949ee2054e4289d456a00614bc200873de77d4c7d754`  
		Last Modified: Fri, 15 May 2026 20:39:07 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c0165a83f801000b2ec396e64d8d9eddfa7074b03bb1da7ae486ad90853e35d`  
		Last Modified: Fri, 15 May 2026 20:39:07 GMT  
		Size: 2.5 KB (2470 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:26-ubi10-minimal` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:4ccdb7d62a9c380cebd27a15b2e41a7a39487c59655ea2a311581d50849d5a2a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3747458 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:675fd3f9ebdb06b0da47e22fb46ffb248941bf7b5e66804b3ce4144afc00ebc0`

```dockerfile
```

-	Layers:
	-	`sha256:9161ecb41fb2ffa2efde5fd6ec88622d0e29e9d3c687912418e92daf4061ae9e`  
		Last Modified: Fri, 15 May 2026 20:39:07 GMT  
		Size: 3.7 MB (3726133 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8027b2525a41525c6e2eda4145ccbc6409f6d8a6c59b902d8bbc4a1d4d4e9bab`  
		Last Modified: Fri, 15 May 2026 20:39:07 GMT  
		Size: 21.3 KB (21325 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-temurin:26-ubi10-minimal` - linux; s390x

```console
$ docker pull eclipse-temurin@sha256:b1dfe82d7351e26a7b2380f1fd92958f17c9ab26bdce6087b574a73011d8db9d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **162.9 MB (162869998 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ddecd9f62b3320c3c618603e53635ce3d752be0a2d8b40079c1c6bc2c12a738`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 12 May 2026 09:27:49 GMT
LABEL maintainer="Red Hat, Inc."
# Tue, 12 May 2026 09:27:49 GMT
LABEL vendor="Red Hat, Inc."
# Tue, 12 May 2026 09:27:49 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Tue, 12 May 2026 09:27:49 GMT
LABEL com.redhat.component="ubi10-minimal-container"       name="ubi10/ubi-minimal"       version="10.1"       cpe="cpe:/o:redhat:enterprise_linux:10.1"       distribution-scope="public"
# Tue, 12 May 2026 09:27:49 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Tue, 12 May 2026 09:27:49 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 10."
# Tue, 12 May 2026 09:27:49 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Tue, 12 May 2026 09:27:49 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Tue, 12 May 2026 09:27:49 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 10 Minimal"
# Tue, 12 May 2026 09:27:49 GMT
LABEL io.openshift.expose-services=""
# Tue, 12 May 2026 09:27:49 GMT
LABEL io.openshift.tags="minimal rhel10"
# Tue, 12 May 2026 09:27:49 GMT
ENV container oci
# Tue, 12 May 2026 09:27:49 GMT
COPY dir:ad73fd8372aea6e68c9b3ea90e4901b979a82fb0f4a43074fa7ea61354ab30b9 in /      
# Tue, 12 May 2026 09:27:49 GMT
COPY file:5de33b5fc08b00635bccf9134a18978dba13e2250aa51838f9969515a3957847 in /etc/yum.repos.d/.      
# Tue, 12 May 2026 09:27:49 GMT
CMD ["/bin/bash"]
# Tue, 12 May 2026 09:27:49 GMT
COPY file:595171150af68abc798ea385f7988d74b566aa8e84babff137f00b08b2164683 in /usr/share/buildinfo/content-sets.json      
# Tue, 12 May 2026 09:27:50 GMT
COPY file:595171150af68abc798ea385f7988d74b566aa8e84babff137f00b08b2164683 in /root/buildinfo/content_manifests/content-sets.json      
# Tue, 12 May 2026 09:27:50 GMT
COPY file:f69727366f08991ceef4955068ba3462c331e0d11189e73f45fe959e3f50f354 in /usr/share/buildinfo/labels.json      
# Tue, 12 May 2026 09:27:50 GMT
COPY file:f69727366f08991ceef4955068ba3462c331e0d11189e73f45fe959e3f50f354 in /root/buildinfo/labels.json      
# Tue, 12 May 2026 09:27:50 GMT
LABEL "architecture"="s390x" "vcs-type"="git" "vcs-ref"="ad7cdeeb08da8825126b10f488e410b0de5902b0" "org.opencontainers.image.revision"="ad7cdeeb08da8825126b10f488e410b0de5902b0" "build-date"="2026-05-12T09:27:06Z" "org.opencontainers.image.created"="2026-05-12T09:27:06Z" "release"="1778576723"org.opencontainers.image.revision=ad7cdeeb08da8825126b10f488e410b0de5902b0,org.opencontainers.image.created=2026-05-12T09:27:06Z
# Tue, 12 May 2026 23:33:20 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 12 May 2026 23:33:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 May 2026 23:33:20 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 12 May 2026 23:33:20 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en         gnupg2     ;     microdnf clean all # buildkit
# Tue, 12 May 2026 23:33:20 GMT
ENV JAVA_VERSION=jdk-26.0.1+8
# Fri, 15 May 2026 20:39:39 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='613f9b2861dea937b24d5eca745ef8567733b377d0bb612195acaad0e3f61360';          BINARY_URL='https://github.com/adoptium/temurin26-binaries/releases/download/jdk-26.0.1%2B8/OpenJDK26U-jdk_aarch64_linux_hotspot_26.0.1_8.tar.gz';          ;;        ppc64le)          ESUM='60e016faf4177840430035d948f83f2887d556fe512b78c1d43b320322fe6685';          BINARY_URL='https://github.com/adoptium/temurin26-binaries/releases/download/jdk-26.0.1%2B8/OpenJDK26U-jdk_ppc64le_linux_hotspot_26.0.1_8.tar.gz';          ;;        s390x)          ESUM='942de7ded1427592a2a4b6dbea4083b2d0891de2626c7863e970de3e2819a93f';          BINARY_URL='https://github.com/adoptium/temurin26-binaries/releases/download/jdk-26.0.1%2B8/OpenJDK26U-jdk_s390x_linux_hotspot_26.0.1_8.tar.gz';          ;;        x86_64)          ESUM='8e512f13e575a43655fc92319436c94890c137b9035cc6bd6f9cf24239704d3a';          BINARY_URL='https://github.com/adoptium/temurin26-binaries/releases/download/jdk-26.0.1%2B8/OpenJDK26U-jdk_x64_linux_hotspot_26.0.1_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Fri, 15 May 2026 20:39:43 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Fri, 15 May 2026 20:39:44 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Fri, 15 May 2026 20:39:44 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Fri, 15 May 2026 20:39:44 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:716b8ccfad2ab26e031483f83283392459a7160cf7d641599a620a485af51f10`  
		Last Modified: Tue, 12 May 2026 12:16:04 GMT  
		Size: 34.5 MB (34450081 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7dec299a1602bf5e0d62202cf77938cca794fdd9ba9bbc56e355abbc7a6a990b`  
		Last Modified: Tue, 12 May 2026 23:33:57 GMT  
		Size: 37.9 MB (37879929 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b73299f4912e862fa2a2cf214ac34578f7ae82f37eb12e612bca48338e9235c`  
		Last Modified: Fri, 15 May 2026 20:41:19 GMT  
		Size: 90.5 MB (90537390 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24141a7d9bdc4d9e494e608278494255fc2c1e5d691b09c5a23f6544525c6b4d`  
		Last Modified: Fri, 15 May 2026 20:41:16 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ac7eb468d8ab4686e91fefc1940b41173f2cb9ac0ecb75fe381480021ed882e`  
		Last Modified: Fri, 15 May 2026 20:41:16 GMT  
		Size: 2.5 KB (2470 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:26-ubi10-minimal` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:f3c6cb523a679dc252ec9581b1e9873f14517d57c4be49641937d3e06a5ab020
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3747430 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e19e092cb72ea1a6b6853313c411dbf3a5373f16323c0bf0d1c7c6e3b5b67079`

```dockerfile
```

-	Layers:
	-	`sha256:df0484213afb73bb5f74e7cb4cd207b58dcea8c8ef7a5ef6c907b99c05653872`  
		Last Modified: Fri, 15 May 2026 20:41:16 GMT  
		Size: 3.7 MB (3726141 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:318877b26982c17c88654d1408ea370d165948df66929b5fd23643c7c01c6cfe`  
		Last Modified: Fri, 15 May 2026 20:41:16 GMT  
		Size: 21.3 KB (21289 bytes)  
		MIME: application/vnd.in-toto+json
