## `eclipse-temurin:8-jdk-ubi9-minimal`

```console
$ docker pull eclipse-temurin@sha256:a4c5b54b5814a676769b6f87149ce3e9eba98158d26f8bde9b88c08c9e1c0c96
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
$ docker pull eclipse-temurin@sha256:20cb6dfda7430bad7cfb683ba6dce62788d9738bf8d32f20e1120c9ea2ee1ccf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **180.0 MB (180049124 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba2aea65dadc2d1df81dde872043aaebc5c3150ee4b0b0aec98d0f69d937e468`
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
COPY dir:ce392e97b0a18d36dffa0c783a840f3ab28026ae011aa3a1855943fa61c597d8 in / 
# Wed, 23 Oct 2024 15:41:32 GMT
COPY file:b37d593713ee21ad52a4cd1424dc019a24f7966f85df0ac4b86d234302695328 in /etc/yum.repos.d/. 
# Wed, 23 Oct 2024 15:41:32 GMT
CMD ["/bin/bash"]
# Wed, 23 Oct 2024 15:41:32 GMT
RUN . /cachi2/cachi2.env &&     rm -rf /var/log/*
# Wed, 23 Oct 2024 15:41:32 GMT
LABEL "build-date"="2024-12-09T18:15:25" "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="fee5a8f3e74ac2340dca04210f5456952058c9f4" "build-date"="2024-12-09T18:11:07Z" "release"="1733767867"
# Wed, 23 Oct 2024 15:41:32 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 23 Oct 2024 15:41:32 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 23 Oct 2024 15:41:32 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 23 Oct 2024 15:41:32 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         fontconfig         glibc-langpack-en     ;     microdnf clean all # buildkit
# Wed, 23 Oct 2024 15:41:32 GMT
ENV JAVA_VERSION=jdk8u432-b06
# Wed, 23 Oct 2024 15:41:32 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='383caabc20428e9500f2e07965317ed4387a0e336104483e29a9e06eeffbf26b';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u432-b06/OpenJDK8U-jdk_aarch64_linux_hotspot_8u432b06.tar.gz';          ;;        ppc64le)          ESUM='64fb17e83b79f9ad41dc18351a408bfe90324fd6360903ca5c0a740006c81be3';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u432-b06/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u432b06.tar.gz';          ;;        x86_64)          ESUM='abaaa90deadf51bd28921453baf2992b3dff6171bb7142f5bdd14ef269f7b245';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u432-b06/OpenJDK8U-jdk_x64_linux_hotspot_8u432b06.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -r "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Wed, 23 Oct 2024 15:41:32 GMT
RUN set -eux;     echo "Verifying install ...";     echo "javac -version"; javac -version;     echo "java -version"; java -version;     echo "Complete." # buildkit
# Wed, 23 Oct 2024 15:41:32 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 23 Oct 2024 15:41:32 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
```

-	Layers:
	-	`sha256:8afba38a614e150d5cec9d32c41bedfe2fe3cc1a11fbd33c712e10abb9e65de9`  
		Last Modified: Mon, 09 Dec 2024 19:12:44 GMT  
		Size: 39.4 MB (39419294 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b9e0f097cc0f4487dee00bd985d6bf5370e82cc60c12022507829d7e7365c9b`  
		Last Modified: Wed, 11 Dec 2024 20:29:38 GMT  
		Size: 37.0 MB (36992809 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17d143b671d10ef1ac2d8c1e2040970c60e38fd37d7bbdfb0e6f1bc000be2767`  
		Last Modified: Wed, 11 Dec 2024 20:29:39 GMT  
		Size: 103.6 MB (103634577 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20a2cbe2e0688bbd3a144de51d3287e2b67cfb8ba1bd2a806f4d6dc82f11707d`  
		Last Modified: Wed, 11 Dec 2024 20:29:38 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db1da1ae7222ba62b46fd0eaa2d3cb6ff212df3f9e42972b8f09caccdc6286bb`  
		Last Modified: Wed, 11 Dec 2024 20:29:39 GMT  
		Size: 2.3 KB (2316 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:8-jdk-ubi9-minimal` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:4f4c61e85b2264a5cf0cf355ccf93f5a56140e24bba207a8bec3f796349a506c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3816792 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf2033b87f6e3baf6a2002a4c03c35b89d7bf8961950acdefca9302b5a743bef`

```dockerfile
```

-	Layers:
	-	`sha256:bd3bd7d38a764d15ef0c4cf91edf11940fa634b2c5c9095303f2b28dad16a3a8`  
		Last Modified: Wed, 11 Dec 2024 20:29:38 GMT  
		Size: 3.8 MB (3797111 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2e83a7a5eaa90c113b3440df3f1f5ecc9f3f630cdb1bc7667e40fffc5728f308`  
		Last Modified: Wed, 11 Dec 2024 20:29:38 GMT  
		Size: 19.7 KB (19681 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-temurin:8-jdk-ubi9-minimal` - linux; arm64 variant v8

```console
$ docker pull eclipse-temurin@sha256:64516efd97650fd4cb3503bdae2dad53787997bd3ef8f37cbf53d9516aafd0f2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **177.8 MB (177849392 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3fff39bdeb8ff7db7740422c6b63fead801c6d0dca5c94250e7d8f9b8205754c`
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
COPY dir:bb4d3e8bf66b9361ce2c66099dbb4009a49deed7f655ac787c49d395bf0c8ed0 in / 
# Wed, 23 Oct 2024 15:41:32 GMT
COPY file:b37d593713ee21ad52a4cd1424dc019a24f7966f85df0ac4b86d234302695328 in /etc/yum.repos.d/. 
# Wed, 23 Oct 2024 15:41:32 GMT
CMD ["/bin/bash"]
# Wed, 23 Oct 2024 15:41:32 GMT
RUN . /cachi2/cachi2.env &&     rm -rf /var/log/*
# Wed, 23 Oct 2024 15:41:32 GMT
LABEL "build-date"="2024-12-09T18:18:20" "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="fee5a8f3e74ac2340dca04210f5456952058c9f4" "build-date"="2024-12-09T18:11:07Z" "release"="1733767867"
# Wed, 23 Oct 2024 15:41:32 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 23 Oct 2024 15:41:32 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 23 Oct 2024 15:41:32 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 23 Oct 2024 15:41:32 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         fontconfig         glibc-langpack-en     ;     microdnf clean all # buildkit
# Wed, 23 Oct 2024 15:41:32 GMT
ENV JAVA_VERSION=jdk8u432-b06
# Wed, 23 Oct 2024 15:41:32 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='383caabc20428e9500f2e07965317ed4387a0e336104483e29a9e06eeffbf26b';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u432-b06/OpenJDK8U-jdk_aarch64_linux_hotspot_8u432b06.tar.gz';          ;;        ppc64le)          ESUM='64fb17e83b79f9ad41dc18351a408bfe90324fd6360903ca5c0a740006c81be3';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u432-b06/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u432b06.tar.gz';          ;;        x86_64)          ESUM='abaaa90deadf51bd28921453baf2992b3dff6171bb7142f5bdd14ef269f7b245';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u432-b06/OpenJDK8U-jdk_x64_linux_hotspot_8u432b06.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -r "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Wed, 23 Oct 2024 15:41:32 GMT
RUN set -eux;     echo "Verifying install ...";     echo "javac -version"; javac -version;     echo "java -version"; java -version;     echo "Complete." # buildkit
# Wed, 23 Oct 2024 15:41:32 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 23 Oct 2024 15:41:32 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
```

-	Layers:
	-	`sha256:0ed94f65e4fba4435c4119e46186c8cd6e06d97d466980566e3061cc1a6a19a2`  
		Last Modified: Mon, 09 Dec 2024 21:46:51 GMT  
		Size: 37.6 MB (37647525 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e16a7178cd631e8e68738f34a2f20d3ba24d9ff892dd572f951fc36b2476268`  
		Last Modified: Wed, 11 Dec 2024 20:38:41 GMT  
		Size: 37.5 MB (37451094 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:304710f64445c75468fe63b2f8d602ee96b6073db13c116348be7b8140277d7c`  
		Last Modified: Wed, 11 Dec 2024 20:38:42 GMT  
		Size: 102.7 MB (102748330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:084bcb8686d4c9eab7b561a4e4168308c00d4da5e0d89a4fd823ed4a93b95281`  
		Last Modified: Wed, 11 Dec 2024 20:38:39 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c42842984f864aa84d6cfda5d2e7ca0c948169e761a4bf343fecb158a89be385`  
		Last Modified: Wed, 11 Dec 2024 20:38:40 GMT  
		Size: 2.3 KB (2316 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:8-jdk-ubi9-minimal` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:8d5a52b2f80ee7a8c0f9d3a3fdcc3797e521a820e808fb80eaf074c7e00ca91e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3816885 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd2de079507b3f9f6a15ff4b754c392c43c27b803cdc6e8997289e559ab905b5`

```dockerfile
```

-	Layers:
	-	`sha256:581c9bbf6913538834de42c090eaf5c04b3fff2097aa7216d799afd12b46134c`  
		Last Modified: Wed, 11 Dec 2024 20:38:40 GMT  
		Size: 3.8 MB (3797085 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:22ebb077405daf12edbd3880d8256db292cf5876c083cda5090f53b71f1be278`  
		Last Modified: Wed, 11 Dec 2024 20:38:39 GMT  
		Size: 19.8 KB (19800 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-temurin:8-jdk-ubi9-minimal` - linux; ppc64le

```console
$ docker pull eclipse-temurin@sha256:9263c1b80807b29a9f0086eb40413b40026ccf82a61e620d477628f597120688
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **184.4 MB (184372602 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:002684aebc2f906836c2bfa0f739f7a50dd0cc17aca4ce67a43e59ec411490bb`
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
COPY dir:8f21bb638bfc9999eb0c06c365b4f63918e550b9f8a3df9bb94983276e9b11a8 in / 
# Wed, 23 Oct 2024 15:41:32 GMT
COPY file:b37d593713ee21ad52a4cd1424dc019a24f7966f85df0ac4b86d234302695328 in /etc/yum.repos.d/. 
# Wed, 23 Oct 2024 15:41:32 GMT
CMD ["/bin/bash"]
# Wed, 23 Oct 2024 15:41:32 GMT
RUN . /cachi2/cachi2.env &&     rm -rf /var/log/*
# Wed, 23 Oct 2024 15:41:32 GMT
LABEL "build-date"="2024-12-09T18:28:12" "architecture"="ppc64le" "vcs-type"="git" "vcs-ref"="fee5a8f3e74ac2340dca04210f5456952058c9f4" "build-date"="2024-12-09T18:11:07Z" "release"="1733767867"
# Wed, 23 Oct 2024 15:41:32 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 23 Oct 2024 15:41:32 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 23 Oct 2024 15:41:32 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 23 Oct 2024 15:41:32 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         fontconfig         glibc-langpack-en     ;     microdnf clean all # buildkit
# Wed, 23 Oct 2024 15:41:32 GMT
ENV JAVA_VERSION=jdk8u432-b06
# Wed, 23 Oct 2024 15:41:32 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='383caabc20428e9500f2e07965317ed4387a0e336104483e29a9e06eeffbf26b';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u432-b06/OpenJDK8U-jdk_aarch64_linux_hotspot_8u432b06.tar.gz';          ;;        ppc64le)          ESUM='64fb17e83b79f9ad41dc18351a408bfe90324fd6360903ca5c0a740006c81be3';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u432-b06/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u432b06.tar.gz';          ;;        x86_64)          ESUM='abaaa90deadf51bd28921453baf2992b3dff6171bb7142f5bdd14ef269f7b245';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u432-b06/OpenJDK8U-jdk_x64_linux_hotspot_8u432b06.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -r "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Wed, 23 Oct 2024 15:41:32 GMT
RUN set -eux;     echo "Verifying install ...";     echo "javac -version"; javac -version;     echo "java -version"; java -version;     echo "Complete." # buildkit
# Wed, 23 Oct 2024 15:41:32 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 23 Oct 2024 15:41:32 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
```

-	Layers:
	-	`sha256:7f109adddadf658534777a91b226ce1bc9f7dcc45f9c30eea9c0e426aadaa062`  
		Last Modified: Tue, 10 Dec 2024 00:14:54 GMT  
		Size: 43.8 MB (43801042 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67d525a4c647a13d8db1417c57a1dc81822cc7796bf044edd48aa9d99ca6ee58`  
		Last Modified: Wed, 11 Dec 2024 20:32:31 GMT  
		Size: 39.5 MB (39476600 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8311d1babf69510b4f7c3b8b3dde02421148aad0dadcf4d02bb19e1614760b85`  
		Last Modified: Wed, 11 Dec 2024 20:32:33 GMT  
		Size: 101.1 MB (101092515 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:918e5a45d955f118e26c0c5761a3fd2453be0b3215c5ca941570f8813794f64f`  
		Last Modified: Wed, 11 Dec 2024 20:32:29 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffbf858bb3508c748bb85f339059116f43d9782a3f3bee3508857b823d8014c6`  
		Last Modified: Wed, 11 Dec 2024 20:32:30 GMT  
		Size: 2.3 KB (2316 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:8-jdk-ubi9-minimal` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:feddd10033c5c6e445344b6fb37a091626916f5748877009cda25829134eaed6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3815447 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e9a444f6c2c230a84592478dc0aa0d00233ec6e5f36f312a86435cf323a3f9fe`

```dockerfile
```

-	Layers:
	-	`sha256:9169a00bcde4fdf02daefaf6a46c88bb26f0bc14ad0fb86e2015066a83626f55`  
		Last Modified: Wed, 11 Dec 2024 20:32:30 GMT  
		Size: 3.8 MB (3795728 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:30a7b2c05469c356b0bb67e1d450631f970a3c32b283ac948f24331d5dd0bbfc`  
		Last Modified: Wed, 11 Dec 2024 20:32:29 GMT  
		Size: 19.7 KB (19719 bytes)  
		MIME: application/vnd.in-toto+json
