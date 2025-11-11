## `eclipse-temurin:17-jre-ubi10-minimal`

```console
$ docker pull eclipse-temurin@sha256:6c11a58ad791bae25ecbec1afe42bb71733fd199f66e8c56a055fe123c39e1a1
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

### `eclipse-temurin:17-jre-ubi10-minimal` - linux; amd64

```console
$ docker pull eclipse-temurin@sha256:832907c43d8ecd93c89d2e3be7cdccae8d449c4468eab431ebe28e363a52fd27
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **141.4 MB (141358204 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:091ae9a4d3098bc195af71e05ecbbad7518b4b5912a9165677faaf4cbd1d53d3`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`

```dockerfile
# Mon, 10 Nov 2025 09:00:40 GMT
LABEL maintainer="Red Hat, Inc."
# Mon, 10 Nov 2025 09:00:40 GMT
LABEL vendor="Red Hat, Inc."
# Mon, 10 Nov 2025 09:00:40 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Mon, 10 Nov 2025 09:00:40 GMT
LABEL com.redhat.component="ubi10-minimal-container"       name="ubi10/ubi-minimal"       version="10.0"       cpe="cpe:/o:redhat:enterprise_linux:10.0"       distribution-scope="public"
# Mon, 10 Nov 2025 09:00:40 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Mon, 10 Nov 2025 09:00:40 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 10."
# Mon, 10 Nov 2025 09:00:40 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 10 Nov 2025 09:00:40 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 10 Nov 2025 09:00:41 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 10 Minimal"
# Mon, 10 Nov 2025 09:00:41 GMT
LABEL io.openshift.expose-services=""
# Mon, 10 Nov 2025 09:00:41 GMT
LABEL io.openshift.tags="minimal rhel10"
# Mon, 10 Nov 2025 09:00:41 GMT
ENV container oci
# Mon, 10 Nov 2025 09:00:41 GMT
COPY dir:1151487a8fe49bf6a88ef514a8355cedfdeab84f41175ca19d399c25d56e0756 in /      
# Mon, 10 Nov 2025 09:00:41 GMT
COPY file:5de33b5fc08b00635bccf9134a18978dba13e2250aa51838f9969515a3957847 in /etc/yum.repos.d/.      
# Mon, 10 Nov 2025 09:00:41 GMT
CMD ["/bin/bash"]
# Mon, 10 Nov 2025 09:00:41 GMT
COPY file:595171150af68abc798ea385f7988d74b566aa8e84babff137f00b08b2164683 in /usr/share/buildinfo/content-sets.json      
# Mon, 10 Nov 2025 09:00:41 GMT
COPY file:595171150af68abc798ea385f7988d74b566aa8e84babff137f00b08b2164683 in /root/buildinfo/content_manifests/content-sets.json      
# Mon, 10 Nov 2025 09:00:41 GMT
COPY file:78d340a91825c21b9da1409e53e49b8dfe282306bad9ddfd7c9094f83382378e in /usr/share/buildinfo/labels.json      
# Mon, 10 Nov 2025 09:00:41 GMT
COPY file:78d340a91825c21b9da1409e53e49b8dfe282306bad9ddfd7c9094f83382378e in /root/buildinfo/labels.json      
# Mon, 10 Nov 2025 09:00:42 GMT
LABEL "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="18068ad623ccc46f729e7cefa6bb8063513ecab3" "org.opencontainers.image.revision"="18068ad623ccc46f729e7cefa6bb8063513ecab3" "build-date"="2025-11-10T09:00:19Z" "release"="1762765041"org.opencontainers.image.revision=18068ad623ccc46f729e7cefa6bb8063513ecab3
# Mon, 10 Nov 2025 20:10:54 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 10 Nov 2025 20:10:54 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 10 Nov 2025 20:10:54 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 10 Nov 2025 20:10:54 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en         gnupg2     ;     microdnf clean all # buildkit
# Mon, 10 Nov 2025 20:10:54 GMT
ENV JAVA_VERSION=jdk-17.0.17+10
# Mon, 10 Nov 2025 20:10:57 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='d184e8d5caabe51b7ce9d4e0410f51b447a703eab3cec60ca94b7c59fecdad01';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.17_10.tar.gz';          ;;        ppc64le)          ESUM='bc39038e7a874da232f80f49f90f7ec08213fc66b956405f6cc45eed3658cd0a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.17_10.tar.gz';          ;;        s390x)          ESUM='489f8187a939a1e065c2e8f13ff7f26514dd7391b4784ae36e21d9f96972e3f2';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_s390x_linux_hotspot_17.0.17_10.tar.gz';          ;;        x86_64)          ESUM='1c607fb19f153b23a7d62ff980eb55cff1a7d47ce565bbc44d14947c93bd33c9';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_x64_linux_hotspot_17.0.17_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz; # buildkit
# Mon, 10 Nov 2025 20:10:57 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Mon, 10 Nov 2025 20:10:57 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Mon, 10 Nov 2025 20:10:57 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
```

-	Layers:
	-	`sha256:32b34b6043df53356073fca74558aa4fb64fa2c3d92bc988ada13ba9600db416`  
		Last Modified: Mon, 10 Nov 2025 12:11:59 GMT  
		Size: 33.4 MB (33442309 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2f9aa33eb8e9645f5e2d3954ca218c02dbd40547977d5ff4e328806c73d122d`  
		Last Modified: Mon, 10 Nov 2025 20:11:27 GMT  
		Size: 60.9 MB (60859041 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e8b09972457dfe9040f31eb9502ab6ddb2c2401644bbf87086e1bfe04c46588`  
		Last Modified: Mon, 10 Nov 2025 20:11:27 GMT  
		Size: 47.1 MB (47054435 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:462fad5e1141f1b2db7b5ef32d3102246561364993960c9c85dd433d06f64fde`  
		Last Modified: Mon, 10 Nov 2025 20:11:22 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee91896e3d48415172429a7b4a1552bdfebe375ee3cd8d60e18f6a8068a80629`  
		Last Modified: Mon, 10 Nov 2025 20:11:22 GMT  
		Size: 2.3 KB (2291 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:17-jre-ubi10-minimal` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:dcb7bf2ad714ced7b3fd7d4bd9606930fce7bf76886d2bbb898a233ecdb2ae2f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5610437 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1aafbf29b0e741966d81b1f3d159f74b9029585dfd0f3d081875e38ca349cfcc`

```dockerfile
```

-	Layers:
	-	`sha256:0b66eb13cb22e43261ce40d777a41d91343fec2b52a0ae4f17d8f8bf26991aae`  
		Last Modified: Mon, 10 Nov 2025 22:13:52 GMT  
		Size: 5.6 MB (5590059 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:30975c9963dab64e6143284e02faf8ee66cdb65c87ab53ea82e4ad23b52ef4bb`  
		Last Modified: Mon, 10 Nov 2025 22:13:53 GMT  
		Size: 20.4 KB (20378 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-temurin:17-jre-ubi10-minimal` - linux; arm64 variant v8

```console
$ docker pull eclipse-temurin@sha256:ae1c912bbba878ced6bbb1429de2c732f530852a0dcb81f821c10bcbbc1c8e61
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **138.0 MB (137998531 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e923496a7aeb3feee2ae901df13d0aab8bcfedf48a34e6bc96a09d703a7af975`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`

```dockerfile
# Mon, 10 Nov 2025 09:03:37 GMT
LABEL maintainer="Red Hat, Inc."
# Mon, 10 Nov 2025 09:03:37 GMT
LABEL vendor="Red Hat, Inc."
# Mon, 10 Nov 2025 09:03:37 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Mon, 10 Nov 2025 09:03:37 GMT
LABEL com.redhat.component="ubi10-minimal-container"       name="ubi10/ubi-minimal"       version="10.0"       cpe="cpe:/o:redhat:enterprise_linux:10.0"       distribution-scope="public"
# Mon, 10 Nov 2025 09:03:37 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Mon, 10 Nov 2025 09:03:37 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 10."
# Mon, 10 Nov 2025 09:03:37 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 10 Nov 2025 09:03:37 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 10 Nov 2025 09:03:37 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 10 Minimal"
# Mon, 10 Nov 2025 09:03:37 GMT
LABEL io.openshift.expose-services=""
# Mon, 10 Nov 2025 09:03:37 GMT
LABEL io.openshift.tags="minimal rhel10"
# Mon, 10 Nov 2025 09:03:37 GMT
ENV container oci
# Mon, 10 Nov 2025 09:03:38 GMT
COPY dir:5f27c3cb719e482fe521704b0fcfe8823184f7bac7981ef4facb5aa58eacca9f in /      
# Mon, 10 Nov 2025 09:03:38 GMT
COPY file:5de33b5fc08b00635bccf9134a18978dba13e2250aa51838f9969515a3957847 in /etc/yum.repos.d/.      
# Mon, 10 Nov 2025 09:03:38 GMT
CMD ["/bin/bash"]
# Mon, 10 Nov 2025 09:03:38 GMT
COPY file:595171150af68abc798ea385f7988d74b566aa8e84babff137f00b08b2164683 in /usr/share/buildinfo/content-sets.json      
# Mon, 10 Nov 2025 09:03:38 GMT
COPY file:595171150af68abc798ea385f7988d74b566aa8e84babff137f00b08b2164683 in /root/buildinfo/content_manifests/content-sets.json      
# Mon, 10 Nov 2025 09:03:38 GMT
COPY file:b708d1caa910d276ff58faaae8986ef542efb0b7b3e35c86e7086c7765f4ff1a in /usr/share/buildinfo/labels.json      
# Mon, 10 Nov 2025 09:03:38 GMT
COPY file:b708d1caa910d276ff58faaae8986ef542efb0b7b3e35c86e7086c7765f4ff1a in /root/buildinfo/labels.json      
# Mon, 10 Nov 2025 09:03:39 GMT
LABEL "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="18068ad623ccc46f729e7cefa6bb8063513ecab3" "org.opencontainers.image.revision"="18068ad623ccc46f729e7cefa6bb8063513ecab3" "build-date"="2025-11-10T09:03:16Z" "release"="1762765041"org.opencontainers.image.revision=18068ad623ccc46f729e7cefa6bb8063513ecab3
# Mon, 10 Nov 2025 20:14:15 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 10 Nov 2025 20:14:15 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 10 Nov 2025 20:14:15 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 10 Nov 2025 20:14:15 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en         gnupg2     ;     microdnf clean all # buildkit
# Mon, 10 Nov 2025 20:14:15 GMT
ENV JAVA_VERSION=jdk-17.0.17+10
# Mon, 10 Nov 2025 20:14:51 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='d184e8d5caabe51b7ce9d4e0410f51b447a703eab3cec60ca94b7c59fecdad01';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.17_10.tar.gz';          ;;        ppc64le)          ESUM='bc39038e7a874da232f80f49f90f7ec08213fc66b956405f6cc45eed3658cd0a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.17_10.tar.gz';          ;;        s390x)          ESUM='489f8187a939a1e065c2e8f13ff7f26514dd7391b4784ae36e21d9f96972e3f2';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_s390x_linux_hotspot_17.0.17_10.tar.gz';          ;;        x86_64)          ESUM='1c607fb19f153b23a7d62ff980eb55cff1a7d47ce565bbc44d14947c93bd33c9';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_x64_linux_hotspot_17.0.17_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz; # buildkit
# Mon, 10 Nov 2025 20:14:51 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Mon, 10 Nov 2025 20:14:51 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Mon, 10 Nov 2025 20:14:51 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
```

-	Layers:
	-	`sha256:bcfce2f653765e7fbc0157676a8995e7c79e4d29c562744818763bd665844191`  
		Last Modified: Mon, 10 Nov 2025 12:11:55 GMT  
		Size: 31.6 MB (31555554 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7137d12faf649745198d2dd94cffa0a18516d5f53ceb1050b83d5f6d1b8b3410`  
		Last Modified: Mon, 10 Nov 2025 20:14:51 GMT  
		Size: 59.9 MB (59906018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64cdd7bf516216a6e6bb5a945de21d6d14aaf27ca026060734c8c71b1b9873d8`  
		Last Modified: Mon, 10 Nov 2025 20:15:16 GMT  
		Size: 46.5 MB (46534541 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f19886efa5e6713dd0ddd1e8d68c5f4b3b76d057a2f204c359268a3796c74dd`  
		Last Modified: Mon, 10 Nov 2025 20:15:11 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2a2b5a5ce5e1dc4911e55332e82004ddc27ae4a1b0846f00604674512f5013e`  
		Last Modified: Mon, 10 Nov 2025 20:15:11 GMT  
		Size: 2.3 KB (2290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:17-jre-ubi10-minimal` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:5250251a13b2b134bdd506c26da7aa85ceeca6bee72a1a265696bd5f68b9ae26
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5610019 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa74c248b0c4bbe10be296831abfe25ead816db61f37a861652b593b5594cc11`

```dockerfile
```

-	Layers:
	-	`sha256:6a6b9e24c9c6b1665bad4940ba113a5259ba90b9f56b3fc52f396df261ed5f32`  
		Last Modified: Mon, 10 Nov 2025 22:13:58 GMT  
		Size: 5.6 MB (5589537 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ac466000757c565058e364796a36fc27e040938b5871b8dc42c0c374f49e799c`  
		Last Modified: Mon, 10 Nov 2025 22:13:59 GMT  
		Size: 20.5 KB (20482 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-temurin:17-jre-ubi10-minimal` - linux; ppc64le

```console
$ docker pull eclipse-temurin@sha256:12fcbd0fa2b0fd3f819e0515545836c5df3cd22e73b7a35d29ba2cecfa2f5154
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **148.0 MB (147991338 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:48f10273d29648dee90866daf75ebfc3908d1510161a2eb7ae83ac7aedda7cde`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`

```dockerfile
# Mon, 10 Nov 2025 09:07:33 GMT
LABEL maintainer="Red Hat, Inc."
# Mon, 10 Nov 2025 09:07:33 GMT
LABEL vendor="Red Hat, Inc."
# Mon, 10 Nov 2025 09:07:33 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Mon, 10 Nov 2025 09:07:33 GMT
LABEL com.redhat.component="ubi10-minimal-container"       name="ubi10/ubi-minimal"       version="10.0"       cpe="cpe:/o:redhat:enterprise_linux:10.0"       distribution-scope="public"
# Mon, 10 Nov 2025 09:07:33 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Mon, 10 Nov 2025 09:07:33 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 10."
# Mon, 10 Nov 2025 09:07:33 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 10 Nov 2025 09:07:33 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 10 Nov 2025 09:07:33 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 10 Minimal"
# Mon, 10 Nov 2025 09:07:33 GMT
LABEL io.openshift.expose-services=""
# Mon, 10 Nov 2025 09:07:33 GMT
LABEL io.openshift.tags="minimal rhel10"
# Mon, 10 Nov 2025 09:07:33 GMT
ENV container oci
# Mon, 10 Nov 2025 09:07:33 GMT
COPY dir:3b3b10e38b1604be9ad4399ace6288103b3f832d58ec15ea17ba00ea93e2b9f7 in /      
# Mon, 10 Nov 2025 09:07:33 GMT
COPY file:5de33b5fc08b00635bccf9134a18978dba13e2250aa51838f9969515a3957847 in /etc/yum.repos.d/.      
# Mon, 10 Nov 2025 09:07:33 GMT
CMD ["/bin/bash"]
# Mon, 10 Nov 2025 09:07:33 GMT
COPY file:595171150af68abc798ea385f7988d74b566aa8e84babff137f00b08b2164683 in /usr/share/buildinfo/content-sets.json      
# Mon, 10 Nov 2025 09:07:34 GMT
COPY file:595171150af68abc798ea385f7988d74b566aa8e84babff137f00b08b2164683 in /root/buildinfo/content_manifests/content-sets.json      
# Mon, 10 Nov 2025 09:07:34 GMT
COPY file:c064500eaa9793e932d2f4ef045195d7141f0508959d80bc76c0e4b59b13a481 in /usr/share/buildinfo/labels.json      
# Mon, 10 Nov 2025 09:07:34 GMT
COPY file:c064500eaa9793e932d2f4ef045195d7141f0508959d80bc76c0e4b59b13a481 in /root/buildinfo/labels.json      
# Mon, 10 Nov 2025 09:07:34 GMT
LABEL "architecture"="ppc64le" "vcs-type"="git" "vcs-ref"="18068ad623ccc46f729e7cefa6bb8063513ecab3" "org.opencontainers.image.revision"="18068ad623ccc46f729e7cefa6bb8063513ecab3" "build-date"="2025-11-10T09:07:22Z" "release"="1762765041"org.opencontainers.image.revision=18068ad623ccc46f729e7cefa6bb8063513ecab3
# Mon, 10 Nov 2025 22:20:01 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 10 Nov 2025 22:20:01 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 10 Nov 2025 22:20:01 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 10 Nov 2025 22:20:01 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en         gnupg2     ;     microdnf clean all # buildkit
# Mon, 10 Nov 2025 22:20:01 GMT
ENV JAVA_VERSION=jdk-17.0.17+10
# Mon, 10 Nov 2025 22:25:03 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='d184e8d5caabe51b7ce9d4e0410f51b447a703eab3cec60ca94b7c59fecdad01';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.17_10.tar.gz';          ;;        ppc64le)          ESUM='bc39038e7a874da232f80f49f90f7ec08213fc66b956405f6cc45eed3658cd0a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.17_10.tar.gz';          ;;        s390x)          ESUM='489f8187a939a1e065c2e8f13ff7f26514dd7391b4784ae36e21d9f96972e3f2';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_s390x_linux_hotspot_17.0.17_10.tar.gz';          ;;        x86_64)          ESUM='1c607fb19f153b23a7d62ff980eb55cff1a7d47ce565bbc44d14947c93bd33c9';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_x64_linux_hotspot_17.0.17_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz; # buildkit
# Mon, 10 Nov 2025 22:25:04 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Mon, 10 Nov 2025 22:25:05 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Mon, 10 Nov 2025 22:25:05 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
```

-	Layers:
	-	`sha256:4228be713e86c1bedeefae4a08794664efeed4203b55a759503d7eaba4964702`  
		Last Modified: Mon, 10 Nov 2025 12:12:00 GMT  
		Size: 36.8 MB (36758319 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:176c50dcfec7b2b334fc4e91aecba50a60520f8dc961a0ec542db5fcf328613c`  
		Last Modified: Mon, 10 Nov 2025 22:21:05 GMT  
		Size: 64.3 MB (64337609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:288bffd623bd037983c884f3426d70531c22600d05048d986f12a5c465faa4c2`  
		Last Modified: Mon, 10 Nov 2025 22:25:45 GMT  
		Size: 46.9 MB (46892994 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0064a057124d5aaaf95984fbb1f29861c8f4571c3b5076f10b3dfd97f0a24c2a`  
		Last Modified: Mon, 10 Nov 2025 22:25:43 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f46fdbff7a1d36172406d5140e59be13b1806020ca0be600e6d40412cca5652a`  
		Last Modified: Mon, 10 Nov 2025 22:25:43 GMT  
		Size: 2.3 KB (2290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:17-jre-ubi10-minimal` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:dcc8b35f2a751332adebbaa0a654b379f7e10a843a98f9a5b8f9621ab4eeb903
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5599532 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8de75abfe76cfe023c36e2cc5fe0aa0a4a697bf31d1dc13db897299bca833de0`

```dockerfile
```

-	Layers:
	-	`sha256:67d3304124653be93ced7d7f2f2bcc02b587dcebaa9ead54690b30f291631494`  
		Last Modified: Tue, 11 Nov 2025 01:13:37 GMT  
		Size: 5.6 MB (5579124 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c69ab7543deae7fcd421b89ee16ec928a35943c85f4e85f3102f239081683aff`  
		Last Modified: Tue, 11 Nov 2025 01:13:38 GMT  
		Size: 20.4 KB (20408 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-temurin:17-jre-ubi10-minimal` - linux; s390x

```console
$ docker pull eclipse-temurin@sha256:5aa9632ff4ce6c27bf9b6372120aa6e1206f10d47ec818cc10d77833b3be8f32
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **138.4 MB (138366681 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff7db3b4693240c5e2e84cfd7c18ce964c43a99277af4223ea3704c24c66a6bb`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`

```dockerfile
# Mon, 10 Nov 2025 09:29:45 GMT
LABEL maintainer="Red Hat, Inc."
# Mon, 10 Nov 2025 09:29:45 GMT
LABEL vendor="Red Hat, Inc."
# Mon, 10 Nov 2025 09:29:45 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Mon, 10 Nov 2025 09:29:45 GMT
LABEL com.redhat.component="ubi10-minimal-container"       name="ubi10/ubi-minimal"       version="10.0"       cpe="cpe:/o:redhat:enterprise_linux:10.0"       distribution-scope="public"
# Mon, 10 Nov 2025 09:29:45 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Mon, 10 Nov 2025 09:29:45 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 10."
# Mon, 10 Nov 2025 09:29:45 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 10 Nov 2025 09:29:45 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 10 Nov 2025 09:29:45 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 10 Minimal"
# Mon, 10 Nov 2025 09:29:45 GMT
LABEL io.openshift.expose-services=""
# Mon, 10 Nov 2025 09:29:45 GMT
LABEL io.openshift.tags="minimal rhel10"
# Mon, 10 Nov 2025 09:29:45 GMT
ENV container oci
# Mon, 10 Nov 2025 09:29:46 GMT
COPY dir:6c57839ff9e4376687d005b2dd39ccb2cab51f91439029283a68660066f453ce in /      
# Mon, 10 Nov 2025 09:29:46 GMT
COPY file:5de33b5fc08b00635bccf9134a18978dba13e2250aa51838f9969515a3957847 in /etc/yum.repos.d/.      
# Mon, 10 Nov 2025 09:29:46 GMT
CMD ["/bin/bash"]
# Mon, 10 Nov 2025 09:29:46 GMT
COPY file:595171150af68abc798ea385f7988d74b566aa8e84babff137f00b08b2164683 in /usr/share/buildinfo/content-sets.json      
# Mon, 10 Nov 2025 09:29:46 GMT
COPY file:595171150af68abc798ea385f7988d74b566aa8e84babff137f00b08b2164683 in /root/buildinfo/content_manifests/content-sets.json      
# Mon, 10 Nov 2025 09:29:46 GMT
COPY file:e7aca2e85df2b708be29fcf6492e0a97a7c66021e1c9892fbb96b00e6743eb74 in /usr/share/buildinfo/labels.json      
# Mon, 10 Nov 2025 09:29:47 GMT
COPY file:e7aca2e85df2b708be29fcf6492e0a97a7c66021e1c9892fbb96b00e6743eb74 in /root/buildinfo/labels.json      
# Mon, 10 Nov 2025 09:29:47 GMT
LABEL "architecture"="s390x" "vcs-type"="git" "vcs-ref"="18068ad623ccc46f729e7cefa6bb8063513ecab3" "org.opencontainers.image.revision"="18068ad623ccc46f729e7cefa6bb8063513ecab3" "build-date"="2025-11-10T09:27:31Z" "release"="1762765041"org.opencontainers.image.revision=18068ad623ccc46f729e7cefa6bb8063513ecab3
# Mon, 10 Nov 2025 21:51:19 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 10 Nov 2025 21:51:19 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 10 Nov 2025 21:51:19 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 10 Nov 2025 21:51:19 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en         gnupg2     ;     microdnf clean all # buildkit
# Mon, 10 Nov 2025 21:51:19 GMT
ENV JAVA_VERSION=jdk-17.0.17+10
# Mon, 10 Nov 2025 21:54:23 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='d184e8d5caabe51b7ce9d4e0410f51b447a703eab3cec60ca94b7c59fecdad01';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.17_10.tar.gz';          ;;        ppc64le)          ESUM='bc39038e7a874da232f80f49f90f7ec08213fc66b956405f6cc45eed3658cd0a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.17_10.tar.gz';          ;;        s390x)          ESUM='489f8187a939a1e065c2e8f13ff7f26514dd7391b4784ae36e21d9f96972e3f2';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_s390x_linux_hotspot_17.0.17_10.tar.gz';          ;;        x86_64)          ESUM='1c607fb19f153b23a7d62ff980eb55cff1a7d47ce565bbc44d14947c93bd33c9';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jre_x64_linux_hotspot_17.0.17_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz; # buildkit
# Mon, 10 Nov 2025 21:54:23 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Mon, 10 Nov 2025 21:54:24 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Mon, 10 Nov 2025 21:54:24 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
```

-	Layers:
	-	`sha256:7f1c5bcca4741d297e22f1dc3025949ada86e7918c015239fbbf81971759082f`  
		Last Modified: Mon, 10 Nov 2025 12:11:54 GMT  
		Size: 33.4 MB (33403080 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:753a4bd28d57ae0089cf8c05a2fbb3b40711d6fae82766de9b160ebe59e240fb`  
		Last Modified: Mon, 10 Nov 2025 21:52:19 GMT  
		Size: 60.9 MB (60935183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24e7e8181ac9816fa781b6ab57dc08eb5c57f992c567221a230745f31b4afd88`  
		Last Modified: Mon, 10 Nov 2025 21:54:58 GMT  
		Size: 44.0 MB (44026000 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c594aa98958c871d22fa16728e5c535535625a809e7f10176d487404e22587ad`  
		Last Modified: Mon, 10 Nov 2025 21:54:53 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef9368a1757982f90a6060f598d15839f39a3621de1cb8db4a96863234038253`  
		Last Modified: Mon, 10 Nov 2025 21:54:53 GMT  
		Size: 2.3 KB (2291 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:17-jre-ubi10-minimal` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:63dc34f08cddf390b1b57c397d657e21d7d155248d37b9ca4b27c688fc9e2d24
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5600363 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c3abf04630986465487897119c5896e8c88037d52102f32c06f976daef57601`

```dockerfile
```

-	Layers:
	-	`sha256:356561878c54b973f9bb61e6c3ed1a04c7eebdc55561ced945355dfd5c4ffd9b`  
		Last Modified: Mon, 10 Nov 2025 22:14:08 GMT  
		Size: 5.6 MB (5579985 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bc99ce0f4c0df75805c17299d5a0d7fd22992919561d5ac713e9b13d00bf2cc3`  
		Last Modified: Mon, 10 Nov 2025 22:14:09 GMT  
		Size: 20.4 KB (20378 bytes)  
		MIME: application/vnd.in-toto+json
