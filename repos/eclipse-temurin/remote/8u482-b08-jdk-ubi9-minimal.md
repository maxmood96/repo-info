## `eclipse-temurin:8u482-b08-jdk-ubi9-minimal`

```console
$ docker pull eclipse-temurin@sha256:262b4291bf12adbb149a1d8d9bcc1ec662c7aeaccd6d490b05ed9a5b8a481f38
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
$ docker pull eclipse-temurin@sha256:d15b2987f568cff22c343088268eb1a0ffaf4678756db6b03c474934a14f9656
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **111.4 MB (111429799 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:427637a10e113896532f880106703f024e4dd538fb43f6f11be10ad1db16c481`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`

```dockerfile
# Mon, 04 May 2026 01:27:16 GMT
LABEL maintainer="Red Hat, Inc."
# Mon, 04 May 2026 01:27:16 GMT
LABEL vendor="Red Hat, Inc."
# Mon, 04 May 2026 01:27:16 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Mon, 04 May 2026 01:27:16 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.7"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Mon, 04 May 2026 01:27:16 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Mon, 04 May 2026 01:27:16 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Mon, 04 May 2026 01:27:17 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 04 May 2026 01:27:17 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 04 May 2026 01:27:17 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Mon, 04 May 2026 01:27:17 GMT
LABEL io.openshift.expose-services=""
# Mon, 04 May 2026 01:27:17 GMT
LABEL io.openshift.tags="minimal rhel9"
# Mon, 04 May 2026 01:27:17 GMT
ENV container oci
# Mon, 04 May 2026 01:27:17 GMT
COPY dir:65829633e0a732ee03a3da731062eca14df67dc0e6bab86d02002ef9d123d97c in /      
# Mon, 04 May 2026 01:27:17 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Mon, 04 May 2026 01:27:17 GMT
CMD ["/bin/bash"]
# Mon, 04 May 2026 01:27:17 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /usr/share/buildinfo/content-sets.json      
# Mon, 04 May 2026 01:27:17 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /root/buildinfo/content_manifests/content-sets.json      
# Mon, 04 May 2026 01:27:18 GMT
COPY file:c2149fceb878782b97b2875047824d21e0e5ecd57a50bf8e1dd5d47550f18358 in /usr/share/buildinfo/labels.json      
# Mon, 04 May 2026 01:27:18 GMT
COPY file:c2149fceb878782b97b2875047824d21e0e5ecd57a50bf8e1dd5d47550f18358 in /root/buildinfo/labels.json      
# Mon, 04 May 2026 01:27:18 GMT
LABEL "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="dbf428e1775c5e4c4802b4c714d3b50b652d0c8a" "org.opencontainers.image.revision"="dbf428e1775c5e4c4802b4c714d3b50b652d0c8a" "build-date"="2026-05-04T01:27:05Z" "org.opencontainers.image.created"="2026-05-04T01:27:05Z" "release"="1777857961"org.opencontainers.image.revision=dbf428e1775c5e4c4802b4c714d3b50b652d0c8a,org.opencontainers.image.created=2026-05-04T01:27:05Z
# Tue, 05 May 2026 23:07:45 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 05 May 2026 23:07:45 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 05 May 2026 23:07:45 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 05 May 2026 23:07:45 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en     ;     microdnf clean all # buildkit
# Tue, 05 May 2026 23:07:45 GMT
ENV JAVA_VERSION=jdk8u482-b08
# Tue, 05 May 2026 23:07:50 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='ada72fbf191fb287b4c1e54be372b64c40c27c2ffbfa01f880c92af11f4e7c94';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u482-b08/OpenJDK8U-jdk_aarch64_linux_hotspot_8u482b08.tar.gz';          ;;        ppc64le)          ESUM='e77ba337c3ebb37fbef4961299f13fc4db87996ffd5470bdfb460cfc2ddb6053';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u482-b08/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u482b08.tar.gz';          ;;        x86_64)          ESUM='e74becad56b4cc01f1556a671e578d3788789f5257f9499f6fbed84e63a55ecf';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u482-b08/OpenJDK8U-jdk_x64_linux_hotspot_8u482b08.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip; # buildkit
# Tue, 05 May 2026 23:07:50 GMT
RUN set -eux;     echo "Verifying install ...";     echo "javac -version"; javac -version;     echo "java -version"; java -version;     echo "Complete." # buildkit
# Tue, 05 May 2026 23:07:50 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 05 May 2026 23:07:50 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
```

-	Layers:
	-	`sha256:cd8d59cb7a894fbcbefe70d3cdbc433492e715351e24e77b24a441609ab2de47`  
		Last Modified: Mon, 04 May 2026 03:52:20 GMT  
		Size: 40.0 MB (40019116 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:969111f31702fd00317b970ea8b98b8a0ffdafb39fed89f357a6c067b1c37c0e`  
		Last Modified: Tue, 05 May 2026 23:08:02 GMT  
		Size: 16.2 MB (16237610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c93fa8028faacddef1ce9b65cf721a4fd7c006c3cc60421298438e249c3bb93`  
		Last Modified: Tue, 05 May 2026 23:08:03 GMT  
		Size: 55.2 MB (55170629 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98eb9e265757dd5a569feceadc98a0ee0188f7df8db755def15af06c5a46f3da`  
		Last Modified: Tue, 05 May 2026 23:08:00 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:445166a5d8823d2ca7966509b94a1b529613b62641a943c15622fd1bcbb9b2ed`  
		Last Modified: Tue, 05 May 2026 23:08:02 GMT  
		Size: 2.3 KB (2316 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:8u482-b08-jdk-ubi9-minimal` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:0b2526353e139eb638c0917b69d22fe29b11bb11cf25bf6bf1936b2523b1dd77
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.9 MB (1901651 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2db47ac7af94a8d8e6ac9c0e6e55b97d76c4158c06a839d501dca1d1dde17e2c`

```dockerfile
```

-	Layers:
	-	`sha256:cade7744389d38f56457e35fbb4e377c05c9ec9179ee76c799c10f79ead7ab83`  
		Last Modified: Tue, 05 May 2026 23:08:01 GMT  
		Size: 1.9 MB (1881779 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:45b7b89fe64448340dd7a896398c7c5d4075cef8c7826b62d33afc023391f950`  
		Last Modified: Tue, 05 May 2026 23:08:01 GMT  
		Size: 19.9 KB (19872 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-temurin:8u482-b08-jdk-ubi9-minimal` - linux; arm64 variant v8

```console
$ docker pull eclipse-temurin@sha256:d703392c5fe22ce7cf0f4bf9bc864867de93ee7df99979aceeaf40b97c6a99d1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **109.2 MB (109227886 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b8aa6f9c8d73248456d8c986ab47a62b4f067fa69ad1c1cd6454d2b5e9d1cf0a`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`

```dockerfile
# Mon, 04 May 2026 01:30:08 GMT
LABEL maintainer="Red Hat, Inc."
# Mon, 04 May 2026 01:30:08 GMT
LABEL vendor="Red Hat, Inc."
# Mon, 04 May 2026 01:30:08 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Mon, 04 May 2026 01:30:08 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.7"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Mon, 04 May 2026 01:30:08 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Mon, 04 May 2026 01:30:08 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Mon, 04 May 2026 01:30:08 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 04 May 2026 01:30:08 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 04 May 2026 01:30:08 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Mon, 04 May 2026 01:30:08 GMT
LABEL io.openshift.expose-services=""
# Mon, 04 May 2026 01:30:08 GMT
LABEL io.openshift.tags="minimal rhel9"
# Mon, 04 May 2026 01:30:08 GMT
ENV container oci
# Mon, 04 May 2026 01:30:09 GMT
COPY dir:5ad712b8248d48b2932fa5bdcc0ad50ec37c7d49fe231a7db1a1c2391217329a in /      
# Mon, 04 May 2026 01:30:09 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Mon, 04 May 2026 01:30:09 GMT
CMD ["/bin/bash"]
# Mon, 04 May 2026 01:30:09 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /usr/share/buildinfo/content-sets.json      
# Mon, 04 May 2026 01:30:09 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /root/buildinfo/content_manifests/content-sets.json      
# Mon, 04 May 2026 01:30:09 GMT
COPY file:11a91ebd5ef22e4f28676b4a9dc8447f7af7f01609b0311ebd76ca9c6631f340 in /usr/share/buildinfo/labels.json      
# Mon, 04 May 2026 01:30:10 GMT
COPY file:11a91ebd5ef22e4f28676b4a9dc8447f7af7f01609b0311ebd76ca9c6631f340 in /root/buildinfo/labels.json      
# Mon, 04 May 2026 01:30:10 GMT
LABEL "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="dbf428e1775c5e4c4802b4c714d3b50b652d0c8a" "org.opencontainers.image.revision"="dbf428e1775c5e4c4802b4c714d3b50b652d0c8a" "build-date"="2026-05-04T01:29:56Z" "org.opencontainers.image.created"="2026-05-04T01:29:56Z" "release"="1777857961"org.opencontainers.image.revision=dbf428e1775c5e4c4802b4c714d3b50b652d0c8a,org.opencontainers.image.created=2026-05-04T01:29:56Z
# Tue, 05 May 2026 23:07:40 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 05 May 2026 23:07:40 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 05 May 2026 23:07:40 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 05 May 2026 23:07:40 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en     ;     microdnf clean all # buildkit
# Tue, 05 May 2026 23:07:40 GMT
ENV JAVA_VERSION=jdk8u482-b08
# Tue, 05 May 2026 23:07:44 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='ada72fbf191fb287b4c1e54be372b64c40c27c2ffbfa01f880c92af11f4e7c94';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u482-b08/OpenJDK8U-jdk_aarch64_linux_hotspot_8u482b08.tar.gz';          ;;        ppc64le)          ESUM='e77ba337c3ebb37fbef4961299f13fc4db87996ffd5470bdfb460cfc2ddb6053';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u482-b08/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u482b08.tar.gz';          ;;        x86_64)          ESUM='e74becad56b4cc01f1556a671e578d3788789f5257f9499f6fbed84e63a55ecf';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u482-b08/OpenJDK8U-jdk_x64_linux_hotspot_8u482b08.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip; # buildkit
# Tue, 05 May 2026 23:07:44 GMT
RUN set -eux;     echo "Verifying install ...";     echo "javac -version"; javac -version;     echo "java -version"; java -version;     echo "Complete." # buildkit
# Tue, 05 May 2026 23:07:44 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 05 May 2026 23:07:44 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
```

-	Layers:
	-	`sha256:eae0b4c39ea6d65927abe502bd11bbd574acc09733cb468c989628c5b204a24b`  
		Last Modified: Mon, 04 May 2026 05:13:02 GMT  
		Size: 38.2 MB (38205818 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9911e69eb771b87df1da974736818ab03548f3b33f77c4107c61598f3f6f375a`  
		Last Modified: Tue, 05 May 2026 23:07:57 GMT  
		Size: 16.8 MB (16767571 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:647a157ef58f91222de1cced3d0afbf551b3730a6c99f68f7441f4b2226147e4`  
		Last Modified: Tue, 05 May 2026 23:07:58 GMT  
		Size: 54.3 MB (54252055 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93f9eb94cf7ab54ced9864b01c57a56d0093969040cc4e2c5b4611293103777c`  
		Last Modified: Tue, 05 May 2026 23:07:56 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01cab788c2f33318b0e92f0955cf56e88c7cc620ce528ec96e681aec798c81ea`  
		Last Modified: Tue, 05 May 2026 23:07:56 GMT  
		Size: 2.3 KB (2316 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:8u482-b08-jdk-ubi9-minimal` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:e8f0422afb16d23c880970841bcf0697431c50c1cd42837c51afbf159b85f6e9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.9 MB (1903068 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f830afb263ddc36100e9ae6826d0ed83b4c8ac103e091196d12ac8e7f799b003`

```dockerfile
```

-	Layers:
	-	`sha256:9469c6d7a5af65a1a63c045908adaf795723ea41d207ada14536db56d5b3f74b`  
		Last Modified: Tue, 05 May 2026 23:07:56 GMT  
		Size: 1.9 MB (1883079 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fa6c291d095041512da36b71032c942ec6ee1b66e98bb2719228cac59224eb76`  
		Last Modified: Tue, 05 May 2026 23:07:56 GMT  
		Size: 20.0 KB (19989 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-temurin:8u482-b08-jdk-ubi9-minimal` - linux; ppc64le

```console
$ docker pull eclipse-temurin@sha256:4cae8e065b70c252a8855cb877f6eeb08e720d2095eb4fcb60b9920c00e4ff47
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.0 MB (114999765 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e719576933022ff9bb1650c391ea01883ed5fc56607dac3691f483909d7493ec`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`

```dockerfile
# Mon, 04 May 2026 01:28:51 GMT
LABEL maintainer="Red Hat, Inc."
# Mon, 04 May 2026 01:28:51 GMT
LABEL vendor="Red Hat, Inc."
# Mon, 04 May 2026 01:28:51 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Mon, 04 May 2026 01:28:52 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.7"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Mon, 04 May 2026 01:28:52 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Mon, 04 May 2026 01:28:52 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Mon, 04 May 2026 01:28:52 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 04 May 2026 01:28:52 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 04 May 2026 01:28:52 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Mon, 04 May 2026 01:28:52 GMT
LABEL io.openshift.expose-services=""
# Mon, 04 May 2026 01:28:52 GMT
LABEL io.openshift.tags="minimal rhel9"
# Mon, 04 May 2026 01:28:52 GMT
ENV container oci
# Mon, 04 May 2026 01:28:52 GMT
COPY dir:95ecb7253fddf635ae6d975427ddb73b0a49c785b217cf296b0a0358678fc43f in /      
# Mon, 04 May 2026 01:28:52 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Mon, 04 May 2026 01:28:52 GMT
CMD ["/bin/bash"]
# Mon, 04 May 2026 01:28:52 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /usr/share/buildinfo/content-sets.json      
# Mon, 04 May 2026 01:28:52 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /root/buildinfo/content_manifests/content-sets.json      
# Mon, 04 May 2026 01:28:53 GMT
COPY file:21c41e3d00d3a684fc39637052cae774dab908d634556245b0fd07fa3273162a in /usr/share/buildinfo/labels.json      
# Mon, 04 May 2026 01:28:53 GMT
COPY file:21c41e3d00d3a684fc39637052cae774dab908d634556245b0fd07fa3273162a in /root/buildinfo/labels.json      
# Mon, 04 May 2026 01:28:53 GMT
LABEL "architecture"="ppc64le" "vcs-type"="git" "vcs-ref"="dbf428e1775c5e4c4802b4c714d3b50b652d0c8a" "org.opencontainers.image.revision"="dbf428e1775c5e4c4802b4c714d3b50b652d0c8a" "build-date"="2026-05-04T01:28:41Z" "org.opencontainers.image.created"="2026-05-04T01:28:41Z" "release"="1777857961"org.opencontainers.image.revision=dbf428e1775c5e4c4802b4c714d3b50b652d0c8a,org.opencontainers.image.created=2026-05-04T01:28:41Z
# Tue, 05 May 2026 23:48:45 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 05 May 2026 23:48:45 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 05 May 2026 23:48:45 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 05 May 2026 23:48:45 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en     ;     microdnf clean all # buildkit
# Tue, 05 May 2026 23:48:45 GMT
ENV JAVA_VERSION=jdk8u482-b08
# Tue, 05 May 2026 23:48:55 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='ada72fbf191fb287b4c1e54be372b64c40c27c2ffbfa01f880c92af11f4e7c94';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u482-b08/OpenJDK8U-jdk_aarch64_linux_hotspot_8u482b08.tar.gz';          ;;        ppc64le)          ESUM='e77ba337c3ebb37fbef4961299f13fc4db87996ffd5470bdfb460cfc2ddb6053';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u482-b08/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u482b08.tar.gz';          ;;        x86_64)          ESUM='e74becad56b4cc01f1556a671e578d3788789f5257f9499f6fbed84e63a55ecf';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u482-b08/OpenJDK8U-jdk_x64_linux_hotspot_8u482b08.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip; # buildkit
# Tue, 05 May 2026 23:48:56 GMT
RUN set -eux;     echo "Verifying install ...";     echo "javac -version"; javac -version;     echo "java -version"; java -version;     echo "Complete." # buildkit
# Tue, 05 May 2026 23:48:56 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 05 May 2026 23:48:56 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
```

-	Layers:
	-	`sha256:651dc6a385386e8e87790c18da9695023b6028435c56101235d26c0359b72932`  
		Last Modified: Mon, 04 May 2026 06:11:22 GMT  
		Size: 44.4 MB (44437692 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1767d5eb85065ec07c318883803129ba6d9958ad6e2956b0bc74061b3eaad718`  
		Last Modified: Tue, 05 May 2026 23:49:22 GMT  
		Size: 17.9 MB (17908683 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07bb7f84a5d484cb3c48a0b0dc34426db873fc684a61542ac942bc3a44e784e6`  
		Last Modified: Tue, 05 May 2026 23:49:24 GMT  
		Size: 52.7 MB (52650947 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b853ed137b8cb407bf383fefd173209e41f7d0ee0e57808c8095878f522a874`  
		Last Modified: Tue, 05 May 2026 23:49:21 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9ced8a6def23624e68bd0f678dc6953c5a58b92610325ffc2b981884c2da8cf`  
		Last Modified: Tue, 05 May 2026 23:49:22 GMT  
		Size: 2.3 KB (2316 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:8u482-b08-jdk-ubi9-minimal` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:804b11b82a4381df1c758044a2c0936416ffabdedcea0e238e70c9dd085ce67e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.9 MB (1902787 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c9d483429f78d15dd703fc13a5be43e45753f7f356212a34fc8014dd3afba750`

```dockerfile
```

-	Layers:
	-	`sha256:6588299ddfb6379f9b3c4468bcba70236012d475b04ac06196b5c4a28f564041`  
		Last Modified: Tue, 05 May 2026 23:49:21 GMT  
		Size: 1.9 MB (1882878 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8614af022c8723dcd30ad4fb0c4a21b9376aac89d41758fe9e6aa172fe2b1a15`  
		Last Modified: Tue, 05 May 2026 23:49:21 GMT  
		Size: 19.9 KB (19909 bytes)  
		MIME: application/vnd.in-toto+json
