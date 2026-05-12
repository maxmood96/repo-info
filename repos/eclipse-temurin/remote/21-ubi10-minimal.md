## `eclipse-temurin:21-ubi10-minimal`

```console
$ docker pull eclipse-temurin@sha256:f3b6db5f0e5070a703511cc3976a47dda5df8429ac69c1d6c1801f0f11218c53
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

### `eclipse-temurin:21-ubi10-minimal` - linux; amd64

```console
$ docker pull eclipse-temurin@sha256:6432b76298daeb448c13a0564ed90819ce630b6438416225bd9e1a07f4683a4e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **230.3 MB (230295698 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2ed53849bf201c8598146191107ccfa0403259f7938cd184c72a1c276132e5e3`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 11 May 2026 01:16:15 GMT
LABEL maintainer="Red Hat, Inc."
# Mon, 11 May 2026 01:16:15 GMT
LABEL vendor="Red Hat, Inc."
# Mon, 11 May 2026 01:16:15 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Mon, 11 May 2026 01:16:15 GMT
LABEL com.redhat.component="ubi10-minimal-container"       name="ubi10/ubi-minimal"       version="10.1"       cpe="cpe:/o:redhat:enterprise_linux:10.1"       distribution-scope="public"
# Mon, 11 May 2026 01:16:15 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Mon, 11 May 2026 01:16:15 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 10."
# Mon, 11 May 2026 01:16:15 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 11 May 2026 01:16:15 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 11 May 2026 01:16:15 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 10 Minimal"
# Mon, 11 May 2026 01:16:15 GMT
LABEL io.openshift.expose-services=""
# Mon, 11 May 2026 01:16:15 GMT
LABEL io.openshift.tags="minimal rhel10"
# Mon, 11 May 2026 01:16:15 GMT
ENV container oci
# Mon, 11 May 2026 01:16:15 GMT
COPY dir:944b21b5e56ba1540a32a325c037508b8301ec37c6f3e20f96a07c3b3ab330c2 in /      
# Mon, 11 May 2026 01:16:16 GMT
COPY file:5de33b5fc08b00635bccf9134a18978dba13e2250aa51838f9969515a3957847 in /etc/yum.repos.d/.      
# Mon, 11 May 2026 01:16:16 GMT
CMD ["/bin/bash"]
# Mon, 11 May 2026 01:16:16 GMT
COPY file:595171150af68abc798ea385f7988d74b566aa8e84babff137f00b08b2164683 in /usr/share/buildinfo/content-sets.json      
# Mon, 11 May 2026 01:16:16 GMT
COPY file:595171150af68abc798ea385f7988d74b566aa8e84babff137f00b08b2164683 in /root/buildinfo/content_manifests/content-sets.json      
# Mon, 11 May 2026 01:16:16 GMT
COPY file:2c395ff24a52d293bfab5aa19a14f53b1efe7d5e8864bf90f387296119a55f72 in /usr/share/buildinfo/labels.json      
# Mon, 11 May 2026 01:16:16 GMT
COPY file:2c395ff24a52d293bfab5aa19a14f53b1efe7d5e8864bf90f387296119a55f72 in /root/buildinfo/labels.json      
# Mon, 11 May 2026 01:16:16 GMT
LABEL "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="356ecb8b806b04797740ef169abe27bf41ac3f8c" "org.opencontainers.image.revision"="356ecb8b806b04797740ef169abe27bf41ac3f8c" "build-date"="2026-05-11T01:16:01Z" "org.opencontainers.image.created"="2026-05-11T01:16:01Z" "release"="1778461919"org.opencontainers.image.revision=356ecb8b806b04797740ef169abe27bf41ac3f8c,org.opencontainers.image.created=2026-05-11T01:16:01Z
# Tue, 12 May 2026 00:03:43 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 12 May 2026 00:03:43 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 May 2026 00:03:43 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 12 May 2026 00:03:43 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en         gnupg2     ;     microdnf clean all # buildkit
# Tue, 12 May 2026 00:03:43 GMT
ENV JAVA_VERSION=jdk-21.0.11+10
# Tue, 12 May 2026 00:05:12 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='8d498ec88e1c1989fab95c6784240ab92d011e29c54d20a3f9c324b13476f9ad';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.11%2B10/OpenJDK21U-jdk_aarch64_linux_hotspot_21.0.11_10.tar.gz';          ;;        ppc64le)          ESUM='3d043ae96d2343962bf2307d8c55f19849fbfa4c6be9fe164a77d79263f0d989';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.11%2B10/OpenJDK21U-jdk_ppc64le_linux_hotspot_21.0.11_10.tar.gz';          ;;        s390x)          ESUM='14dbe3cb226e64b945a36bea32686e8deec746504fe3ccee8de585c54af41ffd';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.11%2B10/OpenJDK21U-jdk_s390x_linux_hotspot_21.0.11_10.tar.gz';          ;;        x86_64)          ESUM='4b2220e232a97997b436ca6ab15cbf70171ecff52958a46159dfa5a8c44ca4de';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.11%2B10/OpenJDK21U-jdk_x64_linux_hotspot_21.0.11_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Tue, 12 May 2026 00:05:13 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 12 May 2026 00:05:13 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 12 May 2026 00:05:13 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 12 May 2026 00:05:13 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:288c81655277add7fa3f1d2c80956ecdc30e861ea53ff003f0eb7d1f488bf24b`  
		Last Modified: Mon, 11 May 2026 02:07:21 GMT  
		Size: 34.6 MB (34622430 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:976cadaa04549e76f7b3506abac395ce237f264ba8f7ff972e45593fc6af4ff3`  
		Last Modified: Tue, 12 May 2026 00:04:01 GMT  
		Size: 37.5 MB (37498138 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ecca8cb77647655ceb5833c21c2ddd6efd8c806e067002638cd889500d6dad9`  
		Last Modified: Tue, 12 May 2026 00:05:35 GMT  
		Size: 158.2 MB (158172711 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79c5445fdde0bc7b52cd4d4aedf80392f104596ebcd631289ba8035f36925347`  
		Last Modified: Tue, 12 May 2026 00:05:31 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10ddb6b59eb80f4653eda5427d8a7e3d3248532874836caabba20c2dc1064d22`  
		Last Modified: Tue, 12 May 2026 00:05:30 GMT  
		Size: 2.3 KB (2291 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:21-ubi10-minimal` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:67eb4c730a28eee048ddd6f2eecb3a820ff3fea2e4c2dbeaaf10a48fbe5c9512
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3813670 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7185298fbd7c1387d5d8fa81a1b8695dfb7ddbcca0ea445f672a44b4c13afa40`

```dockerfile
```

-	Layers:
	-	`sha256:96373c0f4154febdfd96aa660e8f2db3b6f22b33d0f88f4c5f0d2799803691a4`  
		Last Modified: Tue, 12 May 2026 00:05:31 GMT  
		Size: 3.8 MB (3792330 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:373105972bc3544f8a0feadc9c32bdf124f47e899c952354af6ec90d381a05a9`  
		Last Modified: Tue, 12 May 2026 00:05:31 GMT  
		Size: 21.3 KB (21340 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-temurin:21-ubi10-minimal` - linux; arm64 variant v8

```console
$ docker pull eclipse-temurin@sha256:6359ffde537d15d08371dcd1f6026d9b89e0a5c0ba8296b73a54b7ce97522731
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **226.7 MB (226658311 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a4bc78098d4ce0eea86f2156304806361b673325b5b92ded367e348879d4bc9f`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 11 May 2026 01:17:49 GMT
LABEL maintainer="Red Hat, Inc."
# Mon, 11 May 2026 01:17:49 GMT
LABEL vendor="Red Hat, Inc."
# Mon, 11 May 2026 01:17:49 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Mon, 11 May 2026 01:17:49 GMT
LABEL com.redhat.component="ubi10-minimal-container"       name="ubi10/ubi-minimal"       version="10.1"       cpe="cpe:/o:redhat:enterprise_linux:10.1"       distribution-scope="public"
# Mon, 11 May 2026 01:17:49 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Mon, 11 May 2026 01:17:49 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 10."
# Mon, 11 May 2026 01:17:49 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 11 May 2026 01:17:49 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 11 May 2026 01:17:49 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 10 Minimal"
# Mon, 11 May 2026 01:17:49 GMT
LABEL io.openshift.expose-services=""
# Mon, 11 May 2026 01:17:49 GMT
LABEL io.openshift.tags="minimal rhel10"
# Mon, 11 May 2026 01:17:49 GMT
ENV container oci
# Mon, 11 May 2026 01:17:50 GMT
COPY dir:c6e5c961b244885bbae5433f1eb0e567eb7e34fa66cb14c7f643fbc5449440ea in /      
# Mon, 11 May 2026 01:17:50 GMT
COPY file:5de33b5fc08b00635bccf9134a18978dba13e2250aa51838f9969515a3957847 in /etc/yum.repos.d/.      
# Mon, 11 May 2026 01:17:50 GMT
CMD ["/bin/bash"]
# Mon, 11 May 2026 01:17:50 GMT
COPY file:595171150af68abc798ea385f7988d74b566aa8e84babff137f00b08b2164683 in /usr/share/buildinfo/content-sets.json      
# Mon, 11 May 2026 01:17:50 GMT
COPY file:595171150af68abc798ea385f7988d74b566aa8e84babff137f00b08b2164683 in /root/buildinfo/content_manifests/content-sets.json      
# Mon, 11 May 2026 01:17:50 GMT
COPY file:10669f015105b6d7eaedf2ab202dda1098c84203dd610f6bad742d23a54f4858 in /usr/share/buildinfo/labels.json      
# Mon, 11 May 2026 01:17:50 GMT
COPY file:10669f015105b6d7eaedf2ab202dda1098c84203dd610f6bad742d23a54f4858 in /root/buildinfo/labels.json      
# Mon, 11 May 2026 01:17:51 GMT
LABEL "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="356ecb8b806b04797740ef169abe27bf41ac3f8c" "org.opencontainers.image.revision"="356ecb8b806b04797740ef169abe27bf41ac3f8c" "build-date"="2026-05-11T01:17:34Z" "org.opencontainers.image.created"="2026-05-11T01:17:34Z" "release"="1778461919"org.opencontainers.image.revision=356ecb8b806b04797740ef169abe27bf41ac3f8c,org.opencontainers.image.created=2026-05-11T01:17:34Z
# Mon, 11 May 2026 23:59:44 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 11 May 2026 23:59:44 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 11 May 2026 23:59:44 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 11 May 2026 23:59:44 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en         gnupg2     ;     microdnf clean all # buildkit
# Mon, 11 May 2026 23:59:44 GMT
ENV JAVA_VERSION=jdk-21.0.11+10
# Tue, 12 May 2026 00:03:08 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='8d498ec88e1c1989fab95c6784240ab92d011e29c54d20a3f9c324b13476f9ad';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.11%2B10/OpenJDK21U-jdk_aarch64_linux_hotspot_21.0.11_10.tar.gz';          ;;        ppc64le)          ESUM='3d043ae96d2343962bf2307d8c55f19849fbfa4c6be9fe164a77d79263f0d989';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.11%2B10/OpenJDK21U-jdk_ppc64le_linux_hotspot_21.0.11_10.tar.gz';          ;;        s390x)          ESUM='14dbe3cb226e64b945a36bea32686e8deec746504fe3ccee8de585c54af41ffd';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.11%2B10/OpenJDK21U-jdk_s390x_linux_hotspot_21.0.11_10.tar.gz';          ;;        x86_64)          ESUM='4b2220e232a97997b436ca6ab15cbf70171ecff52958a46159dfa5a8c44ca4de';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.11%2B10/OpenJDK21U-jdk_x64_linux_hotspot_21.0.11_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Tue, 12 May 2026 00:03:09 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 12 May 2026 00:03:09 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 12 May 2026 00:03:09 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 12 May 2026 00:03:09 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:b0d48ca6ae597735e3215ce3085802fb19010a7e5256d1d09af0257d955c5185`  
		Last Modified: Mon, 11 May 2026 02:10:59 GMT  
		Size: 32.7 MB (32747172 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e535de146c71409c11cf88a63583572bd33e66987e6acf72dee80eb746c5b27`  
		Last Modified: Tue, 12 May 2026 00:00:08 GMT  
		Size: 37.4 MB (37444321 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:392a2686044fee0ada94c1dd4d8eea298773bd5fb944f59b0234e7c1fe5476de`  
		Last Modified: Tue, 12 May 2026 00:03:30 GMT  
		Size: 156.5 MB (156464398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4502211045bd5de7d3de0a3ba84ca695f24b4650aa8d58eb869df366209c9e31`  
		Last Modified: Tue, 12 May 2026 00:03:26 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:942875047dfaa4c900ced58665fac899818215d5f249ab42c855b373919f479d`  
		Last Modified: Tue, 12 May 2026 00:03:25 GMT  
		Size: 2.3 KB (2291 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:21-ubi10-minimal` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:c257c0a8d2fba6673be855c92cc947319363018b1c1e6534957132490f476450
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3813212 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7033a6c3fcc2caad5fda985fac341934633bd10f5af93cb56271b26db9395143`

```dockerfile
```

-	Layers:
	-	`sha256:8837ff22af98892a17e0a7aebd5f120582818e8a6f801c14d24a590d20a0bc29`  
		Last Modified: Tue, 12 May 2026 00:03:27 GMT  
		Size: 3.8 MB (3791756 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:818475aed2d32d8b3fe14e59be799a029c41c96b1e002d3e3d0db740ac93836c`  
		Last Modified: Tue, 12 May 2026 00:03:26 GMT  
		Size: 21.5 KB (21456 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-temurin:21-ubi10-minimal` - linux; ppc64le

```console
$ docker pull eclipse-temurin@sha256:60ae43f7310c0c3eb33edc4dcdc0b0a373a52af5b8e9870f845bd45ee5750672
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **236.4 MB (236359182 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d200bc4588f7cbe429af9ee190b5afa0c97af652eec1a2d486b9407c10766a5`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 11 May 2026 01:17:29 GMT
LABEL maintainer="Red Hat, Inc."
# Mon, 11 May 2026 01:17:29 GMT
LABEL vendor="Red Hat, Inc."
# Mon, 11 May 2026 01:17:29 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Mon, 11 May 2026 01:17:29 GMT
LABEL com.redhat.component="ubi10-minimal-container"       name="ubi10/ubi-minimal"       version="10.1"       cpe="cpe:/o:redhat:enterprise_linux:10.1"       distribution-scope="public"
# Mon, 11 May 2026 01:17:29 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Mon, 11 May 2026 01:17:29 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 10."
# Mon, 11 May 2026 01:17:29 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 11 May 2026 01:17:29 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 11 May 2026 01:17:29 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 10 Minimal"
# Mon, 11 May 2026 01:17:29 GMT
LABEL io.openshift.expose-services=""
# Mon, 11 May 2026 01:17:29 GMT
LABEL io.openshift.tags="minimal rhel10"
# Mon, 11 May 2026 01:17:29 GMT
ENV container oci
# Mon, 11 May 2026 01:17:29 GMT
COPY dir:f86ae0d0c4a87090459f5dd2e52db1242d0bf9305bb73e66dc55f51f70971c00 in /      
# Mon, 11 May 2026 01:17:29 GMT
COPY file:5de33b5fc08b00635bccf9134a18978dba13e2250aa51838f9969515a3957847 in /etc/yum.repos.d/.      
# Mon, 11 May 2026 01:17:29 GMT
CMD ["/bin/bash"]
# Mon, 11 May 2026 01:17:29 GMT
COPY file:595171150af68abc798ea385f7988d74b566aa8e84babff137f00b08b2164683 in /usr/share/buildinfo/content-sets.json      
# Mon, 11 May 2026 01:17:30 GMT
COPY file:595171150af68abc798ea385f7988d74b566aa8e84babff137f00b08b2164683 in /root/buildinfo/content_manifests/content-sets.json      
# Mon, 11 May 2026 01:17:30 GMT
COPY file:3937609775d6da2876c2843dd2634469abf69886b03de03bc99d3e8daa564f9c in /usr/share/buildinfo/labels.json      
# Mon, 11 May 2026 01:17:30 GMT
COPY file:3937609775d6da2876c2843dd2634469abf69886b03de03bc99d3e8daa564f9c in /root/buildinfo/labels.json      
# Mon, 11 May 2026 01:17:30 GMT
LABEL "architecture"="ppc64le" "vcs-type"="git" "vcs-ref"="356ecb8b806b04797740ef169abe27bf41ac3f8c" "org.opencontainers.image.revision"="356ecb8b806b04797740ef169abe27bf41ac3f8c" "build-date"="2026-05-11T01:17:17Z" "org.opencontainers.image.created"="2026-05-11T01:17:17Z" "release"="1778461919"org.opencontainers.image.revision=356ecb8b806b04797740ef169abe27bf41ac3f8c,org.opencontainers.image.created=2026-05-11T01:17:17Z
# Tue, 12 May 2026 00:28:47 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 12 May 2026 00:28:47 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 May 2026 00:28:47 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 12 May 2026 00:28:47 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en         gnupg2     ;     microdnf clean all # buildkit
# Tue, 12 May 2026 00:28:47 GMT
ENV JAVA_VERSION=jdk-21.0.11+10
# Tue, 12 May 2026 00:34:39 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='8d498ec88e1c1989fab95c6784240ab92d011e29c54d20a3f9c324b13476f9ad';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.11%2B10/OpenJDK21U-jdk_aarch64_linux_hotspot_21.0.11_10.tar.gz';          ;;        ppc64le)          ESUM='3d043ae96d2343962bf2307d8c55f19849fbfa4c6be9fe164a77d79263f0d989';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.11%2B10/OpenJDK21U-jdk_ppc64le_linux_hotspot_21.0.11_10.tar.gz';          ;;        s390x)          ESUM='14dbe3cb226e64b945a36bea32686e8deec746504fe3ccee8de585c54af41ffd';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.11%2B10/OpenJDK21U-jdk_s390x_linux_hotspot_21.0.11_10.tar.gz';          ;;        x86_64)          ESUM='4b2220e232a97997b436ca6ab15cbf70171ecff52958a46159dfa5a8c44ca4de';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.11%2B10/OpenJDK21U-jdk_x64_linux_hotspot_21.0.11_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Tue, 12 May 2026 00:34:42 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 12 May 2026 00:34:42 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 12 May 2026 00:34:42 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 12 May 2026 00:34:42 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:dfc37eccb37a052e4fa7be870ee6db7544ef15834a2dfa05156adc7b3f0064f8`  
		Last Modified: Mon, 11 May 2026 06:17:19 GMT  
		Size: 38.8 MB (38752382 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5b57514fb022bd5104b331922465798e8b81622c1daf6f728be81eb5ba7748c`  
		Last Modified: Tue, 12 May 2026 00:29:32 GMT  
		Size: 39.3 MB (39255864 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2bec5d6160fab7bb43cb85e34e2d64c7dbd5c8e547330806bd8ad4e3e6889252`  
		Last Modified: Tue, 12 May 2026 00:35:23 GMT  
		Size: 158.3 MB (158348515 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d45091514043f02932e3635c2785a5d815508abe4aba66163fc278ccb06be31`  
		Last Modified: Tue, 12 May 2026 00:35:18 GMT  
		Size: 130.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa11df45e1848370c0f7481bea86ecdcf04585601b0804c612ebba0528bf7ac4`  
		Last Modified: Tue, 12 May 2026 00:35:19 GMT  
		Size: 2.3 KB (2291 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:21-ubi10-minimal` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:a136ae9e02b334de973696d09d3d64680194ccde553504f740bd6ba906ca862a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3800538 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:423f2147377780633fca9db3be365b17d09e04792b4a1a6d5dfd8ce8083b8313`

```dockerfile
```

-	Layers:
	-	`sha256:a3bd283f58e28fc503d989475e8d755a8bb86138d5be9252b8b0bafe294f4c4b`  
		Last Modified: Tue, 12 May 2026 00:35:19 GMT  
		Size: 3.8 MB (3779162 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:24b8414ad1b2bfd0bbe99f3e547ca6fe9926c00be7ca25ea34fd6d7792845c9d`  
		Last Modified: Tue, 12 May 2026 00:35:19 GMT  
		Size: 21.4 KB (21376 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-temurin:21-ubi10-minimal` - linux; s390x

```console
$ docker pull eclipse-temurin@sha256:6aa5dd34ef96858fd717391a2c091b523ad8552acdf499ae16735f613d6e7333
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **219.7 MB (219723736 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f7003a70a54d2fa5f1021b662d0cc7199c67a5b19ccbce1b0d610ea68074e35a`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 11 May 2026 01:23:16 GMT
LABEL maintainer="Red Hat, Inc."
# Mon, 11 May 2026 01:23:16 GMT
LABEL vendor="Red Hat, Inc."
# Mon, 11 May 2026 01:23:16 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Mon, 11 May 2026 01:23:16 GMT
LABEL com.redhat.component="ubi10-minimal-container"       name="ubi10/ubi-minimal"       version="10.1"       cpe="cpe:/o:redhat:enterprise_linux:10.1"       distribution-scope="public"
# Mon, 11 May 2026 01:23:16 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Mon, 11 May 2026 01:23:16 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 10."
# Mon, 11 May 2026 01:23:16 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 11 May 2026 01:23:16 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 11 May 2026 01:23:16 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 10 Minimal"
# Mon, 11 May 2026 01:23:16 GMT
LABEL io.openshift.expose-services=""
# Mon, 11 May 2026 01:23:16 GMT
LABEL io.openshift.tags="minimal rhel10"
# Mon, 11 May 2026 01:23:16 GMT
ENV container oci
# Mon, 11 May 2026 01:23:17 GMT
COPY dir:0579bc85c05b217dd77b2ce225f64d3cb10f81a6a3726b91387ffbc978d6e453 in /      
# Mon, 11 May 2026 01:23:17 GMT
COPY file:5de33b5fc08b00635bccf9134a18978dba13e2250aa51838f9969515a3957847 in /etc/yum.repos.d/.      
# Mon, 11 May 2026 01:23:17 GMT
CMD ["/bin/bash"]
# Mon, 11 May 2026 01:23:17 GMT
COPY file:595171150af68abc798ea385f7988d74b566aa8e84babff137f00b08b2164683 in /usr/share/buildinfo/content-sets.json      
# Mon, 11 May 2026 01:23:17 GMT
COPY file:595171150af68abc798ea385f7988d74b566aa8e84babff137f00b08b2164683 in /root/buildinfo/content_manifests/content-sets.json      
# Mon, 11 May 2026 01:23:17 GMT
COPY file:81f827a1784652793e747198fea65ce1ad402e9b3c1587adce62db262e60fb88 in /usr/share/buildinfo/labels.json      
# Mon, 11 May 2026 01:23:17 GMT
COPY file:81f827a1784652793e747198fea65ce1ad402e9b3c1587adce62db262e60fb88 in /root/buildinfo/labels.json      
# Mon, 11 May 2026 01:23:17 GMT
LABEL "architecture"="s390x" "vcs-type"="git" "vcs-ref"="356ecb8b806b04797740ef169abe27bf41ac3f8c" "org.opencontainers.image.revision"="356ecb8b806b04797740ef169abe27bf41ac3f8c" "build-date"="2026-05-11T01:22:36Z" "org.opencontainers.image.created"="2026-05-11T01:22:36Z" "release"="1778461919"org.opencontainers.image.revision=356ecb8b806b04797740ef169abe27bf41ac3f8c,org.opencontainers.image.created=2026-05-11T01:22:36Z
# Tue, 12 May 2026 00:00:39 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 12 May 2026 00:00:39 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 May 2026 00:00:39 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 12 May 2026 00:00:39 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en         gnupg2     ;     microdnf clean all # buildkit
# Tue, 12 May 2026 00:00:39 GMT
ENV JAVA_VERSION=jdk-21.0.11+10
# Tue, 12 May 2026 00:02:17 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='8d498ec88e1c1989fab95c6784240ab92d011e29c54d20a3f9c324b13476f9ad';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.11%2B10/OpenJDK21U-jdk_aarch64_linux_hotspot_21.0.11_10.tar.gz';          ;;        ppc64le)          ESUM='3d043ae96d2343962bf2307d8c55f19849fbfa4c6be9fe164a77d79263f0d989';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.11%2B10/OpenJDK21U-jdk_ppc64le_linux_hotspot_21.0.11_10.tar.gz';          ;;        s390x)          ESUM='14dbe3cb226e64b945a36bea32686e8deec746504fe3ccee8de585c54af41ffd';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.11%2B10/OpenJDK21U-jdk_s390x_linux_hotspot_21.0.11_10.tar.gz';          ;;        x86_64)          ESUM='4b2220e232a97997b436ca6ab15cbf70171ecff52958a46159dfa5a8c44ca4de';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.11%2B10/OpenJDK21U-jdk_x64_linux_hotspot_21.0.11_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Tue, 12 May 2026 00:02:18 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 12 May 2026 00:02:18 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 12 May 2026 00:02:18 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 12 May 2026 00:02:18 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:c8191d3132a8f64ba77e2e7e35ea28fba961048b0be562036986e4b4138e5000`  
		Last Modified: Mon, 11 May 2026 06:17:00 GMT  
		Size: 34.4 MB (34447893 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:edbb67b875402a07d4d37d60a9c04f86b7bb89be6c15373d36cf06b6b31221fb`  
		Last Modified: Tue, 12 May 2026 00:01:10 GMT  
		Size: 37.9 MB (37883242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ea07dd9e55bfbb256bff139d80f150c1b431ff522c3d936c17bd43f6d34bb98`  
		Last Modified: Tue, 12 May 2026 00:02:45 GMT  
		Size: 147.4 MB (147390185 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:137708bee83ef122b4d66345511132ba988e6b979ad2de55f506b6c639518083`  
		Last Modified: Tue, 12 May 2026 00:02:42 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8137005b72e476419d64e1aa73ab87e6702b31836bbc8c9ffa452fe14ccec1f6`  
		Last Modified: Tue, 12 May 2026 00:02:36 GMT  
		Size: 2.3 KB (2290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:21-ubi10-minimal` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:f913e9a63b3930053240c810f6c814f933878e50bf26ea7429d67afe125dcfbf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3799260 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:426e0d36eff29c103914e41b1605b5b45e5b24f8706c39498d92434b75464478`

```dockerfile
```

-	Layers:
	-	`sha256:5e0da249bc1fd57e79fd9d2e8d2e4420ce02b3422453f9d1e58fbc0a34687e84`  
		Last Modified: Tue, 12 May 2026 00:02:42 GMT  
		Size: 3.8 MB (3777920 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b66d4a7e1f96fecfb8293af8bbc0546d33e692d5d36eb6c4c07f6fa204a95af6`  
		Last Modified: Tue, 12 May 2026 00:02:42 GMT  
		Size: 21.3 KB (21340 bytes)  
		MIME: application/vnd.in-toto+json
