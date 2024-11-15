## `eclipse-temurin:11-jre-ubi9-minimal`

```console
$ docker pull eclipse-temurin@sha256:8680ea445b9b440c3c56816092c6638d56990614a477f444f6093641d8cc324f
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
$ docker pull eclipse-temurin@sha256:d031275db4d8922d78222a42eb1198833402534f13ba4b1f3849162ff6379011
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **121.2 MB (121157737 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c0967e1069f2c5122e54adc94584a3ab898f5c8de4192cd528bfe2517cebfe4d`
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
ENV JAVA_VERSION=jdk-11.0.25+9
# Wed, 23 Oct 2024 15:41:32 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='e37ba6636e31f3c9191ac7e3fd0ab7fb354a2f3b320d68bfb95efd1e053134c9';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.25%2B9/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.25_9.tar.gz';          ;;        ppc64le)          ESUM='7e7edaf34c29c304514d60f40f6c9ce58eb3e32b0dec20bb6ccd1cfbb4456698';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.25%2B9/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.25_9.tar.gz';          ;;        s390x)          ESUM='4ec884fe3874e258ae2253d535d3d92d6c313542fd973e8963c2eb87d68fb273';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.25%2B9/OpenJDK11U-jre_s390x_linux_hotspot_11.0.25_9.tar.gz';          ;;        x86_64)          ESUM='84cd7101f39172a4db085fb52940595bb14dad6bc3afb5bf82ee497eceaf86d3';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.25%2B9/OpenJDK11U-jre_x64_linux_hotspot_11.0.25_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -r "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
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
	-	`sha256:98178e12f6a2e470f90cecb151253a3a93ac338815b25ca9578ca971d9cf4c66`  
		Last Modified: Thu, 14 Nov 2024 21:18:11 GMT  
		Size: 37.0 MB (36989743 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfb1106393651f8572ffa2f99e76a546bed5a1b04078c0c0238d696f03a312f0`  
		Last Modified: Thu, 14 Nov 2024 21:18:12 GMT  
		Size: 44.2 MB (44230703 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd709fff324c77eabef91ce1d51c39939fb70791377cb599373f7e60713be665`  
		Last Modified: Thu, 14 Nov 2024 21:18:10 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5ac2a9f16ad78f1b93091e1f02a8abc7938e893b716e06428ad7cb53915b663`  
		Last Modified: Thu, 14 Nov 2024 21:18:10 GMT  
		Size: 2.3 KB (2291 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:11-jre-ubi9-minimal` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:b306e09a28b9731e25afacbe69287d515c8c9f9cc2621d9c5634831c45335929
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4749123 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:075800488bcecc5b569b8764b010fc41f1ed2228121de3923905ea2ce25ebc1f`

```dockerfile
```

-	Layers:
	-	`sha256:5ece5963c6a48e87bdcee1b9e421269ed67e6404bcc6c62a0e2b4778f0df6457`  
		Last Modified: Thu, 14 Nov 2024 21:18:11 GMT  
		Size: 4.7 MB (4728300 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7bb2cf214f2af5e6683fa8e7a8b9fd9029faf4fb0643c8ce89dcbc2ce7199a30`  
		Last Modified: Thu, 14 Nov 2024 21:18:10 GMT  
		Size: 20.8 KB (20823 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-temurin:11-jre-ubi9-minimal` - linux; arm64 variant v8

```console
$ docker pull eclipse-temurin@sha256:17cbcd165bf5082a7c10fb437dfc7255861761e8f08d9481a14393c64e67fa5c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **118.2 MB (118173633 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f8e74a04ff22dc318c6676fe1e31002b274e3d05861361273d4a314d03ccd25`
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
ENV JAVA_VERSION=jdk-11.0.25+9
# Wed, 23 Oct 2024 15:41:32 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='e37ba6636e31f3c9191ac7e3fd0ab7fb354a2f3b320d68bfb95efd1e053134c9';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.25%2B9/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.25_9.tar.gz';          ;;        ppc64le)          ESUM='7e7edaf34c29c304514d60f40f6c9ce58eb3e32b0dec20bb6ccd1cfbb4456698';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.25%2B9/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.25_9.tar.gz';          ;;        s390x)          ESUM='4ec884fe3874e258ae2253d535d3d92d6c313542fd973e8963c2eb87d68fb273';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.25%2B9/OpenJDK11U-jre_s390x_linux_hotspot_11.0.25_9.tar.gz';          ;;        x86_64)          ESUM='84cd7101f39172a4db085fb52940595bb14dad6bc3afb5bf82ee497eceaf86d3';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.25%2B9/OpenJDK11U-jre_x64_linux_hotspot_11.0.25_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -r "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
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
	-	`sha256:54043989883c318360d9fd46b1371c8b816b80326deb5f334fcd7e277a244341`  
		Last Modified: Thu, 14 Nov 2024 21:57:51 GMT  
		Size: 42.6 MB (42586556 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c4f1df8d8a7db91575883a44dd304dfcab73115ec9d72ca8a99304f335376f9`  
		Last Modified: Thu, 14 Nov 2024 21:57:49 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77b104bde030e8221554ae4c0d840a4d29e4fe6a166b788a8c7a2735ed7380a4`  
		Last Modified: Thu, 14 Nov 2024 21:57:49 GMT  
		Size: 2.3 KB (2290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:11-jre-ubi9-minimal` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:c6d436fe82c0a4dbdef50658a8f14df4dedc8428525129d12c913f4278e2bd73
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4749109 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b4e8d15810ad30ed460f62ef86c52b5ad968c43ea35b627882e5cb5c91b1fc90`

```dockerfile
```

-	Layers:
	-	`sha256:ff1b20b6c8c9c36fabe9e2b1b06356298fae62f33fb65882ddbdf0d945e269f9`  
		Last Modified: Thu, 14 Nov 2024 21:57:50 GMT  
		Size: 4.7 MB (4728182 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ea47dc902cbdad77b3725aa7bb44b7fadfc8674332540bf3533df9a9e60c7c14`  
		Last Modified: Thu, 14 Nov 2024 21:57:49 GMT  
		Size: 20.9 KB (20927 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-temurin:11-jre-ubi9-minimal` - linux; ppc64le

```console
$ docker pull eclipse-temurin@sha256:5aae8975453e05fe149539bc088481a00043b14e39bf5b08607cada448aa7ea5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **123.6 MB (123608501 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6aafb791bcc49e51ed2897d1e5b4c66ea33d8d40179a0779b8b0d98113fe74ab`
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
ENV JAVA_VERSION=jdk-11.0.25+9
# Wed, 23 Oct 2024 15:41:32 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='e37ba6636e31f3c9191ac7e3fd0ab7fb354a2f3b320d68bfb95efd1e053134c9';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.25%2B9/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.25_9.tar.gz';          ;;        ppc64le)          ESUM='7e7edaf34c29c304514d60f40f6c9ce58eb3e32b0dec20bb6ccd1cfbb4456698';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.25%2B9/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.25_9.tar.gz';          ;;        s390x)          ESUM='4ec884fe3874e258ae2253d535d3d92d6c313542fd973e8963c2eb87d68fb273';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.25%2B9/OpenJDK11U-jre_s390x_linux_hotspot_11.0.25_9.tar.gz';          ;;        x86_64)          ESUM='84cd7101f39172a4db085fb52940595bb14dad6bc3afb5bf82ee497eceaf86d3';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.25%2B9/OpenJDK11U-jre_x64_linux_hotspot_11.0.25_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -r "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
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
	-	`sha256:cf01078fb2f910cd7a9c69c23266324de6511dabfd18e7b13af55133cdddfb49`  
		Last Modified: Thu, 14 Nov 2024 22:08:06 GMT  
		Size: 39.7 MB (39724080 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87d5565defb475c681ebc191530ea0c88449ea09a55583f8a78b0648a1ea8666`  
		Last Modified: Thu, 14 Nov 2024 22:08:04 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca1d4a9d95b28fdccee4fd6a732850f43fe39f2aea4524b09003e3ae29cebe67`  
		Last Modified: Thu, 14 Nov 2024 22:08:04 GMT  
		Size: 2.3 KB (2291 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:11-jre-ubi9-minimal` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:fd51d405d04af6cf069ef555c1868bea18d59d648a5d1b54f13451a2a2eb582a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4749087 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6402f5fdf82c592a180e28e7a9512929a212df4fcb865564e5f743ca9e2bce24`

```dockerfile
```

-	Layers:
	-	`sha256:3bde10afc25de9f0bf4af78dc058c51f2a31b9527d68508026e1517a1e68f37d`  
		Last Modified: Thu, 14 Nov 2024 22:08:05 GMT  
		Size: 4.7 MB (4728234 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f6f0336d568907d6211f434fe67a2bbb2cdcda81bcefca9f71c981f1105f84bb`  
		Last Modified: Thu, 14 Nov 2024 22:08:04 GMT  
		Size: 20.9 KB (20853 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-temurin:11-jre-ubi9-minimal` - linux; s390x

```console
$ docker pull eclipse-temurin@sha256:cdb7be574e0c24c5d48608ca59b33038dab73f9edae64e98a19c3388ea97b90d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **112.9 MB (112883469 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30b0d675e774ba7b2292f192c9a1e52d42bdd5b735f7ad7b18bade966c2fdf20`
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
ENV JAVA_VERSION=jdk-11.0.25+9
# Wed, 23 Oct 2024 15:41:32 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='e37ba6636e31f3c9191ac7e3fd0ab7fb354a2f3b320d68bfb95efd1e053134c9';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.25%2B9/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.25_9.tar.gz';          ;;        ppc64le)          ESUM='7e7edaf34c29c304514d60f40f6c9ce58eb3e32b0dec20bb6ccd1cfbb4456698';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.25%2B9/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.25_9.tar.gz';          ;;        s390x)          ESUM='4ec884fe3874e258ae2253d535d3d92d6c313542fd973e8963c2eb87d68fb273';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.25%2B9/OpenJDK11U-jre_s390x_linux_hotspot_11.0.25_9.tar.gz';          ;;        x86_64)          ESUM='84cd7101f39172a4db085fb52940595bb14dad6bc3afb5bf82ee497eceaf86d3';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.25%2B9/OpenJDK11U-jre_x64_linux_hotspot_11.0.25_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -r "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
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
	-	`sha256:4737cbcdd6bbb6a65ea9a1324efaa2acc2df19a2c9ca55e24180a2d7aa653f9a`  
		Last Modified: Thu, 14 Nov 2024 22:45:34 GMT  
		Size: 37.8 MB (37809087 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3a04a148bbc818d04e3395ee0da0efc649df0128c28205f775efe4f1881e011`  
		Last Modified: Thu, 14 Nov 2024 22:45:33 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90d2ab13e4b7953c3dbe91fd04868d9c9db738b6cbb2858bfaf145e36c642852`  
		Last Modified: Thu, 14 Nov 2024 22:45:33 GMT  
		Size: 2.3 KB (2292 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:11-jre-ubi9-minimal` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:590a85c229c25578f1f6a8f5aa8c4edfcb7c47205a86cbbcbdda593ee3f05c18
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4740814 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:78dfbac73876e93cad637045287a1bb36ce6b338f0d82fa5c7bf0b76a6556dc1`

```dockerfile
```

-	Layers:
	-	`sha256:447370763266b4f6ec9e4f62963b98c900b674b9b16c871730211f5d0eb5f3cb`  
		Last Modified: Thu, 14 Nov 2024 22:45:33 GMT  
		Size: 4.7 MB (4719991 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ace08054f70a51f3116bd8ec28c400f8c95c22ad790bcc208f76e96aaa996a50`  
		Last Modified: Thu, 14 Nov 2024 22:45:33 GMT  
		Size: 20.8 KB (20823 bytes)  
		MIME: application/vnd.in-toto+json
