## `eclipse-temurin:8-jre-ubi9-minimal`

```console
$ docker pull eclipse-temurin@sha256:8e91b5c076000efb68270530ff692ae958d77ac21b341d1e1c1d438719feb9ad
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
$ docker pull eclipse-temurin@sha256:73c0495d21ae7bf97e9f76a60f74efe3f9da6480bfd11d1392b77b7cdf93a2db
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **110.7 MB (110679317 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:15945267898be30f562090747bde17259abe90feebef3eee8fc46966bc08750e`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`

```dockerfile
# Mon, 15 Jun 2026 04:14:14 GMT
LABEL maintainer="Red Hat, Inc."
# Mon, 15 Jun 2026 04:14:14 GMT
LABEL vendor="Red Hat, Inc."
# Mon, 15 Jun 2026 04:14:14 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Mon, 15 Jun 2026 04:14:14 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.8"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Mon, 15 Jun 2026 04:14:14 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Mon, 15 Jun 2026 04:14:14 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Mon, 15 Jun 2026 04:14:14 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 15 Jun 2026 04:14:14 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 15 Jun 2026 04:14:14 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Mon, 15 Jun 2026 04:14:14 GMT
LABEL io.openshift.expose-services=""
# Mon, 15 Jun 2026 04:14:14 GMT
LABEL io.openshift.tags="minimal rhel9"
# Mon, 15 Jun 2026 04:14:14 GMT
ENV container oci
# Mon, 15 Jun 2026 04:14:14 GMT
COPY dir:37b1ea11a739ebaa3fdc4f74d963b56e5e50e2e4b048d008948978527dfc6171 in /      
# Mon, 15 Jun 2026 04:14:14 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Mon, 15 Jun 2026 04:14:14 GMT
CMD ["/bin/bash"]
# Mon, 15 Jun 2026 04:14:15 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /usr/share/buildinfo/content-sets.json      
# Mon, 15 Jun 2026 04:14:15 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /root/buildinfo/content_manifests/content-sets.json      
# Mon, 15 Jun 2026 04:14:15 GMT
COPY file:df404a029d790f68220d23dfb53723434fcb08b3371b285cdfe02b423b1e978d in /usr/share/buildinfo/labels.json      
# Mon, 15 Jun 2026 04:14:15 GMT
COPY file:df404a029d790f68220d23dfb53723434fcb08b3371b285cdfe02b423b1e978d in /root/buildinfo/labels.json      
# Mon, 15 Jun 2026 04:14:15 GMT
LABEL "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="92938083b76077787596c980f5cdc39e89c50a24" "org.opencontainers.image.revision"="92938083b76077787596c980f5cdc39e89c50a24" "build-date"="2026-06-15T04:14:02Z" "org.opencontainers.image.created"="2026-06-15T04:14:02Z" "release"="1781496742"org.opencontainers.image.revision=92938083b76077787596c980f5cdc39e89c50a24,org.opencontainers.image.created=2026-06-15T04:14:02Z
# Mon, 15 Jun 2026 23:13:44 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 15 Jun 2026 23:13:44 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 15 Jun 2026 23:13:44 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 15 Jun 2026 23:13:44 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en     ;     microdnf clean all # buildkit
# Mon, 15 Jun 2026 23:13:44 GMT
ENV JAVA_VERSION=jdk8u492-b09
# Mon, 15 Jun 2026 23:13:46 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='d5e50cb002600007dbdfac523605d26196607fa5212db0942ef05cdce9fe2892';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u492-b09/OpenJDK8U-jre_aarch64_linux_hotspot_8u492b09.tar.gz';          ;;        ppc64le)          ESUM='4f724a0fce1117521a3a3e55ebb0281d56f6c9a066092bc3186ee40d8cd955a2';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u492-b09/OpenJDK8U-jre_ppc64le_linux_hotspot_8u492b09.tar.gz';          ;;        x86_64)          ESUM='8eef3d4a837bb7a9e45d30a7579d84d5b76a4321f4376573311e6bf89e48f9b0';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u492-b09/OpenJDK8U-jre_x64_linux_hotspot_8u492b09.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz; # buildkit
# Mon, 15 Jun 2026 23:13:47 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java -version"; java -version;     echo "Complete." # buildkit
# Mon, 15 Jun 2026 23:13:47 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Mon, 15 Jun 2026 23:13:47 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
```

-	Layers:
	-	`sha256:48538841ca5147d36a25e82713e079413d3c2a137f5ea5df68a1c5da1e3a677e`  
		Last Modified: Mon, 15 Jun 2026 04:45:40 GMT  
		Size: 40.7 MB (40680192 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fcbe8c1a4c339c191db2254b53e4f0df9c68adacdf82b796a48808d6f441c4b`  
		Last Modified: Mon, 15 Jun 2026 23:13:59 GMT  
		Size: 27.7 MB (27664333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac97b70fd18e72b4462f79039db4aead9f34dc71b139c0d30ff6fce879abd7b3`  
		Last Modified: Mon, 15 Jun 2026 23:13:59 GMT  
		Size: 42.3 MB (42332193 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c69132cf1832a4246226d55cf65a5a0893ffe151d8c448bd9adfb52d5825705`  
		Last Modified: Mon, 15 Jun 2026 23:13:57 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d236033e8b73117712c71bcbbc3de260747cbe568f0a27675f757c4e83d03a1e`  
		Last Modified: Mon, 15 Jun 2026 23:13:57 GMT  
		Size: 2.5 KB (2471 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:8-jre-ubi9-minimal` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:e628b672d0de02550f9a7f5fa42a6197adb021b16e3973008de6f90001d126db
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2458827 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4fe9f30f754743940a5833146af7bc453cb920a08a61e0085379684c6a67a781`

```dockerfile
```

-	Layers:
	-	`sha256:849e5a81e391f56309b299145feedf9912e827b8ba48afbae27d114c901a8a54`  
		Last Modified: Mon, 15 Jun 2026 23:13:58 GMT  
		Size: 2.4 MB (2439480 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9f2a7230df64275bee64e7bb050f4063ec154300683a8fd44df5f1b793c3541d`  
		Last Modified: Mon, 15 Jun 2026 23:13:57 GMT  
		Size: 19.3 KB (19347 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-temurin:8-jre-ubi9-minimal` - linux; arm64 variant v8

```console
$ docker pull eclipse-temurin@sha256:592e51c8ab939781cb2ba5efdc66e992afe3a1b701ca7f107ecbea5900d833cc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **108.3 MB (108276170 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c9444d9ce56b3884f8aade3a690f82a3afa84ec492b9c9c8cba97e092772c96f`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`

```dockerfile
# Mon, 15 Jun 2026 04:15:43 GMT
LABEL maintainer="Red Hat, Inc."
# Mon, 15 Jun 2026 04:15:43 GMT
LABEL vendor="Red Hat, Inc."
# Mon, 15 Jun 2026 04:15:43 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Mon, 15 Jun 2026 04:15:43 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.8"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Mon, 15 Jun 2026 04:15:43 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Mon, 15 Jun 2026 04:15:43 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Mon, 15 Jun 2026 04:15:43 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 15 Jun 2026 04:15:43 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 15 Jun 2026 04:15:43 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Mon, 15 Jun 2026 04:15:43 GMT
LABEL io.openshift.expose-services=""
# Mon, 15 Jun 2026 04:15:43 GMT
LABEL io.openshift.tags="minimal rhel9"
# Mon, 15 Jun 2026 04:15:43 GMT
ENV container oci
# Mon, 15 Jun 2026 04:15:44 GMT
COPY dir:553346a2ec24f0a482095311bcf74fe382a66c8cb976ea0b61f6d55ee917aca4 in /      
# Mon, 15 Jun 2026 04:15:44 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Mon, 15 Jun 2026 04:15:44 GMT
CMD ["/bin/bash"]
# Mon, 15 Jun 2026 04:15:45 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /usr/share/buildinfo/content-sets.json      
# Mon, 15 Jun 2026 04:15:45 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /root/buildinfo/content_manifests/content-sets.json      
# Mon, 15 Jun 2026 04:15:45 GMT
COPY file:f3a7d39ee1404b5d93b5454e6014ed02f219e8a196f3df41d84d2e0e61c935f5 in /usr/share/buildinfo/labels.json      
# Mon, 15 Jun 2026 04:15:45 GMT
COPY file:f3a7d39ee1404b5d93b5454e6014ed02f219e8a196f3df41d84d2e0e61c935f5 in /root/buildinfo/labels.json      
# Mon, 15 Jun 2026 04:15:45 GMT
LABEL "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="92938083b76077787596c980f5cdc39e89c50a24" "org.opencontainers.image.revision"="92938083b76077787596c980f5cdc39e89c50a24" "build-date"="2026-06-15T04:15:31Z" "org.opencontainers.image.created"="2026-06-15T04:15:31Z" "release"="1781496742"org.opencontainers.image.revision=92938083b76077787596c980f5cdc39e89c50a24,org.opencontainers.image.created=2026-06-15T04:15:31Z
# Mon, 15 Jun 2026 23:13:13 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 15 Jun 2026 23:13:13 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 15 Jun 2026 23:13:13 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 15 Jun 2026 23:13:13 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en     ;     microdnf clean all # buildkit
# Mon, 15 Jun 2026 23:13:13 GMT
ENV JAVA_VERSION=jdk8u492-b09
# Mon, 15 Jun 2026 23:13:17 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='d5e50cb002600007dbdfac523605d26196607fa5212db0942ef05cdce9fe2892';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u492-b09/OpenJDK8U-jre_aarch64_linux_hotspot_8u492b09.tar.gz';          ;;        ppc64le)          ESUM='4f724a0fce1117521a3a3e55ebb0281d56f6c9a066092bc3186ee40d8cd955a2';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u492-b09/OpenJDK8U-jre_ppc64le_linux_hotspot_8u492b09.tar.gz';          ;;        x86_64)          ESUM='8eef3d4a837bb7a9e45d30a7579d84d5b76a4321f4376573311e6bf89e48f9b0';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u492-b09/OpenJDK8U-jre_x64_linux_hotspot_8u492b09.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz; # buildkit
# Mon, 15 Jun 2026 23:13:17 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java -version"; java -version;     echo "Complete." # buildkit
# Mon, 15 Jun 2026 23:13:17 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Mon, 15 Jun 2026 23:13:17 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
```

-	Layers:
	-	`sha256:06005d885e6ce6c0708c4294316153d2de40b8859a131bbba11795c4f1e5eb71`  
		Last Modified: Mon, 15 Jun 2026 04:58:33 GMT  
		Size: 38.9 MB (38873024 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbc626b606cc6508a44cd43c74c96a166e86742c3654a2e137dbcab54f867b3a`  
		Last Modified: Mon, 15 Jun 2026 23:13:29 GMT  
		Size: 28.1 MB (28098935 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39989372d9910fe3ab5b09df7a6122eaf99d2fd499e541f54983852fd598777f`  
		Last Modified: Mon, 15 Jun 2026 23:13:30 GMT  
		Size: 41.3 MB (41301611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b661ced8847924d98333c2255f45c735267d3ce81fb8c8d6e38591f729560066`  
		Last Modified: Mon, 15 Jun 2026 23:13:28 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0a30c28c6d36f61fcfd599a3751369c41102bc7758d01bb3c26e7e7eb3844a7`  
		Last Modified: Mon, 15 Jun 2026 23:13:28 GMT  
		Size: 2.5 KB (2472 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:8-jre-ubi9-minimal` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:9a201a6851473cb1c86a8eefc7362d5473ceda9cc40d5d3204e7ad59a97688d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2458981 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:692347e9c76bac652d05f238b8195cdd3bbfc6fb9e84768a0c05514c35665b09`

```dockerfile
```

-	Layers:
	-	`sha256:b9cf5b6e93d59168345d8e800b0dedb866487e156af516b886bd912daa55715b`  
		Last Modified: Mon, 15 Jun 2026 23:13:28 GMT  
		Size: 2.4 MB (2439530 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:550b855008c7d6d90563c11e9bb20c84d583d98083864b74671d62e45a861a17`  
		Last Modified: Mon, 15 Jun 2026 23:13:28 GMT  
		Size: 19.5 KB (19451 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-temurin:8-jre-ubi9-minimal` - linux; ppc64le

```console
$ docker pull eclipse-temurin@sha256:6e637869d237541ebbd1c9af4cb3b86a966e019473c5afd711b1958bd81e6dd8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **117.0 MB (116983201 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1587fc6c51be30a998aebf05b08a9cb8a6d00a64e8076d80318670cbade75627`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`

```dockerfile
# Tue, 02 Jun 2026 05:43:57 GMT
LABEL maintainer="Red Hat, Inc."
# Tue, 02 Jun 2026 05:43:57 GMT
LABEL vendor="Red Hat, Inc."
# Tue, 02 Jun 2026 05:43:57 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Tue, 02 Jun 2026 05:43:57 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.8"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Tue, 02 Jun 2026 05:43:57 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Tue, 02 Jun 2026 05:43:57 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Tue, 02 Jun 2026 05:43:57 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Tue, 02 Jun 2026 05:43:57 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Tue, 02 Jun 2026 05:43:57 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Tue, 02 Jun 2026 05:43:57 GMT
LABEL io.openshift.expose-services=""
# Tue, 02 Jun 2026 05:43:57 GMT
LABEL io.openshift.tags="minimal rhel9"
# Tue, 02 Jun 2026 05:43:57 GMT
ENV container oci
# Tue, 02 Jun 2026 05:43:58 GMT
COPY dir:e2b77dc18737d07e8e5246d22c774c81a15fd49086dce884c4ad7e020854e7f1 in /      
# Tue, 02 Jun 2026 05:43:58 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Tue, 02 Jun 2026 05:43:58 GMT
CMD ["/bin/bash"]
# Tue, 02 Jun 2026 05:43:58 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /usr/share/buildinfo/content-sets.json      
# Tue, 02 Jun 2026 05:43:58 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /root/buildinfo/content_manifests/content-sets.json      
# Tue, 02 Jun 2026 05:43:58 GMT
COPY file:51b0adf8b5a4c3a24ace6c346ea6678803925c6cc30d08b64751f980b4528cc2 in /usr/share/buildinfo/labels.json      
# Tue, 02 Jun 2026 05:43:58 GMT
COPY file:51b0adf8b5a4c3a24ace6c346ea6678803925c6cc30d08b64751f980b4528cc2 in /root/buildinfo/labels.json      
# Tue, 02 Jun 2026 05:43:58 GMT
LABEL "architecture"="ppc64le" "vcs-type"="git" "vcs-ref"="842dd1c603c36c8d242d5ec075adccffb3bfea5c" "org.opencontainers.image.revision"="842dd1c603c36c8d242d5ec075adccffb3bfea5c" "build-date"="2026-06-02T05:43:46Z" "org.opencontainers.image.created"="2026-06-02T05:43:46Z" "release"="1780378819"org.opencontainers.image.revision=842dd1c603c36c8d242d5ec075adccffb3bfea5c,org.opencontainers.image.created=2026-06-02T05:43:46Z
# Tue, 02 Jun 2026 22:45:42 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 02 Jun 2026 22:45:42 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Jun 2026 22:45:42 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 02 Jun 2026 22:45:42 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en     ;     microdnf clean all # buildkit
# Tue, 02 Jun 2026 22:45:42 GMT
ENV JAVA_VERSION=jdk8u492-b09
# Tue, 02 Jun 2026 22:46:26 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='d5e50cb002600007dbdfac523605d26196607fa5212db0942ef05cdce9fe2892';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u492-b09/OpenJDK8U-jre_aarch64_linux_hotspot_8u492b09.tar.gz';          ;;        ppc64le)          ESUM='4f724a0fce1117521a3a3e55ebb0281d56f6c9a066092bc3186ee40d8cd955a2';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u492-b09/OpenJDK8U-jre_ppc64le_linux_hotspot_8u492b09.tar.gz';          ;;        x86_64)          ESUM='8eef3d4a837bb7a9e45d30a7579d84d5b76a4321f4376573311e6bf89e48f9b0';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u492-b09/OpenJDK8U-jre_x64_linux_hotspot_8u492b09.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz; # buildkit
# Tue, 02 Jun 2026 22:46:27 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java -version"; java -version;     echo "Complete." # buildkit
# Tue, 02 Jun 2026 22:46:28 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 02 Jun 2026 22:46:28 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
```

-	Layers:
	-	`sha256:5ff77d7ff78e7752137c3eba042a793ae2b415158af730c2f66c23814842a63f`  
		Last Modified: Tue, 02 Jun 2026 12:13:00 GMT  
		Size: 45.1 MB (45149918 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1fe7aeed3e9a0e4db7600177f2e2ad0b5eafa7a4390b1e052377528fb46b8a3`  
		Last Modified: Tue, 02 Jun 2026 22:46:32 GMT  
		Size: 30.1 MB (30090253 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c260d5b9fab40b35083ec1b817bc7e62616a1f425d5c96f123f712fd4b5e4be`  
		Last Modified: Tue, 02 Jun 2026 22:46:52 GMT  
		Size: 41.7 MB (41740436 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc4ab35fd90fc748f8809558d4d2307b54eb1af16f99344dc148151ac19307b3`  
		Last Modified: Tue, 02 Jun 2026 22:46:49 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6f52d7c135aa30470807db5d4d000225137b6b9728ab07929ccdf3092390206`  
		Last Modified: Tue, 02 Jun 2026 22:46:51 GMT  
		Size: 2.5 KB (2468 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:8-jre-ubi9-minimal` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:092a433a2870eefd5255c773c964be07fbb5d000ad8be44f1bb0901525a20771
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2459576 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e33a4af8bc4d610c00eff8da61b612a5c48c3a49d3ac6893a4cc79c9e0b386a`

```dockerfile
```

-	Layers:
	-	`sha256:26608ac9a3f8bc6cdeee5cb0a788b0b42fb8429487c75a1b57d5b09d3fcd7eb4`  
		Last Modified: Tue, 02 Jun 2026 22:46:51 GMT  
		Size: 2.4 MB (2440199 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f420a0990ebacfac32ac9aa458e780f8843f1bfc0bbeae550e47c4a638e9d4bf`  
		Last Modified: Tue, 02 Jun 2026 22:46:51 GMT  
		Size: 19.4 KB (19377 bytes)  
		MIME: application/vnd.in-toto+json
