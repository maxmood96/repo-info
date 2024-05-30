## `eclipse-temurin:22-jdk-ubi9-minimal`

```console
$ docker pull eclipse-temurin@sha256:8b5a593524f0a93082ea6ed3e0c63de68061197909e5bd310c3fcec6325c2647
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `eclipse-temurin:22-jdk-ubi9-minimal` - linux; amd64

```console
$ docker pull eclipse-temurin@sha256:dc98e98b9edb9cc32f832892ade5ae3f6c4ab2af26b2884ba8d1130d0afd6142
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **222.8 MB (222756873 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f498b43b4e2db459f4db4a3a86525dca89d7543e228cf8300e38898a97483e3`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 23 May 2024 13:57:54 GMT
ADD file:2853019fb5062d9ddbe9a00ce8d69abd9c77dc27a92d0916b1b58324b73c8025 in / 
# Thu, 23 May 2024 13:57:55 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Thu, 23 May 2024 13:57:55 GMT
ADD file:5b1f650e1376d79fa3a65df4a154ea5166def95154b52c1c1097dfd8fc7d58eb in /tmp/tls-ca-bundle.pem 
# Thu, 23 May 2024 13:57:56 GMT
ADD multi:9e111fe87abb88c147eef501698b720ace4a55fea6c2cefb58b36419afd47460 in /etc/yum.repos.d/ 
# Thu, 23 May 2024 13:57:56 GMT
LABEL maintainer="Red Hat, Inc."
# Thu, 23 May 2024 13:57:56 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.4"
# Thu, 23 May 2024 13:57:56 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Thu, 23 May 2024 13:57:56 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Thu, 23 May 2024 13:57:56 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 23 May 2024 13:57:56 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Thu, 23 May 2024 13:57:56 GMT
LABEL io.openshift.expose-services=""
# Thu, 23 May 2024 13:57:56 GMT
LABEL io.openshift.tags="minimal rhel9"
# Thu, 23 May 2024 13:57:56 GMT
ENV container oci
# Thu, 23 May 2024 13:57:56 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 23 May 2024 13:57:56 GMT
CMD ["/bin/bash"]
# Thu, 23 May 2024 13:57:56 GMT
RUN rm -rf /var/log/*
# Thu, 23 May 2024 13:57:57 GMT
ADD file:18b284325bdf076af4a7ec16bd2e0e88cf3a5867dcb1fbf78c832341428ffc7c in /root/buildinfo/content_manifests/ubi9-minimal-container-9.4-949.1716471857.json 
# Thu, 23 May 2024 13:57:57 GMT
ADD file:028809d600161529d0b52d671fd12d867bd33bbfd1a26fd35f139c8a31e26483 in /root/buildinfo/Dockerfile-ubi9-minimal-9.4-949.1716471857 
# Thu, 23 May 2024 13:57:57 GMT
LABEL "release"="949.1716471857" "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2024-05-23T13:47:36" "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="4b4efbdd5a311b6a9c56319e756ca58c10a2b4de" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi9-minimal/images/9.4-949.1716471857"
# Thu, 23 May 2024 13:57:58 GMT
RUN rm -f '/etc/yum.repos.d/odcs-3103507-55f7b.repo' '/etc/yum.repos.d/rhel-9.4-compose-34ae9.repo'
# Thu, 23 May 2024 13:57:58 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Thu, 23 May 2024 13:57:59 GMT
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
ENV JAVA_VERSION=jdk-22.0.1+8
# Tue, 23 Apr 2024 20:51:38 GMT
RUN set -eux;     ARCH="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')";     case "${ARCH}" in        aarch64|arm64)          ESUM='d8488fa1e4e8c1e318cef4c0fc3842a7f15a4cf52b27054663bb94471f54b3fa';          BINARY_URL='https://github.com/adoptium/temurin22-binaries/releases/download/jdk-22.0.1%2B8/OpenJDK22U-jdk_aarch64_linux_hotspot_22.0.1_8.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='e59c6bf801cc023a1ea78eceb5e6756277f1564cd0a421ea984efe6cb96cfcf8';          BINARY_URL='https://github.com/adoptium/temurin22-binaries/releases/download/jdk-22.0.1%2B8/OpenJDK22U-jdk_x64_linux_hotspot_22.0.1_8.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='4113606ba65044a3cbd7678e1c0d41881d24a2441c8ab8b658b4ac58da624de5';          BINARY_URL='https://github.com/adoptium/temurin22-binaries/releases/download/jdk-22.0.1%2B8/OpenJDK22U-jdk_ppc64le_linux_hotspot_22.0.1_8.tar.gz';          ;;        s390x|s390:64-bit)          ESUM="9f648abfa8ae82a1138bf069f498bc73d5ed0463b3f5d79e5d0988d28f9ffcc5";          BINARY_URL='https://github.com/adoptium/temurin22-binaries/releases/download/jdk-22.0.1.1%2B1/OpenJDK22U-jdk_s390x_linux_hotspot_22.0.1.1_1.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Tue, 23 Apr 2024 20:51:38 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 23 Apr 2024 20:51:38 GMT
COPY entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 23 Apr 2024 20:51:38 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 23 Apr 2024 20:51:38 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:570d5d7d3a6a72fe2fa36c5d2c31cde66a5b88741d1336218422745bd35cf321`  
		Last Modified: Tue, 28 May 2024 15:00:00 GMT  
		Size: 38.9 MB (38877065 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a814d11fa8b73b3ddb18de2fe02e124df88ae14f2c54be3d88e8448ea9bfe909`  
		Last Modified: Thu, 30 May 2024 00:44:04 GMT  
		Size: 27.2 MB (27159706 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9f47892a53dde06d02105789803a1e2b4adb104019ea4d17dbffe61de236716`  
		Last Modified: Thu, 30 May 2024 00:47:07 GMT  
		Size: 156.7 MB (156719213 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bff2de7f6f4e5940e48868ff7797e678610e3b0416d058cab0fa71e560a872a6`  
		Last Modified: Thu, 30 May 2024 00:46:53 GMT  
		Size: 178.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd09f276f6af41fc156fd14bb7774494f9479aa66576e47dfb3668bf62eff69f`  
		Last Modified: Thu, 30 May 2024 00:46:53 GMT  
		Size: 711.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:22-jdk-ubi9-minimal` - linux; arm64 variant v8

```console
$ docker pull eclipse-temurin@sha256:0579f1d02929798534444a8c2f40faf4878bd4cfe5853672591e4e1c096088cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **219.4 MB (219416064 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:532f8ada38208e6e64c20e12ee318761084ce72071c304550483825c6582a890`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 23 May 2024 13:57:51 GMT
ADD file:32aa20e449b3486807d09d4c296901fcc11bd3ac0350736dd920d37dabf414d7 in / 
# Thu, 23 May 2024 13:57:53 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Thu, 23 May 2024 13:57:53 GMT
ADD file:5b1f650e1376d79fa3a65df4a154ea5166def95154b52c1c1097dfd8fc7d58eb in /tmp/tls-ca-bundle.pem 
# Thu, 23 May 2024 13:57:53 GMT
ADD multi:9e111fe87abb88c147eef501698b720ace4a55fea6c2cefb58b36419afd47460 in /etc/yum.repos.d/ 
# Thu, 23 May 2024 13:57:53 GMT
LABEL maintainer="Red Hat, Inc."
# Thu, 23 May 2024 13:57:53 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.4"
# Thu, 23 May 2024 13:57:53 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Thu, 23 May 2024 13:57:53 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Thu, 23 May 2024 13:57:53 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 23 May 2024 13:57:53 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Thu, 23 May 2024 13:57:53 GMT
LABEL io.openshift.expose-services=""
# Thu, 23 May 2024 13:57:53 GMT
LABEL io.openshift.tags="minimal rhel9"
# Thu, 23 May 2024 13:57:53 GMT
ENV container oci
# Thu, 23 May 2024 13:57:53 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 23 May 2024 13:57:53 GMT
CMD ["/bin/bash"]
# Thu, 23 May 2024 13:57:54 GMT
RUN rm -rf /var/log/*
# Thu, 23 May 2024 13:57:55 GMT
ADD file:52288ae6de2702c2325e6cc064a56303f60253b9695a25411e571ba09df18eaa in /root/buildinfo/content_manifests/ubi9-minimal-container-9.4-949.1716471857.json 
# Thu, 23 May 2024 13:57:55 GMT
ADD file:7a01c517d9beace4ea2a507407c840ca8ccd93e24a89ab5d836f247a9bd2ae0a in /root/buildinfo/Dockerfile-ubi9-minimal-9.4-949.1716471857 
# Thu, 23 May 2024 13:57:55 GMT
LABEL "release"="949.1716471857" "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2024-05-23T13:47:36" "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="4b4efbdd5a311b6a9c56319e756ca58c10a2b4de" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi9-minimal/images/9.4-949.1716471857"
# Thu, 23 May 2024 13:57:56 GMT
RUN rm -f '/etc/yum.repos.d/odcs-3103507-55f7b.repo' '/etc/yum.repos.d/rhel-9.4-compose-34ae9.repo'
# Thu, 23 May 2024 13:57:58 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Thu, 23 May 2024 13:58:00 GMT
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
ENV JAVA_VERSION=jdk-22.0.1+8
# Tue, 23 Apr 2024 20:51:38 GMT
RUN set -eux;     ARCH="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')";     case "${ARCH}" in        aarch64|arm64)          ESUM='d8488fa1e4e8c1e318cef4c0fc3842a7f15a4cf52b27054663bb94471f54b3fa';          BINARY_URL='https://github.com/adoptium/temurin22-binaries/releases/download/jdk-22.0.1%2B8/OpenJDK22U-jdk_aarch64_linux_hotspot_22.0.1_8.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='e59c6bf801cc023a1ea78eceb5e6756277f1564cd0a421ea984efe6cb96cfcf8';          BINARY_URL='https://github.com/adoptium/temurin22-binaries/releases/download/jdk-22.0.1%2B8/OpenJDK22U-jdk_x64_linux_hotspot_22.0.1_8.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='4113606ba65044a3cbd7678e1c0d41881d24a2441c8ab8b658b4ac58da624de5';          BINARY_URL='https://github.com/adoptium/temurin22-binaries/releases/download/jdk-22.0.1%2B8/OpenJDK22U-jdk_ppc64le_linux_hotspot_22.0.1_8.tar.gz';          ;;        s390x|s390:64-bit)          ESUM="9f648abfa8ae82a1138bf069f498bc73d5ed0463b3f5d79e5d0988d28f9ffcc5";          BINARY_URL='https://github.com/adoptium/temurin22-binaries/releases/download/jdk-22.0.1.1%2B1/OpenJDK22U-jdk_s390x_linux_hotspot_22.0.1.1_1.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Tue, 23 Apr 2024 20:51:38 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 23 Apr 2024 20:51:38 GMT
COPY entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 23 Apr 2024 20:51:38 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 23 Apr 2024 20:51:38 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:03e931dae087208f4604cf960cff372993a4a6c742b5dd267e17106fa743d48f`  
		Last Modified: Tue, 28 May 2024 15:00:01 GMT  
		Size: 37.1 MB (37080662 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:913a6b10fe35995ec7a7e21b29cba86fdac1f07c7b79ec2b84863499bb95ef59`  
		Last Modified: Thu, 30 May 2024 00:05:20 GMT  
		Size: 27.6 MB (27588844 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4104fb749debfe94026d8f3fe555dd6fac58d6946d2fff9e7703f8bc27a1414`  
		Last Modified: Thu, 30 May 2024 00:08:07 GMT  
		Size: 154.7 MB (154745669 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2cabdea9ae1d1b51879c5139fe3380a1427b20c866ae1ff12c6025fbafb0dd3`  
		Last Modified: Thu, 30 May 2024 00:07:57 GMT  
		Size: 178.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1744b03aec2d6f9f8de712c75391a70606c602fced72d3d0f64665a275d816f9`  
		Last Modified: Thu, 30 May 2024 00:07:56 GMT  
		Size: 711.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:22-jdk-ubi9-minimal` - linux; ppc64le

```console
$ docker pull eclipse-temurin@sha256:943a55d28c31434de1710da35ed4d617f0a4038df14f17d3eccdfd9023d9367d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **229.6 MB (229598291 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:11285493840eca1e3f79ff71556747e4cf1255dacb3dfe223d8f7c5575729b6f`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 23 May 2024 13:57:55 GMT
ADD file:0a163e5cc623159d8a10c082754e05de157bdde7729978401f1dad5f9701b130 in / 
# Thu, 23 May 2024 13:57:56 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Thu, 23 May 2024 13:57:56 GMT
ADD file:5b1f650e1376d79fa3a65df4a154ea5166def95154b52c1c1097dfd8fc7d58eb in /tmp/tls-ca-bundle.pem 
# Thu, 23 May 2024 13:57:57 GMT
ADD multi:9e111fe87abb88c147eef501698b720ace4a55fea6c2cefb58b36419afd47460 in /etc/yum.repos.d/ 
# Thu, 23 May 2024 13:57:57 GMT
LABEL maintainer="Red Hat, Inc."
# Thu, 23 May 2024 13:57:57 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.4"
# Thu, 23 May 2024 13:57:57 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Thu, 23 May 2024 13:57:57 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Thu, 23 May 2024 13:57:57 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 23 May 2024 13:57:57 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Thu, 23 May 2024 13:57:57 GMT
LABEL io.openshift.expose-services=""
# Thu, 23 May 2024 13:57:57 GMT
LABEL io.openshift.tags="minimal rhel9"
# Thu, 23 May 2024 13:57:57 GMT
ENV container oci
# Thu, 23 May 2024 13:57:57 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 23 May 2024 13:57:57 GMT
CMD ["/bin/bash"]
# Thu, 23 May 2024 13:57:58 GMT
RUN rm -rf /var/log/*
# Thu, 23 May 2024 13:57:59 GMT
ADD file:59d7a0456128ae89ea16e93b99c6691a9a59afb50f5392bf4ba22029f53d05a0 in /root/buildinfo/content_manifests/ubi9-minimal-container-9.4-949.1716471857.json 
# Thu, 23 May 2024 13:57:59 GMT
ADD file:3461432594d7ff6aade7d9ba0528b0105a1836fd26566a2271f6ce5bcc2c16fd in /root/buildinfo/Dockerfile-ubi9-minimal-9.4-949.1716471857 
# Thu, 23 May 2024 13:57:59 GMT
LABEL "release"="949.1716471857" "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2024-05-23T13:47:36" "architecture"="ppc64le" "vcs-type"="git" "vcs-ref"="4b4efbdd5a311b6a9c56319e756ca58c10a2b4de" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi9-minimal/images/9.4-949.1716471857"
# Thu, 23 May 2024 13:58:00 GMT
RUN rm -f '/etc/yum.repos.d/odcs-3103507-55f7b.repo' '/etc/yum.repos.d/rhel-9.4-compose-34ae9.repo'
# Thu, 23 May 2024 13:58:02 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Thu, 23 May 2024 13:58:05 GMT
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
ENV JAVA_VERSION=jdk-22.0.1+8
# Tue, 23 Apr 2024 20:51:38 GMT
RUN set -eux;     ARCH="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')";     case "${ARCH}" in        aarch64|arm64)          ESUM='d8488fa1e4e8c1e318cef4c0fc3842a7f15a4cf52b27054663bb94471f54b3fa';          BINARY_URL='https://github.com/adoptium/temurin22-binaries/releases/download/jdk-22.0.1%2B8/OpenJDK22U-jdk_aarch64_linux_hotspot_22.0.1_8.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='e59c6bf801cc023a1ea78eceb5e6756277f1564cd0a421ea984efe6cb96cfcf8';          BINARY_URL='https://github.com/adoptium/temurin22-binaries/releases/download/jdk-22.0.1%2B8/OpenJDK22U-jdk_x64_linux_hotspot_22.0.1_8.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='4113606ba65044a3cbd7678e1c0d41881d24a2441c8ab8b658b4ac58da624de5';          BINARY_URL='https://github.com/adoptium/temurin22-binaries/releases/download/jdk-22.0.1%2B8/OpenJDK22U-jdk_ppc64le_linux_hotspot_22.0.1_8.tar.gz';          ;;        s390x|s390:64-bit)          ESUM="9f648abfa8ae82a1138bf069f498bc73d5ed0463b3f5d79e5d0988d28f9ffcc5";          BINARY_URL='https://github.com/adoptium/temurin22-binaries/releases/download/jdk-22.0.1.1%2B1/OpenJDK22U-jdk_s390x_linux_hotspot_22.0.1.1_1.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Tue, 23 Apr 2024 20:51:38 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 23 Apr 2024 20:51:38 GMT
COPY entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 23 Apr 2024 20:51:38 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 23 Apr 2024 20:51:38 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:b5a9869bf68d50132f0329a511d3472c8ce0b262cb85d0b9ba8d4fe5e504b8ed`  
		Last Modified: Wed, 29 May 2024 12:11:52 GMT  
		Size: 43.3 MB (43314906 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8559ceec7d6e14b5c99660ff925baacc663b2dcb68d14c7031b361cf8b4d147`  
		Last Modified: Thu, 30 May 2024 00:03:55 GMT  
		Size: 29.6 MB (29584110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6761e4dd49ea514e8368780101ad52c427f3a6853b62f13e85e483faa6591b5d`  
		Last Modified: Thu, 30 May 2024 00:06:57 GMT  
		Size: 156.7 MB (156698386 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:900acd1daa8a22d7d65c5df6944c1fc087b42dfc205a98ee21b0caff66d9a905`  
		Last Modified: Thu, 30 May 2024 00:06:39 GMT  
		Size: 178.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db5b34775936e1eb67b14082f9a156e389991ff5f7438b8bbf3acd58fff7c844`  
		Last Modified: Thu, 30 May 2024 00:06:39 GMT  
		Size: 711.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:22-jdk-ubi9-minimal` - linux; s390x

```console
$ docker pull eclipse-temurin@sha256:6c60243b113b0a867e6439fcbc52ef1ba9b8218ee08d054da40394be47ce21dd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **210.1 MB (210076600 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c3e0bcb18f7dffe8e2478c300cc670fd63a587d9ceafb1f45a2177afeb43af05`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 23 May 2024 13:58:06 GMT
ADD file:798b7a2209629e07af18955422fac24bc8e70bab90cc0d26a8b853277bd2644f in / 
# Thu, 23 May 2024 13:58:09 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Thu, 23 May 2024 13:58:10 GMT
ADD file:5b1f650e1376d79fa3a65df4a154ea5166def95154b52c1c1097dfd8fc7d58eb in /tmp/tls-ca-bundle.pem 
# Thu, 23 May 2024 13:58:11 GMT
ADD multi:9e111fe87abb88c147eef501698b720ace4a55fea6c2cefb58b36419afd47460 in /etc/yum.repos.d/ 
# Thu, 23 May 2024 13:58:11 GMT
LABEL maintainer="Red Hat, Inc."
# Thu, 23 May 2024 13:58:11 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.4"
# Thu, 23 May 2024 13:58:11 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Thu, 23 May 2024 13:58:11 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Thu, 23 May 2024 13:58:11 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 23 May 2024 13:58:11 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Thu, 23 May 2024 13:58:11 GMT
LABEL io.openshift.expose-services=""
# Thu, 23 May 2024 13:58:11 GMT
LABEL io.openshift.tags="minimal rhel9"
# Thu, 23 May 2024 13:58:11 GMT
ENV container oci
# Thu, 23 May 2024 13:58:11 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 23 May 2024 13:58:11 GMT
CMD ["/bin/bash"]
# Thu, 23 May 2024 13:58:14 GMT
RUN rm -rf /var/log/*
# Thu, 23 May 2024 13:58:15 GMT
ADD file:750c52518541df4f4a6417171fb56dcf4f4073f467939d0505590148498ae4b3 in /root/buildinfo/content_manifests/ubi9-minimal-container-9.4-949.1716471857.json 
# Thu, 23 May 2024 13:58:16 GMT
ADD file:87fe2066c3b36663dc4ed1d2b7f3039618e482f655f701d6035dbf482e5b57a3 in /root/buildinfo/Dockerfile-ubi9-minimal-9.4-949.1716471857 
# Thu, 23 May 2024 13:58:16 GMT
LABEL "release"="949.1716471857" "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2024-05-23T13:47:36" "architecture"="s390x" "vcs-type"="git" "vcs-ref"="4b4efbdd5a311b6a9c56319e756ca58c10a2b4de" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi9-minimal/images/9.4-949.1716471857"
# Thu, 23 May 2024 13:58:19 GMT
RUN rm -f '/etc/yum.repos.d/odcs-3103507-55f7b.repo' '/etc/yum.repos.d/rhel-9.4-compose-34ae9.repo'
# Thu, 23 May 2024 13:58:22 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Thu, 23 May 2024 13:58:24 GMT
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
ENV JAVA_VERSION=jdk-22.0.1+8
# Tue, 23 Apr 2024 20:51:38 GMT
RUN set -eux;     ARCH="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')";     case "${ARCH}" in        aarch64|arm64)          ESUM='d8488fa1e4e8c1e318cef4c0fc3842a7f15a4cf52b27054663bb94471f54b3fa';          BINARY_URL='https://github.com/adoptium/temurin22-binaries/releases/download/jdk-22.0.1%2B8/OpenJDK22U-jdk_aarch64_linux_hotspot_22.0.1_8.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='e59c6bf801cc023a1ea78eceb5e6756277f1564cd0a421ea984efe6cb96cfcf8';          BINARY_URL='https://github.com/adoptium/temurin22-binaries/releases/download/jdk-22.0.1%2B8/OpenJDK22U-jdk_x64_linux_hotspot_22.0.1_8.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='4113606ba65044a3cbd7678e1c0d41881d24a2441c8ab8b658b4ac58da624de5';          BINARY_URL='https://github.com/adoptium/temurin22-binaries/releases/download/jdk-22.0.1%2B8/OpenJDK22U-jdk_ppc64le_linux_hotspot_22.0.1_8.tar.gz';          ;;        s390x|s390:64-bit)          ESUM="9f648abfa8ae82a1138bf069f498bc73d5ed0463b3f5d79e5d0988d28f9ffcc5";          BINARY_URL='https://github.com/adoptium/temurin22-binaries/releases/download/jdk-22.0.1.1%2B1/OpenJDK22U-jdk_s390x_linux_hotspot_22.0.1.1_1.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Tue, 23 Apr 2024 20:51:38 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 23 Apr 2024 20:51:38 GMT
COPY entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 23 Apr 2024 20:51:38 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 23 Apr 2024 20:51:38 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:258e30c6f516fe7233d638e11a594714dfe8e78952d8eecf1f69907c371494df`  
		Last Modified: Wed, 29 May 2024 12:11:58 GMT  
		Size: 37.1 MB (37121987 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:780a1e38de5b0d2fac2904887eea328051410273344fb26da45c9d083279e22b`  
		Last Modified: Wed, 29 May 2024 23:38:19 GMT  
		Size: 27.2 MB (27181156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93729f6727cea7cb2ded5a91a46a1692372d42ef0a8489355a3d99beeab0ddcd`  
		Last Modified: Wed, 29 May 2024 23:40:08 GMT  
		Size: 145.8 MB (145772569 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea037a2c98f7bdb7673a2457999e6391c34edf4d285f42e4645f0f575296d549`  
		Last Modified: Wed, 29 May 2024 23:39:57 GMT  
		Size: 177.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51f36ddc4e885a401f804cb2c42c08cba7899bb48b32190b4d734cd2a82c328b`  
		Last Modified: Wed, 29 May 2024 23:39:57 GMT  
		Size: 711.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
