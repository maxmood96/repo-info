## `eclipse-temurin:8u392-b08-jdk-ubi9-minimal`

```console
$ docker pull eclipse-temurin@sha256:7fe3fd32a069ff9741e04ee0aa690a86a691c8100634f3fbe0763b89e6294f53
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `eclipse-temurin:8u392-b08-jdk-ubi9-minimal` - linux; amd64

```console
$ docker pull eclipse-temurin@sha256:e3142ae6e2402f6bf71dc2fb739a105329ce1dfc48f502b4147bea071c891c53
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **169.2 MB (169205257 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa5da7c8265b808dfdfec0da30cc588ed764ed9a3374c11667a50ca2dd6edac3`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`

```dockerfile
# Thu, 07 Dec 2023 04:19:06 GMT
ADD file:3b29fba5e73efe9ec5cf915f4a12bcfc1233baf57b701cd7f46462ebf85c5421 in / 
# Thu, 07 Dec 2023 04:19:07 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Thu, 07 Dec 2023 04:19:07 GMT
ADD file:ecc29a1455ca1b7c82018555e16e2e802135974523df6748e431f8707e759ddd in /tmp/tls-ca-bundle.pem 
# Thu, 07 Dec 2023 04:19:08 GMT
ADD multi:8257bc82024891d335e91a6d5e44bb825bdb87abe8bc1d2ee3fcfb9e8cbecea1 in /etc/yum.repos.d/ 
# Thu, 07 Dec 2023 04:19:08 GMT
LABEL maintainer="Red Hat, Inc."
# Thu, 07 Dec 2023 04:19:08 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.3"
# Thu, 07 Dec 2023 04:19:08 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Thu, 07 Dec 2023 04:19:08 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Thu, 07 Dec 2023 04:19:08 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 07 Dec 2023 04:19:08 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Thu, 07 Dec 2023 04:19:08 GMT
LABEL io.openshift.expose-services=""
# Thu, 07 Dec 2023 04:19:08 GMT
LABEL io.openshift.tags="minimal rhel9"
# Thu, 07 Dec 2023 04:19:08 GMT
ENV container oci
# Thu, 07 Dec 2023 04:19:08 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 07 Dec 2023 04:19:08 GMT
CMD ["/bin/bash"]
# Thu, 07 Dec 2023 04:19:08 GMT
RUN rm -rf /var/log/*
# Thu, 07 Dec 2023 04:19:08 GMT
LABEL release=1475
# Thu, 07 Dec 2023 04:19:09 GMT
ADD file:2f91406cebe76f5a68d0aed7a9142410aa2ad41c096c1c117a8b580e3b56e55c in /root/buildinfo/content_manifests/ubi9-minimal-container-9.3-1475.json 
# Thu, 07 Dec 2023 04:19:09 GMT
ADD file:8af5a93a05a5b30bf94d83167bac0b48e41ee4f966d909ff7d9660196be34c4c in /root/buildinfo/Dockerfile-ubi9-minimal-9.3-1475 
# Thu, 07 Dec 2023 04:19:09 GMT
LABEL "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2023-12-07T04:10:36" "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="e8510c65a9be4b0635372fd09bee126ce7e08bc7" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi9-minimal/images/9.3-1475"
# Thu, 07 Dec 2023 04:19:10 GMT
RUN rm -f '/etc/yum.repos.d/repo-84783.repo' '/etc/yum.repos.d/repo-186d3.repo'
# Thu, 07 Dec 2023 04:19:11 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Thu, 07 Dec 2023 04:19:12 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Thu, 14 Dec 2023 01:49:31 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 14 Dec 2023 01:49:32 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 14 Dec 2023 01:49:32 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 14 Dec 2023 01:49:48 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         openssl         wget         ca-certificates         fontconfig         glibc-langpack-en     ;     microdnf clean all
# Thu, 14 Dec 2023 01:49:49 GMT
ENV JAVA_VERSION=jdk8u392-b08
# Thu, 14 Dec 2023 01:49:54 GMT
RUN set -eux;     ARCH="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')";     case "${ARCH}" in        aarch64|arm64)          ESUM='70636c2fa4927913e9e869d471607a99d3a521c1fa3f3687b889c2acba67c493';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u392-b08/OpenJDK8U-jdk_aarch64_linux_hotspot_8u392b08.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='15d091e22aa0cad12a241acff8c1634e7228b9740f8d19634250aa6fe0c19a33';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u392-b08/OpenJDK8U-jdk_x64_linux_hotspot_8u392b08.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='9d9813d2840360ffdbc449c45e71124e8170c31a3b6cce9151fbb31352064406';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u392-b08/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u392b08.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;
# Thu, 14 Dec 2023 01:49:55 GMT
RUN set -eux;     echo "Verifying install ...";     echo "javac -version"; javac -version;     echo "java -version"; java -version;     echo "Complete."
# Thu, 14 Dec 2023 01:49:55 GMT
COPY file:e097c113ce7e2c199bdbde78dd6f9b89c841d973017b0333b39720f0efa4c730 in /__cacert_entrypoint.sh 
# Thu, 14 Dec 2023 01:49:55 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
```

-	Layers:
	-	`sha256:e6e98c874e21bf68ae62db244603d751054b20b94888bfb1adb157827cd38c92`  
		Last Modified: Wed, 13 Dec 2023 17:00:23 GMT  
		Size: 37.7 MB (37721982 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a2ae6a725bd5e58600f85d2090852440f19f984fb02a57124291673e262a11b`  
		Last Modified: Thu, 14 Dec 2023 01:53:18 GMT  
		Size: 27.9 MB (27883877 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c45ccba8a1fdde9270d5463564f4d8f65465bcc4439172f97fd4acf096a5601f`  
		Last Modified: Thu, 14 Dec 2023 01:53:22 GMT  
		Size: 103.6 MB (103598528 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9d68b86439e2e02db15b14727310a0cfc3f4fb8b4a505276abb479d0cca1135`  
		Last Modified: Thu, 14 Dec 2023 01:53:14 GMT  
		Size: 159.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c10d2f35f99c12f3d304b99a338ed2f1d68617a3b7758bae028e7faaefcfcec2`  
		Last Modified: Thu, 14 Dec 2023 01:53:14 GMT  
		Size: 711.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:8u392-b08-jdk-ubi9-minimal` - linux; arm64 variant v8

```console
$ docker pull eclipse-temurin@sha256:cacf6c4a81c2986dfae8f4c1f331ff97052f8040e731b8b581d0f5d5556d3890
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **167.0 MB (167030795 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:54f721ee0de43ff4e525a65c305ef465d23c4665f6c84e36ffde39c0ce9f1ca2`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`

```dockerfile
# Thu, 07 Dec 2023 04:19:06 GMT
ADD file:7ba972e538cfd486a9ead8e6c555a813a0fdd8c971fece26107d633360ca400e in / 
# Thu, 07 Dec 2023 04:19:08 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Thu, 07 Dec 2023 04:19:08 GMT
ADD file:ecc29a1455ca1b7c82018555e16e2e802135974523df6748e431f8707e759ddd in /tmp/tls-ca-bundle.pem 
# Thu, 07 Dec 2023 04:19:08 GMT
ADD multi:8257bc82024891d335e91a6d5e44bb825bdb87abe8bc1d2ee3fcfb9e8cbecea1 in /etc/yum.repos.d/ 
# Thu, 07 Dec 2023 04:19:08 GMT
LABEL maintainer="Red Hat, Inc."
# Thu, 07 Dec 2023 04:19:08 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.3"
# Thu, 07 Dec 2023 04:19:08 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Thu, 07 Dec 2023 04:19:08 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Thu, 07 Dec 2023 04:19:08 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 07 Dec 2023 04:19:08 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Thu, 07 Dec 2023 04:19:08 GMT
LABEL io.openshift.expose-services=""
# Thu, 07 Dec 2023 04:19:08 GMT
LABEL io.openshift.tags="minimal rhel9"
# Thu, 07 Dec 2023 04:19:08 GMT
ENV container oci
# Thu, 07 Dec 2023 04:19:08 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 07 Dec 2023 04:19:08 GMT
CMD ["/bin/bash"]
# Thu, 07 Dec 2023 04:19:09 GMT
RUN rm -rf /var/log/*
# Thu, 07 Dec 2023 04:19:09 GMT
LABEL release=1475
# Thu, 07 Dec 2023 04:19:09 GMT
ADD file:81f4709f6c901cfae1353cf48b313f40bcb74c28a4a486b53e093a5b3d4a8b47 in /root/buildinfo/content_manifests/ubi9-minimal-container-9.3-1475.json 
# Thu, 07 Dec 2023 04:19:09 GMT
ADD file:1ff4ce5b17d000737bdcb251e3ecc8506100fc38c8fdd75265dcf2699f35103c in /root/buildinfo/Dockerfile-ubi9-minimal-9.3-1475 
# Thu, 07 Dec 2023 04:19:09 GMT
LABEL "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2023-12-07T04:10:36" "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="e8510c65a9be4b0635372fd09bee126ce7e08bc7" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi9-minimal/images/9.3-1475"
# Thu, 07 Dec 2023 04:19:11 GMT
RUN rm -f '/etc/yum.repos.d/repo-84783.repo' '/etc/yum.repos.d/repo-186d3.repo'
# Thu, 07 Dec 2023 04:19:12 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Thu, 07 Dec 2023 04:19:13 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Thu, 14 Dec 2023 01:51:06 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 14 Dec 2023 01:51:06 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 14 Dec 2023 01:51:06 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 14 Dec 2023 01:51:24 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         openssl         wget         ca-certificates         fontconfig         glibc-langpack-en     ;     microdnf clean all
# Thu, 14 Dec 2023 01:51:25 GMT
ENV JAVA_VERSION=jdk8u392-b08
# Thu, 14 Dec 2023 01:51:30 GMT
RUN set -eux;     ARCH="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')";     case "${ARCH}" in        aarch64|arm64)          ESUM='70636c2fa4927913e9e869d471607a99d3a521c1fa3f3687b889c2acba67c493';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u392-b08/OpenJDK8U-jdk_aarch64_linux_hotspot_8u392b08.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='15d091e22aa0cad12a241acff8c1634e7228b9740f8d19634250aa6fe0c19a33';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u392-b08/OpenJDK8U-jdk_x64_linux_hotspot_8u392b08.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='9d9813d2840360ffdbc449c45e71124e8170c31a3b6cce9151fbb31352064406';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u392-b08/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u392b08.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;
# Thu, 14 Dec 2023 01:51:32 GMT
RUN set -eux;     echo "Verifying install ...";     echo "javac -version"; javac -version;     echo "java -version"; java -version;     echo "Complete."
# Thu, 14 Dec 2023 01:51:32 GMT
COPY file:e097c113ce7e2c199bdbde78dd6f9b89c841d973017b0333b39720f0efa4c730 in /__cacert_entrypoint.sh 
# Thu, 14 Dec 2023 01:51:32 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
```

-	Layers:
	-	`sha256:f4849aa241c326e575522a63046cad5e53ec51b8e918d232021fc78d31e146fa`  
		Last Modified: Wed, 13 Dec 2023 17:00:20 GMT  
		Size: 36.0 MB (36010908 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d07d5d8f482e628787b0283e4b5bf1bb77ed91bf99882fd31d18c4a369503b37`  
		Last Modified: Thu, 14 Dec 2023 01:54:13 GMT  
		Size: 28.3 MB (28317176 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d6be3387c840365b4ab9480bec6881184dcc64b1869eee52223f52283b4b671`  
		Last Modified: Thu, 14 Dec 2023 01:54:15 GMT  
		Size: 102.7 MB (102701838 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9d7233838000aa06e699fdc6a29e7776f77ab37cca77b26fbd2de3039950f8c`  
		Last Modified: Thu, 14 Dec 2023 01:54:09 GMT  
		Size: 162.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43065437d1d2a06e57512af6a2dbffa0d5a72a5516b17c468b2729d48dcc3f1d`  
		Last Modified: Thu, 14 Dec 2023 01:54:09 GMT  
		Size: 711.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:8u392-b08-jdk-ubi9-minimal` - linux; ppc64le

```console
$ docker pull eclipse-temurin@sha256:e5ed956bc7335693ebf96f67f6b0d867a68422dc9c465f7afe7c0c98f3fb122c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **173.6 MB (173645940 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:15265a2603a9e32e8f84eeb149d9418899d19ace0e671085c17c10c2fb3f4d5b`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`

```dockerfile
# Thu, 07 Dec 2023 04:19:10 GMT
ADD file:82b0903051ac27f66d120ca59a87f8b5bfc31c8e4f19f88d41b7e189dd5f9848 in / 
# Thu, 07 Dec 2023 04:19:11 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Thu, 07 Dec 2023 04:19:11 GMT
ADD file:ecc29a1455ca1b7c82018555e16e2e802135974523df6748e431f8707e759ddd in /tmp/tls-ca-bundle.pem 
# Thu, 07 Dec 2023 04:19:11 GMT
ADD multi:8257bc82024891d335e91a6d5e44bb825bdb87abe8bc1d2ee3fcfb9e8cbecea1 in /etc/yum.repos.d/ 
# Thu, 07 Dec 2023 04:19:11 GMT
LABEL maintainer="Red Hat, Inc."
# Thu, 07 Dec 2023 04:19:11 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.3"
# Thu, 07 Dec 2023 04:19:11 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Thu, 07 Dec 2023 04:19:11 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Thu, 07 Dec 2023 04:19:11 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 07 Dec 2023 04:19:11 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Thu, 07 Dec 2023 04:19:11 GMT
LABEL io.openshift.expose-services=""
# Thu, 07 Dec 2023 04:19:11 GMT
LABEL io.openshift.tags="minimal rhel9"
# Thu, 07 Dec 2023 04:19:11 GMT
ENV container oci
# Thu, 07 Dec 2023 04:19:11 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 07 Dec 2023 04:19:11 GMT
CMD ["/bin/bash"]
# Thu, 07 Dec 2023 04:19:13 GMT
RUN rm -rf /var/log/*
# Thu, 07 Dec 2023 04:19:13 GMT
LABEL release=1475
# Thu, 07 Dec 2023 04:19:13 GMT
ADD file:d551330fb95bb45b70652e0761f50eba42eb6aa5681123b038c37fdca6bad444 in /root/buildinfo/content_manifests/ubi9-minimal-container-9.3-1475.json 
# Thu, 07 Dec 2023 04:19:13 GMT
ADD file:a493a33c479aa9eca7d6a43f9973055b7d838c41bd3ed43d03df6d30f8078ba0 in /root/buildinfo/Dockerfile-ubi9-minimal-9.3-1475 
# Thu, 07 Dec 2023 04:19:13 GMT
LABEL "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2023-12-07T04:10:36" "architecture"="ppc64le" "vcs-type"="git" "vcs-ref"="e8510c65a9be4b0635372fd09bee126ce7e08bc7" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi9-minimal/images/9.3-1475"
# Thu, 07 Dec 2023 04:19:14 GMT
RUN rm -f '/etc/yum.repos.d/repo-84783.repo' '/etc/yum.repos.d/repo-186d3.repo'
# Thu, 07 Dec 2023 04:19:16 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Thu, 07 Dec 2023 04:19:18 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Thu, 14 Dec 2023 02:22:43 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 14 Dec 2023 02:22:45 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 14 Dec 2023 02:22:45 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 14 Dec 2023 02:23:36 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         openssl         wget         ca-certificates         fontconfig         glibc-langpack-en     ;     microdnf clean all
# Thu, 14 Dec 2023 02:23:42 GMT
ENV JAVA_VERSION=jdk8u392-b08
# Thu, 14 Dec 2023 02:23:53 GMT
RUN set -eux;     ARCH="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')";     case "${ARCH}" in        aarch64|arm64)          ESUM='70636c2fa4927913e9e869d471607a99d3a521c1fa3f3687b889c2acba67c493';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u392-b08/OpenJDK8U-jdk_aarch64_linux_hotspot_8u392b08.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='15d091e22aa0cad12a241acff8c1634e7228b9740f8d19634250aa6fe0c19a33';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u392-b08/OpenJDK8U-jdk_x64_linux_hotspot_8u392b08.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='9d9813d2840360ffdbc449c45e71124e8170c31a3b6cce9151fbb31352064406';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u392-b08/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u392b08.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;
# Thu, 14 Dec 2023 02:23:57 GMT
RUN set -eux;     echo "Verifying install ...";     echo "javac -version"; javac -version;     echo "java -version"; java -version;     echo "Complete."
# Thu, 14 Dec 2023 02:23:57 GMT
COPY file:e097c113ce7e2c199bdbde78dd6f9b89c841d973017b0333b39720f0efa4c730 in /__cacert_entrypoint.sh 
# Thu, 14 Dec 2023 02:23:58 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
```

-	Layers:
	-	`sha256:c721e8705d331953b5dcba6f470f14a60df884f6177622562d6d4fed0fe02d41`  
		Last Modified: Wed, 13 Dec 2023 18:09:18 GMT  
		Size: 42.1 MB (42148257 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4cd525af4bd813e8ef5d4e2fa0475beee9b649b527b923a3a810516e15fc635`  
		Last Modified: Thu, 14 Dec 2023 02:28:15 GMT  
		Size: 30.4 MB (30432228 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4862d50795821e92c88bc5a92f02a27bc99a3fea5309fc32b90ee7311d8c2abf`  
		Last Modified: Thu, 14 Dec 2023 02:28:20 GMT  
		Size: 101.1 MB (101064584 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b7023cbf2f9110f6eacec4f952d3de5336a3c2ba6a8e80deac670677a1a3915`  
		Last Modified: Thu, 14 Dec 2023 02:28:09 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70bbff2ade6ee03f0102ebca49edf0ddf2859536d7d9aa3da7660b8d50076c14`  
		Last Modified: Thu, 14 Dec 2023 02:28:09 GMT  
		Size: 711.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
