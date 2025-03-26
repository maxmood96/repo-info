## `eclipse-temurin:8u442-b06-jre-ubi9-minimal`

```console
$ docker pull eclipse-temurin@sha256:0cac3cdda9b40cd2a9a30d3a16def05032f136cfc9517ad0fe917690c1f015b2
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `eclipse-temurin:8u442-b06-jre-ubi9-minimal` - linux; amd64

```console
$ docker pull eclipse-temurin@sha256:68b209d94c03c8e72444dceca4bae9d3f2d9e84dbdd9c3f3d6380d5114869647
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.3 MB (94326748 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f544802f2255ddbab129487c021bf489a4ce17aa8697d0bb86fff1d3b6a34884`
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
ENV JAVA_VERSION=jdk8u442-b06
# Tue, 25 Mar 2025 17:58:27 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='730ed649ee973b7408cf7107e90576b67e8ed4b3aebb9e3e8a1056151f373152';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u442-b06/OpenJDK8U-jre_aarch64_linux_hotspot_8u442b06.tar.gz';          ;;        ppc64le)          ESUM='812ebf110f1d1cfc26a135368850064f96689e7918aa6bbac1c8f210fad5752f';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u442-b06/OpenJDK8U-jre_ppc64le_linux_hotspot_8u442b06.tar.gz';          ;;        x86_64)          ESUM='730fe33b1fc1f7da1e325d007b475d25a063850a167b548ea4bf689d4fcd867d';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u442-b06/OpenJDK8U-jre_x64_linux_hotspot_8u442b06.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz; # buildkit
# Tue, 25 Mar 2025 17:58:27 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java -version"; java -version;     echo "Complete." # buildkit
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
	-	`sha256:f91db7a27910da4a283f78d1ff95ee9dd2a54a0b80f058a24d2397d494160f2a`  
		Last Modified: Tue, 25 Mar 2025 21:57:24 GMT  
		Size: 13.1 MB (13088152 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5220cd17b9d5ee4ef590c69836daca9137ee0f65674e9b2886c61f08a5ba9ace`  
		Last Modified: Tue, 25 Mar 2025 21:57:25 GMT  
		Size: 41.9 MB (41876315 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13d8716e6c86bbada58153160053912a078d4703777142b2d1bcd51af84c63f4`  
		Last Modified: Tue, 25 Mar 2025 21:57:24 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:725c9c4b5773f354d4bd230f844815712c54bf192b574f65c34c127478af598f`  
		Last Modified: Tue, 25 Mar 2025 21:57:24 GMT  
		Size: 2.3 KB (2288 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:8u442-b06-jre-ubi9-minimal` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:efda1a53b13066d20f1cbee986b11b099ea45cae132f8377dbc4b06c05e96b04
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.7 MB (1682546 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eafae25482e4209718c3141e652d804b3d828c68aca157c936c90287aba28a60`

```dockerfile
```

-	Layers:
	-	`sha256:a8150a14b7b9c6c4f1fdcd124e1e25e7650b55afa8ca4c95a8055131b40d298f`  
		Last Modified: Tue, 25 Mar 2025 21:57:24 GMT  
		Size: 1.7 MB (1662416 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3096016a12a25a5ffb299449a9b6d943d5dc0d52bca5beb9b9bc00997451376c`  
		Last Modified: Tue, 25 Mar 2025 21:57:24 GMT  
		Size: 20.1 KB (20130 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-temurin:8u442-b06-jre-ubi9-minimal` - linux; arm64 variant v8

```console
$ docker pull eclipse-temurin@sha256:8f190a7501e422ae1beefa32ea7589655d394de8ea22ceb2df8e50400ada6539
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.1 MB (92093862 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b803af42ef86cd59f4998438ecffc3c9f2d9a2f151aff327f77d497e0ba163d8`
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
ENV JAVA_VERSION=jdk8u442-b06
# Tue, 25 Mar 2025 17:58:27 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='730ed649ee973b7408cf7107e90576b67e8ed4b3aebb9e3e8a1056151f373152';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u442-b06/OpenJDK8U-jre_aarch64_linux_hotspot_8u442b06.tar.gz';          ;;        ppc64le)          ESUM='812ebf110f1d1cfc26a135368850064f96689e7918aa6bbac1c8f210fad5752f';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u442-b06/OpenJDK8U-jre_ppc64le_linux_hotspot_8u442b06.tar.gz';          ;;        x86_64)          ESUM='730fe33b1fc1f7da1e325d007b475d25a063850a167b548ea4bf689d4fcd867d';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u442-b06/OpenJDK8U-jre_x64_linux_hotspot_8u442b06.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz; # buildkit
# Tue, 25 Mar 2025 17:58:27 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java -version"; java -version;     echo "Complete." # buildkit
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
	-	`sha256:2d762811691ad0237c9d8b597c07c43be1b6050e361dd62d8742be6aa9b1fa34`  
		Last Modified: Tue, 25 Mar 2025 21:58:07 GMT  
		Size: 40.9 MB (40876036 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b781305bf23c972ce9a224c93d7183b072a152fe3a3021be4149a10017ede68d`  
		Last Modified: Tue, 25 Mar 2025 21:58:05 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d50fa6618f11fe46873b614bdc460cba5690f355d3b20af9282062e00458546d`  
		Last Modified: Tue, 25 Mar 2025 21:58:05 GMT  
		Size: 2.3 KB (2290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:8u442-b06-jre-ubi9-minimal` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:200194eb71f4ebda2f320e918bd0a7590f94494c4bb2c45d2e2048e622731963
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.7 MB (1683753 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:61cc5fee848c1d1c0e63998dc597125c7ffd34840740fd88ef8d4a13ec336eee`

```dockerfile
```

-	Layers:
	-	`sha256:3c75699c315f7035fb89e8f286e4a2930ceb06c256036b95add952b78fd89f31`  
		Last Modified: Tue, 25 Mar 2025 21:58:05 GMT  
		Size: 1.7 MB (1663519 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:28f31521b601f238deb1e3542c15170263556ae9c1c2b29e53dfb8366434585b`  
		Last Modified: Tue, 25 Mar 2025 21:58:05 GMT  
		Size: 20.2 KB (20234 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-temurin:8u442-b06-jre-ubi9-minimal` - linux; ppc64le

```console
$ docker pull eclipse-temurin@sha256:26b32b85d9267127db7d05a3ca7c8ce67887d067bc991e7b2087985d2ecea13c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **99.7 MB (99746600 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e530755f6b37b3aef69b37b47ecb003e4be06ae49539c94d6249ccad02a4430a`
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
ENV JAVA_VERSION=jdk8u442-b06
# Tue, 25 Mar 2025 17:58:27 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='730ed649ee973b7408cf7107e90576b67e8ed4b3aebb9e3e8a1056151f373152';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u442-b06/OpenJDK8U-jre_aarch64_linux_hotspot_8u442b06.tar.gz';          ;;        ppc64le)          ESUM='812ebf110f1d1cfc26a135368850064f96689e7918aa6bbac1c8f210fad5752f';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u442-b06/OpenJDK8U-jre_ppc64le_linux_hotspot_8u442b06.tar.gz';          ;;        x86_64)          ESUM='730fe33b1fc1f7da1e325d007b475d25a063850a167b548ea4bf689d4fcd867d';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u442-b06/OpenJDK8U-jre_x64_linux_hotspot_8u442b06.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz; # buildkit
# Tue, 25 Mar 2025 17:58:27 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java -version"; java -version;     echo "Complete." # buildkit
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
	-	`sha256:df051c3c315bd478f4be3db9dec0bbe0b07ebbdf74e7b6d0978eeff0eb320217`  
		Last Modified: Tue, 25 Mar 2025 21:59:20 GMT  
		Size: 41.3 MB (41253811 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b66d0a142be212f4b0d7d33477e513912f19165205ed3483978c11662c40a76`  
		Last Modified: Tue, 25 Mar 2025 21:59:18 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:844d32e9b082626cc83ef98ce0b687084e009181fcaa79365b737ba312adab6d`  
		Last Modified: Tue, 25 Mar 2025 21:59:18 GMT  
		Size: 2.3 KB (2290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:8u442-b06-jre-ubi9-minimal` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:78a8cfefa3a4fac1c0cd679c520927429c7ab69b5a64d2ccd33a4805448df356
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.7 MB (1685507 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0de26b59a66185b0083f78960c780276de38306bce5aebcb79344d0d4f9c12a3`

```dockerfile
```

-	Layers:
	-	`sha256:7c92f315b197b3e6edf97631d39e0b35e39ebca814a018aa5899afd91330ee80`  
		Last Modified: Tue, 25 Mar 2025 21:59:18 GMT  
		Size: 1.7 MB (1665348 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d24fee21a5e78d8361ba0273cd4b9db3312dadbecc1eb34e6b482fd573a76e96`  
		Last Modified: Tue, 25 Mar 2025 21:59:18 GMT  
		Size: 20.2 KB (20159 bytes)  
		MIME: application/vnd.in-toto+json
