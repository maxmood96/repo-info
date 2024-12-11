## `eclipse-temurin:23-jdk-ubi9-minimal`

```console
$ docker pull eclipse-temurin@sha256:7db8c30378bb136a70eec7a5830994f6e96e18de156de767dec9f87b0c8058b0
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

### `eclipse-temurin:23-jdk-ubi9-minimal` - linux; amd64

```console
$ docker pull eclipse-temurin@sha256:7510436d9a164deb639da031e4d223cfd2d546a59d9d80b6aa9f509e085b148c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **241.7 MB (241718811 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d648d95e33ed7ac92685e44a10bc2b3ea672a332329c9fc26ded1ce2c179c216`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 23 Oct 2024 15:41:32 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 23 Oct 2024 15:41:32 GMT
LABEL vendor="Red Hat, Inc."
# Wed, 23 Oct 2024 15:41:32 GMT
LABEL url="https://www.redhat.com"
# Wed, 23 Oct 2024 15:41:32 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.5"       distribution-scope="public"
# Wed, 23 Oct 2024 15:41:32 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 23 Oct 2024 15:41:32 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Wed, 23 Oct 2024 15:41:32 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 23 Oct 2024 15:41:32 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 23 Oct 2024 15:41:32 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Wed, 23 Oct 2024 15:41:32 GMT
LABEL io.openshift.expose-services=""
# Wed, 23 Oct 2024 15:41:32 GMT
LABEL io.openshift.tags="minimal rhel9"
# Wed, 23 Oct 2024 15:41:32 GMT
ENV container oci
# Wed, 23 Oct 2024 15:41:32 GMT
COPY dir:ce392e97b0a18d36dffa0c783a840f3ab28026ae011aa3a1855943fa61c597d8 in / 
# Wed, 23 Oct 2024 15:41:32 GMT
COPY file:b37d593713ee21ad52a4cd1424dc019a24f7966f85df0ac4b86d234302695328 in /etc/yum.repos.d/. 
# Wed, 23 Oct 2024 15:41:32 GMT
CMD ["/bin/bash"]
# Wed, 23 Oct 2024 15:41:32 GMT
RUN . /cachi2/cachi2.env &&     rm -rf /var/log/*
# Wed, 23 Oct 2024 15:41:32 GMT
LABEL "build-date"="2024-12-09T18:15:25" "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="fee5a8f3e74ac2340dca04210f5456952058c9f4" "build-date"="2024-12-09T18:11:07Z" "release"="1733767867"
# Wed, 23 Oct 2024 15:41:32 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 23 Oct 2024 15:41:32 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 23 Oct 2024 15:41:32 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 23 Oct 2024 15:41:32 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         fontconfig         glibc-langpack-en     ;     microdnf clean all # buildkit
# Wed, 23 Oct 2024 15:41:32 GMT
ENV JAVA_VERSION=jdk-23.0.1+11
# Wed, 23 Oct 2024 15:41:32 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='808e3843293e50515bf02ad2f956e543da65e32dac82ae7a266a147b3485c61a';          BINARY_URL='https://github.com/adoptium/temurin23-binaries/releases/download/jdk-23.0.1%2B11/OpenJDK23U-jdk_aarch64_linux_hotspot_23.0.1_11.tar.gz';          ;;        ppc64le)          ESUM='1885ab141fe7b8ed6beb77b814b1c1c99fd54713399bf917edb6a4020545adde';          BINARY_URL='https://github.com/adoptium/temurin23-binaries/releases/download/jdk-23.0.1%2B11/OpenJDK23U-jdk_ppc64le_linux_hotspot_23.0.1_11.tar.gz';          ;;        s390x)          ESUM='39419d72082faea6d2501223f1cbf6a9128bc23000adfb7b7ee7acfce422509c';          BINARY_URL='https://github.com/adoptium/temurin23-binaries/releases/download/jdk-23.0.1%2B11/OpenJDK23U-jdk_s390x_linux_hotspot_23.0.1_11.tar.gz';          ;;        x86_64)          ESUM='2400267e4e9c0f6ae880a4d763af6caf18c673714bdee5debf8388b0b5d52886';          BINARY_URL='https://github.com/adoptium/temurin23-binaries/releases/download/jdk-23.0.1%2B11/OpenJDK23U-jdk_x64_linux_hotspot_23.0.1_11.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -r "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Wed, 23 Oct 2024 15:41:32 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 23 Oct 2024 15:41:32 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 23 Oct 2024 15:41:32 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 23 Oct 2024 15:41:32 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:8afba38a614e150d5cec9d32c41bedfe2fe3cc1a11fbd33c712e10abb9e65de9`  
		Last Modified: Mon, 09 Dec 2024 19:12:44 GMT  
		Size: 39.4 MB (39419294 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af629cc6e22c24122233933f6f28e31d576a66e121841074aad3ebc2be483839`  
		Last Modified: Wed, 11 Dec 2024 20:29:57 GMT  
		Size: 37.0 MB (36992599 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a22d7fffe0eb78e6b250aa491a298e70b17c9bc4650981df451c400e41d188f`  
		Last Modified: Wed, 11 Dec 2024 20:29:59 GMT  
		Size: 165.3 MB (165304496 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfb3626d2bc1bd73eecb4cac71e8f444d8b054ef1d021fc34bb2fbc07edb5cde`  
		Last Modified: Wed, 11 Dec 2024 20:29:56 GMT  
		Size: 131.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c94b649bf503e4b03d8b18162dc49d8d8532fc072555ebe51b81287f55aa433e`  
		Last Modified: Wed, 11 Dec 2024 20:29:56 GMT  
		Size: 2.3 KB (2291 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:23-jdk-ubi9-minimal` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:13a83a6253e8d64444fd12e56f6d768d1f825275de74278e2a41882e06c050fd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3700896 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d7825792ab1ac6cc0aa75a1de103522a2cc3defcbf06b0a653b8b3af73bbee07`

```dockerfile
```

-	Layers:
	-	`sha256:d75e64345fb1239e5bd98c90eafa6d4c04cc9a216a0698a777151f2627debb8a`  
		Last Modified: Wed, 11 Dec 2024 20:29:56 GMT  
		Size: 3.7 MB (3679952 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d7ad0eb23266ebc1db599826ef0c2ab292f1faf85f048fce0b37b34f82140a6a`  
		Last Modified: Wed, 11 Dec 2024 20:29:56 GMT  
		Size: 20.9 KB (20944 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-temurin:23-jdk-ubi9-minimal` - linux; arm64 variant v8

```console
$ docker pull eclipse-temurin@sha256:d08c57e7c95504d7f6deb9660611f0db8b15ed26a178adec703448fd04382fa4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **238.4 MB (238391206 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8561aaa98145d97d24bd77d746cc2653a1b04e912ca2b8c64338782d8293e299`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 23 Oct 2024 15:41:32 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 23 Oct 2024 15:41:32 GMT
LABEL vendor="Red Hat, Inc."
# Wed, 23 Oct 2024 15:41:32 GMT
LABEL url="https://www.redhat.com"
# Wed, 23 Oct 2024 15:41:32 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.5"       distribution-scope="public"
# Wed, 23 Oct 2024 15:41:32 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 23 Oct 2024 15:41:32 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Wed, 23 Oct 2024 15:41:32 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 23 Oct 2024 15:41:32 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 23 Oct 2024 15:41:32 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Wed, 23 Oct 2024 15:41:32 GMT
LABEL io.openshift.expose-services=""
# Wed, 23 Oct 2024 15:41:32 GMT
LABEL io.openshift.tags="minimal rhel9"
# Wed, 23 Oct 2024 15:41:32 GMT
ENV container oci
# Wed, 23 Oct 2024 15:41:32 GMT
COPY dir:bb4d3e8bf66b9361ce2c66099dbb4009a49deed7f655ac787c49d395bf0c8ed0 in / 
# Wed, 23 Oct 2024 15:41:32 GMT
COPY file:b37d593713ee21ad52a4cd1424dc019a24f7966f85df0ac4b86d234302695328 in /etc/yum.repos.d/. 
# Wed, 23 Oct 2024 15:41:32 GMT
CMD ["/bin/bash"]
# Wed, 23 Oct 2024 15:41:32 GMT
RUN . /cachi2/cachi2.env &&     rm -rf /var/log/*
# Wed, 23 Oct 2024 15:41:32 GMT
LABEL "build-date"="2024-12-09T18:18:20" "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="fee5a8f3e74ac2340dca04210f5456952058c9f4" "build-date"="2024-12-09T18:11:07Z" "release"="1733767867"
# Wed, 23 Oct 2024 15:41:32 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 23 Oct 2024 15:41:32 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 23 Oct 2024 15:41:32 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 23 Oct 2024 15:41:32 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         fontconfig         glibc-langpack-en     ;     microdnf clean all # buildkit
# Wed, 23 Oct 2024 15:41:32 GMT
ENV JAVA_VERSION=jdk-23.0.1+11
# Wed, 23 Oct 2024 15:41:32 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='808e3843293e50515bf02ad2f956e543da65e32dac82ae7a266a147b3485c61a';          BINARY_URL='https://github.com/adoptium/temurin23-binaries/releases/download/jdk-23.0.1%2B11/OpenJDK23U-jdk_aarch64_linux_hotspot_23.0.1_11.tar.gz';          ;;        ppc64le)          ESUM='1885ab141fe7b8ed6beb77b814b1c1c99fd54713399bf917edb6a4020545adde';          BINARY_URL='https://github.com/adoptium/temurin23-binaries/releases/download/jdk-23.0.1%2B11/OpenJDK23U-jdk_ppc64le_linux_hotspot_23.0.1_11.tar.gz';          ;;        s390x)          ESUM='39419d72082faea6d2501223f1cbf6a9128bc23000adfb7b7ee7acfce422509c';          BINARY_URL='https://github.com/adoptium/temurin23-binaries/releases/download/jdk-23.0.1%2B11/OpenJDK23U-jdk_s390x_linux_hotspot_23.0.1_11.tar.gz';          ;;        x86_64)          ESUM='2400267e4e9c0f6ae880a4d763af6caf18c673714bdee5debf8388b0b5d52886';          BINARY_URL='https://github.com/adoptium/temurin23-binaries/releases/download/jdk-23.0.1%2B11/OpenJDK23U-jdk_x64_linux_hotspot_23.0.1_11.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -r "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Wed, 23 Oct 2024 15:41:32 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 23 Oct 2024 15:41:32 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 23 Oct 2024 15:41:32 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 23 Oct 2024 15:41:32 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:0ed94f65e4fba4435c4119e46186c8cd6e06d97d466980566e3061cc1a6a19a2`  
		Last Modified: Mon, 09 Dec 2024 21:46:51 GMT  
		Size: 37.6 MB (37647525 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e16a7178cd631e8e68738f34a2f20d3ba24d9ff892dd572f951fc36b2476268`  
		Last Modified: Wed, 11 Dec 2024 20:38:41 GMT  
		Size: 37.5 MB (37451094 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3e11ce114b8b830b1aac074767a49881f46b14efd308a42584c04cc096d8548`  
		Last Modified: Wed, 11 Dec 2024 20:43:10 GMT  
		Size: 163.3 MB (163290167 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e1cbffbcc45c3987c81e86bd6397dc28e4b08f6fc4cdf88aeeef6b41206509c`  
		Last Modified: Wed, 11 Dec 2024 20:43:06 GMT  
		Size: 130.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e6a311ca2338646f64c4957a6feffce235f52f3f0cba931ddb143d64ff07874`  
		Last Modified: Wed, 11 Dec 2024 20:43:06 GMT  
		Size: 2.3 KB (2290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:23-jdk-ubi9-minimal` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:df5227da818ddecf81450c4970346549e4b617e46311d74425a16e6002b4bf3f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3699665 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:74b533e34e13d0053efb1cb3e8afacc589f2aa3b11bc6217f9b5553fc013193e`

```dockerfile
```

-	Layers:
	-	`sha256:4ed0ff61aa82bdcb91e95b123a5ef5ee244d2db04fbf86dfa5ee48be68e876da`  
		Last Modified: Wed, 11 Dec 2024 20:43:06 GMT  
		Size: 3.7 MB (3678605 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fd06529940458f37e7e3206940d1110965c6947c857cc4886681b463dd37d6b2`  
		Last Modified: Wed, 11 Dec 2024 20:43:06 GMT  
		Size: 21.1 KB (21060 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-temurin:23-jdk-ubi9-minimal` - linux; ppc64le

```console
$ docker pull eclipse-temurin@sha256:eada56d8cca00bdd08273868f6a98ce6e41966deab5f6642bb3f13cb5ec913c2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **248.5 MB (248467883 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa59c6133e3ee38bdedbefe7d24f86ffe351126e66d605d011ad1786393859f0`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 23 Oct 2024 15:41:32 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 23 Oct 2024 15:41:32 GMT
LABEL vendor="Red Hat, Inc."
# Wed, 23 Oct 2024 15:41:32 GMT
LABEL url="https://www.redhat.com"
# Wed, 23 Oct 2024 15:41:32 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.5"       distribution-scope="public"
# Wed, 23 Oct 2024 15:41:32 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 23 Oct 2024 15:41:32 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Wed, 23 Oct 2024 15:41:32 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 23 Oct 2024 15:41:32 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 23 Oct 2024 15:41:32 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Wed, 23 Oct 2024 15:41:32 GMT
LABEL io.openshift.expose-services=""
# Wed, 23 Oct 2024 15:41:32 GMT
LABEL io.openshift.tags="minimal rhel9"
# Wed, 23 Oct 2024 15:41:32 GMT
ENV container oci
# Wed, 23 Oct 2024 15:41:32 GMT
COPY dir:8f21bb638bfc9999eb0c06c365b4f63918e550b9f8a3df9bb94983276e9b11a8 in / 
# Wed, 23 Oct 2024 15:41:32 GMT
COPY file:b37d593713ee21ad52a4cd1424dc019a24f7966f85df0ac4b86d234302695328 in /etc/yum.repos.d/. 
# Wed, 23 Oct 2024 15:41:32 GMT
CMD ["/bin/bash"]
# Wed, 23 Oct 2024 15:41:32 GMT
RUN . /cachi2/cachi2.env &&     rm -rf /var/log/*
# Wed, 23 Oct 2024 15:41:32 GMT
LABEL "build-date"="2024-12-09T18:28:12" "architecture"="ppc64le" "vcs-type"="git" "vcs-ref"="fee5a8f3e74ac2340dca04210f5456952058c9f4" "build-date"="2024-12-09T18:11:07Z" "release"="1733767867"
# Wed, 23 Oct 2024 15:41:32 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 23 Oct 2024 15:41:32 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 23 Oct 2024 15:41:32 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 23 Oct 2024 15:41:32 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         fontconfig         glibc-langpack-en     ;     microdnf clean all # buildkit
# Wed, 23 Oct 2024 15:41:32 GMT
ENV JAVA_VERSION=jdk-23.0.1+11
# Wed, 23 Oct 2024 15:41:32 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='808e3843293e50515bf02ad2f956e543da65e32dac82ae7a266a147b3485c61a';          BINARY_URL='https://github.com/adoptium/temurin23-binaries/releases/download/jdk-23.0.1%2B11/OpenJDK23U-jdk_aarch64_linux_hotspot_23.0.1_11.tar.gz';          ;;        ppc64le)          ESUM='1885ab141fe7b8ed6beb77b814b1c1c99fd54713399bf917edb6a4020545adde';          BINARY_URL='https://github.com/adoptium/temurin23-binaries/releases/download/jdk-23.0.1%2B11/OpenJDK23U-jdk_ppc64le_linux_hotspot_23.0.1_11.tar.gz';          ;;        s390x)          ESUM='39419d72082faea6d2501223f1cbf6a9128bc23000adfb7b7ee7acfce422509c';          BINARY_URL='https://github.com/adoptium/temurin23-binaries/releases/download/jdk-23.0.1%2B11/OpenJDK23U-jdk_s390x_linux_hotspot_23.0.1_11.tar.gz';          ;;        x86_64)          ESUM='2400267e4e9c0f6ae880a4d763af6caf18c673714bdee5debf8388b0b5d52886';          BINARY_URL='https://github.com/adoptium/temurin23-binaries/releases/download/jdk-23.0.1%2B11/OpenJDK23U-jdk_x64_linux_hotspot_23.0.1_11.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -r "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Wed, 23 Oct 2024 15:41:32 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 23 Oct 2024 15:41:32 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 23 Oct 2024 15:41:32 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 23 Oct 2024 15:41:32 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:7f109adddadf658534777a91b226ce1bc9f7dcc45f9c30eea9c0e426aadaa062`  
		Last Modified: Tue, 10 Dec 2024 00:14:54 GMT  
		Size: 43.8 MB (43801042 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67d525a4c647a13d8db1417c57a1dc81822cc7796bf044edd48aa9d99ca6ee58`  
		Last Modified: Wed, 11 Dec 2024 20:32:31 GMT  
		Size: 39.5 MB (39476600 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1c8db3958e1107d9146dd97410847a651683166696a3369bf61f290d694223c`  
		Last Modified: Wed, 11 Dec 2024 20:40:14 GMT  
		Size: 165.2 MB (165187819 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cd3b75694eb6be5171b1987ae78f49e3aa0a03daae637bec1161470e055ab99`  
		Last Modified: Wed, 11 Dec 2024 20:40:07 GMT  
		Size: 131.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba5df69e75ba3a577854c26ff8ca1550fea339d71863e377a637a9f650655ed2`  
		Last Modified: Wed, 11 Dec 2024 20:40:08 GMT  
		Size: 2.3 KB (2291 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:23-jdk-ubi9-minimal` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:22497dfc87348553e4ebdab43036ec805316f2b4e9f0e6681cb12201ee8f3761
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3698334 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e4b2d998ce20bc5481e977933719ddb6de2d38434b488115815e265c17b3d7b`

```dockerfile
```

-	Layers:
	-	`sha256:aa586e874b4ccc557cbb88cad6e77a8712145662605ec417e1f51a476da031c1`  
		Last Modified: Wed, 11 Dec 2024 20:40:08 GMT  
		Size: 3.7 MB (3677354 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b8cf1e0f6dec4def6fa0ea7834fe40547514e3e426e80054774e4f20ee20fb38`  
		Last Modified: Wed, 11 Dec 2024 20:40:07 GMT  
		Size: 21.0 KB (20980 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-temurin:23-jdk-ubi9-minimal` - linux; s390x

```console
$ docker pull eclipse-temurin@sha256:bc7abaaff39c3e2a2c40ac6e968e5dd425ee0a72b15cda6a8d18270235cbbf5e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.9 MB (228946891 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1706fe3504f9b8fb36ef979323eabc04dc16a55ed9f5cefb4a49af600d350387`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 23 Oct 2024 15:41:32 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 23 Oct 2024 15:41:32 GMT
LABEL vendor="Red Hat, Inc."
# Wed, 23 Oct 2024 15:41:32 GMT
LABEL url="https://www.redhat.com"
# Wed, 23 Oct 2024 15:41:32 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.5"       distribution-scope="public"
# Wed, 23 Oct 2024 15:41:32 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 23 Oct 2024 15:41:32 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Wed, 23 Oct 2024 15:41:32 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 23 Oct 2024 15:41:32 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 23 Oct 2024 15:41:32 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Wed, 23 Oct 2024 15:41:32 GMT
LABEL io.openshift.expose-services=""
# Wed, 23 Oct 2024 15:41:32 GMT
LABEL io.openshift.tags="minimal rhel9"
# Wed, 23 Oct 2024 15:41:32 GMT
ENV container oci
# Wed, 23 Oct 2024 15:41:32 GMT
COPY dir:15154cbbad0a9e611ddbf1b6b01214f2adf2a74178d5cedb5367eaa0b5389b14 in / 
# Wed, 23 Oct 2024 15:41:32 GMT
COPY file:b37d593713ee21ad52a4cd1424dc019a24f7966f85df0ac4b86d234302695328 in /etc/yum.repos.d/. 
# Wed, 23 Oct 2024 15:41:32 GMT
CMD ["/bin/bash"]
# Wed, 23 Oct 2024 15:41:32 GMT
RUN . /cachi2/cachi2.env &&     rm -rf /var/log/*
# Wed, 23 Oct 2024 15:41:32 GMT
LABEL "build-date"="2024-12-09T18:21:24" "architecture"="s390x" "vcs-type"="git" "vcs-ref"="fee5a8f3e74ac2340dca04210f5456952058c9f4" "build-date"="2024-12-09T18:11:07Z" "release"="1733767867"
# Wed, 23 Oct 2024 15:41:32 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 23 Oct 2024 15:41:32 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 23 Oct 2024 15:41:32 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 23 Oct 2024 15:41:32 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         fontconfig         glibc-langpack-en     ;     microdnf clean all # buildkit
# Wed, 23 Oct 2024 15:41:32 GMT
ENV JAVA_VERSION=jdk-23.0.1+11
# Wed, 23 Oct 2024 15:41:32 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='808e3843293e50515bf02ad2f956e543da65e32dac82ae7a266a147b3485c61a';          BINARY_URL='https://github.com/adoptium/temurin23-binaries/releases/download/jdk-23.0.1%2B11/OpenJDK23U-jdk_aarch64_linux_hotspot_23.0.1_11.tar.gz';          ;;        ppc64le)          ESUM='1885ab141fe7b8ed6beb77b814b1c1c99fd54713399bf917edb6a4020545adde';          BINARY_URL='https://github.com/adoptium/temurin23-binaries/releases/download/jdk-23.0.1%2B11/OpenJDK23U-jdk_ppc64le_linux_hotspot_23.0.1_11.tar.gz';          ;;        s390x)          ESUM='39419d72082faea6d2501223f1cbf6a9128bc23000adfb7b7ee7acfce422509c';          BINARY_URL='https://github.com/adoptium/temurin23-binaries/releases/download/jdk-23.0.1%2B11/OpenJDK23U-jdk_s390x_linux_hotspot_23.0.1_11.tar.gz';          ;;        x86_64)          ESUM='2400267e4e9c0f6ae880a4d763af6caf18c673714bdee5debf8388b0b5d52886';          BINARY_URL='https://github.com/adoptium/temurin23-binaries/releases/download/jdk-23.0.1%2B11/OpenJDK23U-jdk_x64_linux_hotspot_23.0.1_11.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -r "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Wed, 23 Oct 2024 15:41:32 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 23 Oct 2024 15:41:32 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 23 Oct 2024 15:41:32 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 23 Oct 2024 15:41:32 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:c873dceccca34a12f0eeb07ee9f08b5f6d1b85ede7ba35ee463559c087165bd1`  
		Last Modified: Tue, 10 Dec 2024 00:14:47 GMT  
		Size: 37.5 MB (37525749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc4161066a865cc801d97152a714a8b78c8f912b9b19a84ce892bc7a3d927843`  
		Last Modified: Wed, 11 Dec 2024 20:31:48 GMT  
		Size: 37.0 MB (37006859 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37274bc1da9882996d08950363e21dcfdfa2b4845bb444e518cd46ea696b8b4f`  
		Last Modified: Wed, 11 Dec 2024 20:37:29 GMT  
		Size: 154.4 MB (154411863 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44f51560d2a0c24abe5d7f2497c71aa836ba10467b2142c3d05e6d22b2e80afd`  
		Last Modified: Wed, 11 Dec 2024 20:37:27 GMT  
		Size: 130.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b60f450b1851f2cd46260bb04bebb5eb693d9a038f7d72b67d52f1a16f729476`  
		Last Modified: Wed, 11 Dec 2024 20:37:27 GMT  
		Size: 2.3 KB (2290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:23-jdk-ubi9-minimal` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:d974f9978347a45c74d1caefb35a032f38c3f04b8e74d9e93d63acd2089fb715
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3687564 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4af985d6ac443e6a686d61dbfa12295499ad8b0dffa26b5fadc8c7070a579fd9`

```dockerfile
```

-	Layers:
	-	`sha256:4c7c3333a0aa1f400a785f658bbeb71bc602e7d47273cba810e5a5d43cd0b675`  
		Last Modified: Wed, 11 Dec 2024 20:37:27 GMT  
		Size: 3.7 MB (3666620 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:23f2b5b5831f1b66e39f124988a7a3d491c39b1cc965deac32937f1525579c39`  
		Last Modified: Wed, 11 Dec 2024 20:37:27 GMT  
		Size: 20.9 KB (20944 bytes)  
		MIME: application/vnd.in-toto+json
