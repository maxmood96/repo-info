## `eclipse-temurin:8-jdk-ubi9-minimal`

```console
$ docker pull eclipse-temurin@sha256:4d15e3b8ba551912bf439692e20acaed0455b9b7db84af38c1b812cf0a003385
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `eclipse-temurin:8-jdk-ubi9-minimal` - linux; amd64

```console
$ docker pull eclipse-temurin@sha256:05332d3be3417096af2fd3277aba3ba6b0e1c3cfb330cd72bca6cd876a6483ea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **121.9 MB (121915203 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:62c471b6c3592662fe0f3814b79d62a7ccee117e5fc5b57ed58905d3fbee6a1f`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`

```dockerfile
# Sun, 27 Apr 2025 20:21:59 GMT
LABEL maintainer="Red Hat, Inc."
# Sun, 27 Apr 2025 20:21:59 GMT
LABEL vendor="Red Hat, Inc."
# Sun, 27 Apr 2025 20:21:59 GMT
LABEL url="https://www.redhat.com"
# Sun, 27 Apr 2025 20:21:59 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.6"       distribution-scope="public"
# Sun, 27 Apr 2025 20:21:59 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Sun, 27 Apr 2025 20:21:59 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Sun, 27 Apr 2025 20:21:59 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Sun, 27 Apr 2025 20:21:59 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Sun, 27 Apr 2025 20:21:59 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Sun, 27 Apr 2025 20:21:59 GMT
LABEL io.openshift.expose-services=""
# Sun, 27 Apr 2025 20:21:59 GMT
LABEL io.openshift.tags="minimal rhel9"
# Sun, 27 Apr 2025 20:21:59 GMT
ENV container oci
# Sun, 27 Apr 2025 20:21:59 GMT
COPY dir:9f1e3d7980aa1b8b007cf8dcf05575fff696655332be09ae87c8f7de7f00e923 in / 
# Sun, 27 Apr 2025 20:21:59 GMT
COPY file:b37d593713ee21ad52a4cd1424dc019a24f7966f85df0ac4b86d234302695328 in /etc/yum.repos.d/. 
# Sun, 27 Apr 2025 20:21:59 GMT
CMD ["/bin/bash"]
# Sun, 27 Apr 2025 20:21:59 GMT
COPY file:58cc94f5b3b2d60de2c77a6ed4b1797dcede502ccdb429a72e7a72d994235b3c in /usr/share/buildinfo/content-sets.json 
# Sun, 27 Apr 2025 20:21:59 GMT
LABEL "build-date"="2025-06-24T16:31:57" "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="69e50e2a07c936e700297091886db408257a857c" "release"="1750782676"
# Sun, 27 Apr 2025 20:21:59 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sun, 27 Apr 2025 20:21:59 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sun, 27 Apr 2025 20:21:59 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Sun, 27 Apr 2025 20:21:59 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en     ;     microdnf clean all # buildkit
# Sun, 27 Apr 2025 20:21:59 GMT
ENV JAVA_VERSION=jdk8u452-b09
# Sun, 27 Apr 2025 20:21:59 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='d8a1aecea0913b7a1e0d737ba6f7ea99059b3f6fd17813d4a24e8b3fc3aee278';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u452-b09/OpenJDK8U-jdk_aarch64_linux_hotspot_8u452b09.tar.gz';          ;;        ppc64le)          ESUM='ff6e0f7fad0f46fea47193b95e4187e294ba69bb9059704f5df9f2fb74125732';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u452-b09/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u452b09.tar.gz';          ;;        x86_64)          ESUM='9448308a21841960a591b47927cf2d44fdc4c0533a5f8111a4b243a6bafb5d27';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u452-b09/OpenJDK8U-jdk_x64_linux_hotspot_8u452b09.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip; # buildkit
# Sun, 27 Apr 2025 20:21:59 GMT
RUN set -eux;     echo "Verifying install ...";     echo "javac -version"; javac -version;     echo "java -version"; java -version;     echo "Complete." # buildkit
# Sun, 27 Apr 2025 20:21:59 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Sun, 27 Apr 2025 20:21:59 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
```

-	Layers:
	-	`sha256:7073092d8bcd7b6d72345cfa87d8389a33f629b3c49ff887ad3a51c6ed8dfd83`  
		Last Modified: Tue, 24 Jun 2025 18:09:29 GMT  
		Size: 39.7 MB (39650665 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11639d3ade5646ac48c61fedaf87359d092793cd58f94a0527c59b4142f2b1b6`  
		Last Modified: Wed, 25 Jun 2025 17:54:26 GMT  
		Size: 27.5 MB (27545286 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75ec5507fad877b6cb578f3fc5c776ccf18d5f75ca04eb53c098748b8a0cb25e`  
		Last Modified: Wed, 25 Jun 2025 17:54:32 GMT  
		Size: 54.7 MB (54716810 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7783baa0d2cb024b743fc875c87d2da2b7614fc6094e9927f878d7aa7dfc83f6`  
		Last Modified: Wed, 25 Jun 2025 17:54:23 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08cbcdb31940222773b2a963f1e0a889b73626f9f15649b1e1493f382cfdc9a5`  
		Last Modified: Wed, 25 Jun 2025 17:54:24 GMT  
		Size: 2.3 KB (2316 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:8-jdk-ubi9-minimal` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:42515ba776be8185eaf651e7e648003d888a253f591d7721e218c413e90eaf6d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2616348 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:83be12ee97723abcbf99bcd170cdb6d0a30b666474a61a7cdc3dcda254d6da46`

```dockerfile
```

-	Layers:
	-	`sha256:f2c0b73b184aff922d5d57b8434f4cb8fa37b6209567af1615f787728d30083d`  
		Last Modified: Wed, 25 Jun 2025 18:16:38 GMT  
		Size: 2.6 MB (2596462 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5f9ecc04c11b0d02a60846aa2872466c34851527302189bcd49c229e4acd91bc`  
		Last Modified: Wed, 25 Jun 2025 18:16:39 GMT  
		Size: 19.9 KB (19886 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-temurin:8-jdk-ubi9-minimal` - linux; arm64 variant v8

```console
$ docker pull eclipse-temurin@sha256:0ffa0c73979ae162bbf9d4ead1c312df0748f58a387373eac724c7ace427f17f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **119.8 MB (119761744 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f6595155b7c02f0f8f61570b6f7b7b03f418f80443d8b8049324162a0abe2cf`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`

```dockerfile
# Sun, 27 Apr 2025 20:21:59 GMT
LABEL maintainer="Red Hat, Inc."
# Sun, 27 Apr 2025 20:21:59 GMT
LABEL vendor="Red Hat, Inc."
# Sun, 27 Apr 2025 20:21:59 GMT
LABEL url="https://www.redhat.com"
# Sun, 27 Apr 2025 20:21:59 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.6"       distribution-scope="public"
# Sun, 27 Apr 2025 20:21:59 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Sun, 27 Apr 2025 20:21:59 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Sun, 27 Apr 2025 20:21:59 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Sun, 27 Apr 2025 20:21:59 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Sun, 27 Apr 2025 20:21:59 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Sun, 27 Apr 2025 20:21:59 GMT
LABEL io.openshift.expose-services=""
# Sun, 27 Apr 2025 20:21:59 GMT
LABEL io.openshift.tags="minimal rhel9"
# Sun, 27 Apr 2025 20:21:59 GMT
ENV container oci
# Sun, 27 Apr 2025 20:21:59 GMT
COPY dir:dd3dc18ab466569b07043336c84190595a673cf78699fcf70dbf83deddf44d87 in / 
# Sun, 27 Apr 2025 20:21:59 GMT
COPY file:b37d593713ee21ad52a4cd1424dc019a24f7966f85df0ac4b86d234302695328 in /etc/yum.repos.d/. 
# Sun, 27 Apr 2025 20:21:59 GMT
CMD ["/bin/bash"]
# Sun, 27 Apr 2025 20:21:59 GMT
COPY file:0667e9d31385a24c3aef13f2dd9ab6a7b71b3dfcfef5127d3c1e2ea2c838e5cb in /usr/share/buildinfo/content-sets.json 
# Sun, 27 Apr 2025 20:21:59 GMT
LABEL "build-date"="2025-06-09T17:24:02" "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="7e18551b8a7ac3e7aa6347d84b9f0b5c8cc8fe52" "release"="1749489516"
# Sun, 27 Apr 2025 20:21:59 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sun, 27 Apr 2025 20:21:59 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sun, 27 Apr 2025 20:21:59 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Sun, 27 Apr 2025 20:21:59 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en     ;     microdnf clean all # buildkit
# Sun, 27 Apr 2025 20:21:59 GMT
ENV JAVA_VERSION=jdk8u452-b09
# Sun, 27 Apr 2025 20:21:59 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='d8a1aecea0913b7a1e0d737ba6f7ea99059b3f6fd17813d4a24e8b3fc3aee278';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u452-b09/OpenJDK8U-jdk_aarch64_linux_hotspot_8u452b09.tar.gz';          ;;        ppc64le)          ESUM='ff6e0f7fad0f46fea47193b95e4187e294ba69bb9059704f5df9f2fb74125732';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u452-b09/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u452b09.tar.gz';          ;;        x86_64)          ESUM='9448308a21841960a591b47927cf2d44fdc4c0533a5f8111a4b243a6bafb5d27';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u452-b09/OpenJDK8U-jdk_x64_linux_hotspot_8u452b09.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip; # buildkit
# Sun, 27 Apr 2025 20:21:59 GMT
RUN set -eux;     echo "Verifying install ...";     echo "javac -version"; javac -version;     echo "java -version"; java -version;     echo "Complete." # buildkit
# Sun, 27 Apr 2025 20:21:59 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Sun, 27 Apr 2025 20:21:59 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
```

-	Layers:
	-	`sha256:f258ee7f14ce0e3998c50b14ce17a0c0115edefcb69d96c3ef016548422246c8`  
		Last Modified: Mon, 09 Jun 2025 18:09:34 GMT  
		Size: 37.9 MB (37922296 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54c92d528d56d0b425ec1ece8f3484b678fe8fbdfc0181c1023bc51b43374538`  
		Last Modified: Tue, 10 Jun 2025 17:44:06 GMT  
		Size: 28.0 MB (28005980 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c27fdcf0ac78087ad292954cd583f2f96566483816768cff3a85753e5bca5830`  
		Last Modified: Tue, 10 Jun 2025 17:44:18 GMT  
		Size: 53.8 MB (53831027 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a432173bb3f9a0b181bcc220e3f2252084b68c0e3f2824765e89c390e48d99fc`  
		Last Modified: Tue, 10 Jun 2025 17:44:01 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:493dfaa6c9345c47486c857b533c7287cdc922c7785238228331d8d649f4c471`  
		Last Modified: Tue, 10 Jun 2025 17:44:01 GMT  
		Size: 2.3 KB (2315 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:8-jdk-ubi9-minimal` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:305cec87ba8d62061a8aaa11487986fdfbeac36e70c72e90e4fcd816f68832a2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2616462 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3888a92690291ef55293f4c760bd687746d6078534ee97a15795d116558ab4b0`

```dockerfile
```

-	Layers:
	-	`sha256:ce6e6574f110d0f70ede18179df2d1727ff854b4380cbef09291a05e4fdb4e8e`  
		Last Modified: Tue, 10 Jun 2025 18:17:03 GMT  
		Size: 2.6 MB (2596460 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:73f059e45d6a4b482888142bc2d689be6c3a3bc5cd068001356ac2d20e392f7e`  
		Last Modified: Tue, 10 Jun 2025 18:17:04 GMT  
		Size: 20.0 KB (20002 bytes)  
		MIME: application/vnd.in-toto+json

### `eclipse-temurin:8-jdk-ubi9-minimal` - linux; ppc64le

```console
$ docker pull eclipse-temurin@sha256:0e2a23169eb15246a5bc4d1e91e38fc9a28a3e765ce840b219308567195f81c9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **126.2 MB (126189725 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f18fa9644ba1acfc101ac9f604b2f92d83df4643e8695a0a0651533b711aadf8`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`

```dockerfile
# Sun, 27 Apr 2025 20:21:59 GMT
LABEL maintainer="Red Hat, Inc."
# Sun, 27 Apr 2025 20:21:59 GMT
LABEL vendor="Red Hat, Inc."
# Sun, 27 Apr 2025 20:21:59 GMT
LABEL url="https://www.redhat.com"
# Sun, 27 Apr 2025 20:21:59 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.6"       distribution-scope="public"
# Sun, 27 Apr 2025 20:21:59 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Sun, 27 Apr 2025 20:21:59 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Sun, 27 Apr 2025 20:21:59 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Sun, 27 Apr 2025 20:21:59 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Sun, 27 Apr 2025 20:21:59 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Sun, 27 Apr 2025 20:21:59 GMT
LABEL io.openshift.expose-services=""
# Sun, 27 Apr 2025 20:21:59 GMT
LABEL io.openshift.tags="minimal rhel9"
# Sun, 27 Apr 2025 20:21:59 GMT
ENV container oci
# Sun, 27 Apr 2025 20:21:59 GMT
COPY dir:d83abf82dbf4be7abfad8c73a5c54416daede00b99a88ceef5492299e80e8120 in / 
# Sun, 27 Apr 2025 20:21:59 GMT
COPY file:b37d593713ee21ad52a4cd1424dc019a24f7966f85df0ac4b86d234302695328 in /etc/yum.repos.d/. 
# Sun, 27 Apr 2025 20:21:59 GMT
CMD ["/bin/bash"]
# Sun, 27 Apr 2025 20:21:59 GMT
COPY file:0667e9d31385a24c3aef13f2dd9ab6a7b71b3dfcfef5127d3c1e2ea2c838e5cb in /usr/share/buildinfo/content-sets.json 
# Sun, 27 Apr 2025 20:21:59 GMT
LABEL "build-date"="2025-06-24T16:34:39" "architecture"="ppc64le" "vcs-type"="git" "vcs-ref"="69e50e2a07c936e700297091886db408257a857c" "release"="1750782676"
# Sun, 27 Apr 2025 20:21:59 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sun, 27 Apr 2025 20:21:59 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sun, 27 Apr 2025 20:21:59 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Sun, 27 Apr 2025 20:21:59 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en     ;     microdnf clean all # buildkit
# Sun, 27 Apr 2025 20:21:59 GMT
ENV JAVA_VERSION=jdk8u452-b09
# Sun, 27 Apr 2025 20:21:59 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='d8a1aecea0913b7a1e0d737ba6f7ea99059b3f6fd17813d4a24e8b3fc3aee278';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u452-b09/OpenJDK8U-jdk_aarch64_linux_hotspot_8u452b09.tar.gz';          ;;        ppc64le)          ESUM='ff6e0f7fad0f46fea47193b95e4187e294ba69bb9059704f5df9f2fb74125732';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u452-b09/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u452b09.tar.gz';          ;;        x86_64)          ESUM='9448308a21841960a591b47927cf2d44fdc4c0533a5f8111a4b243a6bafb5d27';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u452-b09/OpenJDK8U-jdk_x64_linux_hotspot_8u452b09.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip; # buildkit
# Sun, 27 Apr 2025 20:21:59 GMT
RUN set -eux;     echo "Verifying install ...";     echo "javac -version"; javac -version;     echo "java -version"; java -version;     echo "Complete." # buildkit
# Sun, 27 Apr 2025 20:21:59 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Sun, 27 Apr 2025 20:21:59 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
```

-	Layers:
	-	`sha256:8374cdcea99a5f341eb5030b5ece88085798cef7a6357cfcc46f8db2ab3dcbc9`  
		Last Modified: Tue, 24 Jun 2025 18:09:28 GMT  
		Size: 44.0 MB (44041398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5872ee8c9a0f398b2cc0631abe2164a5c0397d35045d1f9af834e8f8f4da60c2`  
		Last Modified: Wed, 25 Jun 2025 17:54:51 GMT  
		Size: 30.0 MB (29977285 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e30567529ed8ba7cf1aa1fe22bb2e18a34b6a842c87ee9edc17699fc86245612`  
		Last Modified: Wed, 25 Jun 2025 17:54:56 GMT  
		Size: 52.2 MB (52168600 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c00db75dd70d27c991465d78951019bb0bf48ff1376711cf100d7227488281a4`  
		Last Modified: Wed, 25 Jun 2025 17:54:47 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea5fee28c835d628dbdc5c5023050174ba606350a75461181842779b5978f862`  
		Last Modified: Wed, 25 Jun 2025 17:54:47 GMT  
		Size: 2.3 KB (2316 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eclipse-temurin:8-jdk-ubi9-minimal` - unknown; unknown

```console
$ docker pull eclipse-temurin@sha256:e840f2d485fe6b7c8db0862bb92316038f8907b779ada561903d5ca1809e3a43
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2615069 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:25935d2400f2df268887d37f4c8bdf627c6f0ee76c2a99abf939440b37e54643`

```dockerfile
```

-	Layers:
	-	`sha256:913446e73e2c5ba9dfc22f77f9d7730e9c0a1ecac1a38472d991439b5539af03`  
		Last Modified: Wed, 25 Jun 2025 18:16:57 GMT  
		Size: 2.6 MB (2595149 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dfd39f53bb67e6930bf7b60994c0d4e1ce320f29e353f97f917132877bff4a17`  
		Last Modified: Wed, 25 Jun 2025 18:16:57 GMT  
		Size: 19.9 KB (19920 bytes)  
		MIME: application/vnd.in-toto+json
