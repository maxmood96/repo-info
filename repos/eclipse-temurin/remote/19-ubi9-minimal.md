## `eclipse-temurin:19-ubi9-minimal`

```console
$ docker pull eclipse-temurin@sha256:2cb43b3e1c1bbd072f09199a5287d3b477988c731f8e5f753f32dddf2703b9c1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `eclipse-temurin:19-ubi9-minimal` - linux; amd64

```console
$ docker pull eclipse-temurin@sha256:f5092d347d0e89a5d57c9032e5b8d910a1f671facbcbbc4b1b94719e2d765ab3
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **268.7 MB (268713389 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e954c7369b966ca468cac703f1526b818c4735849c3ebb9235180e57d4a23d5a`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 09 Nov 2022 13:44:42 GMT
ADD file:7b3aab3c25c29047a9bd11941a3e9ccfde01adc9bbbbf15bbdd780231892edc1 in / 
# Wed, 09 Nov 2022 13:44:42 GMT
ADD file:214c1de395c24e4a86ef9a706069ef30a9e804c63f851c37c35655e16fea3ced in /tmp/tls-ca-bundle.pem 
# Wed, 09 Nov 2022 13:44:42 GMT
ADD multi:30ff6a02e0f899d3bc68d3fabc66b2b79dc0a64adc0f1b34ed26fe13df185b90 in /etc/yum.repos.d/ 
# Wed, 09 Nov 2022 13:44:42 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 09 Nov 2022 13:44:42 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.1.0"
# Wed, 09 Nov 2022 13:44:42 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 09 Nov 2022 13:44:42 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Wed, 09 Nov 2022 13:44:42 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 09 Nov 2022 13:44:42 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Wed, 09 Nov 2022 13:44:42 GMT
LABEL io.openshift.expose-services=""
# Wed, 09 Nov 2022 13:44:42 GMT
LABEL io.openshift.tags="minimal rhel9"
# Wed, 09 Nov 2022 13:44:42 GMT
ENV container oci
# Wed, 09 Nov 2022 13:44:42 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 09 Nov 2022 13:44:42 GMT
CMD ["/bin/bash"]
# Wed, 09 Nov 2022 13:44:43 GMT
RUN rm -rf /var/log/*
# Wed, 09 Nov 2022 13:44:43 GMT
LABEL release=1656
# Wed, 09 Nov 2022 13:44:44 GMT
ADD file:2ee23fa79b125669153ba526f3027c406136fcda77f38f5b972b6909b03bd62b in /root/buildinfo/content_manifests/ubi9-minimal-container-9.1.0-1656.json 
# Wed, 09 Nov 2022 13:44:44 GMT
ADD file:cba9034625dcd3d13a92da2b903766954a174dea51345b8298bf1b82d79d01be in /root/buildinfo/Dockerfile-ubi9-minimal-9.1.0-1656 
# Wed, 09 Nov 2022 13:44:44 GMT
LABEL "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2022-11-09T13:34:12" "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="befaf1f5ec7b874aef2651ee1384d51828504eb9" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi9-minimal/images/9.1.0-1656"
# Wed, 09 Nov 2022 13:44:45 GMT
RUN rm -f '/etc/yum.repos.d/repo-f4c1a.repo' '/etc/yum.repos.d/repo-33b3b.repo'
# Wed, 09 Nov 2022 13:44:47 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Thu, 17 Nov 2022 00:20:15 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 17 Nov 2022 00:20:15 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 17 Nov 2022 00:20:15 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 17 Nov 2022 00:20:24 GMT
RUN microdnf install -y binutils tzdata openssl wget ca-certificates fontconfig glibc-langpack-en gzip tar     && microdnf clean all
# Thu, 17 Nov 2022 00:22:25 GMT
ENV JAVA_VERSION=jdk-19.0.1+10
# Thu, 17 Nov 2022 00:22:43 GMT
RUN set -eux;     ARCH="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')";     case "${ARCH}" in        aarch64|arm64)          ESUM='5e8d7b3189364afd78d936bad140dbe1e7025d4b96d530ed5536d035c21afb7c';          BINARY_URL='https://github.com/adoptium/temurin19-binaries/releases/download/jdk-19.0.1%2B10/OpenJDK19U-jdk_aarch64_linux_hotspot_19.0.1_10.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='79320712bbef13825a0aa308621006f32e54f503142737fb21ff085185a61a96';          BINARY_URL='https://github.com/adoptium/temurin19-binaries/releases/download/jdk-19.0.1%2B10/OpenJDK19U-jdk_ppc64le_linux_hotspot_19.0.1_10.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='0b4168e5a98d89b0a24fb2357b3544980d8c88a639024cde18b119b27d7583ae';          BINARY_URL='https://github.com/adoptium/temurin19-binaries/releases/download/jdk-19.0.1%2B10/OpenJDK19U-jdk_s390x_linux_hotspot_19.0.1_10.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='163da7ea140210bae97c6a4590c757858ab4520a78af0e3e33129863d4087552';          BINARY_URL='https://github.com/adoptium/temurin19-binaries/releases/download/jdk-19.0.1%2B10/OpenJDK19U-jdk_x64_linux_hotspot_19.0.1_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm /tmp/openjdk.tar.gz;
# Thu, 17 Nov 2022 00:22:46 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Thu, 17 Nov 2022 00:22:46 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:370b922a565a4b8fc293d71dfab1a9b03877e7981e294fb4d032629cff2908ea`  
		Last Modified: Wed, 16 Nov 2022 03:31:29 GMT  
		Size: 37.9 MB (37924180 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a4a315172de5e471c299b202c75ad450791e6a58aafc696280fdde7bf9de66a`  
		Last Modified: Thu, 17 Nov 2022 00:25:05 GMT  
		Size: 29.7 MB (29681415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e52c52c34cde40309434bf03c165f80a679fe073af27b0d5d95b9e3749e0501`  
		Last Modified: Thu, 17 Nov 2022 00:27:35 GMT  
		Size: 201.1 MB (201107618 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37742c263024194cf6d00dfe4e12886b7ef902d10512a883ac25435b35d39b4e`  
		Last Modified: Thu, 17 Nov 2022 00:27:19 GMT  
		Size: 176.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:19-ubi9-minimal` - linux; arm64 variant v8

```console
$ docker pull eclipse-temurin@sha256:50b81c3ca130e1eba00ccedc23dbe90e09ed3996e27758b61a0a6a7654f6aa43
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **266.1 MB (266050175 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a738c4d22021748a1b95010f036ec5f3f8bfcd04ed06d12add191d9e3d738016`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 09 Nov 2022 13:44:44 GMT
ADD file:4bdffe661347b90e953f55c24556c3b4f4e5ba3f83e11ba255b6991fc4388f0d in / 
# Wed, 09 Nov 2022 13:44:44 GMT
ADD file:214c1de395c24e4a86ef9a706069ef30a9e804c63f851c37c35655e16fea3ced in /tmp/tls-ca-bundle.pem 
# Wed, 09 Nov 2022 13:44:44 GMT
ADD multi:30ff6a02e0f899d3bc68d3fabc66b2b79dc0a64adc0f1b34ed26fe13df185b90 in /etc/yum.repos.d/ 
# Wed, 09 Nov 2022 13:44:44 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 09 Nov 2022 13:44:44 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.1.0"
# Wed, 09 Nov 2022 13:44:44 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 09 Nov 2022 13:44:44 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Wed, 09 Nov 2022 13:44:44 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 09 Nov 2022 13:44:44 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Wed, 09 Nov 2022 13:44:44 GMT
LABEL io.openshift.expose-services=""
# Wed, 09 Nov 2022 13:44:44 GMT
LABEL io.openshift.tags="minimal rhel9"
# Wed, 09 Nov 2022 13:44:44 GMT
ENV container oci
# Wed, 09 Nov 2022 13:44:44 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 09 Nov 2022 13:44:44 GMT
CMD ["/bin/bash"]
# Wed, 09 Nov 2022 13:44:45 GMT
RUN rm -rf /var/log/*
# Wed, 09 Nov 2022 13:44:45 GMT
LABEL release=1656
# Wed, 09 Nov 2022 13:44:46 GMT
ADD file:92a16ecbaa8d380506f46b78ebac1017789d726f830c1562f9310d3e5dbec611 in /root/buildinfo/content_manifests/ubi9-minimal-container-9.1.0-1656.json 
# Wed, 09 Nov 2022 13:44:46 GMT
ADD file:01629bc17614a262eab3033c276469803729534b11886fd19242e772ccb80ca8 in /root/buildinfo/Dockerfile-ubi9-minimal-9.1.0-1656 
# Wed, 09 Nov 2022 13:44:46 GMT
LABEL "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2022-11-09T13:34:12" "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="befaf1f5ec7b874aef2651ee1384d51828504eb9" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi9-minimal/images/9.1.0-1656"
# Wed, 09 Nov 2022 13:44:47 GMT
RUN rm -f '/etc/yum.repos.d/repo-f4c1a.repo' '/etc/yum.repos.d/repo-33b3b.repo'
# Wed, 09 Nov 2022 13:44:49 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Wed, 16 Nov 2022 23:39:50 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 16 Nov 2022 23:39:50 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 16 Nov 2022 23:39:50 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 16 Nov 2022 23:40:00 GMT
RUN microdnf install -y binutils tzdata openssl wget ca-certificates fontconfig glibc-langpack-en gzip tar     && microdnf clean all
# Wed, 16 Nov 2022 23:41:56 GMT
ENV JAVA_VERSION=jdk-19.0.1+10
# Wed, 16 Nov 2022 23:42:10 GMT
RUN set -eux;     ARCH="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')";     case "${ARCH}" in        aarch64|arm64)          ESUM='5e8d7b3189364afd78d936bad140dbe1e7025d4b96d530ed5536d035c21afb7c';          BINARY_URL='https://github.com/adoptium/temurin19-binaries/releases/download/jdk-19.0.1%2B10/OpenJDK19U-jdk_aarch64_linux_hotspot_19.0.1_10.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='79320712bbef13825a0aa308621006f32e54f503142737fb21ff085185a61a96';          BINARY_URL='https://github.com/adoptium/temurin19-binaries/releases/download/jdk-19.0.1%2B10/OpenJDK19U-jdk_ppc64le_linux_hotspot_19.0.1_10.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='0b4168e5a98d89b0a24fb2357b3544980d8c88a639024cde18b119b27d7583ae';          BINARY_URL='https://github.com/adoptium/temurin19-binaries/releases/download/jdk-19.0.1%2B10/OpenJDK19U-jdk_s390x_linux_hotspot_19.0.1_10.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='163da7ea140210bae97c6a4590c757858ab4520a78af0e3e33129863d4087552';          BINARY_URL='https://github.com/adoptium/temurin19-binaries/releases/download/jdk-19.0.1%2B10/OpenJDK19U-jdk_x64_linux_hotspot_19.0.1_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm /tmp/openjdk.tar.gz;
# Wed, 16 Nov 2022 23:42:14 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Wed, 16 Nov 2022 23:42:14 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:017404579d24b362f0902de606e00d1778350beb20d740b3d5a93e9fce757028`  
		Last Modified: Wed, 16 Nov 2022 03:31:28 GMT  
		Size: 36.1 MB (36113178 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c9c397b088b3d30bce459b5efbcc1ca184b7cceeeca6ef7742a3d5a65d9cf86`  
		Last Modified: Wed, 16 Nov 2022 23:44:11 GMT  
		Size: 30.1 MB (30068286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a208e2b64cbe61fe821cd277ff5218048fcc26d9b974bd40279e4d50304c18f6`  
		Last Modified: Wed, 16 Nov 2022 23:46:17 GMT  
		Size: 199.9 MB (199868537 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4279fc23a245b8e638bffd2094b1ef5fb9b1a2651ae9a53ff361dc5682a031fd`  
		Last Modified: Wed, 16 Nov 2022 23:46:04 GMT  
		Size: 174.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:19-ubi9-minimal` - linux; ppc64le

```console
$ docker pull eclipse-temurin@sha256:c32cb0f6c6247dba19c59b993c1a47cc2d0fa54f0c94031a8bb429ad7b5b56ec
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **273.6 MB (273570285 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a18718f7b0be1fff292c327f5dd73d7931413a66c19ecb7d9b7e233f8fd698d`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 09 Nov 2022 13:44:29 GMT
ADD file:b7fa848956dba9d5b7e47ce28fe09611e7916334adb166f4d923d2acc3b62dfa in / 
# Wed, 09 Nov 2022 13:44:29 GMT
ADD file:214c1de395c24e4a86ef9a706069ef30a9e804c63f851c37c35655e16fea3ced in /tmp/tls-ca-bundle.pem 
# Wed, 09 Nov 2022 13:44:30 GMT
ADD multi:30ff6a02e0f899d3bc68d3fabc66b2b79dc0a64adc0f1b34ed26fe13df185b90 in /etc/yum.repos.d/ 
# Wed, 09 Nov 2022 13:44:30 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 09 Nov 2022 13:44:30 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.1.0"
# Wed, 09 Nov 2022 13:44:30 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 09 Nov 2022 13:44:30 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Wed, 09 Nov 2022 13:44:30 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 09 Nov 2022 13:44:30 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Wed, 09 Nov 2022 13:44:30 GMT
LABEL io.openshift.expose-services=""
# Wed, 09 Nov 2022 13:44:30 GMT
LABEL io.openshift.tags="minimal rhel9"
# Wed, 09 Nov 2022 13:44:30 GMT
ENV container oci
# Wed, 09 Nov 2022 13:44:30 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 09 Nov 2022 13:44:30 GMT
CMD ["/bin/bash"]
# Wed, 09 Nov 2022 13:44:32 GMT
RUN rm -rf /var/log/*
# Wed, 09 Nov 2022 13:44:32 GMT
LABEL release=1656
# Wed, 09 Nov 2022 13:44:32 GMT
ADD file:67f707548ff6615b646dd023e0a11ef26064bb17ff187cf60508cfd387c8dd94 in /root/buildinfo/content_manifests/ubi9-minimal-container-9.1.0-1656.json 
# Wed, 09 Nov 2022 13:44:33 GMT
ADD file:4ddcfe8ebb6a1157eb414014a1ed71157dfc0268903635f6ab7da5807eb88547 in /root/buildinfo/Dockerfile-ubi9-minimal-9.1.0-1656 
# Wed, 09 Nov 2022 13:44:33 GMT
LABEL "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2022-11-09T13:34:12" "architecture"="ppc64le" "vcs-type"="git" "vcs-ref"="befaf1f5ec7b874aef2651ee1384d51828504eb9" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi9-minimal/images/9.1.0-1656"
# Wed, 09 Nov 2022 13:44:34 GMT
RUN rm -f '/etc/yum.repos.d/repo-f4c1a.repo' '/etc/yum.repos.d/repo-33b3b.repo'
# Wed, 09 Nov 2022 13:44:37 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Thu, 17 Nov 2022 01:13:03 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 17 Nov 2022 01:13:03 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 17 Nov 2022 01:13:03 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 17 Nov 2022 01:13:30 GMT
RUN microdnf install -y binutils tzdata openssl wget ca-certificates fontconfig glibc-langpack-en gzip tar     && microdnf clean all
# Thu, 17 Nov 2022 01:17:35 GMT
ENV JAVA_VERSION=jdk-19.0.1+10
# Thu, 17 Nov 2022 01:17:59 GMT
RUN set -eux;     ARCH="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')";     case "${ARCH}" in        aarch64|arm64)          ESUM='5e8d7b3189364afd78d936bad140dbe1e7025d4b96d530ed5536d035c21afb7c';          BINARY_URL='https://github.com/adoptium/temurin19-binaries/releases/download/jdk-19.0.1%2B10/OpenJDK19U-jdk_aarch64_linux_hotspot_19.0.1_10.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='79320712bbef13825a0aa308621006f32e54f503142737fb21ff085185a61a96';          BINARY_URL='https://github.com/adoptium/temurin19-binaries/releases/download/jdk-19.0.1%2B10/OpenJDK19U-jdk_ppc64le_linux_hotspot_19.0.1_10.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='0b4168e5a98d89b0a24fb2357b3544980d8c88a639024cde18b119b27d7583ae';          BINARY_URL='https://github.com/adoptium/temurin19-binaries/releases/download/jdk-19.0.1%2B10/OpenJDK19U-jdk_s390x_linux_hotspot_19.0.1_10.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='163da7ea140210bae97c6a4590c757858ab4520a78af0e3e33129863d4087552';          BINARY_URL='https://github.com/adoptium/temurin19-binaries/releases/download/jdk-19.0.1%2B10/OpenJDK19U-jdk_x64_linux_hotspot_19.0.1_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm /tmp/openjdk.tar.gz;
# Thu, 17 Nov 2022 01:18:06 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Thu, 17 Nov 2022 01:18:06 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:f67e11af6c0f957f8aaf4aa1c82d719ae236aea00d1ce0b61e682e04bbf8f8f8`  
		Last Modified: Wed, 16 Nov 2022 12:27:18 GMT  
		Size: 40.8 MB (40829227 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5281831dd83348105313170c050e6e082e67c269bbc07976066171a271af40cc`  
		Last Modified: Thu, 17 Nov 2022 01:22:08 GMT  
		Size: 32.4 MB (32431799 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:604437a19257c2bbe6e70222580115178d2a3ec185912415eec383e2dbe8dd85`  
		Last Modified: Thu, 17 Nov 2022 01:25:43 GMT  
		Size: 200.3 MB (200309082 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e7e491e3154f84243db998266cf99f349a1a82717eaf8c6704f9e5ce70823572`  
		Last Modified: Thu, 17 Nov 2022 01:25:16 GMT  
		Size: 177.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:19-ubi9-minimal` - linux; s390x

```console
$ docker pull eclipse-temurin@sha256:cad2e46422eade6be583cc14815e91b91997549ec29d0ece12169d5604f4fc63
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **260.3 MB (260331296 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c07744b43cf8a913181202ad5ce31329e65b0338dffa92bdd963833131ccb8d4`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 09 Nov 2022 13:45:00 GMT
ADD file:c696a6975b26d0bc58510e6f82144dd22f1da20d6144a50ea8acfbcf6c722471 in / 
# Wed, 09 Nov 2022 13:45:01 GMT
ADD file:214c1de395c24e4a86ef9a706069ef30a9e804c63f851c37c35655e16fea3ced in /tmp/tls-ca-bundle.pem 
# Wed, 09 Nov 2022 13:45:01 GMT
ADD multi:30ff6a02e0f899d3bc68d3fabc66b2b79dc0a64adc0f1b34ed26fe13df185b90 in /etc/yum.repos.d/ 
# Wed, 09 Nov 2022 13:45:01 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 09 Nov 2022 13:45:01 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.1.0"
# Wed, 09 Nov 2022 13:45:01 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 09 Nov 2022 13:45:01 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Wed, 09 Nov 2022 13:45:01 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 09 Nov 2022 13:45:01 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Wed, 09 Nov 2022 13:45:01 GMT
LABEL io.openshift.expose-services=""
# Wed, 09 Nov 2022 13:45:01 GMT
LABEL io.openshift.tags="minimal rhel9"
# Wed, 09 Nov 2022 13:45:01 GMT
ENV container oci
# Wed, 09 Nov 2022 13:45:01 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 09 Nov 2022 13:45:01 GMT
CMD ["/bin/bash"]
# Wed, 09 Nov 2022 13:45:03 GMT
RUN rm -rf /var/log/*
# Wed, 09 Nov 2022 13:45:03 GMT
LABEL release=1656
# Wed, 09 Nov 2022 13:45:04 GMT
ADD file:d59ff54c102e6e4131f19b9acc93224b25457c4205967321323811051c1b9360 in /root/buildinfo/content_manifests/ubi9-minimal-container-9.1.0-1656.json 
# Wed, 09 Nov 2022 13:45:04 GMT
ADD file:a669e390d7b1390e068b1d844ee5b8733c2383a9853cba6cbc831aca94110042 in /root/buildinfo/Dockerfile-ubi9-minimal-9.1.0-1656 
# Wed, 09 Nov 2022 13:45:04 GMT
LABEL "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2022-11-09T13:34:12" "architecture"="s390x" "vcs-type"="git" "vcs-ref"="befaf1f5ec7b874aef2651ee1384d51828504eb9" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi9-minimal/images/9.1.0-1656"
# Wed, 09 Nov 2022 13:45:06 GMT
RUN rm -f '/etc/yum.repos.d/repo-f4c1a.repo' '/etc/yum.repos.d/repo-33b3b.repo'
# Wed, 09 Nov 2022 13:45:08 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Wed, 16 Nov 2022 23:59:19 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 16 Nov 2022 23:59:19 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 16 Nov 2022 23:59:19 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 16 Nov 2022 23:59:42 GMT
RUN microdnf install -y binutils tzdata openssl wget ca-certificates fontconfig glibc-langpack-en gzip tar     && microdnf clean all
# Thu, 17 Nov 2022 00:01:48 GMT
ENV JAVA_VERSION=jdk-19.0.1+10
# Thu, 17 Nov 2022 00:01:57 GMT
RUN set -eux;     ARCH="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')";     case "${ARCH}" in        aarch64|arm64)          ESUM='5e8d7b3189364afd78d936bad140dbe1e7025d4b96d530ed5536d035c21afb7c';          BINARY_URL='https://github.com/adoptium/temurin19-binaries/releases/download/jdk-19.0.1%2B10/OpenJDK19U-jdk_aarch64_linux_hotspot_19.0.1_10.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='79320712bbef13825a0aa308621006f32e54f503142737fb21ff085185a61a96';          BINARY_URL='https://github.com/adoptium/temurin19-binaries/releases/download/jdk-19.0.1%2B10/OpenJDK19U-jdk_ppc64le_linux_hotspot_19.0.1_10.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='0b4168e5a98d89b0a24fb2357b3544980d8c88a639024cde18b119b27d7583ae';          BINARY_URL='https://github.com/adoptium/temurin19-binaries/releases/download/jdk-19.0.1%2B10/OpenJDK19U-jdk_s390x_linux_hotspot_19.0.1_10.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='163da7ea140210bae97c6a4590c757858ab4520a78af0e3e33129863d4087552';          BINARY_URL='https://github.com/adoptium/temurin19-binaries/releases/download/jdk-19.0.1%2B10/OpenJDK19U-jdk_x64_linux_hotspot_19.0.1_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm /tmp/openjdk.tar.gz;
# Thu, 17 Nov 2022 00:02:03 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Thu, 17 Nov 2022 00:02:03 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:f1551d58b2309089dfc342db62ee900f5b92a06b0a749d6b8700e31e9fb5f0d8`  
		Last Modified: Wed, 16 Nov 2022 12:27:26 GMT  
		Size: 36.2 MB (36198583 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2fdb8f863ee656899ec04a324225fe008cc6737be0bdf34580d6e057d74cb1df`  
		Last Modified: Thu, 17 Nov 2022 00:04:36 GMT  
		Size: 35.6 MB (35623466 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a587b298c2dc1f9d9d0a144389b1b1a59f2816759c09be083a1c9296b1a22dd3`  
		Last Modified: Thu, 17 Nov 2022 00:06:11 GMT  
		Size: 188.5 MB (188509073 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b908a788194121982c03acb690caeed31390c9b170c574514e1e62e1b141e020`  
		Last Modified: Thu, 17 Nov 2022 00:05:58 GMT  
		Size: 174.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
