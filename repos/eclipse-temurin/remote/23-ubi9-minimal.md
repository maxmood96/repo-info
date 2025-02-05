## `eclipse-temurin:23-ubi9-minimal`

```console
$ docker pull eclipse-temurin@sha256:f7e94d100e264822ffabcc8becacd42f6137d1058af0404e3ef0f263e979efa3
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

### `eclipse-temurin:23-ubi9-minimal` - linux; amd64

```console
$ docker pull eclipse-temurin@sha256:402a255d7c9a045694e48440082ec3b1a06c0e6345159bcb6d98dac1bb38a0e8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **241.7 MB (241683191 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6d10be959b6fd9e91dd2472d460ca7de62511b0a5649711c1535d65c2836b8eb`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["jshell"]`

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
COPY dir:791945992d1a1a0e69cb46f548168dd778c0a5b28228ca7d157145f53fdb49cd in / 
# Thu, 30 Jan 2025 14:32:57 GMT
COPY file:b37d593713ee21ad52a4cd1424dc019a24f7966f85df0ac4b86d234302695328 in /etc/yum.repos.d/. 
# Thu, 30 Jan 2025 14:32:57 GMT
CMD ["/bin/bash"]
# Thu, 30 Jan 2025 14:32:57 GMT
RUN . /cachi2/cachi2.env &&     rm -rf /var/log/*
# Thu, 30 Jan 2025 14:32:57 GMT
LABEL "build-date"="2025-02-04T04:38:14" "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="177f460763ad3b12e4b8be13035c0af01fc0d47e" "build-date"="2025-02-04T04:34:12Z" "release"="1738643652"
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
ENV JAVA_VERSION=jdk-23.0.2+7
# Thu, 30 Jan 2025 14:32:57 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='fb43ae1202402842559cb6223886ec1663b90ffbec48479abbcb92c92c9012eb';          BINARY_URL='https://github.com/adoptium/temurin23-binaries/releases/download/jdk-23.0.2%2B7/OpenJDK23U-jdk_aarch64_linux_hotspot_23.0.2_7.tar.gz';          ;;        ppc64le)          ESUM='548fd82af4eb0802fe20b0b61a4664a69c7f03cd963540908f30dbf73636dafe';          BINARY_URL='https://github.com/adoptium/temurin23-binaries/releases/download/jdk-23.0.2%2B7/OpenJDK23U-jdk_ppc64le_linux_hotspot_23.0.2_7.tar.gz';          ;;        s390x)          ESUM='591ccf4d27016315700cc9cc979f7cf343900b6bee1b0b45c93f2c5f946e5aac';          BINARY_URL='https://github.com/adoptium/temurin23-binaries/releases/download/jdk-23.0.2%2B7/OpenJDK23U-jdk_s390x_linux_hotspot_23.0.2_7.tar.gz';          ;;        x86_64)          ESUM='870ac8c05c6fe563e7a3878a47d0234b83c050e83651d2c47e8b822ec74512dd';          BINARY_URL='https://github.com/adoptium/temurin23-binaries/releases/download/jdk-23.0.2%2B7/OpenJDK23U-jdk_x64_linux_hotspot_23.0.2_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Thu, 30 Jan 2025 14:32:57 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 30 Jan 2025 14:32:57 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 30 Jan 2025 14:32:57 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 30 Jan 2025 14:32:57 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:24436b52f270faaf1cd45508746ed85af4420ecadbf33becda289f2e4221eb18`  
		Last Modified: Tue, 04 Feb 2025 06:12:46 GMT  
		Size: 39.4 MB (39370931 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7773c651ce2558c22521f6ea1bb2e11b3a7e0f291de522fb1183c6ab4e62c1a6`  
		Last Modified: Tue, 04 Feb 2025 06:12:45 GMT  
		Size: 462.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96aaf6686c94802eebc743eb8a67f824ec136ae628d290753ebf73987d9dcb54`  
		Last Modified: Tue, 04 Feb 2025 20:33:26 GMT  
		Size: 37.0 MB (36988161 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4bd13ebba1a5e6a2dc7be0255af922316c5cb63e4e47c50cd263f256b3d7c5d7`  
		Last Modified: Tue, 04 Feb 2025 20:33:27 GMT  
		Size: 165.3 MB (165321216 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc75688a7a7a42e91ca620a319dba41c58265bddf0f5d3c521e09257a0c27699`  
		Last Modified: Tue, 04 Feb 2025 20:33:25 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d5ed6cfd769f86e3c2f42df2752427112dcbb9d1b2fa6a5410f2086ddae1c92`  
		Last Modified: Tue, 04 Feb 2025 20:33:25 GMT  
		Size: 2.3 KB (2292 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:23-ubi9-minimal` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:8fd4cf4c821368f5722efe028d00698097518292afb31d6cf5e9db9edc66dab7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3693499 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d2a30d9299151c4fb1e9e858cba3db033585fbccb738d5bca9d7b9175d1cdd38`

```dockerfile
```

-	Layers:
	-	`sha256:e3559af834e9e1adc15b3f06af892b1bfb82dad8933c37d96c5bfb17c37d99f6`  
		Last Modified: Tue, 04 Feb 2025 20:33:25 GMT  
		Size: 3.7 MB (3671809 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1aa243e41848b2f56275808a9b451f1e43ffd027d539968a9ee45f6e874ec048`  
		Last Modified: Tue, 04 Feb 2025 20:33:25 GMT  
		Size: 21.7 KB (21690 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-temurin:23-ubi9-minimal` - linux; arm64 variant v8

```console
$ docker pull eclipse-temurin@sha256:4562d5f27796cde9df7e65aca6862dcb698feb5e7824012b4562b17c07b68b8a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **238.4 MB (238385689 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:80ed1c345082c1f66321947feb8e0e65b970eb439cd1d3368bf2e292c02dbe72`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["jshell"]`

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
COPY dir:9a473b4852f6cbe9a0f08b40d1fff87f485e10a0b3973b8009cae74075e5e063 in / 
# Thu, 30 Jan 2025 14:32:57 GMT
COPY file:b37d593713ee21ad52a4cd1424dc019a24f7966f85df0ac4b86d234302695328 in /etc/yum.repos.d/. 
# Thu, 30 Jan 2025 14:32:57 GMT
CMD ["/bin/bash"]
# Thu, 30 Jan 2025 14:32:57 GMT
RUN . /cachi2/cachi2.env &&     rm -rf /var/log/*
# Thu, 30 Jan 2025 14:32:57 GMT
LABEL "build-date"="2025-02-04T04:40:56" "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="177f460763ad3b12e4b8be13035c0af01fc0d47e" "build-date"="2025-02-04T04:34:12Z" "release"="1738643652"
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
ENV JAVA_VERSION=jdk-23.0.2+7
# Thu, 30 Jan 2025 14:32:57 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='fb43ae1202402842559cb6223886ec1663b90ffbec48479abbcb92c92c9012eb';          BINARY_URL='https://github.com/adoptium/temurin23-binaries/releases/download/jdk-23.0.2%2B7/OpenJDK23U-jdk_aarch64_linux_hotspot_23.0.2_7.tar.gz';          ;;        ppc64le)          ESUM='548fd82af4eb0802fe20b0b61a4664a69c7f03cd963540908f30dbf73636dafe';          BINARY_URL='https://github.com/adoptium/temurin23-binaries/releases/download/jdk-23.0.2%2B7/OpenJDK23U-jdk_ppc64le_linux_hotspot_23.0.2_7.tar.gz';          ;;        s390x)          ESUM='591ccf4d27016315700cc9cc979f7cf343900b6bee1b0b45c93f2c5f946e5aac';          BINARY_URL='https://github.com/adoptium/temurin23-binaries/releases/download/jdk-23.0.2%2B7/OpenJDK23U-jdk_s390x_linux_hotspot_23.0.2_7.tar.gz';          ;;        x86_64)          ESUM='870ac8c05c6fe563e7a3878a47d0234b83c050e83651d2c47e8b822ec74512dd';          BINARY_URL='https://github.com/adoptium/temurin23-binaries/releases/download/jdk-23.0.2%2B7/OpenJDK23U-jdk_x64_linux_hotspot_23.0.2_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Thu, 30 Jan 2025 14:32:57 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 30 Jan 2025 14:32:57 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 30 Jan 2025 14:32:57 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 30 Jan 2025 14:32:57 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:93168a48887270ffcd74fa1e7b5a85a6420b35b7dca5a5971f063fb8a0d3264a`  
		Last Modified: Tue, 04 Feb 2025 06:12:53 GMT  
		Size: 37.6 MB (37592781 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c3b362866ca09649c77058b63f51549ffa71c5ffce326fe4b42995cfb1180db`  
		Last Modified: Tue, 04 Feb 2025 06:12:52 GMT  
		Size: 460.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84479dead7bf933b66919d3f2ec6e0c436e237743bb05b2641923502bc6498ad`  
		Last Modified: Wed, 05 Feb 2025 01:56:02 GMT  
		Size: 37.4 MB (37442468 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd3279270828406cee4bf5f085eebd096432572988cee1b7af0267ab456651cb`  
		Last Modified: Wed, 05 Feb 2025 02:00:31 GMT  
		Size: 163.3 MB (163347561 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55669bbaed5aadd8d608e1934f285003efda09ad4770ebe029e56819abf925cc`  
		Last Modified: Wed, 05 Feb 2025 02:00:26 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77c7a1686b40b56413ae198162e5e8488b9681c4373940647852d5593dd58aab`  
		Last Modified: Wed, 05 Feb 2025 02:00:26 GMT  
		Size: 2.3 KB (2291 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:23-ubi9-minimal` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:e3eba0dd39ccf82204119875ba6069d93c246956b88e13b2ec5ddcc0a422ae5f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3692186 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e250347e765b6cfb30f42b7533a55cea97192910c13e14761d46258fbf338a7e`

```dockerfile
```

-	Layers:
	-	`sha256:ec03c1cda730ad8652c3da21478b2f07e8113e6939e3252f4009125ecb8ecab8`  
		Last Modified: Wed, 05 Feb 2025 02:00:27 GMT  
		Size: 3.7 MB (3670379 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ac947079f51fd14a3f63f00aa72053f7ac28eeca8a84cfca194dceb23b12d7a3`  
		Last Modified: Wed, 05 Feb 2025 02:00:26 GMT  
		Size: 21.8 KB (21807 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-temurin:23-ubi9-minimal` - linux; ppc64le

```console
$ docker pull eclipse-temurin@sha256:779738f3cf481c0bfb40459a74ab1f4063908c92ed4d6e5f96ca053c0c7b5f15
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **248.5 MB (248508862 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c9b7d8c62373c81ffd7916493019ee2c0b9a13d446b179b8229307344de54647`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["jshell"]`

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
COPY dir:86eaaeeda22f0fc1610df3530c5b1f3ed71bded65fc4f1a6f230c64b6243fd6f in / 
# Thu, 30 Jan 2025 14:32:57 GMT
COPY file:b37d593713ee21ad52a4cd1424dc019a24f7966f85df0ac4b86d234302695328 in /etc/yum.repos.d/. 
# Thu, 30 Jan 2025 14:32:57 GMT
CMD ["/bin/bash"]
# Thu, 30 Jan 2025 14:32:57 GMT
RUN . /cachi2/cachi2.env &&     rm -rf /var/log/*
# Thu, 30 Jan 2025 14:32:57 GMT
LABEL "build-date"="2025-02-04T04:45:48" "architecture"="ppc64le" "vcs-type"="git" "vcs-ref"="177f460763ad3b12e4b8be13035c0af01fc0d47e" "build-date"="2025-02-04T04:34:12Z" "release"="1738643652"
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
ENV JAVA_VERSION=jdk-23.0.2+7
# Thu, 30 Jan 2025 14:32:57 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='fb43ae1202402842559cb6223886ec1663b90ffbec48479abbcb92c92c9012eb';          BINARY_URL='https://github.com/adoptium/temurin23-binaries/releases/download/jdk-23.0.2%2B7/OpenJDK23U-jdk_aarch64_linux_hotspot_23.0.2_7.tar.gz';          ;;        ppc64le)          ESUM='548fd82af4eb0802fe20b0b61a4664a69c7f03cd963540908f30dbf73636dafe';          BINARY_URL='https://github.com/adoptium/temurin23-binaries/releases/download/jdk-23.0.2%2B7/OpenJDK23U-jdk_ppc64le_linux_hotspot_23.0.2_7.tar.gz';          ;;        s390x)          ESUM='591ccf4d27016315700cc9cc979f7cf343900b6bee1b0b45c93f2c5f946e5aac';          BINARY_URL='https://github.com/adoptium/temurin23-binaries/releases/download/jdk-23.0.2%2B7/OpenJDK23U-jdk_s390x_linux_hotspot_23.0.2_7.tar.gz';          ;;        x86_64)          ESUM='870ac8c05c6fe563e7a3878a47d0234b83c050e83651d2c47e8b822ec74512dd';          BINARY_URL='https://github.com/adoptium/temurin23-binaries/releases/download/jdk-23.0.2%2B7/OpenJDK23U-jdk_x64_linux_hotspot_23.0.2_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Thu, 30 Jan 2025 14:32:57 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 30 Jan 2025 14:32:57 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 30 Jan 2025 14:32:57 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 30 Jan 2025 14:32:57 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:ab1f86d0f34fa967c24e957a9589d5e97ac11fbc48f1c47f2ad66357588ea649`  
		Last Modified: Tue, 04 Feb 2025 06:13:08 GMT  
		Size: 43.8 MB (43812384 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02a26502eee0ac1b566e8c1915dcb2d87d299688b9b9004feafb89ec7b29c48e`  
		Last Modified: Tue, 04 Feb 2025 06:13:06 GMT  
		Size: 459.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:347e995a3ea744fbc6cc7a931bed349b6719e0856e76ac20c2e4b79b93870d5a`  
		Last Modified: Tue, 04 Feb 2025 22:22:34 GMT  
		Size: 39.5 MB (39477501 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64a594671340c15ba9334675c01928b1041c43627441a2d756340615e026c577`  
		Last Modified: Tue, 04 Feb 2025 22:30:34 GMT  
		Size: 165.2 MB (165216099 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23dc03e184770ce2dc72e3860c0dda13f0fe6ead25ed151ebe464675c31a6b7d`  
		Last Modified: Tue, 04 Feb 2025 22:30:30 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51e0cb23404dedbe3cf0c9247730fb479abfb23ba45f1531823774f422941294`  
		Last Modified: Tue, 04 Feb 2025 22:30:30 GMT  
		Size: 2.3 KB (2291 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:23-ubi9-minimal` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:1da739baacf0d8dc57bb5b8edbec1945e2825c261f97e94f6a9d5cbb21ee01f1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3690840 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:76880a356943a987f6945c558f65b1ba4b6ee58c61b80275f2b259c07b202b90`

```dockerfile
```

-	Layers:
	-	`sha256:0983ffee02c8d3838e8307e91bc4bcc177cb44acb892243985941fac01a9f7f1`  
		Last Modified: Tue, 04 Feb 2025 22:30:30 GMT  
		Size: 3.7 MB (3669113 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fb965342bcfaa00a77b3d79b61a30597186f3b44b634c1fdb34681799388c53b`  
		Last Modified: Tue, 04 Feb 2025 22:30:30 GMT  
		Size: 21.7 KB (21727 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-temurin:23-ubi9-minimal` - linux; s390x

```console
$ docker pull eclipse-temurin@sha256:cc7a5c91b13f607deeb844f0431b42578c65864c5bfe0b182e6e5575f66d5df3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **229.0 MB (228961582 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f7ea562b00f29aadf783833a9d909681e4fc6fd0f89c0230c8acc244a33aa6ba`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["jshell"]`

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
COPY dir:e4f2c18684ff5ef7306326b55f2c892a9155159af76ab7e5cd185fec25280bc1 in / 
# Thu, 30 Jan 2025 14:32:57 GMT
COPY file:b37d593713ee21ad52a4cd1424dc019a24f7966f85df0ac4b86d234302695328 in /etc/yum.repos.d/. 
# Thu, 30 Jan 2025 14:32:57 GMT
CMD ["/bin/bash"]
# Thu, 30 Jan 2025 14:32:57 GMT
RUN . /cachi2/cachi2.env &&     rm -rf /var/log/*
# Thu, 30 Jan 2025 14:32:57 GMT
LABEL "build-date"="2025-02-04T04:44:01" "architecture"="s390x" "vcs-type"="git" "vcs-ref"="177f460763ad3b12e4b8be13035c0af01fc0d47e" "build-date"="2025-02-04T04:34:12Z" "release"="1738643652"
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
ENV JAVA_VERSION=jdk-23.0.2+7
# Thu, 30 Jan 2025 14:32:57 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='fb43ae1202402842559cb6223886ec1663b90ffbec48479abbcb92c92c9012eb';          BINARY_URL='https://github.com/adoptium/temurin23-binaries/releases/download/jdk-23.0.2%2B7/OpenJDK23U-jdk_aarch64_linux_hotspot_23.0.2_7.tar.gz';          ;;        ppc64le)          ESUM='548fd82af4eb0802fe20b0b61a4664a69c7f03cd963540908f30dbf73636dafe';          BINARY_URL='https://github.com/adoptium/temurin23-binaries/releases/download/jdk-23.0.2%2B7/OpenJDK23U-jdk_ppc64le_linux_hotspot_23.0.2_7.tar.gz';          ;;        s390x)          ESUM='591ccf4d27016315700cc9cc979f7cf343900b6bee1b0b45c93f2c5f946e5aac';          BINARY_URL='https://github.com/adoptium/temurin23-binaries/releases/download/jdk-23.0.2%2B7/OpenJDK23U-jdk_s390x_linux_hotspot_23.0.2_7.tar.gz';          ;;        x86_64)          ESUM='870ac8c05c6fe563e7a3878a47d0234b83c050e83651d2c47e8b822ec74512dd';          BINARY_URL='https://github.com/adoptium/temurin23-binaries/releases/download/jdk-23.0.2%2B7/OpenJDK23U-jdk_x64_linux_hotspot_23.0.2_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Thu, 30 Jan 2025 14:32:57 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 30 Jan 2025 14:32:57 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 30 Jan 2025 14:32:57 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 30 Jan 2025 14:32:57 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:f2c60604373bca3b723153547f9e3eb1b61b4624a6533a0e44a4a24b3a6a5fd9`  
		Last Modified: Tue, 04 Feb 2025 06:12:59 GMT  
		Size: 37.5 MB (37509933 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffad1e63add1f545943d65ae14bc90751c2d7d5a9bf5feb6dde9cdf16d6faa0e`  
		Last Modified: Tue, 04 Feb 2025 06:12:58 GMT  
		Size: 459.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79d8dde926e1cd7b699bd4757bc6b3441a0004e029140a4dfd9157b6d0cd6670`  
		Last Modified: Tue, 04 Feb 2025 22:36:20 GMT  
		Size: 37.0 MB (37005223 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8f4bffcd3dc2d82b3eba0cb30aaa992da7ca8817d2f7ab3641a372ba8ad024a`  
		Last Modified: Tue, 04 Feb 2025 22:43:05 GMT  
		Size: 154.4 MB (154443550 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d1108dde35842bdefdf648ab71dee952ccd5a291e2f5fef65c1627105f61d63`  
		Last Modified: Tue, 04 Feb 2025 22:43:02 GMT  
		Size: 130.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15bd30fdc35876b2998cfbf45c2a003c2bce1c1fd9099f8dbf16fa4441cf55be`  
		Last Modified: Tue, 04 Feb 2025 22:43:02 GMT  
		Size: 2.3 KB (2287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:23-ubi9-minimal` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:b938f2a282fae410d3fa6297810b3fb68d4e2ef7f152587476e33ca118e14a8a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3680104 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e2e8d013e4acf2df4a60c42a97db8395e44b23241df415695c371cacea4442c`

```dockerfile
```

-	Layers:
	-	`sha256:a2e65a820a189e40788c3f720f7eee0f6fd8f1979134ce684c5d396546447758`  
		Last Modified: Tue, 04 Feb 2025 22:43:02 GMT  
		Size: 3.7 MB (3658413 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d7f14b951dc37a46c212832400bfee0bc70503680a7bd714095c452282b8ac5e`  
		Last Modified: Tue, 04 Feb 2025 22:43:01 GMT  
		Size: 21.7 KB (21691 bytes)  
		MIME: application/vnd.in-toto+json
