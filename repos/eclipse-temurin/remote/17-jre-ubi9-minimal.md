## `eclipse-temurin:17-jre-ubi9-minimal`

```console
$ docker pull eclipse-temurin@sha256:ce22025a0a8cee9474211a5ed07b1e771e1f8453130179895a9fd4854eb95b85
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `eclipse-temurin:17-jre-ubi9-minimal` - linux; amd64

```console
$ docker pull eclipse-temurin@sha256:9f429570df50ea4f597740e0d665f3e31eee31b29b1ced533ac5b319e1ba3665
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **113.6 MB (113566688 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f135ec10cce16920baaeff090fdac2f8a2d6a2972a20e571ed3f429fe8fc910`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`

```dockerfile
# Thu, 29 Feb 2024 14:19:45 GMT
ADD file:68e24d23b5f22084b226415d33dd1fcc53f68b0b3949e70fad3179e338fc8077 in / 
# Thu, 29 Feb 2024 14:19:46 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Thu, 29 Feb 2024 14:19:46 GMT
ADD file:ecc29a1455ca1b7c82018555e16e2e802135974523df6748e431f8707e759ddd in /tmp/tls-ca-bundle.pem 
# Thu, 29 Feb 2024 14:19:46 GMT
ADD multi:76ed2bd9c036240d42925ff871f73866e886bea98859bc8c40c9fb05e07b6fb9 in /etc/yum.repos.d/ 
# Thu, 29 Feb 2024 14:19:46 GMT
LABEL maintainer="Red Hat, Inc."
# Thu, 29 Feb 2024 14:19:46 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.3"
# Thu, 29 Feb 2024 14:19:46 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Thu, 29 Feb 2024 14:19:46 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Thu, 29 Feb 2024 14:19:46 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 29 Feb 2024 14:19:46 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Thu, 29 Feb 2024 14:19:46 GMT
LABEL io.openshift.expose-services=""
# Thu, 29 Feb 2024 14:19:46 GMT
LABEL io.openshift.tags="minimal rhel9"
# Thu, 29 Feb 2024 14:19:46 GMT
ENV container oci
# Thu, 29 Feb 2024 14:19:46 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 29 Feb 2024 14:19:46 GMT
CMD ["/bin/bash"]
# Thu, 29 Feb 2024 14:19:47 GMT
RUN rm -rf /var/log/*
# Thu, 29 Feb 2024 14:19:47 GMT
LABEL release=1612
# Thu, 29 Feb 2024 14:19:47 GMT
ADD file:96798c96d3dfcbd827cc4604cb7c680f64dbd1730ae16ef972d4c8c1724e5dfb in /root/buildinfo/content_manifests/ubi9-minimal-container-9.3-1612.json 
# Thu, 29 Feb 2024 14:19:47 GMT
ADD file:77a2a326b0f16be9a06e11649cf96f606502d3b242d11c8f6562a4f7c2b91d9d in /root/buildinfo/Dockerfile-ubi9-minimal-9.3-1612 
# Thu, 29 Feb 2024 14:19:47 GMT
LABEL "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2024-02-29T14:02:27" "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="e8510c65a9be4b0635372fd09bee126ce7e08bc7" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi9-minimal/images/9.3-1612"
# Thu, 29 Feb 2024 14:19:48 GMT
RUN rm -f '/etc/yum.repos.d/repo-3cf8a.repo' '/etc/yum.repos.d/repo-e6c6f.repo'
# Thu, 29 Feb 2024 14:19:48 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Thu, 29 Feb 2024 14:19:49 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Tue, 23 Apr 2024 20:51:38 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 23 Apr 2024 20:51:38 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 23 Apr 2024 20:51:38 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 23 Apr 2024 20:51:38 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         fontconfig         glibc-langpack-en     ;     microdnf clean all # buildkit
# Tue, 23 Apr 2024 20:51:38 GMT
ENV JAVA_VERSION=jdk-17.0.11+9
# Tue, 23 Apr 2024 20:51:38 GMT
RUN set -eux;     ARCH="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')";     case "${ARCH}" in        aarch64|arm64)          ESUM='ccfa23c25790475c84df983cc5f729b94c04d9ea9863912deb15c6266782cf16';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.11%2B9/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.11_9.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='bcb1b7b8ad68c93093f09b591b7cb17161d39891f7d29d33a586f5a328603707';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.11%2B9/OpenJDK17U-jre_x64_linux_hotspot_17.0.11_9.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='884b5cb817e50010b4d0a3252afb6a80db18995af19bbd16a37348b2c37949bc';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.11%2B9/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.11_9.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='67dd46352ba94f273579a04ef0756408b06db82b1b4ddf050045c226212f76fd';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.11%2B9/OpenJDK17U-jre_s390x_linux_hotspot_17.0.11_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Tue, 23 Apr 2024 20:51:38 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 23 Apr 2024 20:51:38 GMT
COPY entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 23 Apr 2024 20:51:38 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
```

-	Layers:
	-	`sha256:2895d6faeea81934722a9a23efd8814ca51c1af558a3a70983ad2f7a412cdbe8`  
		Last Modified: Tue, 05 Mar 2024 21:18:08 GMT  
		Size: 37.7 MB (37695188 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:440448b8b996ac596b9214d68c607662000c8e74ad26b922b0283d11eb829154`  
		Last Modified: Mon, 15 Apr 2024 18:58:06 GMT  
		Size: 28.6 MB (28612828 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fac16dd16cc79f1570c3c664cbe12b49ce1d4882b9d910d1d1631794ab485af4`  
		Last Modified: Wed, 24 Apr 2024 19:15:52 GMT  
		Size: 47.3 MB (47257799 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c94b45a4f4f6b0daed964da3bd69f57ed5771e09d239d3b7ca072b511c264353`  
		Last Modified: Wed, 24 Apr 2024 19:15:44 GMT  
		Size: 161.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00038fe29d657c9f73f54b95fc70c85097da6a833b40506b19dd2ecb5297222e`  
		Last Modified: Wed, 24 Apr 2024 19:15:44 GMT  
		Size: 712.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:17-jre-ubi9-minimal` - linux; arm64 variant v8

```console
$ docker pull eclipse-temurin@sha256:06d5368bc588c0118307c29184ceffc501783752c9074d939729b89027fc7a68
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **111.8 MB (111751235 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:520c1abfa4ab50e4fe0f9a89d5b999d2774cbf02e0edd295f1f7ae44009825eb`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`

```dockerfile
# Thu, 29 Feb 2024 14:19:42 GMT
ADD file:437369795a208dae019ad106a8100166db532f040a1b0872857a6e2765904923 in / 
# Thu, 29 Feb 2024 14:19:43 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Thu, 29 Feb 2024 14:19:43 GMT
ADD file:ecc29a1455ca1b7c82018555e16e2e802135974523df6748e431f8707e759ddd in /tmp/tls-ca-bundle.pem 
# Thu, 29 Feb 2024 14:19:43 GMT
ADD multi:76ed2bd9c036240d42925ff871f73866e886bea98859bc8c40c9fb05e07b6fb9 in /etc/yum.repos.d/ 
# Thu, 29 Feb 2024 14:19:43 GMT
LABEL maintainer="Red Hat, Inc."
# Thu, 29 Feb 2024 14:19:43 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.3"
# Thu, 29 Feb 2024 14:19:43 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Thu, 29 Feb 2024 14:19:43 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Thu, 29 Feb 2024 14:19:43 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 29 Feb 2024 14:19:43 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Thu, 29 Feb 2024 14:19:43 GMT
LABEL io.openshift.expose-services=""
# Thu, 29 Feb 2024 14:19:43 GMT
LABEL io.openshift.tags="minimal rhel9"
# Thu, 29 Feb 2024 14:19:43 GMT
ENV container oci
# Thu, 29 Feb 2024 14:19:43 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 29 Feb 2024 14:19:43 GMT
CMD ["/bin/bash"]
# Thu, 29 Feb 2024 14:19:44 GMT
RUN rm -rf /var/log/*
# Thu, 29 Feb 2024 14:19:44 GMT
LABEL release=1612
# Thu, 29 Feb 2024 14:19:44 GMT
ADD file:96d801555bcde0b213796fa230f06bd442ea605a02a35260236e9b419cfd729d in /root/buildinfo/content_manifests/ubi9-minimal-container-9.3-1612.json 
# Thu, 29 Feb 2024 14:19:44 GMT
ADD file:ae24bc70d71374ac8bbfcf5164284b94f4587f14ff3b75af2fe02d3bc797deac in /root/buildinfo/Dockerfile-ubi9-minimal-9.3-1612 
# Thu, 29 Feb 2024 14:19:44 GMT
LABEL "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2024-02-29T14:02:27" "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="e8510c65a9be4b0635372fd09bee126ce7e08bc7" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi9-minimal/images/9.3-1612"
# Thu, 29 Feb 2024 14:19:45 GMT
RUN rm -f '/etc/yum.repos.d/repo-3cf8a.repo' '/etc/yum.repos.d/repo-e6c6f.repo'
# Thu, 29 Feb 2024 14:19:47 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Thu, 29 Feb 2024 14:19:48 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Tue, 23 Apr 2024 20:51:38 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 23 Apr 2024 20:51:38 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 23 Apr 2024 20:51:38 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 23 Apr 2024 20:51:38 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         fontconfig         glibc-langpack-en     ;     microdnf clean all # buildkit
# Tue, 23 Apr 2024 20:51:38 GMT
ENV JAVA_VERSION=jdk-17.0.11+9
# Tue, 23 Apr 2024 20:51:38 GMT
RUN set -eux;     ARCH="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')";     case "${ARCH}" in        aarch64|arm64)          ESUM='ccfa23c25790475c84df983cc5f729b94c04d9ea9863912deb15c6266782cf16';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.11%2B9/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.11_9.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='bcb1b7b8ad68c93093f09b591b7cb17161d39891f7d29d33a586f5a328603707';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.11%2B9/OpenJDK17U-jre_x64_linux_hotspot_17.0.11_9.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='884b5cb817e50010b4d0a3252afb6a80db18995af19bbd16a37348b2c37949bc';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.11%2B9/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.11_9.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='67dd46352ba94f273579a04ef0756408b06db82b1b4ddf050045c226212f76fd';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.11%2B9/OpenJDK17U-jre_s390x_linux_hotspot_17.0.11_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Tue, 23 Apr 2024 20:51:38 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 23 Apr 2024 20:51:38 GMT
COPY entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 23 Apr 2024 20:51:38 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
```

-	Layers:
	-	`sha256:29e2333f8e0bceaa897a773c4379290a140a34c907a4e38ccf82a09fe20181bd`  
		Last Modified: Tue, 05 Mar 2024 21:53:06 GMT  
		Size: 36.0 MB (35983791 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1833003c62adc51f6cc3c367fb7787c6e8b6bdc508130c0ef4323e9e4806e3f`  
		Last Modified: Mon, 15 Apr 2024 18:50:59 GMT  
		Size: 29.0 MB (29049830 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2ce1dd42c2c32e7cd1f20e30b88067f88392de5404e8b87152b8409a1dbf154`  
		Last Modified: Wed, 24 Apr 2024 18:00:07 GMT  
		Size: 46.7 MB (46716742 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b769aacc66c0f50c5c09438bcc97c254247ed8f46035b348f081d72c12aa0bb`  
		Last Modified: Wed, 24 Apr 2024 18:00:02 GMT  
		Size: 161.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8f08e81a108843552ad15bd5655c34551bcfecb540b7adeb171b85fad376ec8`  
		Last Modified: Wed, 24 Apr 2024 18:00:02 GMT  
		Size: 711.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:17-jre-ubi9-minimal` - linux; ppc64le

```console
$ docker pull eclipse-temurin@sha256:ea52f0d046b0304e7152eb138fe419bd553115eb3d6d3113c956139d3d7a4795
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **120.4 MB (120358232 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac48933147c2cc85e57d196c3c4715fd365584ed82f26a6553524fd386ad731a`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`

```dockerfile
# Thu, 29 Feb 2024 14:19:45 GMT
ADD file:e100ce295764ee5bd8795041bb4862d3fb9f62818b8b8e7b65a32cee1fce1afa in / 
# Thu, 29 Feb 2024 14:19:46 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Thu, 29 Feb 2024 14:19:47 GMT
ADD file:ecc29a1455ca1b7c82018555e16e2e802135974523df6748e431f8707e759ddd in /tmp/tls-ca-bundle.pem 
# Thu, 29 Feb 2024 14:19:47 GMT
ADD multi:76ed2bd9c036240d42925ff871f73866e886bea98859bc8c40c9fb05e07b6fb9 in /etc/yum.repos.d/ 
# Thu, 29 Feb 2024 14:19:47 GMT
LABEL maintainer="Red Hat, Inc."
# Thu, 29 Feb 2024 14:19:47 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.3"
# Thu, 29 Feb 2024 14:19:47 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Thu, 29 Feb 2024 14:19:47 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Thu, 29 Feb 2024 14:19:47 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 29 Feb 2024 14:19:47 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Thu, 29 Feb 2024 14:19:47 GMT
LABEL io.openshift.expose-services=""
# Thu, 29 Feb 2024 14:19:47 GMT
LABEL io.openshift.tags="minimal rhel9"
# Thu, 29 Feb 2024 14:19:47 GMT
ENV container oci
# Thu, 29 Feb 2024 14:19:47 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 29 Feb 2024 14:19:47 GMT
CMD ["/bin/bash"]
# Thu, 29 Feb 2024 14:19:48 GMT
RUN rm -rf /var/log/*
# Thu, 29 Feb 2024 14:19:48 GMT
LABEL release=1612
# Thu, 29 Feb 2024 14:19:48 GMT
ADD file:b6e7a73897a55184357ba915feb05b8bf7c348344fa75e8c843db12ccaec3e21 in /root/buildinfo/content_manifests/ubi9-minimal-container-9.3-1612.json 
# Thu, 29 Feb 2024 14:19:48 GMT
ADD file:3c70a25705cace759733fff14c8b2d0e1dc0f21628fff6d121c38656560f65c4 in /root/buildinfo/Dockerfile-ubi9-minimal-9.3-1612 
# Thu, 29 Feb 2024 14:19:48 GMT
LABEL "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2024-02-29T14:02:27" "architecture"="ppc64le" "vcs-type"="git" "vcs-ref"="e8510c65a9be4b0635372fd09bee126ce7e08bc7" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi9-minimal/images/9.3-1612"
# Thu, 29 Feb 2024 14:19:50 GMT
RUN rm -f '/etc/yum.repos.d/repo-3cf8a.repo' '/etc/yum.repos.d/repo-e6c6f.repo'
# Thu, 29 Feb 2024 14:19:51 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Thu, 29 Feb 2024 14:19:53 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Tue, 23 Apr 2024 20:51:38 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 23 Apr 2024 20:51:38 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 23 Apr 2024 20:51:38 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 23 Apr 2024 20:51:38 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         fontconfig         glibc-langpack-en     ;     microdnf clean all # buildkit
# Tue, 23 Apr 2024 20:51:38 GMT
ENV JAVA_VERSION=jdk-17.0.11+9
# Tue, 23 Apr 2024 20:51:38 GMT
RUN set -eux;     ARCH="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')";     case "${ARCH}" in        aarch64|arm64)          ESUM='ccfa23c25790475c84df983cc5f729b94c04d9ea9863912deb15c6266782cf16';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.11%2B9/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.11_9.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='bcb1b7b8ad68c93093f09b591b7cb17161d39891f7d29d33a586f5a328603707';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.11%2B9/OpenJDK17U-jre_x64_linux_hotspot_17.0.11_9.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='884b5cb817e50010b4d0a3252afb6a80db18995af19bbd16a37348b2c37949bc';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.11%2B9/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.11_9.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='67dd46352ba94f273579a04ef0756408b06db82b1b4ddf050045c226212f76fd';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.11%2B9/OpenJDK17U-jre_s390x_linux_hotspot_17.0.11_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Tue, 23 Apr 2024 20:51:38 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 23 Apr 2024 20:51:38 GMT
COPY entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 23 Apr 2024 20:51:38 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
```

-	Layers:
	-	`sha256:c77c514a1cb5c6b968ce2a99c2b9cdd751b585456e06761249027a93afab424f`  
		Last Modified: Fri, 15 Mar 2024 10:54:10 GMT  
		Size: 42.1 MB (42080689 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63ba206225c418784da485680a1a4d57d824add72e88c85419005f79fb4f7b5e`  
		Last Modified: Mon, 15 Apr 2024 19:31:58 GMT  
		Size: 31.2 MB (31174818 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce4efde7cde689ee32a2dbaf1d13a98117780af07fe5f5b36ed206b756c18c64`  
		Last Modified: Wed, 24 Apr 2024 17:49:33 GMT  
		Size: 47.1 MB (47101855 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:216c5e9966b35aaa819dca2c12d2b37c9a5b5577d1157b2f3515a595d9da4e19`  
		Last Modified: Wed, 24 Apr 2024 17:49:25 GMT  
		Size: 159.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0297da6dacc02fd9db4c63d14b4abeaaec4e25c1cd0ffbe72a0990bfd6fbdf0`  
		Last Modified: Wed, 24 Apr 2024 17:49:25 GMT  
		Size: 711.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:17-jre-ubi9-minimal` - linux; s390x

```console
$ docker pull eclipse-temurin@sha256:8960a09afe6eb2c839ef8b1517d9468c31aee007ae89071ff7dd9f9aa9f10a46
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **108.4 MB (108436780 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d3543a64f64319cf01f6bad6d67da54c7190b8341c71772115faa344df553db`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`

```dockerfile
# Thu, 29 Feb 2024 14:19:45 GMT
ADD file:465c4ec12c3e7a2bfc5cd03e9f3aa6a19dedcdc752e13bb403061a90fa926352 in / 
# Thu, 29 Feb 2024 14:19:46 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Thu, 29 Feb 2024 14:19:46 GMT
ADD file:ecc29a1455ca1b7c82018555e16e2e802135974523df6748e431f8707e759ddd in /tmp/tls-ca-bundle.pem 
# Thu, 29 Feb 2024 14:19:46 GMT
ADD multi:76ed2bd9c036240d42925ff871f73866e886bea98859bc8c40c9fb05e07b6fb9 in /etc/yum.repos.d/ 
# Thu, 29 Feb 2024 14:19:46 GMT
LABEL maintainer="Red Hat, Inc."
# Thu, 29 Feb 2024 14:19:46 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.3"
# Thu, 29 Feb 2024 14:19:46 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Thu, 29 Feb 2024 14:19:46 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Thu, 29 Feb 2024 14:19:46 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 29 Feb 2024 14:19:46 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Thu, 29 Feb 2024 14:19:46 GMT
LABEL io.openshift.expose-services=""
# Thu, 29 Feb 2024 14:19:46 GMT
LABEL io.openshift.tags="minimal rhel9"
# Thu, 29 Feb 2024 14:19:46 GMT
ENV container oci
# Thu, 29 Feb 2024 14:19:46 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 29 Feb 2024 14:19:46 GMT
CMD ["/bin/bash"]
# Thu, 29 Feb 2024 14:19:47 GMT
RUN rm -rf /var/log/*
# Thu, 29 Feb 2024 14:19:47 GMT
LABEL release=1612
# Thu, 29 Feb 2024 14:19:47 GMT
ADD file:7fb44a99d2f255cdb26a060af528a42b2a203a2f6c3b4d3b6308869c46735761 in /root/buildinfo/content_manifests/ubi9-minimal-container-9.3-1612.json 
# Thu, 29 Feb 2024 14:19:48 GMT
ADD file:fa6f2decc3fbdf555d09f8bf18bf1ba4ccadf833c3e66c953a84d3fd68c58c72 in /root/buildinfo/Dockerfile-ubi9-minimal-9.3-1612 
# Thu, 29 Feb 2024 14:19:48 GMT
LABEL "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2024-02-29T14:02:27" "architecture"="s390x" "vcs-type"="git" "vcs-ref"="e8510c65a9be4b0635372fd09bee126ce7e08bc7" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi9-minimal/images/9.3-1612"
# Thu, 29 Feb 2024 14:19:49 GMT
RUN rm -f '/etc/yum.repos.d/repo-3cf8a.repo' '/etc/yum.repos.d/repo-e6c6f.repo'
# Thu, 29 Feb 2024 14:19:50 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Thu, 29 Feb 2024 14:19:51 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Wed, 24 Jan 2024 16:26:40 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 24 Jan 2024 16:26:40 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Jan 2024 16:26:40 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 24 Jan 2024 16:26:40 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         fontconfig         glibc-langpack-en     ;     microdnf clean all # buildkit
# Wed, 24 Jan 2024 16:26:40 GMT
ENV JAVA_VERSION=jdk-17.0.10+7
# Wed, 24 Jan 2024 16:26:40 GMT
RUN set -eux;     ARCH="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')";     case "${ARCH}" in        aarch64|arm64)          ESUM='16080d055da0962fbd6b40f659a98a457cba3efa7ea716d5400cfebe8b935bf0';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.10_7.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='620cc0e7338f2722f3ed076ac65c0fafb575981426bac4e1970860e5e2d048f0';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jre_x64_linux_hotspot_17.0.10_7.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='4e18b60dba540b5c431ff03f74a1c73b22d83151f93b8768241d264d1a53582d';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.10_7.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='c1b2fd232fc55e814479d7585d7ec45bae952a2f4137084f1d99f958c6880a49';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jre_s390x_linux_hotspot_17.0.10_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Wed, 24 Jan 2024 16:26:40 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 24 Jan 2024 16:26:40 GMT
COPY entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 24 Jan 2024 16:26:40 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
```

-	Layers:
	-	`sha256:9ef500aca087afa9d068f2596af99aa8adb962a9735fee0ed5f51427b200e3b9`  
		Last Modified: Fri, 15 Mar 2024 10:52:04 GMT  
		Size: 36.0 MB (36004563 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d4f5203495cd3d68a5c6c43646819d0dc7afff7fd4a62070628da685f759c85`  
		Last Modified: Mon, 15 Apr 2024 20:46:08 GMT  
		Size: 28.7 MB (28669934 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21fb4b4c1c6fc9a79a16d343673b83fc3b8dc7e79bf997b7cde8dbea9434968e`  
		Last Modified: Mon, 15 Apr 2024 20:47:12 GMT  
		Size: 43.8 MB (43761412 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:edeeb895f07df223aa809b2d3dbbece8224a5916036307a904276dec6ce11201`  
		Last Modified: Mon, 15 Apr 2024 20:47:05 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50c8d8a683b9f51c82bd00ca93a962baa4272e72adce9d7fc8c4a4915df72364`  
		Last Modified: Mon, 15 Apr 2024 20:47:05 GMT  
		Size: 711.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
