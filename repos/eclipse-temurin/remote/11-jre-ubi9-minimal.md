## `eclipse-temurin:11-jre-ubi9-minimal`

```console
$ docker pull eclipse-temurin@sha256:dd05ea5598f45505a518d169fa44cc18af66715f863535459635e104dfe07e9e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `eclipse-temurin:11-jre-ubi9-minimal` - linux; amd64

```console
$ docker pull eclipse-temurin@sha256:624db8654170221540f84bb5f585d5c6d1aec085ebf9424b63ba9240c8972220
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **110.8 MB (110829962 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:06d92abf46f6b6f9e99826f274638fe3aa3565913041b29680f53d24f29da209`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`

```dockerfile
# Thu, 18 Jul 2024 16:00:41 GMT
ADD file:87021d55df71c4e3f216afb8a8fafe806663072c4406db403bba88d029cd4114 in / 
# Thu, 18 Jul 2024 16:00:41 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Thu, 18 Jul 2024 16:00:41 GMT
ADD file:5b1f650e1376d79fa3a65df4a154ea5166def95154b52c1c1097dfd8fc7d58eb in /tmp/tls-ca-bundle.pem 
# Thu, 18 Jul 2024 16:00:42 GMT
ADD multi:39cf1126311f383f05bcdcfb2be4d277a3c28e8231fe3885ec63ceb2c04249b8 in /etc/yum.repos.d/ 
# Thu, 18 Jul 2024 16:00:42 GMT
LABEL maintainer="Red Hat, Inc."
# Thu, 18 Jul 2024 16:00:42 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.4"
# Thu, 18 Jul 2024 16:00:42 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Thu, 18 Jul 2024 16:00:42 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Thu, 18 Jul 2024 16:00:42 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 18 Jul 2024 16:00:42 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Thu, 18 Jul 2024 16:00:42 GMT
LABEL io.openshift.expose-services=""
# Thu, 18 Jul 2024 16:00:42 GMT
LABEL io.openshift.tags="minimal rhel9"
# Thu, 18 Jul 2024 16:00:42 GMT
ENV container oci
# Thu, 18 Jul 2024 16:00:42 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 18 Jul 2024 16:00:42 GMT
CMD ["/bin/bash"]
# Thu, 18 Jul 2024 16:00:42 GMT
RUN rm -rf /var/log/*
# Thu, 18 Jul 2024 16:00:42 GMT
LABEL release=1194
# Thu, 18 Jul 2024 16:00:43 GMT
ADD file:5044c31992c75e94cf041ad1beda86a0b218ead5785a55734e242465ef7798db in /root/buildinfo/content_manifests/ubi9-minimal-container-9.4-1194.json 
# Thu, 18 Jul 2024 16:00:43 GMT
ADD file:97862c9bc77fad8fca444d897df1eb9d08bd77f12f61288c39c576743736d49f in /root/buildinfo/Dockerfile-ubi9-minimal-9.4-1194 
# Thu, 18 Jul 2024 16:00:43 GMT
LABEL "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2024-07-18T15:52:43" "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="94baa7760359088a42ad33dc22d329a5ee2c7209" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi9-minimal/images/9.4-1194"
# Thu, 18 Jul 2024 16:00:44 GMT
RUN rm -f '/etc/yum.repos.d/repo-05248.repo' '/etc/yum.repos.d/repo-09742.repo'
# Thu, 18 Jul 2024 16:00:44 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Thu, 18 Jul 2024 16:00:46 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Wed, 24 Jul 2024 22:19:06 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 24 Jul 2024 22:19:06 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Jul 2024 22:19:06 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 24 Jul 2024 22:19:06 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         fontconfig         glibc-langpack-en     ;     microdnf clean all # buildkit
# Wed, 24 Jul 2024 22:19:06 GMT
ENV JAVA_VERSION=jdk-11.0.24+8
# Wed, 24 Jul 2024 22:19:06 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='1fe97cdaad47d7d108f329c6e4560b46748ef7f2948a1027812ade0bbc2a3597';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.24_8.tar.gz';          ;;        ppc64le)          ESUM='8ee351314182df93fbad96139bb74b97814944d66197896e388404a1ecfa06b3';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.24_8.tar.gz';          ;;        s390x)          ESUM='5b331f093bb03126334bbbc24f05f60681baeda461d860e4e2cdb693ee54e0ed';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_s390x_linux_hotspot_11.0.24_8.tar.gz';          ;;        x86_64)          ESUM='e0c1938093da3780e4494d366a4e6b75584dde8d46a19acea6691ae11df4cda5';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_x64_linux_hotspot_11.0.24_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Wed, 24 Jul 2024 22:19:06 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 24 Jul 2024 22:19:06 GMT
COPY entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 24 Jul 2024 22:19:06 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
```

-	Layers:
	-	`sha256:247c2d03e9487628cb6754ff5385a670df160f7bba36af8fc1f2066e461dc36e`  
		Last Modified: Tue, 23 Jul 2024 23:20:51 GMT  
		Size: 38.9 MB (38868726 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1aaee12b977e4ae44bfa23329349fce502becf1c26fb7c4e164ee2229771d754`  
		Last Modified: Wed, 24 Jul 2024 22:53:43 GMT  
		Size: 27.7 MB (27742709 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b075a2816de807b281229d1099a0fc64425cc4b4bfe74be2550c849519a8258d`  
		Last Modified: Wed, 24 Jul 2024 22:54:45 GMT  
		Size: 44.2 MB (44216534 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55f4a2870a02bb8ea38db1a6a5850e35c0b5200dffcbace998c87bf78def6810`  
		Last Modified: Wed, 24 Jul 2024 22:54:40 GMT  
		Size: 127.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba9d3f345341200bad4a78e6f053e60f8bd80e615212116c51a9453f61627573`  
		Last Modified: Thu, 25 Jul 2024 17:29:18 GMT  
		Size: 1.9 KB (1866 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:11-jre-ubi9-minimal` - linux; arm64 variant v8

```console
$ docker pull eclipse-temurin@sha256:6866d7b344c69cc243808ee6e7f08d6bc3b27507173f6e039b6d96a524a0844a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.9 MB (107859632 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d6927ec3ccc852ee060fcaee697502b4148d32e32083afa727a35b6c1f95fcef`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`

```dockerfile
# Thu, 18 Jul 2024 16:00:25 GMT
ADD file:f709fba0574079e9aa46a5b75f6fc5d799887bd4f82a7be2013a2e4437ff041f in / 
# Thu, 18 Jul 2024 16:00:27 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Thu, 18 Jul 2024 16:00:27 GMT
ADD file:5b1f650e1376d79fa3a65df4a154ea5166def95154b52c1c1097dfd8fc7d58eb in /tmp/tls-ca-bundle.pem 
# Thu, 18 Jul 2024 16:00:27 GMT
ADD multi:39cf1126311f383f05bcdcfb2be4d277a3c28e8231fe3885ec63ceb2c04249b8 in /etc/yum.repos.d/ 
# Thu, 18 Jul 2024 16:00:27 GMT
LABEL maintainer="Red Hat, Inc."
# Thu, 18 Jul 2024 16:00:27 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.4"
# Thu, 18 Jul 2024 16:00:27 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Thu, 18 Jul 2024 16:00:27 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Thu, 18 Jul 2024 16:00:27 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 18 Jul 2024 16:00:27 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Thu, 18 Jul 2024 16:00:27 GMT
LABEL io.openshift.expose-services=""
# Thu, 18 Jul 2024 16:00:27 GMT
LABEL io.openshift.tags="minimal rhel9"
# Thu, 18 Jul 2024 16:00:27 GMT
ENV container oci
# Thu, 18 Jul 2024 16:00:27 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 18 Jul 2024 16:00:27 GMT
CMD ["/bin/bash"]
# Thu, 18 Jul 2024 16:00:29 GMT
RUN rm -rf /var/log/*
# Thu, 18 Jul 2024 16:00:29 GMT
LABEL release=1194
# Thu, 18 Jul 2024 16:00:29 GMT
ADD file:c9f3c26999c1ebf7b158f6d526405f4f2a7761aeaf3986c120c5ba32f61b0820 in /root/buildinfo/content_manifests/ubi9-minimal-container-9.4-1194.json 
# Thu, 18 Jul 2024 16:00:29 GMT
ADD file:ba00fa3144a82bce8698247481dc2415535fa14e5557f1639e90fdfa9c65461d in /root/buildinfo/Dockerfile-ubi9-minimal-9.4-1194 
# Thu, 18 Jul 2024 16:00:29 GMT
LABEL "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2024-07-18T15:52:43" "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="94baa7760359088a42ad33dc22d329a5ee2c7209" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi9-minimal/images/9.4-1194"
# Thu, 18 Jul 2024 16:00:30 GMT
RUN rm -f '/etc/yum.repos.d/repo-05248.repo' '/etc/yum.repos.d/repo-09742.repo'
# Thu, 18 Jul 2024 16:00:32 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Thu, 18 Jul 2024 16:00:34 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Wed, 24 Jul 2024 22:19:06 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 24 Jul 2024 22:19:06 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Jul 2024 22:19:06 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 24 Jul 2024 22:19:06 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         fontconfig         glibc-langpack-en     ;     microdnf clean all # buildkit
# Wed, 24 Jul 2024 22:19:06 GMT
ENV JAVA_VERSION=jdk-11.0.24+8
# Wed, 24 Jul 2024 22:19:06 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='1fe97cdaad47d7d108f329c6e4560b46748ef7f2948a1027812ade0bbc2a3597';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.24_8.tar.gz';          ;;        ppc64le)          ESUM='8ee351314182df93fbad96139bb74b97814944d66197896e388404a1ecfa06b3';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.24_8.tar.gz';          ;;        s390x)          ESUM='5b331f093bb03126334bbbc24f05f60681baeda461d860e4e2cdb693ee54e0ed';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_s390x_linux_hotspot_11.0.24_8.tar.gz';          ;;        x86_64)          ESUM='e0c1938093da3780e4494d366a4e6b75584dde8d46a19acea6691ae11df4cda5';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_x64_linux_hotspot_11.0.24_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Wed, 24 Jul 2024 22:19:06 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 24 Jul 2024 22:19:06 GMT
COPY entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 24 Jul 2024 22:19:06 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
```

-	Layers:
	-	`sha256:63c76be6b13c3916a86a82fe30d0c63bde321c804abe11ea9f3bae73f5832bdf`  
		Last Modified: Tue, 23 Jul 2024 23:20:54 GMT  
		Size: 37.1 MB (37072383 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36321a62a9265712a80b7f2e7c81ebc1733d378845ac21f2f64b709605ee3875`  
		Last Modified: Wed, 24 Jul 2024 22:50:04 GMT  
		Size: 28.2 MB (28214767 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3838cf4f0dd108474f75b3660e7aa9085c9e9b1480f30b05232319e2744ac9a`  
		Last Modified: Wed, 24 Jul 2024 22:50:57 GMT  
		Size: 42.6 MB (42570487 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e80c34c381d86ea197615af04680b9653fdf5c7b096db0d1857e03f61da3d896`  
		Last Modified: Wed, 24 Jul 2024 22:50:52 GMT  
		Size: 128.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eaa040fd3331b61b68038aae0d6db98dc1e972f239d7e9ce585a1bef210a04a7`  
		Last Modified: Thu, 25 Jul 2024 17:45:35 GMT  
		Size: 1.9 KB (1867 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:11-jre-ubi9-minimal` - linux; ppc64le

```console
$ docker pull eclipse-temurin@sha256:eb36794045eb02b809ff8985e33246cba9a6d10d221bed7d8a3dcc96edcad1c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **113.2 MB (113248565 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:44d3cdc0640d654a650a1f2b6d92a28560a5e39925c424521b3737bc60b695f3`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`

```dockerfile
# Thu, 18 Jul 2024 16:00:28 GMT
ADD file:506188f12e028f4115fb2ba353f364678bbb8ea8c5ec9b669f44281addfd1c23 in / 
# Thu, 18 Jul 2024 16:00:29 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Thu, 18 Jul 2024 16:00:29 GMT
ADD file:5b1f650e1376d79fa3a65df4a154ea5166def95154b52c1c1097dfd8fc7d58eb in /tmp/tls-ca-bundle.pem 
# Thu, 18 Jul 2024 16:00:29 GMT
ADD multi:39cf1126311f383f05bcdcfb2be4d277a3c28e8231fe3885ec63ceb2c04249b8 in /etc/yum.repos.d/ 
# Thu, 18 Jul 2024 16:00:29 GMT
LABEL maintainer="Red Hat, Inc."
# Thu, 18 Jul 2024 16:00:29 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.4"
# Thu, 18 Jul 2024 16:00:29 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Thu, 18 Jul 2024 16:00:29 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Thu, 18 Jul 2024 16:00:29 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 18 Jul 2024 16:00:29 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Thu, 18 Jul 2024 16:00:29 GMT
LABEL io.openshift.expose-services=""
# Thu, 18 Jul 2024 16:00:29 GMT
LABEL io.openshift.tags="minimal rhel9"
# Thu, 18 Jul 2024 16:00:29 GMT
ENV container oci
# Thu, 18 Jul 2024 16:00:29 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 18 Jul 2024 16:00:29 GMT
CMD ["/bin/bash"]
# Thu, 18 Jul 2024 16:00:30 GMT
RUN rm -rf /var/log/*
# Thu, 18 Jul 2024 16:00:30 GMT
LABEL release=1194
# Thu, 18 Jul 2024 16:00:31 GMT
ADD file:3f6d24259ae37b294276696c5e5ca3f2dcb0aad9637655ed1e08e29dbfc6190c in /root/buildinfo/content_manifests/ubi9-minimal-container-9.4-1194.json 
# Thu, 18 Jul 2024 16:00:31 GMT
ADD file:3a81328001d719dfa2946d3215c3dd6d6a01bef72303dd878a79d9b8d46b2979 in /root/buildinfo/Dockerfile-ubi9-minimal-9.4-1194 
# Thu, 18 Jul 2024 16:00:31 GMT
LABEL "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2024-07-18T15:52:43" "architecture"="ppc64le" "vcs-type"="git" "vcs-ref"="94baa7760359088a42ad33dc22d329a5ee2c7209" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi9-minimal/images/9.4-1194"
# Thu, 18 Jul 2024 16:00:32 GMT
RUN rm -f '/etc/yum.repos.d/repo-05248.repo' '/etc/yum.repos.d/repo-09742.repo'
# Thu, 18 Jul 2024 16:00:33 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Thu, 18 Jul 2024 16:00:35 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Wed, 24 Jul 2024 22:19:06 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 24 Jul 2024 22:19:06 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Jul 2024 22:19:06 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 24 Jul 2024 22:19:06 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         fontconfig         glibc-langpack-en     ;     microdnf clean all # buildkit
# Wed, 24 Jul 2024 22:19:06 GMT
ENV JAVA_VERSION=jdk-11.0.24+8
# Wed, 24 Jul 2024 22:19:06 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='1fe97cdaad47d7d108f329c6e4560b46748ef7f2948a1027812ade0bbc2a3597';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.24_8.tar.gz';          ;;        ppc64le)          ESUM='8ee351314182df93fbad96139bb74b97814944d66197896e388404a1ecfa06b3';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.24_8.tar.gz';          ;;        s390x)          ESUM='5b331f093bb03126334bbbc24f05f60681baeda461d860e4e2cdb693ee54e0ed';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_s390x_linux_hotspot_11.0.24_8.tar.gz';          ;;        x86_64)          ESUM='e0c1938093da3780e4494d366a4e6b75584dde8d46a19acea6691ae11df4cda5';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_x64_linux_hotspot_11.0.24_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Wed, 24 Jul 2024 22:19:06 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 24 Jul 2024 22:19:06 GMT
COPY entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 24 Jul 2024 22:19:06 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
```

-	Layers:
	-	`sha256:4a7d93ea5d89e1a76516910d4ef69c80d2186bf11033dd5d398ced6ab61a80eb`  
		Last Modified: Wed, 24 Jul 2024 00:09:48 GMT  
		Size: 43.3 MB (43310938 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89cb42c7d0dfc48bf0d24dfb4ec2140937def9b7df480c49635b57340944615d`  
		Last Modified: Thu, 25 Jul 2024 01:19:36 GMT  
		Size: 30.2 MB (30236532 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7077f3b0d46cd339c6d94434b3cc4cf4d7611f6505121fb71d5392583be22855`  
		Last Modified: Thu, 25 Jul 2024 01:20:31 GMT  
		Size: 39.7 MB (39699105 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18dd687762d99335a10e389591b65c02a4fbca614a4c5675b7bf8e6d3f8a6a7f`  
		Last Modified: Thu, 25 Jul 2024 01:20:25 GMT  
		Size: 127.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:322561c1dbd50a9114f86e04858d71061a5b48517cbec2435c3bedd4c304b5d2`  
		Last Modified: Thu, 25 Jul 2024 17:24:41 GMT  
		Size: 1.9 KB (1863 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:11-jre-ubi9-minimal` - linux; s390x

```console
$ docker pull eclipse-temurin@sha256:0c275cf9e64531fb9923cc270ae9870bee60fd74858eda12662a571225a46f15
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **102.7 MB (102675470 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f60a8d263984b40b5cc08768db4f8ce836ef551847debcbcd7088adc74c5fb60`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`

```dockerfile
# Thu, 18 Jul 2024 16:02:12 GMT
ADD file:1a0498fcbd53ea6a4cce5caa1a166c86ab5a3d63fb2e6f1005f6229cd3fd8ddc in / 
# Thu, 18 Jul 2024 16:02:13 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Thu, 18 Jul 2024 16:02:13 GMT
ADD file:5b1f650e1376d79fa3a65df4a154ea5166def95154b52c1c1097dfd8fc7d58eb in /tmp/tls-ca-bundle.pem 
# Thu, 18 Jul 2024 16:02:13 GMT
ADD multi:39cf1126311f383f05bcdcfb2be4d277a3c28e8231fe3885ec63ceb2c04249b8 in /etc/yum.repos.d/ 
# Thu, 18 Jul 2024 16:02:13 GMT
LABEL maintainer="Red Hat, Inc."
# Thu, 18 Jul 2024 16:02:13 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.4"
# Thu, 18 Jul 2024 16:02:13 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Thu, 18 Jul 2024 16:02:13 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Thu, 18 Jul 2024 16:02:13 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 18 Jul 2024 16:02:13 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Thu, 18 Jul 2024 16:02:13 GMT
LABEL io.openshift.expose-services=""
# Thu, 18 Jul 2024 16:02:13 GMT
LABEL io.openshift.tags="minimal rhel9"
# Thu, 18 Jul 2024 16:02:13 GMT
ENV container oci
# Thu, 18 Jul 2024 16:02:13 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 18 Jul 2024 16:02:13 GMT
CMD ["/bin/bash"]
# Thu, 18 Jul 2024 16:02:14 GMT
RUN rm -rf /var/log/*
# Thu, 18 Jul 2024 16:02:14 GMT
LABEL release=1194
# Thu, 18 Jul 2024 16:02:15 GMT
ADD file:260b735774b29b332765c57758623137b24eea7dfd0749ddc4f622d177cc9a81 in /root/buildinfo/content_manifests/ubi9-minimal-container-9.4-1194.json 
# Thu, 18 Jul 2024 16:02:15 GMT
ADD file:6c5a2a1a67a074079cab4ce304a1b74e6ebbcec0d31479580388db97c242c818 in /root/buildinfo/Dockerfile-ubi9-minimal-9.4-1194 
# Thu, 18 Jul 2024 16:02:15 GMT
LABEL "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2024-07-18T15:52:43" "architecture"="s390x" "vcs-type"="git" "vcs-ref"="94baa7760359088a42ad33dc22d329a5ee2c7209" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi9-minimal/images/9.4-1194"
# Thu, 18 Jul 2024 16:02:16 GMT
RUN rm -f '/etc/yum.repos.d/repo-05248.repo' '/etc/yum.repos.d/repo-09742.repo'
# Thu, 18 Jul 2024 16:02:17 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Thu, 18 Jul 2024 16:02:18 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Wed, 24 Jul 2024 22:19:06 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 24 Jul 2024 22:19:06 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Jul 2024 22:19:06 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 24 Jul 2024 22:19:06 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         fontconfig         glibc-langpack-en     ;     microdnf clean all # buildkit
# Wed, 24 Jul 2024 22:19:06 GMT
ENV JAVA_VERSION=jdk-11.0.24+8
# Wed, 24 Jul 2024 22:19:06 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='1fe97cdaad47d7d108f329c6e4560b46748ef7f2948a1027812ade0bbc2a3597';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.24_8.tar.gz';          ;;        ppc64le)          ESUM='8ee351314182df93fbad96139bb74b97814944d66197896e388404a1ecfa06b3';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.24_8.tar.gz';          ;;        s390x)          ESUM='5b331f093bb03126334bbbc24f05f60681baeda461d860e4e2cdb693ee54e0ed';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_s390x_linux_hotspot_11.0.24_8.tar.gz';          ;;        x86_64)          ESUM='e0c1938093da3780e4494d366a4e6b75584dde8d46a19acea6691ae11df4cda5';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jre_x64_linux_hotspot_11.0.24_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Wed, 24 Jul 2024 22:19:06 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 24 Jul 2024 22:19:06 GMT
COPY entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 24 Jul 2024 22:19:06 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
```

-	Layers:
	-	`sha256:503bb890315f555a5f9d7cf50d5a90a092481d25c9c474822b5e12c758ad6065`  
		Last Modified: Wed, 24 Jul 2024 00:09:55 GMT  
		Size: 37.1 MB (37116517 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:067abbd59221a137019fc8775d8224b3867a3583ecfaf2af6a4d69582b0d7643`  
		Last Modified: Wed, 24 Jul 2024 23:02:44 GMT  
		Size: 27.8 MB (27772786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c91b6d6fb33affeebe2d6d82c73f816831d7a2778bf1d9b4f023a073abcb75e6`  
		Last Modified: Wed, 24 Jul 2024 23:03:01 GMT  
		Size: 37.8 MB (37784173 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:527caced2889872e10088b435fdf34114a16ebdc59586cd77db42623ffb13a6e`  
		Last Modified: Wed, 24 Jul 2024 23:02:57 GMT  
		Size: 127.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2496384606e91daad5308c1716a6bd115e83dd4b9a48c7f5327a1808fe9b868`  
		Last Modified: Thu, 25 Jul 2024 17:48:17 GMT  
		Size: 1.9 KB (1867 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
