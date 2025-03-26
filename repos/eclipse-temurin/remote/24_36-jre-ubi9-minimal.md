## `eclipse-temurin:24_36-jre-ubi9-minimal`

```console
$ docker pull eclipse-temurin@sha256:48332a6ab43a8284977220bf08044f32a684129eaddc754a1b1b081b5172b15c
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

### `eclipse-temurin:24_36-jre-ubi9-minimal` - linux; amd64

```console
$ docker pull eclipse-temurin@sha256:409634d84baf09c14fea289b54f24cfb6eb342d88dc76f6a6969a7335207f14c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **113.3 MB (113276248 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:da960bc8531621a9cce4194affe8afd520587d39167bf71ae05d4a796d81aa1a`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`

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
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='782a46008490272affe0b797155c2ae8e759e10c8ba4540f1f7285ef3d2902de';          BINARY_URL='https://github.com/adoptium/temurin24-binaries/releases/download/jdk-24%2B36/OpenJDK24U-jre_aarch64_linux_hotspot_24_36.tar.gz';          ;;        ppc64le)          ESUM='e7c90ab80d5e9419f794aee63c8f1bf3ed29e656d4e8e967a45d3069bd643c07';          BINARY_URL='https://github.com/adoptium/temurin24-binaries/releases/download/jdk-24%2B36/OpenJDK24U-jre_ppc64le_linux_hotspot_24_36.tar.gz';          ;;        s390x)          ESUM='65a9a1e685b81bf80d89a5b45d5f49655e938f3e175accf98c2cb13df07753fd';          BINARY_URL='https://github.com/adoptium/temurin24-binaries/releases/download/jdk-24%2B36/OpenJDK24U-jre_s390x_linux_hotspot_24_36.tar.gz';          ;;        x86_64)          ESUM='e8d8f5707d765a6bfca3de61320e0bb2618191c77947bc467ac5021e6193f351';          BINARY_URL='https://github.com/adoptium/temurin24-binaries/releases/download/jdk-24%2B36/OpenJDK24U-jre_x64_linux_hotspot_24_36.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz; # buildkit
# Tue, 25 Mar 2025 17:58:27 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 25 Mar 2025 17:58:27 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 25 Mar 2025 17:58:27 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
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
	-	`sha256:930794ddcffc1c3002923419bc00b9740a77ddde28ec5c1e22b9f32c29cde0c0`  
		Last Modified: Tue, 25 Mar 2025 21:57:39 GMT  
		Size: 13.1 MB (13088126 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c82490968a3919c253f81e9ee62030bbf84a1c537a0e2e3b36bd046252348b5`  
		Last Modified: Tue, 25 Mar 2025 21:57:40 GMT  
		Size: 60.8 MB (60825837 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c054c16ec1e9c552baa0cb653cef0dce09bd3582d6b9e9c7198def3bae38047f`  
		Last Modified: Tue, 25 Mar 2025 21:57:38 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:581e5b6854ea0421864c074a17f5e210ede98dabca62aa4356edf55c0b6edf55`  
		Last Modified: Tue, 25 Mar 2025 21:57:38 GMT  
		Size: 2.3 KB (2292 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:24_36-jre-ubi9-minimal` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:19d5d696d606a80346ce5eeb1f354f69524c818658148399577041cf6faafcf6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.7 MB (1662598 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7869d71ec38af5beabd77e71bc0ac0d56fe5ded5998d7769a2624396aa46d272`

```dockerfile
```

-	Layers:
	-	`sha256:a57b304a03778171cbb0185f0beae17be2605dab385f9759f8de6c24f3331bf3`  
		Last Modified: Tue, 25 Mar 2025 21:57:38 GMT  
		Size: 1.6 MB (1641726 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ebaaaf3e6673cfc41f2cd477ea1810e3858026d6afd8dd200e9be2b733242566`  
		Last Modified: Tue, 25 Mar 2025 21:57:38 GMT  
		Size: 20.9 KB (20872 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-temurin:24_36-jre-ubi9-minimal` - linux; arm64 variant v8

```console
$ docker pull eclipse-temurin@sha256:42535499ffed3d208223d58c9f0c88b2055b9d2f1acebdcbbdb931eba068bae6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **111.1 MB (111101109 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c8bca2de61dae624625ab8f5173a1d30ee50b0f4c1f4d48df67fefc0935dd371`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`

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
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='782a46008490272affe0b797155c2ae8e759e10c8ba4540f1f7285ef3d2902de';          BINARY_URL='https://github.com/adoptium/temurin24-binaries/releases/download/jdk-24%2B36/OpenJDK24U-jre_aarch64_linux_hotspot_24_36.tar.gz';          ;;        ppc64le)          ESUM='e7c90ab80d5e9419f794aee63c8f1bf3ed29e656d4e8e967a45d3069bd643c07';          BINARY_URL='https://github.com/adoptium/temurin24-binaries/releases/download/jdk-24%2B36/OpenJDK24U-jre_ppc64le_linux_hotspot_24_36.tar.gz';          ;;        s390x)          ESUM='65a9a1e685b81bf80d89a5b45d5f49655e938f3e175accf98c2cb13df07753fd';          BINARY_URL='https://github.com/adoptium/temurin24-binaries/releases/download/jdk-24%2B36/OpenJDK24U-jre_s390x_linux_hotspot_24_36.tar.gz';          ;;        x86_64)          ESUM='e8d8f5707d765a6bfca3de61320e0bb2618191c77947bc467ac5021e6193f351';          BINARY_URL='https://github.com/adoptium/temurin24-binaries/releases/download/jdk-24%2B36/OpenJDK24U-jre_x64_linux_hotspot_24_36.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz; # buildkit
# Tue, 25 Mar 2025 17:58:27 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 25 Mar 2025 17:58:27 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 25 Mar 2025 17:58:27 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
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
	-	`sha256:586eb7d2a4a2439ce30079252a7a434fc249f8447fd2f263f498443a9fbc693c`  
		Last Modified: Tue, 25 Mar 2025 22:07:12 GMT  
		Size: 59.9 MB (59883282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:760438ca6c6f8c9ce6a249c86904717143f9e06bce9f4726ef219f1dbf51d288`  
		Last Modified: Tue, 25 Mar 2025 22:07:11 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be20d5870c145777521055d7efac99a43cb10aeac45904bf92033f2125172584`  
		Last Modified: Tue, 25 Mar 2025 22:07:11 GMT  
		Size: 2.3 KB (2291 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:24_36-jre-ubi9-minimal` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:f608591d5157f2edc1b37cca16ee0ec5401eeefe116f27a782cd1c7847f8b08a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.7 MB (1663113 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3576a97eae9de17a42e59aba95f82b7640470b0826b44eb4044f3bf23a8ad5b`

```dockerfile
```

-	Layers:
	-	`sha256:50fee44664d8dc3de96af5126c88cdbd3af85ff879b3b47d38dcaa058fcecf8a`  
		Last Modified: Tue, 25 Mar 2025 22:07:11 GMT  
		Size: 1.6 MB (1642136 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:da6b17d0080b0ab91c1f988dc5fc01970d1aa1693c105b882606da818dbe8071`  
		Last Modified: Tue, 25 Mar 2025 22:07:10 GMT  
		Size: 21.0 KB (20977 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-temurin:24_36-jre-ubi9-minimal` - linux; ppc64le

```console
$ docker pull eclipse-temurin@sha256:f1c30fc07d83a9393fc9bf3385c9eca59eeefae0fe8d6442ae88c9141378a7cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **119.2 MB (119159891 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc5ae5083344fae5a148aac49c4f1e84e8cc57483f3de67d5aac428bca89b5bf`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`

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
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='782a46008490272affe0b797155c2ae8e759e10c8ba4540f1f7285ef3d2902de';          BINARY_URL='https://github.com/adoptium/temurin24-binaries/releases/download/jdk-24%2B36/OpenJDK24U-jre_aarch64_linux_hotspot_24_36.tar.gz';          ;;        ppc64le)          ESUM='e7c90ab80d5e9419f794aee63c8f1bf3ed29e656d4e8e967a45d3069bd643c07';          BINARY_URL='https://github.com/adoptium/temurin24-binaries/releases/download/jdk-24%2B36/OpenJDK24U-jre_ppc64le_linux_hotspot_24_36.tar.gz';          ;;        s390x)          ESUM='65a9a1e685b81bf80d89a5b45d5f49655e938f3e175accf98c2cb13df07753fd';          BINARY_URL='https://github.com/adoptium/temurin24-binaries/releases/download/jdk-24%2B36/OpenJDK24U-jre_s390x_linux_hotspot_24_36.tar.gz';          ;;        x86_64)          ESUM='e8d8f5707d765a6bfca3de61320e0bb2618191c77947bc467ac5021e6193f351';          BINARY_URL='https://github.com/adoptium/temurin24-binaries/releases/download/jdk-24%2B36/OpenJDK24U-jre_x64_linux_hotspot_24_36.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz; # buildkit
# Tue, 25 Mar 2025 17:58:27 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 25 Mar 2025 17:58:27 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 25 Mar 2025 17:58:27 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
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
	-	`sha256:53aaf5bc4187e57205eb8086bcad2196e0e5dcac7ba498e55c5a6b2b4d37a510`  
		Last Modified: Tue, 25 Mar 2025 22:11:22 GMT  
		Size: 60.7 MB (60667102 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd998ee612415dd4294aed79946755742a0ec639c9476b4058ea1df8b5eea0a2`  
		Last Modified: Tue, 25 Mar 2025 22:11:20 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d6f55c6a32190c924df45f1be88f53fcf14a7e6c8d865c0ee9864a379654491`  
		Last Modified: Tue, 25 Mar 2025 22:11:20 GMT  
		Size: 2.3 KB (2291 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:24_36-jre-ubi9-minimal` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:ce24f9804a23d56f3acc25855eea812f3b0400e9599b8a1dd9884b1723279b82
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.7 MB (1664249 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:542584499418049a5443f53e5ab3a36567ba4787a85697837ef10232914922cc`

```dockerfile
```

-	Layers:
	-	`sha256:ab995c398c8aee0602cb04170eb9a5a82757e689eb77ced2110ac0fd3b3e6f90`  
		Last Modified: Tue, 25 Mar 2025 22:11:20 GMT  
		Size: 1.6 MB (1643347 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9230fc45c8d7c4cc424aed82065fefe72d73c902419627f5a96534d04c7add8a`  
		Last Modified: Tue, 25 Mar 2025 22:11:20 GMT  
		Size: 20.9 KB (20902 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-temurin:24_36-jre-ubi9-minimal` - linux; s390x

```console
$ docker pull eclipse-temurin@sha256:7b72c39b519c9804e720911ab68486cc5ad9c581c1cc83ebadc7bfa1bf2d3a8d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **108.6 MB (108555306 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:842b570639b308d27e7db11499124c396e02cbf2b917528b9e8162737d4cdf94`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`

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
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='782a46008490272affe0b797155c2ae8e759e10c8ba4540f1f7285ef3d2902de';          BINARY_URL='https://github.com/adoptium/temurin24-binaries/releases/download/jdk-24%2B36/OpenJDK24U-jre_aarch64_linux_hotspot_24_36.tar.gz';          ;;        ppc64le)          ESUM='e7c90ab80d5e9419f794aee63c8f1bf3ed29e656d4e8e967a45d3069bd643c07';          BINARY_URL='https://github.com/adoptium/temurin24-binaries/releases/download/jdk-24%2B36/OpenJDK24U-jre_ppc64le_linux_hotspot_24_36.tar.gz';          ;;        s390x)          ESUM='65a9a1e685b81bf80d89a5b45d5f49655e938f3e175accf98c2cb13df07753fd';          BINARY_URL='https://github.com/adoptium/temurin24-binaries/releases/download/jdk-24%2B36/OpenJDK24U-jre_s390x_linux_hotspot_24_36.tar.gz';          ;;        x86_64)          ESUM='e8d8f5707d765a6bfca3de61320e0bb2618191c77947bc467ac5021e6193f351';          BINARY_URL='https://github.com/adoptium/temurin24-binaries/releases/download/jdk-24%2B36/OpenJDK24U-jre_x64_linux_hotspot_24_36.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz; # buildkit
# Tue, 25 Mar 2025 17:58:27 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 25 Mar 2025 17:58:27 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 25 Mar 2025 17:58:27 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
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
	-	`sha256:f732d2377b830bd789ef6c22b88088b4169c1304e1c2f33cf6893227e1c6a6ce`  
		Last Modified: Tue, 25 Mar 2025 22:06:03 GMT  
		Size: 57.6 MB (57601760 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed4945c99391c851db72bae8821a03223413f31ff01dd6ac10f7364cc5841083`  
		Last Modified: Tue, 25 Mar 2025 22:06:02 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c57e88f53376102767029f2c0388c9784bfc5c9ca7034b939ec9d66f0a9a9d24`  
		Last Modified: Tue, 25 Mar 2025 22:06:02 GMT  
		Size: 2.3 KB (2292 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:24_36-jre-ubi9-minimal` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:ab559d499b9c547f9057bb01b46ffef9c487d3e8be19ca2c3039470ebadcb610
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.7 MB (1665465 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d5a37b94e76988c5b4a67a3ac8316d64e309caae0b037cbe1ff8ede2dfb07db3`

```dockerfile
```

-	Layers:
	-	`sha256:84ba1d7c16523041196c73174b822309aa18723414871791f05b8f3c43fb2f68`  
		Last Modified: Tue, 25 Mar 2025 22:06:02 GMT  
		Size: 1.6 MB (1644592 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:60cb420be053d7f617492db1dd2354f834b3ef587d411ee236122d22592290d8`  
		Last Modified: Tue, 25 Mar 2025 22:06:02 GMT  
		Size: 20.9 KB (20873 bytes)  
		MIME: application/vnd.in-toto+json
