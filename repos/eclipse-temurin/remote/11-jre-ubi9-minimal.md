## `eclipse-temurin:11-jre-ubi9-minimal`

```console
$ docker pull eclipse-temurin@sha256:7250ad340fc399687cb2e9e742fb25181dad8537c675a62ee343c435e4482844
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

### `eclipse-temurin:11-jre-ubi9-minimal` - linux; amd64

```console
$ docker pull eclipse-temurin@sha256:afd924f725d142892d392f94d97194f2b3ec515dcbfd207a5baa3b50ee8fc65b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **120.6 MB (120577937 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:231f621dc223da05497adcff75193fd27ff7f1f09537d9fec7ddc76074e30ebd`
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
COPY dir:0423d0cd4a34047821e55a2806cb02fc682f017fba03e4344223878a61041986 in / 
# Thu, 30 Jan 2025 14:32:57 GMT
COPY file:b37d593713ee21ad52a4cd1424dc019a24f7966f85df0ac4b86d234302695328 in /etc/yum.repos.d/. 
# Thu, 30 Jan 2025 14:32:57 GMT
CMD ["/bin/bash"]
# Thu, 30 Jan 2025 14:32:57 GMT
RUN . /cachi2/cachi2.env &&     rm -rf /var/log/*
# Thu, 30 Jan 2025 14:32:57 GMT
LABEL "build-date"="2025-02-13T04:19:45" "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="c0546ad1ce412f8077a547cb8d0d68d04f08815c" "build-date"="2025-02-13T04:15:47Z" "release"="1739420147"
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
ENV JAVA_VERSION=jdk-11.0.26+4
# Thu, 30 Jan 2025 14:32:57 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='4ececb5c229763107e9e4acf3b7035db38cf18a98a47176fa5ed1be3f3d15518';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.26%2B4/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.26_4.tar.gz';          ;;        ppc64le)          ESUM='69b38f0dde128d8c606012335cd60f1f55afa09b4135582188943bee699ebf03';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.26%2B4/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.26_4.tar.gz';          ;;        s390x)          ESUM='5d9552b1fb699da6052cbd600e750dd8ff48a89a384d537919a3c999257979dc';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.26%2B4/OpenJDK11U-jre_s390x_linux_hotspot_11.0.26_4.tar.gz';          ;;        x86_64)          ESUM='d26c566a7010d1303d3979b6f076e7911b49419a609c9e4d81f27262bf47f87c';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.26%2B4/OpenJDK11U-jre_x64_linux_hotspot_11.0.26_4.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz; # buildkit
# Thu, 30 Jan 2025 14:32:57 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 30 Jan 2025 14:32:57 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 30 Jan 2025 14:32:57 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
```

-	Layers:
	-	`sha256:3333307dcd2e4279579646a05a5f99082a61a20906175240445b0e15f73b6d6e`  
		Last Modified: Thu, 13 Feb 2025 06:13:39 GMT  
		Size: 39.4 MB (39366553 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5025173ec0b35686a33458b367c2a6e898c824f57a07925c25d26a0cfb5f2e50`  
		Last Modified: Thu, 13 Feb 2025 06:13:37 GMT  
		Size: 461.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28f689a175815b2e7c5062ed9a00f0f526d8dd86ae51eb49a39078c1604475c0`  
		Last Modified: Fri, 14 Feb 2025 00:27:48 GMT  
		Size: 37.0 MB (36979983 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee954c9f32a3ddbeab18c6173237d52b2b8009ba7d1ed536ee361a58d0d3f497`  
		Last Modified: Fri, 14 Feb 2025 00:27:48 GMT  
		Size: 44.2 MB (44228521 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e7673eea5e02c5a01fec074c7b59813dc71a5da8b49f161226efd4a0fd0bb53`  
		Last Modified: Fri, 14 Feb 2025 00:27:48 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31f385c99999cf91b8da1399a6b3abbe3141cfe31b4d9252e15402174045b933`  
		Last Modified: Fri, 14 Feb 2025 01:27:33 GMT  
		Size: 2.3 KB (2291 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:11-jre-ubi9-minimal` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:f23757d7523a593b611c0d91c74735fc58f56374a34d1de707399a84845dea64
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3615595 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7600f0750aa5e33bc035d4355604b778d1f18ca6cc2e972a236735e6e86a9f9d`

```dockerfile
```

-	Layers:
	-	`sha256:656a733f6ac071c3b72b792165e479d5f8a7070d5d80f5025cf3d87b1914c248`  
		Last Modified: Fri, 14 Feb 2025 04:12:53 GMT  
		Size: 3.6 MB (3594838 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:026e45b97762fdc265d1ee9f78e30fd75fc93b21a00ce1b4bf6015b896b006d4`  
		Last Modified: Fri, 14 Feb 2025 04:12:53 GMT  
		Size: 20.8 KB (20757 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-temurin:11-jre-ubi9-minimal` - linux; arm64 variant v8

```console
$ docker pull eclipse-temurin@sha256:73e5d4a4683f902db0a49be1da702ee44d75611c67db98f2760c877deb04109c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **117.7 MB (117651218 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e0c32eb2cd4bee8808c768f2b3c789b8e0e36b9cb258cd1c8d28522abdd2a78`
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
COPY dir:5809c16e2c5c048de6a8d8eea9437ac183b7d2503e26b24a2422ead5736aecad in / 
# Thu, 30 Jan 2025 14:32:57 GMT
COPY file:b37d593713ee21ad52a4cd1424dc019a24f7966f85df0ac4b86d234302695328 in /etc/yum.repos.d/. 
# Thu, 30 Jan 2025 14:32:57 GMT
CMD ["/bin/bash"]
# Thu, 30 Jan 2025 14:32:57 GMT
RUN . /cachi2/cachi2.env &&     rm -rf /var/log/*
# Thu, 30 Jan 2025 14:32:57 GMT
LABEL "build-date"="2025-02-13T04:25:01" "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="c0546ad1ce412f8077a547cb8d0d68d04f08815c" "build-date"="2025-02-13T04:15:47Z" "release"="1739420147"
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
ENV JAVA_VERSION=jdk-11.0.26+4
# Thu, 30 Jan 2025 14:32:57 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='4ececb5c229763107e9e4acf3b7035db38cf18a98a47176fa5ed1be3f3d15518';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.26%2B4/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.26_4.tar.gz';          ;;        ppc64le)          ESUM='69b38f0dde128d8c606012335cd60f1f55afa09b4135582188943bee699ebf03';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.26%2B4/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.26_4.tar.gz';          ;;        s390x)          ESUM='5d9552b1fb699da6052cbd600e750dd8ff48a89a384d537919a3c999257979dc';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.26%2B4/OpenJDK11U-jre_s390x_linux_hotspot_11.0.26_4.tar.gz';          ;;        x86_64)          ESUM='d26c566a7010d1303d3979b6f076e7911b49419a609c9e4d81f27262bf47f87c';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.26%2B4/OpenJDK11U-jre_x64_linux_hotspot_11.0.26_4.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz; # buildkit
# Thu, 30 Jan 2025 14:32:57 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 30 Jan 2025 14:32:57 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 30 Jan 2025 14:32:57 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
```

-	Layers:
	-	`sha256:56631da24b0de345717238daea2e3e61c768d081572916ae06b08b19126a740d`  
		Last Modified: Thu, 13 Feb 2025 06:13:39 GMT  
		Size: 37.6 MB (37626059 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5aee836c3728069e82153bf7b209c409d3343adaea6ab6b31546e5ce09250db5`  
		Last Modified: Thu, 13 Feb 2025 06:13:36 GMT  
		Size: 460.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d886f1d0418fbd67439d630adb0cd82ab5ccf9bc0d3c039cbd36d622e8eaa96`  
		Last Modified: Fri, 14 Feb 2025 04:27:18 GMT  
		Size: 37.4 MB (37436415 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fd1fcfa2c04a9f82d48afd01b85c6838e3df6834e13b9b517852aa392d74451`  
		Last Modified: Fri, 14 Feb 2025 01:09:02 GMT  
		Size: 42.6 MB (42585864 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de77fcaac8ab18175dae8ebe55e16e459cfca8454e6313f9ca53cbc2f38304ea`  
		Last Modified: Fri, 14 Feb 2025 01:09:00 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef4135f486d6c8796c9d3828c83e53797d3585ea13e9ed291cd2d76d980e990e`  
		Last Modified: Fri, 14 Feb 2025 01:09:00 GMT  
		Size: 2.3 KB (2292 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:11-jre-ubi9-minimal` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:4a79e46ccb60d2c4dfcda8027a1ee17c6277c5bf4066d9a4eb05c24afe82a083
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3615499 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c2c9dec3c7c84dae0a0713422632531135c7c344338b6b2b0a5aaab1b68245b`

```dockerfile
```

-	Layers:
	-	`sha256:2bdf19e8b9df3abbab8be31fce415d175415795a07f97f101f3e40772339a4bc`  
		Last Modified: Fri, 14 Feb 2025 04:12:56 GMT  
		Size: 3.6 MB (3594639 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:581fcd268030091103bcadc611c5bc9beb98e8f409b92106326471b28ccc7055`  
		Last Modified: Fri, 14 Feb 2025 04:12:56 GMT  
		Size: 20.9 KB (20860 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-temurin:11-jre-ubi9-minimal` - linux; ppc64le

```console
$ docker pull eclipse-temurin@sha256:b6965c8bc4ad775d1f6d7229ee0ff5762a0dfa1c38709b8e8c9af4ca3f8ae25d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **123.0 MB (122975803 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a4143318ce1e2c3ea9834b3b8d5ae041aa7f42f9ebb75d1babd35486a565c99a`
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
COPY dir:2c0c7900d5f6c40d02b1787c7aed15027e6a404d210587076552b87add6a3c87 in / 
# Thu, 30 Jan 2025 14:32:57 GMT
COPY file:b37d593713ee21ad52a4cd1424dc019a24f7966f85df0ac4b86d234302695328 in /etc/yum.repos.d/. 
# Thu, 30 Jan 2025 14:32:57 GMT
CMD ["/bin/bash"]
# Thu, 30 Jan 2025 14:32:57 GMT
RUN . /cachi2/cachi2.env &&     rm -rf /var/log/*
# Thu, 30 Jan 2025 14:32:57 GMT
LABEL "build-date"="2025-02-13T04:27:14" "architecture"="ppc64le" "vcs-type"="git" "vcs-ref"="c0546ad1ce412f8077a547cb8d0d68d04f08815c" "build-date"="2025-02-13T04:15:47Z" "release"="1739420147"
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
ENV JAVA_VERSION=jdk-11.0.26+4
# Thu, 30 Jan 2025 14:32:57 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='4ececb5c229763107e9e4acf3b7035db38cf18a98a47176fa5ed1be3f3d15518';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.26%2B4/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.26_4.tar.gz';          ;;        ppc64le)          ESUM='69b38f0dde128d8c606012335cd60f1f55afa09b4135582188943bee699ebf03';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.26%2B4/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.26_4.tar.gz';          ;;        s390x)          ESUM='5d9552b1fb699da6052cbd600e750dd8ff48a89a384d537919a3c999257979dc';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.26%2B4/OpenJDK11U-jre_s390x_linux_hotspot_11.0.26_4.tar.gz';          ;;        x86_64)          ESUM='d26c566a7010d1303d3979b6f076e7911b49419a609c9e4d81f27262bf47f87c';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.26%2B4/OpenJDK11U-jre_x64_linux_hotspot_11.0.26_4.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz; # buildkit
# Thu, 30 Jan 2025 14:32:57 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 30 Jan 2025 14:32:57 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 30 Jan 2025 14:32:57 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
```

-	Layers:
	-	`sha256:9e6b2a031935c86976201f383962f66d759b1c458d46f7f8db9cd32663dd945f`  
		Last Modified: Thu, 13 Feb 2025 06:13:41 GMT  
		Size: 43.8 MB (43777674 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f65b64183df0b784e7e5f8c0c986254fe70af80954963d80c5fa6ab3c2e153af`  
		Last Modified: Thu, 13 Feb 2025 06:13:37 GMT  
		Size: 460.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8145a963593a244638406fe09abc4846c151008fbc794c259f3023bea468137`  
		Last Modified: Fri, 14 Feb 2025 00:28:47 GMT  
		Size: 39.5 MB (39470783 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad5460a284f9fee95fbda5a8ac194bdf467b74ecb009518e37802e226df0fdf3`  
		Last Modified: Fri, 14 Feb 2025 00:32:10 GMT  
		Size: 39.7 MB (39724466 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b488c48714637c7e9618b67501a86c230434a3540837b47c241c990da42fb36`  
		Last Modified: Fri, 14 Feb 2025 00:32:08 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f18357c706bbdba8054a80f7746f3c8d7f93fb99c25efa1415034c0cd807f943`  
		Last Modified: Fri, 14 Feb 2025 00:32:08 GMT  
		Size: 2.3 KB (2292 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:11-jre-ubi9-minimal` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:ef7d6074348467794c241d366cf168c1130ef8b15255f1f381edaea62a8f05bd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3615461 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d8082f5cf46134fb661decff9b0913cdf5b8618a62bd01181894ffe5395ba82`

```dockerfile
```

-	Layers:
	-	`sha256:a180eb1028d277a00516189dde6918f13d9087015e1e65620a3d85eabd4b3e7d`  
		Last Modified: Fri, 14 Feb 2025 04:12:58 GMT  
		Size: 3.6 MB (3594674 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fedbdb3efd47d31f103de0ac632464dc4addcd59a1884f02f2c1a32b9ad0b84e`  
		Last Modified: Fri, 14 Feb 2025 04:12:58 GMT  
		Size: 20.8 KB (20787 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-temurin:11-jre-ubi9-minimal` - linux; s390x

```console
$ docker pull eclipse-temurin@sha256:3755a28a3a2c8033142ff9be3878fea9128749739788883697a7c3b6fb10f489
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **112.3 MB (112324658 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d38edee5234e98c043f27fd3e46b9f1f3e0ddfa0a0c351734e81f28344039e5f`
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
COPY dir:86825579d6c6c7e4802643396fb14124acbbf3b24f22947be66f890a734b7e7b in / 
# Thu, 30 Jan 2025 14:32:57 GMT
COPY file:b37d593713ee21ad52a4cd1424dc019a24f7966f85df0ac4b86d234302695328 in /etc/yum.repos.d/. 
# Thu, 30 Jan 2025 14:32:57 GMT
CMD ["/bin/bash"]
# Thu, 30 Jan 2025 14:32:57 GMT
RUN . /cachi2/cachi2.env &&     rm -rf /var/log/*
# Thu, 30 Jan 2025 14:32:57 GMT
LABEL "build-date"="2025-02-06T04:49:32" "architecture"="s390x" "vcs-type"="git" "vcs-ref"="adfffabe9acacc27d15fc0ceb8e083254ca7b450" "build-date"="2025-02-06T04:39:35Z" "release"="1738816775"
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
ENV JAVA_VERSION=jdk-11.0.26+4
# Thu, 30 Jan 2025 14:32:57 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='4ececb5c229763107e9e4acf3b7035db38cf18a98a47176fa5ed1be3f3d15518';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.26%2B4/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.26_4.tar.gz';          ;;        ppc64le)          ESUM='69b38f0dde128d8c606012335cd60f1f55afa09b4135582188943bee699ebf03';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.26%2B4/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.26_4.tar.gz';          ;;        s390x)          ESUM='5d9552b1fb699da6052cbd600e750dd8ff48a89a384d537919a3c999257979dc';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.26%2B4/OpenJDK11U-jre_s390x_linux_hotspot_11.0.26_4.tar.gz';          ;;        x86_64)          ESUM='d26c566a7010d1303d3979b6f076e7911b49419a609c9e4d81f27262bf47f87c';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.26%2B4/OpenJDK11U-jre_x64_linux_hotspot_11.0.26_4.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz; # buildkit
# Thu, 30 Jan 2025 14:32:57 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 30 Jan 2025 14:32:57 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 30 Jan 2025 14:32:57 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
```

-	Layers:
	-	`sha256:dff3dae8634485c4d1f14243b55a740b473ee901b87cfd847a4234dc5a1b876d`  
		Last Modified: Thu, 06 Feb 2025 07:04:17 GMT  
		Size: 37.5 MB (37509515 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8ba975a618e9922cb358fe027051fa5621498ddb470d175378812c757e5d91c`  
		Last Modified: Thu, 06 Feb 2025 07:04:18 GMT  
		Size: 461.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86a94d5be3d999c406cf4b6c9139018b7dc00cef5387313637ff1e80cd68cb67`  
		Last Modified: Fri, 07 Feb 2025 05:30:50 GMT  
		Size: 37.0 MB (37004700 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8beaf4c8bcdd455da0d00e1faf0c06793f4f0c79b30c7f285a81eb787f10891e`  
		Last Modified: Sat, 08 Feb 2025 00:49:24 GMT  
		Size: 37.8 MB (37807564 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ef5225476660135db3b50ddb084d7f0ec10738a1cc8a3850d496eb0607edde7`  
		Last Modified: Fri, 07 Feb 2025 01:47:52 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:102e9cebd51d9f3ae39402a96e9beca54939657ef35b1529257c026aa1de2d07`  
		Last Modified: Sat, 08 Feb 2025 00:49:22 GMT  
		Size: 2.3 KB (2290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:11-jre-ubi9-minimal` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:f7faa5651944bf4a8c83fc65100d33125445680385ba5fe5fa70e278f956673d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3607190 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b55c95663630483a2cf556ec1e364bb81e7d9c8fa9d093053c1bc032aa90c94c`

```dockerfile
```

-	Layers:
	-	`sha256:d43dbc0febed1c20fb54326221d68ebf96dfe5b3cd82ea37f3f3c086690da289`  
		Last Modified: Fri, 07 Feb 2025 08:53:21 GMT  
		Size: 3.6 MB (3586433 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cb5aa27cbfee6ef8e02ee1c59db813c08d7a325138760d0eac8ed2fe96b6dcb1`  
		Last Modified: Sat, 08 Feb 2025 00:49:27 GMT  
		Size: 20.8 KB (20757 bytes)  
		MIME: application/vnd.in-toto+json
