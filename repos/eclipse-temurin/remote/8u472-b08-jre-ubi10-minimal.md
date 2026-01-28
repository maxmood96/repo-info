## `eclipse-temurin:8u472-b08-jre-ubi10-minimal`

```console
$ docker pull eclipse-temurin@sha256:46b1d5e6239b4000512da5865380c2a38e43e9ec979ff9b630e9af96af49370d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `eclipse-temurin:8u472-b08-jre-ubi10-minimal` - linux; amd64

```console
$ docker pull eclipse-temurin@sha256:97ff0b47cfffc072b47457d957aef536271b38523a876fc3f47501e3b443849d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **116.7 MB (116664029 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:38518db53982d687fa40d4845dcdcaba71d7a59761d7760038772402869ca551`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`

```dockerfile
# Tue, 27 Jan 2026 13:43:38 GMT
LABEL maintainer="Red Hat, Inc."
# Tue, 27 Jan 2026 13:43:38 GMT
LABEL vendor="Red Hat, Inc."
# Tue, 27 Jan 2026 13:43:38 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Tue, 27 Jan 2026 13:43:38 GMT
LABEL com.redhat.component="ubi10-minimal-container"       name="ubi10/ubi-minimal"       version="10.1"       cpe="cpe:/o:redhat:enterprise_linux:10.1"       distribution-scope="public"
# Tue, 27 Jan 2026 13:43:38 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Tue, 27 Jan 2026 13:43:39 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 10."
# Tue, 27 Jan 2026 13:43:39 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Tue, 27 Jan 2026 13:43:39 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Tue, 27 Jan 2026 13:43:39 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 10 Minimal"
# Tue, 27 Jan 2026 13:43:39 GMT
LABEL io.openshift.expose-services=""
# Tue, 27 Jan 2026 13:43:39 GMT
LABEL io.openshift.tags="minimal rhel10"
# Tue, 27 Jan 2026 13:43:39 GMT
ENV container oci
# Tue, 27 Jan 2026 13:43:40 GMT
COPY dir:c206a7c74c2764db52e4fe9e9bb5506227dd2a550e47afa696c9a7c923f9a0ff in /      
# Tue, 27 Jan 2026 13:43:40 GMT
COPY file:5de33b5fc08b00635bccf9134a18978dba13e2250aa51838f9969515a3957847 in /etc/yum.repos.d/.      
# Tue, 27 Jan 2026 13:43:40 GMT
CMD ["/bin/bash"]
# Tue, 27 Jan 2026 13:43:40 GMT
COPY file:595171150af68abc798ea385f7988d74b566aa8e84babff137f00b08b2164683 in /usr/share/buildinfo/content-sets.json      
# Tue, 27 Jan 2026 13:43:40 GMT
COPY file:595171150af68abc798ea385f7988d74b566aa8e84babff137f00b08b2164683 in /root/buildinfo/content_manifests/content-sets.json      
# Tue, 27 Jan 2026 13:43:40 GMT
COPY file:8db1dc4b84412d8a3137b92a8b51dc81382218dadd1dc925bd2c056986c8eb72 in /usr/share/buildinfo/labels.json      
# Tue, 27 Jan 2026 13:43:40 GMT
COPY file:8db1dc4b84412d8a3137b92a8b51dc81382218dadd1dc925bd2c056986c8eb72 in /root/buildinfo/labels.json      
# Tue, 27 Jan 2026 13:43:40 GMT
LABEL "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="2945215ed3e1eed38f41b60201d6d7def9446c9f" "org.opencontainers.image.revision"="2945215ed3e1eed38f41b60201d6d7def9446c9f" "build-date"="2026-01-27T13:43:17Z" "org.opencontainers.image.created"="2026-01-27T13:43:17Z" "release"="1769521234"org.opencontainers.image.revision=2945215ed3e1eed38f41b60201d6d7def9446c9f,org.opencontainers.image.created=2026-01-27T13:43:17Z
# Wed, 28 Jan 2026 19:00:39 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 28 Jan 2026 19:00:39 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 28 Jan 2026 19:00:39 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 28 Jan 2026 19:00:39 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en         gnupg2     ;     microdnf clean all # buildkit
# Wed, 28 Jan 2026 19:00:39 GMT
ENV JAVA_VERSION=jdk8u472-b08
# Wed, 28 Jan 2026 19:00:42 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='c043807ad995fb3987bc1c42b16ebf0f1b5010868c3e9d20a941236d5bbb22b7';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u472-b08/OpenJDK8U-jre_aarch64_linux_hotspot_8u472b08.tar.gz';          ;;        ppc64le)          ESUM='a76eb0f46cd5134b0b8b52ef4dd54ac7fd7e5960fc7dce8772bfc455a5e83e40';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u472-b08/OpenJDK8U-jre_ppc64le_linux_hotspot_8u472b08.tar.gz';          ;;        x86_64)          ESUM='6f7fb5fd640a0fd00837344b0920cbc4b9b9284b50e66f33789e3b250446a16e';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u472-b08/OpenJDK8U-jre_x64_linux_hotspot_8u472b08.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz; # buildkit
# Wed, 28 Jan 2026 19:00:42 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java -version"; java -version;     echo "Complete." # buildkit
# Wed, 28 Jan 2026 19:00:42 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 28 Jan 2026 19:00:42 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
```

-	Layers:
	-	`sha256:6af7d70117fb54a1c19fa7ab0dd6387be5ab897497b2986acffbb49ebe56b290`  
		Last Modified: Tue, 27 Jan 2026 17:15:27 GMT  
		Size: 34.6 MB (34556452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf9f43f89163703a5ad210893837e14e26c900f728b405f5ed19d147e9b95d5e`  
		Last Modified: Wed, 28 Jan 2026 19:01:05 GMT  
		Size: 40.2 MB (40217468 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d03762d2026e751a1c23d78e5c54bd2077849176bfaa395fcda35224a0cd0e8`  
		Last Modified: Wed, 28 Jan 2026 19:01:00 GMT  
		Size: 41.9 MB (41887691 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24c330ac5dbd571e2d244624a0370f15f5cf7124a591715e4cc7a4f3cbe89ecf`  
		Last Modified: Wed, 28 Jan 2026 19:00:58 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a0ade64b77998e5cd3e8b59a891e8f0f47f17c605f42efcc9766fd8bd393724`  
		Last Modified: Wed, 28 Jan 2026 19:01:00 GMT  
		Size: 2.3 KB (2289 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:8u472-b08-jre-ubi10-minimal` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:8e2c804170afb9c6801a1ad1c9eb5e6877ecbe5d1e1aeebc1def83fd82b1939a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3753592 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1be7fa5dbb2d1f8e1af75ef10586aede7ca8254a36f90ce883fdeaaaa1314235`

```dockerfile
```

-	Layers:
	-	`sha256:996bd58f64c7da7752fd52beaa10cb2c7534bb29d082b1c1b5eadecfbadaf53e`  
		Last Modified: Wed, 28 Jan 2026 19:00:58 GMT  
		Size: 3.7 MB (3734081 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9e298f0d5253af30ccfc2a86534b07349c4ee9271c8356e9d0a62173b65ea82d`  
		Last Modified: Wed, 28 Jan 2026 19:00:55 GMT  
		Size: 19.5 KB (19511 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-temurin:8u472-b08-jre-ubi10-minimal` - linux; arm64 variant v8

```console
$ docker pull eclipse-temurin@sha256:7f5eb8c4dc963172462f8da277e101529860bf3fbd0cda6314a9b87b7134c644
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **110.8 MB (110811886 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c9c7327d06dd99353b28651b62d0d76d1aa84151017021e0fc8d567c2974d9f`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`

```dockerfile
# Thu, 22 Jan 2026 14:10:51 GMT
LABEL maintainer="Red Hat, Inc."
# Thu, 22 Jan 2026 14:10:51 GMT
LABEL vendor="Red Hat, Inc."
# Thu, 22 Jan 2026 14:10:51 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Thu, 22 Jan 2026 14:10:51 GMT
LABEL com.redhat.component="ubi10-minimal-container"       name="ubi10/ubi-minimal"       version="10.1"       cpe="cpe:/o:redhat:enterprise_linux:10.1"       distribution-scope="public"
# Thu, 22 Jan 2026 14:10:51 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Thu, 22 Jan 2026 14:10:51 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 10."
# Thu, 22 Jan 2026 14:10:51 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 22 Jan 2026 14:10:51 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 22 Jan 2026 14:10:51 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 10 Minimal"
# Thu, 22 Jan 2026 14:10:51 GMT
LABEL io.openshift.expose-services=""
# Thu, 22 Jan 2026 14:10:51 GMT
LABEL io.openshift.tags="minimal rhel10"
# Thu, 22 Jan 2026 14:10:51 GMT
ENV container oci
# Thu, 22 Jan 2026 14:10:52 GMT
COPY dir:909d569786ad4226e9c77ee4fc4d27953d579517f60f8a0f25e4d85964a100a3 in /      
# Thu, 22 Jan 2026 14:10:52 GMT
COPY file:5de33b5fc08b00635bccf9134a18978dba13e2250aa51838f9969515a3957847 in /etc/yum.repos.d/.      
# Thu, 22 Jan 2026 14:10:52 GMT
CMD ["/bin/bash"]
# Thu, 22 Jan 2026 14:10:52 GMT
COPY file:595171150af68abc798ea385f7988d74b566aa8e84babff137f00b08b2164683 in /usr/share/buildinfo/content-sets.json      
# Thu, 22 Jan 2026 14:10:52 GMT
COPY file:595171150af68abc798ea385f7988d74b566aa8e84babff137f00b08b2164683 in /root/buildinfo/content_manifests/content-sets.json      
# Thu, 22 Jan 2026 14:10:52 GMT
COPY file:ea81599b2ebb991911687a996e9dca425fe171d768273735cf8dd2c299ff0d3d in /usr/share/buildinfo/labels.json      
# Thu, 22 Jan 2026 14:10:52 GMT
COPY file:ea81599b2ebb991911687a996e9dca425fe171d768273735cf8dd2c299ff0d3d in /root/buildinfo/labels.json      
# Thu, 22 Jan 2026 14:10:52 GMT
LABEL "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="0912ab420a80f21132d8a5e29d19a23339176677" "org.opencontainers.image.revision"="0912ab420a80f21132d8a5e29d19a23339176677" "build-date"="2026-01-22T14:10:29Z" "org.opencontainers.image.created"="2026-01-22T14:10:29Z" "release"="1769090502"org.opencontainers.image.revision=0912ab420a80f21132d8a5e29d19a23339176677,org.opencontainers.image.created=2026-01-22T14:10:29Z
# Fri, 23 Jan 2026 00:58:22 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 23 Jan 2026 00:58:22 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 23 Jan 2026 00:58:22 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 23 Jan 2026 00:58:22 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en         gnupg2     ;     microdnf clean all # buildkit
# Fri, 23 Jan 2026 00:58:22 GMT
ENV JAVA_VERSION=jdk8u472-b08
# Fri, 23 Jan 2026 00:58:26 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='c043807ad995fb3987bc1c42b16ebf0f1b5010868c3e9d20a941236d5bbb22b7';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u472-b08/OpenJDK8U-jre_aarch64_linux_hotspot_8u472b08.tar.gz';          ;;        ppc64le)          ESUM='a76eb0f46cd5134b0b8b52ef4dd54ac7fd7e5960fc7dce8772bfc455a5e83e40';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u472-b08/OpenJDK8U-jre_ppc64le_linux_hotspot_8u472b08.tar.gz';          ;;        x86_64)          ESUM='6f7fb5fd640a0fd00837344b0920cbc4b9b9284b50e66f33789e3b250446a16e';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u472-b08/OpenJDK8U-jre_x64_linux_hotspot_8u472b08.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz; # buildkit
# Fri, 23 Jan 2026 00:58:26 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java -version"; java -version;     echo "Complete." # buildkit
# Fri, 23 Jan 2026 00:58:26 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Fri, 23 Jan 2026 00:58:26 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
```

-	Layers:
	-	`sha256:855d6cc175ead513a1945d3f0933680ee64146fa0bb48e8f15fcefa1fe9b0b14`  
		Last Modified: Thu, 22 Jan 2026 17:36:15 GMT  
		Size: 32.6 MB (32613686 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec5126df4c87caee6494718693ad8240f44d25aaad7929df5fc7c27713bc0fed`  
		Last Modified: Fri, 23 Jan 2026 00:58:41 GMT  
		Size: 37.3 MB (37315577 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:208647b4d9266880ef4687cb1893b49422617e671906fdd8e48e9d9c1e5a947e`  
		Last Modified: Fri, 23 Jan 2026 00:58:41 GMT  
		Size: 40.9 MB (40880203 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7eaa156e6061700466da2d340b110ac0685652f94c503ae5f71f6a6f844442c5`  
		Last Modified: Fri, 23 Jan 2026 00:58:39 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4935554bffa52332385e4c03f4a5242ff6b73fade79cf81da5bb2a16acd5128a`  
		Last Modified: Fri, 23 Jan 2026 00:58:40 GMT  
		Size: 2.3 KB (2291 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:8u472-b08-jre-ubi10-minimal` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:f930fe81d276b9897735d30b35569c7cea9b39fab12801416b59e30a5726e510
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3753800 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:02a0d2a972af742cfd8c765b74f7b1f79bdfdd224d89fec77345e7dbf370763e`

```dockerfile
```

-	Layers:
	-	`sha256:3b0b6a4161ea807729c0f333ad25677494c18484df83d107ec346bead050c4c4`  
		Last Modified: Fri, 23 Jan 2026 00:58:39 GMT  
		Size: 3.7 MB (3734185 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:36f76ac0115cbb67a117e9b0a4bf31c49e408fc2ab78be673f9b4836905afe15`  
		Last Modified: Fri, 23 Jan 2026 00:58:39 GMT  
		Size: 19.6 KB (19615 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-temurin:8u472-b08-jre-ubi10-minimal` - linux; ppc64le

```console
$ docker pull eclipse-temurin@sha256:95ff1fa40652a7ad88492ede7bc34a7cbdee96a4437aee52eb70468a4f99cff0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **119.0 MB (119036366 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff66e1572284cfce174b93527a607e9e683500eb270777dadfb580172f473a17`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`

```dockerfile
# Tue, 27 Jan 2026 15:50:35 GMT
LABEL maintainer="Red Hat, Inc."
# Tue, 27 Jan 2026 15:50:35 GMT
LABEL vendor="Red Hat, Inc."
# Tue, 27 Jan 2026 15:50:35 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Tue, 27 Jan 2026 15:50:35 GMT
LABEL com.redhat.component="ubi10-minimal-container"       name="ubi10/ubi-minimal"       version="10.1"       cpe="cpe:/o:redhat:enterprise_linux:10.1"       distribution-scope="public"
# Tue, 27 Jan 2026 15:50:35 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Tue, 27 Jan 2026 15:50:35 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 10."
# Tue, 27 Jan 2026 15:50:35 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Tue, 27 Jan 2026 15:50:35 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Tue, 27 Jan 2026 15:50:35 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 10 Minimal"
# Tue, 27 Jan 2026 15:50:35 GMT
LABEL io.openshift.expose-services=""
# Tue, 27 Jan 2026 15:50:35 GMT
LABEL io.openshift.tags="minimal rhel10"
# Tue, 27 Jan 2026 15:50:35 GMT
ENV container oci
# Tue, 27 Jan 2026 15:50:36 GMT
COPY dir:b1fb54cba477aa8e5cc12c75f143c33f00068a49e572e2a9058ca695db013356 in /      
# Tue, 27 Jan 2026 15:50:36 GMT
COPY file:5de33b5fc08b00635bccf9134a18978dba13e2250aa51838f9969515a3957847 in /etc/yum.repos.d/.      
# Tue, 27 Jan 2026 15:50:36 GMT
CMD ["/bin/bash"]
# Tue, 27 Jan 2026 15:50:36 GMT
COPY file:595171150af68abc798ea385f7988d74b566aa8e84babff137f00b08b2164683 in /usr/share/buildinfo/content-sets.json      
# Tue, 27 Jan 2026 15:50:36 GMT
COPY file:595171150af68abc798ea385f7988d74b566aa8e84babff137f00b08b2164683 in /root/buildinfo/content_manifests/content-sets.json      
# Tue, 27 Jan 2026 15:50:36 GMT
COPY file:7b0b7973b756ae5fa48a994ea290e7e8ecbd19057a845071702a88d3f44c82d7 in /usr/share/buildinfo/labels.json      
# Tue, 27 Jan 2026 15:50:36 GMT
COPY file:7b0b7973b756ae5fa48a994ea290e7e8ecbd19057a845071702a88d3f44c82d7 in /root/buildinfo/labels.json      
# Tue, 27 Jan 2026 15:50:36 GMT
LABEL "architecture"="ppc64le" "vcs-type"="git" "vcs-ref"="2945215ed3e1eed38f41b60201d6d7def9446c9f" "org.opencontainers.image.revision"="2945215ed3e1eed38f41b60201d6d7def9446c9f" "build-date"="2026-01-27T15:50:23Z" "org.opencontainers.image.created"="2026-01-27T15:50:23Z" "release"="1769521234"org.opencontainers.image.revision=2945215ed3e1eed38f41b60201d6d7def9446c9f,org.opencontainers.image.created=2026-01-27T15:50:23Z
# Wed, 28 Jan 2026 18:56:47 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 28 Jan 2026 18:56:47 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 28 Jan 2026 18:56:47 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 28 Jan 2026 18:56:47 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en         gnupg2     ;     microdnf clean all # buildkit
# Wed, 28 Jan 2026 18:56:47 GMT
ENV JAVA_VERSION=jdk8u472-b08
# Wed, 28 Jan 2026 18:56:54 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='c043807ad995fb3987bc1c42b16ebf0f1b5010868c3e9d20a941236d5bbb22b7';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u472-b08/OpenJDK8U-jre_aarch64_linux_hotspot_8u472b08.tar.gz';          ;;        ppc64le)          ESUM='a76eb0f46cd5134b0b8b52ef4dd54ac7fd7e5960fc7dce8772bfc455a5e83e40';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u472-b08/OpenJDK8U-jre_ppc64le_linux_hotspot_8u472b08.tar.gz';          ;;        x86_64)          ESUM='6f7fb5fd640a0fd00837344b0920cbc4b9b9284b50e66f33789e3b250446a16e';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u472-b08/OpenJDK8U-jre_x64_linux_hotspot_8u472b08.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz; # buildkit
# Wed, 28 Jan 2026 18:56:55 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java -version"; java -version;     echo "Complete." # buildkit
# Wed, 28 Jan 2026 18:56:56 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 28 Jan 2026 18:56:56 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
```

-	Layers:
	-	`sha256:ae80e80c08d44fa3239f0258ba6b08c404cdebc7b53393a151fa1f93bcf7bf6e`  
		Last Modified: Tue, 27 Jan 2026 18:12:32 GMT  
		Size: 38.6 MB (38638820 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a3882d9c01ea5c0cb5dd62cb2df6f92c42b9844d566e2f851eefbf5dc55868c`  
		Last Modified: Wed, 28 Jan 2026 18:57:36 GMT  
		Size: 39.1 MB (39126257 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7cc5335e50d3af4dc3e264b2a3f20f69fbc4bc1d8a24d0dc20e48adf9659a0ee`  
		Last Modified: Wed, 28 Jan 2026 18:57:36 GMT  
		Size: 41.3 MB (41268871 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af782b19491eced1d66d2c1bcb5ba88ea15841a1ec0ef35f4c79284bf0f897d3`  
		Last Modified: Wed, 28 Jan 2026 18:57:33 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9bac6f1816882e8c7dabcd11f43d756ce998722c9d3fd3dac7e797a14a2111b`  
		Last Modified: Wed, 28 Jan 2026 18:57:35 GMT  
		Size: 2.3 KB (2291 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:8u472-b08-jre-ubi10-minimal` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:50b7a55f7562f06a4baa6958c0d51ae6e75226184412fe00ac6394a5b6f03852
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3743057 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:14b368e93829ac7aeaa728281fe2cf50ef0ed1e676f7c373372d8eed0566005f`

```dockerfile
```

-	Layers:
	-	`sha256:31353a961badb0cde67d13dab5610785c6e2375ae8eabcf8f112c50ceeedfdcd`  
		Last Modified: Wed, 28 Jan 2026 18:57:34 GMT  
		Size: 3.7 MB (3723516 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:eea1d18ebdaaccdbe48dbfc79e2b9131f329118cfce52afe71ea082f5f8b9df4`  
		Last Modified: Wed, 28 Jan 2026 18:57:33 GMT  
		Size: 19.5 KB (19541 bytes)  
		MIME: application/vnd.in-toto+json
