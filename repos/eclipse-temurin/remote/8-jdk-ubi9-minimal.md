## `eclipse-temurin:8-jdk-ubi9-minimal`

```console
$ docker pull eclipse-temurin@sha256:d8cac27af7f0a1f763ed3d15e781d01f50d13c878f1ed198d4ab399958ae8545
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `eclipse-temurin:8-jdk-ubi9-minimal` - linux; amd64

```console
$ docker pull eclipse-temurin@sha256:456cec48393be5bdf385876bd69a142261bd953efa87605793c7a3d6ebe95864
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **180.1 MB (180056994 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed7bd66fbe51063035f793468cecea0b81eeef230d134a192d806ec5c932c84c`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`

```dockerfile
# Wed, 23 Oct 2024 15:41:32 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 23 Oct 2024 15:41:32 GMT
LABEL vendor="Red Hat, Inc."
# Wed, 23 Oct 2024 15:41:32 GMT
LABEL url="https://www.redhat.com"
# Wed, 23 Oct 2024 15:41:32 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.5"       distribution-scope="public"
# Wed, 23 Oct 2024 15:41:32 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 23 Oct 2024 15:41:32 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Wed, 23 Oct 2024 15:41:32 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 23 Oct 2024 15:41:32 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 23 Oct 2024 15:41:32 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Wed, 23 Oct 2024 15:41:32 GMT
LABEL io.openshift.expose-services=""
# Wed, 23 Oct 2024 15:41:32 GMT
LABEL io.openshift.tags="minimal rhel9"
# Wed, 23 Oct 2024 15:41:32 GMT
ENV container oci
# Wed, 23 Oct 2024 15:41:32 GMT
COPY dir:0485e287b26ef73c199c820b8915015ba33a659f620dc17eafe7e7a33f8bf780 in / 
# Wed, 23 Oct 2024 15:41:32 GMT
COPY file:b37d593713ee21ad52a4cd1424dc019a24f7966f85df0ac4b86d234302695328 in /etc/yum.repos.d/. 
# Wed, 23 Oct 2024 15:41:32 GMT
CMD ["/bin/bash"]
# Wed, 23 Oct 2024 15:41:32 GMT
RUN . /cachi2/cachi2.env &&     rm -rf /var/log/*
# Wed, 23 Oct 2024 15:41:32 GMT
LABEL "build-date"="2024-12-18T04:56:25" "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="0724d65b854a0151fb7d10b0e6510d8aee28e115" "build-date"="2024-12-18T04:52:16Z" "release"="1734497536"
# Wed, 23 Oct 2024 15:41:32 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 23 Oct 2024 15:41:32 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 23 Oct 2024 15:41:32 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 23 Oct 2024 15:41:32 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         fontconfig         glibc-langpack-en     ;     microdnf clean all # buildkit
# Wed, 23 Oct 2024 15:41:32 GMT
ENV JAVA_VERSION=jdk8u432-b06
# Wed, 23 Oct 2024 15:41:32 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='383caabc20428e9500f2e07965317ed4387a0e336104483e29a9e06eeffbf26b';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u432-b06/OpenJDK8U-jdk_aarch64_linux_hotspot_8u432b06.tar.gz';          ;;        ppc64le)          ESUM='64fb17e83b79f9ad41dc18351a408bfe90324fd6360903ca5c0a740006c81be3';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u432-b06/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u432b06.tar.gz';          ;;        x86_64)          ESUM='abaaa90deadf51bd28921453baf2992b3dff6171bb7142f5bdd14ef269f7b245';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u432-b06/OpenJDK8U-jdk_x64_linux_hotspot_8u432b06.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -r "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Wed, 23 Oct 2024 15:41:32 GMT
RUN set -eux;     echo "Verifying install ...";     echo "javac -version"; javac -version;     echo "java -version"; java -version;     echo "Complete." # buildkit
# Wed, 23 Oct 2024 15:41:32 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 23 Oct 2024 15:41:32 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
```

-	Layers:
	-	`sha256:1e6b7297048ae70484705dda4e582fb8ad5778ea4c8ae464cf3e6a02ac439012`  
		Last Modified: Wed, 18 Dec 2024 06:15:23 GMT  
		Size: 39.4 MB (39432409 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a4c0bdf87f2f7631825895366e35f2619c6b33c42306c94e50a0d38a10697b8`  
		Last Modified: Thu, 19 Dec 2024 06:28:11 GMT  
		Size: 37.0 MB (36987481 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f015e0b629d45b851e2d40a752ea2b54fffed94b8b130ecacf6c63ae37d8aa8`  
		Last Modified: Thu, 19 Dec 2024 06:28:12 GMT  
		Size: 103.6 MB (103634661 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e938961550369e58a8bce822a4d86a001339cf7fd7822a5a63ba08c9823e9b40`  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f09fa5db038fcbc0ba3204a180a4c9622afdb4a61f9aa9c449c7a40fb3254f5c`  
		Last Modified: Thu, 19 Dec 2024 06:28:10 GMT  
		Size: 2.3 KB (2316 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:8-jdk-ubi9-minimal` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:8992d01f19c67fc84ece8508e75de01363a287a31bab560f95e689cb1d306cca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3808700 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:67c93089b04822571e6df2d54dd9971f0f0f0870b0724d6329d0fb5d8519ca91`

```dockerfile
```

-	Layers:
	-	`sha256:b816277af8fabd51ba219e8727956db9d615e07c68da1bea7d3450337f45dbe4`  
		Last Modified: Thu, 19 Dec 2024 06:28:10 GMT  
		Size: 3.8 MB (3789016 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:abbcada83b34d1b510c03fccb56bd1e5c465ee7ab990de8b1ba81df9321c898b`  
		Last Modified: Thu, 19 Dec 2024 06:28:09 GMT  
		Size: 19.7 KB (19684 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-temurin:8-jdk-ubi9-minimal` - linux; arm64 variant v8

```console
$ docker pull eclipse-temurin@sha256:0b0b57460d9376d177b764b5ed9a6c2e88777bbf8d3e50d87bfd1d31f3edd78b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **177.8 MB (177771946 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bbcc02ef3f059474153240e4fcc353c647768670ff53285844ccc44f4bec65bb`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`

```dockerfile
# Wed, 23 Oct 2024 15:41:32 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 23 Oct 2024 15:41:32 GMT
LABEL vendor="Red Hat, Inc."
# Wed, 23 Oct 2024 15:41:32 GMT
LABEL url="https://www.redhat.com"
# Wed, 23 Oct 2024 15:41:32 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.5"       distribution-scope="public"
# Wed, 23 Oct 2024 15:41:32 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 23 Oct 2024 15:41:32 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Wed, 23 Oct 2024 15:41:32 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 23 Oct 2024 15:41:32 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 23 Oct 2024 15:41:32 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Wed, 23 Oct 2024 15:41:32 GMT
LABEL io.openshift.expose-services=""
# Wed, 23 Oct 2024 15:41:32 GMT
LABEL io.openshift.tags="minimal rhel9"
# Wed, 23 Oct 2024 15:41:32 GMT
ENV container oci
# Wed, 23 Oct 2024 15:41:32 GMT
COPY dir:2b8ad1e81974d4feec292500267d9d72634438f9ec07a466db827a8114ef0993 in / 
# Wed, 23 Oct 2024 15:41:32 GMT
COPY file:b37d593713ee21ad52a4cd1424dc019a24f7966f85df0ac4b86d234302695328 in /etc/yum.repos.d/. 
# Wed, 23 Oct 2024 15:41:32 GMT
CMD ["/bin/bash"]
# Wed, 23 Oct 2024 15:41:32 GMT
RUN . /cachi2/cachi2.env &&     rm -rf /var/log/*
# Wed, 23 Oct 2024 15:41:32 GMT
LABEL "build-date"="2024-12-18T05:01:43" "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="0724d65b854a0151fb7d10b0e6510d8aee28e115" "build-date"="2024-12-18T04:52:16Z" "release"="1734497536"
# Wed, 23 Oct 2024 15:41:32 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 23 Oct 2024 15:41:32 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 23 Oct 2024 15:41:32 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 23 Oct 2024 15:41:32 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         fontconfig         glibc-langpack-en     ;     microdnf clean all # buildkit
# Wed, 23 Oct 2024 15:41:32 GMT
ENV JAVA_VERSION=jdk8u432-b06
# Wed, 23 Oct 2024 15:41:32 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='383caabc20428e9500f2e07965317ed4387a0e336104483e29a9e06eeffbf26b';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u432-b06/OpenJDK8U-jdk_aarch64_linux_hotspot_8u432b06.tar.gz';          ;;        ppc64le)          ESUM='64fb17e83b79f9ad41dc18351a408bfe90324fd6360903ca5c0a740006c81be3';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u432-b06/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u432b06.tar.gz';          ;;        x86_64)          ESUM='abaaa90deadf51bd28921453baf2992b3dff6171bb7142f5bdd14ef269f7b245';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u432-b06/OpenJDK8U-jdk_x64_linux_hotspot_8u432b06.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -r "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Wed, 23 Oct 2024 15:41:32 GMT
RUN set -eux;     echo "Verifying install ...";     echo "javac -version"; javac -version;     echo "java -version"; java -version;     echo "Complete." # buildkit
# Wed, 23 Oct 2024 15:41:32 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 23 Oct 2024 15:41:32 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
```

-	Layers:
	-	`sha256:3415b32764d8c185fafcd0c946a41d5028c72a76a1c10bcd8690f139ff79eb40`  
		Last Modified: Wed, 18 Dec 2024 06:15:28 GMT  
		Size: 37.6 MB (37577418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57f5ca1f094534b84eeb5099558913cebb9becc0ece5d82f47d4ed1bff8f0530`  
		Last Modified: Thu, 19 Dec 2024 06:29:45 GMT  
		Size: 37.4 MB (37443775 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d05d4c74dbd539def0b06aaf95cd4574000f88abced66b1b48b8c63c0eaffa12`  
		Last Modified: Thu, 19 Dec 2024 06:29:47 GMT  
		Size: 102.7 MB (102748307 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8d96ec8b3e5c16416a1942a544b38927254346aadd9595f22628bfcc4f5dfe8`  
		Last Modified: Thu, 19 Dec 2024 06:29:44 GMT  
		Size: 130.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8d48e096894e475cb0d7b4e1647df2e61db4f7ebc20799d8d8988365a14b299`  
		Last Modified: Thu, 19 Dec 2024 06:29:44 GMT  
		Size: 2.3 KB (2316 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:8-jdk-ubi9-minimal` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:af636183212db93e81350fb74f4f8fc3e70f361010284d2e1901f3535c7ac937
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3808704 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4da0afa3f232f048818868b60609637610f907cd32a1c98d0ef28d05b43be303`

```dockerfile
```

-	Layers:
	-	`sha256:5f98603d3e35d85566b13b9d9d3b719b6a626d359df5075824be60ab12c37d15`  
		Last Modified: Thu, 19 Dec 2024 06:29:44 GMT  
		Size: 3.8 MB (3788905 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0127ffe4504ff85bc789edf0569591343388352e25e4c90c822dc4a4fda2b713`  
		Last Modified: Thu, 19 Dec 2024 06:29:43 GMT  
		Size: 19.8 KB (19799 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-temurin:8-jdk-ubi9-minimal` - linux; ppc64le

```console
$ docker pull eclipse-temurin@sha256:15e6c0a4948cc8b29fc1775e5c4dc5e444915d56130b7bdb4326bfe87631e1c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **184.4 MB (184365596 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:592f10607361e061358f231293d08654776e257fa6b74ea390219a09dd153d9e`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`

```dockerfile
# Wed, 23 Oct 2024 15:41:32 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 23 Oct 2024 15:41:32 GMT
LABEL vendor="Red Hat, Inc."
# Wed, 23 Oct 2024 15:41:32 GMT
LABEL url="https://www.redhat.com"
# Wed, 23 Oct 2024 15:41:32 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.5"       distribution-scope="public"
# Wed, 23 Oct 2024 15:41:32 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 23 Oct 2024 15:41:32 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Wed, 23 Oct 2024 15:41:32 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 23 Oct 2024 15:41:32 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 23 Oct 2024 15:41:32 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Wed, 23 Oct 2024 15:41:32 GMT
LABEL io.openshift.expose-services=""
# Wed, 23 Oct 2024 15:41:32 GMT
LABEL io.openshift.tags="minimal rhel9"
# Wed, 23 Oct 2024 15:41:32 GMT
ENV container oci
# Wed, 23 Oct 2024 15:41:32 GMT
COPY dir:812543eca6d750875f0aa085b69e2a0865cd4978afc12d0f5ee611cc97abcc57 in / 
# Wed, 23 Oct 2024 15:41:32 GMT
COPY file:b37d593713ee21ad52a4cd1424dc019a24f7966f85df0ac4b86d234302695328 in /etc/yum.repos.d/. 
# Wed, 23 Oct 2024 15:41:32 GMT
CMD ["/bin/bash"]
# Wed, 23 Oct 2024 15:41:32 GMT
RUN . /cachi2/cachi2.env &&     rm -rf /var/log/*
# Wed, 23 Oct 2024 15:41:32 GMT
LABEL "build-date"="2024-12-18T05:08:50" "architecture"="ppc64le" "vcs-type"="git" "vcs-ref"="0724d65b854a0151fb7d10b0e6510d8aee28e115" "build-date"="2024-12-18T04:52:16Z" "release"="1734497536"
# Wed, 23 Oct 2024 15:41:32 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 23 Oct 2024 15:41:32 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 23 Oct 2024 15:41:32 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 23 Oct 2024 15:41:32 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         fontconfig         glibc-langpack-en     ;     microdnf clean all # buildkit
# Wed, 23 Oct 2024 15:41:32 GMT
ENV JAVA_VERSION=jdk8u432-b06
# Wed, 23 Oct 2024 15:41:32 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='383caabc20428e9500f2e07965317ed4387a0e336104483e29a9e06eeffbf26b';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u432-b06/OpenJDK8U-jdk_aarch64_linux_hotspot_8u432b06.tar.gz';          ;;        ppc64le)          ESUM='64fb17e83b79f9ad41dc18351a408bfe90324fd6360903ca5c0a740006c81be3';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u432-b06/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u432b06.tar.gz';          ;;        x86_64)          ESUM='abaaa90deadf51bd28921453baf2992b3dff6171bb7142f5bdd14ef269f7b245';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u432-b06/OpenJDK8U-jdk_x64_linux_hotspot_8u432b06.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -r "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Wed, 23 Oct 2024 15:41:32 GMT
RUN set -eux;     echo "Verifying install ...";     echo "javac -version"; javac -version;     echo "java -version"; java -version;     echo "Complete." # buildkit
# Wed, 23 Oct 2024 15:41:32 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 23 Oct 2024 15:41:32 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
```

-	Layers:
	-	`sha256:08256d51c6c275f4c9f694d18b8f1c909073b012ba7c7d9b5ea9f948ab194c83`  
		Last Modified: Wed, 18 Dec 2024 06:15:40 GMT  
		Size: 43.8 MB (43794286 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43ba1070e381ba17323f8d239e6cdd49953a6bc3dd93eb1d577039150e95992e`  
		Last Modified: Thu, 19 Dec 2024 06:29:27 GMT  
		Size: 39.5 MB (39476308 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:608d7d537ce291956b994e859271fe5d2d99433ac694a1da086137ad8713a636`  
		Last Modified: Thu, 19 Dec 2024 06:29:28 GMT  
		Size: 101.1 MB (101092559 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c823f4a9493363fbac99e9f17625cedb2bd6a9bef4b81c2158f5c735863d8a2b`  
		Last Modified: Thu, 19 Dec 2024 06:29:25 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7697ea9b6e0ac6fdf94a8aa5c8b6e0944aaf24b708f40e36589608e9f077daed`  
		Last Modified: Thu, 19 Dec 2024 06:29:26 GMT  
		Size: 2.3 KB (2315 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:8-jdk-ubi9-minimal` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:d9a6f585e55a1550ae6352b6b06c04838a73bcb3562f27f1f7b0b8323c50ea5f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3807241 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:18c23e1be4dfe227f147d83ddfe0374bfc3b55615f7707936362cc2cffeb9ff3`

```dockerfile
```

-	Layers:
	-	`sha256:54f6751f56b200f8a450c03bbee03130b124822289b7a73335e9a433a0b9673f`  
		Last Modified: Thu, 19 Dec 2024 06:29:25 GMT  
		Size: 3.8 MB (3787522 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7f3ea84f6c33bf15d05143ddcebd09e01f110bc450052012b7cb42e61b1e1e3a`  
		Last Modified: Thu, 19 Dec 2024 06:29:25 GMT  
		Size: 19.7 KB (19719 bytes)  
		MIME: application/vnd.in-toto+json
