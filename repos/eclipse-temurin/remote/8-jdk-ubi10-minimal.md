## `eclipse-temurin:8-jdk-ubi10-minimal`

```console
$ docker pull eclipse-temurin@sha256:1668b0d8e4929f6175a03e6f8a9afc9993ddc96d2260abe3b4b6d33aa15675f4
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `eclipse-temurin:8-jdk-ubi10-minimal` - linux; amd64

```console
$ docker pull eclipse-temurin@sha256:e1e84db7d27add1b22e1cc3ff35ac67aef5f8bf857a6ad4d1f1c1ce6ba782fab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.2 MB (127236870 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b2451358fd0a67f7d5005ddb69c90d9a49f0b7bc29f1b222f253f5308e02796`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`

```dockerfile
# Thu, 26 Mar 2026 17:20:47 GMT
LABEL maintainer="Red Hat, Inc."
# Thu, 26 Mar 2026 17:20:47 GMT
LABEL vendor="Red Hat, Inc."
# Thu, 26 Mar 2026 17:20:47 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Thu, 26 Mar 2026 17:20:47 GMT
LABEL com.redhat.component="ubi10-minimal-container"       name="ubi10/ubi-minimal"       version="10.1"       cpe="cpe:/o:redhat:enterprise_linux:10.1"       distribution-scope="public"
# Thu, 26 Mar 2026 17:20:47 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Thu, 26 Mar 2026 17:20:48 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 10."
# Thu, 26 Mar 2026 17:20:48 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 26 Mar 2026 17:20:48 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 26 Mar 2026 17:20:48 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 10 Minimal"
# Thu, 26 Mar 2026 17:20:48 GMT
LABEL io.openshift.expose-services=""
# Thu, 26 Mar 2026 17:20:48 GMT
LABEL io.openshift.tags="minimal rhel10"
# Thu, 26 Mar 2026 17:20:48 GMT
ENV container oci
# Thu, 26 Mar 2026 17:20:48 GMT
COPY dir:013378efc21240669710b39853c72e001fd6ffb5e0383845178fe8e7ffe47e8f in /      
# Thu, 26 Mar 2026 17:20:48 GMT
COPY file:5de33b5fc08b00635bccf9134a18978dba13e2250aa51838f9969515a3957847 in /etc/yum.repos.d/.      
# Thu, 26 Mar 2026 17:20:48 GMT
CMD ["/bin/bash"]
# Thu, 26 Mar 2026 17:20:48 GMT
COPY file:595171150af68abc798ea385f7988d74b566aa8e84babff137f00b08b2164683 in /usr/share/buildinfo/content-sets.json      
# Thu, 26 Mar 2026 17:20:48 GMT
COPY file:595171150af68abc798ea385f7988d74b566aa8e84babff137f00b08b2164683 in /root/buildinfo/content_manifests/content-sets.json      
# Thu, 26 Mar 2026 17:20:49 GMT
COPY file:f920fc5dc4d46ff47508071b2b2abe21bc425c8efd4d327551b88c78a46db925 in /usr/share/buildinfo/labels.json      
# Thu, 26 Mar 2026 17:20:49 GMT
COPY file:f920fc5dc4d46ff47508071b2b2abe21bc425c8efd4d327551b88c78a46db925 in /root/buildinfo/labels.json      
# Thu, 26 Mar 2026 17:20:49 GMT
LABEL "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="4d17df4ea3ff25815cca2550bc445280420af0a9" "org.opencontainers.image.revision"="4d17df4ea3ff25815cca2550bc445280420af0a9" "build-date"="2026-03-26T17:20:31Z" "org.opencontainers.image.created"="2026-03-26T17:20:31Z" "release"="1774545417"org.opencontainers.image.revision=4d17df4ea3ff25815cca2550bc445280420af0a9,org.opencontainers.image.created=2026-03-26T17:20:31Z
# Fri, 27 Mar 2026 18:42:11 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 27 Mar 2026 18:42:11 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 27 Mar 2026 18:42:11 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 27 Mar 2026 18:42:11 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en         gnupg2     ;     microdnf clean all # buildkit
# Fri, 27 Mar 2026 18:42:11 GMT
ENV JAVA_VERSION=jdk8u482-b08
# Fri, 27 Mar 2026 18:42:14 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='ada72fbf191fb287b4c1e54be372b64c40c27c2ffbfa01f880c92af11f4e7c94';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u482-b08/OpenJDK8U-jdk_aarch64_linux_hotspot_8u482b08.tar.gz';          ;;        ppc64le)          ESUM='e77ba337c3ebb37fbef4961299f13fc4db87996ffd5470bdfb460cfc2ddb6053';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u482-b08/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u482b08.tar.gz';          ;;        x86_64)          ESUM='e74becad56b4cc01f1556a671e578d3788789f5257f9499f6fbed84e63a55ecf';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u482-b08/OpenJDK8U-jdk_x64_linux_hotspot_8u482b08.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip; # buildkit
# Fri, 27 Mar 2026 18:42:15 GMT
RUN set -eux;     echo "Verifying install ...";     echo "javac -version"; javac -version;     echo "java -version"; java -version;     echo "Complete." # buildkit
# Fri, 27 Mar 2026 18:42:15 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Fri, 27 Mar 2026 18:42:15 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
```

-	Layers:
	-	`sha256:e6c23a286985c06cc6d9b05d3d1e515a2fe5443b2da741ed6bc423f7907d3e67`  
		Last Modified: Thu, 26 Mar 2026 18:05:52 GMT  
		Size: 34.6 MB (34608408 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae11d1549633c5635252da904e6ce7aa6e9acb79dff945086afe3b153cb70015`  
		Last Modified: Fri, 27 Mar 2026 18:42:29 GMT  
		Size: 37.5 MB (37455344 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d3395eda32f25702bfebed65c27cc62ea3a181b13ef6e601c3cbd20b57569ff`  
		Last Modified: Fri, 27 Mar 2026 18:42:29 GMT  
		Size: 55.2 MB (55170674 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85e5f432a85e09168c4bf227c4839f97017172678a1c9e85d099dbb935c1e810`  
		Last Modified: Fri, 27 Mar 2026 18:42:27 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3902f9648fae4501748667b2c6a93915bee6e459df3bb8bebb1d8952e2d3e5ce`  
		Last Modified: Fri, 27 Mar 2026 18:42:28 GMT  
		Size: 2.3 KB (2316 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:8-jdk-ubi10-minimal` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:4970aed74c999602c59e4165ffc4c1d9b658373ebd3025b5a1d686055e355f3e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3930813 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de7f331c99569bdd1e73c0c8be39247c9a9324530dd75becee2b8885b68523c6`

```dockerfile
```

-	Layers:
	-	`sha256:d3ae9721afe172ae755d10b342a3343fc64227b8baa32d485a71bc206e354204`  
		Last Modified: Fri, 27 Mar 2026 18:42:27 GMT  
		Size: 3.9 MB (3910774 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bf858a4c9bcab25df885920961239426c5bbfc600cce2c484dc65838fc7630b3`  
		Last Modified: Fri, 27 Mar 2026 18:42:27 GMT  
		Size: 20.0 KB (20039 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-temurin:8-jdk-ubi10-minimal` - linux; arm64 variant v8

```console
$ docker pull eclipse-temurin@sha256:2c58c4e3402b4c5a57a319e08dc26285c795f90cc584a537bec5348fc2f0aadd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.3 MB (124341175 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0cf101a593b32915fb350f6fbc171060dff4731e7d0bf3a0f36038372008d78a`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`

```dockerfile
# Thu, 26 Mar 2026 17:23:52 GMT
LABEL maintainer="Red Hat, Inc."
# Thu, 26 Mar 2026 17:23:52 GMT
LABEL vendor="Red Hat, Inc."
# Thu, 26 Mar 2026 17:23:52 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Thu, 26 Mar 2026 17:23:52 GMT
LABEL com.redhat.component="ubi10-minimal-container"       name="ubi10/ubi-minimal"       version="10.1"       cpe="cpe:/o:redhat:enterprise_linux:10.1"       distribution-scope="public"
# Thu, 26 Mar 2026 17:23:52 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Thu, 26 Mar 2026 17:23:52 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 10."
# Thu, 26 Mar 2026 17:23:52 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 26 Mar 2026 17:23:52 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 26 Mar 2026 17:23:52 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 10 Minimal"
# Thu, 26 Mar 2026 17:23:52 GMT
LABEL io.openshift.expose-services=""
# Thu, 26 Mar 2026 17:23:52 GMT
LABEL io.openshift.tags="minimal rhel10"
# Thu, 26 Mar 2026 17:23:52 GMT
ENV container oci
# Thu, 26 Mar 2026 17:23:53 GMT
COPY dir:7d6c6936964da50429cf71ef4747883349075c5f65fea997c68d435e4becb027 in /      
# Thu, 26 Mar 2026 17:23:53 GMT
COPY file:5de33b5fc08b00635bccf9134a18978dba13e2250aa51838f9969515a3957847 in /etc/yum.repos.d/.      
# Thu, 26 Mar 2026 17:23:53 GMT
CMD ["/bin/bash"]
# Thu, 26 Mar 2026 17:23:53 GMT
COPY file:595171150af68abc798ea385f7988d74b566aa8e84babff137f00b08b2164683 in /usr/share/buildinfo/content-sets.json      
# Thu, 26 Mar 2026 17:23:54 GMT
COPY file:595171150af68abc798ea385f7988d74b566aa8e84babff137f00b08b2164683 in /root/buildinfo/content_manifests/content-sets.json      
# Thu, 26 Mar 2026 17:23:54 GMT
COPY file:72d28a3a1bd9c93099bf92feb048cbf67d57de2e84328846e17d81fa1ecc79fa in /usr/share/buildinfo/labels.json      
# Thu, 26 Mar 2026 17:23:54 GMT
COPY file:72d28a3a1bd9c93099bf92feb048cbf67d57de2e84328846e17d81fa1ecc79fa in /root/buildinfo/labels.json      
# Thu, 26 Mar 2026 17:23:54 GMT
LABEL "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="4d17df4ea3ff25815cca2550bc445280420af0a9" "org.opencontainers.image.revision"="4d17df4ea3ff25815cca2550bc445280420af0a9" "build-date"="2026-03-26T17:23:36Z" "org.opencontainers.image.created"="2026-03-26T17:23:36Z" "release"="1774545417"org.opencontainers.image.revision=4d17df4ea3ff25815cca2550bc445280420af0a9,org.opencontainers.image.created=2026-03-26T17:23:36Z
# Fri, 27 Mar 2026 18:43:28 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 27 Mar 2026 18:43:28 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 27 Mar 2026 18:43:28 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 27 Mar 2026 18:43:28 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en         gnupg2     ;     microdnf clean all # buildkit
# Fri, 27 Mar 2026 18:43:28 GMT
ENV JAVA_VERSION=jdk8u482-b08
# Fri, 27 Mar 2026 18:43:32 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='ada72fbf191fb287b4c1e54be372b64c40c27c2ffbfa01f880c92af11f4e7c94';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u482-b08/OpenJDK8U-jdk_aarch64_linux_hotspot_8u482b08.tar.gz';          ;;        ppc64le)          ESUM='e77ba337c3ebb37fbef4961299f13fc4db87996ffd5470bdfb460cfc2ddb6053';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u482-b08/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u482b08.tar.gz';          ;;        x86_64)          ESUM='e74becad56b4cc01f1556a671e578d3788789f5257f9499f6fbed84e63a55ecf';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u482-b08/OpenJDK8U-jdk_x64_linux_hotspot_8u482b08.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip; # buildkit
# Fri, 27 Mar 2026 18:43:32 GMT
RUN set -eux;     echo "Verifying install ...";     echo "javac -version"; javac -version;     echo "java -version"; java -version;     echo "Complete." # buildkit
# Fri, 27 Mar 2026 18:43:32 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Fri, 27 Mar 2026 18:43:32 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
```

-	Layers:
	-	`sha256:3bdc97aa816d30cff74675555d7b3f29b652ed3811ef43aff9bf264de81602f2`  
		Last Modified: Thu, 26 Mar 2026 18:05:46 GMT  
		Size: 32.7 MB (32681363 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b56b697405e695d3b65cc0df4ec3a539efd5116b2159b73f51f7b79a7744452`  
		Last Modified: Fri, 27 Mar 2026 18:43:47 GMT  
		Size: 37.4 MB (37405287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc48a0827b456421d2706633916489554caa50026a358caefdf1604c5f9c27c1`  
		Last Modified: Fri, 27 Mar 2026 18:43:48 GMT  
		Size: 54.3 MB (54252081 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46a19441b026cbd5e75f56f9f2a95477d345c6db247feaf4f1f3cb88e9eaee01`  
		Last Modified: Fri, 27 Mar 2026 18:43:45 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aca84e815ddd8a4a23d207184eee6912897645e2cefdaddc69963476872cbdf8`  
		Last Modified: Fri, 27 Mar 2026 18:43:47 GMT  
		Size: 2.3 KB (2316 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:8-jdk-ubi10-minimal` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:91189ce9ba3fdf99f8a6d16147a8dd917e76ff700a15d1c4ee223424f467d98c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3931055 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a88cae4f6713671be38a750d6352f7e9aeb3e6075f00de989da6d15a1d7bec7`

```dockerfile
```

-	Layers:
	-	`sha256:99a4b38c547f49daf405c7e94dddc23901202dc99fa115f859211cb3b39892c5`  
		Last Modified: Fri, 27 Mar 2026 18:43:46 GMT  
		Size: 3.9 MB (3910900 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3df8a5f4a3679d0984a6cad2518052f2b1b5f7b43451ebe8e481a17de01c50ed`  
		Last Modified: Fri, 27 Mar 2026 18:43:45 GMT  
		Size: 20.2 KB (20155 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-temurin:8-jdk-ubi10-minimal` - linux; ppc64le

```console
$ docker pull eclipse-temurin@sha256:219b503f5ae0b66c4e31b3c0169fc367cd56dc6016819317dd77afbfeb45d5b3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **130.6 MB (130571899 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b0cf7ddc9d91b1575e4ca0c11a14793eb032bb444d7e8fa6ddbcd81fe2f0281`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`

```dockerfile
# Thu, 26 Mar 2026 17:22:03 GMT
LABEL maintainer="Red Hat, Inc."
# Thu, 26 Mar 2026 17:22:03 GMT
LABEL vendor="Red Hat, Inc."
# Thu, 26 Mar 2026 17:22:03 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Thu, 26 Mar 2026 17:22:03 GMT
LABEL com.redhat.component="ubi10-minimal-container"       name="ubi10/ubi-minimal"       version="10.1"       cpe="cpe:/o:redhat:enterprise_linux:10.1"       distribution-scope="public"
# Thu, 26 Mar 2026 17:22:03 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Thu, 26 Mar 2026 17:22:03 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 10."
# Thu, 26 Mar 2026 17:22:03 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 26 Mar 2026 17:22:03 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 26 Mar 2026 17:22:03 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 10 Minimal"
# Thu, 26 Mar 2026 17:22:03 GMT
LABEL io.openshift.expose-services=""
# Thu, 26 Mar 2026 17:22:03 GMT
LABEL io.openshift.tags="minimal rhel10"
# Thu, 26 Mar 2026 17:22:03 GMT
ENV container oci
# Thu, 26 Mar 2026 17:22:03 GMT
COPY dir:c58a58aa30d2fc124efbb2fad87948342334ec1169d24c59d7c515f23167fc05 in /      
# Thu, 26 Mar 2026 17:22:04 GMT
COPY file:5de33b5fc08b00635bccf9134a18978dba13e2250aa51838f9969515a3957847 in /etc/yum.repos.d/.      
# Thu, 26 Mar 2026 17:22:04 GMT
CMD ["/bin/bash"]
# Thu, 26 Mar 2026 17:22:04 GMT
COPY file:595171150af68abc798ea385f7988d74b566aa8e84babff137f00b08b2164683 in /usr/share/buildinfo/content-sets.json      
# Thu, 26 Mar 2026 17:22:04 GMT
COPY file:595171150af68abc798ea385f7988d74b566aa8e84babff137f00b08b2164683 in /root/buildinfo/content_manifests/content-sets.json      
# Thu, 26 Mar 2026 17:22:04 GMT
COPY file:dd5a12247eaa56c1bce4445e2f72f6ec10e514179740b9b280ada967bb02c904 in /usr/share/buildinfo/labels.json      
# Thu, 26 Mar 2026 17:22:04 GMT
COPY file:dd5a12247eaa56c1bce4445e2f72f6ec10e514179740b9b280ada967bb02c904 in /root/buildinfo/labels.json      
# Thu, 26 Mar 2026 17:22:04 GMT
LABEL "architecture"="ppc64le" "vcs-type"="git" "vcs-ref"="4d17df4ea3ff25815cca2550bc445280420af0a9" "org.opencontainers.image.revision"="4d17df4ea3ff25815cca2550bc445280420af0a9" "build-date"="2026-03-26T17:21:51Z" "org.opencontainers.image.created"="2026-03-26T17:21:51Z" "release"="1774545417"org.opencontainers.image.revision=4d17df4ea3ff25815cca2550bc445280420af0a9,org.opencontainers.image.created=2026-03-26T17:21:51Z
# Fri, 27 Mar 2026 19:25:44 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 27 Mar 2026 19:25:44 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 27 Mar 2026 19:25:44 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 27 Mar 2026 19:25:44 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en         gnupg2     ;     microdnf clean all # buildkit
# Fri, 27 Mar 2026 19:25:44 GMT
ENV JAVA_VERSION=jdk8u482-b08
# Fri, 27 Mar 2026 19:25:55 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='ada72fbf191fb287b4c1e54be372b64c40c27c2ffbfa01f880c92af11f4e7c94';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u482-b08/OpenJDK8U-jdk_aarch64_linux_hotspot_8u482b08.tar.gz';          ;;        ppc64le)          ESUM='e77ba337c3ebb37fbef4961299f13fc4db87996ffd5470bdfb460cfc2ddb6053';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u482-b08/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u482b08.tar.gz';          ;;        x86_64)          ESUM='e74becad56b4cc01f1556a671e578d3788789f5257f9499f6fbed84e63a55ecf';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u482-b08/OpenJDK8U-jdk_x64_linux_hotspot_8u482b08.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip; # buildkit
# Fri, 27 Mar 2026 19:25:56 GMT
RUN set -eux;     echo "Verifying install ...";     echo "javac -version"; javac -version;     echo "java -version"; java -version;     echo "Complete." # buildkit
# Fri, 27 Mar 2026 19:25:56 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Fri, 27 Mar 2026 19:25:56 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
```

-	Layers:
	-	`sha256:d3afc82808d99ce4baa1bde62af82befcf71b8d6cb81303429e8a1936966a71f`  
		Last Modified: Thu, 26 Mar 2026 18:15:14 GMT  
		Size: 38.7 MB (38703412 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60ff6796efd7123f48d41ed631253b9606a3787b30627617e5128dcacafc4e44`  
		Last Modified: Fri, 27 Mar 2026 19:26:28 GMT  
		Size: 39.2 MB (39215080 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4194801d5263be7155c4884ae5aed40475969e48411f420d17039850dc71014a`  
		Last Modified: Fri, 27 Mar 2026 19:26:28 GMT  
		Size: 52.7 MB (52650966 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b51ff4d5ba178e9cfad43d970236491057eddfe3af891269883dae58cd5e7da2`  
		Last Modified: Fri, 27 Mar 2026 19:26:25 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fe2a609fe89ffc40623dc06b7b79a9048c01a1e6773d4ad76092cf5c639ed9c`  
		Last Modified: Fri, 27 Mar 2026 19:26:27 GMT  
		Size: 2.3 KB (2314 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:8-jdk-ubi10-minimal` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:d447da0fae4faae37262badcb58fe85c7239ad703b6821818881a9b3bfd3caec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3918275 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:545051755b4cfcda8a6b2353e656007b08c7712325f4d1958ae045fdb24ec49f`

```dockerfile
```

-	Layers:
	-	`sha256:1c1415d2502a25d460393b0ff31db7ad4d877cefbc07f2fc6cd4a74187908275`  
		Last Modified: Fri, 27 Mar 2026 19:26:26 GMT  
		Size: 3.9 MB (3898201 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:94cb188efa4dc9905e97b02b5dbc9167e895999d2ffdaeafa6751f2e3eb6f7d4`  
		Last Modified: Fri, 27 Mar 2026 19:26:25 GMT  
		Size: 20.1 KB (20074 bytes)  
		MIME: application/vnd.in-toto+json
