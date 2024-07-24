## `eclipse-temurin:11-jdk-ubi9-minimal`

```console
$ docker pull eclipse-temurin@sha256:ad9615021e067226b793166fab48b3efad8e76b8e2e298705d85402b1064e5fe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `eclipse-temurin:11-jdk-ubi9-minimal` - linux; amd64

```console
$ docker pull eclipse-temurin@sha256:396efd87af8fd505cfba83de8100379c38d9b1159aeae5f2a0d55f7c7c55ac7f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **208.0 MB (207995891 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c302914a917b9b9530b2b8252caeb698a0e0b7e50fafa93c0da585cd162d399a`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 06 Jun 2024 01:00:45 GMT
ADD file:0177c7dc75a5666fd7d839eb5a0fe92cceec6ce76ec113c5d876fdb57ce3b149 in / 
# Thu, 06 Jun 2024 01:00:46 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Thu, 06 Jun 2024 01:00:46 GMT
ADD file:5b1f650e1376d79fa3a65df4a154ea5166def95154b52c1c1097dfd8fc7d58eb in /tmp/tls-ca-bundle.pem 
# Thu, 06 Jun 2024 01:00:47 GMT
ADD multi:171eafe5d6538aeb2cf5cf9f6e8618f56eddbc2d8e3acf65107d17c6cc9c35de in /etc/yum.repos.d/ 
# Thu, 06 Jun 2024 01:00:47 GMT
LABEL maintainer="Red Hat, Inc."
# Thu, 06 Jun 2024 01:00:47 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.4"
# Thu, 06 Jun 2024 01:00:47 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Thu, 06 Jun 2024 01:00:47 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Thu, 06 Jun 2024 01:00:47 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 06 Jun 2024 01:00:47 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Thu, 06 Jun 2024 01:00:47 GMT
LABEL io.openshift.expose-services=""
# Thu, 06 Jun 2024 01:00:47 GMT
LABEL io.openshift.tags="minimal rhel9"
# Thu, 06 Jun 2024 01:00:47 GMT
ENV container oci
# Thu, 06 Jun 2024 01:00:47 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 06 Jun 2024 01:00:47 GMT
CMD ["/bin/bash"]
# Thu, 06 Jun 2024 01:00:47 GMT
RUN rm -rf /var/log/*
# Thu, 06 Jun 2024 01:00:47 GMT
LABEL release=1134
# Thu, 06 Jun 2024 01:00:48 GMT
ADD file:4163a5d830cc37221be507fb49bdb623672e7a59ca81defe42fc0122ff2067cc in /root/buildinfo/content_manifests/ubi9-minimal-container-9.4-1134.json 
# Thu, 06 Jun 2024 01:00:48 GMT
ADD file:0394409f6db7784d16a6bf3439e7470dbb324dc30ed9d4c8db797157e4501a3f in /root/buildinfo/Dockerfile-ubi9-minimal-9.4-1134 
# Thu, 06 Jun 2024 01:00:48 GMT
LABEL "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2024-06-06T00:53:59" "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="4b4efbdd5a311b6a9c56319e756ca58c10a2b4de" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi9-minimal/images/9.4-1134"
# Thu, 06 Jun 2024 01:00:49 GMT
RUN rm -f '/etc/yum.repos.d/repo-d5140.repo' '/etc/yum.repos.d/repo-4f47a.repo'
# Thu, 06 Jun 2024 01:00:50 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Thu, 06 Jun 2024 01:00:51 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Tue, 23 Jul 2024 17:08:23 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 23 Jul 2024 17:08:23 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 23 Jul 2024 17:08:23 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 23 Jul 2024 17:08:23 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         fontconfig         glibc-langpack-en     ;     microdnf clean all # buildkit
# Tue, 23 Jul 2024 17:08:23 GMT
ENV JAVA_VERSION=jdk-11.0.24+8
# Tue, 23 Jul 2024 17:08:23 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='04e21301fedc76841fb03929ac6cacfbbda30b5693acfd515a8f34d4a0cdeb28';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.24_8.tar.gz';          ;;        ppc64le)          ESUM='4dfdc498938a159c592a2f094576f09c94999e17327c1f5ff81794694992054d';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.24_8.tar.gz';          ;;        s390x)          ESUM='7f049af5d3ff8794d07da1c31752e18e204653930f1d422e2d42905c90c1c408';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.24_8.tar.gz';          ;;        x86_64)          ESUM='0e71a01563a5c7b9988a168b0c4ce720a6dff966b3c27bb29d1ded461ff71d0e';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jdk_x64_linux_hotspot_11.0.24_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Tue, 23 Jul 2024 17:08:23 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 23 Jul 2024 17:08:23 GMT
COPY entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 23 Jul 2024 17:08:23 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 23 Jul 2024 17:08:23 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:e394ea8406c7ed85ddc862f882ec77dcfd3863de3cb90fd8006238d521d22d44`  
		Last Modified: Thu, 13 Jun 2024 09:01:28 GMT  
		Size: 38.9 MB (38852317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e6375c986c88b85d8725ab13e1c29fc69490232914f075cade4cdbf691b5348`  
		Last Modified: Thu, 13 Jun 2024 18:53:58 GMT  
		Size: 27.1 MB (27134546 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33a4880a67094b1ba1f59b459fb97dfcd00aaa1a0f8c6a8bfc71c2d874ce0a4f`  
		Last Modified: Wed, 24 Jul 2024 01:27:47 GMT  
		Size: 142.0 MB (142007447 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1622a7190bb3de0525bb68cd33918e13ce2e730957dba37fdb4530f775b27171`  
		Last Modified: Wed, 24 Jul 2024 01:27:37 GMT  
		Size: 147.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b8e6c875948b1f02fcd9d5dbfea0cd727cdee74350d217f992621334fbf175a`  
		Last Modified: Wed, 24 Jul 2024 01:27:37 GMT  
		Size: 1.4 KB (1434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:11-jdk-ubi9-minimal` - linux; arm64 variant v8

```console
$ docker pull eclipse-temurin@sha256:8ca96d2004bb23be1f763c9ba6a87ad361723f092da6c4e636ab681fc09b26e6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **203.5 MB (203506702 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a10861625d3f80797463a577e878e8caeb6377edb3e58d36cb2d5cdcf28f25ed`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 06 Jun 2024 01:00:43 GMT
ADD file:a0eabcdf2ab69cce7aa1eb328b862afe9d22c644fe1194679f30c6f67e244c6b in / 
# Thu, 06 Jun 2024 01:00:44 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Thu, 06 Jun 2024 01:00:44 GMT
ADD file:5b1f650e1376d79fa3a65df4a154ea5166def95154b52c1c1097dfd8fc7d58eb in /tmp/tls-ca-bundle.pem 
# Thu, 06 Jun 2024 01:00:44 GMT
ADD multi:171eafe5d6538aeb2cf5cf9f6e8618f56eddbc2d8e3acf65107d17c6cc9c35de in /etc/yum.repos.d/ 
# Thu, 06 Jun 2024 01:00:44 GMT
LABEL maintainer="Red Hat, Inc."
# Thu, 06 Jun 2024 01:00:44 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.4"
# Thu, 06 Jun 2024 01:00:44 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Thu, 06 Jun 2024 01:00:44 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Thu, 06 Jun 2024 01:00:44 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 06 Jun 2024 01:00:44 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Thu, 06 Jun 2024 01:00:44 GMT
LABEL io.openshift.expose-services=""
# Thu, 06 Jun 2024 01:00:44 GMT
LABEL io.openshift.tags="minimal rhel9"
# Thu, 06 Jun 2024 01:00:44 GMT
ENV container oci
# Thu, 06 Jun 2024 01:00:44 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 06 Jun 2024 01:00:44 GMT
CMD ["/bin/bash"]
# Thu, 06 Jun 2024 01:00:45 GMT
RUN rm -rf /var/log/*
# Thu, 06 Jun 2024 01:00:45 GMT
LABEL release=1134
# Thu, 06 Jun 2024 01:00:45 GMT
ADD file:889f44042d0c51b9eda12ed533aa1fb117a8ffcf209c0ad0a329baaa81eac425 in /root/buildinfo/content_manifests/ubi9-minimal-container-9.4-1134.json 
# Thu, 06 Jun 2024 01:00:45 GMT
ADD file:b6af28769ecb7942ba5cf7b0e1bbf054cd8a414727a87e4ff5ecb40886563b94 in /root/buildinfo/Dockerfile-ubi9-minimal-9.4-1134 
# Thu, 06 Jun 2024 01:00:45 GMT
LABEL "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2024-06-06T00:53:59" "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="4b4efbdd5a311b6a9c56319e756ca58c10a2b4de" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi9-minimal/images/9.4-1134"
# Thu, 06 Jun 2024 01:00:47 GMT
RUN rm -f '/etc/yum.repos.d/repo-d5140.repo' '/etc/yum.repos.d/repo-4f47a.repo'
# Thu, 06 Jun 2024 01:00:48 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Thu, 06 Jun 2024 01:00:49 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Tue, 23 Jul 2024 17:08:23 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 23 Jul 2024 17:08:23 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 23 Jul 2024 17:08:23 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 23 Jul 2024 17:08:23 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         fontconfig         glibc-langpack-en     ;     microdnf clean all # buildkit
# Tue, 23 Jul 2024 17:08:23 GMT
ENV JAVA_VERSION=jdk-11.0.24+8
# Tue, 23 Jul 2024 17:08:23 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='04e21301fedc76841fb03929ac6cacfbbda30b5693acfd515a8f34d4a0cdeb28';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.24_8.tar.gz';          ;;        ppc64le)          ESUM='4dfdc498938a159c592a2f094576f09c94999e17327c1f5ff81794694992054d';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.24_8.tar.gz';          ;;        s390x)          ESUM='7f049af5d3ff8794d07da1c31752e18e204653930f1d422e2d42905c90c1c408';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.24_8.tar.gz';          ;;        x86_64)          ESUM='0e71a01563a5c7b9988a168b0c4ce720a6dff966b3c27bb29d1ded461ff71d0e';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jdk_x64_linux_hotspot_11.0.24_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Tue, 23 Jul 2024 17:08:23 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 23 Jul 2024 17:08:23 GMT
COPY entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 23 Jul 2024 17:08:23 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 23 Jul 2024 17:08:23 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:12041dc61838218321383650a1641a04f91cba754a7465ce28de10da7d0af785`  
		Last Modified: Thu, 13 Jun 2024 09:26:57 GMT  
		Size: 37.1 MB (37118393 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab92e4fa2e666442516b083f88db062d022d302e1a9ed9430c5a7743cc377b2d`  
		Last Modified: Thu, 13 Jun 2024 18:34:36 GMT  
		Size: 27.6 MB (27572657 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89cead1c332edcbb2f69032f5e50bdb4db650237dcddcd73a0a5cc38790fde45`  
		Last Modified: Wed, 24 Jul 2024 00:51:24 GMT  
		Size: 138.8 MB (138814072 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07fa84d516625174a44896755db756abcefb2e3e13264a8b33f02a4e67dbf74e`  
		Last Modified: Wed, 24 Jul 2024 00:51:16 GMT  
		Size: 146.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2fa16c1f16050ed2c069a08edfd251398c326ba2e66ff123fa665cfaf921aebe`  
		Last Modified: Wed, 24 Jul 2024 00:51:16 GMT  
		Size: 1.4 KB (1434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:11-jdk-ubi9-minimal` - linux; ppc64le

```console
$ docker pull eclipse-temurin@sha256:f40a71700a1e8a8366544fba6badf0579db2cd36a2afdbb770ffc724d1919217
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **202.2 MB (202159444 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f7467c0af1362e37994a73768f972db2905207da34562cf4fe266ec6bd377234`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 06 Jun 2024 01:00:47 GMT
ADD file:08e799b553ca381241eb51a31a1ee7c9ca460c662c2c16a91f95cedffe556f65 in / 
# Thu, 06 Jun 2024 01:00:49 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Thu, 06 Jun 2024 01:00:49 GMT
ADD file:5b1f650e1376d79fa3a65df4a154ea5166def95154b52c1c1097dfd8fc7d58eb in /tmp/tls-ca-bundle.pem 
# Thu, 06 Jun 2024 01:00:49 GMT
ADD multi:171eafe5d6538aeb2cf5cf9f6e8618f56eddbc2d8e3acf65107d17c6cc9c35de in /etc/yum.repos.d/ 
# Thu, 06 Jun 2024 01:00:49 GMT
LABEL maintainer="Red Hat, Inc."
# Thu, 06 Jun 2024 01:00:49 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.4"
# Thu, 06 Jun 2024 01:00:49 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Thu, 06 Jun 2024 01:00:49 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Thu, 06 Jun 2024 01:00:49 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 06 Jun 2024 01:00:49 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Thu, 06 Jun 2024 01:00:49 GMT
LABEL io.openshift.expose-services=""
# Thu, 06 Jun 2024 01:00:49 GMT
LABEL io.openshift.tags="minimal rhel9"
# Thu, 06 Jun 2024 01:00:49 GMT
ENV container oci
# Thu, 06 Jun 2024 01:00:49 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 06 Jun 2024 01:00:49 GMT
CMD ["/bin/bash"]
# Thu, 06 Jun 2024 01:00:50 GMT
RUN rm -rf /var/log/*
# Thu, 06 Jun 2024 01:00:50 GMT
LABEL release=1134
# Thu, 06 Jun 2024 01:00:51 GMT
ADD file:d5256988023f3e471eb14a7af9564f7c60a67157fde7e15bf77b2e1de43dae53 in /root/buildinfo/content_manifests/ubi9-minimal-container-9.4-1134.json 
# Thu, 06 Jun 2024 01:00:51 GMT
ADD file:46bfa545b2d866eea3fb9f054d54e5e57bbab38aa0340aca4ca393a489cfa2ba in /root/buildinfo/Dockerfile-ubi9-minimal-9.4-1134 
# Thu, 06 Jun 2024 01:00:51 GMT
LABEL "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2024-06-06T00:53:59" "architecture"="ppc64le" "vcs-type"="git" "vcs-ref"="4b4efbdd5a311b6a9c56319e756ca58c10a2b4de" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi9-minimal/images/9.4-1134"
# Thu, 06 Jun 2024 01:00:52 GMT
RUN rm -f '/etc/yum.repos.d/repo-d5140.repo' '/etc/yum.repos.d/repo-4f47a.repo'
# Thu, 06 Jun 2024 01:00:54 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Thu, 06 Jun 2024 01:00:56 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Tue, 23 Jul 2024 17:08:23 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 23 Jul 2024 17:08:23 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 23 Jul 2024 17:08:23 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 23 Jul 2024 17:08:23 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         fontconfig         glibc-langpack-en     ;     microdnf clean all # buildkit
# Tue, 23 Jul 2024 17:08:23 GMT
ENV JAVA_VERSION=jdk-11.0.24+8
# Tue, 23 Jul 2024 17:08:23 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='04e21301fedc76841fb03929ac6cacfbbda30b5693acfd515a8f34d4a0cdeb28';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.24_8.tar.gz';          ;;        ppc64le)          ESUM='4dfdc498938a159c592a2f094576f09c94999e17327c1f5ff81794694992054d';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.24_8.tar.gz';          ;;        s390x)          ESUM='7f049af5d3ff8794d07da1c31752e18e204653930f1d422e2d42905c90c1c408';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.24_8.tar.gz';          ;;        x86_64)          ESUM='0e71a01563a5c7b9988a168b0c4ce720a6dff966b3c27bb29d1ded461ff71d0e';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jdk_x64_linux_hotspot_11.0.24_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Tue, 23 Jul 2024 17:08:23 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 23 Jul 2024 17:08:23 GMT
COPY entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 23 Jul 2024 17:08:23 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 23 Jul 2024 17:08:23 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:8b8b86a0ce1c4731395e06bea9200f9baa7149a52efacd1e4802e0e18d2d532b`  
		Last Modified: Thu, 13 Jun 2024 12:10:19 GMT  
		Size: 43.3 MB (43338217 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9108aa162224809f661a0bf1222b33bfa68e47315ca1522df958c7eed8ded4c`  
		Last Modified: Thu, 13 Jun 2024 18:25:50 GMT  
		Size: 29.6 MB (29567669 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb4ed80a5ae637a0fea91a6a55d76d4a0d879fb43d4f148389dbbd5b7a16c1ae`  
		Last Modified: Wed, 24 Jul 2024 04:12:52 GMT  
		Size: 129.3 MB (129251982 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ac9ecdff532f269a3b960be73558fa06a81873017ca2c7e670428a26d40c9b9`  
		Last Modified: Wed, 24 Jul 2024 04:12:40 GMT  
		Size: 145.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8a8a1ce610e15eb9d808f87642e8a1ede320c1c3b6bbd0b982d60318fa5c4c3`  
		Last Modified: Wed, 24 Jul 2024 04:12:40 GMT  
		Size: 1.4 KB (1431 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:11-jdk-ubi9-minimal` - linux; s390x

```console
$ docker pull eclipse-temurin@sha256:23d4426aabf32e55466a560dd0189a895d449dac3f440fb548c4f070e1ea5900
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **186.2 MB (186212112 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9eef3a62a507f5adf3ec88704731d6f5e0e49fefb89ab927eb2a7f26c5561e20`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 06 Jun 2024 01:00:49 GMT
ADD file:b21a8bc3ef68d6bce1d25e12d0b78b31c49207e12b886ebdd7cb11178ef475bd in / 
# Thu, 06 Jun 2024 01:00:50 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Thu, 06 Jun 2024 01:00:50 GMT
ADD file:5b1f650e1376d79fa3a65df4a154ea5166def95154b52c1c1097dfd8fc7d58eb in /tmp/tls-ca-bundle.pem 
# Thu, 06 Jun 2024 01:00:50 GMT
ADD multi:171eafe5d6538aeb2cf5cf9f6e8618f56eddbc2d8e3acf65107d17c6cc9c35de in /etc/yum.repos.d/ 
# Thu, 06 Jun 2024 01:00:50 GMT
LABEL maintainer="Red Hat, Inc."
# Thu, 06 Jun 2024 01:00:50 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.4"
# Thu, 06 Jun 2024 01:00:50 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Thu, 06 Jun 2024 01:00:50 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Thu, 06 Jun 2024 01:00:50 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 06 Jun 2024 01:00:50 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Thu, 06 Jun 2024 01:00:50 GMT
LABEL io.openshift.expose-services=""
# Thu, 06 Jun 2024 01:00:50 GMT
LABEL io.openshift.tags="minimal rhel9"
# Thu, 06 Jun 2024 01:00:50 GMT
ENV container oci
# Thu, 06 Jun 2024 01:00:50 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 06 Jun 2024 01:00:50 GMT
CMD ["/bin/bash"]
# Thu, 06 Jun 2024 01:00:51 GMT
RUN rm -rf /var/log/*
# Thu, 06 Jun 2024 01:00:51 GMT
LABEL release=1134
# Thu, 06 Jun 2024 01:00:52 GMT
ADD file:220d43ebc0448d8362945e8e42d9c13d9b5cd70387a6ab5cfc6510d21af21993 in /root/buildinfo/content_manifests/ubi9-minimal-container-9.4-1134.json 
# Thu, 06 Jun 2024 01:00:52 GMT
ADD file:70110f96db0c0dc971bede13c726432bddb352060c14ba3efc93e4bee1b5e7cc in /root/buildinfo/Dockerfile-ubi9-minimal-9.4-1134 
# Thu, 06 Jun 2024 01:00:52 GMT
LABEL "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2024-06-06T00:53:59" "architecture"="s390x" "vcs-type"="git" "vcs-ref"="4b4efbdd5a311b6a9c56319e756ca58c10a2b4de" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi9-minimal/images/9.4-1134"
# Thu, 06 Jun 2024 01:00:53 GMT
RUN rm -f '/etc/yum.repos.d/repo-d5140.repo' '/etc/yum.repos.d/repo-4f47a.repo'
# Thu, 06 Jun 2024 01:00:54 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Thu, 06 Jun 2024 01:00:56 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Tue, 23 Jul 2024 17:08:23 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 23 Jul 2024 17:08:23 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 23 Jul 2024 17:08:23 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 23 Jul 2024 17:08:23 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         fontconfig         glibc-langpack-en     ;     microdnf clean all # buildkit
# Tue, 23 Jul 2024 17:08:23 GMT
ENV JAVA_VERSION=jdk-11.0.24+8
# Tue, 23 Jul 2024 17:08:23 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='04e21301fedc76841fb03929ac6cacfbbda30b5693acfd515a8f34d4a0cdeb28';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.24_8.tar.gz';          ;;        ppc64le)          ESUM='4dfdc498938a159c592a2f094576f09c94999e17327c1f5ff81794694992054d';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.24_8.tar.gz';          ;;        s390x)          ESUM='7f049af5d3ff8794d07da1c31752e18e204653930f1d422e2d42905c90c1c408';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.24_8.tar.gz';          ;;        x86_64)          ESUM='0e71a01563a5c7b9988a168b0c4ce720a6dff966b3c27bb29d1ded461ff71d0e';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jdk_x64_linux_hotspot_11.0.24_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Tue, 23 Jul 2024 17:08:23 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 23 Jul 2024 17:08:23 GMT
COPY entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 23 Jul 2024 17:08:23 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 23 Jul 2024 17:08:23 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:e9ed43d0c04feff07fcf0295330d9685993995f0185d271299e97e711ce45c19`  
		Last Modified: Thu, 13 Jun 2024 12:10:24 GMT  
		Size: 37.1 MB (37114295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82dae315f4b984fb474d84af85982fb8900a27ce6206438dcb3dbb4b52fdbf1b`  
		Last Modified: Thu, 13 Jun 2024 19:04:39 GMT  
		Size: 27.2 MB (27168221 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ebf980ee4d678123e33927308edfe2c9d618ae3bc25d6099ebea7a278048abe`  
		Last Modified: Wed, 24 Jul 2024 00:57:05 GMT  
		Size: 121.9 MB (121928014 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9d7fd75afbb1ff3322e24bcffe6d431fdcaf0627804ecaeb090e79947ac0942`  
		Last Modified: Wed, 24 Jul 2024 00:56:57 GMT  
		Size: 146.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ed0496e575e76a7043e1fb2d2f4f50aa51f7468a7736b186dbf023857a6a285`  
		Last Modified: Wed, 24 Jul 2024 00:56:57 GMT  
		Size: 1.4 KB (1436 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
