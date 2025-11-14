## `eclipse-temurin:8-jre-ubi10-minimal`

```console
$ docker pull eclipse-temurin@sha256:32e19909128cd09f11d837d50fe0730a72a186dcb60e3730a423dff74744479e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `eclipse-temurin:8-jre-ubi10-minimal` - linux; amd64

```console
$ docker pull eclipse-temurin@sha256:0e4d3854357178d39837ab482e9429fad26a9cd2e8ebb35c177ba4000bd2b194
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.6 MB (134584714 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f44a626a86311ac670ab2725cbe1bbdeacd23f52147a38761530044a117d77a2`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`

```dockerfile
# Wed, 12 Nov 2025 13:01:22 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 12 Nov 2025 13:01:22 GMT
LABEL vendor="Red Hat, Inc."
# Wed, 12 Nov 2025 13:01:22 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Wed, 12 Nov 2025 13:01:22 GMT
LABEL com.redhat.component="ubi10-minimal-container"       name="ubi10/ubi-minimal"       version="10.1"       cpe="cpe:/o:redhat:enterprise_linux:10.1"       distribution-scope="public"
# Wed, 12 Nov 2025 13:01:22 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 12 Nov 2025 13:01:22 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 10."
# Wed, 12 Nov 2025 13:01:22 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 12 Nov 2025 13:01:22 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 12 Nov 2025 13:01:22 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 10 Minimal"
# Wed, 12 Nov 2025 13:01:22 GMT
LABEL io.openshift.expose-services=""
# Wed, 12 Nov 2025 13:01:22 GMT
LABEL io.openshift.tags="minimal rhel10"
# Wed, 12 Nov 2025 13:01:22 GMT
ENV container oci
# Wed, 12 Nov 2025 13:01:23 GMT
COPY dir:f2440371cac1ecd5821b1d2fdba3a255aaff3a1a77b5c3da42649fb9aa41eacf in /      
# Wed, 12 Nov 2025 13:01:23 GMT
COPY file:5de33b5fc08b00635bccf9134a18978dba13e2250aa51838f9969515a3957847 in /etc/yum.repos.d/.      
# Wed, 12 Nov 2025 13:01:23 GMT
CMD ["/bin/bash"]
# Wed, 12 Nov 2025 13:01:23 GMT
COPY file:595171150af68abc798ea385f7988d74b566aa8e84babff137f00b08b2164683 in /usr/share/buildinfo/content-sets.json      
# Wed, 12 Nov 2025 13:01:23 GMT
COPY file:595171150af68abc798ea385f7988d74b566aa8e84babff137f00b08b2164683 in /root/buildinfo/content_manifests/content-sets.json      
# Wed, 12 Nov 2025 13:01:23 GMT
COPY file:38c762d98ec7c6a2f80e50bd0d7f55f749ddc727f82c6ec0ecf03ddb34a3b284 in /usr/share/buildinfo/labels.json      
# Wed, 12 Nov 2025 13:01:23 GMT
COPY file:38c762d98ec7c6a2f80e50bd0d7f55f749ddc727f82c6ec0ecf03ddb34a3b284 in /root/buildinfo/labels.json      
# Wed, 12 Nov 2025 13:01:23 GMT
LABEL "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="c2904cc9bad715599f86f4c20562b90929d43731" "org.opencontainers.image.revision"="c2904cc9bad715599f86f4c20562b90929d43731" "build-date"="2025-11-12T13:01:03Z" "release"="1762952303"org.opencontainers.image.revision=c2904cc9bad715599f86f4c20562b90929d43731
# Fri, 14 Nov 2025 01:12:20 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 14 Nov 2025 01:12:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 14 Nov 2025 01:12:20 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 14 Nov 2025 01:12:20 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en         gnupg2     ;     microdnf clean all # buildkit
# Fri, 14 Nov 2025 01:12:20 GMT
ENV JAVA_VERSION=jdk8u472-b08
# Fri, 14 Nov 2025 01:12:22 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='c043807ad995fb3987bc1c42b16ebf0f1b5010868c3e9d20a941236d5bbb22b7';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u472-b08/OpenJDK8U-jre_aarch64_linux_hotspot_8u472b08.tar.gz';          ;;        ppc64le)          ESUM='a76eb0f46cd5134b0b8b52ef4dd54ac7fd7e5960fc7dce8772bfc455a5e83e40';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u472-b08/OpenJDK8U-jre_ppc64le_linux_hotspot_8u472b08.tar.gz';          ;;        x86_64)          ESUM='6f7fb5fd640a0fd00837344b0920cbc4b9b9284b50e66f33789e3b250446a16e';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u472-b08/OpenJDK8U-jre_x64_linux_hotspot_8u472b08.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz; # buildkit
# Fri, 14 Nov 2025 01:12:22 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java -version"; java -version;     echo "Complete." # buildkit
# Fri, 14 Nov 2025 01:12:22 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Fri, 14 Nov 2025 01:12:22 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
```

-	Layers:
	-	`sha256:7164be7c15828f5ba5fa7731cf51dad23a5d6c99e19fa840e574def3f4c05894`  
		Last Modified: Wed, 12 Nov 2025 17:56:02 GMT  
		Size: 34.5 MB (34515519 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb8a855ba5fa3e811a5758958d49fa619f3dfae5ee0c972b482f5814e9102954`  
		Last Modified: Fri, 14 Nov 2025 01:12:54 GMT  
		Size: 58.2 MB (58179093 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:345f1b4c49bd1c9abf2cf9c6eb0c1418c7a2817f068ca33edf84b0cf8d581db5`  
		Last Modified: Fri, 14 Nov 2025 01:12:51 GMT  
		Size: 41.9 MB (41887686 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ccc61ea85954dcb5e700d5f0a450aa0a27ec257609bd99de265434304de9c86`  
		Last Modified: Fri, 14 Nov 2025 01:12:44 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c83f8537069aca3645836bad04ba44c9f6038da04c3ec2a8ca28df7a6dcbf573`  
		Last Modified: Fri, 14 Nov 2025 01:12:46 GMT  
		Size: 2.3 KB (2289 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:8-jre-ubi10-minimal` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:2e92668aadb971670ffc04d181de4858dc60b32ff52409daf09276f2585736d3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5645641 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d35c23f31a6b87323ba6d58208b9e159e22888f136b020747f30b47978bfd211`

```dockerfile
```

-	Layers:
	-	`sha256:b10f87044f229e7e9345565597bd87244c45840302be064d020ac2c7a418daa6`  
		Last Modified: Fri, 14 Nov 2025 04:19:03 GMT  
		Size: 5.6 MB (5626130 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:84d4a6e2f187ea21c4a711b9f01cd4be846cac32372175e61a5b960be7092c32`  
		Last Modified: Fri, 14 Nov 2025 04:19:05 GMT  
		Size: 19.5 KB (19511 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-temurin:8-jre-ubi10-minimal` - linux; arm64 variant v8

```console
$ docker pull eclipse-temurin@sha256:1308337031026f881c107d83cf6e000323a1cd96bc3ba0c00fee7f5ab3b6cd21
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **131.3 MB (131269796 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f2df2d477f93229e049c776a4127d7542baa52a665071b9652bcb9c71304cab`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`

```dockerfile
# Wed, 12 Nov 2025 13:07:41 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 12 Nov 2025 13:07:41 GMT
LABEL vendor="Red Hat, Inc."
# Wed, 12 Nov 2025 13:07:41 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Wed, 12 Nov 2025 13:07:41 GMT
LABEL com.redhat.component="ubi10-minimal-container"       name="ubi10/ubi-minimal"       version="10.1"       cpe="cpe:/o:redhat:enterprise_linux:10.1"       distribution-scope="public"
# Wed, 12 Nov 2025 13:07:41 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 12 Nov 2025 13:07:41 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 10."
# Wed, 12 Nov 2025 13:07:41 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 12 Nov 2025 13:07:41 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 12 Nov 2025 13:07:41 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 10 Minimal"
# Wed, 12 Nov 2025 13:07:41 GMT
LABEL io.openshift.expose-services=""
# Wed, 12 Nov 2025 13:07:41 GMT
LABEL io.openshift.tags="minimal rhel10"
# Wed, 12 Nov 2025 13:07:41 GMT
ENV container oci
# Wed, 12 Nov 2025 13:07:42 GMT
COPY dir:7dfb9511ae2d70910df52107d5c96c0335e87f2a1f5d8a5592e4e62e34a4c8d6 in /      
# Wed, 12 Nov 2025 13:07:42 GMT
COPY file:5de33b5fc08b00635bccf9134a18978dba13e2250aa51838f9969515a3957847 in /etc/yum.repos.d/.      
# Wed, 12 Nov 2025 13:07:42 GMT
CMD ["/bin/bash"]
# Wed, 12 Nov 2025 13:07:42 GMT
COPY file:595171150af68abc798ea385f7988d74b566aa8e84babff137f00b08b2164683 in /usr/share/buildinfo/content-sets.json      
# Wed, 12 Nov 2025 13:07:42 GMT
COPY file:595171150af68abc798ea385f7988d74b566aa8e84babff137f00b08b2164683 in /root/buildinfo/content_manifests/content-sets.json      
# Wed, 12 Nov 2025 13:07:42 GMT
COPY file:5949e56b1cb83ef43c9cba7c361cdb23e3aace250acdaec4205faff29b91de6c in /usr/share/buildinfo/labels.json      
# Wed, 12 Nov 2025 13:07:42 GMT
COPY file:5949e56b1cb83ef43c9cba7c361cdb23e3aace250acdaec4205faff29b91de6c in /root/buildinfo/labels.json      
# Wed, 12 Nov 2025 13:07:42 GMT
LABEL "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="c2904cc9bad715599f86f4c20562b90929d43731" "org.opencontainers.image.revision"="c2904cc9bad715599f86f4c20562b90929d43731" "build-date"="2025-11-12T13:07:20Z" "release"="1762952303"org.opencontainers.image.revision=c2904cc9bad715599f86f4c20562b90929d43731
# Fri, 14 Nov 2025 01:29:00 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 14 Nov 2025 01:29:00 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 14 Nov 2025 01:29:00 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 14 Nov 2025 01:29:00 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en         gnupg2     ;     microdnf clean all # buildkit
# Fri, 14 Nov 2025 01:29:00 GMT
ENV JAVA_VERSION=jdk8u472-b08
# Fri, 14 Nov 2025 01:29:03 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='c043807ad995fb3987bc1c42b16ebf0f1b5010868c3e9d20a941236d5bbb22b7';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u472-b08/OpenJDK8U-jre_aarch64_linux_hotspot_8u472b08.tar.gz';          ;;        ppc64le)          ESUM='a76eb0f46cd5134b0b8b52ef4dd54ac7fd7e5960fc7dce8772bfc455a5e83e40';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u472-b08/OpenJDK8U-jre_ppc64le_linux_hotspot_8u472b08.tar.gz';          ;;        x86_64)          ESUM='6f7fb5fd640a0fd00837344b0920cbc4b9b9284b50e66f33789e3b250446a16e';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u472-b08/OpenJDK8U-jre_x64_linux_hotspot_8u472b08.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz; # buildkit
# Fri, 14 Nov 2025 01:29:03 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java -version"; java -version;     echo "Complete." # buildkit
# Fri, 14 Nov 2025 01:29:03 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Fri, 14 Nov 2025 01:29:03 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
```

-	Layers:
	-	`sha256:372b71efdab733f5ad0749f1537278e34899107888219d8358967ddbd9eb2db3`  
		Last Modified: Wed, 12 Nov 2025 18:16:55 GMT  
		Size: 32.6 MB (32601501 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8dc4888be6fc0a3367114ba3f3609c9cc616577ecbdc94909455c924659c3e85`  
		Last Modified: Fri, 14 Nov 2025 01:29:40 GMT  
		Size: 57.8 MB (57785680 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbdda7c10bfca8b444b0f63b014f65ce55d79403c39e022a4e67a953ae71fa59`  
		Last Modified: Fri, 14 Nov 2025 01:29:32 GMT  
		Size: 40.9 MB (40880199 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a626ecf8415934e8086f02c67c9d7c2949034d0682ec38d4f8ca583c4ae1ab2`  
		Last Modified: Fri, 14 Nov 2025 01:29:27 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50e55d807d2c202017f114876c1874defb6978c9ca5de544f31d549f3275d7f0`  
		Last Modified: Fri, 14 Nov 2025 01:29:27 GMT  
		Size: 2.3 KB (2289 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:8-jre-ubi10-minimal` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:265e5f5b3a575038aa0babbf909ba1ecf4ce51e6864e70b852fffbb1ebdddee2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5645913 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:afac35466f6199eb3299402fe17fd2a615aeb583ecc133cbcc7bf21abf55d234`

```dockerfile
```

-	Layers:
	-	`sha256:4bd9b88ee165161e7f0f91199457433b45b5ea2b1e4308b667ea202d146a5dec`  
		Last Modified: Fri, 14 Nov 2025 04:19:11 GMT  
		Size: 5.6 MB (5626298 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:37366b9972b362737e950aa114c1d42d91a2ac0277874410165dd5564ae08b86`  
		Last Modified: Fri, 14 Nov 2025 04:19:11 GMT  
		Size: 19.6 KB (19615 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-temurin:8-jre-ubi10-minimal` - linux; ppc64le

```console
$ docker pull eclipse-temurin@sha256:72d5752bd9c747c8a2176e39265e40f7aaff1fe3d11bb416b01ec03be642c7af
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **140.4 MB (140375725 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b868d95a656ee062d4bdf51d68a96453aba9c95bda54be589b31cf459e6eddf`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`

```dockerfile
# Wed, 12 Nov 2025 13:21:41 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 12 Nov 2025 13:21:41 GMT
LABEL vendor="Red Hat, Inc."
# Wed, 12 Nov 2025 13:21:41 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Wed, 12 Nov 2025 13:21:41 GMT
LABEL com.redhat.component="ubi10-minimal-container"       name="ubi10/ubi-minimal"       version="10.1"       cpe="cpe:/o:redhat:enterprise_linux:10.1"       distribution-scope="public"
# Wed, 12 Nov 2025 13:21:41 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 12 Nov 2025 13:21:41 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 10."
# Wed, 12 Nov 2025 13:21:41 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 12 Nov 2025 13:21:41 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 12 Nov 2025 13:21:41 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 10 Minimal"
# Wed, 12 Nov 2025 13:21:41 GMT
LABEL io.openshift.expose-services=""
# Wed, 12 Nov 2025 13:21:41 GMT
LABEL io.openshift.tags="minimal rhel10"
# Wed, 12 Nov 2025 13:21:41 GMT
ENV container oci
# Wed, 12 Nov 2025 13:21:42 GMT
COPY dir:7f428fa29fa8f7e829b041452235ccc73eb7caf26242995ea3907c084b7e797f in /      
# Wed, 12 Nov 2025 13:21:42 GMT
COPY file:5de33b5fc08b00635bccf9134a18978dba13e2250aa51838f9969515a3957847 in /etc/yum.repos.d/.      
# Wed, 12 Nov 2025 13:21:42 GMT
CMD ["/bin/bash"]
# Wed, 12 Nov 2025 13:21:42 GMT
COPY file:595171150af68abc798ea385f7988d74b566aa8e84babff137f00b08b2164683 in /usr/share/buildinfo/content-sets.json      
# Wed, 12 Nov 2025 13:21:42 GMT
COPY file:595171150af68abc798ea385f7988d74b566aa8e84babff137f00b08b2164683 in /root/buildinfo/content_manifests/content-sets.json      
# Wed, 12 Nov 2025 13:21:42 GMT
COPY file:aa98cda558c12f3c05f9e28e398d23d3217b73b93e9d498cde74f10837d73035 in /usr/share/buildinfo/labels.json      
# Wed, 12 Nov 2025 13:21:42 GMT
COPY file:aa98cda558c12f3c05f9e28e398d23d3217b73b93e9d498cde74f10837d73035 in /root/buildinfo/labels.json      
# Wed, 12 Nov 2025 13:21:42 GMT
LABEL "architecture"="ppc64le" "vcs-type"="git" "vcs-ref"="c2904cc9bad715599f86f4c20562b90929d43731" "org.opencontainers.image.revision"="c2904cc9bad715599f86f4c20562b90929d43731" "build-date"="2025-11-12T13:21:30Z" "release"="1762952303"org.opencontainers.image.revision=c2904cc9bad715599f86f4c20562b90929d43731
# Fri, 14 Nov 2025 02:04:01 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 14 Nov 2025 02:04:01 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 14 Nov 2025 02:04:01 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 14 Nov 2025 02:04:01 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en         gnupg2     ;     microdnf clean all # buildkit
# Fri, 14 Nov 2025 02:04:01 GMT
ENV JAVA_VERSION=jdk8u472-b08
# Fri, 14 Nov 2025 02:07:07 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='c043807ad995fb3987bc1c42b16ebf0f1b5010868c3e9d20a941236d5bbb22b7';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u472-b08/OpenJDK8U-jre_aarch64_linux_hotspot_8u472b08.tar.gz';          ;;        ppc64le)          ESUM='a76eb0f46cd5134b0b8b52ef4dd54ac7fd7e5960fc7dce8772bfc455a5e83e40';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u472-b08/OpenJDK8U-jre_ppc64le_linux_hotspot_8u472b08.tar.gz';          ;;        x86_64)          ESUM='6f7fb5fd640a0fd00837344b0920cbc4b9b9284b50e66f33789e3b250446a16e';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u472-b08/OpenJDK8U-jre_x64_linux_hotspot_8u472b08.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz; # buildkit
# Fri, 14 Nov 2025 02:07:08 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java -version"; java -version;     echo "Complete." # buildkit
# Fri, 14 Nov 2025 02:07:08 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Fri, 14 Nov 2025 02:07:08 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
```

-	Layers:
	-	`sha256:402f9c025c3a63d9edbbd78a8cf9e2813de76854342058db2814aa404ddbcf6c`  
		Last Modified: Wed, 12 Nov 2025 18:16:57 GMT  
		Size: 38.7 MB (38746677 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6af666f8de2b0c285f4b7d038631ab495275355fdde5c07cca653c2f3d29143`  
		Last Modified: Fri, 14 Nov 2025 02:05:21 GMT  
		Size: 60.4 MB (60357723 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67e72ee79fe3b39e331e13bfb0ceb91af1e20a82f24e27c07e67c4eac05d691b`  
		Last Modified: Fri, 14 Nov 2025 02:07:51 GMT  
		Size: 41.3 MB (41268907 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3ad5c9eea83657b81f1023195fa7012efda84504d53908b32c284cca1993a96`  
		Last Modified: Fri, 14 Nov 2025 02:07:47 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5af58fdd1ae848cdc8b765f10ce606e117c0a56d84e7f872683cc1dae928891c`  
		Last Modified: Fri, 14 Nov 2025 02:07:47 GMT  
		Size: 2.3 KB (2291 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:8-jre-ubi10-minimal` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:35d61667f6518f5e7520e856bab066891290ee17f85bd3b87b95798e549f64b4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5635426 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0eda798203217949c469ff63d686a9cf2e9359ea81e4389fc5af9e1c8836389e`

```dockerfile
```

-	Layers:
	-	`sha256:07fe51207b43bebeba45edf622f5b0f961e242aaf5fcf86c05d929b392029384`  
		Last Modified: Fri, 14 Nov 2025 04:19:16 GMT  
		Size: 5.6 MB (5615885 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c7c7e59e3eddf3579801c6e60bc44552dbe51bea899452915b1588776a24558a`  
		Last Modified: Fri, 14 Nov 2025 04:19:17 GMT  
		Size: 19.5 KB (19541 bytes)  
		MIME: application/vnd.in-toto+json
