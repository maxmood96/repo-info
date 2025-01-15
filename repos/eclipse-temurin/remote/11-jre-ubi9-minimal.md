## `eclipse-temurin:11-jre-ubi9-minimal`

```console
$ docker pull eclipse-temurin@sha256:a32a31b9bf3f97d8291a7db22ee99e924c5e8c0fb192cb810b7d4e5db3302f83
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
$ docker pull eclipse-temurin@sha256:b3d4267aaa62459476a0a1de0d3ea65092ca63e8dc0e969d55794657bea63eaf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **120.7 MB (120653476 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e063458affd4fe8313f98070f671b8c553752e23339fe31ded90676e5d65451`
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
	-	`sha256:eeaa3613f51c4b5b7fcccfbff65d07d2d2db56a76e38e2e028020458a3016d3b`  
		Last Modified: Thu, 09 Jan 2025 07:47:12 GMT  
		Size: 39.4 MB (39432422 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5808a11b7bed4fb0f4e0161a315ca539c1c940faabe1402029784919a7dc4599`  
		Last Modified: Tue, 14 Jan 2025 20:34:08 GMT  
		Size: 400.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d055bad7813338a64df60f0c110e612ad74274d61b0d4a9a576722527e7f39d`  
		Last Modified: Sat, 11 Jan 2025 01:29:10 GMT  
		Size: 37.0 MB (36987538 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2cbe4906dabbfe6a7f01a3814a3e442f4e4dfb9e6bdb0eb63b5ab699add81d35`  
		Last Modified: Tue, 14 Jan 2025 20:59:59 GMT  
		Size: 44.2 MB (44230699 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6168a67dbf0f3b18e3bad0f862c981921eceb8ed80e0331295de5667d98a9b3f`  
		Last Modified: Sat, 11 Jan 2025 01:29:10 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6932d229ded6655fcede8ccaba81b12ac8f45b23f1e08d21f4ba5c508c18cdeb`  
		Last Modified: Tue, 14 Jan 2025 21:21:23 GMT  
		Size: 2.3 KB (2291 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:11-jre-ubi9-minimal` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:b90e071d530b3ea526945d772ba02441ce501282d6d348d782cf4bc3c66884a6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3615614 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c9e3fcfab81d5b87c31ae441a5e48004afc7b233ae904362ec2debd0614dd77c`

```dockerfile
```

-	Layers:
	-	`sha256:8747df2ac22c677cc7af67ef3c88a24269a5ce51bad5f01828301c9ef4b910e7`  
		Last Modified: Sat, 11 Jan 2025 01:29:10 GMT  
		Size: 3.6 MB (3594802 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:40f794348cb6fd33cc5c431d4e8b26d325d5980e6953ebb66f0a9cacdff6942f`  
		Last Modified: Wed, 15 Jan 2025 01:01:23 GMT  
		Size: 20.8 KB (20812 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-temurin:11-jre-ubi9-minimal` - linux; arm64 variant v8

```console
$ docker pull eclipse-temurin@sha256:4f12cb6bccdb3a13477cd3b47d871c00d369068be43e1337156dfb1b30f9e018
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **117.6 MB (117610639 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:620002249118beeeab47e9d26ca92936810bcf3bc04dbdd27c90ca932c4bf89d`
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
	-	`sha256:993bfc176cd8d0372914aae800decf36d6fd3b827bddcc23db1ade8868617a10`  
		Last Modified: Tue, 14 Jan 2025 20:48:48 GMT  
		Size: 37.6 MB (37577421 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9200dd396fa930ba9b5e574dd1a7a802d293946384b1287a63757a8458d18bb`  
		Last Modified: Thu, 09 Jan 2025 07:47:11 GMT  
		Size: 400.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0fa58217e45d8c73add5161d30458971a85903091e2941eecf4af13cf21c3bb9`  
		Last Modified: Sat, 11 Jan 2025 01:33:38 GMT  
		Size: 37.4 MB (37443828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e704cadde093ce772a73b8b3727ad5366b9ec22a6f5b950e86181526a71b275c`  
		Last Modified: Sat, 11 Jan 2025 01:35:11 GMT  
		Size: 42.6 MB (42586572 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff7aded5784bdda813ae2f6aa77e9d7150e5e9fbda43678e9a4a1611c5866079`  
		Last Modified: Sat, 11 Jan 2025 01:35:10 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67394fed0bb3c31997e0d04522df2ebb89cb284b66117d08ae94445c65a03791`  
		Last Modified: Sat, 11 Jan 2025 01:35:10 GMT  
		Size: 2.3 KB (2292 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:11-jre-ubi9-minimal` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:9474aac5b5bc14967dc6aef9672db651c2f4383f75ca985dd17f0df59464e1f9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3615516 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a7754dd4efe5d5161956b88335e26676dd5bfca3472b1f442746947edc720bc8`

```dockerfile
```

-	Layers:
	-	`sha256:564e54d641b13371a0e0382eab3ef680f95c5c8f2e2a709846eab1e543c5c17d`  
		Last Modified: Sat, 11 Jan 2025 01:35:10 GMT  
		Size: 3.6 MB (3594599 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f86dbcf28b75da79a560a661ecde95c976e83f519b657ab9188e471136fb34b6`  
		Last Modified: Wed, 15 Jan 2025 01:01:35 GMT  
		Size: 20.9 KB (20917 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-temurin:11-jre-ubi9-minimal` - linux; ppc64le

```console
$ docker pull eclipse-temurin@sha256:52f2ca6c32d1920c255e12e9e8e9b6000f895eb605831ab42ebaacc822a97273
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **123.0 MB (122997692 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e4dea8276c239507600bcd8a1a72a07498ef317948128fae42aaf8353fbf129`
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
	-	`sha256:dce878563f15050dbee433ee11b302dc91caccb7bbf30b63a4d16c18ac4571ad`  
		Last Modified: Wed, 15 Jan 2025 01:00:14 GMT  
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
	-	`sha256:151d8356bbf235485f85af72e9b03eac6aca94f72e39df8eaabc26571ca0f075`  
		Last Modified: Sat, 11 Jan 2025 01:37:14 GMT  
		Size: 39.7 MB (39724080 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5bacdf073a0e666561e451e76002ece2ed49a5d6c58537559cc85808b12f761`  
		Last Modified: Sat, 11 Jan 2025 01:37:12 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22421a58f599217a61b7e399da0ac3f42e5d592665dae1220cce35fcc6737159`  
		Last Modified: Sat, 11 Jan 2025 01:37:12 GMT  
		Size: 2.3 KB (2290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:11-jre-ubi9-minimal` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:03fab403aabce28db025d016abeacbec96cdd92e6776d7033f35870735c2dec7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3615477 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f5f2bae84aa97e2b37714f8f58fc382cfde3a2bc583badb703f6168e4056b14`

```dockerfile
```

-	Layers:
	-	`sha256:b1405158df06629f7e24c1a0e00a7e6013b8eb28e3f7aae9eef59e02d48b6327`  
		Last Modified: Sat, 11 Jan 2025 01:37:13 GMT  
		Size: 3.6 MB (3594634 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8ffb26f0c43e41a4e19dec146e6b64db82f4d6b4ff48a23c3828c969a488dfc0`  
		Last Modified: Wed, 15 Jan 2025 01:01:47 GMT  
		Size: 20.8 KB (20843 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-temurin:11-jre-ubi9-minimal` - linux; s390x

```console
$ docker pull eclipse-temurin@sha256:b4b4ca3d43780017a5b856bc7ae8c9e41bf04295e5869634ecc1803b5cb8d8c1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **112.4 MB (112352096 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c4d3b6e5cbdb5fb262ce5afc4aaa38ec0715dc13e9e7d3b7cb64810ff7c7eb0`
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
	-	`sha256:8ee56b4600df35f4679f31d612bb546f04a8c0ff236484b5c24d4beec3d209ff`  
		Last Modified: Wed, 15 Jan 2025 01:01:56 GMT  
		Size: 37.5 MB (37533310 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:168fa7af747923a20c9ccecc35d6f8ea158b325819f175b7fbc3590d84656a8a`  
		Last Modified: Thu, 09 Jan 2025 12:32:32 GMT  
		Size: 400.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a675f375cbacf7119aacbe8ef40ba25c801eee392e2f25776fea276c3252f817`  
		Last Modified: Sat, 11 Jan 2025 01:35:34 GMT  
		Size: 37.0 MB (37006874 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29fbfac263a9644b7c21d2b880c55ca9a5e41f03c00ebf1d416f0c2af7ff1fab`  
		Last Modified: Wed, 15 Jan 2025 01:01:56 GMT  
		Size: 37.8 MB (37809092 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e420cb88460325732b4c5e1899fe7fbab54be780b9dd03f8a47a75eec00eb2a0`  
		Last Modified: Sat, 11 Jan 2025 01:36:35 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5638db7815f87ace482b8580cd29a1b72b9e9fd158f7032012803e4afda0dc9`  
		Last Modified: Sat, 11 Jan 2025 01:36:35 GMT  
		Size: 2.3 KB (2292 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:11-jre-ubi9-minimal` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:7d80a88f65192ba8fd7f1f66c9cd561fce567cf3621f512fb96c24db1ccef0e0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3607233 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a91c3fd9d199af24ef0d4e009cc8c28bed52af89dc2ddfd6058bcf55db8c5518`

```dockerfile
```

-	Layers:
	-	`sha256:2a63283bb38fe8499a9c63f8b2b9745464d14270d913e431254c92beb44740c8`  
		Last Modified: Sat, 11 Jan 2025 01:36:34 GMT  
		Size: 3.6 MB (3586421 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a4857eaa56819333d334f642cfd6aaf52778a2ea64f7fdc84e0bbaa6ff6c3b47`  
		Last Modified: Sat, 11 Jan 2025 01:36:34 GMT  
		Size: 20.8 KB (20812 bytes)  
		MIME: application/vnd.in-toto+json
