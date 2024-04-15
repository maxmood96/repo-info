## `eclipse-temurin:17-jdk-ubi9-minimal`

```console
$ docker pull eclipse-temurin@sha256:54bafe179eff3cd8d2890763a55729a5f3d66601cce81b005acd3c3dad039cd7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `eclipse-temurin:17-jdk-ubi9-minimal` - linux; amd64

```console
$ docker pull eclipse-temurin@sha256:f304487af147aefcde1b3fd155991994b7f642188606f54b9e679126d3736aca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **211.2 MB (211205610 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:93cc20778122abf173cdf527617ce624d39bf9850389a6acec04f2214db393f5`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["jshell"]`

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
ENV JAVA_VERSION=jdk-17.0.10+7
# Wed, 24 Jan 2024 16:26:40 GMT
RUN set -eux;     ARCH="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')";     case "${ARCH}" in        aarch64|arm64)          ESUM='6e4201abfb3b020c1fb899b7ac063083c271250bf081f3aa7e63d91291a90b74';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jdk_aarch64_linux_hotspot_17.0.10_7.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='a8fd07e1e97352e97e330beb20f1c6b351ba064ca7878e974c7d68b8a5c1b378';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jdk_x64_linux_hotspot_17.0.10_7.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='f5fc5c9273b722ad73241a5e84feb4eba21697a57ba718dd16cfbddda45a6a4b';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jdk_ppc64le_linux_hotspot_17.0.10_7.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='691f625edd425022500eea3b41ec6137fa078dab15632fda42de04f804079774';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jdk_s390x_linux_hotspot_17.0.10_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Wed, 24 Jan 2024 16:26:40 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 24 Jan 2024 16:26:40 GMT
COPY entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 24 Jan 2024 16:26:40 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 24 Jan 2024 16:26:40 GMT
CMD ["jshell"]
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
	-	`sha256:7d806fa367250c2b39cc308c4674ad0805b18f27bd255a2b7fda082b1f81872b`  
		Last Modified: Mon, 15 Apr 2024 18:59:40 GMT  
		Size: 144.9 MB (144896706 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3360cf06de33a8454a3226d503bfa29f505bfa4f170da0f7e99ae3ebaf9ac84`  
		Last Modified: Mon, 15 Apr 2024 18:59:28 GMT  
		Size: 177.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2bace691746250997f5268d9df51ca75187ee4147732062113f8346c02e4b63a`  
		Last Modified: Mon, 15 Apr 2024 18:59:28 GMT  
		Size: 711.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:17-jdk-ubi9-minimal` - linux; arm64 variant v8

```console
$ docker pull eclipse-temurin@sha256:8098371848b238e72992fd5b305598f1ef2e7ad6943e4c5d6a9418286f7d00c7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **208.8 MB (208760142 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:febe27b393971d3849dcbf782931ee7a3eb7816e8b373c1806705ba7be669dad`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["jshell"]`

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
ENV JAVA_VERSION=jdk-17.0.10+7
# Wed, 24 Jan 2024 16:26:40 GMT
RUN set -eux;     ARCH="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')";     case "${ARCH}" in        aarch64|arm64)          ESUM='6e4201abfb3b020c1fb899b7ac063083c271250bf081f3aa7e63d91291a90b74';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jdk_aarch64_linux_hotspot_17.0.10_7.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='a8fd07e1e97352e97e330beb20f1c6b351ba064ca7878e974c7d68b8a5c1b378';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jdk_x64_linux_hotspot_17.0.10_7.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='f5fc5c9273b722ad73241a5e84feb4eba21697a57ba718dd16cfbddda45a6a4b';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jdk_ppc64le_linux_hotspot_17.0.10_7.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='691f625edd425022500eea3b41ec6137fa078dab15632fda42de04f804079774';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jdk_s390x_linux_hotspot_17.0.10_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Wed, 24 Jan 2024 16:26:40 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 24 Jan 2024 16:26:40 GMT
COPY entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 24 Jan 2024 16:26:40 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 24 Jan 2024 16:26:40 GMT
CMD ["jshell"]
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
	-	`sha256:ae0f748a0cbf2eb354f085e3bf0e9c5e954622c3c8524d890c86c3c49a6b9911`  
		Last Modified: Mon, 15 Apr 2024 18:52:18 GMT  
		Size: 143.7 MB (143725632 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:561b57f0824744ca2179dc2505c62e755c04aa83c5d858d20f63a17ae5b8e9fb`  
		Last Modified: Mon, 15 Apr 2024 18:52:09 GMT  
		Size: 178.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6402bc4a3bfca4e7473009a471b500ba03c83776f5d1a43c5de351c2a2f80228`  
		Last Modified: Mon, 15 Apr 2024 18:52:09 GMT  
		Size: 711.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:17-jdk-ubi9-minimal` - linux; ppc64le

```console
$ docker pull eclipse-temurin@sha256:98af3adc3e0604d7710d5c9b295133d5daa58e0eb6b4002f7204b8e86c181eaf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **217.9 MB (217906751 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:74c4f665463969c2db1cd20c253b50812a5e24f9d9c09f259d77f1d56d62dfe9`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["jshell"]`

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
ENV JAVA_VERSION=jdk-17.0.10+7
# Wed, 24 Jan 2024 16:26:40 GMT
RUN set -eux;     ARCH="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')";     case "${ARCH}" in        aarch64|arm64)          ESUM='6e4201abfb3b020c1fb899b7ac063083c271250bf081f3aa7e63d91291a90b74';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jdk_aarch64_linux_hotspot_17.0.10_7.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='a8fd07e1e97352e97e330beb20f1c6b351ba064ca7878e974c7d68b8a5c1b378';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jdk_x64_linux_hotspot_17.0.10_7.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='f5fc5c9273b722ad73241a5e84feb4eba21697a57ba718dd16cfbddda45a6a4b';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jdk_ppc64le_linux_hotspot_17.0.10_7.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='691f625edd425022500eea3b41ec6137fa078dab15632fda42de04f804079774';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jdk_s390x_linux_hotspot_17.0.10_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Wed, 24 Jan 2024 16:26:40 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 24 Jan 2024 16:26:40 GMT
COPY entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 24 Jan 2024 16:26:40 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 24 Jan 2024 16:26:40 GMT
CMD ["jshell"]
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
	-	`sha256:05130f0e4b52099cde3026c13d4a3ac6647b29d3590064c28e6a80e395c9e729`  
		Last Modified: Mon, 15 Apr 2024 19:33:40 GMT  
		Size: 144.7 MB (144650356 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ba827e5a9f338c23a764b53b1ffc60da3c58f719005b8f6bce973b2e86c5b9c`  
		Last Modified: Mon, 15 Apr 2024 19:33:25 GMT  
		Size: 177.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ee50783ee682283b88a0290e789bc54749c0b8d3411e6c389c68fa7f0748efa`  
		Last Modified: Mon, 15 Apr 2024 19:33:25 GMT  
		Size: 711.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:17-jdk-ubi9-minimal` - linux; s390x

```console
$ docker pull eclipse-temurin@sha256:0f5c68a46f2a03ee5594e5a6f31c5304aad32e292de0ae0d9f34faa2ca1c5a1b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **198.9 MB (198889604 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07ec9fce6a5afb6964b74b2a747ba5e855312b30cbe539e98b15503016076ec2`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["jshell"]`

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
RUN set -eux;     ARCH="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')";     case "${ARCH}" in        aarch64|arm64)          ESUM='6e4201abfb3b020c1fb899b7ac063083c271250bf081f3aa7e63d91291a90b74';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jdk_aarch64_linux_hotspot_17.0.10_7.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='a8fd07e1e97352e97e330beb20f1c6b351ba064ca7878e974c7d68b8a5c1b378';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jdk_x64_linux_hotspot_17.0.10_7.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='f5fc5c9273b722ad73241a5e84feb4eba21697a57ba718dd16cfbddda45a6a4b';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jdk_ppc64le_linux_hotspot_17.0.10_7.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='691f625edd425022500eea3b41ec6137fa078dab15632fda42de04f804079774';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jdk_s390x_linux_hotspot_17.0.10_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Wed, 24 Jan 2024 16:26:40 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 24 Jan 2024 16:26:40 GMT
COPY entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 24 Jan 2024 16:26:40 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 24 Jan 2024 16:26:40 GMT
CMD ["jshell"]
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
	-	`sha256:d66123ef9844574ee80aec4d4bc0622103a0a215d432d29efeb67f16d965ce84`  
		Last Modified: Mon, 15 Apr 2024 20:46:55 GMT  
		Size: 134.2 MB (134214218 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52839056538bd7aebe0a1a92bc49ca5df03e3de3ef59d49bab9d88b29c0e64ef`  
		Last Modified: Mon, 15 Apr 2024 20:46:45 GMT  
		Size: 178.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:297882a164e13e39319352031db0d5b5973d829d66104a5e46ea3bdde1674433`  
		Last Modified: Mon, 15 Apr 2024 20:46:45 GMT  
		Size: 711.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
