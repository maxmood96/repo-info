## `eclipse-temurin:22_36-jre-ubi9-minimal`

```console
$ docker pull eclipse-temurin@sha256:625b45bd3e16539d6e49040a596957368a8459b44fb49a840098da7fe7fac5f5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `eclipse-temurin:22_36-jre-ubi9-minimal` - linux; amd64

```console
$ docker pull eclipse-temurin@sha256:9050df6b16195368e881063e23120b54073f0ca74739df4bb08e477901ed5d96
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **106.7 MB (106740751 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc683d1ade3877e50615821b6036eff807802363289084af71dd96655e147b7e`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`

```dockerfile
# Wed, 17 Jan 2024 19:18:25 GMT
ADD file:f74dfa5d345e76f1f4d9df6077b0cdeaa5b5171f6b548ed1cac475f14515a809 in / 
# Wed, 17 Jan 2024 19:18:26 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Wed, 17 Jan 2024 19:18:27 GMT
ADD file:ecc29a1455ca1b7c82018555e16e2e802135974523df6748e431f8707e759ddd in /tmp/tls-ca-bundle.pem 
# Wed, 17 Jan 2024 19:18:27 GMT
ADD multi:655128808f9801300e5f5790b55c073636035214aee6c75e0582afd288da8973 in /etc/yum.repos.d/ 
# Wed, 17 Jan 2024 19:18:27 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 17 Jan 2024 19:18:27 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.3"
# Wed, 17 Jan 2024 19:18:27 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 17 Jan 2024 19:18:27 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Wed, 17 Jan 2024 19:18:27 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 17 Jan 2024 19:18:27 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Wed, 17 Jan 2024 19:18:27 GMT
LABEL io.openshift.expose-services=""
# Wed, 17 Jan 2024 19:18:27 GMT
LABEL io.openshift.tags="minimal rhel9"
# Wed, 17 Jan 2024 19:18:27 GMT
ENV container oci
# Wed, 17 Jan 2024 19:18:27 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 17 Jan 2024 19:18:27 GMT
CMD ["/bin/bash"]
# Wed, 17 Jan 2024 19:18:28 GMT
RUN rm -rf /var/log/*
# Wed, 17 Jan 2024 19:18:28 GMT
LABEL release=1552
# Wed, 17 Jan 2024 19:18:28 GMT
ADD file:ef91ccf9344b424c8ead898c7856a891de97edf7461478fa846b6deffe2e8379 in /root/buildinfo/content_manifests/ubi9-minimal-container-9.3-1552.json 
# Wed, 17 Jan 2024 19:18:28 GMT
ADD file:75532600b86e8dbdc355d76b86fe28e825754c0d0a529f9282427ca23ab066ef in /root/buildinfo/Dockerfile-ubi9-minimal-9.3-1552 
# Wed, 17 Jan 2024 19:18:28 GMT
LABEL "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2024-01-17T19:05:39" "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="e8510c65a9be4b0635372fd09bee126ce7e08bc7" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi9-minimal/images/9.3-1552"
# Wed, 17 Jan 2024 19:18:29 GMT
RUN rm -f '/etc/yum.repos.d/repo-cbf3a.repo' '/etc/yum.repos.d/repo-a4968.repo'
# Wed, 17 Jan 2024 19:18:29 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Wed, 17 Jan 2024 19:18:31 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Wed, 27 Mar 2024 15:44:12 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 27 Mar 2024 15:44:12 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 27 Mar 2024 15:44:12 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 27 Mar 2024 15:44:12 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         fontconfig         glibc-langpack-en     ;     microdnf clean all # buildkit
# Wed, 27 Mar 2024 15:44:12 GMT
ENV JAVA_VERSION=jdk-22+36
# Wed, 27 Mar 2024 15:44:12 GMT
RUN set -eux;     ARCH="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')";     case "${ARCH}" in        aarch64|arm64)          ESUM='4748e5024eb0251ddf0f576e4c56d21270b1f2186f62b25fc1d89c888d742ed4';          BINARY_URL='https://github.com/adoptium/temurin22-binaries/releases/download/jdk-22%2B36/OpenJDK22U-jre_aarch64_linux_hotspot_22_36.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='faceda94ffd16e177cb674471f29789e48378f9f190eac8523713a0cb3324be9';          BINARY_URL='https://github.com/adoptium/temurin22-binaries/releases/download/jdk-22%2B36/OpenJDK22U-jre_x64_linux_hotspot_22_36.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='e1cce04600b388777a1a278dda572a664db14cea034dc131155b3da5e6e885e5';          BINARY_URL='https://github.com/adoptium/temurin22-binaries/releases/download/jdk-22%2B36/OpenJDK22U-jre_ppc64le_linux_hotspot_22_36.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Wed, 27 Mar 2024 15:44:12 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 27 Mar 2024 15:44:12 GMT
COPY entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 27 Mar 2024 15:44:12 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
```

-	Layers:
	-	`sha256:0765fffac8ba6e6750a4f53defaa3c6361fb9dd8a72d4aa3eecea0b6a9d035dd`  
		Last Modified: Thu, 25 Jan 2024 16:53:03 GMT  
		Size: 37.7 MB (37721772 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63acc1c5de9b94bdc730c8889f3d45a67690208601712550866373557cc3a582`  
		Last Modified: Thu, 28 Mar 2024 02:04:08 GMT  
		Size: 15.6 MB (15553473 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bfbbf87358369f6a98d2482ff3f25be8f0a75e01377d402098c33f8fbabd786f`  
		Last Modified: Thu, 28 Mar 2024 02:15:07 GMT  
		Size: 53.5 MB (53464637 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:286026a2482b297f985126bca837b784cb254b48ab80fa63c6341a7610d51f10`  
		Last Modified: Thu, 28 Mar 2024 02:15:00 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0843d41fecfd64a89bbc9dff6f1f7dbce542794734f08e332ae0870b12a26da4`  
		Last Modified: Thu, 28 Mar 2024 02:15:00 GMT  
		Size: 709.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:22_36-jre-ubi9-minimal` - linux; arm64 variant v8

```console
$ docker pull eclipse-temurin@sha256:20f194f26423967f9dde8799e2f9ac2a154ab23fa5d02fcb5c59f8b3f244e9ea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **104.2 MB (104167547 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e670c3b8103509d63d4eda662c2b94efe53b481c3a8a0d1bd70cd0d93cfbf540`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`

```dockerfile
# Wed, 17 Jan 2024 19:18:24 GMT
ADD file:a7c0bdd56d7a77d1a191f8c8ed79585935e74fd20271d6124981f2cbafd9a3e5 in / 
# Wed, 17 Jan 2024 19:18:25 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Wed, 17 Jan 2024 19:18:25 GMT
ADD file:ecc29a1455ca1b7c82018555e16e2e802135974523df6748e431f8707e759ddd in /tmp/tls-ca-bundle.pem 
# Wed, 17 Jan 2024 19:18:25 GMT
ADD multi:655128808f9801300e5f5790b55c073636035214aee6c75e0582afd288da8973 in /etc/yum.repos.d/ 
# Wed, 17 Jan 2024 19:18:25 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 17 Jan 2024 19:18:25 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.3"
# Wed, 17 Jan 2024 19:18:25 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 17 Jan 2024 19:18:25 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Wed, 17 Jan 2024 19:18:25 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 17 Jan 2024 19:18:25 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Wed, 17 Jan 2024 19:18:25 GMT
LABEL io.openshift.expose-services=""
# Wed, 17 Jan 2024 19:18:25 GMT
LABEL io.openshift.tags="minimal rhel9"
# Wed, 17 Jan 2024 19:18:25 GMT
ENV container oci
# Wed, 17 Jan 2024 19:18:25 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 17 Jan 2024 19:18:25 GMT
CMD ["/bin/bash"]
# Wed, 17 Jan 2024 19:18:27 GMT
RUN rm -rf /var/log/*
# Wed, 17 Jan 2024 19:18:27 GMT
LABEL release=1552
# Wed, 17 Jan 2024 19:18:27 GMT
ADD file:bfcc8382df280418e841771f63af4ab23c26bfdabccba49320eca21344392059 in /root/buildinfo/content_manifests/ubi9-minimal-container-9.3-1552.json 
# Wed, 17 Jan 2024 19:18:27 GMT
ADD file:855fc5d4bbaa177d330e050fbde5d82d06b15af68fb9fcc1051cfdaafc7dcc07 in /root/buildinfo/Dockerfile-ubi9-minimal-9.3-1552 
# Wed, 17 Jan 2024 19:18:27 GMT
LABEL "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2024-01-17T19:05:39" "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="e8510c65a9be4b0635372fd09bee126ce7e08bc7" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi9-minimal/images/9.3-1552"
# Wed, 17 Jan 2024 19:18:28 GMT
RUN rm -f '/etc/yum.repos.d/repo-cbf3a.repo' '/etc/yum.repos.d/repo-a4968.repo'
# Wed, 17 Jan 2024 19:18:30 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Wed, 17 Jan 2024 19:18:32 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Wed, 27 Mar 2024 15:44:12 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 27 Mar 2024 15:44:12 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 27 Mar 2024 15:44:12 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 27 Mar 2024 15:44:12 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         fontconfig         glibc-langpack-en     ;     microdnf clean all # buildkit
# Wed, 27 Mar 2024 15:44:12 GMT
ENV JAVA_VERSION=jdk-22+36
# Wed, 27 Mar 2024 15:44:12 GMT
RUN set -eux;     ARCH="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')";     case "${ARCH}" in        aarch64|arm64)          ESUM='4748e5024eb0251ddf0f576e4c56d21270b1f2186f62b25fc1d89c888d742ed4';          BINARY_URL='https://github.com/adoptium/temurin22-binaries/releases/download/jdk-22%2B36/OpenJDK22U-jre_aarch64_linux_hotspot_22_36.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='faceda94ffd16e177cb674471f29789e48378f9f190eac8523713a0cb3324be9';          BINARY_URL='https://github.com/adoptium/temurin22-binaries/releases/download/jdk-22%2B36/OpenJDK22U-jre_x64_linux_hotspot_22_36.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='e1cce04600b388777a1a278dda572a664db14cea034dc131155b3da5e6e885e5';          BINARY_URL='https://github.com/adoptium/temurin22-binaries/releases/download/jdk-22%2B36/OpenJDK22U-jre_ppc64le_linux_hotspot_22_36.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Wed, 27 Mar 2024 15:44:12 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 27 Mar 2024 15:44:12 GMT
COPY entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 27 Mar 2024 15:44:12 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
```

-	Layers:
	-	`sha256:5995d2c3a044ca24b3d19b7e7e55d359fc18627baa8aef944edb65b14383cefc`  
		Last Modified: Thu, 25 Jan 2024 16:53:01 GMT  
		Size: 36.0 MB (36049053 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a449b367a2d349cbebf401a06fd0ca92b6c554a6a2e5f6fd06a080dc0a25cde8`  
		Last Modified: Thu, 28 Mar 2024 00:49:15 GMT  
		Size: 15.6 MB (15609081 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10faab9dd0fafd637f3b5ad01ba9404aa96fb7392be06eba1b60afd1c8741982`  
		Last Modified: Thu, 28 Mar 2024 00:57:54 GMT  
		Size: 52.5 MB (52508542 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7228c24376370cd29c2a57c0e0a2633cf058eef69f2d8a27f9c6e0ffb480349`  
		Last Modified: Thu, 28 Mar 2024 00:57:48 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ddd6a2cc0923afd99f953c2ff77cc966a5ad304a33c1ee1342293527d4072a77`  
		Last Modified: Thu, 28 Mar 2024 00:57:48 GMT  
		Size: 711.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:22_36-jre-ubi9-minimal` - linux; ppc64le

```console
$ docker pull eclipse-temurin@sha256:1d21cc8ba60de612db13ba81c92c7a1d27627d1b0bde08d808ff720464befabb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.1 MB (114062187 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a1ed927a96c303620a45886e79fb627256999770b5d2ca397ab14ca8dbd2796`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`

```dockerfile
# Wed, 17 Jan 2024 19:19:03 GMT
ADD file:df0617a0702d6fcc11ee30e344357a75c6c91c5e5eb174951aad6c5cef0e845b in / 
# Wed, 17 Jan 2024 19:19:06 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Wed, 17 Jan 2024 19:19:06 GMT
ADD file:ecc29a1455ca1b7c82018555e16e2e802135974523df6748e431f8707e759ddd in /tmp/tls-ca-bundle.pem 
# Wed, 17 Jan 2024 19:19:07 GMT
ADD multi:655128808f9801300e5f5790b55c073636035214aee6c75e0582afd288da8973 in /etc/yum.repos.d/ 
# Wed, 17 Jan 2024 19:19:07 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 17 Jan 2024 19:19:07 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.3"
# Wed, 17 Jan 2024 19:19:07 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 17 Jan 2024 19:19:07 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Wed, 17 Jan 2024 19:19:07 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 17 Jan 2024 19:19:07 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Wed, 17 Jan 2024 19:19:07 GMT
LABEL io.openshift.expose-services=""
# Wed, 17 Jan 2024 19:19:07 GMT
LABEL io.openshift.tags="minimal rhel9"
# Wed, 17 Jan 2024 19:19:07 GMT
ENV container oci
# Wed, 17 Jan 2024 19:19:07 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 17 Jan 2024 19:19:07 GMT
CMD ["/bin/bash"]
# Wed, 17 Jan 2024 19:19:10 GMT
RUN rm -rf /var/log/*
# Wed, 17 Jan 2024 19:19:10 GMT
LABEL release=1552
# Wed, 17 Jan 2024 19:19:10 GMT
ADD file:3f468e77179542afdf211420f105b5678cd54f2e899d127556bc80a014fbae6a in /root/buildinfo/content_manifests/ubi9-minimal-container-9.3-1552.json 
# Wed, 17 Jan 2024 19:19:10 GMT
ADD file:aeb01c9a1302a02244512fc6820189c5bc5001c9a42470420da268fb1cee5295 in /root/buildinfo/Dockerfile-ubi9-minimal-9.3-1552 
# Wed, 17 Jan 2024 19:19:10 GMT
LABEL "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2024-01-17T19:05:39" "architecture"="ppc64le" "vcs-type"="git" "vcs-ref"="e8510c65a9be4b0635372fd09bee126ce7e08bc7" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi9-minimal/images/9.3-1552"
# Wed, 17 Jan 2024 19:19:13 GMT
RUN rm -f '/etc/yum.repos.d/repo-cbf3a.repo' '/etc/yum.repos.d/repo-a4968.repo'
# Wed, 17 Jan 2024 19:19:16 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Wed, 17 Jan 2024 19:19:21 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Wed, 27 Mar 2024 15:44:12 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 27 Mar 2024 15:44:12 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 27 Mar 2024 15:44:12 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 27 Mar 2024 15:44:12 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         fontconfig         glibc-langpack-en     ;     microdnf clean all # buildkit
# Wed, 27 Mar 2024 15:44:12 GMT
ENV JAVA_VERSION=jdk-22+36
# Wed, 27 Mar 2024 15:44:12 GMT
RUN set -eux;     ARCH="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')";     case "${ARCH}" in        aarch64|arm64)          ESUM='4748e5024eb0251ddf0f576e4c56d21270b1f2186f62b25fc1d89c888d742ed4';          BINARY_URL='https://github.com/adoptium/temurin22-binaries/releases/download/jdk-22%2B36/OpenJDK22U-jre_aarch64_linux_hotspot_22_36.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='faceda94ffd16e177cb674471f29789e48378f9f190eac8523713a0cb3324be9';          BINARY_URL='https://github.com/adoptium/temurin22-binaries/releases/download/jdk-22%2B36/OpenJDK22U-jre_x64_linux_hotspot_22_36.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='e1cce04600b388777a1a278dda572a664db14cea034dc131155b3da5e6e885e5';          BINARY_URL='https://github.com/adoptium/temurin22-binaries/releases/download/jdk-22%2B36/OpenJDK22U-jre_ppc64le_linux_hotspot_22_36.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Wed, 27 Mar 2024 15:44:12 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 27 Mar 2024 15:44:12 GMT
COPY entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 27 Mar 2024 15:44:12 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
```

-	Layers:
	-	`sha256:d8e558e99693b636a7ac64b024a003c505239316a353b7663603283057bcb110`  
		Last Modified: Thu, 25 Jan 2024 18:08:23 GMT  
		Size: 42.1 MB (42101515 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1df6c4cf99c4441e36b5e826a7491f0ebb1fffa2c853dd5744553325b46aa470`  
		Last Modified: Thu, 28 Mar 2024 01:41:13 GMT  
		Size: 18.9 MB (18851495 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:118149e863ab187565ef59dc49e0cbcf234cd643ade389a45a68d2bd614d44bd`  
		Last Modified: Thu, 28 Mar 2024 01:51:03 GMT  
		Size: 53.1 MB (53108306 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ceb057768a95af679b264ca9c15503643a5c283a0448f7c0b8ca14c496b4f60`  
		Last Modified: Thu, 28 Mar 2024 01:50:55 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac2bbe2b607b32d07af52ba395747591c6676360b18149104f1df779b9008970`  
		Last Modified: Thu, 28 Mar 2024 01:50:55 GMT  
		Size: 711.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
