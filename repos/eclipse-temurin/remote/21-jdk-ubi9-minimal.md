## `eclipse-temurin:21-jdk-ubi9-minimal`

```console
$ docker pull eclipse-temurin@sha256:71e3cad7b42565557dfdc1594849242e2c12aeae93f1c59c55c0ac9536e63a9a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `eclipse-temurin:21-jdk-ubi9-minimal` - linux; amd64

```console
$ docker pull eclipse-temurin@sha256:8ac0c6014bd17811b0ca603252b563b572f21158838bb8d09eba7d2e943b505a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **225.4 MB (225431591 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8099bbf412ffefe5e247f4a64468753a78ae10a1d8249ee7f53046ebe2bd2d93`
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
# Thu, 22 Aug 2024 07:58:33 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 22 Aug 2024 07:58:33 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 22 Aug 2024 07:58:33 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 22 Aug 2024 07:58:33 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         fontconfig         glibc-langpack-en     ;     microdnf clean all # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
ENV JAVA_VERSION=jdk-21.0.4+7
# Thu, 22 Aug 2024 07:58:33 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='d768eecddd7a515711659e02caef8516b7b7177fa34880a56398fd9822593a79';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.4%2B7/OpenJDK21U-jdk_aarch64_linux_hotspot_21.0.4_7.tar.gz';          ;;        ppc64le)          ESUM='c208cd0fb90560644a90f928667d2f53bfe408c957a5e36206585ad874427761';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.4%2B7/OpenJDK21U-jdk_ppc64le_linux_hotspot_21.0.4_7.tar.gz';          ;;        s390x)          ESUM='c900c8d64fab1e53274974fa4a4c736a5a3754485a5c56f4947281480773658a';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.4%2B7/OpenJDK21U-jdk_s390x_linux_hotspot_21.0.4_7.tar.gz';          ;;        x86_64)          ESUM='51fb4d03a4429c39d397d3a03a779077159317616550e4e71624c9843083e7b9';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.4%2B7/OpenJDK21U-jdk_x64_linux_hotspot_21.0.4_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 22 Aug 2024 07:58:33 GMT
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
	-	`sha256:24e217906c198b63baaaad734e2acfb740df5a71b3d38b54710c0b9d2246e689`  
		Last Modified: Wed, 11 Sep 2024 00:56:01 GMT  
		Size: 158.6 MB (158582841 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:561d8a06afdb4c6d5074ccd85600dbc0856aa1b5741141421e704be4f882c325`  
		Last Modified: Wed, 11 Sep 2024 00:55:49 GMT  
		Size: 145.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2fa4c423afee685b088eed6fe9615148c3f57e15ebf3c5ae9652e8a33367001a`  
		Last Modified: Wed, 11 Sep 2024 00:55:49 GMT  
		Size: 2.1 KB (2115 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:21-jdk-ubi9-minimal` - linux; arm64 variant v8

```console
$ docker pull eclipse-temurin@sha256:3f66dbbe40f08df921cc7b06473a2bfb1bafbb6abdba9d21ed6e7d5d1bedd174
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **222.3 MB (222331580 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c85426be8d23e87be9b33a4834372c5555916b3af2e34021a623e559909aaf01`
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
# Thu, 22 Aug 2024 07:58:33 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 22 Aug 2024 07:58:33 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 22 Aug 2024 07:58:33 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 22 Aug 2024 07:58:33 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         fontconfig         glibc-langpack-en     ;     microdnf clean all # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
ENV JAVA_VERSION=jdk-21.0.4+7
# Thu, 22 Aug 2024 07:58:33 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='d768eecddd7a515711659e02caef8516b7b7177fa34880a56398fd9822593a79';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.4%2B7/OpenJDK21U-jdk_aarch64_linux_hotspot_21.0.4_7.tar.gz';          ;;        ppc64le)          ESUM='c208cd0fb90560644a90f928667d2f53bfe408c957a5e36206585ad874427761';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.4%2B7/OpenJDK21U-jdk_ppc64le_linux_hotspot_21.0.4_7.tar.gz';          ;;        s390x)          ESUM='c900c8d64fab1e53274974fa4a4c736a5a3754485a5c56f4947281480773658a';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.4%2B7/OpenJDK21U-jdk_s390x_linux_hotspot_21.0.4_7.tar.gz';          ;;        x86_64)          ESUM='51fb4d03a4429c39d397d3a03a779077159317616550e4e71624c9843083e7b9';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.4%2B7/OpenJDK21U-jdk_x64_linux_hotspot_21.0.4_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 22 Aug 2024 07:58:33 GMT
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
	-	`sha256:fbe1ab9bf9c40d9d10f7a9e02b6c7885e5c0217f6ff3203f5da6108a720449ed`  
		Last Modified: Wed, 11 Sep 2024 00:52:14 GMT  
		Size: 156.8 MB (156752890 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:933af237048fadc5d8df6817184a5e6d12e2811ab9d053693ce2b3df95c04629`  
		Last Modified: Wed, 11 Sep 2024 00:52:03 GMT  
		Size: 145.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cbb440b86ef002f3aa61535bff721f96e4b04546d4ae56ef1f15480a5c77ec33`  
		Last Modified: Wed, 11 Sep 2024 00:52:03 GMT  
		Size: 2.1 KB (2114 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:21-jdk-ubi9-minimal` - linux; ppc64le

```console
$ docker pull eclipse-temurin@sha256:c44b8a1ee212ba3f4c0e5ec3270269fcdaf41d9b583e5ca41280b7ca28098bbd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.7 MB (232704692 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c4678751c1932411b6a6f54559114aabcda4624f2dddc3f6f8ecef8dc698d33e`
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
# Thu, 22 Aug 2024 07:58:33 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 22 Aug 2024 07:58:33 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 22 Aug 2024 07:58:33 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 22 Aug 2024 07:58:33 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         fontconfig         glibc-langpack-en     ;     microdnf clean all # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
ENV JAVA_VERSION=jdk-21.0.4+7
# Thu, 22 Aug 2024 07:58:33 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='d768eecddd7a515711659e02caef8516b7b7177fa34880a56398fd9822593a79';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.4%2B7/OpenJDK21U-jdk_aarch64_linux_hotspot_21.0.4_7.tar.gz';          ;;        ppc64le)          ESUM='c208cd0fb90560644a90f928667d2f53bfe408c957a5e36206585ad874427761';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.4%2B7/OpenJDK21U-jdk_ppc64le_linux_hotspot_21.0.4_7.tar.gz';          ;;        s390x)          ESUM='c900c8d64fab1e53274974fa4a4c736a5a3754485a5c56f4947281480773658a';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.4%2B7/OpenJDK21U-jdk_s390x_linux_hotspot_21.0.4_7.tar.gz';          ;;        x86_64)          ESUM='51fb4d03a4429c39d397d3a03a779077159317616550e4e71624c9843083e7b9';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.4%2B7/OpenJDK21U-jdk_x64_linux_hotspot_21.0.4_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 22 Aug 2024 07:58:33 GMT
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
	-	`sha256:dbbad2a763e420c5dba242e9dcf2c75573df733c8006976c06138869a47a4d55`  
		Last Modified: Wed, 11 Sep 2024 00:28:14 GMT  
		Size: 158.8 MB (158824121 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b025fdbe676bfb254378efa0058baf9ce8933e9069d1221c264d3988093b52bd`  
		Last Modified: Wed, 11 Sep 2024 00:27:59 GMT  
		Size: 145.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf8d5ceec333cfdaaf62d12ef982f3ed9464e185a16f9a51e5579295ca9706c5`  
		Last Modified: Wed, 11 Sep 2024 00:27:59 GMT  
		Size: 2.1 KB (2114 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:21-jdk-ubi9-minimal` - linux; s390x

```console
$ docker pull eclipse-temurin@sha256:eb9b31393668886de3cf14b4ac6ce7d87429712e120b6b84c211b2bb627e49d6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **212.2 MB (212224302 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd32352906dae8620f07d5c59166c1d209e172b5dce0aeae528de463ae1d84c9`
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
# Thu, 22 Aug 2024 07:58:33 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 22 Aug 2024 07:58:33 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 22 Aug 2024 07:58:33 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 22 Aug 2024 07:58:33 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         fontconfig         glibc-langpack-en     ;     microdnf clean all # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
ENV JAVA_VERSION=jdk-21.0.4+7
# Thu, 22 Aug 2024 07:58:33 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='d768eecddd7a515711659e02caef8516b7b7177fa34880a56398fd9822593a79';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.4%2B7/OpenJDK21U-jdk_aarch64_linux_hotspot_21.0.4_7.tar.gz';          ;;        ppc64le)          ESUM='c208cd0fb90560644a90f928667d2f53bfe408c957a5e36206585ad874427761';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.4%2B7/OpenJDK21U-jdk_ppc64le_linux_hotspot_21.0.4_7.tar.gz';          ;;        s390x)          ESUM='c900c8d64fab1e53274974fa4a4c736a5a3754485a5c56f4947281480773658a';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.4%2B7/OpenJDK21U-jdk_s390x_linux_hotspot_21.0.4_7.tar.gz';          ;;        x86_64)          ESUM='51fb4d03a4429c39d397d3a03a779077159317616550e4e71624c9843083e7b9';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.4%2B7/OpenJDK21U-jdk_x64_linux_hotspot_21.0.4_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 22 Aug 2024 07:58:33 GMT
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
	-	`sha256:bbd4e6a998dc72970fc3fb3405bee4a3e7547baa3f1d064686f703fdba87deb5`  
		Last Modified: Wed, 11 Sep 2024 01:04:22 GMT  
		Size: 147.1 MB (147058295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbb018e8349418ff65a8708397897530b6614484708eba3a6a60e86a99403cf6`  
		Last Modified: Wed, 11 Sep 2024 01:04:11 GMT  
		Size: 143.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4947001a7f11334e2146e72d4326d44ccde90255bdcfd6ee5faa57a6dd0b65b`  
		Last Modified: Wed, 11 Sep 2024 01:04:11 GMT  
		Size: 2.1 KB (2115 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
