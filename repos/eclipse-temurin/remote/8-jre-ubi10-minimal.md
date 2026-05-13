## `eclipse-temurin:8-jre-ubi10-minimal`

```console
$ docker pull eclipse-temurin@sha256:d60e2dfb8ba2b7e4cea923875582d133949949386e3e66d5dcf3d24913815f20
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `eclipse-temurin:8-jre-ubi10-minimal` - linux; amd64

```console
$ docker pull eclipse-temurin@sha256:3e26a8bddcd9842939645e4531eb4e3a7b7cafac6ed3f349e31cd5e56b544557
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.5 MB (114460242 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:265c45eaf8838a19ae783d3aecfbb21822685b5c69bc83331d7e6e2580a657c4`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`

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
# Tue, 12 May 2026 23:33:19 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 12 May 2026 23:33:19 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 May 2026 23:33:19 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 12 May 2026 23:33:19 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en         gnupg2     ;     microdnf clean all # buildkit
# Tue, 12 May 2026 23:33:19 GMT
ENV JAVA_VERSION=jdk8u492-b09
# Tue, 12 May 2026 23:33:22 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='d5e50cb002600007dbdfac523605d26196607fa5212db0942ef05cdce9fe2892';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u492-b09/OpenJDK8U-jre_aarch64_linux_hotspot_8u492b09.tar.gz';          ;;        ppc64le)          ESUM='4f724a0fce1117521a3a3e55ebb0281d56f6c9a066092bc3186ee40d8cd955a2';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u492-b09/OpenJDK8U-jre_ppc64le_linux_hotspot_8u492b09.tar.gz';          ;;        x86_64)          ESUM='8eef3d4a837bb7a9e45d30a7579d84d5b76a4321f4376573311e6bf89e48f9b0';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u492-b09/OpenJDK8U-jre_x64_linux_hotspot_8u492b09.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz; # buildkit
# Tue, 12 May 2026 23:33:22 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java -version"; java -version;     echo "Complete." # buildkit
# Tue, 12 May 2026 23:33:23 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 12 May 2026 23:33:23 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
```

-	Layers:
	-	`sha256:20e8bbd1fa594932c31db6c97d64754bd505f260fa2792d4a021081374b77b54`  
		Last Modified: Tue, 12 May 2026 10:16:05 GMT  
		Size: 34.6 MB (34624258 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fcbda714acc20930199eb2668a25fabe8519c59c5535068226974ff2f44e388f`  
		Last Modified: Tue, 12 May 2026 23:33:37 GMT  
		Size: 37.5 MB (37501150 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70487bc61eaa4e79720140405b13f2e018df42c96011a434a7439ee7ad5f80a3`  
		Last Modified: Tue, 12 May 2026 23:33:37 GMT  
		Size: 42.3 MB (42332237 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:906f88f526871b215c833125836e7a6288823a7a8fcae8a487530073304d436a`  
		Last Modified: Tue, 12 May 2026 23:33:35 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ef5afd0ab1c2a4500a34a3f8155c2697e3c1f252ad85905c009f68866cced65`  
		Last Modified: Tue, 12 May 2026 23:33:35 GMT  
		Size: 2.5 KB (2470 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:8-jre-ubi10-minimal` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:67a2a4c2ec1e3c6ac1c256f0d49d5ae98452904e9673d9cfe1067c8620f7d637
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3754360 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c5e8ca3cf009084809149a26373ba02d491f49d42aa4a089832b46b6643f09b`

```dockerfile
```

-	Layers:
	-	`sha256:1c02334906054dd28d1f5cc413952a7cab8aa6ee3528ec0691d111a4f44f1721`  
		Last Modified: Tue, 12 May 2026 23:33:36 GMT  
		Size: 3.7 MB (3734850 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:77a190c10b9c3404da5469aa91e558af757af16defe2e6b413101a75a012fa6d`  
		Last Modified: Tue, 12 May 2026 23:33:35 GMT  
		Size: 19.5 KB (19510 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-temurin:8-jre-ubi10-minimal` - linux; arm64 variant v8

```console
$ docker pull eclipse-temurin@sha256:889159f0b6779de629ed8aa680f21f9f98706e7726e18c1aa460c44234f24714
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **111.5 MB (111459243 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e9ef6c48a2400649875cca7246019ae717f7c7dea99ecde24a15f7fd3ab3f75e`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`

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
# Tue, 12 May 2026 23:32:51 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 12 May 2026 23:32:51 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 May 2026 23:32:51 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 12 May 2026 23:32:51 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en         gnupg2     ;     microdnf clean all # buildkit
# Tue, 12 May 2026 23:32:51 GMT
ENV JAVA_VERSION=jdk8u492-b09
# Tue, 12 May 2026 23:32:54 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='d5e50cb002600007dbdfac523605d26196607fa5212db0942ef05cdce9fe2892';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u492-b09/OpenJDK8U-jre_aarch64_linux_hotspot_8u492b09.tar.gz';          ;;        ppc64le)          ESUM='4f724a0fce1117521a3a3e55ebb0281d56f6c9a066092bc3186ee40d8cd955a2';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u492-b09/OpenJDK8U-jre_ppc64le_linux_hotspot_8u492b09.tar.gz';          ;;        x86_64)          ESUM='8eef3d4a837bb7a9e45d30a7579d84d5b76a4321f4376573311e6bf89e48f9b0';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u492-b09/OpenJDK8U-jre_x64_linux_hotspot_8u492b09.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz; # buildkit
# Tue, 12 May 2026 23:32:54 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java -version"; java -version;     echo "Complete." # buildkit
# Tue, 12 May 2026 23:32:54 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 12 May 2026 23:32:54 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
```

-	Layers:
	-	`sha256:24bccfaffdcba4dab6b032daed65e4f69253b002d2af6f83ce7d6d966c20583a`  
		Last Modified: Tue, 12 May 2026 10:25:24 GMT  
		Size: 32.7 MB (32711659 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7bc25fae89e88744ad1afadaf68f3d6628ed4008d7376269133379e53a9c386`  
		Last Modified: Tue, 12 May 2026 23:33:08 GMT  
		Size: 37.4 MB (37443356 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67ad6607662dba5c6ba29a4ce5cd18a1c9c0dcfb5e2d82daeeda4945c41cf5c6`  
		Last Modified: Tue, 12 May 2026 23:33:08 GMT  
		Size: 41.3 MB (41301632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ddae99603a6ac8d4b6d7398d7e216741e0334648f8ae3294b7117ae0c215d472`  
		Last Modified: Tue, 12 May 2026 23:33:06 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef3ffaf59a03bfb0da7503e16599d9b149fa5ed1790ef01492e19b2671df2617`  
		Last Modified: Tue, 12 May 2026 23:33:06 GMT  
		Size: 2.5 KB (2470 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:8-jre-ubi10-minimal` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:6e6151cf06166c52e4394b1d13818de891c23dea839a695605909df8ce4270c7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3754571 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:068e2c3ee3a68a1fda7bc44a50e725ad248b2049c95e3ab577899016e5e0121d`

```dockerfile
```

-	Layers:
	-	`sha256:6664c4bf6df26e1f5d4fde6f3ab12786428ac758acc65b5ac8629b80130b0a09`  
		Last Modified: Tue, 12 May 2026 23:33:06 GMT  
		Size: 3.7 MB (3734956 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:08bbf0220a86602a2be722873c9f169b1bfc387eebf9fcd1459389bd6391b8ee`  
		Last Modified: Tue, 12 May 2026 23:33:06 GMT  
		Size: 19.6 KB (19615 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-temurin:8-jre-ubi10-minimal` - linux; ppc64le

```console
$ docker pull eclipse-temurin@sha256:cff64dad6a5d6f52365b11ef07fbe973925d329f1c8afca6e48f6f12c903123d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **119.8 MB (119793334 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:52b9d8613e745729667547ab433d227981ff43001ee0190c6b37f6a4ea01c9d2`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`

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
ENV JAVA_VERSION=jdk8u492-b09
# Tue, 12 May 2026 23:32:48 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='d5e50cb002600007dbdfac523605d26196607fa5212db0942ef05cdce9fe2892';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u492-b09/OpenJDK8U-jre_aarch64_linux_hotspot_8u492b09.tar.gz';          ;;        ppc64le)          ESUM='4f724a0fce1117521a3a3e55ebb0281d56f6c9a066092bc3186ee40d8cd955a2';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u492-b09/OpenJDK8U-jre_ppc64le_linux_hotspot_8u492b09.tar.gz';          ;;        x86_64)          ESUM='8eef3d4a837bb7a9e45d30a7579d84d5b76a4321f4376573311e6bf89e48f9b0';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u492-b09/OpenJDK8U-jre_x64_linux_hotspot_8u492b09.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz; # buildkit
# Tue, 12 May 2026 23:32:49 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java -version"; java -version;     echo "Complete." # buildkit
# Tue, 12 May 2026 23:32:49 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 12 May 2026 23:32:49 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
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
	-	`sha256:e29b133eb7a90cf00781cf064ee3e9f3365c42b1b01dce94cd5ec9c392562e5a`  
		Last Modified: Tue, 12 May 2026 23:33:14 GMT  
		Size: 41.7 MB (41740464 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54e8d3a2bd388af3406b45208458d487af27d1bd1183171d3c46a402f23f6508`  
		Last Modified: Tue, 12 May 2026 23:33:02 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90018e0c51821339964de72faae10fafeb9d4e423fcad61f9fa37ebeccdb36cf`  
		Last Modified: Tue, 12 May 2026 23:33:13 GMT  
		Size: 2.5 KB (2471 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:8-jre-ubi10-minimal` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:bbfd3b750e03b71022bd0ac3288b3b2835f31aa9ef1ac76b451b74e4c863c20b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3743827 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eedf437e07f71224c3cd80d064009db11fddd7b23a735309211fc7f9bf8ecdf0`

```dockerfile
```

-	Layers:
	-	`sha256:95f96328002e2fa9dd131bfb3ea9f8257b9334e4b07e60db6a8668aa487e21d6`  
		Last Modified: Tue, 12 May 2026 23:33:13 GMT  
		Size: 3.7 MB (3724287 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:caf98bfe0a8fbc2b0fa25c43da741ace5da6fb4362cbdc69d31ecb42b30404c8`  
		Last Modified: Tue, 12 May 2026 23:33:12 GMT  
		Size: 19.5 KB (19540 bytes)  
		MIME: application/vnd.in-toto+json
