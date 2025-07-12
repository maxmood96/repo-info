## `eclipse-temurin:8-jre-ubi9-minimal`

```console
$ docker pull eclipse-temurin@sha256:dfed5bf280442a1f50e1451a85f9bbfdadd8580a7c437ec4086175181a613a22
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `eclipse-temurin:8-jre-ubi9-minimal` - linux; amd64

```console
$ docker pull eclipse-temurin@sha256:a7a2b5bffc4ecf12d731d416be0b3bb46b0273c5c92efbe04c03716c28823d11
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **109.1 MB (109087356 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:09e4ad6d151f1de5bcf0b2093b3878ef2151a72801d4020f62a4082efcff8c9d`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`

```dockerfile
# Sun, 27 Apr 2025 20:21:59 GMT
LABEL maintainer="Red Hat, Inc."
# Sun, 27 Apr 2025 20:21:59 GMT
LABEL vendor="Red Hat, Inc."
# Sun, 27 Apr 2025 20:21:59 GMT
LABEL url="https://www.redhat.com"
# Sun, 27 Apr 2025 20:21:59 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.6"       distribution-scope="public"
# Sun, 27 Apr 2025 20:21:59 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Sun, 27 Apr 2025 20:21:59 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Sun, 27 Apr 2025 20:21:59 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Sun, 27 Apr 2025 20:21:59 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Sun, 27 Apr 2025 20:21:59 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Sun, 27 Apr 2025 20:21:59 GMT
LABEL io.openshift.expose-services=""
# Sun, 27 Apr 2025 20:21:59 GMT
LABEL io.openshift.tags="minimal rhel9"
# Sun, 27 Apr 2025 20:21:59 GMT
ENV container oci
# Sun, 27 Apr 2025 20:21:59 GMT
COPY dir:763be6363f3253ea0e05459116de22ba38b02ee7990e3e17aa7c2682d7098cf0 in /    
# Sun, 27 Apr 2025 20:21:59 GMT
COPY file:b37d593713ee21ad52a4cd1424dc019a24f7966f85df0ac4b86d234302695328 in /etc/yum.repos.d/.    
# Sun, 27 Apr 2025 20:21:59 GMT
CMD ["/bin/bash"]
# Sun, 27 Apr 2025 20:21:59 GMT
COPY file:58cc94f5b3b2d60de2c77a6ed4b1797dcede502ccdb429a72e7a72d994235b3c in /usr/share/buildinfo/content-sets.json    
# Sun, 27 Apr 2025 20:21:59 GMT
LABEL "build-date"="2025-07-09T14:05:26" "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="b946af027f523f072a8882a41937895e04be5bec" "release"="1752069876"
# Sun, 27 Apr 2025 20:21:59 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sun, 27 Apr 2025 20:21:59 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sun, 27 Apr 2025 20:21:59 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Sun, 27 Apr 2025 20:21:59 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en     ;     microdnf clean all # buildkit
# Sun, 27 Apr 2025 20:21:59 GMT
ENV JAVA_VERSION=jdk8u452-b09
# Sun, 27 Apr 2025 20:21:59 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='5d0c81fd8bee49d1b9931acaecdc528fdc9393547cf5b24880445ade6b3f2384';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u452-b09/OpenJDK8U-jre_aarch64_linux_hotspot_8u452b09.tar.gz';          ;;        ppc64le)          ESUM='d9b523defdea8b82647726de8f62b57a19f2c64020b9ab6dbc5ae4929d0ee64e';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u452-b09/OpenJDK8U-jre_ppc64le_linux_hotspot_8u452b09.tar.gz';          ;;        x86_64)          ESUM='0c76f94e1b400a4da932a3f581b0788af2101819083184f40a6c76ac9b97081f';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u452-b09/OpenJDK8U-jre_x64_linux_hotspot_8u452b09.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz; # buildkit
# Sun, 27 Apr 2025 20:21:59 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java -version"; java -version;     echo "Complete." # buildkit
# Sun, 27 Apr 2025 20:21:59 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Sun, 27 Apr 2025 20:21:59 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
```

-	Layers:
	-	`sha256:4aebf8512d837638f2ec264e09f9e51206cfe9dfbeea1dadda474ea4e2e32dc2`  
		Last Modified: Wed, 09 Jul 2025 15:41:38 GMT  
		Size: 39.7 MB (39656780 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4aefe6d64b981d33d4838e5b175cf408733d0e2e9423a7ecac4bd09bfe96e4c1`  
		Last Modified: Fri, 11 Jul 2025 23:33:32 GMT  
		Size: 27.5 MB (27545737 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42c4854cbf5eb9e709290084f612924a8d86addeb039b1096e0ac32ae27f5238`  
		Last Modified: Fri, 11 Jul 2025 23:33:33 GMT  
		Size: 41.9 MB (41882421 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ee0a63903882627286dbf5d188e7c0ebf97ae078843bc246a59c56d87ddd971`  
		Last Modified: Fri, 11 Jul 2025 23:33:30 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66ee07eb76d71ebf9973809bc5991a106f55df77757ea8569eec336b63f10c72`  
		Last Modified: Fri, 11 Jul 2025 23:33:30 GMT  
		Size: 2.3 KB (2291 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:8-jre-ubi9-minimal` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:99014876f702856a9d87ce846159e7387d3912e84b9b722ec6ea0e8368e7af6c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2439841 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ee9530666de785d08d5f05d0c4177b8cf36c478b7461d21d032e8b37145fdf4`

```dockerfile
```

-	Layers:
	-	`sha256:407cc550c77424127de04528cb5fb1007357e432e5dc43ed6c06ce603bed1f02`  
		Last Modified: Sat, 12 Jul 2025 00:17:04 GMT  
		Size: 2.4 MB (2420482 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bb176ccc44a3ee08684511ab3624c8b152ce8f4e2d8216ff3f5cb3de35111bde`  
		Last Modified: Sat, 12 Jul 2025 00:17:04 GMT  
		Size: 19.4 KB (19359 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-temurin:8-jre-ubi9-minimal` - linux; arm64 variant v8

```console
$ docker pull eclipse-temurin@sha256:bd72c6bb852a79140a000203f773e7c8080ecf618656e9643e257af9c08c9a86
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **106.7 MB (106729078 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d3362d15640683215ceb4c4e8378300e4cca6a33f04b6ec9d5ff3e69da454a0`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`

```dockerfile
# Sun, 27 Apr 2025 20:21:59 GMT
LABEL maintainer="Red Hat, Inc."
# Sun, 27 Apr 2025 20:21:59 GMT
LABEL vendor="Red Hat, Inc."
# Sun, 27 Apr 2025 20:21:59 GMT
LABEL url="https://www.redhat.com"
# Sun, 27 Apr 2025 20:21:59 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.6"       distribution-scope="public"
# Sun, 27 Apr 2025 20:21:59 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Sun, 27 Apr 2025 20:21:59 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Sun, 27 Apr 2025 20:21:59 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Sun, 27 Apr 2025 20:21:59 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Sun, 27 Apr 2025 20:21:59 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Sun, 27 Apr 2025 20:21:59 GMT
LABEL io.openshift.expose-services=""
# Sun, 27 Apr 2025 20:21:59 GMT
LABEL io.openshift.tags="minimal rhel9"
# Sun, 27 Apr 2025 20:21:59 GMT
ENV container oci
# Sun, 27 Apr 2025 20:21:59 GMT
COPY dir:b783331d27fd913eeb2432850fad52ee030371aaa92d5026fe285216c5bf07a4 in /    
# Sun, 27 Apr 2025 20:21:59 GMT
COPY file:b37d593713ee21ad52a4cd1424dc019a24f7966f85df0ac4b86d234302695328 in /etc/yum.repos.d/.    
# Sun, 27 Apr 2025 20:21:59 GMT
CMD ["/bin/bash"]
# Sun, 27 Apr 2025 20:21:59 GMT
COPY file:0667e9d31385a24c3aef13f2dd9ab6a7b71b3dfcfef5127d3c1e2ea2c838e5cb in /usr/share/buildinfo/content-sets.json    
# Sun, 27 Apr 2025 20:21:59 GMT
LABEL "build-date"="2025-07-09T14:10:01" "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="b946af027f523f072a8882a41937895e04be5bec" "release"="1752069876"
# Sun, 27 Apr 2025 20:21:59 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sun, 27 Apr 2025 20:21:59 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sun, 27 Apr 2025 20:21:59 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Sun, 27 Apr 2025 20:21:59 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en     ;     microdnf clean all # buildkit
# Sun, 27 Apr 2025 20:21:59 GMT
ENV JAVA_VERSION=jdk8u452-b09
# Sun, 27 Apr 2025 20:21:59 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='5d0c81fd8bee49d1b9931acaecdc528fdc9393547cf5b24880445ade6b3f2384';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u452-b09/OpenJDK8U-jre_aarch64_linux_hotspot_8u452b09.tar.gz';          ;;        ppc64le)          ESUM='d9b523defdea8b82647726de8f62b57a19f2c64020b9ab6dbc5ae4929d0ee64e';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u452-b09/OpenJDK8U-jre_ppc64le_linux_hotspot_8u452b09.tar.gz';          ;;        x86_64)          ESUM='0c76f94e1b400a4da932a3f581b0788af2101819083184f40a6c76ac9b97081f';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u452-b09/OpenJDK8U-jre_x64_linux_hotspot_8u452b09.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz; # buildkit
# Sun, 27 Apr 2025 20:21:59 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java -version"; java -version;     echo "Complete." # buildkit
# Sun, 27 Apr 2025 20:21:59 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Sun, 27 Apr 2025 20:21:59 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
```

-	Layers:
	-	`sha256:20903621eaed1da24bbd033a1782d897d15ed92cf3430cd60e3ec0cda4a1bb69`  
		Last Modified: Thu, 10 Jul 2025 01:38:24 GMT  
		Size: 37.9 MB (37863034 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9f616163d50a0cbf3a1601df8ccedc3236bfc89127db1cc57876f59772411e7`  
		Last Modified: Fri, 11 Jul 2025 23:39:32 GMT  
		Size: 28.0 MB (27987767 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ed60e23c4ff27312291262e6803a76d72110080c0175f539cf5c434fe3d1c62`  
		Last Modified: Fri, 11 Jul 2025 23:39:50 GMT  
		Size: 40.9 MB (40875859 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52a3bb9f30019d6e1ce10209108f7b71d740c72e4b54c522fc4788e8bf4d0834`  
		Last Modified: Fri, 11 Jul 2025 23:39:47 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8e9b272f96a125822ac84402d6ba451bb6e3657077402f1a3230967cd89cf2a`  
		Last Modified: Fri, 11 Jul 2025 23:39:47 GMT  
		Size: 2.3 KB (2290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:8-jre-ubi9-minimal` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:54fb2487484f058570fbb544f59585b31f2177bc49bcc7afd964eabfaf17e78d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2439996 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd17945c8297dbfc0e2be98f261cb043f228b36ffe3bc3444676e2d19da18302`

```dockerfile
```

-	Layers:
	-	`sha256:9218c8f1d1fd32c183d3832925609b32849e0fad66b0ad29f795e6e930cdc22c`  
		Last Modified: Sat, 12 Jul 2025 00:17:08 GMT  
		Size: 2.4 MB (2420532 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3216be33fab5343469dd7c8e77c69488f62daf1164d2d02b4e5c322d89184ad8`  
		Last Modified: Sat, 12 Jul 2025 00:17:09 GMT  
		Size: 19.5 KB (19464 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-temurin:8-jre-ubi9-minimal` - linux; ppc64le

```console
$ docker pull eclipse-temurin@sha256:a664133e6f477075888b1e1fc8133b4b05d5ed6a18f68eb7d0ce9eebd3ce4856
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.3 MB (115261492 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b72b76e2939e1dec2043ffdc8a467d6416b9899abd2680f7043a9a9b22d6bd7`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`

```dockerfile
# Sun, 27 Apr 2025 20:21:59 GMT
LABEL maintainer="Red Hat, Inc."
# Sun, 27 Apr 2025 20:21:59 GMT
LABEL vendor="Red Hat, Inc."
# Sun, 27 Apr 2025 20:21:59 GMT
LABEL url="https://www.redhat.com"
# Sun, 27 Apr 2025 20:21:59 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.6"       distribution-scope="public"
# Sun, 27 Apr 2025 20:21:59 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Sun, 27 Apr 2025 20:21:59 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Sun, 27 Apr 2025 20:21:59 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Sun, 27 Apr 2025 20:21:59 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Sun, 27 Apr 2025 20:21:59 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Sun, 27 Apr 2025 20:21:59 GMT
LABEL io.openshift.expose-services=""
# Sun, 27 Apr 2025 20:21:59 GMT
LABEL io.openshift.tags="minimal rhel9"
# Sun, 27 Apr 2025 20:21:59 GMT
ENV container oci
# Sun, 27 Apr 2025 20:21:59 GMT
COPY dir:73930ed21f69466bc4b38ffc8263e56640090f18dc00dc206ddc704b5b9f1ca0 in /    
# Sun, 27 Apr 2025 20:21:59 GMT
COPY file:b37d593713ee21ad52a4cd1424dc019a24f7966f85df0ac4b86d234302695328 in /etc/yum.repos.d/.    
# Sun, 27 Apr 2025 20:21:59 GMT
CMD ["/bin/bash"]
# Sun, 27 Apr 2025 20:21:59 GMT
COPY file:0667e9d31385a24c3aef13f2dd9ab6a7b71b3dfcfef5127d3c1e2ea2c838e5cb in /usr/share/buildinfo/content-sets.json    
# Sun, 27 Apr 2025 20:21:59 GMT
LABEL "build-date"="2025-07-09T14:35:36" "architecture"="ppc64le" "vcs-type"="git" "vcs-ref"="b946af027f523f072a8882a41937895e04be5bec" "release"="1752069876"
# Sun, 27 Apr 2025 20:21:59 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sun, 27 Apr 2025 20:21:59 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sun, 27 Apr 2025 20:21:59 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Sun, 27 Apr 2025 20:21:59 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en     ;     microdnf clean all # buildkit
# Sun, 27 Apr 2025 20:21:59 GMT
ENV JAVA_VERSION=jdk8u452-b09
# Sun, 27 Apr 2025 20:21:59 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='5d0c81fd8bee49d1b9931acaecdc528fdc9393547cf5b24880445ade6b3f2384';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u452-b09/OpenJDK8U-jre_aarch64_linux_hotspot_8u452b09.tar.gz';          ;;        ppc64le)          ESUM='d9b523defdea8b82647726de8f62b57a19f2c64020b9ab6dbc5ae4929d0ee64e';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u452-b09/OpenJDK8U-jre_ppc64le_linux_hotspot_8u452b09.tar.gz';          ;;        x86_64)          ESUM='0c76f94e1b400a4da932a3f581b0788af2101819083184f40a6c76ac9b97081f';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u452-b09/OpenJDK8U-jre_x64_linux_hotspot_8u452b09.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz; # buildkit
# Sun, 27 Apr 2025 20:21:59 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java -version"; java -version;     echo "Complete." # buildkit
# Sun, 27 Apr 2025 20:21:59 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Sun, 27 Apr 2025 20:21:59 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
```

-	Layers:
	-	`sha256:8ca48092d0e85ccf7e1d265436c83d1bf5ecbe3d844259987ae6b1612d5b9d28`  
		Last Modified: Thu, 10 Jul 2025 09:40:32 GMT  
		Size: 44.0 MB (44022415 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a35efa0cbfd7ed6dd2d014d4e50676fd66853f250fe119d4d3eae79827a21f3`  
		Last Modified: Fri, 11 Jul 2025 23:42:45 GMT  
		Size: 30.0 MB (29979021 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c24a0f49fc33f02b11d1da0e791e148cf41c05ae613b2bdc2b8fae82c848078`  
		Last Modified: Fri, 11 Jul 2025 23:43:33 GMT  
		Size: 41.3 MB (41257640 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cde53e7077b452e3d5065b22e6e7b632a2623df6c78702286d9e744965410b35`  
		Last Modified: Fri, 11 Jul 2025 23:43:29 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:723a252f33964714204664c6227bb05ccac253c9bf3c56028db4adb7f6c9bc8d`  
		Last Modified: Fri, 11 Jul 2025 23:43:29 GMT  
		Size: 2.3 KB (2290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:8-jre-ubi9-minimal` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:c1367fae1a915952627ebdbcaaf2d6db6c89d6ae6420376394e7a08053d7beab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2440569 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:44ceb925bbe8add5288d105c14048aaae2a1b3168c45131634fcaa52e396da9f`

```dockerfile
```

-	Layers:
	-	`sha256:9cb161ccc300b8da6a6ad73b99426475d13ed42dbd86b8956b43b2bc574215e4`  
		Last Modified: Sat, 12 Jul 2025 00:17:14 GMT  
		Size: 2.4 MB (2421179 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bee81df8c1c369906bed0c622d7002b87fee5a0a9c7fddab677e60c41990b794`  
		Last Modified: Sat, 12 Jul 2025 00:17:14 GMT  
		Size: 19.4 KB (19390 bytes)  
		MIME: application/vnd.in-toto+json
