## `eclipse-temurin:8u442-b06-jdk-ubi9-minimal`

```console
$ docker pull eclipse-temurin@sha256:ae246d9e0353f18e6424c9a9323e222209d2778e3b7c21a571928c14c0efaefc
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
$ docker pull eclipse-temurin@sha256:913d04a391833b44035a3032eee50d5fef8d2d66354607d08fd5c77481b30e78
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.2 MB (107172260 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:796ab77a1ebca10b1c3017a956269a5564430af71ef653ba90a77dde2f960bfa`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`

```dockerfile
# Thu, 13 Mar 2025 07:20:26 GMT
LABEL maintainer="Red Hat, Inc."
# Thu, 13 Mar 2025 07:20:26 GMT
LABEL vendor="Red Hat, Inc."
# Thu, 13 Mar 2025 07:20:26 GMT
LABEL url="https://www.redhat.com"
# Thu, 13 Mar 2025 07:20:26 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.5"       distribution-scope="public"
# Thu, 13 Mar 2025 07:20:26 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Thu, 13 Mar 2025 07:20:26 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Thu, 13 Mar 2025 07:20:27 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 13 Mar 2025 07:20:27 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 13 Mar 2025 07:20:27 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Thu, 13 Mar 2025 07:20:27 GMT
LABEL io.openshift.expose-services=""
# Thu, 13 Mar 2025 07:20:27 GMT
LABEL io.openshift.tags="minimal rhel9"
# Thu, 13 Mar 2025 07:20:27 GMT
ENV container oci
# Thu, 13 Mar 2025 07:20:27 GMT
COPY dir:15b23b07af120e2e0a5f4d490f44d738ca8fb631feddbf3564dd5d54104ea356 in / 
# Thu, 13 Mar 2025 07:20:27 GMT
COPY file:b37d593713ee21ad52a4cd1424dc019a24f7966f85df0ac4b86d234302695328 in /etc/yum.repos.d/. 
# Thu, 13 Mar 2025 07:20:27 GMT
CMD ["/bin/bash"]
# Thu, 13 Mar 2025 07:20:28 GMT
RUN . /cachi2/cachi2.env &&     rm -rf /var/log/*
# Thu, 13 Mar 2025 07:20:28 GMT
LABEL "build-date"="2025-03-13T07:20:00" "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="7865437f00d10c54ee1c3a6268b5ff65b38afba5" "build-date"="2025-03-13T07:15:09Z" "release"="1741850109"
# Thu, 13 Mar 2025 07:20:34 GMT
RUN /bin/sh
# Tue, 25 Mar 2025 17:58:27 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 25 Mar 2025 17:58:27 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 25 Mar 2025 17:58:27 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 25 Mar 2025 17:58:27 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en     ;     microdnf clean all # buildkit
# Tue, 25 Mar 2025 17:58:27 GMT
ENV JAVA_VERSION=jdk8u442-b06
# Tue, 25 Mar 2025 17:58:27 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='1d1662bd8ca7edc9281c723d9eebafea940e6a41464bdc43a83b564bc974c7e5';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u442-b06/OpenJDK8U-jdk_aarch64_linux_hotspot_8u442b06.tar.gz';          ;;        ppc64le)          ESUM='7eac77deb8fc6c6130f9445c9a68af0bcc40bf6736b5672ef5c3d737c025e84d';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u442-b06/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u442b06.tar.gz';          ;;        x86_64)          ESUM='5b0a0145e7790552a9c8767b4680074c4628ec276e5bb278b61d85cf90facafa';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u442-b06/OpenJDK8U-jdk_x64_linux_hotspot_8u442b06.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip; # buildkit
# Tue, 25 Mar 2025 17:58:27 GMT
RUN set -eux;     echo "Verifying install ...";     echo "javac -version"; javac -version;     echo "java -version"; java -version;     echo "Complete." # buildkit
# Tue, 25 Mar 2025 17:58:27 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 25 Mar 2025 17:58:27 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
```

-	Layers:
	-	`sha256:533b69cfd644e5f3e5bde1a8c302567c595a28af93b9318ac6a3e9394740fb4d`  
		Last Modified: Thu, 13 Mar 2025 08:27:55 GMT  
		Size: 39.4 MB (39359404 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:863e9a7e21028fb223595c360e0b25839f814e468af01725b95defa89bd29b53`  
		Last Modified: Thu, 13 Mar 2025 08:27:58 GMT  
		Size: 461.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13044d897508010517910d3ce6c9a3c6ddddd607f22b7ee1af33d1ac2e417421`  
		Last Modified: Tue, 25 Mar 2025 21:57:31 GMT  
		Size: 13.1 MB (13088218 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8124c3b0b4b417b209981b2afcb217bc45130a1694f2732641f1bfefccfb6352`  
		Last Modified: Tue, 25 Mar 2025 21:57:32 GMT  
		Size: 54.7 MB (54721732 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d0c36e77cf56851b7d27f56fdf04d694c63314b4afacc797ad003ad3bceb172`  
		Last Modified: Tue, 25 Mar 2025 21:57:31 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:612ea2d51464fb8c32619a964a2fa4d84080d11d3a483f2550717fe5618e0644`  
		Last Modified: Tue, 25 Mar 2025 21:57:31 GMT  
		Size: 2.3 KB (2316 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:8u442-b06-jdk-ubi9-minimal` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:0361a055cc8ed2d30940cfb79dcaa3e400b1f719de56ad1f4c1db4b14633057e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.9 MB (1859054 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f151bdb01c9e24b60b8ea3d175c02882bd023bcbd39a22586426afcf660e6ac`

```dockerfile
```

-	Layers:
	-	`sha256:37bf37b3e1c125988324854d8cb1a2e4b1f3e271f67665150439945beaf05a0c`  
		Last Modified: Tue, 25 Mar 2025 21:57:31 GMT  
		Size: 1.8 MB (1838398 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cd159a6734e43cff14c65e7f399e2c50cf3723be62b8abf63d2a587a1056489f`  
		Last Modified: Tue, 25 Mar 2025 21:57:31 GMT  
		Size: 20.7 KB (20656 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-temurin:8u442-b06-jdk-ubi9-minimal` - linux; arm64 variant v8

```console
$ docker pull eclipse-temurin@sha256:01c60c20334a7b243455860c2ae22379dbf87572958b556427e51c97cc19b956
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.0 MB (105041160 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd20ba4a0f4cafa08a3ba202c44ebc485098e6c212da503b0ce196f828547feb`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`

```dockerfile
# Thu, 13 Mar 2025 07:22:24 GMT
LABEL maintainer="Red Hat, Inc."
# Thu, 13 Mar 2025 07:22:24 GMT
LABEL vendor="Red Hat, Inc."
# Thu, 13 Mar 2025 07:22:24 GMT
LABEL url="https://www.redhat.com"
# Thu, 13 Mar 2025 07:22:24 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.5"       distribution-scope="public"
# Thu, 13 Mar 2025 07:22:24 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Thu, 13 Mar 2025 07:22:24 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Thu, 13 Mar 2025 07:22:24 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 13 Mar 2025 07:22:24 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 13 Mar 2025 07:22:24 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Thu, 13 Mar 2025 07:22:24 GMT
LABEL io.openshift.expose-services=""
# Thu, 13 Mar 2025 07:22:24 GMT
LABEL io.openshift.tags="minimal rhel9"
# Thu, 13 Mar 2025 07:22:24 GMT
ENV container oci
# Thu, 13 Mar 2025 07:22:25 GMT
COPY dir:b7138ac36fc7710c19e28655d453b8712ae774de42fbfc7d7975b03b9664b7ae in / 
# Thu, 13 Mar 2025 07:22:25 GMT
COPY file:b37d593713ee21ad52a4cd1424dc019a24f7966f85df0ac4b86d234302695328 in /etc/yum.repos.d/. 
# Thu, 13 Mar 2025 07:22:25 GMT
CMD ["/bin/bash"]
# Thu, 13 Mar 2025 07:22:25 GMT
RUN . /cachi2/cachi2.env &&     rm -rf /var/log/*
# Thu, 13 Mar 2025 07:22:26 GMT
LABEL "build-date"="2025-03-13T07:21:58" "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="7865437f00d10c54ee1c3a6268b5ff65b38afba5" "build-date"="2025-03-13T07:15:09Z" "release"="1741850109"
# Thu, 13 Mar 2025 07:22:36 GMT
RUN /bin/sh
# Tue, 25 Mar 2025 17:58:27 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 25 Mar 2025 17:58:27 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 25 Mar 2025 17:58:27 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 25 Mar 2025 17:58:27 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en     ;     microdnf clean all # buildkit
# Tue, 25 Mar 2025 17:58:27 GMT
ENV JAVA_VERSION=jdk8u442-b06
# Tue, 25 Mar 2025 17:58:27 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='1d1662bd8ca7edc9281c723d9eebafea940e6a41464bdc43a83b564bc974c7e5';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u442-b06/OpenJDK8U-jdk_aarch64_linux_hotspot_8u442b06.tar.gz';          ;;        ppc64le)          ESUM='7eac77deb8fc6c6130f9445c9a68af0bcc40bf6736b5672ef5c3d737c025e84d';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u442-b06/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u442b06.tar.gz';          ;;        x86_64)          ESUM='5b0a0145e7790552a9c8767b4680074c4628ec276e5bb278b61d85cf90facafa';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u442-b06/OpenJDK8U-jdk_x64_linux_hotspot_8u442b06.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip; # buildkit
# Tue, 25 Mar 2025 17:58:27 GMT
RUN set -eux;     echo "Verifying install ...";     echo "javac -version"; javac -version;     echo "java -version"; java -version;     echo "Complete." # buildkit
# Tue, 25 Mar 2025 17:58:27 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 25 Mar 2025 17:58:27 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
```

-	Layers:
	-	`sha256:8f0b1160a7bdb1abc6f59217ba0a1ed1eb53a9ddbbcaddd95d709604e095f742`  
		Last Modified: Thu, 13 Mar 2025 08:37:12 GMT  
		Size: 37.6 MB (37590719 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2e019691d61a0d5163ed02fe7a0cee4161254fd2d91b44221c46f8f765e011b`  
		Last Modified: Thu, 13 Mar 2025 08:37:13 GMT  
		Size: 459.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cecaa9a0e7b9e986580faf82cb0f61b4b374585587485ca9f2f92ea54752543`  
		Last Modified: Tue, 25 Mar 2025 21:57:40 GMT  
		Size: 13.6 MB (13624229 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4a30aae41bf12a58a64c093234453babc2ee4f2f6784b04cad233c00b03cf5e`  
		Last Modified: Tue, 25 Mar 2025 21:57:41 GMT  
		Size: 53.8 MB (53823311 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9eec133c81e85ac47a6c774f7a0c6f8813af8254b3826925eb22610bd3e782c1`  
		Last Modified: Tue, 25 Mar 2025 21:57:40 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:883152c2b92a03ea6912bbcf0a6cbedd2dd6b9bdf4972e64a0b9f3938f17e5fd`  
		Last Modified: Tue, 25 Mar 2025 21:57:39 GMT  
		Size: 2.3 KB (2316 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:8u442-b06-jdk-ubi9-minimal` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:6a8e45e3512800db37696b7d0dd55ba72c29e85e62b3d1d8e615206d9f92dce2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.9 MB (1860293 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a0400f7fec2ff6311ba9eac7cf1ee2abfae732d7087ee0b2ef6d73c389e3efa`

```dockerfile
```

-	Layers:
	-	`sha256:4cda00e37da2e18d2a5c5318be3fc41ca82d8f90066d364d07cc8e8ff0f11cd3`  
		Last Modified: Tue, 25 Mar 2025 21:57:40 GMT  
		Size: 1.8 MB (1839521 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fb64924610a2e6ff346421994e2a41445c3114b229d0c213059360d226f4af5c`  
		Last Modified: Tue, 25 Mar 2025 21:57:40 GMT  
		Size: 20.8 KB (20772 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-temurin:8u442-b06-jdk-ubi9-minimal` - linux; ppc64le

```console
$ docker pull eclipse-temurin@sha256:13d7853f067bfc8d70e17c4c7ac674c217ccf2abfddc549b53c4c16f6f85a0aa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **110.7 MB (110662892 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a8d6f5f288e588002386cd0735264aba545deebdbd28f573daecd27e5d82069b`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`

```dockerfile
# Thu, 13 Mar 2025 07:27:04 GMT
LABEL maintainer="Red Hat, Inc."
# Thu, 13 Mar 2025 07:27:04 GMT
LABEL vendor="Red Hat, Inc."
# Thu, 13 Mar 2025 07:27:04 GMT
LABEL url="https://www.redhat.com"
# Thu, 13 Mar 2025 07:27:04 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.5"       distribution-scope="public"
# Thu, 13 Mar 2025 07:27:04 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Thu, 13 Mar 2025 07:27:04 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Thu, 13 Mar 2025 07:27:04 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 13 Mar 2025 07:27:04 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 13 Mar 2025 07:27:04 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Thu, 13 Mar 2025 07:27:04 GMT
LABEL io.openshift.expose-services=""
# Thu, 13 Mar 2025 07:27:04 GMT
LABEL io.openshift.tags="minimal rhel9"
# Thu, 13 Mar 2025 07:27:04 GMT
ENV container oci
# Thu, 13 Mar 2025 07:27:05 GMT
COPY dir:2930069cafd499c2bb484a4452129437fee8075431fe0148ba9db5d528b083c7 in / 
# Thu, 13 Mar 2025 07:27:05 GMT
COPY file:b37d593713ee21ad52a4cd1424dc019a24f7966f85df0ac4b86d234302695328 in /etc/yum.repos.d/. 
# Thu, 13 Mar 2025 07:27:05 GMT
CMD ["/bin/bash"]
# Thu, 13 Mar 2025 07:27:05 GMT
RUN . /cachi2/cachi2.env &&     rm -rf /var/log/*
# Thu, 13 Mar 2025 07:27:06 GMT
LABEL "build-date"="2025-03-13T07:26:37" "architecture"="ppc64le" "vcs-type"="git" "vcs-ref"="7865437f00d10c54ee1c3a6268b5ff65b38afba5" "build-date"="2025-03-13T07:15:09Z" "release"="1741850109"
# Thu, 13 Mar 2025 07:28:01 GMT
RUN /bin/sh
# Tue, 25 Mar 2025 17:58:27 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 25 Mar 2025 17:58:27 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 25 Mar 2025 17:58:27 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 25 Mar 2025 17:58:27 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en     ;     microdnf clean all # buildkit
# Tue, 25 Mar 2025 17:58:27 GMT
ENV JAVA_VERSION=jdk8u442-b06
# Tue, 25 Mar 2025 17:58:27 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='1d1662bd8ca7edc9281c723d9eebafea940e6a41464bdc43a83b564bc974c7e5';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u442-b06/OpenJDK8U-jdk_aarch64_linux_hotspot_8u442b06.tar.gz';          ;;        ppc64le)          ESUM='7eac77deb8fc6c6130f9445c9a68af0bcc40bf6736b5672ef5c3d737c025e84d';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u442-b06/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u442b06.tar.gz';          ;;        x86_64)          ESUM='5b0a0145e7790552a9c8767b4680074c4628ec276e5bb278b61d85cf90facafa';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u442-b06/OpenJDK8U-jdk_x64_linux_hotspot_8u442b06.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip; # buildkit
# Tue, 25 Mar 2025 17:58:27 GMT
RUN set -eux;     echo "Verifying install ...";     echo "javac -version"; javac -version;     echo "java -version"; java -version;     echo "Complete." # buildkit
# Tue, 25 Mar 2025 17:58:27 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 25 Mar 2025 17:58:27 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
```

-	Layers:
	-	`sha256:45bd43bfc7accd96f346d44555dfd3c49fe61e223a5edc723f7e6e800686210b`  
		Last Modified: Thu, 13 Mar 2025 12:28:04 GMT  
		Size: 43.8 MB (43765030 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8dd5893f1906dca44bb5215e6c9cec6ab4d26c1be7354e08d4a40339ea1bd0ad`  
		Last Modified: Thu, 13 Mar 2025 12:28:03 GMT  
		Size: 459.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:914af573e0553dbd0d38d7286a66c85ce9c38d0316f769a5f0399abff06eab9e`  
		Last Modified: Tue, 25 Mar 2025 21:58:18 GMT  
		Size: 14.7 MB (14724882 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c94d695287aabf5d0339d73ea0df9541efa538519985cc188bd95f33c50d323b`  
		Last Modified: Tue, 25 Mar 2025 21:58:19 GMT  
		Size: 52.2 MB (52170076 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:033c4972239e3a10e2682e7881fbfd8ae61678c4a1d0442abbc65c9ed12a3100`  
		Last Modified: Tue, 25 Mar 2025 21:58:17 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a0cb2f80b7d06c701a2f3ce233ba29ae3b5011ed74d4fe15db1ba1766847b64`  
		Last Modified: Tue, 25 Mar 2025 21:58:17 GMT  
		Size: 2.3 KB (2316 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:8u442-b06-jdk-ubi9-minimal` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:69b4dd581e2388482866fab558403d43635bed133d8464edf9b32a5aec3d417f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.9 MB (1860012 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:35cbdef6036be19ebdf490f5916ac7e821f9ab3db0e7c6bdfe0741ba9b5f90d4`

```dockerfile
```

-	Layers:
	-	`sha256:2992c7f6b4b7f6f2ef56bef117cd72c917e37b1be10ebf44c141193c62c54480`  
		Last Modified: Tue, 25 Mar 2025 21:58:17 GMT  
		Size: 1.8 MB (1839320 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1b9d777ce8d7b13d941b9a87ad9fa6d040590a05b9752cf9736233a1870dcfc8`  
		Last Modified: Tue, 25 Mar 2025 21:58:17 GMT  
		Size: 20.7 KB (20692 bytes)  
		MIME: application/vnd.in-toto+json
