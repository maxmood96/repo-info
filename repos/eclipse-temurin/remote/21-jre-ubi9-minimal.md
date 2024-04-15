## `eclipse-temurin:21-jre-ubi9-minimal`

```console
$ docker pull eclipse-temurin@sha256:019fc3c0b61b23482ef424bb50a48a8e2ee4524b5d31bd7b102716b2e7527b95
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `eclipse-temurin:21-jre-ubi9-minimal` - linux; amd64

```console
$ docker pull eclipse-temurin@sha256:c9c7a937878c94a03e51b266f2b0dfa70a8f8af63264fc625f3ecf5bb3886207
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **120.3 MB (120293812 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e12ab2e3ce64e184d77517bc190c546a0fefe0cfdee86a0d5a20d7d6c81631ef`
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
# Wed, 24 Jan 2024 16:26:40 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 24 Jan 2024 16:26:40 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Jan 2024 16:26:40 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 24 Jan 2024 16:26:40 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         fontconfig         glibc-langpack-en     ;     microdnf clean all # buildkit
# Wed, 24 Jan 2024 16:26:40 GMT
ENV JAVA_VERSION=jdk-21.0.2+13
# Wed, 24 Jan 2024 16:26:40 GMT
RUN set -eux;     ARCH="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')";     case "${ARCH}" in        aarch64|arm64)          ESUM='64c78854184c92a4da5cda571c8e357043bfaf03a03434eef58550cc3410d8a4';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.2%2B13/OpenJDK21U-jre_aarch64_linux_hotspot_21.0.2_13.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='51141204fe01a9f9dd74eab621d5eca7511eac67315c9975dbde5f2625bdca55';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.2%2B13/OpenJDK21U-jre_x64_linux_hotspot_21.0.2_13.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='caaf48e50787b80b810dc08ee91bd4ffe0d0696bd14906a92f05bf8c14aabb22';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.2%2B13/OpenJDK21U-jre_ppc64le_linux_hotspot_21.0.2_13.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='ff8191fa5b23a175932e7f4fab10a6e8df61fd71b6529c7d21451c81e82f8d55';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.2%2B13/OpenJDK21U-jre_s390x_linux_hotspot_21.0.2_13.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Wed, 24 Jan 2024 16:26:40 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 24 Jan 2024 16:26:40 GMT
COPY entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 24 Jan 2024 16:26:40 GMT
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
	-	`sha256:1de016b21b741645c98d42d9f450719dd55c1f343c895f66e9e892771f3ef1f8`  
		Last Modified: Mon, 15 Apr 2024 19:00:51 GMT  
		Size: 54.0 MB (53984925 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:821e926825b0a9ff062aabe7ed79df21a8edaee853c1ab3a00cf5d11cf129494`  
		Last Modified: Mon, 15 Apr 2024 19:00:43 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a7f6a1c5223bd1822022c8c01957117c1aceb166ee42deccdd17ffc986380b1`  
		Last Modified: Mon, 15 Apr 2024 19:00:43 GMT  
		Size: 711.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:21-jre-ubi9-minimal` - linux; arm64 variant v8

```console
$ docker pull eclipse-temurin@sha256:d6ac37425a623ac3d32b70a01ff86a542d3c55bbe6f6d7a0a1d515bfb26f7a3f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **118.2 MB (118169681 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:08ba92aeea80e9c594e2bf89944e41bf281322d1bf80084d5acf4edfa4366e72`
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
# Wed, 24 Jan 2024 16:26:40 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 24 Jan 2024 16:26:40 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Jan 2024 16:26:40 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 24 Jan 2024 16:26:40 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         fontconfig         glibc-langpack-en     ;     microdnf clean all # buildkit
# Wed, 24 Jan 2024 16:26:40 GMT
ENV JAVA_VERSION=jdk-21.0.2+13
# Wed, 24 Jan 2024 16:26:40 GMT
RUN set -eux;     ARCH="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')";     case "${ARCH}" in        aarch64|arm64)          ESUM='64c78854184c92a4da5cda571c8e357043bfaf03a03434eef58550cc3410d8a4';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.2%2B13/OpenJDK21U-jre_aarch64_linux_hotspot_21.0.2_13.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='51141204fe01a9f9dd74eab621d5eca7511eac67315c9975dbde5f2625bdca55';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.2%2B13/OpenJDK21U-jre_x64_linux_hotspot_21.0.2_13.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='caaf48e50787b80b810dc08ee91bd4ffe0d0696bd14906a92f05bf8c14aabb22';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.2%2B13/OpenJDK21U-jre_ppc64le_linux_hotspot_21.0.2_13.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='ff8191fa5b23a175932e7f4fab10a6e8df61fd71b6529c7d21451c81e82f8d55';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.2%2B13/OpenJDK21U-jre_s390x_linux_hotspot_21.0.2_13.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Wed, 24 Jan 2024 16:26:40 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 24 Jan 2024 16:26:40 GMT
COPY entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 24 Jan 2024 16:26:40 GMT
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
	-	`sha256:868a20ea9d8771a7c54fd610249ecc541b793317d5b6cc3ee7ffcdf01415953c`  
		Last Modified: Mon, 15 Apr 2024 18:53:17 GMT  
		Size: 53.1 MB (53135188 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe44571250816396e280932e91657042b256eeb626ad0530302a9da5a2baac76`  
		Last Modified: Mon, 15 Apr 2024 18:53:11 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bcecff573b84f895ec5b494650d760352b91e25f8131e689af3685e12bee3851`  
		Last Modified: Mon, 15 Apr 2024 18:53:11 GMT  
		Size: 712.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:21-jre-ubi9-minimal` - linux; ppc64le

```console
$ docker pull eclipse-temurin@sha256:fd1e29ab76b1868167a9c98dfd71fe3880337a1f3c5296efe8b704bad7797904
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.0 MB (127048439 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e88703a09424131a6ff7ca3bb3cae470aeb00ba4e95b16d169a9e5bcb911503`
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
# Wed, 24 Jan 2024 16:26:40 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 24 Jan 2024 16:26:40 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Jan 2024 16:26:40 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 24 Jan 2024 16:26:40 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         fontconfig         glibc-langpack-en     ;     microdnf clean all # buildkit
# Wed, 24 Jan 2024 16:26:40 GMT
ENV JAVA_VERSION=jdk-21.0.2+13
# Wed, 24 Jan 2024 16:26:40 GMT
RUN set -eux;     ARCH="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')";     case "${ARCH}" in        aarch64|arm64)          ESUM='64c78854184c92a4da5cda571c8e357043bfaf03a03434eef58550cc3410d8a4';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.2%2B13/OpenJDK21U-jre_aarch64_linux_hotspot_21.0.2_13.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='51141204fe01a9f9dd74eab621d5eca7511eac67315c9975dbde5f2625bdca55';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.2%2B13/OpenJDK21U-jre_x64_linux_hotspot_21.0.2_13.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='caaf48e50787b80b810dc08ee91bd4ffe0d0696bd14906a92f05bf8c14aabb22';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.2%2B13/OpenJDK21U-jre_ppc64le_linux_hotspot_21.0.2_13.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='ff8191fa5b23a175932e7f4fab10a6e8df61fd71b6529c7d21451c81e82f8d55';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.2%2B13/OpenJDK21U-jre_s390x_linux_hotspot_21.0.2_13.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Wed, 24 Jan 2024 16:26:40 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 24 Jan 2024 16:26:40 GMT
COPY entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 24 Jan 2024 16:26:40 GMT
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
	-	`sha256:051822aeb997e3ed11605685a831aa0075e08383915739cb1cf175fcbe6bf01f`  
		Last Modified: Mon, 15 Apr 2024 19:34:50 GMT  
		Size: 53.8 MB (53792064 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d912be7fac34076ca5afe2a1eed982ba3cb812b6d473aca792b3537de4364a8b`  
		Last Modified: Mon, 15 Apr 2024 19:34:41 GMT  
		Size: 159.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb29874ba56754ae3c3216d8b90dd7ed83f0e357a3e1b29c1257cdfca5883546`  
		Last Modified: Mon, 15 Apr 2024 19:34:41 GMT  
		Size: 709.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:21-jre-ubi9-minimal` - linux; s390x

```console
$ docker pull eclipse-temurin@sha256:a3c312d41204ec30e6ca5e41c274698f99b4f0d9776623ad00e471f43f8df103
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.5 MB (114513478 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c3cef929f806efbf4938e0822915ed3bf2fd401ed4e5421440569a60e5ce6433`
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
ENV JAVA_VERSION=jdk-21.0.2+13
# Wed, 24 Jan 2024 16:26:40 GMT
RUN set -eux;     ARCH="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')";     case "${ARCH}" in        aarch64|arm64)          ESUM='64c78854184c92a4da5cda571c8e357043bfaf03a03434eef58550cc3410d8a4';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.2%2B13/OpenJDK21U-jre_aarch64_linux_hotspot_21.0.2_13.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='51141204fe01a9f9dd74eab621d5eca7511eac67315c9975dbde5f2625bdca55';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.2%2B13/OpenJDK21U-jre_x64_linux_hotspot_21.0.2_13.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='caaf48e50787b80b810dc08ee91bd4ffe0d0696bd14906a92f05bf8c14aabb22';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.2%2B13/OpenJDK21U-jre_ppc64le_linux_hotspot_21.0.2_13.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='ff8191fa5b23a175932e7f4fab10a6e8df61fd71b6529c7d21451c81e82f8d55';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.2%2B13/OpenJDK21U-jre_s390x_linux_hotspot_21.0.2_13.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
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
	-	`sha256:0ffb3156af170868ec2fc895dafb2e8ab340a10a8dd641e01f288085ca923e7d`  
		Last Modified: Mon, 15 Apr 2024 20:47:48 GMT  
		Size: 49.8 MB (49838109 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff27f859055adc60e3b16b06ae9e527b0bc8ff0ae45ad43ced927ca047d60643`  
		Last Modified: Mon, 15 Apr 2024 20:47:41 GMT  
		Size: 161.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1055119f44c6d1e6a99784ed544f122d793d1aa0aa1bcd22a583ef9cc7861e24`  
		Last Modified: Mon, 15 Apr 2024 20:47:41 GMT  
		Size: 711.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
