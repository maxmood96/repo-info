## `eclipse-temurin:23-jre-ubi9-minimal`

```console
$ docker pull eclipse-temurin@sha256:6272767cace61b132c112eff4a2c5c4bba5b83256be75e6295c58c384c993618
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

### `eclipse-temurin:23-jre-ubi9-minimal` - linux; amd64

```console
$ docker pull eclipse-temurin@sha256:1103755b019ec4d5c76224e051eeecda229520b11ddd0305cc87887069239a0b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **129.9 MB (129889318 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a1f06e8ee68a137019c41da29a64f1656fba7934d4f6b5d65af70616a3f04c6`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`

```dockerfile
# Wed, 23 Oct 2024 15:41:32 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 23 Oct 2024 15:41:32 GMT
LABEL vendor="Red Hat, Inc."
# Wed, 23 Oct 2024 15:41:32 GMT
LABEL url="https://www.redhat.com"
# Wed, 23 Oct 2024 15:41:32 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.5"       distribution-scope="public"
# Wed, 23 Oct 2024 15:41:32 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 23 Oct 2024 15:41:32 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Wed, 23 Oct 2024 15:41:32 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 23 Oct 2024 15:41:32 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 23 Oct 2024 15:41:32 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Wed, 23 Oct 2024 15:41:32 GMT
LABEL io.openshift.expose-services=""
# Wed, 23 Oct 2024 15:41:32 GMT
LABEL io.openshift.tags="minimal rhel9"
# Wed, 23 Oct 2024 15:41:32 GMT
ENV container oci
# Wed, 23 Oct 2024 15:41:32 GMT
COPY dir:45c667d4bed394050d06fa644ce9574d9fe75c2ed92a12e23fb5b733428b21f6 in / 
# Wed, 23 Oct 2024 15:41:32 GMT
COPY file:b37d593713ee21ad52a4cd1424dc019a24f7966f85df0ac4b86d234302695328 in /etc/yum.repos.d/. 
# Wed, 23 Oct 2024 15:41:32 GMT
CMD ["/bin/bash"]
# Wed, 23 Oct 2024 15:41:32 GMT
RUN . /cachi2/cachi2.env &&     rm -rf /var/log/*
# Wed, 23 Oct 2024 15:41:32 GMT
LABEL "build-date"="2024-11-13T17:20:39" "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="8389cd46e6826a07db9fbf425dd110900e32c6f9" "build-date"="2024-11-13T17:16:40Z" "release"="1731518200"
# Wed, 23 Oct 2024 15:41:32 GMT
RUN /bin/sh
# Wed, 23 Oct 2024 15:41:32 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 23 Oct 2024 15:41:32 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 23 Oct 2024 15:41:32 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 23 Oct 2024 15:41:32 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         fontconfig         glibc-langpack-en     ;     microdnf clean all # buildkit
# Wed, 23 Oct 2024 15:41:32 GMT
ENV JAVA_VERSION=jdk-23.0.1+11
# Wed, 23 Oct 2024 15:41:32 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='0b498a5b673cb50fe9cfd0a13bd39c7259b4fad4d930d614e1563aeb8bca7f0e';          BINARY_URL='https://github.com/adoptium/temurin23-binaries/releases/download/jdk-23.0.1%2B11/OpenJDK23U-jre_aarch64_linux_hotspot_23.0.1_11.tar.gz';          ;;        ppc64le)          ESUM='ae5d49932f7d9b182c2d9ededa18bd4defc61873f1d717caa3d905bba870a683';          BINARY_URL='https://github.com/adoptium/temurin23-binaries/releases/download/jdk-23.0.1%2B11/OpenJDK23U-jre_ppc64le_linux_hotspot_23.0.1_11.tar.gz';          ;;        s390x)          ESUM='d1d46933716a0eb5a6385980fa98c858c90e72bdc6d14b88d25b20980c5bc7f9';          BINARY_URL='https://github.com/adoptium/temurin23-binaries/releases/download/jdk-23.0.1%2B11/OpenJDK23U-jre_s390x_linux_hotspot_23.0.1_11.tar.gz';          ;;        x86_64)          ESUM='1233cbec40f05c76ad926b68521ae78c6ae4f454996ef549602be6987069fa77';          BINARY_URL='https://github.com/adoptium/temurin23-binaries/releases/download/jdk-23.0.1%2B11/OpenJDK23U-jre_x64_linux_hotspot_23.0.1_11.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -r "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Wed, 23 Oct 2024 15:41:32 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 23 Oct 2024 15:41:32 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 23 Oct 2024 15:41:32 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
```

-	Layers:
	-	`sha256:d2e5d6c907c71aea278da1e0e3424927afce03a253cba174efe5392fcba72b55`  
		Last Modified: Wed, 13 Nov 2024 18:56:52 GMT  
		Size: 39.9 MB (39871319 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7b6ec0388eddfe9b76df03c99092e0ca82d8a980895ea6ec4f7d925e674d7c5`  
		Last Modified: Wed, 13 Nov 2024 18:56:51 GMT  
		Size: 63.6 KB (63553 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7e3d0af7fd3a3c9d76910978e7075f83dd17f65249bd04508b2a5dcd9429058`  
		Last Modified: Thu, 14 Nov 2024 21:18:28 GMT  
		Size: 37.0 MB (36989722 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f6c9a67b326ef472d29d47843f437dd27cf7bb605f6869e329693ad47500d31`  
		Last Modified: Thu, 14 Nov 2024 21:18:28 GMT  
		Size: 53.0 MB (52962305 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3438b166bdd457fd355c4c1392e5f0bd8f7214e88ba0789f579df28a59f133ee`  
		Last Modified: Thu, 14 Nov 2024 21:18:27 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70725d41853ea4e143d7720b8dbf9c75d6f4fbb3df518e7eadddfe3dd7c24ffd`  
		Last Modified: Thu, 14 Nov 2024 21:18:27 GMT  
		Size: 2.3 KB (2291 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:23-jre-ubi9-minimal` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:e4f50414b134f92435ef9ef6745052770d0a763fcccff74a2058d4cd761d43b1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4740372 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:097d1d617734fc4d11402f2029e7596a2625201a90f1c067d198c7793b4a941c`

```dockerfile
```

-	Layers:
	-	`sha256:07c27f45e7e36088ca13a6f02b93e0016d48a492871ef37143e61d65b50065cc`  
		Last Modified: Thu, 14 Nov 2024 21:18:28 GMT  
		Size: 4.7 MB (4719549 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fa8d978cd5d74b884e143758272a4f806f47a75bd9290577d7aea787189729c0`  
		Last Modified: Thu, 14 Nov 2024 21:18:27 GMT  
		Size: 20.8 KB (20823 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-temurin:23-jre-ubi9-minimal` - linux; arm64 variant v8

```console
$ docker pull eclipse-temurin@sha256:c65a55a7112ac8e328371f9a487a4c975c8328297fa60ab7e6dd92276901d55d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.6 MB (127563831 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:862f5efca20351c0e4892906f82656d46ae3e55b803e01aaec7e909f1c5eaa2b`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`

```dockerfile
# Wed, 23 Oct 2024 15:41:32 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 23 Oct 2024 15:41:32 GMT
LABEL vendor="Red Hat, Inc."
# Wed, 23 Oct 2024 15:41:32 GMT
LABEL url="https://www.redhat.com"
# Wed, 23 Oct 2024 15:41:32 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.5"       distribution-scope="public"
# Wed, 23 Oct 2024 15:41:32 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 23 Oct 2024 15:41:32 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Wed, 23 Oct 2024 15:41:32 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 23 Oct 2024 15:41:32 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 23 Oct 2024 15:41:32 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Wed, 23 Oct 2024 15:41:32 GMT
LABEL io.openshift.expose-services=""
# Wed, 23 Oct 2024 15:41:32 GMT
LABEL io.openshift.tags="minimal rhel9"
# Wed, 23 Oct 2024 15:41:32 GMT
ENV container oci
# Wed, 23 Oct 2024 15:41:32 GMT
COPY dir:e27ddab6b88291890d801136d36e16fa6ad2af7f2a7e00f455a75bd89d96622f in / 
# Wed, 23 Oct 2024 15:41:32 GMT
COPY file:b37d593713ee21ad52a4cd1424dc019a24f7966f85df0ac4b86d234302695328 in /etc/yum.repos.d/. 
# Wed, 23 Oct 2024 15:41:32 GMT
CMD ["/bin/bash"]
# Wed, 23 Oct 2024 15:41:32 GMT
RUN . /cachi2/cachi2.env &&     rm -rf /var/log/*
# Wed, 23 Oct 2024 15:41:32 GMT
LABEL "build-date"="2024-11-13T17:24:29" "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="8389cd46e6826a07db9fbf425dd110900e32c6f9" "build-date"="2024-11-13T17:16:40Z" "release"="1731518200"
# Wed, 23 Oct 2024 15:41:32 GMT
RUN /bin/sh
# Wed, 23 Oct 2024 15:41:32 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 23 Oct 2024 15:41:32 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 23 Oct 2024 15:41:32 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 23 Oct 2024 15:41:32 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         fontconfig         glibc-langpack-en     ;     microdnf clean all # buildkit
# Wed, 23 Oct 2024 15:41:32 GMT
ENV JAVA_VERSION=jdk-23.0.1+11
# Wed, 23 Oct 2024 15:41:32 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='0b498a5b673cb50fe9cfd0a13bd39c7259b4fad4d930d614e1563aeb8bca7f0e';          BINARY_URL='https://github.com/adoptium/temurin23-binaries/releases/download/jdk-23.0.1%2B11/OpenJDK23U-jre_aarch64_linux_hotspot_23.0.1_11.tar.gz';          ;;        ppc64le)          ESUM='ae5d49932f7d9b182c2d9ededa18bd4defc61873f1d717caa3d905bba870a683';          BINARY_URL='https://github.com/adoptium/temurin23-binaries/releases/download/jdk-23.0.1%2B11/OpenJDK23U-jre_ppc64le_linux_hotspot_23.0.1_11.tar.gz';          ;;        s390x)          ESUM='d1d46933716a0eb5a6385980fa98c858c90e72bdc6d14b88d25b20980c5bc7f9';          BINARY_URL='https://github.com/adoptium/temurin23-binaries/releases/download/jdk-23.0.1%2B11/OpenJDK23U-jre_s390x_linux_hotspot_23.0.1_11.tar.gz';          ;;        x86_64)          ESUM='1233cbec40f05c76ad926b68521ae78c6ae4f454996ef549602be6987069fa77';          BINARY_URL='https://github.com/adoptium/temurin23-binaries/releases/download/jdk-23.0.1%2B11/OpenJDK23U-jre_x64_linux_hotspot_23.0.1_11.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -r "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Wed, 23 Oct 2024 15:41:32 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 23 Oct 2024 15:41:32 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 23 Oct 2024 15:41:32 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
```

-	Layers:
	-	`sha256:636ce8d23eab8a4456a354f6ee07a387ed3d02c854cfe9deacc58ab7259339bf`  
		Last Modified: Wed, 13 Nov 2024 19:37:14 GMT  
		Size: 38.1 MB (38073783 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce756de279cd0aa23acc884e1d32ccff7fef4582b5922432ba03c8fe651a180b`  
		Last Modified: Wed, 13 Nov 2024 19:37:13 GMT  
		Size: 63.6 KB (63602 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b840ae373448a46eb9b3959fa1d0b67dac5393295e5dee28898b93570675096`  
		Last Modified: Thu, 14 Nov 2024 21:55:38 GMT  
		Size: 37.4 MB (37447275 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a93a77137cc39ca72eb6b38b335de2c5b0e9ff98c12610dcb41464e3188eab9`  
		Last Modified: Thu, 14 Nov 2024 22:02:48 GMT  
		Size: 52.0 MB (51976757 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbe4211de0f3414560c3582ae82ff9eb3555b11fdf76b76e20d6bb1c70dd57f3`  
		Last Modified: Thu, 14 Nov 2024 22:02:46 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3c201d53f508d9a48fed00b48f68f269726df7f7ea8250aae5e7f9c8c033731`  
		Last Modified: Thu, 14 Nov 2024 22:02:46 GMT  
		Size: 2.3 KB (2288 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:23-jre-ubi9-minimal` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:a4febec3efa141ffc8b166a987c787f553145b805f995fe817d4a8ebc7bfd087
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4739117 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f5e3686704b3ed32a016110bac33599c51090b6359a608a1aa9ac7cc7dc6694e`

```dockerfile
```

-	Layers:
	-	`sha256:be521c16fd24f277f2a2b6e48c3de987ad1210112d203b14991fccbe3a96a54f`  
		Last Modified: Thu, 14 Nov 2024 22:02:47 GMT  
		Size: 4.7 MB (4718190 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:11869bfc3d56efe3b1cad578e9f58406274aa7c9c02fba6e74c5b4f29ef7f42d`  
		Last Modified: Thu, 14 Nov 2024 22:02:46 GMT  
		Size: 20.9 KB (20927 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-temurin:23-jre-ubi9-minimal` - linux; ppc64le

```console
$ docker pull eclipse-temurin@sha256:66a76c13ea7bd513062efb5e690812292c67d5a9a2f08d56d8a4eeb2c369cf82
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **136.7 MB (136729846 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8490f8f9fe2db63ea8d518fd9c155dd0e4754cbd9e98a7cc5104e66f4ddd26a8`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`

```dockerfile
# Wed, 23 Oct 2024 15:41:32 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 23 Oct 2024 15:41:32 GMT
LABEL vendor="Red Hat, Inc."
# Wed, 23 Oct 2024 15:41:32 GMT
LABEL url="https://www.redhat.com"
# Wed, 23 Oct 2024 15:41:32 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.5"       distribution-scope="public"
# Wed, 23 Oct 2024 15:41:32 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 23 Oct 2024 15:41:32 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Wed, 23 Oct 2024 15:41:32 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 23 Oct 2024 15:41:32 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 23 Oct 2024 15:41:32 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Wed, 23 Oct 2024 15:41:32 GMT
LABEL io.openshift.expose-services=""
# Wed, 23 Oct 2024 15:41:32 GMT
LABEL io.openshift.tags="minimal rhel9"
# Wed, 23 Oct 2024 15:41:32 GMT
ENV container oci
# Wed, 23 Oct 2024 15:41:32 GMT
COPY dir:6c2a5bc58c122f09d1fd3561f787b77c331815b22c12f8c67d609e22265d6d20 in / 
# Wed, 23 Oct 2024 15:41:32 GMT
COPY file:b37d593713ee21ad52a4cd1424dc019a24f7966f85df0ac4b86d234302695328 in /etc/yum.repos.d/. 
# Wed, 23 Oct 2024 15:41:32 GMT
CMD ["/bin/bash"]
# Wed, 23 Oct 2024 15:41:32 GMT
RUN . /cachi2/cachi2.env &&     rm -rf /var/log/*
# Wed, 23 Oct 2024 15:41:32 GMT
LABEL "build-date"="2024-11-13T18:14:04" "architecture"="ppc64le" "vcs-type"="git" "vcs-ref"="8389cd46e6826a07db9fbf425dd110900e32c6f9" "build-date"="2024-11-13T17:16:40Z" "release"="1731518200"
# Wed, 23 Oct 2024 15:41:32 GMT
RUN /bin/sh
# Wed, 23 Oct 2024 15:41:32 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 23 Oct 2024 15:41:32 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 23 Oct 2024 15:41:32 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 23 Oct 2024 15:41:32 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         fontconfig         glibc-langpack-en     ;     microdnf clean all # buildkit
# Wed, 23 Oct 2024 15:41:32 GMT
ENV JAVA_VERSION=jdk-23.0.1+11
# Wed, 23 Oct 2024 15:41:32 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='0b498a5b673cb50fe9cfd0a13bd39c7259b4fad4d930d614e1563aeb8bca7f0e';          BINARY_URL='https://github.com/adoptium/temurin23-binaries/releases/download/jdk-23.0.1%2B11/OpenJDK23U-jre_aarch64_linux_hotspot_23.0.1_11.tar.gz';          ;;        ppc64le)          ESUM='ae5d49932f7d9b182c2d9ededa18bd4defc61873f1d717caa3d905bba870a683';          BINARY_URL='https://github.com/adoptium/temurin23-binaries/releases/download/jdk-23.0.1%2B11/OpenJDK23U-jre_ppc64le_linux_hotspot_23.0.1_11.tar.gz';          ;;        s390x)          ESUM='d1d46933716a0eb5a6385980fa98c858c90e72bdc6d14b88d25b20980c5bc7f9';          BINARY_URL='https://github.com/adoptium/temurin23-binaries/releases/download/jdk-23.0.1%2B11/OpenJDK23U-jre_s390x_linux_hotspot_23.0.1_11.tar.gz';          ;;        x86_64)          ESUM='1233cbec40f05c76ad926b68521ae78c6ae4f454996ef549602be6987069fa77';          BINARY_URL='https://github.com/adoptium/temurin23-binaries/releases/download/jdk-23.0.1%2B11/OpenJDK23U-jre_x64_linux_hotspot_23.0.1_11.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -r "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Wed, 23 Oct 2024 15:41:32 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 23 Oct 2024 15:41:32 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 23 Oct 2024 15:41:32 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
```

-	Layers:
	-	`sha256:68f9d27ca5ac31d5c0ec42759a142541ceb9cec644f734c3a9e0bcf6cbfc705c`  
		Last Modified: Thu, 14 Nov 2024 00:15:06 GMT  
		Size: 44.3 MB (44340470 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ec943cf70fba3160f966d46cdde1b9fce3e5b1924ead0008cface91354effac`  
		Last Modified: Thu, 14 Nov 2024 00:15:05 GMT  
		Size: 63.6 KB (63571 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72bcc9b1511e3e1fb956bc42694740f0ec50e8f1bb1d5b76848d9c232da2a240`  
		Last Modified: Thu, 14 Nov 2024 22:04:35 GMT  
		Size: 39.5 MB (39477961 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b8dd3647c4b94dd615c35d1c09be84bc1e6c1138075c406daed360c0938dda7`  
		Last Modified: Thu, 14 Nov 2024 22:17:07 GMT  
		Size: 52.8 MB (52845425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce31ee820abdf4823e1a706f58f92c305a0d02dc350c925f72a54504e81a0176`  
		Last Modified: Thu, 14 Nov 2024 22:17:05 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98ddda73612dd5e99be8a19d94a09bb9dc34b06b7260302f50d5edec9c07d0a7`  
		Last Modified: Thu, 14 Nov 2024 22:17:05 GMT  
		Size: 2.3 KB (2291 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:23-jre-ubi9-minimal` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:3d23303d3f95137134c6ccc926216aa6d86ea818c04faa4797b4ab7de996dc3f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4739708 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c1de515437ecddf4ce929702c5aab595253ebb92c435e8aab3925c44eb998933`

```dockerfile
```

-	Layers:
	-	`sha256:a8bf43c270dd742d3bbace65c008783414116d34922c0d7399d04cf67cd90ee6`  
		Last Modified: Thu, 14 Nov 2024 22:17:06 GMT  
		Size: 4.7 MB (4718855 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:adbd913275878a5554456a0bace176c331b31cae3759da91a6f27290ad8f1d25`  
		Last Modified: Thu, 14 Nov 2024 22:17:05 GMT  
		Size: 20.9 KB (20853 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-temurin:23-jre-ubi9-minimal` - linux; s390x

```console
$ docker pull eclipse-temurin@sha256:83d22d0d49c70718607f61000ec321c26aebc4e53e10bb84397f9bf042bc0566
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.5 MB (124515707 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f0c19e5edbfc0cf2baf7ef6dcddf816dab49c8667aebb374d3cf41aecbea6263`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`

```dockerfile
# Wed, 23 Oct 2024 15:41:32 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 23 Oct 2024 15:41:32 GMT
LABEL vendor="Red Hat, Inc."
# Wed, 23 Oct 2024 15:41:32 GMT
LABEL url="https://www.redhat.com"
# Wed, 23 Oct 2024 15:41:32 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.5"       distribution-scope="public"
# Wed, 23 Oct 2024 15:41:32 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 23 Oct 2024 15:41:32 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Wed, 23 Oct 2024 15:41:32 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 23 Oct 2024 15:41:32 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 23 Oct 2024 15:41:32 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Wed, 23 Oct 2024 15:41:32 GMT
LABEL io.openshift.expose-services=""
# Wed, 23 Oct 2024 15:41:32 GMT
LABEL io.openshift.tags="minimal rhel9"
# Wed, 23 Oct 2024 15:41:32 GMT
ENV container oci
# Wed, 23 Oct 2024 15:41:32 GMT
COPY dir:ef726d13946d4bd75cbadb4155f1b5cc97b6ae23aeab850377a90a84c0910ffd in / 
# Wed, 23 Oct 2024 15:41:32 GMT
COPY file:b37d593713ee21ad52a4cd1424dc019a24f7966f85df0ac4b86d234302695328 in /etc/yum.repos.d/. 
# Wed, 23 Oct 2024 15:41:32 GMT
CMD ["/bin/bash"]
# Wed, 23 Oct 2024 15:41:32 GMT
RUN . /cachi2/cachi2.env &&     rm -rf /var/log/*
# Wed, 23 Oct 2024 15:41:32 GMT
LABEL "build-date"="2024-11-13T17:26:31" "architecture"="s390x" "vcs-type"="git" "vcs-ref"="8389cd46e6826a07db9fbf425dd110900e32c6f9" "build-date"="2024-11-13T17:16:40Z" "release"="1731518200"
# Wed, 23 Oct 2024 15:41:32 GMT
RUN /bin/sh
# Wed, 23 Oct 2024 15:41:32 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 23 Oct 2024 15:41:32 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 23 Oct 2024 15:41:32 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 23 Oct 2024 15:41:32 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         fontconfig         glibc-langpack-en     ;     microdnf clean all # buildkit
# Wed, 23 Oct 2024 15:41:32 GMT
ENV JAVA_VERSION=jdk-23.0.1+11
# Wed, 23 Oct 2024 15:41:32 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='0b498a5b673cb50fe9cfd0a13bd39c7259b4fad4d930d614e1563aeb8bca7f0e';          BINARY_URL='https://github.com/adoptium/temurin23-binaries/releases/download/jdk-23.0.1%2B11/OpenJDK23U-jre_aarch64_linux_hotspot_23.0.1_11.tar.gz';          ;;        ppc64le)          ESUM='ae5d49932f7d9b182c2d9ededa18bd4defc61873f1d717caa3d905bba870a683';          BINARY_URL='https://github.com/adoptium/temurin23-binaries/releases/download/jdk-23.0.1%2B11/OpenJDK23U-jre_ppc64le_linux_hotspot_23.0.1_11.tar.gz';          ;;        s390x)          ESUM='d1d46933716a0eb5a6385980fa98c858c90e72bdc6d14b88d25b20980c5bc7f9';          BINARY_URL='https://github.com/adoptium/temurin23-binaries/releases/download/jdk-23.0.1%2B11/OpenJDK23U-jre_s390x_linux_hotspot_23.0.1_11.tar.gz';          ;;        x86_64)          ESUM='1233cbec40f05c76ad926b68521ae78c6ae4f454996ef549602be6987069fa77';          BINARY_URL='https://github.com/adoptium/temurin23-binaries/releases/download/jdk-23.0.1%2B11/OpenJDK23U-jre_x64_linux_hotspot_23.0.1_11.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -r "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Wed, 23 Oct 2024 15:41:32 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 23 Oct 2024 15:41:32 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 23 Oct 2024 15:41:32 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
```

-	Layers:
	-	`sha256:92ea49de5d68e42d8be380cdbf37cd5d5a9cea20cf132e33742012d3864fd520`  
		Last Modified: Thu, 14 Nov 2024 00:14:58 GMT  
		Size: 38.0 MB (37998260 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b551c10007f8c2b0f7b6d7d03385dd5d0d30ec6059461a744884ddd2c58875a4`  
		Last Modified: Thu, 14 Nov 2024 00:14:57 GMT  
		Size: 63.5 KB (63550 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d095b66e2ef546d6102ea9a22a4a8ff2b59440db07ba44bb37d85c920bd41be`  
		Last Modified: Thu, 14 Nov 2024 22:44:18 GMT  
		Size: 37.0 MB (37010153 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7151b65ce849e831f9706279f09c475883b2ffc3294551af1d4b6371190ba92e`  
		Last Modified: Thu, 14 Nov 2024 22:53:51 GMT  
		Size: 49.4 MB (49441327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e037c1dc37ec0784c5264da93df41f1609b5976c6ba2781fb70d7afc0ca9d7b4`  
		Last Modified: Thu, 14 Nov 2024 22:53:51 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4646b05d4dfb0304efc6f1172d77ee93fced6665147ef46d9dad0d38eb8e967d`  
		Last Modified: Thu, 14 Nov 2024 22:53:51 GMT  
		Size: 2.3 KB (2291 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:23-jre-ubi9-minimal` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:dd2e7c9923385717c8f5627603fd619716b6fb11010b4230cf628cf18cd7b42b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4731435 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0203fcf14ea4d18d6701117d21bf46d164b5adec27f00742f430b6b9012129f3`

```dockerfile
```

-	Layers:
	-	`sha256:0a7c0978bd76cf1c37d5f5956e6a322020e0e214e9f297ebdd7c3270a12debc9`  
		Last Modified: Thu, 14 Nov 2024 22:53:51 GMT  
		Size: 4.7 MB (4710612 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cb2e367fba6f73f211a104418f8ee317ff6c4e77da1c083535d1b139e6d6fe07`  
		Last Modified: Thu, 14 Nov 2024 22:53:50 GMT  
		Size: 20.8 KB (20823 bytes)  
		MIME: application/vnd.in-toto+json
