## `eclipse-temurin:8u472-b08-jre-ubi9-minimal`

```console
$ docker pull eclipse-temurin@sha256:da6fa8afa8e85b75e5c638e7e4dae34e078f81e894913138020cb7e388fcf418
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `eclipse-temurin:8u472-b08-jre-ubi9-minimal` - linux; amd64

```console
$ docker pull eclipse-temurin@sha256:f6df9ce5490c5cc223487b6ccf1ba43656acf4c7e0fdf6f7ea24becea825cc02
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **112.3 MB (112337524 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f849ad5290e63de79c8f54bad78d69946bbf0d8bfe8ce15fbabab9ee875fb16a`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`

```dockerfile
# Mon, 01 Dec 2025 08:46:04 GMT
LABEL maintainer="Red Hat, Inc."
# Mon, 01 Dec 2025 08:46:04 GMT
LABEL vendor="Red Hat, Inc."
# Mon, 01 Dec 2025 08:46:04 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Mon, 01 Dec 2025 08:46:04 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.7"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Mon, 01 Dec 2025 08:46:04 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Mon, 01 Dec 2025 08:46:04 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Mon, 01 Dec 2025 08:46:04 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 01 Dec 2025 08:46:04 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 01 Dec 2025 08:46:04 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Mon, 01 Dec 2025 08:46:04 GMT
LABEL io.openshift.expose-services=""
# Mon, 01 Dec 2025 08:46:04 GMT
LABEL io.openshift.tags="minimal rhel9"
# Mon, 01 Dec 2025 08:46:04 GMT
ENV container oci
# Mon, 01 Dec 2025 08:46:05 GMT
COPY dir:9e1be6ea7c9ab655dce87115dc5a86f74430f6cce27de363947899ca9c40a12b in /      
# Mon, 01 Dec 2025 08:46:05 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Mon, 01 Dec 2025 08:46:05 GMT
CMD ["/bin/bash"]
# Mon, 01 Dec 2025 08:46:05 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /usr/share/buildinfo/content-sets.json      
# Mon, 01 Dec 2025 08:46:05 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /root/buildinfo/content_manifests/content-sets.json      
# Mon, 01 Dec 2025 08:46:05 GMT
COPY file:b2d99215ad0f777fc208a0abcf88392b89d81310198466ef08702f0413990c72 in /usr/share/buildinfo/labels.json      
# Mon, 01 Dec 2025 08:46:06 GMT
COPY file:b2d99215ad0f777fc208a0abcf88392b89d81310198466ef08702f0413990c72 in /root/buildinfo/labels.json      
# Mon, 01 Dec 2025 08:46:06 GMT
LABEL "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="aa778ff26f397863d5f50a6cf5f17a2343e5a626" "org.opencontainers.image.revision"="aa778ff26f397863d5f50a6cf5f17a2343e5a626" "build-date"="2025-12-01T08:45:48Z" "org.opencontainers.image.created"="2025-12-01T08:45:48Z" "release"="1764578379"org.opencontainers.image.revision=aa778ff26f397863d5f50a6cf5f17a2343e5a626,org.opencontainers.image.created=2025-12-01T08:45:48Z
# Tue, 02 Dec 2025 00:37:52 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 02 Dec 2025 00:37:52 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Dec 2025 00:37:52 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 02 Dec 2025 00:37:52 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en     ;     microdnf clean all # buildkit
# Tue, 02 Dec 2025 00:37:52 GMT
ENV JAVA_VERSION=jdk8u472-b08
# Tue, 02 Dec 2025 00:38:20 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='c043807ad995fb3987bc1c42b16ebf0f1b5010868c3e9d20a941236d5bbb22b7';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u472-b08/OpenJDK8U-jre_aarch64_linux_hotspot_8u472b08.tar.gz';          ;;        ppc64le)          ESUM='a76eb0f46cd5134b0b8b52ef4dd54ac7fd7e5960fc7dce8772bfc455a5e83e40';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u472-b08/OpenJDK8U-jre_ppc64le_linux_hotspot_8u472b08.tar.gz';          ;;        x86_64)          ESUM='6f7fb5fd640a0fd00837344b0920cbc4b9b9284b50e66f33789e3b250446a16e';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u472-b08/OpenJDK8U-jre_x64_linux_hotspot_8u472b08.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz; # buildkit
# Tue, 02 Dec 2025 00:38:20 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java -version"; java -version;     echo "Complete." # buildkit
# Tue, 02 Dec 2025 00:38:20 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 02 Dec 2025 00:38:20 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
```

-	Layers:
	-	`sha256:e33884b9ee6fd9f34b4688c1f3f27e3a36be1a8633a805f0780dcfa23073efcb`  
		Last Modified: Mon, 01 Dec 2025 09:26:00 GMT  
		Size: 40.0 MB (40040081 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7684bd6ea6b6d7232aa145adc30f5e6adb974b545e91d61990706b3096865481`  
		Last Modified: Tue, 02 Dec 2025 00:38:37 GMT  
		Size: 30.4 MB (30407377 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f87654c89fc8832425499666f7ce9b029706e2177a9997431d8404b8a28fd482`  
		Last Modified: Tue, 02 Dec 2025 00:38:56 GMT  
		Size: 41.9 MB (41887647 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a431a86c5032f5d2a1f5817532507ec9f3cc18ca0feaf785b14a08cb85f61fc`  
		Last Modified: Tue, 02 Dec 2025 00:38:50 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce481bcadc67f149996bfbf97b544c8f839c22eb2e0ef60da72d2a541eb6a054`  
		Last Modified: Tue, 02 Dec 2025 00:38:50 GMT  
		Size: 2.3 KB (2291 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:8u472-b08-jre-ubi9-minimal` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:2f57a41ed69e2d3429ce7d82a3432be08413f85daecbd8e69d0df7ee6c361809
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2463783 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d116883849e36eed23740ac2f40716bf1fb28e6b816cad2fd5e86e092f1eef2`

```dockerfile
```

-	Layers:
	-	`sha256:e41ac23dc20847b221dcef09f6edf64e84e30f617fa182fe29305bb28d84b61f`  
		Last Modified: Tue, 02 Dec 2025 01:18:41 GMT  
		Size: 2.4 MB (2444436 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fcd85ca1842a8c86ddf747b26b1f8de22eba5f8da83e2738452a9bc04a0d6c89`  
		Last Modified: Tue, 02 Dec 2025 01:18:42 GMT  
		Size: 19.3 KB (19347 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-temurin:8u472-b08-jre-ubi9-minimal` - linux; arm64 variant v8

```console
$ docker pull eclipse-temurin@sha256:77cf126e88bf0761bbdac45c4e2d1d052a1d4a87ccc46fad2609323679cab819
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **110.0 MB (109957591 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:53f8760cfced7adf3b0ce39441b62cfdf6e47acc7d1580e9f06fcf9b40b13c72`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`

```dockerfile
# Mon, 01 Dec 2025 08:45:36 GMT
LABEL maintainer="Red Hat, Inc."
# Mon, 01 Dec 2025 08:45:36 GMT
LABEL vendor="Red Hat, Inc."
# Mon, 01 Dec 2025 08:45:36 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Mon, 01 Dec 2025 08:45:36 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.7"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Mon, 01 Dec 2025 08:45:36 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Mon, 01 Dec 2025 08:45:36 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Mon, 01 Dec 2025 08:45:36 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 01 Dec 2025 08:45:36 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 01 Dec 2025 08:45:36 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Mon, 01 Dec 2025 08:45:36 GMT
LABEL io.openshift.expose-services=""
# Mon, 01 Dec 2025 08:45:36 GMT
LABEL io.openshift.tags="minimal rhel9"
# Mon, 01 Dec 2025 08:45:36 GMT
ENV container oci
# Mon, 01 Dec 2025 08:45:37 GMT
COPY dir:0300512c6394db4e597803fcc03b9993a2a4c4d9c6e4eb31c5a64534316ae291 in /      
# Mon, 01 Dec 2025 08:45:37 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Mon, 01 Dec 2025 08:45:37 GMT
CMD ["/bin/bash"]
# Mon, 01 Dec 2025 08:45:37 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /usr/share/buildinfo/content-sets.json      
# Mon, 01 Dec 2025 08:45:37 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /root/buildinfo/content_manifests/content-sets.json      
# Mon, 01 Dec 2025 08:45:37 GMT
COPY file:9ba4e215cc648b0ee2f7a9114145896fc716da8ab330689b6c8358fccff02c52 in /usr/share/buildinfo/labels.json      
# Mon, 01 Dec 2025 08:45:37 GMT
COPY file:9ba4e215cc648b0ee2f7a9114145896fc716da8ab330689b6c8358fccff02c52 in /root/buildinfo/labels.json      
# Mon, 01 Dec 2025 08:45:38 GMT
LABEL "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="aa778ff26f397863d5f50a6cf5f17a2343e5a626" "org.opencontainers.image.revision"="aa778ff26f397863d5f50a6cf5f17a2343e5a626" "build-date"="2025-12-01T08:45:20Z" "org.opencontainers.image.created"="2025-12-01T08:45:20Z" "release"="1764578379"org.opencontainers.image.revision=aa778ff26f397863d5f50a6cf5f17a2343e5a626,org.opencontainers.image.created=2025-12-01T08:45:20Z
# Tue, 02 Dec 2025 00:43:28 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 02 Dec 2025 00:43:28 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Dec 2025 00:43:28 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 02 Dec 2025 00:43:28 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en     ;     microdnf clean all # buildkit
# Tue, 02 Dec 2025 00:43:28 GMT
ENV JAVA_VERSION=jdk8u472-b08
# Tue, 02 Dec 2025 00:44:29 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='c043807ad995fb3987bc1c42b16ebf0f1b5010868c3e9d20a941236d5bbb22b7';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u472-b08/OpenJDK8U-jre_aarch64_linux_hotspot_8u472b08.tar.gz';          ;;        ppc64le)          ESUM='a76eb0f46cd5134b0b8b52ef4dd54ac7fd7e5960fc7dce8772bfc455a5e83e40';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u472-b08/OpenJDK8U-jre_ppc64le_linux_hotspot_8u472b08.tar.gz';          ;;        x86_64)          ESUM='6f7fb5fd640a0fd00837344b0920cbc4b9b9284b50e66f33789e3b250446a16e';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u472-b08/OpenJDK8U-jre_x64_linux_hotspot_8u472b08.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz; # buildkit
# Tue, 02 Dec 2025 00:44:29 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java -version"; java -version;     echo "Complete." # buildkit
# Tue, 02 Dec 2025 00:44:29 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 02 Dec 2025 00:44:29 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
```

-	Layers:
	-	`sha256:2318060655d9ba0a61831256291e1482c38f67e2e0879a90ccd9008c0ed03b36`  
		Last Modified: Mon, 01 Dec 2025 12:11:26 GMT  
		Size: 38.2 MB (38221706 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0fd4ef6da9f9ae1a10f689ed0d4112554c216caf370d452faa417f248e8e211`  
		Last Modified: Tue, 02 Dec 2025 00:43:56 GMT  
		Size: 30.9 MB (30853297 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3af06a62aec539fe23b0a49aae3cb30e0377d000f35e418ade7a9f0fdb21609d`  
		Last Modified: Tue, 02 Dec 2025 00:44:51 GMT  
		Size: 40.9 MB (40880171 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68f635907abbb71d1c780f36daf7c511882873af9ac0c2cb4cd38317d5c8caa6`  
		Last Modified: Tue, 02 Dec 2025 00:44:46 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8dfa1ae74edec06f4ad2917840bc276b38dc5157d28bceaf87904e26ec05cd03`  
		Last Modified: Tue, 02 Dec 2025 00:44:46 GMT  
		Size: 2.3 KB (2290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:8u472-b08-jre-ubi9-minimal` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:8913629f3898bc8067f47f739b59863c434b24db8e3122650a065e55d0e74b92
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2463935 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ba4483eb148b26f7354d0664799218f0484d6685a9f7e004965e32d55e3d0c8`

```dockerfile
```

-	Layers:
	-	`sha256:f40d005adf224c1a97107311663c11b004c5acad52acb1af35da2002d3866134`  
		Last Modified: Tue, 02 Dec 2025 01:18:46 GMT  
		Size: 2.4 MB (2444484 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7a2e6b98c11c6961e4579d787f0a1ea7fdd568a68d8ed8b403eb5f23efa8294e`  
		Last Modified: Tue, 02 Dec 2025 01:18:47 GMT  
		Size: 19.5 KB (19451 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-temurin:8u472-b08-jre-ubi9-minimal` - linux; ppc64le

```console
$ docker pull eclipse-temurin@sha256:328a9f5dd2ff2104f22cd86807da6a942e1d42d1f27fea83e6c84c0fdc8df647
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.8 MB (115826711 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d94140aed41c767936f25022b8801475ceb53d61c8eebdb44fd7be9c7e3c92d`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`

```dockerfile
# Mon, 17 Nov 2025 06:52:34 GMT
LABEL maintainer="Red Hat, Inc."
# Mon, 17 Nov 2025 06:52:34 GMT
LABEL vendor="Red Hat, Inc."
# Mon, 17 Nov 2025 06:52:34 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Mon, 17 Nov 2025 06:52:34 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.7"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Mon, 17 Nov 2025 06:52:34 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Mon, 17 Nov 2025 06:52:34 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Mon, 17 Nov 2025 06:52:34 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 17 Nov 2025 06:52:34 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 17 Nov 2025 06:52:34 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Mon, 17 Nov 2025 06:52:34 GMT
LABEL io.openshift.expose-services=""
# Mon, 17 Nov 2025 06:52:34 GMT
LABEL io.openshift.tags="minimal rhel9"
# Mon, 17 Nov 2025 06:52:34 GMT
ENV container oci
# Mon, 17 Nov 2025 06:52:35 GMT
COPY dir:9a9add289f1055504c42bfa45e0dd9890598235dacbc2320fb6adf8f7795427f in /      
# Mon, 17 Nov 2025 06:52:35 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Mon, 17 Nov 2025 06:52:35 GMT
CMD ["/bin/bash"]
# Mon, 17 Nov 2025 06:52:35 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /usr/share/buildinfo/content-sets.json      
# Mon, 17 Nov 2025 06:52:35 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /root/buildinfo/content_manifests/content-sets.json      
# Mon, 17 Nov 2025 06:52:35 GMT
COPY file:df039a12e94c358b58fd977c386a5daf1a5d5ee9447df76db2fd5246917af6b7 in /usr/share/buildinfo/labels.json      
# Mon, 17 Nov 2025 06:52:35 GMT
COPY file:df039a12e94c358b58fd977c386a5daf1a5d5ee9447df76db2fd5246917af6b7 in /root/buildinfo/labels.json      
# Mon, 17 Nov 2025 06:52:36 GMT
LABEL "architecture"="ppc64le" "vcs-type"="git" "vcs-ref"="f7f5876a3d86ded473c14b11d7491c2b6ddf39ce" "org.opencontainers.image.revision"="f7f5876a3d86ded473c14b11d7491c2b6ddf39ce" "build-date"="2025-11-17T06:52:24Z" "release"="1763362218"org.opencontainers.image.revision=f7f5876a3d86ded473c14b11d7491c2b6ddf39ce
# Mon, 17 Nov 2025 23:18:50 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 17 Nov 2025 23:18:50 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 17 Nov 2025 23:18:50 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 17 Nov 2025 23:18:50 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en     ;     microdnf clean all # buildkit
# Mon, 17 Nov 2025 23:18:50 GMT
ENV JAVA_VERSION=jdk8u472-b08
# Mon, 17 Nov 2025 23:20:52 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='c043807ad995fb3987bc1c42b16ebf0f1b5010868c3e9d20a941236d5bbb22b7';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u472-b08/OpenJDK8U-jre_aarch64_linux_hotspot_8u472b08.tar.gz';          ;;        ppc64le)          ESUM='a76eb0f46cd5134b0b8b52ef4dd54ac7fd7e5960fc7dce8772bfc455a5e83e40';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u472-b08/OpenJDK8U-jre_ppc64le_linux_hotspot_8u472b08.tar.gz';          ;;        x86_64)          ESUM='6f7fb5fd640a0fd00837344b0920cbc4b9b9284b50e66f33789e3b250446a16e';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u472-b08/OpenJDK8U-jre_x64_linux_hotspot_8u472b08.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz; # buildkit
# Mon, 17 Nov 2025 23:20:57 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java -version"; java -version;     echo "Complete." # buildkit
# Mon, 17 Nov 2025 23:21:00 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Mon, 17 Nov 2025 23:21:00 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
```

-	Layers:
	-	`sha256:6fccaa32330f08c5e0cbe4fb16bd3e3944f9e113abfe46581e3f895ddfc1db49`  
		Last Modified: Mon, 17 Nov 2025 12:10:03 GMT  
		Size: 44.4 MB (44431008 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79ae5c71fee127db36920f76d71bcf3210a5ea9baf4a783f6ef553746a98cae7`  
		Last Modified: Mon, 17 Nov 2025 23:19:50 GMT  
		Size: 30.1 MB (30124462 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e1796eb9fe4c2f4fcec595ad316c9ab9736637f08eaac109b5b15e61b064cec`  
		Last Modified: Mon, 17 Nov 2025 23:21:46 GMT  
		Size: 41.3 MB (41268822 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e4077ce533e2ccf3a99e3d7a9012960aed66228211ac1c0c397dc3e846a3bed`  
		Last Modified: Mon, 17 Nov 2025 23:21:43 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87b714877c4f78ef20b624172fcf2cc98a3fef3fe1fe81496a32ac6c9bcc9c92`  
		Last Modified: Mon, 17 Nov 2025 23:21:43 GMT  
		Size: 2.3 KB (2291 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:8u472-b08-jre-ubi9-minimal` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:eedc15228129d29ea9d42a76c907e11d754835d85f0e71fc44bb6e662335c42f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2455197 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f94665e5a3433b39a617b661269bf37ba388419c733658e1def645693cad9008`

```dockerfile
```

-	Layers:
	-	`sha256:68bbb624bddd6714bbb8c4a04cdd01bbe424803dde84d8d76e25c012b04884cf`  
		Last Modified: Tue, 18 Nov 2025 01:20:12 GMT  
		Size: 2.4 MB (2435820 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7375d6e4a434d0560a7db1be14d3115171d714a6704c5fa7fcf676bff4e04596`  
		Last Modified: Tue, 18 Nov 2025 01:20:13 GMT  
		Size: 19.4 KB (19377 bytes)  
		MIME: application/vnd.in-toto+json
