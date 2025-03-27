## `eclipse-temurin:8-jdk-ubi9-minimal`

```console
$ docker pull eclipse-temurin@sha256:3eee13dfd02458a781cc5df4c96465af6d1c2b4d79ac824ba27da7dd5ca93567
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `eclipse-temurin:8-jdk-ubi9-minimal` - linux; amd64

```console
$ docker pull eclipse-temurin@sha256:e5dd945533cd10675ac9e03193e4c8c7b7f69aeb5fb18e464449d1868ef5a9e3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **121.5 MB (121456204 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3eaaff014e21331ab985731caa52f58a1b37cd5bec27a04757ddae282db11d27`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`

```dockerfile
# Tue, 25 Mar 2025 15:00:05 GMT
LABEL maintainer="Red Hat, Inc."
# Tue, 25 Mar 2025 15:00:05 GMT
LABEL vendor="Red Hat, Inc."
# Tue, 25 Mar 2025 15:00:06 GMT
LABEL url="https://www.redhat.com"
# Tue, 25 Mar 2025 15:00:06 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.5"       distribution-scope="public"
# Tue, 25 Mar 2025 15:00:06 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Tue, 25 Mar 2025 15:00:06 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Tue, 25 Mar 2025 15:00:06 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Tue, 25 Mar 2025 15:00:06 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Tue, 25 Mar 2025 15:00:06 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Tue, 25 Mar 2025 15:00:06 GMT
LABEL io.openshift.expose-services=""
# Tue, 25 Mar 2025 15:00:06 GMT
LABEL io.openshift.tags="minimal rhel9"
# Tue, 25 Mar 2025 15:00:06 GMT
ENV container oci
# Tue, 25 Mar 2025 15:00:06 GMT
COPY dir:df27096315f97be2134faf11df5dc31f92c8dd671e0b8267905e1f2330865336 in / 
# Tue, 25 Mar 2025 15:00:06 GMT
COPY file:b37d593713ee21ad52a4cd1424dc019a24f7966f85df0ac4b86d234302695328 in /etc/yum.repos.d/. 
# Tue, 25 Mar 2025 15:00:06 GMT
CMD ["/bin/bash"]
# Tue, 25 Mar 2025 15:00:06 GMT
RUN . /cachi2/cachi2.env &&     rm -rf /var/log/*
# Tue, 25 Mar 2025 15:00:07 GMT
LABEL "build-date"="2025-03-25T14:59:41" "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="63823c7605fee63261a8e33cad8085bc4bb24676" "build-date"="2025-03-25T14:50:12Z" "release"="1742914212"
# Tue, 25 Mar 2025 15:00:12 GMT
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
	-	`sha256:9d561c17444a5f9cb82fc40d3d0e3f59b9f53e51dfb1c9e3d71c5c3ff898d151`  
		Last Modified: Tue, 25 Mar 2025 17:57:41 GMT  
		Size: 39.4 MB (39406022 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:adc97f92dbce4567ee13d265c17bca44426acd9f0e61a1f559344ae03bb336d2`  
		Last Modified: Tue, 25 Mar 2025 17:57:40 GMT  
		Size: 453.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3f12c9e9da2105b2d8f1415d22f2ec1ad2ea0f91be856194ca97c76ed0a6331`  
		Last Modified: Thu, 27 Mar 2025 17:59:21 GMT  
		Size: 27.3 MB (27325575 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d41ad398580cd2007bfd12b749910f5f102fc7c284b8a1025c8bac1af5097efb`  
		Last Modified: Thu, 27 Mar 2025 17:59:22 GMT  
		Size: 54.7 MB (54721713 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64a7ab70172d6e169058f138fea722da46d4b4ffb41458bb0ee076561566f173`  
		Last Modified: Thu, 27 Mar 2025 17:59:20 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a35be6697d891b63db0ac710bf6840c925bf1ef43336f3f03a75ceb5ac4d0cdf`  
		Last Modified: Thu, 27 Mar 2025 17:59:20 GMT  
		Size: 2.3 KB (2314 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:8-jdk-ubi9-minimal` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:b9a04ab5e46ca9a3f50ea529b68004e9d038ec7112c39baa2f58d92517860f87
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2597699 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f329595121e6abfabc00b819ac5803a1db31f46ed8a792af7346a8d98251fca`

```dockerfile
```

-	Layers:
	-	`sha256:4275bfe9c25b9d6b8220147e696c5fa358b618ee325d226e02a74925b381d163`  
		Last Modified: Thu, 27 Mar 2025 17:59:20 GMT  
		Size: 2.6 MB (2577043 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a8aaf071fda0e55b98078a8ad6d17328aec8852802b5938e1d8a452ad16d0689`  
		Last Modified: Thu, 27 Mar 2025 17:59:20 GMT  
		Size: 20.7 KB (20656 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-temurin:8-jdk-ubi9-minimal` - linux; arm64 variant v8

```console
$ docker pull eclipse-temurin@sha256:119d63ff34c5033ae11f15a959b8983dd4c5f7a4d33e6212e70fbcc67dbd3f2f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **119.2 MB (119158724 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:76c7c3089a0c665a8f50f94d93c18b5fb186cef9b38c904ba65ec604b58a4dc6`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`

```dockerfile
# Tue, 25 Mar 2025 15:05:12 GMT
LABEL maintainer="Red Hat, Inc."
# Tue, 25 Mar 2025 15:05:12 GMT
LABEL vendor="Red Hat, Inc."
# Tue, 25 Mar 2025 15:05:12 GMT
LABEL url="https://www.redhat.com"
# Tue, 25 Mar 2025 15:05:12 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.5"       distribution-scope="public"
# Tue, 25 Mar 2025 15:05:12 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Tue, 25 Mar 2025 15:05:13 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Tue, 25 Mar 2025 15:05:13 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Tue, 25 Mar 2025 15:05:13 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Tue, 25 Mar 2025 15:05:13 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Tue, 25 Mar 2025 15:05:13 GMT
LABEL io.openshift.expose-services=""
# Tue, 25 Mar 2025 15:05:13 GMT
LABEL io.openshift.tags="minimal rhel9"
# Tue, 25 Mar 2025 15:05:13 GMT
ENV container oci
# Tue, 25 Mar 2025 15:05:14 GMT
COPY dir:36dabe56d778e21d6cac6872809f7ae0932c9956fe7621a40aed471a4eb28b35 in / 
# Tue, 25 Mar 2025 15:05:14 GMT
COPY file:b37d593713ee21ad52a4cd1424dc019a24f7966f85df0ac4b86d234302695328 in /etc/yum.repos.d/. 
# Tue, 25 Mar 2025 15:05:14 GMT
CMD ["/bin/bash"]
# Tue, 25 Mar 2025 15:05:14 GMT
RUN . /cachi2/cachi2.env &&     rm -rf /var/log/*
# Tue, 25 Mar 2025 15:05:14 GMT
LABEL "build-date"="2025-03-25T15:04:42" "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="63823c7605fee63261a8e33cad8085bc4bb24676" "build-date"="2025-03-25T14:50:12Z" "release"="1742914212"
# Tue, 25 Mar 2025 15:05:25 GMT
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
	-	`sha256:7b061f511294c383e785796c55415ec3bed7fbb0a98d6cee8c8c6a1436d4ada8`  
		Last Modified: Tue, 25 Mar 2025 18:27:33 GMT  
		Size: 37.6 MB (37588703 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d6607d3dbc4fd04e0d544f944d20a47a5af1fa8a7520e1f37683ab236e23734`  
		Last Modified: Tue, 25 Mar 2025 18:27:31 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4fe6d8a840a9a19a4792a64986c4f2705bdfa57e1b81dec892e5e52397ad6ca`  
		Last Modified: Thu, 27 Mar 2025 18:07:23 GMT  
		Size: 27.7 MB (27743807 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c6e79ae33f45b06dbece436d4439bac74d7bdb906c11c4e14daed1e4e1de9b7`  
		Last Modified: Thu, 27 Mar 2025 18:07:24 GMT  
		Size: 53.8 MB (53823316 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0df432f90ac77e01b7564aef926a1c767ba68c1e711c22d3ce94fd0e7b42b08`  
		Last Modified: Thu, 27 Mar 2025 18:07:23 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4931da6a37967cbcf28d5d145b06045338b0b51b8784ffdf7084ea55eb6ece60`  
		Last Modified: Thu, 27 Mar 2025 18:07:24 GMT  
		Size: 2.3 KB (2316 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:8-jdk-ubi9-minimal` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:1e84af5761e50f5cfcafb3e34569a5c425cfeb97d74d34056a3fce07e096e32a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2597706 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f613cdd849e6acf6372250a0e902cf9f4648f73cfbdeb271dccc17f678a78453`

```dockerfile
```

-	Layers:
	-	`sha256:5e5cb720980166358598786ca309fd973b2006b1bde8a5709a1106a42888515c`  
		Last Modified: Thu, 27 Mar 2025 18:07:22 GMT  
		Size: 2.6 MB (2576936 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0c0cb57886abbfdb937fa06eb812a76d2cc510918d6264360763c44c1db1ab1d`  
		Last Modified: Thu, 27 Mar 2025 18:07:22 GMT  
		Size: 20.8 KB (20770 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-temurin:8-jdk-ubi9-minimal` - linux; ppc64le

```console
$ docker pull eclipse-temurin@sha256:3c77b24c17737718a4b94cb1c57338f0194fad6eb63e14341463c57cc54e9eef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **125.7 MB (125702841 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:69f46e4dce987573857454562589b0433693b85a7358439370ec6a302d9d7662`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`

```dockerfile
# Tue, 25 Mar 2025 15:07:41 GMT
LABEL maintainer="Red Hat, Inc."
# Tue, 25 Mar 2025 15:07:41 GMT
LABEL vendor="Red Hat, Inc."
# Tue, 25 Mar 2025 15:07:41 GMT
LABEL url="https://www.redhat.com"
# Tue, 25 Mar 2025 15:07:41 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.5"       distribution-scope="public"
# Tue, 25 Mar 2025 15:07:41 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Tue, 25 Mar 2025 15:07:41 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Tue, 25 Mar 2025 15:07:41 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Tue, 25 Mar 2025 15:07:41 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Tue, 25 Mar 2025 15:07:41 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Tue, 25 Mar 2025 15:07:41 GMT
LABEL io.openshift.expose-services=""
# Tue, 25 Mar 2025 15:07:41 GMT
LABEL io.openshift.tags="minimal rhel9"
# Tue, 25 Mar 2025 15:07:41 GMT
ENV container oci
# Tue, 25 Mar 2025 15:07:42 GMT
COPY dir:b00ac549f2dec3c1bd1264d0d7e9b7a2b7f966cc212ebc6aee6ca6e7f8acdce4 in / 
# Tue, 25 Mar 2025 15:07:42 GMT
COPY file:b37d593713ee21ad52a4cd1424dc019a24f7966f85df0ac4b86d234302695328 in /etc/yum.repos.d/. 
# Tue, 25 Mar 2025 15:07:42 GMT
CMD ["/bin/bash"]
# Tue, 25 Mar 2025 15:07:43 GMT
RUN . /cachi2/cachi2.env &&     rm -rf /var/log/*
# Tue, 25 Mar 2025 15:07:43 GMT
LABEL "build-date"="2025-03-25T15:07:15" "architecture"="ppc64le" "vcs-type"="git" "vcs-ref"="63823c7605fee63261a8e33cad8085bc4bb24676" "build-date"="2025-03-25T14:50:12Z" "release"="1742914212"
# Tue, 25 Mar 2025 15:08:06 GMT
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
	-	`sha256:32cf36dcf251c02cfc81f25bda80482c1e6394e4c1c7cb07317eebdc82a6ef45`  
		Last Modified: Tue, 25 Mar 2025 18:27:46 GMT  
		Size: 43.8 MB (43784360 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37f45749a0d155c224422d2f971c243e88e0afd5c485b88efda6760e3b544483`  
		Last Modified: Tue, 25 Mar 2025 18:27:43 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87fed99b32c92f36f6b421efa94367eed10b83edeecbacfa18dca2b5821dfb3b`  
		Last Modified: Thu, 27 Mar 2025 18:00:08 GMT  
		Size: 29.7 MB (29745465 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c6a148010012e50942c8a130289862647faf6b89f2c219da6cb7abdc2ee7695`  
		Last Modified: Thu, 27 Mar 2025 18:00:09 GMT  
		Size: 52.2 MB (52170121 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0eb37b4443652509554dfcc7e7f89c9e91c7182611c713ae474a2b4f665ea4de`  
		Last Modified: Thu, 27 Mar 2025 18:00:08 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d42aaa492a03bdec9491fea881091e48e761d32d05c8166ffeef9d2845e1b40`  
		Last Modified: Thu, 27 Mar 2025 18:00:09 GMT  
		Size: 2.3 KB (2314 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:8-jdk-ubi9-minimal` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:7a9bc22f3a979729208bd2ea1071d9b877e97de89cdb95160a6a57ec79b72705
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2596245 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b8c9a58748026e8053e0932117f888385823e2eb948b8325f303c892b553e551`

```dockerfile
```

-	Layers:
	-	`sha256:631506c35fd6fb7a8826c04eb02005e9a0939b8209af782fa34b5389356f60ad`  
		Last Modified: Thu, 27 Mar 2025 18:00:07 GMT  
		Size: 2.6 MB (2575553 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9aa2899354b64e96025d86aa90d032fb096be0324bc4ec4cabec35ffa7ec4d19`  
		Last Modified: Thu, 27 Mar 2025 18:00:07 GMT  
		Size: 20.7 KB (20692 bytes)  
		MIME: application/vnd.in-toto+json
