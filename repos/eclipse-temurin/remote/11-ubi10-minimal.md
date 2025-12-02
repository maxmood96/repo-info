## `eclipse-temurin:11-ubi10-minimal`

```console
$ docker pull eclipse-temurin@sha256:e53d12ac13c7fcc4011116d948e96bd7bda50ae26f52bc020b1b76d2e7a97d17
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
$ docker pull eclipse-temurin@sha256:5779293b2ac4a2043773d9e202b3a6de4da06e3e05947116a7059cccb39ea393
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **231.4 MB (231389853 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f65802659594e824e701b2de020107cfd8228b2d8f6127ad632ef5e48b60ddad`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["jshell"]`

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
ENV JAVA_VERSION=jdk-11.0.29+7
# Tue, 02 Dec 2025 00:38:42 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='71e00cd0ab4371a4e9d67d1a2ca3e8ed2f126dff6a6ab152a6ecdec60100fbdd';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.29%2B7/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.29_7.tar.gz';          ;;        ppc64le)          ESUM='d6136c0baafd588ba4f9be9f81285052f03b5366868e98fcd38fa5fb43c9121d';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.29%2B7/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.29_7.tar.gz';          ;;        s390x)          ESUM='12a494209c04a4cacee1615708b6856a770391d2588251a9a36e767ca4a07ac4';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.29%2B7/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.29_7.tar.gz';          ;;        x86_64)          ESUM='3c8f2b53dd137cd86e54f40df96fd0fc56df72c749c06469e7eab216503bc7cf';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.29%2B7/OpenJDK11U-jdk_x64_linux_hotspot_11.0.29_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Tue, 02 Dec 2025 00:38:43 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 02 Dec 2025 00:38:43 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 02 Dec 2025 00:38:43 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 02 Dec 2025 00:38:43 GMT
CMD ["jshell"]
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
	-	`sha256:6ff019032321d950198cfd6ee2328edc4d35f223d932e64c299f87ca964f591d`  
		Last Modified: Tue, 02 Dec 2025 00:39:03 GMT  
		Size: 141.4 MB (141425250 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5cfe3f788bab82654e67b14d5205048f81574ab1346a3400d85102b1cac4c529`  
		Last Modified: Tue, 02 Dec 2025 01:05:49 GMT  
		Size: 130.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b44839cef70098258a67a71fcc5650998f1c3fcf29f1db3e45e8e48c6af6daf`  
		Last Modified: Tue, 02 Dec 2025 01:05:53 GMT  
		Size: 2.3 KB (2292 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:11-ubi10-minimal` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:9c7027e53e2ad0534fbf4a3fdbeaa29187f2c3a2613412daa3e2626676a4df1c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5721334 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b128f1bb6149feb45a35d361cbd55282133d3f298817b2dd75c0943d4542430`

```dockerfile
```

-	Layers:
	-	`sha256:3d104ce5104075d56a521a6852a66f4d6b5214298b53683104d7d85c4041bf2f`  
		Last Modified: Tue, 02 Dec 2025 01:13:01 GMT  
		Size: 5.7 MB (5700018 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8d00ccdc1a9c4f57f26fae81d8e829faaed1a977e15633745cbcca6f535035c7`  
		Last Modified: Tue, 02 Dec 2025 01:13:02 GMT  
		Size: 21.3 KB (21316 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-temurin:11-ubi10-minimal` - linux; arm64 variant v8

```console
$ docker pull eclipse-temurin@sha256:b107bf4b4ef41389c46109b3ff8a4fc63627ff8b5137c0ed24bbd6325fe78bf9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **225.9 MB (225933305 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:51208e4fca93a711a0f85470ff5d534e5e5a3315b4b9259f8c0676fac609fbc7`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["jshell"]`

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
ENV JAVA_VERSION=jdk-11.0.29+7
# Tue, 02 Dec 2025 00:45:01 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='71e00cd0ab4371a4e9d67d1a2ca3e8ed2f126dff6a6ab152a6ecdec60100fbdd';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.29%2B7/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.29_7.tar.gz';          ;;        ppc64le)          ESUM='d6136c0baafd588ba4f9be9f81285052f03b5366868e98fcd38fa5fb43c9121d';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.29%2B7/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.29_7.tar.gz';          ;;        s390x)          ESUM='12a494209c04a4cacee1615708b6856a770391d2588251a9a36e767ca4a07ac4';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.29%2B7/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.29_7.tar.gz';          ;;        x86_64)          ESUM='3c8f2b53dd137cd86e54f40df96fd0fc56df72c749c06469e7eab216503bc7cf';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.29%2B7/OpenJDK11U-jdk_x64_linux_hotspot_11.0.29_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Tue, 02 Dec 2025 00:45:02 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 02 Dec 2025 00:45:02 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 02 Dec 2025 00:45:02 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 02 Dec 2025 00:45:02 GMT
CMD ["jshell"]
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
	-	`sha256:e9f9e11d2fdf7996e7037de67b44e89b36896c71bd9528192827ff6a261e55dc`  
		Last Modified: Tue, 02 Dec 2025 00:45:23 GMT  
		Size: 138.2 MB (138190281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6257a05820d7673d4c06bff1d4c78d27ccabb320e6ce0fb0076d3f41efdf4e1`  
		Last Modified: Tue, 02 Dec 2025 00:45:32 GMT  
		Size: 130.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0881e9bbbe5339ecfaf4f2f89a967e639ee8aa92f32dc097b7c1f1ac864dddbd`  
		Last Modified: Tue, 02 Dec 2025 00:45:33 GMT  
		Size: 2.3 KB (2291 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:11-ubi10-minimal` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:47b3ea7b03cb1cd03b056834dd74ab52b33706afcb86f726ec65a21e215e53cc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5721558 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cac8694930c9d308d8ea7caa57db7218e533cec0f64269c6b842d1c341c8ed0b`

```dockerfile
```

-	Layers:
	-	`sha256:f0a398c2e9540ac7f36b29e72c565b8a075e83fd4c7fc7ab04215f0dba9fe09a`  
		Last Modified: Tue, 02 Dec 2025 01:13:08 GMT  
		Size: 5.7 MB (5700126 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0c082371ff961aba3d0879f7a60044f814060eb4b49b7a32f8e237d4b9b29a2a`  
		Last Modified: Tue, 02 Dec 2025 01:13:09 GMT  
		Size: 21.4 KB (21432 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-temurin:11-ubi10-minimal` - linux; ppc64le

```console
$ docker pull eclipse-temurin@sha256:922e8457f20c0145610ce55f33efff663815bad9e975bf88a55b99fcbef5b457
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **224.7 MB (224661903 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a99131c1bbabe7495fe0abd93d843cec5a9dcb7eeaa4eb7908595f40115d9e6`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["jshell"]`

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
ENV JAVA_VERSION=jdk-11.0.29+7
# Mon, 17 Nov 2025 23:20:57 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='71e00cd0ab4371a4e9d67d1a2ca3e8ed2f126dff6a6ab152a6ecdec60100fbdd';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.29%2B7/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.29_7.tar.gz';          ;;        ppc64le)          ESUM='d6136c0baafd588ba4f9be9f81285052f03b5366868e98fcd38fa5fb43c9121d';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.29%2B7/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.29_7.tar.gz';          ;;        s390x)          ESUM='12a494209c04a4cacee1615708b6856a770391d2588251a9a36e767ca4a07ac4';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.29%2B7/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.29_7.tar.gz';          ;;        x86_64)          ESUM='3c8f2b53dd137cd86e54f40df96fd0fc56df72c749c06469e7eab216503bc7cf';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.29%2B7/OpenJDK11U-jdk_x64_linux_hotspot_11.0.29_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Mon, 17 Nov 2025 23:21:03 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Mon, 17 Nov 2025 23:21:05 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Mon, 17 Nov 2025 23:21:05 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Mon, 17 Nov 2025 23:21:05 GMT
CMD ["jshell"]
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
	-	`sha256:64151cc1590f5ac9e50c70005e8c90283133c0b1dc0726c2aa061d4c52a47098`  
		Last Modified: Tue, 18 Nov 2025 09:19:09 GMT  
		Size: 128.6 MB (128584322 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9261e78cdf7bb5ce224c7f6010b2ea14adc3971e759025902e3b531c4cf80c7c`  
		Last Modified: Mon, 17 Nov 2025 23:22:03 GMT  
		Size: 130.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2ca3344e9c4ae4bb15c30ce3e3bea25ad2124761b10a2ff1aa8307bc1540794`  
		Last Modified: Mon, 17 Nov 2025 23:22:03 GMT  
		Size: 2.3 KB (2290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:11-ubi10-minimal` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:0b8c0c341366f8c20a755f0117194485701cc2d44138cf529e6186ab94b2a7b1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5707907 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8eb74907c5e0b193d08f4b6344cd22e1616925b591cafd858b223dfd1475d4b0`

```dockerfile
```

-	Layers:
	-	`sha256:23f281a35bccdd66a3bc2b0e0f6a57abc1bc7ca5ca52662453226b98efad4dc6`  
		Last Modified: Tue, 18 Nov 2025 01:13:43 GMT  
		Size: 5.7 MB (5686555 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:655226150d69c738174faa59353e175825410cd5faa36d5634ee5185f69a2698`  
		Last Modified: Tue, 18 Nov 2025 01:13:44 GMT  
		Size: 21.4 KB (21352 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-temurin:11-ubi10-minimal` - linux; s390x

```console
$ docker pull eclipse-temurin@sha256:7c230abe02bb7c821b51f812131fada7064d12e5bb53b647fcf00a222eb83908
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **212.4 MB (212416224 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2157c573a8e64e06c44e715c8bea5af9f28eb172025b12ac4cab23f5d4175f5b`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 01 Dec 2025 16:13:45 GMT
LABEL maintainer="Red Hat, Inc."
# Mon, 01 Dec 2025 16:13:45 GMT
LABEL vendor="Red Hat, Inc."
# Mon, 01 Dec 2025 16:13:45 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Mon, 01 Dec 2025 16:13:45 GMT
LABEL com.redhat.component="ubi10-minimal-container"       name="ubi10/ubi-minimal"       version="10.1"       cpe="cpe:/o:redhat:enterprise_linux:10.1"       distribution-scope="public"
# Mon, 01 Dec 2025 16:13:45 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Mon, 01 Dec 2025 16:13:45 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 10."
# Mon, 01 Dec 2025 16:13:45 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 01 Dec 2025 16:13:45 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 01 Dec 2025 16:13:45 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 10 Minimal"
# Mon, 01 Dec 2025 16:13:45 GMT
LABEL io.openshift.expose-services=""
# Mon, 01 Dec 2025 16:13:45 GMT
LABEL io.openshift.tags="minimal rhel10"
# Mon, 01 Dec 2025 16:13:45 GMT
ENV container oci
# Mon, 01 Dec 2025 16:13:46 GMT
COPY dir:ee1f1fb58b73712e067b524f29b07cf434abeebd65fa952bf194a31a9e96dd28 in /      
# Mon, 01 Dec 2025 16:13:46 GMT
COPY file:5de33b5fc08b00635bccf9134a18978dba13e2250aa51838f9969515a3957847 in /etc/yum.repos.d/.      
# Mon, 01 Dec 2025 16:13:46 GMT
CMD ["/bin/bash"]
# Mon, 01 Dec 2025 16:13:46 GMT
COPY file:595171150af68abc798ea385f7988d74b566aa8e84babff137f00b08b2164683 in /usr/share/buildinfo/content-sets.json      
# Mon, 01 Dec 2025 16:13:46 GMT
COPY file:595171150af68abc798ea385f7988d74b566aa8e84babff137f00b08b2164683 in /root/buildinfo/content_manifests/content-sets.json      
# Mon, 01 Dec 2025 16:13:46 GMT
COPY file:178efaed95a9f3c67a11443e55f39f4bf9d142ac34782d99fc4d745647dcdc7b in /usr/share/buildinfo/labels.json      
# Mon, 01 Dec 2025 16:13:46 GMT
COPY file:178efaed95a9f3c67a11443e55f39f4bf9d142ac34782d99fc4d745647dcdc7b in /root/buildinfo/labels.json      
# Mon, 01 Dec 2025 16:13:46 GMT
LABEL "architecture"="s390x" "vcs-type"="git" "vcs-ref"="f3ce7416a648177fb2c54fd1c28cc0dab0304a68" "org.opencontainers.image.revision"="f3ce7416a648177fb2c54fd1c28cc0dab0304a68" "build-date"="2025-12-01T16:11:22Z" "org.opencontainers.image.created"="2025-12-01T16:11:22Z" "release"="1764604111"org.opencontainers.image.revision=f3ce7416a648177fb2c54fd1c28cc0dab0304a68,org.opencontainers.image.created=2025-12-01T16:11:22Z
# Tue, 02 Dec 2025 00:33:30 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 02 Dec 2025 00:33:30 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Dec 2025 00:33:30 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 02 Dec 2025 00:33:30 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en         gnupg2     ;     microdnf clean all # buildkit
# Tue, 02 Dec 2025 00:33:30 GMT
ENV JAVA_VERSION=jdk-11.0.29+7
# Tue, 02 Dec 2025 00:33:38 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='71e00cd0ab4371a4e9d67d1a2ca3e8ed2f126dff6a6ab152a6ecdec60100fbdd';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.29%2B7/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.29_7.tar.gz';          ;;        ppc64le)          ESUM='d6136c0baafd588ba4f9be9f81285052f03b5366868e98fcd38fa5fb43c9121d';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.29%2B7/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.29_7.tar.gz';          ;;        s390x)          ESUM='12a494209c04a4cacee1615708b6856a770391d2588251a9a36e767ca4a07ac4';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.29%2B7/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.29_7.tar.gz';          ;;        x86_64)          ESUM='3c8f2b53dd137cd86e54f40df96fd0fc56df72c749c06469e7eab216503bc7cf';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.29%2B7/OpenJDK11U-jdk_x64_linux_hotspot_11.0.29_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Tue, 02 Dec 2025 00:33:41 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 02 Dec 2025 00:33:42 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 02 Dec 2025 00:33:42 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 02 Dec 2025 00:33:42 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:4c2d3b17031accf5277814f24c5959875fea29c3417bd21d9ab38a4021f9b098`  
		Last Modified: Mon, 01 Dec 2025 18:12:30 GMT  
		Size: 34.4 MB (34366787 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34d6f29237cb9bac260bb875e3ab78f2c39de4f6195073d574380d496293d5d9`  
		Last Modified: Tue, 02 Dec 2025 00:34:52 GMT  
		Size: 55.9 MB (55943138 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d7968fa818c2dd752d347ec0406df57c39a0cc9afcdd531e3a5551498e7b2f7`  
		Last Modified: Tue, 02 Dec 2025 00:35:01 GMT  
		Size: 122.1 MB (122103881 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:281e447ea7bde74601f8415c5ebb2f98d0ded187341c094a8e4398ef3cc98972`  
		Last Modified: Tue, 02 Dec 2025 00:34:46 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18ac05011ff37b8f986af5e63104fe535dbb3463951b2871ea44577e8a7d9ad2`  
		Last Modified: Tue, 02 Dec 2025 00:34:45 GMT  
		Size: 2.3 KB (2290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:11-ubi10-minimal` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:51d0072222db7fc94ba8a4159bb83d7da438317cb42935145895c4138dc521f5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5706864 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:da1af24ba64ae28a277a99b9f822df9578665ddc4b7c2dba848505f5b5890157`

```dockerfile
```

-	Layers:
	-	`sha256:4645a237dd923dddc329904043d4e0de9c3bdf41d20eecf64c2bb8845e1a1991`  
		Last Modified: Tue, 02 Dec 2025 01:13:19 GMT  
		Size: 5.7 MB (5685548 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2b8baa68eb4135224180db178a20d972c845b46bcff214371c4523074041f83f`  
		Last Modified: Tue, 02 Dec 2025 01:13:20 GMT  
		Size: 21.3 KB (21316 bytes)  
		MIME: application/vnd.in-toto+json
