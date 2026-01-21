## `eclipse-temurin:17-jdk-ubi10-minimal`

```console
$ docker pull eclipse-temurin@sha256:32da388ebadd9e625f5d4190cd36f52b3ef5ac84f31b4c7b43ebf51d84683d3e
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

### `eclipse-temurin:17-jdk-ubi10-minimal` - linux; amd64

```console
$ docker pull eclipse-temurin@sha256:31ede3809fff110d2d81a97fa4cb6903e0fbdc6c908db21bf07a2275e83ec540
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **234.7 MB (234712466 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:76ff38790a7e10d872f35122d932db780f239f0a73f9d3fa53052a92c1f74110`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 18 Dec 2025 04:59:16 GMT
LABEL maintainer="Red Hat, Inc."
# Thu, 18 Dec 2025 04:59:16 GMT
LABEL vendor="Red Hat, Inc."
# Thu, 18 Dec 2025 04:59:16 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Thu, 18 Dec 2025 04:59:16 GMT
LABEL com.redhat.component="ubi10-minimal-container"       name="ubi10/ubi-minimal"       version="10.1"       cpe="cpe:/o:redhat:enterprise_linux:10.1"       distribution-scope="public"
# Thu, 18 Dec 2025 04:59:16 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Thu, 18 Dec 2025 04:59:16 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 10."
# Thu, 18 Dec 2025 04:59:16 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 18 Dec 2025 04:59:16 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 18 Dec 2025 04:59:16 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 10 Minimal"
# Thu, 18 Dec 2025 04:59:16 GMT
LABEL io.openshift.expose-services=""
# Thu, 18 Dec 2025 04:59:16 GMT
LABEL io.openshift.tags="minimal rhel10"
# Thu, 18 Dec 2025 04:59:16 GMT
ENV container oci
# Thu, 18 Dec 2025 04:59:17 GMT
COPY dir:fdc8c39dddd7104eb139c404c8e963d7763f4f2dba800adb3cb1affa751115f3 in /      
# Thu, 18 Dec 2025 04:59:17 GMT
COPY file:5de33b5fc08b00635bccf9134a18978dba13e2250aa51838f9969515a3957847 in /etc/yum.repos.d/.      
# Thu, 18 Dec 2025 04:59:17 GMT
CMD ["/bin/bash"]
# Thu, 18 Dec 2025 04:59:17 GMT
COPY file:595171150af68abc798ea385f7988d74b566aa8e84babff137f00b08b2164683 in /usr/share/buildinfo/content-sets.json      
# Thu, 18 Dec 2025 04:59:17 GMT
COPY file:595171150af68abc798ea385f7988d74b566aa8e84babff137f00b08b2164683 in /root/buildinfo/content_manifests/content-sets.json      
# Thu, 18 Dec 2025 04:59:17 GMT
COPY file:7bed867b68b82c11d96a326acbe92a53eeb4b701a4a63e4b069dab774da39ed9 in /usr/share/buildinfo/labels.json      
# Thu, 18 Dec 2025 04:59:17 GMT
COPY file:7bed867b68b82c11d96a326acbe92a53eeb4b701a4a63e4b069dab774da39ed9 in /root/buildinfo/labels.json      
# Thu, 18 Dec 2025 04:59:17 GMT
LABEL "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="3dbd4aac2bce2ca6b13274bf0662e947c80b18b9" "org.opencontainers.image.revision"="3dbd4aac2bce2ca6b13274bf0662e947c80b18b9" "build-date"="2025-12-18T04:58:54Z" "org.opencontainers.image.created"="2025-12-18T04:58:54Z" "release"="1766033715"org.opencontainers.image.revision=3dbd4aac2bce2ca6b13274bf0662e947c80b18b9,org.opencontainers.image.created=2025-12-18T04:58:54Z
# Thu, 18 Dec 2025 22:23:40 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 18 Dec 2025 22:23:40 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 18 Dec 2025 22:23:40 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 18 Dec 2025 22:23:40 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en         gnupg2     ;     microdnf clean all # buildkit
# Thu, 18 Dec 2025 22:23:40 GMT
ENV JAVA_VERSION=jdk-17.0.17+10
# Thu, 18 Dec 2025 22:23:46 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='dc29ca6d35beb4419b4b00419b8a3dfbf5ae551e1ae2b046b516d9a579d04533';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jdk_aarch64_linux_hotspot_17.0.17_10.tar.gz';          ;;        ppc64le)          ESUM='2a29d1be61940c1bd639018c07f4622e1f145a7ef34e7294fee877e39226d9da';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jdk_ppc64le_linux_hotspot_17.0.17_10.tar.gz';          ;;        s390x)          ESUM='76327b1d00c67f6be91717754fd85fc85ce496d48876f69accb9c53ed31dc546';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jdk_s390x_linux_hotspot_17.0.17_10.tar.gz';          ;;        x86_64)          ESUM='992f96e7995075ac7636bb1a8de52b0c61d71ed3137fafc979ab96b4ab78dd75';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jdk_x64_linux_hotspot_17.0.17_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Thu, 18 Dec 2025 22:23:47 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 18 Dec 2025 22:23:47 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 18 Dec 2025 22:23:47 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 18 Dec 2025 22:23:47 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:bbf656ece02bf42bcb72be26aaced8f9084f91250ae2336e1f2b7b9e8b979727`  
		Last Modified: Thu, 18 Dec 2025 11:19:29 GMT  
		Size: 34.5 MB (34531778 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff3edaec2a8085b53169aad00e500cf23a536467b74e25d584ed4acb2e687224`  
		Last Modified: Thu, 18 Dec 2025 22:24:22 GMT  
		Size: 55.3 MB (55325379 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1eb60cfd75dd4fc77f99cf2a8b6d3f6f8096a4ad985f32c7f9ca790ae3338e0`  
		Last Modified: Thu, 18 Dec 2025 22:24:11 GMT  
		Size: 144.9 MB (144852890 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89ea47bf79f4686431f239f9867a8d5d46f991862612adc2bb48503fd471419e`  
		Last Modified: Thu, 18 Dec 2025 22:24:16 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0200b26b13e4ec50e65be104cd1ea9b5bf7714b3371732961563cc3c461267c6`  
		Last Modified: Thu, 18 Dec 2025 22:24:06 GMT  
		Size: 2.3 KB (2291 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:17-jdk-ubi10-minimal` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:30f8d6b3191e787ad85bceaa42332a5c8c80be999c8445304c454d677d166b02
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5701869 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a7b88acf1f397a0baf9bdda518f5c8b540b7ba217a7402a25e37629b945f9f21`

```dockerfile
```

-	Layers:
	-	`sha256:7e4a7156390b08b4c7e4c69fd25ccacbc9a4337f9d2e5c9a79ef2e96c1fa66f4`  
		Last Modified: Thu, 18 Dec 2025 22:24:06 GMT  
		Size: 5.7 MB (5680530 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2ac12aed51456b2f3c7ff0a8790a7a692ab57414f7c4292b7771d826e9163b89`  
		Last Modified: Thu, 18 Dec 2025 22:24:06 GMT  
		Size: 21.3 KB (21339 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-temurin:17-jdk-ubi10-minimal` - linux; arm64 variant v8

```console
$ docker pull eclipse-temurin@sha256:5beead0efe79e4f02b59ec4cf9a22b768b903cc91e0c27b89bf4e09804633adf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **231.4 MB (231440194 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1804ccaa67bc4a4ac1f4927a6824f13117177d24457bac3f7c0f8230eb71d257`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 18 Dec 2025 05:04:19 GMT
LABEL maintainer="Red Hat, Inc."
# Thu, 18 Dec 2025 05:04:19 GMT
LABEL vendor="Red Hat, Inc."
# Thu, 18 Dec 2025 05:04:19 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Thu, 18 Dec 2025 05:04:19 GMT
LABEL com.redhat.component="ubi10-minimal-container"       name="ubi10/ubi-minimal"       version="10.1"       cpe="cpe:/o:redhat:enterprise_linux:10.1"       distribution-scope="public"
# Thu, 18 Dec 2025 05:04:19 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Thu, 18 Dec 2025 05:04:19 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 10."
# Thu, 18 Dec 2025 05:04:19 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 18 Dec 2025 05:04:19 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 18 Dec 2025 05:04:19 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 10 Minimal"
# Thu, 18 Dec 2025 05:04:19 GMT
LABEL io.openshift.expose-services=""
# Thu, 18 Dec 2025 05:04:19 GMT
LABEL io.openshift.tags="minimal rhel10"
# Thu, 18 Dec 2025 05:04:19 GMT
ENV container oci
# Thu, 18 Dec 2025 05:04:20 GMT
COPY dir:04b750083472751a7f5154bb88e2ce4d0526c13f7486508dfd32af911f2d6c12 in /      
# Thu, 18 Dec 2025 05:04:20 GMT
COPY file:5de33b5fc08b00635bccf9134a18978dba13e2250aa51838f9969515a3957847 in /etc/yum.repos.d/.      
# Thu, 18 Dec 2025 05:04:20 GMT
CMD ["/bin/bash"]
# Thu, 18 Dec 2025 05:04:20 GMT
COPY file:595171150af68abc798ea385f7988d74b566aa8e84babff137f00b08b2164683 in /usr/share/buildinfo/content-sets.json      
# Thu, 18 Dec 2025 05:04:20 GMT
COPY file:595171150af68abc798ea385f7988d74b566aa8e84babff137f00b08b2164683 in /root/buildinfo/content_manifests/content-sets.json      
# Thu, 18 Dec 2025 05:04:20 GMT
COPY file:3a827beb44c0bded02518913eace1a58024dbf0ce6482c0f23a932e3e59b2536 in /usr/share/buildinfo/labels.json      
# Thu, 18 Dec 2025 05:04:20 GMT
COPY file:3a827beb44c0bded02518913eace1a58024dbf0ce6482c0f23a932e3e59b2536 in /root/buildinfo/labels.json      
# Thu, 18 Dec 2025 05:04:20 GMT
LABEL "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="3dbd4aac2bce2ca6b13274bf0662e947c80b18b9" "org.opencontainers.image.revision"="3dbd4aac2bce2ca6b13274bf0662e947c80b18b9" "build-date"="2025-12-18T05:03:56Z" "org.opencontainers.image.created"="2025-12-18T05:03:56Z" "release"="1766033715"org.opencontainers.image.revision=3dbd4aac2bce2ca6b13274bf0662e947c80b18b9,org.opencontainers.image.created=2025-12-18T05:03:56Z
# Thu, 18 Dec 2025 22:30:35 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 18 Dec 2025 22:30:35 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 18 Dec 2025 22:30:35 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 18 Dec 2025 22:30:35 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en         gnupg2     ;     microdnf clean all # buildkit
# Thu, 18 Dec 2025 22:30:35 GMT
ENV JAVA_VERSION=jdk-17.0.17+10
# Thu, 18 Dec 2025 22:30:41 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='dc29ca6d35beb4419b4b00419b8a3dfbf5ae551e1ae2b046b516d9a579d04533';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jdk_aarch64_linux_hotspot_17.0.17_10.tar.gz';          ;;        ppc64le)          ESUM='2a29d1be61940c1bd639018c07f4622e1f145a7ef34e7294fee877e39226d9da';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jdk_ppc64le_linux_hotspot_17.0.17_10.tar.gz';          ;;        s390x)          ESUM='76327b1d00c67f6be91717754fd85fc85ce496d48876f69accb9c53ed31dc546';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jdk_s390x_linux_hotspot_17.0.17_10.tar.gz';          ;;        x86_64)          ESUM='992f96e7995075ac7636bb1a8de52b0c61d71ed3137fafc979ab96b4ab78dd75';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jdk_x64_linux_hotspot_17.0.17_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Thu, 18 Dec 2025 22:30:43 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 18 Dec 2025 22:30:43 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 18 Dec 2025 22:30:43 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 18 Dec 2025 22:30:43 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:f416e7c13e96a1bec342af3e79184aaf45de55dd66939245eb76ca02465c54c7`  
		Last Modified: Thu, 18 Dec 2025 12:14:26 GMT  
		Size: 32.6 MB (32633678 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e61b0adcf4dfc94959f8c24835e9abdd7725d04bbce687fb4a2960fd5a01bd0`  
		Last Modified: Thu, 18 Dec 2025 22:31:21 GMT  
		Size: 55.1 MB (55118684 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84d58fedeb1b3cb3b0d1cec92ce6450469c5d2a526b057e593368f225cafe59c`  
		Last Modified: Thu, 18 Dec 2025 22:31:31 GMT  
		Size: 143.7 MB (143685415 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b62062e9551742241b8c9963a44cf30627e1b3d3704e27f766fbd370a0765d15`  
		Last Modified: Thu, 18 Dec 2025 22:31:10 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4da885a238dc54e31835a16697bbe5f703e3318bcc4f3517fcbc7005d4537b3`  
		Last Modified: Thu, 18 Dec 2025 22:31:10 GMT  
		Size: 2.3 KB (2288 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:17-jdk-ubi10-minimal` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:f7582662331348fb5188d9cacc2719475a35b9817d042f27d125c57b0827a800
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5701476 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c09012294d7b5c3b7086db5575c67afe3c317414e453ab3bb1c09bbd66bcfd2d`

```dockerfile
```

-	Layers:
	-	`sha256:deaefb7f00625deed9bc084b9697d0145b117e9212d908b6b368ab0de0c9b7ee`  
		Last Modified: Fri, 19 Dec 2025 00:24:02 GMT  
		Size: 5.7 MB (5680020 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f0872c70b6191fdfc81c135b60d3fadbe15375ade0417fa1a52e0252361c333b`  
		Last Modified: Fri, 19 Dec 2025 00:24:03 GMT  
		Size: 21.5 KB (21456 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-temurin:17-jdk-ubi10-minimal` - linux; ppc64le

```console
$ docker pull eclipse-temurin@sha256:58a2f5700d063904c98d4b3981dc0e149dca48f75297f08ea2e81d7f0360181c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **240.6 MB (240582048 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:293d774e2b0a34da0e358f535f3705cc31d476ef72e0c81da3e03c6df06a4a89`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 18 Dec 2025 07:03:44 GMT
LABEL maintainer="Red Hat, Inc."
# Thu, 18 Dec 2025 07:03:44 GMT
LABEL vendor="Red Hat, Inc."
# Thu, 18 Dec 2025 07:03:44 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Thu, 18 Dec 2025 07:03:44 GMT
LABEL com.redhat.component="ubi10-minimal-container"       name="ubi10/ubi-minimal"       version="10.1"       cpe="cpe:/o:redhat:enterprise_linux:10.1"       distribution-scope="public"
# Thu, 18 Dec 2025 07:03:44 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Thu, 18 Dec 2025 07:03:44 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 10."
# Thu, 18 Dec 2025 07:03:44 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 18 Dec 2025 07:03:44 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 18 Dec 2025 07:03:44 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 10 Minimal"
# Thu, 18 Dec 2025 07:03:44 GMT
LABEL io.openshift.expose-services=""
# Thu, 18 Dec 2025 07:03:44 GMT
LABEL io.openshift.tags="minimal rhel10"
# Thu, 18 Dec 2025 07:03:44 GMT
ENV container oci
# Thu, 18 Dec 2025 07:03:45 GMT
COPY dir:530980282317924eec1c6623b725ebfc8622f7b70907079d2b485327f826b92a in /      
# Thu, 18 Dec 2025 07:03:45 GMT
COPY file:5de33b5fc08b00635bccf9134a18978dba13e2250aa51838f9969515a3957847 in /etc/yum.repos.d/.      
# Thu, 18 Dec 2025 07:03:45 GMT
CMD ["/bin/bash"]
# Thu, 18 Dec 2025 07:03:45 GMT
COPY file:595171150af68abc798ea385f7988d74b566aa8e84babff137f00b08b2164683 in /usr/share/buildinfo/content-sets.json      
# Thu, 18 Dec 2025 07:03:45 GMT
COPY file:595171150af68abc798ea385f7988d74b566aa8e84babff137f00b08b2164683 in /root/buildinfo/content_manifests/content-sets.json      
# Thu, 18 Dec 2025 07:03:45 GMT
COPY file:c62fb4530a421926bb6d3aa12f09ef125c8c4fff4293e7e931975ad4241f6f26 in /usr/share/buildinfo/labels.json      
# Thu, 18 Dec 2025 07:03:45 GMT
COPY file:c62fb4530a421926bb6d3aa12f09ef125c8c4fff4293e7e931975ad4241f6f26 in /root/buildinfo/labels.json      
# Thu, 18 Dec 2025 07:03:46 GMT
LABEL "architecture"="ppc64le" "vcs-type"="git" "vcs-ref"="3dbd4aac2bce2ca6b13274bf0662e947c80b18b9" "org.opencontainers.image.revision"="3dbd4aac2bce2ca6b13274bf0662e947c80b18b9" "build-date"="2025-12-18T07:03:33Z" "org.opencontainers.image.created"="2025-12-18T07:03:33Z" "release"="1766033715"org.opencontainers.image.revision=3dbd4aac2bce2ca6b13274bf0662e947c80b18b9,org.opencontainers.image.created=2025-12-18T07:03:33Z
# Thu, 18 Dec 2025 22:39:15 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 18 Dec 2025 22:39:15 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 18 Dec 2025 22:39:15 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 18 Dec 2025 22:39:15 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en         gnupg2     ;     microdnf clean all # buildkit
# Thu, 18 Dec 2025 22:39:15 GMT
ENV JAVA_VERSION=jdk-17.0.17+10
# Thu, 18 Dec 2025 22:41:29 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='dc29ca6d35beb4419b4b00419b8a3dfbf5ae551e1ae2b046b516d9a579d04533';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jdk_aarch64_linux_hotspot_17.0.17_10.tar.gz';          ;;        ppc64le)          ESUM='2a29d1be61940c1bd639018c07f4622e1f145a7ef34e7294fee877e39226d9da';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jdk_ppc64le_linux_hotspot_17.0.17_10.tar.gz';          ;;        s390x)          ESUM='76327b1d00c67f6be91717754fd85fc85ce496d48876f69accb9c53ed31dc546';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jdk_s390x_linux_hotspot_17.0.17_10.tar.gz';          ;;        x86_64)          ESUM='992f96e7995075ac7636bb1a8de52b0c61d71ed3137fafc979ab96b4ab78dd75';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jdk_x64_linux_hotspot_17.0.17_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Thu, 18 Dec 2025 22:41:31 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 18 Dec 2025 22:41:32 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 18 Dec 2025 22:41:32 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 18 Dec 2025 22:41:32 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:97de3b33554c63d2e40af1481c1da99bde18eb30eff5e4d230d8ec855811f50c`  
		Last Modified: Thu, 18 Dec 2025 12:14:46 GMT  
		Size: 38.7 MB (38688551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4559e7867acf4f05baf702a54db8a3e2cc5bd1a16c2dcecfa940d5c1ad1b6dfd`  
		Last Modified: Thu, 18 Dec 2025 22:40:19 GMT  
		Size: 57.3 MB (57343233 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a85df18c6dbb78b5ab81911a4f2b8dcbecb7644cb147e1d39f6db9e9e6c7274`  
		Last Modified: Thu, 18 Dec 2025 22:42:16 GMT  
		Size: 144.5 MB (144547846 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd608fb95264e7759f937cd7eb538270370998d72adfe9dc8fb3f82635c94028`  
		Last Modified: Thu, 18 Dec 2025 22:42:22 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abd3d371d3c17a3035a31a196fc0cf23d5214c4eb85bd00f1e8e2925725ba49e`  
		Last Modified: Thu, 18 Dec 2025 22:41:58 GMT  
		Size: 2.3 KB (2289 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:17-jdk-ubi10-minimal` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:b4c3b84e90929e548838e4691e8f40a4c21bbe5500ec625dbb1471383a228b81
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5689058 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a5a4fdf57c5547c5e295327acc64f21263ed61c8791afa2dcbfb01b518f5bfd5`

```dockerfile
```

-	Layers:
	-	`sha256:b5771f15418802a001cb62f0ad502b7caec77e8c72eff0595ebb0963a00eaa33`  
		Last Modified: Fri, 19 Dec 2025 01:14:22 GMT  
		Size: 5.7 MB (5667682 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4107a7a931c8fa6d13fdb5be21cd596e19f6e07fc1b8d257aea39c41bdb96d47`  
		Last Modified: Fri, 19 Dec 2025 01:14:23 GMT  
		Size: 21.4 KB (21376 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-temurin:17-jdk-ubi10-minimal` - linux; s390x

```console
$ docker pull eclipse-temurin@sha256:0a93a92dbb7982ddd6b7767ca31a4c08bc18bb1bbd4e54aadc3c2c2d5fa68a9a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **225.1 MB (225125872 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:76ad244a4c86e108ea1e21a4b6c107701bf93141d83a6d772df389f683c62e62`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 18 Dec 2025 07:10:02 GMT
LABEL maintainer="Red Hat, Inc."
# Thu, 18 Dec 2025 07:10:02 GMT
LABEL vendor="Red Hat, Inc."
# Thu, 18 Dec 2025 07:10:02 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Thu, 18 Dec 2025 07:10:02 GMT
LABEL com.redhat.component="ubi10-minimal-container"       name="ubi10/ubi-minimal"       version="10.1"       cpe="cpe:/o:redhat:enterprise_linux:10.1"       distribution-scope="public"
# Thu, 18 Dec 2025 07:10:02 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Thu, 18 Dec 2025 07:10:02 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 10."
# Thu, 18 Dec 2025 07:10:02 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 18 Dec 2025 07:10:02 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 18 Dec 2025 07:10:02 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 10 Minimal"
# Thu, 18 Dec 2025 07:10:02 GMT
LABEL io.openshift.expose-services=""
# Thu, 18 Dec 2025 07:10:03 GMT
LABEL io.openshift.tags="minimal rhel10"
# Thu, 18 Dec 2025 07:10:03 GMT
ENV container oci
# Thu, 18 Dec 2025 07:10:03 GMT
COPY dir:7d54469de7c29eaa832f7e98c75ae08842b7fae9314e66ea7e9e482c3966eeca in /      
# Thu, 18 Dec 2025 07:10:03 GMT
COPY file:5de33b5fc08b00635bccf9134a18978dba13e2250aa51838f9969515a3957847 in /etc/yum.repos.d/.      
# Thu, 18 Dec 2025 07:10:03 GMT
CMD ["/bin/bash"]
# Thu, 18 Dec 2025 07:10:03 GMT
COPY file:595171150af68abc798ea385f7988d74b566aa8e84babff137f00b08b2164683 in /usr/share/buildinfo/content-sets.json      
# Thu, 18 Dec 2025 07:10:03 GMT
COPY file:595171150af68abc798ea385f7988d74b566aa8e84babff137f00b08b2164683 in /root/buildinfo/content_manifests/content-sets.json      
# Thu, 18 Dec 2025 07:10:03 GMT
COPY file:bea094e4f4ee0e91f623d002425004416b4556dc8f71bf399fffb85c16bafec5 in /usr/share/buildinfo/labels.json      
# Thu, 18 Dec 2025 07:10:03 GMT
COPY file:bea094e4f4ee0e91f623d002425004416b4556dc8f71bf399fffb85c16bafec5 in /root/buildinfo/labels.json      
# Thu, 18 Dec 2025 07:10:03 GMT
LABEL "architecture"="s390x" "vcs-type"="git" "vcs-ref"="3dbd4aac2bce2ca6b13274bf0662e947c80b18b9" "org.opencontainers.image.revision"="3dbd4aac2bce2ca6b13274bf0662e947c80b18b9" "build-date"="2025-12-18T07:07:43Z" "org.opencontainers.image.created"="2025-12-18T07:07:43Z" "release"="1766033715"org.opencontainers.image.revision=3dbd4aac2bce2ca6b13274bf0662e947c80b18b9,org.opencontainers.image.created=2025-12-18T07:07:43Z
# Thu, 18 Dec 2025 22:41:25 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 18 Dec 2025 22:41:25 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 18 Dec 2025 22:41:25 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 18 Dec 2025 22:41:25 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en         gnupg2     ;     microdnf clean all # buildkit
# Thu, 18 Dec 2025 22:41:25 GMT
ENV JAVA_VERSION=jdk-17.0.17+10
# Thu, 18 Dec 2025 22:41:31 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='dc29ca6d35beb4419b4b00419b8a3dfbf5ae551e1ae2b046b516d9a579d04533';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jdk_aarch64_linux_hotspot_17.0.17_10.tar.gz';          ;;        ppc64le)          ESUM='2a29d1be61940c1bd639018c07f4622e1f145a7ef34e7294fee877e39226d9da';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jdk_ppc64le_linux_hotspot_17.0.17_10.tar.gz';          ;;        s390x)          ESUM='76327b1d00c67f6be91717754fd85fc85ce496d48876f69accb9c53ed31dc546';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jdk_s390x_linux_hotspot_17.0.17_10.tar.gz';          ;;        x86_64)          ESUM='992f96e7995075ac7636bb1a8de52b0c61d71ed3137fafc979ab96b4ab78dd75';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jdk_x64_linux_hotspot_17.0.17_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Thu, 18 Dec 2025 22:41:32 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 18 Dec 2025 22:41:32 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 18 Dec 2025 22:41:32 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 18 Dec 2025 22:41:32 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:27a76ad55c4b879c1269027dfeec6783f235d82059544eeb7c62ecb7ad66011a`  
		Last Modified: Thu, 18 Dec 2025 12:14:48 GMT  
		Size: 34.3 MB (34340329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df1d3cf471e26ffcdb87047fde314dc15dda443a859121fd8a7f0a4295aa2e08`  
		Last Modified: Thu, 18 Dec 2025 22:42:01 GMT  
		Size: 55.9 MB (55920917 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29262ed9bc3b2acd928fbd26876ee259cdc8bac4893636200d240fafd5e748ed`  
		Last Modified: Fri, 19 Dec 2025 01:53:03 GMT  
		Size: 134.9 MB (134862207 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:807da3ed1e940fab0a5dc01fa92c97f7390e490de3e473bc3ef56ded78956e39`  
		Last Modified: Thu, 18 Dec 2025 22:42:04 GMT  
		Size: 130.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abd3d371d3c17a3035a31a196fc0cf23d5214c4eb85bd00f1e8e2925725ba49e`  
		Last Modified: Thu, 18 Dec 2025 22:41:58 GMT  
		Size: 2.3 KB (2289 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:17-jdk-ubi10-minimal` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:0ffa2a941456153634f2c742af1115e58c5bc15bdc19fc29819a54bffd01f35b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5687396 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1aaa124e21ac77ebe245cd39e3a08458d30f71bf2be48071584d979760bee46b`

```dockerfile
```

-	Layers:
	-	`sha256:02960724c8cf20b3929dce83a92572cede77438980086ade9b10ba82029bc61d`  
		Last Modified: Thu, 18 Dec 2025 22:41:58 GMT  
		Size: 5.7 MB (5666056 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3f78e0d1f85437ffa2fd204f703f3aa56bb187aa38482a6ff422a2ff43aa87c1`  
		Last Modified: Thu, 18 Dec 2025 22:41:57 GMT  
		Size: 21.3 KB (21340 bytes)  
		MIME: application/vnd.in-toto+json
