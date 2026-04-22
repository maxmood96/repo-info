## `eclipse-temurin:8u482-b08-jdk-ubi9-minimal`

```console
$ docker pull eclipse-temurin@sha256:3ccbab56140896f98fe31b3a95a3366aac4a20bd820c2f2214b27b15424afdea
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `eclipse-temurin:8u482-b08-jdk-ubi9-minimal` - linux; amd64

```console
$ docker pull eclipse-temurin@sha256:ec915da8eb5048d55d4209cec34a69b2266470503157f731668ee815ea6b9317
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **125.6 MB (125565831 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:941d58e18cb986dcac719a7019885503a9437f7719598e5fb7f90765bb8b2c80`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`

```dockerfile
# Wed, 22 Apr 2026 04:58:45 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 22 Apr 2026 04:58:45 GMT
LABEL vendor="Red Hat, Inc."
# Wed, 22 Apr 2026 04:58:45 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Wed, 22 Apr 2026 04:58:45 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.7"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Wed, 22 Apr 2026 04:58:45 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 22 Apr 2026 04:58:45 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Wed, 22 Apr 2026 04:58:45 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 22 Apr 2026 04:58:45 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 22 Apr 2026 04:58:45 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Wed, 22 Apr 2026 04:58:45 GMT
LABEL io.openshift.expose-services=""
# Wed, 22 Apr 2026 04:58:45 GMT
LABEL io.openshift.tags="minimal rhel9"
# Wed, 22 Apr 2026 04:58:45 GMT
ENV container oci
# Wed, 22 Apr 2026 04:58:45 GMT
COPY dir:82e03e3ceb4a712116e9d6ecd1b99e2e729a68954b82c791f435d1cb8db14f8a in /      
# Wed, 22 Apr 2026 04:58:46 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Wed, 22 Apr 2026 04:58:46 GMT
CMD ["/bin/bash"]
# Wed, 22 Apr 2026 04:58:46 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /usr/share/buildinfo/content-sets.json      
# Wed, 22 Apr 2026 04:58:46 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /root/buildinfo/content_manifests/content-sets.json      
# Wed, 22 Apr 2026 04:58:46 GMT
COPY file:bc4dcbf01192949338f7e5550a4152e5364437463c0f897fd55b15eb58f57ead in /usr/share/buildinfo/labels.json      
# Wed, 22 Apr 2026 04:58:46 GMT
COPY file:bc4dcbf01192949338f7e5550a4152e5364437463c0f897fd55b15eb58f57ead in /root/buildinfo/labels.json      
# Wed, 22 Apr 2026 04:58:46 GMT
LABEL "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="5bb1e5f6eb0dd42dce5d2f21f64a3a9feec995f1" "org.opencontainers.image.revision"="5bb1e5f6eb0dd42dce5d2f21f64a3a9feec995f1" "build-date"="2026-04-22T04:58:33Z" "org.opencontainers.image.created"="2026-04-22T04:58:33Z" "release"="1776833838"org.opencontainers.image.revision=5bb1e5f6eb0dd42dce5d2f21f64a3a9feec995f1,org.opencontainers.image.created=2026-04-22T04:58:33Z
# Wed, 22 Apr 2026 18:16:15 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 22 Apr 2026 18:16:15 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 Apr 2026 18:16:15 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 22 Apr 2026 18:16:15 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en     ;     microdnf clean all # buildkit
# Wed, 22 Apr 2026 18:16:15 GMT
ENV JAVA_VERSION=jdk8u482-b08
# Wed, 22 Apr 2026 18:16:19 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='ada72fbf191fb287b4c1e54be372b64c40c27c2ffbfa01f880c92af11f4e7c94';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u482-b08/OpenJDK8U-jdk_aarch64_linux_hotspot_8u482b08.tar.gz';          ;;        ppc64le)          ESUM='e77ba337c3ebb37fbef4961299f13fc4db87996ffd5470bdfb460cfc2ddb6053';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u482-b08/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u482b08.tar.gz';          ;;        x86_64)          ESUM='e74becad56b4cc01f1556a671e578d3788789f5257f9499f6fbed84e63a55ecf';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u482-b08/OpenJDK8U-jdk_x64_linux_hotspot_8u482b08.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip; # buildkit
# Wed, 22 Apr 2026 18:16:20 GMT
RUN set -eux;     echo "Verifying install ...";     echo "javac -version"; javac -version;     echo "java -version"; java -version;     echo "Complete." # buildkit
# Wed, 22 Apr 2026 18:16:20 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 22 Apr 2026 18:16:20 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
```

-	Layers:
	-	`sha256:c770e69088fa05bea8942da1c1e3fa6066cc7c288153d81443e0c9435861e0b1`  
		Last Modified: Wed, 22 Apr 2026 05:40:43 GMT  
		Size: 40.0 MB (40024775 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59b6fd58dbc64bc342acd6d215a0173a72e7d61c0aae2f0c7ba581e509526511`  
		Last Modified: Wed, 22 Apr 2026 18:16:34 GMT  
		Size: 30.4 MB (30367990 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28bc484bf07cde32bae987bda06155887d87fb8e110b42530755ffbc9b516e9a`  
		Last Modified: Wed, 22 Apr 2026 18:16:35 GMT  
		Size: 55.2 MB (55170622 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e08e5fb782e2570a8ae241d1b2bd6e56a7734eb5661ff4637f925549b442c934`  
		Last Modified: Wed, 22 Apr 2026 18:16:32 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b52f9cfde6c4e04631e31ebe6739088755c3065a79cd17136699783886d3f964`  
		Last Modified: Wed, 22 Apr 2026 18:16:33 GMT  
		Size: 2.3 KB (2315 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:8u482-b08-jdk-ubi9-minimal` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:85f4eedfff6d28d1d155a00bc2882b6537bb31e419de7d6a9b45932fdb50ac0e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2641052 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b40e50dee3d0d29c9662a3aeaecf4b904147168cb4112cb798b6dedfdda66468`

```dockerfile
```

-	Layers:
	-	`sha256:6b19b8bf8abebea66a9755e3d9e5bf2f574c0e935d1af719fd0e2bb5dfb8f6f0`  
		Last Modified: Wed, 22 Apr 2026 18:16:32 GMT  
		Size: 2.6 MB (2621179 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2a6a896423eb0a0844b5c6ee69cd582bc233144cf06c0e54d3bd664e870b2e79`  
		Last Modified: Wed, 22 Apr 2026 18:16:32 GMT  
		Size: 19.9 KB (19873 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-temurin:8u482-b08-jdk-ubi9-minimal` - linux; arm64 variant v8

```console
$ docker pull eclipse-temurin@sha256:8c0a697047cd4109cf1720161d8b8772b9b5fbabbdcc14c3892b14785ee2b803
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **123.3 MB (123252043 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21a33efdeff886f01c285e4ea9e2293328c5096afdc059806df1b8efa5f3db54`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`

```dockerfile
# Wed, 22 Apr 2026 05:00:29 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 22 Apr 2026 05:00:29 GMT
LABEL vendor="Red Hat, Inc."
# Wed, 22 Apr 2026 05:00:29 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Wed, 22 Apr 2026 05:00:29 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.7"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Wed, 22 Apr 2026 05:00:29 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 22 Apr 2026 05:00:29 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Wed, 22 Apr 2026 05:00:29 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 22 Apr 2026 05:00:29 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 22 Apr 2026 05:00:29 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Wed, 22 Apr 2026 05:00:29 GMT
LABEL io.openshift.expose-services=""
# Wed, 22 Apr 2026 05:00:29 GMT
LABEL io.openshift.tags="minimal rhel9"
# Wed, 22 Apr 2026 05:00:29 GMT
ENV container oci
# Wed, 22 Apr 2026 05:00:30 GMT
COPY dir:5dfc5d431dcfd4937d8e6a4dd1184486112214c6f8d103a0640fb0f8231a0840 in /      
# Wed, 22 Apr 2026 05:00:30 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Wed, 22 Apr 2026 05:00:30 GMT
CMD ["/bin/bash"]
# Wed, 22 Apr 2026 05:00:30 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /usr/share/buildinfo/content-sets.json      
# Wed, 22 Apr 2026 05:00:30 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /root/buildinfo/content_manifests/content-sets.json      
# Wed, 22 Apr 2026 05:00:30 GMT
COPY file:15cced1d80c5bc31ac720f4e201d7d85c034d443588a80d803a468e8714fc167 in /usr/share/buildinfo/labels.json      
# Wed, 22 Apr 2026 05:00:30 GMT
COPY file:15cced1d80c5bc31ac720f4e201d7d85c034d443588a80d803a468e8714fc167 in /root/buildinfo/labels.json      
# Wed, 22 Apr 2026 05:00:31 GMT
LABEL "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="5bb1e5f6eb0dd42dce5d2f21f64a3a9feec995f1" "org.opencontainers.image.revision"="5bb1e5f6eb0dd42dce5d2f21f64a3a9feec995f1" "build-date"="2026-04-22T05:00:16Z" "org.opencontainers.image.created"="2026-04-22T05:00:16Z" "release"="1776833838"org.opencontainers.image.revision=5bb1e5f6eb0dd42dce5d2f21f64a3a9feec995f1,org.opencontainers.image.created=2026-04-22T05:00:16Z
# Wed, 22 Apr 2026 18:16:04 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 22 Apr 2026 18:16:04 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 Apr 2026 18:16:04 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 22 Apr 2026 18:16:04 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en     ;     microdnf clean all # buildkit
# Wed, 22 Apr 2026 18:16:04 GMT
ENV JAVA_VERSION=jdk8u482-b08
# Wed, 22 Apr 2026 18:16:09 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='ada72fbf191fb287b4c1e54be372b64c40c27c2ffbfa01f880c92af11f4e7c94';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u482-b08/OpenJDK8U-jdk_aarch64_linux_hotspot_8u482b08.tar.gz';          ;;        ppc64le)          ESUM='e77ba337c3ebb37fbef4961299f13fc4db87996ffd5470bdfb460cfc2ddb6053';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u482-b08/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u482b08.tar.gz';          ;;        x86_64)          ESUM='e74becad56b4cc01f1556a671e578d3788789f5257f9499f6fbed84e63a55ecf';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u482-b08/OpenJDK8U-jdk_x64_linux_hotspot_8u482b08.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip; # buildkit
# Wed, 22 Apr 2026 18:16:09 GMT
RUN set -eux;     echo "Verifying install ...";     echo "javac -version"; javac -version;     echo "java -version"; java -version;     echo "Complete." # buildkit
# Wed, 22 Apr 2026 18:16:09 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 22 Apr 2026 18:16:09 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
```

-	Layers:
	-	`sha256:c57a97b2502dbf8d905aa782f6a2be8f57c8774e28f6d2ddf6a9a866fcc5fd8b`  
		Last Modified: Wed, 22 Apr 2026 06:11:08 GMT  
		Size: 38.2 MB (38204491 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6c9bc24c0acdf270fe94e074b68fedf41d00d9b9237e86cf07e30494f14572b`  
		Last Modified: Wed, 22 Apr 2026 18:16:24 GMT  
		Size: 30.8 MB (30793080 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba2eec6f6928395a35f611a28dd8a5bf1da33cd690df60695e3ff6f44f735163`  
		Last Modified: Wed, 22 Apr 2026 18:16:24 GMT  
		Size: 54.3 MB (54252030 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d785564a79c1ea669bffe73a52c19b2748cab5bd1167fa6c36467bbbe4d96e8`  
		Last Modified: Wed, 22 Apr 2026 18:16:21 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab21335db5cee72ce834f9314b17d6f599360cdafd810a8f702cd26b48d4502a`  
		Last Modified: Wed, 22 Apr 2026 18:16:23 GMT  
		Size: 2.3 KB (2314 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:8u482-b08-jdk-ubi9-minimal` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:1c7c0cb2d3afbd9b059765f4ea78e9537cd7f80f05986dac0e5e39d02b0a0504
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2641238 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b4a9b363d3f40b038f5087f6cbfbec3679604366fd4b4b8d9c3890f091bec09`

```dockerfile
```

-	Layers:
	-	`sha256:ca5c821e4db14ec52a5bca5db96c6ddc92d53814028f8fff5c318f64abc0872f`  
		Last Modified: Wed, 22 Apr 2026 18:16:22 GMT  
		Size: 2.6 MB (2621249 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7dc1dbace7fa7e0f8c8a784157866a69b9c6afa3b15765dc4257dc7359468798`  
		Last Modified: Wed, 22 Apr 2026 18:16:21 GMT  
		Size: 20.0 KB (19989 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-temurin:8u482-b08-jdk-ubi9-minimal` - linux; ppc64le

```console
$ docker pull eclipse-temurin@sha256:a976c1f8797b8044af471e80c13e4b4a24b42bbe966a0df613a09ab4ae1be9ac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **129.9 MB (129945752 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:58eacaab10a90e83fe2ccf4200190cb5f60203b00bcaded6433fbf44d777b004`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`

```dockerfile
# Mon, 20 Apr 2026 00:48:23 GMT
LABEL maintainer="Red Hat, Inc."
# Mon, 20 Apr 2026 00:48:23 GMT
LABEL vendor="Red Hat, Inc."
# Mon, 20 Apr 2026 00:48:23 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Mon, 20 Apr 2026 00:48:23 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.7"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Mon, 20 Apr 2026 00:48:23 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Mon, 20 Apr 2026 00:48:23 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Mon, 20 Apr 2026 00:48:23 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 20 Apr 2026 00:48:23 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 20 Apr 2026 00:48:23 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Mon, 20 Apr 2026 00:48:23 GMT
LABEL io.openshift.expose-services=""
# Mon, 20 Apr 2026 00:48:23 GMT
LABEL io.openshift.tags="minimal rhel9"
# Mon, 20 Apr 2026 00:48:23 GMT
ENV container oci
# Mon, 20 Apr 2026 00:48:24 GMT
COPY dir:8240d23726e865ba51f291ba4ea188782a75a0af67ec349dc8d9d3bc145ecd05 in /      
# Mon, 20 Apr 2026 00:48:24 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Mon, 20 Apr 2026 00:48:24 GMT
CMD ["/bin/bash"]
# Mon, 20 Apr 2026 00:48:24 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /usr/share/buildinfo/content-sets.json      
# Mon, 20 Apr 2026 00:48:24 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /root/buildinfo/content_manifests/content-sets.json      
# Mon, 20 Apr 2026 00:48:24 GMT
COPY file:54c55160da8e94b0ed06988eaccac768df07b2ab8418806d9245b992ab4c1444 in /usr/share/buildinfo/labels.json      
# Mon, 20 Apr 2026 00:48:24 GMT
COPY file:54c55160da8e94b0ed06988eaccac768df07b2ab8418806d9245b992ab4c1444 in /root/buildinfo/labels.json      
# Mon, 20 Apr 2026 00:48:25 GMT
LABEL "architecture"="ppc64le" "vcs-type"="git" "vcs-ref"="0bc61a274edddc1467c2ad0ddc3139543c4da4da" "org.opencontainers.image.revision"="0bc61a274edddc1467c2ad0ddc3139543c4da4da" "build-date"="2026-04-20T00:48:13Z" "org.opencontainers.image.created"="2026-04-20T00:48:13Z" "release"="1776645941"org.opencontainers.image.revision=0bc61a274edddc1467c2ad0ddc3139543c4da4da,org.opencontainers.image.created=2026-04-20T00:48:13Z
# Mon, 20 Apr 2026 23:00:52 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 20 Apr 2026 23:00:52 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 20 Apr 2026 23:00:52 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 20 Apr 2026 23:00:52 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en     ;     microdnf clean all # buildkit
# Mon, 20 Apr 2026 23:00:52 GMT
ENV JAVA_VERSION=jdk8u482-b08
# Mon, 20 Apr 2026 23:01:01 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='ada72fbf191fb287b4c1e54be372b64c40c27c2ffbfa01f880c92af11f4e7c94';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u482-b08/OpenJDK8U-jdk_aarch64_linux_hotspot_8u482b08.tar.gz';          ;;        ppc64le)          ESUM='e77ba337c3ebb37fbef4961299f13fc4db87996ffd5470bdfb460cfc2ddb6053';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u482-b08/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u482b08.tar.gz';          ;;        x86_64)          ESUM='e74becad56b4cc01f1556a671e578d3788789f5257f9499f6fbed84e63a55ecf';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u482-b08/OpenJDK8U-jdk_x64_linux_hotspot_8u482b08.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip; # buildkit
# Mon, 20 Apr 2026 23:01:02 GMT
RUN set -eux;     echo "Verifying install ...";     echo "javac -version"; javac -version;     echo "java -version"; java -version;     echo "Complete." # buildkit
# Mon, 20 Apr 2026 23:01:02 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Mon, 20 Apr 2026 23:01:02 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
```

-	Layers:
	-	`sha256:9d0996bd7c74d1634fd0ba1753a8f74e86b97c5b41318f888d6b7bcc768131db`  
		Last Modified: Mon, 20 Apr 2026 12:13:59 GMT  
		Size: 44.4 MB (44443917 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:242b1bfcc64f23f4a2cc6ba069104831d0f144abd63cec2aa7e370ca093096b9`  
		Last Modified: Mon, 20 Apr 2026 23:01:35 GMT  
		Size: 32.8 MB (32848454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa0223b5bba3a24a61223e695ef63fb88ada0769d482fef46112476e17c806f1`  
		Last Modified: Mon, 20 Apr 2026 23:01:36 GMT  
		Size: 52.7 MB (52650935 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7af817865ea173c7f075bf41861f64df6f193de215cad24960eb8fcb7b9df9a9`  
		Last Modified: Mon, 20 Apr 2026 23:01:33 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a9c720ef1359090bb4052ef4152e3c095b19e7bc48701b2451ad0f0d0f83cb6`  
		Last Modified: Mon, 20 Apr 2026 23:01:34 GMT  
		Size: 2.3 KB (2317 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:8u482-b08-jdk-ubi9-minimal` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:bd34aa2da07ff9aece9cec9ae0d8c5f0aeb5610b0f99d038611c80fcc4e61370
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2639775 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a8959c962ae9cacd2e755332341e55e74e731f8ceb815d941b7957fd7270676b`

```dockerfile
```

-	Layers:
	-	`sha256:982b5537868717166af424002789fe990311974791a3f9f53b3776d327cec58d`  
		Last Modified: Mon, 20 Apr 2026 23:01:33 GMT  
		Size: 2.6 MB (2619866 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f020d8af2634f678958ad146749b32c094a7de579e8527befd9b136e698a832b`  
		Last Modified: Mon, 20 Apr 2026 23:01:33 GMT  
		Size: 19.9 KB (19909 bytes)  
		MIME: application/vnd.in-toto+json
