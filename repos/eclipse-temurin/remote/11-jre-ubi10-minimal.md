## `eclipse-temurin:11-jre-ubi10-minimal`

```console
$ docker pull eclipse-temurin@sha256:507ad2aa1bfd76c4f77ec059d99bfe35ec0e334c2fbc86da95bf32c3138c8527
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

### `eclipse-temurin:11-jre-ubi10-minimal` - linux; amd64

```console
$ docker pull eclipse-temurin@sha256:19cea5f975c4db5279c778c7ee0baf4864c93fe49fc12f4f09a02ea0371b94ef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **116.5 MB (116474316 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f4cce6a50cf98b566014892e36e050b4ded569679186d8a8932fe40e2fb3f9b6`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`

```dockerfile
# Tue, 12 May 2026 09:09:41 GMT
LABEL maintainer="Red Hat, Inc."
# Tue, 12 May 2026 09:09:41 GMT
LABEL vendor="Red Hat, Inc."
# Tue, 12 May 2026 09:09:41 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Tue, 12 May 2026 09:09:41 GMT
LABEL com.redhat.component="ubi10-minimal-container"       name="ubi10/ubi-minimal"       version="10.1"       cpe="cpe:/o:redhat:enterprise_linux:10.1"       distribution-scope="public"
# Tue, 12 May 2026 09:09:41 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Tue, 12 May 2026 09:09:41 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 10."
# Tue, 12 May 2026 09:09:41 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Tue, 12 May 2026 09:09:41 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Tue, 12 May 2026 09:09:41 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 10 Minimal"
# Tue, 12 May 2026 09:09:41 GMT
LABEL io.openshift.expose-services=""
# Tue, 12 May 2026 09:09:41 GMT
LABEL io.openshift.tags="minimal rhel10"
# Tue, 12 May 2026 09:09:41 GMT
ENV container oci
# Tue, 12 May 2026 09:09:41 GMT
COPY dir:70c9e4dfd7df3debe1e0457260915a9c0446c87d882b979cfec229a5714bf4c7 in /      
# Tue, 12 May 2026 09:09:41 GMT
COPY file:5de33b5fc08b00635bccf9134a18978dba13e2250aa51838f9969515a3957847 in /etc/yum.repos.d/.      
# Tue, 12 May 2026 09:09:41 GMT
CMD ["/bin/bash"]
# Tue, 12 May 2026 09:09:42 GMT
COPY file:595171150af68abc798ea385f7988d74b566aa8e84babff137f00b08b2164683 in /usr/share/buildinfo/content-sets.json      
# Tue, 12 May 2026 09:09:42 GMT
COPY file:595171150af68abc798ea385f7988d74b566aa8e84babff137f00b08b2164683 in /root/buildinfo/content_manifests/content-sets.json      
# Tue, 12 May 2026 09:09:42 GMT
COPY file:0753abbd85f48d60c6079bc7ee41700b66d3abf1c27ef1da2779ce2ba16ca2c5 in /usr/share/buildinfo/labels.json      
# Tue, 12 May 2026 09:09:42 GMT
COPY file:0753abbd85f48d60c6079bc7ee41700b66d3abf1c27ef1da2779ce2ba16ca2c5 in /root/buildinfo/labels.json      
# Tue, 12 May 2026 09:09:42 GMT
LABEL "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="ad7cdeeb08da8825126b10f488e410b0de5902b0" "org.opencontainers.image.revision"="ad7cdeeb08da8825126b10f488e410b0de5902b0" "build-date"="2026-05-12T09:09:25Z" "org.opencontainers.image.created"="2026-05-12T09:09:25Z" "release"="1778576723"org.opencontainers.image.revision=ad7cdeeb08da8825126b10f488e410b0de5902b0,org.opencontainers.image.created=2026-05-12T09:09:25Z
# Tue, 12 May 2026 23:33:01 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 12 May 2026 23:33:01 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 May 2026 23:33:01 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 12 May 2026 23:33:01 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en         gnupg2     ;     microdnf clean all # buildkit
# Tue, 12 May 2026 23:33:01 GMT
ENV JAVA_VERSION=jdk-11.0.31+11
# Tue, 12 May 2026 23:33:31 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='eabe05fb80626ad24db17cf1df137855e77fbacbc83c11aaf243cedd224467de';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.31%2B11/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.31_11.tar.gz';          ;;        ppc64le)          ESUM='11e58bf1eeae10f0dc1a98cc43bf97af270a0b516f6ff9fb3189024c5e22550a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.31%2B11/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.31_11.tar.gz';          ;;        s390x)          ESUM='4c311b19aa3922951be288076f0f41a831ab7af32284da9b3e21cdaa251a078a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.31%2B11/OpenJDK11U-jre_s390x_linux_hotspot_11.0.31_11.tar.gz';          ;;        x86_64)          ESUM='a6af3d61851f57eb79ef0189837522329717458bf230ee284da2d26634f1ea3a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.31%2B11/OpenJDK11U-jre_x64_linux_hotspot_11.0.31_11.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz; # buildkit
# Tue, 12 May 2026 23:33:31 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 12 May 2026 23:33:31 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 12 May 2026 23:33:31 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
```

-	Layers:
	-	`sha256:20e8bbd1fa594932c31db6c97d64754bd505f260fa2792d4a021081374b77b54`  
		Last Modified: Tue, 12 May 2026 10:16:05 GMT  
		Size: 34.6 MB (34624258 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:596ac6fc2c873ba35cbe0380a8b5776ebb7e5e456b2f3e120a893d5a91199b42`  
		Last Modified: Tue, 12 May 2026 23:33:21 GMT  
		Size: 37.5 MB (37501052 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a39361ed7b32310c5afc5dedc5bbd2b36f28af35e52e9aada6d1ab51a6329e5b`  
		Last Modified: Tue, 12 May 2026 23:33:44 GMT  
		Size: 44.3 MB (44346587 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26fdfc6340a0edb753f19ebc0119923ea316945498aa21128ddc6b1ee0beace2`  
		Last Modified: Tue, 12 May 2026 23:33:43 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:926edcfc029d7ccfc89b41d2e81db1d68b8a9b211c7ba0c90e5284edabd3bcfd`  
		Last Modified: Tue, 12 May 2026 23:33:44 GMT  
		Size: 2.3 KB (2291 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:11-jre-ubi10-minimal` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:4fc84987d30b19e568c3efa74e192347c2349b0bb860b06f7f7baa13c01b9c14
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3738237 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c6e8b16e96e8e6d889e0b977a45e89fb4ec7d8c5dbb549943c8467eec40b3cde`

```dockerfile
```

-	Layers:
	-	`sha256:b2e9318f7ae0c835600cfcdc6bc9176adad3eceacde9724012e0b33e2e4a62b3`  
		Last Modified: Tue, 12 May 2026 23:33:44 GMT  
		Size: 3.7 MB (3717859 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:58d10ef5ed2a437c72760ce98c05317e0c9b0a3568b3eb7b9d41f2e5765a4b0e`  
		Last Modified: Tue, 12 May 2026 23:33:43 GMT  
		Size: 20.4 KB (20378 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-temurin:11-jre-ubi10-minimal` - linux; arm64 variant v8

```console
$ docker pull eclipse-temurin@sha256:fc9ed9a2ab310e581f3c57cfebd0e0878f971866a5ae15fd727cf022f0a7a97d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **112.8 MB (112825941 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2fa3fd57f5be6f42764a398fc60486ad3fa104e72e79c1e7b818382b2d5105c5`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`

```dockerfile
# Tue, 12 May 2026 09:11:34 GMT
LABEL maintainer="Red Hat, Inc."
# Tue, 12 May 2026 09:11:34 GMT
LABEL vendor="Red Hat, Inc."
# Tue, 12 May 2026 09:11:34 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Tue, 12 May 2026 09:11:34 GMT
LABEL com.redhat.component="ubi10-minimal-container"       name="ubi10/ubi-minimal"       version="10.1"       cpe="cpe:/o:redhat:enterprise_linux:10.1"       distribution-scope="public"
# Tue, 12 May 2026 09:11:34 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Tue, 12 May 2026 09:11:34 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 10."
# Tue, 12 May 2026 09:11:34 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Tue, 12 May 2026 09:11:34 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Tue, 12 May 2026 09:11:34 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 10 Minimal"
# Tue, 12 May 2026 09:11:35 GMT
LABEL io.openshift.expose-services=""
# Tue, 12 May 2026 09:11:35 GMT
LABEL io.openshift.tags="minimal rhel10"
# Tue, 12 May 2026 09:11:35 GMT
ENV container oci
# Tue, 12 May 2026 09:11:35 GMT
COPY dir:2877d8ca2be54c031321bcf5c5c002de1e88fc4d881af88566c341114955d981 in /      
# Tue, 12 May 2026 09:11:35 GMT
COPY file:5de33b5fc08b00635bccf9134a18978dba13e2250aa51838f9969515a3957847 in /etc/yum.repos.d/.      
# Tue, 12 May 2026 09:11:35 GMT
CMD ["/bin/bash"]
# Tue, 12 May 2026 09:11:36 GMT
COPY file:595171150af68abc798ea385f7988d74b566aa8e84babff137f00b08b2164683 in /usr/share/buildinfo/content-sets.json      
# Tue, 12 May 2026 09:11:36 GMT
COPY file:595171150af68abc798ea385f7988d74b566aa8e84babff137f00b08b2164683 in /root/buildinfo/content_manifests/content-sets.json      
# Tue, 12 May 2026 09:11:36 GMT
COPY file:ed5db005734a9cf660fffe0f9d4de854f99deb1e83b8a69fd4b48dc74dea4448 in /usr/share/buildinfo/labels.json      
# Tue, 12 May 2026 09:11:36 GMT
COPY file:ed5db005734a9cf660fffe0f9d4de854f99deb1e83b8a69fd4b48dc74dea4448 in /root/buildinfo/labels.json      
# Tue, 12 May 2026 09:11:36 GMT
LABEL "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="ad7cdeeb08da8825126b10f488e410b0de5902b0" "org.opencontainers.image.revision"="ad7cdeeb08da8825126b10f488e410b0de5902b0" "build-date"="2026-05-12T09:11:19Z" "org.opencontainers.image.created"="2026-05-12T09:11:19Z" "release"="1778576723"org.opencontainers.image.revision=ad7cdeeb08da8825126b10f488e410b0de5902b0,org.opencontainers.image.created=2026-05-12T09:11:19Z
# Tue, 12 May 2026 23:33:22 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 12 May 2026 23:33:22 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 May 2026 23:33:22 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 12 May 2026 23:33:22 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en         gnupg2     ;     microdnf clean all # buildkit
# Tue, 12 May 2026 23:33:22 GMT
ENV JAVA_VERSION=jdk-11.0.31+11
# Tue, 12 May 2026 23:33:25 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='eabe05fb80626ad24db17cf1df137855e77fbacbc83c11aaf243cedd224467de';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.31%2B11/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.31_11.tar.gz';          ;;        ppc64le)          ESUM='11e58bf1eeae10f0dc1a98cc43bf97af270a0b516f6ff9fb3189024c5e22550a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.31%2B11/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.31_11.tar.gz';          ;;        s390x)          ESUM='4c311b19aa3922951be288076f0f41a831ab7af32284da9b3e21cdaa251a078a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.31%2B11/OpenJDK11U-jre_s390x_linux_hotspot_11.0.31_11.tar.gz';          ;;        x86_64)          ESUM='a6af3d61851f57eb79ef0189837522329717458bf230ee284da2d26634f1ea3a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.31%2B11/OpenJDK11U-jre_x64_linux_hotspot_11.0.31_11.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz; # buildkit
# Tue, 12 May 2026 23:33:25 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 12 May 2026 23:33:25 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 12 May 2026 23:33:25 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
```

-	Layers:
	-	`sha256:24bccfaffdcba4dab6b032daed65e4f69253b002d2af6f83ce7d6d966c20583a`  
		Last Modified: Tue, 12 May 2026 10:25:24 GMT  
		Size: 32.7 MB (32711659 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:accdb763b46ede5375ef813aac9bc39ce687fcfa5f91f2a868b64e5e3150a9cf`  
		Last Modified: Tue, 12 May 2026 23:33:40 GMT  
		Size: 37.4 MB (37443276 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7026cf43cadf69b2d13e0dcd1542fb74ccaaebc2132356539d0e03921923945f`  
		Last Modified: Tue, 12 May 2026 23:33:40 GMT  
		Size: 42.7 MB (42668589 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b54e0255adee0ea9565b9ba3d5d69d0eac777e9932fdfaa9fcfe598f2d30bc2`  
		Last Modified: Tue, 12 May 2026 23:33:39 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0f2067c8de893232f3f093ba006bab20db6c7a758d619fde446469e4ce508b1`  
		Last Modified: Tue, 12 May 2026 23:33:39 GMT  
		Size: 2.3 KB (2290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:11-jre-ubi10-minimal` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:5a321b348bebe666bf798f836877be005c62570e26beaabd6a14b7dea0604dd6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3738373 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:05d5aa0909ca4cf0fdc52fc932897d821a5bf9d4790b8f13b827c700170a3f10`

```dockerfile
```

-	Layers:
	-	`sha256:b8e8abdfa23841c60fd6a09c6bbe298353a03b088c0811fa1946493cd67c687c`  
		Last Modified: Tue, 12 May 2026 23:33:39 GMT  
		Size: 3.7 MB (3717891 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8c3260970d82d720144531194112fd0fb485ce3db3ce5aad4e525559de5a3ff2`  
		Last Modified: Tue, 12 May 2026 23:33:38 GMT  
		Size: 20.5 KB (20482 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-temurin:11-jre-ubi10-minimal` - linux; ppc64le

```console
$ docker pull eclipse-temurin@sha256:1fb3e90d6b7cee9e009dc51b99eb075cef70aed87e709b41f47c952ee4da2b51
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **117.9 MB (117914647 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7362da1b53c21fa3707e911d9b6dd9e99e45424db121246d72d1478f4d247e2d`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`

```dockerfile
# Tue, 12 May 2026 09:13:30 GMT
LABEL maintainer="Red Hat, Inc."
# Tue, 12 May 2026 09:13:30 GMT
LABEL vendor="Red Hat, Inc."
# Tue, 12 May 2026 09:13:30 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Tue, 12 May 2026 09:13:30 GMT
LABEL com.redhat.component="ubi10-minimal-container"       name="ubi10/ubi-minimal"       version="10.1"       cpe="cpe:/o:redhat:enterprise_linux:10.1"       distribution-scope="public"
# Tue, 12 May 2026 09:13:30 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Tue, 12 May 2026 09:13:30 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 10."
# Tue, 12 May 2026 09:13:30 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Tue, 12 May 2026 09:13:30 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Tue, 12 May 2026 09:13:30 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 10 Minimal"
# Tue, 12 May 2026 09:13:31 GMT
LABEL io.openshift.expose-services=""
# Tue, 12 May 2026 09:13:31 GMT
LABEL io.openshift.tags="minimal rhel10"
# Tue, 12 May 2026 09:13:31 GMT
ENV container oci
# Tue, 12 May 2026 09:13:32 GMT
COPY dir:584fbc93c21a7184a941a4142a12f835dcfca07a9a2dfc5bd8298fc624407c1a in /      
# Tue, 12 May 2026 09:13:32 GMT
COPY file:5de33b5fc08b00635bccf9134a18978dba13e2250aa51838f9969515a3957847 in /etc/yum.repos.d/.      
# Tue, 12 May 2026 09:13:32 GMT
CMD ["/bin/bash"]
# Tue, 12 May 2026 09:13:32 GMT
COPY file:595171150af68abc798ea385f7988d74b566aa8e84babff137f00b08b2164683 in /usr/share/buildinfo/content-sets.json      
# Tue, 12 May 2026 09:13:32 GMT
COPY file:595171150af68abc798ea385f7988d74b566aa8e84babff137f00b08b2164683 in /root/buildinfo/content_manifests/content-sets.json      
# Tue, 12 May 2026 09:13:33 GMT
COPY file:101e1b19e6d0f9785c2d23ecc61947a5882edebf262baa5a4ebcee0c3b40e8a2 in /usr/share/buildinfo/labels.json      
# Tue, 12 May 2026 09:13:33 GMT
COPY file:101e1b19e6d0f9785c2d23ecc61947a5882edebf262baa5a4ebcee0c3b40e8a2 in /root/buildinfo/labels.json      
# Tue, 12 May 2026 09:13:33 GMT
LABEL "architecture"="ppc64le" "vcs-type"="git" "vcs-ref"="ad7cdeeb08da8825126b10f488e410b0de5902b0" "org.opencontainers.image.revision"="ad7cdeeb08da8825126b10f488e410b0de5902b0" "build-date"="2026-05-12T09:13:14Z" "org.opencontainers.image.created"="2026-05-12T09:13:14Z" "release"="1778576723"org.opencontainers.image.revision=ad7cdeeb08da8825126b10f488e410b0de5902b0,org.opencontainers.image.created=2026-05-12T09:13:14Z
# Tue, 12 May 2026 23:31:50 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 12 May 2026 23:31:50 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 May 2026 23:31:50 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 12 May 2026 23:31:50 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en         gnupg2     ;     microdnf clean all # buildkit
# Tue, 12 May 2026 23:31:50 GMT
ENV JAVA_VERSION=jdk-11.0.31+11
# Tue, 12 May 2026 23:34:54 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='eabe05fb80626ad24db17cf1df137855e77fbacbc83c11aaf243cedd224467de';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.31%2B11/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.31_11.tar.gz';          ;;        ppc64le)          ESUM='11e58bf1eeae10f0dc1a98cc43bf97af270a0b516f6ff9fb3189024c5e22550a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.31%2B11/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.31_11.tar.gz';          ;;        s390x)          ESUM='4c311b19aa3922951be288076f0f41a831ab7af32284da9b3e21cdaa251a078a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.31%2B11/OpenJDK11U-jre_s390x_linux_hotspot_11.0.31_11.tar.gz';          ;;        x86_64)          ESUM='a6af3d61851f57eb79ef0189837522329717458bf230ee284da2d26634f1ea3a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.31%2B11/OpenJDK11U-jre_x64_linux_hotspot_11.0.31_11.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz; # buildkit
# Tue, 12 May 2026 23:34:55 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 12 May 2026 23:34:57 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 12 May 2026 23:34:57 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
```

-	Layers:
	-	`sha256:f815e851aa9d271f09d3448e8acc95ebed62472057c9b0368d01b242d1468875`  
		Last Modified: Tue, 12 May 2026 12:16:14 GMT  
		Size: 38.8 MB (38794493 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d1fdf741746dd4482bfc42d70a6f2954201df0346c653d262b3e220a6a63447`  
		Last Modified: Tue, 12 May 2026 23:32:30 GMT  
		Size: 39.3 MB (39255778 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9939b0dcc880bb045a14ad95c1b513552141763c91e768c99877d37bb533eb8e`  
		Last Modified: Tue, 12 May 2026 23:35:25 GMT  
		Size: 39.9 MB (39861959 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b14efb1bdd52925a4509f59759e25ffe990a43b7cd09e66ea887057cd5f1c92e`  
		Last Modified: Tue, 12 May 2026 23:35:21 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc12eda6ec2babbe9e8e87294c8f1398e12311ae4c5b16cbfb4188defdf222ae`  
		Last Modified: Tue, 12 May 2026 23:35:23 GMT  
		Size: 2.3 KB (2291 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:11-jre-ubi10-minimal` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:2b49ab3b65b1cf6ccd3aa2623c3b53e91bc486edd251318f57581e968638b374
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3727018 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:027aee2e883a54f5df8bc4e1b5b32a3b38fe709dd3db2d506e27187915807c96`

```dockerfile
```

-	Layers:
	-	`sha256:4fb5c259af10159ae2a50a52f986f6c0d8f14cb884ae889656ee36be12006d27`  
		Last Modified: Tue, 12 May 2026 23:35:23 GMT  
		Size: 3.7 MB (3706610 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:48fd4bdc649863779a61c9f107cad48c05ce5eb4baa1486e2dcd7f9758a06eb6`  
		Last Modified: Tue, 12 May 2026 23:35:23 GMT  
		Size: 20.4 KB (20408 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-temurin:11-jre-ubi10-minimal` - linux; s390x

```console
$ docker pull eclipse-temurin@sha256:f5ef4e6c487e110014f4bb79076f842bcffa0c8f41b7c66925fba09ef013c9d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **110.7 MB (110662745 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b93619350fd1f628bbc18a7bbe3f870579bd9521d1f67d821d7d883485fe8cb1`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`

```dockerfile
# Tue, 12 May 2026 09:27:49 GMT
LABEL maintainer="Red Hat, Inc."
# Tue, 12 May 2026 09:27:49 GMT
LABEL vendor="Red Hat, Inc."
# Tue, 12 May 2026 09:27:49 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Tue, 12 May 2026 09:27:49 GMT
LABEL com.redhat.component="ubi10-minimal-container"       name="ubi10/ubi-minimal"       version="10.1"       cpe="cpe:/o:redhat:enterprise_linux:10.1"       distribution-scope="public"
# Tue, 12 May 2026 09:27:49 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Tue, 12 May 2026 09:27:49 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 10."
# Tue, 12 May 2026 09:27:49 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Tue, 12 May 2026 09:27:49 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Tue, 12 May 2026 09:27:49 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 10 Minimal"
# Tue, 12 May 2026 09:27:49 GMT
LABEL io.openshift.expose-services=""
# Tue, 12 May 2026 09:27:49 GMT
LABEL io.openshift.tags="minimal rhel10"
# Tue, 12 May 2026 09:27:49 GMT
ENV container oci
# Tue, 12 May 2026 09:27:49 GMT
COPY dir:ad73fd8372aea6e68c9b3ea90e4901b979a82fb0f4a43074fa7ea61354ab30b9 in /      
# Tue, 12 May 2026 09:27:49 GMT
COPY file:5de33b5fc08b00635bccf9134a18978dba13e2250aa51838f9969515a3957847 in /etc/yum.repos.d/.      
# Tue, 12 May 2026 09:27:49 GMT
CMD ["/bin/bash"]
# Tue, 12 May 2026 09:27:49 GMT
COPY file:595171150af68abc798ea385f7988d74b566aa8e84babff137f00b08b2164683 in /usr/share/buildinfo/content-sets.json      
# Tue, 12 May 2026 09:27:50 GMT
COPY file:595171150af68abc798ea385f7988d74b566aa8e84babff137f00b08b2164683 in /root/buildinfo/content_manifests/content-sets.json      
# Tue, 12 May 2026 09:27:50 GMT
COPY file:f69727366f08991ceef4955068ba3462c331e0d11189e73f45fe959e3f50f354 in /usr/share/buildinfo/labels.json      
# Tue, 12 May 2026 09:27:50 GMT
COPY file:f69727366f08991ceef4955068ba3462c331e0d11189e73f45fe959e3f50f354 in /root/buildinfo/labels.json      
# Tue, 12 May 2026 09:27:50 GMT
LABEL "architecture"="s390x" "vcs-type"="git" "vcs-ref"="ad7cdeeb08da8825126b10f488e410b0de5902b0" "org.opencontainers.image.revision"="ad7cdeeb08da8825126b10f488e410b0de5902b0" "build-date"="2026-05-12T09:27:06Z" "org.opencontainers.image.created"="2026-05-12T09:27:06Z" "release"="1778576723"org.opencontainers.image.revision=ad7cdeeb08da8825126b10f488e410b0de5902b0,org.opencontainers.image.created=2026-05-12T09:27:06Z
# Tue, 12 May 2026 23:33:21 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 12 May 2026 23:33:21 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 May 2026 23:33:21 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 12 May 2026 23:33:21 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en         gnupg2     ;     microdnf clean all # buildkit
# Tue, 12 May 2026 23:33:21 GMT
ENV JAVA_VERSION=jdk-11.0.31+11
# Tue, 12 May 2026 23:33:25 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='eabe05fb80626ad24db17cf1df137855e77fbacbc83c11aaf243cedd224467de';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.31%2B11/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.31_11.tar.gz';          ;;        ppc64le)          ESUM='11e58bf1eeae10f0dc1a98cc43bf97af270a0b516f6ff9fb3189024c5e22550a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.31%2B11/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.31_11.tar.gz';          ;;        s390x)          ESUM='4c311b19aa3922951be288076f0f41a831ab7af32284da9b3e21cdaa251a078a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.31%2B11/OpenJDK11U-jre_s390x_linux_hotspot_11.0.31_11.tar.gz';          ;;        x86_64)          ESUM='a6af3d61851f57eb79ef0189837522329717458bf230ee284da2d26634f1ea3a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.31%2B11/OpenJDK11U-jre_x64_linux_hotspot_11.0.31_11.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz; # buildkit
# Tue, 12 May 2026 23:33:25 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 12 May 2026 23:33:25 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 12 May 2026 23:33:25 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
```

-	Layers:
	-	`sha256:716b8ccfad2ab26e031483f83283392459a7160cf7d641599a620a485af51f10`  
		Last Modified: Tue, 12 May 2026 12:16:04 GMT  
		Size: 34.5 MB (34450081 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2bc9efccaf12b37be6730ba1e31ac63abf961e8edbd64e5978191049713f989`  
		Last Modified: Tue, 12 May 2026 23:33:51 GMT  
		Size: 37.9 MB (37879927 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a344120fba6e25befcb4d6efa9bab8f3524f78939edc7b9d4e9ce17a8d30376`  
		Last Modified: Tue, 12 May 2026 23:33:52 GMT  
		Size: 38.3 MB (38330320 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b54e0255adee0ea9565b9ba3d5d69d0eac777e9932fdfaa9fcfe598f2d30bc2`  
		Last Modified: Tue, 12 May 2026 23:33:39 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ed55f45dbc575903afef42ed4919e8647f048898999d588001fd10eeb266486`  
		Last Modified: Tue, 12 May 2026 23:33:50 GMT  
		Size: 2.3 KB (2290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:11-jre-ubi10-minimal` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:85d91962bf17d9f3f262816a8ddbc007785eed647cb24c7d85fbc72475dd37fb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3728230 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dc734710125f3848ba73e36be7e5456a8dad8d4dfdedaba877e0dd73f39bc7c7`

```dockerfile
```

-	Layers:
	-	`sha256:fe1905b4f257fdf7015d7650eb0f3982c863c15a69fc219ee439d13e58d06ebc`  
		Last Modified: Tue, 12 May 2026 23:33:49 GMT  
		Size: 3.7 MB (3707855 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:90cf97af9f54e3cde8d0934594f4a88b5d4aa97951d36e4b18ea7d5fb29e5d9e`  
		Last Modified: Tue, 12 May 2026 23:33:48 GMT  
		Size: 20.4 KB (20375 bytes)  
		MIME: application/vnd.in-toto+json
