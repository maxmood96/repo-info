## `eclipse-temurin:8-jdk-ubi9-minimal`

```console
$ docker pull eclipse-temurin@sha256:1a1c998efd30be2c5c159f4e4f7360c2d539f1390a6de3755ab60a955ca52f54
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
$ docker pull eclipse-temurin@sha256:1cf0ec009e9ec44b0e0f215bd7b433cc55746b56662aaf154b8980757f19f57c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **180.6 MB (180561489 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c94625821c5e613252d849b0b382c384cc07afadcf51815f358e23ece36c0dd5`
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
COPY dir:45c667d4bed394050d06fa644ce9574d9fe75c2ed92a12e23fb5b733428b21f6 in / 
# Wed, 23 Oct 2024 15:41:32 GMT
COPY file:b37d593713ee21ad52a4cd1424dc019a24f7966f85df0ac4b86d234302695328 in /etc/yum.repos.d/. 
# Wed, 23 Oct 2024 15:41:32 GMT
CMD ["/bin/bash"]
# Wed, 23 Oct 2024 15:41:32 GMT
RUN . /cachi2/cachi2.env &&     rm -rf /var/log/*
# Wed, 23 Oct 2024 15:41:32 GMT
LABEL "build-date"="2024-11-13T17:20:39" "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="8389cd46e6826a07db9fbf425dd110900e32c6f9" "build-date"="2024-11-13T17:16:40Z" "release"="1731518200"
# Wed, 23 Oct 2024 15:41:32 GMT
RUN /bin/sh
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
	-	`sha256:d2e5d6c907c71aea278da1e0e3424927afce03a253cba174efe5392fcba72b55`  
		Last Modified: Wed, 13 Nov 2024 18:56:52 GMT  
		Size: 39.9 MB (39871319 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7b6ec0388eddfe9b76df03c99092e0ca82d8a980895ea6ec4f7d925e674d7c5`  
		Last Modified: Wed, 13 Nov 2024 18:56:51 GMT  
		Size: 63.6 KB (63553 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4cec7d48dd02e679dcb4a0274046f5b6dc4f3c283b7c0c1fada1dc109c293b0`  
		Last Modified: Thu, 14 Nov 2024 21:17:08 GMT  
		Size: 37.0 MB (36989543 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c80b94e1ffbc830edfa0a4eadaf9e061e0a1ad2dac288915c84ce5815f40913`  
		Last Modified: Thu, 14 Nov 2024 21:17:09 GMT  
		Size: 103.6 MB (103634630 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4481e6c98622fb0c18285825498b066c2c9aa3c7a737a7dfc85e8a31a1e6080`  
		Last Modified: Thu, 14 Nov 2024 21:17:08 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:650662d1020ec98d629b31851ef81ee2526976875eb4aa195494d3c7a5d7ee38`  
		Last Modified: Thu, 14 Nov 2024 21:17:08 GMT  
		Size: 2.3 KB (2316 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:8-jdk-ubi9-minimal` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:f08c9d59831716415599f6756789c818c560c5855b5f707b9a7a61e334878744
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4943045 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f7d014c7d8f078fef008644591f92ce90ee3afb8f699526de0c84ee06af6d5d4`

```dockerfile
```

-	Layers:
	-	`sha256:1d782368c446a9ab1813d570dc80375610f9c37eaafbd2d21b1a625069d4d7f3`  
		Last Modified: Thu, 14 Nov 2024 21:17:08 GMT  
		Size: 4.9 MB (4922581 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ff4bc1711be2a7358a8cfbe2a6ddc026184db899ac2c22c5a9013e359c07b103`  
		Last Modified: Thu, 14 Nov 2024 21:17:08 GMT  
		Size: 20.5 KB (20464 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-temurin:8-jdk-ubi9-minimal` - linux; arm64 variant v8

```console
$ docker pull eclipse-temurin@sha256:ebee37e7fda5c656c68e8198ff2cd0414031573d6ccdc2b40b5f712aa1ed8a9d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **178.3 MB (178335476 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c9a9b3dd4153dbc74242e1e32732a11fb1302462f2b6ea846c34b9bfa4286816`
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
COPY dir:e27ddab6b88291890d801136d36e16fa6ad2af7f2a7e00f455a75bd89d96622f in / 
# Wed, 23 Oct 2024 15:41:32 GMT
COPY file:b37d593713ee21ad52a4cd1424dc019a24f7966f85df0ac4b86d234302695328 in /etc/yum.repos.d/. 
# Wed, 23 Oct 2024 15:41:32 GMT
CMD ["/bin/bash"]
# Wed, 23 Oct 2024 15:41:32 GMT
RUN . /cachi2/cachi2.env &&     rm -rf /var/log/*
# Wed, 23 Oct 2024 15:41:32 GMT
LABEL "build-date"="2024-11-13T17:24:29" "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="8389cd46e6826a07db9fbf425dd110900e32c6f9" "build-date"="2024-11-13T17:16:40Z" "release"="1731518200"
# Wed, 23 Oct 2024 15:41:32 GMT
RUN /bin/sh
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
	-	`sha256:636ce8d23eab8a4456a354f6ee07a387ed3d02c854cfe9deacc58ab7259339bf`  
		Last Modified: Wed, 13 Nov 2024 19:37:14 GMT  
		Size: 38.1 MB (38073783 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce756de279cd0aa23acc884e1d32ccff7fef4582b5922432ba03c8fe651a180b`  
		Last Modified: Wed, 13 Nov 2024 19:37:13 GMT  
		Size: 63.6 KB (63602 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b840ae373448a46eb9b3959fa1d0b67dac5393295e5dee28898b93570675096`  
		Last Modified: Thu, 14 Nov 2024 21:55:38 GMT  
		Size: 37.4 MB (37447275 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dfb22198328c5f21b792f1900e67dd53f18aedbc48dcf750e71d3c5469a7f04e`  
		Last Modified: Thu, 14 Nov 2024 21:55:39 GMT  
		Size: 102.7 MB (102748372 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee701eb92843bbe29f78abbd3bea8111c2a33608c2d9666255099b5e6a4eae25`  
		Last Modified: Thu, 14 Nov 2024 21:55:37 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:edd704841a5f201ce6eacf1765e3dcd9791751d2a2b6b7f85d6f8de9f434c9bd`  
		Last Modified: Thu, 14 Nov 2024 21:55:38 GMT  
		Size: 2.3 KB (2316 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:8-jdk-ubi9-minimal` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:737ce9218c8306ade4c8a324706659b27e217771393cc1da8bd6ad398ff749ca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4943135 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4502885e37f8fbc993fc79db3243a5a40fe7e8c5edaa1cba4e27bea9e59bc8de`

```dockerfile
```

-	Layers:
	-	`sha256:11d5e035b8c880844f45dedc02b8aae6f6a7a4bef6f846bfbdac6e9f4b253087`  
		Last Modified: Thu, 14 Nov 2024 21:55:37 GMT  
		Size: 4.9 MB (4922555 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ff64f3dc3cefdd9f305cd6d32e6b4fe09ebbe0fa21c3e9b819d7126f44809657`  
		Last Modified: Thu, 14 Nov 2024 21:55:37 GMT  
		Size: 20.6 KB (20580 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-temurin:8-jdk-ubi9-minimal` - linux; ppc64le

```console
$ docker pull eclipse-temurin@sha256:7c4998d7522251c3bc6634c010fb960410a0733c507844f49b45ef33227e518d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **185.0 MB (184976985 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b7c8fef9cfaa8df473d15248cf6f2cbb92606f1c213aa385ddbddc3b27163943`
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
COPY dir:6c2a5bc58c122f09d1fd3561f787b77c331815b22c12f8c67d609e22265d6d20 in / 
# Wed, 23 Oct 2024 15:41:32 GMT
COPY file:b37d593713ee21ad52a4cd1424dc019a24f7966f85df0ac4b86d234302695328 in /etc/yum.repos.d/. 
# Wed, 23 Oct 2024 15:41:32 GMT
CMD ["/bin/bash"]
# Wed, 23 Oct 2024 15:41:32 GMT
RUN . /cachi2/cachi2.env &&     rm -rf /var/log/*
# Wed, 23 Oct 2024 15:41:32 GMT
LABEL "build-date"="2024-11-13T18:14:04" "architecture"="ppc64le" "vcs-type"="git" "vcs-ref"="8389cd46e6826a07db9fbf425dd110900e32c6f9" "build-date"="2024-11-13T17:16:40Z" "release"="1731518200"
# Wed, 23 Oct 2024 15:41:32 GMT
RUN /bin/sh
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
	-	`sha256:68f9d27ca5ac31d5c0ec42759a142541ceb9cec644f734c3a9e0bcf6cbfc705c`  
		Last Modified: Thu, 14 Nov 2024 00:15:06 GMT  
		Size: 44.3 MB (44340470 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ec943cf70fba3160f966d46cdde1b9fce3e5b1924ead0008cface91354effac`  
		Last Modified: Thu, 14 Nov 2024 00:15:05 GMT  
		Size: 63.6 KB (63571 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72bcc9b1511e3e1fb956bc42694740f0ec50e8f1bb1d5b76848d9c232da2a240`  
		Last Modified: Thu, 14 Nov 2024 22:04:35 GMT  
		Size: 39.5 MB (39477961 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2aa9e372255269af67956397c586927a34d5f569c89aab02065fb96fa91d42d1`  
		Last Modified: Thu, 14 Nov 2024 22:04:37 GMT  
		Size: 101.1 MB (101092541 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3083e87121fc07d2d9db540fb29579c95ed9d7e015b1600de5f0180518b1474b`  
		Last Modified: Thu, 14 Nov 2024 22:04:35 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3404b943209f9d924b27bb5aacb211c60ac7c6bc6e71778e579215e03199bcb1`  
		Last Modified: Thu, 14 Nov 2024 22:04:36 GMT  
		Size: 2.3 KB (2314 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:8-jdk-ubi9-minimal` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:54971a82479ad6d5da85a5ea3ff2dccd1ea3f6a133c6675c84a82ff6070c00b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4941697 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:28436ba6dbf5757473e3e11bfcaa94278270b4f9ab46e974f657ca033c440ea4`

```dockerfile
```

-	Layers:
	-	`sha256:f1838098372ba2ff3702ff3d92ff214210bf5624e224bc10bbe2e420b95aca7b`  
		Last Modified: Thu, 14 Nov 2024 22:04:34 GMT  
		Size: 4.9 MB (4921198 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:987c4a21ea56ea5b7c22427584b3c41d8db62f5c4b75c086be3a295fa8c261a6`  
		Last Modified: Thu, 14 Nov 2024 22:04:34 GMT  
		Size: 20.5 KB (20499 bytes)  
		MIME: application/vnd.in-toto+json
