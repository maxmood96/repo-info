## `eclipse-temurin:11-jdk-ubi9-minimal`

```console
$ docker pull eclipse-temurin@sha256:1bebbe0fda5b0a0b23d27e02e5417b34a1c6e5d0c6bb1dc62aa49e6a0c3d5f65
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `eclipse-temurin:11-jdk-ubi9-minimal` - linux; amd64

```console
$ docker pull eclipse-temurin@sha256:b8a27c2a6ce8c3de79e4aaaf4043ac24a392227b89d4fbcdd6eaa9efadb2a79b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **207.0 MB (206990106 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f0036cc3ee8584ac0cee322adcd45a481575b3681e7b6f7a88808fc0ec6daf4`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 15 Jun 2023 01:53:36 GMT
ADD file:80304e0bef72b7ea92e51e210b2106f2c76929c20237bda1e2504ed5f08a797b in / 
# Thu, 15 Jun 2023 01:53:37 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Thu, 15 Jun 2023 01:53:37 GMT
ADD file:214c1de395c24e4a86ef9a706069ef30a9e804c63f851c37c35655e16fea3ced in /tmp/tls-ca-bundle.pem 
# Thu, 15 Jun 2023 01:53:38 GMT
ADD multi:9849bd0aefa7f9f98ad6e5e3688cb1fbc7313bd1a292ba10ed260c50163f7cee in /etc/yum.repos.d/ 
# Thu, 15 Jun 2023 01:53:38 GMT
LABEL maintainer="Red Hat, Inc."
# Thu, 15 Jun 2023 01:53:38 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.2"
# Thu, 15 Jun 2023 01:53:38 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Thu, 15 Jun 2023 01:53:38 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Thu, 15 Jun 2023 01:53:38 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 15 Jun 2023 01:53:38 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Thu, 15 Jun 2023 01:53:38 GMT
LABEL io.openshift.expose-services=""
# Thu, 15 Jun 2023 01:53:38 GMT
LABEL io.openshift.tags="minimal rhel9"
# Thu, 15 Jun 2023 01:53:38 GMT
ENV container oci
# Thu, 15 Jun 2023 01:53:38 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 15 Jun 2023 01:53:38 GMT
CMD ["/bin/bash"]
# Thu, 15 Jun 2023 01:53:39 GMT
RUN rm -rf /var/log/*
# Thu, 15 Jun 2023 01:53:39 GMT
LABEL release=691
# Thu, 15 Jun 2023 01:53:39 GMT
ADD file:f9ce97cb03af747b91e8159962dd1fafb4875a94fd8e03fa1bea1e9a7c1ba028 in /root/buildinfo/content_manifests/ubi9-minimal-container-9.2-691.json 
# Thu, 15 Jun 2023 01:53:39 GMT
ADD file:2ff83eb5063de7c62bc86b57ae37130f3c49c5f7d6920bc96b44baad3134fcb8 in /root/buildinfo/Dockerfile-ubi9-minimal-9.2-691 
# Thu, 15 Jun 2023 01:53:39 GMT
LABEL "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2023-06-15T01:42:07" "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="7ef59505f75bf0c11c8d3addefebee5ceaaf4c41" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi9-minimal/images/9.2-691"
# Thu, 15 Jun 2023 01:53:40 GMT
RUN rm -f '/etc/yum.repos.d/repo-dc573.repo' '/etc/yum.repos.d/repo-ef080.repo'
# Thu, 15 Jun 2023 01:53:41 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Thu, 15 Jun 2023 01:53:42 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Thu, 22 Jun 2023 01:08:18 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 22 Jun 2023 01:08:18 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 22 Jun 2023 01:08:18 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 22 Jun 2023 01:08:25 GMT
RUN microdnf install -y binutils tzdata openssl wget ca-certificates fontconfig glibc-langpack-en gzip tar     && microdnf clean all
# Wed, 26 Jul 2023 00:53:56 GMT
ENV JAVA_VERSION=jdk-11.0.20+8
# Wed, 26 Jul 2023 00:54:04 GMT
RUN set -eux;     ARCH="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')";     case "${ARCH}" in        aarch64|arm64)          ESUM='eb821c049c2d2f7c3fbf8ddcce2d608d3aa7d488700e76bfbbebabba93021748';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.20%2B8/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.20_8.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='1125931b3a38e6e305a1932fc6cfd0b023a0fbec2cab10e835a2ee2c50848b42';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.20%2B8/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.20_8.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='688c83d9edf2204220df94ce5bab4a6d19f3d91bc0e500f31dda41e16d9a383f';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.20%2B8/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.20_8.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='7a99258af2e3ee9047e90f1c0c1775fd6285085759501295358d934d662e01f9';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.20%2B8/OpenJDK11U-jdk_x64_linux_hotspot_11.0.20_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;
# Wed, 26 Jul 2023 00:54:07 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Wed, 26 Jul 2023 00:54:07 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:62742f27dce5ebff467a57ad6bfa680820f3bc534cc313627f8113246276bf0f`  
		Last Modified: Wed, 21 Jun 2023 18:10:35 GMT  
		Size: 37.8 MB (37833161 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd89fad3074e960a219b14c1d9389a3f59012f3496f87a126808d6aef4ac84ee`  
		Last Modified: Thu, 22 Jun 2023 01:11:48 GMT  
		Size: 27.9 MB (27864943 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0a15b94426788457dd9e67b9f224a2bea01c1fafe4412f87f46bbc3c2fb6797`  
		Last Modified: Wed, 26 Jul 2023 00:58:47 GMT  
		Size: 141.3 MB (141291824 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28055bd58311fddec71309b6538daf7611beef53b9bd6bb01a6caf579d82bbf8`  
		Last Modified: Wed, 26 Jul 2023 00:58:36 GMT  
		Size: 178.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:11-jdk-ubi9-minimal` - linux; arm64 variant v8

```console
$ docker pull eclipse-temurin@sha256:c8303515b2a50303275187b95c5d69d381a275c23ede8a24e33caa58965b71e9
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **202.5 MB (202463738 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:70750a99e762fe192f68e06ba47d4f312349c548a170d5c626cdb4703a7cf8df`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 15 Jun 2023 01:53:37 GMT
ADD file:2ddf47843f2f56bf055d8a2d5a986816d35279705fd72a482cc996e557eb4d0d in / 
# Thu, 15 Jun 2023 01:53:38 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Thu, 15 Jun 2023 01:53:38 GMT
ADD file:214c1de395c24e4a86ef9a706069ef30a9e804c63f851c37c35655e16fea3ced in /tmp/tls-ca-bundle.pem 
# Thu, 15 Jun 2023 01:53:38 GMT
ADD multi:9849bd0aefa7f9f98ad6e5e3688cb1fbc7313bd1a292ba10ed260c50163f7cee in /etc/yum.repos.d/ 
# Thu, 15 Jun 2023 01:53:38 GMT
LABEL maintainer="Red Hat, Inc."
# Thu, 15 Jun 2023 01:53:38 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.2"
# Thu, 15 Jun 2023 01:53:38 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Thu, 15 Jun 2023 01:53:38 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Thu, 15 Jun 2023 01:53:38 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 15 Jun 2023 01:53:38 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Thu, 15 Jun 2023 01:53:38 GMT
LABEL io.openshift.expose-services=""
# Thu, 15 Jun 2023 01:53:38 GMT
LABEL io.openshift.tags="minimal rhel9"
# Thu, 15 Jun 2023 01:53:38 GMT
ENV container oci
# Thu, 15 Jun 2023 01:53:38 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 15 Jun 2023 01:53:38 GMT
CMD ["/bin/bash"]
# Thu, 15 Jun 2023 01:53:39 GMT
RUN rm -rf /var/log/*
# Thu, 15 Jun 2023 01:53:39 GMT
LABEL release=691
# Thu, 15 Jun 2023 01:53:39 GMT
ADD file:266cf5a0a08ad49bce286a2a6e6ed92bb75eaeccf0647ce1785fde528a6e4ce7 in /root/buildinfo/content_manifests/ubi9-minimal-container-9.2-691.json 
# Thu, 15 Jun 2023 01:53:39 GMT
ADD file:fd14cf6ab7b729a931fbee6ca52647a4566540b77950a20a9e14019b02a75ae8 in /root/buildinfo/Dockerfile-ubi9-minimal-9.2-691 
# Thu, 15 Jun 2023 01:53:39 GMT
LABEL "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2023-06-15T01:42:07" "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="7ef59505f75bf0c11c8d3addefebee5ceaaf4c41" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi9-minimal/images/9.2-691"
# Thu, 15 Jun 2023 01:53:41 GMT
RUN rm -f '/etc/yum.repos.d/repo-dc573.repo' '/etc/yum.repos.d/repo-ef080.repo'
# Thu, 15 Jun 2023 01:53:42 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Thu, 15 Jun 2023 01:53:43 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Thu, 22 Jun 2023 01:22:21 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 22 Jun 2023 01:22:21 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 22 Jun 2023 01:22:21 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 22 Jun 2023 01:22:29 GMT
RUN microdnf install -y binutils tzdata openssl wget ca-certificates fontconfig glibc-langpack-en gzip tar     && microdnf clean all
# Wed, 26 Jul 2023 00:37:47 GMT
ENV JAVA_VERSION=jdk-11.0.20+8
# Wed, 26 Jul 2023 00:37:55 GMT
RUN set -eux;     ARCH="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')";     case "${ARCH}" in        aarch64|arm64)          ESUM='eb821c049c2d2f7c3fbf8ddcce2d608d3aa7d488700e76bfbbebabba93021748';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.20%2B8/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.20_8.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='1125931b3a38e6e305a1932fc6cfd0b023a0fbec2cab10e835a2ee2c50848b42';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.20%2B8/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.20_8.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='688c83d9edf2204220df94ce5bab4a6d19f3d91bc0e500f31dda41e16d9a383f';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.20%2B8/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.20_8.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='7a99258af2e3ee9047e90f1c0c1775fd6285085759501295358d934d662e01f9';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.20%2B8/OpenJDK11U-jdk_x64_linux_hotspot_11.0.20_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;
# Wed, 26 Jul 2023 00:37:58 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Wed, 26 Jul 2023 00:37:58 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:4933b799093955850acfb98487d4801e9a478436ebdbe4db2585569f7dfc7a73`  
		Last Modified: Wed, 21 Jun 2023 18:10:47 GMT  
		Size: 36.1 MB (36137191 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:221abf6c7eabaab989c2b30a6ba34fbf0d167b44ff1c2c8ad78d55925af18fe9`  
		Last Modified: Thu, 22 Jun 2023 01:25:14 GMT  
		Size: 28.3 MB (28296608 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38e4475285c15e1c69cbac280cbf922319ca7bce227439debbfbf4a33f63b4cf`  
		Last Modified: Wed, 26 Jul 2023 00:40:44 GMT  
		Size: 138.0 MB (138029762 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7bec85460a10935cca06f450a93cedc9ddd532689a1df87e17253474a43670f`  
		Last Modified: Wed, 26 Jul 2023 00:40:36 GMT  
		Size: 177.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:11-jdk-ubi9-minimal` - linux; ppc64le

```console
$ docker pull eclipse-temurin@sha256:b5ea277e196100ba17a18e18eb5373ea5d6710aa7b7b9df12bbac1816e05653f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **201.2 MB (201178947 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e5fd352e6affe047c631721e0ebf3064f29d45931c6c172d98743404b05aaac`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 15 Jun 2023 01:54:23 GMT
ADD file:c1d758c5131eb31c12267045c3ab457513fcf413dda42a4641fa6e60cf265fd3 in / 
# Thu, 15 Jun 2023 01:54:24 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Thu, 15 Jun 2023 01:54:24 GMT
ADD file:214c1de395c24e4a86ef9a706069ef30a9e804c63f851c37c35655e16fea3ced in /tmp/tls-ca-bundle.pem 
# Thu, 15 Jun 2023 01:54:24 GMT
ADD multi:9849bd0aefa7f9f98ad6e5e3688cb1fbc7313bd1a292ba10ed260c50163f7cee in /etc/yum.repos.d/ 
# Thu, 15 Jun 2023 01:54:24 GMT
LABEL maintainer="Red Hat, Inc."
# Thu, 15 Jun 2023 01:54:24 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.2"
# Thu, 15 Jun 2023 01:54:24 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Thu, 15 Jun 2023 01:54:24 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Thu, 15 Jun 2023 01:54:24 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 15 Jun 2023 01:54:24 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Thu, 15 Jun 2023 01:54:24 GMT
LABEL io.openshift.expose-services=""
# Thu, 15 Jun 2023 01:54:24 GMT
LABEL io.openshift.tags="minimal rhel9"
# Thu, 15 Jun 2023 01:54:24 GMT
ENV container oci
# Thu, 15 Jun 2023 01:54:24 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 15 Jun 2023 01:54:24 GMT
CMD ["/bin/bash"]
# Thu, 15 Jun 2023 01:54:26 GMT
RUN rm -rf /var/log/*
# Thu, 15 Jun 2023 01:54:26 GMT
LABEL release=691
# Thu, 15 Jun 2023 01:54:26 GMT
ADD file:0eda173520172f76a0b725b37803c57a32c1391cda8419639363f4c2b7f4ac18 in /root/buildinfo/content_manifests/ubi9-minimal-container-9.2-691.json 
# Thu, 15 Jun 2023 01:54:26 GMT
ADD file:5a376fbc447f597f91a76df815d29f894dce397f746be88bd73c0c852bd868aa in /root/buildinfo/Dockerfile-ubi9-minimal-9.2-691 
# Thu, 15 Jun 2023 01:54:26 GMT
LABEL "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2023-06-15T01:42:07" "architecture"="ppc64le" "vcs-type"="git" "vcs-ref"="7ef59505f75bf0c11c8d3addefebee5ceaaf4c41" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi9-minimal/images/9.2-691"
# Thu, 15 Jun 2023 01:54:27 GMT
RUN rm -f '/etc/yum.repos.d/repo-dc573.repo' '/etc/yum.repos.d/repo-ef080.repo'
# Thu, 15 Jun 2023 01:54:29 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Thu, 15 Jun 2023 01:54:30 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Thu, 22 Jun 2023 01:15:23 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 22 Jun 2023 01:15:24 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 22 Jun 2023 01:15:24 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 22 Jun 2023 01:15:54 GMT
RUN microdnf install -y binutils tzdata openssl wget ca-certificates fontconfig glibc-langpack-en gzip tar     && microdnf clean all
# Wed, 26 Jul 2023 00:18:23 GMT
ENV JAVA_VERSION=jdk-11.0.20+8
# Wed, 26 Jul 2023 00:18:43 GMT
RUN set -eux;     ARCH="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')";     case "${ARCH}" in        aarch64|arm64)          ESUM='eb821c049c2d2f7c3fbf8ddcce2d608d3aa7d488700e76bfbbebabba93021748';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.20%2B8/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.20_8.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='1125931b3a38e6e305a1932fc6cfd0b023a0fbec2cab10e835a2ee2c50848b42';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.20%2B8/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.20_8.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='688c83d9edf2204220df94ce5bab4a6d19f3d91bc0e500f31dda41e16d9a383f';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.20%2B8/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.20_8.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='7a99258af2e3ee9047e90f1c0c1775fd6285085759501295358d934d662e01f9';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.20%2B8/OpenJDK11U-jdk_x64_linux_hotspot_11.0.20_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;
# Wed, 26 Jul 2023 00:18:50 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Wed, 26 Jul 2023 00:18:50 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:e3f3a1bf0aa97991a0413fbe9daa5105fc285b24b4e2ac14458522802ff4e0ec`  
		Last Modified: Wed, 21 Jun 2023 18:11:05 GMT  
		Size: 42.3 MB (42261485 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d76b5a334e3072ec76c9e2fa0cbaea07673b1437abfa3bdd3c23ed0eca21d193`  
		Last Modified: Thu, 22 Jun 2023 01:19:16 GMT  
		Size: 30.4 MB (30423134 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f980785bbaefbb47e6682c13e0b73215e1f48fea4e086ebe4710bb57fefc842`  
		Last Modified: Wed, 26 Jul 2023 00:24:01 GMT  
		Size: 128.5 MB (128494149 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2977b13533510cfcb3cc554153e790de3cd43634e5f934c0c0ae2313ca3d05e8`  
		Last Modified: Wed, 26 Jul 2023 00:23:43 GMT  
		Size: 179.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:11-jdk-ubi9-minimal` - linux; s390x

```console
$ docker pull eclipse-temurin@sha256:ae6f71eed011adaf3aba9a2ced546137561eae73b27b05f1ab04f6f4ab712432
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **185.6 MB (185598936 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:633a813c66db76c1cb6d344efb1a83532be6007cf971c8018107170d3b210f1b`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 15 Jun 2023 01:54:11 GMT
ADD file:1775ae97b5220749eab6d9503babb3e1efe0851edd912ad8074b248d97008cc6 in / 
# Thu, 15 Jun 2023 01:54:12 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Thu, 15 Jun 2023 01:54:12 GMT
ADD file:214c1de395c24e4a86ef9a706069ef30a9e804c63f851c37c35655e16fea3ced in /tmp/tls-ca-bundle.pem 
# Thu, 15 Jun 2023 01:54:13 GMT
ADD multi:9849bd0aefa7f9f98ad6e5e3688cb1fbc7313bd1a292ba10ed260c50163f7cee in /etc/yum.repos.d/ 
# Thu, 15 Jun 2023 01:54:13 GMT
LABEL maintainer="Red Hat, Inc."
# Thu, 15 Jun 2023 01:54:13 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.2"
# Thu, 15 Jun 2023 01:54:13 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Thu, 15 Jun 2023 01:54:13 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Thu, 15 Jun 2023 01:54:13 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 15 Jun 2023 01:54:13 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Thu, 15 Jun 2023 01:54:13 GMT
LABEL io.openshift.expose-services=""
# Thu, 15 Jun 2023 01:54:13 GMT
LABEL io.openshift.tags="minimal rhel9"
# Thu, 15 Jun 2023 01:54:13 GMT
ENV container oci
# Thu, 15 Jun 2023 01:54:13 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 15 Jun 2023 01:54:13 GMT
CMD ["/bin/bash"]
# Thu, 15 Jun 2023 01:54:14 GMT
RUN rm -rf /var/log/*
# Thu, 15 Jun 2023 01:54:14 GMT
LABEL release=691
# Thu, 15 Jun 2023 01:54:14 GMT
ADD file:432371a4e24db05d750ad4e0b7532faf0193716bb081c6328fb80f0b333cc51d in /root/buildinfo/content_manifests/ubi9-minimal-container-9.2-691.json 
# Thu, 15 Jun 2023 01:54:15 GMT
ADD file:24941b7e43d9d830add98ca27ba9e24220a151f9664be0d6bfdf242d07c75fe8 in /root/buildinfo/Dockerfile-ubi9-minimal-9.2-691 
# Thu, 15 Jun 2023 01:54:15 GMT
LABEL "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2023-06-15T01:42:07" "architecture"="s390x" "vcs-type"="git" "vcs-ref"="7ef59505f75bf0c11c8d3addefebee5ceaaf4c41" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi9-minimal/images/9.2-691"
# Thu, 15 Jun 2023 01:54:16 GMT
RUN rm -f '/etc/yum.repos.d/repo-dc573.repo' '/etc/yum.repos.d/repo-ef080.repo'
# Thu, 15 Jun 2023 01:54:17 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Thu, 15 Jun 2023 01:54:19 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Thu, 22 Jun 2023 10:50:52 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 22 Jun 2023 10:50:52 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 22 Jun 2023 10:50:52 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 22 Jun 2023 10:51:12 GMT
RUN microdnf install -y binutils tzdata openssl wget ca-certificates fontconfig glibc-langpack-en gzip tar     && microdnf clean all
# Wed, 26 Jul 2023 00:42:41 GMT
ENV JAVA_VERSION=jdk-11.0.20+8
# Wed, 26 Jul 2023 00:42:50 GMT
RUN set -eux;     ARCH="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')";     case "${ARCH}" in        aarch64|arm64)          ESUM='eb821c049c2d2f7c3fbf8ddcce2d608d3aa7d488700e76bfbbebabba93021748';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.20%2B8/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.20_8.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='1125931b3a38e6e305a1932fc6cfd0b023a0fbec2cab10e835a2ee2c50848b42';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.20%2B8/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.20_8.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='688c83d9edf2204220df94ce5bab4a6d19f3d91bc0e500f31dda41e16d9a383f';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.20%2B8/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.20_8.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='7a99258af2e3ee9047e90f1c0c1775fd6285085759501295358d934d662e01f9';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.20%2B8/OpenJDK11U-jdk_x64_linux_hotspot_11.0.20_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;
# Wed, 26 Jul 2023 00:42:56 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Wed, 26 Jul 2023 00:42:56 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:39b28ee62fc117719f2eda7966033df48e130840bc47191d514b060095150ad3`  
		Last Modified: Wed, 21 Jun 2023 18:11:16 GMT  
		Size: 36.1 MB (36138929 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d634303d8e857e7d44c63bde0fba9c4dc0e91855fd9ba333358865a7529b8c0`  
		Last Modified: Thu, 22 Jun 2023 10:53:58 GMT  
		Size: 27.9 MB (27917054 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78cad07c65308366231070d629111c02c33972189b505f2c2fe31a441da231f6`  
		Last Modified: Wed, 26 Jul 2023 00:45:27 GMT  
		Size: 121.5 MB (121542776 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db3bde6d7623a279228d044bdc6ef3980e4a6d4edcb2c92811456da9dac0aebf`  
		Last Modified: Wed, 26 Jul 2023 00:45:18 GMT  
		Size: 177.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
