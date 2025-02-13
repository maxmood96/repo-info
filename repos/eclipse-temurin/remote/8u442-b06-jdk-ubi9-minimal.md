## `eclipse-temurin:8u442-b06-jdk-ubi9-minimal`

```console
$ docker pull eclipse-temurin@sha256:e38a8e1310089cbb39dc7daaaa0612b721650a147984308aa1b401ae0850e7ce
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
$ docker pull eclipse-temurin@sha256:c4aafdbd49b3f81f3fcc1d520e047b8dea16f7a27604b7a3f485471ab6aabd07
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **131.1 MB (131083790 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:33d2a06c5907c87358ebf5ae637a422e37058e3c5158de001d9eb98fa3d9c20e`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`

```dockerfile
# Thu, 30 Jan 2025 14:32:57 GMT
LABEL maintainer="Red Hat, Inc."
# Thu, 30 Jan 2025 14:32:57 GMT
LABEL vendor="Red Hat, Inc."
# Thu, 30 Jan 2025 14:32:57 GMT
LABEL url="https://www.redhat.com"
# Thu, 30 Jan 2025 14:32:57 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.5"       distribution-scope="public"
# Thu, 30 Jan 2025 14:32:57 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Thu, 30 Jan 2025 14:32:57 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Thu, 30 Jan 2025 14:32:57 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 30 Jan 2025 14:32:57 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 30 Jan 2025 14:32:57 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Thu, 30 Jan 2025 14:32:57 GMT
LABEL io.openshift.expose-services=""
# Thu, 30 Jan 2025 14:32:57 GMT
LABEL io.openshift.tags="minimal rhel9"
# Thu, 30 Jan 2025 14:32:57 GMT
ENV container oci
# Thu, 30 Jan 2025 14:32:57 GMT
COPY dir:fc29285925cd626d62a818aff5b79af4bb61fc4890fdd703305a9455e4e11f19 in / 
# Thu, 30 Jan 2025 14:32:57 GMT
COPY file:b37d593713ee21ad52a4cd1424dc019a24f7966f85df0ac4b86d234302695328 in /etc/yum.repos.d/. 
# Thu, 30 Jan 2025 14:32:57 GMT
CMD ["/bin/bash"]
# Thu, 30 Jan 2025 14:32:57 GMT
RUN . /cachi2/cachi2.env &&     rm -rf /var/log/*
# Thu, 30 Jan 2025 14:32:57 GMT
LABEL "build-date"="2025-02-06T04:43:42" "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="adfffabe9acacc27d15fc0ceb8e083254ca7b450" "build-date"="2025-02-06T04:39:35Z" "release"="1738816775"
# Thu, 30 Jan 2025 14:32:57 GMT
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
	-	`sha256:667deb3fcbde45825554b378b8e593f6c3c4a339133a1a80c4d2e1594ff96723`  
		Last Modified: Thu, 06 Feb 2025 05:39:44 GMT  
		Size: 39.4 MB (39370269 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8339c472296e0e9bde11d7c0a4c8b8c7060108aa1aa729ab95b5275b1fa7163`  
		Last Modified: Thu, 06 Feb 2025 05:39:42 GMT  
		Size: 462.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95fcd48ae10263316b1f75ab3a5e14016fb08a36163380e25b8a56d11447312f`  
		Last Modified: Fri, 07 Feb 2025 05:05:01 GMT  
		Size: 37.0 MB (36988839 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ef59420dada219db77b0bf7a6d762abaa406299c7f2e17e522f58780a5f095f`  
		Last Modified: Fri, 07 Feb 2025 05:05:00 GMT  
		Size: 54.7 MB (54721776 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb18b7a12c88c361ec9fda82aed3419c45555451d40f052eb1539cd8fa624d66`  
		Last Modified: Fri, 07 Feb 2025 05:04:57 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3af9a2d5124b9c23b43744bf115715fd634058067a5968c300b2d2214068760e`  
		Last Modified: Fri, 07 Feb 2025 05:04:59 GMT  
		Size: 2.3 KB (2317 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:8u442-b06-jdk-ubi9-minimal` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:b84be593dd9bede5db40f1fc4af29bb0804b14863a519e49fe5013c339eb76df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3808862 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a8e075ba68c9e7a71e16ea161a47c79317db1f48152ccb97e9acd322e3781bda`

```dockerfile
```

-	Layers:
	-	`sha256:27b8481d8aaf26d3aa464b2a4cc8bd545c17c523a3702ceb785e4a8e8aed9308`  
		Last Modified: Fri, 07 Feb 2025 00:30:09 GMT  
		Size: 3.8 MB (3788418 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ff9e252b6ffd47f7702405e5c006351bd48f8c5b17045381a5d6cad7dc06768a`  
		Last Modified: Fri, 07 Feb 2025 00:30:08 GMT  
		Size: 20.4 KB (20444 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-temurin:8u442-b06-jdk-ubi9-minimal` - linux; arm64 variant v8

```console
$ docker pull eclipse-temurin@sha256:3f1fe396339fdc950185207908a42c263c5751f3e721a3f044d227187de8f3a7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **128.9 MB (128860478 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fce7db6a3c90cfbe95e4e4bd95915ad804ccc65703560c2e850aa32ef3db9f1b`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`

```dockerfile
# Thu, 30 Jan 2025 14:32:57 GMT
LABEL maintainer="Red Hat, Inc."
# Thu, 30 Jan 2025 14:32:57 GMT
LABEL vendor="Red Hat, Inc."
# Thu, 30 Jan 2025 14:32:57 GMT
LABEL url="https://www.redhat.com"
# Thu, 30 Jan 2025 14:32:57 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.5"       distribution-scope="public"
# Thu, 30 Jan 2025 14:32:57 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Thu, 30 Jan 2025 14:32:57 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Thu, 30 Jan 2025 14:32:57 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 30 Jan 2025 14:32:57 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 30 Jan 2025 14:32:57 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Thu, 30 Jan 2025 14:32:57 GMT
LABEL io.openshift.expose-services=""
# Thu, 30 Jan 2025 14:32:57 GMT
LABEL io.openshift.tags="minimal rhel9"
# Thu, 30 Jan 2025 14:32:57 GMT
ENV container oci
# Thu, 30 Jan 2025 14:32:57 GMT
COPY dir:389f5f73f217a50cb052c224af980ef5943f8527170a8ed8ba3b540101351720 in / 
# Thu, 30 Jan 2025 14:32:57 GMT
COPY file:b37d593713ee21ad52a4cd1424dc019a24f7966f85df0ac4b86d234302695328 in /etc/yum.repos.d/. 
# Thu, 30 Jan 2025 14:32:57 GMT
CMD ["/bin/bash"]
# Thu, 30 Jan 2025 14:32:57 GMT
RUN . /cachi2/cachi2.env &&     rm -rf /var/log/*
# Thu, 30 Jan 2025 14:32:57 GMT
LABEL "build-date"="2025-02-06T04:48:45" "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="adfffabe9acacc27d15fc0ceb8e083254ca7b450" "build-date"="2025-02-06T04:39:35Z" "release"="1738816775"
# Thu, 30 Jan 2025 14:32:57 GMT
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
	-	`sha256:8174eb1151f28d1a88085da5d27ffd5729467439a2f1a77d03498e89f9f7ef4b`  
		Last Modified: Thu, 06 Feb 2025 06:30:59 GMT  
		Size: 37.6 MB (37592304 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc6c4d65a5f9a8b0c8f76083cf10d14a2417324b530dfde1115d46147afe1c17`  
		Last Modified: Thu, 06 Feb 2025 06:26:49 GMT  
		Size: 460.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc676c7b0d497bf2463a37af5f2c36a9724601e6cd79a9e4fa127c484ad01df3`  
		Last Modified: Fri, 07 Feb 2025 04:47:29 GMT  
		Size: 37.4 MB (37441949 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7bab7d258f97283b324626b7f7777eb537624902cafba0f1c14d4f0088de59c`  
		Last Modified: Sat, 08 Feb 2025 03:25:58 GMT  
		Size: 53.8 MB (53823321 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20f581d38e382843aac139d86bea3b3083a20fc74efc523be3d9114a739aa0e1`  
		Last Modified: Sat, 08 Feb 2025 03:26:46 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1962bc86314c06a0df623d77ff7bd437f9f4df9c8c4d112c464317f3a16eee11`  
		Last Modified: Sat, 08 Feb 2025 03:26:46 GMT  
		Size: 2.3 KB (2316 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:8u442-b06-jdk-ubi9-minimal` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:8926b0c4284678028f36a1109405035b68031c5e33a7fb9bdd116830b72855a6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3808867 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a8ab61f8111940db3808a09859ef56635ea0ce6420d329c2c2271659951dd37c`

```dockerfile
```

-	Layers:
	-	`sha256:b726f69526a385ef03a61d475a9c3f2e84b4611c5cdcf5f26f5f1ca4febde570`  
		Last Modified: Fri, 07 Feb 2025 02:22:28 GMT  
		Size: 3.8 MB (3788307 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2bb6b8a8140fb402aaeef84d1e779e902dddea909656e2565e0507d149273f62`  
		Last Modified: Fri, 07 Feb 2025 02:22:28 GMT  
		Size: 20.6 KB (20560 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-temurin:8u442-b06-jdk-ubi9-minimal` - linux; ppc64le

```console
$ docker pull eclipse-temurin@sha256:7b44fd19d561d01973b07ffed95d4c220da830ce79527fe60adcbf0d2e400bd7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **135.5 MB (135461185 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:76808bba956a50189b0f1cb273125581a3f0247852a988d97aa0e4f80da53d3b`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`

```dockerfile
# Thu, 30 Jan 2025 14:32:57 GMT
LABEL maintainer="Red Hat, Inc."
# Thu, 30 Jan 2025 14:32:57 GMT
LABEL vendor="Red Hat, Inc."
# Thu, 30 Jan 2025 14:32:57 GMT
LABEL url="https://www.redhat.com"
# Thu, 30 Jan 2025 14:32:57 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.5"       distribution-scope="public"
# Thu, 30 Jan 2025 14:32:57 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Thu, 30 Jan 2025 14:32:57 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Thu, 30 Jan 2025 14:32:57 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 30 Jan 2025 14:32:57 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 30 Jan 2025 14:32:57 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Thu, 30 Jan 2025 14:32:57 GMT
LABEL io.openshift.expose-services=""
# Thu, 30 Jan 2025 14:32:57 GMT
LABEL io.openshift.tags="minimal rhel9"
# Thu, 30 Jan 2025 14:32:57 GMT
ENV container oci
# Thu, 30 Jan 2025 14:32:57 GMT
COPY dir:4b7f9a609ef7d9b773f245d53ef2354786362b2e75b9988fe7bd642ce728205f in / 
# Thu, 30 Jan 2025 14:32:57 GMT
COPY file:b37d593713ee21ad52a4cd1424dc019a24f7966f85df0ac4b86d234302695328 in /etc/yum.repos.d/. 
# Thu, 30 Jan 2025 14:32:57 GMT
CMD ["/bin/bash"]
# Thu, 30 Jan 2025 14:32:57 GMT
RUN . /cachi2/cachi2.env &&     rm -rf /var/log/*
# Thu, 30 Jan 2025 14:32:57 GMT
LABEL "build-date"="2025-02-06T04:53:22" "architecture"="ppc64le" "vcs-type"="git" "vcs-ref"="adfffabe9acacc27d15fc0ceb8e083254ca7b450" "build-date"="2025-02-06T04:39:35Z" "release"="1738816775"
# Thu, 30 Jan 2025 14:32:57 GMT
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
	-	`sha256:dce4a6a210ec1ffa38c334f3d0bde7e211e699baa435083097a719864994a122`  
		Last Modified: Thu, 06 Feb 2025 07:04:21 GMT  
		Size: 43.8 MB (43811508 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9afaf9d1aa9b6d6e11a6a514269450db16106e006fbbe873e9f503b11a04ce1f`  
		Last Modified: Thu, 06 Feb 2025 07:04:22 GMT  
		Size: 460.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95584c2b6fee8cd3a7b6ddc79425576afe40f52f01efd248564da9afcd4ca985`  
		Last Modified: Fri, 07 Feb 2025 05:30:38 GMT  
		Size: 39.5 MB (39476691 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a71b0bf23fc79ccad1a43cd1658abae91bf626c19fa269bb3c7ca806de428890`  
		Last Modified: Fri, 07 Feb 2025 01:26:24 GMT  
		Size: 52.2 MB (52170079 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43709e8b3ee9caa7ae52c1998f5f191a2b8ef5f1ba0216841ef7da4a6da8c4d8`  
		Last Modified: Fri, 07 Feb 2025 01:26:23 GMT  
		Size: 131.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9038801d749e89a93537e987925903967cd59e5295359b7fe1601c386ea63b8`  
		Last Modified: Fri, 07 Feb 2025 01:26:24 GMT  
		Size: 2.3 KB (2316 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:8u442-b06-jdk-ubi9-minimal` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:5b215a2748f554df9dd98652e0e92c24ef73580f569554a371f36d5a0d7fbae5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3807404 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:63106c5a20df8573e84a38a9cec15a912eeaed0838491b35808c86d641ed92a2`

```dockerfile
```

-	Layers:
	-	`sha256:77a2746c571fc96392097d4e4e71636a61e5d41dbc08df8668c4f119e120f048`  
		Last Modified: Fri, 07 Feb 2025 01:26:23 GMT  
		Size: 3.8 MB (3786924 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8f7ff3618fe8d898306f8c5f4514a6867f3df367b5b3c63184ae40cc83cbb3a9`  
		Last Modified: Fri, 07 Feb 2025 01:26:22 GMT  
		Size: 20.5 KB (20480 bytes)  
		MIME: application/vnd.in-toto+json
