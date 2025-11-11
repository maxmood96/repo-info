## `eclipse-temurin:8-jdk-ubi10-minimal`

```console
$ docker pull eclipse-temurin@sha256:c160e45343c6f9b1bce78ad7d636f57ab0d8e46602ed767899e85c00da14659e
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
$ docker pull eclipse-temurin@sha256:c18fe0363f93fcd2d09e8bf870c30035943dc6d07c8cfa09132b4afe6339103b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **149.0 MB (149037910 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f9158c1e998e5902dbeaf0f9ca54c4f69e1aafb9d197b976ab774349fae8799`
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
# Mon, 10 Nov 2025 20:10:23 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 10 Nov 2025 20:10:23 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 10 Nov 2025 20:10:23 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 10 Nov 2025 20:10:23 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en         gnupg2     ;     microdnf clean all # buildkit
# Mon, 10 Nov 2025 20:10:23 GMT
ENV JAVA_VERSION=jdk8u472-b08
# Mon, 10 Nov 2025 20:10:27 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='e2aff19d85d2441e409d6cbdf12ef7c2acabb0de73bca4207947135dcaa935a2';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u472-b08/OpenJDK8U-jdk_aarch64_linux_hotspot_8u472b08.tar.gz';          ;;        ppc64le)          ESUM='eaf57a4564265583b0641c878bea8943d27ef110c096868f686dae179fb45d8f';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u472-b08/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u472b08.tar.gz';          ;;        x86_64)          ESUM='5becaa4ac660e844c5a39e2ebc39ff5ac824c37ff1b625af8c8b111dc13c3592';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u472-b08/OpenJDK8U-jdk_x64_linux_hotspot_8u472b08.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip; # buildkit
# Mon, 10 Nov 2025 20:10:27 GMT
RUN set -eux;     echo "Verifying install ...";     echo "javac -version"; javac -version;     echo "java -version"; java -version;     echo "Complete." # buildkit
# Mon, 10 Nov 2025 20:10:27 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Mon, 10 Nov 2025 20:10:27 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
```

-	Layers:
	-	`sha256:32b34b6043df53356073fca74558aa4fb64fa2c3d92bc988ada13ba9600db416`  
		Last Modified: Mon, 10 Nov 2025 12:11:59 GMT  
		Size: 33.4 MB (33442309 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e703bfd16214419f0ce2ef4600fdb92412059a8cfaa6ef3f22d5971a161f5c45`  
		Last Modified: Mon, 10 Nov 2025 20:10:52 GMT  
		Size: 60.9 MB (60859250 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03b5a64e3cbbfeccd8dcee03f29ebc86b98d10279f6acf1a69f74dd2036cc8a2`  
		Last Modified: Mon, 10 Nov 2025 20:10:57 GMT  
		Size: 54.7 MB (54733908 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d48dc00bde046575a9c5859e3efa409df5ef816d3cb5d6a139b9bf898ecee12e`  
		Last Modified: Mon, 10 Nov 2025 20:10:48 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28cb6df4fc0c8e134afd55e6fdc15920ddbe2216f953a5994ddd9a96dd35d5cf`  
		Last Modified: Mon, 10 Nov 2025 20:10:48 GMT  
		Size: 2.3 KB (2315 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:8-jdk-ubi10-minimal` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:19e9ac4f344bf3469cc2582e051678b27b31466464eb359be33d9e582b1ab58a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5816189 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fae99c0eab45b0ad0d8aa021ab8885d0166a8af4c63ba185b9923398d55858cb`

```dockerfile
```

-	Layers:
	-	`sha256:5d1fb311b6db958fe21cca5888cd392b32efe34a46dc9585b291bb9bd4cc44d9`  
		Last Modified: Mon, 10 Nov 2025 22:16:34 GMT  
		Size: 5.8 MB (5796150 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0560c51efdbe424f2baff3c6e9b7f4c42d8e7eeed41074ab79a12086b7312d5c`  
		Last Modified: Mon, 10 Nov 2025 22:16:35 GMT  
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
$ docker pull eclipse-temurin@sha256:6fdfb1a34a84d1205ef5fd9e9f7c3b2b0f28db190870ac1a82900d388ffb2290
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **153.3 MB (153274242 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:62bfcbfc6289f0e5cb3b7ff3b4f70d7c49190fdd264cc0e177f32aa00a188812`
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
ENV JAVA_VERSION=jdk8u472-b08
# Mon, 10 Nov 2025 22:20:10 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='e2aff19d85d2441e409d6cbdf12ef7c2acabb0de73bca4207947135dcaa935a2';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u472-b08/OpenJDK8U-jdk_aarch64_linux_hotspot_8u472b08.tar.gz';          ;;        ppc64le)          ESUM='eaf57a4564265583b0641c878bea8943d27ef110c096868f686dae179fb45d8f';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u472-b08/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u472b08.tar.gz';          ;;        x86_64)          ESUM='5becaa4ac660e844c5a39e2ebc39ff5ac824c37ff1b625af8c8b111dc13c3592';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u472-b08/OpenJDK8U-jdk_x64_linux_hotspot_8u472b08.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip; # buildkit
# Mon, 10 Nov 2025 22:20:10 GMT
RUN set -eux;     echo "Verifying install ...";     echo "javac -version"; javac -version;     echo "java -version"; java -version;     echo "Complete." # buildkit
# Mon, 10 Nov 2025 22:20:10 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Mon, 10 Nov 2025 22:20:10 GMT
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
	-	`sha256:8e99da5cc84301bc9a63fd2c72472e795f0c9d7a116b22272e3424cd67d923bd`  
		Last Modified: Mon, 10 Nov 2025 22:21:05 GMT  
		Size: 52.2 MB (52175870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f12f1660c5c7624ab30f9c644c3180e200d75aa1575f1ba96dc60add6a210f63`  
		Last Modified: Mon, 10 Nov 2025 22:21:02 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:615b04889b03c043f34d5d0d898f94be76f56b96ad4f24a3dcb875c1617d31b4`  
		Last Modified: Mon, 10 Nov 2025 22:21:02 GMT  
		Size: 2.3 KB (2316 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:8-jdk-ubi10-minimal` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:171f26edfb0104f039150eed29b3372a23b3fcafbbb42435c8ac48eace928884
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5803970 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5721fd3145c1770c45dacd6357e7eff9f891a72688ab7a06c27c8e46f5c524c4`

```dockerfile
```

-	Layers:
	-	`sha256:68904d91e1e1bd4a0bc553632abb34e99faf9906e4819af37d1ec72292e26e54`  
		Last Modified: Tue, 11 Nov 2025 01:15:53 GMT  
		Size: 5.8 MB (5783895 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:362fb6f2878bd83c471564a751de2da621abb69d522f5a1e590f77902eac46c1`  
		Last Modified: Tue, 11 Nov 2025 01:15:53 GMT  
		Size: 20.1 KB (20075 bytes)  
		MIME: application/vnd.in-toto+json
