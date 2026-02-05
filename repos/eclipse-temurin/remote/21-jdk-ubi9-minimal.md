## `eclipse-temurin:21-jdk-ubi9-minimal`

```console
$ docker pull eclipse-temurin@sha256:c1f19469cf4518108c0f0791fb5ac462149f4df2aba9d38c4ba942662ed2590d
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

### `eclipse-temurin:21-jdk-ubi9-minimal` - linux; amd64

```console
$ docker pull eclipse-temurin@sha256:fecfb860900020fabdf93691f6ee6a50bb12ae1de52f215e23c3d657066789d7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **214.1 MB (214087143 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:086240f34132790743def703c74f69d81b15a0c814b335afb469eb047c6edf9f`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 04 Feb 2026 11:16:42 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 04 Feb 2026 11:16:42 GMT
LABEL vendor="Red Hat, Inc."
# Wed, 04 Feb 2026 11:16:42 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Wed, 04 Feb 2026 11:16:42 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.7"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Wed, 04 Feb 2026 11:16:42 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 04 Feb 2026 11:16:43 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Wed, 04 Feb 2026 11:16:43 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 04 Feb 2026 11:16:43 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 04 Feb 2026 11:16:43 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Wed, 04 Feb 2026 11:16:43 GMT
LABEL io.openshift.expose-services=""
# Wed, 04 Feb 2026 11:16:43 GMT
LABEL io.openshift.tags="minimal rhel9"
# Wed, 04 Feb 2026 11:16:43 GMT
ENV container oci
# Wed, 04 Feb 2026 11:16:43 GMT
COPY dir:e45f16623580cdab20a9c9f5e40207717eeb9bb3de78238f58a6f3e3c0582b7c in /      
# Wed, 04 Feb 2026 11:16:44 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Wed, 04 Feb 2026 11:16:44 GMT
CMD ["/bin/bash"]
# Wed, 04 Feb 2026 11:16:44 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /usr/share/buildinfo/content-sets.json      
# Wed, 04 Feb 2026 11:16:44 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /root/buildinfo/content_manifests/content-sets.json      
# Wed, 04 Feb 2026 11:16:44 GMT
COPY file:1096bfd713df78e6dcdc10ea239637d266b09713d9b530275900d932460bb966 in /usr/share/buildinfo/labels.json      
# Wed, 04 Feb 2026 11:16:44 GMT
COPY file:1096bfd713df78e6dcdc10ea239637d266b09713d9b530275900d932460bb966 in /root/buildinfo/labels.json      
# Wed, 04 Feb 2026 11:16:44 GMT
LABEL "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="3ae6fd96d0d9bad11e8002483701f39edf2317f5" "org.opencontainers.image.revision"="3ae6fd96d0d9bad11e8002483701f39edf2317f5" "build-date"="2026-02-04T11:16:28Z" "org.opencontainers.image.created"="2026-02-04T11:16:28Z" "release"="1770203734"org.opencontainers.image.revision=3ae6fd96d0d9bad11e8002483701f39edf2317f5,org.opencontainers.image.created=2026-02-04T11:16:28Z
# Thu, 05 Feb 2026 00:08:21 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 05 Feb 2026 00:08:21 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 05 Feb 2026 00:08:21 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 05 Feb 2026 00:08:21 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en     ;     microdnf clean all # buildkit
# Thu, 05 Feb 2026 00:08:21 GMT
ENV JAVA_VERSION=jdk-21.0.9+10
# Thu, 05 Feb 2026 00:08:28 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='edf0da4debe7cf475dbe320d174d6eed81479eb363f41e38a2efb740428c603a';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.9%2B10/OpenJDK21U-jdk_aarch64_linux_hotspot_21.0.9_10.tar.gz';          ;;        ppc64le)          ESUM='ac5a0394a234269b4e20459649ac93cb702cde29b3e46a0bcf3aa53958f2d4a4';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.9%2B10/OpenJDK21U-jdk_ppc64le_linux_hotspot_21.0.9_10.tar.gz';          ;;        s390x)          ESUM='e8ede0fb48aaa3a0cc1ac7c8522f8ca7938bdbb8be0d603b61134de7f898aff4';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.9%2B10/OpenJDK21U-jdk_s390x_linux_hotspot_21.0.9_10.tar.gz';          ;;        x86_64)          ESUM='810d3773df7e0d6c4394e4e244b264c8b30e0b05a0acf542d065fd78a6b65c2f';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.9%2B10/OpenJDK21U-jdk_x64_linux_hotspot_21.0.9_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Thu, 05 Feb 2026 00:08:29 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 05 Feb 2026 00:08:29 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 05 Feb 2026 00:08:29 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 05 Feb 2026 00:08:29 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:b6f39ea02118ec2218902231f7c1bd7f8869072595a1fc81ad65ced100bfe327`  
		Last Modified: Wed, 04 Feb 2026 12:07:03 GMT  
		Size: 40.0 MB (40009059 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f1b10b3a42005669c4d444e5213eee3bb466cd85ec131877d5b4e733f86beb5`  
		Last Modified: Thu, 05 Feb 2026 00:08:46 GMT  
		Size: 16.2 MB (16246764 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26b6c6ce65ce93b7d87fd274d6ec3fb048000f7068db9bb430516b313592bf36`  
		Last Modified: Thu, 05 Feb 2026 00:08:49 GMT  
		Size: 157.8 MB (157828901 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc819f53c90331d24ebe7c1dcc8a0b6f53e4ac17c89137557bc5f74818137509`  
		Last Modified: Thu, 05 Feb 2026 00:08:45 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33bf1bfa4dfa30b97e781d982bfcee2042a9f6345fbd1052d434e53e0b43c6bb`  
		Last Modified: Thu, 05 Feb 2026 00:08:40 GMT  
		Size: 2.3 KB (2290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:21-jdk-ubi9-minimal` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:88892b15aff38beb3be0973d92afc7eb7b2725b8c1289e366c376a6cbe2535eb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.8 MB (1783722 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:835a179b172236fbc5f15ba37ff54f3bc327238a50f7738d73b0bb952c38c45d`

```dockerfile
```

-	Layers:
	-	`sha256:9d07d730ca75d029283f7111f65cd2125b44ac615060e197ef81fabfeb951094`  
		Last Modified: Thu, 05 Feb 2026 00:08:45 GMT  
		Size: 1.8 MB (1762578 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cecf66363af61b4c7c9653151590f07b43e57a9bb20e95a1ca2099b668e973e3`  
		Last Modified: Thu, 05 Feb 2026 00:08:45 GMT  
		Size: 21.1 KB (21144 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-temurin:21-jdk-ubi9-minimal` - linux; arm64 variant v8

```console
$ docker pull eclipse-temurin@sha256:c4b213297a8d66a17cf94ff3864680df5bb6f58f92b3b74614da2f4ff2d593ba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **211.1 MB (211094456 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb40f13ce635193336b4c31d53c8a0645d2bb7051cb76de0c2dbf0b94696700b`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 04 Feb 2026 11:19:42 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 04 Feb 2026 11:19:42 GMT
LABEL vendor="Red Hat, Inc."
# Wed, 04 Feb 2026 11:19:42 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Wed, 04 Feb 2026 11:19:42 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.7"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Wed, 04 Feb 2026 11:19:42 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 04 Feb 2026 11:19:42 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Wed, 04 Feb 2026 11:19:42 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 04 Feb 2026 11:19:42 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 04 Feb 2026 11:19:42 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Wed, 04 Feb 2026 11:19:42 GMT
LABEL io.openshift.expose-services=""
# Wed, 04 Feb 2026 11:19:42 GMT
LABEL io.openshift.tags="minimal rhel9"
# Wed, 04 Feb 2026 11:19:42 GMT
ENV container oci
# Wed, 04 Feb 2026 11:19:43 GMT
COPY dir:0c6fd0301db67da56e5ab3d7939a023e089cbf858b44dcb22c5b0ce99938dd88 in /      
# Wed, 04 Feb 2026 11:19:43 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Wed, 04 Feb 2026 11:19:43 GMT
CMD ["/bin/bash"]
# Wed, 04 Feb 2026 11:19:43 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /usr/share/buildinfo/content-sets.json      
# Wed, 04 Feb 2026 11:19:43 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /root/buildinfo/content_manifests/content-sets.json      
# Wed, 04 Feb 2026 11:19:43 GMT
COPY file:a4da6eddc8c7915fe221c5dff204968b8d70b2b38eb431f23c9bd1ea8a51989b in /usr/share/buildinfo/labels.json      
# Wed, 04 Feb 2026 11:19:43 GMT
COPY file:a4da6eddc8c7915fe221c5dff204968b8d70b2b38eb431f23c9bd1ea8a51989b in /root/buildinfo/labels.json      
# Wed, 04 Feb 2026 11:19:44 GMT
LABEL "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="3ae6fd96d0d9bad11e8002483701f39edf2317f5" "org.opencontainers.image.revision"="3ae6fd96d0d9bad11e8002483701f39edf2317f5" "build-date"="2026-02-04T11:19:27Z" "org.opencontainers.image.created"="2026-02-04T11:19:27Z" "release"="1770203734"org.opencontainers.image.revision=3ae6fd96d0d9bad11e8002483701f39edf2317f5,org.opencontainers.image.created=2026-02-04T11:19:27Z
# Thu, 05 Feb 2026 00:07:55 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 05 Feb 2026 00:07:55 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 05 Feb 2026 00:07:55 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 05 Feb 2026 00:07:55 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en     ;     microdnf clean all # buildkit
# Thu, 05 Feb 2026 00:07:55 GMT
ENV JAVA_VERSION=jdk-21.0.9+10
# Thu, 05 Feb 2026 00:08:03 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='edf0da4debe7cf475dbe320d174d6eed81479eb363f41e38a2efb740428c603a';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.9%2B10/OpenJDK21U-jdk_aarch64_linux_hotspot_21.0.9_10.tar.gz';          ;;        ppc64le)          ESUM='ac5a0394a234269b4e20459649ac93cb702cde29b3e46a0bcf3aa53958f2d4a4';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.9%2B10/OpenJDK21U-jdk_ppc64le_linux_hotspot_21.0.9_10.tar.gz';          ;;        s390x)          ESUM='e8ede0fb48aaa3a0cc1ac7c8522f8ca7938bdbb8be0d603b61134de7f898aff4';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.9%2B10/OpenJDK21U-jdk_s390x_linux_hotspot_21.0.9_10.tar.gz';          ;;        x86_64)          ESUM='810d3773df7e0d6c4394e4e244b264c8b30e0b05a0acf542d065fd78a6b65c2f';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.9%2B10/OpenJDK21U-jdk_x64_linux_hotspot_21.0.9_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Thu, 05 Feb 2026 00:08:04 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 05 Feb 2026 00:08:04 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 05 Feb 2026 00:08:04 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 05 Feb 2026 00:08:04 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:afeee6a1a7760e6f32c7c8492fc015c48e0a3314849bd8e7fd5fd947d0f45087`  
		Last Modified: Wed, 04 Feb 2026 12:09:12 GMT  
		Size: 38.2 MB (38195721 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bcaba18dbfe41d660df8c161c2cc784d1aa60c458f01944629d7289c48c61831`  
		Last Modified: Thu, 05 Feb 2026 00:08:22 GMT  
		Size: 16.8 MB (16784502 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3773a8479e5907a8d81afd806bd27ab0ba8414b104f7a8b1f3486210efbf37d`  
		Last Modified: Thu, 05 Feb 2026 00:08:26 GMT  
		Size: 156.1 MB (156111813 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:860e74498696f2aa69c86f87132677f4b292dd845c4643ba077f7de91ad11531`  
		Last Modified: Thu, 05 Feb 2026 00:08:21 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:685f247820aa7416397c3cdac48a8a216f99ba7b4cfe1995a4e26d451b58adb2`  
		Last Modified: Thu, 05 Feb 2026 00:08:21 GMT  
		Size: 2.3 KB (2291 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:21-jdk-ubi9-minimal` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:1dc2b99abafbb9529e0ab866e5d6eefa6be70d7115710393cab60d235facf08d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.8 MB (1784437 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d35bbfe264832937ad5d0c6d090eaf2f9459c886b2c1810ebde66bf4cca2335f`

```dockerfile
```

-	Layers:
	-	`sha256:b36f5175d85b8456aef6f5e581e95304659c12d96ff9aa0c2301c05554f5e56b`  
		Last Modified: Thu, 05 Feb 2026 00:08:21 GMT  
		Size: 1.8 MB (1763178 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bbb9118667b0e03e725fb94380cd9893ec21c1fd3a6ebce8fcaa1758e57cf26a`  
		Last Modified: Thu, 05 Feb 2026 00:08:21 GMT  
		Size: 21.3 KB (21259 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-temurin:21-jdk-ubi9-minimal` - linux; ppc64le

```console
$ docker pull eclipse-temurin@sha256:ee4e749cb96fda4a5b2096c2c486c9639dc90808001be03c875badfaafd6e0f9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **220.3 MB (220332055 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:43a4930489c7103c23521d8d926c3dbc40acd021dcb7d8516b47ed739c3366a3`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 04 Feb 2026 11:18:55 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 04 Feb 2026 11:18:55 GMT
LABEL vendor="Red Hat, Inc."
# Wed, 04 Feb 2026 11:18:55 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Wed, 04 Feb 2026 11:18:55 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.7"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Wed, 04 Feb 2026 11:18:55 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 04 Feb 2026 11:18:55 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Wed, 04 Feb 2026 11:18:55 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 04 Feb 2026 11:18:55 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 04 Feb 2026 11:18:55 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Wed, 04 Feb 2026 11:18:55 GMT
LABEL io.openshift.expose-services=""
# Wed, 04 Feb 2026 11:18:55 GMT
LABEL io.openshift.tags="minimal rhel9"
# Wed, 04 Feb 2026 11:18:55 GMT
ENV container oci
# Wed, 04 Feb 2026 11:18:56 GMT
COPY dir:ac22932cb19e0040fdd682ddcf58eafa9048ed80bbb0d7207ce4b58b9e8c1ce2 in /      
# Wed, 04 Feb 2026 11:18:56 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Wed, 04 Feb 2026 11:18:56 GMT
CMD ["/bin/bash"]
# Wed, 04 Feb 2026 11:18:56 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /usr/share/buildinfo/content-sets.json      
# Wed, 04 Feb 2026 11:18:56 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /root/buildinfo/content_manifests/content-sets.json      
# Wed, 04 Feb 2026 11:18:56 GMT
COPY file:fc9edd6729debe0b8fd283950946b54a98819aab2c1a7de7861de07a73ecdf6a in /usr/share/buildinfo/labels.json      
# Wed, 04 Feb 2026 11:18:57 GMT
COPY file:fc9edd6729debe0b8fd283950946b54a98819aab2c1a7de7861de07a73ecdf6a in /root/buildinfo/labels.json      
# Wed, 04 Feb 2026 11:18:57 GMT
LABEL "architecture"="ppc64le" "vcs-type"="git" "vcs-ref"="3ae6fd96d0d9bad11e8002483701f39edf2317f5" "org.opencontainers.image.revision"="3ae6fd96d0d9bad11e8002483701f39edf2317f5" "build-date"="2026-02-04T11:18:45Z" "org.opencontainers.image.created"="2026-02-04T11:18:45Z" "release"="1770203734"org.opencontainers.image.revision=3ae6fd96d0d9bad11e8002483701f39edf2317f5,org.opencontainers.image.created=2026-02-04T11:18:45Z
# Thu, 05 Feb 2026 01:21:28 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 05 Feb 2026 01:21:28 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 05 Feb 2026 01:21:28 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 05 Feb 2026 01:21:28 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en     ;     microdnf clean all # buildkit
# Thu, 05 Feb 2026 01:21:28 GMT
ENV JAVA_VERSION=jdk-21.0.9+10
# Thu, 05 Feb 2026 01:27:40 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='edf0da4debe7cf475dbe320d174d6eed81479eb363f41e38a2efb740428c603a';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.9%2B10/OpenJDK21U-jdk_aarch64_linux_hotspot_21.0.9_10.tar.gz';          ;;        ppc64le)          ESUM='ac5a0394a234269b4e20459649ac93cb702cde29b3e46a0bcf3aa53958f2d4a4';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.9%2B10/OpenJDK21U-jdk_ppc64le_linux_hotspot_21.0.9_10.tar.gz';          ;;        s390x)          ESUM='e8ede0fb48aaa3a0cc1ac7c8522f8ca7938bdbb8be0d603b61134de7f898aff4';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.9%2B10/OpenJDK21U-jdk_s390x_linux_hotspot_21.0.9_10.tar.gz';          ;;        x86_64)          ESUM='810d3773df7e0d6c4394e4e244b264c8b30e0b05a0acf542d065fd78a6b65c2f';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.9%2B10/OpenJDK21U-jdk_x64_linux_hotspot_21.0.9_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Thu, 05 Feb 2026 01:27:44 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 05 Feb 2026 01:27:45 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 05 Feb 2026 01:27:45 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 05 Feb 2026 01:27:45 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:9453cd9cf4ac5c59d91e7e792edc9ae031294feb6835b6b8c1c7fe6c37f48881`  
		Last Modified: Wed, 04 Feb 2026 12:09:30 GMT  
		Size: 44.5 MB (44463451 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d170a20879686144c2b4ce9850ec6c0a9ed22c29984ec411fbe7dbf6e9e455e`  
		Last Modified: Thu, 05 Feb 2026 01:22:09 GMT  
		Size: 17.9 MB (17922900 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2ef6f17003bc37854e3228e3852f440a4f0b9a294d2cc34fc6be8e80e7fed69`  
		Last Modified: Thu, 05 Feb 2026 01:28:26 GMT  
		Size: 157.9 MB (157943284 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8469088fbdf4d7b21b80f8c7ca27b7074c26c65da488549766e28c9466928dde`  
		Last Modified: Thu, 05 Feb 2026 01:28:22 GMT  
		Size: 130.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8557c584a6546f2e4deff532f4ae98186f43d3fd20fb4b680efb44f78188887`  
		Last Modified: Thu, 05 Feb 2026 01:28:22 GMT  
		Size: 2.3 KB (2290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:21-jdk-ubi9-minimal` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:691fa3a5e3be609b9891939ed035a38b54145d15d44b7db045b72c3cc9e84b7f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.8 MB (1784261 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:48adccc7fbe9e812e7293b402e9dca85cb05521e677cf2247d3809ddbca38d88`

```dockerfile
```

-	Layers:
	-	`sha256:7259b0edfb537856521f59862015de6e8310eaf8735e507c58e01eff2282547e`  
		Last Modified: Thu, 05 Feb 2026 01:28:23 GMT  
		Size: 1.8 MB (1763082 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9b940451719e7fea183a801a83b4b1320d81c5b3689c9eebe3935e07837f5d27`  
		Last Modified: Thu, 05 Feb 2026 01:28:22 GMT  
		Size: 21.2 KB (21179 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-temurin:21-jdk-ubi9-minimal` - linux; s390x

```console
$ docker pull eclipse-temurin@sha256:97db90e304ccb9a92f1f9771c9239132316ec37f58b54f4e9234f6d8247ba4e0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **201.8 MB (201814580 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:80a6a70de4a955ca117ff7a6e064e28f8906af9a3af2bf09eed0b6d814c0608d`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 04 Feb 2026 11:28:10 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 04 Feb 2026 11:28:10 GMT
LABEL vendor="Red Hat, Inc."
# Wed, 04 Feb 2026 11:28:10 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Wed, 04 Feb 2026 11:28:10 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.7"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Wed, 04 Feb 2026 11:28:10 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 04 Feb 2026 11:28:10 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Wed, 04 Feb 2026 11:28:10 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 04 Feb 2026 11:28:10 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 04 Feb 2026 11:28:10 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Wed, 04 Feb 2026 11:28:10 GMT
LABEL io.openshift.expose-services=""
# Wed, 04 Feb 2026 11:28:10 GMT
LABEL io.openshift.tags="minimal rhel9"
# Wed, 04 Feb 2026 11:28:10 GMT
ENV container oci
# Wed, 04 Feb 2026 11:28:10 GMT
COPY dir:ed1f066185517b0a2e4ef9432478916be75ee58442b799a2d0b87cd51ad8226a in /      
# Wed, 04 Feb 2026 11:28:10 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Wed, 04 Feb 2026 11:28:10 GMT
CMD ["/bin/bash"]
# Wed, 04 Feb 2026 11:28:10 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /usr/share/buildinfo/content-sets.json      
# Wed, 04 Feb 2026 11:28:11 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /root/buildinfo/content_manifests/content-sets.json      
# Wed, 04 Feb 2026 11:28:11 GMT
COPY file:696c21c97fda61d0f3f09e274ba392676dba268826f34e2eb4e63f66e68bb97f in /usr/share/buildinfo/labels.json      
# Wed, 04 Feb 2026 11:28:11 GMT
COPY file:696c21c97fda61d0f3f09e274ba392676dba268826f34e2eb4e63f66e68bb97f in /root/buildinfo/labels.json      
# Wed, 04 Feb 2026 11:28:11 GMT
LABEL "architecture"="s390x" "vcs-type"="git" "vcs-ref"="3ae6fd96d0d9bad11e8002483701f39edf2317f5" "org.opencontainers.image.revision"="3ae6fd96d0d9bad11e8002483701f39edf2317f5" "build-date"="2026-02-04T11:27:14Z" "org.opencontainers.image.created"="2026-02-04T11:27:14Z" "release"="1770203734"org.opencontainers.image.revision=3ae6fd96d0d9bad11e8002483701f39edf2317f5,org.opencontainers.image.created=2026-02-04T11:27:14Z
# Thu, 05 Feb 2026 00:08:02 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 05 Feb 2026 00:08:02 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 05 Feb 2026 00:08:02 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 05 Feb 2026 00:08:02 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en     ;     microdnf clean all # buildkit
# Thu, 05 Feb 2026 00:08:02 GMT
ENV JAVA_VERSION=jdk-21.0.9+10
# Thu, 05 Feb 2026 00:09:58 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='edf0da4debe7cf475dbe320d174d6eed81479eb363f41e38a2efb740428c603a';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.9%2B10/OpenJDK21U-jdk_aarch64_linux_hotspot_21.0.9_10.tar.gz';          ;;        ppc64le)          ESUM='ac5a0394a234269b4e20459649ac93cb702cde29b3e46a0bcf3aa53958f2d4a4';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.9%2B10/OpenJDK21U-jdk_ppc64le_linux_hotspot_21.0.9_10.tar.gz';          ;;        s390x)          ESUM='e8ede0fb48aaa3a0cc1ac7c8522f8ca7938bdbb8be0d603b61134de7f898aff4';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.9%2B10/OpenJDK21U-jdk_s390x_linux_hotspot_21.0.9_10.tar.gz';          ;;        x86_64)          ESUM='810d3773df7e0d6c4394e4e244b264c8b30e0b05a0acf542d065fd78a6b65c2f';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.9%2B10/OpenJDK21U-jdk_x64_linux_hotspot_21.0.9_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Thu, 05 Feb 2026 00:09:59 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 05 Feb 2026 00:09:59 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 05 Feb 2026 00:09:59 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 05 Feb 2026 00:09:59 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:a3073672938ee024c2e2b6308a166357e08b9d63db19f1301982940b3e05b9c5`  
		Last Modified: Wed, 04 Feb 2026 12:09:20 GMT  
		Size: 38.1 MB (38133403 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5540faaaec6efc23993321bef40a91c418bc593aa0b371fea6e1d4ab9d645a2c`  
		Last Modified: Thu, 05 Feb 2026 00:08:21 GMT  
		Size: 16.6 MB (16610355 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4fc4c295529c2827fb403c1d1e0e9589229427d9658e64a8d7b58bd2d7be7b8`  
		Last Modified: Thu, 05 Feb 2026 00:10:24 GMT  
		Size: 147.1 MB (147068401 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac4711d8cd411aded283fce2aa1863e61aa9427e910e542f5842296695ae2375`  
		Last Modified: Thu, 05 Feb 2026 00:10:21 GMT  
		Size: 130.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b71be70739272a4a7d73636965d4c8bc6f9c7854f1cd2f90ad918148870c3b4`  
		Last Modified: Thu, 05 Feb 2026 00:10:21 GMT  
		Size: 2.3 KB (2291 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:21-jdk-ubi9-minimal` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:17019a5ac620d65954eb76bb531d4de012cc2e31657d1813bf1b6bce61dc01a9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.8 MB (1782984 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a1be56fe4dc350cbfff4cc832b9bcaa8bfc7b969ab0ef0c1d85b3d511d442b61`

```dockerfile
```

-	Layers:
	-	`sha256:aabad0fa622ac691b095290e1ad0f20db9d4e800156bd5b2fdbd759eac69c306`  
		Last Modified: Thu, 05 Feb 2026 00:10:21 GMT  
		Size: 1.8 MB (1761840 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3dd6eb207802dca5b0b932f9296894837848d82c50db31d603bc72ccc4776634`  
		Last Modified: Thu, 05 Feb 2026 00:10:21 GMT  
		Size: 21.1 KB (21144 bytes)  
		MIME: application/vnd.in-toto+json
