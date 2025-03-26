## `eclipse-temurin:21-jdk-ubi9-minimal`

```console
$ docker pull eclipse-temurin@sha256:53bb9b3343fa0e2667884ab1764bbd73772e7b0e6f407a0b1370d00a01425a28
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

### `eclipse-temurin:21-jdk-ubi9-minimal` - linux; amd64

```console
$ docker pull eclipse-temurin@sha256:e099bb0771400bd41a36edadbf5db7f03944b1826013ce4b66143b990f036d20
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **210.0 MB (210041105 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:15d5a4d71bb8c342875a7cd57a54893397d825b362351e83e6ae53765acd3111`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["jshell"]`

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
ENV JAVA_VERSION=jdk-21.0.6+7
# Tue, 25 Mar 2025 17:58:27 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='04fe1273f624187d927f1b466e8cdb630d70786db07bee7599bfa5153060afd3';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.6%2B7/OpenJDK21U-jdk_aarch64_linux_hotspot_21.0.6_7.tar.gz';          ;;        ppc64le)          ESUM='163724b70b86d5a8461f85092165a9cc5a098ed900fee90d1b0c0be9607ae3d2';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.6%2B7/OpenJDK21U-jdk_ppc64le_linux_hotspot_21.0.6_7.tar.gz';          ;;        s390x)          ESUM='5ba742c87d48fcf564def56812699f6499a1cfd3535ae43286e94e74b8165faf';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.6%2B7/OpenJDK21U-jdk_s390x_linux_hotspot_21.0.6_7.tar.gz';          ;;        x86_64)          ESUM='a2650fba422283fbed20d936ce5d2a52906a5414ec17b2f7676dddb87201dbae';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.6%2B7/OpenJDK21U-jdk_x64_linux_hotspot_21.0.6_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Tue, 25 Mar 2025 17:58:27 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 25 Mar 2025 17:58:27 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 25 Mar 2025 17:58:27 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 25 Mar 2025 17:58:27 GMT
CMD ["jshell"]
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
	-	`sha256:d078fe9379a58cb578f03e9404b65a62d056d129295f2281c1e62d9eec99eeab`  
		Last Modified: Tue, 25 Mar 2025 21:57:52 GMT  
		Size: 13.1 MB (13088162 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8a426d3769c070204e4d1bb982e0b894ca5d9a8cb614076f064798e98c5cd37`  
		Last Modified: Tue, 25 Mar 2025 21:57:57 GMT  
		Size: 157.6 MB (157590657 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52aa53e42dc85af196835b73904870a796f4d5c27e8ac0237aa784d89bd16eee`  
		Last Modified: Tue, 25 Mar 2025 21:57:52 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:581e5b6854ea0421864c074a17f5e210ede98dabca62aa4356edf55c0b6edf55`  
		Last Modified: Tue, 25 Mar 2025 21:57:38 GMT  
		Size: 2.3 KB (2292 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:21-jdk-ubi9-minimal` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:bb3782c3cfbc64d2fd7ff3dce174266ffc8c803c1457f9d56d361d7ff2ad7e9c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.7 MB (1741789 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ce4c0450f7a69ec7d31eb34ecc1fa5ecc375ecc2083f0d69bb224e137f21aa11`

```dockerfile
```

-	Layers:
	-	`sha256:96849fe51d586c99abca9f787f3a93f691e995b563d85db0828ed35704a405c8`  
		Last Modified: Tue, 25 Mar 2025 21:57:52 GMT  
		Size: 1.7 MB (1719886 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3d6554dfee14422f85a1d66e8fe04e4ab5f6066a74d0ec22ce61e11d850fde78`  
		Last Modified: Tue, 25 Mar 2025 21:57:51 GMT  
		Size: 21.9 KB (21903 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-temurin:21-jdk-ubi9-minimal` - linux; arm64 variant v8

```console
$ docker pull eclipse-temurin@sha256:eba65f239dd140d8ab9e711fa5594e13497b6161b4f4f4992a092947e35ea4da
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **207.1 MB (207076683 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:93637c7ed6da2b702693fb2a4896bc2aaef6f5365fff4604e085fe25af0648ca`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["jshell"]`

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
ENV JAVA_VERSION=jdk-21.0.6+7
# Tue, 25 Mar 2025 17:58:27 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='04fe1273f624187d927f1b466e8cdb630d70786db07bee7599bfa5153060afd3';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.6%2B7/OpenJDK21U-jdk_aarch64_linux_hotspot_21.0.6_7.tar.gz';          ;;        ppc64le)          ESUM='163724b70b86d5a8461f85092165a9cc5a098ed900fee90d1b0c0be9607ae3d2';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.6%2B7/OpenJDK21U-jdk_ppc64le_linux_hotspot_21.0.6_7.tar.gz';          ;;        s390x)          ESUM='5ba742c87d48fcf564def56812699f6499a1cfd3535ae43286e94e74b8165faf';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.6%2B7/OpenJDK21U-jdk_s390x_linux_hotspot_21.0.6_7.tar.gz';          ;;        x86_64)          ESUM='a2650fba422283fbed20d936ce5d2a52906a5414ec17b2f7676dddb87201dbae';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.6%2B7/OpenJDK21U-jdk_x64_linux_hotspot_21.0.6_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Tue, 25 Mar 2025 17:58:27 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 25 Mar 2025 17:58:27 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 25 Mar 2025 17:58:27 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 25 Mar 2025 17:58:27 GMT
CMD ["jshell"]
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
	-	`sha256:11d56f12c12cc77cc1c1cf254ce34ad2a226dbc45310dfd164078eba39acc25c`  
		Last Modified: Tue, 25 Mar 2025 22:00:57 GMT  
		Size: 155.9 MB (155858858 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:401450abacc3078400112b57a2fb6c241ca0761ffe1b6d705a96ee2f9c4f7fb4`  
		Last Modified: Tue, 25 Mar 2025 22:00:53 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:668c388d59995eec127a146d1f02e1a99cbe81d7675cc01ffa265dc28f234b33`  
		Last Modified: Tue, 25 Mar 2025 22:00:53 GMT  
		Size: 2.3 KB (2292 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:21-jdk-ubi9-minimal` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:cac3f8606af92521247cdcc972799db2d07ef72cacb1343940ac9812c6dde767
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.7 MB (1742330 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e21e748d9e9e24965ecec7a9a467e49822625d2b0a018e305779a4eb3c46ba9`

```dockerfile
```

-	Layers:
	-	`sha256:b300703ebcb06ce038d69697fc87e966e70f409c13b42ac1bd6807ee93f22ea8`  
		Last Modified: Tue, 25 Mar 2025 22:00:53 GMT  
		Size: 1.7 MB (1720311 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4cd2a40343eac91ad3d388a7426f572fa08281cbd1020f9736ee41d9492afc95`  
		Last Modified: Tue, 25 Mar 2025 22:00:53 GMT  
		Size: 22.0 KB (22019 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-temurin:21-jdk-ubi9-minimal` - linux; ppc64le

```console
$ docker pull eclipse-temurin@sha256:1e23f89c81b687fe7b0aa6e3c7efe599f7d6e05d9738d17aba184cbe96dc2077
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **216.2 MB (216238352 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f8c620ce41e56655d48a9e2c14d6a7ab3b4f0d502f6cbe8b133df3e5e95feef`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["jshell"]`

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
ENV JAVA_VERSION=jdk-21.0.6+7
# Tue, 25 Mar 2025 17:58:27 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='04fe1273f624187d927f1b466e8cdb630d70786db07bee7599bfa5153060afd3';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.6%2B7/OpenJDK21U-jdk_aarch64_linux_hotspot_21.0.6_7.tar.gz';          ;;        ppc64le)          ESUM='163724b70b86d5a8461f85092165a9cc5a098ed900fee90d1b0c0be9607ae3d2';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.6%2B7/OpenJDK21U-jdk_ppc64le_linux_hotspot_21.0.6_7.tar.gz';          ;;        s390x)          ESUM='5ba742c87d48fcf564def56812699f6499a1cfd3535ae43286e94e74b8165faf';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.6%2B7/OpenJDK21U-jdk_s390x_linux_hotspot_21.0.6_7.tar.gz';          ;;        x86_64)          ESUM='a2650fba422283fbed20d936ce5d2a52906a5414ec17b2f7676dddb87201dbae';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.6%2B7/OpenJDK21U-jdk_x64_linux_hotspot_21.0.6_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Tue, 25 Mar 2025 17:58:27 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 25 Mar 2025 17:58:27 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 25 Mar 2025 17:58:27 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 25 Mar 2025 17:58:27 GMT
CMD ["jshell"]
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
	-	`sha256:9bd8c872d51b334d70929f3207586b12a33fb602b9b1a347dd8ecffaf0865350`  
		Last Modified: Tue, 25 Mar 2025 22:05:05 GMT  
		Size: 157.7 MB (157745560 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2df57c840178745c35224d8ff825cdf94f9ab2ae8fa531caaddef9b4b3b160d9`  
		Last Modified: Tue, 25 Mar 2025 22:04:56 GMT  
		Size: 130.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21c7451a3c6a4a0d5ded64d017b029cf9acf37ae547b62d31d9665a389ced66d`  
		Last Modified: Tue, 25 Mar 2025 22:04:56 GMT  
		Size: 2.3 KB (2291 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:21-jdk-ubi9-minimal` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:aaee2cb9c894f58c69b7cf2e0368a9bb0e7150432206314760f5a5cd576fced3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.7 MB (1742154 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:24b026f7de151043826b4e9a40c259b0492f56b739fc8d4a30833b796a60c90c`

```dockerfile
```

-	Layers:
	-	`sha256:4b8fa130b08403738c9bbfdc347b87e5f0956e1a68b5a30ff0a26b9f3c61668c`  
		Last Modified: Tue, 25 Mar 2025 22:04:56 GMT  
		Size: 1.7 MB (1720215 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4537e48a21756e6c9235337b2e024adeb56c149e7ae1d63776f35e52960d6643`  
		Last Modified: Tue, 25 Mar 2025 22:04:56 GMT  
		Size: 21.9 KB (21939 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-temurin:21-jdk-ubi9-minimal` - linux; s390x

```console
$ docker pull eclipse-temurin@sha256:76bfefe0a6f87c025ed144d46948c38782db6d9cd9587c6695c6e1980822ab22
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **197.8 MB (197812197 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ef8dd1c08ecdb26c2ebc4ae6f2f3cfc256e8efba499ff3e8c00793557a4b27f`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 13 Mar 2025 07:26:20 GMT
LABEL maintainer="Red Hat, Inc."
# Thu, 13 Mar 2025 07:26:20 GMT
LABEL vendor="Red Hat, Inc."
# Thu, 13 Mar 2025 07:26:20 GMT
LABEL url="https://www.redhat.com"
# Thu, 13 Mar 2025 07:26:20 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.5"       distribution-scope="public"
# Thu, 13 Mar 2025 07:26:20 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Thu, 13 Mar 2025 07:26:20 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Thu, 13 Mar 2025 07:26:20 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 13 Mar 2025 07:26:20 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 13 Mar 2025 07:26:20 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Thu, 13 Mar 2025 07:26:20 GMT
LABEL io.openshift.expose-services=""
# Thu, 13 Mar 2025 07:26:20 GMT
LABEL io.openshift.tags="minimal rhel9"
# Thu, 13 Mar 2025 07:26:20 GMT
ENV container oci
# Thu, 13 Mar 2025 07:26:21 GMT
COPY dir:0bd2f8345c36703c483db0ee0404e33109a312f452aed24ac4080629e2197763 in / 
# Thu, 13 Mar 2025 07:26:21 GMT
COPY file:b37d593713ee21ad52a4cd1424dc019a24f7966f85df0ac4b86d234302695328 in /etc/yum.repos.d/. 
# Thu, 13 Mar 2025 07:26:21 GMT
CMD ["/bin/bash"]
# Thu, 13 Mar 2025 07:26:21 GMT
RUN . /cachi2/cachi2.env &&     rm -rf /var/log/*
# Thu, 13 Mar 2025 07:26:21 GMT
LABEL "build-date"="2025-03-13T07:25:32" "architecture"="s390x" "vcs-type"="git" "vcs-ref"="7865437f00d10c54ee1c3a6268b5ff65b38afba5" "build-date"="2025-03-13T07:15:09Z" "release"="1741850109"
# Thu, 13 Mar 2025 07:26:33 GMT
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
ENV JAVA_VERSION=jdk-21.0.6+7
# Tue, 25 Mar 2025 17:58:27 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='04fe1273f624187d927f1b466e8cdb630d70786db07bee7599bfa5153060afd3';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.6%2B7/OpenJDK21U-jdk_aarch64_linux_hotspot_21.0.6_7.tar.gz';          ;;        ppc64le)          ESUM='163724b70b86d5a8461f85092165a9cc5a098ed900fee90d1b0c0be9607ae3d2';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.6%2B7/OpenJDK21U-jdk_ppc64le_linux_hotspot_21.0.6_7.tar.gz';          ;;        s390x)          ESUM='5ba742c87d48fcf564def56812699f6499a1cfd3535ae43286e94e74b8165faf';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.6%2B7/OpenJDK21U-jdk_s390x_linux_hotspot_21.0.6_7.tar.gz';          ;;        x86_64)          ESUM='a2650fba422283fbed20d936ce5d2a52906a5414ec17b2f7676dddb87201dbae';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.6%2B7/OpenJDK21U-jdk_x64_linux_hotspot_21.0.6_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Tue, 25 Mar 2025 17:58:27 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 25 Mar 2025 17:58:27 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 25 Mar 2025 17:58:27 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 25 Mar 2025 17:58:27 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:5c803ecc47a0d9d9d66bd6164bdefc7148562b976f8369af7f3ec1cc62c37cca`  
		Last Modified: Thu, 13 Mar 2025 12:27:57 GMT  
		Size: 37.5 MB (37504197 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:094529012ae62f39a61b16721406ec6b3762288ce40141f72e6917263ab122de`  
		Last Modified: Thu, 13 Mar 2025 12:27:56 GMT  
		Size: 458.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3eb8106808808f1d5a5b735787511265d305fd4624296a16f2d1eb222401d55a`  
		Last Modified: Tue, 25 Mar 2025 21:57:55 GMT  
		Size: 13.4 MB (13446471 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a96ddc2683c969514920393e1859b0c6bbc5e3792d716ff7c502de850a664ca7`  
		Last Modified: Tue, 25 Mar 2025 22:01:08 GMT  
		Size: 146.9 MB (146858650 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1b6ad5d64d7e6542a8c377c9920ab0389a08e2674b43ef0e9112860283c8782`  
		Last Modified: Tue, 25 Mar 2025 22:01:05 GMT  
		Size: 130.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7724f5a812430a41abd41ae2b82b1fa38ab7728a8078e00b96ed3fe1f0d96aa`  
		Last Modified: Tue, 25 Mar 2025 22:01:05 GMT  
		Size: 2.3 KB (2291 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:21-jdk-ubi9-minimal` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:19701f9286fb9635465fb5d5aab709b101d10f2745f691835e6be7b8e400d1d0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.7 MB (1740876 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9bb913ac2014d8e5bd694d01907730ab602a83eca376b462be5ef72bf98f3c0b`

```dockerfile
```

-	Layers:
	-	`sha256:beb621eca3dd80b5e74759b16dc9dc6fd7be897ae2e24d6185185468111b2390`  
		Last Modified: Tue, 25 Mar 2025 22:01:05 GMT  
		Size: 1.7 MB (1718973 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:05aa7a25de808c87493a2c55751bfea1eef01c50330cf013837ee94ac38a6a28`  
		Last Modified: Tue, 25 Mar 2025 22:01:05 GMT  
		Size: 21.9 KB (21903 bytes)  
		MIME: application/vnd.in-toto+json
