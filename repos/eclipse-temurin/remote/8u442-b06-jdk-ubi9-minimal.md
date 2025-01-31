## `eclipse-temurin:8u442-b06-jdk-ubi9-minimal`

```console
$ docker pull eclipse-temurin@sha256:ef0599cfdc12aad1ad8eeb2cc1e2a7cd6fc6fd66f4df2c6efaf1a117b061ef62
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `eclipse-temurin:8u442-b06-jdk-ubi9-minimal` - linux; amd64

```console
$ docker pull eclipse-temurin@sha256:6d09f08d5c3e8d08c906fe5ae0cb3a848578e0e6f64da00a00160ec045f13c64
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **131.1 MB (131144836 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7f07ec684e13df5d966ca6e60af1beee1ad54cc8230bf662adc9d2e2cbc43945`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`

```dockerfile
# Thu, 09 Jan 2025 06:41:15 GMT
LABEL maintainer="Red Hat, Inc."
# Thu, 09 Jan 2025 06:41:15 GMT
LABEL vendor="Red Hat, Inc."
# Thu, 09 Jan 2025 06:41:15 GMT
LABEL url="https://www.redhat.com"
# Thu, 09 Jan 2025 06:41:15 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.5"       distribution-scope="public"
# Thu, 09 Jan 2025 06:41:15 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Thu, 09 Jan 2025 06:41:15 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Thu, 09 Jan 2025 06:41:15 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 09 Jan 2025 06:41:15 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 09 Jan 2025 06:41:15 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Thu, 09 Jan 2025 06:41:15 GMT
LABEL io.openshift.expose-services=""
# Thu, 09 Jan 2025 06:41:15 GMT
LABEL io.openshift.tags="minimal rhel9"
# Thu, 09 Jan 2025 06:41:15 GMT
ENV container oci
# Thu, 09 Jan 2025 06:41:15 GMT
COPY dir:ca56c4399f153561fdce7628edce358895393e72057424065cc9920dd3bc2dfc in / 
# Thu, 09 Jan 2025 06:41:15 GMT
COPY file:b37d593713ee21ad52a4cd1424dc019a24f7966f85df0ac4b86d234302695328 in /etc/yum.repos.d/. 
# Thu, 09 Jan 2025 06:41:15 GMT
CMD ["/bin/bash"]
# Thu, 09 Jan 2025 06:41:16 GMT
RUN . /cachi2/cachi2.env &&     rm -rf /var/log/*
# Thu, 09 Jan 2025 06:41:16 GMT
LABEL "build-date"="2025-01-09T06:40:34" "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="98c9e4c67f5f2dfc85d12e0f1fd70b809f2a3132" "build-date"="2025-01-09T06:29:15Z" "release"="1736404155"
# Thu, 09 Jan 2025 06:41:20 GMT
RUN /bin/sh
# Thu, 30 Jan 2025 14:32:57 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 30 Jan 2025 14:32:57 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 30 Jan 2025 14:32:57 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 30 Jan 2025 14:32:57 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         fontconfig         glibc-langpack-en     ;     microdnf clean all # buildkit
# Thu, 30 Jan 2025 14:32:57 GMT
ENV JAVA_VERSION=jdk8u442-b06
# Thu, 30 Jan 2025 14:32:57 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='1d1662bd8ca7edc9281c723d9eebafea940e6a41464bdc43a83b564bc974c7e5';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u442-b06/OpenJDK8U-jdk_aarch64_linux_hotspot_8u442b06.tar.gz';          ;;        ppc64le)          ESUM='7eac77deb8fc6c6130f9445c9a68af0bcc40bf6736b5672ef5c3d737c025e84d';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u442-b06/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u442b06.tar.gz';          ;;        x86_64)          ESUM='5b0a0145e7790552a9c8767b4680074c4628ec276e5bb278b61d85cf90facafa';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u442-b06/OpenJDK8U-jdk_x64_linux_hotspot_8u442b06.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip; # buildkit
# Thu, 30 Jan 2025 14:32:57 GMT
RUN set -eux;     echo "Verifying install ...";     echo "javac -version"; javac -version;     echo "java -version"; java -version;     echo "Complete." # buildkit
# Thu, 30 Jan 2025 14:32:57 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 30 Jan 2025 14:32:57 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
```

-	Layers:
	-	`sha256:eeaa3613f51c4b5b7fcccfbff65d07d2d2db56a76e38e2e028020458a3016d3b`  
		Last Modified: Thu, 09 Jan 2025 07:47:12 GMT  
		Size: 39.4 MB (39432422 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5808a11b7bed4fb0f4e0161a315ca539c1c940faabe1402029784919a7dc4599`  
		Last Modified: Thu, 09 Jan 2025 07:47:09 GMT  
		Size: 400.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a8180e0dd376880a87ed9d46181240e115bdb97f0b3ecfd78db0e92926f2476`  
		Last Modified: Fri, 31 Jan 2025 01:30:12 GMT  
		Size: 37.0 MB (36987852 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45d84f988e146594ec8a607905dabf6924e3a12aa48906e1fc939d805bdad1fc`  
		Last Modified: Fri, 31 Jan 2025 01:30:13 GMT  
		Size: 54.7 MB (54721720 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93091cdc99f1a6a917aa5d0b9e410ec6c5b5abb127c8c74dffdef1bf5c7326ff`  
		Last Modified: Fri, 31 Jan 2025 01:30:11 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05eed7d385b8fb5b5d024d676cde1a690975ce7e6e35a08d016241e3a56cee4d`  
		Last Modified: Fri, 31 Jan 2025 01:30:11 GMT  
		Size: 2.3 KB (2315 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:8u442-b06-jdk-ubi9-minimal` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:e35d921822beff22244b2ce7bbc7dacc77d1209c2884c6d13d85e727ea745a7c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3808850 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e40f5bfcde6fb0e76af44a704b31050e2683efd5483a42de8f86e67a658683b`

```dockerfile
```

-	Layers:
	-	`sha256:4235278cc75b5653264f4db9b40d19a1ccfe5d63d9b9e5b7b689b1ea66b50c49`  
		Last Modified: Fri, 31 Jan 2025 01:30:11 GMT  
		Size: 3.8 MB (3788406 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:aa3c10590302ac3222fb6e231b0dd2978b810ba486cbd88abf4baa8375a9656b`  
		Last Modified: Fri, 31 Jan 2025 01:30:11 GMT  
		Size: 20.4 KB (20444 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-temurin:8u442-b06-jdk-ubi9-minimal` - linux; arm64 variant v8

```console
$ docker pull eclipse-temurin@sha256:da648055a9a506a13cbe843fb052dddb69131b124ed2202ad5a30227bffc9284
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **128.8 MB (128847470 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9d4b1c2a781b5d4653aff8d0b545f8798450bc27200ee660ac1bbee471bbbcce`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`

```dockerfile
# Thu, 09 Jan 2025 06:40:01 GMT
LABEL maintainer="Red Hat, Inc."
# Thu, 09 Jan 2025 06:40:01 GMT
LABEL vendor="Red Hat, Inc."
# Thu, 09 Jan 2025 06:40:01 GMT
LABEL url="https://www.redhat.com"
# Thu, 09 Jan 2025 06:40:01 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.5"       distribution-scope="public"
# Thu, 09 Jan 2025 06:40:01 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Thu, 09 Jan 2025 06:40:01 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Thu, 09 Jan 2025 06:40:01 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 09 Jan 2025 06:40:01 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 09 Jan 2025 06:40:01 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Thu, 09 Jan 2025 06:40:01 GMT
LABEL io.openshift.expose-services=""
# Thu, 09 Jan 2025 06:40:01 GMT
LABEL io.openshift.tags="minimal rhel9"
# Thu, 09 Jan 2025 06:40:01 GMT
ENV container oci
# Thu, 09 Jan 2025 06:40:02 GMT
COPY dir:a2d26ebdf33d503cef16329462fc71203b97f5498da2b33d90e85b40b7a5617a in / 
# Thu, 09 Jan 2025 06:40:02 GMT
COPY file:b37d593713ee21ad52a4cd1424dc019a24f7966f85df0ac4b86d234302695328 in /etc/yum.repos.d/. 
# Thu, 09 Jan 2025 06:40:02 GMT
CMD ["/bin/bash"]
# Thu, 09 Jan 2025 06:40:02 GMT
RUN . /cachi2/cachi2.env &&     rm -rf /var/log/*
# Thu, 09 Jan 2025 06:40:03 GMT
LABEL "build-date"="2025-01-09T06:39:36" "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="98c9e4c67f5f2dfc85d12e0f1fd70b809f2a3132" "build-date"="2025-01-09T06:29:15Z" "release"="1736404155"
# Thu, 09 Jan 2025 06:40:13 GMT
RUN /bin/sh
# Thu, 30 Jan 2025 14:32:57 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 30 Jan 2025 14:32:57 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 30 Jan 2025 14:32:57 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 30 Jan 2025 14:32:57 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         fontconfig         glibc-langpack-en     ;     microdnf clean all # buildkit
# Thu, 30 Jan 2025 14:32:57 GMT
ENV JAVA_VERSION=jdk8u442-b06
# Thu, 30 Jan 2025 14:32:57 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='1d1662bd8ca7edc9281c723d9eebafea940e6a41464bdc43a83b564bc974c7e5';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u442-b06/OpenJDK8U-jdk_aarch64_linux_hotspot_8u442b06.tar.gz';          ;;        ppc64le)          ESUM='7eac77deb8fc6c6130f9445c9a68af0bcc40bf6736b5672ef5c3d737c025e84d';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u442-b06/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u442b06.tar.gz';          ;;        x86_64)          ESUM='5b0a0145e7790552a9c8767b4680074c4628ec276e5bb278b61d85cf90facafa';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u442-b06/OpenJDK8U-jdk_x64_linux_hotspot_8u442b06.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip; # buildkit
# Thu, 30 Jan 2025 14:32:57 GMT
RUN set -eux;     echo "Verifying install ...";     echo "javac -version"; javac -version;     echo "java -version"; java -version;     echo "Complete." # buildkit
# Thu, 30 Jan 2025 14:32:57 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 30 Jan 2025 14:32:57 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
```

-	Layers:
	-	`sha256:993bfc176cd8d0372914aae800decf36d6fd3b827bddcc23db1ade8868617a10`  
		Last Modified: Thu, 09 Jan 2025 07:47:11 GMT  
		Size: 37.6 MB (37577421 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9200dd396fa930ba9b5e574dd1a7a802d293946384b1287a63757a8458d18bb`  
		Last Modified: Thu, 09 Jan 2025 07:47:11 GMT  
		Size: 400.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4cc249bdcd042886f9e42f55ca1acbc155028117c6226b2cd68dd2d0b94af56f`  
		Last Modified: Wed, 22 Jan 2025 20:54:17 GMT  
		Size: 37.4 MB (37443876 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79c6d140f47bea58597157b8f4f0fc5bbc045adf7d2c85c930c251b1caf8acb6`  
		Last Modified: Fri, 31 Jan 2025 01:32:42 GMT  
		Size: 53.8 MB (53823328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e29a0fa302a4dab3fdc6836f549b12017f1b657bfc83fd8dc3efd3e6ef23d03`  
		Last Modified: Fri, 31 Jan 2025 01:32:41 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5811e3f276d0d09e2be81cbc84b7e3eec6138f4f7f6bf58ad07b18cbc36c93de`  
		Last Modified: Fri, 31 Jan 2025 01:32:41 GMT  
		Size: 2.3 KB (2316 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:8u442-b06-jdk-ubi9-minimal` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:9524c2c7945ac2df16443a12041653efa516d6fb77cbd0472ee40e912ff3e168
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3808855 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:56d519806105587ac1b218a27467ca5da91bba86276674cca21e846601a0f77f`

```dockerfile
```

-	Layers:
	-	`sha256:ea84d1d8727466d77fd43143fd18de09d2c7e7de2b1e1c5ddbdfa0df9ee5b431`  
		Last Modified: Fri, 31 Jan 2025 01:32:41 GMT  
		Size: 3.8 MB (3788295 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:55aa605d3dfb1102849ed8093a1298bf00430d8192ef7d7386fcaa7668d17cf4`  
		Last Modified: Fri, 31 Jan 2025 01:32:41 GMT  
		Size: 20.6 KB (20560 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-temurin:8u442-b06-jdk-ubi9-minimal` - linux; ppc64le

```console
$ docker pull eclipse-temurin@sha256:67542739fe3f72540e2dd3b0dfdd608e23957ac4320004fcd1bb084ca2ae19a7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **135.4 MB (135443708 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3146689cb912d7bb66a26f2c2c732c937eeee63a8acc03e20e95d7679a4e6bd6`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`

```dockerfile
# Thu, 09 Jan 2025 06:41:59 GMT
LABEL maintainer="Red Hat, Inc."
# Thu, 09 Jan 2025 06:41:59 GMT
LABEL vendor="Red Hat, Inc."
# Thu, 09 Jan 2025 06:41:59 GMT
LABEL url="https://www.redhat.com"
# Thu, 09 Jan 2025 06:41:59 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.5"       distribution-scope="public"
# Thu, 09 Jan 2025 06:41:59 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Thu, 09 Jan 2025 06:41:59 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Thu, 09 Jan 2025 06:41:59 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 09 Jan 2025 06:41:59 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 09 Jan 2025 06:41:59 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Thu, 09 Jan 2025 06:41:59 GMT
LABEL io.openshift.expose-services=""
# Thu, 09 Jan 2025 06:41:59 GMT
LABEL io.openshift.tags="minimal rhel9"
# Thu, 09 Jan 2025 06:41:59 GMT
ENV container oci
# Thu, 09 Jan 2025 06:42:00 GMT
COPY dir:d7227f71d224f4a0ce6e41e096c5f35be3bfb0d1cc57d5e656694dcabcc752aa in / 
# Thu, 09 Jan 2025 06:42:00 GMT
COPY file:b37d593713ee21ad52a4cd1424dc019a24f7966f85df0ac4b86d234302695328 in /etc/yum.repos.d/. 
# Thu, 09 Jan 2025 06:42:00 GMT
CMD ["/bin/bash"]
# Thu, 09 Jan 2025 06:42:00 GMT
RUN . /cachi2/cachi2.env &&     rm -rf /var/log/*
# Thu, 09 Jan 2025 06:42:01 GMT
LABEL "build-date"="2025-01-09T06:41:34" "architecture"="ppc64le" "vcs-type"="git" "vcs-ref"="98c9e4c67f5f2dfc85d12e0f1fd70b809f2a3132" "build-date"="2025-01-09T06:29:15Z" "release"="1736404155"
# Thu, 09 Jan 2025 06:42:17 GMT
RUN /bin/sh
# Thu, 30 Jan 2025 14:32:57 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 30 Jan 2025 14:32:57 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 30 Jan 2025 14:32:57 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 30 Jan 2025 14:32:57 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         fontconfig         glibc-langpack-en     ;     microdnf clean all # buildkit
# Thu, 30 Jan 2025 14:32:57 GMT
ENV JAVA_VERSION=jdk8u442-b06
# Thu, 30 Jan 2025 14:32:57 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='1d1662bd8ca7edc9281c723d9eebafea940e6a41464bdc43a83b564bc974c7e5';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u442-b06/OpenJDK8U-jdk_aarch64_linux_hotspot_8u442b06.tar.gz';          ;;        ppc64le)          ESUM='7eac77deb8fc6c6130f9445c9a68af0bcc40bf6736b5672ef5c3d737c025e84d';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u442-b06/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u442b06.tar.gz';          ;;        x86_64)          ESUM='5b0a0145e7790552a9c8767b4680074c4628ec276e5bb278b61d85cf90facafa';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u442-b06/OpenJDK8U-jdk_x64_linux_hotspot_8u442b06.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip; # buildkit
# Thu, 30 Jan 2025 14:32:57 GMT
RUN set -eux;     echo "Verifying install ...";     echo "javac -version"; javac -version;     echo "java -version"; java -version;     echo "Complete." # buildkit
# Thu, 30 Jan 2025 14:32:57 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 30 Jan 2025 14:32:57 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
```

-	Layers:
	-	`sha256:dce878563f15050dbee433ee11b302dc91caccb7bbf30b63a4d16c18ac4571ad`  
		Last Modified: Thu, 09 Jan 2025 12:32:39 GMT  
		Size: 43.8 MB (43794360 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35e8d75484ae7e9cfff00aa310d4197973e5e690156a92349511c158be98059f`  
		Last Modified: Thu, 09 Jan 2025 12:32:38 GMT  
		Size: 400.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18197cf46ebd87e4c786c45f34ea15620d00514afdc79daf54b112ed798a5efc`  
		Last Modified: Sat, 11 Jan 2025 01:35:09 GMT  
		Size: 39.5 MB (39476434 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf54e44dc9d0e77e320e7421759cf4c56d4ca7e70706538b3d6c76918d5e9843`  
		Last Modified: Fri, 31 Jan 2025 01:34:09 GMT  
		Size: 52.2 MB (52170074 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f243744283d5241e95bdfa7dbcdf9de950530484b7b976b93db6bf46d86b0a56`  
		Last Modified: Fri, 31 Jan 2025 01:34:07 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d093e078141478702cf57d114388454e8089991b2d96fac8c9f5c5541e08eb57`  
		Last Modified: Fri, 31 Jan 2025 01:34:07 GMT  
		Size: 2.3 KB (2314 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:8u442-b06-jdk-ubi9-minimal` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:f2b12c6457641c845e1bd9da57992a59618c02b07bac43e4ec2ff87754fbbbd2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3807391 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea444c63f97b5a04ad509b64f7d83f6ba77b80ebd11f8ea78717bd3e7886dad1`

```dockerfile
```

-	Layers:
	-	`sha256:bd6e25f8a2b785116e93e252018bdf0005b8c7202d02839680e9303df2624ab6`  
		Last Modified: Fri, 31 Jan 2025 01:34:07 GMT  
		Size: 3.8 MB (3786912 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:902d9ba3120a5bd6f8765104bccb86a9cf08f649f464fb2b9033513840724821`  
		Last Modified: Fri, 31 Jan 2025 01:34:07 GMT  
		Size: 20.5 KB (20479 bytes)  
		MIME: application/vnd.in-toto+json
