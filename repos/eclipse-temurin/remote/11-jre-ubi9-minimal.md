## `eclipse-temurin:11-jre-ubi9-minimal`

```console
$ docker pull eclipse-temurin@sha256:a14ea2feac1f1c9f1d813251ce94da140a920d1e7224876edb5b5ac7e64b959c
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

### `eclipse-temurin:11-jre-ubi9-minimal` - linux; amd64

```console
$ docker pull eclipse-temurin@sha256:52222912c9aeef9dbc2d97172b11e380f5e7b92264a6a84994bfd1b2a59da19a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **112.7 MB (112680581 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f51d4465045c8863299b8d5b5019c37c5bceb65288964c98b1a5c4f7d90d0a16`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`

```dockerfile
# Tue, 23 Jun 2026 05:11:46 GMT
LABEL maintainer="Red Hat, Inc."
# Tue, 23 Jun 2026 05:11:46 GMT
LABEL vendor="Red Hat, Inc."
# Tue, 23 Jun 2026 05:11:46 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Tue, 23 Jun 2026 05:11:46 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.8"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Tue, 23 Jun 2026 05:11:46 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Tue, 23 Jun 2026 05:11:46 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Tue, 23 Jun 2026 05:11:46 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Tue, 23 Jun 2026 05:11:46 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Tue, 23 Jun 2026 05:11:46 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Tue, 23 Jun 2026 05:11:46 GMT
LABEL io.openshift.expose-services=""
# Tue, 23 Jun 2026 05:11:46 GMT
LABEL io.openshift.tags="minimal rhel9"
# Tue, 23 Jun 2026 05:11:46 GMT
ENV container oci
# Tue, 23 Jun 2026 05:11:46 GMT
COPY dir:f278a99c81d25e574e4095be97d2e212c8bd76544b73ffdab7eab4c5e42d12b6 in /      
# Tue, 23 Jun 2026 05:11:46 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Tue, 23 Jun 2026 05:11:46 GMT
CMD ["/bin/bash"]
# Tue, 23 Jun 2026 05:11:47 GMT
COPY dir:c2709a3d2c126f3448a9859c7e12a4347d4fe7ea0104c04c47ebdcbe0d9f7851 in /usr/share/buildinfo/      
# Tue, 23 Jun 2026 05:11:47 GMT
COPY dir:c2709a3d2c126f3448a9859c7e12a4347d4fe7ea0104c04c47ebdcbe0d9f7851 in /root/buildinfo/      
# Tue, 23 Jun 2026 05:11:47 GMT
LABEL "org.opencontainers.image.created"="2026-06-23T05:11:30Z" "org.opencontainers.image.revision"="e834ed7be4fa69fe8faf5574157c5c65992ace09" "build-date"="2026-06-23T05:11:30Z" "architecture"="x86_64" "vcs-ref"="e834ed7be4fa69fe8faf5574157c5c65992ace09" "vcs-type"="git" "release"="1782191395"org.opencontainers.image.created=2026-06-23T05:11:30Z,org.opencontainers.image.revision=e834ed7be4fa69fe8faf5574157c5c65992ace09
# Wed, 24 Jun 2026 23:04:02 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 24 Jun 2026 23:04:02 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Jun 2026 23:04:02 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 24 Jun 2026 23:04:02 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en     ;     microdnf clean all # buildkit
# Wed, 24 Jun 2026 23:04:02 GMT
ENV JAVA_VERSION=jdk-11.0.31+11
# Wed, 24 Jun 2026 23:04:05 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='eabe05fb80626ad24db17cf1df137855e77fbacbc83c11aaf243cedd224467de';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.31%2B11/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.31_11.tar.gz';          ;;        ppc64le)          ESUM='11e58bf1eeae10f0dc1a98cc43bf97af270a0b516f6ff9fb3189024c5e22550a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.31%2B11/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.31_11.tar.gz';          ;;        s390x)          ESUM='4c311b19aa3922951be288076f0f41a831ab7af32284da9b3e21cdaa251a078a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.31%2B11/OpenJDK11U-jre_s390x_linux_hotspot_11.0.31_11.tar.gz';          ;;        x86_64)          ESUM='a6af3d61851f57eb79ef0189837522329717458bf230ee284da2d26634f1ea3a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.31%2B11/OpenJDK11U-jre_x64_linux_hotspot_11.0.31_11.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz; # buildkit
# Wed, 24 Jun 2026 23:04:05 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 24 Jun 2026 23:04:05 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 24 Jun 2026 23:04:05 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
```

-	Layers:
	-	`sha256:689a2fa06433046ccdc79ee32d366190123758804fb645bc032123dc904e226b`  
		Last Modified: Tue, 23 Jun 2026 05:49:10 GMT  
		Size: 40.7 MB (40671135 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebae513aeb8ed601ee9e4340f9bfd7988fdf183154f58fe3012e168057643f53`  
		Last Modified: Wed, 24 Jun 2026 23:04:17 GMT  
		Size: 27.7 MB (27660469 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eaf768d90056d2704e7797622cd8c64ea5b69a499bcf96b63f0db32b41be4a6d`  
		Last Modified: Wed, 24 Jun 2026 23:04:18 GMT  
		Size: 44.3 MB (44346559 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57bad991bf15b33d6f1511c057e9208295910ead5ae57692e869f98926c35ca0`  
		Last Modified: Wed, 24 Jun 2026 23:04:16 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe96e70f4bfb0d30a0981e6f6fc095957045caa25b76feedfbde48385595101e`  
		Last Modified: Wed, 24 Jun 2026 23:04:16 GMT  
		Size: 2.3 KB (2290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:11-jre-ubi9-minimal` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:a7861f98f0ee960c465de6be6b22c36fa60b8ddccfee3a131c931e4da6402807
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2442711 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f33320ead33db692ee4c948b3fb527beaa14c7e5c8adb4d9865ebb99fd2c0ce4`

```dockerfile
```

-	Layers:
	-	`sha256:acddec8d7fe3b7b4129e37960d2820f8489d2af3e2357e0ae8bae1df0c95e9a4`  
		Last Modified: Wed, 24 Jun 2026 23:04:16 GMT  
		Size: 2.4 MB (2422501 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b952fdc46cae5f58afd1d07633494c52e7d6e601f47bdb3d2d6951ddb02afefa`  
		Last Modified: Wed, 24 Jun 2026 23:04:16 GMT  
		Size: 20.2 KB (20210 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-temurin:11-jre-ubi9-minimal` - linux; arm64 variant v8

```console
$ docker pull eclipse-temurin@sha256:f01929cfe25a031ea34d9b5808d641bcc3cd200727bc42e23362ee711ede3a42
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **95.5 MB (95536376 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ad9b85ce6dd2ecc224fc5c9895b7eb83df7cc243dd6443de6b0e7735e284ddc`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`

```dockerfile
# Tue, 23 Jun 2026 05:12:59 GMT
LABEL maintainer="Red Hat, Inc."
# Tue, 23 Jun 2026 05:12:59 GMT
LABEL vendor="Red Hat, Inc."
# Tue, 23 Jun 2026 05:12:59 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Tue, 23 Jun 2026 05:12:59 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.8"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Tue, 23 Jun 2026 05:12:59 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Tue, 23 Jun 2026 05:12:59 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Tue, 23 Jun 2026 05:12:59 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Tue, 23 Jun 2026 05:12:59 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Tue, 23 Jun 2026 05:12:59 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Tue, 23 Jun 2026 05:12:59 GMT
LABEL io.openshift.expose-services=""
# Tue, 23 Jun 2026 05:12:59 GMT
LABEL io.openshift.tags="minimal rhel9"
# Tue, 23 Jun 2026 05:12:59 GMT
ENV container oci
# Tue, 23 Jun 2026 05:12:59 GMT
COPY dir:923fd04a317c8ab7292cc4c6490977e5f3d0a2e1ff9dc5a4ce7f5c95aef17062 in /      
# Tue, 23 Jun 2026 05:13:00 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Tue, 23 Jun 2026 05:13:00 GMT
CMD ["/bin/bash"]
# Tue, 23 Jun 2026 05:13:00 GMT
COPY dir:dffe6ac0f40d1fc4397ba26e90223bac1cf14e7dcba262c2807afbcac45f5ea3 in /usr/share/buildinfo/      
# Tue, 23 Jun 2026 05:13:00 GMT
COPY dir:dffe6ac0f40d1fc4397ba26e90223bac1cf14e7dcba262c2807afbcac45f5ea3 in /root/buildinfo/      
# Tue, 23 Jun 2026 05:13:00 GMT
LABEL "org.opencontainers.image.created"="2026-06-23T05:12:36Z" "org.opencontainers.image.revision"="e834ed7be4fa69fe8faf5574157c5c65992ace09" "build-date"="2026-06-23T05:12:36Z" "architecture"="aarch64" "vcs-ref"="e834ed7be4fa69fe8faf5574157c5c65992ace09" "vcs-type"="git" "release"="1782191395"org.opencontainers.image.created=2026-06-23T05:12:36Z,org.opencontainers.image.revision=e834ed7be4fa69fe8faf5574157c5c65992ace09
# Wed, 24 Jun 2026 23:03:14 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 24 Jun 2026 23:03:14 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Jun 2026 23:03:14 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 24 Jun 2026 23:03:14 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en     ;     microdnf clean all # buildkit
# Wed, 24 Jun 2026 23:03:14 GMT
ENV JAVA_VERSION=jdk-11.0.31+11
# Wed, 24 Jun 2026 23:03:17 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='eabe05fb80626ad24db17cf1df137855e77fbacbc83c11aaf243cedd224467de';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.31%2B11/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.31_11.tar.gz';          ;;        ppc64le)          ESUM='11e58bf1eeae10f0dc1a98cc43bf97af270a0b516f6ff9fb3189024c5e22550a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.31%2B11/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.31_11.tar.gz';          ;;        s390x)          ESUM='4c311b19aa3922951be288076f0f41a831ab7af32284da9b3e21cdaa251a078a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.31%2B11/OpenJDK11U-jre_s390x_linux_hotspot_11.0.31_11.tar.gz';          ;;        x86_64)          ESUM='a6af3d61851f57eb79ef0189837522329717458bf230ee284da2d26634f1ea3a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.31%2B11/OpenJDK11U-jre_x64_linux_hotspot_11.0.31_11.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz; # buildkit
# Wed, 24 Jun 2026 23:03:17 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 24 Jun 2026 23:03:17 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 24 Jun 2026 23:03:17 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
```

-	Layers:
	-	`sha256:989109f74f2ed8868dc53877eebf602a5b9e56448cce38c307c203e890a4c731`  
		Last Modified: Tue, 23 Jun 2026 06:05:10 GMT  
		Size: 38.8 MB (38805824 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8718ba58e2fe31c2551647686dedf3c91d0362f3add72eebf3c9747af157156d`  
		Last Modified: Wed, 24 Jun 2026 23:03:28 GMT  
		Size: 14.1 MB (14059547 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee9a4d82e405b4cd6880f3330fe683715b5b13285d1f8ba9d0e391a5bf6f0187`  
		Last Modified: Wed, 24 Jun 2026 23:03:29 GMT  
		Size: 42.7 MB (42668588 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80dfe630d524d753caf0337180945895d97ed3a468096573f2e72dc9d48bdb32`  
		Last Modified: Wed, 24 Jun 2026 23:03:28 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a130a99b261e5d2290d2e16de66a6fc38bad22864f601a51d4cf3ce9029c2cd`  
		Last Modified: Wed, 24 Jun 2026 23:03:28 GMT  
		Size: 2.3 KB (2291 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:11-jre-ubi9-minimal` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:cd90cca30e7b83e8f91921418ff74e8972f2964c666cfec75cde08b9dd43833a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.7 MB (1704625 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ba5049208144b88de60a9e0dba48b4addaf1f7e9ec32f093d58f2df56203f8a`

```dockerfile
```

-	Layers:
	-	`sha256:f1e697f5bc1083c27f893ea1fb4ad4c5d136d61ba4a92d0f9c93ead0b0f66032`  
		Last Modified: Wed, 24 Jun 2026 23:03:28 GMT  
		Size: 1.7 MB (1684311 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bd2bdb38eb3726b6b7e3668145fc15183e7e0f9ae13462327fe1f736748b8f00`  
		Last Modified: Wed, 24 Jun 2026 23:03:28 GMT  
		Size: 20.3 KB (20314 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-temurin:11-jre-ubi9-minimal` - linux; ppc64le

```console
$ docker pull eclipse-temurin@sha256:0460520e13deb51b2ffe0086ce9559a5aa5b637742e7bc9f423cae0b86dbdfe7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **100.2 MB (100166884 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2030a3e3b935df8c62751fcd4442599871cd5c7497555a7e57a21a82ea3836dd`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`

```dockerfile
# Tue, 23 Jun 2026 05:13:01 GMT
LABEL maintainer="Red Hat, Inc."
# Tue, 23 Jun 2026 05:13:01 GMT
LABEL vendor="Red Hat, Inc."
# Tue, 23 Jun 2026 05:13:01 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Tue, 23 Jun 2026 05:13:01 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.8"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Tue, 23 Jun 2026 05:13:01 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Tue, 23 Jun 2026 05:13:01 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Tue, 23 Jun 2026 05:13:01 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Tue, 23 Jun 2026 05:13:01 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Tue, 23 Jun 2026 05:13:01 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Tue, 23 Jun 2026 05:13:01 GMT
LABEL io.openshift.expose-services=""
# Tue, 23 Jun 2026 05:13:01 GMT
LABEL io.openshift.tags="minimal rhel9"
# Tue, 23 Jun 2026 05:13:01 GMT
ENV container oci
# Tue, 23 Jun 2026 05:13:02 GMT
COPY dir:4d2a3ebfba3e6886b6504d8dd92beaac194e548e40aa4bca182adbaa9be02afc in /      
# Tue, 23 Jun 2026 05:13:02 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Tue, 23 Jun 2026 05:13:02 GMT
CMD ["/bin/bash"]
# Tue, 23 Jun 2026 05:13:02 GMT
COPY dir:b7827d131ad066b0f131c7ebfb16ff261b70c3cbb8cf357ab0913f8aa1eef055 in /usr/share/buildinfo/      
# Tue, 23 Jun 2026 05:13:02 GMT
COPY dir:b7827d131ad066b0f131c7ebfb16ff261b70c3cbb8cf357ab0913f8aa1eef055 in /root/buildinfo/      
# Tue, 23 Jun 2026 05:13:02 GMT
LABEL "org.opencontainers.image.created"="2026-06-23T05:12:46Z" "org.opencontainers.image.revision"="e834ed7be4fa69fe8faf5574157c5c65992ace09" "build-date"="2026-06-23T05:12:46Z" "architecture"="ppc64le" "vcs-ref"="e834ed7be4fa69fe8faf5574157c5c65992ace09" "vcs-type"="git" "release"="1782191395"org.opencontainers.image.created=2026-06-23T05:12:46Z,org.opencontainers.image.revision=e834ed7be4fa69fe8faf5574157c5c65992ace09
# Wed, 24 Jun 2026 23:01:50 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 24 Jun 2026 23:01:50 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Jun 2026 23:01:50 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 24 Jun 2026 23:01:50 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en     ;     microdnf clean all # buildkit
# Wed, 24 Jun 2026 23:01:50 GMT
ENV JAVA_VERSION=jdk-11.0.31+11
# Wed, 24 Jun 2026 23:04:55 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='eabe05fb80626ad24db17cf1df137855e77fbacbc83c11aaf243cedd224467de';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.31%2B11/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.31_11.tar.gz';          ;;        ppc64le)          ESUM='11e58bf1eeae10f0dc1a98cc43bf97af270a0b516f6ff9fb3189024c5e22550a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.31%2B11/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.31_11.tar.gz';          ;;        s390x)          ESUM='4c311b19aa3922951be288076f0f41a831ab7af32284da9b3e21cdaa251a078a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.31%2B11/OpenJDK11U-jre_s390x_linux_hotspot_11.0.31_11.tar.gz';          ;;        x86_64)          ESUM='a6af3d61851f57eb79ef0189837522329717458bf230ee284da2d26634f1ea3a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.31%2B11/OpenJDK11U-jre_x64_linux_hotspot_11.0.31_11.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz; # buildkit
# Wed, 24 Jun 2026 23:04:55 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 24 Jun 2026 23:04:57 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 24 Jun 2026 23:04:57 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
```

-	Layers:
	-	`sha256:4bac72a9a1f43367def803d06c2dab63b4bb0e322cb08ee3db80259d84e62045`  
		Last Modified: Tue, 23 Jun 2026 06:12:06 GMT  
		Size: 45.1 MB (45144751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93f99e1bd1d0e0245b9ff9de06dc4f155f0170e63761b11e9c13863eabbea391`  
		Last Modified: Wed, 24 Jun 2026 23:02:32 GMT  
		Size: 15.2 MB (15157790 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b31e1ef6b7cb4cefb1da94b990f7d905d10ec1a7e29f4b772468e09f3796a3a`  
		Last Modified: Wed, 24 Jun 2026 23:05:31 GMT  
		Size: 39.9 MB (39861926 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b296a26cbe2f10b522829ce7529c7ea0117b4b021024597870e0fd84be985716`  
		Last Modified: Wed, 24 Jun 2026 23:05:30 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d044ef56f5322c71f5df752a9f0609accf5f763c5d21d6029e0893fecc1b978e`  
		Last Modified: Wed, 24 Jun 2026 23:05:30 GMT  
		Size: 2.3 KB (2289 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:11-jre-ubi9-minimal` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:42f1136b756bc6b86cdc15f604564e09bed2ec4ed3b42159bb82a836477f58d4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.7 MB (1705767 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e1fb1366e4de2f3cbd4411554dbaff117c87512ce641b54972342cde097c4a6f`

```dockerfile
```

-	Layers:
	-	`sha256:3461e6b9429473bd63005f92ee65ed0eea7431d1690d2be28a8f25a8d1b3bbbd`  
		Last Modified: Wed, 24 Jun 2026 23:05:30 GMT  
		Size: 1.7 MB (1685528 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ed6b7696852595da3a5d5d4b0e33b96bc395a653b4fe125634238eec0d24b119`  
		Last Modified: Wed, 24 Jun 2026 23:05:29 GMT  
		Size: 20.2 KB (20239 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-temurin:11-jre-ubi9-minimal` - linux; s390x

```console
$ docker pull eclipse-temurin@sha256:3d5209fbfa5e6d22b91a2516db9fb033ed20dc1c53a44d5d0c1f79a08e94ada4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **91.0 MB (90979000 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:604889f4ae03bea97558af10e378da3bb3f9bf53e3b68f8691446de1e4a03f0b`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`

```dockerfile
# Tue, 23 Jun 2026 05:18:00 GMT
LABEL maintainer="Red Hat, Inc."
# Tue, 23 Jun 2026 05:18:00 GMT
LABEL vendor="Red Hat, Inc."
# Tue, 23 Jun 2026 05:18:00 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Tue, 23 Jun 2026 05:18:00 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.8"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Tue, 23 Jun 2026 05:18:00 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Tue, 23 Jun 2026 05:18:00 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Tue, 23 Jun 2026 05:18:00 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Tue, 23 Jun 2026 05:18:00 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Tue, 23 Jun 2026 05:18:00 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Tue, 23 Jun 2026 05:18:00 GMT
LABEL io.openshift.expose-services=""
# Tue, 23 Jun 2026 05:18:00 GMT
LABEL io.openshift.tags="minimal rhel9"
# Tue, 23 Jun 2026 05:18:00 GMT
ENV container oci
# Tue, 23 Jun 2026 05:18:00 GMT
COPY dir:27877c357368aea512a88a6f3ff986d2f2cae38facf5c958fc65210886393092 in /      
# Tue, 23 Jun 2026 05:18:00 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Tue, 23 Jun 2026 05:18:00 GMT
CMD ["/bin/bash"]
# Tue, 23 Jun 2026 05:18:00 GMT
COPY dir:93599b4d15b0e179c067caa1878c815ffdcb1bde2382dffed0b86ba833b3047a in /usr/share/buildinfo/      
# Tue, 23 Jun 2026 05:18:00 GMT
COPY dir:93599b4d15b0e179c067caa1878c815ffdcb1bde2382dffed0b86ba833b3047a in /root/buildinfo/      
# Tue, 23 Jun 2026 05:18:01 GMT
LABEL "org.opencontainers.image.created"="2026-06-23T05:17:03Z" "org.opencontainers.image.revision"="e834ed7be4fa69fe8faf5574157c5c65992ace09" "build-date"="2026-06-23T05:17:03Z" "architecture"="s390x" "vcs-ref"="e834ed7be4fa69fe8faf5574157c5c65992ace09" "vcs-type"="git" "release"="1782191395"org.opencontainers.image.created=2026-06-23T05:17:03Z,org.opencontainers.image.revision=e834ed7be4fa69fe8faf5574157c5c65992ace09
# Wed, 24 Jun 2026 23:01:49 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 24 Jun 2026 23:01:49 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Jun 2026 23:01:49 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 24 Jun 2026 23:01:49 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en     ;     microdnf clean all # buildkit
# Wed, 24 Jun 2026 23:01:49 GMT
ENV JAVA_VERSION=jdk-11.0.31+11
# Wed, 24 Jun 2026 23:01:51 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='eabe05fb80626ad24db17cf1df137855e77fbacbc83c11aaf243cedd224467de';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.31%2B11/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.31_11.tar.gz';          ;;        ppc64le)          ESUM='11e58bf1eeae10f0dc1a98cc43bf97af270a0b516f6ff9fb3189024c5e22550a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.31%2B11/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.31_11.tar.gz';          ;;        s390x)          ESUM='4c311b19aa3922951be288076f0f41a831ab7af32284da9b3e21cdaa251a078a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.31%2B11/OpenJDK11U-jre_s390x_linux_hotspot_11.0.31_11.tar.gz';          ;;        x86_64)          ESUM='a6af3d61851f57eb79ef0189837522329717458bf230ee284da2d26634f1ea3a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.31%2B11/OpenJDK11U-jre_x64_linux_hotspot_11.0.31_11.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz; # buildkit
# Wed, 24 Jun 2026 23:01:51 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 24 Jun 2026 23:01:51 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 24 Jun 2026 23:01:51 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
```

-	Layers:
	-	`sha256:027b6558e15fa03e681ac683754dd2058185e2be499788f5e5a422bfa61b34db`  
		Last Modified: Tue, 23 Jun 2026 06:11:50 GMT  
		Size: 38.8 MB (38754261 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ccc3c995a28750c2f09cf32cfcd7c1996bd7b1abf0d62aae5150ce2be1e50a1`  
		Last Modified: Wed, 24 Jun 2026 23:02:08 GMT  
		Size: 13.9 MB (13892031 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a7aa10b1d05b677f7a09c638bb69d38895216df069dc2ab0388f70d37c151c5`  
		Last Modified: Wed, 24 Jun 2026 23:02:09 GMT  
		Size: 38.3 MB (38330291 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c321ea1af888abecbe956938680da2f10c4f63ca45ff2d8f3bd0ce6939fb36a7`  
		Last Modified: Wed, 24 Jun 2026 23:02:08 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3320a4a84ff76284cc02f0bc35b9276be5093ab4e40f3723198c1c686737b331`  
		Last Modified: Wed, 24 Jun 2026 23:02:09 GMT  
		Size: 2.3 KB (2291 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:11-jre-ubi9-minimal` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:50eb73d4e6901edde7daafdc017670c828bc317a438e6fbea135c80bd7643e4a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.7 MB (1706983 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d270de76e67bc9131212b86e9700352013eb0a794fc9d6c8e9d13ea6924a39aa`

```dockerfile
```

-	Layers:
	-	`sha256:555f54cb6e309ab7b766cbe71620eab8c8d66bd9c85bcc80b10df0aded11d47d`  
		Last Modified: Wed, 24 Jun 2026 23:02:07 GMT  
		Size: 1.7 MB (1686773 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2253324a32f429cb45807ca2ecdae067420dc667056825830a0e4ed600ddc221`  
		Last Modified: Wed, 24 Jun 2026 23:02:07 GMT  
		Size: 20.2 KB (20210 bytes)  
		MIME: application/vnd.in-toto+json
