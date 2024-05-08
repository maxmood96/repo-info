## `eclipse-temurin:21-jre-ubi9-minimal`

```console
$ docker pull eclipse-temurin@sha256:fc76243eda08755d309109148aa4b1ce3e65dffb1fdc9123ce9ec968918153b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `eclipse-temurin:21-jre-ubi9-minimal` - linux; amd64

```console
$ docker pull eclipse-temurin@sha256:ec819a3a6662b1e51953e05224d5bc8591a42cc69156de834adbb7f2eb957636
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **119.5 MB (119518688 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:478e1940060274d62891fe5ec3d68efbf1bb76fa169f711210b32b1d0a9a2c10`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`

```dockerfile
# Thu, 02 May 2024 15:39:52 GMT
ADD file:110d10a9b23c80354ffdbfe8bd85e3d5b457994a103f1abbf26b015237bd40eb in / 
# Thu, 02 May 2024 15:39:53 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Thu, 02 May 2024 15:39:53 GMT
ADD file:5b1f650e1376d79fa3a65df4a154ea5166def95154b52c1c1097dfd8fc7d58eb in /tmp/tls-ca-bundle.pem 
# Thu, 02 May 2024 15:39:53 GMT
ADD multi:bba82b2c530381d750ea64baaac8ed3e48c924899e721737bc8d6b93fa43f96d in /etc/yum.repos.d/ 
# Thu, 02 May 2024 15:39:53 GMT
LABEL maintainer="Red Hat, Inc."
# Thu, 02 May 2024 15:39:53 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.4"
# Thu, 02 May 2024 15:39:53 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Thu, 02 May 2024 15:39:53 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Thu, 02 May 2024 15:39:53 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 02 May 2024 15:39:53 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Thu, 02 May 2024 15:39:53 GMT
LABEL io.openshift.expose-services=""
# Thu, 02 May 2024 15:39:53 GMT
LABEL io.openshift.tags="minimal rhel9"
# Thu, 02 May 2024 15:39:53 GMT
ENV container oci
# Thu, 02 May 2024 15:39:53 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 02 May 2024 15:39:53 GMT
CMD ["/bin/bash"]
# Thu, 02 May 2024 15:39:54 GMT
RUN rm -rf /var/log/*
# Thu, 02 May 2024 15:39:54 GMT
ADD file:abe7837e0dc0e89a912f6b868587e0a08d39dcb102d3a3fb70a61523b02f45f7 in /root/buildinfo/content_manifests/ubi9-minimal-container-9.4-949.1714662671.json 
# Thu, 02 May 2024 15:39:54 GMT
ADD file:b3873917276c24f5d9b9de472d5ccc929d2592a1b24d043712215a667e437b4f in /root/buildinfo/Dockerfile-ubi9-minimal-9.4-949.1714662671 
# Thu, 02 May 2024 15:39:54 GMT
LABEL "release"="949.1714662671" "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2024-05-02T15:15:48" "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="4b4efbdd5a311b6a9c56319e756ca58c10a2b4de" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi9-minimal/images/9.4-949.1714662671"
# Thu, 02 May 2024 15:39:55 GMT
RUN rm -f '/etc/yum.repos.d/odcs-3029549-719f4.repo' '/etc/yum.repos.d/rhel-9.4-compose-34ae9.repo'
# Thu, 02 May 2024 15:39:55 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Thu, 02 May 2024 15:39:57 GMT
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
ENV JAVA_VERSION=jdk-21.0.3+9
# Tue, 23 Apr 2024 20:51:38 GMT
RUN set -eux;     ARCH="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')";     case "${ARCH}" in        aarch64|arm64)          ESUM='c7c31bc6f5ab4c4b6f4559e11c2fa9541ae6757ab8da6dd85c29163913bd9238';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.3%2B9/OpenJDK21U-jre_aarch64_linux_hotspot_21.0.3_9.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='f1af100c4afca2035f446967323230150cfe5872b5a664d98c86963e5c066e0d';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.3%2B9/OpenJDK21U-jre_x64_linux_hotspot_21.0.3_9.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='aa628c6accc9d075b7b0f2bff6487f8ca0b8f057af31842a85fc8b363e1e10f3';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.3%2B9/OpenJDK21U-jre_ppc64le_linux_hotspot_21.0.3_9.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='a60dbad08a1977269dec7782f90225107479bfc8d10d2894f437778ae2e2b737';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.3%2B9/OpenJDK21U-jre_s390x_linux_hotspot_21.0.3_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Tue, 23 Apr 2024 20:51:38 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 23 Apr 2024 20:51:38 GMT
COPY entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 23 Apr 2024 20:51:38 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
```

-	Layers:
	-	`sha256:2dad23f0e70929aa1350f15046f40dff7e1b3ccaa9d55389f0041f8d7ccdcb36`  
		Last Modified: Mon, 06 May 2024 14:10:03 GMT  
		Size: 38.9 MB (38886732 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75515f257f71b4a75c2235522bf865034ab2bc721042481bdcd28480c2f09f99`  
		Last Modified: Tue, 07 May 2024 22:33:03 GMT  
		Size: 27.2 MB (27164890 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c9da2719d3e1215fd3538320bb51f993fa789f8aa28c97c55c6449d9c9ea112`  
		Last Modified: Tue, 07 May 2024 22:35:36 GMT  
		Size: 53.5 MB (53466196 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:146550a80a5b706ee2cfcc3604d254580df73de37a966ff9d0b195d8c627e756`  
		Last Modified: Tue, 07 May 2024 22:35:28 GMT  
		Size: 161.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d620c0b9593788e06b27c389321b5f6dd249f2aa67bfe67b6e3ae93d593d8a9`  
		Last Modified: Tue, 07 May 2024 22:35:28 GMT  
		Size: 709.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:21-jre-ubi9-minimal` - linux; arm64 variant v8

```console
$ docker pull eclipse-temurin@sha256:29fa2feb554b26889e82fb2afe517399b62cd4eca803dd2ce1fc2b979ed16f63
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **117.3 MB (117289550 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:39f86d68f353d49e2374ac8bf5e0b32bb41d3dbcfa99cdc211e427bb26c45918`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`

```dockerfile
# Thu, 02 May 2024 15:39:54 GMT
ADD file:64ec164ec6824f7f5315c6b92aa679b834b744e93866622ed6275a74c95044df in / 
# Thu, 02 May 2024 15:39:55 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Thu, 02 May 2024 15:39:55 GMT
ADD file:5b1f650e1376d79fa3a65df4a154ea5166def95154b52c1c1097dfd8fc7d58eb in /tmp/tls-ca-bundle.pem 
# Thu, 02 May 2024 15:39:55 GMT
ADD multi:bba82b2c530381d750ea64baaac8ed3e48c924899e721737bc8d6b93fa43f96d in /etc/yum.repos.d/ 
# Thu, 02 May 2024 15:39:55 GMT
LABEL maintainer="Red Hat, Inc."
# Thu, 02 May 2024 15:39:55 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.4"
# Thu, 02 May 2024 15:39:55 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Thu, 02 May 2024 15:39:55 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Thu, 02 May 2024 15:39:55 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 02 May 2024 15:39:55 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Thu, 02 May 2024 15:39:55 GMT
LABEL io.openshift.expose-services=""
# Thu, 02 May 2024 15:39:55 GMT
LABEL io.openshift.tags="minimal rhel9"
# Thu, 02 May 2024 15:39:55 GMT
ENV container oci
# Thu, 02 May 2024 15:39:55 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 02 May 2024 15:39:55 GMT
CMD ["/bin/bash"]
# Thu, 02 May 2024 15:39:57 GMT
RUN rm -rf /var/log/*
# Thu, 02 May 2024 15:39:57 GMT
ADD file:504fa4e582282d72e34a7b86d423f73d40478fcf621b8bfb86af63ee405088ed in /root/buildinfo/content_manifests/ubi9-minimal-container-9.4-949.1714662671.json 
# Thu, 02 May 2024 15:39:57 GMT
ADD file:f8d27e45663c02bc2603f266cf0eb3b9dc8c37b04c0f1f0775bda4758d09ddfb in /root/buildinfo/Dockerfile-ubi9-minimal-9.4-949.1714662671 
# Thu, 02 May 2024 15:39:57 GMT
LABEL "release"="949.1714662671" "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2024-05-02T15:15:48" "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="4b4efbdd5a311b6a9c56319e756ca58c10a2b4de" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi9-minimal/images/9.4-949.1714662671"
# Thu, 02 May 2024 15:39:58 GMT
RUN rm -f '/etc/yum.repos.d/odcs-3029549-719f4.repo' '/etc/yum.repos.d/rhel-9.4-compose-34ae9.repo'
# Thu, 02 May 2024 15:39:59 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Thu, 02 May 2024 15:40:01 GMT
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
ENV JAVA_VERSION=jdk-21.0.3+9
# Tue, 23 Apr 2024 20:51:38 GMT
RUN set -eux;     ARCH="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')";     case "${ARCH}" in        aarch64|arm64)          ESUM='c7c31bc6f5ab4c4b6f4559e11c2fa9541ae6757ab8da6dd85c29163913bd9238';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.3%2B9/OpenJDK21U-jre_aarch64_linux_hotspot_21.0.3_9.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='f1af100c4afca2035f446967323230150cfe5872b5a664d98c86963e5c066e0d';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.3%2B9/OpenJDK21U-jre_x64_linux_hotspot_21.0.3_9.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='aa628c6accc9d075b7b0f2bff6487f8ca0b8f057af31842a85fc8b363e1e10f3';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.3%2B9/OpenJDK21U-jre_ppc64le_linux_hotspot_21.0.3_9.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='a60dbad08a1977269dec7782f90225107479bfc8d10d2894f437778ae2e2b737';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.3%2B9/OpenJDK21U-jre_s390x_linux_hotspot_21.0.3_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Tue, 23 Apr 2024 20:51:38 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 23 Apr 2024 20:51:38 GMT
COPY entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 23 Apr 2024 20:51:38 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
```

-	Layers:
	-	`sha256:e118b45596900675775a6359d1f05008d9a4a750c50eb18862ce0c097abc0326`  
		Last Modified: Mon, 06 May 2024 14:15:20 GMT  
		Size: 37.1 MB (37090800 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0857cba8853068f3acfe6d30985c6ccd3a73a1a7d844b9532b99eb89fb30122`  
		Last Modified: Tue, 07 May 2024 23:38:08 GMT  
		Size: 27.6 MB (27602887 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26f00f55848c280ac81f6390176d286b4b27a7677563905098c8eb396be3c2de`  
		Last Modified: Tue, 07 May 2024 23:40:16 GMT  
		Size: 52.6 MB (52594991 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b30a30f09ff2376575ea25fb95e18098c9b061911a70e3ab1e3f942dbdbbafc2`  
		Last Modified: Tue, 07 May 2024 23:40:09 GMT  
		Size: 161.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:478fb67e6a95acf366ed84789cb92995d7e8df8d5063ee1e4b0a7c8618151e4e`  
		Last Modified: Tue, 07 May 2024 23:40:10 GMT  
		Size: 711.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:21-jre-ubi9-minimal` - linux; ppc64le

```console
$ docker pull eclipse-temurin@sha256:8f5e008758825643d511f736506bb93857e41669614bb08b13d4987dd3f3cfe2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **126.5 MB (126454457 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a03b5932c1d7c9198c478f6d7ba0a89737d09afd1d63537ff6db1e82babf5d47`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`

```dockerfile
# Thu, 02 May 2024 15:39:57 GMT
ADD file:7d746f8141e85677c8544c9ed3e1f2949be35c7c39558f4ba5472959f1d25910 in / 
# Thu, 02 May 2024 15:39:58 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Thu, 02 May 2024 15:39:58 GMT
ADD file:5b1f650e1376d79fa3a65df4a154ea5166def95154b52c1c1097dfd8fc7d58eb in /tmp/tls-ca-bundle.pem 
# Thu, 02 May 2024 15:39:59 GMT
ADD multi:bba82b2c530381d750ea64baaac8ed3e48c924899e721737bc8d6b93fa43f96d in /etc/yum.repos.d/ 
# Thu, 02 May 2024 15:39:59 GMT
LABEL maintainer="Red Hat, Inc."
# Thu, 02 May 2024 15:39:59 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.4"
# Thu, 02 May 2024 15:39:59 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Thu, 02 May 2024 15:39:59 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Thu, 02 May 2024 15:39:59 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 02 May 2024 15:39:59 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Thu, 02 May 2024 15:39:59 GMT
LABEL io.openshift.expose-services=""
# Thu, 02 May 2024 15:39:59 GMT
LABEL io.openshift.tags="minimal rhel9"
# Thu, 02 May 2024 15:39:59 GMT
ENV container oci
# Thu, 02 May 2024 15:39:59 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 02 May 2024 15:39:59 GMT
CMD ["/bin/bash"]
# Thu, 02 May 2024 15:40:00 GMT
RUN rm -rf /var/log/*
# Thu, 02 May 2024 15:40:00 GMT
ADD file:9baae6b041681d8f893fa372cb2aeb4704667f1f0a4e5ea0ea4ae3095067fb91 in /root/buildinfo/content_manifests/ubi9-minimal-container-9.4-949.1714662671.json 
# Thu, 02 May 2024 15:40:00 GMT
ADD file:3b8c3e6f38dab645ed4d1e7d69204c8abf21bb91145320e21b8ba3d2866f17bf in /root/buildinfo/Dockerfile-ubi9-minimal-9.4-949.1714662671 
# Thu, 02 May 2024 15:40:00 GMT
LABEL "release"="949.1714662671" "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2024-05-02T15:15:48" "architecture"="ppc64le" "vcs-type"="git" "vcs-ref"="4b4efbdd5a311b6a9c56319e756ca58c10a2b4de" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi9-minimal/images/9.4-949.1714662671"
# Thu, 02 May 2024 15:40:01 GMT
RUN rm -f '/etc/yum.repos.d/odcs-3029549-719f4.repo' '/etc/yum.repos.d/rhel-9.4-compose-34ae9.repo'
# Thu, 02 May 2024 15:40:03 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Thu, 02 May 2024 15:40:06 GMT
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
ENV JAVA_VERSION=jdk-21.0.3+9
# Tue, 23 Apr 2024 20:51:38 GMT
RUN set -eux;     ARCH="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')";     case "${ARCH}" in        aarch64|arm64)          ESUM='c7c31bc6f5ab4c4b6f4559e11c2fa9541ae6757ab8da6dd85c29163913bd9238';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.3%2B9/OpenJDK21U-jre_aarch64_linux_hotspot_21.0.3_9.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='f1af100c4afca2035f446967323230150cfe5872b5a664d98c86963e5c066e0d';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.3%2B9/OpenJDK21U-jre_x64_linux_hotspot_21.0.3_9.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='aa628c6accc9d075b7b0f2bff6487f8ca0b8f057af31842a85fc8b363e1e10f3';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.3%2B9/OpenJDK21U-jre_ppc64le_linux_hotspot_21.0.3_9.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='a60dbad08a1977269dec7782f90225107479bfc8d10d2894f437778ae2e2b737';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.3%2B9/OpenJDK21U-jre_s390x_linux_hotspot_21.0.3_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Tue, 23 Apr 2024 20:51:38 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 23 Apr 2024 20:51:38 GMT
COPY entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 23 Apr 2024 20:51:38 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
```

-	Layers:
	-	`sha256:f4736302151836a01824eee75b18783a300902ab42bd068453e9969f4501c0b9`  
		Last Modified: Mon, 06 May 2024 18:09:10 GMT  
		Size: 43.3 MB (43326085 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1478b397a2ff36a5c119139b77cc87c97180a17909aba0003aa4cbb732af645`  
		Last Modified: Tue, 07 May 2024 23:08:18 GMT  
		Size: 29.6 MB (29591710 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:866792ddba307894fcda8c374b2f4ac74c56bddae9c030bbe2d540683fc29a95`  
		Last Modified: Tue, 07 May 2024 23:10:46 GMT  
		Size: 53.5 MB (53535791 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e09834e7c49e6c2e477490a7e6c989aa0f7cc8d2730a8fb0dd74c37d8f0896e`  
		Last Modified: Tue, 07 May 2024 23:10:38 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ccc019bed614d1135712904288f8977c946638b6caceb6a3c5cdfb4a5f77c320`  
		Last Modified: Tue, 07 May 2024 23:10:38 GMT  
		Size: 711.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:21-jre-ubi9-minimal` - linux; s390x

```console
$ docker pull eclipse-temurin@sha256:4f4e78fe25b31bf198c1394f0aa0895556f17ff7a07fc1bd00f4abeffcaa5cc0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.0 MB (113954260 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:801cfc1d2d301b160a86020c0033ab50eb2a0777f1a4023b77f63ed87b7b6a22`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`

```dockerfile
# Thu, 02 May 2024 15:39:59 GMT
ADD file:bc975f437e965779b31f554b308b5230db8bc75b69df3faa5072e14a1be77794 in / 
# Thu, 02 May 2024 15:40:00 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Thu, 02 May 2024 15:40:01 GMT
ADD file:5b1f650e1376d79fa3a65df4a154ea5166def95154b52c1c1097dfd8fc7d58eb in /tmp/tls-ca-bundle.pem 
# Thu, 02 May 2024 15:40:01 GMT
ADD multi:bba82b2c530381d750ea64baaac8ed3e48c924899e721737bc8d6b93fa43f96d in /etc/yum.repos.d/ 
# Thu, 02 May 2024 15:40:01 GMT
LABEL maintainer="Red Hat, Inc."
# Thu, 02 May 2024 15:40:01 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.4"
# Thu, 02 May 2024 15:40:01 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Thu, 02 May 2024 15:40:01 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Thu, 02 May 2024 15:40:01 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 02 May 2024 15:40:01 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Thu, 02 May 2024 15:40:01 GMT
LABEL io.openshift.expose-services=""
# Thu, 02 May 2024 15:40:01 GMT
LABEL io.openshift.tags="minimal rhel9"
# Thu, 02 May 2024 15:40:01 GMT
ENV container oci
# Thu, 02 May 2024 15:40:01 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 02 May 2024 15:40:01 GMT
CMD ["/bin/bash"]
# Thu, 02 May 2024 15:40:02 GMT
RUN rm -rf /var/log/*
# Thu, 02 May 2024 15:40:03 GMT
ADD file:3da459f4620e3767a9cf5fe57dbd18460dae303babd2334817c62af3621836d4 in /root/buildinfo/content_manifests/ubi9-minimal-container-9.4-949.1714662671.json 
# Thu, 02 May 2024 15:40:04 GMT
ADD file:56859532df86046f45297e45c776c540aeb57c663972f75d157d244e3eeb5c02 in /root/buildinfo/Dockerfile-ubi9-minimal-9.4-949.1714662671 
# Thu, 02 May 2024 15:40:04 GMT
LABEL "release"="949.1714662671" "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2024-05-02T15:15:48" "architecture"="s390x" "vcs-type"="git" "vcs-ref"="4b4efbdd5a311b6a9c56319e756ca58c10a2b4de" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi9-minimal/images/9.4-949.1714662671"
# Thu, 02 May 2024 15:40:05 GMT
RUN rm -f '/etc/yum.repos.d/odcs-3029549-719f4.repo' '/etc/yum.repos.d/rhel-9.4-compose-34ae9.repo'
# Thu, 02 May 2024 15:40:06 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Thu, 02 May 2024 15:40:07 GMT
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
ENV JAVA_VERSION=jdk-21.0.3+9
# Tue, 23 Apr 2024 20:51:38 GMT
RUN set -eux;     ARCH="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')";     case "${ARCH}" in        aarch64|arm64)          ESUM='c7c31bc6f5ab4c4b6f4559e11c2fa9541ae6757ab8da6dd85c29163913bd9238';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.3%2B9/OpenJDK21U-jre_aarch64_linux_hotspot_21.0.3_9.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='f1af100c4afca2035f446967323230150cfe5872b5a664d98c86963e5c066e0d';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.3%2B9/OpenJDK21U-jre_x64_linux_hotspot_21.0.3_9.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='aa628c6accc9d075b7b0f2bff6487f8ca0b8f057af31842a85fc8b363e1e10f3';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.3%2B9/OpenJDK21U-jre_ppc64le_linux_hotspot_21.0.3_9.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='a60dbad08a1977269dec7782f90225107479bfc8d10d2894f437778ae2e2b737';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.3%2B9/OpenJDK21U-jre_s390x_linux_hotspot_21.0.3_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Tue, 23 Apr 2024 20:51:38 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 23 Apr 2024 20:51:38 GMT
COPY entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 23 Apr 2024 20:51:38 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
```

-	Layers:
	-	`sha256:bdc04348c2a649ed7a5a685056e12e086dc90de6891d008fd7ce5ac5db66b407`  
		Last Modified: Mon, 06 May 2024 18:09:15 GMT  
		Size: 37.1 MB (37131250 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b595c3cd232f943d6f1ba78daff9db7955b9240daf115d6d44e94d929f0aa6b3`  
		Last Modified: Tue, 07 May 2024 23:33:34 GMT  
		Size: 27.2 MB (27197725 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c724ee102935864d0c4b702219891d842d91f026acc94f5fc603ca33efae7ed`  
		Last Modified: Tue, 07 May 2024 23:35:11 GMT  
		Size: 49.6 MB (49624412 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68b53db025aba082be86651b5d3c779a5fc1c41532c0881dfa80246bfee28433`  
		Last Modified: Tue, 07 May 2024 23:35:03 GMT  
		Size: 162.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a05d1592d1bdd1c8b21c1ef7c22380b40005dbc2338ed6264653e01105a943dc`  
		Last Modified: Tue, 07 May 2024 23:35:03 GMT  
		Size: 711.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
