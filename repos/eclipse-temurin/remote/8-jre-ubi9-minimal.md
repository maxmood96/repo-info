## `eclipse-temurin:8-jre-ubi9-minimal`

```console
$ docker pull eclipse-temurin@sha256:6b0bed46e644d391d1a03c83d0535b056be438de55c36c988f92a018f85b97ab
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `eclipse-temurin:8-jre-ubi9-minimal` - linux; amd64

```console
$ docker pull eclipse-temurin@sha256:ef93309eb4aa0dbc51af63f31f087e401e0707fd65b17125059842c83f214679
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **110.7 MB (110683334 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7981f55ba429a9dc05454807ba84febce05f4336dacedca466c44625121b8d2e`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`

```dockerfile
# Tue, 02 Jun 2026 05:45:15 GMT
LABEL maintainer="Red Hat, Inc."
# Tue, 02 Jun 2026 05:45:15 GMT
LABEL vendor="Red Hat, Inc."
# Tue, 02 Jun 2026 05:45:15 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Tue, 02 Jun 2026 05:45:15 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.8"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Tue, 02 Jun 2026 05:45:15 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Tue, 02 Jun 2026 05:45:15 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Tue, 02 Jun 2026 05:45:15 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Tue, 02 Jun 2026 05:45:15 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Tue, 02 Jun 2026 05:45:15 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Tue, 02 Jun 2026 05:45:15 GMT
LABEL io.openshift.expose-services=""
# Tue, 02 Jun 2026 05:45:15 GMT
LABEL io.openshift.tags="minimal rhel9"
# Tue, 02 Jun 2026 05:45:15 GMT
ENV container oci
# Tue, 02 Jun 2026 05:45:16 GMT
COPY dir:089626db9f0e556d2460ea9b02a44cc63366766c2d8912a1fd05fdd542cbb8e4 in /      
# Tue, 02 Jun 2026 05:45:16 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Tue, 02 Jun 2026 05:45:16 GMT
CMD ["/bin/bash"]
# Tue, 02 Jun 2026 05:45:17 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /usr/share/buildinfo/content-sets.json      
# Tue, 02 Jun 2026 05:45:17 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /root/buildinfo/content_manifests/content-sets.json      
# Tue, 02 Jun 2026 05:45:17 GMT
COPY file:aae7c733edba3a2c94cde549acbeb2025333f3fac20483f5ec988a263ea63dc6 in /usr/share/buildinfo/labels.json      
# Tue, 02 Jun 2026 05:45:17 GMT
COPY file:aae7c733edba3a2c94cde549acbeb2025333f3fac20483f5ec988a263ea63dc6 in /root/buildinfo/labels.json      
# Tue, 02 Jun 2026 05:45:17 GMT
LABEL "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="842dd1c603c36c8d242d5ec075adccffb3bfea5c" "org.opencontainers.image.revision"="842dd1c603c36c8d242d5ec075adccffb3bfea5c" "build-date"="2026-06-02T05:44:58Z" "org.opencontainers.image.created"="2026-06-02T05:44:58Z" "release"="1780378819"org.opencontainers.image.revision=842dd1c603c36c8d242d5ec075adccffb3bfea5c,org.opencontainers.image.created=2026-06-02T05:44:58Z
# Tue, 02 Jun 2026 22:44:32 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 02 Jun 2026 22:44:32 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Jun 2026 22:44:32 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 02 Jun 2026 22:44:32 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en     ;     microdnf clean all # buildkit
# Tue, 02 Jun 2026 22:44:32 GMT
ENV JAVA_VERSION=jdk8u492-b09
# Tue, 02 Jun 2026 22:44:35 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='d5e50cb002600007dbdfac523605d26196607fa5212db0942ef05cdce9fe2892';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u492-b09/OpenJDK8U-jre_aarch64_linux_hotspot_8u492b09.tar.gz';          ;;        ppc64le)          ESUM='4f724a0fce1117521a3a3e55ebb0281d56f6c9a066092bc3186ee40d8cd955a2';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u492-b09/OpenJDK8U-jre_ppc64le_linux_hotspot_8u492b09.tar.gz';          ;;        x86_64)          ESUM='8eef3d4a837bb7a9e45d30a7579d84d5b76a4321f4376573311e6bf89e48f9b0';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u492-b09/OpenJDK8U-jre_x64_linux_hotspot_8u492b09.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz; # buildkit
# Tue, 02 Jun 2026 22:44:36 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java -version"; java -version;     echo "Complete." # buildkit
# Tue, 02 Jun 2026 22:44:36 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 02 Jun 2026 22:44:36 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
```

-	Layers:
	-	`sha256:dd148063a98f38d63a03cea2357d237d418889b91f204f507c033c944e443f45`  
		Last Modified: Tue, 02 Jun 2026 07:03:29 GMT  
		Size: 40.7 MB (40687042 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:737d5834ac9e90baacae81f66d9889c18c39c842a58221625641a8cf7547345c`  
		Last Modified: Tue, 02 Jun 2026 22:44:49 GMT  
		Size: 27.7 MB (27661506 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3218214c65f1592725d9fbc9a403c0ac16a6edca8e596a6aadd6ef2734a993ff`  
		Last Modified: Tue, 02 Jun 2026 22:44:49 GMT  
		Size: 42.3 MB (42332191 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8998ecdc37c2ed0900cdab6cbb6a161bb3f916802b36d9d05a137d2d78021c67`  
		Last Modified: Tue, 02 Jun 2026 22:44:47 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6588ac76dd0f5cef16f31fa0bde8e6d34bfa5e60e0ffd1088138750f59cf4784`  
		Last Modified: Tue, 02 Jun 2026 22:44:48 GMT  
		Size: 2.5 KB (2467 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:8-jre-ubi9-minimal` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:474ae37527c96a2152948c81990b5f0cd1ef38f444c09b21334b9cb88455532d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2458811 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac4bc53d5c48872f1d29c4ae4615ea6b7dde48001739a8c5c5a7d8c6132eb01e`

```dockerfile
```

-	Layers:
	-	`sha256:10cfc9653fed65341839caefee072db43ad85b8ce6874b657902913db5c6f807`  
		Last Modified: Tue, 02 Jun 2026 22:44:47 GMT  
		Size: 2.4 MB (2439464 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c8f828f359a237141e2c4a089d611bf2adf8b1e531762ebb325f9c1dd154e4a8`  
		Last Modified: Tue, 02 Jun 2026 22:44:47 GMT  
		Size: 19.3 KB (19347 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-temurin:8-jre-ubi9-minimal` - linux; arm64 variant v8

```console
$ docker pull eclipse-temurin@sha256:dd60f15c698b34fc5caa48eda410371a45bc6965f94e5c7a430a622642dd0f40
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **108.3 MB (108264707 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff114799ab5554a156f42b4978b20e5a6d7b2888f2754839b79391e89acb306c`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`

```dockerfile
# Tue, 02 Jun 2026 05:43:50 GMT
LABEL maintainer="Red Hat, Inc."
# Tue, 02 Jun 2026 05:43:50 GMT
LABEL vendor="Red Hat, Inc."
# Tue, 02 Jun 2026 05:43:50 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Tue, 02 Jun 2026 05:43:50 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.8"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Tue, 02 Jun 2026 05:43:50 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Tue, 02 Jun 2026 05:43:50 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Tue, 02 Jun 2026 05:43:50 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Tue, 02 Jun 2026 05:43:50 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Tue, 02 Jun 2026 05:43:50 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Tue, 02 Jun 2026 05:43:50 GMT
LABEL io.openshift.expose-services=""
# Tue, 02 Jun 2026 05:43:50 GMT
LABEL io.openshift.tags="minimal rhel9"
# Tue, 02 Jun 2026 05:43:50 GMT
ENV container oci
# Tue, 02 Jun 2026 05:43:51 GMT
COPY dir:45e3b0db7c7574b63ad7ec3e8aa88c1c154d382f5d855d74a5a8b46ed379a850 in /      
# Tue, 02 Jun 2026 05:43:51 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Tue, 02 Jun 2026 05:43:51 GMT
CMD ["/bin/bash"]
# Tue, 02 Jun 2026 05:43:51 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /usr/share/buildinfo/content-sets.json      
# Tue, 02 Jun 2026 05:43:51 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /root/buildinfo/content_manifests/content-sets.json      
# Tue, 02 Jun 2026 05:43:52 GMT
COPY file:7aad34f99b458abb22df8550ad1aaf3928f914f8d425e14ac9708e9a77642cae in /usr/share/buildinfo/labels.json      
# Tue, 02 Jun 2026 05:43:52 GMT
COPY file:7aad34f99b458abb22df8550ad1aaf3928f914f8d425e14ac9708e9a77642cae in /root/buildinfo/labels.json      
# Tue, 02 Jun 2026 05:43:52 GMT
LABEL "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="842dd1c603c36c8d242d5ec075adccffb3bfea5c" "org.opencontainers.image.revision"="842dd1c603c36c8d242d5ec075adccffb3bfea5c" "build-date"="2026-06-02T05:43:37Z" "org.opencontainers.image.created"="2026-06-02T05:43:37Z" "release"="1780378819"org.opencontainers.image.revision=842dd1c603c36c8d242d5ec075adccffb3bfea5c,org.opencontainers.image.created=2026-06-02T05:43:37Z
# Tue, 02 Jun 2026 22:45:08 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 02 Jun 2026 22:45:08 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Jun 2026 22:45:08 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 02 Jun 2026 22:45:08 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en     ;     microdnf clean all # buildkit
# Tue, 02 Jun 2026 22:45:08 GMT
ENV JAVA_VERSION=jdk8u492-b09
# Tue, 02 Jun 2026 22:45:11 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='d5e50cb002600007dbdfac523605d26196607fa5212db0942ef05cdce9fe2892';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u492-b09/OpenJDK8U-jre_aarch64_linux_hotspot_8u492b09.tar.gz';          ;;        ppc64le)          ESUM='4f724a0fce1117521a3a3e55ebb0281d56f6c9a066092bc3186ee40d8cd955a2';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u492-b09/OpenJDK8U-jre_ppc64le_linux_hotspot_8u492b09.tar.gz';          ;;        x86_64)          ESUM='8eef3d4a837bb7a9e45d30a7579d84d5b76a4321f4376573311e6bf89e48f9b0';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u492-b09/OpenJDK8U-jre_x64_linux_hotspot_8u492b09.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz; # buildkit
# Tue, 02 Jun 2026 22:45:11 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java -version"; java -version;     echo "Complete." # buildkit
# Tue, 02 Jun 2026 22:45:11 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 02 Jun 2026 22:45:11 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
```

-	Layers:
	-	`sha256:7db43598c7e47cf895f880f92e3cee9c07787091c97802ea3f2bea8fa4848040`  
		Last Modified: Tue, 02 Jun 2026 07:03:29 GMT  
		Size: 38.9 MB (38863161 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9521dd1bbb2c89c1d73bc2821c947b3a0ed4f31ab21ff2cafc7e7d29f5a247a`  
		Last Modified: Tue, 02 Jun 2026 22:45:23 GMT  
		Size: 28.1 MB (28097288 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e967b595f5967ce5197fd4b26f531284ded8e5f86250825c3700d4e0245ce8b`  
		Last Modified: Tue, 02 Jun 2026 22:45:24 GMT  
		Size: 41.3 MB (41301659 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f55a8cd59304a4d37a6c1bca4c9e75db54904f3cc3066e6b13b6746042e9b248`  
		Last Modified: Tue, 02 Jun 2026 22:45:22 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de3986e628a81148d5a5a3d71d9d3829aeb01622ae3c39f914176fe50b7980d4`  
		Last Modified: Tue, 02 Jun 2026 22:45:22 GMT  
		Size: 2.5 KB (2472 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:8-jre-ubi9-minimal` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:20925dd7ba269cb21f94a3b76176da75ae643258196454b48a191fb0dc8708e2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2458965 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:54b1cd1eb712e6ae9a1b02ef17e9ca88f2dac1e627c1c6ccdbaf5099258879df`

```dockerfile
```

-	Layers:
	-	`sha256:b919ff724d86d0abcc0b708a8345622acf6bdfba2f4784b1b7c72e0b6eedd25c`  
		Last Modified: Tue, 02 Jun 2026 22:45:22 GMT  
		Size: 2.4 MB (2439514 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c9da954c2eb194de16efc704f68441e7ca0c8aef266c7c937e3c8045bdf8e52b`  
		Last Modified: Tue, 02 Jun 2026 22:45:22 GMT  
		Size: 19.5 KB (19451 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-temurin:8-jre-ubi9-minimal` - linux; ppc64le

```console
$ docker pull eclipse-temurin@sha256:6e637869d237541ebbd1c9af4cb3b86a966e019473c5afd711b1958bd81e6dd8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **117.0 MB (116983201 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1587fc6c51be30a998aebf05b08a9cb8a6d00a64e8076d80318670cbade75627`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`

```dockerfile
# Tue, 02 Jun 2026 05:43:57 GMT
LABEL maintainer="Red Hat, Inc."
# Tue, 02 Jun 2026 05:43:57 GMT
LABEL vendor="Red Hat, Inc."
# Tue, 02 Jun 2026 05:43:57 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Tue, 02 Jun 2026 05:43:57 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.8"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Tue, 02 Jun 2026 05:43:57 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Tue, 02 Jun 2026 05:43:57 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Tue, 02 Jun 2026 05:43:57 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Tue, 02 Jun 2026 05:43:57 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Tue, 02 Jun 2026 05:43:57 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Tue, 02 Jun 2026 05:43:57 GMT
LABEL io.openshift.expose-services=""
# Tue, 02 Jun 2026 05:43:57 GMT
LABEL io.openshift.tags="minimal rhel9"
# Tue, 02 Jun 2026 05:43:57 GMT
ENV container oci
# Tue, 02 Jun 2026 05:43:58 GMT
COPY dir:e2b77dc18737d07e8e5246d22c774c81a15fd49086dce884c4ad7e020854e7f1 in /      
# Tue, 02 Jun 2026 05:43:58 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Tue, 02 Jun 2026 05:43:58 GMT
CMD ["/bin/bash"]
# Tue, 02 Jun 2026 05:43:58 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /usr/share/buildinfo/content-sets.json      
# Tue, 02 Jun 2026 05:43:58 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /root/buildinfo/content_manifests/content-sets.json      
# Tue, 02 Jun 2026 05:43:58 GMT
COPY file:51b0adf8b5a4c3a24ace6c346ea6678803925c6cc30d08b64751f980b4528cc2 in /usr/share/buildinfo/labels.json      
# Tue, 02 Jun 2026 05:43:58 GMT
COPY file:51b0adf8b5a4c3a24ace6c346ea6678803925c6cc30d08b64751f980b4528cc2 in /root/buildinfo/labels.json      
# Tue, 02 Jun 2026 05:43:58 GMT
LABEL "architecture"="ppc64le" "vcs-type"="git" "vcs-ref"="842dd1c603c36c8d242d5ec075adccffb3bfea5c" "org.opencontainers.image.revision"="842dd1c603c36c8d242d5ec075adccffb3bfea5c" "build-date"="2026-06-02T05:43:46Z" "org.opencontainers.image.created"="2026-06-02T05:43:46Z" "release"="1780378819"org.opencontainers.image.revision=842dd1c603c36c8d242d5ec075adccffb3bfea5c,org.opencontainers.image.created=2026-06-02T05:43:46Z
# Tue, 02 Jun 2026 22:45:42 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 02 Jun 2026 22:45:42 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Jun 2026 22:45:42 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 02 Jun 2026 22:45:42 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en     ;     microdnf clean all # buildkit
# Tue, 02 Jun 2026 22:45:42 GMT
ENV JAVA_VERSION=jdk8u492-b09
# Tue, 02 Jun 2026 22:46:26 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='d5e50cb002600007dbdfac523605d26196607fa5212db0942ef05cdce9fe2892';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u492-b09/OpenJDK8U-jre_aarch64_linux_hotspot_8u492b09.tar.gz';          ;;        ppc64le)          ESUM='4f724a0fce1117521a3a3e55ebb0281d56f6c9a066092bc3186ee40d8cd955a2';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u492-b09/OpenJDK8U-jre_ppc64le_linux_hotspot_8u492b09.tar.gz';          ;;        x86_64)          ESUM='8eef3d4a837bb7a9e45d30a7579d84d5b76a4321f4376573311e6bf89e48f9b0';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u492-b09/OpenJDK8U-jre_x64_linux_hotspot_8u492b09.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz; # buildkit
# Tue, 02 Jun 2026 22:46:27 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java -version"; java -version;     echo "Complete." # buildkit
# Tue, 02 Jun 2026 22:46:28 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 02 Jun 2026 22:46:28 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
```

-	Layers:
	-	`sha256:5ff77d7ff78e7752137c3eba042a793ae2b415158af730c2f66c23814842a63f`  
		Last Modified: Tue, 02 Jun 2026 12:13:00 GMT  
		Size: 45.1 MB (45149918 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1fe7aeed3e9a0e4db7600177f2e2ad0b5eafa7a4390b1e052377528fb46b8a3`  
		Last Modified: Tue, 02 Jun 2026 22:46:32 GMT  
		Size: 30.1 MB (30090253 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c260d5b9fab40b35083ec1b817bc7e62616a1f425d5c96f123f712fd4b5e4be`  
		Last Modified: Tue, 02 Jun 2026 22:46:52 GMT  
		Size: 41.7 MB (41740436 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc4ab35fd90fc748f8809558d4d2307b54eb1af16f99344dc148151ac19307b3`  
		Last Modified: Tue, 02 Jun 2026 22:46:49 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6f52d7c135aa30470807db5d4d000225137b6b9728ab07929ccdf3092390206`  
		Last Modified: Tue, 02 Jun 2026 22:46:51 GMT  
		Size: 2.5 KB (2468 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:8-jre-ubi9-minimal` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:092a433a2870eefd5255c773c964be07fbb5d000ad8be44f1bb0901525a20771
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2459576 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e33a4af8bc4d610c00eff8da61b612a5c48c3a49d3ac6893a4cc79c9e0b386a`

```dockerfile
```

-	Layers:
	-	`sha256:26608ac9a3f8bc6cdeee5cb0a788b0b42fb8429487c75a1b57d5b09d3fcd7eb4`  
		Last Modified: Tue, 02 Jun 2026 22:46:51 GMT  
		Size: 2.4 MB (2440199 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f420a0990ebacfac32ac9aa458e780f8843f1bfc0bbeae550e47c4a638e9d4bf`  
		Last Modified: Tue, 02 Jun 2026 22:46:51 GMT  
		Size: 19.4 KB (19377 bytes)  
		MIME: application/vnd.in-toto+json
