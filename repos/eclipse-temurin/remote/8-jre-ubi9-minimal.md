## `eclipse-temurin:8-jre-ubi9-minimal`

```console
$ docker pull eclipse-temurin@sha256:8319c592c00d4ee89fc54636e153547436716480d0ce2840d9e14ccddab68fed
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
$ docker pull eclipse-temurin@sha256:b7bbf64c441d92aa00ff20f0ac991ca3bcf00a27078e84bfdf0753900b60c60c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **118.2 MB (118238325 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a8233338172f08342ba48c55699f7ae7c04ff1aa3b94fff470969ae28c21a6c`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`

```dockerfile
# Thu, 30 Jan 2025 14:32:57 GMT
LABEL maintainer="Red Hat, Inc."
# Thu, 30 Jan 2025 14:32:57 GMT
LABEL vendor="Red Hat, Inc."
# Thu, 30 Jan 2025 14:32:57 GMT
LABEL url="https://www.redhat.com"
# Thu, 30 Jan 2025 14:32:57 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.5"       distribution-scope="public"
# Thu, 30 Jan 2025 14:32:57 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Thu, 30 Jan 2025 14:32:57 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Thu, 30 Jan 2025 14:32:57 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 30 Jan 2025 14:32:57 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 30 Jan 2025 14:32:57 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Thu, 30 Jan 2025 14:32:57 GMT
LABEL io.openshift.expose-services=""
# Thu, 30 Jan 2025 14:32:57 GMT
LABEL io.openshift.tags="minimal rhel9"
# Thu, 30 Jan 2025 14:32:57 GMT
ENV container oci
# Thu, 30 Jan 2025 14:32:57 GMT
COPY dir:fc29285925cd626d62a818aff5b79af4bb61fc4890fdd703305a9455e4e11f19 in / 
# Thu, 30 Jan 2025 14:32:57 GMT
COPY file:b37d593713ee21ad52a4cd1424dc019a24f7966f85df0ac4b86d234302695328 in /etc/yum.repos.d/. 
# Thu, 30 Jan 2025 14:32:57 GMT
CMD ["/bin/bash"]
# Thu, 30 Jan 2025 14:32:57 GMT
RUN . /cachi2/cachi2.env &&     rm -rf /var/log/*
# Thu, 30 Jan 2025 14:32:57 GMT
LABEL "build-date"="2025-02-06T04:43:42" "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="adfffabe9acacc27d15fc0ceb8e083254ca7b450" "build-date"="2025-02-06T04:39:35Z" "release"="1738816775"
# Thu, 30 Jan 2025 14:32:57 GMT
RUN /bin/sh
# Thu, 30 Jan 2025 14:32:57 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 30 Jan 2025 14:32:57 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 30 Jan 2025 14:32:57 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 30 Jan 2025 14:32:57 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         fontconfig         glibc-langpack-en     ;     microdnf clean all # buildkit
# Thu, 30 Jan 2025 14:32:57 GMT
ENV JAVA_VERSION=jdk8u442-b06
# Thu, 30 Jan 2025 14:32:57 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='730ed649ee973b7408cf7107e90576b67e8ed4b3aebb9e3e8a1056151f373152';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u442-b06/OpenJDK8U-jre_aarch64_linux_hotspot_8u442b06.tar.gz';          ;;        ppc64le)          ESUM='812ebf110f1d1cfc26a135368850064f96689e7918aa6bbac1c8f210fad5752f';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u442-b06/OpenJDK8U-jre_ppc64le_linux_hotspot_8u442b06.tar.gz';          ;;        x86_64)          ESUM='730fe33b1fc1f7da1e325d007b475d25a063850a167b548ea4bf689d4fcd867d';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u442-b06/OpenJDK8U-jre_x64_linux_hotspot_8u442b06.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz; # buildkit
# Thu, 30 Jan 2025 14:32:57 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java -version"; java -version;     echo "Complete." # buildkit
# Thu, 30 Jan 2025 14:32:57 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 30 Jan 2025 14:32:57 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
```

-	Layers:
	-	`sha256:667deb3fcbde45825554b378b8e593f6c3c4a339133a1a80c4d2e1594ff96723`  
		Last Modified: Thu, 06 Feb 2025 05:39:44 GMT  
		Size: 39.4 MB (39370269 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8339c472296e0e9bde11d7c0a4c8b8c7060108aa1aa729ab95b5275b1fa7163`  
		Last Modified: Thu, 06 Feb 2025 05:39:42 GMT  
		Size: 462.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea95d18298f0acb1568846a72ac33509ce34484ba7d95e5d7c7fdc601a7c1ce8`  
		Last Modified: Fri, 07 Feb 2025 04:44:11 GMT  
		Size: 37.0 MB (36988895 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:468e383b7f8196eb04d9a842710cffdafc16c66d4247fe250b871d6757a94199`  
		Last Modified: Fri, 07 Feb 2025 04:44:12 GMT  
		Size: 41.9 MB (41876283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2141891a728a118a95d63bdbddaf434dde76618ffcf473ae462e57207c94e228`  
		Last Modified: Fri, 07 Feb 2025 08:53:14 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68de3aee70e263303e9b7c389194ca2327bbb19211e8b78866ed926d268c591a`  
		Last Modified: Fri, 07 Feb 2025 04:44:10 GMT  
		Size: 2.3 KB (2290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:8-jre-ubi9-minimal` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:dbc5acbeb12a4aaad7ab32257e3e27a388bc65bd021478725d5593b60853b969
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3632354 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:012604de599089a2b1da909ba75ffc35d97fb5888aad08da94b1cf4f5d85ca3f`

```dockerfile
```

-	Layers:
	-	`sha256:96d95121d2cfec92e66bb7434225219a7b06051ca33a166a2f58a4de0d05e3d1`  
		Last Modified: Fri, 07 Feb 2025 00:30:02 GMT  
		Size: 3.6 MB (3612436 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fdf779073f051b71ec1be78d0f5640784d5f495894eb536cec6725483a5ff4be`  
		Last Modified: Fri, 07 Feb 2025 00:30:02 GMT  
		Size: 19.9 KB (19918 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-temurin:8-jre-ubi9-minimal` - linux; arm64 variant v8

```console
$ docker pull eclipse-temurin@sha256:081f35227face679a68d31c65a1fedb2362e9d687a19132ab33e5404bf700933
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.9 MB (115913176 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f3bbba02c43451df2da2c5a786f8d80dd1963af232ca5dce651bfcbf1f480b80`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`

```dockerfile
# Thu, 30 Jan 2025 14:32:57 GMT
LABEL maintainer="Red Hat, Inc."
# Thu, 30 Jan 2025 14:32:57 GMT
LABEL vendor="Red Hat, Inc."
# Thu, 30 Jan 2025 14:32:57 GMT
LABEL url="https://www.redhat.com"
# Thu, 30 Jan 2025 14:32:57 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.5"       distribution-scope="public"
# Thu, 30 Jan 2025 14:32:57 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Thu, 30 Jan 2025 14:32:57 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Thu, 30 Jan 2025 14:32:57 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 30 Jan 2025 14:32:57 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 30 Jan 2025 14:32:57 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Thu, 30 Jan 2025 14:32:57 GMT
LABEL io.openshift.expose-services=""
# Thu, 30 Jan 2025 14:32:57 GMT
LABEL io.openshift.tags="minimal rhel9"
# Thu, 30 Jan 2025 14:32:57 GMT
ENV container oci
# Thu, 30 Jan 2025 14:32:57 GMT
COPY dir:389f5f73f217a50cb052c224af980ef5943f8527170a8ed8ba3b540101351720 in / 
# Thu, 30 Jan 2025 14:32:57 GMT
COPY file:b37d593713ee21ad52a4cd1424dc019a24f7966f85df0ac4b86d234302695328 in /etc/yum.repos.d/. 
# Thu, 30 Jan 2025 14:32:57 GMT
CMD ["/bin/bash"]
# Thu, 30 Jan 2025 14:32:57 GMT
RUN . /cachi2/cachi2.env &&     rm -rf /var/log/*
# Thu, 30 Jan 2025 14:32:57 GMT
LABEL "build-date"="2025-02-06T04:48:45" "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="adfffabe9acacc27d15fc0ceb8e083254ca7b450" "build-date"="2025-02-06T04:39:35Z" "release"="1738816775"
# Thu, 30 Jan 2025 14:32:57 GMT
RUN /bin/sh
# Thu, 30 Jan 2025 14:32:57 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 30 Jan 2025 14:32:57 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 30 Jan 2025 14:32:57 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 30 Jan 2025 14:32:57 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         fontconfig         glibc-langpack-en     ;     microdnf clean all # buildkit
# Thu, 30 Jan 2025 14:32:57 GMT
ENV JAVA_VERSION=jdk8u442-b06
# Thu, 30 Jan 2025 14:32:57 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='730ed649ee973b7408cf7107e90576b67e8ed4b3aebb9e3e8a1056151f373152';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u442-b06/OpenJDK8U-jre_aarch64_linux_hotspot_8u442b06.tar.gz';          ;;        ppc64le)          ESUM='812ebf110f1d1cfc26a135368850064f96689e7918aa6bbac1c8f210fad5752f';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u442-b06/OpenJDK8U-jre_ppc64le_linux_hotspot_8u442b06.tar.gz';          ;;        x86_64)          ESUM='730fe33b1fc1f7da1e325d007b475d25a063850a167b548ea4bf689d4fcd867d';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u442-b06/OpenJDK8U-jre_x64_linux_hotspot_8u442b06.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz; # buildkit
# Thu, 30 Jan 2025 14:32:57 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java -version"; java -version;     echo "Complete." # buildkit
# Thu, 30 Jan 2025 14:32:57 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 30 Jan 2025 14:32:57 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
```

-	Layers:
	-	`sha256:8174eb1151f28d1a88085da5d27ffd5729467439a2f1a77d03498e89f9f7ef4b`  
		Last Modified: Thu, 06 Feb 2025 06:30:59 GMT  
		Size: 37.6 MB (37592304 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc6c4d65a5f9a8b0c8f76083cf10d14a2417324b530dfde1115d46147afe1c17`  
		Last Modified: Thu, 06 Feb 2025 06:26:49 GMT  
		Size: 460.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc676c7b0d497bf2463a37af5f2c36a9724601e6cd79a9e4fa127c484ad01df3`  
		Last Modified: Fri, 07 Feb 2025 04:47:29 GMT  
		Size: 37.4 MB (37441949 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83c9244bb2a6b6dd6c39e57e6f88516414b3d16894af71b22ffcffd2cd74d04e`  
		Last Modified: Fri, 07 Feb 2025 04:47:27 GMT  
		Size: 40.9 MB (40876044 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c517546c7b6301b821d466d933bcecd542c60551302ac1b7d18231fc9604d5c3`  
		Last Modified: Fri, 07 Feb 2025 14:56:35 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cab6abb3ccc0fcd080330f73d9f0371b0bc9f6e79f4a576f6d30710c2edcf29d`  
		Last Modified: Fri, 07 Feb 2025 04:47:01 GMT  
		Size: 2.3 KB (2291 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:8-jre-ubi9-minimal` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:26aa7757e4c3165f75e7f90c4814d785d65207c9ab3987af87ca43578e6dd715
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3632326 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:81b9c0566dd61811076b2d7fd88ac2a1f20ba4c16c38be4d444d51e7e8c7378f`

```dockerfile
```

-	Layers:
	-	`sha256:d75e55f46f3f74bdcdd69f54a2b24ad17931d457304b9b41c55272e0f6d33cb2`  
		Last Modified: Fri, 07 Feb 2025 02:22:55 GMT  
		Size: 3.6 MB (3612305 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b01c2140c7aa0e3482d36b1b71bce65ce7ce08cacc5676fa986a8c5ab54df3fb`  
		Last Modified: Fri, 07 Feb 2025 02:22:55 GMT  
		Size: 20.0 KB (20021 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-temurin:8-jre-ubi9-minimal` - linux; ppc64le

```console
$ docker pull eclipse-temurin@sha256:8ffe7c5894c216702ef6424afbd7c97dce0a4cdf41afb7ea3b2ba896bf938783
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.5 MB (124544856 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1cb774133d8eade4c0e660806ec82d790588f3f069df331288a2c0fef8f2ffc0`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`

```dockerfile
# Thu, 30 Jan 2025 14:32:57 GMT
LABEL maintainer="Red Hat, Inc."
# Thu, 30 Jan 2025 14:32:57 GMT
LABEL vendor="Red Hat, Inc."
# Thu, 30 Jan 2025 14:32:57 GMT
LABEL url="https://www.redhat.com"
# Thu, 30 Jan 2025 14:32:57 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.5"       distribution-scope="public"
# Thu, 30 Jan 2025 14:32:57 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Thu, 30 Jan 2025 14:32:57 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Thu, 30 Jan 2025 14:32:57 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 30 Jan 2025 14:32:57 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 30 Jan 2025 14:32:57 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Thu, 30 Jan 2025 14:32:57 GMT
LABEL io.openshift.expose-services=""
# Thu, 30 Jan 2025 14:32:57 GMT
LABEL io.openshift.tags="minimal rhel9"
# Thu, 30 Jan 2025 14:32:57 GMT
ENV container oci
# Thu, 30 Jan 2025 14:32:57 GMT
COPY dir:4b7f9a609ef7d9b773f245d53ef2354786362b2e75b9988fe7bd642ce728205f in / 
# Thu, 30 Jan 2025 14:32:57 GMT
COPY file:b37d593713ee21ad52a4cd1424dc019a24f7966f85df0ac4b86d234302695328 in /etc/yum.repos.d/. 
# Thu, 30 Jan 2025 14:32:57 GMT
CMD ["/bin/bash"]
# Thu, 30 Jan 2025 14:32:57 GMT
RUN . /cachi2/cachi2.env &&     rm -rf /var/log/*
# Thu, 30 Jan 2025 14:32:57 GMT
LABEL "build-date"="2025-02-06T04:53:22" "architecture"="ppc64le" "vcs-type"="git" "vcs-ref"="adfffabe9acacc27d15fc0ceb8e083254ca7b450" "build-date"="2025-02-06T04:39:35Z" "release"="1738816775"
# Thu, 30 Jan 2025 14:32:57 GMT
RUN /bin/sh
# Thu, 30 Jan 2025 14:32:57 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 30 Jan 2025 14:32:57 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 30 Jan 2025 14:32:57 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 30 Jan 2025 14:32:57 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         fontconfig         glibc-langpack-en     ;     microdnf clean all # buildkit
# Thu, 30 Jan 2025 14:32:57 GMT
ENV JAVA_VERSION=jdk8u442-b06
# Thu, 30 Jan 2025 14:32:57 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='730ed649ee973b7408cf7107e90576b67e8ed4b3aebb9e3e8a1056151f373152';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u442-b06/OpenJDK8U-jre_aarch64_linux_hotspot_8u442b06.tar.gz';          ;;        ppc64le)          ESUM='812ebf110f1d1cfc26a135368850064f96689e7918aa6bbac1c8f210fad5752f';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u442-b06/OpenJDK8U-jre_ppc64le_linux_hotspot_8u442b06.tar.gz';          ;;        x86_64)          ESUM='730fe33b1fc1f7da1e325d007b475d25a063850a167b548ea4bf689d4fcd867d';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u442-b06/OpenJDK8U-jre_x64_linux_hotspot_8u442b06.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz; # buildkit
# Thu, 30 Jan 2025 14:32:57 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java -version"; java -version;     echo "Complete." # buildkit
# Thu, 30 Jan 2025 14:32:57 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 30 Jan 2025 14:32:57 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
```

-	Layers:
	-	`sha256:dce4a6a210ec1ffa38c334f3d0bde7e211e699baa435083097a719864994a122`  
		Last Modified: Thu, 06 Feb 2025 07:04:21 GMT  
		Size: 43.8 MB (43811508 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9afaf9d1aa9b6d6e11a6a514269450db16106e006fbbe873e9f503b11a04ce1f`  
		Last Modified: Thu, 06 Feb 2025 07:04:22 GMT  
		Size: 460.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95584c2b6fee8cd3a7b6ddc79425576afe40f52f01efd248564da9afcd4ca985`  
		Last Modified: Fri, 07 Feb 2025 05:30:38 GMT  
		Size: 39.5 MB (39476691 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:faa9e444907d2bb931ff5513938eb1e4a92616748228f0be1ab250f708af568f`  
		Last Modified: Fri, 07 Feb 2025 01:27:08 GMT  
		Size: 41.3 MB (41253781 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4bc94488b01107aac2a218834fcb856fac6bcd595edbe3ec2f5e3037b937c608`  
		Last Modified: Fri, 07 Feb 2025 01:27:07 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b313354e577cac4f7e240f4567a64b6be3ad6cca36d2a25af157e7e1c7c233c`  
		Last Modified: Fri, 07 Feb 2025 01:27:07 GMT  
		Size: 2.3 KB (2290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:8-jre-ubi9-minimal` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:e248fdd9894c3f1134f36f240680a28c5d559d3e2bced9e4bdd59e95d9af794f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3632900 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:25144fa878713e645b5e209fe737ee55ee01d3768186366a97f6a54db00c7926`

```dockerfile
```

-	Layers:
	-	`sha256:70d9d31277e2a41c675622da1d4231fe43148704e29da8d1707fb94982da3c22`  
		Last Modified: Fri, 07 Feb 2025 01:27:07 GMT  
		Size: 3.6 MB (3612952 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:566f8067cfae13ba99b0bb621f504a59a2263aed6d2092aa5b4f40b67b108c8c`  
		Last Modified: Fri, 07 Feb 2025 01:27:07 GMT  
		Size: 19.9 KB (19948 bytes)  
		MIME: application/vnd.in-toto+json
