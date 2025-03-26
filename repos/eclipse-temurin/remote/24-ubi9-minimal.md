## `eclipse-temurin:24-ubi9-minimal`

```console
$ docker pull eclipse-temurin@sha256:62e032e903758c5b98a23e1ff1b7b54863d5af6df506f5089f1d8be64fb45ddd
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

### `eclipse-temurin:24-ubi9-minimal` - linux; amd64

```console
$ docker pull eclipse-temurin@sha256:6b6ccab69a851b3c5f320b09d7a6f9f75a84326d94e4a39b3d516e9884fd2c8a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **142.4 MB (142400434 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c1ecf8d2c6c156238431460f994ba27001fb52f167672b7870fb9742f1914242`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 13 Mar 2025 07:20:26 GMT
LABEL maintainer="Red Hat, Inc."
# Thu, 13 Mar 2025 07:20:26 GMT
LABEL vendor="Red Hat, Inc."
# Thu, 13 Mar 2025 07:20:26 GMT
LABEL url="https://www.redhat.com"
# Thu, 13 Mar 2025 07:20:26 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.5"       distribution-scope="public"
# Thu, 13 Mar 2025 07:20:26 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Thu, 13 Mar 2025 07:20:26 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Thu, 13 Mar 2025 07:20:27 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 13 Mar 2025 07:20:27 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 13 Mar 2025 07:20:27 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Thu, 13 Mar 2025 07:20:27 GMT
LABEL io.openshift.expose-services=""
# Thu, 13 Mar 2025 07:20:27 GMT
LABEL io.openshift.tags="minimal rhel9"
# Thu, 13 Mar 2025 07:20:27 GMT
ENV container oci
# Thu, 13 Mar 2025 07:20:27 GMT
COPY dir:15b23b07af120e2e0a5f4d490f44d738ca8fb631feddbf3564dd5d54104ea356 in / 
# Thu, 13 Mar 2025 07:20:27 GMT
COPY file:b37d593713ee21ad52a4cd1424dc019a24f7966f85df0ac4b86d234302695328 in /etc/yum.repos.d/. 
# Thu, 13 Mar 2025 07:20:27 GMT
CMD ["/bin/bash"]
# Thu, 13 Mar 2025 07:20:28 GMT
RUN . /cachi2/cachi2.env &&     rm -rf /var/log/*
# Thu, 13 Mar 2025 07:20:28 GMT
LABEL "build-date"="2025-03-13T07:20:00" "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="7865437f00d10c54ee1c3a6268b5ff65b38afba5" "build-date"="2025-03-13T07:15:09Z" "release"="1741850109"
# Thu, 13 Mar 2025 07:20:34 GMT
RUN /bin/sh
# Tue, 25 Mar 2025 17:58:27 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 25 Mar 2025 17:58:27 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 25 Mar 2025 17:58:27 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 25 Mar 2025 17:58:27 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en     ;     microdnf clean all # buildkit
# Tue, 25 Mar 2025 17:58:27 GMT
ENV JAVA_VERSION=jdk-24+36
# Tue, 25 Mar 2025 17:58:27 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='18071047526ab4b53131f9bb323e8703485ae37fcb2f2c5ef0f1b7bab66d1b94';          BINARY_URL='https://github.com/adoptium/temurin24-binaries/releases/download/jdk-24%2B36/OpenJDK24U-jdk_aarch64_linux_hotspot_24_36.tar.gz';          ;;        ppc64le)          ESUM='3a5641ab862a2bbae56886d4ec47f735052780bfe124df7aea2ca40e0f973b5a';          BINARY_URL='https://github.com/adoptium/temurin24-binaries/releases/download/jdk-24%2B36/OpenJDK24U-jdk_ppc64le_linux_hotspot_24_36.tar.gz';          ;;        s390x)          ESUM='e3149dc2ab1db0bdf86ab8d27a5ad67e32e30c829cef8a02628d36e5781f44ff';          BINARY_URL='https://github.com/adoptium/temurin24-binaries/releases/download/jdk-24%2B36/OpenJDK24U-jdk_s390x_linux_hotspot_24_36.tar.gz';          ;;        x86_64)          ESUM='c340dee97b6aa215d248bc196dcac5b56e7be9b5c5d45e691344d40d5d0b171d';          BINARY_URL='https://github.com/adoptium/temurin24-binaries/releases/download/jdk-24%2B36/OpenJDK24U-jdk_x64_linux_hotspot_24_36.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Tue, 25 Mar 2025 17:58:27 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 25 Mar 2025 17:58:27 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 25 Mar 2025 17:58:27 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 25 Mar 2025 17:58:27 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:533b69cfd644e5f3e5bde1a8c302567c595a28af93b9318ac6a3e9394740fb4d`  
		Last Modified: Thu, 13 Mar 2025 08:27:55 GMT  
		Size: 39.4 MB (39359404 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:863e9a7e21028fb223595c360e0b25839f814e468af01725b95defa89bd29b53`  
		Last Modified: Thu, 13 Mar 2025 08:27:58 GMT  
		Size: 461.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c901340f96bf8174457dcf8ad35f01da040909787fcafabfefad749ef4b8a24c`  
		Last Modified: Tue, 25 Mar 2025 21:57:52 GMT  
		Size: 13.1 MB (13088156 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df858e6116596bc536e3ce1abee5c532a085ee1115a284db31af4eb149976cb8`  
		Last Modified: Tue, 25 Mar 2025 21:57:54 GMT  
		Size: 89.9 MB (89949994 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3a4e60586fd16cf956f06997571646fac5e88378d8b0b4cce3b16750b128910`  
		Last Modified: Tue, 25 Mar 2025 21:57:52 GMT  
		Size: 130.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:299ac3d8ce843b8a28cbe00086b3b452e2dee123b4819f7fc12623332d458e65`  
		Last Modified: Tue, 25 Mar 2025 21:57:52 GMT  
		Size: 2.3 KB (2289 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:24-ubi9-minimal` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:26dd865de55b654e9ec371fa083909f51cba59119810c1561f6544ea38938bb7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.7 MB (1689238 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:12afe4786a7b629fe6119596cf1e746a11d5683b97a47d7da8682c385160eed6`

```dockerfile
```

-	Layers:
	-	`sha256:57695d4d9fd6dea95309ea898b099bc66da52e266063a885ef339881e0316545`  
		Last Modified: Tue, 25 Mar 2025 21:57:52 GMT  
		Size: 1.7 MB (1667410 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1cd550358f09a80310c02f0cbee3ad8ff1b52d3b4c712374176d752d0f92ca86`  
		Last Modified: Tue, 25 Mar 2025 21:57:52 GMT  
		Size: 21.8 KB (21828 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-temurin:24-ubi9-minimal` - linux; arm64 variant v8

```console
$ docker pull eclipse-temurin@sha256:d73c29d7dd61362d0894b2b24ee896aec7dfed7e8f6b34f17ad854ee8d1de096
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **140.3 MB (140311740 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ffdb7348f1d3f910dbd3b45758944a5b7a1d8a0ba008c8069551401944929579`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 13 Mar 2025 07:22:24 GMT
LABEL maintainer="Red Hat, Inc."
# Thu, 13 Mar 2025 07:22:24 GMT
LABEL vendor="Red Hat, Inc."
# Thu, 13 Mar 2025 07:22:24 GMT
LABEL url="https://www.redhat.com"
# Thu, 13 Mar 2025 07:22:24 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.5"       distribution-scope="public"
# Thu, 13 Mar 2025 07:22:24 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Thu, 13 Mar 2025 07:22:24 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Thu, 13 Mar 2025 07:22:24 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 13 Mar 2025 07:22:24 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 13 Mar 2025 07:22:24 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Thu, 13 Mar 2025 07:22:24 GMT
LABEL io.openshift.expose-services=""
# Thu, 13 Mar 2025 07:22:24 GMT
LABEL io.openshift.tags="minimal rhel9"
# Thu, 13 Mar 2025 07:22:24 GMT
ENV container oci
# Thu, 13 Mar 2025 07:22:25 GMT
COPY dir:b7138ac36fc7710c19e28655d453b8712ae774de42fbfc7d7975b03b9664b7ae in / 
# Thu, 13 Mar 2025 07:22:25 GMT
COPY file:b37d593713ee21ad52a4cd1424dc019a24f7966f85df0ac4b86d234302695328 in /etc/yum.repos.d/. 
# Thu, 13 Mar 2025 07:22:25 GMT
CMD ["/bin/bash"]
# Thu, 13 Mar 2025 07:22:25 GMT
RUN . /cachi2/cachi2.env &&     rm -rf /var/log/*
# Thu, 13 Mar 2025 07:22:26 GMT
LABEL "build-date"="2025-03-13T07:21:58" "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="7865437f00d10c54ee1c3a6268b5ff65b38afba5" "build-date"="2025-03-13T07:15:09Z" "release"="1741850109"
# Thu, 13 Mar 2025 07:22:36 GMT
RUN /bin/sh
# Tue, 25 Mar 2025 17:58:27 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 25 Mar 2025 17:58:27 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 25 Mar 2025 17:58:27 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 25 Mar 2025 17:58:27 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en     ;     microdnf clean all # buildkit
# Tue, 25 Mar 2025 17:58:27 GMT
ENV JAVA_VERSION=jdk-24+36
# Tue, 25 Mar 2025 17:58:27 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='18071047526ab4b53131f9bb323e8703485ae37fcb2f2c5ef0f1b7bab66d1b94';          BINARY_URL='https://github.com/adoptium/temurin24-binaries/releases/download/jdk-24%2B36/OpenJDK24U-jdk_aarch64_linux_hotspot_24_36.tar.gz';          ;;        ppc64le)          ESUM='3a5641ab862a2bbae56886d4ec47f735052780bfe124df7aea2ca40e0f973b5a';          BINARY_URL='https://github.com/adoptium/temurin24-binaries/releases/download/jdk-24%2B36/OpenJDK24U-jdk_ppc64le_linux_hotspot_24_36.tar.gz';          ;;        s390x)          ESUM='e3149dc2ab1db0bdf86ab8d27a5ad67e32e30c829cef8a02628d36e5781f44ff';          BINARY_URL='https://github.com/adoptium/temurin24-binaries/releases/download/jdk-24%2B36/OpenJDK24U-jdk_s390x_linux_hotspot_24_36.tar.gz';          ;;        x86_64)          ESUM='c340dee97b6aa215d248bc196dcac5b56e7be9b5c5d45e691344d40d5d0b171d';          BINARY_URL='https://github.com/adoptium/temurin24-binaries/releases/download/jdk-24%2B36/OpenJDK24U-jdk_x64_linux_hotspot_24_36.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Tue, 25 Mar 2025 17:58:27 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 25 Mar 2025 17:58:27 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 25 Mar 2025 17:58:27 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 25 Mar 2025 17:58:27 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:8f0b1160a7bdb1abc6f59217ba0a1ed1eb53a9ddbbcaddd95d709604e095f742`  
		Last Modified: Thu, 13 Mar 2025 08:37:12 GMT  
		Size: 37.6 MB (37590719 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2e019691d61a0d5163ed02fe7a0cee4161254fd2d91b44221c46f8f765e011b`  
		Last Modified: Thu, 13 Mar 2025 08:37:13 GMT  
		Size: 459.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cecaa9a0e7b9e986580faf82cb0f61b4b374585587485ca9f2f92ea54752543`  
		Last Modified: Tue, 25 Mar 2025 21:57:40 GMT  
		Size: 13.6 MB (13624229 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d22bf9ccf2dd2fc55bb878e8e30b39700a02d4d6a32d89eff2365a01cd6d31c`  
		Last Modified: Tue, 25 Mar 2025 22:04:36 GMT  
		Size: 89.1 MB (89093912 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a368d8b24a8259d26f9d772725209ca18767110ea7014738b8c56c9d61d06977`  
		Last Modified: Tue, 25 Mar 2025 22:04:33 GMT  
		Size: 131.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d6c0e387fa31c7c487632cc678738aa778265c569a21e1bbe9e41e31648300e`  
		Last Modified: Tue, 25 Mar 2025 22:04:33 GMT  
		Size: 2.3 KB (2290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:24-ubi9-minimal` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:96cda1d980a2a7a4451634676905e78d5d16eebf60e7726cd7ddf1b7bb87d14d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.7 MB (1689776 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b21fab6c08b5fff006c34d0ed39a35b8898c60333da989112b2eded16d80f4c5`

```dockerfile
```

-	Layers:
	-	`sha256:821444fb66b2dd3bbdbb9e64b892ff03013b4cc1e03a20659c8015123d77c9d8`  
		Last Modified: Tue, 25 Mar 2025 22:04:33 GMT  
		Size: 1.7 MB (1667832 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b5b2545a093e79b43d44eb3064e4a80bd31144a2851efb62a62097ac72ef31ba`  
		Last Modified: Tue, 25 Mar 2025 22:04:33 GMT  
		Size: 21.9 KB (21944 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-temurin:24-ubi9-minimal` - linux; ppc64le

```console
$ docker pull eclipse-temurin@sha256:cbc7c1633148781228c9bd0089509afc51501180718d2b0e02dbe4ac7c26973d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **148.4 MB (148415428 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ebe9ff8008d75cef6a19a23036492e64ad272b20e9c408b98a12d0d452c6685`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 13 Mar 2025 07:27:04 GMT
LABEL maintainer="Red Hat, Inc."
# Thu, 13 Mar 2025 07:27:04 GMT
LABEL vendor="Red Hat, Inc."
# Thu, 13 Mar 2025 07:27:04 GMT
LABEL url="https://www.redhat.com"
# Thu, 13 Mar 2025 07:27:04 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.5"       distribution-scope="public"
# Thu, 13 Mar 2025 07:27:04 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Thu, 13 Mar 2025 07:27:04 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Thu, 13 Mar 2025 07:27:04 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 13 Mar 2025 07:27:04 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 13 Mar 2025 07:27:04 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Thu, 13 Mar 2025 07:27:04 GMT
LABEL io.openshift.expose-services=""
# Thu, 13 Mar 2025 07:27:04 GMT
LABEL io.openshift.tags="minimal rhel9"
# Thu, 13 Mar 2025 07:27:04 GMT
ENV container oci
# Thu, 13 Mar 2025 07:27:05 GMT
COPY dir:2930069cafd499c2bb484a4452129437fee8075431fe0148ba9db5d528b083c7 in / 
# Thu, 13 Mar 2025 07:27:05 GMT
COPY file:b37d593713ee21ad52a4cd1424dc019a24f7966f85df0ac4b86d234302695328 in /etc/yum.repos.d/. 
# Thu, 13 Mar 2025 07:27:05 GMT
CMD ["/bin/bash"]
# Thu, 13 Mar 2025 07:27:05 GMT
RUN . /cachi2/cachi2.env &&     rm -rf /var/log/*
# Thu, 13 Mar 2025 07:27:06 GMT
LABEL "build-date"="2025-03-13T07:26:37" "architecture"="ppc64le" "vcs-type"="git" "vcs-ref"="7865437f00d10c54ee1c3a6268b5ff65b38afba5" "build-date"="2025-03-13T07:15:09Z" "release"="1741850109"
# Thu, 13 Mar 2025 07:28:01 GMT
RUN /bin/sh
# Tue, 25 Mar 2025 17:58:27 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 25 Mar 2025 17:58:27 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 25 Mar 2025 17:58:27 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 25 Mar 2025 17:58:27 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en     ;     microdnf clean all # buildkit
# Tue, 25 Mar 2025 17:58:27 GMT
ENV JAVA_VERSION=jdk-24+36
# Tue, 25 Mar 2025 17:58:27 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='18071047526ab4b53131f9bb323e8703485ae37fcb2f2c5ef0f1b7bab66d1b94';          BINARY_URL='https://github.com/adoptium/temurin24-binaries/releases/download/jdk-24%2B36/OpenJDK24U-jdk_aarch64_linux_hotspot_24_36.tar.gz';          ;;        ppc64le)          ESUM='3a5641ab862a2bbae56886d4ec47f735052780bfe124df7aea2ca40e0f973b5a';          BINARY_URL='https://github.com/adoptium/temurin24-binaries/releases/download/jdk-24%2B36/OpenJDK24U-jdk_ppc64le_linux_hotspot_24_36.tar.gz';          ;;        s390x)          ESUM='e3149dc2ab1db0bdf86ab8d27a5ad67e32e30c829cef8a02628d36e5781f44ff';          BINARY_URL='https://github.com/adoptium/temurin24-binaries/releases/download/jdk-24%2B36/OpenJDK24U-jdk_s390x_linux_hotspot_24_36.tar.gz';          ;;        x86_64)          ESUM='c340dee97b6aa215d248bc196dcac5b56e7be9b5c5d45e691344d40d5d0b171d';          BINARY_URL='https://github.com/adoptium/temurin24-binaries/releases/download/jdk-24%2B36/OpenJDK24U-jdk_x64_linux_hotspot_24_36.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Tue, 25 Mar 2025 17:58:27 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 25 Mar 2025 17:58:27 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 25 Mar 2025 17:58:27 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 25 Mar 2025 17:58:27 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:45bd43bfc7accd96f346d44555dfd3c49fe61e223a5edc723f7e6e800686210b`  
		Last Modified: Thu, 13 Mar 2025 12:28:04 GMT  
		Size: 43.8 MB (43765030 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8dd5893f1906dca44bb5215e6c9cec6ab4d26c1be7354e08d4a40339ea1bd0ad`  
		Last Modified: Thu, 13 Mar 2025 12:28:03 GMT  
		Size: 459.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:914af573e0553dbd0d38d7286a66c85ce9c38d0316f769a5f0399abff06eab9e`  
		Last Modified: Tue, 25 Mar 2025 21:58:18 GMT  
		Size: 14.7 MB (14724882 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a133bc1bccab6313cbbca9491b56d97316a754520a33e80fd7127e924957b608`  
		Last Modified: Tue, 25 Mar 2025 22:09:13 GMT  
		Size: 89.9 MB (89922635 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35f09b12aac624ef0b449113528e265644511eb82c15494e739b033f96ab6fb2`  
		Last Modified: Tue, 25 Mar 2025 22:09:10 GMT  
		Size: 131.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c68f75af0723a24268ace5850953da967c58fcc0ca3b991b0602d4440bd34bc3`  
		Last Modified: Tue, 25 Mar 2025 22:09:10 GMT  
		Size: 2.3 KB (2291 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:24-ubi9-minimal` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:9588a14435fdc62323099686bacc116f9c369176181c90acfa91258175def91d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.7 MB (1690901 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:080be2872620ceac667a61c59ff5bf62fee1fcd3ded595f5c88ff8bfb9bc5974`

```dockerfile
```

-	Layers:
	-	`sha256:20d276c94448c923347c38f3719cb7e62ece7394737f20857c96b0f6ea16e65b`  
		Last Modified: Tue, 25 Mar 2025 22:09:10 GMT  
		Size: 1.7 MB (1669037 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b480632ad250ab057838c71f3ed64880d489a5bde8913600c1e4fd75b4140200`  
		Last Modified: Tue, 25 Mar 2025 22:09:10 GMT  
		Size: 21.9 KB (21864 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-temurin:24-ubi9-minimal` - linux; s390x

```console
$ docker pull eclipse-temurin@sha256:234d49f5b37a43cd3ef099900db7503ee2ebb75d0c4e9c7416acc875fbad5201
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **136.2 MB (136177733 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:27c17f2d3d75706dd4d17d706ea6b70e893b907ae8eff1acdcd1c354c05a9c31`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 13 Mar 2025 07:26:20 GMT
LABEL maintainer="Red Hat, Inc."
# Thu, 13 Mar 2025 07:26:20 GMT
LABEL vendor="Red Hat, Inc."
# Thu, 13 Mar 2025 07:26:20 GMT
LABEL url="https://www.redhat.com"
# Thu, 13 Mar 2025 07:26:20 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.5"       distribution-scope="public"
# Thu, 13 Mar 2025 07:26:20 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Thu, 13 Mar 2025 07:26:20 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Thu, 13 Mar 2025 07:26:20 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 13 Mar 2025 07:26:20 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 13 Mar 2025 07:26:20 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Thu, 13 Mar 2025 07:26:20 GMT
LABEL io.openshift.expose-services=""
# Thu, 13 Mar 2025 07:26:20 GMT
LABEL io.openshift.tags="minimal rhel9"
# Thu, 13 Mar 2025 07:26:20 GMT
ENV container oci
# Thu, 13 Mar 2025 07:26:21 GMT
COPY dir:0bd2f8345c36703c483db0ee0404e33109a312f452aed24ac4080629e2197763 in / 
# Thu, 13 Mar 2025 07:26:21 GMT
COPY file:b37d593713ee21ad52a4cd1424dc019a24f7966f85df0ac4b86d234302695328 in /etc/yum.repos.d/. 
# Thu, 13 Mar 2025 07:26:21 GMT
CMD ["/bin/bash"]
# Thu, 13 Mar 2025 07:26:21 GMT
RUN . /cachi2/cachi2.env &&     rm -rf /var/log/*
# Thu, 13 Mar 2025 07:26:21 GMT
LABEL "build-date"="2025-03-13T07:25:32" "architecture"="s390x" "vcs-type"="git" "vcs-ref"="7865437f00d10c54ee1c3a6268b5ff65b38afba5" "build-date"="2025-03-13T07:15:09Z" "release"="1741850109"
# Thu, 13 Mar 2025 07:26:33 GMT
RUN /bin/sh
# Tue, 25 Mar 2025 17:58:27 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 25 Mar 2025 17:58:27 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 25 Mar 2025 17:58:27 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 25 Mar 2025 17:58:27 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en     ;     microdnf clean all # buildkit
# Tue, 25 Mar 2025 17:58:27 GMT
ENV JAVA_VERSION=jdk-24+36
# Tue, 25 Mar 2025 17:58:27 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='18071047526ab4b53131f9bb323e8703485ae37fcb2f2c5ef0f1b7bab66d1b94';          BINARY_URL='https://github.com/adoptium/temurin24-binaries/releases/download/jdk-24%2B36/OpenJDK24U-jdk_aarch64_linux_hotspot_24_36.tar.gz';          ;;        ppc64le)          ESUM='3a5641ab862a2bbae56886d4ec47f735052780bfe124df7aea2ca40e0f973b5a';          BINARY_URL='https://github.com/adoptium/temurin24-binaries/releases/download/jdk-24%2B36/OpenJDK24U-jdk_ppc64le_linux_hotspot_24_36.tar.gz';          ;;        s390x)          ESUM='e3149dc2ab1db0bdf86ab8d27a5ad67e32e30c829cef8a02628d36e5781f44ff';          BINARY_URL='https://github.com/adoptium/temurin24-binaries/releases/download/jdk-24%2B36/OpenJDK24U-jdk_s390x_linux_hotspot_24_36.tar.gz';          ;;        x86_64)          ESUM='c340dee97b6aa215d248bc196dcac5b56e7be9b5c5d45e691344d40d5d0b171d';          BINARY_URL='https://github.com/adoptium/temurin24-binaries/releases/download/jdk-24%2B36/OpenJDK24U-jdk_x64_linux_hotspot_24_36.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Tue, 25 Mar 2025 17:58:27 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 25 Mar 2025 17:58:27 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 25 Mar 2025 17:58:27 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 25 Mar 2025 17:58:27 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:5c803ecc47a0d9d9d66bd6164bdefc7148562b976f8369af7f3ec1cc62c37cca`  
		Last Modified: Thu, 13 Mar 2025 12:27:57 GMT  
		Size: 37.5 MB (37504197 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:094529012ae62f39a61b16721406ec6b3762288ce40141f72e6917263ab122de`  
		Last Modified: Thu, 13 Mar 2025 12:27:56 GMT  
		Size: 458.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3eb8106808808f1d5a5b735787511265d305fd4624296a16f2d1eb222401d55a`  
		Last Modified: Tue, 25 Mar 2025 21:57:55 GMT  
		Size: 13.4 MB (13446471 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f3a5f0a0397e16796350f730245f922c55af54cdaf3504ed7f059e07208cec9`  
		Last Modified: Tue, 25 Mar 2025 22:04:21 GMT  
		Size: 85.2 MB (85224188 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8505fd9c6ad5da7063895f614a5f90e6e637b651ec42f4465a03be68352f5b9`  
		Last Modified: Tue, 25 Mar 2025 22:04:19 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1dad62e710d75d4f30ddb685c651e87f4aa14501e6e86401a2d0f439454f0ff4`  
		Last Modified: Tue, 25 Mar 2025 22:04:19 GMT  
		Size: 2.3 KB (2291 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:24-ubi9-minimal` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:c7413ddd9c0449de859fc35490800056802fc0422477c0cc594a682b17cfe63a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.7 MB (1690873 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e7170a74b446c48f3114da65f315a97bb46d317b315c2df94006df56da0b138`

```dockerfile
```

-	Layers:
	-	`sha256:03532b400120404e48558705f1b2c08413a6ff164c0a966af954724d5d947268`  
		Last Modified: Tue, 25 Mar 2025 22:04:19 GMT  
		Size: 1.7 MB (1669045 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:66d1d53e9682ca277c634fe28686ac33d1b0b28e77c302c5d8b3bc46124d65c8`  
		Last Modified: Tue, 25 Mar 2025 22:04:19 GMT  
		Size: 21.8 KB (21828 bytes)  
		MIME: application/vnd.in-toto+json
