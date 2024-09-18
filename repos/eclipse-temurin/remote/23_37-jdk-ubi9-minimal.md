## `eclipse-temurin:23_37-jdk-ubi9-minimal`

```console
$ docker pull eclipse-temurin@sha256:6af5ee805c79837f52b1abc0ea61d10c23bdbf70820bc6ecb0c5894ea0e3d90a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `eclipse-temurin:23_37-jdk-ubi9-minimal` - linux; amd64

```console
$ docker pull eclipse-temurin@sha256:0178e0305940907d292f9fb95b07a2d6447293f1dcfc3ef1756208575dcefc2e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.1 MB (232125086 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c606b1eecbcbe5d9ca39d065380ad168d5f48a9eb3373f16508c9443aaf9f9cc`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 09 Sep 2024 02:59:59 GMT
ADD file:b37317a01d7c138350a7dd1214596c9e331f2443e4202fb62e450e297a8884ec in / 
# Mon, 09 Sep 2024 03:00:00 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Mon, 09 Sep 2024 03:00:00 GMT
ADD file:5b1f650e1376d79fa3a65df4a154ea5166def95154b52c1c1097dfd8fc7d58eb in /tmp/tls-ca-bundle.pem 
# Mon, 09 Sep 2024 03:00:00 GMT
ADD multi:91888bb231f36a25c84f05db4d13197ea848b09abe661f7b153d55f6f6af43de in /etc/yum.repos.d/ 
# Mon, 09 Sep 2024 03:00:00 GMT
LABEL maintainer="Red Hat, Inc."
# Mon, 09 Sep 2024 03:00:00 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.4"
# Mon, 09 Sep 2024 03:00:00 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Mon, 09 Sep 2024 03:00:00 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Mon, 09 Sep 2024 03:00:00 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 09 Sep 2024 03:00:00 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Mon, 09 Sep 2024 03:00:00 GMT
LABEL io.openshift.expose-services=""
# Mon, 09 Sep 2024 03:00:00 GMT
LABEL io.openshift.tags="minimal rhel9"
# Mon, 09 Sep 2024 03:00:00 GMT
ENV container oci
# Mon, 09 Sep 2024 03:00:00 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 09 Sep 2024 03:00:00 GMT
CMD ["/bin/bash"]
# Mon, 09 Sep 2024 03:00:01 GMT
RUN rm -rf /var/log/*
# Mon, 09 Sep 2024 03:00:01 GMT
ADD file:b7994b75b70a7a3dfcf6b1fce6d3be08fac202f008a87a5e9c4a46e3ba552516 in /root/buildinfo/content_manifests/ubi9-minimal-container-9.4-1227.1725849298.json 
# Mon, 09 Sep 2024 03:00:01 GMT
ADD file:42184a4eb8e0b654da33b3c8593adbf1bd40e95928a3bb35c340d1f9eb9affbd in /root/buildinfo/Dockerfile-ubi9-minimal-9.4-1227.1725849298 
# Mon, 09 Sep 2024 03:00:01 GMT
LABEL "release"="1227.1725849298" "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2024-09-09T02:35:25" "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="94baa7760359088a42ad33dc22d329a5ee2c7209" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi9-minimal/images/9.4-1227.1725849298"
# Mon, 09 Sep 2024 03:00:06 GMT
RUN rm -f '/etc/yum.repos.d/odcs-3464206-199c4.repo' '/etc/yum.repos.d/rhel-9.4-compose-34ae9.repo'
# Mon, 09 Sep 2024 03:00:12 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Mon, 09 Sep 2024 03:00:14 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Wed, 18 Sep 2024 19:12:13 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 18 Sep 2024 19:12:13 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 18 Sep 2024 19:12:13 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 18 Sep 2024 19:12:13 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         fontconfig         glibc-langpack-en     ;     microdnf clean all # buildkit
# Wed, 18 Sep 2024 19:12:13 GMT
ENV JAVA_VERSION=jdk-23+37
# Wed, 18 Sep 2024 19:12:13 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='e8043d1bd9c4f42c5cf7883aca1fc3ef6bcccf4a664f378818ac0fd4fb987b7e';          BINARY_URL='https://github.com/adoptium/temurin23-binaries/releases/download/jdk-23%2B37/OpenJDK23U-jdk_aarch64_linux_hotspot_23_37.tar.gz';          ;;        ppc64le)          ESUM='4d3b0609c783dea1f6a899bfc8c84b4000d1f48f39e2489d70050bbf2c7f7d9c';          BINARY_URL='https://github.com/adoptium/temurin23-binaries/releases/download/jdk-23%2B37/OpenJDK23U-jdk_ppc64le_linux_hotspot_23_37.tar.gz';          ;;        s390x)          ESUM='2f9cb1db72ddc91f0b90904d038bca9314bc0bafedb0efe1233469bf3c934e58';          BINARY_URL='https://github.com/adoptium/temurin23-binaries/releases/download/jdk-23%2B37/OpenJDK23U-jdk_s390x_linux_hotspot_23_37.tar.gz';          ;;        x86_64)          ESUM='630c4f3870056e7e005736ec1edc34ee63a9b45e2027582c52f53a9bf44314b8';          BINARY_URL='https://github.com/adoptium/temurin23-binaries/releases/download/jdk-23%2B37/OpenJDK23U-jdk_x64_linux_hotspot_23_37.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Wed, 18 Sep 2024 19:12:13 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 18 Sep 2024 19:12:13 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 18 Sep 2024 19:12:13 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 18 Sep 2024 19:12:13 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:0d4f239055d063750dddeb4ae84b23d0a708ce76be3167f93d2ba2ba70b50547`  
		Last Modified: Mon, 09 Sep 2024 20:38:20 GMT  
		Size: 39.1 MB (39082464 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49b328994d9bd23b172075615472354832cdadb44241996fca017f328b8c3823`  
		Last Modified: Wed, 11 Sep 2024 00:54:03 GMT  
		Size: 27.8 MB (27764026 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4434613cbece4e78c8f2ca7f9b2c54195da8fc384cf81f540d5b020c2c6061fc`  
		Last Modified: Wed, 18 Sep 2024 21:25:12 GMT  
		Size: 165.3 MB (165276337 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fce36addd9dbb0d5a1044713ffc4c272a5bb76646710698585b426f4a200f5a8`  
		Last Modified: Wed, 18 Sep 2024 21:25:00 GMT  
		Size: 145.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:331d4000920a09d18919bdd7f82889ce662daf2766423f77870fd0ca122037d1`  
		Last Modified: Wed, 18 Sep 2024 21:25:00 GMT  
		Size: 2.1 KB (2114 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:23_37-jdk-ubi9-minimal` - linux; arm64 variant v8

```console
$ docker pull eclipse-temurin@sha256:24e40a3b779afe6e106e5d2fe73353c858bf9d5bbaa6423e9c6d6e8fb8a0b636
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.8 MB (228840255 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9831b9f66729689a8caa7d3282441e1a175423494e74173805158eb48fb3dc6d`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 09 Sep 2024 02:59:59 GMT
ADD file:56f22ae3154053f9bb870d963b65d5bc807ceb1db4d62ee1e134d6b82240d225 in / 
# Mon, 09 Sep 2024 03:00:00 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Mon, 09 Sep 2024 03:00:00 GMT
ADD file:5b1f650e1376d79fa3a65df4a154ea5166def95154b52c1c1097dfd8fc7d58eb in /tmp/tls-ca-bundle.pem 
# Mon, 09 Sep 2024 03:00:00 GMT
ADD multi:91888bb231f36a25c84f05db4d13197ea848b09abe661f7b153d55f6f6af43de in /etc/yum.repos.d/ 
# Mon, 09 Sep 2024 03:00:00 GMT
LABEL maintainer="Red Hat, Inc."
# Mon, 09 Sep 2024 03:00:00 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.4"
# Mon, 09 Sep 2024 03:00:00 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Mon, 09 Sep 2024 03:00:00 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Mon, 09 Sep 2024 03:00:00 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 09 Sep 2024 03:00:00 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Mon, 09 Sep 2024 03:00:00 GMT
LABEL io.openshift.expose-services=""
# Mon, 09 Sep 2024 03:00:00 GMT
LABEL io.openshift.tags="minimal rhel9"
# Mon, 09 Sep 2024 03:00:00 GMT
ENV container oci
# Mon, 09 Sep 2024 03:00:00 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 09 Sep 2024 03:00:00 GMT
CMD ["/bin/bash"]
# Mon, 09 Sep 2024 03:00:02 GMT
RUN rm -rf /var/log/*
# Mon, 09 Sep 2024 03:00:02 GMT
ADD file:a072fef81c54a753e1604edc416ac2544eecc9191cf9e4acaf7cbf28183d7ce7 in /root/buildinfo/content_manifests/ubi9-minimal-container-9.4-1227.1725849298.json 
# Mon, 09 Sep 2024 03:00:02 GMT
ADD file:b7e28c2e39378854f86cb05f59f944d37a1f7191a4c55a40adcd823d87e2c90b in /root/buildinfo/Dockerfile-ubi9-minimal-9.4-1227.1725849298 
# Mon, 09 Sep 2024 03:00:02 GMT
LABEL "release"="1227.1725849298" "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2024-09-09T02:35:25" "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="94baa7760359088a42ad33dc22d329a5ee2c7209" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi9-minimal/images/9.4-1227.1725849298"
# Mon, 09 Sep 2024 03:00:04 GMT
RUN rm -f '/etc/yum.repos.d/odcs-3464206-199c4.repo' '/etc/yum.repos.d/rhel-9.4-compose-34ae9.repo'
# Mon, 09 Sep 2024 03:00:05 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Mon, 09 Sep 2024 03:00:07 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Wed, 18 Sep 2024 19:12:13 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 18 Sep 2024 19:12:13 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 18 Sep 2024 19:12:13 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 18 Sep 2024 19:12:13 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         fontconfig         glibc-langpack-en     ;     microdnf clean all # buildkit
# Wed, 18 Sep 2024 19:12:13 GMT
ENV JAVA_VERSION=jdk-23+37
# Wed, 18 Sep 2024 19:12:13 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='e8043d1bd9c4f42c5cf7883aca1fc3ef6bcccf4a664f378818ac0fd4fb987b7e';          BINARY_URL='https://github.com/adoptium/temurin23-binaries/releases/download/jdk-23%2B37/OpenJDK23U-jdk_aarch64_linux_hotspot_23_37.tar.gz';          ;;        ppc64le)          ESUM='4d3b0609c783dea1f6a899bfc8c84b4000d1f48f39e2489d70050bbf2c7f7d9c';          BINARY_URL='https://github.com/adoptium/temurin23-binaries/releases/download/jdk-23%2B37/OpenJDK23U-jdk_ppc64le_linux_hotspot_23_37.tar.gz';          ;;        s390x)          ESUM='2f9cb1db72ddc91f0b90904d038bca9314bc0bafedb0efe1233469bf3c934e58';          BINARY_URL='https://github.com/adoptium/temurin23-binaries/releases/download/jdk-23%2B37/OpenJDK23U-jdk_s390x_linux_hotspot_23_37.tar.gz';          ;;        x86_64)          ESUM='630c4f3870056e7e005736ec1edc34ee63a9b45e2027582c52f53a9bf44314b8';          BINARY_URL='https://github.com/adoptium/temurin23-binaries/releases/download/jdk-23%2B37/OpenJDK23U-jdk_x64_linux_hotspot_23_37.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Wed, 18 Sep 2024 19:12:13 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 18 Sep 2024 19:12:13 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 18 Sep 2024 19:12:13 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 18 Sep 2024 19:12:13 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:abd9eccbef61279a9e1f196b399e5d6336f30519eb5063b2b0fa30be9e4e845d`  
		Last Modified: Tue, 10 Sep 2024 14:48:49 GMT  
		Size: 37.3 MB (37337162 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4383f3f4ab0221848aacb530c0ed4524f6705b84fcb60132c748d9bf10764d55`  
		Last Modified: Wed, 11 Sep 2024 00:50:26 GMT  
		Size: 28.2 MB (28239269 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb58ef4a49045a0ef70f4e78fd358d4a8154d47e0608d8e732d14ef438758da2`  
		Last Modified: Wed, 18 Sep 2024 21:43:42 GMT  
		Size: 163.3 MB (163261563 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80cbbe58de09d24cabb707852dc2916fc8edd7e4a73fdf3f820de0fce3633204`  
		Last Modified: Wed, 18 Sep 2024 21:43:32 GMT  
		Size: 146.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a0ceb4e4c41bb9dddf9d655ccd0893e871534acc9a6529ab7201ed219b1a3cd`  
		Last Modified: Wed, 18 Sep 2024 21:43:32 GMT  
		Size: 2.1 KB (2115 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:23_37-jdk-ubi9-minimal` - linux; ppc64le

```console
$ docker pull eclipse-temurin@sha256:661ce13e87684f255a56f5a1a45ffce7ca87933f2ee6babb903678d2a024fc46
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **239.0 MB (239038660 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:443a5316cf378ae0d8b824e6b8e469ed05ba73a3f2608796cfb366d11960a932`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 09 Sep 2024 03:00:09 GMT
ADD file:53f505eeabbc2654e5516e5aae0ecaf62fce16a6f00ef5bda096d4bdb7176df3 in / 
# Mon, 09 Sep 2024 03:00:11 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Mon, 09 Sep 2024 03:00:11 GMT
ADD file:5b1f650e1376d79fa3a65df4a154ea5166def95154b52c1c1097dfd8fc7d58eb in /tmp/tls-ca-bundle.pem 
# Mon, 09 Sep 2024 03:00:12 GMT
ADD multi:91888bb231f36a25c84f05db4d13197ea848b09abe661f7b153d55f6f6af43de in /etc/yum.repos.d/ 
# Mon, 09 Sep 2024 03:00:12 GMT
LABEL maintainer="Red Hat, Inc."
# Mon, 09 Sep 2024 03:00:12 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.4"
# Mon, 09 Sep 2024 03:00:12 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Mon, 09 Sep 2024 03:00:12 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Mon, 09 Sep 2024 03:00:12 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 09 Sep 2024 03:00:12 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Mon, 09 Sep 2024 03:00:12 GMT
LABEL io.openshift.expose-services=""
# Mon, 09 Sep 2024 03:00:12 GMT
LABEL io.openshift.tags="minimal rhel9"
# Mon, 09 Sep 2024 03:00:12 GMT
ENV container oci
# Mon, 09 Sep 2024 03:00:12 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 09 Sep 2024 03:00:12 GMT
CMD ["/bin/bash"]
# Mon, 09 Sep 2024 03:00:14 GMT
RUN rm -rf /var/log/*
# Mon, 09 Sep 2024 03:00:14 GMT
ADD file:176c74ab7f462b30313432d52b7c6f58fe2edd170551781a42448723c65e7f5f in /root/buildinfo/content_manifests/ubi9-minimal-container-9.4-1227.1725849298.json 
# Mon, 09 Sep 2024 03:00:14 GMT
ADD file:6891f0d7036caee7d12991bdd35d9026311e2ed866921adfe8f47a7aea2c4bd3 in /root/buildinfo/Dockerfile-ubi9-minimal-9.4-1227.1725849298 
# Mon, 09 Sep 2024 03:00:14 GMT
LABEL "release"="1227.1725849298" "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2024-09-09T02:35:25" "architecture"="ppc64le" "vcs-type"="git" "vcs-ref"="94baa7760359088a42ad33dc22d329a5ee2c7209" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi9-minimal/images/9.4-1227.1725849298"
# Mon, 09 Sep 2024 03:00:16 GMT
RUN rm -f '/etc/yum.repos.d/odcs-3464206-199c4.repo' '/etc/yum.repos.d/rhel-9.4-compose-34ae9.repo'
# Mon, 09 Sep 2024 03:00:17 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Mon, 09 Sep 2024 03:00:19 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Wed, 18 Sep 2024 19:12:13 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 18 Sep 2024 19:12:13 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 18 Sep 2024 19:12:13 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 18 Sep 2024 19:12:13 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         fontconfig         glibc-langpack-en     ;     microdnf clean all # buildkit
# Wed, 18 Sep 2024 19:12:13 GMT
ENV JAVA_VERSION=jdk-23+37
# Wed, 18 Sep 2024 19:12:13 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='e8043d1bd9c4f42c5cf7883aca1fc3ef6bcccf4a664f378818ac0fd4fb987b7e';          BINARY_URL='https://github.com/adoptium/temurin23-binaries/releases/download/jdk-23%2B37/OpenJDK23U-jdk_aarch64_linux_hotspot_23_37.tar.gz';          ;;        ppc64le)          ESUM='4d3b0609c783dea1f6a899bfc8c84b4000d1f48f39e2489d70050bbf2c7f7d9c';          BINARY_URL='https://github.com/adoptium/temurin23-binaries/releases/download/jdk-23%2B37/OpenJDK23U-jdk_ppc64le_linux_hotspot_23_37.tar.gz';          ;;        s390x)          ESUM='2f9cb1db72ddc91f0b90904d038bca9314bc0bafedb0efe1233469bf3c934e58';          BINARY_URL='https://github.com/adoptium/temurin23-binaries/releases/download/jdk-23%2B37/OpenJDK23U-jdk_s390x_linux_hotspot_23_37.tar.gz';          ;;        x86_64)          ESUM='630c4f3870056e7e005736ec1edc34ee63a9b45e2027582c52f53a9bf44314b8';          BINARY_URL='https://github.com/adoptium/temurin23-binaries/releases/download/jdk-23%2B37/OpenJDK23U-jdk_x64_linux_hotspot_23_37.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Wed, 18 Sep 2024 19:12:13 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 18 Sep 2024 19:12:13 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 18 Sep 2024 19:12:13 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 18 Sep 2024 19:12:13 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:cd32d68ae8ad7b6fc852a3e507326fa79010c8e32d67f10b8ff3a556c8295726`  
		Last Modified: Tue, 10 Sep 2024 18:11:59 GMT  
		Size: 43.6 MB (43616552 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1f4590d8c9bbb50bc8088444f7f7e7079f5addeb0a5cef252098fea8c7b01d8`  
		Last Modified: Wed, 11 Sep 2024 00:26:02 GMT  
		Size: 30.3 MB (30261760 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8dcedf860b73dd8c8e6a89c113ec0b7c24f98226d090fd34104557694f2a4c0`  
		Last Modified: Wed, 18 Sep 2024 21:21:54 GMT  
		Size: 165.2 MB (165158089 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e51a6cac88064c6cd363f004198cb0da2988f79f9b2dfd4e4dabfe8bf8b315c8`  
		Last Modified: Wed, 18 Sep 2024 21:21:39 GMT  
		Size: 145.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e694a67891ab39c32a3bf7537a466f8a46a23420da0939e4c545e9dca5e8feb`  
		Last Modified: Wed, 18 Sep 2024 21:21:39 GMT  
		Size: 2.1 KB (2114 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:23_37-jdk-ubi9-minimal` - linux; s390x

```console
$ docker pull eclipse-temurin@sha256:3169f3b58af8671ffc246fa0346e60df5bd0afb82caeb188211d70f6581f6ca5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **219.5 MB (219536464 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f13ecf27de9ef956ee5992da924ff4e4f050f39985e56d197c09c736616659a4`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 09 Sep 2024 03:00:03 GMT
ADD file:8d40c10f9f027f5f474f167499faeef6e3d6559f6ddc2ca95a8987fa9c0aaed9 in / 
# Mon, 09 Sep 2024 03:00:06 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Mon, 09 Sep 2024 03:00:06 GMT
ADD file:5b1f650e1376d79fa3a65df4a154ea5166def95154b52c1c1097dfd8fc7d58eb in /tmp/tls-ca-bundle.pem 
# Mon, 09 Sep 2024 03:00:07 GMT
ADD multi:91888bb231f36a25c84f05db4d13197ea848b09abe661f7b153d55f6f6af43de in /etc/yum.repos.d/ 
# Mon, 09 Sep 2024 03:00:07 GMT
LABEL maintainer="Red Hat, Inc."
# Mon, 09 Sep 2024 03:00:07 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.4"
# Mon, 09 Sep 2024 03:00:07 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Mon, 09 Sep 2024 03:00:07 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Mon, 09 Sep 2024 03:00:07 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 09 Sep 2024 03:00:07 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Mon, 09 Sep 2024 03:00:07 GMT
LABEL io.openshift.expose-services=""
# Mon, 09 Sep 2024 03:00:07 GMT
LABEL io.openshift.tags="minimal rhel9"
# Mon, 09 Sep 2024 03:00:07 GMT
ENV container oci
# Mon, 09 Sep 2024 03:00:07 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 09 Sep 2024 03:00:07 GMT
CMD ["/bin/bash"]
# Mon, 09 Sep 2024 03:00:08 GMT
RUN rm -rf /var/log/*
# Mon, 09 Sep 2024 03:00:08 GMT
ADD file:538df4a720878d2d8af3716831813f400c0017437b26768453d9943abfd1cc3e in /root/buildinfo/content_manifests/ubi9-minimal-container-9.4-1227.1725849298.json 
# Mon, 09 Sep 2024 03:00:08 GMT
ADD file:8aa8329cf2c2ef5c7579d955360b975dcec438ae1b3291b1267d91dafc715966 in /root/buildinfo/Dockerfile-ubi9-minimal-9.4-1227.1725849298 
# Mon, 09 Sep 2024 03:00:08 GMT
LABEL "release"="1227.1725849298" "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2024-09-09T02:35:25" "architecture"="s390x" "vcs-type"="git" "vcs-ref"="94baa7760359088a42ad33dc22d329a5ee2c7209" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi9-minimal/images/9.4-1227.1725849298"
# Mon, 09 Sep 2024 03:00:09 GMT
RUN rm -f '/etc/yum.repos.d/odcs-3464206-199c4.repo' '/etc/yum.repos.d/rhel-9.4-compose-34ae9.repo'
# Mon, 09 Sep 2024 03:00:11 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Mon, 09 Sep 2024 03:00:12 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Wed, 18 Sep 2024 19:12:13 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 18 Sep 2024 19:12:13 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 18 Sep 2024 19:12:13 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 18 Sep 2024 19:12:13 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         fontconfig         glibc-langpack-en     ;     microdnf clean all # buildkit
# Wed, 18 Sep 2024 19:12:13 GMT
ENV JAVA_VERSION=jdk-23+37
# Wed, 18 Sep 2024 19:12:13 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='e8043d1bd9c4f42c5cf7883aca1fc3ef6bcccf4a664f378818ac0fd4fb987b7e';          BINARY_URL='https://github.com/adoptium/temurin23-binaries/releases/download/jdk-23%2B37/OpenJDK23U-jdk_aarch64_linux_hotspot_23_37.tar.gz';          ;;        ppc64le)          ESUM='4d3b0609c783dea1f6a899bfc8c84b4000d1f48f39e2489d70050bbf2c7f7d9c';          BINARY_URL='https://github.com/adoptium/temurin23-binaries/releases/download/jdk-23%2B37/OpenJDK23U-jdk_ppc64le_linux_hotspot_23_37.tar.gz';          ;;        s390x)          ESUM='2f9cb1db72ddc91f0b90904d038bca9314bc0bafedb0efe1233469bf3c934e58';          BINARY_URL='https://github.com/adoptium/temurin23-binaries/releases/download/jdk-23%2B37/OpenJDK23U-jdk_s390x_linux_hotspot_23_37.tar.gz';          ;;        x86_64)          ESUM='630c4f3870056e7e005736ec1edc34ee63a9b45e2027582c52f53a9bf44314b8';          BINARY_URL='https://github.com/adoptium/temurin23-binaries/releases/download/jdk-23%2B37/OpenJDK23U-jdk_x64_linux_hotspot_23_37.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Wed, 18 Sep 2024 19:12:13 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 18 Sep 2024 19:12:13 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 18 Sep 2024 19:12:13 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 18 Sep 2024 19:12:13 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:d5267c99eb044e958a4c01af00d35530b55934f8976717b26fca5beda78facfa`  
		Last Modified: Tue, 10 Sep 2024 18:12:04 GMT  
		Size: 37.4 MB (37365527 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57c74c5ce69a21b534518d260e68380bb5dcae359b4bada2aa9d4cc602fcaaef`  
		Last Modified: Wed, 11 Sep 2024 01:03:12 GMT  
		Size: 27.8 MB (27798222 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7274d81d7ed228796392e0cfe2918a30935de4e8333252b2b32a7d71d570aea6`  
		Last Modified: Wed, 18 Sep 2024 21:48:08 GMT  
		Size: 154.4 MB (154370454 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5892ccf71c81591555dc370a1ae072595977f97dec5dbab388d27c49bf92c1f9`  
		Last Modified: Wed, 18 Sep 2024 21:47:56 GMT  
		Size: 147.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:048b010c37e5437085dcaac41cba331819cd5b251cadb4d4d4e2038338b8d826`  
		Last Modified: Wed, 18 Sep 2024 21:47:56 GMT  
		Size: 2.1 KB (2114 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
