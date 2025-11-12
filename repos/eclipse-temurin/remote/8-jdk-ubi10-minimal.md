## `eclipse-temurin:8-jdk-ubi10-minimal`

```console
$ docker pull eclipse-temurin@sha256:f2228b6421ce11708f8f398e0ecc3b5c3a930fe4d05376544a9d280af4808191
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `eclipse-temurin:8-jdk-ubi10-minimal` - linux; amd64

```console
$ docker pull eclipse-temurin@sha256:9975d76b8e0afa414872fd0da99bca38d98c1aca303170ecd01733932eeb2272
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **146.6 MB (146569075 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b83bde2cadfe4d774a5a24c1d6258fceaee01d89576937c25adc74e9529366b`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`

```dockerfile
# Mon, 03 Nov 2025 17:11:07 GMT
LABEL maintainer="Red Hat, Inc."
# Mon, 03 Nov 2025 17:11:07 GMT
LABEL vendor="Red Hat, Inc."
# Mon, 03 Nov 2025 17:11:07 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Mon, 03 Nov 2025 17:11:07 GMT
LABEL com.redhat.component="ubi10-minimal-container"       name="ubi10/ubi-minimal"       version="10.1"       cpe="cpe:/o:redhat:enterprise_linux:10.1"       distribution-scope="public"
# Mon, 03 Nov 2025 17:11:07 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Mon, 03 Nov 2025 17:11:07 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 10."
# Mon, 03 Nov 2025 17:11:08 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 03 Nov 2025 17:11:08 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 03 Nov 2025 17:11:08 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 10 Minimal"
# Mon, 03 Nov 2025 17:11:08 GMT
LABEL io.openshift.expose-services=""
# Mon, 03 Nov 2025 17:11:08 GMT
LABEL io.openshift.tags="minimal rhel10"
# Mon, 03 Nov 2025 17:11:08 GMT
LABEL compose-id="RHEL-10.1-updates-20251031.1"
# Mon, 03 Nov 2025 17:11:09 GMT
ENV container oci
# Mon, 03 Nov 2025 17:11:10 GMT
COPY dir:b2070c3a584696dfa50295995b98f1ca6f69ef03e4ee4a779757baf0b56a1546 in /      
# Mon, 03 Nov 2025 17:11:10 GMT
COPY file:5de33b5fc08b00635bccf9134a18978dba13e2250aa51838f9969515a3957847 in /etc/yum.repos.d/.      
# Mon, 03 Nov 2025 17:11:10 GMT
CMD ["/bin/bash"]
# Mon, 03 Nov 2025 17:11:10 GMT
COPY file:595171150af68abc798ea385f7988d74b566aa8e84babff137f00b08b2164683 in /usr/share/buildinfo/content-sets.json      
# Mon, 03 Nov 2025 17:11:10 GMT
COPY file:595171150af68abc798ea385f7988d74b566aa8e84babff137f00b08b2164683 in /root/buildinfo/content_manifests/content-sets.json      
# Mon, 03 Nov 2025 17:11:10 GMT
COPY file:e8d237b49ae34a5f140de55c7c082573fef974034e3d7ddb0b43a196c7b15275 in /usr/share/buildinfo/labels.json      
# Mon, 03 Nov 2025 17:11:11 GMT
COPY file:e8d237b49ae34a5f140de55c7c082573fef974034e3d7ddb0b43a196c7b15275 in /root/buildinfo/labels.json      
# Mon, 03 Nov 2025 17:11:12 GMT
LABEL "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="95310b85c4dfa1ed23494ca51d86f210cb1256bf" "org.opencontainers.image.revision"="95310b85c4dfa1ed23494ca51d86f210cb1256bf" "build-date"="2025-11-03T17:10:18Z" "release"="1762189639"org.opencontainers.image.revision=95310b85c4dfa1ed23494ca51d86f210cb1256bf
# Wed, 12 Nov 2025 18:38:21 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 12 Nov 2025 18:38:21 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 12 Nov 2025 18:38:21 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 12 Nov 2025 18:38:21 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en         gnupg2     ;     microdnf clean all # buildkit
# Wed, 12 Nov 2025 18:38:21 GMT
ENV JAVA_VERSION=jdk8u472-b08
# Wed, 12 Nov 2025 18:38:24 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='e2aff19d85d2441e409d6cbdf12ef7c2acabb0de73bca4207947135dcaa935a2';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u472-b08/OpenJDK8U-jdk_aarch64_linux_hotspot_8u472b08.tar.gz';          ;;        ppc64le)          ESUM='eaf57a4564265583b0641c878bea8943d27ef110c096868f686dae179fb45d8f';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u472-b08/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u472b08.tar.gz';          ;;        x86_64)          ESUM='5becaa4ac660e844c5a39e2ebc39ff5ac824c37ff1b625af8c8b111dc13c3592';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u472-b08/OpenJDK8U-jdk_x64_linux_hotspot_8u472b08.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip; # buildkit
# Wed, 12 Nov 2025 18:38:24 GMT
RUN set -eux;     echo "Verifying install ...";     echo "javac -version"; javac -version;     echo "java -version"; java -version;     echo "Complete." # buildkit
# Wed, 12 Nov 2025 18:38:24 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 12 Nov 2025 18:38:24 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
```

-	Layers:
	-	`sha256:e2fb7c31c3da29493a9042fb2aac284034d054c3aa5fe92e1f234b9e077ede47`  
		Last Modified: Wed, 12 Nov 2025 00:12:41 GMT  
		Size: 34.2 MB (34167037 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6dd037d4d03f153721fcc127ef99b1ed3824457180380298974f168a684431ab`  
		Last Modified: Wed, 12 Nov 2025 18:38:54 GMT  
		Size: 57.7 MB (57665717 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1dba10efa1666a5b9ccc8212c5372a42662aebf2e1425e7dacdd76f07ed447b8`  
		Last Modified: Wed, 12 Nov 2025 18:38:57 GMT  
		Size: 54.7 MB (54733880 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63f68132c1792534f32cb37e913afaa8aa27420b97aa9ad17e403f9f553b66c7`  
		Last Modified: Wed, 12 Nov 2025 18:38:46 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:face33f212139785515a92f7aed50d5f43c7aaa0cd2f40c03ce5c5fac09a11c0`  
		Last Modified: Wed, 12 Nov 2025 18:38:50 GMT  
		Size: 2.3 KB (2315 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:8-jdk-ubi10-minimal` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:d0de58fd293b7254e7681dd83069e3952ce0f79abc9674aff59fcd9dce428cee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5822551 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:92f06c1440f24c628e2811b0ed6cc82276dee311f77691327be7f6e0424aacd6`

```dockerfile
```

-	Layers:
	-	`sha256:80c9885caab065fb188cee4403b13f95434fd305c91cc4abcb157b6b59395c91`  
		Last Modified: Wed, 12 Nov 2025 19:16:32 GMT  
		Size: 5.8 MB (5802512 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c07563eefdcfea304f30064282672fb255818027ff3a6623ce1cda312f3b9502`  
		Last Modified: Wed, 12 Nov 2025 19:16:33 GMT  
		Size: 20.0 KB (20039 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-temurin:8-jdk-ubi10-minimal` - linux; arm64 variant v8

```console
$ docker pull eclipse-temurin@sha256:776bda337729aee7fd5c1e45e03dcbb37023268a366fdd7946d4dfc6b09515f2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **145.3 MB (145279603 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b6f9668ac6fe70c79d3e198dd77e29759fe31980ce369013b59d13b4400f0d12`
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
ENV JAVA_VERSION=jdk8u472-b08
# Mon, 10 Nov 2025 20:14:20 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='e2aff19d85d2441e409d6cbdf12ef7c2acabb0de73bca4207947135dcaa935a2';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u472-b08/OpenJDK8U-jdk_aarch64_linux_hotspot_8u472b08.tar.gz';          ;;        ppc64le)          ESUM='eaf57a4564265583b0641c878bea8943d27ef110c096868f686dae179fb45d8f';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u472-b08/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u472b08.tar.gz';          ;;        x86_64)          ESUM='5becaa4ac660e844c5a39e2ebc39ff5ac824c37ff1b625af8c8b111dc13c3592';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u472-b08/OpenJDK8U-jdk_x64_linux_hotspot_8u472b08.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip; # buildkit
# Mon, 10 Nov 2025 20:14:20 GMT
RUN set -eux;     echo "Verifying install ...";     echo "javac -version"; javac -version;     echo "java -version"; java -version;     echo "Complete." # buildkit
# Mon, 10 Nov 2025 20:14:20 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Mon, 10 Nov 2025 20:14:20 GMT
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
	-	`sha256:9a1698631c79a7cbbfb07f22bdb364aad36affd59724c3adcb83ff3e12823504`  
		Last Modified: Mon, 10 Nov 2025 20:14:50 GMT  
		Size: 53.8 MB (53815587 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3e0e20335867ebdf9dc43db4bab1f253a603d5b7409b78722a7e7a0b53611a6`  
		Last Modified: Mon, 10 Nov 2025 20:14:44 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ba848f0ac7f32ac330c5bafc449d54e45897ff507489b547cdd4059ab332197`  
		Last Modified: Mon, 10 Nov 2025 20:14:43 GMT  
		Size: 2.3 KB (2316 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:8-jdk-ubi10-minimal` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:1ac1709336ecd024219fbea93f6c00d9f6472bcb62ee514f5345be2d717ca1f4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5816493 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eae2f4b98744811d6f3bee5483355631c7ee63a864ec78d60c115137f656b45d`

```dockerfile
```

-	Layers:
	-	`sha256:65f3e69e680e1dbac70056d8a4fd8141b10c0367c484abe96b73b819c86fc994`  
		Last Modified: Mon, 10 Nov 2025 22:16:42 GMT  
		Size: 5.8 MB (5796338 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:336f36d76df973da6104ed160744ff4e34254c26e6d8a51cc28786fa0c451a59`  
		Last Modified: Mon, 10 Nov 2025 22:16:43 GMT  
		Size: 20.2 KB (20155 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-temurin:8-jdk-ubi10-minimal` - linux; ppc64le

```console
$ docker pull eclipse-temurin@sha256:4f32fb7c687f56dfb7ed889628864b9dff59033d9759065879cfd994ff4aae60
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **150.1 MB (150092501 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ade3b2392e1c2936853fb50bf6e1d3a18f3bb9f4b6a96b74fba94068aff140c1`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`

```dockerfile
# Mon, 03 Nov 2025 18:21:16 GMT
LABEL maintainer="Red Hat, Inc."
# Mon, 03 Nov 2025 18:21:16 GMT
LABEL vendor="Red Hat, Inc."
# Mon, 03 Nov 2025 18:21:16 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Mon, 03 Nov 2025 18:21:16 GMT
LABEL com.redhat.component="ubi10-minimal-container"       name="ubi10/ubi-minimal"       version="10.1"       cpe="cpe:/o:redhat:enterprise_linux:10.1"       distribution-scope="public"
# Mon, 03 Nov 2025 18:21:16 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Mon, 03 Nov 2025 18:21:16 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 10."
# Mon, 03 Nov 2025 18:21:16 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 03 Nov 2025 18:21:16 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 03 Nov 2025 18:21:16 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 10 Minimal"
# Mon, 03 Nov 2025 18:21:17 GMT
LABEL io.openshift.expose-services=""
# Mon, 03 Nov 2025 18:21:17 GMT
LABEL io.openshift.tags="minimal rhel10"
# Mon, 03 Nov 2025 18:21:17 GMT
LABEL compose-id="RHEL-10.1-updates-20251031.1"
# Mon, 03 Nov 2025 18:21:17 GMT
ENV container oci
# Mon, 03 Nov 2025 18:21:19 GMT
COPY dir:bddbfbd27697aed0d6ba6e3639d53eb2bcbf54a469bc264141734564ee0873d3 in /      
# Mon, 03 Nov 2025 18:21:19 GMT
COPY file:5de33b5fc08b00635bccf9134a18978dba13e2250aa51838f9969515a3957847 in /etc/yum.repos.d/.      
# Mon, 03 Nov 2025 18:21:19 GMT
CMD ["/bin/bash"]
# Mon, 03 Nov 2025 18:21:20 GMT
COPY file:595171150af68abc798ea385f7988d74b566aa8e84babff137f00b08b2164683 in /usr/share/buildinfo/content-sets.json      
# Mon, 03 Nov 2025 18:21:21 GMT
COPY file:595171150af68abc798ea385f7988d74b566aa8e84babff137f00b08b2164683 in /root/buildinfo/content_manifests/content-sets.json      
# Mon, 03 Nov 2025 18:21:21 GMT
COPY file:db0b3bfc9b0c5f121f2453bb59e26e6e1b4ab566a800db9e34c541da8076e42d in /usr/share/buildinfo/labels.json      
# Mon, 03 Nov 2025 18:21:22 GMT
COPY file:db0b3bfc9b0c5f121f2453bb59e26e6e1b4ab566a800db9e34c541da8076e42d in /root/buildinfo/labels.json      
# Mon, 03 Nov 2025 18:21:23 GMT
LABEL "architecture"="ppc64le" "vcs-type"="git" "vcs-ref"="95310b85c4dfa1ed23494ca51d86f210cb1256bf" "org.opencontainers.image.revision"="95310b85c4dfa1ed23494ca51d86f210cb1256bf" "build-date"="2025-11-03T18:20:23Z" "release"="1762189639"org.opencontainers.image.revision=95310b85c4dfa1ed23494ca51d86f210cb1256bf
# Wed, 12 Nov 2025 18:51:18 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 12 Nov 2025 18:51:18 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 12 Nov 2025 18:51:18 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 12 Nov 2025 18:51:18 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en         gnupg2     ;     microdnf clean all # buildkit
# Wed, 12 Nov 2025 18:51:18 GMT
ENV JAVA_VERSION=jdk8u472-b08
# Wed, 12 Nov 2025 18:51:25 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='e2aff19d85d2441e409d6cbdf12ef7c2acabb0de73bca4207947135dcaa935a2';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u472-b08/OpenJDK8U-jdk_aarch64_linux_hotspot_8u472b08.tar.gz';          ;;        ppc64le)          ESUM='eaf57a4564265583b0641c878bea8943d27ef110c096868f686dae179fb45d8f';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u472-b08/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u472b08.tar.gz';          ;;        x86_64)          ESUM='5becaa4ac660e844c5a39e2ebc39ff5ac824c37ff1b625af8c8b111dc13c3592';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u472-b08/OpenJDK8U-jdk_x64_linux_hotspot_8u472b08.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip; # buildkit
# Wed, 12 Nov 2025 18:51:26 GMT
RUN set -eux;     echo "Verifying install ...";     echo "javac -version"; javac -version;     echo "java -version"; java -version;     echo "Complete." # buildkit
# Wed, 12 Nov 2025 18:51:26 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 12 Nov 2025 18:51:26 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
```

-	Layers:
	-	`sha256:f0606a13920710459cad07c2d91ffb3bc0d8c2d18eb333131c2e90dc0ae025c2`  
		Last Modified: Wed, 12 Nov 2025 00:12:42 GMT  
		Size: 38.2 MB (38231260 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:496c0fa2afff4fce2da3348f13f3ff118dfa655106daf72e83b8d728ab5a3304`  
		Last Modified: Wed, 12 Nov 2025 18:52:31 GMT  
		Size: 59.7 MB (59682969 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:819c4da5f0f5e6ff12c45b7c62421e7c8ce42b9afb440182d0484c43a1d07fcb`  
		Last Modified: Wed, 12 Nov 2025 18:52:31 GMT  
		Size: 52.2 MB (52175830 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fcec7059fdb0263d0aec74e5b3e89eac6cb88d3fe090ec8a4255015d24b7e83`  
		Last Modified: Wed, 12 Nov 2025 18:52:25 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:616a55ca3f9fb4fe7ac8f69d1f45809a0f8014829b5e3e5232d13506a83f8a40`  
		Last Modified: Wed, 12 Nov 2025 18:52:26 GMT  
		Size: 2.3 KB (2314 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:8-jdk-ubi10-minimal` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:db763423c6282290497668b3fbefd7034ebcbfc0ee0cdaad7bcb3fcad21f19a7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5810332 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e2ad0e2d0958739bcf6a4be4d5a6256bad455e2f2618a0b95114b1e1db2e4d8`

```dockerfile
```

-	Layers:
	-	`sha256:fb421b6711a17553b5d9541d3a5419a13beecd28243c88cdb52703f6a8f6f82f`  
		Last Modified: Wed, 12 Nov 2025 19:16:44 GMT  
		Size: 5.8 MB (5790257 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5ecab2de58e302207c7d071401aafd8b5c73defe6ede9ee5de2016adc1fb0be4`  
		Last Modified: Wed, 12 Nov 2025 19:16:45 GMT  
		Size: 20.1 KB (20075 bytes)  
		MIME: application/vnd.in-toto+json
