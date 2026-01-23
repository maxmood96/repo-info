## `eclipse-temurin:11-ubi10-minimal`

```console
$ docker pull eclipse-temurin@sha256:53a357003a8453db6a7e5bb2d709e437ba6128d96efdacc7342dad6ebea87abc
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

### `eclipse-temurin:11-ubi10-minimal` - linux; amd64

```console
$ docker pull eclipse-temurin@sha256:315e702f2aabf9e06538958968c75bb67a39690067f2e81ef1f4bc74a1cf963f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **213.3 MB (213328253 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d65a56aeb7423d97e67ade55e9ef854c7893d53a4990ef2ced2b623d8a97d052`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 22 Jan 2026 14:19:49 GMT
LABEL maintainer="Red Hat, Inc."
# Thu, 22 Jan 2026 14:19:49 GMT
LABEL vendor="Red Hat, Inc."
# Thu, 22 Jan 2026 14:19:49 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Thu, 22 Jan 2026 14:19:49 GMT
LABEL com.redhat.component="ubi10-minimal-container"       name="ubi10/ubi-minimal"       version="10.1"       cpe="cpe:/o:redhat:enterprise_linux:10.1"       distribution-scope="public"
# Thu, 22 Jan 2026 14:19:49 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Thu, 22 Jan 2026 14:19:49 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 10."
# Thu, 22 Jan 2026 14:19:49 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 22 Jan 2026 14:19:49 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 22 Jan 2026 14:19:49 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 10 Minimal"
# Thu, 22 Jan 2026 14:19:49 GMT
LABEL io.openshift.expose-services=""
# Thu, 22 Jan 2026 14:19:49 GMT
LABEL io.openshift.tags="minimal rhel10"
# Thu, 22 Jan 2026 14:19:49 GMT
ENV container oci
# Thu, 22 Jan 2026 14:19:50 GMT
COPY dir:4f39f7f54b1623f2373491e5bcb10b3c35efaa04126f246c1c0ae784bb3d7f42 in /      
# Thu, 22 Jan 2026 14:19:50 GMT
COPY file:5de33b5fc08b00635bccf9134a18978dba13e2250aa51838f9969515a3957847 in /etc/yum.repos.d/.      
# Thu, 22 Jan 2026 14:19:50 GMT
CMD ["/bin/bash"]
# Thu, 22 Jan 2026 14:19:50 GMT
COPY file:595171150af68abc798ea385f7988d74b566aa8e84babff137f00b08b2164683 in /usr/share/buildinfo/content-sets.json      
# Thu, 22 Jan 2026 14:19:50 GMT
COPY file:595171150af68abc798ea385f7988d74b566aa8e84babff137f00b08b2164683 in /root/buildinfo/content_manifests/content-sets.json      
# Thu, 22 Jan 2026 14:19:50 GMT
COPY file:e86693423cdd34ed7ac6eb4c5f916f086a37eeca572019e4cfd639c87f98a6ae in /usr/share/buildinfo/labels.json      
# Thu, 22 Jan 2026 14:19:50 GMT
COPY file:e86693423cdd34ed7ac6eb4c5f916f086a37eeca572019e4cfd639c87f98a6ae in /root/buildinfo/labels.json      
# Thu, 22 Jan 2026 14:19:51 GMT
LABEL "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="0912ab420a80f21132d8a5e29d19a23339176677" "org.opencontainers.image.revision"="0912ab420a80f21132d8a5e29d19a23339176677" "build-date"="2026-01-22T14:19:22Z" "org.opencontainers.image.created"="2026-01-22T14:19:22Z" "release"="1769090502"org.opencontainers.image.revision=0912ab420a80f21132d8a5e29d19a23339176677,org.opencontainers.image.created=2026-01-22T14:19:22Z
# Fri, 23 Jan 2026 00:59:56 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 23 Jan 2026 00:59:56 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 23 Jan 2026 00:59:56 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 23 Jan 2026 00:59:56 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en         gnupg2     ;     microdnf clean all # buildkit
# Fri, 23 Jan 2026 00:59:56 GMT
ENV JAVA_VERSION=jdk-11.0.29+7
# Fri, 23 Jan 2026 01:00:29 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='71e00cd0ab4371a4e9d67d1a2ca3e8ed2f126dff6a6ab152a6ecdec60100fbdd';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.29%2B7/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.29_7.tar.gz';          ;;        ppc64le)          ESUM='d6136c0baafd588ba4f9be9f81285052f03b5366868e98fcd38fa5fb43c9121d';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.29%2B7/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.29_7.tar.gz';          ;;        s390x)          ESUM='12a494209c04a4cacee1615708b6856a770391d2588251a9a36e767ca4a07ac4';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.29%2B7/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.29_7.tar.gz';          ;;        x86_64)          ESUM='3c8f2b53dd137cd86e54f40df96fd0fc56df72c749c06469e7eab216503bc7cf';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.29%2B7/OpenJDK11U-jdk_x64_linux_hotspot_11.0.29_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Fri, 23 Jan 2026 01:00:31 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Fri, 23 Jan 2026 01:00:31 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Fri, 23 Jan 2026 01:00:31 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Fri, 23 Jan 2026 01:00:31 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:0d4f698c23e56c30d1371a123d48250f3a8dd3de24cc53c15e862c4210c331c2`  
		Last Modified: Thu, 22 Jan 2026 16:13:48 GMT  
		Size: 34.5 MB (34531934 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b92c2bf188648a091c1b8c8c61f955acb465fa45078ec7172314d61bd5c4667`  
		Last Modified: Fri, 23 Jan 2026 01:00:15 GMT  
		Size: 37.4 MB (37368644 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2027b6e2329ac48c0eec054f5075fafa4926bd5db39c6b593d59a32d63a4764`  
		Last Modified: Fri, 23 Jan 2026 01:00:50 GMT  
		Size: 141.4 MB (141425255 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dcee7fda51a7edff0c2a970a8836c81befbfe0e43878830aadd1c438c7590d1a`  
		Last Modified: Fri, 23 Jan 2026 01:00:46 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4bc2a2785f4abe671af96f544cf187076e8c74cf884e99df5e7901b70786fbdf`  
		Last Modified: Fri, 23 Jan 2026 01:00:45 GMT  
		Size: 2.3 KB (2291 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:11-ubi10-minimal` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:06571577cf2ca2fb15975d410776714794332c9aaccc2a9c2d972ee241cbcd87
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3829285 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:da79edb9ba0c295e0bc78e89ecd39d83f810f315210312c61164953ee7d096e2`

```dockerfile
```

-	Layers:
	-	`sha256:8ea72ea909b1801bbe9becce2b77c7440acef80e88d82be647433be43d6624e3`  
		Last Modified: Fri, 23 Jan 2026 01:00:46 GMT  
		Size: 3.8 MB (3807969 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f2188dc728052aae8052ab433f344baf5bb53a9e1f78aff959437525c1be08ff`  
		Last Modified: Fri, 23 Jan 2026 01:00:46 GMT  
		Size: 21.3 KB (21316 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-temurin:11-ubi10-minimal` - linux; arm64 variant v8

```console
$ docker pull eclipse-temurin@sha256:087981f6f125c323d6c273629151bd7a9c57b6279bac4915a63646f05be37952
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **208.1 MB (208121942 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f3d56524d9023d4f02aa4a727569e59179fa85c7ee5ba442073717553f8529c`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["jshell"]`

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
ENV JAVA_VERSION=jdk-11.0.29+7
# Fri, 23 Jan 2026 00:58:55 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='71e00cd0ab4371a4e9d67d1a2ca3e8ed2f126dff6a6ab152a6ecdec60100fbdd';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.29%2B7/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.29_7.tar.gz';          ;;        ppc64le)          ESUM='d6136c0baafd588ba4f9be9f81285052f03b5366868e98fcd38fa5fb43c9121d';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.29%2B7/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.29_7.tar.gz';          ;;        s390x)          ESUM='12a494209c04a4cacee1615708b6856a770391d2588251a9a36e767ca4a07ac4';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.29%2B7/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.29_7.tar.gz';          ;;        x86_64)          ESUM='3c8f2b53dd137cd86e54f40df96fd0fc56df72c749c06469e7eab216503bc7cf';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.29%2B7/OpenJDK11U-jdk_x64_linux_hotspot_11.0.29_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Fri, 23 Jan 2026 00:58:57 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Fri, 23 Jan 2026 00:58:57 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Fri, 23 Jan 2026 00:58:57 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Fri, 23 Jan 2026 00:58:57 GMT
CMD ["jshell"]
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
	-	`sha256:175e64ce7adc05ce294f2fc697e7f21480d5cdb777c779bd26d7246d99fd4b0e`  
		Last Modified: Fri, 23 Jan 2026 00:59:20 GMT  
		Size: 138.2 MB (138190258 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a9021efa9f87979e160610077ce8ca2b88bee5b5a56558d78d20d5ffc4ad9d2`  
		Last Modified: Fri, 23 Jan 2026 00:59:14 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db5589746cf599c0edfbbebbe08baf90672283c3f58afbb6170afc8bb816db84`  
		Last Modified: Fri, 23 Jan 2026 00:59:14 GMT  
		Size: 2.3 KB (2292 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:11-ubi10-minimal` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:007b0b2487b86e1239d06e92c1ff9376dbc6cefdfb7c3a88133ee13f4349bbe5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3829445 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f89d1925a86fd72b6255c56df707d86e6da25799eab310261590a721b940610`

```dockerfile
```

-	Layers:
	-	`sha256:5fbd8da25a664b8fe7d2691a3e5732d3aff0c31a392e692f6b9cc38560e96bec`  
		Last Modified: Fri, 23 Jan 2026 00:59:14 GMT  
		Size: 3.8 MB (3808013 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:061b3b96f1aaf16bb30a45e15c52ac132d80ad16dbcd62c3449addff2bf85dff`  
		Last Modified: Fri, 23 Jan 2026 00:59:14 GMT  
		Size: 21.4 KB (21432 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-temurin:11-ubi10-minimal` - linux; ppc64le

```console
$ docker pull eclipse-temurin@sha256:d2789639b0268fe3daebb33bd643cbc881309d66cad68f37e7a40be611d1165e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **206.4 MB (206429819 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:09d4dc42377b2a2f2c9807e45611238a724a6e14876baa5046ebdb65bec9098e`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 22 Jan 2026 14:54:45 GMT
LABEL maintainer="Red Hat, Inc."
# Thu, 22 Jan 2026 14:54:45 GMT
LABEL vendor="Red Hat, Inc."
# Thu, 22 Jan 2026 14:54:45 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Thu, 22 Jan 2026 14:54:45 GMT
LABEL com.redhat.component="ubi10-minimal-container"       name="ubi10/ubi-minimal"       version="10.1"       cpe="cpe:/o:redhat:enterprise_linux:10.1"       distribution-scope="public"
# Thu, 22 Jan 2026 14:54:45 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Thu, 22 Jan 2026 14:54:45 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 10."
# Thu, 22 Jan 2026 14:54:45 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 22 Jan 2026 14:54:45 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 22 Jan 2026 14:54:45 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 10 Minimal"
# Thu, 22 Jan 2026 14:54:45 GMT
LABEL io.openshift.expose-services=""
# Thu, 22 Jan 2026 14:54:45 GMT
LABEL io.openshift.tags="minimal rhel10"
# Thu, 22 Jan 2026 14:54:45 GMT
ENV container oci
# Thu, 22 Jan 2026 14:54:45 GMT
COPY dir:7bdbe74d43c251ef87ffde9a283489e444dd9e506bb8c01cd1c97a9f3ac52ddd in /      
# Thu, 22 Jan 2026 14:54:45 GMT
COPY file:5de33b5fc08b00635bccf9134a18978dba13e2250aa51838f9969515a3957847 in /etc/yum.repos.d/.      
# Thu, 22 Jan 2026 14:54:45 GMT
CMD ["/bin/bash"]
# Thu, 22 Jan 2026 14:54:46 GMT
COPY file:595171150af68abc798ea385f7988d74b566aa8e84babff137f00b08b2164683 in /usr/share/buildinfo/content-sets.json      
# Thu, 22 Jan 2026 14:54:46 GMT
COPY file:595171150af68abc798ea385f7988d74b566aa8e84babff137f00b08b2164683 in /root/buildinfo/content_manifests/content-sets.json      
# Thu, 22 Jan 2026 14:54:46 GMT
COPY file:fa7fed90e5fa59b018eb8aa0c4c26e4f0c5e15ab4b12ea84973f9ece212d9ed6 in /usr/share/buildinfo/labels.json      
# Thu, 22 Jan 2026 14:54:46 GMT
COPY file:fa7fed90e5fa59b018eb8aa0c4c26e4f0c5e15ab4b12ea84973f9ece212d9ed6 in /root/buildinfo/labels.json      
# Thu, 22 Jan 2026 14:54:46 GMT
LABEL "architecture"="ppc64le" "vcs-type"="git" "vcs-ref"="0912ab420a80f21132d8a5e29d19a23339176677" "org.opencontainers.image.revision"="0912ab420a80f21132d8a5e29d19a23339176677" "build-date"="2026-01-22T14:54:33Z" "org.opencontainers.image.created"="2026-01-22T14:54:33Z" "release"="1769090502"org.opencontainers.image.revision=0912ab420a80f21132d8a5e29d19a23339176677,org.opencontainers.image.created=2026-01-22T14:54:33Z
# Fri, 23 Jan 2026 00:57:54 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 23 Jan 2026 00:57:54 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 23 Jan 2026 00:57:54 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 23 Jan 2026 00:57:54 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en         gnupg2     ;     microdnf clean all # buildkit
# Fri, 23 Jan 2026 00:57:54 GMT
ENV JAVA_VERSION=jdk-11.0.29+7
# Fri, 23 Jan 2026 00:59:13 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='71e00cd0ab4371a4e9d67d1a2ca3e8ed2f126dff6a6ab152a6ecdec60100fbdd';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.29%2B7/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.29_7.tar.gz';          ;;        ppc64le)          ESUM='d6136c0baafd588ba4f9be9f81285052f03b5366868e98fcd38fa5fb43c9121d';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.29%2B7/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.29_7.tar.gz';          ;;        s390x)          ESUM='12a494209c04a4cacee1615708b6856a770391d2588251a9a36e767ca4a07ac4';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.29%2B7/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.29_7.tar.gz';          ;;        x86_64)          ESUM='3c8f2b53dd137cd86e54f40df96fd0fc56df72c749c06469e7eab216503bc7cf';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.29%2B7/OpenJDK11U-jdk_x64_linux_hotspot_11.0.29_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Fri, 23 Jan 2026 00:59:16 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Fri, 23 Jan 2026 00:59:17 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Fri, 23 Jan 2026 00:59:17 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Fri, 23 Jan 2026 00:59:17 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:ca7d82d686e4448886b5d40d7ede2a94863423d05f007fae2fdf719fb557a51e`  
		Last Modified: Thu, 22 Jan 2026 18:12:54 GMT  
		Size: 38.7 MB (38718444 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b83cbc42d47e675c60991c0dfbc843db7691ef4e8247a33f719b14ab372f6ea2`  
		Last Modified: Fri, 23 Jan 2026 00:58:44 GMT  
		Size: 39.1 MB (39124637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6490e7132525e369691bcc75763a256f05dc949c217a2b525a8f1715faa5c924`  
		Last Modified: Fri, 23 Jan 2026 00:59:56 GMT  
		Size: 128.6 MB (128584317 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a67f826d7aa181d7e49d23aaa2e1be9a8ff01237265bc69356e8dc2e628ab0c`  
		Last Modified: Fri, 23 Jan 2026 00:59:52 GMT  
		Size: 130.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:161e34106cc1d2cc0548fab65e179aa4c1ed79b99764dd91acdabbdce18e3fe9`  
		Last Modified: Fri, 23 Jan 2026 00:59:52 GMT  
		Size: 2.3 KB (2291 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:11-ubi10-minimal` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:afc20628ddf88230d9029f636a29ee597f2621af263236600e6df8e37f1c30c2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3815537 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db561e5551a2cde683d8f8334800746ec75601440873eeb99d05a66c3aba36c2`

```dockerfile
```

-	Layers:
	-	`sha256:73f993e9b00a8b2ca7b7ca1752141ffd9dbd2cd55afc327e09b758847ecad1d3`  
		Last Modified: Fri, 23 Jan 2026 00:59:53 GMT  
		Size: 3.8 MB (3794186 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:89e523e9af0ee5affd6f515d3521aae62b50d3dbbfdc76c8b8e52e1f19282485`  
		Last Modified: Fri, 23 Jan 2026 00:59:52 GMT  
		Size: 21.4 KB (21351 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-temurin:11-ubi10-minimal` - linux; s390x

```console
$ docker pull eclipse-temurin@sha256:9638976a7b2fc47c3138ce4c82c44e2bda714a08ac6c20d3599dc5ba9faeb422
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **194.2 MB (194218672 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:521eb1920b0100ba332593ee13b7d852cb12a0bbb04a384a5678d2c64c8131ac`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 22 Jan 2026 14:57:07 GMT
LABEL maintainer="Red Hat, Inc."
# Thu, 22 Jan 2026 14:57:07 GMT
LABEL vendor="Red Hat, Inc."
# Thu, 22 Jan 2026 14:57:07 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Thu, 22 Jan 2026 14:57:07 GMT
LABEL com.redhat.component="ubi10-minimal-container"       name="ubi10/ubi-minimal"       version="10.1"       cpe="cpe:/o:redhat:enterprise_linux:10.1"       distribution-scope="public"
# Thu, 22 Jan 2026 14:57:07 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Thu, 22 Jan 2026 14:57:07 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 10."
# Thu, 22 Jan 2026 14:57:07 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 22 Jan 2026 14:57:07 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 22 Jan 2026 14:57:07 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 10 Minimal"
# Thu, 22 Jan 2026 14:57:08 GMT
LABEL io.openshift.expose-services=""
# Thu, 22 Jan 2026 14:57:08 GMT
LABEL io.openshift.tags="minimal rhel10"
# Thu, 22 Jan 2026 14:57:08 GMT
ENV container oci
# Thu, 22 Jan 2026 14:57:08 GMT
COPY dir:b163faed476797909497b9e9cbceacce9d202c7df0108da15dd805a940495105 in /      
# Thu, 22 Jan 2026 14:57:08 GMT
COPY file:5de33b5fc08b00635bccf9134a18978dba13e2250aa51838f9969515a3957847 in /etc/yum.repos.d/.      
# Thu, 22 Jan 2026 14:57:08 GMT
CMD ["/bin/bash"]
# Thu, 22 Jan 2026 14:57:08 GMT
COPY file:595171150af68abc798ea385f7988d74b566aa8e84babff137f00b08b2164683 in /usr/share/buildinfo/content-sets.json      
# Thu, 22 Jan 2026 14:57:08 GMT
COPY file:595171150af68abc798ea385f7988d74b566aa8e84babff137f00b08b2164683 in /root/buildinfo/content_manifests/content-sets.json      
# Thu, 22 Jan 2026 14:57:08 GMT
COPY file:d6bdaa4e7d25601d04555b39b781ff4f9dacbc577ea220997429cff55f920063 in /usr/share/buildinfo/labels.json      
# Thu, 22 Jan 2026 14:57:08 GMT
COPY file:d6bdaa4e7d25601d04555b39b781ff4f9dacbc577ea220997429cff55f920063 in /root/buildinfo/labels.json      
# Thu, 22 Jan 2026 14:57:09 GMT
LABEL "architecture"="s390x" "vcs-type"="git" "vcs-ref"="0912ab420a80f21132d8a5e29d19a23339176677" "org.opencontainers.image.revision"="0912ab420a80f21132d8a5e29d19a23339176677" "build-date"="2026-01-22T14:54:50Z" "org.opencontainers.image.created"="2026-01-22T14:54:50Z" "release"="1769090502"org.opencontainers.image.revision=0912ab420a80f21132d8a5e29d19a23339176677,org.opencontainers.image.created=2026-01-22T14:54:50Z
# Fri, 23 Jan 2026 00:57:41 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 23 Jan 2026 00:57:41 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 23 Jan 2026 00:57:41 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 23 Jan 2026 00:57:41 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en         gnupg2     ;     microdnf clean all # buildkit
# Fri, 23 Jan 2026 00:57:41 GMT
ENV JAVA_VERSION=jdk-11.0.29+7
# Fri, 23 Jan 2026 00:57:46 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='71e00cd0ab4371a4e9d67d1a2ca3e8ed2f126dff6a6ab152a6ecdec60100fbdd';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.29%2B7/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.29_7.tar.gz';          ;;        ppc64le)          ESUM='d6136c0baafd588ba4f9be9f81285052f03b5366868e98fcd38fa5fb43c9121d';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.29%2B7/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.29_7.tar.gz';          ;;        s390x)          ESUM='12a494209c04a4cacee1615708b6856a770391d2588251a9a36e767ca4a07ac4';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.29%2B7/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.29_7.tar.gz';          ;;        x86_64)          ESUM='3c8f2b53dd137cd86e54f40df96fd0fc56df72c749c06469e7eab216503bc7cf';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.29%2B7/OpenJDK11U-jdk_x64_linux_hotspot_11.0.29_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Fri, 23 Jan 2026 00:57:47 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Fri, 23 Jan 2026 00:57:47 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Fri, 23 Jan 2026 00:57:47 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Fri, 23 Jan 2026 00:57:47 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:4305950dff5b7a63645441b4e7ab741317691b48df386123d1f9cf51b053ff55`  
		Last Modified: Thu, 22 Jan 2026 18:12:46 GMT  
		Size: 34.4 MB (34360531 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60a32a7eba25e3f29f4e39e71b6844c79632eddfad3907c76a741789b46122d0`  
		Last Modified: Fri, 23 Jan 2026 00:58:04 GMT  
		Size: 37.8 MB (37751890 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21f61da2e1554bf08ed1aa3ff78c8ad71979c13fefad93b6c8af9128aefbe301`  
		Last Modified: Fri, 23 Jan 2026 00:58:10 GMT  
		Size: 122.1 MB (122103832 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11ad9b47429c2105e88f2293a7f526696b00ed5b4cd7bcd259d6223437d7da3e`  
		Last Modified: Fri, 23 Jan 2026 00:58:08 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec2ca8c39e8f22a38c640dab1b696e96625761fa2d1414f892043c40dc33a6c4`  
		Last Modified: Fri, 23 Jan 2026 00:58:08 GMT  
		Size: 2.3 KB (2290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:11-ubi10-minimal` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:90a83ca03d0af7623d36c9d13d90d894a5a512b8c9682ce3036b61b9ad696e7f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3814879 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:97c17520395c8e554d86d0f0a2c5a3c8ef6f1090c9002d6f8015d641559f07ac`

```dockerfile
```

-	Layers:
	-	`sha256:6e90b5d11d29de6d2b8b547c881037d0216945944005964a15686d43f67e11f2`  
		Last Modified: Fri, 23 Jan 2026 00:58:08 GMT  
		Size: 3.8 MB (3793563 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:df8bbb92b4545ccf36ba71a7203b92de625da675743adc0495a47fb81cd6fc21`  
		Last Modified: Fri, 23 Jan 2026 00:58:08 GMT  
		Size: 21.3 KB (21316 bytes)  
		MIME: application/vnd.in-toto+json
