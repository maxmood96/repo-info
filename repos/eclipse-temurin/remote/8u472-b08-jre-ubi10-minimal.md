## `eclipse-temurin:8u472-b08-jre-ubi10-minimal`

```console
$ docker pull eclipse-temurin@sha256:e1685f8c2424474d7a35f6e24e13da149714c4b521c0edc74c9c02fe72ac7e1d
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
$ docker pull eclipse-temurin@sha256:48ac4636b7dbca4207ae04d485f0b5c237108212fe0eb99fd36cd18f1ee4742a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **131.9 MB (131852270 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0cbe3b1d28ecd02fc0a372959f00b7917fd4a42fb3becc8cf323decd7df65149`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`

```dockerfile
# Mon, 01 Dec 2025 15:52:04 GMT
LABEL maintainer="Red Hat, Inc."
# Mon, 01 Dec 2025 15:52:04 GMT
LABEL vendor="Red Hat, Inc."
# Mon, 01 Dec 2025 15:52:04 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Mon, 01 Dec 2025 15:52:04 GMT
LABEL com.redhat.component="ubi10-minimal-container"       name="ubi10/ubi-minimal"       version="10.1"       cpe="cpe:/o:redhat:enterprise_linux:10.1"       distribution-scope="public"
# Mon, 01 Dec 2025 15:52:04 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Mon, 01 Dec 2025 15:52:04 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 10."
# Mon, 01 Dec 2025 15:52:04 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 01 Dec 2025 15:52:04 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 01 Dec 2025 15:52:04 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 10 Minimal"
# Mon, 01 Dec 2025 15:52:04 GMT
LABEL io.openshift.expose-services=""
# Mon, 01 Dec 2025 15:52:05 GMT
LABEL io.openshift.tags="minimal rhel10"
# Mon, 01 Dec 2025 15:52:05 GMT
ENV container oci
# Mon, 01 Dec 2025 15:52:05 GMT
COPY dir:e3f52ba99077b3bc7b7921467816c9e1d6afafe638b5c85f61d17a96c866d5a4 in /      
# Mon, 01 Dec 2025 15:52:06 GMT
COPY file:5de33b5fc08b00635bccf9134a18978dba13e2250aa51838f9969515a3957847 in /etc/yum.repos.d/.      
# Mon, 01 Dec 2025 15:52:06 GMT
CMD ["/bin/bash"]
# Mon, 01 Dec 2025 15:52:06 GMT
COPY file:595171150af68abc798ea385f7988d74b566aa8e84babff137f00b08b2164683 in /usr/share/buildinfo/content-sets.json      
# Mon, 01 Dec 2025 15:52:06 GMT
COPY file:595171150af68abc798ea385f7988d74b566aa8e84babff137f00b08b2164683 in /root/buildinfo/content_manifests/content-sets.json      
# Mon, 01 Dec 2025 15:52:06 GMT
COPY file:922399bb1f6dd7741b16f1cdd9842f87612db7b462e38b1bbeae37d5c71e21d7 in /usr/share/buildinfo/labels.json      
# Mon, 01 Dec 2025 15:52:07 GMT
COPY file:922399bb1f6dd7741b16f1cdd9842f87612db7b462e38b1bbeae37d5c71e21d7 in /root/buildinfo/labels.json      
# Mon, 01 Dec 2025 15:52:07 GMT
LABEL "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="f3ce7416a648177fb2c54fd1c28cc0dab0304a68" "org.opencontainers.image.revision"="f3ce7416a648177fb2c54fd1c28cc0dab0304a68" "build-date"="2025-12-01T15:51:47Z" "org.opencontainers.image.created"="2025-12-01T15:51:47Z" "release"="1764604111"org.opencontainers.image.revision=f3ce7416a648177fb2c54fd1c28cc0dab0304a68,org.opencontainers.image.created=2025-12-01T15:51:47Z
# Tue, 02 Dec 2025 00:37:44 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 02 Dec 2025 00:37:44 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Dec 2025 00:37:44 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 02 Dec 2025 00:37:44 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en         gnupg2     ;     microdnf clean all # buildkit
# Tue, 02 Dec 2025 00:37:44 GMT
ENV JAVA_VERSION=jdk8u472-b08
# Tue, 02 Dec 2025 00:38:15 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='c043807ad995fb3987bc1c42b16ebf0f1b5010868c3e9d20a941236d5bbb22b7';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u472-b08/OpenJDK8U-jre_aarch64_linux_hotspot_8u472b08.tar.gz';          ;;        ppc64le)          ESUM='a76eb0f46cd5134b0b8b52ef4dd54ac7fd7e5960fc7dce8772bfc455a5e83e40';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u472-b08/OpenJDK8U-jre_ppc64le_linux_hotspot_8u472b08.tar.gz';          ;;        x86_64)          ESUM='6f7fb5fd640a0fd00837344b0920cbc4b9b9284b50e66f33789e3b250446a16e';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u472-b08/OpenJDK8U-jre_x64_linux_hotspot_8u472b08.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz; # buildkit
# Tue, 02 Dec 2025 00:38:15 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java -version"; java -version;     echo "Complete." # buildkit
# Tue, 02 Dec 2025 00:38:16 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 02 Dec 2025 00:38:16 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
```

-	Layers:
	-	`sha256:3fe7185a3562260af267162d9816b8c41f88072fc86a6884c33d874ef0a74688`  
		Last Modified: Mon, 01 Dec 2025 18:12:29 GMT  
		Size: 34.6 MB (34621933 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1dfd0be18fe4c33d84edfb20868c6ad1174990231e9a127a60cb06607ff7fab8`  
		Last Modified: Tue, 02 Dec 2025 01:02:53 GMT  
		Size: 55.3 MB (55340248 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:386cb55151c6f797a17cd130d31a2ec87046df74ca7c0baa4dc61861e6c61258`  
		Last Modified: Tue, 02 Dec 2025 00:38:52 GMT  
		Size: 41.9 MB (41887670 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8c0b94564fea5b37cd66159b942a762ae6f51bca396f4e6e972a0878d81ba05`  
		Last Modified: Tue, 02 Dec 2025 00:38:45 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b621783ebeef1924ab158673bef35af44db07c5fafd7e3a12ee44a8646761de`  
		Last Modified: Tue, 02 Dec 2025 00:38:46 GMT  
		Size: 2.3 KB (2291 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:8u472-b08-jre-ubi10-minimal` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:35ab941b27e45d5393da8bc41705eb25f2eae13c1db637748c3c1f5b5c2ba88a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5645641 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e53978a0ae24715ee716baac65300a86f652f476a81098e5da3379a1fcfae634`

```dockerfile
```

-	Layers:
	-	`sha256:6ec9047e964ed5b6b445965500d6c211277f41e481ece5ada415e8f34c84340d`  
		Last Modified: Tue, 02 Dec 2025 01:18:35 GMT  
		Size: 5.6 MB (5626130 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:713b279da6b067bb3351bdab93982199faf11263317672f1e4c633289ee85333`  
		Last Modified: Tue, 02 Dec 2025 01:18:36 GMT  
		Size: 19.5 KB (19511 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-temurin:8u472-b08-jre-ubi10-minimal` - linux; arm64 variant v8

```console
$ docker pull eclipse-temurin@sha256:171f606fafba13bc53e105451869e282266a5b8eb45eef7a4b7ee75f351bcd52
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **128.6 MB (128623204 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c00e02261d9dcd9a1bd20dff561ea51c5d2decc3ac31b1aee9b46436d9842278`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`

```dockerfile
# Mon, 01 Dec 2025 16:14:10 GMT
LABEL maintainer="Red Hat, Inc."
# Mon, 01 Dec 2025 16:14:10 GMT
LABEL vendor="Red Hat, Inc."
# Mon, 01 Dec 2025 16:14:10 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Mon, 01 Dec 2025 16:14:10 GMT
LABEL com.redhat.component="ubi10-minimal-container"       name="ubi10/ubi-minimal"       version="10.1"       cpe="cpe:/o:redhat:enterprise_linux:10.1"       distribution-scope="public"
# Mon, 01 Dec 2025 16:14:10 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Mon, 01 Dec 2025 16:14:10 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 10."
# Mon, 01 Dec 2025 16:14:10 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 01 Dec 2025 16:14:10 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 01 Dec 2025 16:14:10 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 10 Minimal"
# Mon, 01 Dec 2025 16:14:10 GMT
LABEL io.openshift.expose-services=""
# Mon, 01 Dec 2025 16:14:10 GMT
LABEL io.openshift.tags="minimal rhel10"
# Mon, 01 Dec 2025 16:14:10 GMT
ENV container oci
# Mon, 01 Dec 2025 16:14:11 GMT
COPY dir:69dd4a0b5ba0f5bf7a4e00ffeb7ef3c8fe0f0bfc2283402327c0309bf841d6fa in /      
# Mon, 01 Dec 2025 16:14:11 GMT
COPY file:5de33b5fc08b00635bccf9134a18978dba13e2250aa51838f9969515a3957847 in /etc/yum.repos.d/.      
# Mon, 01 Dec 2025 16:14:11 GMT
CMD ["/bin/bash"]
# Mon, 01 Dec 2025 16:14:11 GMT
COPY file:595171150af68abc798ea385f7988d74b566aa8e84babff137f00b08b2164683 in /usr/share/buildinfo/content-sets.json      
# Mon, 01 Dec 2025 16:14:11 GMT
COPY file:595171150af68abc798ea385f7988d74b566aa8e84babff137f00b08b2164683 in /root/buildinfo/content_manifests/content-sets.json      
# Mon, 01 Dec 2025 16:14:11 GMT
COPY file:6f341067110dc29b8758b5d271970b09cd64dcb0e30a85b18012a177bb71753e in /usr/share/buildinfo/labels.json      
# Mon, 01 Dec 2025 16:14:11 GMT
COPY file:6f341067110dc29b8758b5d271970b09cd64dcb0e30a85b18012a177bb71753e in /root/buildinfo/labels.json      
# Mon, 01 Dec 2025 16:14:11 GMT
LABEL "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="f3ce7416a648177fb2c54fd1c28cc0dab0304a68" "org.opencontainers.image.revision"="f3ce7416a648177fb2c54fd1c28cc0dab0304a68" "build-date"="2025-12-01T16:13:49Z" "org.opencontainers.image.created"="2025-12-01T16:13:49Z" "release"="1764604111"org.opencontainers.image.revision=f3ce7416a648177fb2c54fd1c28cc0dab0304a68,org.opencontainers.image.created=2025-12-01T16:13:49Z
# Tue, 02 Dec 2025 00:42:46 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 02 Dec 2025 00:42:46 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Dec 2025 00:42:46 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 02 Dec 2025 00:42:46 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en         gnupg2     ;     microdnf clean all # buildkit
# Tue, 02 Dec 2025 00:42:46 GMT
ENV JAVA_VERSION=jdk8u472-b08
# Tue, 02 Dec 2025 00:44:02 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='c043807ad995fb3987bc1c42b16ebf0f1b5010868c3e9d20a941236d5bbb22b7';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u472-b08/OpenJDK8U-jre_aarch64_linux_hotspot_8u472b08.tar.gz';          ;;        ppc64le)          ESUM='a76eb0f46cd5134b0b8b52ef4dd54ac7fd7e5960fc7dce8772bfc455a5e83e40';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u472-b08/OpenJDK8U-jre_ppc64le_linux_hotspot_8u472b08.tar.gz';          ;;        x86_64)          ESUM='6f7fb5fd640a0fd00837344b0920cbc4b9b9284b50e66f33789e3b250446a16e';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u472-b08/OpenJDK8U-jre_x64_linux_hotspot_8u472b08.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz; # buildkit
# Tue, 02 Dec 2025 00:44:02 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java -version"; java -version;     echo "Complete." # buildkit
# Tue, 02 Dec 2025 00:44:02 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 02 Dec 2025 00:44:02 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
```

-	Layers:
	-	`sha256:9c27140b3e778c26a038c982eb0b0d7c55918358b1c1e3afdb013d53d318ad1f`  
		Last Modified: Mon, 01 Dec 2025 18:12:35 GMT  
		Size: 32.6 MB (32592499 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:272c1596a90b8edab1636e1e07b23392699072b955939a84b61846f1d64bdb40`  
		Last Modified: Tue, 02 Dec 2025 00:43:42 GMT  
		Size: 55.1 MB (55148104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e50c8e1f2ce76b4ef5989cd3f58746eedeeef0a4e6a9cd121f2fffa55278045b`  
		Last Modified: Tue, 02 Dec 2025 00:44:25 GMT  
		Size: 40.9 MB (40880182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dde10f2d2460e234891576ed5c5c4127011ddde430bcff516448782adc41205d`  
		Last Modified: Tue, 02 Dec 2025 00:44:22 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0772c82d8d1be932729e5de90658ff56390bdd2f7111a9ab6cffde4cb0a902b0`  
		Last Modified: Tue, 02 Dec 2025 00:44:22 GMT  
		Size: 2.3 KB (2291 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:8u472-b08-jre-ubi10-minimal` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:c24d061f9613a6617e53d16498727342f8397600cf20e7c48f48474757d7853f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5645912 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e892b20805378a4f9c7571db7a706b26a458eab7cc8fee852863df41651cf29`

```dockerfile
```

-	Layers:
	-	`sha256:b1e7e18c552a49c014865f42f25b921dd24ae990a262663313cbc20ee34507e0`  
		Last Modified: Tue, 02 Dec 2025 01:18:42 GMT  
		Size: 5.6 MB (5626298 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ebbe762702beaab3b633016fb3983bfa4eb73525fcf7619cfac8e55807412e4e`  
		Last Modified: Tue, 02 Dec 2025 01:18:43 GMT  
		Size: 19.6 KB (19614 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-temurin:8u472-b08-jre-ubi10-minimal` - linux; ppc64le

```console
$ docker pull eclipse-temurin@sha256:9cbb34b3a16150153def6c62950ad6a487c39c805025c18c5073e99b6bc5afdc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **137.3 MB (137346462 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cab0c730e9f6a6b047de000f642f2c6b6ff558d2fd6df67e5290a7603d9f628e`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`

```dockerfile
# Mon, 17 Nov 2025 07:03:31 GMT
LABEL maintainer="Red Hat, Inc."
# Mon, 17 Nov 2025 07:03:31 GMT
LABEL vendor="Red Hat, Inc."
# Mon, 17 Nov 2025 07:03:31 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Mon, 17 Nov 2025 07:03:31 GMT
LABEL com.redhat.component="ubi10-minimal-container"       name="ubi10/ubi-minimal"       version="10.1"       cpe="cpe:/o:redhat:enterprise_linux:10.1"       distribution-scope="public"
# Mon, 17 Nov 2025 07:03:31 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Mon, 17 Nov 2025 07:03:31 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 10."
# Mon, 17 Nov 2025 07:03:31 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 17 Nov 2025 07:03:31 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 17 Nov 2025 07:03:31 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 10 Minimal"
# Mon, 17 Nov 2025 07:03:31 GMT
LABEL io.openshift.expose-services=""
# Mon, 17 Nov 2025 07:03:31 GMT
LABEL io.openshift.tags="minimal rhel10"
# Mon, 17 Nov 2025 07:03:31 GMT
ENV container oci
# Mon, 17 Nov 2025 07:03:32 GMT
COPY dir:3f836289fcb5e4834914ff52d15c42d6b925906d318eaeb6e7ece83b813f7798 in /      
# Mon, 17 Nov 2025 07:03:32 GMT
COPY file:5de33b5fc08b00635bccf9134a18978dba13e2250aa51838f9969515a3957847 in /etc/yum.repos.d/.      
# Mon, 17 Nov 2025 07:03:32 GMT
CMD ["/bin/bash"]
# Mon, 17 Nov 2025 07:03:32 GMT
COPY file:595171150af68abc798ea385f7988d74b566aa8e84babff137f00b08b2164683 in /usr/share/buildinfo/content-sets.json      
# Mon, 17 Nov 2025 07:03:32 GMT
COPY file:595171150af68abc798ea385f7988d74b566aa8e84babff137f00b08b2164683 in /root/buildinfo/content_manifests/content-sets.json      
# Mon, 17 Nov 2025 07:03:32 GMT
COPY file:040b4789124c20d56e0f81f37d756e271408963b29b2b4b1e2a7e2c073e4ad50 in /usr/share/buildinfo/labels.json      
# Mon, 17 Nov 2025 07:03:32 GMT
COPY file:040b4789124c20d56e0f81f37d756e271408963b29b2b4b1e2a7e2c073e4ad50 in /root/buildinfo/labels.json      
# Mon, 17 Nov 2025 07:03:33 GMT
LABEL "architecture"="ppc64le" "vcs-type"="git" "vcs-ref"="f3ce7416a648177fb2c54fd1c28cc0dab0304a68" "org.opencontainers.image.revision"="f3ce7416a648177fb2c54fd1c28cc0dab0304a68" "build-date"="2025-11-17T07:03:20Z" "release"="1763362715"org.opencontainers.image.revision=f3ce7416a648177fb2c54fd1c28cc0dab0304a68
# Mon, 17 Nov 2025 23:14:49 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 17 Nov 2025 23:14:49 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 17 Nov 2025 23:14:49 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 17 Nov 2025 23:14:49 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en         gnupg2     ;     microdnf clean all # buildkit
# Mon, 17 Nov 2025 23:14:49 GMT
ENV JAVA_VERSION=jdk8u472-b08
# Mon, 17 Nov 2025 23:19:00 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='c043807ad995fb3987bc1c42b16ebf0f1b5010868c3e9d20a941236d5bbb22b7';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u472-b08/OpenJDK8U-jre_aarch64_linux_hotspot_8u472b08.tar.gz';          ;;        ppc64le)          ESUM='a76eb0f46cd5134b0b8b52ef4dd54ac7fd7e5960fc7dce8772bfc455a5e83e40';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u472-b08/OpenJDK8U-jre_ppc64le_linux_hotspot_8u472b08.tar.gz';          ;;        x86_64)          ESUM='6f7fb5fd640a0fd00837344b0920cbc4b9b9284b50e66f33789e3b250446a16e';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u472-b08/OpenJDK8U-jre_x64_linux_hotspot_8u472b08.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz; # buildkit
# Mon, 17 Nov 2025 23:19:02 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java -version"; java -version;     echo "Complete." # buildkit
# Mon, 17 Nov 2025 23:19:03 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Mon, 17 Nov 2025 23:19:03 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
```

-	Layers:
	-	`sha256:6e24e81139d30a463716e63229e1184a2b4250bb139ff88e3682c9e552661b81`  
		Last Modified: Mon, 17 Nov 2025 12:13:13 GMT  
		Size: 38.7 MB (38721761 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:106e259b55af997c3f2efc1cf8633c914cd06061615b03cbef4967d4541d920a`  
		Last Modified: Mon, 17 Nov 2025 23:16:28 GMT  
		Size: 57.4 MB (57353400 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ace61fd33c2d28395f2f46c4023c12fe0b230ea53d9ada1211cd808b72c06ad`  
		Last Modified: Mon, 17 Nov 2025 23:19:51 GMT  
		Size: 41.3 MB (41268883 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3769566cbddaaab495b2d28844a077012058eff11ae307ee64546fa26d592000`  
		Last Modified: Mon, 17 Nov 2025 23:19:47 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0605a6c3c2cd56814e98bf02db8c363af0f0e4352bbda9cdb86927f6b24ad6d5`  
		Last Modified: Mon, 17 Nov 2025 23:19:48 GMT  
		Size: 2.3 KB (2290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:8u472-b08-jre-ubi10-minimal` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:e3836a7b4517ff8b7a89ffa818eec2d55fc2bf6388b61e0165d8616ab88bf562
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5635426 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd528430fa0df3035b07232cec431b8d91129cf370e4d385e06d05065c9db956`

```dockerfile
```

-	Layers:
	-	`sha256:e73e99d1869d6e96000a80d05e3f1e28a95f0ab8e12b672d5afa893d87099e02`  
		Last Modified: Tue, 18 Nov 2025 01:20:04 GMT  
		Size: 5.6 MB (5615885 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:40ff92282996f662745cc395fb6eb85ea1ab5da600fa96e774c4cd81fcf2ac50`  
		Last Modified: Tue, 18 Nov 2025 01:20:05 GMT  
		Size: 19.5 KB (19541 bytes)  
		MIME: application/vnd.in-toto+json
