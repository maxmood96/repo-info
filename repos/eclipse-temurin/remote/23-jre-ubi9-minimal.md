## `eclipse-temurin:23-jre-ubi9-minimal`

```console
$ docker pull eclipse-temurin@sha256:2e78333cd0a05c91f7559b37ee039b1dfc1d71777d578afa0cb95518c016d8c8
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
$ docker pull eclipse-temurin@sha256:edc97ea9bea19bd7a13fb506a4833324f1e8989a9bc7861e34f25bcdb7ef5bdf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **129.4 MB (129387056 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b6118e0d0b287a63e199e8ee2baffd4a3ccc1c84fe7f4068cd1e647b4b82d33`
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
COPY dir:ca56c4399f153561fdce7628edce358895393e72057424065cc9920dd3bc2dfc in / 
# Wed, 23 Oct 2024 15:41:32 GMT
COPY file:b37d593713ee21ad52a4cd1424dc019a24f7966f85df0ac4b86d234302695328 in /etc/yum.repos.d/. 
# Wed, 23 Oct 2024 15:41:32 GMT
CMD ["/bin/bash"]
# Wed, 23 Oct 2024 15:41:32 GMT
RUN . /cachi2/cachi2.env &&     rm -rf /var/log/*
# Wed, 23 Oct 2024 15:41:32 GMT
LABEL "build-date"="2025-01-09T06:40:34" "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="98c9e4c67f5f2dfc85d12e0f1fd70b809f2a3132" "build-date"="2025-01-09T06:29:15Z" "release"="1736404155"
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
	-	`sha256:eeaa3613f51c4b5b7fcccfbff65d07d2d2db56a76e38e2e028020458a3016d3b`  
		Last Modified: Tue, 14 Jan 2025 20:37:28 GMT  
		Size: 39.4 MB (39432422 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5808a11b7bed4fb0f4e0161a315ca539c1c940faabe1402029784919a7dc4599`  
		Last Modified: Tue, 14 Jan 2025 20:34:08 GMT  
		Size: 400.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef492d72f74376cb4285f966371cb7828a21c3c695c962d377d687bfaa176ecb`  
		Last Modified: Tue, 14 Jan 2025 21:56:15 GMT  
		Size: 37.0 MB (36989476 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e08d209a97dc4f43fda88733c2d2eee1dd18389b388101d4cf6cab22e8f7c3f3`  
		Last Modified: Sat, 11 Jan 2025 02:29:57 GMT  
		Size: 53.0 MB (52962339 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35f9a9b987c2632ca9e22bae2719b36612f69b501433bc1e74434f976560eee8`  
		Last Modified: Sat, 11 Jan 2025 02:29:56 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:274166ff0557b15a5437d290ac8b579eafe1d8a3763ecb16b91c798c538fc35a`  
		Last Modified: Tue, 14 Jan 2025 21:55:02 GMT  
		Size: 2.3 KB (2291 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:23-jre-ubi9-minimal` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:14129527b887fb625f265289cc350be23f09e1234e96342453a2d2446235d3cb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3606877 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2879d9dd9e073cbdd755aeacc328e48e1d68ead0dba2ea06b71caf312d08c4b6`

```dockerfile
```

-	Layers:
	-	`sha256:13c40516b5e8a685ba7406294d795ec84d2c370a9807709d249762ee6a9cf7f1`  
		Last Modified: Sat, 11 Jan 2025 02:29:56 GMT  
		Size: 3.6 MB (3586065 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7c9ca4b2885122f10e2424815db7d5ea33cd825cbe330e62388a107f6298e4f0`  
		Last Modified: Sat, 11 Jan 2025 02:29:56 GMT  
		Size: 20.8 KB (20812 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-temurin:23-jre-ubi9-minimal` - linux; arm64 variant v8

```console
$ docker pull eclipse-temurin@sha256:c61b0201f7751d3e0e7138f6f00050e7c632a7dec3ecd6045a5ab397256101bc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.0 MB (127000835 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c0d6c7380c4e32f4c25eb3e22e2659c623c7c1c5c098581811da423cce7fc081`
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
COPY dir:a2d26ebdf33d503cef16329462fc71203b97f5498da2b33d90e85b40b7a5617a in / 
# Wed, 23 Oct 2024 15:41:32 GMT
COPY file:b37d593713ee21ad52a4cd1424dc019a24f7966f85df0ac4b86d234302695328 in /etc/yum.repos.d/. 
# Wed, 23 Oct 2024 15:41:32 GMT
CMD ["/bin/bash"]
# Wed, 23 Oct 2024 15:41:32 GMT
RUN . /cachi2/cachi2.env &&     rm -rf /var/log/*
# Wed, 23 Oct 2024 15:41:32 GMT
LABEL "build-date"="2025-01-09T06:39:36" "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="98c9e4c67f5f2dfc85d12e0f1fd70b809f2a3132" "build-date"="2025-01-09T06:29:15Z" "release"="1736404155"
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
	-	`sha256:993bfc176cd8d0372914aae800decf36d6fd3b827bddcc23db1ade8868617a10`  
		Last Modified: Tue, 14 Jan 2025 20:48:48 GMT  
		Size: 37.6 MB (37577421 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9200dd396fa930ba9b5e574dd1a7a802d293946384b1287a63757a8458d18bb`  
		Last Modified: Tue, 14 Jan 2025 20:48:45 GMT  
		Size: 400.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0fa58217e45d8c73add5161d30458971a85903091e2941eecf4af13cf21c3bb9`  
		Last Modified: Tue, 14 Jan 2025 21:19:45 GMT  
		Size: 37.4 MB (37443828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c2c95f88ab92b1237207a0f6f63dc74771168a8f7da9e89363c302eadd28923`  
		Last Modified: Sat, 11 Jan 2025 01:38:41 GMT  
		Size: 52.0 MB (51976768 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15e58c3cc7ea6b9f1f41dc2dace0a1bd8f20664f37ee18b1f82eab0150a7f6ee`  
		Last Modified: Sat, 11 Jan 2025 01:38:40 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41644386e0c7eb5c1209f76187a9dae1595934e8b1c12efe7f49ee87736e158c`  
		Last Modified: Wed, 15 Jan 2025 10:33:33 GMT  
		Size: 2.3 KB (2290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:23-jre-ubi9-minimal` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:04ef890365b33894b8171edb824eb670cbdbd88e0a7a1ab45536c38f528532fe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3605540 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e2c3ee1181da2e8e28d1a2e876516a2364da0ff0e53717b17b7521153d7ea8c`

```dockerfile
```

-	Layers:
	-	`sha256:9948f1f94309757944cac64090947c98b2533ad3f8acc59116a0c3f53471eae0`  
		Last Modified: Sat, 11 Jan 2025 01:38:40 GMT  
		Size: 3.6 MB (3584623 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0d38d16384d0348d91877d4cf35a1e0964a73459bc4c44cd690a4c096cd2840c`  
		Last Modified: Sat, 11 Jan 2025 01:38:40 GMT  
		Size: 20.9 KB (20917 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-temurin:23-jre-ubi9-minimal` - linux; ppc64le

```console
$ docker pull eclipse-temurin@sha256:afb0cda94c9247bfda1b1476ed4ac73cdf4747301ab75419421a02110e69332c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **136.1 MB (136119038 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:36afea29b600cfd7d28af4397fb928464f9aa5bda59f48647afd3a0558aa8a5f`
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
COPY dir:d7227f71d224f4a0ce6e41e096c5f35be3bfb0d1cc57d5e656694dcabcc752aa in / 
# Wed, 23 Oct 2024 15:41:32 GMT
COPY file:b37d593713ee21ad52a4cd1424dc019a24f7966f85df0ac4b86d234302695328 in /etc/yum.repos.d/. 
# Wed, 23 Oct 2024 15:41:32 GMT
CMD ["/bin/bash"]
# Wed, 23 Oct 2024 15:41:32 GMT
RUN . /cachi2/cachi2.env &&     rm -rf /var/log/*
# Wed, 23 Oct 2024 15:41:32 GMT
LABEL "build-date"="2025-01-09T06:41:34" "architecture"="ppc64le" "vcs-type"="git" "vcs-ref"="98c9e4c67f5f2dfc85d12e0f1fd70b809f2a3132" "build-date"="2025-01-09T06:29:15Z" "release"="1736404155"
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
	-	`sha256:dce878563f15050dbee433ee11b302dc91caccb7bbf30b63a4d16c18ac4571ad`  
		Last Modified: Wed, 15 Jan 2025 01:00:14 GMT  
		Size: 43.8 MB (43794360 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35e8d75484ae7e9cfff00aa310d4197973e5e690156a92349511c158be98059f`  
		Last Modified: Wed, 15 Jan 2025 01:48:54 GMT  
		Size: 400.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18197cf46ebd87e4c786c45f34ea15620d00514afdc79daf54b112ed798a5efc`  
		Last Modified: Wed, 15 Jan 2025 01:00:12 GMT  
		Size: 39.5 MB (39476434 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5327b9321168fea8955936de450d0b3e5e7796b80436deee17d3fa60e6d1b643`  
		Last Modified: Sat, 11 Jan 2025 01:41:40 GMT  
		Size: 52.8 MB (52845426 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9de577b5cc2149366129dbfc95d199a5bb4febbdf26615efa677e7bcefe1042`  
		Last Modified: Sat, 11 Jan 2025 01:41:38 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dff545ee2b0a9f270d5d615e06bf418a085fc03464b2ee14d09db44780397a8b`  
		Last Modified: Sat, 11 Jan 2025 01:41:38 GMT  
		Size: 2.3 KB (2290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:23-jre-ubi9-minimal` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:7db913871ec279403d5b25005873916865735c15f175108b4c71c47b275420fe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3606113 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d800181c3927fbb08a0affbcf404a36fba0ab15e8cd8514014e24bfb46c3d16`

```dockerfile
```

-	Layers:
	-	`sha256:71f96132d1472b4d14f8eb00b48b233aa15444ed74190c1f185db4186638ecff`  
		Last Modified: Sat, 11 Jan 2025 01:41:39 GMT  
		Size: 3.6 MB (3585270 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5ed6e3a0399769673db101182939ec6621dd472aa52fa80da2a61ecde899c957`  
		Last Modified: Sat, 11 Jan 2025 01:41:38 GMT  
		Size: 20.8 KB (20843 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-temurin:23-jre-ubi9-minimal` - linux; s390x

```console
$ docker pull eclipse-temurin@sha256:f4884ba6056c505e3d1626774d6e2790b2be4dcda43c248fab80c13f37ad68a4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.0 MB (123984325 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4552677292a1ee3d783878e00624e5949dd209390bde43178166a92b786f6bd7`
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
COPY dir:ac9a6f98f459f2b182d154b46dbecb42555c6dd9f1103593ad7ba35ef49f1c66 in / 
# Wed, 23 Oct 2024 15:41:32 GMT
COPY file:b37d593713ee21ad52a4cd1424dc019a24f7966f85df0ac4b86d234302695328 in /etc/yum.repos.d/. 
# Wed, 23 Oct 2024 15:41:32 GMT
CMD ["/bin/bash"]
# Wed, 23 Oct 2024 15:41:32 GMT
RUN . /cachi2/cachi2.env &&     rm -rf /var/log/*
# Wed, 23 Oct 2024 15:41:32 GMT
LABEL "build-date"="2025-01-09T06:38:39" "architecture"="s390x" "vcs-type"="git" "vcs-ref"="98c9e4c67f5f2dfc85d12e0f1fd70b809f2a3132" "build-date"="2025-01-09T06:29:15Z" "release"="1736404155"
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
	-	`sha256:8ee56b4600df35f4679f31d612bb546f04a8c0ff236484b5c24d4beec3d209ff`  
		Last Modified: Thu, 09 Jan 2025 12:32:33 GMT  
		Size: 37.5 MB (37533310 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:168fa7af747923a20c9ccecc35d6f8ea158b325819f175b7fbc3590d84656a8a`  
		Last Modified: Thu, 09 Jan 2025 12:32:32 GMT  
		Size: 400.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a675f375cbacf7119aacbe8ef40ba25c801eee392e2f25776fea276c3252f817`  
		Last Modified: Wed, 15 Jan 2025 01:01:55 GMT  
		Size: 37.0 MB (37006874 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f413c7dfa9c9e92b9d80f973a8ee872431e777d19ff607f995d701e8f32463d6`  
		Last Modified: Sat, 11 Jan 2025 01:42:42 GMT  
		Size: 49.4 MB (49441323 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:856b89ead41b68bd44c58b92c6bd8dc3d6d3d9127d1b631755270ae55d4d0d42`  
		Last Modified: Sat, 11 Jan 2025 01:42:42 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ca52bc31bde2bd3f48f0ec9c72a6fd1099c48613844a63526fb2aac0d669d36`  
		Last Modified: Sat, 11 Jan 2025 01:42:42 GMT  
		Size: 2.3 KB (2290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:23-jre-ubi9-minimal` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:3b1f52e16ac4933004baa5de565c524d8f2ee7183fe9779852a48b892e08bf3e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3597870 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e49447d633bd9a61fced4377ea486cdee31e48bf4a63857f0020bba3fb51d8c5`

```dockerfile
```

-	Layers:
	-	`sha256:0149d7f178f4b6db8d2e9305875a982ca741d73cee69c99c4b158f84fd158c87`  
		Last Modified: Sat, 11 Jan 2025 01:42:41 GMT  
		Size: 3.6 MB (3577057 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:143e78ec3b9737b77f312807239ebb9cfff20f3a87d03c4c246b546051c25691`  
		Last Modified: Sat, 11 Jan 2025 01:42:41 GMT  
		Size: 20.8 KB (20813 bytes)  
		MIME: application/vnd.in-toto+json
