## `eclipse-temurin:11-jdk-ubi9-minimal`

```console
$ docker pull eclipse-temurin@sha256:c3959b5a0fbfb42b1b649752e1504116c3d8533ede8f59656005bc4c4c27c660
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 8
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `eclipse-temurin:11-jdk-ubi9-minimal` - linux; amd64

```console
$ docker pull eclipse-temurin@sha256:80d46c81fac757030995e6d0b10bed55b7413d5a61f0eeed9704ae6ffe470988
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **209.6 MB (209571564 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:243e9a8543f1ab7034cd611d7a5232165450b4e7b66a614fb8437ff53ae39df1`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 25 Mar 2025 15:00:05 GMT
LABEL maintainer="Red Hat, Inc."
# Tue, 25 Mar 2025 15:00:05 GMT
LABEL vendor="Red Hat, Inc."
# Tue, 25 Mar 2025 15:00:06 GMT
LABEL url="https://www.redhat.com"
# Tue, 25 Mar 2025 15:00:06 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.5"       distribution-scope="public"
# Tue, 25 Mar 2025 15:00:06 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Tue, 25 Mar 2025 15:00:06 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Tue, 25 Mar 2025 15:00:06 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Tue, 25 Mar 2025 15:00:06 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Tue, 25 Mar 2025 15:00:06 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Tue, 25 Mar 2025 15:00:06 GMT
LABEL io.openshift.expose-services=""
# Tue, 25 Mar 2025 15:00:06 GMT
LABEL io.openshift.tags="minimal rhel9"
# Tue, 25 Mar 2025 15:00:06 GMT
ENV container oci
# Tue, 25 Mar 2025 15:00:06 GMT
COPY dir:df27096315f97be2134faf11df5dc31f92c8dd671e0b8267905e1f2330865336 in / 
# Tue, 25 Mar 2025 15:00:06 GMT
COPY file:b37d593713ee21ad52a4cd1424dc019a24f7966f85df0ac4b86d234302695328 in /etc/yum.repos.d/. 
# Tue, 25 Mar 2025 15:00:06 GMT
CMD ["/bin/bash"]
# Tue, 25 Mar 2025 15:00:06 GMT
RUN . /cachi2/cachi2.env &&     rm -rf /var/log/*
# Tue, 25 Mar 2025 15:00:07 GMT
LABEL "build-date"="2025-03-25T14:59:41" "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="63823c7605fee63261a8e33cad8085bc4bb24676" "build-date"="2025-03-25T14:50:12Z" "release"="1742914212"
# Tue, 25 Mar 2025 15:00:12 GMT
RUN /bin/sh
# Wed, 23 Apr 2025 14:48:05 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 23 Apr 2025 14:48:05 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 23 Apr 2025 14:48:05 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 23 Apr 2025 14:48:05 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en     ;     microdnf clean all # buildkit
# Wed, 23 Apr 2025 14:48:05 GMT
ENV JAVA_VERSION=jdk-11.0.27+6
# Wed, 23 Apr 2025 14:48:05 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='4decd2e5caf4667144091cf723458b14148dc990730b3ecb34bba5eb1aa4ad5d';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.27%2B6/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.27_6.tar.gz';          ;;        ppc64le)          ESUM='9407ecef765ec681fb187f084f1e029001abd5baf7a13b32067e9cbdfb140130';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.27%2B6/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.27_6.tar.gz';          ;;        s390x)          ESUM='89df8583779b880f21b6cf29ddd9438961e2b1a092f416d05255fd6cd7f0e9fe';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.27%2B6/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.27_6.tar.gz';          ;;        x86_64)          ESUM='dc6136eaa8c1898cbf8973bb1e203e1f653f4c9166be0f5bebe0b02c5f3b5ae3';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.27%2B6/OpenJDK11U-jdk_x64_linux_hotspot_11.0.27_6.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Wed, 23 Apr 2025 14:48:05 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 23 Apr 2025 14:48:05 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 23 Apr 2025 14:48:05 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 23 Apr 2025 14:48:05 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:9d561c17444a5f9cb82fc40d3d0e3f59b9f53e51dfb1c9e3d71c5c3ff898d151`  
		Last Modified: Tue, 25 Mar 2025 17:57:41 GMT  
		Size: 39.4 MB (39406022 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:adc97f92dbce4567ee13d265c17bca44426acd9f0e61a1f559344ae03bb336d2`  
		Last Modified: Tue, 25 Mar 2025 17:57:40 GMT  
		Size: 453.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f737f3b9a87c9eb9991bc22800465f1b0309dc2ca386ef0668a320c722806fd`  
		Last Modified: Wed, 23 Apr 2025 16:31:51 GMT  
		Size: 28.1 MB (28065839 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:112153c535379de650e0d80fd0ea51f8b9306b216e42b9c4f53d6a17dede0f8d`  
		Last Modified: Wed, 23 Apr 2025 16:31:54 GMT  
		Size: 142.1 MB (142096832 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f2ac010ff27f2821aa9a33f3b97b16e2298e086e9664e8c061fdf27936ebdc9`  
		Last Modified: Wed, 23 Apr 2025 16:31:50 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba8e1a87ffbb4cbf0153f38088cfd73f4d9ace35ec68344ab4a6b9673ef8e0d0`  
		Last Modified: Wed, 23 Apr 2025 16:31:50 GMT  
		Size: 2.3 KB (2289 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:11-jdk-ubi9-minimal` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:5250c51f767d7d34cb9299d9b59fb6967a87a81fdaac8e0745b93eb27b6b7833
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3621743 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cbb809d1f0cd58693cc09855a7c036e6b2373d6f107ecaa17114957e20bf57cb`

```dockerfile
```

-	Layers:
	-	`sha256:6e353c50863354d4479c1f9eecd23ff0d865a85d23c63fe5cc39086374e00efe`  
		Last Modified: Wed, 23 Apr 2025 16:31:51 GMT  
		Size: 3.6 MB (3599816 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1a604c9d123de36ed9e622a20fcdca1d2a1def7f5b7a737b9c459abef404dd13`  
		Last Modified: Wed, 23 Apr 2025 16:31:50 GMT  
		Size: 21.9 KB (21927 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-temurin:11-jdk-ubi9-minimal` - linux; arm64 variant v8

```console
$ docker pull eclipse-temurin@sha256:abf8a663db3214e4650d64e982d86e6329077ffe544bae3360e965741a4be8ce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **205.0 MB (204975953 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b545cc3631c55119cec76232e95176ea74f855537068e63d6e4737310180c3fa`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 25 Mar 2025 15:05:12 GMT
LABEL maintainer="Red Hat, Inc."
# Tue, 25 Mar 2025 15:05:12 GMT
LABEL vendor="Red Hat, Inc."
# Tue, 25 Mar 2025 15:05:12 GMT
LABEL url="https://www.redhat.com"
# Tue, 25 Mar 2025 15:05:12 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.5"       distribution-scope="public"
# Tue, 25 Mar 2025 15:05:12 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Tue, 25 Mar 2025 15:05:13 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Tue, 25 Mar 2025 15:05:13 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Tue, 25 Mar 2025 15:05:13 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Tue, 25 Mar 2025 15:05:13 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Tue, 25 Mar 2025 15:05:13 GMT
LABEL io.openshift.expose-services=""
# Tue, 25 Mar 2025 15:05:13 GMT
LABEL io.openshift.tags="minimal rhel9"
# Tue, 25 Mar 2025 15:05:13 GMT
ENV container oci
# Tue, 25 Mar 2025 15:05:14 GMT
COPY dir:36dabe56d778e21d6cac6872809f7ae0932c9956fe7621a40aed471a4eb28b35 in / 
# Tue, 25 Mar 2025 15:05:14 GMT
COPY file:b37d593713ee21ad52a4cd1424dc019a24f7966f85df0ac4b86d234302695328 in /etc/yum.repos.d/. 
# Tue, 25 Mar 2025 15:05:14 GMT
CMD ["/bin/bash"]
# Tue, 25 Mar 2025 15:05:14 GMT
RUN . /cachi2/cachi2.env &&     rm -rf /var/log/*
# Tue, 25 Mar 2025 15:05:14 GMT
LABEL "build-date"="2025-03-25T15:04:42" "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="63823c7605fee63261a8e33cad8085bc4bb24676" "build-date"="2025-03-25T14:50:12Z" "release"="1742914212"
# Tue, 25 Mar 2025 15:05:25 GMT
RUN /bin/sh
# Wed, 23 Apr 2025 14:48:05 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 23 Apr 2025 14:48:05 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 23 Apr 2025 14:48:05 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 23 Apr 2025 14:48:05 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en     ;     microdnf clean all # buildkit
# Wed, 23 Apr 2025 14:48:05 GMT
ENV JAVA_VERSION=jdk-11.0.27+6
# Wed, 23 Apr 2025 14:48:05 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='4decd2e5caf4667144091cf723458b14148dc990730b3ecb34bba5eb1aa4ad5d';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.27%2B6/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.27_6.tar.gz';          ;;        ppc64le)          ESUM='9407ecef765ec681fb187f084f1e029001abd5baf7a13b32067e9cbdfb140130';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.27%2B6/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.27_6.tar.gz';          ;;        s390x)          ESUM='89df8583779b880f21b6cf29ddd9438961e2b1a092f416d05255fd6cd7f0e9fe';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.27%2B6/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.27_6.tar.gz';          ;;        x86_64)          ESUM='dc6136eaa8c1898cbf8973bb1e203e1f653f4c9166be0f5bebe0b02c5f3b5ae3';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.27%2B6/OpenJDK11U-jdk_x64_linux_hotspot_11.0.27_6.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Wed, 23 Apr 2025 14:48:05 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 23 Apr 2025 14:48:05 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 23 Apr 2025 14:48:05 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 23 Apr 2025 14:48:05 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:7b061f511294c383e785796c55415ec3bed7fbb0a98d6cee8c8c6a1436d4ada8`  
		Last Modified: Tue, 25 Mar 2025 18:27:33 GMT  
		Size: 37.6 MB (37588703 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d6607d3dbc4fd04e0d544f944d20a47a5af1fa8a7520e1f37683ab236e23734`  
		Last Modified: Tue, 25 Mar 2025 18:27:31 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc161fbd238b5be2bdd624ab40e89933f0e00808deb9bfed3955aa0c6bfb80d7`  
		Last Modified: Wed, 23 Apr 2025 16:33:26 GMT  
		Size: 28.5 MB (28499508 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:222d01c4c6bdeb83106cfc195a47c32f5d592550987ca18cbeeffb82e41182be`  
		Last Modified: Wed, 23 Apr 2025 16:33:29 GMT  
		Size: 138.9 MB (138884868 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fe955643e5b09b2f34331e448ea05d99069037506ace497b993ca3680a5647e`  
		Last Modified: Wed, 23 Apr 2025 16:33:25 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12e67c74b7fbb9acdffc137f5fc910eee7e4400cbaf031cde8119fef53ae6bad`  
		Last Modified: Wed, 23 Apr 2025 16:33:25 GMT  
		Size: 2.3 KB (2289 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:11-jdk-ubi9-minimal` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:26b032c00e2fbdb95353e1ac57de96b272e0eb9ed1d1aa482d2555e9fd177fd8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3621672 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a64611d4ca963ef0a825fcec217dd7066cf7770248cfbc30de9f97562bb7d2cc`

```dockerfile
```

-	Layers:
	-	`sha256:f5649414fd0d9fc42ab97f8bfd8e128cd9416b7d07f22bf6e4aa016fc210f7b2`  
		Last Modified: Wed, 23 Apr 2025 16:33:25 GMT  
		Size: 3.6 MB (3599629 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1c5a50f91106e2366b70b491794dae1485dbe700ebd3b0128b1962580330b075`  
		Last Modified: Wed, 23 Apr 2025 16:33:25 GMT  
		Size: 22.0 KB (22043 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-temurin:11-jdk-ubi9-minimal` - linux; ppc64le

```console
$ docker pull eclipse-temurin@sha256:57cba8a739b92fa48e5030f094d8436031b663f40ac6ead6ff7644e7d1dbb10f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **203.6 MB (203585577 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:138013a30b5fe5aef91b1f2122291eda245ca7b4e5ef8c94b34c79d1729c0f89`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 25 Mar 2025 15:07:41 GMT
LABEL maintainer="Red Hat, Inc."
# Tue, 25 Mar 2025 15:07:41 GMT
LABEL vendor="Red Hat, Inc."
# Tue, 25 Mar 2025 15:07:41 GMT
LABEL url="https://www.redhat.com"
# Tue, 25 Mar 2025 15:07:41 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.5"       distribution-scope="public"
# Tue, 25 Mar 2025 15:07:41 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Tue, 25 Mar 2025 15:07:41 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Tue, 25 Mar 2025 15:07:41 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Tue, 25 Mar 2025 15:07:41 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Tue, 25 Mar 2025 15:07:41 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Tue, 25 Mar 2025 15:07:41 GMT
LABEL io.openshift.expose-services=""
# Tue, 25 Mar 2025 15:07:41 GMT
LABEL io.openshift.tags="minimal rhel9"
# Tue, 25 Mar 2025 15:07:41 GMT
ENV container oci
# Tue, 25 Mar 2025 15:07:42 GMT
COPY dir:b00ac549f2dec3c1bd1264d0d7e9b7a2b7f966cc212ebc6aee6ca6e7f8acdce4 in / 
# Tue, 25 Mar 2025 15:07:42 GMT
COPY file:b37d593713ee21ad52a4cd1424dc019a24f7966f85df0ac4b86d234302695328 in /etc/yum.repos.d/. 
# Tue, 25 Mar 2025 15:07:42 GMT
CMD ["/bin/bash"]
# Tue, 25 Mar 2025 15:07:43 GMT
RUN . /cachi2/cachi2.env &&     rm -rf /var/log/*
# Tue, 25 Mar 2025 15:07:43 GMT
LABEL "build-date"="2025-03-25T15:07:15" "architecture"="ppc64le" "vcs-type"="git" "vcs-ref"="63823c7605fee63261a8e33cad8085bc4bb24676" "build-date"="2025-03-25T14:50:12Z" "release"="1742914212"
# Tue, 25 Mar 2025 15:08:06 GMT
RUN /bin/sh
# Wed, 23 Apr 2025 14:48:05 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 23 Apr 2025 14:48:05 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 23 Apr 2025 14:48:05 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 23 Apr 2025 14:48:05 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en     ;     microdnf clean all # buildkit
# Wed, 23 Apr 2025 14:48:05 GMT
ENV JAVA_VERSION=jdk-11.0.27+6
# Wed, 23 Apr 2025 14:48:05 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='4decd2e5caf4667144091cf723458b14148dc990730b3ecb34bba5eb1aa4ad5d';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.27%2B6/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.27_6.tar.gz';          ;;        ppc64le)          ESUM='9407ecef765ec681fb187f084f1e029001abd5baf7a13b32067e9cbdfb140130';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.27%2B6/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.27_6.tar.gz';          ;;        s390x)          ESUM='89df8583779b880f21b6cf29ddd9438961e2b1a092f416d05255fd6cd7f0e9fe';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.27%2B6/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.27_6.tar.gz';          ;;        x86_64)          ESUM='dc6136eaa8c1898cbf8973bb1e203e1f653f4c9166be0f5bebe0b02c5f3b5ae3';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.27%2B6/OpenJDK11U-jdk_x64_linux_hotspot_11.0.27_6.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Wed, 23 Apr 2025 14:48:05 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 23 Apr 2025 14:48:05 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 23 Apr 2025 14:48:05 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 23 Apr 2025 14:48:05 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:32cf36dcf251c02cfc81f25bda80482c1e6394e4c1c7cb07317eebdc82a6ef45`  
		Last Modified: Tue, 25 Mar 2025 18:27:46 GMT  
		Size: 43.8 MB (43784360 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37f45749a0d155c224422d2f971c243e88e0afd5c485b88efda6760e3b544483`  
		Last Modified: Tue, 25 Mar 2025 18:27:43 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8dd16b4078507feb1a749b2528be46acfd33dc5eb554c6066f4283898325da2`  
		Last Modified: Wed, 23 Apr 2025 16:36:18 GMT  
		Size: 30.5 MB (30483703 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93020df380414b2d9fd3abc35766f5114277230541d924f55743400d3fad513d`  
		Last Modified: Wed, 23 Apr 2025 16:36:20 GMT  
		Size: 129.3 MB (129314643 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:418513018029083c31147431c8fe51d2c2293fd0e166cef65cba24e7c6607506`  
		Last Modified: Wed, 23 Apr 2025 16:36:16 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83fef8afd042df66056e2597d69219b184e06045b31940646318973f5b534424`  
		Last Modified: Wed, 23 Apr 2025 16:36:16 GMT  
		Size: 2.3 KB (2287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:11-jdk-ubi9-minimal` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:f39740f249f0a796ded1b7288aac0a65261e82d4901706573722ff0ecb655ab1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3619081 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e1d5e4a7a1c16ad853fbc1901827f96cd529b11527a903b1feb29b619b00092e`

```dockerfile
```

-	Layers:
	-	`sha256:049747633937aca9c94260bb8cc117bbaac549ffd7ddd1d29cd66ff453cb9bb0`  
		Last Modified: Wed, 23 Apr 2025 16:36:17 GMT  
		Size: 3.6 MB (3597118 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fe12a3ffa6ecc4cab243dc860007bcff4d0d0edfdf7f24279c343498cd974dc9`  
		Last Modified: Wed, 23 Apr 2025 16:36:16 GMT  
		Size: 22.0 KB (21963 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-temurin:11-jdk-ubi9-minimal` - linux; s390x

```console
$ docker pull eclipse-temurin@sha256:5494a8b9dad1c2e2dc0b8949ed6c8fa8a960a4ae41c1c355a3aafa52483f6d32
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **187.6 MB (187572493 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:970b863c10d29370a1f6986d61af79016e58b5d402a03c9c4902a0da4626fad7`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 25 Mar 2025 15:02:51 GMT
LABEL maintainer="Red Hat, Inc."
# Tue, 25 Mar 2025 15:02:51 GMT
LABEL vendor="Red Hat, Inc."
# Tue, 25 Mar 2025 15:02:51 GMT
LABEL url="https://www.redhat.com"
# Tue, 25 Mar 2025 15:02:51 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.5"       distribution-scope="public"
# Tue, 25 Mar 2025 15:02:51 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Tue, 25 Mar 2025 15:02:51 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Tue, 25 Mar 2025 15:02:51 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Tue, 25 Mar 2025 15:02:51 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Tue, 25 Mar 2025 15:02:51 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Tue, 25 Mar 2025 15:02:51 GMT
LABEL io.openshift.expose-services=""
# Tue, 25 Mar 2025 15:02:51 GMT
LABEL io.openshift.tags="minimal rhel9"
# Tue, 25 Mar 2025 15:02:51 GMT
ENV container oci
# Tue, 25 Mar 2025 15:02:52 GMT
COPY dir:a7bb5171f825e631f2fbfeb72bf76644ef5188e2e0888380a0572aaba26faac9 in / 
# Tue, 25 Mar 2025 15:02:52 GMT
COPY file:b37d593713ee21ad52a4cd1424dc019a24f7966f85df0ac4b86d234302695328 in /etc/yum.repos.d/. 
# Tue, 25 Mar 2025 15:02:52 GMT
CMD ["/bin/bash"]
# Tue, 25 Mar 2025 15:02:53 GMT
RUN . /cachi2/cachi2.env &&     rm -rf /var/log/*
# Tue, 25 Mar 2025 15:02:53 GMT
LABEL "build-date"="2025-03-25T15:02:03" "architecture"="s390x" "vcs-type"="git" "vcs-ref"="63823c7605fee63261a8e33cad8085bc4bb24676" "build-date"="2025-03-25T14:50:12Z" "release"="1742914212"
# Tue, 25 Mar 2025 15:03:05 GMT
RUN /bin/sh
# Wed, 23 Apr 2025 14:48:05 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 23 Apr 2025 14:48:05 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 23 Apr 2025 14:48:05 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 23 Apr 2025 14:48:05 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en     ;     microdnf clean all # buildkit
# Wed, 23 Apr 2025 14:48:05 GMT
ENV JAVA_VERSION=jdk-11.0.27+6
# Wed, 23 Apr 2025 14:48:05 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='4decd2e5caf4667144091cf723458b14148dc990730b3ecb34bba5eb1aa4ad5d';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.27%2B6/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.27_6.tar.gz';          ;;        ppc64le)          ESUM='9407ecef765ec681fb187f084f1e029001abd5baf7a13b32067e9cbdfb140130';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.27%2B6/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.27_6.tar.gz';          ;;        s390x)          ESUM='89df8583779b880f21b6cf29ddd9438961e2b1a092f416d05255fd6cd7f0e9fe';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.27%2B6/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.27_6.tar.gz';          ;;        x86_64)          ESUM='dc6136eaa8c1898cbf8973bb1e203e1f653f4c9166be0f5bebe0b02c5f3b5ae3';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.27%2B6/OpenJDK11U-jdk_x64_linux_hotspot_11.0.27_6.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Wed, 23 Apr 2025 14:48:05 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 23 Apr 2025 14:48:05 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 23 Apr 2025 14:48:05 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 23 Apr 2025 14:48:05 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:74f4d563c72f05b431ebba5e82692949551dc223392c5db8c42b58bb6f55d86e`  
		Last Modified: Tue, 25 Mar 2025 18:27:40 GMT  
		Size: 37.5 MB (37501550 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ad3638df35816097dbfdec8d194c1189b9a49dd23bab5049024abcbef9c3efd`  
		Last Modified: Tue, 25 Mar 2025 18:27:37 GMT  
		Size: 459.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f746f27a376f740459d18683b51e242d1f6d93ce0a59662ea97dec4e1ed5dcf`  
		Last Modified: Wed, 23 Apr 2025 16:34:10 GMT  
		Size: 28.1 MB (28073479 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5ffbb5c0205bdf53451c82230e6a1d9838f6691fa34dd027e1d4ebf7099fccb`  
		Last Modified: Wed, 23 Apr 2025 16:34:12 GMT  
		Size: 122.0 MB (121994587 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b28535c37be7dbec3a91828f837192369ba3c1484d34d9d9d6da6491d73f01c`  
		Last Modified: Wed, 23 Apr 2025 16:34:10 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c09f3ec8a74349761861f9db3fac55f0603362e002388c8011428ea140956ae`  
		Last Modified: Wed, 23 Apr 2025 16:34:10 GMT  
		Size: 2.3 KB (2289 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:11-jdk-ubi9-minimal` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:eadf1d029bb2052fe99ef1edadb1239323b9be2f1716eafabef2acca092a7b28
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3608963 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:016187eced769c062f45280cc9d238131bf1d0f7eb8c096140f21f422feda222`

```dockerfile
```

-	Layers:
	-	`sha256:4812a588b261478622036d68641d2a5896e2cfd99706c501545c199f1d364084`  
		Last Modified: Wed, 23 Apr 2025 16:34:11 GMT  
		Size: 3.6 MB (3587037 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0d37f9411a0e05bc9e1ce0879572b9f0fcffd3cd249c00919d522962877d5321`  
		Last Modified: Wed, 23 Apr 2025 16:34:09 GMT  
		Size: 21.9 KB (21926 bytes)  
		MIME: application/vnd.in-toto+json
