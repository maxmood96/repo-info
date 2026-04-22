## `eclipse-temurin:8u482-b08-jdk-ubi10-minimal`

```console
$ docker pull eclipse-temurin@sha256:b5b973baac00e127f76621447292be4738eb348a0e5503e4dfff08818aeb95ce
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `eclipse-temurin:8u482-b08-jdk-ubi10-minimal` - linux; amd64

```console
$ docker pull eclipse-temurin@sha256:3992525002940de57d743d0be207b7545527e32d7e96438a743ceda0df17c107
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.2 MB (127237131 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1aa8f4bd9c42b2e031eca3569af1292fe03205511bb9bf66c0026d79a063bf1f`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`

```dockerfile
# Wed, 22 Apr 2026 05:17:54 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 22 Apr 2026 05:17:54 GMT
LABEL vendor="Red Hat, Inc."
# Wed, 22 Apr 2026 05:17:54 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Wed, 22 Apr 2026 05:17:54 GMT
LABEL com.redhat.component="ubi10-minimal-container"       name="ubi10/ubi-minimal"       version="10.1"       cpe="cpe:/o:redhat:enterprise_linux:10.1"       distribution-scope="public"
# Wed, 22 Apr 2026 05:17:54 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 22 Apr 2026 05:17:54 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 10."
# Wed, 22 Apr 2026 05:17:55 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 22 Apr 2026 05:17:55 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 22 Apr 2026 05:17:55 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 10 Minimal"
# Wed, 22 Apr 2026 05:17:55 GMT
LABEL io.openshift.expose-services=""
# Wed, 22 Apr 2026 05:17:55 GMT
LABEL io.openshift.tags="minimal rhel10"
# Wed, 22 Apr 2026 05:17:55 GMT
ENV container oci
# Wed, 22 Apr 2026 05:17:55 GMT
COPY dir:dff10165caa8c30a8c2673a95ace4a09e747d1c9e656d37fe7e2593a4192cea1 in /      
# Wed, 22 Apr 2026 05:17:55 GMT
COPY file:5de33b5fc08b00635bccf9134a18978dba13e2250aa51838f9969515a3957847 in /etc/yum.repos.d/.      
# Wed, 22 Apr 2026 05:17:55 GMT
CMD ["/bin/bash"]
# Wed, 22 Apr 2026 05:17:55 GMT
COPY file:595171150af68abc798ea385f7988d74b566aa8e84babff137f00b08b2164683 in /usr/share/buildinfo/content-sets.json      
# Wed, 22 Apr 2026 05:17:55 GMT
COPY file:595171150af68abc798ea385f7988d74b566aa8e84babff137f00b08b2164683 in /root/buildinfo/content_manifests/content-sets.json      
# Wed, 22 Apr 2026 05:17:55 GMT
COPY file:1096e68e00ce2e3d16a7fbd65fd0781406fccc42abee623e8fa1f8395c75478b in /usr/share/buildinfo/labels.json      
# Wed, 22 Apr 2026 05:17:56 GMT
COPY file:1096e68e00ce2e3d16a7fbd65fd0781406fccc42abee623e8fa1f8395c75478b in /root/buildinfo/labels.json      
# Wed, 22 Apr 2026 05:17:56 GMT
LABEL "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="8f919d0175e713e927f4fc60c8a4a7f7d7d63a58" "org.opencontainers.image.revision"="8f919d0175e713e927f4fc60c8a4a7f7d7d63a58" "build-date"="2026-04-22T05:17:41Z" "org.opencontainers.image.created"="2026-04-22T05:17:41Z" "release"="1776834797"org.opencontainers.image.revision=8f919d0175e713e927f4fc60c8a4a7f7d7d63a58,org.opencontainers.image.created=2026-04-22T05:17:41Z
# Wed, 22 Apr 2026 18:16:15 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 22 Apr 2026 18:16:15 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 Apr 2026 18:16:15 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 22 Apr 2026 18:16:15 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en         gnupg2     ;     microdnf clean all # buildkit
# Wed, 22 Apr 2026 18:16:15 GMT
ENV JAVA_VERSION=jdk8u482-b08
# Wed, 22 Apr 2026 18:16:20 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='ada72fbf191fb287b4c1e54be372b64c40c27c2ffbfa01f880c92af11f4e7c94';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u482-b08/OpenJDK8U-jdk_aarch64_linux_hotspot_8u482b08.tar.gz';          ;;        ppc64le)          ESUM='e77ba337c3ebb37fbef4961299f13fc4db87996ffd5470bdfb460cfc2ddb6053';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u482-b08/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u482b08.tar.gz';          ;;        x86_64)          ESUM='e74becad56b4cc01f1556a671e578d3788789f5257f9499f6fbed84e63a55ecf';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u482-b08/OpenJDK8U-jdk_x64_linux_hotspot_8u482b08.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip; # buildkit
# Wed, 22 Apr 2026 18:16:21 GMT
RUN set -eux;     echo "Verifying install ...";     echo "javac -version"; javac -version;     echo "java -version"; java -version;     echo "Complete." # buildkit
# Wed, 22 Apr 2026 18:16:21 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 22 Apr 2026 18:16:21 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
```

-	Layers:
	-	`sha256:74bbdc6f81c25b3fa8d6367ec856d92f28db48c1860a008184a1d723c8d399cc`  
		Last Modified: Wed, 22 Apr 2026 06:14:16 GMT  
		Size: 34.6 MB (34590462 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f685e5b87dd061925558e3c45ed769f2548d459f3d91eca60df9d864c51b411`  
		Last Modified: Wed, 22 Apr 2026 18:16:37 GMT  
		Size: 37.5 MB (37473579 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4aa794138a35ec8ece0039c26f618e4a945d36e9578b31c4cbb6303825a87ee4`  
		Last Modified: Wed, 22 Apr 2026 18:16:37 GMT  
		Size: 55.2 MB (55170647 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97ec21b3b159f03c4563728cae885fa4fef4f4c394ef9715052e6f29162c61e9`  
		Last Modified: Wed, 22 Apr 2026 18:16:34 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39804d7ebc48b0bfcf311f4409ae634794c44bb234f5ec0796c5f2d9650dfd0f`  
		Last Modified: Wed, 22 Apr 2026 18:16:36 GMT  
		Size: 2.3 KB (2314 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:8u482-b08-jdk-ubi10-minimal` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:dd661d268f8d560abc590104b576710571d80bdfc2a5d88b81fecc88c59da77b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3930829 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:19adad23533ac3a7879208c15a7cea31e1e80450d669e7ec41f169a160994d47`

```dockerfile
```

-	Layers:
	-	`sha256:253e061c2fbedfd3137ff31a491b65c7f72b472f8cbde12a203303fc25456791`  
		Last Modified: Wed, 22 Apr 2026 18:16:34 GMT  
		Size: 3.9 MB (3910790 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:060407cc3a9500592840a1ebaa6aae2fb5507641fe33f0e90d27a9f2e58dcf4f`  
		Last Modified: Wed, 22 Apr 2026 18:16:35 GMT  
		Size: 20.0 KB (20039 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-temurin:8u482-b08-jdk-ubi10-minimal` - linux; arm64 variant v8

```console
$ docker pull eclipse-temurin@sha256:41b6b12603a6b846ce86382d63bd90e83e24178e0f6a61e92f152529abd5d6b2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.4 MB (124383173 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4bcad7ee84d00a431d84564d6df7bbab30191222744428b34041a0c2d9cd70a8`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`

```dockerfile
# Wed, 22 Apr 2026 05:20:36 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 22 Apr 2026 05:20:36 GMT
LABEL vendor="Red Hat, Inc."
# Wed, 22 Apr 2026 05:20:37 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Wed, 22 Apr 2026 05:20:37 GMT
LABEL com.redhat.component="ubi10-minimal-container"       name="ubi10/ubi-minimal"       version="10.1"       cpe="cpe:/o:redhat:enterprise_linux:10.1"       distribution-scope="public"
# Wed, 22 Apr 2026 05:20:37 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 22 Apr 2026 05:20:37 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 10."
# Wed, 22 Apr 2026 05:20:37 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 22 Apr 2026 05:20:37 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 22 Apr 2026 05:20:37 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 10 Minimal"
# Wed, 22 Apr 2026 05:20:37 GMT
LABEL io.openshift.expose-services=""
# Wed, 22 Apr 2026 05:20:37 GMT
LABEL io.openshift.tags="minimal rhel10"
# Wed, 22 Apr 2026 05:20:37 GMT
ENV container oci
# Wed, 22 Apr 2026 05:20:38 GMT
COPY dir:3a08e309561c3ef0f2f1f503de8f559ee625841311cafaf96b59ce47a8f1ffce in /      
# Wed, 22 Apr 2026 05:20:38 GMT
COPY file:5de33b5fc08b00635bccf9134a18978dba13e2250aa51838f9969515a3957847 in /etc/yum.repos.d/.      
# Wed, 22 Apr 2026 05:20:38 GMT
CMD ["/bin/bash"]
# Wed, 22 Apr 2026 05:20:38 GMT
COPY file:595171150af68abc798ea385f7988d74b566aa8e84babff137f00b08b2164683 in /usr/share/buildinfo/content-sets.json      
# Wed, 22 Apr 2026 05:20:38 GMT
COPY file:595171150af68abc798ea385f7988d74b566aa8e84babff137f00b08b2164683 in /root/buildinfo/content_manifests/content-sets.json      
# Wed, 22 Apr 2026 05:20:38 GMT
COPY file:70c2dda7fafaa9f54a42bab62bbf07c21fa030503d7cbb51eb7b6ef84bbbba51 in /usr/share/buildinfo/labels.json      
# Wed, 22 Apr 2026 05:20:38 GMT
COPY file:70c2dda7fafaa9f54a42bab62bbf07c21fa030503d7cbb51eb7b6ef84bbbba51 in /root/buildinfo/labels.json      
# Wed, 22 Apr 2026 05:20:38 GMT
LABEL "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="8f919d0175e713e927f4fc60c8a4a7f7d7d63a58" "org.opencontainers.image.revision"="8f919d0175e713e927f4fc60c8a4a7f7d7d63a58" "build-date"="2026-04-22T05:20:21Z" "org.opencontainers.image.created"="2026-04-22T05:20:21Z" "release"="1776834797"org.opencontainers.image.revision=8f919d0175e713e927f4fc60c8a4a7f7d7d63a58,org.opencontainers.image.created=2026-04-22T05:20:21Z
# Wed, 22 Apr 2026 18:15:26 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 22 Apr 2026 18:15:26 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 Apr 2026 18:15:26 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 22 Apr 2026 18:15:26 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en         gnupg2     ;     microdnf clean all # buildkit
# Wed, 22 Apr 2026 18:15:26 GMT
ENV JAVA_VERSION=jdk8u482-b08
# Wed, 22 Apr 2026 18:15:30 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='ada72fbf191fb287b4c1e54be372b64c40c27c2ffbfa01f880c92af11f4e7c94';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u482-b08/OpenJDK8U-jdk_aarch64_linux_hotspot_8u482b08.tar.gz';          ;;        ppc64le)          ESUM='e77ba337c3ebb37fbef4961299f13fc4db87996ffd5470bdfb460cfc2ddb6053';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u482-b08/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u482b08.tar.gz';          ;;        x86_64)          ESUM='e74becad56b4cc01f1556a671e578d3788789f5257f9499f6fbed84e63a55ecf';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u482-b08/OpenJDK8U-jdk_x64_linux_hotspot_8u482b08.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip; # buildkit
# Wed, 22 Apr 2026 18:15:30 GMT
RUN set -eux;     echo "Verifying install ...";     echo "javac -version"; javac -version;     echo "java -version"; java -version;     echo "Complete." # buildkit
# Wed, 22 Apr 2026 18:15:30 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 22 Apr 2026 18:15:30 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
```

-	Layers:
	-	`sha256:e8c4c206e9282db63c5bc98a6b172b79a7673404566e305674f0176bf9808f38`  
		Last Modified: Wed, 22 Apr 2026 06:16:01 GMT  
		Size: 32.7 MB (32712089 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5522414fdc285cba72d2cc96b4dbf4de8d46347523c20443e7c1ba23c3636977`  
		Last Modified: Wed, 22 Apr 2026 18:15:46 GMT  
		Size: 37.4 MB (37416584 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d310752ed62fb1fcccb48cf25606d917a881e5818fba2baf5c3fe4b3f6f4e2c4`  
		Last Modified: Wed, 22 Apr 2026 18:15:46 GMT  
		Size: 54.3 MB (54252058 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f165ea6467a534f1b3c172a9ada4d9e0be53eaecbf72988fd517d181e0aa635`  
		Last Modified: Wed, 22 Apr 2026 18:15:43 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1712d930038efd2bd0d43d56447f16aacd61c4ed839a95c4363b9da67e71709`  
		Last Modified: Wed, 22 Apr 2026 18:15:45 GMT  
		Size: 2.3 KB (2315 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:8u482-b08-jdk-ubi10-minimal` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:7f9306d916bc8795b35268326dc479fcd160d849aac75344aa65b915b1c13799
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3931070 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:70c038000650e2d424009328ae1f96bfea8855e7786b87253b0c485b5a970ea6`

```dockerfile
```

-	Layers:
	-	`sha256:d499968eb448ae2f4beef3cd2eaa1e5624bf7f159c28f8e98c7683b6e387d3f1`  
		Last Modified: Wed, 22 Apr 2026 18:15:44 GMT  
		Size: 3.9 MB (3910916 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ad337c0e9134553029e0164494fb26961163ed1895959665a62b427043b52951`  
		Last Modified: Wed, 22 Apr 2026 18:15:43 GMT  
		Size: 20.2 KB (20154 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-temurin:8u482-b08-jdk-ubi10-minimal` - linux; ppc64le

```console
$ docker pull eclipse-temurin@sha256:35dfeec8ce8d312cc8b7cf8c2104adba4f7e73d427be1d8f117913ef7caed4d8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **130.6 MB (130611570 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a7bbd8dcdeabf01731efa9b030361d7b9f4b7bcbc7bf4e5d65b7db9595fd3a04`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`

```dockerfile
# Wed, 22 Apr 2026 05:19:25 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 22 Apr 2026 05:19:25 GMT
LABEL vendor="Red Hat, Inc."
# Wed, 22 Apr 2026 05:19:25 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Wed, 22 Apr 2026 05:19:25 GMT
LABEL com.redhat.component="ubi10-minimal-container"       name="ubi10/ubi-minimal"       version="10.1"       cpe="cpe:/o:redhat:enterprise_linux:10.1"       distribution-scope="public"
# Wed, 22 Apr 2026 05:19:25 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 22 Apr 2026 05:19:25 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 10."
# Wed, 22 Apr 2026 05:19:25 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 22 Apr 2026 05:19:25 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 22 Apr 2026 05:19:25 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 10 Minimal"
# Wed, 22 Apr 2026 05:19:25 GMT
LABEL io.openshift.expose-services=""
# Wed, 22 Apr 2026 05:19:25 GMT
LABEL io.openshift.tags="minimal rhel10"
# Wed, 22 Apr 2026 05:19:25 GMT
ENV container oci
# Wed, 22 Apr 2026 05:19:26 GMT
COPY dir:8ebfd472fb6c3a18db13a69e93e153e014f1bb212fbd41469e95368f33c9855b in /      
# Wed, 22 Apr 2026 05:19:26 GMT
COPY file:5de33b5fc08b00635bccf9134a18978dba13e2250aa51838f9969515a3957847 in /etc/yum.repos.d/.      
# Wed, 22 Apr 2026 05:19:26 GMT
CMD ["/bin/bash"]
# Wed, 22 Apr 2026 05:19:26 GMT
COPY file:595171150af68abc798ea385f7988d74b566aa8e84babff137f00b08b2164683 in /usr/share/buildinfo/content-sets.json      
# Wed, 22 Apr 2026 05:19:26 GMT
COPY file:595171150af68abc798ea385f7988d74b566aa8e84babff137f00b08b2164683 in /root/buildinfo/content_manifests/content-sets.json      
# Wed, 22 Apr 2026 05:19:26 GMT
COPY file:1be71759ffffc91e186254d5919b2addc4c673e22dcd491b1496fe531cd50a49 in /usr/share/buildinfo/labels.json      
# Wed, 22 Apr 2026 05:19:26 GMT
COPY file:1be71759ffffc91e186254d5919b2addc4c673e22dcd491b1496fe531cd50a49 in /root/buildinfo/labels.json      
# Wed, 22 Apr 2026 05:19:27 GMT
LABEL "architecture"="ppc64le" "vcs-type"="git" "vcs-ref"="8f919d0175e713e927f4fc60c8a4a7f7d7d63a58" "org.opencontainers.image.revision"="8f919d0175e713e927f4fc60c8a4a7f7d7d63a58" "build-date"="2026-04-22T05:19:14Z" "org.opencontainers.image.created"="2026-04-22T05:19:14Z" "release"="1776834797"org.opencontainers.image.revision=8f919d0175e713e927f4fc60c8a4a7f7d7d63a58,org.opencontainers.image.created=2026-04-22T05:19:14Z
# Wed, 22 Apr 2026 20:20:47 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 22 Apr 2026 20:20:47 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 Apr 2026 20:20:47 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 22 Apr 2026 20:20:47 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en         gnupg2     ;     microdnf clean all # buildkit
# Wed, 22 Apr 2026 20:20:47 GMT
ENV JAVA_VERSION=jdk8u482-b08
# Wed, 22 Apr 2026 20:20:54 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='ada72fbf191fb287b4c1e54be372b64c40c27c2ffbfa01f880c92af11f4e7c94';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u482-b08/OpenJDK8U-jdk_aarch64_linux_hotspot_8u482b08.tar.gz';          ;;        ppc64le)          ESUM='e77ba337c3ebb37fbef4961299f13fc4db87996ffd5470bdfb460cfc2ddb6053';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u482-b08/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u482b08.tar.gz';          ;;        x86_64)          ESUM='e74becad56b4cc01f1556a671e578d3788789f5257f9499f6fbed84e63a55ecf';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u482-b08/OpenJDK8U-jdk_x64_linux_hotspot_8u482b08.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip; # buildkit
# Wed, 22 Apr 2026 20:20:55 GMT
RUN set -eux;     echo "Verifying install ...";     echo "javac -version"; javac -version;     echo "java -version"; java -version;     echo "Complete." # buildkit
# Wed, 22 Apr 2026 20:20:55 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 22 Apr 2026 20:20:55 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
```

-	Layers:
	-	`sha256:948a2ed1d2b45707813b0dd77e6a53e4f19eb962b9d9bd8172ed211361568ec7`  
		Last Modified: Wed, 22 Apr 2026 06:16:32 GMT  
		Size: 38.7 MB (38732470 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2433584b22c8a5a7b6fce7b912874af7acd3331970ae9ba91fbe6f82ec3637a`  
		Last Modified: Wed, 22 Apr 2026 20:21:23 GMT  
		Size: 39.2 MB (39225692 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfcb66bb807c6aeac824389500c8de0c36ecaff96ffd8a1c15ea524792af3e69`  
		Last Modified: Wed, 22 Apr 2026 20:21:24 GMT  
		Size: 52.7 MB (52650965 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c8d18cf1b0bd498236ddf3ec05602bbe43cc8b2220f00f9956d7174412d3628`  
		Last Modified: Wed, 22 Apr 2026 20:21:20 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc0c64f52b6132cd4aa2a3b9c95a72bd94929aeead759ef364d51834e3d4220a`  
		Last Modified: Wed, 22 Apr 2026 20:21:22 GMT  
		Size: 2.3 KB (2315 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:8u482-b08-jdk-ubi10-minimal` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:b2e91e817fcae1c050aa0c84b9598332088db5483e2a41e157ea4001113871c5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3918292 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:17387d79b38a4887179ef4f98390e425f38948c6aef28fd8367169322112f4ca`

```dockerfile
```

-	Layers:
	-	`sha256:20043b872b32ac026b876c12779b2520b6dae8b020b7ad975023a25f4513817f`  
		Last Modified: Wed, 22 Apr 2026 20:21:21 GMT  
		Size: 3.9 MB (3898217 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0a144b791118934a6ff214354cf80a305e613eaabee92adf78808cc53f5a48ca`  
		Last Modified: Wed, 22 Apr 2026 20:21:20 GMT  
		Size: 20.1 KB (20075 bytes)  
		MIME: application/vnd.in-toto+json
